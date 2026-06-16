---
title: Allgemeine Geschäftsbedingungen für den Checkout
description: Erfahren Sie mehr über die Geschäftsbedingungen, die für Ihren Store konfiguriert werden können.
exl-id: 59ba6385-3cc6-43e8-b984-5c26516bba88
feature: Checkout, Compliance
TQID: https://experienceleague.adobe.com/xHlKdFJPVInadvAyFbs6jFYz4AECWJdkbV8FRoHxE8U
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 325
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
