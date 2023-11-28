---
title: Sendungen
description: Erfahren Sie, wie Sie Lieferaufzeichnungen für Rechnungen erstellen und Sendungen stornieren können.
exl-id: 6df83549-ba38-43f7-aab1-dbf3f6b89d74
feature: Shipping/Delivery, Invoices
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '943'
ht-degree: 1%

---

# Sendungen

Die _[!UICONTROL Shipments]_grid listet den Versanddatensatz aller Rechnungen auf, die für den Versand vorbereitet wurden. Ein Versanddatensatz kann erstellt werden, wenn eine Bestellung [fakturiert](invoices.md) oder höher.

Adobe Commerce und Magento Open Source unterstützen einen teilweisen und vollständigen Auftragsantrag mit zusätzlichen Optionen von [Inventory management](../inventory-management/introduction.md) und Drittanbietererweiterungen.

![Versand-Raster](./assets/shipments.png){width="600" zoomable="yes"}

## Spaltenbeschreibungen

| Spalte oder Kontrolle | Beschreibung |
|--- |--- |
| [!UICONTROL Select] | Aktivieren Sie das Kontrollkästchen für jedes Anführungszeichen, das einer Aktion unterzogen werden soll, oder verwenden Sie das Auswahlsteuerelement in der Spaltenüberschrift. Optionen: `Select All` / `Deselect All` |
| [!UICONTROL Shipment] | Eine eindeutige, sequenzielle Nummer, die zugewiesen wird, wenn eine neue Sendung zum ersten Mal gespeichert wird |
| [!UICONTROL Ship Date] | Versanddatum |
| [!UICONTROL Order] | Eindeutige Nummer der Bestellung |
| [!UICONTROL Order Date] | Datum und Uhrzeit der Bestellung |
| [!UICONTROL Ship-to Name] | Name der Person, an die die Bestellung versandt wird |
| [!UICONTROL Total Quantity] | Gesamtzahl der zu verschiffenden Güter |
| [!UICONTROL Action] | Ansicht öffnet die Sendung im Bearbeitungsmodus |

{style="table-layout:auto"}

Zusätzliche Spalten:

| Spalte | Beschreibung |
|--- |--- |
| [!UICONTROL Order Status] | Gibt den Bestellstatus an |
| [!UICONTROL Purchased From] | Gibt die Website-, Store- und Store-Ansicht an, in der die Bestellung aufgegeben wurde |
| [!UICONTROL Customer Name] | Name des Kunden oder Käufers, der die Bestellung aufgegeben hat |
| [!UICONTROL Email] | Die E-Mail-Adresse eines registrierten Kunden |
| [!UICONTROL Customer Group] | Der Name der Kundengruppe oder des freigegebenen Katalogs, der der Kunde zugewiesen ist |
| [!UICONTROL Billing Address] | Name des Kunden oder Käufers, der die Bestellung aufgegeben hat |
| [!UICONTROL Shipping Address] | Name der Person, an die die Bestellung versandt wird |
| [!UICONTROL Payment Method] | Die Zahlungsmethode für die Bestellung |
| [!UICONTROL Shipping Information] | Die zum Versand der Bestellung zu verwendende Methode |

{style="table-layout:auto"}

## Erstellen einer Sendung

Die folgenden Anweisungen führen Sie durch den Prozess zur Erstellung einer Sendung in Adobe Commerce oder Magento Open Source. Wenn Sie Inventory management aktiviert haben, sollten Sie [Erstellen von Sendungen mit mehreren Quellen](../inventory-management/shipments-create.md) und wählen Sie eine Quelle (oder einen Ort) und eine Menge aus, die pro Zeileneintrag gesendet werden sollen.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Suchen Sie die Reihenfolge im Raster und öffnen Sie sie.

1. Wenn die Bestellung bezahlt, in Rechnung gestellt und versandbereit ist, klicken Sie auf **[!UICONTROL Ship]**.

   Die Abschnitte am oberen Rand des Versands enthalten Name, Anschrift und Zahlungsinformationen aus dem Verkaufsauftrag.

1. Füllen Sie jeden Abschnitt des Versandformulars mit den Anweisungen in den folgenden Abschnitten aus.

### [!UICONTROL Items to Ship]

Für jedes Zeilenelement in der Reihenfolge ändern Sie die **[!UICONTROL Qty to Ship]** nach Bedarf.

### [!UICONTROL Shipping Information]

**Methode 1:** Verwenden der Bestellseite

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Im **[!UICONTROL Action]** Spalte für die ausgewählte Reihenfolge, klicken Sie auf **[!UICONTROL View]**.

1. Klicken **[!UICONTROL Ship]**.

1. Scrollen Sie nach unten zum _[!UICONTROL Payment & Shipping Method]_Block und klicken Sie auf **[!UICONTROL Add Tracking Number]**.

1. Satz **[!UICONTROL Carrier]**:

   - `Custom Value`
   - `DHL`
   - `Federal Express`
   - `United Parcel Service`
   - `United States Postal Service`

1. Um die Sendung zu verfolgen, geben Sie die **[!UICONTROL Title]** und **[!UICONTROL Number]** .

**Methode 2:** Verwenden der Versandseite

Diese Methode ist nur zulässig, wenn die Auftragslieferung bereits von der Bestellseite aus erstellt wurde.
Sie können die Versand- und Tracking-Informationen nach Bedarf über die Seite für den direkten Versand ändern:

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. Suchen und öffnen Sie die Sendung im Bearbeitungsmodus.

1. Scrollen Sie nach unten zum _[!UICONTROL Payment & Shipping Method]_blockieren.

1. Wählen Sie die **[!UICONTROL Carrier]**.

1. Geben Sie einen **[!UICONTROL Title]** für das Paket.

1. Tracking eingeben **[!UICONTROL Number]**.

1. Klicken **[!UICONTROL Add]**.

1. Um eine E-Mail mit Tracking-Informationen an den Kunden zu senden, klicken Sie auf **[!UICONTROL Send Tracking Information]** und bestätigen Sie die Aktion.

   Um den Speicherort einer Sendung zu verfolgen, öffnen Sie die gewünschte Sendung im Bearbeitungsmodus und klicken Sie auf **[!UICONTROL Track this shipment]**.

   ![Versand- und Tracking-Informationen](./assets/tracking-information.png){width="600" zoomable="yes"}

### Schaltflächen

| Schaltfläche | Beschreibung |
|--- |--- |
| **[!UICONTROL Back]** | Schließt das Formular für den neuen Versand und kehrt zur Bestellung zurück |
| **[!UICONTROL Submit Shipment]** | Fügt die Sendung für die Bestellung hinzu. |
| **[!UICONTROL Reset]** | Setzt alle Felder auf die ursprünglichen Werte zurück. |

{style="table-layout:auto"}

### Versandkommentare

1. Eingabe **Kommentare** für die Verbringung, falls erforderlich.

1. Wenn die Sendung fertig ist, klicken Sie auf **Sendung übermitteln**.

## Anmerkungen für Sendungen einrichten

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. under _[!UICONTROL Sales]_auswählen **[!UICONTROL Sales Email]**.

1. Erweitern Sie die **Versandreaktionen** und ändern Sie die Einstellungen nach Bedarf:

   ![Konfiguration von Versandkommentaren](../configuration-reference/sales/assets/sales-emails-shipment-comments.png){width="600" zoomable="yes"}

   - Die **[!UICONTROL Enabled]** ist auf `Yes` Standardmäßig bedeutet dies, dass die E-Mail an einen Kunden gesendet wird, wenn ein Versandkommentar eingegeben wird.

   - Für **[!UICONTROL Shipment Comment Email Sender]**, wählen Sie die Person aus, von der die E-Mail mit dem Versandkommentar versandt wird. Standardmäßig sind fünf E-Mail-Adressen verfügbar.

   - Für **[!UICONTROL Shipment Comment Email Template]**, wählen Sie die Vorlage basierend auf Ihrer Anforderung oder die Standardoption aus.

   - Für **[!UICONTROL Shipment Comment Email Template for Guests]** wählen Sie die Vorlage aus, die für Kunden verwendet wird, die kein Konto in Ihrem Geschäft haben.

   - Für **[!UICONTROL Shipment Comment Email Copy To]** Geben Sie die E-Mail-Adressen ein, um eine E-Mail-Kopie des Versandkommentars zu versenden. Trennen Sie mehrere E-Mail-Adressen durch Kommas.

   - Für **[!UICONTROL Shipment Comment Email Copy Method]** auswählen `bcc` (Blindkohlekopie) oder `separate email copy` -Methode basierend auf Ihrer Präferenz.

1. Klicken **[!UICONTROL Save Config]**.

## Abbrechen einer Sendung

Bevor eine Sendung an einen Beförderer versandt wird, kann sie durch Öffnen der Bestellung und Navigieren zur Sendung storniert werden, sofern der Beförderer Stornierungen unterstützt. Einige Fluggesellschaften beschränken oder beschränken Stornierungen nach einer Buchung. Beispielsweise erlaubt UPS Absagen, aber Sie müssen 24 Stunden warten, nachdem die Sendung gebucht wurde. Bei Annullierung einer Sendung kann die Stornierung nicht rückgängig gemacht werden. Der einzige Rückgriff besteht darin, die Bestellung neu zu erstellen.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Suchen Sie die Reihenfolge im Raster.

1. Im _Aktion_ Spalte, wählen **[!UICONTROL View]**.

1. Wählen Sie im linken Bereich die Option **[!UICONTROL Shipments]**.

   Kann die Sendung storniert werden, _[!UICONTROL Cancel Shipment]_wird als Option in der oberen Schaltflächenleiste angezeigt.

1. Klicken **[!UICONTROL Cancel Shipment]**.

1. Klicken Sie bei Aufforderung zur Bestätigung auf **[!UICONTROL OK]**.

Der Status der Verbringung ändert sich in `Canceled`. Wenn der Beförderer Stornierungen nicht unterstützt, erscheint eine Fehlermeldung, in der erklärt wird, warum die Sendung nicht storniert werden konnte.

## Beschreibung der Versandfelder

### [!UICONTROL Shipping Information]

| Feld | Beschreibung |
|-----|-----------|
| [!UICONTROL Carrier] | Der Name des ausgewählten Trägers |
| [!UICONTROL Title] | Ein beschreibender Name, der dem Paket vom Träger zugewiesen wird. |
| [!UICONTROL Number] | Die verknüpfte Trackingnummer, die dem Paket zugewiesen ist. |
| [!UICONTROL Action] | ![Papierkorbsymbol](../assets/icon-delete-trashcan-solid.png) - Löscht die Paketinformationen aus dem Versanddatensatz. |
| [!UICONTROL Add] | Fügen Sie der Sendung ein weiteres Paket hinzu. |

{style="table-layout:auto"}

### [!UICONTROL Route Information]

| Feld | Beschreibung |
|-----|-----------|
| [!UICONTROL Origin Location] | Zeigt eine Liste der verfügbaren Orte an. |
| [!UICONTROL International] | Ist diese Option aktiviert, wird die Verbringung als internationale Verbringung gekennzeichnet. |

{style="table-layout:auto"}

### [!UICONTROL Items Ordered]

| Feld | Beschreibung |
|-----|-----------|
| [!UICONTROL Description] | Die Beschreibung des Elements. |
| [!UICONTROL SKU] | Die Bestandseinheit des Artikels. |
| [!UICONTROL Weight] | Die Gewichtung des Artikels. |
| [!UICONTROL Qty Ordered] | Die Menge des bestellten Artikels. |
| [!UICONTROL Qty Shipped] | Die Anzahl der versandten Artikel. |
| [!UICONTROL Qty Packed] | Die Anzahl der in diesem Paket enthaltenen Elemente. |

{style="table-layout:auto"}

### [!UICONTROL Shipment Comments]

| Feld | Beschreibung |
|-----|-----------|
| [!UICONTROL Comments] | Kommentare zur Sendung sind für den internen Gebrauch bestimmt. |

{style="table-layout:auto"}

### [!UICONTROL Documentation]

| Feld | Beschreibung |
|-----|-----------|
| [!UICONTROL Package Label] | **PNG** - Laden Sie das Versandverpackungsetikett herunter. Größe: A6 (105 x 148 mm; 4,1 x 5,6 Zoll) |

{style="table-layout:auto"}
