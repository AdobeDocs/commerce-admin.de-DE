---
title: URL-Neuschreibungen
description: Erfahren Sie mehr über URL-Neuschreibungen und die Verwendung des Commerce URL-Umschreibungs-Tools, um URLs zu ändern, die mit einem Produkt, einer Kategorie oder einer CMS-Seite verknüpft sind.
exl-id: 91e65f7f-7e33-4da5-b0a1-538ace56328a
feature: Categories, Products, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '635'
ht-degree: 0%

---

# URL-Neuschreibungen

Mit dem URL-Umschreibungstool können Sie jede URL ändern, die mit einem Produkt, einer Kategorie oder einer CMS-Seite verknüpft ist. Wenn das Neuschreiben in Kraft tritt, werden alle Links, die auf die vorherige URL verweisen, an die neue Adresse weitergeleitet.

>[!NOTE]
>
>Informationen zum gleichzeitigen Aktualisieren von URL-Neuschreibungen für mehrere oder alle Produkte finden Sie unter [Mehrere URL-Neuschreibungen](url-rewrite-product.md#multiple-url-rewrites).

Die Begriffe _rewrite_ und _redirect_ werden häufig synonym verwendet, beziehen sich jedoch auf etwas unterschiedliche Prozesse. Eine URL ändert die Art und Weise, wie eine URL im Browser angezeigt wird. Eine URL-Umleitung aktualisiert die auf dem Server gespeicherte URL. Eine URL-Umleitung kann entweder temporär oder dauerhaft sein. Ihr Store verwendet URL-Umschreibungen und -Umleitungen, um Ihnen das Ändern des URL-Schlüssels eines Produkts, einer Kategorie oder einer Seite zu erleichtern und vorhandene Links beizubehalten.

Standardmäßig sind [automatische URL-Umleitungen](url-redirect-product-automatic.md) für Ihren Store aktiviert und das Kontrollkästchen **Dauerhafte Umleitung für alte URL erstellen** ist unter dem Feld URL-Schlüssel für jedes Produkt aktiviert.

{{url-rewrite-skip}}

{{url-rewrite-params}}

![Suchmaschinenoptimierung - Erstellen einer dauerhaften URL-Umleitung](./assets/product-search-engine-optimization-create-permanent-redirect.png){width="600" zoomable="yes"}

## Kanonische URLs

Für SEO-Zwecke ist eine gute Idee, dass jede Ihrer Webseiten nur eine eigene URL hat.

Wenn Sie über eine einzelne Seite, auf die mehrere URLs oder verschiedene Seiten mit ähnlichem Inhalt zugreifen können, sieht Google diese als doppelte Versionen derselben Seite. Google wählt eine URL als kanonische Version aus und durchsucht diese. Alle anderen URLs werden als doppelte URLs betrachtet und werden seltener durchsucht.

Wenn Sie Google nicht explizit angeben, welche URL kanonisch ist, wird Ihnen die Wahl getroffen oder Sie können beide gleich gewichten. Dies könnte zu unerwünschtem Verhalten führen und birgt das Risiko eines ineffizienten Crawl-Budgets und geringer verteilter Backlinks.

Je nachdem, wie Sie Ihre Website einrichten, kann der Index mehrere Versionen Ihrer Site enthalten, darunter:

    https://www.example.com
    https://www.example.com/
    http://www.example.com
    https://example.com
    https://www.example.com/index.html

Informationen zum Angeben einer kanonischen Seite finden Sie in der [Dokumentation zu Google Search Central](https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls) .

## Konfigurieren von URL-Neuschreibungen

Die Aktivierung von Webserver-Apache-Neuschreibungen ist Teil des ersten Commerce-Setups. Commerce verwendet URL-Neuschreibungen routinemäßig, um den Dateinamen &quot;`index.php`&quot;zu entfernen, der normalerweise in der URL direkt nach dem Stammordner angezeigt wird. Wenn Webserver-Neuschreibungen aktiviert sind, schreibt das System jede URL neu, sodass `index.php` weggelassen wird. Durch das Umschreiben werden Wörter entfernt, die Suchmaschinen oder Kunden keinen Wert vermitteln und keine Auswirkungen auf die Leistung oder den Site-Rang haben.

URL ohne Neuschreiben des Webservers

    http://www.yourdomain.com/magento/index.php/storeview/url-identifier

URL mit Neuschreiben des Webservers

    http://www.yourdomain.com/magento/storeview/url-identifier

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wählen Sie im linken Bereich, in dem **[!UICONTROL General]** erweitert ist, **[!UICONTROL Web]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Search Engine Optimization]** .

   ![Allgemeine Konfiguration - Optimierung der Web-Suchmaschine](../configuration-reference/general/assets/web-search-engine-optimization.png){width="600" zoomable="yes"}

1. Legen Sie **[!UICONTROL Use Web Server Rewrites]** auf Ihre Voreinstellung fest.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

## Erstellen von URL-Neuschreibungen

Sie können das Tool zum Umschreiben von URLs verwenden, um Produkt- und Kategorieüberarbeitungen sowie benutzerdefinierte Neuschreibungen für jede Seite in Ihrem Store zu erstellen. Wenn das Neuschreiben in Kraft tritt, werden alle vorhandenen Links, die auf die vorherige URL verweisen, nahtlos an die neue Adresse weitergeleitet.

URL-Neuschreibungen können verwendet werden, um hochwertige Suchbegriffe hinzuzufügen, um die Indexierung des Produkts durch Suchmaschinen zu verbessern. Sie können auch Neuschreibungen verwenden, um zusätzliche URLs für eine vorübergehende saisonale Änderung oder dauerhafte Änderung zu erstellen. Umschreibungen können für jeden gültigen Pfad erstellt werden, einschließlich CMS-Inhaltsseiten. Intern referenziert das System immer Produkte und Kategorien anhand ihrer Kennung. Unabhängig davon, wie oft sich die URL ändert, bleibt die ID gleich. Im Folgenden finden Sie einige Möglichkeiten, eine URL-Umschreibung zu verwenden:

System-URL

    http://www.example.com/catalog/category/id/6

Ursprüngliche URL

    http://www.example.com/peripherals/keyboard.html

Umgeleitete Produkt-URL

    http://www.example.com/ergonomic-keyboard.html

Zusätzliche Kategorie-URLs

    http://www.example.com/all-on-sale.html
    http://www.example.com/save-now/spring-sale

![URL schreibt Raster neu](./assets/url-rewrites.png){width="700" zoomable="yes"}

Commerce bietet die folgenden URL-Neuschreibungstypen:

* [Produktneuschreibungen](url-rewrite-product.md)
* [Kategorieumschreibungen](url-rewrite-category.md)
* [CMS-Seitenumbrüche](url-rewrite-cms-page.md)
* [Benutzerdefinierte Neuschreibungen](url-rewrite-custom.md)

## URL schreibt Demo neu

In diesem Video erfahren Sie mehr über die Verwaltung von URL-Neuschreibungen:

>[!VIDEO](https://video.tv.adobe.com/v/343751?quality=12&learn=on)
