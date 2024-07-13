---
title: Lohn- und Treueprogramme
description: Erfahren Sie mehr über das Bonuspunktsystem, mit dem Sie die Kundeninteraktion fördern und die Kundenloyalität fördern können.
exl-id: 2bccdcce-7936-4449-9634-d463ad29e5cc
feature: Rewards, Promotions/Events, Customers, Configuration
source-git-commit: 3376b6f4fd558f7dd10133beeabf87e7228776a1
workflow-type: tm+mt
source-wordcount: '1395'
ht-degree: 0%

---

# Lohn- und Treueprogramme

{{ee-feature}}

Mit dem System _Bonuspunkte_ in Adobe Commerce können Sie eindeutige Programme implementieren, die die Kundeninteraktion fördern und die Kundenloyalität fördern. Punkte können für eine breite Palette von Transaktions- und Kundenaktivitäten vergeben werden. Die Konfiguration kann so konfiguriert werden, dass sie die Punktzahl, die Balance und den Ablauf steuert. Kunden können Punkte in Bezug auf Käufe einlösen, basierend auf dem Konversionskurs, den Sie zwischen Belohnungspunkten und Währung einrichten.

## Preisregeln für Warenkorb

Punkte können Kunden anhand einer [Warenkorbregel](price-rules-cart.md) belohnt werden. Sie können als einzige Aktion der Preisregel oder zusammen mit einem Rabatt belohnt werden.

## Kundenkonto

Prämienpunktbilanzen können von Admin-Benutzern pro Kunde verwaltet werden. Wenn diese Option in der Storefront aktiviert ist, können Kunden auch die Details ihres Punktstandes anzeigen.

## Ersetzungspunkte

>[!NOTE]
>
>Die Konfiguration der Rewards-Wechselkurse ](reward-exchange-rates.md) ist erforderlich, damit Kunden und Admin-Benutzer während des Checkout die Punkte einlösen können.[

Punkte können von Admin-Benutzern und -Kunden beim Checkout eingelöst werden (sofern aktiviert). Im Abschnitt Zahlungsmethode wird oberhalb der aktivierten Zahlungsmethoden das Kontrollkästchen Meine Prämienpunkte verwenden angezeigt. Die verfügbaren Punkte und der Währungskurs sind eingeschlossen. Wenn der verfügbare Restbetrag die Gesamtsumme der Bestellung übersteigt, ist keine zusätzliche Zahlungsmethode erforderlich. Die Anzahl der auf die Bestellung angewendeten Bonuspunkte wird mit den Gesamtbestellungen angezeigt, die von der Gesamtsumme abgezogen werden, ähnlich wie bei einer Kredit- oder Geschenkkarte im Geschäft. Wenn Prämienpunkte zusammen mit einer Gutschrift oder einer Geschenkkarte verwendet werden, werden die Prämienpunkte zuerst abgezogen. Die Kredit- oder Geschenkkarte wird dann abgezogen, wenn die Bestellsumme die einlösbare Anzahl von Prämienpunkten übersteigt.

>[!NOTE]
>
>Für die Verwendung mit CSB-Käufen werden keine Prämienpunkte empfohlen, da der Zahlungseingang erst nach Rechnungsstellung bestätigt werden kann.

## Rückerstattung an Prämienpunkte

Bestellungen mit Prämienpunkten können bis zu dem in der Bestellung eingelösten Betrag an die Prämienpunkte zurückerstattet werden. Auf der Seite [_New Credit Memo_](../stores-purchase/credit-memo-create.md) kann die Anzahl der Punkte eingegeben werden, die auf den Kundensaldo angewendet werden sollen. Standardmäßig enthält das Feld die vollständige Anzahl der Punkte, die in der Reihenfolge verwendet wurden.

## Aktivieren von Belohnungspunktvorgängen für Ihren Store

Die Rewards-Punktkonfiguration bestimmt, wie im Store Prämienpunkte angezeigt werden, und definiert die grundlegenden Betriebsparameter.

![Kundenkonfiguration - Belohnungspunkte](../configuration-reference/customers/assets/reward-points-reward-points.png){width="600" zoomable="yes"}

### Schritt 1. Belohnungspunkte konfigurieren

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Customers]** und wählen Sie **[!UICONTROL Reward Points]** aus.

1. Erweitern Sie den Abschnitt **[!UICONTROL Reward Points]** des Erweiterungsselektors ![Erweiterung](../assets/icon-display-expand.png) und führen Sie folgende Schritte aus:

   - Um Belohnungspunkte zu aktivieren, setzen Sie **[!UICONTROL Enable Reward Points Functionality]** auf `Yes`.

   - Setzen Sie **[!UICONTROL Enable Reward Points Functionality on Storefront]** auf `Yes`, damit Kunden ihre eigenen Bonuspunkte sammeln können.

   - Damit Kunden einen detaillierten Verlauf ihrer Belohnungen sehen können, setzen Sie **[!UICONTROL Customers May See Reward Point History]** auf `Yes`.

1. Geben Sie für &quot;**[!UICONTROL Reward Points Balance Redemption Threshold]**&quot;die Anzahl der Punkte ein, die gesammelt werden müssen, bevor sie eingelöst werden können (kein Minimum).

1. Geben Sie für &quot;**[!UICONTROL Cap Reward Points Balance At]**&quot;die maximale Anzahl von Punkten ein, die ein Kunde sammeln kann (leer für keine Begrenzung).

1. Geben Sie für **[!UICONTROL Reward Points Expire in (days)]** die Anzahl der Tage ein, bevor die Belohnungspunkte ablaufen (leer für keinen Ablauf).

1. Setzen Sie **[!UICONTROL Reward Points Expiry Calculation]** auf einen der folgenden Werte:

   - `Static` - Bestimmt die verbleibende Lebensdauer der Belohnungspunkte anhand der in der Konfiguration festgelegten Anzahl von Tagen. Wenn sich das Ablaufdatum in der Konfiguration ändert, ändert sich das Ablaufdatum vorhandener Punkte nicht.

   - `Dynamic` - Berechnet die verbleibende Anzahl von Tagen, wenn sich der Saldo des Belohnungspunkts erhöht. Wenn sich das Ablauflimit in der Konfiguration ändert, wird der Ablauf aller vorhandenen Punkte entsprechend aktualisiert.

1. Wenn Sie verfügbare Prämienpunkte automatisch zurückerstatten möchten, setzen Sie **[!UICONTROL Refund Reward Points Automatically]** auf `Yes`.

1. Setzen Sie **[!UICONTROL Deduct Reward Points from Refund Amount Automatically]** auf `Yes`, um durch Käufe verdiente Bonuspunkte zu vermeiden, wenn die Bestellung, die die Punkte gesammelt hat, vollständig oder teilweise zurückerstattet wird.

   >[!NOTE]
   >
   >Nur die Punkte, die mit der Bestellung verdient werden, die zurückerstattet wird, sind betroffen.

1. Setzen Sie **[!UICONTROL Landing Page]** auf die Inhaltsseite, auf der Ihr Prämienpunktprogramm erläutert wird.

   Aktualisieren Sie unbedingt die standardmäßige Seite mit den Rewards-Punkten mit Ihren eigenen Informationen.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

### Schritt 2. Erfasste Punkte für Kundenaktivitäten konfigurieren

In diesem Schritt wird die Anzahl der Belohnungspunkte angegeben, die für verschiedene Kundenaktivitäten verdient werden können. Wenn Kunden eine Aktion ausführen, der Punkte zugewiesen sind, wird dem Kunden eine Meldung angezeigt, die angibt, wie viele Punkte er gesammelt hat.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Actions for Acquiring Reward Points by Customer]** .

   ![Kundenkonfiguration - Aktionen zum Erwerb von Prämienpunkten durch Kunden](../configuration-reference/customers/assets/reward-points-actions-for-acquiring.png){width="600" zoomable="yes"}

1. Setzen Sie **[!UICONTROL Purchase]** auf `Yes`, damit Belohnungspunkte für die Käufe basierend auf den konfigurierten [Belohnungskursen](reward-exchange-rates.md) gesammelt werden können.

   >[!NOTE]
   >
   >Um Belohnungspunkte für ihre _erste_ Bestellung zu erhalten, muss der Kunde _vor_ registriert sein, bevor die Transaktion von der Zahlungsmethode erfasst wird. Die meisten Zahlungsmethoden können so konfiguriert werden, dass Transaktionen _automatisch_ erfasst werden, wenn die Bestellung aufgegeben wird, aber _vor_ die Registrierung des Kundenkontos abgeschlossen ist.

1. Geben Sie für &quot;**[!UICONTROL Registration]**&quot;die Anzahl der Punkte ein, die Sie für die Eröffnung eines Kundenkontos erhalten haben.

1. Geben Sie für &quot;**[!UICONTROL Newsletter Signup]**&quot;die Anzahl der Punkte ein, die von registrierten Kunden, die einen Newsletter abonnieren, gesammelt wurden.

1. Geben Sie für &quot;**[!UICONTROL Converting Invitation to Customer]**&quot;die Anzahl der Punkte ein, die ein Kunde erhält, der eine Einladung sendet, und der Empfänger öffnet dann ein Kundenkonto.

   Sie können die Anzahl der Einladungskonversionen einschränken, mit denen Punkte für den Kunden gesammelt werden können, der die Einladung sendet (leer, wenn kein Limit vorhanden ist). Geben Sie dazu eine Zahl in das Feld **[!UICONTROL Invitation to Customer Conversions Quantity Limit]** ein.

1. Geben Sie für &quot;**[!UICONTROL Converting Invitation to Order]**&quot;die Anzahl der Punkte ein, die ein Kunde erhält, der eine Einladung an den Empfänger sendet, der dann eine Bestellung aufgibt, und führen Sie die folgenden Schritte aus:

   - Geben Sie für **Mengenbegrenzung für Einladung zur Bestellungsumrechnung** die Anzahl der Punkte ein, die der Kunde beim Versand der Einladung erhalten hat, wenn der Empfänger eine Erstbestellung aufgibt (ohne Begrenzung leer).

   - Wählen Sie für **[!UICONTROL Invitation Conversion to Order Reward]** die Option `Each` aus, um Punkte für jede platzierte Empfängerreihenfolge zu sammeln, oder wählen Sie die Option `First` , um nur Punkte für die erste platzierte Bestellung des Empfängers zu sammeln.

1. Geben Sie für &quot;**[!UICONTROL Review Submission]**&quot;die Anzahl der Punkte ein, die ein Kunde erhält, der einen zur Veröffentlichung genehmigten Review sendet.

1. Geben Sie dann die Zahl in das Feld **[!UICONTROL Rewarded Reviews Submission Quantity Limit]** ein, um die Anzahl der Reviews zu begrenzen, die zum Sammeln von Punkten pro Kunde verwendet werden können (leer für keine Begrenzung).

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

### Schritt 3. E-Mail-Benachrichtigungseinstellungen abschließen

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Email Notification Settings]** .

   ![Kundenkonfiguration - E-Mail-Benachrichtigungen zu Rewards-Punkten](../configuration-reference/customers/assets/reward-points-email-notification-settings.png){width="600" zoomable="yes"}

1. Setzen Sie **[!UICONTROL Email Sender]** auf den Store-Kontakt, der als Absender von Bilanzaktualisierungen und Ablaufbenachrichtigungen angezeigt wird.

1. Wenn Sie Kunden abonnieren möchten, die standardmäßig über Bilanzaktualisierungen und bevorstehende Ablaufdaten informiert werden sollen, setzen Sie **[!UICONTROL Subscribe Customers by Default]** auf `Yes`.

1. Setzen Sie **[!UICONTROL Balance Update Email]** auf die Vorlage, die für die Benachrichtigung verwendet wird, die an Kunden gesendet wird, wenn deren Punktstand aktualisiert wird.

1. Setzen Sie **[!UICONTROL Reward Points Expiry Warning Email]** auf die Vorlage, die für die Benachrichtigung verwendet wird, die an Kunden gesendet wird, wenn das Ablauflimit für einen Punktstapel erreicht ist.

1. Geben Sie für &quot;**[!UICONTROL Expiry Warning Before (days)]**&quot;die Anzahl der Tage ein, bevor Punkte ablaufen, an die die Benachrichtigung gesendet wird.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

## Aktualisieren des Saldos der belohnten Punkte

Der Saldo der Prämienpunkte kann vom Administrator aktualisiert werden.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Suchen Sie den Kunden im Raster und klicken Sie in der Spalte _[!UICONTROL Action]_auf **[!UICONTROL Edit]**.

1. Wählen Sie unter _Kundeninformationen_ den Abschnitt **[!UICONTROL Reward Points]** aus.

1. Geben Sie die Nummer **[!UICONTROL Update Points]** ein:

   - Um den Betrag der Belohnungspunkte zu aktualisieren, geben Sie die Zahl ein, um den Saldo der Gesamtpunkte zu erhöhen.
   - Geben Sie die negative Zahl ein, um die Summe der Punkte zu reduzieren.

1. Geben Sie bei Bedarf **[!UICONTROL Comments]** für die Anpassung der Belohnungspunkte ein.

   ![Guthaben-Punkte-Saldo](./assets/reward-points-balance.png){width="700" zoomable="yes"}

1. Abonnieren Sie optional den Kunden für _Bonuspunkte-Benachrichtigungen_:

   - **[!UICONTROL Subscribe for Balance Updates]**
   - **[!UICONTROL Subscribe for Points Expiration Notifications]**

1. Klicken Sie auf **[!UICONTROL Save Customer]**.

Alle Aktionen im Zusammenhang mit Prämienpunkten werden im Block _[!UICONTROL Reward Points History]_des Kunden in seinem Konto auf der Storefront angezeigt.

## Feldbeschreibungen

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Balance] | Aktuelle Bilanzsumme der Kundenprämien |
| [!UICONTROL Amount Balance] | Betrag des aktuellen Zahlungsbilanzsaldos |
| [!UICONTROL Points] | Die Anzahl der hinzugefügten oder subtraktierten Punkte |
| [!UICONTROL Amount] | Zugeschlagener oder subtraktierter Geldbetrag |
| [!UICONTROL Rate] | Der [Belohnungskurs](reward-exchange-rates.md) |
| [!UICONTROL Website] | Website, der der Verlauf der Belohnungspunkte zugewiesen wurde |
| [!UICONTROL Reason] | Gründe für die Punktzahl:<br>**[!UICONTROL Making purchases]**- Jedes Mal, wenn der Kunde einen Kauf tätigt, kann er Punkte sammeln.<br>**[!UICONTROL Registering on the site]** - Bei der Registrierung angehoben (einmal).<br>**[!UICONTROL Subscribing to a newsletter]**- Für das erste Abonnement (einmal) erfasst.<br>**[!UICONTROL Sending Invitations]** - Verdienen Sie Punkte, indem Sie ihre Freunde einladen, der Site beizutreten.<br>**[!UICONTROL Converting Invitations to Customer]**- Sammeln Sie Punkte für jede Einladung, die sie versenden, und führen Sie führende Freunde ein, die sich auf der Site registrieren.<br>**[!UICONTROL Converting Invitations to Order]** - Sammeln Sie Punkte für jeden Verkauf, der aus einer gesendeten Einladung resultiert.<br>**[!UICONTROL Review Submission]**- Sammeln Sie Punkte für die Übermittlung von Produktüberprüfungen. |
| [!UICONTROL Created] | Datum und Uhrzeit der Aktualisierung der Bonuspunkte |
| [!UICONTROL Expired] | Anzahl abgelaufener Bonuspunkte |
| [!UICONTROL Comment] | Kommentare beim Hinzufügen oder Abziehen von Punkten |

{style="table-layout:auto"}

## Fehlerbehebung bei Ressourcen

Hilfe zur Fehlerbehebung bei Problemen mit belohnten Punkten finden Sie in den folgenden Artikeln der Commerce Support Knowledge Base:

- [Treuepunkte bei partiellen Bestellungen](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-8/mdva-31295-magento-patch-loyalty-points-on-partial-orders.html)
- [404-Fehler - Entfernen von Belohnungspunkten beim Checkout mit mehreren Sendungen](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/storefront/magento-2.4.0-404-error-removing-rewards-points-on-multi-shipping-checkout.html)
