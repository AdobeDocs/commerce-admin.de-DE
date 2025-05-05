---
title: Einfaches Produkt
description: Erfahren Sie, wie Sie ein einfaches Produkt erstellen, das einzeln oder als Teil eines gruppierten, konfigurierbaren oder gebündelten Produkts verkauft werden kann.
exl-id: 3ac9b28d-3929-4fd6-97ca-145ea6d6897c
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 0%

---

# Einfaches Produkt

Einer der Schlüssel zur Nutzung der Leistungsfähigkeit von Produktarten besteht darin, zu lernen, wann ein einfaches, eigenständiges Produkt verwendet wird. Ein einfaches Produkt kann einzeln oder als Teil eines gruppierten, konfigurierbaren oder gebündelten Produkts verkauft werden. Ein einfaches Produkt mit benutzerdefinierten Optionen wird manchmal als „zusammengesetztes _&quot;_.

Die folgenden Anweisungen zeigen den Prozess der Erstellung eines einfachen Produkts mithilfe einer [Produktvorlage](attribute-sets.md), erforderlichen Feldern und grundlegenden Einstellungen. Jedes erforderliche Feld ist mit einem roten Sternchen (`*`) gekennzeichnet. Wenn Sie die Grundlagen fertig gestellt haben, können Sie die anderen Produkteinstellungen nach Bedarf abschließen.

![Einfaches Produkt](./assets/product-simple.png){width="700" zoomable="yes"}

## Schritt 1: Produkttyp auswählen

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Wählen Sie oben rechts im Menü _[!UICONTROL Add Product]_![Menüpfeil](../assets/icon-menu-down-arrow-red.png){width="25"} aus,**[!UICONTROL Simple Product]**.

   ![Einfaches Produkt hinzufügen](./assets/product-add-simple.png){width="700" zoomable="yes"}

## Schritt 2: Attributsatz auswählen

So wählen Sie [Attributsatz](attribute-sets.md) aus, der als Vorlage für das Produkt verwendet wird:

- Klicken Sie in das Feld **[!UICONTROL Attribute Set]** und geben Sie den vollständigen oder einen Teil des Namens des Attributsatzes ein.

- Wählen Sie in der angezeigten Liste das Attributset aus, das Sie verwenden möchten.

Das Formular wird mit der Änderung aktualisiert.

![Attributsatz auswählen](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

## Schritt 3: Erforderliche Einstellungen vornehmen

1. Geben Sie die **[!UICONTROL Product Name]** ein.

1. Akzeptieren Sie die **[!UICONTROL SKU]**, die auf dem Produktnamen basiert, oder geben Sie einen anderen ein.

1. Geben Sie die **[!UICONTROL Price]** ein.

1. Da das Produkt noch nicht zur Veröffentlichung bereit ist, setzen Sie die **[!UICONTROL Enable Product]** auf `No`.

1. Klicken Sie auf **[!UICONTROL Save]** und fahren Sie fort.

   Wenn das Produkt gespeichert wird, wird [ Auswahl „Store](introduction.md#product-scope)Ansicht“ in der oberen linken Ecke angezeigt.

1. Wählen Sie die **[!UICONTROL Store View]** aus, in der das Produkt verfügbar sein soll.

   ![Store-Ansicht auswählen](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## Schritt 4: Vervollständigen Sie die Grundeinstellungen

1. Legen Sie **[!UICONTROL Tax Class]** auf eine der folgenden Einstellungen fest:

   - `None`
   - `Taxable Goods`
   - `Refund Adjustments`
   - `Gift Options`
   - `Order Gift Wrapping`
   - `Item Gift Wrapping`
   - `Printed Gift Card`
   - `Reward Points`
   - `VAT Reduced`
   - `VAT Standard`

1. Geben Sie die **[!UICONTROL Quantity]** des Produkts ein, das auf Lager ist.

   Standardmäßig ist **[!UICONTROL Stock Status]** auf `In Stock` festgelegt.

   >[!NOTE]
   >
   >Wenn Sie [Inventory management](../inventory-management/introduction.md) aktivieren, legen Einzelhändler von Source die Menge in diesem Abschnitt fest. Händler, die mehrere Source verwenden, fügen im Abschnitt „Quellen“ Quellen und Mengen hinzu. Siehe folgenden Abschnitt _Zuweisen von Quellen und Mengen (Inventory management_.

1. Geben Sie die **[!UICONTROL Weight]** des Produkts ein.

1. Akzeptieren Sie die **[!UICONTROL Visibility]** Standardeinstellung von `Catalog, Search`.

1. Um dem Produkt _[!UICONTROL Categories]_&#x200B;zuzuweisen, klicken Sie auf das **[!UICONTROL Select…]**&#x200B;und führen Sie einen der folgenden Schritte aus:

   **Vorhandene Kategorie auswählen**:

   - Beginnen Sie mit der Eingabe in das Feld, bis Sie eine Übereinstimmung finden.

   - Aktivieren Sie das Kontrollkästchen jeder Kategorie, die zugewiesen werden soll.

   **Erstellen einer Kategorie**:

   - Klicken Sie auf **[!UICONTROL New Category]**.

   - Geben Sie die **[!UICONTROL Category Name]** ein und wählen Sie die **[!UICONTROL Parent Category]** aus, die ihre Position in der Menüstruktur bestimmt.

   - Klicken Sie auf **[!UICONTROL Create Category]**.

1. Um das Produkt in der Liste der [neuen Produkte](../content-design/widget-new-products-list.md) zu verwenden, aktivieren Sie das Kontrollkästchen **[!UICONTROL Set Product as New]** .

1. Wählen Sie die **[!UICONTROL Country of Manufacture]** aus.

Möglicherweise gibt es zusätzliche individuelle Attribute, die das Produkt beschreiben. Die Auswahl variiert je nach Attributsatz, und Sie können sie später abschließen.

### Zuweisen von Quellen und Mengen ([!DNL Inventory Management])

{{$include /help/_includes/inventory-assign-sources.md}}

## Schritt 5: Füllen Sie die Produktinformationen aus

Scrollen Sie nach unten und füllen Sie die Informationen in den folgenden Abschnitten nach Bedarf aus:

- [Inhalt](product-content.md)
- [Bilder und Videos](product-images-and-video.md)
- [Ähnliche Produkte, Upsell und Crosssell](related-products-up-sells-cross-sells.md)
- [Suchmaschinenoptimierung](product-search-engine-optimization.md)
- [Anpassbare Optionen](settings-advanced-custom-options.md)
- [Produkte in Websites](settings-basic-websites.md)
- [Design](settings-advanced-design.md)
- [Geschenkoptionen](product-gift-options.md)

## Schritt 6: Publish das Produkt

1. Wenn Sie bereit sind, das Produkt im Katalog zu veröffentlichen, legen Sie den **[!UICONTROL Enable Product]** auf `Yes` fest.

1. Führen Sie einen der folgenden Schritte aus:

   - **Methode 1: Speichern** Vorschau

      - Klicken Sie oben rechts auf **[!UICONTROL Save]**.

      - Um das Produkt in Ihrem Geschäft anzuzeigen, wählen Sie **[!UICONTROL Customer View]** im Menü _Admin_ (![Menüpfeil](../assets/icon-menu-down-arrow-black.png)).

     Der Store wird in einer neuen Browser-Registerkarte geöffnet.

     ![Kundenansicht](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   - **Methode 2: Speichern und schließen**

     Wählen Sie im Menü _[!UICONTROL Save]_( ![Menüpfeil](../assets/icon-menu-down-arrow-red.png){width="25"} ) die Option **[!UICONTROL Save & Close]**&#x200B;aus.

## Zu beachtende Dinge

- Einfache Produkte können in konfigurierbare, gebündelte und gruppierte Produktarten aufgenommen werden.

- Eine einfache Produktkonfiguration überschreibt konfigurierbare Produktkonfigurationen für ein bestimmtes Produkt.

- Ein einfaches Produkt kann über benutzerdefinierte Optionen mit verschiedenen Arten von Eingaben verfügen, was es ermöglicht, viele Produktvarianten aus einer einzigen SKU zu verkaufen.
