---
title: Asset-Verwaltung für Media Gallery
description: Erfahren Sie, wie Sie hochgeladene Mediendateien und Assets verwalten, die Sie über eine Adobe Stock-Integration erwerben.
exl-id: 4fc489ae-b1e5-4aa4-832d-cd88c58d103a
feature: Page Content, Media
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 0%

---

# Asset-Verwaltung für Media Gallery

Die neue [Media Gallery](media-gallery.md) bietet Tools zum Verwalten von hochgeladenen Mediendateien und Assets, die Sie über ein [Adobe Stock-Integration](adobe-stock.md). Wenn Sie eine Adobe Stock gespeichert haben [Bildvorschau](adobe-stock-save-preview.md)können Sie auch [Lizenz](adobe-stock-license-image.md) das Bild in der neuen Media Gallery.

## Hochladen eines Assets

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Klicken **[!UICONTROL Upload Image]**.

1. Wählen Sie die hochzuladende Datei aus.

   Das ausgewählte Asset wird automatisch in den ausgewählten Ordner hochgeladen (oder in den Speicherstamm, wenn kein Ordner ausgewählt ist).

## Asset-Details anzeigen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Klicken Sie auf die drei Punkte unter dem Asset (![Symbol Details](./assets/media-gallery-asset-menu-icon.png){width="10" zoomable="no"}), klicken Sie auf **[!UICONTROL View Details]**.

   ![Asset-Aktionen](./assets/media-gallery-asset-actions.png){width="600" zoomable="yes"}

   Die Asset-Details werden in einem Diabereich angezeigt. Sie enthalten die Informationen, in denen das Asset verwendet wird:

   - **[!UICONTROL Categories]**
   - **[!UICONTROL Products]**
   - **[!UICONTROL Pages]**
   - **[!UICONTROL Blocks]**

   ![Asset-Details](./assets/media-gallery-asset-details.png){width="600" zoomable="yes"}

   Um die Details anzuzeigen, klicken Sie auf das **[!UICONTROL Used In]** Links . Das Raster im folgenden Beispiel zeigt alle Kategorien an, in denen ein bestimmtes Asset verwendet wird.

   ![Kategorienraster](./assets/media-gallery-asset-categories.png){width="600" zoomable="yes"}

   Es ist auch möglich, das Asset aus dem _Details anzeigen_ Abschnitt.

## Bearbeiten von Assets

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Klicken Sie auf die drei Punkte unter dem Asset (![Asset-Menüsymbol](./assets/media-gallery-asset-menu-icon.png){width="10" zoomable="no"}), klicken Sie auf **[!UICONTROL Edit]**.

   ![Asset bearbeiten](./assets/media-gallery-edit-asset.png){width="600" zoomable="yes"}

1. Ändern Sie bei Bedarf einen der folgenden Metadatenwerte:

   - **[!UICONTROL Title]**
   - **[!UICONTROL Description]**
   - **[!UICONTROL Tags/Keywords]**

   Diese Daten werden in der Datenbank und in den Dateimetadaten selbst gespeichert. Derzeit werden XMP- und IPTC-Formate unterstützt.

   Sie können das Bild mit den aktualisierten Metadaten herunterladen.

## Verwenden eines Assets

Assets können im gesamten Admin umfassend verwendet werden, z. B. [Hinzufügen oder Bearbeiten einer Seite](page-add.md), [Erstellen oder Bearbeiten von Kategorien](../catalog/category-create.md)oder [Bilder aus dem Inhaltseditor einfügen](editor-insert-image.md).

1. Greifen Sie über einen Bereich, in dem Sie Medien-Assets verwenden können, auf die neue Media Gallery zu.

1. Wählen Sie das Asset aus und klicken Sie auf **[!UICONTROL Add Selected]**.

## Löschen von Assets

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Klicks **[!UICONTROL Delete Images...]** und aktivieren Sie das Kontrollkästchen für jedes Asset, das Sie löschen möchten.

1. Klicken Sie im Bestätigungsdialogfeld auf **[!UICONTROL Delete Image]**.

   ![Löschbestätigung](./assets/media-gallery-bulk-delete-confirm.png){width="500" zoomable="yes"}

## Suchen nach Assets

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Verwenden Sie die **[!UICONTROL Search by keywords]** -Eingabe, um die Bildsuche nach Keywords/Tags durchzuführen.

   Die Suche im folgenden Beispiel findet Assets, die ein bestimmtes Tag (`mountain`).

   ![Asset-Suche](./assets/media-gallery-asset-search.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Informationen dazu, wie Sie Bild-Tags aktualisieren können, finden Sie unter _[Bearbeiten von Assets](#edit-an-asset)_ Abschnitt.

## Filtern von Assets

>[!NOTE]
>
>Die _Verwendet in_ -Funktion muss [!UICONTROL Media Gallery Image Optimization] ist in der Variablen [Konfigurationseinstellungen](media-gallery-image-optimization.md).

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Klicken Sie auf **[!UICONTROL Filters]** Registerkarte.

   ![Filter](./assets/media-gallery-filters.png){width="600" zoomable="yes"}

1. Festlegen der Filteroptionen.

   Sie können die Assets nach Verwendung durch die Entitäten filtern:

   - **[!UICONTROL Used in Categories]**
   - **[!UICONTROL Used in Products]**
   - **[!UICONTROL Used in Pages]**
   - **[!UICONTROL Used in Blocks]**

   Sie können die Assets auch nach **[!UICONTROL Store View]**, **[!UICONTROL License Status]**, und **[!UICONTROL Content Status]**. Festlegen eines Datumsbereichs für **[!UICONTROL Uploaded Date]** und/oder **[!UICONTROL Modification Date]** , um Assets nach Dateidaten zu filtern.

1. Klicks **[!UICONTROL Apply Filters]** um die Ergebnisse anzuzeigen.

   Die Filterung im folgenden Beispiel findet Assets, die in einer bestimmten Kategorie (`cars`) und aktiviert sind.

   ![Filtern nach aktivierten Assets nach Kategorie](./assets/media-gallery-filter-by-category.png){width="600" zoomable="yes"}

## Suchen von Bildduplikaten

1. Klicken Sie auf **[!UICONTROL Filters]** und wählen Sie die **[!UICONTROL Show duplicates]** aktivieren.

1. Um die Ergebnisse anzuzeigen, klicken Sie auf **[!UICONTROL Apply Filters]**.
