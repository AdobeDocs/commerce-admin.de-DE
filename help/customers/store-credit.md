---
title: Warenkredit
description: Warenkredit ist ein Betrag, der auf einem Kundenkonto wiederhergestellt wird und zur Zahlung für Käufe oder für Barerstattungen verwendet werden kann.
exl-id: 1fe627dd-5c49-4ff8-85e0-3c987285726d
feature: Customers, Storefront
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 0%

---

# Warenkredit

{{ee-feature}}

Warenkorb-Guthaben ist ein Betrag, der auf einem Kundenkonto wiederhergestellt wird. Kunden können ihre Ladenkredite verwenden, um für Käufe zu bezahlen, und Administratoren können die Ladenkredite für Barerstattungen verwenden. Die Guthaben auf der Geschenkkarte können dem Konto des Kunden gutgeschrieben werden, anstatt den Geschenkkartencode für zukünftige Käufe zu verwenden.

Nachdem eine Bestellung bezahlt und fakturiert wurde, kann die Bestellung oder ein Teil davon zurückerstattet werden ([&#x200B; Gutschrift](../stores-purchase/credit-memo-create.md). Eine Gutschrift unterscheidet sich von einer Rückerstattung, da der Betrag der Gutschrift auf dem Konto des Kunden wiederhergestellt wird, wo er für zukünftige Käufe verwendet werden kann. Manchmal kann eine Rückerstattung gleichzeitig mit der Ausstellung einer Gutschrift gewährt und auf das Guthaben des Kunden im Geschäft angewendet werden. Der Betrag des Speicherguthabens, der auf dem Konto des Kunden verfügbar ist, wird in der Konfiguration angegeben.

>[!NOTE]
>
>Die [_Null Zwischensumme Checkout_](../stores-purchase/zero-subtotal-checkout.md)-Zahlungsmethode muss aktiviert sein, falls die Speichergutschrift die Bestellsumme deckt.

## Kredit-Workflow speichern

1. **Kundenanmeldung** - Der Kunde meldet sich bei seinem Konto an, bevor der Checkout-Prozess gestartet wird.

1. **Store verwenden** - Guthaben Während des [!UICONTROL _Überprüfen und_]) des Checkout-Prozesses wählt der Kunde [!UICONTROL _Store-Guthaben verwenden_] als Zahlungsoption aus. Der verfügbare Saldo wird in Klammern angezeigt. Ist der verfügbare Saldo größer als die Gesamtsumme, werden die anderen Zahlungsmethoden nicht mehr angezeigt.

1. **Gutschrift auf Bestellung angewendet** - Der Betrag der Speichergutschrift, die auf die Bestellung angewendet wird, wird mit den Bestellsummen angezeigt und von der Gesamtsumme abgezogen.

1. **Kundensaldo angepasst** - Der verfügbare Saldo des Kunden wird bei der Bestellung angepasst.
