---
title: Suchbegriff-Umleitungen und Storefront-Routing
description: Erfahren Sie, wie Sie Suchbegriffe, URL-Neuschreibungen, Live-Suchregeln oder Storefront-Routing nach Bereitstellung für Adobe Commerce und Edge Delivery Services auswählen.
feature: Merchandising, Search
role: Admin, User
level: Intermediate
topic: Commerce, Administration
autotag-review: '2026-09-10T17:42:01.349Z'
TQID: 'https://experienceleague.adobe.com/Vxw3B0zOzLZfAm3qn8gJKHGSNtVhkN2Bfmcauhj0sdM'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 67a00b294f1946da5795cd8fb7ea9fac1c80edcd
workflow-type: tm+mt
source-wordcount: '970'
ht-degree: 0%
---
# Suchbegriff-Umleitungen und Storefront-Routing

Suchbegriff-Weiterleitungen, URL-Weiterleitungen und Merchandising-Suchvorgänge lösen verschiedene Probleme. Verwenden Sie dieses Handbuch, um die richtigen Funktionen für die standardmäßige [!DNL Adobe Commerce]-Suche, [!DNL Live Search] und [!DNL Commerce Storefront] mit [!DNL Edge Delivery Services] auszuwählen.

## Umleitungstypen verstehen

Diese Funktionen unterscheiden sich in den Triggern des Verhaltens und dem, was der Käufer sieht:

* Eine **Suchbegriff-Umleitung** sendet einen Einkäufer, der einen bestimmten Suchbegriff eingibt, an eine bestimmte Seite.

* Eine **URL-Umleitung** sendet eine Anfrage nach einer alten URL an eine neue URL, in der Regel mit einer HTTP-Antwort von 301 oder 302. Die Browser-Adressleiste ändert sich in die neue URL.

* **Search Merchandising** ändert, welche Produkte in den Suchergebnissen angezeigt werden, ohne die angeforderte URL zu ändern.

* Eine **URL-Umschreibung** ordnet eine URL einer anderen auf dem Server zu. Das [!DNL Adobe Commerce] URL Rewrite-Tool erstellt eine permanente Umleitung (301) für die alte URL. Weitere Informationen finden Sie unter [URL-Neuschreibungen](url-rewrite.md).

## Routing-Funktion auswählen

Verwenden Sie die folgende Anleitung, um die Funktion zu ermitteln, die Ihrer Anforderung entspricht:

| Anforderung | Empfohlene Funktion |
| --- | --- |
| Senden einer bestimmten Abfrage von der Standardsuche [!DNL Adobe Commerce] eine Seite | Konfigurieren Sie einen Suchbegriff in [Suchbegriffe verwalten](../catalog/search-terms.md), sofern unterstützt. |
| Ändern des Produkt-Rankings oder der Sichtbarkeit in Suchergebnissen | Verwenden Sie [!DNL Live Search] [Synonyme](https://experienceleague.adobe.com/en/docs/commerce/live-search/live-search-admin/synonyms/synonyms) oder [Merchandising-Regeln](https://experienceleague.adobe.com/en/docs/commerce/live-search/live-search-admin/rules/rules-add). |
| Alte Produkt-, Kategorie- oder CMS-URL umleiten | Verwenden Sie das Commerce [URL Rewrite](url-rewrite.md)-Tool, wenn es auf Ihre Bereitstellung anwendbar ist. |
| [!DNL Edge Delivery Services] umleiten | Storefront- oder CDN-Routing verwenden. |
| Alte URLs nach einer Storefront-Migration beibehalten | Erstellen und testen Sie eine Umleitungszuordnung von einer veralteten zu einer neuen URL. |

## Standardmäßige Commerce-Suche

Mit der standardmäßigen Katalogsuche können Sie einen Suchbegriff konfigurieren, um eine Inhaltsseite, Kategorieseite, Produktseite oder externe Seite zu öffnen, auf der/der diese Funktion von der Bereitstellung unterstützt wird. Verwenden Sie sie, wenn eine vom Käufer eingegebene Abfrage, z. B. `gift cards` oder `returns`, eine Kampagne oder eine Informationsseite öffnen muss.

Informationen zum Erstellen oder Aktualisieren dieses Umleitungstyps finden Sie unter [Verwalten von Suchbegriffen](../catalog/search-terms.md). Die Suchbegriffkonfiguration ist vom URL-Rewrite-Tool getrennt, da der Trigger die Abfrage des Käufers ist, keine vorhandene URL.

>[!NOTE]
>
>Vergewissern Sie sich, dass die Storefront die standardmäßige Katalogsuche verwendet und native Suchbegriff-Umleitungen unterstützt. Das Verhalten und die verfügbare Konfiguration können für [!DNL Live Search], [!DNL Adobe Commerce as a Cloud Service] oder eine Headless-Storefront unterschiedlich sein.

## URL-Umleitungen und -Neuschreibungen

Verwenden Sie eine URL-Umschreibung, wenn die Quelle eine vorhandene URL ist und kein vom Käufer eingegebener Suchbegriff. Häufige Beispiele sind die Umleitungen:

* Eine alte Produkt-URL zu einer neuen Produkt-URL.

* Eine eingestellte Kategorie-URL zu einer Ersatz-Kategorie-URL.

* Eine veraltete CMS-Seiten-URL zu einer neuen Inhaltsseiten-URL.

Für Bereitstellungen, die das URL Rewrite-Tool unterstützen, gehen Sie zu **[!UICONTROL Marketing]** > **[!UICONTROL SEO & Search]** > **[!UICONTROL URL Rewrites]** , um die Umleitung zu erstellen. Eine schrittweise Anleitung finden Sie unter [URL-Neuschreibungen](url-rewrite.md).

>[!NOTE]
>
>Das Thema [URL-Neuschreibungen](url-rewrite.md) gilt nur für PaaS. Verwenden Sie für [!DNL Adobe Commerce as a Cloud Service] oder eine [!DNL Edge Delivery Services] Storefront stattdessen die Routing-Anleitung für diese Storefront.

## Live Search

[!DNL Live Search] ersetzt das standardmäßige Storefront-Sucherlebnis und bietet Funktionen wie Synonyme, Facetten und Merchandising-Regeln.

Verwenden Sie [!DNL Live Search], wenn Sie die Suchrelevanz, das Produkt-Ranking oder die Sichtbarkeit des Produkts ändern müssen. Verwenden Sie Synonyme, wenn verschiedene Wörter ähnliche Produkte zurückgeben sollen. Verwenden Sie Merchandising-Regeln, wenn Produkte geboostert, beerdigt oder anders eingestuft werden müssen.

[!DNL Live Search] Suchverhalten sollte nicht als Dropdown-Ersatz für jede native Commerce-Suchbegriffkonfiguration behandelt werden. Wenn eine Abfrage zu einer Inhalts- oder Kampagnenseite navigieren muss, implementieren Sie die Umleitung in der Storefront oder Edge-Routing-Ebene, die die Anfrage erhält. Weitere Informationen finden Sie in der [[!DNL Live Search] Dokumentation](https://experienceleague.adobe.com/en/docs/commerce/live-search/overview).

## Edge-Bereitstellungsdienste

Für eine Storefront mit [!DNL Edge Delivery Services] verwalten Sie Umleitungen in der Storefront- oder Edge-Routing-Ebene. Gehen Sie nicht davon aus, dass [!DNL Adobe Commerce] Admin-URL jede Anfrage neu schreibt.

Wenn Sie das Erstellen von Dokumenten verwenden, verwalten Sie Umleitungszuordnungen in der Umleitungskonfiguration der Site. Verwenden Sie für Umleitungen, die ausgeführt werden müssen, bevor eine Anfrage die Quelle erreicht, die entsprechende CDN- oder Edge-Konfiguration. Weitere Informationen zu SEO finden Sie unter [SEO-Richtlinien für Commerce Storefront](https://experienceleague.adobe.com/developer/commerce/storefront/setup/seo/indexing/).

## Aus Luma migrieren

Umleitungsmigration als Teil der Storefront-Migration behandeln. Bewahren Sie die Journey- und SEO-Absichten Ihrer Kunden auf und implementieren Sie dann erneut das Routing für die Ziel-Storefront.

Vor dem Wechsel des Traffics zur neuen Storefront:

1. Exportieren und inventarisieren Sie vorhandene Luma-URLs und Suchbegriff-Landingpages.

1. Klassifizieren Sie jedes Element als Suchbegriff-Umleitung, URL-Umleitung oder Merchandising-Regel.

1. Ordnen Sie jede veraltete URL ihrem neuen Storefront-Pfad zu.

1. Implementieren Sie jede Weiterleitung auf der Ebene, die die Anfrage erhält.

1. Teststatus-Codes, Abfrageparameter, kanonische URLs, Gebietsschema-Pfade und Umleitungsschleifen.

1. Überwachen Sie Protokolle und Analysen nach dem Start auf nicht aufgelöste Legacy-URLs.

## Fehlerbehebung bei Weiterleitungen

Verwenden Sie die folgenden Prüfungen, wenn sich eine Umleitung nicht wie erwartet über [!DNL Adobe Commerce] Such-, Storefront-Routing- und Store-Ansichten hinweg verhält.

| Problem | Was zu überprüfen ist |
| --- | --- |
| Ein Suchbegriff wird nicht umgeleitet | Vergewissern Sie sich, dass die Storefront die standardmäßige Katalogsuche verwendet, die Suchabfrage mit dem konfigurierten Begriff übereinstimmt und der Suchbegriff der richtigen Store-Ansicht zugewiesen wird. Wenn [!DNL Live Search] aktiviert ist, stellen Sie sicher, dass die Umleitung in der Storefront oder Edge-Ebene implementiert ist. |
| Eine Umleitung funktioniert in Luma, aber nicht in Edge Delivery Services | Vergewissern Sie sich, dass die Umleitung in der [!DNL Edge Delivery Services] Storefront- oder CDN-Routing-Ebene konfiguriert ist. [!DNL Adobe Commerce] Admin-URL-Neuschreibungen erhalten die Anfrage möglicherweise nicht. |
| Live Search gibt Ergebnisse zurück, anstatt umzuleiten | Verwenden Sie [!DNL Live Search] Regeln für Produkt-Ranking und Sichtbarkeit. Um zu einer Inhalts- oder Kampagnenseite zu navigieren, konfigurieren Sie die Umleitung in der Storefront- oder Edge-Ebene. |
| Eine Umleitung funktioniert in einer Store-Ansicht, aber nicht in einer anderen | Überprüfen Sie die Store-Ansicht, die dem Suchbegriff oder der URL-Regel zugewiesen ist. Testen Sie den vollständigen Gebietsschemapfad und die Abfrage in jeder betroffenen Store-Ansicht. |

## Weitere Hilfe zu diesem Thema

* [SEO - Überblick und Best Practices](seo-overview.md)

* [Was ist die Storefront?](../getting-started/storefront.md)

* [Verwalten von Suchbegriffen](../catalog/search-terms.md)

* [URL-Neuschreibungen](url-rewrite.md)
