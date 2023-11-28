---
title: Versandeinstellungen
description: Erfahren Sie, wie Sie die Versandeinstellungen konfigurieren, die den Ausgangspunkt und die Versandrichtlinie für Ihren Store definieren.
exl-id: 767b3039-39c7-4692-a0a8-a8fde27622cc
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 0%

---

# Versandeinstellungen

Die Versandkonfiguration bestimmt den Herkunftsort für alle Sendungen, Ihre Versandrichtlinien und die Handhabung von Sendungen an mehrere Adressen.

## Ursprungsort

Der Ausgangspunkt wird verwendet, um die Gebühr für Sendungen aus Ihrem Geschäft oder Lager zu berechnen und auch den Steuersatz für verkaufte Produkte zu bestimmen. Bei der Berechnung [EU-Steuern](international-tax-guidelines.md#eu-tax-configuration), stellen Sie sicher, dass die Variable [Standardmäßige Berechnung des Steuerziels](../configuration-reference/sales/tax.md) für jede Store-Ansicht dem Ausgangspunkt der Versandeinstellungen entspricht.

![Origin](../configuration-reference/sales/assets/shipping-settings-origin.png){width="600" zoomable="yes"}

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen **[!UICONTROL Shipping Settings]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Origin]** und führen Sie Folgendes aus:

   - [!UICONTROL Country]
   - [!UICONTROL Region / State]
   - [!UICONTROL ZIP / Postal Code]
   - [!UICONTROL City]
   - [!UICONTROL Street Address] (und Zeile 2, falls erforderlich)

1. Klicken **[!UICONTROL Save Config]**.

## Versandpolitik

Eine Versandpolitik sollte die Geschäftsregeln und Richtlinien Ihres Unternehmens für Sendungen erläutern. Wenn Sie beispielsweise über Preisregeln verfügen, die den kostenlosen Versand von Triggern ermöglichen, können Sie die Bedingungen in Ihrer Versandrichtlinie erläutern.

![Versandrichtlinien während der Kasse](./assets/storefront-checkout-shipping-policy.png){width="700" zoomable="yes"}

Um Ihre Versandrichtlinien während des Checkout anzuzeigen, füllen Sie die Versandrichtlinien-Parameter in der Konfiguration aus. Der Text wird angezeigt, wenn Kunden auf _Siehe Versandpolitik ._ während des Checkout.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen **[!UICONTROL Shipping Settings]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Shipping Policy Parameters]** Abschnitt.

1. Satz **[!UICONTROL Apply Custom Shipping Policy]** nach `Yes`.

1. Fügen Sie entweder Ihre **[!UICONTROL Shipping Policy]** in das Textfeld ein.

   >[!NOTE]
   >
   >Wenn Sie zum Erstellen des Textes ein Textverarbeitungsprogramm verwenden, achten Sie darauf, das Dokument als .txt-Datei zu speichern, um Steuerzeichen aus dem Text zu entfernen. Kopieren Sie dann den Text und fügen Sie ihn in das Textfeld Versandrichtlinie ein.

   ![Versandrichtlinienparameter](../configuration-reference/sales/assets/shipping-settings-shipping-policy-parameters.png){width="600" zoomable="yes"}

1. Klicken **[!UICONTROL Save Config]**.

## Mehrere Adressen

Die Versandoptionen mit mehreren Adressen ermöglichen es Kunden, eine Bestellung während des Checkout an mehrere Adressen zu senden und die maximale Anzahl von Adressen zu bestimmen, an die eine Bestellung versandt werden kann.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen **[!UICONTROL Multishipping Settings]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Options]** Abschnitt.

   ![Versandoptionen für mehrere Adressen](../configuration-reference/sales/assets/multishipping-settings-options.png){width="600" zoomable="yes"}

1. Satz **[!UICONTROL Allow Shipping to Multiple Addresses]** nach `Yes`.

1. Geben Sie die **[!UICONTROL Maximum Qty Allowed for Shipping to Multiple Addresses]**.

1. Klicken **[!UICONTROL Save Config]**.

>[!NOTE]
>
>![B2B für Adobe Commerce](../assets/b2b.svg) (B2B für Adobe Commerce) Bei Bestellungen mit mehreren Versandadressen muss die Variable [Kontozahlung](../b2b/enable-basic-features.md#configure-payment-on-account) Zahlungsmethode, auch wenn sie aktiviert ist, ist während des Checkouts nicht verfügbar.
