---
title: Firmenkredite verwalten
description: Erfahren Sie mehr über Firmenkreditlinien, das Festlegen von Parametern und die Verarbeitung von Zahlungen auf Konto.
exl-id: 62ff2a36-053d-4ba0-9969-0f05701afbff
feature: B2B, Companies, Payments
role: Admin
source-git-commit: 7288a4f47940e07c4d083826532308228d271c5e
workflow-type: tm+mt
source-wordcount: '802'
ht-degree: 0%

---

# Firmenkredite verwalten

Wenn [Zahlung auf Konto](../getting-started/../b2b/enable-basic-features.md#configure-payment-on-account) in der Konfiguration aktiviert ist, können Unternehmen bis zu dem Kreditlimit, das dem Unternehmen gewährt wird, auf ihrem Konto Käufe tätigen. Wenn diese Option aktiviert ist, können Kundinnen und Kunden den Status ihres Firmenguthabens über ihr Konto-Dashboard überprüfen.

![Firmenkredit](./assets/company-create-credit-admin.png){width="700" zoomable="yes"}

Für jedes Unternehmensprofil können die folgenden kreditbezogenen Parameter festgelegt werden:

- Kreditwährung
- Kreditlimit
- Überschreiten des Kreditlimits zulassen
- Änderungsgrund

Wenn das Unternehmen über einen ausstehenden Saldo verfügt, wird bei der Anzeige im Admin-Bereich oben im Kundenauftrag ein Hinweis an den Filialadministrator angezeigt. Weitere Informationen finden Sie unter [Erstellen eines Unternehmenskontos](account-company-create.md).

## Firmenkreditaktivität

Im Abschnitt [!UICONTROL Company Credit] des Firmenprofils wird eine Zusammenfassung der Aktivität „Kundenkredit“ mit einem Raster der Historie der Firmenkredite angezeigt.

![Firmenkreditaktivität](./assets/company-credit-reimbursements-grid.png){width="700" zoomable="yes"}

| Spalte | Beschreibung |
|--- |--- |
| [!UICONTROL Date] | Das Datum der Transaktion. Um Datum und Uhrzeit anzuzeigen, bewegen Sie den Mauszeiger über das Datum. |
| [!UICONTROL Operation] | Der Aktivitätstyp, der mit der Transaktion verbunden ist. Werte: <br/>**[!UICONTROL Allocated]**- Dem Unternehmen zugewiesene Gutschrift.<br/>**[!UICONTROL Updated]** - Änderung wurde auf eines der folgenden Felder angewendet: [!UICONTROL Credit limit] / [!UICONTROL Credit currency] / [!UICONTROL Allow to exceed credit limit] <br/>**[!UICONTROL Purchased]**- Bestellung wurde aufgegeben.<br/>**[!UICONTROL Reimbursed]** - Der ausstehende Restbetrag wurde zurückgezahlt. <br/>**[!UICONTROL Refunded]**- Ein Gutschriftsbetrag wurde zurückerstattet.<br/>**[!UICONTROL Reverted]** - Der Auftrag wurde storniert und der Betrag auf das Guthaben zurückgeführt. |
| [!UICONTROL Amount] | Der Transaktionsbetrag, der den folgenden Transaktionsarten zugeordnet ist: `Purchased` / `Reimbursed` / `Refunded` / `Reverted` <br/>Bei Kaufbeträgen wird der Betrag in der Anzeigewährung des Geschäfts und im Format der Einstellung der Kreditwährung angezeigt, gefolgt vom aktuellen Umrechnungskurs (falls zutreffend). Beispiel: <br/>EUR 20.000,00 ($22.400,00) <br/>USD/EUR 0,8928 |
| [!UICONTROL Outstanding Balance] | Der erstattete Betrag abzüglich des fälligen Gesamtbetrags aller Bestellungen, die mit der Zahlungsmethode „Auf Konto“ aufgegeben wurden. Der Betrag kann als positiver oder negativer Wert erscheinen. <br/>**[!UICONTROL Positive value]**- Eine Vorauszahlung wird als positiver Wert dargestellt.<br/>**[!UICONTROL Negative value]** - Ein fälliger Betrag wird als negativer Wert dargestellt. |
| [!UICONTROL Available Credit] | Die Summe aus _[!UICONTROL Credit Limit]_&#x200B;und&#x200B;_[!UICONTROL Outstanding Balance]_. Wenn das Unternehmen das Kreditlimit überschritten hat, erscheint der Betrag als negativer Wert. |
| [!UICONTROL Credit Limit] | Der dem Unternehmen gewährte Kreditbetrag. |
| [!UICONTROL Updated By] | Der Name der Person, die den Vorgang initiiert hat. |
| [!UICONTROL Custom Reference Number] | Die benutzerdefinierte Referenznummer, die mit der Transaktion verknüpft ist. |
| [!UICONTROL Comment] | Eine Kompilierung der Werte aus dem `Reason for Change` Feld, abhängig vom Vorgangstyp. <br/>**[!UICONTROL Purchased]**- Enthält Kommentare zum Kauf sowie die Bestellnummer und den Link zur Bestellung.<br/>**[!UICONTROL Reimbursed]** - Enthält Kommentare aus der zurückgezahlten Transaktion. |
| [!UICONTROL Action] | Nur für `Reimbursed` Vorgänge. **[!UICONTROL Edit]** - Ermöglicht die Aktualisierung des Erstattungsbetrags. |

{style="table-layout:auto"}

## Aktualisieren der Kreditdaten

Wenn der Kunde die Zahlung für seinen ausstehenden Kredit an den Händler leistet, muss ein Store-Administrator die Kundenkreditinformationen in der Admin aktualisieren.

1. Navigieren Sie in _Admin_-Seitenleiste zu **Kunden > Firmen**.

1. Suchen Sie die Firma im Raster und öffnen Sie im _Bearbeiten_-Modus.

1. Erweitern Sie den Abschnitt **Firmenkredite**.

1. Geben **unter „Kreditlimit** den neuen Wert ein.

1. Ändern Sie die anderen Werte nach Bedarf.

1. Wenn die Aktualisierungen abgeschlossen sind, klicken Sie auf **[!UICONTROL Save]**.

## Zahlungen empfangen

Ein erstatteter Saldo ist eine Offline-Zahlung, die von einem Unternehmen auf den Saldo seines Kontos geleistet wird. Der Store-Administrator gibt den Betrag manuell im Firmenprofil ein, indem er die Schaltfläche _Saldo zurückerstatten_ verwendet. Wenn der Betrag übermittelt wird, berechnet das System den ausstehenden Saldo und die verfügbare Unternehmensgutschrift neu und erfasst die Aktion in der Kredithistorie des Unternehmens. Der erstattete Betrag wird in der Kreditwährung angegeben, wie in der Konfiguration angegeben.

### Zahlung auf ein Firmenkonto anwenden

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Suchen Sie den Firmendatensatz in der Liste und öffnen Sie ihn im **[!UICONTROL Edit]**.

1. Klicken Sie oben auf der Seite auf **Kontostand**.

1. Fügen Sie im Dialogfeld die Zahlungsinformationen hinzu:

   ![Rückerstattungsbetrag](./assets/company-reimburse-balance.png){width="500"}

   - Geben Sie den **Betrag** der Zahlung ein.

     Der Betrag kann als positiver oder negativer Wert eingegeben werden.

   - Geben Sie gegebenenfalls als Referenz **Benutzerdefinierte Referenznummer** ein.

     Pro Kostenerstattung kann nur eine individuelle Referenznummer eingegeben werden. Um die Zahlung auf mehrere Bestellungen anzuwenden, erstellen Sie für jede Bestellung eine separate Kostenerstattung.

   - Geben Sie bei Bedarf einen **Kommentar** ein, um die Erstattung zu beschreiben.

1. Klicken Sie **Rückerstattung**.

   Der ausstehende Saldo des Unternehmens und das verfügbare Guthaben des Unternehmens werden neu berechnet, und die Kredithistorie des Unternehmens wird aktualisiert, um die Rückzahlung widerzuspiegeln.

### Bearbeiten einer Kostenerstattung

1. Öffnen Sie das Unternehmensprofil im **[!UICONTROL Edit]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **Firmenkredite**.

1. Suchen Sie die Rückerstattungstransaktion im Raster und klicken Sie auf **[!UICONTROL Edit]**.

1. Nehmen Sie die erforderlichen Änderungen an **Benutzerdefinierte Referenznummer** und &quot;**&quot;**.

   Der Erstattungsbetrag kann nicht geändert werden.

1. Klicken Sie auf **[!UICONTROL Save]**.

## Storefront-Kreditinformationen

Für den Unternehmensadministrator zeigt das Konto-Dashboard den Abschnitt _Firmenguthaben_ an. Sie enthält den aktuellen ausstehenden Saldo, das verfügbare Guthaben und das Kreditlimit, das ihrem Unternehmenskonto zugeordnet ist, gefolgt von einer Liste ausstehender Rechnungen.

Wenn der Händler eine Bestellung storniert, die mit dem Firmenkredit belastet wurde, wird der Auftragsbetrag an den Firmensaldo zurückgegeben und in der _Kreditzuordnungshistorie_ wird die Aktion aufgezeichnet.

![Firmenkredit](./assets/company-credit.png){width="700" zoomable="yes"}

## Firmenkreditdemo

In diesem Demovideo erfahren Sie mehr über die Verwaltung von Firmenkrediten:

>[!VIDEO](https://video.tv.adobe.com/v/344445?quality=12&learn=on)
