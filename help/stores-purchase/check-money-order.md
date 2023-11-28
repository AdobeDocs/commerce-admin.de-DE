---
title: Schecks und Geldaufträge
description: Erfahren Sie, wie Sie Scheck- und Geldbestellungen als Offline-Zahlungsmethode in Ihrem Geschäft einrichten.
exl-id: e004f0c3-f659-4b08-a41a-88bfc05acaab
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# Schecks und Geldaufträge

Mit Adobe Commerce und Magento Open Source können Sie Zahlungen per Scheck oder per Überweisung annehmen. Die _Überprüfen/Monatsbestellung_ Die Zahlungsmethode ist für Ihren Store standardmäßig aktiviert. Sie können Schecks und Geldbestellungen nur aus bestimmten Ländern akzeptieren und die Konfiguration mit Mindest- und Höchstbestellsummen anpassen.

**_So konfigurieren Sie die Zahlung per Scheck oder Geldauftrag:_**

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen **[!UICONTROL Payment Methods]**.

1. under _[!UICONTROL Other Payment Methods]_, erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Check / Money Order]**Abschnitt.

   ![Überprüfen/Monatsbestellung](../configuration-reference/sales/assets/payment-methods-check-money-order.png){width="600" zoomable="yes"}

   Eine ausführliche Beschreibung der einzelnen Konfigurationseinstellungen finden Sie unter [Überprüfen/Monatsbestellung](../configuration-reference/sales/payment-methods.md#check--money-order) im _Konfigurationshandbuch_.

   >[!NOTE]
   >
   >Bei Bedarf muss zunächst die **[!UICONTROL Use system value]** aktivieren, um diese Einstellungen zu ändern.

1. Um die Zahlung per Scheck oder Zahlungsauftrag zu akzeptieren, setzen Sie **[!UICONTROL Enabled]** nach `Yes`.

1. Für **[!UICONTROL Title]**, geben Sie einen Titel ein, der die Zahlungsmethode für Scheck-/Geldbestellungen während des Checkouts identifiziert.

1. Wenn Bestellungen in der Regel auf die Validierung warten, akzeptieren Sie die Standardeinstellung **[!UICONTROL New Order Status]** as `Pending"` bis zur Genehmigung.

   Wenn Sie es bevorzugen, können Sie die `Processing` oder `Suspected Fraud` Status für neue Bestellungen mit dieser Zahlungsmethode.

1. Satz **[!UICONTROL Payment from Applicable Countries]** auf einen der folgenden Werte zu:

   - `All Allowed Countries` - Kunden von allen [Länder](../getting-started/store-details.md#country-options) Diese Zahlungsmethode kann in Ihrer Store-Konfiguration verwendet werden.
   - `Specific Countries` - Wenn Sie diese Option ausgewählt haben, wird die _[!UICONTROL Payment from Specific Countries]_angezeigt. Um mehrere Länder auszuwählen, halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie auf jede Option.

1. Für **[!UICONTROL Make Check Payable To]** den Namen der Partei, an die die Scheck zu zahlen ist.

1. Für **[!UICONTROL Send Check To]**, geben Sie die Straße oder das Postfach ein, an das die Schecks versandt werden.

1. Satz **[!UICONTROL Minimum Order Total]** und **[!UICONTROL Maximum Order Total]** auf die Bestellbeträge, die für diese Zahlungsmethode erforderlich sind.

   >[!NOTE]
   >
   >Eine Bestellung qualifiziert sich, wenn der Gesamtwert zwischen den minimalen oder maximalen Gesamtwerten liegt oder genau damit übereinstimmt.

1. Für **[!UICONTROL Sort Order]** eingeben, geben Sie eine Zahl ein, die die Position dieses Elements in der Liste der Zahlungsmethoden bestimmt, die beim Checkout angezeigt werden.

   Diese Zahl ist relativ zu den anderen Zahlungsmethoden. (`0` = first, `1` = Sekunde, `2` = drittes Element usw.)

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.
