---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Reward Points]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der [!UICONTROL Customers] &gt; [!UICONTROL Reward Points] Seite des Commerce-Administrators.
exl-id: 0b7f8806-74c5-4467-87da-0faae50f164b
feature: Configuration, Rewards
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '766'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Reward Points]

{{ee-feature}}

{{config}}

>[!NOTE]
>
>[Wechselkurse der Prämien](../../merchandising-promotions/reward-exchange-rates.md) -Konfiguration ist erforderlich, damit Kunden und Administratoren während des Checkouts die Punkte einlösen können.

## [!UICONTROL Reward Points]

![Prämienpunkte](./assets/reward-points-reward-points.png)<!-- zoom -->

<!-- [Reward Points](https://docs.magento.com/user-guide/marketing/reward-point-configure.html) -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable Reward Points Functionality] | Global | Aktiviert oder deaktiviert Prämienpunkte. Optionen: `Yes` / `No`. |
| [!UICONTROL Enable Reward Points Functionality on Storefront] | Webseite | Wenn diese Option aktiviert ist, können Kunden durch ihre Aktivitäten Punkte sammeln und sie beim Checkout einlösen. Wenn diese Option deaktiviert ist, können nur Admin-Benutzer im Namen von Kunden Punkte zuweisen und einlösen. Optionen: `Yes` / `No`. |
| [!UICONTROL Customers May See Reward Points History] | Webseite | Wenn diese Option aktiviert ist, können Kunden in ihrem Konto-Dashboard einen detaillierten Verlauf mit jedem Periodenergebnis, jeder Auszahlung und jedem Ablauf der Punkte sehen. Optionen: `Yes` / `No` |
| [!UICONTROL Reward Points Balance Redemption Threshold] | Webseite | Erfordert Kunden, einen minimalen Punktstand zu erzielen, bevor sie diese für Bestellungen einlösen können. Leer lassen - kein Minimum. |
| [!UICONTROL Cap Reward Points Balance At] | Webseite | Verhindert, dass Kunden mehr als diesen maximalen Punktstand erzielen. Leer lassen für kein Maximum. |
| [!UICONTROL Reward Points Expire in (days)] | Webseite | Gibt die Lebensdauer der Belohnungspunkte in Tagen an. Jeder Punktstapel, der bei separaten Aktivitäten gesammelt wird, hat eine separate Lebensdauer. Jeder Batch im Verlauf der Punkte zeigt die Anzahl der Tage an, die noch vergangen sind, bevor die Punkte ablaufen. Der Verlauf kann über das Konto-Dashboard des Kunden, sofern aktiviert, und über den Admin angezeigt werden. Lassen Sie das Feld für keinen Ablauf leer. |
| [!UICONTROL Reward Points Expiry Calculation] | Webseite | Bestimmt die Methode, mit der bestimmt wird, wann die Belohnungspunkte ablaufen. Optionen: <br/>**`Static`**- Bestimmt die verbleibende Lebensdauer der Bonuspunkte basierend auf der in der Konfiguration festgelegten Anzahl von Tagen. Wenn sich das Ablaufdatum in der Konfiguration ändert, ändert sich das Ablaufdatum vorhandener Punkte nicht.<br/>**`Dynamic`** - Berechnet die Anzahl der verbleibenden Tage, wenn der Saldo des Bonuspunkts zunimmt. Wenn sich das Ablauflimit in der Konfiguration ändert, werden die Ablaufberechnungen für alle vorhandenen Punkte entsprechend aktualisiert. |
| [!UICONTROL Refund Reward Points Automatically] | Global | Bestimmt, ob verfügbare Bonuspunkte automatisch zurückerstattet werden. Optionen: `Yes` / `No` |
| [!UICONTROL Deduct Reward Points from Refund Amount Automatically] | Global | Bestimmt, ob die Belohnungspunkte automatisch vom Erstattungsbetrag abgezogen werden. Optionen: `Yes` / `No`. |
| [!UICONTROL Landing Page] | Store-Ansicht | Gibt die CMS-Seite an, auf der Ihr Prämienpunktprogramm erläutert wird. Ein Link zur standardmäßigen Belohnungsseite wird an den Stellen in Ihrem Geschäft angezeigt, an denen Punkte gesammelt werden können. |

{style="table-layout:auto"}

## [!UICONTROL Actions for Acquiring Reward Points by Customers]

![Aktionen zum Erfassen von Prämienpunkten durch Kunden](./assets/reward-points-actions-for-acquiring.png)<!-- zoom -->

<!-- [Actions for Acquiring Reward Points by Customers](https://docs.magento.com/user-guide/marketing/reward-point-configure.html) -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Purchase] | Webseite | Bestimmt, ob im Warenkorb eine Meldung angezeigt wird, die die für den Kauf erzielten Prämienpunkte und den aktuellen Guthaben-Punkt-Saldo des Kunden anzeigt. Optionen: `Yes` / `No` |
| [!UICONTROL Registration] | Webseite | Gibt die Anzahl der Punkte an, die für das Öffnen eines Kundenkontos gesammelt wurden. |
| [!UICONTROL Newsletter Signup] | Webseite | Gibt die Anzahl der Punkte an, die registrierte Kunden erhalten haben, die einen Newsletter abonnieren. (Punkte stehen nicht für Abonnements durch Gäste zur Verfügung.) Wenn sich ein Kunde abmeldet und sich dann erneut anmeldet, werden für das zweite Abonnement keine Punkte gesammelt. |
| [!UICONTROL Converting Invitation to Customer] | Webseite | Gibt die Anzahl der Punkte an, die ein Kunde erhält, der eine Einladung sendet, wenn der Empfänger dann ein Kundenkonto öffnet. |
| [!UICONTROL Invitation to Customer Conversions Quantity Limit] | Webseite | Begrenzt die Anzahl der Einladungskonversionen, die zum Verdienen von Punkten für den Kunden verwendet werden können, der die Einladung sendet. Lassen Sie das Feld leer, ohne Einschränkung. |
| [!UICONTROL Converting Invitation to Order] | Webseite | Gibt die Anzahl der Punkte an, die ein Kunde erhält, der eine Einladung sendet, wenn der Empfänger eine Erstbestellung aufgibt. |
| [!UICONTROL Invitation to Order Conversions Quantity Limit] | Webseite | Beschränkt die Anzahl der Bestellkonversionen, die Punkte für die Person sammeln können, die die Einladung sendet. Wenn leer, gibt es keine maximale Begrenzung. |
| [!UICONTROL Invitation Conversion to Order Reward] | Webseite | Gibt an, wie oft ein Kunde beim Kauf durch eingeladene Personen Punkte sammeln kann. Optionen: <br/>**`Each`**- Der Kunde erhält Belohnungspunkte für jede von der eingeladenen Person aufgegebene fakturierte Bestellung. Die Treuepunkte werden entsprechend den Wechselkursen festgelegt, die für die erforderliche Kombination aus einer Website und einer Kundengruppe festgelegt wurden.<br/>**`First`** - Der Kunde erhält nur für die erste von den eingeladenen Personen aufgegebene fakturierte Bestellung Belohnungspunkte. Wenn sich mehr als eine eingeladene Person registriert und eine Bestellung aufgibt, wird nur der Betrag der ersten Bestellung in Belohnungspunkte umgewandelt und dem Kunden gewährt. |
| [!UICONTROL Review Submission] | Webseite | Bestimmt die Anzahl der Punkte, die ein Kunde erhält, der eine für die Veröffentlichung genehmigte Überprüfung einreicht. |
| [!UICONTROL Rewarded Reviews Submission Quantity Limit] | Webseite | Begrenzt die Anzahl der Reviews, die verwendet werden können, um Punkte pro Kunde zu sammeln. Lassen Sie das Feld leer, ohne Einschränkung. |

{style="table-layout:auto"}

## [!UICONTROL Email Notification Settings]

![Einstellungen für E-Mail-Benachrichtigungen](./assets/reward-points-email-notification-settings.png)<!-- zoom -->

<!-- [Email Notification Settings](https://docs.magento.com/user-guide/marketing/reward-point-configure.html) -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Email Sender] | Store-Ansicht | Bestimmt den Store-Kontakt, der als Absender der E-Mail-Benachrichtigung zur Bilanzaktualisierung und zum Ablauf angezeigt wird. |
| [!UICONTROL Subscribe Customers by Default] | Global | Bestimmt den standardmäßigen Abonnementstatus von Kunden für E-Mails zu Kontoaktualisierungen und Ablaufbenachrichtigungen. |
| [!UICONTROL Balance Update Email] | Store-Ansicht | Legt die Vorlage fest, die für die Benachrichtigung verwendet wird, die an Kunden gesendet wird, wenn deren Punktstand aktualisiert wird. Standardvorlage: `Reward Points Balance Update` |
| [!UICONTROL Reward Points Expiry Warning Email] | Store-Ansicht | Bestimmt die Vorlage der E-Mail, die Kunden erhalten, wenn die Ablaufwarnungsbegrenzung für eine Reihe von Punkten erreicht wurde. Standardvorlage: `Reward Points Expiry Warning` |
| [!UICONTROL Expiry Warning before (days)] | Global | Gibt die Anzahl der Tage vor Ablauf des Punkts an, um die Benachrichtigung zu senden. Lassen Sie das Feld leer, um keine Ablaufbenachrichtigungen zu senden. Eine Benachrichtigung wird nicht gesendet, wenn die angegebene Anzahl von Tagen die verbleibende Lebensdauer der Punkte überschreitet. |

{style="table-layout:auto"}
