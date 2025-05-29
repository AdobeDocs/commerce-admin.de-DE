---
title: URL-Neuschreibungen
description: Erfahren Sie mehr über URL-Neuschreibungen und die Verwendung des Commerce URL Rewrite Tools zum Ändern von URLs, die mit einem Produkt, einer Kategorie oder einer CMS-Seite verknüpft sind.
exl-id: 91e65f7f-7e33-4da5-b0a1-538ace56328a
feature: Categories, Products, Configuration
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/de/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
source-git-commit: 7e28081ef2723d4113b957edede6a8e13612ad2f
workflow-type: tm+mt
source-wordcount: '669'
ht-degree: 0%

---

# URL-Neuschreibungen

>[!TIP]
>
>Informationen zu Adobe Commerce as a Cloud Service finden Sie in den [SEO-Richtlinien](https://experienceleague.adobe.com/developer/commerce/storefront/setup/seo/indexing/?lang=de) in der Dokumentation zu Commerce Storefront

Mit dem URL-Rewrite-Tool können Sie jede URL ändern, die mit einem Produkt, einer Kategorie oder einer CMS-Seite verknüpft ist. Wenn die Umschreibung wirksam wird, werden alle Links, die auf die vorherige URL verweisen, an die neue Adresse umgeleitet.

>[!NOTE]
>
>Informationen zum Aktualisieren von URL-Neuschreibungen für mehrere oder alle Produkte gleichzeitig finden Sie unter [Mehrere URL-Neuschreibungen](url-rewrite-product.md#multiple-url-rewrites).

Die Begriffe _umschreiben_ und _umleiten_ werden oft synonym verwendet, beziehen sich aber auf leicht unterschiedliche Prozesse. Eine URL-Umschreibung ändert die Darstellung einer URL im Browser. Eine URL-Umleitung aktualisiert die auf dem Server gespeicherte URL. Eine URL-Umleitung kann temporär oder dauerhaft sein. Ihr Store verwendet URL-Neuschreibungen und -Weiterleitungen, um Ihnen das Ändern des URL-Schlüssels eines Produkts, einer Kategorie oder einer Seite und das Beibehalten vorhandener Links zu erleichtern.

Standardmäßig sind [automatische URL-Umleitungen](url-redirect-product-automatic.md) für Ihren Store aktiviert und das Kontrollkästchen **Ständige Umleitung für alte URL erstellen** unter dem URL-Schlüsselfeld jedes Produkts ist aktiviert.

{{url-rewrite-skip}}

{{url-rewrite-params}}

![Suchmaschinenoptimierung - Erstellen einer permanenten URL-Umleitung](./assets/product-search-engine-optimization-create-permanent-redirect.png){width="600" zoomable="yes"}

## Kanonische URLs

Für SEO-Zwecke ist es eine gute Idee, dass jede Ihrer Web-Seiten nur eine, unterschiedliche URL hat.

Wenn Sie über eine einzelne Seite verfügen, auf die über mehrere URLs zugegriffen werden kann, oder über verschiedene Seiten mit ähnlichem Inhalt, werden diese von Google als doppelte Versionen derselben Seite angezeigt. Google wählt eine URL als die kanonische Version und durchsucht diese. Alle anderen URLs werden als doppelte URLs betrachtet und seltener durchsucht.

Wenn Sie Google nicht explizit mitteilen, welche URL kanonisch ist, trifft es die Entscheidung für Sie, oder beide werden als gleich wichtig erachtet. Dies kann zu unerwünschtem Verhalten führen und birgt das Risiko eines ineffektiven Durchforstungsbudgets und geringer verteilter Backlinks.

Je nachdem, wie Sie Ihre Website einrichten, kann der Index mehrere Versionen Ihrer Website enthalten, darunter:

    https://www.example.com
    https://www.example.com/
    http://www.example.com
    https://example.com
    https://www.example.com/index.html

Informationen zum Angeben einer kanonischen Seite finden Sie in der [Dokumentation zu Google Search Central](https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls).

## Konfigurieren von URL-Neuschreibungen

Die Aktivierung von Apache-Neuschreibungen auf Webservern ist Teil der ersten Commerce-Einrichtung. Commerce verwendet routinemäßig URL-Neuschreibungen, um die `index.php` zu entfernen, die normalerweise in der URL direkt nach dem Stammordner angezeigt werden. Wenn Webserver-Neuschreibungen aktiviert sind, schreibt das System jede URL neu, um `index.php` wegzulassen. Die Neufassung entfernt Wörter, die Suchmaschinen oder Kunden keinen Wert vermitteln, und hat keine Auswirkungen auf die Leistung oder den Site-Rang.

URL ohne Webserver-Umschreibung

    http://www.yourdomain.com/magento/index.php/storeview/url-identifier

URL mit Webserver-Umschreibung

    http://www.yourdomain.com/magento/storeview/url-identifier

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wählen Sie im linken Bedienfeld, in dem **[!UICONTROL General]** erweitert ist, **[!UICONTROL Web]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Search Engine Optimization]** .

   ![Allgemeine Konfiguration - Web-Suchmaschinenoptimierung](../configuration-reference/general/assets/web-search-engine-optimization.png){width="600" zoomable="yes"}

1. Legen Sie **[!UICONTROL Use Web Server Rewrites]** auf Ihre Voreinstellung fest.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

## URL-Neuschreibungen erstellen

Sie können das URL Rewrite-Tool verwenden, um Produkt- und Kategorieüberschreibungen sowie benutzerdefinierte Überschreibungen für jede Seite in Ihrem Store zu erstellen. Wenn die Umschreibung in Kraft tritt, werden alle vorhandenen Links, die auf die vorherige URL verweisen, nahtlos an die neue Adresse umgeleitet.

URL-Neuschreibungen können verwendet werden, um hochwertige Keywords hinzuzufügen, um die Art und Weise zu verbessern, wie das Produkt von Suchmaschinen indiziert wird. Sie können auch Umschreibungen verwenden, um zusätzliche URLs für eine temporäre saisonale oder permanente Änderung zu erstellen. Umschreibungen können für jeden gültigen Pfad erstellt werden, einschließlich CMS-Inhaltsseiten. Intern verweist das System immer auf Produkte und Kategorien anhand ihrer ID. Unabhängig davon, wie oft sich die URL ändert, die ID bleibt gleich. Im Folgenden finden Sie einige Möglichkeiten, eine URL-Umschreibung zu verwenden:

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
* [Neuschreibungen von Kategorien](url-rewrite-category.md)
* [CMS-Seitenumschreibungen](url-rewrite-cms-page.md)
* [Benutzerdefinierte Neuschreibungen](url-rewrite-custom.md)

## Demo-URL-Neuschreibungen

In diesem Video erfahren Sie mehr über die Verwaltung von URL-Neuschreibungen:

>[!VIDEO](https://video.tv.adobe.com/v/3411957?quality=12&learn=on&captions=ger)
