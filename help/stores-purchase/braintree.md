---
title: Braintree
description: Erfahren Sie, wie Sie Braintree als online Zahlungslösung auf Ihrem Geschäft einrichten.
exl-id: 781b385f-926e-4047-b7da-6f7c090d75d8
feature: Payments
source-git-commit: bb083698aff1da145bbb661307148c9223d5b545
workflow-type: tm+mt
source-wordcount: '2873'
ht-degree: 0%

---

# Braintree

>[!IMPORTANT]
>
>Wenn Sie Hilfe bei unerwarteten Abbuchungen auf Ihrem Karte benötigen, Visit Sie die Mitgliedschaft[&#128279;](https://helpx.adobe.com/manage-account/using/cancel-subscription.html) Seite zum Stornieren, um Unterstützung zu erhalten.

Braintree bietet eine vollständig anpassbare Checkout Erlebnis mit Betrugserkennung und PayPal-Integration. Es unterstützt [!DNL Apple Pay], [!DNL Google Pay], ACH, Venmo und lokale Zahlungsmethoden. Braintree reduziert den PCI Compliance-Aufwand für Händler, da die Transaktion auf dem Braintree System stattfindet. Die Integration von Braintree Payments wird von [GENE Commerce](https://www.gene.co.uk/gene-braintree-payments/) entwickelt.

>[!NOTE]
>
>Wenn Sie ein Upgrade auf 2.4.x von einer früheren Version von Adobe Systems Commerce oder Magento Open Source durchführen, auf dem die Braintree Erweiterung von Commerce Marketplace installiert ist, lesen Sie die [2.4-Upgradehinweise](#24-upgrade-notes) am Ende dieser Seite.


## Schritt 1: Holen Sie sich Ihre Braintree-Anmeldeinformationen

OK zu [Braintree Payments][1] und melden Sie sich für ein Konto an.

## Schritt 2: Alle Applikationen die Grundeinstellungen

1. Wechseln Sie in der _Admin-Seitenleiste_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich, und **[!UICONTROL Sales]** wählen Sie **[!UICONTROL Payment Methods]** aus.

   - Wenn Ihre Commerce-Installation über mehrere Websites, Shops oder Ansichten verfügt, wählen Sie in der oberen linken Ecke aus, wo **[!UICONTROL Store View]** die Konfiguration angewendet wird.

   - _[!UICONTROL Merchant Location]_&#x200B;Vergewissern Sie sich im Abschnitt, dass der **[!UICONTROL Merchant Country]**&#x200B;Standort Ihres Unternehmens festgelegt ist.

1. Klicken Sie unter _[!UICONTROL Recommended Solutions]_&#x200B;_[!UICONTROL Braintree Payments] im Abschnitt (von [GENE Commerce](https://www.gene.co.uk/gene-braintree-payments/) v4.7.0 - [Versionshinweise](https://support.gene.co.uk/support/solutions/articles/35000278668)_) auf **[!UICONTROL Configure]**.

   ![Konfigurieren Braintree](./assets/braintree-payments.png){width="600" zoomable="yes"}

1. Geben **[!UICONTROL Title]** Sie für einen Titel ein, der Braintree als Zahlungsoption beim Checkout identifiziert.

1. Festlegen der aktuellen Vorgänge **[!UICONTROL Environment]** für Braintree Transaktionen nach `Sandbox` oder `Production`

   Verwenden Sie beim Testen der Konfiguration in einer Sandbox nur [Gutschriften Karte Zahlen][2] , die von Braintree empfohlen werden. Wenn Sie bereit sind, mit Braintree in die Produktion zu gehen, legen **[!UICONTROL Environment]** Sie .`Production`

   ![Standard Credentials Einstellungen](../configuration-reference/sales/assets/payment-methods-braintree-basic-config.png){width="600" zoomable="yes"}

1. **[!UICONTROL Payment Action]** Festlegen auf eine der folgenden Optionen:

   - `Authorize Only` - Genehmigt den Kauf und sperrt das Geld. Der Betrag wird erst dann von der Bank des Kunden abgehoben Konto, wenn der Verkauf __ von der Händler.|
   - `Intent Sale`  - Der Kaufbetrag wird autorisiert und sofort vom Konto des Kunden abgezogen. **_Hinweis:_** Dieser Wert wurde  _in 2.3.x und früheren Versionen autorisiert und Capture_ .|

1. Geben Sie in Ihrem Braintree Konto ein **[!UICONTROL Sandbox Merchant ID / Merchant ID]** .

1. Geben Sie die folgenden Anmeldedaten aus Ihrem Braintree Konto ein:

   - **[!UICONTROL Sandbox Public Key / Public Key]**
   - **[!UICONTROL Sandbox Private Key / Private Key]**

   >[!NOTE]
   >
   >Es gibt separate Felder für beide **Umgebungen (Sandbox und Produktion),** und die anderen Felder werden gerendert, je nachdem, welche Umgebung ausgewählt ist.

1. Klicken Sie vor dem Speichern der Konfiguration auf die Schaltfläche **[!UICONTROL Validate Credentials]** , um Ihre Anmeldedaten zu überprüfen.

1. **[!UICONTROL Enable Card Payments]** Festlegen bis `Yes`.

1. Wenn Sie die Möglichkeit haben möchten, Kundeninformationen sicher zu Geschäft, damit Kunden sie nicht bei jedem Kauf erneut eingeben müssen, setzen Sie **[!UICONTROL Enable Vault for Card Payments]** auf `Yes`.

1. Wenn Sie möchten, dass ein Kunde die CVV-Nummer für seine Tresor-Karte bei jedem Kauf überprüft, setzen Sie **[!UICONTROL Enable Vault CVV Re-verification]** auf `Yes`.

## Schritt 3: Erweiterte Einstellungen Alle Applikationen

1. ![Erweitern Erweiterung Selektor](../assets/icon-display-expand.png) den **[!UICONTROL Advanced Braintree Settings]** Abschnitt.

   ![Erweiterte Einstellungen](../configuration-reference/sales/assets/payment-methods-braintree-advanced-config.png){width="550" zoomable="yes"}

1. Geben **[!UICONTROL Vault Title]** Sie für einen beschreibenden Titel als Referenz ein, der den Tresor identifiziert, in dem Ihre Kunden Karte Informationen gespeichert sind.

1. Geben Sie in Ihrem Braintree Konto ein **[!UICONTROL Merchant Account ID]** .

   Wenn Sie die zu verwendende Händler Konto nicht angeben, verarbeitet Braintree die Transaktion mit Ihrer Standard Händler Konto.

1. Um eine schnellere Checkout zu ermöglichen, Erlebnis Express-Zahlungsoptionen zu Beginn der Checkout-Prozess, einschließlich PayPal, PayLater, Apple Pay und Google Pay, die auf **[!UICONTROL Enable Checkout Express Payments]** eingestellt sind `Yes`.

1. Wenn Sie verhindern möchten, dass die Transaktion im Rahmen von Erweitert Fraud Werkzeuge-Überprüfungen zur Auswertung gesendet wird, setzen Sie bei Bestellungen, die über den Administrator aufgegeben wurden, auf **[!UICONTROL Skip Fraud Checks on Admin Orders]** `Yes`.

1. **[!UICONTROL Bypass Fraud Protection Threshold]** Festlegen, damit die `Advanced Fraud Protection` Prüfungen umgangen werden, wenn die Schwellenwert erfüllt oder überschritten wird.

   Wenn Sie dieses Feld leer lassen, wird diese Option deaktiviert.

1. Wenn das System eine Protokolldatei der Interaktionen zwischen Ihrem Geschäft und Braintree speichern soll, setzen **[!UICONTROL Debug]** Sie auf `Yes`.

1. Wenn Sie von den Kunden verlangen möchten, dass sie die dreistellige Sicherheitscode auf der Rückseite einer Kredit-Karte angeben, legen Sie **[!UICONTROL CVV Verification]** fest `Yes`.

   Wenn Sie die CVV-Verifizierung verwenden, stellen Sie sicher, dass AVS und/oder CVV im _Abschnitt Einstellungen/Verarbeitung_ Ihres Braintree Konto aktiviert ist.

1. Um die Artikel im Warenkorb für alle Zahlungsmethoden zu senden, setzen Sie **[!UICONTROL Send Card Line Items]** auf `Yes`.

1. Wählen Sie **[!UICONTROL Credit Card Types]** jede Kreditkarte aus, die von Ihrem Geschäft als Zahlung über Braintree akzeptiert wird.

   Zur Auswahl mehrerer Kartentypen halten Sie die Strg -Taste (PC) bzw. die Befehlstaste (Mac) gedrückt und klicken auf die einzelnen Optionen.

1. Geben **[!UICONTROL Sort Order]** Sie für eine Zahl ein, um die Sequenz zu bestimmen, in der Braintree angezeigt wird, wenn sie während der Checkout mit anderen Zahlungsmethoden aufgeführt wird.

## Schritt 4: Alle Applikationen die Braintree Webhook-Einstellungen

![Braintree Webhooks Einstellungen](../configuration-reference/sales/assets/payment-methods-braintree-webhooks-config.png){width="600" zoomable="yes"}

1. **[!UICONTROL Enable Webhook]** Festlegen, um die Webhook-Funktionen für Betrugsschutz, ACH-Zahlungen und lokale Zahlungsmethoden zu `Yes` aktivieren.

1. Kopie die URL im **[!UICONTROL Fraud Protection URL]** Feld und fügen Sie sie Ihrem Braintree Konto als _[!UICONTROL Webhook Destination URL]_&#x200B;hinzu.

   >[!IMPORTANT]
   >
   >Diese URL muss sicher und öffentlich zugänglich sein.

1. Festlegen das **[!UICONTROL Fraud Protection Approve Order Status]** Feld, um festzustellen, wann der Betrugsschutz von Braintree genehmigt wurde.

   Der ausgewählte bestellen Status wird der Commerce-bestellen zugewiesen.

1. Festlegen das **[!UICONTROL Fraud Protection Reject Order Status]** Feld, um festzustellen, wann der Betrugsschutz von Braintree abgelehnt wird.

   Der ausgewählte bestellen Status wird der Commerce-bestellen zugewiesen.

## Schritt 5: Länderspezifische Einstellungen Alle Applikationen

1. **[!UICONTROL Payment from Applicable Countries]** Festlegen auf eine der folgenden Optionen:

   - `All Allowed Countries` - Kunden aus allen [Ländern,](../getting-started/store-details.md#country-options) die in Ihrer Geschäft-Konfiguration angegeben sind, können diese Zahlungsmethode verwenden.
   - `Specific Countries` - Nachdem Sie diese Option ausgewählt haben, wird die _[!UICONTROL Payment from Specific Countries]_&#x200B;Liste angezeigt. Halten Sie die Strg-Taste (PC) oder die Befehl-Taste (Mac) gedrückt und wählen Sie jedes Land im Liste aus, in dem Kunden bei Ihrem Geschäft einkaufen können.

   ![Land-spezifische Einstellungen](../configuration-reference/sales/assets/payment-methods-braintree-country-specific-config.png){width="600" zoomable="yes"}

1. So richten Sie Folgendes ein **[!UICONTROL Country Specific Credit Card Types]**:

   - Klicken Sie auf **[!UICONTROL Add]**.

   - Festlegen die **[!UICONTROL Country]** und wählen Sie jede **[!UICONTROL Allowed Credit Card Type]**.

   - Wiederholen Sie diesen Vorgang, um die Kreditkarten zu identifizieren, die von jedem Land akzeptiert werden.

## Schritt 6: Alle Applikationen des ACH über Braintree Einstellungen

![Von ACH bis Braintree](../configuration-reference/sales/assets/payment-methods-braintree-ach-config.png){width="600" zoomable="yes"}

1. Um ACH als Zahlungsoption mit Braintree einzuschließen, legen Sie **[!UICONTROL Enable ACH Direct Debit]** fest `Yes`.

1. Kunden können ihre Einweg-ACH-Lastschrift-Zahlungsmethode in den Tresor übernehmen und für die zukünftige Verwendung Geschäft. Nach dem Tresor können Kunden das ACH-Lastschriftverfahren wiederverwenden, ohne ihre Zahlungsinformationen erneut eingeben oder authentifizieren zu müssen, wenn **[!UICONTROL Enable Vault for ACH Direct Debit]** sie auf eingestellt sind `Yes`.

1. Geben **[!UICONTROL Sort Order]** Sie für eine Zahl ein, um die Sequenz zu bestimmen, in der die Braintree ACH-Zahlungsoption angezeigt wird, wenn sie während der Checkout mit anderen Zahlungsoptionen aufgeführt wird.

## Schritt 7: Alle Applikationen die Einstellungen für die durchgehende [!UICONTROL Apple Pay] Braintree

![ApplePay über Braintree Einstellungen](../configuration-reference/sales/assets/payment-methods-braintree-applepay-config.png){width="600" zoomable="yes"}

1. Um als Zahlungsoption mit Braintree aufzunehmen [!DNL Apple Pay] , setzen Sie **[!UICONTROL Enable ApplePay through Braintree]** auf `Yes`.

   Stellen Sie sicher, dass Sie [zuerst Ihren Domainnamen](https://developer.paypal.com/braintree/docs/guides/apple-pay/configuration/javascript/v3) in Ihrem Braintree Konto verifizieren.

1. Wenn Sie die Möglichkeit haben möchten, Kundeninformationen sicher zu Geschäft, damit Kunden sie nicht jedes Mal neu eingeben müssen, wenn sie einen Kauf mit Apple Pay tätigen, legen Sie **[!UICONTROL Enable Vault for ApplePay]** `Yes`fest.

1. **[!UICONTROL Payment Action]** Festlegen auf eine der folgenden Optionen:

   - `Authorize Only` - Genehmigt den Kauf und sperrt das Geld. Der Betrag wird erst dann von der Bank des Kunden abgehoben Konto, wenn der Verkauf vom Händler erfasst _wird_.
   - `Intent Sale` - Der Kaufbetrag wird autorisiert und sofort vom Konto des Kunden abgezogen.

1. Geben **[!UICONTROL Merchant Name]** Sie für einen Text ein, der die Beschriftung angibt, die Kunden im Dialogfeld &quot;Apple Pay&quot; angezeigt wird.

1. Geben **[!UICONTROL Sort Order]** Sie für eine Zahl ein, um die Sequenz zu bestimmen, in der die Zahlungsoption angezeigt wird, [!DNL Apple Pay] wenn sie während der Checkout mit anderen Zahlungsoptionen aufgeführt wird.

## Schritt 8: Alle Applikationen die Einstellungen für lokale Zahlungsmethoden

1. Um lokale Zahlungsmethoden als Zahlungsoption mit Braintree einzuschließen, legen Sie **[!UICONTROL Enable Local Payment Methods]** fest `Yes`.

1. Geben **[!UICONTROL Title]** Sie für den Text für das Etikett ein, das im Abschnitt Checkout Zahlungsmethode angezeigt wird (Standardwert: `Local Payments`).

1. Geben **[!UICONTROL Fallback Button Text]** Sie für den Text ein, der für die Button verwendet werden soll, die auf dem Fallback-Braintree Seite angezeigt wird, um den Kunden zurück zur Website zu führen (z. B `Complete Checkout`. ).

1. Geben **[!UICONTROL Redirect on Fail]** Sie für die URL ein, auf die Kunden umgeleitet werden sollen, wenn Transaktionen mit lokalen Zahlungsmethoden abgebrochen werden, fehlschlagen oder Fehler auftreten. Es sollte die Checkout Zahlungs Seite sein (z. B `https://www.domain.com/checkout#payment`. ).

1. Wählen **[!UICONTROL Allowed Payment Methods]** Sie für die lokale Zahlungsmethode aus, die aktiviert werden soll.

   Optionen: `Bancontact` / `EPS` / `giropay` / `iDeal` / `Klarna Pay Now` / `SOFORT` / `MyBank` / `P24` / `SEPA/ELV Direct Debit` (noch nicht unterstützt)

   ![Einstellungen für lokale Zahlungsmethoden](../configuration-reference/sales/assets/payment-methods-braintree-local-payment-config.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Die gebündelte Braintree-Erweiterung unterstützt nicht alle in der Entwicklerdokumentation zu [Braintree aufgeführten lokalen ](https://developer.paypal.com/braintree/docs/guides/local-payment-methods/overview). Weitere lokale Zahlungsmethoden werden derzeit entwickelt, um in zukünftigen Versionen unterstützt zu werden.

1. Geben Sie **[!UICONTROL Sort Order]** eine Zahl ein, um die Reihenfolge zu bestimmen, in der die lokale Zahlungsmethode angezeigt wird, wenn sie während des Checkouts mit anderen Zahlungsoptionen aufgelistet wird.

## Schritt 9: [!DNL Google Pay] über Braintree-Einstellungen abschließen

![Google Pay über Braintree](../configuration-reference/sales/assets/payment-methods-braintree-googlepay-config.png){width="600" zoomable="yes"}

1. Um als Zahlungsoption mit Braintree aufzunehmen [!DNL Google Pay] , setzen Sie **[!UICONTROL Enable GooglePay Through Braintree]** auf `Yes`.

1. Wenn Sie die Möglichkeit haben möchten, Kundeninformationen sicher zu Geschäft, damit Kunden sie nicht bei jedem Einkauf mit Google Pay erneut eingeben müssen, legen Sie **[!UICONTROL Enable Vault for GooglePay]** `Yes`fest.

1. **[!UICONTROL Payment Action]** Festlegen auf eine der folgenden Optionen:

   - `Authorize Only` - Genehmigt den Kauf und sperrt das Geld. Der Betrag wird erst dann von der Bank des Kunden abgehoben Konto, wenn der Verkauf vom Händler erfasst _wird_.
   - `Intent Sale`  - Der Kaufbetrag wird autorisiert und sofort vom Konto des Kunden abgezogen.

1. **[!UICONTROL Button Color]** Festlegen, um die Farbe der [!DNL Google Pay] Button zu bestimmen: `White` oder`Black`

1. Geben **[!UICONTROL Merchant ID]** Sie für Ihre (von Google bereitgestellte) MerchantID ein.

1. Wählen Sie für **[!UICONTROL Accepted Cards]** den Kartentyp aus, mit dem ein Kunde eine bestellen platzieren [!DNL Google Pay]kann.

   Optionen: `Visa` / `MasterCard` / `AMEX` / / `Discover` `JCB`

1. Geben Sie **[!UICONTROL Sort Order]** eine Zahl ein, um die Reihenfolge zu bestimmen, in der die [!DNL Google Pay] angezeigt wird, wenn sie während des Checkouts mit anderen Zahlungsoptionen aufgelistet wird.

## Schritt 10: Venmo durch Braintree-Einstellungen fertig stellen

1. Um Venmo als Zahlungsoption mit Braintree einzubeziehen, setzen Sie **[!UICONTROL Enable Venmo through Braintree]** auf `Yes`.

1. Legen Sie **[!UICONTROL Enable Vault for Venmo]** auf `Yes` fest, um die Verwendung eines sicheren Tresors zum Speichern des Venmo-Kontos von Kunden zu ermöglichen, sodass sich Kunden für zukünftige Transaktionen nicht erneut bei ihrem Venmo-Konto anmelden müssen.

   ![Venmo durch Braintree](../configuration-reference/sales/assets/payment-methods-braintree-venmo-config.png){width="600" zoomable="yes"}

1. **[!UICONTROL Payment Action]** Festlegen auf eine der folgenden Optionen:

   - `Authorize Only` - Genehmigt den Kauf und sperrt das Geld. Der Betrag wird erst dann von der Bank des Kunden abgehoben Konto, wenn der Verkauf vom Händler erfasst _wird_.
   - `Intent Sale`  - Der Kaufbetrag wird autorisiert und sofort vom Konto des Kunden abgezogen.

1. Geben **[!UICONTROL Sort Order]** Sie für eine Zahl ein, um die Sequenz zu bestimmen, in der Venmo angezeigt wird, wenn es während der Checkout mit anderen Zahlungsoptionen aufgeführt wird.

## Schritt 11: Alle Applikationen Sie die PayPal über Braintree Einstellungen

![PayPal durch Braintree Einstellungen 1](../configuration-reference/sales/assets/payment-methods-braintree-paypal-config-1.png){width="550" zoomable="yes"}

1. Um PayPal als Zahlungsoption mit Braintree einzuschließen, setzen Sie **[!UICONTROL Enable PayPal through Braintree]** auf `Yes`.

1. Geben Sie Ihre PayPal über Braintree Zahlungsmethode an:

   >[!NOTE]
   >
   >&quot;Entweder **[!DNL PayPal Credit]** oder&quot; **[!DNL PayPal PayLater]** kann aktiviert werden. Es ist nicht möglich, beide Methoden gleichzeitig zu aktivieren.

   - Um als Zahlungsoption mit Braintree aufzunehmen [!DNL PayPal Credit] , setzen Sie **[!UICONTROL Enable PayPal Credit through Braintree]** auf `Yes`.

     Wenn **&quot;PayPal über Braintree** aktivieren auf `Yes`festgelegt ist, wird nur dieses Feld angezeigt.

     >[!NOTE]
     >
     >PayPal Credit ist nur in den USA und im Vereinigten Königreich verfügbar. PayPal Gutschrift wird deaktiviert, wenn der ausgewählte Wert für das _[!UICONTROL Merchant Country]_&#x200B;Feld nicht `US` oder `UK`ist.

   - Um als Zahlungsoption mit Braintree aufzunehmen [!DNL PayPal PayLater] , setzen Sie **[!UICONTROL Enable PayPal PayLater through Braintree]** auf `Yes`.

     Wenn **[!UICONTROL Enable PayPal PayLater through Braintree]** auf `Yes`eingestellt ist, wird nur dieses Feld angezeigt.

     Sie können PayLater-Messaging auf Ihrer Website für Angebote anzeigen, z. B _. Pay in 3_, mit denen Kunden mit drei monatlichen Interesse-gratis-Zahlungen bezahlen können. Die Braintree Integration kann Nachrichten auf Ihrer Website anzeigen, die für diese Funktion werben. Sie können PayLater-Angebote nicht mit anderen Inhalte, Marketing oder Materialien bewerben.

1. Geben Sie für **[!UICONTROL Title]** einen Titel ein, der die Option Braintree Zahlung nach PayPal während der Checkout identifiziert.

1. **[!UICONTROL Vault Enabled]** Festlegen, um die Verwendung eines sicheren Tresors für die Geschäft PayPal Konto der Kunden zu `Yes` ermöglichen. Vaulted PayPal Konto kann für zukünftige Transaktionen verwendet werden, wodurch die Anzahl der Schritte für Kunden reduziert wird.

1. **[!UICONTROL Send Cart Line Items for PayPal]** `Yes` Festlegen, um die Werbebuchungen (bestellen Artikel) zusammen mit Geschenkkarten, Geschenkverpackung für Artikel, Geschenkverpackung für bestellen, Store-Guthaben, Versand und Steuern als Einzelposten an PayPal zu senden.

1. Geben **[!UICONTROL Sort Order]** Sie für eine Zahl ein, um die Sequenz zu bestimmen, in der die Braintree PayPal Zahlungsoption angezeigt wird, wenn sie während der Checkout zusammen mit anderen Zahlungsoptionen aufgeführt wird.

1. Wenn Sie Ihren Händler Namen anders anzeigen möchten als in Ihrer [Geschäft Konfiguration](../getting-started/store-details.md#store-information), geben Sie den Namen so in das **[!UICONTROL Override Merchant Name]** Feld ein, wie er angezeigt werden soll.

1. **[!UICONTROL Payment Action]** Festlegen auf eine der folgenden Optionen:

   - `Authorize Only` - Genehmigt den Kauf und sperrt das Geld. Der Betrag wird erst dann von der Bank des Kunden abgehoben Konto, wenn der Verkauf vom Händler erfasst _wird_.
   - `Authorize and Capture` - Der Kaufbetrag wird autorisiert und sofort vom Konto des Kunden abgezogen.

1. **[!UICONTROL Payment from Applicable Countries]** Festlegen eine der folgenden Optionen für Braintree Transaktionen, die von PayPal verarbeitet werden:

   - `All Allowed Countries` - Kunden aus allen [Ländern,](../getting-started/store-details.md#country-options) die in Ihrer Geschäft-Konfiguration angegeben sind, können diese Zahlungsmethode verwenden.
   - `Specific Countries` - Nachdem Sie diese Option ausgewählt haben, wird die _[!UICONTROL Payment from Specific Countries]_&#x200B;Liste angezeigt. Halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und wählen Sie jedes Land in der Liste aus, in dem Kunden in Ihrem Geschäft Einkäufe tätigen können.

   ![PayPal über Braintree Settings 2](../configuration-reference/sales/assets/payment-methods-braintree-paypal-config-2.png){width="550" zoomable="yes"}

1. Um von Kunden die Angabe einer Rechnungsadresse zu verlangen, setzen Sie **[!UICONTROL Require Customer's Billing Address]** auf `Yes`.

   >[!NOTE]
   >
   >Diese Funktion muss vom technischen Support von PayPal für Ihr Konto aktiviert werden.

1. Um die Seite zur Bestellüberprüfung für PayPal Express zu überspringen, setzen Sie **[!UICONTROL Skip Order Review Step]** auf `Yes`.

   Für Kunden, die mit PayPal Express bezahlen: Wenn Sie möchten, dass Kunden vor Abschluss der Zahlung zu einem Bewertungs-Seite weitergeleitet werden, stellen Sie dies auf `No`ein. Wenn Sie möchten, dass Kunden die Bewertungs Seite überspringen, stellen Sie sie auf `Yes`ein.

1. Um eine Protokolldatei der Interaktionen zwischen Ihren Geschäft und PayPal über Braintree zu speichern, legen Sie **[!UICONTROL Debug]** fest `Yes`:

1. Um die PayPal Button sowohl auf der Mini-Warenkorb als auch auf der Warenkorb Seite anzuzeigen, stellen Sie **[!UICONTROL Display on Shopping Cart]** auf `Yes`ein.

1. Um Paket Tracking Informationen an PayPal zu senden, legen Sie fest **[!UICONTROL Send Package Tracking]** `Yes`.

   Informationen zu Package Tracking werden nur für PayPal Transaktionen/Bestellungen an PayPal gesendet. Sie müssen das Konfigurationsfeld in bestellen [!UICONTROL Send Cart Line Items for PayPal] aktivieren, damit die [!UICONTROL Package Tracking] Funktion ordnungsgemäß funktioniert.

1. Um einen Käufer oder Zahler durch PayPal über die Paketverfolgungsaktualisierungen zu informieren, setzen Sie **[!UICONTROL Use PayPal's "Notify Payer" functionality]** auf `Yes`.

## Schritt 12: Festlegen der Stileinstellungen

1. Wählen Sie **[!UICONTROL Location]**, wo PayPal-Schaltflächen und -Nachrichten gerendert werden sollen: `Mini-Cart and Cart Page`, `Checkout Page` oder `Product Page`

   ![PayPal-Stileinstellungen](../configuration-reference/sales/assets/payment-methods-braintree-paypal-styling.png){width="600" zoomable="yes"}

### [!UICONTROL Mini-Cart and Cart Page]

Die Optionen und Einstellungen in diesem Abschnitt variieren je nach Einstellung im _[!UICONTROL Location]_&#x200B;Feld.

1. **[!UICONTROL PayPal Button Type]** Festlegen auf eine von drei Arten von Schaltflächen: `PayPal Button` / `PayPal Pay Later Button` /`PayPal Credit Button`

**[!UICONTROL PayPal Button]**

Die Optionen und Einstellungen in diesem Abschnitt variieren je nach dem im _[!UICONTROL PayPal Button Type]_&#x200B;Feld ausgewählten Button Typ.

1. Um die PayPal Button im Schaufenster am ausgewählten Standort anzuzeigen, legen Sie **[!UICONTROL Show PayPal Button]** fest `Yes`.

1. Wählen Sie für **[!UICONTROL Button Label]** die PayPal Button Beschriftung aus: `Paypal`, `Checkout`, `Buynow`oder `Pay`

1. Wählen **[!UICONTROL Color]** Sie für die PayPal Button Farbe aus: `Blue`, `Black`, `Gold`oder `Silver`

1. Wählen Sie für **[!UICONTROL Shape]** die Form PayPal Button aus: `Pill` oder `Rectangle`

1. Wählen **[!UICONTROL Size (Deprecated)]** Sie für die PayPal Button Größe aus: `Medium`, `Large`, oder `Responsive`

>[!NOTE]
>
>Das **[!DNL Size(Deprecated)]** Konfigurationsfeld ist veraltet und wird nicht zum Gestalten der PayPal Schaltflächen verwendet.

Wenn diese Optionen festgelegt sind, können Sie den Vorschau der PayPal Schaltflächen sehen. Es gibt Steuerelemente, mit denen Sie die Einstellungen übernehmen oder die Werte zurücksetzen können:

- Klicken Sie auf **[!UICONTROL Apply]**, um die ausgewählten Stileinstellungen für Schaltflächen und PayLater-Messaging zu Geschäft und auf die aktuelle Position und den aktuellen Button-Typ anzuwenden.

- Um die ausgewählten Stileinstellungen für Schaltflächen und PayLater-Messaging-Werte zu speichern und sie auf alle Schaltflächentypen und Standorte anzuwenden, klicken Sie auf **[!UICONTROL Apply to All Buttons]**.

- Um die Stileinstellungen auf die empfohlenen Standardwerte für Schaltflächen und PayLater-Messaging zurückzusetzen und sie auf alle Schaltflächentypen und Standorte anzuwenden, klicken Sie auf **[!UICONTROL Reset to Recommended Defaults]**.

## Schritt 13: Später bezahlen

**[!UICONTROL Product Page]**

![Nachricht &quot;Später bezahlen&quot; – Produkteinstellungen Seite](../configuration-reference/sales/assets/payment-methods-braintree-paylater-messaging-product.png){width="600" zoomable="yes"}

1. Um Messaging im Schaufenster bei Produktseite anzuzeigen [!DNL Pay Later] , setzen Sie **[!UICONTROL Show PayLater Messaging]** auf `Yes`.

   Zeigt &quot;Später bezahlen&quot; Messaging für verfügbare Angebote an. Es gelten Einschränkungen. Weitere Informationen finden Sie [in der Dokumentation](https://developer.paypal.com/studio/checkout/pay-later/us) von PayPal.

1. Wählen Sie für **[!UICONTROL Message Layout]** das [!DNL Pay Later] Nachrichtenlayout aus: `Text` oder `Flex`

1. Wählen **[!UICONTROL Logo]** Sie für den PayPal Logotyp aus: `Inline`, `Primary`, `Alternative`oder `None`

1. Wählen **[!UICONTROL Logo Position]** Sie für die PayPal Logoposition aus: `Left`, `Right`, oder `Top`

1. **[!UICONTROL Text Color]** Wählen Sie für die Textfarbe der [!DNL PayLater] Nachricht aus: `Black`, `White`, `Monochrome`, oder`Grayscale`

**[!UICONTROL Cart]**

![Nachricht &quot;Später bezahlen&quot; - Einstellungen für Seite Warenkorb](../configuration-reference/sales/assets/payment-methods-braintree-paylater-messaging-cart.png){width="600" zoomable="yes"}

1. Um Messaging im Schaufenster in Mini-Warenkorb oder Warenkorb Seite anzuzeigen [!DNL Pay Later] , setzen Sie **[!UICONTROL Show PayLater Messaging]** auf `Yes`.

   Zeigt &quot;Später bezahlen&quot; Messaging für verfügbare Angebote an. Es gelten Einschränkungen. Weitere Informationen finden Sie [in der Dokumentation](https://developer.paypal.com/studio/checkout/pay-later/us) von PayPal.

1. Wählen Sie für **[!UICONTROL Message Layout]** das [!DNL Pay Later] Nachrichtenlayout aus: `Text` oder `Flex`

1. Wählen **[!UICONTROL Logo]** Sie für den PayPal Logotyp aus: `Inline`, `Primary`, `Alternative`oder `None`

1. Wählen **[!UICONTROL Logo Position]** Sie für die PayPal Logoposition aus: `Left`, `Right`, oder `Top`

1. **[!UICONTROL Text Color]** Wählen Sie für die Textfarbe der [!DNL PayLater] Nachricht aus: `Black`, `White`, `Monochrome`, oder`Grayscale`

**[!UICONTROL Checkout]**

![Nachricht &quot;Später bezahlen&quot; - Einstellungen für Seite Checkout](../configuration-reference/sales/assets/payment-methods-braintree-paylater-messaging-checkout.png){width="600" zoomable="yes"}

1. Um Messaging im Schaufenster bei Checkout anzuzeigen [!DNL Pay Later] , setzen Sie **[!UICONTROL Show PayLater Messaging]** auf `Yes`.

   Zeigt &quot;Später bezahlen&quot; Messaging für verfügbare Angebote an. Es gelten Einschränkungen. Weitere Informationen finden Sie [in der Dokumentation](https://developer.paypal.com/studio/checkout/pay-later/us) von PayPal.

1. Wählen **[!UICONTROL Text Align]** Sie für die Option Textausrichtung für [!DNL Pay Later] Nachricht aus: `Text` oder `Center` oder `Right`

1. Wählen **[!UICONTROL Text Color]** Sie für die Textfarbe der [!DNL Pay Later] Nachricht aus: `Black`, `White`

## Schritt 14: Alle Applikationen der 3D-Verifizierungseinstellungen

1. Wenn Sie einen Verifizierungsschritt für Kunden hinzufügen möchten, die Kreditkarten verwenden, die in einem Verifizierungs-Programm registriert sind (z. B. _Verifiziert von VISA),_ legen Sie **[!UICONTROL 3D Secure Verification]** `Yes`fest.

   Während des Prozesses wird der zur Verifizierung übermittelte Transaktionsbetrag mit dem Betrag abgeglichen, der für Autorisierung gesendet wird.

2. Um die 3D Secure-Anfrage für alle Transaktionen immer in Frage zu stellen, setzen Sie **[!UICONTROL Always request 3DS]** auf `Yes`.

3. Geben **[!UICONTROL Threshold Amount]** Sie für den Mindestbetrag bestellen ein, der erforderlich ist, um die 3D-Verifizierung auszulösen.

4. **[!UICONTROL Verify for Applicable Countries]** Festlegen auf eine der folgenden Optionen:

   - `All Allowed Countries` - Kunden aus allen [Ländern,](../getting-started/store-details.md#country-options) die in Ihrer Geschäft-Konfiguration angegeben sind, können diese Zahlungsmethode verwenden.
   - `Specific Countries` - Nachdem Sie diese Option ausgewählt haben, wird die _[!UICONTROL Verify for Specific Countries]_&#x200B;Liste angezeigt. Halten Sie die Strg-Taste (PC) oder die Befehl-Taste (Mac) gedrückt und wählen Sie jedes Land im Liste aus, in dem Kunden bei Ihrem Geschäft einkaufen können.

   ![3D-Verifizierungseinstellungen](../configuration-reference/sales/assets/payment-methods-braintree-3d-secure-verify-config.png){width="600" zoomable="yes"}

## Schritt 15: Dynamische Deskriptoren für Braintree einrichten

Die folgenden Deskriptoren werden verwendet, um Käufe auf Kunden-Kreditkartenauszügen zu identifizieren. Sie können die Anzahl der Rückbelastungen reduzieren, indem Sie das Unternehmen, das mit jedem Kauf verbunden ist, eindeutig identifizieren. Wenn dynamische Deskriptoren für Ihr Konto nicht aktiviert sind, wenden Sie sich an den Braintree-Support.

![Dynamische Deskriptoren](../configuration-reference/sales/assets/payment-methods-braintree-dynamic-config.png){width="600" zoomable="yes"}

1. Geben Sie den dynamischen Deskriptor für , **[!UICONTROL Name]**&#x200B;**[!UICONTROL Phone]**, und **[!UICONTROL URL]** gemäß folgenden Richtlinien ein:

   - **[!UICONTROL Name]** - Der Namensdeskriptor besteht aus zwei Teilen, die durch ein Sternchen (*) getrennt sind. Beispiel:

     `company*myproduct`

     Der erste Teil des Deskriptors identifiziert den Firma oder DBA, der zweite Teil identifiziert das Produkt. Die Länge des und Teile des `company` `product` Deskriptors können auf folgende Weise zugewiesen werden, für eine kombinierte Länge von bis zu 22 Zeichen.

     **_Zeichen in der Namensbeschreibung_**

     _Option 1:_ `Company` muss drei Zeichen lang sein, `Product` kann bis zu 18 Zeichen lang sein

     _Option 2:_ `Company` muss sieben Zeichen lang sein, `Product` kann bis zu 14 Zeichen lang sein

     _Option 3_: `Company` muss 12 Zeichen lang sein, `Product` kann bis zu neun Zeichen lang sein

   - **[!UICONTROL Phone]** - Der Telefondeskriptor muss 10 bis 14 Zeichen lang sein und darf nur Zahlen, Bindestriche, Klammern und Punkte enthalten. Beispiel:

     `9999999999`

     `(999) 999-9999`

     `999.999.9999`

   - **[!UICONTROL URL]** - Der URL-Deskriptor stellt Ihren Domain-Namen dar und kann bis zu 13 Zeichen lang sein. Beispiel:

     `company.com`

1. Wenn die Braintree Konfiguration abgeschlossen ist, klicken Sie auf **[!UICONTROL Save Config]**.

## 2.4 Aktualisierungshinweise

Ab Adobe Systems Commerce und Magento Open Source 2.4.0 ist die Braintree Erweiterung in der Version enthalten. Wenn Sie von einer Version vor 2.4.0, auf der die Marketplace Braintree-Erweiterung installiert ist, zu Commerce 2.4.x migrieren, müssen Sie diese Erweiterung (`paypal/module-braintree` oder `gene/module-braintree`) deinstallieren und alle Codeanpassungen aktualisieren, um die `PayPal_Braintree` Namespace anstelle von `Magento_Braintree`zu verwenden. Die Konfigurationseinstellungen der gebündelten Erweiterung &quot;Commerce Braintree Payments&quot; und der auf Commerce Marketplace verteilten Erweiterung bleiben bestehen, und Zahlungen, die mit diesen früheren Versionen getätigt wurden, können weiterhin wie gewohnt erfasst, storniert oder erstattet werden.

[1]: https://www.braintreepayments.com/
[2]: https://developers.braintreepayments.com/reference/general/testing/php
