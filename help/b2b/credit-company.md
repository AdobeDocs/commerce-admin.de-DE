---
title: Verwalten von Firmenkrediten
description: Erfahren Sie mehr über die Kreditlinien von Unternehmen, das Festlegen von Parametern und die Verarbeitung von Zahlungen für Konten.
exl-id: 62ff2a36-053d-4ba0-9969-0f05701afbff
feature: B2B, Companies, Payments
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '799'
ht-degree: 0%

---

# Verwalten von Firmenkrediten

Wenn [Kontozahlung](../getting-started/../b2b/enable-basic-features.md#configure-payment-on-account) in der Konfiguration aktiviert ist, können Unternehmen bis zu dem für das Unternehmen gewährten Kreditlimit auf ihrem Konto Einkäufe tätigen. Wenn diese Option aktiviert ist, können Kunden den Status ihrer Unternehmensgutschrift über ihr Konto-Dashboard überprüfen.

![Firmenguthaben](./assets/company-create-credit-admin.png){width="700" zoomable="yes"}

Sie können für jedes Unternehmensprofil die folgenden kreditbezogenen Parameter festlegen:

- Kreditwährung
- Kreditbeschränkung
- Erlauben, die Kreditbeschränkung zu überschreiten
- Grund für die Veränderung

Wenn das Unternehmen über einen ausstehenden Saldo verfügt, wird oben in der Bestellung ein Hinweis an den Store-Administrator angezeigt, wenn er vom Administrator angezeigt wird. Weitere Informationen finden Sie unter [Unternehmenskonto erstellen](account-company-create.md).

## Firmenkreditgeschäfte

Die [!UICONTROL Company Credit] im Firmenprofil wird eine Zusammenfassung der Kundenkreditaktivität mit einer Übersicht über den Verlauf der Firmenkredite angezeigt.

![Aktive Unternehmenskredite](./assets/company-credit-reimbursements-grid.png){width="700" zoomable="yes"}

| Spalte | Beschreibung |
|--- |--- |
| [!UICONTROL Date] | Das Datum der Transaktion. Um Datum und Uhrzeit anzuzeigen, bewegen Sie den Mauszeiger über das Datum. |
| [!UICONTROL Operation] | Der mit der Transaktion verknüpfte Aktivitätstyp. Werte: <br/>**[!UICONTROL Allocated]**- dem Unternehmen zugewiesener Kredit.<br/>**[!UICONTROL Updated]** - Eine Änderung wurde auf eines der folgenden Felder angewendet: [!UICONTROL Credit limit] / [!UICONTROL Credit currency] / [!UICONTROL Allow to exceed credit limit] <br/>**[!UICONTROL Purchased]**- Eine Bestellung wurde aufgegeben.<br/>**[!UICONTROL Reimbursed]** - Der ausstehende Restbetrag wurde zurückgezahlt. <br/>**[!UICONTROL Refunded]**- Ein Kreditnachrichtenbetrag wurde zurückerstattet.<br/>**[!UICONTROL Reverted]** - Die Bestellung wurde storniert und der Betrag an den Guthaben zurückgegeben. |
| [!UICONTROL Amount] | Die Höhe der Transaktion, die den folgenden Transaktionstypen zugeordnet ist: `Purchased` / `Reimbursed` / `Refunded` / `Reverted` <br/>Bei Kaufbeträgen wird der Betrag in der Anzeigewährung des Stores und im Format der Einstellung der Kreditwährung angezeigt, gefolgt von der aktuellen Konversionsrate (falls zutreffend). Beispiel: <br/>20.000,00 EUR (22.400,00 USD) <br/>USD/EUR 0.8928 |
| [!UICONTROL Outstanding Balance] | Der erstattete Betrag abzüglich der fälligen Gesamtsumme aller Bestellungen, die mit der Methode Zahlung auf Konto aufgegeben wurden. Der Betrag kann als positiver oder negativer Wert erscheinen. <br/>**[!UICONTROL Positive value]**- Eine Vorauszahlung wird als positiver Wert dargestellt.<br/>**[!UICONTROL Negative value]** - Ein fälliger Betrag wird als negativer Wert dargestellt. |
| [!UICONTROL Available Credit] | Die Summe der _[!UICONTROL Credit Limit]_und_[!UICONTROL Outstanding Balance]_. Wenn das Unternehmen die Kreditgrenze überschritten hat, erscheint der Betrag als negativer Wert. |
| [!UICONTROL Credit Limit] | Die dem Unternehmen gewährte Kreditsumme. |
| [!UICONTROL Updated By] | Der Name der Person, die den Vorgang initiiert hat. |
| [!UICONTROL Custom Reference Number] | Die mit der Transaktion verknüpfte benutzerdefinierte Referenznummer. |
| [!UICONTROL Comment] | Eine Kompilierung der Werte aus der `Reason for Change` -Feld entsprechend dem Kampagnentyp. <br/>**[!UICONTROL Purchased]**- Enthält Kommentare aus dem Kauf, die Bestellnummer und den Link zur Bestellung.<br/>**[!UICONTROL Reimbursed]** - Enthält Bemerkungen aus der rückzahlbaren Transaktion. |
| [!UICONTROL Action] | Für `Reimbursed` nur Vorgänge. **[!UICONTROL Edit]** - Ermöglicht die Aktualisierung des Erstattungsbetrags. |

{style="table-layout:auto"}

## Aktualisieren der Kreditdaten

Wenn der Kunde die Zahlung für die ausstehende Gutschrift an den Händler vornimmt, muss ein Store-Administrator die Kundenkreditinformationen dann im Admin aktualisieren.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **Kunden > Unternehmen**.

1. Suchen Sie das Unternehmen im Raster und öffnen Sie es in _Bearbeiten_ -Modus.

1. Erweitern Sie die **Firmenguthaben** Abschnitt.

1. Für **Kreditbeschränkung**, geben Sie den neuen Wert ein.

1. Ändern Sie die anderen Werte nach Bedarf.

1. Klicken Sie nach Abschluss der Aktualisierungen auf **[!UICONTROL Save]**.

## Empfangen von Zahlungen

Ein erstatteter Saldo ist eine Offline-Zahlung, die von einem Unternehmen zum Saldo seines Kontos geleistet wird. Der Store-Administrator gibt den Betrag manuell im Unternehmensprofil ein, indem er die Variable _Erstattungssaldo_ Schaltfläche. Bei Einreichung des Betrags berechnet das System den ausstehenden Saldo und die verfügbaren Unternehmenskredite neu und erfasst die Aktion in der Kreditgeschichte des Unternehmens. Der erstattete Betrag wird in der in der Konfiguration angegebenen Kreditwährung angegeben.

### Anwenden einer Zahlung auf ein Unternehmenskonto

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Suchen Sie den Firmendatensatz in der Liste und öffnen Sie ihn in **[!UICONTROL Edit]** -Modus.

1. Klicken Sie oben auf der Seite auf **Erstattungssaldo**.

1. Fügen Sie im Dialogfeld die Zahlungsinformationen hinzu:

   ![Erstattungssaldo](./assets/company-reimburse-balance.png){width="500"}

   - Geben Sie die **Betrag** der Zahlung.

     Der Betrag kann als positiver oder negativer Wert angegeben werden.

   - Geben Sie gegebenenfalls die **Benutzerdefinierte Referenznummer** als Referenz.

     Pro Kostenerstattung kann nur eine benutzerdefinierte Referenznummer angegeben werden. Um die Zahlung auf mehrere EOs anzuwenden, erstellen Sie jeweils eine separate Erstattung.

   - Geben Sie bei Bedarf eine **Kommentar** zur Beschreibung der Erstattung.

1. Klicks **Kostenerstattung**.

   Der ausstehende Saldo und die verfügbaren Kredite des Unternehmens werden neu berechnet und der Verlauf der Unternehmenskredite wird aktualisiert, um die Rückzahlung widerzuspiegeln.

### Kostenerstattung bearbeiten

1. Öffnen Sie das Firmenprofil in **[!UICONTROL Edit]** -Modus.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **Firmenguthaben** Abschnitt.

1. Suchen Sie die Erstattungsaktion in der Tabelle und klicken Sie auf **[!UICONTROL Edit]**.

1. Nehmen Sie die erforderlichen Änderungen vor **Benutzerdefinierte Referenznummer** und **Kommentar**.

   Der Erstattungsbetrag kann nicht geändert werden.

1. Klicken **[!UICONTROL Save]**.

## Storefront-Kreditdaten

Für den Unternehmensadministrator wird im Konto-Dashboard der _Firmenguthaben_ Abschnitt. Sie enthält den aktuellen ausstehenden Saldo, die verfügbaren Kredite und die Kreditgrenze, die ihrem Unternehmenskonto zugeordnet werden, gefolgt von einer Liste der ausstehenden Rechnungen.

Wenn der Händler einen Auftrag storniert, der dem Firmenguthaben in Rechnung gestellt wurde, wird der Auftragsbetrag an den Firmensaldo zurückgegeben und die _Verlauf der Kreditzuweisung_ enthält einen Datensatz der Aktion.

![Firmenguthaben](./assets/company-credit.png){width="700" zoomable="yes"}

## Demo zu Firmenkrediten

In diesem Demo-Video erfahren Sie, wie Sie Firmenkredite verwalten:

>[!VIDEO](https://video.tv.adobe.com/v/344445?quality=12)
