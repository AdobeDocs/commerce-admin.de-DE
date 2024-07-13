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

Der Checkout-Vorgang mit der Zwischensumme _kann für Bestellungen mit einer Zwischensumme von null verwendet werden, die besteuert werden, nachdem ein Rabatt angewendet wurde._ Beispielsweise kann der Checkout mit einer Zwischensumme von null in folgenden Situationen verwendet werden:

- Ein Rabatt deckt den gesamten Kaufpreis ohne zusätzliche Versandkosten ab.

- Der Kunde fügt dem Warenkorb ein [herunterladbares](../catalog/product-create-downloadable.md) - oder [virtuelles](../catalog/product-create-virtual.md) -Produkt hinzu und der Preis entspricht null.

- Der Preis eines [einfachen](../catalog/product-create-simple.md) -Produkts ist null, und die Methode [kostenloser Versand](shipping-free.md) ist verfügbar.

- Ein [Couponcode](../merchandising-promotions/price-rules-cart-coupon.md) deckt den vollen Preis der Produkte und der Lieferung ab.

Um Zeit zu sparen, können keine Teilsummenbestellungen auf die automatische Rechnung gesetzt werden.

**_So konfigurieren Sie den Checkout für die Zwischensumme null:_**

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Payment Methods]** aus.

1. Erweitern Sie unter _[!UICONTROL Other Payment Methods]_den Abschnitt ![Erweiterungsauswahl](../assets/icon-display-expand.png) um den Abschnitt **[!UICONTROL Zero Subtotal Checkout]**.

   ![Null Zwischensumme Checkout](../configuration-reference/sales/assets/payment-methods-zero-subtotal-checkout.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Deaktivieren Sie bei Bedarf zunächst das Kontrollkästchen **[!UICONTROL Use system value]** , um diese Einstellungen zu ändern.

1. Setzen Sie **[!UICONTROL Enabled]** auf `Yes`, um die Zwischensumme des Auscheckens auf null zu aktivieren.

1. Geben Sie für &quot;**[!UICONTROL Title]**&quot;einen Titel ein, der die Null-Zwischensumme-Methode beim Checkout angibt.

1. Wenn Bestellungen in der Regel auf die Genehmigung warten, akzeptieren Sie den Standardwert **[!UICONTROL New Order Status]** als `Pending"`, bis die Bestellung validiert wurde.

   Wenn Sie es bevorzugen, können Sie den Status `Processing` oder `Suspected Fraud` für neue Bestellungen mit dieser Zahlungsmethode verwenden.

1. Setzen Sie **[!UICONTROL Automatically Invoice All Items]** auf `Yes` , wenn Sie automatisch alle Artikel in Rechnung stellen möchten, die einen Nullsaldo aufweisen.

   Diese Option ist nur verfügbar, wenn die **[!UICONTROL New Order Status]** -Option auf `Processing` gesetzt ist.

   >[!NOTE]
   >
   >Wenn _[!UICONTROL New Order Status]_auf `Processing` und_[!UICONTROL Automatically Invoice All Items]_ auf `No` gesetzt ist, müssen Sie auch **[!UICONTROL Order Status]** = `Processing` für die Zuordnung **[!UICONTROL Order State]** = `Pending` und **[!UICONTROL Default Status]** = `No` auf der Seite [Bestellstatus](order-status.md#custom-order-status) zuweisen.

1. Setzen Sie **[!UICONTROL Payment from Applicable Countries]** auf einen der folgenden Werte:

   - `All Allowed Countries` - Kunden aus allen in Ihrer Store-Konfiguration angegebenen [Ländern](../getting-started/store-details.md#country-options) können diese Zahlungsmethode verwenden.
   - `Specific Countries` - Nachdem Sie diese Option ausgewählt haben, wird die Liste _[!UICONTROL Payment from Specific Countries]_angezeigt. Um mehrere Länder auszuwählen, halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie auf jede Option.

1. Geben Sie für **[!UICONTROL Sort Order]** eine Zahl ein, die die Position dieses Elements in der Liste der Zahlungsmethoden bestimmt, die beim Checkout angezeigt werden.

   Diese Zahl ist relativ zu den anderen Zahlungsmethoden. (`0` = first, `1` = second, `2` = third usw.)

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.
