---
title: Suchbegriffe verwalten
description: Erfahren Sie, wie Sie die Suchbegriffe für Ihren Store verwalten, um Kunden mit falsch geschriebenen oder alternativen Begriffen umzuleiten.
exl-id: e21ece58-2bc2-49ef-96d3-3be930e09f94
feature: Catalog Management, Search
source-git-commit: 3851258543ba829a4bdbfdb5d3d053ec4627184a
workflow-type: tm+mt
source-wordcount: '1166'
ht-degree: 0%

---

# Suchbegriffe verwalten

Die [Landingpage](../content-design/pages.md) für einen Suchbegriff kann eine Inhaltsseite, eine Kategorieseite, eine Produktdetailseite oder sogar eine Seite auf einer anderen Site sein.

Verwenden Sie Suchbegriffe, um gängige Rechtschreibfehler zu erfassen und sie auf die entsprechende Seite umzuleiten. Wenn Sie beispielsweise Möbel aus Schmiedeeisen verkaufen, wissen Sie, dass viele Menschen den Begriff falsch schreiben als _Stangeneisen_ oder sogar _Roseneisen_. Sie können jedes falsch geschriebene Wort als Suchbegriff eingeben und zu Synonymen für _Schmiedeeisen_ machen. Obwohl das Wort falsch geschrieben ist, wird die Suche auf die Seite für Schmiedeeisen geleitet.

Sie können auch erfahren, wonach Ihre Kunden suchen, indem Sie die Suchbegriffe untersuchen, mit denen sie Produkte in Ihrem Geschäft finden. Wenn ausreichend Personen nach einem Produkt suchen, das nicht in Ihrem Katalog enthalten ist, könnte dies auf eine Verkaufschance hindeuten. In der Zwischenzeit können Sie sie zu einem anderen Produkt in Ihrem Katalog umleiten, anstatt sie leer zu lassen.

## Suchbegriffe hinzufügen

Wenn Sie neue Wörter lernen, die Benutzer für die Suche in Ihrem Geschäft verwenden, können Sie sie zu Ihrer Suchbegriffliste hinzufügen, um Personen zu den am ehesten passenden Produkten in Ihrem Katalog zu leiten.

![Raster der Suchbegriffe](./assets/search-terms.png){width="700" zoomable="yes"}

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

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Search Terms]**.

1. Klicken Sie auf **[!UICONTROL Add New Search Term]**.

   ![Allgemeine Informationen zu Suchbegriffen](./assets/search-terms-information.png){width="600" zoomable="yes"}

1. Geben Sie unter _[!UICONTROL General Information]_in das Feld **[!UICONTROL Search Query]**das Wort oder die Wortgruppe ein, das/die Sie als neuen Suchbegriff hinzufügen möchten.

1. Wenn Ihr Store in mehreren Sprachen verfügbar ist, wählen Sie die entsprechende **[!UICONTROL Store]**-Ansicht aus.

1. Um die Suchergebnisse auf eine andere Seite in Ihrem Store oder auf eine andere Website umzuleiten, geben Sie die vollständige URL der Zielseite in das Feld **[!UICONTROL Redirect URL]** ein.

1. Wenn Sie möchten, dass dieser Begriff immer als Vorschlag verwendet werden kann, wenn eine Suche keine Ergebnisse zurückgibt, setzen Sie **[!UICONTROL Display in Suggested Terms]** auf `Yes`.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Search]**.

## Suchbegriffe bearbeiten

1. Klicken Sie im Raster _[!UICONTROL Search Terms]_auf die Zeile eines Datensatzes, um den Suchbegriff im Bearbeitungsmodus zu öffnen.

1. Nehmen Sie die erforderlichen Änderungen vor.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Search]**.

## Suchbegriff löschen

Es gibt zwei Methoden zum Löschen eines Suchbegriffs aus dem Raster und auf der Bearbeitungsseite.

**Methode 1:** im Raster _[!UICONTROL Search Terms]_

1. Aktivieren Sie in der Liste das Kontrollkästchen des zu löschenden Begriffs.

1. Setzen Sie **[!UICONTROL Actions]** in der linken oberen Ecke der Liste auf `Delete`.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Submit]**.

**Methode 2:** auf der Seite _[!UICONTROL Edit a Search Term]_

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Search Terms]**.

1. Suchen Sie den zu löschenden Suchbegriff und öffnen Sie ihn im Bearbeitungsmodus.

1. Klicken Sie auf **[!UICONTROL Delete Search]**.

1. Um die Aktion zu bestätigen, klicken Sie auf **[!UICONTROL OK]**.

## Beliebte Suchbegriffe

Der Link _Suchbegriffe_ in der Fußzeile Ihres Stores zeigt die Suchbegriffe an, die von Besuchern Ihres Stores verwendet werden, sortiert nach Beliebtheit. Suchbegriffe werden im Format _Tag-Cloud_ angezeigt, wobei die Textgröße die Beliebtheit des Begriffs anzeigt.

Standardmäßig sind populäre Suchbegriffe als Suchmaschinen-Optimierungs-Tool aktiviert, doch es besteht keine direkte Verbindung zum Katalogsuchprozess. Da die Seite &quot;Suchbegriffe&quot;von Suchmaschinen indexiert wird, können alle Begriffe auf der Seite dazu beitragen, das Ranking Ihrer Suchmaschine und die Sichtbarkeit Ihres Geschäfts zu verbessern. Die URL der Seite &quot;Beliebte Suchbegriffe&quot;lautet: `mystore.com/search/term/popular/`

![Beispiel-Storefront - beliebte Suchbegriffe](./assets/store-front-search-terms-yoga-pants.png){width="600" zoomable="yes"}

**_So konfigurieren Sie beliebte Suchbegriffe:_**

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bedienfeld den Wert **[!UICONTROL Catalog]** und wählen Sie unter &quot;**[!UICONTROL Catalog]**&quot;.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Search Engine Optimization]** .

   ![Katalogkonfiguration - Suchmaschinenoptimierung](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

   Eine detaillierte Liste dieser Optionen finden Sie unter [Suchmaschinenoptimierung](../configuration-reference/catalog/catalog.md#search-engine-optimization) in der _Konfigurationsreferenz_.

1. Legen Sie **[!UICONTROL Popular Search Terms]** nach Bedarf fest.

   Deaktivieren Sie bei Bedarf das Kontrollkästchen **[!UICONTROL Use system value]** , um diese Einstellung zu ändern.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

>[!NOTE]
>
>Sie können die Zwischenspeicherung beliebter [Katalogsuchvorgänge](search-configuration.md) weiter konfigurieren.

## Synonyme suchen

Eine Möglichkeit, die Effektivität der [Katalogsuche](search-configuration.md) zu verbessern, besteht darin, verschiedene Begriffe einzuschließen, die zur Beschreibung desselben Elements verwendet werden können. Sie möchten keinen Verkauf verlieren, nur weil jemand nach einem _Sofa_ sucht und Ihr Produkt als _Couch_ aufgeführt ist. Sie können einen breiteren Bereich von Suchbegriffen erfassen, indem Sie _sofa_, _davenport_ und _loveseat_ als Synonyme für _couch_ eingeben und sie auf dieselbe Landingpage weiterleiten.

Adobe Commerce unterstützt zwei verschiedene Synonym-Verwaltungslösungen:

- Die Funktion &quot;Live-Suche&quot;[Synonyme](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/live-search-admin/synonyms/synonyms.html) ist für Adobe Commerce-Installationen mit installierter Live-Suche verfügbar.
- Die standardmäßige Funktion &quot;Synonyme suchen&quot;(auf dieser Seite beschrieben) ist für alle Adobe Commerce-Installationen standardmäßig verfügbar.

>[!NOTE]
>
>Die standardmäßige Funktion &quot;Synonyme suchen&quot;unterstützt standardmäßig die Produktattribute `name` und `sku` **_nur_**.

>[!IMPORTANT]
>
>Die Funktion &quot;Synonyme suchen&quot;verwendet nur die Suchmethode für die Volltextabstimmung.

![Beispiel-Storefront - Suchergebnisse mit Synonymen](./assets/storefront-search-results-synonyms.png){width="700" zoomable="yes"}

### Synonymisierungsgruppe erstellen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Search Synonyms]**.

   Das Raster _[!UICONTROL Search Synonyms]_wird angezeigt. Wenn Sie zum ersten Mal Suchsynonyme verwenden, ist das Raster leer.

   ![Synonym-Raster durchsuchen](./assets/search-synonyms-grid-empty.png){width="700" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL New Synonym Group]**.

   ![Neue Gruppe von Suchsynonymen](./assets/search-synonym-group-new.png){width="700" zoomable="yes"}

1. Setzen Sie **[!UICONTROL Scope]** auf die Store-Ansichten, für die die Synonyme gelten.

1. Geben Sie jedes Synonym in der Gruppe durch Kommas getrennt ein. Wählen Sie Wörter aus, die Personen als Suchkriterien verwenden können. Beispiel:

   - `sweatshirt, sweat shirt, hoodie, fleece`
   - `cell phone, mobile phone, smart phone`
   - `couch, sofa, davenport`
   - `wrought iron, rot iron, rod iron`

1. Um diese Synonyme mit anderen Gruppen mit demselben Gültigkeitsbereich zusammenzuführen, aktivieren Sie das Kontrollkästchen **[!UICONTROL Merge existing synonyms]** .

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Synonym Group]**.

### Eine Synonymisierungsgruppe bearbeiten

1. Klicken Sie im Raster _[!UICONTROL Search Synonyms]_auf die Zeile eines Datensatzes, um die Synonym-Gruppe im Bearbeitungsmodus zu öffnen.

1. Nehmen Sie die erforderlichen Änderungen vor.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Synonym Group]**.

### Eine Synonymisierungsgruppe löschen

Es gibt zwei Methoden zum Löschen einer Synonym-Gruppe - aus dem Raster und auf der Bearbeitungsseite.

**Methode 1:** im Raster &quot;Suchsynonyme&quot;

1. Aktivieren Sie im Raster _[!UICONTROL Search Synonyms]_das Kontrollkästchen der zu löschenden Gruppe.

1. Setzen Sie **[!UICONTROL Actions]** in der linken oberen Ecke der Liste auf `Delete`.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Submit]**.

**Methode 2:** auf der Seite &quot;Synonyme Gruppe bearbeiten&quot;

1. Klicken Sie im Raster &quot;Synonyme suchen&quot;auf die Zeile eines Datensatzes, um die Synonym-Gruppe im Bearbeitungsmodus zu öffnen.

1. Klicken Sie auf **[!UICONTROL Delete Synonym Group]**.

1. Bestätigen Sie bei entsprechender Aufforderung das Entfernen der Gruppe.

## Bericht &quot;Suchbegriffe&quot;

Der Bericht zu Suchbegriffen zeigt die Anzahl der Ergebnisse für jeden Begriff und die Anzahl der verwendeten Begriffe (Treffer) an. Die Berichtsdaten können nach Begriff, Speicher, Ergebnissen und Treffern gefiltert und zur weiteren Analyse exportiert werden.

### Bericht anzeigen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Reports]** > _[!UICONTROL Marketing]_>**[!UICONTROL Search Terms]**.

1. Verwenden Sie die Steuerelemente, um den Bericht nach Bedarf zu filtern.

   ![Suchbegriffsbericht](./assets/search-terms-report.png){width="700" zoomable="yes"}

## Bericht exportieren

1. Wählen Sie für **[!UICONTROL Export to]** ein Exportformat:

   - `CSV` - Eine kommagetrennte Wertdatei mit Textdaten
   - `Excel XML` - Ein XML-basiertes Tabellendatenformat

1. Klicken Sie auf **[!UICONTROL Export]**.

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
