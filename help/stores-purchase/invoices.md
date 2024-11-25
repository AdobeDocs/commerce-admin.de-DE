---
title: Rechnungen
description: Erfahren Sie, wie Sie Rechnungen erstellen und drucken können, um die Auftragsverarbeitung und den Kundendienst zu unterstützen.
exl-id: 6141b182-1467-4416-a07f-864333318428
feature: Invoices, Admin Workspace
source-git-commit: f8254db7d69e58c8e9a78948ee6e40f5ea88cea0
workflow-type: tm+mt
source-wordcount: '1072'
ht-degree: 0%

---

# Rechnungen

Eine Rechnung ist eine Aufzeichnung der Zahlungsaufzeichnungen für eine Bestellung. Mehrere Rechnungen können [für eine einzelne Bestellung erstellt](#create-an-invoice) werden und jeweils beliebig viele oder nur wenige der gekauften Produkte enthalten, die Sie angeben. Sie können auch [druckfertige PDF-Rechnungen](#print-invoices) als Verkaufsdokumente für Ihre Kunden erstellen.

Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Sales]** > _Vorgänge_ > **Rechnungen** , um das Raster _Rechnungen_ zu öffnen und auf Ihre erstellten Rechnungen zuzugreifen.

![Rechnungen grid](./assets/invoices.png){width="700" zoomable="yes"}

## Spaltenbeschreibungen

| Spalte | Beschreibung |
|--- |--- |
| [!UICONTROL Select] | Aktivieren Sie die Kontrollkästchen für die Anführungszeichen, die einer Aktion unterzogen werden sollen, oder verwenden Sie das Auswahlsteuerelement in der Spaltenüberschrift. Optionen: `Select All` / `Deselect All` |
| [!UICONTROL Invoice] | Eine eindeutige numerische Kennung, die zugewiesen wird, wenn eine Rechnung vom Administrator übermittelt wird. Bei Ansicht der Rechnungsdetails wird diese Zahl oben auf der Seite anstelle des Anführungszeichens angezeigt. |
| [!UICONTROL Invoice Date] | Datum und Uhrzeit der ersten Übermittlung der Rechnung durch den Administrator. |
| [!UICONTROL Order#] | Eine eindeutige numerische Kennung, die zugewiesen wird, wenn ein Käufer eine Bestellung aufgibt. Bei der Anzeige der Rechnungsdetails erscheint diese Zahl als Link im Bereich &quot;Bestellinformationen und Kontoinformationen&quot;. |
| [!UICONTROL Order Date] | Datum und Uhrzeit der ersten erfolgreichen Auftragserteilung durch den Kunden. |
| [!UICONTROL Bill-to Name] | Der Name der Person, die für die Bestellung verantwortlich ist. |
| [!UICONTROL Status] | Gibt den aktuellen Status einer Rechnung an. Der Status kann nur durch Handlung des Käufers oder Verkäufers geändert werden. |
| [!UICONTROL Grand Total (Base)] | Der Gesamtpreis der zu kaufenden Produkte. Der Gesamtbetrag wird in der Basiswährung der Website und in der Währung der Storefront angezeigt. |
| [!UICONTROL Grand Total (purchase)] | Die Gesamtsumme der in der Bestellung gekauften Produkte. Der Gesamtbetrag wird in der Basiswährung der Website und in der Währung der Storefront angezeigt. |
| [!UICONTROL Purchased From] | Die Website-/Store-/Store-Ansicht, aus der die Rechnung erstellt wurde. |
| [!UICONTROL Billing Address] | Die Rechnungsadresse des Kunden, der die Bestellung aufgegeben hat. |
| [!UICONTROL Shipping Address] | Die Adresse, an die die Bestellung versandt werden soll. |
| [!UICONTROL Customer Name] | Vor- und Nachname des Kunden, der die Rechnung erhält. |
| [!UICONTROL Email] | Die E-Mail-Adresse des Kunden, der die Rechnung erhält. |
| [!UICONTROL Customer Group] | Die Kundengruppe, die dem Kunden zugewiesen wurde, der die Rechnung erhält. |
| [!UICONTROL Payment Method] | Die Zahlungsmethode, die für die Zahlung verwendet wird. |
| [!UICONTROL Shipping Information] | Die zum Versand der Bestellung verwendete Methode. |
| [!UICONTROL Subtotal] | Die Teilsumme der Bestellungen, ohne Versand und Bearbeitung, sowie Steuern. |
| [!UICONTROL Shipping and Handling] | Der für Versand und Bearbeitung berechnete Betrag. |
| [!UICONTROL Action] | **[!UICONTROL View]** - öffnet die Rechnung im Bearbeitungsmodus. |

{style="table-layout:auto"}

## Rechnung erstellen

Wenn Sie eine Rechnung für eine Bestellung erstellen, wird sie in einen Status versetzt, in dem sie nicht storniert oder geändert werden kann. Eine neue Rechnungsseite ähnelt einer abgeschlossenen Bestellung mit einigen zusätzlichen Feldern. Jede Aktivität im Zusammenhang mit einer Bestellung wird im Abschnitt Kommentare der Rechnung angegeben.

Normalerweise werden Bestellungen bei Beginn des Versandvorgangs in Rechnung gestellt und erfasst. Wenn es sich bei der Zahlungsmethode um eine Bestellung handelt oder die [Zahlungsaktion](../configuration-reference/sales/payment-methods.md#payment-actions) auf `Authorize and Capture` festgelegt ist, wird die Bestellung in Rechnung gestellt und die Zahlung während des Checkout erfasst. Sie können eine Rechnung mit einem Verpackungsschein generieren und auch Versandtitel von Ihrem Betreiberkonto ausdrucken. Eine einzige Bestellung kann in Teilsendungen unterteilt werden, die bei Bedarf gesondert in Rechnung gestellt werden.

Wenn der Status neuer Bestellungen auf `Processing` festgelegt ist, wird die Option auf _Alle Elemente automatisch aufrechnen_ in der Konfiguration verfügbar. Einige Kreditkartenzahlmethoden schließen den Rechnungsschritt als Teil des Prozesses ab, wenn die [Zahlungsaktion](../configuration-reference/sales/payment-methods.md#payment-actions) auf `Authorize and Capture` gesetzt ist. In diesem Fall wird die Schaltfläche Rechnungsstellung nicht angezeigt und die Bestellung kann versandbereit sein.

>[!NOTE]
>
>Rechnungen werden nicht automatisch für Bestellungen erstellt, die mit `Gift Card`, `Store Credit`, `Reward Points` oder anderen Offline-Zahlungsmethoden aufgegeben werden.

Eine Rechnung für die Bestellung muss vor dem Drucken erstellt werden. Um das PDF anzuzeigen oder zu drucken, laden Sie zunächst einen PDF-Reader wie [Adobe Acrobat Reader][1] herunter und installieren Sie ihn.

**_So berechnen Sie eine Bestellung:_**

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Suchen Sie die Verkaufsreihenfolge mit dem Status &quot;`Processing`&quot; im Raster. Führen Sie dann die folgenden Schritte aus:

1. Klicken Sie in der Spalte _Aktion_ auf **[!UICONTROL View]**.

1. Wählen Sie in der Kopfzeile des Verkaufsauftrags die Option **[!UICONTROL Invoice]** aus.

   >[!NOTE]
   >
   >Die Option _[!UICONTROL Invoice]_wird nicht angezeigt, wenn die [Zahlungsaktion](../configuration-reference/sales/payment-methods.md#payment-actions) für Ihre spezifische [Zahlungsmethode](../configuration-reference/sales/payment-methods.md) auf `Authorize and Capture` gesetzt ist, wodurch automatisch eine Rechnung generiert wird. Dies ist auch der Fall, wenn die Bestellung aufgegeben wird und die Zahlungsaktion für Ihre Zahlungsmethode auf `Authorize` gesetzt ist und die Bestellung in Rechnung gestellt wird.

   ![Invoice Sales Order](./assets/invoice-sales-order.png){width="700" zoomable="yes"}

   Die neue Rechnungsseite ähnelt einer abgeschlossenen Bestellseite mit zusätzlichen Feldern, die bearbeitet werden können.

1. Wenn die Artikel versandbereit sind, erstellen Sie gleichzeitig mit der Erstellung der Rechnung einen Verpackungsschein für die Sendung:

   - Klicken Sie im Abschnitt _Versandinformationen_ auf das Kontrollkästchen **[!UICONTROL Create Shipment]** , um es auszuwählen.

     Der Versanddatensatz wird gleichzeitig mit der Erstellung der Rechnung erstellt.

   - Fügen Sie eine Trackingnummer hinzu:

      - Klicken Sie auf **[!UICONTROL Add Tracking Number]**.
      - Geben Sie die Tracking-Informationen ein: _[!UICONTROL Carrier]_,_[!UICONTROL Title]_ und _[!UICONTROL Number]_

     ![Erstellen einer Fedex-Sendung](./assets/invoice-create-shipment-fedex.png){width="600" zoomable="yes"}

   - Optional können Sie eine Teilrechnung erstellen:

      - Aktualisieren Sie im Abschnitt _Elemente zur Rechnung_ die Spalte **[!UICONTROL Qty to Invoice]**, um nur bestimmte Elemente auf der Rechnung einzuschließen.
      - Klicken Sie dann auf **[!UICONTROL Update Qty's]**.

        ![Zu belastende Elemente](./assets/invoice-items-to-invoice.png){width="600" zoomable="yes"}

1. Wenn für die Bestellung eine Online-Zahlungsmethode verwendet wurde, setzen Sie **[!UICONTROL Amount]** auf die entsprechende Option.

1. Gehen Sie wie folgt vor, um Kunden per E-Mail zu benachrichtigen, wenn die Rechnung erstellt wird:

   - Aktivieren Sie das Kontrollkästchen **[!UICONTROL Email Copy of Invoice]** .

   - Geben Sie beliebige **[!UICONTROL Invoice Comments]** ein. Um die Kommentare in die Benachrichtigungs-E-Mail aufzunehmen, aktivieren Sie das Kontrollkästchen **[!UICONTROL Append Comments]** .

1. Klicken Sie nach Abschluss des Vorgangs unten auf der Seite auf **[!UICONTROL Submit Invoice]** .

   **_Online-Zahlungsmethode:_**

   ![Rechnung einreichen - Online-Zahlungsmethode](./assets/invoice-submit-invoice-capture-online.png){width="600" zoomable="yes"}

   **_Offline-Zahlungsmethode:_**

   ![Rechnungen übermitteln - Offline-Zahlungsmethode)](./assets/invoice-submit-invoice.png){width="600" zoomable="yes"}

   Der Status der Reihenfolge ändert sich von `Pending` in `Complete`.

   ![Abgeschlossene Rechnungszusammenfassung](./assets/invoice-complete.png){width="600" zoomable="yes"}

## Druckrechnungen

Rechnungen können einzeln oder als Stapel gedruckt werden. Bevor eine Rechnung jedoch gedruckt werden kann, muss sie zunächst für die Bestellung generiert werden. Sie können ein hochauflösendes Logo für eine druckfertige PDF-Rechnung hochladen und die [Bestell-ID](../stores-purchase/sales-documents.md#add-reference-ids) in die Kopfzeile einschließen. Informationen zum Anpassen der Rechnungsvorlage mit Ihrem Logo und Ihrer Adresse finden Sie unter [PDF Logo Requirements](../stores-purchase/sales-documents.md#image-formats).

>[!NOTE]
>
>Um die PDF anzeigen oder drucken zu können, benötigen Sie einen PDF-Reader. Sie können [Adobe Reader][1] kostenlos herunterladen.

### Eine einzelne Rechnung drucken

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Invoices]**.

1. Suchen Sie im Raster _[!UICONTROL Invoices]_die Rechnung und klicken Sie in der Spalte_ Aktion _auf **[!UICONTROL View]**.

1. Klicken Sie oben auf der Rechnung auf **[!UICONTROL Print]** , um eine PDF der Rechnung zu generieren.

1. Speichern Sie die generierte PDF in einer Datei oder drucken Sie sie.

### Mehrere Rechnungen drucken

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Invoices]**.

1. Aktivieren Sie im Raster _[!UICONTROL Invoices]_das Kontrollkästchen für jede Rechnung, die gedruckt werden soll.

1. Setzen Sie das Steuerelement **[!UICONTROL Actions]** auf `PDF Invoices`.

   ![Mehrere Rechnungen drucken](./assets/invoices-print-batch.png){width="600" zoomable="yes"}

Die Rechnungen werden in einer einzigen PDF-Datei gespeichert, die an einen Drucker gesendet oder gespeichert werden kann.

[1]: https://www.adobe.com/acrobat/pdf-reader.html "Adobe Reader abrufen"
