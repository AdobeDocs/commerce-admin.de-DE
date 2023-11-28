---
title: Benutzerrollen
description: Erfahren Sie, wie Sie Benutzerrollen und die zugehörigen Berechtigungen erstellen, um den Zugriff auf Admin-Funktionen zu verwalten.
exl-id: a70f74d4-72b4-4639-a67d-9fc13df65924
feature: Admin Workspace, Roles/Permissions, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '659'
ht-degree: 0%

---

# Benutzerrollen

Um jemandem eingeschränkten Zugriff auf den Admin zu gewähren, besteht der erste Schritt darin, eine Rolle zu erstellen, die über die entsprechenden Berechtigungen verfügt. Nachdem die Rolle gespeichert wurde, können Sie neue Benutzer hinzufügen und ihnen die eingeschränkte Rolle zuweisen, um ihnen eingeschränkten Zugriff auf den Administrator zu gewähren.

![Admin - Benutzerrollen](./assets/permissions-role-grid.png){width="600" zoomable="yes"}

## Rollen definieren

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**.

1. Klicken Sie oben rechts auf **[!UICONTROL Add New Role]**.

1. Führen Sie die Schritte aus, um die Rolle zu definieren:

### Schritt 1: Hinzufügen des Rollennamens

1. under _[!UICONTROL Role Information]_, eine Beschreibung eingeben **[!UICONTROL Role Name]**.

1. under _[!UICONTROL Current User Identity Verification]_, geben Sie Ihr Kennwort ein.

   ![Systemberechtigungen - Rolleninformationen](./assets/permissions-role-info.png){width="600" zoomable="yes"}

### Schritt 2: Ressourcen zuweisen

>[!IMPORTANT]
>
>Stellen Sie beim Zuweisen von Ressourcen sicher, dass Sie den Zugriff auf das Berechtigungs-Tool deaktivieren, wenn Sie den Zugriff auf eine bestimmte Rolle beschränken. Andernfalls können Benutzer ihre eigenen Berechtigungen ändern.

1. Satz **[!UICONTROL Role Scopes]** auf einen der folgenden Werte zu:

   - `All`
   - `Custom`

   Wenn auf `Custom` für eine Multisite-Installation aktivieren Sie das Kontrollkästchen der Website und speichern Sie, wo die Rolle verwendet werden soll.

   ![Benutzerrollenressourcen - benutzerdefinierter Umfang](./assets/permissions-role-scope-custom.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Benutzer mit `Custom` Der Rollenbereich kann keine Websites und Kategorien erstellen, Produkte Kategorien zuweisen oder Produkte bearbeiten unter _[!UICONTROL All Store Views]_Umfang, wenn sie eingeschränkten Stores zugewiesen werden. Diese Benutzer können auch keine anderen_ global _Aktionen, die Bereiche betreffen, auf die sie keinen Zugriff haben.

1. under _[!UICONTROL Roles Resources]_, set **[!UICONTROL Resource Access]**nach `Custom`.

1. Im **[!UICONTROL Resource]** Baumstruktur verwenden, aktivieren Sie das Kontrollkästchen der einzelnen Admin-Funktionen, auf die die Rolle zugreifen kann.

   Um eine Administratorrolle mit Zugriff auf Steuereinstellungen zu erstellen, wählen Sie die Ressourcen Verkauf/Steuern und System/Steuern aus. Wenn Sie eine Website für eine Region einrichten, die sich von Ihrer Standardeinstellung unterscheidet [Versandort](../stores-purchase/shipping-settings.md#point-of-origin), müssen Sie den Zugriff auf die System-/Versandressourcen für die Rolle zulassen. Die Versandeinstellungen bestimmen den für Katalogpreise verwendeten Steuersatz.

   ![Zugewiesene Benutzerrollenressourcen](./assets/permissions-role-resources-product.png){width="600" zoomable="yes"}

   Die Liste der verfügbaren Berechtigungen kann zusätzliche Optionen für gebündelte und installierte Erweiterungen enthalten. Durch Auswahl der höchsten Berechtigung für jede Funktion weisen Sie alle für den Benutzer verfügbaren Berechtigungen zu.

   >[!NOTE]
   >
   >Ein Admin-Benutzer muss **[!UICONTROL Sales / Archive]** -Berechtigungen für ihren Rollenbereich zum Anzeigen der _[!UICONTROL Invoices]_,_[!UICONTROL Credit Memos]_, und _[!UICONTROL Shipments]_bestellen [Tabs](../stores-purchase/order-processing.md).

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Role]**.

   Die Rolle wird nun im Raster angezeigt und kann Benutzerkonten zugewiesen werden.

## Benutzern eine Rolle zuweisen

1. Aus dem _[!UICONTROL Roles]_-Raster den Datensatz im Bearbeitungsmodus öffnen.

1. under _[!UICONTROL Current User Identity Verification]_, geben Sie Ihr Passwort für Ihr Benutzerkonto ein.

1. Wählen Sie im linken Bereich die Option **[!UICONTROL Role Users]**.

   Die _[!UICONTROL Role Users]_wird nur angezeigt, nachdem eine neue Rolle gespeichert wurde.

   ![Benutzerkonten, die der Rolle zugewiesen sind](./assets/permissions-role-users.png){width="600" zoomable="yes"}

1. Gehen Sie wie folgt vor, um nach einem bestimmten Benutzerdatensatz zu suchen:

   - Geben Sie den Wert im Suchfilter oben in einer Spalte ein und drücken Sie die Eingabetaste **Eingabe**.

   - Wenn Sie zur vollständigen Liste zurückkehren möchten, klicken Sie auf **[!UICONTROL Reset Filter]**.

1. Aktivieren Sie das Kontrollkästchen der Benutzer, die der Rolle zugewiesen werden sollen.

1. Klicken **[!UICONTROL Save Role]**.

## Rollen bearbeiten

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**.

1. Suchen Sie die Rolle mithilfe von Filtern über dem Raster und klicken Sie auf den Namen der Rolle.

1. Nehmen Sie die erforderlichen Änderungen vor.

   Informationen zu den Rolleneinstellungen finden Sie in den Schritten zum Erstellen einer Benutzerrolle .

1. Geben Sie bei Aufforderung Ihr Kennwort zur Bestätigung Ihrer Identität ein.

1. Klicken Sie auf **[!UICONTROL Save Role]**.

## Rollen löschen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**.

1. Suchen Sie die Rolle mithilfe von Filtern über dem Raster und öffnen Sie sie im Bearbeitungsmodus.

1. Klicken Sie oben rechts auf **[!UICONTROL Delete Role]**.

1. Klicken Sie zur Bestätigung der Aktion auf **[!UICONTROL OK]**.

## Demo zu Benutzerrollen

In diesem Video erfahren Sie mehr über die Verwaltung von Benutzerrollen:

>[!VIDEO](https://video.tv.adobe.com/v/343654?quality=12)

## Rollenressourcen

Der Zugriff auf die folgenden Ressourcen kann einer benutzerdefinierten Rolle zugewiesen werden. Auf der verknüpften Seite erfahren Sie mehr über die Funktionen, die mit den einzelnen Ressourcen verknüpft sind.

![Adobe Commerce](../assets/adobe-logo.svg) - Nur Adobe Commerce

![B2B für Adobe Commerce](../assets/b2b.svg) - Nur mit B2B für Adobe Commerce verfügbar

| Ressource |   |   |
| --- | --- | --- |
| [`Dashboard`](../getting-started/admin-dashboard.md) |  |  |
| [`Sales`](../stores-purchase/sales-menu.md) | [`Operations`](../stores-purchase/orders.md) |  |
|  | [`Quotes`](../b2b/quotes.md) ![B2B für Adobe Commerce](../assets/b2b.svg) <br/>[`Orders`](../stores-purchase/orders.md)<br/>[`Invoices`](../stores-purchase/invoices.md)<br/>[`Shipments`](../stores-purchase/shipments.md)<br/>[`Credit Memos`](../stores-purchase/credit-memos.md)<br/>[`Billing Agreements`](../stores-purchase/paypal-billing-agreements.md)<br/>[`Returns`](../stores-purchase/returns.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br/>[`Transactions`](../stores-purchase/transactions.md) |
|  | [`Archive`](action-log-archive.md)![Adobe Commerce] |  |
|  | [`Shopping Cart Management`](../stores-purchase/cart.md) |  |
| [`Catalog`](../catalog/catalog-menu.md) | [`Category Permissions`](../catalog/categories.md) ![Adobe Commerce](../assets/adobe-logo.svg) |  |
|  | [`Inventory`](../inventory-management/introduction.md) | [`Products`](../catalog/products-list.md)<br/>[`Categories`](../catalog/categories.md) |
|  | [`Shared Catalog`](../b2b/catalog-shared-create.md) ![B2B für Adobe Commerce](../assets/b2b.svg) | [`Manage Shared Catalog`](../b2b/catalog-shared-manage.md) |
| [`Customers`](../customers/guide-overview.md) | [`All Customers`](../customers/customers-all.md)<br/>[`Now Online`](../customers/now-online.md)<br/>[`Customer Groups`](../customers/customer-groups.md)<br/>[`Segments`](../customers/customer-segments.md) ![Adobe Commerce](../assets/adobe-logo.svg) |  |
|  | [`Login as Customer`](../customers/login-as-customer.md) | `Allow Login as Customer Button`<br/>`View Login as Customer Log` ![Adobe Commerce](../assets/adobe-logo.svg) |
|  | [`Companies`](../b2b/account-companies.md) ![B2B für Adobe Commerce](../assets/b2b.svg) | [`Manage Companies`](../b2b/account-company-manage.md) <br/>`Add New Company` <br/>`Delete Company` <br/>`Reimburse Balance` |
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
|  | [Inhaltstaging](../content-design/content-staging.md) ![Adobe Commerce](../assets/adobe-logo.svg)<br /> |  |
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
