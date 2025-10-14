---
title: Aktualisieren einer Bestellung
description: Erfahren Sie, wie Sie die Bestellung eines Kunden in Admin aktualisieren können.
exl-id: 15c73d27-f4bd-47d6-8d36-902074f9c3e6
feature: Orders, Customer Service
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 0%

---

# Aktualisieren einer Bestellung

Wenn Sie einem Kunden helfen, der eine Bestellung aufgegeben hat, müssen Sie den Status der Bestellung ermitteln. Die verfügbaren Optionen für eine `Pending` unterscheiden sich von den Optionen für eine `Processing`. Weitere Informationen finden Sie unter [Bearbeiten einer Bestellung](order-processing.md).

## Ausstehende Bestellungen

Nachdem ein Kunde eine Bestellung aufgegeben hat, aber bevor die Zahlung empfangen wird, befindet sich die Bestellung in `Pending` Status. Sie können die Bestellung bearbeiten, zurückstellen oder vollständig abbrechen. Die Schaltflächenleiste einer ausstehenden Bestellung listet die verfügbaren Aktionen für eine Bestellung auf.

![Ausstehende Bestelloptionen](./assets/order-button-bar-pending.png){width="600" zoomable="yes"}

Wenn Sie wesentliche Teile einer Bestellung ändern, wird die ursprüngliche Bestellung storniert und eine neue Bestellung erzeugt. Sie können jedoch die Rechnungs- oder Lieferadresse ändern, ohne eine neue Bestellung zu generieren.

| Schaltfläche | Beschreibung |
|--- |--- |
| **[!UICONTROL Back]** | Kehrt zur Seite Bestellungen zurück, ohne die Änderungen zu speichern. |
| **[!UICONTROL Login as Customer]** | Ermöglicht es einem Admin-Benutzer, Kunden bei ihren Bestellungen zu unterstützen. |
| **[!UICONTROL Cancel]** | Storniert die ausstehende Bestellung. |
| **[!UICONTROL Send Email]** | Sendet eine E-Mail über die ausstehende Bestellung an den Kunden. |
| **[!UICONTROL Hold]**/**[!UICONTROL Unhold]** | Ändert den Status der ausstehenden Bestellung in `On Hold`. Um den Haltebereich zu lösen, wählen Sie _[!UICONTROL Unhold]_&#x200B;aus. |
| **[!UICONTROL Invoice]** | Erstellt eine [Rechnung](invoices.md#create-an-invoice) aus der ausstehenden Bestellung, indem die Bestellung in eine Rechnung umgewandelt wird, und ändert den Bestellstatus in `processing`. |
| **[!UICONTROL Ship]** | Erstellt einen [Sendung](shipments.md#create-a-shipment)-Datensatz für die Bestellung. |
| **[!UICONTROL Reorder]** | Erstellt einen neuen ausstehenden Auftrag, der ein Duplikat des aktuellen ausstehenden Auftrags ist. |
| **[!UICONTROL Edit]** | Öffnet eine ausstehende Bestellung im Bearbeitungsmodus. Die Schaltfläche „Bearbeiten“ ist nur für ausstehende Bestellungen oder für Bestellungen auf der Grundlage von ausgehandelten [Angeboten](../b2b/quotes.md) verfügbar. |

{style="table-layout:auto"}

## Bearbeiten von Bestellungen

Eine Bestellung wird in einen `Processing` Status versetzt, wenn:

* Die Zahlung für eine Bestellung wird empfangen/erfasst und die Rechnung wird generiert - wenn die Zahlungsaktion auf `Authorize and Capture` gesetzt ist.
* Eine Auftragstransaktion ist autorisiert, aber die Zahlung wird noch nicht erfasst - wenn die Zahlungsaktion auf `Authorize` gesetzt ist.

Die [Konfiguration der Zahlungsaktion](../configuration-reference/sales/payment-methods.md#payment-actions) bestimmt, welche Bestellaktionen nach der Erstellung eines Auftrags verfügbar sind.

Sie können eine `Processing` Bestellung nicht wesentlich ändern, aber Sie können die Rechnungs- und Lieferadresse bearbeiten.

![Optionen für Verarbeitungsreihenfolge](./assets/order-button-bar-processing.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Wenn die Zahlungsaktion der Zahlungsmethode auf `Authorize and Capture` gesetzt ist, wird automatisch eine Rechnung erstellt, wenn der Kunde eine Bestellung aufgibt. In diesem Fall können Sie die Rückerstattung über eine [Gutschrift](credit-memo-create.md) vornehmen, die Bestellung jedoch nicht [stornieren](#cancel-a-pending-order) oder [stornieren](#void-a-processing-order).

| Schaltfläche | Beschreibung |
|--- |--- |
| **[!UICONTROL Back]** | Kehrt zur Seite Bestellungen zurück, ohne die Änderungen zu speichern. |
| **[!UICONTROL Send Email]** | Sendet eine E-Mail über die Bestellung an den Kunden. |
| **[!UICONTROL Void]** | [Voids](#void-a-processing-order) eine Auftragstransaktion oder eine Teilauftragstransaktion. |
| **[!UICONTROL Credit Memo]** | Startet den Prozess zum Erstellen einer [Gutschrift](credit-memo-create.md). |
| **[!UICONTROL Hold]**/**[!UICONTROL Unhold]** | Ändert den Status des Kundenauftrags in `On Hold`. Um die Sperre des Kundenauftrags aufzuheben, wählen Sie _[!UICONTROL Unhold]_&#x200B;aus. |
| **[!UICONTROL Reorder]** | Erstellt einen neuen ausstehenden Auftrag basierend auf dem aktuellen Auftrag. |
| **[!UICONTROL Create Returns]** | ![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Initiiert den Prozess zum [&#x200B; (](returns.md)) eines oder mehrerer Elemente aus der Bestellung. |

{style="table-layout:auto"}

## Aufheben einer Verarbeitungsreihenfolge

Wenn sich eine Bestellung noch im Status `Processing` befindet und die Zahlungsintegration auf `Authorize` (nicht `Authorize and Capture`) gesetzt ist, können Sie nur eine Transaktion stornieren oder eine Bestellung stornieren. [Durch das Stornieren einer Bestellung &#x200B;](#cancel-a-pending-order) auch die Autorisierung aufgehoben.

Wenn eine Bestellung mit einer Zahlungsmethode aufgegeben wird, bei der der Zahlungsvorgang auf `Authorize and Capture` gesetzt ist, können Sie das Guthaben per Gutschrift zurückerstatten, es jedoch nicht stornieren, da es in Rechnung gestellt und die Zahlung erfasst wird.

Ihre Zahlungsmethode bestimmt Ihre verfügbaren Zahlungsaktionen. Weitere Informationen [&#x200B; Sie unter &#x200B;](../configuration-reference/sales/payment-methods.md#payment-actions)Zahlungsaktionen“.

**_So heben Sie eine Bestellung auf:_**

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Klicken Sie in der Spalte **[!UICONTROL Action]** für die zu bearbeitende Bestellung auf **[!UICONTROL View]**.

1. Klicken Sie auf **[!UICONTROL Void]** , um die Bestellung zu stornieren.

1. Klicken Sie an der Eingabeaufforderung auf **[!UICONTROL OK]** , um die Bestellung zu stornieren.

Sie können alle erforderlichen Rückerstattungen über eine [Gutschrift](credit-memo-create.md) ausstellen, nachdem die Mittel erfasst wurden. Sie können auch eine [Warenrücksendeautorisierung (Return Merchandise Authorization, RMA) erstellen](returns.md) die für Produktrücksendungen ausgestellt wird. Weitere Informationen finden Sie unter [Verarbeitung einer Bestellung](order-processing.md).

## Ausstehende Bestellung bearbeiten

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Klicken Sie in der Spalte **[!UICONTROL Action]** für die zu bearbeitende Bestellung auf **[!UICONTROL View]**.

1. Klicken Sie auf **[!UICONTROL Edit]**.

   ![Reihenfolge bearbeiten](./assets/order-edit.png){width="600" zoomable="yes"}

1. Klicken Sie an der Eingabeaufforderung auf **[!UICONTROL OK]** , um mit der Bearbeitung fortzufahren.

1. Aktualisieren Sie die Reihenfolge nach Bedarf.

1. Übernehmen Sie Ihre Änderungen:
   * Um Änderungen an der Rechnungs- oder Lieferadresse zu speichern, klicken Sie auf **[!UICONTROL Save]**.
   * Um Änderungen an Zeileneinträgen zu speichern und die Bestellung erneut zu verarbeiten, klicken Sie auf **[!UICONTROL Submit Order]**.

## Bestellung zurückstellen

Wenn die bevorzugte Zahlungsmethode des Kunden nicht verfügbar ist oder der Artikel vorübergehend nicht vorrätig ist, können Sie die Bestellung zurückstellen.

1. Suchen Sie im _Bestellungen_ die `Pending` Bestellung, die Sie zurückstellen möchten.

1. Klicken Sie in _Spalte_ Aktion **[!UICONTROL View]** auf.

1. Klicken Sie auf **[!UICONTROL Hold]** , um den Auftrag zurückzusetzen.

Um die Sperre einer Bestellung aufzuheben, bearbeiten Sie die Bestellung erneut und klicken Sie auf **[!UICONTROL Unhold]**.

## Ausstehende Bestellung stornieren

Beim Abbrechen einer Bestellung ändert sich ihr Status von `Pending` in `Canceled`.

1. Suchen Sie im _[!UICONTROL Orders]_&#x200B;Raster nach der ausstehenden Bestellung, die storniert werden soll.

1. Klicken Sie in der Spalte _[!UICONTROL Action]_&#x200B;auf **[!UICONTROL View]**.

1. Klicken Sie auf **[!UICONTROL Cancel]** , um die Bestellung abzubrechen.

Der Status der Bestellung ist jetzt `Canceled`.
