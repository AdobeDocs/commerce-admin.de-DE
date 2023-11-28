---
title: Elemente - Trennlinie
description: Erfahren Sie mehr über den Inhaltstyp "Divider", mit dem eine Regel als visueller Umbruch zwischen Inhaltsabschnitten in der [!DNL Page Builder] Bühne.
exl-id: e1052170-6d2f-4893-a78b-a845a8b6c0d9
feature: Page Builder, Page Content
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 0%

---

# Elemente - Trennlinie

Verwenden Sie die _Trennlinie_ Inhaltstyp , um eine Regel als visuellen Umbruch zwischen Inhaltsabschnitten im [[!DNL Page Builder] Schritt](workspace.md#stage). Sie können die Linienfarbe, die Dicke und die Breite des Trennzeichens angeben. Sie können auch die Ausrichtung, die Ränder und den Abstand sowie das Format des Containerrahmens steuern. Standardmäßig ist der Divider eine Haarregel, die die gesamte Breite des Containers erweitert, wobei der Abstand berücksichtigt wird.

![Standardunterteilung in einem Container ohne Rahmen](./assets/pb-elements-divider-default.png){width="500" zoomable="yes"}

Obwohl die meisten Divider-Container unsichtbar sind, zeigt das folgende Beispiel den Container mit einem roten gestrichelten Rand, sodass Sie die Beziehung zwischen dem Divider, dem Abstand und dem Container sehen können. Sie können den Abstand am oberen und unteren Rand der Trennlinie anpassen, um den Abstand zwischen Elementen zu steuern.

![Trennlinie mit Abstand im Container mit gestricheltem Rahmen](./assets/pb-elements-divider-default-border-dashed.png){width="500" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Trennlinien-Toolbox

| Tool | Symbol | Beschreibung |
| ---- | --------------------| ------------|
| Verschieben | ![Symbol Verschieben](./assets/pb-icon-move.png){width="25"} | Verschiebt den Divider-Container an eine andere gültige Position auf der Seite. |
| (Titel) | DIVIDER | Identifiziert den aktuellen Container als Trennelement. |
| Einstellungen | ![Symbol Einstellungen](./assets/pb-icon-settings.png){width="25"} | Öffnet die Seite Divider bearbeiten , auf der Sie die Eigenschaften des Dividers und seines Containers ändern können. |
| Ausblenden | ![Symbol &quot;Ausblenden&quot;](./assets/pb-icon-hide.png){width="25"} | Blendet den Trenncontainer aus. |
| Anzeigen | ![Symbol &quot;Anzeigen&quot;](./assets/pb-icon-show.png){width="25"} | Zeigt den ausgeblendeten Divider-Container an. |
| Duplizieren | ![Symbol &quot;Duplizieren&quot;](./assets/pb-icon-duplicate.png){width="25"} | Kopiert den Divider-Container. |
| Entfernen | ![Symbol &quot;Entfernen&quot;](./assets/pb-icon-remove.png){width="25"} | Löscht den Divider-Container und seinen Inhalt aus der Bühne. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Divider hinzufügen

1. Im [!DNL Page Builder] Bedienfeld, erweitern **[!UICONTROL Elements]** und ziehen Sie eine **[!UICONTROL Divider]** Platzhalter für eine Zeile, Spalte oder Registerkarte, die auf der Bühne festgelegt ist.

   Verwenden Sie die rote Führungslinie für die Referenz, wenn Sie die Trennlinie entweder vor oder nach einem anderen Inhaltscontainer auf der Bühne positionieren.

   ![Ziehen einer Trennlinie auf die Bühne](./assets/pb-elements-divider-drag.png){width="600" zoomable="yes"}

   Im folgenden Beispiel markiert die Trennlinie den Anfang eines neuen Textabschnitts.

   ![Trennlinien für Textabschnitte](./assets/pb-elements-dividers-multiple-text-row.png){width="500" zoomable="yes"}

1. Gehen Sie wie folgt vor, um die Einstellungen der neuen Trennlinie festzulegen.

## Dividereinstellungen ändern

1. Bewegen Sie den Mauszeiger über den Divider-Container, um die Toolbox anzuzeigen und die _Einstellungen_ ( ![Symbol Einstellungen](./assets/pb-icon-settings.png){width="20"} ).

   ![Trennlinien-Toolbox](./assets/pb-elements-divider-toolbox.png){width="500" zoomable="yes"}

1. Divider ändern **[!UICONTROL Line Color]** Verwendung einer der folgenden Methoden:

   - Gültige eingeben [HTML-Farbname][1]. Beispiel, `Teal`.
   - Geben Sie den hexadezimalen Farbwert ein. Beispiel, `#008080`.

   Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Apply]**.

   ![Festlegen der Linienfarbe](./assets/pb-elements-divider-settings-line-color.png){width="600" zoomable="yes"}

1. Geben Sie die **[!UICONTROL Line Thickness]** in Pixel.

1. Um die Maßeinheit anzugeben, geben Sie die **[!UICONTROL Line Width]** gefolgt von `px` oder `%`.

   ![Festlegen von Linienfarbe, -dicke und -breite](./assets/pb-elements-divider-settings-line-color-thickness-width.png){width="600" zoomable="yes"}

1. Aktualisieren Sie die _[!UICONTROL Advanced]_nach Bedarf.

   - Um die Positionierung des Trennzeichens im übergeordneten Container zu steuern, wählen Sie die **[!UICONTROL Alignment]**:

     | Option | Beschreibung |
     | ------ | ----------- |
     | `Default` | Wendet die Standardeinstellung für die Ausrichtung an, die im Stylesheet des aktuellen Designs angegeben ist. |
     | `Left` | Richtet die Liste am linken Rand des übergeordneten Containers aus, wobei der angegebene Abstand berücksichtigt wird. |
     | `Center` | Richtet die Liste in der Mitte des übergeordneten Containers aus, wobei der angegebene Abstand berücksichtigt wird. |
     | `Right` | Richtet den Block am rechten Rand des übergeordneten Containers aus, wobei der angegebene Abstand berücksichtigt wird. |

     {style="table-layout:auto"}

     Im folgenden Beispiel werden die Optionen so eingestellt, dass eine mittlere Ausrichtung für die Trennlinie verwendet wird.

     ![Trennlinie mit Mittelausrichtung](./assets/pb-elements-divider-settings-advanced-alignment-center.png){width="600" zoomable="yes"}

   - Legen Sie die **[!UICONTROL Border]** Stil, der auf alle vier Seiten des Trenncontainers angewendet wird:

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

     | Option | Beschreibung |
     | ------ |------------ |
     | [!UICONTROL Border Color] | Geben Sie die Farbe an, indem Sie ein Muster auswählen, auf die Farbauswahl klicken oder einen gültigen Farbnamen oder einen entsprechenden Hexadezimalwert eingeben. |
     | [!UICONTROL Border Width] | Geben Sie die Anzahl Pixel für die Rahmenlinienbreite an. |
     | [!UICONTROL Border Radius] | Geben Sie die Anzahl der Pixel an, um die die Größe des Radius definiert wird, mit dem die einzelnen Ecken des Rands gerundet werden. |

     {style="table-layout:auto"}

   - (Optional) Geben Sie die Namen von **[!UICONTROL CSS classes]** aus dem aktuellen Stylesheet, das auf den Container angewendet werden soll.

     Trennen Sie mehrere Klassennamen durch ein Leerzeichen.

   - Geben Sie Werte in Pixel für die **[!UICONTROL Margins and Padding]** um die äußeren Ränder und den inneren Abstand des Trennbehälters zu bestimmen.

     Geben Sie die entsprechenden Werte in das Diagramm ein.

     | Container-Bereich | Beschreibung |
     | -------------- | ----------- |
     | [!UICONTROL Margins] | Die Menge an leerem Raum, die auf den äußeren Rand aller Seiten des Containers angewendet wird. Optionen: `Top` / `Right` / `Bottom` / `Left` |
     | [!UICONTROL Padding] | Die Menge an leerem Raum, die auf den inneren Rand aller Seiten des Containers angewendet wird. Optionen: `Top` / `Right` / `Bottom` / `Left` |

     {style="table-layout:auto"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]** , um die Einstellungen anzuwenden und zum [!DNL Page Builder] Arbeitsbereich.

   ![In einer Zeile zentrierte Trennlinie](./assets/pb-elements-divider-settings-2px-centered.png){width="500" zoomable="yes"}

## Divider duplizieren

Für einen formatierten Divider mit bestimmten Einstellungen ist es effizienter, ein Duplikat zu erstellen, anstatt von vorn mit einem neuen Platzhalter zu beginnen.

1. Bewegen Sie den Mauszeiger über den Divider-Container, um die Toolbox anzuzeigen und die _Duplizieren_ ( ![Symbol &quot;Duplizieren&quot;](./assets/pb-icon-duplicate.png){width="20"} ).

   Der doppelte Divider-Container wird direkt unter dem Original angezeigt.

   ![Duplizierte Trennlinie](./assets/pb-elements-divider-duplicate.png){width="500" zoomable="yes"}

1. Bewegen Sie den Mauszeiger über den neuen Divider-Container, um die Toolbox anzuzeigen und die _Verschieben_ ( ![Symbol Verschieben](./assets/pb-icon-move.png){width="20"} ).

   ![Verschieben einer Trennlinie](./assets/pb-elements-divider-move.png){width="500" zoomable="yes"}

1. Wählen Sie die Trennlinie aus und ziehen Sie sie, bis die rote Führungslinie die neue Position markiert.

   Die oberen und unteren Ränder jedes Containers werden als gestrichelte Linien angezeigt, während der Divider verschoben wird.

   ![Duplizierte Trennlinie in Position verschieben](./assets/pb-elements-divider-move-guideline.png){width="500" zoomable="yes"}

[1]: https://en.wikipedia.org/wiki/Web_colors
