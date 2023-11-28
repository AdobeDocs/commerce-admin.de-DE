---
title: 'Beispiel einer Preisregel für den Warenkorb - kaufen Sie diesen Artikel:'
description: Sehen Sie sich ein Beispiel für die Verwendung einer Preisregel für den Warenkorb an, um eine Promotion für "buy-this-get-that"anzubieten.
exl-id: 49e4f9d1-bc60-4861-baca-a23fe148d1c4
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '582'
ht-degree: 0%

---

# Beispiel einer Preisregel für den Warenkorb - kaufen Sie diesen Artikel:

In diesem Beispiel wird gezeigt, wie eine [Warenkorbpreisregel](price-rules-cart.md) für _Kaufen Sie das hier, bestellen Sie das kostenlos._ Förderung. Der Rabatt hat folgendes Format:

_X Produktmenge kaufen, Y Menge kostenlos kaufen_

## Schritt 1. Erstellen einer Preisregel für den Warenkorb

Fertig [Schritt 1](price-rules-cart.md) der Anweisungen zur Preisregel des Warenkorbs, um die Regelinformationen auszufüllen.

## Schritt 2. Bedingungen definieren

Fertig [Schritt 2](price-rules-cart.md) der Warenkorbanweisungen, um die Bedingungen für die Preisregel zu definieren. Dies ist die erste von zwei Bedingungen, die der Regel hinzugefügt werden können, und bestimmt, wann die Regel ausgelöst wird. Sie kann auf einer Kombination der folgenden Elemente basieren:

- Produktattribute
- Produkte
- Warenkorbattribute
- ![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce) Kundensegmente

Wenn Sie das Feld leer lassen, wird die Regel für jeden Warenkorb ausgelöst.

![Preisregel für Warenkorb - Bedingung](./assets/buy-x-get-y-condition-default.png){width="600" zoomable="yes"}

## Schritt 3. Aktionen definieren

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Actions]** und führen Sie folgende Schritte aus:

   - Satz **[!UICONTROL Apply]** nach `Buy X get Y free (_[!UICONTROL _[!UICONTROL Discount Amount]_]_ is Y)`.

   - Satz **[!UICONTROL Discount Amount]** nach `1`. Dies ist die Menge, die der Kunde kostenlos erhält.

   - Um die Anzahl der Rabatte zu begrenzen, die bei Erfüllung der Bedingung gewährt werden können, geben Sie die Zahl in **[!UICONTROL Maximum Qty Discount is Applied To]** -Feld. Dies wird wie folgt berechnet: [Formel](#maximum-quantity-discount).

   - Für **[!UICONTROL Discount Qty Step (Buy X)]** Geben Sie die Menge ein, die der Kunde kaufen muss, um für den Rabatt zu infrage zu kommen. In diesem Beispiel muss der Kunde drei Einkäufe tätigen.

   - Wenn Sie verhindern möchten, dass andere Rabatte auf den Kauf angewendet werden, legen Sie **[!UICONTROL Discard subsequent rules]** nach `Yes`.

   ![Preisregel für Warenkorb - kaufen 3 erhalten 1 gratis](./assets/buy-3-get-1-actions.png){width="600" zoomable="yes"}

1. Um die Regel nur auf bestimmte Artikel im Warenkorb anzuwenden, füllen Sie die Bedingung aus, um die Warenkorbartikel und/oder Produktattribute zu beschreiben, die für die Promotion erforderlich sind.

   Im folgenden Beispiel wird die SKU verwendet, um die Regel auf alle zugehörigen Varianten eines konfigurierbaren Produkts anzuwenden.

   ![Preisregel für Warenkorb - Bedingung für Warenkorbartikel](./assets/buy-3-get-1-actions-condition.png){width="600" zoomable="yes"}

1. Einbeziehen **[!UICONTROL Free Shipping]** auswählen `For matching items only`.

1. Klicks **[!UICONTROL Save and Continue Edit]** und führen Sie den Rest der Regel nach Bedarf aus.

## Schritt 4. Titel ausfüllen

Fertig [Schritt 4](price-rules-cart.md) der Preisregel des Warenkorbs, um den Titel einzugeben, der beim Checkout angezeigt wird.

## Schritt 5: Speichern und testen Sie die Regel

{{new-price-rule}}

1. Klicken Sie nach Abschluss der Regel auf **[!UICONTROL Save Rule]**.

1. Testen Sie die Regel, um sicherzustellen, dass sie ordnungsgemäß funktioniert.

## Varianten

Kaufen Sie X Get Y Free wird als einzelne Aktion verarbeitet, mit einer _Zeilensumme_ Abhängigkeit. Alle Artikel müssen von derselben SKU stammen, um für die Promotion qualifiziert zu sein. Beispiel:

Kaufen Sie X Produktmenge aus Kategorie A, erhalten Sie Y Menge des gleichen Produkts kostenlos.

Um das freie Produkt auf die Kategorien A, B und C zu beschränken, legen Sie die Aktion wie folgt fest:

Wenn ALLE dieser Bedingungen TRUE sind: Die Kategorie ist eine von A, B, C

Um die freien Artikel jeder Kategorie (A, B oder C) zu begrenzen und Y von SKUs zu erhalten (D123, E123 oder F123), setzen Sie die Aktion wie folgt:

Wenn ALLE dieser Bedingungen TRUE sind: SKU ist eine der Bedingungen D123, E123, F123

## Maximaler Mengenrabatt

Verwenden Sie die folgende Formel, um den richtigen Wert für den maximalen Rabatt zu ermitteln:

Formel = `(X+Y) * (M/Y)`
Wo
`X` = Anzahl der gekauften Artikel
`Y` = Anzahl der kostenlosen Artikel
`M` = Maximale Anzahl der zulässigen freien Artikel

Beispiel:

Kaufen Sie fünf und erhalten Sie zwei kostenlose Artikel mit maximal vier kostenlosen Artikeln.

    Wo
    X = 5
    Y = 2
    M = 4
    Maximaler Mengenrabatt = (5+2)*(4/2)=(7)*(2)=14

Kaufen Sie fünf und erhalten Sie drei kostenlose Artikel mit maximal neun kostenlosen Artikeln.

    Wo
    X = 5
    Y = 3
    M = 9
    Maximaler Mengenrabatt = (5+3)*(9/3)=24

Kaufen Sie 20 und erhalten Sie zwei gratis mit maximal 20 kostenlosen Artikeln.

    Wo
    X = 20
    Y = 2
    M = 20
    Maximaler Mengenrabatt = (20+2)*(20/2)=(22)*(10)=220
