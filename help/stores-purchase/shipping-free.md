---
title: Kostenloser Versand
description: Erfahren Sie, wie Sie eine kostenlose Versandoption für Ihren Store einrichten.
exl-id: 3ce69583-0f7f-4c23-b3e3-7d2502bc1bca
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 0%

---

# Kostenloser Versand

_Kostenloser Versand_ ist eine der effektivsten Aktionen, die Sie anbieten können. Sie kann auf einem Mindestkauf basieren oder als [Warenkorbpreisregel“ eingerichtet &#x200B;](../merchandising-promotions/price-rules-cart.md), die angewendet wird, wenn eine Reihe von Bedingungen erfüllt ist. Wenn beide für dieselbe Reihenfolge gelten, hat die Konfigurationseinstellung Vorrang vor der Warenkorbregel.

>[!NOTE]
>
>Überprüfen Sie die Konfiguration Ihres Spediteurs auf zusätzliche Einstellungen, die für den kostenlosen Versand erforderlich sein können.

## Schritt 1: Konfigurieren des kostenlosen Versands

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Delivery Methods]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Free Shipping]** .

   >[!NOTE]
   >
   >Deaktivieren Sie bei Bedarf zunächst das Kontrollkästchen **[!UICONTROL Use system value]** , um die folgenden Einstellungen wie beschrieben zu ändern.

1. Legen Sie **[!UICONTROL Enabled]** auf `Yes` fest.

1. Geben Sie **[!UICONTROL Title]** einen Titel, der die kostenlose Versandmethode beim Checkout angibt, und einen **[!UICONTROL Method Name]** ein, um sie zu beschreiben.

1. Geben Sie **[!UICONTROL Minimum Order Amount]** den Mindestgesamtwert ein, der für den kostenlosen Versand qualifiziert ist.

   >[!TIP]
   >
   >Um den kostenlosen Versand mit [Tabellenraten](shipping-table-rate.md) zu verwenden, müssen Sie die _[!UICONTROL Minimum Order Amount]_&#x200B;so hoch gestalten, dass sie nie erfüllt wird. Die Verwendung dieses hohen Werts verhindert, dass der kostenlose Versand in Kraft tritt, es sei denn, er wird durch eine Preisregel ausgelöst.

1. **[!UICONTROL Include Tax to Amount]** festlegen:

   - `Yes` - Enthält Steuer bei der Berechnung des Mindestbestellbetrags (Zwischensumme + Steuer - Rabatt).
   - `No` - Enthält bei der Berechnung des Mindestauftragsbetrags keine Steuer (Zwischensumme - Rabatt).

   ![Kostenloser Versand](../configuration-reference/sales/assets/delivery-methods-free-shipping.png){width="600" zoomable="yes"}

1. Geben Sie **[!UICONTROL Displayed Error Message]** die Nachricht ein, die angezeigt werden soll, wenn der kostenlose Versand nicht mehr verfügbar ist.

1. **[!UICONTROL Ship to Applicable Countries]** festlegen:

   - `All Allowed Countries` - Kunden aus allen [Ländern](../getting-started/store-details.md#country-options) die in Ihrer Store-Konfiguration angegeben sind, können den kostenlosen Versand verwenden.

   - `Specific Countries` - Nachdem Sie diesen Wert ausgewählt haben, wird die _[!UICONTROL Ship to Specific Countries]_&#x200B;angezeigt. Wählen Sie jedes Land in der Liste aus, in dem der kostenlose Versand verwendet werden kann.

1. **[!UICONTROL Show Method if Not Applicable]** festlegen:

   - `Yes` - Zeigt immer die kostenlose Versandmethode an, auch wenn sie nicht anwendbar ist.
   - `No` - Zeigt die kostenlose Versandmethode nur an, wenn zutreffend.

1. Geben Sie **[!UICONTROL Sort Order]** die Nummer ein, die die Position des kostenlosen Versands während des Checkouts in der Liste der Versandmethoden bestimmt.

   `0` = First, `1` = Second, `2` = Third usw.

1. Klicken Sie auf **[!UICONTROL Save Config]**.

## Schritt 2: Freien Versand in der Provider-Konfiguration aktivieren

Stellen Sie sicher, dass Sie alle Konfigurationen durchführen, die für jeden Spediteur erforderlich sind, den Sie für den kostenlosen Versand verwenden möchten. Wenn Ihre [UPS-Konfiguration](ups.md) ansonsten vollständig ist, aktualisieren Sie die folgenden Einstellungen, um den kostenlosen Versand zu aktivieren und zu konfigurieren.

1. Erweitern Sie in der _[!UICONTROL Delivery Methods]_-Konfiguration ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL UPS]**.

1. Legen Sie **[!UICONTROL Free Method]** auf `UPS Ground` oder einen anderen Typ fest, den Sie für den kostenlosen Versand angeben möchten.

1. Um eine Mindestbestellung für den kostenlosen Versand zu verlangen, setzen Sie **[!UICONTROL Enable Free Shipping Threshold]** auf `Enable`.

   Wenn Sie eine Mindestbestellung verwenden möchten, geben Sie den erforderlichen Betrag für die **[!UICONTROL Free Shipping Amount Threshold]** ein.

1. Klicken Sie auf **[!UICONTROL Save Config]**.
