---
title: Layout-Aktualisierungen
description: Erfahren Sie, wie Sie mit Layoutaktualisierungen das Layout einer Seite anpassen können.
exl-id: e2d8261f-cae1-4bd4-a047-f861dd7ca14e
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '1007'
ht-degree: 0%

---

# Layout-Aktualisierungen

Bevor Sie mit der Arbeit mit benutzerdefinierten Layout-Aktualisierungen beginnen, müssen Sie wissen, wie die Seiten Ihres Stores aufgebaut sind und wie sich die Begriffe unterscheiden *layout* und *Layoutaktualisierung*. Layout bezieht sich auf die visuelle und strukturelle Zusammensetzung der Seite. Layout-Update bezieht sich auf einen bestimmten Satz von XML-Anweisungen, die die Erstellung der Seite überschreiben oder anpassen können.

Das XML-Layout Ihrer [!DNL Commerce] store ist eine hierarchische Struktur von Containern und Blöcken. Einige Elemente werden auf jeder Seite angezeigt, andere nur auf bestimmten Seiten. Weitere Informationen zu Layout, Containern und Bausteinen finden Sie unter [Layouts - Übersicht](https://developer.adobe.com/commerce/frontend-core/guide/layouts/) im _Frontend-Entwicklerhandbuch_.

Die [Widget](widgets.md) ist eine einfache Möglichkeit, ein vorhandenes [Inhaltsbaustein](blocks.md) zum Standardlayout einer Seite. Für erweiterte Aktualisierungen müssen Sie den XML-Layout-Aktualisierungscode auf dem Server speichern und dann auf die Datei als benutzerdefinierte Layout-Update vom Administrator verweisen. Einen Überblick über den Prozess finden Sie unter [Layout-Updates verwenden](layout-updates.md#place-a-block-using-layout-updates).

Im folgenden Diagramm sind die Namen, die auf Container verweisen, schwarz und die Blocktypen bzw. Blockklassenpfade blau.

![Layout von Standardblöcken](./assets/page-layout-default.png){width="500" zoomable="yes"}

| Blocktyp | Beschreibung |
|--- |--- |
| `page/html` | Der Name dieses Blocks lautet `root` und es ist einer der wenigen Stammbausteine im Layout. Sie können auch einen eigenen Block erstellen und ihn benennen `root`, der Standardname für Bausteine dieses Typs ist. Pro Seite kann nur ein Block dieses Typs vorhanden sein. |
| `page/html_head` | Der Blockname lautet `head` und es ist ein untergeordnetes Element des Stammblocks. Pro Seite kann nur ein Block dieses Typs vorhanden sein, der nicht entfernt werden darf. |
| `page/html_notices` | Der Blockname lautet `global_notices` und es ist ein untergeordnetes Element des Stammblocks. Wenn dieser Baustein aus dem Layout entfernt wird, werden die globalen Hinweise nicht auf der Seite angezeigt. Pro Seite kann nur ein Block dieses Typs vorhanden sein. |
| `page/html_header` | Der Blockname lautet `header` und es ist ein untergeordnetes Element des Stammblocks. Dieser Block entspricht der visuellen Kopfzeile am oberen Seitenrand und enthält mehrere Standardblöcke. Pro Seite kann nur ein Block dieses Typs vorhanden sein, der nicht entfernt werden darf. |
| `page/html_wrapper` | Dieser Block ist zwar im Standardlayout enthalten, wird jedoch nicht mehr unterstützt und ist nur zur Gewährleistung der Abwärtskompatibilität enthalten. Verwenden Sie keine Blöcke dieses Typs. |
| `page/html_breadcrumbs` | Der Name dieses Blocks lautet `breadcrumbs` und es ist ein untergeordnetes Element des Kopfzeilenblocks. In diesem Block werden Breadcrumbs für die aktuelle Seite angezeigt. Pro Seite kann nur ein Block dieses Typs vorhanden sein. |
| `page/html_footer` | Der Blockname lautet `footer` und es ist ein untergeordnetes Element des Stammblocks. Der Fußzeilenblock entspricht der visuellen Fußzeile am unteren Seitenrand und enthält mehrere Standardblöcke. Pro Seite kann nur ein Block dieses Typs vorhanden sein, der nicht entfernt werden darf. |
| `page/template_links` | Es gibt zwei Blöcke dieses Typs im Standardlayout. Die `top.links` block ist ein untergeordnetes Element des Kopfzeilenblocks und entspricht dem oberen Navigationsmenü. Die `footer_links` block ist ein untergeordnetes Element des Fußzeilenblocks und entspricht dem unteren Navigationsmenü. <br/><br/>**_Hinweis:_**Sie können die Vorlagenlinks bearbeiten, wie in den Beispielen dargestellt. |
| `page/switch` | Ein Standardlayout besteht aus zwei Blöcken dieses Typs. Die `store_language` -Block ist ein untergeordnetes Element des Kopfzeilenblocks und entspricht dem Sprachwechsel in der obersten Sprache. Die `store_switcher` -Block ist ein untergeordnetes Element des Fußzeilenblocks und entspricht dem unteren Store-Umschalter. |
| core/messages | Ein Standardlayout besteht aus zwei Blöcken dieses Typs. Die `global_messages` -Block zeigt globale Nachrichten an. Die `messages` -Block verwendet wird, um alle anderen Nachrichten anzuzeigen. Wenn Sie diese Bausteine entfernen, werden dem Kunden keine Nachrichten angezeigt. |
| `core/text_list` | Diese Art von Block ist in der Regel [!DNL Commerce] als Platzhalter für das Rendern von untergeordneten Bausteinen. |
| `core/profiler` | Pro Seite gibt es nur eine Instanz dieses Blocktyps. Sie wird für die interne [!DNL Commerce] Profiler und sollten für keinen anderen Zweck verwendet werden. |

{style="table-layout:auto"}

## Bausteine mithilfe von Layoutaktualisierungen platzieren

[Layout-Aktualisierungen](layout-updates.md) ermöglichen die Anpassung des Layouts einer Seite. Layout-Aktualisierungen bieten mehr Flexibilität als [Widget](widgets.md), benötigen jedoch Zugriff auf den Server und grundlegende Kenntnisse von XML.

Die folgenden Schritte zeigen, wie Sie mit einem Layout-Update einen Block auf einer Seite platzieren können. Spezifische Beispiele und Hilfe zur Syntax finden Sie unter [Allgemeine Aufgaben zur Layoutanpassung](https://developer.adobe.com/commerce/frontend-core/guide/layouts/) im _Frontend-Entwicklerhandbuch_.

### 1. Schritt: Baustein erstellen

1. Erstellen Sie die [block](block-add.md) die du platzieren willst.

1. Beachten Sie die `block_id`, da sie in den Anweisungen zur Layout-Aktualisierung verwendet wird.

### Schritt 2: Layout-Update in XML erstellen

1. Erstellen Sie die Layoutanweisungen in XML in [Referenzieren eines CMS-Bausteins](https://developer.adobe.com/commerce/frontend-core/guide/layouts/xml-manage/).

1. Speichern Sie die [Layoutanleitungen](https://developer.adobe.com/commerce/frontend-core/guide/layouts/xml-instructions/) auf dem Server im Ordner &quot;Layout&quot;, in dem XML-Dateien für das Design gespeichert werden.

   Beispiel:

   `<theme_dir>/<Namespace>_<Module>/layout`

   Der Layout-Handle ist der Dateiname, der mit `cms_page_view_selectable_`, gefolgt vom URL-Schlüssel der CMS-Seite, der Layout-Aktualisierungsoption und der `xml` Dateisuffix. Im folgenden Beispiel: `customer-service` der URL-Schlüssel der Seite ist und `ChatTool` ist die Option, die Sie auswählen, um das Layout-Update auf die Seite anzuwenden.

   `cms_page_view_selectable_`&lt;`customer-service`>`_`&lt;`ChatTool`>`.xml`

   | Element | Beschreibung |
   |--- |--- |
   | CMS-Seiten-ID | Der URL-Schlüssel der Seite mit einem Schrägstrich (`/`) ersetzt durch einen Unterstrich (`_`). |
   | Name der Layoutaktualisierung | Die Option, die für _Benutzerdefiniertes Layout - Update_. |

   {style="table-layout:auto"}

### Schritt 3: Referenzieren Sie das Layout-Update von der Seite

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Suchen Sie die Seite, auf der Sie den Block platzieren möchten, und öffnen Sie ihn im Bearbeitungsmodus.

1. Hinunter scrollen und erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Design]** Abschnitt.

1. Um alle verfügbaren Layout-Aktualisierungen anzuzeigen, die mit der Seite verbunden sind, klicken Sie auf die **[!UICONTROL Custom Layout Update]** Menü.

   ![Liste der benutzerdefinierten Layoutaktualisierungen](./assets/page-design-custom-layout-update.png){width="400" zoomable="yes"}

1. Wählen Sie das Layout-Update aus, das Sie auf die Seite anwenden möchten.

### Schritt 4: Speichern und aktualisieren Sie den Cache

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save & Close]**.

1. Klicken Sie in der Meldung oben im Arbeitsbereich auf **[!UICONTROL Cache Management]** und aktualisieren Sie alle ungültigen Cache-Elemente.
