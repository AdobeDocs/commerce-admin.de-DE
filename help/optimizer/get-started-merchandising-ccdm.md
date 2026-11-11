---
title: Katalog-Merchandising-Aufgaben nach Rolle
description: Hier finden Sie Anleitungen zu Aufgaben für Administratoren, Entwickler und Merchandiser, die mit mit CCDM bereitgestellten Adobe Commerce as a Cloud Service-Instanzen arbeiten.
role: Admin, Developer
recommendations: noCatalog
badgeSaas: label="Nur SaaS" type="Positive" url="https://experienceleague.adobe.com/de/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce as a Cloud Service-Instanzen, die mit CCDM bereitgestellt werden (von Adobe verwaltete SaaS-Infrastruktur)."
TQID: 'https://experienceleague.adobe.com/0PmobUkdEWspxuRSaIPL8vS1ojDDZ3gw-L-3SfPmJAg'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: de2e2e68-c5d7-4efe-be7b-27528698f06b
    internal-label: Commerce as a Cloud Service
feature_v2:
  - id: cc04bd17-78d5-5120-8c3d-1b8a57e49280
    internal-label: Integration
  - id: dec06508-d41f-555a-87e8-29e8bcdfa95a
    internal-label: Recommendations
  - id: e8818fe6-9c8b-4bc0-9ef8-377a10b7bc75
    internal-label: Architecture
  - id: f37757d8-3174-5335-b977-1161792f965d
    internal-label: Personalization
subfeature_v2:
  - id: f8ddfd3b-6194-46e8-a176-0e918039be56
    internal-label: Cloud architecture
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: dba482e5-29a8-4127-afa2-c4b913512ef8
    internal-label: Data and analytics
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
    internal-label: Data integration
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: 742236e7fdb26c56a80f66a44b0a4960210f4dac
workflow-type: tm+mt
source-wordcount: '548'
ht-degree: 0%
---

# Katalog-Merchandising-Aufgaben nach Rolle

Verwenden Sie diese Aufgabenreferenz, um Anleitungen zum Konfigurieren von Katalogdaten, zum Integrieren der Storefront, zum Verwalten von Merchandising und zum Überprüfen der Leistung in Adobe Commerce as a Cloud Service-Instanzen zu finden, die mit dem Composable Catalog Data Model (CCDM) bereitgestellt werden.

Die Zuständigkeiten variieren je nach Implementierung. In den folgenden Abschnitten werden Aufgaben nach den Rollen gruppiert, die sie normalerweise ausführen.

- Administratoren verwalten Produkte, Preise und B2B-Konfigurationen in Commerce Foundation.
- Entwickler konfigurieren die Storefront-Integration und überprüfen Kataloganfragen und die Erfassung von Verhaltensdaten.
- Merchandising-Experten konfigurieren Produkterkennung und Empfehlungen und verwenden Reporting, um Merchandising-Entscheidungen zu beeinflussen.

Produkt- und Preisdaten werden über die native Adobe Commerce as a Cloud Service-Integration mit dem CDM synchronisiert. Es ist keine separate Connector-Installation oder App Builder-App erforderlich.

## Katalog und Storefront vorbereiten

Schließen Sie die Aufgaben ab, die für Ihre Implementierung gelten. B2C-Katalogansichten können manuell erstellt werden. B2B-Katalogansichten, Richtlinien und Preislisten werden aus der B2B-Konfiguration in Commerce Foundation generiert.

| Aufgabe | Beschreibung | Ressourcen |
| --- | --- | --- |
| **Produkte und Preise konfigurieren** | Produkte und Preise in Commerce Foundation verwalten. Preisdaten werden mit CCDM als Preiskataloge synchronisiert. Erstellen Sie keine Preise unabhängig in CCDM. | [Produktliste](../catalog/products-list.md), [Produkt erstellen](../catalog/product-create.md), [Preisbereich](../catalog/catalog-price-scope.md) und [Erweiterte Preise](../catalog/pricing-advanced.md) |
| **Store-Ansichten konfigurieren** | Konfigurieren Sie die Store-Ansichten und lokalisierten Produktdaten, die für Ihre Storefront in Commerce Foundation erforderlich sind. | [Ansichten speichern](../stores-purchase/store-views.md) |
| **Einrichten von freigegebenen B2B-Katalogen und -Unternehmen** | Konfigurieren Sie bei B2B-Implementierungen freigegebene Kataloge und Unternehmensbeziehungen in Commerce Foundation, bevor Sie die generierte Katalogkonfiguration überprüfen. | [Freigegebene Kataloge](../b2b/catalog-shared.md) und [Firmen](../b2b/account-companies.md) |
| **Konfigurieren von B2C-Katalogansichten und -Richtlinien** | Erstellen Sie Katalogansichten und wählen Sie die Richtlinien aus, die das verfügbare Produktsortiment definieren. Ordnen Sie jeder Ansicht die entsprechenden synchronisierten Preislisten zu. | [Katalogansichten](./setup/catalog-view.md) |
| **B2B-Katalogansichten überprüfen** | Vergewissern Sie sich, dass die native Synchronisierung die erwarteten Katalogansichten, Richtlinien und Preislisten generiert hat. Verwalten Sie die zugrunde liegende B2B-Konfiguration in Commerce Foundation, anstatt doppelte Strukturen manuell zu erstellen. | [B2B-Katalogansichten](./setup/catalog-view.md#b2b-catalog-views) |
| **Konfigurieren der Storefront** | Konfigurieren Sie die Storefront, um den gewünschten Katalogkontext anzufordern. Für benutzerdefinierte oder andere Storefront-Integrationen überprüfen Sie die entsprechenden Kopfzeilen für Kataloganfragen. | [Storefront-Konfiguration](https://experienceleague.adobe.com/en/tools/commerce-storefront/setup/configuration/commerce-configuration/) |

Bevor Sie Merchandising konfigurieren, überprüfen Sie, ob die Storefront die erwarteten Produkte und Preise zurückgibt. Testen Sie das Hinzufügen zum Warenkorb, den Warenkorb und den Checkout, um sicherzustellen, dass die Transaktionskosten mit der beabsichtigten Commerce Foundation-Konfiguration übereinstimmen.

## Merchandising konfigurieren und Leistung überprüfen

| Aufgabe | Beschreibung | Ressourcen |
| --- | --- | --- |
| **Produkterkennung konfigurieren** | Richten Sie Merchandising-Regeln, Facetten und Synonyme ein. Regeln können für alle Katalogansichten gelten oder auf eine bestimmte Ansicht zugeschnitten sein. | [Merchandising - Übersicht](./merchandising/overview.md) |
| **Sucheinstellungen überprüfen** | Überprüfen Sie die Suchkonfiguration und die verfügbaren semantischen Suchoptionen für Ihre Implementierung. | [Merchandising-Einstellungen](./settings.md) und [Semantische Suche](./setup/semantic-search.md) |
| **Empfehlungen konfigurieren** | Erstellen Sie Empfehlungseinheiten und überprüfen Sie, ob die Storefront die für die Implementierung erforderlichen Verhaltensdaten erfasst. | [Recommendations - Übersicht](./merchandising/recommendations/overview.md) |
| **Leistung überprüfen** | Verwenden Sie Erfolgsmetriken und Berichte zur Suchleistung, um die Storefront-Aktivität zu bewerten und in Merchandising-Entscheidungen einfließen zu lassen. | [Erfolgsmetriken](./manage-results/success-metrics.md) und [Suchleistung](./manage-results/search-performance.md) |

## Nächste Schritte

Nach der Konfiguration von Merchandising und der Überprüfung der Leistung sollten Sie Ihre Regeln, Facetten und Empfehlungen weiterhin überwachen und nach Bedarf anpassen, um das Erlebnis in der Storefront zu optimieren.
