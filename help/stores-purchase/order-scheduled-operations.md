---
title: Geplante Bestellvorgänge
description: Erfahren Sie mehr über die geplanten Bestellvorgänge und Cron-Einstellungen für Bestellungen, die diese Funktion unterstützen.
exl-id: 330fe75a-d901-4696-946e-fa7af9ea3d40
feature: Orders, Configuration
source-git-commit: db859c40cd6f052a8f1153e245c23d9f1ea97d33
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# Geplante Bestellvorgänge

Verwenden Sie [Cron](../systems/cron.md)-Aufträge, um die folgenden Auftragsverarbeitungsaufgaben zu planen:

![Auftragsraster](./assets/orders-grid.png){width="700" zoomable="yes"}

## Ausstehende Lebensdauer von Zahlungsaufträgen festlegen

Die Lebensdauer von Bestellungen mit ausstehenden Zahlungen wird durch die Konfiguration _Bestellungen Cron-Einstellungen_ bestimmt. Der Standardwert ist 480 Minuten, d. h. acht Stunden.

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Abschnitt **[!UICONTROL Sales]** und wählen Sie darunter **[!UICONTROL Sales]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Orders Cron Settings]** .

   ![Bestellungen Cron-Einstellungen](../configuration-reference/sales/assets/sales-orders-cron-settings.png){width="600" zoomable="yes"}

1. Geben Sie **[!UICONTROL Pending Payment Order Lifetime (minutes)]** die Anzahl der Minuten ein, nach denen eine ausstehende Zahlung abläuft.

1. Klicken Sie auf **[!UICONTROL Save Config]**.

## Geplante Rasteraktualisierungen und Neuindizierungen aktivieren

Die Konfiguration der Rastereinstellungen plant Aktualisierungen an den folgenden Auftragsverwaltungsrastern und indiziert die Daten wie von [Cron](../systems/cron.md) geplant neu:

- [Bestellungen](orders.md#orders-workspace)
- [Rechnungen](invoices.md)
- [Sendungen](shipments.md)
- [Gutschriften](credit-memos.md)

Durch die Planung dieser Aufgaben können Sie die Sperren vermeiden, die beim Speichern von Daten auftreten, und die Verarbeitungszeit verkürzen. Wenn diese Option aktiviert ist, finden Aktualisierungen nur während des geplanten Cron-Auftrags statt. Für optimale Ergebnisse sollte Cron so konfiguriert werden, dass es einmal pro Minute ausgeführt wird.

**_So aktivieren Sie die Aktualisierungen und Neuindizierungen:_**

Wenn [Produktionsmodus](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html?lang=de#production-mode) (der in Adobe Commerce in der Cloud-Infrastruktur verwendete Standardmodus) aktiviert ist, führen Sie den folgenden Befehl aus:

``bin/magento config:set dev/grid/async_indexing 1``

Wenn [Standardmodus](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html?lang=de#default-mode) aktiviert ist, führen Sie die folgenden Schritte aus:

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Abschnitt **[!UICONTROL Advanced]** und wählen Sie **[!UICONTROL Developer]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Grid Settings]** .

1. Legen Sie **[!UICONTROL Asynchronous Indexing]** auf `Enable` fest.

   ![Rastereinstellungen](../configuration-reference/advanced/assets/developer-grid-settings.png){width="600" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Save Config]**.
