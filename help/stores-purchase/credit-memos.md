---
title: Gutschriften
description: Erfahren Sie mehr über Gutschriften und darüber, wie sie zur Ausstellung einer teilweisen oder vollständigen Rückerstattung verwendet werden.
exl-id: dc2faf86-0182-4661-9543-bc6e00e06dbf
feature: Orders, Invoices, Returns
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 0%

---

# Gutschriften

Eine _Gutschrift_ ist ein Dokument, das den Betrag anzeigt, der dem Kunden für eine vollständige oder teilweise Rückerstattung geschuldet wird. Der Betrag kann auf einen Kauf angerechnet oder dem Kunden zurückerstattet werden. Sie können eine Gutschrift für einen einzelnen Auftrag oder für mehrere Bestellungen als Stapel drucken. Bevor eine Gutschrift gedruckt werden kann, muss sie zuerst für die Bestellung generiert werden. Auf _Seite „Gutschriften_ werden die Gutschriften aufgelistet, die Kunden ausgestellt wurden.

![Gutschriften](./assets/credit-memos.png){width="700" zoomable="yes"}

## Rückerstattungsmethode

Die [Zahlungsmethode](payments.md) für die Bestellung bestimmt in gewissem Umfang die Methode, mit der Sie eine Bestellung zurückerstatten.

Sie können Bestellungen auf drei Arten zurückerstatten:

- Kontoguthaben - Bestellungen, die über ein Kreditkonto bezahlt wurden, können als Kontoguthaben zurückerstattet werden:
   - ![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) [Gutschrift speichern](../customers/store-credit-using.md)
   - ![Adobe Commerce B2B](../assets/b2b.svg) (verfügbar mit Adobe Commerce B2B) [Zahlung auf Rechnung](../b2b/enable-basic-features.md#configure-payment-on-account) (Offline-Methode)
   - ![Adobe Commerce B2B](../assets/b2b.svg) (mit Adobe Commerce B2B verfügbar) [Firmenguthaben](../b2b/credit-company.md)
- [Online-Rückerstattung](payments.md#online-payment-methods) - Bestellungen, die per Kreditkarte über ein Zahlungs-Gateway wie PayPal oder Braintree bezahlt werden, werden online über den Zahlungsprozessor zurückerstattet.
- [Offline-Rückerstattung](payments.md#offline-payment-methods) - Bestellungen, die per Nachnahme ([COD](cash-on-delivery.md)) oder per [Scheck oder Zahlungsanweisung bezahlt werden](check-money-order.md) werden offline zurückerstattet.

Sie können für jede Zahlungsmethode eine Offline-Rückerstattung oder Kontogutschrift (falls aktiviert) vornehmen.

Eine Bestellung, die per Nachnahme ([](cash-on-delivery.md) COD) oder per [Scheck oder ](check-money-order.md) bezahlt wurde, wird offline zurückerstattet.

## Erstattungs-Workflow

1. **Zahlungsaktion** - Wenn die Konfiguration [Zahlungsaktion](credit-memo-create.md#payment-action-setting) auf `Authorize` gesetzt ist, müssen Sie vor dem Erstellen einer Gutschrift eine Rechnung generieren. Fahren Sie mit Schritt 2 fort. Ist hierfür `Authorize and Capture` festgelegt, wurde bereits eine Rechnung generiert. Fahren Sie mit Schritt 3 fort.

1. **Rechnung generieren** - [Rechnung erstellen](invoices.md#create-an-invoice) für die Bestellung, damit Sie dem Kunden eine Rückerstattung per Gutschrift senden können.

1. **Gutschrift erstellen** - [Gutschrift ausstellen](credit-memo-create.md) in der Admin für einen [Kreditkauf](credit-memo-create.md#issue-a-refund-for-a-credit-purchase) oder einen [Scheck oder eine Zahlungsanweisung](credit-memo-create.md#issue-an-offline-refund-for-check-or-money-order).

## Spaltenbeschreibungen

| Spalte | Beschreibung |
|--- |--- |
| [!UICONTROL Select] | Aktivieren Sie die Kontrollkästchen der Gutschriftenartikel, die einer Aktion unterzogen werden sollen, oder verwenden Sie die Auswahlsteuerung in der Spaltenüberschrift. Optionen: `Select All` / `Deselect All` |
| [!UICONTROL Credit Memo] | Eine eindeutige numerische Kennung, die zugewiesen wird, wenn eine Anforderung für eine Gutschrift gesendet wird. |
| [!UICONTROL Created] | Datum und Uhrzeit, zu der der Käufer die Anforderung einer Gutschrift erstmals eingereicht hat. |
| [!UICONTROL Order#] | Auftrags-ID der Bestellung, deren Produkte zurückgesendet werden. |
| [!UICONTROL Order Date] | Datum und Uhrzeit der Bestellung durch den Käufer. |
| [!UICONTROL Bill-to Name] | Der Name der für die Bestellung verantwortlichen Person. |
| [!UICONTROL Status] | Gibt den aktuellen Status einer Gutschriftanforderung an. |
| [!UICONTROL Refunded] | Der Gesamtbetrag, der aus der Bestellung zurückerstattet wurde. |
| [!UICONTROL Actions] | **[!UICONTROL View]** - Öffnet die Anfrage einer Gutschrift und zeichnet die Verhandlungen zwischen Käufer und Verkäufer auf. |
| [!UICONTROL Order Status] | Zeigt den Bestellstatus an. |
| [!UICONTROL Purchased From] | Gibt die Website-, Store- und Store-Ansicht an, in der die Bestellung aufgegeben wurde. |
| [!UICONTROL Billing Address] | Die Rechnungsadresse des Kunden, der die Bestellung aufgegeben hat. |
| [!UICONTROL Shipping Address] | Die Adresse, an die die Bestellung versendet werden soll. |
| [!UICONTROL Customer Name] | Der Vor- und Nachname des Kunden, der die Bestellung aufgegeben hat. |
| [!UICONTROL Email] | Die E-Mail-Adresse der Person, die die Bestellung aufgegeben hat. |
| [!UICONTROL Customer Group] | Die Debitorengruppe, der der Debitor zugewiesen ist. |
| [!UICONTROL Payment Method] | Die für die Zahlung zu verwendende Zahlungsmethode. |
| [!UICONTROL Shipping Information] | Die Methode, die für den Versand der Bestellung verwendet werden soll. |
| [!UICONTROL Subtotal] | Die Zwischensumme der Bestellung, ohne Versand und Bearbeitung, und Steuer. |
| [!UICONTROL Shipping & Handling] | Der für Versand und Bearbeitung berechnete Betrag. |
| [!UICONTROL Adjustment Refund] | Der Betrag, der dem Gesamtbetrag hinzugefügt wird, der als zusätzliche Rückerstattung zurückerstattet wird. |
| [!UICONTROL Adjustment Fee] | Der Betrag, der vom erstatteten Gesamtbetrag abgezogen wird. |
| [!UICONTROL Grand Total] | Die Bestellsumme. |

{style="table-layout:auto"}
