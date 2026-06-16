---
title: Administratorraster-Steuerelemente
description: Erfahren Sie, wie Sie in Admin-Seiten arbeiten, die Daten verwalten und eine Sammlung von Datensätzen in einem Raster anzeigen.
exl-id: a4a9531d-eb2f-41d6-bb36-dc6d8811ee95
TQID: https://experienceleague.adobe.com/-BGRS0qjthE3-oWu1DbrxeEUVk1aXdgW-RPRO1dYND0
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 519
ht-degree: 0%

---

# Administratorraster-Steuerelemente

Admin-Seiten, die Daten verwalten, zeigen eine Sammlung von Datensätzen in einem Raster an. Die Steuerelemente am oberen Rand jeder Spalte können zum Sortieren der Daten verwendet werden. Die aktuelle Sortierreihenfolge wird durch einen aufsteigenden oder absteigenden Pfeil in der Spaltenüberschrift angezeigt. Sie können angeben, welche Spalten im Raster angezeigt werden, und sie an verschiedene Positionen ziehen. Sie können auch verschiedene Spaltenanordnungen als Ansichten speichern, die später verwendet werden können. Die Spalte **[!UICONTROL Action]** listet Vorgänge auf, die auf einen einzelnen Datensatz angewendet werden können. Darüber hinaus können Datumsangaben aus der aktuellen Ansicht der meisten Raster in eine CSV- oder [-](../systems/data-csv.md) exportiert werden.

![Seite „Bestellungen“ - Rasteranzeige](./assets/admin-workspace-grid.png){width="700" zoomable="yes"}

## Sortieren der Liste

1. Klicken Sie auf eine beliebige Spaltenüberschrift.

   Der Pfeil zeigt die aktuelle Reihenfolge als aufsteigend oder absteigend an.

1. Verwenden Sie die Steuerelemente für die Paginierung, um zusätzliche Seiten in der Auflistung anzuzeigen.

   ![Rasteranzeige - Seitensteuerelemente](./assets/pagination-controls.png){width="300"}

## Paginieren der Liste

1. Legen Sie das **[!UICONTROL Pagination]**-Steuerelement auf die Anzahl der Datensätze fest, die pro Seite angezeigt werden sollen.

1. Klicken Sie auf **[!UICONTROL Next]** und **[!UICONTROL Previous]** Sie, um durch die Liste zu blättern, oder geben Sie einen bestimmten **[!UICONTROL Page Number]** ein.

## Filtern der Liste

1. Klicken Sie auf **[!UICONTROL Filters]**.

1. Füllen Sie so viele Filter wie nötig aus, um den zu suchenden Datensatz zu beschreiben.

1. Klicken Sie auf **[!UICONTROL Apply Filters]**.

   ![Auftragsliste - Filtersteuerelemente](./assets/admin-workspace-filters.png){width="700" zoomable="yes"}

## Daten exportieren

1. Wählen Sie die Datensätze aus, die Sie exportieren möchten.

   >[!NOTE]
   >
   >Produktdaten können nicht aus dem Raster exportiert werden. Weitere Informationen finden Sie unter [Exportieren](../systems/data-export.md).

1. Wählen Sie _Menü_ Export![ (](../assets/icon-export.png)) oben rechts eines der folgenden Dateiformate aus:

   - `CSV`
   - `Excel XML`

   ![Auftragsliste - Exportoptionen](./assets/customers-grid-export.png){width="700" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Export]**.

1. Suchen Sie die heruntergeladene Datei der exportierten Daten an dem Speicherort, der von Ihrem Browser für Downloads verwendet wird.

## Rasterlayout

Die Auswahl der Spalten und ihre Reihenfolge im Raster können nach Ihren Wünschen geändert und als _Ansicht“ gespeichert_. Sie können steuern, welche Attribute im Raster unter der Konfiguration der einzelnen Attribute angezeigt werden. Wenn im Produktraster viele Attribute angezeigt werden, kann sich dies auf die Ladezeit und Leistung des Admins auswirken.

![Sortieren von Rasterspalten](./assets/admin-grid-columns.png){width="700" zoomable="yes"}

### Spaltenauswahl ändern

1. Klicken Sie oben rechts auf das Steuerelement _Spalten_ (![Spalten-Steuerelement](../assets/icon-columns.png)).

1. Ändern Sie die Spaltenauswahl:

   - Aktivieren Sie das Kontrollkästchen einer beliebigen Spalte, die Sie dem Raster hinzufügen möchten.
   - Deaktivieren Sie das Kontrollkästchen für alle Spalten, die Sie aus dem Raster entfernen möchten.
   - Um zur Standardrasteransicht zurückzukehren, klicken Sie auf **[!UICONTROL Reset]**.

Scrollen Sie nach unten, um alle verfügbaren Spalten anzuzeigen.

### Spalte verschieben

1. Klicken Sie auf die Spaltenüberschrift und halten Sie die Maustaste gedrückt.

1. Ziehen Sie die Spalte an die neue Position und lassen Sie sie los.

### Speichern einer Rasteransicht

1. Klicken Sie auf das _View_-Steuerelement ![View-Steuerelement](../assets/icon-view-eye.png).

1. Klicken Sie auf **[!UICONTROL Save Current View]**.

1. Geben Sie einen **[!UICONTROL name]** für die Ansicht ein.

1. Um alle Änderungen zu speichern, klicken Sie auf _Pfeil_ (![Alle Änderungen speichern](../assets/icon-arrow-save.png)).

   Der Name der Ansicht wird jetzt als aktuelle Ansicht angezeigt.

### Ändern der Rasteransicht

1. Klicken Sie auf _Steuerelement_ Ansicht![ (](../assets/icon-view-eye.png)).

1. Führen Sie einen der folgenden Schritte aus:

   - Um eine andere Ansicht zu verwenden, klicken Sie auf den Namen der Ansicht.
   - Um den Namen einer Ansicht zu ändern, klicken Sie auf das Symbol _Bearbeiten_ (![Bearbeiten-Symbol](../assets/icon-edit-pencil.png)) und aktualisieren Sie den Namen.
   - Um eine Ansicht zu löschen, klicken Sie auf das Symbol _Bearbeiten_ (![Bearbeiten](../assets/icon-edit-pencil.png)) und dann auf das Symbol _Löschen_ (![Löschen](../assets/icon-delete-trashcan-solid.png)).
