---
title: Hinzufügen von Attributen zu einem Produkt
description: Erfahren Sie, wie Sie Produkte in Ihrem Katalog Attribute hinzufügen.
exl-id: 1f92807a-2362-48a2-8d3a-4aef90a5671f
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '737'
ht-degree: 0%

---

# Hinzufügen von Attributen zu einem Produkt

Obwohl Attribute primär über die [Stores](../stores-purchase/stores-menu.md) Menü können Sie auch neue Attribute hinzufügen _im Flugbetrieb_ während der Arbeit an einem Produkt. Sie können aus der Liste der vorhandenen Attribute wählen oder ein Attribut erstellen. Das neue Attribut wird dem [Attributset](../catalog/attribute-sets.md) auf dem das Produkt basiert.

## Schritt 1: Attribut hinzufügen

1. Öffnen Sie das Produkt im Bearbeitungsmodus.

1. Klicken Sie oben rechts auf **[!UICONTROL Add Attribute]**.

   ![Neues Produkt mit standardmäßigem Attributsatz](./assets/product-attribute-add.png){width="600" zoomable="yes"}

1. Um dem Produkt ein vorhandenes Attribut hinzuzufügen, verwenden Sie die [Filtersteuerelemente](../getting-started/admin-grid-controls.md) , um das Attribut im Raster zu finden, und gehen Sie wie folgt vor:

   - Aktivieren Sie das Kontrollkästchen in der ersten Spalte jedes hinzugefügten Attributs.

   - Klicken **[!UICONTROL Add Selected]**.

   ![Attribut auswählen](./assets/product-attribute-add-select.png){width="600" zoomable="yes"}

1. Um ein neues Attribut zu definieren, klicken Sie auf **[!UICONTROL Create New Attribute]** und füllen Sie die Elemente in Schritt 2 aus.

## Schritt 2: Grundlegende Attributeigenschaften beschreiben

![Attributeigenschaften](./assets/product-attribute-add-new.png){width="600" zoomable="yes"}

1. under _[!UICONTROL Attribute Properties]_, geben Sie eine **[!UICONTROL Attribute Label]**, um das Attribut zu identifizieren.

1. Satz **[!UICONTROL Catalog Input Type for Store Owner]** der Art der [Eingabefeld](attributes-input-types.md) für die Dateneingabe verwendet werden.

   Wenn das Attribut für eine [konfigurierbares Produkt](product-create-configurable.md)auswählen `Dropdown`. Legen Sie anschließend **[!UICONTROL Required]** nach `Yes`.

1. Für `Dropdown` und `Multiple Select` Eingabetypen verwenden Sie folgende Schritte:

   - under **[!UICONTROL Values]** klicken **[!UICONTROL Add Value]**.

   - Geben Sie den ersten Wert ein, der in der Liste angezeigt werden soll.

     Sie können einen Wert für den Administrator und eine Übersetzung des Werts für jede Store-Ansicht eingeben. Wenn Sie nur eine Store-Ansicht haben, können Sie nur den Admin-Wert eingeben, der auch für die Storefront verwendet wird.

   - Klicks **[!UICONTROL Add Value]** und wiederholen Sie den vorherigen Schritt für jede Option, die Sie in die Liste aufnehmen möchten.

   - Auswählen **[!UICONTROL Is Default]** , um die Option als Standardwert zu verwenden.

   ![Werte](./assets/product-attribute-add-values-colors.png){width="600" zoomable="yes"}

1. Wenn Sie möchten, dass der Kunde eine Option auswählt, bevor das Produkt erworben werden kann, legen Sie **[!UICONTROL Required]** nach `Yes`.

## Schritt 3: Beschreibung der erweiterten Eigenschaften (optional)

![Erweiterte Attributeigenschaften](./assets/product-attribute-advanced-attribute-properties.png){width="600" zoomable="yes"}

1. Eindeutige Eingabe **[!UICONTROL Attribute Code]** in Kleinbuchstaben und ohne Leerzeichen.

1. Satz **[!UICONTROL Scope]** , um anzugeben, wo in Ihrer Store-Hierarchie das -Attribut verwendet werden kann.

   Wenn das Attribut für eine [konfigurierbares Produkt](product-create-configurable.md)auswählen `Global`.

1. Wenn dieses Attribut nur für dieses Produkt gilt, legen Sie **[!UICONTROL Unique Value]** nach `Yes`.

1. Um einen Gültigkeitstest für alle in ein Textfeld eingegebenen Daten durchzuführen, legen Sie **[!UICONTROL Input Validation for Store Owner]** auf den Datentyp, den das Feld enthalten soll.

   Dieses Feld ist nicht für Eingabetypen mit ausgewählten Werten verfügbar. Die Eingabevalidierung kann für Folgendes verwendet werden:

   - `Decimal Number`
   - `Integer Number`
   - `Email`
   - `URL`
   - `Letters`
   - `Letters (a-z, A-Z) or Numbers (0-9)`

   ![Eingabevalidierung](./assets/product-attribute-input-validation.png){width="500"}

1. Wenn Sie das Attribut als Spalte in das Raster Produkte einbeziehen möchten, legen Sie **[!UICONTROL Add to Column Options]** nach `Yes`.

1. Wenn Sie die _[!UICONTROL Products]_Raster nach dieser Spalte, festlegen **[!UICONTROL Use in Filter Options]**nach `Yes`.

## Schritt 4: Feldbezeichnung eingeben

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Manage titles]** Abschnitt.

1. Geben Sie einen **[!UICONTROL Title]** als Beschriftung für das Feld verwendet werden.

   Wenn Ihr Store in verschiedenen Sprachen verfügbar ist, können Sie für jede Ansicht einen übersetzten Titel eingeben.

   ![Titel verwalten](./assets/product-attribute-add-manage-titles.png){width="600" zoomable="yes"}

## Schritt 5: Beschreibung der Storefront-Eigenschaften

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Storefront Properties]** Abschnitt.

   ![Store-Eigenschaften](./assets/product-attribute-add-storefront-properties.png){width="600" zoomable="yes"}

1. Um das Attribut für die Suche verfügbar zu machen, legen Sie **[!UICONTROL Use in Search]** nach `Yes`.

1. Um das -Attribut in den Produktvergleich einzubeziehen, legen Sie **[!UICONTROL Comparable on Storefront]** nach `Yes`.

1. Um Dropdown, mehrere Auswahl- oder Preisattribute in die Navigation mit Ebenen einzubeziehen, legen Sie **[!UICONTROL Use in Search Results Layered Navigation]** auf einen der folgenden Werte zu:

   - `Filterable (with results)` - Die Navigation mit Ebenen umfasst nur die Filter, für die passende Produkte gefunden werden können. Ein Attributwert, der bereits für alle in der Liste angezeigten Produkte gilt, wird nicht als verfügbarer Filter angezeigt. Attributwerte mit einer Anzahl von Nullprodukt-Übereinstimmungen (0) werden ebenfalls aus der Liste der verfügbaren Filter weggelassen.<br/><br/>Die gefilterte Liste von Produkten enthält nur die Produkte, die mit dem Filter übereinstimmen. Die Produktliste wird nur aktualisiert, wenn die ausgewählten Filter die angezeigten Elemente ändern.

   - `Filterable (no results)` - Die Navigation mit Ebenen umfasst Filter für alle verfügbaren Attributwerte und deren Produktzahlen, einschließlich der Produkte mit null (0) Produktübereinstimmungen. Wenn es sich bei dem Attributwert um ein Muster handelt, wird der Wert als Filter angezeigt, jedoch ausgekreuzt.

1. Um in der mehrteiligen Navigation auf Suchergebnisseiten zu verwenden, legen Sie **[!UICONTROL Use in Search Results Navigation]** nach `Yes` und geben Sie eine Zahl in die **[!UICONTROL Position]** -Feld.

   Die Positionsnummer gibt die relative Position des Attributs innerhalb des Navigationsblocks mit Ebenen an.

1. Um das Attribut in den Preisregeln zu verwenden, legen Sie **[!UICONTROL Use for Promo Rule Conditions]** nach `Yes`.

1. Damit der Text mit HTML formatiert werden kann, legen Sie **[!UICONTROL Allow HTML Tags on Storefront]** nach `Yes`.

   Durch diese Einstellung wird der WYSIWYG-Editor beim Bearbeiten des Felds verfügbar.

1. Um das Attribut auf der Produktseite einzubeziehen, legen Sie **[!UICONTROL Visible on Catalog Pages on Storefront]** nach `Yes`.

1. Führen Sie die folgenden Einstellungen aus, wie von Ihrem Design unterstützt:

   - Um das -Attribut in Produktlisten aufzunehmen, legen Sie **[!UICONTROL Used in Product Listing]** nach `Yes`.

   - Um das Attribut als Sortierparameter für Produktlisten zu verwenden, legen Sie **[!UICONTROL Used for Sorting in Product Listing]** nach `Yes`.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Attribute]**.
