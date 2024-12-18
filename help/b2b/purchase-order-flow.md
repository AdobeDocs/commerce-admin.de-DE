---
title: Bestellungen für Unternehmen
description: Erfahren Sie mehr über Auftrags-Workflows, mit denen Unternehmen Ausgaben verfolgen und kontrollieren können.
exl-id: 4f93ab4c-6bdf-495e-9183-3a18898b377f
feature: B2B, Purchase Orders
source-git-commit: c1d8bdcd2d09567846ef6819660c57468062ab01
workflow-type: tm+mt
source-wordcount: '941'
ht-degree: 0%

---

# Bestellungen für Unternehmen

Bestellungen (POs) sind eine gängige Methode für Unternehmen, die Ausgaben zu verfolgen und zu kontrollieren. [Bestellung](../stores-purchase/purchase-order.md) ist eine der standardmäßigen Offline-Zahlungsmethoden, die in Adobe Commerce und Magento Open Source unterstützt werden. Wenn B2B von Adobe Commerce installiert und [_Bestellungen aktivieren_](account-company-manage.md#advanced-settings) für ein Unternehmenskonto aktiviert wird, werden alle Bestellungen automatisch als Bestellungen (Purchase Orders, PO) erstellt. Firmenbenutzer mit den erforderlichen [Berechtigungen](account-company-roles-permissions.md) können von ihnen erstellte Bestellungen und von untergeordneten Benutzern erstellte Bestellungen erstellen, bearbeiten und löschen.

## Bestellfluss

Je nach Rolle und Reihenfolge können für Firmenbenutzer mehrere Genehmigungsregeln gelten. Und je nachdem, ob Sie Online- oder Offline-Zahlungsmethoden verwenden, ist der Fluss etwas anders. Firmenadministratoren können Bestellungen automatisch erstellen und dabei die Genehmigungsregeln umgehen. Da das Speichern von Online-Zahlungsdetails während des Genehmigungsprozesses ein Sicherheitsrisiko darstellt, werden diese Details nach der Genehmigung hinzugefügt und die Bestellung wird dann in eine echte Bestellung umgewandelt.

![Bestellfluss](./assets/purchase-order-flow.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Eine Bestellung kann nicht aufgegeben werden, wenn ein oder mehrere Produkte in der Bestellung derzeit deaktiviert oder nicht vorrätig sind.

Der Workflow für Bestellungen für eine Firma kann auf verschiedene Weise variieren:

- Wenn keine Validierungsregeln festgelegt sind, können Bestellungen aufgegeben und die Bestellung direkt abgeschlossen werden.

  >[!NOTE]
  >
  >Standardmäßig wird Firmenbenutzenden immer eine `Purchase order has been submitted for approval` angezeigt, auch wenn keine Validierungsregeln festgelegt sind. Wenn kein Genehmigungsprozess erforderlich ist, erhalten die Benutzer des Unternehmens automatisch eine E-Mail, in der sie darüber informiert werden, dass die Bestellung erstellt und genehmigt wurde.

- Wenn Genehmigungsregeln vom Unternehmensadministrator definiert werden, durchlaufen die Benutzer den Genehmigungsprozess.
- Wenn für eine Bestellung mehrere Genehmigungsregeln gelten, müssen alle erforderlichen Einzelgenehmiger sie genehmigen.
- Offline-Zahlungsdetails werden bei der Erstellung der Bestellung eingegeben.
- Online-Zahlungsdetails werden eingegeben, nachdem die Bestellung genehmigt wurde.

>[!NOTE]
>
>Bestellungen erstellen eine _Momentaufnahme_ der Artikelpreise, Rabatte und Versandpreise zum Zeitpunkt der Auftragserstellung. Wenn sich der Preis eines Artikels nach der Erstellung der Bestellung ändert, wird der ursprüngliche Preis verwendet.

### Beispiel für einen einfachen Workflow

Unternehmen verwenden Bestellungen, um zu steuern, was Mitarbeiter im Namen des Unternehmens kaufen können, und richten häufig Genehmigungsregeln ein, um Unternehmensrichtlinien durchzusetzen. Abhängig von den Genehmigungsregeln müssen möglicherweise mehrere Personen die Bestellung genehmigen.

1. Der Benutzer erstellt eine Bestellung für Waren im Wert von 25.000 US-Dollar.
1. Ihr Manager muss zustimmen.
1. Da die Bestellung mehr als 10.000 US-Dollar beträgt, muss der V.P. auch genehmigen.
1. Je nach Zahlungsmethode wird die Bestellung nach den Validierungen automatisch in eine Bestellung umgewandelt, oder der Benutzer kehrt zurück, um Zahlungsdetails einzugeben.

### Validierungsregeln

Validierungsregeln werden verwendet, um Ausgaben auf der Grundlage von Unternehmensrichtlinien zu steuern. Beispiele für Genehmigungsregeln sind:

- Jede Bestellung über 100 $ bedarf der Genehmigung Ihres Managers.
- Für jede Bestellung über 1.000 US-Dollar benötigen Sie die Genehmigung Ihres Managers und des Unternehmensadministrators.
- Für jede Bestellung mit mehr als 30 eindeutigen SKUs ist die Genehmigung des Unternehmensadministrators erforderlich.

Wenn diese Regeln für ein Unternehmen gelten, kann ein Firmenbenutzer die Bestellung sofort abschließen, wenn die Bestellung weniger als 100 US-Dollar beträgt. Informationen zur Definition von Genehmigungsregeln finden Sie unter [Genehmigungsregeln](account-dashboard-approval-rules.md).

### Typen von Store-Benutzern

Der Workflow für Bestellungen kann auch unterschiedlich sein, je nachdem, wer den Kauf tätigt.

- Ein regulärer Mitarbeiter kann allen Genehmigungsregeln unterliegen
- Ein Manager könnte über mehr Kaufkraft verfügen und hätte andere Genehmigungsregeln
- Firmenadministratoren können alle Genehmigungsregeln umgehen und ihre Bestellungen automatisch ausführen lassen.

Alle diese Faktoren können sich auf den exakten Checkout-Prozess auswirken.

## [!UICONTROL My Purchase Orders]

Wenn Bestellungen für ein Unternehmen aktiviert sind, wird der **[!UICONTROL My Purchase Orders]** im linken Bereich für Kunden angezeigt, die bei einem Firmenbenutzerkonto angemeldet sind. Es gibt drei Registerkarten mit verschiedenen Bestelllisten und Funktionen:

- **[!UICONTROL My Purchase Orders]**: Vom Kunden erstellte Bestellungen.
- **[!UICONTROL Company Purchase Orders]**: Bestellungen von untergeordneten Benutzern innerhalb des Unternehmens (hängt von der Unternehmensstruktur und den Rollen ab).
- **[!UICONTROL Requires My Approval]**: (Sichtbar für bestimmte genehmigende Personen) Bestellungen, die auf die Genehmigung durch den Kunden warten. Der Zähler zeigt an, wie viele Aufträge auf Genehmigung warten.

![Meine Bestellungen](./assets/account-dashboard-my-purchase-orders.png){width="700" zoomable="yes"}

Weitere Informationen zu den unterstützten Bestellfunktionen, die für Firmenbenutzer in der Storefront verfügbar sind, finden Sie unter [Meine Bestellungen](account-dashboard-my-purchase-orders.md).

## Offline- vs. Online-Zahlungsmethoden

Workflows können je nach Zahlungsmethode variieren. Weitere Informationen zu Adobe Commerce-Zahlungsmethoden finden Sie unter [Zahlungsmethoden](../stores-purchase/payments.md) im _Handbuch zu Vertriebs- und Kauferlebnissen_.

>[!IMPORTANT]
>
>Bestellungen sollten ein _-_-Erlebnis verwenden. _Out-of-Context_ Auscheckvorgänge werden nicht unterstützt, da sie den normalen Auscheckfluss umgehen. Im Allgemeinen bedeutet _In-Context_, dass der Kunde auf Ihrer Commerce-Site bleibt, um den Prozess abzuschließen. _Nicht im Kontext_ liegt vor, wenn der Kunde zu einer anderen Website weitergeleitet wird, um den Kauf abzuschließen.

### Online-Zahlungen

Aus Sicherheitsgründen möchten Online-Shops normalerweise keine Kreditkartendetails erfassen, während sie auf den Abschluss des Genehmigungsprozesses warten. Wenn daher eine Online-Zahlungsoption ausgewählt wird, kehrt der Ersteller der Bestellung nach der Genehmigung zum Geschäft zurück, gibt die Zahlungsdetails ein und schließt die Bestellung ab. Beispiele für Online-Zahlungen sind:

- Kredit-/Debitkarten
- PayPal
- Braintree

>[!IMPORTANT]
>
>Die Verwendung von Geschenkkarten, Gutschriften oder Belohnungspunkten mit Online-Zahlungsmethoden für Bestellungen wird nicht unterstützt. Die Aktivierung dieser Funktionen bei Online-Zahlungen kann zu unerwartetem Verhalten führen. Es wird empfohlen, Geschenkgutscheine zu deaktivieren, Guthaben zu speichern und Punkte zu belohnen, wenn Online-Zahlungen für Bestellungen aktiviert sind.

### Offline-Zahlungen

Da Offline-Zahlungsmethoden, wie z. B. eine Geldbestellung, außerhalb der Website abgewickelt werden, sind sie sicherer. Bestellungen mit Offline-Zahlungen können nach jedem Genehmigungsprozess automatisch verarbeitet werden.

Beispiele für Offline-Zahlungen sind:

- Scheck/Zahlungsanweisung
- Anzahlung
- Nachnahme
- Banküberweisungen
- Warenkredit
