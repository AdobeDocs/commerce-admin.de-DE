---
title: '[!UICONTROL Services] > ACO-Katalogansicht synchronisieren'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Services] > [!UICONTROL ACO Catalog View Sync] des Commerce Admin.
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
source-git-commit: 9ec73be87dd329dc04e7b133885fcc156f4ffcb6
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 3%
---
# [!UICONTROL Services] > [!UICONTROL ACO Catalog View Sync]

Verwenden Sie diese Einstellungen, um zu steuern, wie die [!DNL Adobe Commerce Optimizer Connector for B2B] freigegebene B2B-Katalogkonfigurationen - Katalogansicht, Richtlinie, Preisbuch und Schlüssel - in [!DNL Adobe Commerce Optimizer] synchronisiert und wie Konfigurationsunterschiede zwischen den beiden Systemen aufgelöst werden. Informationen [&#x200B; Überwachung der Ergebnisse dieser Einstellungen finden &#x200B;](../../systems/catalog-view-sync-status.md) unter „Catalog View Sync Status Monitoring“.

{{config}}

## [!UICONTROL Deletion]

![Löschen](./assets/aco-catalog-view-sync-configuration.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
| --- | --- | --- |
| [!UICONTROL Deletion Grace Period (days)] | Global | Aufbewahrungszeitraum für freigegebene Katalogdaten. Gibt die Anzahl der Tage an, die die Katalogansichten, Richtlinien und Metadaten eines gelöschten freigegebenen Katalogs aufbewahrt werden, bevor sie dauerhaft gelöscht werden. Der Standardwert ist 7 Tage. Auf `0` setzen, um das Löschen sofort zu wiederholen. |

{style="table-layout:auto"}

## [!UICONTROL Creation]

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
| --- | --- | --- |
| [!UICONTROL Creation Grace Period (days)] | Global | Anzahl der Tage, die eine neu registrierte Katalogansicht warten kann, bis die [!DNL Adobe Commerce Optimizer Connector for B2B] die erste Synchronisierung der Katalogansicht, Richtlinie, Preisliste und Schlüsselkonfigurationen abgeschlossen hat, während ihr Status als [!UICONTROL Pending] gemeldet wird. Wenn die Übergangsphase ohne erfolgreiche Synchronisierung abläuft, ändert sich der Status in [!UICONTROL Failed]. Standardwert: `1` |

{style="table-layout:auto"}

## [!UICONTROL Drift Reconciler]

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
| --- | --- | --- |
| [!UICONTROL Enabled] | Global | Führt den geplanten Drift-Abstimmer aus, um Unterschiede zwischen der von [!DNL Adobe Commerce] projizierten Katalogansicht und der Katalogansichtskonfiguration in [!DNL Adobe Commerce Optimizer] zu erkennen und zu melden. Wenn `automatically repair drift` aktiviert ist, wird auch versucht, alle reparierbaren Diskrepanzen zu beheben. |
| [!UICONTROL Automatically Repair Drift] | Global | Bei Festlegung auf `Yes` aktualisiert der geplante Drift-Abstimmer die [!DNL Adobe Commerce Optimizer]-Konfiguration entsprechend der [!DNL Adobe Commerce] und synchronisiert die Konfiguration erneut. Bei Festlegung auf `No` werden bei der Ausführung nur Abweichungen erkannt und gemeldet. Verwaiste [!DNL Adobe Commerce Optimizer] werden immer gemeldet und nie automatisch entfernt. |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
> - [ACO-Katalogansicht](./aco-catalog-view.md) - Konfigurieren von Zugriffstoken für Storefront-Lesevorgänge einer Katalogansicht
> - [Überwachung des Synchronisationsstatus der Katalogansicht](../../systems/catalog-view-sync-status.md) — Überwachen des Synchronisationszustands und Abgleichen von Drift mit diesen Einstellungen
> - [Verwaltung von eingeschränkten Zugriffsschlüsseln](../../systems/restricted-access-keys.md) - Verwalten der Zugriffsschlüssel, die synchronisierten Katalogansichten zugewiesen sind
