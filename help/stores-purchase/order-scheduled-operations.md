---
title: Vorgänge für geplante Aufträge
description: Erfahren Sie mehr über die Cron-Einstellungen für geplante Bestellungsvorgänge und Bestellungen, die diese Funktion unterstützen.
exl-id: 330fe75a-d901-4696-946e-fa7af9ea3d40
feature: Orders, Configuration
source-git-commit: db859c40cd6f052a8f1153e245c23d9f1ea97d33
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# Vorgänge für geplante Aufträge

Verwenden Sie [Cron](../systems/cron.md)-Aufträge, um die folgenden Auftragsverarbeitungsaufgaben zu planen:

![Raster &quot;Bestellungen&quot;](./assets/orders-grid.png){width="700" zoomable="yes"}

## Lebensdauer ausstehender Zahlungsaufträge festlegen

Die Lebensdauer von Bestellungen mit ausstehenden Zahlungen wird durch die Konfiguration der _Bestellungen-Cron-Einstellungen_ bestimmt. Der Standardwert ist auf 480 Minuten festgelegt, was acht Stunden entspricht.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Abschnitt **[!UICONTROL Sales]** und wählen Sie unter &quot;**[!UICONTROL Sales]**&quot;.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Orders Cron Settings]** .

   ![Bestellungen Cron Settings](../configuration-reference/sales/assets/sales-orders-cron-settings.png){width="600" zoomable="yes"}

1. Geben Sie für &quot;**[!UICONTROL Pending Payment Order Lifetime (minutes)]**&quot;die Anzahl der Minuten ein, bevor eine ausstehende Zahlung abläuft.

1. Klicken Sie auf **[!UICONTROL Save Config]**.

## Geplante Rasteraktualisierungen und Neuindizierungen aktivieren

Die Konfiguration der Rastereinstellungen plant Aktualisierungen an den folgenden Rastern für die Auftragsverwaltung und deklariert die Daten gemäß der Planung von [Cron](../systems/cron.md) neu:

- [Bestellungen](orders.md#orders-workspace)
- [Rechnungen](invoices.md)
- [Sendungen](shipments.md)
- [Credit Memos](credit-memos.md)

Durch die Planung dieser Aufgaben können Sie Sperren vermeiden, die beim Speichern von Daten auftreten, und die Verarbeitungszeit verkürzen. Wenn diese Option aktiviert ist, finden Aktualisierungen nur während des geplanten Cron-Auftrags statt. Um die besten Ergebnisse zu erzielen, sollte Cron so konfiguriert werden, dass er jede Minute einmal ausgeführt wird.

**_So aktivieren Sie die Aktualisierungen und Neuindizierungen:_**

Wenn der [Produktionsmodus](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html#production-mode) (der Standardmodus, der in Adobe Commerce in der Cloud-Infrastruktur verwendet wird) aktiviert ist, führen Sie den folgenden Befehl aus:

``bin/magento config:set dev/grid/async_indexing 1``

Wenn [Standardmodus](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html#default-mode) aktiviert ist, führen Sie die folgenden Schritte aus:

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Abschnitt **[!UICONTROL Advanced]** und wählen Sie **[!UICONTROL Developer]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Grid Settings]** .

1. Setzen Sie **[!UICONTROL Asynchronous Indexing]** auf `Enable`.

   ![Rastereinstellungen](../configuration-reference/advanced/assets/developer-grid-settings.png){width="600" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Save Config]**.
