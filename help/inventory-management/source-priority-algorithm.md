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

Benutzerdefinierte Lager enthalten eine zugewiesene Liste von Quellen für den Verkauf und Versand des verfügbaren Produktbestands über Ihre Storefront. Dieser Algorithmus verwendet die Reihenfolge der zugewiesenen Quellen in Ihrem Lager, um Empfehlungen zu geben.

Beim Ausführen des Algorithmus:

- Durchläuft die konfigurierte Quellreihenfolge auf der Lagerebene, beginnend oben.

- Empfiehlt je nach Bestellung in der Liste, verfügbarer Menge und bestellter Menge eine zu liefernde Menge sowie eine zu beschaffende Menge pro Produkt

- Fahren Sie in der Liste nach unten, bis die Bestellanlieferung ausgefüllt ist

- Deaktivierte Quellen werden übersprungen, wenn sie in der Liste gefunden wurden

Zur Konfiguration ordnen Sie diese Quellen für die Auftragserfüllung von oben nach unten an. Der Source-Auswahlalgorithmus (SSA) bietet eine Algorithmuspriorität, die diese Reihenfolge bei der Bestimmung von Versand- und Lagerabzügen verwendet. Siehe [Priorisieren von Quellen für einen Bestand](stocks-prioritize-sources.md).

## Konfigurieren der Priorität von Quellen

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > **[!UICONTROL Inventory]** > **[!UICONTROL Stocks]**.

1. Öffnen Sie ein Lager im Bearbeitungsmodus und navigieren Sie zum _[!UICONTROL Sources]_&#x200B;Bereich.

1. Klicken Sie auf **[!UICONTROL Assign Sources]**.

1. Aktivieren Sie in der _[!UICONTROL Assign Sources]_&#x200B;das Kontrollkästchen für die gewünschte Quelle und klicken Sie dann auf **[!UICONTROL Done]**, um dem Lager eine Quelle zuzuweisen.

>[!NOTE]
>
>Wenn bei der Verwendung des [Distance Priority](distance-priority-algorithm.md)-Algorithmus für den Versand Routen und Daten für den ausgewählten [Berechnungsmodus](distance-priority-algorithm.md) (Fahren, Radfahren oder Gehen) für eine Sendung nicht zurückgegeben werden, verwendet die SSA standardmäßig die Source-Priorität.

![Source-Reihenfolge nach der Priorisierung](assets/inventory-stock-priority-after.png)

| Symbole | Beschreibung |
|----------------------------------------------|----------------------------------------------------------------|
| ![Ziehen Sie das Symbol per Drag-and-Drop, um die Priorität festzulegen](assets/icon-drag-and-drop-action.png) | Verwenden Sie , um Quellen entsprechend der Priorität per Drag-and-Drop abzulegen. |
| ![Klicken Sie auf das Symbol , um die Zuweisung einer Quelle aufzuheben](assets/icon-delete-action.png) | Zuweisung einer Quelle zu einem Lager aufheben. |
