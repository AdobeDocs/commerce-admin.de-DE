---
title: Beispiel einer Warenkorbpreisregel - kostenlose Versandaktion
description: Sehen Sie sich ein Beispiel für die Verwendung einer Preisregel für den Warenkorb an, um kostenlosen Versand anzubieten.
exl-id: f7652254-ff01-44ff-a207-2d7cf2017517
feature: Merchandising, Price Rules, Shopping Cart, Shipping/Delivery
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 0%

---

# Beispiel einer Warenkorbpreisregel - kostenlose Versandaktion

Kostenloser Versand kann als Promotion angeboten werden, entweder mit oder ohne einen [Coupon](price-rules-cart-coupon.md). Ein kostenloser Versand-Gutschein oder Gutschein kann auch auf Kundenabholaufträge angewendet werden, sodass die Bestellung in Rechnung gestellt und versandt werden kann, um den [Workflow](../stores-purchase/order-processing.md#order-workflow-and-processing) abzuschließen.

Einige Konfigurationen von Versandunternehmen ermöglichen Ihnen, kostenlosen Versand auf Basis einer Mindestbestellung anzubieten. Um diese grundlegende Funktion zu erweitern, können Sie mithilfe von Preisregeln für Warenkorb komplexe Bedingungen erstellen, die auf mehreren Produktattributen, Warenkorbinhalten und Kundengruppen basieren.

## Schritt 1. Kostenlosen Versand aktivieren

1. Aktivieren Sie [kostenlosen Versand](../stores-purchase/shipping-free.md) in Ihrer Store-Konfiguration.

1. Füllen Sie die kostenlosen Versandeinstellungen für jeden [Betreiberdienst](../stores-purchase/carriers.md) aus, den Sie für den kostenlosen Versand verwenden möchten.

## Schritt 2. Erstellen einer Preisregel für den Warenkorb

Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Cart Price Rules]**.

Gehen Sie wie folgt vor, um die Art der kostenlosen Versandaktion einzurichten, die Sie anbieten möchten.

### Beispiel 1: Kostenloser Versand für jede Bestellung

1. Vervollständigen Sie den **[!UICONTROL Rule Information]** wie folgt:

   - Geben Sie einen &quot;**[!UICONTROL Rule Name]**&quot;-Wert für die interne Referenz ein.
   - Geben Sie einen kurzen **[!UICONTROL Description]** -Wert ein, um die Regel zu beschreiben.
   - Setzen Sie **[!UICONTROL Active]** auf `Yes`.
   - Wählen Sie im Feld &quot;**[!UICONTROL Websites]**&quot;jede Website aus, auf der der kostenlose Versand-Coupon verfügbar sein soll.
   - Wählen Sie die **[!UICONTROL Customer Groups]** aus, für die die Regel gilt.
   - Setzen Sie **[!UICONTROL Coupon]** auf einen der folgenden Werte:
      - Um eine kostenlose Versandaktion ohne Coupon anzubieten, akzeptieren Sie die Standardeinstellung (`No Coupon`).
      - Um einen Gutschein mit der Preisregel zu verwenden, wählen Sie `Specific Coupon` aus. Führen Sie bei Bedarf die Anweisungen zum Einrichten eines [Coupons](price-rules-cart-coupon.md) aus.

1. Scrollen Sie nach unten und erweitern Sie den Abschnitt **[!UICONTROL Actions]** um den ![Erweiterungsselektor](../assets/icon-display-expand.png) und gehen Sie folgendermaßen vor:

   - Setzen Sie **[!UICONTROL Apply]** auf `Percent of product price discount`.
   - Setzen Sie **[!UICONTROL Apply to Shipping Amount]** auf `Yes`.
   - Setzen Sie **[!UICONTROL Free Shipping]** auf `For matching items only`.

   ![Warenkorbpreisregel - Kostenlose Versandaktionen](./assets/free-shipping-actions.png){width="600" zoomable="yes"}

### Beispiel 2: Kostenloser Versand für Bestellungen über $

1. Füllen Sie die Einstellungen für **[!UICONTROL General Information]** aus, wie im vorherigen Beispiel beschrieben.

1. Scrollen Sie nach unten und erweitern Sie den Abschnitt **[!UICONTROL Conditions]** um den ![Erweiterungsselektor](../assets/icon-display-expand.png).

1. Klicken Sie auf _Hinzufügen_ (![Symbol hinzufügen](../assets/icon-add-green-circle.png)), um eine Bedingung einzufügen, und führen Sie die folgenden Schritte aus:

   - Wählen Sie in der Liste unter **[!UICONTROL Cart Attribute]** die Option `Subtotal`.
   - Klicken Sie auf **[!UICONTROL is]** und wählen Sie `equals or greater than` aus.
   - Klicken Sie auf **..** und geben Sie einen Schwellenwert für die Zwischensumme ein, z. B. `100`, um die Bedingung abzuschließen.

   ![Warenkorbpreisregel - Bedingung](./assets/free-shipping-condition1.png){width="600" zoomable="yes"}

1. Erweitern Sie ggf. den Abschnitt **[!UICONTROL Actions]** um den ![Erweiterungsselektor](../assets/icon-display-expand.png) und führen Sie die folgenden Schritte aus:

   - Setzen Sie **[!UICONTROL Apply]** auf `Percent of product price discount`.
   - Setzen Sie **[!UICONTROL Apply to Shipping Amount]** auf `Yes`.
   - Setzen Sie **[!UICONTROL Free Shipping]** auf `For matching items only`.

## Schritt 3. Bezeichnungen ausfüllen

Führen Sie [Schritt 4](price-rules-cart.md) der Anweisungen für Warenkorbpreisregeln aus, um alle Beschriftungen einzugeben, die beim Checkout erscheinen.

## Schritt 4. Speichern und testen Sie die Regel

{{new-price-rule}}

1. Klicken Sie nach Abschluss der Regel auf **[!UICONTROL Save Rule]**.

1. Testen Sie die Regel, um sicherzustellen, dass sie ordnungsgemäß funktioniert.
