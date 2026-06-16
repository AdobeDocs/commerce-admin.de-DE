---
title: Neuanordnung von Datensätzen zulassen
description: Erfahren Sie, wie Sie Ihren Kunden Funktionen zur Neuanordnung bereitstellen können.
exl-id: 9fe4c4fb-8596-4fd0-a93b-927ebdfc0c94
feature: Orders, Storefront
TQID: https://experienceleague.adobe.com/comSKludWZnDkDjdZyhi4-9WNAE9scH3dgSce08IyJo
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
source-wordcount: 432
ht-degree: 0%

---

# Neuanordnung von Datensätzen zulassen

Wenn diese Option aktiviert ist, können Neubestellungen direkt über das Kundenkonto oder über die ursprüngliche Bestellung in der _Admin_ vorgenommen werden. Neuanordnungen sind standardmäßig aktiviert.

![Link zur Neuanordnung durch Kunden im Admin-Bereich](./assets/customer-reorder.png){width="700" zoomable="yes"}

## Kriterien für die Aktivierung der Neuanordnung für eine Bestellung

- Die _„Neu anordnen_ zulassen“ muss aktiviert sein.

- Wenn sich die Bestellung im Status `Hold` oder `Payment Review` befindet, ist die Option zur Neuanordnung deaktiviert.

- Wenn eines der Elemente in der Bestellung nicht verfügbar, nicht vorrätig oder deaktiviert ist, ist die Option zur Neuanordnung in der Storefront deaktiviert.

- Ein _Administrator_ kann Artikel auch dann neu anordnen, wenn diese nicht vorrätig oder deaktiviert sind.

## Konfigurieren, um Neubestellungen durch Kunden zuzulassen

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen Sie darunter **[!UICONTROL Sales]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Reorder]** .

   ![Optionen neu anordnen](../configuration-reference/sales/assets/sales-reorder.png){width="600" zoomable="yes"}

1. Legen Sie **[!UICONTROL Allow Reorder]** auf `Yes` fest.

   Diese Einstellung aktiviert die Funktion zum Neuanordnen über das Kundenkonto in der Storefront oder in der Bestellliste in Admin.

1. Klicken Sie auf **[!UICONTROL Save Config]**.

## Neu aus der Storefront bestellen

Ein Kunde kann die Funktion zur Neuanordnung für eine bestimmte Bestellung von zwei Seiten aus starten:

- _Meine Bestellungen_ Seite

- _Bestellansicht_ Seite

### Meine Bestellungen

Die Schaltfläche _Neu anordnen_ wird immer in der Liste mit Bestellungen angezeigt (auch wenn nicht alle Produkte aus der Bestellung zur Neubestellung verfügbar sind).

![Beispiel-Storefront - Seite „Meine Bestellungen“](./assets/my-order-page-view.png){width="700" zoomable="yes"}

**Fall 1.** Alle Produkte aus der Bestellung sind **verfügbar** zur Nachbestellung

Der Benutzer wird zum Warenkorb weitergeleitet, und alle Produkte werden zum Warenkorb hinzugefügt

![Warenkorb](./assets/shopping-cart-page.png){width="700" zoomable="yes"}

**Fall 2.** Einige/alle Produkte aus der Bestellung sind **nicht verfügbar** zur Nachbestellung

>[!NOTE]
>
>Es ist möglich, `Not Visible Individually` Produkte neu zu bestellen.

Die Schaltfläche _Neu anordnen_ wird nicht auf den Seiten _Meine_) und _Bestellung anzeigen_ angezeigt.

![Meine Bestellungen Seite 1](./assets/my-orders-view-page1.png){width="700" zoomable="yes"}

### Seite „Bestellansicht“

**Fall 1.** Alle Produkte aus der Bestellung können nachbestellt werden

Der Benutzer wird zum Warenkorb weitergeleitet, und alle Produkte werden zum Warenkorb hinzugefügt

**Fall 2.** Einige/alle Produkte aus der Bestellung sind **nicht verfügbar** zur Nachbestellung

>[!NOTE]
>
>Es ist möglich, `Not Visible Individually` Produkte neu zu bestellen.

Die Schaltfläche _Neu anordnen_ wird nicht auf den Seiten _Meine_) und _Bestellung anzeigen_ angezeigt.

![Seite mit den Bestelldetails](./assets/order-view-page.png){width="700" zoomable="yes"}

### Warenkorb ist nicht leer

Wenn der Warenkorb nicht leer ist und der Benutzer auf **[!UICONTROL Reorder]** klickt (auf der Seite _Meine Bestellungen_ oder _Bestellansicht_), bleiben die vorhandenen Produkte mit den hinzugefügten Produkten im Warenkorb.

![Elemente neu anordnen](./assets/shopping-cart-view1.png){width="700" zoomable="yes"}

## Über den Administrator neu anordnen

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Suchen Sie die Bestellung und öffnen Sie sie im **[!UICONTROL View]**.

1. Klicken Sie auf **[!UICONTROL Reorder]** , das in der oberen Schaltflächenleiste angezeigt wird.

   ![Auftragsdetails in der Admin](./assets/order-view-admin.png){width="600" zoomable="yes"}

   Nachdem Sie auf **[!UICONTROL Reorder]** geklickt haben, wird die _Neue Bestellung erstellen_ Seite mit Produkten neu anordnen geöffnet.

   ![Neu anordnen](./assets/create-reorder-page.png){width="600" zoomable="yes"}

1. Füllen Sie alle erforderlichen Felder nach Bedarf aus.

1. Um die Bestellung abzusenden, klicken Sie auf **[!UICONTROL Submit Order]**.
