---
title: PayPal-Abrechnungsvereinbarungen
description: Erfahren Sie, wie Sie PayPal-Abrechnungsvereinbarungen und eine Zahlungsmethode in Ihrem Geschäft unterstützen können.
exl-id: b0800b41-816a-4c48-a54d-41ddc1d586ce
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 0%

---

# PayPal-Abrechnungsvereinbarungen

Um den Checkout-Prozess zu vereinfachen, können Kunden mit PayPal als Zahlungsdienstleister einen Abrechnungsvertrag schließen. Beim Checkout wählt der Kunde den Abrechnungsvertrag als Zahlungsmethode aus. Das Zahlungssystem überprüft den Abrechnungsvertrag anhand seiner eindeutigen Nummer und berechnet dem Kundenkonto eine Gebühr. Mit einem bestehenden Abrechnungsvertrag ist es nicht mehr erforderlich, Zahlungsinformationen für jeden Kauf einzugeben. Kunden können ihre Abrechnungsvereinbarungen über das Dashboard ihres Kundenkontos verwalten, wobei der Status jedes einzelnen Kontos in der Form _Aktiv_ oder _Abgebrochen_. Wenn eine Abrechnungsvereinbarung storniert wird, kann sie nicht reaktiviert werden.

## Workflow für Abrechnungsvereinbarungen

1. **Kunde meldet sich für eine Abrechnungsvereinbarung an**. Nach Abschluss eines Abrechnungsvertrags können zusätzliche Abrechnungsverträge nur vom Kundenkonto hinzugefügt werden. Die Anzahl der Abrechnungsvereinbarungen, die ein Kunde erstellen kann, ist unbegrenzt. Kunden können eine der folgenden Methoden verwenden, um sich für Abrechnungsvereinbarungen zu registrieren:

   - **Anmelden bei Kundenkonto** - Kunden können sich über ihre Kundenkonten für einen Abrechnungsvertrag anmelden.
   - **Beim Checkout anmelden** - Kunden, die für einen Kauf mit PayPal Express Checkout bezahlen, können ein Kontrollkästchen aktivieren, um einen Abrechnungsvertrag zu erstellen. Obwohl der Abrechnungsvertrag nicht für die aktuelle Bestellung verwendet wird, wird er als Zahlungsmethode verfügbar, wenn der Kunde das nächste Mal eine Bestellung aufgibt.
   - **Registrieren Sie sich beim Store-Administrator.** - Auf Kundenanfrage kann der Store-Administrator mithilfe des Abrechnungsvertrags des Kunden einen Verkaufsauftrag erstellen.

1. **PayPal überprüft und zeichnet die Vereinbarung auf**. Wenn der Kunde die Bestellung mit Zahlung durch Abrechnungsvertrag aufgibt, werden die Referenz-ID des Abrechnungsvertrags und die Zahlungsdetails des Verkaufsauftrags an PayPal übertragen und im Kundenkonto erfasst, zusammen mit Referenzinformationen. Wenn die Zahlung erlaubt ist, wird eine Bestellung in Commerce erstellt. Die Referenz-ID der Abrechnungsvereinbarung wird an den Kunden und an den Store gesendet.

## Rechnungsvereinbarungen verwalten

Die _[!UICONTROL Billing Agreements]_auf der Seite werden alle Abrechnungsvereinbarungen zwischen Ihrem Store und seinen Kunden aufgelistet. Händler können die Datensätze nach Kunden- oder Abrechnungsvertragsinformationen filtern, einschließlich Referenz-ID der Abrechnungsvereinbarung, Status und Erstellungsdatum. Jeder Datensatz enthält allgemeine Informationen über den Abrechnungsvertrag und alle Verkaufsaufträge, die ihn als Zahlungsmethode verwendet haben. Sie können Abrechnungsvereinbarungen von Kunden anzeigen, widerrufen oder löschen. Eine stornierte Abrechnungsvereinbarung kann nur vom Store-Administrator gelöscht werden.

### Rechnungsvereinbarung anzeigen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Billing Agreements]**.

1. Suchen Sie die Abrechnungsvereinbarung in der Liste und klicken Sie auf , um sie zu öffnen.

Jede Seite der Abrechnungsvereinbarung besteht aus zwei Registerkarten: _[!UICONTROL General Information]_und_[!UICONTROL Related Orders]_.

#### Allgemeine Informationen

Dieser Tab enthält allgemeine Informationen zur Abrechnungsvereinbarung:

- [!UICONTROL Reference ID]: Eine eindeutige numerische Kennung, die der aktuellen Abrechnungsvereinbarung zugewiesen ist.
- [!UICONTROL Customer]: Dem aktuellen Abrechnungsvertrag zugewiesenes Konto des Kunden.
- [!UICONTROL Status]: Status der Zahlungsvereinbarung.
- [!UICONTROL Created At]: Erstellungsdatum.
- [!UICONTROL Updated At]: Datum der Aktualisierung.

![Ansicht der Abrechnungsvereinbarung](./assets/billing-agreement-view.png){width="600" zoomable="yes"}

#### Verwandte Bestellungen

Auf diesem Tab wird die Liste der Bestellungen angezeigt, die mit der aktuellen Abrechnungsvereinbarung aufgegeben wurden.

![Ansicht der Abrechnungsvereinbarung](./assets/billing-agreement-related-orders.png){width="600" zoomable="yes"}

### Abbrechen einer Abrechnungsvereinbarung

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Billing Agreements]**.

1. Suchen Sie die Abrechnungsvereinbarung in der Liste und klicken Sie auf , um sie zu öffnen.

1. Klicken Sie oben rechts auf **[!UICONTROL Cancel]**.

1. Klicken Sie zur Bestätigung der Aktion auf **[!UICONTROL OK]**.

### Rechnungsvereinbarung löschen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Billing Agreements]**.

1. Suchen Sie die Abrechnungsvereinbarung in der Liste und klicken Sie auf , um sie zu öffnen.

1. Klicken Sie oben rechts auf **[!UICONTROL Delete]**.

1. Klicken Sie zur Bestätigung der Aktion auf **[!UICONTROL OK]**.

### Spaltenbeschreibungen

| Spalte | Beschreibung |
|--- |--- |
| [!UICONTROL ID] | Eine eindeutige numerische Kennung, die jeder Abrechnungsvereinbarung zugewiesen wird |
| [!UICONTROL Email] | Kontakt-E-Mail eines Kunden |
| [!UICONTROL First Name] | Vorname eines Kunden |
| [!UICONTROL Last Name] | Nachname eines Kunden |
| [!UICONTROL Reference ID] | Eine eindeutige, numerische Referenz-ID, die jeder Abrechnungsvereinbarung zugewiesen wird |
| [!UICONTROL Status] | Status der Zahlungsvereinbarung. Optionen: `Active` oder `Canceled` |
| [!UICONTROL Created] | Erstellungsdatum |
| [!UICONTROL Updated] | Datum aktualisieren |

{style="table-layout:auto"}

## Storefront-Erlebnis

Kunden, die mit einem Zahlungsdienstleister einen Abrechnungsvertrag schließen, können jetzt Einkäufe tätigen und später entsprechend der Vereinbarung für sie bezahlen. Die

![Liste der Abrechnungsvereinbarungen im Dashboard des Kunden](./assets/billing-agreements-dashboard.png){width="700" zoomable="yes"}

| Spalte | Beschreibung |
|--- |--- |
| [!UICONTROL Reference ID] | Eine eindeutige, numerische Referenz-ID, die jeder Abrechnungsvereinbarung zugewiesen wird |
| [!UICONTROL Status] | Status der Zahlungsvereinbarung. Optionen: `Active` oder `Canceled` |
| [!UICONTROL Created At] | Erstellungsdatum |
| [!UICONTROL Updated At] | Datum aktualisieren |
| [!UICONTROL Payment Method] | Zahlungsdienstleister einer Abrechnungsvereinbarung |
| [!UICONTROL View] | Schaltfläche zum Anzeigen von Abrechnungsvereinbarungen |

{style="table-layout:auto"}

### Erstellen einer Abrechnungsvereinbarung

1. Im Konto-Dashboard wählt der Kunde **[!UICONTROL Billing Agreements]**.

1. under **[!UICONTROL New Billing Agreement]**, wählt einen Zahlungsdienstleister aus.

1. Klicken **[!UICONTROL Create]**.

Diese Aktion leitet den Kunden zur Zahlungssystem-Website weiter.

![Neuer Abrechnungsvertrag im Dashboard des Kundenkontos](./assets/create-billing-agreement-dashboard.png){width="700" zoomable="yes"}

### Rechnungsvereinbarung anzeigen

1. Im Konto-Dashboard wählt der Kunde **[!UICONTROL Billing Agreements]**.

1. Auswahl der Abrechnungsvereinbarung und Klicks **[!UICONTROL View]**.

![Anzeigen des Abrechnungsvertrags im Dashboard des Kunden](./assets/view-billing-agreement.png){width="700" zoomable="yes"}

### Abbrechen einer Abrechnungsvereinbarung

1. Im Konto-Dashboard wählt der Kunde **[!UICONTROL Billing Agreements]**.

1. Auswahl der Abrechnungsvereinbarung und Klicks **[!UICONTROL View]**.

1. Klicken Sie oben rechts auf **[!UICONTROL Cancel]** und dann **[!UICONTROL OK]** zur Bestätigung.

>[!NOTE]
>
>Wenn ein Admin-Benutzer (Händler) die Abrechnungsvereinbarung storniert, kann sie auf der Storefront nicht storniert werden. Die _Abgebrochen_ für diese Vereinbarung angezeigt.
