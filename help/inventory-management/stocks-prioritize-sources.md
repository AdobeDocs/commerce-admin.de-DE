---
title: Priorisieren von Lagerbestandsquellen für einen Bestand
description: Erfahren Sie, wie Sie Quellen mit Priorität von oben nach unten sortieren, was bei der Bestimmung von Versand- und Lagerabzügen verwendet wird.
exl-id: 16db3ee3-ce99-40dd-b1a3-fcb145b1298f
feature: Inventory, Configuration
TQID: https://experienceleague.adobe.com/oPgeuN3-Il-yf3zpG2r4PNAmNbf-4gmz5-GFngM3-Ng
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
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
source-wordcount: 210
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
