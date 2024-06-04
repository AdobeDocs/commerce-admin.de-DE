---
title: Ein Kreditmemo ausgeben
description: Erfahren Sie, wie Sie ein Kreditmemo für eine fakturierte Bestellung generieren und drucken.
exl-id: 84ec72ba-7f72-4fa1-a9bf-91c17f43a3a7
feature: Orders, Invoices
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '2132'
ht-degree: 0%

---

# Ein Kreditmemo ausgeben

Bevor ein Kreditmemo gedruckt werden kann, muss es zunächst für eine [Rechnungsstellung](invoices.md#create-an-invoice). Sie können je nach Zahlungsmethode sowohl Online- als auch Offline-Erstattungen (teilweise oder vollständig) aus einem offenen Kreditmemo ausstellen.

- ![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce) Erstattungen können auf die Kreditspeicherung angewendet werden.
- ![Adobe Commerce B2B](../assets/b2b.svg) (Verfügbar mit Adobe Commerce B2B) Rückerstattungen können auf Firmenkredite angewendet werden.
- Mit Kreditkarte getätigte Käufe können entweder online oder offline zurückerstattet werden.
- Käufe, die per Scheck oder Geldbestellung getätigt werden, müssen offline zurückerstattet werden.

Beliebiges Kreditmemo mit einer [Öffnungsstatus](order-status.md) eine ausstehende Rückerstattung fällig ist.

Mit Kreditkarten können Sie:

- Den vollen Rechnungsbetrag zurückerstatten.
- Erstattung eines Teilbetrags der Rechnung.
- Rückerstattung mehrerer Teilbeträge einer Rechnung.
- Rückerstattung mehrerer Rechnungen pro Bestellung, um den Gesamtbetrag der Bestellung nicht zu überschreiten.
- Erstattet einen Teil der Menge für einen Zeileneintrag, z. B. drei der fünf Hemden in einer Bestellung.

Siehe [Rechnung erstellen](invoices.md#create-an-invoice) für weitere Informationen.

## Einstellung der Zahlungsaktion

Der Erstattungs-Workflow für Bestellungen, die per Kreditkarte bestellt werden, wird durch die Variable [Einstellung der Zahlungsaktion](../configuration-reference/sales/payment-methods.md#payment-actions) in der Konfiguration für jede verfügbare Zahlungsmethode. Rückerstattungen können erst nach Abwicklung der Transaktion ausgegeben werden.

![Einstellung der Zahlungsaktion](./assets/payment-action-setting.png){width="600" zoomable="yes"}

- Wenn die Zahlungsaktion für die konfigurierte Zahlungsmethode auf `Authorize`müssen Sie zunächst die Rechnung vom Administrator generieren, bevor ein Kreditmemo erstellt werden kann.
- Wenn die Zahlungsaktion für Ihre konfigurierte Zahlungsmethode auf `Authorize and Capture`, wurde die Rechnung bereits vom Zahlungsverarbeiter erstellt, aber die Mittel sind erst verfügbar, wenn die Transaktion abgewickelt wurde. Diese kurze Wartezeit wird von vielen Zahlungsverarbeitern als Sicherheitsmaßnahme empfohlen und kann normalerweise automatisch durchgeführt werden. Transaktionen können auch manuell von Ihrem Händlerkonto beim Zahlungsverarbeiter abgewickelt werden.
- ![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce) Wenn Sie eine Kreditkarte für eine Bestellung erstellen, die Geschenkoptionen enthält, wird die Rückerstattung für die Geschenkverpackung und/oder die gedruckte Karte im Abschnitt Rückerstattungssummen des Kreditkarten-Memos angezeigt. Um diese Kosten von dem zurückzuerstattenden Betrag auszuschließen, geben Sie den Betrag als Anpassungsgebühr an. Wenn mehrere Kreditkarten für dieselbe Bestellung ausgegeben werden, erscheint die Rückerstattung für Geschenkgutscheine nur in der ersten Kreditkarte.

## Erstellen Sie ein Kreditmemo

Bestimmen Sie die Art der Rückerstattung, die Sie vornehmen möchten - für eine [Kreditkauf](#issue-a-refund-for-a-credit-purchase) oder [Scheck- oder Geldbestellung](#issue-an-offline-refund-for-check-or-money-order)- und generieren Sie das Kreditmemo und geben Sie eine Rückerstattung.

### Rückerstattung für einen Kreditkauf

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

   ![Raster &quot;Bestellungen&quot;](./assets/orders-grid.png){width="700" zoomable="yes"}

1. Suchen Sie die Reihenfolge im Raster und klicken Sie auf **[!UICONTROL View]**.

1. Wenn die Variable _[!UICONTROL Credit Memo]_-Schaltfläche in der Schaltflächenleiste angezeigt wird, führen Sie einen der folgenden Schritte aus:

   - So erstellen Sie eine `offline` Rückerstattung, gehen Sie zu Schritt 6.
   - So erstellen Sie eine `online` Rückerstattung, fahren Sie mit Schritt 4 fort.

   Siehe [Credit Memos](credit-memos.md) für weitere Informationen zu Offline- und Online-Erstattungen.

1. Klicks **[!UICONTROL Invoices]** im linken Bereich.

1. Suchen Sie die Rechnung im Raster und klicken Sie auf **[!UICONTROL View]**.

   ![Rechnungsraster](./assets/order-invoices-grid.png){width="700" zoomable="yes"}

1. Scrollen Sie nach unten zum **[!UICONTROL Invoice Totals]** überprüfen Sie, ob die Rechnung auf `Capture Online`und klicken Sie auf **[!UICONTROL Submit Invoice]**.

   ![Online erfassen](./assets/order-invoice-capture-online.png){width="600" zoomable="yes"}

   Wenn diese Option nicht verfügbar ist, wird die Rechnung bereits erstellt. Fahren Sie mit dem nächsten Schritt fort.

1. Klicken Sie in der Schaltflächenleiste oben auf der Rechnung auf **[!UICONTROL Credit Memo]**.

1. Überprüfen Sie die Informationen in der **[!UICONTROL Items to Refund]** und führen Sie gegebenenfalls folgende Schritte aus:

   - Um das Produkt in den Bestand zu bringen, wählen Sie die **[!UICONTROL Return to Stock]** aktivieren.

     Das Produkt wird automatisch auf Lager zurückgesetzt, wenn _Optionen für Produktspeicher_ auf `Automatically Return Credit Memo Item to Stock`. Mit [Inventory management aktiviert](../inventory-management/enable.md), kehrt der Artikel an die Quelle zurück, an die die Sendung versandt wurde.

   - Aktualisieren Sie die **[!UICONTROL Qty to Refund]** und klicken Sie auf **[!UICONTROL Update Qty's]**.

     ![Erstattungsbeträge](./assets/invoice-credit-memo-items-to-refund.png){width="600" zoomable="yes"}

1. Aktualisieren Sie die **[!UICONTROL Refunds Totals]** wie folgt:

   - Für **[!UICONTROL Refund Shipping]**, geben Sie einen Betrag ein, der von der Versandgebühr zurückerstattet werden soll.

     In diesem Feld wird zunächst der gesamte Versandbetrag aus der Bestellung angezeigt, die zur Rückerstattung verfügbar ist. Sie entspricht dem vollen Versandbetrag aus der Bestellung abzüglich des bereits zurückerstatteten Versandbetrags. Wie die Menge kann der Betrag reduziert, aber nicht erhöht werden.

   - Für **[!UICONTROL Adjustment Refund]** Geben Sie einen Wert an, der dem erstatteten Gesamtbetrag zuzüglich einer zusätzlichen Erstattung hinzugefügt werden soll, die für einen bestimmten Teil der Bestellung (Versand, Artikel oder Steuern) nicht gilt. Es kann auch für die teilweise Rückerstattung mit virtuellem Geld, wie eine Geschenkkarte, verwendet werden, wenn ein Administrator eine nicht virtuelle Zahlungsmethode zuerst zurückzahlen möchte.

     Der angegebene Betrag kann die Gesamtrückerstattung nicht über den gezahlten Betrag erhöhen.

   - Für **[!UICONTROL Adjustment Fee]**, geben Sie einen Wert an, der vom erstatteten Gesamtbetrag abgezogen werden soll.

     Dieser Betrag wird nicht von einem bestimmten Teil der Bestellung abgezogen, z. B. Versand, Artikel oder Steuern.

1. Um einen Kommentar hinzuzufügen, geben Sie den Text im **[!UICONTROL Credit Memo Comments]** ankreuzen.

   - Um eine E-Mail-Benachrichtigung an den Kunden zu senden, wählen Sie die **[!UICONTROL Email Copy of Credit Memo]** aktivieren.

1. Klicks **[!UICONTROL Update Totals]**.

1. Führen Sie gegebenenfalls folgende Schritte aus:

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce) Um den Betrag an das Kundenkonto-Guthaben zurückzuerstatten, wählen Sie die **[!UICONTROL Refund to Store Credit]** aktivieren.

   - ![Adobe Commerce B2B](../assets/b2b.svg) (Verfügbar mit Adobe Commerce B2B) Um den Betrag auf das Firmenguthaben des Kunden zurückzuerstatten, wählen Sie die **[!UICONTROL Refund to Company Credit]** aktivieren.

   - Klicken Sie auf , um die Offline-Rückerstattung zu beantragen. **[!UICONTROL Refund Offline]**.

   - Um eine Online-Rückerstattung zu erteilen, klicken Sie auf **[!UICONTROL Refund]**.

   - ![Adobe Commerce B2B](../assets/b2b.svg) (Verfügbar bei Adobe Commerce B2B) Wenn der Kauf mit Firmenguthaben bezahlt wurde, klicken Sie auf **[!UICONTROL Refund to Company Credit]**.

   Siehe [Credit Memos](credit-memos.md) für weitere Informationen zu Offline- und Online-Erstattungen.

   ![Gesamtrückerstattung](./assets/credit-memo-order-total-refund.png){width="600" zoomable="yes"}

### Offline-Rückerstattung für Scheck- oder Geldbestellung

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Suchen Sie die abgeschlossene Reihenfolge im Raster und öffnen Sie sie durch Klicken auf die **[!UICONTROL View]** -Link.

1. Klicken Sie in der Schaltflächenleiste oben auf der Seite auf **[!UICONTROL Invoice]**.

1. Scrollen Sie nach unten zum unteren Seitenrand und klicken Sie auf **[!UICONTROL Submit Invoice]**.

1. Klicken Sie in der Schaltflächenleiste oben auf der Rechnung auf **[!UICONTROL Credit Memo]**.

   ![Erstellen eines Credit Memo](./assets/order-invoice-info-company.png){width="600" zoomable="yes"}

1. Überprüfen Sie die Informationen in der **[!UICONTROL Items to Refund]** und führen Sie gegebenenfalls folgende Schritte aus:

   ![Erstattungsbeträge](./assets/credit-memo-items-to-refund.png){width="600" zoomable="yes"}

   - Wählen Sie die **[!UICONTROL Return to Stock]** aktivieren, wenn Sie das zurückgegebene Produkt in den Bestand zurückgeben möchten.

     Wenn Inventory management aktiviert ist, wird die Lagerbestandsmenge an die Quelle zurückgegeben, an die die Sendung gesendet wurde. Das Produkt wird automatisch auf Lager zurückgesetzt, wenn [Optionen für Produktspeicher](../inventory-management/enable.md) auf `Automatically Return Credit Memo Item to Stock`.

   - Aktualisieren Sie die **[!UICONTROL Qty to Refund]** und klicken **[!UICONTROL Update Qty's]**.

     Der zu erstattende Betrag darf den zur Erstattung verfügbaren Höchstbetrag nicht überschreiten.

1. Aktualisieren Sie die **[!UICONTROL Refunds Totals]** gegebenenfalls:

   - Für **[!UICONTROL Refund Shipping]**, geben Sie einen Betrag ein, der von der Versandgebühr zurückerstattet werden soll.

     In diesem Feld wird zunächst der gesamte Versandbetrag aus der Bestellung angezeigt, die zur Rückerstattung verfügbar ist. Sie entspricht dem vollen Versandbetrag aus der Bestellung abzüglich des bereits zurückerstatteten Versandbetrags. Wie die Menge kann der Betrag reduziert, aber nicht erhöht werden.

   - Für **[!UICONTROL Adjustment Refund]** Geben Sie einen Wert an, der dem erstatteten Gesamtbetrag zuzüglich einer zusätzlichen Erstattung hinzugefügt werden soll, die für einen bestimmten Teil der Bestellung (Versand, Artikel oder Steuern) nicht gilt. Es kann auch für die teilweise Rückerstattung mit virtuellem Geld, wie eine Geschenkkarte, verwendet werden, wenn ein Administrator eine nicht virtuelle Zahlungsmethode zuerst zurückzahlen möchte.

     Der angegebene Betrag kann die Gesamtrückerstattung nicht über den gezahlten Betrag erhöhen.

   - Für **[!UICONTROL Adjustment Fee]**, geben Sie einen Wert an, der vom erstatteten Gesamtbetrag abgezogen werden soll.

     Dieser Betrag wird nicht von einem bestimmten Teil der Bestellung abgezogen, z. B. Versand, Artikel oder Steuern.

   - Wenn der Kauf mit einem Store-Guthaben bezahlt wurde, wählen Sie die **[!UICONTROL Refund to Store Credit]** das Kontrollkästchen, um den Betrag dem Kundenkonto-Kontostand zuzuordnen.

1. Um einen Kommentar hinzuzufügen, geben Sie den Text im **[!UICONTROL Credit Memo Comments]** und gehen Sie wie folgt vor:

   - Um eine E-Mail-Benachrichtigung an den Kunden zu senden, wählen Sie die **[!UICONTROL Email Copy of Credit Memo]** aktivieren.

   - Um die in die E-Mail eingegebenen Kommentare einzuschließen, wählen Sie die **[!UICONTROL Append Comments]** aktivieren.

     Der Status einer Benachrichtigung über ein Kreditmemo wird im abgeschlossenen Kreditmemo neben der Kreditmemo-Nummer angezeigt.

     ![Erstattungssummen](./assets/credit-memo-order-totals.png){width="600" zoomable="yes"}

1. Um den Vorgang abzuschließen und die Erstattung zu erteilen, klicken Sie auf **[!UICONTROL Refund Offline]**.

## Feldbeschreibungen

### [!UICONTROL Order & Account Information]

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Order Number] | Die Bestellnummer wird im _Bestellungen und Kontoinformationen_, gefolgt von einem Hinweis, der angibt, ob die Bestätigungs-E-Mail gesendet wurde. |
| [!UICONTROL Order Date] | Datum und Uhrzeit der Bestellung. |
| [!UICONTROL Order Status] | Gibt den Bestellstatus als `Complete`. |
| [!UICONTROL Purchased From] | Gibt die Website-, Store- und Store-Ansicht an, in der die Bestellung aufgegeben wurde. |
| [!UICONTROL Placed from IP] | Gibt die IP-Adresse des Computers an, von dem aus die Bestellung aufgegeben wurde. |

{style="table-layout:auto"}

### [!UICONTROL Account Information]

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Customer Name] | Der Name des Kunden oder Käufers, der die Bestellung aufgegeben hat. Der Kundenname ist mit dem Kundenprofil verknüpft. |
| [!UICONTROL Email] | Die E-Mail-Adresse des Kunden oder Käufers. Die E-Mail-Adresse ist mit dem Öffnen einer neuen E-Mail verknüpft. |
| [!UICONTROL Customer Group] | Der Name der Kundengruppe oder des freigegebenen Katalogs, der der Kunde zugewiesen ist. |
| [!UICONTROL Company Name] | ![Adobe Commerce B2B](../assets/b2b.svg) (Verfügbar mit Adobe Commerce B2B) Der Name des mit dem Käufer verbundenen Unternehmens und in dessen Auftrag die Bestellung aufgegeben wird. Der Firmenname ist mit dem Firmenprofil verknüpft. |

{style="table-layout:auto"}

### [!UICONTROL Address Information]

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Billing Address] | Name des Kunden oder Käufers, der die Bestellung aufgegeben hat, gefolgt von Rechnungsadresse, Telefonnummer und [Mehrwertsteuer](vat.md), falls zutreffend. Die Telefonnummer ist mit dem automatischen Anruf auf einem Mobilgerät verbunden. |
| [!UICONTROL Shipping Address] | Der Name der Person, der die Bestellung zugestellt werden soll, gefolgt von der Lieferadresse und der Telefonnummer. Die Telefonnummer ist mit dem automatischen Anruf auf einem Mobilgerät verbunden. |

{style="table-layout:auto"}

### [!UICONTROL Payment & Shipping Method]

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Payment Information] | Die Zahlungsmethode, die für die Bestellung verwendet wird, und die Bestellnummer, sofern zutreffend, gefolgt von der Währung, die für die Bestellung verwendet wurde. Wenn die Bestellung dem Unternehmen mittels [Kontozahlung](../b2b/enable-basic-features.md#configure-payment-on-account)angegeben ist, ist der Betrag, der dem Konto in Rechnung gestellt wird, angegeben. |
| [!UICONTROL Shipping & Handling Information] | Die zu verwendende Versandmethode und die anwendbare Bearbeitungsgebühr. |

{style="table-layout:auto"}

### [!UICONTROL Items to Refund]

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Product] | Produktname, SKU und Optionen (falls zutreffend). |
| [!UICONTROL Price] | Der Kaufpreis des Artikels. Bei Adobe Commerce B2B spiegelt dieser Wert ggf. jeden Rabatt wider, der auf den Artikel aus dem freigegebenen Katalog angewendet wird. |
| [!UICONTROL Qty] | Die bestellte Menge. |
| [!UICONTROL Return to Stock] | Kontrollkästchen, das angibt, ob das zurückgegebene Element auf Lager zurückgegeben werden soll. |
| [!UICONTROL Qty to Refund] | Gibt die Anzahl der vom Produkt zurückgegebenen Einheiten an. |
| [!UICONTROL Subtotal] | Die Zwischensumme ist der Kaufpreis multipliziert mit der Menge der zurückgegebenen Produkteinheiten. |
| [!UICONTROL Tax Amount] | Der Steuerbetrag, der für das zurückgegebene Element als Dezimalwert gilt. |
| [!UICONTROL Tax Percent] | Der Prozentsatz der Steuer, der auf das zurückgegebene Element in Prozent angewendet wird. |
| [!UICONTROL Discount Amount] | Alle Rabatte, die für das zurückgegebene Element gelten. |
| [!UICONTROL Row Total] | Die Zeileneintrag-Summe, einschließlich der anwendbaren Steuern, die für die zurückgegebene Produktebene fällig sind, abzüglich Rabatte. |
| _Bestellsumme_ |  |

{style="table-layout:auto"}

### [!UICONTROL Credit Memo Comments]

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Comment Text] | Ein Textfeld, in das der Kunde einen Kommentar zum Kreditmemo eingeben kann. |

{style="table-layout:auto"}

### [!UICONTROL Refund Totals]

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Refund Shipping] | Der zu erstattende Versandbetrag. |
| [!UICONTROL Adjustment Refund] | Ein Betrag, der zu dem erstatteten Gesamtbetrag als zusätzliche Erstattung hinzugerechnet wird, die nicht für einen bestimmten Teil der Bestellung gilt, z. B. Versand, Artikel oder Steuern. Der angegebene Betrag kann die Gesamtrückerstattung nicht über den gezahlten Betrag erhöhen. |
| [!UICONTROL Adjustment Fee] | Ein Betrag, der von dem erstatteten Gesamtbetrag abgezogen wird, z. B. eine Wiederaufstockungsgebühr oder ein Betrag, der mit Geschenkverpackungs- oder Geschenkoptionen in Verbindung steht. |
| [!UICONTROL Grand Total] | Gesamtbetrag der zu erstattenden Beihilfe |
| [!UICONTROL Append Comments] | Kontrollkästchen, mit denen bestimmt wird, ob Kommentare in das Kreditmemo aufgenommen werden. |
| [!UICONTROL Email Copy of Credit Memo] | Kontrollkästchen, mit dem bestimmt wird, ob eine Kopie des Guthabens per E-Mail versendet wird. |
| [!UICONTROL Refund to Store Credit] | ![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce) Kontrollkästchen, mit denen bestimmt wird, ob der Gesamtbetrag an [Store-Gutschrift](../customers/store-credit-using.md). |
| [!UICONTROL Subtotal] | ![Adobe Commerce B2B](../assets/b2b.svg) (Verfügbar bei Adobe Commerce B2B) Die Gesamtzahl aller zu erstattenden Zeileneinträge. |

{style="table-layout:auto"}

### Erstattungsschaltflächen

Die für die Bestellung verwendete Zahlungsmethode bestimmt die Erstattungsschaltflächen, die für ein Kreditmemo verfügbar sind.

| Schaltfläche | Beschreibung |
|--- |--- |
| **[!UICONTROL Refund]** | Wenn der ursprüngliche Kauf über eine Kreditkarte über ein Zahlungsportal bezahlt wurde, wird der Erstattungsbetrag vom Zahlungsverarbeiter verwaltet. Informationen zur Verwaltung von Erstattungen finden Sie in der von Ihrem Zahlungsdienstleister bereitgestellten Dokumentation. |
| **[!UICONTROL Refund Offline]** | Wenn der ursprüngliche Kauf per Scheck oder Zahlungsanweisung bezahlt wurde, wird die Rückerstattung direkt an den Kunden gezahlt, indem ein Scheck, eine Geschenkkarte oder Bargeld, wenn Sie eine Backsteine und Mörtel Storefront haben. Das Kreditmemo dient als Datensatz der Offline-Transaktion. |
| **[!UICONTROL Refund to Company Credit]** | ![Adobe Commerce B2B](../assets/b2b.svg) (Verfügbar bei Adobe Commerce B2B) Wenn der Kauf dem Firmenguthaben angerechnet wurde, wird die Rückerstattung an den [Firmenkonto](../b2b/credit-company.md). |

{style="table-layout:auto"}

## Ein Kreditdokument drucken

Zum Drucken oder Anzeigen des ausgefüllten Credit Memos muss ein PDF-Reader installiert sein. Sie können [Adobe Reader][1] kostenlos.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Credit Memos]**.

1. Verwenden Sie eine der folgenden Methoden, um das Kreditmemo zu drucken:

### Methode 1: Aktuelles Kreditverzeichnis drucken

1. Öffnen Sie im Raster das Kreditmemo.

1. Klicks **[!UICONTROL Print]**.

   ![Kreditkartenauszug drucken](./assets/credit-memo-print.png){width="600" zoomable="yes"}

### Methode 2: Drucken mehrerer Kreditkarten

1. Aktivieren Sie in der Liste das Kontrollkästchen der einzelnen Kreditkarten, die Sie drucken möchten.

1. Legen Sie die **[!UICONTROL Actions]** Kontrolle an `PDF Credit Memos` und klicken **[!UICONTROL Submit]**.

   ![Ausgewählte Kreditkarten drucken](./assets/credit-memos-print.png){width="600" zoomable="yes"}

1. Führen Sie nach Aufforderung einen der folgenden Schritte aus:

   - Klicken Sie zum Speichern des Dokuments auf **[!UICONTROL Save]** und befolgen Sie die Anweisungen, um die Datei auf Ihrem Computer zu speichern. Wenn der Download abgeschlossen ist, öffnen Sie das PDF in Adobe Reader und drucken Sie das Dokument.

   - Um das Dokument anzuzeigen, klicken Sie auf **[!UICONTROL Open]**. Das gedruckte PDF-Credit-Memo wird in Adobe Reader geöffnet. Von hier aus können Sie entweder das Credit Memo drucken oder es auf Ihrem Computer speichern.


[1]: https://www.adobe.com/acrobat/pdf-reader.html "Adobe Reader abrufen"
