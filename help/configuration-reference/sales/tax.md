---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Tax]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Sales] &gt; [!UICONTROL Tax] des Commerce-Administrators.
exl-id: eb929a6c-adb2-45ac-b6ec-6239938355bf
feature: Configuration, Taxes
source-git-commit: f95e6d22f83b518c64b254f0d98147e3c6ebaf42
workflow-type: tm+mt
source-wordcount: '1305'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Tax]

>[!NOTE]
>
>Die Versionen 2.4.0 bis 2.4.3 von Adobe Commerce und Magento Open Source enthielten die vom Vertex-Anbieter entwickelte Erweiterung, die zur Integration in den [!UICONTROL Vertex Cloud] verwendet wurde. Ab Version 2.4.4 ist diese Erweiterung nicht mehr im Paket mit der Kernversion enthalten und muss über die Commerce Marketplace installiert und aktualisiert werden. Der Marketplace bietet außerdem Zugriff auf die aktuelle Dokumentation, die vom Erweiterungsentwickler bereitgestellt wird.
><br><br>
>Wenn Sie die gebündelte Erweiterung aktiviert und konfiguriert haben, müssen Sie Ihre Composer.json-Datei im Rahmen des Aktualisierungsprozesses von 2.4.4 aktualisieren und zukünftige Erweiterungs-Updates verwalten. Weitere Informationen finden Sie unter [Upgrade-Module und -Erweiterungen](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) im _Upgrade-Handbuch_.

{{config}}

## [!UICONTROL Tax Classes]

![Steuerklassen](./assets/tax-tax-classes.png)<!-- zoom -->

Weitere Informationen zum Ändern dieser Einstellungen finden Sie unter [Steuerklassen](../../stores-purchase/tax-class.md) im _Erlebnis-Handbuch für Geschäfte und Kauf_.

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Tax Class for Shipping] | Webseite | Gibt die für den Versand verwendete Steuerklasse an. Zu den Optionen gehören alle verfügbaren Produktsteuerklassen: `None` / `Taxable Goods` / `Shipping` / `Tax Exempt` |
| [!UICONTROL Tax Class for Gift Options] | Webseite | ![Adobe Commerce](../../assets/adobe-logo.svg) (nur Adobe Commerce) Gibt die Standardsteuerklasse an, die für Geschenkoptionen verwendet wird. |
| [!UICONTROL Default Tax Class for Product] | Global | Gibt die für Produkte verwendete Standardsteuerklasse an. |
| [!UICONTROL Default Tax Class for Customer] | Global | Gibt die Standardsteuerklasse an, die für Kunden verwendet wird. |

{style="table-layout:auto"}

## [!UICONTROL Calculation Settings]

![Berechnungseinstellungen](./assets/tax-calculation-settings.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Tax Calculation Method Based On] | Webseite | Bestimmt die Methode zur Berechnung der Steuer für eine Bestellung. Optionen:<br/>**`Unit Price`**- Steuerberechnungen basieren auf dem Stückpreis jedes Produkts.<br/>**`Row Total`** - Steuerberechnungen basieren auf der Zeileneintrag &quot;Summe&quot;. <br/>**`Total`**- Steuerberechnungen basieren auf der Bestellsumme.<br/><br/>_** Hinweis: **_Wenn vom Marketplace eine Erweiterung für die Steuerberechnung installiert wird, z. B. _Vertex Cloud_, wird der Erweiterungsdienst als Option aufgelistet. |
| [!UICONTROL Tax Calculation Based On] | Webseite | Bestimmt, ob die Steuerberechnung auf der Lieferadresse, der Rechnungsadresse oder dem Versandursprung basiert. Optionen: `Shipping Address` / `Billing Address` / `Shipping Origin` |
| [!UICONTROL Catalog Prices] | Webseite | Bestimmt, ob die Katalogpreise Steuern enthalten oder ausschließen. Optionen: `Excluding Tax` / `Including Tax` |
| [!UICONTROL Shipping Prices] | Webseite | Die Bestimmung der Versandpreise schließt die Steuer ein oder schließt sie aus. Optionen: `Excluding Tax` / `Including Tax` |
| [!UICONTROL Apply Customer Tax] | Webseite | Bestimmt, ob die Steuer vor oder nach einem Rabatt angewendet wird. Optionen: `Before Discount` / `After Discount` |
| [!UICONTROL Apply Discount on Prices] | Webseite | Bestimmt, ob Abzinsungspreise Steuern enthalten oder ausschließen. Optionen: `Excluding Tax` / `Including Tax` |
| [!UICONTROL Apply Tax On] | Webseite | Bestimmt, ob die Steuer auf den ursprünglichen Preis oder gegebenenfalls auf einen benutzerdefinierten Preis angewendet wird. Optionen: `Custom price if available` / `Original price only` |
| [!UICONTROL Enable Cross Border Trade] | Webseite | Wenn diese Option aktiviert ist, wird eine konsistente Preisgestaltung grenzüberschreitend in Regionen mit unterschiedlichen Steuersätzen angewendet. Optionen: `Yes` / `No` <br/><br/>**_Hinweis:_**Durch die Verwendung des grenzüberschreitenden Handels wird die Gewinnspanne nach Steuersatz angepasst. |

{style="table-layout:auto"}

## [!UICONTROL Default Tax Destination Calculation]

![Berechnung des steuerlichen Ziels ](./assets/tax-default-tax-destination-calculation.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Default Country] | Store-Ansicht | Bestimmt das Land, auf dem die Steuerberechnungen basieren. |
| [!UICONTROL Default State] | Store-Ansicht | Bestimmt den Status, auf dem Steuerberechnungen basieren. Ein Sternchen (*) kann als Platzhalter dienen, der alle Staaten im ausgewählten Land angibt. |
| [!UICONTROL Default Post Code] | Store-Ansicht | Gibt die Postleitzahl oder Postleitzahl an, auf der die Steuerberechnungen basieren. Ein Sternchen (*) kann als Platzhalter dienen, der alle Postleitzahlen im ausgewählten Status angibt. |

{style="table-layout:auto"}

## [!UICONTROL Price Display Settings]

![Preisanzeigeeinstellungen](./assets/tax-price-display-settings.png)<!-- zoom -->

Weitere Informationen zum Ändern dieser Einstellungen finden Sie unter [Einstellungen für die Preisanzeige konfigurieren](../../stores-purchase/display-settings.md#configure-price-display-settings) im Handbuch _Stores and Purchase Experience Guide_.

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Display Product Prices in Catalog] | Store-Ansicht | Bestimmt, ob die im Katalog veröffentlichten Produktpreise Steuern enthalten oder ausschließen oder zwei Versionen des Preises anzeigen, eine mit und die andere ohne Steuern. Optionen: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` <br/><br/>**_Hinweis:_**Wenn Sie das Feld &quot;Produktpreise anzeigen&quot;auf `Including Tax` setzen, wird die Steuer nur angezeigt, wenn eine Steuerregel vorhanden ist, die mit der Steuerursache übereinstimmt, oder es eine Kundenadresse gibt, die der Steuerregel entspricht. Zu den Ereignissen, die eine Übereinstimmung Trigger haben können, gehören die Erstellung von Kundenkonten, die Anmeldung oder die Verwendung des Steuerungs- und Versandschätzungs-Tools im Warenkorb. |
| [!UICONTROL Display Shipping Prices] | Store-Ansicht | Bestimmt, ob die Versandpreise Steuern enthalten oder ausschließen oder zwei Versionen des Versandpreises anzeigen, eine mit und die andere ohne Steuern. Optionen: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |

{style="table-layout:auto"}

## [!UICONTROL Shopping Cart Display Settings]

![Anzeigeeinstellungen für Warenkorb](./assets/tax-shopping-cart-display-settings.png)<!-- zoom -->

Weitere Informationen zum Ändern dieser Einstellungen finden Sie unter [Einstellungen für die Anzeige des Warenkorbs konfigurieren](../../stores-purchase/display-settings.md#step-2-configure-shopping-cart-display-settings) im Handbuch _Stores and Purchase Experience Guide_.

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Display Prices] | Store-Ansicht | Bestimmt, ob die Warenkorbpreise Steuern enthalten oder ausschließen oder zwei Versionen des Preises anzeigen, eine mit und die andere ohne Steuern. Optionen: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Display Subtotal|Store View] | Bestimmt, ob in der Zwischensumme des Warenkorbs Steuern enthalten sind oder ausgeschlossen sind, oder zeigt zwei Versionen der Zwischensumme an: eine mit und die andere ohne Steuern. Optionen: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Display Shipping Amount] | Store-Ansicht | Stellt fest, ob der Versandbetrag des Warenkorbs Steuern enthält oder ausschließt, oder zeigt zwei Versionen des Versandbetrags an: eine mit und die andere ohne Steuern. Optionen: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Additionally Show Order Total Without Tax] | Store-Ansicht | Bestimmt, ob eine zusätzliche Zeile mit dem Gesamtwert ohne Steuern im Warenkorb angezeigt wird. Optionen: `Yes` / `No` |
| [!UICONTROL Display Full Tax Summary] | Store-Ansicht | Stellt fest, ob der Warenkorb eine vollständige Steuerübersicht enthält. Optionen: `Yes` / `No` |
| [!UICONTROL Display Zero Tax Subtotal] | Store-Ansicht | Stellt fest, ob der Warenkorb eine Untersumme Steuern enthält, wenn die Steuer gleich null ist. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Orders, Invoices, Credit Memos Display Settings]

![Anzeigeeinstellungen für Bestellungen, Rechnungen, Credit Memos](./assets/tax-orders-invoices-credit-memos-display-settings.png)<!-- zoom -->

Weitere Informationen zum Ändern dieser Einstellungen finden Sie unter [Einstellungen für die Anzeige von Bestell-, Handels- und Kreditkarten konfigurieren](../../stores-purchase/display-settings.md#step-3-configure-order-invoice-and-credit-memo-display-settings) im _Erlebnis-Handbuch für Geschäfte und Kauf_.

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Display Prices] | Store-Ansicht | Bestimmt, ob die Preise für Verkaufsdokumente Steuern enthalten oder ausschließen oder ob in jedem Dokument zwei Versionen des Preises angezeigt werden: eine mit und die andere ohne Steuern. Optionen: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Display Subtotal] | Store-Ansicht | Bestimmt, ob die Zwischensumme bei Verkaufsdokumenten Steuern enthält oder ausschließt oder ob in jedem Dokument zwei Versionen der Zwischensumme angezeigt werden: eine mit und die andere ohne Steuern. Optionen: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Display Shipping Amount] | Store-Ansicht | Bestimmt, ob der Versandbetrag für Verkaufsdokumente Steuern enthält oder ausschließt oder ob in jedem Dokument zwei Versionen der Zwischensumme angezeigt werden, eine mit und die andere ohne Steuern. Optionen: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Additionally Show Order Total Without Tax] | Store-Ansicht | Bestimmt, ob eine zusätzliche Zeile mit dem Gesamtbetrag ohne Steuern in Verkaufsdokumenten angezeigt wird. Optionen: `Yes` / `No` |
| [!UICONTROL Display Full Tax Summary] | Store-Ansicht | Bestimmt, ob die vollständige Steuerübersicht in Verkaufsdokumenten angezeigt wird. Optionen: `Yes` / `No` |
| [!UICONTROL Display Zero Tax Subtotal] | Store-Ansicht | Bestimmt, welcher Teil der Zwischensumme bei Verkaufsunterlagen angezeigt wird, wenn keine Steuer erhoben wird. Optionen: `Yes` / `No` |
| [!UICONTROL Display Gift Wrapping Prices] | Store-Ansicht | ![Adobe Commerce](../../assets/adobe-logo.svg) (nur Adobe Commerce) Bestimmt, ob die Geschenkverpackungspreise in der Zwischensumme enthalten sind. Optionen: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Display Printed Card Prices] | Store-Ansicht | ![Adobe Commerce](../../assets/adobe-logo.svg) (nur Adobe Commerce) Bestimmt, ob die Preise für gedruckte Karten in der Zwischensumme enthalten sind. Optionen: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |

{style="table-layout:auto"}

## [!UICONTROL Fixed Product Taxes]

![Feste Produktsteuer](./assets/tax-fixed-product-taxes.png)<!-- zoom -->

Weitere Informationen zum Ändern dieser Einstellungen finden Sie unter [Feste Produktsteuer (FPT)](../../stores-purchase/fixed-product-tax.md) im _Handbuch zu Geschäften und Kauferlebnissen_.

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable FPT] | Webseite | Bestimmt, ob FPT verfügbar ist. Optionen: `Yes` / `No` |
| [!UICONTROL Display Prices in Product Lists] | Webseite | Steuert die Anzeige von FPT in Produktlisten. Optionen:<br/> **`Including FPT Only`** - Die angezeigten Preise beinhalten feste Produktsteuern. Der FPT-Betrag wird nicht separat angezeigt.<br/>**`Including FPT and FPT description`**- Die angezeigten Preise beinhalten feste Produktsteuern. Der FPT-Betrag wird separat angezeigt.<br/>**`Excluding FPT. Including FPT description and final price`** - Die angezeigten Preise enthalten keine festen Produktsteuern. Der FPT-Betrag wird separat angezeigt.<br/>**`Excluding FPT`**- Die angezeigten Preise enthalten keine festen Produktsteuern. Der FPT-Betrag wird nicht separat angezeigt. |
| [!UICONTROL Display Prices On Product View Page] | Webseite | Steuert die Anzeige von FPT auf der Produktseite. Optionen:<br/> **`Including FPT Only`** - Die angezeigten Preise beinhalten feste Produktsteuern. Der FPT-Betrag wird nicht separat angezeigt.<br/>**`Including FPT and FPT description`**- Die angezeigten Preise beinhalten feste Produktsteuern. Der FPT-Betrag wird separat angezeigt.<br/>**`Excluding FPT. Including FPT description and final price`** - Die angezeigten Preise enthalten keine festen Produktsteuern. Der FPT-Betrag wird separat angezeigt.<br/>**`Excluding FPT`**- Die angezeigten Preise enthalten keine festen Produktsteuern. Der FPT-Betrag wird nicht separat angezeigt. |
| [!UICONTROL Display Prices in Sales Modules] | Webseite | Steuert die Anzeige von FPT im Warenkorb und während des Kassengangs. Optionen:<br/> **`Including FPT Only`** - Die angezeigten Preise beinhalten feste Produktsteuern. Der FPT-Betrag wird nicht separat angezeigt.<br/>**`Including FPT and FPT description`**- Die angezeigten Preise beinhalten feste Produktsteuern. Der FPT-Betrag wird separat angezeigt.<br/>**`Excluding FPT. Including FPT description and final price`** - Die angezeigten Preise enthalten keine festen Produktsteuern. Der FPT-Betrag wird separat angezeigt.<br/>**`Excluding FPT`**- Die angezeigten Preise enthalten keine festen Produktsteuern. Der FPT-Betrag wird nicht separat angezeigt. |
| [!UICONTROL Display Prices in Emails] | Webseite | Steuert die Anzeige von FPT in E-Mails. Optionen:<br/> **`Including FPT Only`** - Die angezeigten Preise beinhalten feste Produktsteuern. Der FPT-Betrag wird nicht separat angezeigt.<br/>**`Including FPT and FPT description`**- Die angezeigten Preise beinhalten feste Produktsteuern. Der FPT-Betrag wird separat angezeigt.<br/>** Ausschließen von FPT. Einschließlich FPT-Beschreibung und Endpreis **- Angezeigte Preise enthalten keine festen Produktsteuern. Der FPT-Betrag wird separat angezeigt.<br/>**`Excluding FPT`** - Die angezeigten Preise enthalten keine festen Produktsteuern. Der FPT-Betrag wird nicht separat angezeigt. |
| [!UICONTROL Apply Tax to FPT] | Webseite | Bestimmt, ob die Steuer auf den FPT-Betrag angewendet wird. Optionen: `Yes` / `No` |
| [!UICONTROL Include FPT in Subtotal] | Webseite | Bestimmt, ob FPT in der Zwischensumme des Warenkorbs enthalten ist. Optionen: <br/>**`Yes`**- Schließt die FPT in die Zwischensumme des Warenkorbs ein.<br/>**`No`** - FPT ist nicht in der Zwischensumme enthalten und wird nach der Zwischensumme im Warenkorb platziert. |

{style="table-layout:auto"}
