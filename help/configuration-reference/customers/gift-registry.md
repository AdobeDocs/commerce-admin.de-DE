---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Gift Registry]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Customers] &gt; [!UICONTROL Gift Registry] des Commerce-Administrators.
exl-id: c5153c4e-897a-41d2-bde1-8483855d1a37
feature: Configuration, Gift
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 1%

---

# [!UICONTROL Customers] > [!UICONTROL Gift Registry]

{{ee-feature}}

{{config}}

Ausführliche Informationen zur Verwendung dieser Einstellungen zum Aktivieren von Geschenkregistern für Ihre Store-Kunden finden Sie unter [Konfigurieren von Geschenkregistern](../../merchandising-promotions/gift-registry-configure.md). Weitere Informationen zum Einschließen der Suche in die Geschenkregistrierung in die Storefront finden Sie unter [Hinzufügen der Suche in der Geschenkregistrierung](../../merchandising-promotions/gift-registry-search.md).

## [!UICONTROL General Options]

![Allgemeine Optionen](./assets/gift-registry-general-options.png)<!-- zoom -->

<!-- [General Options](https://docs.magento.com/user-guide/marketing/gift-registry-configure.html) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable Gift Registry] | Store-Ansicht | Bestimmt, ob Geschenkgutscheine verfügbar sind. Optionen: <br/>**`Yes`**- Aktiviert Geschenkeintragungen für die ausgewählte Store-Ansicht. Die Registerkarte Gift Registry wird im Konto-Dashboard registrierter Kunden angezeigt.<br/>**`No`** - Geschenk-Registrierungen sind nicht für die Store-Ansicht verfügbar. |
| [!UICONTROL Maximum Registrants] | Store-Ansicht | Legt die Anzahl der Personen fest, die ein Kunde einer Geschenkregistrierung hinzufügen kann. Der Kunde teilt die Geschenkregistrierung mit jedem Registrierungspflichtigen. In der Storefront steht Kunden die Schaltfläche _Registrant hinzufügen_ zur Verfügung, bis die maximale Anzahl erreicht ist. |

{style="table-layout:auto"}

## [!UICONTROL Owner Notification]

![Benachrichtigung des Eigentümers](./assets/gift-registry-owner-notification.png)<!-- zoom -->

<!-- [Owner Notification](https://docs.magento.com/user-guide/marketing/gift-registry-configure.html) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Email Template] | Store-Ansicht | Legt die Vorlage fest, die für die E-Mail-Benachrichtigung des Eigentümers verwendet wird, die beim Erstellen einer Geschenkregistrierung gesendet wird. Standardvorlage: Benachrichtigung des Eigentümers der Geschenkregistrierung |
| [!UICONTROL Email Sender] | Store-Ansicht | Gibt den [Store-Kontakt](../../getting-started/store-details.md#store-email-addresses) an, der als Absender der Benachrichtigungs-E-Mail für Geschenkregistereigentümer angezeigt wird. Standardwert: `General Contact` |

{style="table-layout:auto"}

## Freigabe der Geschenkregistrierung

![Freigabe der Geschenkregistrierung](./assets/gift-registry-gift-registry-sharing.png)<!-- zoom -->

<!-- Gift Registry Sharing](https://docs.magento.com/user-guide/marketing/gift-registry-configure.html) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Email Template] | Store-Ansicht | Legt die Vorlage fest, die für die E-Mail-Freigabe in der Geschenkregistrierung verwendet wird, die gesendet wird, wenn eine Geschenkregistrierung erstellt wird. Wenn der Inhaber auf _Geschenkregistrierung teilen_ klickt, wird die E-Mail an jeden Empfänger gesendet. Standardvorlage: `Gift Registry Sharing` |
| [!UICONTROL Email Sender] | Store-Ansicht | Gibt den [Store-Kontakt](../../getting-started/store-details.md#store-email-addresses) an, der als Absender der E-Mail zur Freigabe der Geschenkregistrierung erscheint. Standardwert: `General Contact` |
| [!UICONTROL Maximum Sent Emails Threshold] | Store-Ansicht | Die maximale Anzahl von E-Mail-Benachrichtigungen, die gleichzeitig an die Geschenkregistrierung gesendet werden können. |

{style="table-layout:auto"}

## [!UICONTROL Gift Registry Update]

![Aktualisierung der Geschenkregistrierung](./assets/gift-registry-gift-registry-update.png)<!-- zoom -->

<!-- [Gift Registry Update](https://docs.magento.com/user-guide/marketing/gift-registry-configure.html) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Email Template] | Store-Ansicht | Legt die Vorlage fest, die für die E-Mail-Aktualisierung der Geschenkregistrierung verwendet wird, die an den Eigentümer der Geschenkregistrierung gesendet wird, wenn ein Kauf aus der Geschenkregistrierung getätigt wird. Die Aktualisierung enthält Informationen über den gekauften Artikel und die gekaufte Menge, enthält jedoch nicht den Namen der Person, die die Bestellung aufgegeben hat. Standardvorlage: `Gift Registry Update` |
| [!UICONTROL Email Sender] | Store-Ansicht | Identifiziert den [Store-Kontakt](../../getting-started/store-details.md#store-email-addresses), der als Absender der E-Mail &quot;Gift Registry-Update&quot;angezeigt wird. Standardwert: `General Contact` |

{style="table-layout:auto"}
