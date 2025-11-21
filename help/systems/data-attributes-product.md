---
title: Referenz zu Produktdatenattributen
description: Verwenden Sie diese Referenz von Produktdatenattributen, wenn Sie mit Produktdatenimporten und -exporten arbeiten.
exl-id: 9ffa4d1f-cbf8-4a08-bb79-33f21e698a74
feature: Products, Attributes
source-git-commit: 3d02b1f6b3051aab133a57497bd0c30ac60bffde
workflow-type: tm+mt
source-wordcount: '2496'
ht-degree: 0%

---

# Referenz zu Produktdatenattributen

In der folgenden Tabelle sind die Attribute eines typischen Produktexports in der Standardreihenfolge aufgeführt, in der sie angezeigt werden. Jedes Attribut wird in der CSV-Datei als Spalte dargestellt, und Produktdatensätze werden durch Zeilen dargestellt. Spalten, die mit einem Unterstrich beginnen, enthalten Service-Daten wie Eigenschaften oder Optionswerte für komplexe Daten. Sie können [ Produkt ](data-export.md) Ihrem Katalog exportieren, um zu sehen, wie die einzelnen Attribute in den Daten dargestellt werden.

Auf der zum Exportieren dieser Daten verwendeten Installation sind die Beispieldaten installiert, außerdem sind dort zwei Websites und mehrere Store-Ansichten vorhanden. Obwohl diese Liste alle Spalten enthält, die normalerweise exportiert werden, ist die `sku` der einzige erforderliche Wert. Um Daten zu importieren, können Sie nur die Spalten mit Änderungen einbeziehen. Die `sku` sollte die erste Spalte sein, aber die Reihenfolge der übrigen Attribute spielt keine Rolle.

## Einfache CSV-Produktdateistruktur

| Attribut | Beschreibung |
|--- |--- |
| `sku` | (Erforderlich) Die Stock-Keeping-Unit ist eine eindeutige alphanumerische Kennung, die zur Nachverfolgung des Bestands verwendet wird. Eine SKU kann bis zu 64 Zeichen lang sein. Beispiel: `sku123`<br/>**_Hinweis:_** Eine SKU mit mehr als 64 Zeichen führt dazu, dass der Import fehlschlägt. |
| `store_view_code` | Gibt die spezifischen Store-Ansichten an, in denen das Produkt verfügbar ist. Wenn dies leer ist, ist das Produkt in der standardmäßigen Store-Ansicht verfügbar. Beispiel: `storeview1`, `english`, `spanish` |
| `attribute_set_code` | Weist das Produkt je nach Produkttyp einem bestimmten Attributsatz oder einer bestimmten Produktvorlage zu. Beispiel: `default`<br><br>Nachdem das Produkt erstellt wurde, kann der Attributsatz nicht mehr mit der Importfunktion geändert werden. Sie können jedoch über die Administratorin bzw. den Administrator das Attribut ändern und das Produkt erneut exportieren, um die CSV-Datei zu aktualisieren. |
| `product_type` | Gibt den Produkttyp an. Werte:<br/>`simple` — Sachgüter, die in der Regel als einzelne Einheiten oder in festen Mengen verkauft werden.<br/>`grouped` - Eine Gruppe separater Produkte, die als Set verkauft werden.<br/>`configurable` - Ein Produkt mit mehreren Optionen, die der Kunde vor dem Kauf auswählen muss. Der Bestand kann für jeden Variantensatz verwaltet werden, da er ein separates Produkt mit einer unterschiedlichen SKU darstellt. Beispielsweise ist eine Kombination aus Farbe und Größe für ein konfigurierbares Produkt mit einer bestimmten SKU im Katalog verknüpft.<br/>`virtual` — Ein nicht materielles Produkt, das nicht versendet werden muss und nicht im Inventar aufbewahrt wird. Beispiele sind Services, Mitgliedschaften und Abonnements.<br/>`bundle` - Ein anpassbarer Produktsatz einfacher Produkte, die zusammen verkauft werden. |
| `categories` | Gibt jede Kategorie an, die dem Produkt zugewiesen ist. Trennen Sie Kategorien und Unterkategorien mit einem Schrägstrich. Um mehrere Kategoriepfade anzugeben, trennen Sie jeden Pfad mit einem senkrechten Strich \| Symbol. Beispiel: `Default Category/Gear\|Default Category/Gear/Bags` |
| `product_websites` | Der Website-Code jeder Website, auf der das Produkt verfügbar ist. Ein einzelnes Produkt kann mehreren Websites zugewiesen oder auf eine Website beschränkt werden. Wenn Sie mehrere Websites angeben, trennen Sie sie jeweils durch ein Komma und ohne Leerzeichen. Beispiel: `base` oder `base,website2` |
| `name` | Der Produktname wird in allen Produktlisten angezeigt und ist der Name, mit dem Kunden das Produkt identifizieren. |
| `description` | Die Produktbeschreibung enthält detaillierte Informationen zum Produkt und kann einfache HTML-Tags enthalten. |
| `short_description` | Die Verwendung der kurzen Produktbeschreibung hängt vom Thema ab. Es kann in Produktlisten angezeigt werden und wird manchmal in RSS-Feed-Listen verwendet, die an Shopping-Sites gesendet werden. |
| `weight` | Das Gewicht des einzelnen Produkts. Das tatsächliche Produktgewicht wird vom Spediteur zum Zeitpunkt des Versands bestimmt. |
| product_online | Bestimmt, ob das Produkt im Geschäft zum Verkauf verfügbar ist. Werte: <br/>`1` - (Ja) Das Produkt ist aktiviert und zum Verkauf verfügbar.<br/>`2` — (Nein) Das Produkt ist deaktiviert und nicht erhältlich. |
| `tax_class_name` | Der Name der Steuerklasse, die mit diesem Produkt verknüpft ist. |
| `visibility` | Bestimmt, ob das Produkt im Katalog sichtbar und für die Suche verfügbar ist. Werte: <br/>`Not Visible Individually` — Das Produkt ist nicht in den Produktlisten enthalten, obwohl es als eine Variante eines anderen Produkts verfügbar sein könnte.<br/>`Catalog` - Das Produkt wird in allen Kataloglisten angezeigt.<br/>`Search` - Das Produkt ist für Suchvorgänge verfügbar.<br/>`Catalog, Search` - Das Produkt ist in den Katalogen enthalten und steht auch zur Suche zur Verfügung. |
| `price` | Der Preis, zu dem das Produkt in Ihrem Geschäft zum Verkauf angeboten wird. |
| `special_price` | Der abgezinste Preis des Produkts während des angegebenen Datumsbereichs. |
| `special_price_from_date` | Das Anfangsdatum des Zeitraums, in dem der Sonderpreis in Kraft ist. |
| `special_price_to_date` | Das letzte Datum des Zeitraums, in dem der Sonderpreis in Kraft ist. |
| `url_key` | Der Teil der URL, der das Produkt identifiziert. Der Standardwert basiert auf dem Produktnamen. Beispiel: `product-name` |
| save_rewrites_history | Wenn der Wert `1` mit einer neuen `url_key` angegeben wird, wird eine neue 301-URL-Umschreibung generiert, sodass die alte URL an die neue URL umgeleitet wird. |
| `meta_title` | Der Meta-Titel wird in der Titelleiste und auf der Registerkarte der Browser- und Suchergebnislisten angezeigt. Der Meta-Titel sollte für das Produkt eindeutig sein, hochwertige Keywords enthalten und weniger als 70 Zeichen lang sein. |
| `meta_keywords` | Meta-Keywords sind nur für Suchmaschinen sichtbar und werden von einigen Suchmaschinen ignoriert. Wählen Sie Schlüsselwörter mit hohem Wert aus, getrennt durch ein Komma. Beispiel: `keyword1`, `keyword2`, `keyword3` |
| `meta_description` | Meta-Beschreibungen bieten einen kurzen Überblick über das Produkt für die Auflistung von Suchergebnissen. Eine Meta-Beschreibung sollte idealerweise zwischen 150 und 160 Zeichen lang sein, obwohl das Feld bis zu 255 Zeichen lang sein kann. |
| `base_image` | Der relative Pfad für das Hauptbild auf der Produktseite. Commerce speichert Dateien intern in einer alphabetischen Ordnerstruktur. Sie können die genaue Position der einzelnen Bilder in den exportierten Daten sehen. Beispiel: `/sample_data/m/b/mb01-blue-0.jpg`<br/>Um ein neues Bild hochzuladen oder über ein vorhandenes Bild zu schreiben, geben Sie den Dateinamen ein, gefolgt von einem Schrägstrich. Beispiel: `/image.jpg` |
| `base_image_label` | Die Bezeichnung, die dem Basisbild zugeordnet ist. |
| `small_image` | Der Dateiname des kleinen Bildes, das auf Katalogseiten verwendet wird, mit vorangestelltem Schrägstrich. Beispiel: `/image.jpg` |
| `small_image_label` | Der Titel, der mit dem kleinen Bild verknüpft ist. Beispiel: `Small Image 1`, `Small Image 2` |
| `thumbnail_image` | Die Dateinamen von Miniaturbildern, die in der Galerie auf der Produktseite angezeigt werden sollen, mit vorangestelltem Schrägstrich. Beispiel: `/image.jpg` |
| `thumbnail_image_label` | Der Titel, der mit allen Miniaturbildern verknüpft ist. Beispiel: `Thumbnail 1`, `Thumbnail 2` |
| `created_at` | Gibt das Datum an, an dem das Produkt erstellt wurde. Das Datum wird bei der Erstellung des Produkts automatisch generiert, kann aber später bearbeitet werden. |
| `updated_at` | Gibt das Datum an, an dem das Produkt zuletzt aktualisiert wurde. |
| `new_from_date` | Gibt das „Von“-Datum für neue Produktlisten an und bestimmt, ob das Produkt als neues Produkt angezeigt wird. |
| `new_to_date` | Gibt das „Bis“-Datum für neue Produktlisten an und bestimmt, ob das Produkt als neues Produkt angezeigt wird. |
| `display_product_options_in` | Wenn das Produkt über mehrere Optionen verfügt, bestimmt , wo diese auf der Produktseite angezeigt werden. Werte: Produktinformationsspalte / -block nach der Informationsspalte |
| `map_price` | Der mindestens angezeigte Preis des Produkts. (Diese Option ist nur verfügbar, wenn MAP aktiviert ist.) |
| `msrp_price` | Der vom Hersteller vorgeschlagene Verkaufspreis für das Produkt. (Diese Option ist nur verfügbar, wenn MAP aktiviert ist.) |
| `map_enabled` | Legt fest, ob der Mindestpreis für Werbung in der Konfiguration aktiviert ist. Werte: <br/>`1` - (Ja) MAP ist aktiviert.<br/>`0` (oder leer) - (Keine) MAP ist nicht aktiviert. |
| `gift_message_available` | Legt fest, ob eine Geschenknachricht in den Produktkauf aufgenommen werden kann. Werte: <br/>`1` - (Ja) Die Option zum Einschließen einer Geschenknachricht wird dem Kunden angezeigt.<br/>`0` (oder leer) - (Nein) Die Option, eine Geschenknachricht einzuschließen, wird dem Kunden nicht angezeigt. |
| `custom_design` | Listet die verfügbaren Designs auf, die auf die Produktseite angewendet werden können. |
| `custom_design_from` | Gibt das Anfangsdatum an, an dem das ausgewählte Design auf die Produktseite angewendet wird. |
| `custom_design_to` | Gibt das Enddatum an, an dem das ausgewählte Design auf die Produktseite angewendet wird. |
| `custom_layout_update` | Zusätzlicher XML-Code, der als Layout-Aktualisierung auf die Produktseite angewendet wird. |
| `page_layout` | Bestimmt das Seiten-Layout der Produktseite. Werte: <br/>`No layout updates` — Am Seiten-Layout wird keine Änderung vorgenommen.<br/>`1 column` - Wendet ein einspaltiges Layout auf die Produktseite an.<br/>`2 columns with left bar` - Wendet ein zweispaltiges Layout mit einer linken Seitenleiste auf die Produktseite an.<br/>`2 columns with right bar` - Wendet ein zweispaltiges Layout mit einer rechten Seitenleiste auf die Produktseite an.<br/>`3 columns` - Wendet ein dreispaltiges Layout auf die Produktseite an.<br/>`empty` - Wendet ein leeres Layout auf die Produktseite an. |
| `product_options_container` | Wenn das Produkt über mehrere Optionen verfügt, bestimmt , wo diese auf der Produktseite angezeigt werden. Werte: Produktinformationsspalte / -block nach der Informationsspalte |
| `msrp_display_actual_price_type` | Bestimmt, wo der tatsächliche Preis eines Produkts für den Kunden sichtbar ist. Werte:<br/>`In Cart` - Zeigt den tatsächlichen Produktpreis im Warenkorb an.<br/>`Before Order Confirmation` - Zeigt den tatsächlichen Produktpreis am Ende des Checkout-Prozesses an, kurz bevor die Bestellung bestätigt wird.<br/>`On Gesture` - Zeigt den tatsächlichen Produktpreis in einem Popup an, wenn der Kunde auf den _Klick für Preis_ oder _Was ist das?Link_. |
| `country_of_manufacture` | Angabe des Landes, in dem das Produkt hergestellt wurde. |
| `additional_attributes` | Zusätzliche Attribute für das Produkt erstellt. Beispiel: <br/>`has_options=0,required_options=0color=Black,has_options=0,required_options=0,size_general=XS` |
| `qty` | Die Menge des Produkts, die derzeit auf Lager ist. |
| `out_of_stock_qty` | Die Lagerebene, die bestimmt, ob das Produkt nicht vorrätig ist. |
| `use_config_min_qty` | Bestimmt, ob der Standardwert aus der Konfiguration verwendet wird, und entspricht dem Kontrollkästchen „Konfigurationseinstellungen verwenden“. Werte: <br/>`1` - (Ja) Die Standardkonfigurationseinstellung wird für den Wert dieses Attributs verwendet.<br/>`0` (oder leer) - (Nein) Die Standardkonfiguration kann für den Wert dieses Attributs überschrieben werden. |
| `is_qty_decimal` | Bestimmt, ob das Mengenattribut einen Dezimalwert aufweist. Werte: <br/>`1` - (Ja) Der Wert des Attributs „quantity“ ist ein Dezimalwert.<br/>`0` (oder leer) - (Nein) Der Wert des Attributs „quantity“ ist eine Ganzzahl (Integer). |
| `allow_backorders` | Legt fest, ob Ihr Store Auftragsrückstände zulässt und wie diese verwaltet werden. |
| `use_config_backorders` | Bestimmt, ob die standardmäßige Konfigurationseinstellung für Backorders verwendet wird, und entspricht dem Status des Kontrollkästchens Konfigurationseinstellungen verwenden . Werte: <br/>`1` - (Ja) Der Wert des Attributs „quantity“ ist ein Dezimalwert.<br/>`0` (oder leer) - (Nein) Der Wert des Attributs „quantity“ ist eine Ganzzahl (Integer). |
| `min_cart_qty` | Gibt die Mindestmenge des Artikels an, die in einem einzelnen Auftrag gekauft werden kann. |
| `use_config_min_sale_qty` | Bestimmt, ob die Standardkonfigurationseinstellung für die Mindestmenge verwendet wird, und entspricht dem Status des Kontrollkästchens Konfigurationseinstellungen verwenden . Werte:<br/>`1` — (Ja)<br/>`0` (oder leer) — (Nein) |
| `max_cart_qty` | Gibt die maximale Menge des Produkts an, die in einer einzelnen Bestellung gekauft werden kann. |
| `use_config_max_sale_qty` | Bestimmt, ob die standardmäßige Konfigurationseinstellung für die maximale Menge verwendet wird, und entspricht dem Status des Kontrollkästchens Konfigurationseinstellungen verwenden . Werte:<br/>`1` — (Ja)<br/>`0` (oder leer) — (Nein) |
| `is_in_stock` | Gibt an, ob das Produkt auf Lager ist. |
| `notify_on_stock_below` | Gibt die Lagerstufe an, für die eine Benachrichtigung _nicht vorrätig_ Trigger wird. |
| `use_config_notify_stock_qty` | Legt fest, ob die Standardkonfigurationseinstellung für die Benachrichtigung auf Trigger-Stock-Ebene verwendet wird, und entspricht dem Status des Kontrollkästchens Konfigurationseinstellungen verwenden . Werte:<br/>`1` — (Ja)<br/>`0` (oder leer) — (Nein) |
| `manage_stock` | Legt fest, ob die Bestandskontrolle zur Verwaltung des Produkts verwendet wird. Werte: <br/>`1` — (Ja) Aktiviert die vollständige Bestandskontrolle, um die Lagerbestände des Produkts zu verwalten.<br/>`0` (oder leer) - (Nein) Das System verfolgt nicht die Anzahl der Artikel, die derzeit auf Lager sind. |
| `use_config_manage_stock` | Bestimmt, ob die standardmäßige Konfigurationseinstellung für die Verwaltung von Stock verwendet wird, und entspricht dem Status des Kontrollkästchens Konfigurationseinstellungen verwenden . Werte:<br/>`1` — (Ja)<br/>`0` (oder leer) — (Nein) |
| `use_config_qty_increments` | Bestimmt, ob die Standardkonfigurationseinstellung für Mengeninkremente verwendet wird, und entspricht dem Status des Kontrollkästchens Konfigurationseinstellungen verwenden . Werte:<br/>`1` — (Ja)<br/>`0` (oder leer) — (Nein) |
| `qty_increments` | Bestimmt die Anzahl der Produkte, aus denen ein Mengenzuwachs besteht. |
| `use_config_enable_qty_inc` | Bestimmt, ob die Standardkonfigurationseinstellung zum Aktivieren von Mengeninkrementen verwendet wird und dem Status des Kontrollkästchens Konfigurationseinstellungen verwenden entspricht. Werte:<br/>`1` — (Ja)<br/>`0` (oder leer) — (Nein) |
| `enable_qty_increments` | Bestimmt, ob Mengeninkremente für das Produkt aktiviert sind. |
| `is_decimal_divided` | Legt fest, ob Teile des Produkts separat versendet werden können. Optionen: `Yes` / `No` |
| `website_id` | Bei Installationen mit mehreren Websites kennzeichnet eine bestimmte Website, auf der das Produkt verfügbar ist. Wenn dieses Feld leer bleibt, ist das Produkt auf allen Websites verfügbar. |
| `related_skus` | Listet die SKU jedes Produkts auf, das als verwandtes Produkt identifiziert wurde. Beispiel: `24-WG080,24-UG03,24-UG01,24-UG02` |
| `related_position` | Bestimmt die Position (Sortierreihenfolge) der SKUs, die in der Spalte related_skus als „Verknüpfte Produkte“ aufgeführt sind. Beispiel: `1,2,3,4` |
| `crosssell_skus` | Listet die SKU jedes Produkts auf, das als Crosssell identifiziert wurde. |
| `crosssell_position` | Bestimmt die Position (Sortierreihenfolge) der SKUs, die in der Spalte &quot;`crosssell_skus`&quot; als Crosssell-Produkte aufgeführt sind. |
| `upsell_skus` | Listet die SKU jedes Produkts auf, das als Upsell identifiziert wurde. |
| `upsell_position` | Bestimmt die Position (Sortierreihenfolge) der SKUs, die als Upsell-Produkte in der Spalte `upsell_skus` aufgeführt sind. |
| `additional_images` | Die Dateinamen aller zusätzlichen Bilder, die mit dem Produkt verknüpft werden sollen, mit vorangestelltem Schrägstrich. Beispiel: `/image.jpg` |
| `additional_image_labels` | Die Beschriftungen, die mit zusätzlichen Bildern verknüpft sind. Beispiel: `Label 1`, `Label 2` |
| `custom_options` | Gibt die Eigenschaften und Werte an, die jeder benutzerdefinierten Option zugewiesen sind. Beispiel: <br/>`name=Color, type=drop_down, required=1, price= price_type=fixed, sku=, option_title=Black|name=Color, type=drop_down, required=1, price=, price_type=fixed, sku=, option_title=White` |

{style="table-layout:auto"}

## Service-Daten für Produktvarianten

| Attribut | Beschreibung | Gilt für |
|--- |--- | --- |
| `_super_products_sku` | Die generierte SKU für eine konfigurierbare Produktvariante. Beispiel: WB03-XS-Green | Konfigurierbare Produkte |
| `_super_attribute_code` | Der Attributcode einer konfigurierbaren Produktvariante. Beispiel: Farbe | Konfigurierbare Produkte |
| `_super_attribute_option` | Der Wert einer konfigurierbaren Produktvariante. Beispiel: grün | Konfigurierbare Produkte |
| `_super_attribute_price_corr` | Eine Preisanpassung, die mit einer konfigurierbaren Produktvariante verknüpft ist. | Konfigurierbare Produkte |
| `_associated_sku` | Die SKU eines Produkts, das mit einem gruppierten Produkt verknüpft ist. | Gruppierte Produkte <br/>gebündelte Produkte |
| `_associated_default_qty` | Bestimmt die Menge des zugehörigen Produkts, das enthalten ist. | Konfigurierbare Produkte<br/>gruppierte Produkte<br/>gebündelte Produkte |
| `_associated_position` | Bestimmt die Position des zugehörigen Produkts, wenn es mit anderen zugehörigen Produkten aufgelistet wird. | Konfigurierbare Produkte<br/>gruppierte Produkte<br/>gebündelte Produkte |

{style="table-layout:auto"}

## Komplexe Produktdatenattribute

Der Begriff „komplexe Daten“ bezieht sich auf die Daten, die mit mehreren Produktoptionen verknüpft sind. Die folgenden Produkttypen verwenden Daten, die von separaten Produkten stammen, um Produktvarianten und mehrere Optionen zu erstellen.

- [Konfigurierbar](../catalog/product-create-configurable.md)
- [Gruppiert](../catalog/product-create-grouped.md)
- [Bündel](../catalog/product-create-bundle.md)

Wenn Sie ein konfigurierbares Produkt exportieren, finden Sie die Standardattribute, aus denen ein einfaches Produkt besteht, sowie die zusätzlichen Attribute, die zum Verwalten komplexer Daten erforderlich sind.

![Konfigurierbares Produkt - exportierte Daten](./assets/data-exported-configurable-product.png){width="600" zoomable="yes"}

### Konfigurierbare Produkte

| Attribut | Beschreibung |
|--- |--- |
| `configurable_variation_labels` | Beschriftungen, die Produktvarianten identifizieren. Beispiel: `Choose Color:` oder `Choose Size:` |
| `configurable_variations` | Beschreibt die Werte, die einer Produktvariante zugeordnet sind. Beispiel: `sku=sku-red xs,color=red,size=xs,price=10.99,display=1,image=/pub/media/import/image1.png|sku=sku-red-m,color=red,size=m,price=20.88,display=1,image=/pub/media/import/image2.png` |

{style="table-layout:auto"}

### Gruppierte Produkte

| Attribut | Beschreibung |
|--- |--- |
| `associated_skus` | Identifiziert die SKUs der einzelnen Produkte, aus denen die Gruppe besteht. |

{style="table-layout:auto"}

### Produkte im Paket

| Attribut | Beschreibung |
|--- |--- |
| `bundle_price_type` | Bestimmt, ob der Preis eines Paketelements fest oder dynamisch ist. |
| `bundle_sku_type` | Bestimmt, ob jedem Element eine Variable oder eine dynamische SKU zugewiesen ist oder ob eine feste SKU für das Bundle verwendet wird. Optionen: Fest/Dynamisch |
| `bundle_weight_type` | Bestimmt, ob die Gewichtung eines Bundle-Elements variabel oder fest ist. |
| `bundle_values` | Beschreibt den mit einer Bundle-Option verknüpften Unterrichtswert. Beispiel: `name=Bundle Option One,type=dropdown; required=1, sku=sku-option2,price=10, price_type=fixed` |

{style="table-layout:auto"}

## Erweiterte Preisattribute

Mit Advanced Price Import/Export können Sie die Preisinformationen für Produktgruppen und Stufenpreise schnell aktualisieren. Der Prozess zum [Importieren](data-import.md) und [Exportieren](data-export.md) der erweiterten Preisdaten ist derselbe wie bei jedem anderen Entitätstyp. Die CSV-Beispieldatei enthält Stufen- und Gruppenpreise für jeden Produkttyp, der erweiterte Preise unterstützt. Die Änderung der erweiterten Preisgestaltung wirkt sich nicht auf den Rest des Produktdatensatzes aus.

![Beispiel für den Datenexport - Erweiterte Preise](./assets/data-advanced-pricing-export-sample.png){width="600" zoomable="yes"}

| Attribut | Beschreibung |
|--- |--- |
| `sku` | (Erforderlich) Die Stock-Keeping-Unit ist eine eindeutige alphanumerische Kennung, die zur Nachverfolgung des Bestands verwendet wird. Eine SKU kann bis zu 64 Zeichen lang sein. Beispiel: `sku123`<br/>**_Hinweis:_** Eine SKU mit mehr als 64 Zeichen führt dazu, dass der Import fehlschlägt. |
| `tier_price_website` | Der [Website-Code](../stores-purchase/stores.md#add-websites) kennzeichnet jede Website, auf der Preisstufen verfügbar sind. Beispiel: `-  website1 -  All Websites [USD]` |
| `tier_price_customer` | Gibt die [Kundengruppen“ an](../customers/customer-groups.md) für die Preisstufen verfügbar sind. Beispiel: `-  ALL GROUPS -  NOT LOGGED IN -  General -  Wholesale -  Retailer` |
| `tier_price_customer_group` | Gibt die Kundengruppen an, für die Preisstufen verfügbar sind. Beispiel: `-  ALL GROUPS -  NOT LOGGED IN -  General -  Wholesale -  Retailer` |
| `tier_price_qty` | Die Menge des Produkts, die bestellt werden muss, um den Stufenpreisrabatt zu erhalten. |
| `tier_price` | Der diskontierte Stufenpreis des Produkts. Für [Paketprodukte](../catalog/product-create-bundle.md) wird der Stufenpreis als Prozentsatz berechnet. |
| `group_price_website` | Der [Website-Code](../stores-purchase/stores.md#add-websites) jeder Website, auf der Gruppenpreise verfügbar sind. Wenn Sie mehrere Websites angeben, trennen Sie sie jeweils durch ein Komma und ohne Leerzeichen. Beispiel: `-  website1 -  All Websites [USD]` |
| `group_price_customer_group` | Gibt die Kundengruppen an, für die Gruppenpreise verfügbar sind. Beispiel: `-  NOT LOGGED IN -  General -  Wholesale -  Retailer` |
| `group_price` | Der ermäßigte Gruppenpreis des Produkts. Für [Paketprodukte](../catalog/product-create-bundle.md) wird der Gruppenpreis als Prozentsatz berechnet. |

{style="table-layout:auto"}
