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

Bei der Unterstützung eines Kunden, der eine Bestellung aufgegeben hat, müssen Sie den Status der Bestellung ermitteln. Die verfügbaren Optionen für eine `Pending` -Bestellung unterscheiden sich von den Optionen für eine `Processing` -Bestellung. Weitere Informationen finden Sie unter [Verarbeiten einer Bestellung](order-processing.md).

## Ausstehende Bestellungen

Nachdem ein Kunde eine Bestellung aufgegeben hat, aber bevor die Zahlung eingegangen ist, befindet sich die Bestellung im Status `Pending`. Sie können die Reihenfolge bearbeiten, sie auf lange halten oder ganz abbrechen. Die Schaltflächenleiste einer ausstehenden Bestellung listet die verfügbaren Aktionen für eine Bestellung auf.

![Ausstehende Bestelloptionen](./assets/order-button-bar-pending.png){width="600" zoomable="yes"}

Wenn Sie wesentliche Teile einer Bestellung ändern, wird die ursprüngliche Bestellung abgebrochen und eine neue Bestellung erzeugt. Sie können jedoch die Abrechnungs- oder Lieferadresse ändern, ohne eine neue Bestellung zu generieren.

| Schaltfläche | Beschreibung |
|--- |--- |
| **[!UICONTROL Back]** | Kehrt zur Seite Bestellungen zurück, ohne Änderungen zu speichern. |
| **[!UICONTROL Login as Customer]** | Ermöglicht es einem Admin-Benutzer, Kunden bei ihren Bestellungen zu unterstützen. |
| **[!UICONTROL Cancel]** | Bricht die ausstehende Bestellung ab. |
| **[!UICONTROL Send Email]** | Sendet eine E-Mail über die ausstehende Bestellung an den Kunden. |
| **[!UICONTROL Hold]** / **[!UICONTROL Unhold]** | Ändert den Status der ausstehenden Bestellung in `On Hold`. Wählen Sie &quot;_[!UICONTROL Unhold]_&quot;, um den Halten freizugeben. |
| **[!UICONTROL Invoice]** | Erstellt eine [Rechnung](invoices.md#create-an-invoice) aus der ausstehenden Bestellung, indem die Bestellung in eine Rechnung konvertiert wird, und ändert den Bestellstatus in `processing`. |
| **[!UICONTROL Ship]** | Erstellt einen [delivery](shipments.md#create-a-shipment) -Datensatz für die Bestellung. |
| **[!UICONTROL Reorder]** | Erstellt eine neue ausstehende Bestellung, die ein Duplikat der aktuellen ausstehenden Bestellung ist. |
| **[!UICONTROL Edit]** | Öffnet eine ausstehende Bestellung im Bearbeitungsmodus. Die Schaltfläche Bearbeiten steht nur für ausstehende Bestellungen oder für Bestellungen mit ausgehandelten [Anführungszeichen](../b2b/quotes.md) zur Verfügung. |

{style="table-layout:auto"}

## Verarbeitungsaufträge

Eine Bestellung wechselt in den Status &quot;`Processing`&quot;, wenn:

* Die Zahlung für eine Bestellung wird empfangen/erfasst und die Rechnung wird generiert - wenn die Zahlungsaktion auf `Authorize and Capture` gesetzt ist.
* Ein Bestellvorgang ist autorisiert, aber die Zahlung wird noch nicht erfasst - wenn die Zahlungsaktion auf `Authorize` gesetzt ist.

Die Konfiguration der [Zahlungsaktion](../configuration-reference/sales/payment-methods.md#payment-actions) bestimmt, welche Bestellaktionen nach der Erstellung einer Bestellung verfügbar sind.

Sie können eine `Processing` -Bestellung nicht wesentlich ändern, aber Sie können die Abrechnungs- und Lieferadresse bearbeiten.

![Verarbeitungsreihenfolgen-Optionen](./assets/order-button-bar-processing.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Wenn die Zahlungsaktion der Zahlungsmethode auf `Authorize and Capture` eingestellt ist, wird automatisch eine Rechnung erstellt, wenn der Kunde eine Bestellung aufgibt. In diesem Fall können Sie Geldmittel mit einem [Credit Memo](credit-memo-create.md) zurückerstatten, aber [stornieren](#cancel-a-pending-order) oder [void](#void-a-processing-order) nicht in der Bestellung.

| Schaltfläche | Beschreibung |
|--- |--- |
| **[!UICONTROL Back]** | Kehrt zur Seite Bestellungen zurück, ohne Änderungen zu speichern. |
| **[!UICONTROL Send Email]** | Sendet eine E-Mail über die Bestellung an den Kunden. |
| **[!UICONTROL Void]** | [Voids](#void-a-processing-order) eine Bestelltransaktion oder eine Teilbestelltransaktion. |
| **[!UICONTROL Credit Memo]** | Initiiert den Prozess zum Erstellen eines [Credit Memo](credit-memo-create.md). |
| **[!UICONTROL Hold]** / **[!UICONTROL Unhold]** | Ändert den Status der Verkaufsreihenfolge in `On Hold`. Wählen Sie &quot;_[!UICONTROL Unhold]_&quot;, um den Halten für den Verkaufsauftrag freizugeben. |
| **[!UICONTROL Reorder]** | Erstellt eine neue ausstehende Bestellung basierend auf der aktuellen Bestellung. |
| **[!UICONTROL Create Returns]** | ![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Initiiert den Prozess zum [return](returns.md) eines oder mehrerer Elemente aus der Bestellung. |

{style="table-layout:auto"}

## Eine Verarbeitungsreihenfolge ausschließen

Wenn eine Bestellung noch den Status &quot;`Processing`&quot; aufweist und die Zahlungsintegration auf &quot;`Authorize`&quot;(nicht auf &quot;`Authorize and Capture`&quot;) gesetzt ist, können Sie nur eine Transaktion stornieren oder eine Bestellung stornieren. [Durch Abbruch einer Bestellung](#cancel-a-pending-order) wird auch die Autorisierung aufgehoben.

Wenn eine Bestellung mittels einer Zahlungsmethode mit der Zahlungsaktion auf `Authorize and Capture` gestellt wird, können Sie die Mittel über die Kreditkarte zurückerstatten, sie aber nicht stornieren, weil sie fakturiert und die Zahlung erfasst wird.

Ihre Zahlungsmethode bestimmt Ihre verfügbaren Zahlungsaktionen. Weitere Informationen finden Sie unter [Zahlungsaktionen](../configuration-reference/sales/payment-methods.md#payment-actions) .

**_So lassen Sie eine Bestellung aus:_**

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Klicken Sie in der Spalte &quot;**[!UICONTROL Action]**&quot;, damit die Reihenfolge bearbeitet werden kann, auf &quot;**[!UICONTROL View]**&quot;.

1. Klicken Sie auf **[!UICONTROL Void]** , um die Bestellung aufzuheben.

1. Klicken Sie in der Eingabeaufforderung auf **[!UICONTROL OK]** , um die Bestellung aufzuheben.

Sie können alle erforderlichen Rückerstattungen mithilfe eines [Credit Memo](credit-memo-create.md) vornehmen, nachdem die Mittel erfasst wurden. Sie können auch eine [RMA (Return Merchandise Autorisierung)](returns.md) erstellen, die für die Produktrückgabe ausgestellt wurde. Weitere Informationen finden Sie unter [Verarbeitung einer Bestellung](order-processing.md).

## Bearbeiten einer ausstehenden Bestellung

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Klicken Sie in der Spalte &quot;**[!UICONTROL Action]**&quot;, damit die Reihenfolge bearbeitet werden kann, auf &quot;**[!UICONTROL View]**&quot;.

1. Klicken Sie auf **[!UICONTROL Edit]**.

   ![Reihenfolge bearbeiten](./assets/order-edit.png){width="600" zoomable="yes"}

1. Klicken Sie in der Eingabeaufforderung auf **[!UICONTROL OK]** , um mit der Bearbeitung fortzufahren.

1. Aktualisieren Sie die Bestellung nach Bedarf.

1. Wenden Sie Ihre Änderungen an:
   * Klicken Sie auf **[!UICONTROL Save]**, um die an der Abrechnungs- oder Versandadresse vorgenommenen Änderungen zu speichern.
   * Klicken Sie auf &quot;**[!UICONTROL Submit Order]**&quot;, um an den Zeileneinträgen vorgenommene Änderungen zu speichern und die Reihenfolge erneut zu verarbeiten.

## Auf Eis legen

Wenn die bevorzugte Zahlungsmethode des Kunden nicht verfügbar ist oder der Artikel vorübergehend nicht vorrätig ist, können Sie die Bestellung auf Lager halten.

1. Suchen Sie im Raster _Bestellungen_ die `Pending`-Reihenfolge, die Sie auf Halten platzieren möchten.

1. Klicken Sie in der Spalte _Aktion_ auf **[!UICONTROL View]**.

1. Klicken Sie auf &quot;**[!UICONTROL Hold]**&quot;, um die Bestellung aufzubewahren.

Um den Haltepunkt einer Bestellung zu entfernen, bearbeiten Sie die Bestellung erneut und klicken Sie auf **[!UICONTROL Unhold]**.

## Abbrechen einer ausstehenden Bestellung

Wenn eine Bestellung abgebrochen wird, ändert sich ihr Status von `Pending` in `Canceled`.

1. Suchen Sie im Raster _[!UICONTROL Orders]_nach der ausstehenden Bestellung, die abgebrochen werden soll.

1. Klicken Sie in der Spalte _[!UICONTROL Action]_auf **[!UICONTROL View]**.

1. Klicken Sie auf **[!UICONTROL Cancel]** , um die Bestellung abzubrechen.

Der Status der Bestellung ist jetzt `Canceled`.
