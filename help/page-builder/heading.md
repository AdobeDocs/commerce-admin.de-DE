---
title: Elemente - Überschrift
description: Erfahren Sie mehr über den Inhaltstyp der Überschrift, der zum Hinzufügen eines Text-Containers mit einer Überschriftenebene von H1 bis H6 zur  [!DNL Page Builder]  verwendet wird.
exl-id: dc51e7f6-a235-49dc-a978-1419a63fa33e
feature: Page Builder, Page Content
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '941'
ht-degree: 0%

---

# Elemente - Überschrift

Überschriftenebenen legen eine Hierarchie fest, die Inhalte organisiert und Suchmaschinen dabei hilft, jede Seite zu indizieren. Verwenden Sie den _Überschrift_-Inhaltstyp in [[!DNL Page Builder] Phase](workspace.md#stage), um der Phase einen Text-Container mit einer Überschriftenebene von H1 bis H6 hinzuzufügen. Überschriften werden entsprechend dem Stylesheet formatiert, das mit dem aktuellen Design verknüpft ist.

Das [Inhaltsüberschrift](workspace.md) im _[!UICONTROL Content]_&#x200B;Abschnitt kann verwendet werden, um eine H1-Überschrift oben auf der Seite hinzuzufügen. Das Feld ist jedoch ein älteres Feld aus früheren [!DNL Commerce] Versionen und wird zur Unterstützung älterer Inhalte bereitgestellt. In diesem Feld werden die erweiterten Funktionen von [!DNL Page Builder] nicht genutzt. Es wird empfohlen, das Feld Inhaltsüberschrift leer zu lassen und den Inhaltstyp [!DNL Page Builder] Überschrift zu verwenden, um der Seite Überschriften einer beliebigen Ebene hinzuzufügen.

Das folgende Beispiel zeigt, wie die Inhaltsüberschrift und der Inhaltstyp der Überschrift angezeigt werden, wenn sie durch das Luma-Design formatiert sind.

![Überschriften- und Überschriftenebenen in der Storefront](./assets/pb-storefront-heading-levels.png){width="700" zoomable="yes"}

Sie können eine Überschrift aus dem Abschnitt _Elemente_ des [!DNL Page Builder] Bedienfelds in eine Zeile, Spalte oder einen Registerkartensatz auf der Bühne ziehen. Die Überschriftenebene und die Ausrichtung können über die Editor-Symbolleiste auf der Bühne oder mithilfe des Steuerelements _Einstellungen_ ( ![Einstellungssymbol](./assets/pb-icon-settings.png){width="20"} ) gesteuert werden.

{{$include /help/_includes/page-builder-save-timeout.md}}

## Überschrifteneditor

![Überschrifteneditor mit Symbolleiste](./assets/pb-elements-heading-toolbar.png){width="500" zoomable="yes"}

## Überschriften-Container-Toolbox

Wie bei allen Inhalts-Containern wird die Toolbox angezeigt, wenn Sie den Mauszeiger über den Container bewegen.

![Überschriften-Container-Toolbox](./assets/pb-elements-heading-toolbox.png){width="500" zoomable="yes"}

| Tool | Symbol | Beschreibung |
| --------- | ----------------- | ---------------------- |
| Verschieben | ![move icon](./assets/pb-icon-move.png){width="25"} | Verschiebt den Überschriften-Container an eine andere gültige Position auf der Seite. |
| (Bezeichnung) | Überschrift | Gibt den aktuellen Container als Überschrift an. |
| Einstellungen | ![Einstellungssymbol](./assets/pb-icon-settings.png){width="25"} | Öffnet die Seite Überschrift bearbeiten , auf der Sie die Eigenschaften des Containers ändern können. |
| Ausblenden | ![Symbol ausblenden](./assets/pb-icon-hide.png){width="25"} | Blendet den Überschriftencontainer aus. |
| Anzeigen | ![Symbol anzeigen](./assets/pb-icon-show.png){width="25"} | Zeigt den ausgeblendeten Überschriftencontainer an. |
| Duplikat | ![Symbol „Duplizieren“](./assets/pb-icon-duplicate.png){width="25"} | Erstellt eine Kopie des Überschriften-Containers. |
| entfernen | ![Symbol entfernen](./assets/pb-icon-remove.png){width="25"} | Löscht den Überschriften-Container und seinen Inhalt aus der Phase. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Überschrift hinzufügen

1. Erweitern Sie im [!DNL Page Builder] Bedienfeld **[!UICONTROL Elements]** und ziehen Sie einen **[!UICONTROL Heading]** Platzhalter in eine Zeile, Spalte oder einen Tab, die bzw. der auf dem Bühnenbild festgelegt ist.

   ![Ziehen einer Überschrift auf die Bühne](./assets/pb-elements-heading-drag.png){width="600" zoomable="yes"}

1. Geben Sie im Editor den Überschrifttext über den `Edit Heading Text` Platzhalter ein.

   Standardmäßig wird dem Überschrifttext die Überschriftart Ebene zwei (H2) zugewiesen.

   ![Platzhalter im Überschriften-Editor](./assets/pb-elements-header-editor-placeholder.png){width="500" zoomable="yes"}

1. Wählen Sie in der Symbolleiste den entsprechenden Überschrifttyp zwischen H1 und H6.

1. Ändern Sie bei Bedarf die Ausrichtung.

## Header-Einstellungen bearbeiten

1. Bewegen Sie den Mauszeiger über den Überschriften-Container, um die Toolbox anzuzeigen, und wählen _das Symbol_ Einstellungen![ ( (](./assets/pb-icon-settings.png){width="20"}) aus.

   ![Überschriften-Toolbox](./assets/pb-elements-heading-toolbox.png){width="500" zoomable="yes"}

1. Aktualisieren Sie bei Bedarf den Überschrifteninhalt (**[!UICONTROL Heading Type]** und **[!UICONTROL Heading Text]**).

   Sie können diesen Inhalt auch im Überschrifteneditor aktualisieren.

1. Aktualisieren Sie die _[!UICONTROL Advanced]_&#x200B;nach Bedarf.

   - Um die Positionierung der Überschrift innerhalb des übergeordneten Containers zu steuern, wählen Sie ein **[!UICONTROL Alignment]** aus:

     | Option | Beschreibung |
     | ------ | ----------- |
     | `Default` | Wendet die Standardeinstellung für die Ausrichtung an, die im Stylesheet des aktuellen Designs angegeben ist. |
     | `Left` | Richtet die Liste am linken Rand des übergeordneten Containers aus, wobei ein etwaiger Abstand berücksichtigt wird. |
     | `Center` | Richtet die Liste in der Mitte des übergeordneten Containers aus, wobei der angegebene Abstand berücksichtigt wird. |
     | `Right` | Richtet den Block am rechten Rand des übergeordneten Containers aus, wobei alle angegebenen Auffüllungen berücksichtigt werden. |

     {style="table-layout:auto"}

   - Legen Sie den **[!UICONTROL Border]** fest, der auf alle vier Seiten des Überschriften-Containers angewendet wird:

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

     | Option | Beschreibung |
     | ------ |------------ |
     | [!UICONTROL Border Color] | Geben Sie die Farbe an, indem Sie einen Musterabschnitt auswählen, auf die Farbauswahl klicken oder einen gültigen Farbnamen oder einen entsprechenden Hexadezimalwert eingeben. |
     | [!UICONTROL Border Width] | Geben Sie die Anzahl der Pixel für die Rahmenlinienbreite ein. |
     | [!UICONTROL Border Radius] | Geben Sie die Anzahl der Pixel ein, um die Größe des Radius festzulegen, mit dem jede Ecke des Rahmens gerundet werden soll. |

     {style="table-layout:auto"}

   - (Optional) Geben Sie die Namen der **[!UICONTROL CSS classes]** aus dem aktuellen Stylesheet an, die auf den Container angewendet werden sollen.

     Trennen Sie mehrere Klassennamen durch ein Leerzeichen.

   - Geben Sie Werte in Pixeln für den **[!UICONTROL Margins and Padding]** ein, um die äußeren Ränder und den inneren Abstand des Überschriften-Containers zu bestimmen.

     Geben Sie die entsprechenden Werte in das Diagramm ein.

     | Container-Bereich | Beschreibung |
     | -------------- | ----------- |
     | [!UICONTROL Margins] | Die Menge des Leerraums, der auf die Außenkante aller Seiten des Containers angewendet wird. Optionen: `Top` / `Right` / `Bottom` / `Left` |
     | [!UICONTROL Padding] | Die Menge des Leerraums, der auf die Innenkante aller Seiten des Containers angewendet wird. Optionen: `Top` / `Right` / `Bottom` / `Left` |

     {style="table-layout:auto"}

1. Klicken Sie abschließend auf **[!UICONTROL Save]** , um die Einstellungen anzuwenden und zum Arbeitsbereich [!DNL Page Builder] zurückzukehren.

## Duplizieren einer Überschrift

Bei einer formatierten Überschrift mit bestimmten Einstellungen ist es effizienter, die Überschrift zu duplizieren, anstatt mit einem neuen Platzhalter von vorne zu beginnen.

1. Bewegen Sie den Mauszeiger über den Überschriften-Container, um die Toolbox anzuzeigen, und wählen Sie _Symbol Duplizieren_ ( ![Duplikatssymbol](./assets/pb-icon-duplicate.png){width="20"} ) aus.

   Das Duplikat wird direkt unter dem Original angezeigt.

   ![Duplizieren eines Überschriften-Containers](./assets/pb-elements-heading-duplicate.png){width="500" zoomable="yes"}

1. Bewegen Sie den Mauszeiger über den neuen Überschriften-Container, um die Toolbox anzuzeigen, und wählen _das Symbol_ Verschieben![ ((Symbol ](./assets/pb-icon-move.png){width="20"} ) aus.

   ![Verschieben einer Überschrift](./assets/pb-elements-heading-move.png){width="500" zoomable="yes"}

1. Wählen Sie die Überschrift aus und ziehen Sie sie, bis die rote Richtlinie die neue Position markiert.

   Der obere und untere Rand jedes Containers werden beim Verschieben der Überschrift als gestrichelte Linien angezeigt.

   ![Verschieben der duplizierten Überschrift an die Position](./assets/pb-elements-heading-move-guideline.png){width="500" zoomable="yes"}

1. Wenn Sie die Überschriftenebene ändern möchten, klicken Sie auf den Überschrifttext und wählen Sie die neue Ebene in der Editor-Symbolleiste aus.

   ![Auswählen einer neuen Überschriftenebene](./assets/pb-elements-heading-change-heading-level.png){width="500" zoomable="yes"}

<!-- Last updated from includes: 2023-09-11 14:30:19 -->
