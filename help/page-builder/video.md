---
title: Medien - Video
description: Erfahren Sie mehr über den Videoinhaltstyp, mit dem ein auf YouTube oder Vimeo gehostetes Video zur  [!DNL Page Builder]  hinzugefügt wird.
exl-id: 9cd075e7-c10d-4c34-8932-c1ccb32bf198
feature: Page Builder, Page Content
source-git-commit: 79dc16dcba239af12793813ae19636bbd7ec49c5
workflow-type: tm+mt
source-wordcount: '918'
ht-degree: 0%

---

# Medien - Video

Verwenden Sie den _Video_-Inhaltstyp, um ein Video, das auf [YouTube][1] oder [Vimeo][2] gehostet wird, zur [[!DNL Page Builder]  hinzuzufügen](workspace.md#stage). Es ist einfach, Videos in eine Seite oder einen Block oder in Produkt- und Kategoriebeschreibungen einzubetten.

![Video auf der Startseite der Storefront](./assets/pb-storefront-video.png){width="700" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Video-Toolbox

![Video-Toolbox](./assets/pb-media-video-toolbox.png){width="600" zoomable="yes"}

| Tool | Symbol | Beschreibung |
|--- |--- |--- |
| Verschieben | ![move icon](./assets/pb-icon-move.png){width="25"} | Verschiebt das Video an eine andere Position auf der Bühne. |
| (Bezeichnung) | [!UICONTROL Video] | Identifiziert den aktuellen Inhalts-Container als Video. Bewegen Sie den Mauszeiger über den Bild-Container, um die Toolbox anzuzeigen. |
| Einstellungen | ![Einstellungssymbol](./assets/pb-icon-settings.png){width="25"} | Öffnet die Seite _[!UICONTROL Edit Video]_, auf der Sie die Eigenschaften des Videos und des Containers ändern können. |
| Ausblenden | ![Symbol ausblenden](./assets/pb-icon-hide.png){width="25"} | Blendet das aktuelle Video aus. |
| Anzeigen | ![Symbol anzeigen](./assets/pb-icon-show.png){width="25"} | Zeigt das ausgeblendete Video an. |
| Duplikat | ![Symbol „Duplizieren“](./assets/pb-icon-duplicate.png){width="25"} | Erstellt eine Kopie des Videos. |
| entfernen | ![Symbol entfernen](./assets/pb-icon-remove.png){width="25"} | Löscht das Video aus der Phase. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Video hinzufügen

1. Bevor Sie beginnen, navigieren Sie zum [YouTube][1]- oder [Vimeo][2]-Video, das Sie einbetten möchten, und kopieren Sie den Link.

   Alternativ können Sie auch einen direkten Link in eine gültige Videodatei kopieren. Gültige [ finden Sie unter &quot;](#basic-video-settings) Videoeinstellungen“.

1. Kehren Sie in der [!DNL Commerce] Admin zu dem Arbeitsbereich [!DNL Page Builder] zurück, in dem Sie das Video hinzufügen möchten.

1. Erweitern Sie im [!DNL Page Builder] Bedienfeld **[!UICONTROL Media]** und ziehen Sie einen **[!UICONTROL Video]** Platzhalter auf das Bühnenbild.

   ![Ziehen eines Video-Platzhalters auf die Bühne](./assets/pb-media-video-drag.png){width="600" zoomable="yes"}

1. Bewegen Sie den Mauszeiger über den Video-Container, um die Toolbox anzuzeigen, und wählen Sie _Symbol_ Einstellungen![ ( Einstellungssymbol](./assets/pb-icon-settings.png){width="20"} ) aus.

1. Fügen Sie **[!UICONTROL Video URL]** die URL des kopierten Videos ein.

   Die URL des in diesem Beispiel verwendeten [!DNL Page Builder]-Videos lautet: `https://www.youtube.com/watch?v=Y0KNS7C5dZA`.

1. Um die **[!UICONTROL Maximum Width]** des Videos zu begrenzen, geben Sie die maximale Breite in Pixel ein.

   Wenn es leer ist, wird das Video so breit wie vom Container erlaubt, wobei Ränder und Abstände berücksichtigt werden.

1. Klicken Sie oben rechts auf **[!UICONTROL Save]** , um die Einstellungen anzuwenden und zum Arbeitsbereich [!DNL Page Builder] zurückzukehren.

## Videoeinstellungen ändern

1. Bewegen Sie den Mauszeiger über den Video-Container, um die Toolbox anzuzeigen, und wählen Sie _Symbol_ Einstellungen![ ( Einstellungssymbol](./assets/pb-icon-settings.png){width="20"} ) aus.

1. Ändern Sie die Einstellungen gemäß den folgenden Abschnitten:

   - [Einfach](#basic-video-settings)
   - [Erweitert](#advanced)

1. Klicken Sie oben rechts auf **[!UICONTROL Save]** , um die Einstellungen anzuwenden und zum Arbeitsbereich [!DNL Page Builder] zurückzukehren.

### Grundlegende Videoeinstellungen

1. Um das aktuelle Video zu ändern, aktualisieren Sie die **[!UICONTROL Video URL]**.

   Geben Sie eine gültige Video-URL ein. Gültige Video-URLs können Links sein zu:

   - Videos zu YouTube: `https://youtu.be/CoDhMRUUjeI`
   - Videos zu Vimeo: `https://vimeo.com/190156113`
   - Gültige Videodateien (`.mp4` wird empfohlen): `https://myvideos.com/spiral.mp4`

1. Um die zulässige Breite für das Video in der Storefront zu ändern, geben Sie die neue **[!UICONTROL Maximum Width]** in Pixel ein.

   Wenn dieses Feld leer ist, erweitert das Video die gesamte Breite des Containers, wobei Ränder und Abstände weniger berücksichtigt werden.

1. Um das Video nach dem Laden der Seite automatisch zu starten, setzen Sie **[!UICONTROL Autoplay]** auf `Yes`.

   Wenn die automatische Wiedergabe auf `Yes` festgelegt ist, wird das Video bei der Wiedergabe gemäß Richtlinie stummgeschaltet. Aber auch mit dieser Einstellung können Mobilgeräte Ihre Videos nicht automatisch abspielen. Weitere Informationen zu diesen Richtlinien finden Sie in den folgenden Entwicklerressourcen:

   - [Autoplay-Richtlinie von Vimeo](https://vimeo.zendesk.com/hc/en-us/articles/115004485728-Autoplaying-and-looping-embedded-videos)
   - [Richtlinie zur automatischen Wiedergabe aus Google (Chrome/YouTube)](https://developer.chrome.com/blog/autoplay/)
   - [Richtlinie zur automatischen Wiedergabe für lokale Videos](https://developer.mozilla.org/en-US/docs/Web/Media/Autoplay_guide)

   Wenn die automatische Wiedergabe auf `No` eingestellt ist, wird das Video nur auf Benutzerwunsch wiedergegeben.

### [!UICONTROL Advanced]

1. Um die horizontale Positionierung des Videos innerhalb des Containers zu steuern, wählen Sie eine **[!UICONTROL Alignment]** aus:

   | Option | Beschreibung |
   | ------ | ----------- |
   | `Default` | Wendet die Standardeinstellung für die Ausrichtung an, die im Stylesheet des aktuellen Designs angegeben ist. |
   | `Left` | Richtet den Inhalt am linken Rand des Video-Containers aus, wobei ein etwaiger Abstand berücksichtigt wird. |
   | `Center` | Richtet den Inhalt in der Mitte des Video-Containers aus, wobei der angegebene Abstand berücksichtigt wird. |
   | `Right` | Richtet den Inhalt am rechten Rand des Video-Containers aus, wobei ein etwaiger Abstand berücksichtigt wird. |

   {style="table-layout:auto"}

- Legen Sie den **[!UICONTROL Border]** fest, der auf alle vier Seiten des Video-Containers angewendet wird:

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

- (Optional) Geben Sie die Namen der **[!UICONTROL CSS classes]** aus dem aktuellen Stylesheet an, die auf den Video-Container angewendet werden sollen.

  Trennen Sie mehrere Klassennamen durch ein Leerzeichen.

- Geben Sie Werte in Pixeln für die **[!UICONTROL Margins and Padding]** ein, um die äußeren Ränder und den inneren Abstand des Video-Containers anzugeben.

  Geben Sie jeden entsprechenden Wert im Video-Container-Diagramm ein.

  | Container-Bereich | Beschreibung |
  | -------------- | ----------- |
  | [!UICONTROL Margins] | Die Menge des Leerraums, der auf die Außenkante aller Seiten des Containers angewendet wird. |
  | [!UICONTROL Padding] | Die Menge des Leerraums, der auf die Innenkante aller Seiten des Containers angewendet wird. |

  {style="table-layout:auto"}

## Video verschieben

1. Bewegen Sie den Mauszeiger über den Video-Container, um die Toolbox anzuzeigen, und wählen Sie _Symbol „Verschieben_ ( ![Symbol Verschieben](./assets/pb-icon-move.png){width="20"} ) aus.

   ![Verschieben eines Videos](./assets/pb-media-video-toolbox-move-col1.png){width="500" zoomable="yes"}

1. Wählen Sie das Video aus und ziehen Sie es an die neue Position, direkt unter der roten Richtlinie.

   ![Verwenden der roten Richtlinie zum Platzieren des Videos](./assets/pb-media-video-toolbox-move-col2.png){width="500" zoomable="yes"}

## Entfernen eines Videos aus der Bühne

1. Bewegen Sie den Mauszeiger über den Video-Container, um die Toolbox anzuzeigen, und wählen Sie _Symbol „Entfernen_ (![Symbol entfernen](./assets/pb-icon-remove.png)) aus.

1. Wenn Sie zum Bestätigen aufgefordert werden, klicken Sie auf **[!UICONTROL OK]**.

[1]: https://www.youtube.com/
[2]: https://vimeo.com/
