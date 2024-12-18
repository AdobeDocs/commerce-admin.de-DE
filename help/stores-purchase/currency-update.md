---
title: Währungskurse aktualisieren
description: Erfahren Sie, wie Sie Währungskurse manuell festlegen oder in Ihren Store importieren.
exl-id: 316a7bc8-1118-46e7-82ff-891ada04cd13
feature: Currency, Configuration, Data Import/Export
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '271'
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

   Die aktualisierten Tarife werden in der Liste _[!UICONTROL Currency Rates]_angezeigt. Wenn sich die Kurse seit der letzten Aktualisierung geändert haben, wird der alte Kurs unten als Referenz angezeigt.

1. Klicken Sie abschließend auf **[!UICONTROL Save Currency Rates]**.

1. Wenn Sie aufgefordert werden, den Cache zu aktualisieren, klicken Sie auf den Link **[!UICONTROL Cache Management]** und aktualisieren Sie den ungültigen Cache.

   ![Systemmeldung - Aktualisieren Sie den ungültigen Cache](./assets/currency-cache-update.png){width="600" zoomable="yes"}

## Währungskurse planmäßig importieren

1. Stellen Sie sicher[ dass &quot;](../systems/cron.md)&quot; für Ihren Store aktiviert ist.

1. Um die Währungen anzugeben, die Sie akzeptieren, und die Importverbindung und den Zeitplan einzurichten, schließen Sie die Einrichtung [Währungskurses“ ](currency-configuration.md).

1. Um sicherzustellen, dass die Tarife planmäßig importiert werden, überprüfen Sie die _[!UICONTROL Currency Rates]_.

1. Warten Sie auf den Zeitraum der für den Zeitplan festgelegten Häufigkeitseinstellung und überprüfen Sie die Tarife erneut.
