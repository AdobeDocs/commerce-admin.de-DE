---
title: Sortieren von Kategorieprodukten
description: Erfahren Sie, wie Sie die Positionierung von Produkten in einer Kategorie manuell oder durch Anwenden einer vordefinierten Sortierreihenfolge definieren.
exl-id: 09c66a5d-57d4-4e78-a8d8-e3047c1bd35a
feature: Catalog Management, Categories, Products
source-git-commit: 5aea3aa13ab0eb74866fc0cbcbfe08b5099abe95
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# Sortieren von Kategorieprodukten

{{ee-feature}}

Die Position von Produkten in einer Kategorie kann manuell festgelegt werden, indem Produkte per Drag-and-Drop an die gewünschte Position gezogen oder eine vordefinierte Sortierreihenfolge angewendet wird. Standardmäßig können Produkte nach Lagerbestand, Alter, Farbe, Name, SKU und Preis sortiert werden. Die automatische Sortierung überschreibt die aktuelle Sortierreihenfolge und setzt alle manuell eingestellten Drag-and-Drop-Positionen zurück. Die Sortierreihenfolge der Farben und der Mindestbestand, der für Produkte, die in die Liste aufgenommen werden sollen, erforderlich sein kann, werden in der Konfiguration [Visual Merchandiser](../configuration-reference/catalog/visual-merchandiser.md) festgelegt.

Sie können die Kategorieoptionen für jede [Store-Ansicht](../stores-purchase/stores.md#add-stores) separat einrichten, um die Auswahl von Produkten, ihre relative Position in der Liste und die Attribute zu bestimmen, die für Kategorieregeln verfügbar sind. Es gibt jedoch eine einzige, **_globale_** Sortierreihenfolge und Produktposition im Katalog und sie werden für alle [Store-Ansichten](../stores-purchase/store-views.md) Stores und Websites freigegeben.

## Schritt 1: Festlegen des Umfangs der Konfiguration

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Wählen Sie bei Bedarf die **[!UICONTROL Store View]** aus, für die die Einstellungen gelten.

   Bei einer Multi-Store-Installation wird die Sortierreihenfolge mit der _[!UICONTROL Store View]_-Einstellung auf alle verfügbaren Ansichten im Store angewendet.

1. Wählen Sie in der Kategoriestruktur auf der linken Seite die Kategorie aus, die Sie bearbeiten möchten.

   ![Kategoriestruktur](./assets/category-selected.png){width="700" zoomable="yes"}

## Schritt 2: Sortieren der Produkte

>[!NOTE]
>
>Beim Sortieren einer Kategorie nach einem Produktattribut werden Produkte mit denselben Attributwerten auch nach ihrem _[!UICONTROL Product ID]_&#x200B;in aufsteigender Reihenfolge sortiert.

Klicken Sie im Abschnitt _[!UICONTROL Products in Category]_&#x200B;auf das Symbol Kacheln ![Anzeigen von Kacheln](../assets/icon-view-tiles.png) , um die Produktkacheln in einem Raster anzuzeigen. Sortieren Sie die Produkte entweder manuell oder automatisch.

![Produktkacheln](./assets/category-products-tiles.png){width="600" zoomable="yes"}

### Methode 1: Manuelle Sortierung

1. Legen Sie **[!UICONTROL Sort Order]** auf Ihre Voreinstellung fest.

   ![Sortierreihenfolge](./assets/category-edit-sort-order.png){width="600" zoomable="yes"}

1. Um die neue Sortierreihenfolge anzuwenden, klicken Sie auf **[!UICONTROL Sort]**.

1. Um die Sortierreihenfolge zu speichern, klicken Sie auf **[!UICONTROL Save Category]**.

1. Aktualisieren Sie alle ungültigen Indexer, wenn Sie dazu aufgefordert werden.

### Methode 2: Automatische Sortierung

1. Setzen Sie **[!UICONTROL Match products by rule]** (![Ja ein](../assets/toggle-yes.png)) auf `Yes`.


1. Legen Sie **[!UICONTROL Automatic Sorting]** auf Ihre Voreinstellung fest.

1. Um eine Kategorieregel zu erstellen, befolgen Sie die Anweisungen im nächsten Schritt.

## Schritt 3: Kategorieregel erstellen

1. Setzen Sie **[!UICONTROL Match products by rule]** (![Ja ein](../assets/toggle-yes.png)) auf `Yes`.

1. Klicken Sie auf **[!UICONTROL Add Condition]**.

1. Wählen Sie die **[!UICONTROL Attribute]** aus, auf der die Bedingung basiert.

1. Legen Sie **[!UICONTROL Operator]** auf eine der folgenden Einstellungen fest:

   - `Equal`
   - `Not equal`
   - `Greater than`
   - `Greater than or equal to`
   - `Less than`
   - `Less than or equal to`
   - `Contains`

1. Geben Sie den entsprechenden **[!UICONTROL Value]** ein.

   ![Kategoriebedingung](./assets/category-rule-create.png){width="600" zoomable="yes"}

1. Um eine weitere Bedingung hinzuzufügen, klicken Sie auf **[!UICONTROL Add Condition]** und wiederholen Sie den Vorgang.

## Schritt 4: Speichern, aktualisieren und überprüfen

1. Klicken Sie abschließend auf **[!UICONTROL Save Category]**.

1. Wenn Sie aufgefordert werden, den Cache zu aktualisieren, klicken Sie auf **[!UICONTROL Cache Management]** und aktualisieren Sie jeden ungültigen Cache.

1. Überprüfen Sie in der Storefront, ob die Regeln für Produktauswahl, Sortierung und Kategorie korrekt funktionieren.

   Wenn Sie Anpassungen vornehmen müssen, ändern Sie die Einstellungen und versuchen Sie es erneut.
