---
title: Preisspanne
description: Erfahren Sie mehr über den Umfang der Produktpreise, die entweder global oder auf Website angewendet werden können.
exl-id: 3726b16b-4ed5-4286-a7fd-69ed6677f87a
feature: Catalog Management, Products
TQID: https://experienceleague.adobe.com/4tNRviXPzBubIpyAn9vgUs8BaILjJ6BEdV4yj5ngz6Y
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c18ed297-2187-4aec-affb-9d9654eca6fcid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 376
ht-degree: 0%

---

# Preisspanne

Der Umfang der [Basiswährung](../stores-purchase/currency-configuration.md) die für Produktpreise verwendet wird, kann so konfiguriert werden, dass er entweder auf globaler Ebene oder auf Website-Ebene gilt. Wird der Preis auf globaler Ebene angewendet, wird er in der gesamten Shop-Hierarchie verwendet. Wenn dasselbe Produkt auf Website-Ebene angewendet wird, kann es zu unterschiedlichen Preisen in Geschäften verfügbar sein, die mit verschiedenen Websites verbunden sind. Standardmäßig ist der Umfang der Produktpreise global.

Verschiedene Faktoren können sich auf den Preis des gleichen Produkts an einem Ort und nicht an einem anderen auswirken. So könnten beispielsweise zusätzliche Vertriebskosten für das Produkt und andere Erwägungen anfallen, die sich auf den Preis der in einem bestimmten Geschäft verkauften Produkte auswirken. Das folgende Diagramm zeigt eine Multi-Site-Installation, bei der die Basiswährung auf Website-Ebene festgelegt ist. Die jeder Website zugeordneten Stores und Store-Ansichten spiegeln die Produktpreise wider, die auf Website-Ebene festgelegt werden.

![Adobe Commerce B2B](../assets/b2b.svg) Wenn Sie freigegebene Kataloge verwenden, lesen Sie auch den Abschnitt [Preise und Struktur für freigegebene Kataloge festlegen](../b2b/catalog-shared-pricing-structure.md) im _Adobe Commerce B2B-Handbuch_.

![Preisfindungsdiagramm](./assets/catalog-price-scope.svg){width="550"}

## Konfigurieren des Preisbereichs

1. Gehen Sie _Menü_ Admin“ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Catalog]** und wählen Sie darunter **[!UICONTROL Catalog]**.

1. Scrollen Sie nach unten zum Abschnitt **[!UICONTROL Price]** und legen Sie **[!UICONTROL Catalog Price Scope]** auf eine der folgenden Einstellungen fest:

   - `Global`
   - `Website`

   Die von Ihnen gewählte Bereichseinstellung wird unter den Preisfeldern in Ihrem Katalog angezeigt.

   ![Katalogpreis-Umfang](./assets/catalog-price.png){width="600" zoomable="yes"}

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

## Berechnung verwenden, um Produktpreise festzulegen

In Commerce ist es nicht zulässig, für jeden Shop einen Produktpreis festzulegen. Sie können jedoch den Preis pro Website ändern:

1. Gehen Sie _Menü_ Admin“ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Catalog]** und wählen Sie darunter **[!UICONTROL Catalog]**.

1. Legen Sie auf der Registerkarte **[!UICONTROL Price]** den Preisbereich auf `Website` statt auf `Global` fest.

1. Legen Sie den Preis fest, indem Sie die Seite zur Produktbearbeitung öffnen, den Umfang oben links auswählen und dann einen neuen Preis pro Website eingeben.

In den seltenen Fällen, in denen der Preisbereich auf `Global` festgelegt ist, kann die Commerce-Datenbank auf der Website weiterhin unterschiedliche Preise aufweisen. Dies kann infolge von Synchronisationsproblemen außerhalb von Commerce auftreten. In diesen Fällen muss der Händler eine Preisbereinigung auf Store-Ebene durchführen und eine Katalogsynchronisierung mit Commerce Services durchführen.