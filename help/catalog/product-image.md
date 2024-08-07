---
title: Produktbilder und Videos verwalten
description: Erfahren Sie mehr über die Verwaltung von Bild- und Video-Assets für Ihre Produktlisten.
exl-id: 3cb4ab8a-8966-400f-be94-a517634d1334
feature: Catalog Management, Products, Media
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1025'
ht-degree: 0%

---

# Produktbilder und Videos verwalten

Für jedes Produkt können Sie mehrere Bilder und Videos hochladen, die Reihenfolge neu anordnen und steuern, wie die einzelnen Bilder verwendet werden. Wenn Sie eine große Anzahl von Bildern verwalten müssen, sollten Sie sie möglicherweise als Batch importieren, anstatt jeden einzelnen hochzuladen. Weitere Informationen finden Sie unter [Importieren von Produktbildern](../systems/data-import-product-images.md).

Wenn Sie große Bilder für die Anzeige auf der Seite _[!UICONTROL Product Details]_hochladen möchten, sollten Sie in Erwägung ziehen, eine maximale Pixelgröße (Breite und Höhe) festzulegen und die Größe der Dateien beim Hochladen automatisch zu ändern. Es gibt eine Option, um die automatische Größenanpassung größerer Bilddateien beim Hochladen zu aktivieren. Weitere Informationen finden Sie unter [Größenanpassung des Produktbilds](product-image-config.md#product-image-resizing).

## Aktualisieren der Produktbilder

1. Öffnen Sie das Produkt im Bearbeitungsmodus.

1. Um mit einer bestimmten Store-Ansicht zu arbeiten, legen Sie die Auswahl **[!UICONTROL Store View]** in der linken oberen Ecke auf die entsprechende Ansicht fest.

   >[!NOTE]
   >
   >Neue Produktbilder werden **_immer_** hochgeladen und in **_allen_** Store-Ansichten angezeigt, selbst wenn der Gültigkeitsbereich `All Store Views` nicht für den Upload verwendet wird. <br/><br/>Um ein Produktbild aus einer bestimmten Store-Ansicht auszublenden, müssen Sie zu dieser Store-Ansicht wechseln, das Kontrollkästchen **[!UICONTROL Hide from Product Page]** für das Bild aktivieren und auf **[!UICONTROL Save]** klicken.

1. Scrollen Sie nach unten und erweitern Sie den Abschnitt _[!UICONTROL Images and Videos]_.

### Bild hochladen

Für eine optimale Kompatibilität wird empfohlen, alle Produktbilder mit dem Farbprofil `sRGB` hochzuladen. Alle anderen Farbprofile werden beim Hochladen des Produktbilds automatisch in das Farbprofil `sRGB` konvertiert, was zu Farbinkonsistenzen im hochgeladenen Bild führen kann.

Die Länge des Bilddateinamens einschließlich der Erweiterung darf 90 Zeichen nicht überschreiten.

Führen Sie einen der folgenden Schritte aus, um ein Bild hochzuladen:

- Ziehen Sie ein Bild von Ihrem Desktop und legen Sie es auf der Kachel _Kamera_ ( ![Kamerasymbol](../assets/icon-camera.png) ) im Feld _[!UICONTROL Images And Videos]_ab.

- Klicken Sie im Feld _[!UICONTROL Images And Videos]_auf die Kachel_ Kamera _( ![Kamerasymbol](../assets/icon-camera.png) ), wählen Sie die Bilddatei auf Ihrem Computer aus und klicken Sie auf **[!UICONTROL Open]**.

  ![Hochladen oder Ziehen und Ablegen](./assets/product-images-and-video-jewel-tee.png){width="600" zoomable="yes"}

### Bilder neu anordnen

Um die Reihenfolge der Bilder in der Galerie zu ändern, klicken Sie auf das Symbol _[!UICONTROL Sort]_( ![Sortiersymbol](./assets/inventory-icon-sort.png) ) am unteren Rand der Bildkachel und ziehen Sie das Bild an eine andere Position im Feld_[!UICONTROL Images And Videos]_.

![Reihenfolge ändern](./assets/product-images-and-videos-drag.png){width="600" zoomable="yes"}

### Löschen eines Bildes

Um ein Bild aus der Galerie zu entfernen, klicken Sie auf das Symbol **[!UICONTROL Delete]** ( ![Papierkorbsymbol](../assets/icon-delete-trashcan.png) ) oben rechts in der Bildkachel und klicken Sie auf **[!UICONTROL Save]**.

### Festlegen von Bilddetails

Klicken Sie auf das Bild, das Sie in der Detailansicht öffnen möchten, und führen Sie einen der folgenden Schritte aus:

![Bilddetailansicht](./assets/product-image-detail-jewel-tee.png){width="600" zoomable="yes"}

Um die Detailansicht zu schließen, klicken Sie oben rechts auf das Symbol _Schließen_ ( ![Symbol Schließen](../assets/icon-close-x.png) ).

Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]**.

#### ALT-Text eingeben

Bild Alternativer Text wird von Bildschirmlesehilfen zur Verbesserung der Web-Zugänglichkeit und von Suchmaschinen bei der Indizierung der Site referenziert. In einigen Browsern wird der Alt-Text beim Bewegen des Mauszeigers angezeigt. Alternativtext kann mehrere Wörter lang sein und sorgfältig ausgewählte Schlüsselwörter enthalten.

Geben Sie im Feld _[!UICONTROL Alt Text]_eine kurze Beschreibung des Bildes ein.

#### Rollen zuweisen

Standardmäßig werden alle Rollen dem ersten Bild zugewiesen, das in das Produkt hochgeladen wird. Gehen Sie wie folgt vor, um eine Rolle einem anderen Bild zuzuweisen:

Wählen Sie im Feld _[!UICONTROL Role]_die Rolle aus, die Sie dem Bild zuweisen möchten.

Wenn Sie zum Abschnitt _Bilder und Videos_ zurückkehren, werden die derzeit zugewiesenen Rollen unter jedem Bild angezeigt.

![Zugewiesene Rollen](./assets/product-images-video-swatch.png){width="600" zoomable="yes"}

#### Bild ausblenden

Um ein Bild aus der Miniaturansicht auszuschließen, aktivieren Sie das Kontrollkästchen **[!UICONTROL Hidden]** und klicken Sie auf **[!UICONTROL Save]**.

![Ausgeblendete Bilder](./assets/product-images-and-videos-hidden.png){width="600" zoomable="yes"}

## Bildrollen

| Bildrolle | Beschreibung |
|--- |--- |
| [!UICONTROL Thumbnail] | Miniaturansichten werden in der Miniaturansichten-Galerie, im Warenkorb und in einigen Blöcken wie z. B. verwandten Artikeln angezeigt. Beispielgröße: 50 x 50 Pixel |
| [!UICONTROL Small Image] | Das kleine Bild wird für die Produktbilder in Listen auf Kategorie- und Suchergebnisseiten verwendet, um die Produktbilder anzuzeigen, die für Abschnitte wie Up-Sells, Cross-Sells und die Liste &quot;Neue Produkte&quot;benötigt werden. Beispielgröße: 470 x 470 Pixel |
| [!UICONTROL Base Image] | Das Basisbild ist das Hauptbild auf der Produktdetailseite. Der Bildzoom wird aktiviert, wenn Sie ein Bild hochladen, das größer als der Bildcontainer ist. Je nach dem Zoomgrad, den Sie erreichen möchten, sollte das Basisbild die Zwei- oder Dreifache der Größe des Containers betragen. Beispielgrößen: 470 x 470 Pixel (ohne Zoom), 1100 x 1100 Pixel (mit Zoom) |
| [!UICONTROL Swatch] | Ein [Muster](swatches.md) kann verwendet werden, um die Farbe, das Muster oder die Textur zu illustrieren. Beispielgröße: 50 x 50 Pixel |

{style="table-layout:auto"}

## Wasserzeichen

Wenn Sie auf Kosten der Erstellung Ihrer eigenen Originalproduktbilder gehen, können Sie nicht viel tun, um zu verhindern, dass skrupellose Konkurrenten sie mit dem Mausklick stehlen. Sie können sie jedoch zu einem weniger attraktiven Ziel machen, indem Sie ein Wasserzeichen auf jedem Bild platzieren, um sie als Ihre Eigenschaft zu identifizieren. Eine Wasserzeichendatei kann entweder ein JPG (JPEG), GIF oder ein PNG-Bild sein. Sowohl GIF- als auch PNG-Dateitypen unterstützen transparente Ebenen, mit denen das Wasserzeichen einen transparenten Hintergrund erhält.

Das im folgenden Beispiel für das Bild _klein_ verwendete Wasserzeichen ist ein schwarzes Logo mit transparentem Hintergrund und wird als PNG-Datei mit den folgenden Einstellungen gespeichert:

- Größe: 50x50
- Deckkraft: 5
- Position: Kachel

![Wasserzeichen mit verschachtelten Zeichen](./assets/storefront-watermark-tiled.png){width="700" zoomable="yes"}

### Hinzufügen von Wasserzeichen zu Produktbildern

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

   Weitere Informationen zu Designkonfigurationen finden Sie unter [Designkonfiguration](../content-design/configuration.md).

1. Suchen Sie die Store-Ansicht, die Sie konfigurieren möchten, und klicken Sie in der Spalte _[!UICONTROL Action]_auf **[!UICONTROL Edit]**.

1. Erweitern Sie unter _[!UICONTROL Other Settings]_den Abschnitt ![Erweiterungsauswahl](../assets/icon-display-expand.png) um den Abschnitt **[!UICONTROL Product Image Watermarks]**.

   ![Produktbild-Wasserzeichen - Base](./assets/config-design-product-image-watermarks-base.png){width="600" zoomable="yes"}

   Die Bildeinstellungen **[!UICONTROL Base]**, **[!UICONTROL Thumbnail]**, **[!UICONTROL Small]** und **[!UICONTROL Swatch Image]** sind identisch.

1. Verwenden Sie eine der folgenden Methoden, um das Bild-Asset des Wasserzeichens hinzuzufügen:

   - Klicken Sie auf **[!UICONTROL Upload]** und wählen Sie die Bilddatei auf Ihrem System aus, die Sie zur Verwendung als Wasserzeichen hochladen möchten.
   - Klicken Sie auf **[!UICONTROL Select from Gallery]** und wählen Sie ein Bild-Asset aus der [Mediengalerie](../content-design/media-gallery.md) aus.

1. Füllen Sie die Einstellungen für die Wasserzeichenanzeige aus:

   - Geben Sie den Wert **[!UICONTROL Image Opacity]** als Prozentsatz ein. Beispiel: `40`

   - Geben Sie den Wert **[!UICONTROL Image Size]** in Pixel ein. Beispiel: `200 x 200`

   - Legen Sie **[!UICONTROL Image Position]** fest, um zu bestimmen, wo das Wasserzeichen angezeigt wird.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

1. Wenn Sie aufgefordert werden, den Cache zu aktualisieren, klicken Sie in der Systemmeldung auf &quot;**[!UICONTROL Cache Management]**&quot; und aktualisieren Sie den ungültigen Cache.

   ![Cache aktualisieren](./assets/msg-cache-management.png){width="600" zoomable="yes"}

>[!TIP]
>
>Sie können auf **[!UICONTROL Use Default Value]** ![Pfeil return](../assets/icon-arrow-return.png) klicken, um den Standardwert wiederherzustellen.

### Wasserzeichen löschen

1. Klicken Sie in der linken unteren Ecke des Bildes auf das Symbol **[!UICONTROL Delete]** ( ![Papierkorbsymbol](../assets/icon-delete-trashcan-solid.png) ).

   ![Wasserzeichen löschen](./assets/product-image-watermark-delete.png){width="300"}

1. Klicken Sie auf **[!UICONTROL Save Config]**.

1. Wenn Sie aufgefordert werden, den Cache zu aktualisieren, klicken Sie in der Systemmeldung auf &quot;**[!UICONTROL Cache Management]**&quot; und aktualisieren Sie den ungültigen Cache.

   Wenn das Wasserzeichenbild in der Storefront erhalten bleibt, kehren Sie zur Cacheverwaltung zurück und klicken Sie auf **[!UICONTROL Flush Magento Cache]**.
