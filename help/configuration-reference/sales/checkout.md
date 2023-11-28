---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Checkout]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der [!UICONTROL Sales] &gt; [!UICONTROL Checkout] Seite des Commerce-Administrators.
exl-id: a912beb0-37a9-407b-83bd-dc6cd0554dc4
feature: Configuration, Checkout
source-git-commit: 1f84bf9ab20aeccacf56eab396b2778140964d17
workflow-type: tm+mt
source-wordcount: '647'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Checkout]

{{config}}

## [!UICONTROL Checkout Options]

>[!NOTE]
>
>[!BADGE 2.4.6-p1]{type=Informative tooltip="Aktualisierungen in 2.4.6-p1"}[!BADGE 2.4.7-beta1]{type=Informative tooltip="Aktualisierungen in 2.4.7-Beta1"}[2.4.7-beta2](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/adobe-commerce/2-4-7.html) und [2.4.6-p3](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html) -Versionen, die Verbesserungen der Sicherheit der beschriebenen Funktionen bieten. Wenn Sie eine oder diese Versionen verwenden, lesen Sie die Versionshinweise.

![Checkout-Optionen](./assets/checkout-checkout-options.png)<!-- zoom -->

<!--[Checkout Options](https://docs.magento.com/user-guide/sales/checkout-options.html) -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable Onepage Checkout] | Store-Ansicht | Bestimmt, ob [einseitige Kasse](../../stores-purchase/checkout-process.md#checkout-options) ist das standardmäßige Checkout-Format. Optionen: `Yes` / `No` |
| [!UICONTROL Allow Guest Checkout] | Store-Ansicht | Bestimmt, ob Gäste durchgehen können [Checkout ohne Registrierung](../../stores-purchase/checkout-guest.md) für ein Konto bei Ihrem Geschäft. Optionen: `Yes` / `No` |
| [!UICONTROL Enable Terms and Conditions] | Store-Ansicht | Bestimmt, ob Kunden dem [Geschäftsbedingungen](../../stores-purchase/terms-and-conditions.md) des Verkaufs vor dem Kauf. Optionen: `Yes` / `No` |
| [!UICONTROL Display Billing Address On] | Store-Ansicht | Bestimmt den Speicherort der Rechnungsadresse während des Checkouts. Optionen: `Payment Method` / `Payment Page` |
| [!UICONTROL Maximum Number of Items to Display in Order Summary] | Store-Ansicht | Bestimmt die maximale Anzahl von Elementen, die im _Bestellübersicht_ während des Checkout. Der Standardwert ist `10`. |
| [!UICONTROL Enable Address Search] | Webseite | ![Adobe Commerce](../../assets/adobe-logo.svg) (Nur Adobe Commerce) Stellt fest, ob Kunden [Adresssuche](../../stores-purchase/checkout-address-search.md) Funktionen für die Schritte Versand und Überprüfung und Zahlungen . Wenn dies aktiviert ist, verwenden Sie die Option Anzahl der Kundenadressen-Beschränkungen , um die Anzahl der gespeicherten Adressen festzulegen, die zum Aktivieren dieser Funktion beim Checkout erforderlich sind. Optionen: `Yes` / `No` |
| Begrenzung der Kundenadressen | Webseite | ![Adobe Commerce](../../assets/adobe-logo.svg) (Nur Adobe Commerce) Wenn die Adresssuche aktiviert ist, bestimmt die Anzahl der gespeicherten Adressen, die zum Aktivieren dieser Funktion beim Checkout erforderlich sind. Wenn die Anzahl der gespeicherten Adressen des Kunden diese Zahl erreicht oder überschreitet, wird nur die Standardadresse auf der Seite _Versand_ und _Überprüfung und Zahlungen_ Schritte. Der Kunde kann eine Suchfunktion verwenden, um die ausgewählte Adresse zu ändern. Der Standardwert ist `10`. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Shopping Cart]

![Warenkorb](./assets/checkout-shopping-cart.png)<!-- zoom -->

<!--[Shopping Cart](https://docs.magento.com/user-guide/sales/cart-configuration.html) -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Quote Lifetime (days)] | Webseite | Bestimmt die [Lebensdauer eines Preises](../../stores-purchase/cart-configuration.md#quote-lifetime)in Tagen. |
| [!UICONTROL After Adding a Product Redirect to Shopping Cart] | Store-Ansicht | Bestimmt, ob die [Warenkorbseite wird angezeigt](../../stores-purchase/cart-configuration.md#redirect-to-cart) unmittelbar nach dem Hinzufügen eines Produkts zum Warenkorb. Optionen: `Yes` / `No` |
| [!UICONTROL Number of Items to Display Pager] | Store-Ansicht | Bestimmt die Anzahl der Artikel im Warenkorb, bevor der Pager ausgelöst wird. Standardwert: `20` |
| [!UICONTROL Show Cross-sell Items in the Shopping Cart] | Store-Ansicht | Gibt an, ob [Crosssell-Artikel](../../catalog/related-products-up-sells-cross-sells.md#cross-sells) werden im Warenkorb angezeigt und bieten Kunden zusätzliche Verkaufsoptionen. Optionen: `Yes` (Standard) / `No` |
| [!UICONTROL Grouped Product Image] | Store-Ansicht | Bestimmt die [thumbnail](../../stores-purchase/cart-configuration.md#cart-thumbnails) Bild, das für eine [gruppiertes Produkt](../../catalog/product-create-grouped.md) im Warenkorb. Optionen: `Product Thumbnail Itself` / `Parent Product Thumbnail` |
| [!UICONTROL Configurable Product Image] | Store-Ansicht | Bestimmt die [thumbnail](../../stores-purchase/cart-configuration.md#cart-thumbnails) Bild, das für ein konfigurierbares Produkt im Warenkorb angezeigt wird. Optionen: `Product Thumbnail Itself` / `Parent Product Thumbnail` |
| [!UICONTROL Preview Quote Lifetime (minutes)] | Store-Ansicht | Bestimmt das maximale Alter des Angebots in Minuten bei der Vorschau über den Warenkorb. |
| [!UICONTROL Enable Clear Shopping Cart] | Webseite | Bestimmt, ob im Warenkorb die Option angezeigt wird, mit der Benutzer den Inhalt des Warenkorbs in einer einzigen Aktion löschen können. Optionen: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL My Cart Link]

![Link zum Warenkorb](./assets/checkout-my-cart-link.png)<!-- zoom -->

<!-- [*My Cart Link*](https://docs.magento.com/user-guide/sales/mini-cart.html) -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Display Cart Summary] | Webseite | Bestimmt den Wert, der in Klammern nach dem Link &quot;Mein Warenkorb&quot;angezeigt wird. Optionen: `Display number of items in cart` / `Display item quantities` |

{:style=&quot;table-layout:auto&quot;}

## Mini-Warenkorb

![Mini-Warenkorb](./assets/checkout-mini-cart.png)<!-- zoom -->

<!-- [*Mini Cart*](https://docs.magento.com/user-guide/sales/mini-cart.html) -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Display Mini Cart] | Store-Ansicht | Bestimmt, ob der Mini-Warenkorb auf Store-Seiten angezeigt wird, wenn auf das Warenkorbsymbol in der Kopfzeile geklickt wird. Die Anzeige des Mini-Warenkorbs hängt vom Thema ab. Optionen: `Yes` / `No` |
| [!UICONTROL Number of Items to Display Scrollbar] | Store-Ansicht | Bestimmt die Anzahl der Artikel, die im Mini-Warenkorb angezeigt werden können, bevor die Bildlaufleiste ausgelöst wird. Standard: `5` |
| [!UICONTROL Maximum Number of Items to Display] | Store-Ansicht | Bestimmt die maximale Anzahl von Artikeln, die im Mini-Warenkorb angezeigt werden können. Standard: `10` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Payment Failed Emails]

![Zahlung fehlgeschlagener E-Mails](./assets/checkout-payment-failed-emails.png)<!-- zoom -->

<!-- [*Payment Failed Emails*](https://docs.magento.com/user-guide/sales/checkout-payment-failed-emails.html) -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Payment Failed Email Receiver] | Store-Ansicht | Identifiziert den Store-Kontakt, der Zahlungsausfall-E-Mails erhält. Standardempfänger: `General Contact` |
| [!UICONTROL Payment Failed Email Sender] | Store-Ansicht | Identifiziert den Store-Kontakt, der als Absender von E-Mails mit Zahlungsausfall angezeigt wird. Standardabsender: `General Contact` |
| [!UICONTROL Payment Failed Template] | Store-Ansicht | Identifiziert die Vorlage, die für E-Mails mit Zahlungsfehlern verwendet wird. Standardvorlage: `Payment Failed` |
| [!UICONTROL Send Payment Failed Copy To] | Store-Ansicht | Gibt die E-Mail-Adresse eines Benutzers an, der eine Kopie der E-Mail mit Zahlungsfehler erhält. Trennen Sie mehrere Adressen durch Kommas. |
| [!UICONTROL Send Payment Failed Copy Method] | Store-Ansicht | Gibt die zum Senden der Kopie verwendete E-Mail-Methode an. Optionen: <br />**`Bcc`**- Sendet eine blinde höfliche Kopie, indem der Empfänger in die Kopfzeile derselben E-Mail eingefügt wird, die an den Kunden gesendet wird. Der BCC-Empfänger ist für den Kunden nicht sichtbar.<br />**`Separate Email`** - Sendet die Kopie als separate E-Mail. |

{:style=&quot;table-layout:auto&quot;}
