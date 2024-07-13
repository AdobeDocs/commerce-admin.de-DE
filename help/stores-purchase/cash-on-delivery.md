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

Mit Adobe Commerce und Magento Open Source können Sie bei Einkäufen _Barzahlungen bei Lieferung_ (COD) akzeptieren. Sie können CSB-Zahlungen nur aus bestimmten Ländern akzeptieren und die Konfiguration mit Mindest- und Höchstbestellsummen anpassen.

Der Lieferant erhält die Zahlung vom Kunden zum Zeitpunkt der Lieferung, die dann auf Sie übertragen wird. Sie können eine Anpassung für alle Gebühren vornehmen, die vom Beförderungsdienst in Ihren Versand- und Bearbeitungsgebühren erhoben werden.

**_So richten Sie Bargeld bei den Lieferzahlungen ein:_**

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Payment Methods]** aus.

1. Erweitern Sie unter _Andere Zahlungsmethoden_ den Abschnitt ![Erweiterungsauswahl](../assets/icon-display-expand.png) des Abschnitts **[!UICONTROL Cash On Delivery Payment]**.

   ![Cash on Delivery Payment](../configuration-reference/sales/assets/payment-methods-cash-on-delivery-payment.png){width="600" zoomable="yes"}

   Eine ausführliche Beschreibung der einzelnen Konfigurationseinstellungen finden Sie unter [Cash On Delivery Payment](../configuration-reference/sales/payment-methods.md#cash-on-delivery-payment) im _Konfigurationshandbuch_.

   >[!NOTE]
   >
   >Deaktivieren Sie bei Bedarf zunächst das Kontrollkästchen **[!UICONTROL Use system value]** , um diese Einstellungen zu ändern.

1. Setzen Sie **[!UICONTROL Enabled]** auf `Yes`, um Bargeld bei der Auslieferung zu aktivieren.

1. Geben Sie für **[!UICONTROL Title]** einen Titel ein, der die CSB-Zahlungsmethode beim Checkout angibt.

1. Setzen Sie **[!UICONTROL New Order Status]** auf `Pending`, bis der Zahlungseingang bestätigt ist.

   Wenn Sie es bevorzugen, können Sie den Status `Processing` oder `Suspected Fraud` für neue Bestellungen mit dieser Zahlungsmethode verwenden.

1. Setzen Sie **[!UICONTROL Payment from Applicable Countries]** auf einen der folgenden Werte:

   - `All Allowed Countries` - Kunden aus allen in Ihrer Store-Konfiguration angegebenen [Ländern](../getting-started/store-details.md#country-options) können diese Zahlungsmethode verwenden.
   - `Specific Countries` - Nachdem Sie diese Option ausgewählt haben, wird die Liste _[!UICONTROL Payment from Specific Countries]_angezeigt. Um mehrere Länder auszuwählen, halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie auf jede Option.

1. Geben Sie den Wert **[!UICONTROL Instructions]** für die Annahme einer CSB-Bestellung ein.

1. Setzen Sie **[!UICONTROL Minimum Order Total]** und **[!UICONTROL Maximum Order Total]** auf die Bestellbeträge, die für die CSB-Zahlung erforderlich sind.

   >[!NOTE]
   >
   >Eine Bestellung qualifiziert sich, wenn die Gesamtsumme zwischen der minimalen oder der maximalen Bestellsumme liegt oder damit übereinstimmt.

1. Geben Sie für **[!UICONTROL Sort Order]** eine Zahl ein, die die Position dieses Elements in der Liste der Zahlungsmethoden bestimmt, die beim Checkout angezeigt werden.

   Diese Zahl ist relativ zu den anderen Zahlungsmethoden. (`0` = first, `1` = second, `2` = third usw.)

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.
