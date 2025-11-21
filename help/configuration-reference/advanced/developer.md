---
title: '[!UICONTROL Advanced] &gt; [!UICONTROL Developer]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Advanced] &gt; [!UICONTROL Developer] des Commerce Admin-Bereichs.
exl-id: 2ef4ba6a-b5a5-419d-8d61-e535e3366370
role: Admin, Developer
feature: Site Management, Configuration, System
source-git-commit: ac364c1b3cab3988c135ade2c6de799c915cee8c
workflow-type: tm+mt
source-wordcount: '798'
ht-degree: 1%

---

# [!UICONTROL Advanced] > [!UICONTROL Developer]

{{config}}

>[!NOTE]
>
>Diese Konfigurationseinstellungen sind nur im [Entwicklermodus](../../systems/developer-tools.md#operation-modes) verfügbar.

## [!UICONTROL Frontend Development Workflow]

![Frontend-Entwicklungs-Workflow](./assets/developer-frontend-development-workflow.png)<!-- zoom -->

Weitere Informationen zum Ändern dieser Einstellungen finden Sie unter [Frontend-Entwicklungs](../../systems/developer-tools.md#frontend-development-workflow)Workflow im _Admin-_).

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Workflow Type] | Global | Bestimmt, ob während der Entwicklung weniger Kompilierung Client- oder Server-seitig stattfindet. Optionen: <br/>**`Client side less compilation`**- Die Kompilierung erfolgt im Browser unter Verwendung der nativen less.js-Bibliothek.<br/>**`Server side less compilation`** - Kompilierung erfolgt auf dem Server mit der Less PHP-Bibliothek. Dies ist der Standardmodus für die Produktion. |

{style="table-layout:auto"}

## [!UICONTROL Developer Client Restrictions]

![Entwickler-Client-Einschränkungen](./assets/developer-developer-client-restrictions.png)<!-- zoom -->

Weitere Informationen zum Ändern dieser Einstellung finden Sie unter [Client-](../../systems/developer-tools.md#client-restrictions)) im _Admin-_.

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Allow IPs (comma separated)] | Shop-Ansicht | Erstellt eine Zulassungsliste von IP-Adressen, die Entwickler-Tools auf einer Live-Site verwenden können, ohne Kunden im Store zu stören. Alle Änderungen an der Site bei Verwendung eines Entwickler-Tools wie _Inline-Übersetzung_ sind nur von den IP-Adressen auf der -Zulassungsliste sichtbar. |

{style="table-layout:auto"}

## [!UICONTROL Template Settings]

![Vorlageneinstellungen](./assets/developer-template-settings.png)<!-- zoom -->

Weitere Informationen zum Ändern dieser Einstellungen finden Sie unter [Optimieren von Ressourcendateien](../../systems/developer-tools.md#optimizing-resource-files) im _Admin-Systemhandbuch_.

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Allow Symlinks] | Shop-Ansicht | Durch die Aktivierung [symbolischer Links](https://en.wikipedia.org/wiki/Symbolic_link) kann Ihre Site Sicherheitsrisiken ausgesetzt sein. Dies wird für einen Produktionsspeicher nicht empfohlen. |
| [!UICONTROL Minify Html] | Shop-Ansicht | Legt fest, ob die HTML für Store-Vorlagen minimiert ist. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Debug]

![Debug](./assets/developer-debug.png)<!-- zoom -->

Weitere Informationen zum Ändern dieser Einstellungen finden Sie unter [Hinweise für Vorlagenpfade](../../systems/developer-tools.md#template-path-hints) im _Admin-_.

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable Template Path Hints for Storefront] | Shop-Ansicht | Fügt zu der Storefront eine Notation hinzu, die den Pfad zu jeder Vorlage angibt, die auf der Seite verwendet wird. Optionen: `Yes` / `No` |
| [!UICONTROL Enable Template Path Hints for Admin] | Global | Fügt der Admin-Instanz eine Notation hinzu, die den Pfad zu jeder Vorlage angibt, die auf der Seite verwendet wird. Optionen: `Yes` / `No` |
| [!UICONTROL Add Block Class Type to Hints] | Shop-Ansicht | Umfasst die Namen von Blöcken in den Hinweisen für Vorlagenpfade. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Translate Inline]

![Inline übersetzen](./assets/developer-translate-inline.png)<!-- zoom -->

Weitere Informationen zum Ändern dieser Einstellungen finden Sie unter [Inline übersetzen](../../systems/developer-tools.md#translate-inline) im _Admin Systems Guide_.

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable for Storefront] | Shop-Ansicht | Aktiviert den Inline-Übersetzer für die Storefront. Der Schnittstellentext kann für jede Shop-Ansicht bearbeitet werden. Auf die Zulassungsliste setzen Um den Inline Translator zu verwenden, ohne den Live-Store zu stören, fügen Sie Ihre IP-Adresse zur Seite „Client-Einschränkungen für Entwickler“ hinzu. |
| [!UICONTROL Enable for Admin] | Global | Aktiviert den Inline-Übersetzer für den Administrator. Im Gegensatz zur Storefront kann der Administrator nicht in mehrere Sprachen übersetzt werden. Die Feldbezeichnungen und anderer Text in der Benutzeroberfläche können jedoch geändert werden. |

{style="table-layout:auto"}

## [!UICONTROL JavaScript Settings]

![JavaScript-Einstellungen](./assets/developer-javascript-settings.png)<!-- zoom -->

Weitere Informationen zum Ändern dieser Einstellungen finden Sie unter [Optimieren von Ressourcendateien](../../systems/developer-tools.md#optimizing-resource-files) im _Admin-Systemhandbuch_.

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Merge JavaScript Files] | Shop-Ansicht | Führt mehrere JavaScript-Dateien in einer Datei zusammen, um die Seitenladezeit zu verbessern. |
| [!UICONTROL Enable JavaScript Bundling] | Shop-Ansicht | Legt fest, ob mehrere JavaScript-Dateien in einer Datei gebündelt werden können. Optionen: `Yes` / `No` |
| [!UICONTROL Minify JavaScript Files] | Shop-Ansicht | Entfernt unnötige Zeichen, Leerzeichen und Einzüge, um die Größe des Codes zu reduzieren. |
| [!UICONTROL Move JS code to the bottom of the page] | Global | Verschiebt, falls aktiviert, den JS-Code zum Seitenende. Optionen: `Yes` / `No` |
| [!UICONTROL Translation Strategy] | Global | Bestimmt die vom System verwendete Übersetzungsmethode. Optionen: <br/>**`Dictionary`**- Übersetzung in der Storefront.<br/>**`Embedded`** - Übersetzung für Administratoren. |
| [!UICONTROL Log JS Errors to Session Storage] | Global | Wenn aktiviert, kann von Funktionstests für das Reporting verwendet werden. Optionen: `Yes` / `No` |
| [!UICONTROL Log JS Errors to Session Storage Key] | Global | Identifiziert den Schlüssel zum Abrufen erfasster JS-Fehler. |

{style="table-layout:auto"}

## [!UICONTROL CSS Settings]

![CSS-Einstellungen](./assets/developer-css-settings.png)<!-- zoom -->

Weitere Informationen zum Ändern dieser Einstellungen finden Sie unter [Optimieren von Ressourcendateien](../../systems/developer-tools.md#optimizing-resource-files) im _Admin-Systemhandbuch_.

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Merge CSS Files] | Shop-Ansicht | Führt mehrere CSS-Dateien in einer Datei zusammen, um die Seitenladezeit zu verbessern. Optionen: `Yes` / `No` |
| [!UICONTROL Minify CSS Files] | Shop-Ansicht | Entfernt unnötige Zeichen, Leerzeichen und Einzüge, um die Größe des Codes zu reduzieren. Optionen: `Yes` / `No` |
| [!UICONTROL Use CSS critical path] | Global | Der _CSS-kritische Pfad_ stellt minimiertes kritisches CSS inline in `<head>` bereit und verzögert alle nicht kritischen Stile, die asynchron geladen werden. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Image Processing Settings]

![Bildverarbeitungseinstellungen](./assets/developer-image-processing-settings.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Image Adapter] | Global | Gibt den Adapter zum Rendern von Bildern an. Leeren Sie nach dem Ändern der Adaptereinstellung den Cache für Katalogbilder. Optionen: `PHP GD2` / `ImageMagick` <br/><br/>**_Hinweis:_** Der ICO-Dateityp wird nur vom ImageMagik-Adapter unterstützt. |

{style="table-layout:auto"}

## [!UICONTROL Caching Settings]

![Caching-Einstellungen](./assets/developer-cache-settings.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Cache User Defined Attributes] | Global | Wenn diese Option aktiviert ist, werden benutzerdefinierte Attribute und EAV-Attribute (System Entity Attribute Value) zwischengespeichert. Diese Option kann die Leistung steigern, erfordert jedoch zusätzlichen Speicherplatz für das Caching. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Static Files Settings]

![Statische Dateieinstellungen](./assets/developer-static-files-settings.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Sign Static Files] | Global | Wenn diese Option aktiviert ist, wird der URL statischer Dateien eine digitale Signatur hinzugefügt, damit Browser erkennen können, wann eine neuere Version der Datei verfügbar ist. Wenn sich die Signatur einer Datei von der unterscheidet, die im Cache des Browsers gespeichert ist, wird die neuere Version der Datei verwendet. Zu den statischen Dateien, die signiert werden können, gehören JavaScript, CSS, Bilder und Schriftarten. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Grid Settings]

![Rastereinstellungen](./assets/developer-grid-settings.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Asynchronous Indexing|Global] | Legt fest, wann Entitäten des Auftragsverarbeitungssystems, wie Bestellungen, Rechnungen, Lieferungen und Gutschriften, dem Raster hinzugefügt und neu indiziert werden. Die asynchrone Indizierung kann verwendet werden, um Datensperren während Speichervorgängen zu vermeiden und die Verarbeitungszeit zu verkürzen. Optionen: <br/>**`Disable`**- (Standard) Entitäten, die sich auf die Reihenfolge beziehen, werden dem Raster zu verschiedenen Zeitpunkten hinzugefügt. wie sie gespeichert werden.<br/>**`Enable`** - Auftragsbezogene Entitäten werden dem Raster nur während eines geplanten Cron-Auftrags hinzugefügt. Cron sollte so konfiguriert sein, dass es einmal pro Minute ausgeführt wird. |

{style="table-layout:auto"}
