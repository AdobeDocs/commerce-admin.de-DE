---
title: '[!UICONTROL Catalog] &gt; [!UICONTROL Catalog]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Catalog] &gt; [!UICONTROL Catalog] des Commerce Admin-Bereichs.
exl-id: fc25ae80-aaa7-42c4-bba2-f03d3caa7970
feature: Configuration, Catalog Management
source-git-commit: 20f97d6ab391b7f5675d6790ab2ec5d24e9dda21
workflow-type: tm+mt
source-wordcount: '3261'
ht-degree: 0%

---

# [!UICONTROL Catalog] > [!UICONTROL Catalog]

{{config}}

## [!UICONTROL Product Fields Auto-Generation]

![Automatische Generierung von Produktfeldern](./assets/catalog-product-fields-auto-generation.png)<!-- zoom -->

<!-- [Product Fields Auto-Generation](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/products/product-workspace#default-field-values) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Mask for SKU] | Global | Bestimmt den Standardwert des SKU-Felds basierend auf Platzhalterwerten aus anderen Feldern und auf zusätzlichem Text, der eingegeben wird. Standardplatzhalter: <br/>Produktname - `{{name}}` |
| [!UICONTROL Mask for Meta Title] | Global | Bestimmt den Standardwert des Felds Meta-Titel basierend auf Platzhalterwerten aus anderen Feldern und allen zusätzlichen eingegebenen Texten. Standardplatzhalter: <br/>Produktname - `{{name}}` |
| [!UICONTROL Mask for Meta Keywords] | Global | Bestimmt den Standardwert des Felds _Meta-Keywords_ basierend auf Platzhalterwerten aus anderen Feldern und allen zusätzlichen eingegebenen Texten. Standardplatzhalter: <br/>Produktname - `{{name}}` |
| [!UICONTROL Mask for Meta Description] | Global | Bestimmt den Standardwert des Felds „Meta-Beschreibung“ basierend auf Platzhalterwerten aus anderen Feldern und allen zusätzlichen eingegebenen Texten. Standard-Platzhalter: <br/>Produktname - `{{name}}` <br/>Beschreibung - `{{description}}` |

{style="table-layout:auto"}

## [!UICONTROL Product Reviews]

![Produktbewertungen](./assets/catalog-product-reviews.png)<!-- zoom -->

<!-- [Product Reviews](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/merchandising/product-reviews/product-reviews) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enabled] | Shop-Ansicht | Ermöglicht Produktbewertungen. Optionen: `Yes` / `No` |
| [!UICONTROL Allow Guests to Write Reviews] | Website | Legt fest, ob Kunden ein Konto bei Ihrem Geschäft eröffnen müssen, um Produktbewertungen schreiben zu können. |

{style="table-layout:auto"}

## [!UICONTROL Storefront]

![Storefront](./assets/catalog-storefront.png)<!-- zoom -->

<!-- [Storefront](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/catalog/navigation/navigation-product-listings) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL List Mode] | Shop-Ansicht | Bestimmt das Format der Suchergebnisliste. Optionen: <br/>**`Grid Only`**- Formatiert die Liste als Raster aus Zeilen und Spalten. Jedes Produkt wird in einer einzelnen Zelle des Rasters angezeigt.<br/>**`List Only`** - Formatiert die Liste mit jedem Produkt in einer separaten Zeile. <br/>**`Grid (default / List)`**: Produkte werden standardmäßig in der Rasteransicht angezeigt und können in die Listenansicht umgeschaltet werden.<br/>**`List (default / Grid)`** : Produkte werden standardmäßig in der Listenansicht angezeigt und können in die Rasteransicht umgeschaltet werden. |
| [!UICONTROL Products per Page on Grid Allowed Values] | Shop-Ansicht | Bestimmt die Anzahl der in der Rasteransicht angezeigten Produkte. Um eine Auswahl von Optionen bereitzustellen, geben Sie mehrere Werte ein, die durch Kommas getrennt sind. |
| [!UICONTROL Products per Page on Grid Default Value] | Shop-Ansicht | Bestimmt die Anzahl der Produkte, die standardmäßig in der Rasteransicht pro Seite angezeigt werden. |
| [!UICONTROL Products per Page on List Allowed Values] | Shop-Ansicht | Bestimmt die Anzahl der in der Listenansicht angezeigten Produkte. Um eine Auswahl von Optionen bereitzustellen, geben Sie mehrere Werte ein, die durch Kommas getrennt sind. |
| [!UICONTROL Products per Page on List Default Value] | Shop-Ansicht | Bestimmt die Anzahl der standardmäßig pro Seite angezeigten Produkte in der Listenansicht. |
| Produktliste sortieren nach | Shop-Ansicht | Bestimmt die Sortierreihenfolge der Suchergebnisliste. Die Auswahl der Optionen wird durch die Anzeigeeinstellungen der Kategorie und die verfügbaren Attribute bestimmt, die als `Used for Sorting in Product Listing` festgelegt sind. Der Standardwert ist auf `Use All Available Attributes` festgelegt und umfasst normalerweise den besten Wert, den Namen und den Preis. Diese Einstellung gilt nicht für das [!DNL Live Search] [Widget „Produktauflistungsseite](https://experienceleague.adobe.com/en/docs/commerce/live-search/live-search-storefront/plp-styling). |
| [!UICONTROL Allow All Products per Page] | Shop-Ansicht | Ist hierfür `Yes` festgelegt, wird die Option `ALL` in das Steuerelement „Pro Seite anzeigen“ einbezogen. |
| [!UICONTROL Remember Category Pagination] | Global | Wenn auf `Yes` festgelegt, werden die aktuellen Paginierungswerte der Kategorie gespeichert, wenn Kundinnen und Kunden in (Produktlisten[ von einer Kategorie zur anderen ](../../catalog/navigation-product-listings.md). Wenn Sie den Wert speichern, wird mehr Cache-Speicher belegt. Dies kann sich auf die Art und Weise auswirken, wie Seiten von Suchmaschinen indiziert werden. Optionen: `Yes` / `No` (Standard) |
| [!UICONTROL Use Flat Catalog Category] | Global | Aktiviert die [flache Kategoriestruktur](../../catalog/catalog-flat.md) (nicht empfohlen). Optionen: `Yes` / `No` |
| [!UICONTROL Use Flat Catalog Product] | Global | Aktiviert die flache Produktstruktur. (nicht empfohlen) Optionen: `Yes` / `No` |
| [!UICONTROL Swatches per Product] | Shop-Ansicht | Bestimmt die Anzahl der für jedes Produkt verfügbaren Farbfelder. Standard: `16` |
| [!UICONTROL Show Swatches in Product List] | Shop-Ansicht | Bestimmt, ob die Farbfelder in der Produktliste angezeigt werden. Optionen: `Yes` / `No` |
| [!UICONTROL Show Swatch Tooltip] | Shop-Ansicht | Bestimmt, ob die QuickInfo für Muster angezeigt wird. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Product Alerts]

![Produktbenachrichtigungen](./assets/catalog-product-alerts.png)<!-- zoom -->

<!-- [Product Alerts](https://experienceleague.adobe.com/en/docs/commerce-admin/inventory/configuration/product-alerts/alert-setup) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Allow Alerts When Product Price Changes] | Shop-Ansicht | Legt fest, ob E-Mail-Warnhinweise für Produktpreisänderungen verfügbar sind. Optionen: `Yes` / `No` |
| [!UICONTROL Price Alert Email Template] | Shop-Ansicht | Identifiziert die Vorlage, die für E-Mail-Warnungen zu Produktpreisänderungen verwendet wird. Standardvorlage: `Product price alert` |
| [!UICONTROL Allow Alert When Product Comes Back in Stock] | Website | Legt fest, ob Kunden einen Warnhinweis erhalten können, wenn das Produkt wieder auf Lager ist. Optionen: `Yes` / `No` |
| [!UICONTROL Stock Alert Email Template] | Shop-Ansicht | Identifiziert die Vorlage, die für E-Mail-Benachrichtigungen zu Warnmeldungen verwendet wird. Standardvorlage: `Product stock alert` |
| [!UICONTROL Alert Email Sender] | Shop-Ansicht | Bestimmt den Store-Kontakt, der als Absender der E-Mail mit der Warnmeldung zum Produkt angezeigt wird. Optionen: `General Contact` / `Sales Representative` / `Customer Support` / `Custom Email` |

{style="table-layout:auto"}

## [!UICONTROL Product Alerts Run Settings]

![Einstellungen für die Ausführung von Produktwarnhinweisen](./assets/catalog-product-alerts-run-settings.png)<!-- zoom -->

<!-- [Product Alerts Run Settings](https://experienceleague.adobe.com/en/docs/commerce-admin/inventory/configuration/product-alerts/alert-setup) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Frequency] | Global | Wählen Sie aus, wie oft Warnhinweise gesendet werden sollen. Optionen: `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL Start Time] | Global | Wählen Sie aus, zu welcher Tageszeit der Warnhinweisprozess für das Produkt gestartet wird. Diese Zeit sollte nach der Durchführung von Preis- oder Bestandsaktualisierungen sein. |
| [!UICONTROL Error Email Recipient] | Global | Ermitteln Sie die E-Mail-Adresse der Person (normalerweise ein Store-Administrator), die eine E-Mail-Benachrichtigung erhalten soll, wenn ein Fehler im Warnhinweisprozess für das Produkt auftritt. |
| [!UICONTROL Error Email Sender] | Global | Wählen Sie die Rolle aus, in der die E-Mail `from` wird. |
| [!UICONTROL Error Email Template] | Global | Wählen Sie die E-Mail-Vorlage aus, die für Benachrichtigungen zu Produktwarnungs-Fehlern verwendet werden soll. |

{style="table-layout:auto"}

## [!UICONTROL Product Image Placeholders]

![Platzhalter für Produktbilder](./assets/catalog-product-image-placeholders.png)<!-- zoom -->

<!-- [Product Image Placeholders](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/products/digital-assets/product-image-config#image-placeholders) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Base Image] | Shop-Ansicht | Gibt die für das Basisbild ausgewählte Platzhalterdatei an. |
| [!UICONTROL Small Image] | Shop-Ansicht | Gibt die Platzhalterdatei an, die für das kleine Bild ausgewählt wurde. |
| [!UICONTROL Swatch] | Shop-Ansicht | Gibt die für das Farbfeld ausgewählte Platzhalterdatei an. |
| [!UICONTROL Thumbnail] | Shop-Ansicht | Identifiziert die für die Miniaturansicht ausgewählte Platzhalterdatei. |
| [!UICONTROL Choose File] |  | Navigiert zur Datei und lädt sie als Platzhalterbild für den Typ hoch. |

{style="table-layout:auto"}

## [!UICONTROL Recently Viewed/Compared Products]

![Kürzlich angesehene/verglichene Produkte](./assets/catalog-recently-viewed-and-compared-products.png)<!-- zoom -->

<!-- Recently Viewed/Compared Products](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/shopper-tools/products-viewed-compared) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Synchronize widget products with backend storage] | Global | Bestimmt die Synchronisierung von Produkt-Widget-Informationen wie Produkt-ID mit der Datenbank. Dies ermöglicht die Wiederverwendung von Informationen auf anderen Geräten. |
| [!UICONTROL Show for Current] | Website | Beschränkt die auf der aktuellen Website angezeigten Produkte. Optionen: `Website` / `Store` / `Store View` |
| [!UICONTROL Default Recently Viewed Products Count] | Shop-Ansicht | Bestimmt die maximale Anzahl der zuletzt angezeigten Produkte, die in der Liste angezeigt werden. |
| [!UICONTROL Default Recently Compared Products Count] | Shop-Ansicht | Bestimmt die maximale Anzahl der kürzlich verglichenen Produkte, die in der Liste angezeigt werden. |
| [!UICONTROL Lifetime of products in Recently Viewed Widget] | Global | Bestimmt, wie lange (in Sekunden) angezeigte Produkte in der zuletzt angezeigten Liste angezeigt werden. |
| [!UICONTROL Lifetime of products in Recently Compared Widget] | Global | Bestimmt, wie lange (in Sekunden) verglichene Produkte in der Liste für den letzten Vergleich angezeigt werden. |

{style="table-layout:auto"}

## [!UICONTROL Product Video]

![Produktvideos](./assets/catalog-product-video.png)<!-- zoom -->

<!-- [Product Videos](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/products/digital-assets/product-video) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL YouTube API key] | Shop-Ansicht | Gibt den API-Schlüssel an, der für die Verbindung mit dem YouTube-Server erforderlich ist. |
| [!UICONTROL Autostart base video] | Shop-Ansicht | Um das Video nach dem Laden der Seite automatisch zu starten, setzen Sie auf `Yes`. |
| [!UICONTROL Show related video] | Shop-Ansicht | Um verwandte Videos anzuzeigen, setzen Sie auf `Yes`. |
| [!UICONTROL Auto restart video] | Shop-Ansicht | Um die automatische Videowiedergabe zu aktivieren, setzen Sie auf `Yes`. |

{style="table-layout:auto"}

## [!UICONTROL Price]

![Preis](./assets/catalog-price.png)<!-- zoom -->

<!--Price](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/products/pricing/catalog-price-scope) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Catalog Price Scope] | Global | Bestimmt den Umfang der Basiswährung. Optionen: `Global` / `Website` |
| [!UICONTROL Default Product Price] | Global | ![Adobe Commerce](../../assets/adobe-logo.svg) (nur Adobe Commerce) Definiert den standardmäßigen Produktpreis, falls zutreffend. |

{style="table-layout:auto"}

## [!UICONTROL Layered Navigation]

>[!NOTE]
>
>Die in diesem Abschnitt beschriebene Standardsuchkonfiguration unterscheidet sich für die [Live-Suche](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html).

<!-- [Layered Navigation - Automatic (equalize price ranges)](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/catalog/navigation/navigation-layered#configure-layered-navigation) -->

![Mehrschichtige Navigation - Automatisch (Preisausgleiche)](./assets/layered-navigation-equalize-price-range.png)<!-- zoom -->

![Mehrschichtige Navigation - Automatisch (gleicht die Produktzahl an)](./assets/layered-navigation-equalize-product-counts.png)<!-- zoom -->

![Mehrschichtige Navigation - Manuell](./assets/layered-navigation-manual.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Display Product Count] | Shop-Ansicht | Bestimmt, ob die Produktanzahl nach jedem Attribut, Preisbereich und Kategorie angezeigt wird. Optionen: `Yes` / `No` |
| [!UICONTROL Price Navigation Step Calculation] | Shop-Ansicht | Bestimmt die Methode, die zur Bestimmung des [Preisnavigationsschritts](../../catalog/navigation-layered.md#configure-price-navigation) verwendet wird. Optionen: <br/>`Automatic (equalize price ranges)` - Basiert die Berechnung auf der Preisspanne der Produkte in der Gruppe. <br/>`Automatic (equalize product counts)` - Basiert die Berechnung auf der Anzahl der Produkte in der Gruppe. Legt einen Schwellenwert für die Mindestanzahl von Produkten in der Gruppe fest, um zu verhindern, dass sie in kleinere Gruppen unterteilt werden. <br/>`Manual` - Verwendet das von Ihnen für Preisintervalle eingegebene Divisionslimit. |
| [!UICONTROL Default Price Navigation Step] | Shop-Ansicht | Bestimmt die Anzahl der Produkte, die in jedem Schritt enthalten sind. |
| [!UICONTROL Maximum Number of Price Intervals] | Shop-Ansicht | Legt eine Begrenzung für die Anzahl der Preisintervalle fest, die in der mehrschichtigen Navigation angezeigt werden. |

{style="table-layout:auto"}

## [!UICONTROL Category Permissions]

{{ee-feature}}

![Kategorieberechtigungen](./assets/catalog-category-permissions.png)<!-- zoom -->

<!-- [Category Permissions](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/categories/category-permissions) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable] | Global | Aktiviert Kategorieeinschränkungen. Standardmäßig beschränkt die Verwendung dieser Funktion alle Kategorien. Optionen: `Yes` / `No` |
| [!UICONTROL Allow Browsing Category] | Website | Bestimmt, wer Kategorien durchsuchen darf. Optionen: <br/>`Yes, for Everyone` - Ermöglicht allen Besuchern und Kunden das Durchsuchen der Kategorie. <br/>`Yes, for Specified Customer Groups` - Ermöglicht es nur Mitgliedern ausgewählter Kundengruppen, die Kategorie zu durchsuchen. <br/>`No, Redirect to Landing Page` - verweigert den Zugriff auf die Kategorie und leitet zur ausgewählten Seite weiter. |
| [!UICONTROL Display Product Prices] | Website | Steuert die Anzeige von Produktpreisen für die Kategorie. Optionen: <br/>`Yes, for Everyone` - Ermöglicht es jedem, den Preis der Produkte in der Kategorie zu sehen. <br/>`Yes, for Specified Customer Groups` - Ermöglicht es nur Mitgliedern ausgewählter Kundengruppen, den Preis von Produkten in der Kategorie anzuzeigen. <br/>`No` - Schaltet die Anzeige von Produktpreisen für die Kategorie aus. |
| [!UICONTROL Allow Adding to Cart] | Website | Legt fest, wer Produkte aus der Kategorie kaufen kann. Optionen: <br/>`Yes, for Everyone` - Ermöglicht es jedem, Produkte aus der Kategorie in den Warenkorb zu legen. <br/>`Yes, for Specified Customer Groups` - Ermöglicht es nur Mitgliedern ausgewählter Kundengruppen, Produkte aus der Kategorie in ihren Warenkorb zu legen. <br/>`No` - Erlaubt niemandem, Produkte aus der Kategorie in den Warenkorb zu legen. |
| [!UICONTROL Disallow Catalog Search by] | Website | Gibt die Kundengruppen an, die nicht nach Produkten in der Kategorie suchen dürfen. |

{style="table-layout:auto"}

## [!UICONTROL Search Engine Optimization]

![Suchmaschinenoptimierung](./assets/catalog-search-engine-optimization.png)<!-- zoom -->

<!-- [Search Engine Optimization](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/products/settings/product-search-engine-optimization) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Popular Search Terms] | Shop-Ansicht | Bestimmt, ob _Beliebte Suchbegriffe_ im Store implementiert sind. Diese Einstellung gilt nicht für Stores, die die [Live Search“ ](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html). Optionen: `Enable` / `Disable` |
| [!UICONTROL Product URL Suffix] | Shop-Ansicht | Bestimmt, ob ein Suffix, wie HTML oder HTML, auf Produkt-URLs angewendet wird. Wenn verwendet, wird ein Punkt vor dem Suffix nicht eingefügt, da er automatisch angewendet wird. |
| [!UICONTROL Category URL Suffix] | Shop-Ansicht | Bestimmt, ob ein Suffix wie HTML oder HTML auf Kategorie-URLs angewendet wird. Wenn verwendet, wird ein Punkt vor dem Suffix nicht eingefügt, da er automatisch angewendet wird. |
| [!UICONTROL Use Categories Path for Product URLs] | Shop-Ansicht | Bestimmt, ob Kategoriepfade in Produkt-URLs in der Storefront enthalten sind. Dies kann dazu führen, dass mehrere URLs auf dieselbe Seite verweisen, was sich auf den Suchrang auswirken kann. Weitere Informationen finden Sie unter [Kanonisches Meta-Tag](../../merchandising-promotions/meta-data.md#canonical-meta-tag). |
| [!UICONTROL Create Permanent Redirect for URLs if URL Key Changed] | Shop-Ansicht | Legt fest, ob bei jeder Änderung eines URL-Schlüssels automatisch eine permanente Umleitung erstellt wird Nach der Implementierung ist das Kontrollkästchen Benutzerdefinierte Umleitung für alte URL erstellen unter dem Feld Produkt-URL-Schlüssel standardmäßig aktiviert. Optionen: `Yes` / `No` |
| [!UICONTROL Generate "category/product" URL Rewrites] | Global | Legt fest, ob Adobe Commerce Daten generiert und in Rewrite-Tabellen speichert, wenn ein Benutzer eine Kategorie mit vielen zugewiesenen Produkten speichert.  <br/><br/>Das Ändern dieser Option wirkt sich nicht darauf aus, wie Produkt-URLs in Adobe Commerce aufgelöst werden, da das System Produkt-URLs unabhängig von dieser Einstellung automatisch auflöst. <br/><br/>Optionen: `Yes` / `No` <br/><br/>**_Wichtig:_**Das Speichern dieser generierten Daten in einer URL-Umschreibungstabelle kann die Leistung beeinträchtigen. Weitere Informationen finden [ unter ](../../merchandising-promotions/url-redirect-product-automatic.md) Produktweiterleitungen . |
| [!UICONTROL Apply transliteration for product URL] | Shop-Ansicht | Bestimmt, ob beim Erstellen oder Aktualisieren von Produkt-URLs Transliteration angewendet wird. Optionen: `Yes` / `No`. Die Standardeinstellung ist `Yes`. <br/><br/>Für bestimmte Anwendungsfälle sollten Sie die Transliteration deaktivieren. Wenn Sie beispielsweise einen Online-Store auf Chinesisch betreiben, empfehlen die Best Practices von SEO, dass die Produkt-URLs mit dem Produktnamen übereinstimmen. Wenn Sie die Option auf `No` setzen, können chinesische Zeichen in Produkt-URLs anstelle einer ASCII-Entsprechung verwendet werden. |
| [!UICONTROL Page Title Separator] | Shop-Ansicht | Gibt das Zeichen an, das den Kategorienamen und die Unterkategorie in der Titelleiste des Browsers trennt. |
| [!UICONTROL Use Canonical Link Meta Tag for Categories] | Shop-Ansicht | Wenn mehrere URLs auf dieselbe Kategorieseite verweisen, verwendet diese Option ein kanonisches Meta-Tag, um die Kategorie-URL zu identifizieren, die Suchmaschinen indizieren sollten. Die URL enthält einen vollständigen Namen für die Kategorie unter Verwendung des Meta-Tags. Dies reduziert doppelte Inhalte und verbessert die SEO. Optionen: `Yes` / `No` |
| [!UICONTROL Use Canonical Link Meta Tag for Products] | Shop-Ansicht | Wenn mehrere URLs auf dieselbe Produktseite verweisen, verwendet diese Option ein kanonisches Meta-Tag, um die Produkt-URL zu identifizieren, die Suchmaschinen indizieren sollten. Die URL enthält einen vollständigen Namen zum Produkt unter Verwendung des Meta-Tags. Dies reduziert doppelte Inhalte und verbessert die SEO. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Category Top Navigation]

![Oberste Navigation der Kategorie](./assets/catalog-category-top-navigation.png)<!-- zoom -->

<!-- Category Top Navigation](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/catalog/navigation/navigation-top) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Maximal Depth] | Global | Bestimmt die Anzahl der Unterkategorieebenen in der oberen Navigation. Beim Standardwert `0` ist die Anzahl der Ebenen nicht beschränkt. |

{style="table-layout:auto"}

## [!UICONTROL Catalog Search]

Sie können die Katalogsuche mithilfe von [[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html) oder Suchmaschinendiensten von Drittanbietern konfigurieren, die von Adobe Commerce unterstützt werden. Folgen Sie den Installationsanweisungen.

### Adobe Commerce mit [!DNL Live Search]

Wenn die Live Search installiert ist, umfasst die Katalogsuche die folgenden Konfigurationseinstellungen:

![Katalogsuche für die Live Search](./assets/catalog-search-live-search.png)<!-- zoom -->

<!-- [Catalog Search for Live Search](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/catalog/search/search-configuration) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Minimal Query Length] | Shop-Ansicht | Die bei einer Katalogsuche zulässige Mindestanzahl von Zeichen. Der für diese Option festgelegte Wert muss mit dem entsprechenden Bereich kompatibel sein, der in Ihren Elasticsearch-Suchmaschinenkonfigurationen festgelegt ist. Wenn Sie diesen Wert beispielsweise in Adobe Commerce auf `2` setzen, aktualisieren Sie den Wert in Ihrer Suchmaschine. |
| [!UICONTROL Maximum Query Length] | Shop-Ansicht | Die maximale Anzahl von Zeichen, die bei einer Katalogsuche zulässig ist. Der für diese Option festgelegte Wert muss mit dem entsprechenden Bereich kompatibel sein, der in Ihren Elasticsearch-Suchmaschinenkonfigurationen festgelegt ist. Wenn Sie diesen Wert in Adobe Commerce beispielsweise auf 300 setzen, aktualisieren Sie den Wert in Ihrer Suchmaschine. |
| [!UICONTROL Number of top search results to cache] | Shop-Ansicht | Die Anzahl der beliebten Suchbegriffe und Ergebnisse, die zwecks schnellerer Antworten zwischengespeichert werden sollen. Bei Eingabe des Werts `0` werden alle Suchbegriffe und Ergebnisse bei einer zweiten Eingabe zwischengespeichert. Standardwert: `100` |
| [!UICONTROL Autocomplete Limit] | Shop-Ansicht | Bestimmt die maximale Anzahl von Zeilen, die auf der Seite [Storefront-Popover] verfügbar sind. Der Standardwert kann bei der Installation der Live Search geändert und später aktualisiert werden, indem diese Konfigurationseinstellung geändert wird. Standardwert: `8` |

{style="table-layout:auto"}

### Suchmaschinen von Drittanbietern

Adobe Commerce unterstützt OpenSearch und Elasticsearch. Die Adobe Commerce-Versionen 2.3.7-p3, 2.4.3-p2 und 2.4.4 und höher unterstützen den OpenSearch-Service. Elasticsearch 7.11 und höher wird in Adobe Commerce nicht für Cloud-Infrastrukturprojekte unterstützt. Elasticsearch wird weiterhin für lokale Installationen unterstützt.

>[!IMPORTANT]
>
>- Aufgrund der Ankündigung zum Ende der Unterstützung für Elasticsearch 7 im August 2023 empfiehlt Adobe allen Adobe Commerce-Kunden, zur OpenSearch 2.x -Suchmaschine zu migrieren. Informationen zur Migration Ihrer Suchmaschine während eines Upgrades finden Sie unter [Migration zu OpenSearch](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/prepare/opensearch-migration.html) im _Upgrade-Handbuch_.
>- In den Versionen 2.4.4 und 2.4.3-p2 gelten alle Felder mit der Bezeichnung Elasticsearch auch für OpenSearch. Mit der Einführung der Unterstützung für Elasticsearch 8.x in Version 2.4.6 wurden neue Bezeichnungen erstellt, um zwischen Elasticsearch- und OpenSearch-Konfigurationen zu unterscheiden. Die Konfigurationsoptionen für beide sind jedoch identisch.

![Konfigurationsoptionen für die Katalogsuche](./assets/catalog-search-opensearch.png){zoomable="yes"}

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Minimal Query Length] | Shop-Ansicht | Die bei einer Katalogsuche zulässige Mindestanzahl von Zeichen. Der für diese Option festgelegte Wert muss mit dem entsprechenden Bereich kompatibel sein, der in Ihrer OpenSearch- oder Elasticsearch-Konfiguration festgelegt ist. Wenn Sie diesen Wert beispielsweise in Adobe Commerce auf `2` setzen, müssen Sie auch den Wert in Ihrer Suchmaschinenkonfiguration aktualisieren. Standardwert: `3` |
| [!UICONTROL Maximum Query Length] | Shop-Ansicht | Die maximale Anzahl von Zeichen, die bei einer Katalogsuche zulässig ist. Der für diese Option festgelegte Wert muss mit dem entsprechenden Bereich kompatibel sein, der in Ihrer OpenSearch- oder Elasticsearch-Konfiguration festgelegt ist. Wenn Sie diesen Wert beispielsweise in Adobe Commerce auf `300` setzen, müssen Sie den Wert in Ihrer Suchmaschinenkonfiguration aktualisieren. Standardwert: `128` |
| [!UICONTROL Number of top search results to cache] | Shop-Ansicht | Die Anzahl der beliebten Suchbegriffe und Ergebnisse, die zwecks schnellerer Antworten zwischengespeichert werden sollen. Bei Eingabe des Werts `0` werden alle Suchbegriffe und Ergebnisse bei einer zweiten Eingabe zwischengespeichert. Standardwert: `100` |
| [!UICONTROL Enable EAV Indexer] | Global | Legt fest, ob der Produkt-EAV-Indexer aktiviert oder deaktiviert werden soll. Diese Funktion verbessert die Indexierungsgeschwindigkeit und verhindert, dass der Indexer von Erweiterungen von Drittanbietern verwendet werden kann. Standardoption: `Yes` für aktiviert |
| [!UICONTROL Autocomplete Limit] | Shop-Ansicht | Die maximale Anzahl von Suchabfragen, die unter dem Suchfeld für die automatische Vervollständigung der Suche angezeigt werden sollen. Wenn Sie diesen Wert einschränken, wird die Leistung der Suche gesteigert und die angezeigte Listengröße verringert. Standardwert: `8` |
| Suchmaschine | Global | Identifiziert die Suchmaschine, die zum Verarbeiten von Anfragen für Katalogdaten erforderlich ist. Die Konfigurationsoptionen für Suchmaschinen sind für OpenSearch und Elasticsearch identisch. Optionen: `OpenSearch` oder `Elasticsearch` |
| [!UICONTROL OpenSearch Server Hostname] | Global | Gibt den Namen des OpenSearch- oder Elasticsearch-Hostservers an. |
| [!UICONTROL OpenSearch Server Port] | Global | Gibt die Nummer des von OpenSearch oder Elasticsearch verwendeten Server-Ports an. Standardwert: `9200` |
| [!UICONTROL OpenSearch Index Prefix] | Global | Weist ein Präfix zu, um den OpenSearch- oder Elasticsearch-Index zu identifizieren. Standardwert: `magento2` |
| [!UICONTROL Enable OpenSearch HTTP Auth] | Global | Wenn diese Option aktiviert ist, verwendet die HTTP-Authentifizierung, um einen Benutzernamen und ein Kennwort einzugeben, bevor auf den OpenSearch- oder Elasticsearch-Server zugegriffen wird. Optionen: `Yes` / `No` |
| [!UICONTROL OpenSearch HTTP Username] | Global | Wenn _Elasticsearch HTTP-Authentifizierung aktivieren_ auf `Yes` gesetzt ist, gibt den Benutzernamen für die OpenSearch- oder Elasticsearch HTTP-Authentifizierung an. |
| [!UICONTROL OpenSearch HTTP Password] | Global | Wenn _Elasticsearch HTTP-Authentifizierung aktivieren_ auf `Yes` gesetzt ist, gibt das Kennwort für die OpenSearch- oder Elasticsearch HTTP-Authentifizierung an. |
| [!UICONTROL OpenSearch Server Timeout] | Global | Bestimmt die Anzahl der Sekunden, nach denen eine Anfrage an den OpenSearch- oder Elasticsearch-Server das Zeitlimit überschreitet. Standardwert: `15` |
| [!UICONTROL Test Connection] |  | Validiert die OpenSearch- oder Elasticsearch-Verbindung. |
| [!UICONTROL Enable Search Recommendations] | Shop-Ansicht | Bestimmt, ob Suchempfehlungen angeboten werden, wenn eine Suche keine Ergebnisse zurückgibt und auf der Suchergebnisseite unter dem Abschnitt `Related search terms` angezeigt wird. Optionen: `Yes` / `No` <br/>Wenn auf „Ja“ gesetzt, werden zusätzliche Optionen für _[!UICONTROL Search Recommendations Count]_und_[!UICONTROL Shows Results Count for Each Recommendation]_ angezeigt. |
| [!UICONTROL Search Recommendations Count] | Shop-Ansicht | Gibt die Anzahl der Suchbegriffe an, die als Empfehlungen angeboten werden. Standardmäßig werden nicht mehr als fünf angezeigt. |
| [!UICONTROL Show Results Count for Each Recommendation] | Shop-Ansicht | Bei Festlegung auf `Yes` wird die Anzahl der für die vorgeschlagene Suchempfehlung gefundenen Produkte in Klammern angezeigt. Optionen: `Yes` / `No` |
| [!UICONTROL Enable Search Suggestions] | Shop-Ansicht | Legt fest, ob Suchvorschläge für häufige Rechtschreibfehler angezeigt werden. Wenn diese Option aktiviert ist, werden Suchvorschläge für alle Anfragen angeboten, die keine Ergebnisse zurückgeben und unter dem Abschnitt `Did you mean` auf der Seite **Suchergebnisse** angezeigt werden. Suchvorschläge können die Leistung der Suche beeinträchtigen. Bei `Yes` werden zusätzliche Optionen für Suchempfehlungen aktivieren und zugehörige Felder angezeigt. Optionen: `Yes` / `No` |
| [!UICONTROL Search Suggestions Count] | Shop-Ansicht | Bestimmt die Anzahl der angebotenen Suchvorschläge. Beispiel: `2` |
| [!UICONTROL Show Results Count for Each Suggestion] | Shop-Ansicht | Bestimmt, ob die Anzahl der Suchergebnisse für jeden Vorschlag angezeigt wird. Je nach Thema wird die Zahl normalerweise nach dem Vorschlag in Klammern angezeigt. Optionen: `Yes` / `No` |
| [!UICONTROL Minimum Terms to Match] | Shop-Ansicht | Gibt einen Wert an, der der Anzahl der Begriffe aus Ihrer Abfrage entspricht, mit denen die Suchergebnisse übereinstimmen müssen, damit sie zurückgegeben werden. Dadurch wird eine optimale Ergebnisrelevanz für Kunden gewährleistet. Prozentwerte entsprechen einer Zahl. Bei Bedarf werden sie abgerundet und als Mindestanzahl von Begriffen verwendet, die in Ihrer Abfrage übereinstimmen müssen. Der Wert kann eine negative oder positive Ganzzahl, ein negativer oder positiver Prozentsatz, eine Kombination aus beiden oder mehrere Kombinationen sein. Weitere Informationen finden Sie unter [minimum_should_match](https://opensearch.org/docs/latest/query-dsl/minimum-should-match/) in der OpenSearch-Dokumentation. |

## [!UICONTROL Downloadable Product Options]

![Download-Produktoptionen](./assets/catalog-downloadable-product-options.png)<!-- zoom -->

<!-- [Downloadable Product Options](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/products/types/product-create-downloadable#configure-the-download-options) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Order Item Status to Enable Downloads] | Website | Bestimmt den Status, den eine Bestellung aufweisen muss, bevor Downloads verfügbar werden. Optionen: `Pending` / `Invoiced` |
| [!UICONTROL Default Maximum Number of Downloads] | Website | Bestimmt die Standardanzahl der Downloads, die einem Kunden zur Verfügung stehen. |
| [!UICONTROL Shareable] | Website | Legt fest, ob sich Kunden bei ihren Konten anmelden müssen, um auf den Download-Link zuzugreifen. Optionen: <br/>**Ja** - Ermöglicht den Versand des Links per E-Mail, die dann für andere freigegeben werden kann. <br/>**Nein** - Erfordert, dass sich Kunden bei ihren Konten anmelden, um auf den Download-Link zuzugreifen. |
| [!UICONTROL Default Sample Title] | Shop-Ansicht | Der Standardtitel für alle Beispieldateien. |
| [!UICONTROL Default Link Title] | Shop-Ansicht | Der Standardlink für alle herunterladbaren Titel. |
| [!UICONTROL Opens Links in New Window] | Website | Bestimmt, ob der Download-Link in einem neuen Browser-Fenster geöffnet wird. Optionen: `Yes` / `No` |
| [!UICONTROL Use Content Disposition] | Shop-Ansicht | Bestimmt, wie der Link zum herunterladbaren Inhalt als E-Mail-Anhang oder als Inline-Link in einem Browser-Fenster bereitgestellt wird. Optionen: <br/>**`Attachment`**- Der Download-Link wird als E-Mail-Anhang bereitgestellt.<br/>**`Inline`** - Der Download-Link wird als Inline-Link auf einer Web-Seite bereitgestellt. |
| [!UICONTROL Disable Guest Checkout if Cart Contains Downloadable Items] | Website | Legt fest, ob Gäste, die herunterladbare Produkte kaufen, sich für ein Konto registrieren und sich anmelden müssen, um den Checkout-Prozess abzuschließen. Optionen: <br/>**`Yes`**- Wenn der Warenkorb herunterladbare Produkte enthält, muss sich der Gast entweder für ein Konto registrieren oder bei einem vorhandenen Konto anmelden, um den Kauf abzuschließen.<br/>**`No`** - Der Download-Link wird als Inline-Link im Textkörper der E-Mail-Nachricht bereitgestellt.  <br/> _**Hinweis**_ Der Gast-Checkout ist nur für Download-Produkte verfügbar, wenn die Option Freigeben auf `Yes` festgelegt ist. |

{style="table-layout:auto"}

## [!UICONTROL Date & Time Custom Options]

![Benutzerdefinierte Optionen für Datum und Uhrzeit](./assets/catalog-date-time-custom-options.png)<!-- zoom -->

<!-- Date & Time Custom Options](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/product-attributes/attributes-input-types#date-and-time-options) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Use JavaScript Calendar] | Shop-Ansicht | Bestimmt, ob der JavaScript-Kalender als Eingabedialog für Datumsfelder verwendet wird. Optionen: `Yes` / `No` <br/>Wenn auf `No` gesetzt, wird für jeden Teil des Datumsfelds ein separates Dropdown-Menü angezeigt. |
| [!UICONTROL Date Fields Order] | Shop-Ansicht | Legt die Reihenfolge der drei Datumsfelder fest. Optionen: `Day` / `Month` / `Year` |
| [!UICONTROL Time Format] | Shop-Ansicht | Legt das Zeitformat entweder auf 12 oder 24 Stunden fest. Optionen: `12h AM/PM` / `24h` |
| [!UICONTROL Year Range] | Shop-Ansicht | Definiert den Anfang und das Ende von Jahren, die im Feld _Jahr_ angezeigt werden. Der Wert muss im Format JJJJ eingegeben werden. |

{style="table-layout:auto"}

## [!UICONTROL Catalog Events]

{{ee-feature}}

![Katalogereignisse](./assets/catalog-events.png)<!-- zoom -->

<!-- [Catalog Events](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/events/events-private-sales) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable Catalog Events Functionality] | Website | Bestimmt, ob das Modul Ereignisse aktiviert ist. |
| [!UICONTROL Enable Catalog Event Widget on Frontend] | Shop-Ansicht | Legt fest, ob das Ereignis-Widget in der Storefront verfügbar ist. Dies ist ein statischer Block mit Informationen zu Ereignissen auf Ihrer Site. |
| [!UICONTROL Number of Events to be Displayed in the Event Slider Widget] | Shop-Ansicht | Bestimmt die Anzahl der Ereignisse, die im Ereignis-Schieberegler-Widget auf den Kategorieseiten angezeigt werden. Verwenden Sie zum Überschreiben die Variable `limit="x"` . |
| [!UICONTROL Events to Scroll per Click in Event Slider Widget] | Shop-Ansicht | Bestimmt die Anzahl der Ereignisse, die auf CMS-Seiten, z. B. auf der Startseite, im Ereignisregler angezeigt werden. Verwenden Sie zum Überschreiben die Variable `scroll="x"` . |

{style="table-layout:auto"}

## [!UICONTROL Rule-Based Product Relations]

{{ee-feature}}

![Regelbasierte Produktbeziehungen](./assets/catalog-rule-based-product-relations.png)<!-- zoom -->

<!-- [Rule-Based Product Relations](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/product-relationships/product-related-rules) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Maximum Number of Products in Related Products List] | Global | Legt die maximale Anzahl von Produkten fest, die in der Liste &quot;_Produkte“ angezeigt_ können. |
| [!UICONTROL Show Related Products] | Global | Bestimmt, welche Liste verwandter Produkte im Store angezeigt wird. Dabei kann es sich entweder um die Liste handeln, die manuell in den Produktinformationen ausgewählt wird, die Liste, die als Reaktion auf eine Produktbeziehungsregel generiert wird, oder um eine Kombination aus beidem. Optionen: `Both Selected and Rule-Based` / `Selected Only` / `Rule-Based Only` |
| [!UICONTROL Rotation Mode for Products in Related Products List] | Global | Bestimmt die Reihenfolge, in der Produkte in der Liste _Verwandte Produkte_ angezeigt werden. Optionen: `Do not rotate` / `Shuffle` |
| [!UICONTROL Maximum Number of Products in Cross-Sell Product List] | Global | Bestimmt die maximale Anzahl von Produkten, die in der Crosssell-Liste angezeigt werden können. |
| [!UICONTROL Show Cross-Sell Products] | Global | Bestimmt, welche Liste von Crosssell-Produkten im Store angezeigt wird. Dabei kann es sich entweder um die Liste handeln, die manuell in den Produktinformationen ausgewählt wird, die Liste, die als Reaktion auf eine Produktbeziehungsregel generiert wird, oder um eine Kombination aus beidem. Optionen: `Both Selected and Rule-Based` / `Selected Only` / `Rule-Based Only` |
| [!UICONTROL Rotation Mode for Products in Cross-Sell Products List] | Global | Bestimmt die Reihenfolge, in der Produkte in der Crossselling-Produktliste angezeigt werden. Optionen: Nicht drehen/mischen |
| [!UICONTROL Maximum Number of Products in Upsell Product List] | Global | Legt die maximale Anzahl von Produkten fest, die in der _Upsell-_&quot; angezeigt werden können. |
| [!UICONTROL Show Upsell Products] | Global | Legt fest, welche Liste von Upsell-Produkten im Store angezeigt wird. Dabei kann es sich entweder um die Liste handeln, die manuell in den Produktinformationen ausgewählt wird, die Liste, die als Reaktion auf eine Produktbeziehungsregel generiert wird, oder um eine Kombination aus beidem. Optionen: `Both Selected and Rule-Based` / `Selected Only` / `Rule-Based Only` |
| [!UICONTROL Rotation Mode for Products in Upsell Product List] | Global | Bestimmt die Reihenfolge, in der Produkte in der Upsell-Produktliste angezeigt werden. Optionen: `Do not rotate` / `Shuffle` |

{style="table-layout:auto"}
