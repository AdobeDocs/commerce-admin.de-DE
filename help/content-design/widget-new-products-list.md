---
title: Neues Produktlisten-Widget
description: Erfahren Sie, wie Sie mit dem neuen Produktlisten-Widget eine Liste der zuletzt hinzugefügten Produkte anzeigen können.
exl-id: bdff3655-cd14-4a19-a51f-4cabeb274d2a
feature: Page Content, Products
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 0%

---

# Neues Produktlisten-Widget

Die Liste der neuen Produkte ist ein Beispiel für dynamischen Inhalt und besteht aus Live-Daten, die aus Ihrem Produktkatalog abgerufen werden. Standardmäßig wird die Variable _Neue Produkte_ enthält die ersten acht der zuletzt hinzugefügten Produkte. Es kann jedoch auch so konfiguriert werden, dass nur Produkte innerhalb eines bestimmten Datumsbereichs einbezogen werden.

![Neue Produktliste auf der Storefront-Homepage](./assets/storefront-home-page-new-products.png){width="700" zoomable="yes"}

## Schritt 1: Jedes Produkt als neu festlegen

![Magento Open Source](../assets/open-source.svg) Dieser Schritt gilt nur für die Magento Open Source.

![Adobe Commerce](../assets/adobe-logo.svg) Informationen zu Adobe Commerce-Stores finden Sie unter [Planung einer Aktualisierung](content-staging-scheduled-update.md) und dann auf dieser Seite mit Schritt 2 fortfahren.

_[!UICONTROL Set Product as New]_Die Einstellung für den Datumsbereich kann nur in geplanten Aktualisierungen konfiguriert werden.

Durch das Festlegen eines Produkts als neu wird das Produkt zum _Neue Produkte_ Liste. Sie können die Einstellung jederzeit wieder ändern, wenn Sie sie nicht mehr in die Liste aufnehmen möchten.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Suchen Sie jedes Produkt, das Sie verwenden möchten, und öffnen Sie es im Bearbeitungsmodus.

1. Für **[!UICONTROL Set Product as New]** aktivieren, aktivieren Sie die Option, um das Produkt als neues Produkt festzulegen.

   ![Festlegen des Produkts als neu](./assets/product-set-as-new.png){width="400" zoomable="yes"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]**.

1. Wenn Sie aufgefordert werden, den Seiten-Cache neu zu indizieren und zu aktualisieren, klicken Sie auf die Links oben auf der Seite und befolgen Sie die Anweisungen.

## Schritt 2: Widget erstellen

Der Code, der den Inhalt der Liste &quot;Neue Produkte&quot;und seine Platzierung in Ihrem Store bestimmt, wird vom Widget-Tool generiert.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Klicken Sie oben rechts auf **[!UICONTROL Add Widget]**.

1. Im _[!UICONTROL Settings]_führen Sie folgende Schritte aus:

   - Satz **[!UICONTROL Type]** nach `Catalog New Products List`.

   - Wählen Sie die **[!UICONTROL Design Theme]** wird vom Store verwendet.

1. Klicken **[!UICONTROL Continue]**.

   ![Neue Widget-Einstellungen für die Produktliste](./assets/widget-settings.png){width="600" zoomable="yes"}

1. Im _[!UICONTROL Storefront Properties]_führen Sie folgende Schritte aus:

   - Für **[!UICONTROL Widget Title]**, geben Sie einen beschreibenden Titel für das Widget ein. (Dieser Titel ist nur über die _Admin_.

   - Für **[!UICONTROL Assign to Store Views]**, wählen Sie die Store-Ansichten aus, in denen das Widget sichtbar ist.

     Sie können eine bestimmte Store-Ansicht auswählen oder `All Store Views`. Um mehrere Ansichten auszuwählen, halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie auf jede Option.

   - (Optional) Für **[!UICONTROL Sort Order]** Geben Sie eine Zahl ein, um die Reihenfolge zu bestimmen, in der dieses Element mit anderen Elementen im selben Teil der Seite angezeigt wird. (`0` = first, `1` = Sekunde, `3` = drittes Element usw.)

   ![Layout-Aktualisierungen](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

## 3. Schritt: Speicherort auswählen

1. Im _[!UICONTROL Layout Updates]_Abschnitt, klicken Sie auf **[!UICONTROL Add Layout Update]**.

1. Satz **[!UICONTROL Display On]** nach `Specified Page.`

1. Satz **[!UICONTROL Page]** nach `CMS Home Page`.

1. Satz **[!UICONTROL Block Reference]** nach `Main Content Area`.

1. Satz **[!UICONTROL Template]** auf einen der folgenden Werte zu:

   - `New Product List Template`
   - `New Products Grid Template`

     ![Layout-Aktualisierungen](./assets/widget-layout-update-new-products-list.png){width="600" zoomable="yes"}

1. Klicken **[!UICONTROL Save and Continue Edit]**.

   Derzeit können Sie die Meldung ignorieren, dass der Cache aktualisiert werden soll.

## Schritt 4: Liste konfigurieren

1. Wählen Sie im linken Bereich die Option **[!UICONTROL Widget Options]**.

1. Satz **[!UICONTROL Display Products]** auf einen der folgenden Werte zu:

   - `All Products` - Führt Produkte nacheinander auf, beginnend mit dem zuletzt hinzugefügten.
   - `New Products` - Listet nur die Produkte auf, die als _new_. Ein Produkt gilt als neu in dem Datumsbereich, der unter _[!UICONTROL Set Product As New From/To]_. Die Liste ist leer, wenn der Datumsbereich abläuft, ohne dass neue Produkte definiert wurden.

1. Um die Navigationssteuerung für Listen mit mehreren Seiten bereitzustellen, legen Sie **[!UICONTROL Display Page Control]** nach `Yes`.

   Für **[!UICONTROL Number of Products per Page]** Geben Sie die Anzahl der Produkte ein, die auf jeder Seite angezeigt werden sollen.

1. Legen Sie die **[!UICONTROL Number of Products to Display]** -Option auf die Anzahl der neuen Produkte, die Sie in die Liste aufnehmen möchten.

   Die Standardeinstellung ist `10`.

1. Für **[!UICONTROL Cache Lifetime (Seconds)]** auswählen, wie oft Sie die Liste der neuen Produkte aktualisieren möchten.

   Standardmäßig ist der Cache auf 86.400 Sekunden (24 Stunden) eingestellt.

   ![Widget-Optionen](./assets/widget-options-new-product-list.png){width="600" zoomable="yes"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]**.

1. Wenn Sie aufgefordert werden, den Cache zu aktualisieren, klicken Sie auf den Link in der Meldung oben auf der Seite und befolgen Sie die Anweisungen.

## Schritt 5: Vorschau Ihrer Arbeit anzeigen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Suchen Sie die Seite im Raster, wo die _Neue Produkte_ Die Liste wird angezeigt und klicken Sie auf **[!UICONTROL Preview]** -Link in _[!UICONTROL Action]_Spalte.
