---
title: Produktlisten
description: Erfahren Sie, wie Sie die Konfiguration der Produktliste ändern, die bestimmt, wie viele Produkte pro Seite angezeigt werden und mit welchem Attribut die Liste sortiert wird.
exl-id: 3779d9db-4adb-473b-b9c9-ad066f50b549
feature: Catalog Management, Products, Page Content
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '792'
ht-degree: 0%

---

# Produktlisten

Produktlisten können standardmäßig als Liste oder Raster angezeigt werden. Sie können auch bestimmen, wie viele Produkte pro Seite angezeigt werden und welches Attribut zum Sortieren der Liste verwendet wird. Die Produktliste enthält eine Reihe von Steuerelementen, mit denen Sie die Produkte sortieren, das Listenformat ändern, nach Attribut sortieren und von einer Seite zur nächsten wechseln können.

>[!NOTE]
>
>Beim Sortieren einer Kategorie nach einem Produktattribut werden Produkte mit denselben Attributwerten auch in aufsteigender Reihenfolge nach ihrem _[!UICONTROL Product ID]_sortiert.

![Als Raster angezeigte Produkte](./assets/storefront-catalog-page.png){width="700" zoomable="yes"}

## Produktlisten konfigurieren

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bedienfeld den Wert **[!UICONTROL Catalog]** und wählen Sie unter &quot;**[!UICONTROL Catalog]**&quot;.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Storefront]** .

   ![Speichervorkonfigurationsoptionen](../configuration-reference/catalog/assets/catalog-storefront.png){width="600" zoomable="yes"}

   Eine detaillierte Liste dieser Optionen finden Sie unter [Storefront](../configuration-reference/catalog/catalog.md#storefront) in der _Konfigurationsreferenz_.

   >[!NOTE]
   >
   >Um Produkte und ihre Preise gemäß der Sortierung nach Preis __ anzuzeigen, stellen Sie sicher, dass die Einstellungen für die Preisanzeige in der [Konfiguration der Umsatzsteuer](../configuration-reference/sales/tax.md) denselben Wert haben (`Excluding Tax` **oder** `Including Tax`). Überprüfen Sie für &quot;_[!UICONTROL Calculation Settings]_&quot;den Wert &quot;**[!UICONTROL Catalog Prices]**&quot;. Überprüfen Sie für_[!UICONTROL Price Display Settings]_ den Wert **[!UICONTROL Display Product Prices in Catalog]** . Wenn diese unterschiedliche Werte aufweisen, können Preisfilter in der mehrschichtigen Navigation Produkte möglicherweise nicht ordnungsgemäß nach Preisen filtern und sortieren.

1. Legen Sie den Standardwert **[!UICONTROL List Mode]** auf einen der folgenden Werte fest:

   - `Grid Only`
   - `List Only`
   - `Grid (default) / List`
   - `List (default / Grid`

1. Geben Sie für &quot;**[!UICONTROL Products per Page on Grid Allowed Values]**&quot;die Anzahl der Produkte ein, die pro Seite angezeigt werden sollen, wenn sie im Rasterformat angezeigt werden.

   Um eine Werteauswahl vorzunehmen, trennen Sie jede Zahl durch ein Komma.

1. Geben Sie für &quot;**[!UICONTROL Products per Page on Grid Default Value]**&quot;die standardmäßige Anzahl von Produkten ein, die pro Seite im Raster angezeigt werden sollen.

1. Geben Sie für &quot;**[!UICONTROL Products per Page on List Allowed Values]**&quot;die Anzahl der Produkte ein, die pro Seite angezeigt werden sollen, wenn sie im Listenformat angezeigt werden.

   Um eine Werteauswahl vorzunehmen, trennen Sie jede Zahl durch ein Komma.

1. Geben Sie für &quot;**[!UICONTROL Products per page on List Default Value]**&quot;die standardmäßige Anzahl von Produkten ein, die pro Seite in der Liste angezeigt werden.

1. Setzen Sie **[!UICONTROL Product Listing Sorted by]** auf das Standardattribut, das ursprünglich zum Sortieren der Liste verwendet wird.

1. Damit Kunden die Möglichkeit erhalten, alle Produkte aufzulisten, setzen Sie **[!UICONTROL Allow All Products on Page]** auf `Yes`.

1. Wenn Sie alle Paginierungseinstellungen beibehalten möchten, während Kunden durch Kataloglisten navigieren, setzen Sie **[!UICONTROL Remember Category Pagination]** auf `Yes`.

   Durch Aktivierung dieser Einstellung wird sichergestellt, dass die Anzahl der in einer Liste oder einem Raster angezeigten Produkte beibehalten wird, wenn Besucher von einer Kategorie zur anderen navigieren. Standardmäßig ist dieses Feld auf `No` gesetzt, da es mehr Cache-Speicher verwendet und sich auf die Art und Weise auswirken kann, wie Seiten von Suchmaschinen indiziert werden.

1. Wenn Sie einen [flachen Katalog](catalog-flat.md) (**nicht empfohlen**) verwenden, gehen Sie wie folgt vor:

   - Um eine flache Liste von Produkten in einer Kategorie anzuzeigen, setzen Sie **[!UICONTROL Use Flat Catalog Category]** auf `Yes`.

   - Um eine flache Produktliste anzuzeigen, setzen Sie **[!UICONTROL Use Flat Catalog Product]** auf `Yes`.

1. Wenn Sie dynamische Verweise für Medien-Assets in Kategorie- und Produkt-URLs zulassen möchten, setzen Sie **[!UICONTROL Allow Dynamic Media URLs in Products and Categories]** auf `Yes`.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

## Seitensteuerelemente

| Kontrolle | Beschreibung |
|--- |--- |
| [!UICONTROL View As] | Zeigt die Produkte im Raster- oder Listenformat an. |
| [!UICONTROL Sort By] | Ändert die Sortierreihenfolge der Liste. |
| [!UICONTROL Show Per Page] | Bestimmt, wie viele Produkte pro Seite angezeigt werden. |
| Paginierungslinks | Navigationslinks zu anderen Seiten. |

{style="table-layout:auto"}

## Paginierungskontrollen

Die Paginierungseinstellungen werden oben und unten in der Liste angezeigt und steuern das Format der Paginierungslinks für Produktlisten. Sie können die Anzahl der Links festlegen, die im Steuerelement angezeigt werden, und die Links Weiter und Zurück konfigurieren. Damit die Paginierungslinks angezeigt werden, muss die Liste mehr Produkte enthalten, als pro Seite in der Produktlistenkonfiguration zulässig sind.

![Paginierungssteuerelemente](./assets/storefront-pagination-controls.png){width="700" zoomable="yes"}

### Steuerelemente für die Storefront-Paginierung

| Kontrolle | Beschreibung |
|--- |--- |
| ![Raster anzeigen](./assets/controls-pagination-list-grid.png) | [!UICONTROL View As] - Zeigt die Liste im Raster- oder Listenformat an. |
| ![Sortieren nach](./assets/control-pagination-sort-by.png) | [!UICONTROL Sort By] - Ändert die Sortierreihenfolge der Liste. Die Eigenschaft _[!UICONTROL Used for Sorting in Product Listing]_storefront bestimmt, welche [Produktattribute](../catalog/product-attributes.md) zum Sortieren der Liste verwendet werden können. |
| ![Pro Seite anzeigen](./assets/control-pagination-show-per-page.png) | [!UICONTROL Show Per Page] - Bestimmt, wie viele Produkte pro Seite angezeigt werden. |
| ![Paginierungslinks](./assets/control-pagination.png) | Paginierungslinks - Navigationslinks zu anderen Seiten. |

{style="table-layout:auto"}

### Paginierungssteuerelemente konfigurieren

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Suchen Sie die Store-Ansicht, die Sie konfigurieren möchten, und klicken Sie in der Spalte **[!UICONTROL Action]** auf **[!UICONTROL Edit]**.

1. Erweitern Sie unter **[!UICONTROL Other Settings]** den Abschnitt ![Erweiterungsauswahl](../assets/icon-display-expand.png) um den Abschnitt **[!UICONTROL Pagination]**.

   ![Paginierung](./assets/config-design-pagination.png){width="600" zoomable="yes"}

   Weitere Informationen zu diesen Einstellungen finden Sie unter [Designkonfiguration](../content-design/configuration.md).

1. Geben Sie für &quot;**[!UICONTROL Pagination Frame]**&quot;die Anzahl der Links ein, die im Paginierungssteuerelement angezeigt werden sollen.

1. Geben Sie für &quot;**[!UICONTROL Pagination Frame Skip]**&quot;die Anzahl der Links ein, die Sie überspringen möchten, bevor Sie den nächsten Satz von Links im Paginierungssteuerelement anzeigen.

   Wenn der Paginierungsrahmen beispielsweise fünf Links hat und Sie zu den nächsten fünf Links springen möchten, wie viele Links möchten Sie dann überspringen? Wenn Sie den Wert auf vier (`4`) festlegen, ist der letzte Link aus dem vorherigen Satz der erste Link im nächsten Satz.

1. Geben Sie für &quot;**[!UICONTROL Anchor Text for Previous]**&quot;den Text ein, der für den vorherigen Link angezeigt werden soll.

   Lassen Sie das Feld leer, um den Standardpfeil zu verwenden.

1. Geben Sie für &quot;**[!UICONTROL Anchor Text for Next]**&quot;den Text ein, der für den nächsten Link angezeigt werden soll. Lassen Sie das Feld leer, um den Standardpfeil zu verwenden.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Configuration]**.
