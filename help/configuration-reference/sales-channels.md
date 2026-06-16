---
title: '[!UICONTROL Sales Channels] > [!UICONTROL Global Settings]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Sales Channels] > [!UICONTROL Global Settings] des Commerce Admin.
exl-id: 28a5ef4b-265e-457a-9480-96763785b5fd
feature: Configuration, Sales Channels
TQID: https://experienceleague.adobe.com/jnjAspEdJbx3unjmoqgH12JEiLz4ThbgFGeFOArOonU
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 225
ht-degree: 0%

---

# [!UICONTROL Sales Channels] > [!UICONTROL Global Settings]

{{config}}

Diese Einstellungen sind verfügbar, wenn [[!DNL Amazon Sales Channel]](https://experienceleague.adobe.com/docs/commerce-channels/amazon/getting-started/install.html?lang=de) installiert ist.

![Sales Channel-Einstellungen](./assets/config-sales-channel-global-settings.png)<!-- zoom -->

| Feld | [Umfang](../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|-----|---------|------|
| [!UICONTROL Clear Log History] | Global | Optionen: <br/><br/>**`Once Daily`**: Wählen Sie diese Option aus, um den Aktivitätsverlauf Ihres Geschäfts einmal täglich zu löschen.<br/><br/>**`Once Weekly`**: Wählen Sie diese Option aus, um den Aktivitätsverlauf Ihres Geschäfts einmal wöchentlich zu löschen.<br/><br/>**`Once Monthly`**: (Standard) Wählen Sie diese Option aus, um den Aktivitätsverlauf Ihres Geschäfts einmal monatlich zu löschen. |
| [!UICONTROL Background Tasks (CRON) Source] | Global | Wählen Sie `Magento CRON` aus, um anzugeben, dass der [!DNL Amazon Sales Channel] Ihre Commerce-Cron-Einstellungen verwendet, um Kommunikations- und Datensynchronisierungsintervalle mit Amazon Seller Central zu bestimmen. |
| [!UICONTROL Enable Debug Logging] | Global | Wählen Sie `Enabled` aus, um zusätzliche Synchronisierungsdaten zu erfassen, wenn eine Fehlerbehebung erforderlich ist.<br/><br/>Diese Option ist standardmäßig deaktiviert und sollte nur aktiviert werden, wenn sie zur Fehlerbehebung benötigt wird, da die kontinuierliche Protokollierung die Leistung beeinträchtigt. Wenn diese Option für die Fehlerbehebung aktiviert ist, sollte sie nach Abschluss deaktiviert werden. |
| [!UICONTROL Read-Only Mode] | Global | Wählen Sie `Enabled` aus, um alle ausgehenden zustandsändernden API-Anfragen zu blockieren. Potenzielle Änderungen werden gespeichert, aber erst gesendet, wenn der schreibgeschützte Modus deaktiviert ist. Um die Datenübertragungen erneut zu starten, wählen Sie `Disabled` aus<br/><br/>Wenn eine Datenbank zu einer neuen Kopie der Instanz migriert wird (erkannt, wenn sich die URL eines Stores in der Konfiguration ändert), wird der schreibgeschützte Modus automatisch aktiviert.<br/><br/>Dies wurde für die Verwendung auf Kopien der Produktionsinstanz entwickelt, z. B _Staging_ oder _QA_, und sollte nicht auf der Produktionsinstanz verwendet werden.<br/><br/>**_Hinweis _**: Der Konfigurations-Cache muss für [!UICONTROL Read-Only Mode] zur Aktivierung gelöscht werden. |

{style="table-layout:auto"}
