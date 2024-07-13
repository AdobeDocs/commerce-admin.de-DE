---
title: Produkteinstellungen - [!UICONTROL Related Products, Up-Sells, and Cross-Sells]
description: Für ein Produkt definieren die [!UICONTROL Related Products, Up-Sells, and Cross-Sells] -Einstellungen einfache Werbeblöcke auf der Produktseite, die eine Auswahl zusätzlicher Produkte hervorheben.
exl-id: 5bd65fad-4e55-40db-8702-10c366261565
feature: Catalog Management, Products, Page Content
source-git-commit: f6d52b1a3c8dd411ad3aa7c6027e964f9d49d608
workflow-type: tm+mt
source-wordcount: '617'
ht-degree: 0%

---

# Produkteinstellungen - [!UICONTROL Related Products, Up-Sells, and Cross-Sells]

Verwenden Sie den Abschnitt &quot;_[!UICONTROL Related Products, Up-Sells, and Cross-Sells]_&quot;, um einfache Werbeblöcke einzurichten, die eine Auswahl zusätzlicher Produkte enthalten, die für den Kunden von Interesse sein könnten. Weitere Informationen finden Sie unter [Produktbeziehungen](../merchandising-promotions/product-relationships.md).

![Zugehörige Produkte, Up-Sells und Cross-Sells](./assets/product-related-up-sell-cross-sell.png){width="600" zoomable="yes"}

Jeder Block besteht aus einer Liste von Produkten, die zu einer bestimmten Option gehören.

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL ID] | Eine eindeutige numerische Kennung, die der Produktidentität zugewiesen wird. |
| [!UICONTROL Thumbnail] | Produktminiaturbild. |
| [!UICONTROL Name] | Der Name des Produkts. |
| [!UICONTROL Status] | Gibt den Produktstatus an. Optionen: `Enabled` / `Disabled`. Deaktivierte Produkte werden nicht in den Bausteinen auf der Vorderseite angezeigt. |
| [!UICONTROL Attribute Set] | Der Name des Attributsatzes, der als Vorlage für das Produkt verwendet wird. |
| [!UICONTROL SKU] | Die eindeutige Lagereinheit, die dem Produkt zugewiesen ist. |
| [!UICONTROL Price] | Der Stückpreis des Produkts. |
| [!UICONTROL Action] | Optionen: `Remove`. Entfernt ein Produkt aus dem Block. |

{style="table-layout:auto"}

>[!TIP]
>
>![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) **Produkt-Recommendations mit Adobe Sensei** vereinfacht die Definition von Produktbeziehungen durch die Verwendung künstlicher Intelligenz und maschineller Lernalgorithmen, um eine tiefgehende Analyse aggregierter Besucherdaten durchzuführen. Diese Daten führen in Kombination mit Ihrem Adobe Commerce-Katalog zu sehr ansprechenden, relevanten und personalisierten Erlebnissen für den Käufer.
><br/>
>Weitere Informationen zur Verwendung dieser von Adobe entwickelten Erweiterung als Alternative zu manuell konfigurierten Produktempfehlungen und Upsells finden Sie im _[Handbuch für Produkt-Recommendations](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/guide-overview.html)_.

## Verwandte Produkte

Zugehörige Produkte sollen zusätzlich zu dem Artikel gekauft werden, den der Kunde ansieht. Der Kunde kann den Artikel in den Warenkorb legen, indem er einfach auf das Kontrollkästchen klickt. Die Platzierung des Bausteins _Zugehörige Produkte_ variiert je nach definiertem Design und Seitenlayout. Im folgenden Beispiel wird der Block _Zugehörige Produkte_ unten auf der Seite _Produktansicht_ angezeigt. Bei einem zweispaltigen Layout wird der Block _Zugehörige Produkte_ häufig in der rechten Seitenleiste angezeigt.

![Verwandte Produkte](./assets/storefront-product-related-products.png){width="600" zoomable="yes"}

So richten Sie verwandte Produkte ein:

1. Öffnen Sie das Produkt im Bearbeitungsmodus.

1. Scrollen Sie nach unten und erweitern Sie den Abschnitt **[!UICONTROL Related Products, Up-Sells, and Cross-Sells]** um den ![Erweiterungsselektor](../assets/icon-display-expand.png).

1. Klicken Sie auf **[!UICONTROL Add Related Products]**.

1. Verwenden Sie die [Filtersteuerelemente](../getting-started/admin-grid-controls.md), um die gewünschten Produkte zu finden.

1. Aktivieren Sie in der Liste das Kontrollkästchen jedes Produkts, das Sie als verwandtes Produkt verwenden möchten.

   ![Verwandte Produkte](./assets/products-related-add.png){width="600" zoomable="yes"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Add Selected Products]**.

## Up-Sells

Up-Sell-Produkte sind Artikel, die Ihr Kunde anstelle des derzeit betrachteten Produkts bevorzugen könnte. Ein Artikel, der als Up-Sell angeboten wird, könnte eine höhere Qualität aufweisen, beliebter sein oder eine bessere Gewinnspanne haben. Upsell-Produkte werden auf der Produktseite unter einer Überschrift wie _Sie können auch an den folgenden Produkten interessiert sein_.

![Up-Sell](./assets/storefront-product-upsell.png){width="600" zoomable="yes"}

So wählen Sie Upsell-Produkte aus:

1. Öffnen Sie das Produkt im Bearbeitungsmodus.

1. Scrollen Sie nach unten und erweitern Sie den Abschnitt **[!UICONTROL Related Products, Up-Sells, and Cross-Sells]** um den ![Erweiterungsselektor](../assets/icon-display-expand.png).

1. Klicken Sie auf **[!UICONTROL Add Up-Sell Products]**.

1. Verwenden Sie die [Filtersteuerelemente](../getting-started/admin-grid-controls.md), um die gewünschten Produkte zu finden.

1. Aktivieren Sie in der Liste das Kontrollkästchen jedes Produkts, das Sie als Upsell-Produkt verwenden möchten.

   ![ Up-Sell Products](./assets/product-up-sell-add.png){width="600" zoomable="yes"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Add Selected Products]**.

>[!NOTE]
>
>Das übergeordnete Bundle-Produkt wird immer automatisch als Upsell-Produkt für alle untergeordneten Produkte angezeigt.

## Cross-Sells

Cross-Sell-Artikel ähneln Impulskäufen, die in der Checkout-Zeile neben dem Kassenregister platziert werden. Produkte, die als Crosssell angeboten werden, erscheinen auf der Warenkorbseite, kurz bevor der Kunde mit dem Checkout-Prozess beginnt.

>[!NOTE]
>
>Um Querverkaufselemente pro Store-Ansicht anzuzeigen oder auszublenden, sehen Sie sich die Option [Checkout > Warenkorb](../configuration-reference/sales/checkout.md) mit der Bezeichnung _[!UICONTROL Show Cross-sell Items]_im Warenkorb an. Sie können Querverkäufe während bestimmter Verkäufe oder für A/B-Tests in einer Store-Ansicht ausblenden.

![Querverkäufe im Warenkorb](./assets/storefront-cart-cross-sells.png){width="600" zoomable="yes"}

**_So wählen Sie Crosssell-Produkte aus:_**

1. Öffnen Sie das Produkt im Bearbeitungsmodus.

1. Scrollen Sie nach unten und erweitern Sie den Abschnitt **[!UICONTROL Related Products, Up-Sells, and Cross-Sells]** um den ![Erweiterungsselektor](../assets/icon-display-expand.png).

1. Klicken Sie auf **[!UICONTROL Add Cross-Sell Products]**.

1. Verwenden Sie die [Filtersteuerelemente](../getting-started/admin-grid-controls.md), um die gewünschten Produkte zu finden.

1. Aktivieren Sie in der Liste das Kontrollkästchen jedes Produkts, das Sie als Crosssell-Produkt verwenden möchten.

   ![Cross-Sell-Produkte](./assets/product-cross-sell-add.png){width="600" zoomable="yes"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Add Selected Products]**.
