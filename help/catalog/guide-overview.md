---
title: Handbuch zur Katalogverwaltung
description: Umfassende Informationen zu den Funktionen des Produktkatalogs für Admins von Adobe Commerce und Magento Open Source sowie E-Commerce-Händler.
seo-title: Adobe Commerce Catalog Management Guide
seo-description: Describes how to use the product catalog features for Adobe Commerce and Magento Open Source.
exl-id: 894b7cc3-8dc5-43aa-ab9c-ebc6480c7b2f
TQID: https://experienceleague.adobe.com/HJiD3cpDixdbHlBXmMhkHpEd40eyjEfNBu3MzEDhBL0
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
    internal-label: Catalog management
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
subfeature_v2:
  - id: e91a50b1-0b31-436e-9033-00e4776e94cb
    internal-label: Categories
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
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: c425649d00a0a57f84ce4042d33f6d0c5eabe99c
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 3%
---
# Handbuch zur Katalogverwaltung in Adobe Commerce

Dieses Handbuch richtet sich an Produkt-Merchandiser und Inventar-Manager, die in der Adobe Commerce und Magento Open Source Admin arbeiten. Es enthält detaillierte Informationen zu den Funktionen des Produktkatalogs, einschließlich der Erstellung der Navigationsstrukturen für einen Katalog. Es setzt ein grundlegendes Verständnis der [!DNL Commerce] Konfiguration und Funktionalität voraus.

Dieses Handbuch behandelt Folgendes:

| Subjekt | Beschreibung |
| ------- | ----------- |
| [Einführung](introduction.md) | Übersicht über die Verwendung der Funktionen zur Katalogverwaltung, um widerzuspiegeln, wie Kunden Produkte in Ihrem Geschäft finden sollen. |
| [Menü Katalog](catalog-menu.md) | Verwenden Sie das Menü [!UICONTROL Catalog] , um auf mehrere Funktionen zum Verwalten von Katalogen, Kategorien und Produkten für Ihren Store zuzugreifen. |
| [Katalog- und Produkt-URLs](catalog-urls.md) | Überprüfen Sie die grundlegenden URL-Typen und wie Sie Ihre URLs entwerfen können, um die Suchmaschinenoptimierung zu maximieren. |
| [Katalognavigation](navigation.md) | Verwenden Sie die Navigations-Tools, um zu definieren, wie Ihre Kunden im gesamten Store von Seite zu Seite wechseln. |
| [Katalogsuche](search.md) | Überprüfen Sie die Tools, mit denen Kunden Produkte in der Storefront finden können, und konfigurieren Sie das Sucherlebnis entsprechend Ihrem Produktkatalog. |
| [Kategorien](categories.md) | Legen Sie die grundlegende Kategoriestruktur Ihres Katalogs so fest, dass das Kundenerlebnis in Ihrer Storefront optimiert wird. |
| [Produkte](products-list.md) | Erstellen Sie Produkte von einfach bis komplex mit mehreren Optionen, Farbfeldern und anpassbaren Bundles. Erstellen Sie herunterladbare Produkte und virtuelle Produkte für Dienstleistungen und andere nicht greifbare Elemente. |
| [Freigegebene Kataloge](../b2b/enable-basic-features.md) | Gemeinsame Kataloge ermöglichen es Händlern, verschiedene Unternehmen kuratierte Produktsortimente und benutzerdefinierte Preise anzubieten. Erfordert die Lizenzierung und Konfiguration von Adobe Commerce B2B, einschließlich Unternehmenskonten und Funktionen für den freigegebenen Katalog. |
| [Kataloganreicherung](catalog-enrichment.md) | Überprüfen und wenden Sie die von KI vorgeschlagenen Verbesserungen an Produktnamen und -beschreibungen an, damit Ihr Katalog in LLM und der KI-unterstützten Erkennung korrekt dargestellt wird. |
| [Produktattribute](product-attributes.md) | Erstellen Sie Attribute mit Eingabesteuerelementen für Produktoptionen und um zusätzliche Informationen auf Produktseiten bereitzustellen. |
| [Nur Katalogansichten](../optimizer/setup/catalog-view.md) [!BADGE SaaS]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce as a Cloud Service- und Adobe Commerce Optimizer-Projekte (von Adobe verwaltete SaaS-Infrastruktur)."} | Für Commerce-Bereitstellungen mit Merchandising Services und dem Composable Catalog Data Model (CCDM) definieren Sie die Produkte und Preise, die ein Kunde abrufen kann, indem Sie Katalogquellen, Katalogebenen, Richtlinien und Preislisten für jede Marke, Region, Geschäftseinheit oder jeden Kanal kombinieren. Optional können Sie die Katalogansicht einschränken, um sie privat zu machen. |
| [Richtlinien](../optimizer/setup/policies.md) [!BADGE nur SaaS]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce as a Cloud Service- und Adobe Commerce Optimizer-Projekte (von Adobe verwaltete SaaS-Infrastruktur)."} | Für Commerce-Bereitstellungen mit CDM definieren Sie die Datenzugriffsfilter, die steuern, welche Produkte jede Katalogansicht bereitstellt, sodass der richtige Inhalt an das richtige Ziel gesendet wird. |

{style="table-layout:auto"}

>[!TIP]
>
>Adobe Commerce B2B bietet Ihnen die Möglichkeit, freigegebene Gated-Kataloge mit benutzerdefinierten Preisen für verschiedene Unternehmen zu verwalten. Zusätzlich zum standardmäßigen, primären Produktkatalog bietet sie dem Kunden Zugriff auf zwei Arten von freigegebenen Katalogen mit unterschiedlichen Preisstrukturen. Weitere Informationen zur Funktion „Freigegebener Katalog“ finden Sie im [Adobe Commerce B2B-Benutzerhandbuch](../b2b/catalog-shared.md).

## Verfügbare Dokumentation

{{docs-links}}
