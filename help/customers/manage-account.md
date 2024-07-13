---
title: Kundenkonten verwalten
description: Verwenden Sie das Raster [!UICONTROL Customers] , um ein beliebiges Kundenkonto zu finden und Informationen für einzelne Kundenkonten aufzurufen.
exl-id: 5f817ca8-9d1f-4498-b3bd-989713f0b6ad
source-git-commit: 0316475a37ee09948b9ba3649e059155212ab1ae
workflow-type: tm+mt
source-wordcount: '882'
ht-degree: 0%

---

# Kundenkonten verwalten

Verwenden Sie das Raster _[!UICONTROL Customers]_, um ein beliebiges Kundenkonto zu finden. Sie können die standardmäßigen [Arbeitsplatzsteuerelemente](../getting-started/admin-workspace.md) verwenden, um die Liste zu filtern, das [Spaltenlayout](../getting-started/admin-grid-controls.md) zu ändern, Ansichten zu speichern und Daten zu exportieren. Das Steuerelement [Aktionen](../getting-started/admin-actions-control.md) oberhalb des Rasters kann verwendet werden, um einen Vorgang auf mehrere Kundendatensätze anzuwenden.

![Alle Kunden](assets/customers-all-customers.png){width="700" zoomable="yes"}

Informationen zum manuellen Aktualisieren eines Kundenkontos finden Sie unter [Kundenprofil aktualisieren](update-account.md) .

## Kundenkontoaktionen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Aktivieren Sie in der ersten Spalte des Rasters das Kontrollkästchen jedes Datensatzes, den Sie aktualisieren möchten.

1. Befolgen Sie die Anweisungen für die Aktion, die Sie anwenden möchten.

   >[!INFO]
   >
   >Die folgenden Aktionen können auf einzelne oder mehrere Datensätze angewendet werden.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

### Newsletter abonnieren

Bei Multi-Store- und Multi-Site-Setups mit einem globalen [Kundenkontobereich](../customers/customer-account-scope.md) kann ein Kundenkonto für Newsletter mehrerer Sites oder Stores abonniert werden. Wenn Sie die Aktion _Abonnieren_ auf ein Kundenkonto anwenden, wird nur das Newsletter-Abonnement für die standardmäßige Site-/Store-Ansicht aktiviert.

* Setzen Sie das Steuerelement **[!UICONTROL Actions]** auf `Subscribe to newsletter`.

Weitere Informationen zur Verwaltung von Newsletter-Abonnements für einen Kunden finden Sie unter [Abonnenten verwalten](../merchandising-promotions/newsletter-subscribers.md) .

### Abmeldung vom Newsletter

Bei Multi-Store- und Multi-Site-Setups mit einem globalen [Kundenkontobereich](customer-account-scope.md) kann ein Kundenkonto für Newsletter für mehrere Sites/Stores abonniert werden. Wenn Sie die Aktion _Abonnement kündigen_ auf ein Kundenkonto anwenden, werden alle aktiven Abonnements abgemeldet.

1. Setzen Sie das Steuerelement **[!UICONTROL Actions]** auf `Unsubscribe to newsletter`.

1. Klicken Sie bei Aufforderung zur Bestätigung auf **OK**.

### Zuweisen einer Kundengruppe

1. Setzen Sie das Steuerelement **[!UICONTROL Actions]** auf `Assign a customer group`.

1. Wählen Sie die Kundengruppe aus, der alle ausgewählten Kundendatensätze zugewiesen werden sollen.

1. Klicken Sie bei Aufforderung zur Bestätigung auf **[!UICONTROL OK]**.

### Kundenkonten löschen

Gelöschte Kundenkonten können nicht wiederhergestellt werden. Informationen über Kundenaktivitäten und Transaktionen werden im System gespeichert.

1. Setzen Sie das Steuerelement **[!UICONTROL Actions]** auf `Delete`.

1. Klicken Sie bei Aufforderung zur Bestätigung auf **[!UICONTROL OK]**.

## Kundenkonten exportieren

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Klicken Sie im Menü &quot;Tabellenüberschrift&quot;auf **[!UICONTROL Export]** und wählen Sie das gewünschte Format aus:

   * CSV
   * Excel XML

1. Klicken Sie auf **[!UICONTROL OK]**.

   Die Datei wird in Ihren standardmäßigen Ordner für Downloads verschoben.

Die obige Anweisung exportiert alle Kundenkonten. Wenn Sie eine begrenzte Anzahl von Konten exportieren möchten, aktivieren Sie die Kontrollkästchen der Konten, die exportiert werden sollen, oder verwenden Sie Filter im Control Panel, um eine Reihe von Kundenkonten auszuwählen.

## Aktionen/Steuerelemente

| Option | Beschreibung |
|--- |--- |
| **[!UICONTROL Delete]** | Löscht ausgewählte Kundenkonten. Wenn das Kundenkonto zu einem Unternehmensadministrator für einen B2B-Store gehört, muss ein anderer Unternehmensbenutzer als Administrator zugewiesen werden, bevor das Kundenkonto gelöscht werden kann. |
| **[!UICONTROL Subscribe to Newsletter]** | Abonniert ausgewählte Kunden für den Newsletter. |
| **[!UICONTROL Unsubscribe from Newsletter]** | Teilt ausgewählte Kunden aus dem Newsletter ab. |
| **[!UICONTROL Assign a Customer Group]** | Weist ausgewählten Kunden einer Kundengruppe zu. |
| **[!UICONTROL Edit]** | Ermöglicht die Bearbeitung einiger Werte eines einzelnen ausgewählten Kundendatensatzes aus dem Raster. Standardmäßig sind die folgenden Werte für eine schnelle Bearbeitung verfügbar: E-Mail, Gruppe, Telefon, Postleitzahl, Website, MwSt.-Nummer und Geschlecht. |

{style="table-layout:auto"}

## Spalten

| Spalte | Beschreibung |
|--- |--- |
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
| **[!UICONTROL Date of Birth]** | Das Geburtsdatum des Kunden. Beachten Sie im Einklang mit den aktuellen Best Practices für Sicherheit und Datenschutz alle potenziellen rechtlichen und sicherheitstechnischen Risiken, die mit der Speicherung des vollständigen Geburtsdatums (Monat, Tag, Jahr) der Kunden mit anderen persönlichen Identifikatoren verbunden sind. Es wird empfohlen, die Speicherung der vollständigen Geburtsdaten der Kunden zu begrenzen und stattdessen das Geburtsjahr des Kunden zu verwenden. |
| **[!UICONTROL Tax / VAT Number]** | Falls zutreffend, die dem Kunden zugewiesene Steuernummer oder Nummer [Mehrwertsteuernummer](../stores-purchase/vat.md). <br/><br/> Dieses Feld entspricht nicht der MwSt.-Nummer. |
| **[!UICONTROL Gender]** | Das Geschlecht des Kunden. |
| **[!UICONTROL Action]** | Bearbeiten - Öffnet das Unternehmenskonto im Bearbeitungsmodus. |

{style="table-layout:auto"}

### Zusätzliche Spalten

Diese Spalten sind verfügbar, indem Sie das [Spaltenlayout](../getting-started/admin-grid-controls.md) des Rasters ändern.

| Spalte | Beschreibung |
|--- |--- |
| **[!UICONTROL Company]** | Der Firmenname des Kunden. |
| **[!UICONTROL Street Address]** | Die Straßenadresse des Kunden. |
| **[!UICONTROL City]** | Die Stadt, in der sich der Kunde befindet. |
| **[!UICONTROL Fax]** | Die Faxnummer des Kunden, falls zutreffend. |
| **[!UICONTROL Billing Firstname]** | Der Vorname in der Rechnungsadresse des Kunden. |
| **[!UICONTROL Billing Lastname]** | Der Nachname in der Rechnungsadresse des Kunden. |
| **[!UICONTROL Billing Address]** | Die Adresse, an die Rechnungsinformationen gesendet werden sollen. |
| **[!UICONTROL Shipping Address]** | Die Adresse, an die Bestellungen versandt werden sollen. |
| **[!UICONTROL VAT Number]** | Die Mehrwertsteuer-Nummer, die mit der Kundenadresse verknüpft ist. Bei in der EU verkauften [digitalen Gütern](../stores-purchase/taxes.md) basiert die Mehrwertsteuer auf der Rechnungsadresse des Kunden. <br/><br/> Dieses Feld entspricht nicht der Steuer-/MwSt-Nummer. |
| **[!UICONTROL Account Lock]** | Gibt den Status des Kontos an. Als Sicherheitsmaßnahme können Kundenkonten nach zu vielen Anmeldeversuchen [gesperrt](../customers/password-options.md) werden. Werte: `Locked` / `Unlocked` |
| **[!UICONTROL Status]** | Der aktuelle Benutzerstatus. Optionen: `Active` / `Inactive` |
| **[!UICONTROL Customer Type]** | Kundenklassifizierung. Optionen: `Individual user` / `Company admin` / `Company user` |
| **[!UICONTROL Sales Representative]** | Der Vertriebsmitarbeiter, der als Kontaktstelle für ein Unternehmenskonto zugewiesen ist und alle automatisierten E-Mail-Nachrichten erhält, die mit dem Unternehmen in Verbindung stehen. |

{style="table-layout:auto"}
