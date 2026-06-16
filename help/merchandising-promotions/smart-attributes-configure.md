---
title: Konfigurieren von Smart-Attributen für Visual Merchandiser
description: Erfahren Sie, wie Sie die vom Visual Merchandiser verwendeten Smart-Attribute konfigurieren.
exl-id: 7bbbca40-d991-4393-b99c-5bef2e711071
feature: Merchandising, Products, Configuration, Attributes
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/de/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
TQID: https://experienceleague.adobe.com/-6tbdpZ7L6nS1sIOXdk5Faxpkkt9qzqWhIjqp9MwgiM
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 196
ht-degree: 0%

---

# Konfigurieren von Smart-Attributen für Visual Merchandiser

{{ee-feature}}

Die Konfiguration des visuellen Merchandisers bestimmt die Attribute, die im Merchandising-Fenster verwendet werden können, sowie den Mindestbestand. Die Konfiguration identifiziert auch das für die Farbe verwendete Attribut und die Reihenfolge der Farbwerte.

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Catalog]** und wählen Sie darunter **[!UICONTROL Visual Merchandiser]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL General Options]** .

   ![Katalogkonfiguration - Visual Merchandiser](../configuration-reference/catalog/assets/catalog-visual-merchandiser-general-options.png){width="600" zoomable="yes"}

1. Wählen Sie in der Liste **[!UICONTROL Attributes for Category Rules]** jedes Attribut aus, das Sie für das visuelle Merchandising verfügbar machen möchten.

   Um mehrere Attribute auszuwählen, halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie auf die einzelnen Elemente.

1. Geben Sie die **[!UICONTROL Minimum Stock Threshold]** ein, die im Fenster „Visual Merchandiser“ angezeigt werden soll.

1. Geben Sie die **[!UICONTROL Color Attribute Code]** ein.

   Der Standardwert ist `color`. Wenn Ihr Katalog ein anderes Attribut verwendet, geben Sie den Attributnamen in Kleinbuchstaben ein.

1. Geben Sie **[!UICONTROL Color Order]** jeden Farbwert in einer separaten Zeile und nacheinander ein, um die Priorität jeder Farbe zu bestimmen.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.
