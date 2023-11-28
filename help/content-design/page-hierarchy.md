---
title: Seitenhierarchie
description: Erfahren Sie, wie Sie mit dem Seitenhierarchiesystem Ihre Inhaltsseiten organisieren und Paginierung, Navigation und Menüs hinzufügen können.
exl-id: 2ce79b85-1420-4640-a4f7-0143a608a71a
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '931'
ht-degree: 0%

---

# Seitenhierarchie

{{ee-feature}}

Mit dem hierarchischen System für Speicherseiten können Sie Ihre Inhaltsseiten organisieren und Paginierung, Navigation und Menüs hinzufügen. Die Seite Datenschutzrichtlinie in den Beispieldaten ist ein Beispiel für eine Seite mit einem Menü auf der linken Seite. Wenn Sie regelmäßig eine große Menge von Inhalten veröffentlichen, können Sie Ihre Inhalte mithilfe einer Seitenhierarchie organisieren, um Personen das Auffinden von interessanten Artikeln zu erleichtern.

Das Seitenhierarchiesystem verwendet Knoten, um verwandte Inhaltselemente zu identifizieren und Inhaltsseiten in übergeordneten/untergeordneten Beziehungen zu organisieren. Ein übergeordneter Knoten ist wie ein Ordner, der untergeordnete Knoten und Seiten enthalten kann. Die relative Position jedes Knotens und jeder Seite in der Hierarchie wird als _tree_ Struktur. Ein Knoten kann andere Knoten und Inhaltsseiten enthalten und eine einzelne Inhaltsseite kann mit mehreren Knoten und anderen Inhaltsseiten in einer übergeordneten/untergeordneten oder benachbarten Beziehung verknüpft sein.

![Seite mit linker Navigation](./assets/storefront-privacy-policy.png){width="600" zoomable="yes"}

## Konfigurieren der Seitenhierarchie

Die Konfigurationseinstellungen aktivieren das Seitenhierarchiesystem und die Metadaten und bestimmen das Standardmenülayout.

![CMS-Seitenhierarchie](./assets/content-management-cms-page-hierarchy.png){width="600" zoomable="yes"}

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Im linken Bereich unter _[!UICONTROL General]_auswählen **[!UICONTROL Content Management]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) **[!UICONTROL CMS Page Hierarchy]**  und nehmen die erforderlichen Änderungen vor.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Enable Hierarchy Functionality] | Aktiviert die Verwendung der Seitenhierarchie für Ihre Inhaltsseiten. Optionen: `Yes` / `No` |
| [!UICONTROL Enable Hierarchy Metadata] | Wenn diese Option aktiviert ist, können Sie Metadaten mit Seiten in der Hierarchie verknüpfen. Optionen: `Yes` / `No` |
| [!UICONTROL Default Layout for Hierarchy Menu] | Legt den Standardmenüstil fest. Optionen: `Content` / `Left Column` / `Right Column` |

{style="table-layout:auto"}

## Hierarchieknoten hinzufügen

Das folgende Beispiel zeigt, wie ein Knoten mit einfacher Navigation zu verwandten Inhaltsseiten erstellt wird. Obwohl einem Knoten keine Inhaltsseite zugeordnet ist, verfügt er über einen URL-Schlüssel, der an anderer Stelle auf Ihrer Site referenziert werden kann.

Sie können beispielsweise einen Knoten mit dem Namen _Pressemitteilungen_ die Navigation zu einzelnen Pressemitteilungen hat. Anschließend können Sie den Link in Ihre _Über uns_ zum Knoten hinzu. Oder Sie erstellen einen Knoten für eine Sammlung von Back-Ausgaben Ihres Newsletters.

Verwenden Sie zum Verknüpfen mit einem Knoten die [Widget](widgets.md) Tool zum Erstellen eines CMS-Hierarchieknotenlinks und Platzieren des Widgets in einem Inhaltsbaustein oder auf einer Seite.

![Beispielnavigationsmenü auf der Seite &quot;Über uns&quot;](./assets/page-navigation-storefront.png){width="600" zoomable="yes"}

### Schritt 1: Erstellen eines Knotens

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Hierarchy]**.

   ![CMS-Seiten-Raster](./assets/page-hierarchy-cms-pages.png){width="600" zoomable="yes"}

1. Klicken Sie über dem Raster auf **[!UICONTROL Add Node...]**.

1. under _[!UICONTROL Page Properties]_eingeben,**[!UICONTROL Title]**für den Knoten und eine geeignete **[!UICONTROL URL Key]**.

   Der URL-Schlüssel stellt eine eindeutige Webadresse für den Knoten bereit. Hierbei muss es sich um Kleinbuchstaben handeln, wobei Trennzeichen anstelle von Leerzeichen verwendet werden.

   ![Seiteneigenschaften](./assets/page-hierarchy-add-node-page-properties.png){width="500" zoomable="yes"}

1. Klicken **[!UICONTROL Save]**.

   Der Knoten wird in der Baumstruktur links auf der Seite als Ordner angezeigt.

### Schritt 2: Hinzufügen von Seiten zum Knoten

1. Klicken Sie in der Hierarchiestruktur auf , um den Knoten auszuwählen.

1. Klicken **[!UICONTROL Add Selected Pages(s) to Tree]**.

   Sie können nach oben scrollen, um zu sehen, dass jede ausgewählte Seite in der Struktur unter dem Knotenordner angezeigt wird.

### 3. Schritt: Struktur definieren

1. Ziehen Sie die Seiten bei Bedarf an die gewünschte Position, um sie im Menü anzuzeigen.

   ![Ziehen von Seiten an die Position](./assets/page-hierarchy-drag-to-position.png){width="500" zoomable="yes"}

1. Klicken Sie oben in der Hierarchie auf den Knoten .

   Die _[!UICONTROL Page Properties]_-Abschnitt zeigt nun Informationen zum Knoten an.

1. under **[!UICONTROL Render Metadata in HTML Head]** führen Sie folgende Schritte aus:

   ![Metadaten-Einstellungen rendern](./assets/page-hierarchy-render-metadata.png){width="400" zoomable="yes"}

   - Um den Knoten als den oberen Rand der Hierarchie zu kennzeichnen, legen Sie **[!UICONTROL First]** nach `Yes`.

   - Um ein Paginierungssteuerelement anzuzeigen, legen Sie **[!UICONTROL Next/Previous]** nach `Yes`.

   - Um die Seiten in der Hierarchie als Buch zu organisieren, legen Sie **[!UICONTROL Enable Chapter/Section]** nach `Yes`.

     Wenn Sie den Knoten nicht als Teil des Buches einbeziehen möchten, behalten Sie die Standardeinstellung bei `No`.

   - Um den Knoten einem bestimmten Teil des Buches zuzuweisen, legen Sie **[!UICONTROL Chapter/Section]** auf einen der folgenden Werte zu:

      - `No` - definiert den Knoten nicht als Kapitel/Abschnitt.
      - `Chapter` - Weist den aktuellen Knoten als Kapitel zu.
      - `Section` - Weist den aktuellen Knoten als Abschnitt zu.
      - `Both` - Weist den aktuellen Knoten sowohl als Kapitel als auch als Abschnitt zu.

### Schritt 4: Hinzufügen von Paginierungskontrollen

1. under _Paginierungsoptionen für verschachtelte Seiten_, set **[!UICONTROL Enable Pagination]** nach `Yes`.

1. Für **[!UICONTROL Frame]** Geben Sie die Anzahl der Seitenlinks ein, die Sie in das Paginierungssteuerelement aufnehmen möchten.

   Wenn die Hierarchie mehrere Seiten enthält, die in das Paginierungssteuerelement aufgenommen werden können.

1. Für **[!UICONTROL Frame Skip]** Geben Sie die Anzahl der Seiten ein, die Sie für den nächsten Satz von Paginierungslinks voraus (oder zurück) überspringen möchten.

### Schritt 5: Menülayout auswählen

Wenn der Knoten im Menü angezeigt werden soll, gehen Sie wie folgt vor:

1. under _Menüoptionen für Seitennavigation_, set **[!UICONTROL Show in navigation menu]** nach `Yes`.

   Diese Einstellung bestimmt, ob ein Navigationsmenü für die Seitenhierarchie generiert wird.

   ![Menüoptionen für Seitennavigation](./assets/page-hierarchy-page-navigation-menu-options.png){width="300" zoomable="yes"}

1. Um die Position des Menüs im Verhältnis zum Inhalt anzugeben, legen Sie die **[!UICONTROL Menu Layout]**:

   - `Content` - Das Menülayout befindet sich im Inhalt.
   - `Use Default` - Verwendet den im [Konfiguration](../configuration-reference/general/content-management.md).
   - `Left Column` - Das Menü wird links neben dem Inhalt angezeigt.
   - `Right Column` - Das Menü wird rechts neben dem Inhalt angezeigt.

1. Um festzulegen, wie viele Details im Menü enthalten sind, legen Sie **[!UICONTROL Menu Detalization]** auf einen der folgenden Werte zu:

   - `Only Children` - Enthält nur Unterseiten im Menü.
   - `Neighbours and Children` - Umfasst Unterseiten und andere Seiten, die sich auf derselben Ebene in der Hierarchie befinden.

1. Um die Tiefe des Menüs zu bestimmen, geben Sie die **[!UICONTROL Maximal Depth]** für die maximale Anzahl der einzuschließenden Ebenen.

1. Um das Menü zu formatieren, wählen Sie eine **[!UICONTROL List Type]**:

   - `Unordered` - Die Menüoptionen sind nicht nummeriert und können mit oder ohne Aufzählungszeichen formatiert werden. Optionen für ungeordneten Listentyp: Standard/Kreis/Datenträger/Quadrat
   - `Ordered` - Die Menüoptionen sind nummeriert und können als numerische, alphabetische oder römische Zahlen in Groß- oder Kleinbuchstaben formatiert werden.

1. Satz **[!UICONTROL List Style]** auf einen der folgenden Werte zu:

   - `Circle`
   - `Disc`
   - `Square`

1. Wenn Sie auch möchten, dass der Knoten im Navigationsmenü angezeigt wird, scrollen Sie zu _Menüoptionen für Hauptnavigation_ und **[!UICONTROL Show in Navigation menu]** nach `Yes`.

   ![Menüoptionen im Hauptnavigationsmenü](./assets/page-hierarchy-main-navigation-menu-options.png){width="250" zoomable="yes"}

1. Klicken **[!UICONTROL Save]**.
