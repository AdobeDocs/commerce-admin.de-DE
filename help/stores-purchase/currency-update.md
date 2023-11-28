---
title: Aktualisieren von Währungskursen
description: Erfahren Sie, wie Sie Währungsraten manuell festlegen oder in Ihren Speicher importieren können.
exl-id: 316a7bc8-1118-46e7-82ff-891ada04cd13
feature: Currency, Configuration, Data Import/Export
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---

# Aktualisieren von Währungskursen

Währungsraten können manuell festgelegt oder in den Store importiert werden. Um sicherzustellen, dass Ihr Store über die aktuellsten Tarife verfügt, können Sie die Währungsraten so konfigurieren, dass sie automatisch planmäßig aktualisiert werden.

Bevor Sie Währungskurse importieren, müssen Sie die Variable [Währungsrateneinrichtung](currency-configuration.md) um die Währungen anzugeben, die Sie akzeptieren, und um die Importverbindung und den Zeitplan festzulegen.

![Währungskurse](./assets/stores-currency-rate-update.png){width="600" zoomable="yes"}

## Manuelles Aktualisieren der Währungsrate

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Currency]_>**[!UICONTROL Currency Rates]**.

1. Klicken Sie auf den Wechselkurs, den Sie ändern möchten, und geben Sie für jede unterstützte Währung den neuen Wert ein.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Currency Rates]**.

## Währungskurse importieren

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Currency]_>**[!UICONTROL Currency Rates]**.

1. Satz **[!UICONTROL Import Service]** an den Währungskursanbieter.

   Der Standardanbieter ist `fixer.io (legacy)`.

   >[!IMPORTANT]
   >
   >Ab Version 2.4.6 wird die [[!DNL Fixer.io]](https://fixer.io/) -Dienst veraltet ist und durch die [[!DNL Fixer API] (APILayer)](https://apilayer.com/marketplace/fixer-api) -Dienst. Es wird dringend empfohlen, ein APILayer-Konto anstelle eines veralteten zu verwenden [!DNL Fixer.io] -Konto.

1. Klicken **[!UICONTROL Import]**.

   Die aktualisierten Raten werden im _[!UICONTROL Currency Rates]_Liste. Wenn sich die Tarife seit der letzten Aktualisierung geändert haben, wird die alte Rate unten als Referenz angezeigt.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Currency Rates]**.

1. Wenn Sie aufgefordert werden, den Cache zu aktualisieren, klicken Sie auf die **[!UICONTROL Cache Management]** verknüpfen und den ungültigen Cache aktualisieren.

   ![Systemmeldung - Aktualisieren des ungültigen Caches](./assets/currency-cache-update.png){width="600" zoomable="yes"}

## Währungskurse planmäßig importieren

1. Stellen Sie sicher, dass [Cron](../systems/cron.md) für Ihren Store aktiviert ist.

1. Um die akzeptierten Währungen anzugeben und die Importverbindung herzustellen und den Zeitplan festzulegen, müssen Sie die Variable [Einrichtung der Währungsrate](currency-configuration.md).

1. Um sicherzustellen, dass die Tarife planmäßig importiert werden, überprüfen Sie das _[!UICONTROL Currency Rates]_Liste.

1. Warten Sie auf den für den Zeitplan festgelegten Zeitraum der Frequenzeinstellung und überprüfen Sie die Tarife erneut.
