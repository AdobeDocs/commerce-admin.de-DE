---
title: Übersicht über Visual Merchandiser
description: Erfahren Sie mehr über die Visual Merchandiser-Tools, mit denen Sie Produkte positionieren und bestimmen können, welche Produkte in der Kategorienliste angezeigt werden.
exl-id: 00fe8b7f-0c33-4f06-a3cd-1f0bd18079f1
feature: Categories, Merchandising, Products
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---

# Visual Merchandiser

{{ee-feature}}

Die _Visual Merchandiser_ ist ein Satz erweiterter Tools, mit denen Sie Produkte positionieren und Bedingungen anwenden können, die bestimmen, welche Produkte in der Kategorienliste angezeigt werden. Das Ergebnis kann eine dynamische Auswahl von Produkten sein, die sich an Änderungen im Katalog anpasst. Sie können in _visueller Modus_, das jedes Produkt als Kachel auf einem Raster anzeigt oder aus einer Liste von Produkten in der Kategorie verwendet werden kann. In jedem Modus sind dieselben Tools verfügbar. Sie können die Schaltflächen in der oberen rechten Ecke verwenden, um zwischen den einzelnen Anzeigetypen umzuschalten.

![Kategorieprodukte in der Kachelansicht](./assets/category-products-visual-with-stock.png){width="600" zoomable="yes"}

## Zugriff auf Visual Merchandiser

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Führen Sie einen Drilldown in der Kategoriestruktur durch und klicken Sie auf die Kategorie, die Sie bearbeiten möchten.

1. Hinunter scrollen und erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Products in Category]** Abschnitt.

1. Klicken Sie auf _Als Kacheln anzeigen_ ( ![Als Kacheln anzeigen](../assets/icon-view-tiles.png) ), um die Produkte als Raster anzuzeigen.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Category]**.

## Position eines Produkts ändern

1. Verwenden Sie die [Sortierreihenfolge](../catalog/navigation-product-listings.md) , um das Produkt anzuzeigen, das Sie verschieben möchten.

   - **Methode 1: Ziehen und Ablegen**

     Grab die _Ziehen_ (![Symbol ziehen](../assets/icon-move.png)) in der oberen rechten Ecke der Kachel &quot;Produkt&quot;ein und legen das Produkt an der Position ab. Die Anzahl der einzelnen Produkte passt sich der neuen Position an.

   - **Methode 2: Positionswert festlegen**

     Im _Position_ Controller![Positionsfeld](../assets/control-position.png)), geben Sie die Nummer ein, unter der das Produkt angezeigt werden soll. Eingabe `0` , um das Produkt oben in der Liste zu platzieren.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Category]**.

>[!NOTE]
>
>Bei einer Neuinstallation behält Adobe Commerce die Kategorie-ID bei `2` für den Stammkatalog des Standardspeichers. Visual Merchandiser kann nur Kategorien mit einer ID-Nummer verwenden `3` oder höher.

## Workspace-Steuerelemente

| Kontrolle | Beschreibung |
|--- |--- |
| ![Symbol &quot;Liste anzeigen&quot;](../assets/icon-view-list.png) | Als Liste anzeigen |
| ![Symbol &quot;Als Kacheln anzeigen&quot;](../assets/icon-view-tiles.png) | Als Kacheln anzeigen |
| ![Übereinstimmung durch Umschalter zwischen Regeln - nein](../assets/toggle-no.png) | Übereinstimmung mit Regel - nein |
| ![Übereinstimmung mit Regelumschalter - ja](../assets/toggle-yes.png) | Übereinstimmung mit Regel - ja |
| ![Symbol Verschieben](../assets/icon-move.png) | Ziehen |
| ![Positionsverantwortlicher](../assets/control-position.png) | Position |
| ![Aus Kategorie-Symbol entfernen](../assets/icon-delete-x.png) | Aus Kategorie entfernen |
| ![Elemente pro Seitensteuerung](../assets/control-items-per-page.png) | Anzeigen pro Seite |
| ![Seitenanzeige ändern](../assets/control-page-display.png) | Weiter zum nächsten/vorherigen |

{style="table-layout:auto"}
