---
title: Übersicht über Visual Merchandiser
description: Erfahren Sie mehr über die Visual Merchandiser-Tools, mit denen Sie Produkte positionieren und bestimmen können, welche Produkte in der Kategorieliste angezeigt werden.
exl-id: 00fe8b7f-0c33-4f06-a3cd-1f0bd18079f1
feature: Categories, Merchandising, Products
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
source-git-commit: 6d782e3aafa7460a0e0d5ca07a2bde2ae371a9ea
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 0%

---

# Visual Merchandiser

{{ee-feature}}

Der _Visual Merchandiser_ ist ein Satz erweiterter Tools, mit denen Sie Produkte positionieren und Bedingungen anwenden können, die bestimmen, welche Produkte in der Kategorieliste angezeigt werden. Das Ergebnis kann eine dynamische Auswahl von Produkten sein, die sich an Änderungen im Katalog anpasst. Sie können im _visuellen Modus_ arbeiten, der jedes Produkt als Kachel auf einem Raster anzeigt, oder aus einer Liste von Produkten in der Kategorie arbeiten. In jedem Modus stehen die gleichen Tools zur Verfügung, und Sie können mit den Schaltflächen in der oberen rechten Ecke zwischen den verschiedenen Anzeigetypen wechseln.

![Kategorieprodukte in der Kachelansicht](./assets/category-products-visual-with-stock.png){width="600" zoomable="yes"}

## Zugriff auf Visual Merchandiser

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Drilldown in der Kategoriestruktur durchführen und auf die Kategorie klicken, die Sie bearbeiten möchten.

1. Scrollen Sie nach unten und erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Products in Category]** .

1. Klicken Sie auf _Als Kacheln anzeigen_ ( ![Als Kacheln anzeigen](../assets/icon-view-tiles.png) ), um die Produkte als Raster anzuzeigen.

1. Klicken Sie abschließend auf **[!UICONTROL Save Category]**.

## Position eines Produkts ändern

1. Verwenden Sie die [Sortierreihenfolge](../catalog/navigation-product-listings.md), um das Produkt anzuzeigen, das Sie verschieben möchten.

   - **Methode 1: Drag-and-Drop**

     Greifen Sie das Steuerelement _Ziehen_ (![Symbol ziehen](../assets/icon-move.png)) in der oberen rechten Ecke der Produktkachel und legen Sie das Produkt in der Position ab. Die Anzahl der einzelnen Produkte wird entsprechend der neuen Position angepasst.

   - **Methode 2: Positionswert festlegen**

     Geben _im_-Controller (![Feld Position](../assets/control-position.png)) auf der Produktkachel die Nummer ein, unter der das Produkt angezeigt werden soll. Geben Sie `0` ein, um das Produkt an den Anfang der Liste zu setzen.

1. Klicken Sie abschließend auf **[!UICONTROL Save Category]**.

>[!NOTE]
>
>Bei einer Neuinstallation reserviert Adobe Commerce die Kategorie-ID `2` für den Stammkatalog des Standardspeichers. Visual Merchandiser kann nur Kategorien mit einer ID-Nummer von `3` oder höher verwenden.

## Workspace-Steuerelemente

| Kontrolle | Beschreibung |
|--- |--- |
| ![Symbol „Liste anzeigen“](../assets/icon-view-list.png) | Als Liste anzeigen |
| ![Als Kacheln anzeigen](../assets/icon-view-tiles.png) | Als Kacheln anzeigen |
| ![Umschalter für Übereinstimmung nach Regel - Nein](../assets/toggle-no.png) | Übereinstimmung nach Regel - Nein |
| ![Umschalter für Übereinstimmung nach Regel - Ja](../assets/toggle-yes.png) | Übereinstimmung nach Regel - ja |
| ![move icon](../assets/icon-move.png) | Schleppen |
| ![Positionsregler](../assets/control-position.png) | Position |
| ![Aus Kategoriesymbol entfernen](../assets/icon-delete-x.png) | Aus Kategorie entfernen |
| ![Elemente pro Seitensteuerelement](../assets/control-items-per-page.png) | Pro Seite anzeigen |
| ![Ändern der Seitenanzeige](../assets/control-page-display.png) | Weiter/Zurück |

{style="table-layout:auto"}
