---
title: Sortieren von Kategorieprodukten
description: Hier erfahren Sie, wie Sie die Positionierung von Produkten in einer Kategorie manuell oder durch Anwendung einer vordefinierten Sortierreihenfolge definieren.
exl-id: 09c66a5d-57d4-4e78-a8d8-e3047c1bd35a
feature: Catalog Management, Categories, Products
source-git-commit: 14c3eb7d54776382bfa196efdac446d42c8dc940
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---

# Sortieren von Kategorieprodukten

{{ee-feature}}

Die Position von Produkten in einer Kategorie kann manuell festgelegt werden, indem Produkte an die gewünschte Position gezogen und dort abgelegt werden oder indem eine vordefinierte Sortierreihenfolge angewendet wird. Standardmäßig können Produkte nach Lagerbestand, Alter, Farbe, Name, SKU und Preis sortiert werden. Die automatische Sortierung setzt die aktuelle Sortierreihenfolge außer Kraft und setzt alle manuell festgelegten Drag &amp; Drop-Positionen zurück. Die Sortierreihenfolge der Farben und die Mindestlagerebene, die für die Aufnahme von Produkten in die Liste erforderlich sein können, werden in der Konfiguration [Visual Merchandiser](../configuration-reference/catalog/visual-merchandiser.md) festgelegt.

>[!NOTE]
>
>Auf den Kategorieseiten werden `Out of stock` -Produkte immer **_nach_** `In Stock` Produkten in der Produktliste mit allen Sortierungstypen angezeigt.

Sie können die Kategorieoptionen für jede [Store-Ansicht](../stores-purchase/stores.md#add-stores) separat einrichten, um die Auswahl der Produkte, ihre relative Position in der Liste und die für Kategorieregeln verfügbaren Attribute zu bestimmen. Es gibt jedoch eine einzige, **_globale_** Sortierreihenfolge und Produktposition im Katalog und sie werden für alle [Store-Ansichten](../stores-purchase/store-views.md), Stores und Websites freigegeben.

## Schritt 1: Festlegen des Umfangs der Konfiguration

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Wählen Sie bei Bedarf die **[!UICONTROL Store View]** aus, für die die Einstellungen gelten.

   Bei einer Installation mit mehreren Stores wendet die Einstellung _[!UICONTROL Store View]_die Sortierreihenfolge auf alle verfügbaren Ansichten im Store an.

1. Wählen Sie links im Kategoriebaum die Kategorie aus, die Sie bearbeiten möchten.

   ![Kategoriestruktur](./assets/category-selected.png){width="700" zoomable="yes"}

## Schritt 2: Sortieren der Produkte

>[!NOTE]
>
>Beim Sortieren einer Kategorie nach einem Produktattribut werden Produkte mit denselben Attributwerten auch in aufsteigender Reihenfolge nach ihrem _[!UICONTROL Product ID]_sortiert.

Klicken Sie im Abschnitt _[!UICONTROL Products in Category]_auf das Symbol Kacheln ( ![Kacheln anzeigen](../assets/icon-view-tiles.png) ), um die Produktkacheln in einem Raster anzuzeigen. Verwenden Sie entweder die manuelle oder automatische Methode, um die Produkte zu sortieren.

![Produktkacheln](./assets/category-products-tiles.png){width="600" zoomable="yes"}

### Methode 1: Manuelle Sortierung

1. Legen Sie **[!UICONTROL Sort Order]** auf Ihre Voreinstellung fest.

   ![Sortierreihenfolge ](./assets/category-edit-sort-order.png){width="600" zoomable="yes"}

1. Um die neue Sortierreihenfolge anzuwenden, klicken Sie auf **[!UICONTROL Sort]**.

1. Um die Sortierreihenfolge zu speichern, klicken Sie auf **[!UICONTROL Save Category]**.

1. Wenn Sie dazu aufgefordert werden, aktualisieren Sie alle ungültigen Indexer.

### Methode 2: Automatische Sortierung

1. Setzen Sie **[!UICONTROL Match products by rule]** (![Umschalten yes](../assets/toggle-yes.png)) auf `Yes`.


1. Legen Sie **[!UICONTROL Automatic Sorting]** auf Ihre Voreinstellung fest.

1. Um eine Kategorieregel zu erstellen, befolgen Sie die Anweisungen im nächsten Schritt.

## Schritt 3: Erstellen einer Kategorieregel

1. Setzen Sie **[!UICONTROL Match products by rule]** (![Umschalten yes](../assets/toggle-yes.png)) auf `Yes`.

1. Klicken Sie auf **[!UICONTROL Add Condition]**.

1. Wählen Sie die **[!UICONTROL Attribute]** aus, die der Bedingung zugrunde liegt.

1. Setzen Sie **[!UICONTROL Operator]** auf einen der folgenden Werte:

   - `Equal`
   - `Not equal`
   - `Greater than`
   - `Greater than or equal to`
   - `Less than`
   - `Less than or equal to`
   - `Contains`

1. Geben Sie den entsprechenden **[!UICONTROL Value]** ein.

   ![Kategoriebedingung](./assets/category-rule-create.png){width="600" zoomable="yes"}

1. Um eine weitere Bedingung hinzuzufügen, klicken Sie auf **[!UICONTROL Add Condition]** und wiederholen Sie den Prozess.

## Schritt 4: Speichern, aktualisieren und überprüfen

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Category]**.

1. Wenn Sie aufgefordert werden, den Cache zu aktualisieren, klicken Sie auf **[!UICONTROL Cache Management]** und aktualisieren Sie jeden ungültigen Cache.

1. Überprüfen Sie in der Storefront, ob die Produktauswahl, Sortierung und Kategorieregeln ordnungsgemäß funktionieren.

   Wenn Sie Anpassungen vornehmen müssen, ändern Sie die Einstellungen und versuchen Sie es erneut.
