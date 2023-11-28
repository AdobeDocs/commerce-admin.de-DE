---
title: Virtuelles Produkt
description: Erfahren Sie, wie Sie ein virtuelles Produkt erstellen, das einen nicht materiellen Artikel darstellt, z. B. eine Mitgliedschaft, einen Service, eine Garantie oder ein Abonnement.
exl-id: 8788ba04-e911-429e-9e48-ce589f0c9fa1
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 0%

---

# Virtuelles Produkt

Virtuelle Produkte oder digitale Güter stellen nicht greifbare Elemente dar, wie z. B. Mitgliedschaften, Dienstleistungen, Garantien oder Abonnements und digitale Downloads von Büchern, Musik, Videos oder anderen Produkten. Virtuelle Produkte können einzeln oder im Rahmen der [Gruppierungsprodukt](product-create-grouped.md), [Konfigurierbares Produkt](product-create-configurable.md)oder [Paket-Produkt](product-create-bundle.md) Produktarten.

Abgesehen von der fehlenden _[!UICONTROL Weight]_-Feld, ist der Prozess der Erstellung eines virtuellen Produkts und eines einfachen Produkts identisch. Die folgenden Anweisungen zeigen den Prozess der Erstellung eines virtuellen Produkts mit einer [Produktvorlage](attribute-sets.md), erforderliche Felder und grundlegende Einstellungen. Wenn Sie die Grundlagen abgeschlossen haben, können Sie die anderen Produkteinstellungen nach Bedarf abschließen.

>[!NOTE]
>
>PayPal unterstützt nicht mehr den Verkauf digitaler Waren über PayPal Express Checkout. Es wird empfohlen, [PayPal Payments Standard](../stores-purchase/paypal-payments-standard.md) oder jedes andere PayPal Payment Gateway, um jede Bestellung zu verarbeiten, die virtuelle Produkte enthält.

![Virtuelles Produkt](./assets/product-virtual-membership.png){width="700" zoomable="yes"}

## Schritt 1: Produkttyp auswählen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Im _[!UICONTROL Add Product]_( ![Menüpfeil](../assets/icon-menu-down-arrow-red.png){width="25"} ) in der oberen rechten Ecke auswählen **[!UICONTROL Virtual Product]**.

   ![Virtuelles Produkt hinzufügen](./assets/product-add-virtual.png){width="700" zoomable="yes"}

## Schritt 2: Attributsatz auswählen

So wählen Sie die [Attributset](attribute-sets.md) , die als Vorlage für das Produkt verwendet wird, führen Sie einen der folgenden Schritte aus:

- Klicken Sie in der **[!UICONTROL Attribute Set]** und geben Sie den Namen des Attributsatzes ganz oder teilweise ein.

- Wählen Sie in der angezeigten Liste den zu verwendenden Attributsatz aus.

Das Formular wird entsprechend der Änderung aktualisiert.

![Attributset auswählen](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

## Schritt 3: Ausführen der erforderlichen Einstellungen

1. Geben Sie die **[!UICONTROL Product Name]**.

1. Standard akzeptieren **[!UICONTROL SKU]** , der auf dem Produktnamen basiert, oder geben Sie einen anderen ein.

1. Produkt eingeben **[!UICONTROL Price]**.

1. Da das Produkt noch nicht zur Veröffentlichung bereit ist, legen Sie **[!UICONTROL Enable Product]** nach `No`.

1. Klicks **[!UICONTROL Save]** und fortfahren.

   Wenn das Produkt gespeichert wird, wird die [Store-Ansicht](introduction.md#product-scope) wird in der linken oberen Ecke angezeigt.

1. Wählen Sie die **[!UICONTROL Store View]** wo das Produkt verfügbar sein soll.

   ![Store-Ansicht auswählen](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## Schritt 4: Grundlegende Einstellungen durchführen

1. Satz **[!UICONTROL Tax Class]** auf einen der folgenden Werte zu:

   - `None`
   - `Taxable Goods`

1. Geben Sie die **[!UICONTROL Quantity]** des vorrätigen Produkts und führen Sie folgende Schritte aus:

   - Standard akzeptieren **[!UICONTROL Stock Status]** Einstellung von `In Stock`.

     Da ein virtuelles Produkt nicht ausgeliefert wird, wird die **[!UICONTROL Weight]** nicht verwendet.

   - Standard akzeptieren **[!UICONTROL Visibility]** Einstellung von `Catalog, Search`.

   >[!NOTE]
   >
   >Wenn Sie [Inventory management](../inventory-management/introduction.md), legen Einzelquellenhändler die Menge in diesem Abschnitt fest. Multi-Source-Händler fügen Quellen und Mengen im Abschnitt Quellen hinzu. Siehe Folgendes _Zuweisen von Quellen und Mengen (Inventory management)_ Abschnitt.

1. Zuweisen **[!UICONTROL Categories]** klicken Sie auf das **[!UICONTROL Select…]** und führen Sie einen der folgenden Schritte aus:

   **Vorhandene Kategorie auswählen**:

   - Beginnen Sie mit der Eingabe in das Feld, bis Sie eine Übereinstimmung finden.

   - Aktivieren Sie das Kontrollkästchen der Kategorie, die zugewiesen werden soll.

   **Erstellen einer Kategorie**:

   - Klicken **[!UICONTROL New Category]**.

   - Geben Sie die **[!UICONTROL Category Name]** und wählen Sie **[!UICONTROL Parent Category]**, der seine Position in der Menüstruktur bestimmt.

   - Klicken **[!UICONTROL Create Category]**.

   Es kann zusätzliche individuelle Attribute geben, die das Produkt beschreiben. Die Auswahl variiert je nach Attributsatz und kann zu einem späteren Zeitpunkt abgeschlossen werden.

### Quellen und Mengen zuweisen ([!DNL Inventory Management])

{{$include /help/_includes/inventory-assign-sources.md}}

## Schritt 5: Ausfüllen der Produktinformationen

Füllen Sie die Informationen in den folgenden Abschnitten nach Bedarf aus:

- [Inhalt](product-content.md)
- [Bilder und Videos](product-images-and-video.md)
- [Suchmaschinenoptimierung](product-search-engine-optimization.md)
- [Zugehörige Produkte, Up-Sells und Cross-Sells](related-products-up-sells-cross-sells.md)
- [Anpassbare Optionen](settings-advanced-custom-options.md)
- [Produkte in Websites](settings-basic-websites.md)
- [Design](settings-advanced-design.md)
- [Geschenkoptionen](product-gift-options.md)

>[!NOTE]
>
>Die _[!UICONTROL Is this downloadable product?]_ist standardmäßig deaktiviert. Durch Aktivierung dieser Funktion für ein virtuelles Produkt wird das Produkt [herunterladbar](product-create-downloadable.md#downloadable-product).

## Schritt 6: Produkt veröffentlichen

1. Wenn Sie bereit sind, das Produkt im Katalog zu veröffentlichen, legen Sie **[!UICONTROL Enable Product]** nach `Yes`.

1. Führen Sie einen der folgenden Schritte aus:

   - **Methode 1:** Speichern und Vorschau anzeigen

      - Klicken Sie oben rechts auf **[!UICONTROL Save]**.

      - Um das Produkt in Ihrem Geschäft anzuzeigen, wählen Sie **[!UICONTROL Customer View]** auf _Admin_ ( ![Menüpfeil](../assets/icon-menu-down-arrow-black.png) ).

     Der Store wird in einer neuen Browser-Registerkarte geöffnet.

     ![Kundenansicht](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   - **Methode 2:** Speichern und schließen

     Im _[!UICONTROL Save]_(![Menüpfeil](../assets/icon-menu-down-arrow-red.png){width="25"} ), wählen Sie **[!UICONTROL Save & Close]**.

## Dinge, die man sich merken sollte

- Virtual Produkte werden für nicht materielle Produkte wie Dienste, Abonnements und Garantien verwendet.

- Virtuelle Produkte ähneln einfachen Produkten, aber ohne Gewicht.

- Die Versandoptionen werden beim Checkout nur angezeigt, wenn ein materielles Produkt im Warenkorb vorhanden ist.
