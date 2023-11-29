---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] &gt;  [!UICONTROL PayPal Payflow Pro]'
description: Überprüfen Sie die Konfigurationseinstellungen im Abschnitt [!UICONTROL PayPal Payflow Pro] im Abschnitt [!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] Seite des Commerce-Administrators.
exl-id: 2aae038b-15c0-452a-98bc-4d97efbb60f6
feature: Configuration, Payments
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '650'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] >  [!UICONTROL PayPal Payflow Pro]

>[!IMPORTANT]
>
>**PSD2-Anforderungen:** <br/>
>Ab dem 14. September 2019 könnten europäische Banken Zahlungen ablehnen, die nicht erfüllt sind [PSD2](../../getting-started/compliance-payment-services-directive.md) Anforderungen. Einhaltung von PSD 2, [!DNL PayPal Payflow Pro] muss in [!DNL Cardinal Commerce]. Weitere Informationen finden Sie unter [3-D-Sicherheit für Payflow](https://developer.paypal.com/api/nvp-soap/payflow/3d-secure-overview/).

{{config}}

## [!UICONTROL Required Settings]

![Erforderliche Einstellungen](./assets/paypal-payflow-pro-settings.png)<!-- zoom -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Email Associated with PayPal Merchant Account] | Webseite | (Optional) Alle E-Mail-Adressen, die mit Ihrem PayPal-Handelskonto verknüpft sind. Bei E-Mail-Adressen muss die Groß-/Kleinschreibung beachtet werden und die Adressen müssen exakt mit denen in Ihrem Konto übereinstimmen. |
| [!UICONTROL Partner] | Webseite | gegebenenfalls Ihre PayPal-Partner-ID. |
| [!UICONTROL Vendor] | Webseite | Ihr PayPal-Benutzername. |
| Benutzer | Webseite | Die ID eines anderen Benutzers in Ihrem PayPal-Konto. |
| [!UICONTROL Password] | Webseite | Das Kennwort, das Ihrem PayPal-Kaufkonto zugeordnet ist. |
| [!UICONTROL Test Mode] | Webseite | Wenn diese Option aktiviert ist, führt PayPal Payflow Pro in einer Testumgebung aus. Deaktivieren Sie den Testmodus, wenn Sie bereit sind, im Produktionsmodus live zu gehen. Optionen: `Yes` / `No` |
| [!UICONTROL Use Proxy] | Webseite | Ein Proxy kann verwendet werden, um den Traffic umzuleiten, wenn die Server-Firewall den direkten Zugriff auf den PayPal-Server verhindert. Gibt ggf. den Proxy-Server an, der zum Herstellen einer Verbindung mit dem PayPal-Server verwendet wird. Optionen: `Yes` / `No` <br/><br/>Wenn diese Option aktiviert ist, legen Sie die Proxy-Optionen fest: <br/>**`Proxy Host`**- Die IP-Adresse des Proxyhosts.<br/>**`Proxy Port`** - Die Nummer des Proxy-Ports. |
| [!UICONTROL Enable this Solution] | Webseite | Stellt fest, ob PayPal Payflow Pro Ihren Kunden als Zahlungsmethode zur Verfügung steht. |
| [!UICONTROL Enable PayPal Credit] | Webseite | Stellt fest, ob PayPal-Guthaben Ihren Kunden als Zahlungsoption zur Verfügung steht. |

{style="table-layout:auto"}

## [!UICONTROL Advertise PayPal Credit]

![Advertise PayPal Credit](./assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png)<!-- zoom -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Publisher ID] | Webseite | Die Herausgeber-ID, die Ihrem PayPal-Konto zugeordnet ist. |
| [!UICONTROL Get Publisher ID from PayPal] |  | Ruft Ihre Herausgeber-ID von PayPal ab. |
| [!UICONTROL Home Page] | Webseite | Bestimmt die Position und Größe der [!DNL PayPal Credit] Banner auf der Startseite. Optionen: <br/>**`Display`**- Bestimmt, ob eine[!DNL PayPal Credit] Banner wird auf der Startseite Ihres Stores angezeigt. Optionen: `Yes` / `No`<br/>**`Position`** - Bestimmt die Position der [!DNL PayPal Credit] Banner auf der Startseite. Optionen: Kopfzeile (zentriert)/Seitenleiste (rechts) <br/>**`Size`**- Bestimmt die Größe der [!DNL PayPal Credit] Banner auf der Startseite. Optionen: `190 x 100` / `234 x 60` / `300 x 50` / `468 x 60` / `728 x 90` /` 800 x 66` |
| [!UICONTROL Catalog Category Page] | Webseite | Bestimmt die Position und Größe der [!DNL PayPal Credit] Banner auf Kategorieseiten. Optionen: (entspricht für [!UICONTROL Home Page]) |
| [!UICONTROL Catalog Product Page] | Webseite | Bestimmt die Position und Größe der [!DNL PayPal Credit] Banner auf Produktseiten. Optionen: (entspricht für [!UICONTROL Home Page]) |
| [!UICONTROL Checkout Cart Page] | Webseite | Bestimmt die Position und Größe der [!DNL PayPal Credit] Banner auf der Warenkorbseite. Optionen: (entspricht für [!UICONTROL Home Page]) |

{style="table-layout:auto"}

## [!UICONTROL Basic Settings - PayPal Payflow Pro]

![Grundlegende Einstellungen](./assets/payment-methods-paypal-payflow-pro-basic-settings.png)<!-- zoom -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Title] | Store-Ansicht | Ein Name, der PayPal Payflow Pro als Zahlungsmethode beim Checkout angibt. |
| [!UICONTROL Sort Order] | Store-Ansicht | Eine Zahl, die bestimmt, in welcher Reihenfolge PayPal Payflow Pro angezeigt wird, wenn sie beim Checkout mit anderen Zahlungsmethoden aufgeführt wird. |
| [!UICONTROL Payment Action] | Webseite | Legt fest, welche Aktion von PayPal bei der Absendung einer Bestellung durchgeführt wird. Optionen: <br/>**`Authorization`**- Genehmigt den Kauf, aber hält die Mittel fest. Der Betrag wird erst dann zurückgezogen, wenn er vom Händler &quot;erfasst&quot;wurde.<br/>**`Sale`** - Der Kaufbetrag wird genehmigt und sofort vom Konto des Kunden zurückgezogen. |
| **[!UICONTROL Credit Card Settings]** |  |  |
| [!UICONTROL Allowed Credit Cart Types] | Webseite | Bestimmt die Kreditkarten, die Kunden beim Checkout zur Verfügung stehen. Wählen Sie jede unterstützte Karte aus. Optionen: `American Express` (erfordert eine zusätzliche Vereinbarung) / `Visa` / `MasterCard` / `Discover` / `JCB` |

{style="table-layout:auto"}

## [!UICONTROL Advanced Settings]

![Erweiterte Einstellungen](./assets/payment-methods-paypal-payflow-pro-advanced-settings.png)<!-- zoom -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| Anzeige im Warenkorb | Store-Ansicht | Bestimmt, ob PayPal Express Checkout als Zahlungsoption im Warenkorb angezeigt wird. Optionen: Ja (empfohlen) / Nein |
| [!UICONTROL Payment Action Applicable From] | Webseite | Bestimmt den Bereich der entsprechenden Länderauswahl. Optionen: Alle zugelassenen Länder/spezifischen Länder |
| [!UICONTROL Countries Payment Applicable From] | Webseite | Identifiziert jedes Land, aus dem die Zahlung akzeptiert wird. Mit dieser Zahlungsmethode können nur Kunden mit einer Rechnungsadresse in einem ausgewählten Land Einkäufe tätigen. |
| [!UICONTROL Debug Mode] | Webseite | Zeichnet die zwischen Ihrem Store und dem PayPal Zahlungssystem gesendeten Nachrichten in einer Protokolldatei auf. Optionen: `Yes` / `No` <br/><br/>**_Hinweis:_**Die Protokolldatei wird auf dem Server gespeichert und steht nur Entwicklern zur Verfügung. Gemäß PCI Data Security Standards werden Kreditkarteninformationen nicht in der Protokolldatei aufgezeichnet. |
| [!UICONTROL Enable SSL Verification] | Webseite | Aktiviert die Überprüfung des Host-Sicherheitszertifikats. Optionen: `Yes` / `No` |
| [!UICONTROL Transfer Cart Line Items] | Webseite | Zeigt eine vollständige Zusammenfassung der Zeileneinträge aus dem Warenkorb des Kunden auf der PayPal-Site an. Optionen: `Yes` / `No` |
| [!UICONTROL Skip Order Review Step] | Webseite | Bestimmt, ob Kunden die Transaktion von der PayPal-Site aus abschließen können oder dazu verpflichtet sind, zu Ihrem Store zurückzukehren und den Schritt &quot;Bestellprüfung&quot;abzuschließen, bevor die Bestellung gesendet wird. Optionen: `Yes` / `No` |

{style="table-layout:auto"}
