---
title: Voraussetzungen für die KI-Produkterkennung
description: Überprüfen Sie die Anforderungen für die Kataloganreicherung und die PDP-Anreicherung und installieren Sie die gemeinsame Anreicherungserweiterung in Adobe Commerce auf der Cloud-Infrastruktur oder lokal.
role: Admin, Developer
source-git-commit: 9e234eb68fe34171d9e5cf95e8cdab5c31825492
workflow-type: tm+mt
source-wordcount: '505'
ht-degree: 0%
---
# Voraussetzungen

Bevor Sie die Kataloganreicherung oder die PDP-Anreicherung verwenden, bestätigen Sie die Anforderungen für jede Bereitstellung und schließen Sie dann die Einrichtung für Ihre Commerce-Plattform ab.

## Anforderungen für alle Bereitstellungen {#all-deployments}

| Anforderung | Gilt für | Details |
| --- | --- | --- |
| Optimieren bei Edge | PDP-Anreicherung | Erforderlich. Optimieren bei Edge stellt die angereicherten Produktdaten für KI-Agenten bereit. Siehe das [Optimieren in Edge](https://experienceleague.adobe.com/en/docs/brand-visibility/using/resources/optimize-at-edge/fastly-byocdn). |
| Protokollweiterleitung | Beide Workflows | Optional. Aktiviert Anreicherungsempfehlungen basierend auf agentem Traffic. Ohne sie können Sie Produkte oder Produktseiten weiterhin manuell auswählen. Weitere Informationen finden [ im Handbuch zur ](https://experienceleague.adobe.com/en/docs/brand-visibility/using/log-forwarding/log-forwarding-overview). |
| Crawlbare Storefront | Kataloganreicherung | Erforderlich für crawlen-basierte Empfehlungen. LLM-orientierte und agentische Bots müssen in der Lage sein, auf Ihre Produktseiten zuzugreifen. |
| [!DNL Adobe Admin Console] | Kataloganreicherung | Erforderlich. Während des Setups prüft [!DNL Adobe Commerce], ob Ihr Unternehmen den GenAI-Fahrer angemeldet hat oder sich gegen die zugrunde liegenden KI-Services entschieden hat. |

<!--
TBD (SME): The Optimize at Edge guide is a Brand Visibility reference, not a Commerce setup guide. Add Commerce-specific Optimize at Edge setup instructions (this might be automated by GA).
TBD (SME): Confirm whether the Admin Console and GenAI rider check also applies to PDP enrichment.
-->

## Einrichten der Commerce-Plattform {#set-up}

>[!BEGINTABS]

>[!TAB Commerce auf Cloud-Infrastruktur oder lokal]

Für [!DNL Adobe Commerce] in der Cloud-Infrastruktur oder lokal installieren Sie die gemeinsame Anreicherungserweiterung, die sowohl die Kataloganreicherung als auch die PDP-Anreicherung ermöglicht.

**Bevor Sie beginnen:**

- [!DNL Adobe Commerce] 2.4.7 oder höher in PHP 8.3 oder höher. Siehe [ Versionshinweise ](release-notes.md).
- Eine [!DNL Adobe IMS] Organisation. Wenn Ihr Unternehmen über keine verfügt, lesen Sie den Abschnitt [Übersicht über die Adobe IMS-Integration](https://experienceleague.adobe.com/en/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview). Die Kataloganreicherung verwendet das IMS-Zugriffstoken des angemeldeten Admin-Benutzers. Wenn Sie sich nur mit einem Commerce-Benutzernamen und -Kennwort anmelden, wird dieses Token nicht bereitgestellt.
- Befehlszeilenzugriff auf den Commerce-Anwendungsserver und Berechtigung zum Herunterladen von Paketen aus `repo.magento.com`.

**Installieren und Überprüfen:**

1. Wenn weder [!DNL Live Search] noch [!DNL Product Recommendations] aktiviert ist, fügen Sie [!DNL Catalog Service] aus Ihrem Commerce-Projektverzeichnis hinzu:

   ```bash
   composer require magento/catalog-service --no-update
   composer update magento/catalog-service
   ```

   [!DNL Catalog Service] wird automatisch mit [!DNL Live Search] und [!DNL Product Recommendations] installiert. Überspringen Sie diesen Schritt, wenn einer der Services aktiviert ist.

1. Wenn er noch nicht für einen anderen Commerce-Service konfiguriert ist, konfigurieren Sie den [Commerce Services Connector](https://experienceleague.adobe.com/en/docs/commerce/user-guides/integration-services/saas) mit API-Schlüsseln und einem SaaS-Datenspeicher.

1. Fügen Sie die gemeinsame Anreicherungserweiterung hinzu:

   ```bash
   composer require magento/module-catalog-enrichment --no-update
   composer update magento/module-catalog-enrichment
   ```

1. Bereitstellen der Änderungen:

   - **Cloud-Infrastruktur:** Übernehmen Sie die Änderungen und übertragen Sie sie auf `composer.json` und `composer.lock`.
   - **On-Premise:** Aktualisieren Sie die Anwendung und löschen Sie den Cache:

     ```bash
     bin/magento setup:upgrade
     bin/magento cache:clean
     ```

1. Wechseln Sie in Admin zu **[!UICONTROL System]** > **[!UICONTROL Data Transfer]** > **[!UICONTROL Data Feed Sync Status]** und bestätigen Sie, dass Commerce Katalogdaten exportiert.

   Die Anzahl der erfolgreich gesendeten Produktdatensätze sollte mit den Quelldatensätzen übereinstimmen, ohne dass Fehler auftreten oder die Übermittlungen ausstehen. Überprüfen Sie bei fehlgeschlagenen Datensätzen die Fehlerdetails, beheben Sie das Problem und planen Sie eine Neusynchronisierung für die betroffenen Datensätze.

1. Navigieren Sie zu **[!UICONTROL System]** > **[!UICONTROL Data Transfer]** > **[!UICONTROL Data Management Dashboard]** und vergewissern Sie sich, dass die erwarteten Katalogdaten in [!DNL Catalog Service] verfügbar sind.

Statusdetails und Fehlerbehebung finden Sie unter [Überwachen des Daten-Feed-Status](/help/systems/data-feed-sync-status.md#monitor-data-feed-status).

>[!TAB Adobe Commerce as a Cloud Service]

[!DNL Adobe Commerce as a Cloud Service] werden die Installation von [!DNL Catalog Service], die Kataloganreicherung und die PDP-Anreicherung während der Kontobereitstellung für Sie durchgeführt.

Füllen Sie die [Anforderungen für alle Bereitstellungen](#all-deployments) aus, die für die Workflows gelten, die Sie verwenden möchten.

<!-- TBD (SME): Confirm whether merchants on Adobe Commerce as a Cloud Service should verify catalog data on the Data Management Dashboard, and whether the IMS and Admin Console requirements apply. -->

>[!ENDTABS]

## Nächster Schritt {#next-step}

[Anreicherungseinstellungen konfigurieren](settings.md) um Ihre Commerce-Instanz mit der KI-Produkterkennung zu verbinden.
