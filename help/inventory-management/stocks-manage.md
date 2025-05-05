---
title: Lagerbestand verwalten
description: Erfahren Sie, wie Stock verwendet wird, um einen virtuellen, aggregierten Bestand von Produkten für Quellen Ihrer Vertriebskanäle darzustellen.
exl-id: 076b1325-2de4-46d3-9976-d900bd2cef47
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 0%

---

# Lagerverwaltung

Stock stellt ein virtuelles, aggregiertes Inventar von Produkten für Quellen Ihrer Vertriebskanäle (Websites) dar. Abhängig von Ihrer Site-Konfiguration kann das Lager einem oder mehreren Vertriebskanälen zugewiesen werden. Jedem Verkaufskanal kann nur ein Lager zugewiesen werden, und ein Lager kann mehreren Verkaufskanälen zugewiesen werden. Über den Lagerbestand können Sie die Priorisierung der verwendeten Quellen ändern, da Bestellungen über einen Vertriebskanal eingehen.

Sie beginnen mit einem Standardlager, das nicht entfernt oder deaktiviert werden kann. Sie können nur zusätzliche Vertriebskanäle zum Lager hinzufügen. Die einzige zugewiesene Quelle ist „Standard-Source&quot;. Dieser Bestand wird von Einzelhändler, Drittanbieterintegrationen und importierten Produkten verwendet.

Sales Channel repräsentieren Entitäten, die Ihr Inventar verkaufen. Standardmäßig stellt [!DNL Commerce] Ihre Store-Websites als Vertriebskanäle bereit. Vertriebskanäle können erweitert werden, um zusätzliche Kanäle wie B2B-Kundengruppen und Store-Ansichten zu unterstützen. Jeder Vertriebskanal kann nur einem Lager zugeordnet werden.

- **Sales Channel-Support** - Die Vertriebskanäle umfassen derzeit vorkonfigurierte Websites. Sie können Vertriebskanäle erweitern, um benutzerdefinierte Optionen wie B2B-Kundengruppen und Store-Ansichten einzuschließen. Jedem Vertriebskanal kann nur ein Lager zugewiesen sein. Ein einzelnes Lager kann mehreren Vertriebskanälen zugewiesen werden.
- **Zu Quellen zuordnen** - Jedem Lager kann eine oder mehrere aktivierte oder deaktivierte Quellen zugewiesen sein, wodurch das virtuelle aggregierte Inventar pro Produkt berechnet wird.
- **Prioritätsauftragserfüllung** - Der vorkonfigurierte Prioritätsalgorithmus für den Source-Auswahlalgorithmus verwendet bei der Auftragserfüllung die Quellliste des Lagers von oben nach unten.

Das folgende Diagramm hilft dabei, die Funktionsweise eines Lagers in Bezug auf die Bezugsquellen und Sales Channel für einen Fahrradhändler zu definieren.

![Diagramm, z. B. Lager für ein Geschäft](assets/diagram-stock.png){width="600" zoomable="yes"}

## Beispiel-Lager für ein Mountainbike und einen Laden

Alle Stores beginnen mit einem Standardlager. Sie muss aus den folgenden Gründen `Enabled` bleiben:

- Es wird beim Importieren neuer Produkte verwendet, wobei Produkte automatisch der Standardquelle und dem Lager zugewiesen werden, um sofortigen Zugriff auf [!DNL Inventory Management] zu erhalten.
- Sie können keine zusätzlichen Quellen über die Standard-Source hinaus zu diesem Bestand hinzufügen.
- Sie ist erforderlich und wird von Einzelhändler, Bundle-Produkten und gruppierten Produkten verwendet.

Erstellen und konfigurieren Sie für Händler, die mehrere Bezugsquellen haben, Lager so, dass sie optimal zu Ihren Geschäften passen und Ihre Bestellungen erfüllen. Wenn Sie einem Vertriebskanal neue Lager zuweisen, wird die Zuweisung aller bereits vorhandenen Lager in diesem Vertriebskanal aufgehoben.

Bei einer Multi-Store-Installation wird der Standardbestand zunächst der [Haupt-Website“ ](../stores-purchase/stores.md#add-websites){target="_blank"} dem Standardspeicher zugewiesen. Der richtige Bestand und die richtigen Mengen werden für aktivierte und deaktivierte Produkte in der **[!UICONTROL Products]** Rasteransicht angezeigt.

![Stock verwalten](assets/inventory-stock.png){width="600" zoomable="yes"}

## Schaltflächenleiste

| Schaltfläche | Beschreibung |
|--|--|
| [!UICONTROL Add New Stock] | Öffnet das _[!UICONTROL New Stock]_&#x200B;Formular, mit dem ein neuer Lagerbestand für die Zuordnung von Lagerbestand und Vertriebskanal eingegeben wird. |

## Verwalten von Stock-Spaltenbeschreibungen

| Spalte | Beschreibung |
|--|--|
| [!UICONTROL ID] | Eindeutige numerische ID, die für den Lagereintrag generiert wurde. |
| [!UICONTROL Name] | Eindeutiger Name, der den Lagerbestand identifiziert. |
| [!UICONTROL Sales Channels] | Definiert den Umfang des Lagers, indem das Lager bestimmten Websites als &quot;_&quot; zugewiesen_. |
| [!UICONTROL Assigned sources] | Dem Lager zugewiesene Quellen, die alle Produktmengen liefern. |
| [!UICONTROL Action] | **[!UICONTROL Edit]** - Öffnet den Lagerdatensatz im Bearbeitungsmodus. |
