---
title: Widget „Liste neuer Produkte“
description: Erfahren Sie, wie Sie mit dem Widget Liste neuer Produkte eine Liste der zuletzt hinzugefügten Produkte anzeigen können.
exl-id: bdff3655-cd14-4a19-a51f-4cabeb274d2a
feature: Page Content, Products
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 0%

---

# Widget „Liste neuer Produkte“

Die Liste der neuen Produkte ist ein Beispiel für dynamische Inhalte und besteht aus Live-Daten, die aus Ihrem Produktkatalog abgerufen werden. Standardmäßig enthält die Liste _Neue Produkte_ die ersten acht der zuletzt hinzugefügten Produkte. Sie kann jedoch auch so konfiguriert werden, dass nur Produkte innerhalb eines bestimmten Datumsbereichs einbezogen werden.

![Liste neuer Produkte auf der Startseite der Storefront](./assets/storefront-home-page-new-products.png){width="700" zoomable="yes"}

## Schritt 1: Jedes Produkt als neu einstellen

![Magento Open Source](../assets/open-source.svg) Dieser Schritt gilt nur für Magento Open Source.

![Adobe Commerce](../assets/adobe-logo.svg) Informationen zu Adobe Commerce-Stores finden Sie unter [Planen einer Aktualisierung](content-staging-scheduled-update.md) und fahren Sie dann mit Schritt 2 auf dieser Seite fort.

_[!UICONTROL Set Product as New]_Einstellung für den Datumsbereich kann nur in geplanten Aktualisierungen konfiguriert werden.

Wenn Sie ein Produkt als neu festlegen, wird das Produkt zur Liste _Neue Produkte_ hinzugefügt. Sie können die Einstellung jederzeit wieder zurücksetzen, wenn Sie sie nicht mehr in die Liste aufnehmen möchten.

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Suchen Sie jedes Produkt, das Sie verwenden möchten, und öffnen Sie es im Bearbeitungsmodus.

1. Schalten Sie **[!UICONTROL Set Product as New]** die Option ein, um das Produkt als neues Produkt festzulegen oder nicht.

   ![Das Produkt als neu einstellen](./assets/product-set-as-new.png){width="400" zoomable="yes"}

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.

1. Wenn Sie aufgefordert werden, den Seiten-Cache neu zu indizieren und zu aktualisieren, klicken Sie auf die Links oben auf der Seite und folgen Sie den Anweisungen.

## Schritt 2: Widget erstellen

Der Code, der den Inhalt der Liste Neue Produkte und deren Platzierung in Ihrem Store bestimmt, wird vom Widget-Tool generiert.

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Klicken Sie oben rechts auf **[!UICONTROL Add Widget]**.

1. Gehen Sie im Abschnitt _[!UICONTROL Settings]_wie folgt vor:

   - Legen Sie **[!UICONTROL Type]** auf `Catalog New Products List` fest.

   - Wählen Sie die **[!UICONTROL Design Theme]** aus, die vom Store verwendet wird.

1. Klicken Sie auf **[!UICONTROL Continue]**.

   ![Einstellungen für neue Produktlisten-Widgets](./assets/widget-settings.png){width="600" zoomable="yes"}

1. Gehen Sie im Abschnitt _[!UICONTROL Storefront Properties]_wie folgt vor:

   - Geben Sie **[!UICONTROL Widget Title]** einen beschreibenden Titel für das Widget ein. (Dieser Titel ist nur in der Datei _Admin_ sichtbar.)

   - Wählen Sie **[!UICONTROL Assign to Store Views]** die Store-Ansichten aus, in denen das Widget sichtbar ist.

     Sie können eine bestimmte Shop-Ansicht oder `All Store Views` auswählen. Halten Sie zum Auswählen mehrerer Ansichten die Strg-Taste (PC) bzw. die Befehlstaste (Mac) gedrückt und klicken Sie auf die einzelnen Optionen.

   - (Optional) Geben Sie **[!UICONTROL Sort Order]** eine Zahl ein, um die Reihenfolge zu bestimmen, in der dieses Element zusammen mit anderen im selben Teil der Seite angezeigt wird. (`0` = First, `1` = Second, `3` = Third usw.)

   ![Layout-Aktualisierungen](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

## Schritt 3: Speicherort auswählen

1. Klicken Sie im Abschnitt _[!UICONTROL Layout Updates]_auf **[!UICONTROL Add Layout Update]**.

1. **[!UICONTROL Display On]** auf `Specified Page.` festlegen

1. Legen Sie **[!UICONTROL Page]** auf `CMS Home Page` fest.

1. Legen Sie **[!UICONTROL Block Reference]** auf `Main Content Area` fest.

1. Legen Sie **[!UICONTROL Template]** auf eine der folgenden Einstellungen fest:

   - `New Product List Template`
   - `New Products Grid Template`

     ![Layout-Aktualisierungen](./assets/widget-layout-update-new-products-list.png){width="600" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Save and Continue Edit]**.

   Vorerst können Sie die Meldung ignorieren, um den Cache zu aktualisieren.

## Schritt 4: Konfigurieren der Liste

1. Wählen Sie im linken Bedienfeld **[!UICONTROL Widget Options]** aus.

1. Legen Sie **[!UICONTROL Display Products]** auf eine der folgenden Einstellungen fest:

   - `All Products` - Listet Produkte der Reihe nach auf, beginnend mit dem zuletzt hinzugefügten.
   - `New Products` - Listet nur die Produkte auf, die als „neu _gekennzeichnet_. Ein Produkt gilt während des in _[!UICONTROL Set Product As New From/To]_angegebenen Datumsbereichs als neu. Die Liste ist leer, wenn der Datumsbereich abläuft, ohne dass neue Produkte definiert wurden.

1. Um Navigationssteuerelemente für Listen mit mehreren Seiten bereitzustellen, legen Sie **[!UICONTROL Display Page Control]** auf `Yes` fest.

   Geben Sie **[!UICONTROL Number of Products per Page]** die Anzahl der Produkte ein, die auf jeder Seite angezeigt werden sollen.

1. Legen Sie die Option **[!UICONTROL Number of Products to Display]** auf die Anzahl der neuen Produkte fest, die Sie in die Liste aufnehmen möchten.

   Die Standardeinstellung ist `10`.

1. Wählen Sie **[!UICONTROL Cache Lifetime (Seconds)]** aus, wie oft Sie die Liste der neuen Produkte aktualisieren möchten.

   Standardmäßig ist der Cache auf 86.400 Sekunden (24 Stunden) festgelegt.

   ![Widget-Optionen](./assets/widget-options-new-product-list.png){width="600" zoomable="yes"}

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.

1. Wenn Sie aufgefordert werden, den Cache zu aktualisieren, klicken Sie auf den Link in der Nachricht oben auf der Seite und folgen Sie den Anweisungen.

## Schritt 5: Vorschau der Arbeit

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Suchen Sie die Seite im Raster, auf der die Liste _Neue Produkte_ angezeigt werden soll, und klicken Sie auf den **[!UICONTROL Preview]** Link in der Spalte _[!UICONTROL Action]_.
