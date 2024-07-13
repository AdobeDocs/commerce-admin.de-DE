---
title: Suchmaschinenoptimierung
description: Erfahren Sie mehr über Suchmaschinen-Optimierungs-Tools (SEO) für Commerce-Sites und Best Practices für optimale SEO.
exl-id: ba09159a-1b40-4592-8758-f7072dab4589
feature: Merchandising, Products, Search
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 0%

---

# SEO-Übersicht

_Suchmaschinenoptimierung_ (SEO) ist die Vorgehensweise, den Inhalt und die Darstellung einer Site zu optimieren, um die Indexierung der Seiten durch Suchmaschinen zu verbessern. Commerce bietet verschiedene Funktionen, um Ihre laufenden SEO-Bemühungen zu unterstützen.

## Metadaten

Erfahren Sie mehr über das Hinzufügen und Verbessern von schlüsselwortreichen [Metadaten](meta-data.md) für Ihre Site und Ihren Store.

## Verwenden einer Sitemap

Eine [Sitemap](sitemap-xml.md) verbessert die Indexierung Ihres Stores durch Suchmaschinen und dient dazu, Seiten zu finden, die von Webcrawlern übersehen werden. Eine Sitemap kann so konfiguriert werden, dass alle Seiten und Bilder indiziert werden.

## URL-Neuschreibungen

Mit dem Tool [URL Rewrite](url-rewrite.md) können Sie jede URL ändern, die mit einem Produkt, einer Kategorie oder einer CMS-Seite verknüpft ist.

## Suchmaschinen-Roboter

Die Commerce-Konfiguration umfasst Einstellungen zum Generieren und Verwalten von Anweisungen für Webcrawler und Bots, die Ihre Site indizieren. Wenn die Anfrage für `robots.txt` Commerce erreicht (und nicht eine physische Datei), wird sie dynamisch an den Robotercontroller weitergeleitet. Die Anweisungen sind Anweisungen, die von den meisten Suchmaschinen erkannt und befolgt werden.

Standardmäßig enthält die von Commerce generierte Datei robots.txt Anweisungen für Webcrawler, um die Indizierung bestimmter Teile der Site zu vermeiden, die Dateien enthalten, die intern vom System verwendet werden. Sie können die Standardeinstellungen verwenden oder eigene benutzerdefinierte Anweisungen für alle oder für bestimmte Suchmaschinen definieren. Es gibt viele Artikel online, die das Thema im Detail untersuchen.

### Beispiel für benutzerdefinierte Anweisungen

**Ermöglicht vollständigen Zugriff**

    User-agent:*
    disallow:

**Ermöglicht den Zugriff auf alle Ordner**

    User-agent:*
    disallow: /

**Standardanweisungen**

    Benutzeragent: *
    Nicht zulassen: /index.php/
    Nicht zulassen: /*?
    Nicht zulassen: /checkout/
    Nicht zulassen: /app/
    Nicht zulassen: /lib/
    Nicht zulassen: /*.php$
    Nicht zulassen: /pkginfo/
    Nicht zulassen: /report/
    Nicht zulassen: /var/
    Nicht zulassen: /catalog/
    Nicht zulassen: /customer/
    Nicht zulassen/
    Nicht zulassen: /review/
    Nicht zulassen: /*SID=

### Konfigurieren von `robots.txt`

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Suchen Sie die Konfiguration **[!UICONTROL Global]** in der ersten Zeile des Rasters und klicken Sie auf **[!UICONTROL Edit]**.

   ![Globale Designkonfiguration](./assets/design-configuration-grid.png){width="700" zoomable="yes"}

1. Scrollen Sie nach unten und erweitern Sie den Abschnitt **[!UICONTROL Search Engine Robots]** um den ![Erweiterungsselektor](../assets/icon-display-expand.png) und gehen Sie folgendermaßen vor:

   ![Designkonfiguration - Suchmaschinen-Roboter](./assets/design-configuration-search-engine-robots.png){width="600" zoomable="yes"}

   - Setzen Sie **[!UICONTROL Default Robots]** auf einen der folgenden Werte:

     | Option | Beschreibung |
     |------|------------|
     | `INDEX, FOLLOW` | Weist Webcrawler an, die Site zu indizieren und später auf Änderungen zu überprüfen. |
     | `NOINDEX, FOLLOW` | Weist Webcrawler an, die Indizierung der Site zu vermeiden, aber später auf Änderungen zurückzugreifen. |
     | `INDEX, NOFOLLOW` | Weist Webcrawler an, die Site einmalig zu indizieren, aber später nicht auf Änderungen zu überprüfen. |
     | `NOINDEX, NOFOLLOW` | Weist Webcrawler an, die Indizierung der Site zu vermeiden und später nicht auf Änderungen zu überprüfen. |

     {style="table-layout:auto"}

   - Geben Sie bei Bedarf benutzerdefinierte Anweisungen in das Feld **[!UICONTROL Edit Custom instruction of robots.txt file]** ein. Während sich beispielsweise eine Site in der Entwicklung befindet, sollten Sie den Zugriff auf alle Ordner untersagen.

   - Um die Standardanweisungen wiederherzustellen, klicken Sie auf **[!UICONTROL Reset to Default]**.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Configuration]**.
