---
title: Kreditkarten
description: Erfahren Sie mehr über Kreditkarten und wie sie zur Ausgabe einer teilweisen oder vollständigen Rückerstattung verwendet werden.
exl-id: dc2faf86-0182-4661-9543-bc6e00e06dbf
feature: Orders, Invoices, Returns
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 0%

---

# Kreditkarten

A _Credit Memo_ ist ein Dokument, das den Betrag angibt, der dem Kunden für eine vollständige oder teilweise Rückerstattung geschuldet wird. Der Betrag kann auf einen Kauf angewendet oder dem Kunden zurückerstattet werden. Sie können ein Kreditmemo für eine einzelne Bestellung oder für mehrere Bestellungen als Batch drucken. Bevor ein Kreditmemo gedruckt werden kann, muss es zunächst für die Bestellung generiert werden. Die _Credit Memos_ auf der Seite werden die Kreditkarten aufgelistet, die an Kunden ausgegeben wurden.

![Credit Memos](./assets/credit-memos.png){width="700" zoomable="yes"}

## Erstattungsmethode

Die [Zahlungsmethode](payments.md) für die Bestellung bestimmt in einem bestimmten Umfang die Methode, mit der Sie eine Bestellung zurückgeben.

Sie können Bestellungen auf drei Arten zurückgeben:

- Kontoguthaben—Bestellungen, die über ein Konto gezahlt werden, können als Kontonummer zurückerstattet werden:
   - ![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce) [Store-Guthaben](../customers/store-credit-using.md)
   - ![Adobe Commerce B2B](../assets/b2b.svg) (Verfügbar mit Adobe Commerce B2B) [Kontozahlung](../b2b/enable-basic-features.md#configure-payment-on-account) (Offline-Methode)
   - ![Adobe Commerce B2B](../assets/b2b.svg) (Verfügbar mit Adobe Commerce B2B) [Firmenguthaben](../b2b/credit-company.md)
- [Online-Rückerstattung](payments.md#online-payment-methods)—Bestellungen, die per Kreditkarte über ein Zahlungsportal wie PayPal oder Braintree bezahlt werden, werden online über den Zahlungsverarbeiter zurückerstattet.
- [Offline-Erstattung](payments.md#offline-payment-methods)—Bestellungen, die per Nachnahme bezahlt werden ([COD](cash-on-delivery.md)) oder durch [Scheck- oder Geldbestellung](check-money-order.md) werden offline zurückerstattet.

Sie können für jede Zahlungsmethode eine Offline-Rückerstattung oder einen Kontokredit (sofern aktiviert) ausgeben.

Eine Bestellung, die per Cash on Delivery bezahlt wurde ([COD](cash-on-delivery.md)) oder durch [Scheck- oder Geldbestellung](check-money-order.md) wird offline zurückerstattet.

## Erstattungs-Workflow

1. **Zahlungsaktion** - Wenn die [Zahlungsaktion](credit-memo-create.md#payment-action-setting) -Konfiguration auf `Authorize`müssen Sie eine Rechnung erstellen, bevor Sie ein Kreditmemo erstellen - fahren Sie mit Schritt 2 fort. Wenn auf `Authorize and Capture`, wurde bereits eine Rechnung erstellt - fahren Sie mit Schritt 3 fort.

1. **Rechnung generieren** - [Rechnung erstellen](invoices.md#create-an-invoice) für die Bestellung, damit Sie eine Rückerstattung per Kreditkarte an den Kunden senden können.

1. **Erstellen eines Credit Memos** - [Ein Kreditmemo ausgeben](credit-memo-create.md) im Admin für eine [Kreditkauf](credit-memo-create.md#issue-a-refund-for-a-credit-purchase)oder [Scheck- oder Geldbestellung](credit-memo-create.md#issue-an-offline-refund-for-check-or-money-order).

## Spaltenbeschreibungen

| Spalte | Beschreibung |
|--- |--- |
| [!UICONTROL Select] | Aktivieren Sie die Kontrollkästchen für die Credit-Memo-Elemente, die einer Aktion unterzogen werden sollen, oder verwenden Sie das Auswahlsteuerelement in der Spaltenüberschrift. Optionen: `Select All` / `Deselect All` |
| [!UICONTROL Credit Memo] | Eine eindeutige numerische Kennung, die zugewiesen wird, wenn eine Anforderung für ein Kreditmemo gesendet wird. |
| [!UICONTROL Created] | Datum und Uhrzeit, zu der der Käufer den Antrag auf ein Kreditmemo erstmals gestellt hat. |
| [!UICONTROL Order#] | Bestell-ID der Bestellung, deren Produkte zurückgegeben werden. |
| [!UICONTROL Order Date] | Datum und Uhrzeit der Bestellung durch den Käufer. |
| [!UICONTROL Bill-to Name] | Der Name der Person, die für die Bestellung verantwortlich ist. |
| [!UICONTROL Status] | Gibt den aktuellen Status einer Kreditnachrichtenanforderung an. |
| [!UICONTROL Refunded] | Der Gesamtbetrag, der von der Bestellung zurückerstattet wurde. |
| [!UICONTROL Actions] | **[!UICONTROL View]** - Öffnet den Antrag auf ein Kreditmemo und führt eine Aufzeichnung der Verhandlungen zwischen Käufer und Verkäufer. |
| [!UICONTROL Order Status] | Gibt den Bestellstatus an. |
| [!UICONTROL Purchased From] | Gibt die Website-, Store- und Store-Ansicht an, in der die Bestellung aufgegeben wurde. |
| [!UICONTROL Billing Address] | Die Rechnungsadresse des Kunden, der die Bestellung aufgegeben hat. |
| [!UICONTROL Shipping Address] | Die Adresse, an die die Bestellung versandt werden soll. |
| [!UICONTROL Customer Name] | Der Vor- und Nachname des Kunden, der die Bestellung aufgegeben hat. |
| [!UICONTROL Email] | Die E-Mail-Adresse der Person, die den Auftrag erteilt hat. |
| [!UICONTROL Customer Group] | Die Kundengruppe, der der Kunde zugewiesen ist. |
| [!UICONTROL Payment Method] | Die Zahlungsmethode, die für die Zahlung verwendet wird. |
| [!UICONTROL Shipping Information] | Die zum Versand der Bestellung verwendete Methode. |
| [!UICONTROL Subtotal] | Die Teilsumme der Bestellungen, ohne Versand und Bearbeitung, sowie Steuern. |
| [!UICONTROL Shipping & Handling] | Der für Versand und Bearbeitung berechnete Betrag. |
| [!UICONTROL Adjustment Refund] | Der Betrag, der zum erstatteten Gesamtbetrag als zusätzliche Erstattung hinzukommt. |
| [!UICONTROL Adjustment Fee] | Der Betrag, der von dem erstatteten Gesamtbetrag abgezogen wird. |
| [!UICONTROL Grand Total] | Die Bestellsumme. |

{style="table-layout:auto"}
