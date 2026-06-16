---
title: Warenkredit
description: Warenkredit ist ein Betrag, der auf einem Kundenkonto wiederhergestellt wird und zur Zahlung für Käufe oder für Barerstattungen verwendet werden kann.
exl-id: 1fe627dd-5c49-4ff8-85e0-3c987285726d
feature: Customers, Storefront
TQID: https://experienceleague.adobe.com/kG-y-O2Yh-h1ct-oCwqylZFvS2FOCXFPD6qVIkKrpbg
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 291
ht-degree: 0%

---

# Warenkredit

{{ee-feature}}

Warenkorb-Guthaben ist ein Betrag, der auf einem Kundenkonto wiederhergestellt wird. Kunden können ihre Ladenkredite verwenden, um für Käufe zu bezahlen, und Administratoren können die Ladenkredite für Barerstattungen verwenden. Die Guthaben auf der Geschenkkarte können dem Konto des Kunden gutgeschrieben werden, anstatt den Geschenkkartencode für zukünftige Käufe zu verwenden.

Nachdem eine Bestellung bezahlt und fakturiert wurde, kann die Bestellung oder ein Teil davon zurückerstattet werden ([ Gutschrift](../stores-purchase/credit-memo-create.md). Eine Gutschrift unterscheidet sich von einer Rückerstattung, da der Betrag der Gutschrift auf dem Konto des Kunden wiederhergestellt wird, wo er für zukünftige Käufe verwendet werden kann. Manchmal kann eine Rückerstattung gleichzeitig mit der Ausstellung einer Gutschrift gewährt und auf das Guthaben des Kunden im Geschäft angewendet werden. Der Betrag des Speicherguthabens, der auf dem Konto des Kunden verfügbar ist, wird in der Konfiguration angegeben.

>[!NOTE]
>
>Die [_Null Zwischensumme Checkout_](../stores-purchase/zero-subtotal-checkout.md)-Zahlungsmethode muss aktiviert sein, falls die Speichergutschrift die Bestellsumme deckt.

## Kredit-Workflow speichern

1. **Kundenanmeldung** - Der Kunde meldet sich bei seinem Konto an, bevor der Checkout-Prozess gestartet wird.

1. **Store verwenden** - Guthaben Während des [!UICONTROL _Überprüfen und_]) des Checkout-Prozesses wählt der Kunde [!UICONTROL _Store-Guthaben verwenden_] als Zahlungsoption aus. Der verfügbare Saldo wird in Klammern angezeigt. Ist der verfügbare Saldo größer als die Gesamtsumme, werden die anderen Zahlungsmethoden nicht mehr angezeigt.

1. **Gutschrift auf Bestellung angewendet** - Der Betrag der Speichergutschrift, die auf die Bestellung angewendet wird, wird mit den Bestellsummen angezeigt und von der Gesamtsumme abgezogen.

1. **Kundensaldo angepasst** - Der verfügbare Saldo des Kunden wird bei der Bestellung angepasst.
