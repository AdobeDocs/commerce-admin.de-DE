---
title: Lagerbestand verwalten
description: Erfahren Sie, wie Stock verwendet wird, um einen virtuellen, aggregierten Bestand von Produkten für Quellen Ihrer Vertriebskanäle darzustellen.
exl-id: 076b1325-2de4-46d3-9976-d900bd2cef47
TQID: https://experienceleague.adobe.com/IeG1bA1etAjxiDjSWY83GLNugllHT1mUrZBde45Ha8g
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 524
ht-degree: 0%

---

# Lagerverwaltung

Stock stellt ein virtuelles, aggregiertes Inventar von Produkten für Quellen Ihrer Vertriebskanäle (Websites) dar. Abhängig von Ihrer Site-Konfiguration kann das Lager einem oder mehreren Vertriebskanälen zugewiesen werden. Jedem Verkaufskanal kann nur ein Lager zugewiesen werden, und ein Lager kann mehreren Verkaufskanälen zugewiesen werden. Über den Lagerbestand können Sie die Priorisierung der verwendeten Quellen ändern, da Bestellungen über einen Vertriebskanal eingehen.

Sie beginnen mit einem Standardlager, das nicht entfernt oder deaktiviert werden kann. Sie können nur zusätzliche Vertriebskanäle zum Lager hinzufügen. Die einzige zugewiesene Quelle ist „Standard-Source&quot;. Dieser Bestand wird von Einzelhändler, Drittanbieterintegrationen und importierten Produkten verwendet.

Vertriebskanäle stellen Entitäten dar, die Ihren Bestand verkaufen. Standardmäßig stellt [!DNL Commerce] Ihre Store-Websites als Vertriebskanäle bereit. Vertriebskanäle können erweitert werden, um zusätzliche Kanäle wie B2B-Kundengruppen und Store-Ansichten zu unterstützen. Jeder Vertriebskanal kann nur einem Lager zugeordnet werden.

- **Sales Channel-Support** - Die Vertriebskanäle umfassen derzeit vorkonfigurierte Websites. Sie können Vertriebskanäle erweitern, um benutzerdefinierte Optionen wie B2B-Kundengruppen und Store-Ansichten einzuschließen. Jedem Vertriebskanal kann nur ein Lager zugewiesen sein. Ein einzelnes Lager kann mehreren Vertriebskanälen zugewiesen werden.
- **Zu Quellen zuordnen** - Jedem Lager kann eine oder mehrere aktivierte oder deaktivierte Quellen zugewiesen sein, wodurch das virtuelle aggregierte Inventar pro Produkt berechnet wird.
- **Prioritätsauftragserfüllung** - Der vorkonfigurierte Prioritätsalgorithmus für den Source-Auswahlalgorithmus verwendet bei der Auftragserfüllung die Quellliste des Lagers von oben nach unten.

Das folgende Diagramm hilft bei der Definition, wie ein Lager in Bezug auf Quellen und Vertriebskanäle für einen Fahrradhändler funktioniert.

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
| [!UICONTROL Add New Stock] | Öffnet das _[!UICONTROL New Stock]_Formular, mit dem ein neuer Lagerbestand für die Zuordnung von Lagerbestand und Vertriebskanal eingegeben wird. |

## Verwalten von Stock-Spaltenbeschreibungen

| Spalte | Beschreibung |
|--|--|
| [!UICONTROL ID] | Eindeutige numerische ID, die für den Lagereintrag generiert wurde. |
| [!UICONTROL Name] | Eindeutiger Name, der den Lagerbestand identifiziert. |
| [!UICONTROL Sales Channels] | Definiert den Umfang des Lagers, indem das Lager bestimmten Websites als &quot;_&quot; zugewiesen_. |
| [!UICONTROL Assigned sources] | Dem Lager zugewiesene Quellen, die alle Produktmengen liefern. |
| [!UICONTROL Action] | **[!UICONTROL Edit]** - Öffnet den Lagerdatensatz im Bearbeitungsmodus. |
