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

_Suchmaschinenoptimierung_ (SEO) ist die Praxis der Feinabstimmung des Inhalts und der Präsentation einer Website, um die Art und Weise zu verbessern, wie die Seiten von Suchmaschinen indiziert werden. Der Handel umfasst verschiedene Funktionen, die Ihre laufenden SEO-Bemühungen unterstützen.

## Metadaten

Erfahren Sie mehr über das Hinzufügen und Verbessern von schlüsselwortreichen Inhalten [Metadaten](meta-data.md) für Ihre Site und Ihr Geschäft.

## Verwenden einer Sitemap

A [Sitemap](sitemap-xml.md) verbessert die Indexierung Ihres Stores durch Suchmaschinen und ist so konzipiert, dass Seiten gefunden werden, die von Webcrawlern möglicherweise übersehen werden. Eine Sitemap kann so konfiguriert werden, dass alle Seiten und Bilder indiziert werden.

## URL-Neuschreibungen

Die [URL-Neufassung](url-rewrite.md) können Sie jede URL ändern, die mit einem Produkt, einer Kategorie oder einer CMS-Seite verknüpft ist.

## Suchmaschinen-Roboter

Die Commerce-Konfiguration enthält Einstellungen zum Generieren und Verwalten von Anweisungen für Webcrawler und Bots, die Ihre Site indizieren. Wenn die Anforderung für `robots.txt` Commerce erreicht (statt einer physischen Datei), wird sie dynamisch zum Robotercontroller weitergeleitet. Die Anweisungen sind Anweisungen, die von den meisten Suchmaschinen erkannt und befolgt werden.

Standardmäßig enthält die von Commerce generierte Datei robots.txt Anweisungen für Webcrawler, um die Indizierung bestimmter Teile der Site zu vermeiden, die Dateien enthalten, die intern vom System verwendet werden. Sie können die Standardeinstellungen verwenden oder eigene benutzerdefinierte Anweisungen für alle oder für bestimmte Suchmaschinen definieren. Es gibt viele Artikel online, die das Thema im Detail untersuchen.

### Beispiel für benutzerdefinierte Anweisungen

**Ermöglicht uneingeschränkten Zugriff**

    User-agent:*
    Nicht zulassen:

**Ermöglicht Zugriff auf alle Ordner**

    User-agent:*
    Nicht zulassen: /

**Standardanweisungen**

    User-agent: *
    Disallow: /index.php/
    Nicht zulassen: /*?
    Disallow: /checkout/
    Disallow: /app/
    Disallow: /lib/
    Nicht zulassen: /*.php$
    Nicht zulassen: /pkginfo/
    Nicht zulassen: /report/
    Nicht zulassen: /var/
    Nicht zulassen: /catalog/
    Disallow: /customer/
    Disallow: /sendfriend/
    Nicht zulassen: /review/
    Nicht zulassen: /*SID=

### Konfigurieren `robots.txt`

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Suchen Sie die **[!UICONTROL Global]** Konfiguration in der ersten Zeile des Rasters und klicken Sie auf **[!UICONTROL Edit]**.

   ![Globale Designkonfiguration](./assets/design-configuration-grid.png){width="700" zoomable="yes"}

1. Hinunter scrollen und erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Search Engine Robots]** und führen Sie folgende Schritte aus:

   ![Designkonfiguration - Suchmaschinen-Roboter](./assets/design-configuration-search-engine-robots.png){width="600" zoomable="yes"}

   - Satz **[!UICONTROL Default Robots]** auf einen der folgenden Werte zu:

     | Option | Beschreibung |
     |------|------------|
     | `INDEX, FOLLOW` | Weist Webcrawler an, die Site zu indizieren und später auf Änderungen zu überprüfen. |
     | `NOINDEX, FOLLOW` | Weist Webcrawler an, die Indizierung der Site zu vermeiden, aber später auf Änderungen zurückzugreifen. |
     | `INDEX, NOFOLLOW` | Weist Webcrawler an, die Site einmalig zu indizieren, aber später nicht auf Änderungen zu überprüfen. |
     | `NOINDEX, NOFOLLOW` | Weist Webcrawler an, die Indizierung der Site zu vermeiden und später nicht auf Änderungen zu überprüfen. |

     {style="table-layout:auto"}

   - Geben Sie bei Bedarf benutzerdefinierte Anweisungen in das **[!UICONTROL Edit Custom instruction of robots.txt file]** ankreuzen. Während sich beispielsweise eine Site in der Entwicklung befindet, sollten Sie den Zugriff auf alle Ordner untersagen.

   - Um die Standardanweisungen wiederherzustellen, klicken Sie auf **[!UICONTROL Reset to Default]**.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Configuration]**.
