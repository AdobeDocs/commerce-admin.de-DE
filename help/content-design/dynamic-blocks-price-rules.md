---
title: Dynamische Blöcke in Preisregeln
description: Verknüpfen Sie einen dynamischen Block mit einer Preisregel für Werbeaktionen.
exl-id: e1564df2-1c06-4d11-a32d-6f5c0be974e3
feature: Page Content, Price Rules
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/de/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
TQID: 'https://experienceleague.adobe.com/Fzw3GXEp2PNXIuvOpN62tBiLhTeMJGsDMfQpRwV1dSg'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: 17d326fa-534a-55a5-b46f-8ae1de1e2f75
    internal-label: Page Content
  - id: a507b1ed-4937-53da-97ae-57d36bd5b9e0
    internal-label: Price Rules
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 0%
---
# Dynamische Blöcke in Preisregeln

{{ee-feature}}

Jeder [dynamische Block](dynamic-blocks.md) den Sie erstellen, kann mit einer Promotion verknüpft werden. Um die Zuordnung vorzunehmen, müssen Sie zunächst sowohl den dynamischen Block als auch die [Katalogpreisregel](../merchandising-promotions/price-rules-catalog.md) oder [Warenkorb-Preisregel](../merchandising-promotions/price-rules-cart.md) erstellen. Die Zuordnung kann bei der Arbeit an einer Preisregel oder bei der Arbeit an einem dynamischen Block erfolgen.

>[!IMPORTANT]
>
>Nachdem Sie diese Zuordnung erstellt haben, wird der dynamische Block (**) angezeigt** wenn die Regel ausgelöst wird. Wenn die Promotion auf Segment A ausgerichtet ist, wird der Block auf Segment A angezeigt. Wenn die Promotion nicht aktiv ist, wird der Block nicht angezeigt.

## Dynamischen Block mit einer Preisregel verknüpfen

1. Wechseln Sie in _Admin_-Seitenleiste zu **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_&#x200B;und wählen Sie eine der folgenden Optionen:

   - **[!UICONTROL Catalog Price Rules]**
   - **[!UICONTROL Cart Price Rules]**

1. Suchen Sie im Raster die Regel, die Sie mit dem dynamischen Block verknüpfen möchten, und öffnen Sie sie im Bearbeitungsmodus.

1. Scrollen Sie nach unten und erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) **[!UICONTROL Related Dynamic Blocks]**.

1. Setzen Sie in der ersten Spalte den Filter auf `Any` und klicken Sie auf **[!UICONTROL Reset Filter]**.

   Im Raster werden nun alle verfügbaren dynamischen Blöcke aufgelistet.

1. Aktivieren Sie das Kontrollkästchen jedes dynamischen Blocks, den Sie mit der Regel verknüpfen möchten.

   ![Ausgewählte dynamische Blöcke hinzufügen](./assets/price-rule-cart-related-dynamic-blocks-any.png){width="600" zoomable="yes"}

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.

## Zuordnen einer Preisregel zu einem dynamischen Block

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Dynamic Blocks]**.

1. Suchen Sie den dynamischen Block im Raster und öffnen Sie ihn im Bearbeitungsmodus.

1. Scrollen Sie nach unten und erweitern Sie **[!UICONTROL Related Promotions]**.

   Alle aktuell verknüpften Preisregeln werden im Raster angezeigt.

1. Fügen Sie eine neue verknüpfte Regel hinzu oder entfernen Sie eine aktuelle Verknüpfung.

   - Um eine Promotion zum Warenkorb zu verknüpfen, klicken Sie auf **[!UICONTROL Add Cart Price Rules]**.

   - Um eine produktbezogene Promotion zu verknüpfen, klicken Sie auf **[!UICONTROL Add Catalog Price Rules]**.

1. Aktivieren Sie im Raster das Kontrollkästchen jeder Regel, die Sie mit dem dynamischen Block verknüpfen möchten.

1. Klicken Sie auf **[!UICONTROL Add Selected]**.

   ![Ausgewählte Preisregeln zu einem dynamischen Block hinzufügen](./assets/pb-dynamic-block-add-related-cart-price-rules.png){width="600" zoomable="yes"}

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.
