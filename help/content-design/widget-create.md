---
title: Widgets erstellen und verwalten
description: Erfahren Sie, wie Sie Widgets erstellen und verwalten, mit denen Inhalte in Ihrem gesamten Store automatisch aktualisiert werden.
exl-id: 680f2f41-ec51-4ac6-9e92-2817591af3e6
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 1%

---

# Widgets erstellen und verwalten

Widgets sind wiederverwendbare Komponenten. Sie können einfach Widgets erstellen und vorhandene ändern, um Inhalte in Ihrem gesamten Store automatisch zu aktualisieren. Sie können auch nicht mehr verwendete Widgets löschen.

![Widgets](./assets/widgets.png){width="700" zoomable="yes"}

## Erstellen eines Widgets

Der Prozess zum Erstellen eines Widgets ist für jede [Widget-Typ](widgets.md#widget-types). Sie können dem ersten Teil der Anweisungen folgen und dann den letzten Teil für den gewünschten Widget-Typ ausfüllen.

### Schritt 1: Auswählen des Typs

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Klicken **[!UICONTROL Add Widget]**.

1. Im _[!UICONTROL Settings]_Abschnitt:

   - Satz **[!UICONTROL Type]** zum Widget-Typ, den Sie erstellen möchten.

   - Stellen Sie sicher, dass **[!UICONTROL Design Theme]** auf das aktuelle Design eingestellt ist.

     ![Widget-Einstellungen](./assets/widget-settings.png){width="600" zoomable="yes"}

1. Klicken **[!UICONTROL Continue]**.

### Schritt 2: Festlegen der Storefront-Eigenschaften und des Layouts

1. Im _[!UICONTROL Storefront Properties]_Abschnitt:

   - Für **[!UICONTROL Widget Title]**, geben Sie einen beschreibenden Titel für das Widget ein.

     Dieser Titel ist nur vom Administrator sichtbar.

   - Für **[!UICONTROL Assign to Store Views]**, wählen Sie die Store-Ansichten aus, in denen das Widget sichtbar sein soll.

     Sie können eine bestimmte Store-Ansicht auswählen oder `All Store Views`. Um mehrere Ansichten auszuwählen, halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie auf jede Option.

   - (Optional) Für **[!UICONTROL Sort Order]** Geben Sie eine Zahl ein, um die Reihenfolge zu bestimmen, in der dieses Element mit anderen Elementen im selben Teil der Seite angezeigt wird. (`0` = first, `1` = Sekunde, `3` = drittes Element usw.)

     ![Storefront-Eigenschaften](./assets/widget-storefront-properties.png){width="600" zoomable="yes"}

1. Im _[!UICONTROL Layout Updates]_Abschnitt, klicken Sie auf **[!UICONTROL Add Layout Update]**.

1. Satz **[!UICONTROL Display On]** zum Typ der Seite, auf der sie angezeigt werden soll.

1. Im **[!UICONTROL Container]** wählen Sie den Bereich des Seitenlayouts aus, in dem er platziert werden soll.

   ![Layout-Aktualisierungen](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

1. Wenn das Widget ein Link ist, legen Sie **[!UICONTROL Template]** auf einen der folgenden Werte zu:

   - `Block Template` - Formatiert den Inhalt so, dass er als eigenständige Einheit auf der Seite platziert werden kann.
   - `Inline Template` - Formatiert den Inhalt, damit er in anderen Inhalten platziert werden kann. Beispiel: ein Link, der in einen Textabsatz gehört.

### Schritt 3: Ausführen der Widget-Optionen

Die Optionen für die einzelnen Widget-Typen variieren geringfügig, doch der Prozess ist im Wesentlichen identisch. Im folgenden Beispiel wird die Produktliste für eine bestimmte Kategorie mit Paginierungssteuerelementen angezeigt.

1. Wählen Sie im linken Bereich die Option **[!UICONTROL Widget Options]**.

1. Klicken **[!UICONTROL Select Block]**.

1. Geben Sie einen **[!UICONTROL Title]** über der Liste angezeigt werden, z. B. `Featured Products`.

1. Legen Sie für Paginierungssteuerungen **[!UICONTROL Display Page Control]** nach `Yes`  und gehen Sie wie folgt vor:

   - Geben Sie die **[!UICONTROL Number of Products per Page]**.

   - Gesamtsumme angeben **[!UICONTROL Number of Products to Display]**.

   - Satz **[!UICONTROL Condition]** in die Kategorie der Produkte, die vorgestellt werden sollen.

     Der Prozess entspricht dem Festlegen einer Bedingung für eine [Preisregel](../merchandising-promotions/price-rules-catalog.md).

### Schritt 4: Speichern und überprüfen Sie das Ergebnis

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]**.

1. Befolgen Sie bei Aufforderung die Anweisungen oben im Arbeitsbereich, um den Cache nach Bedarf zu aktualisieren.

1. Kehren Sie zu Ihrer Storefront zurück, um zu überprüfen, ob das Widget ordnungsgemäß funktioniert.

   Um es an eine andere Position zu verschieben, können Sie das Widget erneut öffnen und eine andere Seite oder Blockreferenz ausprobieren.

## Demo zur Widget-Erstellung

In diesem Video erfahren Sie mehr über das Erstellen von Widgets:

>[!VIDEO](https://video.tv.adobe.com/v/343786?quality=12)

## Widget bearbeiten

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Suchen Sie das Widget mithilfe der Filter über dem Raster und klicken Sie dann auf den Widget-Namen.

1. Nehmen Sie die erforderlichen Änderungen vor.

   Informationen zu den Widget-Optionen finden Sie in den Schritten zum Erstellen eines Widgets .

1. Klicken Sie auf **[!UICONTROL Save]**.

## Widget löschen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Suchen Sie die Widgets mithilfe der Filter über dem Raster und aktivieren Sie dann das Kontrollkästchen der zu löschenden Widgets.

1. Legen Sie in der linken oberen Ecke der Liste **[!UICONTROL Actions]** nach `Delete`.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Submit]**.

1. Klicken Sie zur Bestätigung der Aktion auf **[!UICONTROL OK]**.
