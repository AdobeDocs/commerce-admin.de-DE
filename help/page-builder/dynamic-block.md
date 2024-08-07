---
title: Inhalt hinzufügen - Dynamischer Block
description: Erfahren Sie mehr über den Inhaltstyp "Dynamischer Block", der zum Hinzufügen eines wiederverwendbaren dynamischen Bausteins zur  [!DNL Page Builder] Bühne verwendet wird.
exl-id: 04c90f47-9e32-4d34-ac0d-a2f2cec95ffc
feature: Page Builder, Page Content
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '828'
ht-degree: 0%

---

# Inhalt hinzufügen - Dynamischer Block

Verwenden Sie den Inhaltstyp &quot;Dynamischer Block&quot;, um einen vorhandenen [dynamischen Block](../content-design/dynamic-blocks.md) zur [[!DNL Page Builder] Bühne](workspace.md#stage) hinzuzufügen.

![Dynamischer Block auf der Storefront](./assets/pb-tutorial2-dynamic-block-storefront.png){width="700" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Dynamic Block-Toolbox

| Tool | Symbol | Beschreibung |
| --------- | ------------- | ----------------- |
| Verschieben | ![Symbol &quot;Verschieben&quot;](./assets/pb-icon-move.png){width="25"} | Verschiebt den Block-Container und seinen Inhalt an eine andere Position auf der Bühne. |
| Einstellungen | ![Einstellungssymbol](./assets/pb-icon-settings.png){width="25"} | Öffnet die Seite _Block bearbeiten_ , auf der Sie den Block auswählen und die Eigenschaften des Containers ändern können. |
| Ausblenden | ![Symbol zum Ausblenden](./assets/pb-icon-hide.png){width="25"} | Blendet den aktuellen Block-Container und seinen Inhalt aus. |
| Anzeigen | ![Symbol &quot;Anzeigen&quot;](./assets/pb-icon-show.png){width="25"} | Zeigt den ausgeblendeten Block-Container und seinen Inhalt an. |
| Duplizieren | ![Symbol &quot;Duplizieren&quot;](./assets/pb-icon-duplicate.png){width="25"} | Kopiert den Block-Container und seinen Inhalt. |
| Entfernen | ![Symbol &quot;Entfernen&quot;](./assets/pb-icon-remove.png){width="25"} | Löscht den Block-Container und seinen Inhalt aus der Bühne. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Hinzufügen eines vorhandenen dynamischen Blocks zur Bühne

1. Navigieren Sie auf der Zielseite, dem Baustein, dem Produkt oder der Kategorie zum Arbeitsbereich &quot;[!DNL Page Builder]&quot;.

1. Erweitern Sie im Bedienfeld [!DNL Page Builder] den Wert **[!UICONTROL Add Content]** und ziehen Sie einen Platzhalter **[!UICONTROL Dynamic Block]** auf die Bühne.

   ![Ziehen eines dynamischen Block-Platzhalters auf die Bühne](./assets/pb-dynamic-block-drag.png){width="600" zoomable="yes"}

1. Bewegen Sie den Mauszeiger über den leeren Container mit dynamischen Bausteinen, um die Toolbox anzuzeigen und das Symbol _Einstellungen_ ( ![Einstellungssymbol](./assets/pb-icon-settings.png){width="20"} ) zu wählen.

   ![Dynamic Block toolbox](./assets/pb-dynamic-block-settings.png){width="600" zoomable="yes"}

1. Klicken Sie auf der Seite _Dynamischen Block bearbeiten_ auf **[!UICONTROL Select Dynamic Block]** und wählen Sie den Block mithilfe der Liste aus.

   ![Dynamischen Block auswählen](./assets/pb-dynamic-block-select.png){width="600" zoomable="yes"}

   Suchen Sie in der Liste den dynamischen Baustein, den Sie einfügen möchten, und klicken Sie auf **[!UICONTROL Select]**. Klicken Sie dann auf **[!UICONTROL Add Selected]**.

   ![Dynamischen Baustein in der Liste auswählen](./assets/pb-add-content-dynamic-block-select-list.png){width="600" zoomable="yes"}

   Nachfolgend finden Sie eine Zusammenfassung der dynamischen Blockinformationen.

   ![Zusammenfassung dynamischer Blöcke](./assets/pb-add-content-dynamic-block-summary.png){width="600" zoomable="yes"}

1. Setzen Sie **[!UICONTROL Template]** auf einen der folgenden Werte:

   | Option | Beschreibung |
   | ------ | ----------- |
   | `Dynamic Block Block Template` | Fügt einen eigenständigen Block hinzu. |
   | `Dynamic Block Inline Template` | Fügt den Blockinhalt in Text ein. |

   {style="table-layout:auto"}

   ![Vorlage für dynamische Bausteine](./assets/pb-add-content-dynamic-block-template.png){width="200"}

1. Nehmen Sie die erweiterten Einstellungen nach Bedarf vor.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]** , um die Einstellungen anzuwenden und zum Arbeitsbereich [!DNL Page Builder] zurückzukehren.

### Erweiterte Einstellungen

1. Um die Positionierung des dynamischen Blocks innerhalb des übergeordneten Containers zu steuern, wählen Sie einen **[!UICONTROL Alignment]**:

   | Option | Beschreibung |
   | ------ | ----------- |
   | `Default` | Wendet die Standardeinstellung für die Ausrichtung an, die im Stylesheet des aktuellen Designs angegeben ist. |
   | `Left` | Richtet die Liste am linken Rand des übergeordneten Containers aus, wobei der angegebene Abstand berücksichtigt wird. |
   | `Center` | Richtet die Liste in der Mitte des übergeordneten Containers aus, wobei der angegebene Abstand berücksichtigt wird. |
   | `Right` | Richtet den Block am rechten Rand des übergeordneten Containers aus, wobei der angegebene Abstand berücksichtigt wird. |

   {style="table-layout:auto"}

1. Legen Sie den **[!UICONTROL Border]** -Stil fest, der auf alle vier Seiten des dynamischen Block-Containers angewendet wird:

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

1. Geben Sie Werte in Pixel für den Wert **[!UICONTROL Margins and Padding]** ein, um die äußeren Ränder und den inneren Abstand des dynamischen Block-Containers zu bestimmen.

   Geben Sie die entsprechenden Werte in das Diagramm ein.

   | Container-Bereich | Beschreibung |
   | -------------- | ----------- |
   | [!UICONTROL Margins] | Die Menge an leerem Raum, die auf den äußeren Rand aller Seiten des Containers angewendet wird. Optionen: `Top` / `Right` / `Bottom` / `Left` |
   | [!UICONTROL Padding] | Die Menge an leerem Raum, die auf den inneren Rand aller Seiten des Containers angewendet wird. Optionen: `Top` / `Right` / `Bottom` / `Left` |

   {style="table-layout:auto"}

## Einstellungen für dynamische Blockcontainer bearbeiten

1. Bewegen Sie den Mauszeiger über den dynamischen Block-Container, um die Toolbox anzuzeigen und das Symbol _Einstellungen_ ( ![Einstellungssymbol](./assets/pb-icon-settings.png){width="20"} ) zu wählen.

   ![Dynamic Block toolbox](./assets/pb-add-content-dynamic-block-toolbox.png){width="500" zoomable="yes"}

1. Ändern Sie bei Bedarf den dynamischen Baustein:

   - Klicken Sie auf **[!UICONTROL Select Dynamic Block]**.

     ![Auswählen eines weiteren dynamischen Blocks](./assets/pb-add-content-dynamic-block-select.png){width="20"}

   - Klicken Sie in der Liste der aktiven dynamischen Blöcke für den hinzuzufügenden Block auf **[!UICONTROL Select]** .

1. Aktualisieren Sie die restlichen Einstellungen nach Bedarf.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]** , um die Einstellungen anzuwenden und zum Arbeitsbereich [!DNL Page Builder] zurückzukehren.

## Dynamischen Block duplizieren

1. Bewegen Sie den Mauszeiger über den dynamischen Block-Container, um die Symbolleiste anzuzeigen, und wählen Sie das Symbol _Duplizieren_ ( ![Duplizieren-Symbol](./assets/pb-icon-duplicate.png){width="20"} ).

   Das Duplikat wird direkt unter dem Original angezeigt.

   ![Dynamischen Block duplizieren](./assets/pb-add-content-dynamic-block-duplicate.png){width="500" zoomable="yes"}

1. Um den neuen dynamischen Block an eine andere Position zu verschieben, bewegen Sie den Mauszeiger über den Container und wählen Sie dann in der Toolbox _Verschieben_ ( ![Verschieben-Symbol](./assets/pb-icon-move.png){width="20"} ).

1. Wählen Sie den dynamischen Block aus und ziehen Sie ihn, bis die rote Führungslinie an der neuen Position angezeigt wird.

   Die oberen und unteren Ränder jedes Containers werden als gestrichelte Linien angezeigt, während der dynamische Block verschoben wird.

## Dynamischen Baustein aus der Bühne entfernen

1. Bewegen Sie den Mauszeiger über den dynamischen Block-Container, um die Toolbox anzuzeigen, und wählen Sie das Symbol _Entfernen_ ( ![Symbol Entfernen](./assets/pb-icon-remove.png){width="20"} ).

1. Klicken Sie bei Aufforderung zur Bestätigung auf **[!UICONTROL OK]**.
