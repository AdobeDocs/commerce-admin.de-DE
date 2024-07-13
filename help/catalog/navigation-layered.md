---
title: Ebenennavigation
description: Erfahren Sie, wie die Navigation mit Ebenen es den Käufern erleichtert, Produkte basierend auf Kategorie, Preisbereich oder anderen verfügbaren Attributen zu finden.
exl-id: 5f17528a-3593-449c-a044-98736a4ae913
feature: Catalog Management, Categories, Site Navigation
source-git-commit: 99049260b4ff490845affd1c98fa4d2536edebd7
workflow-type: tm+mt
source-wordcount: '1303'
ht-degree: 0%

---

# Ebenennavigation

>[!NOTE]
>
>Die in diesem Abschnitt beschriebene Standardnavigation mit Ebenen unterscheidet sich von der in der Live-Suche gefilterten Navigation mit [Facetten](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/live-search-admin/facets/facets.html).

Durch die mehrschichtige Navigation können Sie Produkte auf der Grundlage von Kategorie, Preisbereich oder anderen verfügbaren Attributen leicht finden. Die Navigation mit Ebenen wird in der Regel in der linken Spalte der Suchergebnisse und Kategorieseiten und manchmal auf der Startseite angezeigt. Die Standardnavigation enthält eine Liste der Kategorien und Preisbereiche von _Shop By_. Sie können die Anzeige der Navigation mit Ebenen konfigurieren, einschließlich Produktanzahl und Preisbereich.

![Navigation mit Ebenen nach Kategorie und Preis](./assets/navigation-layered-basic.png){width="700" zoomable="yes"}

## Filterbare Attribute

>[!NOTE]
>
>Die in diesem Thema beschriebenen filterbaren Attributanforderungen unterscheiden sich für [Live Search](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html). Weitere Informationen finden Sie unter [Facets](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/live-search-admin/facets/facets.html).

Die Navigation mit Ebenen kann verwendet werden, um nach Produkten nach Kategorie oder Attribut zu suchen. Wenn beispielsweise ein Käufer in der oberen Navigation die Kategorie Männer/Shorts auswählt, umfassen die ersten Ergebnisse alle Produkte in der Kategorie. Die Liste kann weiter gefiltert werden, indem ein bestimmter Stil, Klima, Farbe, Material, Muster oder Preis oder eine Kombination von Werten ausgewählt wird. Filterbare Attribute werden in einem erweiterten Abschnitt angezeigt, in dem jeder Attributwert aufgeführt wird. Als Option kann die Liste der Produkte mit übereinstimmenden Ergebnissen so konfiguriert werden, dass sie Produkte mit oder ohne Übereinstimmung enthält.

Die Attributeigenschaften bestimmen in Verbindung mit dem Produktangabetyp, welche Attribute für die mehrteilige Navigation verwendet werden können. Die Navigation mit Ebenen ist nur für [_Anker_](categories-display-settings.md) -Kategorien verfügbar, kann aber auch zu Suchergebnisseiten hinzugefügt werden. Die Eigenschaft **Catalog Input Type for Store Owner** jedes Attributs muss auf `Yes/No`, `Dropdown`, `Multiple Select` oder `Price` eingestellt sein. Damit die Attribute gefiltert werden können, muss die Eigenschaft **Use in Layered Navigation** jeder Eigenschaft auf `Filterable (with results)` oder `Filterable (no results)` gesetzt werden.

_Beispiel: Filterbare Attribute mit Ergebnissen_

![Filterbare Attribute in mehrschichtiger Navigation](./assets/storefront-layered-navigation-filtered.png){width="700" zoomable="yes"}

_Beispiel: Gefilterbare Musterwerte, die ohne Ergebnis angezeigt werden_

![Filterbarer Farbfeldwert ohne Ergebnisse](./assets/storefront-product-attribute-filter-no-results.png){width="700" zoomable="yes"}

Die folgenden Anweisungen zeigen, wie Sie eine einfache Navigation mit mehreren Ebenen mit filterbaren Attributen einrichten. Informationen zur erweiterten Navigation mit Ebenen mit Preisschritten finden Sie unter [Preisnavigation](navigation-layered.md#configure-price-navigation).

## Schritt 1: Einrichten der Attributeigenschaften

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Suchen Sie nach einem Attribut in der Liste oder öffnen Sie es mithilfe der gefilterten Suche im Bearbeitungsmodus.

   ![Suchbegriffe pro Spalte eingeben, um gefilterte Suche zu verwenden](./assets/attribute-search.png){width="700" zoomable="yes"}

1. Wählen Sie im linken Bereich **[!UICONTROL Storefront Properties]** und legen Sie **[!UICONTROL Use In Layered Navigation]** auf einen der folgenden Werte fest:

   - `Filterable (with results)` - Die Navigation mit Ebenen umfasst nur die Filter, für die passende Produkte gefunden werden können. Jeder Attributwert, der bereits für alle in der Liste angezeigten Produkte gilt, sollte weiterhin als verfügbarer Filter angezeigt werden. Attributwerte mit einer Anzahl von null (0) Produktübereinstimmungen werden in der Liste der verfügbaren Filter weggelassen. Die gefilterte Liste enthält nur die Produkte, die mit dem Filter übereinstimmen. Die Produktliste wird nur aktualisiert, wenn die ausgewählten Filter die angezeigten Elemente ändern.

   - `Filterable (no results)` - Die Navigation mit Ebenen umfasst Filter für alle verfügbaren Attributwerte und deren Produktzahlen, einschließlich Produkten mit null (0) Produktübereinstimmungen. Wenn es sich bei dem Attributwert um ein Muster handelt, wird der Wert als Filter angezeigt, jedoch ausgekreuzt. Preisorientierte Filter werden von dieser Option nicht unterstützt und wirken sich nicht auf Preisfilter aus.

1. Setzen Sie **[!UICONTROL Use In Search Results Layered Navigation]** auf `Yes`.

   ![Storefront-Eigenschaften](./assets/attribute-storefront-properties.png){width="600" zoomable="yes"}

1. Wiederholen Sie diese Schritte für jedes Attribut, das Sie in die Navigation mit Ebenen aufnehmen möchten.

>[!NOTE]
>
>Wenn die Einstellung _[!UICONTROL Use in Search]_auf `No` gesetzt ist, wird die Einstellung_[!UICONTROL Use in Search Results Layered Navigation]_ nicht angezeigt und das Produktattribut wird bei der Suche mit einem [!UICONTROL Use in Layered Navigation] -Einstellungswert nicht verwendet.

>[!NOTE]
>
>Das Feld [!UICONTROL Position] ist standardmäßig abgeblendet. Daher müssen Sie das Attribut speichern, bevor Sie diese Einstellung ändern können.

## Schritt 2: Kategorisierung als Anker festlegen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Wählen Sie in der Kategorienstruktur die Kategorie aus, in der Sie die Navigation mit Ebenen verwenden möchten.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Display Settings]** und legen Sie **[!UICONTROL Anchor]** auf `Yes` fest.

   ![Anzeigeeinstellungen für Kategorien](./assets/category-layered-navigation-anchor.png){width="600" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Save]**.

## Schritt 3: Testen der Ergebnisse

Um die Einstellung zu testen, besuchen Sie Ihren Store und navigieren Sie im Hauptmenü zur Kategorie . Die Auswahl der filterbaren Attribute wird in der mehrstufigen Navigation der Kategorieseite angezeigt.

Suchen, filtern und überprüfen Sie die angezeigten Produkte.

## Entfernen filterbarer Attributwerte aus der Navigationsschicht

Die Navigation mit Ebenen umfasst Filter für alle verfügbaren Attributwerte und deren Produktzahlen, einschließlich Produkten mit null (0) Produktübereinstimmungen (wie in der folgenden Abbildung dargestellt).

![Null-Filter, die](./assets/filterable-attributes-on-plp.png){width="700" zoomable="yes"} anzeigen

Dadurch kann es für Kunden schwierig werden, ein bevorzugtes Produkt auszuwählen, und es ist nicht erforderlich, Attributwerte &#x200B; mit 0 Produkten im Frontend anzuzeigen.

Sie können die folgenden Schritte ausführen, um filterbare Attributwerte mit 0 Produkten aus der Navigationsschicht zu entfernen:

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Suchen Sie nach einem Attribut in der Liste oder öffnen Sie es mithilfe der gefilterten Suche im Bearbeitungsmodus.

1. Klicken Sie unter _[!UICONTROL Attribute Information]_auf **[!UICONTROL Storefront Properties]**.

1. Wählen Sie für **[!UICONTROL Layered Navigation]** `Filterable (with results)` aus.

   ![Abschnitt &quot;Attributinformationen&quot;](./assets/storefront-properties-tab.png){width="600" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Save Attribute]**.

## Preisnavigation

>[!NOTE]
>
>Die in diesem Thema beschriebene Preisnavigationskonfiguration unterscheidet sich für [Live Search](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html).

Die Preisnavigation kann verwendet werden, um Produkte nach Preisbereich in der Navigation mit Ebenen zu verteilen. Sie können jeden Bereich auch in Intervallen aufteilen. Es gibt verschiedene Möglichkeiten, die Preisnavigation zu berechnen:

- Automatisch (Preisbereiche ausgleichen)
- Automatisch (Produktanzahl ausgleichen)
- Manuell

Bei den ersten beiden Methoden werden die Navigationsschritte automatisch berechnet. Die manuelle Methode ermöglicht die Angabe einer Trennungsbegrenzung für Preisintervalle. Das folgende Beispiel zeigt den Unterschied zwischen den Preisnavigationsschritten 10 und 100.

Iterative Aufteilung bietet die beste Verteilung der Produkte auf die Preisbereiche. Durch iterative Aufteilung kann der Kunde nach Auswahl des Bereichs zwischen 0,00 und 99 USD einen Drilldown durch mehrere Unterbereiche von Preisen durchführen. Die Aufteilung der Preisbereiche wird gestoppt, wenn die Anzahl der Produkte den durch die Begrenzung der Intervallabteilung festgelegten Schwellenwert erreicht.

## Beispiel: Schritte zur Preisnavigation

| Preis Schritt um 10 | Preis Schritt bis 100 |
|----------|--------|
| 20,00 $ - 29,99 $ (1) | 0,00 $ - 99,99 $ (4) |
| 30,00 $ - 39,99 $ (2) | 100 $ - 199,99 $ (5) |
| 70,00 $ - 79,99 $ (1) | 400,00 $ - 499,99 $ (2) |
| 100,00 $ - 109,99 $ (1) | 700,00 $ und höher (1) |
| 120,00 $ - 129,99 $ (2) |   |
| 150,00 $ - 159,99 $ (1) |   |
| 180,00 $ - 189,99 $ (1) |   |
| 420,00 $ - 429,99 $ (1) |   |
| 440,00 $ - 449,99 $ (1) |   |
| $ 710.00 und höher (1) |   |

{style="table-layout:auto"}

## Preisnavigation konfigurieren

>[!IMPORTANT]
>
>Um Produkte und deren Preise gemäß _Preisfiltern_ in der geschichteten Navigation korrekt anzuzeigen, stellen Sie sicher, dass die Einstellungen für die Preisanzeige in der [Konfiguration der Umsatzsteuer](../configuration-reference/sales/tax.md) denselben Wert haben (`Excluding Tax` **oder** `Including Tax`). Überprüfen Sie für &quot;_[!UICONTROL Calculation Settings]_&quot;den Wert &quot;**[!UICONTROL Catalog Prices]**&quot;. Überprüfen Sie für_[!UICONTROL Price Display Settings]_ den Wert **[!UICONTROL Display Product Prices in Catalog]** . Wenn diese unterschiedliche Werte aufweisen, können Preisfilter in der mehrschichtigen Navigation Produkte möglicherweise nicht ordnungsgemäß nach Preisen filtern und sortieren.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bedienfeld den Wert **[!UICONTROL Catalog]** und wählen Sie unter &quot;**[!UICONTROL Catalog]**&quot;.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt _Navigation mit Ebenen_ .

   Standardmäßig ist **[!UICONTROL Display Product Count]** auf `Yes` gesetzt. Deaktivieren Sie bei Bedarf das Kontrollkästchen **[!UICONTROL Use system value]** , um diese Einstellung zu ändern.

   ![Navigation mit Ebenen](../configuration-reference/catalog/assets/layered-navigation.png){width="600" zoomable="yes"}

   Eine detaillierte Liste dieser Konfigurationsoptionen finden Sie unter [Navigation mit Ebenen](../configuration-reference/catalog/catalog.md#layered-navigation) in der _Konfigurationsreferenz_.

1. Legen Sie für eine der Methoden in den folgenden Abschnitten den Wert &quot;**[!UICONTROL Price Navigation Steps Calculation]**&quot;fest.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

### Methode 1: Automatisch (Preisspannen angleichen)

Belassen Sie **[!UICONTROL Price Navigation Steps Calculation]** auf `Automatic (Equalize Price Ranges)` (Standard). Diese Einstellung verwendet den Standardalgorithmus für die Preisnavigation.

### Methode 2: Automatisch (Produktzahlen angleichen)

>[!TIP]
>
>Heben Sie bei Bedarf zunächst das Kontrollkästchen **[!UICONTROL Use system value]** auf, um diese Einstellungen zu ändern.

1. Setzen Sie **[!UICONTROL Price Navigation Steps Calculation]** auf `Automatic (equalize product counts)`.

1. Um einen einzelnen Preis anzuzeigen, wenn mehrere Produkte mit demselben Preis vorhanden sind, setzen Sie **[!UICONTROL Display Price Interval as One Price]** auf `Yes`.

1. Geben Sie für &quot;**[!UICONTROL Interval Division Limit]**&quot;den Schwellenwert für die Anzahl der Produkte innerhalb eines Preisbereichs ein.

   Der Bereich kann über diese Grenze hinaus nicht weiter aufgeteilt werden. Der Standardwert ist `9`.

   ![Automatisch (gleich Produktzahlen)](../configuration-reference/catalog/assets/layered-navigation-equalize-product-counts.png){width="600" zoomable="yes"}

### Methode 3: Manuell

>[!NOTE]
>
>Heben Sie bei Bedarf zunächst das Kontrollkästchen **[!UICONTROL Use system value]** auf, um diese Einstellungen zu ändern.

1. Setzen Sie **[!UICONTROL Price Navigation Steps Calculation]** auf `Manual`.

1. Geben Sie einen Wert ein, der den **[!UICONTROL Default Price Navigation Step]** bestimmt.

1. Geben Sie die zulässige **[!UICONTROL Maximum Number of Price Intervals]** bis `100` ein.

   ![Manuell](../configuration-reference/catalog/assets/layered-navigation-manual.png){width="600" zoomable="yes"}

## Konfigurieren der Navigation mit Ebenen

>[!NOTE]
>
>Die auf dieser Seite beschriebene Standardkonfiguration unterscheidet sich bei der [Live-Suche](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html).

Die Navigationskonfiguration mit Ebenen bestimmt, ob nach jedem Attribut eine Produktanzahl in Klammern angezeigt wird, sowie die Größe der Schrittberechnung, die in der Preisnavigation verwendet wird.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Abschnitt _[!UICONTROL Catalog]_und wählen Sie unter &quot;**[!UICONTROL Catalog]**&quot;.

1. Erweitern Sie den Abschnitt _[!UICONTROL Layered Navigation]_.

   >[!NOTE]
   >
   >Heben Sie bei Bedarf zunächst das Kontrollkästchen **[!UICONTROL Use system value]** auf, um diese Einstellungen zu ändern.

1. Um die Anzahl der für jedes Attribut gefundenen Produkte anzuzeigen, setzen Sie **[!UICONTROL Display Product Count]** auf `Yes`.

1. Setzen Sie **[!UICONTROL Price Navigation Step Calculation]** auf `Automatic (equalize price ranges)`.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.
