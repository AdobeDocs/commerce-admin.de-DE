---
title: Bestellung nach SKU
description: Erfahren Sie, wie Sie Ihren Store so konfigurieren, dass die Bestellung durch SKU unterstützt wird, um Ihre Kunden zu unterstützen.
exl-id: cb39554f-ab76-46d5-8217-e43bc8f9f88d
feature: Orders, Storefront, Configuration
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '586'
ht-degree: 0%

---

# Bestellung nach SKU

{{ee-feature}}

Eine &quot;SKU&quot;ist eine &quot;Bestandseinheit&quot;. SKUs helfen Online-Anbietern im Allgemeinen dabei, die wichtigsten Produktmerkmale wie Größe, Farbe, Preis und Material zu identifizieren. Produkt-IDs unterscheiden sich von SKUs:

- Der `Product ID` ist eine sequenzielle Zahlenreihe, die intern zur Identifizierung von Produkten verwendet wird und nicht für Kunden verfügbar ist.
- Der `SKU` wird vom Verkäufer generiert, normalerweise basierend auf dem Produktnamen und den Attributen für das Marketing oder interne Tracking. Beispiel: Ein blaues T-Shirt aus Baumwolle, ein Medium der Größe: T-COT-MED-BL. Die SKU kann vom Verkäufer bei Bedarf geändert werden.

Normalerweise enthält eine SKU eine Reihe von Abkürzungen, die die Unterscheidungsmerkmale des Produkts angeben. Die maximale SKU-Länge beträgt 64 Zeichen. SKUs sind wichtig, um Lagerbestände effektiv zu verfolgen und zu verwalten. Daher ist die korrekte Einrichtung für den elektronischen Geschäftsverkehr von entscheidender Bedeutung.

_Bestellung durch SKU_ ist ein [Widget](../content-design/widgets.md), das im Speicher angezeigt werden kann, um es allen Käufern zu erleichtern, oder nur den Käufern in bestimmten Kundengruppen zur Verfügung gestellt wird. Käufer können entweder die SKU und die Mengeninformationen direkt in den SKU-Block &quot;Bestellung nach SKU&quot;eingeben oder eine CSV-Datei aus ihrem Kundenkonto hochladen. Unabhängig von der Konfiguration ist die Bestellung nach SKU immer für Store-Administratoren verfügbar.

![Bestellen nach SKU in der Storefront](./assets/storefront-order-by-sku.png){width="700" zoomable="yes"}

## Bestellung nach SKU konfigurieren

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Abschnitt **[!UICONTROL Sales]** und wählen Sie unter &quot;**[!UICONTROL Sales]**&quot;.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Order by SKU Settings]** .

1. Setzen Sie **[!UICONTROL Enable Order by SKU on my Account in Storefront]** auf einen der folgenden Werte:

   - `Yes, for Everyone` - Der Block Bestellung nach SKU ist im Speicher für jeden Käufer verfügbar.
   - `Yes, for Specified Customer Groups` - Die Bestellung nach SKU ist nur für Mitglieder einer bestimmten Kundengruppe wie `Wholesale` verfügbar.
   - `No` - Der Block Bestellung nach SKU wird nicht in der Storefront angezeigt und die Seite Bestellung nach SKU ist nicht im Kundenkonto verfügbar.

   ![Bestellen nach SKU-Einstellungen](../configuration-reference/sales/assets/sales-order-by-sku-settings.png){width="600" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Save Config]**.

![Adobe Commerce B2B](../assets/b2b.svg) (nur Adobe Commerce B2B) _**Deaktivieren Sie die Funktion &quot;Quick Order&quot;, um die Funktion &quot;Order by SKU&quot;zu aktivieren:**_

1. Gehen Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wählen Sie im linken Bereich unter _[!UICONTROL General]_die Option **[!UICONTROL B2B Features]**

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL B2B Features]** .

1. Setzen Sie **[!UICONTROL Enable Quick Order]** auf `No`.

   Mit der Funktion [Quick Order](../b2b/quick-order.md) können Kunden und Gäste schnell Bestellungen basierend auf der SKU oder dem Produktnamen aufgeben.

## Storefront-Erlebnis

Wenn die Funktionalität für den Store konfiguriert ist, können Kunden die Bestellung nach SKU über jede Seite vornehmen, die das Widget _Bestellung nach SKU_ enthält, oder über ihr Konto-Dashboard.

### Bestellung nach SKU aus dem Seitenblock

1. Im Block _Bestellung durch SKU_ gibt der Kunde die **[!UICONTROL SKU]** und die **[!UICONTROL Qty]** des zu bestellenden Artikels ein.

1. Um ein weiteres Element hinzuzufügen, klicken Sie auf &quot;**[!UICONTROL Add Row]**&quot;und wiederholen Sie den Prozess.

1. Klicks **[!UICONTROL Add to Cart]**.

### Bestellung durch SKU über ein Kundenkonto

1. Über die Storefront meldet sich der Kunde bei seinem Konto an.

1. Wählen Sie im linken Bereich **[!UICONTROL Order by SKU]** aus.

1. Fügt einzelne Elemente nach Präferenz hinzu:

   _**Fügt jedes Element nach SKU hinzu:**_

   - Fügt die **[!UICONTROL SKU]** und **[!UICONTROL Qty]** des Elements ein, das bestellt werden soll.

   - Um nach Bedarf weitere Elemente hinzuzufügen, klicken Sie auf die Schaltfläche _Zeile hinzufügen_ ![Plus-Zeichen](../assets/button-add-item.png) und wiederholt sich für so viele Elemente wie nötig.

   - Klicks **[!UICONTROL Add to Cart]**.

   _**Lädt eine CSV-Datei mit mehreren Elementen hoch:**_

   - Bereitet eine Datei mit dem Namen [import data CSV](../systems/data-csv.md) (kommagetrennter Wert) vor, die Spalten für `SKU` und `Qty` enthält.

   ![Zu importierende SKUs](./assets/account-dashboard-order-by-sku-import.png){width="500" zoomable="yes"}

   - Um die CSV-Datei hochzuladen, klicken Sie auf **[!UICONTROL Choose File]** und wählen Sie die hochzuladende Datei aus.

   - Klicks **[!UICONTROL Add to Cart]**.

   Wenn eines der Produkte zusätzliche Optionen aufweist, wird der Kunde vom Warenkorb aufgefordert, darauf zu achten, dass das Produkt beachtet werden muss.

   ![Produkt erfordert Aufmerksamkeit](./assets/account-dashboard-order-by-sku-cart-product-requires-attention.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Bei doppelten SKUs werden die Mengen zu einem Zeileneintrag im Warenkorb zusammengefasst. Der Kunde kann die Menge eines Elements ändern und auf **[!UICONTROL Update Shopping Cart]** klicken, um die Summen neu zu berechnen.

