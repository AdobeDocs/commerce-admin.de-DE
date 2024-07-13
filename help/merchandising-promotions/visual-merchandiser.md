---
title: Übersicht über Visual Merchandiser
description: Erfahren Sie mehr über die Visual Merchandiser-Tools, mit denen Sie Produkte positionieren und bestimmen können, welche Produkte in der Kategorienliste angezeigt werden.
exl-id: 00fe8b7f-0c33-4f06-a3cd-1f0bd18079f1
feature: Categories, Merchandising, Products
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 0%

---

# Visual Merchandiser

{{ee-feature}}

Der _Visual Merchandiser_ ist ein Satz erweiterter Tools, mit denen Sie Produkte positionieren und Bedingungen anwenden können, die bestimmen, welche Produkte in der Kategorienliste angezeigt werden. Das Ergebnis kann eine dynamische Auswahl von Produkten sein, die sich an Änderungen im Katalog anpasst. Sie können im _visuellen Modus_ arbeiten, in dem jedes Produkt als Kachel auf einem Raster angezeigt wird, oder aus einer Liste von Produkten in der Kategorie arbeiten. In jedem Modus sind dieselben Tools verfügbar. Sie können die Schaltflächen in der oberen rechten Ecke verwenden, um zwischen den einzelnen Anzeigetypen umzuschalten.

![Kategorieprodukte in der Kachelansicht](./assets/category-products-visual-with-stock.png){width="600" zoomable="yes"}

## Zugriff auf Visual Merchandiser

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Führen Sie einen Drilldown in der Kategoriestruktur durch und klicken Sie auf die Kategorie, die Sie bearbeiten möchten.

1. Scrollen Sie nach unten und erweitern Sie den Abschnitt **[!UICONTROL Products in Category]** um den ![Erweiterungsselektor](../assets/icon-display-expand.png).

1. Klicken Sie auf die Schaltfläche _Als Kacheln anzeigen_ ( ![Als Kacheln anzeigen](../assets/icon-view-tiles.png) ), um die Produkte als Raster anzuzeigen.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Category]**.

## Position eines Produkts ändern

1. Verwenden Sie die [Sortierreihenfolge](../catalog/navigation-product-listings.md) , um das Produkt anzuzeigen, das Sie verschieben möchten.

   - **Methode 1: Ziehen und Ablegen**

     Ziehen Sie das Steuerelement _Ziehen_ (![Ziehen-Symbol](../assets/icon-move.png)) in der oberen rechten Ecke der Produktkachel und legen Sie das Produkt an einer Position ab. Die Anzahl der einzelnen Produkte passt sich der neuen Position an.

   - **Methode 2: Positionswert festlegen**

     Geben Sie im Controller _Position_ (![Positionsfeld](../assets/control-position.png)) auf der Produktkachel die Nummer ein, unter der das Produkt angezeigt werden soll. Geben Sie `0` ein, um das Produkt oben in der Liste zu platzieren.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Category]**.

>[!NOTE]
>
>Bei einer ordnungsgemäßen Installation reserviert Adobe Commerce die Kategorie-ID `2` für den Stammkatalog des Standardspeichers. Visual Merchandiser kann nur Kategorien mit der ID-Nummer `3` oder höher verwenden.

## Workspace-Steuerelemente

| Kontrolle | Beschreibung |
|--- |--- |
| ![Symbol &quot;Liste anzeigen&quot;](../assets/icon-view-list.png) | Als Liste anzeigen |
| ![Als Kachelsymbol anzeigen](../assets/icon-view-tiles.png) | Als Kacheln anzeigen |
| ![Übereinstimmung mit Regelumschalter - nein](../assets/toggle-no.png) | Übereinstimmung mit Regel - nein |
| ![Übereinstimmung mit Regelumschalter - ja](../assets/toggle-yes.png) | Übereinstimmung mit Regel - ja |
| ![Symbol &quot;Verschieben&quot;](../assets/icon-move.png) | Ziehen |
| ![Positionscontroller](../assets/control-position.png) | Position |
| ![Symbol &quot;Aus Kategorie entfernen&quot;](../assets/icon-delete-x.png) | Aus Kategorie entfernen |
| ![Elemente pro Seitensteuerelement](../assets/control-items-per-page.png) | Anzeigen pro Seite |
| ![Ändern der Seitenanzeige](../assets/control-page-display.png) | Weiter zum nächsten/vorherigen |

{style="table-layout:auto"}
