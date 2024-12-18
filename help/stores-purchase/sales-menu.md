---
title: Menü [!UICONTROL Sales]
description: Commerce Admin enthält das Menü [!UICONTROL Sales] , das je nach Position im Workflow Zugriff auf Tools zur Bearbeitung von Aufträgen bietet.
exl-id: 105106a4-85f7-4143-8411-69ff67ff9331
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '435'
ht-degree: 0%

---

# Menü [!UICONTROL Sales]

Im Menü Verkauf werden die Transaktionen nach ihrer Position im Auftrags-Workflow aufgelistet. Sie können sich jede dieser Optionen als ein anderes Stadium in der Lebensdauer einer Bestellung vorstellen.

![Menü „Verkauf](./assets/admin-menu-sales.png){width="450" zoomable="yes"}

## Anzeigen des [!UICONTROL Sales]

Klicken Sie in der _Admin_-Seitenleiste auf **[!UICONTROL Sales]**.

## Menüoptionen

### [!UICONTROL Quotes]

![Adobe Commerce B2B](../assets/b2b.svg) (verfügbar mit Adobe Commerce B2B)

Autorisierte Käufer können [den Preis aushandeln](../b2b/quotes.md) mit dem Verkäufer, indem sie eine [Anfrage](../b2b/quote-request.md) aus dem Warenkorb senden.

### [!UICONTROL Orders]

Wenn [Auftrag](orders.md) aufgegeben wird, wird ein Kundenauftrag als temporärer Datensatz der Transaktion erstellt. Die Zahlung wurde nicht bearbeitet und die Bestellung kann trotzdem storniert werden.

### [!UICONTROL Invoices]

Eine [Rechnung](invoices.md) ist ein Datensatz über den Zahlungseingang für eine Bestellung. Für eine einzelne Bestellung können mehrere Rechnungen erstellt werden, wobei jede mit so vielen oder so wenigen der von Ihnen angegebenen gekauften Produkte ausgestattet sein kann. Abhängig von der Zahlungsaktion kann die Zahlung automatisch erfasst werden, wenn die Rechnung generiert wird.

### [!UICONTROL Shipments]

Eine [Sendung](shipments.md) ist eine Aufzeichnung der Produkte in einer Bestellung, die versendet wurden. Wie bei Rechnungen können mehrere Lieferungen mit einer Bestellung verknüpft werden, bis alle Produkte der Bestellung versendet werden.

### [!UICONTROL Credit Memos]

Eine [Gutschrift](credit-memos.md) ist ein Dokument, das den Betrag anzeigt, der dem Kunden für eine vollständige oder teilweise Rückerstattung geschuldet wird. Der Betrag kann auf einen Kauf angerechnet oder dem Kunden zurückerstattet werden.

### [!UICONTROL Returns]

![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce)

Kunden[ die einen Artikel zum Austausch oder zur Rückerstattung ](returns.md) möchten, kann eine „Rücksendung von Waren“ (RMA) erteilt werden. RMAs können für die Produktarten „Einfach“, „Gruppiert“, „Konfigurierbar“ und „Bundle“ ausgestellt werden. RMAs sind jedoch nicht für virtuelle und herunterladbare Produkte oder Geschenkgutscheine verfügbar.

### [!UICONTROL Billing Agreements]

Eine [Abrechnungsvereinbarung](paypal-billing-agreements.md) ähnelt einer Bestellung, mit dem Unterschied, dass sie nicht auf einen einzigen Kauf beschränkt ist. Beim Checkout wählt der Kunde als Zahlungsmethode die Abrechnungsvereinbarung. Eine Abrechnungsvereinbarung optimiert den Checkout-Prozess, da der Kunde nicht für jeden Kauf Zahlungsinformationen eingeben muss.

### [!UICONTROL Transactions]

Die [Transaktionen](transactions.md) Seite listet alle Zahlungsaktivitäten auf, die zwischen Ihrem Geschäft und allen Zahlungssystemen stattgefunden haben, und bietet Zugriff auf detailliertere Informationen.

### [!UICONTROL Braintree Virtual Terminal]

Auf der Braintree Virtual Terminal-Seite kann ein Administrator die Zahlung für den ausgewählten Betrag akzeptieren. Um die Terminalfunktion verfügbar zu machen, sollte ein Händler die grundlegenden [Braintree-Einstellungen konfigurieren](braintree.md). Braintree bietet ein vollständig anpassbares Checkout-Erlebnis mit Betrugserkennung und PayPal-Integration.

### [!UICONTROL Archive]

![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce)

(Archivierungsoption muss aktiviert sein) [Archivierungsaufträge](order-archive.md) und andere Verkaufsdokumente verbessern regelmäßig die Leistung und halten Ihren Arbeitsbereich frei von unnötigen Informationen.
