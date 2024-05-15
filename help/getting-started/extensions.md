---
title: Erweiterungen von Adobe
description: Überprüfen Sie Informationen zu Erweiterungen für Adobe Commerce und Magento Open Source, die von Adobe veröffentlicht werden.
exl-id: 86338edc-c32a-41c8-9594-6aec26f53ac6
feature: Extensions
source-git-commit: 6414a7aea7dcbe0f2379ed74455518220a1fbd64
workflow-type: tm+mt
source-wordcount: '950'
ht-degree: 0%

---

# Erweiterungen von Adobe

Dieses Thema enthält Informationen zu Erweiterungen für Adobe Commerce und Magento Open Source, die von Adobe veröffentlicht werden. Erweiterungen fügen dem Admin und der Storefront Funktionen, Dienste und Integrationen hinzu. Einige dieser Erweiterungen werden durch Gemeinschaftsbeiträge der Magento Open Source entwickelt. Einige Erweiterungen erfordern eine separate Installation, andere sind standardmäßig installiert.

## Installierte Erweiterungen

Es gibt einige Erweiterungen, die automatisch mit Adobe Commerce oder Magento Open Source installiert werden.

### [!DNL Inventory Management]

[!DNL Commerce] [[!DNL Inventory Management]](../inventory-management/introduction.md) bietet ein verbessertes Lager- und Versandmanagement über einen oder mehrere Standorte und Vertriebskanäle hinweg mit gleichzeitigem Schutz und gleichzeitigen Algorithmen zum Abgleich von Sendungen. Verfolgen Sie Ihre Lagerbestandsmengen, liefern Sie exakte Verkaufsmengen an Kunden, und versenden Sie gemäß Empfehlungen oder manueller Auswahl, um Ihren gesamten Bestand zu kontrollieren. Konfigurieren Sie Verwaltungseinstellungen global, pro Quelle und pro Produkt.

>[!NOTE]
>
>Diese Erweiterung wurde im Rahmen der [[!DNL Inventory Management]](https://github.com/magento/inventory) (ehemals MSI) Projekt durch das Engineering-Programm der Community.

[!DNL Inventory Management] installiert, wobei alle Funktionen standardmäßig aktiviert sind. Zur Aktivierung dieser Bestandsfunktionen sind keine zusätzlichen Schritte erforderlich. Weitere Informationen zum [!DNL Inventory Management] -Funktionen, siehe [[!DNL Inventory Management] Benutzerhandbuch](../inventory-management/guide-overview.md).

### Braintree

PayPal und Gene Commerce haben gemeinsam die offizielle Braintree-Erweiterung für Commerce 2.4.x Stores entwickelt. Dank eines verbesserten Checkout-Erlebnisses, das die Konversion fördern soll, enthalten die Updates PayLater-Optionen, mit denen Verbraucher beim Einkauf und während des Checkout automatisch relevante PayLater-Nachrichten und -Schaltflächen sehen können.

Diese Erweiterung ist standardmäßig installiert, erfordert jedoch eine [Braintree-Konto](https://www.braintreepayments.com/) und der Konfiguration in der Admin-Funktion, die für Ihren Store aktiviert werden soll. Um die Gebühren für die Verwendung von Braintree zur Verarbeitung Ihrer Transaktionen zu bestimmen, überprüfen Sie die [Braintree-Preise](https://www.braintreepayments.com/braintree-pricing).

Informationen zur Braintree-Konfiguration im Admin finden Sie in der [Braintree](../stores-purchase/braintree.md) Thema im _Handbuch für Verkaufs- und Kauferlebnisse_.

### Google reCAPTCHA

Google reCAPTCHA bietet sowohl für die Storefront als auch für die Admin-Benutzeroberfläche ein höheres Sicherheitsniveau als mit dem Standard-CAPTCHA verfügbar ist und bietet Ihnen die Möglichkeit:

- Überprüfen Sie, wann Kunden Konten erstellen, Kennwörter abrufen, sich bei ihren Konten anmelden oder sich an Ihr Unternehmen wenden.
- Erhöhen Sie die Sicherheit bei der Anmeldung von Admin-Benutzern.

Dadurch wird der potenzielle Benutzerfehler bei der Eingabe eines Captcha-Codes reduziert und die Konversion des Warenkorbs gefördert, ohne dass beim Checkout Hürden hinzugefügt werden. [reCAPTCHA aktivieren und konfigurieren](../systems/security-google-recaptcha.md) mit unsichtbaren oder interaktiven Prüfungen, um den sicheren Zugriff auf die [!DNL Commerce] Admin und Storefront.

### Zweifaktorauthentifizierung

Die [!DNL Commerce] Admin bietet Zugriff auf Ihre Store-, Bestellungen- und Kundendaten. [Zweifaktorauthentifizierung](../systems/security-two-factor-authentication.md) (2FA oder TFA) verbessert die Sicherheit, indem zusätzliche Authentifizierung erforderlich ist, die über den standardmäßigen Anmeldenamen und das Standardkennwort hinausgeht, um auf die [!DNL Commerce] Admin von allen Geräten aus. Die Erweiterung unterstützt mehrere Authentifizierer, einschließlich Google Authenticator, [!DNL Duo], und U2F-Schlüssel. Diese Authentifizierung gilt nur für Admin-Benutzer. Sie ist nicht für Storefront-Kundenkonten verfügbar.

Diese Funktionen sind standardmäßig aktiviert. Jeder Admin-Benutzer muss einen der unterstützten Authentifizierer installieren und konfigurieren.

>[!NOTE]
>
>Bei Adobe Commerce-Stores, bei denen die Authentifizierung für Adobe Identity Management Services (IMS) für den Admin aktiviert wurde, ist die native Commerce 2FA deaktiviert. Benutzer, die mit ihren Adobe-Anmeldedaten beim Admin angemeldet sind, müssen sich nicht für viele Administratoraufgaben erneut authentifizieren. Die Authentifizierung wird von Adobe IMS verarbeitet, wenn sich der Administrator in seiner aktuellen Sitzung anmeldet. Siehe [Integrationsübersicht für Adobe Identity Management Service (IMS)](./adobe-ims-integration-overview.md).

## Hinzufügen von Erweiterungen

Die [[!DNL Commerce Marketplace]](https://marketplace.magento.com/) ist die globale eCommerce-Ressource für Anwendungen und Dienste, die erweitert werden [!DNL Commerce] Lösungen mit leistungsstarken neuen Funktionen. Adobe veröffentlicht mehrere Erweiterungen über [!DNL Marketplace] die in Ihrem Adobe Commerce- oder Magento Open Source-Store installiert und konfiguriert werden können, um erweiterte Integrationen und Funktionen bereitzustellen.

### [!DNL Live Search]

![Adobe Commerce](../assets/adobe-logo.svg) Nur Adobe Commerce

Die [!DNL Live Search] -Erweiterung verbindet Ihren Store mit dem Live-Suchdienst - einer kostenlosen Suchplattform aus Adobe Commerce, mit der Verkäufer nahtlos in der Lage sind, Kunden eine KI-gestützte Sucherfahrung anzubieten. Intelligente Faceting-Tools, die mit künstlicher Intelligenz von Adobe entwickelt wurden, helfen Händlern, mit weniger zu arbeiten, indem die manuelle Arbeit rund um Facettierung/Filterung entfernt wird.

Siehe [Benutzerhandbuch zur Live Search](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/guide-overview.html) für weitere Informationen.

### [!DNL Product Recommendations]

![Adobe Commerce](../assets/adobe-logo.svg) Nur Adobe Commerce

Die [!DNL Product Recommendations] -Erweiterung verbindet Ihren Speicher mit dem Product Recommendations-Dienst - einem leistungsstarken Marketing-Tool, mit dem Sie Konversionen, Umsätze und Interaktionen steigern können. [!DNL Product Recommendations] wurde von Adobe Commerce errichtet und wird von der gekämpften künstlichen Intelligenz, Adobe Sensei, angetrieben, sodass Sie sicher Engagement und Konversion fördern können. Diese Funktion entfernt die manuelle Arbeit, die erforderlich ist, um jedem Käufer relevante Produktempfehlungen zu unterbreiten.

Siehe [[!DNL Product Recommendations] Benutzerhandbuch](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/guide-overview.html?lang=en) für weitere Informationen.

### [!DNL Catalog Service]

Die [!DNL Catalog Service] ermöglicht es Ihnen, Kunden ein optimiertes Produkterlebnis zu bieten und gleichzeitig die Leistung zu steigern, die Skalierbarkeit zu verbessern und Konversionen zu steigern. Siehe [[!DNL Catalog Service] Benutzerhandbuch](https://experienceleague.adobe.com/docs/commerce-merchant-services/catalog-service/guide-overview.html) für weitere Informationen.

### [!DNL Payment Services]

[!DNL Payment services] für Adobe Commerce und Magento Open Source ist eine vollständig integrierte Zahlungslösung, die das Zahlungsmanagement vereinfacht und Ihren Kunden die Möglichkeit gibt, ihren Weg zu bezahlen. Sichere Abstimmung aller Zahlungs- und Transaktionsdaten innerhalb des Adobe Commerce-Administrators, sodass Sie Bestellungen und Zahlungen zentral verwalten und gleichzeitig einen nahtlosen Checkout durchführen können. Siehe [[!DNL Payment Services] Benutzerhandbuch](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html) für weitere Informationen.

### [!DNL Store Fulfillment]

Store Fulfillment für Adobe Commerce und Magento Open Source ermöglicht einen erstklassigen Online-Einkauf, eine BOPIS-Kundenerfahrung und eine maximale Mitarbeiterproduktivität, indem ein umfassender, auf einem Mobilgerät aktivierter Fulfillment-Workflow bereitgestellt wird. Siehe [[!DNL Store Fulfillment] Benutzerhandbuch](https://experienceleague.adobe.com/docs/commerce-merchant-services/store-fulfillment/guide-overview.html) für weitere Informationen.

### [!DNL Amazon Sales Channel]

Die [!DNL Amazon Sales Channel] für Adobe Commerce ermöglicht Ihnen die Integration Ihrer Amazon Seller Central-Listing-Datenbank in Ihre [!DNL Commerce] Produktkatalog erstellen und Ihre Amazon-Auflistungen und -Verkäufe in der Commerce Admin verwalten. Siehe [[!DNL Amazon Sales] Benutzerhandbuch](https://experienceleague.adobe.com/docs/commerce-channels/amazon/guide-overview.html) für weitere Informationen.

### [!DNL Channel Manager]

[!DNL Channel Manager] ermöglicht es Ihnen, den Umsatz zu steigern, neue Kunden zu erreichen, den Betrieb zu optimieren und Zeit zu sparen, indem Sie einen Adobe Commerce- oder Magento Open Source-Produktkatalog in den Walmart Marketplace integrieren. Nachdem Sie die Erweiterung installiert und konfiguriert haben, können Ihre Mitarbeiter die Walmart Marketplace-Listen, Inventare, Bestellungen, Rückgaben und Erstattungen nahtlos über die [!DNL Commerce Admin]. Siehe [[!DNL Channel Manager] Benutzerhandbuch](https://experienceleague.adobe.com/docs/commerce-channels/channel-manager/guide-overview.html) für weitere Informationen.
