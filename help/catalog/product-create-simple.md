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

Einer der Schlüssel zur Nutzung der Leistungsfähigkeit von Produktarten besteht darin, zu lernen, wann ein einfaches, eigenständiges Produkt verwendet werden soll. Ein einfaches Produkt kann einzeln oder als Teil eines gruppierten, konfigurierbaren oder gebündelten Produkts verkauft werden. Ein einfaches Produkt mit benutzerdefinierten Optionen wird manchmal als _zusammengesetztes Produkt_ bezeichnet.

Die folgenden Anweisungen zeigen den Prozess der Erstellung eines einfachen Produkts mit einer [Produktvorlage](attribute-sets.md), erforderlichen Feldern und grundlegenden Einstellungen. Jedes erforderliche Feld ist mit einem roten Sternchen (`*`) gekennzeichnet. Wenn Sie die Grundlagen abgeschlossen haben, können Sie die anderen Produkteinstellungen nach Bedarf abschließen.

![Einfaches Produkt](./assets/product-simple.png){width="700" zoomable="yes"}

## Schritt 1: Produkttyp auswählen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Wählen Sie im Menü _[!UICONTROL Add Product]_( ![Menüpfeil](../assets/icon-menu-down-arrow-red.png){width="25"} ) oben rechts **[!UICONTROL Simple Product]**aus.

   ![Einfaches Produkt hinzufügen](./assets/product-add-simple.png){width="700" zoomable="yes"}

## Schritt 2: Attributsatz auswählen

So wählen Sie den als Vorlage für das Produkt verwendeten [Attributsatz](attribute-sets.md) aus:

- Klicken Sie in das Feld **[!UICONTROL Attribute Set]** und geben Sie den gesamten oder einen Teil des Namens des Attributsatzes ein.

- Wählen Sie in der angezeigten Liste den zu verwendenden Attributsatz aus.

Das Formular wird entsprechend der Änderung aktualisiert.

![Attributsatz auswählen](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

## Schritt 3: Ausführen der erforderlichen Einstellungen

1. Geben Sie den Wert **[!UICONTROL Product Name]** ein.

1. Nehmen Sie die standardmäßige **[!UICONTROL SKU]** an, die auf dem Produktnamen basiert, oder geben Sie einen anderen ein.

1. Geben Sie das Produkt **[!UICONTROL Price]** ein.

1. Da das Produkt noch nicht zur Veröffentlichung bereit ist, setzen Sie die Option **[!UICONTROL Enable Product]** auf `No`.

1. Klicken Sie auf **[!UICONTROL Save]** und fahren Sie fort.

   Wenn das Produkt gespeichert wird, wird die Auswahl für die [Store-Ansicht](introduction.md#product-scope) in der oberen linken Ecke angezeigt.

1. Wählen Sie die **[!UICONTROL Store View]** aus, in der das Produkt verfügbar sein soll.

   ![Auswählen der Store-Ansicht](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## Schritt 4: Grundlegende Einstellungen durchführen

1. Setzen Sie **[!UICONTROL Tax Class]** auf einen der folgenden Werte:

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

1. Geben Sie den Wert **[!UICONTROL Quantity]** des vorrätigen Produkts ein.

   Standardmäßig ist **[!UICONTROL Stock Status]** auf `In Stock` gesetzt.

   >[!NOTE]
   >
   >Wenn Sie [Inventory management](../inventory-management/introduction.md) aktivieren, legen Einzelhändler der Source die Menge in diesem Abschnitt fest. Mehrere Source-Händler fügen im Bereich Quellen Quellen und Mengen hinzu. Siehe folgenden Abschnitt _Quellen und Mengen zuweisen (Inventory management)_ .

1. Geben Sie den Wert **[!UICONTROL Weight]** des Produkts ein.

1. Nehmen Sie die standardmäßige **[!UICONTROL Visibility]** -Einstellung von `Catalog, Search` an.

1. Um dem Produkt _[!UICONTROL Categories]_zuzuweisen, klicken Sie auf das Feld **[!UICONTROL Select…]**und führen Sie einen der folgenden Schritte aus:

   **Wählen Sie eine vorhandene Kategorie**:

   - Beginnen Sie mit der Eingabe in das Feld, bis Sie eine Übereinstimmung finden.

   - Aktivieren Sie das Kontrollkästchen der jeweiligen Kategorie, die zugewiesen werden soll.

   **Erstellen einer Kategorie**:

   - Klicken Sie auf **[!UICONTROL New Category]**.

   - Geben Sie den Wert **[!UICONTROL Category Name]** ein und wählen Sie den Wert **[!UICONTROL Parent Category]** aus, der seine Position in der Menüstruktur bestimmt.

   - Klicken Sie auf **[!UICONTROL Create Category]**.

1. Um das Produkt in der Liste der [neuen Produkte](../content-design/widget-new-products-list.md) zu kennzeichnen, aktivieren Sie das Kontrollkästchen **[!UICONTROL Set Product as New]** .

1. Wählen Sie die **[!UICONTROL Country of Manufacture]** aus.

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

## Schritt 6: Publish des Produkts

1. Wenn Sie bereit sind, das Produkt im Katalog zu veröffentlichen, setzen Sie den **[!UICONTROL Enable Product]** -Umschalter auf `Yes`.

1. Führen Sie einen der folgenden Schritte aus:

   - **Methode 1:** Speichern und Vorschau anzeigen

      - Klicken Sie in der oberen rechten Ecke auf **[!UICONTROL Save]**.

      - Um das Produkt in Ihrem Store anzuzeigen, wählen Sie im Menü _Admin_ (![Menüpfeil](../assets/icon-menu-down-arrow-black.png)) die Option **[!UICONTROL Customer View]** aus.

     Der Store wird in einer neuen Browser-Registerkarte geöffnet.

     ![Kundenansicht](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   - **Methode 2:** Speichern und schließen

     Wählen Sie im Menü _[!UICONTROL Save]_( ![Menüpfeil](../assets/icon-menu-down-arrow-red.png){width="25"} ) die Option **[!UICONTROL Save & Close]**.

## Dinge, die man sich merken sollte

- Einfache Produkte können in konfigurierbare, gebündelte und gruppierte Produktarten enthalten sein.

- Die einfache Produktkonfiguration setzt konfigurierbare Produktkonfigurationen für ein bestimmtes Produkt außer Kraft.

- Ein einfaches Produkt kann über benutzerdefinierte Optionen mit verschiedenen Eingabetypen verfügen, sodass viele Produktvarianten von einer einzigen SKU verkauft werden können.
