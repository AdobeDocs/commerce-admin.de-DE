---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Shipping Settings]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Sales] &gt; [!UICONTROL Shipping Settings] des Commerce Admin-Bereichs.
exl-id: d7d46946-f8c9-4714-96c3-2173e28f7bfa
feature: Configuration, Shipping/Delivery
source-git-commit: 528e57df775b53b6137e1542ad0583c60d2f47ff
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL Shipping Settings]

{{config}}

Weitere Informationen zum Ändern dieser Einstellungen finden Sie unter [Versandeinstellungen](../../stores-purchase/shipping-settings.md) im _Handbuch für Stores und Kauferlebnisse_.

## [!UICONTROL Origin]

![Herkunft](./assets/shipping-settings-origin.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Country] | Website | Das Herkunftsland des Punktes. |
| [!UICONTROL Region/State] | Website | Die Region oder das Bundesland mit dem Ursprungsort. |
| [!UICONTROL ZIP/Postal Code] | Website | Die Postleitzahl am Ursprungsort. |
| [!UICONTROL City] | Website | Die Stadt am Ausgangspunkt. |
| [!UICONTROL Street Address] | Website | Die Straße, von der aus die Straße stammt. |
| [!UICONTROL Street Address Line 2] | Website | Bei Bedarf eine zusätzliche Zeile für die Straßenadresse des Herkunftsorts. |

{style="table-layout:auto"}

## [!UICONTROL Shipping Policy Parameters]

![Versandrichtlinienparameter](./assets/shipping-settings-shipping-policy-parameters.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Apply Custom Shipping Policy] | Website | Bestimmt, ob Ihre Versandrichtlinie während des Checkouts angezeigt wird. Optionen: `Yes` / `No` |
| [!UICONTROL Shipping Policy] | Shop-Ansicht | Enthält Ihre Versandrichtlinie als Text. |

{style="table-layout:auto"}

## [!UICONTROL Shipment Tracking URLs]

[!BADGE nur SaaS]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce as a Cloud Service-Projekte (von Adobe verwaltete SaaS-Infrastruktur)."}

[!BADGE Sandbox]{type=Caution tooltip="Die aufgelisteten Elemente sind derzeit nur in Sandbox-Umgebungen verfügbar. Adobe stellt neue Versionen zunächst in Sandbox-Umgebungen bereit, um Zeit zum Testen bevorstehender Änderungen zu haben, bevor die Version in Produktionsumgebungen verfügbar ist."}

![Versandrichtlinienparameter](./assets/shipping-settings-shipment-tracking-urls.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable Custom Tracking URLs] | Shop-Ansicht | Bestimmt, ob die Sendungsverfolgungsnummern, die in Kunden-E-Mails gesendet werden, Links oder Nur-Text-Nachrichten sind. Der Standardwert `No` zeigt an, dass die Zahlen Nur-Text-Werte sind. Optionen: `Yes` / `No` |
| [!UICONTROL USPS Tracking URL] | Shop-Ansicht | Die URL-Vorlage für Postsendungen in den USA. |
| [!UICONTROL UPS Tracking URL] | Shop-Ansicht | Die URL-Vorlage für Sendungen mit United Parcel Service. |
| [!UICONTROL FedEx Tracking URL] | Shop-Ansicht | Die URL-Vorlage für Federal Express-Sendungen. |
| [!UICONTROL DHL Tracking URL] | Shop-Ansicht | Die URL-Vorlage für DHL-Express-Sendungen. |

{style="table-layout:auto"}
