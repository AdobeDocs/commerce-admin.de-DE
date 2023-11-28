---
title: Importieren von Produktbildern
description: Erfahren Sie, wie Sie Produktbilder mithilfe des Pfads und des Dateinamens der einzelnen Bilder importieren.
exl-id: 991550e6-9ce2-4472-becb-3492bd4c9582
feature: Products, Data Import/Export, Media
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '835'
ht-degree: 0%

---

# Importieren von Produktbildern

Es können mehrere Produktbilder jeden Typs in Adobe Commerce und Magento Open Source importiert und mit einem bestimmten Produkt verknüpft werden. Der Pfad und der Dateiname jedes Produktbilds werden in die CSV-Datei eingegeben und die zu importierenden Bilddateien werden in den entsprechenden Pfad auf den Commerce-Server oder externen Server hochgeladen.

Commerce erstellt eine eigene Verzeichnisstruktur für Produktbilder, die alphabetisch organisiert sind. Wenn Sie Produktdaten mit vorhandenen Bildern in eine CSV-Datei exportieren, wird der alphabetisierte Pfad vor dem Dateinamen jedes Bildes angezeigt. Beim Import neuer Bilder müssen Sie jedoch keinen Pfad angeben, da Commerce die Verzeichnisstruktur automatisch verwaltet. Geben Sie jedoch den relativen Pfad zum Importverzeichnis vor dem Dateinamen der zu importierenden Bilder an.

Um Bilder hochladen zu können, müssen Sie über Anmeldedaten und die entsprechenden Berechtigungen für den Zugriff auf den Ordner Commerce auf dem Server verfügen. Mit den richtigen Anmeldeinformationen können Sie jedes SFTP-Dienstprogramm verwenden, um die Dateien von Ihrem Desktop-Computer auf den Server hochzuladen.

Bevor Sie versuchen, viele Bilder zu importieren, überprüfen Sie die Schritte in der Importmethode, die Sie verwenden möchten, und führen Sie den Prozess mit einigen Produkten durch. Wenn Sie wissen, wie es funktioniert, können Sie große Mengen von Bildern importieren.

>[!IMPORTANT]
>
>Es wird empfohlen, ein Programm zu verwenden, das die UTF-8-Kodierung unterstützt, um CSV-Dateien zu bearbeiten, z. B. Notepad++. Microsoft® Excel fügt zusätzliche Zeichen in die Spaltenüberschrift der CSV-Datei ein, wodurch verhindert werden kann, dass die Daten wieder in Commerce importiert werden.

## Methode 1: Importieren von Bildern vom lokalen Server

1. Laden Sie die Bilddateien auf dem Commerce-Server in die `var/import/images` Ordner oder Unterordner, z. B. `var/import/images/product_images`. Dies ist der Standardstammordner für den Import von Produktbildern.

   ```terminal
   <Magento root folder>/var/import/images
   ```

   >[!NOTE]
   >
   Einstieg in Adobe Commerce und Magento Open Source `2.3.2` release den Pfad, der in der **[!UICONTROL Images File Directory]** Verketten für den Import in das Basisverzeichnis der Bilder - `<Magento-root-folder>/var/import/images`. Bei früheren Adobe Commerce- und Magento Open Source-Versionen können Sie einen anderen Ordner auf dem Commerce-Server verwenden, sofern der Ordnerpfad während des Importvorgangs angegeben wird.

1. Geben Sie in den CSV-Daten den Namen jeder Bilddatei ein, die in die richtige Zeile importiert werden soll, indem Sie `sku`und in der richtigen Spalte nach Bildtyp (`base_image`, `small_image`, `thumbnail_image`oder `additional_images`).

   >[!NOTE]
   >
   Für Bilder im standardmäßigen Importordner (`var/import/images`) nicht den Pfad vor dem Dateinamen in die CSV-Daten aufnehmen.

   Die CSV-Datei darf nur die `sku` und die zugehörigen Bildspalten.

   ![Beispiel: Import von CSV-Bilddaten](./assets/data-import-csv-image-files-default-local.png){width="600" zoomable="yes"}

1. Befolgen Sie die Anweisungen unter [importieren](data-import.md) die Daten.

1. Geben Sie nach Auswahl der zu importierenden Datei den relativen Pfad wie folgt ein: **[!UICONTROL Images File Directory]**.

   ```terminal
   var/import/images
   ```

   ![Dateiverzeichnis für Datenimport-Bilder](./assets/data-import-file-to-import.png){width="600" zoomable="yes"}

   >[!TIP]
   >
   Urlaub _[!UICONTROL Images File Directory]_leer zur Verwendung der `<Magento-root-folder>/var/import/images` Verzeichnis. Ab Adobe Commerce- und Magento Open Source-Version 2.3.2 ist dies der standardmäßige Basisordner für Importbilder.

   Wenn mehrere Bilder für eine `sku`, fügen Sie die Bilder in eine Spalte mit dem Namen ein. `additional_images` (Spalte hinzufügen, falls noch nicht hinzugefügt), durch Kommas getrennt. Beispiel: `image02.jpg,image03.jpg`

## Methode 2: Importieren von Bildern von einem externen Server

1. Laden Sie die zu importierenden Bilder in den angegebenen Ordner auf den externen Server hoch.

1. Geben Sie in den CSV-Daten die vollständige URL für jede Bilddatei in der richtigen Spalte nach Bildtyp ein (`base_image`, `small_image`, `thumbnail_image`oder `additional_images`).

   ```terminal
   https://example.com/images/image.jpg
   ```

1. Befolgen Sie die Anweisungen unter [importieren](data-import.md) die Daten.

## Methode 3: Importieren von Bildern mit Remote-Speicher

1. Laden Sie im Remote Storage-Modul die Bilddateien in die `var/import/images` Ordner oder Unterordner, z. B. `var/import/images/product_images`. Dies ist der Standardstammordner für den Import von Produktbildern.

   ```terminal
   <remote-storage-root-folder>/var/import/images
   ```

   >[!NOTE]
   >
   Einstieg in Adobe Commerce und Magento Open Source `2.3.2` release den Pfad, der in der _[!UICONTROL Images File Directory]_Verkettet zum Importieren in den Ordner &quot;images base&quot;: `<remote-storage-root-folder>/var/import/images`. Bei früheren Adobe Commerce- und Magento Open Source-Versionen können Sie einen anderen Ordner auf dem Commerce-Server verwenden, sofern der Ordnerpfad während des Importvorgangs angegeben wird.

1. Geben Sie in den CSV-Daten den Namen jeder Bilddatei ein, die in die richtige Zeile importiert werden soll, indem Sie `sku`und in der richtigen Spalte nach Bildtyp (`base_image`, `small_image`, `thumbnail_image`oder `additional_images`).

   >[!NOTE]
   >
   Für Bilder im standardmäßigen Importordner (`var/import/images`) nicht den Pfad vor dem Dateinamen in die CSV-Daten aufnehmen.

   Die CSV-Datei darf nur die `sku` und die zugehörigen Bildspalten.

   ![Beispiel: Import von CSV-Bilddaten](./assets/data-import-csv-image-files-default-local.png){width="600" zoomable="yes"}

1. Befolgen Sie die Anweisungen unter [importieren](data-import.md) die Daten.

1. Geben Sie nach Auswahl der zu importierenden Datei den relativen Pfad wie folgt ein: **[!UICONTROL Images File Directory]**.

   ```terminal
   var/import/images/product_images
   ```

   >[!TIP]
   >
   Lassen Sie die _[!UICONTROL Images File Directory]_leer zur Verwendung der `<Magento-root-folder>/var/import/images` Verzeichnis. Ab Adobe Commerce- und Magento Open Source-Version 2.3.2 ist dies der standardmäßige Basisordner für Importbilder.

   Wenn mehrere Bilder für eine `sku`, fügen Sie die Bilder in eine Spalte mit dem Namen ein. `additional_images` (Fügen Sie die Spalte hinzu, falls noch nicht geschehen), getrennt durch Kommas: `image02.jpg,image03.jpg`

Weitere Informationen zum Aktivieren und Verwalten des Remote-Speichermoduls finden Sie unter [Remote-Speicher konfigurieren](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/storage/remote-storage/remote-storage.html) im _Konfigurationshandbuch_.

>[!NOTE]
>
Beim Importieren von Produktbildern wird die Bildgröße nicht erhöht. Die Größe von Produktbildern wird auf dem Frontend von `pub/get.php`. Stellen Sie sicher, dass Ihr `pub/get.php` funktioniert ordnungsgemäß. Andernfalls kann die Größe von Bildern nicht geändert werden.
