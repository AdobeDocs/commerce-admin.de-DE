---
title: Hinzufügen von Attributen zu einem Produkt
description: Erfahren Sie, wie Sie Attribute zu Produkten in Ihrem Katalog hinzufügen.
exl-id: 1f92807a-2362-48a2-8d3a-4aef90a5671f
feature: Catalog Management, Products
source-git-commit: 99049260b4ff490845affd1c98fa4d2536edebd7
workflow-type: tm+mt
source-wordcount: '790'
ht-degree: 0%

---

# Hinzufügen von Attributen zu einem Produkt

Obwohl Attribute in erster Linie über die [Stores](../stores-purchase/stores-menu.md) -Menü können Sie auch neue Attribute hinzufügen _im laufenden Betrieb_ während der Arbeit an einem Produkt. Sie können aus der Liste der vorhandenen Attribute auswählen oder ein Attribut erstellen. Das neue Attribut wird zum hinzugefügt [Attributsatz](../catalog/attribute-sets.md) auf dem das Produkt basiert.

## Schritt 1: Attribut hinzufügen

1. Öffnen Sie das Produkt im Bearbeitungsmodus.

1. Klicken Sie oben rechts auf **[!UICONTROL Add Attribute]**.

   ![Neues Produkt mit Standardattribut festgelegt](./assets/product-attribute-add.png){width="600" zoomable="yes"}

1. Um ein vorhandenes Attribut zum Produkt hinzuzufügen, verwenden Sie die [Filtersteuerelemente](../getting-started/admin-grid-controls.md) Gehen Sie wie folgt vor, um das Attribut im Raster zu finden:

   - Aktivieren Sie das Kontrollkästchen in der ersten Spalte jedes Attributs, das hinzugefügt werden soll.

   - Klick **[!UICONTROL Add Selected]**.

   ![Attribut auswählen](./assets/product-attribute-add-select.png){width="600" zoomable="yes"}

1. Um ein neues Attribut zu definieren, klicken Sie auf **[!UICONTROL Create New Attribute]** und schließen Sie die Elemente in Schritt 2 ab.

## Schritt 2: Beschreiben der grundlegenden Attributeigenschaften

![Attributeigenschaften](./assets/product-attribute-add-new.png){width="600" zoomable="yes"}

1. Unter _[!UICONTROL Attribute Properties]_, geben Sie ein **[!UICONTROL Attribute Label]**, um das Attribut zu identifizieren.

1. set **[!UICONTROL Catalog Input Type for Store Owner]** auf den Typ von [Eingabekontrolle](attributes-input-types.md) Zur Dateneingabe.

   Wenn das Attribut für ein [konfigurierbares Produkt](product-create-configurable.md), wählen Sie `Dropdown`. Legen Sie dann fest **[!UICONTROL Required]** bis `Yes`.

1. für `Dropdown` und `Multiple Select` Führen Sie die folgenden Schritte aus:

   - Unter **[!UICONTROL Values]**, klicken Sie auf **[!UICONTROL Add Value]**.

   - Geben Sie den ersten Wert ein, der in der Liste angezeigt werden soll.

     Sie können für jede Shop-Ansicht einen Wert für den Administrator und eine Übersetzung des Werts eingeben. Wenn Sie nur eine Store-Ansicht haben, können Sie nur den Admin-Wert eingeben. Dieser wird auch für die Storefront verwendet.

   - Klick **[!UICONTROL Add Value]** und wiederholen Sie den vorherigen Schritt für jede Option, die Sie in die Liste aufnehmen möchten.

   - Auswählen **[!UICONTROL Is Default]** , um die Option als Standardwert zu verwenden.

   ![Werte](./assets/product-attribute-add-values-colors.png){width="600" zoomable="yes"}

1. Wenn Sie möchten, dass der Kunde eine Option auswählen muss, bevor das Produkt gekauft werden kann, legen Sie Folgendes fest **[!UICONTROL Required]** bis `Yes`.

## Schritt 3: Erweiterte Eigenschaften beschreiben (optional)

![Erweiterte Attributeigenschaften](./assets/product-attribute-advanced-attribute-properties.png){width="600" zoomable="yes"}

1. Eindeutigen Wert eingeben **[!UICONTROL Attribute Code]** in Kleinbuchstaben und ohne Leerzeichen.

1. set **[!UICONTROL Scope]** um anzugeben, wo in der Store-Hierarchie das Attribut verwendet werden kann.

   Wenn das Attribut für ein [konfigurierbares Produkt](product-create-configurable.md), wählen Sie `Global`.

1. Wenn dieses Attribut nur für dieses Produkt gilt, setzen Sie **[!UICONTROL Unique Value]** bis `Yes`.

1. Um einen Gültigkeitstest für alle in ein Textfeld eingegebenen Daten durchzuführen, legen Sie Folgendes fest: **[!UICONTROL Input Validation for Store Owner]** auf den Typ der Daten, die das Feld enthalten soll.

   Dieses Feld ist nicht für Eingabetypen mit ausgewählten Werten verfügbar. Die Eingabevalidierung kann für eine der folgenden Aktionen verwendet werden:

   - `Decimal Number`
   - `Integer Number`
   - `Email`
   - `URL`
   - `Letters`
   - `Letters (a-z, A-Z) or Numbers (0-9)`

   ![Eingabevalidierung](./assets/product-attribute-input-validation.png){width="500"}

1. Wenn Sie das Attribut als Spalte in das Produktraster aufnehmen möchten, legen Sie Folgendes fest **[!UICONTROL Add to Column Options]** bis `Yes`.

1. Wenn Sie in der Lage sein möchten, die _[!UICONTROL Products]_Raster nach dieser Spalte, festlegen **[!UICONTROL Use in Filter Options]**bis `Yes`.

## Schritt 4: Geben Sie die Feldbezeichnung ein

1. Expand ![Erweiterungsauswahl](../assets/icon-display-expand.png) Die **[!UICONTROL Manage titles]** -Abschnitt.

1. Geben Sie ein **[!UICONTROL Title]** Wird als Bezeichnung für das Feld verwendet.

   Wenn Ihr Store in verschiedenen Sprachen verfügbar ist, können Sie für jede Ansicht einen übersetzten Titel eingeben.

   ![Titel verwalten](./assets/product-attribute-add-manage-titles.png){width="600" zoomable="yes"}

## Schritt 5: Beschreiben Sie die Eigenschaften der Storefront

1. Expand ![Erweiterungsauswahl](../assets/icon-display-expand.png) Die **[!UICONTROL Storefront Properties]** -Abschnitt.

   ![Storefront-Eigenschaften](./assets/product-attribute-add-storefront-properties.png){width="600" zoomable="yes"}

1. Um das Attribut für die Suche verfügbar zu machen, legen Sie Folgendes fest **[!UICONTROL Use in Search]** bis `Yes`.

1. Um das Attribut in den Produktvergleich einzuschließen, legen Sie Folgendes fest **[!UICONTROL Comparable on Storefront]** bis `Yes`.

1. Um Dropdown-, Mehrfachauswahl- oder Preisattribute in die mehrschichtige Navigation einzuschließen, legen Sie Folgendes fest **[!UICONTROL Use in Search Results Layered Navigation]** eine der folgenden Möglichkeiten:

   - `Filterable (with results)` - Die mehrschichtige Navigation umfasst nur die Filter, für die passende Produkte gefunden werden können. Attributwerte, die bereits für alle in der Liste aufgeführten Produkte gelten, werden nicht als verfügbare Filter angezeigt. Attributwerte mit einer Anzahl von null (0) Produktübereinstimmungen werden ebenfalls nicht in der Liste der verfügbaren Filter angezeigt.<br/><br/>Die gefilterte Liste von Produkten enthält nur die Produkte, die dem Filter entsprechen. Die Produktliste wird nur aktualisiert, wenn die ausgewählten Filter das Gezeigte ändern.

   - `Filterable (no results)` - Die mehrschichtige Navigation umfasst Filter für alle verfügbaren Attributwerte und ihre Produktanzahl, einschließlich der Produkte mit null (0) Produktübereinstimmungen. Wenn der Attributwert ein Farbfeld ist, wird der Wert als Filter angezeigt, aber durchgestrichen.

   >[!NOTE]
   >
   >Wenn die _[!UICONTROL Use in Search]_Einstellung ist festgelegt auf `No`, die_[!UICONTROL Use in Search Results Layered Navigation]_ -Einstellung wird nicht angezeigt und das Produktattribut wird bei der Suche mit keinem verwendet [!UICONTROL Use in Layered Navigation] Einstellwert.

1. Um das -Attribut in der mehrschichtigen Navigation auf Suchergebnisseiten zu verwenden, legen Sie Folgendes fest **[!UICONTROL Use in Search Results Layered Navigation]** bis `Yes` und geben Sie eine Zahl in das Feld **[!UICONTROL Position]** Feld.

   Die Positionsnummer gibt die relative Position des Attributs innerhalb des mehrschichtigen Navigationsblocks an.

   >[!NOTE]
   >
   >Die _[!UICONTROL Position]_Das Feld ist standardmäßig abgeblendet und Sie müssen das Attribut speichern, bevor Sie diese Einstellung ändern können.

1. Um das Attribut in Preisregeln zu verwenden, legen Sie Folgendes fest **[!UICONTROL Use for Promo Rule Conditions]** bis `Yes`.

1. Um die Textformatierung mit HTML zuzulassen, legen Sie Folgendes fest **[!UICONTROL Allow HTML Tags on Storefront]** bis `Yes`.

   Durch diese Einstellung wird der WYSIWYG-Editor beim Bearbeiten des Felds verfügbar.

1. Um das Attribut in die Produktseite aufzunehmen, legen Sie Folgendes fest **[!UICONTROL Visible on Catalog Pages on Storefront]** bis `Yes`.

1. Füllen Sie die folgenden Einstellungen wie vom Design unterstützt aus:

   - Um das Attribut in Produktlisten aufzunehmen, legen Sie Folgendes fest **[!UICONTROL Used in Product Listing]** bis `Yes`.

   - Um das Attribut als Sortierparameter für Produktlisten zu verwenden, legen Sie Folgendes fest **[!UICONTROL Used for Sorting in Product Listing]** bis `Yes`.

1. Klicken Sie abschließend auf **[!UICONTROL Save Attribute]**.
