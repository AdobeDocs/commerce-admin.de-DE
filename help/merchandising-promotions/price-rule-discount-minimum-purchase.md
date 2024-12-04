---
title: Beispiel einer Warenkorbpreisregel - Rabatt mit Mindestproduktpreis
description: Sehen Sie sich ein Beispiel für die Verwendung einer Regel zum Warenkorbpreis an, um einen Rabatt mit einem Mindestproduktpreis anzubieten.
exl-id: dc06cd12-d23b-4836-9ad2-93ca60dac927
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: 6bc76c76bc7a17e115696911cc2499075d35c541
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# Beispiel einer Warenkorbpreisregel - Rabatt mit Mindestkauf

Mit Warenkorbpreisregeln können Sie einen prozentualen Rabatt auf der Grundlage eines Mindestproduktpreises im Warenkorb anbieten. Im folgenden Beispiel wird ein Rabatt von 10 % auf alle Produkte im gesamten Warenkorb angewendet, wenn mindestens 1 Produkt mit einem Preis über 30,00 USD aus einer bestimmten Kategorie zum Warenkorb hinzugefügt wird. Der Rabatt hat folgendes Format:

X % des gesamten Warenkorbs, wenn mindestens 1 Produkt aus der Kategorie Y stammt und sein Preis über $Z beträgt.

## Schritt 1. Eine Warenkorbregel erstellen

Befolgen Sie die grundlegenden [Anweisungen](price-rules-cart.md) , um eine Warenkorbregel zu erstellen.

## Schritt 2. Bedingungen definieren

1. Scrollen Sie nach unten und erweitern Sie den Abschnitt **[!UICONTROL Conditions]** um den ![Erweiterungsselektor](../assets/icon-display-expand.png).

1. Klicken Sie auf _Hinzufügen_ (![Symbol hinzufügen](../assets/icon-add-green-circle.png)) und wählen Sie **[!UICONTROL Product Attribute Combination]** aus.

   ![Bedingung der Warenkorbpreisregel - Kombination von Produktattributen](./assets/condition1.png){width="500" zoomable="yes"}

1. Klicken Sie am Anfang der nächsten Zeile auf _Hinzufügen_ (![Symbol hinzufügen](../assets/icon-add-green-circle.png)) und wählen Sie in der Liste unter **[!UICONTROL Product Attribute]** die Option **[!UICONTROL Category]**.

   - Klicken Sie auf den Link (**..**) _more_ , um weitere Optionen anzuzeigen.

     ![Bedingung der Warenkorbpreisregel - Kategorieoptionen](./assets/condition3.png){width="600" zoomable="yes"}

   - Klicken Sie auf das Symbol _Auswahl_ (![Listensymbol](../assets/icon-list-chooser.png)), um die verfügbaren Kategorien anzuzeigen. Aktivieren Sie im Kategoriebaum das Kontrollkästchen der Kategorien, die Sie einbeziehen möchten. Klicken Sie auf das Häkchen, um die Kategorieauswahlen zu akzeptieren.

     ![Bedingung der Warenkorbpreisregel - Kategorie](./assets/condition4.png){width="600" zoomable="yes"}

1. Klicken Sie am Anfang der nächsten Zeile auf _Hinzufügen_ (![Symbol hinzufügen](../assets/icon-add-green-circle.png)) und führen Sie folgende Schritte aus:

   - Wählen Sie in der Liste unter **[!UICONTROL Cart Item Attribute]** die Option **[!UICONTROL Price in cart]**.

     ![Bedingung der Warenkorbpreisregel - Warenkorbelementattribut](./assets/condition5.png){width="500"}

   - Klicken Sie auf **is** und wählen Sie `equals or greater than`.

   - Klicken Sie auf **..** und geben Sie den Betrag ein, der der Preis im Warenkorb sein muss, um die Bedingung zu erfüllen. Geben Sie beispielsweise `30` ein.

     ![Preisregel für Warenkorb - Preis im Warenkorb](./assets/condition6.png){width="500"}

1. Klicken Sie auf **[!UICONTROL Save and Continue Edit]**.

## Schritt 3. Aktionen definieren

1. Erweitern Sie den Abschnitt **[!UICONTROL Actions]** des Erweiterungsselektors ![Erweiterung](../assets/icon-display-expand.png) und führen Sie folgende Schritte aus:

   ![Aktionen der Preisregel für Warenkorb](./assets/minimum-discount-actions.png){width="600" zoomable="yes"}

   - Setzen Sie **[!UICONTROL Apply]** auf `Percent of product price discount`.

   - Geben Sie den Wert **[!UICONTROL Discount Amount]** ein. Geben Sie beispielsweise `10` für einen 10-%-Rabatt ein.

   - Um zu verhindern, dass zusätzliche Promotions auf den Kauf angewendet werden, setzen Sie **[!UICONTROL Discard subsequent rules]** auf `Yes`.

1. Klicken Sie auf &quot;**[!UICONTROL Save and Continue Edit]**&quot;und füllen Sie die Regel nach Bedarf aus.

## Schritt 4. Bezeichnungen ausfüllen

Führen Sie [Schritt 4](price-rules-cart.md) der Anweisungen für Warenkorbpreisregeln aus, um alle Beschriftungen einzugeben, die beim Checkout erscheinen.

## Schritt 5: Speichern und testen Sie die Regel

{{new-price-rule}}

1. Klicken Sie nach Abschluss der Regel auf **[!UICONTROL Save Rule]**.

1. Testen Sie die Regel, um sicherzustellen, dass sie ordnungsgemäß funktioniert.
