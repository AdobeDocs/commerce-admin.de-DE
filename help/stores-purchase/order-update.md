---
title: Auftrag aktualisieren
description: Erfahren Sie, wie Sie die Bestellung eines Kunden in der Admin-Konsole aktualisieren.
exl-id: 15c73d27-f4bd-47d6-8d36-902074f9c3e6
feature: Orders, Customer Service
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 0%

---

# Auftrag aktualisieren

Bei der Unterstützung eines Kunden, der eine Bestellung aufgegeben hat, müssen Sie den Status der Bestellung ermitteln. Die verfügbaren Optionen für eine `Pending` -Reihenfolge sich von den Optionen für `Processing` bestellen. Weitere Informationen finden Sie unter [Auftrag verarbeiten](order-processing.md).

## Ausstehende Bestellungen

Nachdem ein Kunde eine Bestellung aufgegeben hat, aber bevor die Zahlung eingegangen ist, befindet sich die Bestellung in `Pending` -Status. Sie können die Reihenfolge bearbeiten, sie auf lange halten oder ganz abbrechen. Die Schaltflächenleiste einer ausstehenden Bestellung listet die verfügbaren Aktionen für eine Bestellung auf.

![Ausstehende Bestelloptionen](./assets/order-button-bar-pending.png){width="600" zoomable="yes"}

Wenn Sie wesentliche Teile einer Bestellung ändern, wird die ursprüngliche Bestellung abgebrochen und eine neue Bestellung erzeugt. Sie können jedoch die Abrechnungs- oder Lieferadresse ändern, ohne eine neue Bestellung zu generieren.

| Schaltfläche | Beschreibung |
|--- |--- |
| **[!UICONTROL Back]** | Kehrt zur Seite Bestellungen zurück, ohne Änderungen zu speichern. |
| **[!UICONTROL Login as Customer]** | Ermöglicht es einem Admin-Benutzer, Kunden bei ihren Bestellungen zu unterstützen. |
| **[!UICONTROL Cancel]** | Bricht die ausstehende Bestellung ab. |
| **[!UICONTROL Send Email]** | Sendet eine E-Mail über die ausstehende Bestellung an den Kunden. |
| **[!UICONTROL Hold]** / **[!UICONTROL Unhold]** | Ändert den Status der ausstehenden Bestellung in `On Hold`. Um den Laderaum freizugeben, wählen Sie _[!UICONTROL Unhold]_. |
| **[!UICONTROL Invoice]** | Erstellt eine [Rechnung](invoices.md#create-an-invoice) aus der ausstehenden Bestellung durch Konvertieren der Bestellung in eine Rechnung und ändert den Bestellstatus in `processing`. |
| **[!UICONTROL Ship]** | Erstellt eine [Verbringung](shipments.md#create-a-shipment) -Datensatz für die Bestellung. |
| **[!UICONTROL Reorder]** | Erstellt eine neue ausstehende Bestellung, die ein Duplikat der aktuellen ausstehenden Bestellung ist. |
| **[!UICONTROL Edit]** | Öffnet eine ausstehende Bestellung im Bearbeitungsmodus. Die Schaltfläche Bearbeiten steht nur bei ausstehenden Bestellungen oder bei auf Verhandlungsbasis erfolgten Bestellungen zur Verfügung [Anführungszeichen](../b2b/quotes.md). |

{style="table-layout:auto"}

## Verarbeitungsaufträge

Eine Bestellung gibt einen `Processing` state when:

* Die Zahlung für eine Bestellung wird empfangen/erfasst und die Rechnung wird generiert, wenn die Zahlungsaktion auf `Authorize and Capture`.
* Ein Bestellvorgang ist autorisiert, aber die Zahlung wird noch nicht erfasst, wenn die Zahlungsaktion auf `Authorize`.

Die [Konfiguration der Zahlungsaktion](../configuration-reference/sales/payment-methods.md#payment-actions) bestimmt, welche Bestellaktionen nach der Erstellung einer Bestellung verfügbar sind.

Sie können eine `Processing` bestellen, aber Sie können die Abrechnungs- und Lieferadresse bearbeiten.

![Optionen für Verarbeitungsreihenfolge](./assets/order-button-bar-processing.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Wenn die Zahlungsaktion der Zahlungsmethode auf `Authorize and Capture`, wird automatisch eine Rechnung erstellt, wenn der Kunde eine Bestellung aufgibt. In diesem Fall können Sie die Rückerstattung von Geldern mithilfe eines [Credit Memo](credit-memo-create.md), aber nicht [cancel](#cancel-a-pending-order) oder [void](#void-a-processing-order) die Bestellung.

| Schaltfläche | Beschreibung |
|--- |--- |
| **[!UICONTROL Back]** | Kehrt zur Seite Bestellungen zurück, ohne Änderungen zu speichern. |
| **[!UICONTROL Send Email]** | Sendet eine E-Mail über die Bestellung an den Kunden. |
| **[!UICONTROL Void]** | [Voids](#void-a-processing-order) eine Bestelltransaktion oder eine Teilbestelltransaktion. |
| **[!UICONTROL Credit Memo]** | Initiiert den Prozess zum Erstellen einer [Credit Memo](credit-memo-create.md). |
| **[!UICONTROL Hold]** / **[!UICONTROL Unhold]** | Ändert den Status des Verkaufsauftrags in `On Hold`. Wählen Sie die Option, um den Kaufauftrag freizugeben. _[!UICONTROL Unhold]_. |
| **[!UICONTROL Reorder]** | Erstellt eine neue ausstehende Bestellung basierend auf der aktuellen Bestellung. |
| **[!UICONTROL Create Returns]** | ![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce) Initiiert den Prozess in [return](returns.md) ein oder mehrere Artikel aus der Bestellung. |

{style="table-layout:auto"}

## Eine Verarbeitungsreihenfolge ausschließen

Wenn sich eine Bestellung noch in einer `Processing` Status und Zahlungsintegration auf `Authorize` (nicht `Authorize and Capture`), können Sie nur eine Transaktion stornieren oder eine Bestellung stornieren. [Abbruch einer Bestellung](#cancel-a-pending-order) auch die Zulassung entfällt.

Wenn eine Bestellung mithilfe einer Zahlungsmethode aufgegeben wird und die Zahlungsaktion auf `Authorize and Capture` Sie können die Mittel über ein Kreditmemo zurückerstatten, aber nicht stornieren, weil es fakturiert wird und die Zahlung erfasst wird.

Ihre Zahlungsmethode bestimmt Ihre verfügbaren Zahlungsaktionen. Siehe [Zahlungsaktionen](../configuration-reference/sales/payment-methods.md#payment-actions) für weitere Informationen.

**_So löschen Sie eine Bestellung:_**

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Im **[!UICONTROL Action]** die Spalte für die zu bearbeitende Reihenfolge, klicken Sie auf **[!UICONTROL View]**.

1. Klicks **[!UICONTROL Void]** , um den Auftrag zu annullieren.

1. Klicken Sie in der Eingabeaufforderung auf **[!UICONTROL OK]** , um den Auftrag zu annullieren.

Sie können alle erforderlichen Erstattungen über eine [Credit Memo](credit-memo-create.md) nachdem Mittel erfasst wurden. Sie können auch eine [Zulassung von Rückwaren (RMA)](returns.md) ausgegeben für Produktrückgaben. Weitere Informationen finden Sie unter [Verarbeitung einer Bestellung](order-processing.md).

## Bearbeiten einer ausstehenden Bestellung

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Im **[!UICONTROL Action]** die Spalte für die zu bearbeitende Reihenfolge, klicken Sie auf **[!UICONTROL View]**.

1. Klicken **[!UICONTROL Edit]**.

   ![Reihenfolge bearbeiten](./assets/order-edit.png){width="600" zoomable="yes"}

1. Klicken Sie in der Eingabeaufforderung auf **[!UICONTROL OK]** , um die Bearbeitung fortzusetzen.

1. Aktualisieren Sie die Bestellung nach Bedarf.

1. Wenden Sie Ihre Änderungen an:
   * Klicken Sie zum Speichern der an der Abrechnungs- oder Versandadresse vorgenommenen Änderungen auf **[!UICONTROL Save]**.
   * Um an Zeileneinträgen vorgenommene Änderungen zu speichern und die Reihenfolge erneut zu verarbeiten, klicken Sie auf **[!UICONTROL Submit Order]**.

## Auf Eis legen

Wenn die bevorzugte Zahlungsmethode des Kunden nicht verfügbar ist oder der Artikel vorübergehend nicht vorrätig ist, können Sie die Bestellung auf Lager halten.

1. Im _Bestellungen_ Raster, suchen Sie die `Pending` Ordnung, die Sie auf Eis legen wollen.

1. Im _Aktion_ Spalte, klicken **[!UICONTROL View]**.

1. Klicks **[!UICONTROL Hold]** um den Befehl auf Eis zu legen.

Um den Haltepunkt einer Bestellung zu entfernen, bearbeiten Sie die Reihenfolge erneut und klicken Sie auf **[!UICONTROL Unhold]**.

## Abbrechen einer ausstehenden Bestellung

Wenn eine Bestellung abgebrochen wird, ändert sich ihr Status von `Pending` nach `Canceled`.

1. Im _[!UICONTROL Orders]_Suchen Sie nach der ausstehenden Bestellung, die abgebrochen werden soll.

1. Im _[!UICONTROL Action]_Spalte, klicken **[!UICONTROL View]**.

1. Klicks **[!UICONTROL Cancel]** , um die Bestellung abzubrechen.

Der Status der Bestellung lautet jetzt `Canceled`.
