---
title: Schnellbestellungen
description: Erfahren Sie mehr über die Schnellbestellungsfunktion und deren Aktivierung für Ihre Kunden.
exl-id: 7007e1b4-a64f-46fe-a235-3ca9f64e77e4
feature: B2B, Orders
TQID: https://experienceleague.adobe.com/iwH1JStasz7KM-ECeWAvP-x4niVm-QFg4-GMw8r3SoI
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 438
ht-degree: 0%

---

# Schnellbestellungen

Die _Schnellbestellung_-Funktion reduziert den Bestellvorgang auf mehrere Klicks für Kunden, die den Produktnamen oder die SKU der Produkte kennen, die sie bestellen möchten. Bestellungen mit mehreren SKUs können manuell eingegeben oder in das Schnellbestellungsformular importiert werden. Die Schnellbestellung kann von Kunden, die bei ihren Konten angemeldet sind, und von Gästen verwendet werden. Wenn diese Option aktiviert _, wird_ Link „Schnellbestellung“ oben auf der Seite neben dem Kundennamen angezeigt.

![Schnellbestelllink](./assets/quick-order-link.png){width="700" zoomable="yes"}

## Aktivieren von Schnellbestellungen für Ihren Store

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wählen Sie im Abschnitt _[!UICONTROL General]_&#x200B;im linken Bereich **[!UICONTROL B2B Features]**&#x200B;aus.

1. Legen Sie **[!UICONTROL Enable Quick Order]** auf `Yes` fest.

   ![Schnellbestellung aktivieren](./assets/quick-orders-config.png){width="600" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Save Config]**.

1. Wenn Sie dazu aufgefordert werden, klicken Sie [Cache-Verwaltung](../systems/cache-management.md) und aktualisieren Sie alle ungültigen Caches.

## Workflows für Schnellbestellungen

Kunden können Produkte für Schnellbestellungen mit einer der folgenden Methoden angeben.

### Methode 1: Einzelne Produkte eingeben

1. Der Kunde klickt auf den **[!UICONTROL Quick Order]**.

1. Wählt das Produkt nach SKU oder Produktname aus:

   Um eine **Schnellbestellung nach SKU** aufzugeben, führt der Kunde Folgendes aus:

   - Betritt die **[!UICONTROL SKU]**.

   - Klicks **[!UICONTROL Add to List]**.

     Die SKU wird in der Eingabezeile mit den Produktdetails unten angezeigt.

     ![Schnellbestellungsdetails](./assets/quick-order-product-detail.png){width="600" zoomable="yes"}

   Um eine **Schnellbestellung anhand des Produktnamens** aufzugeben, führt der Kunde Folgendes aus:

   - Gibt die ersten Zeichen des **[!UICONTROL Product Name]** ein.

     >[!NOTE]
     >
     >Verwenden Sie nicht die _Eingabetaste_, um den Namen des Produkts auszuwählen.

   - Wenn die Liste der möglichen Übereinstimmungen angezeigt wird, klickt der Kunde auf das Produkt, das er bestellen möchte.

     ![Klicken, um Produktname auszuwählen](./assets/quick-order-product-name.png){width="700" zoomable="yes"}

1. Betritt die **[!UICONTROL Qty]**.

1. Wiederholt diesen Vorgang mit der nächsten Eingabezeile so oft wie nötig.

1. Klicks **[!UICONTROL Add to Cart]**.

### Methode 2: Mehrere Produkte eingeben

1. Im Feld **[!UICONTROL Enter Multiple SKUs]** führt der Kunde einen der folgenden Schritte aus:

   - Gibt eine SKU pro Zeile ein

   - Gibt alle SKUs in derselben Zeile ein, getrennt durch Kommas und ohne Leerzeichen.

     ![Geben Sie mehrere SKUs ein](./assets/quick-order-skus.png){width="600" zoomable="yes"}

1. Um die Produkte der Liste hinzuzufügen, klicken Sie auf **[!UICONTROL Add to List]**.

1. Gibt für jedes Element in der Liste den zu sortierenden **[!UICONTROL Qty]** an.

   ![Schnellbestellungsliste](./assets/quick-order-skus-detail.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Wenn das Produkt über die erforderlichen Optionen verfügt, wird der Kunde aufgefordert, die Optionen auszuwählen. Sie können warten, bis sie den Warenkorb erreichen, um Produktoptionen hinzuzufügen.

   ![Optionen auswählen](./assets/quick-order-skus-product-options.png){width="600" zoomable="yes"}

### Methode 3: Hochladen einer Liste von Produkten

1. Klicken Sie im Abschnitt _[!UICONTROL Add from File]_&#x200B;auf **[!UICONTROL Download Sample]**, um eine Bestellvorlage herunterzuladen.

   ![Aus Datei hinzufügen](./assets/quick-order-skus-add-from-file.png){width="600" zoomable="yes"}

1. Öffnet die heruntergeladene Datei.

1. Verwendet die Vorlage zum Hinzufügen der Produkt-SKUs, die für die Schnellbestellungsliste hochgeladen werden sollen.

1. Wenn Sie fertig sind, klicken Sie **[!UICONTROL Save]**.

   ![SKUs zum Hochladen](./assets/quick-order-skus-add-from-file-sample.png){width="400" zoomable="yes"}

1. Um die Datei hochzuladen, klicken Sie auf **[!UICONTROL Choose]** und wählen Sie die Datei aus ihrem System aus.

   Die Artikel werden der Schnellbestellungsliste hinzugefügt.

1. Wenn Sie bereit sind, klicken Sie auf **[!UICONTROL Add to Cart]**.

Nachdem der Kunde die Schnellbestellung erstellt hat, kann er wie gewohnt die Kasse durchlaufen.

![Schnellbestellung](./assets/quick-order-add-to-cart.png){width="700" zoomable="yes"}
