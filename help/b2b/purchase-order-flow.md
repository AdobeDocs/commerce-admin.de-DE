---
title: Kaufaufträge für Unternehmen
description: Erfahren Sie mehr über Workflows für Bestellungen, mit denen Unternehmen Ausgaben verfolgen und kontrollieren können.
exl-id: 4f93ab4c-6bdf-495e-9183-3a18898b377f
feature: B2B, Purchase Orders
source-git-commit: c1d8bdcd2d09567846ef6819660c57468062ab01
workflow-type: tm+mt
source-wordcount: '941'
ht-degree: 0%

---

# Kaufaufträge für Unternehmen

Kaufaufträge sind eine gängige Methode für Unternehmen, Ausgaben zu verfolgen und zu kontrollieren. [Bestellung](../stores-purchase/purchase-order.md) ist eine der standardmäßigen Offline-Zahlungsmethoden, die in Adobe Commerce und Magento Open Source unterstützt werden. Wenn B2B von Adobe Commerce installiert ist und [_Bestellung aktivieren_](account-company-manage.md#advanced-settings) für ein Unternehmenskonto aktiviert ist, werden alle Bestellungen automatisch als Bestellung (Bestellformular) erstellt. Unternehmensbenutzer mit den erforderlichen [Berechtigungen](account-company-roles-permissions.md) können von ihnen erstellte und von untergeordneten Benutzern erstellte POs und POs erstellen, bearbeiten und löschen.

## Ablauf der Bestellung

Je nach Rolle und Bestellung können Benutzer des Unternehmens mehreren Validierungsregeln unterliegen. Je nachdem, ob Online- oder Offline-Zahlungsmethoden verwendet werden, unterscheidet sich der Fluss geringfügig. Unternehmensadministratoren können automatisch Bestellungen erstellen und dabei die Validierungsregeln umgehen. Da die Speicherung von Online-Zahlungsdetails während des Validierungsprozesses ein Sicherheitsrisiko darstellt, werden diese Details nach der Validierung hinzugefügt und der Bestellauftrag in eine reale Bestellung umgewandelt.

![Ablauf der Bestellung](./assets/purchase-order-flow.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Eine Bestellung kann nicht aufgegeben werden, wenn ein oder mehrere Produkte in der Bestellung derzeit deaktiviert oder nicht vorrätig sind.

Der Workflow für die Bestellung eines Unternehmens kann auf verschiedene Weise variieren:

- Wenn keine Validierungsregeln festgelegt sind, können Bestellungen direkt aufgegeben und die Bestellung abgeschlossen werden.

  >[!NOTE]
  >
  >Standardmäßig wird den Benutzern des Unternehmens immer eine `Purchase order has been submitted for approval` -Meldung angezeigt, selbst wenn keine Validierungsregeln festgelegt sind. Wenn kein Validierungsprozess erforderlich ist, erhalten die Benutzer des Unternehmens automatisch eine E-Mail, in der sie darüber informiert werden, dass die Bestellung erstellt und validiert wurde.

- Wenn die Genehmigungsregeln vom Unternehmensadministrator definiert werden, durchlaufen die Benutzer den Genehmigungsprozess.
- Wenn für eine Bestellung mehrere Validierungsregeln gelten, müssen alle eindeutigen erforderlichen Genehmiger sie genehmigen.
- Bei der Erstellung der Bestellung werden die Details der Offline-Zahlung angegeben.
- Die Online-Zahlungsdetails werden nach der Validierung der Bestellung angegeben.

>[!NOTE]
>
>Die Bestelldaten erzeugen einen _Schnappschuss_ der Artikelpreise, Rabatte und Versandpreise zum Zeitpunkt der Bestellerstellung. Wenn sich der Preis eines Artikels nach der Erstellung des Bestellformulars ändert, wird der ursprüngliche Preis verwendet.

### Grundlegendes Workflow-Beispiel

Unternehmen verwenden Bestellungen, um zu steuern, was Mitarbeiter im Namen des Unternehmens kaufen können, und legen häufig Genehmigungsregeln fest, um Unternehmensrichtlinien durchzusetzen. Abhängig von den Validierungsregeln müssen möglicherweise mehrere Benutzer die Bestellung validieren.

1. Der Benutzer erstellt eine Bestellung für Waren im Wert von 25.000 $.
1. Ihr Manager muss zustimmen.
1. Da die Bestellung mehr als 10.000 $ beträgt, muss der V.P. auch genehmigen.
1. Je nach Zahlungsmethode wird nach der Validierung der Auftrag automatisch in eine Bestellung umgewandelt oder der Benutzer kehrt zur Eingabe der Zahlungsdetails zurück.

### Validierungsregeln

Genehmigungsregeln werden verwendet, um Ausgaben anhand von Unternehmensrichtlinien zu kontrollieren. Beispiele für Validierungsregeln sind:

- Für alle Bestellungen über 100 Euro ist die Genehmigung Ihres Managers erforderlich.
- Für Bestellungen über 1000 USD ist die Genehmigung durch Ihren Manager und den Unternehmensadministrator erforderlich.
- Für Bestellungen mit mehr als 30 eindeutigen SKUs ist die Genehmigung des Unternehmens-Administrators erforderlich.

Wenn diese Regeln für ein Unternehmen gelten, kann ein Unternehmensbenutzer die Bestellung sofort abschließen, wenn die Bestellung weniger als 100 USD beträgt. Informationen zur Definition von Genehmigungsregeln finden Sie unter [Genehmigungsregeln](account-dashboard-approval-rules.md).

### Typen von Store-Benutzern

Der Workflow für die Bestellung kann auch je nach dem, der den Kauf durchführt, unterschiedlich ausfallen.

- Ein regulärer Arbeitnehmer kann allen Genehmigungsregeln unterliegen
- Ein Manager könnte mehr Kaufkraft haben und unterschiedliche Genehmigungsregeln haben.
- Unternehmensadministratoren können alle Validierungsregeln umgehen und ihre Bestellungen automatisch abschließen lassen.

All diese Faktoren können sich auf den exakten Checkout-Prozess auswirken.

## [!UICONTROL My Purchase Orders]

Wenn Bestellungen für ein Unternehmen aktiviert sind, wird das Element &quot;**[!UICONTROL My Purchase Orders]**&quot;im linken Bereich für Kunden angezeigt, die bei einem Unternehmensbenutzerkonto angemeldet sind. Es gibt drei Registerkarten, die unterschiedliche Bestelllisten und Funktionen bereitstellen:

- **[!UICONTROL My Purchase Orders]**: Vom Kunden erstellte POs.
- **[!UICONTROL Company Purchase Orders]**: POs von untergeordneten Benutzern innerhalb des Unternehmens (abhängig von der Unternehmensstruktur und den Rollen).
- **[!UICONTROL Requires My Approval]**: (Sichtbar für bestimmte Genehmiger) POs, die auf die Genehmigung des Kunden warten. Der Zähler zeigt an, wie viele Bestellungen auf die Validierung warten.

![Meine Kaufaufträge](./assets/account-dashboard-my-purchase-orders.png){width="700" zoomable="yes"}

Weitere Informationen zu den unterstützten Bestellfunktionen, die für Unternehmensbenutzer im Storefront verfügbar sind, finden Sie unter [Meine Kaufaufträge](account-dashboard-my-purchase-orders.md).

## Offline- und Online-Zahlungsmethoden

Workflows können je nach Zahlungsmethode variieren. Weitere Informationen zu Adobe Commerce-Zahlungsmethoden finden Sie unter [Zahlungsmethoden](../stores-purchase/payments.md) im _Verkaufs- und Kauferlebnis-Handbuch_.

>[!IMPORTANT]
>
>Für Bestellungen sollte ein _In-Context_-Checkout-Erlebnis verwendet werden. _Out-of-Context_ Checkouts werden nicht unterstützt, da sie den normalen Checkout-Fluss umgehen. Im Allgemeinen bedeutet _In-Context_, dass der Kunde auf Ihrer Commerce-Site bleibt, um den Prozess abzuschließen. _Out-of-Context_ ist der Zeitpunkt, zu dem der Kunde zu einer anderen Site geleitet wird, um den Kauf abzuschließen.

### Online-Zahlungen

Aus Sicherheitsgründen möchten Online-Stores normalerweise keine Kreditkartendaten erfassen, während auf den Abschluss des Genehmigungsprozesses gewartet wird. Wenn also eine Online-Zahlungsoption ausgewählt ist, kehrt der Ersteller der Bestellung nach der Genehmigung zum Speicher zurück, gibt die Zahlungsdetails ein und schließt die Bestellung ab. Beispiele für Online-Zahlungen sind:

- Kredit-/Debug-Karten
- PayPal
- Braintree

>[!IMPORTANT]
>
>Die Verwendung von Geschenkkarten, Gutschriften oder Bonuspunkten mit Online-Zahlungsmethoden für Bestellungen wird nicht unterstützt. Die Aktivierung dieser Funktionen mit Online-Zahlungen kann zu unerwartetem Verhalten führen. Es wird empfohlen, Geschenkkarten zu deaktivieren, Kredit- und Bonuspunkte zu speichern, wenn Online-Zahlungen für Bestellungen aktiviert sind.

### Offline-Zahlungen

Da Offline-Zahlungsmethoden wie beispielsweise eine Geldbestellung außerhalb der Website abgewickelt werden, sind sie sicherer. Kaufaufträge mit Offline-Zahlungen können nach jedem Validierungsprozess automatisch verarbeitet werden.

Beispiele für Offline-Zahlungen sind:

- Überprüfen/Money Order
- Kontozahlung
- Zustellbare Barmittel
- Banküberweisungen
- Store-Guthaben
