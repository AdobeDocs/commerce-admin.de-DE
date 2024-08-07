---
title: Admin-Rastersteuerelemente
description: Erfahren Sie, wie Sie auf Admin-Seiten arbeiten, auf denen Daten verwaltet werden, und eine Sammlung von Datensätzen in einem Raster anzeigen.
exl-id: a4a9531d-eb2f-41d6-bb36-dc6d8811ee95
source-git-commit: a3fb702d0b6e08c3aaaa0d6b5e07aa825026ef76
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 0%

---

# Admin-Rastersteuerelemente

Admin-Seiten, die Daten verwalten, zeigen eine Sammlung von Datensätzen in einem Raster an. Die Steuerelemente am oberen Rand jeder Spalte können zum Sortieren der Daten verwendet werden. Die aktuelle Sortierreihenfolge wird durch einen auf- oder absteigenden Pfeil in der Spaltenüberschrift angezeigt. Sie können festlegen, welche Spalten im Raster angezeigt werden, und sie an verschiedene Positionen ziehen. Sie können auch verschiedene Spaltenanordnungen als Ansichten speichern, die später verwendet werden können. In der Spalte **[!UICONTROL Action]** werden Vorgänge aufgelistet, die auf einen einzelnen Datensatz angewendet werden können. Darüber hinaus kann das Datum aus der aktuellen Ansicht der meisten Raster in eine [CSV](../systems/data-csv.md)- oder XML-Datei exportiert werden.

![Bestellungsseite - Rasteranzeige](./assets/admin-workspace-grid.png){width="700" zoomable="yes"}

## Liste sortieren

1. Klicken Sie auf eine beliebige Spaltenüberschrift.

   Der Pfeil zeigt die aktuelle Reihenfolge entweder auf- oder absteigend an.

1. Verwenden Sie die Paginierungssteuerelemente, um zusätzliche Seiten in der Sammlung anzuzeigen.

   ![Rasteranzeige - Seitensteuerelemente](./assets/pagination-controls.png){width="300"}

## Liste paginieren

1. Stellen Sie das Steuerelement **[!UICONTROL Pagination]** auf die Anzahl der Datensätze ein, die pro Seite angezeigt werden sollen.

1. Klicken Sie auf **[!UICONTROL Next]** und **[!UICONTROL Previous]** , um durch die Liste zu blättern, oder geben Sie einen bestimmten **[!UICONTROL Page Number]** ein.

## Liste filtern

1. Klicken Sie auf **[!UICONTROL Filters]**.

1. Füllen Sie so viele Filter wie nötig aus, um den gewünschten Datensatz zu beschreiben.

1. Klicken Sie auf **[!UICONTROL Apply Filters]**.

   ![Liste der Bestellungen - Filtersteuerelemente](./assets/admin-workspace-filters.png){width="700" zoomable="yes"}

## Daten exportieren

1. Wählen Sie die Datensätze aus, die exportiert werden sollen.

   >[!NOTE]
   >
   >Produktdaten können nicht aus dem Raster exportiert werden. Weitere Informationen finden Sie unter [Exportieren](../systems/data-export.md).

1. Wählen Sie im Menü _Export_ (![Menüauswahl](../assets/icon-export.png)) oben rechts eines der folgenden Dateiformate aus:

   - `CSV`
   - `Excel XML`

   ![Bestellliste - Exportoptionen](./assets/customers-grid-export.png){width="700" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Export]**.

1. Suchen Sie nach der heruntergeladenen Datei der exportierten Daten an dem Speicherort, der für Downloads durch Ihren Browser verwendet wird.

## Rasterlayout

Die Auswahl der Spalten und ihre Reihenfolge im Raster können nach Ihren Vorstellungen geändert und als _Ansicht_ gespeichert werden. Sie können steuern, welche Attribute im Raster unter der jeweiligen Attributkonfiguration angezeigt werden. Die Anzeige vieler Attribute im Produktraster kann sich auf die Ladezeit und Leistung der Administratoren auswirken.

![Sortieren von Rasterspalten](./assets/admin-grid-columns.png){width="700" zoomable="yes"}

### Spaltenauswahl ändern

1. Klicken Sie in der oberen rechten Ecke auf das Steuerelement _Spalten_ (![Spalten-Steuerelement](../assets/icon-columns.png)).

1. Ändern Sie die Spaltenauswahl:

   - Aktivieren Sie das Kontrollkästchen einer Spalte, die Sie zum Raster hinzufügen möchten.
   - Deaktivieren Sie das Kontrollkästchen aller Spalten, die Sie aus dem Raster entfernen möchten.
   - Um die standardmäßige Rasteransicht zurückzugeben, klicken Sie auf **[!UICONTROL Reset]**.

Scrollen Sie nach unten, um alle verfügbaren Spalten anzuzeigen.

### Verschieben einer Spalte

1. Klicken Sie auf die Spaltenüberschrift und halten Sie die Maustaste gedrückt.

1. Ziehen Sie die Spalte an die neue Position und veröffentlichen Sie sie.

### Speichern einer Rasteransicht

1. Klicken Sie auf das Steuerelement _Ansicht_ (![Steuerelement anzeigen](../assets/icon-view-eye.png)).

1. Klicken Sie auf **[!UICONTROL Save Current View]**.

1. Geben Sie eine **[!UICONTROL name]** für die Ansicht ein.

1. Um alle Änderungen zu speichern, klicken Sie auf den _Pfeil_ (![Alle Änderungen speichern](../assets/icon-arrow-save.png)).

   Der Name der Ansicht wird jetzt als aktuelle Ansicht angezeigt.

### Ändern der Rasteransicht

1. Klicken Sie auf das Steuerelement _Ansicht_ (![Ansichtssymbol](../assets/icon-view-eye.png)).

1. Führen Sie einen der folgenden Schritte aus:

   - Um eine andere Ansicht zu verwenden, klicken Sie auf den Namen der Ansicht.
   - Um den Namen einer Ansicht zu ändern, klicken Sie auf das Symbol _Bearbeiten_ (![Symbol Bearbeiten](../assets/icon-edit-pencil.png)) und aktualisieren Sie den Namen.
   - Um eine Ansicht zu löschen, klicken Sie auf das Symbol _Bearbeiten_ (![Symbol Bearbeiten](../assets/icon-edit-pencil.png)) und dann auf das Symbol _Löschen_ (![Symbol Löschen](../assets/icon-delete-trashcan-solid.png)).
