---
title: herunterladbares Produkt
description: Erfahren Sie, wie Sie ein herunterladbares Produkt erstellen, das als digitale Datei bereitgestellt werden kann.
exl-id: c3dd4c5f-adc1-4a8f-a9da-7f0dedd1ee34
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1622'
ht-degree: 0%

---

# herunterladbares Produkt

Ein herunterladbares Produkt kann alles sein, was Sie als Datei bereitstellen können, z. B. ein eBook, eine Musik, ein Video, eine Software-Anwendung oder ein Update. Sie können ein Album zum Verkauf anbieten und jedes Lied einzeln verkaufen. Sie können auch ein herunterladbares Produkt verwenden, um eine elektronische Version Ihres Produktkatalogs bereitzustellen.

Da der Download erst nach dem Kauf verfügbar ist, können Sie Beispiele wie einen Auszug aus einem Buch, einen Clip aus einer Audiodatei oder einen Trailer aus einem Video bereitstellen. Ein Beispiel kann der Kunde vor dem Kauf des Produkts ausprobieren. Die Dateien, die Sie zum Herunterladen bereitstellen, können entweder auf Ihren Server oder von einem anderen Server hochgeladen werden.

![ Herunterladbares Produkt](./assets/storefront-product-downloadable.png){width="700" zoomable="yes"}

Herunterladbare Produkte können so konfiguriert werden, dass der Kunde sich bei einem Konto anmeldet, um den Link zu erhalten, oder dass er per E-Mail gesendet und für andere freigegeben werden kann. Der Status der Bestellung, bevor der Download verfügbar wird, Standardwerte und andere Bereitstellungsoptionen werden in der Konfiguration festgelegt. Beachten Sie beim Planen der herunterladbaren Katalogadditionen Folgendes:

- Herunterladbare Produkte können auf den Server hochgeladen oder von einem anderen Server im Internet mit verlinkt werden.

- Sie können bestimmen, wie oft ein Kunde ein Produkt herunterladen kann.

- Kunden, die ein herunterladbares Produkt erwerben, müssen sich vor dem Checkout anmelden.

- Der Versand eines herunterladbaren Produkts kann erfolgen, wenn die Bestellung entweder den Status `Pending` oder `Invoiced` aufweist.

- Da herunterladbare Produkte nicht ausgeliefert werden, wird der Schritt _Versand_ des Checkouts übersprungen, wenn der Warenkorb nur das herunterladbare Produkt enthält.


## Download-Optionen konfigurieren

Die herunterladbaren Konfigurationseinstellungen bestimmen die Standardwerte und Bereitstellungsoptionen für herunterladbare Produkte und geben an, ob Gäste Downloads erwerben können.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bedienfeld den Wert **[!UICONTROL Catalog]** und wählen Sie unter &quot;**[!UICONTROL Catalog]**&quot;.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt _[!UICONTROL Downloadable Product Options]_.

   ![Herunterladbare Produktoptionen](../configuration-reference/catalog/assets/catalog-downloadable-product-options.png){width="700" zoomable="yes"}

   Eine detaillierte Liste dieser Konfigurationsoptionen finden Sie unter [_Download-Produktoptionen_](../configuration-reference/catalog/catalog.md#downloadable-product-options) in der _Konfigurationsreferenz_.

1. Um den Status des Bestellprozesses zu bestimmen, wenn der Download verfügbar wird, setzen Sie **[!UICONTROL Order Item Status to Enable Downloads]** auf einen der folgenden Werte:

   - `Pending`
   - `Invoiced`

1. Geben Sie die Zahl für **[!UICONTROL Default Maximum Number of Downloads]** ein, um die Anzahl der Downloads, die ein einzelner Kunde ausführen kann, standardmäßig zu begrenzen.

1. Setzen Sie **[!UICONTROL Shareable]** auf einen der folgenden Werte:

   - `Yes` - Ermöglicht es Kunden, den Downloadlink per E-Mail an andere weiterzuleiten.
   - `No` - Verhindert, dass Kunden den Downloadlink für andere freigeben, indem sie Kunden auffordern, sich bei ihren Konten anzumelden, um auf Download-Links zugreifen zu können.

1. Geben Sie für &quot;**[!UICONTROL Default Sample Title]**&quot;die Überschrift ein, die über der Auswahl der Beispiele angezeigt werden soll.

   ![Beispieltitel](./assets/product-downloadable-config-sample-title.png){width="400"}

1. Geben Sie für &quot;**[!UICONTROL Default Link Title]**&quot;den Standardtext ein, den Sie für Downloadlinks verwenden möchten.

1. Wenn der Downloadlink in einem neuen Browserfenster geöffnet werden soll, setzen Sie **[!UICONTROL Opens Links in New Window]** auf `Yes`.

   Mit dieser Einstellung wird das Browser-Fenster für Ihren Store geöffnet gehalten.

1. Um zu bestimmen, wie herunterladbare Inhalte bereitgestellt werden, setzen Sie **[!UICONTROL Use Content Disposition]** auf einen der folgenden Werte:

   - `Attachment` - Stellt den Download-Link per E-Mail als Anlage bereit.
   - `Inline` - Stellt den Download-Link als Link auf einer Webseite bereit.

1. Wenn Sie verlangen möchten, dass sich Käufer für ein Kundenkonto registrieren und sich vor dem Kauf eines Downloads anmelden, setzen Sie **[!UICONTROL Disable Guest Checkout if Cart Contains Downloadable Items]** auf `Yes`.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

## Erstellen eines herunterladbaren Produkts

Die folgenden Anweisungen zeigen den Prozess der Erstellung eines herunterladbaren Produkts mit einer [Produktvorlage](attribute-sets.md), erforderlichen Feldern und grundlegenden Einstellungen. Jedes erforderliche Feld ist mit einem roten Sternchen (`*`) gekennzeichnet. Wenn Sie die Grundlagen abgeschlossen haben, können Sie die anderen Produkteinstellungen nach Bedarf abschließen.

>[!NOTE]
>
>Herunterladbare Dateinamen können Buchstaben und Zahlen enthalten. Entweder ein Bindestrich oder ein Unterstrich kann verwendet werden, um einen Abstand zwischen Wörtern darzustellen. Ungültige Zeichen im Dateinamen werden durch einen Unterstrich ersetzt.

### Schritt 1: Produkttyp auswählen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Wählen Sie im Menü _[!UICONTROL Add Product]_( ![Menüpfeil](../assets/icon-menu-down-arrow-red.png){width="25"} ) oben rechts `Downloadable Product` aus.

   ![Herunterladbares Produkt hinzufügen](./assets/product-add-downloadable.png){width="700" zoomable="yes"}

### Schritt 2: Attributsatz auswählen

Die Beispieldaten enthalten einen [Attributsatz](attribute-sets.md) namens _herunterladbar_ mit speziellen Feldern für herunterladbare Produkte. Sie können eine vorhandene Vorlage verwenden oder eine andere erstellen, bevor das Produkt gespeichert wird.

Führen Sie einen der folgenden Schritte aus, um den Attributsatz auszuwählen, der als Vorlage für das Produkt verwendet wird:

- Geben Sie für &quot;**[!UICONTROL Search]**&quot;den Namen des Attributsatzes ein.

- Wählen Sie in der Liste den Attributsatz `Downloadable` aus.

Das Formular wird entsprechend der Änderung aktualisiert.

![Attributsatz auswählen](./assets/product-create-choose-attribute-set-downloadable.png){width="600" zoomable="yes"}

### Schritt 3: Ausführen der erforderlichen Einstellungen

1. Geben Sie den Wert **[!UICONTROL Product Name]** ein.

1. Nehmen Sie die standardmäßige **[!UICONTROL SKU]** an, die auf dem Produktnamen basiert, oder geben Sie einen anderen ein.

1. Geben Sie das Produkt **[!UICONTROL Price]** ein.

1. Da das Produkt noch nicht zur Veröffentlichung bereit ist, setzen Sie **[!UICONTROL Enable Product]** auf `No`.

1. Klicken Sie auf **[!UICONTROL Save]** und fahren Sie fort.

   Wenn das Produkt gespeichert wird, wird die Auswahl für die [Store-Ansicht](introduction.md#product-scope) in der oberen linken Ecke angezeigt.

1. Wählen Sie die **[!UICONTROL Store View]** aus, in der das Produkt verfügbar sein soll.

   ![Speicheransicht auswählen](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

### Schritt 4: Grundlegende Einstellungen durchführen

1. Setzen Sie **[!UICONTROL Tax Class]** auf einen der folgenden Werte:

   - `None`
   - `Taxable Goods`

1. Geben Sie den Wert **[!UICONTROL Quantity]** des vorrätigen Produkts ein.

   Beachten Sie Folgendes:

   - Standardmäßig ist **[!UICONTROL Stock Status]** auf `Out of Stock` gesetzt.

   - Da herunterladbare Produkte nicht ausgeliefert werden, wird das Feld **[!UICONTROL Weight]** nicht verwendet. Wenn Sie diese Funktion aktivieren, wird sie zu einem [einfachen Produkt](product-create-simple.md) und _Ist dieses herunterladbare Produkt?Der Tab_ kann nicht verwendet werden.

   >[!NOTE]
   >
   >Wenn Sie [Inventory management](../inventory-management/introduction.md) aktivieren, legen Einzelhändler der Source die Menge in diesem Abschnitt fest. Mehrere Source-Händler fügen im Bereich Quellen Quellen und Mengen hinzu. Siehe folgenden Abschnitt _Quellen und Mengen zuweisen (Inventory management)_ .

1. Nehmen Sie die standardmäßige **[!UICONTROL Visibility]** -Einstellung von `Catalog, Search` an.

1. Um das Produkt in der Liste [ der neuen Produkte](../content-design/widget-new-products-list.md) zu kennzeichnen, aktivieren Sie das Kontrollkästchen **[!UICONTROL Set Product as New]** .

1. Um dem Produkt _[!UICONTROL Categories]_zuzuweisen, klicken Sie auf das Feld **[!UICONTROL Select…]**und führen Sie einen der folgenden Schritte aus:

   **Wählen Sie eine vorhandene Kategorie**:

   - Beginnen Sie mit der Eingabe in das Feld, bis Sie eine Übereinstimmung finden.

   - Aktivieren Sie das Kontrollkästchen der jeweiligen Kategorie, die zugewiesen werden soll.

   **Erstellen einer Kategorie**:

   - Klicken Sie auf **[!UICONTROL New Category]**.

   - Geben Sie den Wert **[!UICONTROL Category Name]** ein und wählen Sie den Wert **[!UICONTROL Parent Category]** aus, der seine Position in der [Menüstruktur](category-root.md) bestimmt.

   - Klicken Sie auf **[!UICONTROL Create Category]**.

1. Setzen Sie **[!UICONTROL Format]** auf einen der folgenden Werte:

   - `Download`
   - `DVD`

   Bei Bedarf können Sie das [Attribut](attribute-product-create.md) bearbeiten, um weitere Werte hinzuzufügen.

   Es kann zusätzliche Attribute geben, die das Produkt beschreiben. Die Auswahl variiert je nach Attributsatz und kann zu einem späteren Zeitpunkt abgeschlossen werden.

#### Quellen und Mengen zuweisen ([!DNL Inventory Management])

{{$include /help/_includes/inventory-assign-sources.md}}

### Schritt 5: Herunterladbare Informationen ausfüllen

Scrollen Sie nach unten, erweitern Sie den Abschnitt _[!UICONTROL Downloadable Information]_um ![Erweiterungsauswahl](../assets/icon-display-expand.png) und aktivieren Sie das Kontrollkästchen **[!UICONTROL Is this downloadable product?]**.

Wenn diese Option aktiviert ist, besteht der Abschnitt &quot;_[!UICONTROL Downloadable Information]_&quot; aus zwei Teilen. Der erste Teil beschreibt jeden Downloadlink und der zweite Teil jede Beispieldatei. Der Standardwert für viele dieser Optionen kann in der [Konfiguration](#configure-the-download-options) festgelegt werden.

![Herunterladbare Informationen](./assets/product-downloadable-information.png){width="600" zoomable="yes"}

#### Links ausfüllen

1. Geben Sie im Abschnitt &quot;_[!UICONTROL Links]_&quot;den **[!UICONTROL Title]**ein, den Sie als Überschrift für die Downloadlinks verwenden möchten.

1. Aktivieren Sie gegebenenfalls das Kontrollkästchen **[!UICONTROL Links can be purchased separately]** .

1. Klicken Sie auf **[!UICONTROL Add Link]** und führen Sie die folgenden Schritte aus:

   - Geben Sie die Werte **[!UICONTROL Title]** und **[!UICONTROL Price]** des Downloads ein.

   - Wählen Sie für sowohl **[!UICONTROL File]**- als auch **[!UICONTROL Sample]**-Dateien eine der folgenden Verteilungsmethoden für die Downloads:

      - `Upload File` - Wählen Sie diese Methode, um die Verteilungsdatei auf den Server hochzuladen. Navigieren Sie zur Datei und wählen Sie sie zum Hochladen aus.
      - `URL` - Wählen Sie diese Methode, um über eine URL auf die Verteilungsdatei zuzugreifen. Geben Sie die vollständige URL zur Download-Datei ein.

   >[!NOTE]
   >
   >Links zu externen Ressourcen können nicht als herunterladbare Produkte verwendet werden. Gültige Link-Domänen sind in der Datei `env.php` programmgesteuert vordefiniert (siehe [env.php-Referenz](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/files/config-reference-envphp.html) im _Konfigurationshandbuch_).

   - Setzen Sie **[!UICONTROL Shareable]** auf einen der folgenden Werte:

      - `No` - Erfordert von Kunden, sich bei ihren Konten anzumelden, um auf den Downloadlink zuzugreifen.

      - `Yes` - Sendet den Link per E-Mail, den Kunden für andere freigeben können.

      - `Use Config` - Verwendet die Methode, die in der Konfiguration [herunterladbare Produktoptionen](../configuration-reference/catalog/catalog.md) angegeben ist.

   - Führen Sie einen der folgenden Schritte aus:

      - Um Downloads pro Kunde zu begrenzen, geben Sie die maximale Anzahl für **[!UICONTROL Max. Downloads]** ein.
      - Um unbegrenzte Downloads zu ermöglichen, aktivieren Sie das Kontrollkästchen **[!UICONTROL Unlimited]** .

   ![Link-Detail](./assets/product-downloadable-link-detail.png){width="600" zoomable="yes"}

1. Um einen weiteren Link hinzuzufügen, klicken Sie auf **[!UICONTROL Add Link]** und wiederholen Sie diese Schritte.

#### Füllen Sie die Beispiele aus

1. Geben Sie im Abschnitt _[!UICONTROL Samples]_den **[!UICONTROL Title]**ein, den Sie als Überschrift für die Beispiele verwenden möchten.

1. Um die Informationen für jedes Beispiel auszufüllen, klicken Sie auf **[!UICONTROL Add Link]**.

   ![Beispiele](./assets/product-downloadable-samples.png){width="600" zoomable="yes"}

1. Füllen Sie die Link-Details wie folgt aus:

   - Geben Sie den Wert **[!UICONTROL Title]** des einzelnen Musters ein.

   - Wählen Sie eine der folgenden Verteilungsmethoden:

      - `Upload File` - Wählen Sie diese Methode, um die Verteilungsdatei auf den Server hochzuladen. Navigieren Sie zur Datei und wählen Sie sie zum Hochladen aus.
      - `URL` - Wählen Sie diese Methode, um über eine URL auf die Verteilungsdatei zuzugreifen. Geben Sie die vollständige URL zur Download-Datei ein.

   - Um ein weiteres Beispiel hinzuzufügen, klicken Sie auf **[!UICONTROL Add Link]** und wiederholen Sie diese Schritte.

   - Um die Reihenfolge der Beispiele zu ändern, ziehen Sie das Symbol _Reihenfolge ändern_ ( ![Controller positionieren](../assets/icon-sort-order.png) ) und ziehen Sie das Beispiel an eine neue Position.

### Schritt 6: Produktinformationen ausfüllen

Scrollen Sie nach unten und füllen Sie die Informationen in den folgenden Abschnitten nach Bedarf aus:

- [Inhalt](product-content.md)
- [Bilder und Videos](product-images-and-video.md)
- [Suchmaschinenoptimierung](product-search-engine-optimization.md)
- [Zugehörige Produkte, Up-Sells und Cross-Sells](related-products-up-sells-cross-sells.md)
- [Anpassbare Optionen](settings-advanced-custom-options.md)
- [Produkte in Websites](settings-basic-websites.md)
- [Design](settings-advanced-design.md)
- [Geschenkoptionen](product-gift-options.md)

### Schritt 7: Publish des Produkts

Wenn Sie bereit sind, das Produkt im Katalog zu veröffentlichen, setzen Sie **[!UICONTROL Enable Product]** auf `Yes` und führen Sie einen der folgenden Schritte aus:

**Methode 1:** Speichern und Vorschau anzeigen

- Klicken Sie in der oberen rechten Ecke auf **[!UICONTROL Save]**.

- Um das Produkt in Ihrem Store anzuzeigen, wählen Sie im Menü _Admin_ ( ![Menüpfeil](../assets/icon-menu-down-arrow-black.png) ) die Option **[!UICONTROL Customer View]** aus.

  Der Store wird in einer neuen Browser-Registerkarte geöffnet.

  ![Kundenansicht](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

**Methode 2:** Speichern und schließen

Wählen Sie im Menü _[!UICONTROL Save]_( ![Menüpfeil](../assets/icon-menu-down-arrow-red.png){width="25"} ) die Option **[!UICONTROL Save & Close]**.

## Storefront-Erlebnis

Im Dashboard des Kundenkontos verlinkt die Seite &quot;_[!UICONTROL My Downloadable Products]_&quot; zu jeder Bestellung herunterladbarer Produkte. Die Downloads sind über das Kundenkonto verfügbar, sobald die Bestellung abgeschlossen ist.

![Meine herunterladbaren Produkte](./assets/customer-account-my-downloadable-products.png){width="700" zoomable="yes"}

In der folgenden Tabelle werden die Werte für _Meine herunterladbaren Produkte_ beschrieben:

| Spalte | Beschreibung |
|--- |--- |
| [!UICONTROL Order#] | Die [Bestellung](../stores-purchase/orders.md), in der das herunterladbare Produkt gekauft wurde. Stellt einen Link zu den Bestelldetails bereit. |
| [!UICONTROL Date] | Erstellungsdatum der Bestellung. |
| [!UICONTROL Title] | Der Name des herunterladbaren Produkts, das mit der Bestellung gekauft wurde. Stellt einen Link zum herunterladbaren Produkt bereit. |
| [!UICONTROL Status] | Auftragsverarbeitungsstatus. |
| [!UICONTROL Remaining Downloads] | Anzahl der verfügbaren Downloads des heruntergeladenen Produkts. |

_**So laden Sie eine Produktdatei vom Konto-Dashboard herunter**_

1. Der Kunde wählt in seinem Konto-Dashboard **[!UICONTROL My Downloadable Products]** aus.

1. Sucht die Reihenfolge in der Liste und klickt auf den Link nach dem Titel.

1. Klicken Sie in der rechten unteren Ecke des Download-Fensters auf das Symbol _Download_ .

1. Platziert die Datei am Speicherort des Downloads und speichert sie am gewünschten Speicherort.
