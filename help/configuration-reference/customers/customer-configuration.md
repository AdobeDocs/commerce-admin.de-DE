---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Customer Configuration]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Customers] &gt; [!UICONTROL Customer Configuration] des Commerce Admin-Bereichs.
exl-id: 596359d7-3891-4e0c-9604-3647032188fd
feature: Configuration, Customers
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '1890'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Customer Configuration]

{{config}}

## [!UICONTROL Account Sharing Options]

![Optionen zur Kontofreigabe](./assets/customer-configuration-account-sharing-options.png)<!-- zoom -->

<!-- [Account Sharing Options](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/customer-accounts/customer-account-scope) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Share Customer Accounts] | Global | Bestimmt den Umfang von Kundenkonten in der Store-Hierarchie. Optionen: <br/>**`Global`**- Kundenkontoinformationen werden für jede Website freigegeben und in der Commerce-Installation gespeichert.<br/>**`Per Website`** - Kundenkontoinformationen sind auf die Website beschränkt, auf der das Konto erstellt wurde. |

{style="table-layout:auto"}

## [!UICONTROL Online Customers Options]

![Online-Kundenoptionen](./assets/customer-configuration-online-customers-options.png)<!-- zoom -->

<!-- [Online Customers Options](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/customers-menu/now-online) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Online Minutes Interval] | Global | Legt fest, wie lange der Admin auf die Online-Aktivität eines Kunden zugreifen kann. Für ein Standardintervall von 15 Minuten leer lassen. |
| [!UICONTROL Customer Data Lifetime] | Global | Bestimmt die Anzahl der Minuten vor Ablauf nicht gespeicherter Daten, die vom Kunden eingegeben werden. Standardmäßig laufen nicht gespeicherte Daten nach 60 Minuten ab. |

{style="table-layout:auto"}

## [!UICONTROL Create New Account Options]

![Neue Kontooptionen erstellen](./assets/customer-configuration-create-new-account-options.png)<!-- zoom -->

![Optionen für neues Konto erstellen (MwSt.-Felder)](./assets/customer-configuration-create-new-account-options-vat.png)<!-- zoom -->

<!-- [Create New Account Options (VAT Fields)](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/customer-accounts/configure/login-landing-page) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable Automatic Assignment to Customer Group] | Shop-Ansicht | Bestimmt, ob Kunden automatisch der Standardkundengruppe zugewiesen werden. Um die MwSt.-Nummer im Geschäft anzuzeigen, setzen Sie MwSt.-Nummer anzeigen in der Storefront und wählen Sie `Yes` aus. Optionen: <br/>**`Yes`**- Das System validiert nicht automatisch die Umsatzsteuer-Identifikatoren des Kunden und ändert auch nicht die Kundengruppen.<br/>**`No`** - Das Systemverhalten ist wie gewohnt und die Standardkundengruppe kann im Feld Standardgruppe festgelegt werden. |
| [!UICONTROL Default Group] | Shop-Ansicht | Gibt die anfängliche Kundengruppe an, die beim Erstellen eines Kontos zugewiesen wurde. |
| [!UICONTROL Default Value for Disable Automatic Group Changes Based on VAT ID] | Global | (Nur verfügbar, wenn der aktuelle Konfigurationsumfang auf `Default Group` festgelegt ist.) Wählen Sie aus, ob die automatische Änderung der Kundengruppe basierend auf der MwSt.-ID standardmäßig aktiviert oder deaktiviert ist. Die Einstellung kann auf Produktebene überschrieben werden. Die Einstellung beeinflusst das Systemverhalten in folgenden Situationen: <br/> - Die MwSt.-ID der Standardadresse des Kunden oder die gesamte Standardadresse ändert sich. <br/> - Die Änderung der Kundengruppe wurde beim Checkout für einen registrierten Kunden emuliert, der zuvor keine gespeicherte Adresse hatte, oder für einen Kunden, der sich während des Checkouts registriert hat. <br/>Wenn die automatische Gruppenänderung aktiviert ist, ändert sich im ersten Fall die Kundengruppe automatisch, und im zweiten Fall wird die vorübergehend emulierte Kundengruppe dem Kunden zugewiesen. Wenn die automatische Gruppenänderung deaktiviert ist, ändert sich die zugewiesene Kundengruppe nie, es sei denn, ein Administrator ändert sie manuell. |
| [!UICONTROL Show VAT Number on Storefront] | Website | Legt fest, ob die MwSt.-Nummer für Kunden im Geschäft sichtbar ist. Optionen: `Yes` / `No` <br/> Betrifft nur reguläre Nicht-B2B-Kundenkonten. Unternehmenskonten verfügen über ein eigenes Feld für die MwSt.-Nummer. |
| [!UICONTROL Default Email Domain] | Shop-Ansicht | Identifiziert die Standard-E-Mail-Domain für den Store. Beispiel: `mystore.com` |
| [!UICONTROL Default Welcome Email] | Shop-Ansicht | Gibt die E-Mail-Vorlage an, die für die standardmäßige _Begrüßungs-)_ verwendet wird. |
| [!UICONTROL Default Welcome Email Without Password] | Shop-Ansicht | Eine alternative Willkommens-E-Mail-Vorlage, die für neue, vom Administrator erstellte Kundenkonten verwendet wird, denen noch kein Kennwort zugewiesen wurde. |
| [!UICONTROL Email Sender] | Shop-Ansicht | Identifiziert den Store-Kontakt, der als Absender der Begrüßungs-E-Mail angezeigt wird. |
| [!UICONTROL Require Emails Confirmation] | Website | Legt fest, ob eine Anforderung zum Erstellen eines Kontos eine Bestätigung vom Kunden erfordert. Optionen: `Yes` / `No`. <br/><br/> _&#x200B;**Hinweis:**&#x200B;_ Ab Version 2.4.7 müssen Kunden unabhängig vom Browser ihre E-Mail-Adresse und ihr Passwort erneut eingeben, um sich nach der E-Mail-Bestätigung bei ihrem Konto anzumelden. |
| [!UICONTROL Confirmation Link Email] | Shop-Ansicht | Identifiziert die E-Mail-Vorlage, die für die Bestätigungs-E-Mail verwendet wird. Standardvorlage: `New account confirmation key` |
| [!UICONTROL Welcome Email] | Shop-Ansicht | Identifiziert die E-Mail-Vorlage, die für die Begrüßungsnachricht verwendet wird, die nach der Bestätigung des Kontos gesendet wird. |
| [!UICONTROL Generate Human-Friendly Customer ID] | Global | Bestimmt, ob das Feld, das zum Eingeben und Speichern der MwSt.-ID-Nummer verwendet wird, in der Storefront sichtbar ist. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Password Options]

![Kennwortoptionen](./assets/customer-configuration-password-options.png)<!-- zoom -->

<!-- [Password Options](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/customer-accounts/configure/password-options) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Password Reset Protection Type] | Shop-Ansicht | Bestimmt die Methode zum Zurücksetzen eines Kennworts für ein Kundenkonto. Optionen: <br/>**`By IP and Email`**- Das Kennwort kann online zurückgesetzt werden, nachdem eine Antwort von einer Zurücksetzungsbenachrichtigung empfangen wurde, die an die mit dem Admin-Konto verknüpfte E-Mail-Adresse gesendet wird.<br/>**`By IP`** - Das Kennwort kann online zurückgesetzt werden. <br/>**`By Email`**- Das Kennwort kann zurückgesetzt werden, indem auf eine E-Mail-Benachrichtigung reagiert wird, die an die mit dem Admin-Konto verknüpfte E-Mail-Adresse gesendet wird.<br/>**`None`** - Das Kennwort kann nur vom Store-Administrator zurückgesetzt werden. |
| [!UICONTROL Max Number of Password Reset Requests] | Shop-Ansicht | Beschränkt die Anzahl der Anfragen zum Zurücksetzen des Kennworts pro Stunde. Geben Sie für unbegrenzte Anfragen null (0) ein. |
| [!UICONTROL Min Time Between Password Reset Requests] | Shop-Ansicht | Bestimmt die Anzahl der Minuten zwischen den Anforderungen zum Zurücksetzen des Kennworts. Geben Sie für keine Verzögerung zwischen den Anfragen null (0) ein. |
| [!UICONTROL Forgot Email Template] | Shop-Ansicht | Identifiziert die E-Mail-Vorlage, die verwendet wird, wenn Kunden ihre Passwörter vergessen. Standardvorlage: `Forgot Password` |
| [!UICONTROL Remind Email Template] | Shop-Ansicht | Identifiziert die E-Mail-Vorlage, die verwendet wird, wenn Kundinnen und Kunden eine Kennworterinnerung oder einen Hinweis erhalten. Standardvorlage: `Remind Password` |
| [!UICONTROL Reset Password Template] | Shop-Ansicht | Bestimmt die E-Mail-Vorlage, die verwendet wird, wenn Kunden ihre Kennwörter zurücksetzen. |
| [!UICONTROL Password Template Email Sender] | Shop-Ansicht | Bestimmt den Store-Kontakt, der als Absender kennwortbezogener E-Mails angezeigt wird. |
| [!UICONTROL Recovery Link Expiration Period (hours)] | Global | Gibt die Anzahl der Stunden an, nach denen ein Link zur Passwortwiederherstellung abläuft. |
| [!UICONTROL Enable Autocomplete on login/forgot password forms] | Website | Bestimmt, ob die automatische Vervollständigung in Anmelde-/Kennwortformularen aktiviert ist. Optionen: `Yes` / `No` |
| [!UICONTROL Number of Required Character Classes] | Global | Bestimmt die Anzahl der verschiedenen Zeichenklassen (Kleinbuchstaben, Großbuchstaben, numerische Zeichen und Sonderzeichen), die in einem Kennwort enthalten sein müssen. |
| [!UICONTROL Maximum Login Failures to Lockout Account] | Global | Bestimmt die Anzahl fehlgeschlagener Anmeldeversuche, bis das Kundenkonto gesperrt ist. Geben Sie für unbegrenzte Versuche null (`0`) ein. |
| [!UICONTROL Minimum Password Length] | Global | Bestimmt die zulässige Mindestanzahl von Zeichen in einem Kennwort. Die Zahl muss größer als null (`0`) sein. |
| [!UICONTROL Lockout Time (minutes)] | Global | Bestimmt die Anzahl der Minuten, die ein Kundenkonto nach zu vielen fehlgeschlagenen Anmeldeversuchen gesperrt ist. |

{style="table-layout:auto"}

## [!UICONTROL Account Information Options]

![Optionen für Kontoinformationen](./assets/customer-configuration-account-info-options.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Change Email Template] | Shop-Ansicht | Identifiziert die standardmäßige E-Mail-Vorlage, die verwendet wird, wenn ein Kunde seine E-Mail-Adresse ändert. |
| [!UICONTROL Change Email and Password Template] | Shop-Ansicht | Identifiziert die Standard-E-Mail-Vorlage, die verwendet wird, wenn ein Kunde seine E-Mail-Adresse und sein Passwort ändert. |

{style="table-layout:auto"}

## [!UICONTROL Name and Address Options]

### Magento Open Source-Optionen

{{ce-feature}}

![Optionen für Name und Adresse - Source öffnen](./assets/customer-configuration-name-address-options-ce.png)<!-- zoom -->

<!-- [Name and Address Options - Open Source](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/customer-accounts/configure/name-address-options) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Number of Lines in a Street Address] | Website | Bestimmt die Anzahl der Zeilen in der Straßenadresse. Die Straßenadresse besteht aus `1` bis `4` Zeilen. Wenn das Feld leer ist, wird die Standardstraßenadresse von drei (`3`) Zeilen verwendet. |
| [!UICONTROL Show Prefix] | Website | Bestimmt, ob der Kundenname am Anfang ein Präfix enthält, z. B. Herr und Frau. Optionen: `No` / `Optional` / `Required` |
| [!UICONTROL Prefix Dropdown Options] | Website | Definiert die Liste der Präfixoptionen. Trennen Sie Werte mit einem Semikolon. Setzen Sie ein Semikolon vor den ersten Wert, um einen leeren Wert am Anfang der Liste anzuzeigen. |
| [!UICONTROL Show Middle Name (initial)] | Website | Legt fest, ob die Initiale der Mitte als Teil des Kundennamens enthalten ist. Bei Verwendung von ist das mittlere Initialzeichen ein optionales Feld. Optionen: `Yes` / `No` |
| [!UICONTROL Show Suffix] | Website | Bestimmt, ob der Kundenname am Ende ein Suffix enthält, z. B. Jr., Sr. und III. Optionen: `No` / `Optional` / `Required` |
| [!UICONTROL Suffix Dropdown Options] | Website | Definiert die Liste der Suffix-Optionen. Trennen Sie Werte mit einem Semikolon. Setzen Sie ein Semikolon vor den ersten Wert, um einen leeren Wert am Anfang der Liste anzuzeigen. |
| [!UICONTROL Show Date of Birth] | Website | Bestimmt, ob das Geburtsdatum des Kunden im Namen- und Adressformular enthalten ist. Optionen: `No` / `Optional` / `Required` <br><br>**_Wichtig:_**&#x200B;Gemäß den aktuellen Best Practices für Sicherheit und Datenschutz sollten Sie sich über potenzielle rechtliche und Sicherheitsrisiken im Zusammenhang mit der Speicherung des vollständigen Geburtsdatums der Kunden (Monat, Tag, Jahr) mit anderen persönlichen Kennungen im Klaren sein. Es wird empfohlen, die Speicherung der vollständigen Geburtsdaten von Kundinnen und Kunden zu begrenzen und alternativ ein Kundenjahr zu verwenden. |
| [!UICONTROL Show Tax/VAT Number] | Website | Legt fest, ob die Steuer oder [Umsatzsteuer-Nummer](../../stores-purchase/vat.md) im Namen- und Adressformular enthalten ist. Optionen: `No` / `Optional` / `Required` |
| [!UICONTROL Show Gender] | Website | Bestimmt, ob das Geschlecht im Namen- und Adressformular enthalten ist. Optionen: `No` / `Optional` / `Required` |
| [!UICONTROL Show Telephone] | Website | Bestimmt, ob die Telefonnummer des Kunden im Namen- und Adressformular enthalten ist. Optionen: `No` / `Optional` / `Required` |
| [!UICONTROL Show Company] | Website | Bestimmt, ob das Unternehmen des Kunden im Namen- und Adressformular enthalten ist. Optionen: `No` / `Optional` / `Required` |
| [!UICONTROL Show Fax] | Website | Bestimmt, ob die Faxnummer des Kunden im Namen- und Adressformular enthalten ist. Optionen: `No` / `Optional` / `Required` |

{style="table-layout:auto"}

### Adobe Commerce-Optionen

{{ee-feature}}

![Optionen für Name und Adresse - Commerce](./assets/customer-configuration-name-address-options-ee.png)<!-- zoom -->

<!-- [Name and Address Options - Commerce](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/customer-accounts/configure/name-address-options) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Prefix Dropdown Options] | Website | Definiert die Liste der Präfixoptionen. Trennen Sie Werte mit einem Semikolon. Setzen Sie ein Semikolon vor den ersten Wert, um einen leeren Wert am Anfang der Liste anzuzeigen. |
| [!UICONTROL Suffix Dropdown Options] | Website | Definiert die Liste der Suffix-Optionen. Trennen Sie Werte mit einem Semikolon. Setzen Sie ein Semikolon vor den ersten Wert, um einen leeren Wert am Anfang der Liste anzuzeigen. |
| [!UICONTROL Show Telephone] | Website | Bestimmt, ob die Telefonnummer des Kunden im Namen- und Adressformular enthalten ist. Optionen: `No` / `Optional` / `Required` |
| [!UICONTROL Show Company] | Website | Bestimmt, ob das Unternehmen des Kunden im Namen- und Adressformular enthalten ist. Optionen: `No` / `Optional` / `Required` |
| [!UICONTROL Show Fax] | Website | Bestimmt, ob die Faxnummer des Kunden im Namen- und Adressformular enthalten ist. Optionen: `No` / `Optional` / `Required` |

{style="table-layout:auto"}

## [!UICONTROL Store Credit Options]

{{ee-feature}}

![Kreditoptionen speichern](./assets/customer-configuration-store-credit-options.png)<!-- zoom -->

<!-- [Store Credit Options](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/customer-accounts/store-credit/credit-configure) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable Store Credit Functionality] | Global | Legt fest, ob Gutschrift gespeichert wird. Durch Deaktivieren wird Filialguthaben aus Kundenkonten und von der Seite „Admin-Kunden verwalten“ entfernt. Optionen: `Yes` / `No`. |
| [!UICONTROL Show Store Credit History to Customers] | Website | Legt fest, ob der Saldenverlauf in Kundenkonten sichtbar ist. Optionen: `Yes` / `No`. |
| [!UICONTROL Refund Store Credit Automatically] | Global | Legt fest, ob die Rückerstattung automatisch ausgestellt wird. Optionen: `Yes` / `No` |
| [!UICONTROL Store Credit Update Email Sender] | Shop-Ansicht | Bestimmt die Store-Identität, die als Absender von an Kunden gesendeten Credit-Update-Benachrichtigungen angezeigt wird. |
| [!UICONTROL Store Credit Update Email Template] | Shop-Ansicht | Bestimmt die E-Mail-Vorlage, die für Bonitätsaktualisierungen verwendet wird. |

{style="table-layout:auto"}

## [!UICONTROL Login Options]

![Anmeldeoptionen](./assets/customer-configuration-login-options.png)<!-- zoom -->

<!-- [Login Options](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/customer-accounts/configure/login-landing-page) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Redirect Customer to Account Dashboard after Logging in] | Website | Legt fest, was passiert, nachdem sich Kunden bei ihren Konten angemeldet haben. Um Kunden zu ihrem Konto-Dashboard umzuleiten, wählen Sie `Yes` aus. Optionen: <br/>**`Yes`**- Das Konto-Dashboard wird angezeigt, wenn sich Kunden bei ihren Konten anmelden.<br/>**`No`** - Kunden können nach der Anmeldung bei ihren Konten weiter einkaufen. |

{style="table-layout:auto"}

## [!UICONTROL Address Templates]

![Adressvorlagen](./assets/customer-configuration-address-templates.png)<!-- zoom -->

<!-- [Address Templates](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/customer-accounts/attributes/address-templates) -->

| Vorlage | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Text] | Shop-Ansicht | Die Vorlage wird für alle gedruckten Adressen verwendet. |
| [!UICONTROL Text One Line] | Shop-Ansicht | Diese Vorlage definiert die Reihenfolge der Adressentitäten in der Adressbuchliste des Warenkorbs des Kunden. Fortschritt beim Auschecken. |
| [!UICONTROL HTML] | Shop-Ansicht | Diese Vorlage definiert die Reihenfolge der Adressfelder unter dem Bereich _Kundenadressen_ im Admin-Bedienfeld ([!UICONTROL Customers] > [!UICONTROL Manage Customers]). Dies betrifft auch diejenigen auf der Seite _Neue Adresse hinzufügen_, wenn ein Kunde eine Rechnungs- oder Versandadresse auf seiner Kontoseite erstellt. |
| [!UICONTROL PDF] | Shop-Ansicht | Die Vorlage definiert die Anzeige von Rechnungs- und Lieferadressen in den gedruckten Rechnungen, Lieferungen und Gutschriften. |

{style="table-layout:auto"}

## [!UICONTROL Customer Segments]

{{ee-feature}}

![Kundensegmente](./assets/customer-configuration-customer-segments.png)<!-- zoom -->

<!-- [Customer Segments](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/segments/customer-segments) -->

| Vorlage | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable Customer Segment Functionality] | Global | Legt fest, ob Kundensegmente zum Erstellen zielgerichteter Promotions verwendet werden können. Optionen: `Yes` / `No` |
| [!UICONTROL Real-time Check if Customer is Matched by Segment] | Global | Bestimmt, ob Kundensegmente in Echtzeit validiert werden. Optionen: <br/>**[!UICONTROL Yes]**- Kundensegmente werden in Echtzeit validiert (Standardwert).<br/>**[!UICONTROL No]** - Kundensegmente werden durch eine einzige kombinierte SQL-Abfrage mit Bedingungen validiert. Dies verbessert die Leistung der Segmentvalidierung, wenn im System viele Kundensegmente vorhanden sind. Die Validierung funktioniert jedoch nicht mit einer geteilten Datenbank oder wenn keine registrierten Kunden vorhanden sind. |

{style="table-layout:auto"}

## [!UICONTROL CAPTCHA]

![CAPTCHA](./assets/customer-configuration-captcha.png)<!-- zoom -->

<!-- [CAPTCHA](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/security/captcha/security-captcha) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable CAPTCHA on Storefront] | Website | Aktiviert CAPTCHA in den Stores, die mit der Commerce-Website verknüpft sind. Optionen: `Yes` / `No` |
| [!UICONTROL Font] | Website | Bestimmt die Schriftart, die für die Anzeige von CAPTCHA verwendet wird. Um Ihre eigene Schriftart hinzuzufügen, fügen Sie die Schriftartdatei in dasselbe Verzeichnis wie Ihre Commerce-Installation ein und fügen Sie die Deklaration zur `config.xml` unter `app/code/Magento/Captcha/etc` hinzu. |
| [!UICONTROL Forms] | Website | Bestimmt die Formulare, in denen CAPTCHA verwendet wird. Optionen: <br />`Applying Coupon Code` <br />`Checkout/Placing Order`<br />`Create user` <br />`Login` <br />`Forgot password` <br />`Contact Us` <br />`Change password` <br />`Share Wishlist Form` <br />`Send to Friend Form` <br />`Payflow Pro` (siehe [Sicherheits-Patch](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/payments/paypal-payflow-pro-active-carding-activity.html)) <br />`Add Gift Card Code` ![&#128279;](../../assets/adobe-logo.svg) ![Adobe Commerce<br />`Create company` ](../../assets/adobe-logo.svg) Adobe Commerce <br /><br />_&#x200B;**Hinweis:**&#x200B;_ Die Formulare „Benutzer erstellen“, „Kennwort vergessen“ und „Payflow Pro“ sind immer aktiviert, wenn sie ausgewählt sind. |
| [!UICONTROL Displaying Mode] | Website | Bestimmt, wann das CAPTCHA angezeigt wird. Optionen: <br/>**`Always`**- CAPTCHA ist immer für die Anmeldung erforderlich.<br/>**`After number of attempts to login`** - Diese Option gilt nur für das Admin-Anmeldeformular. Wenn diese Option ausgewählt ist, wird das Feld _[!UICONTROL Number of Unsuccessful Attempts to Login]_&#x200B;angezeigt. Geben Sie die Anzahl der Anmeldeversuche ein, die Sie zulassen möchten. Ein Wert von `0` (Null) ist ähnlich wie das Festlegen von [!UICONTROL Displaying Mode] auf `Always`.<br/>_&#x200B;**Hinweis:**&#x200B;_Um die Anzahl erfolgloser Anmeldeversuche zu verfolgen, wird jeder Anmeldeversuch unter einer E-Mail-Adresse und von einer IP-Adresse gezählt. Die maximale Anzahl von Anmeldeversuchen, die von derselben IP-Adresse aus zulässig sind, beträgt 1.000. Diese Einschränkung gilt nur, wenn CAPTCHA aktiviert ist. |
| [!UICONTROL Number of Unsuccessful Attempts to Login] | Website | Gibt an, wie oft sich ein Kunde anmelden kann, bevor das Konto gesperrt wird. |
| [!UICONTROL CAPTCHA Timeout (minutes)] | Website | Bestimmt die Lebensdauer des aktuellen CAPTCHA. Wenn das CAPTCHA abläuft, muss der Benutzer die Seite neu laden. |
| [!UICONTROL Number of Symbols] | Website | Bestimmt die Anzahl der Symbole, die im CAPTCHA angezeigt werden, mit maximal 8. Sie können auch einen Bereich angeben, z. B. 5-8. |
| [!UICONTROL Symbols Used in CAPTCHA] | Website | Bestimmt die Buchstaben (a-z und A-Z) und Zahlen (0-9), die im CAPTCHA angezeigt werden. Symbole, die nur schwer von anderen Symbolen wie `i`, `l` oder `1` zu unterscheiden sind, sind nicht im Standardsatz von CAPTCHA-Symbolen enthalten. |
| [!UICONTROL Case Sensitive] | Website | Bestimmt, ob bei CAPTCHA-Zeichen zwischen Groß- und Kleinschreibung unterschieden wird. Optionen: `Yes` / `No` |

{style="table-layout:auto"}
