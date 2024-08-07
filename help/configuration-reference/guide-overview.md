---
title: Konfigurationshandbuch
description: Überprüfen Sie die beschreibenden Informationen für alle Commerce Admin Store-Konfigurationseinstellungen, die durch die Konfigurationsregisterkarten, -seiten und -abschnitte organisiert sind.
exl-id: b0359ba4-3643-4355-9154-adfedb369ec3
source-git-commit: 323ea635286fcb9a2bcc7f4f56b32c1518a7beef
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 0%

---

# Konfigurationshandbuch

Dieses Handbuch richtet sich an Händler und Systemadministratoren, die in Adobe Commerce oder Magento Open Source arbeiten. Sie enthält Referenzinformationen für alle Speicherkonfigurationseinstellungen, auf die über die Seitenleiste _Admin_ unter **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**zugegriffen wird.

Es werden keine Details zu den Funktionen von Adobe Commerce und der Magento Open Source oder Verfahren für die Speicherkonfiguration behandelt.

Diese Anleitung ist entsprechend der Konfiguration der linken Navigation organisiert:

| Registerkarte &quot;Konfiguration&quot; | Untergeordnete Registerkarten |
| ----------------- | ---------- |
| **[!UICONTROL General]** <br/><br/> Die _[!UICONTROL General]_-Konfigurationsabschnitte bestimmen Store-Parameter, URLs, Design, Währung, E-Mail-Adressen, Storekontakte, Editor und Dashboard-Bericht. | - [[!UICONTROL General]](./general/general.md)<br>- [[!UICONTROL B2B Features]](./general/b2b-features.md)<br>- [[!UICONTROL Web]](./general/web.md)<br>- [[!UICONTROL Currency Setup]](./general/currency-setup.md)<br>- [[!UICONTROL Store Email Addresses]](./general/store-email-addresses.md)<br>- [[!UICONTROL Contacts]](./general/contacts.md)<br>- [[!UICONTROL Reports]](./general/reports.md)<br>- [[!UICONTROL Content Management]](./general/content-management.md)<br>- [[!UICONTROL New Relic Reporting]](./general/new-relic-reporting.md)<br>- [[!UICONTROL Advanced Reporting]](./general/advanced-reporting.md) |
| **[!UICONTROL Catalog]** <br/><br/> Die Konfigurationseinstellungen _[!UICONTROL Catalog]_bestimmen die Produkt- und Bestandseinstellungen, steuern die Sitemap- und RSS-Feed-Generierung und geben die E-Mail-Vorlage an, die zum Freigeben von Produkten für Freunde verwendet wird. | - [[!UICONTROL Catalog]](./catalog/catalog.md)<br>- [[!UICONTROL Visual Merchandiser]](./catalog/visual-merchandiser.md)<br>- [[!UICONTROL Inventory]](./catalog/inventory.md)<br>- [[!UICONTROL XML Sitemap]](./catalog/xml-sitemap.md)<br>- [[!UICONTROL RSS Feeds]](./catalog/rss-feeds.md)<br>- [[!UICONTROL Email to a Friend]](./catalog/email-to-a-friend.md) |
| **[!UICONTROL Security]** <br/><br/> Die _[!UICONTROL Security]_Konfigurationseinstellungen steuern die Speichersicherheit, die Zwei-Faktor-Authentifizierung und die Google reCAPTCHA-Funktion. | - [[!UICONTROL 2FA]](./security/2fa.md)<br>- [[!UICONTROL Google reCAPTCHA Admin Panel]](./security/google-recaptcha-admin.md)<br>- [[!UICONTROL Google reCAPTCHA Storefront]](./security/google-recaptcha-storefront.md)<br>- [[!UICONTROL Security.txt]](./security/security-txt.md) |
| **[!UICONTROL Customers]** <br/><br/>Die Konfigurationseinstellungen für _[!UICONTROL Customers]_legen grundlegende Kundenkonto- und Anmeldeoptionen, Newsletter-Einstellungen, Wunschlisten und das Format der automatisch generierten Coupon-Codes fest. | - [[!UICONTROL Login as Customer]](./customers/login-as-customer.md)<br>- [[!UICONTROL Newsletter]](./customers/newsletter.md)<br>- [[!UICONTROL Company Configuration]](./customers/company-configuration.md)<br>- [[!UICONTROL Customer Configuration]](./customers/customer-configuration.md)<br>- [[!UICONTROL Requisition Lists]](./customers/requisition-lists.md)<br>- [[!UICONTROL Wish List]](./customers/wishlist.md)<br>- [[!UICONTROL Invitations]](./customers/invitations.md)<br>- [[!UICONTROL Reward Points]](./customers/reward-points.md)<br>- [[!UICONTROL Promotions]](./customers/promotions.md)<br>- [[!UICONTROL Gift Registry]](./customers/gift-registry.md)<br>- [[!UICONTROL Persistent Shopping Cart]](./customers/persistent-shopping-cart.md) |
| **[!UICONTROL Sales]** <br/><br/> Die Konfigurationseinstellungen für _[!UICONTROL Sales]_bestimmen die Kasse- und Steuereinstellungen, die Zahlungs- und Versandoptionen, Verkaufs-E-Mail- und PDF-Druck-outs sowie die Google-API-Einstellungen. | - [[!UICONTROL Sales]](./sales/sales.md)<br>- [[!UICONTROL Sales Emails]](./sales/sales-emails.md)<br>- [[!UICONTROL Quotes]](./sales/quotes.md)<br>- [[!UICONTROL PDF Print-outs]](./sales/pdf-print-outs.md)<br>- [[!UICONTROL Tax]](./sales/tax.md)<br>- [[!UICONTROL Checkout]](./sales/checkout.md)<br>- [[!UICONTROL Shipping Settings]](./sales/shipping-settings.md)<br>- [[!UICONTROL Multishipping Settings]](./sales/multishipping-settings.md)<br>- [[!UICONTROL Delivery Methods]](./sales/delivery-methods.md)<br>- [[!UICONTROL Google API]](./sales/google-api.md)<br>- [[!UICONTROL 3D Secure]](./sales/3d-secure.md)<br>- [[!UICONTROL Gift Cards]](./sales/gift-cards.md)<br>- [[!UICONTROL Payment Methods]](./sales/payment-methods.md) |
| **[!UICONTROL Sales Channels]** <br/><br/>Wenn die [!DNL Amazon Sales Channel] -Erweiterung installiert ist, steuern die _[!UICONTROL Sales Channels]_-Einstellungen die automatisierten Integrationsvorgänge mit Ihrem Amazon-Store. | - [[!UICONTROL Global Settings]](sales-channels.md) |
| **[!UICONTROL Services]** <br/><br/>Die Konfigurationseinstellungen _[!UICONTROL Services]_bestimmen die Integrationseinstellungen der Commerce-API, einschließlich SOAP und OAuth. | - [[!UICONTROL Web API]](./services/magento-web-api.md)<br>- [[!UICONTROL Commerce Services]](./services/saas.md)<br>- [[!UICONTROL OAuth]](./services/oauth.md) |
| **[!UICONTROL Advanced]** <br/><br/> Die Konfigurationseinstellungen _[!UICONTROL Advanced]_bestimmen die standardmäßigen Admin-Einstellungen, verschiedene Systemkonfigurationseinstellungen, erweiterte Modulsteuerelemente und Entwickler-Tools. | - [[!UICONTROL Admin]](./advanced/admin.md)<br>- [[!UICONTROL System]](./advanced/system.md)<br>- [[!UICONTROL Developer]](./advanced/developer.md) |

{style="table-layout:auto"}

Es werden keine Details zu den Funktionen von Adobe Commerce und der Magento Open Source oder Verfahren für die Speicherkonfiguration behandelt.

## Verfügbare Dokumentation

{{docs-links}}
