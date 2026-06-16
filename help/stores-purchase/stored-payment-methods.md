---
title: Gespeicherte Zahlungsmethoden
description: Erfahren Sie, wie Kunden gespeicherte Zahlungsmethoden in Ihrer Commerce-Storefront verwenden können.
exl-id: 5e264f84-1891-4ee9-8ebe-55ac9c93ab8c
feature: Payments
TQID: https://experienceleague.adobe.com/dYEYXgEIp83AKhHepfDQVNR9YBUQGbJ7B2zu8UTM-I4
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 226
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
