---
title: URLs für dynamische Medien
description: Erfahren Sie, wie Sie eine URL für dynamische Medien als relativen Verweis auf ein Bild oder ein anderes Medien-Asset verwenden.
exl-id: 41aabde2-f6cc-4b83-8d56-9753a7aa93e9
feature: CMS, Media
source-git-commit: d3b9b4cd0d12f8d5feb2bad0bf601970f9ee1a36
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%

---

# URLs für dynamische Medien

Eine URL für dynamische Medien ist ein relativer Verweis auf ein Bild oder ein anderes Medien-Asset. Wenn diese Option aktiviert ist, können URLs für dynamische Medien verwendet werden, um eine direkte Verknüpfung zu Assets auf Ihrem Server oder zu Dateien herzustellen, die in einem [Netzwerk zur Inhaltsbereitstellung](media-storage-content-delivery-network.md) gespeichert sind. Die Verwendung von URLs für dynamische Medien kann sich auf die Katalogleistung auswirken, und der [Editor](editor.md#configure-the-editor) kann so konfiguriert werden, dass entweder statische oder dynamische Medien-URLs verwendet werden.

Wie bei allen [Markup-Tags](../systems/markup-tags.md) ist die Anweisung in zwei geschweifte Klammern eingeschlossen. Das Format einer URL für dynamische Medien sieht wie folgt aus:

`\{\{media url="path/to/image.jpg"}}`

Dynamische URL-Anweisungen werden aus gespeicherten HTML-Inhalten verarbeitet, wenn die Seite auf der Storefront gerendert wird. Jedes Mal, wenn die Seite gerendert wird, wird der Inhalt auf `\{\{media url="..."}}` überprüft und jede Direktive wird durch die entsprechende Medien-URL ersetzt.

{{$include /help/_includes/directives-caution.md}}

## Konfigurieren von statischen Medien-URLs

Bilder, die aus dem WYSIWYG-Editor in den Katalog eingefügt werden, haben standardmäßig relative, dynamische URLs. Wenn Sie lieber eine statische URL verwenden möchten, können Sie die Konfigurationseinstellung ändern.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wählen Sie im linken Bereich unter _[!UICONTROL General]_die Option **[!UICONTROL Content Management]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL WYSIWYG Options]** .

   ![WYSIWYG-Optionen](./assets/content-management-wysiwyg-options.png){width="600" zoomable="yes"}

1. Setzen Sie **[!UICONTROL Use Static URLs for Media Content in WYSIWYG]** auf einen der folgenden Werte:

   - `Yes` - Verwendet statische URLs für Medieninhalte, die mit dem WYSIWYG-Editor eingefügt werden. Statische URLs sind absolut und umbrechen, wenn sich die [Basis-URL](../stores-purchase/store-urls.md) des Stores ändert.

   - `No` - (Standard) Verwendet dynamische URLs für Medieninhalte, die mit dem WYSIWYG-Editor basierend auf der `\{\{media url="..."}}` -Direktive eingefügt werden. Dynamische URLs sind relativ und beschädigen nicht, wenn sich die Basis-URL des Stores ändert.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.
