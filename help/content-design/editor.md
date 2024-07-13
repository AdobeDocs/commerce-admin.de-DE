---
title: WYSIWYG Editor
description: Erfahren Sie, wie Sie den Editor verwenden und mit Inhalten in der Ansicht _What You See Is What You Get_ (WYSIWYG) arbeiten.
exl-id: 209ca9d6-973c-4ad9-b7cd-4fba58dbfbb8
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# WYSIWYG Editor

Der Editor bietet Ihnen die Möglichkeit, während der Arbeit in einer Ansicht _Was Sie sehen ist was Sie erhalten_ (WYSIWYG) des Inhalts eingeben und formatieren zu können. Wenn Sie es vorziehen, direkt mit dem zugrunde liegenden HTML-Code zu arbeiten, können Sie die Modi einfach ändern. Mit dem Editor können Inhalte für [Seiten](pages.md), [Blöcke](blocks.md) und [Produktbeschreibungen](../catalog/product-content.md) erstellt werden. Wenn Sie an Produktdetails arbeiten, greifen Sie auf den Editor zu, indem Sie auf **[!UICONTROL Show / Hide Editor]** klicken.

>[!NOTE]
>
>TinyMCE 5 ist der standardmäßige WYSIWYG-Editor. Durch ein Update der TinyMCE 5.10-Bibliothek in Adobe Commerce und Magento Open Source 2.4.5 wurde eine Sicherheitslücke behoben, die eine beliebige Ausführung von JavaScript bei der Aktualisierung eines Bildes oder Links mit einigen URL-Typen ermöglichte. TinyMCE 3 wurde in Version 2.4.0 eingestellt und in Version 2.4.3 entfernt. TinyMCE 4 wurde in Version 2.4.4 entfernt.

![Editor-Symbolleiste](./assets/editor-toolbar.png){width="700" zoomable="yes"}

Die folgenden Themen enthalten detaillierte Informationen zur Verwendung des Editors:

- [Link einfügen](editor-insert-link.md)
- [Einfügen eines Bildes](editor-insert-image.md)
- [Widget einfügen](editor-widget.md)
- [Einfügen einer Variablen](editor-insert-variable.md)

## Konfigurieren des Editors

Der WYSIWYG-Editor ist standardmäßig aktiviert und kann zum Bearbeiten von Inhalten auf CMS-Seiten und -Blöcken sowie in Produkten und Kategorien verwendet werden. In der Konfiguration können Sie den Editor aktivieren oder deaktivieren und festlegen, dass anstelle von [dynamisch](../catalog/catalog-urls.md#dynamic-url) statische URLs für Medieninhalte in Produkt- und Kategoriebeschreibungen verwendet werden.

![WYSIWYG-Optionen](./assets/content-management-wysiwyg-options.png){width="600" zoomable="yes"}

Eine ausführliche Beschreibung aller WYSIWYG-Optionen finden Sie unter [Content Management](../configuration-reference/general/content-management.md) in der _Konfigurationsreferenz_.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wählen Sie im linken Bereich unter _[!UICONTROL General]_die Option **[!UICONTROL Content Management]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) **[!UICONTROL WYSIWYG Options]**.

1. Legen Sie **[!UICONTROL Enable WYSIWYG Editor]** auf Ihre Voreinstellung fest.

   Der Editor ist standardmäßig aktiviert.

1. Legen Sie **[!UICONTROL Static URLs for Media Content in WYSIWYG]** für alle mit dem WYSIWYG-Editor eingegebenen [Medieninhalte](../catalog/catalog-urls.md#static-url) auf Ihre Voreinstellung fest.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.
