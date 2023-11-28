---
title: WYSIWYG Editor
description: Erfahren Sie, wie Sie den Editor verwenden und mit Inhalten in der Ansicht _What You See Is What You Get_ (WYSIWYG) arbeiten.
exl-id: 209ca9d6-973c-4ad9-b7cd-4fba58dbfbb8
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 0%

---

# WYSIWYG Editor

Der Editor bietet Ihnen die Möglichkeit, während der Arbeit in einem _Was du siehst, ist was du bekommst_ (WYSIWYG) anzeigen. Wenn Sie es vorziehen, direkt mit dem zugrunde liegenden HTML-Code zu arbeiten, können Sie die Modi einfach ändern. Der Editor kann zum Erstellen von Inhalten für [pages](pages.md), [Bausteine](blocks.md), und [Produktbeschreibungen](../catalog/product-content.md). Wenn Sie an Produktdetails arbeiten, rufen Sie den Editor auf, indem Sie auf **[!UICONTROL Show / Hide Editor]**.

>[!NOTE]
>
>TinyMCE 5 ist der standardmäßige WYSIWYG-Editor. Durch ein Update der TinyMCE 5.10-Bibliothek in Adobe Commerce und Magento Open Source 2.4.5 wurde eine Sicherheitslücke behoben, die eine beliebige JavaScript-Ausführung ermöglichte, wenn ein Bild oder ein Link mit einigen URL-Typen aktualisiert wurde. TinyMCE 3 wurde in Version 2.4.0 eingestellt und in Version 2.4.3 entfernt. TinyMCE 4 wurde in Version 2.4.4 entfernt.

![Editor-Symbolleiste](./assets/editor-toolbar.png){width="700" zoomable="yes"}

Die folgenden Themen enthalten detaillierte Informationen zur Verwendung des Editors:

- [Link einfügen](editor-insert-link.md)
- [Einfügen eines Bildes](editor-insert-image.md)
- [Widget einfügen](editor-widget.md)
- [Einfügen einer Variablen](editor-insert-variable.md)

## Konfigurieren des Editors

Der WYSIWYG-Editor ist standardmäßig aktiviert und kann zum Bearbeiten von Inhalten auf CMS-Seiten und -Blöcken sowie in Produkten und Kategorien verwendet werden. In der Konfiguration können Sie den Editor aktivieren bzw. deaktivieren und die Verwendung von statischem anstelle von [dynamisch](../catalog/catalog-urls.md#dynamic-url), URLs für Medieninhalte in Produkt- und Kategoriebeschreibungen.

![WYSIWYG-Optionen](./assets/content-management-wysiwyg-options.png){width="600" zoomable="yes"}

Eine ausführliche Beschreibung aller WYSIWYG-Optionen finden Sie unter [Content Management](../configuration-reference/general/content-management.md) im _Konfigurationsreferenz_.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Im linken Bereich unter _[!UICONTROL General]_auswählen **[!UICONTROL Content Management]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) **[!UICONTROL WYSIWYG Options]**.

1. Satz **[!UICONTROL Enable WYSIWYG Editor]** nach Ihren Wünschen.

   Der Editor ist standardmäßig aktiviert.

1. Satz **[!UICONTROL Static URLs for Media Content in WYSIWYG]** zu Ihrer Präferenz für alle [Medieninhalte](../catalog/catalog-urls.md#static-url) wird mit dem WYSIWYG-Editor eingegeben.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.
