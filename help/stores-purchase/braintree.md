---
title: Braintree
description: Erfahren Sie, wie Sie Braintree als Online-Zahlungslösung in Ihrem Geschäft einrichten.
exl-id: 781b385f-926e-4047-b7da-6f7c090d75d8
feature: Payments
source-git-commit: fcd08ea5d8c3bd498eb4beae41bdf2f078a89f55
workflow-type: tm+mt
source-wordcount: '2625'
ht-degree: 0%

---

# Braintree

Braintree bietet ein vollständig anpassbares Checkout-Erlebnis mit Betrugserkennung und PayPal-Integration. Es unterstützt [!DNL Apple Pay], [!DNL Google Pay], ACH, Venmo und lokale Zahlungsmethoden. Braintree reduziert den Aufwand für die PCI-Compliance für Händler, da die Transaktion auf dem Braintree-System stattfindet. Die Braintree Payments-Integration wird entwickelt von [GENE Commerce](https://www.gene.co.uk/gene-braintree-payments/).

>[!NOTE]
>
>Wenn Sie ein Upgrade auf 2.4.x von einer früheren Version von Adobe Commerce oder Magento Open Source durchführen, während die Braintree-Erweiterung von Commerce Marketplace installiert ist, lesen Sie die Datei [2.4 Aktualisierungshinweise](#24-upgrade-notes) am Ende dieser Seite.


## Schritt 1: Braintree-Anmeldedaten abrufen

Zu gehen [Braintree Payments][1] und sich für ein Konto anmelden.

## Schritt 2: Abschließen der Grundeinstellungen

1. Auf der _Admin_ Seitenleiste, zu gehen **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich . **[!UICONTROL Sales]** und wählen **[!UICONTROL Payment Methods]**.

   - Wenn Ihre Commerce-Installation über mehrere Websites, Stores oder Ansichten verfügt, wählen Sie oben links die Option aus. **[!UICONTROL Store View]** Wo die Konfiguration gilt.

   - In der _[!UICONTROL Merchant Location]_überprüfen, ob **[!UICONTROL Merchant Country]**ist auf den Standort Ihres Unternehmens eingestellt.

1. Unter _[!UICONTROL Recommended Solutions]_, in der_[!UICONTROL Braintree Payments] (von [GENE Commerce](https://www.gene.co.uk/gene-braintree-payments/) v4.6.1 - [Versionshinweise](https://support.gene.co.uk/support/solutions/articles/35000228529)_klicken Sie auf **[!UICONTROL Configure]**.

   ![Braintree konfigurieren](./assets/braintree-payments.png){width="600" zoomable="yes"}

1. für **[!UICONTROL Title]**, geben Sie einen Titel ein, der das Braintree als Zahlungsoption beim Checkout kennzeichnet.

1. Einstellung des aktuellen Betriebs **[!UICONTROL Environment]** für Braintree-Transaktionen an `Sandbox` oder `Production`

   Verwenden Sie beim Testen der Konfiguration in einer Sandbox nur [Kreditkartennummern][2] die von Braintree empfohlen werden. Wenn Sie bereit sind, mit Braintree zur Produktion zu wechseln, legen Sie Folgendes fest **[!UICONTROL Environment]** bis `Production`.

   ![Grundlegende Einstellungen für Anmeldeinformationen](./assets/braintree-settings1.png){width="600" zoomable="yes"}

1. set **[!UICONTROL Payment Action]** eine der folgenden Möglichkeiten:

   - `Authorize Only` - Genehmigt den Kauf und setzt die Mittel zurück. Der Betrag wird erst dann vom Bankkonto des Kunden abgehoben, wenn der Verkauf abgeschlossen ist _Gefangen_ Durch den Händler.
   - `Intent Sale`  - Der Betrag des Kaufs wird autorisiert und sofort vom Konto des Kunden zurückgezogen. **_Hinweis:_** Dieser Wert war  _Autorisieren und erfassen_ In 2.3.x und früheren Versionen.|

1. Geben Sie die **[!UICONTROL Sandbox Merchant ID / Merchant ID]** von Ihrem Braintree-Konto.

1. Geben Sie die folgenden Anmeldeinformationen von Ihrem Braintree-Konto ein:

   - **[!UICONTROL Sandbox Public Key / Public Key]**
   - **[!UICONTROL Sandbox Private Key / Private Key]**

   >[!NOTE]
   >
   >Für beide gibt es separate Felder **(Sandbox und Produktion)** Umgebungen und die anderen Felder werden basierend auf der ausgewählten Umgebung gerendert.

1. Bevor Sie die Konfiguration speichern, klicken Sie auf **[!UICONTROL Validate Credentials]** , um Ihre Anmeldedaten zu validieren.

1. set **[!UICONTROL Enable Card Payments]** bis `Yes`.

   ![Allgemeine Einstellungen](./assets/braintree-settings2.png){width="600" zoomable="yes"}

   Wenn Sie Kundeninformationen sicher speichern möchten, sodass Kunden sie nicht bei jedem Kauf erneut eingeben müssen, legen Sie Folgendes fest **[!UICONTROL Enable Vault for Card Payments]** bis `Yes`.

## Schritt 3: Erweiterte Einstellungen abschließen

1. Expand ![Erweiterungsauswahl](../assets/icon-display-expand.png) Die **[!UICONTROL Advanced Braintree Settings]** -Abschnitt.

   ![Erweiterte Einstellungen](../configuration-reference/sales/assets/payment-methods-braintree-advanced-config.png){width="550" zoomable="yes"}

1. für **[!UICONTROL Vault Title]** Geben Sie einen beschreibenden Titel für Ihre Referenz ein, der den Tresor identifiziert, in dem Ihre Kundenkarteninformationen gespeichert sind.

1. Geben Sie die **[!UICONTROL Merchant Account ID]** von Ihrem Braintree-Konto.

   Wenn Sie das zu verwendende Händlerkonto nicht angeben, verarbeitet Braintree die Transaktion mit Ihrem standardmäßigen Händlerkonto.

1. Um ein schnelleres Checkout-Erlebnis mit Express-Zahlungsoptionen zu Beginn des Checkout-Prozesses zu bieten, einschließlich PayPal, PayLater, Apple Pay und Google Pay, legen Sie Folgendes fest **[!UICONTROL Enable Checkout Express Payments]** bis `Yes`.

1. Wenn Sie verhindern möchten, dass die Transaktion im Rahmen der erweiterten Prüfung der Betrugs-Tools zur Auswertung gesendet wird, legen Sie bei Bestellungen, die über den Administrator aufgegeben werden, Folgendes fest **[!UICONTROL Skip Fraud Checks on Admin Orders]** bis `Yes`.

1. Legen Sie die **[!UICONTROL Bypass Fraud Protection Threshold]** sodass die `Advanced Fraud Protection` Prüfungen werden umgangen, wenn der Schwellenwert erreicht oder überschritten wird.

   Wenn Sie dieses Feld leer lassen, wird diese Option deaktiviert.

1. Wenn das System eine Protokolldatei mit Interaktionen zwischen Ihrem Store und Braintree speichern soll, legen Sie Folgendes fest **[!UICONTROL Debug]** bis `Yes`.

1. Wenn Kunden den dreistelligen Sicherheitscode auf der Rückseite einer Kreditkarte bereitstellen müssen, legen Sie Folgendes fest **[!UICONTROL CVV Verification]** bis `Yes`.

   Wenn Sie die CVV-Überprüfung verwenden, stellen Sie sicher, dass Sie AVS und/oder CVV im _Einstellungen/Verarbeitung_ -Abschnitt Ihres Braintree-Kontos.

1. Um die Artikel im Warenkorb für alle Zahlungsmethoden zu senden, legen Sie Folgendes fest **[!UICONTROL Send Card Line Items]** bis `Yes`.

1. für **[!UICONTROL Credit Card Types]** Wählen Sie jede Kreditkarte aus, die von Ihrem Geschäft als Zahlung per Braintree akzeptiert wird.

   Zur Auswahl mehrerer Kartentypen halten Sie die Strg -Taste (PC) bzw. die Befehlstaste (Mac) gedrückt und klicken auf die einzelnen Optionen.

1. für **[!UICONTROL Sort Order]**, geben Sie eine Zahl ein, um die Reihenfolge zu bestimmen, in der die Braintree angezeigt wird, wenn sie mit anderen Zahlungsmethoden während des Checkouts aufgelistet wird.

## Schritt 4: Braintree-Webhook-Einstellungen abschließen

![Braintree Webhooks-Einstellungen](../configuration-reference/sales/assets/payment-methods-braintree-webhooks-config.png){width="600" zoomable="yes"}

1. set **[!UICONTROL Enable Webhook]** bis `Yes` , um die Webhook-Funktionalität für den Schutz vor Betrug, ACH-Zahlungen und lokale Zahlungsmethoden zu aktivieren.

1. Kopieren Sie die URL in das **[!UICONTROL Fraud Protection URL]** und fügen Sie es Ihrem Braintree-Konto als _[!UICONTROL Webhook Destination URL]_.

   >[!IMPORTANT]
   >
   >Diese URL muss sicher und öffentlich zugänglich sein.

1. Legen Sie die **[!UICONTROL Fraud Protection Approve Order Status]** Feld, um zu bestimmen, wann der Betrugsschutz vom Braintree genehmigt wird.

   Der ausgewählte Bestellstatus wird der Commerce-Bestellung zugewiesen.

1. Legen Sie die **[!UICONTROL Fraud Protection Reject Order Status]** Feld, das angibt, wann der Betrugsschutz vom Braintree abgelehnt wird.

   Der ausgewählte Bestellstatus wird der Commerce-Bestellung zugewiesen.

## Schritt 5: Länderspezifische Einstellungen vornehmen

1. set **[!UICONTROL Payment from Applicable Countries]** eine der folgenden Möglichkeiten:

   - `All Allowed Countries` - Kunden aus allen [Länder](../getting-started/store-details.md#country-options) Diese Zahlungsmethode kann verwendet werden, wenn sie in Ihrer Store-Konfiguration angegeben ist.
   - `Specific Countries` - Nach Auswahl dieser Option wird die _[!UICONTROL Payment from Specific Countries]_Liste angezeigt. Halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und wählen Sie jedes Land in der Liste aus, in dem Kunden in Ihrem Geschäft Einkäufe tätigen können.

   ![Länderspezifische Einstellungen](../configuration-reference/sales/assets/payment-methods-braintree-country-specific-config.png){width="600" zoomable="yes"}

1. Einrichten **[!UICONTROL Country Specific Credit Card Types]**:

   - Klick **[!UICONTROL Add]**.

   - Legen Sie die **[!UICONTROL Country]** und jede auswählen **[!UICONTROL Allowed Credit Card Type]**.

   - Wiederholen Sie dies, um die Kreditkarten zu identifizieren, die von jedem Land akzeptiert werden.

## Schritt 6: Vervollständigen Sie das ACH durch die Braintree-Einstellungen

![ACH durch Braintree](../configuration-reference/sales/assets/payment-methods-braintree-ach-config.png){width="600" zoomable="yes"}

1. Um ACH als Zahlungsoption mit Braintree einzubeziehen, stellen Sie Folgendes ein **[!UICONTROL Enable ACH Direct Debit]** bis `Yes`.

1. Kunden können ihre Einweg-ACH-Lastschriftzahlungsmethode tresoren und für die zukünftige Verwendung speichern. Nach dem Tresor können Kunden JEDES Lastschriftverfahren wiederverwenden, ohne ihre Zahlungsinformationen erneut eingeben oder authentifizieren zu müssen, falls festgelegt **[!UICONTROL Enable Vault for ACH Direct Debit]** bis `Yes`.

1. für **[!UICONTROL Sort Order]**, geben Sie eine Zahl ein, um die Reihenfolge zu bestimmen, in der die Zahlungsoption Braintree ACH angezeigt wird, wenn sie mit anderen Zahlungsoptionen während des Checkouts aufgelistet wird.

## Schritt 7: Vervollständigen Sie die [!UICONTROL Apple Pay] Über Braintree-Einstellungen

![ApplePay über Braintree-Einstellungen](../configuration-reference/sales/assets/payment-methods-braintree-applepay-config.png){width="600" zoomable="yes"}

1. Einzuschließen [!DNL Apple Pay] Als Zahlungsoption mit Braintree, festlegen **[!UICONTROL Enable ApplePay through Braintree]** bis `Yes`.

   Achten Sie auf Folgendes [Domain-Namen überprüfen](https://developer.paypal.com/braintree/docs/guides/apple-pay/configuration/javascript/v3) zuerst in Ihrem Braintree-Konto.

1. Wenn Sie Kundeninformationen sicher speichern möchten, sodass Kunden sie nicht bei jedem Kauf mit Apple Pay erneut eingeben müssen, legen Sie Folgendes fest **[!UICONTROL Enable Vault for ApplePay]** bis `Yes`.

1. set **[!UICONTROL Payment Action]** eine der folgenden Möglichkeiten:

   - `Authorize Only` - Genehmigt den Kauf und setzt die Mittel zurück. Der Betrag wird erst dann vom Bankkonto des Kunden abgehoben, wenn der Verkauf abgeschlossen ist _Gefangen_ Vom Händler.
   - `Intent Sale` - Der Betrag des Kaufs wird autorisiert und sofort vom Konto des Kunden zurückgezogen.

1. für **[!UICONTROL Merchant Name]** Geben Sie einen Text ein, der die Beschriftung angibt, die Kunden im Dialogfeld „Bezahlen“ in Apple angezeigt wird.

1. für **[!UICONTROL Sort Order]** Geben Sie eine Zahl ein, um die Reihenfolge zu bestimmen, in der [!DNL Apple Pay] Die Zahlungsoption wird angezeigt, wenn sie während des Checkouts mit anderen Zahlungsoptionen aufgelistet wird.

## Schritt 8: Vervollständigen Sie die Einstellungen für lokale Zahlungsmethoden

1. Um lokale Zahlungsmethoden als Zahlungsoption mit Braintree einzubeziehen, legen Sie Folgendes fest **[!UICONTROL Enable Local Payment Methods]** bis `Yes`.

1. für **[!UICONTROL Title]**, geben Sie den Text ein, der für die Beschriftung verwendet werden soll, die im Abschnitt Checkout-Zahlungsmethode angezeigt wird (Standardwert: `Local Payments`).

1. für **[!UICONTROL Fallback Button Text]** Geben Sie den Text ein, der für die Schaltfläche verwendet werden soll, die auf der Fallback-Braintree-Seite angezeigt wird, um den Kunden zurück zur Website zu bringen (z. B. `Complete Checkout`).

1. für **[!UICONTROL Redirect on Fail]**, geben Sie die URL ein, zu der Kunden umgeleitet werden sollen, wenn Transaktionen der lokalen Zahlungsmethode storniert werden, fehlschlagen oder auf Fehler stoßen. Dies sollte die Checkout-Zahlungsseite sein (z. B. `https://www.domain.com/checkout#payment`).

1. für **[!UICONTROL Allowed Payment Methods]**, wählen Sie die zu aktivierende lokale Zahlungsmethode aus.

   Optionen: `Bancontact` / `EPS` / `giropay` / `iDeal` / `Klarna Pay Now` / `SOFORT` / `MyBank` / `P24` / `SEPA/ELV Direct Debit` (noch nicht unterstützt)

   ![Einstellungen für lokale Zahlungsmethoden](../configuration-reference/sales/assets/payment-methods-braintree-local-payment-config.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Die gebündelte Braintree-Erweiterung unterstützt nicht alle in der aufgeführten lokalen Zahlungsmethoden. [Braintree-Entwicklerdokumentation](https://developer.paypal.com/braintree/docs/guides/local-payment-methods/overview). Weitere lokale Zahlungsmethoden werden derzeit entwickelt, um in zukünftigen Versionen unterstützt zu werden.

1. für **[!UICONTROL Sort Order]** Geben Sie eine Zahl ein, um die Reihenfolge zu bestimmen, in der die lokale Zahlungsmethode angezeigt wird, wenn sie mit anderen Zahlungsoptionen während des Checkouts aufgelistet wird.

## Schritt 9: Vervollständigen Sie die [!DNL Google Pay] Über Braintree-Einstellungen

![Google Pay-through-Braintree](../configuration-reference/sales/assets/payment-methods-braintree-googlepay-config.png){width="600" zoomable="yes"}

1. Einzuschließen [!DNL Google Pay] Als Zahlungsoption mit Braintree, festlegen **[!UICONTROL Enable GooglePay Through Braintree]** bis `Yes`.

1. Wenn Sie Kundeninformationen sicher speichern möchten, sodass Kunden sie nicht bei jedem Kauf mit Google Pay erneut eingeben müssen, legen Sie Folgendes fest **[!UICONTROL Enable Vault for GooglePay]** bis `Yes`.

1. set **[!UICONTROL Payment Action]** eine der folgenden Möglichkeiten:

   - `Authorize Only` - Genehmigt den Kauf und setzt die Mittel zurück. Der Betrag wird erst dann vom Bankkonto des Kunden abgehoben, wenn der Verkauf abgeschlossen ist _Gefangen_ Vom Händler.
   - `Intent Sale`  - Der Betrag des Kaufs wird autorisiert und sofort vom Konto des Kunden zurückgezogen.

1. set **[!UICONTROL Button Color]** So bestimmen Sie die Farbe von [!DNL Google Pay] Schaltfläche: `White` oder `Black`

1. für **[!UICONTROL Merchant ID]**, geben Sie Ihre MerchantID ein (bereitgestellt von Google).

1. für **[!UICONTROL Accepted Cards]** Wählen Sie den Kartentyp aus, den ein Kunde für die Bestellung verwenden kann, indem er [!DNL Google Pay].

   Optionen: `Visa` / `MasterCard` / `AMEX` / `Discover` / `JCB`

1. für **[!UICONTROL Sort Order]** Geben Sie eine Zahl ein, um die Reihenfolge zu bestimmen, in der [!DNL Google Pay] Wird angezeigt, wenn es während des Checkouts mit anderen Zahlungsoptionen aufgelistet wird.

## Schritt 10: Vervollständigen Sie die Einstellungen für Venmo durch Braintree.

1. Um Venmo als Zahlungsoption mit Braintree einzubeziehen, stellen Sie Folgendes ein **[!UICONTROL Enable Venmo through Braintree]** bis `Yes`.

1. set **[!UICONTROL Enable Vault for Venmo]** bis `Yes` um die Verwendung eines sicheren Tresors zur Speicherung des Venmo-Kontos von Kunden zu ermöglichen, sodass sich Kunden für zukünftige Transaktionen nicht erneut bei ihrem Venmo-Konto anmelden müssen.

   ![Venmo durch Braintree](../configuration-reference/sales/assets/payment-methods-braintree-venmo-config.png){width="600" zoomable="yes"}

1. set **[!UICONTROL Payment Action]** eine der folgenden Möglichkeiten:

   - `Authorize Only` - Genehmigt den Kauf und setzt die Mittel zurück. Der Betrag wird erst dann vom Bankkonto des Kunden abgehoben, wenn der Verkauf abgeschlossen ist _Gefangen_ Vom Händler.
   - `Intent Sale`  - Der Betrag des Kaufs wird autorisiert und sofort vom Konto des Kunden zurückgezogen.

1. für **[!UICONTROL Sort Order]** Geben Sie eine Zahl ein, um die Reihenfolge zu bestimmen, in der Venmo angezeigt wird, wenn es mit anderen Zahlungsoptionen während des Checkouts aufgelistet wird.

## Schritt 11: Vervollständigen Sie die PayPal durch Braintree-Einstellungen

![PayPal über Braintree-Einstellungen](./assets/braintree-paypal.png){width="550" zoomable="yes"}

1. Um PayPal als Zahlungsoption mit Braintree einzubeziehen, legen Sie Folgendes fest **[!UICONTROL Enable PayPal through Braintree]** bis `Yes`.

1. Geben Sie Ihre PayPal-Zahlungsmethode per Braintree an:

   >[!NOTE]
   >
   >Entweder **[!DNL PayPal Credit]** oder **[!DNL PayPal PayLater]** kann aktiviert werden. Beide Methoden können nicht gleichzeitig aktiviert werden.

   - Einzuschließen [!DNL PayPal Credit] Als Zahlungsoption mit Braintree, festlegen **[!UICONTROL Enable PayPal Credit through Braintree]** bis `Yes`.

     Wenn **PayPal über Braintree aktivieren** ist festgelegt auf `Yes`, nur dieses Feld wird angezeigt.

     >[!NOTE]
     >
     >PayPal-Guthaben ist nur in den Vereinigten Staaten und Großbritannien verfügbar. PayPal-Guthaben ist deaktiviert, wenn der ausgewählte Wert für die _[!UICONTROL Merchant Country]_Feld ist nicht `US` oder `UK`.

   - Einzuschließen [!DNL PayPal PayLater] Als Zahlungsoption mit Braintree, festlegen **[!UICONTROL Enable PayPal PayLater through Braintree]** bis `Yes`.

     Wenn **[!UICONTROL Enable PayPal PayLater through Braintree]** ist festgelegt auf `Yes`, nur dieses Feld wird angezeigt.

     Sie können auf Ihrer Site PayLater-Nachrichten für Angebote anzeigen, z. B. _Bezahlen in 3_, mit dem Kunden mit drei zinslosen monatlichen Zahlungen bezahlen können. Die Braintree-Integration kann Nachrichten auf Ihrer Site anzeigen, um diese Funktion zu bewerben. Sie können keine PayLater-Angebote mit anderen Inhalten, Marketing- oder Materialien bewerben.

1. für **[!UICONTROL Title]**, geben Sie einen Titel ein, der die Option Braintree-Zahlung per PayPal während des Checkouts identifiziert.

1. set **[!UICONTROL Vault Enabled]** bis `Yes` , um die Verwendung eines sicheren Tresors zum Speichern des PayPal-Kontos von Kunden zu ermöglichen. Ein Tresor-PayPal-Konto kann für zukünftige Transaktionen verwendet werden, was die Anzahl der Schritte für Kunden reduziert.

1. set **[!UICONTROL Send Cart Line Items for PayPal]** bis `Yes` , um die Positionen (Bestellpositionen) zusammen mit Geschenkgutscheinen, Geschenkverpackung für Artikel, Geschenkverpackung für Bestellung, Warenkredit, Versand und Steuer als Positionen an PayPal zu senden.

1. für **[!UICONTROL Sort Order]**, geben Sie eine Zahl ein, um die Reihenfolge zu bestimmen, in der die Zahlungsoption Braintree PayPal angezeigt wird, wenn sie während des Checkouts mit anderen Zahlungsoptionen aufgelistet wird.

1. So zeigen Sie Ihren Händlernamen anders an als in Ihrem [Store-Konfiguration](../getting-started/store-details.md#store-information), geben Sie den Namen in das Feld **[!UICONTROL Override Merchant Name]** -Feld, wie es angezeigt werden soll.

1. set **[!UICONTROL Payment Action]** eine der folgenden Möglichkeiten:

   - `Authorize Only` - Genehmigt den Kauf und setzt die Mittel zurück. Der Betrag wird erst dann vom Bankkonto des Kunden abgehoben, wenn der Verkauf abgeschlossen ist _Gefangen_ Vom Händler.
   - `Authorize and Capture` - Der Betrag des Kaufs wird autorisiert und sofort vom Konto des Kunden zurückgezogen.

1. set **[!UICONTROL Payment from Applicable Countries]** für Braintree-Transaktionen, die von PayPal verarbeitet werden, an einen der folgenden Empfänger:

   - `All Allowed Countries` - Kunden aus allen [Länder](../getting-started/store-details.md#country-options) Diese Zahlungsmethode kann verwendet werden, wenn sie in Ihrer Store-Konfiguration angegeben ist.
   - `Specific Countries` - Nach Auswahl dieser Option wird die _[!UICONTROL Payment from Specific Countries]_Liste angezeigt. Halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und wählen Sie jedes Land in der Liste aus, in dem Kunden in Ihrem Geschäft Einkäufe tätigen können.

1. Um von Kunden die Angabe einer Rechnungsadresse zu verlangen, legen Sie Folgendes fest: **[!UICONTROL Require Customer's Billing Address]** bis `Yes`.

   >[!NOTE]
   >
   >Diese Funktion muss vom technischen Support von PayPal für Ihr Konto aktiviert werden.

1. Um eine Protokolldatei der Interaktionen zwischen Ihrem Shop und PayPal über Braintree zu speichern, stellen Sie Folgendes ein **[!UICONTROL Debug]** bis `Yes`.

1. Um die PayPal-Schaltfläche sowohl auf der Seite mit dem Mini-Warenkorb als auch dem Warenkorb anzuzeigen, stellen Sie Folgendes ein: **[!UICONTROL Display on Shopping Cart]** bis `Yes`.

## Schritt 12: Festlegen der Stileinstellungen

1. für **[!UICONTROL Location]**, wo die PayPal-Schaltflächen und -Nachrichten gerendert werden: `Mini-Cart and Cart Page`, `Checkout Page`, oder `Product Page`

   ![PayPal-Stileinstellungen](../configuration-reference/sales/assets/payment-methods-braintree-paypal-styling.png){width="600" zoomable="yes"}

### [!UICONTROL Mini-Cart and Cart Page]

Die Optionen und Einstellungen in diesem Abschnitt variieren je nach der Einstellung in der _[!UICONTROL Location]_Feld.

1. set **[!UICONTROL PayPal Button Type]** zu einem von drei Schaltflächentypen: `PayPal Button` / `PayPal Pay Later Button` / `PayPal Credit Button`

**[!UICONTROL PayPal Button]**

Die Optionen und Einstellungen in diesem Abschnitt variieren je nach dem in der _[!UICONTROL PayPal Button Type]_Feld.

1. Um die PayPal-Schaltfläche auf der Storefront am ausgewählten Ort anzuzeigen, stellen Sie **[!UICONTROL Show PayPal Button]** bis `Yes`.

1. für **[!UICONTROL Button Label]**, wählen Sie die Beschriftung der PayPal-Schaltfläche aus: `Paypal`, `Checkout`, `Buynow`, oder `Pay`

1. für **[!UICONTROL Color]**, wählen Sie die Farbe der PayPal-Schaltfläche: `Blue`, `Black`, `Gold`, oder `Silver`

1. für **[!UICONTROL Shape]**, wählen Sie die Form der PayPal-Schaltfläche: `Pill` oder `Rectangle`

1. für **[!UICONTROL Size (Deprecated)]**, wählen Sie die Größe der PayPal-Schaltfläche: `Medium`, `Large`, oder `Responsive`

>[!NOTE]
>
>Die **[!DNL Size(Deprecated)]** Das Konfigurationsfeld ist veraltet und wird nicht mehr zur Gestaltung der PayPal-Schaltflächen verwendet.

**[!UICONTROL PayLater Messaging]**

1. Zu zeigen [!DNL PayLater] Messaging in der Storefront am ausgewählten Speicherort, festlegen **[!UICONTROL Show PayLater Messaging]** bis `Yes`.

   Diese Meldung enthält die Anzeige von [!DNL PayLater] Messaging für verfügbare Angebote ([Es gelten Einschränkungen](https://developer.paypal.com/docs/checkout/pay-later/us/)).

1. für **[!UICONTROL Message Layout]**, wählen Sie die [!DNL PayLater] Nachrichten-Layout: `Text` oder `Flex`

1. für **[!UICONTROL Logo]**, wählen Sie den PayPal-Logotyp aus: `Inline`, `Primary`, `Alternative`, oder `None`

1. für **[!UICONTROL Logo Position]**, wählen Sie die Position des PayPal-Logos: `Left`, `Right`, oder `Top`

1. für **[!UICONTROL Text Color]**, wählen Sie die [!DNL PayLater] Textfarbe der Nachricht: `Black`, `White`, `Monochrome`, oder `Grayscale`

Wenn diese Optionen festgelegt sind, können Sie die Vorschau der PayPal-Schaltflächen und PayLater-Nachrichten sehen. Es gibt Steuerelemente, mit denen Sie die Einstellungen anwenden oder die Werte zurücksetzen können:

- Um die ausgewählten Stileinstellungen für Schaltflächen und PayLater-Messaging zu speichern und sie auf die aktuelle Position und den aktuellen Schaltflächentyp anzuwenden, klicken Sie auf **[!UICONTROL Apply]**.

- Um die ausgewählten Stileinstellungen für Schaltflächen und PayLater-Messaging-Werte zu speichern und sie auf alle Schaltflächentypen und Positionen anzuwenden, klicken Sie auf **[!UICONTROL Apply to All Buttons]**.

- Um die Stileinstellungen auf die empfohlenen Standardwerte für Schaltflächen und PayLater-Messaging zurückzusetzen und sie auf alle Schaltflächentypen und Positionen anzuwenden, klicken Sie auf **[!UICONTROL Reset to Recommended Defaults]**.

## Schritt 13: 3D-Verifizierungseinstellungen abschließen

1. Wenn Sie einen Verifizierungsschritt für Kunden hinzufügen möchten, die Kreditkarten verwenden, die in einem Verifizierungsprogramm registriert sind (z. B. _Verifiziert durch VISA_), festlegen **[!UICONTROL 3D Secure Verification]** bis `Yes`.

   Während des Prozesses wird der Transaktionsbetrag, der zur Überprüfung übermittelt wird, mit dem Betrag verglichen, der zur Autorisierung gesendet wird.

2. Um die 3D-Secure-Anfrage für alle Transaktionen immer herauszufordern, legen Sie Folgendes fest: **[!UICONTROL Always request 3DS]** bis `Yes`.

3. für **[!UICONTROL Threshold Amount]**, geben Sie den Mindestbestellbetrag ein, der für die Trigger-3D-Verifizierung erforderlich ist.

4. set **[!UICONTROL Verify for Applicable Countries]** eine der folgenden Möglichkeiten:

   - `All Allowed Countries` - Kunden aus allen [Länder](../getting-started/store-details.md#country-options) Diese Zahlungsmethode kann verwendet werden, wenn sie in Ihrer Store-Konfiguration angegeben ist.
   - `Specific Countries` - Nach Auswahl dieser Option wird die _[!UICONTROL Verify for Specific Countries]_Liste angezeigt. Halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und wählen Sie jedes Land in der Liste aus, in dem Kunden in Ihrem Geschäft Einkäufe tätigen können.

   ![3D-Verifizierungseinstellungen](../configuration-reference/sales/assets/payment-methods-braintree-3d-secure-verify-config.png){width="600" zoomable="yes"}

## Schritt 14: Einrichten der dynamischen Braintree-Deskriptoren

Die folgenden Deskriptoren werden verwendet, um Käufe auf Kunden-Kreditkartenauszügen zu identifizieren. Sie können die Anzahl der Rückbelastungen reduzieren, indem Sie das Unternehmen, das mit jedem Kauf verbunden ist, eindeutig identifizieren. Wenn dynamische Deskriptoren für Ihr Konto nicht aktiviert sind, wenden Sie sich an den Braintree-Support.

![Dynamische Deskriptoren](../configuration-reference/sales/assets/payment-methods-braintree-dynamic-config.png){width="600" zoomable="yes"}

1. Geben Sie den dynamischen Deskriptor für das **[!UICONTROL Name]**, **[!UICONTROL Phone]**, und **[!UICONTROL URL]** Gemäß diesen Richtlinien:

   - **[!UICONTROL Name]** - Der Namensdeskriptor besteht aus zwei Teilen, die durch ein Sternchen (*) voneinander getrennt sind. Beispiel:

     `company*myproduct`

     Der erste Teil des Deskriptors identifiziert das Unternehmen oder die DBA, und der zweite Teil identifiziert das Produkt. Die Länge des `company` und `product` Teile des Deskriptors können auf folgende Weise für eine kombinierte Länge von bis zu 22 Zeichen zugewiesen werden.

     **_Zeichen im Namensdeskriptor_**

     _Option 1:_ `Company` muss drei Zeichen lang sein, `Product` Kann bis zu 18 Zeichen lang sein

     _Option 2:_ `Company` muss sieben Zeichen lang sein, `Product` Kann bis zu 14 Zeichen lang sein

     _Option 3_: `Company` muss 12 Zeichen lang sein, `Product` Kann bis zu neun Zeichen lang sein

   - **[!UICONTROL Phone]** - Der Telefondeskriptor muss 10 bis 14 Zeichen lang sein und darf nur Zahlen, Gedankenstriche, Klammern und Punkte enthalten. Beispiel:

     `9999999999`

     `(999) 999-9999`

     `999.999.9999`

   - **[!UICONTROL URL]** - Der URL-Deskriptor stellt Ihren Domain-Namen dar und kann bis zu 13 Zeichen lang sein. Beispiel:

     `company.com`

1. Wenn die Braintree-Konfiguration abgeschlossen ist, klicken Sie auf **[!UICONTROL Save Config]**.

## 2.4 Aktualisierungshinweise

Ab Adobe Commerce und Magento Open Source 2.4.0 ist die Braintree-Erweiterung in der Version enthalten. Wenn Sie von einer Version vor 2.4.0, in der die Marketplace-Braintree-Erweiterung installiert ist, auf Commerce 2.4.x migrieren, müssen Sie diese Erweiterung deinstallieren (`paypal/module-braintree` oder `gene/module-braintree`) und alle Code-Anpassungen aktualisieren, um die `PayPal_Braintree` Namespace statt `Magento_Braintree`. Konfigurationseinstellungen aus der gebündelten Haupterweiterung Commerce Braintree Payments und der auf Commerce Marketplace verteilten Erweiterung bleiben bestehen und Zahlungen, die mit diesen Vorgängerversionen platziert wurden, können weiterhin wie gewohnt erfasst, storniert oder erstattet werden.

[1]: https://www.braintreepayments.com/
[2]: https://developers.braintreepayments.com/reference/general/testing/php
