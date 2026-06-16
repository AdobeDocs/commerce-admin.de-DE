---
title: Herunterladbare Produkte importieren
description: Sehen Sie sich ein Beispiel für den Import von Produktdaten für ein herunterladbares Produkt an.
exl-id: e0b45ef5-dff1-4ee4-aa7e-2407162669fd
feature: Products, Data Import/Export
TQID: https://experienceleague.adobe.com/a62y8GDLpN0PHxlm8EYHHMsHfzzkjB4mSNa-BV78Ra8
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 183
ht-degree: 0%

---

# Herunterladbare Produkte importieren

Der Ablauf für den Import herunterladbarer Produkte ist derselbe wie für [Bundle-](data-transfer-bundle-products.md) oder [konfigurierbare Produkte](data-transfer-configurable-products.md). Der Unterschied besteht darin, dass ein herunterladbares Produkt [herunterladbare Links](../catalog/product-create-downloadable.md) und [herunterladbare Beispiele](../catalog/product-create-downloadable.md) mit seinen Bildern hat.

Der standardmäßige Stammordner für herunterladbare Links und Beispiele ist `<Magento-root-folder>/pub/media/import`. Wenn das Remote-Speichermodul aktiviert ist, ist der standardmäßige Stammordner für herunterladbare Links und Beispiele der `<remote-storage-root-folder>/media/import`.

Die CSV-Datei enthält separate Spalten für `downloadable_links` und `downloadable_samples`.

- **Herunterladbare Link**-Bilder: Im folgenden Beispiel befinden sich herunterladbare Link-Bilder (`red.jpg` und `black.jpg`) im Ordner `<Magento-root-folder>/pub/media/import/test` . Wenn die Remote-Speicherung aktiviert ist, befinden sich diese Bilder im Ordner `<remote-storage-root-folder>/media/import/test`.

  ![Beispieldaten - herunterladbares Produkt mit herunterladbaren Links](./assets/data-import-downloadable-links.png){width="600" zoomable="yes"}

- **Herunterladbare Beispielbilder** - Im folgenden Beispiel befindet sich das herunterladbare Beispielbild (`white.jpg`) im Ordner `<Magento-root-folder>/pub/media/import/test`. Wenn die Remotespeicherung aktiviert ist, befindet sich dieses Bild im Ordner `<remote-storage-root-folder>/media/import/test`.

  ![Beispieldaten - herunterladbares Produkt mit herunterladbaren Beispielen](./assets/data-import-downloadable-samples.png){width="400" zoomable="yes"}

Weitere Informationen zur Aktivierung und Verwaltung des Remote-Speichermoduls finden Sie unter [Konfigurieren von Remote](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/storage/remote-storage/remote-storage.html?lang=de) im _Konfigurationshandbuch_.
