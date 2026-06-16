---
title: '[!UICONTROL My Purchase Orders]'
description: Erfahren Sie mehr über Bestellungen und darüber, wie Unternehmen sie zur Verwaltung ihrer Einkäufe verwenden können.
exl-id: b7348bc8-b874-4642-a372-530883d9d94c
feature: B2B, Companies, Purchase Orders
TQID: https://experienceleague.adobe.com/3Vb9ux3eccHF7GUlNdiKIkc12vLFNJv9R3Rkz81ch4M
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 474
ht-degree: 0%

---

# [!UICONTROL My Purchase Orders]

Wenn Bestellungen [für ein Unternehmen aktiviert) &#x200B;](purchase-order-flow.md), wird jede Bestellung für einen Kunden, der bei einem Firmenbenutzerkonto angemeldet ist, automatisch als Bestellung (Bestellung) erstellt. Firmenbenutzer mit den erforderlichen Berechtigungen können von ihnen erstellte Bestellungen zusammen mit den von untergeordneten Benutzern erstellten Bestellungen erstellen, bearbeiten und löschen.

![Meine Bestellungen](./assets/account-dashboard-my-purchase-orders.png){width="700" zoomable="yes"}

>[!NOTE]
>
>Bestellungen erstellen eine _Momentaufnahme_ der Artikelpreise, Rabatte und Versandpreise zum Zeitpunkt der Auftragserstellung. Wenn sich der Preis eines Artikels nach der Erstellung der Bestellung ändert, wird der ursprüngliche Preis verwendet.

## Bestellungen verwalten

Auf der Seite _Bestellung anzeigen_ kann der Kunde die Bestellung je nach seinen [Rollenberechtigungen](account-company-roles-permissions.md) verwalten.

- Um die Bestellung anzuzeigen, klicken Sie auf **[!UICONTROL View]**.
- Um Kommentare zur Bestellung anzuzeigen, klicken Sie auf die Registerkarte **[!UICONTROL Comments]** .
- Um einen vollständigen Auftragsverlauf anzuzeigen, klicken Sie auf die Registerkarte **[!UICONTROL History Log]** .

>[!IMPORTANT]
>
>Wenn ein Artikel in einer Bestellung nicht vorrätig ist oder nicht genügend Menge verfügbar ist, tritt beim Konvertieren der Bestellung in eine tatsächliche Bestellung ein Fehler auf. Wenn Nachbestellungen aktiviert sind, wird die Bestellung normal verarbeitet.

## Neue Bestellung aus vorhandener Bestellung

Wenn der Kunde über eine bestehende Bestellung verfügt und neue Artikel hinzufügen möchte, kann er eine doppelte Bestellung mit neuen Produkten erstellen, die der neuen Bestellung hinzugefügt werden. Der Kunde führt die folgenden Schritte aus:

1. Auf der _Meine Bestellung_ findet der Kunde die Bestellung und klickt auf den **[!UICONTROL View]** Link.

1. Der Kunde klickt auf **[!UICONTROL Add Items to Shopping Cart]**.

   Die Seite „Warenkorb“ wird mit allen aufgelisteten Artikeln geöffnet.

1. Ergänzt oder ändert die Seite.

1. (Optional) Verwendet die **[!UICONTROL Custom Reference Number]**, um der Bestellung eine interne Rechnungs-/Bestellnummer hinzuzufügen.

1. Folgt dem normalen Checkout-Workflow und klickt **[!UICONTROL Place Purchase Order]**.

Wenn sich Artikel im Warenkorb befinden, wenn auf _[!UICONTROL Add Items to Shopping Cart]_&#x200B;geklickt wird, zeigt das System ein Dialogfeld an. In diesem Dialogfeld können sie zwischen dem Zusammenführen der Artikel im Warenkorb und den neuen Artikeln oder dem Ersetzen der Artikel im Warenkorb durch die Artikel in der Bestellung wählen.

Die ursprüngliche Bestellung kann geschlossen werden, wenn sie nicht mehr benötigt wird.

## Bestellgenehmigungen

Für einen Kunden, der basierend auf der Unternehmensstruktur oder der zugewiesenen Unternehmensrolle als genehmigende Person bestimmt ist, wird auf der _[!UICONTROL My Purchase Orders]_-Dashboard-Seite die Registerkarte **[!UICONTROL Requires My Approval]**&#x200B;angezeigt. Der Kunde klickt auf diese Registerkarte, um die Bestellungen zu überprüfen, die auf ihre Genehmigung warten. Der Zähler zeigt an, wie viele Aufträge auf Genehmigung warten.

Nachdem der Genehmiger auf **[!UICONTROL View]** für eine Bestellung geklickt und die Details geprüft hat, kann er auf **[!UICONTROL Approve]** oder **[!UICONTROL Reject]** klicken.

### Massenvalidierung/-ablehnung

Ab Adobe Commerce 2.4.1 können genehmigende Personen mehrere Bestellungen gleichzeitig genehmigen oder ablehnen.

1. Klicken Sie auf der Seite _[!UICONTROL My Purchase Order]_&#x200B;auf die Registerkarte **[!UICONTROL Requires My Approval]**.

1. Aktivieren Sie das Kontrollkästchen für jede Bestellung, die genehmigt oder abgelehnt werden soll.

1. Klicks **[!UICONTROL Approve Selected]** oder **[!UICONTROL Reject Selected]**.

Ein Kunde kann nur die Bestellungen auswählen, deren Status eine Aktion zulässt. Firmenadministratoren können für alle aktiven Bestellungen in ihrem Unternehmen Massengenehmigungen oder Ablehnungen vornehmen.
