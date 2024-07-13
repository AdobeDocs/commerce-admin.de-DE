---
title: Neues Produktlisten-Widget
description: Erfahren Sie, wie Sie mit dem neuen Produktlisten-Widget eine Liste der zuletzt hinzugefügten Produkte anzeigen können.
exl-id: bdff3655-cd14-4a19-a51f-4cabeb274d2a
feature: Page Content, Products
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '610'
ht-degree: 0%

---

# Neues Produktlisten-Widget

Die Liste der neuen Produkte ist ein Beispiel für dynamischen Inhalt und besteht aus Live-Daten, die aus Ihrem Produktkatalog abgerufen werden. Standardmäßig enthält die Liste _Neue Produkte_ die ersten acht der zuletzt hinzugefügten Produkte. Es kann jedoch auch so konfiguriert werden, dass nur Produkte innerhalb eines bestimmten Datumsbereichs einbezogen werden.

![Neue Produktliste auf der Storefront-Startseite](./assets/storefront-home-page-new-products.png){width="700" zoomable="yes"}

## Schritt 1: Jedes Produkt als neu festlegen

![Magento Open Source](../assets/open-source.svg) Dieser Schritt gilt nur für die Magento Open Source.

![Adobe Commerce](../assets/adobe-logo.svg): Informationen zu Adobe Commerce-Stores finden Sie unter [Planen eines Updates](content-staging-scheduled-update.md) und fahren Sie dann mit Schritt 2 auf dieser Seite fort.

Die Einstellung _[!UICONTROL Set Product as New]_für den Datumsbereich kann nur in geplanten Aktualisierungen konfiguriert werden.

Wenn Sie ein Produkt als neu festlegen, wird das Produkt zur Liste _Neue Produkte_ hinzugefügt. Sie können die Einstellung jederzeit wieder ändern, wenn Sie sie nicht mehr in die Liste aufnehmen möchten.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Suchen Sie jedes Produkt, das Sie verwenden möchten, und öffnen Sie es im Bearbeitungsmodus.

1. Für **[!UICONTROL Set Product as New]** können Sie die Option umschalten, um das Produkt als neues Produkt festzulegen oder nicht.

   ![Festlegen des Produkts als neu](./assets/product-set-as-new.png){width="400" zoomable="yes"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]**.

1. Wenn Sie aufgefordert werden, den Seiten-Cache neu zu indizieren und zu aktualisieren, klicken Sie auf die Links oben auf der Seite und befolgen Sie die Anweisungen.

## Schritt 2: Widget erstellen

Der Code, der den Inhalt der Liste &quot;Neue Produkte&quot;und seine Platzierung in Ihrem Store bestimmt, wird vom Widget-Tool generiert.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Klicken Sie in der oberen rechten Ecke auf **[!UICONTROL Add Widget]**.

1. Gehen Sie im Abschnitt _[!UICONTROL Settings]_wie folgt vor:

   - Setzen Sie **[!UICONTROL Type]** auf `Catalog New Products List`.

   - Wählen Sie die **[!UICONTROL Design Theme]** aus, die vom Store verwendet wird.

1. Klicken Sie auf **[!UICONTROL Continue]**.

   ![Neue Einstellungen für das Produktlisten-Widget](./assets/widget-settings.png){width="600" zoomable="yes"}

1. Gehen Sie im Abschnitt _[!UICONTROL Storefront Properties]_wie folgt vor:

   - Geben Sie für **[!UICONTROL Widget Title]** einen beschreibenden Titel für das Widget ein. (Dieser Titel ist nur in _Admin_ sichtbar.)

   - Wählen Sie für &quot;**[!UICONTROL Assign to Store Views]**&quot;die Store-Ansichten aus, in denen das Widget sichtbar ist.

     Sie können eine bestimmte Store-Ansicht oder `All Store Views` auswählen. Um mehrere Ansichten auszuwählen, halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie auf jede Option.

   - (Optional) Geben Sie für &quot;**[!UICONTROL Sort Order]**&quot;eine Zahl ein, um die Reihenfolge zu bestimmen, in der dieses Element mit anderen im selben Teil der Seite angezeigt wird. (`0` = first, `1` = second, `3` = third usw.)

   ![Layout-Updates](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

## 3. Schritt: Speicherort auswählen

1. Klicken Sie im Abschnitt _[!UICONTROL Layout Updates]_auf **[!UICONTROL Add Layout Update]**.

1. Setzen Sie **[!UICONTROL Display On]** auf `Specified Page.`

1. Setzen Sie **[!UICONTROL Page]** auf `CMS Home Page`.

1. Setzen Sie **[!UICONTROL Block Reference]** auf `Main Content Area`.

1. Setzen Sie **[!UICONTROL Template]** auf einen der folgenden Werte:

   - `New Product List Template`
   - `New Products Grid Template`

     ![Layout-Updates](./assets/widget-layout-update-new-products-list.png){width="600" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Save and Continue Edit]**.

   Derzeit können Sie die Meldung ignorieren, dass der Cache aktualisiert werden soll.

## Schritt 4: Liste konfigurieren

1. Wählen Sie im linken Bereich **[!UICONTROL Widget Options]** aus.

1. Setzen Sie **[!UICONTROL Display Products]** auf einen der folgenden Werte:

   - `All Products` - Listet Produkte in Folge auf, beginnend mit dem zuletzt hinzugefügten.
   - `New Products` - Listet nur die Produkte auf, die als _neu_ gekennzeichnet sind. Ein Produkt gilt als neu im Datumsbereich, der in _[!UICONTROL Set Product As New From/To]_angegeben ist. Die Liste ist leer, wenn der Datumsbereich abläuft, ohne dass neue Produkte definiert wurden.

1. Um die Navigationssteuerung für Listen mit mehreren Seiten bereitzustellen, setzen Sie **[!UICONTROL Display Page Control]** auf `Yes`.

   Geben Sie für &quot;**[!UICONTROL Number of Products per Page]**&quot;die Anzahl der Produkte ein, die auf jeder Seite angezeigt werden sollen.

1. Stellen Sie die Option **[!UICONTROL Number of Products to Display]** auf die Anzahl neuer Produkte ein, die Sie in die Liste aufnehmen möchten.

   Die Standardeinstellung ist `10`.

1. Wählen Sie für &quot;**[!UICONTROL Cache Lifetime (Seconds)]**&quot;aus, wie oft Sie die Liste der neuen Produkte aktualisieren möchten.

   Standardmäßig ist der Cache auf 86.400 Sekunden (24 Stunden) eingestellt.

   ![Widget-Optionen](./assets/widget-options-new-product-list.png){width="600" zoomable="yes"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]**.

1. Wenn Sie aufgefordert werden, den Cache zu aktualisieren, klicken Sie auf den Link in der Meldung oben auf der Seite und befolgen Sie die Anweisungen.

## Schritt 5: Vorschau Ihrer Arbeit anzeigen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Suchen Sie die Seite im Raster, in der die Liste _Neue Produkte_ angezeigt werden soll, und klicken Sie auf den Link **[!UICONTROL Preview]** in der Spalte _[!UICONTROL Action]_.
