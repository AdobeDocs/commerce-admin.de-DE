---
title: Bildoptimierung der Media Gallery
description: Erfahren Sie, wie Sie die Bildoptimierung für Ihre [!DNL Commerce] Medien-Assets.
exl-id: ba75e90a-406b-4b14-b049-0b78c4a27188
feature: Page Content, Media
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---

# Bildoptimierung der Media Gallery

Die neue [Media Gallery](media-gallery.md) bietet eine _Bildoptimierung_ -Funktion, die die Leistung verbessert und die Größe der Mediendateien im Storefront verringert. Diese Optimierung ist standardmäßig aktiviert und kann in den Store-Konfigurationseinstellungen geändert werden.

## Bildoptimierung konfigurieren

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Advanced]** und wählen **[!UICONTROL System]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery Image Optimization]** und gehen Sie wie folgt vor:

   - Satz **[!UICONTROL Enable Image Optimization]** nach `Yes`.
   - Geben Sie die **[!UICONTROL Maximum Width]** und **[!UICONTROL Maximum Height]** -Werte (in Pixel) entsprechend Ihren Anforderungen.

## Verhalten

Wenn die Bildoptimierungsfunktion der Media Gallery aktiviert ist, wird automatisch eine optimierte Kopie eines Bildes aus dem [Media Gallery](media-gallery.md) anstelle der Originaldatei.

Wenn die Variable _Maximale Breite_ und _Maximale Höhe_ -Werte in der Konfiguration geändert werden, werden alle vorhandenen optimierten Bilder aktualisiert, die zuvor eingefügt wurden.

Für die Bildoptimierung der Media Gallery muss die Variable `media.gallery.renditions.update` Kunden in der Warteschlange werden zum erneuten Generieren optimierter Bilder ausgeführt, wenn die Konfiguration geändert wird. Siehe [Verwalten von Nachrichtenwarteschlangen](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) im _Konfigurationshandbuch_ für weitere Details.
