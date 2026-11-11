---
title: '[!UICONTROL Services] > ACO - Schlüssel mit eingeschränktem Zugriff'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Services] > [!UICONTROL ACO Restricted Access Keys] des Commerce Admin.
feature: Configuration, Security
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
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
source-git-commit: df30ce0e482be65523f346d578be481b3ff893c8
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 3%
---
# [!UICONTROL Services] > [!UICONTROL ACO Restricted Access Keys]

Verwenden Sie diese Einstellung, um den Standardablaufzeitraum zu steuern, den die [!DNL Adobe Commerce Optimizer Connector for B2B] für eingeschränkte Zugriffsschlüssel anwendet, die sie für freigegebene B2B-Katalogansichten bereitstellt. Informationen zum Erstellen, Zuweisen und Löschen dieser Schlüssel finden Sie unter [Verwaltung von eingeschränkten Zugriffsschlüsseln](../../systems/restricted-access-keys.md).

>[!NOTE]
>
>Diese Seite gilt für den Connector. Instanzen, die mit dem Composable Catalog Data Model (CCDM) bereitgestellt werden, synchronisieren Daten nativ und verwenden den Connector nicht. Siehe [Merchandising-Services mit CCDM](/help/optimizer/overview.md).

{{config}}

## [!UICONTROL Provisioning]

![Bereitstellung](./assets/optimizer-restricted-access-key-config.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
| --- | --- | --- |
| [!UICONTROL Default key expiry (days)] | Global | Gültigkeitszeitraum für neu bereitgestellte eingeschränkte Zugriffsschlüssel. [!DNL Adobe Commerce Optimizer] erfordert für jeden Schlüssel ein Ablaufdatum von mindestens einer Minute in der Zukunft und schließt abgelaufene Schlüssel aus Gateway-Lesevorgängen aus, sodass immer ein Wert von mindestens einem Tag angewendet wird. Standardwert: `36500` |

{style="table-layout:auto"}

>[!NOTE]
>
>Der Standardablauf ist auf einen langen Ablaufzeitraum festgelegt, da die automatische Schlüsselrotation noch nicht verfügbar ist. Siehe [Auswahl und Drehung von Tasten](../../systems/restricted-access-keys.md#key-selection-and-rotation).

>[!MORELIKETHIS]
>
> - [ACO-Katalogansicht](./aco-catalog-view.md) - Konfigurieren von Storefront-Zugriffstoken für Katalogansichten
> - [Verwaltung von eingeschränkten Zugriffsschlüsseln](../../systems/restricted-access-keys.md) — Erstellen, Zuweisen und Löschen von eingeschränkten Zugriffsschlüsseln
> - [Überwachung des Synchronisierungsstatus der Katalogansicht](../../systems/catalog-view-sync-status.md) — Überwacht Schlüssel, die bald ablaufen
