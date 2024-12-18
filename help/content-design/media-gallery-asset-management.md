---
title: Asset-Management für Mediensammlung
description: Erfahren Sie, wie Sie hochgeladene Mediendateien und Assets verwalten, die Sie über eine Adobe Stock-Integration erhalten.
exl-id: 4fc489ae-b1e5-4aa4-832d-cd88c58d103a
feature: Page Content, Media
source-git-commit: a93e96353f4be0e771064cdcfbdf794772386a28
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 0%

---

# Asset-Management für Mediensammlung

Die neue [Mediensammlung](media-gallery.md) bietet Tools zum Verwalten hochgeladener Mediendateien und Assets, die Sie über eine [Adobe Stock-Integration](adobe-stock.md) erwerben. Wenn Sie eine Adobe Stock [Bildvorschau) gespeichert haben](adobe-stock-save-preview.md) können Sie das Bild auch [lizenzieren](adobe-stock-license-image.md) in der neuen Mediensammlung speichern.

## Hochladen eines Assets

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Klicken Sie auf **[!UICONTROL Upload Image]**.

1. Datei zum Hochladen auswählen.

   Das ausgewählte Asset wird automatisch in den ausgewählten Ordner hochgeladen (oder in den Speicherstamm, wenn kein Ordner ausgewählt ist).

## Asset-Details anzeigen

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Klicken Sie auf die drei Punkte unter dem Asset (![Detailsymbol](./assets/media-gallery-asset-menu-icon.png){width="10" zoomable="no"}) und dann auf **[!UICONTROL View Details]**.

   ![Asset-Aktionen](./assets/media-gallery-asset-actions.png){width="600" zoomable="yes"}

   Die Asset-Details werden auf einer Folie angezeigt. Sie enthalten die Informationen, wo das Asset verwendet wird:

   - **[!UICONTROL Categories]**
   - **[!UICONTROL Products]**
   - **[!UICONTROL Pages]**
   - **[!UICONTROL Blocks]**

   ![Asset-Details](./assets/media-gallery-asset-details.png){width="600" zoomable="yes"}

   Um die Details anzuzeigen, klicken Sie auf die **[!UICONTROL Used In]** Links . Das Raster im folgenden Beispiel zeigt alle Kategorien, in denen ein bestimmtes Asset verwendet wird.

   ![Kategorienraster](./assets/media-gallery-asset-categories.png){width="600" zoomable="yes"}

   Es ist auch möglich, das Asset aus dem Abschnitt _Details anzeigen_ zu löschen.

## Asset bearbeiten

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Klicken Sie auf die drei Punkte unter dem Asset (![Asset-Menüsymbol](./assets/media-gallery-asset-menu-icon.png){width="10" zoomable="no"}) und dann auf **[!UICONTROL Edit]**.

   ![Asset bearbeiten](./assets/media-gallery-edit-asset.png){width="600" zoomable="yes"}

1. Ändern Sie bei Bedarf einen der folgenden Metadatenwerte:

   - **[!UICONTROL Title]**
   - **[!UICONTROL Description]**
   - **[!UICONTROL Tags/Keywords]**

   Diese Daten werden in der Datenbank und in den Dateimetadaten selbst gespeichert. Derzeit werden XMP- und IPTC-Formate unterstützt.

   Sie können das Bild mit den aktualisierten Metadaten herunterladen.

## Verwenden von Assets

Assets kann im gesamten Admin-Bereich umfassend verwendet werden, z. B[ (Hinzufügen oder Bearbeiten einer Seite](page-add.md), [Erstellen oder Bearbeiten einer Kategorie](../catalog/category-create.md) oder [Einfügen von Bildern aus dem Inhaltseditor](editor-insert-image.md).

1. Greifen Sie in einem Bereich auf die neue Mediensammlung zu, in dem Sie Medien-Assets verwenden können.

1. Wählen Sie das Asset aus und klicken Sie auf **[!UICONTROL Add Selected]**.

{{$include /help/_includes/image-optimization-animated-gif-note.md}}

## Löschen von Assets

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Klicken Sie auf **[!UICONTROL Delete Images...]** und aktivieren Sie das Kontrollkästchen für jedes Asset, das Sie löschen möchten.

1. Klicken Sie im Bestätigungsdialogfeld auf **[!UICONTROL Delete Image]**.

   ![Löschbestätigung](./assets/media-gallery-bulk-delete-confirm.png){width="500" zoomable="yes"}

## Nach Assets suchen

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Verwenden Sie die **[!UICONTROL Search by keywords]**-Eingabe, um die Bildsuche nach Keywords/Tags durchzuführen.

   Die Suche im folgenden Beispiel findet Assets, die ein bestimmtes Tag (`mountain`) enthalten.

   ![Asset-Suche](./assets/media-gallery-asset-search.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Informationen zum Aktualisieren von Bild-Tags finden Sie im Abschnitt _[Bearbeiten eines Assets](#edit-an-asset)_.

## Filtern von Assets

>[!NOTE]
>
>Die Funktion _Verwendet in_ erfordert, dass [!UICONTROL Media Gallery Image Optimization] in den [Konfigurationseinstellungen“ aktiviert ](media-gallery-image-optimization.md).

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Klicken Sie auf die Registerkarte **[!UICONTROL Filters]** .

   ![Filter](./assets/media-gallery-filters.png){width="600" zoomable="yes"}

1. Legen Sie die Filteroptionen fest.

   Sie können die Assets nach Nutzung durch die Entitäten filtern:

   - **[!UICONTROL Used in Categories]**
   - **[!UICONTROL Used in Products]**
   - **[!UICONTROL Used in Pages]**
   - **[!UICONTROL Used in Blocks]**

   Sie können die Assets auch nach **[!UICONTROL Store View]**, **[!UICONTROL License Status]** und **[!UICONTROL Content Status]** filtern. Legen Sie einen Datumsbereich für **[!UICONTROL Uploaded Date]** und/oder **[!UICONTROL Modification Date]** fest, um Assets nach Dateidaten zu filtern.

1. Klicken Sie auf **[!UICONTROL Apply Filters]** , um die Ergebnisse anzuzeigen.

   Die Filterung im folgenden Beispiel findet Assets, die in einer bestimmten Kategorie (`cars`) verwendet werden und aktiviert sind.

   ![Filtern Sie nach aktivierter Assets nach Kategorie](./assets/media-gallery-filter-by-category.png){width="600" zoomable="yes"}

## Suchen nach Bildduplikaten

1. Klicken Sie auf die Registerkarte **[!UICONTROL Filters]** und aktivieren Sie das Kontrollkästchen **[!UICONTROL Show duplicates]** .

1. Um die Ergebnisse anzuzeigen, klicken Sie auf **[!UICONTROL Apply Filters]**.
