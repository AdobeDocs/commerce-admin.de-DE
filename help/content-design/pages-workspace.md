---
title: Seitenarbeitssteuerelemente
description: Erfahren Sie mehr über die Workspace-Tools, die zum Suchen und Aktualisieren von Inhaltsseiten verwendet werden.
exl-id: c53e3e70-9f88-46ec-b44d-133a2ff5d0d5
feature: Page Content, Admin Workspace
source-git-commit: 3d04e7213d90bb4c323acce69ac31c1dbcb7ca49
workflow-type: tm+mt
source-wordcount: '1280'
ht-degree: 0%

---

# Seitenarbeitssteuerelemente

Der Seitenarbeitsbereich enthält Tools, die Ihnen dabei helfen, die benötigten Seiten schnell zu finden, sowie Befehle zur routinemäßigen Wartung auf einzelnen oder mehreren Seiten. Sie können die Seiteneigenschaften auch schnell über das Raster aktualisieren.

![Seitenraster](./assets/pages-grid.png){width="700" zoomable="yes"}

## Schnelles Aktualisieren der Seiteneigenschaften

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.
1. Klicken Sie auf eine beliebige Zeile im Raster.

   ![Seiteneigenschaften können im Raster Seiten bearbeitet werden](./assets/page-grid-properties-update.png){width="600" zoomable="yes"}

   Um mehrere Datensätze auszuwählen, aktivieren Sie das Kontrollkästchen jeder Zeile, die Sie aktualisieren möchten.

1. Aktualisieren Sie eine der folgenden Eigenschaften:

   - **[!UICONTROL Title]**
   - **[!UICONTROL URL Key]**
   - **[!UICONTROL Status]**
   - **[!UICONTROL Layout]**

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]**.

## Workspace-Steuerelemente

| Kontrolle | Beschreibung |
|--- |--- |
| [!UICONTROL Add New Page] | Fügt eine Seite hinzu. |
| [!UICONTROL Search] | Startet eine Katalogsuche basierend auf den aktuellen Filtern. |
| [!UICONTROL Actions] | Listet alle Aktionen auf, die auf ausgewählte Elemente in der Liste angewendet werden können. Um eine Aktion auf eine Seite oder mehrere Seiten anzuwenden, aktivieren Sie das Kontrollkästchen in der ersten Spalte jedes Datensatzes, für den die Aktion gilt. Optionen: `Delete` / `Disable` / `Enable` / `Edit` |
| [!UICONTROL Select] | Das Steuerelement in der Kopfzeile der ersten Spalte kann verwendet werden, um mehrere Datensätze als Zielgruppe der Aktion auszuwählen. Aktivieren Sie das Kontrollkästchen in der ersten Spalte jedes Datensatzes, den Sie auswählen möchten. Optionen: `Select All` / `Deselect All` |
| [!UICONTROL Save Edits] | Wendet die aktuelle Aktion auf ausgewählte Datensätze an. |
| [!UICONTROL Edit] | Öffnet den Datensatz im Bearbeitungsmodus. Sie können dasselbe erreichen, indem Sie auf eine beliebige Stelle in der Zeile klicken. |

{style="table-layout:auto"}

## Spalten

| Spalte | Beschreibung |
|--- |--- |
| [!UICONTROL Select] | Das Kontrollkästchen in der ersten Spalte wird zur Auswahl mehrerer Datensätze verwendet. Optionen: `Select All` / `Deselect All` |
| [!UICONTROL ID] | Die ID ist eine inkrementelle Zahl, die jeder Seite zugewiesen wird. |
| [!UICONTROL Title] | Der Titel, der oben auf der Seite angezeigt wird. |
| [!UICONTROL URL Key] | Der URL-Schlüssel ähnelt einem Dateinamen und identifiziert die Seite in der URL. |
| [!UICONTROL Layout] | Bestimmt, ob die Seite mit Seitenleisten rechts oder links neben dem Hauptinhaltsbereich angezeigt wird. Optionen: `1 column` / `2 columns with left bar` / `2 columns with right bar` / `3 columns` / `Empty` |
| [!UICONTROL Store View] | Wird verwendet, um die Seite einer bestimmten Store-Ansicht zuzuordnen. |
| [!UICONTROL Status] | Gibt an, ob die Seite online oder offline ist. Optionen: `Enabled` / `Disabled` |
| [!UICONTROL Created] | Das Datum der Erstellung der Seite. |
| [!UICONTROL Modified] | Das Datum der letzten Änderung der Seite. |
| [!UICONTROL Action] | Folgende Aktionen können auf einzelne Datensätze angewendet werden:<br/>**[!UICONTROL Edit]**- Öffnet die Seite im Bearbeitungsmodus.<br/>**[!UICONTROL Delete]** - Löscht die Seite.<br/>**[!UICONTROL View]**- Zeigt die Seite im Vorschaumodus an. |

{style="table-layout:auto"}

## Sonstige Spalten

| Spalte | Beschreibung |
|--- |--- |
| [!UICONTROL Custom design from/to] | Gibt das Start- und Enddatum an, an dem das ausgewählte Design auf die Seite angewendet wird. ![Magento Open Source](../assets/open-source.svg) (nur Magento Open Source). |
| [!UICONTROL Custom Theme] | Wendet ein benutzerdefiniertes Design auf die Seite an |
| [!UICONTROL Custom Layout] | Legt das benutzerdefinierte Layout der Seite fest |
| [!UICONTROL Meta Title] | Metadatentitel für die Seite |
| [!UICONTROL Meta Keywords] | Die Meta-Suchbegriffe für die Seite |
| [!UICONTROL Meta Description] | Die Meta-Beschreibung für die Seite |

{style="table-layout:auto"}

## Seitensuche

Das Suchfeld oben links im _[!UICONTROL Pages]_raster kann verwendet werden, um bestimmte Seiten nach Keywords zu finden. Für eine erweiterte Suche können Sie [filter](../getting-started/admin-grid-controls.md) die Suche nach mehreren Parametern.

### Suche nach Keyword

1. Geben Sie einen Suchbegriff in das Seitensuchfeld ein.

1. Um die Ergebnisse anzuzeigen, klicken Sie auf die Suche (![Lupensymbol](../assets/icon-magnify-search.png)).

   Die Ergebnisse umfassen alle Seiten, die den Suchbegriff enthalten.

### Suchergebnisse filtern

1. Klicken Sie bei Bedarf auf **[!UICONTROL Clear All]** , um die vorherigen Suchkriterien zu löschen.

1. Um die Auswahl der Suchfilter anzuzeigen, klicken Sie auf die **[!UICONTROL Filters]** !([Trichtersymbol](../assets/icon-filter-search.png)).

1. Füllen Sie so viele Filter wie nötig aus, um die Seiten zu beschreiben, die Sie finden möchten.

1. Klicks **[!UICONTROL Apply Filters]** , um die Ergebnisse anzuzeigen.

### Suchfilter

| Filter | Beschreibung |
|--- |--- |
| [!UICONTROL ID] | Filtern Sie die Suche nach der Datensatz-ID der Seite. |
| [!UICONTROL Title] | Filtern Sie die Suche nach dem Seitentitel. |
| [!UICONTROL URL Key] | Filtern Sie die Suche nach dem URL-Schlüssel. |
| [!UICONTROL Created] | Filtern Sie die Suche nach dem Datum, an dem die Seite erstellt wurde. |
| [!UICONTROL Modified] | Filtern Sie die Suche nach dem Datum, an dem die Seite zuletzt geändert wurde. |
| [!UICONTROL Store View] | Filtern Sie die Suche nach der Store-Ansicht. Optionen: `All available` / `Store Views` |
| [!UICONTROL Layout] | Filtern Sie die Suche nach dem Seitenlayout. Optionen: `1 column` / `2 columns with left bar` / `2 columns with right bar` / `3 columns` / `Empty` |
| [!UICONTROL Status] | Filtern Sie die Suche nach dem Seitenstatus. Optionen: `Disabled` / `Published` |
| [!UICONTROL Custom design from / to] | Filtern Sie die Suche nach dem Start- und Enddatum, wenn das ausgewählte Design auf die Seite angewendet wird. ![Magento Open Source](../assets/open-source.svg) (nur Magento Open Source). |
| [!UICONTROL Asset] | Filtern der Suche nach den Asset-Titeln der Seite |
| [!UICONTROL Custom Layout] | Filtern Sie die Suche nach einem benutzerdefinierten Layout. Optionen: `1 column` / `2 columns with left bar` / `2 columns with right bar` / `3 columns` / `Empty` / `Page -- Full Width` / `Category -- Full Width` / `Product -- Full Width` |
| [!UICONTROL Custom Theme] | Filtern Sie die Suche nach einem benutzerdefinierten Design. Standardoptionen: `Magento Blank` / `Magento Luma` |
| [!UICONTROL Meta Keywords] | Filtern Sie die Suche nach den Meta-Keywords für die Seite. |
| [!UICONTROL Meta Title] | Filtern Sie die Suche anhand des Metadatentitels für die Seite. |
| [!UICONTROL Meta Description] | Filtern Sie die Suche anhand der Metadatenbeschreibung für die Seite. |

{style="table-layout:auto"}

### Suchwerkzeuge

| Tool | Beschreibung |
|--- |--- |
| [!UICONTROL Apply Filters] | Wendet alle Filter auf die Suchergebnisse an. |
| [!UICONTROL Cancel] | Bricht die aktuelle Suche ab. |
| [!UICONTROL Clear All] | Löscht alle Suchfilter. |

{style="table-layout:auto"}

## Seitenaktionen

Seiten können bearbeitet, deaktiviert, aktiviert und gelöscht werden. Um eine Aktion auf eine einzelne Seite anzuwenden, aktivieren Sie das Kontrollkästchen in der ersten Spalte. Um alle Seiten auszuwählen oder die Auswahl aufzuheben, verwenden Sie das Auswahlsteuerelement oben in der Spalte.

![Seitenaktionen](./assets/pages-select.png){width="400" zoomable="yes"}

### Einzelaktion

Verwenden Sie die _[!UICONTROL Action]_-Spalte ganz rechts, um eine der folgenden Aktionen auf die einzelne Seite anzuwenden:

- [!UICONTROL Edit] - öffnet die Seite im Bearbeitungsmodus
- [!UICONTROL Delete] - löscht die Seite (Bestätigung erforderlich)
- [!UICONTROL View] - öffnet eine Seite direkt auf der Storefront

![Einzelseitenaktionen](./assets/page-grid-actions.png){width="600" zoomable="yes"}

### Massenaktionen

Wenden Sie eine der folgenden Aktionen mit der _[!UICONTROL Action]_Auswahl oben links:

- [!UICONTROL Delete] - löscht die Seiten (Bestätigung erforderlich)
- [!UICONTROL Disable] - deaktiviert die Seiten auf der Storefront
- [!UICONTROL Enable] - aktiviert die Seiten auf der Storefront
- [!UICONTROL Edit] - öffnet Spalten im Raster im Bearbeitungsmodus (**[!UICONTROL Title]**, **[!UICONTROL URL Key]**, **[!UICONTROL Layout]**, und **[!UICONTROL Status]**)

## Seiten-Raster-Layout

Die Auswahl der Spalten und ihre Reihenfolge im Raster können nach Ihren Wünschen geändert werden. Um die neue Spaltenanordnung beizubehalten, können Sie sie als Ansicht speichern.

### Spaltenauswahl ändern

Klicken Sie oben rechts auf die _Spalten_ (![Spaltensymbol](../assets/icon-columns.png)) steuern und gehen Sie wie folgt vor:

- Aktivieren Sie das Kontrollkästchen einer Spalte, die Sie zum Raster hinzufügen möchten.

- Deaktivieren Sie das Kontrollkästchen aller Spalten, die Sie aus dem Raster entfernen möchten.

### Verschieben einer Spalte

1. Klicken Sie auf die Spaltenüberschrift und halten Sie die Maustaste gedrückt.

1. Ziehen Sie die Spalte an die neue Position und veröffentlichen Sie sie.

### Ansicht speichern

1. Klicken Sie auf _Ansicht_ (![Augensymbol](../assets/icon-view-eye.png)) steuern und klicken Sie dann auf **[!UICONTROL Save View As]**.

1. Geben Sie einen Namen für die Ansicht ein.

1. Um die Ansicht zu speichern, klicken Sie auf die _Pfeil_ (![Pfeilsymbol](../assets/icon-arrow-save.png)).

   Der Name der Ansicht wird jetzt als aktuelle Ansicht angezeigt.

### Ansicht ändern

Klicken Sie auf _Ansicht_ (![Augensymbol](../assets/icon-view-eye.png)) steuern und einen der folgenden Schritte ausführen:

- Wählen Sie die Ansicht aus, die Sie verwenden möchten.

- Ändern Sie den Namen einer Ansicht, indem Sie auf Bearbeiten (![Stiftsymbol](../assets/icon-edit-pencil.png)) und den Namen aktualisieren.

  ![Die gespeicherte Ansicht wird in den Ansichtssteuerelementen mit einem Bearbeitungssymbol angezeigt](./assets/pages-default-grid-control.png){width="600" zoomable="yes"}

## Geplante Änderungen

{{ee-feature}}

Seitenänderungen können planmäßig angewendet und mit anderen Inhaltsänderungen gruppiert werden. Sie können eine Kampagne basierend auf geplanten Änderungen auf einer Seite erstellen oder die Änderungen auf eine bestehende Kampagne anwenden. Weitere Informationen finden Sie unter [Inhaltstaging](content-staging.md).

>[!NOTE]
>
>Die [!UICONTROL Custom Design Update] Registerkarte wurde entfernt in ![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce und können nicht direkt auf der Seite geändert werden. Sie müssen eine geplante Aktualisierung für diese Aktivierungen erstellen.

>[!NOTE]
>
>Alle geplanten Aktualisierungen werden nacheinander angewendet, d. h. jede Entität kann an einem Punkt nur eine geplante Aktualisierung erhalten. Jede geplante Aktualisierung wird auf alle Store-Ansichten innerhalb des Zeitrahmens angewendet. Daher kann eine Entität nicht gleichzeitig eine andere geplante Aktualisierung für verschiedene Store-Ansichten haben. Alle Entitätsattributwerte in allen Store-Ansichten, die von der aktuellen geplanten Aktualisierung nicht betroffen sind, werden von den Standardwerten übernommen und nicht von der vorherigen geplanten Aktualisierung.

![Auf der Startseite werden die geplanten Änderungen oben angezeigt.](./assets/page-scheduled-change.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Das Start- und Enddatum der Kampagne muss mithilfe der Variablen **_default_** Admin-Zeitzone, die aus der lokalen Zeitzone jeder Website konvertiert wird. Betrachten wir ein Beispiel, bei dem Sie mehrere Websites in verschiedenen Zeitzonen haben, aber eine Kampagne basierend auf einer US-Zeitzone starten möchten. In diesem Fall müssen Sie für jede lokale Zeitzone eine separate Aktualisierung planen und **[!UICONTROL Start Date]** und **[!UICONTROL End Date]** aus jeder lokalen Website-Zeitzone in die standardmäßige Admin-Zeitzone konvertiert.

Außerdem können Sie Änderungen für Produktaktualisierungen planen und in der Vorschau anzeigen. Weitere Informationen finden Sie unter [Planung einer Aktualisierung](content-staging-scheduled-update.md).
