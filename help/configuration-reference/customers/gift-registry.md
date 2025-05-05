---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Gift Registry]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Customers] &gt; [!UICONTROL Gift Registry] des Commerce Admin-Bereichs.
exl-id: c5153c4e-897a-41d2-bde1-8483855d1a37
feature: Configuration, Gift
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 1%

---

# [!UICONTROL Customers] > [!UICONTROL Gift Registry]

{{ee-feature}}

{{config}}

Detaillierte Informationen zur Verwendung dieser Einstellungen zum Aktivieren von Geschenkregistrierungen für Ihre Store-Kunden finden Sie unter [Konfigurieren von Geschenkregistrierungen](../../merchandising-promotions/gift-registry-configure.md). Weitere Informationen zur Verwendung der Geschenkregistrierung in der Storefront finden Sie unter [Geschenkregistrierung hinzufügen](../../merchandising-promotions/gift-registry-search.md).

## [!UICONTROL General Options]

![Allgemeine Optionen](./assets/gift-registry-general-options.png)<!-- zoom -->

<!-- [General Options](https://experienceleague.adobe.com/de/docs/commerce-admin/marketing/merchandising/gift-registry/gift-registry-configure) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable Gift Registry] | Shop-Ansicht | Legt fest, ob Geschenkregistrierungen verfügbar sind. Optionen: <br/>**`Yes`**- Ermöglicht Geschenkregistrierungen für die ausgewählte Shop-Ansicht. Die Registerkarte Geschenkregistrierung wird im Konto-Dashboard registrierter Kundinnen und Kunden angezeigt.<br/>**`No`** - Geschenkregistrierungen sind für die Store-Ansicht nicht verfügbar. |
| [!UICONTROL Maximum Registrants] | Shop-Ansicht | Legt die Anzahl der Personen fest, die eine Kundin oder ein Kunde einer Geschenkregistrierung hinzufügen kann. Der Kunde teilt die Geschenkregistrierung mit jedem Registranten. In der Storefront ist die Schaltfläche _Registranten hinzufügen_ für Kundinnen und Kunden verfügbar, bis die maximale Anzahl erreicht ist. |

{style="table-layout:auto"}

## [!UICONTROL Owner Notification]

![Benachrichtigung des Inhabers](./assets/gift-registry-owner-notification.png)<!-- zoom -->

<!-- [Owner Notification](https://experienceleague.adobe.com/de/docs/commerce-admin/marketing/merchandising/gift-registry/gift-registry-configure) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Email Template] | Shop-Ansicht | Bestimmt die Vorlage für die E-Mail-Benachrichtigung des Inhabers, die bei der Erstellung einer Geschenkregistrierung gesendet wird. Standardvorlage: Benachrichtigung des Inhabers der Geschenkregistrierung |
| [!UICONTROL Email Sender] | Shop-Ansicht | Identifiziert den [Store-Kontakt](../../getting-started/store-details.md#store-email-addresses) der als Absender der E-Mail mit der Benachrichtigung des Eigentümers der Geschenkregistrierung angezeigt wird. Standardwert: `General Contact` |

{style="table-layout:auto"}

## Freigabe der Geschenkregistrierung

![Gift Registry Sharing](./assets/gift-registry-gift-registry-sharing.png)<!-- zoom -->

<!-- Gift Registry Sharing](https://experienceleague.adobe.com/de/docs/commerce-admin/marketing/merchandising/gift-registry/gift-registry-configure) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Email Template] | Shop-Ansicht | Bestimmt die Vorlage für die E-Mail zur Freigabe der Geschenkregistrierung, die bei der Erstellung einer Geschenkregistrierung gesendet wird. Wenn der Besitzer auf _Geschenkregistrierung freigeben_ klickt, wird die E-Mail an jeden Empfänger gesendet. Standardvorlage: `Gift Registry Sharing` |
| [!UICONTROL Email Sender] | Shop-Ansicht | Identifiziert den [Store-Kontakt](../../getting-started/store-details.md#store-email-addresses) der als Absender der E-Mail zur Freigabe der Geschenkregistrierung angezeigt wird. Standardwert: `General Contact` |
| [!UICONTROL Maximum Sent Emails Threshold] | Shop-Ansicht | Die maximale Anzahl von E-Mail-Benachrichtigungsnachrichten zur Gift Registry-Freigabe, die gleichzeitig gesendet werden können. |

{style="table-layout:auto"}

## [!UICONTROL Gift Registry Update]

![Geschenkregistrierungs-Aktualisierung](./assets/gift-registry-gift-registry-update.png)<!-- zoom -->

<!-- [Gift Registry Update](https://experienceleague.adobe.com/de/docs/commerce-admin/marketing/merchandising/gift-registry/gift-registry-configure) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Email Template] | Shop-Ansicht | Bestimmt die Vorlage für die E-Mail zur Aktualisierung der Geschenkregistrierung, die an den Besitzer der Geschenkregistrierung gesendet wird, wenn ein Kauf über die Geschenkregistrierung getätigt wird. Die Aktualisierung enthält Informationen über den Artikel und die gekaufte Menge, aber nicht den Namen der Person, die die Bestellung aufgegeben hat. Standardvorlage: `Gift Registry Update` |
| [!UICONTROL Email Sender] | Shop-Ansicht | Identifiziert den [Store-Kontakt](../../getting-started/store-details.md#store-email-addresses) der als Absender der E-Mail mit der Aktualisierung der Geschenkregistrierung angezeigt wird. Standardwert: `General Contact` |

{style="table-layout:auto"}
