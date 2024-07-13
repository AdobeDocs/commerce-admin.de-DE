---
title: Elemente - Text
description: Erfahren Sie mehr über den Inhaltstyp "Text", der zum Hinzufügen eines Textcontainers in der  [!DNL Page Builder] Bühne verwendet wird.
exl-id: 3f14af35-9c04-4f4b-b3dd-d3406d56a9c0
feature: Page Builder, Page Content
source-git-commit: 79dc16dcba239af12793813ae19636bbd7ec49c5
workflow-type: tm+mt
source-wordcount: '945'
ht-degree: 0%

---

# Elemente - Text

Verwenden Sie den Inhaltstyp _Text_ , um einen Textcontainer mit einem WYSIWYG-Editor (&quot;What You See Is What You Get&quot;) in der [[!DNL Page Builder] Bühne](workspace.md#stage) hinzuzufügen. Darüber hinaus können Sie dem Text über die Editor-Symbolleiste Links, Bilder, [Variablen](../systems/variables-predefined.md) und Widgets hinzufügen.

![Formatierter Text auf einem Banner](./assets/pb-storefont-banner-with-button.png){width="700"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Texteditor-Tools

Sie können auf den Texteditor direkt von der Bühne oder von einer Einstellungsseite aus zugreifen. Änderungen, die direkt an der Bühne vorgenommen werden, werden automatisch gespeichert. Weitere Informationen finden Sie unter [Verwenden des Editors](../content-design/editor.md).

![Text-Editor-Tool - TinyMCE](./assets/pb-elements-text-editor-tools.png){width="600"}

## Textcontainer-Toolbox

![Textcontainer-Toolbox](./assets/pb-elements-text-toolbox.png){width="600"}

| Tool | Symbol | Beschreibung |
| --------- | --------------------- | -------------- |
| Verschieben | ![Symbol &quot;Verschieben&quot;](./assets/pb-icon-move.png){width="25"} | Verschiebt den Text-Container an eine andere gültige Position auf der Seite. |
| (Titel) | TEXT | Identifiziert den aktuellen Container als Textelement. |
| Einstellungen | ![Einstellungssymbol](./assets/pb-icon-settings.png){width="25"} | Öffnet die Eigenschaften des Textcontainers im Bearbeitungsmodus. |
| Ausblenden | ![Symbol zum Ausblenden](./assets/pb-icon-hide.png){width="25"} | Blendet den Textcontainer aus. |
| Anzeigen | ![Symbol &quot;Anzeigen&quot;](./assets/pb-icon-show.png){width="25"} | Zeigt den ausgeblendeten Textcontainer an. |
| Duplizieren | ![Symbol &quot;Duplizieren&quot;](./assets/pb-icon-duplicate.png){width="25"} | Kopiert den Textcontainer. |
| Entfernen | ![Symbol &quot;Entfernen&quot;](./assets/pb-icon-remove.png){width="25"} | Löscht den Text-Container und seinen Inhalt aus der Bühne. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Text hinzufügen

1. Erweitern Sie im Bedienfeld [!DNL Page Builder] den Eintrag **[!UICONTROL Elements]** und ziehen Sie einen Platzhalter **[!UICONTROL Text]** auf eine Zeile, Spalte oder Registerkarte, die auf der Bühne festgelegt ist.

   ![Ziehen eines Text-Platzhalters auf die Bühne](./assets/pb-elements-text-drag.png){width="600" zoomable="yes"}

1. Verwenden Sie den Editor, um Text nach Bedarf einzugeben und zu formatieren.

   Weitere Informationen finden Sie unter [Verwenden des Editors](../content-design/editor.md).

   ![Texteditor mit Inhalt](./assets/pb-elements-text-editor.png){width="600"}

## Erstellen eines Links

Die Schaltfläche Link einfügen im Editor erleichtert das Hinzufügen eines Hyperlinks zu einem Bild in der Galerie. Sie kann jedoch auch verwendet werden, um einen Inline-Link im Text zu erstellen, wenn Sie die URL im Voraus haben. Im Gegensatz zur Schaltfläche Widget ist die Schaltfläche Link einfügen/bearbeiten nicht mit Seiten, Produkten oder Kategorien im Store integriert.

Informationen zum Erstellen eines Links für eine Telefonnummer oder E-Mail finden Sie unter [Hinzufügen benutzerdefinierter Variablen](../systems/variables-custom.md).

1. Navigieren Sie in der Storefront zu der Seite, die das Ziel des Links sein soll, und kopieren Sie die Link-Informationen.

   Sie können entweder die vollständig qualifizierte URL oder eine relative URL verwenden, die den Verweis auf Ihre Store-Domäne weglässt.

   Vollständige URL - `https://mystore.com/women/tops-women/tees-women.html`

   Relative URL - `../women/tops-women/tees-women.html`

1. Wählen Sie den Text im Editor-Bereich aus und klicken Sie in der Editor-Symbolleiste auf _Link einfügen/bearbeiten_ ( ![Link-Schaltfläche einfügen/bearbeiten](./assets/pb-icon-add-link.png){width="20"} ).

   ![Hinzufügen eines Links zu formatiertem Text](./assets/pb-tutorial2-column-text-editor-link-insert.png){width="500" zoomable="yes"}

1. Geben Sie für &quot;**[!UICONTROL URL]**&quot;den relativen Link ein, den Sie vorbereitet haben.

1. Setzen Sie **[!UICONTROL Target]** auf `None`.

   Mit dieser Einstellung wird die Seite im selben Browserfenster geöffnet, anstatt eine neue Registerkarte zu öffnen.

1. Geben Sie für **[!UICONTROL Title]** den Wert `Shop Tees` ein.

   Das Link-Attribut `Title` wird von einigen Browsern als QuickInfo verwendet.

1. Um den Link zu speichern und zum Arbeitsbereich [!DNL Page Builder] zurückzukehren, klicken Sie auf **[!UICONTROL OK]**.

   ![Link-Detail](./assets/pb-tutorial2-column-text-editor-link-insert-detail.png){width="500" zoomable="yes"}

## Bild einfügen

1. Platzieren Sie den Cursor in den Text, an dem Sie das Bild einfügen möchten.

1. Klicken Sie in der Editor-Symbolleiste auf _Bild einfügen/bearbeiten_ ( ![Schaltfläche Bild einfügen/bearbeiten](./assets/icon-pb-add-image.png){width="20"} ).

1. Klicken Sie für &quot;**[!UICONTROL Source]**&quot;auf das Suchsymbol, um den Medienspeicher zum Suchen und Auswählen eines Bildes zu verwenden.

1. Geben Sie für &quot;**[!UICONTROL Image Description]**&quot;beschreibenden Text für das Bild ein.

   Dieser Text füllt das Link-Attribut `alt` für das Bild und wird von einigen Browsern für die Barrierefreiheit verwendet.

1. Geben Sie die Breite und Höhe **[!UICONTROL Dimensions]** in Pixel für das Rendern des Bildes auf der Seite ein.

   Behalten Sie das Kontrollkästchen **[!UICONTROL Constrain proportions]** bei, um das Seitenverhältnis für das Bild automatisch beizubehalten.

1. Um das Bild einzufügen und dann zum Arbeitsbereich [!DNL Page Builder] zurückzukehren, klicken Sie auf **[!UICONTROL OK]**.

## Texteinstellungen ändern

1. Bewegen Sie den Mauszeiger über den Textcontainer, um die Toolbox anzuzeigen, und wählen Sie das Symbol _Einstellungen_ ( ![Einstellungssymbol](./assets/pb-icon-settings.png){width="20"} ).

   >[!NOTE]
   >
   >Da der Textcontainer in einem anderen Container eng verschachtelt ist, stellen Sie sicher, dass Sie über die richtige Toolbox verfügen.

1. Aktualisieren Sie den Inhalt nach Bedarf.

1. Aktualisieren Sie die _[!UICONTROL Advanced]_-Einstellungen nach Bedarf.

   - Um die Positionierung des Texts innerhalb des übergeordneten Containers zu steuern, wählen Sie einen **[!UICONTROL Alignment]**:

     | Option | Beschreibung |
     | ------ |------------ |
     | `Default` | Wendet die Standardeinstellung für die Ausrichtung an, die im Stylesheet des aktuellen Designs angegeben ist. |
     | `Left` | Richtet die Liste am linken Rand des übergeordneten Containers aus, wobei der angegebene Abstand berücksichtigt wird. |
     | `Center` | Richtet die Liste in der Mitte des übergeordneten Containers aus, wobei der angegebene Abstand berücksichtigt wird. |
     | `Right` | Richtet den Block am rechten Rand des übergeordneten Containers aus, wobei der angegebene Abstand berücksichtigt wird. |

     {style="table-layout:auto"}

   - Legen Sie den **[!UICONTROL Border]** -Stil fest, der auf alle vier Seiten des Textcontainers angewendet wird:

     | Option | Beschreibung |
     | ------ |------------ |
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

   - Wenn Sie einen anderen Rahmenstil als `None` festlegen, füllen Sie die Anzeigeoptionen für die Rahmenanzeige aus:

     | Option | Beschreibung |
     | ------ |------------ |
     | [!UICONTROL Border Color] | Geben Sie die Farbe an, indem Sie ein Muster auswählen, auf die Farbauswahl klicken oder einen gültigen Farbnamen oder einen entsprechenden Hexadezimalwert eingeben. |
     | [!UICONTROL Border Width] | Geben Sie die Anzahl Pixel für die Rahmenlinienbreite an. |
     | [!UICONTROL Border Radius] | Geben Sie die Anzahl der Pixel an, um die die Größe des Radius definiert wird, mit dem die einzelnen Ecken des Rands gerundet werden. |

     {style="table-layout:auto"}

   - (Optional) Geben Sie die Namen von **[!UICONTROL CSS classes]** aus dem aktuellen Stylesheet an, das auf den Container angewendet werden soll.

     Trennen Sie mehrere Klassennamen durch ein Leerzeichen.

   - Geben Sie Werte in Pixel für den Wert **[!UICONTROL Margins and Padding]** ein, um die äußeren Ränder und den inneren Abstand des Textcontainers zu bestimmen.

     Geben Sie die entsprechenden Werte in das Diagramm ein.

     | Container-Bereich | Beschreibung |
     | -------------- |------------ |
     | [!UICONTROL Margins] | Die Menge an leerem Raum, die auf den äußeren Rand aller Seiten des Containers angewendet wird. Optionen: `Top` / `Right` / `Bottom` / `Left` |
     | [!UICONTROL Padding] | Die Menge an leerem Raum, die auf den inneren Rand aller Seiten des Containers angewendet wird. Optionen: `Top` / `Right` / `Bottom` / `Left` |

     {style="table-layout:auto"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]** , um die Einstellungen anzuwenden und zum Arbeitsbereich [!DNL Page Builder] zurückzukehren.
