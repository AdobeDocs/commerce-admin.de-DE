---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] &gt; [!UICONTROL PayPal Express Checkout]'
description: Überprüfen Sie die Konfigurationseinstellungen im Abschnitt [!UICONTROL PayPal Express Checkout] im Abschnitt [!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] Seite des Commerce-Administrators.
exl-id: aae5b1d9-f47e-447a-b40c-924f8d2ee824
feature: Configuration, Payments
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '1735'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] > [!UICONTROL PayPal Express Checkout]

>[!IMPORTANT]
>
>**PSD2-Anforderungen:** <br/>
>Ab dem 14. September 2019 könnten europäische Banken Zahlungen ablehnen, die nicht erfüllt sind [PSD2](../../getting-started/compliance-payment-services-directive.md) Anforderungen. Für PayPal Express Checkout ist kein Eingreifen erforderlich, um PSD 2 zu erfüllen, da alle Anforderungen von PayPal erfüllt werden.

{{config}}

## [!UICONTROL Required PayPal Settings]

![PayPal Express Checkout - Erforderliche Einstellungen](./assets/paypal-express-required-settings.png)<!-- zoom -->

<!-- [PayPal Express Checkout Required Settings](../../stores-purchase/paypal-express-checkout.html) -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable this Solution] | Webseite | Aktiviert [!DNL PayPal Express Checkout] als Zahlungsmethode, die Ihren Kunden zur Verfügung steht. Optionen: `Yes` / `No` |
| [!UICONTROL Enable In-Context Checkout Experience] | Webseite | Aktiviert optimierte PayPal In-Context Checkout als Zahlungsmethode, die Ihren Kunden zur Verfügung steht. Optionen: `Yes` / `No` |
| [!UICONTROL Enable PayPal Credit] | Webseite | Aktiviert PayPal Credit, damit Kunden jetzt kaufen können, aber später zahlen können. Sie erhalten zwar vorab bezahlt, aber die Kunden haben mehr Zeit zu bezahlen. Optionen: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

### [!UICONTROL Express Checkout]

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Email Associated with PayPal Merchant Account] | Webseite | Gibt die E-Mail-Adresse an, die Sie bei der Einrichtung Ihres PayPal-Kaufkontos angegeben haben. Bei der E-Mail-Adresse wird zwischen Groß- und Kleinschreibung unterschieden und sie muss genau mit Ihrer E-Mail-Adresse im PayPal-System übereinstimmen. |
| [!UICONTROL API Authentication Methods] | Webseite | Bestimmt die für die API-Authentifizierung verwendete Methode. Optionen: <br/>**`API Signature`**- Zeigt die _[!UICONTROL API Signature]_im Formular ein.<br/>**`API Certificate`**- Zeigt die_[!UICONTROL API Certificate]_ im Formular ein. |
| [!UICONTROL API Username] | Webseite | Der API-Benutzername, der mit Ihrem PayPal-Handelskonto verknüpft ist. |
| [!UICONTROL API Password] | Webseite | Das API-Kennwort, das mit Ihrem PayPal-Kaufkonto verknüpft ist. |
| [!UICONTROL API Signature] | Webseite | Die API-Signatur, die mit Ihrem PayPal-Handelskonto verknüpft ist. |
| [!UICONTROL API Certificate] | Webseite | Navigieren Sie zu , um Ihr API-Zertifikat hochzuladen. |
| [!UICONTROL Get Credentials from PayPal] |  | Ruft Ihre API-Anmeldeinformationen von PayPal ab. |
| [!UICONTROL Sandbox Credentials] |  | Ruft Ihre Sandbox-Anmeldeinformationen von PayPal ab. |
| [!UICONTROL Sandbox Mode] | Webseite | Um PayPal Express Checkout in einer Testumgebung auszuführen, geben Sie Ihre Sandbox-API-Anmeldeinformationen ein und setzen Sie dies auf `Yes`. Optionen: `Yes` / `No` |
| [!UICONTROL API Uses Proxy] | Webseite | Wenn Ihr System einen Proxy-Server verwendet, um die Verbindung zwischen Commerce und dem PayPal-System herzustellen, setzen Sie dies auf `Yes`. Optionen: `Yes` / `No` |
| [!UICONTROL Proxy Host] | Webseite | Wenn die API einen Proxy verwendet, gibt dies die IP-Adresse des Proxy-Hosts an. |
| [!UICONTROL Proxy Port] | Webseite | Wenn die API einen Proxy verwendet, gibt dies den vom Proxy-Host verwendeten Port an. |

{:style=&quot;table-layout:auto&quot;}

### [!UICONTROL Advertise PayPal Credit]

![Advertise PayPal Credit](./assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png)<!-- zoom -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Publisher ID] | Webseite | Die Herausgeber-ID, die Ihrem PayPal-Konto zugeordnet ist. |
| [!UICONTROL Get Publisher ID from PayPal] |  | Ruft Ihre Herausgeber-ID von PayPal ab. |
| [!UICONTROL Home Page] | Webseite | Bestimmt die Position und Größe der [!DNL PayPal Credit] Banner auf der Startseite. Optionen: <br/>**Anzeige** - Zeigt eine[!DNL PayPal Credit] Banner auf der Startseite Ihres Stores. Optionen: `Yes` / `No` <br/>**Position** - Bestimmt die Position der [!DNL PayPal Credit] Banner auf der Startseite. Optionen: Kopfzeile (zentriert)/Seitenleiste (rechts) <br/>**Größe** - Bestimmt die Größe der [!DNL PayPal Credit] Banner auf der Startseite. Optionen: `190 x 100` / `234 x 60` / `300 x 50` / `468 x 60` / `728 x 90` /` 800 x 66` |
| [!UICONTROL Catalog Category Page] | Webseite | Bestimmt die Position und Größe der [!DNL PayPal Credit] Banner auf Kategorieseiten. Optionen: (entspricht für [!UICONTROL Home Page]) |
| [!UICONTROL Catalog Product Page] | Webseite | Bestimmt die Position und Größe der [!DNL PayPal Credit] Banner auf Produktseiten. Optionen: (entspricht für [!UICONTROL Home Page]) |
| [!UICONTROL Checkout Cart Page] | Webseite | Bestimmt die Position und Größe der [!DNL PayPal Credit] Banner auf der Warenkorbseite. Optionen: (entspricht für [!UICONTROL Home Page]) |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Basic Settings]

![Grundlegende Einstellungen](./assets/payment-methods-paypal-express-checkout-basic-settings.png)<!-- zoom -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Title] | Store-Ansicht | Ein Name, der die Zahlungsmethode PayPal Express Checkout beim Checkout angibt. |
| [!UICONTROL Sort Order] | Store-Ansicht | Eine Zahl, die bestimmt, in welcher Reihenfolge PayPal Express Checkout angezeigt wird, wenn es beim Checkout mit anderen Zahlungsmethoden aufgeführt wird. Eingabe `0` für den Anfang der Liste. |
| [!UICONTROL Payment Action] | Webseite | Bestimmt die Aktion, die PayPal beim Erhalt einer Bestellung durchführt. Optionen: <br/>**`Authorization`**- Genehmigt den Kauf, aber hält die Mittel fest. Der Betrag wird erst dann zurückgezogen, wenn er vom Händler &quot;erfasst&quot;wurde.<br/>**`Sale`** - Der Kaufbetrag wird genehmigt und sofort vom Konto des Kunden zurückgezogen. <br/>**`Order`**- Stellt einen Vertrag mit PayPal dar, der es dem Händler ermöglicht, innerhalb eines bestimmten Zeitraums einen oder mehrere Beträge bis zum bestellten Gesamtbetrag aus dem Käuferkonto des Kunden zu erfassen. Dies kann bis zu 29 Tage dauern. Eine oder mehrere Rechnungen müssen vom Commerce Admin erstellt werden, um die Mittel zu erfassen. |
| [!UICONTROL Display on Product Details Page] | Store-Ansicht | Bestimmt, ob die Schaltfläche &quot;Checkout mit PayPal&quot;auf Produktseiten angezeigt wird. Zu den Optionen gehören: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Advanced Settings]

![Erweiterte Einstellungen](./assets/payment-methods-paypal-express-checkout-advanced-settings.png)<!-- zoom -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Display on Shopping Cart] | Store-Ansicht | Bestimmt, ob PayPal Express Checkout als Zahlungsoption im Warenkorb angezeigt wird. Optionen: `Yes` (PayPal empfohlen) / `No` |
| [!UICONTROL Payment Action Applicable From] | Webseite | Bestimmt den Bereich der entsprechenden Länderauswahl. Optionen: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Countries Payment Applicable From] | Webseite | Identifiziert jedes Land, aus dem die Zahlung akzeptiert wird. Mit dieser Zahlungsmethode können nur Kunden mit einer Rechnungsadresse in einem ausgewählten Land Einkäufe tätigen. |
| [!UICONTROL Debug Mode] | Webseite | Zeichnet die zwischen Ihrem Geschäft und dem Zahlungssystem gesendeten Nachrichten in einer Protokolldatei auf. Optionen: `Yes` / `No` <br/><br/>**_Hinweis:_**Die Protokolldatei wird auf dem Server gespeichert und steht nur Entwicklern zur Verfügung. Gemäß PCI Data Security Standards werden Kreditkarteninformationen nicht in der Protokolldatei aufgezeichnet. |
| [!UICONTROL Enable SSL Verification] | Webseite | Aktiviert die Überprüfung des Host-Sicherheitszertifikats. Optionen: `Yes` / `No` |
| [!UICONTROL Transfer Cart Line Items] | Webseite | Zeigt eine vollständige Zusammenfassung der Zeileneinträge aus dem Warenkorb des Kunden auf der PayPal-Site an. Optionen: `Yes` / `No` |
| [!UICONTROL Transfer Shipping Options] | Webseite | Enthält bis zu zehn Versandoptionen auf der PayPal-Site. Optionen: `Yes` / `No` |
| [!UICONTROL Shortcut Buttons Flavor] | Store-Ansicht | Bestimmt den Typ des Bildes, das für die PayPal-Akzeptanzschaltfläche verwendet wird. Optionen: <br/>**`Dynamic`**- (Empfohlen) Zeigt ein Bild an, das dynamisch vom PayPal-Server aus geändert werden kann.<br/>**`Static`** - Zeigt ein statisches Bild an, das nicht dynamisch geändert werden kann. |
| [!UICONTROL Enable PayPal Guest Checkout] | Webseite | Ermöglicht Kunden, die keine PayPal-Konten haben, mit PayPal Express Checkout Einkäufe zu tätigen. Optionen: `Yes` / `No` |
| [!UICONTROL Require Customer's Billing Address] | Webseite | Bestimmt, ob die Rechnungsadresse des Kunden erforderlich ist. Optionen: `Yes` / `No` / `For Virtual Quotes Only` |
| [!UICONTROL Billing Agreement Signup] | Webseite | Stellt fest, ob Kunden in der Lage sind, [Abrechnungsvereinbarung](../../stores-purchase/paypal-billing-agreements.md) mit Ihrem Geschäft. Optionen: <br/>**`Auto`**- Der Kunde kann sich während des Express Checkout für eine Abrechnungsvereinbarung anmelden.<br/>**`Ask Customer`** - Der Kunde wird gefragt, ob er sich für eine Abrechnungsvereinbarung anmelden möchte. <br/>**`Never`**- Kunden wird nicht die Möglichkeit angeboten, sich für einen Abrechnungsvertrag zu registrieren. |
| [!UICONTROL Skip Order Review Step] | Webseite | Bestimmt, ob Kunden die Transaktion von der PayPal-Site aus abschließen können oder dazu verpflichtet sind, zu Ihrem Store zurückzukehren und den Schritt &quot;Bestellprüfung&quot;abzuschließen, bevor die Bestellung gesendet wird. Optionen: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

### [!UICONTROL Billing Agreement Settings]

![Rechnungsabschlussparameter](./assets/payment-methods-paypal-express-checkout-billing-agreement-settings.png)<!-- zoom -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enabled] | Webseite | Wenn diese Option aktiviert ist, erscheinen Abrechnungsvereinbarungen den Kunden während des Checkout als Zahlungsoption. Optionen: `Yes` / `No` |
| [!UICONTROL Title] | Store-Ansicht | Der Titel für die PayPal-Abrechnungsoption, die beim Checkout als Zahlungsoption angezeigt wird. |
| [!UICONTROL Sort Order] | Store-Ansicht | Bestimmt die Reihenfolge, in der Abrechnungsvereinbarungen während des Checkout mit anderen Zahlungsmethoden aufgelistet werden. |
| [!UICONTROL Payment Action] | Webseite | Bestimmt, wie PayPal die Transaktion verwaltet: Optionen: <br/>**Autorisierung** - Genehmigt den Kauf, aber hält die Mittel fest. Der Betrag wird erst dann zurückgezogen, wenn er vom Händler &quot;erfasst&quot;wurde. <br/>**Verkauf** - Der Kaufbetrag wird genehmigt und sofort vom Konto des Kunden zurückgezogen. |
| [!UICONTROL Payment Applicable From] | Webseite | Bestimmt den Bereich der entsprechenden Länderauswahl. Optionen: Alle zugelassenen Länder/spezifischen Länder |
| [!UICONTROL Countries Payment Applicable From] | Webseite | Identifiziert jedes Land, aus dem die Zahlung akzeptiert wird. Mit dieser Zahlungsmethode können nur Kunden mit einer Rechnungsadresse in einem ausgewählten Land Einkäufe tätigen. |
| [!UICONTROL Debug Mode] | Webseite | Zeichnet die Kommunikation mit dem Zahlungssystem in einer Protokolldatei auf. Optionen: `Yes` / `No` <br/><br/>**_Hinweis:_**Die Protokolldatei wird auf dem Server gespeichert und steht nur Entwicklern zur Verfügung. Gemäß PCI Data Security Standards werden Kreditkarteninformationen nicht in der Protokolldatei aufgezeichnet. |
| [!UICONTROL Enable SSL Verification] | Webseite | Aktiviert einen Überprüfungsschritt zu , der sicherstellt, dass die Transaktion über einen verschlüsselten SSL-Kanal erfolgt. Optionen: `Yes` / `No` |
| [!UICONTROL Transfer Cart Line Items] | Webseite | Wenn diese Option aktiviert ist, zeigt eine Zusammenfassung der Zeileneinträge aus dem Warenkorb auf Ihrer PayPal-Zahlungsseite an. Optionen: `Yes` / `No` |
| [!UICONTROL Allow in Billing Agreement Wizard] | Webseite | Wenn diese Option aktiviert ist, können Kunden über das Dashboard ihres Kundenkontos eine Abrechnungsvereinbarung einleiten. |

{:style=&quot;table-layout:auto&quot;}

### [!UICONTROL Settlement Report Settings]

![Berichtseinstellungen einrichten](./assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png)<!-- zoom -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| **[!UICONTROL SFTP Credentials]** |  |  |
| [!UICONTROL Login] | Webseite | Ihr Benutzername, der zum Anmelden beim sicheren FTP-Server von PayPal erforderlich ist. |
| [!UICONTROL Password] | Webseite | Ihr Kennwort, das zum Anmelden beim sicheren FTP-Server von PayPal erforderlich ist. |
| [!UICONTROL Sandbox Mode] | Webseite | Wenn diese Option aktiviert ist, werden Berichte in einer Testumgebung ausgeführt, bevor sie in der Produktionsumgebung live geschaltet werden. Optionen: `Yes` / `No` |
| [!UICONTROL Custom Endpoint Hostname or IP-Address] | Webseite | Die URL, unter der Abwicklungsberichte verwaltet werden. Standardwert: `reports.paypal.com` |
| [!UICONTROL Custom Path] | Webseite | Der Pfad, unter dem die Abwicklungsberichte auf Ihrem Server gespeichert werden. Standardwert: `/ppreports/outgoing` |
| **[!UICONTROL Scheduled Fetching]** |  |  |
| [!UICONTROL Enable Automatic Fetching] | Webseite | Wenn diese Option aktiviert ist, werden die Vergleichsberichte automatisch nach Zeitplan abgerufen. Optionen: `Yes` / `No` |
| [!UICONTROL Schedule] | Webseite | Bestimmt, wie oft Vergleichsberichte von PayPal generiert werden. Optionen: `Daily` / `Every 3 days` / `Every 7 days` / `Every 10 days` / `Every 14 days` / `Every 30 days` / `Every 40 days` |
| [!UICONTROL Time of Day] | Webseite | Bestimmt die Stunde, Minute und Sekunde, in der die Vergleichsberichte generiert werden. |

{:style=&quot;table-layout:auto&quot;}

### [!UICONTROL Frontend Experience Settings]

![Frontend-Erlebniseinstellungen - PayPal Merchant Pages-Stil](./assets/payment-methods-paypal-payments-advanced-frontend-experience-settings1.png)<!-- zoom -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL PayPal Product Logo] | Store-Ansicht | Bestimmt das PayPal-Logo, das in Ihrem Store angezeigt wird. Es gibt vier grundlegende Stile in zwei Größen. Optionen: `No Logo` / `We prefer PayPal (150 x 60)` / `We prefer PayPal (150 x 40)` / `Now accepting PayPal (150 x 60)` / `Now accepting PayPal (150 x 40)` / `Payments by PayPal (150 x 60)` / `Payments by PayPal (150 x 40)` / `Shop now using (150 x 60)` / `Shop now using (150 x 40)` |
| **[!UICONTROL PayPal Merchant Pages Style]** |  |  |
| [!UICONTROL Page Style] | Store-Ansicht | Bestimmt das Erscheinungsbild Ihrer PayPal-Kaufseite. Zulässige Werte: **`paypal`** - Verwendet den PayPal-Seitenstil. <br/>**`primary`**- Verwendet den Seitenstil, den Sie in Ihrem Kontoprofil als &quot;primär&quot;identifiziert haben.<br/>**`your_custom_value`** - Verwendet einen benutzerdefinierten Zahlungsseitenstil, der in Ihrem Kontoprofil angegeben ist. |
| [!UICONTROL Header Image URL] | Store-Ansicht | Die URL des Bildes, das in der oberen linken Ecke der Checkout-Seite angezeigt wird. Die maximale Größe beträgt 750 x 90 Pixel. <br/><br/>**_Hinweis:_**PayPal empfiehlt, dass das Bild auf einem sicheren (HTTPS-)Server gespeichert wird. Andernfalls kann der Browser des Kunden warnen, dass &quot;die Seite sowohl sichere als auch nicht sichere Elemente enthält&quot;. |
| [!UICONTROL Header Image Background Color] | Store-Ansicht | Die sechs Zeichen [hexadezimale Farbe](https://en.wikipedia.org/wiki/Web_colors) Code für die Hintergrundfarbe der Kopfzeile auf der Checkout-Seite. Sie können den Code in Groß- und Kleinbuchstaben eingeben. |
| [!UICONTROL Header Image Border Color] | Store-Ansicht | Die sechs Zeichen [hexadezimale Farbe](https://en.wikipedia.org/wiki/Web_colors) -Code für den Rahmen von zwei Pixeln um die Kopfzeile. |
| [!UICONTROL Page Background Color] | Store-Ansicht | Die sechs Zeichen [hexadezimale Farbe](https://en.wikipedia.org/wiki/Web_colors) Code für die Hintergrundfarbe der Checkout-Seite, die hinter der Kopfzeile und dem Zahlungsformular angezeigt wird. |

{:style=&quot;table-layout:auto&quot;}

#### [!UICONTROL Customize Smart Buttons (Basic)]

![Frontend-Erlebniseinstellungen - Anpassen von Smart-Schaltflächen](./assets/payment-methods-paypal-payments-advanced-frontend-experience-settings2.png)<!-- zoom -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Customize Button] | Store-Ansicht | Bestimmt, ob die PayPal-Smart-Schaltflächen an das Layout und Design Ihres Stores angepasst werden können. Sie können diese Änderungen unabhängig auf die Checkout-Seite, die Produktseiten, die Warenkorbseite und den Warenkorb anwenden. |
| [!UICONTROL Label] | Store-Ansicht | Der Text, den PayPal auf der Schaltfläche Smart Payment anzeigt. Optionen: <br/>**`Checkout`**(wird als &quot;PayPal Checkout&quot;angezeigt)<br/>**`Pay`** (wird als &quot;PayPal&quot;angezeigt) <br/>**`Buy Now`**(wird als &quot;Jetzt mit PayPal kaufen&quot;angezeigt)<br/>**`PayPal`** (wird als &quot;PayPal&quot;angezeigt) <br/>**`Installment`**(wird als &quot;PayPal&quot;angezeigt)<br/>**`Credit`** (wird als &quot;PayPal CREDIT&quot;angezeigt) |
| [!UICONTROL Layout] | Store-Ansicht | Bestimmt, ob PayPal-Smart-Schaltflächen vertikal oder horizontal angezeigt werden. Optionen: <br/>**`Vertical`**- Der Käufer muss sich entweder bei PayPal anmelden oder ein PayPal-Konto erstellen, unabhängig davon, ob &quot;Gastkasse aktivieren&quot;ausgewählt ist.<br/>**`Horizontal`** - Wenn &quot;Gastauschecken aktivieren&quot;ausgewählt ist, zeigt das **`Pay with Debit Card or Credit Card`** im PayPal-Popup-Fenster. Andernfalls muss sich der Käufer entweder bei PayPal anmelden oder ein PayPal-Konto erstellen. |
| [!UICONTROL Size] | Store-Ansicht | Legt die Größe der Schaltfläche Smart Payment fest. Optionen: <br/>**`Medium`**- 250 Pixel x 35 Pixel<br/>**`Large`** - 350 Pixel x 40 Pixel <br/>**`Responsive`**- (Standard) Passt die Breite des Containers an. Die Mindestbreite beträgt 100 Pixel, die maximale Breite 500 Pixel. Die Höhe passt sich dynamisch an die Breite an. |
| [!UICONTROL Shape] | Store-Ansicht | Legt die Form der intelligenten Zahlungsschaltfläche fest. Optionen: `Pill` (Standard) / `Rectangle` |
| [!UICONTROL Color] | Store-Ansicht | Legen Sie die Farbe der Schaltfläche Smart Payment fest. Optionen: `Gold` (Standard) / `Blue` / `Silver` / `Black` |

{:style=&quot;table-layout:auto&quot;}

#### [!UICONTROL Customize Smart Buttons (Features)]

![Frontend-Erlebniseinstellungen - Anpassen von Smart-Schaltflächen (Funktionen)](./assets/payment-methods-paypal-payments-advanced-frontend-experience-settings3.png)<!-- zoom -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Disable Funding Options] | Store-Ansicht | Bestimmt, welche anderen PayPal-Finanzierungsoptionen auf der Seite &quot;Checkout&quot;angezeigt werden. Die ausgewählten Optionen werden nie auf der Seite &quot;Auschecken&quot;angezeigt. Nicht ausgewählte Optionen werden nur angezeigt, wenn PayPal die Währung des Stores und den Standort des Käufers unterstützt. Optionen: `PayPal Credit` / `PayPal Guest Checkout` `Credit Card Icons` / `Elektronisches Lastschriftverfahren - German ELV` |

{:style=&quot;table-layout:auto&quot;}
