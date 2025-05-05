---
title: Produktlisten
description: Erfahren Sie, wie Sie die Konfiguration der Produktliste ändern, die bestimmt, wie viele Produkte pro Seite angezeigt werden, und welches Attribut zum Sortieren der Liste verwendet wird.
exl-id: 3779d9db-4adb-473b-b9c9-ad066f50b549
feature: Catalog Management, Products, Page Content
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '792'
ht-degree: 0%

---

# Produktlisten

Produktlisten können so eingestellt werden, dass sie standardmäßig entweder als Liste oder als Raster angezeigt werden. Sie können auch festlegen, wie viele Produkte pro Seite angezeigt werden und mit welchem Attribut die Liste sortiert wird. Die Produktliste enthält eine Reihe von Steuerelementen, mit denen Sie die Produkte sortieren, das Format der Liste ändern, nach Attribut sortieren und von einer Seite zur nächsten wechseln können.

>[!NOTE]
>
>Beim Sortieren einer Kategorie nach einem Produktattribut werden Produkte mit denselben Attributwerten auch nach ihrem _[!UICONTROL Product ID]_&#x200B;in aufsteigender Reihenfolge sortiert.

![Produkte werden als Raster angezeigt](./assets/storefront-catalog-page.png){width="700" zoomable="yes"}

## Konfigurieren von Produktlisten

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Catalog]** und wählen Sie darunter **[!UICONTROL Catalog]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Storefront]** .

   ![Storefront-Konfigurationsoptionen](../configuration-reference/catalog/assets/catalog-storefront.png){width="600" zoomable="yes"}

   Eine detaillierte Liste dieser Optionen finden Sie unter [Storefront](../configuration-reference/catalog/catalog.md#storefront) in _Konfigurationsreferenz_.

   >[!NOTE]
   >
   >Um Produkte und ihre Preise korrekt nach _Produktsortierung nach Preis_ anzuzeigen, stellen Sie sicher, dass die Einstellungen für die Preisanzeige in der [Mehrwertsteuerkonfiguration](../configuration-reference/sales/tax.md) denselben Wert aufweisen (`Excluding Tax` **oder**`Including Tax`). Überprüfen Sie für die _[!UICONTROL Calculation Settings]_&#x200B;den **[!UICONTROL Catalog Prices]**. Überprüfen Sie&#x200B;_[!UICONTROL Price Display Settings]_ den **[!UICONTROL Display Product Prices in Catalog]**. Wenn diese unterschiedliche Werte haben, können Preisfilter in der mehrschichtigen Navigation Produkte möglicherweise nicht ordnungsgemäß nach Preis filtern und sortieren.

1. Legen Sie die **[!UICONTROL List Mode]** auf einen der folgenden Werte fest:

   - `Grid Only`
   - `List Only`
   - `Grid (default) / List`
   - `List (default / Grid`

1. Geben Sie **[!UICONTROL Products per Page on Grid Allowed Values]** die Anzahl der Produkte ein, die pro Seite angezeigt werden sollen, wenn sie im Rasterformat angezeigt werden.

   Um eine Werteauswahl einzugeben, trennen Sie jede Zahl durch ein Komma.

1. Geben Sie **[!UICONTROL Products per Page on Grid Default Value]** die Standardanzahl von Produkten ein, die pro Seite im Raster angezeigt werden sollen.

1. Geben Sie **[!UICONTROL Products per Page on List Allowed Values]** die Anzahl der Produkte ein, die pro Seite angezeigt werden sollen, wenn sie im Listenformat angezeigt werden.

   Um eine Werteauswahl einzugeben, trennen Sie jede Zahl durch ein Komma.

1. Geben Sie **[!UICONTROL Products per page on List Default Value]** die Standardanzahl der Produkte ein, die pro Seite in der Liste angezeigt werden.

1. Setzen Sie **[!UICONTROL Product Listing Sorted by]** auf das Standardattribut, das ursprünglich zum Sortieren der Liste verwendet wird.

1. Um Kunden die Möglichkeit zu geben, alle Produkte aufzulisten, setzen Sie **[!UICONTROL Allow All Products on Page]** auf `Yes`.

1. Wenn Sie alle Paginierungseinstellungen beibehalten möchten, während Kunden durch Kataloglisten navigieren, setzen Sie **[!UICONTROL Remember Category Pagination]** auf `Yes`.

   Durch Aktivierung dieser Einstellung wird sichergestellt, dass die Anzahl der in einer Liste oder einem Raster angezeigten Produkte beibehalten wird, wenn Käufer von einer Kategorie zur anderen navigieren. Standardmäßig ist dieses Feld auf `No` festgelegt, da es mehr Cache-Speicher verwendet und die Art und Weise, wie Seiten von Suchmaschinen indiziert werden, beeinflussen kann.

1. Wenn Sie einen [flachen Katalog](catalog-flat.md) verwenden (**nicht empfohlen**), gehen Sie wie folgt vor:

   - Um eine flache Kategorieliste von Produkten anzuzeigen, setzen Sie **[!UICONTROL Use Flat Catalog Category]** auf `Yes`.

   - Um eine flache Produktliste anzuzeigen, setzen Sie **[!UICONTROL Use Flat Catalog Product]** auf `Yes`.

1. Wenn Sie dynamische Verweise für Medien-Assets in Kategorie- und Produkt-URLs zulassen möchten, setzen Sie **[!UICONTROL Allow Dynamic Media URLs in Products and Categories]** auf `Yes`.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

## Seitensteuerelemente

| Kontrolle | Beschreibung |
|--- |--- |
| [!UICONTROL View As] | Zeigt die Produkte entweder im Raster- oder Listenformat an. |
| [!UICONTROL Sort By] | Ändert die Sortierreihenfolge der Liste. |
| [!UICONTROL Show Per Page] | Legt fest, wie viele Produkte pro Seite angezeigt werden. |
| Seitenumbruch-Links | Navigations-Links zu anderen Seiten |

{style="table-layout:auto"}

## Steuerelemente für die Paginierung

Die Paginierungseinstellungen werden oben und unten in der Liste angezeigt und steuern das Format der Paginierungslinks für Produktlisten. Sie können die Anzahl der Links festlegen, die im Steuerelement angezeigt werden, und die nächsten und vorherigen Links konfigurieren. Damit die Paginierungslinks angezeigt werden, muss die Liste mehr Produkte enthalten, als pro Seite in der Produktlistenkonfiguration zulässig sind.

![Steuerelemente für die Paginierung](./assets/storefront-pagination-controls.png){width="700" zoomable="yes"}

### Steuerung der Storefront-Paginierung

| Kontrolle | Beschreibung |
|--- |--- |
| ![Raster anzeigen](./assets/controls-pagination-list-grid.png) | [!UICONTROL View As] - Zeigt die Liste entweder im Raster- oder im Listenformat an. |
| ![Sortieren nach](./assets/control-pagination-sort-by.png) | [!UICONTROL Sort By] - Ändert die Sortierreihenfolge der Liste. Die Eigenschaft &quot;_[!UICONTROL Used for Sorting in Product Listing]_&#x200B;Storefront“ bestimmt, welche [Produktattribute](../catalog/product-attributes.md) zum Sortieren der Liste verwendet werden können. |
| ![Pro Seite anzeigen](./assets/control-pagination-show-per-page.png) | [!UICONTROL Show Per Page] - Legt fest, wie viele Produkte pro Seite angezeigt werden. |
| ![Paginierungs-Links](./assets/control-pagination.png) | Seitenumbruch-Links : Navigations-Links zu anderen Seiten. |

{style="table-layout:auto"}

### Konfigurieren der Steuerelemente für die Paginierung

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Suchen Sie die Store-Ansicht, die Sie konfigurieren möchten, und klicken Sie in der Spalte **[!UICONTROL Action]** auf **[!UICONTROL Edit]**.

1. Erweitern Sie unter **[!UICONTROL Other Settings]** ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Pagination]** .

   ![Paginierung](./assets/config-design-pagination.png){width="600" zoomable="yes"}

   Weitere Informationen zu diesen Einstellungen finden Sie unter [Design-Konfiguration](../content-design/configuration.md).

1. Geben Sie **[!UICONTROL Pagination Frame]** die Anzahl der Links ein, die im Paginierungssteuerelement angezeigt werden sollen.

1. Geben Sie **[!UICONTROL Pagination Frame Skip]** die Anzahl der Links ein, die Sie überspringen möchten, bevor Sie den nächsten Satz von Links im Paginierungssteuerelement anzeigen.

   Wenn beispielsweise der Paginierungsrahmen fünf Links enthält und Sie zu den nächsten fünf Links springen möchten, wie viele Links möchten Sie überspringen? Wenn Sie den Wert auf vier (`4`) setzen, ist der letzte Link aus der vorherigen Gruppe der erste Link in der nächsten Gruppe.

1. Geben Sie **[!UICONTROL Anchor Text for Previous]** den Text ein, der für den vorherigen Link angezeigt werden soll.

   Lassen Sie das Feld leer, um den Standardpfeil zu verwenden.

1. Geben Sie **[!UICONTROL Anchor Text for Next]** den Text ein, der für den nächsten Link angezeigt werden soll. Lassen Sie das Feld leer, um den Standardpfeil zu verwenden.

1. Klicken Sie abschließend auf **[!UICONTROL Save Configuration]**.
