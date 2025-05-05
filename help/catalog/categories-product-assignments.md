---
title: Produktzuweisungen für Kategorien
description: Erfahren Sie, wie Sie mit den [!UICONTROL Products in Category] Einstellungen steuern können, welche Produkte derzeit der Kategorie zugewiesen sind.
exl-id: e7ab11c0-2d55-4824-a397-a1c858344d4f
feature: Catalog Management, Categories, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '811'
ht-degree: 0%

---

# Produktzuweisungen für Kategorien

Für eine Kategorie können Sie im Abschnitt _[!UICONTROL Products in Category]_&#x200B;die Produkte überprüfen, die derzeit der Kategorie zugewiesen sind. Die Suchfilter oben in jeder Spalte werden verwendet, um Produkte zur Kategorie hinzuzufügen und daraus zu entfernen. Sie können auch [Kategorieregeln](../merchandising-promotions/category-product-rules.md) verwenden (nur ![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce), um die Produktauswahl dynamisch zu ändern, wenn eine Reihe von Bedingungen erfüllt ist. Weitere Informationen finden Sie unter [Visual Merchandiser](../merchandising-promotions/visual-merchandiser.md)).

>[!TIP]
>
>Während der Einrichtung der Kategorieregel werden die Produkte _sortiert_, _abgeglichen_, _zugewiesen_ und _nicht zugewiesen_ gemäß dieser Regel **_only_**, wenn diese Kategorie gespeichert wird. Um sicherzustellen, dass ein neues Produkt gemäß der Regel zugewiesen wird, wenn Sie es zum Katalog hinzufügen, **Sie „jede Kategorie erneut speichern**, die so eingestellt ist, dass sie Produkten anhand der Regel entspricht. Wenn außerdem ein Produktbestandsstatus in `In Stock` oder `Out of Stock` geändert wird und Produkte in der Kategorie _sortiert_ gemäß der Regel **Automatische Sortierung** werden, müssen Sie auf **[!UICONTROL Save Category]** klicken.

![Kategorie Produkte](./assets/category-products-in-category.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Auf den Kategorieseiten werden `Out of stock` Produkte immer **_nachher_** `In Stock` in der Produktliste mit allen Sortiertypen angezeigt.

>[!NOTE]
>
>Die Spalte _Lager_ zeigt nur die verkaufbare Produktmenge für _&#x200B;**ausgewählten**&#x200B;_) an. Wenn mehrere Lager für Produkte verwaltet werden, sollten Sie zwischen den entsprechenden Umfängen wechseln, um andere _Lager_ Spaltenwerte im Raster _Kategorie Produkte_ anzuzeigen.

## Kategorieregel anwenden

{{ee-feature}}

1. Legen Sie **[!UICONTROL Match products by rule]** auf `Yes` fest.

   Die Optionen für die automatische Sortierung und Bedingung werden angezeigt.

   ![So ordnen Sie Produkte anhand einer Regel zu](./assets/category-match-products-by-rule.png){width="600" zoomable="yes"}

1. Legen Sie die **[!UICONTROL Automatic Sorting]** fest.

   Diese automatische Sortierung basiert auf aktuellen Bedingungen.

   - `Stock level` - Nach oben oder unten verschieben.
   - `Special price` - Nach oben oder unten verschieben.
   - `New Products` - Listet die neuesten Produkte zuerst auf.
   - `Color` - Alphabetisch nach Farbe sortieren.
   - `Name` - Sortieren Sie in auf- oder absteigender Reihenfolge nach Name.
   - `SKU` - In auf- oder absteigender Reihenfolge nach SKU sortieren
   - `Price` - Sortieren Sie in auf- oder absteigender Reihenfolge nach Preis.

1. Klicken Sie auf **[!UICONTROL Add Condition]** und führen Sie folgende Schritte aus:

   - Wählen Sie die **[!UICONTROL Attribute]** aus, auf der die Bedingung basiert.
   - Wählen Sie die **[!UICONTROL Operator]** aus, die zum Erstellen des Ausdrucks erforderlich ist.
   - Geben Sie die **[!UICONTROL Value]** ein, die abgeglichen werden soll.

   ![Bedingung zu Kategorieregel hinzufügen](./assets/category-rule-create.png){width="600" zoomable="yes"}

   Wiederholen Sie diesen Vorgang für jedes Attribut, das zur Beschreibung der zu erfüllenden Bedingungen verwendet werden soll. Um beispielsweise Produkte abzugleichen, die vor 7 bis 30 Tagen erstellt wurden, gehen Sie wie folgt vor:

   - Legen Sie **[!UICONTROL Date Created]** auf `Less than 30` fest.
   - Legen Sie **[!UICONTROL Logic]** auf `AND` fest.
   - Legen Sie **[!UICONTROL Date Modified]** auf `Greater than 7` fest.

1. Klicken Sie abschließend auf **[!UICONTROL Save Category]**.

### Seitenoptionen

| Option | Beschreibung |
|--- |--- |
| [!UICONTROL Match products by rule] | Bestimmt, ob die Liste der Produkte in der Kategorie durch eine Kategorieregel dynamisch generiert wird. Optionen: `Yes` / `No` |
| [!UICONTROL Automatic Sorting] | Wendet automatisch eine Sortierreihenfolge auf die Liste der Kategorieprodukte an. Optionen: <br/>`None`<br/>`Move low stock to top`<br/>`Move low stock to bottom`<br/>`Special price to top`<br/>`Special price to bottom`<br/>`Newest products first`<br/>`Sort by color`<br/>`Name: A - Z`<br/>`Name: Z - A`<br/>`SKU: Ascending`<br/>`SKU: Descending`<br/>`Price: High to Low`<br/>`Price: Low to High` |
| [!UICONTROL Add Condition] | Fügt eine weitere Bedingung zur Regel hinzu. |

{style="table-layout:auto"}

### Seitenbedingungen

| Option | Beschreibung |
|--- |--- |
| [!UICONTROL Attribute] | Bestimmt das Attribut, das als Grundlage für die Bedingung verwendet wird. Optionen: <br/>**[!UICONTROL Clone Category ID(s)]**: Klont Produkte dynamisch ohne Sortierung und Reihenfolge aus mehreren Kategorien basierend auf der Kategorie-ID.<br/>**[!UICONTROL Color]** - Enthält Produkte basierend auf Farbe. <br/>**[!UICONTROL Date Created (days ago)]**- Enthält Produkte basierend auf der Anzahl der Tage seit dem Hinzufügen der Produkte zum Katalog.<br/>**[!UICONTROL Date Modified (days ago)]** - Enthält Produkte basierend auf der Anzahl der Tage seit der letzten Änderung der Produkte. <br/>**[!UICONTROL Name]**- Enthält Produkte basierend auf dem Produktnamen.<br/>**[!UICONTROL Price]** - Enthält Produkte basierend auf dem Preis. <br/>**[!UICONTROL Quantity]**- Enthält Produkte basierend auf der Lagermenge.<br/>**&#x200B; SKU &#x200B;**- Enthält Produkte basierend auf SKU. |
| [!UICONTROL Operator] | Gibt den Operator an, der auf den Attributwert angewendet wird, um die Bedingung zu erfüllen. Sofern kein Operator angegeben ist, wird `Equal` als Standard verwendet. Optionen: `Equal` / `Not equal` / `Greater than` / `Greater than or equal to` / `Less than` / `Less than or equal to` / `Contains` |
| [!UICONTROL Value] | Gibt den Wert an, den das Attribut aufweisen muss, um die Bedingung zu erfüllen. |
| [!UICONTROL Logic] | Wird zum Definieren mehrerer Bedingungen verwendet und wird nur angezeigt, wenn eine andere Bedingung hinzugefügt wird. Optionen: `OR` / `AND` |

{style="table-layout:auto"}

>[!NOTE]
>
>Die Menge eines konfigurierbaren Produkts mit untergeordneten Optionen wird berechnet, indem alle verkäuflichen untergeordneten Produktmengen kombiniert werden. Betrachten wir ein Beispiel für ein konfigurierbares Produkt _Endurance Fitness-_) mit violetten, roten und gelben Farboptionen und unterschiedlichen Mengen von jedem. In diesem Szenario entspricht die Menge des übergeordneten Produkts der kombinierten verkäuflichen Menge der violetten, roten und gelben untergeordneten Produkte.

## Kontrollen


## Seitensteuerelemente

{{ee-feature}}

| Kontrolle | Beschreibung |
|----------|--------------|
| ![Als Liste anzeigen](../assets/icon-view-list.png) | Als Liste anzeigen |
| ![Als Kacheln anzeigen](../assets/icon-view-tiles.png) | Als Kacheln anzeigen |
| ![Umschalten auf](../assets/toggle-no.png) | Übereinstimmung nach Regel - Nein |
| ![Ja ein/aus](../assets/toggle-yes.png) | Übereinstimmung nach Regel - Ja |
| ![Steuerung verschieben](../assets/icon-move.png) | Mit der Drag-and-Drop-Steuerung können Sie ein Produkt erfassen und an eine andere Position auf der aktuellen Seite des Rasters verschieben. Weitere Informationen finden Sie unter [Visual Merchandiser](../merchandising-promotions/visual-merchandiser.md). |
| ![Positionsregler](../assets/control-position.png) | Bestimmt die Position des Produkts in der Liste. |

{style="table-layout:auto"}

## Seitensteuerelemente

{{ce-feature}}

| Kontrolle | Beschreibung |
|----------|--------------|
| ![Kontrollkästchen aktiviert](../assets/checkbox-selected.png) | Aktivieren Sie das Kontrollkästchen in der Kopfzeile der ersten Spalte, um alle Produkte auszuwählen oder alle Auswahlen zu deaktivieren. Das Steuerelement in der ersten Zeile bestimmt den Typ der Suche und kann so festgelegt werden, dass alle Datensätze einbezogen werden oder nur die Datensätze einbezogen werden, die der Kategorie zugewiesen oder nicht zugewiesen sind. Das Kontrollkästchen in der ersten Spalte jeder Zeile identifiziert Produkte, die der Kategorie hinzugefügt werden sollen. Optionen: `Yes` / `No` / `Any` |
| [!UICONTROL Search Filters] | Mit den Filtersteuerelementen oben in jeder Spalte können Sie bestimmte Werte eingeben, die Sie je nach Einstellung Alle auswählen in die Liste einbeziehen oder daraus auslassen möchten. |
| [!UICONTROL Reset Filter] | Löscht alle Suchfilter. |
| [!UICONTROL Search] | Durchsucht den Katalog anhand der Filterkriterien und zeigt das Ergebnis an. |

{style="table-layout:auto"}
