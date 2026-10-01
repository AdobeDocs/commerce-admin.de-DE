---
title: '[!UICONTROL Services] > ACO-Katalogansicht'
description: Überprüfen und aktualisieren Sie die Adobe Commerce Optimizer-Konfigurationseinstellungen auf der Seite [!UICONTROL Services] > [!UICONTROL ACO Catalog View] des Commerce-Administrators.
feature: Configuration, Security
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/de/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: b32c28afffe75b3f684f0fef81bd61e9cdcb485a
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 3%
---
# [!UICONTROL Services] > [!UICONTROL ACO Catalog View]

Verwenden Sie diese Einstellungen, um die von der [!DNL Adobe Commerce Optimizer Connector for B2B] ausgegebenen Zugriffstoken zu steuern. Storefronts verwenden diese Token, um sich bei privaten Commerce Optimizer-Katalogansichten zu authentifizieren, die mit Daten gefüllt sind, die aus benutzerdefinierten, im Administrator konfigurierten freigegebenen Katalogen synchronisiert wurden.

{{config}}

![Adobe Commerce Admin zeigt die Einstellungen der ACO-Katalogansicht für Zugriffstoken an, wobei die TTL- und Token-Ausgabe für 3.600 Sekunden aktiviert ist.](./assets/aco-catalog-view-access-token-config.png)<!-- zoom -->

## [!UICONTROL Access Token Configuration]

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
| --- | --- | --- |
| [!UICONTROL Token TTL (seconds)] | Global | Anzahl der Sekunden, die ein Zugriffs-Token gültig bleibt, nachdem es generiert wurde. Diese Einstellung ist im Standardbereich schreibgeschützt. Werte, die im Website- oder Store-Ansichtsbereich konfiguriert wurden, werden ignoriert. Standardwert ist: 3600 Sekunden. |
| [!UICONTROL Issue Access Tokens] | Shop-Ansicht | Steuert, ob die Storefront ein Zugriffstoken für eine Katalogansicht erhalten kann. Bei Festlegung auf `No` gibt `Company.catalogViewContext` die Katalogansichts-ID, aber kein Zugriffstoken zurück, sodass sich Storefronts nicht authentifizieren können, um aus [!DNL Adobe Commerce Optimizer] von Adobe Commerce synchronisierten privaten Katalogansichten zu lesen. |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
> - [ACO Catalog View Sync](./aco-catalog-view-sync.md) - Konfigurieren Sie, wie Katalogansichten in [!DNL Adobe Commerce Optimizer] synchronisiert werden
> - [Überwachung des Synchronisationsstatus der Katalogansicht](../../systems/catalog-view-sync-status.md) — Überwachen des Synchronisationszustands und Abgleichen von Drift
