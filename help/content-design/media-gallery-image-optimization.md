---
title: Bildoptimierung der Media Gallery
description: Erfahren Sie, wie Sie die Bildoptimierung für Ihre [!DNL Commerce] Medien-Assets verwenden.
exl-id: ba75e90a-406b-4b14-b049-0b78c4a27188
feature: Page Content, Media
source-git-commit: a93e96353f4be0e771064cdcfbdf794772386a28
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---

# Bildoptimierung der Media Gallery

Die neue [Mediengalerie](media-gallery.md) bietet eine Funktion zur _Bildoptimierung_, die die Leistung verbessert und die Größe der Mediendateien im Storefront verringert. Diese Optimierung ist standardmäßig aktiviert und kann in den Store-Konfigurationseinstellungen geändert werden.

## Bildoptimierung konfigurieren

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Advanced]** und wählen Sie **[!UICONTROL System]** aus.

1. Erweitern Sie ![Erweiterungsselektor](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery Image Optimization]** und führen Sie folgende Schritte aus:

   - Setzen Sie **[!UICONTROL Enable Image Optimization]** auf `Yes`.
   - Geben Sie die Werte **[!UICONTROL Maximum Width]** und **[!UICONTROL Maximum Height]** (in Pixel) entsprechend Ihren Anforderungen ein.

## Verhalten

Wenn die Bildoptimierungsfunktion der Media Gallery aktiviert ist, wird automatisch eine optimierte Kopie eines Bildes aus der [Mediengalerie](media-gallery.md) anstelle der Originaldatei in den Inhalt eingefügt.

Wenn die Werte _Maximale Breite_ und _Maximale Höhe_ in der Konfiguration geändert werden, werden alle vorhandenen optimierten Bilder aktualisiert, die zuvor eingefügt wurden.

Für die Bildoptimierung der Media Gallery ist es erforderlich, dass die Verbraucher der `media.gallery.renditions.update`-Warteschlange für die Neugenerierung optimierter Bilder ausgeführt werden, wenn die Konfiguration geändert wird. Weitere Informationen finden Sie unter [Verwalten von Nachrichtenwarteschlangen](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) im _Konfigurationshandbuch_ .

{{$include /help/_includes/image-optimization-animated-gif-note.md}}
