---
title: Produktliste
description: Erfahren Sie mehr über die Seite „_[!UICONTROL Products]_“ in Admin, auf der Sie Produkte erstellen und vorhandene bearbeiten können.
exl-id: 47e14f72-017f-456a-8904-6d32ef47e6f1
feature: Catalog Management, Products, Admin Workspace
source-git-commit: 8bb91b80f8ba957676c654e984deb5704b777612
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 0%

---

# Produktliste

Auf alle Produkte im Katalog kann über die Seite &quot;_[!UICONTROL Products]_&quot; in der Admin Console zugegriffen werden. Dort können Sie Produkte erstellen und vorhandene bearbeiten. Bei einer Multi-Site-Installation kann jede Website eine andere Auswahl von Produkten zum Verkauf aus demselben Katalog anbieten.

Die _[!UICONTROL Products]_&#x200B;Liste enthält alle Produkte im Katalog, gibt die Websites an, auf denen sie verfügbar sind, und ob sie derzeit für den Verkauf aktiviert sind. In Adobe Commerce B2B-Installationen mit [freigegebenen Katalogen](../b2b/catalog-shared.md) enthält das Raster eine Spalte, die angibt, für welche Produkte in einem freigegebenen Katalog alternative Rabattpreise gelten.

Sie können die Liste Seite für Seite durchsuchen oder nach bestimmten Produkten suchen. Verwenden Sie die standardmäßigen [Steuerelemente](../getting-started/admin-grid-controls.md), um die Liste zu sortieren und zu filtern und [Aktionen](../getting-started/admin-actions-control.md) auf ausgewählte Produkte anzuwenden.

![Produktraster](./assets/products-grid.png){width="700" zoomable="yes"}

## Anzeige von Produkten begrenzen

Um die Leistung großer Kataloge zu verbessern, wird empfohlen, die Anzahl der im Raster angezeigten Produkte zu begrenzen. Sie können die angezeigten Produktraster einschränken für:

- Produktseite
- Hinzufügen verwandter/Upsell-/Crosssell-Produkte
- Produkte zum Produktpaket hinzufügen
- Produkte zu Produktgruppe hinzufügen
- Bestellung erstellen (Admin)

Diese Konfigurationseinstellung für die Begrenzung der Produktanzeige ist standardmäßig deaktiviert. Durch Aktivierung können Sie die Anzahl der Produkte im Raster auf einen bestimmten Wert begrenzen. Wenn diese Option aktiviert ist und die Anzahl der passenden Produkte für die Rasteranzeige größer als das Datensatzlimit ist, wird eine begrenzte Sammlung von Datensätzen zurückgegeben. Wenn das Limit erreicht ist, werden die insgesamt gefundenen Datensätze, die Anzahl der ausgewählten Datensätze und die Paginierungselemente nicht in der Rasterkopfzeile angezeigt.

>[!NOTE]
>
>Wenn Ihr Produktraster nicht beschränkt werden soll, verwenden Sie Filter präziser, um eine Sammlung zu erstellen, die weniger Elemente als die im Feld _[!UICONTROL Records Limit]_&#x200B;angegebene Anzahl enthält.

**_So konfigurieren Sie die Begrenzung der Produktanzeige:_**

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie **[!UICONTROL Advanced]** und wählen Sie **[!UICONTROL Admin]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Admin Grids]** und führen Sie folgende Schritte aus:

   - Legen Sie **[!UICONTROL Limit Number of Products in Grid]** auf `Yes` fest.

   - (Optional) Geben Sie einen Wert in das Feld **[!UICONTROL Records Limit]** ein, um die Anzahl der Produkte im Raster auf einen bestimmten Wert zu begrenzen. Der standardmäßige Mindestwert ist `20000`.

   ![Admin Grids-Konfigurationseinstellungen](../configuration-reference/advanced/assets/admin-admin-grids.png){width="600" zoomable="yes"}

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

## Seitensteuerelemente

| Kontrolle | Beschreibung |
|--- |--- |
| [!UICONTROL Add Product] | Startet den Prozess zum Erstellen eines neuen einfachen Produkts. Um einen bestimmten Produkttyp auszuwählen, klicken Sie auf den Abwärtspfeil. Optionen: [[!UICONTROL Simple Product]](product-create-simple.md) / [[!UICONTROL Configurable Product]](product-create-configurable.md) / [[!UICONTROL Grouped Product]](product-create-grouped.md) / [[!UICONTROL Virtual Product]](product-create-virtual.md) / [[!UICONTROL Bundle Product]](product-create-bundle.md) / [[!UICONTROL Downloadable Product]](product-create-downloadable.md) / [[!UICONTROL Gift Card]](product-gift-card-create.md) |
| [!UICONTROL Actions] | Listet alle Aktionen auf, die auf ausgewählte Produkte in der Liste angewendet werden können. Um eine Aktion auf ein Produkt oder eine Gruppe von Produkten anzuwenden, aktivieren Sie das Kontrollkästchen in der ersten Spalte jedes Produkts. Optionen: `Delete` / `Change Status` / `Update Attributes` / `Assign Inventory Source` / `Unassign Inventory Source` / `Transfer Inventory To Source` |
| [!UICONTROL Filters] | Startet eine Katalogsuche anhand der aktuellen Filter. |
| [!UICONTROL Default View] | Gibt das aktuelle Rasterspaltenlayout an. Wenn es gespeicherte Rasterspaltenansichten gibt, können Sie eine andere auswählen. |
| [!UICONTROL Columns] | Listet alle Aktionen auf, die auf ausgewählte Produkte in der Liste angewendet werden können. Um eine Aktion auf ein Produkt oder eine Gruppe von Produkten anzuwenden, aktivieren Sie das Kontrollkästchen in der ersten Spalte jedes Produkts. |
| [!UICONTROL Search by keyword] | Das Suchfeld oben links wird verwendet, um Produkte nach Keyword zu finden. |
| [!UICONTROL Edit] | Öffnet das Produkt im Bearbeitungsmodus. Dasselbe können Sie erreichen, indem Sie auf eine beliebige Stelle in der Zeile klicken. |

{style="table-layout:auto"}

## Standardspalten

| Spalte | Beschreibung |
|--- |--- |
| (Kontrollkästchen) | Wählt mehrere Datensätze aus, die einer Aktion unterzogen werden sollen. Das Kontrollkästchen in der ersten Spalte jedes ausgewählten Datensatzes ist markiert. Optionen: <br/>**[!UICONTROL Select All]**- Wählt alle gefundenen Datensätze aus, die den aktuellen Filtereinstellungen entsprechen.<br/>**[!UICONTROL Select All on This Page]** - Wählt nur die auf der aktuellen Seite gefundenen Datensätze aus, die den Filtereinstellungen entsprechen. |
| [!UICONTROL ID] | Eine eindeutige, sequenzielle Nummer, die zugewiesen wird, wenn ein neues Produkt zum ersten Mal gespeichert wird. |
| [!UICONTROL Thumbnail] | Zeigt eine Miniaturansicht des Hauptproduktbilds an. |
| [!UICONTROL Name] | Der Produktname. |
| [!UICONTROL Type] | Der Produkttyp. |
| [!UICONTROL Attribute Set] | Der Name des Attributsatzes, der als Vorlage für das Produkt verwendet wird. |
| [!UICONTROL SKU] | Die eindeutige Lagerhaltungseinheit, die dem Produkt zugewiesen ist. |
| [!UICONTROL Price] | Der Stückpreis des Produkts. |
| [!UICONTROL Quantity] | Die auf Lager befindliche Menge. |
| [!UICONTROL Salable Quantity] | Die Summe aller verfügbaren Einheiten dieses Produkts. |
| [!UICONTROL Visibility] | Gibt an, wo das Produkt im Katalog sichtbar ist. Optionen: `Not Visible Individually` / `Catalog` / `Search` / `Catalog, Search` |
| [!UICONTROL Status] | Gibt den Status des Produkts an. Optionen: `Enabled` und `Disabled` |
| [!UICONTROL Websites] | Gibt die Websites an, auf denen das Produkt verfügbar ist. |
| [!UICONTROL Action] | Öffnet das Produkt im Bearbeitungsmodus. |
| [!UICONTROL Shared Catalog] | ![Adobe Commerce B2B](../assets/b2b.svg) (nur verfügbar mit [Adobe Commerce B2B](./b2b/../introduction.md)) Gibt die freigegebenen Kataloge an, die benutzerdefinierte Preise für das Produkt enthalten. |

{style="table-layout:auto"}

## Andere Spalten

| Spalte | Beschreibung |
|--- |--- |
| [!UICONTROL Short Description] | Kurze Beschreibung des Produkts. |
| [!UICONTROL Special Price From Date] | Das erste Datum der Sonderpreisaktion. |
| [!UICONTROL Special Price To Date] | Das letzte Datum der Sonderpreisaktion. |
| [!UICONTROL Cost] | Die Ist-Kosten des Artikels. |
| [!UICONTROL Manufacturer] | Der Hersteller des Produkts. |
| [!UICONTROL Meta Keywords] | Meta-Schlüsselwörter für das Produkt. |
| [!UICONTROL Color] | Die Produktfarbe. |
| [!UICONTROL Set Product as New from Date] | Das erste Datum der eingestellten Ware als neue Promotion. |
| [!UICONTROL Set Product as New to Date] | Das letzte Datum der eingestellten Produkt als neue Promotion. |
| [!UICONTROL Active From / To] | Das Start- und Enddatum des Produkts. |
| [!UICONTROL Layout] | Das Produkt-Layout. |
| [!UICONTROL Minimum Advertised Price] | Der mindestens angezeigte Preis des Produkts. |
| [!UICONTROL Allow Gift Message] | Die Geschenknachricht an Kunden, die eine Geschenkkarte kaufen. |
| [!UICONTROL Special Price] | Sonderpreis für das Produkt. |
| [!UICONTROL Weight] | Das Produktgewicht. |
| [!UICONTROL Meta Title] | Meta-Titel für das Produkt. |
| [!UICONTROL Meta Description] | Die Beschreibung der Produktmetadaten. |
| [!UICONTROL Country of Manufacture] | Das Land der Herstellung. |
| [!UICONTROL New Theme] | Benutzerdefiniertes Design auf das Produkt angewendet. |
| [!UICONTROL URL Key] | Der URL-Schlüssel des Produkts. |
| [!UICONTROL Tax Class] | Die Produktsteuerklasse. |
| [!UICONTROL Allow Gift Message] | Zeigt die Verfügbarkeit der Option Geschenknachricht für das Produkt an. |

{style="table-layout:auto"}
