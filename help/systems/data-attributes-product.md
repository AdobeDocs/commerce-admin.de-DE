---
title: Referenz zu Produktdatenattributen
description: Verwenden Sie diese Referenz zu Produktdatenattributen, wenn Sie mit Produktdatenimporten und -exporten arbeiten.
exl-id: 9ffa4d1f-cbf8-4a08-bb79-33f21e698a74
feature: Products, Attributes
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '2469'
ht-degree: 2%

---

# Referenz zu Produktdatenattributen

In der folgenden Tabelle werden die Attribute eines typischen Produktexports in der Standardreihenfolge aufgelistet, in der sie angezeigt werden. Jedes Attribut wird in der CSV-Datei als Spalte dargestellt und die Produktdatensätze werden durch Zeilen dargestellt. Spalten, die mit einem Unterstrich beginnen, enthalten Dienstdaten wie Eigenschaften oder Optionswerte für komplexe Daten. Sie können [export](data-export.md) ein Produkt aus Ihrem Katalog, um zu sehen, wie jedes Attribut in den Daten dargestellt wird.

Die zum Exportieren dieser Daten verwendete Installation enthält die installierten Beispieldaten und verfügt über zwei Websites und mehrere Store-Ansichten. Obwohl diese Liste alle Spalten enthält, die normalerweise exportiert werden, wird die `sku` ist der einzige erforderliche Wert. Um Daten zu importieren, können Sie nur die Spalten mit Änderungen einbeziehen. Die `sku` sollte die erste Spalte sein, aber die Reihenfolge der übrigen Attribute spielt keine Rolle.

## Einfache Produkt-CSV-Dateistruktur

| Attribut | Beschreibung |
|--- |--- |
| `sku` | (Erforderlich) Die Bestandseinheit ist eine eindeutige alphanumerische Kennung, die zur Bestandsverfolgung verwendet wird. Eine SKU kann bis zu 64 Zeichen lang sein. Beispiel: `sku123`<br/>**_Hinweis:_**Eine SKU, die länger als 64 Zeichen ist, führt dazu, dass der Import fehlschlägt. |
| `store_view_code` | Identifiziert die spezifischen Store-Ansichten, in denen das Produkt verfügbar ist. Wenn leer, ist das Produkt in der standardmäßigen Store-Ansicht verfügbar. Beispiel: `storeview1`, `english`, `spanish` |
| `attribute_set_code` | Weist das Produkt je nach Produkttyp einem bestimmten Attributsatz oder einer bestimmten Produktvorlage zu. Nachdem das Produkt erstellt wurde, kann der Attributsatz nicht mehr geändert werden. Beispiel: `default` |
| `product_type` | Gibt den Produkttyp an. Werte:<br/>`simple` — Sachanlagen, die in der Regel als Einzeleinheiten oder in festen Mengen verkauft werden.<br/>`grouped` — Eine Gruppe von Einzelprodukten, die als Set verkauft werden.<br/>`configurable` — Ein Produkt mit mehreren Optionen, die der Kunde auswählen muss, bevor er einen Kauf tätigt. Der Bestand kann für jeden Variantensatz verwaltet werden, da er ein separates Produkt mit einer eigenen SKU darstellt. Beispielsweise ist eine Kombination aus Farbe und Größe für ein konfigurierbares Produkt mit einer bestimmten SKU im Katalog verknüpft.<br/>`virtual` — Ein nicht materielles Produkt, das nicht versandpflichtig ist und nicht im Bestandsverzeichnis aufbewahrt wird. Beispiele sind Dienste, Mitgliedschaften und Abonnements.<br/>`bundle` — Ein anpassbarer Produktsatz mit einfachen Produkten, die zusammen verkauft werden. |
| `categories` | Gibt jede Kategorie an, die dem Produkt zugewiesen ist. Trennen Sie Kategorien und Unterkategorien durch einen Schrägstrich. Um mehrere Kategoriepfade anzugeben, trennen Sie jeden Pfad durch einen senkrechten Strich | Symbol. Beispiel: `Default Category/Gear&#124;Default Category/Gear/Bags` |
| `product_websites` | Der Website-Code jeder Website, auf der das Produkt verfügbar ist. Ein einzelnes Produkt kann mehreren Websites zugewiesen oder auf eine beschränkt werden. Wenn Sie mehrere Websites angeben, trennen Sie jede durch ein Komma und ohne Leerzeichen. Beispiel: `base` oder `base,website2` |
| `name` | Der Produktname wird in allen Produktlisten angezeigt und ist der Name, den Kunden zur Identifizierung des Produkts verwenden. |
| `description` | Die Produktbeschreibung enthält detaillierte Informationen zum Produkt und kann einfache HTML-Tags enthalten. |
| `short_description` | Die Verwendung der kurzen Produktbeschreibung hängt vom Thema ab. Sie kann in Produktlisten angezeigt werden und wird manchmal in RSS-Feed-Listen verwendet, die an Shopping-Sites gesendet werden. |
| `weight` | Das Gewicht des einzelnen Erzeugnisses. Das tatsächliche Produktgewicht wird vom Transportunternehmen zum Zeitpunkt des Versands bestimmt. |
| product_online | Bestimmt, ob das Produkt im Laden zum Verkauf angeboten wird. Werte:<br/>`1` — (Ja) Das Produkt ist aktiviert und zum Verkauf verfügbar.<br/>`2` — (Nein) Das Produkt ist deaktiviert und kann nicht verkauft werden. |
| `tax_class_name` | Der Name der mit diesem Produkt verknüpften Steuerklasse. |
| `visibility` | Bestimmt, ob das Produkt im Katalog sichtbar und für die Suche verfügbar ist. Werte:<br/>`Not Visible Individually` — Das Produkt ist nicht in Produktlisten enthalten, obwohl es als Variante eines anderen Produkts verfügbar sein könnte.<br/>`Catalog` — Das Produkt wird in allen Kataloglisten angezeigt.<br/>`Search` - Das Produkt ist für Suchvorgänge verfügbar.<br/>`Catalog, Search` — Das Produkt ist in Kataloglisten enthalten und auch für die Suche verfügbar. |
| `price` | Der Preis, den das Produkt in Ihrem Geschäft zum Verkauf angeboten wird. |
| `special_price` | Der ermäßigte Preis des Produkts im angegebenen Datumsbereich. |
| `special_price_from_date` | Das Anfangsdatum des Zeitraums, in dem der Sonderpreis in Kraft ist. |
| `special_price_to_date` | Das letzte Datum des Zeitraums, in dem der Sonderpreis in Kraft tritt. |
| `url_key` | Der Teil der URL, der das Produkt identifiziert. Der Standardwert basiert auf dem Produktnamen. Beispiel: `product-name` |
| save_rewrites_history | Wenn der Wert bereitgestellt wird `1` mit einer neuen `url_key`, wird ein neues 301-URL-Umschreiben generiert, sodass die alte URL an die neue URL umgeleitet wird. |
| `meta_title` | Der Metadatentitel wird in der Titelleiste und auf der Registerkarte des Browsers und in den Suchergebnislisten angezeigt. Der Metadatentitel sollte für das Produkt eindeutig sein, hochwertige Schlüsselwörter enthalten und weniger als 70 Zeichen lang sein. |
| `meta_keywords` | Meta-Suchbegriffe sind nur für Suchmaschinen sichtbar und werden von einigen Suchmaschinen ignoriert. Wählen Sie Suchbegriffe mit hohem Wert, durch Kommas getrennt. Beispiel: `keyword1`, `keyword2`, `keyword3` |
| `meta_description` | Meta-Beschreibungen bieten einen kurzen Überblick über das Produkt für Suchergebnislisten. Idealerweise sollte eine Meta-Beschreibung zwischen 150 und 160 Zeichen lang sein, obwohl das Feld bis zu 255 Zeichen akzeptiert. |
| `base_image` | Der relative Pfad für das Hauptbild auf der Produktseite. Commerce speichert Dateien intern in einer alphabetischen Ordnerstruktur. Sie können die exakte Position jedes Bildes in den exportierten Daten sehen. Beispiel: `/sample_data/m/b/mb01-blue-0.jpg`<br/>Um ein neues Bild hochzuladen oder ein vorhandenes Bild zu überschreiben, geben Sie den Dateinamen ein, dem ein Schrägstrich vorangestellt ist. Beispiel: `/image.jpg` |
| `base_image_label` | Die mit dem Basisbild verknüpfte Beschriftung. |
| `small_image` | Der Dateiname des kleinen Bildes, das auf Katalogseiten verwendet wird, gefolgt von einem Schrägstrich. Beispiel: `/image.jpg` |
| `small_image_label` | Die mit dem kleinen Bild verknüpfte Bezeichnung. Beispiel: `Small Image 1`, `Small Image 2` |
| `thumbnail_image` | Die Dateinamen von Miniaturbildern, die in der Galerie auf der Produktseite angezeigt werden sollen, gefolgt von einem Schrägstrich. Beispiel: `/image.jpg` |
| `thumbnail_image_label` | Die mit Miniaturbildern verknüpfte Bezeichnung. Beispiel: `Thumbnail 1`, `Thumbnail 2` |
| `created_at` | Gibt das Datum der Erstellung des Produkts an. Das Datum wird automatisch bei der Erstellung des Produkts generiert, kann aber später bearbeitet werden. |
| `updated_at` | Gibt das Datum der letzten Aktualisierung des Produkts an. |
| `new_from_date` | Gibt das &quot;Von&quot;-Datum für neue Produktlisten an und bestimmt, ob das Produkt als neues Produkt präsentiert wird. |
| `new_to_date` | Gibt das &quot;bis&quot;-Datum für neue Produktlisten an und bestimmt, ob das Produkt als neues Produkt präsentiert wird. |
| `display_product_options_in` | Wenn das Produkt mehrere Optionen hat, bestimmt, wo sie auf der Produktseite angezeigt werden. Werte: Spalte &quot;Produktinformationen&quot;/&quot;Block&quot;nach der Spalte &quot;Info&quot; |
| `map_price` | Der beworbene Mindestpreis des Produkts. (Wird nur angezeigt, wenn MAP aktiviert ist.) |
| `msrp_price` | Der vom Hersteller vorgeschlagene Einzelhandelspreis für das Produkt. (Wird nur angezeigt, wenn MAP aktiviert ist.) |
| `map_enabled` | Bestimmt, ob der Mindestpreis für Werbung in der Konfiguration aktiviert ist. Werte:<br/>`1` — (Ja) MAP ist aktiviert.<br/>`0` (oder leer) — (Nein) MAP ist nicht aktiviert. |
| `gift_message_available` | Bestimmt, ob eine Geschenknachricht beim Produktkauf enthalten sein kann. Werte:<br/>`1` — (Ja) Die Option, eine Geschenknachricht einzuschließen, wird dem Kunden angezeigt.<br/>`0` (oder leer) - (Nein) Die Option, eine Geschenknachricht einzuschließen, wird dem Kunden nicht angezeigt. |
| `custom_design` | Listet die verfügbaren Designs auf, die auf die Produktseite angewendet werden können. |
| `custom_design_from` | Gibt das Anfangsdatum an, an dem das ausgewählte Design auf die Produktseite angewendet wird. |
| `custom_design_to` | Gibt das Enddatum an, an dem das ausgewählte Design auf die Produktseite angewendet wird. |
| `custom_layout_update` | Zusätzlicher XML-Code, der als Layout-Update auf die Produktseite angewendet wird. |
| `page_layout` | Legt das Seitenlayout der Produktseite fest. Werte:<br/>`No layout updates` — Das Seitenlayout wird nicht geändert.<br/>`1 column` — Wendet ein einspaltiges Layout auf die Produktseite an.<br/>`2 columns with left bar` — Wendet ein zweispaltiges Layout mit einer linken Seitenleiste auf die Produktseite an.<br/>`2 columns with right bar` — Wendet ein zweispaltiges Layout mit einer rechten Seitenleiste auf die Produktseite an.<br/>`3 columns` — Wendet ein dreiseitiges Layout auf die Produktseite an.<br/>`empty` — Wendet ein leeres Layout auf die Produktseite an. |
| `product_options_container` | Wenn das Produkt mehrere Optionen hat, bestimmt, wo sie auf der Produktseite angezeigt werden. Werte: Spalte &quot;Produktinformationen&quot;/&quot;Block&quot;nach der Spalte &quot;Info&quot; |
| `msrp_display_actual_price_type` | Bestimmt, wo der tatsächliche Preis eines Produkts für den Kunden sichtbar ist. Werte:<br/>`In Cart` — Zeigt den tatsächlichen Produktpreis im Warenkorb an.<br/>`Before Order Confirmation` — Zeigt den tatsächlichen Produktpreis am Ende des Checkout-Prozesses an, kurz bevor die Bestellung bestätigt wird.<br/>`On Gesture` — Zeigt den tatsächlichen Produktpreis in einem Popup an, wenn der Kunde auf die _Zum Preis hier klicken_ oder _Was ist das?_ -Link. |
| `country_of_manufacture` | Identifiziert das Land, in dem das Produkt hergestellt wurde. |
| `additional_attributes` | Zusätzliche Attribute, die für das Produkt erstellt wurden. Beispiel: <br/>`has_options=0,required_options=0color=Black,has_options=0,required_options=0,size_general=XS` |
| `qty` | Die Menge des Produkts, die derzeit auf Lager ist. |
| `out_of_stock_qty` | Die Lagerposition, die bestimmt, ob das Produkt nicht vorrätig ist. |
| `use_config_min_qty` | Bestimmt, ob der Standardwert aus der Konfiguration verwendet wird, und entspricht dem Kontrollkästchen &quot;Use Config Settings&quot;. Werte:<br/>`1` — (Ja) Die standardmäßige Konfigurationseinstellung wird für den Wert dieses Attributs verwendet.<br/>`0` (oder leer) - (Nein) Die Standardkonfiguration kann für den Wert dieses Attributs überschrieben werden. |
| `is_qty_decimal` | Bestimmt, ob das Attribut qty einen Dezimalwert hat. Werte:<br/>`1` — (Ja) Der Wert des Attributs qty ist ein Dezimalwert.<br/>`0` (oder leer) — (Nein) Der Wert des Attributs qty ist eine ganze Zahl (Integer). |
| `allow_backorders` | Bestimmt, ob in Ihrem Store Rückstände zulässig sind und wie diese verwaltet werden. |
| `use_config_backorders` | Bestimmt, ob die standardmäßige Konfigurationseinstellung für Rückorder verwendet wird, und entspricht dem Status des Kontrollkästchens &quot;Use Config Settings&quot;. Werte:<br/>`1` — (Ja) Der Wert des Attributs qty ist ein Dezimalwert.<br/>`0` (oder leer) — (Nein) Der Wert des Attributs qty ist eine ganze Zahl (Integer). |
| `min_cart_qty` | Gibt die Mindestmenge des Artikels an, der in einer Bestellung erworben werden kann. |
| `use_config_min_sale_qty` | Bestimmt, ob die standardmäßige Konfigurationseinstellung für die Mindestmenge verwendet wird, und entspricht dem Status des Kontrollkästchens &quot;Use Config Settings&quot;. Werte:<br/>`1` — (Ja)<br/>`0` (oder leer) — (Nein) |
| `max_cart_qty` | Gibt die maximale Menge des Produkts an, die in einer Bestellung erworben werden kann. |
| `use_config_max_sale_qty` | Bestimmt, ob die standardmäßige Konfigurationseinstellung für die maximale Menge verwendet wird, und entspricht dem Status des Kontrollkästchens &quot;Use Config Settings&quot;. Werte:<br/>`1` — (Ja)<br/>`0` (oder leer) — (Nein) |
| `is_in_stock` | Gibt an, ob das Produkt vorrätig ist. |
| `notify_on_stock_below` | Gibt den Lagerbestand an, den Trigger und _nicht vorrätig_ Benachrichtigung. |
| `use_config_notify_stock_qty` | Bestimmt, ob die Standardkonfigurationseinstellung für die Benachrichtigung auf Lagerbestandsebene verwendet wird, und entspricht dem Status des Kontrollkästchens &quot;Use Config Settings&quot;. Werte:<br/>`1` — (Ja)<br/>`0` (oder leer) — (Nein) |
| `manage_stock` | Bestimmt, ob die Bestandskontrolle zur Verwaltung des Produkts verwendet wird. Werte:<br/>`1` — (Ja) Aktiviert die vollständige Bestandskontrolle, um die Lagerbestände des Produkts zu verwalten.<br/>`0` (oder leer) — (Nein) Das System verfolgt nicht die Anzahl der derzeit auf Lager befindlichen Artikel. |
| `use_config_manage_stock` | Bestimmt, ob die Standardkonfigurationseinstellung für die Verwaltung von Lagern verwendet wird, und entspricht dem Status des Kontrollkästchens &quot;Use Config Settings&quot;. Werte:<br/>`1` — (Ja)<br/>`0` (oder leer) — (Nein) |
| `use_config_qty_increments` | Bestimmt, ob die standardmäßige Konfigurationseinstellung für Mengenerhöhungen verwendet wird, und entspricht dem Status des Kontrollkästchens &quot;Use Config Settings&quot;. Werte:<br/>`1` — (Ja)<br/>`0` (oder leer) — (Nein) |
| `qty_increments` | Legt die Anzahl der Produkte fest, aus denen eine Mengenerhöhung besteht. |
| `use_config_enable_qty_inc` | Bestimmt, ob die Standardkonfigurationseinstellung zum Aktivieren von Mengenerhöhungen verwendet wird, und entspricht dem Status des Kontrollkästchens &quot;Use Config Settings&quot;. Werte:<br/>`1` — (Ja)<br/>`0` (oder leer) — (Nein) |
| `enable_qty_increments` | Bestimmt, ob Mengenerhöhungen für das Produkt aktiviert sind. |
| `is_decimal_divided` | Bestimmt, ob Teile des Produkts separat ausgeliefert werden können. Optionen: `Yes` / `No` |
| `website_id` | Bei Installationen mit mehreren Websites gibt eine bestimmte Website an, auf der das Produkt verfügbar ist. Wenn das Feld leer ist, ist das Produkt auf allen Websites verfügbar. |
| `related_skus` | Führt die SKU jedes Produkts auf, das als verwandtes Produkt identifiziert wurde. Beispiel: `24-WG080,24-UG03,24-UG01,24-UG02` |
| `related_position` | Bestimmt die Position (Sortierreihenfolge) der SKUs, die in der Spalte related_skus als verwandte Produkte aufgeführt sind. Beispiel: `1,2,3,4` |
| `crosssell_skus` | Führt die SKU jedes Produkts auf, das als Crosssell identifiziert wurde. |
| `crosssell_position` | Bestimmt die Position (Sortierreihenfolge) der SKUs, die in der Variablen `crosssell_skus` Spalte. |
| `upsell_skus` | Führt die SKU jedes Produkts auf, das als Up Sell identifiziert wurde. |
| `upsell_position` | Bestimmt die Position (Sortierreihenfolge) der SKUs, die in der Variablen `upsell_skus` Spalte. |
| `additional_images` | Die Dateinamen aller zusätzlichen Bilder, die mit dem Produkt verknüpft werden sollen, gefolgt von einem Schrägstrich. Beispiel: `/image.jpg` |
| `additional_image_labels` | Die Beschriftungen, die mit weiteren Bildern verknüpft sind. Beispiel: `Label 1`, `Label 2` |
| `custom_options` | Gibt die Eigenschaften und Werte an, die jeder benutzerdefinierten Option zugewiesen sind. Beispiel: <br/>`name=Color, type=drop_down, required=1, price= price_type=fixed, sku=, option_title=Black|name=Color, type=drop_down, required=1, price=, price_type=fixed, sku=, option_title=White` |

{style="table-layout:auto"}

## Servicedaten für Produktvarianten

| Attribut | Beschreibung | Gilt für |
|--- |--- | --- |
| `_super_products_sku` | Die generierte SKU für eine konfigurierbare Produktvariante. Beispiel: WB03-XS-Green | Konfigurierbare Produkte |
| `_super_attribute_code` | Der Attributcode einer konfigurierbaren Produktvariante. Beispiel: Farbe | Konfigurierbare Produkte |
| `_super_attribute_option` | Der -Wert einer konfigurierbaren Produktvariante. Beispiel: grün | Konfigurierbare Produkte |
| `_super_attribute_price_corr` | Eine Preisanpassung, die mit einer konfigurierbaren Produktvariante verbunden ist. | Konfigurierbare Produkte |
| `_associated_sku` | Die SKU eines Produkts, das mit einem gruppierten Produkt verknüpft ist. | Gruppierungsprodukte <br/>Bundle-Produkte |
| `_associated_default_qty` | Bestimmt die Menge des zugehörigen Produkts, das eingeschlossen ist. | Konfigurierbare Produkte<br/>Gruppierungsprodukte<br/>Bundle-Produkte |
| `_associated_position` | Bestimmt die Position des verknüpften Produkts, wenn es mit anderen verknüpften Produkten aufgeführt wird. | Konfigurierbare Produkte<br/>Gruppierungsprodukte<br/>Bundle-Produkte |

{style="table-layout:auto"}

## Komplexe Produktdatenattribute

Der Begriff &quot;komplexe Daten&quot;bezieht sich auf die Daten, die mit mehreren Produktoptionen verknüpft sind. Die folgenden Produktarten verwenden Daten, die aus separaten Produkten stammen, um Produkvarianten und mehrere Optionen zu erstellen.

- [Konfigurierbar](../catalog/product-create-configurable.md)
- [gruppiert](../catalog/product-create-grouped.md)
- [Paket](../catalog/product-create-bundle.md)

Wenn Sie ein konfigurierbares Produkt exportieren, finden Sie die Standardattribute, aus denen ein einfaches Produkt besteht, sowie die zusätzlichen Attribute, die zum Verwalten komplexer Daten erforderlich sind.

![Konfigurierbares Produkt - exportierte Daten](./assets/data-exported-configurable-product.png){width="600" zoomable="yes"}

### Konfigurierbare Produkte

| Attribut | Beschreibung |
|--- |--- |
| `configurable_variation_labels` | Beschriftungen, die Produktvarianten identifizieren. Beispiel: `Choose Color:` oder `Choose Size:` |
| `configurable_variations` | Beschreibt die Werte, die mit einer Produktvariante verknüpft sind. Beispiel: `sku=sku-red xs,color=red,size=xs,price=10.99,display=1,image=/pub/media/import/image1.png|sku=sku-red-m,color=red,size=m,price=20.88,display=1,image=/pub/media/import/image2.png` |

{style="table-layout:auto"}

### Gruppierungsprodukte

| Attribut | Beschreibung |
|--- |--- |
| `associated_skus` | Identifiziert die SKUs der einzelnen Produkte, aus denen die Gruppe besteht. |

{style="table-layout:auto"}

### Paketprodukte

| Attribut | Beschreibung |
|--- |--- |
| `bundle_price_type` | Bestimmt, ob der Preis eines Bundle-Elements fest oder dynamisch ist. |
| `bundle_sku_type` | Bestimmt, ob jedem Element eine Variable und dynamische SKU zugewiesen wird oder ob eine feste SKU für das Bundle verwendet wird. Optionen: Festgelegt/Dynamisch |
| `bundle_weight_type` | Bestimmt, ob die Gewichtung eines Bundle-Elements variabel oder fest ist. |
| `bundle_values` | Beschreibt den mit einer Bundle-Option verknüpften Lehrwert. Beispiel: `name=Bundle Option One,type=dropdown; required=1, sku=sku-option2,price=10, price_type=fixed` |

{style="table-layout:auto"}

## Erweiterte Preisattribute

Mit dem erweiterten Preis-Import/-Export können Sie die Preisinformationen für Produktgruppen und Tier-Preise schnell aktualisieren. Der Prozess [importieren](data-import.md) und [export](data-export.md) erweiterte Preisdaten sind mit allen anderen Entitätstypen identisch. Die CSV-Beispieldatei enthält Tier- und Gruppenpreise für jeden Produkttyp, der erweiterte Preise unterstützt. Eine Änderung der erweiterten Preisgestaltung wirkt sich nicht auf den Rest des Produktdatensatzes aus.

![Beispiel-Exportdaten - erweiterte Preisgestaltung](./assets/data-advanced-pricing-export-sample.png){width="600" zoomable="yes"}

| Attribut | Beschreibung |
|--- |--- |
| `sku` | (Erforderlich) Die Bestandseinheit ist eine eindeutige alphanumerische Kennung, die zur Bestandsverfolgung verwendet wird. Eine SKU kann bis zu 64 Zeichen lang sein. Beispiel: `sku123`<br/>**_Hinweis:_**Eine SKU, die länger als 64 Zeichen ist, führt dazu, dass der Import fehlschlägt. |
| `tier_price_website` | Die [Website-Code](../stores-purchase/stores.md#add-websites) gibt jede Website an, auf der die Tier-Preise verfügbar sind. Beispiel: `-  website1 -  All Websites [USD]` |
| `tier_price_customer` | Identifiziert die [Kundengruppen](../customers/customer-groups.md) wo die Tier-Preise verfügbar sind. Beispiel: `-  ALL GROUPS -  NOT LOGGED IN -  General -  Wholesale -  Retailer` |
| `tier_price_customer_group` | Identifiziert die Kundengruppen, für die Tierpreise verfügbar sind. Beispiel: `-  ALL GROUPS -  NOT LOGGED IN -  General -  Wholesale -  Retailer` |
| `tier_price_qty` | Die Menge des Produkts, die bestellt werden muss, um den Tier-Preisnachlass zu erhalten. |
| `tier_price` | Der abgezinste Tier-Preis des Produkts. Für [Paket-Produkte](../catalog/product-create-bundle.md), wird der Ebenenpreis als Prozentsatz berechnet. |
| `group_price_website` | Die [Website-Code](../stores-purchase/stores.md#add-websites) auf jeder Website, auf der Gruppenpreise verfügbar sind. Wenn Sie mehrere Websites angeben, trennen Sie jede durch ein Komma und ohne Leerzeichen. Beispiel: `-  website1 -  All Websites [USD]` |
| `group_price_customer_group` | Identifiziert die Gruppen der Kunden, für die Gruppenpreise verfügbar sind. Beispiel: `-  NOT LOGGED IN -  General -  Wholesale -  Retailer` |
| `group_price` | Der abgezinste Gruppenpreis des Produkts. Für [Paket-Produkte](../catalog/product-create-bundle.md)wird der Gruppenpreis als Prozentsatz berechnet. |

{style="table-layout:auto"}
