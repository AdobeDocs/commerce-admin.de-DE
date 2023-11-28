---
title: Einfuhrstufungspreise
description: Erfahren Sie, wie Sie Tier-Preisdaten exportieren und aktualisierte Daten importieren können.
exl-id: b19d0208-68b3-45ba-9896-318e12ff4131
feature: Products, Data Import/Export
source-git-commit: 55b0672984ce8cdb853daf024299919beaf7ce0b
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 0%

---

# Einfuhrstufungspreise

anstatt [Staffelpreise](../catalog/product-price-tier.md) manuell für jedes Produkt verwenden, kann es effizienter sein, [importieren](data-import.md) die Preisdaten. Bevor Sie beginnen, erstellen Sie eine Beispieldatei mit exportierten Tier-Preisdaten, die Sie als Vorlage verwenden können.

![Beispiel-Storefront - gestaffelte Preise](./assets/storefront-tier-pricing-water-bottle.png){width="700" zoomable="yes"}

## Schritt 1: Exportieren Sie die Daten zum Tierpreis.

Im folgenden Beispiel werden die Kategoriedaten für ein einzelnes Produkt exportiert. Anschließend können Sie die exportierten Daten als Vorlage für Massenimporte von Tier-Preisdaten verwenden. Weitere Informationen zum Exportieren erweiterter Preisdaten finden Sie unter [Erweiterte Preisdaten](data-attributes-product.md#advanced-pricing-attributes).

![Produktgestaffelte Preise](./assets/price-tier-customer-group-discount.png){width="600" zoomable="yes"}

1. on _Admin_ Seitenleiste, navigieren Sie zu  **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. under _[!UICONTROL Export Settings]_, set **[!UICONTROL Entity Type]**nach `Advanced Pricing`.

1. Im **[!UICONTROL Entity Attributes]** scrollen Sie nach unten zu den SKU-Attributen und führen Sie die folgenden Schritte aus:

   - Für Tier-Preise, die auf einem Rabattprozentsatz basieren, geben Sie die SKU jedes zu exportierenden Produkts ein, getrennt durch Kommas.

     ![Datenexport - Produkt-SKUs](./assets/price-tier-export-sku.png){width="600" zoomable="yes"}

   - Für Tier-Preise, die auf einem festen Betrag basieren, geben Sie die SKU jedes Produkts an.

   - Scrollen Sie nach unten und klicken Sie auf **[!UICONTROL Continue]**.

1. Suchen Sie die Exportdatei im Speicherort für Downloads Ihres Webbrowsers und öffnen Sie die Datei.

   ![Beispiel: exportierte Rabattstufenpreisdaten der Kundengruppe](./assets/price-tier-customer-group-discount-export.png){width="600" zoomable="yes"}

**_Exportierte Tier-Preisdaten_**

Die folgenden Spalten sind in den exportierten Daten enthalten:

- `sku`
- `tier_price_website`
- `tier_price_customer_group`
- `tier_price_qty`
- `tier_price`
- `tier_price_value_type`

Sie verwenden die exportierten Daten als Vorlage zum Importieren von Tier-Preisdaten.

## Schritt 2: Daten aktualisieren

1. Aktualisieren Sie bei Bedarf die Stufenpreisdaten für jedes Produkt.

   Alle Produkte ohne Tier-Preisaktualisierungen können aus der CSV-Datei gelöscht werden. Es ist nicht erforderlich, nicht geänderte Produkte erneut zu importieren.

1. **[!UICONTROL Save]** die aktualisierte CSV-Datei.

>[!NOTE]
>
>Die Importdatei darf nicht größer als 2 MB sein.

## Schritt 3: Aktualisierte Daten importieren

1. on _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**.

1. under _Importeinstellungen_, set **[!UICONTROL Entity Type]** nach `Advanced Pricing`.

1. Satz **[!UICONTROL Import Behavior]** nach `Add/Update`.

1. under **[!UICONTROL File to Import]** klicken **[!UICONTROL Choose File]** und wählen Sie die Datei aus, die Sie für den Import aus Ihrem Verzeichnis vorbereitet haben.

1. Klicken Sie oben rechts auf **[!UICONTROL Check Data]**.

1. Wenn die Datei gültig ist, klicken Sie auf **[!UICONTROL Import]**.

   Korrigieren Sie andernfalls jedes Problem mit den in der Nachricht aufgelisteten Daten und versuchen Sie erneut, die Datei zu importieren.
