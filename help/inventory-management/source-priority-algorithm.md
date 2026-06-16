---
title: Konfigurieren des Source-Prioritätsalgorithmus
description: Erfahren Sie, wie Sie die Quellpriorität konfigurieren, die für die Reihenfolge der zugewiesenen Quellen in Ihrem Lager verwendet wird, um Empfehlungen zu geben.
exl-id: 7b25212d-0cd0-4280-be23-c67f06db900a
feature: Inventory, Shipping/Delivery
TQID: https://experienceleague.adobe.com/TB4THYjkzbNvEbsjNzOewNtYS6JoRvLDiQQCovSMkbI
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 271
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
