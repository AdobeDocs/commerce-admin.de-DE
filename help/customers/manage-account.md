---
title: Kundenkonten verwalten
description: Verwenden Sie die [!UICONTROL Customers] -Raster zur Suche nach einem beliebigen Kundenkonto und Zugriffsinformationen für einzelne Kundenkonten.
exl-id: 5f817ca8-9d1f-4498-b3bd-989713f0b6ad
source-git-commit: 0316475a37ee09948b9ba3649e059155212ab1ae
workflow-type: tm+mt
source-wordcount: '883'
ht-degree: 0%

---

# Kundenkonten verwalten

Verwenden Sie die _[!UICONTROL Customers]_-Raster, um ein beliebiges Kundenkonto zu finden. Sie können den Standard [Arbeitsablaufkontrollen](../getting-started/admin-workspace.md) Um die Liste zu filtern, ändern Sie die [Spaltenlayout](../getting-started/admin-grid-controls.md), Ansichten speichern und Daten exportieren. Die [Aktionssteuerung](../getting-started/admin-actions-control.md) über dem Raster können Sie einen Vorgang auf mehrere Kundendatensätze anwenden.

![Alle Kunden](assets/customers-all-customers.png){width="700" zoomable="yes"}

Siehe [Kundenprofil aktualisieren](update-account.md) für Informationen zum manuellen Aktualisieren eines Kundenkontos.

## Kundenkontoaktionen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Aktivieren Sie in der ersten Spalte des Rasters das Kontrollkästchen jedes Datensatzes, den Sie aktualisieren möchten.

1. Befolgen Sie die Anweisungen für die Aktion, die Sie anwenden möchten.

   >[!INFO]
   >
   >Die folgenden Aktionen können auf einzelne oder mehrere Datensätze angewendet werden.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

### Newsletter abonnieren

In Multi-Store- und Multi-Site-Setups mit einer globalen [Kundenkontobereich](../customers/customer-account-scope.md), kann ein Kundenkonto Newsletter über mehrere Sites oder Stores abonnieren. Wenn Sie die _Abonnieren_ -Aktion auf ein Kundenkonto verweist, wird das Newsletter-Abonnement nur für die standardmäßige Site-/Store-Ansicht aktiviert.

* Legen Sie die **[!UICONTROL Actions]** Kontrolle an `Subscribe to newsletter`.

Siehe [Abonnenten verwalten](../merchandising-promotions/newsletter-subscribers.md) für weitere Informationen zur Verwaltung von Newsletter-Abonnements für einen Kunden.

### Abmeldung vom Newsletter

In Multi-Store- und Multi-Site-Setups mit einer globalen [Kundenkontobereich](customer-account-scope.md), kann ein Kundenkonto für Newsletter für mehrere Sites/Geschäfte abonniert werden. Wenn Sie die _Abmelden_ -Aktion auf ein Kundenkonto verweist, werden alle aktiven Abonnements abgemeldet.

1. Legen Sie die **[!UICONTROL Actions]** Kontrolle an `Unsubscribe to newsletter`.

1. Klicken Sie bei Aufforderung zur Bestätigung auf **OK**.

### Zuweisen einer Kundengruppe

1. Legen Sie die **[!UICONTROL Actions]** Kontrolle an `Assign a customer group`.

1. Wählen Sie die Kundengruppe aus, der alle ausgewählten Kundendatensätze zugewiesen werden sollen.

1. Klicken Sie bei Aufforderung zur Bestätigung auf **[!UICONTROL OK]**.

### Kundenkonten löschen

Gelöschte Kundenkonten können nicht wiederhergestellt werden. Informationen über Kundenaktivitäten und Transaktionen werden im System gespeichert.

1. Legen Sie die **[!UICONTROL Actions]** Kontrolle an `Delete`.

1. Klicken Sie bei Aufforderung zur Bestätigung auf **[!UICONTROL OK]**.

## Kundenkonten exportieren

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Klicken Sie im Menü Tabellenüberschrift auf **[!UICONTROL Export]** und wählen Sie das gewünschte Format aus:

   * CSV
   * Excel XML

1. Klicken **[!UICONTROL OK]**.

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
| **[!UICONTROL Tax / VAT Number]** | Gegebenenfalls die Steuernummer oder [Mehrwertsteuer](../stores-purchase/vat.md) Nummer, die dem Kunden zugewiesen ist. <br/><br/> Dieses Feld entspricht nicht der MwSt.-Nummer. |
| **[!UICONTROL Gender]** | Das Geschlecht des Kunden. |
| **[!UICONTROL Action]** | Bearbeiten - Öffnet das Unternehmenskonto im Bearbeitungsmodus. |

{style="table-layout:auto"}

### Zusätzliche Spalten

Diese Spalten können durch Ändern der [Spaltenlayout](../getting-started/admin-grid-controls.md) des Rasters.

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
| **[!UICONTROL VAT Number]** | Die Mehrwertsteuer-Nummer, die mit der Kundenadresse verknüpft ist. Für [digitale Waren](../stores-purchase/taxes.md) in der EU verkauft wird, basiert die Mehrwertsteuer auf der Rechnungsadresse des Kunden. <br/><br/> Dieses Feld entspricht nicht der Steuer-/MwSt-Nummer. |
| **[!UICONTROL Account Lock]** | Gibt den Status des Kontos an. Als Sicherheitsmaßnahme können Kundenkonten [locked](../customers/password-options.md) nach zu vielen Anmeldeversuchen. Werte: `Locked` / `Unlocked` |
| **[!UICONTROL Status]** | Der aktuelle Benutzerstatus. Optionen: `Active` / `Inactive` |
| **[!UICONTROL Customer Type]** | Kundenklassifizierung. Optionen: `Individual user` / `Company admin` / `Company user` |
| **[!UICONTROL Sales Representative]** | Der Vertriebsmitarbeiter, der als Kontaktstelle für ein Unternehmenskonto zugewiesen ist und alle automatisierten E-Mail-Nachrichten erhält, die mit dem Unternehmen in Verbindung stehen. |

{style="table-layout:auto"}
