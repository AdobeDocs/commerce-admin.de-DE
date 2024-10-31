---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Sales]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Sales] &gt; [!UICONTROL Sales] des Commerce-Administrators.
exl-id: 29091aab-e608-4e68-a6fe-f2808c78581c
feature: Configuration, Orders
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '1186'
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL Sales]

{{config}}

## [!UICONTROL General]

![Allgemein](./assets/sales-general.png)<!-- zoom -->

<!-- [General](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/site-store/sales-documents) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Hide Customer IP] | Store-Ansicht | Bestimmt, ob die IP-Adresse des Kunden auf Bestellungen, Rechnungen, Sendungen und Kreditkarten angezeigt wird. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Checkout Totals Sort Order]

![Sortierreihenfolge insgesamt auschecken](./assets/sales-checkout-totals-sort-order.png)<!-- zoom -->

<!-- [Checkout Totals Sort Order](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/checkout/checkout-totals-sort-order) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Subtotal] | Webseite | Eine Zahl, die bestimmt, wann die Zwischensumme in Bezug auf andere Checkout-Summen berechnet wird. Standardwert: `10` |
| [!UICONTROL Discount] | Webseite | Eine Zahl, die bestimmt, wann der Rabatt im Vergleich zu anderen Checkout-Summen berechnet wird. Standardwert: `20` |
| [!UICONTROL Shipping] | Webseite | Eine Zahl, die bestimmt, wann der Versand im Verhältnis zu anderen Checkout-Summen berechnet wird. Standardwert: `30` |
| [!UICONTROL Tax] | Webseite | Eine Zahl, die bestimmt, wann die Steuer im Verhältnis zu anderen Checkout-Summen berechnet wird. Standardwert: `40` |
| [!UICONTROL Fixed Product Tax] | Webseite | Eine Zahl, die bestimmt, wann die feste Produktsteuer in Bezug auf andere Checkout-Summen berechnet wird. Standardwert: `50` |
| [!UICONTROL Grand Total] | Webseite | Eine Zahl, die bestimmt, wann die Gesamtsumme in Bezug auf andere Checkout-Summen berechnet wird. Standardwert: `100` |

{style="table-layout:auto"}

## [!UICONTROL Reorder]

![Neu anordnen](./assets/sales-reorder.png)<!-- zoom -->

<!-- [Reorder](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/shopper-tools/reorders-allow) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Allow Reorder] | Store-Ansicht | Stellt fest, ob die Kunden ihre Konten neu anordnen können. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Allow Zero Grand Total]

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Allow Zero Grand Total for Credit Memo] | Store-Ansicht | Ermittelt die Möglichkeit, ein Credit Memo mit einer Nullsumme zu erstellen. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Invoice and Packing Slip Design]

![Invoice and Packing Slip Design](./assets/sales-invoice-packing-slip-design.png)<!-- zoom -->

<!-- [Invoice and Packing Slip Design](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/site-store/sales-documents) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Logo for PDF Print-outs] | Store-Ansicht | Identifiziert die Logodatei, die in der Kopfzeile von PDF-Rechnungen und Packungsbeilagen angezeigt wird. Zulässige Dateitypen: <br/>JPG/JPEG <br/>TIF/TIFF <br/>PNG |
| [!UICONTROL Logo for HTML Print View] | Store-Ansicht | Identifiziert die Logodatei, die in der Kopfzeile der HTML-Druckansicht von Rechnungen und Packungsbeilagen angezeigt wird. Zulässige Dateitypen: <br/>JPG /JPEG <br/>GIF <br/>PNG |
| [!UICONTROL Address] | Store-Ansicht | Die Adresse des Lagers, wie sie auf Rechnungen und Packstücken erscheinen soll. |

{style="table-layout:auto"}

## [!UICONTROL Minimum Order Amount]

![Mindestbestellbetrag](./assets/sales-minimum-order-amount.png)<!-- zoom -->

<!-- [Minimum Order Amount](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/cart/cart-configuration#minimum-order-amount) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable] | Webseite | Bestimmt, ob ein Mindestbestellbetrag für die Site festgelegt ist. Optionen: `Yes` / `No` |
| [!UICONTROL Minimum Amount] | Webseite | Gibt die minimale Zwischensumme an, d. h. die Reihenfolge nach Anwendung der Rabatte. |
| [!UICONTROL Include Discount Amount] | Webseite | Bestimmt, ob der Mindestbestellbetrag angewendete Rabatte enthält. Optionen: `Yes` / `No` |
| [!UICONTROL Include Tax to Amount] | Webseite | Bestimmt, ob der Mindestbestellbetrag Steuern enthält. Optionen: `Yes` / `No` |
| [!UICONTROL Description Message] | Store-Ansicht | Bestimmt die Meldung, die oben im Warenkorb angezeigt wird, wenn die Warenkorbsumme kleiner als der Mindestbestellwert ist. Wenn Sie das Feld leer lassen, wird die folgende Standardmeldung angezeigt: `Minimum order amount is $[minimum_amount]` |
| [!UICONTROL Error to Show in Shopping Cart] | Store-Ansicht | Bestimmt die Meldung, die über den Mini-Warenkorb- oder Checkout-Link angezeigt wird, wenn der Bestellbetrag unter dem erforderlichen Mindestbestellbetrag liegt. Wenn Sie das Feld leer lassen, wird eine Standardmeldung angezeigt. |
| [!UICONTROL Validate Each Address Separately in Multi-address Checkout] | Webseite | Stellt bei Bestellungen mit mehreren Artikeln fest, ob die Bestellgegenstände, die an verschiedene Adressen verteilt werden, den Mindestbestellwert erreichen. Optionen: `Yes` / `No` |
| [!UICONTROL Multi-address Description Message] | Store-Ansicht | Bei Bestellungen mit mehreren Adressen bestimmt die Nachricht, die im Warenkorb angezeigt wird, wenn die an eine Adresse gesendeten Artikel kleiner als der Mindestbestellbetrag sind. |
| [!UICONTROL Multi-address Error to Show in Shopping Cart] | Store-Ansicht | Bei Bestellungen mit mehreren Adressen bestimmt die Nachricht, die über den Mini-Warenkorb oder Checkout-Link angezeigt wird, wenn der Bestellbetrag unter dem erforderlichen Mindestbestellbetrag liegt. Wenn Sie das Feld leer lassen, wird eine Standardmeldung angezeigt. |

{style="table-layout:auto"}

## [!UICONTROL Dashboard]

![Dashboard](./assets/sales-dashboard.png)<!-- zoom -->

<!-- [Dashboard](https://experienceleague.adobe.com/en/docs/commerce-admin/start/admin/tools/admin-dashboard) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Use Aggregated Data] | Global | Bestimmt, ob aggregierte Verkaufsdaten in Echtzeit verwendet werden, um Dashboard-Momentaufnahmen-Berichte zu erstellen. Wenn Sie eine große Menge an zu verarbeitenden Daten haben, kann die Leistung verbessert werden, indem die Anzeige von Echtzeitdaten deaktiviert wird. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Orders Cron Settings]

![Bestellungen Cron Settings](./assets/sales-orders-cron-settings.png)<!-- zoom -->

<!-- [Orders Cron Settings](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/tools/cron) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Pending Payment Order Lifetime] | Webseite | Bestimmt die Lebensdauer ausstehender Bestellungen in Minuten. Standardeinstellung: `480` Minuten (8 Stunden) |

{style="table-layout:auto"}

## [!UICONTROL Gift Options]

![Geschenkoptionen](./assets/sales-gift-options.png)<!-- zoom -->

<!-- [Gift Options](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/cart/cart-configuration#gift-options) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Allow Gift Messages on Order Level] | Webseite | Geben Sie an, ob eine Geschenknachricht für die gesamte Bestellung hinzugefügt werden kann. |
| [!UICONTROL Allow Gift Messages on Order Items] | Webseite | Geben Sie an, ob eine Geschenknachricht für einen einzelnen Bestellartikel hinzugefügt werden kann. |
| [!UICONTROL Allow Gift Wrapping on Order Level] | Webseite | ![Adobe Commerce](../../assets/adobe-logo.svg) (nur Adobe Commerce) Geben Sie an, ob eine Geschenkverpackung für die gesamte Bestellung hinzugefügt werden kann. |
| [!UICONTROL Allow Gift Wrapping for Order Items] | Webseite | ![Adobe Commerce](../../assets/adobe-logo.svg) (nur Adobe Commerce) Geben Sie an, ob für den einzelnen Bestellartikel eine Geschenkverpackung hinzugefügt werden kann. |
| [!UICONTROL Allow Gift Receipt] | Webseite | ![Adobe Commerce](../../assets/adobe-logo.svg) (nur Adobe Commerce) Geben Sie an, ob ein Geschenkgutschein für die Bestellung hinzugefügt werden kann. |
| [!UICONTROL Allow Printed Card] | Webseite | ![Adobe Commerce](../../assets/adobe-logo.svg) (nur Adobe Commerce) Geben Sie an, ob eine gedruckte Karte für die Bestellung hinzugefügt werden kann. |
| [!UICONTROL Default Price for Printed Card] | Webseite | ![Adobe Commerce](../../assets/adobe-logo.svg) (nur Adobe Commerce) Geben Sie den Standardpreis für die gedruckte Karte an. |

{style="table-layout:auto"}

## [!UICONTROL Minimum Advertised Price]

![Mindestpreis für Werbung](./assets/sales-minimum-advertised-price.png)<!-- zoom -->

<!-- [Minimum Advertised Price](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/products/pricing/product-price-minimum-advertised) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable MAP] | Webseite | Aktiviert den Mindestpreis für Werbung für Ihren Store. Optionen: `Yes` / `No` |
| [!UICONTROL Display Actual Price] | Webseite | Bestimmt, wo der tatsächliche Preis eines Produkts für den Kunden sichtbar ist. Optionen: <br/>**`In Cart`**- Zeigt den tatsächlichen Produktpreis im Warenkorb an.<br/>**`Before Order Confirmation`** - Zeigt den tatsächlichen Produktpreis am Ende des Checkout-Prozesses an, kurz bevor die Bestellung bestätigt wird. <br/>**`On Gesture`**- Zeigt den tatsächlichen Produktpreis in einem Popup an, wenn der Kunde auf &quot;Zum Preis klicken&quot;oder &quot;Was ist das?&quot; klickt. -Link. |
| [!UICONTROL Default Popup Text Message] | Store-Ansicht | Die Textnachricht, die angezeigt wird, wenn der Kunde auf einer Kategorienliste oder Produktansichtsseite den Link &quot;Zum Preis klicken&quot;auswählt. |
| [!UICONTROL Default "What's This" Text Message] | Store-Ansicht | Die Textnachricht, die angezeigt wird, wenn der Kunde auf &quot;Was ist das?&quot; klickt auf der Produktansichtsseite. |
| [!UICONTROL Manufacturer's Suggested Retail Price] | Global | Der vom Hersteller vorgeschlagene Einzelhandelspreis (MSRP). |

{style="table-layout:auto"}

## [!UICONTROL Multicoupon Settings]

{{ee-feature}}

![Multicoupon-Einstellungen](./assets/sales-multicoupon-settings.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Maximum number of coupons per order] | Webseite | Bestimmt die maximal zulässige Anzahl von Coupons pro Bestellung. Diese Funktion ist nur in der Admin-, GraphQL- und REST-API verfügbar. Und es ist **_nicht verfügbar_** in der Storefront. |

{style="table-layout:auto"}

## [!UICONTROL Order by SKU Settings]

{{ee-feature}}

![Bestellen nach SKU-Einstellungen](./assets/sales-order-by-sku-settings.png)<!-- zoom -->

<!-- [Order by SKU Settings](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/cart/order-by-sku) -->

![Bestellen nach SKU-Einstellungen für die Kundengruppe](./assets/sales-order-by-sku-settings.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable Order by SKU on My Account in Storefront] | Webseite | Bestimmt, ob die Option Bestellung nach SKU im Dashboard des Kundenkontos verfügbar ist. Optionen: <br/>**`Yes, for Everyone`**- Die Registerkarte Bestellung nach SKU wird im Konto-Dashboard aller Kunden angezeigt.<br/>**`Yes, for Specified Customer Groups`** - Die Registerkarte Bestellung nach SKU wird im Konto-Dashboard für Mitglieder bestimmter Gruppen oder eines freigegebenen Katalogs angezeigt. <br/>**`No`**- Die Registerkarte &quot;Bestellung nach SKU&quot;ist im Kundenkonto nicht verfügbar. |
| [!UICONTROL Customer Groups] | Webseite | Bestimmt die Kundengruppen. Optionen: `General` / `Retailer` / `Wholesale` |

{style="table-layout:auto"}

## [!UICONTROL Instant Purchase]

![Sofortiger Kauf](./assets/sales-instant-purchase.png)<!-- zoom -->

<!-- [Instant Purchase](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/checkout-instant-purchase) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enabled] | Store-Ansicht | Aktiviert &quot;Instant Purchase&quot;für die Store-Ansicht, wenn die Zahlungsmethode (z. B. Braintree) Vault aktiviert hat. Optionen: `Yes` / `No` |
| [!UICONTROL Button Text] | Store-Ansicht | Gibt den Text an, der auf der Schaltfläche Sofortiger Kauf angezeigt wird. Der Standardtext lautet `Instant Purchase`. |

{style="table-layout:auto"}

## [!UICONTROL Rate Limiting]

![Ratenbegrenzung](assets/sales-rate-limiting.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--------------------------------------------------------|--- |------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable rate limiting for placing orders] | Store-Ansicht | Bestimmt, ob die Ratenbegrenzung für die Platzierung von Bestellungen aus der Store-Ansicht verwendet wird (Standard ist `No`). Optionen: `Yes` / `No`. |
| [!UICONTROL Requests limit per authenticated customer] | Store-Ansicht | Die Anzahl der Kaufanfragen, die ein authentifizierter Kunde während des Zeitraums stellen kann. Der Standardwert ist `10`. |
| [!UICONTROL Requests limit per guest] | Store-Ansicht | Die Anzahl der Kaufanfragen, die ein nicht authentifizierter Kunde während des angegebenen Zeitraums stellen kann. Der Standardwert ist `50`. |
| [!UICONTROL Counter resets in a ...] | Store-Ansicht | Der Zeitraum, in dem ein authentifizierter/nicht authentifizierter Kunde eine bestimmte Anzahl von Kaufanfragen stellen kann (der Standardwert ist `Minute`). Optionen: `Minute` / `Hour` /`Day` |

{style="table-layout:auto"}

## [!UICONTROL Orders, Invoices, Shipments, Credit Memos Archiving]

{{ee-feature}}

![Bestellungen, Rechnungen, Sendungen, Archivierung von Kreditkarten](./assets/sales-orders-invoices-shipments-credit-memos-archiving.png)<!-- zoom -->

Weitere Informationen zum Ändern dieser Einstellungen finden Sie unter [Konfigurieren des Bestellarchivs](../../stores-purchase/order-archive.md#configure-the-order-archive) im Handbuch _Stores and Purchase Experience Guide_.

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable Archiving] | Global | Bestimmt, ob die Archivierung aktiviert ist. Optionen: `Yes` / `No` |
| [!UICONTROL Archive Orders Purchased] | Global | Bestimmt die Anzahl der Tage, die vergangen sind, bevor eine abgeschlossene Bestellung archiviert wird. Standardwert: `30` |
| [!UICONTROL Order  Statuses to be Archived] | Global | Bestimmt den [Status](../../stores-purchase/order-status.md) der zu archivierenden Bestellungen. Standardmäßig werden Bestellungen mit dem Status &quot;Abgeschlossen&quot;oder &quot;Geschlossen&quot;archiviert. Optionen: `Pending` / `Processing` / `Suspected Fraud` / `Complete` / `Closed` / `Canceled` / `On Hold` |

{style="table-layout:auto"}

## [!UICONTROL RMA Settings]

{{ee-feature}}

![RMA-Einstellungen](./assets/sales-rma-settings.png)<!-- zoom -->

Weitere Informationen zum Ändern dieser Einstellungen finden Sie unter [Rückgabe konfigurieren](../../stores-purchase/rma-configure.md) im Handbuch _Stores and Purchase Experience Guide_.

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable RMA on Storefront] | Webseite | Ermittelt, ob Kunden RMA-Anforderungen aus der Storefront erstellen und anzeigen können. RMA kann sowohl auf neue als auch auf bestehende Bestellungen angewendet werden. Standardmäßig ist RMA für die Storefront nicht aktiviert. Optionen: `Yes` / `No` |
| [!UICONTROL Enable RMA on Product Level] | Webseite | Legt den Standardwert für das Feld RMA aktivieren in den Produktinformationen fest. |
| [!UICONTROL Use Store Address] | Webseite | Bestimmt den Kontaktnamen und die Adresse, die für Sendungen von zurückgegebenen Waren verwendet werden. Optionen: <br/>**`Yes`**- Verwendet die Adresse [Ausgangspunkt](../../stores-purchase/shipping-settings.md#point-of-origin) aus den Versandeinstellungen.<br/>**`No`** - Öffnet das Adressformular, in das Sie eine alternative Adresse eingeben können. |

{style="table-layout:auto"}
