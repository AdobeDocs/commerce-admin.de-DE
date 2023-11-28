---
title: Produktmuster
description: Erfahren Sie, wie Sie Muster für Ihre konfigurierbaren Produktlisten definieren.
exl-id: 6163cec4-5d84-4e2c-ba5c-3c22ac4e3f28
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1160'
ht-degree: 0%

---

# Produktmuster

Kunden haben hohe Erwartungen an die Auswahl einer Farbe, und es ist wichtig, dass Produktbeschreibungen jede verfügbare Farbe, Muster oder Textur genau darstellen. Beispielsweise sind die Hosen im folgenden Beispiel nicht in Rot, Grün und Blau verfügbar. Stattdessen sind sie nur in bestimmten Rot-, Grün- und Blau-Farbtönen verfügbar, die für dieses Produkt wahrscheinlich einzigartig sind.

![Muster auf einer Produktseite](./assets/storefront-color-swatches.png){width="700" zoomable="yes"}

Für [konfigurierbare Produkte](product-create-configurable.md), kann die Farbe durch ein visuelles Muster, ein Textmuster oder ein Eingabefeld angegeben werden. Muster können auf der Produktseite, in Produktlisten und in [mehrstufige Navigation](navigation-layered.md). Auf der Produktseite werden Muster synchronisiert, um das entsprechende Produktbild anzuzeigen, wenn das Muster ausgewählt wird. Wenn der Kunde das Muster auswählt, wird der entsprechende Wert im Eingabefeld angezeigt und das Muster wird als aktuelle Auswahl dargestellt.

>[!NOTE]
>
>Farbfeldattribute können so konfiguriert werden, dass bei Auswahl des Farbmusters keine entsprechenden einfachen Produktbilder angezeigt werden, indem die Einstellung _[!UICONTROL Update Product Preview Image]_Optionswert auf `No` auf [!UICONTROL Attribute Edit] in der Admin-Seite.

## Textbasierte Farbfelder

Wenn für ein Muster kein Bild verfügbar ist, wird der Attributwert als Text angezeigt. Ein textbasiertes Muster ähnelt einer Schaltfläche mit einer Textbeschriftung und verhält sich genauso wie ein Muster mit einem Bild. Wenn textbasierte Muster verwendet werden, um die verfügbaren Größen anzuzeigen, wird jede nicht verfügbare Größe durchkreuzt.

![Textbasierte Musterauswahl zeigt die nicht vorrätige Größe an](./assets/storefront-swatch-size-out-of-stock.png){width="700" zoomable="yes"}

## Muster in der Navigation mit Ebenen

Muster können auch in der Navigation mit Ebenen verwendet werden, wenn die _[!UICONTROL Use in Layered Navigation]_-Eigenschaft des Farbattributs auf `Yes`. Das folgende Beispiel zeigt sowohl textbasierte als auch farbige Bildmuster in der Navigation mit Ebenen.

![Muster in der Navigation mit Ebenen](./assets/storefront-swatches-layered-navigation.png){width="700" zoomable="yes"}

## Erstellen von Mustern für Produkte

Muster können als Komponente der `color` Attribut zuweisen oder lokal für ein bestimmtes Produkt einrichten und als [Produktbilder](product-image.md#upload-an-image).

In den vorherigen Beispielen sind die Hosen &quot;Sylvia Capri&quot;in bestimmten Werten von `red`, `green`, und `blue`. Da die Farbmuster aus dem Produktbild entnommen wurden, ist jede eine wahre Darstellung der Farbe. Die `color` -Attribut wird verwendet, um die Informationen für alle Produktfarben und Farbfelder zu verwalten.

### Schritt 1: Erstellen der Muster

Verwenden Sie eine der folgenden Methoden, um Muster für Ihre Produkte zu erstellen.

#### Methode 1: Farbmuster hinzufügen

1. Um die wahre Farbe eines Produkts zu erfassen, öffnen Sie das Bild in einem Foto-Editor und verwenden Sie das Auge-Dropper-Tool, um die genaue Farbe zu identifizieren und den entsprechenden Hexadezimalwert zu beachten.

   ![Hexadezimalfarbwerte](./assets/swatch-hex-values.png){width="400"}

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Öffnen Sie im Raster die _color_ -Attribut im Bearbeitungsmodus.

1. Stellen Sie sicher, dass **[!UICONTROL Catalog Input Type for Store Owner]** auf `Visual Swatch`.

1. Wenn Sie es vorziehen, keine entsprechenden einfachen Produktbilder anzuzeigen, wenn das Muster auf der Produktansichtsseite ausgewählt ist, legen Sie **[!UICONTROL Update Product Preview Image]** nach `No`.

1. under _[!UICONTROL Manage Swatch (Values of Your Attribute)]_klicken **[!UICONTROL Add Swatch]**und gehen Sie wie folgt vor:

   ![Verwalten von Musterwerten](./assets/attribute-color-manage-swatch-values.png){width="600" zoomable="yes"}

   - Im _Muster_ klicken Sie auf das neue Muster und wählen Sie **[!UICONTROL Choose a color]** aus dem Menü.

     ![Auswählen einer Musterfarbe](./assets/attribute-color-swatch-menu.png){width="500" zoomable="yes"}

   - Platzieren Sie den Cursor in der Farbauswahl im **#** den aktuellen Wert löschen und den sechstelligen Hexadezimalwert der neuen Farbe eingeben.

     ![Hexadezimalwert eingeben](./assets/attribute-swatch-color-picker-hex-value.png){width="500" zoomable="yes"}

   - Um das Muster zu speichern, klicken Sie auf die Schaltfläche _Farbrad_ ( ![Farbsymbol](../assets/icon-color-wheel.png) ) in der rechten unteren Ecke der Farbauswahl.

   - Im _Admin_ geben Sie einen Titel ein, um die Farbe für den Store-Administrator zu beschreiben.

     Falls zutreffend, können Sie auch die Übersetzung der Farbe für jede unterstützte Sprache eingeben. Im folgenden Beispiel wird die SKU als Referenz in die _Admin_ -Beschriftung, da die Farben nur für ein bestimmtes Produkt verwendet werden. Sie können ein Leerzeichen oder einen Unterstrich in die Beschriftung einfügen, aber keinen Bindestrich.

   - Im _Ist Standard_ auswählen, wählen Sie die Standardoption für das Muster aus.

   - Um die Reihenfolge der Farbmuster zu ändern, klicken Sie auf die Schaltfläche _[!UICONTROL Order]_![Symbol &quot;Sortierung&quot;](../assets/icon-sort-order.png) und ziehen Sie das Element an eine neue Position in der Liste.

     ![Musterbezeichnungen](./assets/attribute-swatch-labels.png){width="400"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Attribute]** und aktualisieren Sie den Cache bei Aufforderung.

1. Öffnen Sie jedes Produkt im Bearbeitungsmodus und aktualisieren Sie die **Farbe** -Attribut mit dem richtigen Farbfeld.

   Gehen Sie wie folgt vor, um mehrere Produkte gleichzeitig zu aktualisieren.

#### Methode 2: Hochladen eines Musterbilds

1. Um ein Bild für ein Muster zu erfassen, öffnen Sie das Produktbild in einem Fotoeditor und speichern Sie einen quadratischen Bereich des Bildes, der die Farbe, das Muster oder die Textur darstellt.

   Bei Bedarf können Sie diese Aktion für jede Produktvariante wiederholen.

   Die Größe und Abmessungen des Musters werden durch das Design bestimmt. Im Allgemeinen trägt das Speichern eines Bildes als Quadrat dazu bei, das Seitenverhältnis eines Musters beizubehalten.

   ![Musterbilder](./assets/swatch-samples.png){width="400"}

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Öffnen Sie im Raster die **[!UICONTROL color]** -Attribut im Bearbeitungsmodus.

1. Stellen Sie sicher, dass **[!UICONTROL Catalog Input Type for Store Owner]** auf `Visual Swatch`.

1. Wenn Sie es vorziehen, keine entsprechenden einfachen Produktbilder anzuzeigen, wenn das Muster auf der Produktansichtsseite ausgewählt ist, legen Sie **[!UICONTROL Update Product Preview Image]** nach `No`.

1. under _[!UICONTROL Manage Swatch]_(Werte Ihres Attributs), klicken Sie auf **[!UICONTROL Add Swatch]**und gehen Sie wie folgt vor:

   - Im _[!UICONTROL Swatch]_klicken Sie auf das neue Muster, um das Menü anzuzeigen und **[!UICONTROL Upload a file]**.

   - Navigieren Sie zu der von Ihnen vorbereiteten Musterdatei und wählen Sie die hochzuladende Datei aus.

   - Wiederholen Sie diese Schritte für jedes Musterbild.

   - Geben Sie die Titel für Admin und Storefront ein.

     In diesem Beispiel wird die SKU zur Referenz in die Admin-Beschriftung aufgenommen, da diese Farben nur für ein bestimmtes Produkt verwendet werden. Sie können ein Leerzeichen oder einen Unterstrich in die Beschriftung einfügen, aber keine Bindestriche einfügen.

     ![Titel eingeben](./assets/swatch-upload.png){width="500" zoomable="yes"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Attribute]** und aktualisieren Sie den Cache bei Aufforderung.

1. Öffnen Sie jedes Produkt im Bearbeitungsmodus und aktualisieren Sie die **[!UICONTROL Color]** -Attribut mit dem richtigen Farbfeld.

   Gehen Sie wie folgt vor, um mehrere Produkte gleichzeitig zu aktualisieren.

### Schritt 2: Aktualisieren der Produkte

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Verwenden Sie die **[!UICONTROL Filter]** , um die Liste nach Name oder SKU anzuzeigen und nur die entsprechenden Produkte einzuschließen.

1. Aktivieren Sie im Raster das Kontrollkästchen jedes Produkts, für das das Muster gilt.

1. Satz **[!UICONTROL Actions]** nach `Update Attributes`.

   In diesem Beispiel werden alle blauen Einstellungen der Hosen ausgewählt.

   ![Aktualisieren von Produktmuster-Attributen](./assets/swatch-apply-update-attributes.png){width="600" zoomable="yes"}

1. Scrollen Sie nach unten zum **[!UICONTROL Color]** und wählen Sie das **[!UICONTROL Change]** aktivieren.

   ![Kontrollkästchen &quot;Ändern&quot;](./assets/swatch-update-attributes-choose-color.png){width="400"}

1. Wählen Sie das für die ausgewählten Produkte zutreffende Muster aus und klicken Sie auf **[!UICONTROL Save]**.

1. Wenn Sie dazu aufgefordert werden, aktualisieren Sie den Cache.

   ![Muster in werden im Storefront angezeigt](./assets/swatch-blue-schmear.png){width="200"}

## Hinzufügen von Farbfeldern zu einem einfachen Produkt

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Öffnen Sie ein Produkt im Bearbeitungsmodus und überprüfen Sie den Produktstatus (sollte aktiviert sein).

1. Klicks **[!UICONTROL Create Configurations]** -Schaltfläche (unter der `Configurations` Registerkarte).

1. Wählen Sie im Popup-Fenster das Attribut Farbe und **[!UICONTROL Next]**.

1. Wählen Sie Farbmuster aus dem Attribut aus, das Sie in dieses Produkt aufnehmen möchten.

1. Klicken Sie in der Fortschrittsleiste auf **[!UICONTROL Next]**.

1. [Bilder, Preise und Menge konfigurieren](product-create-configurable.md#step-3-configure-the-images-price-and-quantity).

   Legen Sie in diesem Schritt die Bilder, Preise und Menge jeder Konfiguration fest. Die verfügbaren Optionen sind für jede Option identisch und Sie können nur eine auswählen. Sie können dieselbe Einstellung auf alle SKUs anwenden, eine eindeutige Einstellung auf jede SKU anwenden oder die Einstellungen vorerst überspringen.

1. Klicken Sie nach Abschluss der Konfiguration für Bilder, Preise und Menge auf **[!UICONTROL Next]** in der oberen rechten Ecke.

   Die aktuellen Produktvarianten werden unten im Abschnitt Konfiguration angezeigt. Wenn Sie mit den Konfigurationen zufrieden sind, klicken Sie auf **[!UICONTROL Generate Products]**.
