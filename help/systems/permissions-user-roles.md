---
title: Benutzerrollen
description: Erfahren Sie, wie Sie Benutzerrollen und die zugehörigen Berechtigungen erstellen, um den Zugriff auf Administratorfunktionen zu verwalten.
exl-id: a70f74d4-72b4-4639-a67d-9fc13df65924
feature: Admin Workspace, Roles/Permissions, Security
source-git-commit: dff29b7c3a95d4a0ae5ce16819c41a4560b477c4
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 0%

---

# Benutzerrollen

Um jemandem eingeschränkten Zugriff auf den Administrator zu gewähren, muss zunächst eine Rolle mit den entsprechenden Berechtigungen erstellt werden. Nachdem die Rolle gespeichert wurde, können Sie neue Benutzer hinzufügen und ihnen die eingeschränkte Rolle zuweisen, um ihnen eingeschränkten Zugriff auf den Admin zu gewähren.

![Admin - User Roles](./assets/permissions-role-grid.png){width="600" zoomable="yes"}

## Definieren einer Rolle

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**.

1. Klicken Sie oben rechts auf **[!UICONTROL Add New Role]**.

1. Führen Sie die Schritte aus, um die Rolle zu definieren:

### Schritt 1: Rollennamen hinzufügen

1. Geben Sie unter _[!UICONTROL Role Information]_&#x200B;einen beschreibenden **[!UICONTROL Role Name]**&#x200B;ein.

1. Geben Sie unter _[!UICONTROL Current User Identity Verification]_&#x200B;Ihr Kennwort ein.

   ![Systemberechtigungen - Rolleninformationen](./assets/permissions-role-info.png){width="600" zoomable="yes"}

### Schritt 2: Ressourcen zuweisen

>[!IMPORTANT]
>
>Stellen Sie bei der Zuweisung von Ressourcen sicher, dass Sie den Zugriff auf das Berechtigungs-Tool deaktivieren, wenn Sie den Zugriff für eine bestimmte Rolle einschränken. Andernfalls können Benutzende ihre eigenen Berechtigungen ändern.

1. Legen Sie **[!UICONTROL Role Scopes]** auf eine der folgenden Einstellungen fest:

   - `All`
   - `Custom`

   Wenn für eine Multisite-Installation `Custom` festgelegt ist, aktivieren Sie das Kontrollkästchen der Website und speichern Sie, wo die Rolle verwendet werden soll.

   ![Benutzerrollenressourcen - Benutzerdefinierter Umfang](./assets/permissions-role-scope-custom.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Benutzer mit einem `Custom` Rollenbereich können keine Websites und Kategorien erstellen, Produkte Kategorien zuweisen oder Produkte _[!UICONTROL All Store Views]_&#x200B;Bereich bearbeiten, wenn sie eingeschränkten Stores zugewiesen sind. Diese Benutzenden können auch keine anderen_ globalen _Aktionen ausführen, die Bereiche betreffen, auf die sie keinen Zugriff haben.

1. Legen Sie unter _[!UICONTROL Roles Resources]_&#x200B;**[!UICONTROL Resource Access]**&#x200B;auf `Custom` fest.

   >[!NOTE]
   >
   >Wenn für die Anmeldung beim Administrator eine Zwei-Faktor-Authentifizierung (2FA) erforderlich ist, stellen Sie sicher, dass Sie für diese Rolle die `Permissions` Ressource > `Two Factor Auth` aktivieren. Andernfalls können neu erstellte Benutzer mit diesem `Custom` Rollenbereich 2FA nicht einrichten, wenn sie zum ersten Mal auf Admin zugreifen.

1. Aktivieren Sie in der **[!UICONTROL Resource]** das Kontrollkästchen jeder Admin-Funktion, auf die die Rolle zugreifen kann.

   Um eine Administratorrolle mit Zugriff auf Steuereinstellungen zu erstellen, wählen Sie sowohl die Ressourcen „Umsatz/Steuer“ als auch „System/Steuer“ aus. Wenn Sie eine Website für eine Region einrichten, die sich von Ihrem standardmäßigen [Versand-Ausgangspunkt](../stores-purchase/shipping-settings.md#point-of-origin) unterscheidet, müssen Sie den Zugriff auf das System/die Versandressourcen für die Rolle zulassen. Die Versandeinstellungen bestimmen den Store-Steuersatz, der für Katalogpreise verwendet wird.

   ![Ressourcen für zugewiesene Benutzerrollen](./assets/permissions-role-resources-product.png){width="600" zoomable="yes"}

   Die Liste der verfügbaren Berechtigungen kann zusätzliche Optionen für gebündelte und installierte Erweiterungen enthalten. Durch Auswahl der Berechtigung, die für jede Funktion am höchsten ist, weisen Sie alle für den Benutzer verfügbaren Berechtigungen zu.

   >[!NOTE]
   >
   >Ein Administrator bzw. eine Administratorin muss über **[!UICONTROL Sales / Archive]** Berechtigungen für den Rollenbereich verfügen, um die _[!UICONTROL Invoices]_,_[!UICONTROL Credit Memos]_ und _[!UICONTROL Shipments]_&#x200B;Reihenfolge ([) &#x200B;](../stores-purchase/order-processing.md).

1. Klicken Sie abschließend auf **[!UICONTROL Save Role]**.

   Die Rolle wird jetzt im Raster angezeigt und kann Benutzerkonten zugewiesen werden.

## Zuweisen einer Rolle zu Benutzern

1. Öffnen Sie den Datensatz im _[!UICONTROL Roles]_&#x200B;im Bearbeitungsmodus.

1. Geben Sie unter _[!UICONTROL Current User Identity Verification]_&#x200B;Ihr Benutzerkonto-Kennwort ein.

1. Wählen Sie im linken Bedienfeld **[!UICONTROL Role Users]** aus.

   Die Option _[!UICONTROL Role Users]_&#x200B;wird erst nach dem Speichern einer neuen Rolle angezeigt.

   ![Benutzerkonten, die der Rolle zugewiesen sind](./assets/permissions-role-users.png){width="600" zoomable="yes"}

1. Gehen Sie wie folgt vor, um nach einem bestimmten Benutzerdatensatz zu suchen:

   - Geben Sie den Wert im Suchfilter oben in einer Spalte ein und drücken Sie die **Eingabetaste**.

   - Wenn Sie bereit sind, zur vollständigen Liste zurückzukehren, klicken Sie **[!UICONTROL Reset Filter]**.

1. Aktivieren Sie das Kontrollkästchen aller Benutzer, die der Rolle zugewiesen werden sollen.

1. Klicken Sie auf **[!UICONTROL Save Role]**.

## Bearbeiten einer Rolle

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**.

1. Suchen Sie die Rolle mithilfe von Filtern über dem Raster und klicken Sie auf den Rollennamen.

1. Nehmen Sie die erforderlichen Änderungen vor.

   Informationen zu den Rolleneinstellungen finden Sie in den Schritten zum Erstellen einer Benutzerrolle .

1. Geben Sie bei Aufforderung Ihr Kennwort ein, um Ihre Identität zu bestätigen.

1. Klicken Sie auf die **[!UICONTROL Save Role]**.

## Löschen einer Rolle

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**.

1. Suchen Sie die Rolle mithilfe von Filtern über dem Raster und öffnen Sie sie im Bearbeitungsmodus.

1. Klicken Sie oben rechts auf **[!UICONTROL Delete Role]**.

1. Um die Aktion zu bestätigen, klicken Sie auf **[!UICONTROL OK]**.

## Demo zu Benutzerrollen

In diesem Video erfahren Sie mehr über die Verwaltung von Benutzerrollen:

>[!VIDEO](https://video.tv.adobe.com/v/343654?quality=12&learn=on)

## Rollenressourcen

Der Zugriff auf die folgenden Ressourcen kann einer benutzerdefinierten Rolle zugewiesen werden. Weitere Informationen zu den Funktionen, die mit den einzelnen Ressourcen verknüpft sind, finden Sie auf der verknüpften Seite .

![Adobe Commerce](../assets/adobe-logo.svg) - nur Adobe Commerce

![Adobe Commerce B2B](../assets/b2b.svg) - Nur in Adobe Commerce B2B verfügbar

| Ressource |   |   |
| --- | --- | --- |
| [`Dashboard`](../getting-started/admin-dashboard.md) |  |  |
| [`Sales`](../stores-purchase/sales-menu.md) | [`Operations`](../stores-purchase/orders.md) |  |
|  | [`Quotes`](../b2b/quotes.md) ![Adobe Commerce B2B](../assets/b2b.svg) <br/>[`Orders`](../stores-purchase/orders.md)<br/>[`Invoices`](../stores-purchase/invoices.md)<br/>[`Shipments`](../stores-purchase/shipments.md)<br/>[`Credit Memos`](../stores-purchase/credit-memos.md)<br/>[`Billing Agreements`](../stores-purchase/paypal-billing-agreements.md)<br/>[`Returns`](../stores-purchase/returns.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`Transactions`](../stores-purchase/transactions.md) |
|  | [`Archive`](action-log-archive.md)![Adobe Commerce] |  |
|  | [`Shopping Cart Management`](../stores-purchase/cart.md) |  |
| [`Catalog`](../catalog/catalog-menu.md) | [`Category Permissions`](../catalog/categories.md) ![Adobe Commerce](../assets/adobe-logo.svg) |  |
|  | [`Inventory`](../inventory-management/introduction.md) | [`Products`](../catalog/products-list.md)<br/>[`Categories`](../catalog/categories.md) |
|  | [`Shared Catalog`](../b2b/catalog-shared-create.md) ![Adobe Commerce B2B](../assets/b2b.svg) | [`Manage Shared Catalog`](../b2b/catalog-shared-manage.md) |
| [`Customers`](../customers/guide-overview.md) | [`All Customers`](../customers/customers-all.md)<br/>[`Now Online`](../customers/now-online.md)<br/>[`Customer Groups`](../customers/customer-groups.md)<br/>[`Segments`](../customers/customer-segments.md) ![Adobe Commerce](../assets/adobe-logo.svg) |  |
|  | [`Login as Customer`](../customers/login-as-customer.md) | `Allow Login as Customer Button`<br/>`View Login as Customer Log` ![Adobe Commerce](../assets/adobe-logo.svg) |
|  | [`Companies`](../b2b/account-companies.md) ![Adobe Commerce B2B](../assets/b2b.svg) | [`Manage Companies`](../b2b/account-company-manage.md) <br/>`Add New Company` <br/>`Delete Company` <br/>`Reimburse Balance` |
| [`Carts`](../stores-purchase/shopping-assisted-cart-manage.md) | [`Manage carts`](../stores-purchase/shopping-assisted-cart-manage.md) |  |
| [`My Account`](../customers/account-dashboard-my-account.md) |  |  |
| [`Marketing`](../merchandising-promotions/marketing-menu.md) | [`Promotions`](../merchandising-promotions/marketing-menu.md#uicontrol-promotions) | [`Catalog Price Rule`](../merchandising-promotions/price-rules-catalog.md) <br/>[`Cart Price Rules`](../merchandising-promotions/price-rules-cart.md) <br/>[`Related Products Rules`](../merchandising-promotions/product-related-rules.md)![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`Gift Card Accounts`](../stores-purchase/product-gift-card-accounts.md) ![Adobe Commerce](../assets/adobe-logo.svg) |
|  | [`Private Sales`](../merchandising-promotions/events-private-sales.md) ![Adobe Commerce](../assets/adobe-logo.svg) | [`Events`](../merchandising-promotions/event-create.md) <br/>[`Invitations`](../merchandising-promotions/invitations.md) |
|  | `Communications` | [`Email Templates`](email-templates.md) <br/>[`Newsletter Template`](../merchandising-promotions/newsletter-template.md) <br/>[`Newsletter Queue`](../merchandising-promotions/newsletter-queue.md) <br/>[`Newsletter Subscribers`](../merchandising-promotions/newsletter-subscribers.md) <br/>[`Email Reminders`](../merchandising-promotions/email-reminder-rules.md) |
|  | `Sales Channel` | [`Amazon Sales Channel`](https://experienceleague.adobe.com/docs/commerce-channels/amazon/overview.html) |
|  | [`SEO & Search`](../merchandising-promotions/marketing-menu.md#uicontrol-seo--search) | [`Search Terms`](../catalog/search-terms.md) <br/>[`Search Synonyms`](../catalog/search-terms.md#search-synonyms) ![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`URL Rewrites`](../merchandising-promotions/url-rewrite-custom.md) <br/>[`Site Map`](../merchandising-promotions/sitemap-xml.md) |
|  | [`User Content`](../merchandising-promotions/product-reviews-moderate.md) | [`All Reviews`](../merchandising-promotions/product-reviews.md) <br/>[`Pending Reviews`](../merchandising-promotions/product-reviews-moderate.md) <br/> |  |
| [`Content`](../content-design/content-menu.md) | [`Elements`](../content-design/content-menu.md#uicontrol-elements)) | [`Pages`](../content-design/pages.md)<br/>[`Hierarchy`](../content-design/page-hierarchy.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`Blocks`](../content-design/blocks.md)<br/>[`Dynamic Blocks`](../content-design/dynamic-blocks.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`Widgets`](../content-design/widgets.md)<br/>[`Media Gallery`](../content-design/media-gallery.md) |  |
|  | [`Design`](../content-design/introduction.md#design) | [`Themes`](../content-design/themes.md)<br/>[`Schedule`](../content-design/schedule.md) |  |
|  | [Inhalts-Staging](../content-design/content-staging.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br /> |  |
| [`Reports`](../getting-started/reports-menu.md) | [`Marketing`](../getting-started/marketing-reports.md) | `Shopping Cart`<br />[`Search Terms`](../catalog/search-terms.md#search-terms-report)<br />`Newsletter Problem Reports` |  |
|  | [`Reviews`](../getting-started/review-reports.md)<br /> |  |
|  | [`Sales`](../getting-started/sales-reports.md) |  |
|  | `System Insights` ![Adobe Commerce](../assets/adobe-logo.svg) | [`Site-Wide Analysis Tool`](https://experienceleague.adobe.com/docs/commerce-operations/tools/site-wide-analysis-tool/access.html) |
|  | [`Customers`](../getting-started/customer-reports.md)<br/>[`Products`](../getting-started/product-reports.md)<br/>[`Private Sales`](../getting-started/private-sales-reports.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br />[`Statistics`](../getting-started/reports-menu.md#uicontrol-statistics)<br />[`Business Intelligence`](../getting-started/business-intelligence.md) |  |
| [`Stores`](../stores-purchase/stores.md) | [`Settings`](../stores-purchase/stores-menu.md) | [`All Stores`](../stores-purchase/stores.md)<br/>[`Configuration`](../configuration-reference/guide-overview.md)<br/>[`Terms and Conditions`](../stores-purchase/terms-and-conditions.md)<br/>[`Order Status`](../stores-purchase/order-status.md) |  |
|  | [`Inventory`](../inventory-management/sources-stocks.md) | [`Sources`](../inventory-management/sources-manage.md)<br/>[`Stocks`](../inventory-management/stocks-manage.md) |  |
|  | [`Taxes`](../stores-purchase/taxes.md) |  |  |
|  | [`Currency`](../stores-purchase/currency.md) | [`Currency Rates`](../stores-purchase/currency-update.md)<br/>[`Currency Symbols`](../stores-purchase/currency-configuration.md#step-5-customize-currency-symbols-optional) |  |
|  | [`Attributes`](../catalog/product-attributes.md) | [`Product`](../catalog/attribute-product-create.md)<br/>[`Update Attributes`](../catalog/attribute-product-create.md)<br/>[`Attribute Set`](../catalog/attribute-sets.md)<br/>[`Ratings`](../merchandising-promotions/product-reviews.md#create-custom-ratings) |
|  | [`Other Settings`](../stores-purchase/stores-menu.md) | [`Customer Groups`](../customers/customer-groups.md) |
| [`System`](system-menu.md) | [`Data Transfer`](data-transfer.md) | [`Import`](data-import.md)<br/>[`Export`](data-export.md)<br/>[`Import/Export Tax Rates`](data-transfer-tax-rates.md)<br/>[`Import History`](data-import.md#import-history) |  |
|  | [`Magento Connect`](../getting-started/commerce-marketplace.md) | `Connect Manager`<br/>`Package Extensions` |  |
|  | [`Tools`](system-menu.md#tools) | [`Cache Management`](cache-management.md)<br/>[`Backups`](backups.md)<br/>[`Index Management`](index-management.md)<br/>[`Change Indexer Mode`](index-management.md) |  |
|  | [`Permissions`](permissions.md) | [`All Users`](permissions-users-all.md)<br/>[`Locked Users`](permissions-users-all.md#locked-users)<br/>[`User Roles`](permissions-user-roles.md) |
| [`Action Log`](action-log.md)![Adobe Commerce](../assets/adobe-logo.svg) | [`Report`](action-log.md)<br/>[`Archive`](action-log-archive.md) |
|  | [`Other Settings`](system-menu.md) | [`Notifications`](notifications.md)<br/>[`Custom Variables`](variables-custom.md)<br/>[`Manage Encryption Key`](encryption-key.md) |  |
| [`Global Search`](../getting-started/admin-workspace.md#workspace-search) |  |  |

{style="table-layout:auto"}
