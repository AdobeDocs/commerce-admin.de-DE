---
title: Herunterladbare Produkte importieren
description: Sehen Sie sich ein Beispiel für den Import von Produktdaten für ein herunterladbares Produkt an.
exl-id: e0b45ef5-dff1-4ee4-aa7e-2407162669fd
feature: Products, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 0%

---

# Herunterladbare Produkte importieren

Der Importfluss von herunterladbaren Produkten entspricht dem von [Bundle-Produkte](data-transfer-bundle-products.md) oder [Konfigurierbare Produkte](data-transfer-configurable-products.md). Der Unterschied besteht darin, dass ein herunterladbares Produkt [herunterladbare Links](../catalog/product-create-downloadable.md) und [herunterladbare Beispiele](../catalog/product-create-downloadable.md) mit den Bildern.

Der Standardstammordner für herunterladbare Links und Beispiele lautet `<Magento-root-folder>/pub/media/import`. Wenn das Remote-Speichermodul aktiviert ist, ist der standardmäßige Stammordner für herunterladbare Links und Beispiele der `<remote-storage-root-folder>/media/import` Verzeichnis.

Die CSV-Datei verfügt über separate Spalten für `downloadable_links` und `downloadable_samples`.

- **Herunterladbare Link-Bilder** — Im folgenden Beispiel werden Bilder von herunterladbaren Links (`red.jpg` und `black.jpg`) in der `<Magento-root-folder>/pub/media/import/test` Ordner. Wenn der Remote-Speicher aktiviert ist, befinden sich diese Bilder im `<remote-storage-root-folder>/media/import/test` Ordner.

  ![Beispieldaten - herunterladbares Produkt mit herunterladbaren Links](./assets/data-import-downloadable-links.png){width="600" zoomable="yes"}

- **Herunterladbare Beispielbilder** — Im folgenden Beispiel wird das herunterladbare Beispielbild (`white.jpg`) im `<Magento-root-folder>/pub/media/import/test` Ordner. Wenn der Remote-Speicher aktiviert ist, befindet sich dieses Bild im `<remote-storage-root-folder>/media/import/test` Ordner.

  ![Beispieldaten - herunterladbares Produkt mit herunterladbaren Beispielen](./assets/data-import-downloadable-samples.png){width="400" zoomable="yes"}

Weitere Informationen zum Aktivieren und Verwalten des Remote-Speichermoduls finden Sie unter [Remote-Speicher konfigurieren](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/storage/remote-storage/remote-storage.html) im _Konfigurationshandbuch_.
