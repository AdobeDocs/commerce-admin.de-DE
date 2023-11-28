---
title: Lagerbestellverwaltung
description: Erfahren Sie, wie Kunden ihren Auftragsverlauf im Commerce-Storefront anzeigen und verwalten können.
exl-id: 85d953e6-f5a1-4a5e-a6ef-36b9cf6988bb
feature: Orders, Storefront
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '515'
ht-degree: 0%

---

# Lagerbestellverwaltung

Kunden haben von ihrem Konto aus Zugriff auf alle ihre Bestellungen. Bestellungen können als neue Bestellungen angezeigt, gefiltert, nachverfolgt und erneut gesendet werden. Je nach Status der Bestellung können Kunden ihre Bestellungen, Rechnungen, Sendungen und Erstattungsaufzeichnungen drucken.

## Filtern von Bestellungen

{{b2b-feature}}

Ihre Initialisierung _[!UICONTROL My Orders]_Die Ergebnisse enthalten auch übereinstimmende Bestellungen von untergeordneten Benutzern von allen Websites innerhalb der Commerce-Instanz. Ein Kunde, der mit einem Unternehmenskonto verknüpft ist, kann die Liste der Bestellungen filtern, um schnell Datensätze in den Ergebnissen zu finden. Zum Anzeigen der Filteroptionen klickt der Kunde auf **[!UICONTROL Filter]**, und Klicks **[!UICONTROL Close]**um die Filter auszublenden.

![Meine Bestellungen](./assets/account-dashboard-my-orders-b2b.png){width="700" zoomable="yes"}

| Filter | Beschreibung |
| ------ | ----------- |
| [!UICONTROL SKU or Product Name] | Fügt entweder eine SKU oder einen Produktnamen ein. |
| [!UICONTROL Order Number] | Kann entweder eine vollständige oder eine Teilbestellnummer sein. |
| [!UICONTROL Order Status] | Wählt einen Wert aus der Dropdown-Liste aus, um nach Status zu filtern. |
| [!UICONTROL Invoice Number] | Fügt entweder eine vollständige oder eine Teilrechnung ein. |
| [!UICONTROL Order Date] | Legt ein oder beide Datumsfelder fest, die nach Bestelldatum gefiltert werden sollen. |
| [!UICONTROL Created by] | Filtert Firmenbestellungen durch den Bestellersteller. |
| [!UICONTROL Order Total] | Legt die Werte min, max oder beides fest, um nach Bestellsumme zu filtern. |

## Bestellung anzeigen

Ein Kunde findet die Bestellung in der Liste und klickt auf **[!UICONTROL View Order]**. In der geöffneten Reihenfolge können sie einen der folgenden Schritte ausführen:

![Bestellung anzeigen](./assets/customer-account-order-items-ordered.png){width="700" zoomable="yes"}

### Kürzlich bestellte Produkte anzeigen

Die **[!UICONTROL Recent Orders]** -Block in der Seitenleiste und auf der **[!UICONTROL My Account]** für Kunden, die nach der Bestellung angemeldet sind. Es werden fünf Produkte seit dem letzten Kauf angezeigt.

Der Kunde kann Produkte in den Warenkorb lesen, indem er die Produkte auswählt und auf **[!UICONTROL Add to Cart]**. Sie können auch die letzte Bestellung durch Klicken auf **[!UICONTROL View all]**, der zu der _[!UICONTROL My Account]_und die **[!UICONTROL Recent Orders]**blockieren.

### Druckauftrag

1. Der Kunde klickt auf **[!UICONTROL Print Order]**.

1. Befolgt die Anweisungen im Dialogfeld Drucken , um den Druck abzuschließen.

### Druckrechnungen

1. Im **[!UICONTROL Invoices]** klicken Sie auf einen der folgenden Punkte:

   - **[!UICONTROL Print All Invoices]**

   - **[!UICONTROL Print Invoice]**

   ![Rechnungen](./assets/customer-account-order-invoices.png){width="700" zoomable="yes"}

1. Verwendet das Dialogfeld Drucken , um den Druck abzuschließen.

### Drucksendungen

1. Im **[!UICONTROL Order Shipments]** klicken Sie auf einen der folgenden Punkte:

   - **[!UICONTROL Print All Shipments]**

   - **[!UICONTROL Print Shipment]**

   ![Alle Sendungen drucken](./assets/customer-account-order-shipments.png){width="700" zoomable="yes"}

1. Verwendet das Dialogfeld Drucken , um den Druck abzuschließen.

### Verfolgen von Sendungen

1. Im **[!UICONTROL Order Shipments]** Registerkarte, klicken **[!UICONTROL Track this Shipment]**.

   Alle verfügbaren Tracking-Informationen werden in einem Popup-Fenster angezeigt.

1. Wenn der Kunde bereit ist, klickt er auf **[!UICONTROL Close Window]**.

### Druckrückerstattungen

1. Im **Erstattungen** klicken Sie auf einen der folgenden Punkte:

   - **Alle Erstattungen drucken**

   - **Druckrückerstattung**

   ![Erstattungen](./assets/customer-account-order-refunds.png){width="700" zoomable="yes"}

1. Verwendet das Dialogfeld Drucken , um den Druck abzuschließen.

Für Kunden sind bei der [_Neuanordnung zulassen_](reorders-allow.md) -Konfigurationsoption aktiviert ist.

Ein Kunde kann die Neuanordnungsfunktion für eine bestimmte Bestellung von zwei Seiten aus initiieren:

- Seite &quot;Meine Bestellungen&quot;
- Seite &quot;Auftragsansicht&quot;

## Nachbestellungen

Die _[!UICONTROL Reorder]_-Link in der Liste mit Bestellungen in der Nähe der_[!UICONTROL View]_ -Link.

![Link auf der Seite &quot;Meine Bestellung&quot;neu anordnen](./assets/account-dashboard-reorder.png){width="700" zoomable="yes"}

**1. Fall.** Alle Produkte aus der Bestellung sind zur Neubestellung verfügbar

Der Kunde wird zum Warenkorb umgeleitet und alle Produkte werden zum Warenkorb hinzugefügt.

**2. Fall.** Einige/alle Produkte aus der Bestellung stehen nicht zur Neubestellung zur Verfügung

>[!NOTE]
>
>Es ist möglich, `Not Visible Individually` Produkte.

Die _[!UICONTROL Reorder]_Der Link wird nicht im_[!UICONTROL My Orders]_ und _[!UICONTROL View Order]_Seiten.

![Meine Bestellseite](./assets/account-dashboard-reorder-grid.png){width="700" zoomable="yes"}

>[!TIP]
>
>Wenn der Warenkorb nicht leer ist und der Kunde auf **[!UICONTROL Reorder]** (aus dem [!UICONTROL My Orders] oder [!UICONTROL Order View] ), bleiben die vorhandenen Produkte im Warenkorb mit den hinzugefügten Produkten zur Neuanordnung.
