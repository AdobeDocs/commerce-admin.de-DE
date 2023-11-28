---
title: Markup-Tags
description: Erfahren Sie mehr über Markup-Tags, die Codefragmente enthalten, um auf ein Objekt in Ihrem Store zu verweisen.
exl-id: 0d6f5a9b-983d-473e-b641-0dceba40974f
feature: Page Content, Communications, Variables
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '1010'
ht-degree: 0%

---

# Markup-Tags

Ein Markup-Tag ist eine Direktive, die einen Codeausschnitt mit einem relativen Verweis auf ein Objekt in Ihrem Store enthält, z. B. eine Variable, eine URL, ein Bild oder einen Block. Markup-Tags können überall dort verwendet werden, wo der Editor verfügbar und in die HTML von [email](email-templates.md) und [Newsletter](../merchandising-promotions/newsletter-template.md) Vorlagen sowie andere Typen von [content](../content-design/introduction.md#content).

Markup-Tags sind in doppelte, geschweifte Klammern eingeschlossen und können entweder vom Widget-Tool generiert oder direkt in HTML-Inhalte eingegeben werden. Anstatt beispielsweise den vollständigen Pfad zu einer Seite fest zu kodieren, können Sie ein Markup-Tag verwenden, um die Store-URL darzustellen. Die Markup-Tags in den folgenden Beispielen umfassen:

{{$include /help/_includes/directives-caution.md}}

## Benutzerdefinierte Variable

Mit dem Variablen-Markup-Tag können Sie eine [benutzerdefinierte Variable](variables-custom.md) in eine E-Mail-Vorlage, Bausteine, Newsletter und Inhaltsseiten.

\{CustomVar code= &quot;my_custom_variable&quot;}

## Store-URL

Das Markup-Tag Store-URL stellt die Basis-URL Ihrer Website dar und wird als Ersatz für den ersten Teil einer vollständigen URL verwendet, einschließlich des Domänennamens. Es gibt zwei Versionen dieses Markup-Tags: eine, die direkt zu Ihrem Store gehört, und die andere mit einem Schrägstrich (`/`) am Ende, das beim Hinzufügen eines Pfads verwendet wird.

\{\{store url=&#39;apparel/shoes/womens&#39;}

## Medien-URL

Das Markup-Tag für dynamische Medien-URLs stellt den Speicherort und den Dateinamen eines Bildes dar, das in einem Inhaltsbereitstellungsnetzwerk (Content Delivery Network, CDN) gespeichert ist. Mit dem -Tag können Sie ein Bild auf einer Seite, einem Block, einem Banner oder einer E-Mail-Vorlage platzieren.

\{\{media url=&#39;shoe-sale.jpg&#39;}

## Block-ID

Das Block-ID-Markup-Tag ist am einfachsten zu verwenden und kann verwendet werden, um einen Block direkt auf einer CMS-Seite zu platzieren oder ihn sogar in einem anderen Block zu verschachteln. Mit dieser Technik können Sie einen Block für verschiedene Promotions oder Sprachen ändern. Das Markup-Tag &quot;Block-ID&quot;referenziert einen Block anhand seiner Kennung.

\{\{block id=&#39;block-id&#39;}

## Vorlagentag

Ein Vorlagen-Tag verweist auf eine PHTML-Vorlagendatei und kann verwendet werden, um den Block auf einer CMS-Seite oder in einem statischen Block anzuzeigen. Der Code im folgenden Beispiel kann zu einer Seite oder einem Block hinzugefügt werden, um das Kontaktformular anzuzeigen.

\{\{block class=&quot;Magento\Contact\Block\ContactForm&quot; name=&quot;contactForm&quot; template=&quot;Magento_Contact::form.phtml&quot;}}

Der Code im nächsten Beispiel kann zu einer Seite oder einem Block hinzugefügt werden, um eine Liste der Produkte einer bestimmten Kategorie nach Kategorie-ID anzuzeigen.

\{block type=&quot;catalog/product_list&quot; category_id=&quot;22&quot; template=&quot;catalog/product/list.phtml&quot;}

## Widget-Code

Das Widget-Tool kann verwendet werden, um Listen von Produkten anzuzeigen oder komplexe Links einzufügen, z. B. Links, die basierend auf der Produkt-ID zu einer bestimmten Produktseite führen. Der generierte Code enthält die Blockreferenz, den Speicherort des Codemoduls und die entsprechende PHTML-Vorlage. Nachdem der Code generiert wurde, können Sie ihn kopieren und an einer anderen Stelle einfügen.

Der Code im folgenden Beispiel kann zu einer Seite oder einem Block hinzugefügt werden, um die Liste der neuen Produkte anzuzeigen.

\{widget type=&quot;catalog/product_widget_new&quot; display_type=&quot;new_products&quot; products_count=&quot;10&quot; template=&quot;catalog/product/widget/new/content/new_grid.phtml&quot;}

Der Code im nächsten Beispiel kann zu einer Seite oder einem Block hinzugefügt werden, um einen Link zu einem bestimmten Produkt nach Produkt-ID anzuzeigen.

\{\{widget type=&quot;catalog/product_widget_link&quot; anchor_text=&quot;My Product Link&quot; title=&quot;My Product Link&quot; template=&quot;catalog/product/widgetlink/link_block.phtml&quot; id_path=&quot;product/31&quot;}

## Markup-Tags in Links verwenden

Sie können Markup-Tags mit HTML-Anker-Tags verwenden und direkt eine Verknüpfung zu einer beliebigen Seite in Ihrem Store herstellen. Der Link kann in Inhaltsseiten, Bausteine oder E-Mail- und Newsletter-Vorlagen integriert werden. Sie können diese Methode auch verwenden, um ein Bild mit einer bestimmten Seite zu verknüpfen.

### Schritt 1. Ziel-URL identifizieren

Navigieren Sie nach Möglichkeit zu der Seite, mit der Sie einen Link verknüpfen möchten, und kopieren Sie die vollständige URL aus der Adressleiste Ihres Browsers. Der benötigte Teil der URL folgt dem `.com/`. Kopieren Sie andernfalls den URL-Schlüssel von der CMS-Seite, die Sie als Link-Ziel verwenden möchten.

#### Vollständige URL zur Kategorieseite

`https://mystore.com/apparel/shoes/womens`
`https://mystore.com/apparel/shoes/womens.html`

#### Vollständige URL zur Produktseite

`https://mystore.com/apparel/shoes/womens/nine-west-pump`
`https://mystore.com/apparel/shoes/womens/nine-west-pump.html`

#### Vollständige URL zur CMS-Seite

`https://mystore.com/about-us`

### Schritt 2. Hinzufügen des Markups zur URL

Das Tag Store-URL stellt die Basis-URL Ihrer Website dar und wird als Ersatz für den Teil der HTTP-Adresse der Store-URL verwendet, einschließlich des Domänennamens und `.com`. Es gibt zwei Versionen des Tags, die Sie je nach den gewünschten Ergebnissen verwenden können.

`store direct_url` - Links direkt zu einer Seite.

`store url` - Platziert einen Schrägstrich am Ende, sodass zusätzliche Verweise als Pfad angehängt werden können.

In den folgenden Beispielen ist der URL-Schlüssel in einfache Anführungszeichen gesetzt und das gesamte Markup-Tag ist in zwei geschweifte Klammern eingeschlossen. Bei Verwendung mit einem Anker-Tag wird das Markup-Tag in die doppelten Anführungszeichen des Anchers gesetzt. Um Verwirrung zu vermeiden, können Sie für jeden verschachtelten Satz von Anführungszeichen einfache und doppelte Anführungszeichen verwenden.

Wenn Sie mit einer vollständigen URL beginnen, löschen Sie die HTTP-Adresse (`http://` oder `https://`) Teil der URL, bis hin zu und einschließlich der `.com/`. Geben Sie an seiner Stelle das Markup-Tag Store-URL ein, und zwar durch das öffnende einfache Anführungszeichen.

#### Store-URL-Markup-Tag

`https://mystore.com/apparel/shoes/womens`

`{{store url='apparel/shoes/womens'}}`

Geben Sie andernfalls den ersten Teil des Markup-Tags Store URL ein und fügen Sie den URL-Schlüssel oder Pfad ein, den Sie zuvor kopiert haben.

### URL-Markup-Tag mit URL-Schlüssel speichern

`{{store url=`

Um das Markup-Tag abzuschließen, geben Sie die schließenden doppelten Anführungszeichen und doppelten Klammern ein.

`{{store url='apparel/shoes/womens'}}`

### Schritt 3. Anker-Tag ausfüllen

Schließen Sie das abgeschlossene Markup-Tag in ein Anker-Tag ein, indem Sie das Markup-Tag anstelle der Ziel-URL verwenden. Fügen Sie dann den Link-Text und das schließende Anker-Tag hinzu.

#### Markup im Anker-Tag

\&lt;a href=&quot;\{\{markup tag goes here}}&quot;>Link Text\&lt;/a>

Fügen Sie das abgeschlossene Anker-Tag in den Code einer beliebigen CMS-Seite, eines Blocks, Banners oder einer E-Mail-Vorlage ein, in der der Link angezeigt werden soll.

### Vollständiger Link mit Markup

\&lt;a href=&quot;\{\{store url=&amp;#39;apparel/shoes&amp;#39;}}&quot;>Shoe Sale\&lt;/a>
