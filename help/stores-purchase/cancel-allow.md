---
title: Auftrag stornieren zulassen
description: Erfahren Sie, wie Sie Ihren Kunden Abbruchfunktionen bereitstellen können.
feature: Orders, Storefront
exl-id: 5a8ef668-f929-4188-8574-0bccdd076f3e
TQID: https://experienceleague.adobe.com/a0jMKgF4a0qXUe15oT2syai6-kGSegU1BX56PO9SSKs
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 291
ht-degree: 0%

---

# Auftrag stornieren zulassen

Wenn diese Option aktiviert ist, können Sie eine Bestellung direkt über das Konto des Kunden stornieren. Abbrechen ist standardmäßig deaktiviert.

## Kriterien für die Stornierung, die für eine Bestellung aktiviert werden sollen

- Die _„Bestellung stornieren_ muss aktiviert sein.

- Wenn sich die Bestellung im Status `Hold`, `Canceled`, `Complete` oder `Closed` befindet, ist die Option Abbrechen in der Storefront deaktiviert.

- Wenn ein Artikel in der Bestellung versendet wurde, ist die Option „Abbrechen“ in der Storefront deaktiviert.

- Wenn ein Artikel bezahlt wurde, ist die Stornierungsoption aktiviert und die Rückerstattung wird für diesen Artikel erstellt.

- Wenn sich die Bestellung im Status `Pending` oder `Processing` befindet, wird die Option Abbrechen in der Storefront aktiviert.

## Konfigurieren Sie so, dass Kunden Stornierungen zulassen und die Stornierungsgründe anpassen können

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Sales]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Order cancellation]** .

   ![Stornierungsoptionen für Bestellungen](../configuration-reference/sales/assets/sales-order-cancellation.png){width="600" zoomable="yes"}

1. Legen Sie **[!UICONTROL Order cancellation through GraphQL]** auf `Yes` fest.

   Mit dieser Einstellung wird die Funktion zum Abbrechen für das Kundenkonto in der Storefront aktiviert.

1. In der **[!UICONTROL Order Order cancellation reasons]** können Sie einen beliebigen Abbruchsgrund hinzufügen, löschen oder ändern.

   Mit dieser Einstellung werden Stornierungsgründe dem Kunden in der Storefront angezeigt, wenn er eine Bestellung storniert.
Stellen Sie sicher, dass Sie mindestens einen Grund angegeben haben.

1. Klicken Sie auf **[!UICONTROL Save Config]**.

## Aus der Storefront abbrechen

Ein Kunde kann die Abbruchfunktion für eine bestimmte Bestellung von drei Seiten aus starten:

- _Meine Bestellungen_ Seite

- _Bestellansicht_ Seite

- _Mein Konto_ Seite

### Meine Bestellungen

Die Schaltfläche _Bestellung abbrechen_ wird auf der Seite Meine Bestellungen angezeigt, wenn die Bestellung storniert werden kann.

![Beispiel-Storefront - Seite „Meine Bestellungen“](./assets/my-order-page-view-cancel.png){width="700" zoomable="yes"}

### Seite „Bestellansicht“

Die Schaltfläche _Bestellung abbrechen_ wird auf der Seite Bestellung anzeigen angezeigt, wenn die Bestellung storniert werden kann.

![Seite mit den Bestelldetails](./assets/order-view-page-cancel.png){width="700" zoomable="yes"}

### Mein Konto

Die Schaltfläche _Bestellung abbrechen_ wird im Abschnitt Letzte Bestellungen auf der Seite Mein Konto angezeigt, wenn die Bestellung storniert werden kann.

![Seite Mein Konto](./assets/my-account-page-view-cancel.png){width="700" zoomable="yes"}
