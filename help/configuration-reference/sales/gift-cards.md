---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Gift Cards]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Sales] &gt; [!UICONTROL Gift Cards] des Commerce-Administrators.
exl-id: 95bfdbde-633e-44d0-9d43-00dde671ab6d
feature: Configuration, Gift
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL Gift Cards]

{{ee-feature}}

{{config}}

## [!UICONTROL Gift Card Email Settings]

![E-Mail-Einstellungen für die Gift-Karte](./assets/gift-cards-gift-card-email-settings.png)<!-- zoom -->

<!-- [Gift Card Email Settings](https://docs.magento.com/user-guide/catalog/product-gift-card-account-configuration.html) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Gift Card Notification Email Sender] | Store-Ansicht | Identifiziert den [Store contact](../../getting-started/store-details.md#store-email-addresses) , der als Absender der Benachrichtigungs-E-Mail über die Geschenkkarte angezeigt wird. Standardwert: `General Contact` |
| [!UICONTROL Gift Card Notification Email Template] | Store-Ansicht | Bestimmt die [Vorlage](../../systems/email-templates.md) , die für die Benachrichtigungs-E-Mail für die Geschenkkarte verwendet wird. |

{style="table-layout:auto"}

## [!UICONTROL Gift Card General Settings]

![Allgemeine Einstellungen für die Geschenkkarte](./assets/gift-cards-gift-card-general-settings.png)<!-- zoom -->

<!-- [Gift Card General Settings](https://docs.magento.com/user-guide/catalog/product-gift-card-account-configuration.html) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Redeemable] | Global | Stellt fest, ob der Inhaber der Geschenkkarte seinen Wert in bar einlösen kann. Optionen: `Yes` / `No`. |
| [!UICONTROL Lifetime (days)] | Global | Bestimmt die Anzahl der Tage, in denen die Karte gültig ist. Wenn Sie das Feld leer lassen, läuft die Karte nicht ab. <br/><br/>**_Wichtig:_**An manchen Stellen ist es verboten, Ablaufdaten für Geschenkkarten festzulegen. Prüfen Sie Ihre lokalen Gesetze, bevor Sie eine Lebensdauer für Ihre Geschenkgutscheine festlegen. |
| [!UICONTROL Allow Gift Message] | Store-Ansicht | Bestimmt, ob die Option zum Einfügen einer Geschenknachricht für Kunden verfügbar ist, die eine Geschenkkarte kaufen. Optionen: `Yes` / `No`. |
| [!UICONTROL Gift Message Maximum Length] | Store-Ansicht | Bestimmt die maximal zulässige Anzahl von Zeichen in einer Geschenkkartennachricht. Standardwert: 255 |
| [!UICONTROL Generate Gift Card Account when Order Item is] | Global | Bestimmt, ob ein Geschenkkartenkonto generiert wird, wenn ein Kunde eine Bestellung aufgibt oder wenn die Bestellung fakturiert wird. Optionen: `Ordered` / `Invoiced` |

{style="table-layout:auto"}

## [!UICONTROL Email Sent from Gift Card Account Management]

![Vom Gift Card Account Management gesendete E-Mail](./assets/gift-cards-email-sent-from-account.png)<!-- zoom -->

<!-- [Email Sent from Gift Card Account Management](https://docs.magento.com/user-guide/catalog/product-gift-card-account-configuration.html) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Gift Card Email Sender] | Store-Ansicht | Identifiziert den [Store contact](../../getting-started/store-details.md#store-email-addresses) , der als Absender der E-Mail mit der Geschenkkarte angezeigt wird. Standardwert: `General Contact` |
| [!UICONTROL Gift Card Template] | Store-Ansicht | Legt die [Vorlage](../../systems/email-templates.md) fest, die für die E-Mail mit der Geschenkkarte verwendet wird. |

{style="table-layout:auto"}

## [!UICONTROL Gift Card Account General Settings]

![Allgemeine Einstellungen des Gift-Card-Kontos](./assets/gift-cards-gift-card-account-general-settings.png)<!-- zoom -->

<!-- [Gift Card Account General Settings](https://docs.magento.com/user-guide/catalog/product-gift-card-account-configuration.html) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Code Length] | Global | Bestimmt die Länge des Geschenkkartencodes. |
| [!UICONTROL Code Format] | Global | Legt das Format des Geschenkkartencodes fest. Optionen: `Alphanumeric` / `Numeric` |
| [!UICONTROL Code Prefix] | Global | Definiert jedes Präfix, das am Anfang des Codes hinzugefügt wird. |
| [!UICONTROL Code Suffix] | Global | Definiert jedes Suffix, das am Ende des Codes hinzugefügt wird. |
| [!UICONTROL Dash Every X Characters] | Global | Wenn Sie Bindestriche in den Code aufnehmen möchten, bestimmt die Anzahl der Zeichen zwischen den einzelnen Bindestrichen. |
| [!UICONTROL New Pool Size] | Global | Bestimmt die Größe des neuen zu generierenden Code-Pools. |
| [!UICONTROL Low Code Pool Threshold] | Global | Bestimmt die Anzahl der Einträge im Code-Pool, die einen Warnhinweis an den Trigger senden, dass der Pool neu aufgefüllt werden muss. |
| [!UICONTROL Generate] | Global | Klicken Sie auf , um die Liste der Geschenkkarten-Codes zu erstellen. |

{style="table-layout:auto"}
