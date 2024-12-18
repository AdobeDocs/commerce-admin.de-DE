---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Checkout]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Sales] &gt; [!UICONTROL Checkout] des Commerce Admin-Bereichs.
exl-id: a912beb0-37a9-407b-83bd-dc6cd0554dc4
feature: Configuration, Checkout
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Checkout]

{{config}}

## [!UICONTROL Checkout Options]

![Checkout-Optionen](./assets/checkout-checkout-options.png)<!-- zoom -->

<!--[Checkout Options](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/checkout/checkout-process#checkout-options) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|------------------------------------------------------------------|--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Guest Checkout Login] | Shop-Ansicht | Aktivieren Sie diese Einstellung, damit nicht authentifizierte Benutzer (Storefront und APIs) abfragen können, ob bereits eine E-Mail-Adresse mit einem Kundenkonto verknüpft ist. Dies kann verwendet werden, um den Checkout-Workflow für Gäste zu verbessern, indem eine Anmeldeaufforderung angezeigt wird, wenn die eingegebene E-Mail-Adresse bereits bei einem Kundenkonto registriert ist, aber zum Preis der Offenlegung von Informationen für nicht authentifizierte Benutzer.  Optionen: `Yes` / `No` |
| [!UICONTROL Enable Onepage Checkout] | Shop-Ansicht | Bestimmt, ob [Einseitiger Auscheck](../../stores-purchase/checkout-process.md#checkout-options) das standardmäßige Auscheckformat ist. Optionen: `Yes` / `No` |
| [!UICONTROL Allow Guest Checkout] | Shop-Ansicht | Legt fest, ob Gäste für ein Konto [ Ihrem Geschäft ](../../stores-purchase/checkout-guest.md) (Checkout ohne Registrierung) durchlaufen können. Optionen: `Yes` / `No` |
| [!UICONTROL Enable Terms and Conditions] | Shop-Ansicht | Legt fest, ob Kunden vor dem Kauf den [Geschäftsbedingungen](../../stores-purchase/terms-and-conditions.md) des Verkaufs zustimmen müssen. Optionen: `Yes` / `No` |
| [!UICONTROL Display Billing Address On] | Shop-Ansicht | Bestimmt den Speicherort der Rechnungsadresse während des Checkouts. Optionen: `Payment Method` / `Payment Page` |
| [!UICONTROL Maximum Number of Items to Display in Order Summary] | Shop-Ansicht | Bestimmt die maximale Anzahl von Elementen, die während des Checkouts in der _Bestellzusammenfassung_ angezeigt werden können. Der Standardwert lautet `10`. |
| [!UICONTROL Enable Address Search] | Website | ![Adobe Commerce](../../assets/adobe-logo.svg) (nur Adobe Commerce) Legt fest, ob Kunden die [Adresssuche](../../stores-purchase/checkout-address-search.md) für die Schritte „Versand“ und „Überprüfung und Zahlung“ verwenden können. Wenn diese Option aktiviert ist, können Sie über das Limit für Kundenadressen die Anzahl der gespeicherten Adressen festlegen, die erforderlich sind, um diese Funktion während des Checkouts zu aktivieren. Optionen: `Yes` / `No` |
| Limit für Kundenadressen | Website | ![Adobe Commerce](../../assets/adobe-logo.svg) (nur Adobe Commerce) Wenn die Adresssuche aktiviert ist, bestimmt die Anzahl der gespeicherten Adressen, die erforderlich sind, um diese Funktion während des Checkouts zu aktivieren. Wenn die Anzahl der gespeicherten Adressen des Kunden diese Zahl erreicht oder überschreitet, wird nur die Standardadresse in den Schritten _Versand_ und _Überprüfen und_) gerendert. Der Kunde kann eine Suchfunktion nutzen, um die ausgewählte Adresse zu ändern. Der Standardwert lautet `10`. |

{style="table-layout:auto"}

## [!UICONTROL Shopping Cart]

![Einkaufswagen](./assets/checkout-shopping-cart.png)<!-- zoom -->

<!--[Shopping Cart](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/cart/cart-configuration) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Quote Lifetime (days)] | Website | Bestimmt die [Lebensdauer eines angegebenen ](../../stores-purchase/cart-configuration.md#quote-lifetime) in Tagen. |
| [!UICONTROL After Adding a Product Redirect to Shopping Cart] | Shop-Ansicht | Bestimmt, ob die [Warenkorbseite](../../stores-purchase/cart-configuration.md#redirect-to-cart) unmittelbar nach dem Hinzufügen eines Produkts zum Warenkorb angezeigt wird. Optionen: `Yes` / `No` |
| [!UICONTROL Number of Items to Display Pager] | Shop-Ansicht | Bestimmt die Anzahl der Artikel im Warenkorb, bevor der Pager ausgelöst wird. Standardwert: `20` |
| [!UICONTROL Show Cross-sell Items in the Shopping Cart] | Shop-Ansicht | Gibt an, ob [Crosssell-Artikel](../../catalog/related-products-up-sells-cross-sells.md#cross-sells) im Warenkorb angezeigt werden, sodass Kunden zusätzliche Verkaufsoptionen erhalten. Optionen: `Yes` (Standard) / `No` |
| [!UICONTROL Grouped Product Image] | Shop-Ansicht | Bestimmt das [Miniaturbild](../../stores-purchase/cart-configuration.md#cart-thumbnails), das für ein [gruppiertes Produkt](../../catalog/product-create-grouped.md) im Warenkorb angezeigt wird. Optionen: `Product Thumbnail Itself` / `Parent Product Thumbnail` |
| [!UICONTROL Configurable Product Image] | Shop-Ansicht | Bestimmt das [Miniaturbild](../../stores-purchase/cart-configuration.md#cart-thumbnails), das für ein konfigurierbares Produkt im Warenkorb angezeigt wird. Optionen: `Product Thumbnail Itself` / `Parent Product Thumbnail` |
| [!UICONTROL Preview Quote Lifetime (minutes)] | Shop-Ansicht | Bestimmt das maximale Alter des Angebots in Minuten, wenn eine Vorschau des Warenkorbs angezeigt wird. |
| [!UICONTROL Enable Clear Shopping Cart] | Website | Bestimmt, ob im Warenkorb die Option angezeigt wird, mit der Benutzer den Inhalt des Warenkorbs in einer einzigen Aktion löschen können. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL My Cart Link]

![Mein Warenkorb-Link](./assets/checkout-my-cart-link.png)<!-- zoom -->

<!-- [*My Cart Link*](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/cart/cart-configuration#mini-cart) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Display Cart Summary] | Website | Bestimmt den Wert, der in Klammern hinter dem Link Mein Warenkorb angezeigt wird. Optionen: `Display number of items in cart` / `Display item quantities` |

{style="table-layout:auto"}

## Mini-Cart

![Mini-Warenkorb](./assets/checkout-mini-cart.png)<!-- zoom -->

<!-- [*Mini Cart*](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/cart/cart-configuration#mini-cart) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Display Mini Cart] | Shop-Ansicht | Bestimmt, ob der Mini-Warenkorb auf Store-Seiten angezeigt wird, wenn auf das Warenkorb-Symbol in der Kopfzeile geklickt wird. Die Anzeige des Mini-Warenkorbs hängt vom Thema ab. Optionen: `Yes` / `No` |
| [!UICONTROL Number of Items to Display Scrollbar] | Shop-Ansicht | Bestimmt die Anzahl der Elemente, die im Mini-Warenkorb angezeigt werden können, bevor die Bildlaufleiste ausgelöst wird. Standard: `5` |
| [!UICONTROL Maximum Number of Items to Display] | Shop-Ansicht | Bestimmt die maximale Anzahl von Artikeln, die im Mini-Warenkorb angezeigt werden können. Standard: `10` |

{style="table-layout:auto"}

## [!UICONTROL Payment Failed Emails]

![Fehlgeschlagene E-Mails](./assets/checkout-payment-failed-emails.png)<!-- zoom -->

<!-- [*Payment Failed Emails*](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/checkout/checkout-payment-failed-emails) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Payment Failed Email Receiver] | Shop-Ansicht | Identifiziert den Store-Kontakt, der E-Mails zu fehlgeschlagenen Zahlungen erhält. Standard-Empfänger: `General Contact` |
| [!UICONTROL Payment Failed Email Sender] | Shop-Ansicht | Identifiziert den Store-Kontakt, der als Absender von E-Mails mit fehlgeschlagener Zahlung angezeigt wird. Standardabsender: `General Contact` |
| [!UICONTROL Payment Failed Template] | Shop-Ansicht | Identifiziert die Vorlage, die für E-Mails zu fehlgeschlagenen Zahlungen verwendet wird. Standardvorlage: `Payment Failed` |
| [!UICONTROL Send Payment Failed Copy To] | Shop-Ansicht | Gibt die E-Mail-Adresse eines jeden an, der eine Kopie einer E-Mail mit einer fehlgeschlagenen Zahlung erhalten soll. Trennen Sie mehrere Adressen durch ein Komma. |
| [!UICONTROL Send Payment Failed Copy Method] | Shop-Ansicht | Gibt die E-Mail-Methode an, die zum Senden der Kopie verwendet wird. Optionen: <br />**`Bcc`**- Sendet eine Blindkopie, indem der Empfänger in die Kopfzeile derselben E-Mail eingefügt wird, die an den Kunden gesendet wird. Der BCC-Empfänger ist für den Kunden nicht sichtbar.<br />**`Separate Email`** - Sendet die Kopie als separate E-Mail. |

{style="table-layout:auto"}
