---
title: Liste der Produkte
description: Erfahren Sie mehr über die Seite _[!UICONTROL Products]_ im Admin, auf der Sie Produkte erstellen und vorhandene bearbeiten können.
exl-id: 47e14f72-017f-456a-8904-6d32ef47e6f1
feature: Catalog Management, Products, Admin Workspace
source-git-commit: 8bb91b80f8ba957676c654e984deb5704b777612
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 0%

---

# Liste der Produkte

Auf alle Produkte im Katalog kann über die Seite &quot;_[!UICONTROL Products]_&quot;in Admin zugegriffen werden. Dort können Sie Produkte erstellen und vorhandene bearbeiten. Für eine Installation auf mehreren Sites kann jede Website eine andere Auswahl von Produkten zum Verkauf aus demselben Katalog anbieten.

Die Liste _[!UICONTROL Products]_enthält alle Produkte im Katalog, zeigt die Websites an, auf denen sie verfügbar sind, und ob sie derzeit zum Verkauf angeboten werden. In Adobe Commerce-B2B-Installationen mit aktivierten [freigegebenen Katalogen](../b2b/catalog-shared.md) enthält das Raster eine Spalte, die angibt, welche Produkte in einem freigegebenen Katalog über alternative Rabattpreise verfügen.

Sie können die Listenseite nach Seite durchsuchen oder nach bestimmten Produkten suchen. Verwenden Sie die standardmäßigen [Steuerelemente](../getting-started/admin-grid-controls.md) zum Sortieren und Filtern der Liste und wenden Sie [Aktionen](../getting-started/admin-actions-control.md) auf ausgewählte Produkte an.

![Produktraster](./assets/products-grid.png){width="700" zoomable="yes"}

## Produktanzeige begrenzen

Um die Leistung bei großen Katalogen zu verbessern, wird empfohlen, die Anzahl der im Raster angezeigten Produkte zu begrenzen. Sie können die angezeigten Produktraster für Folgendes einschränken:

- Produktseite
- Zugehörige/Up-Sell-/Cross-Selling-Produkte hinzufügen
- Produkte zum Bundle-Produkt hinzufügen
- Produkte zum Gruppenprodukt hinzufügen
- Bestellung erstellen (Admin)

Diese Konfigurationseinstellung für die Anzeigebegrenzung für das Produkt ist standardmäßig deaktiviert. Durch Aktivierung dieser Option können Sie die Anzahl der Produkte im Raster auf einen bestimmten Wert begrenzen. Wenn sie aktiviert ist und die Anzahl der übereinstimmenden Produkte für die Rasteranzeige größer als die Datensatzgrenze ist, wird eine begrenzte Sammlung von Datensätzen zurückgegeben. Bei Erreichen des Grenzwerts werden die gefundenen Datensätze insgesamt, die Anzahl der ausgewählten Datensätze und die Paginierungselemente nicht im Rasterheader angezeigt.

>[!NOTE]
>
>Wenn Sie nicht möchten, dass Ihr Produktraster eingeschränkt wird, verwenden Sie Filter genauer, um eine Sammlung zu erstellen, die weniger Elemente enthält als die im Feld _[!UICONTROL Records Limit]_angegebene Zahl.

**_So konfigurieren Sie die Anzeigebegrenzung für das Produkt:_**

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie **[!UICONTROL Advanced]** und wählen Sie **[!UICONTROL Admin]** aus.

1. Erweitern Sie den Abschnitt **[!UICONTROL Admin Grids]** des Erweiterungsselektors ![Erweiterung](../assets/icon-display-expand.png) und führen Sie folgende Schritte aus:

   - Setzen Sie **[!UICONTROL Limit Number of Products in Grid]** auf `Yes`.

   - (Optional) Geben Sie einen Wert in das Feld **[!UICONTROL Records Limit]** ein, um die Anzahl der Produkte im Raster auf einen bestimmten Wert zu begrenzen. Der Standardwert für den Mindestwert ist `20000`.

   ![Konfigurationseinstellungen für Admin Grids](../configuration-reference/advanced/assets/admin-admin-grids.png){width="600" zoomable="yes"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

## Seitensteuerelemente

| Kontrolle | Beschreibung |
|--- |--- |
| [!UICONTROL Add Product] | Initiiert den Prozess zum Erstellen eines neuen einfachen Produkts. Um einen bestimmten Produkttyp auszuwählen, klicken Sie auf den Abwärtspfeil. Optionen: [[!UICONTROL Simple Product]](product-create-simple.md) / [[!UICONTROL Configurable Product]](product-create-configurable.md) / [[!UICONTROL Grouped Product]](product-create-grouped.md) / [[!UICONTROL Virtual Product]](product-create-virtual.md) / [[!UICONTROL Bundle Product]](product-create-bundle.md) / [[!UICONTROL Downloadable Product]](product-create-downloadable.md) / [[!UICONTROL Gift Card]](product-gift-card-create.md) |
| [!UICONTROL Actions] | Listet alle Aktionen auf, die auf ausgewählte Produkte in der Liste angewendet werden können. Um eine Aktion auf ein Produkt oder eine Gruppe von Produkten anzuwenden, aktivieren Sie das Kontrollkästchen in der ersten Spalte jedes Produkts. Optionen: `Delete` / `Change Status` / `Update Attributes` / `Assign Inventory Source` / `Unassign Inventory Source` / `Transfer Inventory To Source` |
| [!UICONTROL Filters] | Startet eine Katalogsuche basierend auf den aktuellen Filtern. |
| [!UICONTROL Default View] | Gibt das aktuelle Rasterspaltenlayout an. Wenn Rasterspaltenansichten gespeichert sind, können Sie eine andere auswählen. |
| [!UICONTROL Columns] | Listet alle Aktionen auf, die auf ausgewählte Produkte in der Liste angewendet werden können. Um eine Aktion auf ein Produkt oder eine Gruppe von Produkten anzuwenden, aktivieren Sie das Kontrollkästchen in der ersten Spalte jedes Produkts. |
| [!UICONTROL Search by keyword] | Das Suchfeld oben links wird verwendet, um Produkte nach Keyword zu finden. |
| [!UICONTROL Edit] | Öffnet das Produkt im Bearbeitungsmodus. Sie können dasselbe erreichen, indem Sie auf eine beliebige Stelle in der Zeile klicken. |

{style="table-layout:auto"}

## Standardspalten

| Spalte | Beschreibung |
|--- |--- |
| (Kontrollkästchen) | Wählt mehrere Datensätze aus, für die eine Aktion durchgeführt werden soll. Das Kontrollkästchen in der ersten Spalte jedes ausgewählten Datensatzes ist markiert. Optionen: <br/>**[!UICONTROL Select All]**- Wählt alle gefundenen Datensätze aus, die den aktuellen Filtereinstellungen entsprechen.<br/>**[!UICONTROL Select All on This Page]** - Wählt nur die auf der aktuellen Seite gefundenen Datensätze aus, die den Filtereinstellungen entsprechen. |
| [!UICONTROL ID] | Eine eindeutige, sequenzielle Zahl, die zugewiesen wird, wenn ein neues Produkt zum ersten Mal gespeichert wird. |
| [!UICONTROL Thumbnail] | Zeigt eine Miniaturansicht des Hauptproduktbilds an. |
| [!UICONTROL Name] | Der Produktname. |
| [!UICONTROL Type] | Der Produkttyp. |
| [!UICONTROL Attribute Set] | Der Name des Attributsatzes, der als Vorlage für das Produkt verwendet wird. |
| [!UICONTROL SKU] | Die eindeutige Lagereinheit, die dem Produkt zugewiesen ist. |
| [!UICONTROL Price] | Der Stückpreis des Produkts. |
| [!UICONTROL Quantity] | Die vorrätige Menge. |
| [!UICONTROL Salable Quantity] | Die Summe aller verfügbaren Einheiten dieses Produkts. |
| [!UICONTROL Visibility] | Gibt an, wo das Produkt im Katalog sichtbar ist. Optionen: `Not Visible Individually` / `Catalog` / `Search` / `Catalog, Search` |
| [!UICONTROL Status] | Gibt den Status des Produkts an. Optionen: `Enabled` und `Disabled` |
| [!UICONTROL Websites] | Gibt die Websites an, auf denen das Produkt verfügbar ist. |
| [!UICONTROL Action] | Öffnet das Produkt im Bearbeitungsmodus. |
| [!UICONTROL Shared Catalog] | ![Adobe Commerce B2B](../assets/b2b.svg) (nur mit [Adobe Commerce B2B](./b2b/../introduction.md) verfügbar) Gibt die freigegebenen Kataloge an, die benutzerdefinierte Produktpreise enthalten. |

{style="table-layout:auto"}

## Sonstige Spalten

| Spalte | Beschreibung |
|--- |--- |
| [!UICONTROL Short Description] | Kurze Beschreibung des Produkts. |
| [!UICONTROL Special Price From Date] | Das erste Datum der Sonderpreisförderung. |
| [!UICONTROL Special Price To Date] | Das letzte Datum der Sonderpreisförderung. |
| [!UICONTROL Cost] | Die tatsächlichen Kosten des Artikels. |
| [!UICONTROL Manufacturer] | Der Hersteller des Produkts. |
| [!UICONTROL Meta Keywords] | Meta-Suchbegriffe für das Produkt. |
| [!UICONTROL Color] | Die Produktfarbe. |
| [!UICONTROL Set Product as New from Date] | Das erste Datum des festgelegten Produkts als neue Promotion. |
| [!UICONTROL Set Product as New to Date] | Das letzte Datum des festgelegten Produkts als neue Promotion. |
| [!UICONTROL Active From / To] | Das Start- und Enddatum des Produkts. |
| [!UICONTROL Layout] | Das Produktlayout. |
| [!UICONTROL Minimum Advertised Price] | Der beworbene Mindestpreis des Produkts. |
| [!UICONTROL Allow Gift Message] | Die Geschenknachricht an Kunden, die eine Geschenkkarte kaufen. |
| [!UICONTROL Special Price] | Sonderpreis für das Produkt. |
| [!UICONTROL Weight] | Das Produktgewicht. |
| [!UICONTROL Meta Title] | Metadatentitel für das Produkt. |
| [!UICONTROL Meta Description] | Die Beschreibung der Produktmetadaten. |
| [!UICONTROL Country of Manufacture] | Das Herstellungsland. |
| [!UICONTROL New Theme] | Benutzerdefiniertes Design auf das Produkt angewendet. |
| [!UICONTROL URL Key] | Der URL-Schlüssel des Produkts. |
| [!UICONTROL Tax Class] | Die Produktsteuerklasse. |
| [!UICONTROL Allow Gift Message] | Zeigt die Verfügbarkeit der Option für die Geschenknachricht für das Produkt an. |

{style="table-layout:auto"}
