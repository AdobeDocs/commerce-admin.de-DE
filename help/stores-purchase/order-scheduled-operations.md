---
title: Geplante Bestellvorgänge
description: Erfahren Sie mehr über die geplanten Bestellvorgänge und Cron-Einstellungen für Bestellungen, die diese Funktion unterstützen.
exl-id: 330fe75a-d901-4696-946e-fa7af9ea3d40
feature: Orders, Configuration
TQID: https://experienceleague.adobe.com/pViPmBFGErjXeFyvBNBVuJiw8Pn51JIGkeZ2mJAf72M
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
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
source-wordcount: 284
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

[!BADGE Nur PaaS]{type=Informative url="https://experienceleague.adobe.com/de/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."} Wenn [Produktionsmodus](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html?lang=de#production-mode) (der in Adobe Commerce in der Cloud-Infrastruktur verwendete Standardmodus) aktiviert ist, führen Sie den folgenden Befehl aus:

`bin/magento config:set dev/grid/async_indexing 1`

Wenn [Standardmodus](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html?lang=de#default-mode) aktiviert ist, führen Sie die folgenden Schritte aus:

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Abschnitt **[!UICONTROL Advanced]** und wählen Sie **[!UICONTROL Developer]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Grid Settings]** .

1. Legen Sie **[!UICONTROL Asynchronous Indexing]** auf `Enable` fest.

   ![Rastereinstellungen](../configuration-reference/advanced/assets/developer-grid-settings.png){width="600" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Save Config]**.
