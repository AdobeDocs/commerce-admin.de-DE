---
title: Sendungen
description: Erfahren Sie, wie Sie Lieferaufzeichnungen für Rechnungen erstellen und Sendungen stornieren können.
exl-id: 6df83549-ba38-43f7-aab1-dbf3f6b89d74
feature: Shipping/Delivery, Invoices
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '948'
ht-degree: 0%

---

# Sendungen

Das Raster _[!UICONTROL Shipments]_listet den Versanddatensatz aller für den Versand vorbereiteten Rechnungen auf. Ein Versanddatensatz kann generiert werden, wenn eine Bestellung [in Rechnung gestellt](invoices.md) oder höher ist.

Adobe Commerce und Magento Open Source unterstützen den teilweisen und vollständigen Versand von Bestellungen, mit zusätzlichen Optionen, die über [Inventory management](../inventory-management/introduction.md) und Erweiterungen von Drittanbietern verfügbar sind.

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

Die folgenden Anweisungen führen Sie durch den Prozess zur Erstellung einer Sendung in Adobe Commerce oder Magento Open Source. Wenn Sie Inventory management aktiviert haben, sollten Sie den Abschnitt [Erstellen von Multi-Source-Sendungen](../inventory-management/shipments-create.md) lesen und eine Quelle (oder einen Ort) und eine Menge auswählen, die pro Zeileneintrag gesendet werden sollen.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Suchen Sie die Reihenfolge im Raster und öffnen Sie sie.

1. Wenn die Bestellung bezahlt, in Rechnung gestellt und versandbereit ist, klicken Sie auf **[!UICONTROL Ship]**.

   Die Abschnitte am oberen Rand des Versands enthalten Name, Anschrift und Zahlungsinformationen aus dem Verkaufsauftrag.

1. Füllen Sie jeden Abschnitt des Versandformulars mit den Anweisungen in den folgenden Abschnitten aus.

### [!UICONTROL Items to Ship]

Ändern Sie für jedes Zeilenelement in der Reihenfolge die **[!UICONTROL Qty to Ship]** nach Bedarf.

### [!UICONTROL Shipping Information]

**Methode 1:** Verwenden der Bestellseite

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Klicken Sie in der Spalte **[!UICONTROL Action]** für die ausgewählte Reihenfolge auf **[!UICONTROL View]**.

1. Klicken Sie auf **[!UICONTROL Ship]**.

1. Scrollen Sie nach unten zum Block _[!UICONTROL Payment & Shipping Method]_und klicken Sie auf **[!UICONTROL Add Tracking Number]**.

1. Legen Sie **[!UICONTROL Carrier]** fest:

   - `Custom Value`
   - `DHL`
   - `Federal Express`
   - `United Parcel Service`
   - `United States Postal Service`

1. Um die Sendung zu verfolgen, geben Sie die Werte **[!UICONTROL Title]** und **[!UICONTROL Number]** ein.

**Methode 2:** Verwenden der Versandseite

Diese Methode ist nur zulässig, wenn die Auftragslieferung bereits von der Bestellseite aus erstellt wurde.
Sie können die Versand- und Tracking-Informationen nach Bedarf über die Seite für den direkten Versand ändern:

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. Suchen und öffnen Sie die Sendung im Bearbeitungsmodus.

1. Scrollen Sie nach unten zum Block _[!UICONTROL Payment & Shipping Method]_.

1. Wählen Sie den Wert **[!UICONTROL Carrier]** aus.

1. Geben Sie eine **[!UICONTROL Title]** für das Paket ein.

1. Geben Sie das Tracking **[!UICONTROL Number]** ein.

1. Klicken Sie auf **[!UICONTROL Add]**.

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

1. Geben Sie bei Bedarf **Kommentare** für die Sendung ein.

1. Wenn die Sendung fertig ist, klicken Sie auf **Sendung übermitteln**.

## Anmerkungen für Sendungen einrichten

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wählen Sie unter &quot;_[!UICONTROL Sales]_&quot;die Option &quot;**[!UICONTROL Sales Email]**&quot;.

1. Erweitern Sie den Abschnitt **Versandkommentare** und ändern Sie die Einstellungen nach Bedarf:

   ![Konfiguration des Versandkommentars](../configuration-reference/sales/assets/sales-emails-shipment-comments.png){width="600" zoomable="yes"}

   - Die Option **[!UICONTROL Enabled]** ist standardmäßig auf `Yes` gesetzt, was bedeutet, dass die E-Mail an einen Kunden gesendet wird, wenn ein Versandkommentar eingegeben wird.

   - Wählen Sie für **[!UICONTROL Shipment Comment Email Sender]** die Person aus, von der die E-Mail mit dem Versandkommentar gesendet wird. Standardmäßig sind fünf E-Mail-Adressen verfügbar.

   - Wählen Sie für **[!UICONTROL Shipment Comment Email Template]** die Vorlage basierend auf Ihrer Anforderung oder die Standardoption aus.

   - Wählen Sie für **[!UICONTROL Shipment Comment Email Template for Guests]** die Vorlage aus, die für Kunden verwendet wird, die kein Konto in Ihrem Store haben.

   - Geben Sie für &quot;**[!UICONTROL Shipment Comment Email Copy To]**&quot; die E-Mail-Adressen ein, an die eine E-Mail-Kopie für Versandkommentare gesendet werden soll. Trennen Sie mehrere E-Mail-Adressen durch Kommas.

   - Wählen Sie für **[!UICONTROL Shipment Comment Email Copy Method]** die Methode `bcc` (Blinde Kopie des Kohlenstoffs) oder `separate email copy` basierend auf Ihrer Voreinstellung aus.

1. Klicken Sie auf **[!UICONTROL Save Config]**.

## Abbrechen einer Sendung

Bevor eine Sendung an einen Beförderer versandt wird, kann sie durch Öffnen der Bestellung und Navigieren zur Sendung storniert werden, sofern der Beförderer Stornierungen unterstützt. Einige Fluggesellschaften beschränken oder beschränken Stornierungen nach einer Buchung. Beispielsweise erlaubt UPS Absagen, aber Sie müssen 24 Stunden warten, nachdem die Sendung gebucht wurde. Bei Annullierung einer Sendung kann die Stornierung nicht rückgängig gemacht werden. Der einzige Rückgriff besteht darin, die Bestellung neu zu erstellen.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Suchen Sie die Reihenfolge im Raster.

1. Wählen Sie in der Spalte _Aktion_ die Option **[!UICONTROL View]**.

1. Wählen Sie im linken Bereich **[!UICONTROL Shipments]** aus.

   Wenn die Sendung abgebrochen werden kann, erscheint _[!UICONTROL Cancel Shipment]_als Option in der oberen Schaltflächenleiste.

1. Klicken Sie auf **[!UICONTROL Cancel Shipment]**.

1. Klicken Sie bei Aufforderung zur Bestätigung auf **[!UICONTROL OK]**.

Der Status der Sendung ändert sich in `Canceled`. Wenn der Beförderer Stornierungen nicht unterstützt, erscheint eine Fehlermeldung, in der erklärt wird, warum die Sendung nicht storniert werden konnte.

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
| [!UICONTROL Package Label] | **PNG** - Laden Sie die Beschriftung des Versandpakets herunter. Größe: A6 (105 x 148 mm; 4,1 x 5,6 Zoll) |

{style="table-layout:auto"}
