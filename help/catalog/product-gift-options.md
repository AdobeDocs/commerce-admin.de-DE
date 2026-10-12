---
title: Produkteinstellungen - [!UICONTROL Gift Options]
description: Für ein Produkt bestimmen die [!UICONTROL Gift Options] Einstellungen, ob eine Geschenknachricht enthalten sein kann oder ob Geschenkverpackungsoptionen während des Checkouts verfügbar sind.
exl-id: 21597e38-60f5-45e5-8d99-955d088c5c48
feature: Catalog Management, Products, Gift
TQID: 'https://experienceleague.adobe.com/MIzb2vY-DiVqODkNFmgX3tFLejQFZMtOETUDPoHrt-Y'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
    internal-label: Catalog management
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: 4067ab89-2e97-5de1-8d98-de8318461a8d
    internal-label: Products
  - id: 4fc0a729-4349-5307-bd06-1b4bfbaf5d0c
    internal-label: Gift
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 0%
---
# Produkteinstellungen - [!UICONTROL Gift Options]

Im Abschnitt _[!UICONTROL Gift Options]_&#x200B;können Sie Optionen für Geschenknachrichten und Geschenkverpackungen beim Checkout auf Produktebene festlegen. Um die Standardkonfigurationseinstellung zu überschreiben, deaktivieren Sie das Kontrollkästchen **[!UICONTROL Use Config Settings]**.

![Geschenkoptionen](./assets/product-gift-options-ee.png){width="600" zoomable="yes"}

## Festlegen von Geschenkoptionen für ein einzelnes Produkt

1. Öffnen Sie das Produkt im Bearbeitungsmodus.

1. Scrollen Sie nach unten und erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt _[!UICONTROL Gift Options]_&#x200B;und führen Sie die folgenden Schritte aus:

   - Um die Standardeinstellung zu überschreiben, deaktivieren Sie das Kontrollkästchen **[!UICONTROL Use Config Settings]** .

   - Legen Sie **[!UICONTROL Allow Gift Message]** nach Bedarf für das Produkt fest.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (nur [Adobe Commerce](../landing/home.md#product-editions)) Legen Sie **[!UICONTROL Allow Gift Wrapping]** nach Bedarf für das Produkt fest.

   - ![Adobe Commerce](../assets/adobe-logo.svg) ([nur Adobe Commerce](../landing/home.md#product-editions)) Geben Sie bei Bedarf die **[!UICONTROL Price for Gift Wrapping]** ein.

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.

## Aktivieren von Geschenknachrichten für Ihren Shop

Standardmäßig ermöglicht Commerce es den Kundinnen und Kunden, ihren Bestellungen und Produkten während des Checkout-Prozesses eine personalisierte Geschenknachricht hinzuzufügen.

Sie können diese Funktion Kunden bereitstellen, indem Sie _Geschenknachricht_ für Ihren Store aktivieren:

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen Sie darunter **[!UICONTROL Sales]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) **[!UICONTROL Gift Options]** auf der Seite.

1. Wählen Sie **[!UICONTROL Allow Gift Messages on Order Level]** die Option `Yes` aus, um eine einzelne Geschenknachricht für die gesamte Bestellung zu aktivieren.

1. Wählen Sie **[!UICONTROL Allow Gift Messages for Order Items]** die Option `Yes` aus, um das separate Hinzufügen von Geschenknachrichten zu einzelnen Artikeln im Warenkorb des Kunden zu aktivieren.

1. Klicken Sie auf **[!UICONTROL Save Config]**.

Mit dieser Konfiguration können Kundinnen und Kunden der Warenkorbseite eine Geschenknachricht von der Storefront hinzufügen, wie im folgenden Beispiel gezeigt:

![Geschenknachricht](./assets/gift-message.png){width="600" zoomable="yes"}
