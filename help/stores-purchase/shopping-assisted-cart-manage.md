---
title: Verwalten eines Warenkorbs
description: Erfahren Sie, wie Sie einem Kunden direkt vom Administrator bei seinem Warenkorb helfen können.
exl-id: beb41dfa-ef87-4065-96fd-0649a5c4c21c
feature: Customer Service, Shopping Cart
source-git-commit: 69cd571b66a81159c2c99e6652907f22142568cb
workflow-type: tm+mt
source-wordcount: '746'
ht-degree: 0%

---

# Verwalten eines Warenkorbs

{{ee-feature}}

Um eine unterstützte Einkaufssession zu starten, muss der Kunde in seinem Konto von der Storefront eingeloggt sein, um die Informationen verfügbar zu machen. Wenn der Kunde kein Konto hat, können Sie [eines erstellen](../customers/account-create.md).

![Warenkorb im Kundenkonto](./assets/customer-account-manage-cart-items.png){width="600" zoomable="yes"}

## Aktionssteuerung

| Option | Beschreibung |
|--- |--- |
| [!UICONTROL Remove] | Entfernt Artikel aus dem aktuellen Warenkorb |
| [!UICONTROL Move to Wish List] | Verschiebt Artikel in die ausgewählte Kunden-Wunschliste |

{style="table-layout:auto"}

## Steuertasten

| Schaltfläche | Beschreibung |
|--- |--- |
| [!UICONTROL Clear my shopping cart] | Entfernt alle Artikel aus dem Warenkorb. |
| [!UICONTROL Update Items and Quantities|]Geben Sie die erforderliche Menge in das Feld **[!UICONTROL Qty]** ein und aktualisieren Sie die Anzahl der Artikel im Warenkorb. |
| [!UICONTROL Add selections to my cart] | Fügt Produkte aus allen Bereichen zum Warenkorb hinzu. |

{style="table-layout:auto"}

## Überprüfen, ob der Kunde angemeldet ist

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Customers]** > **[!UICONTROL Now Online]**.

   Alle Besucher des Stores und angemeldeten Kunden werden in der Liste angezeigt.

   ![Kunden jetzt online](./assets/customers-now-online.png){width="700" zoomable="yes"}

## Angebotsunterstütztes Einkaufen

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Öffnen Sie in der Liste den Kundendatensatz im Bearbeitungsmodus.

   >[!TIP]
   >
   >Um den Kundendatensatz schnell zu finden, verwenden Sie das Steuerelement [Filter](../getting-started/admin-grid-controls.md).

   Im Kundenprofil unter _[!UICONTROL Personal Information]_&#x200B;zeigt das&#x200B;_[!UICONTROL Last Logged In]_ Datum und die Uhrzeit an, dass der Kunde online ist.

   ![Kundenprofil eines Online-Kunden](./assets/customer-account-manage-cart.png){width="600" zoomable="yes"}

1. Um in den unterstützten Shopping-Modus zu wechseln, klicken Sie in der oberen Schaltflächenleiste auf **[!UICONTROL Manage Shopping Cart]** .

   ![Assisted Shopping-Modus](./assets/customer-manage-shopping-cart.png){width="600" zoomable="yes"}

## Produkte nach Attribut zum Warenkorb hinzufügen

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Products]** .

1. Suchen Sie mithilfe eines der Filter oben in jeder Spalte nach einem Produkt.

1. Klicken Sie auf **[!UICONTROL Search]**.

1. Verwenden Sie je nach Produkttyp einen der folgenden Schritte:

### Einfaches Produkt hinzufügen

1. Klicken Sie auf das Produkt, das Sie bestellen möchten.

   Diese Aktion wählt den Datensatz aus und setzt **[!UICONTROL Quantity]** auf den Standardwert `1`.

1. Aktualisieren Sie bei Bedarf die bestellte Menge.

1. Klicken Sie links über dem Raster auf **[!UICONTROL Add selections to my cart]**.

   ![Produkt zum Warenkorb hinzufügen](./assets/customer-account-manage-cart-order-products.png){width="600" zoomable="yes"}

   Der Zeileneintrag wird dem Warenkorb oben auf der Seite hinzugefügt.

   ![Warenkorb aktualisiert](./assets/customer-account-manage-cart-update-cart.png){width="600" zoomable="yes"}

### Produkt mit Konfiguration hinzufügen

Es gibt drei Arten von Produkten, die vor dem Hinzufügen zum Warenkorb konfiguriert werden müssen: `Bundle Product`, `Configurable Product` und `Grouped Product`.

1. Klicken Sie im Raster auf **[!UICONTROL Configure]** neben dem Produktnamen.

   ![Produkt konfigurieren](./assets/customer-account-manage-cart-order-configurable-product.png){width="600" zoomable="yes"}

1. Wählen _Dialogfeld „Zugehörige Produkte_ jede Produktoption aus, um das zu bestellende Element zu beschreiben, geben Sie den **[!UICONTROL Quantity]** ein und klicken Sie auf **[!UICONTROL OK]**.

   Das Produkt wird mit einem Häkchen ausgewählt und die bestellte Menge wird im Raster angezeigt.

1. Um das Produkt zum Warenkorb hinzuzufügen, klicken Sie auf **[!UICONTROL Add selections to my cart]**.

   ![Konfigurierbares Produkt im Warenkorb](./assets/customer-account-manage-cart-order-configurable-product-cart.png){width="600" zoomable="yes"}

1. Aktualisieren Sie bei Bedarf die Produktoptionen im Warenkorb:

   - Klicken Sie auf **[!UICONTROL Configure]**.

   - Aktualisieren Sie die Optionen und klicken Sie dann auf **[!UICONTROL OK]**.

## Produkt nach SKU hinzufügen

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Add to Shopping Cart by SKU]** .

1. Produkte einzeln per **[!UICONTROL SKU]** hinzufügen oder Produkte durch Hochladen einer CSV-Datei hinzufügen.

### Elemente einzeln nach SKU hinzufügen

1. Geben Sie **[!UICONTROL SKU]** und **[!UICONTROL Qty]** des zu bestellenden Artikels ein.

1. Um ein anderes Produkt zu bestellen, klicken Sie auf **[!UICONTROL Add another]**.

   ![Produkte hinzufügen nach SKU](./assets/customer-account-manage-cart-order-product-by-sku.png){width="600" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Add selections to my cart]**.

1. Wenn das Element ein konfigurierbares Produkt ist, wählen Sie die Produktoptionen aus, wenn Sie dazu aufgefordert werden, und klicken Sie dann auf **[!UICONTROL Add to Shopping Cart]**.

### Hinzufügen von Produkten durch Hochladen einer CSV-Datei

1. Bereiten Sie eine [CSV](../systems/data-csv.md)Datei) mit den Artikeln vor, die dem Warenkorb hinzugefügt werden sollen.

   Die Datei darf nur zwei Spalten enthalten, wobei `sku` und `qty` in der Kopfzeile stehen müssen.

1. Hochladen der vorbereiteten Datei:

   - Klicken Sie auf **[!UICONTROL Choose File]**.

   - Wählen Sie die Datei aus, die aus Ihrem Verzeichnis hochgeladen werden soll.

## Übertragen eines Artikels

Sie können Artikel aus der Wunschliste eines Kunden in den Warenkorb legen und kürzlich angesehene, verglichene oder bestellte Artikel anzeigen. Die Anzahl der Elemente in den einzelnen Abschnitten wird in Klammern hinter der Abschnittsüberschrift angezeigt.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) einen der folgenden Abschnitte:

   - [!UICONTROL Wish List]
   - [!UICONTROL Products in the Comparison List]
   - [!UICONTROL Recently Compared Products]
   - [!UICONTROL Recently Viewed Products]
   - [!UICONTROL Last Ordered Items]

1. Wählen Sie im Raster jedes zu bestellende Produkt aus und geben Sie die **[!UICONTROL Quantity]** ein.

1. Um die Optionen für ein konfigurierbares Produkt einzugeben, klicken Sie auf **[!UICONTROL Configure]** und legen Sie die Produktoptionen nach Bedarf fest.

1. Klicken Sie auf **[!UICONTROL Add selections to my cart]**.

1. Wenden Sie einen oder mehrere Gutscheincodes an, falls verfügbar:

   - Geben Sie **[!UICONTROL Apply Coupon Code]** einen gültigen Gutscheincode ein.

   - Klicken Sie auf _Pfeil_&#x200B;Übernehmen![ ( Pfeilsymbol](../assets/icon-apply-arrow.png) ).

1. Passen Sie die bestellte Menge nach Bedarf an:

   - Geben Sie in der Spalte &quot;**[!UICONTROL Qty]**&quot; des anzupassenden Produkts die richtige Menge ein.

   - Klicken Sie auf **[!UICONTROL Update Items and Quantities]**.

## Bestellung erstellen

1. Klicken Sie auf **[!UICONTROL Create Order]**.

   Auf der Seite _[!UICONTROL Create New Order]_&#x200B;werden die Artikel im Warenkorb angezeigt, gefolgt von den Versand- und Zahlungsinformationen.

1. Füllen Sie die Versand- und Zahlungsinformationen aus.

1. Klicken Sie auf **[!UICONTROL Submit Order]**.

Weitere Informationen finden Sie unter [Bestellung erstellen](customer-account-create-order.md).

## Alle Artikel aus einem Warenkorb entfernen

Das Entfernen aller Artikel aus dem Warenkorb eines Kunden im unterstützten Einkaufsmodus ist nützlich, wenn der Kunde von vorn beginnen möchte, falsche Artikel hinzugefügt hat oder seinen Warenkorb löschen muss, bevor er eine neue Bestellung aufgeben kann. Dadurch wird sichergestellt, dass der Warenkorb nur die Produkte enthält, die der Kunde tatsächlich kaufen möchte.

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Öffnen Sie in der Liste den Kundendatensatz im Bearbeitungsmodus.

1. Klicken Sie in der oberen Schaltflächenleiste auf **[!UICONTROL Manage Shopping Cart]** .

1. Klicken Sie auf **[!UICONTROL Clear my shopping cart]**.

   ![Leeren Sie meinen Warenkorb](./assets/customer-manage-shopping-cart-clear.png){width="600" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL OK]**, wenn Sie zum Bestätigen der Aktion aufgefordert werden.
