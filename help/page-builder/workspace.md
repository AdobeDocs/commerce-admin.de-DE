---
title: '[!DNL Page Builder] Workspace'
description: Erfahren Sie mehr über die Tools,  [!DNL Page Builder]  im Arbeitsbereich verfügbar sind, wenn Sie einfache Seiten, Produkt- und Katalogseiten, Blöcke und dynamische Blöcke erstellen.
exl-id: 1cd7b300-0a18-490f-bc11-36de3fec13dc
feature: Page Builder, Page Content
source-git-commit: 69adfa95a11c8a62bd97bd917cebcaa22d3a8087
workflow-type: tm+mt
source-wordcount: '1505'
ht-degree: 0%

---

# [!DNL Page Builder] Workspace

Wenn [[!DNL Page Builder] aktiviert](setup.md) werden der _[!UICONTROL Content]_Abschnitt und der Inhaltserstellungsprozess geändert, um die erweiterten [!DNL Page Builder]-Tools für CMS [Pages](../content-design/page-add.md), [Product](../catalog/product-content.md) und [category](../catalog/categories-content-settings.md) Seiten, [Blocks](../content-design/block-add.md) und [dynamic blocks](../content-design/dynamic-blocks.md) zu nutzen. Dieser Abschnitt enthält ein Feld_ Inhaltsüberschrift _, eine Vorschau des Inhalts und einfachen Zugriff auf den [!DNL Page Builder]-Arbeitsbereich im Vollbildmodus.

![Inhaltsabschnitt mit [!DNL Page Builder] Vorschau](./assets/pb-content-preview.png){width="700" zoomable="yes"}

## Inhaltsüberschrift

Da Suchmaschinen nach Überschriften der Ebene 1 (H1) suchen, können Sie durch Hinzufügen einer Überschrift der Ebene 1 leicht sicherstellen, dass die Seite korrekt indiziert wird.

>[!NOTE]
>
>Das _[!UICONTROL Content Heading]_Feld, das oben auf der Seite angezeigt wird, ist ein älteres Feld, das Inhalte unterstützt, die mit früheren [!DNL Commerce]-Versionen erstellt wurden. Sie ist jedoch nicht Teil von [!DNL Page Builder]. Die [!UICONTROL Content Heading] wird entsprechend dem Stylesheet, das mit dem aktuellen Design verknüpft ist, als Überschrift H1 formatiert. Sie wird direkt über dem aktiven Inhaltsbereich positioniert, der durch die [!DNL Page Builder] definiert wird.

Um die Positionierung und das Format von Überschriften auf allen Ebenen optimal steuern zu können, wird empfohlen, das Feld _[!UICONTROL Content Heading]_leer zu lassen und den Inhaltstyp [!DNL Page Builder]Überschrift[ ](heading.md) zu verwenden.

![Inhaltsüberschrift und andere Überschriften](./assets/pb-storefront-heading-levels.png){width="700" zoomable="yes"}

## Vorschau

Wenn Sie den _[!UICONTROL Content]_erweitern und bereits vorhandene Inhalte vorhanden sind, die mit [!DNL Page Builder] erstellt wurden, wird eine Vorschau des Inhalts so angezeigt, wie er auf einer Seite erscheinen würde. Klicken Sie auf **[!UICONTROL Edit with Page Builder]**oder im Bereich für die Inhaltsvorschau, um den [!DNL Page Builder] Workspace zu öffnen, in dem Sie alle erforderlichen Aktualisierungen vornehmen können.

>[!NOTE]
>
>Der Inhaltseditor von Page Builder zeigt keine Vorschau der Seitenelemente von CMS an, die nicht für die standardmäßige Store-Ansicht verfügbar sind. Sie können beispielsweise keine Vorschau eines CMS-Blocks anzeigen, der nur nicht standardmäßigen Store-Ansichten zugewiesen ist. In diesem Fall müssen Sie zuerst Ihre CMS-Seite veröffentlichen. Dann können Sie diese Seite direkt in der Storefront anzeigen. Alternativ können Sie die Seite im [!UICONTROL Pages] im Admin-Bereich anzeigen, indem Sie die [!UICONTROL View] CMS in der Spalte [!UICONTROL Action] auswählen.

![Vorschau der Produktbeschreibung](./assets/pb-product-category-content-preview.png){width="500" zoomable="yes"}

>[!NOTE]
>
>Für Produkt- und Kategorieformulare ist diese Inhaltsvorschau standardmäßig aktiviert, kann aber deaktiviert werden. Wenn die Leistung aufgrund des Ladens der Vorschau beeinträchtigt ist, können Sie die Vorschau in den Einstellungen [Content-Management-](../configuration-reference/general/content-management.md#advanced-content-tools)) deaktivieren.

## Etappe

Wenn Sie den Arbeitsbereich [!DNL Page Builder] über die Vorschau öffnen, ist die Phase der primäre Arbeitsbereich, in dem Sie Inhalte erstellen und formatieren und sogar schnelle Änderungen an Live-Inhalten vornehmen können. Der Schritt ist zunächst leer und stellt die Design-Oberfläche bereit, auf die Sie Zeilen, Spalten und Registerkarten aus dem linken Bedienfeld ziehen können.

>[!NOTE]
>
>Ab Version 2.4.1 ist die Inhaltsbearbeitung nun nur noch für alle Bereiche im Vollbildmodus verfügbar, die von [!DNL Page Builder] kontrolliert werden - CMS-Seiten, Produkt- und Kategorieseiten, Blöcke und dynamische Blöcke. Die Bearbeitung im Vollbildmodus legt den Fokus auf Ihren Inhalt und bietet eine Ansicht, die dem Benutzererlebnis auf der Storefront besser entspricht.

![Staging mit Seiteninhalten](./assets/pb-workspace-simple-page.png){width="600" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Viewports

Ein _Viewport_ ist der sichtbare Bereich einer Web-Seite, den ein Benutzer sieht. Im Vollbild-Design-Modus werden die Viewport-Schaltflächen über dem [!DNL Page Builder] angezeigt, um Ihnen den Inhalt so anzuzeigen, wie der Site-Benutzer ihn in der Storefront sieht.

![Viewport-Schaltflächen](./assets/pb-workspace-viewport-buttons.png){width="500" zoomable="yes"}

[!DNL Page Builder] definiert auch Haltepunkte für Darstellungsfelder. Haltepunkte definieren minimale und maximale Breiten, innerhalb derer bestimmte Stile angewendet werden. Die [!DNL Page Builder] Viewports bieten die folgenden Inhalts-Breakpoints:

- **Desktop Breakpoint** - `min-width: 1024px`. Dieser Breakpoint wendet Stile an, die für Darstellungsfeldbreiten definiert sind, die 1024 Pixel und mehr messen.
- **Mobile Breakpoints**—`max-width: 768px, min-width: 640px`. Diese Haltepunkte wenden Stile an, die für Darstellungsfeldbreiten zwischen 768 Pixel und 640 Pixel definiert sind.

[!DNL Page Builder] Viewports bieten zwei Funktionen: **_Inhaltsvorschau_** und **_Breakpoint-Einstellungen_**.

### Inhaltsvorschauen

Standardmäßig bietet [!DNL Page Builder] zwei Viewport-Vorschauen:

- **Desktop** - Zeigt die Inhaltsvorschau ohne vordefinierte Breite an. Desktop-definierte Stile (mit einer Mindestbreite von 1024 Pixel als Breakpoint) werden weiterhin auf die Seite angewendet. Die Breite des Desktop-Darstellungsfelds wird jedoch durch Einstellungen für Container-Inhaltstypen wie Zeilen definiert. Wenn Sie das Desktop-Viewport auswählen, wird angezeigt, wie Ihr Inhalt in der Storefront formatiert ist, wenn die Browser-Seitenbreite 1024 Pixel und höher ist.

  ![Desktop-Viewport-Vorschau mit 1024 Pixel Mindestbreite](./assets/pb-workspace-viewport-desktop.png){width="500" zoomable="yes"}

- **Mobil** - Zeigt die Inhaltsvorschau mit einer vordefinierten Breite von 768 Pixel an. Im Gegensatz zum Desktop-Viewport wird der Seiteninhalt im mobilen Viewport nicht in einer Breite von 768 Pixel zusammen mit den Stilen angezeigt, die für die Breakpoint-Breiten von 768 Pixel (maximal) und 640 Pixel (minimal) definiert sind.

  ![Mobile Viewport-Vorschau mit mindestens 768 Pixel Breite](./assets/pb-workspace-viewport-mobile.png){width="500" zoomable="yes"}

### Breakpoint-Einstellungen

Die Viewport-Schaltflächen bieten außerdem die Möglichkeit, je nach ausgewähltem Viewport unterschiedliche Breakpoint-Stile auf Inhaltstypen anzuwenden. Standardmäßig stellt [!DNL Page Builder] Breakpoint-Einstellungen für die _[!UICONTROL Minimum Height]_Felder von Zeilen, Spalten, Registerkarten, Registerkartenelementen, Bannern, Schiebereglern und Folien bereit. Wenn Sie den mobilen Viewport auswählen und dann den Editor für einen dieser Inhaltstypen öffnen, können Sie für die mobilen Viewport-Breakpoints spezifische Feldwerte eingeben. Content-Typ-Felder, die bestimmte Breakpoint-Einstellungen ermöglichen, zeigen rechts neben dem Feld ein Symbol an, ähnlich dem folgenden Beispiel für eine Zeile:

![Symbolanzeige für Breakpoint-Einstellung](./assets/pb-workspace-viewport-field-breakpoint.png){width="400"}

## Bedienfeld

Das [!DNL Page Builder] Bedienfeld befindet sich links neben der Bühne und enthält Inhaltstypen, die auf die Bühne gezogen werden können. Ein Container, der für den Inhaltstyp spezifisch ist, wird dann mit einer Toolbox mit Optionen angezeigt. Die Inhaltstypen sind im Bedienfeld wie folgt organisiert:

### Layout

Der _[!UICONTROL Layout]_Abschnitt des [!DNL Page Builder] Bedienfelds wird verwendet, um Zeilen, Spalten oder Registerkarten zum Schritt hinzuzufügen. Wenn Sie einen Inhaltstyp aus dem Bedienfeld auf den Schritt ziehen, wird ein Container mit einer Toolbox mit Optionen angezeigt, die für den Inhaltstyp spezifisch sind.

Standardmäßig ist die [!DNL Page Builder] leer. Beim Ziehen von Layout-Inhaltstypen aus dem Bedienfeld auf die Bühne können Sie diese über, unter oder in anderen Layout-Containern auf der Seite platzieren. Zeilen können nur direkt zum Schritt hinzugefügt werden.

![[!DNL Page Builder] Bedienfeld mit Layout-Inhaltstypen und -Phase](./assets/pb-stage-toolbox.png){width="600" zoomable="yes"}

| Inhaltstyp des Layouts | Beschreibung |
| ------------------- |------------ |
| [Reihe](row.md) | Eine neue Zeile kann nur aus dem Bedienfeld in den Schritt gezogen und entweder über oder unter einer anderen Zeile, Registerkarte oder Spaltengruppe positioniert werden. Sie können auch die Option Duplizieren verwenden, um eine Kopie einer vorhandenen Zeile zu erstellen. |
| [Spalte](column.md) | Eine Spalte kann aus dem Bedienfeld auf die Bühne oder in Zeilen und Registerkarten gezogen werden. Die maximale Anzahl von Spalten, die hinzugefügt werden können, wird durch die Anzahl der Rasterunterteilungen bestimmt, die in der [Konfiguration“ angegeben ](setup.md). |
| [Registerkarten](tabs.md) | Eine einzelne Registerkarte kann aus dem Bedienfeld in das Stadium oder in Zeilen und Spalten gezogen werden. Zusätzliche Registerkarten können aus der Toolbox hinzugefügt werden. |

{style="table-layout:auto"}

### Elemente

Verwenden Sie den _[!UICONTROL Elements]_Abschnitt des [!DNL Page Builder] Bedienfelds, um Text, Überschriften, Schaltflächen, Trennzeichen und HTML-Code zu jedem Layout-Container auf der [[!DNL Page Builder] Bühne“ ](workspace.md#stage). Wenn Sie einen Inhaltstyp aus dem Bedienfeld in eine Zeile oder Spalte oder in einen Registerkartensatz auf der Bühne ziehen, wird ein Container angezeigt. Verwenden Sie die Toolbox Inhaltstyp , um auf die für den Typ spezifischen Einstellungen zuzugreifen.

Bedienfeld mit Inhaltstypen für Elemente ![[!DNL Page Builder]](./assets/pb-elements.png){width="600" zoomable="yes"}

| Inhaltstyp des Elements | Beschreibung |
| -------------------- | ----------- |
| [Text](text.md) | Fügt einen Textcontainer und einen Editor zum Schritt hinzu. |
| [Überschrift](heading.md) | Fügt der Phase einen Überschriften-Container hinzu. |
| [Schaltflächen](buttons.md) | Fügt der Bühne einen Container für eine einzelne Schaltfläche oder eine Gruppe von Schaltflächen hinzu. |
| [Teiler](divider.md) | Fügt der Bühne einen Container für eine Unterteilung hinzu. |
| [HTML-Code](html-code.md) | Fügt der Phase einen Container für HTML-Code hinzu. |

{style="table-layout:auto"}

### Medien

Verwenden Sie den Abschnitt _[!UICONTROL Media]_des [!DNL Page Builder] Bedienfelds, um Bilder, Videos, Banner, Schieberegler und [!DNL Google Maps] zu einem beliebigen Layout-Container auf der [[!DNL Page Builder]  hinzuzufügen](workspace.md#stage). Wenn ein Medieninhaltstyp aus dem Bedienfeld auf die Bühne gezogen wird, wird ein Container mit einer Toolbox mit Optionen angezeigt, die für den Inhaltstyp spezifisch sind.

![[!DNL Page Builder] Bedienfeld mit Medieninhaltstypen](./assets/pb-media-content-types.png){width="600" zoomable="yes"}

| Medien-Content-Typ | Beschreibung |
| ------------------- | ------------------------------------------ |
| [image](image.md) | Fügt der Phase einen Bild-Container hinzu. |
| [Video](video.md) | Fügt der Phase einen Video-Container hinzu. |
| [Banner](banner.md) | Fügt der Phase einen Banner-Container hinzu. |
| [Schieberegler](slider.md) | Fügt der Bühne einen Schieberegler-Container hinzu. |
| [Map](map.md) | Fügt der Phase einen [!DNL Google Maps]-Container hinzu. |

{style="table-layout:auto"}

### Inhalt hinzufügen

Verwenden Sie den Abschnitt _[!UICONTROL Add Content]_des Bedienfelds [!DNL Page Builder] , um vorhandene Inhalte zur [[!DNL Page Builder] Phase“ ](workspace.md#stage). Wenn Sie einen Medien-Content-Typ aus dem Bedienfeld in das Stadium ziehen, wird ein Container angezeigt. Verwenden Sie die Toolbox Inhaltstyp , um auf die_ Einstellungen _zuzugreifen, die für den Typ spezifisch sind.

![[!DNL Page Builder] Bedienfeld mit „Inhaltstypen hinzufügen“](./assets/pb-add-content.png){width="600" zoomable="yes"}

| Content-Typ | Beschreibung |
| ---------------------------------------------------------------- | -------------------------------------------- |
| [Block](block.md) | Fügt der Phase einen vorhandenen Block hinzu. |
| [Dynamischer Block](dynamic-block.md) | Fügt dem Schritt einen vorhandenen dynamischen Block hinzu. |
| [Produkte](products.md) | Fügt der Phase eine Liste von Produkten hinzu. |
| ![Nur Adobe Commerce](../assets/adobe-logo.svg) [Produktempfehlungen](recommendations.md) | Fügt eine Empfehlungseinheit zur Phase hinzu. |

{style="table-layout:auto"}

## Werkzeugkasten

Jeder Inhalts-Container auf der Bühne verfügt über eine Toolbox von Optionen. Die Optionen variieren je nach Inhaltstyp, umfassen jedoch normalerweise Verschieben, Einstellungen, Ausblenden/Anzeigen, Duplizieren und Entfernen.

### Toolbox anzeigen

Bewegen Sie den Mauszeiger über den Container, um die Toolbox anzuzeigen, und wählen Sie eine Option aus.

![Zeilen-Toolbox-Optionen](./assets/pb-tutorial1-row-toolbox.png){width="600" zoomable="yes"}

### Toolbox-Optionen

| Option | Symbol | Beschreibung |
| --------- | ---------------------------------------- | ------------ |
| Verschieben | ![move icon](./assets/pb-icon-move.png){width="25"} | Verschiebt den aktuellen Inhalts-Container an eine andere Position auf der Bühne. |
| Hinzufügen | ![Symbol hinzufügen](./assets/pb-icon-add.png){width="25"} | Fügt untergeordnete Elemente wie eine Schaltfläche, eine Folie oder eine Registerkarte hinzu. |
| (Bezeichnung) |           | Identifiziert den Container-Inhaltstyp. |
| Einstellungen | ![Einstellungssymbol](./assets/pb-icon-settings.png){width="25"} | Öffnet die Content-Container-Eigenschaften im Bearbeitungsmodus. |
| Ausblenden | ![Symbol ausblenden](./assets/pb-icon-hide.png){width="25"} | Blendet den aktuellen Inhaltscontainer aus. |
| Anzeigen | ![Symbol anzeigen](./assets/pb-icon-show.png){width="25"} | Zeigt den aktuellen Inhaltscontainer an. |
| Duplikat | ![Symbol „Duplizieren“](./assets/pb-icon-duplicate.png){width="25"} | Erstellt eine Kopie des aktuellen Inhalts-Containers. |
| entfernen | ![Entfernen](./assets/pb-icon-remove.png){width="25"} | Löscht den aktuellen Inhalts-Container aus der Phase . |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

<!-- Last updated from includes: 2023-09-11 14:30:19 -->
