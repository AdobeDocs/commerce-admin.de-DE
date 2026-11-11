---
title: Übersicht über Merchandising-Services
description: Erfahren Sie mehr über Katalogkonfigurations-, Merchandising-, Berichts- und Überwachungs-Tools für Adobe Commerce as a Cloud Service-Instanzen, die mit CCDM bereitgestellt werden.
recommendations: noCatalog
badgeSaas: label="Nur SaaS" type="Positive" url="https://experienceleague.adobe.com/de/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce as a Cloud Service-Instanzen, die mit CCDM bereitgestellt werden (von Adobe verwaltete SaaS-Infrastruktur)."
exl-id: f9516d4c-fbae-4db2-a1a9-cda3684a8122
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: de2e2e68-c5d7-4efe-be7b-27528698f06b
    internal-label: Commerce as a Cloud Service
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: a6a5a899ba60097bd6baf2a5de14063a0af2f313
workflow-type: tm+mt
source-wordcount: '710'
ht-degree: 0%
---
# Übersicht über Merchandising-Services mit CCDM

Adobe Commerce as a Cloud Service-Instanzen, die mit dem Composable Catalog Data Model (CCDM) bereitgestellt werden, bieten Katalogkonfigurations-, Merchandising-, Berichts- und Überwachungs-Tools in [Commerce Admin in Adobe Unified Experience](../getting-started/admin-unified-experience.md). CCDM ist dieselbe Kataloggrundlage, die auch Adobe Commerce Optimizer unterstützt.

Mit Merchandising-Services können Sie:

- Verwenden Sie Katalogdaten aus Ihrer Adobe Commerce as a Cloud Service-Instanz, um Storefront-Erlebnisse zu unterstützen.
- Konfigurieren Sie Katalogansichten und Richtlinien, um Storefront-Produktsortimente zu definieren.
- Wenden Sie Merchandising-Regeln auf alle Katalogansichten an oder passen Sie sie an eine bestimmte Ansicht an.
- Konfigurieren Sie Produktempfehlungen, Suchfacetten und Synonyme.
- Überprüfen Sie die Leistung der Storefront durch Erfolgsmetriken und Suchleistungsberichte.
- Überwachen der Katalogsynchronisierung und der erfassten Storefront-Ereignisse.

Commerce Foundation bleibt die Quelle der Wahrheit für Produkte und Preise und verwaltet weiterhin Warenkorb-, Checkout- und andere Transaktionsvorgänge.

## Schneller Überblick

>[!BEGINTABS]

>[!TAB Katalogkonfiguration]

Konfigurieren des Katalogkontexts, der für eine Storefront verfügbar ist

- **Katalogansichten** - Kombinieren Sie Katalogquellen, Richtlinien und Preisbücher, um die Produkte und Preise zu definieren, die eine Storefront abrufen kann. Siehe [Katalogansichten](./setup/catalog-view.md).
- **Katalogebenen** - Überschreiben ausgewählter Produktattribute, ohne die Quelldaten zu ändern. Bei Verwendung von AEM Assets für Produktbilder wird die AEM-Assets-Ebene über Produktvisualisierungen angewendet. Siehe [Katalogebenen](./setup/catalog-layer.md).
- **Private Katalogansichten** - Aktivieren Sie den Katalogschutz, um ein gültiges signiertes Token zum Abrufen der Daten einer Katalogansicht anzufordern. Siehe [Private Katalogansichten](./setup/private-catalog-view.md).

>[!TAB Richtlinien]

Richtlinien filtern die verfügbaren Produkte über eine Katalogansicht basierend auf Produktattributen. Beispielsweise kann eine Richtlinie ein Sortiment auf eine bestimmte Marke oder Produktkategorie beschränken.

Richtlinien bestimmen das verfügbare Sortiment. Sie ersetzen nicht den Katalogschutz, der den Zugriff auf eine private Katalogansicht steuert.

>[!TAB Merchandising]

Konfigurieren Sie, wie Käufer Produkte entdecken und wie Produkte innerhalb des verfügbaren Sortiments beworben werden.

- **Opportunities** - Überprüfen Sie die Produktleistung, das Kundenverhalten und die Suchtrends, um Bereiche für Merchandising-Verbesserungen zu identifizieren.
- **Recommendations** - Erstellen und Verwalten von Empfehlungseinheiten in Commerce Admin. Recommendations verwenden Katalogdaten und das aggregierte Käuferverhalten, um relevante Produkte vorzuschlagen, z. B. „Kunden, die sich dieses Produkt angesehen haben, haben sich auch angesehen“.
- **Merchandising-Regeln** - Steuern Sie, wie Produkte beworben und eingestuft werden. Regeln können für alle Katalogansichten gelten oder auf eine bestimmte Ansicht zugeschnitten sein. Siehe [Erstellen einer Merchandising-Regel](https://experienceleague.adobe.com/de/docs/commerce/optimizer/merchandising/rules/add#create-a-rule).
- **Facetten** - Konfigurieren Sie die Filter, die Käufer verwenden, um die Produktergebnisse nach Attributen wie Marke, Größe oder Preis einzugrenzen.
- **Synonyme** - Verknüpfen Sie äquivalente Suchbegriffe, um Käufern zu helfen, Produkte mit verschiedenen Wörtern für dasselbe Konzept zu finden.
- **Einstellungen** - Konfigurieren von Such- und Merchandising-Optionen, einschließlich Preisfacetten, Sprache und erweiterter Suche.

Richtlinien bestimmen, welche Produkte über eine Katalogansicht verfügbar sind. Merchandising-Regeln steuern, wie Produkte innerhalb dieses Sortiments beworben und eingestuft werden.

Einzelheiten dazu, wie Suchergebnisse abgeglichen und sortiert werden, finden Sie unter [Suchabgleich und Rangfolge](./manage-results/search-relevance-matching.md).

>[!TAB Berichte]

Verwenden Sie Berichte, um die Storefront-Aktivität zu überprüfen und in Merchandising-Entscheidungen einfließen zu lassen.

- **Erfolgsmetriken** - Überprüfen Sie Umsatz, Konversion, Interaktion, Akquise und Absprungrate basierend auf der Aktivität in der Storefront.
- **Suchleistung** - Überprüfen Sie die Suchbegriffe, die Käuferinnen und Käufer verwenden, und ihre Leistung, um Bereiche zu identifizieren, in denen die Produktsuche verfeinert werden kann.

Die Berichterstellung hängt von den Aktivitätsdaten der Storefront ab, die von der Implementierung erfasst werden.

>[!TAB Systemkonfiguration]

Überwachen Sie die Katalogsynchronisierung und die Storefront-Ereignissammlung, um Probleme mit der Datenverfügbarkeit und -implementierung zu untersuchen.

- **Katalogsynchronisierung** - Überprüfen Sie den Synchronisierungsstatus für Katalogdaten, die von Commerce Foundation übertragen werden.
- **Ereignisse** - Überprüfen Sie erfasste Storefront-Ereignisse, die von der Produkterkennung, von Empfehlungen und von Berichten verwendet werden. Verwenden Sie die Seite „Ereignisse“, um die Erfassung von Verhaltensdaten zu überprüfen und fehlende oder unerwartete Ereignisse zu untersuchen.

>[!ENDTABS]
<!--
Watch the following video for a high-level overview of [!DNL Adobe Commerce Optimizer]:

>[!VIDEO](https://video.tv.adobe.com/v/3450226)
-->

## Bestätigen, dass eine Instanz CDM verwendet

1. Melden Sie sich über Unified Shell bei Commerce Admin an und wählen Sie die gewünschte Adobe Commerce as a Cloud Service-Instanz aus.
1. Vergewissern Sie sich, dass CDM-Merchandising-Seiten, z. B. Katalogansichten und Richtlinien, in der Navigation der Instanz verfügbar sind.
1. Wenn diese Seiten nicht verfügbar sind, überprüfen Sie, ob Sie die richtige Instanz ausgewählt haben und Unified Shell verwenden.

   Wenden Sie sich an den Adobe-Support oder das Commerce-Bereitstellungs-Team, um den CDM-Bereitstellungsstatus der Instanz zu überprüfen.

Der Status Bereit der Instanz bestätigt, dass sie bereitgestellt wird, bestätigt jedoch nicht allein, dass sie CDM verwendet.

