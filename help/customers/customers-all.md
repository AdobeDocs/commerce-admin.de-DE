---
title: Kundenliste
description: Das Raster Kunden listet alle Kunden auf, die sich für ein Konto bei Ihrem Geschäft registriert haben oder vom Administrator hinzugefügt wurden.
exl-id: a7d9b098-4892-492c-b937-61cc33b836d8
source-git-commit: c855a691ed33e1e6e74865ebdfb30ddad21ad83e
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# Kundenliste

In Admin listet das [!UICONTROL Customers] alle Kunden auf, die sich für ein Konto bei Ihrem Geschäft registriert haben oder vom Administrator hinzugefügt wurden. Verwenden Sie die standardmäßigen [Rastersteuerelemente](../getting-started/admin-grid-controls.md), um die Liste zu filtern und das Spaltenlayout anzupassen. Weitere Informationen finden Sie unter [Verwalten von Kundenkonten](../customers/manage-account.md).

![Kundenliste](assets/customer-accounts-all-grid.png){width="700" zoomable="yes"}

## Kundeninformationen aktualisieren

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Suchen Sie den Kundendatensatz und klicken Sie in [!UICONTROL **Spalte _[!UICONTROL Action]_&#x200B;auf**]Bearbeiten“.

1. Wählen Sie im linken Bedienfeld die Informationen aus, die Sie bearbeiten möchten, und nehmen Sie die erforderlichen Änderungen vor.

   >[!NOTE]
   >
   >Weitere Informationen finden Sie unter [Aktualisieren von ](../customers/update-account.md).

1. Klicken Sie abschließend auf **[!UICONTROL Save Customer]**.

## Workspace-Steuerelemente

| Kontrolle | Beschreibung |
| --- | --- |
| **[!UICONTROL Add New Customer]** | Erstellt ein Kundenkonto. |
| **[!UICONTROL Search]** | Startet eine Kundensuche basierend auf den aktuellen Filtern. |
| **[!UICONTROL Filters]** | Definiert einen Satz von Suchparametern, die zum Filtern der Datensätze verwendet werden, die im [Raster“ ](../getting-started/admin-grid-controls.md). |
| **[!UICONTROL Default View]** | Bestimmt die Standardspalte [Layout](../getting-started/admin-grid-controls.md) des Rasters. |
| **[!UICONTROL Columns]** | Bestimmt die Auswahl von [Spalten](../getting-started/admin-grid-controls.md) und deren Konten im Raster. Das Spalten-Layout kann geändert und als (_) gespeichert_. Standardmäßig sind nur einige der Spalten im Raster enthalten. |
| **[!UICONTROL Export]** | Exportiert die ausgewählten Datensätze als CSV- oder Excel-XML-Datei. |

{style="table-layout:auto"}

## Spalten

| Spalte | Beschreibung |
| --- | --- |
| **[!UICONTROL Select]** | Verwaltet die Kontrollkästchen-Auswahl für die Kundendatensätze zum Anwenden einer Aktion. Sie können auch die Auswahlsteuerung in der Spaltenüberschrift verwenden, um alle auszuwählen bzw. deren Auswahl aufzuheben. |
| **[!UICONTROL ID]** | Eine eindeutige numerische Kennung, die zugewiesen wird, wenn das Kundenkonto erstellt wird. |
| **[!UICONTROL Name]** | Der Vor- und Nachname des Kunden. |
| **[!UICONTROL Email]** | Die E-Mail-Adresse des Kunden. |
| **[!UICONTROL Group]** | Die Debitorengruppe, der der Debitor zugewiesen ist. |
| **[!UICONTROL Phone]** | Die Telefonnummer des Kunden. |
| **[!UICONTROL ZIP]** | Die Postleitzahl des Kunden. |
| **[!UICONTROL Country]** | Das Land, in dem sich der Kunde befindet. |
| **[!UICONTROL State/Province]** | Das Bundesland, in dem sich der Kunde befindet. |
| **[!UICONTROL Customer Since]** | Datum und Uhrzeit der Erstellung des Kundenkontos. |
| **[!UICONTROL Web Site]** | Die Website in der Store-Hierarchie, mit der das Kundenkonto verknüpft ist. |
| **[!UICONTROL Confirmed Email]** | Zeigt an, ob eine Bestätigungs-E-Mail erforderlich ist. |
| **[!UICONTROL Account Created In]** | Gibt die Store-Ansicht an, aus der das Kundenkonto erstellt wurde. |
| **[!UICONTROL Date of Birth]** | Das Geburtsdatum des Kunden. <br><br>**_Wichtig:_**&#x200B;Halten Sie sich im Einklang mit den aktuellen Best Practices für Sicherheit und Datenschutz vor potenziellen Rechts- und Sicherheitsrisiken, die mit der Speicherung des vollständigen Geburtsdatums der Kundinnen und Kunden (Monat, Tag, Jahr) mit anderen persönlichen Kennungen verbunden sind. Es wird empfohlen, die Speicherung der vollständigen Geburtsdaten von Kundinnen und Kunden zu begrenzen und vorzuschlagen, alternativ das Kundenjahr zu verwenden. |
| **[!UICONTROL Tax / VAT Number]** | Gegebenenfalls die Steuernummer oder [Umsatzsteuer-](../stores-purchase/vat.md)), die dem Kunden zugeordnet ist. <br/><br/>Dieses Feld ist nicht dasselbe wie die MwSt.-Nummer. |
| **[!UICONTROL Gender]** | Das Geschlecht des Kunden. |
| **[!UICONTROL Action]** | Bearbeiten - Öffnet das Unternehmenskonto im Bearbeitungsmodus. |

{style="table-layout:auto"}

### Zusätzliche Spalten

Diese Spalten sind verfügbar, indem Sie das [Spalten-Layout](../getting-started/admin-grid-controls.md) des Rasters ändern.

| Spalte | Beschreibung |
| --- | --- |
| **[!UICONTROL Company]** | Der Firmenname des Kunden. |
| **[!UICONTROL Street Address]** | Die Straße des Kunden. |
| **[!UICONTROL City]** | Die Stadt, in der sich der Kunde befindet. |
| **[!UICONTROL Fax]** | Die Faxnummer des Kunden, falls zutreffend. |
| **[!UICONTROL Billing Firstname]** | Der Vorname in der Rechnungsadresse des Kunden. |
| **[!UICONTROL Billing Lastname]** | Der Nachname in der Rechnungsadresse des Kunden. |
| **[!UICONTROL Billing Address]** | Die Adresse, an die die Rechnungsinformationen gesendet werden sollen. |
| **[!UICONTROL Shipping Address]** | Die Adresse, an die die Bestellungen versendet werden sollen. |
| **[!UICONTROL VAT Number]** | Die Mehrwertsteuernummer, die mit der Kundenadresse verknüpft ist. Bei [digitalen Waren](../stores-purchase/taxes.md) die in der EU verkauft werden, basiert die Mehrwertsteuer auf der Rechnungsadresse des Kunden. <br/><br/>Dieses Feld ist nicht identisch mit der Steuer-/MwSt.-Nummer. |
| **[!UICONTROL Account Lock]** | Zeigt den Status des Kontos an. Als Sicherheitsmaßnahme können Kundenkonten nach zu vielen Anmeldeversuchen [gesperrt](../customers/password-options.md) werden. Werte: `Locked` / `Unlocked` |

{style="table-layout:auto"}
