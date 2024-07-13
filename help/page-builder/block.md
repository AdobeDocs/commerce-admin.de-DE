---
title: Inhalt hinzufügen - Block
description: Erfahren Sie mehr über den Inhaltstyp Block , der zum Hinzufügen eines wiederverwendbaren Bausteins zur Phase [!DNL Page Builder] verwendet wird.
exl-id: fcedb125-e0c8-4b59-bd26-7f3912e0db2a
feature: Page Builder, Page Content
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 0%

---

# Inhalt hinzufügen - Block

Verwenden Sie den Inhaltstyp _Block_ , um einen vorhandenen, aktiven [Block](../content-design/blocks.md) zur [[!DNL Page Builder] Bühne](workspace.md#stage) hinzuzufügen. Im folgenden Beispiel enthält die erste Spalte den Block mit einem Seitenmenü für die Seite. Die zweite Spalte enthält ein Bild.

![Blockieren mit einem Seitenmenü](./assets/pb-add-content-block-example.png){width="600" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Block-Toolbox

| Tool | Symbol | Beschreibung |
| --------- | -------- | ------------- |
| Verschieben | ![Symbol &quot;Verschieben&quot;](./assets/pb-icon-move.png) | Verschiebt den Block-Container und seinen Inhalt an eine andere Position auf der Bühne. |
| Einstellungen | ![Einstellungssymbol](./assets/pb-icon-settings.png) | Öffnet die Seite Block bearbeiten , auf der Sie den Block auswählen und die Eigenschaften des Containers ändern können. |
| Ausblenden | ![Symbol zum Ausblenden](./assets/pb-icon-hide.png) | Blendet den aktuellen Block-Container und seinen Inhalt aus. |
| Anzeigen | ![Symbol &quot;Anzeigen&quot;](./assets/pb-icon-show.png) | Zeigt den ausgeblendeten Block-Container und seinen Inhalt an. |
| Duplizieren | ![Symbol &quot;Duplizieren&quot;](./assets/pb-icon-duplicate.png) | Kopiert den Block-Container und seinen Inhalt. |
| Entfernen | ![Symbol &quot;Entfernen&quot;](./assets/pb-icon-remove.png) | Löscht den Block-Container und seinen Inhalt aus der Bühne. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Vorhandenen Baustein hinzufügen

1. Navigieren Sie auf der Zielseite, dem Baustein, dem dynamischen Block, dem Produkt oder der Kategorie zum Arbeitsbereich &quot;[!DNL Page Builder]&quot;.

1. Erweitern Sie im Bedienfeld [!DNL Page Builder] den Wert **[!UICONTROL Add Content]** und ziehen Sie einen Platzhalter **[!UICONTROL Block]** auf die Bühne.

   ![Ziehen eines Blocks auf die Bühne](./assets/pb-add-content-block-drag.png){width="600" zoomable="yes"}

1. Bewegen Sie den Mauszeiger über den leeren Block-Container, um die Toolbox anzuzeigen und das Symbol _Einstellungen_ ( ![Einstellungssymbol](./assets/pb-icon-settings.png){width="25"} ) zu wählen.

1. Klicken Sie auf **[!UICONTROL Select Block]**.

   ![Auswählen eines Blocks](./assets/pb-add-content-block-select.png){width="200"}

1. Klicken Sie in der Zeile des Blocks, den Sie hinzufügen möchten, in der letzten Spalte auf **[!UICONTROL Select]** .

   ![Ausgewählter Block](./assets/pb-add-content-block-selected.png){width="600" zoomable="yes"}

   Der Name des ausgewählten Bausteins wird auf der Seite angezeigt.

   ![Blockname](./assets/pb-add-content-block-name.png){width="200"}

1. Nehmen Sie die restlichen Einstellungen wie gewünscht vor und verwenden Sie die Feldbeschreibungen am Ende dieser Seite, um sie zu referenzieren.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]** , um die Einstellungen anzuwenden und zum Arbeitsbereich [!DNL Page Builder] zurückzukehren.

### Erweiterte Einstellungen

1. Um die Positionierung des Blocks innerhalb des übergeordneten Containers zu steuern, wählen Sie einen **[!UICONTROL Alignment]**:

   | Option | Beschreibung |
   | ------ | ----------- |
   | `Default` | Wendet die Standardeinstellung für die Ausrichtung an, die im Stylesheet des aktuellen Designs angegeben ist. |
   | `Left` | Richtet die Liste am linken Rand des übergeordneten Containers aus, wobei der angegebene Abstand berücksichtigt wird. |
   | `Center` | Richtet die Liste in der Mitte des übergeordneten Containers aus, wobei der angegebene Abstand berücksichtigt wird. |
   | `Right` | Richtet den Block am rechten Rand des übergeordneten Containers aus, wobei der angegebene Abstand berücksichtigt wird. |

   {style="table-layout:auto"}

1. Legen Sie einen **[!UICONTROL Border]** -Stil fest, der auf alle vier Seiten des Block-Containers angewendet wird:

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

1. Wenn Sie einen anderen Rahmenstil als `None` festlegen, füllen Sie die Anzeigeoptionen für die Rahmenanzeige aus:

   | Option | Beschreibung |
   | ------ |------------ |
   | [!UICONTROL Border Color] | Geben Sie die Farbe an, indem Sie ein Muster auswählen, auf die Farbauswahl klicken oder einen gültigen Farbnamen oder einen entsprechenden Hexadezimalwert eingeben. |
   | [!UICONTROL Border Width] | Geben Sie die Anzahl Pixel für die Rahmenlinienbreite an. |
   | [!UICONTROL Border Radius] | Geben Sie die Anzahl der Pixel an, um die die Größe des Radius definiert wird, mit dem die einzelnen Ecken des Rands gerundet werden. |

   {style="table-layout:auto"}

1. (Optional) Geben Sie die Namen von **[!UICONTROL CSS classes]** aus dem aktuellen Stylesheet an, das auf den Container angewendet werden soll.

   Trennen Sie mehrere Klassennamen durch ein Leerzeichen.

1. Geben Sie Werte in Pixel für den Wert **[!UICONTROL Margins and Padding]** ein, um die äußeren Ränder und den inneren Abstand des Block-Containers zu bestimmen.

   Geben Sie die entsprechenden Werte in das Diagramm ein.

   | Container-Bereich | Beschreibung |
   | -------------- | ----------- |
   | [!UICONTROL Margins] | Die Menge an leerem Raum, die auf den äußeren Rand aller Seiten des Containers angewendet wird. Optionen: `Top` / `Right` / `Bottom` / `Left` |
   | [!UICONTROL Padding] | Die Menge an leerem Raum, die auf den inneren Rand aller Seiten des Containers angewendet wird. Optionen: `Top` / `Right` / `Bottom` / `Left` |

   {style="table-layout:auto"}

## Blockeinstellungen bearbeiten

1. Bewegen Sie den Mauszeiger über den Block-Container und wählen Sie in der Toolbox das Symbol _Einstellungen_ ( ![Einstellungssymbol](./assets/pb-icon-settings.png){width="25"} ).

   ![Block Toolbox](./assets/pb-add-content-block-toolbox.png){width="600" zoomable="yes"}

1. Um einen anderen Block auszuwählen, klicken Sie auf **[!UICONTROL Select Block]**.

   - Klicken Sie in der Liste der aktiven Bausteine auf den Block &quot;**[!UICONTROL Select]**&quot;, den Sie hinzufügen möchten.
   - Klicken Sie auf **[!UICONTROL Add Selected]**.

1. Aktualisieren Sie die restlichen Einstellungen nach Bedarf mithilfe der Feldbeschreibungen am Ende dieser Seite, um sie zu referenzieren.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]** , um die Einstellungen anzuwenden und zum Arbeitsbereich [!DNL Page Builder] zurückzukehren.

## Baustein duplizieren

1. Bewegen Sie den Mauszeiger über den Block-Container, um die Symbolleiste anzuzeigen, und wählen Sie das Symbol _Duplizieren_ (![Symbol Duplizieren](./assets/pb-icon-duplicate.png)).

   Das Duplikat wird direkt unter dem Original angezeigt.

1. Um den neuen Block an eine neue Position zu verschieben, bewegen Sie den Mauszeiger über den Container und klicken Sie dann in der Toolbox auf _Verschieben_ (![Verschieben-Symbol](./assets/pb-icon-move.png)).

1. Wählen Sie den Block aus und ziehen Sie ihn, bis die rote Führungslinie an der neuen Position angezeigt wird.

   Die oberen und unteren Ränder jedes Containers werden beim Verschieben des Blocks als gestrichelte Linien angezeigt.

## Entfernen eines Bausteins aus der Bühne

1. Bewegen Sie den Mauszeiger über den Block-Container, um die Toolbox anzuzeigen, und wählen Sie das Symbol _Entfernen_ (![Symbol &quot;Entfernen&quot;](./assets/pb-icon-remove.png)).

1. Klicken Sie bei Aufforderung zur Bestätigung auf **[!UICONTROL OK]**.
