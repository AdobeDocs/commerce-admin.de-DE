---
title: '[!UICONTROL General] &gt; [!UICONTROL New Relic Reporting]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL General] &gt; [!UICONTROL New Relic Reporting] des Commerce Admin-Bereichs.
exl-id: d6bf4810-81a3-420d-abc9-9b87c1e92551
feature: Configuration, System, Reporting
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL New Relic Reporting]

{{config}}

>[!NOTE]
>Diese Konfigurationsoptionen gelten nicht für Adobe Commerce in der Cloud-Infrastruktur.
>
>Wenn Sie den Pro-Plan verwenden, ist New Relic bereits [vorkonfiguriert und standardmäßig aktiviert](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html). Wenn Sie den Starter-Plan verwenden, müssen Sie die [New Relic-Konfigurationsschritte](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/account-management.html#configure-new-relic-for-starter-environment) ausführen, die Teil des Einrichtungsprozesses sind.

## [!UICONTROL General]

![Allgemein](./assets/new-relic-reporting-general.png)<!-- zoom -->

<!-- [General](https://experienceleague.adobe.com/en/docs/commerce-admin/start/reporting/new-relic-reporting) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable New Relic Integration] | Shop-Ansicht | Legt fest, ob Ihr Store mit [!DNL New Relic] Reporting verwendet werden kann. Optionen: `Yes` / `No` |
| [!UICONTROL New Relic API URL] | Shop-Ansicht | Die URL, unter der New Relic-APIs bereitgestellt werden. Beispiel: `https://api.newrelic.com/deployments.xml` |
| Insights-API-URL | Shop-Ansicht | Die URL, unter der Insights-APIs bereitgestellt werden. Verwenden Sie das Prozentsymbol (%), um Ihre Konto-ID darzustellen. Beispiel: `https://insights-collector.newrelic.com/v1/accounts/%s/events` |
| [!UICONTROL New Relic Account ID] | Shop-Ansicht | Die Ihrem [!DNL New Relic] Konto zugewiesene Konto-ID. |
| [!UICONTROL New Relic Application ID] | Shop-Ansicht | Die Anwendungs-ID, die Ihrem [!DNL New Relic]-Konto für die Commerce-Integration zugewiesen ist. |
| [!UICONTROL New Relic API Key] | Shop-Ansicht | Der Schlüssel, der Ihnen für den Zugriff auf die [!DNL New Relic]-API zugewiesen ist. |
| [!UICONTROL Insights API Key] | Shop-Ansicht | Der Schlüssel, der Ihnen für den Zugriff auf Insights zugewiesen ist. |
| [!UICONTROL New Relic Application Name] | Shop-Ansicht | Der Name, den Sie Ihrer [!DNL New Relic]-Integration zugewiesen haben. |
| [!UICONTROL Send Adminhtml and Frontend as Separate Apps] | Shop-Ansicht | Eine Option zum Senden von Berichtsdaten, die für die Storefront und Admin als separate Apps erfasst wurden, an New Relic. Für diese Option ist die Eingabe eines Namens für die [!UICONTROL New Relic Application Name] erforderlich. Die Funktion hängt den App-Namen mit einem Unterstrich an die erfassten App-Daten an. Beispiel: `MyStore_Adminhtml`, `MyStore_frontend` |

{style="table-layout:auto"}

## [!UICONTROL Cron]

![Cron](./assets/new-relic-reporting-cron.png)<!-- zoom -->

<!-- Cron](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/tools/cron) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable Cron] | Shop-Ansicht | Legt fest, ob [!DNL New Relic] Berichte planmäßig mit [Cron](../../systems/cron.md) ausgeführt werden können Optionen: `Yes` / `No` |

{style="table-layout:auto"}
