---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Checkout]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der [!UICONTROL Sales] &gt; [!UICONTROL Checkout] Seite des Commerce-Administrators.
exl-id: a912beb0-37a9-407b-83bd-dc6cd0554dc4
feature: Configuration, Checkout
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Checkout]

{{config}}

## [!UICONTROL Checkout Options]

![Checkout-Optionen](./assets/checkout-checkout-options.png)<!-- zoom -->

<!--[Checkout Options](https://docs.magento.com/user-guide/sales/checkout-options.html) -->

| Feld | [Scope](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|------------------------------------------------------------------|--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Guest Checkout Login] | Shop-Ansicht | Aktivieren Sie diese Einstellung, damit nicht authentifizierte Benutzer (Storefront und APIs) abfragen können, ob bereits eine E-Mail-Adresse mit einem Kundenkonto verknüpft ist. Dies kann verwendet werden, um den Checkout-Workflow für Gäste zu verbessern, indem eine Anmeldeaufforderung angezeigt wird, wenn die eingegebene E-Mail-Adresse bereits bei einem Kundenkonto registriert ist, aber zum Preis der Offenlegung von Informationen für nicht authentifizierte Benutzer geschieht.  Optionen: `Yes` / `No` |
| [!UICONTROL Enable Onepage Checkout] | Shop-Ansicht | Bestimmt, ob [Einseitiger Checkout](../../stores-purchase/checkout-process.md#checkout-options) ist das standardmäßige Checkout-Format. Optionen: `Yes` / `No` |
| [!UICONTROL Allow Guest Checkout] | Shop-Ansicht | Legt fest, ob Gäste Folgendes durchlaufen können [Checkout ohne Registrierung](../../stores-purchase/checkout-guest.md) für ein Konto in Ihrem Geschäft. Optionen: `Yes` / `No` |
| [!UICONTROL Enable Terms and Conditions] | Shop-Ansicht | Legt fest, ob Kunden dem zustimmen müssen [Allgemeine Geschäftsbedingungen](../../stores-purchase/terms-and-conditions.md) vor dem Kauf zu verkaufen. Optionen: `Yes` / `No` |
| [!UICONTROL Display Billing Address On] | Shop-Ansicht | Bestimmt den Speicherort der Rechnungsadresse während des Checkouts. Optionen: `Payment Method` / `Payment Page` |
| [!UICONTROL Maximum Number of Items to Display in Order Summary] | Shop-Ansicht | Legt die maximale Anzahl von Elementen fest, die in der _Bestellzusammenfassung_ Während des Checkouts. Der Standardwert lautet `10`. |
| [!UICONTROL Enable Address Search] | Website | ![Adobe Commerce](../../assets/adobe-logo.svg) (Nur Adobe Commerce) Legt fest, ob Kunden Folgendes verwenden können [Adresssuche](../../stores-purchase/checkout-address-search.md) Funktionen für die Schritte „Versand“ und „Überprüfung und Zahlungen„. Wenn diese Option aktiviert ist, verwenden Sie das Limit für Kundenadressen , um die Anzahl der gespeicherten Adressen festzulegen, die erforderlich sind, um diese Funktion während des Checkouts zu aktivieren. Optionen: `Yes` / `No` |
| Limit für Kundenadressen | Website | ![Adobe Commerce](../../assets/adobe-logo.svg) (Nur Adobe Commerce) Wenn die Adresssuche aktiviert ist, bestimmt die Anzahl der gespeicherten Adressen, die erforderlich sind, um diese Funktion während des Checkouts zu aktivieren. Wenn die Anzahl der gespeicherten Adressen des Kunden diese Anzahl erreicht oder überschreitet, wird nur die Standardadresse auf der Seite gerendert. _Versand_ und _Überprüfung und Zahlungen_ Schritte. Der Kunde kann eine Suchfunktion nutzen, um die ausgewählte Adresse zu ändern. Der Standardwert lautet `10`. |

{style="table-layout:auto"}

## [!UICONTROL Shopping Cart]

![Warenkorb](./assets/checkout-shopping-cart.png)<!-- zoom -->

<!--[Shopping Cart](https://docs.magento.com/user-guide/sales/cart-configuration.html) -->

| Feld | [Scope](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Quote Lifetime (days)] | Website | Bestimmt die [Lebensdauer eines notierten Preises](../../stores-purchase/cart-configuration.md#quote-lifetime), in Tagen. |
| [!UICONTROL After Adding a Product Redirect to Shopping Cart] | Shop-Ansicht | Legt fest, ob [Die Seite Warenkorb wird angezeigt](../../stores-purchase/cart-configuration.md#redirect-to-cart) Unmittelbar nachdem ein Produkt zum Warenkorb hinzugefügt wurde. Optionen: `Yes` / `No` |
| [!UICONTROL Number of Items to Display Pager] | Shop-Ansicht | Bestimmt die Anzahl der Artikel im Warenkorb, bevor der Pager ausgelöst wird. Standardwert: `20` |
| [!UICONTROL Show Cross-sell Items in the Shopping Cart] | Shop-Ansicht | Zeigt an, wenn [Crosssell-Artikel](../../catalog/related-products-up-sells-cross-sells.md#cross-sells) werden im Warenkorb angezeigt und bieten Kunden zusätzliche Verkaufsoptionen. Optionen: `Yes` (Standard) / `No` |
| [!UICONTROL Grouped Product Image] | Shop-Ansicht | Bestimmt die [Miniaturansicht](../../stores-purchase/cart-configuration.md#cart-thumbnails) Bild, das für ein [Produktgruppe](../../catalog/product-create-grouped.md) im Warenkorb. Optionen: `Product Thumbnail Itself` / `Parent Product Thumbnail` |
| [!UICONTROL Configurable Product Image] | Shop-Ansicht | Bestimmt die [Miniaturansicht](../../stores-purchase/cart-configuration.md#cart-thumbnails) Bild, das für ein konfigurierbares Produkt im Warenkorb angezeigt wird. Optionen: `Product Thumbnail Itself` / `Parent Product Thumbnail` |
| [!UICONTROL Preview Quote Lifetime (minutes)] | Shop-Ansicht | Bestimmt das maximale Alter des Angebots in Minuten, wenn eine Vorschau des Warenkorbs angezeigt wird. |
| [!UICONTROL Enable Clear Shopping Cart] | Website | Legt fest, ob im Warenkorb die Option angezeigt wird, mit der Benutzer den Inhalt des Warenkorbs in einer einzigen Aktion löschen können. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL My Cart Link]

![Mein Warenkorb-Link](./assets/checkout-my-cart-link.png)<!-- zoom -->

<!-- [*My Cart Link*](https://docs.magento.com/user-guide/sales/mini-cart.html) -->

| Feld | [Scope](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Display Cart Summary] | Website | Bestimmt den Wert, der in Klammern hinter dem Link Mein Warenkorb angezeigt wird. Optionen: `Display number of items in cart` / `Display item quantities` |

{style="table-layout:auto"}

## Mini-Cart

![Mini-Cart](./assets/checkout-mini-cart.png)<!-- zoom -->

<!-- [*Mini Cart*](https://docs.magento.com/user-guide/sales/mini-cart.html) -->

| Feld | [Scope](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Display Mini Cart] | Shop-Ansicht | Bestimmt, ob der Mini-Warenkorb auf Store-Seiten angezeigt wird, wenn auf das Warenkorb-Symbol in der Kopfzeile geklickt wird. Die Anzeige des Mini-Warenkorbs hängt vom Thema ab. Optionen: `Yes` / `No` |
| [!UICONTROL Number of Items to Display Scrollbar] | Shop-Ansicht | Bestimmt die Anzahl der Elemente, die im Minicart angezeigt werden können, bevor die Bildlaufleiste ausgelöst wird. Standard: `5` |
| [!UICONTROL Maximum Number of Items to Display] | Shop-Ansicht | Bestimmt die maximale Anzahl von Artikeln, die im Mini-Warenkorb angezeigt werden können. Standard: `10` |

{style="table-layout:auto"}

## [!UICONTROL Payment Failed Emails]

![E-Mails zu fehlgeschlagenen Zahlungen](./assets/checkout-payment-failed-emails.png)<!-- zoom -->

<!-- [*Payment Failed Emails*](https://docs.magento.com/user-guide/sales/checkout-payment-failed-emails.html) -->

| Feld | [Scope](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Payment Failed Email Receiver] | Shop-Ansicht | Identifiziert den Store-Kontakt, der E-Mails zu fehlgeschlagenen Zahlungen erhält. Standard-Empfänger: `General Contact` |
| [!UICONTROL Payment Failed Email Sender] | Shop-Ansicht | Identifiziert den Store-Kontakt, der als Absender der E-Mails mit fehlgeschlagener Zahlung angezeigt wird. Standardabsender: `General Contact` |
| [!UICONTROL Payment Failed Template] | Shop-Ansicht | Identifiziert die Vorlage, die für E-Mails zu fehlgeschlagenen Zahlungen verwendet wird. Standardvorlage: `Payment Failed` |
| [!UICONTROL Send Payment Failed Copy To] | Shop-Ansicht | Gibt die E-Mail-Adresse eines jeden an, der eine Kopie einer E-Mail mit einer fehlgeschlagenen Zahlung erhalten soll. Trennen Sie mehrere Adressen durch ein Komma. |
| [!UICONTROL Send Payment Failed Copy Method] | Shop-Ansicht | Gibt die E-Mail-Methode an, die zum Senden der Kopie verwendet wird. Optionen: <br />**`Bcc`**- Sendet eine Blind-Höflichkeitskopie, indem der Empfänger in die Kopfzeile derselben E-Mail eingefügt wird, die an den Kunden gesendet wird. Der BCC-Empfänger ist für den Kunden nicht sichtbar.<br />**`Separate Email`** - Sendet die Kopie als separate E-Mail. |

{style="table-layout:auto"}
