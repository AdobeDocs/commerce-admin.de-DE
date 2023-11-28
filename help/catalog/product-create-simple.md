---
title: Einfaches Produkt
description: Erfahren Sie, wie Sie ein einfaches Produkt erstellen, das einzeln oder als Teil eines gruppierten, konfigurierbaren oder gebündelten Produkts verkauft werden kann.
exl-id: 3ac9b28d-3929-4fd6-97ca-145ea6d6897c
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '594'
ht-degree: 0%

---

# Einfaches Produkt

Einer der Schlüssel zur Nutzung der Leistungsfähigkeit von Produktarten besteht darin, zu lernen, wann ein einfaches, eigenständiges Produkt verwendet werden soll. Ein einfaches Produkt kann einzeln oder als Teil eines gruppierten, konfigurierbaren oder gebündelten Produkts verkauft werden. Ein einfaches Produkt mit benutzerdefinierten Optionen wird manchmal auch als _zusammengesetztes Produkt_.

Die folgenden Anweisungen zeigen den Prozess der Erstellung eines einfachen Produkts mit einer [Produktvorlage](attribute-sets.md), erforderliche Felder und grundlegende Einstellungen. Jedes erforderliche Feld ist mit einem roten Sternchen (`*`). Wenn Sie die Grundlagen abgeschlossen haben, können Sie die anderen Produkteinstellungen nach Bedarf abschließen.

![Einfaches Produkt](./assets/product-simple.png){width="700" zoomable="yes"}

## Schritt 1: Produkttyp auswählen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Im _[!UICONTROL Add Product]_( ![Menüpfeil](../assets/icon-menu-down-arrow-red.png){width="25"} ) oben rechts, wählen Sie **[!UICONTROL Simple Product]**.

   ![Einfaches Produkt hinzufügen](./assets/product-add-simple.png){width="700" zoomable="yes"}

## Schritt 2: Attributsatz auswählen

So wählen Sie die [Attributset](attribute-sets.md) wird als Vorlage für das Produkt verwendet:

- Klicken Sie in der **[!UICONTROL Attribute Set]** und geben Sie den gesamten oder einen Teil des Namens des Attributsatzes ein.

- Wählen Sie in der angezeigten Liste den zu verwendenden Attributsatz aus.

Das Formular wird entsprechend der Änderung aktualisiert.

![Attributset auswählen](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

## Schritt 3: Ausführen der erforderlichen Einstellungen

1. Geben Sie die **[!UICONTROL Product Name]**.

1. Standard akzeptieren **[!UICONTROL SKU]** , der auf dem Produktnamen basiert, oder geben Sie einen anderen ein.

1. Produkt eingeben **[!UICONTROL Price]**.

1. Da das Produkt noch nicht zur Veröffentlichung bereit ist, legen Sie die **[!UICONTROL Enable Product]** -Option `No`.

1. click **[!UICONTROL Save]** und fortfahren.

   Wenn das Produkt gespeichert wird, wird die [Store-Ansicht](introduction.md#product-scope) wird in der linken oberen Ecke angezeigt.

1. Wählen Sie die **[!UICONTROL Store View]** wo das Produkt verfügbar sein soll.

   ![Auswählen der Store-Ansicht](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## Schritt 4: Grundlegende Einstellungen durchführen

1. Satz **[!UICONTROL Tax Class]** auf einen der folgenden Werte zu:

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

1. Geben Sie die **[!UICONTROL Quantity]** des vorrätigen Erzeugnisses.

   Standardmäßig ist **[!UICONTROL Stock Status]** auf `In Stock`.

   >[!NOTE]
   >
   >Wenn Sie [Inventory management](../inventory-management/introduction.md), legen Einzelquellenhändler die Menge in diesem Abschnitt fest. Multi-Source-Händler fügen Quellen und Mengen im Bereich Quellen hinzu. Siehe Folgendes _Zuweisen von Quellen und Mengen (Inventory management)_ Abschnitt.

1. Geben Sie die **[!UICONTROL Weight]** des Erzeugnisses.

1. Standard akzeptieren **[!UICONTROL Visibility]** Einstellung von `Catalog, Search`.

1. Zuweisen _[!UICONTROL Categories]_klicken Sie auf das **[!UICONTROL Select…]**und führen Sie einen der folgenden Schritte aus:

   **Vorhandene Kategorie auswählen**:

   - Beginnen Sie mit der Eingabe in das Feld, bis Sie eine Übereinstimmung finden.

   - Aktivieren Sie das Kontrollkästchen der jeweiligen Kategorie, die zugewiesen werden soll.

   **Erstellen einer Kategorie**:

   - Klicken **[!UICONTROL New Category]**.

   - Geben Sie die **[!UICONTROL Category Name]** und wählen Sie **[!UICONTROL Parent Category]**, der seine Position in der Menüstruktur bestimmt.

   - Klicken **[!UICONTROL Create Category]**.

1. So stellen Sie das Produkt in der Liste der [neue Produkte](../content-design/widget-new-products-list.md), wählen Sie die **[!UICONTROL Set Product as New]** aktivieren.

1. Wählen Sie die **[!UICONTROL Country of Manufacture]**.

Es kann zusätzliche individuelle Attribute geben, die das Produkt beschreiben. Die Auswahl variiert je nach Attributsatz und kann zu einem späteren Zeitpunkt abgeschlossen werden.

### Quellen und Mengen zuweisen ([!DNL Inventory Management])

{{$include /help/_includes/inventory-assign-sources.md}}

## Schritt 5: Ausfüllen der Produktinformationen

Scrollen Sie nach unten und füllen Sie die Informationen in den folgenden Abschnitten nach Bedarf aus:

- [Inhalt](product-content.md)
- [Bilder und Videos](product-images-and-video.md)
- [Zugehörige Produkte, Up-Sells und Cross-Sells](related-products-up-sells-cross-sells.md)
- [Suchmaschinenoptimierung](product-search-engine-optimization.md)
- [Anpassbare Optionen](settings-advanced-custom-options.md)
- [Produkte in Websites](settings-basic-websites.md)
- [Design](settings-advanced-design.md)
- [Geschenkoptionen](product-gift-options.md)

## Schritt 6: Produkt veröffentlichen

1. Wenn Sie bereit sind, das Produkt im Katalog zu veröffentlichen, legen Sie die **[!UICONTROL Enable Product]** Switch zu `Yes`.

1. Führen Sie einen der folgenden Schritte aus:

   - **Methode 1:** Speichern und Vorschau anzeigen

      - Klicken Sie oben rechts auf **[!UICONTROL Save]**.

      - Um das Produkt in Ihrem Geschäft anzuzeigen, wählen Sie **[!UICONTROL Customer View]** auf _Admin_ (![Menüpfeil](../assets/icon-menu-down-arrow-black.png)).

     Der Store wird in einer neuen Browser-Registerkarte geöffnet.

     ![Kundenansicht](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   - **Methode 2:** Speichern und schließen

     Im _[!UICONTROL Save]_ ( ![Menüpfeil](../assets/icon-menu-down-arrow-red.png){width="25"} ), wählen Sie **[!UICONTROL Save & Close]**.

## Dinge, die man sich merken sollte

- Einfache Produkte können in konfigurierbare, gebündelte und gruppierte Produktarten enthalten sein.

- Die einfache Produktkonfiguration setzt konfigurierbare Produktkonfigurationen für ein bestimmtes Produkt außer Kraft.

- Ein einfaches Produkt kann über benutzerdefinierte Optionen mit verschiedenen Eingabetypen verfügen, sodass viele Produktvarianten von einer einzigen SKU verkauft werden können.
