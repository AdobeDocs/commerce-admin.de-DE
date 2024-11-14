---
title: Einführung in Stores und Kauferlebnisse
description: Erfahren Sie mehr über die Funktionen, mit denen Sie Ihre Online-Stores erstellen und verwalten können, sowie über die Einkaufserfahrung für Ihre Kunden.
exl-id: 7ced9cbc-49b4-48f7-aae2-fcb48fdb888f
source-git-commit: 7288a4f47940e07c4d083826532308228d271c5e
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 0%

---

# Einführung in Stores und Kauferlebnisse

Adobe Commerce und Magento Open Source bieten eine umfangreiche Reihe von Funktionen, mit denen Sie Ihre Online-Stores und die Einkaufserfahrung für Ihre Kunden erstellen und verwalten können. Innerhalb Ihrer Commerce-Instanz können Sie die Store-Hierarchie von Websites, Stores und Ansichten verwalten. Sie können auch die Steuern und Währungssätze konfigurieren, die zum Ausführen von Geschäften für mehrere Gebietsschemas erforderlich sind, einschließlich der Steuerklassen für Produkte und Kundengruppen.

## Speicherstruktur

Eine einzelne Instanz von Adobe Commerce oder Magento Open Source kann mehrere Sites, Stores oder Store-Ansichten unterstützen, die unterschiedliche Attribute und Inhalte verwenden. Ein typisches Szenario besteht darin, Geschäfte mit verschiedenen Optionen in verschiedenen Domänen einzurichten. Sie möchten beispielsweise vielleicht eine Gruppe von Kategorien und Produkten auf einer Domäne und eine andere Gruppe von Kategorien und Produkten auf einer anderen Domäne in einer anderen Sprache haben. Händler können die Websites, Stores und Ansichten in der Admin-Konsole konfigurieren.

Wenn die [Hierarchie](stores.md) definiert ist, können Sie Konfigurationseinstellungen gemäß [Umfang](../getting-started/websites-stores-views.md#scope-settings) anwenden, sodass jede Site-, Store- und Store-Ansicht den gewünschten Produktkatalog und das Storefront-Erlebnis bereitstellt.

## Kaufpunkt

Adobe Commerce und Magento Open Source reduzieren Bestellfehler, indem sie die SKU und Verfügbarkeit aller Artikel vor der Absendung einer Bestellung automatisch überprüfen. Sie können die Optionen [Warenkorb](cart.md) und [Checkout](checkout-process.md) konfigurieren, um ein optimales Kauferlebnis von der Transaktion bis zum Versand zu bieten. Kunden, die bei ihren Konten angemeldet sind, können den Kassengang schnell abschließen, da ein Großteil der Informationen bereits in ihren Konten enthalten ist. Die Seite _Checkout_ führt den Kunden durch jeden Schritt des Prozesses zum Abschluss der Bestelltransaktion. Wenn Sie [Sofortiger Kauf](checkout-instant-purchase.md) aktivieren, können Kunden den Checkout-Prozess mit in ihrem Konto gespeicherten Informationen beschleunigen.

>[!TIP]
>
>![Adobe Commerce B2B](../assets/b2b.svg) Mit der Installation und Aktivierung von Adobe Commerce B2B können Sie _Quick Order_ für Kunden konfigurieren, die mit einem Unternehmenskonto verknüpft sind. Diese Funktion reduziert den Bestellvorgang auf mehrere Klicks, wenn sie den Namen oder die SKU der Produkte kennen, die sie bestellen möchten. Sie können auch die Unterstützung für verhandelbare Anführungszeichen für Ihre Unternehmenskonten konfigurieren. Weitere Informationen zu den B2B-Funktionen finden Sie im [Adobe Commerce B2B-Benutzerhandbuch](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html).

## Shopping-Hilfe

Kunden benötigen manchmal Hilfe, um einen Kauf abzuschließen. Einige Kunden kaufen gerne online ein, bestellen aber lieber telefonisch. Sie können sowohl den Gästen als auch den Kunden, die sich für ein Konto bei Ihrem Geschäft angemeldet haben, sofortige Hilfe anbieten.

- [Warenkorb verwalten](shopping-assisted-cart-manage.md)
- [Erstellen von Bestellungen](customer-account-create-order.md) für registrierte Kunden
- [Auftrag aktualisieren](order-update.md)

![Warenkorb](./assets/storefront-cart-price-group-discount.png){width="700" zoomable="yes"}

In diesem Video erfahren Sie mehr über den von Verkäufern unterstützten Einkauf:

>[!VIDEO](https://video.tv.adobe.com/v/343662/?quality=12&learn=on)

## Auftragsverwaltung und -vorgänge

Im Admin können Händler auf Informationen in jeder Phase des Auftrags-Workflows zugreifen und Bestellungen verarbeiten:

- Die Seite [Bestellungen](orders.md) bietet Händlern eine leicht zugängliche Liste aller aktuellen Bestellungen sowie Tools zum Bearbeiten und Verarbeiten bestehender Bestellungen und zum Erstellen von Bestellungen im Auftrag von Kunden.

- Auf der Seite [Rechnungen](invoices.md) wird eine Rechnung aufgelistet, die auf einem temporären Verkaufsauftrag basiert und einen permanenten Datensatz der Bestellung liefert.

- Auf der Seite [Sendungen](shipments.md) wird der Versanddatensatz jeder Rechnung aufgelistet, die versandbereit ist.

- Auf der Seite &quot;[Credit Memos](credit-memos.md)&quot;können Händler ein Kreditmemo verarbeiten und verwalten, bei dem es sich um ein Dokument handelt, das den dem Kunden geschuldeten Betrag anzeigt. Der Betrag kann auf einen Kauf angewendet oder dem Kunden zurückerstattet werden.

- ![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Die Seite &quot;[Gibt ](returns.md)&quot;listet die aktuellen zurückgegebenen Merchandise-Anfragen (RMAs) auf und wird verwendet, um neue Rückgabeanforderungen einzugeben.

- Auf der Seite [Transaktionen](transactions.md) werden alle Zahlungsaktivitäten aufgelistet, die zwischen Ihrem Store und einem Zahlungssystem stattgefunden haben, und Sie erhalten Zugriff auf detailliertere Informationen.

## Versand und Lieferung

Studien zeigen, dass Geschäfte, die Kunden eine Auswahl an verschiedenen [Versandmethoden](delivery.md) anbieten, höhere Konversionsraten aufweisen als Geschäfte, die eine einzige Methode verwenden. Der Administrator bietet verschiedene Tools, mit denen Händler mehrere Versandmethoden und [Versandunternehmen](carriers.md) einrichten und [Versandtitel](shipping-labels.md) drucken können.
