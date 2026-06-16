---
title: '[!UICONTROL Sales] > [!UICONTROL Gift Cards]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Sales] > [!UICONTROL Gift Cards] des Commerce Admin.
exl-id: 95bfdbde-633e-44d0-9d43-00dde671ab6d
feature: Configuration, Gift
TQID: https://experienceleague.adobe.com/J-VH-mdaM7HrMRHJMNmmbBPggm1hjtHHWTh3q-5en0w
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: d9ced453-36f4-4eb5-b2f3-1d593e32476b
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
source-wordcount: 333
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL Gift Cards]

{{ee-feature}}

{{config}}

## [!UICONTROL Gift Card Email Settings]

![E-Mail-Einstellungen für Geschenkkarte](./assets/gift-cards-gift-card-email-settings.png)<!-- zoom -->

<!-- [Gift Card Email Settings](https://experienceleague.adobe.com/de/docs/commerce-admin/stores-sales/point-of-purchase/gift-cards/product-gift-card-accounts#configure-gift-card-accounts) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Gift Card Notification Email Sender] | Shop-Ansicht | Identifiziert den [Store-Kontakt](../../getting-started/store-details.md#store-email-addresses) der als Absender der E-Mail mit der Geschenkkarte angezeigt wird. Standardwert: `General Contact` |
| [!UICONTROL Gift Card Notification Email Template] | Shop-Ansicht | Bestimmt die [Vorlage](../../systems/email-templates.md), die für die E-Mail mit der Geschenkkarte verwendet wird. |

{style="table-layout:auto"}

## [!UICONTROL Gift Card General Settings]

![Allgemeine Einstellungen für Geschenkgutscheine](./assets/gift-cards-gift-card-general-settings.png)<!-- zoom -->

<!-- [Gift Card General Settings](https://experienceleague.adobe.com/de/docs/commerce-admin/stores-sales/point-of-purchase/gift-cards/product-gift-card-accounts#configure-gift-card-accounts) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Redeemable] | Global | Legt fest, ob der Besitzer der Geschenkkarte seinen Wert in bar einlösen kann. Optionen: `Yes` / `No`. |
| [!UICONTROL Lifetime (days)] | Global | Bestimmt die Anzahl der Tage, die die Karte gültig ist. Wenn Sie das Feld leer lassen, läuft die Karte nicht ab. <br/><br/>**_Wichtig:_** An manchen Stellen ist es illegal, Ablaufdaten auf Geschenkgutscheinen festzulegen. Überprüfen Sie Ihre lokalen Gesetze, bevor Sie eine Lebensdauer für Ihre Geschenkgutscheine festlegen. |
| [!UICONTROL Allow Gift Message] | Shop-Ansicht | Legt fest, ob Kunden, die eine Geschenkkarte erwerben, die Option zum Einschließen einer Geschenknachricht zur Verfügung steht. Optionen: `Yes` / `No`. |
| [!UICONTROL Gift Message Maximum Length] | Shop-Ansicht | Bestimmt die maximale Anzahl von Zeichen, die in einer Geschenkkartennachricht zulässig ist. Standardwert: 255 |
| [!UICONTROL Generate Gift Card Account when Order Item is] | Global | Bestimmt, ob ein Geschenkkartenkonto generiert wird, wenn ein Kunde eine Bestellung aufgibt oder wenn die Bestellung fakturiert wird. Optionen: `Ordered` / `Invoiced` |

{style="table-layout:auto"}

## [!UICONTROL Email Sent from Gift Card Account Management]

![E-Mail von Gift Card Account Management gesendet](./assets/gift-cards-email-sent-from-account.png)<!-- zoom -->

<!-- [Email Sent from Gift Card Account Management](https://experienceleague.adobe.com/de/docs/commerce-admin/stores-sales/point-of-purchase/gift-cards/product-gift-card-accounts#configure-gift-card-accounts) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Gift Card Email Sender] | Shop-Ansicht | Identifiziert den [Store-Kontakt](../../getting-started/store-details.md#store-email-addresses) der als Absender der E-Mail mit der Geschenkkarte angezeigt wird. Standardwert: `General Contact` |
| [!UICONTROL Gift Card Template] | Shop-Ansicht | Bestimmt die [Vorlage](../../systems/email-templates.md), die für die E-Mail mit der Geschenkkarte verwendet wird. |

{style="table-layout:auto"}

## [!UICONTROL Gift Card Account General Settings]

![Allgemeine Einstellungen für Geschenkkartenkonten](./assets/gift-cards-gift-card-account-general-settings.png)<!-- zoom -->

<!-- [Gift Card Account General Settings](https://experienceleague.adobe.com/de/docs/commerce-admin/stores-sales/point-of-purchase/gift-cards/product-gift-card-accounts#configure-gift-card-accounts) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Code Length] | Global | Bestimmt die Länge des Geschenkkartencodes. |
| [!UICONTROL Code Format] | Global | Bestimmt das Format des Geschenkkartencodes. Optionen: `Alphanumeric` / `Numeric` |
| [!UICONTROL Code Prefix] | Global | Definiert jedes Präfix, das am Anfang des Codes hinzugefügt wird. |
| [!UICONTROL Code Suffix] | Global | Definiert jedes Suffix, das am Ende des Codes hinzugefügt wird. |
| [!UICONTROL Dash Every X Characters] | Global | Wenn Sie Bindestriche in den Code aufnehmen möchten, bestimmt die Anzahl der Zeichen zwischen den einzelnen Bindestrichen. |
| [!UICONTROL New Pool Size] | Global | Bestimmt die Größe des neuen zu generierenden Code-Pools. |
| [!UICONTROL Low Code Pool Threshold] | Global | Bestimmt die Anzahl der Datensätze im Code-Pool, in denen ein Warnhinweis enthalten ist, dass der Trigger aufgefüllt werden muss. |
| [!UICONTROL Generate] | Global | Klicken, um die Liste der Geschenkkartencodes zu generieren. |

{style="table-layout:auto"}
