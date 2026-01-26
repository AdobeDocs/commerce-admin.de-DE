---
title: Source-Algorithmen und -Reservierungen
description: Erfahren Sie mehr über den Source-Auswahlalgorithmus und Reservierungssysteme, die im Hintergrund ausgeführt werden, um Ihre Verkaufsmengen auf dem neuesten Stand zu halten.
exl-id: dcd63322-fb4c-4448-b6e7-0c54350905d7
feature: Inventory, Shipping/Delivery
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '2196'
ht-degree: 0%

---

# Source-Algorithmen und -Reservierungen

Das Herzstück von [!DNL Inventory Management] verfolgt jedes verfügbare Produkt virtuell und auf Lager und Vorrat. Die Source-Auswahlalgorithmus- und Reservierungssysteme werden im Hintergrund ausgeführt. So bleiben Ihre Verkaufsmengen auf dem neuesten Stand, der Checkout ist frei von Kollisionen und es werden Lieferoptionen empfohlen.

>[!NOTE]
>
>Informationen zur programmgesteuerten Arbeit mit dem [&#x200B; finden &#x200B;](https://developer.adobe.com/commerce/php/development/framework/inventory-management/) in [!DNL Inventory Management] Entwicklerdokumentation.

## Source-Auswahlalgorithmus

Der Source-Auswahlalgorithmus (SSA) analysiert und bestimmt die beste Übereinstimmung für Quellen und Versand anhand der Prioritätsreihenfolge der in einem Lager konfigurierten Quellen. Beim Versand der Bestellung liefert der Algorithmus eine empfohlene Liste der Quellen, verfügbaren Mengen und Beträge, die entsprechend dem ausgewählten Algorithmus abgezogen werden können. [!DNL Inventory Management] bietet einen Prioritätsalgorithmus und unterstützt Erweiterungen für neue Optionen.

Mit mehreren Bezugsstandorten, globalen Kunden und Spediteuren mit verschiedenen Versandoptionen und -gebühren kann es schwierig sein, Ihr tatsächliches verfügbares Inventar zu kennen und die beste Versandoption zu finden. SSA erledigt die Arbeit für Sie, von der Verfolgung der verkäuflichen Lagermengen über alle Quellen hinweg bis hin zur Berechnung und Abgabe von Empfehlungen für Sendungen.

**Inventar nachverfolgen** - Mithilfe von Lagern und Quellen prüft die SSA den Vertriebskanal eingehender Produktanfragen und ermittelt den verfügbaren Bestand:

- Berechnet die aggregierte virtuelle Verkaufsmenge aller zugewiesenen Quellen pro Lager: aggregates Menge - Nicht vorrätiger Schwellenwert pro Quelle
- Subtrahiert den nicht vorrätigen Schwellenbetrag von der verkaufsfähigen Menge, um einen Überverkauf zu verhindern
- Reserviert Lagermengen bei der Bestellübermittlung, abzüglich Lagerbestand bei Auftragsverarbeitung und Versand
- Unterstützt Nachbestellungen mit erweiterten Optionen für negative Schwellenwerte

**Sendungen verwalten** - Der Algorithmus hilft bei der Verarbeitung und Lieferung von Bestellungen. Sie können den Algorithmus ausführen, um Empfehlungen zu den besten Quellen für den Versand des Produkts zu erhalten, oder die Auswahl überschreiben, um:

- Versand von Teilsendungen, wobei nur wenige Produkte von bestimmten Standorten gesendet werden und die gesamte Bestellung später abgeschlossen wird
- Versand der gesamten Bestellung aus einer Quelle
- Sendungen über mehrere Quellen in verschiedenen Mengen aufteilen und so einen ausgewogenen Bestand über alle Lager und Lager halten

SSA ist erweiterbar für Support von Drittanbietern und benutzerdefinierte Algorithmen zur Empfehlung kosteneffizienter Sendungen.

>[!NOTE]
>
>SSA funktioniert für virtuelle und herunterladbare Produkte unterschiedlich, was möglicherweise keine Versandkosten verursacht. In diesen Fällen führt das System den Algorithmus implizit aus, wenn es Rechnungen erstellt, und verwendet immer die vorgeschlagenen Ergebnisse. Sie können diese Ergebnisse nicht für virtuelle und herunterladbare Produkte anpassen.

### Source-Prioritätsalgorithmus

Benutzerdefinierte Lager enthalten eine zugewiesene Liste von Quellen für den Verkauf und Versand des verfügbaren Produktbestands über Ihre Storefront. Der Source-Prioritätsalgorithmus verwendet die Reihenfolge der zugeordneten Bezugsquellen im Lager, um beim Fakturieren und Versand der Bestellung Produktabzüge pro Bezugsquelle zu empfehlen.

Beim Ausführen des Algorithmus:

- Durchläuft die konfigurierte Quellreihenfolge auf der Lagerebene, beginnend oben.
- Empfiehlt je nach Bestellung in der Liste, verfügbarer Menge und bestellter Menge eine zu liefernde Menge sowie eine zu beschaffende Menge pro Produkt
- Fahren Sie in der Liste nach unten, bis die Bestellanlieferung ausgefüllt ist
- Deaktivierte Quellen werden übersprungen, wenn sie in der Liste gefunden wurden

Zum Konfigurieren, Zuweisen und Sortieren von Quellen zu einem benutzerdefinierten Lager. Siehe [Priorisieren von Quellen für einen Bestand](stocks-prioritize-sources.md).

Im folgenden Beispiel werden die zugeordneten Quellen in der Reihenfolge, die verfügbare Menge und die empfohlene Quelle und der empfohlene Betrag beschrieben, die abgezogen und versendet werden sollen. Die Top-Quelle ist ein Drop-Shipper in Großbritannien mit einer verfügbaren Menge von 240.

![Beispiel SSA-Empfehlungen für ein Mountainbike](assets/ssa-sources-example.png){width="600" zoomable="yes"}

### Algorithmus für Abstandspriorität

Der Distance Priority Algorithm vergleicht den Standort der Versandzieladresse mit den Quellorten, um die nächstgelegene Quelle für die Erfüllung von Sendungen zu ermitteln. Die Entfernung kann durch die physische Entfernung oder die Zeit bestimmt werden, die auf Reisen von einem Ort zum anderen verbracht wurde, indem importierte Datenbankstandorte oder Google-Richtungen (Fahren, Gehen oder Fahrradfahren) verwendet werden.

Sie haben zwei Möglichkeiten, die Entfernung und die Zeit zu berechnen, um die nächstgelegene Quelle für die Sendungserfüllung zu finden:

- **Google MAP** - Verwendet [Google Maps Platform](https://cloud.google.com/maps-platform/)-Services zur Berechnung der Entfernung und Zeit zwischen der Versandzieladresse und den Quellorten (Adresse und GPS-Koordinaten). Diese Option verwendet den Breiten- und Längengrad der Quelle. Ein Google-API-Schlüssel ist erforderlich, wenn [Geocoding-](https://developers.google.com/maps/documentation/geocoding/start)) und [Distanzmatrix-](https://developers.google.com/maps/documentation/distance-matrix/start) aktiviert sind. Diese Option erfordert einen Google-Abrechnungsplan und kann über Google Gebühren verursachen.

- **Offline-Berechnung** - Berechnet die Entfernung anhand heruntergeladener und importierter Geocode-Daten, um die Quelle zu ermitteln, die der Versandzieladresse am nächsten liegt. Diese Option verwendet die Länder-Codes der Lieferadresse und der Quelle. Um diese Option zu konfigurieren, benötigen Sie möglicherweise die Unterstützung eines Entwicklers, um Geocodes zunächst über eine Befehlszeile herunterzuladen und zu importieren.

Wählen Sie zur Konfiguration Konfigurationen aus und führen Sie zusätzliche Schritte durch, z. B. den Google-API-Schlüssel oder das Herunterladen von Versanddaten. Siehe [Konfigurieren des Distance Priority Algorithm](distance-priority-algorithm.md).

### Benutzerdefinierte Algorithmen

[!DNL Commerce] unterstützt benutzerdefinierte Entwicklung und Erweiterungen zum Hinzufügen alternativer Algorithmen, um Quellen zu priorisieren. Sie können beispielsweise einen Prioritätsalgorithmus basierend auf der Geografie und einen anderen basierend auf den Lagerkosten oder einem Kundenattribut verwenden. Wenn sich die Lagerkosten ändern, kann Ihre Implementierung die Algorithmen einfach ändern, um die niedrigsten Kosten sicherzustellen.

## Vorbehalte

Anstatt sofort Produktinventarmengen abzuziehen oder hinzuzufügen, behalten Reservierungen Lagerbeträge bis zum Versand oder zur Stornierung von Bestellungen. Reservierungen funktionieren vollständig im Backend, um Ihre Verkaufsmenge automatisch auf Lagerebene zu aktualisieren.

>[!NOTE]
>
>[!BADGE Nur PaaS]{type=Informative url="https://experienceleague.adobe.com/de/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."} Für die Reservierungsfunktion muss die `inventory.reservations.updateSalabilityStatus` Nachrichtenwarteschlange kontinuierlich ausgeführt werden. Um zu überprüfen, ob es ausgeführt wird, verwenden Sie den `bin/magento queue:consumers:list`. Wenn der Nachrichtenwarteschlangenbenutzer nicht aufgeführt ist, starten Sie ihn: `bin/magento queue:consumers:start inventory.reservations.updateSalabilityStatus`.

### Reservierungen bestellen

Reservierungen für Lagermengen, die bei der Auftragserteilung von der Verkaufsmenge abgezogen werden, werden zurückgestellt. Die Reservierungen werden auf Lagerebene durchgeführt und zählen mit den Mengen, bis die Bestellung fakturiert und versendet, storniert wird usw. Beim Versand der Bestellung können Sie die SSA-Empfehlungen verwenden oder manuell Mengenabzüge pro Quelle eingeben. Beim Versand werden die Reservierungen automatisch gelöscht und die Menge abgezogen. Die verkaufbare Menge berechnet für den Bestand mit einer aktualisierten Menge und allen im System verbleibenden Reservierungsbeträgen neu.

Das folgende Diagramm hilft bei der Definition des Prozesses der Reservierung während einer Bestellung und bis zum Versand.

![Reservierungen von Bestellung bis Lieferung](assets/diagram-quantity.png){width="600" zoomable="yes"}

Ein Kunde reicht eine Bestellung ein. [!DNL Commerce] prüft die aktuelle Lagerverkaufsmenge. Wenn auf Lagerebene genügend Lagerbestand vorhanden ist, wird eine Reservierung eingetreten, die einen temporären Sperrstatus für die Produkt-SKU (für diesen Bestand) anlegt, und die verkaufbare Menge wird neu berechnet.

Nachdem Sie die Bestellung fakturiert haben, bestimmen Sie die Produktbeträge, die Sie von Ihren Quellen abziehen und versenden möchten. Die Lieferung wird verarbeitet und von einer oder mehreren ausgewählten Quellen an den Kunden gesendet. Die Mengen werden automatisch von der Quellinventarmenge abgezogen und die Reservierungen werden gelöscht. Umfassende Details und Beispiele finden Sie [Über den Bestellstatus und Reservierungen](order-status.md).

## Reservierungsberechnungen

Das System erstellt eine Reservierung für jedes Produkt, wenn die folgenden Ereignisse eintreten:

- Ein Kunde oder Händler gibt eine Bestellung auf.
- Ein Kunde oder Händler storniert eine Bestellung ganz oder teilweise.
- Der Händler erstellt eine Sendung für ein physisches Produkt.
- Der Händler erstellt eine Rechnung für ein virtuelles oder herunterladbares Produkt.
- Der Händler gibt eine Gutschrift aus.

Reservierungen sind reine Anlagenvorgänge, die einem Ereignisprotokoll ähneln. Der ursprünglichen Reservierung wird ein negativer Mengenwert zugewiesen. Alle nachfolgenden Reservierungen, die bei der Verarbeitung der Bestellung erstellt wurden, sind positive Werte. Wenn die Bestellung abgeschlossen ist, ist die Summe aller Reservierungen für das Produkt 0.

Bevor das System eine Reservierung als Antwort auf eine neue Bestellung ausstellen kann, bestimmt es, ob genügend verkaufbare Artikel vorhanden sind, um die Bestellung zu erfüllen. Die folgenden Mengen fließen in die Berechnung ein:

- **LagerArtikel Menge**. Die Lagerartikelmenge ist die aggregierte Lagermenge aus allen physischen Quellen für den aktuellen Verkaufskanal. Betrachten wir ein Beispiel, bei dem die Quelle von Baltimore 20 Einheiten eines Produkts enthält, die Quelle von Austin 25 Einheiten desselben Produkts enthält und die Quelle von Reno 10. Wenn alle diese Quellen mit Lager A verknüpft sind, beträgt die StockItem-Anzahl für dieses Produkt 55 (20 + 25 + 10). (Wenn Artikel versendet werden, aktualisiert der Inventar-Indexer die verfügbaren Mengen an jeder Quelle.)

- **Ausstehende Reservierungen**. Das System summiert alle anfänglichen Reservierungen, die nicht kompensiert wurden. Diese Zahl ist immer negativ. Wenn Kunde A eine Reservierung für zehn Artikel hat und Kunde B eine Reservierung für Artikel 5, dann ausstehende Reservierungen für die Produktsumme -15.

Daher kann der Händler eine eingehende Bestellung erfüllen, solange der Kunde weniger als 40 (55 + -15) Einheiten bestellt.

Wenn Sie die Verarbeitung einer Bestellung abgeschlossen haben (abgeschlossen, storniert, geschlossen), sollten alle Reservierungen im Umfang dieser Bestellung auf `0` aufgelöst werden. Dadurch werden alle Lagerbestände für die verkaufsfähige Menge gelöscht.

>[!NOTE]
>
>Nachbestellungen (mit Schwellenwerten für nicht vorrätige Artikel) und Benachrichtigungen bei einer Menge unterhalb des Schwellenwerts wirken sich auch auf die Berechnung von Verkaufsmengen aus, sie sind jedoch nicht Gegenstand dieses Themas. Weitere Informationen zu diesen Einstellungen finden Sie unter [Konfigurieren [!DNL Inventory Management]](./configuration.md).

## Reservierungsobjekte

Eine Reservierung enthält folgende Informationen:

| Parameter | Datentyp | Beschreibung |
| --- | --- | --- |
| `reservation_id` | Ganzzahl | Eine systemgenerierte ID |
| `stock_id` | Ganzzahl | Die ID des Lagers, dem das Produkt zugewiesen ist |
| `sku` | Zeichenfolge | Die SKU des Produkts |
| `quantity` | Gleitkommazahl | Die Anzahl der Elemente in dieser Reservierung |
| `metadata` | Zeichenfolge | Der Ereignistyp, Objekttyp und Objekt-ID für diese Reservierung. Beispiel: `{"event_type":"order_placed","object_type":"order",| "object_id":"8"}` |

{style="table-layout:auto"}

Die `event_type` kann die folgenden Werte aufweisen:

- `order_placed`
- `order_canceled`
- `shipment_created`
- `creditmemo_created`
- `invoice_created`

Derzeit muss der Metadaten-Objekttyp `order` sein, und die Objekt-ID ist die Bestell-ID.

In zukünftigen Versionen ist es möglicherweise möglich, eine Reservierung zu erstellen, wenn ein Kunde einen Artikel zu einem Warenkorb hinzufügt. Jeder Artikel kann für einen bestimmten Zeitraum, z. B. 15 Minuten, reserviert werden, sodass der Kunde Artikel reservieren kann, während er weiter einkauft. Wenn dieser Reservierungstyp aktiviert ist, können die Metadaten zusätzliche Informationstypen enthalten.

## Reservierungslebenszyklus

Das folgende Beispiel zeigt die Reihenfolge der Reservierungen, die für eine einfache Bestellung generiert wurden.

1. Der Kunde bestellt 25 Stück `SKU-1`. Die Reservierung enthält folgende Informationen:

   ```text
   reservation_id = 1
   stock_id = 1
   sku = SKU-1
   quantity = -25
   event_type = order_placed
   ```

1. Der Kunde sendet eine Rechnung für 20 Artikel, im Wesentlichen Stornierung von 5 der bestellten Einheiten.

   ```text
   reservation_id = 2
   stock_id = 1
   sku = SKU-1
   quantity = 5
   event_type = order_canceled
   ```

1. Der Händler verschifft die gekauften 20 Einheiten.

   ```text
   reservation_id = 3
   stock_id = 1
   sku = `SKU-1`
   quantity = 20
   event_type = shipment_created
   ```

Die drei `quantity` summieren sich bis zu 0 (-25 + 5 + 20). Das System ändert keine vorhandenen Reservierungen.

## Verarbeitete Reservierungen entfernen

Der `inventory_cleanup_reservations` Cron-Auftrag führt SQL-Abfragen aus, um die Reservierungsdatenbanktabelle zu löschen. Standardmäßig wird sie täglich um Mitternacht ausgeführt, aber Sie können die Zeiten und die Häufigkeit konfigurieren. Der Cron-Auftrag führt ein Skript aus, das die Datenbank abfragt, um vollständige Reservierungssequenzen zu finden, in denen die Summe der Mengenwerte 0 ist. Wenn alle Reservierungen für ein bestimmtes Produkt, die am selben Tag (oder einer anderen konfigurierten Zeit) entstanden sind, kompensiert wurden, löscht der Cron-Auftrag die Reservierungen alle auf einmal.

Der `inventory_reservations_cleanup` Cron-Auftrag ist nicht identisch mit dem `inventory.reservations.cleanup` Nachrichtenwarteschlange-Verbraucher. Der -Verbraucher löscht Reservierungen asynchron nach Produkt-SKU, nachdem ein Produkt entfernt wurde, während der Cron-Auftrag die gesamte Reservierungstabelle löscht. Der -Verbraucher wird benötigt, wenn Sie die Stock [**Option „Mit Katalog synchronisieren**](../configuration-reference/catalog/inventory.md) in der Store-Konfiguration aktivieren. Siehe [Verwalten von Nachrichtenwarteschlangen](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html?lang=de) im _Konfigurationshandbuch_.

Häufig können alle anfänglichen Reservierungen, die an einem einzigen Tag erstellt wurden, nicht am selben Tag kompensiert werden. Diese Situation kann auftreten, wenn ein Kunde eine Bestellung aufgibt, kurz bevor der Cron-Auftrag beginnt, oder den Kauf mit einer Offline-Zahlungsmethode tätigt, wie z. B. einer Banküberweisung. Die kompensierten Reservierungssequenzen verbleiben in der Datenbank, bis sie alle kompensiert werden. Diese Vorgehensweise beeinträchtigt die Reservierungsberechnungen nicht, da die Summe für jede Reservierung 0 beträgt.

>[!NOTE]
>
>Es gibt CLI-Befehle, mit denen Sie Reservierungsinkonsistenzen erkennen und verwalten können (siehe [[!DNL Inventory Management] CLI-Referenz](cli.md)).

### Aktualisierungen der Reservierung

Wenn Änderungen an Bestellungen und Produktbeträgen abgeschlossen sind, gibt [!DNL Commerce] automatisch Reservierungskompensationen ein. Sie müssen keine Vergütungen über den Admin oder den Code eingeben, um diese Sperren zu aktualisieren oder zu löschen. Reservierungen sind nur von eingegebenen Reservierungen betroffen, um eine Menge zu sperren oder einen Sperrbetrag zu löschen (Ausgleich der Reservierungen).

So funktionieren sie:

- **Bestellung gesendet** - Wenn eine Bestellung für mehrere Produkte gesendet wird, wird eine Reservierung für diesen Betrag eingegeben. Wenn Sie z. B. fünf Rucksäcke von einer US-Website bestellen, wird eine Reservierung von `-5` für diese SKU und diesen Lagerbestand vorgenommen. Die verkaufsfähige Menge wird um 5 verringert.

- **Stornierte Bestellung** - Wenn eine Bestellung storniert wird (ganz oder teilweise), gibt eine Ausgleichsreservierung ein, um diesen Betrag zu löschen. Wenn Sie beispielsweise drei Rucksäcke stornieren, wird eine +3-Reservierung für diese SKU und diesen Lagerplatz eingegeben, wodurch der Laderaum aufgehoben wird. Die verkaufsfähige Menge wird um 3 erhöht.

- **Lieferauftrag** - Wenn eine Bestellung (ganz oder teilweise) versendet wird, wird eine Ausgleichsreservierung eingegeben, um diesen Betrag zu verrechnen. Beispielsweise gibt der Versand von zwei Rucksäcken eine +2-Reservierung für diese SKU und dieses Lager ein und löscht den Laderaum. Die Produktmenge wird für die Sendung direkt um 2 reduziert. Die berechnete verkaufbare Menge wird auch für den reduzierten Lagerbetrag aktualisiert, ist aber von der Reservierung nicht mehr betroffen.

![Reservierungs-Updates](assets/diagram-reservation.png){width="600" zoomable="yes"}

Alle Reservierungen müssen durch Kompensationen verrechnet werden, wenn die Bestellungen vollständig ausgeführt, Produkte storniert, Gutschriften ausgestellt werden usw. Wenn die Ausgleichszahlungen die Reservierungen nicht ausräumen, könnten Sie Mengen in Stasis halten (nicht zum Verkauf verfügbar und nie Versand).

>[!NOTE]
>
>Wenn Sie Reservierungen überprüfen möchten, stehen eine Reihe von Befehlszeilenoptionen zur Verfügung. Reservierungen können nur über eine Befehlszeilenschnittstelle angezeigt werden. Die Verwendung von CLI-Befehlen kann Entwicklerunterstützung erfordern. Siehe [[!DNL Inventory Management] CLI-](cli.md).

Wenn Sie alle Quellen aus einem Produkt für ein Lager mit ausstehenden Bestellungen entfernen, haben Sie möglicherweise Reservierungen blockiert.

{{$include /help/_includes/unassign-source.md}}


<!-- Last updated from includes: 2022-08-30 15:36:09 -->
