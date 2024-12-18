---
title: Verwalten von Produktbildern und Videos
description: Erfahren Sie mehr über die Verwaltung von Bild- und Video-Assets für Ihre Produktlisten.
exl-id: 3cb4ab8a-8966-400f-be94-a517634d1334
feature: Catalog Management, Products, Media
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1025'
ht-degree: 0%

---

# Verwalten von Produktbildern und Videos

Für jedes Produkt können Sie mehrere Bilder und Videos hochladen, ihre Reihenfolge neu anordnen und steuern, wie sie verwendet werden. Wenn Sie eine große Anzahl von Bildern verwalten müssen, empfiehlt es sich möglicherweise, die Bilder als Batch zu importieren, anstatt sie einzeln hochzuladen. Weitere Informationen finden Sie unter [Produktbilder importieren](../systems/data-import-product-images.md).

Wenn Sie große Bilder für die Anzeige auf der _[!UICONTROL Product Details]_hochladen möchten, sollten Sie eine maximale Pixelgröße (Breite und Höhe) festlegen und die Größe der Dateien beim Hochladen automatisch ändern. Es gibt eine Option, um die automatische Größenanpassung größerer Bilddateien beim Hochladen zu aktivieren. Weitere Informationen finden Sie unter [Größenänderung von Produktbildern](product-image-config.md#product-image-resizing).

## Aktualisieren der Produktbilder

1. Öffnen Sie das Produkt im Bearbeitungsmodus.

1. Um mit einer bestimmten Store-Ansicht zu arbeiten, legen Sie die **[!UICONTROL Store View]** in der linken oberen Ecke auf die entsprechende Ansicht fest.

   >[!NOTE]
   >
   >Neue Produktbilder werden **_immer_** hochgeladen und in **_allen_**-Ansichten angezeigt, auch wenn der `All Store Views` nicht für den Upload verwendet wird. <br/><br/>Um ein Produktbild in einer bestimmten Shop-Ansicht auszublenden, müssen Sie zu dieser Shop-Ansicht wechseln, das **[!UICONTROL Hide from Product Page]** für das Bild aktivieren und auf **[!UICONTROL Save]** klicken.

1. Scrollen Sie nach unten und erweitern Sie den Abschnitt _[!UICONTROL Images and Videos]_.

### Bild hochladen

Aus Gründen der Kompatibilität wird empfohlen, alle Produktbilder mit dem `sRGB` Farbprofil hochzuladen. Alle anderen Farbprofile werden beim Hochladen des Produktbilds automatisch in das `sRGB` Farbprofil konvertiert, was zu Farbinkonsistenzen im hochgeladenen Bild führen kann.

Die Länge des Bilddateinamens, einschließlich Erweiterung, darf 90 Zeichen nicht überschreiten.

Führen Sie einen der folgenden Schritte aus, um ein Bild hochzuladen:

- Ziehen Sie ein Bild von Ihrem Desktop und legen Sie es auf der Kachel _Kamera_ ( ![Kamerasymbol](../assets/icon-camera.png) ) im _[!UICONTROL Images And Videos]_ab.

- Klicken Sie im _[!UICONTROL Images And Videos]_auf die Kachel_ Kamera _( ![Kamerasymbol](../assets/icon-camera.png) ), wählen Sie die Bilddatei auf Ihrem Computer aus und klicken Sie auf **[!UICONTROL Open]**.

  ![Hochladen oder Drag-and-Drop](./assets/product-images-and-video-jewel-tee.png){width="600" zoomable="yes"}

### Bilder neu anordnen

Um die Reihenfolge der Bilder in der Galerie zu ändern, klicken Sie auf das _[!UICONTROL Sort]_( ![Sortiersymbol](./assets/inventory-icon-sort.png) ) unten auf der Bildkachel und ziehen Sie das Bild an eine andere Position im_[!UICONTROL Images And Videos]_.

![Änderungsanforderung](./assets/product-images-and-videos-drag.png){width="600" zoomable="yes"}

### Löschen eines Bildes

Um ein Bild aus der Galerie zu entfernen, klicken Sie auf das **[!UICONTROL Delete]**-Symbol ![Papierkorb](../assets/icon-delete-trashcan.png) ) in der oberen rechten Ecke der Bildkachel und klicken Sie auf **[!UICONTROL Save]**.

### Festlegen von Bilddetails

Klicken Sie auf das Bild, das Sie in der Detailansicht öffnen möchten, und führen Sie einen der folgenden Schritte aus:

![Bilddetailansicht](./assets/product-image-detail-jewel-tee.png){width="600" zoomable="yes"}

Um die Detailansicht zu schließen, klicken Sie auf _Schließen_ ( ![Schließen-Symbol](../assets/icon-close-x.png) ) oben rechts.

Klicken Sie abschließend auf **[!UICONTROL Save]**.

#### Alten Text eingeben

Bild-Alternativtext wird von Sprachausgaben referenziert, um die Barrierefreiheit im Web zu verbessern, und von Suchmaschinen beim Indizieren der Site. In einigen Browsern wird beim Bewegen des Mauszeigers der ALT-Text angezeigt. Alternativtext kann mehrere Wörter lang sein und sorgfältig ausgewählte Schlüsselwörter enthalten.

Geben Sie im _[!UICONTROL Alt Text]_eine kurze Beschreibung des Bildes ein.

#### Rollen zuweisen

Standardmäßig sind alle Rollen dem ersten Bild zugewiesen, das in das Produkt hochgeladen wird. Gehen Sie wie folgt vor, um einem anderen Bild eine Rolle zuzuweisen:

Wählen Sie im _[!UICONTROL Role]_die Rolle aus, die Sie dem Bild zuweisen möchten.

Wenn Sie zum Abschnitt _Bilder und Videos_ zurückkehren, werden die aktuell zugewiesenen Rollen unter den einzelnen Bildern angezeigt.

![Zugewiesene Rollen](./assets/product-images-video-swatch.png){width="600" zoomable="yes"}

#### Bild ausblenden

Um ein Bild aus dem Miniaturbildkatalog auszuschließen, aktivieren Sie das Kontrollkästchen **[!UICONTROL Hidden]** und klicken Sie auf **[!UICONTROL Save]**.

![Ausgeblendete Bilder](./assets/product-images-and-videos-hidden.png){width="600" zoomable="yes"}

## Bildrollen

| Image Role | Beschreibung |
|--- |--- |
| [!UICONTROL Thumbnail] | Miniaturbilder werden in der Miniaturbildgalerie, im Warenkorb und in einigen Blöcken, z. B. „Zugehörige Elemente“, angezeigt. Beispielgröße: 50 x 50 Pixel |
| [!UICONTROL Small Image] | Das kleine Bild wird für die Produktbilder in den Listeneinträgen auf den Kategorie- und Suchergebnisseiten und zur Anzeige der Produktbilder verwendet, die für Abschnitte wie für Upsell, Crosssell und die Liste für neue Produkte benötigt werden. Beispielgröße: 470 x 470 Pixel |
| [!UICONTROL Base Image] | Das Basisbild ist das Hauptbild auf der Produktdetailseite. Der Bildzoom ist aktiviert, wenn Sie ein Bild hochladen, das größer ist als der Bild-Container. Je nach dem gewünschten Zoom sollte das Basisbild zwei- oder dreimal so groß wie der Container sein. Beispielgrößen: 470 x 470 Pixel (ohne Zoom), 1100 x 1100 Pixel (mit Zoom) |
| [!UICONTROL Swatch] | Ein [Muster](swatches.md) kann verwendet werden, um die Farbe, das Muster oder die Textur zu veranschaulichen. Beispielgröße: 50 x 50 Pixel |

{style="table-layout:auto"}

## Wasserzeichen

Wenn Sie Ihre eigenen Originalproduktbilder erstellen müssen, können Sie nicht viel tun, um skrupellose Konkurrenten daran zu hindern, sie mit einem Mausklick zu stehlen. Sie können sie jedoch zu einem weniger attraktiven Ziel machen, indem Sie ein Wasserzeichen auf jedem Bild platzieren, um sie als Ihre Eigenschaft zu identifizieren. Eine Wasserzeichendatei kann entweder ein JPG- (JPEG), GIF- oder PNG-Bild sein. Sowohl GIF- als auch PNG-Dateitypen unterstützen transparente Ebenen, die verwendet werden können, um dem Wasserzeichen einen transparenten Hintergrund zu verleihen.

Das im folgenden Beispiel für das _kleine_ Bild verwendete Wasserzeichen ist ein schwarzes Logo mit transparentem Hintergrund, das als PNG-Datei mit den folgenden Einstellungen gespeichert wird:

- Größe: 50x50
- Deckkraft: 5
- Position: Kachel

![Gekacheltes Wasserzeichen](./assets/storefront-watermark-tiled.png){width="700" zoomable="yes"}

### Hinzufügen von Wasserzeichen zu Produktbildern

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

   Weitere Informationen zu Design-Konfigurationen finden Sie unter [Design-Konfiguration](../content-design/configuration.md).

1. Suchen Sie die Store-Ansicht, die Sie konfigurieren möchten, und klicken Sie in der Spalte _[!UICONTROL Action]_auf **[!UICONTROL Edit]**.

1. Erweitern Sie unter _[!UICONTROL Other Settings]_![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Product Image Watermarks]**.

   ![Produktbild-Wasserzeichen - Basis](./assets/config-design-product-image-watermarks-base.png){width="600" zoomable="yes"}

   Die Bildeinstellungen für **[!UICONTROL Base]**, **[!UICONTROL Thumbnail]**, **[!UICONTROL Small]** und **[!UICONTROL Swatch Image]** sind identisch.

1. Verwenden Sie eine der folgenden Methoden, um das Wasserzeichenbild-Asset hinzuzufügen:

   - Klicken Sie auf **[!UICONTROL Upload]** und wählen Sie die Bilddatei auf Ihrem System aus, die Sie zur Verwendung als Wasserzeichen hochladen möchten.
   - Klicken Sie auf **[!UICONTROL Select from Gallery]** und wählen Sie ein Bild-Asset aus der [Mediensammlung](../content-design/media-gallery.md).

1. Vervollständigen Sie die Einstellungen für die Wasserzeichenanzeige:

   - Geben Sie die **[!UICONTROL Image Opacity]** als Prozentsatz ein. Beispiel: `40`

   - Geben Sie die **[!UICONTROL Image Size]** in Pixeln an. Beispiel: `200 x 200`

   - Legen Sie **[!UICONTROL Image Position]** fest, um zu bestimmen, wo das Wasserzeichen angezeigt wird.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

1. Wenn Sie aufgefordert werden, den Cache zu aktualisieren, klicken Sie in der Systemmeldung auf **[!UICONTROL Cache Management]** und aktualisieren Sie den ungültigen Cache.

   ![Cache aktualisieren](./assets/msg-cache-management.png){width="600" zoomable="yes"}

>[!TIP]
>
>Sie können auf **[!UICONTROL Use Default Value]** Pfeiltaste ![Zurück](../assets/icon-arrow-return.png) klicken, um den Standardwert wiederherzustellen.

### Wasserzeichen löschen

1. Klicken Sie unten links im Bild auf das **[!UICONTROL Delete]** ( ![Papierkorb-Symbol](../assets/icon-delete-trashcan-solid.png) ).

   ![Wasserzeichen löschen](./assets/product-image-watermark-delete.png){width="300"}

1. Klicken Sie auf **[!UICONTROL Save Config]**.

1. Wenn Sie aufgefordert werden, den Cache zu aktualisieren, klicken Sie in der Systemmeldung auf **[!UICONTROL Cache Management]** und aktualisieren Sie den ungültigen Cache.

   Wenn das Wasserzeichenbild in der Storefront erhalten bleibt, kehren Sie zur Cache-Verwaltung zurück und klicken Sie auf **[!UICONTROL Flush Magento Cache]**.
