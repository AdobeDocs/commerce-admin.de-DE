---
title: Katalogpreisregel mit mehreren SKUs
description: Erfahren Sie, wie Sie eine einzelne Katalogpreisregel auf mehrere SKUs anwenden.
exl-id: 99023460-0501-45cd-8990-5f2b9ed7b4a2
feature: Merchandising, Price Rules, Catalog Management
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 0%

---

# Katalogpreisregel mit mehreren SKUs

Eine einzige Katalogpreisregel kann auf mehrere SKUs angewendet werden, wodurch es möglich ist, verschiedene Promotions basierend auf einem Produkt, einer Marke oder einer Kategorie zu erstellen. Beim Erstellen dieser Regel sollten Sie Bedingungen festlegen, die den ausgewählten SKUs entsprechen. Beim Erstellen der Regel können Sie SKUs einfach im Raster durchsuchen und auswählen.

## Schritt 1. Überprüfen der Storefront-Eigenschaften des Produktattributs

Bevor Sie beginnen, stellen Sie sicher, [ die „Storefront](../catalog/attribute-product-create.md#step-4-describe-the-storefront-properties)-Eigenschaften des `sku`-Attributs auf `Use in Promo Rules` festgelegt sind.

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Geben Sie im Suchfilter oben in der Spalte _[!UICONTROL Attribute Code]_&#x200B;den Wert `sku` ein und klicken Sie auf **[!UICONTROL Search]**.

1. Klicken Sie, um das Attribut `sku` im Bearbeitungsmodus zu öffnen.

1. Klicken Sie im linken Bedienfeld auf **[!UICONTROL Storefront Properties]** und stellen Sie sicher, dass **[!UICONTROL Use for Promo Rule Conditions]** auf `Yes` gesetzt ist.

1. Wenn Sie den Wert der Eigenschaft geändert haben, klicken Sie auf **[!UICONTROL Save Attribute]**.

## Schritt 2. Preisregel auf mehrere SKUs anwenden

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Catalog Price Rules]**.

1. Führen Sie einen der folgenden Schritte aus:

   - Befolgen Sie die Anweisungen zum Erstellen [Katalogpreisregel](price-rules-catalog.md).
   - Öffnen Sie eine vorhandene Katalogpreisregel.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Conditions]** und führen Sie folgende Schritte aus:

   - Setzen Sie in der ersten Zeile den ersten Parameter auf `ANY`.

     ![Bedingung der Katalogpreisregel - ANY](./assets/multiple-skus-condition1.png){width="600" zoomable="yes"}

   - Klicken Sie _Hinzufügen_ (![Symbol hinzufügen](../assets/icon-add-green-circle.png)) am Anfang der nächsten Zeile und klicken Sie in der Liste unter **[!UICONTROL Product Attribute]** auf `SKU`.

     ![Bedingung der Katalogpreisregel - SKU ist eine der folgenden](./assets/multiple-skus-condition1a.png){width="600" zoomable="yes"}

   - Für den Vergleich haben Sie Optionen. Wenn Sie mindestens eine SKU aus einer Liste von SKUs suchen möchten, `select is one of` Sie. Wenn Sie eine Gruppe von SKUs suchen möchten, für die alle gefunden werden müssen, wählen Sie `is` aus. Wir empfehlen die Auswahl von `is one of`.

     ![Bedingung der Katalogpreisregel - SKU ist eine der folgenden](./assets/multiple-skus-condition1b.png){width="600" zoomable="yes"}

   - Um die Bedingung abzuschließen, klicken Sie auf den Link Mehr (**…**) und klicken Sie auf _Auswahl_ (![Listensymbol](../assets/icon-list-chooser.png)) für die Liste der verfügbaren Produkte.

     ![Bedingung der Katalogpreisregel - mehrere SKUs](./assets/multiple-skus-condition2b.png){width="600" zoomable="yes"}

   - Durchsuchen, filtern oder suchen Sie nach den SKUs, die Sie hinzufügen möchten. Aktivieren Sie in der Liste das Kontrollkästchen jedes Produkts, das einbezogen werden soll.

   - Klicken Sie auf **[!UICONTROL Save and Apply]** , um der Bedingung die SKUs hinzuzufügen.

     ![Bedingung der Katalogpreisregel - mehrere SKUs](./assets/multiple-skus-condition2.png){width="600" zoomable="yes"}

1. Schließen Sie die Regel einschließlich aller [Aktionen](price-rules-catalog.md) ab, die ausgeführt werden sollen, wenn die Bedingungen erfüllt sind.

1. Wenn Ihre Regel abgeschlossen ist, klicken Sie auf **[!UICONTROL Save]**.

{{new-price-rule}}
