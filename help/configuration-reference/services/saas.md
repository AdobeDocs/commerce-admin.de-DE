---
title: '[!UICONTROL Services] > [!UICONTROL Commerce Services Connector]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Services] > [!UICONTROL Commerce Services Connector] des Commerce Admin.
exl-id: 3570e846-c8ab-4a36-b020-1b536bbd377d
feature: Configuration, Saas
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
TQID: https://experienceleague.adobe.com/50XCqY8JMjvf9G-wcHLxvlskSd5noIAB0LIX6xMarL0
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
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 238
ht-degree: 2%

---

# [!UICONTROL Services] > [!UICONTROL Commerce Services Connector]

Informationen zum Verbinden Ihres Stores mit Adobe Commerce-Services finden Sie unter [Commerce-Services](https://experienceleague.adobe.com/docs/commerce/user-guides/integration-services/saas.html).

{{config}}

## [!UICONTROL Sandbox API Keys]

![Sandbox-API-Schlüssel](./assets/sandbox-key-saas-configuration.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Sandbox public API key] | Global | API-Schlüssel, der den Autor und gegebenenfalls seine Berechtigungen identifiziert. |
| [!UICONTROL Sandbox private API key] | Global | Ein mit dem API-Schlüssel verknüpfter privater Schlüssel. |

{style="table-layout:auto"}

## [!UICONTROL Production Keys]

![Produktions-API-Schlüssel](./assets/prod-key-saas-configuration.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Production public API key] | Global | API-Schlüssel, der den Autor und gegebenenfalls seine Berechtigungen identifiziert. |
| [!UICONTROL Production private API key] | Global | Ein mit dem API-Schlüssel verknüpfter privater Schlüssel. |

{style="table-layout:auto"}

## [!UICONTROL SaaS Identifier]

![SaaS-Kennung](./assets/saas-identifier.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Project] | Global | Name des SaaS-Projekts, das alle Ihre SaaS-Datenräume gruppiert. Wenn _SaaS-Projekte nicht vorhanden sind, wird die Schaltfläche_ Projekt erstellen“ angezeigt. |
| [!UICONTROL Data Space] | Global | Listet die SaaS-Datenräume im angegebenen SaaS-Projekt auf. Die Anzahl der SaaS-Datenräume hängt von Ihrer [Commerce-Lizenz ab](https://experienceleague.adobe.com/docs/commerce/user-guides/integration-services/saas.html)<br />Adobe Commerce: ein Produktionsdatenraum; zwei Testdatenräume;<br />Magento Open Source: ein Produktionsdatenraum; keine Testdatenräume |

{style="table-layout:auto"}

## [!UICONTROL IMS Organization]

![IMS-Organisation](./assets/ims-organization.png)<!-- zoom -->

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Sign in using Adobe ID] | Ihre Adobe ID ist in der Regel die E-Mail-Adresse, die Sie zum ersten Mal verwendet haben, als Sie Ihre Mitgliedschaft begonnen oder eine Anwendung oder einen Service für Adobe erworben haben. Ihre Adobe ID ist der Schlüssel, den Sie für den Zugriff auf Ihr Adobe-Konto benötigen. |

{style="table-layout:auto"}
