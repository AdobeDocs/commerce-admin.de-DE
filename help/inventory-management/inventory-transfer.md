---
title: Inventar an Quelle übertragen
description: Erfahren Sie, wie Händler mit mehreren Quellen Produktbestände von einem Quellspeicherort an einen anderen übertragen können.
exl-id: 30438412-bc93-4e65-8b6a-5ddb50afa7ff
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---

# Inventar an Quelle übertragen

Abhängig von den Geschäftsanforderungen und dem Status des Standorts übertragen Multi-Source-Händler häufig den Produktbestand von einem Quellstandort an einen anderen. Sie können beispielsweise einen Lagerort schließen oder bestimmte Produkte nicht mehr von einem Standort versenden und alle Vorgänge für diese Produkte an einen neuen Speicherort verschieben.

Diese Option ermöglicht die Auswahl eines oder mehrerer Produkte, der Quelle, an die das Inventar übertragen werden soll, und der Bestimmungsquelle, an die die Mengen geliefert werden sollen:

- Die Lagerbestandsmengen, der Source-Artikelstatus (Auf Lager/nicht auf Lager) und die Meldung &quot;Menge&quot;für die ausgewählte Quelle werden pro Produkt verschoben.

- Wenn ein Produkt nicht über diese Quelle verfügt, wird es übersprungen.

- Der gesamte Produktbestand für die Quelle wird verschoben. Eine Teilmenge kann nicht übertragen werden.

>[!NOTE]
>
>Befinden sich die Herkunft und die Bestimmungsquelle in unterschiedlichen Lagerbeständen, wirkt sich dies auf die aggregierte Menge der verkauften Mengen und die Reservierungen für laufende Aufträge aus.

Sie können die Zuweisung der Quelle auch aufheben, wenn Sie Lagerbestandsmengen übertragen.

{{$include /help/_includes/unassign-source.md}}

![Übertragen des Bestands an eine andere Quelle](assets/inventory-bulk-transfer-source.gif)

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Wählen Sie die Produkte aus, deren Quellen Sie ändern möchten.

   Suchen oder suchen Sie nach Produkten und aktivieren Sie die Kontrollkästchen für die Übertragung.

1. Klicken Sie auf das Menü **[!UICONTROL Actions]** oben und wählen Sie **[!UICONTROL Transfer Inventory to Source]** aus.

1. Klicken Sie im Bestätigungsdialogfeld auf &quot;**[!UICONTROL OK]**&quot;.

1. Um Produkte an einen neuen Zielort zu übertragen, wählen Sie die Quelle (_[!UICONTROL from]_) aus.

1. Um Produkte an einen neuen Zielort zu übertragen, wählen Sie die Zielquelle (_[!UICONTROL to]_) aus.

1. Um die Quelle aus den Produkten zu entfernen, aktivieren Sie das optionale Kontrollkästchen **[!UICONTROL Unassign from origin source after transfer]**.

   ![Wählen Sie Ursprung und Ziel für die Übertragung aus](assets/inventory-bulk-transfer-summary.png){width="600" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Transfer Inventory]**.

   Alle Erzeugnismengen werden von der Ursprungsquelle abgezogen und der Bestimmungsquelle hinzugefügt. Die Menge und die Verkaufsmenge werden automatisch aktualisiert.
