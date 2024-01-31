---
title: Unternehmenskonto erstellen
description: Erfahren Sie mehr über die Erstellung von Unternehmenskonten in der Adobe Commerce-Admin- und -Storefront.
exl-id: 8c06395b-102b-4a41-8eb3-e6a344feac70
feature: B2B, Companies, Configuration, Storefront
role: Admin, User
source-git-commit: 582f15c422e43af9acec6313c7b777b3126030f8
workflow-type: tm+mt
source-wordcount: '1784'
ht-degree: 0%

---

# Unternehmenskonto erstellen

Unternehmenskonten können vom Store oder vom Administrator eingerichtet werden. Alle Anforderungen zum Erstellen eines Unternehmenskontos müssen vom Store-Administrator genehmigt werden, bevor das Konto aktiv wird.

Der Person, die ein Unternehmenskonto über die Storefront erstellt, wird eine Rolle als [Unternehmensadministrator](account-company-admin.md). Nachdem die Anfrage zur Erstellung eines Unternehmenskontos genehmigt wurde, kann der Unternehmensadministrator ein Kontokennwort festlegen und sich bei dem Konto anmelden.

## Methode 1: Der Kunde erstellt das Konto über die Storefront

>[!IMPORTANT]
>
>Um diese Methode zu unterstützen (sodass Kunden ihr Unternehmen über die Storefront registrieren können), stellen Sie sicher, dass die Variable [B2B-Funktionen](enable-basic-features.md) so konfiguriert werden, dass **[!UICONTROL Allow Company Registration from the Storefront]** auf `Yes`.

1. In der oberen rechten Ecke der Storefront-Kopfzeile klickt der Kunde auf **[!UICONTROL Create an Account]** und wählt **[!UICONTROL Create New Company Account]**.

   ![Neues Unternehmenskonto erstellen](./assets/company-account-create-storefront-options.png){width="700" zoomable="yes"}

   >[!NOTE]
   >
   >Wenn ein Besucher bei einem registrierten Benutzerkonto angemeldet ist, kann er ein Unternehmenskonto erstellen, indem er zu _[!UICONTROL Customer Profile]_>**[!UICONTROL Company Structure]**>**[!UICONTROL Create a Company Account]**. Bei Erstellung des Unternehmenskontos wird das Kundenkonto als Hauptkontakt zugewiesen. Andernfalls erstellt das System einen Kunden, der eine E-Mail erhält, um ein Kennwort festzulegen.

1. Im _[!UICONTROL Company Information]_-Abschnitt, führt der Kunde Folgendes aus:

   - Fügt die erforderlichen Felder aus:

      - **[!UICONTROL Company Name]**
      - **[!UICONTROL Company Email]**

   - Fügt die übrigen Felder ggf. aus:

      - **[!UICONTROL Company Legal Name]**
      - **[!UICONTROL VAT/TAX ID]**
      - **[!UICONTROL Reseller ID]**

   ![Unternehmensinformationen](./assets/company-information-storefront.png){width="700" zoomable="yes"}

1. Fügt die erforderlichen Felder im _[!UICONTROL Legal Address]_Abschnitt.

   - **[!UICONTROL Street Address]**
   - **[!UICONTROL City]**
   - **[!UICONTROL Country]**
   - **[!UICONTROL State/Province]**
   - **[!UICONTROL ZIP/Postal Code]**
   - **[!UICONTROL Phone Number]**

   ![Anschrift](./assets/company-legal-address-storefront.png){width="700" zoomable="yes"}

1. Im _[!UICONTROL Company Administrator]_führt Folgendes aus:

   - Fügt die **[!UICONTROL Email address]** für den Unternehmensadministrator.

     Die E-Mail-Adresse für den Unternehmensadministrator kann mit der E-Mail-Adresse des Unternehmens oder einer anderen E-Mail-Adresse übereinstimmen. Wenn eine andere E-Mail-Adresse angegeben wird, wird zusätzlich zum Administratorkonto des Unternehmens ein Unternehmensbenutzerkonto erstellt.

   - Fügt die **[!UICONTROL First Name]** und **[!UICONTROL Last Name]** des Unternehmensadministrators.

   - Fügt optional die folgenden Felder aus:

      - **[!UICONTROL Job Title]**
      - **[!UICONTROL Gender]**

   ![Unternehmensadministrator](./assets/company-administrator-account-storefront.png)

1. Schließt die Validierung ab, wenn reCAPTCHA für diese Storefront-Funktion aktiviert ist.

1. Wenn die Informationen vollständig sind, wählen Sie **[!UICONTROL Submit]**.

   Wenn die Anfrage zur Erstellung eines Unternehmenskontos vom Händler genehmigt wird, wird die E-Mail-Benachrichtigung an den Unternehmensadministrator gesendet.

   ![Beispiel für eine Begrüßungs-E-Mail](./assets/company-admin-welcome-email.png){width="500"}

   Wenn das Kennwort festgelegt ist, kann der Unternehmensadministrator [Anmelden](../customers/customer-sign-in.md) auf das Konto zu.

## Methode 2: Der Händler erstellt das Konto vom Administrator

Der Prozess der Erstellung eines Unternehmens über den Administrator ist im Wesentlichen identisch mit dem der Storefront, jedoch mit zusätzlichen Feldern.

![Hinzufügen eines neuen Unternehmens über den Administrator](./assets/company-add-new.png){width="700" zoomable="yes"}

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Klicks **[!UICONTROL Add New Company]** und gehen Sie wie folgt vor:

   - Füllen Sie diese erforderlichen Felder aus:

      - **[!UICONTROL Company Name]**
      - **[!UICONTROL Company Email]**

   - Wenn Sie nicht bereit sind, das Konto zu aktivieren, legen Sie **[!UICONTROL Status]** nach `Pending Approval`. (Festlegen auf `Active` standardmäßig verwendet.)

   - Wählen Sie gegebenenfalls das Admin-Konto der **[!UICONTROL Sales Representative]** der das Konto verwalten soll.

1. Im _[!UICONTROL Account Information]_führen Sie folgende Schritte aus:

   - Füllen Sie je nach Bedarf die folgenden Felder aus:

      - **[!UICONTROL Company Legal Name]**
      - **[!UICONTROL VAT/TAX ID]**
      - **[!UICONTROL Reseller ID]**

   - Für **[!UICONTROL Comment]** Geben Sie zusätzliche Informationen zum Kunden ein, die möglicherweise benötigt werden.

     Die Kommentare sind nur vom Administrator sichtbar.

   ![Kontoinformationen](./assets/company-create-account-information-admin.png){width="700" zoomable="yes"}

1. Bei der ersten Erstellung des Unternehmens muss die Variable _[!UICONTROL Company Hierarchy]_grid ist leer, wenn Sie es erweitern. Nachdem Sie das Unternehmen gespeichert haben, können Sie es in eine Unternehmenshierarchie aufnehmen. Siehe [Unternehmensverwaltung](manage-companies.md).

1. Im _[!UICONTROL Legal Address]_diese erforderlichen Felder auszufüllen:

   - **[!UICONTROL Street Address]**
   - **[!UICONTROL City Country]**
   - **[!UICONTROL ZIP/Postal Code]**
   - **[!UICONTROL Phone Number]**

1. Im _[!UICONTROL Company Admin]_führen Sie folgende Schritte aus:

   - Füllen Sie diese erforderlichen Felder aus:

      - **[!UICONTROL Email]**
      - **[!UICONTROL First Name]**
      - **[!UICONTROL Last Name]**

   - Füllen Sie die folgenden optionalen Teile des Namens aus, die möglicherweise für einige Kundennamen häufiger als andere gelten und nach Ihrem Ermessen verwendet werden können:

      - **[!UICONTROL Prefix]**
      - **[!UICONTROL Middle Name/Initial]**
      - **[!UICONTROL Suffix]**

   - Wenn die Informationen verfügbar sind, füllen Sie die übrigen Felder aus, um den Unternehmensadministrator zu beschreiben:

      - **[!UICONTROL Website]**
      - **[!UICONTROL Job Title]**
      - **[!UICONTROL Gender]**
      - **[!UICONTROL Send Welcome Email From]**

   ![Unternehmensadministrator](./assets/company-create-company-admin.png){width="700" zoomable="yes"}

1. Im _[!UICONTROL Company Credit]_-Abschnitt, der eine Zusammenfassung der Kundenkreditaktivität anzeigt, so viele Felder im unteren Teil des Abschnitts wie möglich ausfüllen:

   - **[!UICONTROL Credit Currency]**
   - **[!UICONTROL Credit Limit]**
   - **[!UICONTROL Allow to Exceed Credit Limit]**
   - **[!UICONTROL Reason for Change]**

   ![Firmenguthaben](./assets/company-create-credit-admin.png){width="700" zoomable="yes"}

1. Im _[!UICONTROL Advanced Settings]_führen Sie folgende Schritte aus:

   >[!NOTE]
   >
   >Die Kundengruppenzuweisung bestimmt, welcher freigegebene Katalog für das Unternehmen und seine Mitarbeiter verfügbar ist. Standardmäßig wird das Unternehmen der Kundengruppe zugewiesen, die in der Konfiguration als Standard festgelegt ist.

   - Sie können die **[!UICONTROL Customer Group]** Zuweisung des Unternehmens und seiner Mitarbeiter zu einer Gruppe, die Zugriff auf einen anderen freigegebenen Katalog hat, oder zu einer standardmäßigen Kundengruppe. Sie werden aufgefordert, dies zu bestätigen, bevor die Gruppe geändert wird.

     ![Ändern der Kundengruppe](./assets/company-advanced-settings-customer-group-admin.png){width="600"}

   - Wenn Sie es Firmenmitarbeitern ermöglichen möchten, Anführungszeichen aus ihrem Konto zu erstellen, legen Sie **[!UICONTROL Allow Quotes]** nach `Yes`.

   - Wenn Sie es Firmenmitarbeitern ermöglichen möchten, Bestellungen über ihr Konto zu erstellen und zu verwenden, legen Sie **[!UICONTROL Enable Purchase Orders]** nach `Yes`.

   - So ändern Sie die **[!UICONTROL Applicable Payment Methods]** die dem Unternehmen zur Verfügung stehen, löschen Sie die **[!UICONTROL Use config settings]** und wählen Sie eine der folgenden Optionen:

     | Option | Beschreibung |
     |-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
     | `B2B Payment Methods` | (Standard) Aktiviert alle [Als Standard festgelegte Zahlungsmethoden](../configuration-reference/general/b2b-features.md#default-b2b-payment-methods) für B2B-Bestellungen. |
     | `All Enabled Payment Methods` | Macht alle [aktivierte Zahlungsmethoden](../configuration-reference/sales/payment-methods.md) für Kundenkonten verfügbar, die mit dem Unternehmenskonto verknüpft sind. |
     | `Selected Payment Methods` | Ermöglicht die Auswahl der Zahlungsmethoden, die für mit dem Unternehmenskonto verbundene Kundenkonten verfügbar sind. Um mehrere Zahlungsmethoden auszuwählen, halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und wählen Sie jede Option aus. |

     {style="table-layout:auto"}

   - So ändern Sie die **[!UICONTROL Applicable Shipping Methods]** die dem Unternehmen zur Verfügung stehen, löschen Sie die **[!UICONTROL Use config settings]** und wählen Sie eine der folgenden Optionen:

     | Option | Beschreibung |
     |--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
     | `B2B Shipping Methods` | (Standard) Aktiviert alle [Versandmethoden als Standard festgelegt](../configuration-reference/general/b2b-features.md#default-b2b-shipping-methods) für B2B-Bestellungen. |
     | `All Enabled Shipping Methods` | Macht alle [aktivierte Versandmethoden](../configuration-reference/sales/delivery-methods.md) für Kundenkonten verfügbar, die mit dem Unternehmenskonto verknüpft sind. |
     | `Selected Shipping Methods` | Ermöglicht die Auswahl der Versandmethoden, die für Kundenkonten verfügbar sind, die mit dem Unternehmenskonto verknüpft sind. Um mehrere Versandmethoden auszuwählen, halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und wählen Sie jede Option aus. |

     {style="table-layout:auto"}

1. Wählen Sie nach Abschluss **[!UICONTROL Save]**.

   Wenn die Anfrage zur Erstellung eines Unternehmenskontos vom Händler genehmigt wird, wird eine E-Mail-Benachrichtigung an die E-Mail-Adresse des Unternehmensadministrators gesendet.

   Wenn das Kennwort festgelegt ist, kann der Unternehmensadministrator [Anmelden](../customers/customer-sign-in.md) auf das Konto zu.

## Schaltflächenleiste

| Schaltfläche | Beschreibung |
|---------------------------|------------------------------------------------------------------|
| [!UICONTROL Back] | Kehrt zur Seite &quot;Unternehmen&quot;zurück, ohne Änderungen zu speichern. |
| [!UICONTROL Reset] | Stellt die ursprünglichen Werte in allen Feldern mit nicht gespeicherten Änderungen wieder her. |
| [!UICONTROL Save] | Speichert Änderungen am Unternehmen und behält das Profil bei. |
| [!UICONTROL Save & Close] | Speichert Änderungen am Unternehmen und schließt das Profil. |

{style="table-layout:auto"}

## Feldbeschreibungen

| Feld | Beschreibung |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company Name] | Der Unternehmensname wird bei der ersten Erstellung des Unternehmenskontos angegeben und kann eine gekürzte Version des vollständigen rechtlichen Namens sein. |
| [!UICONTROL Status] | (Nur Administrator) Gibt den aktuellen Status des Unternehmenskontos an. Optionen: <br/>**[!UICONTROL Active]**- Das Unternehmenskonto wird vom Store-Administrator genehmigt. Der Unternehmensadministrator und die zugehörigen Mitglieder können sich über die Storefront bei dem Konto anmelden und Käufe tätigen.<br/>**[!UICONTROL Pending Approval]** - Eine Anfrage zum Öffnen eines Unternehmenskontos wurde eingereicht, aber noch nicht vom Store-Administrator genehmigt. <br/>**[!UICONTROL Rejected]**- Eine Anfrage zum Öffnen eines Unternehmenskontos wurde gesendet, aber vom Store-Administrator nicht genehmigt. Die ursprünglichen Anmeldedaten, die zum Senden der Anfrage verwendet wurden, werden blockiert.<br/>** Blockierung **- Die Mitglieder des Unternehmens können sich anmelden und auf den Katalog zugreifen, jedoch keine Käufe tätigen. Der Store-Administrator blockiert möglicherweise ein Unternehmenskonto, das nicht gut aufgestellt ist. Der Block auf dem Konto kann vom Store-Administrator jederzeit entfernt werden. |
| [!UICONTROL Company Email] | Die mit dem Unternehmenskonto verknüpfte E-Mail-Adresse. |
| [!UICONTROL Sales Representative] | (Nur Admin) Der Admin-Benutzer, der der Hauptkontakt für das Unternehmenskonto ist. |

{style="table-layout:auto"}

### [!UICONTROL Account Information]

| Feld | Beschreibung |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company Legal Name] | Der vollständige rechtsgültige Name des Unternehmens. |
| [!UICONTROL VAT / TAX ID] | Die [Mehrwertsteuer](../stores-purchase/vat.md) Nummer, die dem Unternehmen von einigen Rechtsgebieten für Steuerberichterstattungszwecke zugewiesen wird. Informationen zum Konfigurieren der Mehrwertsteuer-/TAX-ID des Kunden, die in der Storefront angezeigt wird, finden Sie unter [Neue Kontooptionen erstellen](../configuration-reference/customers/customer-configuration.md). <br/> **_Hinweis:_** Der Unternehmensadministrator und andere Benutzer des Unternehmens verfügen nicht über eigene MwSt.-/TAX-ID-Nummern in ihren Kundenkonten. |
| [!UICONTROL Reseller ID] | Die Wiederverkaufsnummer, die dem Unternehmen für Steuerberichterstattungszwecke zugewiesen wird. |
| [!UICONTROL Comment] | (Nur Administrator) Diese Hinweise zum Unternehmenskonto dienen nur als Referenz und sind nur vom Administrator sichtbar. |

{style="table-layout:auto"}

### [!UICONTROL Company Hierarchy]

| Feld | Beschreibung |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company ID] | Die ID-Nummer des Unternehmens |
| [!UICONTROL Company Name] | Der vollständige Name des Unternehmens. <br/>A `current company indicator` in der sich in Bearbeitung befindenden Firmenzeile angezeigt. |
| [!UICONTROL Company Email] | Die mit dem Unternehmenskonto verknüpfte E-Mail-Adresse. |
| [!UICONTROL Phone Number] | Die primäre Telefonnummer des Unternehmens. |
| [!UICONTROL Country] | Das Land, in dem die Gesellschaft zur Ausübung ihrer Tätigkeit eingetragen ist. |
| [!UICONTROL State/Province] | Das Bundesland oder die Provinz, in dem das Unternehmen für die Geschäftstätigkeit registriert ist. |
| [!UICONTROL City] | Die Stadt, in der das Unternehmen für die Geschäftstätigkeit registriert ist. |
| [!UICONTROL Group/Shared Catalog] | (Nur Admin) Gibt die [Kundengruppe](../customers/customer-groups.md) oder [freigegebener Katalog](catalog-shared.md) , das dem Unternehmen zugewiesen ist. |
| [!UICONTROL Company Admin] | Der vollständige Name des Unternehmensadministrators. |
| [!UICONTROL Action] | Die Liste möglicher Aktionen für diese Unternehmenszeile. |

{style="table-layout:auto"}

### [!UICONTROL Legal Address]

| Feld | Beschreibung |
|------------------------------|-----------------------------------------------------------------------------|
| [!UICONTROL Street Address] | Die Straßenadresse, unter der die Gesellschaft für die Geschäftstätigkeit registriert ist. |
| [!UICONTROL City] | Die Stadt, in der das Unternehmen für die Geschäftstätigkeit registriert ist. |
| [!UICONTROL Country] | Das Land, in dem die Gesellschaft zur Ausübung ihrer Tätigkeit eingetragen ist. |
| [!UICONTROL State/Province] | Das Bundesland oder die Provinz, in dem das Unternehmen für die Geschäftstätigkeit registriert ist. |
| [!UICONTROL ZIP/Postal Code] | Postleitzahl, unter der das Unternehmen für die Geschäftstätigkeit registriert ist. |
| [!UICONTROL Phone Number] | Die primäre Telefonnummer des Unternehmens. |

{style="table-layout:auto"}

### [!UICONTROL Company Admin]

| Feld | Beschreibung |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Website] | Bestimmt die Website, zu der der Unternehmensadministrator gehört. |
| [!UICONTROL Job Title] | Der Titel des Unternehmensadministrators, der das Unternehmenskonto verwaltet. |
| [!UICONTROL Email] | Die E-Mail-Adresse des Unternehmensadministrators kann mit der E-Mail-Adresse des Unternehmens übereinstimmen. Wenn eine andere E-Mail-Adresse angegeben wird, wird zusätzlich zum Unternehmenskonto ein eigenes Konto für den Unternehmensadministrator erstellt. |
| [!UICONTROL Prefix] | Gegebenenfalls das Präfix, das mit dem Namen des Unternehmensadministrators verknüpft ist (z. B. `Mr.`, `Ms.`, `Mrs.`oder `Dr.`). Je nach Konfiguration kann das Eingabefeld ein Textfeld oder eine Liste sein. |
| [!UICONTROL First Name] | Der Vorname des Unternehmensadministrators. |
| [!UICONTROL Middle Name/Initial] | Der Vorname oder die Initialname des Unternehmensadministrators. |
| [!UICONTROL Last Name] | Der Nachname des Unternehmensadministrators. |
| [!UICONTROL Suffix] | Gegebenenfalls das Suffix, das mit dem Namen des Unternehmensadministrators verknüpft ist (z. B. `Jr.`, `Sr.`oder `III.`). Je nach Konfiguration kann das Eingabefeld ein Textfeld oder eine Liste sein. |
| [!UICONTROL Gender] | Das Geschlecht des Unternehmensadministrators. Optionen: `Male` / `Female` / `Not Specified` |
| [!UICONTROL Send Welcome Email From] | Die Store-Ansicht, von der die Willkommens-E-Mail gesendet werden soll. |

{style="table-layout:auto"}

### [!UICONTROL Company Credit]

| Feld | Beschreibung |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Credit Currency] | (Nur Administrator) Die Währung, die vom Store für Käufe auf Firmenkredite akzeptiert wird. |
| [!UICONTROL Credit Limit] | (Nur Administrator) Die Kreditbeschränkung, die auf das Unternehmenskonto erweitert wird. |
| [!UICONTROL Allow to Exceed Credit Limit] | (Nur Admin) Gibt an, ob das Unternehmen über die Berechtigung zum Überschreiten des Kreditlimits verfügt. Optionen: `Yes` / `No` |
| [!UICONTROL Reason for Change] | (Nur Administrator) Ein Hinweis, der erklärt, warum das Unternehmen die Kreditbeschränkung überschreiten darf oder nicht überschreiten darf. Dieses Feld ist nur dann aktiv, wenn sich die Berechtigung zum Überschreiten des Kreditlimits ändert. |

{style="table-layout:auto"}

### [!UICONTROL Advanced Settings]

| Feld | Beschreibung |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Customer Group] | (Nur Admin) Gibt die [Kundengruppe](../customers/customer-groups.md) oder [freigegebener Katalog](catalog-shared.md) , das dem Unternehmen zugewiesen ist. |
| [!UICONTROL Allow Quotes] | (Nur Administrator) Bestimmt, ob Unternehmensmitglieder im Namen des Unternehmens verhandelbare Kurse vorbereiten und einreichen können. |
| [!UICONTROL Enable Purchase Orders] | (Nur Administrator) Bestimmt, ob Unternehmensmitglieder Bestellungen als [Bestellaufträge](account-dashboard-my-purchase-orders.md) im Namen des Unternehmens. |
| Anwendbare Zahlungsmethoden | (Nur Administrator) Gibt die Zahlungsmethoden an, die für Unternehmenskäufe verfügbar sind. Optionen: `B2B Payment Methods` / `All Enabled Payment Methods` / `Selected Payment Methods` |
| [!UICONTROL Payment Methods] | (Nur Administrator) Wird aktiv, wenn bestimmte Zahlungsmethoden aktiviert sind. Um mehrere Zahlungsmethoden für das Unternehmenskonto verfügbar zu machen, halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und wählen Sie jede Option aus. |
| [!UICONTROL Applicable Shipping Methods] | (Nur Administrator) Gibt die Versandmethoden an, die für Unternehmenskäufe verfügbar sind. Optionen: `B2B Shipping Methods` / `All Enabled Shipping Methods` / `Selected Shipping Methods` |
| [!UICONTROL Shipping Methods] | (Nur Administrator) Wird aktiv, wenn bestimmte Versandmethoden aktiviert sind. Um mehrere Zahlungsmethoden für das Unternehmenskonto verfügbar zu machen, halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und wählen Sie jede Option aus. |

{style="table-layout:auto"}
