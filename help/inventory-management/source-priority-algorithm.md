---
title: Konfigurieren des Source-Prioritätsalgorithmus
description: Erfahren Sie, wie Sie die Quellpriorität konfigurieren, die für die Reihenfolge der zugewiesenen Quellen in Ihrem Lager verwendet wird, um Empfehlungen zu geben.
exl-id: 7b25212d-0cd0-4280-be23-c67f06db900a
feature: Inventory, Shipping/Delivery
source-git-commit: 023716935a6657b0dc2317876debe608e65bf010
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# Konfigurieren des Source-Prioritätsalgorithmus

Benutzerdefinierte Lager enthalten eine zugewiesene Liste von Quellen, um verfügbare Produktbestände über Ihre Storefront zu verkaufen und zu versenden. Dieser Algorithmus verwendet die Reihenfolge der zugewiesenen Quellen in Ihrem Lager, um Empfehlungen abzugeben.

Wenn der Algorithmus ausgeführt wird:

- Durchläuft die konfigurierte Reihenfolge der Quellen auf der Lagerposition, beginnend am Anfang

- Empfiehlt eine Menge zum Versand und eine Quelle pro Produkt basierend auf der Bestellung in der Liste, der verfügbaren Menge und der bestellten Menge

- Fahren Sie die Liste so lange hinunter, bis der Bestellversand abgeschlossen ist.

- Überspringt deaktivierte Quellen, wenn sie in der Liste gefunden werden

Zum Konfigurieren ordnen Sie diese Quellen prioritär von oben nach unten an, um Bestellungen zu erfüllen. Der Source Selection Algorithm (SSA) bietet eine Algorithmuspriorität, die diese Reihenfolge bei der Bestimmung von Versand- und Bestandsabzügen verwendet. Siehe [Priorisieren von Quellen für einen Lagerbestand](stocks-prioritize-sources.md).

## Konfigurieren der Priorität von Quellen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > **[!UICONTROL Inventory]** > **[!UICONTROL Stocks]**.

1. Öffnen Sie ein Lager im Bearbeitungsmodus und navigieren Sie zum Bereich _[!UICONTROL Sources]_.

1. Klicken Sie auf **[!UICONTROL Assign Sources]**.

1. Aktivieren Sie in der Ansicht &quot;_[!UICONTROL Assign Sources]_&quot;das Kontrollkästchen für die gewünschte Quelle und klicken Sie dann auf &quot;**[!UICONTROL Done]**&quot;, um dem Lager eine Quelle zuzuweisen.

>[!NOTE]
>
>Bei Verwendung des Algorithmus [Entfernungspriorität](distance-priority-algorithm.md) für den Versand verwendet die SSA standardmäßig die Source-Priorität, wenn Routen und Daten für den ausgewählten [Berechnungsmodus](distance-priority-algorithm.md) (Fahren, Fahren oder Gehen) für eine Sendung nicht zurückgegeben werden.

![Reihenfolge der Source nach der Priorisierung](assets/inventory-stock-priority-after.png)

| Symbole | Beschreibung |
|----------------------------------------------|----------------------------------------------------------------|
| ![Ziehen Sie das Symbol per Drag-and-Drop, um die Priorität festzulegen](assets/icon-drag-and-drop-action.png) | Verwenden Sie , um Quellen je nach Priorität per Drag-and-Drop zu verschieben. |
| ![Klicken Sie auf das Symbol, um die Zuweisung einer Quelle aufzuheben](assets/icon-delete-action.png) | Aufheben der Zuweisung einer Quelle zu einem Lager. |
