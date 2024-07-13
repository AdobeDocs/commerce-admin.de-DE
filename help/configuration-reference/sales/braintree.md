---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] &gt; [!UICONTROL Braintree]'
description: Überprüfen Sie die Konfigurationseinstellungen für den Abschnitt "[!UICONTROL Braintree]"auf der Seite "[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods]"des Commerce-Administrators.
exl-id: cf08bc4d-8d88-45e7-af71-f1ff90023766
feature: Configuration, Payments
source-git-commit: 5488a0a991f497059ea39fbbc8a08fd8f546e1ac
workflow-type: tm+mt
source-wordcount: '2603'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] > [!UICONTROL Braintree]

>[!IMPORTANT]
>
>**Migration zu Commerce 2.4:**<br/>
>Für Versionen von Adobe Commerce und Magento Open Source, die älter als Version 2.4.0 sind, wurde empfohlen, dass Händler die offizielle Braintree-Zahlungsintegrationserweiterung von [Commerce Marketplace](https://marketplace.magento.com/catalogsearch/result/?q=braintree) installieren und konfigurieren, um die Kernintegration zu ersetzen. Ab 2.4.0 ist die Erweiterung jetzt in der Kernversion enthalten.
><br/><br/>
>Bei der Migration zu Commerce 2.4 müssen Händler die auf dem Marketplace bereitgestellte Erweiterung (`paypal/module-braintree` oder `gene/module-braintree`) deinstallieren und alle Code-Anpassungen aktualisieren, um den Namespace `PayPal_Braintree` anstelle von `Magento_Braintree` zu verwenden. Die Konfigurationseinstellungen aus der gebündelten Erweiterung für Commerce und die auf der Commerce Marketplace verteilte Erweiterung werden beibehalten. Zahlungen, die mit diesen Versionen der Erweiterung platziert werden, werden wie üblich erfasst, annulliert oder erstattet.
><br/><br/>
>Wenn Sie auf Commerce 2.4.0 aktualisieren und nicht die empfohlene Commerce Marketplace-Erweiterung in Ihrer vorherigen Version 2.3.x verwenden, funktioniert die Funktion für mehrere Adressen nicht mit der Version 2.4.0 von Braintree. Wenn ein Käufer _an mehrere Adressen senden_ auswählt, wird die Braintree-Zahlungsmethode nicht angezeigt. Die zuvor für 2.3.x empfohlene Commerce Marketplace-Erweiterung weist dieses Problem mit mehreren Adressen auf.

{{config}}

## [!UICONTROL Basic Braintree Settings]

![Grundlegende Braintree-Einstellungen](./assets/payment-methods-braintree-basic-config.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Title] | Store-Ansicht | Standardwert: `Credit Card` (Braintree) |
| [!UICONTROL Environment] | Store-Ansicht | Optionen: `Sandbox` / `Production` |
| [!UICONTROL Payment Action] | Store-Ansicht | Bestimmt die Aktion, die von der Braintree bei der Verarbeitung einer Zahlung durchgeführt wird. Optionen: <br/>**`Authorize`**- Die Mittel auf der Kreditkarte des Kunden werden genehmigt, aber nicht vom Konto übertragen. Eine Bestellung wird in Ihrem Store-Administrator erstellt. Sie können den Verkauf später erfassen und eine Rechnung erstellen.<br/>**`Intent Sale`** (früher `Authorize and Capture` in früheren Versionen) - Die Mittel auf der Kreditkarte des Kunden werden von Braintree autorisiert und erfasst und eine Bestellung und Rechnung werden in Ihrem Store-Administrator erstellt. |
| [!UICONTROL Sandbox Merchant ID] | Store-Ansicht | Dies ist die eindeutige Kennung für Ihr gesamtes Sandbox-Gateway-Konto. Ihre Händler-ID, die auch als _öffentliche ID_ oder _Produktions-ID_ bezeichnet wird, unterscheidet sich von Ihren Produktions- und Sandbox-Gateways. Dieses Feld wird angezeigt, wenn das Feld _[!UICONTROL Environment]_auf `Sandbox` gesetzt ist. |
| [!UICONTROL Sandbox Public Key] | Store-Ansicht | Dies ist Ihre benutzerspezifische öffentliche Kennung, die den Zugriff auf verschlüsselte Daten einschränkt. Jeder Benutzer, der mit Ihrem Sandbox-Braintree-Gateway verbunden ist, verfügt über einen eigenen öffentlichen Sandbox-Schlüssel. Dieses Feld wird angezeigt, wenn das Feld _[!UICONTROL Environment]_auf `Sandbox` gesetzt ist. |
| [!UICONTROL Sandbox Private Key] | Store-Ansicht | Dies ist Ihre benutzerspezifische, private Kennung, die den Zugriff auf verschlüsselte Daten einschränkt. Jeder Benutzer, der mit Ihrem Sandbox Braintree Gateway verbunden ist, hat seinen eigenen privaten Schlüssel für die Sandbox. Dieses Feld wird angezeigt, wenn das Feld _[!UICONTROL Environment]_auf `Sandbox` gesetzt ist. |
| [!UICONTROL Merchant ID] | Store-Ansicht | Dies ist die eindeutige Kennung für Ihr gesamtes Gateway-Konto, einschließlich der verschiedenen Händlerkonten, die sich möglicherweise in Ihrem Gateway befinden. Ihre Händler-ID, die auch als _öffentliche ID_ oder _Produktions-ID_ bezeichnet wird, unterscheidet sich von Ihren Produktions- und Sandbox-Gateways. Dieses Feld wird angezeigt, wenn das Feld _[!UICONTROL Environment]_auf `Production` gesetzt ist. |
| [!UICONTROL Public Key] | Store-Ansicht | Dies ist Ihre benutzerspezifische öffentliche Kennung, die den Zugriff auf verschlüsselte Daten einschränkt. Jeder Benutzer, der mit Ihrem Braintree-Gateway verbunden ist, verfügt über einen eigenen öffentlichen Schlüssel. Dieses Feld wird angezeigt, wenn das Feld _[!UICONTROL Environment]_auf `Production` gesetzt ist. |
| [!UICONTROL Private Key] | Store-Ansicht | Dies ist Ihre benutzerspezifische, private Kennung, die den Zugriff auf verschlüsselte Daten einschränkt. Jeder Benutzer, der mit Ihrem Braintree-Gateway verbunden ist, verfügt über einen eigenen privaten Schlüssel. Dieses Feld wird angezeigt, wenn das Feld _[!UICONTROL Environment]_auf `Production` gesetzt ist. |
| [!UICONTROL Enable Card Payments] | Webseite | Stellt fest, ob die Braintree-Kreditkartenzahlmethode Ihren Kunden als Zahlungsmethode zur Verfügung steht. Optionen: `Yes` / `No` |
| [!UICONTROL Enable Vault for Card Payments] | Webseite | Wenn diese Option aktiviert ist, wird eine sichere Datenspeicherung für Kundendaten bereitgestellt, sodass Kunden ihre Kreditkarteninformationen nicht bei jedem Kauf erneut eingeben müssen. Optionen: `Yes` / `No` |
| [!UICONTROL Enable Vault CVV Reverification] | Webseite | Wenn diese Option aktiviert ist, wird die Überprüfung für die Einrichtung der CVV-Regeln in Ihrem Braintree-Konto durchgeführt. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Advanced Braintree Settings]

![Braintree Erweiterte Einstellungen](./assets/payment-methods-braintree-advanced-config.png){width="550" zoomable="yes"}

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Vault Title] | Webseite | Ein beschreibender Titel für Ihre Referenz, der den Vault angibt, in dem die Kundenkarteninformationen gespeichert sind. |
| [!UICONTROL Merchant Account ID] | Webseite | Die Merchant Account ID, die mit Braintree-Transaktionen von dieser Website verknüpft werden soll. Wenn Sie das Feld leer lassen, wird das standardmäßige Händlerkonto aus Ihrem Braintree-Konto verwendet. |
| [!UICONTROL Enable Checkout Express Payments] | Webseite | Bietet ein schnelleres Checkout-Erlebnis mit Express Payment-Optionen zu Beginn des Checkout-Prozesses, einschließlich PayPal, PayLater, Apple Pay und Google Pay. Optionen: `Yes` / `No` |
| [!UICONTROL Skip Fraud Checks on Admin Orders] | Webseite | Verhindert, dass die Transaktion im Rahmen von [!DNL Advanced Fraud Tools] -Prüfungen zur Auswertung gesendet wird, wenn Bestellungen vom Administrator nur auf `Yes` gesetzt werden.<br/>Optionen: `Yes` / `No` |
| [!UICONTROL Bypass Fraud Protection Threshold] | Webseite | `Advanced Fraud Protection` -Prüfungen werden umgangen, wenn der Schwellenwert erreicht oder überschritten wird. Wenn Sie dieses Feld leer lassen, wird diese Option deaktiviert. |
| [!UICONTROL Debug] | Webseite | Bestimmt, ob die Kommunikation zwischen dem Braintree-System und Ihrem Speicher in einer Protokolldatei aufgezeichnet wird. Optionen: `Yes` / `No` |
| [!UICONTROL CVV Verification] | Webseite | Bestimmt, ob Kunden den dreistelligen Sicherheitscode von der Rückseite einer Kreditkarte aus bereitstellen müssen. Optionen: `Yes` / `No` |
| [!UICONTROL Send Card Line Items] | Webseite | Senden Sie die Artikel mit den Warenkorbzeilen für alle Zahlungsmethoden. Optionen: `Yes` / `No` |
| [!UICONTROL Credit Card Types] | Webseite | Gibt jede Kreditkarte an, die Sie als Zahlung über Braintree akzeptieren. Halten Sie `Ctrl` (oder `Command` in Mac) gedrückt, um eine Kombination von Karten auszuwählen. Optionen: `American Express` / `Visa` / `MasterCard` / `Discover` / `JCB` / `Diners` / `Maestro International` |
| [!UICONTROL Sort Order] | Webseite | Bestimmt die Reihenfolge, in der Braintree beim Checkout mit anderen Zahlungsmethoden aufgeführt wird. |

## [!UICONTROL Braintree Webhooks Settings]

![Braintree Webhooks-Einstellungen](./assets/payment-methods-braintree-webhooks-config.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable Webhook] | Webseite | Um die Webhook-Funktionalität für den Schutz von Betrug, ACH-Zahlungen, lokale Zahlungsmethoden und Streitigkeiten zu ermöglichen. Optionen: `Yes` / `No` |
| [!UICONTROL Fraud Protection URL] | Webseite | Fügen Sie diese URL Ihrem Braintree-Konto als [!UICONTROL Webhook Destination URL] hinzu. **Diese URL muss sicher und öffentlich zugänglich sein.** |
| [!UICONTROL Fraud Protection Approve Order Status] | Webseite | Wenn der Betrugsschutz von Braintree genehmigt wird, wird der ausgewählte Auftragsstatus der Commerce-Bestellung zugewiesen. Dieser Status wird verwendet, um den Status der Bestellung zu aktualisieren, bei der die ACH-Zahlungsmethode verwendet wird und bei der Umstellung auf `SETTLED` in der Braintree. |
| [!UICONTROL Fraud Protection Reject Order Status] | Webseite | Wenn der Betrugsschutz von Braintree abgelehnt wird, wird der ausgewählte Auftragsstatus der Commerce-Bestellung zugewiesen. Dieser Status wird verwendet, um den Status der Bestellung zu aktualisieren, bei der die ACH-Zahlungsmethode verwendet wird und bei der `SETTLEMENT` der Wert `DECLINED` im Braintree ist. |

{style="table-layout:auto"}

## [!UICONTROL Country Specific Settings]

![Länderspezifische Einstellungen](./assets/payment-methods-braintree-country-specific-config.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Payment from Applicable Countries] | Webseite | Bestimmt, ob Sie Zahlungen akzeptieren, die von Braintree aus allen Ländern oder nur aus bestimmten Ländern verarbeitet werden. Optionen: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Webseite | Gibt gegebenenfalls an, aus welchen Ländern Sie Zahlungen, die von Braintree verarbeitet werden, annehmen. |
| [!UICONTROL Country Specific Credit Card Types] | Webseite | Identifiziert die Kreditkarten, die pro Land für von der Braintree verarbeitete Zahlungen akzeptiert werden. Für jedes Land wird ein Datensatz gespeichert. Optionen: <br/>**`Country`**- Wählen Sie das Land aus.<br/>**`Allowed Card Types`** - Wählen Sie jede Kreditkarte aus, die vom Land als Zahlung durch Braintree akzeptiert wird. <br/>**`Add`**- Fügen Sie eine Zeile hinzu, um Kreditkarten für ein anderes Land zuzulassen.<br/>**`Action`** - Löscht den Datensatz der zulässigen Kreditkarten für das Land. |

{style="table-layout:auto"}

## [!UICONTROL ACH through Braintree]

![ACH DURCH Braintree](./assets/payment-methods-braintree-ach-config.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enabled ACH Direct Debit] | Webseite | Stellt fest, ob [!DNL ACH Direct Debit] als Zahlungsmethode über Braintree enthalten ist. Optionen: `Yes` / `No` |
| [!UICONTROL Enable Vault for ACH Direct Debit] | Webseite | Kunden können ihre einmalige Zahlungs-Methode für die ACH Direct Debit-Einmalzahlung für die zukünftige Verwendung einsetzen/speichern. Sobald die Zahlungsdetails validiert wurden, kann der Kunde die Zahlungsmethode ACH Direct Debit verwenden, ohne die Daten erneut einzugeben oder seine Zahlungsinformationen erneut zu authentifizieren. Optionen: `Yes` / `No` |
| [!UICONTROL Sort Order] | Webseite | Bestimmt die Reihenfolge, in der [!DNL ACH Direct Debit] beim Checkout mit anderen Zahlungsmethoden aufgeführt wird. |

{style="table-layout:auto"}

## [!UICONTROL Apple Pay through Braintree]

![Apple-Pay durch Braintree](./assets/payment-methods-braintree-applepay-config.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable ApplePay through Braintree] | Webseite | Stellt fest, ob Apple Pay als Zahlungsmethode über Braintree enthalten ist. Optionen: `Yes` / `No` <br/><br/> Die Domäne muss [im Braintree Account first](https://developer.paypal.com/braintree/docs/guides/apple-pay/configuration/javascript/v3) verifiziert sein. |
| [!UICONTROL Enable Vault for ApplePay] | Webseite | Kunden können ihre Apple Pay-Zahlungsmethode für die zukünftige Verwendung aufbewahren. Sobald die Zahlungsdetails validiert wurden, kann der Kunde Apple Pay verwenden, ohne die Daten erneut einzugeben oder seine Zahlungsinformationen erneut zu authentifizieren. Optionen: `Yes` / `No` |
| [!UICONTROL Payment Action] | Webseite | Bestimmt die Aktion, die von der Braintree bei der Verarbeitung einer Zahlung durchgeführt wird. Optionen: <br/>**`Authorize`**- Mittel auf der Kundenkarte sind autorisiert, aber nicht vom Kundenkonto übertragen. Eine Bestellung wird in Ihrem Store-Administrator erstellt. Sie können den Verkauf später erfassen und eine Rechnung erstellen.<br/>**`Intent Sale`** - Die Mittel auf der Kundenkarte werden von Braintree autorisiert und erfasst. Eine Bestellung und Rechnung werden in Ihrem Store-Administrator erstellt. **_Hinweis:_** Dies war `Authorize and Capture` in 2.3.x und früheren Versionen. |
| [!UICONTROL Merchant Name] | Store-Ansicht | Beschriftung, die Kunden im ApplePay-Popup angezeigt wird. |
| [!UICONTROL Sort Order] | Webseite | Bestimmt die Reihenfolge, in der Apple Pay beim Checkout mit anderen Zahlungsmethoden aufgeführt wird. |

{style="table-layout:auto"}

## [!UICONTROL Local Payment Methods]

![Lokale Zahlungsmethoden](./assets/payment-methods-braintree-local-payment-config.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enabled Local Payment Methods] | Webseite | Bestimmt, ob die lokale Zahlungsmethode über Braintree als Zahlungsmethode einbezogen wird. Optionen: `Yes` / `No` |
| [!UICONTROL Title] | Webseite | Titel, der im Abschnitt Zahlungsmethode des Kassengangs angezeigt wird. Standardwert: `Local Payments` |
| [!UICONTROL Fallback Button Text] | Webseite | Geben Sie den Text ein, der für die Schaltfläche verwendet werden soll, die auf der Fallback-Braintree-Seite angezeigt wird, über die Kunden zur Website zurückkehren. Standardwert: `Complete Checkout` |
| [!UICONTROL Redirect on Fail] | Webseite | Gibt die URL an, an die Kunden weitergeleitet werden sollen, wenn lokale Zahlungsmethoden-Transaktionen abgebrochen werden, fehlschlagen oder Fehler auftreten. Dies sollte die Zahlungsseite für den Checkout sein (z. B. `https://www.domain.com/checkout#payment`). |
| [!UICONTROL Allowed Payment Method] | Webseite | Wählen Sie die lokale Zahlungsmethode aus, die aktiviert werden soll. Optionen: `Bancontact` / `EPS` / `giropay` / `iDeal` / `Klarna Pay Now` / `SOFORT` / `MyBank` / `P24` / `SEPA/ELV Direct Debit` (noch nicht unterstützt) |
| [!UICONTROL Sort Order] | Webseite | Bestimmt die Reihenfolge, in der die lokale Zahlungsmethode beim Checkout mit anderen Zahlungsmethoden aufgelistet wird. |

{style="table-layout:auto"}

>[!NOTE]
>
>Die gebündelte Braintree-Erweiterung unterstützt nicht alle in der [Braintree-Entwicklerdokumentation](https://developer.paypal.com/braintree/docs/guides/local-payment-methods/overview) aufgelisteten lokalen Zahlungsmethoden. Andere lokale Zahlungsmethoden werden derzeit entwickelt, um in zukünftigen Versionen unterstützt zu werden.

## [!UICONTROL GooglePay through Braintree]

![GooglePay über Braintree](./assets/payment-methods-braintree-googlepay-config.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enabled GooglePay through Braintree] | Webseite | Stellt fest, ob [!DNL Google Pay]-Zahlung als Zahlungsmethode über Braintree enthalten ist. Optionen: `Yes` / `No` |
| [!UICONTROL Enable Vault for GooglePay] | Webseite | Kunden können ihre Google Pay-Zahlungsmethode für die zukünftige Verwendung aufbewahren. Sobald die Zahlungsdetails validiert wurden, kann der Kunde Google Pay verwenden, ohne die Daten erneut einzugeben oder seine Zahlungsinformationen erneut zu authentifizieren. Optionen: `Yes` / `No` |
| [!UICONTROL Payment Action] | Webseite | Bestimmt die Aktion, die von der Braintree bei der Verarbeitung einer Zahlung durchgeführt wird. Optionen: <br/>**`Authorize`**- Mittel auf der Kundenkarte sind autorisiert, aber nicht vom Kundenkonto übertragen. Eine Bestellung wird in Ihrem Store-Administrator erstellt. Sie können den Verkauf später erfassen und eine Rechnung erstellen.<br/>**`Intent Sale`** - Die Mittel auf der Kundenkarte werden von Braintree autorisiert und erfasst. Eine Bestellung und Rechnung werden in Ihrem Store-Administrator erstellt. **_Hinweis:_** Dies war `Authorize and Capture` in 2.3.x und früheren Versionen. |
| [!UICONTROL Button Color] | Webseite | Legt die Farbe der Schaltfläche [!DNL Google Pay] fest. Optionen: `White` / `Black` |
| [!UICONTROL Merchant ID] | Store-Ansicht | Die von Google bereitgestellte ID muss hier eingegeben werden. |
| [!UICONTROL Accepted Cards] | Webseite | Wählen Sie den Kartentyp aus, den ein Kunde verwenden kann, um eine Bestellung mit [!DNL Google Pay] aufzugeben. |
| [!UICONTROL Sort Order] | Webseite | Bestimmt die Reihenfolge, in der Google Pay beim Checkout mit anderen Zahlungsmethoden aufgeführt wird. |

{style="table-layout:auto"}

## [!UICONTROL Venmo through Braintree]

![Venmo durch Braintree](./assets/payment-methods-braintree-venmo-config.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable Venmo through Braintree] | Webseite | Stellt fest, ob [!DNL Venmo] als Zahlungsmethode über Braintree enthalten ist. Optionen: `Yes` / `No` |
| [!UICONTROL Enable Vault for Venmo] | Webseite | Kunden können ihre Venmo-Zahlungsmethode für die zukünftige Verwendung aufbewahren. Sobald die Zahlungsdetails validiert wurden, kann der Kunde die Venmo-Zahlungsmethode verwenden, ohne die Daten erneut einzugeben oder seine Zahlungsinformationen erneut zu authentifizieren. Optionen: `Yes` / `No` |
| [!UICONTROL Payment Action] | Webseite | Bestimmt die Aktion, die von der Braintree bei der Verarbeitung einer Zahlung durchgeführt wird. Optionen: <br/>**`Authorize`**- Mittel auf der Kundenkarte sind autorisiert, aber nicht vom Kundenkonto übertragen. Eine Bestellung wird in Ihrem Store-Administrator erstellt. Sie können den Verkauf später erfassen und eine Rechnung erstellen.<br/>**`Intent Sale`** - Die Mittel auf der Kundenkarte werden von Braintree autorisiert und erfasst. Eine Bestellung und Rechnung werden in Ihrem Store-Administrator erstellt. **_Hinweis:_** Dies war _Autorisierung und Erfassung_ in 2.3.x und früheren Versionen. |
| [!UICONTROL Sort Order] | Webseite | Bestimmt die Reihenfolge, in der Venmo beim Checkout mit anderen Zahlungsmethoden aufgeführt wird. |

{style="table-layout:auto"}

## [!UICONTROL PayPal through Braintree]

![PayPal durch Braintree](./assets/payment-methods-braintree-paypal-config.png){width="550" zoomable="yes"}

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable PayPal through Braintree] | Webseite | Bestimmt, ob PayPal als Zahlungsmethode über Braintree enthalten ist. Optionen: `Yes` / `No` |
| [!UICONTROL Enable PayPal Credit through Braintree] | Webseite | Stellt fest, ob PayPal-Guthaben als Zahlungsmethode über Braintree enthalten ist. Optionen: `Yes` / `No`. Dieses Feld wird angezeigt, wenn `Enable PayPal through Braintree` auf `Yes` gesetzt ist |
| [!UICONTROL Enable PayPal PayLater through Braintree] | Webseite | Bestimmt, ob PayPal PayLater als Zahlungsmethode über Braintree enthalten ist. Optionen: `Yes` / `No`. Dieses Feld wird angezeigt, wenn `Enable PayPal through Braintree` auf `Yes` gesetzt ist |
| [!UICONTROL Title] | Store-Ansicht | Die Bezeichnung, die PayPal durch Braintree an Kunden während des Checkout identifiziert. Standardwert: `PayPal` |
| [!UICONTROL Vault Enabled] | Webseite | Wenn diese Option aktiviert ist, wird für Kunden-Zahlungsinformationen sicherer Speicher bereitgestellt, sodass Kunden ihre PayPal-Informationen nicht für jeden Kauf erneut eingeben müssen. Optionen: `Yes` / `No` |
| [!UICONTROL Send Cart Line Items for PayPal] | Webseite | Senden Sie die Zeileneinträge (Bestellartikel) zusammen mit Geschenkkarten, Geschenkverpackung für Artikel, Geschenkverpackung für Bestellung, Gutschrift für Geschäft, Versand und Steuern als Zeileneinträge an PayPal. Optionen: `Yes` / `No` |
| [!UICONTROL Sort Order] | Webseite | Eine Zahl, die die Reihenfolge bestimmt, in der PayPal durch Braintree mit anderen Zahlungsmethoden beim Checkout aufgeführt wird. |
| [!UICONTROL Override Merchant Name] | Store-Ansicht | Ein alternativer Name, mit dem der Händler für jede Store-Ansicht identifiziert werden kann. |
| [!UICONTROL Payment Action] | Webseite | Bestimmt die Aktion, die PayPal bei der Bearbeitung einer Zahlung durch Braintree durchführt. Optionen: <br/>**`Authorize`**- Mittel auf der Kundenkarte sind autorisiert, aber nicht vom Kundenkonto übertragen. Eine Bestellung wird in Ihrem Store-Administrator erstellt. Sie können den Verkauf später erfassen und eine Rechnung erstellen.<br/>**`Authorize and Capture`** - Die Mittel auf der Kundenkarte werden von PayPal über Braintree autorisiert und erfasst. Eine Bestellung und Rechnung werden in Ihrem Store-Administrator erstellt. |
| [!UICONTROL Payment from Applicable Countries] | Webseite | Bestimmt, ob Sie Zahlungen akzeptieren, die von PayPal über Braintree aus allen Ländern oder nur aus bestimmten Ländern verarbeitet werden. Optionen: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | Webseite | Gibt gegebenenfalls an, aus welchen Ländern Sie Zahlungen, die von Braintree verarbeitet werden, annehmen. |
| [!UICONTROL Require Customer's Billing Address] | Webseite | Bestimmt, ob die Rechnungsadresse des Kunden zum Senden einer Bestellung erforderlich ist. Optionen: `Yes` / `No` |
| [!UICONTROL Debug] | Webseite | Bestimmt, ob die Kommunikation zwischen dem PayPal über das Braintree-System und Ihrem Speicher in einer Protokolldatei aufgezeichnet wird. Optionen: `Yes` / `No` |
| [!UICONTROL Display on Shopping Cart] | Webseite | Bestimmt, ob die Schaltfläche PayPal im [Mini-Warenkorb](../../stores-purchase/cart-configuration.md#mini-cart) und auf der Seite [Warenkorb](../../stores-purchase/cart.md) angezeigt wird. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

>[!NOTE]
>
>Es kann entweder **[!DNL PayPal Credit]** oder **[!DNL PayPal PayLater]** aktiviert werden. Beide Methoden können nicht gleichzeitig aktiviert werden.

### [!UICONTROL Styling]

![PayPal Styling](./assets/payment-methods-braintree-paypal-styling.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Location] | Webseite | Legt fest, wo PayPal-Schaltflächen und -Nachrichten auf der Storefront gerendert werden. Optionen: `Mini-Cart and Cart Page` / `Checkout Page` / `Product Page` |

{style="table-layout:auto"}

**[!UICONTROL Mini-Cart and Cart Page]**

Die Option und die Einstellungen in diesem Abschnitt variieren je nach Einstellung im Feld _[!UICONTROL Location]_.

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL PayPal Button Type] | Webseite | Legt die Schaltfläche auf einen der drei Typen fest: `PayPal Button` / `PayPal Pay Later Button` / `PayPal Credit Button` |

**[!UICONTROL PayPal Button]**

Die Optionen und Einstellungen in diesem Abschnitt variieren je nach dem im Feld _[!UICONTROL PayPal Button Type]_ausgewählten Schaltflächentyp.

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Show PayPal Button] | Webseite | Bestimmt die Position der Schaltfläche &quot;PayPal&quot;an der ausgewählten Position. Optionen: `Yes` / `No` |
| [!UICONTROL Button Label] | Webseite | Legt die Bezeichnung für die Schaltfläche PayPal fest. Optionen: `Paypal` / `Checkout` / `Buy Now` / `Pay` |
| [!UICONTROL Color] | Webseite | Legt die Farbe der Schaltfläche PayPal fest. Optionen: `Blue` / `Black` / `Gold` / `Silver` |
| [!UICONTROL Shape] | Webseite | Bestimmt die Form der PayPal-Schaltfläche. Optionen: `Pill` / `Rectangle` |
| [!UICONTROL Size(Deprecated)] | Webseite | Bestimmt die Größe der PayPal-Schaltfläche. Optionen: `Medium` / `Large` / `Responsive` |

{style="table-layout:auto"}

>[!NOTE]
>
>Das Konfigurationsfeld **[!DNL Size(Deprecated)]** ist veraltet und wird nicht zum Formatieren der PayPal-Schaltflächen verwendet.

**[!UICONTROL PayLater Messaging]**

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Show PayLater Messaging] | Webseite | Aktiviert PayLater-Nachrichten am ausgewählten Ort. Optionen: `Yes` / `No`. Wenn diese Option aktiviert ist, werden PayLater-Nachrichten für verfügbare Angebote angezeigt ([Beschränkungen gelten](https://developer.paypal.com/docs/checkout/pay-later/us/)). |
| [!UICONTROL Message Layout] | Webseite | Bestimmt das Layout der PayLater-Nachricht. Optionen: `Text` / `Flex` |
| [!UICONTROL Logo] | Webseite | Bestimmt den für die Schaltfläche PayPal verwendeten Logotyp. Optionen: `Inline` / `Primary` / `Alternative` / `None` |
| [!UICONTROL Logo Position] | Webseite | Legt die Logoposition für die Schaltfläche PayPal fest. Optionen: `Left` / `Right` / `Top` |
| [!UICONTROL Text Color] | Webseite | Bestimmt die Textfarbe der PayPal-Schaltfläche. Optionen: `Black` / `White` / `Monochrome` / `Grayscale` |

{style="table-layout:auto"}

Wenn diese Optionen festgelegt sind, können Sie die Vorschau der PayPal-Schaltflächen und PayLater-Nachrichten sehen. Es gibt Steuerelemente, mit denen Sie die Einstellungen anwenden oder die Werte zurücksetzen können:

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Apply] | Webseite | Speichert die ausgewählten Stileinstellungen für Schaltflächen und PayLater-Nachrichten und wendet sie auf die aktuelle Position und den aktuellen Schaltflächentyp an. |
| [!UICONTROL Apply to All Buttons] | Webseite | Speichert die ausgewählten Stileinstellungen für Schaltflächen und PayLater-Nachrichtenwerte und wendet sie auf alle Schaltflächentypen und -speicherorte an. |
| [!UICONTROL Reset to Recommended Defaults] | Webseite | Gibt die Stileinstellungen auf die empfohlenen Standardwerte für Schaltflächen und PayLater-Nachrichten zurück und wendet sie auf alle Schaltflächentypen und -speicherorte an. |

{style="table-layout:auto"}

## 3d Sichere Überprüfungseinstellungen

![3D Secure Verification Settings](./assets/payment-methods-braintree-3d-secure-verify-config.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL 3D Secure Verification] | Webseite | Bestimmt, ob eine Transaktion einen zusätzlichen Verifizierungsprozess bestehen muss, wenn der Kunde in ein Programm wie _Verifiziert durch VISA_ eingeschrieben ist. Optionen: `Yes` / `No` |
| [!UICONTROL Always request 3DS] | Webseite | Fordern Sie die 3D Secure-Anfrage immer für alle Transaktionen an. Optionen: `Yes` / `No` |
| [!UICONTROL Threshold Amount] | Webseite | Bestimmt den maximalen Bestellbetrag, der für die Verarbeitung auf einer Bestellung zulässig ist. Braintree lehnt die Autorisierung ab, wenn der Bestellbetrag diesen Schwellenwert überschreitet. |
| [!UICONTROL Verify for Applicable Countries] | Webseite | Bestimmt die Länder, in denen die Zahlung überprüft werden muss. Optionen: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Verify for Specific Countries] | Webseite | Gegebenenfalls Angabe der Länder, aus denen die Zahlung durch Braintree überprüft werden muss. |

{style="table-layout:auto"}

## [!UICONTROL Dynamic Descriptors]

![Dynamische Deskriptoren](./assets/payment-methods-braintree-dynamic-config.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Name] | Store-Ansicht | Der Name-Deskriptor besteht aus zwei Teilen, die durch ein Sternchen (*) getrennt sind. Der erste Teil des Deskriptors identifiziert das Unternehmen oder DBA und der zweite Teil das Produkt. Beispiel: `company*myproduct` <br/><br/>Die Länge der Unternehmens- und Produktteile des Deskriptors kann auf folgende Weise für eine kombinierte Länge von bis zu 22 Zeichen zugeordnet werden: <br/>**`Option 1`**- Firma muss drei Zeichen sein / Produkt kann bis zu 18 Zeichen<br/>**`Option 2`** - Firma muss sieben Zeichen lang sein / Produkt kann bis zu 14 Zeichen lang sein <br/>**`Option 3`**- Firma muss 12 Zeichen lang sein / Produkt darf maximal neun Zeichen lang sein |
| [!UICONTROL Phone] | Store-Ansicht | Der Phone-Deskriptor muss zwischen 14 und 14 Zeichen lang sein und darf nur Zahlen, Bindestriche, Klammern und Punkte enthalten. Beispiel: `9999999999` `(999) 999-9999` `999.999.9999` |
| [!UICONTROL URL] | Store-Ansicht | Der URL-Deskriptor stellt Ihren Domänennamen dar und kann bis zu 13 Zeichen lang sein. Beispiel: `company.com` |

{style="table-layout:auto"}
