---
title: Hinzufügen und Entfernen von Seiten
description: Erfahren Sie, wie Sie in Ihrem [!DNL Commerce] Speicher verwendete Inhaltsseiten hinzufügen und entfernen.
exl-id: a7a503ea-3631-4be2-81e4-aed2ae9419dc
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '1105'
ht-degree: 0%

---

# Hinzufügen und Entfernen von Seiten

Der Prozess zum Hinzufügen einer Inhaltsseite zu Ihrem Store ist im Wesentlichen derselbe für jeden Seitentyp, den Sie erstellen möchten. Sie können Text, Bilder, Inhaltsblöcke, Variablen und Widgets einschließen. Die meisten Inhaltsseiten sind für das Lesen von Suchmaschinen zuerst und von Personen danach konzipiert. Berücksichtigen Sie bei der Auswahl des Seitentitels und der URL sowie beim Zusammenstellen der Metadaten und Inhalte die Bedürfnisse jeder dieser beiden Zielgruppen. Wenn Ihre Seite abgeschlossen ist, kann sie zu Ihrer Store-Navigation hinzugefügt, mit anderen Seiten verknüpft, über die Fußzeile Ihres Stores verknüpft oder als neue [Homepage](page-home-new.md) verwendet werden.

![Seitenraster](./assets/pages-grid.png){width="700" zoomable="yes"}

## Hinzufügen einer Seite

Die folgenden Anweisungen führen Sie durch jeden Schritt, um eine einfache Seite zu erstellen. Einige erweiterte Funktionen werden übersprungen, aber in anderen Themen behandelt.

### Schritt 1: Erstellen der Seite

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Klicken Sie auf **[!UICONTROL Add New Page]**.

   ![Neue Seite](./assets/pages-new-page.png){width="600" zoomable="yes"}

1. Wenn Sie die Seite nicht sofort veröffentlichen möchten, setzen Sie **[!UICONTROL Enable Page]** auf `No`.

1. Geben Sie den Wert **[!UICONTROL Page Title]** ein.

   Der Seitentitel wird in der Navigation [Breadcrumb](../catalog/navigation-breadcrumb-trail.md) angezeigt.

### Schritt 2: Inhalt abschließen

Fügen Sie je nach der Konfiguration der [erweiterten Content Tools](../configuration-reference/general/content-management.md) den Seiteninhalt hinzu.

#### Verwenden der Inhaltstools für den Seitenaufbau

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) **[!UICONTROL Content]**.

   ![Inhalt mit Seitenaufbau](../page-builder/assets/pb-page-content.png){width="600" zoomable="yes"}

1. Geben Sie in das Feld **[!UICONTROL Content Heading]** die Überschrift ein, die oben auf der Seite angezeigt werden soll.

   Wenn diese Option aktiviert ist, werden die Bühne und das Bedienfeld [Seitenaufbau](../page-builder/introduction.md) unter der Inhaltsüberschrift angezeigt. Weitere Informationen finden Sie unter [Workspace](../page-builder/workspace.md). Wenn _Seitenaufbau_ nicht aktiviert ist, wird der Editor im WYSIWYG-Modus mit der Symbolleiste oben geöffnet.

1. Füllen Sie den Inhalt aus und formatieren Sie den Text nach Bedarf.

#### Verwenden der Editor-Symbolleiste

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) **[!UICONTROL Content]**.

   ![Inhalt](./assets/page-content-editor.png){width="600" zoomable="yes"}

1. Geben Sie in das Feld **[!UICONTROL Content Heading]** die Überschrift ein, die oben auf der Seite angezeigt werden soll.

1. Füllen Sie den Inhalt aus und formatieren Sie den Text nach Bedarf.

   Sie können nach Bedarf [Bilder](media-storage.md), [Variablen](../systems/variables-predefined.md) und [Widgets](widgets.md) hinzufügen. Weitere Informationen finden Sie unter [Verwenden des Editors](editor.md).

### Schritt 3: SEO-Informationen ausfüllen

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) **[!UICONTROL Search Engine Optimization]**.

   ![Suchmaschinenoptimierung](./assets/page-search-engine-optimization.png){width="600" zoomable="yes"}

1. Akzeptieren Sie entweder die Standardeinstellung oder geben Sie einen anderen **[!UICONTROL URL Key]** ein, der aus allen Kleinbuchstaben mit Bindestrichen anstelle von Leerzeichen besteht.

   Der Standard-URL-Schlüssel wurde beim Speichern der Seite erstellt und basiert auf der Inhaltsüberschrift.

1. Geben Sie eine **[!UICONTROL Meta Title]** für die Seite ein.

   Der Metadatentitel sollte weniger als 70 Zeichen enthalten und wird in der Titelleiste und Registerkarte des Browsers angezeigt.

1. Geben Sie den hohen Wert **[!UICONTROL Meta Keywords]** ein, den Suchmaschinen für die Indizierung der Seite verwenden können.

   Trennen Sie mehrere Wörter durch ein Komma. Meta-Suchbegriffe werden von einigen Suchmaschinen ignoriert, aber von anderen verwendet.

1. Geben Sie für &quot;**[!UICONTROL Meta Description]**&quot;eine kurze Beschreibung der Seite für die Liste der Suchergebnisse ein.

   Idealerweise sollte die Beschreibung 150 bis 160 Zeichen lang sein, mit einer maximalen Länge von 255 Zeichen.

1. Klicken Sie auf **[!UICONTROL Save]**.

### Schritt 4: Festlegen des Umfangs der Seite

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) **[!UICONTROL Page in Websites]**.

   ![Seiten in Websites](./assets/page-in-websites.png){width="600" zoomable="yes"}

1. Wählen Sie in der Liste **[!UICONTROL Store View]** jede Ansicht aus, in der die Seite verfügbar sein soll.

   Wenn die Installation über mehrere Websites verfügt, wählen Sie jede Website und Store-Ansicht aus, in der die Seite verfügbar sein soll.

### Schritt 5: Übergeordnete Seite identifizieren (falls zutreffend)

{{ee-feature}}

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) **[!UICONTROL Hierarchy]**.

   ![Hierarchy](./assets/page-hierarchy.png){width="600" zoomable="yes"}

1. Wenn diese Seite ein untergeordnetes Element einer anderen Seite ist, aktivieren Sie das Kontrollkästchen von **[!UICONTROL Parent page]**.

### Schritt 6: Designänderungen eingeben (optional)

1. Um das Layout der Seite zu ändern, erweitern Sie den ![Erweiterungsselektor](../assets/icon-display-expand.png) **[!UICONTROL Design]**.

   ![Design](./assets/page-design.png){width="600" zoomable="yes"}

1. Um das Spaltenlayout der Seite zu ändern, setzen Sie **[!UICONTROL Layout]** auf einen der folgenden Werte:

   - `Empty`
   - `1 column`
   - `2 columns with left bar`
   - `2 columns with right bar`
   - `3 columns`
   - `Page -- Full Width` (Erfordert [Seitenaufbau](../page-builder/introduction.md))
   - `Category -- Full Width` (Erfordert den Seitenaufbau)
   - `Product -- Full Width` (Erfordert den Seitenaufbau)

1. Um einen **[!UICONTROL Custom Layout Update]** -Wert anzuwenden, wählen Sie den Namen der Datei aus der Liste aus.

   Weitere Informationen finden Sie unter [Layout-Aktualisierungen](layout-updates.md).

1. Um das Design der Seite zu ändern, setzen Sie **[!UICONTROL New Theme]** auf einen der folgenden Werte:

   - `Magento Black`
   - `Magento Luma`

1. ![Magento Open Source](../assets/open-source.svg) (nur Magento Open Source) Um eine Designänderung zu planen, erweitern Sie den ![Erweiterungsselektor](../assets/icon-display-expand.png) **[!UICONTROL Custom Design Update]** und führen Sie folgende Schritte aus:

   ![Benutzerdefiniertes Design-Update](./assets/page-custom-design-update.png){width="600" zoomable="yes"}

   - Verwenden Sie den Kalender (![Kalendersymbol](../assets/icon-calendar.png)), um das **[!UICONTROL From]** - und das **[!UICONTROL To]** -Datum auszuwählen, damit die Änderung wirksam wird.

   - Um ein anderes Design auf die Seite anzuwenden, wählen Sie den Namen des **[!UICONTROL New Theme]** aus.

   - Um das Spaltenlayout der Seite zu ändern, wählen Sie die **[!UICONTROL Layout]** aus, die Sie anwenden möchten.

### Schritt 7: Vorschau der Seite anzeigen

1. Klicken Sie auf den Pfeil **[!UICONTROL Save]** und wählen Sie **[!UICONTROL Save & Close]** aus, um zum Raster Seiten zurückzukehren.

1. Suchen Sie die Seite im Raster und wählen Sie **[!UICONTROL View]** in der Spalte _[!UICONTROL Action]_aus.

1. Um zum Raster zurückzukehren, klicken Sie in der oberen linken Ecke des Browser-Fensters auf **[!UICONTROL Back]** .

### Schritt 8: Publish der Seite

1. Wählen Sie **[!UICONTROL Edit]** in der Spalte _[!UICONTROL Action]_des Rasters aus.

1. Setzen Sie **[!UICONTROL Enable Page]** auf `Yes`.

1. Klicken Sie auf den Pfeil **[!UICONTROL Save]** und wählen Sie **[!UICONTROL Save & Close]**.

## Seite duplizieren

Jede Inhaltsseite kann als Vorlage verwendet und als Duplikat gespeichert werden. Sie können diese zeitsparende Technik verwenden, um ein konsistentes Design für Inhaltsseiten auf Ihrer gesamten Site zu erstellen. Auf der doppelten Seite wird der Seitentitel des Originals beibehalten, aber die Felder URL-Schlüssel und Status müssen aktualisiert werden.

![Speichern und Duplizieren](./assets/page-duplicate-save-menu.png){width="600" zoomable="yes"}

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Suchen Sie im Raster die zu duplizierende Seite und klicken Sie in der Spalte _[!UICONTROL Action]_auf **[!UICONTROL Edit]**.

1. Klicken Sie auf den Pfeil **[!UICONTROL Save]** und wählen Sie **[!UICONTROL Save & Duplicate]**.

1. Wenn Sie die Meldungen sehen, die die Seite gespeichert und dupliziert wurde, klicken Sie in der oberen Schaltflächenleiste auf **[!UICONTROL Back]** , um zum Raster zurückzukehren.

1. Suchen Sie die doppelte Seite im Raster und beachten Sie Folgendes:

   - Der Seitentitel ist identisch mit dem Original.
   - Ein eindeutiger, aber temporärer URL-Schlüssel wird zugewiesen.
   - Der Status der Seite ist `Disabled`.

1. Öffnen Sie die doppelte Seite im Modus _Bearbeiten_ und führen Sie die folgenden Schritte aus:

   - Wenn Sie die Seite sofort veröffentlichen möchten, setzen Sie **[!UICONTROL Enable Page]** auf `Yes`.

   - Aktualisieren Sie die **[!UICONTROL Page Title]** nach Bedarf.

   - Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Search Engine Optimization]** und geben Sie den eindeutigen **[!UICONTROL URL Key]** ein, den Sie für die duplizierte Seite verwenden möchten.

     ![Temporärer URL-Schlüssel](./assets/page-search-engine-optimization-url-key-duplicate.png){width="600" zoomable="yes"}

   - Aktualisieren Sie den verbleibenden Seiteninhalt nach Bedarf.

1. Klicken Sie auf den Pfeil **[!UICONTROL Save]** und wählen Sie **[!UICONTROL Save & Close]**.

   Die doppelte Seite im Raster spiegelt Ihre Änderungen wider.

## Menü &quot;Speichern&quot;

| Befehl | Beschreibung |
|--- |--- |
| [!UICONTROL Save] | Speichern Sie die aktuelle Seite und fahren Sie mit der Arbeit fort. |
| [!UICONTROL Save & New] | Speichern und schließen Sie die aktuelle Seite und beginnen Sie mit einer neuen Seite. |
| [!UICONTROL Save & Duplicate] | Speichern und schließen Sie die aktuelle Seite und öffnen Sie eine neue Kopie. |
| [!UICONTROL Save & Close] | Speichern und schließen Sie die aktuelle Seite und kehren Sie zum Raster Seiten zurück. |

{style="table-layout:auto"}

## Löschen einer Seite

Es gibt zwei Möglichkeiten, eine erstellte Seite zu entfernen. Sie können sie aus dem Raster _[!UICONTROL Pages]_oder aus der Seite_[!UICONTROL Edit]_ entfernen.

### Methode 1: Entfernen einer Seite aus dem Raster &quot;Seiten&quot;

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Suchen Sie die Seiten mithilfe von Filtern über dem Raster und aktivieren Sie das Kontrollkästchen für eine oder mehrere Seiten, die gelöscht werden sollen.

1. Setzen Sie **[!UICONTROL Actions]** in der linken oberen Ecke der Liste auf `Delete`.

1. Um die Aktion zu bestätigen, klicken Sie auf **[!UICONTROL OK]**.

### Methode 2: Entfernen einer Seite aus der Bearbeitungsseite

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Suchen Sie die zu löschende Seite.

1. Klicken Sie in der Spalte _[!UICONTROL Actions]_für die Seitenentität auf **[!UICONTROL Select]**und wählen Sie **[!UICONTROL Edit]**.

1. Klicken Sie in der Schaltflächenleiste auf **[!UICONTROL Delete Page]**.

1. Um die Aktion zu bestätigen, klicken Sie auf **[!UICONTROL OK]**.
