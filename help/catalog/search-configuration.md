---
title: Katalogsuche konfigurieren
description: Erfahren Sie, wie Sie die Katalogsuche für Ihren Store konfigurieren.
exl-id: b4f22bce-39e2-4269-99a4-eb2d647df939
feature: Catalog Management, Search
source-git-commit: 279f54d41264a081166cfda7d2216172ac22cd26
workflow-type: tm+mt
source-wordcount: '775'
ht-degree: 0%

---

# Katalogsuche konfigurieren

Es gibt zwei Varianten der Konfiguration der Katalogsuche. Die erste Methode beschreibt die verfügbaren Einstellungen, wenn [Live Search](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html) installiert ist. Die zweite Methode beschreibt die Konfigurationseinstellungen für nativen Adobe Commerce mit [OpenSearch](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/search-engine/overview.html){:target=&quot;_blank&quot;}.

>[!NOTE]
>
>Informationen zu Cloud-Infrastrukturprojekten finden Sie in den zusätzlichen Anweisungen im [_Handbuch zu Commerce on Cloud Infrastructure_](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/configure/service/opensearch).

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

## Methode 2: Commerce mit OpenSearch

>[!IMPORTANT]
>
>- Aufgrund der Ankündigung zum Ende des Supports für August 2023 wird empfohlen, dass alle Adobe Commerce-Kunden zur OpenSearch 2.x-Suchmaschine migrieren. [!DNL Elasticsearch 7] Informationen zur Migration Ihrer Suchmaschine während der Produktaktualisierung finden Sie unter [Migration zu OpenSearch](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/prepare/opensearch-migration.html) im _Upgrade-Handbuch_.
>- In den Versionen 2.4.4 und 2.4.3-p2 gelten alle Felder mit der Bezeichnung Elasticsearch auch für OpenSearch. Als die Unterstützung für Elasticsearch 8.x in Version 2.4.6 eingeführt wurde, wurden neue Bezeichnungen erstellt, um zwischen Elasticsearch- und OpenSearch-Konfigurationen zu unterscheiden. Die Konfigurationsoptionen für beide sind jedoch identisch.

### Schritt 1: Konfigurieren allgemeiner Suchoptionen

>[!NOTE]
>
>Bei OpenSearch und Elasticsearch gibt es keine native Unterstützung für die Suche nach dem Suffix. Beispielsweise gibt die Suche nach SKU möglicherweise nicht das erwartete Ergebnis zurück, wenn der Suchbegriff nur den Endteil der SKU enthält.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bedienfeld den Wert **[!UICONTROL Catalog]** und wählen Sie unter &quot;**[!UICONTROL Catalog]**&quot;.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Catalog Search]** .

   ![Suchmaschineneinstellungen](../configuration-reference/catalog/assets/catalog-search-opensearch.png){zoomable="yes"}

   Weitere Informationen zu diesen Optionen finden Sie unter [Adobe Commerce mit nativer Suche](../configuration-reference/catalog/catalog.md#adobe-commerce-with-native-search) in der _Konfigurationsreferenz_.

1. Legen Sie einen Wert für **[!UICONTROL Minimal Query Length]** und **[!UICONTROL Maximum Query Length]** fest, um die Länge und Wortanzahl des Suchabfragetexts zu begrenzen.

   >[!IMPORTANT]
   >
   >Der für diesen Mindest- und Höchstbereich festgelegte Wert muss mit dem entsprechenden in Ihrer Suchmaschinenkonfiguration festgelegten Bereich kompatibel sein. Wenn Sie diese Werte beispielsweise in Commerce auf `2` und `300` setzen, aktualisieren Sie die entsprechenden Werte in Ihrer Suchmaschine.

1. Um die Anzahl der beliebten Suchergebnisse zu begrenzen, die für schnellere Antworten zwischengespeichert werden sollen, legen Sie einen Wert für **[!UICONTROL Number of top search results to cache]** fest.

   Der Standardwert ist `100`. Wenn Sie den Wert `0` eingeben, werden alle Suchbegriffe und Ergebnisse zwischengespeichert, wenn Sie zum zweiten Mal eingegeben werden.

1. Wenn Sie den Produkt-EAV-Indexer aktivieren oder deaktivieren möchten, legen Sie den **[!UICONTROL Enable EAV Indexer]** fest.

   Diese Funktion verbessert die Indexierungsgeschwindigkeit und verhindert, dass der Indexer von Drittanbietererweiterungen verwendet wird.

1. Um die maximale Anzahl von Suchergebnissen zu begrenzen, die für die automatische Suchabwicklung angezeigt werden sollen, legen Sie einen Wert für **[!UICONTROL Autocomplete Limit]** fest.

   Durch die Beschränkung dieses Betrags wird die Leistung von Suchvorgängen erhöht und die angezeigte Listengröße verringert. Der Standardwert ist `8`.

### Schritt 2: Konfigurieren der OpenSearch-Verbindung

>[!IMPORTANT]
>
>Die Felder **[!UICONTROL Search Engine]**, **[!UICONTROL OpenSearch Server Hostname]**, **[!UICONTROL OpenSearch Server Port]**, **[!UICONTROL OpenSearch Index Prefix]**, **[!UICONTROL Enable OpenSearch HTTP Auth]** und **[!UICONTROL OpenSearch Server Timeout]** wurden bei der Installation oder Aktualisierung von Commerce konfiguriert. Diese Werte sollten nur bei der Aktualisierung oder Änderung von OpenSearch geändert werden.

1. Wählen Sie für **[!UICONTROL Search Engine]** `OpenSearch` aus.

1. Akzeptieren Sie für **[!UICONTROL OpenSearch Server Hostname]** den Standardwert, der bei der Installation von Commerce konfiguriert wurde.

1. Akzeptieren Sie für **[!UICONTROL OpenSearch Server Port]** den Standardwert, der bei der Installation von Commerce konfiguriert wurde.

   In diesem Beispiel ist der Standardwert `9200`.

1. Geben Sie für &quot;**[!UICONTROL OpenSearch Index Prefix]**&quot;ein Präfix ein, um den Elasticsearch-Index zu identifizieren.

   Der Standardwert ist `magento2`.

1. Um die HTTP-Authentifizierung zu verwenden, um zur Eingabe eines Benutzernamens und Kennworts für den Zugriff auf den OpenSearch-Server aufzufordern, setzen Sie **[!UICONTROL Enable OpenSearch HTTP Auth]** auf `Yes`.

1. Geben Sie für &quot;**[!UICONTROL OpenSearch Server Timeout]**&quot;die Anzahl der Sekunden ein, bevor das System eine Zeitüberschreitung aufweist.

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

Um die Mindestanzahl von Begriffen aus Ihrer Abfrage zu steuern, mit denen die Suchergebnisse übereinstimmen sollen, geben Sie einen Wert für **[!UICONTROL Minimum Terms to Match]** an. Durch die Angabe dieses Werts wird eine optimale Ergebnisrelevanz für Käufer sichergestellt. Eine Liste der zulässigen Werte finden Sie unter [minimum_should_match parameter](https://opensearch.org/docs/latest/query-dsl/minimum-should-match/) in der OpenSearch-Dokumentation.

Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.
