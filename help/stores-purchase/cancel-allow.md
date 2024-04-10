---
title: Auftrag stornieren zulassen
description: Erfahren Sie, wie Sie Ihren Kunden Abbruchfunktionen bereitstellen können.
feature: Orders, Storefront
source-git-commit: 613c081c02dd9b5e55de37dccd021af4e429d424
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 0%

---


# Auftrag stornieren zulassen

Wenn diese Option aktiviert ist, können Sie eine Bestellung direkt über das Konto des Kunden stornieren. Abbrechen ist standardmäßig deaktiviert.

## Kriterien für die Stornierung, die für eine Bestellung aktiviert werden sollen

- Die _Bestellung stornieren zulassen_ Die Konfigurationsoption muss aktiviert sein.

- Wenn die Bestellung in `Hold`, `Canceled`, `Complete`, oder `Closed` Status festgelegt ist, ist die Option Abbrechen in der Storefront deaktiviert.

- Wenn ein Artikel in der Bestellung versendet wurde, ist die Option „Abbrechen“ in der Storefront deaktiviert.

- Wenn ein Artikel bezahlt wurde, ist die Option „Stornieren“ aktiviert und die Rückerstattung wird für diesen Artikel erstellt.

- Wenn die Bestellung in `Pending` oder `Processing` Status festgelegt ist, wird die Option Abbrechen in der Storefront aktiviert.

## Konfigurieren Sie so, dass Kunden stornieren können und die Stornierungsgründe angepasst werden können

1. Auf der _Admin_ Seitenleiste, zu gehen **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich . **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Sales]**.

1. Expand ![Erweiterungsauswahl](../assets/icon-display-expand.png) Die **[!UICONTROL Order cancellation]** -Abschnitt.

   ![Optionen für Auftragsstornierungen](../configuration-reference/sales/assets/sales-order-cancellation.png){width="600" zoomable="yes"}

1. set **[!UICONTROL Order cancellation through GraphQL]** bis `Yes`.

   Mit dieser Einstellung wird die Abbruchfunktion für das Kundenkonto in der Storefront aktiviert.

1. In der **[!UICONTROL Order Order cancellation reasons]** Sie können einen beliebigen Abbruchgrund hinzufügen, löschen oder ändern.

   Mit dieser Einstellung werden Stornierungsgründe dem Kunden in der Storefront angezeigt, wenn er eine Bestellung storniert.
Stellen Sie sicher, dass Sie mindestens einen Grund angegeben haben.

1. Klick **[!UICONTROL Save Config]**.

## Aus der Storefront abbrechen

Ein Kunde kann die Abbruchfunktion für eine bestimmte Bestellung von drei Seiten aus starten:

- _Meine Bestellungen_ Seite

- _Bestellansicht_ Seite

- _Mein Konto_ Seite

### Meine Bestellungen

Die _Bestellung stornieren_ Die Schaltfläche „Meine Bestellungen“ wird auf der Seite „Meine Bestellungen“ angezeigt, wenn die Bestellung storniert werden kann.

![Beispiel einer Storefront - Seite „Meine Bestellungen“](./assets/my-order-page-view-cancel.png){width="700" zoomable="yes"}

### Bestellansichtsseite

Die _Bestellung stornieren_ auf der Seite Bestellung anzeigen angezeigt wird, wenn die Bestellung storniert werden kann.

![Seite mit den Bestelldetails](./assets/order-view-page-cancel.png){width="700" zoomable="yes"}

### Mein Konto

Die _Bestellung stornieren_ Die Schaltfläche „Letzte Bestellungen“ wird auf der Seite Mein Konto angezeigt, wenn die Bestellung storniert werden kann.

![Seite Mein Konto](./assets/my-account-page-view-cancel.png){width="700" zoomable="yes"}


