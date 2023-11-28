---
title: Rechnungen
description: Erfahren Sie, wie Sie Rechnungen erstellen und drucken können, um die Auftragsverarbeitung und den Kundendienst zu unterstützen.
exl-id: 6141b182-1467-4416-a07f-864333318428
feature: Invoices, Admin Workspace
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1155'
ht-degree: 0%

---

# Rechnungen

Eine Rechnung ist eine Aufzeichnung der Zahlungsaufzeichnungen für eine Bestellung. Mehrere Rechnungen können [created](#create-an-invoice) für eine einzelne Bestellung und jede kann beliebig viele oder nur wenige der von Ihnen angegebenen gekauften Produkte enthalten. Sie können auch [druckfertige PDF-Rechnungen](#print-invoices) als Verkaufsdokumente für Ihre Kunden.

Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Sales]** > _Aktivitäten_ > **Rechnungen** , um die _Rechnungen_ und greifen Sie auf Ihre erstellten Rechnungen zu.

![Rechnungsraster](./assets/invoices.png){width="700" zoomable="yes"}

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

Normalerweise werden Bestellungen bei Beginn des Versandvorgangs in Rechnung gestellt und erfasst. Wenn es sich bei der Zahlungsmethode um einen Kaufauftrag handelt oder wenn die [Zahlungsaktion](../configuration-reference/sales/payment-methods.md#payment-actions) auf `Authorize and Capture`, wird die Bestellung fakturiert und die Zahlung beim Checkout erfasst. Sie können eine Rechnung mit einem Verpackungsschein generieren und auch Versandtitel von Ihrem Betreiberkonto ausdrucken. Eine einzige Bestellung kann in Teilsendungen unterteilt werden, die bei Bedarf gesondert in Rechnung gestellt werden.

Wenn der Status neuer Bestellungen auf `Processing`, die Option _Automatisch alle Elemente einrechnen_ wird in der Konfiguration verfügbar. Einige Kreditkartenzahlmethoden schließen den Rechnungsschritt als Teil des Prozesses ab, wenn die [Zahlungsaktion](../configuration-reference/sales/payment-methods.md#payment-actions) auf `Authorize and Capture`. In diesem Fall wird die Schaltfläche Rechnungsstellung nicht angezeigt und die Bestellung kann versandbereit sein.

>[!NOTE]
>
>Rechnungen werden nicht automatisch für Bestellungen erstellt, die mithilfe von `Gift Card`, `Store Credit`, `Reward Points`oder anderen Offline-Zahlungsmethoden.

Eine Rechnung für die Bestellung muss vor dem Drucken erstellt werden. Laden Sie zum Anzeigen oder Drucken des PDF zunächst einen PDF-Reader herunter und installieren Sie ihn, z. B. [Adobe Acrobat Reader][1].

**_So berechnen Sie eine Bestellung:_**

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Suchen Sie nach der Bestellung mit dem Status `Processing` im Raster. Führen Sie dann die folgenden Schritte aus:

1. Im _Aktion_ Spalte, klicken **[!UICONTROL View]**.

1. Wählen Sie in der Kopfzeile des Verkaufsauftrags die **[!UICONTROL Invoice]** -Option.

   >[!NOTE]
   >
   >Die _[!UICONTROL Invoice]_wird nicht angezeigt, wenn die [Zahlungsaktion](../configuration-reference/sales/payment-methods.md#payment-actions) für Ihre [Zahlungsmethode](../configuration-reference/sales/payment-methods.md) auf `Authorize and Capture`, wodurch automatisch eine Rechnung generiert wird. Dies ist auch der Fall, wenn die Bestellung aufgegeben wird und die Zahlungsaktion für Ihre Zahlungsmethode auf `Authorize` und die Bestellung in Rechnung gestellt wird.

   ![Rechnungsverkaufsauftrag](./assets/invoice-sales-order.png){width="700" zoomable="yes"}

   Die neue Rechnungsseite ähnelt einer abgeschlossenen Bestellseite mit zusätzlichen Feldern, die bearbeitet werden können.

1. Wenn die Artikel versandbereit sind, erstellen Sie gleichzeitig mit der Erstellung der Rechnung einen Verpackungsschein für die Sendung:

   - Im _Versandinformationen_ klicken Sie auf die **[!UICONTROL Create Shipment]** aktivieren, um es auszuwählen.

     Der Versanddatensatz wird gleichzeitig mit der Erstellung der Rechnung erstellt.

   - Fügen Sie eine Trackingnummer hinzu:

      - Klicken **[!UICONTROL Add Tracking Number]**.
      - Geben Sie die Tracking-Informationen ein: _[!UICONTROL Carrier]_,_[!UICONTROL Title]_, und _[!UICONTROL Number]_

     ![Erstellen einer Fedex-Sendung](./assets/invoice-create-shipment-fedex.png){width="600" zoomable="yes"}

   - Optional können Sie eine Teilrechnung erstellen:

      - Im _Rechnungselemente_ -Abschnitt aktualisieren Sie die **[!UICONTROL Qty to Invoice]** -Spalte, um nur bestimmte Elemente auf der Rechnung aufzunehmen.
      - Klicken Sie anschließend auf **[!UICONTROL Update Qty's]**.

        ![Rechnungselemente](./assets/invoice-items-to-invoice.png){width="600" zoomable="yes"}

1. Wenn für die Bestellung eine Online-Zahlungsmethode verwendet wurde, legen Sie **[!UICONTROL Amount]** zur entsprechenden Option.

1. Gehen Sie wie folgt vor, um Kunden per E-Mail zu benachrichtigen, wenn die Rechnung erstellt wird:

   - Wählen Sie die **[!UICONTROL Email Copy of Invoice]** aktivieren.

   - Beliebige eingeben **[!UICONTROL Invoice Comments]**. Um die Kommentare in die Benachrichtigungs-E-Mail aufzunehmen, markieren Sie die **[!UICONTROL Append Comments]** aktivieren.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Submit Invoice]** unten auf der Seite.

   **_Online-Zahlungsmethode:_**

   ![Submit Invoice - Online-Zahlungsmethode](./assets/invoice-submit-invoice-capture-online.png){width="600" zoomable="yes"}

   **_Offline-Zahlungsmethode:_**

   ![Submit Invoice - Offline-Zahlungsmethode](./assets/invoice-submit-invoice.png){width="600" zoomable="yes"}

   Der Status der Bestellung ändert sich von `Pending` nach `Complete`.

   ![Abgeschlossene Rechnungszusammenfassung](./assets/invoice-complete.png){width="600" zoomable="yes"}

## Druckrechnungen

Rechnungen können einzeln oder als Stapel gedruckt werden. Bevor eine Rechnung jedoch gedruckt werden kann, muss sie zunächst für die Bestellung generiert werden. Sie können ein hochauflösendes Logo für eine druckfertige PDF-Rechnung hochladen und die [Auftrags-ID](../stores-purchase/sales-documents.md#add-reference-ids) in der Kopfzeile. Informationen zum Anpassen der Rechnungsvorlage mit Ihrem Logo und Ihrer Adresse finden Sie unter [PDF-Logo-Anforderungen](../stores-purchase/sales-documents.md#image-formats).

>[!NOTE]
>
>Um die PDF anzeigen oder drucken zu können, benötigen Sie einen PDF-Reader. Sie können [Adobe Reader][1] kostenlos.

### Eine einzelne Rechnung drucken

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Invoices]**.

1. Im _[!UICONTROL Invoices]_Raster, Rechnung suchen und klicken **[!UICONTROL View]**im_ Aktion _Spalte.

1. Klicken Sie oben auf der Rechnung auf **[!UICONTROL Print]** , um eine PDF der Rechnung zu generieren.

1. Speichern Sie die generierte PDF in einer Datei oder drucken Sie sie.

### Mehrere Rechnungen drucken

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Invoices]**.

1. Im _[!UICONTROL Invoices]_ausfüllen, aktivieren Sie das Kontrollkästchen für jede zu druckende Rechnung.

1. Legen Sie die **[!UICONTROL Actions]** Kontrolle an `PDF Invoices`.

   ![Mehrere Rechnungen drucken](./assets/invoices-print-batch.png){width="600" zoomable="yes"}

Die Rechnungen werden in einer einzigen PDF-Datei gespeichert, die an einen Drucker gesendet oder gespeichert werden kann.

## Fehlerbehebung bei Ressourcen

Hilfe zur Fehlerbehebung bei Rechnungsproblemen finden Sie unter folgenden Themen _Knowledge Base für Commerce-Support_ Artikel:

- [Bundle-Produkte können nicht virtuell und einfach berechnet werden](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-9/mdva-30889-magento-patch-can-t-invoice-bundle-products-virtual-and-simple.html)
- [Rechnungsstellung ohne Store-Kreditdaten](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-8/mdva-31150-magento-patch-invoice-without-store-credit-info.html)
- [Die Steuer wird auf der Rechnung mit 100 % Rabatt angezeigt](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-22/mdva-35773-tax-appears-on-invoice-with-100-discount.html)
- [Bestellrechnungen werden nicht automatisch gesendet](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-13/mdva-32545-magento-patch-order-invoices-don-t-send-automatically.html)


[1]: https://www.adobe.com/acrobat/pdf-reader.html "Adobe Reader abrufen"
