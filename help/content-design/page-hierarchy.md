---
title: Seitenhierarchie
description: Erfahren Sie, wie Sie mit dem Seitenhierarchiesystem Ihre Inhaltsseiten organisieren und Seitenumbrüche, Navigation und Menüs hinzufügen können.
exl-id: 2ce79b85-1420-4640-a4f7-0143a608a71a
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/de/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '953'
ht-degree: 0%

---

# Seitenhierarchie

{{ee-feature}}

Mit dem Hierarchie-System der Inhaltsseite können Sie Ihre Inhaltsseiten organisieren und Paginierung, Navigation und Menüs hinzufügen. Die Seite mit den Datenschutzrichtlinien in den Beispieldaten ist ein Beispiel für eine Seite mit einem Menü auf der linken Seite. Wenn Sie regelmäßig eine große Menge an Inhalten veröffentlichen, können Sie eine Seitenhierarchie verwenden, um Ihre Inhalte zu organisieren, damit Personen die interessanten Artikel leicht finden können.

Das Seitenhierarchiesystem verwendet -Knoten, um verwandte Inhaltselemente zu identifizieren und Inhaltsseiten in hierarchische Beziehungen zwischen übergeordneten und untergeordneten Elementen zu organisieren. Ein übergeordneter Knoten ist wie ein Ordner, der untergeordnete Knoten und Seiten enthalten kann. Die relative Position jedes Knotens und jeder Seite in der Hierarchie wird als _Baumstruktur_ angezeigt. Ein Knoten kann andere Knoten und Inhaltsseiten enthalten, und eine einzelne Inhaltsseite kann mit mehreren Knoten und anderen Inhaltsseiten in einer übergeordneten/untergeordneten oder benachbarten Beziehung verknüpft sein.

![Seite mit linker Navigation](./assets/storefront-privacy-policy.png){width="600" zoomable="yes"}

## Konfigurieren der Seitenhierarchie

Die Konfigurationseinstellungen aktivieren das Seitenhierarchiesystem und die Metadaten und bestimmen das Standardmenü-Layout.

![CMS-Seitenhierarchie](./assets/content-management-cms-page-hierarchy.png){width="600" zoomable="yes"}

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wählen Sie im linken Bedienfeld unter _[!UICONTROL General]_&#x200B;die Option **[!UICONTROL Content Management]**&#x200B;aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) **[!UICONTROL CMS Page Hierarchy]** und nehmen Sie die erforderlichen Änderungen vor.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Enable Hierarchy Functionality] | Aktiviert die Verwendung der Seitenhierarchie für Ihre Inhaltsseiten. Optionen: `Yes` / `No` |
| [!UICONTROL Enable Hierarchy Metadata] | Wenn diese Option aktiviert ist, können Sie Metadaten mit Seiten in der Hierarchie verknüpfen. Optionen: `Yes` / `No` |
| [!UICONTROL Default Layout for Hierarchy Menu] | Bestimmt den Standardstil des Menüs. Optionen: `Content` / `Left Column` / `Right Column` |

{style="table-layout:auto"}

## Hierarchieknoten hinzufügen

Das folgende Beispiel zeigt, wie Sie einen Knoten mit einfacher Navigation zu verwandten Inhaltsseiten erstellen. Obwohl einem Knoten keine Inhaltsseite zugeordnet ist, verfügt er über einen URL-Schlüssel, der an anderer Stelle auf Ihrer Site referenziert werden kann.

Sie können beispielsweise einen Knoten mit dem Namen _Pressemitteilungen_ erstellen, der Navigation zu einzelnen Pressemitteilungen enthält. Anschließend können Sie den Link auf Ihrer Seite &quot;_&quot;_ Knoten einfügen. Oder Sie erstellen einen Knoten für eine Sammlung von früheren Ausgaben Ihres Newsletters.

Verwenden Sie zum Verknüpfen mit einem Knoten das [Widget](widgets.md)-Tool, um einen CMS Hierarchy Node-Link zu erstellen und das Widget in einem Inhaltsbaustein oder einer Seite zu platzieren.

![Beispiel-Navigationsmenü auf der Seite „Über uns“](./assets/page-navigation-storefront.png){width="600" zoomable="yes"}

### Schritt 1: Erstellen eines Knotens

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Hierarchy]**.

   ![Raster für CMS-Seiten](./assets/page-hierarchy-cms-pages.png){width="600" zoomable="yes"}

1. Klicken Sie über dem Raster auf **[!UICONTROL Add Node...]**.

1. Geben Sie unter _[!UICONTROL Page Properties]_&#x200B;einen **[!UICONTROL Title]**&#x200B;für den Knoten und einen geeigneten **[!UICONTROL URL Key]**&#x200B;ein.

   Der URL-Schlüssel stellt eine eindeutige Web-Adresse für den Knoten bereit. Es müssen nur Kleinbuchstaben verwendet werden, wobei Bindestriche anstelle von Leerzeichen verwendet werden müssen, um Wörter zu trennen.

   ![Seiteneigenschaften](./assets/page-hierarchy-add-node-page-properties.png){width="500" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Save]**.

   Der Knoten wird als Ordner in der Baumstruktur links auf der Seite angezeigt.

### Schritt 2: Hinzufügen von Seiten zum Knoten

1. Klicken Sie in der Hierarchiestruktur auf , um den Knoten auszuwählen.

1. Klicken Sie auf **[!UICONTROL Add Selected Pages(s) to Tree]**.

   Sie können nach oben scrollen, um zu sehen, dass jede ausgewählte Seite in der Baumstruktur unter dem Knotenordner angezeigt wird.

### Schritt 3: Definieren der Struktur

1. Ziehen Sie die Seiten gegebenenfalls in die Position, in der sie im Menü angezeigt werden sollen.

   ![Seiten in Position ziehen](./assets/page-hierarchy-drag-to-position.png){width="500" zoomable="yes"}

1. Klicken Sie auf den Knoten oben in der Hierarchie.

   Im Abschnitt _[!UICONTROL Page Properties]_&#x200B;werden jetzt Informationen zum Knoten angezeigt.

1. Gehen Sie unter **[!UICONTROL Render Metadata in HTML Head]** wie folgt vor:

   ![Rendern von Metadateneinstellungen](./assets/page-hierarchy-render-metadata.png){width="400" zoomable="yes"}

   - Um den Knoten als oberste Ebene der Hierarchie zu identifizieren, setzen Sie **[!UICONTROL First]** auf `Yes`.

   - Um ein Paginierungssteuerelement anzuzeigen, setzen Sie **[!UICONTROL Next/Previous]** auf `Yes`.

   - Um die Seiten in der Hierarchie wie ein Buch zu organisieren, legen Sie **[!UICONTROL Enable Chapter/Section]** auf `Yes` fest.

     Wenn Sie den Knoten nicht als Teil des Buchs einbeziehen möchten, lassen Sie die `No`.

   - Um den Knoten einem bestimmten Teil des Buches zuzuweisen, legen Sie **[!UICONTROL Chapter/Section]** auf einen der folgenden Werte fest:

      - `No` - Der Knoten wird nicht als Kapitel/Abschnitt definiert.
      - `Chapter` - Weist den aktuellen Knoten als Kapitel zu.
      - `Section` - Weist den aktuellen Knoten als Abschnitt zu.
      - `Both` - Weist den aktuellen Knoten sowohl als Kapitel als auch als Abschnitt zu.

### Schritt 4: Paginierungssteuerelemente hinzufügen

1. Legen _unter „Paginierungsoptionen für verschachtelte_&quot; **[!UICONTROL Enable Pagination]** auf `Yes` fest.

1. Geben Sie **[!UICONTROL Frame]** die Anzahl der Seitenlinks ein, die Sie in das Paginierungssteuerelement aufnehmen möchten.

   Wenn es mehr Seiten in der Hierarchie gibt, die in das Paginierungssteuerelement aufgenommen werden können.

1. Geben Sie **[!UICONTROL Frame Skip]** die Anzahl der Seiten ein, die Sie für den nächsten Satz von Paginierungslinks überspringen (oder zurückspringen) möchten.

### Schritt 5: Menülayout auswählen

Wenn der Knoten im Menü angezeigt werden soll, gehen Sie wie folgt vor:

1. Legen _unter „Optionen im Seitennavigationsmenü_ den **[!UICONTROL Show in navigation menu]** auf `Yes` fest.

   Diese Einstellung bestimmt, ob ein Navigationsmenü für die Seitenhierarchie generiert wird.

   ![Menüoptionen für die Seitennavigation](./assets/page-hierarchy-page-navigation-menu-options.png){width="300" zoomable="yes"}

1. Um die Position des Menüs in Bezug auf den Inhalt anzugeben, legen Sie die **[!UICONTROL Menu Layout]** fest:

   - `Content` - Das Menü-Layout befindet sich im Inhalt.
   - `Use Default` - Verwendet den in der [ angegebenen Menüstil](../configuration-reference/general/content-management.md).
   - `Left Column` - Das Menü wird links neben dem Inhalt angezeigt.
   - `Right Column` - Das Menü wird rechts neben dem Inhalt angezeigt.

1. Um festzulegen, wie viele Details das Menü enthalten soll, legen Sie **[!UICONTROL Menu Detalization]** auf eine der folgenden Optionen fest:

   - `Only Children` - Enthält nur Unterseiten im Menü.
   - `Neighbours and Children` - Enthält Unterseiten und andere Seiten, die sich auf derselben Ebene in der Hierarchie befinden.

1. Um die Tiefe des Menüs zu bestimmen, geben Sie den **[!UICONTROL Maximal Depth]** für die maximale Anzahl der einzuschließenden Ebenen ein.

1. Um das Menü zu formatieren, wählen Sie eine **[!UICONTROL List Type]** aus:

   - `Unordered` - Die Menüoptionen sind nicht nummeriert und können mit oder ohne Aufzählungszeichen formatiert werden. Optionen für unsortierten Listentyp: Standard / Kreis / Scheibe / Quadrat
   - `Ordered` - Die Menüoptionen sind nummeriert und können als numerische, alphabetische oder römische Ziffern in Groß- oder Kleinbuchstaben formatiert werden.

1. Legen Sie **[!UICONTROL List Style]** auf eine der folgenden Einstellungen fest:

   - `Circle`
   - `Disc`
   - `Square`

1. Wenn der Knoten auch im Navigationsmenü sichtbar sein soll, scrollen Sie zu _Hauptnavigationsmenüoptionen_ und setzen Sie **[!UICONTROL Show in Navigation menu]** auf `Yes`.

   ![Optionen im Hauptnavigationsmenü](./assets/page-hierarchy-main-navigation-menu-options.png){width="250" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Save]**.
