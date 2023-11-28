---
title: Bestellungen
description: Erfahren Sie, wie Sie Bestellungen als Offline-Zahlungsmethode in Ihrem Geschäft einrichten.
exl-id: 493c1b59-2155-449f-a08a-eb1aa2af9b3e
feature: Purchase Orders
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# Bestellungen

A _Bestellauftrag_ (PO) ermöglicht es kommerziellen Kunden, für zugelassene Käufe zu zahlen, indem sie die Bestellnummer angeben. Die Bestellung wird im Voraus von der Firma, die den Kauf tätigt, genehmigt und ausgestellt. Beim Checkout wählt der Kunde Bestellung als Zahlungsmethode aus. Nach Eingang Ihrer Rechnung bearbeitet das Unternehmen die Zahlung in seinem zahlbaren System und zahlt für den Kauf.

Vor Annahme der Zahlung durch den Kaufauftrag ist stets die Kreditwürdigkeit des kommerziellen Kunden zu ermitteln.

**_So konfigurieren Sie die Zahlung nach Bestellung:_**

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen **[!UICONTROL Payment Methods]**.

1. under _[!UICONTROL Other Payment Methods]_, erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Purchase Order]**Abschnitt.

   ![Bestellung](../configuration-reference/sales/assets/payment-methods-purchase-order.png){width="600" zoomable="yes"}

   Eine ausführliche Beschreibung der einzelnen Konfigurationseinstellungen finden Sie unter [Bestellung](../configuration-reference/sales/payment-methods.md#purchase-order) im _Konfigurationshandbuch_.

   >[!NOTE]
   >
   >Bei Bedarf muss zunächst die **[!UICONTROL Use system value]** aktivieren, um diese Einstellungen zu ändern.

1. Um diese Zahlungsmethode zu aktivieren, legen Sie **[!UICONTROL Enabled]** nach `Yes`.

1. Für **[!UICONTROL Title]** Geben Sie einen Titel ein, der diese Zahlungsmethode beim Checkout angibt.

1. Satz **[!UICONTROL New Order Status]** nach `Pending` bis die Zahlung genehmigt ist.

1. Satz **[!UICONTROL Payment from Applicable Countries]** auf einen der folgenden Werte zu:

   - `All Allowed Countries` - Kunden von allen [Länder](../getting-started/store-details.md#country-options) Diese Zahlungsmethode kann in Ihrer Store-Konfiguration verwendet werden.
   - `Specific Countries` - Wenn Sie diese Option ausgewählt haben, wird die _[!UICONTROL Payment from Specific Countries]_angezeigt. Um mehrere Länder auszuwählen, halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie auf jede Option.

1. Satz **[!UICONTROL Minimum Order Total]** und **[!UICONTROL Maximum Order Total]** auf die Beträge, die für diese Zahlungsmethode erforderlich sind.

   >[!NOTE]
   >
   >Eine Bestellung qualifiziert sich, wenn der Gesamtwert zwischen den minimalen oder maximalen Gesamtwerten liegt oder genau damit übereinstimmt.

1. Für **[!UICONTROL Sort Order]** eingeben, geben Sie eine Zahl ein, die die Position dieses Elements in der Liste der Zahlungsmethoden bestimmt, die beim Checkout angezeigt werden.

   Diese Zahl ist relativ zu den anderen Zahlungsmethoden. (`0` = first, `1` = Sekunde, `2` = drittes Element usw.)

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.
