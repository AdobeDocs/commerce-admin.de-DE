---
title: Dynamischen Block hinzufügen
description: Präsentieren Sie eine Bildschirmpräsentation mit interaktiven Inhalten auf der Storefront, indem Sie einem Rotator mehrere dynamische Blöcke hinzufügen.
exl-id: 3d338014-cf26-4171-b48b-d37b3d7b0e81
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/de/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '641'
ht-degree: 0%

---

# Dynamischen Block hinzufügen

{{ee-feature}}

Um eine Bildschirmpräsentation mit interaktiven Inhalten zu präsentieren, können Sie mehrere [dynamische Blöcke](dynamic-blocks.md) zu einem Rotator hinzufügen. Das [Widget](widgets.md)-Tool wird verwendet, um den Rotator an einer bestimmten Stelle entweder auf einer einzelnen Seite oder auf mehreren Seiten in Ihrem Geschäft zu platzieren.

![Dynamischer Blockrotator](./assets/widget-dynamic-block-rotator.png){width="700" zoomable="yes"}

## Schritt 1: Erstellen Sie einzelne dynamische Blöcke

Um [&#x200B; dynamischen Blöcke zu erstellen](dynamic-blocks.md) die Sie in den Rotator einfügen möchten, befolgen Sie die folgenden Anweisungen:

## Schritt 2: Dynamisches Block-Rotator-Widget hinzufügen

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Klicken Sie oben rechts auf **[!UICONTROL Add Widget]**.

1. Legen _unter &quot;_&quot; **[!UICONTROL Type]** auf `Dynamic Blocks Rotator` fest.

1. Wählen Sie die aktuelle **[!UICONTROL Design Theme]** des Stores aus.

   Diese Einstellung identifiziert das aktuelle Paket oder [Design](themes.md) das das Seiten-Layout des Stores bestimmt.

1. Klicken Sie auf **[!UICONTROL Continue]**.

   ![Dynamische Blockrotator-Einstellungen](./assets/widget-dynamic-block-rotator-settings.png){width="600" zoomable="yes"}

## Schritt 3: Vervollständigen Sie die Optionen

1. Legen _unter „Storefront-_&quot; die folgenden Optionen fest:

   - Geben Sie einen **[!UICONTROL Title]** für den Rotator ein.

   - Wählen Sie in der Liste **[!UICONTROL Assign to Store Views]** die Option [Store-](../getting-started/websites-stores-views.md)) aus, in der der Rotator verfügbar ist.

   - (Optional) Geben Sie eine **[!UICONTROL Sort Order]** ein, um die Position des Rotators im Zielcontainer zu bestimmen. Sie ist relativ zu anderen Widgets, die demselben Container zugewiesen sein können.

   ![Rotator-Storefront-Eigenschaften](./assets/widget-dynamic-block-rotator-storefront-properties.png){width="600" zoomable="yes"}

1. Klicken _unter_ Layout-Optionen“ auf **[!UICONTROL Add Layout Update]** und führen Sie folgende Schritte aus:

   - Legen Sie **[!UICONTROL Display on]** auf die Seite bzw. den Seitentyp fest, auf der der Rotator angezeigt werden soll.

      - `Categories` - Zeigt den Rotator auf Kategorieseiten [Anker](../catalog/navigation-layered.md) oder Nicht-Anker an. Optionen: Ankerkategorien/Kategorien ohne Anker
      - `Products` - Zeigt den Rotator entweder auf einer bestimmten Produktseite oder auf allen Produktseiten an. Optionen: Alle Produktarten / [Einfaches Produkt](../catalog/product-create-simple.md) / [Virtuelles Produkt](../catalog/product-create-virtual.md) / [Bundle-Produkt](../catalog/product-create-bundle.md) / [Herunterladbares Produkt](../catalog/product-create-downloadable.md) / [Geschenkkarte](../catalog/product-gift-card-create.md) / [Konfigurierbares Produkt](../catalog/product-create-configurable.md) / [gruppiertes Produkt](../catalog/product-create-grouped.md)
      - `Generic Pages` - Zeigt den Rotator auf allen Seiten, auf einer bestimmten Seite oder nur auf Seiten mit einem bestimmten Layout an. Optionen: `All Pages` / `Specified Page` / `Page Layouts`

     Im Beispiel soll der Rotator auf einem `Specified Page` platziert werden.

   - Wählen Sie die spezifische **[!UICONTROL Page]** aus, in der der Rotator angezeigt werden soll.

   - Legen Sie **[!UICONTROL Container]** auf den Teil des [Seiten-Layouts](page-layout.md#standard-page-layouts) fest, in dem der Rotator angezeigt werden soll.

     Wenn andere Widgets demselben Container zugewiesen sind, werden sie entsprechend der Sortierreihenfolge nacheinander angezeigt.

   - Akzeptieren Sie `Dynamic Block Template` als **[!UICONTROL Template]**.

     Diese Einstellung bestimmt die Vorlage, die zum Formatieren des Rotators verwendet wird, je nachdem, ob der Rotator eigenständig sein oder in vorhandenen Text platziert werden soll.

     ![Aktualisierungen des Rotator-Layouts](./assets/widget-dynamic-block-rotator-layout-updates.png){width="600" zoomable="yes"}

   - Klicken Sie auf **[!UICONTROL Save and Continue Edit]**.

1. Wählen Sie im linken Bedienfeld **[!UICONTROL Widget Options]** aus.

1. Für die **[!UICONTROL Dynamic Blocks to Display]** akzeptieren Sie `Specified Dynamic Blocks`.

   Diese Einstellung bestimmt den Typ der dynamischen Blöcke, die im Rotator enthalten sind.

   - `Specified Dynamic Blocks` - Enthält nur bestimmte dynamische Blöcke.
   - `Cart Price Rule Related` - Enthält nur dynamische Blöcke, die mit einer Warenkorb-Preisregel verknüpft sind.
   - `Catalog Price Rule Related` - Enthält nur dynamische Blöcke, die mit einer Katalogpreisregel verknüpft sind.

1. Um **[!UICONTROL Restrict the Dynamic Block Types]**, die mit dem Widget verwendet werden können, wählen Sie `Content Area` aus.

   Diese Einstellung beschränkt das Banner auf einen bestimmten Teil des Seiten-Layouts.

   - `Content Area` - Platziert den dynamischen Block im Hauptinhaltsbereich der Seite.
   - `Footer` - Platziert den dynamischen Block in der Fußzeile der Seite.
   - `Header` - Platziert den dynamischen Block im Seitenkopf.
   - `Left Column` - Platziert den dynamischen Block in der linken Spalte des Seiten-Layouts, sofern verfügbar.
   - `Right Column` - Platziert den dynamischen Block in der rechten Spalte des Seiten-Layouts, sofern verfügbar.

1. Legen Sie **[!UICONTROL Rotation Mode]** auf eine der folgenden Einstellungen fest:

   - `Display all instead of rotating` : Zeigt einen Stapel dynamischer Blöcke an, auf denen alle sichtbar sind.
   - `One at a time, Random` - Zeigt die angegebenen dynamischen Blöcke in zufälliger Reihenfolge an. Wenn die Seite aktualisiert wird, wird ein anderer (und zufälliger) dynamischer Block angezeigt.
   - `One at the time, Series` - Zeigt die angegebenen dynamischen Blöcke in der Reihenfolge an, in der sie hinzugefügt wurden. Nach dem Aktualisieren der Seite wird der nächste dynamische Block in der Sequenz angezeigt.
   - `One at the time, Shuffle` : Zeigt einen dynamischen Block nach dem anderen in einer gemischten Reihenfolge an. Diese Option ähnelt der Option `One at a time, Random`, mit dem Unterschied, dass derselbe dynamische Block nicht wiederholt wird.

     ![Optionen für Rotator-Widgets](./assets/widget-dynamic-block-rotator-widget-options.png){width="600" zoomable="yes"}

1. Aktivieren Sie im **[!UICONTROL Specify Dynamic Blocks]** das Kontrollkästchen jedes dynamischen Blocks, den Sie in den Rotator aufnehmen möchten.

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.
