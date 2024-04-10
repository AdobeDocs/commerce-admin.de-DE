---
title: Konfigurieren der Katalogsuche
description: Erfahren Sie, wie Sie die Katalogsuche für Ihren Store konfigurieren.
exl-id: b4f22bce-39e2-4269-99a4-eb2d647df939
feature: Catalog Management, Search
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '729'
ht-degree: 0%

---

# Konfigurieren der Katalogsuche

Es gibt zwei Varianten der Konfiguration der Katalogsuche. Die erste Methode beschreibt die verfügbaren Einstellungen, wenn [Live Search](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html) ist installiert. Die zweite Methode beschreibt die Konfigurationseinstellungen für native Adobe Commerce mit [Elasticsearch][1]{:target=„_blank„}.

## Methode 1: Adobe Commerce mit [!DNL Live Search]

1. Auf der _Admin_ Seitenleiste, zu gehen **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich . **[!UICONTROL Catalog]** und wählen **[!UICONTROL Catalog]** Darunter.

1. Expand ![Erweiterungsauswahl](../assets/icon-display-expand.png) Die **[!UICONTROL Catalog Search]** -Abschnitt.

   ![Katalogsuche für die Live Search](../configuration-reference/catalog/assets/catalog-search-live-search.png){width="600" zoomable="yes"}

   Eine detaillierte Liste dieser Optionen finden Sie unter [Adobe Commerce mit Live Search](../configuration-reference/catalog/catalog.md#adobe-commerce-with-live-search) in der _Konfigurationsreferenz_.

1. Legen Sie einen Wert für fest, um die Länge und Wortzahl des Suchabfragetextes zu begrenzen **[!UICONTROL Minimal Query Length]** und **[!UICONTROL Maximum Query Length]**.

1. Um die Anzahl der beliebten Suchergebnisse zu begrenzen, die für schnellere Antworten zwischengespeichert werden sollen, legen Sie einen Wert für fest. **[!UICONTROL Number of top search results to cache]**.

   Der Standardwert lautet `100`. Einen Wert eingeben von `0` speichert alle Suchbegriffe und Ergebnisse bei einer zweiten Eingabe zwischen.

1. So ändern Sie die maximale Anzahl von Zeilen, die für zurückgegebene Ergebnisse in der [Schaufenster-Pop-Over](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/live-search-storefront/quick-tour.html), einen anderen eingeben **[!UICONTROL Autocomplete Limit]** Wert.

   Durch die Begrenzung der Zeilenanzahl wird die Leistung der Suchvorgänge verbessert und die Größe der zurückgegebenen Liste verringert. Der Standardwert lautet `8` Zeilen.

## Methode 2: Handel mit Elasticsearch

>[!IMPORTANT]
>
>Aufgrund der [!DNL Elasticsearch 7] Ankündigung zum Ende der Unterstützung für August 2023 wird empfohlen, dass alle Adobe Commerce-Kunden zur OpenSearch 2.x -Suchmaschine migrieren. Informationen zur Migration Ihrer Suchmaschine während des Produkt-Upgrades finden Sie unter [Migration zu OpenSearch](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/prepare/opensearch-migration.html) in der _Aktualisierungshandbuch_.

### Schritt 1: Konfigurieren der allgemeinen Suchoptionen

>[!NOTE]
>
>Bei Elasticsearch gibt es keine vordefinierte Unterstützung für die Suche nach dem Suffix. Beispielsweise liefert die Suche nach SKU möglicherweise nicht das erwartete Ergebnis, wenn das Keyword nur den Endteil der SKU enthält.

1. Auf der _Admin_ Seitenleiste, zu gehen **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich . **[!UICONTROL Catalog]** und wählen **[!UICONTROL Catalog]** Darunter.

1. Expand ![Erweiterungsauswahl](../assets/icon-display-expand.png) Die **[!UICONTROL Catalog Search]** -Abschnitt.

   ![Elasticsearch Settings](../configuration-reference/catalog/assets/catalog-search-elasticsearch.png){width="600" zoomable="yes"}

   Weitere Informationen zu diesen Optionen finden Sie unter [Adobe Commerce mit Elasticsearch](../configuration-reference/catalog/catalog.md#adobe-commerce-with-elasticsearch) in der _Konfigurationsreferenz_.

1. Legen Sie einen Wert für fest, um die Länge und Wortzahl des Suchabfragetextes zu begrenzen **[!UICONTROL Minimal Query Length]** und **[!UICONTROL Maximum Query Length]**.

   >[!IMPORTANT]
   >
   >Der für diesen Mindest- und Höchstbereich festgelegte Wert muss mit dem entsprechenden Bereich kompatibel sein, der in Ihrer Elasticsearch-Suchmaschinenkonfiguration festgelegt ist. Wenn Sie diese Werte beispielsweise auf setzen `2` und `300` Aktualisieren Sie in Commerce die entsprechenden Werte in Ihrer Suchmaschine.

1. Um die Anzahl der beliebten Suchergebnisse zu begrenzen, die für schnellere Antworten zwischengespeichert werden sollen, legen Sie einen Wert für fest. **[!UICONTROL Number of top search results to cache]**.

   Der Standardwert lautet `100`. Einen Wert eingeben von `0` speichert alle Suchbegriffe und Ergebnisse bei einer zweiten Eingabe zwischen.

1. Wenn Sie den Produkt-EAV-Indexer aktivieren oder deaktivieren möchten, legen Sie Folgendes fest: **[!UICONTROL Enable EAV Indexer]**.

   Diese Funktion verbessert die Indexierungsgeschwindigkeit und verhindert, dass der Indexer von Erweiterungen von Drittanbietern verwendet werden kann.

1. Um die maximale Anzahl von Suchergebnissen zu begrenzen, die für die automatische Vervollständigung der Suche angezeigt werden sollen, legen Sie einen Betrag für fest **[!UICONTROL Autocomplete Limit]**.

   Wenn Sie diesen Wert einschränken, wird die Leistung der Suchvorgänge gesteigert und die angezeigte Listengröße verringert. Der Standardwert lautet `8`.

### Schritt 2: Konfigurieren der Elasticsearch-Verbindung

>[!IMPORTANT]
>
>Die **[!UICONTROL Search Engine]**, **[!UICONTROL Elasticsearch Server Hostname]**, **[!UICONTROL Elasticsearch Server Port]**, **[!UICONTROL Elasticsearch Index Prefix]**, **[!UICONTROL Enable Elasticsearch HTTP Auth]**, und **[!UICONTROL Elasticsearch Server Timeout]** -Felder wurden konfiguriert, als Commerce installiert oder aktualisiert wurde. Diese Werte sollten nur beim Aktualisieren oder Ändern von Elasticsearch geändert werden.

1. für **[!UICONTROL Search Engine]**, akzeptieren den Standardwert `Elasticsearch 7`.

   Für alle Commerce-Installationen ist Elasticsearch 7.6.x erforderlich.

1. für **[!UICONTROL Elasticsearch Server Hostname]**, akzeptieren den Standardwert, der bei der Installation von Commerce konfiguriert wurde.

   In diesem Beispiel lautet der Standardwert `elasticsearch.internal`.

1. für **[!UICONTROL Elasticsearch Server Port]**, akzeptieren den Standardwert, der bei der Installation von Commerce konfiguriert wurde.

   In diesem Beispiel lautet der Standardwert `9200`.

1. für **[!UICONTROL Elasticsearch Index Prefix]**, geben Sie ein Präfix ein, um den Elasticsearch-Index zu identifizieren.

   Der Standardwert lautet `magento2`.

1. Um die HTTP-Authentifizierung zur Eingabe eines Benutzernamens und Kennworts für den Zugriff auf den Elasticsearch-Server zu verwenden, legen Sie Folgendes fest **[!UICONTROL Enable Elasticsearch HTTP Auth]** bis `Yes`.

1. für **[!UICONTROL Elasticsearch Server Timeout]** Geben Sie hier die Anzahl der Sekunden ein, nach denen das System eine Zeitüberschreitung erleidet.

   Der Standardwert lautet `15`.

1. Um die Konfiguration zu überprüfen, klicken Sie auf **[!UICONTROL Test Connection]**.

### Schritt 3: Konfigurieren von Vorschlägen und Empfehlungen

>[!NOTE]
>
>Suchvorschläge und -empfehlungen können die Serverleistung beeinträchtigen.

1. Um Empfehlungen anzubieten, legen Sie Folgendes fest **[!UICONTROL Enable Search Recommendations]** bis `Yes` und führen Sie folgende Schritte aus:

   - für **[!UICONTROL Search Recommendation Count]**, geben Sie die Anzahl der zu unterbreitenden Empfehlungen ein.

   - Um die Anzahl der Ergebnisse anzuzeigen, die für jede Empfehlung gefunden wurden, legen Sie fest **[!UICONTROL Show Results Count for Each Recommendation]** bis `Yes`.

1. set **[!UICONTROL Enable Search Suggestions]** bis `Yes` und führen Sie folgende Schritte aus:

   - für **[!UICONTROL Search Suggestions Count]**, geben Sie die Anzahl der Suchvorschläge ein, die unterbreitet werden sollen.

   - Um die Anzahl der Ergebnisse anzuzeigen, die für jeden Vorschlag gefunden wurden, legen Sie Folgendes fest **[!UICONTROL Show Results for Each Suggestion]** bis `Yes`.

### Schritt 4: Konfigurieren der Mindestbedingungen, die übereinstimmen

Um die Mindestanzahl von Begriffen aus Ihrer Abfrage zu steuern, mit denen die Suchergebnisse für die Rückgabe übereinstimmen sollen, geben Sie einen Wert für an **[!UICONTROL Minimum Terms to Match]**. Durch die Angabe dieses Werts wird eine optimale Ergebnisrelevanz für Erstkäufer sichergestellt. Eine Liste der zulässigen Werte finden Sie unter [minimum_should_match-Parameter](https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl-minimum-should-match.html) in der Dokumentation zum Elasticsearch.

Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

[1]: https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/search-engine/overview.html
[2]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/search/overview-search.html
