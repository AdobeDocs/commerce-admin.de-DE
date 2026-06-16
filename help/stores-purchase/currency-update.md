---
title: Währungskurse aktualisieren
description: Erfahren Sie, wie Sie Währungskurse manuell festlegen oder in Ihren Store importieren.
exl-id: 316a7bc8-1118-46e7-82ff-891ada04cd13
feature: Currency, Configuration, Data Import/Export
TQID: https://experienceleague.adobe.com/tEt15Mzt7MeDtf6MZfu9n6EsvJKUCNBdGhUo0-RK3zk
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
source-wordcount: 275
ht-degree: 0%

---

# Währungskurse aktualisieren

Die Währungskurse können manuell festgelegt oder in den Store importiert werden. Um sicherzustellen, dass Ihr Geschäft über die aktuellen Kurse verfügt, können Sie die Währungskurse so konfigurieren, dass sie automatisch planmäßig aktualisiert werden.

Bevor Sie Währungskurse importieren, schließen Sie die [Währungskurseinrichtung“ ab](currency-configuration.md) um die akzeptierten Währungen anzugeben und die Importverbindung und den Zeitplan einzurichten.

![Währungskurse](./assets/stores-currency-rate-update.png){width="600" zoomable="yes"}

## Wechselkurs manuell aktualisieren

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Currency]_>**[!UICONTROL Currency Rates]**.

1. Klicken Sie auf den Kurs, den Sie ändern möchten, und geben Sie den neuen Wert für jede unterstützte Währung ein.

1. Klicken Sie abschließend auf **[!UICONTROL Save Currency Rates]**.

## Währungskurse importieren

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Currency]_>**[!UICONTROL Currency Rates]**.

1. Legen Sie **[!UICONTROL Import Service]** auf den Währungskursanbieter fest.

   Der Standardanbieter ist `fixer.io (legacy)`.

   >[!IMPORTANT]
   >
   >Ab Version 2.4.6 wird der [[!DNL Fixer.io]](https://fixer.io/)-Service nicht mehr unterstützt und durch den Service [[!DNL Fixer API] (APILayer)](https://apilayer.com/marketplace/fixer-api) ersetzt. Es wird dringend empfohlen, ein APILayer-Konto anstelle eines veralteten [!DNL Fixer.io]-Kontos zu verwenden.

1. Klicken Sie auf **[!UICONTROL Import]**.

   Die aktualisierten Tarife werden in der Liste _[!UICONTROL Currency Rates]_&#x200B;angezeigt. Wenn sich die Kurse seit der letzten Aktualisierung geändert haben, wird der alte Kurs unten als Referenz angezeigt.

1. Klicken Sie abschließend auf **[!UICONTROL Save Currency Rates]**.

1. Wenn Sie aufgefordert werden, den Cache zu aktualisieren, klicken Sie auf den Link **[!UICONTROL Cache Management]** und aktualisieren Sie den ungültigen Cache.

   ![Systemmeldung - Aktualisieren Sie den ungültigen Cache](./assets/currency-cache-update.png){width="600" zoomable="yes"}

## Währungskurse planmäßig importieren

1. Stellen Sie sicher[&#x200B; dass &quot;](../systems/cron.md)&quot; für Ihren Store aktiviert ist.

1. Um die Währungen anzugeben, die Sie akzeptieren, und die Importverbindung und den Zeitplan einzurichten, schließen Sie die Einrichtung [Währungskurses“ &#x200B;](currency-configuration.md).

1. Um sicherzustellen, dass die Tarife planmäßig importiert werden, überprüfen Sie die _[!UICONTROL Currency Rates]_.

1. Warten Sie auf den Zeitraum der für den Zeitplan festgelegten Häufigkeitseinstellung und überprüfen Sie die Tarife erneut.
