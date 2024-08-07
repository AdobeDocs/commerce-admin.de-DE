---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] &gt; [!UICONTROL PayPal Payments Advanced]'
description: Überprüfen Sie die Konfigurationseinstellungen im Abschnitt [!UICONTROL PayPal Payments Advanced] auf der Seite [!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] des Commerce-Administrators.
exl-id: c9159408-fbdf-4146-8292-9952cd5d01fa
feature: Configuration, Payments
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '1280'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] > [!UICONTROL PayPal Payments Advanced]

>[!IMPORTANT]
>
>**Anforderungen an PSD2:** <br/>
>Ab dem 14. September 2019 könnten europäische Banken Zahlungen ablehnen, die nicht den Anforderungen von [PSD2](../../getting-started/compliance-payment-services-directive.md) entsprechen. Um PSD2 zu erfüllen, muss [!DNL PayPal Payments Advanced] in [!DNL Cardinal Commerce] integriert sein. Weitere Informationen finden Sie unter [3-D Secure for Payflow](https://developer.paypal.com/api/nvp-soap/payflow/3d-secure-overview/).

{{config}}

## [!UICONTROL Required Settings]

![Erforderliche Einstellungen](./assets/payment-methods-paypal-payments-advanced-required.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Email Associated with PayPal Merchant Account] | Webseite | (Optional) Alle E-Mail-Adressen, die mit Ihrem PayPal-Handelskonto verknüpft sind. Bei E-Mail-Adressen muss die Groß-/Kleinschreibung beachtet werden und die Adressen müssen exakt mit denen in Ihrem Konto übereinstimmen. |
| [!UICONTROL Partner] | Webseite | gegebenenfalls Ihre PayPal-Partner-ID. |
| [!UICONTROL Vendor] | Webseite | Ihr PayPal-Benutzername. |
| Benutzer | Webseite | Die ID eines anderen Benutzers in Ihrem PayPal-Konto. |
| [!UICONTROL Password] | Webseite | Das Kennwort, das Ihrem PayPal-Kaufkonto zugeordnet ist. |
| [!UICONTROL Test Mode] | Webseite | Wenn diese Option aktiviert ist, wird PayPal Payments Advanced in einer Testumgebung ausgeführt. Deaktivieren Sie den Testmodus, wenn Sie bereit sind, im Produktionsmodus live zu gehen. Optionen: `Yes` / `No` |
| [!UICONTROL Use Proxy] | Webseite | Ein Proxy kann verwendet werden, um den Traffic umzuleiten, wenn die Server-Firewall den direkten Zugriff auf den PayPal-Server verhindert. Gibt ggf. den Proxy-Server an, der zum Herstellen einer Verbindung mit dem PayPal-Server verwendet wird. Optionen: `Yes` / `No` <br/><br/>Legen Sie bei Aktivierung die Optionen fest: <br/>**`Proxy Host`**- Die IP-Adresse des Proxyhosts.<br/>**`Proxy Port`** - Die Nummer des Proxy-Ports. |
| [!UICONTROL Enable this Solution] | Webseite | Stellt fest, ob PayPal Payments Advanced Ihren Kunden als Zahlungsmethode zur Verfügung steht. |
| [!UICONTROL Enable PayPal Credit] | Webseite | Stellt fest, ob PayPal-Guthaben Ihren Kunden als Zahlungsoption zur Verfügung steht. |

{style="table-layout:auto"}

## [!UICONTROL Advertise PayPal Credit]

![PayPal-Guthaben für Werbung](./assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Publisher ID] | Webseite | Die Herausgeber-ID, die Ihrem PayPal-Konto zugeordnet ist. |
| [!UICONTROL Get Publisher ID from PayPal] |  | Ruft Ihre Herausgeber-ID von PayPal ab. |
| [!UICONTROL Home Page] | Webseite | Bestimmt die Position und Größe des [!DNL PayPal Credit] -Banners auf der Startseite. Optionen: <br/>**`Display`**- Bestimmt, ob ein [!DNL PayPal Credit] -Banner auf der Startseite Ihres Stores angezeigt wird. Optionen: `Yes` / `No`<br/>**`Position`** - Bestimmt die Position des [!DNL PayPal Credit] -Banners auf der Startseite. Optionen: Kopfzeile (zentriert) / Seitenleiste (rechts) <br/>**`Size`**- Legt die Größe des [!DNL PayPal Credit] -Banners auf der Startseite fest. Optionen: `190 x 100` / `234 x 60` / `300 x 50` / `468 x 60` / `728 x 90` /` 800 x 66` |
| [!UICONTROL Catalog Category Page] | Webseite | Bestimmt die Position und Größe des [!DNL PayPal Credit] -Banners auf Kategorieseiten. Optionen: (wie für [!UICONTROL Home Page]) |
| [!UICONTROL Catalog Product Page] | Webseite | Bestimmt die Position und Größe des [!DNL PayPal Credit] -Banners auf Produktseiten. Optionen: (wie für [!UICONTROL Home Page]) |
| [!UICONTROL Checkout Cart Page] | Webseite | Bestimmt die Position und Größe des [!DNL PayPal Credit] -Banners auf der Warenkorbseite. Optionen: (wie für [!UICONTROL Home Page]) |

{style="table-layout:auto"}

## [!UICONTROL Basic Settings]

![Grundlegende Einstellungen](./assets/payment-methods-paypal-payments-advanced-basic-settings.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Title] | Store-Ansicht | Ein Name, der PayPal Payments Advanced als Zahlungsmethode beim Checkout angibt. |
| [!UICONTROL Sort Order] | Store-Ansicht | Eine Zahl, die bestimmt, in welcher Reihenfolge PayPal Payments Advanced angezeigt wird, wenn sie beim Checkout mit anderen Zahlungsmethoden aufgeführt wird. |
| [!UICONTROL Payment Action] | Webseite | Legt fest, welche Aktion von PayPal bei der Absendung einer Bestellung durchgeführt wird. Optionen: <br/>**`Authorization`**- Genehmigt den Kauf, legt jedoch einen Halten für die Fonds fest. Der Betrag wird erst dann zurückgezogen, wenn er vom Händler &quot;erfasst&quot;wurde.<br/>**`Sale`** - Der Betrag des Kaufs wird genehmigt und sofort vom Konto des Kunden zurückgezogen. |

{style="table-layout:auto"}

## [!UICONTROL Advanced Settings]

![Erweiterte Einstellungen](./assets/paypal-advanced-settings2.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Payment Applicable From] | Webseite | Bestimmt den Bereich der entsprechenden Länderauswahl. Optionen: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Countries Payment Applicable From] | Webseite | Identifiziert jedes Land, aus dem die Zahlung akzeptiert wird. Mit dieser Zahlungsmethode können nur Kunden mit einer Rechnungsadresse in einem ausgewählten Land Einkäufe tätigen. |
| [!UICONTROL Debug Mode] | Webseite | Zeichnet die zwischen Ihrem Geschäft und dem Zahlungssystem gesendeten Nachrichten in einer Protokolldatei auf. Optionen: `Yes` / `No` <br/><br/>**_Hinweis:_**Die Protokolldatei wird auf dem Server gespeichert und steht nur Entwicklern zur Verfügung. Gemäß PCI Data Security Standards werden Kreditkarteninformationen nicht in der Protokolldatei aufgezeichnet. |
| [!UICONTROL Enable SSL Verification] | Webseite | Bestimmt, ob der sichere Kanal auf dem Host vor einer Transaktion überprüft wird. Optionen: `Yes` / `No` |
| [!UICONTROL CVV Entry is Editable] | Webseite | Stellt fest, ob der Kunde das CVV bearbeiten kann, nachdem es eingegeben wurde. Optionen: `Yes` / `No` |
| [!UICONTROL Require CVV Entry] | Webseite | Bestimmt, ob Kunden den CVV-Code von der Rückseite ihrer Kreditkarte aus eingeben müssen. Optionen: `Yes` / `No` |
| [!UICONTROL Send Email Confirmation] | Webseite | Bestimmt, ob der Kunde eine E-Mail-Bestätigung der Zahlung erhält. Optionen: `Yes` / `No` |
| [!UICONTROL URL Method for Cancel URL and Return URL] | Webseite | Bestimmt die Methode, die zum Austausch von Informationen mit dem PayPal-Server während einer Transaktion verwendet wird. Optionen: <br/>**`GET`**- Ruft Informationen ab, die das Ergebnis eines Prozesses sind. (Dies ist die Standardmethode.)<br/>**`POST`** - Sendet einen Datenblock, z. B. die in ein Formular eingegebenen Daten, an den Datenverarbeitungsprozess. |

{style="table-layout:auto"}

## [!UICONTROL Settlement Report Settings]

![Berichtseinstellungen festlegen](./assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| **[!UICONTROL SFTP Credentials]** |  |  |
| [!UICONTROL Login] | Webseite | Ihr Benutzername, der zum Anmelden beim sicheren FTP-Server von PayPal erforderlich ist. |
| [!UICONTROL Password] | Webseite | Ihr Kennwort, das zum Anmelden beim sicheren FTP-Server von PayPal erforderlich ist. |
| [!UICONTROL Sandbox Mode] | Webseite | Wenn diese Option aktiviert ist, werden Berichte in einer Testumgebung ausgeführt, bevor sie in der Produktionsumgebung live geschaltet werden. Optionen: `Yes` / `No` |
| [!UICONTROL Custom Endpoint Hostname or IP-Address] | Webseite | Die URL, unter der Abwicklungsberichte verwaltet werden. Standardwert: `reports.paypal.com` |
| [!UICONTROL Custom Path] | Webseite | Der Pfad, unter dem die Abwicklungsberichte auf Ihrem Server gespeichert werden. Standardwert: `/ppreports/outgoing` |
| **[!UICONTROL Scheduled Fetching]** |  |  |
| [!UICONTROL Enable Automatic Fetching] | Webseite | Wenn diese Option aktiviert ist, werden die Vergleichsberichte automatisch nach Zeitplan abgerufen. Optionen: `Yes` / `No` |
| [!UICONTROL Schedule] | Global | Bestimmt, wie oft Vergleichsberichte von PayPal generiert werden. Optionen: `Daily` / `Every 3 days` / `Every 7 days` / `Every 10 days` / `Every 14 days` / `Every 30 days` / `Every 40 days` |
| [!UICONTROL Time of Day] | Global | Bestimmt die Stunde, Minute und Sekunde, in der die Vergleichsberichte generiert werden. |

{style="table-layout:auto"}

## [!UICONTROL Frontend Experience Settings]

![Frontend-Erlebniseinstellungen](./assets/payment-methods-paypal-payments-advanced-frontend-experience-settings.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL PayPal Product Logo] | Store-Ansicht | Bestimmt das PayPal-Logo, das in Ihrem Store angezeigt wird. Es gibt vier grundlegende Stile in zwei Größen. Optionen: `No Logo` / `We prefer PayPal (150 x 60)` / `We prefer PayPal (150 x 40)` / `Now accepting PayPal (150 x 60)` / `Now accepting PayPal (150 x 40)` / `Payments by PayPal (150 x 60)` / `Payments by PayPal (150 x 40)` / `Shop now using (150 x 60)` / `Shop now using (150 x 40)` |
| **[!UICONTROL PayPal Merchant Pages Style]** |  |  |
| [!UICONTROL Page Style] | Store-Ansicht | Bestimmt das Erscheinungsbild Ihrer PayPal-Kaufseite. Zulässige Werte: <br/>**`paypal`**- Verwendet den PayPal-Seitenstil.<br/>**`primary`** - Verwendet den Seitenstil, den Sie in Ihrem Kontoprofil als &quot;primär&quot;identifiziert haben. <br/>**`your_custom_value`**- Verwendet einen benutzerdefinierten Zahlungsseitenstil, der in Ihrem Kontoprofil angegeben ist. |
| [!UICONTROL Header Image URL] | Store-Ansicht | Die URL des Bildes, das in der oberen linken Ecke der Checkout-Seite angezeigt wird. Die maximale Größe beträgt 750 x 90 Pixel. <br/><br/>**_Hinweis:_**PayPal empfiehlt, dass das Bild auf einem sicheren (HTTPS-)Server gespeichert wird. Andernfalls kann der Browser des Kunden warnen, dass &quot;die Seite sowohl sichere als auch nicht sichere Elemente enthält&quot;. |
| [!UICONTROL Header Image Background Color] | Store-Ansicht | Der sechsstellige Code [hexadezimale Farbe](https://en.wikipedia.org/wiki/Web_colors) für die Hintergrundfarbe der Kopfzeile auf der Checkout-Seite. Sie können den Code in Groß- und Kleinbuchstaben eingeben. |
| [!UICONTROL Header Image Border Color] | Store-Ansicht | Der sechsstellige hexadezimale Farbcode für den zweiPixelrahmen um die Kopfzeile. |
| [!UICONTROL Page Background Color] | Store-Ansicht | Der sechsstellige hexadezimale Farbcode für die Hintergrundfarbe der Checkout-Seite, der hinter der Kopfzeile und dem Zahlungsformular angezeigt wird. |

{style="table-layout:auto"}

## [!UICONTROL Basic Settings - PayPal Express Checkout]

![PayPal Express Checkout - Grundlegende Einstellungen](./assets/payment-methods-paypal-advanced-express-checkout-basic-settings.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Title] | Store-Ansicht | Ein Name, der die Zahlungsmethode PayPal Express Checkout beim Checkout angibt. |
| [!UICONTROL Sort Order] | Store-Ansicht | Eine Zahl, die bestimmt, in welcher Reihenfolge PayPal Express Checkout angezeigt wird, wenn es beim Checkout mit anderen Zahlungsmethoden aufgeführt wird. Geben Sie oben in der Liste `0` ein. |
| [!UICONTROL Payment Action] | Webseite | Bestimmt die Aktion, die PayPal beim Erhalt einer Bestellung durchführt. Optionen: <br/>**`Authorization`**- Genehmigt den Kauf, legt jedoch einen Halten für die Fonds fest. Der Betrag wird erst dann zurückgezogen, wenn er vom Händler &quot;erfasst&quot;wurde.<br/>**`Sale`** - Der Betrag des Kaufs wird genehmigt und sofort vom Konto des Kunden zurückgezogen. <br/>**`Order`**- Stellt einen Vertrag mit PayPal dar, der es dem Händler ermöglicht, innerhalb eines bestimmten Zeitraums einen oder mehrere Beträge bis zum bestellten Gesamtbetrag aus dem Käuferkonto des Kunden zu erfassen. Dies kann bis zu 29 Tage dauern. Eine oder mehrere Rechnungen müssen vom Commerce-Administrator erstellt werden, um die Mittel zu erfassen. |
| [!UICONTROL URL Display on Product Details Page] | Store-Ansicht | Bestimmt, ob die Schaltfläche &quot;Checkout mit PayPal&quot;auf Produktseiten angezeigt wird. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL PayPal Express Checkout - Advanced Settings]

![PayPal Express Checkout - Erweiterte Einstellungen](./assets/payment-methods-paypal-payments-advanced-express-checkout-advanced.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Display on Shopping Cart] | Store-Ansicht | Bestimmt, ob PayPal Express Checkout als Zahlungsoption im Warenkorb angezeigt wird. Optionen: `Yes` (empfohlen) / `No` |
| [!UICONTROL Payment Action Applicable From] | Webseite | Bestimmt den Bereich der entsprechenden Länderauswahl. Optionen: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Countries Payment Applicable From] | Webseite | Identifiziert jedes Land, aus dem die Zahlung akzeptiert wird. Mit dieser Zahlungsmethode können nur Kunden mit einer Rechnungsadresse in einem ausgewählten Land Einkäufe tätigen. |
| [!UICONTROL Debug Mode] | Webseite | Zeichnet die zwischen Ihrem Store und dem PayPal Zahlungssystem gesendeten Nachrichten in einer Protokolldatei auf. Optionen: `Yes` / `No` <br/><br/>**_Hinweis:_**Die Protokolldatei wird auf dem Server gespeichert und steht nur Entwicklern zur Verfügung. Gemäß PCI Data Security Standards werden Kreditkarteninformationen nicht in der Protokolldatei aufgezeichnet. |
| [!UICONTROL Enable SSL Verification] | Webseite | Aktiviert die Überprüfung des Host-Sicherheitszertifikats. Optionen: `Yes` / `No` |
| [!UICONTROL Transfer Cart Line Items] | Webseite | Zeigt eine vollständige Zusammenfassung der Zeileneinträge aus dem Warenkorb des Kunden auf der PayPal-Site an. Optionen: `Yes` / `No` |
| [!UICONTROL Skip Order Review Step] | Webseite | Bestimmt, ob Kunden die Transaktion von der PayPal-Site aus abschließen können oder dazu verpflichtet sind, zu Ihrem Store zurückzukehren und den Schritt &quot;Bestellprüfung&quot;abzuschließen, bevor die Bestellung gesendet wird. Optionen: `Yes` / `No` |

{style="table-layout:auto"}
