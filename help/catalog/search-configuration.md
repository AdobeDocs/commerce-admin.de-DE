---
title: Katalogsuche konfigurieren
description: Erfahren Sie, wie Sie die Katalogsuche für Ihren Store konfigurieren.
exl-id: b4f22bce-39e2-4269-99a4-eb2d647df939
feature: Catalog Management, Search
source-git-commit: 1f84bf9ab20aeccacf56eab396b2778140964d17
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 0%

---

# Katalogsuche konfigurieren

Es gibt zwei Varianten der Konfiguration der Katalogsuche. Die erste Methode beschreibt die verfügbaren Einstellungen, wenn [Live Search](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html) installiert ist. Die zweite Methode beschreibt die Konfigurationseinstellungen für den nativen Adobe Commerce mit [Elasticsearch][1]{:target=&quot;_blank&quot;}.

## Methode 1: Adobe Commerce mit [!DNL Live Search]

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Catalog]** und wählen **[!UICONTROL Catalog]** darunter.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Catalog Search]** Abschnitt.

   ![Katalogsuche für Live Search](../configuration-reference/catalog/assets/catalog-search-live-search.png){width="600" zoomable="yes"}

   Eine detaillierte Liste dieser Optionen finden Sie unter [Adobe Commerce mit Live Search](../configuration-reference/catalog/catalog.md#adobe-commerce-with-live-search) im _Konfigurationsreferenz_.

1. Um die Länge und Wortanzahl des Suchabfragetexts zu begrenzen, legen Sie einen Wert für **[!UICONTROL Minimal Query Length]** und **[!UICONTROL Maximum Query Length]**.

1. Um die Anzahl der beliebten Suchergebnisse zu begrenzen, die für schnellere Antworten zwischengespeichert werden sollen, setzen Sie einen Wert für **[!UICONTROL Number of top search results to cache]**.

   Der Standardwert ist `100`. Wert eingeben von `0` speichert alle Suchbegriffe und Ergebnisse bei der zweiten Eingabe zwischen.

1. So ändern Sie die maximale Anzahl von Zeilen, die für zurückgegebene Ergebnisse verfügbar sind: [Storefront-Pop](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/live-search-storefront/quick-tour.html), geben Sie einen anderen ein **[!UICONTROL Autocomplete Limit]** -Wert.

   Die Einschränkung der Zeilenanzahl verbessert die Suchleistung und verringert die Größe der zurückgegebenen Liste. Der Standardwert ist `8` Zeilen.

## Methode 2: Handel mit Elasticsearch

>[!IMPORTANT]
>
>Aufgrund der [!DNL Elasticsearch 7] Ankündigung zum Ende der Unterstützung für August 2023 wird empfohlen, dass alle Adobe Commerce-Kunden zur OpenSearch 2.x-Suchmaschine migrieren. Informationen zur Migration Ihrer Suchmaschine während der Produktaktualisierung finden Sie unter [Migration zu OpenSearch](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/prepare/opensearch-migration.html) im _Upgrade-Handbuch_.

{{beta2-updates}}

### Schritt 1: Konfigurieren allgemeiner Suchoptionen

>[!NOTE]
>
>Mit Elasticsearch gibt es keine native Unterstützung für die Suche nach dem Suffix. Beispielsweise gibt die Suche nach SKU möglicherweise nicht das erwartete Ergebnis zurück, wenn der Suchbegriff nur den Endteil der SKU enthält.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Catalog]** und wählen **[!UICONTROL Catalog]** darunter.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Catalog Search]** Abschnitt.

   ![Elasticsearch-Einstellungen](../configuration-reference/catalog/assets/catalog-search-elasticsearch.png){width="600" zoomable="yes"}

   Weitere Informationen zu diesen Optionen finden Sie unter [Adobe Commerce mit Elasticsearch](../configuration-reference/catalog/catalog.md#adobe-commerce-with-elasticsearch) im _Konfigurationsreferenz_.

1. Um die Länge und Wortanzahl des Suchabfragetexts zu begrenzen, legen Sie einen Wert für **[!UICONTROL Minimal Query Length]** und **[!UICONTROL Maximum Query Length]**.

   >[!IMPORTANT]
   >
   >Der für diesen Mindest- und Höchstbereich eingestellte Wert muss mit dem entsprechenden in Ihrer Elasticsearch-Suchmaschinenkonfiguration festgelegten Bereich kompatibel sein. Wenn Sie diese Werte beispielsweise auf `2` und `300` Aktualisieren Sie in Commerce die entsprechenden Werte in Ihrer Suchmaschine.

1. Um die Anzahl der beliebten Suchergebnisse zu begrenzen, die für schnellere Antworten zwischengespeichert werden sollen, setzen Sie einen Wert für **[!UICONTROL Number of top search results to cache]**.

   Der Standardwert ist `100`. Wert eingeben von `0` speichert alle Suchbegriffe und Ergebnisse bei der zweiten Eingabe zwischen.

1. Wenn Sie den Produkt-EAV-Indexer aktivieren oder deaktivieren möchten, legen Sie die **[!UICONTROL Enable EAV Indexer]**.

   Diese Funktion verbessert die Indexierungsgeschwindigkeit und verhindert, dass der Indexer von Drittanbietererweiterungen verwendet wird.

1. Um die maximale Anzahl von Suchergebnissen zu begrenzen, die für die automatische Suche angezeigt werden sollen, legen Sie einen Wert für **[!UICONTROL Autocomplete Limit]**.

   Durch die Beschränkung dieses Betrags wird die Leistung von Suchvorgängen erhöht und die angezeigte Listengröße verringert. Der Standardwert ist `8`.

### Schritt 2: Konfigurieren der Elasticsearch-Verbindung

>[!IMPORTANT]
>
>Die **[!UICONTROL Search Engine]**, **[!UICONTROL Elasticsearch Server Hostname]**, **[!UICONTROL Elasticsearch Server Port]**, **[!UICONTROL Elasticsearch Index Prefix]**, **[!UICONTROL Enable Elasticsearch HTTP Auth]**, und **[!UICONTROL Elasticsearch Server Timeout]** -Felder wurden bei der Installation oder Aktualisierung von Commerce konfiguriert. Diese Werte sollten nur bei der Aktualisierung oder Änderung des Elasticsearchs geändert werden.

1. Für **[!UICONTROL Search Engine]**, den Standardwert akzeptieren `Elasticsearch 7`.

   Elasticsearch 7.6.x ist für alle Commerce-Installationen erforderlich.

1. Für **[!UICONTROL Elasticsearch Server Hostname]**, akzeptieren Sie den Standardwert, der bei der Installation von Commerce konfiguriert wurde.

   In diesem Beispiel lautet der Standardwert `elasticsearch.internal`.

1. Für **[!UICONTROL Elasticsearch Server Port]**, akzeptieren Sie den Standardwert, der bei der Installation von Commerce konfiguriert wurde.

   In diesem Beispiel lautet der Standardwert `9200`.

1. Für **[!UICONTROL Elasticsearch Index Prefix]**, geben Sie ein Präfix ein, um den Elasticsearch-Index zu identifizieren.

   Der Standardwert ist `magento2`.

1. Wenn Sie die HTTP-Authentifizierung verwenden möchten, um zur Eingabe eines Benutzernamens und Kennworts für den Zugriff auf Elasticsearch Server aufzufordern, legen Sie **[!UICONTROL Enable Elasticsearch HTTP Auth]** nach `Yes`.

1. Für **[!UICONTROL Elasticsearch Server Timeout]** Geben Sie die Anzahl der Sekunden ein, bevor das System eine Zeitüberschreitung aufweist.

   Der Standardwert ist `15`.

1. Klicken Sie zur Überprüfung der Konfiguration auf **[!UICONTROL Test Connection]**.

### Schritt 3: Konfigurieren von Vorschlägen und Empfehlungen

>[!NOTE]
>
>Suchvorschläge und Empfehlungen können sich auf die Serverleistung auswirken.

1. Um Empfehlungen anzubieten, legen Sie **[!UICONTROL Enable Search Recommendations]** nach `Yes` und gehen Sie wie folgt vor:

   - Für **[!UICONTROL Search Recommendation Count]**, geben Sie die Anzahl der zu unterbreitenden Empfehlungen an.

   - Um die Anzahl der für jede Empfehlung gefundenen Ergebnisse anzuzeigen, legen Sie **[!UICONTROL Show Results Count for Each Recommendation]** nach `Yes`.

1. Satz **[!UICONTROL Enable Search Suggestions]** nach `Yes` und gehen Sie wie folgt vor:

   - Für **[!UICONTROL Search Suggestions Count]**, geben Sie die Anzahl der Suchvorschläge an.

   - Um die Anzahl der für jeden Vorschlag gefundenen Ergebnisse anzuzeigen, legen Sie **[!UICONTROL Show Results for Each Suggestion]** nach `Yes`.

### Schritt 4: Konfigurieren Sie die Mindestbedingungen für die Übereinstimmung

Um die Mindestanzahl von Begriffen aus Ihrer Abfrage zu steuern, mit denen die Suchergebnisse übereinstimmen sollen, geben Sie einen Wert für **[!UICONTROL Minimum Terms to Match]**. Durch die Angabe dieses Werts wird eine optimale Ergebnisrelevanz für Käufer sichergestellt. Eine Liste der zulässigen Werte finden Sie unter [Parameter &quot;minimum_should_match&quot;](https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl-minimum-should-match.html) in der Dokumentation zum Elasticsearch.

Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

[1]: https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/search-engine/overview.html
[2]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/search/overview-search.html
