---
title: Herunterladbares Produkt
description: Erfahren Sie, wie Sie ein herunterladbares Produkt erstellen, das als digitale Datei bereitgestellt werden kann.
exl-id: c3dd4c5f-adc1-4a8f-a9da-7f0dedd1ee34
feature: Catalog Management, Products
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '1622'
ht-degree: 0%

---

# Herunterladbares Produkt

Bei einem herunterladbaren Produkt kann es sich um alles handeln, was Sie als Datei bereitstellen können, z. B. ein E-Book, Musik, Video, eine Software-Anwendung oder ein Update. Sie können ein Album zum Verkauf anbieten und jedes Lied einzeln verkaufen. Sie können auch ein herunterladbares Produkt verwenden, um eine elektronische Version Ihres Produktkatalogs bereitzustellen.

Da der Download erst nach dem Kauf verfügbar ist, können Sie Beispiele wie einen Auszug aus einem Buch, einen Clip aus einer Audiodatei oder einen Trailer aus einem Video bereitstellen. Ein Beispiel ist etwas, das der Kunde vor dem Kauf des Produkts ausprobieren kann. Die Dateien, die Sie zum Download bereitstellen, können entweder auf Ihren Server oder von einem anderen Server hochgeladen werden.

![Herunterladbares Produkt](./assets/storefront-product-downloadable.png){width="700" zoomable="yes"}

Herunterladbare Produkte können so konfiguriert werden, dass der Kunde sich bei einem Konto anmelden muss, um den Link zu erhalten, oder per E-Mail gesendet und für andere freigegeben werden kann. Der Status der Bestellung, bevor der Download verfügbar wird, Standardwerte und andere Lieferoptionen werden in der Konfiguration festgelegt. Beachten Sie bei der Planung von Katalogergänzungen zum Herunterladen Folgendes:

- Herunterladbare Produkte können von einem anderen Server im Internet auf den Server hochgeladen oder mit ihm verknüpft werden.

- Sie können bestimmen, wie oft eine Kundin oder ein Kunde ein Produkt herunterladen kann.

- Kunden, die ein herunterladbares Produkt erwerben, können vor dem Checkout aufgefordert werden, sich anzumelden.

- Die Lieferung eines herunterladbaren Produkts kann erfolgen, wenn sich die Bestellung entweder im Status `Pending` oder `Invoiced` befindet.

- Da herunterladbare Produkte nicht versendet werden, wird der _Versand_-Schritt der Kasse übersprungen, wenn der Warenkorb nur das herunterladbare Produkt enthält.


## Download-Optionen konfigurieren

Die Konfigurationseinstellungen für den Download bestimmen die Standardwerte und Lieferoptionen für herunterladbare Produkte und geben an, ob Gäste Downloads erwerben können.

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Catalog]** und wählen Sie darunter **[!UICONTROL Catalog]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt _[!UICONTROL Downloadable Product Options]_.

   ![Download-Produktoptionen](../configuration-reference/catalog/assets/catalog-downloadable-product-options.png){width="700" zoomable="yes"}

   Eine detaillierte Liste dieser Konfigurationsoptionen finden Sie unter [_Herunterladbare Produktoptionen_](../configuration-reference/catalog/catalog.md#downloadable-product-options) in der _Konfigurationsreferenz_.

1. Um den Status des Bestellvorgangs zu ermitteln, wenn der Download verfügbar wird, legen Sie **[!UICONTROL Order Item Status to Enable Downloads]** auf eine der folgenden Einstellungen fest:

   - `Pending`
   - `Invoiced`

1. Um ein Standardlimit für die Anzahl der Downloads festzulegen, die ein einzelner Kunde durchführen kann, geben Sie die Zahl für **[!UICONTROL Default Maximum Number of Downloads]** ein.

1. Legen Sie **[!UICONTROL Shareable]** auf eine der folgenden Einstellungen fest:

   - `Yes` - Ermöglicht es Kunden, den Download-Link per E-Mail an andere zu senden.
   - `No` - Verhindert, dass Kunden den Download-Link für andere freigeben, indem sie von Kunden verlangen, sich bei ihren Konten anzumelden, um auf Download-Links zuzugreifen.

1. Geben Sie **[!UICONTROL Default Sample Title]** die Überschrift ein, die über der Auswahl der Beispiele angezeigt werden soll.

   ![Beispieltitel](./assets/product-downloadable-config-sample-title.png){width="400"}

1. Geben Sie **[!UICONTROL Default Link Title]** den Standardtext ein, den Sie für Download-Links verwenden möchten.

1. Wenn der Download-Link in einem neuen Browser-Fenster geöffnet werden soll, setzen Sie **[!UICONTROL Opens Links in New Window]** auf `Yes`.

   Diese Einstellung wird verwendet, um das Browser-Fenster Ihres Shops offen zu halten.

1. Legen Sie **[!UICONTROL Use Content Disposition]** auf eine der folgenden Einstellungen fest, um zu bestimmen, wie herunterladbare Inhalte bereitgestellt werden:

   - `Attachment` - Stellt den Download-Link per E-Mail als Anhang bereit.
   - `Inline` - Stellt den Download-Link als Link auf einer Web-Seite bereit.

1. Wenn Sie möchten, dass sich Käufer für ein Kundenkonto registrieren und sich anmelden müssen, bevor sie einen Download erwerben, setzen Sie **[!UICONTROL Disable Guest Checkout if Cart Contains Downloadable Items]** auf `Yes`.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

## Herunterladbares Produkt erstellen

Die folgenden Anweisungen zeigen den Prozess der Erstellung eines herunterladbaren Produkts mithilfe einer [Produktvorlage](attribute-sets.md), erforderlichen Feldern und Grundeinstellungen. Jedes erforderliche Feld ist mit einem roten Sternchen (`*`) gekennzeichnet. Wenn Sie die Grundlagen fertig gestellt haben, können Sie die anderen Produkteinstellungen nach Bedarf abschließen.

>[!NOTE]
>
>Herunterladbare Dateinamen können Buchstaben und Zahlen enthalten. Zur Darstellung von Leerzeichen zwischen Wörtern kann entweder ein Strich oder ein Unterstrich verwendet werden. Alle ungültigen Zeichen im Dateinamen werden durch einen Unterstrich ersetzt.

### Schritt 1: Produkttyp auswählen

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Wählen Sie im Menü _[!UICONTROL Add Product]_![Menüpfeil](../assets/icon-menu-down-arrow-red.png){width="25"} oben rechts `Downloadable Product` aus.

   ![Herunterladbares Produkt hinzufügen](./assets/product-add-downloadable.png){width="700" zoomable="yes"}

### Schritt 2: Attributsatz auswählen

Die Beispieldaten enthalten einen [Attributsatz](attribute-sets.md) namens _Downloadable_ mit speziellen Feldern für herunterladbare Produkte. Sie können eine vorhandene Vorlage verwenden oder eine andere erstellen, bevor das Produkt gespeichert wird.

Um den Attributsatz auszuwählen, der als Vorlage für das Produkt verwendet wird, führen Sie einen der folgenden Schritte aus:

- Geben Sie **[!UICONTROL Search]** den Namen des Attributsatzes an.

- Wählen Sie in der Liste den `Downloadable` Attributsatz aus.

Das Formular wird mit der Änderung aktualisiert.

![Attributsatz auswählen](./assets/product-create-choose-attribute-set-downloadable.png){width="600" zoomable="yes"}

### Schritt 3: Erforderliche Einstellungen vornehmen

1. Geben Sie die **[!UICONTROL Product Name]** ein.

1. Akzeptieren Sie die **[!UICONTROL SKU]**, die auf dem Produktnamen basiert, oder geben Sie einen anderen ein.

1. Geben Sie die **[!UICONTROL Price]** ein.

1. Da das Produkt noch nicht zur Veröffentlichung bereit ist, setzen Sie **[!UICONTROL Enable Product]** auf `No`.

1. Klicken Sie auf **[!UICONTROL Save]** und fahren Sie fort.

   Wenn das Produkt gespeichert wird, wird [ Auswahl „Store](introduction.md#product-scope)Ansicht“ in der oberen linken Ecke angezeigt.

1. Wählen Sie die **[!UICONTROL Store View]** aus, in der das Produkt verfügbar sein soll.

   ![Store-Ansicht auswählen](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

### Schritt 4: Vervollständigen Sie die Grundeinstellungen

1. Legen Sie **[!UICONTROL Tax Class]** auf eine der folgenden Einstellungen fest:

   - `None`
   - `Taxable Goods`

1. Geben Sie die **[!UICONTROL Quantity]** des Produkts ein, das auf Lager ist.

   Beachten Sie Folgendes:

   - Standardmäßig ist **[!UICONTROL Stock Status]** auf `Out of Stock` festgelegt.

   - Da herunterladbare Produkte nicht versendet werden, wird das Feld **[!UICONTROL Weight]** nicht verwendet. Wenn Sie diese Funktion aktivieren, wird sie zu [Einfaches Produkt](product-create-simple.md) und der _Ist dieses herunterladbare Produkt?_ Registerkarte kann nicht verwendet werden.

   >[!NOTE]
   >
   >Wenn Sie [Inventory management](../inventory-management/introduction.md) aktivieren, legen Einzelhändler von Source die Menge in diesem Abschnitt fest. Händler, die mehrere Source verwenden, fügen im Abschnitt „Quellen“ Quellen und Mengen hinzu. Siehe folgenden Abschnitt _Zuweisen von Quellen und Mengen (Inventory management_.

1. Akzeptieren Sie die **[!UICONTROL Visibility]** Standardeinstellung von `Catalog, Search`.

1. Um das Produkt in der [Liste neuer Produkte](../content-design/widget-new-products-list.md) zu verwenden, aktivieren Sie das Kontrollkästchen **[!UICONTROL Set Product as New]** .

1. Um dem Produkt _[!UICONTROL Categories]_zuzuweisen, klicken Sie auf das **[!UICONTROL Select…]**und führen Sie einen der folgenden Schritte aus:

   **Vorhandene Kategorie auswählen**:

   - Beginnen Sie mit der Eingabe in das Feld, bis Sie eine Übereinstimmung finden.

   - Aktivieren Sie das Kontrollkästchen jeder Kategorie, die zugewiesen werden soll.

   **Erstellen einer Kategorie**:

   - Klicken Sie auf **[!UICONTROL New Category]**.

   - Geben Sie die **[!UICONTROL Category Name]** ein und wählen Sie die **[!UICONTROL Parent Category]** aus, die ihre Position in der [Menüstruktur](category-root.md) bestimmt.

   - Klicken Sie auf **[!UICONTROL Create Category]**.

1. Legen Sie **[!UICONTROL Format]** auf eine der folgenden Einstellungen fest:

   - `Download`
   - `DVD`

   Bei Bedarf können Sie das Attribut [ bearbeiten](attribute-product-create.md) um weitere Werte hinzuzufügen.

   Möglicherweise gibt es zusätzliche Attribute, die das Produkt beschreiben. Die Auswahl variiert je nach Attributsatz, und Sie können sie später abschließen.

#### Zuweisen von Quellen und Mengen ([!DNL Inventory Management])

{{$include /help/_includes/inventory-assign-sources.md}}

### Schritt 5: Vervollständigen Sie die herunterladbaren Informationen

Scrollen Sie nach unten, erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt _[!UICONTROL Downloadable Information]_und aktivieren Sie das Kontrollkästchen **[!UICONTROL Is this downloadable product?]**.

Nach der Aktivierung besteht der _[!UICONTROL Downloadable Information]_aus zwei Teilen. Der erste Teil beschreibt jeden Download-Link, und der zweite Teil beschreibt jede Beispieldatei. Der Standardwert für viele dieser Optionen kann in der [Konfiguration“ festgelegt ](#configure-the-download-options).

![Informationen zum Herunterladen](./assets/product-downloadable-information.png){width="600" zoomable="yes"}

#### Vervollständigen Sie die Links

1. Geben Sie im Abschnitt _[!UICONTROL Links]_die **[!UICONTROL Title]**ein, die Sie als Überschrift für die Download-Links verwenden möchten.

1. Aktivieren Sie bei Bedarf das Kontrollkästchen **[!UICONTROL Links can be purchased separately]** .

1. Klicken Sie auf **[!UICONTROL Add Link]** und führen Sie folgende Schritte aus:

   - Geben Sie die **[!UICONTROL Title]** und **[!UICONTROL Price]** des Downloads ein.

   - Wählen Sie sowohl für **[!UICONTROL File]**- als auch für **[!UICONTROL Sample]**-Dateien eine der folgenden Verteilungsmethoden für die Downloads:

      - `Upload File` : Wählen Sie diese Methode aus, um die Verteilungsdatei auf den Server hochzuladen. Navigieren Sie zur Datei und wählen Sie sie zum Hochladen aus.
      - `URL` : Wählen Sie diese Methode aus, um über eine URL auf die Verteilungsdatei zuzugreifen. Geben Sie die vollständige URL zum Herunterladen der Datei ein.

   >[!NOTE]
   >
   >Sie können keine Links zu externen Ressourcen als herunterladbare Produkte verwenden. Gültige Link-Domains sind programmgesteuert in der `env.php`-Datei vordefiniert (siehe [env.php](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/files/config-reference-envphp.html) im _Configuration Guide_).

   - Legen Sie **[!UICONTROL Shareable]** auf eine der folgenden Einstellungen fest:

      - `No` - Erfordert, dass sich Kunden bei ihren Konten anmelden, um auf den Download-Link zuzugreifen.

      - `Yes` - Sendet den Link per E-Mail, die Kundinnen und Kunden für andere freigeben können.

      - `Use Config` - Verwendet die Methode, die in der Konfiguration [Herunterladbare Produktoptionen](../configuration-reference/catalog/catalog.md) angegeben ist.

   - Führen Sie einen der folgenden Schritte aus:

      - Um Downloads pro Kunde zu begrenzen, geben Sie die maximale Anzahl für **[!UICONTROL Max. Downloads]** ein.
      - Um unbegrenzte Downloads zuzulassen, aktivieren Sie das Kontrollkästchen **[!UICONTROL Unlimited]** .

   ![Link-Detail](./assets/product-downloadable-link-detail.png){width="600" zoomable="yes"}

1. Um einen weiteren Link hinzuzufügen, klicken Sie auf **[!UICONTROL Add Link]** und wiederholen Sie diese Schritte.

#### Füllen Sie die Beispiele aus

1. Geben Sie im Abschnitt _[!UICONTROL Samples]_die **[!UICONTROL Title]**ein, die Sie als Überschrift für die Beispiele verwenden möchten.

1. Um die Informationen für jedes Beispiel auszufüllen, klicken Sie auf **[!UICONTROL Add Link]**.

   ![Beispiele](./assets/product-downloadable-samples.png){width="600" zoomable="yes"}

1. Vervollständigen Sie die Link-Details wie folgt:

   - Geben Sie die **[!UICONTROL Title]** der einzelnen Stichprobe ein.

   - Wählen Sie eine der folgenden Verteilungsmethoden:

      - `Upload File` : Wählen Sie diese Methode aus, um die Verteilungsdatei auf den Server hochzuladen. Navigieren Sie zur Datei und wählen Sie sie zum Hochladen aus.
      - `URL` : Wählen Sie diese Methode aus, um über eine URL auf die Verteilungsdatei zuzugreifen. Geben Sie die vollständige URL zum Herunterladen der Datei ein.

   - Um ein weiteres Beispiel hinzuzufügen, klicken Sie auf **[!UICONTROL Add Link]** und wiederholen Sie diese Schritte.

   - Um die Reihenfolge der Muster zu ändern, greifen Sie das Symbol _Reihenfolge ändern_ ( ![Positions-Controller](../assets/icon-sort-order.png) ) und ziehen Sie das Muster an eine neue Position.

### Schritt 6: Füllen Sie die Produktinformationen aus

Scrollen Sie nach unten und füllen Sie die Informationen in den folgenden Abschnitten nach Bedarf aus:

- [Inhalt](product-content.md)
- [Bilder und Videos](product-images-and-video.md)
- [Suchmaschinenoptimierung](product-search-engine-optimization.md)
- [Ähnliche Produkte, Upsell und Crosssell](related-products-up-sells-cross-sells.md)
- [Anpassbare Optionen](settings-advanced-custom-options.md)
- [Produkte in Websites](settings-basic-websites.md)
- [Design](settings-advanced-design.md)
- [Geschenkoptionen](product-gift-options.md)

### Schritt 7: Produkt veröffentlichen

Wenn Sie bereit sind, das Produkt im Katalog zu veröffentlichen, legen Sie **[!UICONTROL Enable Product]** auf `Yes` fest und führen Sie einen der folgenden Schritte aus:

**Methode 1: Speichern** Vorschau

- Klicken Sie oben rechts auf **[!UICONTROL Save]**.

- Um das Produkt in Ihrem Geschäft anzuzeigen, wählen Sie **[!UICONTROL Customer View]** im Menü _Admin_ ( ![Menüpfeil](../assets/icon-menu-down-arrow-black.png) ).

  Der Store wird in einer neuen Browser-Registerkarte geöffnet.

  ![Kundenansicht](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

**Methode 2: Speichern und schließen**

Wählen Sie im Menü _[!UICONTROL Save]_( ![Menüpfeil](../assets/icon-menu-down-arrow-red.png){width="25"} ) die Option **[!UICONTROL Save & Close]**aus.

## Storefront-Erlebnis

Im Dashboard des Kundenkontos ist die _[!UICONTROL My Downloadable Products]_mit jeder Bestellung herunterladbarer Produkte verknüpft. Die Downloads werden nach Abschluss der Bestellung über das Konto des Kunden verfügbar.

![Meine herunterladbaren Produkte](./assets/customer-account-my-downloadable-products.png){width="700" zoomable="yes"}

In der folgenden Tabelle werden die Werte _Meine herunterladbaren Produkte_ beschrieben:

| Spalte | Beschreibung |
|--- |--- |
| [!UICONTROL Order#] | Die [Bestellung](../stores-purchase/orders.md) in der das herunterladbare Produkt gekauft wurde. Enthält einen Link zu den Bestelldetails. |
| [!UICONTROL Date] | Erstellungsdatum der Bestellung. |
| [!UICONTROL Title] | Der Name des herunterladbaren Produkts, das mit der Bestellung gekauft wurde. Stellt einen Link zum herunterladbaren Produkt bereit. |
| [!UICONTROL Status] | Status der Bestellabwicklung. |
| [!UICONTROL Remaining Downloads] | Anzahl der verfügbaren Downloads des heruntergeladenen Produkts. |

_**So laden Sie eine Produktdatei vom Konto-Dashboard herunter**_

1. In ihrem Konto-Dashboard wählt der Kunde **[!UICONTROL My Downloadable Products]** aus.

1. Sucht die Reihenfolge in der Liste und klickt auf den Link nach dem Titel.

1. Klicken Sie in der rechten unteren Ecke des Download-Fensters auf das Symbol _Herunterladen_.

1. Sucht die Datei in ihrem Downloads-Speicherort und speichert die Datei am gewünschten Speicherort.

<!-- Last updated from includes: 2023-05-19 17:14:58 -->
