---
title: Neuberechtigungen zulassen
description: Erfahren Sie, wie Sie Ihren Kunden Umstellungsfunktionen bereitstellen.
exl-id: 9fe4c4fb-8596-4fd0-a93b-927ebdfc0c94
feature: Orders, Storefront
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 0%

---

# Neuberechtigungen zulassen

Wenn diese Option aktiviert ist, können Neubestellungen direkt über das Kundenkonto oder über die ursprüngliche Bestellung im _Admin_. Die Neuanordnung ist standardmäßig aktiviert.

![Link zur Neuanordnung des Kunden in der Admin-Konsole](./assets/customer-reorder.png){width="700" zoomable="yes"}

## Kriterien für die Neuanordnung, die für eine Bestellung aktiviert werden sollen

- Die _Neuanordnung zulassen_ -Konfigurationsoption aktiviert sein.

- Wenn die Bestellung in `Hold` oder `Payment Review` -Status, ist die Option &quot;Neu anordnen&quot;deaktiviert.

- Wenn eines der Elemente in der Reihenfolge nicht verfügbar, nicht vorrätig oder deaktiviert ist, wird die Option &quot;Neu anordnen&quot;im Storefront deaktiviert.

- Ein _Admin_ kann auch dann neu angeordnet werden, wenn eines der Elemente nicht vorrätig oder deaktiviert ist.

## Konfigurieren, um Neubestellungen von Kunden zuzulassen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen **[!UICONTROL Sales]** darunter.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Reorder]** Abschnitt.

   ![Optionen neu anordnen](../configuration-reference/sales/assets/sales-reorder.png){width="600" zoomable="yes"}

1. Satz **[!UICONTROL Allow Reorder]** nach `Yes`.

   Diese Einstellung ermöglicht die Neuanordnungsfunktion über das Kundenkonto in der Storefront oder der Liste der Bestellungen in der Admin-Konsole.

1. Klicken **[!UICONTROL Save Config]**.

## Von der Storefront neu anordnen

Ein Kunde kann die Neuanordnungsfunktion für eine bestimmte Bestellung von zwei Seiten aus initiieren:

- _Meine Bestellungen_ page

- _Bestellansicht_ page

### Meine Bestellungen

Die _Neu anordnen_ -Schaltfläche wird immer in der Liste mit Bestellungen angezeigt (auch wenn nicht alle Produkte der Bestellung zur Neubestellung verfügbar sind).

![Beispiel-Storefront - Seite &quot;Meine Bestellungen&quot;](./assets/my-order-page-view.png){width="700" zoomable="yes"}

**1. Fall.** Alle Produkte aus der Bestellung sind **available** für Neuanordnung

Der Benutzer wird zum Warenkorb umgeleitet und alle Produkte werden zum Warenkorb hinzugefügt.

![Warenkorb](./assets/shopping-cart-page.png){width="700" zoomable="yes"}

**2. Fall.** Einige/alle Produkte aus der Bestellung sind **nicht verfügbar** für Neuanordnung

>[!NOTE]
>
>Es ist möglich, `Not Visible Individually` Produkte.

Die _Neu anordnen_ -Schaltfläche wird nicht auf der _Meine Bestellungen_ und _Bestellung anzeigen_ Seiten.

![Meine Bestellungen Seite 1](./assets/my-orders-view-page1.png){width="700" zoomable="yes"}

### Bestellseite

**1. Fall.** Alle Produkte aus der Bestellung sind zur Neubestellung verfügbar

Der Benutzer wird zum Warenkorb umgeleitet und alle Produkte werden zum Warenkorb hinzugefügt.

**2. Fall.** Einige/alle Produkte aus der Bestellung sind **nicht verfügbar** für Neuanordnung

>[!NOTE]
>
>Es ist möglich, `Not Visible Individually` Produkte.

Die _Neu anordnen_ -Schaltfläche wird nicht auf der _Meine Bestellungen_ und _Bestellung anzeigen_ Seiten.

![Bestelldetailseite](./assets/order-view-page.png){width="700" zoomable="yes"}

### Der Warenkorb ist nicht leer

Wenn der Warenkorb nicht leer ist und der Benutzer auf **[!UICONTROL Reorder]** (aus dem _Meine Bestellungen_  oder _Bestellansicht_ ), bleiben die vorhandenen Produkte im Warenkorb mit den hinzugefügten Produkten zur Neuanordnung.

![Elemente neu anordnen](./assets/shopping-cart-view1.png){width="700" zoomable="yes"}

## Von Admin neu anordnen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Suchen Sie die Bestellung und öffnen Sie sie in **[!UICONTROL View]** -Modus.

1. Klicks **[!UICONTROL Reorder]** wird in der oberen Schaltflächenleiste angezeigt.

   ![Bestelldetails in der Admin-Konsole](./assets/order-view-admin.png){width="600" zoomable="yes"}

   Nachdem Sie auf **[!UICONTROL Reorder]**, die _Neue Bestellung erstellen_ Seite mit Produkten zur Neuanordnung geöffnet.

   ![Neuanordnung erstellen](./assets/create-reorder-page.png){width="600" zoomable="yes"}

1. Füllen Sie nach Bedarf alle erforderlichen Felder aus.

1. Um die Bestellung zu senden, klicken Sie auf **[!UICONTROL Submit Order]**.
