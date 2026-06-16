---
title: Nachnahme (Nachnahme)
description: Erfahren Sie, wie Sie Cash on Delivery als Offline-Zahlungsmethode in Ihrem Geschäft einrichten.
exl-id: dcf94734-a66e-4d32-b389-b47c979ceaa9
feature: Payments
TQID: https://experienceleague.adobe.com/xKFjuGpjrF-XfVnNqWR2St8v3D4Lnr74WozkrynBbdo
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 336
ht-degree: 0%

---

# Nachnahme (Nachnahme)

Adobe Commerce und Magento Open Source ermöglichen es Ihnen, _(Nachnahme_ (Nachnahme) für Käufe zu akzeptieren. Sie können die Zahlung per Nachnahme nur aus bestimmten Ländern akzeptieren. Außerdem können Sie die Konfiguration mit Mindest- und Höchstbestellmengen anpassen.

Der Spediteur erhält die Zahlung vom Kunden zum Zeitpunkt der Lieferung, die dann an Sie überwiesen wird. Sie können eine Berichtigung für alle Gebühren vornehmen, die der Spediteurdienst in Ihren Versand- und Bearbeitungsgebühren erhebt.

**_So richten Sie Nachnahmenzahlungen ein:_**

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Payment Methods]**.

1. Erweitern _unter „Andere_&quot; den ![Erweiterungsselektor](../assets/icon-display-expand.png) im **[!UICONTROL Cash On Delivery Payment]**.

   ![Nachnahme](../configuration-reference/sales/assets/payment-methods-cash-on-delivery-payment.png){width="600" zoomable="yes"}

   Eine ausführliche Beschreibung jeder dieser Konfigurationseinstellungen finden Sie unter [Barzahlung bei Versand](../configuration-reference/sales/payment-methods.md#cash-on-delivery-payment) im _Konfigurationshandbuch_.

   >[!NOTE]
   >
   >Deaktivieren Sie bei Bedarf zunächst das Kontrollkästchen **[!UICONTROL Use system value]** , um diese Einstellungen zu ändern.

1. Um Barzahlung bei Versand zu aktivieren, setzen Sie **[!UICONTROL Enabled]** auf `Yes`.

1. Geben Sie **[!UICONTROL Title]** einen Titel ein, der die Nachnahmenzahlungsmethode beim Checkout angibt.

1. Setzen Sie **[!UICONTROL New Order Status]** auf `Pending`, bis der Zahlungseingang bestätigt wird.

   Wenn Sie es vorziehen, können Sie den `Processing`- oder `Suspected Fraud` für neue Bestellungen mit dieser Zahlungsmethode verwenden.

1. Legen Sie **[!UICONTROL Payment from Applicable Countries]** auf eine der folgenden Einstellungen fest:

   - `All Allowed Countries` - Kunden aus allen [Ländern](../getting-started/store-details.md#country-options) die in Ihrer Store-Konfiguration angegeben sind, können diese Zahlungsmethode verwenden.
   - `Specific Countries` - Nachdem Sie diese Option ausgewählt haben, wird die _[!UICONTROL Payment from Specific Countries]_&#x200B;angezeigt. Zur Auswahl mehrerer Länder halten Sie die Strg-Taste (PC) bzw. die Befehlstaste (Mac) gedrückt und klicken auf die einzelnen Optionen.

1. Geben Sie die **[!UICONTROL Instructions]** für die Annahme eines Nachnahmenauftrags ein.

1. Legen Sie **[!UICONTROL Minimum Order Total]** und **[!UICONTROL Maximum Order Total]** auf die Bestellbeträge fest, die für die Zahlung per Nachnahme erforderlich sind.

   >[!NOTE]
   >
   >Eine Bestellung ist dann geeignet, wenn die Gesamtsumme zwischen der Mindest- oder Höchstauftragssumme liegt oder mit dieser übereinstimmt.

1. Geben Sie **[!UICONTROL Sort Order]** eine Zahl ein, die die Position dieses Artikels in der Liste der Zahlungsmethoden bestimmt, die beim Checkout angezeigt wird.

   Diese Zahl steht im Verhältnis zu den anderen Zahlungsmethoden. (`0` = First, `1` = Second, `2` = Third usw.)

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.
