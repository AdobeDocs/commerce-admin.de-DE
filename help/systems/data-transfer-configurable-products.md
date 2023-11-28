---
title: Konfigurierbare Produkte importieren
description: Überprüfen Sie ein Beispiel für den Import von Produktdaten für ein konfigurierbares Produkt.
exl-id: bb8b2a6d-867e-4ab2-bdfd-98a01d79c457
feature: Products, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '943'
ht-degree: 0%

---

# Konfigurierbare Produkte importieren

Die beste Möglichkeit, zu verstehen, wie konfigurierbare Produktdaten strukturiert sind, besteht darin, ein konfigurierbares Produkt und seine Varianten zu exportieren und die Daten in einer Tabelle zu untersuchen.

Im folgenden Beispiel fügen Sie für jede Farbe eine Reihe von Produktvarianten für eine neue Größe hinzu. Exportieren Sie zunächst das konfigurierbare Produkt und untersuchen Sie die Datenstruktur. Aktualisieren Sie dann die Daten und importieren Sie sie wieder in den Katalog. Wenn Sie den Datenexport nicht durchlaufen möchten, können Sie die im Beispiel verwendete CSV-Datei herunterladen.

![Beispiel-Storefront - Größe und Farbattribute](./assets/storefront-hoodie-new-size.png){width="700" zoomable="yes"}

## Schritt 1: Überprüfen der Attributeinstellungen und -werte

1. Bevor Sie beginnen, stellen Sie sicher, dass die Attribute, die für Produktvarianten verwendet werden, über die erforderlichen Eigenschaftseinstellungen verfügen.

   - [**[!UICONTROL Scope]**](../getting-started/websites-stores-views.md#scope-settings) - `Global`
   - [**[!UICONTROL Catalog Input Type for Store Owner]**](data-attributes-product.md) - Der Eingabetyp eines Attributs, das für eine Produktvariante verwendet wird, muss einer der folgenden sein:

      - `Dropdown`
      - `Visual Swatch`
      - `Text Swatch`
      - `Multi-Select`

   - **[!UICONTROL Values Required]** - `Yes`

1. Wenn Sie eine Größe oder Farbe hinzufügen oder eine andere Änderung an einem vorhandenen Attribut vornehmen, stellen Sie sicher, dass Sie das Attribut mit dem neuen Wert aktualisieren.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Suchen Sie das Attribut in der Liste und öffnen Sie es im Bearbeitungsmodus.

1. Fügen Sie dem Attribut den neuen Wert hinzu.

   Im folgenden Beispiel wird einem Textmuster eine neue Größe hinzugefügt.

   ![Produktattribut - neuen Wert hinzufügen](./assets/data-transfer-configurable-product-add-new-attribute-value.png){width="500" zoomable="yes"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Attribute]**.

1. Wenn Sie ein Attribut hinzufügen, befolgen Sie die Anweisungen unter [Attribut erstellen](../catalog/attribute-product-create.md) bevor Sie beginnen.

## Schritt 2: Konfigurierbares Produkt exportieren

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Suchen Sie das konfigurierbare Produkt, das exportiert werden soll:

   - Klicken **[!UICONTROL Filters]**.
   - Satz **[!UICONTROL Type]** nach `Configurable Product` und klicken **[!UICONTROL Apply Filters]**.
   - Wählen Sie das konfigurierbare Produkt aus, das Sie für Ihren Testexport verwenden möchten, und beachten Sie Folgendes: **[!UICONTROL SKU]**.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

   ![Datenexporteinstellungen](./assets/data-transfer-export-settings.png){width="600" zoomable="yes"}

1. under _[!UICONTROL Export Setting]s_ führen Sie folgende Schritte aus:

   - Satz **[!UICONTROL Entity Type]** nach `Products`.

   - Satz **[!UICONTROL Export File Format]** nach `CSV`.

1. under _[!UICONTROL Entity Attributes]_, scrollen Sie nach unten oder verwenden Sie den Filter für die Attributbeschriftung , um die **[!UICONTROL SKU]**Fügen Sie hinzu und führen Sie folgende Schritte aus:

   - Geben Sie die SKU des konfigurierbaren Produkts ein, das Sie exportieren möchten, und klicken Sie auf **[!UICONTROL Continue]**.

     ![Datenexport-SKU](./assets/data-transfer-export-sku.png){width="600" zoomable="yes"}

   - Suchen Sie nach der Datei im Download-Speicherort für Ihren Webbrowser und öffnen Sie sie als Tabelle.

     Die CSV-Datei verfügt über eine separate Zeile für jede einfache Produktvariante und eine Zeile für das konfigurierbare Produkt. Die `product_type column` zeigt mehrere einfache Produktvarianten an, die mit einem konfigurierbaren Produkt verknüpft sind.

     ![Beispieldaten - konfigurierbares Produkt mit Varianten](./assets/data-transfer-csv-configurable-product.png){width="600" zoomable="yes"}

   - Scrollen Sie nach rechts, um die folgenden Spalten zu finden.

      - `configurable_variations` - Definiert die 1:n-Beziehung zwischen dem konfigurierbaren Produktdatensatz und den einzelnen Varianten.
      - `configurable_variation_labels` - Definiert den Titel, der jede Variante identifiziert.

     In diesem Beispiel befinden sich die Daten in den Spalten CG und CH. Je nach Anzahl der Varianten wird die Datenzeichenfolge in der Variablen `configurable_variations` -Spalte kann lang sein. Die Daten werden als Index für die zugehörigen Produktvarianten verwendet und weisen die folgende Struktur auf:

     ```text
     sku={{SKU_VALUE}},attribute1={{VALUE}},attribute2={{VALUE}}| sku={{SKU_VALUE}},attribute1={{VALUE}},attribute2={{VALUE}}
     ```

     Jede SKU wird durch ein senkreches Symbol (|) getrennt und Attribute werden durch ein Komma getrennt. Der Wert jedes Attributs wird durch den Attributcode und nicht durch die Attributbeschriftung dargestellt. So werden die tatsächlichen Daten angezeigt:

     ```text
     sku=MH01-XS-Black,size=XS,color=Black|sku=MH01-XS-Gray,size=XS,color=Gray|sku=MH01-XS-Orange,size=XS,color=Orange</pre>
     ```

1. Wenn Sie die Struktur konfigurierbarer Produktdaten verstehen, können Sie die Daten bearbeiten oder neue Varianten direkt zur CSV-Datei hinzufügen.

   Weitere Informationen finden Sie unter [Komplexe Daten](data-attributes-product.md#complex-product-data-attributes).

## 3. Schritt: Daten bearbeiten

Im folgenden Beispiel wird der Satz von XL-Größen kopiert und in das Arbeitsblatt eingefügt, um eine Reihe von Produktvarianten für eine neue Größe in jeder Farbe zu erstellen.

1. Kopieren Sie die Produktvarianten, die Sie als Vorlage für die neuen Produkte verwenden möchten.

   ![Exportierte Daten - Produktvarianten kopieren](./assets/data-transfer-export-configurable-copy-rows.png){width="600" zoomable="yes"}

1. Fügen Sie die kopierten Zeileneinträge in das Arbeitsblatt ein.

   Sie verfügen nun über zwei identische Sätze der einfachen Produktvarianten.

   ![CSV-Daten - Hinzufügen von Produktvarianten](./assets/data-transfer-export-configurable-copy-rows.png){width="600" zoomable="yes"}

1. Aktualisieren Sie bei Bedarf die Daten in den folgenden Spalten der neuen Varianten.

   - `sku`
   - `name`
   - `url_key`
   - `additional_attributes`

   In diesem Beispiel wird die `XL` Verweise werden geändert in `XXL`.

1. Aktualisieren Sie die Informationen in der `product_variations` -Spalte des konfigurierbaren Produktdatensatzes, sodass die neuen Varianten als Teil des konfigurierbaren Produkts enthalten sind.

   Klicken Sie in der Zeile mit dem konfigurierbaren Produktdatensatz auf die Zelle, die die `product_variations` Daten. Kopieren Sie dann in der Formelleiste den letzten Parametersatz, beginnend mit dem Pipe-Symbol.

   ![product_variations-Daten](./assets/data-transfer-export-configurable-product-product-variations-data.png){width="600" zoomable="yes"}

1. Fügen Sie die Parameter am Ende der Daten ein und bearbeiten Sie sie nach Bedarf für die neuen Varianten.

   In diesem Beispiel wird die `sku` und `size` -Parameter für die neue XXL-Größe aktualisiert.

1. Bevor die Daten wieder in den Katalog importiert werden, löschen Sie alle Zeilen, die nicht geändert wurden.

   In diesem Beispiel werden nur die drei neuen Varianten für die neue Größe und die Zeile mit dem aktualisierten konfigurierbaren Produkt wieder in den Katalog importiert. Die anderen Zeilen können aus der CSV-Datei gelöscht werden. Achten Sie jedoch darauf, die Kopfzeile mit Spaltenbezeichnungen nicht zu löschen.

   ![Zu importierende CSV-Daten](./assets/data-transfer-csv-configurable-product-data-ready-to-import.png){width="600" zoomable="yes"}

1. **[!UICONTROL Save]** die CSV-Datei.

   Die Daten können in den Katalog importiert werden.

   >[!NOTE]
   >
   >Die Importdatei darf nicht größer als 2 MB sein.

## Schritt 4: Aktualisierte Daten importieren

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**.

1. under _[!UICONTROL Import Settings]_, set **[!UICONTROL Entity Type]**nach `Products`.

1. under _[!UICONTROL Import Behavior]_, set **[!UICONTROL Import Behavior]**nach `Add/Update`.

   ![Verhalten beim Datenimport](./assets/data-transfer-configurable-product-import-behavior.png){width="600" zoomable="yes"}

1. under _[!UICONTROL File to Import]_klicken **[!UICONTROL Choose File]**und navigieren Sie zur CSV-Datei, die Sie für den Import vorbereitet haben, und wählen Sie die Datei aus.

   ![Datenimportdatei](./assets/data-import-file-to-import.png){width="600" zoomable="yes"}

1. Klicken Sie oben rechts auf **[!UICONTROL Check Data]**.

1. Wenn die Datei gültig ist, klicken Sie auf **[!UICONTROL Import]**.

   Korrigieren Sie andernfalls alle Probleme in den Daten und versuchen Sie es erneut.

   ![Systemmeldung - Datei ist gültig](./assets/data-transfer-configurable-product-import-validation-results.png){width="600" zoomable="yes"}

1. Wenn der Import abgeschlossen ist, klicken Sie auf **[!UICONTROL Cache Management]** in der Nachricht am oberen Seitenrand ein und aktualisieren Sie alle ungültigen Caches.

   Die neuen Produktvarianten sind jetzt im Katalog vom Administrator und im Storefront verfügbar. In diesem Beispiel ist die Hoodie jetzt in Größe XXL für alle Farben verfügbar.
