---
title: Gruppierungsprodukt
description: Erfahren Sie, wie Sie ein gruppiertes Produkt erstellen, das aus einfachen eigenständigen Produkten besteht, die als Gruppe präsentiert werden.
exl-id: af42b7fc-27f2-4c5a-b504-a70a324fae76
feature: Catalog Management, Products
source-git-commit: ce36104913434bb71115e1a5b497f38f75fbd3c5
workflow-type: tm+mt
source-wordcount: '1078'
ht-degree: 0%

---

# Gruppierungsprodukt

Ein gruppiertes Produkt besteht aus einfachen eigenständigen Produkten, die als Gruppe präsentiert werden. Sie können Varianten eines einzelnen Produkts anbieten oder sie nach Saison oder Thema gruppieren. Die Präsentation eines gruppierten Produkts kann einen Anreiz für Kunden schaffen, zusätzliche Artikel zu kaufen. Ein gruppiertes Produkt bietet eine einfache Möglichkeit, Varianten eines Produkts anzubieten und sie alle auf derselben Seite aufzulisten.

Sie können beispielsweise Open Stock-Flachbildschirme verkaufen und alle Arten von Utensilien auflisten, die in einer formalen Platzierungseinstellung verwendet werden. Manche bestellen vielleicht mehrere Salatgabeln, Fischgabeln, Essgabeln, Essmesser, Fischmesser, Buttermesser, Suppenlöffel und Dessert-Löffel. Andere Kunden könnten eine einfache Gabel, ein Messer und einen Löffel bestellen. Kunden können beliebig viele Artikel bestellen.

Obwohl sie als Gruppe präsentiert werden, wird jedes Produkt der Gruppe als separater Artikel gekauft. Im Warenkorb wird jeder Artikel und die gekaufte Menge als separater Zeileneintrag angezeigt.

Die folgenden Anweisungen zeigen den Prozess der Erstellung eines gruppierten Produkts mit einer [Produktvorlage](attribute-sets.md), erforderlichen Feldern und grundlegenden Einstellungen. Jedes erforderliche Feld ist mit einem roten Sternchen (`*`) gekennzeichnet. Wenn Sie die Grundlagen abgeschlossen haben, können Sie die anderen Produkteinstellungen nach Bedarf abschließen.

![Grouped Product](./assets/product-grouped.png){width="700" zoomable="yes"}

## Schritt 1: Produkttyp auswählen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Wählen Sie im Menü _[!UICONTROL Add Product]_( ![Menüpfeil](../assets/icon-menu-down-arrow-red.png){width="25"} ) oben rechts **[!UICONTROL Grouped Product]**aus.

   ![Gruppiertes Produkt hinzufügen](./assets/product-add-grouped.png){width="700" zoomable="yes"}

## Schritt 2: Attributsatz auswählen

Führen Sie einen der folgenden Schritte aus, um den [Attributsatz](attribute-sets.md) auszuwählen, der als Vorlage für das Produkt verwendet wird:

- Um zu suchen, geben Sie den Namen des **[!UICONTROL Attribute Set]** ein.
- Wählen Sie in der Liste den Attributsatz aus, den Sie verwenden möchten.

Das Formular wird entsprechend der Änderung aktualisiert.

![Vorlage auswählen](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

Wenn die erforderlichen Attribute nicht vorhanden sind, können Sie beim Erstellen eines Produkts neue Attribute hinzufügen:

- Klicken Sie in der oberen rechten Ecke auf **[!UICONTROL Add Attribute]**.
- Definieren Sie ein neues Attribut (siehe [Hinzufügen eines Attributs zu einem Produkt](product-attributes-add.md)).

  ![Neues Attribut](./assets/product-attribute-add-select.png){width="600" zoomable="yes"}

Um dem Produkt ein vorhandenes Attribut hinzuzufügen, verwenden Sie die [Filtersteuerelemente](../getting-started/admin-grid-controls.md) , um das Attribut im Raster zu finden, und gehen Sie wie folgt vor:

- Aktivieren Sie das Kontrollkästchen in der ersten Spalte jedes hinzugefügten Attributs.
- Klicken Sie auf **[!UICONTROL Add Selected]**.

## Schritt 3: Ausführen der erforderlichen Einstellungen

1. Geben Sie den Wert **[!UICONTROL Product Name]** ein.

1. Nehmen Sie die standardmäßige **[!UICONTROL SKU]** an, die auf dem Produktnamen basiert, oder geben Sie einen anderen ein.

   Beachten Sie, dass das Feld **[!UICONTROL Quantity]** nicht verfügbar ist, da der Wert aus den einzelnen Produkten der Gruppe abgeleitet wird.

   Ein gruppiertes Produkt hat keinen eigenen Preis im Katalog. Der gruppierte Produktpreis ergibt sich aus dem Preis der einzelnen Produkte, die in der Gruppe enthalten sind.

1. Da das Produkt noch nicht zur Veröffentlichung bereit ist, setzen Sie **[!UICONTROL Enable Product]** auf `No` ( ![Umschalten auf ](../assets/toggle-no.png) ).

1. Klicken Sie auf **[!UICONTROL Save]** und fahren Sie fort.

   Wenn das Produkt gespeichert wird, wird der Produktname oben auf der Seite angezeigt und die Auswahl [Store-Ansicht](introduction.md#product-scope) wird in der oberen linken Ecke angezeigt.

1. Wählen Sie die **[!UICONTROL Store View]** aus, in der das Produkt verfügbar sein soll.

   ![Speicheransicht auswählen](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## Schritt 4: Grundlegende Einstellungen durchführen

1. Nehmen Sie die Einstellung **[!UICONTROL Stock Status]** von `In Stock` an.

1. Um dem Produkt **[!UICONTROL Categories]** zuzuweisen, klicken Sie auf das Feld **[!UICONTROL Select…]** und führen Sie einen der folgenden Schritte aus:

   **Wählen Sie eine vorhandene Kategorie:**

   - Beginnen Sie mit der Eingabe in das Feld, bis Sie eine Übereinstimmung finden.

   - Aktivieren Sie das Kontrollkästchen der Kategorie, die zugewiesen werden soll.

   **Erstellen einer Kategorie:**

   - Klicken Sie auf **[!UICONTROL New Category]**.

   - Geben Sie den Wert **[!UICONTROL Category Name]** ein und wählen Sie den Wert **[!UICONTROL Parent Category]** aus, der seine Position in der Menüstruktur bestimmt.

   - Klicken Sie auf **[!UICONTROL Create Category]**.

1. Nehmen Sie die **[!UICONTROL Visibility]**-Einstellungen von `Catalog, Search` an.

1. Um das Produkt in der [Liste der neuen Produkte](../content-design/widget-new-products-list.md) zu kennzeichnen, wählen Sie die **[!UICONTROL Set Product as New]** **[!UICONTROL from]** - und **[!UICONTROL to]** -Daten im Kalender aus.

1. Wählen Sie die **[!UICONTROL Country of Manufacture]** aus.

   Es kann zusätzliche individuelle Attribute geben, die das Produkt beschreiben. Die Auswahl variiert den Attributsatz und kann später abgeschlossen werden.

## Schritt 5: Produkte zur Gruppe hinzufügen

1. Scrollen Sie nach unten zum Abschnitt **[!UICONTROL Grouped Products]** und klicken Sie auf **[!UICONTROL Add Products to Group]**.

   ![Gruppierte Produkte](./assets/product-grouped-products.png){width="600" zoomable="yes"}

1. Verwenden Sie bei Bedarf die [Filter](../getting-started/admin-grid-controls.md) , um die Produkte zu finden, die Sie in die Gruppe aufnehmen möchten.

1. Aktivieren Sie in der Liste das Kontrollkästchen der einzelnen Elemente, die Sie in die Gruppe aufnehmen möchten.

   >[!NOTE]
   >
   >Nur einfache, herunterladbare und virtuelle Produkte ohne konfigurierbare Optionen können untergeordnete Produkte gruppiert werden. Andere Produkttypen werden nicht in der Auswahlliste angezeigt.

   ![Ausgewählte Produkte hinzufügen](./assets/product-grouped-add-products.png){width="600" zoomable="yes"}

1. Um sie zur Produktgruppe hinzuzufügen, klicken Sie auf **[!UICONTROL Add Selected Products]**.

   Die ausgewählten Produkte werden im Abschnitt _[!UICONTROL Grouped Products]_angezeigt.

   Bei Multi-Source-Händlern mit [Inventory management](../inventory-management/sources-stocks.md) enthält das Raster eine **[!UICONTROL Quantity per Source]** -Spalte mit jeder zugewiesenen Quelle und jedem Lagerbestand.

   ![Produkte in Gruppe](./assets/product-grouped-grouped-products-section.png){width="600" zoomable="yes"}

1. Geben Sie für eines der Elemente den Wert **[!UICONTROL Default Quantity]** ein.

1. Um die Reihenfolge der Produkte zu ändern, ziehen Sie in der ersten Spalte das Symbol _Reihenfolge ändern_ ( ![Positionscontroller](../assets/icon-sort-order.png) ) und ziehen Sie das Produkt an die neue Position in der Liste.

1. Um ein Produkt aus der Gruppe zu entfernen, klicken Sie auf **[!UICONTROL Remove]**.

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

## Schritt 6: Publish des Produkts

1. Wenn Sie bereit sind, das Produkt im Katalog zu veröffentlichen, setzen Sie **[!UICONTROL Enable Product]** auf `Yes`.

1. Führen Sie einen der folgenden Schritte aus:

   **Methode 1:** Speichern und Vorschau anzeigen

   - Klicken Sie in der oberen rechten Ecke auf **[!UICONTROL Save]**.

   - Um das Produkt in Ihrem Store anzuzeigen, wählen Sie im Menü _Admin_ ( ![Menüpfeil](../assets/icon-menu-down-arrow-black.png) ) die Option **[!UICONTROL Customer View]** aus.

     Der Store wird in einer neuen Browser-Registerkarte geöffnet.

     ![Kundenansicht](./assets/product-admin-customer-view.png){width="700" zoomable="yes"}

   **Methode 2:** Speichern und schließen

   - Wählen Sie im Menü _[!UICONTROL Save]_( ![Menüpfeil](../assets/icon-menu-down-arrow-red.png){width="25"} ) die Option **[!UICONTROL Save & Close]**.

## Schritt 7: Konfigurieren Sie die Miniaturansichten des Warenkorbs (optional)

Wenn Sie für jedes Produkt in der Gruppe ein anderes Bild haben, können Sie die Konfiguration so konfigurieren, dass das richtige Bild für die Warenkorbminiatur verwendet wird.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Checkout]** aus.

1. Erweitern Sie ![Erweiterungsselektor](../assets/icon-display-expand.png) den **[!UICONTROL Shopping Cart]**.

   Eine detaillierte Liste dieser Konfigurationsoptionen finden Sie unter [Warenkorb](../configuration-reference/sales/checkout.md#shopping-cart) in der _Konfigurationsreferenz_.

1. Setzen Sie **[!UICONTROL Grouped Product Image]** auf `Product Thumbnail Itself`.

   ![Warenkorb](./assets/config-sales-cart-grouped-product.png){width="600" zoomable="yes"}

   Deaktivieren Sie bei Bedarf das Kontrollkästchen **[!UICONTROL Use system value]** , um diese Option festzulegen.

1. Klicken Sie auf **[!UICONTROL Save Config]**.

## Dinge, die man sich merken sollte

- Ein gruppiertes Produkt ist im Wesentlichen eine Sammlung einfacher verknüpfter Produkte.

- Alle untergeordneten Produkte werden dem gruppierten Produkt **_global_** zugewiesen und nicht zugewiesen. Dies gilt für alle Websites, Stores und Storeansichten gleichzeitig.

- Gruppierte untergeordnete Produkte können einfach, herunterladbar oder virtuelle Produkte **[!UICONTROL without custom options]** sein.

- Jeder gekaufte Artikel erscheint einzeln im Warenkorb und nicht als Teil der Gruppe.

- Ein gruppiertes Produkt hat keinen eigenen Preis im Katalog. Der gruppierte Produktpreis ergibt sich aus dem Preis der einzelnen Produkte, die in der Gruppe enthalten sind.

- Das Miniaturbild im Warenkorb kann so eingestellt werden, dass es das Bild des gruppierten übergeordneten Produkts oder des zugehörigen Produkts anzeigt.
