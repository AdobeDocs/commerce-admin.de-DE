---
title: Gruppiertes Produkt
description: Erfahren Sie, wie Sie ein gruppiertes Produkt erstellen, das aus einfachen eigenständigen Produkten besteht, die als Gruppe präsentiert werden.
exl-id: af42b7fc-27f2-4c5a-b504-a70a324fae76
feature: Catalog Management, Products
source-git-commit: ce36104913434bb71115e1a5b497f38f75fbd3c5
workflow-type: tm+mt
source-wordcount: '1078'
ht-degree: 0%

---

# Gruppiertes Produkt

Ein gruppiertes Produkt besteht aus einfachen eigenständigen Produkten, die als Gruppe präsentiert werden. Sie können Varianten eines einzelnen Produkts anbieten oder sie nach Saison oder Thema gruppieren. Die Präsentation eines gruppierten Produkts kann einen Anreiz für Kunden schaffen, zusätzliche Artikel zu kaufen. Ein gruppiertes Produkt bietet eine einfache Möglichkeit, Varianten eines Produkts anzubieten und sie alle auf derselben Seite aufzulisten.

Zum Beispiel könnten Sie offene Stock-Besteck verkaufen und alle Arten von Utensilien auflisten, die in einer formellen Umgebung verwendet werden. Manche bestellen vielleicht mehrere Salatgabeln, Fischgabeln, Essgabeln, Essensmesser, Fischmesser, Buttermesser, Suppenlöffel und Dessertlöffel. Andere Kunden könnten eine einfache Gabel, ein Messer und einen Löffel bestellen. Kunden können beliebig viele Artikel bestellen.

Obwohl sie als Gruppe präsentiert werden, wird jedes Produkt in der Gruppe als separater Artikel gekauft. Im Warenkorb wird jeder Artikel und die gekaufte Menge als separater Zeileneintrag angezeigt.

Die folgenden Anweisungen zeigen den Prozess der Erstellung eines gruppierten Produkts mithilfe einer [Produktvorlage](attribute-sets.md), erforderlichen Feldern und grundlegenden Einstellungen. Jedes erforderliche Feld ist mit einem roten Sternchen (`*`) gekennzeichnet. Wenn Sie die Grundlagen fertig gestellt haben, können Sie die anderen Produkteinstellungen nach Bedarf abschließen.

![Gruppiertes Produkt](./assets/product-grouped.png){width="700" zoomable="yes"}

## Schritt 1: Produkttyp auswählen

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Wählen Sie im Menü _[!UICONTROL Add Product]_![Menüpfeil](../assets/icon-menu-down-arrow-red.png){width="25"} oben rechts **[!UICONTROL Grouped Product]**aus.

   ![Gruppiertes Produkt hinzufügen](./assets/product-add-grouped.png){width="700" zoomable="yes"}

## Schritt 2: Attributsatz auswählen

Um den [Attributsatz](attribute-sets.md) auszuwählen, der als Vorlage für das Produkt verwendet wird, führen Sie einen der folgenden Schritte aus:

- Geben Sie zum Suchen den Namen der **[!UICONTROL Attribute Set]** ein.
- Wählen Sie in der Liste den Attributsatz aus, den Sie verwenden möchten.

Das Formular wird mit der Änderung aktualisiert.

![Vorlage wählen](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

Wenn die erforderlichen Attribute nicht vorhanden sind, können Sie beim Erstellen eines Produkts neue Attribute hinzufügen:

- Klicken Sie oben rechts auf **[!UICONTROL Add Attribute]**.
- Definieren Sie ein neues Attribut (siehe [Hinzufügen eines Attributs zu einem Produkt](product-attributes-add.md)).

  ![Neues Attribut](./assets/product-attribute-add-select.png){width="600" zoomable="yes"}

Um dem Produkt ein vorhandenes Attribut hinzuzufügen, verwenden Sie die [Filtersteuerelemente](../getting-started/admin-grid-controls.md), um das Attribut im Raster zu finden, und führen Sie folgende Schritte aus:

- Aktivieren Sie das Kontrollkästchen in der ersten Spalte jedes hinzuzufügenden Attributs.
- Klicken Sie auf **[!UICONTROL Add Selected]**.

## Schritt 3: Erforderliche Einstellungen vornehmen

1. Geben Sie die **[!UICONTROL Product Name]** ein.

1. Akzeptieren Sie die **[!UICONTROL SKU]**, die auf dem Produktnamen basiert, oder geben Sie einen anderen ein.

   Beachten Sie, dass das Feld **[!UICONTROL Quantity]** nicht verfügbar ist, da der Wert aus den einzelnen Produkten der Gruppe abgeleitet wird.

   Ein gruppiertes Produkt hat keinen eigenen Preis im Katalog. Der Preis der zusammengeführten Produkte wird aus dem Preis der einzelnen Produkte abgeleitet, die in der Gruppe enthalten sind.

1. Da das Produkt noch nicht zur Veröffentlichung bereit ist, setzen Sie **[!UICONTROL Enable Product]** auf `No` ( ![Umschalten auf](../assets/toggle-no.png) ).

1. Klicken Sie auf **[!UICONTROL Save]** und fahren Sie fort.

   Wenn das Produkt gespeichert wird, wird der Produktname oben auf der Seite angezeigt und die [Store-Ansicht](introduction.md#product-scope)-Auswahl wird in der oberen linken Ecke angezeigt.

1. Wählen Sie die **[!UICONTROL Store View]** aus, in der das Produkt verfügbar sein soll.

   ![Store-Ansicht auswählen](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## Schritt 4: Vervollständigen Sie die Grundeinstellungen

1. Akzeptieren Sie die **[!UICONTROL Stock Status]** von `In Stock`.

1. Um dem Produkt **[!UICONTROL Categories]** zuzuweisen, klicken Sie auf das **[!UICONTROL Select…]** und führen Sie einen der folgenden Schritte aus:

   **Vorhandene Kategorie auswählen:**

   - Beginnen Sie mit der Eingabe in das Feld, bis Sie eine Übereinstimmung finden.

   - Aktivieren Sie das Kontrollkästchen der Kategorie, die zugewiesen werden soll.

   **Erstellen einer Kategorie:**

   - Klicken Sie auf **[!UICONTROL New Category]**.

   - Geben Sie die **[!UICONTROL Category Name]** ein und wählen Sie die **[!UICONTROL Parent Category]** aus, die ihre Position in der Menüstruktur bestimmt.

   - Klicken Sie auf **[!UICONTROL Create Category]**.

1. Akzeptieren Sie die **[!UICONTROL Visibility]** von `Catalog, Search`.

1. Um das Produkt in der [Liste neuer Produkte“ ](../content-design/widget-new-products-list.md), wählen Sie die **[!UICONTROL Set Product as New]** **[!UICONTROL from]** und **[!UICONTROL to]** im Kalender aus.

1. Wählen Sie die **[!UICONTROL Country of Manufacture]** aus.

   Möglicherweise gibt es zusätzliche individuelle Attribute, die das Produkt beschreiben. Die Auswahl variiert im Attributsatz und kann später abgeschlossen werden.

## Schritt 5: Hinzufügen von Produkten zur Gruppe

1. Scrollen Sie nach unten zum Abschnitt **[!UICONTROL Grouped Products]** und klicken Sie auf **[!UICONTROL Add Products to Group]**.

   ![Gruppierte Produkte](./assets/product-grouped-products.png){width="600" zoomable="yes"}

1. Verwenden Sie bei Bedarf [Filter](../getting-started/admin-grid-controls.md), um die Produkte zu finden, die Sie in die Gruppe aufnehmen möchten.

1. Aktivieren Sie in der Liste das Kontrollkästchen jedes Elements, das Sie in die Gruppe aufnehmen möchten.

   >[!NOTE]
   >
   >Nur einfache, herunterladbare und virtuelle Produkte ohne konfigurierbare Optionen können in untergeordneten Produkten gruppiert werden. Andere Produktarten werden nicht in der Auswahlliste angezeigt.

   ![Ausgewählte Produkte hinzufügen](./assets/product-grouped-add-products.png){width="600" zoomable="yes"}

1. Um sie der Produktgruppe hinzuzufügen, klicken Sie auf **[!UICONTROL Add Selected Products]**.

   Die ausgewählten Produkte werden im Abschnitt _[!UICONTROL Grouped Products]_angezeigt.

   Bei Multi-Source-Händlern mit [Inventory management](../inventory-management/sources-stocks.md) enthält das Raster eine **[!UICONTROL Quantity per Source]** mit jeder zugewiesenen Quell- und Lagerbestandsmenge.

   ![Produkte in Gruppe](./assets/product-grouped-grouped-products-section.png){width="600" zoomable="yes"}

1. Geben Sie einen **[!UICONTROL Default Quantity]** für einen der Artikel ein.

1. Um die Reihenfolge der Produkte zu ändern, greifen Sie das Symbol _Reihenfolge ändern_ ( ![Positionscontroller](../assets/icon-sort-order.png) ) in der ersten Spalte und ziehen Sie das Produkt an die neue Position in der Liste.

1. Um ein Produkt aus der Gruppe zu entfernen, klicken Sie auf **[!UICONTROL Remove]**.

## Schritt 5: Füllen Sie die Produktinformationen aus

Füllen Sie die Informationen in den folgenden Abschnitten nach Bedarf aus:

- [Inhalt](product-content.md)
- [Bilder und Videos](product-images-and-video.md)
- [Suchmaschinenoptimierung](product-search-engine-optimization.md)
- [Ähnliche Produkte, Upsell und Crosssell](related-products-up-sells-cross-sells.md)
- [Anpassbare Optionen](settings-advanced-custom-options.md)
- [Produkte in Websites](settings-basic-websites.md)
- [Design](settings-advanced-design.md)
- [Geschenkoptionen](product-gift-options.md)

## Schritt 6: Publish das Produkt

1. Wenn Sie bereit sind, das Produkt im Katalog zu veröffentlichen, legen Sie **[!UICONTROL Enable Product]** auf `Yes` fest.

1. Führen Sie einen der folgenden Schritte aus:

   **Methode 1: Speichern** Vorschau

   - Klicken Sie oben rechts auf **[!UICONTROL Save]**.

   - Um das Produkt in Ihrem Geschäft anzuzeigen, wählen Sie **[!UICONTROL Customer View]** im Menü _Admin_ ( ![Menüpfeil](../assets/icon-menu-down-arrow-black.png) ).

     Der Store wird in einer neuen Browser-Registerkarte geöffnet.

     ![Kundenansicht](./assets/product-admin-customer-view.png){width="700" zoomable="yes"}

   **Methode 2: Speichern und schließen**

   - Wählen Sie im Menü _[!UICONTROL Save]_( ![Menüpfeil](../assets/icon-menu-down-arrow-red.png){width="25"} ) die Option **[!UICONTROL Save & Close]**aus.

## Schritt 7: Konfigurieren der Miniaturen für den Warenkorb (optional)

Wenn Sie für jedes Produkt in der Gruppe ein anderes Bild haben, können Sie die Konfiguration so einrichten, dass das richtige Bild für die Miniaturansicht des Warenkorbs verwendet wird.

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Checkout]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Shopping Cart]**.

   Eine detaillierte Liste dieser Konfigurationsoptionen finden Sie unter [Warenkorb](../configuration-reference/sales/checkout.md#shopping-cart) in _Konfigurationsreferenz_.

1. Legen Sie **[!UICONTROL Grouped Product Image]** auf `Product Thumbnail Itself` fest.

   ![Einkaufswagen](./assets/config-sales-cart-grouped-product.png){width="600" zoomable="yes"}

   Deaktivieren Sie bei Bedarf das Kontrollkästchen **[!UICONTROL Use system value]** , um diese Option festzulegen.

1. Klicken Sie auf **[!UICONTROL Save Config]**.

## Zu beachtende Dinge

- Ein gruppiertes Produkt ist im Wesentlichen eine Sammlung von einfachen zugehörigen Produkten.

- Alle untergeordneten Produkte werden dem gruppierten Produkt (global **_für alle Websites_** Stores und Store-Ansichten gleichzeitig zugewiesen und deren Zuweisung aufgehoben.

- Gruppierte untergeordnete Produkte können **[!UICONTROL without custom options]** einfache, herunterladbare oder virtuelle Produkte sein.

- Jeder gekaufte Artikel wird einzeln im Warenkorb angezeigt und nicht als Teil der Gruppe.

- Ein gruppiertes Produkt hat keinen eigenen Preis im Katalog. Der Preis der zusammengeführten Produkte wird aus dem Preis der einzelnen Produkte abgeleitet, die in der Gruppe enthalten sind.

- Das Miniaturbild im Warenkorb kann so eingestellt werden, dass das Bild vom gruppierten übergeordneten Produkt oder dem zugehörigen Produkt angezeigt wird.
