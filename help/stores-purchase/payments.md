---
title: Zahlungsübersicht
description: Erfahren Sie mehr über die Zahlungsmethoden und Services, die nativ in Adobe Commerce und Magento Open Source unterstützt werden.
exl-id: 474bf6df-96e2-4db3-ad3c-1804b5de33b0
feature: Payments
source-git-commit: 15118877bb8cc533b2323819db34da0513899e25
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 0%

---

# Zahlungsübersicht

Adobe Commerce und Magento Open Source unterstützen eine Vielzahl von Zahlungsmethoden und -services. Dazu gehören mehrere Offline-Zahlungsmethoden, einschließlich Zahlung per Scheck oder Bestellung und Nachnahme (Nachnahme). Es gibt auch native Integrationen für zahlreiche Online-Zahlungslösungen und -Gateways, einschließlich Braintree als gebündelte, vom Anbieter entwickelte Erweiterung.

>[!TIP]
>
>Payment Services für Adobe Commerce und Magento Open Source bietet eine schlüsselfertige Self-Service-Lösung, einschließlich Sandbox-Tests und einer einfachen Einrichtung, für eine robuste und sichere Zahlungsabwicklung. Weitere Informationen zu diesem leistungsstarken Tool-Set und dazu, wie es Ihnen die insight und die Kontrolle gibt, die Sie benötigen, um das beste Erlebnis für Ihre Käufer zu schaffen, finden Sie im [Benutzerhandbuch für Zahlungsdienste](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html). Dies ist die standardmäßige Zahlungslösung in [Adobe Commerce as a Cloud Service](https://experienceleague.adobe.com/en/docs/commerce/cloud-service/overview).

>[!NOTE]
>
>Lesen Sie die [PCI Compliance Guidelines](../getting-started/compliance-pci.md), in denen die Anforderungen der Payment Card Industry (PCI) für Unternehmen beschrieben werden, die Zahlungen per Kreditkarte über das Internet akzeptieren.

## Änderungen in 2.4

[!BADGE Nur PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."}

Einige Zahlungsintegrationen und gebündelte Erweiterungen wurden in den Versionen 2.4.x entfernt und in die Commerce Marketplace verschoben. Die neuesten offiziellen Zahlungsintegrationserweiterungen finden Sie in der [Commerce Marketplace](https://marketplace.magento.com/extensions/payments-security.html){:target="_blank"}.

- **Amazon Pay** und **Klarna**: Die Adobe Commerce- und Magento Open Source-Versionen 2.4.0 bis 2.4.3 enthielten diese vom Anbieter entwickelten Erweiterungen. Ab Version 2.4.4 sind diese Erweiterungen nicht mehr mit der Hauptversion gebündelt und müssen von der Commerce Marketplace installiert und aktualisiert werden. Der Marketplace bietet außerdem Zugriff auf die aktuelle Dokumentation, die vom Erweiterungsentwickler bereitgestellt wird.

  Wenn Sie eine dieser gebündelten Erweiterungen aktiviert und konfiguriert haben, müssen Sie Ihre Datei „composer.json“ im Rahmen des Upgrade-Prozesses auf 2.4.4 aktualisieren, um zukünftige Erweiterungs-Updates zu verwalten. Siehe [Upgrade-Module](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) im _Upgrade-Handbuch_ für weitere Informationen.

- **Worldpay**, **Eway**, **CyberSource** und **Authorize.Net**: Einzelheiten zu einem sicheren Übergang von diesen Zahlungsintegrationen finden Sie im [DevBlog](https://community.magento.com/t5/Magento-DevBlog/Deprecation-of-Magento-core-payment-integrations/ba-p/426445){:target="_blank"}.

## Offline-Zahlungsmethoden

Adobe Commerce und Magento Open Source umfassen mehrere integrierte Offline-Zahlungsmethoden, für die keine Dienste eines Drittanbieters zur Zahlungsverarbeitung erforderlich sind:

- [Null-Zwischensumme-Checkout](zero-subtotal-checkout.md)
- [Nachnahmeleistung](cash-on-delivery.md)
- [Banküberweisung](bank-transfer.md)
- [Scheck/Zahlungsanweisung](check-money-order.md)
- [Bestellung](purchase-order.md)
- [Zahlung auf Rechnung](../b2b/enable-basic-features.md#configure-payment-on-account) ![Adobe Commerce B2B](../assets/b2b.svg) (verfügbar mit Adobe Commerce B2B)

## Online-Zahlungsmethoden

Adobe Commerce und Magento Open Source unterstützen zahlreiche Zahlungslösungen, die Handelsdienstleistungen in allen Teilen der Welt anbieten. Im Gegensatz zu Zahlungslösungen, die die Kontrolle auf eine andere Website übertragen, um die Transaktion abzuschließen, ermöglicht ein Zahlungs-Gateway es Ihnen, Kreditkartenzahlungen direkt von Ihrem Geschäft zu akzeptieren, ohne dass der Kunde Ihre Website verlässt.

### Empfohlene Lösungen

- [Zahlungsdienste](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html)
- [!BADGE Nur PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."} [PayPal Express-Checkout](paypal-express-checkout.md)
- [!BADGE Nur PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."} [Braintree](braintree.md)

### Andere PayPal-Zahlungslösungen

[!BADGE Nur PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."}

Weitere Informationen [&#x200B; Zahlungsmethoden bei PayPal finden &#x200B;](paypal.md) unter „PayPal-&quot;.

#### All-in-One-PayPal-Lösungen

[!BADGE Nur PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."}

- [PayPal-Zahlungen - Erweitert](paypal-payments-advanced.md)
- [PayPal Payments Pro](paypal-payments-pro.md)
- [PayPal-Zahlungsstandard](paypal-payments-standard.md)

#### PayPal-Zahlungs-Gateways

[!BADGE Nur PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."}

- [PayPal Payflow Pro](paypal-payflow-pro.md)
- [PayPal-Payflow-Link](paypal-payflow-link.md)

## Schutz vor Betrug

[!BADGE Nur PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."}

Betrugsschutz-Services und Filter prüfen gesendete Bestellungen, bevor die Transaktion verarbeitet wird, um betrügerische Bestellungen zu erkennen und Sie vor den Kosten von Rückbelastungen zu schützen. Adobe Commerce und Magento Open Source unterstützen die folgenden Lösungen zum Schutz vor Betrug:

- [PayPal-Betrugsverwaltungsfilter](paypal.md#paypal-fraud-management-filters)

- [Lösungen zum Schutz vor Betrug auf dem Marketplace][1]

>[!NOTE]
>
>Um Aktualisierungen zur Einhaltung von Sicherheitsvorschriften zu unterstützen, wird der Signifyd-Betrugsschutz ab Version 2.4.0 von Commerce entfernt. Wenn Sie die Signifyd-Integration in einer Version 2.3.x oder einer früheren Version verwendet haben, wird empfohlen, zur Erweiterung [Signifyd Fraud &amp; Chargeback Protection](https://marketplace.magento.com/signifyd-module-connect.html){:target="_blank"} zu wechseln. Stellen Sie sicher, dass Sie Aktualisierungen für die Erweiterung gemäß den Herstellerrichtlinien verwalten.

## Fehlerbehebung bei Ressourcen

[!BADGE Nur PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."}

Hilfe bei der Fehlerbehebung bei Zahlungsproblemen finden Sie in der [Support-Wissensdatenbank](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/overview.html).

[1]: https://marketplace.magento.com/catalogsearch/result?q=fraud%20protection
