---
title: Bestellungen
description: Erfahren Sie mehr über den Arbeitsbereich "Bestellungen"und die Suchfunktionen, mit denen Bestellungen in Admin gefunden werden können.
exl-id: 6ec8b8c7-97c4-446e-9420-e36e72e90237
feature: Orders, Admin Workspace
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1245'
ht-degree: 0%

---

# Bestellungen

Die _Bestellungen_ Das Raster listet alle aktuellen Bestellungen auf und verfolgt ihren Fortschritt. [Bestellstatus](order-status.md) durch die [Workflow](order-processing.md). Eine einfache Möglichkeit, den grundlegenden Prozess zu verstehen, besteht darin, dass eine Bestellung zu einem [Rechnung](invoices.md)und eine Rechnung wird zu einer [Verbringung](shipments.md). Das Raster stellt den ersten Schritt des Prozesses dar und ist der Ort, an dem Sie [update](order-update.md) bestehende Bestellungen und Bestellungen erstellen.

Normalerweise werden Bestellungen erstellt, wenn Kunden den Checkout-Prozess über die Storefront abschließen. Wenn ein Kunde jedoch Hilfe benötigt, können Sie auch auf seine [Warenkorb](shopping-assisted-cart-manage.md) oder [Bestellung erstellen](customer-account-create-order.md) entweder von der _Bestellungen_ oder direkt über ihr Kundenkonto.

## Arbeitsbereich &quot;Bestellungen&quot;

Im Arbeitsbereich &quot;Bestellungen&quot;werden alle aktuellen Bestellungen aufgelistet, sodass Sie bestehende Bestellungen bearbeiten und [erstellen](customer-account-create-order.md) Bestellungen. Jede Zeile im Raster stellt eine Kundenreihenfolge dar und jede Spalte stellt ein Attribut oder Datenfeld dar. Verwenden Sie den Standard [Steuerelemente](../getting-started/admin-grid-controls.md) zum Sortieren und Filtern der Liste, Suchen von Bestellungen und Anwenden [Aktionen](../getting-started/admin-actions-control.md) auf ausgewählte Bestellungen. Verwenden Sie die Registerkarten oberhalb der Seitensteuerelemente, um die Liste zu filtern, die Standardansicht zu ändern, Spalten zu ändern und neu anzuordnen und Daten zu exportieren.

![Raster &quot;Bestellungen&quot;](./assets/orders-grid.png){width="700" zoomable="yes"}

### Rasterlayout

Die Auswahl der Spalten und ihre Reihenfolge im Raster können nach Ihren Wünschen geändert werden. Das neue Layout kann als Raster gespeichert werden _Ansicht_. Standardmäßig sind nur neun von 20 verfügbaren Spalten in das Raster eingeschlossen.

![Sortieren von Rasterspalten](./assets/order-grid-columns.png){width="600" zoomable="yes"}

#### Spaltenauswahl ändern

Klicken Sie oben rechts auf die _Spalten_ ( ![Spalteneinstellungen](../assets/icon-columns.png) ) steuern und gehen Sie wie folgt vor:

- Aktivieren Sie das Kontrollkästchen einer Spalte, die Sie zum Raster hinzufügen möchten.
- Deaktivieren Sie das Kontrollkästchen aller Spalten, die Sie aus dem Raster entfernen möchten.

#### Zurücksetzen der Spaltenauswahl

1. Klicken Sie auf _Spalten_ ( ![Spalteneinstellungen](../assets/icon-columns.png) ).

1. Um die Rasterspalten zurückzusetzen, klicken Sie auf **[!UICONTROL Reset]**.

   Das Rasterlayout ändert sich so, dass nur die Anzeige erfolgt. [Standardspalten](#column-descriptions).

#### Verschieben einer Spalte

1. Klicken Sie auf die Spaltenüberschrift und halten Sie sie.

1. Ziehen Sie die Spalte an die neue Position und veröffentlichen Sie sie.

#### Speichern einer Rasteransicht

1. Klicken Sie auf **[!UICONTROL View]** ( ![Augensymbol](../assets/icon-view-eye.png) ).

1. Klicken **[!UICONTROL Save Current View]**.

1. Geben Sie einen **[!UICONTROL name]** für die Ansicht.

1. Klicken Sie zum Speichern aller Änderungen auf den Pfeil ( ![Pfeilsymbol](../assets/icon-arrow-save.png) ).

   Der Name der Ansicht wird jetzt als aktuelle Ansicht angezeigt.

#### Ansicht ändern

Klicken Sie auf **[!UICONTROL View]** ( ![Augensymbol](../assets/icon-view-eye.png) ). Führen Sie dann einen der folgenden Schritte aus:

- Um eine andere Ansicht zu verwenden, klicken Sie auf den Namen der Ansicht.

- Um den Namen einer Ansicht zu ändern, klicken Sie auf die _Bearbeiten_ ( ![Stiftsymbol](../assets/icon-edit-pencil.png) ) und aktualisieren Sie den Namen.

### Workspace-Steuerelemente

| Kontrolle | Beschreibung |
|--- |--- |
| [!UICONTROL Create New Order] | Erstellt eine Bestellung. Siehe [Erstellen einer Bestellung](customer-account-create-order.md) für weitere Informationen. |
| [!UICONTROL Go to Archive] | Zeigt die Liste der archivierten Bestellungen an. |
| [!UICONTROL Search] | Startet eine Suche nach Bestellungen anhand der aktuellen Filter. |
| [!UICONTROL Filters] | Definiert einen Satz von Suchparametern, mit denen die im Raster angezeigten Datensätze gefiltert werden. |
| [!UICONTROL Default View] | Legt das standardmäßige Spaltenlayout des Rasters fest. |
| [!UICONTROL Columns] | Bestimmt die Auswahl der Spalten und ihre Reihenfolge im Raster. Das Spaltenlayout kann geändert und als _Ansicht_. Standardmäßig sind nur einige der Spalten im Raster enthalten. |
| [!UICONTROL Export] | Exportiert die ausgewählten Datensätze als CSV- oder Excel-XML-Datei. |

{style="table-layout:auto"}

### Aktionen

Um eine Aktion auf bestimmte Bestellungen anzuwenden, aktivieren Sie das Kontrollkästchen in der ersten Spalte jeder Bestellung. Um alle Bestellungen auszuwählen oder die Auswahl aufzuheben, verwenden Sie das Steuerelement oben in der Spalte.

![Bestellaktionen](./assets/orders-action.png){width="600" zoomable="yes"}

| Kontrolle | Beschreibung |
|--- |--- |
| [!UICONTROL Actions] | Listet alle Aktionen auf, die auf ausgewählte Bestellungen angewendet werden können. Um eine Aktion auf eine Bestellung oder eine Gruppe von Bestellungen anzuwenden, aktivieren Sie das Kontrollkästchen in der ersten Spalte jeder Bestellung. <br/>Bestellaktionen: `Cancel` / `Hold` / `Unhold` / `Print Invoices` / `Print Packing Slips` / `Print Credit Memos` / `Print All` / `Print Shipping Labels` / `Move to Archive` ![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce) |
| [!UICONTROL Mass Actions] | Kann verwendet werden, um mehrere Datensätze als Ziel der Aktion auszuwählen. Aktivieren Sie das Kontrollkästchen in der ersten Spalte jedes Datensatzes, der der Aktion unterliegt. Optionen: `Select All` / `Unselect All` / `Select Visible` / `Unselect Visible` |
| [!UICONTROL Submit] | Wendet die aktuelle Aktion auf die ausgewählten Bestelldatensätze an. |
| [!UICONTROL Edit] | Öffnet die Bestellung im Bearbeitungsmodus. |

{style="table-layout:auto"}

### Spaltenbeschreibungen

| Spalte | Beschreibung |
|--- |--- |
| [!UICONTROL Select] | Aktivieren Sie die Kontrollkästchen für die Anführungszeichen, die einer Aktion unterzogen werden sollen, oder verwenden Sie das Auswahlsteuerelement in der Spaltenüberschrift. Optionen: Alle auswählen/Auswahl aufheben |
| [!UICONTROL ID] | Eine eindeutige, sequenzielle Zahl, die zugewiesen wird, wenn eine neue Bestellung zum ersten Mal gespeichert wird. |
| [!UICONTROL Purchase Point] | Gibt die Store-Ansicht an, in der die Bestellung aufgegeben wurde. |
| [!UICONTROL Purchase Date] | Datum und Uhrzeit der Platzierung der Bestellung. Sie wird immer entsprechend der Standardzeitzone angezeigt. |
| [!UICONTROL Bill-to Name] | Der Name der Person, die für die Bestellung verantwortlich ist. |
| [!UICONTROL Ship-to Name] | Der Name der Person, an die die Bestellung versandt werden soll. |
| [!UICONTROL Grand Total (Base)] | Die Gesamtsumme der Bestellung. |
| [!UICONTROL Grand Total (Purchased)] | Die Gesamtsumme der in der Bestellung gekauften Produkte. |
| [!UICONTROL Status] | Der aktuelle Bestellstatus. |
| [!UICONTROL Action] | _[!UICONTROL View]_öffnet die Bestellung im Bearbeitungsmodus. |
| [!UICONTROL Allocated sources] | Die der spezifischen Bestellung zugewiesenen Quellen. |

{style="table-layout:auto"}

Zusätzliche verfügbare Spalten:

| Spalte | Beschreibung |
|--- |--- |
| [!UICONTROL Billing Address] | Die Rechnungsadresse des Kunden, der die Bestellung aufgegeben hat. |
| [!UICONTROL Shipping Address] | Die Adresse, an die die Bestellung versandt werden soll. |
| [!UICONTROL Shipping Information] | Die Methode, die zum Versand der Bestellung verwendet werden soll. |
| [!UICONTROL Customer Email] | Die E-Mail-Adresse der Person, die den Auftrag erteilt hat. |
| [!UICONTROL Customer Group] | Die Kundengruppe, der die Person zugewiesen wird, die die Bestellung aufgegeben hat. |
| [!UICONTROL Subtotal] | Die Teilsumme der Bestellungen, ohne Versand und Bearbeitung, sowie Steuern. |
| [!UICONTROL Shipping and Handling] | Der für Versand und Bearbeitung berechnete Betrag. |
| [!UICONTROL Customer Name] | Der Vor- und Nachname des Kunden, der die Bestellung aufgegeben hat. |
| [!UICONTROL Payment Method] | Die Zahlungsmethode, die für die Bestellung verwendet wird. |
| [!UICONTROL Total Refunded] | Alle Beträge aus der Bestellung, die dem Kunden zurückerstattet werden sollen. |
| [!UICONTROL Refunded to Store Credit] | ![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce) Jeder Betrag aus der Bestellung, der an den Kundenvorrat zurückgezahlt werden soll. |
| [!UICONTROL Company Name] | ![B2B für Adobe Commerce](../assets/b2b.svg) (Verfügbar mit B2B für Adobe Commerce) Der Name der [Firma](../b2b/account-companies.md) der die Bestellung aufgegeben hat. |

{style="table-layout:auto"}

## Bestellsuche

Das Suchfeld oben links im Raster Bestellungen kann verwendet werden, um bestimmte Bestellungen nach Keyword zu finden oder um die Bestelldatensätze im Raster zu filtern.

![Suchergebnisse](./assets/order-search.png){width="600" zoomable="yes"}

### Suche nach einer Übereinstimmung

1. Geben Sie einen Suchbegriff in das Seitensuchfeld ein.

1. Um die Ergebnisse anzuzeigen, klicken Sie auf _Suche_ ( ![Lupensymbol](../assets/icon-magnify-search.png) ).

### Filtern der Suche

1. Um die Auswahl der Suchfilter anzuzeigen, klicken Sie auf die _Filter_ ( ![Trichtersymbol](../assets/icon-filter-search.png) ).

   ![Bestellfilter](./assets/order-search-filter.png){width="600" zoomable="yes"}

1. Geben Sie so viele Filter an, wie Sie die gewünschten Bestellungen beschreiben möchten.

1. Klicks **[!UICONTROL Apply Filters]** , um die Ergebnisse anzuzeigen.

### Suchfilter

| Filter | Beschreibung |
|--- |--- |
| [!UICONTROL Purchase Date] | Filtert die Suche nach dem gekauften Datum. Um Bestellungen innerhalb eines Datumsbereichs zu finden, geben Sie beide **[!UICONTROL from]** und **[!UICONTROL to]** Daten. |
| [!UICONTROL ID] | Filtert die Suche anhand der Bestell-ID. |
| [!UICONTROL Grand Total (Base)] | Filtert die Suche anhand der Gesamtsumme jeder Bestellung, einschließlich etwaiger Gutschriften, die auf die Bestellung angewendet werden. |
| [!UICONTROL Grand Total (Purchased)] | Filtert die Suche nach der Gesamtsumme der bei jeder Bestellung gekauften Artikel. |
| [!UICONTROL Bill-to Name] | Filtert die Suche nach dem Namen der Person, die für die Bestellung verantwortlich ist. |
| [!UICONTROL Ship-to Name] | Filtert die Suche nach dem Namen der Person, an die jede Bestellung versandt wird . |
| [!UICONTROL Purchase Point] | Filtert die Suche nach Website-, Store- oder Store-Ansicht, in der die Bestellung aufgegeben wurde. |
| [!UICONTROL Status] | Filtert die Suche nach dem Bestellstatus. Optionen: `Canceled` / `Closed` / `Complete` / `Suspected Fraud` / `On Hold` / `Payment Review` / `PayPal Canceled Reversal` /` PayPal Reversed` /` Pending` / `Pending Payment` / `Pending PayPal` / `Processing` |
| [!UICONTROL Braintree Transaction Source] | Filtert die Suche anhand der Transaktionsquelle. |

{style="table-layout:auto"}

### Suchwerkzeuge

| Tool | Beschreibung |
|--- |--- |
| [!UICONTROL Apply Filters] | Wendet alle Filter auf die Suchergebnisse an. |
| [!UICONTROL Cancel] | Bricht die aktuelle Suche ab. |
| [!UICONTROL Clear All] | Löscht alle Suchfilter. |

{style="table-layout:auto"}

## Fehlerbehebung bei Ressourcen

Hilfe zur Fehlerbehebung bei Bestellproblemen finden Sie in den folgenden Knowledge Base-Artikeln des Commerce-Supports:

- [Anzeigefehler der Bestellungen](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/storefront/magento-2.4.0-known-issue-orders-display-error.html)
- [Fehler &quot;PayPal doppelte Bestellungen 10415&quot;](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-6/mdva-31006-magento-patch-paypal-duplicate-orders-10415-error.html)
- [Neue Bestellungen werden archiviert](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/new-orders-are-sent-to-archive.html)
- [Bestellungen werden nicht im Raster Bestellungen in der Admin-Konsole angezeigt](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/orders-not-displayed-in-the-orders-grid-in-the-admin.html)
- [Bestellstatus - inkorrekte Sendung über REST API erstellt](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-7/mdva-30972-magento-patch-order-status-incorrect-shipment-created-via-rest-api.html)
