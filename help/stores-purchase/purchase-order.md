---
title: Bestellungen
description: Erfahren Sie, wie Sie Bestellungen als Offline-Zahlungsmethode in Ihrem Geschäft einrichten.
exl-id: 493c1b59-2155-449f-a08a-eb1aa2af9b3e
feature: Purchase Orders
TQID: https://experienceleague.adobe.com/Oc2vdP-OTXwo-6cjKWFj5zPf-QJVvU8aK6OUMPko4eY
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
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
source-wordcount: 296
ht-degree: 0%

---

# Bestellungen

Eine _Bestellung_ (PO) ermöglicht es gewerblichen Kunden, für autorisierte Käufe zu bezahlen, indem sie die Bestellnummer angeben. Die Bestellung wird von dem Unternehmen, das den Kauf tätigt, im Voraus autorisiert und ausgestellt. Beim Checkout wählt der Kunde als Zahlungsmethode die Bestellung. Nach Erhalt Ihrer Rechnung verarbeitet das Unternehmen die Zahlung in seinem Kreditorensystem und bezahlt den Kauf.

Bevor Sie eine Zahlung per Bestellung annehmen, stellen Sie immer die Kreditwürdigkeit des gewerblichen Kunden fest.

**_So konfigurieren Sie die Zahlung nach Bestellung:_**

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Payment Methods]**.

1. Erweitern Sie unter _[!UICONTROL Other Payment Methods]_![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Purchase Order]**.

   ![Bestellung](../configuration-reference/sales/assets/payment-methods-purchase-order.png){width="600" zoomable="yes"}

   Eine ausführliche Beschreibung jeder dieser Konfigurationseinstellungen finden Sie unter [Bestellung](../configuration-reference/sales/payment-methods.md#purchase-order) im _Konfigurationsreferenzhandbuch_.

   >[!NOTE]
   >
   >Deaktivieren Sie bei Bedarf zunächst das Kontrollkästchen **[!UICONTROL Use system value]** , um diese Einstellungen zu ändern.

1. Um diese Zahlungsmethode zu aktivieren, setzen Sie **[!UICONTROL Enabled]** auf `Yes`.

1. Geben Sie **[!UICONTROL Title]** einen Titel ein, der diese Zahlungsmethode beim Checkout identifiziert.

1. Setzen Sie **[!UICONTROL New Order Status]** auf `Pending`, bis die Zahlung autorisiert ist.

1. Legen Sie **[!UICONTROL Payment from Applicable Countries]** auf eine der folgenden Einstellungen fest:

   - `All Allowed Countries` - Kunden aus allen [Ländern](../getting-started/store-details.md#country-options) die in Ihrer Store-Konfiguration angegeben sind, können diese Zahlungsmethode verwenden.
   - `Specific Countries` - Nachdem Sie diese Option ausgewählt haben, wird die _[!UICONTROL Payment from Specific Countries]_&#x200B;angezeigt. Zur Auswahl mehrerer Länder halten Sie die Strg-Taste (PC) bzw. die Befehlstaste (Mac) gedrückt und klicken auf die einzelnen Optionen.

1. Legen Sie **[!UICONTROL Minimum Order Total]** und **[!UICONTROL Maximum Order Total]** auf die Beträge fest, die für diese Zahlungsmethode erforderlich sind.

   >[!NOTE]
   >
   >Eine Bestellung ist dann geeignet, wenn die Summe zwischen den minimalen oder maximalen Gesamtwerten liegt oder genau mit diesen übereinstimmt.

1. Geben Sie **[!UICONTROL Sort Order]** eine Zahl ein, die die Position dieses Artikels in der Liste der Zahlungsmethoden bestimmt, die beim Checkout angezeigt wird.

   Diese Zahl steht im Verhältnis zu den anderen Zahlungsmethoden. (`0` = First, `1` = Second, `2` = Third usw.)

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.
