---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Tax]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Sales] &gt; [!UICONTROL Tax] des Commerce Admin-Bereichs.
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
>Die Adobe Commerce- und Magento Open Source-Versionen 2.4.0 bis 2.4.3 enthielten die von Vertex entwickelte Erweiterung, die zur Integration mit dem [!UICONTROL Vertex Cloud] verwendet wurde. Ab Version 2.4.4 ist diese Erweiterung nicht mehr mit der Hauptversion gebündelt und muss von der Commerce Marketplace installiert und aktualisiert werden. Der Marketplace bietet außerdem Zugriff auf die aktuelle Dokumentation, die vom Erweiterungsentwickler bereitgestellt wird.
><br><br>
>Wenn Sie die gebündelte Erweiterung aktiviert und konfiguriert haben, müssen Sie Ihre Datei „composer.json“ im Rahmen des Upgrade-Prozesses auf 2.4.4 aktualisieren, um zukünftige Erweiterungs-Updates zu verwalten. Weitere Informationen [&#x200B; Sie unter „Upgrade](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html?lang=de)Module und -Erweiterungen“ _„Upgrade-Handbuch_.

{{config}}

## [!UICONTROL Tax Classes]

![Steuerklassen](./assets/tax-tax-classes.png)<!-- zoom -->

Weitere Informationen zum Ändern dieser Einstellungen finden Sie unter [Steuerklassen](../../stores-purchase/tax-class.md) im Handbuch _Stores und Kauferlebnis_.

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Tax Class for Shipping] | Website | Gibt die Steuerklasse an, die für den Versand verwendet wird. Die Optionen umfassen alle verfügbaren Produktsteuerklassen: `None` / `Taxable Goods` / `Shipping` / `Tax Exempt` |
| [!UICONTROL Tax Class for Gift Options] | Website | ![Adobe Commerce](../../assets/adobe-logo.svg) (nur Adobe Commerce) Gibt die standardmäßige Steuerklasse an, die für Geschenkoptionen verwendet wird. |
| [!UICONTROL Default Tax Class for Product] | Global | Gibt die standardmäßige Steuerklasse an, die für Produkte verwendet wird. |
| [!UICONTROL Default Tax Class for Customer] | Global | Gibt die standardmäßige Steuerklasse an, die für Debitoren verwendet wird. |

{style="table-layout:auto"}

## [!UICONTROL Calculation Settings]

![Berechnungseinstellungen](./assets/tax-calculation-settings.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Tax Calculation Method Based On] | Website | Bestimmt die Methode, die zur Berechnung der Steuer für einen Auftrag verwendet wird. Optionen: <br/>**`Unit Price`**- Steuerberechnungen basieren auf dem Einheitspreis jedes Produkts.<br/>**`Row Total`** - Steuerberechnungen basieren auf der Zeileneintragssumme. <br/>**`Total`**- Steuerberechnungen basieren auf der Bestellsumme.<br/><br/>_ **&#x200B; Hinweis:**&#x200B;_Wenn eine Steuerberechnungserweiterung vom Marketplace installiert wird, z. B. _Vertex Cloud_, wird der Erweiterungsdienst als Option aufgeführt. |
| [!UICONTROL Tax Calculation Based On] | Website | Bestimmt, ob die Steuerberechnung auf der Lieferadresse, der Rechnungsadresse oder der Versandherkunft basiert. Optionen: `Shipping Address` / `Billing Address` / `Shipping Origin` |
| [!UICONTROL Catalog Prices] | Website | Legt fest, ob Katalogpreise Steuern enthalten oder nicht. Optionen: `Excluding Tax` / `Including Tax` |
| [!UICONTROL Shipping Prices] | Website | Bestimmt in den Versandpreisen inklusive oder exklusive Steuer. Optionen: `Excluding Tax` / `Including Tax` |
| [!UICONTROL Apply Customer Tax] | Website | Bestimmt, ob vor oder nach einem Rabatt eine Steuer erhoben wird. Optionen: `Before Discount` / `After Discount` |
| [!UICONTROL Apply Discount on Prices] | Website | Bestimmt, ob Rabattpreise Steuern enthalten oder nicht. Optionen: `Excluding Tax` / `Including Tax` |
| [!UICONTROL Apply Tax On] | Website | Legt fest, ob die Steuer auf den ursprünglichen Preis oder, falls verfügbar, auf einen benutzerdefinierten Preis angewendet wird. Optionen: `Custom price if available` / `Original price only` |
| [!UICONTROL Enable Cross Border Trade] | Website | Wenn diese Option aktiviert ist, wird eine konsistente Preisgestaltung über Grenzen von Regionen mit unterschiedlichen Steuersätzen hinweg angewendet. Optionen: `Yes` / `No` <br/><br/>**_Hinweis:_**&#x200B;Bei grenzüberschreitendem Handel wird die Gewinnspanne nach Steuersatz angepasst. |

{style="table-layout:auto"}

## [!UICONTROL Default Tax Destination Calculation]

![Standardmäßige Zielberechnung der Steuer](./assets/tax-default-tax-destination-calculation.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Default Country] | Shop-Ansicht | Bestimmt das Land, auf dem die Steuerberechnungen basieren. |
| [!UICONTROL Default State] | Shop-Ansicht | Bestimmt den Status, auf dem die Steuerberechnungen basieren. Ein Sternchen (*) kann als Platzhalter dienen, um alle Bundesstaaten innerhalb des gewählten Landes anzuzeigen. |
| [!UICONTROL Default Post Code] | Shop-Ansicht | Gibt die Postleitzahl oder Postleitzahl an, auf der die Steuerberechnungen basieren. Ein Sternchen (*) kann als Platzhalter dienen, um alle Postleitzahlen innerhalb des gewählten Status anzuzeigen. |

{style="table-layout:auto"}

## [!UICONTROL Price Display Settings]

![Preisanzeigeeinstellungen](./assets/tax-price-display-settings.png)<!-- zoom -->

Weitere Informationen zum Ändern dieser Einstellungen finden Sie unter [Konfigurieren der Preisanzeigeeinstellungen](../../stores-purchase/display-settings.md#configure-price-display-settings) im _Shops und Kauferlebnis_.

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Display Product Prices in Catalog] | Shop-Ansicht | Bestimmt, ob im Katalog veröffentlichte Produktpreise Steuern enthalten oder ausschließen oder zwei Versionen des Preises anzeigen, eine mit und die andere ohne Steuer. Optionen: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` <br/><br/>**_Hinweis:_**&#x200B;Wenn Sie das Feld „Produktpreise anzeigen“ auf `Including Tax` setzen, wird die Steuer nur angezeigt, wenn eine Steuerregel vorhanden ist, die mit der Steuerherkunft übereinstimmt, oder wenn eine Kundenadresse vorhanden ist, die mit der Steuerregel übereinstimmt. Zu den Ereignissen, bei denen eine Übereinstimmung Trigger werden kann, gehören die Erstellung von Kundenkonten, die Anmeldung oder die Verwendung des Tools für Steuer- und Versandschätzungen im Warenkorb. |
| [!UICONTROL Display Shipping Prices] | Shop-Ansicht | Bestimmt, ob die Versandpreise Steuern beinhalten oder ausschließen oder zwei Versionen des Versandpreises anzeigen, eine mit und die andere ohne Steuern. Optionen: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |

{style="table-layout:auto"}

## [!UICONTROL Shopping Cart Display Settings]

![Anzeigeeinstellungen für den Warenkorb](./assets/tax-shopping-cart-display-settings.png)<!-- zoom -->

Weitere Informationen zum Ändern dieser Einstellungen finden Sie unter [Konfigurieren der Anzeigeeinstellungen für den Warenkorb](../../stores-purchase/display-settings.md#step-2-configure-shopping-cart-display-settings) im _Handbuch für Stores und Kauferlebnisse_.

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Display Prices] | Shop-Ansicht | Bestimmt, ob die Preise des Warenkorbs Steuern enthalten oder ausschließen oder zwei Versionen des Preises anzeigen, eine mit und die andere ohne Steuern. Optionen: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Display Subtotal|Store View] | Bestimmt, ob die Zwischensumme des Warenkorbs die Steuer enthält oder ausschließt oder ob zwei Versionen der Zwischensumme angezeigt werden, eine mit und die andere ohne Steuer. Optionen: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Display Shipping Amount] | Shop-Ansicht | Bestimmt, ob der Warenkorb-Versandbetrag die Steuer beinhaltet oder ausschließt oder zwei Versionen des Versandbetrags anzeigt; eine mit und die andere ohne Steuer. Optionen: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Additionally Show Order Total Without Tax] | Shop-Ansicht | Legt fest, ob eine zusätzliche Zeile mit dem Gesamtbetrag ohne Steuer im Warenkorb angezeigt wird. Optionen: `Yes` / `No` |
| [!UICONTROL Display Full Tax Summary] | Shop-Ansicht | Legt fest, ob der Warenkorb eine vollständige Steuerzusammenfassung enthält. Optionen: `Yes` / `No` |
| [!UICONTROL Display Zero Tax Subtotal] | Shop-Ansicht | Bestimmt, ob der Warenkorb eine Steuerzwischensumme enthält, wenn die Steuer null ist. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Orders, Invoices, Credit Memos Display Settings]

![Einstellungen für Bestellungen, Rechnungen, Gutschriften](./assets/tax-orders-invoices-credit-memos-display-settings.png)<!-- zoom -->

Weitere Informationen zum Ändern dieser Einstellungen finden Sie unter [Anzeigeeinstellungen für Bestellungen, Rechnungen und Gutschriften konfigurieren](../../stores-purchase/display-settings.md#step-3-configure-order-invoice-and-credit-memo-display-settings) im Handbuch _Stores und Kauf_.

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Display Prices] | Shop-Ansicht | Bestimmt, ob die Preise in Verkaufsbelegen Steuern enthalten oder nicht enthalten oder ob jedes Dokument zwei Versionen des Preises anzeigt, eine mit und die andere ohne Steuern. Optionen: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Display Subtotal] | Shop-Ansicht | Bestimmt, ob die Zwischensumme der Verkaufsbelege Steuern enthält oder ausschließt oder ob jedes Dokument zwei Versionen der Zwischensumme anzeigt, eine mit und die andere ohne Steuern. Optionen: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Display Shipping Amount] | Shop-Ansicht | Bestimmt, ob der Versandbetrag auf den Verkaufsbelegen die Steuer beinhaltet oder ausschließt oder ob jeder Beleg zwei Versionen der Zwischensumme anzeigt, eine mit und die andere ohne Steuer. Optionen: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Additionally Show Order Total Without Tax] | Shop-Ansicht | Legt fest, ob eine zusätzliche Zeile mit dem Gesamtbetrag ohne Steuer auf Verkaufsbelegen angezeigt wird. Optionen: `Yes` / `No` |
| [!UICONTROL Display Full Tax Summary] | Shop-Ansicht | Legt fest, ob die vollständige Steuerzusammenfassung in den Verkaufsbelegen angezeigt wird. Optionen: `Yes` / `No` |
| [!UICONTROL Display Zero Tax Subtotal] | Shop-Ansicht | Bestimmt, welcher Zwischensummenabschnitt auf Verkaufsbelegen angezeigt wird, wenn keine Steuer erhoben wird. Optionen: `Yes` / `No` |
| [!UICONTROL Display Gift Wrapping Prices] | Shop-Ansicht | ![Adobe Commerce](../../assets/adobe-logo.svg) (nur Adobe Commerce) Legt fest, ob Preise für Geschenkverpackungen in der Zwischensumme enthalten sind. Optionen: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Display Printed Card Prices] | Shop-Ansicht | ![Adobe Commerce](../../assets/adobe-logo.svg) (nur Adobe Commerce) Legt fest, ob die Preise für gedruckte Karten in der Zwischensumme enthalten sind. Optionen: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |

{style="table-layout:auto"}

## [!UICONTROL Fixed Product Taxes]

![Feste Produktsteuer](./assets/tax-fixed-product-taxes.png)<!-- zoom -->

Weitere Informationen zum Ändern dieser Einstellungen finden Sie unter [Feste Produktsteuer (FPT)](../../stores-purchase/fixed-product-tax.md) im _Handbuch zu Stores und Kauferlebnissen_.

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable FPT] | Website | Legt fest, ob FTP verfügbar ist. Optionen: `Yes` / `No` |
| [!UICONTROL Display Prices in Product Lists] | Website | Steuert die Anzeige von Schriftarten in Produktlisten. Optionen:<br/> **`Including FPT Only`** - Die angezeigten Preise beinhalten die fixen Produktsteuern. Der fpt-Betrag wird nicht separat angezeigt.<br/>**`Including FPT and FPT description`**- Die angezeigten Preise beinhalten die fixen Produktsteuern. Der fpt-Betrag wird separat angezeigt.<br/>**`Excluding FPT. Including FPT description and final price`** - Die angezeigten Preise beinhalten keine fixen Produktsteuern. Der fpt-Betrag wird separat angezeigt.<br/>**`Excluding FPT`**- Die angezeigten Preise beinhalten keine fixen Produktsteuern. Der fpt-Betrag wird nicht separat angezeigt. |
| [!UICONTROL Display Prices On Product View Page] | Website | Steuert die Anzeige von FTP auf der Produktseite. Optionen:<br/> **`Including FPT Only`** - Die angezeigten Preise beinhalten die fixen Produktsteuern. Der fpt-Betrag wird nicht separat angezeigt.<br/>**`Including FPT and FPT description`**- Die angezeigten Preise beinhalten die fixen Produktsteuern. Der fpt-Betrag wird separat angezeigt.<br/>**`Excluding FPT. Including FPT description and final price`** - Die angezeigten Preise beinhalten keine fixen Produktsteuern. Der fpt-Betrag wird separat angezeigt.<br/>**`Excluding FPT`**- Die angezeigten Preise beinhalten keine fixen Produktsteuern. Der fpt-Betrag wird nicht separat angezeigt. |
| [!UICONTROL Display Prices in Sales Modules] | Website | Steuert die Anzeige von FTP im Warenkorb und beim Checkout. Optionen:<br/> **`Including FPT Only`** - Die angezeigten Preise beinhalten die fixen Produktsteuern. Der fpt-Betrag wird nicht separat angezeigt.<br/>**`Including FPT and FPT description`**- Die angezeigten Preise beinhalten die fixen Produktsteuern. Der fpt-Betrag wird separat angezeigt.<br/>**`Excluding FPT. Including FPT description and final price`** - Die angezeigten Preise beinhalten keine fixen Produktsteuern. Der fpt-Betrag wird separat angezeigt.<br/>**`Excluding FPT`**- Die angezeigten Preise beinhalten keine fixen Produktsteuern. Der fpt-Betrag wird nicht separat angezeigt. |
| [!UICONTROL Display Prices in Emails] | Website | Steuert die Anzeige von FTP in E-Mails. Optionen:<br/> **`Including FPT Only`** - Die angezeigten Preise beinhalten die fixen Produktsteuern. Der fpt-Betrag wird nicht separat angezeigt.<br/>**`Including FPT and FPT description`**- Die angezeigten Preise beinhalten die fixen Produktsteuern. Der fpt-Betrag wird separat angezeigt.<br/>**&#x200B; Ohne FTP. Einschließlich FTP-Beschreibung und Endpreis &#x200B;**- Die angezeigten Preise beinhalten keine festen Produktsteuern. Der fpt-Betrag wird separat angezeigt.<br/>**`Excluding FPT`** - Die angezeigten Preise beinhalten keine fixen Produktsteuern. Der fpt-Betrag wird nicht separat angezeigt. |
| [!UICONTROL Apply Tax to FPT] | Website | Legt fest, ob der FTP-Betrag mit Steuern belegt wird. Optionen: `Yes` / `No` |
| [!UICONTROL Include FPT in Subtotal] | Website | Bestimmt, ob die FTP in der Zwischensumme des Warenkorbs enthalten ist. Optionen: <br/>**`Yes`**- Enthält FPT in der Zwischensumme des Warenkorbs.<br/>**`No`** - FPT ist nicht in der Zwischensumme enthalten und wird nach der Zwischensumme im Warenkorb platziert. |

{style="table-layout:auto"}
