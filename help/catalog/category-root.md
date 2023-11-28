---
title: Stammkategorie und Hierarchie
description: Erfahren Sie mehr über die Kategoriehierarchie und die Stammkategorie, die als Container für das Hauptmenü in der Kategoriestruktur fungiert.
exl-id: b419cb45-4fe5-42c4-be20-667c7e1e4354
feature: Catalog Management, Categories, Site Navigation
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 0%

---

# Stammkategorie und Hierarchie

Die Produkte im Hauptmenü werden durch die der [store](../stores-purchase/stores.md#add-stores). Die Stammkategorie ist im Wesentlichen ein Container für das Hauptmenü im Kategoriebaum. Sie können eine Stammkategorie mit einem völlig neuen Satz von Produkten erstellen oder Produkte aus einer vorhandenen Stammkategorie kopieren. Die Stammkategorie kann dem aktuellen Store oder einem anderen Store auf derselben Website zugewiesen werden.

![Kataloghierarchiediagramm](./assets/catalog-hierarchy-scope.svg){width="550"}

Vom Administrator aus ähnelt die Kategoriestruktur einer Aufwärtsstruktur, wobei sich der Stamm oben befindet. Der Stamm hat einen Namen, aber keinen URL-Schlüssel und wird nicht im [oberste Navigation](navigation-top.md) des Stores. Alle anderen Kategorien im Menü sind unter dem Stammverzeichnis verschachtelt. Da die Stammkategorie die höchste Ebene des Katalogs ist, kann in Ihrem Store jeweils nur eine Stammkategorie aktiv sein. Sie können jedoch zusätzliche Stammkategorien für alternative Katalogstrukturen und verschiedene Stores erstellen.

Im folgenden Beispiel wird gezeigt, wie eine Stammkategorie erstellt und einem anderen Speicher zugewiesen wird.

## Schritt 1: Erstellen einer Stammkategorie

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Klicken Sie links auf **[!UICONTROL Add Root Category]**.

   ![Neue Stammkategorie](./assets/category-root-ee.png){width="600" zoomable="yes"}

1. Geben Sie einen **[!UICONTROL Category Name]**.

   Der gewählte Name wird zunächst allen Store-Ansichten zugewiesen.

1. Wenn Sie Produkte aus dem aktuellen Katalog zum Katalog hinzufügen möchten, gehen Sie wie folgt vor:

   - Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die _Produkte der Kategorie_ Abschnitt.

   - Verwenden Sie die [Suchfilter](../getting-started/admin-grid-controls.md) , um die gewünschten Produkte zu finden, und aktivieren Sie das Kontrollkästchen für jedes Produkt, das Sie in den neuen Katalog kopieren möchten.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]**.

## Schritt 2: Hauptmenü erstellen

1. Wählen Sie links die neue Stammkategorie aus, die Sie im vorherigen Schritt erstellt haben.

1. So erstellen Sie die [Kategoriestruktur](category-create.md) Klicken Sie im Hauptmenü auf **[!UICONTROL Add Subcategory]** und befolgen Sie die Anweisungen.

## Schritt 3: Zuweisen der Stammkategorie zum Store

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. Im _Stores_ Klicken Sie in der Rasterspalte auf den Store, dem Sie den neuen Katalog zuweisen möchten.

1. Satz **[!UICONTROL Root Category]** in die neue Stammkategorie, die Sie erstellt haben.

1. Stellen Sie sicher, dass der Store über eine **[!UICONTROL Default Store View]** zugewiesen wurde.

   Der Laden muss mindestens eine [Store-Ansicht](../stores-purchase/store-views.md).

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Store]**.

1. Gehen Sie wie folgt vor, um zu überprüfen, ob der Store über einen neuen Katalog verfügt:

   - Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

     Alle Produkte, die in den neuen Katalog kopiert wurden, werden im Raster angezeigt.

   - Um zu überprüfen, ob der neue Katalog und das Hauptmenü ordnungsgemäß funktionieren, besuchen Sie die Storefront.
