---
title: Beispiel einer Warenkorbpreisregel - Rabatt mit Mindestkauf
description: Sehen Sie sich ein Beispiel für die Verwendung einer Preisregel für den Warenkorb an, um einen Rabatt mit einem Mindestkauf anzubieten.
exl-id: dc06cd12-d23b-4836-9ad2-93ca60dac927
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 0%

---

# Beispiel einer Warenkorbpreisregel - Rabatt mit Mindestkauf

Mit den Regeln zum Warenkorbpreis können Sie einen prozentualen Rabatt auf der Grundlage eines Mindestkäufs anbieten. Im folgenden Beispiel wird ein Rabatt von 25 % auf alle Käufe über 200,00 USD in einer bestimmten Kategorie angewendet. Der Rabatt hat folgendes Format:

X % aller Y (Kategorie) über Z Dollar

## Schritt 1. Eine Warenkorbregel erstellen

Grundlegende [instructions](price-rules-cart.md) , um eine Warenkorbregel zu erstellen.

## Schritt 2. Bedingungen definieren

1. Hinunter scrollen und erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Conditions]** Abschnitt.

1. Klicks _Hinzufügen_ (![Symbol &quot;Hinzufügen&quot;](../assets/icon-add-green-circle.png)) und wählen Sie **[!UICONTROL Product Attribute Combination]**.

   ![Preisregel für Warenkorb - Produktattributkombination](./assets/condition1.png){width="500" zoomable="yes"}

1. Klicks _Hinzufügen_ (![Symbol &quot;Hinzufügen&quot;](../assets/icon-add-green-circle.png)) am Anfang der nächsten Zeile und in der Liste unter **[!UICONTROL Product Attribute]** auswählen **[!UICONTROL Category]**.

   - Klicken Sie auf (**...**) _more_ -Link, um weitere Optionen anzuzeigen.

     ![Preisregel für Warenkorb - Kategorieoptionen](./assets/condition3.png){width="600" zoomable="yes"}

   - Klicken Sie auf _Auswahl_ (![Listen-Symbol](../assets/icon-list-chooser.png)), um die verfügbaren Kategorien anzuzeigen. Aktivieren Sie im Kategoriebaum das Kontrollkästchen der Kategorien, die Sie einbeziehen möchten. Klicken Sie auf das Häkchen, um die Kategorieauswahlen zu akzeptieren.

     ![Preisregel für Warenkorb - Kategorie](./assets/condition4.png){width="600" zoomable="yes"}

1. Klicks _Hinzufügen_ (![Symbol &quot;Hinzufügen&quot;](../assets/icon-add-green-circle.png)) am Anfang der nächsten Zeile und gehen Sie wie folgt vor:

   - In der Liste unter **[!UICONTROL Cart Item Attribute]** auswählen **[!UICONTROL Price in cart]**.

     ![Preisregel für Warenkorb - Warenkorbelement-Attribut](./assets/condition5.png){width="500"}

   - Klicks **is** und wählen `equals or greater than`.

   - Klicks **...** und geben Sie den Betrag ein, der vom Preis im Warenkorb benötigt wird, um die Bedingung zu erfüllen. Geben Sie beispielsweise `30`.

     ![Preisregel für Warenkorb - Preis im Warenkorb](./assets/condition6.png){width="500"}

1. Klicken **[!UICONTROL Save and Continue Edit]**.

## Schritt 3. Aktionen definieren

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Actions]** und führen Sie folgende Schritte aus:

   ![Aktionen zu Warenkorbpreisregeln](./assets/minimum-discount-actions.png){width="600" zoomable="yes"}

   - Satz **[!UICONTROL Apply]** nach `Percent of product price discount`.

   - Geben Sie die **[!UICONTROL Discount Amount]**. Geben Sie beispielsweise `10` für einen 10% Rabatt.

   - Um zu verhindern, dass zusätzliche Promotions auf den Kauf angewendet werden, legen Sie **[!UICONTROL Discard subsequent rules]** nach `Yes`.

1. Klicks **[!UICONTROL Save and Continue Edit]** und führen Sie die Regel nach Bedarf aus.

## Schritt 4. Bezeichnungen ausfüllen

Fertig [Schritt 4](price-rules-cart.md) der Preisregel des Warenkorbs, um alle Bezeichnungen einzugeben, die beim Checkout erscheinen.

## Schritt 5: Speichern und testen Sie die Regel

{{new-price-rule}}

1. Klicken Sie nach Abschluss der Regel auf **[!UICONTROL Save Rule]**.

1. Testen Sie die Regel, um sicherzustellen, dass sie ordnungsgemäß funktioniert.
