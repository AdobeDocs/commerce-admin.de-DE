---
title: '[!DNL Inventory Management] CLI-Referenz'
description: Erfahren Sie mehr über die Befehle, die das  [!DNL Inventory Management] -Modul zum Verwalten von Inventardaten und Konfigurationseinstellungen bereitstellt.
exl-id: d92dffce-94a1-443c-8c72-98fecbbd5320
level: Experienced
feature: Inventory, Configuration
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/de/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
source-git-commit: b4623ada788d44f4628930dcf5dfcb51dd88ee3a
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 0%

---

# [!DNL Inventory Management] CLI-Referenz

[!DNL Inventory Management] bietet Befehle zum Verwalten von Inventardaten und Konfigurationseinstellungen.

Zu diesen Befehlen gehören:

- Überprüfen und Beheben von Reservierungsinkonsistenzen, die sich auf die Verkaufsmenge auswirken
- Hinzufügen von Geocodes für den Distance Priority Algorithmus

## Beheben von Reservierungsinkonsistenzen

Bei Reservierungen wird eine Verkaufsmenge für Produkt-SKUs pro Lager zurückgestellt. Wenn Sie eine Bestellung versenden, Produkte hinzufügen, stornieren oder zurückerstatten, geben Sie eine Ausgleichsreservierung ein, um diese Sperren zu platzieren oder zu löschen.

[!DNL Inventory Management] bietet zwei Befehle zum Überprüfen und Beheben von Reservierungsinkonsistenzen:

- [`inventar:reservation:list-inconsistences`](#list-inconsistencies-command)
- [`inventar:reservation:create-kompensations`](#create-compensations-command)

### Ursachen für Reservierungsinkonsistenzen

[!DNL Inventory Management] generiert Reservierungen für wichtige Ereignisse:

- Auftragserteilung (Erstreservierung)
- Versand bestellen (Ausgleichsreservierung)
- Rückzahlungsanordnung oder Ausstellung einer Gutschrift (Ausgleichsvorbehalt)
- Stornierung der Bestellung (Ausgleichsreservierung)

Reservierungsinkonsistenzen können auftreten, wenn:

- [!DNL Inventory Management] verliert die ursprüngliche Reservierung und gibt zu viele Reservierungsentschädigungen ein (überkompensiert und führt zu inkonsistenten Beträgen)
- [!DNL Inventory Management] platziert die ursprüngliche Reservierung korrekt, verliert jedoch die Ausgleichsreservierung.

Sie können Reservierungen in der `inventory_reservation` Tabelle manuell überprüfen und überprüfen.

Die folgenden Konfigurationen und Ereignisse können zu Inkonsistenzen bei der Reservierung führen:

- **Upgrade auf 2.3.x mit Bestellungen, die sich noch nicht im endgültigen Status befinden (abgeschlossen, storniert oder geschlossen).** [!DNL Inventory Management] erstellt Ausgleichsreservierungen für diese Bestellungen, aber er nimmt die ursprüngliche Reservierung, die von der Verkaufsmenge abgezogen wird, nicht ein oder verfügt nicht über diese. Es wird empfohlen, nach dem Upgrade auf Adobe Commerce oder Magento Open Source v2.3.x von 2.1.x oder 2.2.x diese Befehle zu verwenden. Wenn Sie ausstehende Bestellungen haben, aktualisieren die Befehle Ihre Verkaufsmenge und Reservierungen für Verkauf und Bestellabwicklung korrekt.
- **Sie verwalten kein Lager und ändern Sie diese Konfiguration später.** Sie können 2.3.x verwenden, wobei **[!UICONTROL Manage Stock]** in der Konfiguration auf `No` gesetzt ist. [!DNL Commerce] platziert keine Reservierungen bei Bestell- und Versandveranstaltungen. Wenn Sie später die **[!UICONTROL Manage Stock]**-Konfiguration aktivieren und einige Bestellungen erstellt werden, wird die Verkaufsmenge bei der Bearbeitung und Ausführung dieser Bestellung durch eine Ausgleichsreservierung beschädigt.
- **Sie weisen das Lager für eine Website neu zu, während Bestellungen an diese Website gesendet werden**. Die Erstreservierung geht für den Anfangsbestand ein, und alle Ausgleichsreservierungen gehen in den neuen Bestand ein.
- **Die Gesamtzahl aller Reservierungen wird möglicherweise nicht auf `0` aufgelöst.** Alle Reservierungen im Umfang einer Bestellung in einem endgültigen Status (abgeschlossen, storniert, geschlossen) sollten auf `0` aufgelöst werden, wobei alle verkaufbaren Lagerbestände gelöscht werden.

### Befehl „Inkonsistenzen auflisten“

Der Befehl `list-inconsistencies` erkennt und listet alle Reservierungsinkonsistenzen auf. Verwenden Sie die Befehlsoptionen, um nur abgeschlossene oder unvollständige Bestellungen oder alle Bestellungen zu überprüfen.

```bash
bin/magento inventory:reservation:list-inconsistencies
```

Befehlsoptionen:

- `-c`, `--complete-orders` - Gibt Inkonsistenzen für abgeschlossene Bestellungen zurück. Falsche Reservierungen können für abgeschlossene Bestellungen weiterhin zurückgestellt werden.
- `-i`, `--incomplete-orders` - Gibt Inkonsistenzen bei unvollständigen Bestellungen zurück (teilweise versandt, nicht versandt). Falsche Reservierungen können zu viel oder zu wenig verkaufsfähige Menge für die Bestellungen enthalten.
- `-b`, `--bunch-size` - Legt fest, wie viele Bestellungen gleichzeitig geladen werden.
- `-r`, `--raw` - Rohausgabe.

Antworten, die `-r` Rückgabe im `<ORDER_INCREMENT_ID>:<SKU>:<QUANTITY>:<STOCK-ID>`-Format verwenden:

- Die Bestell-ID gibt den Umfang der Inkonsistenz an.
- Die SKU zeigt das Produkt mit der Inkonsistenz an.
- Menge legt den Betrag fest, der für die Reservierungskompensation eingegeben werden soll.
- Die Lagerkennung definiert den Umfang für den Lagerbestand, der die Reservierungen zur Berechnung der Verkaufsmenge verwendet.

Beispiele:

```bash
bin/magento inventory:reservation:list-inconsistencies

Inconsistencies found on following entries:
Order 172:
- Product bike-123 should be compensated by +2.000000 for stock 1
```

```bash
bin/magento inventory:reservation:list-inconsistencies -r

172:bike-123:+2.000000:1
```

Wenn keine Probleme gefunden werden, gibt diese Nachricht zurück: Es wurden keine Bestellinkonsistenzen gefunden.

### Kompensationsbefehl erstellen

Der Befehl `create-compensations` erstellt Ausgleichsreservierungen. Je nach Problem werden neue Reservierungen erstellt, um die verkaufsfähige Menge entweder zu platzieren oder freizugeben.

Um Reservierungen zu erstellen, geben Sie Kompensationen mithilfe des Formats `<ORDER_INCREMENT_ID>:<SKU>:<QUANTITY>:<STOCK-ID>` an, z. B. `172:bike-123:+2.000000:1`.

```bash
bin/magento inventory:reservation:create-compensations
```

Befehlsoption:

- `-r`, `--raw` - Gibt die Rohausgabe zurück.

Wenn das Format der Anfrage falsch ist, wird die folgende Meldung angezeigt:

```
Error while parsing argument "your_incorrect_format_argument". Given argument does not match pattern "/(?P<increment_id>.*):(?P<sku>.*):(?P<quantity>.*):(?P<stock_id>.*)/".
```

Wenn der Befehl Reservierungen erstellt, werden Meldungen angezeigt, die die Aktualisierungen nach SKU, Bestellung und Lager angeben.

```bash
bin/magento inventory:reservation:create-compensations 172:bike-123:+2.000000:1

Following reservations were created:
- Product bike-123 was compensated by +2.000000 for stock 1
```

Wenn die SKU für einen Ausgleichseintrag Leerzeichen enthält, setzen Sie die SKU in Anführungszeichen.

```bash
bin/magento inventory:reservation:create-compensations 172:"bike 123":+2.000000:1
```

### Inkonsistenzen erkennen und Kompensationen erstellen

Sie können Inkonsistenzen erkennen und sofort Kompensationen erstellen, indem Sie einen senkrechten Strich verwenden, um sowohl den `list-inconsistencies` als auch den `create-compensations` auszuführen. Verwenden Sie die `-r` Befehlsoption zum Generieren und Senden der Rohdaten an `create-compensations`.

```bash
bin/magento inventory:reservation:list-inconsistencies -r | bin/magento inventory:reservation:create-compensations
```

Beispielantwort:

```bash
bin/magento inventory:reservation:list-inconsistencies -r | bin/magento inventory:reservation:create-compensations
```

```
Following reservations were created:
- Product bike-123 was compensated by +2.000000 for stock 1
- Product bikehat-456 was compensated by +1.000000 for stock 1
```

Führen Sie nach Abschluss der Aktualisierungen den Listenbefehl zur Überprüfung aus:

```bash
bin/magento inventory:reservation:list-inconsistencies -r
```

```
No order inconsistencies were found.
```

Sie können die Befehle auch über Pipes weiterleiten, um Inkonsistenzen zu erkennen und Kompensationen für nur unvollständige (`-i`) oder vollständige (`-c`) Bestellungen zu erstellen.

```bash
bin/magento inventory:reservation:list-inconsistencies -r -i | bin/magento inventory:reservation:create-compensations
```

```bash
bin/magento inventory:reservation:list-inconsistencies -r -c | bin/magento inventory:reservation:create-compensations
```

## Geocodes importieren

[!DNL Inventory Management] bietet den [Distance Priority Algorithmus](distance-priority-algorithm.md), der dabei hilft, die beste Option für den Versand einer Voll- oder Teilbestellung zu ermitteln. Der Algorithmus verwendet GPS-Informationen oder Geocodes, um den Abstand zwischen der Quelle (einem Lager oder einem anderen physischen Standort) jedes Artikels in einer Bestellung und der Lieferadresse zu berechnen. Basierend auf diesen Ergebnissen empfiehlt der Algorithmus, welche Quelle verwendet werden sollte, um jedes Element in der Bestellung auszuliefern.

Der Händler wählt den Anbieter der zur Berechnung der Entfernungen erforderlichen GPS- oder Geocode-Daten aus:

- **Google MAP** verwendet [Google Maps Platform](https://mapsplatform.google.com/)-Services, um die Entfernung und die Zeit zwischen der Versandzieladresse und den Quellorten zu berechnen. Diese Option erfordert einen Google-Abrechnungsplan und kann über Google Gebühren verursachen.

- **Offline-Berechnung** Berechnet die Entfernung anhand von Daten, die von [geonames.org](https://www.geonames.org/) heruntergeladen und mit einem Befehl in Commerce importiert wurden. Diese Option ist kostenlos.

So importieren Sie Geocodes für Offline-Berechnungen:

Geben Sie den folgenden Befehl mit einer durch Leerzeichen getrennten Liste der [ISO-3166 alpha2-Länder-Codes](https://www.geonames.org/countries/) ein:

```bash
bin/magento inventory-geonames:import <country code> <country code> ...
```

Beispiel:

```bash
bin/magento inventory-geonames:import us ca gb de
```

Das System lädt die Geocode-Daten herunter und importiert sie in Ihre Datenbank und zeigt dann die `Importing <country code>: OK` an.
