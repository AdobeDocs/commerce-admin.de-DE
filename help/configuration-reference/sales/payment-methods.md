---
title: '[!UICONTROL Sales] > [!UICONTROL Payment Methods]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Sales] > [!UICONTROL Payment Methods] des Commerce Admin.
exl-id: 6545b980-c8ef-460a-a884-d5315f5ad513
feature: Configuration, Payments
TQID: https://experienceleague.adobe.com/Z6f-lyypn4xUeVxiR0SQ81PswzU69X3sVCqEa8bTDnc
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: c32adafa-ed01-4b31-997e-2413013911b0
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 1746
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods]

>[!TIP]
>
>Payment Services für Adobe Commerce und Magento Open Source bietet eine schlüsselfertige Self-Service-Lösung, einschließlich Sandbox-Tests und einer einfachen Einrichtung, für eine robuste und sichere Zahlungsabwicklung. Weitere Informationen zu diesem leistungsstarken Tool-Set und dazu, wie es Ihnen die insight und die Kontrolle gibt, die Sie benötigen, um das beste Erlebnis für Ihre Käufer zu schaffen, finden Sie im [_Benutzerhandbuch für Zahlungsdienste_](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html?lang=de).

{{config}}

## [!UICONTROL Merchant Location]

[!BADGE Nur PaaS]{type=Informative url="https://experienceleague.adobe.com/de/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."}

![Standort des Händlers](./assets/payment-methods-merchant-location.png)<!-- zoom -->

<!-- [Merchant Location](https://experienceleague.adobe.com/de/docs/commerce-admin/start/setup/store-details#merchant-location) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Merchant Country] | Website | Gibt das Land an, in dem der Händler registriert ist, um Geschäfte zu tätigen. |

{style="table-layout:auto"}

## Empfohlene Lösungen

Die folgenden Zahlungslösungen werden als einfache Möglichkeit für Händler empfohlen, die gerade erst anfangen, Online-Zahlungen per PayPal-Konto oder Kreditkarte zu akzeptieren. Wenn Ihr Unternehmen wächst, können Sie diese mit zusätzlichen PayPal-Zahlungslösungen kombinieren.

- [Zahlungsdienste](payment-services.md)
- [!BADGE Nur PaaS]{type=Informative url="https://experienceleague.adobe.com/de/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."} [PayPal Express-Checkout](paypal-express-checkout.md)
- [!BADGE Nur PaaS]{type=Informative url="https://experienceleague.adobe.com/de/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."} [Braintree](braintree.md)

>[!NOTE]
>
>Einige Zahlungsintegrationen und gebündelte Erweiterungen wurden in den Versionen 2.4.x entfernt und nach Commerce Marketplace verschoben. Die neuesten offiziellen Zahlungsintegrationserweiterungen finden Sie in [Commerce Marketplace](https://marketplace.magento.com/extensions/payments-security.html){:target="_blank"}.
><br/>>**Amazon Pay** und **Klarna**: Adobe Commerce und Magento Open Source veröffentlichen 2.4.0 bis 2.4.3 und beinhalten diese vom Anbieter entwickelten Erweiterungen. Ab Version 2.4.4 sind diese Erweiterungen nicht mehr mit der Hauptversion gebündelt und müssen von der Commerce Marketplace installiert und aktualisiert werden. Der Marketplace bietet außerdem Zugriff auf die aktuelle Dokumentation, die vom Erweiterungsentwickler bereitgestellt wird.
><br/>>Wenn Sie eine dieser gebündelten Erweiterungen aktiviert und konfiguriert haben, müssen Sie Ihre `composer.json` im Rahmen des Upgrade-Prozesses auf 2.4.4 aktualisieren, um zukünftige Erweiterungs-Updates zu verwalten. Siehe [Upgrade-Module](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html?lang=de) im _Upgrade-Handbuch_ für weitere Informationen.<br/>
><br/>>**Worldpay**, **Eway**, **CyberSource** und **Authorize.Net**: Einzelheiten zu einem sicheren Übergang von diesen Zahlungsintegrationen finden Sie im [DevBlog](https://community.magento.com/t5/Magento-DevBlog/Deprecation-of-Magento-core-payment-integrations/ba-p/426445){:target="_blank"}.

## Andere PayPal-Methoden

[!BADGE Nur PaaS]{type=Informative url="https://experienceleague.adobe.com/de/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."}

PayPal bietet verschiedene Zahlungslösungen an, die den Bedürfnissen von Unternehmen jeder Größe entsprechen und die auf der ganzen Welt tätig sind. PayPal bietet Ihnen die Möglichkeit, Zahlungen von allen gängigen Debit- und Kreditkarten zu akzeptieren. PayPal bietet zusätzlichen Komfort ohne zusätzlichen Aufwand, da auch Kunden, die kein PayPal-Konto haben, mit PayPal für ihre Einkäufe bezahlen können.

### PayPal-All-in-One-Methoden

[!BADGE Nur PaaS]{type=Informative url="https://experienceleague.adobe.com/de/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."}

- [PayPal-Zahlung - Erweitert](paypal-payments-advanced.md)
- [PayPal Payments Pro](paypal-payments-pro.md)
- [PayPal-Zahlungsstandard](paypal-payments-standard.md)

### PayPal-Zahlungs-Gateways

[!BADGE Nur PaaS]{type=Informative url="https://experienceleague.adobe.com/de/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."}

- [PayPal Payflow Pro](paypal-payflow-pro.md) (einschließlich Express-Checkout)
- [PayPal-Payflow-Link](paypal-payflow-link.md) (einschließlich Express-Checkout)

## Grundlegende Zahlungsmethoden

Die folgenden Zahlungsmethoden sind in Commerce integriert und verwenden keinen externen Zahlungsdienstleister zur Verarbeitung der Transaktion. Viele der grundlegenden Zahlungsmethoden wurden offline statt online verwaltet.

### [!UICONTROL Check / Money Order]

![Scheck/Zahlungsanweisung](./assets/payment-methods-check-money-order.png)<!-- zoom -->

<!-- [Check / Money Order](https://experienceleague.adobe.com/de/docs/commerce-admin/stores-sales/payments/offline/check-money-order) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enabled] | Website | Legt fest, ob Kunden per Scheck oder Zahlungsanweisung zahlen können. Optionen: `Yes` / `No` |
| [!UICONTROL Title] | Shop-Ansicht | Der Name für diese Zahlungsmethode, der Kunden während des Checkouts angezeigt wird. |
| [!UICONTROL New Order Status] | Website | Bestimmt den ursprünglichen [Bestellstatus](../../stores-purchase/order-status.md) der Bestellungen, die per Scheck oder Zahlungsanweisung bezahlt wurden. Standardwert: `Pending` |
| [!UICONTROL Payment from Applicable Countries] | Website | Bestimmt die Länder, aus denen Sie die Zahlung per Scheck oder Zahlungsanweisung akzeptieren. Optionen: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Website | Gibt die Länder an, aus denen Sie die Zahlung per Scheck oder per Zahlungsanweisung akzeptieren. |
| [!UICONTROL Make Check Payable to] | Shop-Ansicht | Name der Stelle, an die Schecks und Zahlungsanweisungen zu zahlen sind. |
| [!UICONTROL Send Check to] | Shop-Ansicht | Die Straße oder das Postfach, an die Schecks und Zahlungsanweisungen gesendet werden sollen. |
| [!UICONTROL Minimum Order Total] | Website | Der kleinste Bestellbetrag, der per Scheck oder Zahlungsanweisung bezahlt werden kann. |
| [!UICONTROL Maximum Order Total] | Website | Der größte Bestellbetrag, der per Scheck oder Zahlungsanweisung bezahlt werden kann. <br/><br/>**_Hinweis:_** Eine Bestellung ist qualifiziert, wenn die Gesamtsumme zwischen der Mindest- oder Höchstauftragssumme liegt oder mit dieser übereinstimmt. |
| [!UICONTROL Sort Order] | Website | Eine Nummer, die die Bestellung bestimmt, dass die Zahlung per Scheck oder Zahlungsanweisung angezeigt wird, wenn sie mit anderen Zahlungsmethoden beim Checkout aufgelistet wird. Geben Sie `0` ein, um sie an den Anfang der Liste zu setzen. |

{style="table-layout:auto"}

### [!UICONTROL Bank Transfer Payment]

![Banküberweisung](./assets/payment-methods-bank-transfer-payment.png)<!-- zoom -->

<!-- [Bank Transfer Payment](https://experienceleague.adobe.com/de/docs/commerce-admin/stores-sales/payments/offline/bank-transfer) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enabled] | Website | Legt fest, ob Kunden bezahlen können, indem sie die Zahlung direkt von ihrer Bank auf Ihr Händlerkonto überweisen. Optionen: `Yes` / `No` |
| [!UICONTROL Title] | Shop-Ansicht | Der Name für diese Zahlungsmethode, der Kunden während des Checkouts angezeigt wird. |
| [!UICONTROL New Order Status] | Website | Bestimmt den ursprünglichen Bestellstatus, der Bestellungen zugewiesen wurde, die per Banküberweisung bezahlt wurden. Standardwert: `Pending` |
| [!UICONTROL Payment from Applicable Countries] | Website | Bestimmt die Länder, von denen Sie die Zahlung per Banküberweisung akzeptieren. Optionen: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Website | Gibt die Länder an, aus denen Sie die Zahlung per Banküberweisung akzeptieren. |
| [!UICONTROL Minimum Order Total] | Website | Der kleinste Bestellbetrag, der per Banküberweisung bezahlt werden kann. |
| [!UICONTROL Maximum Order Total] | Website | Der größte Bestellbetrag, der per Banküberweisung bezahlt werden kann. <br/><br/>**_Hinweis:_** Eine Bestellung ist qualifiziert, wenn die Gesamtsumme zwischen der Mindest- oder Höchstauftragssumme liegt oder mit dieser übereinstimmt. |
| [!UICONTROL Sort Order] | Website | Eine Zahl, die die Reihenfolge bestimmt, in der die Zahlung per Banküberweisung angezeigt wird, wenn sie beim Checkout mit anderen Zahlungsmethoden aufgelistet wird. Geben Sie `0` ein, um sie an den Anfang der Liste zu setzen. |

{style="table-layout:auto"}

### [!UICONTROL Payment on Account]

{{b2b-feature}}

![Zahlung auf Rechnung](./assets/payment-methods-payment-on-account.png)<!-- zoom -->

<!-- [Payment on Account](https://experienceleague.adobe.com/de/docs/commerce-admin/b2b/enable-basic-features#configure-payment-on-account) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enabled] | Website | Legt fest, ob Unternehmen Firmenkredite für Käufe verwenden können. Optionen: `Yes` / `No` |
| [!UICONTROL Title] | Shop-Ansicht | Der Name für diese Zahlungsmethode, der Kunden während des Checkouts angezeigt wird. |
| [!UICONTROL New Order Status] | Website | Bestimmt den Status von neuen Aufträgen, die einem Firmenkonto belastet werden. Optionen: `Pending (default)` / `Processing` / `Suspected Fraud` |
| [!UICONTROL Payment from Applicable Countries] | Website | Legt die Länder fest, in denen Unternehmen Einkäufe mit ihren Konten verrechnen dürfen. Optionen: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Website | Gibt die spezifischen Länder an, in denen Unternehmen Käufe mit ihren Konten verbuchen können. |
| [!UICONTROL Minimum Order Total] | Website | Gibt den kleinsten Bestellbetrag an, der einem Firmenkonto belastet werden kann. |
| [!UICONTROL Maximum Order Total] | Website | Der größte Auftragsbetrag, der einem Firmenkonto belastet werden kann. <br/><br/>**_Hinweis:_** Eine Bestellung ist qualifiziert, wenn die Gesamtsumme zwischen der Mindest- oder Höchstauftragssumme liegt oder mit dieser übereinstimmt. |
| [!UICONTROL Sort Order] | Website | Eine Zahl, die die Reihenfolge bestimmt, in der die Zahlung auf Konto angezeigt wird, wenn sie beim Checkout mit anderen Zahlungsmethoden aufgelistet wird. Geben Sie `0` ein, um sie an den Anfang der Liste zu setzen. |

{style="table-layout:auto"}

>[!NOTE]
>
>Die Zahlung auf Konto wird bei Bestellungen mit [mehreren Versandadressen](../../stores-purchase/shipping-settings.md#multiple-addresses) nicht unterstützt und wird nicht unter den Zahlungsoptionen angezeigt.

### [!UICONTROL Cash On Delivery Payment]

![Nachnahme](./assets/payment-methods-cash-on-delivery-payment.png)<!-- zoom -->

<!-- [Cash On Delivery Payment](../../stores-purchase/cash-on-delivery.html) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enabled] | Website | Legt fest, ob Kunden bezahlen können, indem sie die Zahlung direkt von ihrer Bank auf Ihr Händlerkonto überweisen. Optionen: `Yes` / `No` |
| [!UICONTROL Title] | Shop-Ansicht | Der Name für diese Zahlungsmethode, der Kunden während des Checkouts angezeigt wird. |
| [!UICONTROL New Order Status] | Website | Bestimmt den ursprünglichen Bestellstatus, der Bestellungen zugewiesen wurde, die per Banküberweisung bezahlt wurden. Standardwert: `Pending` |
| [!UICONTROL Payment from Applicable Countries] | Website | Bestimmt die Länder, von denen Sie die Zahlung per Banküberweisung akzeptieren. Optionen: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Website | Gibt die Länder an, aus denen Sie die Zahlung per Banküberweisung akzeptieren. |
| [!UICONTROL Minimum Order Total] | Website | Gibt den kleinsten Bestellbetrag an, der per Banküberweisung bezahlt werden kann. |
| [!UICONTROL Maximum Order Total] | Website | Der größte Bestellbetrag, der per Banküberweisung bezahlt werden kann. <br/><br/>**_Hinweis:_** Eine Bestellung ist qualifiziert, wenn die Gesamtsumme zwischen der Mindest- oder Höchstauftragssumme liegt oder mit dieser übereinstimmt. |
| [!UICONTROL Sort Order] | Website | Eine Zahl, die die Reihenfolge bestimmt, in der die Zahlung per Banküberweisung angezeigt wird, wenn sie beim Checkout mit anderen Zahlungsmethoden aufgelistet wird. Geben Sie `0` ein, um sie an den Anfang der Liste zu setzen. |

{style="table-layout:auto"}

### [!UICONTROL Zero Subtotal Checkout]

![Null Zwischensumme Checkout](./assets/payment-methods-zero-subtotal-checkout.png)<!-- zoom -->

<!-- [Zero Subtotal Checkout](../../stores-purchase/zero-subtotal-checkout.html) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Title] | Shop-Ansicht | Der Name, der während des Checkouts für diese Zahlungsmethode verwendet wird. Standardwert: Keine Zahlungsinformationen erforderlich |
| [!UICONTROL Enabled] | Website | Legt fest, ob der Store-Administrator einen Null-Zwischensummen-Checkout für die Verwaltung von Bestellungen mit einer Zwischensumme von null haben kann, z. B. eine Bestellung, die besteuert wurde, aber ein Rabatt hat den Betrag auf null reduziert. Optionen: `Yes` / `No` |
| [!UICONTROL New Order Status] | Website | Bestimmt den ursprünglichen Bestellstatus, der Bestellungen zugewiesen wurde, die als Zwischensumme Null Checkout verarbeitet wurden. Standardwert: `Pending` |
| [!UICONTROL Payment from Applicable Countries] | Website | Bestimmt die Länder, aus denen der Null-Zwischensumme-Checkout angewendet werden kann. Optionen: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Website | Gibt die spezifischen Länder an, für die ein Null-Zwischensumme-Checkout angewendet werden kann. |
| [!UICONTROL Sort Order] | Website | Eine Zahl, die die Reihenfolge bestimmt, in der der Titel angezeigt wird, z. B. „Keine Zahlungsinformationen erforderlich“, wird angezeigt, wenn sie während des Checkouts mit anderen Zahlungsmethoden aufgelistet wird. Geben Sie `0` ein, um sie an den Anfang der Liste zu setzen. |

{style="table-layout:auto"}

## [!UICONTROL Payment actions]

[!BADGE Nur PaaS]{type=Informative url="https://experienceleague.adobe.com/de/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."}

Zahlungsaktionen werden (_Zahlungsmethode)_. Die Zahlungsaktion bestimmt, wann die Mittel erfasst werden und wann Rechnungen für Ihre Aufträge erstellt werden.

Eine umfassende Liste der individuellen Konfigurationsoptionen finden Sie im Abschnitt Grundeinstellungen jedes einzelnen Artikels zur Zahlungsmethode .

| Zahlungsaktion | Beschreibung |
|--- |---|
| [!UICONTROL Authorization] | Genehmigt den Kauf, setzt jedoch die Mittel zurück. Der Betrag wird erst abgehoben, wenn er vom Händler eingezogen wurde. |
| [!UICONTROL Authorize] | Autorisiert das Konto des Käufers für die Bestellsumme, erfasst jedoch nicht die Zahlung. Zahlung durch Erstellen einer Rechnung erfassen. Autorisierte Bestellungen können annulliert oder storniert werden. |
| [!UICONTROL Authorize and Capture] | Autorisiert das Konto des Käufers für die Bestellsumme und erfasst die Zahlung. Eine Rechnung wird automatisch erstellt. Sie können eingezogene Beträge per Gutschrift zurückerstatten. Sie können eine Bestellung nicht mehr stornieren, nachdem die Zahlung erfasst wurde. |
| [!UICONTROL Charge on shipment] | Amazon erhält eine Erfassungsanfrage und belastet den Kunden, wenn in Commerce eine Rechnung erstellt wird. |
| [!UICONTROL Charge on order] | Amazon erstellt die Rechnung und belastet den Kunden bei der Bestellung. |
| [!UICONTROL Not Capture] | Wenn die Rechnung übermittelt wird, erfasst das System die Zahlung nicht. Es wird davon ausgegangen, dass Sie die Zahlung später über Commerce erfassen. Die fertige Rechnung enthält eine Schaltfläche „Erfassen“. Vor der Erfassung können Sie die Rechnung stornieren. Nach der Erfassung können Sie eine Gutschrift erstellen und die Rechnung stornieren. |
| [!UICONTROL Order] | Stellt eine Vereinbarung mit PayPal dar, die es dem Händler ermöglicht, einen oder mehrere Beträge bis zur Bestellsumme vom Käuferkonto des Kunden innerhalb eines bestimmten Zeitraums (bis zu 29 Tage) zu erfassen. |
| [!UICONTROL Sale] | Der Kaufbetrag wird autorisiert und sofort vom Konto des Kunden zurückgezogen. |

{style="table-layout:auto"}

>[!NOTE]
>
>Wählen Sie die Option _[!UICONTROL Not Capture]_&#x200B;nur aus, wenn Sie sicher sind, dass Sie die Zahlung später über Commerce erfassen werden. Sie können erst dann eine Gutschrift erstellen, wenn die Zahlung mit der Schaltfläche „Erfassen“ erfasst wurde.

## [!UICONTROL Purchase Order]

![Bestellung](./assets/payment-methods-purchase-order.png)<!-- zoom -->

<!-- [Purchase Order](../../stores-purchase/purchase-order.html) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enabled] | Website | Legt fest, ob Kunden per Bestellung (PO) bezahlen können. Optionen: `Yes` / `No` |
| [!UICONTROL Title] | Shop-Ansicht | Der Name dieser Zahlungsmethode, die Kunden während des Checkouts angezeigt wird. |
| [!UICONTROL New Order Status] | Website | Bestimmt den anfänglichen [Auftragsstatus](../../stores-purchase/order-status.md) der Bestellungen zugewiesen wurde, die von der Bestellung bezahlt wurden. Standardwert: Ausstehend |
| [!UICONTROL Payment from Applicable Countries] | Website | Bestimmt die Länder, aus denen Sie die Zahlung per Bestellung akzeptieren. Optionen: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Website | Gibt die Länder an, aus denen Sie die Zahlung per Bestellung akzeptieren. |
| [!UICONTROL Minimum Order Total] | Website | Der kleinste Bestellbetrag, der von der Bestellung bezahlt werden kann. |
| [!UICONTROL Maximum Order Total] | Website | Der größte Auftragsbetrag, der von der Bestellung bezahlt werden kann. <br/><br/>**_Hinweis:_** Eine Bestellung ist qualifiziert, wenn die Gesamtsumme zwischen der Mindest- oder Höchstauftragssumme liegt oder mit dieser übereinstimmt. |
| [!UICONTROL Sort Order] | Website | Eine Zahl, die die Reihenfolge bestimmt, in der die Zahlung per Bestellung angezeigt wird, wenn sie mit anderen Zahlungsmethoden beim Checkout aufgelistet wird. Geben Sie `0` ein, um sie an den Anfang der Liste zu setzen. |

{style="table-layout:auto"}
