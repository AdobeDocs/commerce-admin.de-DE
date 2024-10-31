---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Checkout]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Sales] &gt; [!UICONTROL Checkout] des Commerce-Administrators.
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
| [!UICONTROL Enable Guest Checkout Login] | Store-Ansicht | Aktivieren Sie diese Einstellung, damit nicht authentifizierte Benutzer (Storefront und APIs) fragen können, ob bereits eine E-Mail-Adresse mit einem Kundenkonto verknüpft ist. Dies kann dazu verwendet werden, den Kasse-Workflow für Gäste zu verbessern, indem eine Anmeldeaufforderung angezeigt wird, wenn die eingegebene E-Mail-Adresse bereits bei einem Kundenkonto registriert ist, aber Kosten der Offenlegung von Informationen für nicht authentifizierte Benutzer verursacht wird.  Optionen: `Yes` / `No` |
| [!UICONTROL Enable Onepage Checkout] | Store-Ansicht | Bestimmt, ob [1-Seiten-Checkout](../../stores-purchase/checkout-process.md#checkout-options) das standardmäßige Checkout-Format ist. Optionen: `Yes` / `No` |
| [!UICONTROL Allow Guest Checkout] | Store-Ansicht | Bestimmt, ob Gäste durch [Checkout gehen können, ohne](../../stores-purchase/checkout-guest.md) für ein Konto bei Ihrem Store zu registrieren. Optionen: `Yes` / `No` |
| [!UICONTROL Enable Terms and Conditions] | Store-Ansicht | Bestimmt, ob Kunden vor dem Kauf den [Geschäftsbedingungen](../../stores-purchase/terms-and-conditions.md) des Verkaufs zustimmen müssen. Optionen: `Yes` / `No` |
| [!UICONTROL Display Billing Address On] | Store-Ansicht | Bestimmt den Speicherort der Rechnungsadresse während des Checkouts. Optionen: `Payment Method` / `Payment Page` |
| [!UICONTROL Maximum Number of Items to Display in Order Summary] | Store-Ansicht | Bestimmt die maximale Anzahl von Elementen, die während des Auscheckens in der _Bestellzusammenfassung_ angezeigt werden können. Der Standardwert ist `10`. |
| [!UICONTROL Enable Address Search] | Webseite | ![Adobe Commerce](../../assets/adobe-logo.svg) (nur Adobe Commerce) Bestimmt, ob Kunden die Funktion [Adressensuche](../../stores-purchase/checkout-address-search.md) für die Schritte &quot;Versand&quot;und &quot;Überprüfung und Zahlungen&quot;verwenden können. Wenn dies aktiviert ist, verwenden Sie die Option Anzahl der Kundenadressen-Beschränkungen , um die Anzahl der gespeicherten Adressen festzulegen, die zum Aktivieren dieser Funktion beim Checkout erforderlich sind. Optionen: `Yes` / `No` |
| Begrenzung der Kundenadressen | Webseite | ![Adobe Commerce](../../assets/adobe-logo.svg) (nur Adobe Commerce) Wenn die Adresssuche aktiviert ist, bestimmt die Anzahl der gespeicherten Adressen, die zum Aktivieren dieser Funktion beim Checkout erforderlich sind. Wenn die Anzahl der gespeicherten Adressen des Kunden diese Zahl erreicht oder überschreitet, wird nur die Standardadresse für die Schritte _Versand_ und _Überprüfung und Zahlungen_ gerendert. Der Kunde kann eine Suchfunktion verwenden, um die ausgewählte Adresse zu ändern. Der Standardwert ist `10`. |

{style="table-layout:auto"}

## [!UICONTROL Shopping Cart]

![Warenkorb](./assets/checkout-shopping-cart.png)<!-- zoom -->

<!--[Shopping Cart](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/cart/cart-configuration) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Quote Lifetime (days)] | Webseite | Bestimmt die [Lebensdauer eines angegebenen Preises](../../stores-purchase/cart-configuration.md#quote-lifetime) in Tagen. |
| [!UICONTROL After Adding a Product Redirect to Shopping Cart] | Store-Ansicht | Bestimmt, ob die [Einkaufswagenseite](../../stores-purchase/cart-configuration.md#redirect-to-cart) unmittelbar nach dem Hinzufügen eines Produkts zum Warenkorb angezeigt wird. Optionen: `Yes` / `No` |
| [!UICONTROL Number of Items to Display Pager] | Store-Ansicht | Bestimmt die Anzahl der Artikel im Warenkorb, bevor der Pager ausgelöst wird. Standardwert: `20` |
| [!UICONTROL Show Cross-sell Items in the Shopping Cart] | Store-Ansicht | Gibt an, ob [Querverkaufselemente](../../catalog/related-products-up-sells-cross-sells.md#cross-sells) im Warenkorb angezeigt werden, und bietet Kunden zusätzliche Verkaufsoptionen. Optionen: `Yes` (Standard) / `No` |
| [!UICONTROL Grouped Product Image] | Store-Ansicht | Bestimmt das [Miniaturbild](../../stores-purchase/cart-configuration.md#cart-thumbnails) , das für ein [gruppiertes Produkt](../../catalog/product-create-grouped.md) im Warenkorb angezeigt wird. Optionen: `Product Thumbnail Itself` / `Parent Product Thumbnail` |
| [!UICONTROL Configurable Product Image] | Store-Ansicht | Bestimmt das Bild [thumbnail](../../stores-purchase/cart-configuration.md#cart-thumbnails) , das für ein konfigurierbares Produkt im Warenkorb angezeigt wird. Optionen: `Product Thumbnail Itself` / `Parent Product Thumbnail` |
| [!UICONTROL Preview Quote Lifetime (minutes)] | Store-Ansicht | Bestimmt das maximale Alter des Angebots in Minuten bei der Vorschau über den Warenkorb. |
| [!UICONTROL Enable Clear Shopping Cart] | Webseite | Bestimmt, ob im Warenkorb die Option angezeigt wird, mit der Benutzer den Inhalt des Warenkorbs in einer einzigen Aktion löschen können. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL My Cart Link]

![Link zum Warenkorb](./assets/checkout-my-cart-link.png)<!-- zoom -->

<!-- [*My Cart Link*](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/cart/cart-configuration#mini-cart) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Display Cart Summary] | Webseite | Bestimmt den Wert, der in Klammern nach dem Link &quot;Mein Warenkorb&quot;angezeigt wird. Optionen: `Display number of items in cart` / `Display item quantities` |

{style="table-layout:auto"}

## Mini-Warenkorb

![Mini-Warenkorb](./assets/checkout-mini-cart.png)<!-- zoom -->

<!-- [*Mini Cart*](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/cart/cart-configuration#mini-cart) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Display Mini Cart] | Store-Ansicht | Bestimmt, ob der Mini-Warenkorb auf Store-Seiten angezeigt wird, wenn auf das Warenkorbsymbol in der Kopfzeile geklickt wird. Die Anzeige des Mini-Warenkorbs hängt vom Thema ab. Optionen: `Yes` / `No` |
| [!UICONTROL Number of Items to Display Scrollbar] | Store-Ansicht | Bestimmt die Anzahl der Artikel, die im Mini-Warenkorb angezeigt werden können, bevor die Bildlaufleiste ausgelöst wird. Standard: `5` |
| [!UICONTROL Maximum Number of Items to Display] | Store-Ansicht | Bestimmt die maximale Anzahl von Artikeln, die im Mini-Warenkorb angezeigt werden können. Standard: `10` |

{style="table-layout:auto"}

## [!UICONTROL Payment Failed Emails]

![Zahlungsfehler bei E-Mails](./assets/checkout-payment-failed-emails.png)<!-- zoom -->

<!-- [*Payment Failed Emails*](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/checkout/checkout-payment-failed-emails) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Payment Failed Email Receiver] | Store-Ansicht | Identifiziert den Store-Kontakt, der Zahlungsausfall-E-Mails erhält. Standardempfänger: `General Contact` |
| [!UICONTROL Payment Failed Email Sender] | Store-Ansicht | Identifiziert den Store-Kontakt, der als Absender von E-Mails mit Zahlungsausfall angezeigt wird. Standardsender: `General Contact` |
| [!UICONTROL Payment Failed Template] | Store-Ansicht | Identifiziert die Vorlage, die für E-Mails mit Zahlungsfehlern verwendet wird. Standardvorlage: `Payment Failed` |
| [!UICONTROL Send Payment Failed Copy To] | Store-Ansicht | Gibt die E-Mail-Adresse eines Benutzers an, der eine Kopie der E-Mail mit Zahlungsfehler erhält. Trennen Sie mehrere Adressen durch Kommas. |
| [!UICONTROL Send Payment Failed Copy Method] | Store-Ansicht | Gibt die zum Senden der Kopie verwendete E-Mail-Methode an. Optionen: <br />**`Bcc`**- Sendet eine blinde höfliche Kopie, indem der Empfänger in die Kopfzeile derselben E-Mail eingefügt wird, die an den Kunden gesendet wird. Der BCC-Empfänger ist für den Kunden nicht sichtbar.<br />**`Separate Email`** - Sendet die Kopie als separate E-Mail. |

{style="table-layout:auto"}
