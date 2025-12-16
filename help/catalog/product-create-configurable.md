---
title: Konfigurierbares Produkt
description: Erfahren Sie, wie Sie ein konfigurierbares Produkt erstellen, das Käufern Varianten zur Auswahl bietet.
exl-id: 2066fd20-5227-41e9-b213-31825a58ebd9
feature: Catalog Management, Products
source-git-commit: 6fcbcd3b7cace10f0841a46b3cd27343862b3f3b
workflow-type: tm+mt
source-wordcount: '1981'
ht-degree: 0%

---

# Konfigurierbares Produkt

Ein konfigurierbares Produkt wird als einzelnes Produkt mit Dropdown-Optionen für Varianten (wie Farbe oder Größe) angezeigt. Jede Variante ist ein separates einfaches Produkt mit einer eigenen SKU, das eine individuelle Bestandsverfolgung ermöglicht - im Gegensatz zu einfachen Produkten mit benutzerdefinierten Optionen.

**Am besten geeignet für** Produkte mit mehreren Optionen (Farbe, Größe, Material usw.), bei denen Sie den Bestand für jede Variante verfolgen müssen. Die Ersteinrichtung dauert länger, bietet jedoch eine bessere Skalierbarkeit.

![Konfigurierbares Produkt](./assets/product-configurable.png){width="700" zoomable="yes"}

## Bevor Sie beginnen

### Checkliste mit Voraussetzungen

Bevor Sie ein konfigurierbares Produkt erstellen, stellen Sie Folgendes sicher:

1. **Attributsatz** - Ein Attributsatz, der Variantenattribute (wie Farbe und Größe) enthält
1. **Variantenattribute erstellt** - Attribute, die mit den folgenden Einstellungen konfiguriert wurden
1. **Produktbilder** - (Optional, aber empfohlen) Bilder für das übergeordnete Produkt und jede Variante

### Attributanforderungen

Jedes für Produktvarianten verwendete Attribut muss die folgenden Einstellungen aufweisen:

| Eigenschaft | Erforderliche Einstellung |
|--- |--- |
| [!UICONTROL Scope] | `Global` |
| [!UICONTROL Catalog Input Type for Store Owner] | `Dropdown`, `Visual Swatch` oder `Text Swatch` |
| [!UICONTROL Values Required] | `Yes` |

{style="table-layout:auto"}

Anweisungen zum Erstellen von Attributen finden Sie unter [Produktattribute](product-attributes.md).

## Phase 1: Erstellen der Produktgrundlage

### Schritt 1: Produkttyp auswählen

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Wählen Sie im Menü _[!UICONTROL Add Product]_![Menüpfeil](../assets/icon-menu-down-arrow-red.png){width="25"} oben rechts **[!UICONTROL Configurable Product]**aus.

   ![Konfigurierbares Produkt hinzufügen](./assets/product-add-configurable.png){width="700" zoomable="yes"}

### Schritt 2: Attributsatz auswählen

Der [Attributsatz](attribute-sets.md) bestimmt, welche Felder im Produktformular angezeigt werden und welche Attribute für Varianten verfügbar sind.

1. Klicken Sie oben auf der Seite auf das Feld Attributsatz und führen Sie einen der folgenden Schritte aus:

   - Geben Sie **[!UICONTROL Search]** den Namen des Attributsatzes an.
   - Wählen Sie in der Liste den Attributsatz aus, den Sie verwenden möchten.

   Das Formular wird mit dem ausgewählten Attributsatz aktualisiert.

1. Wenn Sie dem Attributsatz ein weiteres Attribut hinzufügen müssen, klicken Sie auf **[!UICONTROL Add Attribute]** und befolgen Sie die Anweisungen unter [Attribut hinzufügen](product-attributes-add.md).

   ![Vorlage wählen](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

### Schritt 3: Grundlegende Informationen eingeben

1. Geben Sie die **[!UICONTROL Product Name]** ein.

1. Akzeptieren Sie die **[!UICONTROL SKU]** basierend auf dem Produktnamen oder geben Sie einen anderen Wert ein.

1. Geben Sie die **[!UICONTROL Price]** ein.

   >[!NOTE]
   >
   >Dieser Preis wird durch die Preise der untergeordneten Produkte überschrieben. Der tatsächliche Preis, der den Kunden angezeigt wird, stammt von den [!UICONTROL In Stock] untergeordneten Produkten.

1. Da das Produkt noch nicht zur Veröffentlichung bereit ist, setzen Sie **[!UICONTROL Enable Product]** auf `No`.

1. Klicken Sie auf **[!UICONTROL Save]** und fahren Sie fort.

   Wenn das Produkt gespeichert wird, wird [ Auswahl „Store](introduction.md#product-scope)Ansicht“ in der oberen linken Ecke angezeigt.

1. Wählen Sie die **[!UICONTROL Store View]** aus, in der das Produkt verfügbar sein soll.

   ![Store-Ansicht auswählen](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

### Schritt 4: Grundeinstellungen abschließen

1. Legen Sie **[!UICONTROL Tax Class]** auf eine der folgenden Einstellungen fest:

   - `None`
   - `Taxable Goods`

1. Lassen Sie **[!UICONTROL Quantity]** leer. Die Menge wird durch die Produktvarianten bestimmt.

1. **[!UICONTROL Stock Status]** als festgelegt belassen.

   Der Lagerstatus eines konfigurierbaren Produkts wird durch die zugehörigen Varianten bestimmt. Da das Produkt ohne Menge gespeichert wurde, wird der **[!UICONTROL Stock Status]** auf `Out of Stock` gesetzt.

   >[!NOTE]
   >
   >Der **Lagerstatus** eines konfigurierbaren Produkts ist eine **_halb manuell_** gesteuerte Einstellung, die teilweise auf dem Lagerstatus seiner untergeordneten Produkte basiert. Sie ist Teil einer **_Mehrkriterien_** Bestandsstatusberechnung. Siehe [Konfigurieren des Lagerstatus](#configure-stock-status) für Details.

1. Geben Sie die **[!UICONTROL Weight]** ein.

   >[!NOTE]
   >
   >Ein konfigurierbares Produkt muss immer eine Gewichtung haben. Wenn Sie im Dropdown-Menü **[!UICONTROL This item has no weight]** auswählen, wird beim Speichern des Produkts automatisch **[!UICONTROL This item has weight]** angezeigt.

1. Akzeptieren Sie die **[!UICONTROL Visibility]** Standardeinstellung von `Catalog, Search`.

1. Um das Produkt in der Liste der [neuen Produkte](../content-design/widget-new-products-list.md) zu verwenden, aktivieren Sie das Kontrollkästchen **[!UICONTROL Set Product as New]** .

1. Um dem Produkt Kategorien zuzuweisen, klicken Sie auf das **[!UICONTROL Select…]** und führen Sie einen der folgenden Schritte aus:

   **Vorhandene Kategorie auswählen:**

   - Beginnen Sie mit der Eingabe in das Feld, um eine Übereinstimmung zu finden.

   - Aktivieren Sie das Kontrollkästchen jeder zuzuweisenden Kategorie.

   ![Wählen Sie eine oder mehrere Kategorien für das Produktpaket aus](./assets/product-create-categories.png){width="600" zoomable="yes"}

   **Erstellen Sie eine neue Kategorie:**

   - Klicken Sie auf **[!UICONTROL New Category]**.

   - Geben Sie die **[!UICONTROL Category Name]** ein und wählen Sie die **[!UICONTROL Parent Category]** aus, um ihre Position in der Menüstruktur zu bestimmen.

   - Klicken Sie auf **[!UICONTROL Create Category]**.

1. Wählen Sie die **[!UICONTROL Country of Manufacture]** aus.

   Je nach eingestelltem Attribut können zusätzliche Attribute angezeigt werden. Sie können sie später abschließen.

### Schritt 5: Speichern und fortfahren

Jetzt ist ein guter Zeitpunkt, um deine Arbeit zu retten. Klicken Sie oben rechts auf **[!UICONTROL Save]** . In der nächsten Phase richten Sie die Konfigurationen für jede Variante ein.

## Phase 2: Hinzufügen von Produktvarianten

Die folgenden Schritte zeigen, wie Sie Konfigurationen für mehrere Varianten hinzufügen. Die Fortschrittsleiste am oberen Seitenrand zeigt Ihre aktuelle Position im Prozess an.

**Beispiel:** Für ein Hemd mit 3 Farben und 3 Größen erstellen Sie 9 einfache Produkte mit eindeutigen SKUs (eine für jede Kombination). Standardmäßig basieren der Produktname und die SKU für jede Variante auf dem Attributwert und dem übergeordneten Produktnamen oder der SKU.

### Schritt 6: Variantenattribute auswählen

1. Scrollen Sie nach unten zum Abschnitt _[!UICONTROL Configurations]_und klicken Sie auf **[!UICONTROL Create Configurations]**.

   ![Konfigurationen](./assets/product-configurable-create-configurations.png){width="600" zoomable="yes"}

1. Aktivieren Sie das Kontrollkästchen jedes Attributs, das als Variante einbezogen werden soll.

   In diesem Beispiel sind `color` und `size` ausgewählt.

   ![Attribute auswählen](./assets/product-create-configurable-step1.png){width="600" zoomable="yes"}

   Die Liste enthält alle Attribute aus dem Attributsatz , die in einem konfigurierbaren Produkt verwendet werden können.

1. Wenn Sie ein Attribut hinzufügen müssen, klicken Sie auf **[!UICONTROL Create New Attribute]** und führen Sie folgende Schritte aus:

   - Vervollständigen Sie die Attributeigenschaften.

   - Klicken Sie auf **[!UICONTROL Save Attribute]**.

   - Aktivieren Sie das Kontrollkästchen für das Attribut .

1. Klicken Sie oben rechts auf **[!UICONTROL Next]** .

### Schritt 7: Attributwerte auswählen

1. Aktivieren Sie für jedes Attribut das Kontrollkästchen der Werte, die für das Produkt gelten.

   ![Attributwerte](./assets/product-create-configurable-step2.png){width="600" zoomable="yes"}

1. Um die Attribute neu anzuordnen, greifen Sie das Symbol _Neu anordnen_ ( ![Sortierreihenfolgesymbol](../assets/icon-sort-order.png) ) und verschieben Sie den Abschnitt an eine neue Position.

   Die Reihenfolge bestimmt die Position der Dropdown-Listen auf der Produktseite.

1. Klicken Sie in der Fortschrittsleiste auf **[!UICONTROL Next]**.

### Schritt 8: Konfigurieren von Bildern, Preisen und Inventar

In diesem Schritt werden die Bilder, die Preise und die Menge für jede Konfiguration festgelegt. Die verfügbaren Optionen sind für jedes identisch. Sie können dieselbe Einstellung auf alle SKUs anwenden, eindeutige Einstellungen auf jede SKU anwenden oder die Einstellungen für vorerst überspringen.

#### Konfigurieren von Bildern

Wählen Sie die entsprechende Konfigurationsoption aus:

**Option 1: Wenden Sie einen einzelnen Bildsatz auf alle SKUs an**

1. Wählen Sie **[!UICONTROL Apply single set of images to all SKUs]** aus.

1. Navigieren Sie zu den einzelnen Bildern, die in die Produktgalerie aufgenommen werden sollen, oder ziehen Sie Bilder in das Feld.

![Verwenden Sie dieselben Bilder für alle SKUs](./assets/product-configurations-images-apply-single-set.png){width="600" zoomable="yes"}

**Option 2: Anwenden eindeutiger Bilder für jede SKU**

Da das übergeordnete Produktbild bereits hochgeladen wurde, verwenden Sie diese Option, um für jede Variante Bilder hochzuladen. Sie können verschiedene Bilder hinzufügen, die im Warenkorb angezeigt werden, wenn jemand eine bestimmte Variante kauft.

1. Wählen Sie **[!UICONTROL Apply unique images by attribute to each SKU]** aus.

1. Wählen Sie die **[!UICONTROL Attribute]** aus, die die Bilder veranschaulichen, z. B. `color`.

1. Navigieren Sie für jeden Attributwert zu den Bildern, die für diese Konfiguration verwendet werden sollen, oder ziehen Sie sie in das Feld.

   Wenn Sie ein Bild in ein Wertefeld ziehen, wird es auch in den Abschnitten für andere Werte angezeigt. Um ein Bild zu löschen, klicken Sie auf das Symbol _Papierkorb_ (![Papierkorb](../assets/icon-delete-trashcan-solid.png)).

   ![Eindeutige Bilder pro SKU](./assets/product-configurable-create-configurations-add-images-unique.png){width="600" zoomable="yes"}

#### Preise konfigurieren

>[!NOTE]
>
>Ein konfigurierbares Produkt hat keinen eigenen Preis im Katalog. Der konfigurierbare Produktpreis wird aus den [!UICONTROL In Stock] untergeordneten Produkten abgeleitet.

Wählen Sie die entsprechende Konfigurationsoption aus:

**Option 1: Wenden Sie für alle SKUs denselben Preis an**

1. Wenn der Preis für alle Varianten gleich ist, wählen Sie **[!UICONTROL Apply single price to all SKUs]** aus.

1. Geben Sie die **[!UICONTROL Price]** ein.

   ![Gleicher Preis pro SKU](./assets/product-configurable-create-configurations-price-all-skus.png){width="600" zoomable="yes"}

**Option 2: Wenden Sie für jede SKU einen anderen Preis an**

1. Wenn der Preis für jede oder einige Varianten unterschiedlich ist, wählen Sie **[!UICONTROL Apply unique prices by attribute to each SKU]** aus.

1. Wählen Sie die **[!UICONTROL Attribute]** aus, die der Preisdifferenz zugrunde liegt.

1. Geben Sie die **[!UICONTROL Price]** für jeden Attributwert ein.

   In diesem Beispiel kostet die XL-Größe mehr.

   ![Eindeutiger Preis pro SKU](./assets/product-configurable-create-configurations-price-unique.png){width="600" zoomable="yes"}

#### Konfigurieren des Inventars

Wählen Sie die entsprechende Konfigurationsoption aus:

**Option 1: Gleiche Menge auf alle SKUs anwenden**

Wenn die Menge für alle SKUs gleich ist, wählen Sie **[!UICONTROL Apply single quantity to each SKU]** aus und geben Sie die Menge an.

_Einzelne Source-Händler :_

Geben Sie die **[!UICONTROL Quantity]** ein.

_Händler mit mehreren Sources, die [Inventory management verwenden ](../inventory-management/introduction.md):_

Quellen zuweisen und Mengen für alle generierten Produktvarianten hinzufügen:

1. Wählen Sie die Option **[!UICONTROL Apply single quantity to each SKU]** aus.

1. Um eine Quelle hinzuzufügen, klicken Sie auf **[!UICONTROL Assign Sources]**.

1. Suchen Sie nach einer hinzuzufügenden Quelle. Aktivieren Sie das Kontrollkästchen neben den Quellen für das Produkt.

1. Geben Sie einen Lagerbestand pro Quelle ein.

   ![Einzelmenge für alle SKUs, Quelle zuweisen](./assets/inventory-configure-product-quantity.png){width="600" zoomable="yes"}

**Option 2: Unterschiedliche Menge nach Attribut anwenden**

_Einzelne Source-Händler :_

Geben Sie die **[!UICONTROL Quantity]** für jeden Attributwert ein.

_Händler mit mehreren Sources, die [Inventory management verwenden ](../inventory-management/introduction.md):_

Quellen zuweisen und Mengen für alle generierten Produktvarianten hinzufügen:

1. Wählen Sie **[!UICONTROL Apply unique quantity by attribute to each SKU]** aus.

1. Geben Sie die **[!UICONTROL Quantity]** für jede Variante ein.

   ![Unterschiedliche Mengen pro Attribut](./assets/product-configurations-quantity-different.png){width="600" zoomable="yes"}

Wenn die Konfiguration der Bilder, des Preises und der Menge abgeschlossen ist, klicken Sie oben rechts auf **[!UICONTROL Next]**.

### Schritt 9: Generieren von Produktkonfigurationen

Warten Sie einen Moment, bis die Liste der Produkte angezeigt wird, und führen Sie einen der folgenden Schritte aus:

- Wenn Sie mit den Konfigurationen zufrieden sind, klicken Sie auf **[!UICONTROL Generate Products]**.

- Um Korrekturen vorzunehmen, klicken Sie auf **[!UICONTROL Back]**.

![Vor dem Generieren von Produktvarianten Zusammenfassung überprüfen](./assets/product-create-configurable-summary.png){width="600" zoomable="yes"}

Die aktuellen Produktvarianten werden unten im Abschnitt _Konfiguration_ angezeigt.

![Aktuelle Konfigurationen](./assets/product-create-configurable-generated.png){width="600" zoomable="yes"}

### Schritt 10: Hinzufügen von Produktbildern

1. Scrollen Sie nach unten und erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt _[!UICONTROL Images and Videos]_.

1. Klicken Sie auf _Kamera_ und navigieren Sie zum Hauptbild für das konfigurierbare Produkt.

Weitere Informationen finden Sie unter [Bilder und Video](product-images-and-video.md).

### Schritt 11: Vollständige Produktinformationen

Scrollen Sie nach unten und füllen Sie die Informationen in den folgenden Abschnitten nach Bedarf aus:

- [Inhalt](product-content.md)

- [Ähnliche Produkte, Upsell und Crosssell](related-products-up-sells-cross-sells.md)

- [Suchmaschinenoptimierung](product-search-engine-optimization.md)

- [Anpassbare Optionen](settings-advanced-custom-options.md)

- [Produkte in Websites](settings-basic-websites.md)

- [Design](settings-advanced-design.md)

- [Geschenkoptionen](product-gift-options.md)

## Phase 3: Produkt veröffentlichen

### Schritt 12: Produkt veröffentlichen

1. Wenn Sie bereit sind, das Produkt im Katalog zu veröffentlichen, legen Sie **[!UICONTROL Enable Product]** auf `Yes` fest.

1. Führen Sie einen der folgenden Schritte aus:

   **Methode 1: Speichern und Vorschau**

   - Klicken Sie oben rechts auf **[!UICONTROL Save]**.

   - Um das Produkt in Ihrem Geschäft anzuzeigen, wählen Sie **[!UICONTROL Customer View]** im Menü _Admin_ ( ![Menüpfeil](../assets/icon-menu-down-arrow-black.png) ).

   Der Store wird in einer neuen Browser-Registerkarte geöffnet.

   ![Kundenansicht](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   **Methode 2: Speichern und schließen**

   Wählen Sie im Menü _[!UICONTROL Save]_( ![Menüpfeil](../assets/icon-menu-down-arrow-red.png){width="25"} ) die Option **[!UICONTROL Save & Close]**aus.

## Lagerstatus konfigurieren

Der konfigurierbare Produktbestandsstatus unterscheidet sich vom einfachen Produktbestandsstatus. Für ein konfigurierbares Produkt ist der Lagerstatus Teil einer **_Mehrkriterienberechnung_**.

### Funktionsweise des Lagerstatus

Die wichtigsten Grundsätze des Verhaltens bezüglich des Bestandsstatus:

| Sie setzen den Status auf | Ergebnis | Kontrolliert von untergeordneten Produkten? |
|---|---|---|
| `Out of Stock` (manuell) | Zeigt `Out of Stock` immer in „Admin“ und „Storefront“ an | Nein - bleibt bis zur manuellen Änderung in `In Stock` bestehen |
| `In Stock` (manuell) | Status ist dynamisch basierend auf untergeordneten Produkten | Teilweise - siehe Details unten |

{style="table-layout:auto"}

### Bei Einstellung auf „Auf Lager“

Wenn Sie den konfigurierbaren Produktbestandsstatus manuell auf `In Stock` setzen, verhält er sich je nach Ihrer Lagereinrichtung anders:

**Nur mit Standardquelle/Standardbestand:**

- **Admin und Storefront:** Der Stock-Status spiegelt automatisch die Verfügbarkeit des untergeordneten Produkts wider

**Mit mindestens einer benutzerdefinierten Quelle/einem benutzerdefinierten Lager:**

- **Storefront:** Der Stock-Status spiegelt automatisch die Verfügbarkeit des untergeordneten Produkts wider
- **Admin:** bleibt bis zur manuellen Änderung `In Stock` (nicht durch untergeordnete Produkte gesteuert)

>[!NOTE]
>
>Benutzerdefinierte Lager und Quellen sind Teil der Erweiterung [Inventory management](../inventory-management/sources-stocks.md). Es wird dringend empfohlen, dieses Tool ausschließlich für die Verwaltung von Beständen und Quellen zu verwenden. Die standardmäßigen Quell- und Stock-Funktionen sind Teil des `CatalogInventory`-Moduls, das jetzt nicht mehr unterstützt wird.

### Manuelle Änderungen des Lagerstatus

Wenn Sie den Lagerstatus manuell auf `Out of Stock` setzen (über die Admin-Benutzeraktion, den Dateiimport oder den API-Aufruf), bleibt er sowohl in der Admin- als auch in der Storefront `Out of Stock`, bis Sie ihn manuell wieder in `In Stock` ändern. Er wird nicht durch den Lagerstatus des untergeordneten Produkts beeinflusst.

## Systemkonfiguration (optional)

### Anzeigen von Variantenbildern in Miniaturansichten des Warenkorbs

Wenn Sie für jede Variante unterschiedliche Bilder haben, können Sie das System so konfigurieren, dass das richtige Bild für die Miniaturansicht des Warenkorbs angezeigt wird.

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Checkout]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt _[!UICONTROL Shopping Cart]_.

1. Legen Sie **[!UICONTROL Configurable Product Image]** auf `Product Thumbnail Itself` fest.

1. Klicken Sie auf **[!UICONTROL Save Config]**.

   ![Warenkorb - konfigurierbares Produktbild](./assets/config-checkout-configurable-product.png){width="600" zoomable="yes"}

## Wichtige Aspekte

- **Variantentypen** Käufer können Optionen aus den Eingabetypen „Dropdown“, „Mehrfachauswahl“, „Visuelles Farb-/Bildmuster“ und „Textmuster“ auswählen. Jede Option ist ein separates, einfaches Produkt.

- **Inventar-Tracking** Im Gegensatz zu einfachen Produkten mit benutzerdefinierten Optionen verfolgen konfigurierbare Produkte den Inventar für jede Variante unabhängig.

- **Untergeordnete Produktarten:** Untergeordnete Produkte können einfache oder virtuelle Produkte (**benutzerdefinierten Optionen)**. Um untergeordnete Produkte als virtuelle Produkte festzulegen, wählen Sie für jedes untergeordnete Produkt die Option `Тhis item has no weight` für die **[!UICONTROL Weight]** aus.

- **Globale Zuweisung** Untergeordnete Produkte werden dem konfigurierbaren Produkt (**)** allen Websites, Stores und Store-Ansichten gleichzeitig zugewiesen und zugewiesen.

- **Preise:** Ein konfigurierbares Produkt hat im Katalog keinen eigenen Preis. Der angezeigte Preis stammt von den [!UICONTROL In Stock] untergeordneten Produkten.

- **Attribute:** Variantenattribute müssen einen globalen Gültigkeitsbereich haben und Kundinnen und Kunden müssen einen Wert auswählen. Die Attribute müssen in dem Attributsatz enthalten sein, der für das konfigurierbare Produkt verwendet wird.

- **Warenkorbminiaturen:** Die Warenkorbminiatur kann das Bild entweder aus dem konfigurierbaren Produktdatensatz oder der Produktvariante anzeigen. Siehe [Systemkonfiguration](#system-configuration-optional) oben.

- **Farbfeldverhalten:** [Farbfeldattribute](swatches.md#create-swatches-for-products) können so konfiguriert werden, dass entsprechende einfache Produktbilder nicht angezeigt werden, wenn das Farbfeld ausgewählt wird, indem **[!UICONTROL Update Product Preview Image]** auf der Seite „Attribut bearbeiten“ auf `No` gesetzt wird.

- **Verhalten der Bildgalerie:** Das Design steuert, wie sich die Bildgalerie verhält, wenn Benutzende zwischen Produktkonfigurationen wechseln. Das Standardverhalten für das Design _leer_ überschreibt die übergeordneten konfigurierbaren Produktbilder mit der ausgewählten Variante. Für das Luma-Design besteht das Standardverhalten darin, den übergeordneten konfigurierbaren Produktbildern die ausgewählten Variantenbilder voranzustellen.
