---
title: Markup-Tags
description: Erfahren Sie mehr über Markup-Tags, die Code-Ausschnitte enthalten, um auf ein Objekt in Ihrem Store zu verweisen.
exl-id: 0d6f5a9b-983d-473e-b641-0dceba40974f
feature: Page Content, Communications, Variables
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '1000'
ht-degree: 0%

---

# Markup-Tags

Ein Markup-Tag ist eine Direktive, die einen Code-Ausschnitt mit einem relativen Verweis auf ein Objekt in Ihrem Store enthält, z. B. eine Variable, URL, ein Bild oder einen Block. Markup-Tags können überall dort verwendet werden, wo der Editor verfügbar ist, und in die HTML der [E](email-templates.md)- und [Newsletter](../merchandising-promotions/newsletter-template.md)-Vorlagen sowie anderer Arten von [Inhalten](../content-design/introduction.md#content) integriert werden.

Markup-Tags sind in doppelte, geschweifte Klammern eingeschlossen und können entweder vom Widget-Tool generiert oder direkt in HTML-Inhalte eingegeben werden. Anstatt beispielsweise den vollständigen Pfad zu einer Seite hartcodiert zu haben, können Sie ein Markup-Tag verwenden, um die Store-URL darzustellen. Die in den folgenden Beispielen aufgeführten Markup-Tags umfassen:

{{$include /help/_includes/directives-caution.md}}

## Benutzerdefinierte Variable

Mit dem Variablen-Markup-Tag können Sie eine [benutzerdefinierte Variable](variables-custom.md) in eine E-Mail-Vorlage, Blöcke, Newsletter und Inhaltsseiten einfügen.

\{\{CustomVar code= „my_custom_variable“}}

## URL speichern

Das Markup-Tag für die Store-URL stellt die Basis-URL Ihrer Website dar und wird als Ersatz für den ersten Teil einer vollständigen URL verwendet, einschließlich des Domain-Namens. Es gibt zwei Versionen dieses Markup-Tags: eine, die direkt zu Ihrem Store geht, und die andere mit einem Schrägstrich (`/`) am Ende, der verwendet wird, wenn ein Pfad hinzugefügt wird.

\{\{store url=&#39;bekleidung/schuhe/frauen&#39;}}

## Medien-URL

Das Dynamic Media URL-Markup-Tag stellt den Speicherort und den Dateinamen eines Bildes dar, das in einem Content Delivery Network (CDN) gespeichert ist. Das Tag kann verwendet werden, um ein Bild auf einer Seite, einem Block, einem Banner oder einer E-Mail-Vorlage zu platzieren.

\{\{media url=&#39;shose-sale.jpg&#39;}}

## Block-ID

Das Markup-Tag für die Block-ID ist eines der am einfachsten zu verwendenden und kann verwendet werden, um einen Block direkt auf einer CMS-Seite zu platzieren oder sogar in einem anderen Block zu verschachteln. Mit dieser Methode können Sie einen Block für verschiedene Promotions oder Sprachen ändern. Das Markup-Tag Block-ID verweist auf einen Block anhand seiner Kennung.

\{\{block id=&#39;block-id&#39;}}

## Vorlagen-Tag

Ein Vorlagen-Tag verweist auf eine PHTML-Vorlagendatei und kann verwendet werden, um den Block auf einer CMS-Seite oder in einem statischen Block anzuzeigen. Der Code im folgenden Beispiel kann zu einer Seite oder einem Block hinzugefügt werden, um das Formular „Kontakt“ anzuzeigen.

\{\{block class=&quot;Magento\Contact\Block\ContactForm&quot; name=„contactForm“ template=&quot;Magento_Contact::form.phtml“}}

Der Code im nächsten Beispiel kann zu einer Seite oder einem Block hinzugefügt werden, um eine Liste von Produkten in einer bestimmten Kategorie nach Kategorie-ID anzuzeigen.

\{\{block type=„catalog/product_list“ category_id=„22“ template=&quot;catalog/product/list.phtml&quot;}}

## Widget-Code

Das Widget-Tool kann verwendet werden, um Produktlisten anzuzeigen oder komplexe Links einzufügen, z. B. einen Link, der basierend auf der Produkt-ID zu einer bestimmten Produktseite wechselt. Der generierte Code umfasst die Blockreferenz, den Speicherort des Code-Moduls und die entsprechende PHTML-Vorlage. Nachdem der Code generiert wurde, können Sie ihn von einer Stelle an eine andere kopieren und einfügen.

Der Code im folgenden Beispiel kann zu einer Seite oder einem Block hinzugefügt werden, um die Liste der neuen Produkte anzuzeigen.

\{\{widget type=„catalog/product_widget_new“ display_type=„new_products“ products_count=„10“ template=&quot;catalog/product/widget/new/content/new_grid.phtml&quot;}}

Der Code im nächsten Beispiel kann zu einer Seite oder einem Block hinzugefügt werden, um einen Link zu einem bestimmten Produkt anhand der Produkt-ID anzuzeigen.

\{\{widget type=„catalog/product_widget_link“ anchor_text=„Mein Produkt-Link“ title=„Mein Produkt-Link“ template=&quot;catalog/product/widgetlink/link_block.phtml&quot; id_path=„product/31“}}

## Verwenden von Markup-Tags in Links

Sie können Markup-Tags mit HTML-Anker-Tags verwenden und direkt eine Verknüpfung zu einer beliebigen Seite in Ihrem Store herstellen. Der Link kann in Inhaltsseiten, Blöcke oder E-Mail- und Newsletter-Vorlagen integriert werden. Sie können diese Technik auch verwenden, um ein Bild mit einer bestimmten Seite zu verknüpfen.

### Schritt 1. Identifizieren der Ziel-URL

Navigieren Sie nach Möglichkeit zu der Seite, auf die Sie eine Verknüpfung herstellen möchten, und kopieren Sie die vollständige URL aus der Adressleiste Ihres Browsers. Der Teil der URL, den Sie benötigen, folgt nach dem `.com/`. Kopieren Sie andernfalls den URL-Schlüssel von der CMS-Seite, die Sie als Link-Ziel verwenden möchten.

#### Vollständige URL zur Kategorieseite

`https://mystore.com/apparel/shoes/womens`
`https://mystore.com/apparel/shoes/womens.html`

#### Vollständige URL zur Produktseite

`https://mystore.com/apparel/shoes/womens/nine-west-pump`
`https://mystore.com/apparel/shoes/womens/nine-west-pump.html`

#### Vollständige URL zur CMS-Seite

`https://mystore.com/about-us`

### Schritt 2. Hinzufügen des Markups zur URL

Das Store-URL-Tag stellt die Basis-URL Ihrer Website dar und wird als Ersatz für den HTTP-Adressteil der Store-URL verwendet, einschließlich Domain-Name und `.com`. Es gibt zwei Versionen des Tags, die Sie je nach den gewünschten Ergebnissen verwenden können.

`store direct_url` - Direkter Link zu einer Seite.

`store url` - Platziert einen Schrägstrich am Ende, sodass zusätzliche Verweise als Pfad angehängt werden können.

In den folgenden Beispielen wird der URL-Schlüssel in einfache Anführungszeichen und das gesamte Markup-Tag in doppelte geschweifte Klammern eingeschlossen. Bei Verwendung mit einem Anker-Tag wird das Markup-Tag in doppelte Anführungszeichen des Ankers gesetzt. Um Verwirrung zu vermeiden, können Sie für jeden verschachtelten Satz von Anführungszeichen abwechselnd einfache und doppelte Anführungszeichen verwenden.

Wenn Sie mit einer vollständigen URL beginnen, löschen Sie den HTTP-Adressbereich (`http://` oder `https://`) der URL, bis einschließlich `.com/`. Geben Sie an seiner Stelle das Markup-Tag für die Store-URL ein, bis durch das öffnende einfache Anführungszeichen.

#### URL-Markup-Tag speichern

`https://mystore.com/apparel/shoes/womens`

`{{store url='apparel/shoes/womens'}}`

Geben Sie andernfalls den ersten Teil des Store-URL-Markup-Tags ein und fügen Sie den zuvor kopierten URL-Schlüssel oder -Pfad ein.

### URL-Markup-Tag mit URL-Schlüssel speichern

`{{store url=`

Um das Markup-Tag abzuschließen, geben Sie die schließenden doppelten Anführungszeichen und doppelten Klammern ein.

`{{store url='apparel/shoes/womens'}}`

### Schritt 3. Vervollständigen Sie das Anker-Tag

Betten Sie das fertige Markup-Tag in ein Anker-Tag ein, indem Sie das Markup-Tag anstelle der Ziel-URL verwenden. Fügen Sie dann den Link-Text und das schließende Anker-Tag hinzu.

#### Markup im Anker-Tag

\&lt;a href=&quot;\{\{Markup-Tag geht hier}}&quot;>Link-Text\&lt;/a>

Fügen Sie das fertige Anker-Tag in den Code einer CMS-Seite, eines -Blocks, eines -Banners oder einer E-Mail-Vorlage ein, in der bzw. dem der Link angezeigt werden soll.

### Vollständiger Link mit Markup

\&lt;a href=&quot;\{\{store url=&#39;bekleidung/Schuhe&#39;}}&quot;>Schuhverkauf\&lt;/a>

<!-- Last updated from includes: 2022-08-30 15:36:09 -->
