---
title: Beispiel für eine Warenkorb-Preisregel - Promotion zum kostenlosen Versand
description: Sehen Sie sich ein Beispiel für die Verwendung einer Warenkorb-Preisregel an, um einen kostenlosen Versand anzubieten.
exl-id: f7652254-ff01-44ff-a207-2d7cf2017517
feature: Merchandising, Price Rules, Shopping Cart, Shipping/Delivery
TQID: https://experienceleague.adobe.com/FR-q4Qj-ZDDzmfEKSvSj-BlwsM7ro-BqAE1yCppTaXE
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5520579-b31f-4df7-9281-f0d9f91e2edcid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 407
ht-degree: 0%

---

# Beispiel für eine Warenkorb-Preisregel - Promotion zum kostenlosen Versand

Kostenloser Versand kann als Promotion angeboten werden, entweder mit oder ohne [Coupon](price-rules-cart-coupon.md). Ein kostenloser Versandcoupon oder Gutschein kann auch auf Kundenabholaufträge angewendet werden, sodass die Bestellung fakturiert und versendet werden kann, um den [Workflow](../stores-purchase/order-processing.md#order-workflow-and-processing) abzuschließen.

Einige Versanddienstleister-Konfigurationen bieten Ihnen die Möglichkeit, kostenlosen Versand auf der Grundlage einer Mindestbestellung anzubieten. Um diese grundlegende Funktion zu erweitern, können Sie Regeln für den Einkaufswagenpreis verwenden, um komplexe Bedingungen auf der Grundlage mehrerer Produktattribute, Warenkorbinhalte und Kundengruppen zu erstellen.

## Schritt 1. Kostenlosen Versand aktivieren

1. Aktivieren Sie [kostenlosen Versand](../stores-purchase/shipping-free.md) in Ihrer Store-Konfiguration.

1. Füllen Sie die Einstellungen für den kostenlosen Versand für jeden [Provider-Dienst](../stores-purchase/carriers.md) aus, den Sie für den kostenlosen Versand verwenden möchten.

## Schritt 2. Erstellen einer Warenkorb-Preisregel

Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Cart Price Rules]**.

Gehen Sie wie folgt vor, um die Art der kostenlosen Versandaktion einzurichten, die Sie anbieten möchten.

### Beispiel 1: Kostenloser Versand für jede Bestellung

1. Vervollständigen Sie die **[!UICONTROL Rule Information]** wie folgt:

   - Geben Sie eine **[!UICONTROL Rule Name]** als interne Referenz ein.
   - Geben Sie eine kurze **[!UICONTROL Description]** zur Beschreibung der Regel ein.
   - Legen Sie **[!UICONTROL Active]** auf `Yes` fest.
   - Wählen Sie im **[!UICONTROL Websites]**-Feld jede Seite aus, auf der der kostenlose Versandcoupon verfügbar sein soll.
   - Wählen Sie die **[!UICONTROL Customer Groups]** aus, für die die Regel gilt.
   - Legen Sie **[!UICONTROL Coupon]** auf eine der folgenden Einstellungen fest:
      - Um eine kostenlose Versandaktion ohne Coupon anzubieten, akzeptieren Sie die Standardeinstellung (`No Coupon`).
      - Um einen Coupon mit der Preisregel zu verwenden, wählen Sie `Specific Coupon` aus. Falls erforderlich, füllen Sie die Anweisungen zum Einrichten eines [Coupons](price-rules-cart-coupon.md) aus.

1. Scrollen Sie nach unten und erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Actions]** und führen Sie die folgenden Schritte aus:

   - Legen Sie **[!UICONTROL Apply]** auf `Percent of product price discount` fest.
   - Legen Sie **[!UICONTROL Apply to Shipping Amount]** auf `Yes` fest.
   - Legen Sie **[!UICONTROL Free Shipping]** auf `For matching items only` fest.

   ![Warenkorb-Preisregel - kostenlose Versandaktionen](./assets/free-shipping-actions.png){width="600" zoomable="yes"}

### Beispiel 2: Kostenloser Versand für Bestellungen über $ Betrag

1. Füllen Sie die **[!UICONTROL General Information]** wie im vorherigen Beispiel beschrieben aus.

1. Scrollen Sie nach unten und erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Conditions]** .

1. Klicken Sie _Hinzufügen_ (![Symbol hinzufügen](../assets/icon-add-green-circle.png)), um eine Bedingung einzufügen, und führen Sie die folgenden Schritte aus:

   - Wählen Sie in der Liste unter **[!UICONTROL Cart Attribute]** die Option `Subtotal` aus.
   - Klicken Sie auf **[!UICONTROL is]** und wählen Sie `equals or greater than` aus.
   - Klicken Sie auf **…** und geben Sie einen Schwellenwert für die Zwischensumme ein, z. B. `100`, um die Bedingung abzuschließen.

   ![Warenkorb-Preisregel - Bedingung](./assets/free-shipping-condition1.png){width="600" zoomable="yes"}

1. Erweitern Sie bei Bedarf ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Actions]** und führen Sie folgende Schritte aus:

   - Legen Sie **[!UICONTROL Apply]** auf `Percent of product price discount` fest.
   - Legen Sie **[!UICONTROL Apply to Shipping Amount]** auf `Yes` fest.
   - Legen Sie **[!UICONTROL Free Shipping]** auf `For matching items only` fest.

## Schritt 3. Vervollständigen Sie die Beschriftungen

Führen Sie [Schritt 4](price-rules-cart.md) der Anleitung zur Warenkorbpreisregel aus, um alle Beschriftungen einzugeben, die während des Checkouts angezeigt werden.

## Schritt 4. Speichern und Testen der Regel

{{new-price-rule}}

1. Wenn Ihre Regel abgeschlossen ist, klicken Sie auf **[!UICONTROL Save Rule]**.

1. Testen Sie die Regel, um sicherzustellen, dass sie korrekt funktioniert.
