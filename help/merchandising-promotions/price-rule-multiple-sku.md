---
title: Katalogpreisregel mit mehreren SKUs
description: Erfahren Sie, wie Sie eine einzige Katalogpreisregel auf mehrere SKUs anwenden.
exl-id: 99023460-0501-45cd-8990-5f2b9ed7b4a2
feature: Merchandising, Price Rules, Catalog Management
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 0%

---

# Katalogpreisregel mit mehreren SKUs

Eine einzige Katalogpreisregel kann auf mehrere SKUs angewendet werden, wodurch verschiedene Promotions basierend auf einem Produkt, einer Marke oder einer Kategorie erstellt werden können. Beim Erstellen dieser Regel möchten Sie Bedingungen festlegen, die mit den ausgewählten SKUs übereinstimmen. Beim Erstellen der Regel können Sie mühelos SKUs aus dem Raster suchen und auswählen.

## Schritt 1. Überprüfen der Storefront-Eigenschaften des Produktattributs

Bevor Sie beginnen, stellen Sie sicher, dass die Variable [Store-Eigenschaften](../catalog/attribute-product-create.md#step-4-describe-the-storefront-properties) des `sku` -Attribut auf `Use in Promo Rules`.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Im Suchfilter oben im _[!UICONTROL Attribute Code]_Spalte eingeben `sku` und klicken **[!UICONTROL Search]**.

1. Klicken Sie auf , um die `sku` -Attribut im Bearbeitungsmodus.

1. Klicken Sie im linken Bereich auf **[!UICONTROL Storefront Properties]** und stellen Sie sicher, dass **[!UICONTROL Use for Promo Rule Conditions]** auf `Yes`.

1. Wenn Sie den Wert der Eigenschaft geändert haben, klicken Sie auf **[!UICONTROL Save Attribute]**.

## Schritt 2. Preisregel auf mehrere SKUs anwenden

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Catalog Price Rules]**.

1. Führen Sie einen der folgenden Schritte aus:

   - Befolgen Sie die Anweisungen zum Erstellen einer [Katalogpreisregel](price-rules-catalog.md).
   - Öffnen Sie eine vorhandene Katalogpreisregel.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Conditions]** und gehen Sie wie folgt vor:

   - Setzen Sie in der ersten Zeile den ersten Parameter auf `ANY`.

     ![Bedingung der Katalogpreisregel - BELIEBIG](./assets/multiple-skus-condition1.png){width="600" zoomable="yes"}

   - Klicks _Hinzufügen_ (![Symbol &quot;Hinzufügen&quot;](../assets/icon-add-green-circle.png)) am Anfang der nächsten Zeile und in der Liste unter **[!UICONTROL Product Attribute]** klicken `SKU`.

     ![Bedingung der Katalogpreisregel - SKU ist eine von](./assets/multiple-skus-condition1a.png){width="600" zoomable="yes"}

   - Für den Vergleich stehen Ihnen Optionen zur Verfügung. Wenn Sie mindestens eine der SKUs aus einer Liste finden möchten, `select is one of`. Wenn Sie eine Gruppe von SKUs finden möchten, die alle angewendet werden sollen, wählen Sie `is`. Es wird empfohlen, `is one of`.

     ![Bedingung der Katalogpreisregel - SKU ist eine von](./assets/multiple-skus-condition1b.png){width="600" zoomable="yes"}

   - Um die Bedingung abzuschließen, klicken Sie auf die weiteren (**...**) und klicken Sie auf den Link _Auswahl_ (![Listen-Symbol](../assets/icon-list-chooser.png)) für die Liste der verfügbaren Produkte.

     ![Bedingung der Katalogpreisregel - mehrere SKUs](./assets/multiple-skus-condition2b.png){width="600" zoomable="yes"}

   - Suchen, filtern oder suchen Sie nach den SKUs, die Sie hinzufügen möchten. Aktivieren Sie in der Liste das Kontrollkästchen der einzuschließenden Produkte.

   - Klicks **[!UICONTROL Save and Apply]** , um die SKUs zur Bedingung hinzuzufügen.

     ![Bedingung der Katalogpreisregel - mehrere SKUs](./assets/multiple-skus-condition2.png){width="600" zoomable="yes"}

1. Schließen Sie die Regel einschließlich aller [Aktionen](price-rules-catalog.md) zu treffen, wenn die Bedingungen erfüllt sind.

1. Klicken Sie nach Abschluss der Regel auf **[!UICONTROL Save]**.

{{new-price-rule}}
