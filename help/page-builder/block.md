---
title: Inhalt hinzufügen - Block
description: Erfahren Sie mehr über den Inhaltsbaustein, der zum Hinzufügen eines wiederverwendbaren Blocks zum  [!DNL Page Builder]  verwendet wird.
exl-id: fcedb125-e0c8-4b59-bd26-7f3912e0db2a
feature: Page Builder, Page Content
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 0%

---

# Inhalt hinzufügen - Block

Verwenden Sie den _Block_-Inhaltstyp, um einen vorhandenen, aktiven [Block](../content-design/blocks.md) zur [[!DNL Page Builder] Phase](workspace.md#stage) hinzuzufügen. Im folgenden Beispiel enthält die erste Spalte den Block mit einem Seitenmenü für die Seite. Die zweite Spalte enthält ein Bild.

![Block mit einem Seitenmenü](./assets/pb-add-content-block-example.png){width="600" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Block-Toolbox

| Tool | Symbol | Beschreibung |
| --------- | -------- | ------------- |
| Verschieben | ![move icon](./assets/pb-icon-move.png) | Verschiebt den Block-Container und dessen Inhalt an eine andere Position auf der Bühne. |
| Einstellungen | ![Einstellungssymbol](./assets/pb-icon-settings.png) | Öffnet die Seite Block bearbeiten, auf der Sie den Block auswählen und die Eigenschaften des Containers ändern können. |
| Ausblenden | ![Symbol ausblenden](./assets/pb-icon-hide.png) | Blendet den aktuellen Block-Container und dessen Inhalt aus. |
| Anzeigen | ![Symbol anzeigen](./assets/pb-icon-show.png) | Zeigt den ausgeblendeten Block-Container und dessen Inhalt an. |
| Duplikat | ![Symbol „Duplizieren“](./assets/pb-icon-duplicate.png) | Erstellt eine Kopie des Block-Containers und seines Inhalts. |
| entfernen | ![Symbol entfernen](./assets/pb-icon-remove.png) | Löscht den Block-Container und seinen Inhalt aus der Phase . |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Einen vorhandenen Block hinzufügen

1. Navigieren Sie zum Arbeitsbereich [!DNL Page Builder] auf der Zielseite, dem Block, dem dynamischen Block, dem Produkt oder der Kategorie.

1. Erweitern Sie im [!DNL Page Builder] Bedienfeld **[!UICONTROL Add Content]** und ziehen Sie einen **[!UICONTROL Block]** Platzhalter auf das Bühnenbild.

   ![Block auf die Bühne ziehen](./assets/pb-add-content-block-drag.png){width="600" zoomable="yes"}

1. Bewegen Sie den Mauszeiger über den leeren Blockcontainer, um die Toolbox anzuzeigen, und wählen Sie das Symbol _Einstellungen_ ( ![Einstellungssymbol](./assets/pb-icon-settings.png){width="25"} ) aus.

1. Klicken Sie auf **[!UICONTROL Select Block]**.

   ![Auswählen eines Blocks](./assets/pb-add-content-block-select.png){width="200"}

1. Klicken Sie in der Zeile des Blocks, den Sie hinzufügen möchten, in der letzten Spalte auf **[!UICONTROL Select]** .

   ![Ausgewählter Block](./assets/pb-add-content-block-selected.png){width="600" zoomable="yes"}

   Der Name des ausgewählten Blocks wird auf der Seite angezeigt.

   ![Blockname](./assets/pb-add-content-block-name.png){width="200"}

1. Füllen Sie die verbleibenden Einstellungen nach Bedarf aus, indem Sie die Feldbeschreibungen am Ende dieser Seite als Referenz verwenden.

1. Klicken Sie abschließend auf **[!UICONTROL Save]** , um die Einstellungen anzuwenden und zum Arbeitsbereich [!DNL Page Builder] zurückzukehren.

### Erweiterte Einstellungen

1. Um die Positionierung des Blocks innerhalb des übergeordneten Containers zu steuern, wählen Sie ein **[!UICONTROL Alignment]** aus:

   | Option | Beschreibung |
   | ------ | ----------- |
   | `Default` | Wendet die Standardeinstellung für die Ausrichtung an, die im Stylesheet des aktuellen Designs angegeben ist. |
   | `Left` | Richtet die Liste am linken Rand des übergeordneten Containers aus, wobei ein etwaiger Abstand berücksichtigt wird. |
   | `Center` | Richtet die Liste in der Mitte des übergeordneten Containers aus, wobei der angegebene Abstand berücksichtigt wird. |
   | `Right` | Richtet den Block am rechten Rand des übergeordneten Containers aus, wobei alle angegebenen Auffüllungen berücksichtigt werden. |

   {style="table-layout:auto"}

1. Legen Sie einen **[!UICONTROL Border]** Stil fest, der auf alle vier Seiten des Block-Containers angewendet wird:

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

1. (Optional) Geben Sie die Namen der **[!UICONTROL CSS classes]** aus dem aktuellen Stylesheet an, die auf den Container angewendet werden sollen.

   Trennen Sie mehrere Klassennamen durch ein Leerzeichen.

1. Geben Sie Werte in Pixeln für den **[!UICONTROL Margins and Padding]** ein, um die äußeren Ränder und den inneren Abstand des Block-Containers zu bestimmen.

   Geben Sie die entsprechenden Werte in das Diagramm ein.

   | Container-Bereich | Beschreibung |
   | -------------- | ----------- |
   | [!UICONTROL Margins] | Die Menge des Leerraums, der auf die Außenkante aller Seiten des Containers angewendet wird. Optionen: `Top` / `Right` / `Bottom` / `Left` |
   | [!UICONTROL Padding] | Die Menge des Leerraums, der auf die Innenkante aller Seiten des Containers angewendet wird. Optionen: `Top` / `Right` / `Bottom` / `Left` |

   {style="table-layout:auto"}

## Blockeinstellungen bearbeiten

1. Bewegen Sie den Mauszeiger über den Block-Container und wählen Sie _Symbol_ Einstellungen![ ( (](./assets/pb-icon-settings.png){width="25"}) ) in der Toolbox aus.

   ![Block-Toolbox](./assets/pb-add-content-block-toolbox.png){width="600" zoomable="yes"}

1. Um einen anderen Block auszuwählen, klicken Sie auf **[!UICONTROL Select Block]**.

   - Klicken Sie in der Liste der aktiven Blöcke **[!UICONTROL Select]** den Block, den Sie hinzufügen möchten.
   - Klicken Sie auf **[!UICONTROL Add Selected]**.

1. Aktualisieren Sie die verbleibenden Einstellungen nach Bedarf, indem Sie die Feldbeschreibungen am Ende dieser Seite als Referenz verwenden.

1. Klicken Sie abschließend auf **[!UICONTROL Save]** , um die Einstellungen anzuwenden und zum Arbeitsbereich [!DNL Page Builder] zurückzukehren.

## Duplizieren eines Blocks

1. Bewegen Sie den Mauszeiger über den Block-Container, um die Toolbox anzuzeigen, und wählen Sie _Symbol Duplizieren_ (![Duplikatssymbol](./assets/pb-icon-duplicate.png)) aus.

   Das Duplikat wird direkt unter dem Original angezeigt.

1. Um den neuen Block an eine neue Position zu verschieben, bewegen Sie den Mauszeiger über den Container und klicken Sie dann auf _Verschieben_ (![Symbol Verschieben](./assets/pb-icon-move.png)) in der Toolbox.

1. Wählen Sie den Block aus und ziehen Sie ihn, bis die rote Richtlinie an der neuen Position angezeigt wird.

   Die oberen und unteren Ränder der einzelnen Container werden beim Verschieben des Blocks als gestrichelte Linien angezeigt.

## Entfernen eines Blocks aus der Phase

1. Bewegen Sie den Mauszeiger über den Block-Container, um die Toolbox anzuzeigen, und wählen _das Symbol_ Entfernen![ (Symbol ](./assets/pb-icon-remove.png)) aus.

1. Wenn Sie zum Bestätigen aufgefordert werden, klicken Sie auf **[!UICONTROL OK]**.

<!-- Last updated from includes: 2023-09-11 14:30:19 -->
