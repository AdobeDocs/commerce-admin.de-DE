---
title: Widgets erstellen und verwalten
description: Erfahren Sie, wie Sie Widgets erstellen und verwalten, mit denen Inhalte in Ihrem gesamten Store automatisch aktualisiert werden.
exl-id: 680f2f41-ec51-4ac6-9e92-2817591af3e6
source-git-commit: 7288a4f47940e07c4d083826532308228d271c5e
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 0%

---

# Widgets erstellen und verwalten

Widgets sind wiederverwendbare Komponenten. Sie können einfach Widgets erstellen und vorhandene ändern, um Inhalte in Ihrem gesamten Store automatisch zu aktualisieren. Sie können auch nicht mehr verwendete Widgets löschen.

![Widgets](./assets/widgets.png){width="700" zoomable="yes"}

## Erstellen eines Widgets

Der Prozess zum Erstellen eines Widgets ist für jeden [Widget-Typ](widgets.md#widget-types) fast identisch. Sie können dem ersten Teil der Anweisungen folgen und dann den letzten Teil für den gewünschten Widget-Typ ausfüllen.

### Schritt 1: Auswählen des Typs

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Klicken Sie auf **[!UICONTROL Add Widget]**.

1. Im Abschnitt _[!UICONTROL Settings]_:

   - Setzen Sie **[!UICONTROL Type]** auf den Widget-Typ, den Sie erstellen möchten.

   - Stellen Sie sicher, dass **[!UICONTROL Design Theme]** auf das aktuelle Design eingestellt ist.

     ![Widget-Einstellungen](./assets/widget-settings.png){width="600" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Continue]**.

### Schritt 2: Festlegen der Storefront-Eigenschaften und des Layouts

1. Im Abschnitt _[!UICONTROL Storefront Properties]_:

   - Geben Sie für **[!UICONTROL Widget Title]** einen beschreibenden Titel für das Widget ein.

     Dieser Titel ist nur vom Administrator sichtbar.

   - Wählen Sie für &quot;**[!UICONTROL Assign to Store Views]**&quot;die Store-Ansichten aus, in denen das Widget sichtbar sein soll.

     Sie können eine bestimmte Store-Ansicht oder `All Store Views` auswählen. Um mehrere Ansichten auszuwählen, halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie auf jede Option.

   - (Optional) Geben Sie für &quot;**[!UICONTROL Sort Order]**&quot;eine Zahl ein, um die Reihenfolge zu bestimmen, in der dieses Element mit anderen im selben Teil der Seite angezeigt wird. (`0` = first, `1` = second, `3` = third usw.)

     ![Storefront-Eigenschaften](./assets/widget-storefront-properties.png){width="600" zoomable="yes"}

1. Klicken Sie im Abschnitt _[!UICONTROL Layout Updates]_auf **[!UICONTROL Add Layout Update]**.

1. Setzen Sie &quot;**[!UICONTROL Display On]**&quot;auf den Seitentyp, auf dem sie angezeigt werden soll.

1. Wählen Sie in der Liste **[!UICONTROL Container]** den Bereich des Seitenlayouts aus, in dem er platziert werden soll.

   ![Layout-Updates](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

1. Wenn das Widget ein Link ist, setzen Sie **[!UICONTROL Template]** auf einen der folgenden Werte:

   - `Block Template` - Formatiert den Inhalt so, dass er als eigenständige Einheit auf der Seite platziert werden kann.
   - `Inline Template` - Formatiert den Inhalt, damit er in anderen Inhalten platziert werden kann. Beispiel: ein Link, der in einen Textabsatz gehört.

### Schritt 3: Ausführen der Widget-Optionen

Die Optionen für die einzelnen Widget-Typen variieren geringfügig, doch der Prozess ist im Wesentlichen identisch. Im folgenden Beispiel wird die Produktliste für eine bestimmte Kategorie mit Paginierungssteuerelementen angezeigt.

1. Wählen Sie im linken Bereich **[!UICONTROL Widget Options]** aus.

1. Klicken Sie auf **[!UICONTROL Select Block]**.

1. Geben Sie eine **[!UICONTROL Title]** ein, die oberhalb der Liste angezeigt werden soll, z. B. `Featured Products`.

1. Legen Sie für die Seitenumbruchsteuerungen **[!UICONTROL Display Page Control]** auf `Yes` fest und führen Sie folgende Schritte aus:

   - Geben Sie den Wert **[!UICONTROL Number of Products per Page]** ein.

   - Geben Sie die Gesamtsumme **[!UICONTROL Number of Products to Display]** ein.

   - Setzen Sie **[!UICONTROL Condition]** auf die Kategorie der Produkte, die vorgestellt werden sollen.

     Der Prozess entspricht dem Festlegen einer Bedingung für eine [Preisregel](../merchandising-promotions/price-rules-catalog.md).

### Schritt 4: Speichern und überprüfen Sie das Ergebnis

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]**.

1. Befolgen Sie bei Aufforderung die Anweisungen oben im Arbeitsbereich, um den Cache nach Bedarf zu aktualisieren.

1. Kehren Sie zu Ihrer Storefront zurück, um zu überprüfen, ob das Widget ordnungsgemäß funktioniert.

   Um es an eine andere Position zu verschieben, können Sie das Widget erneut öffnen und eine andere Seite oder Blockreferenz ausprobieren.

## Demo zur Widget-Erstellung

In diesem Video erfahren Sie mehr über das Erstellen von Widgets:

>[!VIDEO](https://video.tv.adobe.com/v/343786?quality=12&learn=on)

## Widget bearbeiten

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Suchen Sie das Widget mithilfe der Filter über dem Raster und klicken Sie dann auf den Widget-Namen.

1. Nehmen Sie die erforderlichen Änderungen vor.

   Informationen zu den Widget-Optionen finden Sie in den Schritten zum Erstellen eines Widgets .

1. Klicken Sie auf &quot;**[!UICONTROL Save]**&quot;.

## Widget löschen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Suchen Sie die Widgets mithilfe der Filter über dem Raster und aktivieren Sie dann das Kontrollkästchen der zu löschenden Widgets.

1. Setzen Sie **[!UICONTROL Actions]** in der linken oberen Ecke der Liste auf `Delete`.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Submit]**.

1. Um die Aktion zu bestätigen, klicken Sie auf **[!UICONTROL OK]**.
