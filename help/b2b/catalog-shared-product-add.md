---
title: Produkte zu einem freigegebenen Katalog hinzufügen
description: Erfahren Sie mehr über das Hinzufügen von Produkten zu einem freigegebenen Katalog, entweder einzeln oder in Gruppen nach Kategorie.
exl-id: c88b46b4-cea8-4f65-b7e4-6681bab64d41
feature: B2B, Companies, Catalog Management
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 0%

---

# Produkte zu einem freigegebenen Katalog hinzufügen

Produkte können entweder einzeln oder in Gruppen mit mehreren Produkten nach Kategorie zu einem freigegebenen Katalog hinzugefügt werden.

Die folgenden Anforderungen müssen erfüllt sein, damit ein komplexes Produkt (z. B. Bundle, Gruppierung oder Konfigurierbar) von der Storefront in einem freigegebenen Katalog angezeigt werden kann:

- Alle [zugehörige Produkte](../catalog/product-configurations.md) und -Optionen müssen demselben freigegebenen Katalog zugewiesen und im primären Katalog aktiviert sein.
- Für [konfigurierbar](../catalog/product-create-configurable.md) und [grouped](../catalog/product-create-grouped.md) -Produkte, sind nur die aktivierten verknüpften Produkte sichtbar.
- Für [Bundle](../catalog/product-create-bundle.md) -Produkt, müssen alle Optionen in den freigegebenen Katalog aufgenommen werden.

  ![Produkte für Katalog auswählen](./assets/shared-catalog-select-products-step-1.png){width="600" zoomable="yes"}

## Methode 1: Hinzufügen eines einzelnen Produkts

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Gehen Sie für das Produkt im Raster, das Sie hinzufügen möchten, zum _[!UICONTROL Action]_Spalte und klicken Sie auf **[!UICONTROL Edit]**.

1. Nach unten scrollen, erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die _[!UICONTROL Product in Shared Catalogs]_und gehen Sie wie folgt vor:

   - Aktivieren Sie das Kontrollkästchen jedes freigegebenen Katalogs, in dem das Produkt angezeigt werden soll. Um alle Kataloge auszuwählen, klicken Sie **[!UICONTROL Select all]**.

     ![Produkt in freigegebenen Katalogen](./assets/shared-catalog-assign-from-product.png){width="600" zoomable="yes"}

     Der Name jedes ausgewählten Katalogs wird im _[!UICONTROL Shared Catalogs]_-Feld.

     ![Freigegebene Kataloge zugewiesen](./assets/shared-catalog-assigned.png){width="600" zoomable="yes"}

   - Klicks **[!UICONTROL Done]** , um die Einstellungen zu speichern.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]**.

## Methode 2: Mehrere Produkte hinzufügen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. Den freigegebenen Katalog im Raster finden Sie im _[!UICONTROL Action]_und wählen Sie **[!UICONTROL Set Pricing and Structure]**.

1. Führen Sie im Kategoriebaum einen der folgenden Schritte aus:

   - Um alle Produkte einzuschließen, klicken Sie auf **[!UICONTROL Select all]** oder aktivieren Sie das Kontrollkästchen der übergeordneten Kategorie.
   - Um bestimmte Produktkategorien einzubeziehen, aktivieren Sie das Kontrollkästchen jeder Kategorie, die Sie einbeziehen möchten.
   - Um ein einzelnes Produkt ein- oder auszuschließen, aktivieren oder deaktivieren Sie das Kontrollkästchen des Produkts.

   Die Notation unter jeder Kategorie im Baum zeigt die Anzahl der Produkte aus der Kategorie an, die derzeit im freigegebenen Katalog enthalten sind. Die -Notation unter der [Stammkategorie](../catalog/category-root.md) zeigt die Gesamtanzahl der Produkte aus allen Kategorien an, die derzeit für den freigegebenen Katalog ausgewählt sind.

1. Um Kategorieprodukte im Raster anzuzeigen, klicken Sie auf den Namen der Kategorie im Baum.

   Wenn eine Kategorie ausgewählt wird, geschieht Folgendes:

   - Der Umschalter in der ersten Spalte des Rasters ist auf `On` für jedes ausgewählte Produkt.
   - Wenn ein Produkt mehreren Kategorien zugewiesen ist und in einer dieser Kategorien weggelassen wird, bleibt es über die anderen Kategorien und über [Katalogsuche](../catalog/search.md).
   - Das System setzt automatisch [Kategorieberechtigungen](../catalog/category-permissions.md) nach `Allow` für die ausgewählten Produkte.
