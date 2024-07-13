---
title: Layout-Aktualisierungen
description: Erfahren Sie, wie Sie mit Layoutaktualisierungen das Layout einer Seite anpassen können.
exl-id: e2d8261f-cae1-4bd4-a047-f861dd7ca14e
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '989'
ht-degree: 0%

---

# Layout-Aktualisierungen

Bevor Sie mit der Arbeit mit benutzerdefinierten Layoutaktualisierungen beginnen, müssen Sie wissen, wie die Seiten Ihres Stores aufgebaut sind und wie sich die Begriffe *layout* und *layout update* unterscheiden. Layout bezieht sich auf die visuelle und strukturelle Zusammensetzung der Seite. Layout-Update bezieht sich auf einen bestimmten Satz von XML-Anweisungen, die die Erstellung der Seite überschreiben oder anpassen können.

Das XML-Layout Ihres [!DNL Commerce]-Stores ist eine hierarchische Struktur von Containern und Blöcken. Einige Elemente werden auf jeder Seite angezeigt, andere nur auf bestimmten Seiten. Weitere Informationen zu Layout, Containern und Bausteinen finden Sie in der [Layouts - Übersicht](https://developer.adobe.com/commerce/frontend-core/guide/layouts/) im _Frontend-Entwicklerhandbuch_.

Mit dem Werkzeug [Widget](widgets.md) können Sie dem Standardlayout einer Seite einfach einen vorhandenen [Inhaltsbaustein](blocks.md) hinzufügen. Für erweiterte Aktualisierungen müssen Sie den XML-Layout-Aktualisierungscode auf dem Server speichern und dann auf die Datei als benutzerdefinierte Layout-Update vom Administrator verweisen. Einen Überblick über den Prozess finden Sie unter [Verwenden von Layout-Updates](layout-updates.md#place-a-block-using-layout-updates).

Im folgenden Diagramm sind die Namen, die auf Container verweisen, schwarz und die Blocktypen bzw. Blockklassenpfade blau.

![Standarddiagramm des Blocklayouts](./assets/page-layout-default.png){width="500" zoomable="yes"}

| Blocktyp | Beschreibung |
|--- |--- |
| `page/html` | Der Name dieses Bausteins ist `root` und einer der wenigen Stamm-Bausteine im Layout. Sie können auch einen eigenen Block erstellen und ihn mit dem Namen &quot;`root`&quot; benennen, der für Blöcke dieses Typs der Standardname ist. Pro Seite kann nur ein Block dieses Typs vorhanden sein. |
| `page/html_head` | Der Blockname lautet `head` und ist ein untergeordnetes Element des Stammblocks. Pro Seite kann nur ein Block dieses Typs vorhanden sein, der nicht entfernt werden darf. |
| `page/html_notices` | Der Blockname lautet `global_notices` und ist ein untergeordnetes Element des Stammblocks. Wenn dieser Baustein aus dem Layout entfernt wird, werden die globalen Hinweise nicht auf der Seite angezeigt. Pro Seite kann nur ein Block dieses Typs vorhanden sein. |
| `page/html_header` | Der Blockname lautet `header` und ist ein untergeordnetes Element des Stammblocks. Dieser Block entspricht der visuellen Kopfzeile am oberen Seitenrand und enthält mehrere Standardblöcke. Pro Seite kann nur ein Block dieses Typs vorhanden sein, der nicht entfernt werden darf. |
| `page/html_wrapper` | Dieser Block ist zwar im Standardlayout enthalten, wird jedoch nicht mehr unterstützt und ist nur zur Gewährleistung der Abwärtskompatibilität enthalten. Verwenden Sie keine Blöcke dieses Typs. |
| `page/html_breadcrumbs` | Der Name dieses Blocks ist `breadcrumbs` und es ist ein untergeordnetes Element des Kopfzeilenblocks. In diesem Block werden Breadcrumbs für die aktuelle Seite angezeigt. Pro Seite kann nur ein Block dieses Typs vorhanden sein. |
| `page/html_footer` | Der Blockname lautet `footer` und ist ein untergeordnetes Element des Stammblocks. Der Fußzeilenblock entspricht der visuellen Fußzeile am unteren Seitenrand und enthält mehrere Standardblöcke. Pro Seite kann nur ein Block dieses Typs vorhanden sein, der nicht entfernt werden darf. |
| `page/template_links` | Es gibt zwei Blöcke dieses Typs im Standardlayout. Der Block `top.links` ist ein untergeordnetes Element des Kopfzeilenblocks und entspricht dem oberen Navigationsmenü. Der Block `footer_links` ist ein untergeordnetes Element des Fußzeilenblocks und entspricht dem unteren Navigationsmenü. <br/><br/>**_Hinweis:_**Die Vorlagenlinks können bearbeitet werden, wie in den Beispielen dargestellt. |
| `page/switch` | Ein Standardlayout besteht aus zwei Blöcken dieses Typs. Der Block `store_language` ist ein untergeordnetes Element des Kopfzeilenblocks und entspricht dem Sprachwechsel in der obersten Sprache. Der Block `store_switcher` ist ein untergeordnetes Element des Fußzeilenblocks und entspricht dem unteren Speicherschalter. |
| core/messages | Ein Standardlayout besteht aus zwei Blöcken dieses Typs. Der Block `global_messages` zeigt globale Nachrichten an. Der Block `messages` wird verwendet, um alle anderen Nachrichten anzuzeigen. Wenn Sie diese Bausteine entfernen, werden dem Kunden keine Nachrichten angezeigt. |
| `core/text_list` | Dieser Blocktyp wird in [!DNL Commerce] häufig als Platzhalter zum Rendern von untergeordneten Blöcken verwendet. |
| `core/profiler` | Pro Seite gibt es nur eine Instanz dieses Blocktyps. Es wird für den internen [!DNL Commerce] Profiler verwendet und sollte nicht für einen anderen Zweck verwendet werden. |

{style="table-layout:auto"}

## Bausteine mithilfe von Layoutaktualisierungen platzieren

[Layout-Aktualisierungen](layout-updates.md) ermöglichen es, das Layout einer Seite anzupassen. Layoutaktualisierungen bieten mehr Flexibilität als ein [Widget](widgets.md), erfordern jedoch Zugriff auf den Server und grundlegende XML-Kenntnisse.

Die folgenden Schritte zeigen, wie Sie mit einem Layout-Update einen Block auf einer Seite platzieren können. Spezifische Beispiele und Hilfe zur Syntax finden Sie unter [Allgemeine Aufgaben zur Layoutanpassung](https://developer.adobe.com/commerce/frontend-core/guide/layouts/) im _Frontend-Entwicklerhandbuch_.

### 1. Schritt: Baustein erstellen

1. Erstellen Sie den [block](block-add.md), den Sie platzieren möchten.

1. Beachten Sie den Wert &quot;`block_id`&quot;, da er in den Anweisungen zum Aktualisieren des Layouts verwendet wird.

### Schritt 2: Layout-Update in XML erstellen

1. Erstellen Sie die Layoutanweisungen in XML so, dass sie [auf einen CMS-Block verweisen](https://developer.adobe.com/commerce/frontend-core/guide/layouts/xml-manage/).

1. Speichern Sie die [Layoutanweisungen](https://developer.adobe.com/commerce/frontend-core/guide/layouts/xml-instructions/) auf dem Server im Ordner &quot;Layout&quot;, in dem die XML-Dateien für das Design gespeichert sind.

   Beispiel:

   `<theme_dir>/<Namespace>_<Module>/layout`

   Der Layout-Handle ist der Dateiname, der mit &quot;`cms_page_view_selectable_`&quot; beginnt, gefolgt vom URL-Schlüssel der CMS-Seite, der Layoutaktualisierungsoption und dem &quot;`xml`&quot;-Dateisuffix. Im folgenden Beispiel ist `customer-service` der URL-Schlüssel der Seite und `ChatTool` die Option, mit der Sie das Layout-Update auf die Seite anwenden.

   `cms_page_view_selectable_`&lt;`customer-service`>`_`&lt;`ChatTool`>`.xml`

   | Element | Beschreibung |
   |--- |--- |
   | CMS-Seiten-ID | Der URL-Schlüssel der Seite mit einem Schrägstrich (`/`), der durch einen Unterstrich (`_`) ersetzt wird. |
   | Name der Layoutaktualisierung | Die Option, die für _Benutzerdefiniertes Layout-Update_ angezeigt wird. |

   {style="table-layout:auto"}

### Schritt 3: Referenzieren Sie das Layout-Update von der Seite

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Suchen Sie die Seite, auf der Sie den Block platzieren möchten, und öffnen Sie ihn im Bearbeitungsmodus.

1. Scrollen Sie nach unten und erweitern Sie den Abschnitt **[!UICONTROL Design]** um den ![Erweiterungsselektor](../assets/icon-display-expand.png).

1. Um alle verfügbaren Layout-Aktualisierungen anzuzeigen, die mit der Seite verbunden sind, klicken Sie auf das Menü **[!UICONTROL Custom Layout Update]** .

   ![Liste der benutzerdefinierten Layoutaktualisierungen](./assets/page-design-custom-layout-update.png){width="400" zoomable="yes"}

1. Wählen Sie das Layout-Update aus, das Sie auf die Seite anwenden möchten.

### Schritt 4: Speichern und aktualisieren Sie den Cache

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save & Close]**.

1. Klicken Sie in der Meldung oben im Arbeitsbereich auf **[!UICONTROL Cache Management]** und aktualisieren Sie alle ungültigen Cache-Elemente.
