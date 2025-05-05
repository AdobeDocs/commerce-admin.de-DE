---
title: Media Gallery-Bildoptimierung
description: Erfahren Sie, wie Sie die Bildoptimierung für Ihre Medien [!DNL Commerce] Assets verwenden.
exl-id: ba75e90a-406b-4b14-b049-0b78c4a27188
feature: Page Content, Media
source-git-commit: a93e96353f4be0e771064cdcfbdf794772386a28
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---

# Media Gallery-Bildoptimierung

Die neue [Mediensammlung](media-gallery.md) bietet eine Funktion _Bildoptimierung_, die die Leistung verbessert und die Größe der Mediendateien in der Storefront verringert. Diese Optimierung ist standardmäßig aktiviert und kann in den Store-Konfigurationseinstellungen geändert werden.

## Konfigurieren der Bildoptimierung

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Advanced]** und wählen Sie **[!UICONTROL System]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery Image Optimization]** und führen Sie folgende Schritte aus:

   - Legen Sie **[!UICONTROL Enable Image Optimization]** auf `Yes` fest.
   - Geben Sie die **[!UICONTROL Maximum Width]** und **[!UICONTROL Maximum Height]** Werte (in Pixeln) entsprechend Ihren Anforderungen ein.

## Verhalten

Wenn die Bildoptimierungsfunktion der Mediensammlung aktiviert ist, wird automatisch eine optimierte Kopie eines Bildes anstelle der Originaldatei in den Inhalt [Mediensammlung](media-gallery.md) eingefügt.

Wenn die Werte _Maximale Breite_ und _Maximale Höhe_ in der Konfiguration geändert werden, werden alle vorhandenen optimierten Bilder aktualisiert, die zuvor eingefügt wurden.

Für die Bildoptimierung der Mediensammlung ist es erforderlich, dass die Verbraucher der `media.gallery.renditions.update`-Warteschlange ausgeführt werden, um optimierte Bilder neu zu generieren, wenn die Konfiguration geändert wird. Weitere [ finden Sie unter „Verwalten ](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html?lang=de) Nachrichtenwarteschlangen _im_ Konfigurationshandbuch“.

{{$include /help/_includes/image-optimization-animated-gif-note.md}}
