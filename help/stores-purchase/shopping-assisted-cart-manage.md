---
title: Warenkorb verwalten
description: Erfahren Sie, wie Sie einen Kunden direkt vom Administrator bei seinem Warenkorb unterstützen.
exl-id: beb41dfa-ef87-4065-96fd-0649a5c4c21c
feature: Customer Service, Shopping Cart
source-git-commit: dc19eeea03dc46b14fcbe339a8e426b249346673
workflow-type: tm+mt
source-wordcount: '658'
ht-degree: 0%

---

# Warenkorb verwalten

{{ee-feature}}

Um eine unterstützende Shopping-Sitzung zu starten, muss der Kunde von der Storefront in sein Konto eingeloggt sein, um die Informationen zur Verfügung zu stellen. Wenn der Kunde über kein Konto verfügt, können Sie [ein](../customers/account-create.md) erstellen.

![Warenkorb im Kundenkonto](./assets/customer-account-manage-cart-items.png){width="600" zoomable="yes"}

## Aktionssteuerung

| Option | Beschreibung |
|--- |--- |
| [!UICONTROL Remove] | Entfernt Artikel aus dem aktuellen Warenkorb |
| [!UICONTROL Move to Wish List] | Verschiebt Elemente in die ausgewählte KundenWunschliste. |

{style="table-layout:auto"}

## Schaltflächen

| Schaltfläche | Beschreibung |
|--- |--- |
| [!UICONTROL Clear my shopping cart] | Löscht den aktuellen Warenkorb aus allen Produkten. |
| [!UICONTROL Update Items and Quantities|]Geben Sie die erforderliche Menge in das Feld **[!UICONTROL Qty]** ein und aktualisieren Sie die Anzahl der Artikel im Warenkorb. |
| [!UICONTROL Add selections to my cart] | Fügt Produkte aus allen Bereichen zum Warenkorb hinzu. |

{style="table-layout:auto"}

## Überprüfen, ob der Kunde angemeldet ist

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Customers]** > **[!UICONTROL Now Online]**.

   Alle Besucher des Stores und angemeldete Kunden werden in der Liste angezeigt.

   ![Kunden sind jetzt online](./assets/customers-now-online.png){width="700" zoomable="yes"}

## Einkaufen mit Angebotsunterstützung

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Öffnen Sie in der Liste den Kundendatensatz im Bearbeitungsmodus.

   >[!TIP]
   >
   >Um den Kundendatensatz in Eile zu finden, verwenden Sie das Steuerelement [Filter](../getting-started/admin-grid-controls.md) .

   Im Kundenprofil unter _[!UICONTROL Personal Information]_zeigt das Datum und die Uhrzeit_[!UICONTROL Last Logged In]_ an, dass der Kunde online ist.

   ![Kundenprofil eines Online-Kunden](./assets/customer-account-manage-cart.png){width="600" zoomable="yes"}

1. Um in den unterstützten Warenkorb zu wechseln, klicken Sie in der oberen Schaltflächenleiste auf **[!UICONTROL Manage Shopping Cart]** .

   ![Assisted shopping mode](./assets/customer-manage-shopping-cart.png){width="600" zoomable="yes"}

## Produkte dem Warenkorb nach Attribut hinzufügen

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Products]** .

1. Suchen Sie mithilfe eines Filters oben in jeder Spalte nach einem Produkt.

1. Klicken Sie auf **[!UICONTROL Search]**.

1. Führen Sie je nach Produkttyp eine der folgenden Schritte aus:

### Einfaches Produkt hinzufügen

1. Klicken Sie auf das Produkt, das Sie bestellen möchten.

   Diese Aktion wählt den Datensatz aus und setzt **[!UICONTROL Quantity]** auf den Standardwert `1`.

1. Aktualisieren Sie bei Bedarf die bestellte Menge.

1. Klicken Sie links über dem Raster auf **[!UICONTROL Add selections to my cart]**.

   ![Produkt zum Warenkorb hinzufügen](./assets/customer-account-manage-cart-order-products.png){width="600" zoomable="yes"}

   Der Zeileneintrag wird dem Warenkorb oben auf der Seite hinzugefügt.

   ![Warenkorb aktualisiert](./assets/customer-account-manage-cart-update-cart.png){width="600" zoomable="yes"}

### Produkt mit Konfiguration hinzufügen

Es gibt drei Arten von Produkten, die konfiguriert werden müssen, bevor sie zum Warenkorb hinzugefügt werden: `Bundle Product`, `Configurable Product` und `Grouped Product`.

1. Klicken Sie im Raster neben dem Produktnamen auf **[!UICONTROL Configure]** .

   ![Konfigurieren des Produkts](./assets/customer-account-manage-cart-order-configurable-product.png){width="600" zoomable="yes"}

1. Wählen Sie im Dialogfeld _Zugeordnete Produkte_ die einzelnen Produktoptionen aus, um das zu bestellende Element zu beschreiben, geben Sie den Wert **[!UICONTROL Quantity]** ein und klicken Sie auf **[!UICONTROL OK]**.

   Das Produkt wird mit einem Häkchen ausgewählt und die sortierte Menge wird im Raster angezeigt.

1. Um das Produkt zum Warenkorb hinzuzufügen, klicken Sie auf **[!UICONTROL Add selections to my cart]**.

   ![Konfigurierbares Produkt im Warenkorb](./assets/customer-account-manage-cart-order-configurable-product-cart.png){width="600" zoomable="yes"}

1. Aktualisieren Sie bei Bedarf die Produktoptionen im Warenkorb:

   - Klicken Sie auf **[!UICONTROL Configure]**.

   - Aktualisieren Sie die Optionen und klicken Sie auf **[!UICONTROL OK]**.

## Produkt nach SKU hinzufügen

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Add to Shopping Cart by SKU]** .

1. Fügen Sie Produkte einzeln nach **[!UICONTROL SKU]** hinzu oder fügen Sie Produkte hinzu, indem Sie eine CSV-Datei hochladen.

### Elemente einzeln nach SKU hinzufügen

1. Geben Sie die **[!UICONTROL SKU]** und die **[!UICONTROL Qty]** des Elements ein, das bestellt werden soll.

1. Um ein anderes Produkt zu bestellen, klicken Sie auf **[!UICONTROL Add another]**.

   ![Produkte von SKU hinzufügen](./assets/customer-account-manage-cart-order-product-by-sku.png){width="600" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Add selections to my cart]**.

1. Wenn es sich bei dem Element um ein konfigurierbares Produkt handelt, wählen Sie die Produktoptionen bei entsprechender Aufforderung aus und klicken Sie auf **[!UICONTROL Add to Shopping Cart]**.

### Hinzufügen von Produkten durch Hochladen einer CSV-Datei

1. Bereiten Sie eine [CSV-Datei](../systems/data-csv.md) mit den Elementen vor, die zum Warenkorb hinzugefügt werden sollen.

   Die Datei darf nur zwei Spalten enthalten, wobei in der Kopfzeile `sku` und `qty` stehen.

1. Laden Sie die vorbereitete Datei hoch:

   - Klicken Sie auf **[!UICONTROL Choose File]**.

   - Wählen Sie die aus Ihrem Verzeichnis hochzuladende Datei aus.

## Element übertragen

Sie können Artikel aus der Wunschliste eines Kunden in den Warenkorb übertragen und kürzlich angezeigte, verglichene oder bestellte Artikel anzeigen. Die Anzahl der Elemente in jedem Abschnitt wird in Klammern nach der Kopfzeile des Abschnitts angezeigt.

1. Erweitern Sie den Erweiterungs-Selektor ](../assets/icon-display-expand.png) um einen der folgenden Abschnitte:![

   - [!UICONTROL Wish List]
   - [!UICONTROL Products in the Comparison List]
   - [!UICONTROL Recently Compared Products]
   - [!UICONTROL Recently Viewed Products]
   - [!UICONTROL Last Ordered Items]

1. Wählen Sie im Raster jedes zu sortierende Produkt aus und geben Sie den Wert **[!UICONTROL Quantity]** ein.

1. Um die Optionen für ein konfigurierbares Produkt einzugeben, klicken Sie auf **[!UICONTROL Configure]** und legen Sie die Produktoptionen nach Bedarf fest.

1. Klicken Sie auf **[!UICONTROL Add selections to my cart]**.

1. Wenden Sie einen oder mehrere Couponcodes an, sofern verfügbar:

   - Geben Sie für **[!UICONTROL Apply Coupon Code]** einen gültigen Gutscheincode ein.

   - Klicken Sie auf den Pfeil _Anwenden_ ( ![Pfeilsymbol](../assets/icon-apply-arrow.png) ).

1. Passen Sie die bestellte Menge nach Bedarf an:

   - Geben Sie in der Spalte **[!UICONTROL Qty]** des zu ändernden Produkts den korrekten Betrag ein.

   - Klicken Sie auf **[!UICONTROL Update Items and Quantities]**.

## Bestellung erstellen

1. Klicken Sie auf **[!UICONTROL Create Order]**.

   Auf der Seite _[!UICONTROL Create New Order]_werden die Artikel im Warenkorb angezeigt, gefolgt von den Versand- und Zahlungsinformationen.

1. Füllen Sie die Versand- und Zahlungsinformationen aus.

1. Klicken Sie auf **[!UICONTROL Submit Order]**.

Weitere Informationen finden Sie unter [Erstellen einer Bestellung](customer-account-create-order.md).
