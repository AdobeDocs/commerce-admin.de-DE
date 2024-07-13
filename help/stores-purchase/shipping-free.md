---
title: Kostenloser Versand
description: Erfahren Sie, wie Sie eine kostenlose Versandoption für Ihren Shop einrichten.
exl-id: 3ce69583-0f7f-4c23-b3e3-7d2502bc1bca
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 0%

---

# Kostenloser Versand

_Kostenloser Versand_ ist eine der effektivsten Promotions, die Sie anbieten können. Sie kann auf einem Mindestkauf basieren oder als [Warenkorbpreisregel](../merchandising-promotions/price-rules-cart.md) einrichten, die angewendet wird, wenn eine Reihe von Bedingungen erfüllt ist. Wenn beide auf dieselbe Reihenfolge zutreffen, hat die Konfigurationseinstellung Vorrang vor der Warenkorbregel.

>[!NOTE]
>
>Prüfen Sie die Konfiguration Ihres Versandnetzbetreibers auf zusätzliche Einstellungen, die für den kostenlosen Versand erforderlich sind.

## Schritt 1: Konfigurieren des kostenlosen Versands

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Delivery Methods]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Free Shipping]** .

   >[!NOTE]
   >
   >Heben Sie bei Bedarf zunächst das Kontrollkästchen **[!UICONTROL Use system value]** auf, um die folgenden Einstellungen wie beschrieben zu ändern.

1. Setzen Sie **[!UICONTROL Enabled]** auf `Yes`.

1. Geben Sie für **[!UICONTROL Title]** einen Titel ein, der die Methode des kostenlosen Versands beim Checkout angibt, und einen **[!UICONTROL Method Name]**, um sie zu beschreiben.

1. Geben Sie für &quot;**[!UICONTROL Minimum Order Amount]**&quot;den Mindestgesamtwert ein, der für den kostenlosen Versand infrage kommt.

   >[!TIP]
   >
   >Um den kostenlosen Versand mit [Tabellenraten](shipping-table-rate.md) zu verwenden, machen Sie die _[!UICONTROL Minimum Order Amount]_so hoch, dass sie nie erfüllt werden. Die Verwendung dieses hohen Werts verhindert, dass der freie Versand in Kraft tritt, es sei denn, er wird durch eine Preisregel ausgelöst.

1. Legen Sie **[!UICONTROL Include Tax to Amount]** fest:

   - `Yes` - Umfasst die Steuer bei der Berechnung des Mindestauftragsbetrags (Zwischensumme + Steuer - Rabatt).
   - `No` - Bei der Berechnung des Mindestauftragsbetrags (Zwischensumme - Rabatt) ist keine Steuer enthalten.

   ![Kostenloser Versand](../configuration-reference/sales/assets/delivery-methods-free-shipping.png){width="600" zoomable="yes"}

1. Geben Sie für **[!UICONTROL Displayed Error Message]** die Meldung ein, die angezeigt werden soll, wenn der kostenlose Versand nicht mehr verfügbar ist.

1. Legen Sie **[!UICONTROL Ship to Applicable Countries]** fest:

   - `All Allowed Countries` - Kunden aus allen in Ihrer Store-Konfiguration angegebenen [Ländern](../getting-started/store-details.md#country-options) können den kostenlosen Versand verwenden.

   - `Specific Countries` - Nach Auswahl dieses Werts wird die Liste _[!UICONTROL Ship to Specific Countries]_angezeigt. Wählen Sie jedes Land in der Liste aus, in dem der kostenlose Versand verwendet werden kann.

1. Legen Sie **[!UICONTROL Show Method if Not Applicable]** fest:

   - `Yes` - Zeigt immer die Methode des kostenlosen Versands an, auch wenn diese nicht anwendbar ist.
   - `No` - Zeigt die Methode des kostenlosen Versands nur an, wenn zutreffend.

1. Geben Sie für &quot;**[!UICONTROL Sort Order]**&quot; die Zahl ein, die die Position des kostenlosen Versands während des Checkout in der Liste der Versandmethoden bestimmt.

   `0` = first, `1` = second, `2` = third usw.

1. Klicken Sie auf **[!UICONTROL Save Config]**.

## Schritt 2: Kostenlosen Versand in der Betreiberkonfiguration aktivieren

Stellen Sie sicher, dass Sie alle Konfigurationen vornehmen, die für jeden Betreiber erforderlich sind, den Sie für den kostenlosen Versand verwenden möchten. Wenn beispielsweise Ihre [UPS-Konfiguration](ups.md) anderweitig abgeschlossen ist, aktualisieren Sie die folgenden Einstellungen, um den kostenlosen Versand zu aktivieren und zu konfigurieren.

1. Erweitern Sie in der _[!UICONTROL Delivery Methods]_-Konfiguration den Abschnitt ![Erweiterungsauswahl](../assets/icon-display-expand.png) für den Abschnitt **[!UICONTROL UPS]**.

1. Setzen Sie **[!UICONTROL Free Method]** auf `UPS Ground` oder einen anderen Typ, den Sie für den kostenlosen Versand festlegen möchten.

1. Um eine Mindestbestellung für den kostenlosen Versand zu verlangen, setzen Sie **[!UICONTROL Enable Free Shipping Threshold]** auf `Enable`.

   Wenn Sie sich für eine Mindestbestellung entscheiden, geben Sie den erforderlichen Betrag für **[!UICONTROL Free Shipping Amount Threshold]** ein.

1. Klicken Sie auf **[!UICONTROL Save Config]**.
