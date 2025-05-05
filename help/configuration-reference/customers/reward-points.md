---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Reward Points]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Customers] &gt; [!UICONTROL Reward Points] des Commerce Admin-Bereichs.
exl-id: 0b7f8806-74c5-4467-87da-0faae50f164b
feature: Configuration, Rewards
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '781'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Reward Points]

{{ee-feature}}

{{config}}

>[!NOTE]
>
>[Rewards-Wechselkurse](../../merchandising-promotions/reward-exchange-rates.md) Die Konfiguration ist erforderlich, um Prämienpunkte während des Checkouts von Kunden und Administratoren einlösen zu können.

## [!UICONTROL Reward Points]

![Belohnungspunkte](./assets/reward-points-reward-points.png)<!-- zoom -->

<!-- [Reward Points](https://experienceleague.adobe.com/de/docs/commerce-admin/marketing/merchandising/reward-points/rewards-loyalty#enable-reward-point-operations-for-your-store) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Reward Points Functionality] | Global | Aktiviert oder deaktiviert Belohnungspunkte. Optionen: `Yes` / `No`. |
| [!UICONTROL Enable Reward Points Functionality on Storefront] | Website | Wenn diese Option aktiviert ist, können Kunden durch ihre Aktivitäten Punkte sammeln und sie an der Kasse einlösen. Wenn diese Option deaktiviert ist, können nur Admin-Benutzer im Namen von Kunden Punkte zuweisen und einlösen. Optionen: `Yes` / `No`. |
| [!UICONTROL Customers May See Reward Points History] | Website | Wenn diese Option aktiviert ist, können Kunden einen detaillierten Verlauf mit jedem Ansammeln, Einlösen und Ablauf von Prämienpunkten in ihrem Konto-Dashboard einsehen. Optionen: `Yes` / `No` |
| [!UICONTROL Reward Points Balance Redemption Threshold] | Website | Erfordert, dass Kunden einen minimalen Punktesaldo erzielen, bevor sie sie für Bestellungen einlösen können. Leer lassen für kein Minimum. |
| [!UICONTROL Cap Reward Points Balance At] | Website | Verhindert, dass Kunden mehr als diesen maximalen Punktestand ansammeln. Leer lassen für kein Maximum. |
| [!UICONTROL Reward Points Expire in (days)] | Website | Gibt die Lebensdauer der Belohnungspunkte in Tagen an. Jeder Batch von Punkten, die während separater Aktivitäten gesammelt werden, hat eine separate Lebensdauer. Jeder Batch im Verlauf der Belohnungspunkte gibt die Anzahl der Tage an, die bis zum Ablauf der Punkte verbleiben. Der Verlauf kann im Konto-Dashboard des Kunden eingesehen werden, falls aktiviert, und im Admin-Bereich. Leer lassen für keinen Ablauf. |
| [!UICONTROL Reward Points Expiry Calculation] | Website | Bestimmt die Methode, mit der bestimmt wird, wann Belohnungspunkte ablaufen. Optionen: <br/>**`Static`**- Bestimmt die verbleibende Gültigkeitsdauer der Belohnungspunkte basierend auf der in der Konfiguration festgelegten Anzahl von Tagen. Wenn sich das Ablaufdatum in der Konfiguration ändert, ändert sich das Ablaufdatum der vorhandenen Punkte nicht.<br/>**`Dynamic`** - Berechnet die Anzahl der verbleibenden Tage, wenn der Belohnungspunkt-Saldo steigt. Wenn sich das Ablauflimit in der Konfiguration ändert, werden die Ablaufberechnungen für alle vorhandenen Punkte entsprechend aktualisiert. |
| [!UICONTROL Refund Reward Points Automatically] | Global | Legt fest, ob verfügbare Belohnungspunkte automatisch zurückerstattet werden. Optionen: `Yes` / `No` |
| [!UICONTROL Deduct Reward Points from Refund Amount Automatically] | Global | Dadurch wird bestimmt, ob durch Käufe erworbene Prämienpunkte bei der Bestellrückerstattung vollständig oder teilweise storniert werden, wenn diese Funktion aktiviert ist. Nur Prämienpunkte aus der Bestellung, die sie verdient haben, sind betroffen, wenn diese Bestellung zurückerstattet wird. Optionen: `Yes` / `No`. |
| [!UICONTROL Landing Page] | Shop-Ansicht | Gibt die CMS-Seite an, auf der Ihr Prämienprogramm erläutert wird. Ein Link zur Standardseite für Prämien wird an den Stellen in Ihrem Geschäft angezeigt, an denen Punkte gesammelt werden können. |

{style="table-layout:auto"}

## [!UICONTROL Actions for Acquiring Reward Points by Customers]

![Aktionen zum Sammeln von Prämienpunkten durch Kunden](./assets/reward-points-actions-for-acquiring.png)<!-- zoom -->

<!-- [Actions for Acquiring Reward Points by Customers](https://experienceleague.adobe.com/de/docs/commerce-admin/marketing/merchandising/reward-points/rewards-loyalty#enable-reward-point-operations-for-your-store) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Purchase] | Website | Legt fest, ob Belohnungspunkte für Käufe basierend auf den konfigurierten [Belohnungswechselkursen](../../merchandising-promotions/reward-exchange-rates.md) verdient werden. Optionen: `Yes` / `No` |
| [!UICONTROL Registration] | Website | Gibt die Anzahl der Punkte an, die für die Eröffnung eines Kundenkontos gesammelt wurden. |
| [!UICONTROL Newsletter Signup] | Website | Gibt die Anzahl der Punkte an, die registrierte Kundinnen und Kunden, die einen Newsletter abonnieren, verdient haben. (Für Abonnements von Gästen stehen keine Punkte zur Verfügung.) Wenn sich ein Kunde abmeldet und sich dann erneut abmeldet, werden für das zweite Abonnement keine Punkte verdient. |
| [!UICONTROL Converting Invitation to Customer] | Website | Gibt die Anzahl der Punkte an, die ein Kunde, der eine Einladung sendet, verdient, wenn der Empfänger dann ein Kundenkonto öffnet. |
| [!UICONTROL Invitation to Customer Conversions Quantity Limit] | Website | Beschränkt die Anzahl der Einladungskonversionen, mit denen Punkte für den Kunden gesammelt werden können, der die Einladung sendet. Leer lassen für keine Beschränkung. |
| [!UICONTROL Converting Invitation to Order] | Website | Gibt die Anzahl der Punkte an, die ein Kunde verdient hat, der eine Einladung sendet, wenn der Empfänger eine Erstbestellung aufgibt. |
| [!UICONTROL Invitation to Order Conversions Quantity Limit] | Website | Beschränkt die Anzahl der Auftragskonversionen, die Punkte für die Person sammeln können, die die Einladung sendet. Wenn dieses Feld leer ist, gibt es keine Obergrenze. |
| [!UICONTROL Invitation Conversion to Order Reward] | Website | Gibt an, wie oft eine Kundin oder ein Kunde Prämienpunkte sammeln kann, wenn Einladende Käufe tätigen. Optionen: <br/>**`Each`**- Der Kunde erhält Prämienpunkte für jede vom Einladenden aufgegebene und in Rechnung gestellte Bestellung. Prämienpunkte werden entsprechend den Wechselkursen vergeben, die für die erforderliche Kombination aus einer Website und einer Kundengruppe festgelegt wurden.<br/>**`First`** - Der Kunde erhält Prämienpunkte nur für die erste fakturierte Bestellung, die von den Eingeladenen aufgegeben wurde. Wenn sich mehr als ein Einladender registriert und eine Bestellung aufgibt, wird nur der Betrag der ersten Bestellung in Prämienpunkte umgewandelt und dem Kunden gewährt. |
| [!UICONTROL Review Submission] | Website | Bestimmt die Anzahl der Punkte, die eine Kundin oder ein Kunde verdient, die bzw. der eine zur Veröffentlichung genehmigte Überprüfung einreicht. |
| [!UICONTROL Rewarded Reviews Submission Quantity Limit] | Website | Beschränkt die Anzahl der Reviews, mit denen pro Kunde Punkte gesammelt werden können. Leer lassen für keine Beschränkung. |

{style="table-layout:auto"}

## [!UICONTROL Email Notification Settings]

![E-Mail-Benachrichtigungseinstellungen](./assets/reward-points-email-notification-settings.png)<!-- zoom -->

<!-- [Email Notification Settings](https://experienceleague.adobe.com/de/docs/commerce-admin/marketing/merchandising/reward-points/rewards-loyalty#enable-reward-point-operations-for-your-store) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Email Sender] | Shop-Ansicht | Bestimmt den Store-Kontakt, der als Absender der E-Mails zur Aktualisierung des Saldos und zur Benachrichtigung über den Ablauf angezeigt wird. |
| [!UICONTROL Subscribe Customers by Default] | Global | Bestimmt den Standardabonnement-Status von Kunden für E-Mails zur Aktualisierung von Salden und zur Gültigkeitsdauer. |
| [!UICONTROL Balance Update Email] | Shop-Ansicht | Legt die Vorlage für die Benachrichtigung fest, die Kunden bei jeder Aktualisierung ihres Punktesaldos gesendet wird. Standardvorlage: `Reward Points Balance Update` |
| [!UICONTROL Reward Points Expiry Warning Email] | Shop-Ansicht | Bestimmt die Vorlage der E-Mail, die Kundinnen und Kunden erhalten, wenn das Ablaufwarnlimit für einen Satz von Punkten erreicht wurde. Standardvorlage: `Reward Points Expiry Warning` |
| [!UICONTROL Expiry Warning before (days)] | Global | Gibt die Anzahl der Tage vor Ablauf des Punkts an, an die die Benachrichtigung gesendet werden soll. Lassen Sie das Feld leer, um keine Ablaufbenachrichtigungen zu senden. Eine Benachrichtigung wird nicht gesendet, wenn die Anzahl der eingegebenen Tage größer ist als die restliche Lebensdauer der Punkte. |

{style="table-layout:auto"}
