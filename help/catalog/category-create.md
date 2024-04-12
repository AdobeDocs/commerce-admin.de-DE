---
title: Kategorien erstellen
description: Je nach der in der Konfiguration festgelegten maximalen Menütiefe können Sie beliebig viele weitere Unterkategorien erstellen.
exl-id: 8ba5fc1a-3bf2-4a29-bbc3-709fc0ad7497
feature: Catalog Management, Categories
source-git-commit: b99212b2c6977fc788e75df4bdce608fc4998dc4
workflow-type: tm+mt
source-wordcount: '1128'
ht-degree: 0%

---

# Kategorien erstellen

Die Kategoriestruktur Ihres Katalogs ähnelt einer Aufwärtsstruktur mit der Wurzel oben. Jeder Bereich des Baums kann erweitert und reduziert werden. Alle deaktivierten oder ausgeblendeten Kategorien sind grau ausgeblendet. Die Kategorien auf der ersten Ebene (unterhalb der [root](category-root.md)) wird normalerweise als Optionen in der [Hauptmenü](navigation-top.md). Je nach der in der Konfiguration festgelegten maximalen Menütiefe können Sie beliebig viele weitere Unterkategorien erstellen. Kategorien können per Drag-and-Drop an andere Positionen im Baum gezogen werden. Die Kategorie-ID-Nummer wird in Klammern hinter dem Kategorienamen oben auf der Seite angezeigt.

Für eine Website mit mehreren [Stores](../stores-purchase/stores.md#add-stores)können Sie für jeden Store, der den für die [oberste Navigation](navigation-top.md).

![Kategoriestruktur](./assets/category-selected.png){width="700" zoomable="yes"}

## Best Practices

Verwenden Sie diese Best Practices bei der Planung und Erstellung von Kategorien.

### Kategoriestruktur

Die Struktur der Kategorien im Hauptmenü kann sich auf das Kundenerlebnis und die Leistung auswirken. Als Best Practice sollten Sie eine übergeordnete Kategorie der obersten Ebene identifizieren und vermeiden, dass andere Kategorien denselben Namen haben. Anstatt beispielsweise mehrere Kategorien für &quot;Kinder&quot;in verschiedenen Abteilungen zu organisieren, z. B. `Clothing/Kids`, `Shoes/Kids`, `Accessories/Kids`. Es kann effizienter sein, die übergeordnete Kategorie der obersten Ebene festzulegen `Kids`und erstellen Sie anschließend nach Bedarf Unterkategorien. Halten Sie sich an die Kategoriestruktur und verwenden Sie denselben Ansatz für alle Produktarten in Ihrem Katalog.

### Geschäftsregeln und Automatisierung

Beachten Sie die Kategoriestruktur und die verfügbaren Attributwerte bei der Verwendung der Geschäftslogik, um ähnliche Elemente auf einer Katalogseite anzuzeigen oder um eine personalisierte Promotion, einen automatisierten Prozess oder Suchkriterien einzurichten. Wenn Sie beispielsweise &quot;polo&quot;als übergeordnete Kategorie angeben, können die Ergebnisse Produkte mit gemischtem Geschlecht und altersfremdem Alter umfassen. Wenn Sie jedoch eine bestimmte Unterkategorie von Polohemden auswählen, sind die Ergebnisse enger und können einen bestimmten Kunden ansprechen. Die Ergebnisse können sogar noch spezifischer sein, wenn sie mit anderen Attributwerten kombiniert werden, die auf einen bestimmten Kunden ausgerichtet sind. Betrachten Sie die Anzahl der Produkte, die gefiltert und abgerufen werden müssen, wenn auf einen bestimmten Kategoriepfad verwiesen wird. Der Unterschied in den Ergebnissen kann dramatisch sein. Betrachten Sie die verschiedenen Ergebnisse, die von den folgenden Kategoriepfaden zurückgegeben werden:

- `[Category:  All Products/Shirts/Father's Day/Polos/Sale]`
- `[Category Path: Men/Shirts/Polos]`
- `[Child Category: Polos]`

Es ist wichtig, kategorische Beziehungen klar zu definieren, z. B.:

- übergeordnete Kategorie
- Unterkategorie
- Kategoriepfad

Definieren Sie auch alle zugehörigen Suchbegriffe und Attribute, z. B.:

- Verfügbarkeit
- Verkaufspreis
- Marke
- size
- color

## Schritt 1: Erstellen einer Kategorie

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Satz **[!UICONTROL Store View]** um zu bestimmen, wo die neue Kategorie verfügbar sein soll.

1. Wählen Sie im Kategoriebaum die übergeordnete Kategorie der neuen Kategorie aus.

   Das übergeordnete Element liegt eine Ebene über der neuen Kategorie.

   Wenn Sie von Anfang an ohne Daten beginnen, enthält die Liste möglicherweise nur zwei Kategorien: _Standardkategorie_, das der Stamm ist, und ein _Beispielkategorie_

1. Klicks **[!UICONTROL Add Subcategory]**.

## Schritt 2: Grundlegende Informationen ausfüllen

1. Wenn die Kategorie sofort im Store verfügbar sein soll, legen Sie **[!UICONTROL Enable Category]** nach `Yes`.

1. So fügen Sie die Kategorie in die [oberste Navigation](navigation-top.md), set **[!UICONTROL Include in Menu]** nach `Yes`.

1. Geben Sie die **[!UICONTROL Category Name]**.

   ![Grundlegende Kategoriedaten](./assets/catalog-categories-currently-active.png){width="500" zoomable="yes"}

1. click **[!UICONTROL Save]** und fortfahren.

## Schritt 3: Kategorieinhalt ausfüllen

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Content]** Abschnitt.

   ![Kategorieinhalt](./assets/category-content.png){width="600" zoomable="yes"}

1. So zeigen Sie **[!UICONTROL Category Image]** oben auf der Seite können Sie entweder Ihr eigenes Bild hochladen oder ein Bild verwenden, das in der [Medienspeicher](../content-design/media-storage.md).

   - Um Ihr eigenes Bild hochzuladen, klicken Sie auf **[!UICONTROL Upload]** und wählen Sie das Bild aus, das Sie für die Kategorie darstellen möchten.

   - Um Bilder aus dem Medienspeicher zu verwenden, klicken Sie auf **[!UICONTROL Select from Gallery]** und wählen Sie das Bild aus, das Sie für die Kategorie darstellen möchten.

   >[!NOTE]
   >
   >Innerhalb der Mediengalerie können Sie auch die [Adobe Stock-Integration](../content-design/adobe-stock.md) , um ein passendes Bild zu finden, indem Sie **[!UICONTROL Search Adobe Stock]**.

1. Für **[!UICONTROL Description]**, geben Sie den Text oder anderen Inhalt ein, der auf der Landingpage der Kategorie angezeigt werden soll.

   Weitere Informationen finden Sie unter [Kategorieinhalt](categories-content-settings.md).

1. Um einen Inhaltsbaustein in die Kategorie-Landingpage einzuschließen, wählen Sie die **[!UICONTROL CMS Block]** , die Sie anzeigen möchten.

1. click **[!UICONTROL Save]** und fortfahren.

## Schritt 4: Ausfüllen der Anzeigeeinstellungen

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Display Setting]** Abschnitt.

   ![Anzeigeeinstellungen](./assets/category-display-settings.png){width="600" zoomable="yes"}

   Weitere Informationen zu diesen Optionen finden Sie unter Weitere Informationen zu diesen Optionen finden Sie unter  [Anzeigeeinstellungen](categories-display-settings.md).

1. Satz **[!UICONTROL Display Mode]** auf einen der folgenden Werte zu:

   - `Products Only`
   - `Static Block Only`
   - `Static Block and Products`

1. Wenn Sie möchten, dass die Kategorieseite die _`Filter by Attribute`_Abschnitt mit mehrschichtiger Navigation,**[!UICONTROL Anchor]**nach `Yes`.

1. Für **[!UICONTROL Available Product Listing Sort By]** auswählen, einen oder mehrere der verfügbaren Werte auswählen, die Kunden zum Sortieren der Liste zur Verfügung stehen. Diese Einstellung gilt nicht für die [!DNL Live Search] [Seiten-Widget &quot;Produktliste&quot;](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-storefront/plp-styling).

   Standardmäßig sind alle verfügbaren Werte eingeschlossen. Deaktivieren Sie die **[!UICONTROL Use All]** aktivieren, um die Auswahl zu ändern. Die Werte können beispielsweise Folgendes umfassen:

   - `Position`
   - `Product Name`
   - `Price`

1. Um die standardmäßige Sortierreihenfolge für die Kategorie festzulegen, wählen Sie die **[!UICONTROL Default Product Listing Sort By]** -Wert. Diese Einstellung gilt nicht für die [!DNL Live Search] [Seiten-Widget &quot;Produktliste&quot;](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-storefront/plp-styling).

1. So ändern Sie die Standardnavigation mit Ebenen [Preisschritt](navigation-layered.md#configure-price-navigation) Gehen Sie wie folgt vor:

   - Deaktivieren Sie die **[!UICONTROL Use Config Settings]** aktivieren.

   - Geben Sie den Wert ein, der als inkrementeller Preisschritt für die Navigation mit Ebenen verwendet werden soll.

1. Klicks **[!UICONTROL Save]** und fortfahren.

## Schritt 5: Suchmaschinen-Optimierungseinstellungen durchführen

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Search Engine Optimization Settings]** Abschnitt.

   ![Suchmaschinenoptimierung](./assets/categories-search-engine-optimization.png){width="600" zoomable="yes"}

   Weitere Informationen zu diesen Optionen finden Sie unter [Suchmaschinenoptimierung](categories-search-engine-optimization.md).

1. Führen Sie Folgendes aus: [Metadaten](../merchandising-promotions/meta-data.md) für die Kategorie:

   - [!UICONTROL Meta Title]
   - [!UICONTROL Meta Keywords]
   - [!UICONTROL Meta Description]

1. Klicks **[!UICONTROL Save]** und fortfahren.

## Schritt 6: Auswählen der Produkte in der Kategorie

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Products in Category]** Abschnitt.

   ![Produkte der Kategorie](./assets/category-products-in-category.png){width="600" zoomable="yes"}

   Weitere Informationen zu diesen Optionen finden Sie unter [Produkte der Kategorie](categories-product-assignments.md).

1. Verwenden Sie bei Bedarf die [Filter](../getting-started/admin-grid-controls.md) um die Produkte zu finden.

   Um alle noch nicht in der Kategorie enthaltenen Datensätze anzuzeigen, wählen Sie in der ersten Spalte den Wert `No` und klicken **[!UICONTROL Search]**.

1. Aktivieren Sie in der ersten Spalte das Kontrollkästchen für jedes Produkt, das in die Kategorie aufgenommen werden soll.

1. Klicks **[!UICONTROL Save]** und fortfahren.

## Schritt 7: Festlegen der Kategorieberechtigungen

{{ee-feature}}

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Category Permissions]** Abschnitt.

1. Wählen Sie für eine Installation mit mehreren Sites die **[!UICONTROL Website]** wo die Kategorieberechtigungen gelten.

1. Wählen Sie die **[!UICONTROL Customer Group]** wo die Kategorieberechtigungen gelten.

   ![B2B für Adobe Commerce](../assets/b2b.svg) ([B2B für Adobe Commerce](../b2b/introduction.md) nur) Bei Bedarf können Sie eine **[!UICONTROL Shared Catalog]** anstatt.

1. Legen Sie die folgenden Berechtigungen nach Bedarf fest:

   - [!UICONTROL Browsing Category]
   - [!UICONTROL Display Product Prices]
   - [!UICONTROL Add to Cart]

1. Um eine weitere Berechtigungsregel hinzuzufügen, klicken Sie auf **[!UICONTROL New Permission]** und wiederholen Sie den Vorgang.

   ![Kategorienberechtigungen](./assets/category-create-permissions.png){width="600" zoomable="yes"}

## Schritt 8: Fertigstellen der Designeinstellungen

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Design]** Abschnitt.

1. Legen Sie die Designeinstellungen nach Bedarf fest:

   - ([B2B für Adobe Commerce](../b2b/introduction.md) nur) Um die Design-Einstellungen der übergeordneten Kategorie auf diese Kategorie anzuwenden, legen Sie **[!UICONTROL Use Parent Category Settings]** nach `Yes`.

   - Um das Design der Kategorieseiten zu ändern, wählen Sie die **[!UICONTROL Theme]** die Sie anwenden möchten.

   - Um das Spaltenlayout der Kategorieseiten zu ändern, wählen Sie die **[!UICONTROL Layout]** die Sie anwenden möchten.

   - Um benutzerdefinierten Code einzugeben, geben Sie gültigen XML-Code in die **[!UICONTROL Layout Update XML]** ankreuzen.

   - Um dasselbe Design für Produktseiten zu verwenden, legen Sie **[!UICONTROL Apply Design to Products]** nach `Yes`.

   ![Designeinstellungen](./assets/category-design.png){width="600" zoomable="yes"}

1. ![Magento Open Source](../assets/open-source.svg) (Nur Magento Open Source) Gehen Sie wie folgt vor, um das Design-Update für einen bestimmten Zeitraum zu planen:

   - Erweitern Sie die _[!UICONTROL Schedule Design Update]_Abschnitt.

   - Verwenden Sie den Kalender (![Kalendersymbol](../assets/icon-calendar.png)), um den Zeitplan für die Aktualisierung auszuwählen. **[!UICONTROL from]** und **[!UICONTROL to]** Daten.

   ![Geplantes Design-Update](./assets/category-scheduled-design-update.png){width="600" zoomable="yes"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]**.
