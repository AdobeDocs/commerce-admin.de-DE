---
title: Kundenliste
description: Das Raster Kunden listet alle Kunden auf, die sich für ein Konto bei Ihrem Store registriert oder vom Administrator hinzugefügt wurden.
exl-id: a7d9b098-4892-492c-b937-61cc33b836d8
source-git-commit: c855a691ed33e1e6e74865ebdfb30ddad21ad83e
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# Kundenliste

Im Admin-Raster werden alle Kunden aufgelistet, die sich für ein Konto bei Ihrem Store registriert oder vom Administrator hinzugefügt wurden. [!UICONTROL Customers] Verwenden Sie die standardmäßigen [Rastersteuerelemente](../getting-started/admin-grid-controls.md), um die Liste zu filtern und das Spaltenlayout anzupassen. Weitere Informationen finden Sie unter [Verwalten von Kundenkonten](../customers/manage-account.md).

![Kundenliste](assets/customer-accounts-all-grid.png){width="700" zoomable="yes"}

## Kundeninformationen aktualisieren

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Suchen Sie den Kundendatensatz und klicken Sie in der Spalte _[!UICONTROL Action]_auf [!UICONTROL **Bearbeiten**].

1. Wählen Sie im linken Bereich die Informationen aus, die Sie bearbeiten möchten, und nehmen Sie die erforderlichen Änderungen vor.

   >[!NOTE]
   >
   >Weitere Informationen finden Sie unter [Aktualisieren von Kundenkonten](../customers/update-account.md).

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Customer]**.

## Workspace-Steuerelemente

| Kontrolle | Beschreibung |
| --- | --- |
| **[!UICONTROL Add New Customer]** | Erstellt ein Kundenkonto. |
| **[!UICONTROL Search]** | Startet eine Suche nach Kunden basierend auf den aktuellen Filtern. |
| **[!UICONTROL Filters]** | Definiert einen Satz von Suchparametern, mit denen die im [Raster](../getting-started/admin-grid-controls.md) angezeigten Datensätze gefiltert werden. |
| **[!UICONTROL Default View]** | Legt die Standardspalte [layout](../getting-started/admin-grid-controls.md) des Rasters fest. |
| **[!UICONTROL Columns]** | Bestimmt die Auswahl von [Spalten](../getting-started/admin-grid-controls.md) und deren Konten im Raster. Das Spaltenlayout kann geändert und als _Ansicht_ gespeichert werden. Standardmäßig sind nur einige der Spalten im Raster enthalten. |
| **[!UICONTROL Export]** | Exportiert die ausgewählten Datensätze als CSV- oder Excel-XML-Datei. |

{style="table-layout:auto"}

## Spalten

| Spalte | Beschreibung |
| --- | --- |
| **[!UICONTROL Select]** | Verwaltet die Kontrollkästchen-Auswahlen für die Kundendatensätze zum Anwenden einer Aktion. Sie können auch das Auswahlsteuerelement in der Spaltenüberschrift verwenden, um alle auszuwählen/die Auswahl aufzuheben. |
| **[!UICONTROL ID]** | Eine eindeutige numerische ID, die beim Erstellen des Kundenkontos zugewiesen wird. |
| **[!UICONTROL Name]** | Der Vor- und Nachname des Kunden. |
| **[!UICONTROL Email]** | Die E-Mail-Adresse des Kunden. |
| **[!UICONTROL Group]** | Die Kundengruppe, der der Kunde zugewiesen ist. |
| **[!UICONTROL Phone]** | Die Telefonnummer des Kunden. |
| **[!UICONTROL ZIP]** | Postleitzahl des Kunden. |
| **[!UICONTROL Country]** | Das Land, in dem sich der Kunde befindet. |
| **[!UICONTROL State/Province]** | Das Bundesland oder die Provinz, in dem sich der Kunde befindet. |
| **[!UICONTROL Customer Since]** | Datum und Uhrzeit der Erstellung des Kundenkontos. |
| **[!UICONTROL Web Site]** | Die Website in der Store-Hierarchie, mit der das Kundenkonto verknüpft ist. |
| **[!UICONTROL Confirmed Email]** | Gibt an, ob eine Bestätigungs-E-Mail erforderlich ist. |
| **[!UICONTROL Account Created In]** | Gibt die Store-Ansicht an, aus der das Kundenkonto erstellt wurde. |
| **[!UICONTROL Date of Birth]** | Das Geburtsdatum des Kunden. <br><br>**_Wichtig:_**Beachten Sie im Einklang mit den aktuellen Best Practices für Sicherheit und Datenschutz alle möglichen rechtlichen und sicherheitstechnischen Risiken, die mit der Speicherung des vollständigen Geburtsdatums (Monat, Tag, Jahr) der Kunden mit anderen persönlichen Identifikatoren verbunden sind. Es wird empfohlen, die Speicherung der vollständigen Geburtsdaten der Kunden zu begrenzen und als Alternative das Geburtsjahr des Kunden zu verwenden. |
| **[!UICONTROL Tax / VAT Number]** | Falls zutreffend, die dem Kunden zugewiesene Steuernummer oder Nummer [Mehrwertsteuernummer](../stores-purchase/vat.md). <br/><br/>Dieses Feld entspricht nicht der MwSt.-Nummer. |
| **[!UICONTROL Gender]** | Das Geschlecht des Kunden. |
| **[!UICONTROL Action]** | Bearbeiten - Öffnet das Unternehmenskonto im Bearbeitungsmodus. |

{style="table-layout:auto"}

### Zusätzliche Spalten

Diese Spalten sind verfügbar, indem Sie das [Spaltenlayout](../getting-started/admin-grid-controls.md) des Rasters ändern.

| Spalte | Beschreibung |
| --- | --- |
| **[!UICONTROL Company]** | Der Firmenname des Kunden. |
| **[!UICONTROL Street Address]** | Die Straßenadresse des Kunden. |
| **[!UICONTROL City]** | Die Stadt, in der sich der Kunde befindet. |
| **[!UICONTROL Fax]** | Die Faxnummer des Kunden, falls zutreffend. |
| **[!UICONTROL Billing Firstname]** | Der Vorname in der Rechnungsadresse des Kunden. |
| **[!UICONTROL Billing Lastname]** | Der Nachname in der Rechnungsadresse des Kunden. |
| **[!UICONTROL Billing Address]** | Die Adresse, an die Rechnungsinformationen gesendet werden sollen. |
| **[!UICONTROL Shipping Address]** | Die Adresse, an die Bestellungen versandt werden sollen. |
| **[!UICONTROL VAT Number]** | Die Mehrwertsteuer-Nummer, die mit der Kundenadresse verknüpft ist. Bei in der EU verkauften [digitalen Gütern](../stores-purchase/taxes.md) basiert die Mehrwertsteuer auf der Rechnungsadresse des Kunden. <br/><br/>Dieses Feld entspricht nicht der Steuer-/MwSt-Nummer. |
| **[!UICONTROL Account Lock]** | Gibt den Status des Kontos an. Als Sicherheitsmaßnahme können Kundenkonten nach zu vielen Anmeldeversuchen [gesperrt](../customers/password-options.md) werden. Werte: `Locked` / `Unlocked` |

{style="table-layout:auto"}
