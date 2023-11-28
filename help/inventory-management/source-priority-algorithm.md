---
title: Quellprioritäts-Algorithmus konfigurieren
description: Erfahren Sie, wie Sie die Quellpriorität konfigurieren, die für die Reihenfolge der zugewiesenen Quellen in Ihrem Lager verwendet wird, um Empfehlungen zu geben.
exl-id: 7b25212d-0cd0-4280-be23-c67f06db900a
feature: Inventory, Shipping/Delivery
source-git-commit: 023716935a6657b0dc2317876debe608e65bf010
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# Quellprioritäts-Algorithmus konfigurieren

Benutzerdefinierte Lager enthalten eine zugewiesene Liste von Quellen, um verfügbare Produktbestände über Ihre Storefront zu verkaufen und zu versenden. Dieser Algorithmus verwendet die Reihenfolge der zugewiesenen Quellen in Ihrem Lager, um Empfehlungen abzugeben.

Wenn der Algorithmus ausgeführt wird:

- Durchläuft die konfigurierte Reihenfolge der Quellen auf der Lagerposition, beginnend am Anfang

- Empfiehlt eine Menge zum Versand und eine Quelle pro Produkt basierend auf der Bestellung in der Liste, der verfügbaren Menge und der bestellten Menge

- Fahren Sie die Liste so lange hinunter, bis der Bestellversand abgeschlossen ist.

- Überspringt deaktivierte Quellen, wenn sie in der Liste gefunden werden

Zum Konfigurieren ordnen Sie diese Quellen prioritär von oben nach unten an, um Bestellungen zu erfüllen. Der Quellauswahlalgorithmus (SSA) bietet eine Algorithmuspriorität, die diese Reihenfolge bei der Bestimmung von Versand- und Bestandsabzügen verwendet. Siehe [Priorisieren von Quellen für einen Bestand](stocks-prioritize-sources.md).

## Konfigurieren der Priorität von Quellen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > **[!UICONTROL Inventory]** > **[!UICONTROL Stocks]**.

1. Öffnen Sie ein Lager im Bearbeitungsmodus und navigieren Sie zum _[!UICONTROL Sources]_Bereich.

1. Klicken **[!UICONTROL Assign Sources]**.

1. Im _[!UICONTROL Assign Sources]_anzeigen, aktivieren Sie das Kontrollkästchen für die gewünschte Quelle und klicken Sie auf **[!UICONTROL Done]**, um dem Lager eine Quelle zuzuweisen.

>[!NOTE]
>
>Bei Verwendung von [Distance Priority](distance-priority-algorithm.md) Versandalgorithmus, wenn Routen und Daten für die ausgewählte [Berechnungsmodus](distance-priority-algorithm.md) (Fahren, Radfahren oder Gehen) für eine Sendung verwendet die SSA standardmäßig die Quellpriorität.

![Quellreihenfolge nach Priorisierung](assets/inventory-stock-priority-after.png)

| Symbole | Beschreibung |
|----------------------------------------------|----------------------------------------------------------------|
| ![Ziehen und Ablegen des Symbols zum Festlegen der Priorität](assets/icon-drag-and-drop-action.png) | Verwenden Sie , um Quellen je nach Priorität per Drag-and-Drop zu verschieben. |
| ![Klicken Sie auf Symbol , um die Zuweisung einer Quelle aufzuheben](assets/icon-delete-action.png) | Aufheben der Zuweisung einer Quelle zu einem Lager. |
