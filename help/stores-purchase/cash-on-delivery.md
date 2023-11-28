---
title: Nachnahme (COD)
description: Erfahren Sie, wie Sie Bargeld bei der Lieferung als Offline-Zahlungsmethode in Ihrem Geschäft einrichten.
exl-id: dcf94734-a66e-4d32-b389-b47c979ceaa9
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# Nachnahme (COD)

Mit Adobe Commerce und Magento Open Source können Sie _Zustellbar_ (COD) Zahlungen für Käufe. Sie können CSB-Zahlungen nur aus bestimmten Ländern akzeptieren und die Konfiguration mit Mindest- und Höchstbestellsummen anpassen.

Der Lieferant erhält die Zahlung vom Kunden zum Zeitpunkt der Lieferung, die dann auf Sie übertragen wird. Sie können eine Anpassung für alle Gebühren vornehmen, die vom Beförderungsdienst in Ihren Versand- und Bearbeitungsgebühren erhoben werden.

**_So richten Sie Barzahlungen bei der Lieferung ein:_**

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen **[!UICONTROL Payment Methods]**.

1. under _Andere Zahlungsmethoden_, erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Cash On Delivery Payment]** Abschnitt.

   ![Bargeld bei der Auslieferung](../configuration-reference/sales/assets/payment-methods-cash-on-delivery-payment.png){width="600" zoomable="yes"}

   Eine ausführliche Beschreibung der einzelnen Konfigurationseinstellungen finden Sie unter [Barzahlung bei Lieferung](../configuration-reference/sales/payment-methods.md#cash-on-delivery-payment) im _Konfigurationshandbuch_.

   >[!NOTE]
   >
   >Bei Bedarf muss zunächst die **[!UICONTROL Use system value]** aktivieren, um diese Einstellungen zu ändern.

1. So aktivieren Sie die Barzahlung bei der Lieferung **[!UICONTROL Enabled]** nach `Yes`.

1. Für **[!UICONTROL Title]**, geben Sie einen Titel ein, der die CSB-Zahlungsmethode beim Checkout angibt.

1. Satz **[!UICONTROL New Order Status]** nach `Pending` bis der Eingang der Zahlung bestätigt wird.

   Wenn Sie es bevorzugen, können Sie die `Processing` oder `Suspected Fraud` Status für neue Bestellungen mit dieser Zahlungsmethode.

1. Satz **[!UICONTROL Payment from Applicable Countries]** auf einen der folgenden Werte zu:

   - `All Allowed Countries` - Kunden von allen [Länder](../getting-started/store-details.md#country-options) Diese Zahlungsmethode kann in Ihrer Store-Konfiguration verwendet werden.
   - `Specific Countries` - Wenn Sie diese Option ausgewählt haben, wird die _[!UICONTROL Payment from Specific Countries]_angezeigt. Um mehrere Länder auszuwählen, halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie auf jede Option.

1. Geben Sie die **[!UICONTROL Instructions]** für die Annahme einer Nachbestellung.

1. Satz **[!UICONTROL Minimum Order Total]** und **[!UICONTROL Maximum Order Total]** auf die Bestellbeträge, die für die CSB-Zahlung infrage kommen.

   >[!NOTE]
   >
   >Eine Bestellung qualifiziert sich, wenn die Gesamtsumme zwischen der minimalen oder der maximalen Bestellsumme liegt oder damit übereinstimmt.

1. Für **[!UICONTROL Sort Order]** eingeben, geben Sie eine Zahl ein, die die Position dieses Elements in der Liste der Zahlungsmethoden bestimmt, die beim Checkout angezeigt werden.

   Diese Zahl ist relativ zu den anderen Zahlungsmethoden. (`0` = first, `1` = Sekunde, `2` = drittes Element usw.)

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.
