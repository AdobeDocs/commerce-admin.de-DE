---
title: Reihenfolge zum Abbrechen zulassen
description: Erfahren Sie, wie Sie Ihren Kunden Funktionen zum Abbrechen bereitstellen.
feature: Orders, Storefront
exl-id: 5a8ef668-f929-4188-8574-0bccdd076f3e
source-git-commit: a9d1dc4fe50e98f0f1dfc8ec204930e2cc885d6e
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 0%

---

# Reihenfolge zum Abbrechen zulassen

Wenn diese Option aktiviert ist, können Sie eine Bestellung direkt über das Kundenkonto stornieren. Abbrechen ist standardmäßig deaktiviert.

## Kriterien für die Stornierung, die für eine Bestellung aktiviert werden soll

- Die Konfigurationsoption _Reihenfolge abbrechen zulassen_ muss aktiviert sein.

- Wenn die Reihenfolge den Status `Hold`, `Canceled`, `Complete` oder `Closed` aufweist, ist die Option zum Abbrechen auf der Storefront deaktiviert.

- Wenn eines der Artikel in der Bestellung versandt wurde, ist die Option &quot;Abbrechen&quot;auf der Storefront deaktiviert.

- Wenn ein Artikel bezahlt wurde, wird die Option &quot;Abbrechen&quot;aktiviert und die Rückerstattung für diesen Artikel erstellt.

- Wenn die Bestellung den Status `Pending` oder `Processing` aufweist, ist die Option zum Abbrechen auf der Storefront aktiviert.

## Konfigurieren, um das Abbrechen von Kundendaten zuzulassen und die Abbruchsgründe anzupassen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Eintrag **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Sales]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Order cancellation]** .

   ![Bestellabbruchsoptionen](../configuration-reference/sales/assets/sales-order-cancellation.png){width="600" zoomable="yes"}

1. Setzen Sie **[!UICONTROL Order cancellation through GraphQL]** auf `Yes`.

   Diese Einstellung ermöglicht die Funktion zum Abbrechen vom Kundenkonto auf der Storefront.

1. In der **[!UICONTROL Order Order cancellation reasons]** können Sie einen beliebigen Löschgrund hinzufügen, löschen oder ändern.

   Mit dieser Einstellung werden dem Kunden auf der Storefront Stornierungsgründe angezeigt, wenn er eine Bestellung storniert.
Achten Sie darauf, mindestens einen Grund angegeben zu haben.

1. Klicken Sie auf **[!UICONTROL Save Config]**.

## Abbrechen über die Storefront

Ein Kunde kann die Funktion zum Abbrechen für eine bestimmte Bestellung von drei Seiten aus initiieren:

- Seite _Meine Bestellungen_

- Seite _Bestellansicht_

- Seite _Mein Konto_

### Meine Bestellungen

Die Schaltfläche _Bestellung abbrechen_ wird auf der Seite &quot;Meine Bestellungen&quot;angezeigt, wenn die Bestellung storniert werden kann.

![Beispiel-Storefront - Seite &quot;Meine Bestellungen&quot;](./assets/my-order-page-view-cancel.png){width="700" zoomable="yes"}

### Bestellseite

Die Schaltfläche _Reihenfolge abbrechen_ wird auf der Seite &quot;Bestellung anzeigen&quot;angezeigt, wenn die Bestellung storniert werden kann.

![Bestelldetailseite](./assets/order-view-page-cancel.png){width="700" zoomable="yes"}

### Mein Konto

Die Schaltfläche _Bestellung abbrechen_ wird im Abschnitt &quot;Letzte Bestellungen&quot;auf der Seite &quot;Mein Konto&quot;angezeigt, wenn die Bestellung storniert werden kann.

![Seite &quot;Mein Konto&quot;](./assets/my-account-page-view-cancel.png){width="700" zoomable="yes"}
