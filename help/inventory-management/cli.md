---
title: '[!DNL Inventory Management] CLI-Referenz'
description: Erfahren Sie mehr über die Befehle des [!DNL Inventory Management] Moduls zum Verwalten von Bestandsdaten und Konfigurationseinstellungen.
exl-id: d92dffce-94a1-443c-8c72-98fecbbd5320
level: Experienced
feature: Inventory, Configuration
source-git-commit: 53c3b6c9fa9c152e6619528a43580b0acc71a2a5
workflow-type: tm+mt
source-wordcount: '826'
ht-degree: 0%

---

# [!DNL Inventory Management] CLI-Referenz

[!DNL Inventory Management] stellt Befehle zum Verwalten von Bestandsdaten und Konfigurationseinstellungen bereit.

Zu diesen Befehlen gehören:

- Kontrolle und Behebung von Inkonsistenzen, die sich auf die Verkaufsmenge auswirken
- Hinzufügen von Geocodes für den Distance Priority-Algorithmus

## Beheben von Inkonsistenzen

Bei Reservierungen wird eine Verkaufsmenge für Produkt-SKUs pro Lager aufbewahrt. Wenn Sie eine Bestellung versenden, Produkte hinzufügen, stornieren oder zurückerstatten, treten Entschädigungsreservierungen ein, um diese Geschäfte zu tätigen oder zu löschen.

[!DNL Inventory Management] stellt zwei Befehle zum Überprüfen und Auflösen von Reservierungsinkonsistenzen bereit:

- [&quot;inventory:reservation:list-inkonsistences&quot;](#list-inconsistencies-command)
- [`inventory:reservation:create-kompenations`](#create-compensations-command)

### Gründe für Unstimmigkeiten bei den Reservierungen

[!DNL Inventory Management] generiert Reservierungen für wichtige Ereignisse:

- Bestellplatzierung (Erstreservierung)
- Auftragsversand (Reservierungsbestätigung)
- Rückerstattungsantrag oder Ausstellung eines Kreditmemo (Reservierung der Ausgleichszahlungen)
- Stornierung der Bestellung (Reservierung)

Reservierungsinkonsistenzen können auftreten, wenn:

- [!DNL Inventory Management] verliert die ursprüngliche Reservierung und gibt zu viele Reservierungsausgleichszahlungen ein (Überkompensierung und zu inkonsistenten Beträgen führt).
- [!DNL Inventory Management] platziert die anfängliche Reservierung korrekt, verliert jedoch die Reservierungen.

Sie können die Reservierungen in der Tabelle `inventory_reservation` manuell überprüfen und überprüfen.

Die folgenden Konfigurationen und Ereignisse können zu Reservierungsinkonsistenzen führen:

- **Aktualisieren Sie auf 2.3.x mit Bestellungen, die sich nicht im finalen Zustand befinden (Complete, Cancelled oder Closed).** [!DNL Inventory Management] führt zu Ausgleichsreservierungen für diese Bestellungen, aber es tritt nicht ein oder hat nicht die ursprüngliche Reservierung, die von der verkaufbaren Menge abgezogen wird. Es wird empfohlen, diese Befehle nach der Aktualisierung auf Adobe Commerce oder Magento Open Source v2.3.x von 2.1.x oder 2.2.x zu verwenden. Wenn Sie ausstehende Bestellungen haben, aktualisieren die Befehle Ihre Verkaufsmenge und Reservierungen für den Vertrieb und die Bestellabwicklung korrekt.
- **Sie verwalten kein Lager und ändern diese Konfiguration später.** Sie können mit der Verwendung von 2.3.x beginnen, wobei **[!UICONTROL Manage Stock]** in der Konfiguration auf `No` gesetzt ist. [!DNL Commerce] stellt keine Reservierungen bei Bestellplatzierungs- und Versandereignissen auf. Wenn Sie später die **[!UICONTROL Manage Stock]** -Konfiguration aktivieren und einige Bestellungen erstellt werden, wird die Salable Qty bei der Bearbeitung und Erfüllung dieser Bestellung mit einer Reservierung beschädigt.
- **Sie weisen den Stock für eine Website zu, während Bestellungen an diese Website gesendet werden**. Die Erstreservierung wird für das Anfangsbestand und alle Reservierungen für die Entschädigung in das neue Lager eingetragen.
- **Die Summe aller Reservierungen darf nicht auf `0` aufgelöst werden.** Alle Vorbehalte im Rahmen einer Bestellung in einem endgültigen Zustand (Complete, Cancelled, Closed) sollten auf `0` aufgelöst werden, wodurch alle verkaufbaren Mengen gelöscht werden.

### Inkonsistenzen auflisten, Befehl

Der Befehl `list-inconsistencies` erkennt und listet alle Reservierungsinkonsistenzen auf. Verwenden Sie die Befehlsoptionen, um nur abgeschlossene oder unvollständige Bestellungen oder alle zu überprüfen.

```bash
bin/magento inventory:reservation:list-inconsistencies
```

Befehlsoptionen:

- `-c`, `--complete-orders` - Gibt Inkonsistenzen für abgeschlossene Bestellungen zurück. Für abgeschlossene Bestellungen können noch falsche Vorbehalte bestehen.
- `-i`, `--incomplete-orders` - Gibt Inkonsistenzen für unvollständige Bestellungen zurück (teilweise versandt, unversandt). Falsche Reservierungen können zu viel oder zu wenig verkaufbare Menge für die Bestellungen enthalten.
- `-b`, `--bunch-size` - Definiert, wie viele Bestellungen gleichzeitig geladen werden.
- `-r`, `--raw` - Rohausgabe.

Antworten mit `-r` geben im Format `<ORDER_INCREMENT_ID>:<SKU>:<QUANTITY>:<STOCK-ID>` zurück:

- Die Bestell-ID gibt den Umfang der Inkonsistenz an.
- Die SKU zeigt das Produkt mit der Inkonsistenz an.
- Die Menge legt den Betrag fest, der für die Reservierungsentschädigung einzutragen ist.
- Kennung des Lagers definiert den Umfang des Bestands, der die Reserven zur Berechnung der Verkaufsmenge verwendet.

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

Wenn keine Probleme gefunden werden, gibt diese Meldung zurück: Es wurden keine Bestellinkonsistenzen gefunden.

### Ausgleichszahlungen erstellen, Befehl

Der Befehl `create-compensations` erzeugt Ausgleichsreservierungen. Je nach Problem werden neue Reservierungen erstellt, um entweder eine Verkaufsmenge zu platzieren oder freizugeben.

Um Reservierungen zu erstellen, stellen Sie Ausgleichszahlungen im Format `<ORDER_INCREMENT_ID>:<SKU>:<QUANTITY>:<STOCK-ID>` wie `172:bike-123:+2.000000:1` bereit.

```bash
bin/magento inventory:reservation:create-compensations
```

Befehlsoption:

- `-r`, `--raw` - Gibt die Rohausgabe zurück.

Wenn das Format der Anforderung falsch ist, wird die folgende Meldung angezeigt:

```
Error while parsing argument "your_incorrect_format_argument". Given argument does not match pattern "/(?P<increment_id>.*):(?P<sku>.*):(?P<quantity>.*):(?P<stock_id>.*)/".
```

Wenn der Befehl Reservierungen erstellt, werden Meldungen angezeigt, die die Aktualisierungen nach SKU, Bestellung und Lager angeben.

```bash
bin/magento inventory:reservation:create-compensations 172:bike-123:+2.000000:1

Following reservations were created:
- Product bike-123 was compensated by +2.000000 for stock 1
```

Wenn die SKU für einen Kompensationseintrag Leerzeichen enthält, fügen Sie die SKU in Anführungszeichen ein.

```bash
bin/magento inventory:reservation:create-compensations 172:"bike 123":+2.000000:1
```

### Inkonsistenzen erkennen und Ausgleichszahlungen erstellen

Sie können Inkonsistenzen erkennen und sofort Ausgleichszahlungen erstellen, indem Sie einen senkrechten Strich verwenden, um sowohl die `list-inconsistencies` als auch die `create-compensations` auszuführen. Verwenden Sie die Befehlsoption `-r` , um die Rohdaten zu generieren und an `create-compensations` zu senden.

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

Führen Sie nach Abschluss der Aktualisierungen den Listenbefehl aus, um Folgendes zu überprüfen:

```bash
bin/magento inventory:reservation:list-inconsistencies -r
```

```
No order inconsistencies were found.
```

Sie können auch die Befehle zum Erkennen von Inkonsistenzen und Erstellen von Ausgleichszahlungen nur für unvollständige (`-i`) oder vollständige (`-c`) Bestellungen senden.

```bash
bin/magento inventory:reservation:list-inconsistencies -r -i | bin/magento inventory:reservation:create-compensations
```

```bash
bin/magento inventory:reservation:list-inconsistencies -r -c | bin/magento inventory:reservation:create-compensations
```

## Importieren von Geocodes

[!DNL Inventory Management] bietet den [Distance Priority-Algorithmus](distance-priority-algorithm.md), der bei der Bestimmung der besten Option für den Versand einer vollständigen oder teilweisen Bestellung hilft. Der Algorithmus verwendet GPS-Informationen oder Geocodes, um den Abstand zwischen der Quelle (einem Lager oder einem anderen physischen Standort) jedes Artikels in einer Bestellung und der Lieferadresse zu berechnen. Basierend auf diesen Ergebnissen empfiehlt der Algorithmus, welche Quelle zum Versand der einzelnen Elemente in der Reihenfolge verwendet werden soll.

Der Händler wählt den Anbieter der GPS- oder Geocode-Daten aus, die zur Berechnung der Entfernungen erforderlich sind:

- **Google MAP** verwendet [Google Maps Platform](https://mapsplatform.google.com/)-Dienste, um den Abstand und die Zeit zwischen der Lieferzieladresse und den Quellspeicherorten zu berechnen. Für diese Option ist ein Google-Abrechnungsplan erforderlich, für den möglicherweise Gebühren über Google anfallen.

- **Offline calculate** berechnet die Entfernung mithilfe von Daten, die von [geonames.org](https://www.geonames.org/) heruntergeladen und mit einem Befehl in Commerce importiert wurden. Diese Option ist kostenlos.

So importieren Sie Geocodes für die Offline-Berechnung:

Geben Sie den folgenden Befehl mit einer durch Leerzeichen getrennten Liste von [ISO-3166 Alpha2-Ländercodes](https://www.geonames.org/countries/) ein:

```bash
bin/magento inventory-geonames:import <country code> <country code> ...
```

Beispiel:

```bash
bin/magento inventory-geonames:import us ca gb de
```

Das System lädt die Geocode-Daten herunter und importiert sie in Ihre Datenbank und zeigt dann die Meldung `Importing <country code>: OK` an.
