---
title: '[!UICONTROL Advanced] &gt; [!UICONTROL Admin]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Advanced] &gt; [!UICONTROL Admin] des Commerce Admin-Bereichs.
exl-id: 546b8d01-9611-4415-ab2b-29be560316f5
role: Admin
feature: Configuration, Admin Workspace
source-git-commit: e05d13f79ceb2fe24c1931fefb48317ebd36d1fc
workflow-type: tm+mt
source-wordcount: '1209'
ht-degree: 0%

---

# Erweitert > Admin

{{config}}

## [!UICONTROL Admin User Emails]

![Admin-Benutzer-E-Mails](./assets/admin-admin-user-emails.png)<!-- zoom -->

Weitere Informationen zum Ändern dieser Einstellungen finden Sie unter [Kennwort vergessen und E-Mail zurücksetzen](../../systems/permissions-users-all.md#forgotten-password-and-reset-emails).

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|---------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Forgot Password Email Template] | Global | Identifiziert die E-Mail-Vorlage, die für die Nachricht verwendet wird, die gesendet wird, wenn ein Administrator sein Kennwort vergisst. Standardvorlage: `Forgot Admin Password` |
| [!UICONTROL Forgot and Reset Email Sender] | Global | Identifiziert den Store-Kontakt, der als Absender der E-Mail _Kennwort vergessen_ angezeigt wird. Standardabsender: `General Contact`<br/>Andere Absenderoptionen: `Sales Representative`, `Customer Support`, `Custom Email` |
| [!UICONTROL User Notification Template] | Global | Bestimmt die E-Mail-Vorlage, die als Standard für Admin-Benachrichtigungen verwendet wird. Standardvorlage: `User Notification` |

{style="table-layout:auto"}

## [!UICONTROL Startup Page]

![Startseite](./assets/admin-startup-page.png)<!-- zoom -->

Weitere Informationen zum Ändern dieser Einstellungen finden Sie unter [Ändern der Startseite](../../getting-started/admin-dashboard.md#change-the-startup-page) im _Erste Schritte_.

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|---------------------------|------------------------------------------------------------------------|------------------------------------------------------------------|
| [!UICONTROL Startup Page] | Global | Bestimmt die Admin-Landingpage, die nach der Anmeldung angezeigt wird. |

{style="table-layout:auto"}

### [!UICONTROL Startup Page]

| Bereich |                                                                                                                                                                                                                                                                                                                                                                           | Option |
|---------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [`Dashboard`](../../getting-started/admin-dashboard.md) |                                                                                                                                                                                                                                                                                                                                                                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| `Sales` | `Operations` | [`Quotes`](../../b2b/quotes.md) ![Adobe Commerce B2B](../../assets/b2b.svg) <br/>[`Orders`](../../stores-purchase/orders.md)<br/>[`Invoices`](../../stores-purchase/invoices.md)<br/>[`Shipments`](../../stores-purchase/shipments.md)<br/>[`Credit Memos`](../../stores-purchase/credit-memos.md)<br/>[`Billing Agreements`](../../stores-purchase/paypal-billing-agreements.md)<br/>[`Returns`](../../stores-purchase/returns.md) ![Adobe Commerce](../../assets/adobe-logo.svg) </span><br/>[`Transactions`](../../stores-purchase/transactions.md)<br/>`Braintree Virtual Terminal` |
| `Catalog` | [`Inventory`](../../inventory-management/introduction.md) | [`Products`](../../catalog/products-list.md)<br/>[`Categories`](../../catalog/categories.md)<br/>[`Shared Catalog`](../../b2b/catalog-shared-create.md) ![Adobe Commerce B2B](../../assets/b2b.svg) |
| `Customers` | [`All Customers`](../../customers/customers-all.md)<br/>[`Now Online`](../../customers/now-online.md)<br/>[`Customer Groups`](../../customers/customer-groups.md)<br/>[`Segments`](../../customers/customer-segments.md) ![Adobe Commerce](../../assets/adobe-logo.svg) <br/>[`Companies`](../../b2b/account-companies.md)![Adobe Commerce B2B](../../assets/b2b.svg) |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| `Marketing` | `Promotions` | [`Catalog Price Rule`](../../merchandising-promotions/price-rules-catalog.md) <br/>[`Cart Price Rules`](../../merchandising-promotions/price-rules-cart.md)) <br/>[`Related Products Rules`](../../merchandising-promotions/product-related-rules.md) ![Adobe Commerce](../../assets/adobe-logo.svg) <br/>[`Gift Card Accounts`](../../stores-purchase/product-gift-card-accounts.md) ![Adobe Commerce](../../assets/adobe-logo.svg) |
|                                                         | [`Private Sales`](../../merchandising-promotions/events-private-sales.md) ![Adobe Commerce](../../assets/adobe-logo.svg) | [`Events`](../../merchandising-promotions/event-configure.md) <br/>[`Invitations`](../../merchandising-promotions/invitations.md) |
|                                                         | `Communications` | [`Email Templates`](../../systems/email-templates.md) <br/>[`Newsletter Template`](../../merchandising-promotions/newsletter-template.md) <br/>[`Newsletter Queue`](../../merchandising-promotions/newsletter-queue.md) <br/>[`Newsletter Subscribers`](../../merchandising-promotions/newsletter-subscribers.md) <br/>[`Email Reminders`](../../merchandising-promotions/email-reminder-rules.md) ![Adobe Commerce](../../assets/adobe-logo.svg) |
|                                                         | `SEO & Search` | [`Search Terms`](../../catalog/search-terms.md) <br/>[`Search Synonyms`](../../catalog/search-terms.md#search-synonyms) ![Adobe Commerce](../../assets/adobe-logo.svg)<br/>[`URL Rewrites`](../../merchandising-promotions/url-rewrite.md) <br/>[`Site Map`](../../merchandising-promotions/sitemap-xml.md) |
|                                                         | [`User Content`](../../catalog/settings-advanced-product-reviews.md) | [`All Reviews`](../../catalog/settings-advanced-product-reviews.md) <br/>[`Pending Reviews`](../../merchandising-promotions/product-reviews-moderate.md) <br/> |
| `Content` | `Elements` | [`Pages`](../../content-design/pages.md)<br/>[`Hierarchy`](../../content-design/page-hierarchy.md) ![Adobe Commerce](../../assets/adobe-logo.svg)<br/>[`Blocks`](../../content-design/blocks.md)<br/>[`Dynamic Blocks`](../../content-design/dynamic-blocks.md) ![Adobe Commerce](../../assets/adobe-logo.svg)<br/>[`Widgets`](../../content-design/widgets.md)<br/>[`Media Gallery`](../../content-design/media-storage.md) |
|                                                         | `Design` | [`Configuration`](../../content-design/configuration.md)<br/>[`Themes`](../../content-design/themes.md)<br/>[`Schedule`](../../content-design/schedule.md) |
|                                                         | `Content Staging` ![Adobe Commerce](../../assets/adobe-logo.svg)<br /> | [Dashboard](../../content-design/content-staging.md) |
| `Reports` | [`Marketing`](../../getting-started/marketing-reports.md) | `Products in Cart`<br />`Search Terms`<br />`Abandoned Carts`<br />`Newsletter Problem Reports` |
|                                                         | [`Reviews`](../../getting-started/review-reports.md) | `By Customer`<br/> `By Products`<br/> |
|                                                         | [`Sales`](../../getting-started/sales-reports.md) | `Orders`<br/>`Tax`<br/>`Invoiced`<br/>`Shipping`<br/>`Refunds`<br/>`Coupons`<br/>`PayPal Settlement`<br/>`Braintree Settlement` |
|                                                         | `System Insights` | [`Site-Wide Analysis Tool`](https://experienceleague.adobe.com/docs/commerce-operations/tools/site-wide-analysis-tool/access.html) ![Adobe Commerce](../../assets/adobe-logo.svg) |
|                                                         | [`Customers`](../../getting-started/customer-reports.md) | `Order Total`<br/>`Order Count`<br/>`New`<br/>`Wish Lists`<br/>`Segments`<br/> |
|                                                         | [`Products`](../../getting-started/product-reports.md) | `Views`<br/>`Bestsellers`<br/>`Low Stock`<br/>`Ordered`<br/>`Downloads` |
|                                                         | [`Private Sales`](../../getting-started/private-sales-reports.md) ![Adobe Commerce](../../assets/adobe-logo.svg) | `Invitations`<br/>`Invited Customers`<br/>`Conversions` |
|                                                         | `Statistics` | [`Refresh Statistics`](../../getting-started/sales-reports.md#refresh-statistics) |
|                                                         | [`Business Intelligence`](../../getting-started/business-intelligence.md) | `Advanced Reporting`<br/>`BI Essentials`<br/> |
|                                                         | `Customer Engagement` | `Dashboard`<br/>`Importer Status`<br/>`Automation Enrollment`<br/>`Campaign Sends`<br/>`SMS Sends`<br/>`Cron Tasks`<br/>`Log Viewer`<br/>`Abandoned Carts` |
| `Stores` | `Settings` | [`All Stores`](../../stores-purchase/stores.md)<br/>[`Configuration`](../../configuration-reference/guide-overview.md)<br/>[`Terms and Conditions`](../../stores-purchase/terms-and-conditions.md)<br/>[`Order Status`](../../stores-purchase/order-status.md) |
|                                                         | [`Inventory`](../../inventory-management/introduction.md) | [`Sources`](../../inventory-management/sources-stocks.md#sources)<br/>[`Stocks`](../../inventory-management/sources-stocks.md#stocks) |
|                                                         | [`Taxes`](../../stores-purchase/taxes.md) | [`Tax Rules`](../../stores-purchase/tax-rules.md)<br/>[`Tax Zones and Rates`](../../stores-purchase/tax-zones-rates.md) |
|                                                         | [`Currency`](../../stores-purchase/currency.md) | [`Currency Rates`](../../stores-purchase/currency-configuration.md)<br/>[`Currency Symbols`](../../stores-purchase/currency-configuration.md#step-5-customize-currency-symbols-optional) |
|                                                         | `Attributes` | [`Customer`](../../systems/data-attributes-customer.md)<br/>[`Customer Address`](../../systems/data-attributes-customer.md#customer-addresses)<br/>[`Product`](../../systems/data-attributes-product.md)<br/>[`Attribute Set`](../../catalog/attribute-sets.md)<br/>[`Returns`](../../stores-purchase/attributes-returns.md)<br/>[`Ratings`](../../merchandising-promotions/product-reviews.md#create-custom-ratings) |
|                                                         | `Other Settings` | [`Reward Exchange Rates`](../../merchandising-promotions/reward-exchange-rates.md)<br/>[`Gift Wrapping`](../../stores-purchase/cart-configuration.md#gift-wrap)<br/>[`Gift Registry`](../../merchandising-promotions/gift-registry-create.md) |
| `System` | [`Data Transfer`](../../systems/data-transfer.md) | [`Import`](../../systems/data-import.md)<br/>[`Export`](../../systems/data-export.md)<br/>[`Import/Export Tax Rates`](../../systems/data-transfer-tax-rates.md)<br/>[`Import History`](../../systems/data-import.md#import-history)<br/>[`Scheduled Import/Export`](../../systems/data-scheduled-import-export.md) |
|                                                         | `Extensions` | [`Integrations`](../../systems/integrations.md) |
|                                                         | `Tools` | [`Cache Management`](../../systems/cache-management.md)<br/>[`Index Management`](../../systems/index-management.md) |
|                                                         | `Support` | [`System Report`](../../systems/support.md#system-reports) |
|                                                         | `Permissions` | [`All Users`](../../systems/permissions-users-all.md)<br/>[`Locked Users`](../../systems/permissions-users-all.md#locked-users)<br/>[`User Roles`](../../systems/permissions-user-roles.md) |
|                                                         | `Action Log` ![Adobe Commerce](../../assets/adobe-logo.svg) | [`Report`](../../systems/action-log.md)<br/>[`Archive`](../../systems/action-log-archive.md)<br/>[`Bulk Actions`](../../systems/action-log-bulk-actions.md) |
|                                                         | `Other Settings` | [`Notifications`](../../systems/notifications.md)<br/>[`Custom Variables`](../../systems/variables-custom.md)<br/>[`Manage Encryption Key`](../../systems/encryption-key.md) |
| `Find Partners & Extensions` |                                                                                                                                                                                                                                                                                                                                                                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |

{style="table-layout:auto"}

<!-- Feature still in development 
## [!UICONTROL Unified Experience]

![Store Configuration for Unified Experience](./assets/admin-uex-configuration.png)

The [!UICONTROL Unified Experience] option is available in Adobe Commerce deployments that have the Commerce Admin Unified Experience extension loaded. This extension enables integration with Experience Cloud to streamline cross-application workflows between Commerce and other Experience Cloud solutions. See [Adobe Experience Cloud Integration for Commerce Admin](../../getting-started/admin-unified-experience-integration-overview.md).

| Field        | [Scope](../../getting-started/websites-stores-views.md#scope-settings) | Description                                                                                                                                                                                                                                                                                                                                                                    |
|--------------|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Enable       | Global                                                                 | Determines if the Commerce instance uses the Experience Cloud integration. Before enabling this feature, review the [requirements and configuration instructions](../../getting-started/admin-unified-experience-integration-overview.md). Options: Yes/No.                                                                                                                    |
| Project Name | Global                                                                 | Identifies the instance in the Experience Cloud Commerce Projects workspace when the Unified Experience is enabled. The name can contain only alphanumeric characters and spaces. Defaults to the [cloud environment name](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-architecture.html?lang=en#pro-environment-architecture). |

{style="table-layout:auto"}

-->

## [!UICONTROL Admin Base URL]

![Admin-Basis-URL](./assets/admin-admin-base-url.png)<!-- zoom -->

Weitere Informationen zum Festlegen dieser Optionen finden Sie unter [Konfigurieren der Basis](../../stores-purchase/store-urls.md#configure-the-base-url)URL im _Handbuch für Stores und Kauferlebnisse_.

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|------------------------------------|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Use Custom Admin URL] | Global | Bestimmt, ob eine benutzerdefinierte URL für den Zugriff auf den Admin verwendet wird. Optionen: `Yes` / `No` |
| [!UICONTROL Custom Admin URL] | Global | Gibt eine benutzerdefinierte URL für den Zugriff auf den Admin an. Standardmäßig entspricht die Admin-URL der Basis-URL.<br/>**Wichtig:** Die Admin-URL muss sich in derselben Commerce-Installation befinden und denselben Dokumentstamm wie die Storefront haben. |
| [!UICONTROL Use Custom Admin Path] | Global | Bestimmt, ob ein benutzerdefinierter Pfad verwendet wird, um auf den Administrator zuzugreifen. Der Standardpfad lautet `admin`. Optionen: `Yes` / `No` |
| [!UICONTROL Custom Admin Path] | Global | Ändert den Namen des standardmäßigen Administratorpfads in etwas, das schwer zu erraten ist. Geben Sie den benutzerdefinierten Pfadnamen in Kleinbuchstaben ein. Beispiel: `aardvark` |

{style="table-layout:auto"}

## [!UICONTROL Security]

![Sicherheit](./assets/admin-security.png)<!-- zoom -->

Weitere Informationen zum Festlegen dieser Optionen finden Sie unter [Konfigurieren der Admin](../../systems/security-admin.md) im _Handbuch für Admin-Systeme_.

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Admin Account Sharing] | Shop-Ansicht | Bestimmt, ob ein Administrator-Benutzer von verschiedenen Geräten gleichzeitig beim selben Konto angemeldet werden kann. Optionen: <br/>**`Yes`**- Ermöglicht mehrere aktive Sitzungen vom selben Administratorkonto aus.<br/>**`No`** - Erlaubt nur eine aktive Sitzung pro Admin-Konto. |
| [!UICONTROL Password Reset Protection Type] | Shop-Ansicht | Bestimmt die Methode, die zum Verwalten von Anfragen zum Zurücksetzen von Passwörtern verwendet wird. Optionen: <br/>**`By IP and Email`**- Das Kennwort kann online zurückgesetzt werden, nachdem eine Antwort von der Benachrichtigung an die mit dem Admin-Konto verknüpfte E-Mail-Adresse gesendet wurde.<br/>**`By IP`** - Das Passwort kann online ohne zusätzliche Bestätigung zurückgesetzt werden. <br/>**`By Email`**- Das Kennwort kann nur zurückgesetzt werden, indem per E-Mail auf die Benachrichtigung geantwortet wird, die an die mit dem Admin-Konto verknüpfte E-Mail-Adresse gesendet wird.<br/>**`None`** - Das Kennwort kann nur vom Store-Administrator zurückgesetzt werden. |
| [!UICONTROL Recovery Link Expiration Period (hours)] | Global | Bestimmt, wie viele Stunden ein Link zur Passwortwiederherstellung gültig bleibt. |
| [!UICONTROL Max Number of Password Reset Requests] | Shop-Ansicht | Bestimmt die maximale Anzahl von Passwortanfragen, die pro Stunde gesendet werden können. |
| [!UICONTROL Min Time Between Password Reset Requests] | Shop-Ansicht | Bestimmt die Mindestanzahl von Minuten zwischen den Anforderungen zum Zurücksetzen des Kennworts. |
| [!UICONTROL Add Secret Key to URLs] | Global | Wenn diese Option aktiviert ist, wird zur Vorbeugung gegen Exploits ein geheimer Schlüssel an die Admin-URL angehängt. Optionen: `Yes` / `No` |
| [!UICONTROL Login Is Case Sensitive] | Global | Bestimmt, ob die von einem Benutzer eingegebenen Anmeldedaten mit den gespeicherten übereinstimmen müssen. Optionen: `Yes` / `No` |
| [!UICONTROL Admin Session Lifetime (seconds)] | Global | Bestimmt die Länge einer Admin-Sitzung in Sekunden. |
| [!UICONTROL Maximum Login Failures to Lockout Account] | Global | Bestimmt, wie oft sich Admin-Benutzer anmelden können, bevor ihre Konten gesperrt werden. Wenn das Feld leer ist, wird kein Minimum festgelegt. Standardwert: `6` |
| [!UICONTROL Lockout Time (minutes)] | Global | Bestimmt die Anzahl der Minuten, die ein Admin-Konto gesperrt ist, bevor der Benutzer erneut versuchen kann, sich anzumelden. Standardwert: `30` |
| [!UICONTROL Password Lifetime (days)] | Global | Bestimmt die Anzahl der Tage bis zum Ablauf eines Administratorkennworts. Wenn das Feld leer ist, wird keine Lebensdauer festgelegt. Standardwert: `90` |
| [!UICONTROL Password Change] | Global | Legt fest, ob Admin-Benutzer ihre Kennwörter ändern müssen. Optionen: <br/>**`Forced`**- Erfordert, dass Admin-Benutzer ihr Passwort ändern, nachdem das Konto eingerichtet wurde.<br/>**`Recommended`** - empfiehlt, dass Admin-Benutzer ihr Passwort ändern, nachdem das Konto eingerichtet wurde. |

{style="table-layout:auto"}

## [!UICONTROL Dashboard]

![Dashboard](./assets/admin-dashboard.png)<!-- zoom -->

Weitere Informationen zum Festlegen dieser Optionen finden Sie unter [Admin-](../../getting-started/admin-dashboard.md)) im _Erste Schritte_.

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|----------------------------|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Charts] | Global | Bestimmt, ob das Dashboard ein Diagramm enthält, das aus aktuellen Verkaufsdaten generiert wurde. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Admin Grids]

![Admin-Raster](./assets/admin-admin-grids.png)<!-- zoom -->

Weitere Informationen zum Festlegen dieser Optionen finden Sie unter [Begrenzen der ](../../catalog/products-list.md#limit-product-display)) im _Handbuch zur Katalogverwaltung_.

>[!NOTE]
>
>Um die Leistung großer Kataloge zu verbessern, wird empfohlen, die Anzahl der im Raster angezeigten Produkte zu begrenzen.

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|-----------------------------------------------|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Limit Number of Products in Grid] | Global | Bestimmt, ob die Anzahl der im Raster angezeigten Produkte auf den _[!UICONTROL Records Limit]_Wert beschränkt ist. Optionen: `Yes` / `No` |
| [!UICONTROL Records Limit] | Global | Legt die maximale Anzahl von Produkten im Produktraster fest. Der standardmäßige Mindestwert ist `20000`. |

## [!UICONTROL CAPTCHA]

![CAPTCHA](./assets/admin-captcha.png)<!-- zoom -->

Weitere Informationen zum Festlegen dieser Optionen finden Sie unter [CAPTCHA](../../systems/security-captcha.md) im _Admin-_.

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|-------------------------------------------------------|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable CAPTCHA in Admin] | Global | Aktiviert CAPTCHA für die Administratoranmeldung. Optionen: `Yes` / `No` |
| [!UICONTROL Font] | Global | Bestimmt die Schriftart, die für die Anzeige von CAPTCHA verwendet wird. Um Ihre eigene Schriftart hinzuzufügen, legen Sie die Schriftartdatei im selben Verzeichnis wie die Commerce-Instanz ab und fügen Sie die Deklaration zur Datei config.xml unter `app/code/Magento/Captcha/etc` Standardschriftart hinzu:` LinLibertine` |
| [!UICONTROL Forms] | Global | Bestimmt die Formulare, in denen CAPTCHA verwendet wird. Optionen: `Admin Login` / `Admin Forgot Password` |
| [!UICONTROL Displaying Mode] | Global | Bestimmt, wann das CAPTCHA angezeigt wird. Optionen: <br/>**`Always`**- CAPTCHA ist immer für die Anmeldung erforderlich.<br/>**`After number of attempts to login`** - Zeigt das [!UICONTROL Number of Unsuccessful Attempts to Login] an. Geben Sie die Anzahl der zulässigen Anmeldeversuche ein. Der Wert 0 (Null) entspricht der Einstellung des Anzeigemodus auf „Immer“. Diese Option gilt nicht für die Formulare „Kennwort vergessen“ und „Benutzer erstellen“. Wenn CAPTCHA aktiviert und so eingestellt ist, dass es angezeigt wird, ist es immer im Formular enthalten.<br />**Hinweis**: Um die Anzahl erfolgloser Anmeldeversuche zu verfolgen, wird jeder Anmeldeversuch unter einer E-Mail-Adresse und von einer IP-Adresse gezählt. Die maximale Anzahl von Anmeldeversuchen, die von derselben IP-Adresse aus zulässig sind, beträgt 1.000. Diese Einschränkung gilt nur, wenn CAPTCHA aktiviert ist. |
| [!UICONTROL Number of Unsuccessful Attempts to Login] | Global | Bestimmt, wie oft eine Person versuchen kann, sich anzumelden, bevor das Konto gesperrt wird. Um die Anzahl erfolgloser Anmeldeversuche zu verfolgen, verfolgt das System die Versuche von einer einzelnen E-Mail-Adresse aus einer einzelnen IP-Adresse. Die maximal zulässige Anzahl von Versuchen von derselben IP-Adresse ist 1.000. Diese Einschränkung gilt nur, wenn CAPTCHA aktiviert ist. |
| [!UICONTROL CAPTCHA Timeout (minutes)] | Global | Bestimmt die Lebensdauer des aktuellen CAPTCHA. Wenn das CAPTCHA abläuft, muss der Benutzer die Seite neu laden. |
| [!UICONTROL Number of Symbols] | Global | Bestimmt die Anzahl der im CAPTCHA verwendeten Symbole. Der maximal zulässige Wert ist `8`. Sie können auch einen Bereich angeben, z. B. `5-8`. |
| [!UICONTROL Symbols Used in CAPTCHA] | Global | Bestimmt, welche Symbole im CAPTCHA verwendet werden. Nur Buchstaben (a-z und A-Z) und Zahlen (0-9) sind zulässig. Der Standardsatz von Symbolen, die im Feld vorgeschlagen werden, schließt ähnlich aussehende Symbole wie i, l oder 1 aus. Die Anzeige dieser Symbole in CAPTCHA verringert die Wahrscheinlichkeit, dass ein Benutzer CAPTCHA korrekt erkennt. |
| [!UICONTROL Case Sensitive] | Global | Bestimmt, ob bei den im CAPTCHA verwendeten Zeichen zwischen Groß- und Kleinschreibung unterschieden wird. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Admin Actions Logging]

{{ee-feature}}

![Admin-Aktionsprotokollierung](./assets/admin-actions-logging.png)<!-- zoom -->

Weitere Informationen zum Festlegen dieser Optionen finden Sie unter [Aktionsprotokollarchiv](../../systems/action-log-archive.md) im _Admin-_.

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|-----------------------------|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Actions] | Global | Aktiviert die Aktionsprotokollierung für jede der ausgewählten Aktionen: <br/>`Admin My Account` <br/>`Admin Permission Roles` <br/>`Admin Permission Users` <br/>`Admin Sign In` <br/>`CMS Hierarchy` <br/>`Cache Management` <br/>`Catalog Ratings` <br/>`CMS Blocks` <br/>`CMS Pages` <br/>`Cart Price Rules` <br/>`Catalog Attributes` <br/>`Catalog Categories` <br/>`Catalog Events` <br/>`Catalog Price Rules` <br/>`Catalog Product Tax Classes` <br/>`Catalog Product Templates` <br/>`Catalog Products` <br/>`Catalog Reviews` <br/>`Catalog Search` <br/>`Checkout Terms and Conditions` <br/>`Companies` <br/>`Company Credit` <br/>`Custom Variables` <br/>`Customer Groups` <br/>`Customer Invitations` <br/>`Customer Tax Classes` <br/>`Customers` <br/>`Design Configuration` <br/>`Gift Card Accounts` <br/>`Gift Registry Entity` <br/>`Gift Registry Type` <br/>`Index Management` <br/>`Login as a Customer` <br/>`Manage Currency Rates` <br/>`Manage Customer Address Attributes` <br/>`Manage Customer Attributes` <br/>`Manage Design` <br/>`Manage Dynamic Blocks` <br/>`Manage Segments` <br/>`Manage Store Views` <br/>`Manage Stores` <br/>`Manage Websites` <br/>`Negotiable Quotes` <br/>`Newsletter Queue` <br/>`Newsletter Subscribers` <br/>`Newsletter Templates` <br/>`PayPal Settlement Reports` <br/>`Reports` <br/> `Reward Points Rates` <br/>`Rule-Based Product Relations` <br/>`Sales Archive` <br/>`Sales Credit Memos` <br/>`Sales Invoices` <br/>`Sales Order Status` <br/>`Sales Orders` <br/>`Sales Shipments` <br/>`Shared Catalog` <br/>`Shopping Cart Management` <br/>`Store Credit` <br/>`System Backups` <br/>`System Configuration` <br/>`Tax Rates` <br/>`Tax Rules` <br/>`Transactional Emails` <br/>`URL Rewrites` <br/>`Widget` <br/>`XML Sitemap` |

{style="table-layout:auto"}

## [!UICONTROL Admin Usage]

![Admin-Nutzung](./assets/admin-usage.png)<!-- zoom -->

Weitere Informationen zum Festlegen dieser Optionen finden Sie unter [Nutzungsdatenerfassung](../../getting-started/admin.md#usage-data-collection) im _Erste Schritte_.

| Feld | Umfang | Beschreibung |
|------------------------------------------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Admin Usage Tracking] | Global | Erteilt Adobe die Berechtigung, Admin-Nutzungsdaten zu erfassen, um das Erlebnis bei der Verwendung von _Admin_ und zugehörigen Produkten und Services zu verbessern. Durch die Datenerfassung wird auch _Produktinterne Anleitung_ ermöglicht, die interaktive Inhalte wie Hilfe, QuickInfos, Anleitungen zu schrittweisen Anleitungen, Onboarding-Informationen, Funktionsankündigungen und mehr für den _Administrator_ bereitstellt. Einzelne Admins werden in den Nutzungsdaten nicht angegeben. Optionen: <br />**`Yes`**- Ermöglicht die Datenerfassung und aktiviert _Produktinterne Anleitung_.<br />**`No`** - Ermöglicht keine Datenerfassung und aktiviert _Produktinterne Anleitung_. |

{style="table-layout:auto"}
