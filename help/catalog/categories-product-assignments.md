---
title: Kategorieproduktzuweisungen
description: Erfahren Sie mehr über die Verwendung der [!UICONTROL Products in Category]-Einstellungen, um zu steuern, welche Produkte derzeit der Kategorie zugewiesen sind.
exl-id: e7ab11c0-2d55-4824-a397-a1c858344d4f
feature: Catalog Management, Categories, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '811'
ht-degree: 0%

---

# Kategorieproduktzuweisungen

Verwenden Sie für eine Kategorie den Abschnitt _[!UICONTROL Products in Category]_, um die Produkte zu überprüfen, die derzeit der Kategorie zugewiesen sind. Die Suchfilter oben in jeder Spalte werden verwendet, um Produkte zur Kategorie hinzuzufügen und daraus zu entfernen. Sie können auch [Kategorieregeln](../merchandising-promotions/category-product-rules.md) ( ![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce) verwenden, um die Produktauswahl dynamisch zu ändern, wenn eine Reihe von Bedingungen erfüllt ist. Weitere Informationen finden Sie unter [Visual Merchandiser](../merchandising-promotions/visual-merchandiser.md)).

>[!TIP]
>
>Während der Einrichtung von Kategorieregeln werden die Produkte gemäß dieser Regel **_nur_** sortiert _sorted_, _match_, _assigned_ und _unassigned_. Um sicherzustellen, dass ein neues Produkt gemäß der Regel zugewiesen wird, wenn Sie es zum Katalog hinzufügen, müssen Sie jede Kategorie **erneut speichern, die so eingestellt ist, dass Produkte nach Regel übereinstimmen.** Außerdem müssen Sie auf **[!UICONTROL Save Category]** klicken, wenn der Status des Produktbestands in `In Stock` oder `Out of Stock` geändert wird und die Produkte in der Kategorie _sortiert_ gemäß der Regel **Automatische Sortierung** sind.

![Kategorieprodukte](./assets/category-products-in-category.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Auf den Kategorieseiten werden `Out of stock` -Produkte immer **_nach_** `In Stock` Produkten in der Produktliste mit allen Sortierungstypen angezeigt.

>[!NOTE]
>
>In der Spalte _Stock_ wird nur die verkaufbare Produktmenge für den Bereich _**ausgewählte Kategorie**_ angezeigt. Wenn mehrere Lager für Produkte verwaltet werden, sollten Sie zwischen den entsprechenden Bereichen wechseln, um andere _Stock_ -Spaltenwerte im Raster _Kategorieprodukte_ anzuzeigen.

## Anwenden einer Kategorieregel

{{ee-feature}}

1. Setzen Sie **[!UICONTROL Match products by rule]** auf `Yes`.

   Die automatischen Sortierungs- und Bedingungsoptionen werden angezeigt.

   ![So gleichen Sie Produkte nach Regel ab](./assets/category-match-products-by-rule.png){width="600" zoomable="yes"}

1. Legen Sie die **[!UICONTROL Automatic Sorting]** -Reihenfolge fest.

   Diese automatische Sortierung basiert auf aktuellen Bedingungen.

   - `Stock level` - Nach oben oder unten verschieben.
   - `Special price` - Nach oben oder unten verschieben.
   - `New Products` - Liste der neuesten Produkte zuerst.
   - `Color` - Sortieren Sie alphabetisch nach Farbe.
   - `Name` - Sortieren Sie die Sortierung in auf- oder absteigender Reihenfolge nach Name.
   - `SKU` - Sortieren in auf- oder absteigender Reihenfolge nach SKU
   - `Price` - Sortieren Sie die Sortierung in auf- oder absteigender Reihenfolge nach Preis.

1. Klicken Sie auf **[!UICONTROL Add Condition]** und führen Sie die folgenden Schritte aus:

   - Wählen Sie die **[!UICONTROL Attribute]** aus, die der Bedingung zugrunde liegt.
   - Wählen Sie den für die Erstellung des Ausdrucks erforderlichen **[!UICONTROL Operator]** aus.
   - Geben Sie den **[!UICONTROL Value]** ein, der abgeglichen werden soll.

   ![Bedingung zur Kategorieregel hinzufügen](./assets/category-rule-create.png){width="600" zoomable="yes"}

   Wiederholen Sie diesen Vorgang für jedes Attribut, das zur Beschreibung der zu erfüllenden Bedingungen verwendet werden soll. Um beispielsweise Produkte abzugleichen, die vor 7 bis 30 Tagen erstellt wurden, gehen Sie wie folgt vor:

   - Setzen Sie **[!UICONTROL Date Created]** auf `Less than 30`.
   - Setzen Sie **[!UICONTROL Logic]** auf `AND`.
   - Setzen Sie **[!UICONTROL Date Modified]** auf `Greater than 7`.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Category]**.

### Seitenoptionen

| Option | Beschreibung |
|--- |--- |
| [!UICONTROL Match products by rule] | Bestimmt, ob die Liste der Produkte in der Kategorie von einer Kategorieregel dynamisch generiert wird. Optionen: `Yes` / `No` |
| [!UICONTROL Automatic Sorting] | wendet automatisch eine Sortierreihenfolge auf die Liste der Kategorieprodukte an. Optionen: <br/>`None`<br/>`Move low stock to top`<br/>`Move low stock to bottom`<br/>`Special price to top`<br/>`Special price to bottom`<br/>`Newest products first`<br/>`Sort by color`<br/>`Name: A - Z`<br/>`Name: Z - A`<br/>`SKU: Ascending`<br/>`SKU: Descending`<br/>`Price: High to Low`<br/>`Price: Low to High` |
| [!UICONTROL Add Condition] | Fügt der Regel eine weitere Bedingung hinzu. |

{style="table-layout:auto"}

### Seitenbedingungen

| Option | Beschreibung |
|--- |--- |
| [!UICONTROL Attribute] | Bestimmt das Attribut, das als Grundlage für die Bedingung verwendet wird. Optionen: <br/>**[!UICONTROL Clone Category ID(s)]**- Dynamisches Klonen von Produkten ohne Sortierung und Reihenfolge aus mehreren Kategorien basierend auf Kategorie-ID.<br/>**[!UICONTROL Color]** - Umfasst Produkte basierend auf Farbe. <br/>**[!UICONTROL Date Created (days ago)]**- Umfasst Produkte basierend auf der Anzahl der Tage seit dem Hinzufügen der Produkte zum Katalog.<br/>**[!UICONTROL Date Modified (days ago)]** - Umfasst Produkte basierend auf der Anzahl der Tage seit der letzten Änderung der Produkte. <br/>**[!UICONTROL Name]**- Umfasst Produkte auf der Grundlage des Produktnamen.<br/>**[!UICONTROL Price]** - Umfasst Produkte basierend auf dem Preis. <br/>**[!UICONTROL Quantity]**- Umfasst Produkte auf der Grundlage der Lagermenge.<br/>** SKU **- Umfasst Produkte auf der Grundlage der SKU. |
| [!UICONTROL Operator] | Gibt den Operator an, der auf den Attributwert angewendet wird, um die Bedingung zu erfüllen. Wenn kein Operator angegeben ist, wird `Equal` als Standard verwendet. Optionen: `Equal` / `Not equal` / `Greater than` / `Greater than or equal to` / `Less than` / `Less than or equal to` / `Contains` |
| [!UICONTROL Value] | Gibt den Wert an, den das Attribut aufweisen muss, um die Bedingung zu erfüllen. |
| [!UICONTROL Logic] | Wird zur Definition mehrerer Bedingungen verwendet und wird nur angezeigt, wenn eine andere Bedingung hinzugefügt wird. Optionen: `OR` / `AND` |

{style="table-layout:auto"}

>[!NOTE]
>
>Die Menge eines konfigurierbaren Produkts mit untergeordneten Optionen wird durch Kombination aller verkaufbaren untergeordneten Produktmengen berechnet. Betrachten Sie ein Beispiel für ein konfigurierbares Produkt _Ausdauungs-Fitness-Tank_ mit lilafarbenen, roten und gelben Farboptionen und verschiedenen Mengen von jedem. In diesem Szenario ist die übergeordnete Produktmenge die kombinierte verkaufbare Menge der lilafarbenen, roten und gelben untergeordneten Produkte.

## Steuerelemente


## Seitensteuerelemente

{{ee-feature}}

| Kontrolle | Beschreibung |
|----------|--------------|
| ![Als Liste anzeigen](../assets/icon-view-list.png) | Als Liste anzeigen |
| ![Als Kacheln anzeigen](../assets/icon-view-tiles.png) | Als Kacheln anzeigen |
| ![Umschalten Nr.](../assets/toggle-no.png) | Übereinstimmung nach Regel - Nein |
| ![Ja umschalten](../assets/toggle-yes.png) | Übereinstimmung nach Regel - Ja |
| ![Controller verschieben](../assets/icon-move.png) | Mit der Drag &amp; Drop-Steuerung können Sie ein Produkt abrufen und an eine andere Position auf der aktuellen Seite des Rasters verschieben. Weitere Informationen finden Sie unter [Visual Merchandiser](../merchandising-promotions/visual-merchandiser.md). |
| ![Positionscontroller](../assets/control-position.png) | Bestimmt die Position des Produkts in der Liste. |

{style="table-layout:auto"}

## Seitensteuerelemente

{{ce-feature}}

| Kontrolle | Beschreibung |
|----------|--------------|
| ![Ausgewähltes Kontrollkästchen](../assets/checkbox-selected.png) | Verwenden Sie das Kontrollkästchen in der Kopfzeile der ersten Spalte, um alle Produkte auszuwählen oder alle Auswahlen zu löschen. Das Steuerelement in der ersten Zeile bestimmt die Art der Suche und kann so eingestellt werden, dass es jeden beliebigen Datensatz einbezieht oder nur die Datensätze einbezieht, die der Kategorie zugewiesen sind oder nicht. Mit dem Kontrollkästchen in der ersten Spalte jeder Zeile werden die Produkte identifiziert, die der Kategorie hinzugefügt werden sollen. Optionen: `Yes` / `No` / `Any` |
| [!UICONTROL Search Filters] | Die Filtersteuerelemente oben in jeder Spalte können verwendet werden, um bestimmte Werte einzugeben, die Sie je nach Einstellung Alle auswählen entweder einbeziehen oder aus der Liste auslassen möchten. |
| [!UICONTROL Reset Filter] | Löscht alle Suchfilter. |
| [!UICONTROL Search] | Durchsucht den Katalog nach den Filterkriterien und zeigt das Ergebnis an. |

{style="table-layout:auto"}
