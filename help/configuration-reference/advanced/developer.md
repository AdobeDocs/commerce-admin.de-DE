---
title: '[!UICONTROL Advanced] &gt; [!UICONTROL Developer]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Advanced] &gt; [!UICONTROL Developer] des Commerce-Administrators.
exl-id: 2ef4ba6a-b5a5-419d-8d61-e535e3366370
role: Admin, Developer
feature: Site Management, Configuration, System
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
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

Weitere Informationen zum Ändern dieser Einstellungen finden Sie unter [Frontend-Entwicklungs-Workflow](../../systems/developer-tools.md#frontend-development-workflow) im _Administratorsystemhandbuch_.

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Workflow Type] | Global | Bestimmt, ob während der Entwicklung eine geringere Kompilierung auf Client- oder Server-Seite stattfindet. Optionen: <br/>**`Client side less compilation`**- Die Kompilierung erfolgt im Browser mithilfe der nativen Bibliothek less.js.<br/>**`Server side less compilation`** - Die Kompilierung erfolgt auf dem Server mithilfe der Less PHP-Bibliothek. Dies ist der Standardmodus für die Produktion. |

{style="table-layout:auto"}

## [!UICONTROL Developer Client Restrictions]

![Client-Beschränkungen für Entwickler](./assets/developer-developer-client-restrictions.png)<!-- zoom -->

Weitere Informationen zum Ändern dieser Einstellung finden Sie unter [Client-Beschränkungen](../../systems/developer-tools.md#client-restrictions) im _Administratorsystemhandbuch_.

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Allow IPs (comma separated)] | Store-Ansicht | Erstellt eine Zulassungsliste von IP-Adressen, die Entwicklertools auf einer Live-Site verwenden können, ohne Kunden im Store zu stören. Änderungen an der Site bei Verwendung eines Entwickler-Tools wie _Inline-Übersetzung_ sind nur in den IP-Adressen auf der Zulassungsliste sichtbar. |

{style="table-layout:auto"}

## [!UICONTROL Template Settings]

![Vorlageneinstellungen](./assets/developer-template-settings.png)<!-- zoom -->

Weitere Informationen zum Ändern dieser Einstellungen finden Sie unter [Optimieren von Ressourcendateien](../../systems/developer-tools.md#optimizing-resource-files) im _Administratorsystemhandbuch_.

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Allow Symlinks] | Store-Ansicht | Die Aktivierung von [symbolischen Links](https://en.wikipedia.org/wiki/Symbolic_link) stellt möglicherweise Sicherheitsrisiken für Ihre Site dar und wird für einen Produktionsspeicher nicht empfohlen. |
| [!UICONTROL Minify Html] | Store-Ansicht | Bestimmt, ob die HTML für Store-Vorlagen minimiert wird. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Debug]

![Debug](./assets/developer-debug.png)<!-- zoom -->

Weitere Informationen zum Ändern dieser Einstellungen finden Sie unter [Vorlagenpfadhinweise](../../systems/developer-tools.md#template-path-hints) im _Administratorsystemhandbuch_.

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable Template Path Hints for Storefront] | Store-Ansicht | Fügt eine Notation zur Storefront hinzu, die den Pfad zu den einzelnen Vorlagen angibt, die auf der Seite verwendet werden. Optionen: `Yes` / `No` |
| [!UICONTROL Enable Template Path Hints for Admin] | Global | Fügt dem Admin eine Notation hinzu, die den Pfad zu den einzelnen Vorlagen angibt, die auf der Seite verwendet werden. Optionen: `Yes` / `No` |
| [!UICONTROL Add Block Class Type to Hints] | Store-Ansicht | Umfasst die Namen der Blöcke in den Vorlagenpfadhinweisen. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Translate Inline]

![Inline übersetzen](./assets/developer-translate-inline.png)<!-- zoom -->

Weitere Informationen zum Ändern dieser Einstellungen finden Sie unter [Inline-Übersetzung](../../systems/developer-tools.md#translate-inline) im _Administratorsystemhandbuch_.

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable for Storefront] | Store-Ansicht | Aktiviert den Inline-Übersetzer für die Storefront. Der Oberflächentext kann für jede Store-Ansicht bearbeitet werden. Um den Inline-Übersetzer zu verwenden, ohne den Live Store zu stören, fügen Sie Ihre IP-Adresse zur Zulassungsliste &quot;Developer Client Restrictions&quot;hinzu. |
| [!UICONTROL Enable for Admin] | Global | Aktiviert den Inline-Übersetzer für den Administrator. Im Gegensatz zur Storefront kann der Administrator nicht in mehrere Sprachen übersetzt werden. Die Feldbezeichnungen und anderen Text in der Benutzeroberfläche können jedoch geändert werden. |

{style="table-layout:auto"}

## [!UICONTROL JavaScript Settings]

![JavaScript-Einstellungen](./assets/developer-javascript-settings.png)<!-- zoom -->

Weitere Informationen zum Ändern dieser Einstellungen finden Sie unter [Optimieren von Ressourcendateien](../../systems/developer-tools.md#optimizing-resource-files) im _Administratorsystemhandbuch_.

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Merge JavaScript Files] | Store-Ansicht | Führt mehrere JavaScript-Dateien in einer Datei zusammen, um die Seitenladezeit zu verbessern. |
| [!UICONTROL Enable JavaScript Bundling] | Store-Ansicht | Bestimmt, ob mehrere JavaScript-Dateien in einer Datei gebündelt werden können. Optionen: `Yes` / `No` |
| [!UICONTROL Minify JavaScript Files] | Store-Ansicht | Entfernt unnötige Zeichen, Leerzeichen und Einzüge, um die Größe des Codes zu reduzieren. |
| [!UICONTROL Move JS code to the bottom of the page] | Global | Wenn diese Option aktiviert ist, wird der JS-Code an den unteren Rand der Seite verschoben. Optionen: `Yes` / `No` |
| [!UICONTROL Translation Strategy] | Global | Bestimmt die Übersetzungsmethode, die vom System verwendet wird. Optionen: <br/>**`Dictionary`**- Übersetzung auf der Storefront.<br/>**`Embedded`** - Übersetzung auf Admin-Seite. |
| [!UICONTROL Log JS Errors to Session Storage] | Global | Wenn diese Option aktiviert ist, kann von Funktionstests für die Berichterstellung verwendet werden. Optionen: `Yes` / `No` |
| [!UICONTROL Log JS Errors to Session Storage Key] | Global | Identifiziert den Schlüssel, der zum Abrufen der erfassten JS-Fehler verwendet wird. |

{style="table-layout:auto"}

## [!UICONTROL CSS Settings]

![CSS-Einstellungen](./assets/developer-css-settings.png)<!-- zoom -->

Weitere Informationen zum Ändern dieser Einstellungen finden Sie unter [Optimieren von Ressourcendateien](../../systems/developer-tools.md#optimizing-resource-files) im _Administratorsystemhandbuch_.

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Merge CSS Files] | Store-Ansicht | Führt mehrere CSS-Dateien in einer Datei zusammen, um die Seitenladezeit zu verbessern. Optionen: `Yes` / `No` |
| [!UICONTROL Minify CSS Files] | Store-Ansicht | Entfernt unnötige Zeichen, Leerzeichen und Einzüge, um die Größe des Codes zu reduzieren. Optionen: `Yes` / `No` |
| [!UICONTROL Use CSS critical path] | Global | Der kritische _CSS-Pfad_ liefert minimierte kritische CSS-Inline-Elemente in `<head>` und verzögert alle nicht kritischen Stile, die asynchron geladen werden. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Image Processing Settings]

![Bildverarbeitungseinstellungen](./assets/developer-image-processing-settings.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Image Adapter] | Global | Gibt den Adapter an, der zum Rendern von Bildern verwendet wird. Nachdem Sie die Adaptereinstellung geändert haben, leeren Sie den Cache für Katalogbilder. Optionen: `PHP GD2` / `ImageMagick` <br/><br/>**_Hinweis:_**Der ICO-Dateityp wird nur vom ImageMagik-Adapter unterstützt. |

{style="table-layout:auto"}

## [!UICONTROL Caching Settings]

![Caching-Einstellungen](./assets/developer-cache-settings.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Cache User Defined Attributes] | Global | Wenn diese Option aktiviert ist, werden benutzerdefinierte Attribute und Attribute des Entitätsattributwerts (EAV) des Systems zwischengespeichert. Diese Option kann die Leistung steigern, erfordert aber auch zusätzlichen Speicherplatz für die Zwischenspeicherung. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Static Files Settings]

![Einstellungen für statische Dateien](./assets/developer-static-files-settings.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Sign Static Files] | Global | Wenn diese Option aktiviert ist, fügt der URL statischer Dateien eine digitale Signatur hinzu, damit Browser erkennen können, wann eine neuere Version der Datei verfügbar ist. Wenn sich die Signatur einer Datei von der im Cache des Browsers gespeicherten Signatur unterscheidet, wird die neuere Version der Datei verwendet. Statische Dateien, die signiert werden können, umfassen JavaScript, CSS, Bilder und Schriftarten. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Grid Settings]

![Rastereinstellungen](./assets/developer-grid-settings.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Asynchronous Indexing|Global] | Bestimmt, wann Entitäten des Auftragsverarbeitungssystems wie Bestellungen, Rechnungen, Sendungen und Kreditkarten zum Raster hinzugefügt und neu indiziert werden. Die asynchrone Indizierung kann verwendet werden, um Datensperren während Speichervorgängen zu vermeiden und die Verarbeitungszeit zu verkürzen. Optionen: <br/>**`Disable`**- (Standard) Auf die Bestellung bezogene Entitäten werden dem Raster zu verschiedenen Zeiten hinzugefügt. gespeichert werden.<br/>**`Enable`** - Auftragsbezogene Entitäten werden dem Raster nur während eines geplanten Cron-Auftrags hinzugefügt. Cron sollte so konfiguriert werden, dass es jede Minute einmal ausgeführt wird. |

{style="table-layout:auto"}
