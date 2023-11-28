---
title: Null subtotal-Checkout
description: Erfahren Sie, wie Sie eine Null-Zwischensumme als Offline-Zahlungsmethode für Ihren Store einrichten.
exl-id: c14ce289-8292-41d9-a448-f493c784f35c
feature: Checkout, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# Null subtotal-Checkout

_Null subtotal-Checkout_ kann für Bestellungen mit einer Zwischensumme von null verwendet werden, die besteuert werden, nachdem ein Rabatt angewendet wurde. Beispielsweise kann der Checkout mit einer Zwischensumme von null in folgenden Situationen verwendet werden:

- Ein Rabatt deckt den gesamten Kaufpreis ohne zusätzliche Versandkosten ab.

- Der Kunde fügt eine [herunterladbar](../catalog/product-create-downloadable.md) oder [virtual](../catalog/product-create-virtual.md) Produkt in den Warenkorb, und der Preis entspricht null.

- Der Preis eines [einfach](../catalog/product-create-simple.md) -Produkt null ist und die [kostenloser Versand](shipping-free.md) -Methode verfügbar ist.

- A [Coupon-Code](../merchandising-promotions/price-rules-cart-coupon.md) deckt den vollen Preis der Produkte und des Versands ab.

Um Zeit zu sparen, können keine Teilsummenbestellungen auf die automatische Rechnung gesetzt werden.

**_So konfigurieren Sie die Checkout-Funktion für die Zwischensumme null:_**

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen **[!UICONTROL Payment Methods]**.

1. under _[!UICONTROL Other Payment Methods]_, erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Zero Subtotal Checkout]**Abschnitt.

   ![Null Zwischensumme Checkout](../configuration-reference/sales/assets/payment-methods-zero-subtotal-checkout.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Bei Bedarf muss zunächst die **[!UICONTROL Use system value]** aktivieren, um diese Einstellungen zu ändern.

1. Um den Ausschluss ohne Zwischensumme zu aktivieren, legen Sie **[!UICONTROL Enabled]** nach `Yes`.

1. Für **[!UICONTROL Title]** Geben Sie einen Titel ein, der die Null-Zwischensummen-Methode beim Checkout angibt.

1. Wenn Bestellungen in der Regel auf die Validierung warten, akzeptieren Sie die Standardeinstellung **[!UICONTROL New Order Status]** as `Pending"` bis die Bestellung validiert wurde.

   Wenn Sie es bevorzugen, können Sie die `Processing` oder `Suspected Fraud` Status für neue Bestellungen mit dieser Zahlungsmethode.

1. Satz **[!UICONTROL Automatically Invoice All Items]** nach `Yes` wenn Sie automatisch alle Artikel mit Nullsaldo berechnen möchten.

   Diese Option ist nur verfügbar, wenn die Variable **[!UICONTROL New Order Status]** ist auf `Processing`.

   >[!NOTE]
   >
   >Wenn _[!UICONTROL New Order Status]_auf `Processing` und_[!UICONTROL Automatically Invoice All Items]_ auf `No`, müssen Sie **[!UICONTROL Order Status]** = `Processing` für die **[!UICONTROL Order State]** = `Pending` und **[!UICONTROL Default Status]** = `No` -Zuordnung auf der [Bestellstatus](order-status.md#custom-order-status) Seite.

1. Satz **[!UICONTROL Payment from Applicable Countries]** auf einen der folgenden Werte zu:

   - `All Allowed Countries` - Kunden von allen [Länder](../getting-started/store-details.md#country-options) Diese Zahlungsmethode kann in Ihrer Store-Konfiguration verwendet werden.
   - `Specific Countries` - Wenn Sie diese Option ausgewählt haben, wird die _[!UICONTROL Payment from Specific Countries]_angezeigt. Um mehrere Länder auszuwählen, halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie auf jede Option.

1. Für **[!UICONTROL Sort Order]** eingeben, geben Sie eine Zahl ein, die die Position dieses Elements in der Liste der Zahlungsmethoden bestimmt, die beim Checkout angezeigt werden.

   Diese Zahl ist relativ zu den anderen Zahlungsmethoden. (`0` = first, `1` = Sekunde, `2` = drittes Element usw.)

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.
