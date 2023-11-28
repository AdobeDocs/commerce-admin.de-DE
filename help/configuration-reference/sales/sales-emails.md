---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Sales Emails]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der [!UICONTROL Sales] &gt; [!UICONTROL Sales Emails] Seite des Commerce-Administrators.
exl-id: f770e202-6f7e-4f84-9251-7d8a760260b4
feature: Configuration, Communications
source-git-commit: 74cc15bd7e0873705b46175ae5f277b1753ec5b5
workflow-type: tm+mt
source-wordcount: '2379'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Sales Emails]

{{config}}

## [!UICONTROL General Settings]

![Allgemeine Einstellungen](./assets/sales-emails-general-settings.png)<!-- zoom -->

<!-- [General Settings](https://docs.magento.com/user-guide/system/email-communications.html) -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Asynchronous sending] | Global | Bestimmt, ob Verkaufs-E-Mails asynchron gesendet werden. Es wird empfohlen, den asynchronen Versand zu aktivieren. Optionen: <br/>**`Disable`**- (Standard) E-Mails zum Verkauf werden gesendet, wenn sie durch ein Ereignis ausgelöst werden.<br/>**`Enable`** - (Empfohlen) E-Mails zum Verkauf werden in vordefinierten, regelmäßigen Abständen gesendet. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Order]

![Bestellung](./assets/sales-emails-order.png)<!-- zoom -->

<!-- [Order](https://docs.magento.com/user-guide/sales/orders.html) -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enabled] | Store-Ansicht | Wenn diese Option aktiviert ist, wird für jede aufgegebene Bestellung eine Transaktions-E-Mail gesendet. Optionen: `Yes` / `No` |
| [!UICONTROL New Order Confirmation Email Sender] | Store-Ansicht | Identifiziert den Store-Kontakt, der als Absender der Nachricht angezeigt wird. Standardabsender: `Sales Representative` |
| [!UICONTROL New Order Confirmation Template] | Store-Ansicht | Identifiziert die Vorlage, die zur Bestätigung neuer von Kunden aufgegebener Bestellungen gesendet wird. Standardvorlage: `New Order` |
| [!UICONTROL New Order Confirmation Template for Guest] | Store-Ansicht | Identifiziert die Vorlage, die zur Bestätigung neuer Bestellungen von Gästen gesendet wird. Standardvorlage: `New Order for Guest` |
| [!UICONTROL Send Order Email Copy To] | Store-Ansicht | Gibt die E-Mail-Adresse eines jeden an, der eine Kopie einer Bestell-E-Mail erhält. Trennen Sie mehrere Adressen durch Kommas. |
| [!UICONTROL Send Order Email Copy Method] | Store-Ansicht | Gibt die zum Senden der Kopie verwendete E-Mail-Methode an. Zu den Optionen gehören: <br/>**`Bcc`**- Sendet eine blinde höfliche Kopie, indem der Empfänger in die Kopfzeile derselben E-Mail eingefügt wird, die an den Kunden gesendet wird. Der BCC-Empfänger ist für den Kunden nicht sichtbar.<br/>**`Separate Email`** - Sendet die Kopie als separate E-Mail. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Order Comments]

![Bestellkommentare](./assets/sales-emails-order-comments.png)<!-- zoom -->

<!-- [Order Comments](https://docs.magento.com/user-guide/sales/order-processing.html) -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enabled] | Store-Ansicht | Wenn diese Option aktiviert ist, wird für jeden Bestellkommentar eine Transaktions-E-Mail gesendet. Optionen: `Yes` / `No` |
| [!UICONTROL Order Comment Email Sender] | Store-Ansicht | Identifiziert den Store-Kontakt, der als Absender der Nachricht angezeigt wird. Standardabsender: `Sales Representative` |
| [!UICONTROL Order Comment Email Template] | Store-Ansicht | Identifiziert die Vorlage, die gesendet wird, wenn einem Kundenauftrag ein Kommentar hinzugefügt wird. Standardvorlage: `Order Update` |
| [!UICONTROL New Order Confirmation Template for Guest] | Store-Ansicht | Identifiziert die Vorlage, die gesendet wird, wenn einem Gastauftrag ein Kommentar hinzugefügt wird. Standardvorlage: `Order Update for Guest` |
| [!UICONTROL Send Order Email Copy To|Store View] | Gibt die E-Mail-Adresse eines jeden an, der eine Kopie einer E-Mail mit einem Bestellkommentar erhält. Trennen Sie mehrere Adressen durch Kommas. |
| [!UICONTROL Send Order Email Copy Method] | Store-Ansicht | Gibt die Methode an, die zum Senden der Kopie verwendet wird. Zu den Optionen gehören: <br/>**`Bcc`**- Sendet eine blinde höfliche Kopie, indem der Empfänger in die Kopfzeile derselben E-Mail eingefügt wird, die an den Kunden gesendet wird. Der BCC-Empfänger ist für den Kunden nicht sichtbar.<br/>**`Separate Email`** - Sendet die Kopie als separate E-Mail. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Invoice]

![Rechnung](./assets/sales-emails-invoice.png)<!-- zoom -->

<!-- [Invoice](https://docs.magento.com/user-guide/sales/invoices.html) -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enabled] | Store-Ansicht | Wenn diese Option aktiviert ist, wird für jede erstellte Rechnung eine Transaktions-E-Mail gesendet. Optionen: `Yes` / `No` |
| [!UICONTROL Invoice Email Sender] | Store-Ansicht | Identifiziert den Store-Kontakt, der als Absender der Nachricht angezeigt wird. Standardabsender: `Sales Representative` |
| [!UICONTROL Invoice Email Template] | Store-Ansicht | Identifiziert die Vorlage, die gesendet wird, wenn eine Rechnung für einen Kunden generiert wird. Standardvorlage: `New Invoice` |
| [!UICONTROL Invoice Email Template for Guest] | Store-Ansicht | Identifiziert die Vorlage, die gesendet wird, wenn eine Rechnung für einen Gast generiert wird. Standardvorlage: `New Invoice for Guest` |
| [!UICONTROL Send Invoice Email Copy To] | Store-Ansicht | Gibt die E-Mail-Adresse eines Empfängers an, um eine Kopie einer E-Mail mit einer Rechnung zu erhalten. Trennen Sie mehrere Adressen durch Kommas. |
| [!UICONTROL Send Invoice Email Copy Method] | Store-Ansicht | Gibt die Methode an, die zum Senden der Kopie verwendet wird. Zu den Optionen gehören: <br/>**`Bcc`**- Sendet eine blinde höfliche Kopie, indem der Empfänger in die Kopfzeile derselben E-Mail eingefügt wird, die an den Kunden gesendet wird. Der BCC-Empfänger ist für den Kunden nicht sichtbar.<br/>**`Separate Email`** - Sendet die Kopie als separate E-Mail. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Invoice Comments]

![Rechnungskommentare](./assets/sales-emails-invoice-comments.png)<!-- zoom -->

<!-- [Invoice Comments](https://docs.magento.com/user-guide/sales/invoice-create.html) -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enabled] | Store-Ansicht | Wenn diese Option aktiviert ist, wird für jeden Rechnungskommentar eine Transaktions-E-Mail gesendet. Optionen: `Yes` / `No` |
| [!UICONTROL Invoice Comment Email Sender] | Store-Ansicht | Identifiziert den Store-Kontakt, der als Absender der Nachricht angezeigt wird. Standardabsender: `Sales Representative` |
| [!UICONTROL Invoice Comment Email Template] | Store-Ansicht | Identifiziert die Vorlage, die gesendet wird, wenn ein Kommentar zu einer Kundenrechnung hinzugefügt wird. Standardvorlage: `Invoice Update` |
| [!UICONTROL Invoice Comment Email Template for Guest] | Store-Ansicht | Identifiziert die Vorlage, die gesendet wird, wenn einem Gastrechner ein Kommentar hinzugefügt wird. Standardvorlage: `Invoice Update for Guest` |
| [!UICONTROL Send Invoice Comment Email Copy To] | Store-Ansicht | Gibt die E-Mail-Adresse eines jeden an, der eine Kopie einer E-Mail mit einem Rechnungskommentar erhält. Trennen Sie mehrere Adressen durch Kommas. |
| [!UICONTROL Send Invoice Comments Email Copy Method] | Store-Ansicht | Gibt die zum Senden der Kopie verwendete E-Mail-Methode an. Zu den Optionen gehören: <br/>**`Bcc`**- Sendet eine blinde höfliche Kopie, indem der Empfänger in die Kopfzeile derselben E-Mail eingefügt wird, die an den Kunden gesendet wird. Der BCC-Empfänger ist für den Kunden nicht sichtbar.<br/>**`Separate Email`** - Sendet die Kopie als separate E-Mail. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Shipment]

![Versand](./assets/sales-emails-shipment.png)<!-- zoom -->

<!-- [Shipment](https://docs.magento.com/user-guide/sales/shipments.html) -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enabled] | Store-Ansicht | Wenn diese Option aktiviert ist, wird für jede erzeugte Sendung eine Transaktions-E-Mail gesendet. Optionen: `Yes` / `No` |
| [!UICONTROL Shipment Email Sender] | Store-Ansicht | Identifiziert den Store-Kontakt, der als Absender der Nachricht angezeigt wird. Standardabsender: `Sales Representative` |
| [!UICONTROL Shipment Email Template] | Store-Ansicht | Identifiziert die Vorlage, die gesendet wird, wenn eine Sendung für einen Kunden generiert wird. Standardvorlage: `New Shipment` |
| [!UICONTROL Shipment Email Template for Guest] | Store-Ansicht | Identifiziert die Vorlage, die gesendet wird, wenn eine Sendung für einen Gast generiert wird. Standardvorlage: `New Shipment for Guest` |
| [!UICONTROL Send Shipment Email Copy To] | Store-Ansicht | Liefert die E-Mail-Adresse eines jeden Empfängers, der eine Kopie einer Versand-E-Mail erhalten soll. Trennen Sie mehrere Adressen durch Kommas. |
| [!UICONTROL Send Shipment Email Copy Method] | Store-Ansicht | Gibt die Methode an, die zum Senden der Kopie verwendet wird. Zu den Optionen gehören: <br/>**`Bcc`**- Sendet eine blinde höfliche Kopie, indem der Empfänger in die Kopfzeile derselben E-Mail eingefügt wird, die an den Kunden gesendet wird. Der BCC-Empfänger ist für den Kunden nicht sichtbar.<br/>**`Separate Email`** - Sendet die Kopie als separate E-Mail. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Shipment Comments]

![Versandreaktionen](./assets/sales-emails-shipment-comments.png)<!-- zoom -->

<!-- [Shipment Comments](https://docs.magento.com/user-guide/sales/shipments.html) -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enabled] | Store-Ansicht | Wenn diese Option aktiviert ist, wird für jeden Versandkommentar eine Transaktions-E-Mail gesendet. Optionen: `Yes` / `No` |
| [!UICONTROL Shipment Comment Email Sender] | Store-Ansicht | Identifiziert den Store-Kontakt, der als Absender der Nachricht angezeigt wird. Standardabsender: `Sales Representative` |
| [!UICONTROL Shipment Comment Email Template] | Store-Ansicht | Gibt die Vorlage an, die gesendet wird, wenn einem Kunden ein Kommentar hinzugefügt wird. Standardvorlage: `Shipment Update` |
| [!UICONTROL Shipment Comment Email Template for Guest] | Store-Ansicht | Gibt die Vorlage an, die gesendet wird, wenn einem Gastversand ein Kommentar hinzugefügt wird. Standardvorlage: `Shipment Update for Guest` |
| [!UICONTROL Send Shipment Comment Email Copy To] | Store-Ansicht | Gibt die E-Mail-Adresse eines jeden an, um eine Kopie einer E-Mail mit einem Versandkommentar zu erhalten. Trennen Sie mehrere Adressen durch Kommas. |
| [!UICONTROL Send Shipment Comments Email Copy Method] | Store-Ansicht | Gibt die zum Senden der Kopie verwendete E-Mail-Methode an. Zu den Optionen gehören: <br/>**`Bcc`**- Sendet eine blinde höfliche Kopie, indem der Empfänger in die Kopfzeile derselben E-Mail eingefügt wird, die an den Kunden gesendet wird. Der BCC-Empfänger ist für den Kunden nicht sichtbar.<br/>**`Separate Email`** - Sendet die Kopie als separate E-Mail. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Credit Memo]

![Credit Memo](./assets/sales-emails-credit-memo.png)<!-- zoom -->

<!-- [Credit Memo](https://docs.magento.com/user-guide/sales/credit-memos.html) -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enabled] | Store-Ansicht | Aktiviert die Transaktions-E-Mail für jedes generierte Kreditmemo. Optionen: `Yes` / `No` |
| [!UICONTROL Credit Memo Email Sender] | Store-Ansicht | Identifiziert den Store-Kontakt, der als Absender der Nachricht angezeigt wird. Standardabsender: `Sales Representative` |
| [!UICONTROL Credit Memo Email Template] | Store-Ansicht | Identifiziert die Vorlage, die gesendet wird, wenn ein Kreditmemo für einen Kunden generiert wird. Standardvorlage: `New Credit Memo` |
| [!UICONTROL Credit Memo Email Template for Guest] | Store-Ansicht | Identifiziert die Vorlage, die gesendet wird, wenn ein Credit Memo für einen Gast generiert wird. Standardvorlage: `New Credit Memo for Guest` |
| [!UICONTROL Send Credit Memo Email Copy To] | Store-Ansicht | Liefert die E-Mail-Adresse eines jeden Empfängers, der eine Kopie einer Kreditmemo-E-Mail erhalten soll. Trennen Sie mehrere Adressen durch Kommas. |
| [!UICONTROL Send Credit Memo Email Copy Method] | Store-Ansicht | Gibt die Methode an, die zum Senden der Kopie verwendet wird. Zu den Optionen gehören: <br/>**`Bcc`**- Sendet eine blinde höfliche Kopie, indem der Empfänger in die Kopfzeile derselben E-Mail eingefügt wird, die an den Kunden gesendet wird. Der BCC-Empfänger ist für den Kunden nicht sichtbar.<br/>**`Separate Email`** - Sendet die Kopie als separate E-Mail. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Credit Memo Comments]

![Kommentare zur Kreditvereinbarung](./assets/sales-emails-credit-memo-comments.png)<!-- zoom -->

<!-- [Credit Memo Comments](https://docs.magento.com/user-guide/sales/credit-memo-create.html) -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enabled] | Store-Ansicht | Wenn diese Option aktiviert ist, wird eine Transaktions-E-Mail für jeden Credit Memo-Kommentar gesendet. Optionen: `Yes` / `No` |
| [!UICONTROL Credit Memo Comment Email Sender] | Store-Ansicht | Identifiziert den Store-Kontakt, der als Absender der Nachricht angezeigt wird. Standardabsender: `Sales Representative` |
| [!UICONTROL Credit Memo Comment Email Template] | Store-Ansicht | Identifiziert die Vorlage, die gesendet wird, wenn einem Kundenkreditdokument ein Kommentar hinzugefügt wird. Standardvorlage: `Credit Memo Update` |
| [!UICONTROL Credit Memo Comment Email Template for Guest] | Store-Ansicht | Identifiziert die Vorlage, die gesendet wird, wenn einem Gastkreditmemo ein Kommentar hinzugefügt wird. Standardvorlage: `Credit Memo Update for Guest` |
| [!UICONTROL Send Credit Memo Comment Email Copy To] | Store-Ansicht | Gibt die E-Mail-Adresse eines jeden an, der eine Kopie einer E-Mail mit einem Kommentar erhalten soll. Trennen Sie mehrere Adressen durch Kommas. |
| [!UICONTROL Send Credit Memo Comments Email Copy Method] | Store-Ansicht | Gibt die zum Senden der Kopie verwendete E-Mail-Methode an. Zu den Optionen gehören: <br/>**`Bcc`**- Sendet eine blinde höfliche Kopie, indem der Empfänger in die Kopfzeile derselben E-Mail eingefügt wird, die an den Kunden gesendet wird. Der BCC-Empfänger ist für den Kunden nicht sichtbar.<br/>**`Separate Email`** - Sendet die Kopie als separate E-Mail. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Order Ready For Pickup in Store]

![Bestellbereit für Abholung im Store](./assets/sales-emails-ready-pickup.png)<!-- zoom -->

<!-- [Order Ready For Pickup in Store](https://docs.magento.com/user-guide/shipping/shipping-in-store-delivery.html) -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enabled] | Store-Ansicht | Wenn diese Option aktiviert ist, wird eine Transaktions-E-Mail gesendet, wenn eine Bestellung zur In-Store-Übernahme bereit ist. Optionen: `Yes` / `No` |
| [!UICONTROL Order Ready For Pickup Email Sender] | Store-Ansicht | Identifiziert den Store-Kontakt, der als Absender der Nachricht angezeigt wird. Standardabsender: `General Contact` |
| [!UICONTROL Order Ready For Pickup Email Template] | Store-Ansicht | Identifiziert die Vorlage, die für die Transaktions-E-Mail für jede Bestellung verwendet wird, die für einen registrierten Kunden abgeholt werden kann. Standardvorlage: `Order is Ready for Pickup` |
| [!UICONTROL Order Ready For Pickup Email Template for Guest] | Store-Ansicht | Identifiziert die Vorlage, die für die Transaktions-E-Mail für jede Bestellung verwendet wird, die für einen Gast abgeholt werden kann. Standardvorlage: `Order is Ready for Pickup for Guest` |
| Bestellung bereit zum Abruf der E-Mail-Kopie an senden | Store-Ansicht | Gibt die E-Mail-Adresse eines jeden an, der eine Kopie eines _Bestellung bereit für Abruf_ E-Mail Trennen Sie mehrere Adressen durch Kommas. |
| [!UICONTROL Send Order Ready For Pickup Email Copy Method] | Store-Ansicht | Gibt die zum Senden der Kopie verwendete E-Mail-Methode an. Optionen: <br/>**`Bcc`**- Sendet eine blinde höfliche Kopie, indem der Empfänger in die Kopfzeile derselben E-Mail eingefügt wird, die an den Kunden gesendet wird. Der BCC-Empfänger ist für den Kunden nicht sichtbar.<br/>**`Separate Email`** - Sendet die Kopie als separate E-Mail. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Purchase Order Approval]

{{b2b-feature}}

![Bestellbestätigung](./assets/sales-emails-purchase-order-approval.png)<!-- zoom -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enabled] | Store-Ansicht | Wenn diese Option aktiviert ist, werden E-Mails während des Bestellvorgangs gesendet. Optionen: `Yes` / `No` |
| [!UICONTROL Created and requires Approval Purchase Order (to Buyer)] | Store-Ansicht | Sendet eine E-Mail-Bestätigung an den Ersteller der Bestellung. |
| [!UICONTROL Created and Automatically approved Purchase Order (to Buyer)] | Store-Ansicht | Sendet eine E-Mail-Bestätigung an den Ersteller der Bestellung. |
| [!UICONTROL Approved Purchase Order (to Buyer)] | Store-Ansicht | Sendet eine E-Mail an den Ersteller bei der Bestellvalidierung. |
| [!UICONTROL Rejected Purchase Order (to Buyer)] | Store-Ansicht | Sendet eine E-Mail an den Ersteller, wenn die Bestellung abgelehnt wurde. |
| [!UICONTROL Comment added to Purchase Order] | Store-Ansicht | Sendet eine E-Mail an den Ersteller, wenn der Bestellung ein Kommentar hinzugefügt wurde. |
| [!UICONTROL Error creating Order from Purchase Order (to Buyer)] | Store-Ansicht | Benachrichtigt den Ersteller darüber, dass beim Konvertieren einer Bestellaufgabe ein Fehler aufgetreten ist. |
| [!UICONTROL Purchase Order required Approval (to Approver)] | Store-Ansicht | Sendet eine E-Mail, um den Genehmiger darüber zu informieren, dass die Bestellung genehmigt werden muss. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Quote]

{{b2b-feature}}

![Anführungszeichen](./assets/sales-emails-quote.png)<!-- zoom -->

<!-- [Quotes](https://docs.magento.com/user-guide/customers/account-dashboard-quotes.html) -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enabled] | Store-Ansicht | Aktiviert Anführungszeichen für E-Mail-Nachrichten, die aus der aktuellen Store-Ansicht gesendet werden. Optionen: `Yes` / `No` |
| [!UICONTROL Updated Quote Template (to Buyer)] | Store-Ansicht | Bestimmt die E-Mail-Vorlage, die für die Benachrichtigung verwendet wird, die an den Käufer gesendet wird, wenn ein aktualisiertes Angebot verfügbar ist. Standardvorlage: `Updated Quote` |
| [!UICONTROL Declined Quote Template (to Buyer)] | Store-Ansicht | Bestimmt die E-Mail-Vorlage, die für Benachrichtigungen verwendet wird, die an den Käufer gesendet werden, wenn ein Angebot abgelehnt wird. Standardvorlage: `Declined Quote` |
| [!UICONTROL New Quote Template (to Seller)] | Store-Ansicht | Bestimmt die E-Mail-Vorlage, die für die Benachrichtigung verwendet wird, die an den Verkäufer gesendet wird, wenn eine Anfrage für ein neues Angebot empfangen wird. Standardvorlage: `New Quote` |
| [!UICONTROL Updated Quote Template (to Seller)] | Store-Ansicht | Bestimmt die E-Mail-Vorlage, die für die Benachrichtigung verwendet wird, die beim Erhalt eines aktualisierten Angebots an den Verkäufer gesendet wird. Standardvorlage: `Updated Quote` |
| [!UICONTROL Quote Expiration (in 48 hrs)] | Store-Ansicht | Gibt die E-Mail-Vorlage an, die für den Ablaufhinweis verwendet wird, der 48 Stunden vor Ablauf des Anführungszeichens gesendet wird. Standardvorlage: `Expiration Warning` |
| [!UICONTROL Quote Expiration (in 24 hrs)] | Store-Ansicht | Gibt die E-Mail-Vorlage an, die für den Ablaufhinweis verwendet wird, der 24 Stunden vor Ablauf des Anführungszeichens gesendet wird. Standardvorlage: `Expiration Warning 1` |
| [!UICONTROL Expiration Date Reset] | Store-Ansicht | Gibt die E-Mail-Vorlage an, die für den Hinweis verwendet wird, der gesendet wird, wenn sich das Ablaufdatum ändert. Standardvorlage: `Expiration Date Reset` |
| [!UICONTROL Send Quote Email Copy To] | Store-Ansicht | Gibt die E-Mail-Adresse jeder Person an, die eine Kopie der Angebots-E-Mail erhalten soll. Trennen Sie mehrere Adressen durch Kommas. |
| [!UICONTROL Send Quote Email Copy Method] | Store-Ansicht | Gibt die zum Senden der Kopie verwendete E-Mail-Methode an. Zu den Optionen gehören: <br/>**`Bcc`**- Sendet eine blinde höfliche Kopie, indem der Empfänger in die Kopfzeile derselben E-Mail eingefügt wird, die an den Kunden gesendet wird. Der BCC-Empfänger ist für den Kunden nicht sichtbar.<br/>**`Separate Email`** - Sendet die Kopie als separate E-Mail. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL RMA]

{{ee-feature}}

![RMA](./assets/sales-emails-rma.png)<!-- zoom -->

<!-- [RMA](https://docs.magento.com/user-guide/sales/returns.html) -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enabled] | Store-Ansicht | Aktiviert E-Mail-Benachrichtigungen für jeden erzeugten RMA. Optionen: `Yes` / `No` |
| [!UICONTROL RMA Email Sender] | Store-Ansicht | Identifiziert die [Store-Kontakt](../../getting-started/store-details.md#store-email-addresses) , der als Absender der Nachricht erscheint. Standardwert: `Sales Representative` |
| [!UICONTROL RMA Email Template] | Store-Ansicht | Bestimmt die [E-Mail-Vorlage](../../systems/email-templates.md) wird für die Benachrichtigung verwendet, die gesendet wird, wenn eine RMA für einen Kunden generiert wird. Standardvorlage: `New RMA` |
| [!UICONTROL RMA Email Template for Guest] | Store-Ansicht | Bestimmt die Vorlage, die gesendet wird, wenn eine RMA für einen Gast generiert wird. Standardvorlage: `New RMA for Guest` |
| [!UICONTROL Send RMA Email Copy To] | Store-Ansicht | Gibt die E-Mail-Adresse eines jeden an, der eine Kopie einer RMA-E-Mail erhalten soll. Trennen Sie mehrere Adressen durch Kommas. |
| [!UICONTROL Send RMA  Email Copy Method] | Store-Ansicht | Gibt die zum Senden der Kopie verwendete E-Mail-Methode an. Zu den Optionen gehören: <br/>**`Bcc`**- Sendet eine blinde höfliche Kopie, indem der Empfänger in die Kopfzeile derselben E-Mail eingefügt wird, die an den Kunden gesendet wird. Der BCC-Empfänger ist für den Kunden nicht sichtbar.<br/>**`Separate Email`** - Sendet die Kopie als separate E-Mail. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL RMA Authorization]

{{ee-feature}}

![RMA-Autorisierung](./assets/sales-emails-rma-auth.png)<!-- zoom -->

<!-- [RMA Authorization](https://docs.magento.com/user-guide/sales/rma-configure.html) -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enabled] | Store-Ansicht | Wenn diese Option aktiviert ist, sendet für jede RMA-Autorisierung eine E-Mail-Benachrichtigung. Optionen: `Yes` / `No` |
| [!UICONTROL RMA Authorization Email Sender] | Store-Ansicht | Identifiziert die [Store-Kontakt](../../getting-started/store-details.md#store-email-addresses) , der als Absender der Nachricht erscheint. Standardwert: `Sales Representative` |
| [!UICONTROL RMA Authorization Email Template] | Store-Ansicht | Bestimmt die [E-Mail-Vorlage](../../systems/email-templates.md) wird verwendet, wenn eine RMA-Genehmigungs-Benachrichtigung gesendet wird. Standardvorlage: `RMA Authorization` |
| [!UICONTROL RMA Authorization Email Template for Guest] | Store-Ansicht | Bestimmt die Vorlage, die verwendet wird, wenn eine RMA-Autorisierungsbenachrichtigung an einen Gast gesendet wird. Standardvorlage: `RMA Authorization for Guest` |
| [!UICONTROL Send RMA Authorization Email Copy To] | Store-Ansicht | Gibt die E-Mail-Adresse eines jeden an, um eine Kopie einer RMA-Autorisierungs-E-Mail zu erhalten. Trennen Sie mehrere Adressen durch Kommas. |
| [!UICONTROL Send RMA Authorization Email Copy Method] | Store-Ansicht | Gibt die zum Senden der Kopie verwendete E-Mail-Methode an. Zu den Optionen gehören: <br/>**`Bcc`**- Sendet eine blinde höfliche Kopie, indem der Empfänger in die Kopfzeile derselben E-Mail eingefügt wird, die an den Kunden gesendet wird. Der BCC-Empfänger ist für den Kunden nicht sichtbar.<br/>**`Separate Email`** - Sendet die Kopie als separate E-Mail. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL RMA Admin Comments]

{{ee-feature}}

![RMA-Administratorkommentare](./assets/sales-emails-rma-admin-comments.png)<!-- zoom -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enabled] | Store-Ansicht | Wenn diese Option aktiviert ist, wird für jeden RMA-Administratorkommentar eine E-Mail-Benachrichtigung gesendet. Optionen: `Yes` / `No` |
| [!UICONTROL RMA Comment Email Sender] | Store-Ansicht | Identifiziert die [Store-Kontakt](../../getting-started/store-details.md#store-email-addresses) , der als Absender der Nachricht erscheint. Standardwert: `Sales Representative` |
| [!UICONTROL RMA Comment Email Template] | Store-Ansicht | Bestimmt die [E-Mail-Vorlage](../../systems/email-templates.md) wird verwendet, wenn ein Administrator einem RMA einen Kommentar für einen Kunden hinzufügt. Standardvorlage: `RMA Admin Comments` |
| [!UICONTROL RMA Comment Email Template for Guest] | Store-Ansicht | Bestimmt die Vorlage, die verwendet wird, wenn ein Administrator einem RMA einen Kommentar für einen Gast hinzufügt. Standardvorlage: `RMA Admin Comments for Guest` |
| [!UICONTROL Send RMA Comment Email Copy To] | Store-Ansicht | Gibt die E-Mail-Adresse eines Kontakts an, um eine Kopie der Benachrichtigung zu erhalten. Trennen Sie mehrere Adressen durch Kommas. |
| [!UICONTROL Send RMA Comments Email Copy Method] | Store-Ansicht | Gibt die zum Senden der Kopie verwendete E-Mail-Methode an. Zu den Optionen gehören: <br/>**`Bcc`**- Sendet eine blinde höfliche Kopie, indem der Empfänger in die Kopfzeile derselben E-Mail eingefügt wird, die an den Kunden gesendet wird. Der BCC-Empfänger ist für den Kunden nicht sichtbar.<br/>**`Separate Email`** - Sendet die Kopie als separate E-Mail. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL RMA Customer Comments]

{{ee-feature}}

![RMA-Kundenkommentare](./assets/sales-emails-rma-customer-comments.png)<!-- zoom -->

<!-- [RMA Customer Comments](https://docs.magento.com/user-guide/sales/returns.html) -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enabled] | Store-Ansicht | Wenn diese Option aktiviert ist, wird eine E-Mail-Benachrichtigung für jeden RMA-Kundenkommentar gesendet. Optionen: `Yes` / `No` |
| [!UICONTROL RMA Comment Email Sender] | Store-Ansicht | Identifiziert die [Store-Kontakt](../../getting-started/store-details.md#store-email-addresses) , der als Absender der Nachricht erscheint. Standardwert: `Customer Support` |
| [!UICONTROL RMA Comment Email Recipient] | Store-Ansicht | Identifiziert den Store-Kontakt, der Empfänger der E-Mail mit dem Kundenkommentar ist. Standardwert: `Sales Representative` |
| [!UICONTROL RMA Comment Email Template] | Store-Ansicht | Bestimmt die [E-Mail-Vorlage](../../systems/email-templates.md) wird verwendet, wenn ein Kunde einem RMA einen Kommentar hinzufügt. Standardvorlage: `RMA Admin Comments` |
| [!UICONTROL Send RMA Comment Email Copy To] | Store-Ansicht | Gibt die E-Mail-Adresse eines Kontakts an, um eine Kopie der Benachrichtigung zu erhalten. Trennen Sie mehrere Adressen durch Kommas. |
| [!UICONTROL Send RMA Comments Email Copy Method] | Store-Ansicht | Gibt die zum Senden der Kopie verwendete E-Mail-Methode an. Zu den Optionen gehören: <br/>**`Bcc`**- Sendet eine blinde höfliche Kopie, indem der Empfänger in die Kopfzeile derselben E-Mail eingefügt wird, die an den Kunden gesendet wird. Der BCC-Empfänger ist für den Kunden nicht sichtbar.<br/>**`Separate Email`** - Sendet die Kopie als separate E-Mail. |

{:style=&quot;table-layout:auto&quot;}
