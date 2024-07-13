---
title: Banküberweisungen
description: Erfahren Sie, wie Sie Banküberweisungen als Offline-Zahlungsmethode für Ihr Geschäft einrichten.
exl-id: 34b2163c-2edd-4741-b002-3d8fb561fc78
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 0%

---

# Banküberweisungen

Mit Adobe Commerce und Magento Open Source können Sie Zahlungen akzeptieren, die von einem Kundenkonto überwiesen und auf Ihrem Händlerkonto eingezahlt werden.

**_So konfigurieren Sie Überweisungszahlungen:_**

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Payment Methods]** aus.

1. Erweitern Sie unter _Andere Zahlungsmethoden_ den Abschnitt ![Erweiterungsauswahl](../assets/icon-display-expand.png) des Abschnitts **[!UICONTROL Bank Transfer Payment]**.

   ![Überweisungszahlung ](../configuration-reference/sales/assets/payment-methods-bank-transfer-payment.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Deaktivieren Sie bei Bedarf zunächst das Kontrollkästchen **[!UICONTROL Use system value]** , um diese Einstellungen zu ändern.

1. Um Banküberweisungen zu aktivieren, setzen Sie **[!UICONTROL Enabled]** auf `Yes`.

1. Geben Sie für &quot;**[!UICONTROL Title]**&quot;einen Titel ein, der die Methode zur Überweisung von Bankguthaben beim Checkout angibt.

1. Setzen Sie **[!UICONTROL New Order Status]** auf `Pending`, bis die Zahlung genehmigt ist.

1. Setzen Sie **[!UICONTROL Payment from Applicable Countries]** auf einen der folgenden Werte:

   - `All Allowed Countries` - Kunden aus allen in Ihrer Store-Konfiguration angegebenen [Ländern](../getting-started/store-details.md#country-options) können diese Zahlungsmethode verwenden.

   - `Specific Countries` - Nachdem Sie diese Option ausgewählt haben, wird die Liste _[!UICONTROL Payment from Specific Countries]_angezeigt. Um mehrere Länder auszuwählen, halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie auf jede Option.

1. Geben Sie die **[!UICONTROL Instructions]** ein, die Ihre Kunden befolgen müssen, um eine Überweisung einzurichten.

   Je nach dem Land, in dem Ihre Bank ansässig ist, und den Anforderungen der Bank können Sie die folgenden Informationen angeben:

   - Name des Bankkontos
   - Kontonummer
   - Bank-Routing-Code
   - Name der Bank
   - Zweigstelle

1. Setzen Sie **[!UICONTROL Minimum Order Total]** und **[!UICONTROL Maximum Order Total]** auf die Beträge, die erforderlich sind, um sich für die Verwendung dieser Zahlungsmethode zu qualifizieren.

   >[!NOTE]
   >
   >Eine Bestellung qualifiziert sich, wenn der Gesamtwert zwischen den minimalen oder maximalen Gesamtwerten liegt oder genau damit übereinstimmt.

1. Geben Sie für **[!UICONTROL Sort Order]** eine Zahl ein, die die Position dieses Elements in der Liste der Zahlungsmethoden bestimmt, die beim Checkout angezeigt werden.

   Diese Zahl ist relativ zu den anderen Zahlungsmethoden. (`0` = first, `1` = second, `2` = third usw.)

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.
