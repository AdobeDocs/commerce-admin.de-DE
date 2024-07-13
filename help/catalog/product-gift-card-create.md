---
title: Geschenkkartenprodukt
description: Erfahren Sie, wie Sie ein Geschenkkartenprodukt erstellen, das einen eindeutigen Code erzeugt, den ein Empfänger beim Checkout einlösen kann.
exl-id: bc4b60fe-10b3-4d17-85ce-35c2720c90a2
feature: Catalog Management, Products, Gift
source-git-commit: e72977596c4479d2e94b1e066ee166d22cb12405
workflow-type: tm+mt
source-wordcount: '962'
ht-degree: 0%

---

# Geschenkkartenprodukt

{{ee-feature}}

Jede Geschenkkarte verfügt über einen eindeutigen Code, der von nur einem Kunden während des Checkout eingelöst werden kann. Ein [Code-Pool](../stores-purchase/product-gift-card-accounts.md#step-3-establish-the-gift-card-code-pool) muss eingerichtet werden, bevor Geschenkkarten verkauft werden können. Informationen dazu, wie Geschenkkarten im Warenkorb eingelöst werden, finden Sie unter [Workflow für Geschenkkarten](../stores-purchase/product-gift-card-workflow.md) .

![Produktseite der Gift-Karte](./assets/storefront-giftcard-product-page.png){width="700" zoomable="yes"}

Es gibt drei Arten von Geschenkgutscheinprodukten:

- **Virtual** - Eine virtuelle Geschenkkarte wird an die E-Mail-Adresse des Empfängers gesendet, die während des Kaufs der Geschenkkarte erforderlich ist. Eine Lieferadresse ist nicht erforderlich.

- **Physikalisch** - Eine physische Geschenkkarte wird an die Adresse des Empfängers versandt, was während des Kaufs der Geschenkkarte erforderlich ist.

- **Kombiniert** - Eine kombinierte Geschenkkarte wird versandt und per E-Mail an den Empfänger gesendet. Die E-Mail-Adresse des Empfängers und die Lieferadresse sind während des Kaufs der Geschenkkarte erforderlich.

## Geschenkkartenprodukt erstellen

Die folgenden Anweisungen zeigen den Prozess der Erstellung einer Geschenkkarte mit einer [Produktvorlage](attribute-sets.md), erforderlichen Feldern und grundlegenden Einstellungen. Jedes erforderliche Feld ist mit einem roten Sternchen (`*`) gekennzeichnet. Wenn Sie die Grundlagen abgeschlossen haben, können Sie die anderen Produkteinstellungen nach Bedarf abschließen.

### Schritt 1: Produkttyp auswählen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. In der oberen rechten Ecke des _[!UICONTROL Add Product]_( ![Menüpfeil](../assets/icon-menu-down-arrow-red.png){width="25"})  ), wählen Sie **[!UICONTROL Gift Card]**.

   ![Geschenkkarte hinzufügen](./assets/product-add-gift-card.png){width="700" zoomable="yes"}

### Schritt 2: Attributsatz auswählen

Sie können den standardmäßigen Attributsatz `Gift Card` verwenden oder einen anderen auswählen. Führen Sie einen der folgenden Schritte aus, um den Attributsatz auszuwählen, der als Vorlage für das Produkt verwendet wird:

- Klicken Sie in das Feld **[!UICONTROL Attribute Set]** und geben Sie den gesamten oder einen Teil des Namens des Attributsatzes ein.

- Wählen Sie in der angezeigten Liste den zu verwendenden Attributsatz aus.

![Attributsatz auswählen](./assets/product-create-choose-attribute-set-gift-card.png){width="600" zoomable="yes"}

### Schritt 3: Ausführen der erforderlichen Einstellungen

1. Geben Sie eine **[!UICONTROL Product Name]** für die Geschenkkarte ein.

   Sie können auch den Typ der Geschenkkarte im Namen angeben. Beispiel: _Luma Virtual Gift Card_.

1. Geben Sie einen **[!UICONTROL SKU]** für das Produkt ein.

   Standardmäßig wird der Produktname als standardmäßige SKU verwendet.

1. Setzen Sie **[!UICONTROL Card Type]** auf einen der folgenden Werte:

   - `Virtual` - Virtuelle Geschenkkarten werden dem Empfänger per E-Mail zugestellt.
   - `Physical` - Körperliche Geschenkgutscheine können im Voraus gebündelt und mit einmaligen Codes versehen werden.
   - `Combined` - Eine kombinierte Geschenkkarte hat sowohl die Eigenschaften einer virtuellen als auch einer physischen Geschenkkarte.

   ![Geschenkkartentyp](./assets/product-create-gift-card-type.png){width="600" zoomable="yes"}

1. Um dem Kunden eine Auswahl von Festbeträgen anzubieten, klicken Sie auf **[!UICONTROL Add Amount]** und geben Sie den ersten festen Wert der Karte als Dezimalzahl ein.

   Wiederholen Sie diesen Schritt für jede Komponente, um die Festbeträge auszuwählen.

1. Gehen Sie wie folgt vor, um Kunden die Möglichkeit zu geben, den Wert der Geschenkkarte festzulegen:

   - Setzen Sie **[!UICONTROL Open Amount]** auf `Yes`.

   - Geben Sie die Werte **[!UICONTROL Open Amount From]** und **[!UICONTROL To]** ein, um den Mindest- und den Höchstwert festzulegen.

   Sie können Geschenkgutscheine mit festen Preisen, einem offenen Preis oder beidem erstellen.

   >[!NOTE]
   >
   >Ein Geschenkgutschein hat keinen eigenen Preis im Katalog. Der Preis der Geschenkkarte wird aus dem ausgewählten Betrag der Geschenkkarte während des Kaufs abgeleitet.

   ![Geldkartenbeträge](./assets/product-create-gift-card-amounts.png){width="600" zoomable="yes"}

### Schritt 4: Grundlegende Einstellungen durchführen

1. Geben Sie für eine physische oder kombinierte Geschenkkarte die **[!UICONTROL Quantity]** auf Lager ein.

1. Wenn die zu versendende Geschenkkarte, geben Sie die **[!UICONTROL Weight]** des Pakets ein.

1. Wählen Sie im Feld **[!UICONTROL Categories]** die Option `Gift Card` aus.

Es kann zusätzliche individuelle Attribute geben, die das Produkt beschreiben. Die Auswahl variiert den Attributsatz und kann später abgeschlossen werden.

### Schritt 5: Geschenkgutschein-Informationen ausfüllen

Der Abschnitt &quot;_[!UICONTROL Gift Card Information]_&quot;der Produkteinstellungen kann verwendet werden, um die Einstellungen für die [Konfiguration der Geschenkkarte](../configuration-reference/sales/gift-cards.md) zu überschreiben, die bestimmen, wie die Karte verwaltet wird.

1. Scrollen Sie nach unten zum Abschnitt &quot;_[!UICONTROL Gift Card Information]_&quot;.

   Die Standardeinstellungen in diesem Abschnitt werden durch die Systemkonfiguration bestimmt.

   ![Informationen zur Gift-Karte](./assets/product-gift-card-information.png){width="600" zoomable="yes"}

1. Ändern Sie zusätzliche Felder entsprechend der gewünschten Funktion der Geschenkkarte:

   - **[!UICONTROL Treat Balance as Store Credit]** - Stellt fest, ob der Besitzer der Geschenkkarte den Restbetrag als Gutschrift einlösen kann.

   - **[!UICONTROL Lifetime (days)]** - Bestimmt die Anzahl der Tage nach dem Kauf, bis die Geschenkkarte abläuft. Wenn Sie keine Begrenzung für die Lebensdauer der Karte festlegen möchten, lassen Sie dieses Feld leer.

   - **[!UICONTROL Allow Message]** - Stellt fest, ob der Käufer der Geschenkkarte eine Nachricht für den Empfänger eingeben kann. Eine Geschenknachricht kann sowohl für virtuelle (per E-Mail versandte) als auch für physische (versandte) Geschenkkarten enthalten sein.

   - **[!UICONTROL Email Template]** - Bestimmt die E-Mail-Vorlage, die für die Benachrichtigung verwendet wird, die an den Empfänger einer Geschenkkarte gesendet wird.

### Schritt 6: Produktinformationen ausfüllen

Füllen Sie die Informationen in den folgenden Abschnitten nach Bedarf aus:

- [Inhalt](product-content.md)
- [Bilder und Videos](product-images-and-video.md)
- [Zugehörige Produkte, Up-Sells und Cross-Sells](related-products-up-sells-cross-sells.md)
- [Suchmaschinenoptimierung](product-search-engine-optimization.md)
- [Anpassbare Optionen](settings-advanced-custom-options.md)
- [Produkte in Websites](settings-basic-websites.md)
- [Design](settings-advanced-design.md)
- [Geschenkoptionen](product-gift-options.md)

### Schritt 7: Publish des Produkts

1. Wenn Sie bereit sind, das Produkt im Katalog zu veröffentlichen, setzen Sie den Schalter **Produkt aktivieren** auf `Yes`.

1. Führen Sie einen der folgenden Schritte aus:

   **Methode 1:** Speichern und Vorschau anzeigen

   - Klicken Sie in der oberen rechten Ecke auf **[!UICONTROL Save]**.

   - Um das Produkt in Ihrem Store anzuzeigen, wählen Sie **[!UICONTROL Customer View]** im Menü _Admin_ ( ![Menüpfeil](../assets/icon-menu-down-arrow-black.png) ),

   ![Kundenansicht](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   **Methode 2:** Speichern und schließen

   Wählen Sie im Menü _[!UICONTROL Save]_( ![Menüpfeil](../assets/icon-menu-down-arrow-red.png){width="25"} ) die Option **[!UICONTROL Save & Close]**.

## Dinge, die man sich merken sollte

- Ein _Codepool_ mit eindeutigen Zahlen muss generiert werden, bevor eine Geschenkkarte zum Verkauf angeboten werden kann.

- Geschenkkarten können auf `Redeemable` oder `Non-Redeemable` gesetzt werden.

- Steuern werden **_nicht auf Geschenkkarten während des Geschenkkartenkaufes angewendet_**. Steuern werden nur auf Produkte erhoben, wenn eine erworbene Geschenkkarte zum Kauf von Produkten verwendet wird.

- Die Lebensdauer einer Geschenkkarte kann unbegrenzt sein oder auf eine bestimmte Anzahl von Tagen festgelegt werden.

- Der Wert einer Geschenkkarte kann auf einen festen Betrag oder auf einen offenen Betrag mit einem Mindest- und Höchstwert gesetzt werden.

- Ein Geschenkgutschein hat keinen eigenen Preis im Katalog. Der Preis der Geschenkkarte wird aus dem ausgewählten Betrag der Geschenkkarte während des Kaufs abgeleitet.

- Ein Geschenkkartenkonto für den Kunden kann bei der Bestellung oder zum Zeitpunkt der Rechnung erstellt werden.
