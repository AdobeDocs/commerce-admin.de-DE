---
title: Beispiel für eine Warenkorb-Preisregel - kaufen Sie diese und erhalten Sie die
description: Sehen Sie sich ein Beispiel für die Verwendung einer Warenkorb-Preisregel an, um eine Buy-this-get-that-Promotion anzubieten.
exl-id: 49e4f9d1-bc60-4861-baca-a23fe148d1c4
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '622'
ht-degree: 0%

---

# Beispiel für eine Warenkorb-Preisregel - kaufen Sie diese und erhalten Sie die

Dieses Beispiel zeigt, wie Sie eine [Warenkorb-Preisregel](price-rules-cart.md) für eine _Kaufen Sie dies, erhalten Sie diese kostenlose_ Promotion einrichten. Der Rabatt hat folgendes Format:

_Kaufen Sie X Menge des Produkts, erhalten Sie Y Menge kostenlos_

## Schritt 1. Erstellen einer Warenkorb-Preisregel

Führen Sie [Schritt 1](price-rules-cart.md) der Anweisungen für die Warenkorbpreisregel aus, um die Regelinformationen auszufüllen.

## Schritt 2. Definieren der Bedingungen

Führen Sie [Schritt 2](price-rules-cart.md) der Warenkorbanweisungen aus, um die Bedingungen für die Preisregel zu definieren. Dies ist die erste von zwei Bedingungen, die der Regel hinzugefügt werden können, und bestimmt, wann die Regel ausgelöst wird. Sie kann auf einer Kombination der folgenden Elemente basieren:

- Produktattribute
- PRODUCT
- Warenkorb-Attribute
- ![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce)-Kundensegmente

Wenn Sie das Feld leer lassen, wird die Regel für jeden Warenkorb ausgelöst.

![Warenkorb-Preisregel - Bedingung](./assets/buy-x-get-y-condition-default.png){width="600" zoomable="yes"}

## Schritt 3. Definieren der Aktionen

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Actions]** und führen Sie folgende Schritte aus:

   - Legen Sie **[!UICONTROL Apply]** auf `Buy X get Y free (_[!UICONTROL _[!UICONTROL Discount Amount]_]_ is Y)` fest.

   - Legen Sie **[!UICONTROL Discount Amount]** auf `1` fest. Dies ist die Menge, die der Kunde kostenlos erhält.

   - Um die Anzahl der Rabatte zu begrenzen, die angewendet werden können, wenn die Bedingung erfüllt ist, geben Sie die Zahl in das Feld **[!UICONTROL Maximum Qty Discount is Applied To]** ein. Dies wird mithilfe dieser [Formel](#maximum-quantity-discount) berechnet.

   - Geben Sie **[!UICONTROL Discount Qty Step (Buy X)]** die Menge ein, die der Kunde erwerben muss, um für den Rabatt in Frage zu kommen. In diesem Beispiel muss der Kunde drei erwerben.

   - Wenn Sie verhindern möchten, dass andere Rabatte auf den Kauf angewendet werden, setzen Sie **[!UICONTROL Discard subsequent rules]** auf `Yes`.

   ![Warenkorb-Preisregel - 3 kaufen und 1 gratis erhalten](./assets/buy-3-get-1-actions.png){width="600" zoomable="yes"}

1. Um die Regel nur auf bestimmte Artikel im Warenkorb anzuwenden, füllen Sie die Bedingung aus, um die für die Promotion erforderlichen Artikel im Warenkorb und/oder Produktattribute zu beschreiben.

   Im folgenden Beispiel wird die SKU verwendet, um die Regel auf alle zugehörigen Varianten eines konfigurierbaren Produkts anzuwenden.

   ![Warenkorb-Preisregel - Bedingung für Warenkorbartikel](./assets/buy-3-get-1-actions-condition.png){width="600" zoomable="yes"}

1. Um **[!UICONTROL Free Shipping]** einzubeziehen, wählen Sie `For matching items only` aus.

1. Klicken Sie auf **[!UICONTROL Save and Continue Edit]** und vervollständigen Sie den Rest der Regel nach Bedarf.

## Schritt 4. Vervollständigen Sie den Titel

Führen Sie [Schritt 4](price-rules-cart.md) der Anleitung zur Warenkorbpreisregel aus, um den Titel einzugeben, der während des Checkouts angezeigt wird.

## Schritt 5: Speichern und Testen der Regel

{{new-price-rule}}

1. Wenn Ihre Regel abgeschlossen ist, klicken Sie auf **[!UICONTROL Save Rule]**.

1. Testen Sie die Regel, um sicherzustellen, dass sie korrekt funktioniert.

## Varianten

Buy X Get Y Free wird als einzelne Aktion verarbeitet, mit einer _Row total_ Abhängigkeit. Alle Elemente müssen von derselben SKU stammen, um für die Promotion qualifiziert zu sein. Beispiel:

Kaufen Sie X Menge des Produkts aus Kategorie A, erhalten Sie Y Menge des gleichen Produkts kostenlos.

Um das freie Produkt auf die Kategorien A, B und C zu beschränken, stellen Sie die Aktion wie folgt ein:

Wenn ALLE diese Bedingungen ERFÜLLT sind:
Kategorie ist eine der Kategorien A, B, C

Um die freien Elemente aus einer beliebigen Kategorie (A, B oder C) zu begrenzen und Y von SKUs (D123, E123 oder F123) zu erhalten, stellen Sie die Aktion wie folgt ein:

Wenn ALLE diese Bedingungen ERFÜLLT sind:
SKU ist eine von D123, E123, F123

## Maximaler Mengenrabatt

Verwenden Sie die folgende Formel, um den korrekten Wert für den maximalen Mengenrabatt zu ermitteln:

Formel = `(X+Y) * (M/Y)`
Hierbei gilt
`X` = Anzahl der gekauften Artikel
`Y` = Anzahl der freien Artikel
`M` = Maximale Anzahl freier Elemente zulässig

Beispiel:

Kaufen Sie fünf und erhalten Sie zwei kostenlose mit maximal vier kostenlosen Artikeln erlaubt.

    Dabei 
    x = 5
    y = 2
    m = 4
    Maximaler Mengenrabatt = (5+2)*(4/2)=(7)*(2)=14

Kaufen Sie fünf und erhalten Sie drei kostenlose Artikel mit maximal neun kostenlosen Artikeln erlaubt.

    Dabei 
    x = 5
    y = 3
    m = 9
    Maximaler Mengenrabatt = (5+3)*(9/3) = 24

Kaufen Sie 20 und erhalten Sie zwei kostenlose Artikel mit maximal 20 kostenlosen Artikeln erlaubt.

    Dabei
    x = 20
    y = 2
    m = 20
    Maximaler Mengenrabatt = (20+2)*(20/2)=(22)*(10)=220
