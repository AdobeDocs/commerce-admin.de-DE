---
title: Stammkategorie und -hierarchie
description: Erfahren Sie mehr über die Kategoriehierarchie und die Stammkategorie, die als Container für das Hauptmenü in der Kategoriestruktur dient.
exl-id: b419cb45-4fe5-42c4-be20-667c7e1e4354
feature: Catalog Management, Categories, Site Navigation
TQID: https://experienceleague.adobe.com/nkUEOu8IqMM21waPwmkp76YckH6cToL6MiaSK--klho
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c18ed297-2187-4aec-affb-9d9654eca6fc
subfeature_v2: id: e91a50b1-0b31-436e-9033-00e4776e94cb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 437
ht-degree: 0%

---

# Stammkategorie und -hierarchie

Die Produkte im Hauptmenü werden durch die Stammkategorie bestimmt, die dem &quot;[&quot; zugewiesen ](../stores-purchase/stores.md#add-stores). Die Stammkategorie ist im Grunde ein Container für das Hauptmenü in der Kategoriestruktur. Sie können eine Stammkategorie mit einem völlig neuen Satz von Produkten erstellen oder Produkte aus einer vorhandenen Stammkategorie kopieren. Die Stammkategorie kann dem aktuellen Store oder einem anderen Store auf derselben Website zugewiesen werden.

![Katalog-Hierarchie-Diagramm](./assets/catalog-hierarchy-scope.svg){width="550"}

Von Admin aus gesehen ist die Kategoriestruktur wie eine umgekehrte Struktur, wobei das Stammverzeichnis oben ist. Der Stamm hat einen Namen, aber keinen URL-Schlüssel und wird nicht in der [oberen Navigation](navigation-top.md) des Stores angezeigt. Alle anderen Kategorien im Menü sind unter dem Stamm verschachtelt. Da die Stammkategorie die höchste Ebene des Katalogs ist, kann für Ihren Store immer nur eine Stammkategorie aktiv sein. Sie können jedoch zusätzliche Stammkategorien für alternative Katalogstrukturen und verschiedene Stores erstellen.

Das folgende Beispiel zeigt, wie Sie eine Stammkategorie erstellen und sie einem anderen Store zuweisen.

## Schritt 1: Erstellen einer Stammkategorie

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Klicken Sie links auf **[!UICONTROL Add Root Category]**.

   ![Neue Stammkategorie](./assets/category-root-ee.png){width="600" zoomable="yes"}

1. Geben Sie einen **[!UICONTROL Category Name]** ein.

   Der ausgewählte Name wird zunächst allen Store-Ansichten zugewiesen.

1. Wenn Sie Produkte aus dem aktuellen Katalog zum Katalog hinzufügen möchten, gehen Sie wie folgt vor:

   - Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt _Produkte in Kategorie_.

   - Verwenden Sie die [Suchfilter](../getting-started/admin-grid-controls.md) um die gewünschten Produkte zu finden, und aktivieren Sie das Kontrollkästchen für jedes Produkt, das Sie in den neuen Katalog kopieren möchten.

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.

## Schritt 2: Aufbauen des Hauptmenüs

1. Wählen Sie links die neue Stammkategorie aus, die Sie im vorherigen Schritt erstellt haben.

1. Um die [Kategoriestruktur](category-create.md) für das Hauptmenü zu erstellen, klicken Sie auf **[!UICONTROL Add Subcategory]** und folgen Sie den Anweisungen.

## Schritt 3: Zuweisen der Stammkategorie zum Store

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. Klicken Sie in _Spalte_ Stores“ des Rasters auf den Store, dem Sie den neuen Katalog zuweisen möchten.

1. Legen Sie **[!UICONTROL Root Category]** auf die neue Stammkategorie fest, die Sie erstellt haben.

1. Stellen Sie sicher, dass dem Store ein **[!UICONTROL Default Store View]** zugewiesen ist.

   Der Store muss mindestens über eine [Store-Ansicht](../stores-purchase/store-views.md) verfügen.

1. Klicken Sie abschließend auf **[!UICONTROL Save Store]**.

1. Um sicherzustellen, dass der Store über einen neuen Katalog verfügt, gehen Sie wie folgt vor:

   - Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

     Alle Produkte, die in den neuen Katalog kopiert wurden, werden im Raster angezeigt.

   - Um sicherzustellen, dass der neue Katalog und das Hauptmenü ordnungsgemäß funktionieren, besuchen Sie die Storefront.
