---
title: Zahlungsübersicht
description: Erfahren Sie mehr über die Zahlungsmethoden und -dienste, die nativ in Adobe Commerce und Magento Open Source unterstützt werden.
exl-id: 474bf6df-96e2-4db3-ad3c-1804b5de33b0
feature: Payments
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '615'
ht-degree: 0%

---

# Zahlungsübersicht

Adobe Commerce und Magento Open Source unterstützen verschiedene Zahlungsmethoden und -dienste, die Sie für einen einfacheren Checkout und eine benutzerfreundliche Lösung anbieten können. Diese Liste enthält verschiedene Offline-Zahlungsmethoden, einschließlich der Zahlung per Scheck oder Geldbestellung und der Nachnahme (COD). Es gibt auch native Integrationen für zahlreiche Online-Zahlungslösungen und Gateways, einschließlich Braintree als gebündelte, von Anbietern entwickelte Erweiterung.

>[!TIP]
>
>Zahlungsdienste für Adobe Commerce und Magento Open Source bieten eine schlüsselfertige Self-Service-Lösung, einschließlich Sandbox-Tests und einer einfachen Einrichtung, die eine robuste und sichere Zahlungsverarbeitung ermöglicht. Weitere Informationen zu diesem leistungsstarken Tool-Set und dazu, wie Sie damit Einblicke und Kontrolle erhalten, die Sie benötigen, um das beste Erlebnis für Ihre Käufer zu erstellen, finden Sie im [Benutzerhandbuch für Zahlungsdienste](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html).

>[!NOTE]
>
>Lesen Sie die [PCI compliance Guidelines](../getting-started/compliance-pci.md) , in denen die von der Zahlungskartenbranche (PCI) festgelegten Anforderungen für Unternehmen erläutert werden, die Zahlungen per Kreditkarte über das Internet akzeptieren.

## Änderungen in 2.4

Einige Zahlungsintegrationen und gebündelte Erweiterungen wurden in Version 2.4.x entfernt und auf Commerce Marketplace verschoben. Sie finden die neuesten offiziellen Zahlungsintegrationserweiterungen in [Commerce Marketplace](https://marketplace.magento.com/extensions/payments-security.html){:target=&quot;_blank&quot;}.

- **Amazon Pay** und **Klarna**: Adobe Commerce- und Magento Open Source-Versionen 2.4.0 bis 2.4.3 umfassten diese vom Anbieter entwickelten Erweiterungen. Ab Version 2.4.4 sind diese Erweiterungen nicht mehr im Paket mit der Kernversion enthalten und müssen über die Commerce Marketplace installiert und aktualisiert werden. Der Marketplace bietet außerdem Zugriff auf die aktuelle Dokumentation, die vom Erweiterungsentwickler bereitgestellt wird.

  Wenn Sie eine dieser gebündelten Erweiterungen aktiviert und konfiguriert haben, müssen Sie Ihre Composer.json-Datei im Rahmen des Aktualisierungsprozesses 2.4.4 aktualisieren und die Erweiterungs-Updates in Zukunft verwalten. Weitere Informationen finden Sie unter [Aktualisierungsmodule](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) im _Aktualisierungshandbuch_.

- **WorldPay**, **Eway**, **CyberSource** und **Authorize.Net**: Weitere Informationen zum Herstellen einer sicheren Transition aus diesen Zahlungsintegrationen finden Sie im Abschnitt [DevBlog](https://community.magento.com/t5/Magento-DevBlog/Deprecation-of-Magento-core-payment-integrations/ba-p/426445){:target=&quot;_blank&quot;}.

## Offline-Zahlungsmethoden

Adobe Commerce und Magento Open Source umfassen mehrere integrierte Offline-Zahlungsmethoden, für die keine Dienste eines Zahlungsverarbeitungsunternehmens eines Drittanbieters erforderlich sind:

- [Null Zwischensumme Checkout](zero-subtotal-checkout.md)
- [Barzahlung bei Lieferung](cash-on-delivery.md)
- [Banküberweisungszahlung](bank-transfer.md)
- [Überprüfen/Monatsbestellung](check-money-order.md)
- [Bestellung](purchase-order.md)
- [Zahlung auf Konto](../b2b/enable-basic-features.md#configure-payment-on-account) ![Adobe Commerce B2B](../assets/b2b.svg) (bei Adobe Commerce B2B verfügbar)

## Online-Zahlungsmethoden

Adobe Commerce und Magento Open Source unterstützen zahlreiche Zahlungslösungen, die Handelsdienstleistungen in allen Teilen der Welt anbieten. Im Gegensatz zu Zahlungslösungen, die die Kontrolle auf eine andere Website übertragen, um die Transaktion abzuschließen, ermöglicht ein Zahlungsportal es Ihnen, Kreditkartenzahlungen direkt von Ihrem Geschäft aus zu akzeptieren, ohne dass der Kunde Ihre Website verlässt.

### Empfohlene Lösungen

- [Zahlungsdienste](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html)
- [PayPal Express Checkout](paypal-express-checkout.md)
- [Braintree](braintree.md)

### Andere PayPal-Zahlungslösungen

Weitere Informationen zu den Zahlungsmethoden von PayPal finden Sie unter [PayPal-Zahlungslösungen](paypal.md) .

#### All-in-One-PayPal-Lösungen

- [PayPal Payments Advanced](paypal-payments-advanced.md)
- [PayPal Payments Pro](paypal-payments-pro.md)
- [PayPal Payments Standard](paypal-payments-standard.md)

#### PayPal-ZahlungsGateways

- [PayPal Payflow Pro](paypal-payflow-pro.md)
- [PayPal-Payflow-Link](paypal-payflow-link.md)

## Betrugsschutz

Betrügerische Schutzdienste und Filter prüfen eingereichte Bestellungen, bevor die Transaktion verarbeitet wird, um betrügerische Bestellungen aufzudecken und Sie vor den Kosten von Rückerstattungen zu schützen. Adobe Commerce und Magento Open Source unterstützen die folgenden Betrugsschutzlösungen:

- [PayPal Fraud Management Filter](paypal.md#paypal-fraud-management-filters)

- [Fraud Protection Solutions on Marketplace][1]

>[!NOTE]
>
>Um Updates für die Sicherheitskonformität zu unterstützen, wird ab Version 2.4.0 der Signifikante Betrugsschutz aus Commerce entfernt. Wenn Sie die Signifyd-Integration in einer Version 2.3.x oder einer früheren Version verwendet haben, wird empfohlen, zur Erweiterung [Signifyd Fraud &amp; Chargeback Protection](https://marketplace.magento.com/signifyd-module-connect.html){:target=&quot;_blank&quot;} zu wechseln. Stellen Sie sicher, dass Sie Aktualisierungen für die Erweiterung gemäß den Richtlinien des Anbieters verwalten.

## Fehlerbehebung bei Ressourcen

Hilfe zur Fehlerbehebung von Zahlungsproblemen finden Sie in der [Support-Wissensdatenbank](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/overview.html?lang=en).

[1]: https://marketplace.magento.com/catalogsearch/result?q=fraud%20protection
