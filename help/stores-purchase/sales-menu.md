---
title: '[!UICONTROL Sales] menu'
description: Der Commerce-Administrator umfasst die [!UICONTROL Sales] -Menü, das den Zugriff auf Tools für die Arbeit mit Bestellungen ermöglicht, je nachdem, wo sie sich im Workflow befinden.
exl-id: 105106a4-85f7-4143-8411-69ff67ff9331
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '435'
ht-degree: 0%

---

# [!UICONTROL Sales] Menü

Im Menü &quot;Verkauf&quot;werden Transaktionen nach dem Ort aufgelistet, an dem sie sich im Bestell-Workflow befinden. Sie können sich jede Option als eine andere Phase im Leben einer Bestellung vorstellen.

![Verkaufsmenü](./assets/admin-menu-sales.png){width="450" zoomable="yes"}

## Anzeigen der [!UICONTROL Sales] Menü

Im _Admin_ Seitenleiste, klicken Sie **[!UICONTROL Sales]**.

## Menüoptionen

### [!UICONTROL Quotes]

![Adobe Commerce B2B](../assets/b2b.svg) (Verfügbar mit Adobe Commerce B2B)

Autorisierte Käufer können [Preisverhandlungen führen](../b2b/quotes.md) mit dem Verkäufer durch Versand einer [Anfrage](../b2b/quote-request.md) aus dem Warenkorb.

### [!UICONTROL Orders]

Wenn ein [bestellen](orders.md) platziert wird, wird ein Verkaufsauftrag als temporärer Datensatz der Transaktion erstellt. Die Zahlung wurde nicht verarbeitet und die Bestellung kann weiterhin storniert werden.

### [!UICONTROL Invoices]

Ein [Rechnung](invoices.md) ist ein Protokoll über den Eingang der Zahlung für eine Bestellung. Es können mehrere Rechnungen für eine einzelne Bestellung erstellt werden, von denen jede so viele oder so wenige der von Ihnen angegebenen gekauften Produkte enthält. Je nach Zahlungsvorgang kann die Zahlung automatisch erfasst werden, wenn die Rechnung erstellt wird.

### [!UICONTROL Shipments]

A [Verbringung](shipments.md) ist ein Datensatz der Produkte in einer Bestellung, die versandt wurden. Wie bei Rechnungen können mehrere Sendungen mit einer einzigen Bestellung verbunden werden, bis alle Produkte in der Bestellung versandt werden.

### [!UICONTROL Credit Memos]

A [Credit Memo](credit-memos.md) ist ein Dokument, das den Betrag angibt, der dem Kunden für eine vollständige oder teilweise Rückerstattung geschuldet wird. Der Betrag kann auf einen Kauf angewendet oder dem Kunden zurückerstattet werden.

### [!UICONTROL Returns]

![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce)

A [Zurückgegebene Warenautorisierung](returns.md) (RMA) können Kunden gewährt werden, die eine Rücksendung für Ersatz oder Rückerstattung beantragen. RMAs können für einfache, gruppierte, konfigurierbare und gebündelte Produktarten ausgestellt werden. RMAs sind jedoch nicht für virtuelle und herunterladbare Produkte oder Geschenkkarten verfügbar.

### [!UICONTROL Billing Agreements]

A [Abrechnungsvereinbarung](paypal-billing-agreements.md) ähnelt einer Bestellung, allerdings ist sie nicht auf einen einzelnen Kauf beschränkt. Während der Kasse wählt der Kunde die Abrechnungsmethode. Durch einen Abrechnungsvertrag wird der Checkout-Prozess optimiert, da der Kunde nicht für jeden Kauf Zahlungsinformationen eingeben muss.

### [!UICONTROL Transactions]

Die [Transaktionen](transactions.md) auf der Seite werden alle Zahlungsaktivitäten aufgelistet, die zwischen Ihrem Geschäft und allen Zahlungssystemen stattgefunden haben, und erhalten Zugriff auf detailliertere Informationen.

### [!UICONTROL Braintree Virtual Terminal]

Auf der Braintree Virtual Terminal-Seite kann ein Admin-Benutzer die Zahlung für den ausgewählten Betrag akzeptieren. Um die Terminalfunktion verfügbar zu machen, sollte ein Händler die grundlegende [Braintree-Einstellungen](braintree.md). Braintree bietet eine vollständig anpassbare Checkout-Erfahrung mit der Betrugserkennung und PayPal-Integration.

### [!UICONTROL Archive]

![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce)

(Archivierungsoption muss aktiviert sein) [Archivieren von Bestellungen](order-archive.md) und andere Verkaufsdokumente verbessern regelmäßig die Leistung und halten Ihren Arbeitsbereich frei von unnötigen Informationen.
