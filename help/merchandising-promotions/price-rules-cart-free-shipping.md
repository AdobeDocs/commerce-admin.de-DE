---
title: Beispiel für eine Warenkorb-Preisregel - Promotion zum kostenlosen Versand
description: Sehen Sie sich ein Beispiel für die Verwendung einer Warenkorb-Preisregel an, um einen kostenlosen Versand anzubieten.
exl-id: f7652254-ff01-44ff-a207-2d7cf2017517
feature: Merchandising, Price Rules, Shopping Cart, Shipping/Delivery
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '407'
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
