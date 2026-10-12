---
title: Konfigurieren von Smart-Attributen für Visual Merchandiser
description: Erfahren Sie, wie Sie die vom Visual Merchandiser verwendeten Smart-Attribute konfigurieren.
exl-id: 7bbbca40-d991-4393-b99c-5bef2e711071
feature: Merchandising, Products, Configuration, Attributes
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
TQID: 'https://experienceleague.adobe.com/-6tbdpZ7L6nS1sIOXdk5Faxpkkt9qzqWhIjqp9MwgiM'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 58c984c2-e237-5c50-9718-500e40d1e82c
    internal-label: Merchandising
  - id: 4067ab89-2e97-5de1-8d98-de8318461a8d
    internal-label: Products
  - id: 76cfaac4-e563-56dd-8938-708bf8b84956
    internal-label: Attributes
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
    internal-label: Customer engagement
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '196'
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
