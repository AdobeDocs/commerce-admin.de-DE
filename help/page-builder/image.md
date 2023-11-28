---
title: Medien - Bild
description: Erfahren Sie mehr über den Bildinhaltstyp, mit dem ein JPG-, GIF- oder PNG-Bild zum [!DNL Page Builder] Bühne.
exl-id: 1b8d906e-7570-4c1f-87a0-992400faf55c
feature: Page Builder, Page Content
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '1551'
ht-degree: 0%

---

# Medien - Bild

Verwenden Sie die _Bild_ Inhaltstyp zum Hinzufügen eines JPG-, GIF- oder PNG-Bildes zum [[!DNL Page Builder] Schritt](workspace.md#stage). Zusätzlich zum standardmäßigen Desktop-Bild können Sie ein sekundäres Bild für Mobilgeräte angeben. Sie können auch eine Beschriftung hinzufügen, die unter dem Bild angezeigt wird, und das Bild mit einer URL, einem Produkt, einer Kategorie oder einer Seite verknüpfen.

>[!TIP]
>
>Sie können die [Adobe Stock-Integration](../content-design/adobe-stock.md) , um ein geeignetes Asset aus den Millionen von [Adobe Stock](https://stock.adobe.com). Siehe [Verwenden von Adobe Stock-Bildern](../content-design/adobe-stock-manage.md) Weitere Informationen zum Suchen, Verfeinern und Speichern von Adobe Stock-Assets in Ihrer Galerie.

{{$include /help/_includes/page-builder-save-timeout.md}}

## Bild-Toolbox

Die Bild-Toolbox wird angezeigt, wenn Sie den Mauszeiger über den Bildcontainer bewegen.

![Bild-Toolbox](./assets/pb-media-image-giftcard-column-toolbox.png){width="500" zoomable="yes"}

| Tool | Symbol | Beschreibung |
|--- |--- |--- |
| Verschieben | ![Symbol Verschieben](./assets/pb-icon-move.png){width="25"} | Verschiebt das Bild an eine andere Position auf der Bühne. |
| (Titel) | Bild | Identifiziert den aktuellen Inhalts-Container als Bild. Bewegen Sie den Mauszeiger über den Bildcontainer, um die Toolbox anzuzeigen. |
| Einstellungen | ![Symbol Einstellungen](./assets/pb-icon-settings.png){width="25"} | Öffnet die _Bild bearbeiten_ Seite, auf der Sie die Eigenschaften des Bildes und Containers ändern können. |
| Ausblenden | ![Symbol &quot;Ausblenden&quot;](./assets/pb-icon-hide.png){width="25"} | Blendet das aktuelle Bild aus. |
| Anzeigen | ![Symbol &quot;Anzeigen&quot;](./assets/pb-icon-show.png){width="25"} | Zeigt das ausgeblendete Bild an. |
| Duplizieren | ![Symbol &quot;Duplizieren&quot;](./assets/pb-icon-duplicate.png){width="25"} | Kopiert das Bild. |
| Entfernen | ![Symbol &quot;Entfernen&quot;](./assets/pb-icon-remove.png){width="25"} | Löscht das Bild aus der Bühne. |
| Neues Bild hochladen |  | Lädt ein Bild aus Ihrem lokalen Dateisystem in die Galerie hoch. |
| Aus Galerie auswählen |  | Auswahl eines vorhandenen Bildes aus der Galerie. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Bild hinzufügen

1. Im [!DNL Page Builder] Bedienfeld, erweitern **[!UICONTROL Media]** und ziehen Sie **[!UICONTROL Image]** Platzhalter zum Ziel-Container hinzu.

   Sie können ein Bild zu einer Zeile, Spalte oder Registerkarte hinzufügen. Im folgenden Beispiel wird das Bild in eine leere Spalte gezogen.

   ![Ziehen eines Bildinhaltstyps auf die Bühne](./assets/pb-media-image-drag.png){width="600" zoomable="yes"}

1. Verwenden Sie eine der folgenden Methoden, um das Bild-Asset hinzuzufügen:

   ![Bild hochladen oder aus Galerie-Tools auf der Bühne auswählen](./assets/pb-media-image-upload-select.png){width="500" zoomable="yes"}

   >[!NOTE]
   >
   >Die maximale Dateigröße beträgt 4 MB. Unterstützte Dateitypen sind JPG, GIF und PNG.

   - _**Neues Bild hochladen**_: Verwenden Sie diese Methode, um eine neue Bilddatei von Ihrem System hochzuladen.

      - Klicken **[!UICONTROL Upload Image]**.

      - Suchen Sie das Bild und wählen Sie es aus, um es der Galerie und dem Zielcontainer hinzuzufügen.

     Alternativ können Sie auch eine Bilddatei aus Ihrem System ziehen und auf der _Kamera_ ( ![Kamerasymbol](./assets/pb-icon-camera.png){width="20"} ).

   - _**Vorhandenes Asset auswählen**_: Verwenden Sie diese Methode, um ein vorhandenes Bild-Asset aus dem Medienspeicher/der Galerie auszuwählen.

      - Klicken **[!UICONTROL Select from Gallery]**.

      - Navigieren Sie mithilfe der Baumstruktur zum Bild.

      - Klicken Sie auf die Miniaturansicht und klicken Sie auf **[!UICONTROL Add Selected]**.

        ![Hinzufügen eines ausgewählten Bildes](./assets/pb-media-image-gallery-add-selected.png){width="600" zoomable="yes"}

   - _**Adobe Stock-Bild suchen und auswählen**_: Verwenden Sie diese Methode, um ein Bild aus Adobe Stock zu suchen.

     >[!NOTE]
     >
     >Diese Methode erfordert eine [Adobe Stock-Integration](../content-design/adobe-stock.md) für Ihren Administrator konfiguriert.

      - Klicks **[!UICONTROL Search Adobe Stock]** und suchen Sie nach einem Bild.

      - Speichern Sie die Vorschau oder das lizenzierte Bild in der Galerie.

        Siehe [Verwenden von Adobe Stock-Bildern](../content-design/adobe-stock-manage.md) Weitere Informationen zum Arbeiten mit Adobe Stock-Assets.

      - Wählen Sie die Asset-Miniaturansicht in der Galerie aus und klicken Sie auf **[!UICONTROL Add Selected]**.

   Das Bild wird im Zielbehälter am Speicherort des Platzhalters angezeigt. Im Gegensatz zu einem Hintergrundbild können Sie das Bild an eine andere Position innerhalb des aktuellen Containers oder in einen anderen Container verschieben.

   >[!NOTE]
   >
   >Die [Banner](banner.md) und [Regler](slider.md) Content-Typen enthalten auch _Bild hochladen_ und _Aus Galerie auswählen_ Optionen zum Hinzufügen von Bildern.

   ![Bild in einer Spalte](./assets/pb-media-image-column1-giftcard.png){width="500" zoomable="yes"}

## Bildeinstellungen ändern

1. Bewegen Sie den Mauszeiger über den Bildcontainer, um das Tool-Feld anzuzeigen und die _Einstellungen_ (![Symbol Einstellungen](./assets/pb-icon-settings.png){width="20"} ).
Dateiname, Abmessungen und Dateigröße werden unter dem aktuellen Bild angezeigt.

   ![Aktuelles Bild](./assets/pb-media-image-settings-image.png){width="600" zoomable="yes"}

1. So ändern Sie die aktuelle **[!UICONTROL Image]** führen Sie einen der folgenden Schritte aus:

   - _**Neues Bild hochladen**_: Verwenden Sie diese Methode, um eine neue Bilddatei von Ihrem System hochzuladen.

      - Klicken **[!UICONTROL Upload Image]**.

      - Suchen Sie das Bild und wählen Sie es aus, um es der Galerie und dem Zielcontainer hinzuzufügen.

   - _**Vorhandenes Asset auswählen**_: Verwenden Sie diese Methode, um ein vorhandenes Bild-Asset aus dem Medienspeicher/der Galerie auszuwählen.

      - Klicken **[!UICONTROL Select from Gallery]**.

      - Navigieren Sie mithilfe der Baumstruktur zum Bild.

      - Klicken Sie auf die Miniaturansicht und klicken Sie auf **[!UICONTROL Add Selected]**.

        ![Hinzufügen eines ausgewählten Bildes](./assets/pb-media-image-gallery-add-selected.png){width="600" zoomable="yes"}

   - **Adobe Stock-Bild suchen und auswählen**: Verwenden Sie diese Methode, um ein Bild aus Adobe Stock zu suchen.

     >[!NOTE]
     >
     >Diese Methode erfordert eine [Adobe Stock-Integration](../content-design/adobe-stock.md) für Ihren Administrator konfiguriert.

      - Klicks **[!UICONTROL Search Adobe Stock]** und suchen Sie nach einem Bild.

      - Speichern Sie die Vorschau oder das lizenzierte Bild in der Galerie.

        Siehe [Verwenden von Adobe Stock-Bildern](../content-design/adobe-stock-manage.md) Weitere Informationen zum Arbeiten mit Adobe Stock-Assets.

      - Wählen Sie die Asset-Miniaturansicht in der Galerie aus und klicken Sie auf **[!UICONTROL Add Selected]**.

1. So fügen Sie eine **[!UICONTROL Mobile Image]** verwenden Sie dieselben Methoden wie im vorherigen Schritt beschrieben, um ein Bild auszuwählen, das für die Anzeige auf Mobilgeräten verwendet werden soll.

   ![Mobilgerät - Bild](./assets/pb-media-image-settings-mobile-image.png){width="600" zoomable="yes"}

1. Geben Sie bei Bedarf eine **[!UICONTROL Link]** für das Bild.

   Der Link ist die Zielseite, die angezeigt wird, wenn der Kunde auf das Bild klickt. Sie können einen von drei Linktypen verwenden:

   - **[!UICONTROL URL]** - Links zu einer relativen oder vollständig qualifizierten URL.

   - **[!UICONTROL Product]** - Identifiziert die Zielseite basierend auf dem Produktnamen oder der SKU. Suchen Sie nach dem Produkt anhand des Namens, der entweder auf einem Teil- oder einem vollständigen Namen basiert. Wählen Sie das Produkt aus der Liste der Suchergebnisse aus.

     ![Produkt auswählen, das verknüpft werden soll](./assets/pb-media-image-settings-image-link-product-results.png){width="600" zoomable="yes"}

   - **[!UICONTROL Category]** - Identifiziert die Zielseite als eine bestimmte Kategorie oder Unterkategorie im Kategoriebaum. Suchen Sie nach der Kategorie basierend auf einem Teil- oder Vollnamen. Wählen Sie die Kategorie aus dem erweiterten Bereich des angezeigten Baums aus.

     ![Zu verlinkende Kategorie auswählen](./assets/pb-media-image-settings-image-link-category-tree.png){width="600" zoomable="yes"}

   - **[!UICONTROL Page]** - Identifiziert die Zielseite als spezifische Inhaltsseite. Suchen Sie nach der Seite, die auf einem Teil- oder vollständigen Namen basiert. Wählen Sie die Seite aus der Liste der Suchergebnisse aus.

     ![Zu verlinkende Seite auswählen](./assets/pb-media-image-settings-image-link-page-results.png){width="600" zoomable="yes"}

   Wenn Sie verhindern möchten, dass der Besucher von Ihrem Store weg navigiert, wählen Sie die **[!UICONTROL Open in new tab]** aktivieren. Wenn das Kontrollkästchen deaktiviert wird, wird das verknüpfte Ziel in derselben Browser-Registerkarte geöffnet, wodurch der Besucher effektiv von Ihrem Store weg navigiert.

1. So fügen Sie eine **[!UICONTROL Image Caption]** eingeben, geben Sie den Text ein, der unter dem Bild angezeigt werden soll.

   Das Format der Beschriftung wird durch das Stylesheet bestimmt, das dem aktuellen Design zugeordnet ist.

   Die Beschriftung wird normalerweise unter dem Bild angezeigt und liefert Informationen über das Bild für Besucher und Suchmaschinen. Wenn Ihre Site in mehreren Sprachen verfügbar ist, können Sie dasselbe Bild verwenden, die Beschriftung jedoch übersetzen. In HTML wird die `<figcaption>` -Tag ist eine Untergruppe der `<figure>` -Tag. `<figcaption>This is the image caption</figcaption>`

1. Aktualisieren Sie die anderen Einstellungen nach Bedarf:

   - [Suchmaschinenoptimierung](#search-engine-optimization)
   - [Erweitert](#advanced)

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]** , um die Einstellungen anzuwenden und zum [!DNL Page Builder] Arbeitsbereich.

## Verschieben eines Bildes

1. Bewegen Sie den Mauszeiger über den Bildcontainer, um die Symbolleiste anzuzeigen und die _Verschieben_ (![Symbol Verschieben](./assets/pb-icon-move.png){width="20"} ).

   ![Verschieben eines Bildes](./assets/pb-media-image-column1-move-giftcard.png){width="500" zoomable="yes"}

1. Wählen Sie das Bild aus und ziehen Sie es an die neue Position, direkt unterhalb der roten Führungslinie.

   ![Positionieren des Bildes mithilfe der roten Führungslinie](./assets/pb-media-image-column2-move-giftcard-red-guideline.png){width="500" zoomable="yes"}

## Entfernen von Bildern

1. Bewegen Sie den Mauszeiger über den Bildcontainer, um die Symbolleiste anzuzeigen und die _Entfernen_ ( ![Symbol &quot;Entfernen&quot;](./assets/pb-icon-remove.png){width="20"} ).

1. Klicken Sie bei Aufforderung zur Bestätigung auf **[!UICONTROL OK]**.

## Suchmaschinenoptimierung

Text für diese Einstellungen ist für Suchmaschinen sichtbar und verbessert die Indexierung der Seite.

- Für **[!UICONTROL Alternative Text]**, geben Sie eine _alt_ Textbeschreibung für die anzuzeigenden Tools für die digitale Barrierefreiheit.

  Die Verwendung von Alternativtext ist eine Best Practice für Barrierefreiheit und ist in einigen Gebietsschemata gesetzlich vorgeschrieben. In HTML wird die `alt` -Attribut ist eine Untergruppe der `image` Tag: `<image title="tooltip" alt="description" src="image.jpg">`.

- Für **[!UICONTROL Title Attribute]** eingeben, geben Sie den Text ein, der beim Bewegen des Mauszeigers als QuickInfo angezeigt werden soll.

  Als Best Practice wird empfohlen, einen beschreibenden, schlüsselwortreichen Titel zu wählen, um die Indexierung des Bildes durch Suchmaschinen zu verbessern. In HTML wird die `title` -Attribut ist eine Untergruppe der `image` Tag: `<image title="tooltip" alt="description" src="image.jpg">`.

## [!UICONTROL Advanced]

- Um die horizontale Positionierung der Bilder zu steuern, die dem Container hinzugefügt werden, wählen Sie eine **[!UICONTROL Alignment]**.

  | Option | Beschreibung |
  | ------ | ----------- |
  | `Default` | Wendet die Standardeinstellung für die Ausrichtung an, die im Stylesheet des aktuellen Designs angegeben ist. |
  | `Left` | Richtet den Bildinhalt am linken Rand des Bildcontainers aus, wobei der angegebene Abstand berücksichtigt wird. |
  | `Center` | Richtet den Bildinhalt in der Mitte des Bildcontainers aus, wobei der angegebene Abstand berücksichtigt wird. |
  | `Right` | Richtet den Bildinhalt am rechten Rand des Bildcontainers aus, wobei der angegebene Abstand berücksichtigt wird. |

  {style="table-layout:auto"}

- Legen Sie die **[!UICONTROL Border]** Stil angewendet auf alle vier Seiten des Bild-Containers:

  | Option | Beschreibung |
  | ------ | ----------- |
  | `Default` | Wendet den standardmäßigen Randstil an, der vom zugehörigen Stylesheet angegeben wird. |
  | `None` | liefert keine sichtbare Anzeige der Containergrenzen. |
  | `Dotted` | Der Container-Rahmen wird als gepunktete Linie angezeigt. |
  | `Dashed` | Der Container-Rahmen wird als gestrichelte Linie angezeigt. |
  | `Solid` | Der Container-Rahmen wird als durchgehende Linie angezeigt. |
  | `Double` | Der Container-Rahmen wird als doppelte Linie angezeigt. |
  | `Groove` | Der Container-Rahmen wird als Rillenlinie angezeigt. |
  | `Ridge` | Der Container-Rahmen wird als gekürzte Linie angezeigt. |
  | `Inset` | Der Container-Rahmen wird als Inset-Zeile angezeigt. |
  | `Outset` | Der Container-Rahmen wird als Ausgangspunkt angezeigt. |

  {style="table-layout:auto"}

- Wenn Sie einen anderen Rahmenstil als `None`, füllen Sie die Randanzeigeoptionen aus:

  ![Rahmenfarbe](./assets/pb-settings-border-color.png){width="600" zoomable="yes"}

  | Option | Beschreibung |
  | ------ |------------ |
  | [!UICONTROL Border Color] | Geben Sie die Farbe an, indem Sie ein Muster auswählen, auf die Farbauswahl klicken oder einen gültigen Farbnamen oder einen entsprechenden Hexadezimalwert eingeben. |
  | [!UICONTROL Border Width] | Geben Sie die Anzahl Pixel für die Rahmenlinienbreite an. |
  | [!UICONTROL Border Radius] | Geben Sie die Anzahl der Pixel an, um die die Größe des Radius definiert wird, mit dem die einzelnen Ecken des Rands gerundet werden. |

  {style="table-layout:auto"}

- (Optional) Geben Sie die Namen von **[!UICONTROL CSS classes]** aus dem aktuellen Stylesheet, das auf den Bildcontainer angewendet werden soll.

  Trennen Sie mehrere Klassennamen durch ein Leerzeichen.

- Geben Sie Werte in Pixel für die **[!UICONTROL Margins and Padding]** um die äußeren Ränder und den inneren Abstand des Bildcontainers anzugeben.

  Geben Sie jeden entsprechenden Wert in das Bild-Container-Diagramm ein.

  | Container-Bereich | Beschreibung |
  | -------------- | ----------- |
  | [!UICONTROL Margins] | Die Menge an leerem Raum, die auf den äußeren Rand aller Seiten des Containers angewendet wird. |
  | [!UICONTROL Padding] | Die Menge an leerem Raum, die auf den inneren Rand aller Seiten des Containers angewendet wird. |

  {style="table-layout:auto"}
