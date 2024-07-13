---
title: Katalogsuche konfigurieren
description: Erfahren Sie, wie Sie die Katalogsuche für Ihren Store konfigurieren.
exl-id: b4f22bce-39e2-4269-99a4-eb2d647df939
feature: Catalog Management, Search
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '729'
ht-degree: 0%

---

# Katalogsuche konfigurieren

Es gibt zwei Varianten der Konfiguration der Katalogsuche. Die erste Methode beschreibt die verfügbaren Einstellungen, wenn [Live Search](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html) installiert ist. Die zweite Methode beschreibt die Konfigurationseinstellungen für den nativen Adobe Commerce mit [Elasticsearch][1]{:target=&quot;_blank&quot;}.

## Methode 1: Adobe Commerce mit [!DNL Live Search]

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bedienfeld den Wert **[!UICONTROL Catalog]** und wählen Sie unter &quot;**[!UICONTROL Catalog]**&quot;.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Catalog Search]** .

   ![Katalogsuche nach Live Search](../configuration-reference/catalog/assets/catalog-search-live-search.png){width="600" zoomable="yes"}

   Eine detaillierte Liste dieser Optionen finden Sie unter [Adobe Commerce mit Live Search](../configuration-reference/catalog/catalog.md#adobe-commerce-with-live-search) in der _Konfigurationsreferenz_.

1. Legen Sie einen Wert für **[!UICONTROL Minimal Query Length]** und **[!UICONTROL Maximum Query Length]** fest, um die Länge und Wortanzahl des Suchabfragetexts zu begrenzen.

1. Um die Anzahl der beliebten Suchergebnisse zu begrenzen, die für schnellere Antworten zwischengespeichert werden sollen, legen Sie einen Wert für **[!UICONTROL Number of top search results to cache]** fest.

   Der Standardwert ist `100`. Wenn Sie den Wert `0` eingeben, werden alle Suchbegriffe und Ergebnisse zwischengespeichert, wenn Sie zum zweiten Mal eingegeben werden.

1. Geben Sie einen anderen **[!UICONTROL Autocomplete Limit]** -Wert ein, um die maximale Anzahl von Zeilen zu ändern, die für zurückgegebene Ergebnisse im [Storefront-Pop over](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/live-search-storefront/quick-tour.html) verfügbar sind.

   Die Einschränkung der Zeilenanzahl verbessert die Suchleistung und verringert die Größe der zurückgegebenen Liste. Der Standardwert ist `8` Zeilen.

## Methode 2: Commerce mit Elasticsearch

>[!IMPORTANT]
>
>Aufgrund der Ankündigung zum Ende des Supports für August 2023 wird empfohlen, dass alle Adobe Commerce-Kunden zur OpenSearch 2.x-Suchmaschine migrieren. [!DNL Elasticsearch 7] Informationen zur Migration Ihrer Suchmaschine während der Produktaktualisierung finden Sie unter [Migration zu OpenSearch](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/prepare/opensearch-migration.html) im _Upgrade-Handbuch_.

### Schritt 1: Konfigurieren allgemeiner Suchoptionen

>[!NOTE]
>
>Mit Elasticsearch gibt es keine native Unterstützung für die Suche nach dem Suffix. Beispielsweise gibt die Suche nach SKU möglicherweise nicht das erwartete Ergebnis zurück, wenn der Suchbegriff nur den Endteil der SKU enthält.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bedienfeld den Wert **[!UICONTROL Catalog]** und wählen Sie unter &quot;**[!UICONTROL Catalog]**&quot;.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Catalog Search]** .

   ![Elasticsearch-Einstellungen](../configuration-reference/catalog/assets/catalog-search-elasticsearch.png){width="600" zoomable="yes"}

   Weitere Informationen zu diesen Optionen finden Sie unter [Adobe Commerce mit Elasticsearch](../configuration-reference/catalog/catalog.md#adobe-commerce-with-elasticsearch) in der _Konfigurationsreferenz_.

1. Legen Sie einen Wert für **[!UICONTROL Minimal Query Length]** und **[!UICONTROL Maximum Query Length]** fest, um die Länge und Wortanzahl des Suchabfragetexts zu begrenzen.

   >[!IMPORTANT]
   >
   >Der für diesen Mindest- und Höchstbereich eingestellte Wert muss mit dem entsprechenden in Ihrer Elasticsearch-Suchmaschinenkonfiguration festgelegten Bereich kompatibel sein. Wenn Sie diese Werte beispielsweise in Commerce auf `2` und `300` setzen, aktualisieren Sie die entsprechenden Werte in Ihrer Suchmaschine.

1. Um die Anzahl der beliebten Suchergebnisse zu begrenzen, die für schnellere Antworten zwischengespeichert werden sollen, legen Sie einen Wert für **[!UICONTROL Number of top search results to cache]** fest.

   Der Standardwert ist `100`. Wenn Sie den Wert `0` eingeben, werden alle Suchbegriffe und Ergebnisse zwischengespeichert, wenn Sie zum zweiten Mal eingegeben werden.

1. Wenn Sie den Produkt-EAV-Indexer aktivieren oder deaktivieren möchten, legen Sie den **[!UICONTROL Enable EAV Indexer]** fest.

   Diese Funktion verbessert die Indexierungsgeschwindigkeit und verhindert, dass der Indexer von Drittanbietererweiterungen verwendet wird.

1. Um die maximale Anzahl von Suchergebnissen zu begrenzen, die für die automatische Suchabwicklung angezeigt werden sollen, legen Sie einen Wert für **[!UICONTROL Autocomplete Limit]** fest.

   Durch die Beschränkung dieses Betrags wird die Leistung von Suchvorgängen erhöht und die angezeigte Listengröße verringert. Der Standardwert ist `8`.

### Schritt 2: Konfigurieren der Elasticsearch-Verbindung

>[!IMPORTANT]
>
>Die Felder **[!UICONTROL Search Engine]**, **[!UICONTROL Elasticsearch Server Hostname]**, **[!UICONTROL Elasticsearch Server Port]**, **[!UICONTROL Elasticsearch Index Prefix]**, **[!UICONTROL Enable Elasticsearch HTTP Auth]** und **[!UICONTROL Elasticsearch Server Timeout]** wurden bei der Installation oder Aktualisierung von Commerce konfiguriert. Diese Werte sollten nur bei der Aktualisierung oder Änderung des Elasticsearchs geändert werden.

1. Für **[!UICONTROL Search Engine]** den Standardwert `Elasticsearch 7` akzeptieren.

   Elasticsearch 7.6.x ist für alle Commerce-Installationen erforderlich.

1. Akzeptieren Sie für **[!UICONTROL Elasticsearch Server Hostname]** den Standardwert, der bei der Installation von Commerce konfiguriert wurde.

   In diesem Beispiel ist der Standardwert `elasticsearch.internal`.

1. Akzeptieren Sie für **[!UICONTROL Elasticsearch Server Port]** den Standardwert, der bei der Installation von Commerce konfiguriert wurde.

   In diesem Beispiel ist der Standardwert `9200`.

1. Geben Sie für &quot;**[!UICONTROL Elasticsearch Index Prefix]**&quot;ein Präfix ein, um den Elasticsearch-Index zu identifizieren.

   Der Standardwert ist `magento2`.

1. Um die HTTP-Authentifizierung zu verwenden, um einen Benutzernamen und ein Kennwort für den Zugriff auf Elasticsearch Server anzufordern, setzen Sie **[!UICONTROL Enable Elasticsearch HTTP Auth]** auf `Yes`.

1. Geben Sie für &quot;**[!UICONTROL Elasticsearch Server Timeout]**&quot;die Anzahl der Sekunden ein, bevor das System eine Zeitüberschreitung aufweist.

   Der Standardwert ist `15`.

1. Um die Konfiguration zu überprüfen, klicken Sie auf **[!UICONTROL Test Connection]**.

### Schritt 3: Konfigurieren von Vorschlägen und Empfehlungen

>[!NOTE]
>
>Suchvorschläge und Empfehlungen können sich auf die Serverleistung auswirken.

1. Um Empfehlungen anzubieten, setzen Sie **[!UICONTROL Enable Search Recommendations]** auf `Yes` und führen Sie die folgenden Schritte aus:

   - Geben Sie für &quot;**[!UICONTROL Search Recommendation Count]**&quot;die Anzahl der anzubietenden Empfehlungen an.

   - Um die Anzahl der für jede Empfehlung gefundenen Ergebnisse anzuzeigen, setzen Sie **[!UICONTROL Show Results Count for Each Recommendation]** auf `Yes`.

1. Setzen Sie **[!UICONTROL Enable Search Suggestions]** auf `Yes` und führen Sie folgende Schritte aus:

   - Geben Sie für &quot;**[!UICONTROL Search Suggestions Count]**&quot;die Anzahl der anzubietenden Suchvorschläge ein.

   - Um die Anzahl der für jeden Vorschlag gefundenen Ergebnisse anzuzeigen, setzen Sie **[!UICONTROL Show Results for Each Suggestion]** auf `Yes`.

### Schritt 4: Konfigurieren Sie die Mindestbedingungen für die Übereinstimmung

Um die Mindestanzahl von Begriffen aus Ihrer Abfrage zu steuern, mit denen die Suchergebnisse übereinstimmen sollen, geben Sie einen Wert für **[!UICONTROL Minimum Terms to Match]** an. Durch die Angabe dieses Werts wird eine optimale Ergebnisrelevanz für Käufer sichergestellt. Eine Liste der zulässigen Werte finden Sie unter [minimum_should_match parameter](https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl-minimum-should-match.html) in der Elasticsearch-Dokumentation.

Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

[1]: https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/search-engine/overview.html
[2]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/search/overview-search.html
