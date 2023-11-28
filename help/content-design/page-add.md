---
title: Hinzufügen und Entfernen von Seiten
description: Erfahren Sie, wie Sie in Ihrer [!DNL Commerce] speichern.
exl-id: a7a503ea-3631-4be2-81e4-aed2ae9419dc
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '1091'
ht-degree: 0%

---

# Hinzufügen und Entfernen von Seiten

Der Prozess zum Hinzufügen einer Inhaltsseite zu Ihrem Store ist im Wesentlichen derselbe für jeden Seitentyp, den Sie erstellen möchten. Sie können Text, Bilder, Inhaltsblöcke, Variablen und Widgets einschließen. Die meisten Inhaltsseiten sind für das Lesen von Suchmaschinen zuerst und von Personen danach konzipiert. Berücksichtigen Sie bei der Auswahl des Seitentitels und der URL sowie beim Zusammenstellen der Metadaten und Inhalte die Bedürfnisse jeder dieser beiden Zielgruppen. Wenn Ihre Seite abgeschlossen ist, kann sie zu Ihrer Store-Navigation hinzugefügt, mit anderen Seiten verknüpft, über die Fußzeile Ihres Stores verknüpft oder als neuer [Startseite](page-home-new.md).

![Seitenraster](./assets/pages-grid.png){width="700" zoomable="yes"}

## Hinzufügen einer Seite

Die folgenden Anweisungen führen Sie durch jeden Schritt, um eine einfache Seite zu erstellen. Einige erweiterte Funktionen werden übersprungen, aber in anderen Themen behandelt.

### Schritt 1: Erstellen der Seite

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Klicken **[!UICONTROL Add New Page]**.

   ![Neue Seite](./assets/pages-new-page.png){width="600" zoomable="yes"}

1. Wenn Sie die Seite nicht sofort veröffentlichen möchten, legen Sie **[!UICONTROL Enable Page]** nach `No`.

1. Geben Sie die **[!UICONTROL Page Title]**.

   Der Seitentitel wird im [Breadcrumb](../catalog/navigation-breadcrumb-trail.md) Navigation.

### Schritt 2: Inhalt abschließen

Je nach [Erweiterte Konfiguration der Inhaltstools](../configuration-reference/general/content-management.md), den Seiteninhalt hinzufügen.

#### Verwenden der Inhaltstools für den Seitenaufbau

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) **[!UICONTROL Content]**.

   ![Inhalt mit Page Builder](../page-builder/assets/pb-page-content.png){width="600" zoomable="yes"}

1. Im **[!UICONTROL Content Heading]** Geben Sie die Überschrift ein, die oben auf der Seite angezeigt werden soll.

   Wenn diese Option aktiviert ist, wird die [Page Builder](../page-builder/introduction.md) Bühne und Bedienfeld werden unter der Inhaltsüberschrift angezeigt. Weitere Informationen finden Sie unter [Arbeitsbereich](../page-builder/workspace.md). Wenn _Page Builder_ nicht aktiviert ist, wird der Editor im WYSIWYG-Modus mit der Symbolleiste am oberen Rand geöffnet.

1. Füllen Sie den Inhalt aus und formatieren Sie den Text nach Bedarf.

#### Verwenden der Editor-Symbolleiste

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) **[!UICONTROL Content]**.

   ![Inhalt](./assets/page-content-editor.png){width="600" zoomable="yes"}

1. Im **[!UICONTROL Content Heading]** Geben Sie die Überschrift ein, die oben auf der Seite angezeigt werden soll.

1. Füllen Sie den Inhalt aus und formatieren Sie den Text nach Bedarf.

   Sie können [images](media-storage.md), [variables](../systems/variables-predefined.md), und [Widgets](widgets.md) nach Bedarf. Weitere Informationen finden Sie unter [Verwenden des Editors](editor.md).

### Schritt 3: SEO-Informationen ausfüllen

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) **[!UICONTROL Search Engine Optimization]**.

   ![Suchmaschinenoptimierung](./assets/page-search-engine-optimization.png){width="600" zoomable="yes"}

1. Akzeptieren Sie entweder die Standardeinstellung oder geben Sie einen anderen ein **[!UICONTROL URL Key]** , die aus allen Kleinbuchstaben mit Bindestrichen anstelle von Leerzeichen besteht.

   Der Standard-URL-Schlüssel wurde beim Speichern der Seite erstellt und basiert auf der Inhaltsüberschrift.

1. Geben Sie einen **[!UICONTROL Meta Title]** für die Seite.

   Der Metadatentitel sollte weniger als 70 Zeichen enthalten und wird in der Titelleiste und Registerkarte des Browsers angezeigt.

1. Geben Sie Ihre Auswahl an High-Value ein. **[!UICONTROL Meta Keywords]** die Suchmaschinen verwenden können, um die Seite zu indizieren.

   Trennen Sie mehrere Wörter durch ein Komma. Meta-Suchbegriffe werden von einigen Suchmaschinen ignoriert, aber von anderen verwendet.

1. Für **[!UICONTROL Meta Description]** eine kurze Beschreibung der Seite für die Liste der Suchergebnisse eingeben.

   Idealerweise sollte die Beschreibung 150 bis 160 Zeichen lang sein, mit einer maximalen Länge von 255 Zeichen.

1. Klicken **[!UICONTROL Save]**.

### Schritt 4: Festlegen des Umfangs der Seite

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) **[!UICONTROL Page in Websites]**.

   ![Seiten in Websites](./assets/page-in-websites.png){width="600" zoomable="yes"}

1. Im **[!UICONTROL Store View]** Liste auswählen, wählen Sie jede Ansicht aus, in der die Seite verfügbar sein soll.

   Wenn die Installation über mehrere Websites verfügt, wählen Sie jede Website und Store-Ansicht aus, in der die Seite verfügbar sein soll.

### Schritt 5: Übergeordnete Seite identifizieren (falls zutreffend)

{{ee-feature}}

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) **[!UICONTROL Hierarchy]**.

   ![Hierarchie](./assets/page-hierarchy.png){width="600" zoomable="yes"}

1. Wenn diese Seite ein untergeordnetes Element einer anderen Seite ist, aktivieren Sie das Kontrollkästchen der **[!UICONTROL Parent page]**.

### Schritt 6: Designänderungen eingeben (optional)

1. Zum Ändern des Seitenlayouts erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) **[!UICONTROL Design]**.

   ![Design](./assets/page-design.png){width="600" zoomable="yes"}

1. Um das Spaltenlayout der Seite zu ändern, legen Sie **[!UICONTROL Layout]** auf einen der folgenden Werte zu:

   - `Empty`
   - `1 column`
   - `2 columns with left bar`
   - `2 columns with right bar`
   - `3 columns`
   - `Page -- Full Width` (Erfordert [Page Builder](../page-builder/introduction.md))
   - `Category -- Full Width` (Seitenaufbau erforderlich)
   - `Product -- Full Width` (Seitenaufbau erforderlich)

1. So wenden Sie eine **[!UICONTROL Custom Layout Update]**, wählen Sie den Namen der Datei aus der Liste aus.

   Weitere Informationen finden Sie unter [Layout-Updates](layout-updates.md).

1. Um das Design der Seite zu ändern, legen Sie **[!UICONTROL New Theme]** auf einen der folgenden Werte zu:

   - `Magento Black`
   - `Magento Luma`

1. ![Magento Open Source](../assets/open-source.svg) (Nur Magento Open Source) Um eine Designänderung zu planen, erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) **[!UICONTROL Custom Design Update]** und gehen Sie wie folgt vor:

   ![Benutzerdefinierte Design-Aktualisierung](./assets/page-custom-design-update.png){width="600" zoomable="yes"}

   - Verwenden Sie den Kalender (![Kalendersymbol](../assets/icon-calendar.png)), um die **[!UICONTROL From]** und **[!UICONTROL To]** Daten für den Wirksamwerden der Änderung.

   - Um ein anderes Design auf die Seite anzuwenden, wählen Sie den Namen der **[!UICONTROL New Theme]**.

   - Um das Spaltenlayout der Seite zu ändern, wählen Sie die **[!UICONTROL Layout]** die Sie anwenden möchten.

### Schritt 7: Vorschau der Seite anzeigen

1. Klicken Sie auf **[!UICONTROL Save]** Pfeil und Auswahl **[!UICONTROL Save & Close]** , um zum Raster Seiten zurückzukehren.

1. Suchen Sie die Seite im Raster und wählen Sie **[!UICONTROL View]** im _[!UICONTROL Action]_Spalte.

1. Um zum Raster zurückzukehren, klicken Sie auf **[!UICONTROL Back]** in der linken oberen Ecke des Browserfensters.

### Schritt 8: Veröffentlichen der Seite

1. Auswählen **[!UICONTROL Edit]** im _[!UICONTROL Action]_Spalte des Rasters.

1. Satz **[!UICONTROL Enable Page]** nach `Yes`.

1. Klicken Sie auf **[!UICONTROL Save]** Pfeil und Auswahl **[!UICONTROL Save & Close]**.

## Seite duplizieren

Jede Inhaltsseite kann als Vorlage verwendet und als Duplikat gespeichert werden. Sie können diese zeitsparende Technik verwenden, um ein konsistentes Design für Inhaltsseiten auf Ihrer gesamten Site zu erstellen. Auf der doppelten Seite wird der Seitentitel des Originals beibehalten, aber die Felder URL-Schlüssel und Status müssen aktualisiert werden.

![Speichern und duplizieren](./assets/page-duplicate-save-menu.png){width="600" zoomable="yes"}

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Suchen Sie im Raster die zu duplizierende Seite und klicken Sie auf **[!UICONTROL Edit]** im _[!UICONTROL Action]_Spalte.

1. Klicken Sie auf **[!UICONTROL Save]** Pfeil und Auswahl **[!UICONTROL Save & Duplicate]**.

1. Wenn Sie die Meldungen sehen, die die Seite gespeichert und dupliziert wurde, klicken Sie auf **[!UICONTROL Back]** in der oberen Schaltflächenleiste, um zum Raster zurückzukehren.

1. Suchen Sie die doppelte Seite im Raster und beachten Sie Folgendes:

   - Der Seitentitel ist identisch mit dem Original.
   - Ein eindeutiger, aber temporärer URL-Schlüssel wird zugewiesen.
   - Der Status der Seite lautet `Disabled`.

1. Öffnen Sie die doppelte Seite in _Bearbeiten_ und führen Sie folgende Schritte aus:

   - Wenn Sie die Seite sofort veröffentlichen möchten, legen Sie **[!UICONTROL Enable Page]** nach `Yes`.

   - Aktualisieren Sie die **[!UICONTROL Page Title]** nach Bedarf.

   - Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Search Engine Optimization]** und geben Sie die eindeutige **[!UICONTROL URL Key]** , die Sie für die duplizierte Seite verwenden möchten.

     ![Temporärer URL-Schlüssel](./assets/page-search-engine-optimization-url-key-duplicate.png){width="600" zoomable="yes"}

   - Aktualisieren Sie den verbleibenden Seiteninhalt nach Bedarf.

1. Klicken Sie auf **[!UICONTROL Save]** Pfeil und Auswahl **[!UICONTROL Save & Close]**.

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

Es gibt zwei Möglichkeiten, eine erstellte Seite zu entfernen. Sie können sie aus dem _[!UICONTROL Pages]_Raster oder aus dem_[!UICONTROL Edit]_ Seite.

### Methode 1: Entfernen einer Seite aus dem Raster &quot;Seiten&quot;

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Suchen Sie die Seiten mithilfe von Filtern über dem Raster und aktivieren Sie das Kontrollkästchen für eine oder mehrere Seiten, die gelöscht werden sollen.

1. Legen Sie in der linken oberen Ecke der Liste **[!UICONTROL Actions]** nach `Delete`.

1. Klicken Sie zur Bestätigung der Aktion auf **[!UICONTROL OK]**.

### Methode 2: Entfernen einer Seite aus der Bearbeitungsseite

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Suchen Sie die zu löschende Seite.

1. Im _[!UICONTROL Actions]_Spalte für die Seitenentität, klicken Sie auf **[!UICONTROL Select]**und wählen **[!UICONTROL Edit]**.

1. Klicken Sie in der Symbolleiste auf **[!UICONTROL Delete Page]**.

1. Klicken Sie zur Bestätigung der Aktion auf **[!UICONTROL OK]**.
