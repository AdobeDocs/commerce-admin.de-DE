---
title: '[!UICONTROL Sales] menu'
description: Der Commerce-Administrator enthält das Menü "[!UICONTROL Sales]", über das Sie auf Tools zugreifen können, mit denen Sie Bestellungen bearbeiten können, abhängig davon, wo sie sich im Workflow befinden.
exl-id: 105106a4-85f7-4143-8411-69ff67ff9331
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '435'
ht-degree: 0%

---

# Menü [!UICONTROL Sales]

Im Menü &quot;Verkauf&quot;werden Transaktionen nach dem Ort aufgelistet, an dem sie sich im Bestell-Workflow befinden. Sie können sich jede Option als eine andere Phase im Leben einer Bestellung vorstellen.

![Menü &quot;Verkauf&quot;](./assets/admin-menu-sales.png){width="450" zoomable="yes"}

## Anzeigen des Menüs [!UICONTROL Sales]

Klicken Sie in der Seitenleiste _Admin_ auf **[!UICONTROL Sales]**.

## Menüoptionen

### [!UICONTROL Quotes]

![Adobe Commerce B2B](../assets/b2b.svg) (verfügbar mit Adobe Commerce B2B)

Autorisierte Käufer können [den Preis ](../b2b/quotes.md) mit dem Verkäufer aushandeln, indem sie eine [Anfrage](../b2b/quote-request.md) aus dem Warenkorb senden.

### [!UICONTROL Orders]

Wenn eine [Bestellung](orders.md) aufgegeben wird, wird eine Verkaufsreihenfolge als temporärer Datensatz der Transaktion erstellt. Die Zahlung wurde nicht verarbeitet und die Bestellung kann weiterhin storniert werden.

### [!UICONTROL Invoices]

Eine [Rechnung](invoices.md) ist ein Datensatz über den Eingang der Zahlung für eine Bestellung. Es können mehrere Rechnungen für eine einzelne Bestellung erstellt werden, von denen jede so viele oder so wenige der von Ihnen angegebenen gekauften Produkte enthält. Je nach Zahlungsvorgang kann die Zahlung automatisch erfasst werden, wenn die Rechnung erstellt wird.

### [!UICONTROL Shipments]

Eine [Sendung](shipments.md) ist ein Datensatz der Produkte in einer Reihenfolge, die versandt wurden. Wie bei Rechnungen können mehrere Sendungen mit einer einzigen Bestellung verbunden werden, bis alle Produkte in der Bestellung versandt werden.

### [!UICONTROL Credit Memos]

Ein [Credit Memo](credit-memos.md) ist ein Dokument, das den Betrag angibt, der dem Kunden für eine vollständige oder teilweise Rückerstattung geschuldet wird. Der Betrag kann auf einen Kauf angewendet oder dem Kunden zurückerstattet werden.

### [!UICONTROL Returns]

![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce)

Eine [zurückgegebene Warenautorisierung](returns.md) (RMA) kann Kunden gewährt werden, die einen Artikel zur Ersatz- oder Rückerstattung zurückgeben möchten. RMAs können für einfache, gruppierte, konfigurierbare und gebündelte Produktarten ausgestellt werden. RMAs sind jedoch nicht für virtuelle und herunterladbare Produkte oder Geschenkkarten verfügbar.

### [!UICONTROL Billing Agreements]

Eine [Abrechnungsvereinbarung](paypal-billing-agreements.md) ähnelt einer Bestellung, ist jedoch nicht auf einen einzelnen Kauf beschränkt. Während der Kasse wählt der Kunde die Abrechnungsmethode. Durch einen Abrechnungsvertrag wird der Checkout-Prozess optimiert, da der Kunde nicht für jeden Kauf Zahlungsinformationen eingeben muss.

### [!UICONTROL Transactions]

Auf der Seite [Transaktionen](transactions.md) werden alle Zahlungsaktivitäten aufgelistet, die zwischen Ihrem Store und allen Zahlungssystemen stattgefunden haben, und es erhalten Sie Zugriff auf detailliertere Informationen.

### [!UICONTROL Braintree Virtual Terminal]

Auf der Braintree Virtual Terminal-Seite kann ein Admin-Benutzer die Zahlung für den ausgewählten Betrag akzeptieren. Um die Terminalfunktion verfügbar zu machen, sollte ein Händler grundlegende [Braintree-Einstellungen](braintree.md) konfigurieren. Braintree bietet eine vollständig anpassbare Checkout-Erfahrung mit der Betrugserkennung und PayPal-Integration.

### [!UICONTROL Archive]

![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce)

(Archivierungsoption muss aktiviert sein) [Die Archivierung von Bestellungen](order-archive.md) und anderen Verkaufsdokumenten verbessert regelmäßig die Leistung und hält Ihren Arbeitsbereich von unnötigen Informationen frei.
