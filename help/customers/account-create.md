---
title: Erstellen eines individuellen Kundenkontos
description: Besucher können einfach ein individuelles Kundenkonto erstellen, um ihre Käufe zu verwalten.
exl-id: 8d08c0e1-f3ba-4423-98a7-ffa8ba5a1b8b
feature: Customers, Storefront
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '1246'
ht-degree: 0%

---

# Erstellen eines individuellen Kundenkontos

Besucher in Ihrem Geschäft können ein Konto öffnen, um ihre Käufe und Aktivitäten zu verwalten. Kunden erstellen in der Regel eigene Konten aus Ihrem Store. Sie können jedoch auch direkt über den Administrator Kundenkonten erstellen, was für die telefonische Unterstützung von Kunden nützlich ist.

Die folgenden Anweisungen stellen die standardmäßige Kundenkontokonfiguration dar. Informationen zum Ändern der Auswahl und des Verhaltens einiger Formularfelder finden Sie unter [Konfigurieren von Kundenkonten](../customers/customer-account-scope.md).

Als Store-Administrator können Sie auch die [Neue Kontooptionen](../customers/account-options-new.md) um eine Bestätigungs-E-Mail an neue registrierte Kunden zu senden, wodurch sichergestellt wird, dass registrierte Konten gültig sind.

{{beta-updates}}

## Konto aus der Storefront erstellen

Ein Store-Kunde erstellt ein Konto in der Storefront.

1. Klicken Sie in der Storefront auf **[!UICONTROL Create an Account]** in der oberen rechten Ecke der Kopfzeile.

   ![Konto erstellen](assets/storefront-create-an-account-link.png){width="700" zoomable="yes"}

1. under **[!UICONTROL Personal Information]**, gibt ihre **[!UICONTROL First Name]** und **[!UICONTROL Last Name]**.

   ![Persönliche Informationen](assets/storefront-create-account-personal-information.png){width="600" zoomable="yes"}

1. Wenn der Kunde seinen Namen und seine E-Mail-Adresse zur Liste der Newsletter-Abonnenten hinzufügen möchte, wählt er die **[!UICONTROL Sign Up for Newsletter]** aktivieren.

   >[!INFO]
   >
   > Diese Option wird auch dann angezeigt, wenn der Store keinen Newsletter veröffentlicht.

1. Wenn Support-Mitarbeiter [sehen, was sie sehen](../customers/login-as-customer.md) und Remote-Unterstützung bereitstellen, wählt der Kunde die **[!UICONTROL Allow remote shopping assistance]** aktivieren.

1. under **[!UICONTROL Sign-in Information]**, gibt ihre **[!UICONTROL Email]** Adresse.

   >[!INFO]
   >
   > Diese E-Mail-Adresse wird Teil ihrer Anmeldedaten und kann keinem anderen Kundenkonto zugeordnet werden.

   ![Anmeldeinformationen](assets/storefront-create-account-signin-information.png){width="600" zoomable="yes"}

1. Fügt eine **[!UICONTROL Password]** , die drei der folgenden Arten von Informationen umfasst:

   - Kleinbuchstaben
   - Großbuchstaben
   - Zahlen
   - Sonderzeichen

   Nach dem Drücken **[!UICONTROL Enter]**, wird die Stärke des Kennworts ausgewertet und unter dem Feld angezeigt. Wenn das Kennwort als _Schwach_ versuchen Sie es mit einem anderen , bis es als _Stark_.

   ![Ein sicheres Kennwort wird empfohlen](assets/storefront-customer-account-create-password-strong.png){width="600" zoomable="yes"}

1. Anschließend gibt der Kunde ihn erneut in **[!UICONTROL Confirm Password]**.

1. Klicks, falls erforderlich **[!UICONTROL Show Password]** um das eingegebene Kennwort anzuzeigen.

1. Klicken Sie nach Abschluss **Konto erstellen**.

Der Kunde kann dann seine E-Mail-Adresse und sein Passwort für [Anmelden](../customers/customer-sign-in.md) auf ihr Konto zugreifen und die Adressdaten ausfüllen.

## Konto vom Administrator erstellen

Als Händler können Sie über den Administrator ein Kundenkonto erstellen.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Klicken **[!UICONTROL Add New Customer]**.

### Schritt 1: Kontoinformationen ausfüllen

![Kundeninformationen](assets/new-information.png){width="700" zoomable="yes"}

1. Im **[!UICONTROL Account Information]** führen Sie folgende Schritte aus:

   - Für eine Multisite-Installation legen Sie **[!UICONTROL Associate to Website]** auf die Website, auf die sich das Kundenkonto bezieht.
   - Weisen Sie den Kunden gegebenenfalls einer anderen **[!UICONTROL Customer Group]**.
   - Wenn Sie [Validierung der MwSt-ID](../stores-purchase/vat.md) und möchten **[!UICONTROL Disable Automatic Group Change Based on VAT ID]**, aktivieren Sie das Kontrollkästchen.

1. Füllen Sie die erforderlichen Felder aus:

   - **[!UICONTROL First Name]**
   - **[!UICONTROL Last Name]**
   - **[!UICONTROL Email]**

1. Füllen Sie die optionalen Felder nach Bedarf aus:

   - **[!UICONTROL Name Prefix]**
   - **[!UICONTROL Middle Name/Initial]**
   - **[!UICONTROL Name Suffix]**
   - **[!UICONTROL Date of Birth]**
   - **[!UICONTROL Tax/VAT Number]**
   - **[!UICONTROL Gender]**

   >[!WARNING]
   >
   >Beachten Sie im Einklang mit den aktuellen Best Practices für Sicherheit und Datenschutz alle potenziellen rechtlichen und sicherheitstechnischen Risiken, die mit der Speicherung des vollständigen Geburtsdatums (Monat, Tag, Jahr) der Kunden mit anderen persönlichen Identifikatoren verbunden sind. Es wird empfohlen, die Speicherung der vollständigen Geburtsdaten der Kunden zu begrenzen und als Alternative das Geburtsjahr des Kunden zu verwenden.

1. Satz **[!UICONTROL Send Welcome Email From]** in die Store-Ansicht, von der aus die _Willkommen_ E-Mail zu senden.

   >[!INFO]
   >
   > Wenn der Store Ansichten für verschiedene [languages](../stores-purchase/store-localize.md)festgelegt ist, bestimmt diese Einstellung die Sprache der Begrüßungs-E-Mail.

1. Klicks **[!UICONTROL Save and Continue Edit]** oben auf der Seite.

   >[!INFO]
   >
   >Nachdem das Kundenkonto gespeichert wurde, wird der vollständige Satz der Optionen im linken Bereich und im Menü oben auf der Seite angezeigt. Die _[!UICONTROL Customer View]_zeigt eine Zusammenfassung des Kontos an.

   ![Kundenansicht](assets/customer-account-create-saved.png){width="600" zoomable="yes"}

### Schritt 2: Adressdaten ausfüllen

1. Wählen Sie im linken Bereich die Option **[!UICONTROL Addresses]** und klicken **[!UICONTROL Add New Addresses]**.

1. Wenn dieselbe Adresse sowohl für die Abrechnung als auch für den Versand verwendet wird, können Sie beide Optionen aktivieren.

   - **[!UICONTROL Default Billing Address]**
   - **[!UICONTROL Default Shipping Address]**

   ![Hinzufügen von Kundenadressinformationen](assets/information-addresses.png){width="600" zoomable="yes"}

1. Scrollen Sie nach unten und füllen Sie die erforderlichen Adressfelder in der zweiten Spalte aus.

   - **[!UICONTROL Street Address]**
   - **[!UICONTROL City]**
   - **[!UICONTROL Country]**
   - **[!UICONTROL State/Province]**
   - **[!UICONTROL ZIP/Postal Code]**

1. Geben Sie die **[!UICONTROL Phone Number]** für diese Adresse.

1. Geben Sie gegebenenfalls die **[!UICONTROL VAT Number]** mit dem Kunden verknüpft sind.

1. Wenn diese Adresse die einzige für das Konto benötigte Adresse ist, klicken Sie auf **[!UICONTROL Save]**.

   Klicken Sie andernfalls auf **[!UICONTROL Save and Continue Edit]** und wiederholen Sie die vorherigen Schritte, um zusätzliche Adressen hinzuzufügen.

   Die neue Adresse wird im [!UICONTROL Addresses] Seite mit der ausgewählten _[!UICONTROL Default Billing]_und_[!UICONTROL Default Shipping]_ Adressen oberhalb der vollständigen Liste.

   ![Adressenansicht](assets/address-list.png){width="600" zoomable="yes"}

### Schritt 3: Kennwort zurücksetzen

Kundenkonten, die vom Administrator erstellt wurden, verfügen zunächst nicht über zugewiesene Passwörter.

1. Suchen Sie das neue Kundenkonto im Raster.

1. Klicks **[!UICONTROL Edit]** im _[!UICONTROL Action]_Spalte.

1. Klicken Sie in der Menüleiste oben auf der Seite auf **[!UICONTROL Reset Password]**.

1. Dem Kontoinhaber wird eine Benachrichtigung mit Anweisungen zum Festlegen des Kennworts gesendet.

## Schaltflächenleiste

Zusätzliche Schaltflächen werden verfügbar, wenn das Profil zum ersten Mal gespeichert wird. Weitere Informationen finden Sie unter [Kundenprofil aktualisieren](../customers/update-account.md).

| Schaltfläche | Beschreibung |
|--- |--- |
| **[!UICONTROL Back]** | Gibt Folgendes zurück _[!UICONTROL Customers]_Seite ohne Speichern von Änderungen. |
| **[!UICONTROL Delete Customer]** | Löscht den aktuellen Kunden. Abgeschlossene Bestellungen, die dem Kunden zugeordnet sind, werden nicht entfernt. |
| **[!UICONTROL Reset]** | Setzt nicht gespeicherte Änderungen im Kundenformular auf die vorherigen Werte zurück. |
| **[!UICONTROL Create Order]** | Erstellt eine Bestellung für den Kunden. |
| **[!UICONTROL Reset Password]** | Sendet eine [Kennwort zurücksetzen](../customers/password-reset.md) per E-Mail zu dem Kunden verlinken. |
| **[!UICONTROL Force Sign-in]** | Ruft die OAuth-Zugriffstoken auf, die mit dem Kundenkonto verknüpft sind. Diese Funktion kann nur mit Kundenkonten verwendet werden, denen OAuth-Token als Teil einer Web-API zugewiesen wurden. [Integration](../systems/integrations.md). Weitere Informationen finden Sie unter [OAuth-basierte Authentifizierung](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/) in der Entwicklerdokumentation. |
| **[!UICONTROL Manage Shopping Cart]** | Ermöglicht dem Administrator, den Warenkorb für den Kunden zu verwalten. |
| **[!UICONTROL Save and Continue Edit]** | Speichert Änderungen und hält das Kundenprofil offen. |
| **[!UICONTROL Save Customer]** | Speichert Änderungen und schließt das Kundenprofil. |

{style="table-layout:auto"}

## Feldbeschreibungen

### [!UICONTROL Account Information]

| Feld | Beschreibung |
|--- |--- |
| **[!UICONTROL Associate to Website]** | Identifiziert die mit dem Kundenkonto verknüpfte Website. |
| **[!UICONTROL Group]** | Identifiziert die [Kundengruppe](../customers/customer-groups.md) wobei der Kunde Mitglied ist. Aktivieren Sie ggf. das Kontrollkästchen, um die automatische Gruppenänderung basierend auf der Mehrwertsteuer zu deaktivieren. |
| **[!UICONTROL Name Prefix]** | Wenn verwendet, das Präfix, das mit dem Namen des Kunden verknüpft ist (z. B. Herr, Frau oder Dr.). Die Präfixwerte werden durch die [Konfiguration](../configuration-reference/customers/customer-configuration.md). Je nach Konfiguration kann das Eingabefeld ein Textfeld oder eine Liste von Optionen sein. |
| **[!UICONTROL First Name]** | Der Vorname des Kunden. |
| **[!UICONTROL Middle Name / Initial]** | Der Vorname oder der Anfangs-Name des Kunden. Dieses Feld wird nur eingeschlossen, wenn es im [Konfiguration](../configuration-reference/customers/customer-configuration.md) Thema. |
| **[!UICONTROL Last Name]** | Der Nachname des Kunden. |
| **[!UICONTROL Name Suffix]** | Bei Verwendung das Suffix, das mit dem Kundennamen verknüpft ist (z. B. Jr., Sr. oder III). Die Suffix-Werte werden durch die [Konfiguration](../configuration-reference/customers/customer-configuration.md). Je nach Konfiguration kann das Eingabefeld ein Textfeld oder eine Dropdown-Liste mit Optionen sein. |
| **[!UICONTROL Email]** | Die E-Mail-Adresse des Kunden. |
| **[!UICONTROL Date of Birth]** | Das Geburtsdatum des Kunden. Das Geburtsdatum ist enthalten, sofern in der Variablen [Konfiguration](../configuration-reference/customers/customer-configuration.md) Thema. <br><br>Beachten Sie im Einklang mit den aktuellen Best Practices für Sicherheit und Datenschutz alle potenziellen rechtlichen und sicherheitstechnischen Risiken, die mit der Speicherung des vollständigen Geburtsdatums (Monat, Tag, Jahr) der Kunden mit anderen persönlichen Identifikatoren verbunden sind. Es wird empfohlen, die Speicherung der vollständigen Geburtsdaten der Kunden zu begrenzen und stattdessen das Geburtsjahr des Kunden zu verwenden. |
| **[!UICONTROL Tax / VAT Number]** | Die Steuer- oder Umsatzsteuer-Nummer des Kunden, falls zutreffend. |
| **[!UICONTROL Gender]** | Identifiziert das Geschlecht des Kunden. Das Geschlecht ist enthalten, wenn es in der Variablen [Konfiguration](../configuration-reference/customers/customer-configuration.md). Optionen: `Male` / `Female` / `Not Specified` |
| **[!UICONTROL Send Welcome Email From]** | Wenn Sie mehrere Store-Ansichten haben, gibt diese Einstellung die Store-Ansicht an, von der die Willkommensnachricht gesendet wird. Wenn Store-Ansichten für verschiedene Sprachen verwendet werden, bestimmt diese Einstellung die Sprache der Begrüßungs-E-Mail. |

### [!UICONTROL Addresses]

| Feld | Beschreibung |
|--- |--- |
| **[!UICONTROL New Addresses]** | Gibt den Typ der neuen Adresse an. Optionen: `Default Billing Address` / `Default Shipping Address` |
| **[!UICONTROL Add New Addresses]** | Zeigt einen weiteren Abschnitt Neue Adresse an, um den Typ der einzugebenden Adresse zu identifizieren. |
| **[!UICONTROL Company]** | Der Name des Unternehmens, falls für diese Adresse zutreffend. |
| **[!UICONTROL Street Address]** | Die Straßenadresse des Kunden. Eine zweite Adresszeile der Straße ist verfügbar, sofern im Feld [Konfiguration](../configuration-reference/customers/customer-configuration.md) Thema. |
| **[!UICONTROL City]** | Die Stadt, in der sich die Kundenadresse befindet. |
| **[!UICONTROL Country]** | Das Land, in dem sich die Kundenadresse befindet. |
| **[!UICONTROL State/Province]** | Das Bundesland oder die Provinz, in dem sich die Kundenadresse befindet. |
| **[!UICONTROL Zip/Postal Code]** | Die Postleitzahl, unter der sich die Kundenadresse befindet. |
| **[!UICONTROL Phone Number]** | Die Telefonnummer des Kunden, die mit der Adresse verknüpft ist. |
| **[!UICONTROL VAT Number]** | Gegebenenfalls die Mehrwertsteuer-Nummer, die für den Kunden an dieser Adresse gilt. |
