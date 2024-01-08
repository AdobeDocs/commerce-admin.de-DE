---
title: Konfigurierbares Produkt
description: Erfahren Sie, wie Sie ein konfigurierbares Produkt erstellen, das den Käufern Varianten zur Auswahl bietet.
exl-id: 2066fd20-5227-41e9-b213-31825a58ebd9
feature: Catalog Management, Products
source-git-commit: f6140fda2769e109d2b38c2f9c458f67097dff0a
workflow-type: tm+mt
source-wordcount: '2483'
ht-degree: 0%

---

# Konfigurierbares Produkt

Ein konfigurierbares Produkt sieht aus wie ein einzelnes Produkt mit einer Dropdown-Liste jeder Variante. Jedes Listenelement ist tatsächlich ein separates einfaches Produkt mit einer eindeutigen SKU, die es ermöglicht, das Inventar für jede Produktvariante zu verfolgen. Sie können einen ähnlichen Effekt erzielen, indem Sie ein einfaches Produkt mit benutzerdefinierten Optionen verwenden, aber ohne die Möglichkeit, Inventar für jede Variante zu verfolgen.

Die folgenden Anweisungen zeigen den Prozess der Erstellung eines konfigurierbaren Produkts mit einem [Produktvorlage](attribute-sets.md), erforderliche Felder und grundlegende Einstellungen. Jedes erforderliche Feld ist mit einem roten Sternchen (`*`). Wenn Sie die Grundlagen abgeschlossen haben, können Sie die anderen Produkteinstellungen nach Bedarf abschließen.

![Konfigurierbares Produkt](./assets/product-configurable.png){width="700" zoomable="yes"}

## Teil 1: Erstellen eines konfigurierbaren Produkts

Obwohl ein konfigurierbares Produkt mehr SKUs verwendet und die Einrichtung zunächst etwas länger dauern kann, kann es am Ende Zeit sparen. Wenn Sie Ihr Unternehmen erweitern möchten, ist der konfigurierbare Produkttyp eine gute Wahl für Produkte mit mehreren Optionen.

Bevor Sie beginnen, bereiten Sie eine [Attributset](attribute-sets.md) , das ein Attribut enthält, das auf einen der zulässigen Eingabetypen für jede Produktvariante festgelegt ist. Beispielsweise kann der Attributsatz Dropdown-Attribute für Farbe und Größe enthalten.

Die Eigenschaften jedes Attributs, das für eine konfigurierbare Produktvariante verwendet wird, müssen die folgenden Einstellungen aufweisen:

### Attributanforderungen für Produktvarianten

| Eigenschaft | Einstellung |
|--- |--- |
| [!UICONTROL Scope] | `Global` |
| [!UICONTROL Catalog Input Type for Store Owner] | Der Eingabetyp eines Attributs, das für eine Produktvariante verwendet wird, muss einer der folgenden sein: `Dropdown`, `Visual Swatch`oder `Text Swatch`. |
| [!UICONTROL Values Required] | `Yes` |

{style="table-layout:auto"}

### Schritt 1: Produkttyp auswählen

1. Im _Admin_ Seitenleiste, navigieren Sie zu  **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Im _[!UICONTROL Add Product]_( ![Menüpfeil](../assets/icon-menu-down-arrow-red.png){width="25"} ) in der oberen rechten Ecke auswählen **[!UICONTROL Configurable Product]**.

   ![Konfigurierbares Produkt hinzufügen](./assets/product-add-configurable.png){width="700" zoomable="yes"}

### Schritt 2: Attributsatz auswählen

Die [Attributset](attribute-sets.md) bestimmt die Auswahl der Felder, die im Produkt verwendet werden. Der im folgenden Beispiel verwendete Attributsatz hat Attribute für Farbe und Größe. Der Name des Attributsatzes wird oben auf der Seite angezeigt und zunächst auf `Default`.

1. Um den Attributsatz für das Produkt auszuwählen, klicken Sie auf das Feld oben auf der Seite und führen Sie einen der folgenden Schritte aus:

   - Für **[!UICONTROL Search]**, geben Sie den Namen des Attributsatzes ein.
   - Wählen Sie in der Liste den Attributsatz aus, den Sie verwenden möchten.

   Das Formular wird entsprechend der Änderung aktualisiert.

1. Wenn Sie dem Attributsatz ein weiteres Attribut hinzufügen möchten, klicken Sie auf **[!UICONTROL Add Attribute]** und befolgen Sie die Anweisungen unter [Hinzufügen eines Attributs](product-attributes-add.md).

   ![Vorlage auswählen](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

### Schritt 3: Ausführen der erforderlichen Einstellungen

1. Produkt eingeben **[!UICONTROL Product Name]**.

1. Standard akzeptieren **[!UICONTROL SKU]** , der auf dem Produktnamen basiert, oder geben Sie einen anderen ein.

1. Produkt eingeben **[!UICONTROL Price]**.

1. Da das Produkt noch nicht zur Veröffentlichung bereit ist, legen Sie **[!UICONTROL Enable Product]** nach `No`.

1. click **[!UICONTROL Save]** und fortfahren.

   Wenn das Produkt gespeichert wird, wird die [Store-Ansicht](introduction.md#product-scope) wird in der linken oberen Ecke angezeigt.

1. Wählen Sie die **[!UICONTROL Store View]** wo das Produkt verfügbar sein soll.

   ![Auswählen der Store-Ansicht](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

### Schritt 4: Grundlegende Einstellungen durchführen

1. Satz **[!UICONTROL Tax Class]** auf einen der folgenden Werte zu:

   - `None`
   - `Taxable Goods`

1. Die **[!UICONTROL Quantity]** wird durch die Produktvarianten bestimmt, sodass Sie es leer lassen können.

1. Lassen Sie die **[!UICONTROL Stock Status]** festgelegt ist.

   Der Lagerstatus eines konfigurierbaren Produkts wird durch jede zugeordnete Konfiguration bestimmt. Da das Produkt ohne Eingabe einer Menge gespeichert wurde, wird die **[!UICONTROL Stock Status]** auf `Out of Stock`.

   >[!NOTE]
   >
   >Die **Lagerstatus** des konfigurierbaren Produkts ist ein **_halbmanuell_** geregelte Einstellung. Sie wird zum Teil durch den Bestandsstatus ihrer untergeordneten Produkte kontrolliert. Es ist Teil eines **_Mehrfachkriterien_** Berechnung des Aktienstatus, wie im Abschnitt [Konfigurieren des Lagerstatus](#configure-the-stock-status) Abschnitt.

1. Produkt eingeben **[!UICONTROL Weight]**.

>[!NOTE]
>
>Ein konfigurierbares Produkt muss immer eine Gewichtung aufweisen. Wenn Sie **[!UICONTROL This item has no weight]** aus der Dropdown-Liste wird er automatisch in **[!UICONTROL This item has weight]** nach dem Speichern des Produkts.

1. Standard akzeptieren **[!UICONTROL Visibility]** Einstellung von `Catalog, Search`.

1. So stellen Sie das Produkt in der Liste der [neue Produkte](../content-design/widget-new-products-list.md), wählen Sie die **[!UICONTROL Set Product as New]** aktivieren.

1. Um dem Produkt Kategorien zuzuweisen, klicken Sie auf das **[!UICONTROL Select…]** und führen Sie einen der folgenden Schritte aus:

   **Vorhandene Kategorie auswählen**:

   - Beginnen Sie mit der Eingabe in das Feld, bis Sie eine Übereinstimmung finden.

   - Aktivieren Sie das Kontrollkästchen der Kategorie, die zugewiesen werden soll.

   ![Wählen Sie eine oder mehrere Kategorien für das Paket-Produkt aus](./assets/product-create-categories.png){width="600" zoomable="yes"}

   **Erstellen einer Kategorie**:

   - Klicks **[!UICONTROL New Category]**.

   - Geben Sie die **[!UICONTROL Category Name]** und wählen Sie **[!UICONTROL Parent Category]**, der seine Position in der Menüstruktur bestimmt.

   s-Click **[!UICONTROL Create Category]**.

1. Wählen Sie die **[!UICONTROL Country of Manufacture]**.

   Es kann zusätzliche Attribute geben, mit denen das Produkt beschrieben wird. Die Auswahl variiert je nach Attributsatz und kann zu einem späteren Zeitpunkt abgeschlossen werden.

### Schritt 5: Speichern und fortfahren

Jetzt ist eine gute Zeit, um Ihre Arbeit zu retten. Klicken Sie oben rechts auf **[!UICONTROL Save]**. In den nächsten Schritten richten Sie die Konfigurationen für jede Produktvariante ein.

## Teil 2: Hinzufügen von Konfigurationen

Im folgenden Beispiel wird gezeigt, wie Konfigurationen für drei Farben und drei Größen hinzugefügt werden. Insgesamt werden neun einfache Produkte mit einzigartigen SKUs erstellt, um jede mögliche Kombination von Varianten abzudecken. Standardmäßig basieren der Produktname und die SKU für jede Variante auf dem Attributwert und entweder dem übergeordneten Produktnamen oder der SKU.

Die Fortschrittsleiste am oberen Seitenrand zeigt an, wo Sie sich im Prozess befinden, und führt Sie durch jeden Schritt.

### Schritt 1: Attribute auswählen

1. Scrollen Sie von oben nach unten zum _[!UICONTROL Configurations]_und klicken Sie auf **[!UICONTROL Create Configurations]**.

   ![Konfigurationen](./assets/product-configurable-create-configurations.png){width="600" zoomable="yes"}

1. Aktivieren Sie das Kontrollkästchen jedes Attributs, das Sie als Konfiguration einbeziehen möchten.

   In diesem Beispiel `color` und `size` ausgewählt sind.

   ![Attribute auswählen](./assets/product-create-configurable-step1.png){width="600" zoomable="yes"}

   Die Liste enthält alle Attribute aus dem Attributsatz, die in einem konfigurierbaren Produkt verwendet werden können.

1. Wenn Sie ein Attribut hinzufügen möchten, klicken Sie auf **[!UICONTROL Create New Attribute]** und gehen Sie wie folgt vor:

   - Füllen Sie die Attributeigenschaften aus.

   - Klicks **[!UICONTROL Save Attribute]**.

   - Aktivieren Sie das Kontrollkästchen für das Attribut.

1. Klicken Sie oben rechts auf **[!UICONTROL Next]**.

### Schritt 2: Attributwerte eingeben

1. Aktivieren Sie für jedes Attribut das Kontrollkästchen der Werte, die für das Produkt gelten.

   ![Attributwerte](./assets/product-create-configurable-step2.png){width="600" zoomable="yes"}

1. Um die Attribute neu anzuordnen, rufen Sie die _Neu anordnen_ ( ![Symbol &quot;Sortierung&quot;](../assets/icon-sort-order.png) ) und verschieben Sie den Abschnitt an eine neue Position.

   Die Reihenfolge bestimmt die Position der Dropdownlisten auf der Produktseite.

1. Klicken Sie in der Fortschrittsleiste auf **[!UICONTROL Next]**.

### Schritt 3: Bilder, Preise und Menge konfigurieren

Dieser Schritt bestimmt die Bilder, Preise und Menge jeder Konfiguration. Die verfügbaren Optionen sind für jede Option identisch und Sie können nur eine auswählen. Sie können dieselbe Einstellung auf alle SKUs anwenden, eine eindeutige Einstellung auf jede SKU anwenden oder die Einstellungen vorerst überspringen.

Wählen Sie die zutreffenden Konfigurationsoptionen aus.

Verwenden Sie eine der folgenden Methoden, um die **[!UICONTROL images]**:

**Methode 1:** Anwenden eines einzigen Bildsatzes auf alle SKUs

1. Auswählen **[!UICONTROL Apply single set of images to all SKUs]**.

1. Navigieren Sie zu jedem Bild, das Sie in die Produktgalerie aufnehmen möchten, oder ziehen Sie es in das Feld.

![Verwenden Sie dieselben Bilder für alle SKUs.](./assets/product-configurations-images-apply-single-set.png){width="600" zoomable="yes"}

**Methode 2:** Anwenden eindeutiger Bilder für jede SKU

Da das Bild für das übergeordnete Produkt bereits hochgeladen wurde, können Sie mit dieser Option ein Bild jeder Farbe hochladen. Sie können ein anderes Bild hinzufügen, das im Warenkorb angezeigt wird, wenn jemand den Artikel in einer bestimmten Farbe kauft.

1. Auswählen **[!UICONTROL Apply unique images by attribute to each SKU]**.

1. Wählen Sie die **[!UICONTROL Attribute]** dass die Bilder illustrieren, z. B. `color`.

1. Durchsuchen Sie für jeden Attributwert die Bilder, die Sie für diese Konfiguration verwenden möchten, oder ziehen Sie sie in das Feld.

   Wenn Sie das Bild in ein Wertefeld ziehen, wird es auch in den Abschnitten für die anderen Werte angezeigt. Wenn Sie ein Bild löschen möchten, klicken Sie auf die _Papierkorb_ (![Papierkorbsymbol](../assets/icon-delete-trashcan-solid.png)).

   ![Eindeutige Bilder pro SKU](./assets/product-configurable-create-configurations-add-images-unique.png){width="600" zoomable="yes"}

Verwenden Sie eine der folgenden Methoden, um die **[!UICONTROL prices]**:

>[!NOTE]
>
>Ein konfigurierbares Produkt hat keinen eigenen Preis im Katalog. Der konfigurierbare Produktpreis ergibt sich aus dem [!UICONTROL In Stock] untergeordnete Produkte.

**Methode 1:** Den gleichen Preis auf alle SKUs anwenden

1. Wenn der Preis für alle Varianten gleich ist, wählen Sie **[!UICONTROL Apply single price to all SKUs]**.

1. Geben Sie die **[!UICONTROL Price]**.

   ![Gleicher Preis pro SKU](./assets/product-configurable-create-configurations-price-all-skus.png){width="600" zoomable="yes"}

**Methode 2:** Anwenden eines anderen Preises für jede SKU

1. Wenn der Preis für jede oder für einige Varianten des Produkts unterschiedlich ist, wählen Sie **[!UICONTROL Apply unique prices by attribute to each SKU]**.

1. Wählen Sie die **[!UICONTROL Attribute]** die Grundlage der Preisdifferenz ist.

1. Geben Sie die **[!UICONTROL Price]** für jeden Attributwert.

   In diesem Beispiel kostet die XL-Größe mehr.

   ![Einzelpreis pro SKU](./assets/product-configurable-create-configurations-price-unique.png){width="600" zoomable="yes"}

Verwenden Sie eine der folgenden Methoden, um die **[!UICONTROL Quantity]**:

**Methode 1:** Dieselbe Menge auf alle SKUs anwenden

Wenn die Menge für alle SKUs identisch ist, wählen Sie **[!UICONTROL Apply single quantity to each SKU]** und geben Sie die Menge an.

_Einzelquell-Händler_ - Geben Sie die **[!UICONTROL Quantity]**.

_Multi-Source-Händler mit [Inventory management](../inventory-management/introduction.md)_ - Weisen Sie Quellen zu und fügen Sie für alle erzeugten Produktvarianten Mengen hinzu:

1. Wählen Sie die **[!UICONTROL Apply single quantity to each SKU]** -Option.

1. Um eine Quelle hinzuzufügen, klicken Sie auf **[!UICONTROL Assign Sources]**.

1. Suchen Sie nach einer Quelle, die Sie hinzufügen möchten. Aktivieren Sie das Kontrollkästchen neben den Quellen, die Sie für das Produkt hinzufügen möchten.

1. Geben Sie einen Inventarbetrag pro Quelle an.

   ![Einzelne Menge für alle SKUs, Quelle zuweisen](./assets/inventory-configure-product-quantity.png){width="600" zoomable="yes"}

**Methode 2:** Anwenden einer anderen Menge nach Attribut

_Einzelquell-Händler_ - Geben Sie die **[!UICONTROL Quantity]**.

_Multi-Source-Händler mit [Inventory management](../inventory-management/introduction.md)_ - Weisen Sie Quellen zu und fügen Sie für alle erzeugten Produktvarianten Mengen hinzu:

1. Wenn die Menge für jede SKU unterschiedlich ist, wählen Sie **[!UICONTROL Apply unique quantity by attribute to each SKU]**.

1. Geben Sie die **[!UICONTROL Quantity]** für jede.

   ![Verschiedene Mengen pro Attribut](./assets/product-configurations-quantity-different.png){width="600" zoomable="yes"}

Klicken Sie nach Abschluss der Konfiguration für Bilder, Preise und Menge auf **[!UICONTROL Next]** in der oberen rechten Ecke.

### Schritt 4: Produktkonfigurationen generieren

Warten Sie einen Moment, bis die Liste der Produkte angezeigt wird, und führen Sie einen der folgenden Schritte aus:

- Wenn Sie mit den Konfigurationen zufrieden sind, klicken Sie auf **[!UICONTROL Generate Products]**.

- Um Korrekturen vorzunehmen, klicken Sie auf **[!UICONTROL Back]**.

![Lesen Sie die Zusammenfassung, bevor Sie Produktvarianten generieren](./assets/product-create-configurable-summary.png){width="600" zoomable="yes"}

Die aktuellen Produktvarianten werden unten in der _Konfiguration_ Abschnitt.

![Aktuelle Konfigurationen](./assets/product-create-configurable-generated.png){width="600" zoomable="yes"}

### Schritt 5: Hinzufügen von Produktbildern

1. Hinunter scrollen und erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die _[!UICONTROL Images and Videos]_Abschnitt.

1. Klicken Sie auf _Kamera_ und navigieren Sie zum Hauptbild, das Sie für das konfigurierbare Produkt verwenden möchten.

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

### Schritt 7: Produkt veröffentlichen

1. Wenn Sie bereit sind, das Produkt im Katalog zu veröffentlichen, legen Sie **[!UICONTROL Enable Product]** nach `Yes` und führen Sie einen der folgenden Schritte aus:

   - **Methode 1:** Speichern und Vorschau anzeigen

      - Klicken Sie oben rechts auf **[!UICONTROL Save]**.

      - Um das Produkt in Ihrem Geschäft anzuzeigen, wählen Sie **[!UICONTROL Customer View]** auf _Admin_ ( ![Menüpfeil](../assets/icon-menu-down-arrow-black.png) ).

     Der Store wird in einer neuen Browser-Registerkarte geöffnet.

     ![Kundenansicht](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   - **Methode 2:** Speichern und schließen

     Im _[!UICONTROL Save]_( ![Menüpfeil](../assets/icon-menu-down-arrow-red.png){width="25"} ), wählen Sie **[!UICONTROL Save & Close]**.

### Schritt 8: Konfigurieren Sie die Miniaturansichten des Warenkorbs

Wenn Sie für jede Variante ein anderes Bild haben, können Sie die Konfiguration so konfigurieren, dass das richtige Bild für die Warenkorbminiatur verwendet wird.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen **[!UICONTROL Checkout]** darunter.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die _[!UICONTROL Shopping Cart]_Abschnitt.

1. Satz **[!UICONTROL Configurable Product Image]** nach `Product Thumbnail Itself`.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

   ![Warenkorb - konfigurierbares Produktbild](./assets/config-checkout-configurable-product.png){width="600" zoomable="yes"}

## Konfigurieren des Lagerstatus

Der konfigurierbare Produktstatus unterscheidet sich vom Lagerstatus des einfachen Produkts, wobei es sich um eine direkte Darstellung der Produktverfügbarkeit handelt. Bei einem konfigurierbaren Produkt ist der Lagerstatus Teil eines **_Mehrfachkriterien_** Berechnung des Aktienstatus.

### Übersicht

Die wichtigsten Grundsätze für die Beziehungen zum Lagerstatus sind:

- Wenn Sie die **[!UICONTROL Stock Status]** des konfigurierbaren Produkts `Out of Stock` und klicken **[!UICONTROL Save]**, ist es **_nicht kontrolliert_** nach dem Bestandsstatus der untergeordneten Erzeugnisse. Sie wird immer als `Out of Stock` in der Admin- und Storefront angezeigt.

- Wenn Sie **[!UICONTROL Stock Status]** des konfigurierbaren Produkts `In Stock` und klicken **[!UICONTROL Save]**, ist es **_nur teilweise kontrolliert_** durch den Lagerstatus der untergeordneten Produkte, der sich in der Admin- und Storefront widerspiegelt.

### Detaillierte Beschreibung

Die _Lagerstatus_ des konfigurierbaren Produkts teilweise durch den Lagerstatus seiner untergeordneten Produkte kontrolliert wird, und zwar gemäß **_Mehrfachkriterien_** Bestandsstatusberechnungen:

#### Nur Standardquelle/Lager:

- Wenn der konfigurierbare Produktstatus &quot;Stock Status&quot;lautet **_manuell_** auf `Out of Stock` von einem Admin-Benutzer, Dateiimport oder API-Aufruf beibehalten als `Out of Stock` auf beiden **_Admin_** und **_Storefront_** bis  **_manuell_** geändert auf `In stock` durch einen Admin-Benutzer, einen Dateiimport oder einen API-Aufruf. Sie kann nicht durch den Bestandsstatus ihrer untergeordneten Produkte kontrolliert werden.

- Wenn der konfigurierbare Produktstatus &quot;Stock Status&quot;lautet **_manuell_** auf `In Stock` durch einen Admin-Benutzer, einen Dateiimport- oder API-Aufruf, lautet der Lagerstatus **_automatisch_** durch den Bestandsstatus seiner untergeordneten Erzeugnisse auf beiden **_Admin_** und **_Storefront_**.

>[!NOTE]
>
>Benutzerdefinierte Bestände und Quellen sind Teil der [Inventory management](../inventory-management/sources-stocks.md) und es wird dringend empfohlen, dieses Tool ausschließlich für die Verwaltung von Lager und Quelle zu verwenden. Die standardmäßigen Quell- und Lagerfunktionen sind Teil der `CatalogInventory` -Modul, das jetzt nicht mehr unterstützt wird.

#### Mit mindestens einer benutzerdefinierten Quelle/Lager:

- Wenn der konfigurierbare Produktstatuswert **_manuell_** auf `Out of Stock` von einem Admin-Benutzer, Dateiimport oder API-Aufruf beibehalten als `Out of Stock` auf beiden **_Admin_** und **_Storefront_** bis **_manuell_** geändert auf `In Stock` durch einen Admin-Benutzer, einen Dateiimport oder einen API-Aufruf. Es **_cannot_** durch den Bestandsstatus seiner untergeordneten Erzeugnisse kontrolliert werden.

- Wenn der konfigurierbare Produktstatuswert **_manuell_** auf `In Stock` durch einen Admin-Benutzer, einen Dateiimport- oder API-Aufruf, lautet der Lagerstatus **_automatisch_** durch den Bestandsstatus seiner untergeordneten Erzeugnisse auf der **_Storefront_** nur.

- Wenn der konfigurierbare Produktstatuswert **_manuell_** auf `In Stock` von einem Admin-Benutzer, Dateiimport oder API-Aufruf beibehalten als `In Stock` im **_Admin_** bis **_manuell_** geändert auf `Out of Stock` durch einen Admin-Benutzer, einen Dateiimport oder einen API-Aufruf. Es **_cannot_** durch den Bestandsstatus seiner untergeordneten Erzeugnisse kontrolliert werden.

## Dinge, die man sich merken sollte

- Ein konfigurierbares Produkt ermöglicht es dem Käufer, Optionen aus Dropdown-, Mehrfachauswahl-, visuellen Farb- und Textmuster-Eingabetypen auszuwählen. Jede Option ist ein separates, einfaches Produkt.

- [Lagerstatus](../inventory-management/sources-stocks.md) für ein konfigurierbares Produkt eine halbmanuell gesteuerte Einstellung ist. Sie unterscheidet sich vom Lagerstatus des einfachen Produkts, wobei es sich um eine direkte Darstellung der Produktverfügbarkeit handelt. Bei einem konfigurierbaren Produkt ist der Lagerstatus Teil einer Berechnung des Aktienstatus mit mehreren Kriterien.

- Konfigurierbare untergeordnete Produkte können einfache oder virtuelle Produkte sein **ohne benutzerdefinierte Optionen**. Um benutzerdefinierte untergeordnete Produkte virtuell zu gestalten, müssen Sie `Тhis item has no weight` für die **[!UICONTROL Weight]** -Einstellung für jeden von ihnen.

- Ein konfigurierbares Produkt hat keinen eigenen Preis im Katalog. Der konfigurierbare Produktpreis ergibt sich aus dem [!UICONTROL In Stock] untergeordnete Produkte.

- Die Attribute, die für Produktvarianten verwendet werden, müssen einen globalen Umfang aufweisen und der Kunde muss einen Wert auswählen müssen. Die Produktvariantenattribute müssen in den Attributsatz aufgenommen werden, der als Vorlage für das konfigurierbare Produkt verwendet wird.

- Der Attributsatz, der als Vorlage für ein konfigurierbares Produkt verwendet wird, muss die Attribute enthalten, die die Werte enthalten, die für jede Produktvariante benötigt werden.

- Das Miniaturbild im Warenkorb kann so eingestellt werden, dass es das Bild aus dem konfigurierbaren Produktdatensatz oder aus der Produktvariante anzeigt.

- [Farbattribute](swatches.md#create-swatches-for-products) kann so konfiguriert werden, dass keine entsprechenden einfachen Produktbilder angezeigt werden, wenn das Farbfeld ausgewählt wird, indem Sie die Einstellung **[!UICONTROL Update Product Preview Image]** Optionswert auf `No` auf der Seite zur Attributbearbeitung in der Admin-Konsole.

- Das Design steuert, wie sich die Image Gallery verhält, wenn ein Benutzer zwischen Produktkonfigurationen wechselt. Das Standardverhalten für die _Leer_ -Design ist es, die übergeordneten konfigurierbaren Produktbilder mit der ausgewählten Produktvariante zu überschreiben. Beim Thema Luma besteht das Standardverhalten darin, den übergeordneten konfigurierbaren Produktbildern die ausgewählten Produktvariantenbilder vorzuhängen.
