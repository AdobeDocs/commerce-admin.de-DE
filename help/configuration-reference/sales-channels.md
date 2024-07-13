---
title: '[!UICONTROL Sales Channels] &gt; [!UICONTROL Global Settings]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Sales Channels] &gt; [!UICONTROL Global Settings] des Commerce-Administrators.
exl-id: 28a5ef4b-265e-457a-9480-96763785b5fd
feature: Configuration, Sales Channels
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---

# [!UICONTROL Sales Channels] > [!UICONTROL Global Settings]

{{config}}

Diese Einstellungen sind verfügbar, wenn [[!DNL Amazon Sales Channel]](https://experienceleague.adobe.com/docs/commerce-channels/amazon/getting-started/install.html) installiert ist.

![Sales Channel Settings](./assets/config-sales-channel-global-settings.png)<!-- zoom -->

| Feld | [Umfang](../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|-----|---------|------|
| [!UICONTROL Clear Log History] | Global | Optionen:<br/><br/>**`Once Daily`**: Wählen Sie diese Option aus, um den Aktivitätsverlauf Ihres Stores einmal täglich zu löschen.<br/><br/>**`Once Weekly`**: Wählen Sie diese Option aus, um den Aktivitätsverlauf Ihres Stores einmal wöchentlich zu löschen.<br/><br/>**`Once Monthly`**: (Standard) Wählen Sie diese Option aus, um den Aktivitätsverlauf Ihres Stores einmal monatlich zu löschen. |
| [!UICONTROL Background Tasks (CRON) Source] | Global | Wählen Sie `Magento CRON` aus, um anzugeben, dass [!DNL Amazon Sales Channel] Ihre Commerce-Cron-Einstellungen verwendet, um die Kommunikations- und Datensynchronisierungsintervalle mit Amazon Seller Central zu bestimmen. |
| [!UICONTROL Enable Debug Logging] | Global | Wählen Sie `Enabled` aus, um bei der erforderlichen Fehlerbehebung zusätzliche Synchronisierungsdaten zu erfassen.<br/><br/>Diese Option ist standardmäßig deaktiviert und sollte nur bei Bedarf zur Fehlerbehebung aktiviert werden, da sich die kontinuierliche Protokollierung negativ auf die Leistung auswirkt. Wenn diese Option für die Fehlerbehebung aktiviert ist, sollte sie nach Abschluss des Vorgangs deaktiviert werden.<br/><br/>**_Hinweis _**: Die Amazon-Sales Channel-Protokollierung wird in die Datei `/var/log/channel_amazon.log` geschrieben und kann im [Entwicklermodus](../systems/developer-tools.md#operation-modes) angezeigt werden. |
| [!UICONTROL Read-Only Mode] | Global | Wählen Sie &quot;`Enabled`&quot;, um alle ausgehenden, sich Statusänderungen ergebenden API-Anfragen zu blockieren. Potenzielle Änderungen werden gespeichert, aber erst gesendet, wenn der schreibgeschützte Modus deaktiviert ist. Um die Datenübertragungen erneut zu starten, wählen Sie `Disabled` aus.<br/><br/>Wenn eine Datenbank auf eine neue Kopie der Instanz migriert wird (erkannt, wenn sich die URL eines Stores in der Konfiguration ändert), wird der schreibgeschützte Modus automatisch aktiviert.<br/><br/>Dies ist für die Verwendung auf Kopien der Produktionsinstanz wie _Staging_ oder _QA_ vorgesehen und sollte nicht in der Produktionsinstanz verwendet werden.<br/><br/>**_Hinweis _**: Der Konfigurationscache muss für [!UICONTROL Read-Only Mode] gelöscht werden, damit er aktiviert werden kann. |

{style="table-layout:auto"}
