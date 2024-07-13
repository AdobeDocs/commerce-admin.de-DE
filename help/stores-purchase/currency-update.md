---
title: Aktualisieren von Währungskursen
description: Erfahren Sie, wie Sie Währungsraten manuell festlegen oder in Ihren Speicher importieren können.
exl-id: 316a7bc8-1118-46e7-82ff-891ada04cd13
feature: Currency, Configuration, Data Import/Export
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# Aktualisieren von Währungskursen

Währungsraten können manuell festgelegt oder in den Store importiert werden. Um sicherzustellen, dass Ihr Store über die aktuellsten Tarife verfügt, können Sie die Währungsraten so konfigurieren, dass sie automatisch planmäßig aktualisiert werden.

Bevor Sie Währungskurse importieren, führen Sie die [Einrichtung des Währungskurses](currency-configuration.md) durch, um die Währungen anzugeben, die Sie akzeptieren, und um die Importverbindung und den Zeitplan festzulegen.

![Währungskurse](./assets/stores-currency-rate-update.png){width="600" zoomable="yes"}

## Manuelles Aktualisieren der Währungsrate

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Currency]_>**[!UICONTROL Currency Rates]**.

1. Klicken Sie auf den Wechselkurs, den Sie ändern möchten, und geben Sie für jede unterstützte Währung den neuen Wert ein.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Currency Rates]**.

## Währungskurse importieren

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Currency]_>**[!UICONTROL Currency Rates]**.

1. Setzen Sie **[!UICONTROL Import Service]** auf den Währungskursanbieter.

   Der Standardanbieter ist `fixer.io (legacy)`.

   >[!IMPORTANT]
   >
   >Ab Version 2.4.6 wird der Dienst [[!DNL Fixer.io]](https://fixer.io/) nicht mehr unterstützt und durch den Dienst [[!DNL Fixer API] (APILayer)](https://apilayer.com/marketplace/fixer-api) ersetzt. Es wird dringend empfohlen, ein APILayer-Konto anstelle eines veralteten [!DNL Fixer.io] -Kontos zu verwenden.

1. Klicken Sie auf **[!UICONTROL Import]**.

   Die aktualisierten Raten werden in der Liste _[!UICONTROL Currency Rates]_angezeigt. Wenn sich die Tarife seit der letzten Aktualisierung geändert haben, wird die alte Rate unten als Referenz angezeigt.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Currency Rates]**.

1. Wenn Sie aufgefordert werden, den Cache zu aktualisieren, klicken Sie auf den Link **[!UICONTROL Cache Management]** und aktualisieren Sie den ungültigen Cache.

   ![Systemmeldung - Aktualisieren des ungültigen Caches](./assets/currency-cache-update.png){width="600" zoomable="yes"}

## Währungskurse planmäßig importieren

1. Stellen Sie sicher, dass [Cron](../systems/cron.md) für Ihren Store aktiviert ist.

1. Um die Währungen anzugeben, die Sie akzeptieren, die Importverbindung herzustellen und den Zeitplan festzulegen, führen Sie die [Einrichtung der Währungsrate](currency-configuration.md) durch.

1. Um sicherzustellen, dass die Tarife planmäßig importiert werden, überprüfen Sie die Liste _[!UICONTROL Currency Rates]_.

1. Warten Sie auf den für den Zeitplan festgelegten Zeitraum der Frequenzeinstellung und überprüfen Sie die Tarife erneut.
