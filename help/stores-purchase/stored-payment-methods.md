---
title: Gespeicherte Zahlungsmethoden
description: Erfahren Sie, wie Kunden gespeicherte Zahlungsmethoden in Ihrer Commerce-Storefront verwenden können.
exl-id: 5e264f84-1891-4ee9-8ebe-55ac9c93ab8c
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---

# Gespeicherte Zahlungsmethoden

Kunden mit Zugriff auf einen sicheren Tresor zur Speicherung von Zahlungsinformationen können den Checkout beschleunigen, ohne jedes Mal ihre Kreditkarteninformationen einzugeben. Wenn [Sofortkauf](checkout-instant-purchase.md) aktiviert ist, können Kunden den zweistufigen Checkout-Prozess umgehen und die Bestellung über die Produktseite aufgeben.

Eine Zahlungsmethode, die einen sicheren Tresor unterstützt, z. B. [Braintree](braintree.md), ist erforderlich. Wenn in der Konfiguration der Zahlungsmethode ein sicherer Tresor aktiviert ist, haben Kunden während des Checkouts die Möglichkeit, ihre Kreditkarteninformationen als gespeicherte Zahlungsmethode zu speichern. Kunden können gespeicherte Zahlungsmethoden über ihr Konto-Dashboard verwalten.

![Gespeicherte Zahlungsmethoden](./assets/customer-account-stored-payment-methods.png){width="700" zoomable="yes"}

## Gespeicherte Zahlungsmethode an der Kasse hinzufügen

1. Von der Storefront aus navigiert der Kunde zur Detailseite des Produkts.

1. Fügt Produkt zum Warenkorb hinzu.

1. Wechselt zur Kasse.

1. Schließt den _Versand_ ab.

1. Wählt die **[!UICONTROL Braintree Credit Card]** Zahlungsmethode aus.

1. Füllen Sie Kreditkartendaten aus.

1. Aktiviert das Kontrollkästchen **[!UICONTROL Save for later use]** .

1. Klicks **[!UICONTROL Place Order]**.

Die gespeicherte Zahlungsmethode wird dann auf der Registerkarte _[!UICONTROL Stored Payment Methods]_&#x200B;des Kunden-Dashboards angezeigt.

## Löschen einer gespeicherten Zahlungsmethode

Zuvor hinzugefügte, gespeicherte Zahlungsmethoden können vom Kunden nicht bearbeitet werden, sondern nur gelöscht werden. Diese Aktion kann nicht rückgängig gemacht werden.

1. In der Seitenleiste seines Kontos wählt der Kunde **[!UICONTROL Stored Payment Methods]** aus.

1. Sucht den zu löschenden Zahlungsmethodeneintrag.

1. Klicks **[!UICONTROL Delete]**.

1. Um die Aktion zu bestätigen, klicken Sie auf **[!UICONTROL OK]**.
