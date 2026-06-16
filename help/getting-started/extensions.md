---
title: Erweiterungen aus Adobe
description: Informationen zu Erweiterungen für Adobe Commerce und Magento Open Source, die von Adobe veröffentlicht wurden, finden Sie.
exl-id: 86338edc-c32a-41c8-9594-6aec26f53ac6
feature: Extensions
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
TQID: https://experienceleague.adobe.com/-QGqm0VMRlCNuKqHGdGVKjs8ZgNcjYZjFaeIFsOLWCA
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: c32adafa-ed01-4b31-997e-2413013911b0
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
subfeature_v2:
  - id: b01a71b7-d17a-42b2-a9ac-af4b8d9d2ef5
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: a09a5a04-e30b-4d55-b031-38e6f5ec86db
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: da3860b0-d637-47df-bef0-273751180266
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f5c2a4bb-71ca-4d7e-8efd-442250e6ba48
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 1434
ht-degree: 0%

---

# Erweiterungen aus Adobe

Dieser Abschnitt enthält Informationen zu PHP-Erweiterungen für Adobe Commerce und Magento Open Source, die von Adobe veröffentlicht werden.

Erweiterungen fügen Funktionen, Dienste und Integrationen zur Admin- und Storefront hinzu. Einige dieser Erweiterungen werden durch Beiträge der Magento Open Source-Community entwickelt. Einige Erweiterungen werden standardmäßig installiert, andere erfordern eine separate Installation.

+++Weitere Informationen zur Erweiterung von Adobe Commerce

Adobe bietet zwei Hauptansätze zum Erweitern oder Anpassen Ihrer Adobe Commerce-Projekte:

- Prozessinterne Erweiterbarkeit: Verwendet benutzerdefinierten Code und Erweiterungen, die innerhalb des Adobe Commerce-Anwendungsprozesses ausgeführt werden, wie PHP Extensions. Dieser herkömmliche Ansatz ermöglicht eine tiefgehende Integration, erfordert jedoch eine sorgfältige Verwaltung bei Upgrades.

- Out-of-process-Erweiterbarkeit: Verwendet benutzerdefinierten Code und Anwendungen, die unabhängig von der Kernsoftware arbeiten. Dieser moderne Ansatz hilft, die Gesamtbetriebskosten zu senken, indem:

   - Vereinfachte Upgrades, da Erweiterungen vom Kern entkoppelt sind
   - Mehr Kontrolle für Entwickler über den Zeitpunkt und die Methoden der Implementierung
   - Unabhängige Skalierung und Wartung von Erweiterungskomponenten

Adobe Commerce bietet Strategien und Tools zur Unterstützung beider Arten der Erweiterbarkeit. Weitere Informationen finden Sie unter [Erweiterbarkeit von Adobe Commerce](https://developer.adobe.com/commerce/extensibility/).

+++

## Standardmäßig installierte Adobe-Erweiterungen

Die folgenden Adobe-Erweiterungen sind in Adobe Commerce enthalten und werden automatisch mit dem Adobe Commerce-Programm installiert. Einige Erweiterungen müssen im Administrator weiter konfiguriert oder aktiviert werden, wie in der Beschreibung der Erweiterung angegeben.

### [!DNL Inventory Management]

[!DNL Commerce] [[!DNL Inventory Management]](../inventory-management/introduction.md) bietet ein verbessertes Lager- und Versandmanagement an einem oder mehreren Standorten und über verschiedene Vertriebskanäle mit gleichzeitigem Checkout-Schutz und Algorithmen zum Abgleich von Sendungen. Verfolgen Sie Ihre Lagermengen, liefern Sie genaue verkaufbare Lagermengen an Kunden und versenden Sie gemäß Empfehlungen oder manueller Auswahl, um Ihren gesamten Bestand zu kontrollieren. Konfigurieren Sie Verwaltungseinstellungen global, pro Quelle und pro Produkt.

>[!NOTE]
>
>Diese Erweiterung wurde im Rahmen des Projekts [[!DNL Inventory Management]](https://github.com/magento/inventory) (ehemals MSI) durch das Community Engineering-Programm entwickelt.

[!DNL Inventory Management] wird mit allen standardmäßig aktivierten Funktionen installiert. Zur Aktivierung dieser Bestandsfunktionen sind keine zusätzlichen Schritte erforderlich. Weitere Informationen zu den [!DNL Inventory Management] finden Sie im [[!DNL Inventory Management] Benutzerhandbuch](../inventory-management/guide-overview.md).

### Braintree

PayPal und Gene Commerce entwickelten gemeinsam die offizielle Braintree-Erweiterung für Commerce 2.4.x-Stores. Die Updates bieten ein verbessertes Checkout-Erlebnis zur Steigerung der Konversionsrate und beinhalten PayLater-Optionen, mit denen beim Einkaufen und beim Checkout automatisch relevante PayLater-Nachrichten und -Schaltflächen angezeigt werden.

Diese Erweiterung wird standardmäßig installiert, erfordert jedoch ein [Braintree-Konto](https://www.braintreepayments.com/) und die Konfiguration im Admin-Bereich, um für Ihren Store aktiviert zu werden. Um die Gebühren zu ermitteln, die bei der Verarbeitung Ihrer Transaktionen mit Braintree anfallen, überprüfen Sie die [Braintree-Preise](https://www.braintreepayments.com/braintree-pricing).

Informationen zur Braintree-Konfiguration in der Admin-Instanz finden Sie im [Braintree](../stores-purchase/braintree.md)-Thema im _Handbuch zu Vertriebs- und Kauferlebnissen_.

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

## Adobe-Erweiterungen, die installiert werden müssen

Adobe bietet zusätzliche Erweiterungen, die mit Composer separat installiert werden müssen. Diese Erweiterungen sind über verschiedene Kanäle verfügbar:

- Repository-Zugriff (repo.magento.com)

  Für die Installation der folgenden Erweiterungen sind die Kontobereitstellung und Anmeldeinformationen erforderlich. Wenden Sie sich an Ihren Adobe-Kundenbetreuer.

   - [Adobe Commerce B2B](#adobe-commerce-b2b)
   - [AEM Assets-Integration für Commerce](#assets-integration-for-commerce)

- Adobe Commerce Marketplace

  Die folgenden Adobe-Erweiterungen sind öffentlich unter [marketplace.magento.com](https://marketplace.magento.com) verfügbar. Diese Erweiterungen sind kostenlos erhältlich.

   - [Live Search](#live-search)
   - [Produkt Recommendations](#product-recommendations)
   - [Katalog-Service](#catalog-service)
   - [Zahlungsdienste](#payment-services)

### [!DNL Adobe Commerce B2B]

![Adobe Commerce](../assets/adobe-logo.svg) Nur Adobe Commerce, erfordert eine separate Lizenz.

[!DNL Adobe Commerce B2B] ist eine integrierte Erweiterung, die standardmäßige Commerce-Stores in umfassende Business-to-Business-Plattformen umwandelt. Es ermöglicht Unternehmen die Verwaltung komplexer Organisationsstrukturen mit mehreren Käufern, benutzerdefinierten Rollen und Kaufberechtigungen unter einheitlichen Unternehmenskonten. Zu den wichtigsten Funktionen gehören unternehmensspezifische Kataloge und Preise, verhandelbare Angebote, Bestellverwaltung, Anforderungslisten und Schnellbestellfunktionen. Die Lösung unterstützt sowohl B2B- als auch B2C-Modelle in einer einzigen Instanz, was sie flexibel für unterschiedliche Geschäftsanforderungen macht. Die Erweiterung erfordert eine separate Lizenz und lässt sich nahtlos in die Kernfunktionen von Adobe Commerce integrieren, um eine vollständige B2B-E-Commerce-Lösung zu bieten.

Wenden Sie sich für die Bereitstellung an Ihren Adobe-Kundenbetreuer. Implementierungsdetails und Konfigurationsschritte finden Sie im [[!DNL B2B for Adobe Commerce] Benutzerhandbuch](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html).

### [!DNL AEM Assets Integration for Commerce]

![Adobe Commerce](../assets/adobe-logo.svg) Nur Adobe Commerce erfordert auch Lizenzen für Adobe Experience Manager (AEM) Assets und AEM Dynamic Media.

[!DNL AEM Assets Integration for Commerce] verbindet Adobe Commerce mit dem DAM-System (Digital Asset Management) von Adobe Experience Manager, um eine zentralisierte Kontrolle über alle digitalen Assets zu ermöglichen. Diese Integration ermöglicht eine automatisierte Synchronisierung von Assets, Echtzeit-Aktualisierungen und eine effiziente Wiederverwendung von Inhalten in allen Commerce-Storefronts. Durch die Kombination der robusten Asset-Management-Funktionen von AEM mit Commerce profitieren Unternehmen von optimierten Workflows, konsistenten Markenerlebnissen und optimierter Medienbereitstellung durch Cloud-basierte Infrastruktur.

Wenden Sie sich für die Bereitstellung an Ihren Adobe-Kundenbetreuer. Implementierungsdetails und Konfigurationsschritte finden Sie im [[!DNL Assets Integration] Benutzerhandbuch](../content-design/aem-assets-integration.md).

### [!DNL Live Search]

![Nur Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce

Die Live-Suche ist eine exklusive Funktion von Adobe Commerce, die eine KI-gestützte Suchlösung mit Echtzeit-Suchfunktion nach dem „gewünschten“ Typ bietet. Es liefert schnelle, relevante Ergebnisse mit Produktminiaturen, während Käufer tippen, zusammen mit intelligenter Facettierung, die Filter automatisch an das Einkaufsverhalten anpasst. Die Lösung umfasst Merchandising-Funktionen für die Produktverbesserung und -vergütung, die Verwaltung von Synonymen und Suchanalysen. Adobe Commerce ist ohne zusätzliche Kosten im Lieferumfang enthalten [!DNL Live Search] ersetzt die standardmäßige Suchfunktion durch ein komplexeres SaaS-basiertes Sucherlebnis. Es erfordert nur eine minimale Konfiguration, um zu beginnen.

Details zur Implementierung und technische Anforderungen finden Sie im [Live Search-Benutzerhandbuch](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html).

### [!DNL Product Recommendations]

![Nur Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce

[!DNL Product Recommendations] ist eine exklusive Funktion von Adobe Commerce auf Basis der Adobe AI-Technologie, die personalisierte Produktvorschläge auf der gesamten Customer Shopping-Journey liefert. Die Lösung analysiert das Kundenverhalten und die Produktbeziehungen in Echtzeit, um automatisch relevante Empfehlungen zu generieren, ohne dass manuelle Merchandising-Regeln erforderlich sind. Dieser KI-gestützte Ansatz trägt dazu bei, Konversionsraten und Umsatzpotenziale zu steigern und gleichzeitig attraktivere Produkterlebnisse für Kunden zu schaffen.

Informationen zur Implementierung und Best Practices finden Sie im [[!DNL Product Recommendations] Benutzerhandbuch](https://experienceleague.adobe.com/docs/commerce/product-recommendations/overview.html).

### [!DNL Catalog Service]

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"} Installationen von Adobe Commerce und Magento Open Source

[!DNL Catalog Service] ist eine leistungsstarke Lösung für Adobe Commerce und Magento Open Source, die über GraphQL-Endpunkte optimierten Zugriff auf Katalogdaten bietet. Sie unterhält eine separate synchronisierte Datenbank für Produktdetails und zugehörige Informationen, wobei die direkte Anwendungskommunikation umgangen wird, um schnellere Seitenladezeiten zu erzielen. Der Service ist besonders für Produktdetailseiten, Kategorienlisten und Suchergebnisseiten nützlich, was ihn sowohl für herkömmliche als auch für Headless-Commerce-Implementierungen ideal macht.

Setup-Anweisungen und technische Details finden Sie im [[!DNL Catalog Service] Benutzerhandbuch](https://experienceleague.adobe.com/docs/commerce/catalog-service/guide-overview.html).

>[!NOTE]
>
>Katalog-Services werden automatisch installiert, wenn die Live Search oder die Produktempfehlungen aktiviert sind. Eine manuelle Installation ist nicht erforderlich.

### [!DNL Payment Services]

[!BADGE Unterstützt]{type=Informative tooltip="Unterstützt"} Installationen von Adobe Commerce und Magento Open Source

[!DNL Payment Services] ist eine schlüsselfertige Zahlungslösung für Adobe Commerce und Magento Open Source Stores, die umfangreiche Zahlungsabwicklungsfunktionen bietet. Der Service integriert sichere Zahlungs-Gateway-Funktionen mit integriertem Betrugsschutz und bietet mehrere Zahlungsoptionen, einschließlich Kredit-/Debitkarten, PayPal, Venmo (US) und PayLater-Pläne. Sie bietet einheitliche Transaktionsberichte und ein einheitliches Auftragsmanagement über die Commerce Admin Interface, sodass Händler Zahlungen einfach verfolgen, Cashflows verwalten und Finanzdaten an einem Ort abstimmen können.

Detaillierte Konfigurationsschritte und Zahlungsoptionen finden Sie im [[!DNL Payment Services] Benutzerhandbuch](https://experienceleague.adobe.com/en/docs/commerce/payment-services/overview).
