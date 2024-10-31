---
title: '[!UICONTROL Catalog] &gt; [!UICONTROL Inventory]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Catalog] &gt; [!UICONTROL Inventory] des Commerce-Administrators.
exl-id: 80113a31-3585-4ee1-95af-31efc09389eb
feature: Configuration, Inventory
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '1195'
ht-degree: 0%

---

# [!UICONTROL Catalog] > [!UICONTROL Inventory]

{{config}}

>[!NOTE]
>
>[!DNL Inventory Management] für Adobe Commerce und Magento Open Source bietet Ihnen die Tools zur Verwaltung Ihres Produktbestands. Händler mit einem einzigen Geschäft zu mehreren Lagern, Geschäften, Abholstandorten, Ablagelagern und mehr können diese Funktionen nutzen, um die Mengen für den Verkauf zu halten und Sendungen für komplette Bestellungen abzuwickeln. Weitere Informationen zu diesen Funktionen und wie Sie sie zur Verwaltung von Lagern an mehreren Standorten verwenden können, finden Sie im [_[!DNL Inventory Management] Benutzerhandbuch _](https://experienceleague.adobe.com/docs/commerce-admin/inventory/introduction.html).

## [!UICONTROL Stock Options]

![Stock Options](./assets/catalog-inventory-stock-options.png)<!-- zoom -->

<!-- [Stock Options](https://experienceleague.adobe.com/en/docs/commerce-admin/inventory/configuration/global-options) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Decrease Stock When Order is Placed] | Global | Wenn der Wert auf &quot;`Yes`&quot; gesetzt wird, verringert sich die Lagermenge, wenn die Bestellung aufgegeben wird. Wenn _Stock verwalten_ aktiviert ist, werden Reservierungen für die bestellten Produkte und Mengen eingegeben. Optionen: `Yes` / `No` |
| [!UICONTROL Set Items' Status to be in Stock When Order is Cancelled] | Store-Ansicht | Wenn auf `Yes` gesetzt, wird beim Abbruch der Bestellung das Element auf Lager zurückgegeben. Wenn _Stock verwalten_ aktiviert ist, wird die Reservierung für die stornierten Produkte und Mengen gelöscht. Optionen: `Yes` / `No` |
| [!UICONTROL Display Out of Stock Products] | Global | Wenn auf &quot;`Yes`&quot; gesetzt, werden nicht vorrätige Produkte angezeigt. Wenn auch Produktwarnungen aktiviert sind, können sich Kunden für eine Benachrichtigung anmelden, wenn das Produkt verfügbar wird. Optionen: `Yes` / `No` |
| [!UICONTROL Only X left Threshold] | Webseite | Legt den Schwellenwert für die Meldung `Only x left` fest. Wenn Sie beispielsweise auf 3 setzen, wird die Meldung angezeigt, wenn mindestens drei Elemente auf Lager sind. Die Meldung wird nicht angezeigt, wenn der Wert auf `0` gesetzt ist. |
| [!UICONTROL Display products availability in Stock on Storefront] | Store-Ansicht | Wenn auf `Yes` gesetzt, wird eine `In Stock` - oder `Out of Stock` -Meldung auf der Produktseite angezeigt. Optionen: `Yes` / `No` |
| [!UICONTROL Enable Inventory Check On Cart Load] | Global | Bestimmt, ob beim Laden eines Produkts in den Warenkorb eine Bestandsüberprüfung durchgeführt wird. Die Deaktivierung dieser Bestandsüberprüfung kann die Leistung bei Checkout-Schritten verbessern, insbesondere wenn viele Artikel im Warenkorb sind. Wenn Sie die Vorab-Validierung jedoch überspringen, können Kunden später im Checkout-Prozess _Nicht vorrätig_-Fehler sehen. Optionen: `Yes` / `No` |
| [!UICONTROL Synchronize with Catalog] | Global | Wenn der Wert auf &quot;`Yes`&quot;gesetzt wird, werden die Bestandsdaten entsprechend den Katalogänderungen angepasst (z. B. Produkterneuerungen, Änderungen der Produkt-SKU und Änderungen des Produkttyps) und es wird für Konsistenz zwischen Bestand und Katalog gesorgt. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Product Stock Options]

![Optionen für Produktspeicher](./assets/catalog-inventory-product-stock-options.png)<!-- zoom -->

<!-- [Product Stock Options](https://experienceleague.adobe.com/en/docs/commerce-admin/inventory/configuration/global-options) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Manage Stock] | Global | Bestimmt, ob Sie die vollständige Bestandskontrolle verwenden, um die Elemente in Ihrem Katalog zu verwalten. Optionen: <br/>**Ja** - Aktiviert die vollständige Bestandskontrolle, um die Anzahl der aktuell auf Lager befindlichen Elemente zu verfolgen. <br/>**Nein** - Verfolgt nicht die Anzahl der aktuell auf Lager befindlichen Elemente. |
| [!UICONTROL Backorders] | Global | Bestimmt, wie Ihr Store Rückstände verwaltet. Ein Rückstand ändert den Verarbeitungsstatus der Bestellung nicht. Die Mittel werden weiterhin unmittelbar bei der Bestellung zugelassen oder erfasst, unabhängig davon, ob das Produkt vorrätig ist. Wenn das Produkt verfügbar wird, wird es versandt. Optionen: <br/>**Keine Rückmeldungen** - Akzeptiert keine Rückstände, wenn das Produkt nicht vorrätig ist. <br/>**Menge unter 0 zulassen** - Akzeptiert Rückläufe, wenn die Menge unter null fällt. <br/>**Menge unter 0 zulassen und Kunde benachrichtigen** - Akzeptiert Rückaufträge, wenn die Menge unter null fällt, benachrichtigt Kunden jedoch darüber, dass Bestellungen weiterhin aufgegeben werden können. |
| [!UICONTROL Use deferred Stock update] | Global | ![Adobe Commerce](../../assets/adobe-logo.svg) (nur Adobe Commerce) Bestimmt, ob die Bestandsaktualisierung verschoben werden soll, wenn Rückorder zulässig sind (die Option _Rückwärts-Bestellungen_ ist auf irgendetwas festgelegt, was über den Standardwert `No backorders` hinausgeht). Es funktioniert für ein einzelnes Produkt oder eine ganze Website und verwendet den Mechanismus _Auftragswarteschlange_ , um die Inventarmengenindikatoren asynchron zu aktualisieren, nachdem die Bestellungen aufgegeben wurden. Diese Option funktioniert auch mit der asynchronen Auftragsplatzierung ](https://experienceleague.adobe.com/docs/commerce-operations/performance-best-practices/high-throughput-order-processing.html#asynchronous-order-placement) in Kombination mit [Inventory management](../../inventory-management/introduction.md).[ |
| Maximale im Warenkorb zulässige Menge | Global | Bestimmt die maximale Anzahl von Produkten, die in einer Bestellung erworben werden können. Standardmäßig ist die maximale Menge auf 10.000 festgelegt. |
| [!UICONTROL Out-of-Stock Threshold] | Global | Bestimmt den Lagerbestand, bei dem eine Ware als nicht vorrätig gilt. Optionen: <br/>**Positiver Betrag** - Geben Sie bei deaktiviertem _Rückorder_ einen positiven Betrag ein. Wenn Rückaufträge aktiviert sind, wird dieser Betrag ignoriert. <br/>**Null** - Wenn _Rückorder_ aktiviert ist, ermöglicht die Eingabe von `0` unendliche Rückorder. <br/>**Negativer Betrag** - Wenn _Rückläufe_ aktiviert ist, empfehlen wir, einen negativen Betrag einzugeben. Der Betrag wird der Verkaufsmenge hinzugefügt. Geben Sie beispielsweise -50 ein, um Bestellungen bis zu diesem Betrag zuzulassen. |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | Global | Bestimmt den Mindestbetrag eines Artikels, der gemäß Kundengruppe zum Kauf verfügbar ist. Standardmäßig ist die Mindestmenge auf 1 gesetzt. Klicken Sie auf **[!UICONTROL Add Minimum Qty]** , um einen anderen Wert für eine bestimmte Kundengruppe einzugeben. |
| [!UICONTROL Notify for Quantity Below] | Global | Bestimmt den Lagerbestand, bei dem die Benachrichtigung gesendet wird, dass der Bestand unter den Schwellenwert gefallen ist. |
| [!UICONTROL Enable Qty Increments] | Global | Bestimmt, ob Artikel in Mengenschritten verkauft werden können. Optionen: `Yes` / `No` |
| [!UICONTROL Qty Increments] | Global | Legt die Anzahl der Produkte fest, aus denen eine Mengenerhöhung besteht. |
| [!UICONTROL Automatically Return Credit Memo Item to Stock] | Global | Bestimmt, ob in Kreditkarten enthaltene Elemente automatisch in den Bestand zurückgegeben werden. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Admin Bulk Operations]

![Massenvorgänge für Administratoren](./assets/catalog-inventory-admin-bulk-operations.png)<!-- zoom -->

<!-- [Admin Bulk Operations](https://experienceleague.adobe.com/en/docs/commerce-admin/inventory/configuration/global-options) -->

>[!NOTE]
>
>Um **asynchrone Warteschlangenmanager** zu konfigurieren und zu unterstützen, müssen Sie die Befehlszeile verwenden. Dies erfordert möglicherweise Hilfe von Entwicklern. Siehe [Starten von Verbrauchern in der Nachrichtenwarteschlange](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/start-message-queues.html) im _Konfigurationshandbuch_.

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Run asynchronously] | Global | Bestimmt, ob Sie Massenvorgänge für Massenproduktaktionen asynchron ausführen, einschließlich [Massenvorgänge](../../inventory-management/bulk-assignment.md) Zuweisen von Quellen, Aufheben der Zuweisung von Quellen und [Bestandsübertragung an Quelle](../../inventory-management/inventory-transfer.md). Sie erfasst Massenaktionen bis zum _[!UICONTROL Asynchronous batch size]_und führt diese Aktionen dann aus. Diese Funktion ist standardmäßig deaktiviert. Es wird empfohlen, Ihre Leistung mit Massenaktionen zu überprüfen, bevor Sie die Aktivierung vornehmen. Optionen:<br/>**`Yes`**- Führt alle Massenvorgänge für [!DNL Inventory Management] asynchron aus. Um dies zu aktivieren, müssen Sie einen asynchronen Warteschlangenmanager konfigurieren.<br/>**`No`**- Standard. Führt keine asynchronen Massenvorgänge aus. |
| [!UICONTROL Asynchronous batch size] | Global | Setzen Sie **[!UICONTROL Run asynchronously]** auf `Yes` , um einen Wert für das Feld _[!UICONTROL Asynchronous batch size]_einzugeben. <br/>Die standardmäßige Batch-Größe ist 100. Wenn Massenprozesse diesen Wert erreichen, werden sie ausgeführt. |

{style="table-layout:auto"}

## [!UICONTROL Inventory Indexer Settings]

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Stock/Source reindex strategy] | Global | Bestimmt die Strategie für die Neuindizierung von Beständen/Quellen. Optionen: `Synchronous` / `Asynchronous` (ein asynchroner Warteschlangenmanager muss für den asynchronen Modus konfiguriert werden) |

{style="table-layout:auto"}

>[!NOTE]
>
> Aufgrund der Abhängigkeiten von Bestandsaktualisierungen für die auftragsbezogenen Aktivitäten wird der Inventarindexer auch beim Speichern des Produkts ausgelöst, unabhängig von der Einstellung `Synchronous` oder `Asynchronous` .


## [!UICONTROL Distance Provider for Distance Based SSA]

![Entfernungsanbieter für entfernungsbasierte SSA](./assets/catalog-inventory-distance-provider.png)<!-- zoom -->

<!-- [Distance Providers for Distance Based SSA](https://experienceleague.adobe.com/en/docs/commerce-admin/inventory/configuration/distance-priority-algorithm) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Provider] | Global | Bestimmt den Provider, der für den Distance Priority Source Selection Algorithm verwendet werden soll. Diese Funktion ist standardmäßig aktiviert. Optionen: <br/>**`Google MAP`**- Verwendet Google-Dienste zur Berechnung der Entfernung zwischen der Lieferzieladresse und den Quellspeicherorten (Adresse und GPS-Koordinaten). Für diese Option ist ein Google-API-Schlüssel erforderlich, für den möglicherweise Gebühren über Google anfallen.<br/>**`Offline Calculation`** - Berechnet den Abstand mithilfe einer eingebetteten Datenbank, um die nächstgelegene Quelle für die Lieferzieladresse zu bestimmen. Um diese Option verwenden zu können, benötigen Sie möglicherweise Hilfe von Entwicklern, um zunächst den Inhalt des Datenbankspeicherorts für alle Länder herunterzuladen, die Sie über eine Befehlszeile versenden. |

{style="table-layout:auto"}

## [!UICONTROL Google Distance Provider]

![Google-Entfernungsanbieter](./assets/catalog-inventory-distance-provider-settings.png)<!-- zoom -->

<!-- [Google Distance Provider](https://experienceleague.adobe.com/en/docs/commerce-admin/inventory/configuration/distance-priority-algorithm) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Google API key] | Global | Geben Sie den Google-API-Schlüssel für den Google MAP-Provider ein. Der Schlüssel stammt aus dem [!DNL Google Maps Platform] und sollte [!DNL Geocoding API] und [!DNL Distance Matrix API] aktiviert haben. Weitere Informationen finden Sie unter [Konfigurieren des Distance Priority Algorithm](../../inventory-management/distance-priority-algorithm.md#configure-the-distance-priority-algorithm) im _Inventory management-Handbuch_. |
| [!UICONTROL Computation mode] | Global | Bestimmt die Anweisungen und Pfade zur Berechnung der Entfernung von der Lieferadresse und allen dem Lager zugewiesenen Quellen. Standardmäßig verwenden Berechnungen den Fahrmodus. Optionen: <br/>**`Driving`**- Standardeinstellung, fordert Standardfahrtanweisungen über das Straßennetz an.<br/>**`Walking`** - Fordert Wanderwege über Fußgängerwege und Bürgersteige an (sofern verfügbar). <br/>**`Bicycling`**- Fordert Fahrradwege über Fahrradwege und bevorzugte Straßen an (derzeit nur in den USA und einigen kanadischen Städten). |
| [!UICONTROL Value] | Global | Gibt an, was für die Entfernung und die Zeit der Quellstandorte zur Lieferzieladresse berechnet und zurückgegeben werden soll. Der Distance Priority Algorithm empfiehlt die Quelle mit der kürzesten Entfernung oder der kürzesten Zeit zur Lieferzieladresse, die schneller und möglicherweise kostengünstiger zur Erfüllung von Sendungen ist. Optionen: <br/>**`Distance`**- Gibt die Entfernung zwischen Punkten in Metriken (Kilometer und Meter) oder dem Kaiserreich (Meilen und Fuß) zurück.<br/>**`Time to Destination`** - Gibt die erforderliche Zeit zurück, um von den Quellspeicherorten in Stunden und Minuten zur Lieferadresse zu gelangen. |

{style="table-layout:auto"}
