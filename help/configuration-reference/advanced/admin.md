---
title: '[!UICONTROL Advanced] &gt; [!UICONTROL Admin]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Advanced] &gt; [!UICONTROL Admin] des Commerce-Administrators.
exl-id: 546b8d01-9611-4415-ab2b-29be560316f5
role: Admin
feature: Configuration, Admin Workspace
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1209'
ht-degree: 0%

---

# Erweitert > Admin

{{config}}

## [!UICONTROL Admin User Emails]

![Admin-Benutzer-E-Mails](./assets/admin-admin-user-emails.png)<!-- zoom -->

Weitere Informationen zum Ändern dieser Einstellungen finden Sie unter [Vergessenes Kennwort und Zurücksetzen der E-Mail](../../systems/permissions-users-all.md#forgotten-password-and-reset-emails).

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|---------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Forgot Password Email Template] | Global | Identifiziert die E-Mail-Vorlage, die für die Nachricht verwendet wird, die gesendet wird, wenn ein Administrator sein Kennwort vergisst. Standardvorlage: `Forgot Admin Password` |
| [!UICONTROL Forgot and Reset Email Sender] | Global | Identifiziert den Store-Kontakt, der als Absender der E-Mail &quot;_Kennwort vergessen_&quot;angezeigt wird. Standardsender: `General Contact`<br/>Sonstige Absenderoptionen: `Sales Representative`, `Customer Support`, `Custom Email` |
| [!UICONTROL User Notification Template] | Global | Legt die E-Mail-Vorlage fest, die als Standard für Admin-Benachrichtigungen verwendet wird. Standardvorlage: `User Notification` |

{style="table-layout:auto"}

## [!UICONTROL Startup Page]

![Startseite](./assets/admin-startup-page.png)<!-- zoom -->

Weitere Informationen zum Ändern dieser Einstellungen finden Sie unter [Ändern der Startseite](../../getting-started/admin-dashboard.md#change-the-startup-page) im _Erste Schritte-Handbuch_.

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|---------------------------|------------------------------------------------------------------------|------------------------------------------------------------------|
| [!UICONTROL Startup Page] | Global | Legt die Admin-Landingpage fest, die nach der Anmeldung angezeigt wird. |

{style="table-layout:auto"}

### [!UICONTROL Startup Page] Optionen

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
|                                                         | `Support` | [`Data Collector`](../../systems/support.md#data-collector)<br/>[`System Report`](../../systems/support.md#system-reports) |
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

![ Basis-Admin-URL](./assets/admin-admin-base-url.png)<!-- zoom -->

Weitere Informationen zum Festlegen dieser Optionen finden Sie unter [Konfigurieren der Basis-URL](../../stores-purchase/store-urls.md#configure-the-base-url) im Handbuch _Stores and Purchase Experience Guide_.

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|------------------------------------|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Use Custom Admin URL] | Global | Bestimmt, ob für den Zugriff auf den Admin eine benutzerdefinierte URL verwendet wird. Optionen: `Yes` / `No` |
| [!UICONTROL Custom Admin URL] | Global | Gibt eine benutzerdefinierte URL für den Zugriff auf den Admin an. Standardmäßig ist die Admin-URL mit der Basis-URL identisch.<br/>**Wichtig:** Die Admin-URL muss sich in derselben Commerce-Installation befinden und denselben Dokumentenstamm wie die Storefront aufweisen. |
| [!UICONTROL Use Custom Admin Path] | Global | Bestimmt, ob für den Zugriff auf den Admin ein benutzerdefinierter Pfad verwendet wird. Der Standardpfad lautet `admin`. Optionen: `Yes` / `No` |
| [!UICONTROL Custom Admin Path] | Global | Ändert den Namen des standardmäßigen Admin-Pfads in etwas, das schwer zu erraten ist. Geben Sie den benutzerdefinierten Pfadnamen in Kleinbuchstaben ein. Beispiel: `aardvark` |

{style="table-layout:auto"}

## [!UICONTROL Security]

![Sicherheit](./assets/admin-security.png)<!-- zoom -->

Weitere Informationen zum Festlegen dieser Optionen finden Sie unter [Konfigurieren der Administrator-Sicherheit](../../systems/security-admin.md) im _Administratorsystemhandbuch_.

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Admin Account Sharing] | Store-Ansicht | Bestimmt, ob ein Admin-Benutzer von verschiedenen Geräten gleichzeitig bei demselben Konto angemeldet werden kann. Optionen: <br/>**`Yes`**- Ermöglicht mehrere aktive Sitzungen desselben Administratorkontos.<br/>**`No`** - Ermöglicht nur eine aktive Sitzung pro Administratorkonto. |
| [!UICONTROL Password Reset Protection Type] | Store-Ansicht | Bestimmt die Methode, die zum Verwalten von Anforderungen zum Zurücksetzen von Passwörtern verwendet wird. Optionen: <br/>**`By IP and Email`**- Das Kennwort kann online zurückgesetzt werden, nachdem eine Antwort von der Benachrichtigung empfangen und an die mit dem Admin-Konto verknüpfte E-Mail-Adresse gesendet wurde.<br/>**`By IP`** - Das Kennwort kann ohne zusätzliche Bestätigung online zurückgesetzt werden. <br/>**`By Email`**- Das Kennwort kann nur zurückgesetzt werden, indem eine E-Mail-Benachrichtigung an die mit dem Admin-Konto verknüpfte E-Mail-Adresse gesendet wird.<br/>**`None`** - Das Kennwort kann nur vom Store-Administrator zurückgesetzt werden. |
| [!UICONTROL Recovery Link Expiration Period (hours)] | Global | Bestimmt die Anzahl der Stunden, in denen ein Link zur Passwortwiederherstellung gültig bleibt. |
| [!UICONTROL Max Number of Password Reset Requests] | Store-Ansicht | Bestimmt die maximale Anzahl von Kennwortanfragen, die pro Stunde gesendet werden können. |
| [!UICONTROL Min Time Between Password Reset Requests] | Store-Ansicht | Bestimmt die Mindestanzahl von Minuten zwischen Anforderungen zum Zurücksetzen des Kennworts. |
| [!UICONTROL Add Secret Key to URLs] | Global | Wenn diese Option aktiviert ist, hängt als Vorsichtsmaßnahme gegen Exploits ein geheimer Schlüssel an die Admin-URL an. Optionen: `Yes` / `No` |
| [!UICONTROL Login Is Case Sensitive] | Global | Bestimmt, ob die von einem Benutzer eingegebenen Anmeldedaten mit der Groß-/Kleinschreibung der gespeicherten Anmeldedaten übereinstimmen müssen. Optionen: `Yes` / `No` |
| [!UICONTROL Admin Session Lifetime (seconds)] | Global | Bestimmt die Dauer einer Admin-Sitzung in Sekunden. |
| [!UICONTROL Maximum Login Failures to Lockout Account] | Global | Bestimmt, wie oft Admin-Benutzer versuchen können, sich anzumelden, bevor ihre Konten gesperrt werden. Wenn das Feld leer ist, wird kein Minimum festgelegt. Standardwert: `6` |
| [!UICONTROL Lockout Time (minutes)] | Global | Bestimmt die Anzahl der Minuten, in denen ein Admin-Konto gesperrt ist, bevor der Benutzer versuchen kann, sich erneut anzumelden. Standardwert: `30` |
| [!UICONTROL Password Lifetime (days)] | Global | Bestimmt die Anzahl der Tage, bevor ein Admin-Kennwort abläuft. Wenn das Feld leer ist, wird keine Lebensdauer festgelegt. Standardwert: `90` |
| [!UICONTROL Password Change] | Global | Bestimmt, ob Admin-Benutzer ihre Kennwörter ändern müssen. Optionen: <br/>**`Forced`**- Erfordert, dass Admin-Benutzer ihr Passwort ändern, nachdem das Konto eingerichtet wurde.<br/>**`Recommended`** - Empfiehlt Admin-Benutzern, ihr Passwort zu ändern, nachdem das Konto eingerichtet wurde. |

{style="table-layout:auto"}

## [!UICONTROL Dashboard]

![Dashboard](./assets/admin-dashboard.png)<!-- zoom -->

Weitere Informationen zum Festlegen dieser Optionen finden Sie unter [Admin-Dashboard](../../getting-started/admin-dashboard.md) im _Erste Schritte-Handbuch_.

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|----------------------------|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Charts] | Global | Bestimmt, ob das Dashboard ein Diagramm enthält, das aus aktuellen Verkaufsdaten generiert wurde. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Admin Grids]

![Admin-Raster](./assets/admin-admin-grids.png)<!-- zoom -->

Weitere Informationen zum Festlegen dieser Optionen finden Sie unter [Beschränken der Produktanzeige](../../catalog/products-list.md#limit-product-display) im _Catalog Management Guide_.

>[!NOTE]
>
>Um die Leistung bei großen Katalogen zu verbessern, wird empfohlen, die Anzahl der im Raster angezeigten Produkte zu begrenzen.

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|-----------------------------------------------|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Limit Number of Products in Grid] | Global | Bestimmt, ob die Anzahl der im Raster angezeigten Produkte auf den Wert _[!UICONTROL Records Limit]_beschränkt ist. Optionen: `Yes` / `No` |
| [!UICONTROL Records Limit] | Global | Legt die Anzahl der Produkte im Produktraster fest. Der Standardwert für den Mindestwert ist `20000`. |

## [!UICONTROL CAPTCHA]

![CAPTCHA](./assets/admin-captcha.png)<!-- zoom -->

Weitere Informationen zum Festlegen dieser Optionen finden Sie unter [CAPTCHA](../../systems/security-captcha.md) im _Administratorsystemhandbuch_.

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|-------------------------------------------------------|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable CAPTCHA in Admin] | Global | Aktiviert CAPTCHA für die Administratoranmeldung. Optionen: `Yes` / `No` |
| [!UICONTROL Font] | Global | Legt die Schriftart fest, die zum Anzeigen des CAPTCHA verwendet wird. Um eine eigene Schriftart hinzuzufügen, legen Sie die Schriftartdatei im selben Ordner ab wie die Commerce-Instanz und fügen Sie die Deklaration zur Datei &quot;config.xml&quot;unter `app/code/Magento/Captcha/etc` Standardschriftart:` LinLibertine` hinzu. |
| [!UICONTROL Forms] | Global | Bestimmt die Formulare, in denen CAPTCHA verwendet wird. Optionen: `Admin Login` / `Admin Forgot Password` |
| [!UICONTROL Displaying Mode] | Global | Bestimmt, wann das CAPTCHA angezeigt wird. Optionen: <br/>**`Always`**- CAPTCHA ist für die Anmeldung immer erforderlich.<br/>**`After number of attempts to login`** - Zeigt das Feld [!UICONTROL Number of Unsuccessful Attempts to Login] an. Geben Sie die zulässige Anzahl von Anmeldeversuchen an. Der Wert 0 (null) ähnelt der Einstellung des Anzeigemodus auf Immer . Diese Option umfasst nicht die Formulare &quot;Kennwort vergessen&quot;und &quot;Benutzer erstellen&quot;. Wenn CAPTCHA aktiviert ist und für die Anzeige festgelegt ist, wird es immer in das Formular aufgenommen.<br />**Hinweis**: Um die Anzahl der fehlgeschlagenen Anmeldeversuche zu verfolgen, wird jeder Versuch, sich unter einer E-Mail-Adresse und von einer IP-Adresse aus anzumelden, gezählt. Die maximal zulässige Anzahl von Anmeldeversuchen für dieselbe IP-Adresse beträgt 1.000. Diese Einschränkung gilt nur, wenn CAPTCHA aktiviert ist. |
| [!UICONTROL Number of Unsuccessful Attempts to Login] | Global | Bestimmt, wie oft eine Person versuchen kann, sich anzumelden, bevor das Konto gesperrt wird. Um die Anzahl der fehlgeschlagenen Anmeldeversuche zu verfolgen, verfolgt das System die Versuche einer E-Mail-Adresse aus einer einzelnen IP-Adresse. Die maximal zulässige Anzahl von Versuchen derselben IP-Adresse beträgt 1.000. Diese Einschränkung gilt nur, wenn CAPTCHA aktiviert ist. |
| [!UICONTROL CAPTCHA Timeout (minutes)] | Global | Bestimmt die Lebensdauer des aktuellen CAPTCHA. Wenn das CAPTCHA abläuft, muss der Benutzer die Seite neu laden. |
| [!UICONTROL Number of Symbols] | Global | Bestimmt die Anzahl der in CAPTCHA verwendeten Symbole. Der maximal zulässige Wert ist `8`. Sie können auch einen Bereich angeben, z. B. `5-8`. |
| [!UICONTROL Symbols Used in CAPTCHA] | Global | Bestimmt, welche Symbole in CAPTCHA verwendet werden. Nur Buchstaben (a-z und A-Z) und Zahlen (0-9) sind zulässig. Der Standardsatz der im Feld vorgeschlagenen Symbole schließt ähnliche Symbole wie i, l oder 1 aus. Die Anzeige dieser Symbole in CAPTCHA verringert die Wahrscheinlichkeit, dass ein Benutzer CAPTCHA richtig erkennt. |
| [!UICONTROL Case Sensitive] | Global | Bestimmt, ob bei den im CAPTCHA verwendeten Zeichen die Groß-/Kleinschreibung beachtet wird. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Admin Actions Logging]

{{ee-feature}}

![Protokollierung von Admin-Aktionen](./assets/admin-actions-logging.png)<!-- zoom -->

Weitere Informationen zum Festlegen dieser Optionen finden Sie unter [Archiv für das Aktionsprotokoll](../../systems/action-log-archive.md) im _Handbuch für Admin-Systeme_.

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|-----------------------------|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Actions] | Global | Aktiviert die Aktionsprotokollierung für jede der ausgewählten Aktionen: <br/>`Admin My Account` <br/>`Admin Permission Roles` <br/>`Admin Permission Users` <br/>`Admin Sign In` <br/>`CMS Blocks` <br/>`CMS Hierarchy` <br/>`CMS Pages` <br/>`Cache Management` <br/>`Cart Price Rules` <br/>`Catalog Attributes` <br/>`Catalog Categories` <br/>`Catalog Events` <br/>`Catalog Price Rules` <br/>`Catalog Product Tax Classes` <br/>`Catalog Product Templates` <br/>`Catalog Products` <br/>`Catalog Ratings` <br/>`Catalog Reviews` <br/>`Catalog Search` <br/>`Checkout Terms and Conditions` <br/>`Companies` <br/>`Company Credit` <br/>`Custom Variables` <br/>`Customer Groups` <br/>`Customer Invitations` <br/>`Customer Tax Classes` <br/>`Customers` <br/>`Design Configuration` <br/>`Gift Card Accounts` <br/>`Gift Registry Entity` <br/>`Gift Registry Type` <br/>`Index Management` <br/>`Login as a Customer` <br/>`Manage Currency Rates` <br/>`Manage Customer Address Attributes` <br/>`Manage Customer Attributes` <br/>`Manage Design` <br/>`Manage Dynamic Blocks` <br/>`Manage Segments` <br/>`Manage Store Views` <br/>`Manage Stores` <br/>`Manage Websites` <br/>`Negotiable Quotes` <br/>`Newsletter Queue` <br/>`Newsletter Subscribers` <br/>`Newsletter Templates` <br/>`PayPal Settlement Reports` <br/>`Reports` <br/> `Reward Points Rates` <br/>`Rule-Based Product Relations` <br/>`Sales Archive` <br/>`Sales Credit Memos` <br/>`Sales Invoices` <br/>`Sales Order Status` <br/>`Sales Orders` <br/>`Sales Shipments` <br/>`Shared Catalog` <br/>`Shopping Cart Management` <br/>`Store Credit` <br/>`System Backups` <br/>`System Configuration` <br/>`Tax Rates` <br/>`Tax Rules` <br/>`Transactional Emails` <br/>`URL Rewrites` <br/>`Widget` <br/>`XML Sitemap` |

{style="table-layout:auto"}

## [!UICONTROL Admin Usage]

![Nutzung der Administratoren](./assets/admin-usage.png)<!-- zoom -->

Weitere Informationen zum Festlegen dieser Optionen finden Sie unter [Datenerfassung über die Nutzung](../../getting-started/admin.md#usage-data-collection) im _Erste Schritte-Handbuch_.

| Feld | Anwendungsbereich | Beschreibung |
|------------------------------------------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Admin Usage Tracking] | Global | Ermöglicht Adobe die Erfassung von Admin-Nutzungsdaten, um die Nutzung von _Admin_ und zugehörigen Produkten und Diensten zu verbessern. Die Datenkollektion ermöglicht auch die _In-Product Guidance_ , die interaktive Inhalte wie Hilfe, QuickInfos, schrittweise Anleitungen, Onboarding-Informationen, Funktionsankündigungen und mehr an den _Administrator_ weiterleitet. Einzelne Administratoren werden in den Nutzungsdaten nicht identifiziert. Optionen:<br />**`Yes`**- Ermöglicht die Datenerfassung und aktiviert die _In-Product Guidance_.<br />**`No`** - Ermöglicht weder die Datenerfassung noch die _In-Product Guidance_. |

{style="table-layout:auto"}
