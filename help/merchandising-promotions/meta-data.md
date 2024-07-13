---
title: Metadaten
description: Erfahren Sie, wie Sie schlüsselwortreiche Metadaten eingeben können, um die Indexierung Ihrer Commerce-Site durch Suchmaschinen zu verbessern.
exl-id: 2acc1523-9da6-4e6f-8e4f-607603a61559
feature: Merchandising, Search
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '669'
ht-degree: 0%

---

# Metadaten

Ihr Store ist mit Orten gefüllt, an denen Sie schlüsselwortreiche Metadaten eingeben können, um die Indexierung Ihrer Site durch Suchmaschinen zu verbessern. Beim Einrichten Ihres Stores können Sie vorläufige Metadaten eingeben, um sie später abzuschließen. Im Laufe der Zeit können Sie die Metadaten so anpassen, dass sie auf die Kaufmuster und Präferenzen Ihrer Kunden ausgerichtet sind.

![Produkteinstellungen - Suchmaschinenoptimierung](./assets/product-basic-settings-search-engine-optimization-yoga-strap.png){width="700" zoomable="yes"}

## Metadatentitel

Der Metadatentitel wird in der Titelleiste und auf der Registerkarte Ihres Browsers und in den Suchergebnislisten angezeigt. Der Metadatentitel sollte für die Seite eindeutig sein und weniger als 70 Zeichen lang sein.

![Beispiel-Storefront - Metadatentitel](./assets/storefront-home-page-meta-title.png){width="600"}

## Meta-Schlüsselwörter

Obwohl einige Suchmaschinen Meta-Suchbegriffe ignorieren, werden sie von anderen weiterhin verwendet. Die aktuelle Best Practice besteht darin, hochwertige Suchbegriffe in den Metadatentitel und die Meta-Beschreibung einzubinden.

![Webbrowser-Suche - Meta-Schlüsselwörter](./assets/storefront-meta-description.png){width="500"}

## Meta-Beschreibung

Meta-Beschreibungen bieten einen kurzen Überblick über die Seite für die Liste der Suchergebnisse. Idealerweise sollte eine Meta-Beschreibung zwischen 150 und 160 Zeichen lang sein, obwohl das Feld bis zu 255 Zeichen akzeptiert.

## Rich-Snippets

Rich-Snippets bieten detaillierte Informationen für Suchergebnislisten und andere Anwendungen. Standardmäßig wird ein strukturiertes Daten-Markup, das auf dem [schema.org][1] -Standard basiert, zur Produktvorlage Ihres Stores hinzugefügt. Daher stehen Suchmaschinen weitere Informationen zur Verfügung, die als _Rich-Snippets_ in Produktlisten aufgenommen werden können.

## Kanonisches Meta-Tag

Einige Suchmaschinen bestrafen Websites mit mehreren URLs, die auf denselben Inhalt verweisen. Das kanonische Meta-Tag teilt Suchmaschinen mit, welche Seite indiziert werden soll, wenn mehrere URLs identische oder ähnliche Inhalte haben. Die Verwendung des kanonischen Meta-Tags kann das Ranking Ihrer Site verbessern und die Seitenansichten aggregieren. Das kanonische Meta-Tag wird im Block `<head>` einer Produkt- oder Kategorieseite platziert. Sie enthält einen Link zu Ihrer bevorzugten URL, sodass Suchmaschinen ihr Gewicht erhöhen.

### Beispiel 1: Kategoriepfad erstellt doppelte URLs

Wenn Ihr Katalog beispielsweise so konfiguriert ist, dass er den Kategoriepfad in Produkt-URLs enthält, generiert Ihr Store mehrere URLs, die auf dieselbe Produktseite verweisen.

    http://mystore.com/gear/bags/driven-backpack.html
    http://mystore.com/driven-backpack.html

### Beispiel 2: vollständige URL der Kategorieseite

Wenn kanonische Meta-Tags für Kategorien aktiviert sind, enthält die Kategorieseite Ihres Stores eine kanonische URL zur vollständigen Kategorie-URL:

    http://mystore.com/gear/bags/

### Beispiel 3: Vollständige Produktseite URL

Wenn kanonische Meta-Tags für Produkte aktiviert sind, enthält die Produktseite eine kanonische URL zum Domänennamen/Produkt-URL-Schlüssel, da Produkt-URL-Schlüssel global eindeutig sind.

    http://mystore.com/driven-backpack.html

Wenn Sie auch den Kategoriepfad in Produkt-URLs einbeziehen, bleibt die kanonische URL der Domänenname/Produkt-URL-Schlüssel. Der Zugriff auf das Produkt ist jedoch auch über seine vollständige URL möglich, die auch die Kategorie enthält. Wenn der Produkt-URL-Schlüssel beispielsweise &quot;`driven-backpack`&quot;lautet und der Kategorie &quot;Gear&quot;> &quot;Bags&quot;zugewiesen ist, kann über eine der beiden URL auf das Produkt zugegriffen werden.

Sie können vermeiden, von Suchmaschinen benachteiligt zu werden, indem Sie die Kategorie aus der URL weglassen oder indem Sie das kanonische Meta-Tag verwenden, um Suchmaschinen anzuweisen, entweder nach Produkt oder Kategorie zu indizieren. Als Best Practice wird empfohlen, kanonische Meta-Tags sowohl für Kategorien als auch für Produkte zu aktivieren.

### Canonical-Meta-Tag aktivieren

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bedienfeld den Wert **[!UICONTROL Catalog]** und wählen Sie unter &quot;**[!UICONTROL Catalog]**&quot;.

1. Erweitern Sie den Abschnitt **Suchmaschinenoptimierung** um ![Erweiterungsauswahl](../assets/icon-display-expand.png).

   Um Feldwerte zu ändern, müssen Sie zunächst das Kontrollkästchen **Systemwert verwenden** hinter jedem Feld deaktivieren.

   ![Katalogkonfiguration - Suchmaschinenoptimierung](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

1. Wenn Suchmaschinen nur Kategorieseiten mit dem vollständigen Kategoriepfad indizieren sollen, gehen Sie wie folgt vor:

   - Setzen Sie **Kanonisches Link-Meta-Tag für Kategorien** auf `Yes`.

   - Setzen Sie **Kanonisches Link-Meta-Tag für Produkte verwenden** auf `No`.

1. Wenn Sie möchten, dass Suchmaschinen Produktseiten nur im Format &quot;domain-name/product-url-key&quot;indizieren, gehen Sie wie folgt vor:

   - Setzen Sie **Kanonisches Link-Meta-Tag für Produkte verwenden** auf `Yes`.

   - Setzen Sie **Kanonisches Link-Meta-Tag für Kategorien** auf `No`.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

## Demo zu Metadaten

Sehen Sie sich dieses Video an, um mehr über die Verwaltung von SEO-Metadaten zu erfahren:

>[!VIDEO](https://video.tv.adobe.com/v/343750?quality=12)

[1]: https://schema.org/
