---
title: Suchbegriffe verwalten
description: Erfahren Sie, wie Sie die Suchbegriffe für Ihren Store verwalten, um Kunden mit falsch geschriebenen oder alternativen Begriffen umzuleiten.
exl-id: e21ece58-2bc2-49ef-96d3-3be930e09f94
feature: Catalog Management, Search
source-git-commit: 6126943f20f33d52085018ca634159918833efc9
workflow-type: tm+mt
source-wordcount: '1158'
ht-degree: 0%

---

# Suchbegriffe verwalten

Die [Landingpage](../content-design/pages.md) für einen Suchbegriff eine Inhaltsseite, eine Kategorieseite, eine Produktdetailseite oder sogar eine Seite auf einer anderen Site sein.

Verwenden Sie Suchbegriffe, um gängige Rechtschreibfehler zu erfassen und sie auf die entsprechende Seite umzuleiten. Wenn Sie beispielsweise Möbel aus Schmiedeeisen verkaufen, wissen Sie, dass viele Menschen den Begriff falsch schreiben als _eim Eisen_ oder sogar _Rot_. Sie können jedes falsch geschriebene Wort als Suchbegriff eingeben und zu Synonymen für _Schmiedeeisen_. Obwohl das Wort falsch geschrieben ist, wird die Suche auf die Seite für Schmiedeeisen geleitet.

Sie können auch erfahren, wonach Ihre Kunden suchen, indem Sie die Suchbegriffe untersuchen, mit denen sie Produkte in Ihrem Geschäft finden. Wenn ausreichend Personen nach einem Produkt suchen, das nicht in Ihrem Katalog enthalten ist, könnte dies auf eine Verkaufschance hindeuten. In der Zwischenzeit können Sie sie zu einem anderen Produkt in Ihrem Katalog umleiten, anstatt sie leer zu lassen.

## Suchbegriffe hinzufügen

Wenn Sie neue Wörter lernen, die Benutzer für die Suche in Ihrem Geschäft verwenden, können Sie sie zu Ihrer Suchbegriffliste hinzufügen, um Personen zu den am ehesten passenden Produkten in Ihrem Katalog zu leiten.

![Suchbegriffsraster](./assets/search-terms.png){width="700" zoomable="yes"}

| Spalte | Beschreibung |
|--- |--- |
| [!UICONTROL Search Query] | Die Abfrage, die zur Durchführung der Suche verwendet wird. |
| [!UICONTROL Store] | Der Store, auf den die Suchabfrage angewendet wurde. |
| [!UICONTROL Results] | Anzahl der durch Abfrage gefundenen Ergebnisse. |
| [!UICONTROL Uses] | Anzahl der Verwendungen. |
| [!UICONTROL Redirect URL] | URL der Zielseite, auf die der Benutzer nach Durchführung der Suche umgeleitet wurde. |
| [!UICONTROL Suggested Terms] | Bestimmt, ob das Abfrageergebnis die vorgeschlagenen Begriffe anzeigt. |
| [!UICONTROL Actions] | Öffnet das Produkt im Bearbeitungsmodus. |

{style="table-layout:auto"}

>[!NOTE]
>
>Die Anzahl der Ergebnisse wird jedes Mal aktualisiert, wenn ein Käufer mithilfe dieser Suchabfrage eine Suche durchführt. Sie wird nicht aktualisiert, wenn eines der Produkte geändert oder entfernt wird.

### Suchbegriff hinzufügen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Search Terms]**.

1. Klicken **[!UICONTROL Add New Search Term]**.

   ![Allgemeine Informationen zu Suchbegriffen](./assets/search-terms-information.png){width="600" zoomable="yes"}

1. under _[!UICONTROL General Information]_im **[!UICONTROL Search Query]**eingeben, das Wort oder die Wortgruppe eingeben, die Sie als neuen Suchbegriff hinzufügen möchten.

1. Wenn Ihr Store in mehreren Sprachen verfügbar ist, wählen Sie die entsprechende **[!UICONTROL Store]** anzeigen.

1. Um die Suchergebnisse auf eine andere Seite in Ihrem Store oder auf eine andere Website umzuleiten, geben Sie die vollständige URL der Zielseite in das **[!UICONTROL Redirect URL]** -Feld.

1. Wenn dieser Begriff immer dann als Vorschlag verwendet werden soll, wenn eine Suche keine Ergebnisse zurückgibt, legen Sie **[!UICONTROL Display in Suggested Terms]** nach `Yes`.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Search]**.

## Suchbegriffe bearbeiten

1. Im _[!UICONTROL Search Terms]_auf die Zeile eines Datensatzes klicken, um den Suchbegriff im Bearbeitungsmodus zu öffnen.

1. Nehmen Sie die erforderlichen Änderungen vor.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Search]**.

## Suchbegriff löschen

Es gibt zwei Methoden zum Löschen eines Suchbegriffs aus dem Raster und auf der Bearbeitungsseite.

**Methode 1:** Im _[!UICONTROL Search Terms]_grid

1. Aktivieren Sie in der Liste das Kontrollkästchen des zu löschenden Begriffs.

1. Legen Sie in der linken oberen Ecke der Liste **[!UICONTROL Actions]** nach `Delete`.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Submit]**.

**Methode 2:** Im _[!UICONTROL Edit a Search Term]_page

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Search Terms]**.

1. Suchen Sie den zu löschenden Suchbegriff und öffnen Sie ihn im Bearbeitungsmodus.

1. Klicken **[!UICONTROL Delete Search]**.

1. Klicken Sie zur Bestätigung der Aktion auf **[!UICONTROL OK]**.

## Beliebte Suchbegriffe

Die _Suchbegriffe_ -Link in der Fußzeile Ihres Stores zeigt die Suchbegriffe an, die von Besuchern Ihres Stores verwendet werden, nach Beliebtheit geordnet. Suchbegriffe werden in einer _Tag-Cloud_ Format, wobei die Textgröße die Beliebtheit des Begriffs anzeigt.

Standardmäßig sind populäre Suchbegriffe als Suchmaschinen-Optimierungs-Tool aktiviert, doch es besteht keine direkte Verbindung zum Katalogsuchprozess. Da die Seite &quot;Suchbegriffe&quot;von Suchmaschinen indexiert wird, können alle Begriffe auf der Seite dazu beitragen, das Ranking Ihrer Suchmaschine und die Sichtbarkeit Ihres Geschäfts zu verbessern. Die URL der Seite &quot;Beliebte Suchbegriffe&quot;lautet: `mystore.com/search/term/popular/`

![Beispiel-Storefront - beliebte Suchbegriffe](./assets/store-front-search-terms-yoga-pants.png){width="600" zoomable="yes"}

**_So konfigurieren Sie beliebte Suchbegriffe:_**

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Catalog]** und wählen **[!UICONTROL Catalog]** darunter.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Search Engine Optimization]** Abschnitt.

   ![Katalogkonfiguration - Suchmaschinenoptimierung](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

   Eine detaillierte Liste dieser Optionen finden Sie unter [Suchmaschinenoptimierung](../configuration-reference/catalog/catalog.md#search-engine-optimization) im _Konfigurationsreferenz_.

1. Satz **[!UICONTROL Popular Search Terms]** nach Bedarf.

   Falls erforderlich, löschen Sie die **[!UICONTROL Use system value]** zum Ändern dieser Einstellung.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

>[!NOTE]
>
>Sie können die Zwischenspeicherung beliebter [Katalogsuche](search-configuration.md).

## Synonyme suchen

Eine Möglichkeit, die Effektivität von [Katalogsuche](search-configuration.md) ist es, verschiedene Begriffe einzubeziehen, die Personen verwenden können, um dasselbe Element zu beschreiben. Sie wollen keinen Verkauf verlieren, nur weil jemand nach einer _Sofa_ und Ihr Produkt als _Couch_. Sie können eine breitere Palette von Suchbegriffen erfassen, indem Sie _Sofa_, _davenport_, und _loveseat_ als Synonyme für _Couch_ und leiten sie zur selben Landingpage weiter.

Adobe Commerce unterstützt zwei verschiedene Synonym-Verwaltungslösungen:

- Live Search [Synonyme](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/live-search-admin/synonyms/synonyms.html) ist für Adobe Commerce-Installationen mit installierter Live Search-Funktion verfügbar.
- Die standardmäßige Funktion &quot;Synonyme suchen&quot;(auf dieser Seite beschrieben) ist für alle Adobe Commerce-Installationen standardmäßig verfügbar.

>[!NOTE]
>
>Die standardmäßige Funktion &quot;Synonyme suchen&quot;unterstützt standardmäßig `name` und `sku` Produktattribute **_only_**.

![Beispiel-Storefront - Suchergebnisse mit Synonymen](./assets/storefront-search-results-synonyms.png){width="700" zoomable="yes"}

### Synonymisierungsgruppe erstellen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Search Synonyms]**.

   Die _[!UICONTROL Search Synonyms]_wird angezeigt. Wenn Sie zum ersten Mal Suchsynonyme verwenden, ist das Raster leer.

   ![Synonymisierungs-Raster suchen](./assets/search-synonyms-grid-empty.png){width="700" zoomable="yes"}

1. Klicken **[!UICONTROL New Synonym Group]**.

   ![Neue Gruppe von Suchsynonymen](./assets/search-synonym-group-new.png){width="700" zoomable="yes"}

1. Satz **[!UICONTROL Scope]** in die Store-Ansichten, in denen die Synonyme gelten.

1. Geben Sie jedes Synonym in der Gruppe durch Kommas getrennt ein. Wählen Sie Wörter aus, die Personen als Suchkriterien verwenden können. Beispiel:

   - `sweatshirt, sweat shirt, hoodie, fleece`
   - `cell phone, mobile phone, smart phone`
   - `couch, sofa, davenport`
   - `wrought iron, rot iron, rod iron`

1. Um diese Synonyme mit anderen Synonymen mit demselben Bereich zu einer Gruppe zusammenzuführen, wählen Sie die **[!UICONTROL Merge existing synonyms]** aktivieren.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Synonym Group]**.

### Eine Synonymisierungsgruppe bearbeiten

1. Im _[!UICONTROL Search Synonyms]_auf die Zeile eines Datensatzes klicken, um die Synonym-Gruppe im Bearbeitungsmodus zu öffnen.

1. Nehmen Sie die erforderlichen Änderungen vor.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Synonym Group]**.

### Eine Synonymisierungsgruppe löschen

Es gibt zwei Methoden zum Löschen einer Synonym-Gruppe - aus dem Raster und auf der Bearbeitungsseite.

**Methode 1:** Im Raster &quot;Suchsynonyme&quot;

1. Im _[!UICONTROL Search Synonyms]_-Raster das Kontrollkästchen der zu löschenden Gruppe.

1. Legen Sie in der linken oberen Ecke der Liste **[!UICONTROL Actions]** nach `Delete`.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Submit]**.

**Methode 2:** Auf der Seite &quot;Synonyme Gruppe bearbeiten&quot;

1. Klicken Sie im Raster &quot;Synonyme suchen&quot;auf die Zeile eines Datensatzes, um die Synonym-Gruppe im Bearbeitungsmodus zu öffnen.

1. Klicken **[!UICONTROL Delete Synonym Group]**.

1. Bestätigen Sie bei entsprechender Aufforderung das Entfernen der Gruppe.

## Bericht &quot;Suchbegriffe&quot;

Der Bericht zu Suchbegriffen zeigt die Anzahl der Ergebnisse für jeden Begriff und die Anzahl der verwendeten Begriffe (Treffer) an. Die Berichtsdaten können nach Begriff, Speicher, Ergebnissen und Treffern gefiltert und zur weiteren Analyse exportiert werden.

### Bericht anzeigen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Reports]** > _[!UICONTROL Marketing]_>**[!UICONTROL Search Terms]**.

1. Verwenden Sie die Steuerelemente, um den Bericht nach Bedarf zu filtern.

   ![Suchbegriffbericht](./assets/search-terms-report.png){width="700" zoomable="yes"}

## Bericht exportieren

1. Für **[!UICONTROL Export to]**, wählen Sie ein Exportformat aus:

   - `CSV` - Eine kommagetrennte Wertdatei mit Textdaten
   - `Excel XML` - Ein XML-basiertes Tabellendatenformat

1. Klicken **[!UICONTROL Export]**.

   Die generierte Datei wird automatisch für Downloads in Ihrem angegebenen Ordner gespeichert.

### Berichtsspalten

| Spalte | Beschreibung |
|--- |--- |
| [!UICONTROL ID] | Eindeutige, numerische ID, die für den Suchbegriffeintrag generiert wird |
| [!UICONTROL Search Query] | Die zur Durchführung der Suche verwendete Abfrage |
| [!UICONTROL Store] | Der Speicher, auf den die Suchabfrage angewendet wurde |
| [!UICONTROL Results] | Anzahl der Ergebnisse |
| [!UICONTROL Hits] | Anzahl der Verwendungen |

{style="table-layout:auto"}
