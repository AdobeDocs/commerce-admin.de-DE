---
title: Versandeinstellungen
description: Erfahren Sie, wie Sie die Versandeinstellungen konfigurieren, die den Ursprungsort und die Versandrichtlinie für Ihren Store definieren.
exl-id: 767b3039-39c7-4692-a0a8-a8fde27622cc
feature: Shipping/Delivery
TQID: https://experienceleague.adobe.com/9sMHWFMnoS-OVhdWjjq8r-KE9hdVD2owO2tI8LoGN0s
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 555
ht-degree: 0%

---

# Versandeinstellungen

Die Versandkonfiguration legt den Ausgangspunkt für alle Sendungen, Ihre Versandrichtlinie und die Handhabung von Sendungen an mehrere Adressen fest.

## Ausgangspunkt

Der Ursprungsort wird verwendet, um die Gebühr für Sendungen aus Ihrem Lager oder Lager zu berechnen, und bestimmt auch den Steuersatz für verkaufte Produkte. Bei der Berechnung [EU](international-tax-guidelines.md#eu-tax-configuration)Steuern) ist sicherzustellen, dass die [Standardzielberechnung](../configuration-reference/sales/tax.md) für jede Shop-Ansicht dem Ausgangspunkt der Versandeinstellungen entspricht.

![Herkunft](../configuration-reference/sales/assets/shipping-settings-origin.png){width="600" zoomable="yes"}

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Shipping Settings]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Origin]** und führen Sie Folgendes aus:

   - [!UICONTROL Country]
   - [!UICONTROL Region / State]
   - [!UICONTROL ZIP / Postal Code]
   - [!UICONTROL City]
   - [!UICONTROL Street Address] (und Zeile 2, falls erforderlich)

1. Klicken Sie auf **[!UICONTROL Save Config]**.

## Schifffahrtspolitik

Eine Versandrichtlinie sollte die Geschäftsregeln und Richtlinien Ihres Unternehmens für Sendungen erläutern. Wenn Sie beispielsweise Preisregeln haben, die kostenlosen Versand zum Trigger haben, können Sie die Bedingungen in Ihrer Versandrichtlinie erklären.

![Versandrichtlinie beim Checkout](./assets/storefront-checkout-shipping-policy.png){width="700" zoomable="yes"}

Um Ihre Versandrichtlinie während des Checkouts anzuzeigen, füllen Sie die Parameter für die Versandrichtlinie in der Konfiguration aus. Der Text wird angezeigt, wenn Kunden beim Checkout _Siehe unsere Versandrichtlinie_ klicken.

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Shipping Settings]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Shipping Policy Parameters]** .

1. Legen Sie **[!UICONTROL Apply Custom Shipping Policy]** auf `Yes` fest.

1. Fügen Sie Ihre **[!UICONTROL Shipping Policy]** in das Textfeld ein oder geben Sie sie ein.

   >[!NOTE]
   >
   >Wenn Sie den Text mit einem Textverarbeitungsprogramm erstellen, stellen Sie sicher, dass Sie das Dokument als TXT-Datei speichern, um alle Steuerzeichen aus dem Text zu entfernen. Kopieren Sie dann den Text und fügen Sie ihn in das Textfeld Versandrichtlinie ein.

   ![Versandrichtlinienparameter](../configuration-reference/sales/assets/shipping-settings-shipping-policy-parameters.png){width="600" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Save Config]**.

## Mehrere Adressen

Die Versandoptionen für mehrere Adressen ermöglichen es Kunden, eine Bestellung während des Checkouts an mehrere Adressen zu versenden und die maximale Anzahl der Adressen zu bestimmen, an die eine Bestellung versendet werden kann.

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Multishipping Settings]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Options]** .

   ![Multiaddress-Lieferoptionen](../configuration-reference/sales/assets/multishipping-settings-options.png){width="600" zoomable="yes"}

1. Legen Sie **[!UICONTROL Allow Shipping to Multiple Addresses]** auf `Yes` fest.

1. Geben Sie die **[!UICONTROL Maximum Qty Allowed for Shipping to Multiple Addresses]** ein.

1. Klicken Sie auf **[!UICONTROL Save Config]**.

>[!NOTE]
>
>![Adobe Commerce B2B](../assets/b2b.svg) (Adobe Commerce B2B) Bei Bestellungen mit mehreren Versandadressen ist die Zahlungsmethode [Zahlung auf Rechnung](../b2b/enable-basic-features.md#configure-payment-on-account) auch wenn sie aktiviert ist, während des Checkouts nicht verfügbar.

## Tracking-URLs von E-Mails zu Sendungen

[!BADGE nur SaaS]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce as a Cloud Service-Projekte (von Adobe verwaltete SaaS-Infrastruktur)."}

Standardmäßig sind Sendungsverfolgungsnummern, die in Kunden-E-Mails gesendet werden, Klartext. Sie können diese Tracking-Nummern in anklickbare Links umwandeln, indem Sie die URL-Funktion für benutzerdefiniertes Tracking aktivieren. Mit dieser Funktion können Sie eine Vorlage für Tracking-URLs für verschiedene Versanddienstleister definieren. Jede Vorlage enthält die vollständige URL zur Tracking-Website und einen Platzhalter für die Tracking-Nummer. Commerce ersetzt den Platzhalter durch die tatsächliche Tracking-Nummer in der E-Mail.

Die folgenden Spediteure werden unterstützt:

- United States Postal Service (USPS)
- United Parcel Service (UPS)
- Federal Express (FedEx)
- DHL Express (DHL)

So aktivieren oder bearbeiten Sie benutzerdefinierte Tracking-URLs:

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Shipping Settings]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Shipment Tracking URLs]** .

1. Legen Sie **[!UICONTROL Enable Custom Tracking URLs]** auf `Yes` fest.

1. Für jeden unterstützten Provider werden Standard-URL-Vorlagen bereitgestellt. Wenn Sie einen dieser Werte ändern müssen, geben Sie eine neue URL-Vorlage in das entsprechende Feld ein. Verwenden Sie `{{tracking_number}}` als Platzhalter für die tatsächliche Tracking-Nummer. Wenn beispielsweise UPS seine URL in `https://www.ups.com/newtracker?tracknumber` ändert, könnte die neue Tracking-URL-Vorlage wie folgt aussehen:

   ```text
   https://www.ups.com/newtracker?tracknumber={{tracking_number}}
   ```

1. Klicken Sie auf **[!UICONTROL Save Config]**.
