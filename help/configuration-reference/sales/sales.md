---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Sales]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Sales] &gt; [!UICONTROL Sales] des Commerce Admin-Bereichs.
exl-id: 29091aab-e608-4e68-a6fe-f2808c78581c
feature: Configuration, Orders
source-git-commit: 8d73a3a635c20e636c4b8bde41a4f807d3fd9f2e
workflow-type: tm+mt
source-wordcount: '1226'
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL Sales]

{{config}}

## [!UICONTROL General]

![Allgemein](./assets/sales-general.png)<!-- zoom -->

<!-- [General](https://experienceleague.adobe.com/de/docs/commerce-admin/stores-sales/site-store/sales-documents) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Hide Customer IP] | Shop-Ansicht | Legt fest, ob die Kunden-IP-Adresse in Bestellungen, Rechnungen, Lieferungen und Gutschriften angezeigt wird. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Checkout Totals Sort Order]

![Checkout-Summen - Sortierreihenfolge](./assets/sales-checkout-totals-sort-order.png)<!-- zoom -->

<!-- [Checkout Totals Sort Order](https://experienceleague.adobe.com/de/docs/commerce-admin/stores-sales/point-of-purchase/checkout/checkout-totals-sort-order) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Subtotal] | Website | Eine Zahl, die bestimmt, wann die Zwischensumme im Verhältnis zu anderen Checkout-Summen berechnet wird. Standardwert: `10` |
| [!UICONTROL Discount] | Website | Eine Zahl, die bestimmt, wann der Rabatt im Verhältnis zu anderen Checkout-Summen berechnet wird. Standardwert: `20` |
| [!UICONTROL Shipping] | Website | Eine Zahl, die bestimmt, wann der Versand im Verhältnis zu anderen Checkout-Summen berechnet wird. Standardwert: `30` |
| [!UICONTROL Tax] | Website | Eine Zahl, die bestimmt, wann die Steuer im Verhältnis zu anderen Checkout-Summen berechnet wird. Standardwert: `40` |
| [!UICONTROL Fixed Product Tax] | Website | Eine Zahl, die bestimmt, wann die feste Produktsteuer im Verhältnis zu anderen Checkout-Summen berechnet wird. Standardwert: `50` |
| [!UICONTROL Grand Total] | Website | Eine Zahl, die bestimmt, wann die Gesamtsumme im Verhältnis zu anderen Checkout-Gesamtsummen berechnet wird. Standardwert: `100` |

{style="table-layout:auto"}

## [!UICONTROL Reorder]

![Neu anordnen](./assets/sales-reorder.png)<!-- zoom -->

<!-- [Reorder](https://experienceleague.adobe.com/de/docs/commerce-admin/stores-sales/shopper-tools/reorders-allow) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Allow Reorder] | Shop-Ansicht | Legt fest, ob Kunden ihre Konten neu bestellen können. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Allow Zero Grand Total]

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Allow Zero Grand Total for Credit Memo] | Shop-Ansicht | Bestimmt die Möglichkeit, eine Gutschrift mit einem Gesamtwert von null zu erstellen. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Invoice and Packing Slip Design]

![Rechnung und Lieferschein-Design](./assets/sales-invoice-packing-slip-design.png)<!-- zoom -->

<!-- [Invoice and Packing Slip Design](https://experienceleague.adobe.com/de/docs/commerce-admin/stores-sales/site-store/sales-documents) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Logo for PDF Print-outs] | Shop-Ansicht | Identifiziert die Logodatei, die in der Kopfzeile von PDF-Rechnungen und Lieferscheinen angezeigt wird. Zulässige Dateitypen: <br/>JPG/JPEG <br/>TIF/TIFF <br/>PNG |
| [!UICONTROL Logo for HTML Print View] | Shop-Ansicht | Identifiziert die Logodatei, die in der Kopfzeile der HTML-Druckansicht von Rechnungen und Lieferscheinen angezeigt wird. Zulässige Dateitypen: <br/>JPG /JPEG <br/>GIF <br/>PNG |
| [!UICONTROL Address] | Shop-Ansicht | Die Store-Adresse, wie sie auf Rechnungen und Lieferscheinen erscheinen soll. |

{style="table-layout:auto"}

## [!UICONTROL Minimum Order Amount]

![Mindestbestellmenge](./assets/sales-minimum-order-amount.png)<!-- zoom -->

<!-- [Minimum Order Amount](https://experienceleague.adobe.com/de/docs/commerce-admin/stores-sales/point-of-purchase/cart/cart-configuration#minimum-order-amount) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable] | Website | Legt fest, ob ein Mindestbestellbetrag für die Website festgelegt wird. Optionen: `Yes` / `No` |
| [!UICONTROL Minimum Amount] | Website | Gibt die Mindest-Zwischensumme für die Bestellung nach der Anwendung von Rabatten an. |
| [!UICONTROL Include Discount Amount] | Website | Legt fest, ob der Mindestbestellbetrag angewendete Rabatte enthält. Optionen: `Yes` / `No` |
| [!UICONTROL Include Tax to Amount] | Website | Legt fest, ob der Mindestbestellbetrag die Steuer enthält. Optionen: `Yes` / `No` |
| [!UICONTROL Description Message] | Shop-Ansicht | Bestimmt die Nachricht, die oben im Warenkorb angezeigt wird, wenn die Summe des Warenkorbs kleiner als der Mindestbestellbetrag ist. Wenn Sie das Feld leer lassen, wird die folgende Standardmeldung angezeigt: `Minimum order amount is $[minimum_amount]` |
| [!UICONTROL Error to Show in Shopping Cart] | Shop-Ansicht | Bestimmt die Nachricht, die vom Mini-Warenkorb oder Checkout-Link angezeigt wird, wenn der Bestellbetrag kleiner als der erforderliche Mindestbestellbetrag ist. Wenn Sie das Feld leer lassen, wird eine Standardmeldung angezeigt. |
| [!UICONTROL Validate Each Address Separately in Multi-address Checkout] | Website | Bei Bestellungen mit mehreren Artikeln bestimmt , ob Bestellartikel, die an separate Adressen gesendet werden, den Mindestbestellbetrag erfüllen. Optionen: `Yes` / `No` |
| [!UICONTROL Multi-address Description Message] | Shop-Ansicht | Bei Bestellungen mit mehreren Adressen bestimmt die Nachricht, die im Warenkorb angezeigt wird, wenn die an eine Adresse gesendeten Artikel kleiner als der Mindestbestellbetrag sind. |
| [!UICONTROL Multi-address Error to Show in Shopping Cart] | Shop-Ansicht | Bei Bestellungen mit mehreren Adressen bestimmt die Nachricht, die über den Mini-Warenkorb oder den Checkout-Link angezeigt wird, wenn der Bestellbetrag kleiner als der erforderliche Mindestbestellbetrag ist. Wenn Sie das Feld leer lassen, wird eine Standardmeldung angezeigt. |

{style="table-layout:auto"}

## [!UICONTROL Dashboard]

![Dashboard](./assets/sales-dashboard.png)<!-- zoom -->

<!-- [Dashboard](https://experienceleague.adobe.com/de/docs/commerce-admin/start/admin/tools/admin-dashboard) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Use Aggregated Data] | Global | Legt fest, ob aggregierte Echtzeit-Verkaufsdaten zur Erstellung von Dashboard-Momentaufnahme-Berichten verwendet werden. Wenn Sie eine große Datenmenge verarbeiten müssen, kann die Leistung verbessert werden, indem die Anzeige von Echtzeitdaten deaktiviert wird. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Orders Cron Settings]

![Bestellungen Cron-Einstellungen](./assets/sales-orders-cron-settings.png)<!-- zoom -->

<!-- [Orders Cron Settings](https://experienceleague.adobe.com/de/docs/commerce-admin/systems/tools/cron) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Pending Payment Order Lifetime] | Website | Bestimmt die Lebensdauer ausstehender Bestellungen in Minuten. Standardeinstellung: `480` Minuten (8 Stunden) |

{style="table-layout:auto"}

## [!UICONTROL Promotions]

[!BADGE nur SaaS]{type=Positive url="https://experienceleague.adobe.com/de/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce as a Cloud Service-Projekte (von Adobe verwaltete SaaS-Infrastruktur)."}

![Einstellungen für Promotions](./assets/sales-promotions-settings.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Apply Catalog Price Rule on Grouped Price] | Global | Aktiviert [Preisstufe für Katalogpreisregeln](../../catalog/product-price-tier.md) wenn die Menge eines Stufenpreises auf `1` festgelegt ist.  Optionen: `Yes` / `No` |

## [!UICONTROL Gift Options]

![Geschenkoptionen](./assets/sales-gift-options.png)<!-- zoom -->

<!-- [Gift Options](https://experienceleague.adobe.com/de/docs/commerce-admin/stores-sales/point-of-purchase/cart/cart-configuration#gift-options) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Allow Gift Messages on Order Level] | Website | Geben Sie an, ob eine Geschenknachricht für die gesamte Bestellung hinzugefügt werden kann. |
| [!UICONTROL Allow Gift Messages on Order Items] | Website | Geben Sie an, ob eine Geschenknachricht für einen einzelnen Bestellartikel hinzugefügt werden kann. |
| [!UICONTROL Allow Gift Wrapping on Order Level] | Website | ![Adobe Commerce](../../assets/adobe-logo.svg) (nur Adobe Commerce) Geben Sie an, ob Geschenkverpackungen für die gesamte Bestellung hinzugefügt werden können. |
| [!UICONTROL Allow Gift Wrapping for Order Items] | Website | ![Adobe Commerce](../../assets/adobe-logo.svg) (nur Adobe Commerce) Geben Sie an, ob Geschenkverpackungen für den jeweiligen Bestellartikel hinzugefügt werden können. |
| [!UICONTROL Allow Gift Receipt] | Website | ![Adobe Commerce](../../assets/adobe-logo.svg) (nur Adobe Commerce) Geben Sie an, ob für die Bestellung eine Geschenkquittung hinzugefügt werden kann. |
| [!UICONTROL Allow Printed Card] | Website | ![Adobe Commerce](../../assets/adobe-logo.svg) (nur Adobe Commerce) Geben Sie an, ob für die Bestellung eine gedruckte Karte hinzugefügt werden kann. |
| [!UICONTROL Default Price for Printed Card] | Website | ![Adobe Commerce](../../assets/adobe-logo.svg) (nur Adobe Commerce) Geben Sie den Standardpreis für die gedruckte Karte an. |

{style="table-layout:auto"}

## [!UICONTROL Minimum Advertised Price]

![Angebotspreis](./assets/sales-minimum-advertised-price.png)<!-- zoom -->

<!-- [Minimum Advertised Price](https://experienceleague.adobe.com/de/docs/commerce-admin/catalog/products/pricing/product-price-minimum-advertised) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable MAP] | Website | Aktiviert den Mindestpreis für Werbung in Ihrem Geschäft. Optionen: `Yes` / `No` |
| [!UICONTROL Display Actual Price] | Website | Bestimmt, wo der tatsächliche Preis eines Produkts für den Kunden sichtbar ist. Optionen: <br/>**`In Cart`**- Zeigt den tatsächlichen Produktpreis im Warenkorb an.<br/>**`Before Order Confirmation`** - Zeigt den tatsächlichen Produktpreis am Ende des Checkout-Prozesses an, kurz bevor die Bestellung bestätigt wird. <br/>**`On Gesture`**- Zeigt den tatsächlichen Produktpreis in einem Popup an, wenn der Kunde auf „Klick für Preis“ oder „Was ist das?“ klickt. Link. |
| [!UICONTROL Default Popup Text Message] | Shop-Ansicht | Die Textmeldung, die angezeigt wird, wenn der Kunde den Link „Klick für Preis“ auf einer Kategorieliste oder Produktansichtsseite auswählt. |
| [!UICONTROL Default "What's This" Text Message] | Shop-Ansicht | Die Textmeldung, die angezeigt wird, wenn der Kunde auf „Was ist das?“ klickt. Link von der Produktansichtsseite. |
| [!UICONTROL Manufacturer's Suggested Retail Price] | Global | Der vom Hersteller vorgeschlagene Einzelhandelspreis (MSRP). |

{style="table-layout:auto"}

## [!UICONTROL Multicoupon Settings]

{{ee-feature}}

![MultiCoupon-Einstellungen](./assets/sales-multicoupon-settings.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Maximum number of coupons per order] | Website | Bestimmt die maximal zulässige Anzahl von Coupons pro Bestellung. Diese Funktion ist nur in Admin, GraphQL und der REST-API verfügbar. Und es ist **_nicht verfügbar_** in der Storefront. |

{style="table-layout:auto"}

## [!UICONTROL Order by SKU Settings]

{{ee-feature}}

![Sortieren nach SKU-Einstellungen](./assets/sales-order-by-sku-settings.png)<!-- zoom -->

<!-- [Order by SKU Settings](https://experienceleague.adobe.com/de/docs/commerce-admin/stores-sales/point-of-purchase/cart/order-by-sku) -->

![Sortieren nach SKU-Einstellungen für Kundengruppe](./assets/sales-order-by-sku-settings.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable Order by SKU on My Account in Storefront] | Website | Legt fest, ob Order by SKU im Kundenkonto-Dashboard verfügbar ist. Optionen: <br/>**`Yes, for Everyone`**- Die Registerkarte „Bestellung nach SKU“ wird im Konto-Dashboard aller Kunden angezeigt.<br/>**`Yes, for Specified Customer Groups`** - Die Registerkarte Order By SKU wird im Konto-Dashboard für Mitglieder bestimmter Gruppen oder eines freigegebenen Katalogs angezeigt. <br/>**`No`**- Die Registerkarte „Bestellung nach SKU“ ist im Kundenkonto nicht verfügbar. |
| [!UICONTROL Customer Groups] | Website | Bestimmt die Kundengruppen. Optionen: `General` / `Retailer` / `Wholesale` |

{style="table-layout:auto"}

## [!UICONTROL Instant Purchase]

![Sofortiger Kauf](./assets/sales-instant-purchase.png)<!-- zoom -->

<!-- [Instant Purchase](https://experienceleague.adobe.com/de/docs/commerce-admin/stores-sales/point-of-purchase/checkout-instant-purchase) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enabled] | Shop-Ansicht | Aktiviert den Sofortkauf für die Store-Ansicht, wenn für die Zahlungsmethode, z. B. Braintree, Vault aktiviert ist. Optionen: `Yes` / `No` |
| [!UICONTROL Button Text] | Shop-Ansicht | Gibt den Text an, der auf der Schaltfläche Sofortkauf angezeigt wird. Der Standardtext ist `Instant Purchase`. |

{style="table-layout:auto"}

## [!UICONTROL Rate Limiting]

![Ratenbegrenzung](assets/sales-rate-limiting.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--------------------------------------------------------|--- |------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable rate limiting for placing orders] | Shop-Ansicht | Bestimmt, ob die Ratenbegrenzung für die Platzierung von Bestellungen in der Store-Ansicht verwendet wird (der Standardwert lautet `No`). Optionen: `Yes` / `No`. |
| [!UICONTROL Requests limit per authenticated customer] | Shop-Ansicht | Die Anzahl der Kaufanfragen, die ein authentifizierter Kunde während des Zeitraums stellen kann. Das standardmäßige Limit ist `10`. |
| [!UICONTROL Requests limit per guest] | Shop-Ansicht | Die Anzahl der Kaufanfragen, die ein nicht authentifizierter Kunde während des angegebenen Zeitraums tätigen kann. Der Standardwert ist `50`. |
| [!UICONTROL Counter resets in a ...] | Shop-Ansicht | Der Zeitraum, in dem ein authentifizierter/nicht authentifizierter Kunde eine bestimmte Anzahl von Kaufanfragen stellen kann (der Standardwert lautet `Minute`). Optionen: `Minute` / `Hour` /`Day` |

{style="table-layout:auto"}

## [!UICONTROL Orders, Invoices, Shipments, Credit Memos Archiving]

{{ee-feature}}

![Bestellungen, Rechnungen, Lieferungen, Gutschriften Archivierung](./assets/sales-orders-invoices-shipments-credit-memos-archiving.png)<!-- zoom -->

Weitere Informationen zum Ändern dieser Einstellungen finden Sie unter [Konfigurieren des Bestellarchivs](../../stores-purchase/order-archive.md#configure-the-order-archive) im Handbuch _Stores und Kauferlebnis_.

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable Archiving] | Global | Legt fest, ob die Archivierung aktiviert ist. Optionen: `Yes` / `No` |
| [!UICONTROL Archive Orders Purchased] | Global | Bestimmt die Anzahl der Tage, die vergehen, bis eine abgeschlossene Bestellung archiviert wird. Standardwert: `30` |
| [!UICONTROL Order  Statuses to be Archived] | Global | Bestimmt den [Status](../../stores-purchase/order-status.md) der zu archivierenden Bestellungen. Standardmäßig werden Bestellungen mit dem Status Abgeschlossen oder Geschlossen archiviert. Optionen: `Pending` / `Processing` / `Suspected Fraud` / `Complete` / `Closed` / `Canceled` / `On Hold` |

{style="table-layout:auto"}

## [!UICONTROL RMA Settings]

{{ee-feature}}

![RMA-Einstellungen](./assets/sales-rma-settings.png)<!-- zoom -->

Weitere Informationen zum Ändern dieser Einstellungen finden Sie unter [Konfigurieren von Rücksendungen](../../stores-purchase/rma-configure.md) im _Handbuch zu Stores und Kauferlebnissen_.

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable RMA on Storefront] | Website | Legt fest, ob Kunden RMA-Anfragen in der Storefront erstellen und anzeigen können. RMA kann sowohl auf neue als auch auf bestehende Bestellungen angewendet werden. RMA ist für die Storefront standardmäßig nicht aktiviert. Optionen: `Yes` / `No` |
| [!UICONTROL Enable RMA on Product Level] | Website | Bestimmt den Standardwert für das Feld RMA aktivieren in den Produktinformationen. |
| [!UICONTROL Use Store Address] | Website | Bestimmt den Kontaktnamen und die Adresse, die für Sendungen von zurückgegebenen Waren verwendet werden. Optionen: <br/>**`Yes`**- Verwendet die [Point of Origin](../../stores-purchase/shipping-settings.md#point-of-origin) Adresse aus den Versandeinstellungen.<br/>**`No`** - Öffnet das Adressformular, in das Sie eine andere Adresse eingeben können. |

{style="table-layout:auto"}
