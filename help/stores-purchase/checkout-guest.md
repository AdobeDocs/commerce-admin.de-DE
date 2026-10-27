---
title: Gast-Checkout
description: Erfahren Sie, wie Sie Gast-Checkout-Funktionen in Ihrem Store aktivieren.
exl-id: ce25eba3-7503-46aa-a5cd-9b7d5662164b
feature: Checkout
TQID: 'https://experienceleague.adobe.com/jxrHQ1knuqHBmM1DsVa9NqdV-XNFdQDWjvwW4kHEyYM'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 8cd50456-5eb0-5364-922a-f14161feb828
    internal-label: Checkout
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 9d3fe9829bb5a7f2a75ad3c89edd38010f816a0c
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%
---
# Gast-Checkout

Ihr Store kann so konfiguriert werden, dass Käufer vor einem Kauf ein Konto eröffnen müssen. In der Standardeinstellung können Gäste Einkäufe tätigen. Nach Abschluss des Checkout-Prozesses können sie sich für ein Konto registrieren lassen.

![Der Luma-Store zeigt das Auschecken als Gast an](./assets/storefront-checkout-as-guest.png){width="600" zoomable="yes"}

**_So deaktivieren Sie den Gast-Checkout:_**

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > **[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Checkout]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Checkout Options]** .

   ![Auf der Konfigurationsseite wurden die Checkout-Optionen erweitert](./assets/checkout-checkout-options.png){width="700" zoomable="yes"}

Eine ausführliche Beschreibung jeder dieser Konfigurationseinstellungen finden Sie unter [Checkout-Optionen](../configuration-reference/sales/checkout.md#checkout-options) im _Konfigurationsreferenzhandbuch_.

1. Wenn die Einstellung für eine bestimmte Store-Ansicht ist, wählen [die Store-Ansicht aus](../configuration-reference/scope-change.md#set-the-scope) für die die Konfiguration gilt.

   Wenn Sie dazu aufgefordert werden, klicken Sie auf **[!UICONTROL OK]** , um fortzufahren.

1. Legen Sie **[!UICONTROL Allow Guest Checkout]** auf `No` fest.

   Deaktivieren Sie bei Bedarf das Kontrollkästchen **[!UICONTROL Use system value]** , um Änderungen an dieser Einstellung zu aktivieren.

1. Klicken Sie auf **[!UICONTROL Save Config]**.

## Zugriff auf Gastbestellungen für registrierte E-Mails zulassen

[!BADGE nur SaaS]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce as a Cloud Service-Projekte (von Adobe verwaltete SaaS-Infrastruktur)."}

Eine optionale Konfiguration auf Store-Ebene, die standardmäßig deaktiviert ist, ermöglicht es Kunden, ihre Bestellungen über eine E-Mail-Adresse zu verfolgen, die mit einem registrierten Kundenkonto übereinstimmt.

Wenn diese Option aktiviert ist, bleiben Gast-Checkout-Bestellungen, die mit einer registrierten E-Mail aufgegeben werden, weiterhin zugänglich und werden auch im Bestellverlauf des Kunden angezeigt.

Um diese Funktion zu aktivieren, navigieren Sie zu **[!UICONTROL Stores]** > **[!UICONTROL Configuration]** > **[!UICONTROL Sales]** > **[!UICONTROL Sales]** > **[!UICONTROL Guest Checkout]** und legen Sie die **[!UICONTROL Allow Guest Order Access for Registered Emails]** auf `Yes` fest.
