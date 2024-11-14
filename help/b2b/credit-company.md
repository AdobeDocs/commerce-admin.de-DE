---
title: Verwalten von Firmenkrediten
description: Erfahren Sie mehr über die Kreditlinien von Unternehmen, das Festlegen von Parametern und die Verarbeitung von Zahlungen für Konten.
exl-id: 62ff2a36-053d-4ba0-9969-0f05701afbff
feature: B2B, Companies, Payments
role: Admin
source-git-commit: 7288a4f47940e07c4d083826532308228d271c5e
workflow-type: tm+mt
source-wordcount: '802'
ht-degree: 0%

---

# Verwalten von Firmenkrediten

Wenn in der Konfiguration die Option [Zahlung auf Konto](../getting-started/../b2b/enable-basic-features.md#configure-payment-on-account) aktiviert ist, können Unternehmen bis zu dem dem Unternehmen gewährten Kreditlimit auf ihrem Konto Einkäufe tätigen. Wenn diese Option aktiviert ist, können Kunden den Status ihrer Unternehmensgutschrift über ihr Konto-Dashboard überprüfen.

![Firmenguthaben](./assets/company-create-credit-admin.png){width="700" zoomable="yes"}

Sie können für jedes Unternehmensprofil die folgenden kreditbezogenen Parameter festlegen:

- Kreditwährung
- Kreditbeschränkung
- Erlauben, die Kreditbeschränkung zu überschreiten
- Grund für die Veränderung

Wenn das Unternehmen über einen ausstehenden Saldo verfügt, wird oben in der Bestellung ein Hinweis an den Store-Administrator angezeigt, wenn er vom Administrator angezeigt wird. Weitere Informationen finden Sie unter [Erstellen eines Unternehmenskontos](account-company-create.md).

## Firmenkreditgeschäfte

Im Abschnitt &quot;[!UICONTROL Company Credit]&quot; des Firmenprofils wird eine Zusammenfassung der Kundenkreditaktivität mit einer Übersicht über den Verlauf des Firmenkredits angezeigt.

![Aktivität &quot;Unternehmensgutschrift&quot;](./assets/company-credit-reimbursements-grid.png){width="700" zoomable="yes"}

| Spalte | Beschreibung |
|--- |--- |
| [!UICONTROL Date] | Das Datum der Transaktion. Um Datum und Uhrzeit anzuzeigen, bewegen Sie den Mauszeiger über das Datum. |
| [!UICONTROL Operation] | Der mit der Transaktion verknüpfte Aktivitätstyp. Werte: <br/>**[!UICONTROL Allocated]**- Dem Unternehmen zugewiesene Gutschrift.<br/>**[!UICONTROL Updated]** - Eine Änderung wurde auf eines der folgenden Felder angewendet: [!UICONTROL Credit limit] / [!UICONTROL Credit currency] / [!UICONTROL Allow to exceed credit limit] <br/>**[!UICONTROL Purchased]**- Eine Bestellung wurde platziert.<br/>**[!UICONTROL Reimbursed]** - Der ausstehende Saldo wurde erstattet. <br/>**[!UICONTROL Refunded]**- Ein Kreditnachrichtenbetrag wurde zurückerstattet.<br/>**[!UICONTROL Reverted]** - Die Bestellung wurde storniert und der Betrag wurde zum Guthaben zurückgegeben. |
| [!UICONTROL Amount] | Der Transaktionsbetrag, der den folgenden Transaktionstypen zugeordnet ist: `Purchased` / `Reimbursed` / `Refunded` / `Reverted` <br/>Bei Kaufbeträgen wird der Betrag in der Anzeigewährung des Geschäfts und im Format der Kreditwährungseinstellung angezeigt, gefolgt von der aktuellen Konversionsrate (falls zutreffend). Beispiel: <br/>20.000,00 EUR ($ 22.400,00) <br/>USD/EUR 0,8928 |
| [!UICONTROL Outstanding Balance] | Der erstattete Betrag abzüglich der fälligen Gesamtsumme aller Bestellungen, die mit der Methode Zahlung auf Konto aufgegeben wurden. Der Betrag kann als positiver oder negativer Wert erscheinen. <br/>**[!UICONTROL Positive value]**- Eine Vorauszahlung wird als positiver Wert dargestellt.<br/>**[!UICONTROL Negative value]** - Ein fälliger Betrag wird als negativer Wert dargestellt. |
| [!UICONTROL Available Credit] | Die Summe der _[!UICONTROL Credit Limit]_und der_[!UICONTROL Outstanding Balance]_. Wenn das Unternehmen die Kreditgrenze überschritten hat, erscheint der Betrag als negativer Wert. |
| [!UICONTROL Credit Limit] | Die dem Unternehmen gewährte Kreditsumme. |
| [!UICONTROL Updated By] | Der Name der Person, die den Vorgang initiiert hat. |
| [!UICONTROL Custom Reference Number] | Die mit der Transaktion verknüpfte benutzerdefinierte Referenznummer. |
| [!UICONTROL Comment] | Eine Kompilierung der Werte aus dem Feld `Reason for Change` entsprechend dem Kampagnentyp. <br/>**[!UICONTROL Purchased]**- Enthält Kommentare aus dem Kauf, die Bestellnummer und den Link zur Bestellung.<br/>**[!UICONTROL Reimbursed]** - Umfasst Kommentare aus der rückerstatteten Transaktion. |
| [!UICONTROL Action] | Nur für `Reimbursed` -Vorgänge. **[!UICONTROL Edit]** - Ermöglicht die Aktualisierung des Erstattungsbetrags. |

{style="table-layout:auto"}

## Aktualisieren der Kreditdaten

Wenn der Kunde die Zahlung für die ausstehende Gutschrift an den Händler vornimmt, muss ein Store-Administrator die Kundenkreditinformationen dann im Admin aktualisieren.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **Kunden > Unternehmen**.

1. Suchen Sie das Unternehmen im Raster und öffnen Sie es im Modus _Bearbeiten_ .

1. Erweitern Sie den Abschnitt **Firmenguthaben** .

1. Geben Sie für **Kreditlimit** den neuen Wert ein.

1. Ändern Sie die anderen Werte nach Bedarf.

1. Klicken Sie nach Abschluss der Aktualisierungen auf **[!UICONTROL Save]**.

## Empfangen von Zahlungen

Ein erstatteter Saldo ist eine Offline-Zahlung, die von einem Unternehmen zum Saldo seines Kontos geleistet wird. Der Store-Administrator gibt den Betrag manuell in das Firmenprofil ein, indem er die Schaltfläche _Restbetrag erstatten_ verwendet. Bei Einreichung des Betrags berechnet das System den ausstehenden Saldo und die verfügbaren Unternehmenskredite neu und erfasst die Aktion in der Kreditgeschichte des Unternehmens. Der erstattete Betrag wird in der in der Konfiguration angegebenen Kreditwährung angegeben.

### Anwenden einer Zahlung auf ein Unternehmenskonto

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Suchen Sie den Firmendatensatz in der Liste und öffnen Sie ihn im Modus **[!UICONTROL Edit]** .

1. Klicken Sie oben auf der Seite auf **Zahlungsausgleich**.

1. Fügen Sie im Dialogfeld die Zahlungsinformationen hinzu:

   ![Rückzahlungssaldo](./assets/company-reimburse-balance.png){width="500"}

   - Geben Sie den **Betrag** der Zahlung ein.

     Der Betrag kann als positiver oder negativer Wert angegeben werden.

   - Geben Sie, falls zutreffend, die **benutzerdefinierte Referenznummer** als Referenz ein.

     Pro Kostenerstattung kann nur eine benutzerdefinierte Referenznummer angegeben werden. Um die Zahlung auf mehrere EOs anzuwenden, erstellen Sie jeweils eine separate Erstattung.

   - Geben Sie nach Bedarf **Kommentar** ein, um die Erstattung zu beschreiben.

1. Klicken Sie auf **Kostenerstattung**.

   Der ausstehende Saldo und die verfügbaren Kredite des Unternehmens werden neu berechnet und der Verlauf der Unternehmenskredite wird aktualisiert, um die Rückzahlung widerzuspiegeln.

### Kostenerstattung bearbeiten

1. Öffnen Sie das Firmenprofil im Modus **[!UICONTROL Edit]** .

1. Erweitern Sie den Abschnitt **Unternehmensgutschrift** um ![Erweiterungsauswahl](../assets/icon-display-expand.png).

1. Suchen Sie die Kostenerstattungstransaktion in der Tabelle und klicken Sie auf **[!UICONTROL Edit]**.

1. Nehmen Sie alle erforderlichen Änderungen an **Benutzerdefinierte Referenznummer** und **Kommentar** vor.

   Der Erstattungsbetrag kann nicht geändert werden.

1. Klicken Sie auf **[!UICONTROL Save]**.

## Storefront-Kreditdaten

Für den Unternehmensadministrator wird im Konto-Dashboard der Abschnitt _Firmenguthaben_ angezeigt. Sie enthält den aktuellen ausstehenden Saldo, die verfügbaren Kredite und die Kreditgrenze, die ihrem Unternehmenskonto zugeordnet werden, gefolgt von einer Liste der ausstehenden Rechnungen.

Wenn der Händler einen Auftrag storniert, der dem Firmenguthaben in Rechnung gestellt wurde, wird der Auftragsbetrag an den Unternehmensstand zurückgegeben und der _Verlauf der Kreditzuweisung_ enthält einen Datensatz der Aktion.

![Firmenguthaben](./assets/company-credit.png){width="700" zoomable="yes"}

## Demo zu Firmenkrediten

In diesem Demo-Video erfahren Sie, wie Sie Firmenkredite verwalten:

>[!VIDEO](https://video.tv.adobe.com/v/344445?quality=12&learn=on)
