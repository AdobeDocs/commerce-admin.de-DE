---
title: 'Beispiel einer Preisregel für den Warenkorb - kaufen Sie diesen Artikel:'
description: Sehen Sie sich ein Beispiel für die Verwendung einer Preisregel für den Warenkorb an, um eine Promotion für "buy-this-get-that"anzubieten.
exl-id: 49e4f9d1-bc60-4861-baca-a23fe148d1c4
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '622'
ht-degree: 0%

---

# Beispiel einer Preisregel für den Warenkorb - kaufen Sie diesen Artikel:

Dieses Beispiel zeigt, wie Sie eine [Warenkorbpreisregel](price-rules-cart.md) für eine _Diese Werbeaktion kaufen, diese kostenlose_ -Promotion abrufen. Der Rabatt hat folgendes Format:

_X Produktmenge kaufen, Y Menge kostenlos abrufen_

## Schritt 1. Erstellen einer Preisregel für den Warenkorb

Führen Sie [Schritt 1](price-rules-cart.md) der Anweisungen für Warenkorbpreisregeln aus, um die Regelinformationen auszufüllen.

## Schritt 2. Bedingungen definieren

Führen Sie [Schritt 2](price-rules-cart.md) der Warenkorbanweisungen aus, um die Bedingungen für die Preisregel zu definieren. Dies ist die erste von zwei Bedingungen, die der Regel hinzugefügt werden können, und bestimmt, wann die Regel ausgelöst wird. Sie kann auf einer Kombination der folgenden Elemente basieren:

- Produktattribute
- Produkte
- Warenkorbattribute
- ![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Kundensegmente

Wenn Sie das Feld leer lassen, wird die Regel für jeden Warenkorb ausgelöst.

![Warenkorbpreisregel - Bedingung](./assets/buy-x-get-y-condition-default.png){width="600" zoomable="yes"}

## Schritt 3. Aktionen definieren

1. Erweitern Sie den Abschnitt **[!UICONTROL Actions]** des Erweiterungsselektors ![Erweiterung](../assets/icon-display-expand.png) und führen Sie folgende Schritte aus:

   - Setzen Sie **[!UICONTROL Apply]** auf `Buy X get Y free (_[!UICONTROL _[!UICONTROL Discount Amount]_]_ is Y)`.

   - Setzen Sie **[!UICONTROL Discount Amount]** auf `1`. Dies ist die Menge, die der Kunde kostenlos erhält.

   - Geben Sie die Zahl im Feld **[!UICONTROL Maximum Qty Discount is Applied To]** ein, um die Anzahl der Rabatte zu begrenzen, die bei Erfüllung der Bedingung gewährt werden können. Dies wird mit dieser [Formel](#maximum-quantity-discount) berechnet.

   - Geben Sie für **[!UICONTROL Discount Qty Step (Buy X)]** die Menge ein, die der Kunde kaufen muss, um sich für den Rabatt zu qualifizieren. In diesem Beispiel muss der Kunde drei Einkäufe tätigen.

   - Wenn Sie verhindern möchten, dass andere Rabatte auf den Kauf angewendet werden, setzen Sie **[!UICONTROL Discard subsequent rules]** auf `Yes`.

   ![Preisregel für Warenkorb - kaufen Sie 3 erhalten 1 kostenlose ](./assets/buy-3-get-1-actions.png){width="600" zoomable="yes"}

1. Um die Regel nur auf bestimmte Artikel im Warenkorb anzuwenden, füllen Sie die Bedingung aus, um die Warenkorbartikel und/oder Produktattribute zu beschreiben, die für die Promotion erforderlich sind.

   Im folgenden Beispiel wird die SKU verwendet, um die Regel auf alle zugehörigen Varianten eines konfigurierbaren Produkts anzuwenden.

   ![Preisregel für Warenkorb - Bedingung für Warenkorbartikel](./assets/buy-3-get-1-actions-condition.png){width="600" zoomable="yes"}

1. Um **[!UICONTROL Free Shipping]** einzubeziehen, wählen Sie `For matching items only`.

1. Klicken Sie auf &quot;**[!UICONTROL Save and Continue Edit]**&quot;und führen Sie den Rest der Regel nach Bedarf aus.

## Schritt 4. Titel ausfüllen

Führen Sie [Schritt 4](price-rules-cart.md) der Anweisungen für Warenkorbpreisregeln aus, um den Titel einzugeben, der beim Checkout angezeigt wird.

## Schritt 5: Speichern und testen Sie die Regel

{{new-price-rule}}

1. Klicken Sie nach Abschluss der Regel auf **[!UICONTROL Save Rule]**.

1. Testen Sie die Regel, um sicherzustellen, dass sie ordnungsgemäß funktioniert.

## Varianten

&quot;X kaufen&quot;Get Y Free wird als einzelne Aktion verarbeitet, mit einer _Zeilensumme_ -Abhängigkeit. Alle Artikel müssen von derselben SKU stammen, um für die Promotion qualifiziert zu sein. Beispiel:

Kaufen Sie X Produktmenge aus Kategorie A, erhalten Sie Y Menge des gleichen Produkts kostenlos.

Um das freie Produkt auf die Kategorien A, B und C zu beschränken, legen Sie die Aktion wie folgt fest:

Wenn ALLE dieser Bedingungen TRUE sind:
Kategorie ist eine Kategorie von A, B, C

Um die freien Artikel jeder Kategorie (A, B oder C) zu begrenzen und Y von SKUs zu erhalten (D123, E123 oder F123), setzen Sie die Aktion wie folgt:

Wenn ALLE dieser Bedingungen TRUE sind:
SKU ist einer der Werte D123, E123, F123

## Maximaler Mengenrabatt

Verwenden Sie die folgende Formel, um den richtigen Wert für den maximalen Rabatt zu ermitteln:

Formel = `(X+Y) * (M/Y)`
Wo
`X` = Anzahl der gekauften Artikel
`Y` = Anzahl der freien Elemente
`M` = Maximale Anzahl der zulässigen freien Elemente

Beispiel:

Kaufen Sie fünf und erhalten Sie zwei kostenlose Artikel mit maximal vier kostenlosen Artikeln.

    Wobei
    X = 5
    Y = 2
    M = 4
    Maximaler Qty-Rabatt = (5+2)*(4/2)=(7)*(2)=14

Kaufen Sie fünf und erhalten Sie drei kostenlose Artikel mit maximal neun kostenlosen Artikeln.

    Wobei
    X = 5
    Y = 3
    M = 9
    Maximaler Qty-Rabatt = (5+3)*(9/3)=24

Kaufen Sie 20 und erhalten Sie zwei gratis mit maximal 20 kostenlosen Artikeln.

    Wobei
    X = 20
    Y = 2
    M = 20
    Maximaler Qty-Rabatt = (20+2)*(20/2)=(22)*(10)=220
