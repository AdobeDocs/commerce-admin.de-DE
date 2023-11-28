---
title: Elemente - Text
description: Erfahren Sie mehr über den Inhaltstyp "Text", der zum Hinzufügen eines Textcontainers im [!DNL Page Builder] Bühne.
exl-id: 3f14af35-9c04-4f4b-b3dd-d3406d56a9c0
feature: Page Builder, Page Content
source-git-commit: 79dc16dcba239af12793813ae19636bbd7ec49c5
workflow-type: tm+mt
source-wordcount: '945'
ht-degree: 0%

---

# Elemente - Text

Verwenden Sie die _Text_ Inhaltstyp zum Hinzufügen eines Textcontainers mit einem WYSIWYG-Editor (&quot;What You See Is What You Get&quot;) im [[!DNL Page Builder] Schritt](workspace.md#stage). Darüber hinaus können Sie Links, Bilder, [variables](../systems/variables-predefined.md)und Widgets zum Text in der Editor-Symbolleiste.

![Formatierter Text auf einem Banner](./assets/pb-storefont-banner-with-button.png){width="700"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Texteditor-Tools

Sie können auf den Texteditor direkt von der Bühne oder von einer Einstellungsseite aus zugreifen. Änderungen, die direkt an der Bühne vorgenommen werden, werden automatisch gespeichert. Weitere Informationen finden Sie unter [Verwenden des Editors](../content-design/editor.md).

![Texteditor-Tool - TinyMCE](./assets/pb-elements-text-editor-tools.png){width="600"}

## Textcontainer-Toolbox

![Textcontainer-Toolbox](./assets/pb-elements-text-toolbox.png){width="600"}

| Tool | Symbol | Beschreibung |
| --------- | --------------------- | -------------- |
| Verschieben | ![Symbol Verschieben](./assets/pb-icon-move.png){width="25"} | Verschiebt den Text-Container an eine andere gültige Position auf der Seite. |
| (Titel) | TEXT | Identifiziert den aktuellen Container als Textelement. |
| Einstellungen | ![Symbol Einstellungen](./assets/pb-icon-settings.png){width="25"} | Öffnet die Eigenschaften des Textcontainers im Bearbeitungsmodus. |
| Ausblenden | ![Symbol &quot;Ausblenden&quot;](./assets/pb-icon-hide.png){width="25"} | Blendet den Textcontainer aus. |
| Anzeigen | ![Symbol &quot;Anzeigen&quot;](./assets/pb-icon-show.png){width="25"} | Zeigt den ausgeblendeten Textcontainer an. |
| Duplizieren | ![Symbol &quot;Duplizieren&quot;](./assets/pb-icon-duplicate.png){width="25"} | Kopiert den Textcontainer. |
| Entfernen | ![Symbol &quot;Entfernen&quot;](./assets/pb-icon-remove.png){width="25"} | Löscht den Text-Container und seinen Inhalt aus der Bühne. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Text hinzufügen

1. Im [!DNL Page Builder] Bedienfeld, erweitern **[!UICONTROL Elements]** und ziehen Sie eine **[!UICONTROL Text]** Platzhalter für eine Zeile, Spalte oder Registerkarte, die auf der Bühne festgelegt ist.

   ![Ziehen eines Text-Platzhalters auf die Bühne](./assets/pb-elements-text-drag.png){width="600" zoomable="yes"}

1. Verwenden Sie den Editor, um Text nach Bedarf einzugeben und zu formatieren.

   Weitere Informationen finden Sie unter [Verwenden des Editors](../content-design/editor.md).

   ![Texteditor mit Inhalt](./assets/pb-elements-text-editor.png){width="600"}

## Link erstellen

Die Schaltfläche Link einfügen im Editor erleichtert das Hinzufügen eines Hyperlinks zu einem Bild in der Galerie. Sie kann jedoch auch verwendet werden, um einen Inline-Link im Text zu erstellen, wenn Sie die URL im Voraus haben. Im Gegensatz zur Schaltfläche Widget ist die Schaltfläche Link einfügen/bearbeiten nicht mit Seiten, Produkten oder Kategorien im Store integriert.

Informationen zum Erstellen eines Links für eine Telefonnummer oder E-Mail-Adresse finden Sie unter [Hinzufügen benutzerdefinierter Variablen](../systems/variables-custom.md).

1. Navigieren Sie in der Storefront zu der Seite, die das Ziel des Links sein soll, und kopieren Sie die Link-Informationen.

   Sie können entweder die vollständig qualifizierte URL oder eine relative URL verwenden, die den Verweis auf Ihre Store-Domäne weglässt.

   Vollständige URL - `https://mystore.com/women/tops-women/tees-women.html`

   Relative URL - `../women/tops-women/tees-women.html`

1. Wählen Sie den Text im Editor aus und klicken Sie auf _Link einfügen/bearbeiten_ ( ![Schaltfläche &quot;Link einfügen/bearbeiten&quot;](./assets/pb-icon-add-link.png){width="20"} ) in der Editor-Symbolleiste.

   ![Link zu formatiertem Text hinzufügen](./assets/pb-tutorial2-column-text-editor-link-insert.png){width="500" zoomable="yes"}

1. Für **[!UICONTROL URL]**, geben Sie den von Ihnen vorbereiteten relativen Link ein.

1. Satz **[!UICONTROL Target]** nach `None`.

   Mit dieser Einstellung wird die Seite im selben Browserfenster geöffnet, anstatt eine neue Registerkarte zu öffnen.

1. Für **[!UICONTROL Title]**, eingeben `Shop Tees`.

   Die `Title` Das Link-Attribut wird von einigen Browsern als QuickInfo verwendet.

1. So speichern Sie den Link und kehren zur [!DNL Page Builder] Arbeitsbereich, klicken Sie auf **[!UICONTROL OK]**.

   ![Link-Detail](./assets/pb-tutorial2-column-text-editor-link-insert-detail.png){width="500" zoomable="yes"}

## Bild einfügen

1. Platzieren Sie den Cursor in den Text, an dem Sie das Bild einfügen möchten.

1. Klicks _Bild einfügen/bearbeiten_ ( ![Schaltfläche &quot;Bild einfügen/bearbeiten&quot;](./assets/icon-pb-add-image.png){width="20"} ) in der Editor-Symbolleiste.

1. Für **[!UICONTROL Source]** klicken Sie auf das Suchsymbol, um den Medienspeicher zum Suchen und Auswählen eines Bildes zu verwenden.

1. Für **[!UICONTROL Image Description]**, geben Sie einen beschreibenden Text für das Bild ein.

   Dieser Text füllt die `alt` Link-Attribut für das Bild und wird von einigen Browsern für die Barrierefreiheit verwendet.

1. Breite und Höhe eingeben **[!UICONTROL Dimensions]**, in Pixel, zum Rendern des Bildes auf der Seite.

   Behalten Sie die **[!UICONTROL Constrain proportions]** aktivieren, um das Seitenverhältnis für das Bild automatisch beizubehalten.

1. So fügen Sie das Bild ein und kehren dann zum [!DNL Page Builder] Arbeitsbereich, klicken Sie auf **[!UICONTROL OK]**.

## Texteinstellungen ändern

1. Bewegen Sie den Mauszeiger über den Textcontainer, um die Toolbox anzuzeigen und die _Einstellungen_ ( ![Symbol Einstellungen](./assets/pb-icon-settings.png){width="20"} ).

   >[!NOTE]
   >
   >Da der Textcontainer in einem anderen Container eng verschachtelt ist, stellen Sie sicher, dass Sie über die richtige Toolbox verfügen.

1. Aktualisieren Sie den Inhalt nach Bedarf.

1. Aktualisieren Sie die _[!UICONTROL Advanced]_nach Bedarf.

   - Um die Positionierung des Texts innerhalb des übergeordneten Containers zu steuern, wählen Sie eine **[!UICONTROL Alignment]**:

     | Option | Beschreibung |
     | ------ |------------ |
     | `Default` | Wendet die Standardeinstellung für die Ausrichtung an, die im Stylesheet des aktuellen Designs angegeben ist. |
     | `Left` | Richtet die Liste am linken Rand des übergeordneten Containers aus, wobei der angegebene Abstand berücksichtigt wird. |
     | `Center` | Richtet die Liste in der Mitte des übergeordneten Containers aus, wobei der angegebene Abstand berücksichtigt wird. |
     | `Right` | Richtet den Block am rechten Rand des übergeordneten Containers aus, wobei der angegebene Abstand berücksichtigt wird. |

     {style="table-layout:auto"}

   - Legen Sie die **[!UICONTROL Border]** -Stil, der auf alle vier Seiten des Textcontainers angewendet wird:

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

   - Wenn Sie einen anderen Rahmenstil als `None`, füllen Sie die Randanzeigeoptionen aus:

     | Option | Beschreibung |
     | ------ |------------ |
     | [!UICONTROL Border Color] | Geben Sie die Farbe an, indem Sie ein Muster auswählen, auf die Farbauswahl klicken oder einen gültigen Farbnamen oder einen entsprechenden Hexadezimalwert eingeben. |
     | [!UICONTROL Border Width] | Geben Sie die Anzahl Pixel für die Rahmenlinienbreite an. |
     | [!UICONTROL Border Radius] | Geben Sie die Anzahl der Pixel an, um die die Größe des Radius definiert wird, mit dem die einzelnen Ecken des Rands gerundet werden. |

     {style="table-layout:auto"}

   - (Optional) Geben Sie die Namen von **[!UICONTROL CSS classes]** aus dem aktuellen Stylesheet, das auf den Container angewendet werden soll.

     Trennen Sie mehrere Klassennamen durch ein Leerzeichen.

   - Geben Sie Werte in Pixel für die **[!UICONTROL Margins and Padding]** um die äußeren Ränder und den inneren Abstand des Textcontainers zu bestimmen.

     Geben Sie die entsprechenden Werte in das Diagramm ein.

     | Container-Bereich | Beschreibung |
     | -------------- |------------ |
     | [!UICONTROL Margins] | Die Menge an leerem Raum, die auf den äußeren Rand aller Seiten des Containers angewendet wird. Optionen: `Top` / `Right` / `Bottom` / `Left` |
     | [!UICONTROL Padding] | Die Menge an leerem Raum, die auf den inneren Rand aller Seiten des Containers angewendet wird. Optionen: `Top` / `Right` / `Bottom` / `Left` |

     {style="table-layout:auto"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]** , um die Einstellungen anzuwenden und zum [!DNL Page Builder] Arbeitsbereich.
