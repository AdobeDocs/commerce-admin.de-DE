---
title: Layout - Zeile
description: Erfahren Sie mehr über den Inhaltstyp der Zeile, der zum Hinzufügen einer Zeile in der  [!DNL Page Builder]  verwendet wird.
exl-id: 0aa8bf6f-7ae3-4718-9f76-430ed63ba05c
feature: Page Builder, Page Content
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '1620'
ht-degree: 0%

---

# Layout - Zeile

Verwenden Sie den _Row_-Content-Typ, um eine Zeile in der [[!DNL Page Builder] Staging](workspace.md#stage) hinzuzufügen.

{{$include /help/_includes/page-builder-save-timeout.md}}

## Zeilen-Toolbox

Die Zeilen-Toolbox wird angezeigt, wenn Sie den Mauszeiger über den Zeilen-Container bewegen. Die Toolbox enthält Optionen zum Verschieben, Ausblenden, Duplizieren, Bearbeiten oder Entfernen der Zeile. Die Auswahl der Einstellungen bestimmt das Erscheinungsbild, den Hintergrund und das Layout der Zeile. Zusätzliche Inhaltselemente können aus dem [!DNL Page Builder] auf der linken Seite in die Zeile gezogen werden.

![Zeilen-Toolbox](./assets/pb-layout-page-add-content-row-tools.png){width="600" zoomable="yes"}

| Tool | Symbol | Beschreibung |
| --------- | ---------- | ----------- |
| Verschieben | ![move icon](./assets/pb-icon-move.png){width="25"} | Verschiebt die Zeile an eine andere Position im Verhältnis zu anderen Zeilen auf der Bühne. |
| (Bezeichnung) | [!UICONTROL Row] | Identifiziert den aktuellen Inhalts-Container als Zeile. Bewegen Sie den Mauszeiger über den Container, um die Toolbox anzuzeigen. |
| Einstellungen | ![Einstellungssymbol](./assets/pb-icon-settings.png){width="25"} | Öffnet die Seite Zeile bearbeiten , auf der Sie die Eigenschaften des Containers ändern können. |
| Ausblenden | ![Symbol ausblenden](./assets/pb-icon-hide.png){width="25"} | Blendet die aktuelle Zeile aus. |
| Anzeigen | ![Symbol anzeigen](./assets/pb-icon-show.png){width="25"} | Zeigt die ausgeblendete Zeile an. |
| Duplikat | ![Symbol „Duplizieren“](./assets/pb-icon-duplicate.png){width="25"} | Erstellt eine Kopie der Zeile. |
| entfernen | ![Symbol entfernen](./assets/pb-icon-remove.png){width="25"} | Löscht den Zeilen-Container und seinen Inhalt aus der Phase. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Zeile hinzufügen

1. Ziehen Sie im [!DNL Page Builder] unter _[!UICONTROL Layout]_einen neuen **[!UICONTROL Row]**auf das Stadium, direkt unter der ersten Zeile.

1. Um die Zeile zu formatieren, bewegen Sie den Mauszeiger über den Zeilen-Container, um die Toolbox anzuzeigen, und wählen _das Symbol_ Einstellungen![ aus (Symbol Einstellungen](./assets/pb-icon-settings.png){width="20"} ).

   In den folgenden Abschnitten finden Sie detaillierte Informationen zum Abschließen der verfügbaren Einstellungen.

   ![Zeile hinzufügen](./assets/pb-layout-row-add.png){width="600" zoomable="yes"}

## Zeileneinstellungen ändern

1. Bewegen Sie den Mauszeiger über den Zeilen-Container, um die Toolbox anzuzeigen, und wählen Sie _Symbol_ Einstellungen![ ( Einstellungssymbol](./assets/pb-icon-settings.png){width="20"} ) aus.

   ![Zeilen-Toolbox](./assets/pb-tutorial1-row-toolbox.png){width="600" zoomable="yes"}

1. In den folgenden Abschnitten finden Sie detaillierte Informationen zum Aktualisieren der verfügbaren Einstellungen.

1. Klicken Sie abschließend auf **[!UICONTROL Save]** , um die Einstellungen anzuwenden und zum Arbeitsbereich [!DNL Page Builder] zurückzukehren.

## Erscheinungsbild

Verwenden Sie die _Erscheinungsbild_, um festzulegen, wie Inhalte in der Zeile angezeigt werden.

![Erscheinungsbildeinstellungen](./assets/pb-row-layout.png){width="600" zoomable="yes"}

- Um zu bestimmen, wie die Hintergrundfarbe und/oder das Hintergrundbild in Bezug auf den Container und die Breite des Inhaltsbereichs angezeigt wird, wählen Sie die Ausrichtung aus:

  | Option | Beschreibung |
  | ------ | ----------- |
  | [!UICONTROL Contained] | Die Hintergrundfarbe oder das Bild ist auf die maximale Seitenbreite beschränkt, die vom Design definiert wird. |
  | [!UICONTROL Full Width] | Beschränkt den Inhalt auf die maximale Seitenbreite, die vom Design definiert wird. Die Hintergrundfarbe und/oder das Bild sind nicht beschränkt und erstrecken sich über die gesamte Breite der Zeile. |
  | [!UICONTROL Full Bleed] | Der Inhalt und das Hintergrundbild und/oder die Farbe sind nicht beschränkt und erweitern die gesamte Breite der Zeile. Vollständiger Anschnitt kann nur mit ([) verwendet werden](../content-design/themes.md) die das Layout unterstützen. |

  {style="table-layout:auto"}

- Geben Sie die **[!UICONTROL Minimum Height]** für die Zeile ein. Dieser Wert kann eine Zahl mit einer beliebigen gültigen CSS-Einheit (z. B. `100px`, `50%`, `50em`, `100vh`) oder eine Berechnung (z. B. `100vh - 237px`) sein.

  Sie können beispielsweise die Mindesthöhe einer Zeile festlegen, um die gesamte Höhe der Seite zu dehnen, sodass Sie überzeugende Optionen für Hintergrundbilder und Videos mit voller Seite erhalten.

- Wählen Sie eine **[!UICONTROL Vertical Alignment]** aus, um alle Inhalts-Container auszurichten, die der Zeile hinzugefügt werden (oben, zentriert oder unten).

## Hintergrund

Es gibt viele Optionen zum Definieren der Hintergrundanzeige einer Zeile. Sie können ein einfaches Farb- oder Hintergrundbild anwenden und komplexere Effekte verwalten.

### Hintergrundfarbe

Geben Sie die Hintergrundfarbe an, indem Sie ein Farbfeld auswählen, auf die Farbauswahl klicken oder einen gültigen Farbnamen oder einen entsprechenden Hexadezimalwert eingeben. Diese Einstellung bestimmt die Hintergrundfarbe der Zeile. Sie können auch die Deckkraft der Farbe anpassen.

![Keine Farbe (Standard)](./assets/pb-settings-background-color-no-color.png){width="200"}

Sie haben drei Möglichkeiten, den Wert festzulegen:

- Ein vordefinierter Farbname, z. B. `White`
- Der hexadezimale Farbwert für die Farbe, z. B. `#ffffff`
- Der RGBA-Wert für die Farbe mit Prozentsatz für die Deckkraft, z. B. `rgba(255, 255, 255, 0.75)`

Wenn Sie eine Farbe auswählen möchten, klicken Sie auf das Farbfeld links neben dem Feld _Keine Farbe_.

![Auswählen eines Farbmusters](./assets/pb-settings-background-color-picker-swatch.png){width="600" zoomable="yes"}

Wenn Sie auf das Farbfeld klicken, um die Farbauswahl erneut zu öffnen, werden im Feld unter dem Schieberegler die aktuellen Rot-, Grün-, Blau- und Alpha-Werte (RGBA) angezeigt. Die letzte Zahl gibt den aktuellen Prozentsatz der Deckkraft als Dezimalzahl an. Sie können den Schieberegler verwenden, um die Deckkraft anzupassen, oder den gewünschten Dezimalwert eingeben.

![Festlegen der Deckkraft](./assets/pb-settings-background-color.png){width="600" zoomable="yes"}

>[!NOTE]
>
>[!DNL Page Builder] unterstützt auch eine Transparenzschicht (_Alphakanal_ in Hintergrundbildern, die verwendet werden können, um Hintergründe mit unterschiedlichem Grad der Deckkraft zu erstellen.

### [!UICONTROL Background Type]

Ein Hintergrundtyp kann ein Bild oder ein Video sein. [!DNL Page Builder] ist standardmäßig `Image` und zeigt verschiedene Bildeinstellungen an. Wenn Sie `Video` auswählen, tauscht [!DNL Page Builder] die Bildeinstellungen durch die Videoeinstellungen aus. Beide Hintergrundtypen werden wie folgt beschrieben.

![Hintergrundtyp](./assets/pb-background-type.png){width="200"}

### Einstellungen für Bildtyp

Wenn Sie die _[!UICONTROL Background Type]_auf `Image` setzen, verwenden Sie die folgenden Einstellungen, um die Hintergrundbildanzeige zu definieren.

![Hintergrundbild](./assets/pb-tutorial1-row-settings-background-image-selected.png){width="600" zoomable="yes"}

- **[!UICONTROL Background Image]** - Verwenden Sie bei Bedarf die bereitgestellten Tools, um ein Hintergrundbild auszuwählen, das auf die Zeile angewendet werden soll:

  | Option | Beschreibung |
  | ------ | ----------- |
  | [!UICONTROL Upload] | Lädt eine Bilddatei von Ihrem lokalen Computer in die Galerie hoch und wendet sie dann als Hintergrundbild für die Zeile an. |
  | [!UICONTROL Select from Gallery] | Fordert Sie auf, ein vorhandenes Bild aus der Galerie als Hintergrundbild für die Zeile auszuwählen. |
  | ![Kamerasymbol](./assets/pb-icon-camera.png){width="25"} | Hiermit können Sie das Bild entweder auf die Kamerakachel ziehen oder zum Bild in Ihrem lokalen Dateisystem navigieren. |

  {style="table-layout:auto"}

- **[!UICONTROL Background Mobile Image]** - Verwenden Sie bei Bedarf dieselben Tools, um ein anderes Hintergrundbild für die Anzeige auf Mobilgeräten auszuwählen.

- **[!UICONTROL Background Size]** - Legen Sie diese Option fest, um festzulegen, wie das Hintergrundbild in Bezug auf die Breite der Zeile skaliert wird:

  | Option | Beschreibung |
  | ------ | ----------- |
  | `Cover` | Das Hintergrundbild deckt die gesamte Breite der Zeile ab. |
  | `Contain` | Das Hintergrundbild ist auf die Breite des Inhaltsbereichs beschränkt. |
  | `Auto` | Wendet die Größe aus dem aktuellen Stylesheet an. |

  {style="table-layout:auto"}

  ![Hintergrundgröße](./assets/pb-layout-row-settings-background-size-cover.png){width="250"}

- **[!UICONTROL Background Position]** - Legen Sie diese Option fest, um festzulegen, wie das Hintergrundbild in Bezug auf die Zeile verankert wird:

  | Ankerpunkt | Position |
  | ------ | ----------- |
  | `Top` | Links/Mitte/Rechts |
  | `Center` | Links/Mitte/Rechts |
  | `Bottom` | Links/Mitte/Rechts |

  {style="table-layout:auto"}

  Der Ankerpunkt ist wie ein Push-Pin, mit dem das Bild an der angegebenen Hintergrundposition an der Zeile befestigt wird.

- **[!UICONTROL Background Attachment]** : Legen Sie den Anlagentyp fest, um zu bestimmen, wie sich das Hintergrundbild in Bezug auf die Bildlaufseite bewegt:

  | Option | Beschreibung |
  | ------ | ----------- |
  | `Scroll` | Das angehängte Hintergrundbild wird synchronisiert, sodass es beim Bildlauf auf der Seite nach unten verschoben wird. Verwenden Sie den Parallax-Hintergrund, um die Bildlaufgeschwindigkeit zu steuern. |
  | `Fixed` | (Nicht für Mobilgeräte verfügbar) Das Hintergrundbild wird nicht verschoben, wenn der Container über das Bild scrollt und an der angegebenen Hintergrundposition fixiert ist. |

  {style="table-layout:auto"}

- **[!UICONTROL Background Repeat]** : Setzen Sie diesen Wert auf `Yes`, um das Hintergrundbild zu wiederholen und den verfügbaren Platz in der Zeile auszufüllen.

### Einstellungen für Videotyp

Wenn Sie den _Hintergrundtyp_ auf `Video` setzen, verwenden Sie die folgenden Einstellungen, um die Hintergrundbildanzeige zu definieren.

- **[!UICONTROL Video URL]** : Geben Sie eine gültige Video-URL ein. Gültige Video-URLs können Links sein zu:

   - Videos zu YouTube: `https://youtu.be/CoDhMRUUjeI`
   - Videos zu Vimeo: `https://vimeo.com/190156113`
   - Gültige Videodateien (`.mp4` wird empfohlen): `https://myvideos.com/spiral.mp4`

  ![URL des Hintergrundvideos](./assets/pb-video-url.png){width="300"}

- **[!UICONTROL Overlay Color]** - Wählen Sie eine Farbe aus, um einen transparenten Farbton auf das Video anzuwenden.

- **[!UICONTROL Infinite Loop]** : Stellen Sie diese Option auf `No` ein, damit das Video einmal abgespielt und dann angehalten wird. Wenn diese Option auf `Yes` (Standard) gesetzt ist, wiederholt sich das Video in einer Endlosschleife.

- **[!UICONTROL Lazy Load]** : Wählen Sie `No` aus, damit das Video mit der Seite geladen wird, auch wenn es nicht sichtbar ist. Wenn diese Option auf `Yes` (Standard) gesetzt ist, wird das Video nur von der Quelle geladen, wenn es auf dem Bildschirm sichtbar ist.

- **[!UICONTROL Play Only When Visible]** : Wählen Sie `No` aus, damit das Video sofort nach dem Laden wiedergegeben wird, unabhängig davon, ob es sichtbar ist. Wenn diese Option auf `Yes` (Standard) gesetzt ist, wird das Video nur abgespielt, wenn es sichtbar ist.

- **[!UICONTROL Fallback Image]** : Geben Sie bei Bedarf ein Bild an, das auf dem Bildschirm angezeigt werden soll, bevor das Video geladen wird, und geben Sie an, ob das Video aus irgendeinem Grund nicht geladen wird.

## Parallaxenhintergrund

Verwenden Sie diese Optionen, um die Geschwindigkeit des Bildlaufs eines Hintergrundbilds oder -videos im Verhältnis zum Bildlauf auf der Seite zu steuern. Der Hintergrund kann so eingestellt werden, dass er langsamer scrollt, um ein Gefühl der Immersion zu erzeugen.

- Setzen Sie **Enable Parallax Background** auf `Yes`.
- Geben Sie die **Parallaxengeschwindigkeit** als Dezimalwert zwischen `-1.0` und `2.0` ein.

![Parallax Hintergrundeinstellungen](./assets/pb-settings-parallax-background.png){width="600" zoomable="yes"}

## Erweitert

- Um die horizontale Positionierung von Inhalts-Containern zu steuern, die der Zeile hinzugefügt werden, wählen Sie eine **[!UICONTROL Alignment]** aus:

  | Option | Beschreibung |
  | ------ | ----------- |
  | `Default` | Wendet die Standardeinstellung für die Ausrichtung an, die im Stylesheet des aktuellen Designs angegeben ist. |
  | `Left` | Richtet die Inhalts-Container am linken Rand des Zeilen-Containers aus, wobei für jeden angegebenen Abstand berücksichtigt wird. |
  | `Center` | Richtet den Inhalts-Container in der Mitte des Zeilen-Containers aus, wobei alle angegebenen Auffüllungen berücksichtigt werden. |
  | `Right` | Richtet den Inhalts-Container am rechten Rand des Zeilen-Containers aus, wobei für jeden angegebenen Abstand berücksichtigt wird. |

  {style="table-layout:auto"}

- Legen Sie den **[!UICONTROL Border]** fest, der auf alle vier Seiten des Zeilen-Containers angewendet wird:

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

- Wenn Sie einen anderen Rahmenstil als `None` festlegen, müssen Sie die Anzeigeoptionen für den Rahmen vervollständigen:

  ![Rahmenfarbe](./assets/pb-settings-border-color.png){width="600" zoomable="yes"}

  | Option | Beschreibung |
  | ------ |------------ |
  | [!UICONTROL Border Color] | Geben Sie die Farbe an, indem Sie einen Musterabschnitt auswählen, auf die Farbauswahl klicken oder einen gültigen Farbnamen oder einen entsprechenden Hexadezimalwert eingeben. |
  | [!UICONTROL Border Width] | Geben Sie die Anzahl der Pixel für die Rahmenlinienbreite ein. |
  | [!UICONTROL Border Radius] | Geben Sie die Anzahl der Pixel ein, um die Größe des Radius festzulegen, mit dem jede Ecke des Rahmens gerundet werden soll. |

  {style="table-layout:auto"}

  Die Zeile im folgenden Beispiel hat einen Rahmenradius von 15.

  ![Zeile mit dem Rahmenradius von 15](./assets/pb-settings-border-radius-15.png){width="500"}

- (Optional) Geben Sie die Namen der **[!UICONTROL CSS classes]** aus dem aktuellen Stylesheet an, die auf den Zeilen-Container angewendet werden sollen.

  Trennen Sie mehrere Klassennamen durch ein Leerzeichen.

- Geben Sie Werte in Pixeln für die **[!UICONTROL Margins and Padding]** ein, um die äußeren Ränder und den inneren Abstand der Zeile festzulegen.

  Geben Sie jeden entsprechenden Wert in das Zeilen-Container-Diagramm ein.

  | Container-Bereich | Beschreibung |
  | -------------- | ----------- |
  | [!UICONTROL Margins] | Die Menge des Leerraums, der auf die Außenkante aller Seiten des Containers angewendet wird. Optionen: `Top` / `Right` / `Bottom` / `Left` |
  | [!UICONTROL Padding] | Die Menge des Leerraums, der auf die Innenkante aller Seiten des Containers angewendet wird. Optionen: `Top` / `Right` / `Bottom` / `Left` |

  {style="table-layout:auto"}

  ![Ränder und Abstand](./assets/pb-layout-row-settings-margin-padding-default.png){width="600" zoomable="yes"}

<!-- Last updated from includes: 2023-09-11 14:30:19 -->
