---
title: Dynamische Blöcke in Preisregeln
description: Verknüpfen Sie einen dynamischen Baustein mit einer Preisregel für Werbeaktionen.
exl-id: e1564df2-1c06-4d11-a32d-6f5c0be974e3
feature: Page Content, Price Rules
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# Dynamische Blöcke in Preisregeln

{{ee-feature}}

Jeder von Ihnen erstellte [dynamische Block](dynamic-blocks.md) kann einer Promotion zugeordnet werden. Um die Zuordnung herzustellen, müssen Sie zunächst sowohl den dynamischen Block als auch die [Katalogpreisregel](../merchandising-promotions/price-rules-catalog.md) oder die [Preisregel für den Warenkorb](../merchandising-promotions/price-rules-cart.md) erstellen. Die Zuordnung kann während der Arbeit an einer Preisregel oder bei der Arbeit an einem dynamischen Block vorgenommen werden.

>[!IMPORTANT]
>
>Nachdem Sie diese Zuordnung erstellt haben, wird der dynamische Block **nur** angezeigt, wenn die Regel ausgelöst wird. Wenn die Promotion auf Segment A ausgerichtet ist, wird der Baustein in Segment A angezeigt. Wenn die Promotion nicht aktiv ist, wird der Block nicht angezeigt.

## Dynamischen Baustein mit einer Preisregel verknüpfen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_und wählen Sie eine der folgenden Optionen:

   - **[!UICONTROL Catalog Price Rules]**
   - **[!UICONTROL Cart Price Rules]**

1. Suchen Sie im Raster die Regel, die Sie mit dem dynamischen Block verknüpfen möchten, und öffnen Sie sie im Bearbeitungsmodus.

1. Scrollen Sie nach unten und erweitern Sie den ![Erweiterungsselektor](../assets/icon-display-expand.png) **[!UICONTROL Related Dynamic Blocks]**.

1. Setzen Sie den Filter in der ersten Spalte auf `Any` und klicken Sie auf **[!UICONTROL Reset Filter]**.

   Das Raster listet jetzt alle verfügbaren dynamischen Blöcke auf.

1. Aktivieren Sie das Kontrollkästchen jedes dynamischen Blocks, den Sie mit der Regel verknüpfen möchten.

   ![Hinzufügen ausgewählter dynamischer Blöcke](./assets/price-rule-cart-related-dynamic-blocks-any.png){width="600" zoomable="yes"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]**.

## Preisregel mit einem dynamischen Block verknüpfen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Dynamic Blocks]**.

1. Suchen Sie den dynamischen Block im Raster und öffnen Sie ihn im Bearbeitungsmodus.

1. Scrollen Sie nach unten und erweitern Sie **[!UICONTROL Related Promotions]**.

   Alle derzeit verknüpften Preisregeln werden im Netz angezeigt.

1. Fügen Sie eine neue zugehörige Regel hinzu oder entfernen Sie eine aktuelle Zuordnung.

   - Um eine Warenkorbaktion zuzuordnen, klicken Sie auf **[!UICONTROL Add Cart Price Rules]**.

   - Um eine produktbezogene Promotion zuzuordnen, klicken Sie auf **[!UICONTROL Add Catalog Price Rules]**.

1. Aktivieren Sie im Raster das Kontrollkästchen der einzelnen Regeln, die Sie mit dem dynamischen Block verknüpfen möchten.

1. Klicken Sie auf **[!UICONTROL Add Selected]**.

   ![Hinzufügen ausgewählter Preisregeln zu einem dynamischen Block](./assets/pb-dynamic-block-add-related-cart-price-rules.png){width="600" zoomable="yes"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]**.
