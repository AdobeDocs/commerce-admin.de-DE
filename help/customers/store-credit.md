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

Nachdem eine Bestellung bezahlt und fakturiert wurde, kann die Bestellung oder ein Teil davon durch [Ausgabe eines Kreditbriefs](../stores-purchase/credit-memo-create.md) zurückerstattet werden. Ein Kreditmemo unterscheidet sich von einer Erstattung, da der Kreditbetrag auf dem Konto des Kunden wiederhergestellt wird, auf dem er für zukünftige Käufe verwendet werden kann. Manchmal kann eine Rückerstattung gleichzeitig erfolgen, wenn ein Kreditmemo ausgestellt und auf den Kundenstand des Guthabens angewendet wird. Der Betrag des Store-Guthabens, der im Konto des Kunden verfügbar ist, wird in der Konfiguration angegeben.

>[!NOTE]
>
>Die Zahlungsmethode [_Null Subtotal Checkout_](../stores-purchase/zero-subtotal-checkout.md) für die Bestellung muss aktiviert sein, falls das Speicherguthaben die Bestellsumme abdeckt.

## Workflow &quot;Gutschriften speichern&quot;

1. **Kundenanmeldung** - Der Kunde meldet sich vor dem Beginn des Checkout-Prozesses mit dem Konto an.

1. **Use Store** - Guthaben Während des Schritts [!UICONTROL _Review &amp; Payments_] des Checkout-Prozesses wählt der Kunde [!UICONTROL _Use Store Credit_] als Zahlungsoption aus. Der verfügbare Saldo wird in Klammern angezeigt. Wenn der verfügbare Restbetrag die Gesamtsumme übersteigt, werden die anderen Zahlungsmethoden nicht mehr angezeigt.

1. **Auf Bestellung angewendeter Guthaben** - Der Betrag des Store-Guthabens, der auf die Bestellung angewendet wird, wird mit den Bestellsummen angezeigt und von der Gesamtsumme abgezogen.

1. **Kundensaldo angepasst** - Der verfügbare Saldo des Kunden wird bei der Bestellung angepasst.
