---
title: Preissegment
description: Erfahren Sie mehr über den Umfang, der für Produktpreise verwendet wird und der so konfiguriert werden kann, dass er auf globaler oder Website-Ebene angewendet werden kann.
exl-id: 3726b16b-4ed5-4286-a7fd-69ed6677f87a
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 0%

---

# Preissegment

Der Anwendungsbereich der [Basiswährung](../stores-purchase/currency-configuration.md) die für Produktpreise verwendet wird, können so konfiguriert werden, dass sie entweder auf globaler oder auf Website-Ebene angewendet werden. Wenn der Preis auf die globale Ebene angewendet wird, wird der gleiche Preis in der gesamten Store-Hierarchie verwendet. Wenn dasselbe Produkt auf Website-Ebene angewendet wird, kann es zu unterschiedlichen Preisen als Geschäfte verfügbar sein, die mit verschiedenen Websites verbunden sind. Standardmäßig ist der Umfang der Produktpreise global.

Verschiedene Faktoren können sich auf den Preis desselben Produkts an einem Ort und nicht an einem anderen auswirken. Beispielsweise können zusätzliche Vertriebskosten für das Produkt und andere Aspekte vorliegen, die sich auf den Preis von Produkten auswirken, die in einem bestimmten Geschäft verkauft werden. Das folgende Diagramm zeigt eine Multisite-Installation, bei der die Basiswährung auf Website-Ebene eingestellt ist. Die Stores und Store-Ansichten, die mit jeder Website verknüpft sind, spiegeln die Produktpreise wider, die auf der Website-Ebene festgelegt werden.

![B2B für Adobe Commerce](../assets/b2b.svg) Wenn Sie freigegebene Kataloge verwenden, lesen Sie auch den Abschnitt [Festlegen der gemeinsamen Preise und Struktur von Katalogen](../b2b/catalog-shared-pricing-structure.md) im _B2B für Adobe Commerce-Handbuch_.

![Preisdiagramm](./assets/catalog-price-scope.svg){width="550"}

## Konfigurieren des Preisumfangs

1. Im _Admin_ Menü, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Catalog]** und wählen **[!UICONTROL Catalog]** darunter.

1. Scrollen Sie nach unten zum **[!UICONTROL Price]** Abschnitt und Satz **[!UICONTROL Catalog Price Scope]** auf einen der folgenden Werte zu:

   - `Global`
   - `Website`

   Die von Ihnen ausgewählte Perimeter-Einstellung wird unter den Preisfeldern in Ihrem Katalog angezeigt.

   ![Katalogpreisbereich](./assets/catalog-price.png){width="600" zoomable="yes"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

## Verwendungsbereich zur Einrichtung der Produktpreise

In Commerce ist es nicht möglich, für jeden Store einen Produktpreis festzulegen. Sie können jedoch den Preis pro Website ändern:

1. Im _Admin_ Menü, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Catalog]** und wählen **[!UICONTROL Catalog]** darunter.

1. Im **[!UICONTROL Price]** Registerkarte festlegen, setzen Sie den Preisbereich auf `Website` anstatt global.

1. Legen Sie den Preis fest, indem Sie die Seite zur Produktbearbeitung öffnen, den Bereich oben links auswählen und dann einen neuen Preis pro Website eingeben.
