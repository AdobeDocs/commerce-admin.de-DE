---
title: '[!UICONTROL Customers]  &gt; [!UICONTROL Customer Configuration]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der [!UICONTROL Customers] &gt; [!UICONTROL Customer Configuration] Seite des Commerce-Administrators.
exl-id: 596359d7-3891-4e0c-9604-3647032188fd
feature: Configuration, Customers
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '1862'
ht-degree: 0%

---

# [!UICONTROL Customers]  > [!UICONTROL Customer Configuration]

{{config}}

## [!UICONTROL Account Sharing Options]

![Optionen für Kontofreigabe](./assets/customer-configuration-account-sharing-options.png)<!-- zoom -->

<!-- [Account Sharing Options](https://docs.magento.com/user-guide/customers/account-scope.html) -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Share Customer Accounts] | Global | Bestimmt den Umfang der Kundenkonten in der Store-Hierarchie. Optionen: <br/>**`Global`**- Kundenkontoinformationen werden für jede Website freigegeben und in der Commerce-Installation gespeichert.<br/>**`Per Website`** - Die Kundenkontoinformationen sind auf die Website beschränkt, auf der das Konto erstellt wurde. |

{style="table-layout:auto"}

## [!UICONTROL Online Customers Options]

![Online-Kundenoptionen](./assets/customer-configuration-online-customers-options.png)<!-- zoom -->

<!-- [Online Customers Options](https://docs.magento.com/user-guide/customers/now-online.html) -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Online Minutes Interval] | Global | Bestimmt, wie lange die Online-Aktivität eines Kunden vom Administrator zugänglich ist. Lassen Sie den Standardwert von 15 Minuten leer. |
| [!UICONTROL Customer Data Lifetime] | Global | Bestimmt die Anzahl der Minuten, bevor nicht gespeicherte Daten ablaufen, die vom Kunden eingegeben wurden. Standardmäßig laufen nicht gespeicherte Daten nach 60 Minuten ab. |

{style="table-layout:auto"}

## [!UICONTROL Create New Account Options]

{{beta-updates}}

![Neue Kontooptionen erstellen](./assets/customer-configuration-create-new-account-options.png)<!-- zoom -->

![Neue Kontooptionen erstellen (MwSt-Felder)](./assets/customer-configuration-create-new-account-options-vat.png)<!-- zoom -->

<!-- [Create New Account Options (VAT Fields)](https://docs.magento.com/user-guide/customers/customer-account-configuration.html) -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable Automatic Assignment to Customer Group] | Store-Ansicht | Bestimmt, ob Kunden automatisch der standardmäßigen Kundengruppe zugewiesen werden. Um die MwSt.-Nummer im Store anzuzeigen, wählen Sie die Option MwSt.-Nummer anzeigen im Schaufenster aus. `Yes`. Optionen: <br/>**`Yes`**- Das System validiert nicht automatisch die MwSt-IDs von Kunden und ändert auch nicht die Kundengruppen.<br/>**`No`** - Das Systemverhalten ist wie gewohnt und die standardmäßige Kundengruppe kann im Feld Standardgruppe festgelegt werden. |
| [!UICONTROL Default Group] | Store-Ansicht | Identifiziert die ursprüngliche Kundengruppe, die bei der Erstellung eines Kontos zugewiesen wurde. |
| [!UICONTROL Default Value for Disable Automatic Group Changes Based on VAT ID] | Global | (Nur verfügbar, wenn der aktuelle Konfigurationsbereich auf `Default Group`. Wählen Sie aus, ob die automatische Änderung der auf der Mehrwertsteuer-ID basierenden Kundengruppe standardmäßig aktiviert oder deaktiviert ist. Die Einstellung kann auf der Produktebene überschrieben werden. Die Einstellung beeinflusst das Systemverhalten in den folgenden Situationen: <br/> - Die Mehrwertsteuer-ID der Standardadresse des Kunden oder die gesamte Standardadresse. <br/> - Die Änderung der Kundengruppe wurde beim Checkout für einen registrierten Kunden, der keine zuvor gespeicherte Adresse hatte, oder für einen Kunden, der sich beim Checkout registriert hat, emuliert. <br/>Wenn die automatische Gruppenänderung aktiviert ist, ändert sich im ersten Fall die Kundengruppe automatisch und im zweiten Fall wird die vorübergehend emulierte Kundengruppe dem Kunden zugewiesen. Wenn die automatische Gruppenänderung deaktiviert ist, ändert sich die zugewiesene Kundengruppe nie, es sei denn, ein Administrator ändert sie manuell. |
| [!UICONTROL Show VAT Number on Storefront] | Webseite | Bestimmt, ob die MwSt-Nummer für Kunden im Geschäft sichtbar ist. Optionen: `Yes` / `No` <br/> Betrifft nur reguläre Nicht-B2B-Kundenkonten. Unternehmenskonten verfügen über ein eigenes Feld für die MwSt.-Nummer. |
| [!UICONTROL Default Email Domain] | Store-Ansicht | Gibt die Standard-E-Mail-Domäne für den Store an. Beispiel: `mystore.com` |
| [!UICONTROL Default Welcome Email] | Store-Ansicht | Identifiziert die für den Standard verwendete E-Mail-Vorlage _Willkommen_ E-Mail |
| [!UICONTROL Default Welcome Email Without Password] | Store-Ansicht | Eine alternative Begrüßungs-E-Mail-Vorlage, die für neue, vom Administrator erstellte Kundenkonten verwendet wird, denen noch kein Kennwort zugewiesen ist. |
| [!UICONTROL Email Sender] | Store-Ansicht | Identifiziert den Store-Kontakt, der als Absender der Begrüßungs-E-Mail angezeigt wird. |
| [!UICONTROL Require Emails Confirmation] | Webseite | Bestimmt, ob eine Anforderung zum Erstellen eines Kontos eine Bestätigung durch den Kunden erfordert. Optionen: `Yes` / `No` |
| [!UICONTROL Confirmation Link Email] | Store-Ansicht | Identifiziert die für die Bestätigungs-E-Mail verwendete E-Mail-Vorlage. Standardvorlage: `New account confirmation key` |
| [!UICONTROL Welcome Email] | Store-Ansicht | Identifiziert die E-Mail-Vorlage, die für die Begrüßungsnachricht verwendet wird, die nach der Bestätigung des Kontos gesendet wird. |
| [!UICONTROL Generate Human-Friendly Customer ID] | Global | Bestimmt, ob das Feld, in das die MwSt.-ID-Nummer eingegeben und gespeichert wird, in der Storefront sichtbar ist. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Password Options]

![Kennwortoptionen](./assets/customer-configuration-password-options.png)<!-- zoom -->

<!-- [Password Options](https://docs.magento.com/user-guide/customers/password-options.html) -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Password Reset Protection Type] | Store-Ansicht | Bestimmt die Methode zum Zurücksetzen des Kennworts für ein Kundenkonto. Optionen: <br/>**`By IP and Email`**- Das Kennwort kann online zurückgesetzt werden, nachdem eine Antwort von einer Zurücksetzungsbenachrichtigung empfangen wurde, die an die mit dem Admin-Konto verknüpfte E-Mail-Adresse gesendet wird.<br/>**`By IP`** - Das Passwort kann online zurückgesetzt werden. <br/>**`By Email`**- Das Kennwort kann zurückgesetzt werden, indem eine E-Mail-Benachrichtigung gesendet wird, die an die mit dem Admin-Konto verknüpfte E-Mail-Adresse gesendet wird.<br/>**`None`** - Das Kennwort kann nur vom Store-Administrator zurückgesetzt werden. |
| [!UICONTROL Max Number of Password Reset Requests] | Store-Ansicht | Beschränkt die Anzahl der Anforderungen zum Zurücksetzen des Kennworts pro Stunde. Geben Sie bei unbegrenzten Anforderungen null (0) ein. |
| [!UICONTROL Min Time Between Password Reset Requests] | Store-Ansicht | Bestimmt die Anzahl der Minuten zwischen Anforderungen zum Zurücksetzen des Kennworts. Geben Sie null (0) ein, damit keine Verzögerung zwischen den Anforderungen eintritt. |
| [!UICONTROL Forgot Email Template] | Store-Ansicht | Identifiziert die E-Mail-Vorlage, die verwendet wird, wenn Kunden ihr Passwort vergessen. Standardvorlage: `Forgot Password` |
| [!UICONTROL Remind Email Template] | Store-Ansicht | Identifiziert die E-Mail-Vorlage, die verwendet wird, wenn Kunden eine Kennworterinnerung oder einen Hinweis erhalten. Standardvorlage: `Remind Password` |
| [!UICONTROL Reset Password Template] | Store-Ansicht | Bestimmt die E-Mail-Vorlage, die verwendet wird, wenn Kunden ihre Kennwörter zurücksetzen. |
| [!UICONTROL Password Template Email Sender] | Store-Ansicht | Legt den Store-Kontakt fest, der als Absender kennwortbezogener E-Mails angezeigt wird. |
| [!UICONTROL Recovery Link Expiration Period (hours)] | Global | Gibt die Anzahl der Stunden an, bevor ein Link zur Passwortwiederherstellung abläuft. |
| [!UICONTROL Enable Autocomplete on login/forgot password forms] | Webseite | Bestimmt, ob die automatische Vervollständigung bei Anmeldeformularen aktiviert ist bzw. ob Kennwortformulare vergessen wurden. Optionen: `Yes` / `No` |
| [!UICONTROL Number of Required Character Classes] | Global | Bestimmt die Anzahl verschiedener Zeichenklassen (Kleinbuchstaben, Großbuchstaben, numerische Zeichen und Sonderzeichen), die in ein Kennwort eingeschlossen werden müssen. |
| [!UICONTROL Maximum Login Failures to Lockout Account] | Global | Bestimmt die Anzahl fehlgeschlagener Anmeldeversuche, bis das Kundenkonto gesperrt ist. Geben Sie für unbegrenzte Versuche null (`0`). |
| [!UICONTROL Minimum Password Length] | Global | Bestimmt die Mindestanzahl von Zeichen, die in einem Kennwort zulässig sind. Die Zahl muss größer als null sein (`0`). |
| [!UICONTROL Lockout Time (minutes)] | Global | Bestimmt die Anzahl der Minuten, in denen ein Kundenkonto nach zu vielen fehlgeschlagenen Anmeldeversuchen gesperrt wird. |

{style="table-layout:auto"}

## [!UICONTROL Account Information Options]

![Kontoinformationsoptionen](./assets/customer-configuration-account-info-options.png)<!-- zoom -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Change Email Template] | Store-Ansicht | Identifiziert die Standard-E-Mail-Vorlage, die verwendet wird, wenn ein Kunde seine E-Mail-Adresse ändert. |
| [!UICONTROL Change Email and Password Template] | Store-Ansicht | Gibt die Standard-E-Mail-Vorlage an, die verwendet wird, wenn ein Kunde seine E-Mail-Adresse und sein Passwort ändert. |

{style="table-layout:auto"}

## [!UICONTROL Name and Address Options]

### Optionen für Magento Open Sourcen

{{ce-feature}}

![Name und Adressenoptionen - Open Source](./assets/customer-configuration-name-address-options-ce.png)<!-- zoom -->

<!-- [Name and Address Options - Open Source](https://docs.magento.com/user-guide/customers/name-address-options.html) -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Number of Lines in a Street Address] | Webseite | Legt die Anzahl der Zeilen in der Straßenadresse fest. Die Straßenadresse besteht aus `1` nach `4` Zeilen. Wenn das Feld leer ist, lautet die Standard-Straßenadresse 3 (`3`) verwendet. |
| [!UICONTROL Show Prefix] | Webseite | Stellt fest, ob der Kundenname am Anfang ein Präfix enthält, z. B. Herr und Frau Options: `No` / `Optional` / `Required` |
| [!UICONTROL Prefix Dropdown Options] | Webseite | Definiert die Liste der Präfixoptionen. Trennen Sie Werte durch Semikolon. Setzen Sie ein Semikolon vor den ersten Wert, um oben in der Liste einen leeren Wert anzuzeigen. |
| [!UICONTROL Show Middle Name (initial)] | Webseite | Bestimmt, ob die mittlere Initiale als Teil des Kundennamens enthalten ist. Bei Verwendung von ist die mittlere Initialisierung ein optionales Feld. Optionen: `Yes` / `No` |
| [!UICONTROL Show Suffix] | Webseite | Bestimmt, ob der Kundenname am Ende ein Suffix enthält, z. B. Jr., Sr. und III. Optionen: `No` / `Optional` / `Required` |
| [!UICONTROL Suffix Dropdown Options] | Webseite | Definiert die Liste der Suffix-Optionen. Trennen Sie Werte durch Semikolon. Setzen Sie ein Semikolon vor den ersten Wert, um oben in der Liste einen leeren Wert anzuzeigen. |
| [!UICONTROL Show Date of Birth] | Webseite | Bestimmt, ob das Geburtsdatum des Kunden im Namen- und Adressformular enthalten ist. Optionen: `No` / `Optional` / `Required`  <br><br>**_Wichtig:_**Beachten Sie im Einklang mit den aktuellen Best Practices für Sicherheit und Datenschutz alle potenziellen rechtlichen und sicherheitstechnischen Risiken, die mit der Speicherung des vollständigen Geburtsdatums (Monat, Tag, Jahr) der Kunden mit anderen persönlichen Identifikatoren verbunden sind. Es wird empfohlen, die Speicherung der vollständigen Geburtsdaten der Kunden zu begrenzen und stattdessen das Geburtsjahr des Kunden zu verwenden. |
| [!UICONTROL Show Tax/VAT Number] | Webseite | Bestimmt, ob die Steuer oder [MwSt. Nummer](../../stores-purchase/vat.md) im Namen und im Adressformular enthalten ist. Optionen: `No` / `Optional` / `Required` |
| [!UICONTROL Show Gender] | Webseite | Bestimmt, ob Geschlecht im Namen- und Adressformular enthalten ist. Optionen: `No` / `Optional` / `Required` |
| [!UICONTROL Show Telephone] | Webseite | Bestimmt, ob die Telefonnummer des Kunden im Namen und im Adressformular enthalten ist. Optionen: `No` / `Optional` / `Required` |
| [!UICONTROL Show Company] | Webseite | Stellt fest, ob das Unternehmen des Kunden im Namen- und Adressformular enthalten ist. Optionen: `No` / `Optional` / `Required` |
| [!UICONTROL Show Fax] | Webseite | Bestimmt, ob die Faxnummer des Kunden im Namen- und Adressformular enthalten ist. Optionen: `No` / `Optional` / `Required` |

{style="table-layout:auto"}

### Adobe Commerce-Optionen

{{ee-feature}}

![Name und Adressenoptionen - Commerce](./assets/customer-configuration-name-address-options-ee.png)<!-- zoom -->

<!-- [Name and Address Options - Commerce](https://docs.magento.com/user-guide/customers/name-address-options.html) -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Prefix Dropdown Options] | Webseite | Definiert die Liste der Präfixoptionen. Trennen Sie Werte durch Semikolon. Setzen Sie ein Semikolon vor den ersten Wert, um oben in der Liste einen leeren Wert anzuzeigen. |
| [!UICONTROL Suffix Dropdown Options] | Webseite | Definiert die Liste der Suffix-Optionen. Trennen Sie Werte durch Semikolon. Setzen Sie ein Semikolon vor den ersten Wert, um oben in der Liste einen leeren Wert anzuzeigen. |
| [!UICONTROL Show Telephone] | Webseite | Bestimmt, ob die Telefonnummer des Kunden im Namen und im Adressformular enthalten ist. Optionen: `No` / `Optional` / `Required` |
| [!UICONTROL Show Company] | Webseite | Stellt fest, ob das Unternehmen des Kunden im Namen- und Adressformular enthalten ist. Optionen: `No` / `Optional` / `Required` |
| [!UICONTROL Show Fax] | Webseite | Bestimmt, ob die Faxnummer des Kunden im Namen- und Adressformular enthalten ist. Optionen: `No` / `Optional` / `Required` |

{style="table-layout:auto"}

## [!UICONTROL Store Credit Options]

{{ee-feature}}

![Kreditoptionen speichern](./assets/customer-configuration-store-credit-options.png)<!-- zoom -->

<!-- [Store Credit Options](https://docs.magento.com/user-guide/customers/credit-configure.html) -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable Store Credit Functionality] | Global | Bestimmt, ob die Store-Gutschrift aktiviert ist. Wenn Sie diese Option deaktivieren, werden die Store-Gutschriften aus den Kundenkonten und auf der Seite &quot;Admin-Kunden verwalten&quot;entfernt. Optionen: `Yes` / `No`. |
| [!UICONTROL Show Store Credit History to Customers] | Webseite | Bestimmt, ob der Bilanzverlauf in Kundenkonten sichtbar ist. Optionen: `Yes` / `No`. |
| [!UICONTROL Refund Store Credit Automatically] | Global | Bestimmt, ob die Store-Erstattung automatisch ausgegeben wird. Optionen: `Yes` / `No` |
| [!UICONTROL Store Credit Update Email Sender] | Store-Ansicht | Bestimmt die Store-Identität, die als Absender von an Kunden gesendeten Kreditaktualisierungsbenachrichtigungen angezeigt wird. |
| [!UICONTROL Store Credit Update Email Template] | Store-Ansicht | Legt die E-Mail-Vorlage fest, die für Kreditaktualisierungen verwendet wird. |

{style="table-layout:auto"}

## [!UICONTROL Login Options]

![Anmeldeoptionen](./assets/customer-configuration-login-options.png)<!-- zoom -->

<!-- [Login Options](https://docs.magento.com/user-guide/customers/login-landing-page.html) -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Redirect Customer to Account Dashboard after Logging in] | Webseite | Bestimmt, was nach der Anmeldung von Kunden bei ihren Konten geschieht. Um Kunden zu ihrem Konto-Dashboard weiterzuleiten, wählen Sie `Yes`. Optionen: <br/>**`Yes`**- Das Konto-Dashboard wird angezeigt, wenn sich Kunden bei ihren Konten anmelden.<br/>**`No`** - Kunden können nach der Anmeldung bei ihren Konten weiterhin einkaufen. |

{style="table-layout:auto"}

## [!UICONTROL Address Templates]

![Adressenvorlagen](./assets/customer-configuration-address-templates.png)<!-- zoom -->

<!-- [Address Templates](https://docs.magento.com/user-guide/customers/address-templates.html) -->

| Vorlage | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Text] | Store-Ansicht | Die Vorlage wird für alle gedruckten Adressen verwendet. |
| [!UICONTROL Text One Line] | Store-Ansicht | Diese Vorlage definiert die Reihenfolge der Adressentitäten in der Buchliste der Warenkorbansicht des Kunden. Fortschritt beim Checkout. |
| [!UICONTROL HTML] | Store-Ansicht | Diese Vorlage definiert die Reihenfolge der Adressfelder unter der _Kundenadressen_ im Admin-Bereich ([!UICONTROL Customers] > [!UICONTROL Manage Customers]). Dies betrifft auch die _Neue Adresse hinzufügen_ Seite, wenn ein Kunde eine Abrechnungs- oder Lieferadresse auf seiner Kontoseite erstellt. |
| [!UICONTROL PDF] | Store-Ansicht | Die Vorlage definiert die Anzeige von Abrechnungs- und Versandadressen in den gedruckten Rechnungen, Sendungen und Kreditkarten. |

{style="table-layout:auto"}

## [!UICONTROL Customer Segments]

{{ee-feature}}

![Kundensegmente](./assets/customer-configuration-customer-segments.png)<!-- zoom -->

<!-- [Customer Segments](https://docs.magento.com/user-guide/marketing/customer-segments.html) -->

| Vorlage | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable Customer Segment Functionality] | Global | Bestimmt, ob Kundensegmente zur Erstellung gezielter Promotions verwendet werden können. Optionen: `Yes` / `No` |
| [!UICONTROL Real-time Check if Customer is Matched by Segment] | Global | Bestimmt, ob Kundensegmente in Echtzeit validiert werden. Optionen: <br/>**[!UICONTROL Yes]**- Kundensegmente werden in Echtzeit validiert (Standardwert).<br/>**[!UICONTROL No]** - Kundensegmente werden durch eine einzige kombinierte Bedingungs-SQL-Abfrage validiert. Dies verbessert die Leistung der Segmentvalidierung, wenn das System viele Kundensegmente enthält. Die Validierung funktioniert jedoch nicht mit einer geteilten Datenbank oder wenn keine registrierten Kunden vorhanden sind. |

{style="table-layout:auto"}

## [!UICONTROL CAPTCHA]

![CAPTCHA](./assets/customer-configuration-captcha.png)<!-- zoom -->

<!-- [CAPTCHA](https://docs.magento.com/user-guide/stores/security-captcha.html) -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable CAPTCHA on Storefront] | Webseite | Aktiviert CAPTCHA in den Stores, die mit der Commerce-Website verknüpft sind. Optionen: `Yes` / `No` |
| [!UICONTROL Font] | Webseite | Legt die Schriftart fest, die zum Anzeigen des CAPTCHA verwendet wird. Um eine eigene Schriftart hinzuzufügen, legen Sie die Schriftartdatei im selben Ordner ab wie Ihre Commerce-Installation und fügen Sie die Deklaration zum `config.xml` Datei unter `app/code/Magento/Captcha/etc`. |
| [!UICONTROL Forms] | Webseite | Bestimmt die Formulare, in denen CAPTCHA verwendet wird. Optionen: <br />`Applying Coupon Code` <br />`Checkout/Placing Order`<br />`Create user` <br />`Login` <br />`Forgot password` <br />`Contact Us` <br />`Change password` <br />`Share Wishlist Form` <br />`Send to Friend Form` <br />`Payflow Pro` (siehe [Sicherheits-Patch](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/payments/paypal-payflow-pro-active-carding-activity.html)) <br />`Add Gift Card Code` ![Adobe Commerce](../../assets/adobe-logo.svg)  <br />`Create company` ![Adobe Commerce](../../assets/adobe-logo.svg)  <br /><br />_**Hinweis:**_ Die Formulare &quot;Benutzer erstellen&quot;, &quot;Kennwort vergessen&quot;und &quot;Payflow Pro&quot;sind bei Auswahl immer aktiviert. |
| [!UICONTROL Displaying Mode] | Webseite | Bestimmt, wann das CAPTCHA angezeigt wird. Optionen: <br/>**`Always`**- CAPTCHA ist immer zum Anmelden erforderlich.<br/>**`After number of attempts to login`** - Diese Option gilt nur für das Anmeldeformular für Administratoren. Wenn ausgewählt, wird die _[!UICONTROL Number of Unsuccessful Attempts to Login]_angezeigt. Geben Sie die Anzahl der Anmeldeversuche ein, die Sie zulassen möchten. Ein Wert von `0` (Null) ähnelt der Einstellung [!UICONTROL Displaying Mode] nach `Always`.<br/>_**Hinweis:**_Um die Anzahl der fehlgeschlagenen Anmeldeversuche zu verfolgen, wird jeder Versuch, sich unter einer E-Mail-Adresse und von einer IP-Adresse aus anzumelden, gezählt. Die maximal zulässige Anzahl von Anmeldeversuchen für dieselbe IP-Adresse beträgt 1.000. Diese Einschränkung gilt nur, wenn CAPTCHA aktiviert ist. |
| [!UICONTROL Number of Unsuccessful Attempts to Login] | Webseite | Gibt an, wie oft ein Kunde versuchen kann, sich anzumelden, bevor das Konto gesperrt wird. |
| [!UICONTROL CAPTCHA Timeout (minutes)] | Webseite | Bestimmt die Lebensdauer des aktuellen CAPTCHA. Wenn das CAPTCHA abläuft, muss der Benutzer die Seite neu laden. |
| [!UICONTROL Number of Symbols] | Webseite | Bestimmt die Anzahl der Symbole, die im CAPTCHA angezeigt werden, mit einer maximalen Anzahl von 8. Sie können auch einen Bereich angeben, z. B. 5-8. |
| [!UICONTROL Symbols Used in CAPTCHA] | Webseite | Bestimmt die Buchstaben (a-z und A-Z) und Zahlen (0-9), die in der CAPTCHA angezeigt werden. Symbole, die sich nur schwer von anderen Symbolen unterscheiden lassen, z. B. `i`, `l`oder `1`, sind nicht im Standardsatz der CAPTCHA-Symbole enthalten. |
| [!UICONTROL Case Sensitive] | Webseite | Bestimmt, ob bei CAPTCHA-Zeichen die Groß-/Kleinschreibung beachtet wird. Optionen: `Yes` / `No` |

{style="table-layout:auto"}
