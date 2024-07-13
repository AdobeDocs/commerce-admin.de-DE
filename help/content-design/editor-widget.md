---
title: Widget in den Editor einfügen
description: Fügen Sie mithilfe des Widget-Tools im WYSIWYG-Editor verschiedene Inhaltselemente zu einer Seite hinzu.
exl-id: bbc5e059-06d8-4dda-89a7-6c9826b73fd3
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---

# Widget in den Editor einfügen

Mit dem Tool [widget](widget-create.md) können Sie verschiedene Inhaltselemente zur Seite hinzufügen, einschließlich Links zu beliebigen Commerce-Inhaltsseiten, -Knoten, -Produkten oder -Kategorien. Links können auf der Seite in einem Blockformat positioniert oder direkt in den Inhalt integriert werden. Sie können das Widget-Tool verwenden, um Links zu den folgenden Inhaltstypen zu erstellen:

- [Inhaltsseiten](pages.md)
- [Katalogkategorien](../catalog/categories.md)
- [Katalogprodukte](../catalog/product-create.md)

Standardmäßig übernehmen Links ihren Stil vom Stylesheet des Designs.

{{$include /help/_includes/directives-caution.md}}

1. Öffnen Sie eine Seite, einen Block oder einen dynamischen Block im Bearbeitungsmodus.

1. Gehen Sie zum Abschnitt _[!UICONTROL Content]_und klicken Sie auf ein Element, das den Editor unterstützt.

1. Positionieren Sie den Cursor an der Stelle, an der das Widget angezeigt werden soll, und klicken Sie auf das Symbol _Widget einfügen_ .

   ![Editor-Symbolleiste - Widget einfügen](./assets/editor-toolbar-widget-button.png){width="700" zoomable="yes"}

   Wenn Sie Page Builder nicht aktiviert haben und es vorziehen, mit dem Code zu arbeiten, klicken Sie auf **[!UICONTROL Show / Hide Editor]**. Positionieren Sie den Einfügepunkt im Text, an dem das Widget angezeigt werden soll. Klicken Sie dann auf **[!UICONTROL Insert Widget]**.

1. Wählen Sie die **[!UICONTROL Widget Type]** aus.

   Weitere Informationen zu diesen Optionen finden Sie unter [Widget-Typen](widgets.md#widget-types). Die folgenden Schritte zeigen ein Beispiel für das Einfügen eines Links zu einem Produkt.

1. Lassen Sie das Feld **[!UICONTROL Anchor Custom Text]** leer, um den Produktnamen zu verwenden.

1. Geben Sie eine **[!UICONTROL Anchor Custom Title]** ein, um Best SEO Practice zu erhalten.

   Dieser Titel ist auf der Seite nicht sichtbar.

1. Setzen Sie **[!UICONTROL Template]** auf einen der folgenden Werte:

   - Um den Link in Text einzufügen, wählen Sie `Product Link Inline Template` aus.

   - Um den Link in einer separaten Zeile zu platzieren, wählen Sie `Product Link Block Template` aus.

1. Klicken Sie auf **[!UICONTROL Select Product]** und führen Sie die folgenden Schritte aus:

   - Navigieren Sie im Baum zu der gewünschten Kategorie.

   - Wählen Sie in der Liste das verknüpfte Produkt aus.

1. Klicken Sie auf **[!UICONTROL Insert Widget]** , um den Link auf der Seite zu platzieren.

   Wenn Sie mit HTML-Code arbeiten, wird oben auf der Seite ein [Markup-Tag](../systems/markup-tags.md) für den Link angezeigt, das in zwei geschweifte Klammern eingeschlossen ist. Verwenden Sie bei Bedarf _Ausschneiden und Einfügen_ , um das Markup-Tag in dem Code zu positionieren, in dem der Link erscheinen soll.

1. Wenn die Inhaltsbearbeitung abgeschlossen ist, klicken Sie auf **[!UICONTROL Save]**.
