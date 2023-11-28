---
title: Layout - Spalte
description: Erfahren Sie mehr über den Inhaltstyp Spalte , mit dem eine Seite in mehrere Spalten im [!DNL Page Builder] Bühne.
exl-id: 9701e1b5-3584-4602-9512-051567274f21
feature: Page Builder, Page Content
source-git-commit: 63b620f2af106108c672a9a91cb66923c5231c53
workflow-type: tm+mt
source-wordcount: '1563'
ht-degree: 0%

---

# Layout - Spalte

Verwenden Sie die _Spalte_ Inhaltstyp , um eine Seite in mehrere Spalten im [[!DNL Page Builder] Schritt](workspace.md#stage). Wenn Sie eine Spalte zu einer Zeile, Registerkarte oder direkt zur Bühne hinzufügen, wird die Spaltengruppe zunächst in zwei Spalten mit gleicher Breite unterteilt. Sie können bei Bedarf Spalten hinzufügen oder entfernen. Die Größe einer Spalte kann durch Ziehen des Rands zwischen zwei Spalten geändert werden. Die Breite der nächsten Spalte wird angepasst, um den verfügbaren Platz in der Zeile, Registerkarte oder Bühne auszufüllen. Eine einzelne Spalte erweitert die gesamte Breite der Bühne oder ihres Containers.

![Spalte hinzufügen](./assets/pb-layout-column-add-drag-placeholder.png){width="600" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Aktualisierungen in Version 2.4.5

Die Funktionen von Page Builder werden in Version 2.4.5 aktualisiert, sodass Benutzer jetzt _[!DNL Columns]_als übergeordneten Container für einzelne Spalten. Dieser neue Container unterstützt auch Eigenschaften für den Hintergrund und entfällt die Notwendigkeit, Spalten in eine Zeile einzuschließen. Dadurch werden unnötiges Markup reduziert und die Anzeige und das Erlebnis in der Storefront besser gesteuert.

Sie können das Layout der [!DNL Columns] -Container, indem Sie eine Spalte über oder unter andere Spalten in der Gruppe ziehen und stapeln. Dadurch wird eine neue Vielzahl möglicher Layoutkombinationen eröffnet, die ohne die Notwendigkeit einer Anpassung durch Entwickler erreicht werden können.

Sehen Sie sich dieses Video an, um zu erfahren, wie die [!DNL Columns] -Container können verwendet werden, um Ihre Seitenlayouts zu verfeinern:

>[!VIDEO](https://video.tv.adobe.com/v/345828?quality=12)

## Spalten-Toolbox

Jede Spalte verfügt über eine Toolbox mit Optionen, die angezeigt wird, wenn Sie den Mauszeiger über den Container bewegen.

| Tool | Symbol | Beschreibung |
|--- |--- |--- |
| Verschieben | ![Symbol Verschieben](./assets/pb-icon-move.png){width="25"} | Verschiebt die Spalte und ihren Inhalt in Bezug auf andere Spalten an eine andere Position. |
| (Titel) | Spalte | Identifiziert den aktuellen Container als Spalte. Bewegen Sie den Mauszeiger über den Spaltenbehälter, um die Toolbox anzuzeigen. |
| Einstellungen | ![Symbol Einstellungen](./assets/pb-icon-settings.png){width="25"} | Öffnet die Seite Spalte bearbeiten , auf der Sie die Eigenschaften des Containers ändern können. |
| Duplizieren | ![Symbol &quot;Duplizieren&quot;](./assets/pb-icon-duplicate.png){width="25"} | Kopiert die aktuelle Spalte. |
| Entfernen | ![Symbol &quot;Entfernen&quot;](./assets/pb-icon-remove.png){width="25"} | Löscht die aktuelle Spalte und ihren Inhalt. |

{style="table-layout:auto"}

## Spaltenraster

Die [grid](workspace.md) stellt sicher, dass der Inhalt in einer Spalte konsistent ausgerichtet ist und die Seite auf Desktop- und Mobilgeräten korrekt dargestellt wird. Weitere Informationen finden Sie unter [Erweiterte Inhaltswerkzeuge](setup.md) Abschnitt [!DNL Page Builder] Konfiguration.

![Rasterunterteilungen in einer Zeile mit einer Spalte](./assets/pb-layout-column-one-grid.png){width="500" zoomable="yes"}

Im folgenden zweispaltigen Beispiel geben die Zahlen in Klammern (6/12) am oberen Rand jedes Spaltenbehälters die Anzahl der Rasterdivisionen in jeder Spalte und die Gesamtzahl der Divisionen an. In diesem Fall entspricht die Spalte der Breite von sechs von insgesamt 12 Rastereinheiten.

![Rasteraufteilungen in Zeilen mit zwei Spalten](./assets/pb-layout-column-two-grid.png){width="600" zoomable="yes"}

## Spalte hinzufügen

1. Im [!DNL Page Builder] Bereich unter _[!UICONTROL Layout]_, ziehen Sie eine **[!UICONTROL Column]**auf die Bühne.

   ![Ziehen einer Spalte auf die Bühne](./assets/pb-layout-column-add-drag-placeholder.png){width="600" zoomable="yes"}

   Die Spaltengruppe ist nun in zwei Spalten mit gleicher Breite unterteilt. Jede Spalte ist ein separater Container für Inhalte und verfügt über einen eigenen Satz an Toolbox-Optionen.

   ![Zwei gleiche Spalten](./assets/pb-layout-columns-two-empty.png){width="600" zoomable="yes"}

1. Klicken Sie in der linken oberen Ecke der Spaltengruppe auf die _Raster_ Tool (![Grid Control](./assets/pb-icon-grid-control.png)) und passen Sie die Rastergröße nach Bedarf an.

   Die Positionierung von Inhalten im Raster hilft, Inhalte konsistent auszurichten, und stellt die Seite auf Desktop- und Mobilgeräten korrekt dar. Weitere Informationen finden Sie unter [Erweiterte Inhaltswerkzeuge](../configuration-reference/general/content-management.md) Abschnitt [!DNL Page Builder] Konfiguration.

   ![Rasterunterteilungen in zwei Spalten](./assets/pb-layout-column-two-grid.png){width="600" zoomable="yes"}

## Spaltengröße ändern

1. Bewegen Sie den Mauszeiger über den Rahmen zwischen zwei Spalten.

   Der Rahmen wird hervorgehoben und das Toolbox für die ausgewählte Spalte wird angezeigt.

   ![Rahmen zwischen zwei Spalten hervorgehoben](./assets/pb-column-resize-border.png){width="600" zoomable="yes"}

1. Halten Sie die Maustaste gedrückt, um das Raster anzuzeigen, und ziehen Sie den Rahmen an eine neue Position auf dem Raster.

   Die Breite beider Spalten wird entsprechend der Änderung angepasst. Die neue Breite jeder Spalte wird nach der Beschriftung angezeigt, z. B. `4/12` (vier von 12) und `8/12` (acht von zwölf).

   ![Größenangepasste Spalten](./assets/pb-columns-resized-grid.png){width="600" zoomable="yes"}

## Spalte entfernen

1. Bewegen Sie den Mauszeiger über die Spalte, die Sie entfernen möchten, um die Toolbox anzuzeigen und die _Entfernen_ ( ![Symbol &quot;Entfernen&quot;](./assets/pb-icon-remove.png){width="20"} ).

   ![Spalten-Toolbox](./assets/pb-column-toolbox-remove.png){width="600" zoomable="yes"}

1. Wenn die Spalte Inhalt enthält, klicken Sie auf **[!UICONTROL OK]** zur Bestätigung.

   Um den Prozess in Zukunft zu beschleunigen, können Sie den Bestätigungsschritt überspringen, indem Sie die **[!UICONTROL Do not show this again]** aktivieren.

   Die Spaltengruppe verfügt nun über eine einzige Spalte (12/12) und ein Raster. Da das Raster nur für Spalten verfügbar ist, können Sie dieses Verfahren verwenden, um das Raster anzuzeigen.

   ![Einzelne Spalte mit Raster](./assets/pb-column-single-grid.png){width="600" zoomable="yes"}

1. Wenn die Spaltengruppe die verbleibende Spalte auf die volle Breite der Zeile oder Phase erweitern soll:

   - Bewegen Sie den Mauszeiger über die Spalte, um die Toolbox anzuzeigen und die _Einstellungen_ ( ![Symbol Einstellungen](./assets/pb-icon-settings.png){width="20"} ).

   - Scrollen Sie nach unten zum _[!UICONTROL Advanced]_und legen Sie alle vier **[!UICONTROL Padding]**Werte in `0`.

     ![Verwenden des Nullpunkts](./assets/pb-tutorial1-row-settings-advanced-margins-padding-zero.png){width="600" zoomable="yes"}

   - Klicken Sie oben rechts auf **[!UICONTROL Save]** zum Schließen der _[!UICONTROL Edit Column]_Seite.

1. Klicken Sie auf _Vollbild schließen_ ( ![Symbol &quot;Vollbild schließen&quot;](./assets/pb-icon-reduce.png){width="20"} ) in der oberen rechten Ecke des Arbeitsbereichs angezeigt, und klicken Sie dann auf **[!UICONTROL Save]** in der oberen rechten Ecke.

## Spalteneinstellungen ändern

1. Bewegen Sie den Mauszeiger über die Spalte, um die Toolbox anzuzeigen und die _Einstellungen_ ( ![Symbol Einstellungen](./assets/pb-icon-settings.png){width="20"} ).

   ![Spalten-Toolbox](./assets/pb-column-toolbox-settings.png){width="600" zoomable="yes"}

1. Ändern Sie die **[!UICONTROL Appearance]** nach Bedarf.

   - Wählen Sie die Ausrichtungseinstellung aus, die die Position der Spalte in Bezug auf ihren Container bestimmt.

     | Option | Beschreibung |
     | ------ | ----------- |
     | `Full Height` | Die Spalte erweitert die volle Höhe ihres Containers. |
     | `Top Aligned` | Die Spalte wird am oberen Rand des Containers ausgerichtet. |
     | `Centered` | Die Spalte in zentriert in der Mitte ihres Containers. |
     | `Bottom Aligned` | Die Spalte wird am unteren Rand des Containers ausgerichtet. |

     {style="table-layout:auto"}

   - Geben Sie bei Bedarf die **[!UICONTROL Minimum Height]** für die Spalte. Sie können beispielsweise die Mindesthöhe so festlegen, dass sie der Höhe eines Hintergrundbilds entspricht.

   - Wenn Sie die Mindesthöhe festlegen, legen Sie die **[!UICONTROL Vertical Alignment]**  zur Steuerung der Position der Inhaltscontainer, die der Spalte hinzugefügt werden (`Top`, `Center`oder `Bottom`).

1. Ändern Sie den Hintergrund für den Spalteninhalt.

   - **[!UICONTROL Background Color]** - Geben Sie die Farbe an, indem Sie ein Muster auswählen, auf die Farbauswahl klicken oder einen gültigen Farbnamen oder einen entsprechenden Hexadezimalwert eingeben. Diese Einstellung bestimmt die Hintergrundfarbe der Spalte.

   - **[!UICONTROL Background Image]** - Verwenden Sie bei Bedarf die bereitgestellten Tools, um ein Hintergrundbild auszuwählen, das auf die Spalte angewendet werden soll:

     | Tool | Beschreibung |
     | ------ | ----------- |
     | [!UICONTROL Upload] | Lädt eine Bilddatei von Ihrem lokalen Computer in die Galerie hoch und wendet sie dann als Hintergrundbild für die Spalte an. |
     | [!UICONTROL Select from Gallery] | fordert Sie auf, ein vorhandenes Bild aus der Galerie als Hintergrundbild für die Spalte auszuwählen. |
     | ![Kamerasymbol](./assets/pb-icon-camera.png){width="25"} | Ermöglicht Ihnen, das Bild entweder auf die Kachel &quot;Kamera&quot;zu ziehen oder zum Bild in Ihrem lokalen Dateisystem zu navigieren. |

     {style="table-layout:auto"}

   - **[!UICONTROL Background Mobile Image]** - Verwenden Sie bei Bedarf dieselben Tools, um ein anderes Hintergrundbild für die Anzeige auf Mobilgeräten auszuwählen.

   - **[!UICONTROL Background Size]** - Ändern Sie diese Einstellung, um festzulegen, wie das Hintergrundbild im Verhältnis zur Breite der Spalte skaliert wird:

     | Option | Beschreibung |
     | ------ | ----------- |
     | `Cover` | Das Hintergrundbild deckt die gesamte Breite der Spalte ab. |
     | `Contain` | Das Hintergrundbild ist auf die Breite des Inhaltsbereichs beschränkt. |
     | `Auto` | Wendet die standardmäßige Hintergrundgröße an, die im Stylesheet des aktuellen Designs angegeben ist. |

     {style="table-layout:auto"}

   - **[!UICONTROL Background Position]** - Ändern Sie diese Einstellung, um den Ankerpunkt des Bildes in Bezug auf die Spalte zu bestimmen. Optionen: `Top Left`, `Top Center`, `Top Right`, `Center Left`, `Center`, `Center Right`, `Bottom Left`, `Bottom Center`oder `Bottom Right`

   - **[!UICONTROL Background Attachment]** - Ändern Sie diese Einstellung, um festzulegen, wie sich das Hintergrundbild im Verhältnis zur Scrollseite bewegt:

     | Option | Beschreibung |
     | ------ | ----------- |
     | `Scroll` | Das Hintergrundbild wird synchronisiert, um beim Bildlauf der Seite nach unten zu navigieren. |
     | `Fixed` | (Für Mobilgeräte nicht verfügbar) Das Hintergrundbild wird nicht verschoben, wenn der Container über das Bild blättert, und ist an der angegebenen Hintergrundposition fixiert. |

     {style="table-layout:auto"}

   - **[!UICONTROL Background Repeat]** - Wenn Sie das Hintergrundbild zum Ausfüllen des Bereichs wiederholen möchten, ändern Sie diese Einstellung `Yes`.

1. Aktualisieren Sie die _[!UICONTROL Advanced]_nach Bedarf.

   - Um die horizontale Positionierung der Inhaltscontainer zu steuern, die der Spalte hinzugefügt werden, wählen Sie eine **[!UICONTROL Alignment]**:

     | Option | Beschreibung |
     | ------ | ----------- |
     | `Default` | Wendet die Standardeinstellung für die Ausrichtung an, die im Stylesheet des aktuellen Designs angegeben ist. |
     | `Left` | Richtet die Inhaltscontainer am linken Rand des Spaltenbehälters aus, wobei der angegebene Abstand berücksichtigt wird. |
     | `Center` | Richtet den Inhalts-Container in der Mitte des Spaltenbehälters aus, wobei der angegebene Abstand berücksichtigt wird. |
     | `Right` | Richtet den Inhalts-Container am rechten Rand des Spaltenbehälters aus, wobei der angegebene Abstand berücksichtigt wird. |

     {style="table-layout:auto"}

   - Legen Sie die **[!UICONTROL Border]** -Stil, der auf alle vier Seiten des Spaltencontainers angewendet wird:

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

   - (Optional) Geben Sie die Namen von **[!UICONTROL CSS classes]** aus dem aktuellen Stylesheet, das auf den Spaltencontainer angewendet werden soll.

     Trennen Sie mehrere Klassennamen durch ein Leerzeichen.

   - Geben Sie Werte in Pixel für die **[!UICONTROL Margins and Padding]** um die äußeren Ränder und den inneren Abstand der Spalte anzugeben.

     Geben Sie jeden entsprechenden Wert in das Spaltenbehälterdiagramm ein.

     | Container-Bereich | Beschreibung |
     | -------------- | ----------- |
     | [!UICONTROL Margins] | Die Menge an leerem Raum, die auf den äußeren Rand aller Seiten des Containers angewendet wird. Optionen: `Top` / `Right` / `Bottom` / `Left` |
     | [!UICONTROL Padding] | Die Menge an leerem Raum, die auf den inneren Rand aller Seiten des Containers angewendet wird. Optionen: `Top` / `Right` / `Bottom` / `Left` |

     {style="table-layout:auto"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]** , um die Einstellungen anzuwenden und zum [!DNL Page Builder] Arbeitsbereich.
