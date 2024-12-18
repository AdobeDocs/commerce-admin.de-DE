---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Gift Cards]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Sales] &gt; [!UICONTROL Gift Cards] des Commerce Admin-Bereichs.
exl-id: 95bfdbde-633e-44d0-9d43-00dde671ab6d
feature: Configuration, Gift
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL Gift Cards]

{{ee-feature}}

{{config}}

## [!UICONTROL Gift Card Email Settings]

![E-Mail-Einstellungen für Geschenkkarte](./assets/gift-cards-gift-card-email-settings.png)<!-- zoom -->

<!-- [Gift Card Email Settings](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/gift-cards/product-gift-card-accounts#configure-gift-card-accounts) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Gift Card Notification Email Sender] | Shop-Ansicht | Identifiziert den [Store-Kontakt](../../getting-started/store-details.md#store-email-addresses) der als Absender der E-Mail mit der Geschenkkarte angezeigt wird. Standardwert: `General Contact` |
| [!UICONTROL Gift Card Notification Email Template] | Shop-Ansicht | Bestimmt die [Vorlage](../../systems/email-templates.md), die für die E-Mail mit der Geschenkkarte verwendet wird. |

{style="table-layout:auto"}

## [!UICONTROL Gift Card General Settings]

![Allgemeine Einstellungen für Geschenkgutscheine](./assets/gift-cards-gift-card-general-settings.png)<!-- zoom -->

<!-- [Gift Card General Settings](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/gift-cards/product-gift-card-accounts#configure-gift-card-accounts) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Redeemable] | Global | Legt fest, ob der Besitzer der Geschenkkarte seinen Wert in bar einlösen kann. Optionen: `Yes` / `No`. |
| [!UICONTROL Lifetime (days)] | Global | Bestimmt die Anzahl der Tage, die die Karte gültig ist. Wenn Sie das Feld leer lassen, läuft die Karte nicht ab. <br/><br/>**_Wichtig:_**An einigen Stellen ist es illegal, auf Geschenkgutscheinen Ablaufdaten festzulegen. Überprüfen Sie Ihre lokalen Gesetze, bevor Sie eine Lebensdauer für Ihre Geschenkgutscheine festlegen. |
| [!UICONTROL Allow Gift Message] | Shop-Ansicht | Legt fest, ob Kunden, die eine Geschenkkarte erwerben, die Option zum Einschließen einer Geschenknachricht zur Verfügung steht. Optionen: `Yes` / `No`. |
| [!UICONTROL Gift Message Maximum Length] | Shop-Ansicht | Bestimmt die maximale Anzahl von Zeichen, die in einer Geschenkkartennachricht zulässig ist. Standardwert: 255 |
| [!UICONTROL Generate Gift Card Account when Order Item is] | Global | Bestimmt, ob ein Geschenkkartenkonto generiert wird, wenn ein Kunde eine Bestellung aufgibt oder wenn die Bestellung fakturiert wird. Optionen: `Ordered` / `Invoiced` |

{style="table-layout:auto"}

## [!UICONTROL Email Sent from Gift Card Account Management]

![E-Mail von Gift Card Account Management gesendet](./assets/gift-cards-email-sent-from-account.png)<!-- zoom -->

<!-- [Email Sent from Gift Card Account Management](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/gift-cards/product-gift-card-accounts#configure-gift-card-accounts) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Gift Card Email Sender] | Shop-Ansicht | Identifiziert den [Store-Kontakt](../../getting-started/store-details.md#store-email-addresses) der als Absender der E-Mail mit der Geschenkkarte angezeigt wird. Standardwert: `General Contact` |
| [!UICONTROL Gift Card Template] | Shop-Ansicht | Bestimmt die [Vorlage](../../systems/email-templates.md), die für die E-Mail mit der Geschenkkarte verwendet wird. |

{style="table-layout:auto"}

## [!UICONTROL Gift Card Account General Settings]

![Allgemeine Einstellungen für Geschenkkartenkonten](./assets/gift-cards-gift-card-account-general-settings.png)<!-- zoom -->

<!-- [Gift Card Account General Settings](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/gift-cards/product-gift-card-accounts#configure-gift-card-accounts) -->

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
