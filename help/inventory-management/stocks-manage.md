---
title: Lagerbestand verwalten
description: Erfahren Sie, wie mit "stock"ein virtueller, aggregierter Produktbestand für die Quellen Ihrer Verkaufskanäle dargestellt wird.
exl-id: 076b1325-2de4-46d3-9976-d900bd2cef47
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 0%

---

# Lagerverwaltung

Stock stellt einen virtuellen, aggregierten Produktbestand für die Quellen Ihrer Vertriebskanäle (Websites) dar. Abhängig von Ihrer Site-Konfiguration kann das Lager einem oder mehreren Vertriebskanälen zugewiesen werden. Jedem Vertriebskanal kann nur ein Lager zugewiesen werden, und ein einzelnes Lager kann mehreren Vertriebskanälen zugewiesen werden. Über das Lager können Sie die Priorisierung von Quellen ändern, die verwendet werden, wenn Bestellungen über einen Vertriebskanal eingehen.

Sie beginnen mit einem Standardbestand, der weder entfernt noch deaktiviert werden kann. Sie können dem Lager nur weitere Absatzkanäle hinzufügen. Die einzige zugewiesene Quelle ist &quot;Default Source&quot;. Dieser Bestand wird von Einzelquell-Merchants, Drittanbieter-Integrationen und importierten Produkten verwendet.

Sales Channel stellen Entitäten dar, die Ihren Bestand verkaufen. Standardmäßig stellt [!DNL Commerce] Ihre Store-Websites als Vertriebskanäle bereit. Vertriebskanäle können erweitert werden, um zusätzliche Kanäle wie B2B-Kundengruppen und Store-Ansichten zu unterstützen. Jeder Vertriebskanal kann nur einem Stock zugeordnet werden.

- **Sales Channel-Support** - Verkaufskanäle enthalten derzeit standardmäßig Websites. Sie können die Verkaufskanäle erweitern und benutzerdefinierte Optionen wie B2B-Kundengruppen und Store-Ansichten einschließen. Jedem Vertriebskanal kann nur ein einziges Lager zugewiesen werden. Ein einzelnes Lager kann mehreren Absatzkanälen zugewiesen werden.
- **Zu Quellen zuordnen** - Jedem Lager können eine oder mehrere aktivierte oder deaktivierte Quellen zugewiesen werden, wobei der virtuelle aggregierte Bestand pro Produkt berechnet wird.
- **Erfüllen der Prioritätsreihenfolge** - Der vordefinierte Prioritätsalgorithmus für den Source-Auswahlalgorithmus verwendet bei der Erfüllung von Bestellungen die Quellliste des Lagers von oben nach unten.

Im folgenden Diagramm wird definiert, wie ein Lager in Bezug auf Quellen und Sales Channel für einen Bicycle Shop-Händler funktioniert.

![Diagramm für z. B. Lager für einen Store](assets/diagram-stock.png){width="600" zoomable="yes"}

## Beispiel-Lager für ein Mountainbike und ein Geschäft

Alle Geschäfte beginnen mit einem Standardbestand. Er muss aus den folgenden Gründen `Enabled` bleiben:

- Sie wird beim Import neuer Produkte verwendet und weist automatisch Produkte der Standardquelle und dem Standardbestand für den sofortigen Zugriff auf [!DNL Inventory Management] zu.
- Sie können diesem Lager keine zusätzlichen Quellen über die standardmäßige Source hinaus hinzufügen.
- Sie ist erforderlich und wird von Einzelquellenhändlern, Bundle-Produkten und gruppierten Produkten verwendet.

Erstellen und konfigurieren Sie bei Händlern mit mehreren Quellen Lagerbestände, die Ihren Geschäften am besten entsprechen, und bestellen Sie sie. Wenn Sie einem Verkaufskanal ein neues Lager zuweisen, wird die Zuweisung von bereits vorhandenen Beständen in diesem Absatzkanal aufgehoben.

Bei einer Installation mit mehreren Stores wird der Standardbestand zunächst der [Hauptwebsite](../stores-purchase/stores.md#add-websites){target="_blank"} und dem Standardspeicher zugewiesen. In der Rasteransicht von **[!UICONTROL Products]** werden für aktivierte und deaktivierte Produkte richtige Lager und Mengen angezeigt.

![Stock verwalten](assets/inventory-stock.png){width="600" zoomable="yes"}

## Schaltflächenleiste

| Schaltfläche | Beschreibung |
|--|--|
| [!UICONTROL Add New Stock] | Öffnet das Formular &quot;_[!UICONTROL New Stock]_&quot;, mit dem ein neuer Lagerbestand für die Zuordnung von Bestand zum Absatzkanal eingegeben wird. |

## Spaltenbeschreibungen für Lager verwalten

| Spalte | Beschreibung |
|--|--|
| [!UICONTROL ID] | Eindeutige, numerische ID, die für den Lagereintrag generiert wird. |
| [!UICONTROL Name] | Eindeutiger Name, der den Lagerbestand identifiziert. |
| [!UICONTROL Sales Channels] | Definiert den Umfang des Bestands, indem der Bestand bestimmten Websites als _Verkaufskanäle_ zugewiesen wird. |
| [!UICONTROL Assigned sources] | Dem Bestand zugewiesene Quellen, die alle Erzeugnismengen liefern. |
| [!UICONTROL Action] | **[!UICONTROL Edit]** - Öffnet den Lagerbestand-Datensatz im Bearbeitungsmodus. |
