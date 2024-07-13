---
title: '[!UICONTROL General] &gt; [!UICONTROL New Relic Reporting]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL General] &gt; [!UICONTROL New Relic Reporting] des Commerce-Administrators.
exl-id: d6bf4810-81a3-420d-abc9-9b87c1e92551
feature: Configuration, System, Reporting
source-git-commit: 1aec5c618d1f3f7f083523956d2aee62b777faca
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL New Relic Reporting]

{{config}}

>[!NOTE]
>Diese Konfigurationsoptionen gelten nicht für Adobe Commerce on Cloud Infrastructure.
>
>Wenn Sie mit dem Pro-Plan arbeiten, ist New Relic bereits [vorkonfiguriert und standardmäßig aktiviert](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html). Wenn Sie den Startplan verwenden, müssen Sie die [New Relic-Konfigurationsschritte](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/account-management.html#configure-new-relic-for-starter-environment) ausführen, die Teil des Einrichtungsprozesses sind.

## [!UICONTROL General]

![Allgemein](./assets/new-relic-reporting-general.png)<!-- zoom -->

<!-- [General](https://docs.magento.com/user-guide/reports/new-relic-reporting.html) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable New Relic Integration] | Store-Ansicht | Bestimmt, ob Ihr Store mit [!DNL New Relic] -Berichten verwendet werden kann. Optionen: `Yes` / `No` |
| [!UICONTROL New Relic API URL] | Store-Ansicht | Die URL, unter der New Relic-APIs bereitgestellt werden. Beispiel: `https://api.newrelic.com/deployments.xml` |
| Insights-API-URL | Store-Ansicht | Die URL, unter der Insights-APIs bereitgestellt werden. Verwenden Sie das Prozentsymbol (%), um Ihre Konto-ID darzustellen. Beispiel: `https://insights-collector.newrelic.com/v1/accounts/%s/events` |
| [!UICONTROL New Relic Account ID] | Store-Ansicht | Die Ihrem [!DNL New Relic] -Konto zugewiesene Konto-ID. |
| [!UICONTROL New Relic Application ID] | Store-Ansicht | Die Anwendungs-ID, die Ihrem [!DNL New Relic] -Konto für die Commerce-Integration zugewiesen ist. |
| [!UICONTROL New Relic API Key] | Store-Ansicht | Der Schlüssel, der Ihnen für den Zugriff auf die [!DNL New Relic] -API zugewiesen ist. |
| [!UICONTROL Insights API Key] | Store-Ansicht | Der Schlüssel, der Ihnen für den Zugriff auf Insights zugewiesen ist. |
| [!UICONTROL New Relic Application Name] | Store-Ansicht | Der Name, den Sie Ihrer [!DNL New Relic] -Integration zugewiesen haben. |
| [!UICONTROL Send Adminhtml and Frontend as Separate Apps] | Store-Ansicht | Eine Option zum Senden der für die Storefront und Admin erfassten Berichtsdaten als separate Apps an New Relic. Für diese Option muss ein Name für die [!UICONTROL New Relic Application Name] eingegeben werden. Die Funktion hängt den App-Namen mit einem Unterstrich an die erfassten App-Daten an. Beispiel: `MyStore_Adminhtml`, `MyStore_frontend` |

{style="table-layout:auto"}

## [!UICONTROL Cron]

![Cron](./assets/new-relic-reporting-cron.png)<!-- zoom -->

<!-- Cron](https://docs.magento.com/user-guide/system/cron.html) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable Cron] | Store-Ansicht | Bestimmt, ob [!DNL New Relic] -Berichte planmäßig mit [Cron](../../systems/cron.md) ausgeführt werden können. Optionen: `Yes` / `No` |

{style="table-layout:auto"}
