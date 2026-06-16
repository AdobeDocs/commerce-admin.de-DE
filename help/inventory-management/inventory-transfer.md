---
title: Inventar an Quelle übertragen
description: Erfahren Sie, wie Händler, die mehrere Quellen nutzen, Produktbestände von einem Quellspeicherort an einen anderen übertragen können.
exl-id: 30438412-bc93-4e65-8b6a-5ddb50afa7ff
feature: Inventory, Configuration
TQID: https://experienceleague.adobe.com/HV6GQjHa88xgcSAi-LXhyqe7k2QW95VzQ8eG2mGlJ8I
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 282
ht-degree: 0%

---

# Inventar an Quelle übertragen

Abhängig von den Geschäftsanforderungen und dem Standortstatus übertragen Händler mit mehreren Bezugsquellen häufig Produktbestände von einem Bezugsort an einen anderen. Sie schließen beispielsweise einen Lagerort oder versenden bestimmte Produkte nicht mehr von einem Standort aus, indem Sie alle Vorgänge für diese Produkte an einen neuen Speicherort verschieben.

Mit dieser Option können Sie ein oder mehrere Produkte, die Ursprungsquelle, aus der das Inventar transferiert werden soll, und die Zielquelle auswählen, aus der die Mengen empfangen werden sollen:

- Lagermengen, der Source-Artikelstatus (Lagerbestand/Nicht vorrätig) und die Benachrichtigungsmenge für die ausgewählte Bezugsquelle werden pro Produkt verschoben.

- Wenn ein Produkt diese Quelle nicht hat, wird es übersprungen.

- Das gesamte Produktinventar für die Quelle wird verschoben. Eine Teilmenge kann nicht übertragen werden.

>[!NOTE]
>
>Wenn sich die Ursprungs- und Zielquellen in verschiedenen Beständen befinden, wirkt sich dies auf die aggregierte Verkaufsmenge und die Reservierungen für laufende Bestellungen aus.

Sie können die Zuordnung der Quelle auch bei der Übertragung von Lagermengen aufheben.

{{$include /help/_includes/unassign-source.md}}

![Übertragen des Inventars an eine andere Quelle](assets/inventory-bulk-transfer-source.gif)

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Wählen Sie die Produkte aus, deren Quellen Sie ändern möchten.

   Durchsuchen oder suchen Sie nach Produkten und aktivieren Sie die Kontrollkästchen für die Übertragung.

1. Klicken Sie oben auf das **[!UICONTROL Actions]** und wählen Sie **[!UICONTROL Transfer Inventory to Source]** aus.

1. Klicken Sie im Bestätigungsdialogfeld auf **[!UICONTROL OK]** .

1. Um Produkte an ein neues Ziel zu übertragen, wählen Sie die Herkunft (_[!UICONTROL from]_) aus.

1. Um Produkte an ein neues Ziel zu übertragen, wählen Sie die Zielquelle (_[!UICONTROL to]_) aus.

1. Um die Quelle aus den Produkten zu entfernen, aktivieren Sie das optionale Kontrollkästchen **[!UICONTROL Unassign from origin source after transfer]**.

   ![Herkunft und Ziel für die Übertragung auswählen](assets/inventory-bulk-transfer-summary.png){width="600" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Transfer Inventory]**.

   Alle Produktmengen werden von der Ursprungsquelle abgezogen und der Zielquelle hinzugefügt. Die Menge und die verkaufbare Menge werden automatisch aktualisiert.

<!-- Last updated from includes: 2022-08-30 15:36:09 -->
