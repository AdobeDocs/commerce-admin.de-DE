---
title: Bedingungen für den Checkout
description: Erfahren Sie mehr über die Nutzungsbedingungen, die für Ihren Store konfiguriert werden können.
exl-id: 59ba6385-3cc6-43e8-b984-5c26516bba88
feature: Checkout, Compliance
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 1%

---

# Bedingungen für den Checkout

Bei manuellen _Geschäftsbedingungen_ -Funktion aktiviert ist, müssen die Kunden den Verkaufsbedingungen zustimmen, bevor der Kauf abgeschlossen ist. Die Verkaufsbedingungen enthalten in der Regel Offenlegungsinformationen, die für B2C- oder B2B-Sites gesetzlich vorgeschrieben sind, und enthalten die Rechte des Käufers und Verkäufers. Die Meldung &quot;Allgemeine Geschäftsbedingungen&quot;erscheint nach den Zahlungsinformationen direkt vor dem _Bestellung platzieren_ Schaltfläche.

![Geschäftsbedingungen beim Checkout](./assets/storefront-checkout-step2-terms-conditions.png){width="700" zoomable="yes"}

## Schritt 1: Nutzungsbedingungen für das Auschecken aktivieren

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen **[!UICONTROL Checkout]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Checkout Options]** Abschnitt.

   ![Checkout-Optionen](../configuration-reference/sales/assets/checkout-checkout-options.png){width="600" zoomable="yes"}

1. Stellen Sie sicher, dass **[!UICONTROL Enable Onepage Checkout]** auf `Yes`.

1. Satz **[!UICONTROL Enable Terms and Conditions]** nach `Yes`.

1. Klicken **[!UICONTROL Save Config]**.

## Schritt 2: Hinzufügen eigener Informationen zu den Geschäftsbedingungen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Terms and Conditions]**.

   ![Raster &quot;Allgemeine Geschäftsbedingungen&quot;](./assets/terms-conditions.png){width="600" zoomable="yes"}

1. Klicken Sie oben rechts auf **[!UICONTROL Add New Condition]**.

1. Geben Sie die **[!UICONTROL Condition Name]** für interne Referenzzwecke.

   ![Neue Bedingung](./assets/terms-conditions-new.png){width="600" zoomable="yes"}

1. Satz **[!UICONTROL Status]** nach `Enabled`.

1. Satz **[!UICONTROL Applied]** auf einen der folgenden Werte zu:

   - `Automatically` - Bedingungen werden automatisch beim Checkout akzeptiert.
   - `Manually` - Kunden müssen die Bedingungen für die Bestellung manuell akzeptieren.

1. Satz **[!UICONTROL Show Content as]** auf einen der folgenden Werte zu:

   - `Text` - Zeigt den Inhalt der Geschäftsbedingungen als nicht formatierten Text an.
   - `HTML` - Zeigt den Inhalt als HTML an, der formatiert werden kann.

1. Jede Auswahl **[!UICONTROL Store View]** wo Sie diese Geschäftsbedingungen verwenden möchten.

1. Scrollen Sie nach unten und füllen Sie die angezeigten Informationen aus:

   - Geben Sie die **[!UICONTROL Checkbox Text]** als Text für den Link Allgemeine Geschäftsbedingungen verwendet werden. Beispiel, `I understand and accept the terms and conditions of the sale`.

   - Im **[!UICONTROL Content]** den vollständigen Wortlaut der Verkaufsbedingungen ein.

1. (Optional) Geben Sie die **[!UICONTROL Content Height (css)]** in Pixel, um die Höhe des Textfelds zu bestimmen, in dem die Erklärung zu den Geschäftsbedingungen während des Auscheckens angezeigt wird.

   Um beispielsweise das Textfeld auf einem 96-dpi-Display 1 Zoll hoch zu machen, geben Sie `96`. Eine Bildlaufleiste wird angezeigt, wenn der Inhalt über die Höhe des Felds hinausgeht.

1. Klicken **[!UICONTROL Save Condition]**.
