---
title: '[!UICONTROL General] &gt; [!UICONTROL B2B Features]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL General] &gt; [!UICONTROL B2B Features] des Commerce-Administrators.
exl-id: fc07a067-b92a-49c7-8512-2dfcc1c6ba0c
feature: Configuration, B2B
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 1%

---

# [!UICONTROL General] > [!UICONTROL B2B Features]

{{b2b-feature}}

{{config}}

>[!TIP]
>
>Mit der Installation und Aktivierung von Adobe Commerce B2B kann das Kauferlebnis mit unternehmensspezifischen Funktionen personalisiert werden. Adobe Commerce B2B ist eine integrierte Lösung, die sowohl B2B- als auch B2C-Modelle unterstützt. Weitere Informationen zu den B2B-Funktionen finden Sie im [_Adobe Commerce B2B-Benutzerhandbuch_](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html).

## [!UICONTROL B2B Features]

![B2B-Funktionen](./assets/b2b-features.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|------- |----------------------------------------------------------------------- |------------ |
| [[!UICONTROL Enable Company]](../../b2b/account-companies.md) | Webseite | Wenn diese Option aktiviert ist, können Kunden ihre Unternehmenszuweisung über ihr Konto-Dashboard verwalten und standardmäßig die Funktionen &quot;Gemeinsamer Katalog&quot;und &quot;B2B-Zitat&quot;aktivieren. Optionen: `Yes` / `No` |
| [[!UICONTROL Enable Quick Order]](../../b2b/quick-order.md) | Webseite | Wenn diese Option aktiviert ist, können Kunden und Gäste schnell Bestellungen basierend auf der SKU oder dem Produktnamen aufgeben. Optionen: `Yes` / `No` |
| [[!UICONTROL Enable Requisition List]](../../b2b/configure-requisition-lists.md) | Webseite | Wenn diese Option aktiviert ist, können Kunden Anforderungslisten über ihr Konto-Dashboard erstellen und verwalten. |

{style="table-layout:auto"}

![B2B Funktionen mit aktivierten Unternehmen und freigegebenen Katalogen](./assets/b2b-features-company-enabled.png)<!-- zoom -->

Wenn die Funktion &quot;Unternehmen&quot;aktiviert ist, stehen zusätzliche Felder für den freigegebenen Katalog und das B2B-Angebot zur Verfügung.

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|------- |----------------------------------------------------------------------- |------------ |
| [[!UICONTROL Enable Shared Catalog]](../../b2b/catalog-shared.md) | Webseite | Wenn diese Option aktiviert ist, können kuratierte Kataloge mit benutzerdefinierten Preisen erstellt werden, die entweder global verfügbar sind oder auf bestimmte Unternehmen beschränkt sind. Optionen: `Yes` / `No` |
| [!UICONTROL Enable Shared Catalog direct products price assigning] | Webseite | Wenn das Feld _[!UICONTROL Enable Shared Catalog]_auf `Yes` gesetzt ist, ist diese Option verfügbar. Wenn diese Option aktiviert ist, werden nur Produkte im Preisindex gespeichert, die einem freigegebenen Katalog zugewiesen sind. Produkte, die nicht dem freigegebenen Katalog zugewiesen sind, werden nicht auf der Storefront angezeigt. Optionen: `Yes` / `No` |
| [[!UICONTROL Enable B2B Quote]](../../b2b/configure-quotes.md) | Webseite | Wenn diese Option aktiviert ist, können Firmenkäufer einen Kostenvoranschlag aus dem Warenkorb einreichen. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

### [!UICONTROL Default B2B Payment Methods]

![B2B-Konfiguration - Standardeinstellungen für Zahlungsmethoden](./assets/b2b-features-default-payment-methods.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|------- |----------------------------------------------------------------------- |------------ |
| [!UICONTROL Applicable Payment Methods] | Global | Bestimmt die Auswahl der Zahlungsmethoden, die für B2B-Käufer verfügbar sind. Optionen: `All Payment Methods` / `Specific Payment Methods` |
| [!UICONTROL Payment Methods] | Global | Gibt jede Zahlungsmethode an, die B2B-Käufern zur Verfügung steht. |

{style="table-layout:auto"}

### [!UICONTROL Default B2B Shipping Methods]

![B2B-Konfiguration - standardmäßige Versandmethoden](./assets/b2b-features-shipping-methods.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|------- |----------------------------------------------------------------------- |------------ |
| [!UICONTROL Applicable Shipping Methods] | Global | Bestimmt die Auswahl der Versandmethoden, die B2B-Käufern standardmäßig zur Verfügung stehen. Optionen: `All Shipping Methods` / `Specific Shipping Methods` |
| [!UICONTROL Shipping Methods] | Global | Gibt jede Versandmethode an, die B2B-Käufern standardmäßig zur Verfügung steht. <br/>**_Hinweis:_**Sie können auch die Versandmethoden für ein bestimmtes [Unternehmenskonto](../../b2b/account-companies.md) einschränken. |

{style="table-layout:auto"}

## [!UICONTROL Order Approval Configuration]

![B2B-Funktionen - Konfiguration der Bestellbestätigung](./assets/b2b-features-order-approval.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|------- |----------------------------------------------------------------------- |------------ |
| [[!UICONTROL Enable Purchase Orders]](../../stores-purchase/purchase-order.md) | Webseite | Wenn diese Option aktiviert ist, können Unternehmen Bestellungen erstellen. Optionen: `Yes` / `No` |

{style="table-layout:auto"}


