---
title: Allgemeine Geschäftsbedingungen für den Checkout
description: Erfahren Sie mehr über die Geschäftsbedingungen, die für Ihren Store konfiguriert werden können.
exl-id: 59ba6385-3cc6-43e8-b984-5c26516bba88
feature: Checkout, Compliance
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 0%

---

# Allgemeine Geschäftsbedingungen für den Checkout

Wenn die _Funktion „Allgemeine Geschäftsbedingungen_ aktiviert ist, müssen Kunden den allgemeinen Geschäftsbedingungen des Verkaufs zustimmen, bevor der Kauf abgeschlossen ist. Die Geschäftsbedingungen des Verkaufs enthalten in der Regel Offenlegungsinformationen, die gesetzlich für B2C- oder B2B-Sites erforderlich sein können, und beschreiben die Rechte des Käufers und Verkäufers. Die Nachricht Geschäftsbedingungen wird nach den Zahlungsinformationen, direkt vor der Schaltfläche _Bestellung aufgeben_ angezeigt.

![Allgemeine Geschäftsbedingungen an der Kasse](./assets/storefront-checkout-step2-terms-conditions.png){width="700" zoomable="yes"}

## Schritt 1: Aktivieren der allgemeinen Geschäftsbedingungen für den Checkout

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Checkout]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Checkout Options]** .

   ![Checkout-Optionen](../configuration-reference/sales/assets/checkout-checkout-options.png){width="600" zoomable="yes"}

1. Stellen Sie sicher, dass **[!UICONTROL Enable Onepage Checkout]** auf `Yes` gesetzt ist.

1. Legen Sie **[!UICONTROL Enable Terms and Conditions]** auf `Yes` fest.

1. Klicken Sie auf **[!UICONTROL Save Config]**.

## Schritt 2: Fügen Sie Ihre eigenen Geschäftsbedingungen hinzu

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Terms and Conditions]**.

   ![Raster für Nutzungsbedingungen](./assets/terms-conditions.png){width="600" zoomable="yes"}

1. Klicken Sie oben rechts auf **[!UICONTROL Add New Condition]**.

1. Geben Sie die **[!UICONTROL Condition Name]** als interne Referenz ein.

   ![Neue Bedingung](./assets/terms-conditions-new.png){width="600" zoomable="yes"}

1. Legen Sie **[!UICONTROL Status]** auf `Enabled` fest.

1. Legen Sie **[!UICONTROL Applied]** auf eine der folgenden Einstellungen fest:

   - `Automatically` - Bedingungen werden beim Checkout automatisch akzeptiert.
   - `Manually` - Kunden müssen die Bedingungen für die Auftragserteilung manuell akzeptieren.

1. Legen Sie **[!UICONTROL Show Content as]** auf eine der folgenden Einstellungen fest:

   - `Text` - Zeigt den Inhalt der allgemeinen Geschäftsbedingungen als unformatierten Text an.
   - `HTML` - Zeigt den Inhalt als HTML an, die formatiert werden kann.

1. Wählen Sie jedes **[!UICONTROL Store View]** aus, in dem diese Nutzungsbedingungen verwendet werden sollen.

1. Scrollen Sie nach unten und füllen Sie die anzuzeigenden Informationen aus:

   - Geben Sie die **[!UICONTROL Checkbox Text]** ein, die als Text für den Link für die Nutzungsbedingungen verwendet werden soll. Beispiel: `I understand and accept the terms and conditions of the sale`.

   - Geben Sie in das **[!UICONTROL Content]** den vollständigen Text der Verkaufsbedingungen ein.

1. (Optional) Geben Sie die **[!UICONTROL Content Height (css)]** in Pixeln ein, um die Höhe des Textfelds zu bestimmen, in dem die Anweisung für Nutzungsbedingungen während des Checkouts angezeigt wird.

   Um beispielsweise das Textfeld auf einem 96-dpi-Display 1 Zoll hoch zu halten, geben Sie `96` ein. Eine Bildlaufleiste wird angezeigt, wenn der Inhalt über die Höhe des Felds hinausgeht.

1. Klicken Sie auf **[!UICONTROL Save Condition]**.
