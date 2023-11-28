---
title: Gespeicherte Zahlungsmethoden
description: Erfahren Sie, wie Kunden gespeicherte Zahlungsmethoden in Ihrem Commerce-Storefront verwenden können.
exl-id: 5e264f84-1891-4ee9-8ebe-55ac9c93ab8c
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---

# Gespeicherte Zahlungsmethoden

Kunden, die Zugriff auf einen sicheren Vault zum Speichern von Zahlungsinformationen haben, können schnell durch den Checkout gehen, ohne ihre Kreditkarteninformationen jedes Mal eingeben zu müssen. Wenn [Sofortiger Kauf](checkout-instant-purchase.md) aktiviert ist, können Kunden den zweistufigen Checkout-Prozess umgehen und die Bestellung von der Produktseite aus platzieren.

Eine Zahlungsmethode, die einen sicheren Vault unterstützt, z. B. [Braintree](braintree.md), ist erforderlich. Wenn ein sicherer Vault in der Zahlungsmethodenkonfiguration aktiviert ist, haben Kunden die Möglichkeit, während des Checkout ihre Kreditkarteninformationen als gespeicherte Zahlungsmethode zu speichern. Kunden können gespeicherte Zahlungsmethoden über ihr Konto-Dashboard verwalten.

![Gespeicherte Zahlungsmethoden](./assets/customer-account-stored-payment-methods.png){width="700" zoomable="yes"}

## Gespeicherte Zahlungsmethode beim Checkout hinzufügen

1. Der Kunde ruft von der Storefront die Detailseite des Produkts auf.

1. Fügt ein Produkt zum Warenkorb hinzu.

1. Fahren Sie mit der Checkout-Seite fort.

1. Schließt die _Versand_ Schritt.

1. Wählt die **[!UICONTROL Braintree Credit Card]** Zahlungsmethode.

1. Fügt Kreditkartendaten ein.

1. Wählt die **[!UICONTROL Save for later use]** aktivieren.

1. Klicks **[!UICONTROL Place Order]**.

Die Methode der gespeicherten Zahlung wird dann im _[!UICONTROL Stored Payment Methods]_im Kunden-Dashboard.

## Gespeicherte Zahlungsmethode löschen

Alle zuvor hinzugefügten gespeicherten Zahlungsmethoden können vom Kunden nicht bearbeitet werden, sie können nur gelöscht werden. Diese Aktion kann nicht rückgängig gemacht werden.

1. In der Seitenleiste seines Kontos wählt der Kunde **[!UICONTROL Stored Payment Methods]**.

1. Findet die Löschung des Zahlungsmethodeneintrags.

1. Klicks **[!UICONTROL Delete]**.

1. Klicken Sie zur Bestätigung der Aktion auf **[!UICONTROL OK]**.
