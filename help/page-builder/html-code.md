---
title: Elemente - HTML-Code
description: Erfahren Sie mehr über den Content-Typ HTML-Code , der zum Hinzufügen von Snippets von HTML-, CSS- und JavaScript-Code in der  [!DNL Page Builder] Bühne verwendet wird.
exl-id: b6e2dff5-ceac-4c7e-a87f-f95a542ada28
feature: Page Builder, Page Content
source-git-commit: 556394327a6eff9282acb09bdd16777dd3fee360
workflow-type: tm+mt
source-wordcount: '979'
ht-degree: 0%

---

# Elemente - HTML-Code

Verwenden Sie den Inhaltstyp _HTML-Code_ , um Snippets von HTML-, CSS- und JavaScript-Code in der [[!DNL Page Builder] Bühne](workspace.md#stage) hinzuzufügen. Sie können beispielsweise eine benutzerdefinierte HTML hinzufügen und eine CSS-Klasse deklarieren, die auf ein Seitenelement angewendet werden kann. Sie können auch einen Codeausschnitt für ein Logo, eine Schaltfläche oder ein Banner hinzufügen, das Sie von einem Drittanbieter erhalten haben.

## HTML-Code-Toolbox

![HTML-Code-Toolbox](./assets/pb-elements-html-code-toolbox.png){width="500" zoomable="yes"}

| Tool | Symbol | Beschreibung |
| --------- | ---------- | ----------------- |
| Verschieben | ![Symbol &quot;Verschieben&quot;](./assets/pb-icon-move.png){width="25"} | Verschiebt den HTML-Code-Container an eine andere gültige Position auf der Seite. |
| Einstellungen | ![Einstellungssymbol](./assets/pb-icon-settings.png){width="25"} | Öffnet die Seite HTML-Code bearbeiten , auf der Sie die Eigenschaften des Containers ändern können. |
| Ausblenden | ![Symbol zum Ausblenden](./assets/pb-icon-hide.png){width="25"} | Blendet den HTML-Code-Container aus. |
| Anzeigen | ![Symbol &quot;Anzeigen&quot;](./assets/pb-icon-show.png){width="25"} | Zeigt den ausgeblendeten HTML-Code-Container an. |
| Duplizieren | ![Symbol &quot;Duplizieren&quot;](./assets/pb-icon-duplicate.png){width="25"} | Kopiert den HTML-Code-Container. |
| Entfernen | ![Symbol &quot;Entfernen&quot;](./assets/pb-icon-remove.png){width="25"} | Löscht den HTML-Code-Container und seinen Inhalt aus der Phase. |

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## HTML-Code hinzufügen

Das folgende Beispiel zeigt, wie Sie den Code für [Google Font][1] einbetten und benutzerdefinierte Überschriftenklassen deklarieren, die das aktuelle Stylesheet überschreiben.

### Schritt 1: Auswählen einer Google-Schriftart

1. Besuchen Sie die Seite [Google Fonts][1] und wählen Sie die Schriftfamilie aus, die Sie verwenden möchten.

1. Kopieren Sie den generierten Code, der in den Abschnitt `<head>` der Seite eingebettet werden soll, und fügen Sie ihn vorübergehend in einen Texteditor ein.

   - Einbetten von Schriftcode
   - CSS-Regel

1. Fügen Sie die Schriftartregel zu jeder Überschriftenklasse hinzu und schließen Sie die Überschriftenklassen in ein `<style>` -Tag ein.

   Dieser Code wird in [!DNL Page Builder] eingefügt.

   ```html
   <style>
      h1 {color: teal; font-family: 'Khand', sans-serif; }
      h2 {color: teal; font-family: 'Khand', sans-serif; }
      h3 {color: teal; font-family: 'Khand', sans-serif; }
   </style>
   ```

### Schritt 2: Hinzufügen des Codes zur Seite

1. Wechseln Sie in der Seitenleiste _Admin_ Ihres Stores zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Suchen Sie die Seite, auf der die Schrift verfügbar sein soll, und öffnen Sie sie im Bearbeitungsmodus.

1. Scrollen Sie nach unten und erweitern Sie den Abschnitt **[!UICONTROL Content]** .

1. Erweitern Sie im Bedienfeld [!DNL Page Builder] den Eintrag **[!UICONTROL Elements]** und ziehen Sie einen Platzhalter **[!UICONTROL HTML Code]** auf eine Zeile, Spalte oder Registerkarte, die auf der Bühne festgelegt ist.

   Verwenden Sie die rote Führungslinie, um die Trennlinie entweder vor oder nach einem anderen Inhaltscontainer in der Zeile, Spalte oder Registerkartengruppe zu positionieren.

   ![Ziehen eines HTML-Code-Platzhalters auf die Bühne](./assets/pb-elements-html-code-drag.png){width="600" zoomable="yes"}

1. Bewegen Sie den Mauszeiger über den HTML-Container, um die Toolbox anzuzeigen, und wählen Sie das Symbol _Einstellungen_ ( ![Einstellungssymbol](./assets/pb-icon-settings.png){width="20"} ).

1. Fügen Sie in das Textfeld den von Ihnen vorbereiteten Code für Google-Schriftarten und Stildeklarationen ein.

   Um das Lesen zu vereinfachen, können Sie einige Leerzeichen zum Einzug des Codes eingeben.

   ![HTML-Code und -Stile](./assets/pb-elements-html-code-example.png){width="500" zoomable="yes"}

1. Aktualisieren Sie die restlichen Einstellungen nach Bedarf (weitere Informationen finden Sie unter [HTML-Codeeinstellungen ändern](#html-settings) ).

1. Klicken Sie oben rechts auf **[!UICONTROL Save]** , um die Einstellungen anzuwenden und zum Arbeitsbereich [!DNL Page Builder] zurückzukehren.

   Die neue Schriftart wird gerendert, wenn die Seite über einen Browser angezeigt wird.

### Schritt 3: Vorschau der Seite anzeigen

1. Setzen Sie im Abschnitt _[!UICONTROL Currently Active]_**[!UICONTROL Enable Page]**auf `Yes`.

   ![Aktivieren der Seite](./assets/pb-elements-html-code-enable-page.png){width="600" zoomable="yes"}

1. Klicken Sie in der oberen rechten Ecke auf den Pfeil **[!UICONTROL Save]** und wählen Sie **[!UICONTROL Save & Close]**.

1. Suchen Sie die Seite im Raster und wählen Sie **[!UICONTROL View]** in der Spalte _[!UICONTROL Actions]_aus.

   ![Anzeigen einer Vorschau der Seitenüberschriften mit der neuen Schriftfamilie](./assets/pb-elements-html-code-preview.png){width="700" zoomable="yes"}

## HTML-Codeeinstellungen ändern {#html-settings}

1. Bewegen Sie den Mauszeiger über den HTML-Container, um die Toolbox anzuzeigen, und wählen Sie das Symbol _Einstellungen_ ( ![Einstellungssymbol](./assets/pb-icon-settings.png){width="20"} ).

1. Bearbeiten Sie den Code im Textfeld nach Bedarf.

   HTML-, CSS- und JavaScript-Code werden unterstützt. Hier können Code-Snippets eingegeben werden, die zum Abschnitt &quot;`<head>`&quot;der Seite gehören.

   Der Editor bietet außerdem Schaltflächen zum Einfügen von Sonderelementen in den Code:

   | Schaltfläche | Beschreibung |
   | ------ | ----------- |
   | Widget einfügen.. | Klicken Sie auf , um ein Widget an der Cursorposition im Textfeld HTML einzufügen. |
   | Bild einfügen... | Klicken Sie auf , um ein hochgeladenes Bild oder ein Bild aus der Galerie an der Cursorposition im Textfeld HTML einzufügen. |
   | Variable einfügen.. | Klicken Sie auf , um eine Variable an der Cursorposition im Textfeld HTML einzufügen. |

1. Aktualisieren Sie die _[!UICONTROL Advanced]_-Einstellungen nach Bedarf.

   - Um die Positionierung des Codes innerhalb des übergeordneten Containers zu steuern, wählen Sie einen **[!UICONTROL Alignment]**:

     | Option | Beschreibung |
     | ------ | ----------- |
     | `Default` | Wendet die Standardeinstellung für die Ausrichtung an, die im Stylesheet des aktuellen Designs angegeben ist. |
     | `Left` | Richtet die Liste am linken Rand des übergeordneten Containers aus, wobei der angegebene Abstand berücksichtigt wird. |
     | `Center` | Richtet die Liste in der Mitte des übergeordneten Containers aus, wobei der angegebene Abstand berücksichtigt wird. |
     | `Right` | Richtet den Block am rechten Rand des übergeordneten Containers aus, wobei der angegebene Abstand berücksichtigt wird. |

     Im folgenden Beispiel werden die Optionen so eingestellt, dass eine mittlere Ausrichtung für den gerenderten Codeblock verwendet wird.

     ![Trennlinie mit Mittelausrichtung](./assets/pb-elements-divider-settings-advanced-alignment-center.png){width="600" zoomable="yes"}

   - Legen Sie den **[!UICONTROL Border]** -Stil fest, der auf alle vier Seiten des Code-Containers angewendet wird:

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

   - Wenn Sie einen anderen Rahmenstil als `None` festlegen, füllen Sie die Anzeigeoptionen für die Rahmenanzeige aus:

     | Option | Beschreibung |
     | ------ |------------ |
     | [!UICONTROL Border Color] | Geben Sie die Farbe an, indem Sie ein Muster auswählen, auf die Farbauswahl klicken oder einen gültigen Farbnamen oder einen entsprechenden Hexadezimalwert eingeben. |
     | [!UICONTROL Border Width] | Geben Sie die Anzahl Pixel für die Rahmenlinienbreite an. |
     | [!UICONTROL Border Radius] | Geben Sie die Anzahl der Pixel an, um die die Größe des Radius definiert wird, mit dem die einzelnen Ecken des Rands gerundet werden. |

     {style="table-layout:auto"}

   - (Optional) Geben Sie die Namen von **[!UICONTROL CSS classes]** aus dem aktuellen Stylesheet an, das auf den Container angewendet werden soll.

     Trennen Sie mehrere Klassennamen durch ein Leerzeichen.

   - Geben Sie Werte in Pixel für den Wert **[!UICONTROL Margins and Padding]** ein, um die äußeren Ränder und den inneren Abstand des Code-Containers zu bestimmen.

     Geben Sie die entsprechenden Werte in das Diagramm ein.

     | Container-Bereich | Beschreibung |
     | -------------- | ----------- |
     | [!UICONTROL Margins] | Die Menge an leerem Raum, die auf den äußeren Rand aller Seiten des Containers angewendet wird. Optionen: `Top` / `Right` / `Bottom` / `Left` |
     | [!UICONTROL Padding] | Die Menge an leerem Raum, die auf den inneren Rand aller Seiten des Containers angewendet wird. Optionen: `Top` / `Right` / `Bottom` / `Left` |

[1]: https://fonts.google.com/
