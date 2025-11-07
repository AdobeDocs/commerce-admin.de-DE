---
title: Prämien- und Treueprogramme
description: Erfahren Sie mehr über das Prämienpunktsystem, mit dem Sie die Kundeninteraktion fördern und die Kundenloyalität steigern können.
exl-id: 2bccdcce-7936-4449-9634-d463ad29e5cc
feature: Rewards, Promotions/Events, Customers, Configuration
source-git-commit: 7a505b1dc953286aa9879e77bd322d9681513096
workflow-type: tm+mt
source-wordcount: '1363'
ht-degree: 0%

---

# Prämien- und Treueprogramme

{{ee-feature}}

Das _Belohnungspunktesystem_ in Adobe Commerce bietet Ihnen die Möglichkeit, einzigartige Programme zu implementieren, die die Kundeninteraktion fördern und die Kundentreue fördern. Punkte können für eine Vielzahl von Transaktions- und Kundenaktivitäten vergeben werden, und die Konfiguration kann so festgelegt werden, dass sie die Punktzuteilung, den Saldo und den Ablauf steuert. Kunden können Punkte für Käufe einlösen, basierend auf dem Konversionsrate, den Sie zwischen Prämienpunkten und Währung festlegen.

## Preisregeln für Warenkorb

Punkte können Kunden auf der Grundlage einer [Warenkorbregel“ belohnt &#x200B;](price-rules-cart.md). Sie können als einzige Aktion der Preisregel oder zusammen mit einem Rabatt belohnt werden.

## Kundensaldo

Prämienpunkte können von Admin-Benutzern pro Kunde verwaltet werden. Wenn diese Option in der Storefront aktiviert ist, können Kunden auch die Details ihrer Punktebilanz anzeigen.

## Punkte einlösen

>[!NOTE]
>
>[Rewards-Wechselkurse](reward-exchange-rates.md) Die Konfiguration ist erforderlich, um Prämienpunkte von Kunden und Admin-Benutzern während des Checkouts einzulösen.

Punkte können von Admin-Benutzern und -Kunden (falls aktiviert) während des Checkouts eingelöst werden. Im Abschnitt Zahlungsmethode wird über den aktivierten Zahlungsmethoden das Kontrollkästchen „Meine Belohnungspunkte verwenden“ angezeigt. Die verfügbaren Punkte und der Geldwechselkurs sind enthalten. Ist der verfügbare Saldo größer als die Gesamtsumme der Bestellung, ist keine zusätzliche Zahlungsmethode erforderlich. Die Anzahl der Belohnungspunkte, die auf die Bestellung angewendet werden, wird mit den Bestellsummen angezeigt, die von der Gesamtsumme abgezogen werden, ähnlich wie bei Kredit- oder Geschenkkarten in einem Geschäft. Wenn Belohnungspunkte zusammen mit einem Gutschein oder einer Geschenkkarte verwendet werden, werden die Belohnungspunkte zuerst abgezogen. Die Store-Kredit- oder Geschenkkarte wird dann abgezogen, wenn die Bestellsumme größer ist als die einlösbare Anzahl an Belohnungspunkten.

>[!NOTE]
>
>Bonuspunkte werden nicht empfohlen, um bei Käufen per Nachnahme verwendet zu werden, da der Zahlungseingang erst bestätigt werden kann, nachdem die Bestellung in Rechnung gestellt wurde.

## Rückerstattung an Prämienpunkte

Bestellungen, die mit Prämienpunkten getätigt werden, können bis zu dem Betrag, der in der Bestellung eingelöst wurde, an die Prämienpunkte zurückerstattet werden. Auf der [_Neue Gutschrift_ &#x200B;](../stores-purchase/credit-memo-create.md) kann die Anzahl der Punkte eingegeben werden, die auf den Saldo des Kunden angewendet werden sollen. Standardmäßig enthält das Feld die vollständige Anzahl der Punkte, die in der Reihenfolge verwendet wurden.

## Belohnungspunkte-Vorgänge für Ihren Store aktivieren

Die Konfiguration der Belohnungspunkte bestimmt, wie Belohnungspunkte im Geschäft angezeigt werden, und definiert die grundlegenden Betriebsparameter.

![Kundenkonfiguration - Prämienpunkte](../configuration-reference/customers/assets/reward-points-reward-points.png){width="600" zoomable="yes"}

### Schritt 1. Konfigurieren der Belohnungspunkte

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Customers]** und wählen Sie **[!UICONTROL Reward Points]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Reward Points]** und führen Sie folgende Schritte aus:

   - Um Belohnungspunkte zu aktivieren, setzen Sie **[!UICONTROL Enable Reward Points Functionality]** auf `Yes`.

   - Damit Kundinnen und Kunden ihre eigenen Prämienpunkte sammeln können, setzen Sie **[!UICONTROL Enable Reward Points Functionality on Storefront]** auf `Yes`.

   - Damit Kunden einen detaillierten Verlauf ihrer Prämien sehen können, setzen Sie **[!UICONTROL Customers May See Reward Point History]** auf `Yes`.

1. Geben Sie **[!UICONTROL Reward Points Balance Redemption Threshold]** die Anzahl der Punkte ein, die anfallen müssen, bevor sie eingelöst werden können (leer für kein Minimum).

1. Geben Sie **[!UICONTROL Cap Reward Points Balance At]** die maximale Anzahl an Punkten ein, die ein Kunde sammeln kann (leer für keine Beschränkung).

1. Geben Sie **[!UICONTROL Reward Points Expire in (days)]** die Anzahl der Tage ein, nach denen die Belohnungspunkte ablaufen (leer, wenn sie nicht ablaufen).

1. Legen Sie **[!UICONTROL Reward Points Expiry Calculation]** auf eine der folgenden Einstellungen fest:

   - `Static` - Bestimmt die verbleibende Gültigkeitsdauer der Belohnungspunkte basierend auf der in der Konfiguration festgelegten Anzahl von Tagen. Wenn sich das Ablaufdatum in der Konfiguration ändert, ändert sich das Ablaufdatum der vorhandenen Punkte nicht.

   - `Dynamic` - Berechnet die verbleibende Anzahl von Tagen, wenn der Belohnungspunkt-Saldo erhöht wird. Wenn sich das Ablaufdatum in der Konfiguration ändert, wird das Ablaufdatum aller vorhandenen Punkte entsprechend aktualisiert.

1. Wenn Sie verfügbare Prämienpunkte automatisch zurückerstatten möchten, setzen Sie **[!UICONTROL Refund Reward Points Automatically]** auf `Yes`.

1. Um Prämienpunkte, die durch Käufe erzielt wurden, bei denen die Bestellung, bei der die Punkte gesammelt wurden, vollständig oder teilweise zurückerstattet wird, zu vermeiden, setzen Sie **[!UICONTROL Deduct Reward Points from Refund Amount Automatically]** auf `Yes`.

   >[!NOTE]
   >
   >Es sind nur die Punkte betroffen, die mit der zurückerstatteten Bestellung verdient wurden.

1. **[!UICONTROL Landing Page]** Sie auf die Inhaltsseite, auf der Ihr Prämienprogramm erläutert wird.

   Stellen Sie sicher, dass Sie die Standardseite für Prämienpunkte mit Ihren eigenen Informationen aktualisieren.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

### Schritt 2. Konfigurieren der für Kundenaktivitäten gesammelten Punkte

In diesem Schritt wird die Anzahl der Prämienpunkte festgelegt, die für verschiedene Kundenaktivitäten gesammelt werden können. Wenn Kundinnen und Kunden eine Aktion abgeschlossen haben, der Punkte zugewiesen sind, wird ihnen eine Meldung angezeigt, die angibt, wie viele Punkte sie verdient haben.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Actions for Acquiring Reward Points by Customer]** .

   ![Kundenkonfiguration - Aktionen zum Sammeln von Prämienpunkten nach Kunde](../configuration-reference/customers/assets/reward-points-actions-for-acquiring.png){width="600" zoomable="yes"}

1. Damit Belohnungspunkte für Käufe basierend auf den konfigurierten [Belohnungswechselkursen“ gesammelt werden können](reward-exchange-rates.md) legen Sie **[!UICONTROL Purchase]** auf `Yes` fest.

   >[!NOTE]
   >
   >Um Prämienpunkte für ihre _erste_ Bestellung zu sammeln, muss der Kunde registriert _bevor_ die Transaktion von der Zahlungsmethode erfasst wird. Die meisten Zahlungsmethoden können so konfiguriert werden, dass Transaktionen _automatisch_ erfasst werden, wenn die Bestellung aufgegeben wird, aber _vor_ die Registrierung des Kundenkontos abgeschlossen ist.

1. Geben Sie **[!UICONTROL Registration]** die Anzahl der Punkte ein, die für die Eröffnung eines Kundenkontos gesammelt wurden.

1. Geben Sie **[!UICONTROL Newsletter Signup]** die Anzahl der Punkte ein, die registrierte Kunden, die einen Newsletter abonnieren, verdient haben.

1. Geben Sie **[!UICONTROL Converting Invitation to Customer]** die Anzahl der Punkte ein, die ein Kunde, der eine Einladung sendet und der Empfänger dann ein Kundenkonto öffnet, verdient hat.

   Sie können die Anzahl der Einladungskonversionen begrenzen, mit denen Punkte für den Kunden gesammelt werden können, der die Einladung sendet (leer für „ohne Limit„). Geben Sie dazu eine Zahl in das **[!UICONTROL Invitation to Customer Conversions Quantity Limit]** ein.

1. Geben Sie **[!UICONTROL Converting Invitation to Order]** die Anzahl der Punkte ein, die ein Kunde verdient hat, der eine Einladung an den Empfänger sendet, der dann eine Bestellung aufgibt, und führen Sie folgende Schritte aus:

   - Geben **unter „Maximale Menge für Auftragskonversionen** die Anzahl der Punkte ein, die der Kunde verdient hat, der die Einladung sendet, wenn der Empfänger eine Erstbestellung aufgibt (leer für „Kein Limit„).

   - Wählen Sie **[!UICONTROL Invitation Conversion to Order Reward]** die Option `Each` aus, um Punkte für jede platzierte Bestellung zu sammeln, oder wählen Sie die Option `First` aus, um Punkte nur für die erste platzierte Bestellung durch den Empfänger zu sammeln.

1. Geben Sie **[!UICONTROL Review Submission]** die Anzahl der Punkte ein, die ein Kunde verdient hat, der eine zur Veröffentlichung genehmigte Überprüfung einreicht.

1. Um die Anzahl der Reviews zu begrenzen, mit denen pro Kunde Punkte gesammelt werden können, geben Sie die Zahl in das Feld **[!UICONTROL Rewarded Reviews Submission Quantity Limit]** ein (leer für „ohne Limit„).

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

### Schritt 3. E-Mail-Benachrichtigungseinstellungen vervollständigen

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Email Notification Settings]** .

   ![Kundenkonfiguration - E-Mail-Benachrichtigungen mit Prämienpunkten](../configuration-reference/customers/assets/reward-points-email-notification-settings.png){width="600" zoomable="yes"}

1. Legen Sie **[!UICONTROL Email Sender]** auf den Store-Kontakt fest, der als Absender von Saldoaktualisierungen und Ablaufbenachrichtigungen angezeigt wird.

1. Wenn Sie Kunden standardmäßig abonnieren möchten, um über Saldenaktualisierungen und bevorstehende Ablaufdaten benachrichtigt zu werden, setzen Sie **[!UICONTROL Subscribe Customers by Default]** auf `Yes`.

1. Legen Sie **[!UICONTROL Balance Update Email]** auf die Vorlage fest, die für die Benachrichtigung verwendet wird, die an Kunden gesendet wird, wenn ihr Punktesaldo aktualisiert wird.

1. Legen Sie **[!UICONTROL Reward Points Expiry Warning Email]** auf die Vorlage fest, die für die Benachrichtigung verwendet wird, die an Kunden gesendet wird, wenn das Ablauflimit für einen Satz von Punkten erreicht ist.

1. Geben Sie **[!UICONTROL Expiry Warning Before (days)]** die Anzahl der Tage vor Ablauf der Punkte ein, für die die Benachrichtigung gesendet wird.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

## Punktestand aktualisieren

Die Prämienpunktebilanz kann von der Administratorin bzw. dem Administrator aktualisiert werden.

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Suchen Sie den Kunden im Raster und klicken Sie in der Spalte **[!UICONTROL Edit]** auf _[!UICONTROL Action]_.

1. Wählen _unter „Kundeninformationen_ den Abschnitt **[!UICONTROL Reward Points]** aus.

1. Geben Sie die Anzahl der **[!UICONTROL Update Points]** ein:

   - Um den Betrag der Belohnungspunkte zu aktualisieren, geben Sie die Zahl ein, um den Gesamtpunktestand zu erhöhen.
   - Um den Betrag der Belohnungspunkte abzuziehen, geben Sie die negative Zahl ein, um den Gesamtpunktestand zu reduzieren.

1. Geben Sie bei Bedarf **[!UICONTROL Comments]** ein, die sich auf die Anpassung der Belohnungspunkte beziehen.

   ![Punktestand belohnen](./assets/reward-points-balance.png){width="700" zoomable="yes"}

1. Optional können Sie beim Kunden _Prämienpunkte-Benachrichtigungen_ abonnieren:

   - **[!UICONTROL Subscribe for Balance Updates]**
   - **[!UICONTROL Subscribe for Points Expiration Notifications]**

1. Klicken Sie auf **[!UICONTROL Save Customer]**.

Alle Aktionen im Zusammenhang mit Belohnungspunkten werden im _[!UICONTROL Reward Points History]_&#x200B;des Kunden in seinem Konto auf der Storefront angezeigt.

## Feldbeschreibungen

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Balance] | Aktueller Saldo der Prämienpunkte für Kunden |
| [!UICONTROL Amount Balance] | Der Betrag des aktuellen Barguthabens |
| [!UICONTROL Points] | Die Anzahl der hinzugefügten oder abgezogenen Punkte |
| [!UICONTROL Amount] | Zu- oder Abzuziehender Betrag |
| [!UICONTROL Rate] | Der [Belohnungs-Wechselkurs](reward-exchange-rates.md) |
| [!UICONTROL Website] | Website, der der Verlauf der Belohnungspunkte zugewiesen wird |
| [!UICONTROL Reason] | Gründe für die Vergabe von Punkten:<br>**[!UICONTROL Making purchases]**&#x200B;Jedes Mal, wenn ein Kunde einen Kauf tätigt, kann er Punkte sammeln.<br>**[!UICONTROL Registering on the site]** - Abgegrenzt bei der Registrierung (einmal).<br>**[!UICONTROL Subscribing to a newsletter]**: Für das Erstabonnement (einmal) anfallen.<br>**[!UICONTROL Sending Invitations]** — Sammeln Sie Punkte, indem Sie Ihre Freunde zur Teilnahme an der Website einladen.<br>**[!UICONTROL Converting Invitations to Customer]**- Sammeln Sie Punkte für jede Einladung, die sie an führende Freunde senden, die sich auf der Website registrieren.<br>**[!UICONTROL Converting Invitations to Order]** - Sammeln Sie Punkte für jeden Verkauf, der aus einer gesendeten Einladung resultiert.<br>**[!UICONTROL Review Submission]**- Sammeln Sie Punkte für die Einreichung von Produktbewertungen. |
| [!UICONTROL Created] | Datum und Uhrzeit der Aktualisierung der Prämienpunkte |
| [!UICONTROL Expired] | Anzahl abgelaufener Belohnungspunkte |
| [!UICONTROL Comment] | Kommentare beim Hinzufügen oder Subtrahieren von Punkten |

{style="table-layout:auto"}

