---
title: Die [!DNL Media Gallery]
description: Verwenden Sie die Media Gallery, um Ihre Mediendateien auf dem Server zu organisieren und zu verwalten.
exl-id: bf730e46-70f3-405c-88cf-62d0a3e8634f
feature: Page Content, Media
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# Die [!DNL Media Gallery]

Mit Adobe Commerce oder Magento Open Source 2.4 können Händler die neue _verbessert_ [!DNL Media Gallery] um ihre Mediendateien auf dem Server zu organisieren und zu verwalten. Diese neue [!DNL Media Gallery] enthält dieselben Funktionen wie der vorhandene Medienspeicher, umfasst jedoch eine verbesserte Benutzeroberfläche und eine engere Integration mit [Adobe Stock][adobe-stock].

![Im Raster &quot;Media Gallery&quot;angezeigte Bilder](./assets/media-gallery-grid.png){width="700" zoomable="yes"}

>[!NOTE]
>
>Produktbilder, die zum [_[!UICONTROL Images and Videos]_Produktabschnitt](../catalog/product-image.md#upload-an-image) werden nicht von der [!DNL Media Gallery]. Nur Bilder, die in_[!UICONTROL Content]_ Produktbereichsfelder werden angezeigt und in der neuen [!DNL Media Gallery].

## Aktivieren Sie das neue [!DNL Media Gallery]

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Advanced]** und wählen **[!UICONTROL System]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery]**.

   ![Erweiterte Konfiguration - [!DNL Media Gallery]](./assets/system-media-gallery.png){width="600" zoomable="yes"}

1. Satz **[!UICONTROL Enable Old Media Gallery]** nach `No`.

1. Klicken **[!UICONTROL Save Config]**.

1. Klicken Sie bei Aufforderung auf das **[!UICONTROL Cache Management]** in der Systemmeldung und aktualisieren Sie den ungültigen Cache.

   Die [[!UICONTROL Content] Menü](/help/content-design/content-menu.md) zeigt jetzt die neue _[!UICONTROL Media Gallery]_-Option.

>[!NOTE]
>
>Vollständige Funktionalität für neue [!DNL Media Gallery] erfordert `media.gallery.synchronization` und `media.content.synchronization` Verbraucher in die Warteschlange einreihen, die für die Erstsynchronisierung gestartet werden sollen. Siehe [Verwalten von Nachrichtenwarteschlangen](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) im _Konfigurationshandbuch_ für weitere Details.

## Zugriff auf die neuen [!DNL Media Gallery]

Die neue [!DNL Media Gallery] über das Menü &quot;Inhalt&quot;oder wenn Sie [Hinzufügen oder Bearbeiten einer Seite](/help/content-design/page-add.md). Sie können auch darauf zugreifen, wenn Sie [Erstellen oder Bearbeiten von Kategorien](/help/catalog/category-create.md)oder wenn Sie [Bilder mit dem Inhaltseditor einfügen](/help/content-design/editor-insert-image.md).

So greifen Sie auf das neue [!UICONTROL Media Gallery] durch die [!UICONTROL Content] Menü:

- Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

So greifen Sie beim Hinzufügen oder Bearbeiten einer Seite auf die neue Mediengalerie zu:

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Klicken **[!UICONTROL Add a New Page]**.

   Wenn Sie eine vorhandene Seite bearbeiten möchten, können Sie die _[!UICONTROL Action]_Zu klickende Spalte **[!UICONTROL Select]**und wählen **[!UICONTROL Edit]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Content]** und führen Sie folgende Schritte aus:

   - Wenn Sie [Page Builder aktiviert](../page-builder/setup.md), erweitern Sie die **[!UICONTROL Media]** Bedienfeld und Ziehen eines **[!UICONTROL Image]** Platzhalter zum Ziel-Container hinzu. Klicken Sie anschließend auf **[!UICONTROL Select from Gallery]**.

     ![Bild in die Bühne ziehen](./assets/pb-media-image-drag.png){width="600" zoomable="yes"}

   - Wenn Sie [WYSIWYG-Editor aktiviert](/help/content-design/editor.md)klicken **[!UICONTROL Show/Hide Editor]** und klicken Sie anschließend auf **[!UICONTROL Insert Image]**.

## [!DNL Media Gallery] Demo

Weitere Informationen zum [!DNL Media Gallery], sehen Sie sich dieses Video an:

>[!VIDEO](https://video.tv.adobe.com/v/343785?quality=12)

[adobe-stock]: https://stock.adobe.com

