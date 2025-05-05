---
title: Bestellungen
description: Erfahren Sie mehr über den Arbeitsbereich „Bestellungen“ und die Suchfunktionen, mit denen Sie in Admin Bestellungen finden.
exl-id: 6ec8b8c7-97c4-446e-9420-e36e72e90237
feature: Orders, Admin Workspace
source-git-commit: f8254db7d69e58c8e9a78948ee6e40f5ea88cea0
workflow-type: tm+mt
source-wordcount: '1180'
ht-degree: 0%

---

# Bestellungen

Das Raster _Bestellungen_ listet alle aktuellen Bestellungen auf und verfolgt deren Fortschritt und [Bestellstatus](order-status.md) über den [Workflow](order-processing.md). Ein einfacher Weg, den grundlegenden Prozess zu verstehen, besteht darin, dass aus einer Bestellung eine [Rechnung](invoices.md) und aus einer Rechnung eine [Lieferung](shipments.md) wird. Das Raster stellt den ersten Schritt des Prozesses dar und ist der Ort, an dem Sie [aktualisieren](order-update.md) und Bestellungen erstellen können.

In der Regel werden Bestellungen erstellt, wenn Kunden den Checkout-Prozess in der Storefront abschließen. Wenn ein Kunde jedoch Hilfe benötigt, können Sie auch auf seinen [Warenkorb](shopping-assisted-cart-manage.md) oder [Bestellung erstellen](customer-account-create-order.md) entweder über das _Bestellungen_ oder direkt über sein Kundenkonto zugreifen.

## Arbeitsbereich Bestellungen

Im Arbeitsbereich Bestellungen werden alle aktuellen Bestellungen aufgelistet. Sie haben die Möglichkeit, vorhandene Bestellungen zu bearbeiten und [Bestellungen zu ](customer-account-create-order.md). Jede Zeile im Raster steht für eine Kundenreihenfolge, und jede Spalte steht für ein Attribut oder ein Datenfeld. Verwenden Sie die standardmäßigen [Steuerelemente](../getting-started/admin-grid-controls.md), um die Liste zu sortieren und zu filtern, Bestellungen zu finden und [Aktionen](../getting-started/admin-actions-control.md) auf ausgewählte Bestellungen anzuwenden. Verwenden Sie die Registerkarten oberhalb der Steuerelemente für die Paginierung, um die Liste zu filtern, die Standardansicht zu ändern, Spalten zu ändern und neu anzuordnen und Daten zu exportieren.

![Auftragsraster](./assets/orders-grid.png){width="700" zoomable="yes"}

### Rasterlayout

Die Auswahl der Spalten und ihre Reihenfolge im Raster können nach Ihren Wünschen geändert werden. Das neue Layout kann als Raster (_) gespeichert_. Standardmäßig sind nur neun von 20 verfügbaren Spalten im Raster enthalten.

![Sortieren von Rasterspalten](./assets/order-grid-columns.png){width="600" zoomable="yes"}

#### Spaltenauswahl ändern

Klicken Sie oben rechts auf das Steuerelement _Spalten_ ( ![Spalteneinstellungen](../assets/icon-columns.png) ) und führen Sie folgende Schritte aus:

- Aktivieren Sie das Kontrollkästchen einer beliebigen Spalte, die Sie dem Raster hinzufügen möchten.
- Deaktivieren Sie das Kontrollkästchen für alle Spalten, die Sie aus dem Raster entfernen möchten.

#### Spaltenauswahl zurücksetzen

1. Klicken Sie auf das Steuerelement _Spalten_ ( ![Spalteneinstellungen](../assets/icon-columns.png) ).

1. Um die Rasterspalten zurückzusetzen, klicken Sie auf **[!UICONTROL Reset]**.

   Das Rasterlayout ändert sich, sodass nur [ (Standardspalten) ](#column-descriptions).

#### Spalte verschieben

1. Klicken Sie auf die Spaltenüberschrift, und halten Sie sie gedrückt.

1. Ziehen Sie die Spalte an die neue Position und lassen Sie sie los.

#### Speichern einer Rasteransicht

1. Klicken Sie auf das Steuerelement **[!UICONTROL View]** ( ![Augensymbol](../assets/icon-view-eye.png) ).

1. Klicken Sie auf **[!UICONTROL Save Current View]**.

1. Geben Sie einen **[!UICONTROL name]** für die Ansicht ein.

1. Um alle Änderungen zu speichern, klicken Sie auf den Pfeil ( ![Pfeilsymbol](../assets/icon-arrow-save.png) ).

   Der Name der Ansicht wird jetzt als aktuelle Ansicht angezeigt.

#### Ändern der Ansicht

Klicken Sie auf das Steuerelement **[!UICONTROL View]** ( ![Augensymbol](../assets/icon-view-eye.png) ). Führen Sie dann einen der folgenden Schritte aus:

- Um eine andere Ansicht zu verwenden, klicken Sie auf den Namen der Ansicht.

- Um den Namen einer Ansicht zu ändern, klicken Sie auf das Symbol _Bearbeiten_ ( ![Bleistiftsymbol](../assets/icon-edit-pencil.png) ) und aktualisieren Sie den Namen.

### Workspace-Steuerelemente

| Kontrolle | Beschreibung |
|--- |--- |
| [!UICONTROL Create New Order] | Erstellt einen Auftrag. Weitere Informationen [ Sie unter ](customer-account-create-order.md) erstellen. |
| [!UICONTROL Go to Archive] | Zeigt die Liste der archivierten Bestellungen an. |
| [!UICONTROL Search] | Startet eine Suche nach Bestellungen anhand der aktuellen Filter. |
| [!UICONTROL Filters] | Definiert einen Satz von Suchparametern, mit denen die im Raster angezeigten Datensätze gefiltert werden. |
| [!UICONTROL Default View] | Bestimmt das standardmäßige Spalten-Layout des Rasters. |
| [!UICONTROL Columns] | Bestimmt die Auswahl der Spalten und ihre Reihenfolge im Raster. Das Spalten-Layout kann geändert und als (_) gespeichert_. Standardmäßig sind nur einige der Spalten im Raster enthalten. |
| [!UICONTROL Export] | Exportiert die ausgewählten Datensätze als CSV- oder Excel-XML-Datei. |

{style="table-layout:auto"}

### Aktionen

Um eine Aktion auf bestimmte Bestellungen anzuwenden, aktivieren Sie das Kontrollkästchen in der ersten Spalte jeder Bestellung. Um alle Bestellungen auszuwählen oder deren Auswahl aufzuheben, verwenden Sie das Steuerelement oben in der Spalte.

![Bestellungsaktionen](./assets/orders-action.png){width="600" zoomable="yes"}

| Kontrolle | Beschreibung |
|--- |--- |
| [!UICONTROL Actions] | Listet alle Aktionen auf, die auf ausgewählte Bestellungen angewendet werden können. Um eine Aktion auf eine Bestellung oder eine Gruppe von Bestellungen anzuwenden, aktivieren Sie das Kontrollkästchen in der ersten Spalte jeder Bestellung. <br/>Bestellaktionen: `Cancel` / `Hold` / `Unhold` / `Print Invoices` / `Print Packing Slips` / `Print Credit Memos` / `Print All` / `Print Shipping Labels` / `Move to Archive` ![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) |
| [!UICONTROL Mass Actions] | Kann verwendet werden, um mehrere Datensätze als Ziel einer Aktion auszuwählen. Aktivieren Sie das Kontrollkästchen in der ersten Spalte jedes Datensatzes, der der Aktion unterliegt. Optionen: `Select All` / `Unselect All` / `Select Visible` / `Unselect Visible` |
| [!UICONTROL Submit] | Wendet die aktuelle Aktion auf die ausgewählten Bestellungsdatensätze an. |
| [!UICONTROL Edit] | Öffnet die Bestellung im Bearbeitungsmodus. |

{style="table-layout:auto"}

### Spaltenbeschreibungen

| Spalte | Beschreibung |
|--- |--- |
| [!UICONTROL Select] | Aktivieren Sie die Kontrollkästchen der Anführungszeichen, die einer Aktion unterzogen werden sollen, oder verwenden Sie die Auswahlsteuerung in der Spaltenüberschrift. Optionen: Alle auswählen / Auswahl aufheben |
| [!UICONTROL ID] | Eine eindeutige, sequenzielle Nummer, die zugewiesen wird, wenn eine neue Bestellung zum ersten Mal gespeichert wird. |
| [!UICONTROL Purchase Point] | Gibt die Store-Ansicht an, in der die Bestellung aufgegeben wurde. |
| [!UICONTROL Purchase Date] | Datum und Uhrzeit der Auftragserteilung. Sie wird immer in der Standardzeitzone angezeigt. |
| [!UICONTROL Bill-to Name] | Der Name der für die Bestellung verantwortlichen Person. |
| [!UICONTROL Ship-to Name] | Der Name der Person, an die die Bestellung versendet werden soll. |
| [!UICONTROL Grand Total (Base)] | Die Gesamtsumme der Bestellung. |
| [!UICONTROL Grand Total (Purchased)] | Die Gesamtsumme der in der Bestellung gekauften Produkte. |
| [!UICONTROL Status] | Der aktuelle Bestellstatus. |
| [!UICONTROL Action] | _[!UICONTROL View]_&#x200B;öffnet die Bestellung im Bearbeitungsmodus. |
| [!UICONTROL Allocated sources] | Die Quellen, die dieser bestimmten Bestellung zugeordnet sind. |

{style="table-layout:auto"}

Zusätzliche Spalten verfügbar:

| Spalte | Beschreibung |
|--- |--- |
| [!UICONTROL Billing Address] | Die Rechnungsadresse des Kunden, der die Bestellung aufgegeben hat. |
| [!UICONTROL Shipping Address] | Die Adresse, an die die Bestellung versendet werden soll. |
| [!UICONTROL Shipping Information] | Die Methode, die zum Versand der Bestellung verwendet werden soll. |
| [!UICONTROL Customer Email] | Die E-Mail-Adresse der Person, die die Bestellung aufgegeben hat. |
| [!UICONTROL Customer Group] | Die Kundengruppe, der die Person zugewiesen ist, die die Bestellung aufgegeben hat. |
| [!UICONTROL Subtotal] | Die Zwischensumme der Bestellung, ohne Versand und Bearbeitung, und Steuer. |
| [!UICONTROL Shipping and Handling] | Der für Versand und Bearbeitung berechnete Betrag. |
| [!UICONTROL Customer Name] | Der Vor- und Nachname des Kunden, der die Bestellung aufgegeben hat. |
| [!UICONTROL Payment Method] | Die Zahlungsmethode, die für die Bestellung verwendet werden soll. |
| [!UICONTROL Total Refunded] | Ein beliebiger Betrag aus der Bestellung, der dem Kunden zurückerstattet werden muss. |
| [!UICONTROL Refunded to Store Credit] | ![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Alle Beträge aus der Bestellung, die dem Store-Guthaben des Kunden zurückerstattet werden müssen. |
| [!UICONTROL Company Name] | ![Adobe Commerce B2B](../assets/b2b.svg) (verfügbar mit Adobe Commerce B2B) Der Name des [Unternehmens](../b2b/account-companies.md) das die Bestellung aufgegeben hat. |

{style="table-layout:auto"}

## Suche nach Bestellungen

Das Suchfeld oben links im Raster Bestellungen kann verwendet werden, um bestimmte Bestellungen nach Keyword oder durch Filtern der Bestellungsdatensätze im Raster zu finden.

![Suchergebnisse](./assets/order-search.png){width="600" zoomable="yes"}

### Nach einer Übereinstimmung suchen

1. Geben Sie einen Suchbegriff in das Seitensuchfeld ein.

1. Um die Ergebnisse anzuzeigen, klicken Sie auf _Suchen_ ( ![Lupensymbol](../assets/icon-magnify-search.png) ).

### Filtern der Suche

1. Um die Auswahl der Suchfilter anzuzeigen, klicken Sie auf die Registerkarte _Filter_ ( ![Trichtersymbol](../assets/icon-filter-search.png) ).

   ![Filter sortieren](./assets/order-search-filter.png){width="600" zoomable="yes"}

1. Schließen Sie so viele Filter ab, wie Sie die Bestellungen beschreiben möchten, die Sie finden möchten.

1. Klicken Sie auf **[!UICONTROL Apply Filters]** , um die Ergebnisse anzuzeigen.

### Suchfilter

| Filter | Beschreibung |
|--- |--- |
| [!UICONTROL Purchase Date] | Filtert die Suche nach dem Kaufdatum. Um Bestellungen innerhalb eines Datumsbereichs zu finden, geben Sie sowohl das **[!UICONTROL from]**- als auch das **[!UICONTROL to]** ein. |
| [!UICONTROL ID] | Filtert die Suche nach der Bestell-ID. |
| [!UICONTROL Grand Total (Base)] | Filtert die Suche nach dem Gesamtwert jeder Bestellung, einschließlich aller auf die Bestellung angewendeten Guthaben. |
| [!UICONTROL Grand Total (Purchased)] | Filtert die Suche nach der Gesamtsumme der in jeder Bestellung gekauften Artikel. |
| [!UICONTROL Bill-to Name] | Filtert die Suche nach dem Namen der Person, die für die Bezahlung der Bestellung verantwortlich ist. |
| [!UICONTROL Ship-to Name] | Filtert die Suche nach dem Namen der Person, an die jede Bestellung gesendet wird . |
| [!UICONTROL Purchase Point] | Filtert die Suche nach Website, Store oder Store-Ansicht, in der die Bestellung aufgegeben wurde. |
| [!UICONTROL Status] | Filtert die Suche nach dem Bestellstatus. Optionen: `Canceled` / `Closed` / `Complete` / `Suspected Fraud` / `On Hold` / `Payment Review` / `PayPal Canceled Reversal` /` PayPal Reversed` /` Pending` / `Pending Payment` / `Pending PayPal` / `Processing` |
| [!UICONTROL Braintree Transaction Source] | Filtert die Suche nach der Transaktionsquelle. |

{style="table-layout:auto"}

### Suchwerkzeuge

| Tool | Beschreibung |
|--- |--- |
| [!UICONTROL Apply Filters] | Wendet alle Filter auf die Suchergebnisse an. |
| [!UICONTROL Cancel] | Bricht die aktuelle Suche ab. |
| [!UICONTROL Clear All] | Löscht alle Suchfilter. |

{style="table-layout:auto"}

## Fehlerbehebung bei Ressourcen

Hilfe bei der Fehlerbehebung bei Bestellproblemen finden Sie in den folgenden Artikeln der Commerce Support Knowledge Base:

- [Fehler bei der Anzeige von Bestellungen](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/storefront/magento-2.4.0-known-issue-orders-display-error.html?lang=de)
- [Bestellungen werden nicht im Raster Bestellungen im Admin-Bereich angezeigt](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/orders-not-displayed-in-the-orders-grid-in-the-admin.html)
