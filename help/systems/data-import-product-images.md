---
title: Import von Produktbildern
description: Erfahren Sie, wie Sie Produktbilder unter Verwendung des Pfads und Dateinamens der einzelnen Bilder importieren.
exl-id: 991550e6-9ce2-4472-becb-3492bd4c9582
feature: Products, Data Import/Export, Media
source-git-commit: 53c3b6c9fa9c152e6619528a43580b0acc71a2a5
workflow-type: tm+mt
source-wordcount: '836'
ht-degree: 0%

---

# Import von Produktbildern

Mehrere Produktbilder jedes Typs können in Adobe Commerce und Magento Open Source importiert und mit einem bestimmten Produkt verknüpft werden. Der Pfad und der Dateiname jedes Produktbilds werden in die CSV-Datei eingegeben, und die zu importierenden Bilddateien werden in den entsprechenden Pfad auf dem Commerce-Server oder externen Server hochgeladen.

Commerce erstellt eine eigene Verzeichnisstruktur für Produktbilder, die alphabetisch angeordnet ist. Wenn Sie Produktdaten mit vorhandenen Bildern in eine CSV-Datei exportieren, sehen Sie den alphabetisch nach dem Dateinamen der einzelnen Bilder sortierten Pfad. Beim Importieren neuer Bilder müssen Sie jedoch keinen Pfad angeben, da Commerce die Verzeichnisstruktur automatisch verwaltet. Achten Sie jedoch darauf, den relativen Pfad zum Importverzeichnis vor dem Dateinamen jedes zu importierenden Bildes einzugeben.

Um Bilder hochzuladen, müssen Sie über Anmeldedaten und korrekte Berechtigungen für den Zugriff auf den Commerce-Ordner auf dem -Server verfügen. Mit den richtigen Anmeldeinformationen können Sie ein beliebiges SFTP-Dienstprogramm verwenden, um die Dateien von Ihrem Desktop-Computer auf den Server hochzuladen.

Bevor Sie versuchen, viele Bilder zu importieren, überprüfen Sie die Schritte in der Importmethode, die Sie verwenden möchten, und durchlaufen Sie den Prozess mit einigen Produkten. Wenn Sie wissen, wie dies funktioniert, werden Sie sicher sein, große Mengen von Bildern zu importieren.

>[!IMPORTANT]
>
>Es wird empfohlen, ein Programm zu verwenden, das die UTF-8-Kodierung zum Bearbeiten von CSV-Dateien unterstützt, z. B. Notepad++. Microsoft® Excel fügt zusätzliche Zeichen in die Spaltenüberschrift der CSV-Datei ein, was verhindern kann, dass die Daten wieder in Commerce importiert werden.

## Methode 1: Importieren von Bildern vom lokalen Server

1. Laden Sie die Grafikdateien auf den Commerce-Server in den `var/import/images` oder in einen Unterordner (z. B. `var/import/images/product_images`) hoch. Dies ist der standardmäßige Stammordner für den Import von Produktbildern.

   ```
   <Magento root folder>/var/import/images
   ```

   >[!NOTE]
   >
   >Ab der Adobe Commerce- und Magento Open Source `2.3.2`-Version wird der im **[!UICONTROL Images File Directory]** angegebene Pfad für den Import in das Bildbasisverzeichnis &quot;`<Magento-root-folder>/var/import/images`&quot; verkettet. Bei früheren Versionen von Adobe Commerce und Magento Open Source können Sie einen anderen Ordner auf dem Commerce-Server verwenden, sofern der Ordnerpfad während des Importvorgangs angegeben wird.

1. Geben Sie in den CSV-Daten den Namen jeder Bilddatei ein, die je nach Bildtyp (`base_image`, `small_image`, `thumbnail_image` oder `additional_images`) in die richtige Zeile, nach `sku` und in die richtige Spalte importiert werden soll.

   >[!NOTE]
   >
   >Fügen Sie für Bilder im standardmäßigen Importordner (`var/import/images`) den Pfad vor dem Dateinamen nicht in die CSV-Daten ein.

   Die CSV-Datei darf nur die Spalte `sku` und die zugehörigen Bildspalten enthalten.

   ![Beispiel - CSV-Bilddatenimport](./assets/data-import-csv-image-files-default-local.png){width="600" zoomable="yes"}

1. Befolgen Sie die Anweisungen zum [Importieren](data-import.md) der Daten.

1. Geben Sie nach Auswahl der zu importierenden Datei den relativen Pfad nach **[!UICONTROL Images File Directory]** ein.

   ```
   var/import/images
   ```

   ![Dateiverzeichnis der Datenimportbilder](./assets/data-import-file-to-import.png){width="600" zoomable="yes"}

   >[!TIP]
   >
   >Lassen Sie _[!UICONTROL Images File Directory]_leer, um das `<Magento-root-folder>/var/import/images` zu verwenden. Ab Adobe Commerce und Magento Open Source 2.3.2 ist dies der standardmäßige Basisordner für den Import von Bildern.

   Wenn Sie mehrere Bilder für ein einzelnes `sku` importieren, fügen Sie die Bilder in eine Spalte mit dem Namen `additional_images` ein (fügen Sie die Spalte hinzu, falls noch nicht hinzugefügt), getrennt durch Kommas. Beispiel: `image02.jpg,image03.jpg`

## Methode 2: Importieren von Bildern von einem externen Server

1. Laden Sie die Bilder hoch, die in den vorgesehenen Ordner auf dem externen Server importiert werden sollen.

1. Geben Sie in den CSV-Daten die vollständige URL für jede Bilddatei in der richtigen Spalte nach Bildtyp (`base_image`, `small_image`, `thumbnail_image` oder `additional_images`) ein.

   ```
   https://example.com/images/image.jpg
   ```

1. Befolgen Sie die Anweisungen zum [Importieren](data-import.md) der Daten.

## Methode 3: Importieren von Bildern mit Remote-Speicher

1. Laden Sie im Remote-Speichermodul die Grafikdateien in den `var/import/images` Ordner oder einen Unterordner hoch, z. B. `var/import/images/product_images`. Dies ist der standardmäßige Stammordner für den Import von Produktbildern.

   ```bash
   <remote-storage-root-folder>/var/import/images
   ```

   >[!NOTE]
   >
   >Ab der Adobe Commerce- und Magento Open Source `2.3.2`-Version wird der im _[!UICONTROL Images File Directory]_angegebene Pfad für den Import in das Bildbasisverzeichnis verkettet: `<remote-storage-root-folder>/var/import/images`. Bei früheren Versionen von Adobe Commerce und Magento Open Source können Sie einen anderen Ordner auf dem Commerce-Server verwenden, sofern der Pfad zum Ordner während des Importvorgangs angegeben wird.

1. Geben Sie in den CSV-Daten den Namen jeder Bilddatei ein, die je nach Bildtyp (`base_image`, `small_image`, `thumbnail_image` oder `additional_images`) in die richtige Zeile, nach `sku` und in die richtige Spalte importiert werden soll.

   >[!NOTE]
   >
   >Fügen Sie für Bilder im standardmäßigen Importordner (`var/import/images`) den Pfad vor dem Dateinamen nicht in die CSV-Daten ein.

   Die CSV-Datei darf nur die Spalte `sku` und die zugehörigen Bildspalten enthalten.

   ![Beispiel - CSV-Bilddatenimport](./assets/data-import-csv-image-files-default-local.png){width="600" zoomable="yes"}

1. Befolgen Sie die Anweisungen zum [Importieren](data-import.md) der Daten.

1. Geben Sie nach Auswahl der zu importierenden Datei den relativen Pfad nach **[!UICONTROL Images File Directory]** ein.

   ```
   var/import/images/product_images
   ```

   >[!TIP]
   >
   >Lassen Sie das _[!UICONTROL Images File Directory]_leer, um das `<Magento-root-folder>/var/import/images` zu verwenden. Ab Adobe Commerce und Magento Open Source 2.3.2 ist dies der standardmäßige Basisordner für den Import von Bildern.

   Wenn Sie mehrere Bilder für ein einzelnes `sku` importieren, fügen Sie die Bilder in eine Spalte mit dem Namen `additional_images` ein (fügen Sie die Spalte hinzu, falls noch nicht hinzugefügt), getrennt durch Kommas: `image02.jpg,image03.jpg`

Weitere Informationen zur Aktivierung und Verwaltung des Remote-Speichermoduls finden Sie unter [Konfigurieren von Remote](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/storage/remote-storage/remote-storage.html) im _Konfigurationshandbuch_.

>[!NOTE]
>
>Beim Importieren von Produktbildern wird keine Bildgröße initiiert. Die Größe der Produktbilder wird im Frontend `pub/get.php` geändert. Vergewissern Sie sich, dass Ihre `pub/get.php` ordnungsgemäß funktioniert. Andernfalls kann es sein, dass die Größe der Bilder nicht geändert wird.
