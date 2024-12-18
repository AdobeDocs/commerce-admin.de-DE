---
title: Priorisieren von Lagerbestandsquellen für einen Bestand
description: Erfahren Sie, wie Sie Quellen mit Priorität von oben nach unten sortieren, was bei der Bestimmung von Versand- und Lagerabzügen verwendet wird.
exl-id: 16db3ee3-ce99-40dd-b1a3-fcb145b1298f
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---

# Quellen für einen Bestand priorisieren

Nachdem Sie [Quellen](sources-manage.md) zum [Lager](stocks-manage.md) hinzugefügt haben, ordnen Sie diese Quellen für die Ausführung von Bestellungen von oben nach unten an. Der Source-Auswahlalgorithmus (SSA) bietet eine Algorithmuspriorität, die diese Reihenfolge bei der Bestimmung von Versand- und Lagerabzügen verwendet.

Die Quellpriorität für Lager hat keinen Einfluss auf zugewiesene Quellen bei der Bearbeitung von Warenbeständen.

In diesem Beispiel hat die britische Stock-Quelle nicht geordnet für ein Geschäft und zwei Lagerhäuser in London und ein Lager in Berlin zugewiesen.

![Source-Reihenfolge vor der Priorisierung](assets/inventory-priority-before.png){width="350" zoomable="yes"}

Der Händler bevorzugt Lieferungen aus dem größeren Berliner Lager, dann dem London Warehouse, dem London Overflow Location und schließlich der Storefront in London. Um die Reihenfolge zu ändern, werden die Einträge per Drag-and-Drop in die gewünschte Reihenfolge verschoben.

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Stocks]**.

1. Öffnen Sie das Lager im _Bearbeiten_-Modus.

1. Erweitern Sie bei Bedarf die Registerkarte _[!UICONTROL Sources]_.

1. Verwenden Sie ![Symbol „Sortieren](assets/icon-sort.png), um die Quellen per Drag-and-Drop von oben (erste) nach unten (letzte) in eine Priorität zu ziehen.

   Diese Bestellung ist beim Versand von Bestellungen wichtig. SSA empfiehlt Lieferungen in der Reihenfolge der Quellen

1. Klicken Sie auf **[!UICONTROL Save & Continue]** , um die Änderungen zu speichern.

![Source-Reihenfolge nach der Priorisierung](assets/inventory-stock-priority-after.png){width="350" zoomable="yes"}
