---
title: Erstellen und Verwalten von Widgets
description: Erfahren Sie, wie Sie Widgets erstellen und verwalten, die automatisch Inhalte in Ihrem Store aktualisieren.
exl-id: 680f2f41-ec51-4ac6-9e92-2817591af3e6
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 0%

---

# Erstellen und Verwalten von Widgets

Widgets sind wiederverwendbare Komponenten. Sie können auf einfache Weise Widgets erstellen und vorhandene ändern, um Inhalte in Ihrem Store automatisch zu aktualisieren. Sie können auch nicht mehr verwendete Widgets löschen.

![Widgets](./assets/widgets.png){width="700" zoomable="yes"}

## Erstellen eines Widgets

Der Prozess zum Erstellen eines Widgets ist für jeden [Widget-Typ“ nahezu ](widgets.md#widget-types). Sie können dem ersten Teil der Anweisungen folgen und dann den letzten Teil für den gewünschten Widget-Typ ausfüllen.

### Schritt 1: Typ auswählen

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Klicken Sie auf **[!UICONTROL Add Widget]**.

1. Im _[!UICONTROL Settings]_Abschnitt:

   - Legen Sie **[!UICONTROL Type]** auf den Widget-Typ fest, den Sie erstellen möchten.

   - Stellen Sie sicher, dass die **[!UICONTROL Design Theme]** auf das aktuelle Design eingestellt ist.

     ![Widget-Einstellungen](./assets/widget-settings.png){width="600" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Continue]**.

### Schritt 2: Eigenschaften und Layout der Storefront angeben

1. Im _[!UICONTROL Storefront Properties]_Abschnitt:

   - Geben Sie **[!UICONTROL Widget Title]** einen beschreibenden Titel für das Widget ein.

     Dieser Titel ist nur von der Administratorin bzw. dem Administrator sichtbar.

   - Wählen Sie **[!UICONTROL Assign to Store Views]** die Store-Ansichten aus, in denen das Widget sichtbar sein soll.

     Sie können eine bestimmte Shop-Ansicht oder `All Store Views` auswählen. Halten Sie zum Auswählen mehrerer Ansichten die Strg-Taste (PC) bzw. die Befehlstaste (Mac) gedrückt und klicken Sie auf die einzelnen Optionen.

   - (Optional) Geben Sie **[!UICONTROL Sort Order]** eine Zahl ein, um die Reihenfolge zu bestimmen, in der dieses Element zusammen mit anderen im selben Teil der Seite angezeigt wird. (`0` = First, `1` = Second, `3` = Third usw.)

     ![Storefront-Eigenschaften](./assets/widget-storefront-properties.png){width="600" zoomable="yes"}

1. Klicken Sie im Abschnitt _[!UICONTROL Layout Updates]_auf **[!UICONTROL Add Layout Update]**.

1. Legen Sie **[!UICONTROL Display On]** auf den Seitentyp fest, auf dem es angezeigt werden soll.

1. Wählen Sie in der **[!UICONTROL Container]**-Liste den Bereich des Seiten-Layouts aus, in dem er platziert werden soll.

   ![Layout-Aktualisierungen](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

1. Wenn es sich bei dem Widget um einen Link handelt, legen Sie **[!UICONTROL Template]** auf einen der folgenden Werte fest:

   - `Block Template` - Formatiert den Inhalt, damit er als eigenständige Einheit auf der Seite platziert werden kann.
   - `Inline Template` - Formatiert den Inhalt, damit er in anderen Inhalten platziert werden kann. Beispiel: ein Link, der in einen Textabsatz eingefügt wird.

### Schritt 3: Vervollständigen Sie die Widget-Optionen

Die Optionen für jeden Widget-Typ variieren geringfügig, der Prozess ist jedoch im Wesentlichen identisch. Im folgenden Beispiel wird die Produktliste für eine bestimmte Kategorie mit Steuerelementen für die Paginierung angezeigt.

1. Wählen Sie im linken Bedienfeld **[!UICONTROL Widget Options]** aus.

1. Klicken Sie auf **[!UICONTROL Select Block]**.

1. Geben Sie einen **[!UICONTROL Title]** ein, der über der Liste angezeigt werden soll, z. B. `Featured Products`.

1. Legen Sie für die Steuerelemente für die Paginierung **[!UICONTROL Display Page Control]** auf `Yes` fest und führen Sie folgende Schritte aus:

   - Geben Sie die **[!UICONTROL Number of Products per Page]** ein.

   - Geben Sie die **[!UICONTROL Number of Products to Display]** ein.

   - **[!UICONTROL Condition]** Sie auf die Kategorie der anzuzeigenden Produkte.

     Der Prozess ist der gleiche wie das Festlegen einer Bedingung für eine [Preisregel](../merchandising-promotions/price-rules-catalog.md).

### Schritt 4: Speichern und überprüfen Sie das Ergebnis

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.

1. Befolgen Sie bei Aufforderung die Anweisungen oben im Arbeitsbereich, um den Cache nach Bedarf zu aktualisieren.

1. Kehren Sie zu Ihrer Storefront zurück, um zu überprüfen, ob das Widget ordnungsgemäß funktioniert.

   Um es an eine andere Position zu verschieben, können Sie das Widget erneut öffnen und eine andere Seite oder Blockreferenz ausprobieren.

## Demo zur Widget-Erstellung

In diesem Video erfahren Sie mehr über das Erstellen von Widgets:

>[!VIDEO](https://video.tv.adobe.com/v/343786?quality=12&learn=on)

## Bearbeiten eines Widgets

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Suchen Sie das Widget mithilfe der Filter über dem Raster und klicken Sie dann auf den Widget-Namen.

1. Nehmen Sie die erforderlichen Änderungen vor.

   Informationen zu den Widget-Optionen finden Sie in den Schritten zum Erstellen eines Widgets .

1. Klicken Sie auf die **[!UICONTROL Save]**.

## Löschen eines Widgets

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Suchen Sie die Widgets mithilfe der Filter über dem Raster und aktivieren Sie dann das Kontrollkästchen der zu löschenden Widgets.

1. Setzen Sie oben links in der Liste **[!UICONTROL Actions]** auf `Delete`.

1. Klicken Sie abschließend auf **[!UICONTROL Submit]**.

1. Um die Aktion zu bestätigen, klicken Sie auf **[!UICONTROL OK]**.
