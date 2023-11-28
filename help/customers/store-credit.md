---
title: Store-Gutschrift
description: Der Kreditbetrag im Geschäft ist ein Betrag, der auf ein Kundenkonto zurückgeführt wird und zur Bezahlung von Käufen oder Barerstattungen verwendet werden kann.
exl-id: 1fe627dd-5c49-4ff8-85e0-3c987285726d
feature: Customers, Storefront
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 0%

---

# Store-Gutschrift

{{ee-feature}}

Die Gutschrift im Store ist ein Betrag, der in einem Kundenkonto wiederhergestellt wird. Kunden können ihr Guthaben im Geschäft verwenden, um Käufe zu bezahlen, und Administratoren können Guthaben im Geschäft für Barerstattungen verwenden. Geschenkgutscheine können dem Konto des Kunden gutgeschrieben werden, anstatt den Geschenkkartencode für zukünftige Käufe zu verwenden.

Nach Bezahlung und Rechnungsstellung kann die Bestellung oder ein Teil davon durch [Angeben eines Kreditprotokolls](../stores-purchase/credit-memo-create.md). Ein Kreditmemo unterscheidet sich von einer Erstattung, da der Kreditbetrag auf dem Konto des Kunden wiederhergestellt wird, auf dem er für zukünftige Käufe verwendet werden kann. Manchmal kann eine Rückerstattung gleichzeitig erfolgen, wenn ein Kreditmemo ausgestellt und auf den Kundenstand des Guthabens angewendet wird. Der Betrag des Store-Guthabens, der im Konto des Kunden verfügbar ist, wird in der Konfiguration angegeben.

>[!NOTE]
>
>Die [_Null Zwischensumme Checkout_](../stores-purchase/zero-subtotal-checkout.md) Die Zahlungsmethode muss aktiviert werden, wenn der Kundenkredit die Bestellsumme abdeckt.

## Workflow &quot;Gutschriften speichern&quot;

1. **Kundenanmeldung** - Der Kunde meldet sich vor Beginn des Checkout-Prozesses mit dem Konto an.

1. **Store verwenden** - Gutschrift während der [!UICONTROL _Überprüfung und Zahlungen_] Schritt des Checkout-Prozesses, wählt der Kunde [!UICONTROL _Store-Guthaben verwenden_] als Zahlungsoption. Der verfügbare Saldo wird in Klammern angezeigt. Wenn der verfügbare Restbetrag die Gesamtsumme übersteigt, werden die anderen Zahlungsmethoden nicht mehr angezeigt.

1. **Auf Bestellung angewendeter Kredit** - Der Betrag des Store-Guthabens, der auf die Bestellung angewendet wird, wird mit den Bestellsummen angezeigt und von der Gesamtsumme abgezogen.

1. **Kundensaldo angepasst** - Der verfügbare Saldo des Kunden wird bei der Bestellung angepasst.
