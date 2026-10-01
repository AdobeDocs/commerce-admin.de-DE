---
title: Handbuch zu [!DNL Adobe Commerce B2B]
description: Umfassende Informationen für [!DNL Adobe Commerce B2B], einschließlich Installation und Konfiguration.
breadcrumb-title: Handbuch-Übersicht
seo-title: "[!DNL Adobe Commerce B2B] Guide"
seo-description: Describes how to use the B2B features module in Adobe Commerce.
exl-id: 8a7fda1d-0040-48fe-b393-9244adca6fde
feature: B2B
TQID: https://experienceleague.adobe.com/DmVKfLqoxDuPtYvrvZ7a8Mkt2hz4eCFALej-ie2tafk
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: e8818fe6-9c8b-4bc0-9ef8-377a10b7bc75
    internal-label: Architecture
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
    internal-label: Reporting
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
    internal-label: B2B
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 9ce6906c107bd91a980e9e522e454452b7fca6f8
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 0%
---
# Adobe Commerce B2B-Handbuch

Dieses Handbuch richtet sich an Administratoren, die in Adobe Commerce Admin arbeiten. Es enthält detaillierte Informationen zur Installation und Aktivierung dieses Moduls, einschließlich Konfiguration und Verwaltung seiner Funktionen. Es setzt ein grundlegendes Verständnis der [!DNL Commerce] Konfiguration und Funktionalität voraus.

Für Store-Administratoren gibt es zwei Bereiche:

- Der Administrator: Verwenden Sie diesen Bereich, um auf die Konfigurations-Benutzeroberfläche und Berichte zuzugreifen.
- [!BADGE Nur PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."} Die Befehlszeilenschnittstelle: Verwenden Sie dieses Tool, um Installations- und Backend-Konfigurationsaufgaben auszuführen.

Dieses Handbuch behandelt Folgendes:

| Subjekt | Beschreibung |
| ------- | ----------- |
| [Einführung](introduction.md) | Welche Funktionen sind bei [!DNL Adobe Commerce B2B] verfügbar? |
| [Versionshinweise](release-notes.md) | Überprüfen Sie die in den einzelnen [!DNL Adobe Commerce B2B] Versionen bereitgestellten Aktualisierungen. |
| [Installieren](install.md) | [!BADGE Nur PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."} Installieren Sie die [!DNL Adobe Commerce B2B]. |
| [Aktivieren der grundlegenden B2B-Funktionen](enable-basic-features.md) | Nach der Installation von [!DNL Adobe Commerce B2B] müssen Sie die Funktionen aktivieren, die Sie für Ihren Store aktivieren möchten. |
| [Unternehmenskonten](account-companies.md) | Erfahren Sie mehr über Unternehmenskonten und darüber, wie sie den Hauptbaustein für die Unterstützung von B2B-Käufern in Ihrem Geschäft darstellen. |
| [Unternehmensführung](manage-companies.md) | Erfahren Sie, wie Administratoren von B2B-Commerce-Websites Unternehmenshierarchien erstellen können, um die Verwaltung mehrerer Unternehmen zu optimieren, die zum selben Unternehmen gehören. |
| [freigegebene Kataloge](catalog-shared.md) | Erfahren Sie, wie Sie freigegebene Kataloge verwenden, um private Kataloge mit benutzerdefinierten Preisen für verschiedene Unternehmen zu verwalten. Erfahren Sie, wie Sie für Kunden mit dem [!DNL Adobe Commerce Optimizer Connector for B2B] freigegebene B2B-Kataloge synchronisieren können, um sie mithilfe erweiterter Merchandising-Funktionen als private Katalogansichten zu [!DNL Adobe Commerce Optimizer] und Storefront-Erlebnisse zu verbessern. |
| [Schnellbestellungen](quick-order.md) | Erfahren Sie mehr über die Schnellbestellungsfunktion und deren Aktivierung für Ihre Kunden. |
| [Bestellungen](purchase-order-flow.md) | Erfahren Sie mehr über Auftrags-Workflows, mit denen Unternehmen ihre Ausgaben verfolgen und kontrollieren können. |
| [Anführungszeichen](quotes.md) | Erfahren Sie mehr über Angebots-Workflows und wie Sie diesen Service für Ihre Unternehmenskonten bereitstellen können. |
| [Anforderungslisten](requisition-lists.md) | Erfahren Sie mehr über Anforderungslisten und wie sie verwendet werden, um häufig bestellte Produkte einfach zum Warenkorb hinzuzufügen. |

{style="table-layout:auto"}

## Zusätzliche Dokumentation

{{docs-links}}

## Entwicklerinformationen

Informationen zu den in den Modulversionen enthaltenen Änderungen finden Sie in den [Versionshinweisen](release-notes.md). Die [B2B-Integrationen](https://developer.adobe.com/commerce/webapi/rest/b2b/) Dokumentation im _Adobe Commerce REST-API-Referenzhandbuch_ enthält Details zur Modularchitektur, zu APIs und zur Algorithmusanpassung.

## Fehlerbehebung und Support

Wenn Sie Informationen benötigen oder Fragen haben, die in diesem Handbuch nicht behandelt werden, verwenden Sie die folgenden Ressourcen:

- [Adobe Commerce Support-Wissensdatenbank](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/overview)
- [Support-](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-help-center-user-guide#support-case): Senden Sie ein Ticket, um zusätzliche Hilfe zu erhalten.
