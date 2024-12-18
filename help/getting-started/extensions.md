---
title: Erweiterungen von Adobe
description: Lesen Sie Informationen zu Erweiterungen für Adobe Commerce und Magento Open Source, die von Adobe veröffentlicht wurden.
exl-id: 86338edc-c32a-41c8-9594-6aec26f53ac6
feature: Extensions
source-git-commit: 6414a7aea7dcbe0f2379ed74455518220a1fbd64
workflow-type: tm+mt
source-wordcount: '950'
ht-degree: 0%

---

# Erweiterungen von Adobe

In diesem Abschnitt finden Sie Informationen zu Erweiterungen für Adobe Commerce und Magento Open Source, die auf Adobe veröffentlicht werden. Erweiterungen fügen Funktionen, Dienste und Integrationen zur Admin- und Storefront hinzu. Einige dieser Erweiterungen werden durch Beiträge der Magento Open Source Community entwickelt. Einige Erweiterungen müssen separat installiert werden, andere sind standardmäßig installiert.

## Installierte Erweiterungen

Es gibt einige Erweiterungen, die automatisch mit Adobe Commerce oder Magento Open Source installiert werden.

### [!DNL Inventory Management]

[!DNL Commerce] [[!DNL Inventory Management]](../inventory-management/introduction.md) bietet ein verbessertes Lager- und Versandmanagement an einem oder mehreren Standorten und über verschiedene Vertriebskanäle mit gleichzeitigem Checkout-Schutz und Algorithmen zum Abgleich von Sendungen. Verfolgen Sie Ihre Lagermengen, liefern Sie genaue verkaufbare Lagermengen an Kunden und versenden Sie gemäß Empfehlungen oder manueller Auswahl, um Ihren gesamten Bestand zu kontrollieren. Konfigurieren Sie Verwaltungseinstellungen global, pro Quelle und pro Produkt.

>[!NOTE]
>
>Diese Erweiterung wurde im Rahmen des Projekts [[!DNL Inventory Management]](https://github.com/magento/inventory) (ehemals MSI) durch das Community Engineering-Programm entwickelt.

[!DNL Inventory Management] wird mit allen standardmäßig aktivierten Funktionen installiert. Zur Aktivierung dieser Bestandsfunktionen sind keine zusätzlichen Schritte erforderlich. Weitere Informationen zu den [!DNL Inventory Management] finden Sie im [[!DNL Inventory Management] Benutzerhandbuch](../inventory-management/guide-overview.md).

### Braintree

PayPal und Gene Commerce entwickelten gemeinsam die offizielle Braintree-Erweiterung für Commerce 2.4.x Stores. Die Updates bieten ein verbessertes Checkout-Erlebnis zur Steigerung der Konversionsrate und beinhalten PayLater-Optionen, mit denen beim Einkaufen und beim Checkout automatisch relevante PayLater-Nachrichten und -Schaltflächen angezeigt werden.

Diese Erweiterung wird standardmäßig installiert, erfordert jedoch ein [Braintree-Konto](https://www.braintreepayments.com/) und die Konfiguration im Admin-Bereich, um für Ihren Store aktiviert zu werden. Um die Gebühren zu ermitteln, die bei der Verwendung von Braintree zur Verarbeitung Ihrer Transaktionen anfallen, überprüfen Sie die [Braintree-Preise](https://www.braintreepayments.com/braintree-pricing).

Informationen zur Braintree-Konfiguration in Admin finden Sie im [Braintree](../stores-purchase/braintree.md)-Thema im _Handbuch zu Vertrieb und Kauf_.

### Google reCAPTCHA

Google reCAPTCHA bietet ein höheres Maß an Sicherheit sowohl für die Storefront als auch für die Admin-Benutzeroberfläche als mit standardmäßigem CAPTCHA verfügbar ist und bietet Ihnen folgende Möglichkeiten:

- Überprüfen Sie, wann Kunden Konten erstellen, Kennwörter abrufen, sich bei ihren Konten anmelden oder sich an Ihr Unternehmen wenden.
- Erhöhen Sie die Sicherheit bei der Anmeldung von Admin-Benutzern.

Dadurch werden potenzielle Benutzerfehler bei der Eingabe eines CAPTCHA-Codes reduziert und die Konversion in den Warenkorb gefördert, ohne dass beim Checkout Hürden hinzugefügt werden. [Aktivieren und konfigurieren Sie reCAPTCHA](../systems/security-google-recaptcha.md) indem Sie unsichtbare oder interaktive Prüfungen verwenden, um den sicheren Zugriff auf die [!DNL Commerce] Admin- und Storefront zu verbessern.

### Zwei-Faktor-Authentifizierung

Der [!DNL Commerce] Admin bietet Zugriff auf alle Ihre Stores, Bestellungen und Kundendaten. [Zwei-Faktor-Authentifizierung](../systems/security-two-factor-authentication.md) (2FA oder TFA) erhöht die Sicherheit, indem eine zusätzliche Authentifizierung über den standardmäßigen Anmeldenamen und das Kennwort hinaus erforderlich ist, um von allen Geräten aus auf den [!DNL Commerce]-Administrator zuzugreifen. Die Erweiterung unterstützt mehrere Authentifizierer, einschließlich Google Authenticator, Authy, [!DNL Duo] und U2F-Schlüsseln. Diese Authentifizierung gilt nur für Admin-Benutzer. Sie ist nicht für Storefront-Kundenkonten verfügbar.

Diese Funktionen sind standardmäßig aktiviert. Jeder Admin-Benutzer muss einen der unterstützten Authentifikatoren installieren und konfigurieren.

>[!NOTE]
>
>In Adobe Commerce-Stores, in denen die Adobe Identity Management Services (IMS)-Authentifizierung für den Administrator aktiviert ist, ist das native Commerce 2FA deaktiviert. Benutzende, die mit ihren Adobe-Anmeldeinformationen bei Admin angemeldet sind, müssen sich für viele Administratoraufgaben nicht erneut authentifizieren. Die Authentifizierung wird von Adobe IMS durchgeführt, wenn sich der Administrator bei seiner aktuellen Sitzung anmeldet. Siehe Übersicht über die Integration von [Adobe Identity Management Service (IMS)](./adobe-ims-integration-overview.md).

## Hinzuzufügende Erweiterungen

Die [[!DNL Commerce Marketplace]](https://marketplace.magento.com/) ist die globale eCommerce-Ressource für Programme und Services, die [!DNL Commerce] Lösungen um leistungsstarke neue Funktionen erweitert. Adobe veröffentlicht mehrere Erweiterungen über die [!DNL Marketplace], die in Ihrem Adobe Commerce- oder Magento Open Source-Store installiert und konfiguriert werden können, um erweiterte Integrationen und Funktionen bereitzustellen.

### [!DNL Live Search]

![Nur Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce

Die [!DNL Live Search]-Erweiterung verbindet Ihren Store mit dem Live Search-Service - einer kostenlosen Suchplattform von Adobe Commerce, mit der Verkäufer nahtlos Kunden ein KI-optimiertes Sucherlebnis bieten können. Adobe Sensei, das auf der Adobe-Ebene mit künstlicher Intelligenz basiert, hilft Händlern, mit weniger Aufwand mehr zu erreichen, indem sie die manuelle Arbeit um das Facettieren/Filtern entfernen.

Weitere Informationen finden Sie [Live Search-](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/guide-overview.html)).

### [!DNL Product Recommendations]

![Nur Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce

Die [!DNL Product Recommendations]-Erweiterung verbindet Ihren Shop mit dem Produkt-Recommendations-Service - einem leistungsstarken Marketing-Tool, mit dem Sie Konversionen, Umsätze und Interaktionen steigern können. [!DNL Product Recommendations] wurde von Adobe Commerce entwickelt und wird von seiner kampferprobten künstlichen Intelligenz, Adobe Sensei, angetrieben, sodass Sie mit Zuversicht Interaktion und Konversion fördern können. Mit dieser Funktion entfällt die manuelle Arbeit, die erforderlich ist, um relevante Produktempfehlungen an jeden Käufer zu senden.

Weitere Informationen finden Sie [[!DNL Product Recommendations] Benutzerhandbuch](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/guide-overview.html?lang=en) .

### [!DNL Catalog Service]

Die [!DNL Catalog Service] ermöglicht es Ihnen, Kunden ein optimiertes Produkterlebnis zu bieten und gleichzeitig die Leistung zu steigern, die Skalierbarkeit zu verbessern und die Konversionen zu erhöhen. Weitere Informationen finden Sie [[!DNL Catalog Service] Benutzerhandbuch](https://experienceleague.adobe.com/docs/commerce-merchant-services/catalog-service/guide-overview.html) .

### [!DNL Payment Services]

[!DNL Payment services] für Adobe Commerce und Magento Open Source ist eine vollständig integrierte Zahlungslösung, die die Zahlungsverwaltung vereinfacht und Ihren Kunden die Möglichkeit gibt, ihren Zahlungsprozess mitzugestalten. So können Sie alle Zahlungs- und Transaktionsdaten innerhalb von Adobe Commerce Admin sicher abstimmen, sodass Sie Bestellungen und Zahlungen an einem Ort verwalten und gleichzeitig einen nahtlosen Checkout bieten können. Weitere Informationen finden Sie [[!DNL Payment Services] Benutzerhandbuch](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html) .

### [!DNL Store Fulfillment]

Store Fulfillment für Adobe Commerce und Magento Open Source ermöglicht einen hervorragenden Online-Einkauf, die Aufnahme im Geschäft (BOPIS)-Kundenerlebnis und maximiert die Mitarbeiterproduktivität durch Bereitstellung eines umfassenden Fulfillment-Workflows, der über ein Mobilgerät ermöglicht wird. Weitere Informationen finden Sie [[!DNL Store Fulfillment] Benutzerhandbuch](https://experienceleague.adobe.com/docs/commerce-merchant-services/store-fulfillment/guide-overview.html) .

### [!DNL Amazon Sales Channel]

Die [!DNL Amazon Sales Channel] für Adobe Commerce ermöglicht es Ihnen, Ihre Amazon Seller Central-Listendatenbank mit Ihrem [!DNL Commerce] Produktkatalog zu integrieren und Ihre Amazon-Listen und -Verkäufe in der Commerce Admin zu verwalten. Weitere Informationen finden Sie [[!DNL Amazon Sales] Benutzerhandbuch](https://experienceleague.adobe.com/docs/commerce-channels/amazon/guide-overview.html).

### [!DNL Channel Manager]

[!DNL Channel Manager] ermöglicht es Ihnen, durch die Integration eines Adobe Commerce- oder Magento Open Source-Produktkatalogs in den Walmart Marketplace den Umsatz zu steigern, neue Kunden zu erreichen, den Betrieb zu optimieren und Zeit zu sparen. Nach der Installation und Konfiguration der Erweiterung können Ihre Mitarbeiter Walmart Marketplace-Listen, Inventar, Bestellungen, Rücksendungen und Rückerstattungen nahtlos von der [!DNL Commerce Admin] aus verwalten. Weitere Informationen finden Sie [[!DNL Channel Manager] Benutzerhandbuch](https://experienceleague.adobe.com/docs/commerce-channels/channel-manager/guide-overview.html) .
