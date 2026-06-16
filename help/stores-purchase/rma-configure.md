---
title: Konfigurieren von Rücksendungen
description: Erfahren Sie, wie Sie Rücksendungen für Ihr Geschäft aktivieren und die unterstützten Versandmethoden konfigurieren.
exl-id: a1b508fc-7e42-4d37-bf7e-dea17a40d39b
feature: Returns, Configuration
TQID: https://experienceleague.adobe.com/TgVsqEceM-mTY91OCl7XRL0Uwk8VJAHatv0kHiOM00g
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 353
ht-degree: 0%

---

# Konfigurieren von Rücksendungen

{{ee-feature}}

Wenn diese Option aktiviert ist, können RMA-Anfragen von Kunden über die Storefront gesendet werden. Eine Rücksendung kann nur generiert werden, wenn ein Artikel in der Bestellung vorhanden ist, der zur Rücksendung zur Verfügung steht. Anfragen zur Rückgabe einzelner Elemente werden vom Attribut _RMA aktivieren_ in jedem Produktdatensatz verwaltet. Standardmäßig werden die Konfigurationseinstellungen auf das Produkt angewendet (_[!UICONTROL Use Config Settings]_ist ausgewählt). Wenn_[!UICONTROL Enable RMA]_ auf `No` gesetzt ist, wird das Produkt nicht in der Liste der Elemente angezeigt, die für die Rückgabe verfügbar sind. Wenn Sie die Einstellung _RMA aktivieren_ ändern, gilt sie sowohl für neue als auch für bestehende Bestellungen.

## RMAs für Ihren Store aktivieren

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen Sie darunter **[!UICONTROL Sales]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL RMA Settings]** .

   ![RMA-Einstellungen](../configuration-reference/sales/assets/sales-rma-settings.png){width="600" zoomable="yes"}

1. Legen Sie **[!UICONTROL Enable RMA on Storefront]** auf `Yes` fest.

   Diese Einstellung bestimmt, ob Kundinnen und Kunden RMA-Anfragen in der Storefront erstellen und anzeigen können. RMAs können sowohl auf neue als auch auf bestehende Bestellungen angewendet werden.

1. Legen Sie **[!UICONTROL Enable RMA on Product Level]** auf `Yes` fest.

   Diese Einstellung bestimmt das Verhalten für das Attribut _RMA aktivieren_ für einzelne Produkte in der Storefront:

   - Wenn [!UICONTROL Enable RMA on Product Level] auf `Yes` gesetzt ist, können Kunden in der Storefront alle einzelnen Produkte zurückgeben. Sie enthält sowohl _[!UICONTROL Enable RMA]_= `Yes` als auch_[!UICONTROL Enable RMA]_ = `No` Produktattributwerte.
   - Wenn [!UICONTROL Enable RMA on Product Level] auf `No` gesetzt ist, können Kunden in der Storefront nur die Produkte mit einem _[!UICONTROL Enable RMA]_= `Yes` Produktattributwert zurückgeben.

1. Legen Sie **[!UICONTROL Use Store Address]** auf einen der folgenden Werte fest:

   - `Yes` - Senden Sie zurückgesendete Produkte an die Adresse des Geschäfts.
   - `No` - Geben Sie eine alternative Adresse für die Produktrücksendung ein.

   ![RMA-Einstellungen mit alternativer Adresse](../configuration-reference/sales/assets/sales-rma-settings.png){width="600" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Save Config]**.

## Konfigurieren der Versandmethoden für Rücksendungen

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Delivery Methods]**.

1. Erweitern Sie den Abschnitt für den Provider, den Sie für den Rücksendedienst verwenden möchten, z. B. **[!UICONTROL UPS]**.

   ![RMA-Dienst für Provider aktivieren](./assets/rma-delivery-method.png){width="600" zoomable="yes"}

1. Legen Sie **[!UICONTROL Enabled for RMA]** auf `Yes` fest.

1. Klicken Sie auf **[!UICONTROL Save Config]**.

## Zulässige RMAs auf Produktebene ändern

Wenn Sie RMAs für Ihren Store aktivieren und Ihr Katalog einige Produkte enthält, für die keine Rückgabe zulässig sein sollte, können Sie die Einstellung auf Produktebene ändern.

1. Öffnen Sie das Produkt im Bearbeitungsmodus.

1. Scrollen Sie nach unten und erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Autosettings]** .

1. Deaktivieren Sie bei Bedarf das Kontrollkästchen **[!UICONTROL Use Config Setting]** .

1. Stellen Sie die **[!UICONTROL Enable RMA]** auf `No`.

   ![Deaktivieren von RMA für ein Produkt](./assets/product-advanced-autosettings-enable-rma.png){width="600" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Save]**.
