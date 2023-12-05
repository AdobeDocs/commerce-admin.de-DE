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

Die _Belohnungspunkte_ -System in Adobe Commerce bietet Ihnen die Möglichkeit, einzigartige Programme zu implementieren, die die Kundeninteraktion fördern und die Kundentreue fördern. Punkte können für eine breite Palette von Transaktions- und Kundenaktivitäten vergeben werden. Die Konfiguration kann so konfiguriert werden, dass sie die Punktzahl, die Balance und den Ablauf steuert. Kunden können Punkte in Bezug auf Käufe einlösen, basierend auf dem Konversionskurs, den Sie zwischen Belohnungspunkten und Währung einrichten.

## Preisregeln für Warenkorb

Punkte können Kunden auf der Grundlage einer [Warenkorbregel](price-rules-cart.md). Sie können als einzige Aktion der Preisregel oder zusammen mit einem Rabatt belohnt werden.

## Kundenkonto

Prämienpunktbilanzen können von Admin-Benutzern pro Kunde verwaltet werden. Wenn diese Option in der Storefront aktiviert ist, können Kunden auch die Details ihres Punktstandes anzeigen.

## Ersetzungspunkte

>[!NOTE]
>
>[Wechselkurse der Prämien](reward-exchange-rates.md) -Konfiguration ist erforderlich, damit Kunden und Admin-Benutzer während des Checkout die Punkte einlösen können.

Punkte können von Admin-Benutzern und -Kunden beim Checkout eingelöst werden (sofern aktiviert). Im Abschnitt Zahlungsmethode wird oberhalb der aktivierten Zahlungsmethoden das Kontrollkästchen Meine Prämienpunkte verwenden angezeigt. Die verfügbaren Punkte und der Währungskurs sind eingeschlossen. Wenn der verfügbare Restbetrag die Gesamtsumme der Bestellung übersteigt, ist keine zusätzliche Zahlungsmethode erforderlich. Die Anzahl der auf die Bestellung angewendeten Bonuspunkte wird mit den Gesamtbestellungen angezeigt, die von der Gesamtsumme abgezogen werden, ähnlich wie bei einer Kredit- oder Geschenkkarte im Geschäft. Wenn Prämienpunkte zusammen mit einer Gutschrift oder einer Geschenkkarte verwendet werden, werden die Prämienpunkte zuerst abgezogen. Die Kredit- oder Geschenkkarte wird dann abgezogen, wenn die Bestellsumme die einlösbare Anzahl von Prämienpunkten übersteigt.

>[!NOTE]
>
>Für die Verwendung mit CSB-Käufen werden keine Prämienpunkte empfohlen, da der Zahlungseingang erst nach Rechnungsstellung bestätigt werden kann.

## Rückerstattung an Prämienpunkte

Bestellungen mit Prämienpunkten können bis zu dem in der Bestellung eingelösten Betrag an die Prämienpunkte zurückerstattet werden. Im [_Neues Credit Memo_ page](../stores-purchase/credit-memo-create.md), kann die Anzahl der Punkte angegeben werden, die auf den Kundenstand angewendet werden sollen. Standardmäßig enthält das Feld die vollständige Anzahl der Punkte, die in der Reihenfolge verwendet wurden.

## Aktivieren von Belohnungspunktvorgängen für Ihren Store

Die Rewards-Punktkonfiguration bestimmt, wie im Store Prämienpunkte angezeigt werden, und definiert die grundlegenden Betriebsparameter.

![Kundenkonfiguration - Prämienpunkte](../configuration-reference/customers/assets/reward-points-reward-points.png){width="600" zoomable="yes"}

### Schritt 1. Belohnungspunkte konfigurieren

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Customers]** und wählen **[!UICONTROL Reward Points]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Reward Points]** und führen Sie folgende Schritte aus:

   - Um Belohnungspunkte zu aktivieren, legen Sie **[!UICONTROL Enable Reward Points Functionality]** nach `Yes`.

   - Um Kunden die Möglichkeit zu geben, ihre eigenen Bonuspunkte zu sammeln, legen Sie **[!UICONTROL Enable Reward Points Functionality on Storefront]** nach `Yes`.

   - Damit Kunden einen detaillierten Verlauf ihrer Belohnungen sehen können, legen Sie **[!UICONTROL Customers May See Reward Point History]** nach `Yes`.

1. Für **[!UICONTROL Reward Points Balance Redemption Threshold]**, geben Sie die Anzahl der Punkte ein, die gesammelt werden müssen, bevor sie eingelöst werden können (kein Minimum).

1. Für **[!UICONTROL Cap Reward Points Balance At]** Geben Sie die maximale Anzahl von Punkten ein, die ein Kunde sammeln kann (leer für keine Begrenzung).

1. Für **[!UICONTROL Reward Points Expire in (days)]** geben Sie die Anzahl der Tage ein, bevor die Belohnungspunkte ablaufen (ohne Ablaufdatum).

1. Satz **[!UICONTROL Reward Points Expiry Calculation]** auf einen der folgenden Werte zu:

   - `Static` - Bestimmt die verbleibende Lebensdauer der Bonuspunkte basierend auf der in der Konfiguration festgelegten Anzahl von Tagen. Wenn sich das Ablaufdatum in der Konfiguration ändert, ändert sich das Ablaufdatum vorhandener Punkte nicht.

   - `Dynamic` - Berechnet die verbleibende Anzahl von Tagen, wenn sich der Saldo des Bonuspunkts erhöht. Wenn sich das Ablauflimit in der Konfiguration ändert, wird der Ablauf aller vorhandenen Punkte entsprechend aktualisiert.

1. Wenn Sie verfügbare Prämienpunkte automatisch zurückerstatten möchten, legen Sie **[!UICONTROL Refund Reward Points Automatically]** nach `Yes`.

1. Um durch Käufe verdiente Bonuspunkte zu vermeiden, wenn die Bestellung, die die Punkte gesammelt hat, vollständig oder teilweise zurückerstattet wird, legen Sie **[!UICONTROL Deduct Reward Points from Refund Amount Automatically]** nach `Yes`.

   >[!NOTE]
   >
   >Nur die Punkte, die mit der Bestellung verdient werden, die zurückerstattet wird, sind betroffen.

1. Satz **[!UICONTROL Landing Page]** auf die Inhaltsseite, auf der Ihr Bonuspunkt-Programm erläutert wird.

   Aktualisieren Sie unbedingt die standardmäßige Seite mit den Rewards-Punkten mit Ihren eigenen Informationen.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

### Schritt 2. Erfasste Punkte für Kundenaktivitäten konfigurieren

In diesem Schritt wird die Anzahl der Belohnungspunkte angegeben, die für verschiedene Kundenaktivitäten verdient werden können. Wenn Kunden eine Aktion ausführen, der Punkte zugewiesen sind, wird dem Kunden eine Meldung angezeigt, die angibt, wie viele Punkte er gesammelt hat.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Actions for Acquiring Reward Points by Customer]** Abschnitt.

   ![Kundenkonfiguration - Aktionen zum Erwerb von Prämienpunkten durch Kunden](../configuration-reference/customers/assets/reward-points-actions-for-acquiring.png){width="600" zoomable="yes"}

1. So lassen Sie Belohnungspunkte für die Käufe basierend auf der konfigurierten [Wechselkurse der Prämien](reward-exchange-rates.md), set **[!UICONTROL Purchase]** nach `Yes`.

   >[!NOTE]
   >
   >So verdienen Sie Belohnungspunkte für ihre _first_ Bestellung, muss der Kunde registriert sein _before_ die Transaktion wird von der Zahlungsmethode erfasst. Die meisten Zahlungsmethoden können zur Erfassung von Transaktionen konfiguriert werden _automatisch_ wann die Bestellung aufgegeben wird, aber _before_ die Registrierung des Kundenkontos abgeschlossen ist.

1. Für **[!UICONTROL Registration]**, geben Sie die Anzahl der Punkte ein, die Sie für die Eröffnung eines Kundenkontos erhalten haben.

1. Für **[!UICONTROL Newsletter Signup]** Geben Sie die Anzahl der Punkte ein, die registrierte Kunden, die einen Newsletter abonnieren, gesammelt haben.

1. Für **[!UICONTROL Converting Invitation to Customer]** Geben Sie die Anzahl der Punkte ein, die ein Kunde erhält, der eine Einladung versendet, und der Empfänger öffnet dann ein Kundenkonto.

   Sie können die Anzahl der Einladungskonversionen einschränken, mit denen Punkte für den Kunden gesammelt werden können, der die Einladung sendet (leer, wenn kein Limit vorhanden ist). Geben Sie dazu eine Zahl im **[!UICONTROL Invitation to Customer Conversions Quantity Limit]** -Feld.

1. Für **[!UICONTROL Converting Invitation to Order]** Geben Sie die Anzahl der Punkte ein, die ein Kunde erhält, der eine Einladung an den Empfänger sendet, der dann eine Bestellung aufgibt, und führen Sie folgende Schritte aus:

   - Für **Mengenbegrenzung für Einladung zur Bestellungsumrechnung**, geben Sie die Anzahl der Punkte ein, die der Kunde, der die Einladung verschickt hat, bei der ersten Bestellung des Empfängers gesammelt hat (leer für keine Begrenzung).

   - Für **[!UICONTROL Invitation Conversion to Order Reward]**, wählen Sie die `Each` Option, um Punkte für jede platzierte Bestellung zu sammeln, oder wählen Sie die `First` -Option, um Punkte nur für die erste Bestellung des Empfängers zu sammeln.

1. Für **[!UICONTROL Review Submission]** eingeben, geben Sie die Anzahl der Punkte ein, die ein Kunde erhält, der eine für die Veröffentlichung genehmigte Überprüfung einreicht.

1. Geben Sie dann die Anzahl der Überprüfungen ein, die zum Sammeln von Punkten pro Kunde verwendet werden können, um die Anzahl der Bewertungen in die **[!UICONTROL Rewarded Reviews Submission Quantity Limit]** -Feld (leer für keine Begrenzung).

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

### Schritt 3. E-Mail-Benachrichtigungseinstellungen abschließen

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Email Notification Settings]** Abschnitt.

   ![Kundenkonfiguration - E-Mail-Benachrichtigungen zu Prämienpunkten](../configuration-reference/customers/assets/reward-points-email-notification-settings.png){width="600" zoomable="yes"}

1. Satz **[!UICONTROL Email Sender]** an den Store-Kontakt, der als Absender von Bilanzaktualisierungen und Ablaufbenachrichtigungen erscheint.

1. Wenn Sie Kunden abonnieren möchten, die standardmäßig über Bilanzaktualisierungen und bevorstehende Ablaufdaten informiert werden sollen, legen Sie **[!UICONTROL Subscribe Customers by Default]** nach `Yes`.

1. Satz **[!UICONTROL Balance Update Email]** der Vorlage, die für die Benachrichtigung verwendet wird, die den Kunden bei jeder Aktualisierung ihrer Punktzahl gesendet wird.

1. Satz **[!UICONTROL Reward Points Expiry Warning Email]** der Vorlage, die für die Benachrichtigung verwendet wird, die an Kunden gesendet wird, wenn das Ablauflimit für einen Punktstapel erreicht ist.

1. Für **[!UICONTROL Expiry Warning Before (days)]** geben Sie die Anzahl der Tage ein, bevor die Punkte ablaufen, an die die Benachrichtigung gesendet wird.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

## Aktualisieren des Saldos der belohnten Punkte

Der Saldo der Prämienpunkte kann vom Administrator aktualisiert werden.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Suchen Sie den Kunden im Raster und klicken Sie auf **[!UICONTROL Edit]** im _[!UICONTROL Action]_Spalte.

1. under _Kundeninformationen_, wählen Sie die **[!UICONTROL Reward Points]** Abschnitt.

1. Geben Sie die Anzahl der **[!UICONTROL Update Points]**:

   - Um den Betrag der Belohnungspunkte zu aktualisieren, geben Sie die Zahl ein, um den Saldo der Gesamtpunkte zu erhöhen.
   - Geben Sie die negative Zahl ein, um die Summe der Punkte zu reduzieren.

1. Eingabe **[!UICONTROL Comments]** bei Bedarf im Zusammenhang mit der Anpassung der Belohnungspunkte.

   ![Bonuspunkte-Saldo](./assets/reward-points-balance.png){width="700" zoomable="yes"}

1. Abonnieren Sie den Kunden optional für _Benachrichtigungen zu Rewards-Punkten_:

   - **[!UICONTROL Subscribe for Balance Updates]**
   - **[!UICONTROL Subscribe for Points Expiration Notifications]**

1. Klicks **[!UICONTROL Save Customer]**.

Alle Aktionen im Zusammenhang mit Prämienpunkten werden im _[!UICONTROL Reward Points History]_auf ihrem Konto auf der Storefront.

## Feldbeschreibungen

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Balance] | Aktuelle Bilanzsumme der Kundenprämien |
| [!UICONTROL Amount Balance] | Betrag des aktuellen Zahlungsbilanzsaldos |
| [!UICONTROL Points] | Die Anzahl der hinzugefügten oder subtraktierten Punkte |
| [!UICONTROL Amount] | Zugeschlagener oder subtraktierter Geldbetrag |
| [!UICONTROL Rate] | Die [Refinanzierungskurs](reward-exchange-rates.md) |
| [!UICONTROL Website] | Website, der der Verlauf der Belohnungspunkte zugewiesen wurde |
| [!UICONTROL Reason] | Gründe für die Vergabe von Punkten:<br>**[!UICONTROL Making purchases]**— Jedes Mal, wenn der Kunde einen Kauf tätigt, kann er Punkte sammeln.<br>**[!UICONTROL Registering on the site]** - bei der Registrierung (einmal) eingezogen.<br>**[!UICONTROL Subscribing to a newsletter]**- Akquise für die Erstanmeldung (einmal).<br>**[!UICONTROL Sending Invitations]** — Sammeln Sie Punkte, indem Sie Ihre Freunde einladen, der Website beizutreten.<br>**[!UICONTROL Converting Invitations to Customer]**— Sammeln Sie Punkte für jede Einladung, die sie senden, und führen Sie Freunde, die sich auf der Website registrieren.<br>**[!UICONTROL Converting Invitations to Order]** — Sammeln Sie für jeden Verkauf Punkte, die sich aus einer ausgehenden Einladung ergeben.<br>**[!UICONTROL Review Submission]**— Sammeln Sie Punkte für die Einreichung von Produktprüfungen. |
| [!UICONTROL Created] | Datum und Uhrzeit der Aktualisierung der Bonuspunkte |
| [!UICONTROL Expired] | Anzahl abgelaufener Bonuspunkte |
| [!UICONTROL Comment] | Kommentare beim Hinzufügen oder Abziehen von Punkten |

{style="table-layout:auto"}

## Fehlerbehebung bei Ressourcen

Hilfe zur Fehlerbehebung bei Problemen mit belohnten Punkten finden Sie in den folgenden Knowledge Base-Artikeln des Commerce-Supports:

- [Treuepunkte bei Teilbestellungen](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-8/mdva-31295-magento-patch-loyalty-points-on-partial-orders.html)
- [404-Fehler - Entfernen von Prämienpunkten beim Multi-Shipping-Checkout](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/storefront/magento-2.4.0-404-error-removing-rewards-points-on-multi-shipping-checkout.html)
