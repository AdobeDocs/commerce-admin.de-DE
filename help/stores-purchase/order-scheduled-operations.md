---
title: Vorgänge für geplante Aufträge
description: Erfahren Sie mehr über die Cron-Einstellungen für geplante Bestellungsvorgänge und Bestellungen, die diese Funktion unterstützen.
exl-id: 330fe75a-d901-4696-946e-fa7af9ea3d40
feature: Orders, Configuration
source-git-commit: db859c40cd6f052a8f1153e245c23d9f1ea97d33
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---

# Vorgänge für geplante Aufträge

Verwendung [Cron](../systems/cron.md) Aufträge zur Planung der folgenden Auftragsverarbeitungsaufgaben:

![Raster &quot;Bestellungen&quot;](./assets/orders-grid.png){width="700" zoomable="yes"}

## Lebensdauer ausstehender Zahlungsaufträge festlegen

Die Gültigkeitsdauer von Aufträgen mit ausstehenden Zahlungen wird durch die Variable _Bestellungen Cron-Einstellungen_ Konfiguration. Der Standardwert ist auf 480 Minuten festgelegt, was acht Stunden entspricht.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den **[!UICONTROL Sales]** auswählen **[!UICONTROL Sales]** darunter.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Orders Cron Settings]** Abschnitt.

   ![Bestellungen Cron-Einstellungen](../configuration-reference/sales/assets/sales-orders-cron-settings.png){width="600" zoomable="yes"}

1. Für **[!UICONTROL Pending Payment Order Lifetime (minutes)]**, geben Sie die Anzahl der Minuten ein, bevor eine ausstehende Zahlung abläuft.

1. Klicken **[!UICONTROL Save Config]**.

## Geplante Rasteraktualisierungen und Neuindizierungen aktivieren

Die Konfiguration der Rastereinstellungen plant Aktualisierungen an den folgenden Rastern zur Verwaltung der Reihenfolge und deklariert die Daten neu, wie dies für [Cron](../systems/cron.md):

- [Bestellungen](orders.md#orders-workspace)
- [Rechnungen](invoices.md)
- [Sendungen](shipments.md)
- [Credit Memos](credit-memos.md)

Durch die Planung dieser Aufgaben können Sie Sperren vermeiden, die beim Speichern von Daten auftreten, und die Verarbeitungszeit verkürzen. Wenn diese Option aktiviert ist, finden Aktualisierungen nur während des geplanten Cron-Auftrags statt. Um die besten Ergebnisse zu erzielen, sollte Cron so konfiguriert werden, dass er jede Minute einmal ausgeführt wird.

**_So aktivieren Sie die Aktualisierungen und die Neuindizierung:_**

Wann [Produktionsmodus](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html#production-mode) (der Standardmodus, der in Adobe Commerce in der Cloud-Infrastruktur verwendet wird) aktiviert ist, führen Sie den folgenden Befehl aus:

``bin/magento config:set dev/grid/async_indexing 1``

Wann [Standardmodus](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html#default-mode) aktiviert ist, führen Sie die folgenden Schritte aus:

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den **[!UICONTROL Advanced]** auswählen **[!UICONTROL Developer]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Grid Settings]** Abschnitt.

1. Satz **[!UICONTROL Asynchronous Indexing]** nach `Enable`.

   ![Rastereinstellungen](../configuration-reference/advanced/assets/developer-grid-settings.png){width="600" zoomable="yes"}

1. Klicken **[!UICONTROL Save Config]**.
