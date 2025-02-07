---
title: Kategorien erstellen
description: Je nach der in der Konfiguration festgelegten maximalen Menütiefe können Sie beliebig viele zusätzliche Unterkategorien erstellen.
exl-id: 8ba5fc1a-3bf2-4a29-bbc3-709fc0ad7497
feature: Catalog Management, Categories
source-git-commit: 6f83e90ed6bacd9e132d5caa01942f0ea90eb4b0
workflow-type: tm+mt
source-wordcount: '1137'
ht-degree: 0%

---

# Kategorien erstellen

Die Kategoriestruktur Ihres Katalogs ist wie ein umgekehrter Baum, wobei das Stammverzeichnis an der Spitze steht. Jeder Abschnitt der Baumstruktur kann erweitert und reduziert werden. Alle deaktivierten oder ausgeblendeten Kategorien werden ausgegraut. Die Kategorien auf der ersten Ebene (unter dem [Stamm](category-root.md)) werden normalerweise als Optionen im [Hauptmenü](navigation-top.md) angezeigt. Je nach der in der Konfiguration festgelegten maximalen Menütiefe können Sie beliebig viele zusätzliche Unterkategorien erstellen. Kategorien können per Drag-and-Drop an andere Stellen in der Baumstruktur verschoben werden. Die Kategorie-ID-Nummer wird oben auf der Seite in Klammern hinter dem Kategorienamen angezeigt.

Bei einer Website mit mehreren [Stores](../stores-purchase/stores.md#add-stores) können Sie für jeden Store eine andere Stammkategorie erstellen, die den Kategoriesatz definiert, der für die &quot;[ Navigation“ verwendet ](navigation-top.md).

![Kategoriestruktur](./assets/category-selected.png){width="700" zoomable="yes"}

## Best Practices

Verwenden Sie diese Best Practices, wenn Sie Kategorien planen und erstellen.

### Kategoriestruktur

Die Struktur der Kategorien im Hauptmenü kann sich auf das Kundenerlebnis und die Leistung auswirken. Als Best Practice sollten Sie eine übergeordnete Kategorie auf höchster Ebene identifizieren und vermeiden, andere Kategorien mit demselben Namen zu haben. Zum Beispiel, anstatt mehrere Kategorien für „Kinder“ in verschiedenen Abteilungen wie `Clothing/Kids`, `Shoes/Kids`, `Accessories/Kids` organisiert zu haben. Es kann effizienter sein, die übergeordnete Kategorie der obersten Ebene `Kids` zu machen und dann unten nach Bedarf Unterkategorien zu erstellen. Konsistent mit der Kategoriestruktur sein und denselben Ansatz für alle Produkttypen in Ihrem Katalog verwenden.

### Geschäftsregeln und Automatisierung

Beachten Sie die Kategoriestruktur und die verfügbaren Attributwerte, wenn Sie Business-Logik verwenden, um ähnliche Elemente auf einer Katalogseite anzuzeigen oder eine personalisierte Promotion, einen automatisierten Prozess oder Suchkriterien einzurichten. Wenn Sie beispielsweise „Polo“ als übergeordnete Kategorie angeben, können die Ergebnisse Produkte mit gemischtem Geschlecht und unangemessenem Alter enthalten. Wenn Sie jedoch eine bestimmte Unterkategorie von Poloshirts abgleichen, sind die Ergebnisse enger und werden wahrscheinlich einen bestimmten Kunden ansprechen. Die Ergebnisse können sogar noch spezifischer sein, wenn sie mit anderen Attributwerten kombiniert werden, die auf einen bestimmten Kunden abzielen. Berücksichtigen Sie die Anzahl der Produkte, die gefiltert und abgerufen werden müssen, wenn auf einen bestimmten Kategoriepfad verwiesen wird. Der Unterschied bei den Ergebnissen kann dramatisch sein. Beachten Sie die verschiedenen Ergebnisse, die von den folgenden Kategoriepfaden zurückgegeben werden:

- `[Category:  All Products/Shirts/Father's Day/Polos/Sale]`
- `[Category Path: Men/Shirts/Polos]`
- `[Child Category: Polos]`

Kategoriale Beziehungen müssen klar definiert werden, z. B.:

- Übergeordnete Kategorie
- Unterkategorie
- Kategoriepfad

Definieren Sie auch alle zugehörigen Keywords und Attribute, z. B.:

- Verfügbarkeit
- Verkaufspreis
- Marke
- Größe
- Farbe

## Schritt 1: Kategorie erstellen

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Legen Sie **[!UICONTROL Store View]** fest, um festzulegen, wo die neue Kategorie verfügbar sein soll.

1. Wählen Sie in der Kategoriestruktur die übergeordnete Kategorie der neuen Kategorie aus.

   Das übergeordnete Element befindet sich eine Ebene über der neuen Kategorie.

   Wenn Sie von Anfang an ohne Daten beginnen, gibt es möglicherweise nur zwei Kategorien in der Liste: _Standardkategorie_, die das Stammverzeichnis ist, und eine _Beispielkategorie_

1. Klicken Sie auf **[!UICONTROL Add Subcategory]**.

## Schritt 2: Vervollständigen Sie die grundlegenden Informationen

1. Wenn die Kategorie sofort im Store verfügbar sein soll, setzen Sie **[!UICONTROL Enable Category]** auf `Yes`.

1. Um die Kategorie in die &quot;[ Navigation“ einzuschließen](navigation-top.md) legen Sie **[!UICONTROL Include in Menu]** auf `Yes` fest.

1. Geben Sie die **[!UICONTROL Category Name]** ein.

   ![Grundlegende Kategorieinformationen](./assets/catalog-categories-currently-active.png){width="500" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Save]** und fahren Sie fort.

## Schritt 3: Kategorieinhalt vervollständigen

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Content]** .

   ![Kategorieinhalt](./assets/category-content.png){width="600" zoomable="yes"}

1. Um eine **[!UICONTROL Category Image]** oben auf der Seite anzuzeigen, können Sie entweder Ihr eigenes Bild hochladen oder ein Bild verwenden, das im [Medienspeicher“ ](../content-design/media-storage.md).

   - Um ein eigenes Bild hochzuladen, klicken Sie auf **[!UICONTROL Upload]** und wählen Sie das Bild aus, das Sie der Kategorie zuordnen möchten.

   - Um Bilder aus dem Medienspeicher zu verwenden, klicken Sie auf **[!UICONTROL Select from Gallery]** und wählen Sie das Bild aus, das die Kategorie darstellen soll.

   Innerhalb der Mediensammlung können Sie auch die [Adobe Stock-Integration](../content-design/adobe-stock.md) verwenden, um durch Klicken auf **[!UICONTROL Search Adobe Stock]** ein passendes Bild zu finden.

   >[!NOTE]
   >
   > Wenn Sie AEM Assets aktiviert haben, finden Sie [Kategorien verwalten](../content-design/aem-assets-manage.md) weitere Informationen.

1. Geben Sie **[!UICONTROL Description]** den Text oder andere Inhalte ein, die auf der Kategorieeinstiegsseite angezeigt werden sollen.

   Weitere Informationen finden Sie unter [Kategorieinhalt](categories-content-settings.md).

1. Um einen Inhaltsbaustein in die Landingpage der Kategorie aufzunehmen, wählen Sie die **[!UICONTROL CMS Block]** aus, die angezeigt werden soll.

1. Klicken Sie auf **[!UICONTROL Save]** und fahren Sie fort.

## Schritt 4: Anzeigeeinstellungen abschließen

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Display Setting]** .

   ![Anzeigeeinstellungen](./assets/category-display-settings.png){width="600" zoomable="yes"}

   Weitere Informationen zu diesen Optionen finden Sie unter Weitere Informationen zu diesen Optionen finden Sie unter [Anzeigeeinstellungen](categories-display-settings.md).

1. Legen Sie **[!UICONTROL Display Mode]** auf eine der folgenden Einstellungen fest:

   - `Products Only`
   - `Static Block Only`
   - `Static Block and Products`

1. Wenn die Kategorieseite den _`Filter by Attribute`_Abschnitt der mehrschichtigen Navigation enthalten soll, setzen Sie **[!UICONTROL Anchor]**auf `Yes`.

1. Wählen Sie für die **[!UICONTROL Available Product Listing Sort By]** Optionen einen oder mehrere der verfügbaren Werte aus, damit Kunden die Liste sortieren können. Diese Einstellung gilt nicht für das [!DNL Live Search] [Widget „Produktauflistungsseite](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-storefront/plp-styling).

   Standardmäßig sind alle verfügbaren Werte enthalten. Deaktivieren Sie das Kontrollkästchen **[!UICONTROL Use All]** , um die Auswahl zu ändern. Die Werte können beispielsweise Folgendes umfassen:

   - `Position`
   - `Product Name`
   - `Price`

1. Um die standardmäßige Sortierreihenfolge für die Kategorie festzulegen, wählen Sie den **[!UICONTROL Default Product Listing Sort By]** aus. Diese Einstellung gilt nicht für das [!DNL Live Search] [Widget „Produktauflistungsseite](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-storefront/plp-styling).

1. Gehen Sie wie folgt vor, um die Standardeinstellung für [ Navigation (](navigation-layered.md#configure-price-navigation)) zu ändern:

   - Deaktivieren Sie das Kontrollkästchen **[!UICONTROL Use Config Settings]** .

   - Geben Sie den Wert ein, der als inkrementeller Preisschritt für die mehrschichtige Navigation verwendet werden soll.

1. Klicken Sie auf **[!UICONTROL Save]** und fahren Sie fort.

## Schritt 5: Vervollständigen Sie die Einstellungen für die Suchmaschinenoptimierung

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Search Engine Optimization Settings]** .

   ![Suchmaschinenoptimierung](./assets/categories-search-engine-optimization.png){width="600" zoomable="yes"}

   Weitere Informationen zu diesen Optionen finden Sie unter [Suchmaschinenoptimierung](categories-search-engine-optimization.md).

1. Füllen Sie die folgenden [Metadaten](../merchandising-promotions/meta-data.md) für die Kategorie aus:

   - [!UICONTROL Meta Title]
   - [!UICONTROL Meta Keywords]
   - [!UICONTROL Meta Description]

1. Klicken Sie auf **[!UICONTROL Save]** und fahren Sie fort.

## Schritt 6: Wählen Sie die Produkte in der Kategorie

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Products in Category]** .

   ![Produkte in Kategorie](./assets/category-products-in-category.png){width="600" zoomable="yes"}

   Weitere Informationen zu diesen Optionen finden Sie unter [Produkte in Kategorie](categories-product-assignments.md).

1. Verwenden Sie bei Bedarf die [Filter](../getting-started/admin-grid-controls.md), um die Produkte zu finden.

   Um alle Datensätze anzuzeigen, die noch nicht in der Kategorie enthalten sind, setzen Sie die Datensatzauswahl in der ersten Spalte auf `No` und klicken Sie auf **[!UICONTROL Search]**.

1. Aktivieren Sie in der ersten Spalte das Kontrollkästchen für jedes Produkt, das in die Kategorie aufgenommen werden soll.

1. Klicken Sie auf **[!UICONTROL Save]** und fahren Sie fort.

## Schritt 7: Festlegen der Kategorieberechtigungen

{{ee-feature}}

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Category Permissions]** .

1. Wählen Sie für eine Installation auf mehreren Sites den **[!UICONTROL Website]** aus, für den die Kategorieberechtigungen gelten.

1. Wählen Sie die **[!UICONTROL Customer Group]** aus, für die die Kategorieberechtigungen gelten.

   ![Adobe Commerce B2B](../assets/b2b.svg) (nur [Adobe Commerce B2B](../b2b/introduction.md)) Bei Bedarf können Sie stattdessen einen **[!UICONTROL Shared Catalog]** auswählen.

1. Legen Sie die folgenden Berechtigungen nach Bedarf fest:

   - [!UICONTROL Browsing Category]
   - [!UICONTROL Display Product Prices]
   - [!UICONTROL Add to Cart]

1. Um eine weitere Berechtigungsregel hinzuzufügen, klicken Sie auf **[!UICONTROL New Permission]** und wiederholen Sie den Vorgang.

   ![Kategorieberechtigungen](./assets/category-create-permissions.png){width="600" zoomable="yes"}

## Schritt 8: Vervollständigen Sie die Designeinstellungen

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Design]** .

1. Legen Sie die Designeinstellungen nach Bedarf fest:

   - ([Nur Adobe Commerce B2B](../b2b/introduction.md)) Wenn Sie die Design-Einstellungen der übergeordneten Kategorie auf diese Kategorie anwenden möchten, setzen Sie **[!UICONTROL Use Parent Category Settings]** auf `Yes`.

   - Um das Design der Kategorieseiten zu ändern, wählen Sie die **[!UICONTROL Theme]** aus, die Sie anwenden möchten.

   - Um das Spalten-Layout der Kategorieseiten zu ändern, wählen Sie die **[!UICONTROL Layout]** aus, die Sie anwenden möchten.

   - Um benutzerdefinierten Code einzugeben, geben Sie gültigen XML-Code in das **[!UICONTROL Layout Update XML]** ein.

   - Um dasselbe Design für Produktseiten zu verwenden, setzen Sie **[!UICONTROL Apply Design to Products]** auf `Yes`.

   ![Designeinstellungen](./assets/category-design.png){width="600" zoomable="yes"}

1. ![Magento Open Source ](../assets/open-source.svg) (nur Magento Open Source) Gehen Sie wie folgt vor, um die Aktualisierung des Designs für einen bestimmten Zeitraum zu planen:

   - Erweitern Sie den Abschnitt _[!UICONTROL Schedule Design Update]_.

   - Verwenden Sie den Kalender (![Kalendersymbol](../assets/icon-calendar.png)), um die **[!UICONTROL from]** und das **[!UICONTROL to]** für die Zeitplanaktualisierung auszuwählen.

   ![Geplante Design-Aktualisierung](./assets/category-scheduled-design-update.png){width="600" zoomable="yes"}

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.
