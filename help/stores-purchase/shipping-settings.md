---
title: Versandeinstellungen
description: Erfahren Sie, wie Sie die Versandeinstellungen konfigurieren, die den Ausgangspunkt und die Versandrichtlinie für Ihren Store definieren.
exl-id: 767b3039-39c7-4692-a0a8-a8fde27622cc
feature: Shipping/Delivery
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 0%

---

# Versandeinstellungen

Die Versandkonfiguration bestimmt den Herkunftsort für alle Sendungen, Ihre Versandrichtlinien und die Handhabung von Sendungen an mehrere Adressen.

## Ursprungsort

Der Ausgangspunkt wird verwendet, um die Gebühr für Sendungen aus Ihrem Geschäft oder Lager zu berechnen und auch den Steuersatz für verkaufte Produkte zu bestimmen. Stellen Sie bei der Berechnung von [EU-Steuern](international-tax-guidelines.md#eu-tax-configuration) sicher, dass die [Berechnung des Standardsteuerziels](../configuration-reference/sales/tax.md) für jede Store-Ansicht dem Ausgangspunkt für die Versandeinstellungen entspricht.

![Origin](../configuration-reference/sales/assets/shipping-settings-origin.png){width="600" zoomable="yes"}

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Shipping Settings]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Origin]** und führen Sie Folgendes aus:

   - [!UICONTROL Country]
   - [!UICONTROL Region / State]
   - [!UICONTROL ZIP / Postal Code]
   - [!UICONTROL City]
   - [!UICONTROL Street Address] (und Zeile 2, falls erforderlich)

1. Klicken Sie auf **[!UICONTROL Save Config]**.

## Versandpolitik

Eine Versandpolitik sollte die Geschäftsregeln und Richtlinien Ihres Unternehmens für Sendungen erläutern. Wenn Sie beispielsweise über Preisregeln verfügen, die den kostenlosen Versand von Triggern ermöglichen, können Sie die Bedingungen in Ihrer Versandrichtlinie erläutern.

![Versandrichtlinie während der Kasse](./assets/storefront-checkout-shipping-policy.png){width="700" zoomable="yes"}

Um Ihre Versandrichtlinien während des Checkout anzuzeigen, füllen Sie die Versandrichtlinien-Parameter in der Konfiguration aus. Der Text wird angezeigt, wenn Kunden beim Checkout auf _See our shipping policy_ klicken.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Shipping Settings]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Shipping Policy Parameters]** .

1. Setzen Sie **[!UICONTROL Apply Custom Shipping Policy]** auf `Yes`.

1. Fügen Sie entweder Ihren **[!UICONTROL Shipping Policy]**-Wert in das Textfeld ein oder geben Sie ihn ein.

   >[!NOTE]
   >
   >Wenn Sie zum Erstellen des Textes ein Textverarbeitungsprogramm verwenden, achten Sie darauf, das Dokument als .txt-Datei zu speichern, um Steuerzeichen aus dem Text zu entfernen. Kopieren Sie dann den Text und fügen Sie ihn in das Textfeld Versandrichtlinie ein.

   ![Versandrichtlinienparameter](../configuration-reference/sales/assets/shipping-settings-shipping-policy-parameters.png){width="600" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Save Config]**.

## Mehrere Adressen

Die Versandoptionen mit mehreren Adressen ermöglichen es Kunden, eine Bestellung während des Checkout an mehrere Adressen zu senden und die maximale Anzahl von Adressen zu bestimmen, an die eine Bestellung versandt werden kann.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Multishipping Settings]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Options]** .

   ![Optionen für die Bereitstellung mehrerer Adressen](../configuration-reference/sales/assets/multishipping-settings-options.png){width="600" zoomable="yes"}

1. Setzen Sie **[!UICONTROL Allow Shipping to Multiple Addresses]** auf `Yes`.

1. Geben Sie den Wert **[!UICONTROL Maximum Qty Allowed for Shipping to Multiple Addresses]** ein.

1. Klicken Sie auf **[!UICONTROL Save Config]**.

>[!NOTE]
>
>![Adobe Commerce B2B](../assets/b2b.svg) (Adobe Commerce B2B) Bei Bestellungen mit mehreren Versandadressen ist die Zahlungsmethode [Zahlung auf Konto](../b2b/enable-basic-features.md#configure-payment-on-account) während des Checkout nicht verfügbar, selbst wenn sie aktiviert ist.
