---
title: Sendungen
description: Erfahren Sie, wie Sie Versanddatensätze für Rechnungen erstellen und Sendungen stornieren können.
exl-id: 6df83549-ba38-43f7-aab1-dbf3f6b89d74
feature: Shipping/Delivery, Invoices
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '948'
ht-degree: 0%

---

# Sendungen

Das _[!UICONTROL Shipments]_-Raster listet den Versanddatensatz aller Rechnungen auf, die für den Versand vorbereitet wurden. Ein Sendungsnachweis kann erzeugt werden, wenn eine Bestellung ([) ](invoices.md) später erstellt wird.

Adobe Commerce und Magento Open Source unterstützen den Versand partieller und vollständiger Bestellungen. Zusätzliche Optionen sind bei [Inventory management](../inventory-management/introduction.md) und Erweiterungen von Drittanbietern verfügbar.

![Versandraster](./assets/shipments.png){width="600" zoomable="yes"}

## Spaltenbeschreibungen

| Spalte oder Steuerelement | Beschreibung |
|--- |--- |
| [!UICONTROL Select] | Aktivieren Sie das Kontrollkästchen für jedes Angebot, das einer Aktion unterzogen werden soll, oder verwenden Sie die Auswahlsteuerung in der Spaltenüberschrift. Optionen: `Select All` / `Deselect All` |
| [!UICONTROL Shipment] | Eine eindeutige, sequenzielle Nummer, die zugewiesen wird, wenn eine neue Sendung zum ersten Mal gespeichert wird |
| [!UICONTROL Ship Date] | Versanddatum |
| [!UICONTROL Order] | Eindeutige Bestellnummer |
| [!UICONTROL Order Date] | Datum und Uhrzeit der Bestellung |
| [!UICONTROL Ship-to Name] | Der Name der Person, an die die Bestellung gesendet wird |
| [!UICONTROL Total Quantity] | Gesamtmenge der zu versendenden Artikel |
| [!UICONTROL Action] | Ansicht öffnet die Sendung im Bearbeitungsmodus |

{style="table-layout:auto"}

Zusätzliche Spalten:

| Spalte | Beschreibung |
|--- |--- |
| [!UICONTROL Order Status] | Zeigt den Bestellstatus an |
| [!UICONTROL Purchased From] | Gibt die Website-, Store- und Store-Ansicht an, in der die Bestellung aufgegeben wurde |
| [!UICONTROL Customer Name] | Der Name des Kunden oder Käufers, der die Bestellung aufgegeben hat |
| [!UICONTROL Email] | Die E-Mail-Adresse eines registrierten Kunden |
| [!UICONTROL Customer Group] | Der Name der Kundengruppe oder des freigegebenen Katalogs, dem der Kunde zugewiesen ist |
| [!UICONTROL Billing Address] | Der Name des Kunden oder Käufers, der die Bestellung aufgegeben hat |
| [!UICONTROL Shipping Address] | Der Name der Person, an die die Bestellung gesendet wird |
| [!UICONTROL Payment Method] | Die für die Bestellung zu verwendende Zahlungsmethode |
| [!UICONTROL Shipping Information] | Die Methode, die für den Versand der Bestellung verwendet werden soll |

{style="table-layout:auto"}

## Erstellen einer Sendung

Die folgenden Anweisungen führen Sie durch den Prozess zum Erstellen einer Sendung in Adobe Commerce oder Magento Open Source. Wenn Sie Inventory management aktiviert haben, können Sie &quot;[ Sendungen mit mehreren Source erstellen](../inventory-management/shipments-create.md) prüfen und eine Herkunft (oder einen Lagerort) sowie eine zu versendende Menge pro Zeileneintrag auswählen.

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Suchen Sie die Reihenfolge im Raster und öffnen Sie sie.

1. Wenn die Bestellung bezahlt, fakturiert und versandbereit ist, klicken Sie auf **[!UICONTROL Ship]**.

   Die Abschnitte oben in der Sendung enthalten Namen, Adresse und Zahlungsinformationen aus dem Kundenauftrag.

1. Füllen Sie jeden Abschnitt des Versandformulars entsprechend den Anweisungen in den folgenden Abschnitten aus.

### [!UICONTROL Items to Ship]

Ändern Sie die **[!UICONTROL Qty to Ship]** für jeden Zeileneintrag in der Reihenfolge nach Bedarf.

### [!UICONTROL Shipping Information]

**Methode 1:** Verwenden der Bestellseite

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Klicken Sie in der Spalte **[!UICONTROL Action]** für die ausgewählte Bestellung auf **[!UICONTROL View]**.

1. Klicken Sie auf **[!UICONTROL Ship]**.

1. Scrollen Sie nach unten zum _[!UICONTROL Payment & Shipping Method]_&#x200B;Block und klicken Sie auf **[!UICONTROL Add Tracking Number]**.

1. **[!UICONTROL Carrier]** festlegen:

   - `Custom Value`
   - `DHL`
   - `Federal Express`
   - `United Parcel Service`
   - `United States Postal Service`

1. Geben Sie **[!UICONTROL Title]** und **[!UICONTROL Number]** ein, um die Sendung zu verfolgen.

**Methode 2:** Versandseite verwenden

Diese Methode ist nur zulässig, wenn die Bestellanlieferung bereits auf der Bestellseite erstellt wurde.
Sie können die Versand- und Tracking-Informationen nach Bedarf auf der Seite „Direktversand“ ändern:

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. Suchen und öffnen Sie die Sendung im Bearbeitungsmodus.

1. Scrollen Sie nach unten zum _[!UICONTROL Payment & Shipping Method]_.

1. Wählen Sie die **[!UICONTROL Carrier]** aus.

1. Geben Sie einen **[!UICONTROL Title]** für das Paket ein.

1. Tracking-**[!UICONTROL Number]** eingeben.

1. Klicken Sie auf **[!UICONTROL Add]**.

1. Um eine E-Mail mit Tracking-Informationen an den Kunden zu senden, klicken Sie auf **[!UICONTROL Send Tracking Information]** und bestätigen Sie die Aktion.

   Um den Standort einer Sendung zu verfolgen, öffnen Sie die gewünschte Sendung im Bearbeitungsmodus und klicken Sie auf **[!UICONTROL Track this shipment]**.

   ![Versand- und Tracking-Informationen](./assets/tracking-information.png){width="600" zoomable="yes"}

### Schaltflächen

| Schaltfläche | Beschreibung |
|--- |--- |
| **[!UICONTROL Back]** | Schließt das Formular Neue Sendung und kehrt zur Bestellung zurück |
| **[!UICONTROL Submit Shipment]** | Fügt die Lieferung für die Bestellung hinzu. |
| **[!UICONTROL Reset]** | Stellt alle Felder auf Originalwerte zurück. |

{style="table-layout:auto"}

### Versandkommentare

1. Geben Sie **Anmerkungen** für die Lieferung ein, falls erforderlich.

1. Wenn die Sendung fertig ist, klicken Sie auf **Sendung starten**.

## Kommentare für Sendungen einrichten

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wählen Sie unter _[!UICONTROL Sales]_&#x200B;die Option **[!UICONTROL Sales Email]**.

1. Erweitern Sie den Abschnitt **Versandkommentare** und ändern Sie die Einstellungen nach Bedarf:

   ![Konfiguration des Versandkommentars](../configuration-reference/sales/assets/sales-emails-shipment-comments.png){width="600" zoomable="yes"}

   - Die Option **[!UICONTROL Enabled]** ist standardmäßig auf `Yes` festgelegt, was bedeutet, dass die E-Mail an einen Kunden gesendet wird, wenn ein Versandkommentar eingegeben wird.

   - Wählen Sie **[!UICONTROL Shipment Comment Email Sender]** die Person aus, von der die E-Mail mit dem Versandkommentar gesendet wird. Der Standard bietet fünf E-Mail-Adressen.

   - Wählen Sie **[!UICONTROL Shipment Comment Email Template]** je nach Anforderung eine Vorlage aus oder wählen Sie die Standardoption aus.

   - Wählen Sie **[!UICONTROL Shipment Comment Email Template for Guests]** die Vorlage für Kunden, die kein Konto in Ihrem Geschäft haben.

   - Geben Sie **[!UICONTROL Shipment Comment Email Copy To]** die E-Mail-Adressen ein, an die eine Kopie des Versandkommentars gesendet werden soll. Trennen Sie mehrere E-Mail-Adressen durch ein Komma.

   - Wählen Sie **[!UICONTROL Shipment Comment Email Copy Method]** je nach Ihren Vorlieben `bcc` (Blindkopie) oder `separate email copy` Methode aus.

1. Klicken Sie auf **[!UICONTROL Save Config]**.

## Sendung stornieren

Bevor eine Sendung an einen Spediteur versendet wird, kann sie storniert werden, indem Sie die Bestellung öffnen und zur Sendung navigieren, sofern der Spediteur Stornierungen unterstützt. Einige Fluggesellschaften schränken Stornierungen nach einer Buchung ein oder begrenzen sie. UPS ermöglicht beispielsweise Stornierungen, verlangt jedoch, dass Sie 24 Stunden nach der Buchung der Sendung warten. Wenn eine Lieferung storniert wird, kann die Stornierung nicht rückgängig gemacht werden. Die einzige Möglichkeit besteht darin, die Bestellung neu zu erstellen.

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Suchen Sie die Reihenfolge im Raster.

1. Wählen Sie in _Spalte_ Aktion **[!UICONTROL View]** aus.

1. Wählen Sie im linken Bedienfeld **[!UICONTROL Shipments]** aus.

   Wenn die Sendung storniert werden kann, wird _[!UICONTROL Cancel Shipment]_&#x200B;als Option in der oberen Symbolleiste angezeigt.

1. Klicken Sie auf **[!UICONTROL Cancel Shipment]**.

1. Wenn Sie zum Bestätigen aufgefordert werden, klicken Sie auf **[!UICONTROL OK]**.

Der Status der Lieferung ändert sich in `Canceled`. Wenn der Spediteur keine Stornierungen unterstützt, wird eine Fehlermeldung angezeigt, in der erläutert wird, warum die Sendung nicht storniert werden konnte.

## Beschreibung der Versandfelder

### [!UICONTROL Shipping Information]

| Feld | Beschreibung |
|-----|-----------|
| [!UICONTROL Carrier] | Der Name des ausgewählten Anbieters |
| [!UICONTROL Title] | Ein beschreibender Name, der dem Paket vom Provider zugewiesen wurde. |
| [!UICONTROL Number] | Die verknüpfte Tracking-Nummer, die dem Paket zugewiesen ist. |
| [!UICONTROL Action] | ![Papierkorb-Symbol](../assets/icon-delete-trashcan-solid.png) - Löscht die Paketinformationen aus dem Sendungsdatensatz. |
| [!UICONTROL Add] | Fügen Sie der Sendung ein weiteres Paket hinzu. |

{style="table-layout:auto"}

### [!UICONTROL Route Information]

| Feld | Beschreibung |
|-----|-----------|
| [!UICONTROL Origin Location] | Zeigt eine Liste der verfügbaren Speicherorte an. |
| [!UICONTROL International] | Wenn diese Option aktiviert ist, wird die Sendung als internationale Sendung identifiziert. |

{style="table-layout:auto"}

### [!UICONTROL Items Ordered]

| Feld | Beschreibung |
|-----|-----------|
| [!UICONTROL Description] | Die Beschreibung des Elements. |
| [!UICONTROL SKU] | Die Lagerhaltungseinheit des Artikels. |
| [!UICONTROL Weight] | Die Gewichtung des Elements. |
| [!UICONTROL Qty Ordered] | Die Menge des bestellten Artikels. |
| [!UICONTROL Qty Shipped] | Die Menge der Artikel, die versandt wurden. |
| [!UICONTROL Qty Packed] | Die Anzahl der in diesem Paket enthaltenen Elemente. |

{style="table-layout:auto"}

### [!UICONTROL Shipment Comments]

| Feld | Beschreibung |
|-----|-----------|
| [!UICONTROL Comments] | Anmerkungen zur Sendung sind für den internen Gebrauch bestimmt. |

{style="table-layout:auto"}

### [!UICONTROL Documentation]

| Feld | Beschreibung |
|-----|-----------|
| [!UICONTROL Package Label] | **PNG** - Laden Sie die Bezeichnung des Versandpakets herunter. Größe: A6 (105 x 148 mm; 4,1 x 5,6 Zoll) |

{style="table-layout:auto"}
