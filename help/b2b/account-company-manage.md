---
title: Verwalten von Unternehmenskonten
description: Erfahren Sie, wie Sie Unternehmenskonten für Ihren Adobe Commerce-Store mithilfe der Seite "Unternehmen"und der im Raster verfügbaren Tools verwalten.
exl-id: 9e125fc2-d20e-463e-a391-582fa0bcb68d
feature: B2B, Companies, Configuration
source-git-commit: fa8083570a4637c4bf67f7657ef9d0d48f962c50
workflow-type: tm+mt
source-wordcount: '2493'
ht-degree: 0%

---

# Verwalten von Unternehmenskonten

Die _[!UICONTROL Companies]_auf der Seite werden alle aktuellen Unternehmenskonten aufgelistet, unabhängig vom Status. Alle ausstehenden Genehmigungsanfragen werden oben in der Liste angezeigt. Der Standard [Arbeitsablaufkontrollen](../getting-started/admin-workspace.md) kann verwendet werden, um die Liste zu filtern, ändern Sie [Spaltenlayout](../getting-started/admin-grid-controls.md), Ansichten speichern oder Daten exportieren.

Die _[!UICONTROL Actions]_-Kontrolle über das Raster kann verwendet werden, um eine Aktion auf mehrere Firmendatensätze anzuwenden. Anstatt beispielsweise jede einzelne Anforderung eines Unternehmens zu genehmigen, können Sie mehrere Anforderungen auswählen und die Konten in einer einzigen Aktion aktivieren. Die verfügbaren Aktionen hängen von der [Berechtigungen](../systems/permissions.md) für die Rolle, die Ihrem Admin-Benutzerkonto zugewiesen ist.

Verwenden Sie die _[!UICONTROL Search]_-Funktion zum Finden von Unternehmen in **Unternehmen**nach Keyword. Die Suche indiziert Suchbegriffe aus der **Firmenname**und **Übergeordnet**Spalten. Sie können nach **Firmentyp**, um nur einzelne Unternehmen, nur Muttergesellschaften oder nur untergeordnete Unternehmen anzuzeigen.

![Unternehmensraster](./assets/companies-grid-view.png){width="700" zoomable="yes"}

## Ressourcen für Unternehmensrollen

Die [Rollenressourcen](../systems/permissions-user-roles.md#role-resources) -Einstellungen bestimmen die Fähigkeit:

- Unternehmen hinzufügen
- Unternehmen löschen
- Anwenden einer Resterstattung
- Unternehmen anzeigen

Diese Rollenressourcen müssen für die [Benutzerrolle](../systems/permissions-user-roles.md) , das für das Admin-Benutzerkonto zugewiesen ist.

## Anwenden einer Aktion

Die folgenden Aktionen können auf einzelne oder mehrere Datensätze angewendet werden.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Aktivieren Sie in der ersten Spalte des Rasters das Kontrollkästchen jedes Datensatzes, den Sie aktualisieren möchten, und befolgen Sie die Anweisungen für die Aktion, die Sie anwenden möchten:

### Unternehmenskonten aktivieren

1. Aus dem **[!UICONTROL Actions]** Kontrolle, wählen Sie **[!UICONTROL Set Active]**.

1. Klicken Sie bei Aufforderung zur Bestätigung auf **[!UICONTROL OK]**.

### Festlegen von aktiv/inaktiv

Kunden mit inaktiven Konten können sich nicht über ihre Konten anmelden oder Einkäufe tätigen. Es gibt zwei Methoden, um ein Kundenkonto als aktiv oder inaktiv festzulegen:

Methode 1: **Über das Kundenraster**

1. Im _Admin_ Seitenleiste, navigieren Sie zu [!UICONTROL **Kunden**] > [!UICONTROL **Alle Kunden**].

1. Aus dem **[!UICONTROL Actions]** Wählen Sie eines der folgenden Elemente aus:

   - **[!UICONTROL Active]**
   - **[!UICONTROL Inactive]**

1. Wählen Sie bei Aufforderung **[!UICONTROL OK]** , um die Änderung anzuwenden.

Methode 2: **Auf der Seite zur Kontobearbeitung**

1. Im _Admin_ Seitenleiste, navigieren Sie zu [!UICONTROL **Kunden**] > [!UICONTROL **Alle Kunden**].

1. Suchen Sie im Raster den zu bearbeitenden Kundendatensatz.

1. Im _Aktionen_ -Spalte ganz rechts auswählen [!UICONTROL **Bearbeiten**].

1. Wählen Sie die [!UICONTROL **Kontoinformationen**] Registerkarte.

1. Satz [!UICONTROL **Kundenaktiv**] nach `Yes` oder `No`.

1. Klicks [!UICONTROL **Kunden speichern**].

### Unternehmenskonten blockieren

Benutzer, die mit einem gesperrten Unternehmenskonto verknüpft sind, können sich anmelden und auf den Katalog zugreifen, jedoch keine Käufe tätigen. Ein Unternehmen mit einem Konto, das nicht in gutem Zustand ist, kann vorübergehend gesperrt werden, bis die Angelegenheit geklärt ist.

1. Aus dem **[!UICONTROL Actions]** Kontrolle, wählen Sie **[!UICONTROL Block]**.

1. Klicken Sie bei Aufforderung zur Bestätigung auf **[!UICONTROL OK]**.

### Unternehmenskonten löschen

Gelöschte Unternehmenskonten können nicht wiederhergestellt werden. Der Status der Benutzerkonten, die mit dem Unternehmen verknüpft sind, wird auf `Inactive` und die Firmen-ID aus den Profilen der Benutzerkonten entfernt wird. Informationen über Unternehmenstätigkeiten und Transaktionen werden im System gespeichert.

1. Aus dem **[!UICONTROL Actions]** Kontrolle, wählen Sie **[!UICONTROL Delete]**.

1. Klicken Sie bei Aufforderung zur Bestätigung auf **[!UICONTROL OK]**.

### Kreditwährung konvertieren

Der Kredit in den Konten ausgewählter Unternehmen wird in den aktuellen Kurs der ausgewählten Währung umgerechnet.

1. Aus dem **[!UICONTROL Actions]** Kontrolle, wählen Sie **[!UICONTROL Convert Currency]**.

1. Klicken Sie bei Aufforderung zur Bestätigung auf **[!UICONTROL OK]**.

1. Wählen Sie die **[!UICONTROL Credit Currency]** für die ausgewählten Unternehmenskonten verwendet werden.

   Die Beträge werden, sofern verfügbar, entsprechend den aktuellen Konversionsraten neu berechnet. Falls nicht verfügbar, können Sie benutzerdefinierte Konversionsraten manuell eingeben. Das System zeigt so viele Konversionsberechnungen an, wie für die von den ausgewählten Unternehmen verwendete Kreditwährung erforderlich sind.

1. Klicks **[!UICONTROL Proceed]** , um die Konvertierung abzuschließen.

## Bearbeiten von Unternehmenskonten

Methode 1: **Schnellbearbeitung**

1. Aktivieren Sie in der ersten Spalte das Kontrollkästchen des zu bearbeitenden Unternehmenskontos.

1. Aus dem **[!UICONTROL Actions]** Kontrolle, wählen Sie **[!UICONTROL Edit]**.

   Jeder zu aktualisierende Wert wird in einem Textfeld angezeigt.

   ![Schnellbearbeitung für ein Unternehmenskonto](./assets/companies-grid-quick-edit.png){width="700" zoomable="yes"}

1. Aktualisieren Sie einen der folgenden Werte nach Bedarf:

   - **[!UICONTROL Company Name]**

   - **[!UICONTROL Company Email]**

   - **[!UICONTROL Phone Number]**

1. Klicks **[!UICONTROL Save]**.

Methode 2: **Vollständige Bearbeitung**

1. Suchen Sie im Raster den zu bearbeitenden Firmendatensatz.

1. Auswählen **[!UICONTROL Edit]** aus dem _[!UICONTROL Action]_Spalte.

1. Nehmen Sie die erforderlichen Änderungen an den Unternehmensinformationen vor.

Feldbeschreibungen finden Sie unter [Unternehmenskonto erstellen](account-company-create.md).

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]**.

## Vertriebsmitarbeiter zuweisen

Der Vertriebsmitarbeiter ist ein [Admin-Benutzer](../systems/permissions.md) der als Kontaktstelle für ein Unternehmenskonto zugewiesen wird und alle automatisierten [E-Mail-Nachrichten](../b2b/enable-basic-features.md#configure-company-email-options) mit dem Unternehmen in Verbindung stehen. Pro Unternehmenskonto kann nur ein Vertriebsmitarbeiter zugewiesen werden, aber ein einzelner Vertriebsmitarbeiter kann mehrere Unternehmenskonten verwalten. Das standardmäßige Admin-Benutzerkonto wird als Vertriebsmitarbeiter zugewiesen, es sei denn, es wird ein anderer Admin-Benutzer zugewiesen.

Der Name und die E-Mail-Adresse des zugewiesenen Vertriebsmitarbeiters sind für die Mitglieder des Unternehmens über das Unternehmenskonto und die Anführungsseite sichtbar.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Suchen Sie das Unternehmen im Raster und öffnen Sie es im Bearbeitungsmodus.

1. Satz **[!UICONTROL Sales Representative]** dem Admin-Benutzer, den Sie als Kontaktpunkt für das Unternehmen zuweisen möchten.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]**.

   Der zugewiesene Vertriebsmitarbeiter erhält eine E-Mail-Benachrichtigung über die Zuweisung.

## Firmenprofil aktualisieren

Das Unternehmensprofil kann vom Storefront durch den Unternehmensadministrator und vom Administrator von einem Store-Administrator gepflegt werden.

![Firmenprofil](./assets/company-update.png){width="700" zoomable="yes"}

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Suchen Sie das Unternehmen im Raster und klicken Sie auf **[!UICONTROL Edit]** im _[!UICONTROL Action]_Spalte.

1. Aktualisieren Sie die Feldwerte in den einzelnen Abschnitten nach Bedarf mithilfe der Feldbeschreibungen zur Referenz.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]**.

## Demo zum Unternehmenskonto

In diesem Video erfahren Sie mehr über die Verwaltung von Unternehmenskonten:

>[!VIDEO](https://video.tv.adobe.com/v/344447?quality=12)

## Unternehmensverwaltung

[!BADGE 1.5.0-Beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Nur für Beta-Programmteilnehmer verfügbar"}

Nachdem ein Unternehmen erstellt wurde, können Admin-Benutzer mit entsprechenden Berechtigungen die [!UICONTROL Company Hierarchy] , um eine Muttergesellschaft zu erstellen, indem Sie die benannte Muttergesellschaft bearbeiten und verbundene Unternehmen zuweisen.

Wenn ein Unternehmen einer Hierarchie hinzugefügt wurde, wird die [!UICONTROL Company Hierarchy] zeigt die Muttergesellschaft und alle zugeordneten Unternehmen im Netz an.

Siehe [Verwalten der Unternehmenshierarchie](assign-companies.md) für weitere Informationen.

## Unternehmensoptionen und Spalten

Die folgenden Abschnitte enthalten eine Referenz zu den verfügbaren Aktionen, Optionen und angezeigten Informationen, die für die Verwaltung von Unternehmenskonten verfügbar sind.

### Aktionssteuerungsoptionen

| Option | Beschreibung |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Set Active] | Legt den Status aller ausgewählten Firmendatensätze auf `Active`. Unternehmensadministratoren erhalten Anweisungen zum Festlegen ihrer Kennwörter, damit sie über das Storefront auf ihre Konten zugreifen und ihre Unternehmen verwalten können. |
| [!UICONTROL Block] | Beschränkt Unternehmenskonten, die nicht gut aufgestellt sind, und behält das Konto bei. Die Mitglieder des Unternehmens können sich anmelden und auf den Katalog zugreifen, können jedoch keine Bestellungen im Namen des Unternehmens tätigen. |
| [!UICONTROL Delete] | Löscht die ausgewählten Unternehmenskonten. Der Status der Benutzerkonten, die einem gelöschten Unternehmen zugeordnet sind, wird auf `Inactive` und die Firmen-ID aus den Profilen der Benutzerkonten entfernt wird. Informationen über Unternehmenstätigkeiten und Transaktionen werden im System gespeichert. |
| [!UICONTROL Edit] | Ermöglicht die Bearbeitung einiger Werte des ausgewählten Firmendatensatzes über das Raster. Standardmäßig sind die Werte &quot;Firmenname&quot;, &quot;Firmenemail&quot;und &quot;Telefonnummer&quot;für eine schnelle Bearbeitung verfügbar. |
| [!UICONTROL Convert Credit] | Konvertiert den Guthaben für die ausgewählten Unternehmen entsprechend den Kursen der angegebenen Währung. |

{style="table-layout:auto"}

### Spaltenbeschreibungen


#### Standardspaltenlayout

| Spalte | Beschreibung |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Select] | Kontrollkästchen zur Auswahl von Firmendatensätzen, die Gegenstand einer Aktion sein sollen, oder zur Auswahl bzw. zum Aufheben der Auswahl aller Datensätze mithilfe des Auswahlsteuerelements in der Spaltenüberschrift |
| [!UICONTROL ID] | Eine eindeutige numerische Kennung, die zugewiesen wird, wenn die Anforderung zum Erstellen eines Unternehmens gesendet wird. |
| [!UICONTROL Company Name] | Der Unternehmensname wird bei der ersten Erstellung des Unternehmenskontos angegeben und kann eine gekürzte Version des vollständigen rechtlichen Namens sein. |
| [!UICONTROL Company Type] | Der Typ von [Firma](manage-companies.md). Optionen: <br/>**[!UICONTROL Company]**- Standardmäßig werden neue Unternehmen als Einzelunternehmen erstellt.<br/>**[!UICONTROL Parent]** - Das Unternehmen ist eine Muttergesellschaft anderer Unternehmen. <br/>**[!UICONTROL Child]**- Dieses Unternehmen ist mit einer Muttergesellschaft verbunden. |
| [!UICONTROL Parent] | Zeigt die Muttergesellschaft für diese spezifische Unternehmenszeile an. |
| [!UICONTROL Company Email] | Die mit dem Unternehmenskonto verknüpfte E-Mail-Adresse. |
| [!UICONTROL Phone Number] | Die primäre Telefonnummer des Unternehmens. |
| [!UICONTROL Country] | Das Land, in dem die Gesellschaft zur Ausübung ihrer Tätigkeit eingetragen ist. |
| [!UICONTROL State Province] | Das Bundesland oder die Provinz, in dem das Unternehmen für die Geschäftstätigkeit registriert ist. |
| [!UICONTROL City] | Die Stadt, in der das Unternehmen für die Geschäftstätigkeit registriert ist. |
| [!UICONTROL Group/Shared Catalog] | Der Spaltenname hängt davon ab, ob der freigegebene Katalog in der Konfiguration aktiviert ist. Optionen: <br/>**[!UICONTROL Customer Group]**- Wenn der freigegebene Katalog in der Konfiguration nicht aktiviert ist, gibt den Namen der [Kundengruppe](../customers/customer-groups.md) dem das Unternehmen angehört.<br/>**[!UICONTROL Shared Catalog]** - Wenn der freigegebene Katalog in der Konfiguration aktiviert ist, gibt den Namen des freigegebenen Katalogs an, der dem Kunden zugewiesen ist. |
| [!UICONTROL Outstanding Balance] | Der ausstehende Saldo des Unternehmensabschlusses. die Spalte ist leer, wenn das Unternehmen keinen Kreditverlauf hat und sein Kreditlimit null ist. |
| [!UICONTROL Company Admin] | Der Vor- und Nachname des Unternehmensadministrators. |
| [!UICONTROL Job Title] | Die Berufsbezeichnung des Unternehmensadministrators. |
| [!UICONTROL Email] | Die E-Mail-Adresse des Unternehmensadministrators. |
| [!UICONTROL Action] | **[!UICONTROL Edit]** - Öffnet das Unternehmenskonto im Bearbeitungsmodus. |

{style="table-layout:auto"}

#### Zusätzliche Spalten

Die folgenden Spalten können durch Ändern der [Spaltenlayout](../getting-started/admin-grid-controls.md) des Rasters.

| Spalte | Beschreibung |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company Legal Name] | Der vollständige rechtsgültige Name des Unternehmens. |
| [!UICONTROL Street Address] | Die Straßenadresse, unter der die Gesellschaft für die Geschäftstätigkeit registriert ist. |
| [!UICONTROL ZIP] | Postleitzahl, unter der das Unternehmen für die Geschäftstätigkeit registriert ist. |
| [!UICONTROL Reseller ID] | Die Wiederverkaufsnummer, die dem Unternehmen für Steuerberichterstattungszwecke zugewiesen wird. |
| [!UICONTROL VAT/TAX ID] | Die [Mehrwertsteuer](../stores-purchase/vat.md) Nummer, die dem Unternehmen von einigen Rechtsgebieten für Steuerberichterstattungszwecke zugewiesen wird. Informationen zum Konfigurieren der Mehrwertsteuer-/TAX-ID des Kunden, die in der Storefront angezeigt wird, finden Sie unter [Neue Kontooptionen erstellen](../configuration-reference/customers/customer-configuration.md). |
| [!UICONTROL Credit Limit] | Die Kreditbeschränkung, die auf das Unternehmenskonto erweitert wird. |
| [!UICONTROL Credit Currency] | Die Währung, die vom Store für Käufe auf Firmenkredite akzeptiert wird. |
| [!UICONTROL Status] | Gibt die [status](account-company-approve.md) des Unternehmenskontos. Optionen: <br/>**[!UICONTROL Active]**- Das Unternehmenskonto wird vom Store-Administrator genehmigt. Der Unternehmensadministrator und die zugehörigen Mitglieder können sich über die Storefront bei dem Konto anmelden und Käufe tätigen.<br/>**[!UICONTROL Pending Approval]** - Eine Anfrage zum Öffnen eines Unternehmenskontos wurde eingereicht, aber noch nicht vom Store-Administrator genehmigt. <br/>**[!UICONTROL Rejected]**- Eine Anfrage zum Öffnen eines Unternehmenskontos wurde gesendet, aber vom Store-Administrator nicht genehmigt. Die ursprünglichen Anmeldedaten, die zum Senden der Anfrage verwendet wurden, werden blockiert.<br/>**[!UICONTROL Blocked]** - Die Mitglieder des Unternehmens können sich anmelden und auf den Katalog zugreifen, jedoch keine Käufe tätigen. Der Store-Administrator blockiert möglicherweise ein Unternehmenskonto, das nicht gut aufgestellt ist. Der Block auf dem Konto kann vom Store-Administrator jederzeit entfernt werden. |
| [!UICONTROL Gender] | Das Geschlecht des Unternehmensadministrators. Optionen: Männlich/Weiblich/nicht angegeben |
| [!UICONTROL Comment] | Hinweise zum Unternehmenskonto als Referenz und nur vom Administrator sichtbar. |

{style="table-layout:auto"}

### Schaltflächenleiste

| Schaltfläche | Beschreibung |
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Back] | Kehrt zur Seite &quot;Unternehmen&quot;zurück, ohne Änderungen zu speichern. |
| [!UICONTROL Login as Customer] | Ermöglicht es einem Admin-Benutzer, [Melden Sie sich als Kunde bei der Storefront an](../customers/login-as-customer.md) und helfen bei ihren Bestellungen. |
| [!DNL Delete Company] | Löscht das Unternehmenskonto. Der Status der Benutzerkonten, die mit dem Unternehmen verknüpft sind, wird auf `Inactive` und die Firmen-ID aus den Profilen der Benutzerkonten entfernt wird. Informationen über Unternehmenstätigkeiten und Transaktionen werden im System gespeichert. |
| [!DNL Reset] | Stellt die ursprünglichen Werte in allen Feldern mit nicht gespeicherten Änderungen wieder her. |
| [!DNL Reimburse Balance] | Ermöglicht dem Administrator die Rückzahlung des Restbetrags aus dem Transaktionsnachweis, referenziert durch die Bestellnummer. |
| [!DNL Save] | Speichert Änderungen am Unternehmen und behält das Profil bei. |
| [!UICONTROL Save & Close] | Speichert Änderungen am Unternehmen und schließt das Profil. |

{style="table-layout:auto"}

### Feldbeschreibungen

| Feld | Beschreibung |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company Name] | Der Unternehmensname wird bei der ersten Erstellung des Unternehmenskontos angegeben und kann eine gekürzte Version des vollständigen rechtlichen Namens sein. |
| [!UICONTROL Status] | Gibt die [status](account-company-approve.md) des Unternehmenskontos. Optionen: <br/>**[!UICONTROL Active]**- Das Unternehmenskonto wird vom Store-Administrator genehmigt. Der Unternehmensadministrator und die zugehörigen Mitglieder können sich über die Storefront bei dem Konto anmelden und Käufe tätigen.<br/>**[!UICONTROL Pending Approval]** - Eine Anfrage zum Öffnen eines Unternehmenskontos wurde eingereicht, aber noch nicht vom Store-Administrator genehmigt. <br/>**[!UICONTROL Rejected]**- Eine Anfrage zum Öffnen eines Unternehmenskontos wurde gesendet, aber vom Store-Administrator nicht genehmigt. Die ursprünglichen Anmeldedaten, die zum Senden der Anfrage verwendet wurden, werden blockiert.<br/>**[!UICONTROL Blocked]** - Die Mitglieder des Unternehmens können sich anmelden und auf den Katalog zugreifen, jedoch keine Käufe tätigen. Der Store-Administrator blockiert möglicherweise ein Unternehmenskonto, das nicht gut aufgestellt ist. Der Block auf dem Konto kann vom Store-Administrator jederzeit entfernt werden. |
| [!UICONTROL Company Email] | Die mit dem Unternehmenskonto verknüpfte E-Mail-Adresse. |
| [!UICONTROL Sales Representative] | Der Admin-Benutzer, der der Hauptkontakt für das Unternehmenskonto ist. |

{style="table-layout:auto"}

#### [!UICONTROL Account Information]

| Feld | Beschreibung |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company Legal Name] | Der vollständige rechtsgültige Name des Unternehmens. |
| [!UICONTROL VAT / TAX ID] | die Steuer oder [Mehrwertsteuer](../stores-purchase/vat.md) Nummer, die dem Unternehmen zu Steuermeldezwecken zugewiesen wird. |
| [!UICONTROL Reseller ID] | Die Wiederverkaufsnummer, die dem Unternehmen für Steuerberichterstattungszwecke zugewiesen wird. |
| [!UICONTROL Comment] | Diese Hinweise zum Unternehmenskonto dienen nur als Referenz und sind nur vom Administrator sichtbar. |
| **[!UICONTROL Legal Address]** |                                                                                                                            |
| [!UICONTROL Street Address] | Die Straßenadresse, unter der die Gesellschaft für die Geschäftstätigkeit registriert ist. |
| [!UICONTROL City] | Die Stadt, in der das Unternehmen für die Geschäftstätigkeit registriert ist. |
| [!UICONTROL Country] | Das Land, in dem die Gesellschaft zur Ausübung ihrer Tätigkeit eingetragen ist. |
| [!UICONTROL State/Province] | Das Bundesland oder die Provinz, in dem das Unternehmen für die Geschäftstätigkeit registriert ist. |
| [!UICONTROL ZIP/Postal Code] | Postleitzahl, unter der das Unternehmen für die Geschäftstätigkeit registriert ist. |
| [!UICONTROL Phone Number] | Die primäre Telefonnummer des Unternehmens. |

{style="table-layout:auto"}

#### [!UICONTROL Company Hierarchy]

[!BADGE 1.5.0-Beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Nur für Beta-Programmteilnehmer verfügbar"}

| Spalten | Beschreibung |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company ID] | Die ID-Nummer des Unternehmens |
| [!UICONTROL Company Name] | Der vollständige Name des Unternehmens. <br/>A `current company indicator` in der sich in Bearbeitung befindenden Firmenzeile angezeigt. |
| [!UICONTROL Company Email] | Die mit dem Unternehmenskonto verknüpfte E-Mail-Adresse. |
| [!UICONTROL Phone Number] | Die primäre Telefonnummer des Unternehmens. |
| [!UICONTROL State/Province] | Das Bundesland oder die Provinz, in dem das Unternehmen für die Geschäftstätigkeit registriert ist. |
| [!UICONTROL City] | Die Stadt, in der das Unternehmen für die Geschäftstätigkeit registriert ist. |
| [!UICONTROL Customer Group] | (Nur Admin) Gibt die [Kundengruppe](../customers/customer-groups.md) oder [freigegebener Katalog](catalog-shared.md) , das dem Unternehmen zugewiesen ist. |
| [!UICONTROL Company Admin] | Der vollständige Name des Unternehmensadministrators. |
| [!UICONTROL Action] | Die Liste möglicher Aktionen für diese Unternehmenszeile. |

{style="table-layout:auto"}

#### [!UICONTROL Company Admin]

| Feld | Beschreibung |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Job Title] | Der Titel des Unternehmensadministrators, der das Unternehmenskonto verwaltet. |
| [!UICONTROL Email] | Die E-Mail-Adresse des Unternehmensadministrators kann mit der E-Mail-Adresse des Unternehmens übereinstimmen. Wenn eine andere E-Mail-Adresse angegeben wird, wird zusätzlich zum Unternehmenskonto ein eigenes Konto für den Unternehmensadministrator erstellt. |
| [!UICONTROL Prefix] | Gegebenenfalls das Präfix, das mit dem Namen des Unternehmensadministrators verknüpft ist (z. B. `Mr.`, `Ms.`, `Mrs.`oder `Dr.`). Je nach Konfiguration kann das Eingabefeld ein Textfeld oder eine Liste sein. |
| [!UICONTROL First Name] | Der Vorname des Unternehmensadministrators. |
| [!UICONTROL Middle Name/Initial] | Der Vorname oder die Initialname des Unternehmensadministrators. |
| [!UICONTROL Last Name] | Der Nachname des Unternehmensadministrators. |
| [!UICONTROL Suffix] | Gegebenenfalls das Suffix, das mit dem Namen des Unternehmensadministrators verknüpft ist (z. B. `Jr.`, `Sr.`oder `III`). Je nach Konfiguration kann das Eingabefeld ein Textfeld oder eine Liste sein. |
| [!UICONTROL Gender] | Das Geschlecht des Unternehmensadministrators. Optionen: `Male` / `Female` / `Not Specified` |

{style="table-layout:auto"}

#### [!UICONTROL Company Credit]

| Feld | Beschreibung |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Credit Currency] | Die Währung, die vom Store für Käufe auf Firmenkredite akzeptiert wird. |
| [!UICONTROL Credit Limit] | Die Kreditbeschränkung, die auf das Unternehmenskonto erweitert wird. |
| [!UICONTROL Allow to Exceed Credit Limit] | Gibt an, ob das Unternehmen berechtigt ist, die Kreditgrenze zu überschreiten. Optionen: Ja/Nein |
| [!UICONTROL Reason for Change] | Ein Hinweis, in dem die Umstände erläutert werden, unter denen das Unternehmen das Kreditlimit überschreiten kann oder nicht. Dieses Feld ist nur dann aktiv, wenn sich die Berechtigung zum Überschreiten des Kreditlimits ändert. |

{style="table-layout:auto"}

#### [!UICONTROL Advanced Settings]

| Feld | Beschreibung |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Customer Group] | Gibt die [Kundengruppe](../customers/customer-groups.md) oder [freigegebener Katalog](catalog-shared.md) , das dem Unternehmen zugewiesen ist. |
| [!UICONTROL Allow Quotes] | Bestimmt, ob die Mitglieder des Unternehmens verhandelbare Kurse im Namen des Unternehmens erstellen und einreichen können. |
| [!UICONTROL Enable Purchase Orders] | Bestimmt, ob Bestellung für das Unternehmen zulässig ist. Damit Bestellungen für Konten von Unternehmensmitgliedern funktionieren, muss der Unternehmensadministrator diese Funktion auch in der Storefront aktivieren. |
| [!UICONTROL Applicable Payment Methods] | Gibt die Zahlungsmethoden an, die für Unternehmenskäufe verfügbar sind. Optionen: `B2B Payment Methods` / `All Enabled Payment Methods` / `Specific Payment Methods` |
| [!UICONTROL Payment Methods] | (Nur Administrator) Wird aktiv, wenn bestimmte Zahlungsmethoden angegeben sind. Um mehrere Zahlungsmethoden auszuwählen, halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie auf jede Option. |

{style="table-layout:auto"}
