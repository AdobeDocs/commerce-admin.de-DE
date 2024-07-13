---
title: Virtuelles Produkt
description: Erfahren Sie, wie Sie ein virtuelles Produkt erstellen, das einen nicht materiellen Artikel darstellt, z. B. eine Mitgliedschaft, einen Service, eine Garantie oder ein Abonnement.
exl-id: 8788ba04-e911-429e-9e48-ce589f0c9fa1
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 0%

---

# Virtuelles Produkt

Virtuelle Produkte oder digitale Güter stellen nicht greifbare Elemente dar, wie z. B. Mitgliedschaften, Dienstleistungen, Garantien oder Abonnements und digitale Downloads von Büchern, Musik, Videos oder anderen Produkten. Virtual Produkte können einzeln oder als Teil der Produktarten [Grouped Product](product-create-grouped.md), [Configurable Product](product-create-configurable.md) oder [Bundle Product](product-create-bundle.md) verkauft werden.

Abgesehen von der Abwesenheit des Felds _[!UICONTROL Weight]_ist der Prozess der Erstellung eines virtuellen Produkts und eines einfachen Produkts identisch. Die folgenden Anweisungen zeigen den Prozess der Erstellung eines virtuellen Produkts mit einer [Produktvorlage](attribute-sets.md), erforderlichen Feldern und grundlegenden Einstellungen. Wenn Sie die Grundlagen abgeschlossen haben, können Sie die anderen Produkteinstellungen nach Bedarf abschließen.

>[!NOTE]
>
>PayPal unterstützt nicht mehr den Verkauf digitaler Waren über PayPal Express Checkout. Es wird empfohlen, entweder [PayPal Payments Standard](../stores-purchase/paypal-payments-standard.md) oder ein anderes PayPal Payment Gateway zu verwenden, um alle Bestellungen zu verarbeiten, die virtuelle Produkte enthalten.

![Virtual Product](./assets/product-virtual-membership.png){width="700" zoomable="yes"}

## Schritt 1: Produkttyp auswählen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Wählen Sie im Menü _[!UICONTROL Add Product]_( ![Menüpfeil](../assets/icon-menu-down-arrow-red.png){width="25"} ) oben rechts **[!UICONTROL Virtual Product]**aus.

   ![Virtuelles Produkt hinzufügen](./assets/product-add-virtual.png){width="700" zoomable="yes"}

## Schritt 2: Attributsatz auswählen

Führen Sie einen der folgenden Schritte aus, um den [Attributsatz](attribute-sets.md) auszuwählen, der als Vorlage für das Produkt verwendet wird:

- Klicken Sie in das Feld **[!UICONTROL Attribute Set]** und geben Sie den gesamten oder einen Teil des Namens des Attributsatzes ein.

- Wählen Sie in der angezeigten Liste den zu verwendenden Attributsatz aus.

Das Formular wird entsprechend der Änderung aktualisiert.

![Attributsatz auswählen](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

## Schritt 3: Ausführen der erforderlichen Einstellungen

1. Geben Sie den Wert **[!UICONTROL Product Name]** ein.

1. Nehmen Sie die standardmäßige **[!UICONTROL SKU]** an, die auf dem Produktnamen basiert, oder geben Sie einen anderen ein.

1. Geben Sie das Produkt **[!UICONTROL Price]** ein.

1. Da das Produkt noch nicht zur Veröffentlichung bereit ist, setzen Sie **[!UICONTROL Enable Product]** auf `No`.

1. Klicken Sie auf **[!UICONTROL Save]** und fahren Sie fort.

   Wenn das Produkt gespeichert wird, wird die Auswahl für die [Store-Ansicht](introduction.md#product-scope) in der oberen linken Ecke angezeigt.

1. Wählen Sie die **[!UICONTROL Store View]** aus, in der das Produkt verfügbar sein soll.

   ![Speicheransicht auswählen](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## Schritt 4: Grundlegende Einstellungen durchführen

1. Setzen Sie **[!UICONTROL Tax Class]** auf einen der folgenden Werte:

   - `None`
   - `Taxable Goods`

1. Geben Sie den Wert **[!UICONTROL Quantity]** des vorrätigen Produkts ein und führen Sie folgende Schritte aus:

   - Nehmen Sie die standardmäßige **[!UICONTROL Stock Status]** -Einstellung von `In Stock` an.

     Da ein virtuelles Produkt nicht ausgeliefert wird, wird das Feld **[!UICONTROL Weight]** nicht verwendet.

   - Nehmen Sie die standardmäßige **[!UICONTROL Visibility]** -Einstellung von `Catalog, Search` an.

   >[!NOTE]
   >
   >Wenn Sie [Inventory management](../inventory-management/introduction.md) aktivieren, legen Einzelquellenhändler die Menge in diesem Abschnitt fest. Multi-Source-Händler fügen Quellen und Mengen im Abschnitt Quellen hinzu. Siehe folgenden Abschnitt _Quellen und Mengen zuweisen (Inventory management)_ .

1. Um dem Produkt **[!UICONTROL Categories]** zuzuweisen, klicken Sie auf das Feld **[!UICONTROL Select…]** und führen Sie einen der folgenden Schritte aus:

   **Wählen Sie eine vorhandene Kategorie**:

   - Beginnen Sie mit der Eingabe in das Feld, bis Sie eine Übereinstimmung finden.

   - Aktivieren Sie das Kontrollkästchen der Kategorie, die zugewiesen werden soll.

   **Erstellen einer Kategorie**:

   - Klicken Sie auf **[!UICONTROL New Category]**.

   - Geben Sie den Wert **[!UICONTROL Category Name]** ein und wählen Sie den Wert **[!UICONTROL Parent Category]** aus, der seine Position in der Menüstruktur bestimmt.

   - Klicken Sie auf **[!UICONTROL Create Category]**.

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
>Die Option _[!UICONTROL Is this downloadable product?]_ist standardmäßig deaktiviert. Durch Aktivierung dieser Funktion für ein virtuelles Produkt ist das Produkt [herunterladbar](product-create-downloadable.md#downloadable-product).

## Schritt 6: Publish des Produkts

1. Wenn Sie bereit sind, das Produkt im Katalog zu veröffentlichen, setzen Sie **[!UICONTROL Enable Product]** auf `Yes`.

1. Führen Sie einen der folgenden Schritte aus:

   - **Methode 1:** Speichern und Vorschau anzeigen

      - Klicken Sie oben rechts auf **[!UICONTROL Save]**.

      - Um das Produkt in Ihrem Store anzuzeigen, wählen Sie im Menü _Admin_ ( ![Menüpfeil](../assets/icon-menu-down-arrow-black.png) ) die Option **[!UICONTROL Customer View]** aus.

     Der Store wird in einer neuen Browser-Registerkarte geöffnet.

     ![Kundenansicht](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   - **Methode 2:** Speichern und schließen

     Wählen Sie im Menü _[!UICONTROL Save]_(![Menüpfeil](../assets/icon-menu-down-arrow-red.png){width="25"} ) die Option **[!UICONTROL Save & Close]**.

## Dinge, die man sich merken sollte

- Virtual Produkte werden für nicht materielle Produkte wie Dienste, Abonnements und Garantien verwendet.

- Virtuelle Produkte ähneln einfachen Produkten, aber ohne Gewicht.

- Die Versandoptionen werden beim Checkout nur angezeigt, wenn ein materielles Produkt im Warenkorb vorhanden ist.
