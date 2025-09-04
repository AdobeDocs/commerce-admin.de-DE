---
title: Medien - Schieberegler
description: Erfahren Sie mehr über den Content-Typ „Regler“, mit dem Sie eine Diashow mit Bildern zur  [!DNL Page Builder]  hinzufügen.
exl-id: 757dbdc3-b146-4ef8-a17d-59f8da62626f
feature: Page Builder, Page Content
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '3810'
ht-degree: 0%

---

# Medien - Schieberegler

Verwenden Sie den _Regler_ Content-Typ, um eine Diashow von Bildern zur [[!DNL Page Builder] Bühne](workspace.md#stage) hinzuzufügen. Sie können neue Bilder hochladen oder vorhandene Bilder aus der Galerie oder dem Produktkatalog auswählen. Ein Schieberegler kann so eingestellt werden, dass er automatisch wiedergegeben wird, oder manuell mit Navigationstasten gesteuert werden. Informationen zum Verknüpfen des Schiebereglers mit einer bestimmten Promotion finden Sie unter [Dynamischer Block](dynamic-block.md).

![Medien-Schieberegler auf der Storefront](./assets/pb-media-slider-buy3-get1free-storefront.png){width="700" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Toolboxes

Beim Arbeiten mit dem Inhaltstyp „Regler“ können Sie einzelne Folien und den Regler-Container mit einer oder mehreren Folien hinzufügen und bearbeiten. Jede Folie verfügt über eine eigene Toolbox, mit der Sie Folien auf der [!DNL Page Builder] entwerfen können.

## Individuelle Folien-Toolbox

![Toolbox für einzelne Folien](./assets/pb-media-slider-toolbox-slide-row.png){width="500" zoomable="yes"}

| Tool | Symbol | Beschreibung |
|--- |--- |--- |
| Verschieben | ![move icon](./assets/pb-icon-move.png){width="25"} | Verschiebt den Schieber in eine andere Position auf dem Schieber. |
| (Bezeichnung) | Folie Nr | Identifiziert die Nummer der aktuellen Folie. |
| Einstellungen | ![Einstellungssymbol](./assets/pb-icon-settings.png){width="25"} | Öffnet die Seite _[!UICONTROL Edit Slide]_, auf der Sie die Eigenschaften der aktuellen Folie ändern können. |
| Duplikat | ![Symbol „Duplizieren“](./assets/pb-icon-duplicate.png){width="25"} | Erstellt eine Kopie der aktuellen Folie. |
| entfernen | ![Symbol entfernen](./assets/pb-icon-remove.png){width="25"} | Löscht die aktuelle Folie aus dem Schieberegler. |

{style="table-layout:auto"}

## Schieberegler-Toolbox

| Tool | Symbol | Beschreibung |
|--- |--- |--- |
| Verschieben | ![move icon](./assets/pb-icon-move.png){width="25"} | Verschiebt den Schieberegler in eine andere Position auf der Bühne. |
| (Bezeichnung) | [!UICONTROL Slider] | Identifiziert den Schieberegler-Container. |
| Einstellungen | ![Einstellungssymbol](./assets/pb-icon-settings.png){width="25"} | Öffnet die Seite _[!UICONTROL Edit Slider]_, auf der Sie die Eigenschaften des Videos und des Containers ändern können. |
| Ausblenden | ![Symbol ausblenden](./assets/pb-icon-hide.png){width="25"} | Blendet den aktuellen Schieberegler aus. |
| Anzeigen | ![Symbol anzeigen](./assets/pb-icon-show.png){width="25"} | Zeigt den ausgeblendeten Schieberegler an. |
| Duplikat | ![Symbol „Duplizieren“](./assets/pb-icon-duplicate.png){width="25"} | Erstellt eine Kopie des Schiebereglers. |
| entfernen | ![Symbol entfernen](./assets/pb-icon-remove.png){width="25"} | Löscht den Schieberegler aus der Bühne. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Hinzufügen einer einzelnen Folie

1. Öffnen Sie die Seite, den Block oder den dynamischen Block, in dem bzw. dem Sie den Schieberegler platzieren möchten, und erweitern Sie den **[!UICONTROL Content]**.

1. Erweitern Sie im [!DNL Page Builder] Bedienfeld **[!UICONTROL Media]** und ziehen Sie einen **[!UICONTROL Slider]** Platzhalter in eine Zeile, Spalte oder Registerkarte auf der Bühne.

   Im folgenden Beispiel ist die Hintergrundfarbe der Zeile gelb (`#fffd16`).

   ![Ziehen Sie den Schieberegler auf die Bühne](./assets/pb-media-slider-drag-row.png){width="600" zoomable="yes"}

   Der Schieberegler-Container wird auf der Bühne mit einer einzigen, leeren Folie angezeigt.

1. Klicken Sie in den Schieberegler-Container, um den [Texteditor](../content-design/editor.md) anzuzeigen, und geben Sie den Inhalt für die erste Folie ein.

   Sie können auch komplexere Bannerinhalte mit den Einstellungen [Inhalt](#content) einfügen.

1. Klicken Sie auf den Navigationspunkt am unteren Rand des Schiebereglers, um die Toolbox für die einzelne Folie anzuzeigen, und wählen Sie das Symbol _Einstellungen_ ( ![Einstellungen](./assets/pb-icon-settings.png){width="20"} ) aus.

   Schieberegler verfügen über zwei Werkzeugkästen. Stellen Sie sicher, dass Sie unten die Werkzeugkiste für Folien verwenden.

1. Füllen Sie die Einstellungen nach Bedarf entsprechend den folgenden Abschnitten aus:

   - [[!UICONTROL Appearance]](#appearance)
   - [[!UICONTROL Background]](#background)
   - [[!UICONTROL Content]](#content)
   - [[!UICONTROL Search Engine Optimization]](#seo)
   - [[!UICONTROL Advanced]](#advanced)

1. Klicken Sie abschließend auf **[!UICONTROL Save]** , um die Einstellungen anzuwenden und zum Arbeitsbereich [!DNL Page Builder] zurückzukehren.

## Weitere Folien hinzufügen

In den folgenden Abschnitten werden eine Reihe von Schritten beschrieben, um mit einer einzelnen Folie zu beginnen und einen responsiven Schieberegler zu erstellen, der Funktionen und Links zu bestimmten Produkten enthält. Wenn Sie noch keine einzelne Folie haben, befolgen Sie die vorherigen Anweisungen, um eine einzelne Folie zum Schritt hinzuzufügen.

Um Folien hinzuzufügen, verwenden Sie eine oder eine Kombination der folgenden Methoden:

### Methode 1: Duplizieren einer vorhandenen Folie

Sie können Zeit sparen, indem Sie eine Folie duplizieren, die bereits mit den erforderlichen Einstellungen konfiguriert wurde.

1. Klicken Sie auf den Navigationspunkt unter der Folie, um die Toolbox anzuzeigen, und wählen Sie das Symbol _Duplizieren_ ( ![Duplizieren](./assets/pb-icon-duplicate.png){width="20"} ) aus.

   ![Duplizieren einer Folie](./assets/pb-media-slider-duplicate-slide.png){width="500" zoomable="yes"}

1. Klicken Sie auf den Navigationspunkt für die neue Folie, um die Toolbox anzuzeigen, und wählen Sie das Symbol _Einstellungen_ ( ![Einstellungssymbol](./assets/pb-icon-settings.png){width="20"} ) aus.

1. Ändern Sie die Einstellungen nach Bedarf entsprechend den folgenden Abschnitten:

   - [[!UICONTROL Appearance]](#appearance)
   - [[!UICONTROL Background]](#background)
   - [[!UICONTROL Content]](#content)
   - [[!UICONTROL Advanced]](#advanced)

1. Klicken Sie abschließend auf **[!UICONTROL Save]** , um die Einstellungen anzuwenden und zum Arbeitsbereich [!DNL Page Builder] zurückzukehren.

### Methode 2: Neue leere Folie hinzufügen

1. Bewegen Sie den Mauszeiger über den Schieberegler oben, um die Toolbox anzuzeigen, und wählen Sie das Symbol _Hinzufügen_ ( ![Symbol hinzufügen](./assets/pb-icon-add.png){width="20"} ) aus.

   ![Leere Folie hinzufügen](./assets/pb-media-slider-toolbox-add.png){width="500" zoomable="yes"}

   Eine neue leere Folie mit einem eigenen Navigationspunkt und einer eigenen Toolbox wird dem Schieberegler hinzugefügt und auf der Bühne angezeigt.

   ![Neue Folie mit Toolbox](./assets/pb-media-slider-slide2-toolbox.png){width="500" zoomable="yes"}

1. Klicken Sie auf den Navigationspunkt für die neue Folie, um die Toolbox anzuzeigen, und wählen Sie das Symbol _Einstellungen_ ( ![Einstellungssymbol](./assets/pb-icon-settings.png){width="20"} ) aus.

1. Ändern Sie die Einstellungen nach Bedarf entsprechend den folgenden Abschnitten:

   - [[!UICONTROL Appearance]](#appearance)
   - [[!UICONTROL Background]](#background)
   - [[!UICONTROL Content]](#content)
   - [[!UICONTROL Advanced]](#advanced)

1. Wenn Sie fertig sind, klicken Sie oben rechts auf **[!UICONTROL Save]** , um die _[!UICONTROL Edit Slide]_&#x200B;zu schließen.

### Widget auf einer Folie hinzufügen

Sie können Ihrer Folie in einem [ Schritt einen beliebigen ](../content-design/widgets.md#widget-types)Widget[!DNL Page Builder]Typ) hinzufügen, indem Sie die folgenden Schritte ausführen:

1. [Erstellen Sie das Widget](../content-design/widget-create.md) das Sie auf einer Folie sehen möchten.

1. Öffnen Sie die Seite, den Block oder den dynamischen Block, in dem bzw. dem Sie den Schieberegler platzieren möchten, und erweitern Sie den **[!UICONTROL Content]**.

1. Erweitern Sie im [!DNL Page Builder] Bedienfeld **[!UICONTROL Media]** und ziehen Sie einen **[!UICONTROL Slider]** Platzhalter in eine Zeile, Spalte oder Registerkarte auf der Bühne.

1. Klicken Sie in den Schieberegler-Container, um die Symbolleiste [Texteditor](../content-design/editor.md) anzuzeigen, und klicken Sie auf _Widget einfügen_ ( ![Widget-Symbol einfügen](./assets/editor-btn-insert-widget.png){width="20"} ).

1. Wählen Sie die gewünschte **[!UICONTROL Widget Type]** aus.

1. Legen Sie die Einstellungen fest, die sich je nach Typ des Widgets unterscheiden

   ![Beispiel für das Einfügen eines Widgets auf der Folie](./assets/insert-widget-to-slide-page.png){width="600" zoomable="yes"}

1. Wenn Sie fertig sind, klicken Sie oben rechts auf **[!UICONTROL Insert Widget]** .

1. Ändern Sie die anderen Einstellungen nach Bedarf.

1. Wenn Sie fertig sind, klicken Sie oben rechts auf **[!UICONTROL Save]** .

   ![Beispiel eines eingefügten Widgets auf der Folie](./assets/inserting-widget-on-slide.png){width="600" zoomable="yes"}

### Anzeigen der einzelnen Folien

Um jede Folie auf der Bühne anzuzeigen, klicken Sie auf den nächsten Punkt unter der aktuell angezeigten Folie.

![Abgeschlossener Schieberegler](./assets/pb-media-slider-slide2.png){width="500" zoomable="yes"}

Die Folie im vorherigen Beispiel verfügt über ein Hintergrundbild, ein transparentes Mobilbild und ein Inline-Bild, das aus dem Texteditor hinzugefügt wurde. Diese Technik funktioniert auf Mobilgeräten gut, indem das Hintergrundbild deaktiviert und nur das kleinere Inline-Bild angezeigt wird. Die Produktfolie in diesem Beispiel weist die folgenden zusätzlichen Einstellungen auf:

| Option | Beispieleinstellung |
|--- |--- |
| [!UICONTROL Appearance] | `Collage Right` |
| [!UICONTROL Background Color] | `#ffffff` (weiß) |
| [!UICONTROL Background Image] | Das Bild auf dieser Folie wurde von der Produktseite gespeichert und in die Galerie hochgeladen. |
| [!UICONTROL Mobile Background Image] | Das mobile Hintergrundbild ist ein transparentes Bild, das 10 Pixel quadratisch ist. Wenn Sie für Mobilgeräte ein leeres Bild verwenden, wird das standardmäßige Hintergrundbild effektiv durch ein unsichtbares Bild ersetzt. |
| [!UICONTROL Background Size] | `Auto` |
| [!UICONTROL Message Text] | `Minerva LumaTech&trade; V-Tee` (Mitte ausrichten) mit eingefügtem Bild, das auf 40 % skaliert ist (Mitte ausrichten) |
| [!UICONTROL Link] | `Product` |
| [!UICONTROL Show Button] | `Always` |
| [!UICONTROL Button Text] | `Buy Now` |
| [!UICONTROL Show Overlay] | `Never Show` |
| [!UICONTROL Alignment] | `Center` (Ausrichten der Schaltfläche) |
| [!UICONTROL Border] | `Solid` |
| [!UICONTROL Border Color] | `#000000` (Schwarz) |
| [!UICONTROL Border Width] | `1 px` |

{style="table-layout:auto"}

## Ändern der individuellen Folieneinstellungen

1. Ändern Sie die Schieberegleranzeige auf der Bühne und zeigen Sie die Folie an, die Sie ändern möchten.

1. Wählen Sie in der Toolbox für die einzelnen Folien das Symbol _Einstellungen_ ( ![Einstellungssymbol](./assets/pb-icon-settings.png){width="20"} ) aus und vervollständigen Sie die Einstellungen nach Bedarf entsprechend den folgenden Abschnitten.

1. Klicken Sie oben rechts auf **[!UICONTROL Save]** , um die Einstellungen anzuwenden und zum Arbeitsbereich [!DNL Page Builder] zurückzukehren.

### [!UICONTROL Appearance]

1. Wählen Sie einen der folgenden Folienplatzierungstypen aus:

   | Typ | Beschreibung |
   | ---- | ----------- |
   | `Poster` | Zentriert den Folieninhalt im Schieberegler-Container. Die Überlagerung erweitert sich, falls verwendet, über die gesamte Breite des Schiebereglers. |
   | `Collage Left` | Platziert den Inhalt der Folie in einem definierten Bereich auf der linken Seite des Schiebereglers. Die Überlagerung deckt bei Verwendung nur den definierten Bereich ab. |
   | `Collage Center` | Platziert Folieninhalt in einem definierten Bereich, der auf dem Schieberegler-Container zentriert ist. Die Überlagerung deckt bei Verwendung nur den definierten Bereich ab. |
   | `Collage Right` | Platziert den Inhalt der Folie in einem definierten Bereich auf der rechten Seite des Schiebereglers. Die Überlagerung deckt bei Verwendung nur den definierten Bereich ab. |

   {style="table-layout:auto"}

   ![Positionierung des Objektträgers](./assets/pb-slide-appearance-collage-right.png){width="600" zoomable="yes"}

1. Geben Sie die **[!UICONTROL Slide Name]** ein.

   Wenn Sie im Bearbeitungsmodus arbeiten, wird der Folienname als QuickInfo über dem Navigationspunkt angezeigt. Der Folienname ist in der Storefront nicht sichtbar.

   ![Folienname in der Navigation](./assets/pb-media-slider-name-buy3-get1free.png){width="500" zoomable="yes"}

1. Geben Sie die **[!UICONTROL Minimum Height]** für die Folie ein.

   Die Mindesthöhe kann eine Zahl mit einer beliebigen gültigen CSS-Einheit (z. B. `100px`, `50%`, `50em`, `100vh`) oder eine Berechnung (z. B. `100vh - 237px`) sein.

   Sie können beispielsweise die Mindesthöhe der Folie so einstellen, dass sie die gesamte Seitenhöhe einnimmt, und dann Hintergrundbilder und Videos für überzeugende Designoptionen verwenden.

   >[!NOTE]
   >
   >Wenn der Objektträger auf die volle Seitenhöhe (100vh) eingestellt ist, dehnt der Schieberegler, der den Objektträger enthält, auch die gesamte Seitenhöhe, um die Höhe des Objektträgers zu berücksichtigen.

## [!UICONTROL Background]

Es gibt viele Möglichkeiten, die Hintergrundanzeige einer Folie zu definieren. Sie können ein einfaches Farb- oder Hintergrundbild anwenden und komplexere Effekte verwalten.

### [!UICONTROL Background Color]

Geben Sie die Hintergrundfarbe an, indem Sie ein Muster auswählen, auf die Farbauswahl klicken oder einen gültigen Farbnamen oder einen entsprechenden Hexadezimalwert eingeben. Diese Einstellung bestimmt die Hintergrundfarbe der Zeile. Sie können auch die Deckkraft der Farbe anpassen.

![Keine Farbe (Standard)](./assets/pb-settings-background-color-no-color.png){width="200"}

Sie haben drei Möglichkeiten, den Wert festzulegen:

- Ein vordefinierter Farbname, z. B. `White`
- Der hexadezimale Farbwert für die Farbe, z. B. `#ffffff`
- Der RGBA-Wert für die Farbe mit Prozentsatz für die Deckkraft, z. B. `rgba(255, 255, 255, 0.75)`

Wenn Sie eine Farbe auswählen möchten, klicken Sie auf das Farbfeld links neben dem Feld _Keine Farbe_.

![Auswählen eines Farbmusters](./assets/pb-settings-background-color-picker-swatch.png){width="600" zoomable="yes"}

Wenn Sie auf das Farbfeld klicken, um die Farbauswahl erneut zu öffnen, werden im Feld unter dem Schieberegler die aktuellen Rot-, Grün-, Blau- und Alpha-Werte (RGBA) angezeigt. Die letzte Zahl gibt den aktuellen Prozentsatz der Deckkraft als Dezimalzahl an. Sie können den Schieberegler verwenden, um die Deckkraft anzupassen, oder den gewünschten Dezimalwert eingeben.

![Festlegen der Hintergrundfarbopazität](./assets/pb-settings-background-color.png){width="600" zoomable="yes"}

>[!NOTE]
>
>[!DNL Page Builder] unterstützt auch eine Transparenzschicht (_Alphakanal_ in Hintergrundbildern, die verwendet werden können, um Hintergründe mit unterschiedlichem Grad der Deckkraft zu erstellen.

### [!UICONTROL Background Type]

Ein Hintergrundtyp kann ein Bild oder ein Video sein. [!DNL Page Builder] ist standardmäßig `Image` und zeigt verschiedene Bildeinstellungen an. Wenn Sie `Video` auswählen, tauscht [!DNL Page Builder] die Bildeinstellungen durch die Videoeinstellungen aus. Beide Einstellungen für den Hintergrundtyp werden in den folgenden Abschnitten beschrieben.

![Hintergrundtyp](./assets/pb-background-type.png){width="400"}

### Einstellungen für Bildtyp

Wenn Sie die _[!UICONTROL Background Type]_&#x200B;auf `Image` setzen, verwenden Sie die folgenden Einstellungen, um die Hintergrundbildanzeige zu definieren.

![Banner mit Hintergrundbild](./assets/pb-tutorial1-banner-background.png){width="600" zoomable="yes"}

- **[!UICONTROL Background Image]** - Verwenden Sie bei Bedarf die bereitgestellten Tools, um ein Hintergrundbild auszuwählen, das auf das Banner angewendet werden soll:

  | Tool | Beschreibung |
  | ---- | ----------- |
  | [!UICONTROL Upload] | Lädt eine Bilddatei von Ihrem lokalen Computer in die Galerie und wendet sie als Hintergrundbild für das Banner an. |
  | [!UICONTROL Select from Gallery] | Fordert Sie auf, ein vorhandenes Bild aus der Galerie als Hintergrundbild für das Banner auszuwählen. |
  | ![Kamerasymbol](./assets/pb-icon-camera.png){width="25"} | Hiermit können Sie das Bild entweder auf die Kamerakachel ziehen oder zum Bild in Ihrem lokalen Dateisystem navigieren. |

  {style="table-layout:auto"}

- **[!UICONTROL Background Mobile Image]** - Verwenden Sie bei Bedarf dieselben Tools, um ein anderes Hintergrundbild für die Anzeige auf Mobilgeräten auszuwählen.

- **[!UICONTROL Background Size]** : Wählen Sie aus, wie das Hintergrundbild in Bezug auf die Breite des Banners skaliert werden soll:

  | Option | Beschreibung |
  | ------ | ----------- |
  | `Cover` | Das Hintergrundbild deckt die gesamte Breite des Banners ab. |
  | `Contain` | Das Hintergrundbild ist auf die Breite des Inhaltsbereichs beschränkt. |
  | `Auto` | Wendet die Größe aus dem aktuellen Stylesheet an. |

  {style="table-layout:auto"}

  ![Hintergrundgröße](./assets/pb-layout-row-settings-background-size-cover.png){width="400"}

- **[!UICONTROL Background Position]** : Wählen Sie aus, wie das Hintergrundbild in Bezug auf das Banner verankert werden soll:

  | Ankerpunkt | Position |
  | ------------ | -------- |
  | `Top` | Links/Mitte/Rechts |
  | `Center` | Links/Mitte/Rechts |
  | `Bottom` | Links/Mitte/Rechts |

  {style="table-layout:auto"}

  Der Ankerpunkt ist wie ein Push-Pin, mit dem das Bild an der angegebenen Hintergrundposition an das Banner angehängt wird.

- **[!UICONTROL Background Repeat]** : Wenn Sie das Hintergrundbild wiederholen möchten, um den Bereich zu füllen, ändern Sie diese Einstellung `Yes`.

### Einstellungen für Videotyp

Wenn Sie den _Hintergrundtyp_ auf `Video` setzen, verwenden Sie die folgenden Einstellungen, um die Hintergrundbildanzeige zu definieren.

- **[!UICONTROL Video URL]** : Geben Sie eine gültige Video-URL ein. Gültige Video-URLs können Links sein zu:

   - Videos zu YouTube: `https://youtu.be/CoDhMRUUjeI`
   - Videos zu Vimeo: `https://vimeo.com/190156113`
   - Gültige Videodateien (`.mp4` wird empfohlen): `https://myvideos.com/spiral.mp4`

  ![URL des Hintergrundvideos](./assets/pb-video-url.png){width="500"}

- **[!UICONTROL Overlay Color]** - Wählen Sie eine Farbe aus, um einen transparenten Farbton auf das Video anzuwenden.

- **[!UICONTROL Infinite Loop]** : Stellen Sie diese Option auf `No` ein, damit das Video einmal abgespielt und dann angehalten wird. Wenn diese Option auf `Yes` (Standard) gesetzt ist, wiederholt sich das Video in einer Endlosschleife.

- **[!UICONTROL Lazy Load]** : Wählen Sie `No` aus, damit das Video mit der Seite geladen wird, auch wenn es nicht sichtbar ist. Wenn diese Option auf `Yes` (Standard) gesetzt ist, wird das Video nur von der Quelle geladen, wenn es auf dem Bildschirm sichtbar ist.

- **[!UICONTROL Play Only When Visible]** : Wählen Sie `No` aus, damit das Video sofort nach dem Laden wiedergegeben wird, unabhängig davon, ob es sichtbar ist. Wenn diese Option auf `Yes` (Standard) gesetzt ist, wird das Video nur abgespielt, wenn es sichtbar ist.

- **[!UICONTROL Fallback Image]** : Geben Sie bei Bedarf ein Bild an, das auf dem Bildschirm angezeigt werden soll, bevor das Video geladen wird, und geben Sie an, ob das Video aus irgendeinem Grund nicht geladen wird.

## [!UICONTROL Content]

Sie können den Folieninhalt direkt auf der Bühne oder beim Ändern der Einstellungen ändern. Die Einstellungen bieten komplexere Inhaltsfunktionen wie Folien-Links und Schaltflächen sowie Überlagerungen. Die Position des Inhalts spiegelt die Platzierungseinstellung [Erscheinungsbild](#appearance) wider.

### Einfacher Inhalt auf der Bühne

1. Klicken Sie auf den Platzhalter oder vorhandenen Text und geben Sie den neuen Text ein, der auf der Folie angezeigt werden soll.

   Die Editor-Symbolleiste wird über dem Textfeld angezeigt.

1. Verwenden Sie die Editor-Symbolleiste, um Text einzugeben und zu formatieren sowie Elemente wie Links, Bilder und Widgets einzufügen.

   ![Bühne mit formatiertem Text](./assets/pb-tutorial1-banner-stage-text-format-line2.png){width="500" zoomable="yes"}

### Komplexe Inhalte in den Einstellungen

1. Klicken Sie auf den Navigationspunkt am unteren Rand des Schiebereglers, um die Toolbox für die einzelne Folie anzuzeigen, und wählen Sie das Symbol _Einstellungen_ ( ![Einstellungen](./assets/pb-icon-settings.png){width="20"} ) aus.

1. Geben Sie im Abschnitt _[!UICONTROL Content]_&#x200B;die **[!UICONTROL Message Text]**&#x200B;ein, die mit der Folie angezeigt werden soll.

1. Scrollen Sie nach unten zum Abschnitt _[!UICONTROL Content]_&#x200B;und verwenden Sie den **[!UICONTROL Message Text]**-Editor, um Bannertext einzugeben und zu formatieren.

   Sie können auch Elemente wie Text-Links, Bilder und Widgets einfügen.

1. Formatieren Sie den Text nach Bedarf mithilfe der Editor-Symbolleiste.

   Die erste Folie in diesem Beispiel zeigt ein Hintergrundbild, aber keinen Nachrichtentext. Der `Buy 3 Get 1 Free` über dem Schieberegler befindet sich in einem Text-Container (später hinzugefügt).

1. Geben Sie bei Bedarf einen **[!UICONTROL Link]** für die Folie an.

   Der Link ist die Zielseite, die angezeigt wird, wenn der Kunde auf den Folienbereich klickt. Sie können einen von drei Link-Typen verwenden:

   - **[!UICONTROL URL]** - Links zu einer relativen oder vollständig qualifizierten URL.

   - **[!UICONTROL Product]** - Identifiziert die Zielseite anhand des Produktnamens oder der SKU. Suchen Sie nach dem Produkt anhand eines Namens, der entweder auf einem Teil- oder einem vollständigen Namen basiert. Wählen Sie das Produkt aus der Suchergebnisliste aus.

     ![Auswählen eines zu verknüpfenden Produkts](./assets/pb-media-image-settings-image-link-product-results.png){width="600" zoomable="yes"}

   - **[!UICONTROL Category]** - Identifiziert die Zielseite als eine bestimmte Kategorie oder Unterkategorie in der Kategoriestruktur. Suche nach der Kategorie basierend auf einem Teil- oder Vollnamen. Wählen Sie die Kategorie aus dem erweiterten Abschnitt der angezeigten Baumstruktur aus.

     ![Auswählen einer zu verknüpfenden Kategorie](./assets/pb-settings-link-category-womens-tees.png){width="600" zoomable="yes"}

   - **[!UICONTROL Page]** - Identifiziert die Zielseite als eine bestimmte Inhaltsseite. Suche nach der Seite basierend auf einem Teil- oder vollständigen Namen. Wählen Sie die Seite aus der Liste Suchergebnisse aus.

     ![Auswählen einer zu verknüpfenden Seite](./assets/pb-media-image-settings-image-link-page-results.png){width="600" zoomable="yes"}

   <div class="bs-callout-info" markdown="1">
   Ab Version 2.4.1 unterstützt [!DNL Page Builder] aufgrund von Problemen mit der Anzeige in der Storefront nicht mehr die Verknüpfung der Folie und von Links innerhalb des verschachtelten Texts. Wenn Sie einen Link in _[!UICONTROL Message Text]_ verwenden, können Sie die Option _[!UICONTROL Link]_ nicht konfigurieren. Wenn Sie es vorziehen, nur einen einzigen Link für die gesamte Folie zu verwenden, können Sie alle Links aus dem Text entfernen.

   ![Link-Konfiguration ist blockiert](./assets/pb-nested-link-blocked.png){width="300"}
   </div>

   Wenn Sie verhindern möchten, dass der Besucher Ihren Store verlässt, aktivieren Sie das Kontrollkästchen **[!UICONTROL Open in new tab]** . Wenn das Kontrollkästchen deaktiviert ist, wird das verknüpfte Ziel in derselben Browser-Registerkarte geöffnet, die den Besucher effektiv von Ihrem Store weg navigieren könnte.

1. Fügen Sie bei Bedarf eine Schaltfläche hinzu, um Kunden aufzufordern, dem Link zu folgen.

   Die Position _Folie_ Erscheinungsbild“ platziert einen einzelnen Link oder eine einzelne Schaltfläche unter dem Text. Füllen Sie die Eigenschaften des Links oder der Schaltfläche aus, den bzw. die Sie hinzufügen möchten.

   ![Slide-Erscheinungsbild - Collage rechts](./assets/pb-slide-appearance-collage-right.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Sie können auch mehrere Schaltflächen oder Links verwenden, indem Sie dem Banner einen [Block](block.md) hinzufügen. Um Konflikte zu vermeiden, behalten Sie alle Links oder Schaltflächen im separaten Block bei und fügen Sie keine Links oder Schaltflächen direkt zum Banner hinzu.

   - Legen Sie **[!UICONTROL Show Button]** auf eine der folgenden Einstellungen fest:

     | Option | Beschreibung |
     | ------ | ----------- |
     | `Always` | Auf der Folie wird immer eine Schaltfläche angezeigt. |
     | `On Hover` | Eine Schaltfläche wird nur beim Bewegen des Mauszeigers auf der Folie angezeigt. |
     | `Never Show` | Eine Schaltfläche wird nie auf der Folie angezeigt. |

     {style="table-layout:auto"}

   - Geben Sie die **[!UICONTROL Button Text]** ein, die auf der Schaltfläche angezeigt werden soll.

   - Legen Sie **[!UICONTROL Button Type]** auf eine der folgenden Einstellungen fest:

     | Option | Beschreibung |
     | ------ | ----------- |
     | `Primary` | Wendet die primäre Schaltflächenformatvorlage aus dem aktuellen Stylesheet an. |
     | `Secondary` | Wendet ggf. die sekundäre Schaltflächenformatvorlage aus dem aktuellen Stylesheet an. |
     | `Link` | Erstellt statt einer Schaltfläche einen Hyperlink. |

     {style="table-layout:auto"}

     Der Schaltflächenstil des aktuellen Designs bestimmt das Schaltflächenformat. In der Regel weist eine primäre Schaltfläche eine auffälligere Hintergrundfarbe auf als eine sekundäre Schaltfläche.

1. Legen Sie **[!UICONTROL Show Overlay]** auf eine der folgenden Einstellungen fest:

   | Option | Beschreibung |
   | ------ | ----------- |
   | `Always` | Die Überlagerung ist immer sichtbar. |
   | `On Hover` | Die Überlagerung wird nur beim Bewegen des Mauszeigers angezeigt. |
   | `Never Show` | Die Überlagerung ist nicht sichtbar. |

   {style="table-layout:auto"}

   Sie können eine Überlagerung verwenden, um eine Hintergrundfarbe auf den aktiven Inhaltsbereich anzuwenden, der durch die Einstellung Erscheinungsbild definiert wird. Das Hintergrundbild der Folie bleibt für die gesamte Breite der Folie sichtbar.

   ![Einstellungen für Folienüberlagerung](./assets/pb-media-slider-overlay-settings.png){width="600" zoomable="yes"}

   Wenn Sie eine Überlagerung anzeigen möchten, legen Sie die **[!UICONTROL Overlay Color]** fest:

   - Klicken Sie auf _Keine Farbe_ und wählen Sie ein Farbfeld aus.
   - Geben Sie im Feld **[!UICONTROL Color]** entweder einen gültigen Farbnamen oder einen Hexadezimalwert ein.

   ![Farbe der Folienüberlagerung](./assets/pb-tutorial1-banner-settings-overlay-color.png){width="600" zoomable="yes"}


## [!UICONTROL Search Engine Optimization] {#seo}

Der Text für diese Einstellungen ist für Suchmaschinen sichtbar und verbessert die Indizierung der Seite.

- Geben Sie **[!UICONTROL Alternative Text]** eine _Alt_-Textbeschreibung für die anzuzeigenden digitalen Barrierefreiheits-Tools ein.

  Die Verwendung von Alternativtext ist eine Best Practice für die Barrierefreiheit und wird in einigen Gebietsschemata gesetzlich vorgeschrieben. In HTML ist das `alt`-Attribut eine Teilmenge des `image`-Tags: `<image title="tooltip" alt="description" src="image.jpg">`.

- Geben Sie **[!UICONTROL Title Attribute]** den Text ein, der beim Bewegen des Mauszeigers als QuickInfo angezeigt werden soll.

  Wählen Sie als Best Practice einen beschreibenden, schlüsselwortreichen Titel aus, um die Art und Weise zu verbessern, wie das Bild von Suchmaschinen indiziert wird. In HTML ist das `title`-Attribut eine Teilmenge des `image`-Tags: `<image title="tooltip" alt="description" src="image.jpg">`.

## [!UICONTROL Advanced]

1. Um die horizontale Positionierung von Inhalten zu steuern, die der Folie hinzugefügt werden, wählen Sie die **[!UICONTROL Alignment]** aus:

   | Option | Beschreibung |
   | ------ | ----------- |
   | `Default` | Wendet die Standardeinstellung für die Ausrichtung an, die im Stylesheet des aktuellen Designs angegeben ist. |
   | `Left` | Richtet den Inhalt am linken Rand der Folie aus, wobei ein etwaiger Abstand berücksichtigt wird. |
   | `Center` | Richtet den Inhalt in der Mitte der Folie aus, wobei der angegebene Abstand berücksichtigt wird. |
   | `Right` | Richtet den Inhalt am rechten Rand der Folie aus, wobei ein etwaiger Abstand berücksichtigt wird. |

   {style="table-layout:auto"}

1. Legen Sie den **[!UICONTROL Border]** fest, der auf alle vier Seiten der Folie angewendet wird:

   | Option | Beschreibung |
   | ------ | ----------- |
   | `Default` | Wendet die Standardformatvorlage für Rahmen an, die im zugehörigen Stylesheet angegeben ist. |
   | `None` | Stellt keine sichtbaren Anzeigen für die Folienrahmen bereit. |
   | `Dotted` | Der Container-Rahmen wird als gepunktete Linie angezeigt. |
   | `Dashed` | Der Container-Rahmen wird als gestrichelte Linie angezeigt. |
   | `Solid` | Der Container-Rahmen wird als durchgezogene Linie angezeigt. |
   | `Double` | Der Container-Rahmen wird als doppelte Linie angezeigt. |
   | `Groove` | Der Container-Rahmen wird als gerillte Linie angezeigt. |
   | `Ridge` | Der Container-Rahmen wird als geriffelte Linie angezeigt. |
   | `Inset` | Der Container-Rahmen wird als Einfügelinie angezeigt. |
   | `Outset` | Der Container-Rahmen wird als Ausgangslinie angezeigt. |

   {style="table-layout:auto"}

1. Wenn Sie einen anderen Rahmenstil als `None` festlegen, müssen Sie die Anzeigeoptionen für den Rahmen vervollständigen:

   ![Rahmenfarbe](./assets/pb-settings-border-color.png){width="600" zoomable="yes"}

   | Option | Beschreibung |
   | ------ |------------ |
   | [!UICONTROL Border Color] | Geben Sie die Farbe an, indem Sie einen Musterabschnitt auswählen, auf die Farbauswahl klicken oder einen gültigen Farbnamen oder einen entsprechenden Hexadezimalwert eingeben. |
   | [!UICONTROL Border Width] | Geben Sie die Anzahl der Pixel für die Rahmenlinienbreite ein. |
   | [!UICONTROL Border Radius] | Geben Sie die Anzahl der Pixel ein, um die Größe des Radius festzulegen, mit dem jede Ecke des Rahmens gerundet werden soll. |

   {style="table-layout:auto"}

1. (Optional) Geben Sie die Namen der **[!UICONTROL CSS classes]** aus dem aktuellen Stylesheet an, die auf die Folie angewendet werden sollen.

   Trennen Sie mehrere Klassennamen durch ein Leerzeichen.

1. Geben Sie Werte in Pixeln für die **[!UICONTROL Margins and Padding]** ein, um die äußeren Ränder und den inneren Abstand der Folie festzulegen.

   Geben Sie jeden entsprechenden Wert in das Foliendiagramm ein.

   | Container-Bereich | Beschreibung |
   | -------------- | ----------- |
   | [!UICONTROL Margins] | Der Leerraum, der auf die Außenkante aller Seiten des Objektträgers angewendet wird. |
   | [!UICONTROL Padding] | Der Leerraum, der auf die Innenkante aller Seiten des Objektträgers angewendet wird. |

   {style="table-layout:auto"}

## Reglertitel hinzufügen

Wenn Sie einen Titel über dem Schieberegler möchten, fügen Sie einfach einen [Textinhaltstyp] über dem Schieberegler hinzu. Formatieren Sie dann den Text nach Bedarf.

1. Erweitern Sie im [!DNL Page Builder] Bedienfeld **[!UICONTROL Elements]** und ziehen Sie einen **Text**-Platzhalter auf eine Zeile, Spalte oder einen Registerkartensatz auf der Bühne.

   Beim Ziehen markiert eine rote Richtlinie die Einfügemarke über dem Schieberegler.

   ![Ziehen eines Textplatzhalters über einen Regler](./assets/pb-media-slider-elements-text-drag.png){width="600" zoomable="yes"}

1. Verwenden Sie den Editor, um den Text nach Bedarf zu formatieren.

   ![Bearbeiten des Reglertiteltextes](./assets/pb-media-slider-elements-text-editor.png){width="500" zoomable="yes"}

## Schiebereglereinstellungen ändern

1. Bewegen Sie den Mauszeiger über den Schieberegler-Container, um die Haupt-Toolbox anzuzeigen, und wählen Sie _Symbol_ Einstellungen![ ( Einstellungssymbol](./assets/pb-icon-settings.png){width="20"} ) aus.

   ![Regler-Toolbox](./assets/pb-media-slider-tee-shirts-main-toolbox.png){width="500" zoomable="yes"}

1. Geben Sie die **[!UICONTROL Minimum Height]** für die Folie ein.

   Die Mindesthöhe kann eine Zahl mit einer beliebigen gültigen CSS-Einheit (z. B. `100px`, `50%`, `50em`, `100vh`) oder eine Berechnung (z. B. `100vh - 237px`) sein.

   Sie können beispielsweise die Mindesthöhe eines Schiebereglers festlegen, um die gesamte Höhe der Seite zu dehnen, sodass Sie überzeugende Optionen für Hintergrundbilder und Videos mit voller Seite erhalten.

   ![Minimale Reglerhöhe](./assets/pb-media-slider-settings-minimum-height.png){width="400"}

1. Soll der Schieberegler beim Laden der Seite gestartet werden, legen Sie **[!UICONTROL Autoplay]** auf `Yes` und **[!UICONTROL Autoplay Speed]** auf die Anzahl der Millisekunden in der Verzögerung zwischen den Folien fest.

   Standardmäßig ist die Geschwindigkeit auf 4000 ms festgelegt, was vier Sekunden entspricht. Wenn Sie die automatische Wiedergabe auf `No` festlegen, wird standardmäßig die erste Folie angezeigt, und der Kunde muss auf die Foliennavigation (Punkte oder Pfeile) klicken, um die nächste Folie in der Reihenfolge anzuzeigen.

   ![Schieberegler für automatische Wiedergabe](./assets/pb-media-slider-settings-autoplay.png){width="600" zoomable="yes"}

1. Um den Übergang von einer Folie zur nächsten zu glätten, setzen Sie **[!UICONTROL Fade]** auf `Yes`.

   Mit dem Ausblenden scheinen die Folien an Ort und Stelle zu bleiben, aber der Inhalt ändert sich von einem zum nächsten reibungslos. Ohne Ausblenden sehen Sie die horizontale Bewegung von einer Folie zur nächsten.

   ![Schiebereglerüberblendung und Endlosschleifeneinstellungen](./assets/pb-media-slider-settings-fade-infinite-loop.png){width="600" zoomable="yes"}

1. Damit die Diashow unbegrenzt wiederholt wird, während die Seite geöffnet ist, legen Sie **[!UICONTROL Infinite Loop]** auf `Yes` fest.

1. Gehen Sie wie folgt vor, um den Typ der Navigationssteuerelemente für den Schieberegler auszuwählen:

   - Um die Pfeile _Weiter_ und _Zurück_ auf der linken und rechten Seite jeder Folie einzuschließen, setzen Sie **[!UICONTROL Show Arrows]** auf `Yes`.

   - Um eine Reihe von Navigationspunkten unter dem Schieberegler einzufügen, setzen Sie **[!UICONTROL Show Dots]** auf `Yes`.

   ![Schieberegler zeigt Pfeile und Punkte an](./assets/pb-media-slider-settings-show-arrows-dots.png){width="600" zoomable="yes"}

1. Füllen Sie [ Schiebereglereinstellungen ](#slider-advanced)Erweitert) nach Bedarf aus.

1. Klicken Sie abschließend auf **[!UICONTROL Save]** , um die Einstellungen anzuwenden und zum Arbeitsbereich [!DNL Page Builder] zurückzukehren.

### Erweitert - Schieberegler {#slider-advanced}

1. Um die Positionierung der Folien im übergeordneten Schieberegler-Container zu steuern, wählen Sie die **[!UICONTROL Alignment]** aus:

   | Option | Beschreibung |
   | ------ | ----------- |
   | `Default` | Wendet die Standardeinstellung für die Ausrichtung an, die im Stylesheet des aktuellen Designs angegeben ist. |
   | `Left` | Richtet die Folien am linken Rand des Schiebereglers aus, wobei der angegebene Abstand berücksichtigt wird. |
   | `Center` | Richtet die Objektträger in der Mitte des Schiebereglers aus, wobei der angegebene Abstand berücksichtigt wird. |
   | `Right` | Richtet die Objektträger am rechten Rand des Objektträgercontainers aus, wobei der angegebene Abstand berücksichtigt wird. |

   {style="table-layout:auto"}

1. Legen Sie den **[!UICONTROL Border]** fest, der auf alle vier Seiten des Schieberegler-Containers angewendet wird:

   | Option | Beschreibung |
   | ------ | ----------- |
   | `Default` | Wendet die Standardformatvorlage für Rahmen an, die im zugehörigen Stylesheet angegeben ist. |
   | `None` | Zeigt keine sichtbaren Begrenzungen des Containers an. |
   | `Dotted` | Der Container-Rahmen wird als gepunktete Linie angezeigt. |
   | `Dashed` | Der Container-Rahmen wird als gestrichelte Linie angezeigt. |
   | `Solid` | Der Container-Rahmen wird als durchgezogene Linie angezeigt. |
   | `Double` | Der Container-Rahmen wird als doppelte Linie angezeigt. |
   | `Groove` | Der Container-Rahmen wird als gerillte Linie angezeigt. |
   | `Ridge` | Der Container-Rahmen wird als geriffelte Linie angezeigt. |
   | `Inset` | Der Container-Rahmen wird als Einfügelinie angezeigt. |
   | `Outset` | Der Container-Rahmen wird als Ausgangslinie angezeigt. |

   {style="table-layout:auto"}

1. Wenn Sie einen anderen Rahmenstil als `None` festlegen, müssen Sie die Anzeigeoptionen für den Rahmen vervollständigen:

   | Option | Beschreibung |
   | ------ |------------ |
   | [!UICONTROL Border Color] | Geben Sie die Farbe an, indem Sie einen Musterabschnitt auswählen, auf die Farbauswahl klicken oder einen gültigen Farbnamen oder einen entsprechenden Hexadezimalwert eingeben. |
   | [!UICONTROL Border Width] | Geben Sie die Anzahl der Pixel für die Rahmenlinienbreite ein. |
   | [!UICONTROL Border Radius] | Geben Sie die Anzahl der Pixel ein, um die Größe des Radius festzulegen, mit dem jede Ecke des Rahmens gerundet werden soll. |

   {style="table-layout:auto"}

1. (Optional) Geben Sie die Namen der **[!UICONTROL CSS classes]** aus dem aktuellen Stylesheet an, die auf den Schieberegler-Container angewendet werden sollen.

   Trennen Sie mehrere Klassennamen durch ein Leerzeichen.

1. Geben Sie Werte in Pixeln für die **[!UICONTROL Margins and Padding]** ein, um die äußeren Ränder und den inneren Abstand des Schieberegler-Containers zu bestimmen.

   Geben Sie die entsprechenden Werte in das Diagramm ein.

   | Container-Bereich | Beschreibung |
   | -------------- | ----------- |
   | [!UICONTROL Margins] | Die Menge des Leerraums, der auf die Außenkante aller Seiten des Containers angewendet wird. |
   | [!UICONTROL Padding] | Die Menge des Leerraums, der auf die Innenkante aller Seiten des Containers angewendet wird. |

   {style="table-layout:auto"}

## Testen des Schiebereglers

1. Öffnen Sie die Seite, auf der Sie den Schieberegler eingefügt haben, und legen Sie **[!UICONTROL Enable Page]** auf `Yes` fest.

1. Klicken Sie oben rechts auf den **[!UICONTROL Save]** und wählen Sie **[!UICONTROL Save & Close]** aus.

1. Suchen Sie die Seite im Raster _Seiten_ und wählen Sie **[!UICONTROL View]** in der Spalte _[!UICONTROL Action]_&#x200B;aus.

   ![Reglervorschau - Standardansicht](./assets/pb-media-slider-desktop-view.png){width="600" zoomable="yes"}

   Ändern Sie bei der Vorschau des Schiebereglers die Größe des Fensters, damit Sie sehen können, wie es auf einem Mobilgerät angezeigt wird.

   ![Schiebereglervorschau - Mobilansicht](./assets/pb-media-slider-mobile-view.png){width="400" zoomable="yes"}

<!-- Last updated from includes: 2023-09-11 14:30:19 -->
