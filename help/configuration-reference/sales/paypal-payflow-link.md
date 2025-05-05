---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] &gt; [!UICONTROL PayPal Payflow Link]'
description: Überprüfen Sie die Konfigurationseinstellungen im Abschnitt [!UICONTROL PayPal Payflow Link] auf der Seite [!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] der Commerce Admin Console.
exl-id: 5ea30b22-e251-4d93-be2c-d34138ef2f7d
feature: Configuration, Payments
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '1324'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] > [!UICONTROL PayPal Payflow Link]

>[!IMPORTANT]
>
>**PSD2-Anforderungen:** <br/>
>Ab dem 14. September 2019 können europäische Banken Zahlungen ablehnen, die [PSD2&rbrace;-](../../getting-started/compliance-payment-services-directive.md) nicht erfüllen. Um PSD2 zu erfüllen, müssen [!DNL PayPal Payflow Link] in [!DNL Cardinal Commerce] integriert sein. Weitere Informationen finden Sie unter [3-D Secure for Payflow](https://developer.paypal.com/api/nvp-soap/payflow/3d-secure-overview/).

{{config}}

## [!UICONTROL Required Settings]

![Erforderliche Einstellungen](./assets/paypal-payflow-link-settings.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Email Associated with PayPal Merchant Account] | Website | (Optional) Alle E-Mail-Adressen, die mit Ihrem PayPal-Händlerkonto verknüpft sind. Bei E-Mail-Adressen wird zwischen Groß- und Kleinschreibung unterschieden und sie müssen genau mit den Adressen in Ihrem Konto übereinstimmen. |
| [!UICONTROL Partner] | Website | Ihre PayPal Partner ID, falls zutreffend. |
| [!UICONTROL Vendor] | Website | Ihr PayPal-Benutzername. |
| Benutzer | Website | Die ID eines zusätzlichen Benutzers auf Ihrem PayPal-Konto. Wenn sich keine anderen Benutzer im Netzwerk befinden, geben Sie Ihre Anbieter- oder Händler-ID ein. |
| [!UICONTROL Password] | Website | Das Passwort, das Ihrem PayPal-Händlerkonto zugeordnet ist. |
| [!UICONTROL Test Mode] | Website | Nach der Aktivierung führt PayPal Payflow Pro in einer Testumgebung aus. Deaktivieren Sie den Testmodus, wenn Sie im Produktionsmodus bereit für die Live-Schaltung sind. Optionen: `Yes` / `No` |
| [!UICONTROL Use Proxy] | Website | Ein Proxy kann verwendet werden, um Traffic umzuleiten, wenn die Server-Firewall den direkten Zugriff auf den PayPal-Server verhindert. Gibt ggf. den Proxy-Server an, der zum Herstellen einer Verbindung mit dem PayPal-Server verwendet wird. Optionen: `Yes` / `No` <br/><br/>Wenn aktiviert, die Proxy-Optionen festlegen: <br/>**`Proxy Host`**- Die IP-Adresse des Proxy-Hosts.<br/>**`Proxy Port`** - Die Nummer des Proxy-Ports. |
| [!UICONTROL Enable Payflow Link] | Website | Bestimmt, ob PayPal Payflow Link für Ihre Kunden als Zahlungsmethode verfügbar ist. |
| [!UICONTROL Enable Express Checkout] | Website | Bestimmt, ob der PayPal Express-Checkout für Ihre Kunden als Zahlungsmethode verfügbar ist. |
| [!UICONTROL Enable PayPal Credit] | Website | Legt fest, ob Ihren Kunden PayPal-Guthaben als Zahlungsoption zur Verfügung steht. |

{style="table-layout:auto"}

## [!UICONTROL Advertise PayPal Credit]

![Advertise PayPal-Guthaben](./assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Publisher ID] | Website | Die mit Ihrem PayPal-Guthabenkonto verknüpfte Publisher-ID. |
| [!UICONTROL Get Publisher ID from PayPal] |  | Ruft Ihre Publisher-ID von PayPal ab. |
| [!UICONTROL Home Page] | Website | Bestimmt die Position und Größe des [!DNL PayPal Credit] auf der Startseite. Optionen: <br/>**`Display`**- Bestimmt, ob [!DNL PayPal Credit] Banner auf der Startseite Ihres Stores angezeigt wird. Optionen: `Yes` / `No`<br/>**`Position`** - Bestimmt die Position des [!DNL PayPal Credit] auf der Startseite. Optionen: Kopfzeile (Mitte) / Seitenleiste (rechts) <br/>**`Size`**- Bestimmt die Größe des [!DNL PayPal Credit] auf der Startseite. Optionen: `190 x 100` / `234 x 60` / `300 x 50` / `468 x 60` / `728 x 90` /` 800 x 66` |
| [!UICONTROL Catalog Category Page] | Website | Bestimmt die Position und Größe des [!DNL PayPal Credit] Banners auf Kategorieseiten. Optionen: (identisch mit [!UICONTROL Home Page]) |
| [!UICONTROL Catalog Product Page] | Website | Bestimmt die Position und Größe des [!DNL PayPal Credit] auf Produktseiten. Optionen: (identisch mit [!UICONTROL Home Page]) |
| [!UICONTROL Checkout Cart Page] | Website | Bestimmt die Position und Größe des [!DNL PayPal Credit] Banners auf der Warenkorbseite. Optionen: (identisch mit [!UICONTROL Home Page]) |

{style="table-layout:auto"}

### [!UICONTROL Basic Settings]

![Grundeinstellungen](./assets/payment-methods-paypal-payflow-link-basic-settings.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Title] | Shop-Ansicht | Ein Name, der PayPal Payflow Link während des Checkouts als Zahlungsmethode identifiziert. |
| [!UICONTROL Sort Order] | Shop-Ansicht | Eine Zahl, die die Reihenfolge bestimmt, in der der PayPal-Payflow-Link angezeigt wird, wenn er während des Checkouts mit anderen Zahlungsmethoden aufgelistet wird. |
| [!UICONTROL Payment Action] | Website | Bestimmt die Aktion, die PayPal bei der Übermittlung einer Bestellung durchführt. Optionen: <br/>**`Authorization`**- Genehmigt den Kauf, setzt jedoch die Mittel zurück. Der Betrag wird erst abgehoben, wenn er vom Händler „eingezogen“ wurde.<br/>**`Sale`** - Der Betrag des Kaufs wird autorisiert und sofort vom Konto des Kunden zurückgezogen. |

{style="table-layout:auto"}

### [!UICONTROL Advanced Settings]

![Erweiterte Einstellungen](./assets/payment-methods-paypal-payflow-link-advanced-settings.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Payment Applicable From] | Website | Bestimmt den Bereich der entsprechenden Länderauswahl. Optionen: Alle zulässigen Länder/bestimmte Länder |
| [!UICONTROL Countries Payment Applicable From] | Website | Gibt jedes Land an, aus dem die Zahlung akzeptiert wird. Nur Kunden mit einer Rechnungsadresse in einem ausgewählten Land können mit dieser Zahlungsmethode Einkäufe tätigen. |
| [!UICONTROL Debug Mode] | Website | Zeichnet Nachrichten, die zwischen Ihrem Geschäft und dem Zahlungssystem gesendet werden, in einer Protokolldatei auf. Optionen: `Yes` / `No` <br/><br/>**_Hinweis:_**&#x200B;Die Protokolldatei wird auf dem Server gespeichert und ist nur für Entwickler zugänglich. In Übereinstimmung mit den PCI Data Security Standards werden Kreditkarteninformationen nicht in der Protokolldatei aufgezeichnet. |
| [!UICONTROL Enable SSL Verification] | Website | Bestimmt, ob der sichere Kanal auf dem Host überprüft wird, bevor eine Transaktion stattfindet. Optionen: `Yes` / `No` |
| [!UICONTROL CVV Entry is Editable] | Website | Legt fest, ob der Kunde das CVV nach der Eingabe bearbeiten kann. Optionen: `Yes` / `No` |
| [!UICONTROL Require CVV Entry] | Website | Legt fest, ob Kunden den CVV-Code von der Rückseite ihrer Kreditkarte eingeben müssen. Optionen: `Yes` / `No` |
| [!UICONTROL Send Email Confirmation] | Website | Bestimmt, ob der Kunde eine E-Mail-Bestätigung der Zahlung erhält. Optionen: `Yes` / `No` |
| [!UICONTROL URL Method for Cancel  URL and Return URL] | Website | Bestimmt die Methode, die zum Austausch von Informationen mit dem PayPal-Server während einer Transaktion verwendet wird. Optionen: <br/>**`GET`**- Ruft Informationen ab, die das Ergebnis eines Prozesses sind. (Dies ist die Standardmethode.)<br/>**`POST`** - Sendet einen Datenblock, z. B. in ein Formular eingegebene Daten, an den Datenverarbeitungsprozess. |

{style="table-layout:auto"}

## [!UICONTROL Settlement Report Settings]

![Einstellungen für Abrechnungsberichte](./assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| **[!UICONTROL SFTP Credentials]** |  |  |
| [!UICONTROL Login] | Website | Ihr Benutzername, der zum Anmelden beim sicheren FTP-Server von PayPal erforderlich ist. |
| [!UICONTROL Password] | Website | Ihr Kennwort, das für die Anmeldung beim sicheren FTP-Server von PayPal erforderlich ist. |
| [!UICONTROL Sandbox Mode] | Website | Wenn diese Option aktiviert ist, führt Berichte in einer Testumgebung aus, bevor sie in der Produktionsumgebung „live“ geschaltet werden. Optionen: `Yes` / `No` |
| [!UICONTROL Custom Endpoint Hostname or IP-Address] | Website | Die URL, unter der Abwicklungsberichte verwaltet werden. Standardwert: `reports.paypal.com` |
| [!UICONTROL Custom Path] | Website | Der Pfad, unter dem Abrechnungsberichte auf Ihrem Server gespeichert werden. Standardwert: `/ppreports/outgoing` |
| **[!UICONTROL Scheduled Fetching]** |  |  |
| [!UICONTROL Enable Automatic Fetching] | Website | Wenn diese Option aktiviert ist, werden Abwicklungsberichte automatisch planmäßig abgerufen. Optionen: `Yes` / `No` |
| [!UICONTROL Schedule] | Global | Bestimmt, wie oft Abrechnungsberichte von PayPal generiert werden. Optionen: `Daily` / `Every 3 days` / `Every 7 days` / `Every 10 days` / `Every 14 days` / `Every 30 days` / `Every 40 days` |
| [!UICONTROL Time of Day] | Global | Bestimmt die Stunde, Minute und Sekunde, in der Abwicklungsberichte generiert werden. |

{style="table-layout:auto"}

## [!UICONTROL Frontend Experience Settings]

![Frontend-Erlebniseinstellungen](./assets/payment-methods-paypal-payments-advanced-frontend-experience-settings.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL PayPal Product Logo] | Shop-Ansicht | Bestimmt das PayPal-Logo, das in Ihrem Geschäft angezeigt wird. Es gibt vier grundlegende Stile in zwei Größen. Optionen: `No Logo` / `We prefer PayPal (150 x 60)` / `We prefer PayPal (150 x 40)` / `Now accepting PayPal (150 x 60)` / `Now accepting PayPal (150 x 40)` / `Payments by PayPal (150 x 60)` / `Payments by PayPal (150 x 40)` / `Shop now using (150 x 60)` / `Shop now using (150 x 40)` |
| PayPal-Stil für Händlerseiten |  |  |
| [!UICONTROL Page Style] | Shop-Ansicht | Bestimmt das Erscheinungsbild Ihrer PayPal-Händlerseite. Zulässige Werte: <br/>**`paypal`**- Verwendet den PayPal-Seitenstil.<br/>**`primary`** - Verwendet den Seitenstil, den Sie in Ihrem Kontoprofil als „primären“ Stil identifiziert haben. <br/>**`your_custom_value`**- Verwendet einen benutzerdefinierten Zahlungsseitenstil, der in Ihrem Kontoprofil angegeben ist. |
| [!UICONTROL Header Image URL] | Shop-Ansicht | Die URL des Bildes, das oben links auf der Kaufbestätigungsseite angezeigt wird. Die maximale Größe beträgt 750 x 90 Pixel. <br/><br/>**_Hinweis:_**&#x200B;PayPal empfiehlt, dass das Bild auf einem sicheren (https)-Server gespeichert wird. Andernfalls kann der Browser des Kunden warnen, dass „die Seite sowohl sichere als auch nicht sichere Elemente enthält“. |
| [!UICONTROL Header Image Background Color] | Shop-Ansicht | Der aus sechs Zeichen [Hexadezimalfarbe) bestehende ](https://en.wikipedia.org/wiki/Web_colors) für die Hintergrundfarbe des Headers auf der Kaufbestätigungsseite. Sie können den Code entweder in Groß- oder Kleinbuchstaben eingeben. |
| [!UICONTROL Header Image Border Color] | Shop-Ansicht | Der sechsstellige hexadezimale Farbcode für den Zwei-Pixel-Rahmen um die Kopfzeile. |
| [!UICONTROL Page Background Color] | Shop-Ansicht | Der sechsstellige hexadezimale Farbcode für die Hintergrundfarbe der Checkout-Seite, die hinter der Kopfzeile und dem Zahlungsformular angezeigt wird. |

{style="table-layout:auto"}

### [!UICONTROL Basic Settings - PayPal Express Checkout]

![PayPal Express Checkout - Grundeinstellungen](./assets/payment-methods-paypal-payflow-link-express-checkout-basic-settings.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Title] | Shop-Ansicht | Ein Name, der die Zahlungsmethode PayPal Express Checkout während des Checkouts identifiziert. |
| [!UICONTROL Sort Order] | Shop-Ansicht | Eine Zahl, die die Reihenfolge bestimmt, in der der PayPal Express-Checkout angezeigt wird, wenn er mit anderen Zahlungsmethoden während des Checkouts aufgeführt wird. Geben Sie `0` als Anfang der Liste ein. |
| [!UICONTROL Payment Action] | Website | Bestimmt die Aktion, die PayPal bei Erhalt einer Bestellung durchführt. Optionen: <br/>**`Authorization`**- Genehmigt den Kauf, setzt jedoch die Mittel zurück. Der Betrag wird erst abgehoben, wenn er vom Händler „eingezogen“ wurde.<br/>**`Sale`** - Der Betrag des Kaufs wird autorisiert und sofort vom Konto des Kunden zurückgezogen. <br/>**`Order`**- Stellt eine Vereinbarung mit PayPal dar, die es dem Händler ermöglicht, innerhalb eines bestimmten Zeitraums einen oder mehrere Beträge bis zur bestellten Summe vom Käuferkonto des Kunden zu erfassen. Dies kann bis zu 29 Tage dauern. Eine oder mehrere Rechnungen müssen vom Commerce-Administrator erstellt werden, um die Mittel zu erfassen. |
| [!UICONTROL URL Display on Product Details Page] | Shop-Ansicht | Bestimmt, ob die Schaltfläche „Checkout mit PayPal“ auf Produktseiten angezeigt wird. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

### [!UICONTROL Advanced Settings - PayPal Express Checkout]

![Erweiterte Einstellungen](./assets/payment-methods-paypal-payflow-link-express-checkout-advanced-settings.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Display on Shopping Cart] | Shop-Ansicht | Bestimmt, ob der PayPal Express-Checkout als Zahlungsoption im Warenkorb angezeigt wird. Optionen: Ja (empfohlen) / Nein |
| [!UICONTROL Payment Action Applicable From] | Website | Bestimmt den Bereich der entsprechenden Länderauswahl. Optionen: Alle zulässigen Länder/bestimmte Länder |
| [!UICONTROL Countries Payment Applicable From] | Website | Gibt jedes Land an, aus dem die Zahlung akzeptiert wird. Nur Kunden mit einer Rechnungsadresse in einem ausgewählten Land können mit dieser Zahlungsmethode Einkäufe tätigen. |
| [!UICONTROL Debug Mode] | Website | Zeichnet Nachrichten, die zwischen Ihrem Geschäft und dem PayPal-Zahlungssystem gesendet werden, in einer Protokolldatei auf. Optionen: `Yes` / `No` <br/><br/>**_Hinweis:_**&#x200B;Die Protokolldatei wird auf dem Server gespeichert und ist nur für Entwickler zugänglich. In Übereinstimmung mit den PCI Data Security Standards werden Kreditkarteninformationen nicht in der Protokolldatei aufgezeichnet. |
| [!UICONTROL Enable SSL Verification] | Website | Ermöglicht die Überprüfung des Host-Sicherheitszertifikats. Optionen: `Yes` / `No` |
| [!UICONTROL Transfer Cart Line Items] | Website | Zeigt eine vollständige Zusammenfassung der Zeileneinträge aus dem Warenkorb des Kunden auf der PayPal-Website an. Optionen: `Yes` / `No` |
| [!UICONTROL Skip Order Review Step] | Website | Legt fest, ob Kundinnen und Kunden die Transaktion über die PayPal-Website abschließen können oder verpflichtet sind, zu Ihrem Geschäft zurückzukehren und den Schritt zur Bestellüberprüfung auszuführen, bevor sie die Bestellung übermitteln. Optionen: `Yes` / `No` |

{style="table-layout:auto"}
