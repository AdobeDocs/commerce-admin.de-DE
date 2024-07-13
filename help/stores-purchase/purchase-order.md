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

Eine _Bestellung_ (PO) ermöglicht es kommerziellen Kunden, für autorisierte Käufe zu zahlen, indem sie auf die Bestellnummer verweisen. Die Bestellung wird im Voraus von der Firma, die den Kauf tätigt, genehmigt und ausgestellt. Beim Checkout wählt der Kunde Bestellung als Zahlungsmethode aus. Nach Eingang Ihrer Rechnung bearbeitet das Unternehmen die Zahlung in seinem zahlbaren System und zahlt für den Kauf.

Vor Annahme der Zahlung durch den Kaufauftrag ist stets die Kreditwürdigkeit des kommerziellen Kunden zu ermitteln.

**_So konfigurieren Sie die Zahlung nach Bestellung:_**

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Payment Methods]** aus.

1. Erweitern Sie unter _[!UICONTROL Other Payment Methods]_den Abschnitt ![Erweiterungsauswahl](../assets/icon-display-expand.png) um den Abschnitt **[!UICONTROL Purchase Order]**.

   ![Bestellung](../configuration-reference/sales/assets/payment-methods-purchase-order.png){width="600" zoomable="yes"}

   Eine ausführliche Beschreibung der einzelnen Konfigurationseinstellungen finden Sie unter [Bestellung](../configuration-reference/sales/payment-methods.md#purchase-order) im _Konfigurationshandbuch_.

   >[!NOTE]
   >
   >Deaktivieren Sie bei Bedarf zunächst das Kontrollkästchen **[!UICONTROL Use system value]** , um diese Einstellungen zu ändern.

1. Um diese Zahlungsmethode zu aktivieren, setzen Sie **[!UICONTROL Enabled]** auf `Yes`.

1. Geben Sie für **[!UICONTROL Title]** einen Titel ein, der diese Zahlungsmethode beim Checkout angibt.

1. Setzen Sie **[!UICONTROL New Order Status]** auf `Pending`, bis die Zahlung genehmigt ist.

1. Setzen Sie **[!UICONTROL Payment from Applicable Countries]** auf einen der folgenden Werte:

   - `All Allowed Countries` - Kunden aus allen in Ihrer Store-Konfiguration angegebenen [Ländern](../getting-started/store-details.md#country-options) können diese Zahlungsmethode verwenden.
   - `Specific Countries` - Nachdem Sie diese Option ausgewählt haben, wird die Liste _[!UICONTROL Payment from Specific Countries]_angezeigt. Um mehrere Länder auszuwählen, halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie auf jede Option.

1. Setzen Sie **[!UICONTROL Minimum Order Total]** und **[!UICONTROL Maximum Order Total]** auf die Beträge, die erforderlich sind, um für diese Zahlungsmethode qualifiziert zu sein.

   >[!NOTE]
   >
   >Eine Bestellung qualifiziert sich, wenn der Gesamtwert zwischen den minimalen oder maximalen Gesamtwerten liegt oder genau damit übereinstimmt.

1. Geben Sie für **[!UICONTROL Sort Order]** eine Zahl ein, die die Position dieses Elements in der Liste der Zahlungsmethoden bestimmt, die beim Checkout angezeigt werden.

   Diese Zahl ist relativ zu den anderen Zahlungsmethoden. (`0` = first, `1` = second, `2` = third usw.)

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.
