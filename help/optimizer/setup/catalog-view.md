---
title: Katalogansichten
description: Erfahren Sie, was Katalogansichten sind und wie Sie sie erstellen, um Ihren Produktkatalog nach Geschäftsstruktur, Richtlinien und Preisen zu organisieren.
role: Admin, Developer
recommendations: noCatalog
badgeSaas: label="Nur SaaS" type="Positive" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce as a Cloud Service-Instanzen, die mit CCDM bereitgestellt werden (von Adobe verwaltete SaaS-Infrastruktur)."
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: de2e2e68-c5d7-4efe-be7b-27528698f06b
    internal-label: Commerce as a Cloud Service
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: 8fbcfcdeb13c452a45e872d939e129703ac5abab
workflow-type: tm+mt
source-wordcount: '997'
ht-degree: 0%
---

# Katalogansichten

Eine Katalogansicht definiert die Produkte und Preise, die eine Storefront abrufen kann. In Adobe Commerce as a Cloud Service-Instanzen, die mit dem Composable Catalog Data Model (CCDM) bereitgestellt werden, verwenden Katalogansichten dieselbe Kataloggrundlage, die auch Adobe Commerce Optimizer unterstützt.

Katalogansichten kombinieren Katalogquellen, Richtlinien und Preisbücher, um den Katalogkontext einer Storefront zu definieren. Richtlinien bestimmen das verfügbare Sortiment. Merchandising-Regeln steuern, wie Produkte innerhalb dieses Sortiments beworben und eingestuft werden. Sie können für alle Katalogansichten gelten oder auf eine bestimmte Ansicht zugeschnitten werden. Siehe [Erstellen einer Merchandising-Regel](../merchandising/rules/add.md).

Commerce Foundation bleibt die wahre Quelle für Produkte und Preise. Produkt- und Preisdaten werden über die native Adobe Commerce as a Cloud Service-Integration auf eine Weise mit dem CDM synchronisiert, ohne dass ein separater Connector oder eine App Builder-App installiert werden müssen. Die Konfiguration von Websites, Stores und Store-Ansichten verbleibt in Commerce Foundation, die auch Warenkorb, Checkout, Werbeaktionen, Kunden, Bestellungen und Zahlungen verwaltet.

>[!NOTE]
>
>Verwenden Sie für mit CCDM bereitgestellte Instanzen [Commerce Admin in Adobe Unified Experience](../../getting-started/admin-unified-experience.md), um Katalogansichten und Richtlinien zu konfigurieren und synchronisierte Preislisten mit Katalogansichten zu verknüpfen. Instanzen, die den Katalog-Service mit Live Search und Product Recommendations verwenden, haben keinen Zugriff auf diese Katalogverwaltungs-Bildschirme.

## Funktionsweise von Katalogansichten

Eine Katalogansicht fasst Katalogdaten und -konfigurationen für einen Storefront-Kontext zusammen. Sie kann zur Darstellung einer Geschäftseinheit, Marke, Region oder eines anderen Storefront-Erlebnisses verwendet werden.

- **[Katalogquellen](catalog-sources.md)** stellen Produktdaten für Katalogerlebnisse bereit.
- **[Richtlinien](policies.md)** Filtern von Produktdaten für eine Katalogansicht.
- **[Preisverzeichnisse](pricebooks.md)** liefern Preisdaten, die mit einer Katalogansicht verknüpft sind.

Katalogansichten ersetzen nicht die Website-, Store- und Store-Ansichtsstruktur in Adobe Commerce as a Cloud Service. Commerce Foundation verwaltet diese Struktur und die Transaktionsvorgänge weiterhin.

Katalogdaten werden von Commerce Foundation in CCDM auf eine Weise synchronisiert. CCDM unterstützt Storefront-Katalogerlebnisse und die Produkterkennung. Commerce Foundation bearbeitet weiterhin Warenkorb, Checkout, Promotions, Kunden und Bestellungen.

## Bevor Sie beginnen

Vor dem Konfigurieren einer Katalogansicht:

- [Bestätigen Sie, dass die Adobe Commerce as a Cloud Service-Instanz CCDM verwendet](../overview.md).
- Bestätigen Sie, dass die für die Storefront erforderlichen Katalogdaten ausgefüllt und [synchronisiert](data-sync.md) wurden.
- Identifizieren Sie die [Katalogquelle](catalog-sources.md), [Richtlinien](policies.md) und [Preisbücher](pricebooks.md), die für den Kontext der Storefront benötigt werden.
- Legen Sie fest, ob Sie B2C-Katalogansichten manuell erstellen oder B2B-Katalogansichten überprüfen müssen, die durch native Synchronisierung generiert wurden.

>[!NOTE]
>
>Bei B2B-Implementierungen generiert die native Synchronisierung Katalogansichten, Richtlinien und Preisverzeichnisse aus der B2B-Konfiguration in Commerce Foundation. Duplikate dieser automatisch generierten Strukturen dürfen nicht manuell erstellt werden.

## Erstellen einer Katalogansicht für eine B2C-Implementierung

Verwenden Sie diesen Workflow, wenn die B2C-Implementierung erfordert, dass Katalogansichten manuell konfiguriert werden.

1. Melden Sie sich beim [Commerce-Administrator in Unified Experience](../../getting-started/admin-unified-experience.md) an und wählen Sie die mit CCDM bereitgestellte Adobe Commerce as a Cloud Service-Instanz aus.
1. Navigieren Sie in der linken Navigation zu **[!UICONTROL Catalog]** > **[!UICONTROL Catalog Views]**.
1. Wählen Sie **[!UICONTROL Create catalog view]** aus.
1. Geben Sie einen Namen für die Katalogansicht ein.
1. Wählen Sie die [Katalogquelle(n](catalog-sources.md) für den Storefront-Kontext aus.
1. Verknüpfen Sie die entsprechenden [Richtlinien](policies.md) mit der Katalogansicht.
1. Ordnen Sie die entsprechenden Preislisten der Katalogansicht zu, indem Sie [Preisbuchverfügbarkeit konfigurieren](pricebooks.md).
1. Erstellen Sie die Katalogansicht.

## B2B-Katalogansichten

Bei B2B-Implementierungen generiert die native Synchronisierung Katalogansichten, Richtlinien und Preisverzeichnisse aus der B2B-Konfiguration in Commerce Foundation. Verwalten des zugrunde liegenden B2B-Katalogs und der Unternehmensbeziehungen in Commerce Foundation, anstatt manuell doppelte Strukturen in CCDM zu erstellen.

Anweisungen zum Einrichten finden Sie unter [Erstellen eines freigegebenen Katalogs](../../b2b/catalog-shared-create.md) und [Zuweisen von Unternehmen zu einem freigegebenen Katalog](../../b2b/catalog-shared-assign-companies.md).

Nach der Konfiguration der B2B-Beziehungen:

1. Bestätigen Sie, dass [Synchronisierung](data-sync.md) abgeschlossen ist.
2. Überprüfen Sie die generierten Katalogansichten, [Richtlinien](policies.md) und [Preisbücher](pricebooks.md) in [Commerce Admin in Unified Experience](../../getting-started/admin-unified-experience.md).
3. Überprüfen Sie, ob die Storefront das erwartete Produktsortiment und die erwarteten Preise für das Unternehmen anzeigt.
4. Testen Sie das Produkt in den Warenkorb, den Warenkorb und die Kasse, um zu bestätigen, dass die Produktverfügbarkeit und die Transaktionspreise mit der beabsichtigten B2B-Konfiguration übereinstimmen.

## Preisbücher und Checkout

Preisverzeichnisse enthalten die Preisdaten, die über eine Katalogansicht verfügbar sind. In Adobe Commerce as a Cloud Service bleibt die Commerce Foundation die wahre Quelle für Preise. Die Preisdaten werden durch native Integration mit dem CDM synchronisiert. Verwenden Sie beim Konfigurieren einer Katalogansicht die entsprechenden synchronisierten Preisverzeichnisse, anstatt Preise unabhängig in CDM zu erstellen.

Der Warenkorb und die Kasse verwenden Commerce Foundation-Preise. Überprüfen Sie, ob die angezeigten Storefront-Preise mit den geltenden Warenkorb- und Checkout-Preisen übereinstimmen.

## Überprüfen und Validieren einer Katalogansicht

Nachdem Sie eine Katalogansicht konfiguriert haben, überprüfen Sie das vollständige Storefront-Erlebnis:

- Überprüfen Sie, ob die gewünschten Katalogdaten [synchronisiert](data-sync.md) sind.
- Vergewissern Sie sich, dass die Katalogansicht mit den beabsichtigten [Richtlinien](policies.md) und [Preisbüchern](pricebooks.md) verknüpft ist.
- Überprüfen Sie, ob die Storefront das erwartete Produktsortiment zurückgibt.
- Überprüfen Sie die angezeigten Preise anhand der entsprechenden Commerce Foundation-Preise.
- Testen Sie „Zum Warenkorb hinzufügen“, „Warenkorb“ und „Zur Kasse“.

Bestätigen Sie bei B2B-Implementierungen auch, dass die durch die Synchronisierung generierten Katalogstrukturen mit der beabsichtigten Unternehmens- und Katalogkonfiguration übereinstimmen.

## Fehlerbehebung

### In der Storefront fehlen Produkte

- [Bestätigen Sie, dass die Instanz CCDM verwendet](../overview.md).
- Bestätigen Sie, dass die Katalogdaten [synchronisiert](data-sync.md) sind.
- Vergewissern Sie sich, dass die Storefront den vorgesehenen Katalogkontext verwendet.
- Überprüfen Sie die [Richtlinien](policies.md), die mit der Katalogansicht verknüpft sind.

### Der angezeigte Preis ist unerwartet

- Bestätigen Sie, dass das [Preisbuch](pricebooks.md) mit der Katalogansicht verknüpft ist.
- Überprüfen Sie, ob die Preisdaten [synchronisiert](data-sync.md) und mit Commerce Foundation konsistent sind.

  Siehe [Preisverzeichnisse](pricebooks.md) für die Preiszuordnungen von Websites und Kundengruppen.

- Überprüfen Sie den Preis erneut im Warenkorb und an der Kasse.

### CDM-Katalogbildschirme sind in Commerce Admin nicht sichtbar

[Bestätigen Sie, dass die ausgewählte Instanz CCDM verwendet ](../overview.md) dass Sie in Unified Experience auf [Commerce Admin zugreifen](../../getting-started/admin-unified-experience.md). Eine Instanz, die Catalog Services v1 ausführt, verfügt nicht über die CCDM-Administrationsbildschirme.

## Verwandte Inhalte

- [Erste Schritte mit Adobe Commerce as a Cloud Service](https://experienceleague.adobe.com/en/docs/commerce/cloud-service/getting-started)
- [Übersicht über den freigegebenen Adobe Commerce B2B-Katalog](../../b2b/catalog-shared.md)
- [Versionshinweise zu Adobe Commerce as a Cloud Service](https://experienceleague.adobe.com/en/docs/commerce/cloud-service/release-notes)
- [Katalogsynchronisierung](data-sync.md)
