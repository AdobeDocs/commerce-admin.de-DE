---
title: Verwalten von Kundenkonten
description: Verwenden Sie das [!UICONTROL Customers] Raster, um ein beliebiges Kundenkonto zu finden und auf Informationen für einzelne Kundenkonten zuzugreifen.
exl-id: 5f817ca8-9d1f-4498-b3bd-989713f0b6ad
source-git-commit: 0316475a37ee09948b9ba3649e059155212ab1ae
workflow-type: tm+mt
source-wordcount: '882'
ht-degree: 0%

---

# Verwalten von Kundenkonten

Verwenden Sie das _[!UICONTROL Customers]_Raster, um ein beliebiges Kundenkonto zu finden. Sie können die standardmäßigen [Arbeitsplatzsteuerelemente“ verwenden](../getting-started/admin-workspace.md) um die Liste zu filtern, das [Spaltenlayout](../getting-started/admin-grid-controls.md) zu ändern, Ansichten zu speichern und Daten zu exportieren. Mit [Aktionssteuerung](../getting-started/admin-actions-control.md) über dem Raster können Sie einen Vorgang auf mehrere Kundendatensätze anwenden.

![Alle Kunden](assets/customers-all-customers.png){width="700" zoomable="yes"}

Informationen [ manuellen Aktualisierungen eines Kundenkontos finden Sie ](update-account.md) „Kundenprofil aktualisieren“.

## Kundenkonto-Aktionen

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Aktivieren Sie in der ersten Spalte des Rasters das Kontrollkästchen jedes Datensatzes, den Sie aktualisieren möchten.

1. Befolgen Sie die Anweisungen für die Aktion, die Sie anwenden möchten.

   >[!INFO]
   >
   >Die folgenden Aktionen können auf einzelne oder mehrere Datensätze angewendet werden.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

### Newsletter abonnieren

Bei Multi-Store- und Multi-Site-Setups mit einem globalen [Kundenkontobereich](../customers/customer-account-scope.md) kann ein Kundenkonto für Newsletter an mehreren Sites oder Stores abonniert werden. Wenn Sie die Aktion _Abonnieren_ auf ein Kundenkonto anwenden, wird nur für die standardmäßige Site-/Store-Ansicht das Newsletter-Abonnement aktiviert.

* Setzen Sie das **[!UICONTROL Actions]** auf `Subscribe to newsletter`.

Weitere Informationen [ Verwalten von Newsletter](../merchandising-promotions/newsletter-subscribers.md)Abonnements für eine Kundin oder einen Kunden finden Sie unter „Verwalten von Abonnentinnen und Abonnenten“.

### Newsletter abbestellen

Bei Multi-Store- und Multi-Site-Setups mit einem globalen [Kundenkontobereich](customer-account-scope.md) kann ein Kundenkonto für mehrere Sites/Stores Newsletter abonniert werden. Wenn Sie die Aktion _Abmelden_ auf ein Kundenkonto anwenden, werden alle aktiven Abonnements storniert.

1. Setzen Sie das **[!UICONTROL Actions]** auf `Unsubscribe to newsletter`.

1. Wenn Sie zur Bestätigung aufgefordert werden, klicken Sie auf **OK**.

### Zuweisen einer Kundengruppe

1. Setzen Sie das **[!UICONTROL Actions]** auf `Assign a customer group`.

1. Wählen Sie die Kundengruppe aus, der alle ausgewählten Kundendatensätze zugewiesen werden sollen.

1. Wenn Sie zum Bestätigen aufgefordert werden, klicken Sie auf **[!UICONTROL OK]**.

### Löschen von Kundenkonten

Gelöschte Kundenkonten können nicht wiederhergestellt werden. Informationen über Kundenaktivität und Transaktionen werden im System gespeichert.

1. Setzen Sie das **[!UICONTROL Actions]** auf `Delete`.

1. Wenn Sie zum Bestätigen aufgefordert werden, klicken Sie auf **[!UICONTROL OK]**.

## Kundenkonten exportieren

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Klicken Sie im Menü Tabellenüberschrift auf **[!UICONTROL Export]** und wählen Sie das gewünschte Format aus:

   * CSV
   * Excel XML

1. Klicken Sie auf **[!UICONTROL OK]**.

   Die Datei wird in den Standard-Downloads-Ordner verschoben.

Die obige Anweisung exportiert alle Kundenkonten. Wenn Sie einen begrenzten Satz exportieren möchten, aktivieren Sie die Kontrollkästchen für die Konten, die Sie exportieren möchten, oder verwenden Sie Filter im Control Panel, um eine Reihe von Kundenkonten auszuwählen.

## Aktionen/Steuerelemente

| Option | Beschreibung |
|--- |--- |
| **[!UICONTROL Delete]** | Löscht ausgewählte Kundenkonten. Wenn das Kundenkonto zu einem Unternehmensadministrator für einen B2B-Store gehört, muss ein anderer Unternehmensbenutzer als Administrator zugewiesen werden, bevor das Kundenkonto gelöscht werden kann. |
| **[!UICONTROL Subscribe to Newsletter]** | Abonniert ausgewählte Kunden für den Newsletter. |
| **[!UICONTROL Unsubscribe from Newsletter]** | Meldet ausgewählte Kunden vom Newsletter ab. |
| **[!UICONTROL Assign a Customer Group]** | Weist ausgewählte Kunden einer Kundengruppe zu. |
| **[!UICONTROL Edit]** | Ermöglicht die Bearbeitung einiger Werte eines einzelnen ausgewählten Kundendatensatzes aus dem Raster. Standardmäßig sind die folgenden Werte für eine Schnellbearbeitung verfügbar: E-Mail, Gruppe, Telefon, Postleitzahl, Website, MwSt.-Nummer und Geschlecht. |

{style="table-layout:auto"}

## Spalten

| Spalte | Beschreibung |
|--- |--- |
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
| **[!UICONTROL Date of Birth]** | Das Geburtsdatum des Kunden. Gemäß den aktuellen Best Practices für Sicherheit und Datenschutz sollten Sie sich über potenzielle rechtliche und Sicherheitsrisiken im Zusammenhang mit der Speicherung des vollständigen Geburtsdatums der Kunden (Monat, Tag, Jahr) mit anderen persönlichen Kennungen im Klaren sein. Es wird empfohlen, die Speicherung der vollständigen Geburtsdaten von Kundinnen und Kunden zu begrenzen und alternativ ein Kundenjahr zu verwenden. |
| **[!UICONTROL Tax / VAT Number]** | Gegebenenfalls die Steuernummer oder [Umsatzsteuer-](../stores-purchase/vat.md)), die dem Kunden zugeordnet ist. <br/><br/> Dieses Feld ist nicht dasselbe wie die MwSt.-Nummer. |
| **[!UICONTROL Gender]** | Das Geschlecht des Kunden. |
| **[!UICONTROL Action]** | Bearbeiten - Öffnet das Unternehmenskonto im Bearbeitungsmodus. |

{style="table-layout:auto"}

### Zusätzliche Spalten

Diese Spalten sind verfügbar, indem Sie das [Spalten-Layout](../getting-started/admin-grid-controls.md) des Rasters ändern.

| Spalte | Beschreibung |
|--- |--- |
| **[!UICONTROL Company]** | Der Firmenname des Kunden. |
| **[!UICONTROL Street Address]** | Die Straße des Kunden. |
| **[!UICONTROL City]** | Die Stadt, in der sich der Kunde befindet. |
| **[!UICONTROL Fax]** | Die Faxnummer des Kunden, falls zutreffend. |
| **[!UICONTROL Billing Firstname]** | Der Vorname in der Rechnungsadresse des Kunden. |
| **[!UICONTROL Billing Lastname]** | Der Nachname in der Rechnungsadresse des Kunden. |
| **[!UICONTROL Billing Address]** | Die Adresse, an die die Rechnungsinformationen gesendet werden sollen. |
| **[!UICONTROL Shipping Address]** | Die Adresse, an die die Bestellungen versendet werden sollen. |
| **[!UICONTROL VAT Number]** | Die Mehrwertsteuernummer, die mit der Kundenadresse verknüpft ist. Bei [digitalen Waren](../stores-purchase/taxes.md) die in der EU verkauft werden, basiert die Mehrwertsteuer auf der Rechnungsadresse des Kunden. <br/><br/> Dieses Feld ist nicht identisch mit der Steuer-/MwSt.-Nummer. |
| **[!UICONTROL Account Lock]** | Zeigt den Status des Kontos an. Als Sicherheitsmaßnahme können Kundenkonten nach zu vielen Anmeldeversuchen [gesperrt](../customers/password-options.md) werden. Werte: `Locked` / `Unlocked` |
| **[!UICONTROL Status]** | Der aktuelle Benutzerstatus. Optionen: `Active` / `Inactive` |
| **[!UICONTROL Customer Type]** | Kundenklassifizierung. Optionen: `Individual user` / `Company admin` / `Company user` |
| **[!UICONTROL Sales Representative]** | Der Vertriebsmitarbeiter, der als Ansprechpartner für ein Firmenkonto zugewiesen wird und alle automatisierten E-Mail-Nachrichten im Zusammenhang mit dem Unternehmen erhält. |

{style="table-layout:auto"}
