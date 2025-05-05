---
title: '[!UICONTROL Sales Channels] &gt; [!UICONTROL Global Settings]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Sales Channels] &gt; [!UICONTROL Global Settings] des Commerce Admin-Bereichs.
exl-id: 28a5ef4b-265e-457a-9480-96763785b5fd
feature: Configuration, Sales Channels
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---

# [!UICONTROL Sales Channels] > [!UICONTROL Global Settings]

{{config}}

Diese Einstellungen sind verfügbar, wenn [[!DNL Amazon Sales Channel]](https://experienceleague.adobe.com/docs/commerce-channels/amazon/getting-started/install.html?lang=de) installiert ist.

![Sales Channel-Einstellungen](./assets/config-sales-channel-global-settings.png)<!-- zoom -->

| Feld | [Umfang](../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|-----|---------|------|
| [!UICONTROL Clear Log History] | Global | Optionen: <br/><br/>**`Once Daily`**: Wählen Sie diese Option aus, um den Aktivitätsverlauf Ihres Stores einmal täglich zu löschen.<br/><br/>**`Once Weekly`**: Wählen Sie diese Option aus, um den Aktivitätsverlauf Ihres Stores einmal wöchentlich zu löschen.<br/><br/>**`Once Monthly`**: (Standard) Wählen Sie diese Option aus, um den Aktivitätsverlauf Ihres Stores einmal monatlich zu löschen. |
| [!UICONTROL Background Tasks (CRON) Source] | Global | Wählen Sie `Magento CRON` aus, um anzugeben, dass der [!DNL Amazon Sales Channel] Ihre Commerce-Cron-Einstellungen verwendet, um Kommunikations- und Datensynchronisierungsintervalle mit Amazon Seller Central zu bestimmen. |
| [!UICONTROL Enable Debug Logging] | Global | Wählen Sie `Enabled` aus, um zusätzliche Synchronisierungsdaten zu erfassen, wenn eine Fehlerbehebung erforderlich ist.<br/><br/>Diese Option ist standardmäßig deaktiviert und sollte nur aktiviert werden, wenn sie zur Fehlerbehebung benötigt wird, da die kontinuierliche Protokollierung die Leistung beeinträchtigt. Wenn diese Option für die Fehlerbehebung aktiviert ist, sollte sie nach Abschluss deaktiviert werden.<br/><br/>**_Hinweis _**: Die Amazon Sales Channel-Protokollierung wird in die `/var/log/channel_amazon.log`-Datei geschrieben und kann im &quot;[&quot; angezeigt ](../systems/developer-tools.md#operation-modes). |
| [!UICONTROL Read-Only Mode] | Global | Wählen Sie `Enabled` aus, um alle ausgehenden zustandsändernden API-Anfragen zu blockieren. Potenzielle Änderungen werden gespeichert, aber erst gesendet, wenn der schreibgeschützte Modus deaktiviert ist. Um die Datenübertragungen erneut zu starten, wählen Sie `Disabled` aus.<br/><br/>Wenn eine Datenbank zu einer neuen Kopie der Instanz migriert wird (erkannt, wenn sich die URL eines Stores in der Konfiguration ändert), wird der schreibgeschützte Modus automatisch aktiviert.<br/><br/>Dies ist für die Verwendung auf Kopien der Produktionsinstanz wie _Staging_ oder _QA) vorgesehen_ sollte nicht auf der Produktionsinstanz verwendet werden.<br/><br/>**_Hinweis _**: Der Konfigurations-Cache muss gelöscht werden, damit er aktiviert [!UICONTROL Read-Only Mode]. |

{style="table-layout:auto"}
