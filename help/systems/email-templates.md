---
title: E-Mail-Vorlagen
description: Erfahren Sie mehr über E-Mail-Vorlagen und wie Sie sie verwenden können, um die Kommunikation mit Ihren Kunden zu unterstützen und Ihre Marke zu stärken.
exl-id: dfe28c77-607e-41e4-b872-3a07bcd67962
feature: Communications, Configuration
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1151'
ht-degree: 0%

---

# E-Mail-Vorlagen

E-Mail-Vorlagen definieren das Layout, den Inhalt und die Formatierung automatisierter Nachrichten, die von Ihrem Store gesendet werden. Sie werden als Transaktions-E-Mails bezeichnet, da jede E-Mail mit einem bestimmten Transaktions- oder Ereignistyp verknüpft ist.

Commerce enthält eine Reihe responsiver E-Mail-Vorlagen, die durch verschiedene Ereignisse ausgelöst werden, die während des Betriebs Ihres Stores stattfinden. Jede Vorlage ist für jede Bildschirmgröße optimiert und kann vom Desktop aus sowie auf Tablets und Mobilgeräten angezeigt werden. Es gibt verschiedene vorbereitete E-Mail-Vorlagen für Kundenaktivitäten, Verkäufe, Produktwarnungen, Admin-Aktionen und Systemnachrichten, die Sie [anpassen](email-template-custom.md) können, um Ihre Marke widerzuspiegeln.

Commerce-E-Mails können von HTML- und Text-E-Mail-Clients gerendert werden. Die Art und Weise, wie E-Mails gerendert werden, kann zwischen den Clients variieren.

## E-Mail-Logo vorbereiten

Logos können als beliebige der folgenden Dateitypen gespeichert werden. Logos mit transparentem Hintergrund können als .GIF- oder .PNG-Dateien gespeichert werden.

- JPG/JPEG
- GIF
- PNG

In der Kopfzeilenvorlage werden Dimensionen angegeben. Um jedoch sicherzustellen, dass Ihr Logo auf hochauflösenden Geräten gut dargestellt wird, sollte das hochgeladene Bild dreimal so groß sein. In der Regel wird das ursprüngliche Logo-Bildmaterial als Vektorbild erstellt, sodass es skaliert werden kann, ohne die Auflösung zu verlieren. Das Bild kann dann in einem der unterstützten Bitmap-Bildformate gespeichert werden.

<!-- ![Logo 3X display size](./assets/email-logo-third-size.png)-->

Um den eingeschränkten vertikalen Bereich in der Kopfzeile nutzen zu können, müssen Sie das Bild beschneiden, um verschwenderischen Platz am oberen oder unteren Rand zu vermeiden. Achten Sie beim Bearbeiten des Bildes darauf, das Seitenverhältnis des Logos beizubehalten, damit Höhe und Breite proportional geändert werden.

In der Regel können Sie ein Bild kleiner als das Original machen, jedoch nicht größer, ohne die Auflösung zu verlieren. Wenn Sie ein kleines Bild aufnehmen und es in einem Foto-Editor vergrößern, wird die Bildauflösung verringert. Wenn die Anzeigeabmessungen des Logos beispielsweise in der Kopfzeilenvorlage 168 Pixel breit und 48 Pixel hoch sind, sollte das hochgeladene Bild 504 Pixel breit und 144 Pixel hoch sein.

| Logo-Dimensionen | 1 x (Anzeigegröße) | 3 x (Bildgröße) |
|----------|----|----|
| Breite: | 168 px | 504 px |
| Höhe: | 48 px | 144 px |

{style="table-layout:auto"}

## E-Mail-Vorlagen konfigurieren

Die Konfiguration bestimmt das Logo, das in der standardmäßigen Kopfzeilenvorlage angezeigt wird, sowie alle benutzerdefinierten Vorlagen [header](email-template-custom.md#header-template) und [footer](email-template-custom.md#footer-template), die Sie für Transaktions-E-Mail-Nachrichten verwenden möchten, die von Ihren Stores gesendet werden.

![E-Mail-Entwurf für Transaktionen](./assets/design-configuration-transactional-emails.png){width="600" zoomable="yes"}

Eine detaillierte Liste der Konfigurationseinstellungen finden Sie unter [_Transaktions-E-Mails_](../content-design/configuration.md) im _Inhalts- und Designhandbuch_.

## Schritt 1. Hochladen Ihres Logos

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Suchen Sie die Store-Ansicht, die Sie konfigurieren möchten, und klicken Sie in der Spalte _[!UICONTROL Action]_auf **[!UICONTROL Edit]**.

1. Erweitern Sie unter _[!UICONTROL Other Settings]_den Abschnitt ![Erweiterungsauswahl](../assets/icon-display-expand.png) um den Abschnitt **[!UICONTROL Transactional Emails]**.

1. Um Ihre vorbereitete **[!UICONTROL Logo Image]** hochzuladen, klicken Sie auf **[!UICONTROL Upload]** und wählen Sie die Datei aus Ihrem System aus.

1. Geben Sie für **[!UICONTROL Logo Image Alt]** alternativen Text ein, um das Bild zu identifizieren.

1. Geben Sie die Werte **[!UICONTROL Logo Width]** und **[!UICONTROL Logo Height]** in Pixel ein.

   Geben Sie jeden Wert als Zahl ohne die Abkürzung `px` ein. Diese Werte beziehen sich auf die Anzeigedimensionen des Logos in der Kopfzeile und nicht auf die tatsächliche Bildgröße.

## Schritt 2. Kopf- und Fußzeilenvorlagen auswählen

Wenn Sie benutzerdefinierte Kopf- und Fußzeilenvorlagen für Ihren Store oder für verschiedene Stores haben, können Sie entsprechend dem [Umfang](../getting-started/websites-stores-views.md#scope-settings) der Konfiguration festlegen, welche Vorlagen jeweils verwendet werden. Andernfalls werden die Standardvorlagen verwendet. Weitere Informationen finden Sie unter [Anpassen von E-Mail-Vorlagen](email-template-custom.md).

1. Wählen Sie die **[!UICONTROL Header Template]** aus, die für alle Transaktions-E-Mail-Nachrichten verwendet werden soll.

1. Wählen Sie die **[!UICONTROL Footer Template]** aus, die für alle Transaktions-E-Mail-Nachrichten verwendet werden soll.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

## Liste der E-Mail-Vorlagen

Die Liste der E-Mail-Vorlagen ist alphabetisch nach Modul geordnet.

### [!DNL Amazon_Payment]

| Vorlage | Konfigurationspfad |
|--- |--- |
| `Hard-declined Authorization` | Nicht zutreffend |
| `Soft-declined Authorization` | Nicht zutreffend |

{style="table-layout:auto"}

### [!DNL Magento_Checkout]

| Vorlage | Konfigurationspfad |
|--- |--- |
| `Payment Failed` | **Seite:** [!UICONTROL Sales] > [[!UICONTROL Checkout]](../configuration-reference/sales/checkout.md)<br/>**Abschnitt:** [!UICONTROL Payment Failed Emails]<br/>**Feld:** [!UICONTROL Payment Failed Template] |

{style="table-layout:auto"}

### [!DNL Magento_Company]

![Adobe Commerce B2B](../assets/b2b.svg) (nur bei Adobe Commerce B2B verfügbar)

| Vorlage | Konfigurationspfad |
|--- |--- |
| `Assign Company Admin` | **Seite:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Abschnitt:** [!UICONTROL Customer-Related Emails]<br/>**Feld:** [!UICONTROL Default 'Assign Company Admin' Email] |
| `Assign Company to Customer` | **Seite:** [!UICONTROL Customers] > [Unternehmenskonfiguration ](../configuration-reference/customers/company-configuration.md)<br/>**Abschnitt:** [!UICONTROL Customer-Related Emails] <br/>**Feld:** [!UICONTROL Default 'Assign Company to Customer' Email] |
| `Company Admin Changed to Member` | **Seite:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Abschnitt:** [!UICONTROL Customer-Related Emails]<br/>**Feld:** [!UICONTROL Default 'Company Admin Changed To Member' Email] |
| `Company Admin Set Inactive` | **Seite:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Abschnitt:** [!UICONTROL Customer-Related Emails]<br/>**Feld:** [!UICONTROL Default 'Customer Status Inactive' Email] |
| `Company Invite` | Nicht zutreffend |
| `Company Registration Request` | **Seite:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Abschnitt:** [!UICONTROL Email Options - Company Registration]<br/>**Feld:** [!UICONTROL Default Company Registration Email] |
| `Company Status Active1` | **Seite:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Abschnitt:** [!UICONTROL Company Status Change]<br/>**Feld:** [!UICONTROL Default 'Company Status Change To Active 1" Email] |
| `Company Status Active2` | **Seite:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Abschnitt:** [!UICONTROL Company Status Change]<br/>**Feld:** [!UICONTROL Default 'Company Status Change To Active 2" Email] |
| `Company Status Blocked` | **Seite:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Abschnitt:** [!UICONTROL Company Status Change]<br/>**Feld:** [!UICONTROL Default 'Company Status Change To Blocked" Email] |
| `Company Status Pending Approval` | **Seite:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Abschnitt:** [!UICONTROL Company Status Change]<br/>**Feld:** [!UICONTROL Default 'Company Status Change To Pending Approval" Email] |
| `Company Status Rejected` | **Seite:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Abschnitt:** [!UICONTROL Company Status Change]<br/>**Feld:** [!UICONTROL Default 'Company Status Change To Rejected" Email] |
| `Customer Status Active` | **Seite:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Abschnitt:** [!UICONTROL Customer-Related Emails]<br/>**Feld:** [!UICONTROL Default 'Customer Status Active' Email] |
| `Customer Status Inactive` | **Seite:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Abschnitt:** [!UICONTROL Customer-Related Emails]<br/>**Feld:** [!UICONTROL Default 'Company Admin Inactive' Email] |
| `Sales Representative Assigned to Company` | **Seite:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Abschnitt:** [!UICONTROL Customer-Related Emails]<br/>**Feld:** [!UICONTROL Default 'Sales Rep Assigned' Email] |

{style="table-layout:auto"}

### [!DNL Magento_CompanyCredit]

![Adobe Commerce B2B](../assets/b2b.svg) (nur bei Adobe Commerce B2B verfügbar)

| Vorlage | Konfigurationspfad |
|--- |--- |
| `Credit Limit Allocated` | **Seite:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Abschnitt:** [!UICONTROL Company Credit]<br/>**Feld:** [!UICONTROL Allocated Email Template] |
| `Credit Limit Updated` | **Seite:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Abschnitt:** [!UICONTROL Company Credit]<br/>**Feld:** [!UICONTROL Updated Email Template] |
| `Credit Reimbursed` | **Seite:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Abschnitt:** [!UICONTROL Company Credit]<br/>**Feld:** [!UICONTROL Reimbursed Email Template] |
| `Order Refunded to Company Credit` | **Seite:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Abschnitt:** [!UICONTROL Company Credit]<br/>**Feld:** [!UICONTROL Refunded Email Template] |
| `Order Reverted to Company Credit` | **Seite:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**Abschnitt:** [!UICONTROL Company Credit]<br/>**Feld:** [!UICONTROL Reverted Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_Contact]

| Vorlage | Konfigurationspfad |
|--- |--- |
| `Contact Form` | **Seite:** [!UICONTROL General] > [[!UICONTROL Contacts]](../configuration-reference/general/contacts.md)<br/>**Abschnitt:** [!UICONTROL Email Options]<br/>**Feld:** [!UICONTROL Email Template] |

{style="table-layout:auto"}

### [!UICONTROL Magento_Customer]

| Vorlage | Konfigurationspfad |
|--- |--- |
| `Change Email` | **Seite:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Abschnitt:** [!UICONTROL Account Information Options]<br/>**Feld:** [!UICONTROL Change Email Template] |
| E-Mail und Kennwort ändern | **Seite:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Abschnitt:** [!UICONTROL Account Information Options]<br/>**Feld:** [!UICONTROL Change Email and Password Template] |
| `Forgot Password` | **Seite:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Abschnitt:** [!UICONTROL Password Options]<br/>**Feld:** E-Mail-Vorlage vergessen: |
| `New Account` | **Seite:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Abschnitt:** [!UICONTROL Create New Account Options]<br/>**Feld:** Standard-Willkommens-E-Mail |
| `New Account (Magento/luma)` | **Seite:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Abschnitt:** [!UICONTROL Create New Account Options]<br/>**Feld:** Standard-Willkommens-E-Mail |
| `New Account Confirmation Key` | **Seite:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Abschnitt:** [!UICONTROL Create New Account Options]<br/>**Feld:** Bestätigungslink-E-Mail |
| `New Account Confirmed` | **Seite:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Abschnitt:** [!UICONTROL Create New Account Options]<br/>**Feld:** Willkommens-E-Mail |
| `New Account Without Password` | **Seite:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Abschnitt:** [!UICONTROL Create New Account Options]<br/>**Feld:** Standardmäßige Willkommens-E-Mail ohne Kennwort |
| `Remind Password` | **Seite:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Abschnitt:** [!UICONTROL Password Options]<br/>**Feld:** E-Mail-Vorlage erinnern |
| `Reset Password` | **Seite:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Abschnitt:** [!UICONTROL Password Options] <br/>**Feld:** Kennwortvorlage zurücksetzen |

{style="table-layout:auto"}

### [!DNL Magento_CustomerBalance]

![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce)

| Vorlage | Konfigurationspfad |
|--- |--- |
| `Store Credit Update` | **Seite:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**Abschnitt:** [!UICONTROL Store Credit Options]<br/>**Feld:** [!UICONTROL Store Credit Update Email Template] |

{style="table-layout:auto"}

### [!UICONTROL Magento_Directory]

| Vorlage | Konfigurationspfad |
|--- |--- |
| `Currency Update Warnings` | **Seite:** [!UICONTROL General] > [[!UICONTROL Currency Setup]](../configuration-reference/general/currency-setup.md)<br/>**Abschnitt:** [!UICONTROL Scheduled Import Settings]<br/>**Feld:** [!UICONTROL Error Email Template] |

{style="table-layout:auto"}

### [!UICONTROL Magento_Email]

| Vorlage | Konfigurationspfad |
|--- |--- |
| `Footer` | Nicht zutreffend |
| `Footer (Magento/luma)` | Nicht zutreffend |
| `Header` | Nicht zutreffend |

{style="table-layout:auto"}

### [!UICONTROL Magento_GiftCard]

![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce)

| Vorlage | Konfigurationspfad |
|--- |--- |
| `Gift Card(s) Purchase` | **Seite:** [!UICONTROL Sales] > [[!UICONTROL Gift Cards]](../catalog/product-gift-card-create.md)<br/>**Abschnitt:** [!UICONTROL Gift Card Email Settings]<br/>**Feld:** [!UICONTROL Gift Card Notification Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_GiftCardAccount]

| Vorlage | Konfigurationspfad |
|--- |--- |
| `Gift Card Code/Balance` | **Seite:** [!UICONTROL Sales] > [[!UICONTROL Gift Cards]](../catalog/product-gift-card-create.md)<br/>**Abschnitt:** [!UICONTROL Email Sent from Gift Card Account Management]<br/>**Feld:** [!UICONTROL Gift Card Template] |

{style="table-layout:auto"}

### [!DNL Magento_GiftRegistry]

| Vorlage | Konfigurationspfad |
|--- |--- |
| `New Registry` | **Seite:** [!UICONTROL  Customers] > [[!UICONTROL  Gift Registry]](../configuration-reference/customers/gift-registry.md) <br/>**Abschnitt:** [!UICONTROL Owner Notification]<br/>**Feld:** [!UICONTROL Email Template] |
| `Registry Sharing` | **Seite:** [!UICONTROL  Customers] > [[!UICONTROL  Gift Registry]](../configuration-reference/customers/gift-registry.md) <br/>**Abschnitt:** [!UICONTROL Gift Registry Sharing]<br/>**Feld:** [!UICONTROL Email Template] |
| `Registry Update` | **Seite:** [!UICONTROL  Customers] > [[!UICONTROL  Gift Registry]](../configuration-reference/customers/gift-registry.md) <br/>**Abschnitt:** [!UICONTROL Gift Registry Update]<br/>**Feld:** [!UICONTROL Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_InventoryInStorePickupSales]

| Vorlage | Konfigurationspfad |
|--- |--- |
| `Order is Ready for Pickup` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Abschnitt:** [!UICONTROL Order Ready For Pickup in Store]<br/>**Feld:** [!UICONTROL Order Ready For Pickup Email Template] |
| `Order is Ready for Pickup For Guest` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Abschnitt:** [!UICONTROL Order Ready For Pickup in Store]<br/>**Feld:** [!UICONTROL Order Ready For Pickup Email Template for Guest] |

{style="table-layout:auto"}

### [!DNL Magento_Invitation]

| Vorlage | Konfigurationspfad |
|--- |--- |
| `Customer Invitation` | **Seite:** [!UICONTROL Customers] > [[!UICONTROL Invitation]](../configuration-reference/customers/invitations.md)<br/>**Abschnitt:** [!UICONTROL Email]<br/>**Feld:** [!UICONTROL Customer Invitation Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_NegotiableQuote]

![Adobe Commerce B2B](../assets/b2b.svg) (nur bei Adobe Commerce B2B verfügbar)

| Vorlage | Konfigurationspfad |
|--- |--- |
| `Declined Quote` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Abschnitt:** [!UICONTROL Quote]<br/>**Feld:** [!UICONTROL Declined Quote Template (to Buyer)] |
| `Expiration Date Reset` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Abschnitt:** [!UICONTROL Quote]<br/>**Feld:** [!UICONTROL Expiration Date Reset] | **Seite:** [!UICONTROL Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Abschnitt:** [!UICONTROL Quote]<br/>**Feld:** [!UICONTROL Order Ready For Pickup Email Template] |
| `Expiration Warning` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Abschnitt:** [!UICONTROL Quote]<br/>**Feld:** [!UICONTROL Quote Expiration (in 48 hrs)] |
| `Expiration Warning1` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Abschnitt:** [!UICONTROL Quote]<br/>**Feld:** [!UICONTROL Quote Expiration (in 24 hrs)] |
| `New Quote` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Abschnitt:** [!UICONTROL Quote]<br/>**Feld:** [!UICONTROL New Quote Template (to Seller)] |
| `Updated Quote` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Abschnitt:** [!UICONTROL Quote]<br/>**Feld:** [!UICONTROL Updated Quote Template (to Seller)] |

{style="table-layout:auto"}

### [!DNL Magento_Newsletter]

| Vorlage | Konfigurationspfad |
|--- |--- |
| `Subscription Confirmation` | **Seite:** [!UICONTROL Customers] > [[!UICONTROL Newsletter]](../configuration-reference/customers/newsletter.md)<br/>**Abschnitt:** [!UICONTROL  Subscription Options]<br/>**Feld:** [!UICONTROL Confirmation Email Template] |
| `Subscription Success` | **Seite:** [!UICONTROL Customers] > [[!UICONTROL Newsletter]](../configuration-reference/customers/newsletter.md)<br/>**Abschnitt:** [!UICONTROL  Subscription Options]<br/>**Feld:** [!UICONTROL Success Email Template] |
| `Unsubscription Success` | **Seite:** [!UICONTROL Customers] > [[!UICONTROL Newsletter]](../configuration-reference/customers/newsletter.md)<br/>**Abschnitt:** [!UICONTROL  Subscription Options]<br/>**Feld:** [!UICONTROL Unsubscription Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_ProductAlert]

| Vorlage | Konfigurationspfad |
|--- |--- |
| `Cron Error Warning` | **Seite:** [!UICONTROL Catalog] > [[!UICONTROL Catalog]](../configuration-reference/catalog/catalog.md)<br/>**Abschnitt:** [!UICONTROL Product Alerts Run Settings]<br/>**Feld:** [!UICONTROL Error Email Template] |
| `Price Alert` | **Seite:** [!UICONTROL Catalog] > [[!UICONTROL Catalog]](../configuration-reference/catalog/catalog.md)<br/>**Abschnitt:** [!UICONTROL Product Alerts]<br/>**Feld:** [!UICONTROL Price Alert Email Template] |
| `Stock Alert` | **Seite:** [!UICONTROL Catalog] > [[!UICONTROL Catalog]](../configuration-reference/catalog/catalog.md)<br/>**Abschnitt:** [!UICONTROL Product Alerts]<br/>**Feld:** [!UICONTROL Stock Alert Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_PurchaseOrder]

| Vorlage | Konfigurationspfad |
|--- |--- |
| `Approved Purchase Order` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Abschnitt:** [!UICONTROL Purchase Order Approval]<br/>**Feld:** [!UICONTROL Approved Purchase Order] |
| `Approved, requires payment` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Abschnitt:** [!UICONTROL Purchase Order Approval]<br/>**Feld:** [!UICONTROL Approved, requires payment details (to Buyer)] |
| `Comment added to Purchase Order` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Abschnitt:** [!UICONTROL Purchase Order Approval]<br/>**Feld:** [!UICONTROL Comment added to Purchase Order] |
| `Created and Auto-approved Purchase Order` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Abschnitt:** [!UICONTROL Purchase Order Approval]<br/>**Feld:** [!UICONTROL Created and Automatically approved Purchase Order (to Buyer)] |
| `Created and automatically approved, requires payment details` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Abschnitt:** [!UICONTROL Purchase Order Approval]<br/>**Feld:** [!UICONTROL Created and automatically approved, requires payment details (to Buyer)] |
| `Created and requires Approval Purchase Order` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Abschnitt:** [!UICONTROL Purchase Order Approval]<br/>**Feld:** [!UICONTROL Created and requires Approval Purchase Order (to Buyer)] |
| `Error creating Order from Purchase Order` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Abschnitt:** [!UICONTROL Purchase Order Approval]<br/>**Feld:** [!UICONTROL Error creating Order from Purchase Order (to Buyer)] |
| `Purchase Order requires Approval` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Abschnitt:** [!UICONTROL Purchase Order Approval]<br/>**Feld:** [!UICONTROL Purchase Order requires Approval (to Approver)] |
| `Rejected Purchase Order` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Abschnitt:** [!UICONTROL Purchase Order Approval]<br/>**Feld:** [!UICONTROL Rejected Purchase Order (to Buyer)] |

{style="table-layout:auto"}

### [!DNL Magento_Reminder]

![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce)

| Vorlage | Konfigurationspfad |
|--- |--- |
| `Promotion Notification/Reminder` | **Seite:** [!UICONTROL Customers] > [[!UICONTROL Promotions]](../configuration-reference/customers/promotions.md)<br/>**Abschnitt:** [!UICONTROL Automated Email Reminder Rules]<br/>**Feld:** [!UICONTROL Reminder Email Sender] |

{style="table-layout:auto"}

### [!DNL Magento_Reward]

![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce)

| Vorlage | Konfigurationspfad |
|--- |--- |
| `Balance Update` | **Seite:** [!UICONTROL Customers] > [[!UICONTROL Reward Points]](../configuration-reference/customers/reward-points.md)<br/>**Abschnitt:** [!UICONTROL Email Notification Settings]<br/>**Feld:** [!UICONTROL Balance Update Email] |
| `Points Expiry Warning` | **Seite:** [!UICONTROL Customers] > [[!UICONTROL Reward Points]](../configuration-reference/customers/reward-points.md)<br/>**Abschnitt:** [!UICONTROL Email Notification Settings]<br/>**Feld:** [!UICONTROL Reward Points Expiry Warning Email] |

{style="table-layout:auto"}

### [!DNL Magento_Rma]

![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce)

| Vorlage | Konfigurationspfad |
|--- |--- |
| `New RMA` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Abschnitt:** [!UICONTROL  RMA]<br/>**Feld:** [!UICONTROL RMA Email Template] |
| `New RMA for Guest` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Abschnitt:** [!UICONTROL  RMA]<br/>**Feld:** [!UICONTROL RMA Email Template for Guest] |
| `RMA Admin Comments` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Abschnitt:** [!UICONTROL  RMA Admin Comments]<br/>**Feld:** [!UICONTROL RMA Comment Email Template] |
| `RMA Admin Comments for Guest` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Abschnitt:** [!UICONTROL  RMA Admin Comments]<br/>**Feld:** [!UICONTROL RMA Comment Email Template for Guest] |
| `RMA Authorization` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Abschnitt:** [!UICONTROL  RMA Authorization]<br/>**Feld:** [!UICONTROL RMA Authorization Email Template] |
| `RMA Authorization for Guest` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Abschnitt:** [!UICONTROL  RMA Authorization]<br/>**Feld:** [!UICONTROL RMA Authorization Email Template for Guest] |
| `RMA Customer Comments` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**Abschnitt:** [!UICONTROL RMA Customer Comments]<br/>**Feld:** [!DNL RMA Comment Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_Sales]

| Vorlage | Konfigurationspfad |
|--- |--- |
| `Credit Memo Update` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Abschnitt:** [!UICONTROL Credit Memo Contents]<br/>**Feld:** [!UICONTROL Credit Memo Comment Email Template] |
| `Credit Memo Update (Magento/luma)` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Abschnitt:** [!UICONTROL Credit Memo Comments]<br/>**Feld:** [!UICONTROL Credit Memo Comment Email Template] |
| `Credit Memo Update for Guest` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Abschnitt:** [!UICONTROL Credit Memo Comments]<br/>**Feld:** [!UICONTROL Credit Memo Comment Email Template for Guest] |
| `Credit Memo Update for Guest (Magento/luma)` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Abschnitt:** [!UICONTROL Credit Memo Comments]<br/>**Feld:** [!UICONTROL Credit Memo Comment Email Template for Guest] |
| `Invoice Update` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/../configuration-reference/sales/sales-emails.md)<br/>**Abschnitt:** [!UICONTROL Invoice Comments]<br/>**Feld:** [!UICONTROL Invoice Comment Email Template] |
| `Invoice Update (Magento/luma)` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Abschnitt:** [!UICONTROL Invoice Comments]<br/>**Feld:** [!UICONTROL Invoice Comment Email Template] |
| `Invoice Update for Guest` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Abschnitt:** [!UICONTROL Invoice Comments]<br/>**Feld:** [!UICONTROL Invoice Comment Email Template for Guest] |
| `Invoice Update for Guest (Magento/luma)` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Abschnitt:** [!UICONTROL Invoice Comments]<br/>**Feld:** [!UICONTROL Invoice Comment Email Template for Guest] |
| `New Credit Memo` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Abschnitt:** [!UICONTROL Credit Memo]<br/>**Feld:** [!UICONTROL Credit Memo Email Template] |
| `New Credit Memo (Magento/luma)` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]]../configuration-reference/sales/sales-emails.md)<br/>**Abschnitt:** [!UICONTROL Credit Memo]<br/>**Feld:** [!UICONTROL Credit Memo Email Template] |
| `New Credit Memo for Guest` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Abschnitt:** [!UICONTROL Credit Memo]<br/>**Feld:** [!UICONTROL Credit Memo Email Template for Guest] |
| `New Credit Memo for Guest (Magento/luma)` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Abschnitt:** [!UICONTROL Credit Memo]<br/>**Feld:** [!UICONTROL Credit Memo Email Template for Guest] |
| `New Invoice` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Abschnitt:** [!UICONTROL Invoice]<br/>**Feld:** [!UICONTROL Invoice Email Template] |
| `New Invoice (Magento/luma)` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Abschnitt:** [!UICONTROL Invoice]<br/>**Feld:** [!UICONTROL Invoice Email Template] |
| `New Invoice for Guest` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Abschnitt:** [!UICONTROL Invoice]<br/>**Feld:** [!UICONTROL Invoice Email Template for Guest] |
| `New Invoice for Guest (Magento/luma)` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Abschnitt:** [!UICONTROL Invoice]<br/>**Feld:** [!UICONTROL Invoice Email Template for Guest] |
| `New Order` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Abschnitt:** [!UICONTROL Order]<br/>**Feld:** [!UICONTROL New Order Confirmation Template] |
| `New Order (Magento/luma)` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Abschnitt:** [!UICONTROL Order]<br/>**Feld:** [!UICONTROL New Order Confirmation Template] |
| `New Order for Guest` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Abschnitt:** [!UICONTROL Order]<br/>**Feld:** [!UICONTROL New Order Confirmation Template for Guest] |
| `New Order for Guest (Magento/luma)` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Abschnitt:** [!UICONTROL Order]<br/>**Feld:** [!UICONTROL New Order Confirmation Template for Guest] |
| `New Shipment` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Abschnitt:** [!UICONTROL Shipment]<br/>**Feld:** [!UICONTROL Shipment Email Template] |
| `New Shipment (Magento/luma)` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Abschnitt:** [!UICONTROL Shipment]<br/>**Feld:** [!UICONTROL Shipment Email Template] |
| `New Shipment for Guest` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Abschnitt:** [!UICONTROL Shipment]<br/>**Feld:** [!UICONTROL Shipment Email Template for Guest] |
| `New Shipment for Guest (Magento/luma)` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Abschnitt:** [!UICONTROL Shipment]<br/>**Feld:** [!UICONTROL Shipment Email Template for Guest] |
| `Order Update` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Abschnitt:** [!UICONTROL Order Comments]<br/>**Feld:** [!UICONTROL Order Comment Email Template] |
| `Order Update (Magento/luma)` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Abschnitt:** [!UICONTROL Order Comments]<br/>**Feld:** [!UICONTROL Order Comment Email Template] |
| `Order Update for Guest` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Abschnitt:** [!UICONTROL Order Comments]<br/>**Feld:** [!UICONTROL Order Comment Email Template for Guest] |
| `Order Update for Guest (Magento/luma)` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Abschnitt:** [!UICONTROL Order Comments]<br/>**Feld:** [!UICONTROL Order Comment Email Template for Guest] |
| `Shipment Update` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Abschnitt:** [!UICONTROL Shipment Comments]<br/>**Feld:** [!UICONTROL Shipment Comment Email Template] |
| `Shipment Update (Magento/luma)` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Abschnitt:** [!UICONTROL Shipment Comments]<br/>**Feld:** [!UICONTROL Shipment Comment Email Template] |
| `Shipment Update for Guest` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Abschnitt:** [!UICONTROL Shipment Comments]<br/>**Feld:** [!UICONTROL Shipment Comment Email Template for Guest] |
| `Shipment Update for Guest (Magento/luma)` | **Seite:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**Abschnitt:** [!UICONTROL Shipment Comments]<br/>**Feld:** [!UICONTROL Shipment Comment Email Template for Guest] |

{style="table-layout:auto"}

### [!DNL Magento_ScheduledImportExport]

![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce)

| Vorlage | Konfigurationspfad |
|--- |--- |
| `Export Failed` | **Seite:** [!UICONTROL Advanced] > [[!UICONTROL System]](../configuration-reference/advanced/system.md)<br/>**Abschnitt:** [!UICONTROL Scheduled Import/Export File History Cleaning]<br/>**Feld:** [!UICONTROL Export Failed Template] |
| `File History Clean Failed` | **Seite:** [!UICONTROL Advanced] > [[!UICONTROL System]](../configuration-reference/advanced/system.md)<br/>**Abschnitt:** [!UICONTROL Scheduled Import/Export File History Cleaning]<br/>**Feld:** [!UICONTROL Error Email Template] |
| `Import Failed` | **Seite:** [!UICONTROL Advanced] > [[!UICONTROL System]](../configuration-reference/advanced/system.md)<br/>**Abschnitt:** [!UICONTROL Scheduled Import/Export File History Cleaning]<br/>**Feld:** [!UICONTROL Import Failed Template] |

{style="table-layout:auto"}

### [!DNL Magento_SendFriend]

| Vorlage | Konfigurationspfad |
|--- |--- |
| `Send Product Link to Friend` | **Seite:** [!UICONTROL Catalog] > [[!UICONTROL Email to a Friend]](../configuration-reference/catalog/email-to-a-friend.md)<br/>**Abschnitt:** [!UICONTROL Email Templates]<br/>**Feld:** [!UICONTROL Select Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_Sitemap]

| Vorlage | Konfigurationspfad |
|--- |--- |
| `Sitemap Generation Settings` | **Seite:** [!UICONTROL Catalog] > [[!UICONTROL XML Sitemap]](../configuration-reference/catalog/xml-sitemap.md)<br/>**Abschnitt:** [!UICONTROL Generation Settings]<br/>**Feld:** [!UICONTROL Error Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_TwoFactorAuth]

| Vorlage | Konfigurationspfad |
|--- |--- |
| `2FA Configuration Required by User` | Nicht zutreffend |
| `2FA Configuration Required for the Application` | Nicht zutreffend |

{style="table-layout:auto"}

### [!DNL Magento_User]

| Vorlage | Konfigurationspfad |
|--- |--- |
| `Forgot Admin Password` | **Seite:** [!UICONTROL Advanced] > [[!UICONTROL Admin]](../configuration-reference/advanced/admin.md)<br/>**Abschnitt:** [!UICONTROL Admin User Emails]<br/>**Feld:** KennwortEmail-Vorlage vergessen |
| `User Notification` | **Seite:** [!UICONTROL Advanced] > [[!UICONTROL Admin]](../configuration-reference/advanced/admin.md)<br/>**Abschnitt:** [!UICONTROL Admin User Emails]<br/>**Feld:** Vorlage für Benutzerbenachrichtigungen |
| `New User Notification` | **Seite:** [!UICONTROL Advanced] > [[!UICONTROL Admin]](../configuration-reference/advanced/admin.md)<br/>**Abschnitt:** [!UICONTROL Admin User Emails]<br/>**Feld:** [!UICONTROL New User Notification Template] |

{style="table-layout:auto"}

### [!DNL Magento_Wishlist]

| Vorlage | Konfigurationspfad |
|--- |--- |
| `Magento Wish List Sharing` | **Seite:** [!UICONTROL Customers] > [[!UICONTROL Wish List]](../configuration-reference/customers/wishlist.md)<br/>**Abschnitt:** [!UICONTROL Share Options]<br/>**Feld:** [!UICONTROL Email Template] |

{style="table-layout:auto"}
