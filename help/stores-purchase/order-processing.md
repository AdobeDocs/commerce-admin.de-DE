---
title: Workflow und Verarbeitung von Bestellungen
description: Erfahren Sie mehr über den Workflow für Bestellungen, den Status, der bei jedem Schritt gilt, und wie Sie Bestellungen durch diesen Prozess verschieben können.
exl-id: 5bc152c8-2adf-4faf-af84-ca65d260c22a
feature: Orders, Customer Service
source-git-commit: 82f040fa34cf96af6f1e9752f8d9f1ddeab9f84c
workflow-type: tm+mt
source-wordcount: '1822'
ht-degree: 0%

---

# Workflow und Verarbeitung von Bestellungen

Wenn ein Kunde eine Bestellung aufgibt, wird ein Kundenauftrag als temporärer Datensatz der Transaktion erstellt. Im Auftragsraster haben Kundenaufträge zunächst den Status „Ausstehend“ und können jederzeit storniert werden, bis die Zahlung verarbeitet wird. Nach Zahlungsbestätigung kann die Bestellung in Rechnung gestellt und versendet werden.

**Schritt 1: Bestellung aufgeben** - Der Checkout-Prozess beginnt, wenn der Käufer **[!UICONTROL Go to Checkout]** auf die Warenkorbseite klickt oder [Neubestellungen](reorders-allow.md) direkt von seinem Kundenkonto aus aufgibt.

**Schritt 2: Auftrag ausstehend** - Der ursprüngliche Auftragsstatus ist `Pending`. In diesem Zustand wurde die Zahlung nicht bearbeitet und die Bestellung kann noch bearbeitet oder storniert werden. Dieser Status tritt auf, wenn die Zahlungsmethode für den Autorisierungsmodus konfiguriert ist.

**Schritt 3: Zahlung empfangen** - Der Bestellstatus ändert sich in `Processing`, wenn die Zahlung empfangen oder autorisiert wird. Je nach Zahlungsmethode erhalten Sie möglicherweise eine Benachrichtigung, wenn die Transaktion autorisiert oder verarbeitet wird. Dieser Status tritt automatisch auf, wenn die Zahlungsmethode für den Erfassungsmodus oder den beabsichtigten Verkaufsmodus konfiguriert ist.

**Schritt 4: Rechnungsbestellung** - Eine Bestellung wird normalerweise nach Zahlungseingang fakturiert. Die Zahlungsmethode bestimmt, welche Rechnungsoptionen für die Bestellung benötigt werden. Nachdem die Rechnung erstellt und übermittelt wurde, wird eine Kopie an den Kunden gesendet. Wenn die Zahlungsmethode mit der `capture` oder `intent sale` Zahlungsaktion konfiguriert ist, wird automatisch eine Rechnung generiert, wenn die Zahlung autorisiert und erfasst wird.

>[!NOTE]
>
>Rechnungen werden für Bestellungen, die über `Gift Card`, `Store Credit`, `Reward Points` oder andere Offline-Zahlungsmethoden aufgegeben werden, nicht automatisch erstellt.

**Schritt 5: Einzelne Lieferung buchen** - Der Bestellstatus ändert sich in &quot;`Complete`&quot;, wenn die Lieferdetails abgeschlossen, die Lieferung gebucht und der Versand festgelegt ist. Die Versandanforderung wird mit einem gedruckten Packzettel erfüllt und das Versandetikett oder _Notify Ready for Pickup_ ausgewählt (In-Store-Liefermethode). Der Kunde erhält eine Benachrichtigung, und das Paket wird versendet. Wenn Tracking-Nummern verwendet werden, kann die Sendung über das Konto des Kunden verfolgt werden.

>[!NOTE]
>
>Details zum Bestellstatus und zu den Konfigurationsoptionen für die Zahlungsmethode finden Sie unter [Bestellstatus](order-status.md) und [Zahlungen](payments.md).

## Bestellung anzeigen

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Suchen Sie die Reihenfolge im Raster.

1. Klicken Sie in der Spalte _[!UICONTROL Action]_&#x200B;auf **[!UICONTROL View]**.

1. Bestellstatus überprüfen:

   - Eine `Pending` Bestellung kann geändert, gesperrt, storniert oder fakturiert und versendet werden.

   - Eine `Processing` Bestellung kann nicht mehr wesentlich bearbeitet oder storniert werden, aber die Rechnungs- und Lieferadresse können bearbeitet werden.

   - Eine `Completed` kann neu angeordnet werden.

Die E-Mail-Adresse des Kunden kann jederzeit im Auftrags-Workflow bearbeitet werden, indem der Kunde bearbeitet wird. Die E-Mail kann nicht bearbeitet werden, wenn die Bestellung von einem Gast aufgegeben wurde.

Das linke Bedienfeld für eine offene Bestellung bietet Zugriff auf verschiedene Arten von Informationen, die sich auf die Bestellung beziehen.

![Bestellung anzeigen](./assets/order-view.png){width="700" zoomable="yes"}

## Bearbeiten einer Bestellung

Wenn ein Kunde eine Bestellung aufgibt, wird ein Kundenauftrag als temporärer Datensatz der Transaktion erstellt. Der Kundenauftrag hat den Status `Pending` bis zum Zahlungseingang. Im Status `Pending` können Bestellungen bis zum Zahlungseingang bearbeitet oder storniert und eine Rechnung erstellt werden. Eine einfache Möglichkeit, sich das vorzustellen, besteht darin, dass Bestellungen zu Rechnungen und Rechnungen zu Lieferungen werden. Im Raster Bestellungen werden alle Bestellungen aufgelistet, unabhängig davon, wo sie sich im Workflow befinden. Informationen zur Unterstützung von Kunden bei einer Bestellung finden Sie unter [Aktualisieren einer Bestellung](order-update.md).

![Bestellungen](./assets/orders-grid.png){width="700" zoomable="yes"}

Um eine `Pending` Reihenfolge zu öffnen, klicken Sie oben rechts auf **[!UICONTROL Edit]** .

>[!NOTE]
>
>Bestellungen können nur bearbeitet werden, wenn sie sich im Status `Pending` befinden. Die Schaltfläche „Bearbeiten“ ist nicht für Bestellungen mit einem anderen Status oder für Bestellungen sichtbar, die auf einem &quot;[ Angebot“ ](../b2b/quotes.md).

![Kundenauftrag bearbeiten](./assets/order-pending.png){width="600" zoomable="yes"}

Überprüfen Sie die folgenden Abschnitte im Kundenauftrag, indem Sie die Feldbeschreibungen als Referenz verwenden.

### Beschreibungen zur Bestellansicht

| Tabulator | Beschreibung |
|--- |--- |
| [!UICONTROL Information] | Zeigen Sie detaillierte Informationen über die Bestellung und das Konto an, einschließlich der Rechnungs- und Versandadressen, Zahlungs- und Liefermethoden, Bestellartikel, Gesamtsummen und Notizen. |
| [!UICONTROL Invoices] | Listet alle Rechnungen auf, die mit der Bestellung verknüpft sind. |
| [!UICONTROL Credit Memos] | Listet alle Gutschriften auf, die mit der Bestellung verknüpft sind. |
| [!UICONTROL Shipments] | Listet alle Sendungsaufzeichnungen auf, die mit der Bestellung verknüpft sind. |
| [!UICONTROL Comments History] | Listet alle Notizen auf, die mit der Bestellung verbunden sind. |

{style="table-layout:auto"}

>[!NOTE]
>
>Ein Administrator muss über **[!UICONTROL Sales / Archive]** [Berechtigungen](../systems/permissions-user-roles.md) für den Rollenbereich verfügen, um die Registerkarten _Rechnungen_, _Gutschriften_ und _Lieferungen_ sehen.

### Schaltflächenleiste

| Schaltfläche | Beschreibung |
|--- |--- |
| **[!UICONTROL Back]** | Kehrt zur Seite Bestellungen zurück, ohne die Änderungen zu speichern. |
| **[!UICONTROL Cancel]** | Storniert den Kundenauftrag. |
| **[!UICONTROL Send Email]** | Sendet eine E-Mail über die Bestellung an den Kunden. |
| **[!UICONTROL Hold]**/**[!UICONTROL Unhold]** | Ändert den Status des Kundenauftrags in `On Hold`. Um die Sperre des Kundenauftrags aufzuheben, wählen Sie **[!UICONTROL Unhold]** aus. |
| **[!UICONTROL Invoice]** | Erstellt eine Rechnung aus dem Kundenauftrag, indem der Auftrag in eine Rechnung umgewandelt wird. |
| **[!UICONTROL Ship]** | Erstellt einen Lieferdatensatz für die Bestellung. |
| **[!UICONTROL Notify Order is Ready for Pickup]** | Erscheint nur, wenn eine Bestellung als Versand im Geschäft aufgegeben wird. Benachrichtigt den Kunden, dass die Bestellung zur Abholung bereit ist. |
| **[!UICONTROL Reorder]** | Erstellt einen Kundenauftrag basierend auf dem aktuellen Auftrag. |
| **[!UICONTROL Edit]** | Öffnet eine ausstehende Bestellung im Bearbeitungsmodus. Die Schaltfläche „Bearbeiten“ ist für Bestellungen mit dem Status &quot;`Processing`&quot; oder Bestellungen, die auf ausgehandelten Angeboten basieren, nicht sichtbar. |

{style="table-layout:auto"}

### Stornieren einer Bestellung

Sie können [stornieren](order-update.md) Bestellungen, die noch nicht fakturiert wurden. Eine [Gutschrift](credit-memos.md) muss ausgestellt werden, wenn ein Kunde eine Bestellung stornieren möchte, nachdem sie in Rechnung gestellt wurde (Zahlung wird erfasst).

Wenn eine Bestellung `Pending` oder `Processing` wird und die Zahlung nicht oder nicht vollständig erfasst wird, können Sie [ Bestellung stornieren](#void-an-order) anstatt sie zu stornieren.

Um eine stornierte Bestellung wiederherzustellen, klicken Sie auf die Schaltfläche **[!UICONTROL Reorder]** und eine neue Bestellung wird mit dem Status `Pending` erstellt.

>[!NOTE]
>
>Die Stornierung einer Bestellung führt auch zur Stornierung, aber die Stornierung einer Bestellung führt nicht zu einem Trigger der Stornierung.

### Stornierung einer Bestellung

Nur Kundenaufträge, die nicht fakturiert wurden, den Status `Processing` und die [Zahlungsintegrationseinstellung `Authorize`](../configuration-reference/sales/payment-methods.md#payment-actions) haben, können [storniert](order-update.md#void-a-processing-order). Nachdem Sie eine Bestellung storniert haben, können Sie sie stornieren.

### [!UICONTROL Order and Account Information]

![Bestell- und Kontoinformationen](./assets/order-account-information.png){width="600" zoomable="yes"}

#### Bestellinformationen

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Order Number] | Die Bestellnummer wird oben im Auftrag angezeigt, gefolgt von einem Hinweis, der angibt, ob die Bestätigungs-E-Mail gesendet wurde. |
| [!UICONTROL Order Date] | Datum und Uhrzeit der Auftragserteilung. |
| [!UICONTROL Purchased From] | Gibt die Website-, Store- und Store-Ansicht an, in der die Bestellung aufgegeben wurde. |
| [!UICONTROL Placed from IP] | Zeigt die IP-Adresse des Computers an, von dem aus die Bestellung aufgegeben wurde. |
| [!UICONTROL Order Placed from Quote] | ![Adobe Commerce B2B](../assets/b2b.svg) (verfügbar mit Adobe Commerce B2B) Gibt das [Angebot](../b2b/quotes.md) an, aus dem die Bestellung generiert wurde, falls zutreffend. Der Angebotsname ist mit dem Angebot verknüpft. |

{style="table-layout:auto"}

#### Kontoinformationen

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Customer Name] | Der Name des Kunden oder Käufers, der die Bestellung aufgegeben hat. Der Kundenname ist mit dem Kundenprofil verknüpft. |
| [!UICONTROL Email] | Die E-Mail-Adresse des Kunden oder Käufers. Die E-Mail-Adresse ist mit dem Öffnen einer neuen E-Mail-Nachricht verknüpft. |
| [!UICONTROL Customer Group] | Der Name der Kundengruppe oder des freigegebenen Katalogs, dem der Kunde zugewiesen ist. |
| [!UICONTROL Company Name] | ![Adobe Commerce B2B](../assets/b2b.svg) (verfügbar mit Adobe Commerce B2B) Der Name des Unternehmens, mit dem der Käufer verknüpft ist und für das die Bestellung aufgegeben wird. Der Firmenname ist mit dem [Firmenprofil“ ](../b2b/account-companies.md). |

{style="table-layout:auto"}

### [!UICONTROL Address Information]

![Adressinformationen](./assets/order-address-information.png){width="600" zoomable="yes"}

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Billing Address] | Der Name des Kunden oder Käufers, der die Bestellung aufgegeben hat, gefolgt von der Rechnungsadresse, der Telefonnummer und [MwSt](vat.md), falls zutreffend. Die Telefonnummer ist mit der automatischen Anwahl auf einem Mobilgerät verknüpft. |
| [!UICONTROL Shipping Address] | Der Name der Person, an die die Bestellung versendet werden soll, gefolgt von der Lieferadresse und der Telefonnummer. Die Telefonnummer ist mit der automatischen Anwahl auf einem Mobilgerät verknüpft. |

{style="table-layout:auto"}

### [!UICONTROL Payment & Shipping Method]

![Zahlungs- und Versandmethode](./assets/order-payment-and-shipping-method-braintree.png){width="600" zoomable="yes"}

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Payment Information] | Die Zahlungsmethode, die für die Bestellung verwendet werden soll, und die Bestellnummer, falls zutreffend, gefolgt von der Währung, die für die Bestellung verwendet wurde. Wird der Auftrag mit dem Firmenkredit ([) belastet](../b2b/enable-basic-features.md#configure-payment-on-account) wird der dem Konto belastete Betrag angegeben. |
| [!UICONTROL Shipping & Handling Information] | Die zu verwendende Versandmethode und etwaige Bearbeitungsgebühren. |

{style="table-layout:auto"}

### Benutzerdefinierte Bestellattribute

[!BADGE nur SaaS]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce as a Cloud Service-Projekte (von Adobe verwaltete SaaS-Infrastruktur)."}

Benutzerdefinierte Bestellattribute ermöglichen es Ihnen, zusätzliche Informationen, die auf Ihre Geschäftsanforderungen zugeschnitten sind, mit der Bestellung zu verknüpfen.

![Benutzerdefinierte Bestellattribute](./assets/custom-order-attributes.png){width="600" zoomable="yes"}

Im **[!UICONTROL Custom Order Attributes]** Abschnitt werden alle benutzerdefinierten Sortierattribute und deren aktuelle Werte angezeigt.

Um ein neues benutzerdefiniertes Sortierattribut zu erstellen, geben Sie einen **[!UICONTROL Attribute Code]** und **[!UICONTROL Value]**

Um zusätzliche benutzerdefinierte Bestellattribute zu erstellen, klicken Sie auf **[!UICONTROL Add Attribute]**.

Um ein benutzerdefiniertes Sortierattribut zu entfernen, klicken Sie auf das **[!UICONTROL X]**.

>[!NOTE]
>
>Benutzerdefinierte Bestellattribute können nur bearbeitet werden, wenn sich die Bestellung im Status `Pending` befindet. Für Bestellungen mit einem anderen Status können Sie die Attributwerte anzeigen, sie jedoch nicht ändern.

### Bestellte Elemente überprüfen

![Artikel bestellt](./assets/order-items-ordered-tee.png){width="600" zoomable="yes"}

Gehen Sie im Abschnitt **[!UICONTROL Order Total]** wie folgt vor:

1. Geben Sie eine **[!UICONTROL Comment]** ein, die in die Bestellung aufgenommen werden soll.

1. Wenn Sie den Kommentar per E-Mail an den Kunden senden möchten, aktivieren Sie das Kontrollkästchen **[!UICONTROL Notify Customer by Email]** .

1. Wenn der Kommentar im Kundenkonto sichtbar sein soll, aktivieren Sie das Kontrollkästchen **[!UICONTROL Visible on Storefront]** .

   ![Bestellsumme](./assets/order-total.png){width="600" zoomable="yes"}

1. Wenn Sie bereit sind, die Bestellung zu fakturieren, klicken Sie auf **[!UICONTROL Invoice]** und folgen Sie den Anweisungen zum [Erstellen einer Rechnung](invoices.md#create-an-invoice).

#### [!UICONTROL Items Ordered]

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Product] | Der Produktname, die SKU und ggf. Optionen. |
| [!UICONTROL Item Status] | Zeigt den Status des Elements an. Wert: `Ordered` |
| [!UICONTROL Original Price] | Der ursprüngliche Katalogpreis des Artikels vor Rabatten. |
| [!UICONTROL Price] | Der Kaufpreis des Artikels. Dieser Wert spiegelt ggf. alle Rabatte wider, die auf den Artikel aus dem freigegebenen Katalog angewendet wurden. |
| [!UICONTROL Qty] | Die bestellte Menge. |
| [!UICONTROL Subtotal] | Die Zwischensumme ist der Einkaufspreis multipliziert mit der Menge. |
| [!UICONTROL Tax Amount] | Der Steuerbetrag, der auf den Artikel als Dezimalwert angewendet wird. |
| [!UICONTROL Tax Percent] | Der Prozentsatz der auf diesen Artikel angewendeten Steuer als Prozentsatz. |
| [!UICONTROL Discount Amount] | Der für diesen Artikel geltende Rabatt. Der Rabattwert ist null, wenn der Auftrag auf einem Angebot basiert. |
| [!UICONTROL Row Total] | Der Zeilenposten insgesamt, einschließlich der auf Produktebene fälligen Steuern, abzüglich Rabatte. |

{style="table-layout:auto"}

#### [!UICONTROL Notes for this Order]

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Status] | Zeigt den Status des Kundenauftrags an. |
| [!UICONTROL Comment] | Ein Textfeld, in das Sie einen Kommentar für den Kunden eingeben können, der der Bestellung beiliegt. <br/>**[!UICONTROL Notify Customer by Email]**- Aktivieren Sie das Kontrollkästchen, wenn Sie den Kommentar als separate E-Mail an den Kunden senden möchten.<br/>**[!UICONTROL Visible on Storefront]** - Aktivieren Sie das Kontrollkästchen, wenn der Kommentar im Konto des Kunden sichtbar sein soll. <br/>**[!UICONTROL Update]**- Fügt den Kommentar hinzu und sendet eine E-Mail, falls zutreffend. |

{style="table-layout:auto"}

#### [!UICONTROL Order Totals]

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Shipping & Handling] | Der Betrag, der für Versand- und Bearbeitungsgebühren berechnet wird. |
| [!UICONTROL Tax] | Der auf den Auftrag angewendete Steuerbetrag, falls zutreffend. |
| [!UICONTROL Grand Total] | Die Bestellsumme. |
| [!UICONTROL Total Paid] | Der für die Bestellung gezahlte Gesamtbetrag, falls zutreffend. |
| [!UICONTROL Total Refunded] | Der Gesamtbetrag, der aus der Bestellung zurückerstattet wurde, falls zutreffend. |
| [!UICONTROL Total Due] | Der insgesamt fällige Betrag. |
| [!UICONTROL Store Credit] | ![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Der Betrag der verfügbaren Speichergutschrift, die auf die Bestellung angewendet wird, falls zutreffend. |
| [!UICONTROL Catalog Total Price] | ![Adobe Commerce B2B](../assets/b2b.svg) (verfügbar mit Adobe Commerce B2B) Der Gesamtpreis der Artikel im Angebot ohne Steuer, entsprechend den Preisen im freigegebenen Katalog oder Standardkatalog, der als Grundlage des Angebots verwendet wird. Wenn die Währung der Storefront von der Basiswährung abweicht, wird der Wert in beiden Währungen angezeigt, wobei die Storefront in eckigen Klammern angezeigt wird. |
| [!UICONTROL Negotiated Discount] | ![Adobe Commerce B2B](../assets/b2b.svg) (verfügbar mit Adobe Commerce B2B) Der Rabatt, der aus einem zwischen Käufer und Verkäufer ausgehandelten Angebot resultiert. Wenn die Währung der Storefront von der Basiswährung abweicht, wird der Wert in beiden Währungen angezeigt, wobei die Storefront in eckigen Klammern angezeigt wird. |
| [!UICONTROL Subtotal] | ![Adobe Commerce B2B](../assets/b2b.svg) (verfügbar mit Adobe Commerce B2B) Der Kataloggesamtpreis abzüglich des ausgehandelten Rabatts. |

{style="table-layout:auto"}

## Demo zur Bestellabwicklung

Sehen Sie sich dieses Video an, um mehr über die Auftragsverarbeitung und den Status zu erfahren:

>[!VIDEO](https://video.tv.adobe.com/v/343935/?quality=12&learn=on)
