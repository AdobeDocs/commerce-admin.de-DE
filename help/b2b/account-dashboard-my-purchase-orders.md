---
title: "[!UICONTROL My Purchase Orders]"
description: Erfahren Sie mehr über Bestellungen und wie Unternehmen diese zur Verwaltung ihrer Einkäufe verwenden können.
exl-id: b7348bc8-b874-4642-a372-530883d9d94c
feature: B2B, Companies, Purchase Orders
source-git-commit: c94d4e8d13c32c1c1b1d37440fdb953c8527b76c
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 0%

---

# [!UICONTROL My Purchase Orders]

Wenn Bestellungen für ein Unternehmen ](purchase-order-flow.md) aktiviert sind, wird jede Bestellung eines Kunden, der bei einem Unternehmensbenutzerkonto angemeldet ist, automatisch als Bestellung (Bestellformular) erstellt. [ Unternehmensbenutzer mit den erforderlichen Berechtigungen können von ihnen erstellte POs sowie von ihnen erstellte POs erstellen, bearbeiten und löschen.

![Meine Kaufaufträge](./assets/account-dashboard-my-purchase-orders.png){width="700" zoomable="yes"}

>[!NOTE]
>
>Die Bestelldaten erzeugen einen _Schnappschuss_ der Artikelpreise, Rabatte und Versandpreise zum Zeitpunkt der Bestellerstellung. Wenn sich der Preis eines Artikels nach der Erstellung des Bestellformulars ändert, wird der ursprüngliche Preis verwendet.

## Verwalten von Kaufaufträgen

Auf der Seite _Bestellung anzeigen_ kann der Kunde die Bestellung je nach seinen [Rollenberechtigungen](account-company-roles-permissions.md) verwalten.

- Um die Bestellung anzuzeigen, klicken Sie auf &quot;**[!UICONTROL View]**&quot;.
- Um Kommentare zum Bestellformular anzuzeigen, klicken Sie auf die Registerkarte **[!UICONTROL Comments]** .
- Um einen vollständigen Bestellverlauf anzuzeigen, klicken Sie auf die Registerkarte **[!UICONTROL History Log]** .

>[!IMPORTANT]
>
>Wenn ein Artikel in einer Bestellung bei der Konvertierung in eine tatsächliche Bestellung nicht vorrätig ist oder nicht über eine ausreichende Menge verfügt, tritt ein Fehler auf. Wenn Rückstände aktiviert sind, wird die Bestellung normal verarbeitet.

## Neue Bestellung aus bestehender Bestellung

Wenn der Kunde über eine bestehende Bestellung verfügt und neue Artikel hinzufügen möchte, kann er eine doppelte Bestellung mit neuen Produkten generieren, die dem neuen Bestellformular hinzugefügt werden. Der Kunde führt die folgenden Schritte aus:

1. Auf der Seite _My Purchase Order_ sucht der Kunde die Bestellung und klickt auf den Link **[!UICONTROL View]** .

1. Der Kunde klickt auf **[!UICONTROL Add Items to Shopping Cart]**.

   Die Seite &quot;Warenkorb&quot;wird mit allen aufgelisteten Elementen geöffnet.

1. Macht alle Ergänzungen oder Änderungen.

1. (Optional) Verwendet den **[!UICONTROL Custom Reference Number]** , um der Bestellung eine interne Rechnungsnummer/Bestellnummer hinzuzufügen.

1. Folgt dem normalen Checkout-Workflow und klickt auf **[!UICONTROL Place Purchase Order]**.

Wenn Artikel in ihrem Warenkorb sind, wenn sie auf _[!UICONTROL Add Items to Shopping Cart]_klicken, zeigt das System ein Dialogfeld an. In diesem Dialogfeld können Sie auswählen, ob Sie die Artikel des Warenkorbs mit den neuen Artikeln zusammenführen oder die Artikel im Warenkorb durch die Artikel im Bestellformular ersetzen möchten.

Die ursprüngliche Bestellung kann geschlossen werden, wenn sie nicht mehr benötigt wird.

## Bestellgenehmigungen

Für einen Kunden, der auf der Grundlage der Unternehmensstruktur oder der zugewiesenen Unternehmensrolle als Genehmiger bestimmt wurde, wird auf der Dashboard-Seite &quot;_[!UICONTROL My Purchase Orders]_&quot;die Registerkarte &quot;**[!UICONTROL Requires My Approval]**&quot;angezeigt. Der Kunde klickt auf diesen Tab, um die POs zu überprüfen, die auf ihre Genehmigung warten. Der Zähler zeigt an, wie viele Bestellungen auf die Validierung warten.

Nachdem der Genehmiger für eine Bestellung auf **[!UICONTROL View]** geklickt und die Details überprüft hat, kann er auf **[!UICONTROL Approve]** oder **[!UICONTROL Reject]** klicken.

### Massengenehmigung/Zurückweisung

Ab Adobe Commerce 2.4.1 können Genehmiger mehrere Bestellungen gleichzeitig genehmigen oder ablehnen.

1. Klicken Sie auf der Seite _[!UICONTROL My Purchase Order]_auf die Registerkarte **[!UICONTROL Requires My Approval]**.

1. Aktivieren Sie das Kontrollkästchen für jede Bestellung, die genehmigt oder abgelehnt werden soll.

1. Klicks **[!UICONTROL Approve Selected]** oder **[!UICONTROL Reject Selected]**.

Ein Kunde kann nur die Bestellungen mit einem Status auswählen, der eine Aktion zulässt. Unternehmensadministratoren können für aktive Bestellungen in ihrem Unternehmen Massengenehmigungen oder Ablehnungen vornehmen.
