---
title: Kein Zwischensummen-Checkout
description: Erfahren Sie, wie Sie eine Null-Zwischensumme als Offline-Zahlungsmethode in Ihrem Geschäft einrichten.
exl-id: c14ce289-8292-41d9-a448-f493c784f35c
feature: Checkout, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# Kein Zwischensummen-Checkout

_Kasse mit Zwischensumme Null_ kann für Bestellungen mit einer Zwischensumme von null verwendet werden, die nach Anwendung eines Rabatts besteuert werden. In folgenden Situationen kann beispielsweise ein Checkout mit einem Zwischensummenwert von null verwendet werden:

- Ein Rabatt deckt den gesamten Kaufpreis ab, ohne zusätzliche Versandkosten.

- Der Kunde fügt ein [herunterladbares](../catalog/product-create-downloadable.md) oder [virtuelles](../catalog/product-create-virtual.md) Produkt zum Warenkorb hinzu, und der Preis ist null.

- Der Preis für ein [einfaches](../catalog/product-create-simple.md) Produkt ist null, und die [kostenloser Versand](shipping-free.md)-Methode ist verfügbar.

- Ein [Gutscheincode](../merchandising-promotions/price-rules-cart-coupon.md) deckt den vollen Preis der Produkte und den Versand ab.

Um Zeit zu sparen, können Null Zwischensummen für Bestellungen auf die automatische Fakturierung eingestellt werden.

**_So konfigurieren Sie einen Null-Zwischensumme-Checkout:_**

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Payment Methods]**.

1. Erweitern Sie unter _[!UICONTROL Other Payment Methods]_![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Zero Subtotal Checkout]**.

   ![Null Zwischensumme Checkout](../configuration-reference/sales/assets/payment-methods-zero-subtotal-checkout.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Deaktivieren Sie bei Bedarf zunächst das Kontrollkästchen **[!UICONTROL Use system value]** , um diese Einstellungen zu ändern.

1. Um einen Null-Zwischensumme-Checkout zu aktivieren, setzen Sie **[!UICONTROL Enabled]** auf `Yes`.

1. Geben Sie **[!UICONTROL Title]** einen Titel ein, der die Methode Null-Zwischensumme beim Checkout angibt.

1. Wenn Bestellungen in der Regel auf die Genehmigung warten, akzeptieren Sie die **[!UICONTROL New Order Status]** als `Pending"`, bis die Bestellung genehmigt wird.

   Wenn Sie es vorziehen, können Sie den `Processing`- oder `Suspected Fraud` für neue Bestellungen mit dieser Zahlungsmethode verwenden.

1. Setzen Sie **[!UICONTROL Automatically Invoice All Items]** auf `Yes`, wenn Sie alle Artikel mit einem Nullsaldo automatisch fakturieren möchten.

   Diese Option ist nur verfügbar, wenn die Option **[!UICONTROL New Order Status]** auf `Processing` festgelegt ist.

   >[!NOTE]
   >
   >Wenn _[!UICONTROL New Order Status]_&#x200B;auf `Processing` und&#x200B;_[!UICONTROL Automatically Invoice All Items]_ auf `No` gesetzt ist, müssen Sie auch **[!UICONTROL Order Status]** = `Processing` für die **[!UICONTROL Order State]** = `Pending` und **[!UICONTROL Default Status]** = `No` Zuordnung auf der Seite [Bestellstatus](order-status.md#custom-order-status) zuweisen.

1. Legen Sie **[!UICONTROL Payment from Applicable Countries]** auf eine der folgenden Einstellungen fest:

   - `All Allowed Countries` - Kunden aus allen [Ländern](../getting-started/store-details.md#country-options) die in Ihrer Store-Konfiguration angegeben sind, können diese Zahlungsmethode verwenden.
   - `Specific Countries` - Nachdem Sie diese Option ausgewählt haben, wird die _[!UICONTROL Payment from Specific Countries]_&#x200B;angezeigt. Zur Auswahl mehrerer Länder halten Sie die Strg-Taste (PC) bzw. die Befehlstaste (Mac) gedrückt und klicken auf die einzelnen Optionen.

1. Geben Sie **[!UICONTROL Sort Order]** eine Zahl ein, die die Position dieses Artikels in der Liste der Zahlungsmethoden bestimmt, die beim Checkout angezeigt wird.

   Diese Zahl steht im Verhältnis zu den anderen Zahlungsmethoden. (`0` = First, `1` = Second, `2` = Third usw.)

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.
