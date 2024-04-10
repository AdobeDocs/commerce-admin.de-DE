---
title: Mehrschichtige Navigation
description: Erfahren Sie, wie die mehrschichtige Navigation es Käufern erleichtert, Produkte anhand der Kategorie, der Preisspanne oder eines anderen verfügbaren Attributs zu finden.
exl-id: 5f17528a-3593-449c-a044-98736a4ae913
feature: Catalog Management, Categories, Site Navigation
source-git-commit: 99049260b4ff490845affd1c98fa4d2536edebd7
workflow-type: tm+mt
source-wordcount: '1303'
ht-degree: 0%

---

# Mehrschichtige Navigation

>[!NOTE]
>
>Die in diesem Abschnitt beschriebene standardmäßige mehrschichtige Navigation unterscheidet sich von der mit gefilterten Live Search-Navigation [Facetten](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/live-search-admin/facets/facets.html).

Die mehrschichtige Navigation erleichtert die Suche nach Produkten basierend auf der Kategorie, der Preisspanne oder einem anderen verfügbaren Attribut. Die mehrschichtige Navigation wird normalerweise in der linken Spalte der Suchergebnisse und Kategorieseiten und manchmal auf der Startseite angezeigt. Die Standardnavigation umfasst ein _Shoppen nach_ Liste der Kategorien und Preisspanne. Sie können die Anzeige der mehrschichtigen Navigation konfigurieren, einschließlich Produktanzahl und Preisspanne.

![Mehrschichtige Navigation nach Kategorie und Preis](./assets/navigation-layered-basic.png){width="700" zoomable="yes"}

## Filterbare Attribute

>[!NOTE]
>
>Die in diesem Thema beschriebenen Anforderungen an filterbare Attribute unterscheiden sich für [Live Search](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html). Weitere Informationen finden Sie unter [Facetten](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/live-search-admin/facets/facets.html).

Die mehrschichtige Navigation kann verwendet werden, um nach Produkten nach Kategorie oder Attribut zu suchen. Wenn beispielsweise ein Käufer die Kategorie Herren/Shorts in der oberen Navigation auswählt, umfassen die ersten Ergebnisse alle Produkte in der Kategorie. Die Liste kann weiter gefiltert werden, indem ein bestimmter Stil, ein bestimmtes Klima, eine bestimmte Farbe, ein bestimmtes Material, ein bestimmtes Muster oder ein bestimmter Preis - oder eine Kombination von Werten - ausgewählt wird. Filterbare Attribute werden in einem sich erweiternden Abschnitt angezeigt, in dem jeder Attributwert aufgelistet wird. Optional kann die Liste der Produkte mit übereinstimmenden Ergebnissen so konfiguriert werden, dass Produkte mit oder ohne Übereinstimmung einbezogen werden.

Die Attributeigenschaften bestimmen in Kombination mit dem Produkteingabetyp, welche Attribute für die mehrschichtige Navigation verwendet werden können. Die mehrschichtige Navigation ist nur für verfügbar. [_Anker_](categories-display-settings.md) Kategorien, können aber auch zu Suchergebnisseiten hinzugefügt werden. Die **Katalogeingabetyp für Store-Inhaber** Die -Eigenschaft jedes Attributs muss auf Folgendes festgelegt sein `Yes/No`, `Dropdown`, `Multiple Select`, oder `Price`. Damit die Attribute gefiltert werden können, **Verwendung in der mehrschichtigen Navigation** Die -Eigenschaft von muss jeweils auf Folgendes festgelegt sein `Filterable (with results)` oder `Filterable (no results)`.

_Beispiel: Filterbare Attribute mit Ergebnissen_

![Filterbare Attribute in der mehrschichtigen Navigation](./assets/storefront-layered-navigation-filtered.png){width="700" zoomable="yes"}

_Beispiel: Filterbare Farbfeldwerte werden ohne Ergebnis angezeigt_

![Filterbarer Farbfeldwert ohne Ergebnisse](./assets/storefront-product-attribute-filter-no-results.png){width="700" zoomable="yes"}

Die folgenden Anweisungen zeigen, wie Sie eine einfache mehrschichtige Navigation mit filterbaren Attributen einrichten. Eine erweiterte mehrschichtige Navigation mit Preisschritten finden Sie unter [Preisnavigation](navigation-layered.md#configure-price-navigation).

## Schritt 1: Einrichten der Attributeigenschaften

1. Auf der _Admin_ Seitenleiste, zu gehen **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Durchsuchen Sie die Liste oder verwenden Sie die gefilterte Suche, um ein Attribut in ihr zu finden und im Bearbeitungsmodus zu öffnen.

   ![Suchbegriffe pro Spalte eingeben, um die gefilterte Suche zu verwenden](./assets/attribute-search.png){width="700" zoomable="yes"}

1. Wählen Sie im linken Bedienfeld **[!UICONTROL Storefront Properties]** und setzen **[!UICONTROL Use In Layered Navigation]** eine der folgenden Möglichkeiten:

   - `Filterable (with results)` - Die mehrschichtige Navigation umfasst nur die Filter, für die passende Produkte gefunden werden können. Jeder Attributwert, der bereits für alle in der Liste aufgeführten Produkte gilt, sollte weiterhin als verfügbarer Filter angezeigt werden. Attributwerte mit einer Anzahl von null (0) Produktübereinstimmungen werden in der Liste der verfügbaren Filter weggelassen. Die gefilterte Liste enthält nur die Produkte, die dem Filter entsprechen. Die Produktliste wird nur aktualisiert, wenn die ausgewählten Filter das Gezeigte ändern.

   - `Filterable (no results)` - Die mehrschichtige Navigation umfasst Filter für alle verfügbaren Attributwerte und ihre Produktanzahl, einschließlich Produkten mit null (0) Produktübereinstimmungen. Wenn der Attributwert ein Farbfeld ist, wird der Wert als Filter angezeigt, aber durchgestrichen. Die Filterung auf Preisebene wird von dieser Option nicht unterstützt und hat keinen Einfluss auf Preisfilter.

1. set **[!UICONTROL Use In Search Results Layered Navigation]** bis `Yes`.

   ![Storefront-Eigenschaften](./assets/attribute-storefront-properties.png){width="600" zoomable="yes"}

1. Wiederholen Sie diese Schritte für jedes Attribut, das Sie in die mehrschichtige Navigation aufnehmen möchten.

>[!NOTE]
>
>Wenn die _[!UICONTROL Use in Search]_Einstellung ist festgelegt auf `No`, die_[!UICONTROL Use in Search Results Layered Navigation]_ -Einstellung wird nicht angezeigt und das Produktattribut wird bei der Suche mit keinem verwendet [!UICONTROL Use in Layered Navigation] Einstellwert.

>[!NOTE]
>
>Die [!UICONTROL Position] Das Feld ist standardmäßig abgeblendet, sodass Sie das Attribut speichern müssen, bevor Sie diese Einstellung ändern können.

## Schritt 2: Kategorie als Anker festlegen

1. Auf der _Admin_ Seitenleiste, zu gehen **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Wählen Sie in der Kategoriestruktur die Kategorie aus, für die Sie die mehrschichtige Navigation verwenden möchten.

1. Expand ![Erweiterungsauswahl](../assets/icon-display-expand.png) Die **[!UICONTROL Display Settings]** Abschnitt und Set **[!UICONTROL Anchor]** bis `Yes`.

   ![Einstellungen für Kategorieanzeige](./assets/category-layered-navigation-anchor.png){width="600" zoomable="yes"}

1. Klick **[!UICONTROL Save]**.

## Schritt 3: Testen der Ergebnisse

Um die Einstellung zu testen, besuchen Sie Ihren Store und navigieren Sie über das Hauptmenü zur Kategorie . Die Auswahl filterbarer Attribute wird im mehrschichtigen Navigationsbereich der Kategorieseite angezeigt.

Durchsuchen, Filtern und Überprüfen der angezeigten Produkte.

## Entfernen von filterbaren Attributwerten aus der mehrschichtigen Navigation

Die mehrschichtige Navigation enthält Filter für alle verfügbaren Attributwerte und ihre Produktanzahl, einschließlich Produkten mit null (0) Produktübereinstimmungen (wie in der folgenden Abbildung dargestellt).

![Keine Filter angezeigt](./assets/filterable-attributes-on-plp.png){width="700" zoomable="yes"}

Dies kann es Kunden erschweren, ein bevorzugtes Produkt auszuwählen, und es ist nicht erforderlich, Attributwerte &#x200B;&#x200B;mit 0 Produkten im Frontend) anzuzeigen.

Sie können die folgenden Schritte verwenden, um filterbare Attributwerte mit 0 Produkten aus der mehrschichtigen Navigation zu entfernen:

1. Auf der _Admin_ Seitenleiste, zu gehen **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Durchsuchen Sie die Liste oder verwenden Sie die gefilterte Suche, um ein Attribut in ihr zu finden und im Bearbeitungsmodus zu öffnen.

1. Unter _[!UICONTROL Attribute Information]_, klicken Sie auf **[!UICONTROL Storefront Properties]**.

1. für **[!UICONTROL Layered Navigation]**, wählen Sie `Filterable (with results)`.

   ![Abschnitt „Attributinformationen“](./assets/storefront-properties-tab.png){width="600" zoomable="yes"}

1. Klick **[!UICONTROL Save Attribute]**.

## Preisnavigation

>[!NOTE]
>
>Die in diesem Thema beschriebene Preisnavigationskonfiguration unterscheidet sich für [Live Search](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html).

Die Preisnavigation kann verwendet werden, um Produkte nach Preisbereich in der mehrschichtigen Navigation zu verteilen. Sie können jeden Bereich auch in Intervallen aufteilen. Es gibt einige Möglichkeiten, die Preisnavigation zu berechnen:

- Automatisch (Preisbereiche angleichen)
- Automatisch (gleicht die Anzahl der Produkte an)
- Manuell

Bei den ersten beiden Methoden werden die Navigationsschritte automatisch berechnet. Mit der manuellen Methode können Sie eine Teilungsgrenze für Preisintervalle festlegen. Das folgende Beispiel zeigt den Unterschied zwischen den Preisnavigationsschritten 10 und 100.

Die iterative Aufteilung bietet die beste Verteilung der Produkte auf die Preisklassen. Bei der iterativen Aufteilung kann der Kunde nach der Auswahl des Bereichs von 0,00 bis 99 US-Dollar mehrere Preisunterbereiche durchgehen. Die Aufteilung der Preisspanne stoppt, wenn die Anzahl der Produkte den Schwellenwert erreicht, der durch die Intervalldivisionsgrenze festgelegt wurde.

## Beispiel: Preisnavigationsschritte

| Preisschritt um 10 | Preisschritt um 100 |
|----------|--------|
| 20,00 - 29,99 $ (1) | 0,00 - 99,99 $ (4) |
| 30,00 - 39,99 $ (2) | 100 - 199,99 $ (5) |
| 70,00 - 79,99 $ (1) | 400,00 $ - 499,99 $ (2) |
| 100,00 $ - 109,99 $ (1) | 700,00 $ und mehr (1) |
| 120,00 $ - 129,99 $ (2) |   |
| 150,00 $ - 159,99 $ (1) |   |
| 180,00 $ - 189,99 $ (1) |   |
| 420,00 $ - 429,99 $ (1) |   |
| 440,00 $ - 449,99 $ (1) |   |
| 710,00 $ und mehr (1) |   |

{style="table-layout:auto"}

## Konfigurieren der Preisnavigation

>[!IMPORTANT]
>
>So zeigen Sie Produkte und ihre Preise korrekt an _Preisfilter_ Stellen Sie in der mehrschichtigen Navigation sicher, dass die Einstellungen für den Preis in der [Konfiguration der Mehrwertsteuer](../configuration-reference/sales/tax.md) den gleichen Wert haben (`Excluding Tax` **oder** `Including Tax`). Für die _[!UICONTROL Calculation Settings]_, überprüfen Sie die **[!UICONTROL Catalog Prices]**Wert. Und für_[!UICONTROL Price Display Settings]_, überprüfen Sie die **[!UICONTROL Display Product Prices in Catalog]** Wert. Wenn diese unterschiedliche Werte haben, können Preisfilter in der mehrschichtigen Navigation Produkte möglicherweise nicht ordnungsgemäß nach Preis filtern und sortieren.

1. Auf der _Admin_ Seitenleiste, zu gehen **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich . **[!UICONTROL Catalog]** und wählen **[!UICONTROL Catalog]** Darunter.

1. Expand ![Erweiterungsauswahl](../assets/icon-display-expand.png) Die _mehrschichtige Navigation_ -Abschnitt.

   Standardmäßig **[!UICONTROL Display Product Count]** ist festgelegt auf `Yes`. Deaktivieren Sie bei Bedarf die Option **[!UICONTROL Use system value]** Kontrollkästchen zum Ändern dieser Einstellung.

   ![mehrschichtige Navigation](../configuration-reference/catalog/assets/layered-navigation.png){width="600" zoomable="yes"}

   Eine detaillierte Liste dieser Konfigurationsoptionen finden Sie unter [mehrschichtige Navigation](../configuration-reference/catalog/catalog.md#layered-navigation) in der _Konfigurationsreferenz_.

1. set **[!UICONTROL Price Navigation Steps Calculation]** für eine der Methoden in den folgenden Abschnitten.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

### Methode 1: Automatisch (Preisspannen angleichen)

Verlassen **[!UICONTROL Price Navigation Steps Calculation]** auf festlegen `Automatic (Equalize Price Ranges)` (Standard). Diese Einstellung verwendet den Standardalgorithmus für die Preisnavigation.

### Methode 2: Automatisch (Produktzahlen angleichen)

>[!TIP]
>
>Deaktivieren Sie bei Bedarf zunächst die Option **[!UICONTROL Use system value]** Kontrollkästchen zum Ändern dieser Einstellungen.

1. set **[!UICONTROL Price Navigation Steps Calculation]** bis `Automatic (equalize product counts)`.

1. Um einen einzelnen Preis anzuzeigen, wenn mehrere Produkte denselben Preis haben, legen Sie Folgendes fest **[!UICONTROL Display Price Interval as One Price]** bis `Yes`.

1. für **[!UICONTROL Interval Division Limit]** Geben Sie den Schwellenwert für die Anzahl der Produkte innerhalb einer Preisspanne ein.

   Der Bereich kann über dieses Limit hinaus nicht weiter aufgeteilt werden. Der Standardwert lautet `9`.

   ![Automatisch (Produktzahlen angleichen)](../configuration-reference/catalog/assets/layered-navigation-equalize-product-counts.png){width="600" zoomable="yes"}

### Methode 3: Manuell

>[!NOTE]
>
>Deaktivieren Sie bei Bedarf zunächst die Option **[!UICONTROL Use system value]** Kontrollkästchen zum Ändern dieser Einstellungen.

1. set **[!UICONTROL Price Navigation Steps Calculation]** bis `Manual`.

1. Geben Sie einen Wert ein, der die **[!UICONTROL Default Price Navigation Step]**.

1. Geben Sie die **[!UICONTROL Maximum Number of Price Intervals]** zulässig, bis zu `100`.

   ![Manuell](../configuration-reference/catalog/assets/layered-navigation-manual.png){width="600" zoomable="yes"}

## Konfigurieren der mehrschichtigen Navigation

>[!NOTE]
>
>Die auf dieser Seite beschriebene Standardkonfiguration unterscheidet sich für [Live Search](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html).

Die Konfiguration der mehrschichtigen Navigation bestimmt, ob eine Produktanzahl nach jedem Attribut in Klammern angezeigt wird, und die Größe der Schrittberechnung, die in der Preisnavigation verwendet wird.

1. Auf der _Admin_ Seitenleiste, zu gehen **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bedienfeld die _[!UICONTROL Catalog]_auswählen **[!UICONTROL Catalog]**Darunter.

1. Erweitern Sie die _[!UICONTROL Layered Navigation]_-Abschnitt.

   >[!NOTE]
   >
   >Deaktivieren Sie bei Bedarf zunächst die Option **[!UICONTROL Use system value]** Kontrollkästchen zum Ändern dieser Einstellungen.

1. Um die Anzahl der für jedes Attribut gefundenen Produkte anzuzeigen, legen Sie Folgendes fest **[!UICONTROL Display Product Count]** bis `Yes`.

1. set **[!UICONTROL Price Navigation Step Calculation]** bis `Automatic (equalize price ranges)`.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.
