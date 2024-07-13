---
title: Erstellen eines individuellen Kundenkontos
description: Besucher können einfach ein individuelles Kundenkonto erstellen, um ihre Käufe zu verwalten.
exl-id: 8d08c0e1-f3ba-4423-98a7-ffa8ba5a1b8b
feature: Customers, Storefront
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '1268'
ht-degree: 0%

---

# Erstellen eines individuellen Kundenkontos

Besucher in Ihrem Geschäft können ein Konto öffnen, um ihre Käufe und Aktivitäten zu verwalten. Kunden erstellen in der Regel eigene Konten aus Ihrem Store. Sie können jedoch auch direkt über den Administrator Kundenkonten erstellen, was für die telefonische Unterstützung von Kunden nützlich ist.

Die folgenden Anweisungen stellen die standardmäßige Kundenkontokonfiguration dar. Informationen zum Ändern der Auswahl und des Verhaltens einiger Felder im Formular finden Sie unter [Konfigurieren von Kundenkonten](../customers/customer-account-scope.md).

Als Store-Administrator können Sie auch die [neuen Kontooptionen](../customers/account-options-new.md) festlegen, um eine Bestätigungs-E-Mail an neue registrierte Kunden zu senden. So können Sie sicherstellen, dass registrierte Konten gültig sind.

>[!NOTE]
>
>Ab Version 2.4.7 müssen Kunden ihre E-Mail-Adresse und ihr Kennwort erneut eingeben, um sich nach einer E-Mail-Bestätigung bei ihrem Konto anzumelden, unabhängig vom Browser.

## Konto aus der Storefront erstellen

Ein Store-Kunde erstellt ein Konto in der Storefront.

1. Klicken Sie in der Storefront auf **[!UICONTROL Create an Account]** in der oberen rechten Ecke der Kopfzeile.

   ![Erstellen eines Kontos](assets/storefront-create-an-account-link.png){width="700" zoomable="yes"}

1. Geben Sie unter **[!UICONTROL Personal Information]** ihre **[!UICONTROL First Name]** und **[!UICONTROL Last Name]** ein.

   ![Persönliche Informationen](assets/storefront-create-account-personal-information.png){width="600" zoomable="yes"}

1. Wenn der Kunde seinen Namen und seine E-Mail-Adresse zur Liste der Newsletter-Abonnenten hinzufügen möchte, aktiviert er das Kontrollkästchen **[!UICONTROL Sign Up for Newsletter]** .

   >[!INFO]
   >
   > Diese Option wird auch dann angezeigt, wenn der Store keinen Newsletter veröffentlicht.

1. Wenn die Support-Mitarbeiter des Stores [sehen sollen, was sie sehen](../customers/login-as-customer.md), und Remote-Unterstützung bereitstellen sollen, wählt der Kunde das Kontrollkästchen **[!UICONTROL Allow remote shopping assistance]** aus.

1. Geben Sie unter **[!UICONTROL Sign-in Information]** ihre **[!UICONTROL Email]**-Adresse ein.

   >[!INFO]
   >
   > Diese E-Mail-Adresse wird Teil ihrer Anmeldedaten und kann keinem anderen Kundenkonto zugeordnet werden.

   ![Anmeldeinformationen](assets/storefront-create-account-signin-information.png){width="600" zoomable="yes"}

1. Fügt einen **[!UICONTROL Password]** ein, der drei der folgenden Arten von Informationen enthält:

   - Kleinbuchstaben
   - Großbuchstaben
   - Zahlen
   - Sonderzeichen

   Nach dem Drücken von **[!UICONTROL Enter]** wird die Stärke des Kennworts ausgewertet und unter dem Feld angezeigt. Wenn das Kennwort als _schwach_ gilt, versuchen Sie es erneut, bis es als _stark_ ausgewertet wird.

   ![Ein sicheres Kennwort wird empfohlen](assets/storefront-customer-account-create-password-strong.png){width="600" zoomable="yes"}

1. Anschließend gibt der Kunde ihn erneut in **[!UICONTROL Confirm Password]** ein.

1. Klicken Sie bei Bedarf auf **[!UICONTROL Show Password]** , um das von Ihnen eingegebene Kennwort anzuzeigen.

1. Klicken Sie nach Abschluss des Vorgangs auf **Konto erstellen**.

Der Kunde kann dann seine E-Mail-Adresse und sein Passwort verwenden, um sich bei seinem Konto anzumelden und die Adressinformationen auszufüllen.[](../customers/customer-sign-in.md)

## Konto vom Administrator erstellen

Als Händler können Sie über den Administrator ein Kundenkonto erstellen.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. Klicken Sie auf **[!UICONTROL Add New Customer]**.

### Schritt 1: Kontoinformationen ausfüllen

![Kundeninformationen](assets/new-information.png){width="700" zoomable="yes"}

1. Gehen Sie im Abschnitt **[!UICONTROL Account Information]** wie folgt vor:

   - Bei einer Installation mit mehreren Sites setzen Sie **[!UICONTROL Associate to Website]** auf die Website, auf die das Kundenkonto angewendet wird.
   - Weisen Sie den Kunden gegebenenfalls eine andere **[!UICONTROL Customer Group]** zu.
   - Wenn Sie [Überprüfung der MwSt-ID](../stores-purchase/vat.md) verwenden und **[!UICONTROL Disable Automatic Group Change Based on VAT ID]** verwenden möchten, aktivieren Sie das Kontrollkästchen.

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

1. Setzen Sie **[!UICONTROL Send Welcome Email From]** auf die Store-Ansicht, von der die _Begrüßungs_-E-Mail gesendet werden soll.

   >[!INFO]
   >
   > Wenn der Store Ansichten für verschiedene [Sprachen](../stores-purchase/store-localize.md) enthält, bestimmt diese Einstellung die Sprache der Begrüßungs-E-Mail.

1. Klicken Sie oben auf der Seite auf **[!UICONTROL Save and Continue Edit]** .

   >[!INFO]
   >
   >Nachdem das Kundenkonto gespeichert wurde, wird der vollständige Satz der Optionen im linken Bereich und im Menü oben auf der Seite angezeigt. Auf der Registerkarte _[!UICONTROL Customer View]_wird eine Zusammenfassung des Kontos angezeigt.

   ![Kundenansicht](assets/customer-account-create-saved.png){width="600" zoomable="yes"}

### Schritt 2: Adressdaten ausfüllen

1. Wählen Sie im linken Bereich **[!UICONTROL Addresses]** und klicken Sie auf **[!UICONTROL Add New Addresses]**.

1. Wenn dieselbe Adresse sowohl für die Abrechnung als auch für den Versand verwendet wird, können Sie beide Optionen aktivieren.

   - **[!UICONTROL Default Billing Address]**
   - **[!UICONTROL Default Shipping Address]**

   ![Hinzufügen von Informationen zur Kundenadresse](assets/information-addresses.png){width="600" zoomable="yes"}

1. Scrollen Sie nach unten und füllen Sie die erforderlichen Adressfelder in der zweiten Spalte aus.

   - **[!UICONTROL Street Address]**
   - **[!UICONTROL City]**
   - **[!UICONTROL Country]**
   - **[!UICONTROL State/Province]**
   - **[!UICONTROL ZIP/Postal Code]**

1. Geben Sie den **[!UICONTROL Phone Number]** für diese Adresse ein.

1. Falls zutreffend, geben Sie den mit dem Kunden verknüpften **[!UICONTROL VAT Number]** ein.

1. Wenn diese Adresse die einzige für das Konto benötigte Adresse ist, klicken Sie auf **[!UICONTROL Save]**.

   Klicken Sie andernfalls auf **[!UICONTROL Save and Continue Edit]** und wiederholen Sie die vorherigen Schritte, um weitere Adressen hinzuzufügen.

   Die neue Adresse wird auf der Seite [!UICONTROL Addresses] mit den ausgewählten Adressen _[!UICONTROL Default Billing]_und_[!UICONTROL Default Shipping]_ oberhalb der vollständigen Liste angezeigt.

   ![Adressansicht](assets/address-list.png){width="600" zoomable="yes"}

### Schritt 3: Kennwort zurücksetzen

Kundenkonten, die vom Administrator erstellt wurden, verfügen zunächst nicht über zugewiesene Passwörter.

1. Suchen Sie das neue Kundenkonto im Raster.

1. Klicken Sie in der Spalte _[!UICONTROL Action]_auf **[!UICONTROL Edit]**.

1. Klicken Sie in der Menüleiste oben auf der Seite auf **[!UICONTROL Reset Password]**.

1. Dem Kontoinhaber wird eine Benachrichtigung mit Anweisungen zum Festlegen des Kennworts gesendet.

## Schaltflächenleiste

Zusätzliche Schaltflächen werden verfügbar, wenn das Profil zum ersten Mal gespeichert wird. Weitere Informationen finden Sie unter [Aktualisieren eines Kundenprofils](../customers/update-account.md).

| Schaltfläche | Beschreibung |
|--- |--- |
| **[!UICONTROL Back]** | Kehrt zur Seite _[!UICONTROL Customers]_zurück, ohne die Änderungen zu speichern. |
| **[!UICONTROL Delete Customer]** | Löscht den aktuellen Kunden. Abgeschlossene Bestellungen, die dem Kunden zugeordnet sind, werden nicht entfernt. |
| **[!UICONTROL Reset]** | Setzt nicht gespeicherte Änderungen im Kundenformular auf die vorherigen Werte zurück. |
| **[!UICONTROL Create Order]** | Erstellt eine Bestellung für den Kunden. |
| **[!UICONTROL Reset Password]** | Sendet per E-Mail einen Link &quot;[Kennwort zurücksetzen](../customers/password-reset.md)&quot; an den Kunden. |
| **[!UICONTROL Force Sign-in]** | Ruft die OAuth-Zugriffstoken auf, die mit dem Kundenkonto verknüpft sind. Diese Funktion kann nur mit Kundenkonten verwendet werden, denen OAuth-Token als Teil einer Web-API [integration](../systems/integrations.md) zugewiesen wurden. Weitere Informationen finden Sie unter [OAuth-basierte Authentifizierung](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/) in der Entwicklerdokumentation. |
| **[!UICONTROL Manage Shopping Cart]** | Ermöglicht dem Administrator, den Warenkorb für den Kunden zu verwalten. |
| **[!UICONTROL Save and Continue Edit]** | Speichert Änderungen und hält das Kundenprofil offen. |
| **[!UICONTROL Save Customer]** | Speichert Änderungen und schließt das Kundenprofil. |

{style="table-layout:auto"}

## Feldbeschreibungen

### [!UICONTROL Account Information]

| Feld | Beschreibung |
|--- |--- |
| **[!UICONTROL Associate to Website]** | Identifiziert die mit dem Kundenkonto verknüpfte Website. |
| **[!UICONTROL Group]** | Identifiziert die [Kundengruppe](../customers/customer-groups.md), der der Kunde angehört. Aktivieren Sie ggf. das Kontrollkästchen, um die automatische Gruppenänderung basierend auf der Mehrwertsteuer zu deaktivieren. |
| **[!UICONTROL Name Prefix]** | Wenn verwendet, das Präfix, das mit dem Namen des Kunden verknüpft ist (z. B. Herr, Frau oder Dr.). Die Präfixwerte werden durch die [Konfiguration](../configuration-reference/customers/customer-configuration.md) bestimmt. Je nach Konfiguration kann das Eingabefeld ein Textfeld oder eine Liste von Optionen sein. |
| **[!UICONTROL First Name]** | Der Vorname des Kunden. |
| **[!UICONTROL Middle Name / Initial]** | Der Vorname oder der Anfangs-Name des Kunden. Dieses Feld ist nur enthalten, wenn im Thema [Konfiguration](../configuration-reference/customers/customer-configuration.md) angegeben. |
| **[!UICONTROL Last Name]** | Der Nachname des Kunden. |
| **[!UICONTROL Name Suffix]** | Bei Verwendung das Suffix, das mit dem Kundennamen verknüpft ist (z. B. Jr., Sr. oder III). Die Suffix-Werte werden durch die [Konfiguration](../configuration-reference/customers/customer-configuration.md) bestimmt. Je nach Konfiguration kann das Eingabefeld ein Textfeld oder eine Dropdown-Liste mit Optionen sein. |
| **[!UICONTROL Email]** | Die E-Mail-Adresse des Kunden. |
| **[!UICONTROL Date of Birth]** | Das Geburtsdatum des Kunden. Das Geburtsdatum wird eingeschlossen, wenn im Thema [Konfiguration](../configuration-reference/customers/customer-configuration.md) angegeben. <br><br>Achten Sie im Einklang mit den aktuellen Best Practices für Sicherheit und Datenschutz auf alle potenziellen rechtlichen und sicherheitstechnischen Risiken, die mit der Speicherung des vollständigen Geburtsdatums (Monat, Tag, Jahr) der Kunden mit anderen persönlichen Identifikatoren verbunden sind. Es wird empfohlen, die Speicherung der vollständigen Geburtsdaten der Kunden zu begrenzen und stattdessen das Geburtsjahr des Kunden zu verwenden. |
| **[!UICONTROL Tax / VAT Number]** | Die Steuer- oder Umsatzsteuer-Nummer des Kunden, falls zutreffend. |
| **[!UICONTROL Gender]** | Identifiziert das Geschlecht des Kunden. Das Geschlecht ist enthalten, wenn es in der [Konfiguration](../configuration-reference/customers/customer-configuration.md) angegeben ist. Optionen: `Male` / `Female` / `Not Specified` |
| **[!UICONTROL Send Welcome Email From]** | Wenn Sie mehrere Store-Ansichten haben, gibt diese Einstellung die Store-Ansicht an, von der die Willkommensnachricht gesendet wird. Wenn Store-Ansichten für verschiedene Sprachen verwendet werden, bestimmt diese Einstellung die Sprache der Begrüßungs-E-Mail. |

### [!UICONTROL Addresses]

| Feld | Beschreibung |
|--- |--- |
| **[!UICONTROL New Addresses]** | Gibt den Typ der neuen Adresse an. Optionen: `Default Billing Address` / `Default Shipping Address` |
| **[!UICONTROL Add New Addresses]** | Zeigt einen weiteren Abschnitt Neue Adresse an, um den Typ der einzugebenden Adresse zu identifizieren. |
| **[!UICONTROL Company]** | Der Name des Unternehmens, falls für diese Adresse zutreffend. |
| **[!UICONTROL Street Address]** | Die Straßenadresse des Kunden. Eine zweite Zeile der Straßenadresse ist verfügbar, wenn im Thema [Konfiguration](../configuration-reference/customers/customer-configuration.md) angegeben. |
| **[!UICONTROL City]** | Die Stadt, in der sich die Kundenadresse befindet. |
| **[!UICONTROL Country]** | Das Land, in dem sich die Kundenadresse befindet. |
| **[!UICONTROL State/Province]** | Das Bundesland oder die Provinz, in dem sich die Kundenadresse befindet. |
| **[!UICONTROL Zip/Postal Code]** | Die Postleitzahl, unter der sich die Kundenadresse befindet. |
| **[!UICONTROL Phone Number]** | Die Telefonnummer des Kunden, die mit der Adresse verknüpft ist. |
| **[!UICONTROL VAT Number]** | Gegebenenfalls die Mehrwertsteuer-Nummer, die für den Kunden an dieser Adresse gilt. |
