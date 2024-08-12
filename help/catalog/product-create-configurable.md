---
title: Konfigurierbares Produkt
description: Erfahren Sie, wie Sie ein konfigurierbares Produkt erstellen, das den Käufern Varianten zur Auswahl bietet.
exl-id: 2066fd20-5227-41e9-b213-31825a58ebd9
feature: Catalog Management, Products
source-git-commit: ce36104913434bb71115e1a5b497f38f75fbd3c5
workflow-type: tm+mt
source-wordcount: '2506'
ht-degree: 0%

---

# Konfigurierbares Produkt

Ein konfigurierbares Produkt sieht aus wie ein einzelnes Produkt mit einer Dropdown-Liste jeder Variante. Jedes Listenelement ist tatsächlich ein separates einfaches Produkt mit einer eindeutigen SKU, die es ermöglicht, das Inventar für jede Produktvariante zu verfolgen. Sie können einen ähnlichen Effekt erzielen, indem Sie ein einfaches Produkt mit benutzerdefinierten Optionen verwenden, aber ohne die Möglichkeit, Inventar für jede Variante zu verfolgen.

Die folgenden Anweisungen zeigen den Prozess der Erstellung eines konfigurierbaren Produkts mit einer [Produktvorlage](attribute-sets.md), erforderlichen Feldern und grundlegenden Einstellungen. Jedes erforderliche Feld ist mit einem roten Sternchen (`*`) gekennzeichnet. Wenn Sie die Grundlagen abgeschlossen haben, können Sie die anderen Produkteinstellungen nach Bedarf abschließen.

![Konfigurierbares Produkt](./assets/product-configurable.png){width="700" zoomable="yes"}

## Teil 1: Erstellen eines konfigurierbaren Produkts

Obwohl ein konfigurierbares Produkt mehr SKUs verwendet und die Einrichtung zunächst etwas länger dauern kann, kann es am Ende Zeit sparen. Wenn Sie Ihr Unternehmen erweitern möchten, ist der konfigurierbare Produkttyp eine gute Wahl für Produkte mit mehreren Optionen.

Bevor Sie beginnen, bereiten Sie einen [Attributsatz](attribute-sets.md) vor, der ein Attribut enthält, das auf einen der zulässigen Eingabetypen für jede Produktvariante festgelegt ist. Beispielsweise kann der Attributsatz Dropdown-Attribute für Farbe und Größe enthalten.

Die Eigenschaften jedes Attributs, das für eine konfigurierbare Produktvariante verwendet wird, müssen die folgenden Einstellungen aufweisen:

### Attributanforderungen für Produktvarianten

| Eigenschaft | Einstellung |
|--- |--- |
| [!UICONTROL Scope] | `Global` |
| [!UICONTROL Catalog Input Type for Store Owner] | Der Eingabetyp eines Attributs, das für eine Produktvariante verwendet wird, muss einer der folgenden sein: `Dropdown`, `Visual Swatch` oder `Text Swatch`. |
| [!UICONTROL Values Required] | `Yes` |

{style="table-layout:auto"}

### Schritt 1: Produkttyp auswählen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Wählen Sie im Menü _[!UICONTROL Add Product]_( ![Menüpfeil](../assets/icon-menu-down-arrow-red.png){width="25"} ) oben rechts **[!UICONTROL Configurable Product]**aus.

   ![Konfigurierbares Produkt hinzufügen](./assets/product-add-configurable.png){width="700" zoomable="yes"}

### Schritt 2: Attributsatz auswählen

Der [Attributsatz](attribute-sets.md) bestimmt die Auswahl der im Produkt verwendeten Felder. Der im folgenden Beispiel verwendete Attributsatz hat Attribute für Farbe und Größe. Der Name des Attributsatzes wird oben auf der Seite angezeigt und zunächst auf `Default` gesetzt.

1. Um den Attributsatz für das Produkt auszuwählen, klicken Sie auf das Feld oben auf der Seite und führen Sie einen der folgenden Schritte aus:

   - Geben Sie für &quot;**[!UICONTROL Search]**&quot;den Namen des Attributsatzes ein.
   - Wählen Sie in der Liste den Attributsatz aus, den Sie verwenden möchten.

   Das Formular wird entsprechend der Änderung aktualisiert.

1. Wenn Sie dem Attributsatz ein weiteres Attribut hinzufügen möchten, klicken Sie auf **[!UICONTROL Add Attribute]** und befolgen Sie die Anweisungen unter [Hinzufügen eines Attributs](product-attributes-add.md).

   ![Vorlage auswählen](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

### Schritt 3: Ausführen der erforderlichen Einstellungen

1. Geben Sie das Produkt **[!UICONTROL Product Name]** ein.

1. Nehmen Sie die standardmäßige **[!UICONTROL SKU]** an, die auf dem Produktnamen basiert, oder geben Sie einen anderen ein.

1. Geben Sie das Produkt **[!UICONTROL Price]** ein.

1. Da das Produkt noch nicht zur Veröffentlichung bereit ist, setzen Sie **[!UICONTROL Enable Product]** auf `No`.

1. Klicken Sie auf **[!UICONTROL Save]** und fahren Sie fort.

   Wenn das Produkt gespeichert wird, wird die Auswahl für die [Store-Ansicht](introduction.md#product-scope) in der oberen linken Ecke angezeigt.

1. Wählen Sie die **[!UICONTROL Store View]** aus, in der das Produkt verfügbar sein soll.

   ![Auswählen der Store-Ansicht](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

### Schritt 4: Grundlegende Einstellungen durchführen

1. Setzen Sie **[!UICONTROL Tax Class]** auf einen der folgenden Werte:

   - `None`
   - `Taxable Goods`

1. Die **[!UICONTROL Quantity]** wird durch die Produktvarianten bestimmt, sodass Sie sie leer lassen können.

1. Belassen Sie die **[!UICONTROL Stock Status]** wie festgelegt.

   Der Lagerstatus eines konfigurierbaren Produkts wird durch jede zugeordnete Konfiguration bestimmt. Da das Produkt gespeichert wurde, ohne eine Menge einzugeben, wird **[!UICONTROL Stock Status]** auf `Out of Stock` gesetzt.

   >[!NOTE]
   >
   >Der **Lagerstatus** des konfigurierbaren Produkts ist eine durch **_halbmanuell_** gesteuerte Einstellung. Sie wird zum Teil durch den Bestandsstatus ihrer untergeordneten Produkte kontrolliert. Sie ist Teil einer Aktienstatusberechnung mit **_mehreren Kriterien_**, die im Abschnitt [Lagerstatus konfigurieren](#configure-the-stock-status) beschrieben wird.

1. Geben Sie das Produkt **[!UICONTROL Weight]** ein.

>[!NOTE]
>
>Ein konfigurierbares Produkt muss immer eine Gewichtung aufweisen. Wenn Sie aus der Dropdownliste die Option &quot;**[!UICONTROL This item has no weight]**&quot; auswählen, wird sie nach dem Speichern des Produkts automatisch in &quot;**[!UICONTROL This item has weight]**&quot;geändert.

1. Nehmen Sie die standardmäßige **[!UICONTROL Visibility]** -Einstellung von `Catalog, Search` an.

1. Um das Produkt in der Liste der [neuen Produkte](../content-design/widget-new-products-list.md) zu kennzeichnen, aktivieren Sie das Kontrollkästchen **[!UICONTROL Set Product as New]** .

1. Um dem Produkt Kategorien zuzuweisen, klicken Sie auf das Feld **[!UICONTROL Select…]** und führen Sie einen der folgenden Schritte aus:

   **Wählen Sie eine vorhandene Kategorie**:

   - Beginnen Sie mit der Eingabe in das Feld, bis Sie eine Übereinstimmung finden.

   - Aktivieren Sie das Kontrollkästchen der Kategorie, die zugewiesen werden soll.

   ![Wählen Sie eine oder mehrere Kategorien für das Bundle-Produkt aus](./assets/product-create-categories.png){width="600" zoomable="yes"}

   **Erstellen einer Kategorie**:

   - Klicken Sie auf **[!UICONTROL New Category]**.

   - Geben Sie den Wert **[!UICONTROL Category Name]** ein und wählen Sie den Wert **[!UICONTROL Parent Category]** aus, der seine Position in der Menüstruktur bestimmt.

   s - Klicken Sie auf **[!UICONTROL Create Category]**.

1. Wählen Sie die **[!UICONTROL Country of Manufacture]** aus.

   Es kann zusätzliche Attribute geben, mit denen das Produkt beschrieben wird. Die Auswahl variiert je nach Attributsatz und kann zu einem späteren Zeitpunkt abgeschlossen werden.

### Schritt 5: Speichern und fortfahren

Jetzt ist eine gute Zeit, um Ihre Arbeit zu retten. Klicken Sie in der oberen rechten Ecke auf **[!UICONTROL Save]**. In den nächsten Schritten richten Sie die Konfigurationen für jede Produktvariante ein.

## Teil 2: Hinzufügen von Konfigurationen

Im folgenden Beispiel wird gezeigt, wie Konfigurationen für drei Farben und drei Größen hinzugefügt werden. Insgesamt werden neun einfache Produkte mit einzigartigen SKUs erstellt, um jede mögliche Kombination von Varianten abzudecken. Standardmäßig basieren der Produktname und die SKU für jede Variante auf dem Attributwert und entweder dem übergeordneten Produktnamen oder der SKU.

Die Fortschrittsleiste am oberen Seitenrand zeigt an, wo Sie sich im Prozess befinden, und führt Sie durch jeden Schritt.

### Schritt 1: Attribute auswählen

1. Scrollen Sie weiter oben zum Abschnitt _[!UICONTROL Configurations]_hinunter und klicken Sie auf **[!UICONTROL Create Configurations]**.

   ![Konfigurationen](./assets/product-configurable-create-configurations.png){width="600" zoomable="yes"}

1. Aktivieren Sie das Kontrollkästchen jedes Attributs, das Sie als Konfiguration einbeziehen möchten.

   Für dieses Beispiel sind `color` und `size` ausgewählt.

   ![Attribute auswählen](./assets/product-create-configurable-step1.png){width="600" zoomable="yes"}

   Die Liste enthält alle Attribute aus dem Attributsatz, die in einem konfigurierbaren Produkt verwendet werden können.

1. Wenn Sie ein Attribut hinzufügen möchten, klicken Sie auf **[!UICONTROL Create New Attribute]** und führen Sie die folgenden Schritte aus:

   - Füllen Sie die Attributeigenschaften aus.

   - Klicken Sie auf **[!UICONTROL Save Attribute]**.

   - Aktivieren Sie das Kontrollkästchen für das Attribut.

1. Klicken Sie in der oberen rechten Ecke auf **[!UICONTROL Next]**.

### Schritt 2: Attributwerte eingeben

1. Aktivieren Sie für jedes Attribut das Kontrollkästchen der Werte, die für das Produkt gelten.

   ![Attributwerte](./assets/product-create-configurable-step2.png){width="600" zoomable="yes"}

1. Um die Attribute neu anzuordnen, greifen Sie auf das Symbol _Neu anordnen_ ( ![Symbol &quot;Sortierreihenfolge&quot;](../assets/icon-sort-order.png) ) und verschieben Sie den Abschnitt an eine neue Position.

   Die Reihenfolge bestimmt die Position der Dropdownlisten auf der Produktseite.

1. Klicken Sie in der Fortschrittsleiste auf **[!UICONTROL Next]**.

### Schritt 3: Bilder, Preise und Menge konfigurieren

Dieser Schritt bestimmt die Bilder, Preise und Menge jeder Konfiguration. Die verfügbaren Optionen sind für jede Option identisch und Sie können nur eine auswählen. Sie können dieselbe Einstellung auf alle SKUs anwenden, eine eindeutige Einstellung auf jede SKU anwenden oder die Einstellungen vorerst überspringen.

Wählen Sie die zutreffenden Konfigurationsoptionen aus.

Verwenden Sie eine der folgenden Methoden, um den **[!UICONTROL images]** zu konfigurieren:

**Methode 1:** Anwenden eines einzelnen Bildsatzes auf alle SKUs

1. Wählen Sie **[!UICONTROL Apply single set of images to all SKUs]** aus.

1. Navigieren Sie zu jedem Bild, das Sie in die Produktgalerie aufnehmen möchten, oder ziehen Sie es in das Feld.

![Verwenden Sie dieselben Bilder für alle SKUs](./assets/product-configurations-images-apply-single-set.png){width="600" zoomable="yes"}

**Methode 2:** Anwenden eindeutiger Bilder für jede SKU

Da das Bild für das übergeordnete Produkt bereits hochgeladen wurde, können Sie mit dieser Option ein Bild jeder Farbe hochladen. Sie können ein anderes Bild hinzufügen, das im Warenkorb angezeigt wird, wenn jemand den Artikel in einer bestimmten Farbe kauft.

1. Wählen Sie **[!UICONTROL Apply unique images by attribute to each SKU]** aus.

1. Wählen Sie den **[!UICONTROL Attribute]** aus, den die Bilder illustrieren, z. B. `color`.

1. Durchsuchen Sie für jeden Attributwert die Bilder, die Sie für diese Konfiguration verwenden möchten, oder ziehen Sie sie in das Feld.

   Wenn Sie das Bild in ein Wertefeld ziehen, wird es auch in den Abschnitten für die anderen Werte angezeigt. Wenn Sie ein Bild löschen möchten, klicken Sie auf das Symbol &quot;_Papierkorb_&quot;(![Papierkorbsymbol](../assets/icon-delete-trashcan-solid.png)).

   ![Eindeutige Bilder pro SKU](./assets/product-configurable-create-configurations-add-images-unique.png){width="600" zoomable="yes"}

Verwenden Sie eine der folgenden Methoden, um den **[!UICONTROL prices]** zu konfigurieren:

>[!NOTE]
>
>Ein konfigurierbares Produkt hat keinen eigenen Preis im Katalog. Der konfigurierbare Produktpreis wird von den untergeordneten [!UICONTROL In Stock] -Produkten abgeleitet.

**Methode 1:** Wenden Sie denselben Preis auf alle SKUs an

1. Wenn der Preis für alle Varianten gleich ist, wählen Sie **[!UICONTROL Apply single price to all SKUs]** aus.

1. Geben Sie den Wert **[!UICONTROL Price]** ein.

   ![Derselbe Preis pro SKU](./assets/product-configurable-create-configurations-price-all-skus.png){width="600" zoomable="yes"}

**Methode 2:** Anwenden eines anderen Preises für jede SKU

1. Wenn der Preis für jede oder für einige Varianten des Produkts unterschiedlich ist, wählen Sie **[!UICONTROL Apply unique prices by attribute to each SKU]** aus.

1. Wählen Sie die **[!UICONTROL Attribute]** aus, die die Grundlage der Preisdifferenz darstellt.

1. Geben Sie für jeden Attributwert den Wert **[!UICONTROL Price]** ein.

   In diesem Beispiel kostet die XL-Größe mehr.

   ![Eindeutiger Preis pro SKU](./assets/product-configurable-create-configurations-price-unique.png){width="600" zoomable="yes"}

Verwenden Sie eine der folgenden Methoden, um den **[!UICONTROL Quantity]** zu konfigurieren:

**Methode 1:** Wenden Sie dieselbe Menge auf alle SKUs an

Wenn die Menge für alle SKUs identisch ist, wählen Sie **[!UICONTROL Apply single quantity to each SKU]** und geben Sie die Menge an.

_Einzelquellenhändler_ - Geben Sie den **[!UICONTROL Quantity]** ein.

_Multi-Source-Händler, die [Inventory management](../inventory-management/introduction.md)_ verwenden: Weisen Sie Quellen zu und fügen Sie Mengen für alle generierten Produktvarianten hinzu:

1. Wählen Sie die Option **[!UICONTROL Apply single quantity to each SKU]** aus.

1. Um eine Quelle hinzuzufügen, klicken Sie auf **[!UICONTROL Assign Sources]**.

1. Suchen Sie nach einer Quelle, die Sie hinzufügen möchten. Aktivieren Sie das Kontrollkästchen neben den Quellen, die Sie für das Produkt hinzufügen möchten.

1. Geben Sie einen Inventarbetrag pro Quelle an.

   ![Einzelne Menge für alle SKUs, Quelle zuweisen](./assets/inventory-configure-product-quantity.png){width="600" zoomable="yes"}

**Methode 2:** Anwenden einer anderen Menge nach Attribut

_Einzelquellenhändler_ - Geben Sie den **[!UICONTROL Quantity]** ein.

_Multi-Source-Händler, die [Inventory management](../inventory-management/introduction.md)_ verwenden: Weisen Sie Quellen zu und fügen Sie Mengen für alle generierten Produktvarianten hinzu:

1. Wenn die Menge für jede SKU unterschiedlich ist, wählen Sie **[!UICONTROL Apply unique quantity by attribute to each SKU]** aus.

1. Geben Sie jeweils den Wert **[!UICONTROL Quantity]** ein.

   ![Verschiedene Mengen pro Attribut](./assets/product-configurations-quantity-different.png){width="600" zoomable="yes"}

Wenn die Konfiguration für Bilder, Preise und Menge abgeschlossen ist, klicken Sie oben rechts auf **[!UICONTROL Next]** .

### Schritt 4: Produktkonfigurationen generieren

Warten Sie einen Moment, bis die Liste der Produkte angezeigt wird, und führen Sie einen der folgenden Schritte aus:

- Wenn Sie mit den Konfigurationen zufrieden sind, klicken Sie auf **[!UICONTROL Generate Products]**.

- Klicken Sie auf &quot;**[!UICONTROL Back]**&quot;, um Korrekturen vorzunehmen.

![Überprüfen Sie die Zusammenfassung, bevor Sie Produktvarianten generieren](./assets/product-create-configurable-summary.png){width="600" zoomable="yes"}

Die aktuellen Produktvarianten werden unten im Abschnitt _Konfiguration_ angezeigt.

![Aktuelle Konfigurationen](./assets/product-create-configurable-generated.png){width="600" zoomable="yes"}

### Schritt 5: Hinzufügen von Produktbildern

1. Scrollen Sie nach unten und erweitern Sie den Abschnitt _[!UICONTROL Images and Videos]_um den ![Erweiterungsselektor](../assets/icon-display-expand.png).

1. Klicken Sie auf die Kachel _Kamera_ und navigieren Sie zum Hauptbild, das Sie für das konfigurierbare Produkt verwenden möchten.

Weitere Informationen finden Sie unter [Bilder und Videos](product-images-and-video.md).

### Schritt 6: Produktinformationen ausfüllen

Scrollen Sie nach unten und füllen Sie die Informationen in den folgenden Abschnitten nach Bedarf aus:

- [Inhalt](product-content.md)

- [Zugehörige Produkte, Up-Sells und Cross-Sells](related-products-up-sells-cross-sells.md)

- [Suchmaschinenoptimierung](product-search-engine-optimization.md)

- [Anpassbare Optionen](settings-advanced-custom-options.md)

- [Produkte in Websites](settings-basic-websites.md)

- [Design](settings-advanced-design.md)

- [Geschenkoptionen](product-gift-options.md)

### Schritt 7: Publish des Produkts

1. Wenn Sie bereit sind, das Produkt im Katalog zu veröffentlichen, setzen Sie **[!UICONTROL Enable Product]** auf `Yes` und führen Sie einen der folgenden Schritte aus:

   - **Methode 1:** Speichern und Vorschau anzeigen

      - Klicken Sie in der oberen rechten Ecke auf **[!UICONTROL Save]**.

      - Um das Produkt in Ihrem Store anzuzeigen, wählen Sie im Menü _Admin_ ( ![Menüpfeil](../assets/icon-menu-down-arrow-black.png) ) die Option **[!UICONTROL Customer View]** aus.

     Der Store wird in einer neuen Browser-Registerkarte geöffnet.

     ![Kundenansicht](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   - **Methode 2:** Speichern und schließen

     Wählen Sie im Menü _[!UICONTROL Save]_( ![Menüpfeil](../assets/icon-menu-down-arrow-red.png){width="25"} ) die Option **[!UICONTROL Save & Close]**.

### Schritt 8: Konfigurieren Sie die Miniaturansichten des Warenkorbs

Wenn Sie für jede Variante ein anderes Bild haben, können Sie die Konfiguration so konfigurieren, dass das richtige Bild für die Warenkorbminiatur verwendet wird.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bedienfeld den Wert **[!UICONTROL Sales]** und wählen Sie unter &quot;**[!UICONTROL Checkout]**&quot;.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt _[!UICONTROL Shopping Cart]_.

1. Setzen Sie **[!UICONTROL Configurable Product Image]** auf `Product Thumbnail Itself`.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

   ![Warenkorb - konfigurierbares Produktbild](./assets/config-checkout-configurable-product.png){width="600" zoomable="yes"}

## Konfigurieren des Lagerstatus

Der konfigurierbare Produktstatus unterscheidet sich vom Lagerstatus des einfachen Produkts, wobei es sich um eine direkte Darstellung der Produktverfügbarkeit handelt. Bei einem konfigurierbaren Produkt ist der Lagerstatus Teil einer **_Berechnung des Aktienstatus mit mehreren Kriterien_**.

### Übersicht

Die wichtigsten Grundsätze für die Beziehungen zum Lagerstatus sind:

- Wenn Sie den **[!UICONTROL Stock Status]** des konfigurierbaren Produkts in `Out of Stock` ändern und auf **[!UICONTROL Save]** klicken, wird er **_nicht durch den Lagerstatus seiner untergeordneten Produkte gesteuert_**. Er wird immer als `Out of Stock` in der Admin- und Storefront angezeigt.

- Wenn Sie den **[!UICONTROL Stock Status]** des konfigurierbaren Produkts auf `In Stock` setzen und auf **[!UICONTROL Save]** klicken, wird **_nur teilweise durch den Lagerstatus der untergeordneten Produkte gesteuert, was in der Admin- und Storefront angezeigt wird._**

### Detaillierte Beschreibung

Der _Lagerstatus_ des konfigurierbaren Produkts wird teilweise durch den Lagerstatus seiner untergeordneten Produkte und gemäß den folgenden **_Mehrfachkriterien_** Bestandsstatusberechnungen gesteuert:

#### Nur Standardquelle/Lager:

- Wenn der konfigurierbare Produktspeicherstatus von einem Admin-Benutzer, Dateiimport oder API-Aufruf auf **_manuell_** festgelegt ist, bleibt er sowohl für den **_Admin_** als auch für den **_Storefront_** als `Out of Stock`, bis er von einem Admin-Benutzer, Dateiimport oder API-Aufruf auf **_manuell_** geändert wird. `Out of Stock``In stock` Sie kann nicht durch den Bestandsstatus ihrer untergeordneten Produkte kontrolliert werden.

- Wenn der konfigurierbare Produktspeicherstatus von einem Admin-Benutzer, Dateiimport oder API-Aufruf auf **_manuell_** festgelegt wird, wird der Lagerstatus von **_automatisch_** durch den Lagerstatus seiner untergeordneten Produkte sowohl in der **_Admin_** als auch in der **_Storefront_** gesteuert.`In Stock`

>[!NOTE]
>
>Benutzerdefinierte Lager und Quellen sind Teil der Erweiterung [Inventory management](../inventory-management/sources-stocks.md) und es wird dringend empfohlen, dieses Tool ausschließlich für die Verwaltung von Lagern und Quellen zu verwenden. Die standardmäßigen Quell- und Lagerfunktionen sind Teil des Moduls `CatalogInventory`, das jetzt nicht mehr unterstützt wird.

#### Mit mindestens einer benutzerdefinierten Quelle/Lager:

- Wenn der konfigurierbare Wert für den Produktstatus-Status **_manuell_** von einem Admin-Benutzer, Dateiimport oder API-Aufruf auf `Out of Stock` festgelegt ist, bleibt er sowohl in der **_Admin_**- als auch in der **_Storefront_** als `Out of Stock` erhalten, bis er von einem Admin-Benutzer, Dateiimport oder API-Aufruf auf **_manuell_** geändert wird. `In Stock` Er kann **_nicht_** durch den Lagerstatus seiner untergeordneten Produkte gesteuert werden.

- Wenn der konfigurierbare Wert für den Produktstatus &quot;Stock Status&quot;von einem Admin-Benutzer, Dateiimport oder API-Aufruf auf &quot;**_manuell_**&quot;`In Stock` festgelegt ist, wird sein Lagerstatus nur durch den Lagerstatus seiner untergeordneten Produkte in der **_Storefront_** automatisch gesteuert.**__**

- Wenn der konfigurierbare Wert für den Produktstatus-Status **_manuell_** von einem Admin-Benutzer, Dateiimport oder API-Aufruf auf `In Stock` festgelegt ist, bleibt er im **_Admin_** als `In Stock` erhalten, bis er von einem Admin-Benutzer, Dateiimport oder API-Aufruf auf **_manuell_** geändert wird. `Out of Stock` Er kann **_nicht_** durch den Lagerstatus seiner untergeordneten Produkte gesteuert werden.

## Dinge, die man sich merken sollte

- Ein konfigurierbares Produkt ermöglicht es dem Käufer, Optionen aus Dropdown-, Mehrfachauswahl-, visuellen Farb- und Textmuster-Eingabetypen auszuwählen. Jede Option ist ein separates, einfaches Produkt.

- [Lagerstatus](../inventory-management/sources-stocks.md) für ein konfigurierbares Produkt ist eine halbmanuell gesteuerte Einstellung. Sie unterscheidet sich vom Lagerstatus des einfachen Produkts, wobei es sich um eine direkte Darstellung der Produktverfügbarkeit handelt. Bei einem konfigurierbaren Produkt ist der Lagerstatus Teil einer Berechnung des Aktienstatus mit mehreren Kriterien.

- Konfigurierbare untergeordnete Produkte können einfache oder virtuelle Produkte **ohne benutzerdefinierte Optionen** sein. Um benutzerdefinierte untergeordnete Produkte virtuell zu machen, müssen Sie für jede dieser Optionen **[!UICONTROL Weight]** als Einstellung wählen.`Тhis item has no weight`

- Alle untergeordneten Produkte werden dem konfigurierbaren Produkt **_global_** zugewiesen und nicht zugewiesen. Dies gilt für alle Websites, Stores und Storeansichten gleichzeitig.

- Ein konfigurierbares Produkt hat keinen eigenen Preis im Katalog. Der konfigurierbare Produktpreis wird von den untergeordneten [!UICONTROL In Stock] -Produkten abgeleitet.

- Die Attribute, die für Produktvarianten verwendet werden, müssen einen globalen Umfang aufweisen und der Kunde muss einen Wert auswählen müssen. Die Produktvariantenattribute müssen in den Attributsatz aufgenommen werden, der als Vorlage für das konfigurierbare Produkt verwendet wird.

- Der Attributsatz, der als Vorlage für ein konfigurierbares Produkt verwendet wird, muss die Attribute enthalten, die die Werte enthalten, die für jede Produktvariante benötigt werden.

- Das Miniaturbild im Warenkorb kann so eingestellt werden, dass es das Bild aus dem konfigurierbaren Produktdatensatz oder aus der Produktvariante anzeigt.

- [Farbfeldattribute](swatches.md#create-swatches-for-products) können so konfiguriert werden, dass keine entsprechenden einfachen Produktbilder angezeigt werden, wenn das Muster ausgewählt wird, indem der Optionswert **[!UICONTROL Update Product Preview Image]** auf der Attributbearbeitungsseite in der Admin-Konsole auf `No` gesetzt wird.

- Das Design steuert, wie sich die Image Gallery verhält, wenn ein Benutzer zwischen Produktkonfigurationen wechselt. Das Standardverhalten des Designs _Leer_ besteht darin, die übergeordneten konfigurierbaren Produktbilder mit der ausgewählten Produktvariante zu überschreiben. Beim Thema Luma besteht das Standardverhalten darin, den übergeordneten konfigurierbaren Produktbildern die ausgewählten Produktvariantenbilder vorzuhängen.
