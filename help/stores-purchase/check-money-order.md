---
title: Schecks und Zahlungsanweisungen
description: Erfahren Sie, wie Sie Schecks und Zahlungsanweisungen als Offline-Zahlungsmethode in Ihrem Geschäft einrichten.
exl-id: e004f0c3-f659-4b08-a41a-88bfc05acaab
feature: Payments
TQID: https://experienceleague.adobe.com/mmlEdLGANV93nvet3YwYoBGZKcft1qYuA6HboQ0Buvw
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 337
ht-degree: 0%

---

# Schecks und Zahlungsanweisungen

Mit Adobe Commerce und Magento Open Source können Sie Zahlungen per Scheck oder Zahlungsanweisung akzeptieren. Die Zahlungsmethode _Scheck /_) ist für Ihren Shop standardmäßig aktiviert. Sie können Schecks und Zahlungsanweisungen nur aus bestimmten Ländern annehmen und die Konfiguration mit Mindest- und Höchstauftragssummen optimieren.

**_So konfigurieren Sie die Zahlung per Scheck oder Zahlungsanweisung:_**

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Payment Methods]**.

1. Erweitern Sie unter _[!UICONTROL Other Payment Methods]_![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Check / Money Order]**.

   ![Scheck/Zahlungsanweisung](../configuration-reference/sales/assets/payment-methods-check-money-order.png){width="600" zoomable="yes"}

   Eine ausführliche Beschreibung jeder dieser Konfigurationseinstellungen finden Sie unter [Scheck/](../configuration-reference/sales/payment-methods.md#check--money-order) im _Konfigurationsreferenzhandbuch_.

   >[!NOTE]
   >
   >Deaktivieren Sie bei Bedarf zunächst das Kontrollkästchen **[!UICONTROL Use system value]** , um diese Einstellungen zu ändern.

1. Um die Zahlung per Scheck oder Zahlungsanweisung zu akzeptieren, setzen Sie **[!UICONTROL Enabled]** auf `Yes`.

1. Geben Sie **[!UICONTROL Title]** einen Titel ein, der die Zahlungsmethode Scheck/Geldanweisung während des Checkouts angibt.

1. Wenn Bestellungen in der Regel auf die Genehmigung warten, akzeptieren Sie die **[!UICONTROL New Order Status]** als `Pending"`, bis sie genehmigt wird.

   Wenn Sie es vorziehen, können Sie den `Processing`- oder `Suspected Fraud` für neue Bestellungen mit dieser Zahlungsmethode verwenden.

1. Legen Sie **[!UICONTROL Payment from Applicable Countries]** auf eine der folgenden Einstellungen fest:

   - `All Allowed Countries` - Kunden aus allen [Ländern](../getting-started/store-details.md#country-options) die in Ihrer Store-Konfiguration angegeben sind, können diese Zahlungsmethode verwenden.
   - `Specific Countries` - Nachdem Sie diese Option ausgewählt haben, wird die _[!UICONTROL Payment from Specific Countries]_angezeigt. Zur Auswahl mehrerer Länder halten Sie die Strg-Taste (PC) bzw. die Befehlstaste (Mac) gedrückt und klicken auf die einzelnen Optionen.

1. Geben Sie **[!UICONTROL Make Check Payable To]** den Namen der Partei ein, an die der Scheck auszustellen ist.

1. Geben Sie **[!UICONTROL Send Check To]** die Straße oder das Postfach ein, an die bzw. das die Schecks gesendet werden.

1. Legen Sie **[!UICONTROL Minimum Order Total]** und **[!UICONTROL Maximum Order Total]** auf die Bestellbeträge fest, die für diese Zahlungsmethode erforderlich sind.

   >[!NOTE]
   >
   >Eine Bestellung ist dann geeignet, wenn die Summe zwischen den minimalen oder maximalen Gesamtwerten liegt oder genau mit diesen übereinstimmt.

1. Geben Sie **[!UICONTROL Sort Order]** eine Zahl ein, die die Position dieses Artikels in der Liste der Zahlungsmethoden bestimmt, die beim Checkout angezeigt wird.

   Diese Zahl steht im Verhältnis zu den anderen Zahlungsmethoden. (`0` = First, `1` = Second, `2` = Third usw.)

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.
