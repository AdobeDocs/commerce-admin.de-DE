---
title: Braintree
description: Erfahren Sie, wie Sie Braintree als Online-Zahlungslösung in Ihrem Geschäft einrichten.
exl-id: 781b385f-926e-4047-b7da-6f7c090d75d8
feature: Payments
source-git-commit: dba610f53893a8698d2c52fe92fd0266f1cfa0cb
workflow-type: tm+mt
source-wordcount: '2380'
ht-degree: 0%

---

# Braintree

Braintree bietet eine vollständig anpassbare Checkout-Erfahrung mit der Betrugserkennung und PayPal-Integration. Es unterstützt [!DNL Apple Pay], [!DNL Google Pay], ACH, Venmo und lokale Zahlungsmethoden. Braintree reduziert die PCI-Compliance-Belastung für Händler, da die Transaktion auf dem Braintree-System stattfindet. Die Braintree Payments-Integration wird von [GENE Commerce](https://www.gene.co.uk/gene-braintree-payments/).

>[!NOTE]
>
>Wenn Sie von einer früheren Version von Adobe Commerce auf 2.4.x aktualisieren oder die Magento Open Source mit der installierten Braintree-Erweiterung von Commerce Marketplace auf 2.4.x aktualisieren, lesen Sie den Abschnitt [2.4 - Upgrade-Hinweise](#24-upgrade-notes) am Ende dieser Seite.

{{beta2-updates}}

## Schritt 1: Braintree-Anmeldedaten abrufen

Navigieren Sie zu [Braintree-Zahlungen][1] und melden Sie sich für ein Konto an.

## Schritt 2: Grundlegende Einstellungen durchführen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen **[!UICONTROL Payment Methods]**.

   - Wenn Ihre Commerce-Installation über mehrere Websites, Stores oder Ansichten verfügt, wählen Sie links oben die Option **[!UICONTROL Store View]** wo die Konfiguration gilt.

   - Im _[!UICONTROL Merchant Location]_überprüfen Sie, ob **[!UICONTROL Merchant Country]**auf den Speicherort Ihres Unternehmens festgelegt ist.

1. under _[!UICONTROL Recommended Solutions]_in der_[!UICONTROL Braintree Payments (by GENE Commerce v4.5.0)]_ Abschnitt, klicken Sie auf **[!UICONTROL Configure]**.

   ![Braintree konfigurieren](./assets/braintree-payments.png){width="600" zoomable="yes"}

1. Für **[!UICONTROL Title]** Geben Sie einen Titel ein, der Braintree beim Checkout als Zahlungsoption angibt.

1. Aktuelle Funktionsweise festlegen **[!UICONTROL Environment]** für Braintree-Transaktionen an `Sandbox` oder `Production`

   Verwenden Sie beim Testen der Konfiguration in einer Sandbox nur [Kreditkartennummern][2] die von Braintree empfohlen werden. Wenn Sie mit Braintree zur Produktion bereit sind, legen Sie **[!UICONTROL Environment]** nach `Production`.

   ![Grundlegende Anmeldeeinstellungen](./assets/braintree-settings1.png){width="600" zoomable="yes"}

1. Satz **[!UICONTROL Payment Action]** auf einen der folgenden Werte zu:

   - `Authorize Only` - Genehmigt den Kauf und hält die Mittel fest. Der Betrag wird erst dann vom Bankkonto des Kunden abgezogen, wenn der Verkauf stattfindet _erfasst_ vom Händler.|
   - `Intent Sale`  - Der Kaufbetrag wird genehmigt und sofort vom Konto des Kunden zurückgezogen. **_Hinweis:_** Dieser Wert  _Autorisieren und Erfassen_ in 2.3.x und früheren Versionen.|

1. Geben Sie die **[!UICONTROL Sandbox Merchant ID / Merchant ID]** von Ihrem Braintree-Konto aus.

1. Geben Sie die folgenden Anmeldedaten aus Ihrem Braintree-Konto ein:

   - **[!UICONTROL Sandbox Public Key / Public Key]**
   - **[!UICONTROL Sandbox Private Key / Private Key]**

   >[!NOTE]
   >
   >Es gibt separate Felder für beide **(Sandbox und Produktion)** Umgebungen und die anderen Felder werden basierend auf der ausgewählten Umgebung dargestellt.

1. Klicken Sie vor dem Speichern der Konfiguration auf **[!UICONTROL Validate Credentials]** , um Ihre Anmeldedaten zu überprüfen.

1. Satz **[!UICONTROL Enable Card Payments]** nach `Yes`.

   ![Grundlegende Einstellungen](./assets/braintree-settings2.png){width="600" zoomable="yes"}

   Wenn Sie möchten, dass Kundeninformationen sicher gespeichert werden können, sodass Kunden sie nicht jedes Mal erneut eingeben müssen, wenn sie einen Kauf tätigen, legen Sie **[!UICONTROL Enable Vault for Card Payments]** nach `Yes`.

## Schritt 3: Erweiterte Einstellungen durchführen

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Advanced Braintree Settings]** Abschnitt.

   ![Erweiterte Einstellungen](../configuration-reference/sales/assets/payment-methods-braintree-advanced-config.png){width="550" zoomable="yes"}

1. Für **[!UICONTROL Vault Title]** Geben Sie einen beschreibenden Titel für Ihre Referenz ein, der angibt, wo die Kundenkarteninformationen gespeichert sind.

1. Geben Sie die **[!UICONTROL Merchant Account ID]** von Ihrem Braintree-Konto aus.

   Wenn Sie das zu verwendende Händlerkonto nicht angeben, verarbeitet Braintree die Transaktion mit Ihrem standardmäßigen Händlerkonto.

1. Wenn Sie verhindern möchten, dass die Transaktion im Rahmen der Prüfungen der erweiterten Betrugswerkzeuge zur Evaluierung gesendet wird, legen Sie für über den Administrator aufgegebene Bestellungen Folgendes fest: **[!UICONTROL Skip Fraud Checks on Admin Orders]** nach `Yes`.

1. Legen Sie die **[!UICONTROL Bypass Fraud Protection Threshold]** damit die `Advanced Fraud Protection` -Prüfungen werden umgangen, wenn die Schwelle erreicht oder überschritten wird.

   Wenn Sie dieses Feld leer lassen, wird diese Option deaktiviert.

1. Wenn das System eine Protokolldatei mit Interaktionen zwischen Ihrem Speicher und Braintree speichern soll, legen Sie **[!UICONTROL Debug]** nach `Yes`.

1. Wenn Sie von Kunden verlangen möchten, dass sie den dreistelligen Sicherheitscode von der Rückseite einer Kreditkarte aus bereitstellen, legen Sie **[!UICONTROL CVV Verification]** nach `Yes`.

   Wenn Sie die CVV-Verifizierung verwenden, aktivieren Sie AVS und/oder CVV im _Einstellungen/Verarbeitung_ -Abschnitt Ihres Braintree-Kontos.

1. Um die Zeileneinträge aus dem Warenkorb für alle Zahlungsmethoden zu senden, legen Sie **[!UICONTROL Send Card Line Items]** nach `Yes`.

1. Für **[!UICONTROL Credit Card Types]**, wählen Sie jede Kreditkarte aus, die von Ihrem Geschäft als Bezahlung über Braintree akzeptiert wird.

   Um mehrere Kartentypen auszuwählen, halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie auf jede Option.

1. Für **[!UICONTROL Sort Order]**, geben Sie eine Zahl ein, um die Reihenfolge zu bestimmen, in der Braintree erscheint, wenn sie beim Checkout mit anderen Zahlungsmethoden aufgelistet wird.

## Schritt 4: Abschließen der Braintree-Webhook-Einstellungen

![Braintree Webhooks-Einstellungen](../configuration-reference/sales/assets/payment-methods-braintree-webhooks-config.png){width="600" zoomable="yes"}

1. Satz **[!UICONTROL Enable Webhook]** nach `Yes` , um die Webhook-Funktionalität für den Schutz von Betrug, ACH-Zahlungen und lokale Zahlungsmethoden zu aktivieren.

1. Kopieren Sie die URL in die **[!UICONTROL Fraud Protection URL]** und fügen Sie es Ihrem Braintree-Konto als _[!UICONTROL Webhook Destination URL]_.

   >[!IMPORTANT]
   >
   >Diese URL muss sicher und öffentlich zugänglich sein.

1. Legen Sie die **[!UICONTROL Fraud Protection Approve Order Status]** -Feld, um festzustellen, wann der Betrugsschutz von der Braintree genehmigt wird.

   Der ausgewählte Bestellstatus wird der Commerce-Bestellung zugewiesen.

1. Legen Sie die **[!UICONTROL Fraud Protection Reject Order Status]** -Feld, um festzustellen, wann der Betrugsschutz von der Braintree abgelehnt wird.

   Der ausgewählte Bestellstatus wird der Commerce-Bestellung zugewiesen.

## Schritt 5: Länderspezifische Einstellungen eingeben

1. Satz **[!UICONTROL Payment from Applicable Countries]** auf einen der folgenden Werte zu:

   - `All Allowed Countries` - Kunden von allen [Länder](../getting-started/store-details.md#country-options) Diese Zahlungsmethode kann in Ihrer Store-Konfiguration verwendet werden.
   - `Specific Countries` - Nach Auswahl dieser Option wird die _[!UICONTROL Payment from Specific Countries]_angezeigt. Halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und wählen Sie jedes Land in der Liste aus, in dem Kunden Käufe in Ihrem Geschäft tätigen können.

   ![Länderspezifische Einstellungen](../configuration-reference/sales/assets/payment-methods-braintree-country-specific-config.png){width="600" zoomable="yes"}

1. Einrichten von **[!UICONTROL Country Specific Credit Card Types]**:

   - Klicken **[!UICONTROL Add]**.

   - Legen Sie die **[!UICONTROL Country]** und wählen Sie **[!UICONTROL Allowed Credit Card Type]**.

   - Wiederholen Sie diese Schritte, um die Kreditkarten zu identifizieren, die von jedem Land akzeptiert werden.

## Schritt 6: Durchführen der ACH-Braintree-Einstellungen

![ACH bis Braintree](../configuration-reference/sales/assets/payment-methods-braintree-ach-config.png){width="600" zoomable="yes"}

1. Um ACH als Zahlungsoption mit Braintree einzubeziehen, legen Sie **[!UICONTROL Enable ACH Direct Debit]** nach `Yes`.

1. Für **[!UICONTROL Sort Order]** Geben Sie eine Zahl ein, um die Reihenfolge zu bestimmen, in der die Braintree ACH-Zahlungsoption erscheint, wenn sie beim Checkout mit anderen Zahlungsoptionen aufgeführt wird.

## Schritt 7: Vervollständigen Sie die [!UICONTROL Apple Pay] durch Braintree-Einstellungen

![ApplePay über Braintree-Einstellungen](../configuration-reference/sales/assets/payment-methods-braintree-applepay-config.png){width="600" zoomable="yes"}

1. Einbeziehen [!DNL Apple Pay] als Zahlungsoption mit Braintree festlegen **[!UICONTROL Enable ApplePay through Braintree]** nach `Yes`.

   Stellen Sie sicher, dass [den Domänennamen überprüfen](https://developer.paypal.com/braintree/docs/guides/apple-pay/configuration/javascript/v3) zuerst in Ihrem Braintree-Konto.

1. Satz **[!UICONTROL Payment Action]** auf einen der folgenden Werte zu:

   - `Authorize Only` - Genehmigt den Kauf und hält die Mittel fest. Der Betrag wird erst dann vom Bankkonto des Kunden abgezogen, wenn der Verkauf stattfindet _erfasst_ durch den Händler.
   - `Intent Sale` - Der Kaufbetrag wird genehmigt und sofort vom Konto des Kunden zurückgezogen.

1. Für **[!UICONTROL Merchant Name]** eingeben, geben Sie einen Text ein, der die Beschriftung angibt, die den Kunden im Dialogfeld &quot;Apple Pay&quot;angezeigt wird.

1. Für **[!UICONTROL Sort Order]**, geben Sie eine Zahl ein, um die Reihenfolge zu bestimmen, in der [!DNL Apple Pay] Die Zahlungsoption erscheint, wenn sie beim Checkout mit anderen Zahlungsoptionen aufgeführt wird.

## Schritt 8: Ausführen der Einstellungen für die lokalen Zahlungsmethoden

1. Um lokale Zahlungsmethoden als Zahlungsoption mit Braintree einzubeziehen, legen Sie **[!UICONTROL Enable Local Payment Methods]** nach `Yes`.

1. Für **[!UICONTROL Title]** Geben Sie den Text ein, der für die Beschriftung verwendet werden soll, die im Abschnitt Zahlungsmethode des Checkout angezeigt wird (Standardwert: `Local Payments`).

1. Für **[!UICONTROL Allowed Payment Methods]**, wählen Sie die lokale Zahlungsmethode aus, die aktiviert werden soll.

   Optionen: `Bancontact` / `EPS` / `giropay` / `iDeal` / `Klarna Pay Now` / `SOFORT` / `MyBank` / `P24` / `SEPA/ELV Direct Debit` (noch nicht unterstützt)

   ![Einstellungen für lokale Zahlungsmethoden](../configuration-reference/sales/assets/payment-methods-braintree-local-payment-config.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Die gebündelte Braintree-Erweiterung unterstützt nicht alle im Abschnitt [Braintree-Entwicklerdokumentation](https://developer.paypal.com/braintree/docs/guides/local-payment-methods/overview). Andere lokale Zahlungsmethoden werden derzeit entwickelt, um in zukünftigen Versionen unterstützt zu werden.

1. Für **[!UICONTROL Sort Order]** Geben Sie eine Zahl ein, um die Reihenfolge zu bestimmen, in der die lokale Zahlungsmethode angezeigt wird, wenn sie während des Checkout mit anderen Zahlungsoptionen aufgeführt wird.

## Schritt 9: Vervollständigen Sie die [!DNL Google Pay] durch Braintree-Einstellungen

![Google Pay-through-Braintree](../configuration-reference/sales/assets/payment-methods-braintree-googlepay-config.png){width="600" zoomable="yes"}

1. Einbeziehen [!DNL Google Pay] als Zahlungsoption mit Braintree festlegen **[!UICONTROL Enable GooglePay Through Braintree]** nach `Yes`.

1. Satz **[!UICONTROL Payment Action]** auf einen der folgenden Werte zu:

   - `Authorize Only` - Genehmigt den Kauf und hält die Mittel fest. Der Betrag wird erst dann vom Bankkonto des Kunden abgezogen, wenn der Verkauf stattfindet _erfasst_ durch den Händler.
   - `Intent Sale`  - Der Kaufbetrag wird genehmigt und sofort vom Konto des Kunden zurückgezogen.

1. Satz **[!UICONTROL Button Color]** zur Bestimmung der Farbe der [!DNL Google Pay] Schaltfläche: `White` oder `Black`

1. Für **[!UICONTROL Merchant ID]** Geben Sie Ihre MerchantID ein (von Google bereitgestellt).

1. Für **[!UICONTROL Accepted Cards]** auswählen, den Kartentyp auswählen, mit dem ein Kunde eine Bestellung aufgeben kann, indem er [!DNL Google Pay].

   Optionen: `Visa` / `MasterCard` / `AMEX` / `Discover` / `JCB`

1. Für **[!UICONTROL Sort Order]**, geben Sie eine Zahl ein, um die Reihenfolge zu bestimmen, in der [!DNL Google Pay] erscheint, wenn beim Checkout mit anderen Zahlungsoptionen aufgeführt wird.

## Schritt 10: Durchführen der Venmo-Braintree-Einstellungen

1. Um Venmo als Zahlungsoption mit Braintree einzubeziehen, legen Sie **[!UICONTROL Enable Venmo through Braintree]** nach `Yes`.

   ![Venmo durch Braintree](../configuration-reference/sales/assets/payment-methods-braintree-venmo-config.png){width="600" zoomable="yes"}

1. Satz **[!UICONTROL Payment Action]** auf einen der folgenden Werte zu:

   - `Authorize Only` - Genehmigt den Kauf und hält die Mittel fest. Der Betrag wird erst dann vom Bankkonto des Kunden abgezogen, wenn der Verkauf stattfindet _erfasst_ durch den Händler.
   - `Intent Sale`  - Der Kaufbetrag wird genehmigt und sofort vom Konto des Kunden zurückgezogen.

1. Für **[!UICONTROL Sort Order]** eingeben, geben Sie eine Zahl ein, um die Reihenfolge zu bestimmen, in der Venmo erscheint, wenn sie während des Checkout mit anderen Zahlungsoptionen aufgeführt wird.

## Schritt 11: Durchführen der PayPal-Braintree-Einstellungen

![PayPal über Braintree-Einstellungen](./assets/braintree-paypal.png){width="550" zoomable="yes"}

1. Um PayPal als Zahlungsoption mit Braintree einzubeziehen, legen Sie **[!UICONTROL Enable PayPal through Braintree]** nach `Yes`.

1. Geben Sie Ihre PayPal über die Braintree-Zahlungsmethode an:

   >[!NOTE]
   >
   >Entweder **[!DNL PayPal Credit]** oder **[!DNL PayPal PayLater]** aktiviert werden. Beide Methoden können nicht gleichzeitig aktiviert werden.

   - Einbeziehen [!DNL PayPal Credit] als Zahlungsoption mit Braintree festlegen **[!UICONTROL Enable PayPal Credit through Braintree]** nach `Yes`.

     Wann **PayPal über Braintree aktivieren** auf `Yes`, wird nur dieses Feld angezeigt.

     >[!NOTE]
     >
     >PayPal Credit ist nur in den Vereinigten Staaten und im Vereinigten Königreich erhältlich. PayPal-Guthaben ist deaktiviert, wenn der ausgewählte Wert für _[!UICONTROL Merchant Country]_Feld ist nicht `US` oder `UK`.

   - Einbeziehen [!DNL PayPal PayLater] als Zahlungsoption mit Braintree festlegen **[!UICONTROL Enable PayPal PayLater through Braintree]** nach `Yes`.

     Wann **[!UICONTROL Enable PayPal PayLater through Braintree]** auf `Yes`, wird nur dieses Feld angezeigt.

     Sie können PayLater-Nachrichten für Angebote wie _Bezahlen in 3_, wodurch Kunden mit drei zinsfreien monatlichen Zahlungen zahlen können. Die Braintree-Integration kann Meldungen auf Ihrer Site anzeigen, um diese Funktion zu bewerben. Sie können PayLater-Angebote nicht mit anderen Inhalten, Marketingaktivitäten oder Materialien bewerben.

1. Für **[!UICONTROL Title]**, geben Sie einen Titel ein, der die Braintree-Zahlung nach PayPal-Option beim Checkout angibt.

1. Satz **[!UICONTROL Vault Title]** nach `Yes` , um die Verwendung eines sicheren Gewebes zur Speicherung der Kreditkarteninformationen von Kunden zu ermöglichen.

1. Für **[!UICONTROL Sort Order]**, geben Sie eine Zahl ein, um die Reihenfolge zu bestimmen, in der die Zahlungsoption Braintree PayPal erscheint, wenn sie beim Checkout mit anderen Zahlungsoptionen aufgeführt wird.

1. So zeigen Sie Ihren Händlernamen anders an als in Ihrem [Store-Konfiguration](../getting-started/store-details.md#store-information), geben Sie den Namen in die **[!UICONTROL Override Merchant Name]** -Feld, wie es angezeigt werden soll.

1. Satz **[!UICONTROL Payment Action]** auf einen der folgenden Werte zu:

   - `Authorize Only` - Genehmigt den Kauf und hält die Mittel fest. Der Betrag wird erst dann vom Bankkonto des Kunden abgezogen, wenn der Verkauf stattfindet _erfasst_ durch den Händler.
   - `Authorize and Capture` - Der Kaufbetrag wird genehmigt und sofort vom Konto des Kunden zurückgezogen.

1. Satz **[!UICONTROL Payment from Applicable Countries]** auf einen der folgenden Werte für Braintree-Transaktionen, die von PayPal verarbeitet werden:

   - `All Allowed Countries` - Kunden von allen [Länder](../getting-started/store-details.md#country-options) Diese Zahlungsmethode kann in Ihrer Store-Konfiguration verwendet werden.
   - `Specific Countries` - Nach Auswahl dieser Option wird die _[!UICONTROL Payment from Specific Countries]_angezeigt. Halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und wählen Sie jedes Land in der Liste aus, in dem Kunden Käufe in Ihrem Geschäft tätigen können.

1. Wenn Sie von Kunden verlangen möchten, eine Rechnungsadresse anzugeben, legen Sie **[!UICONTROL Require Customer's Billing Address]** nach `Yes`.

   >[!NOTE]
   >
   >Diese Funktion muss vom technischen Support von PayPal für Ihr Konto aktiviert werden.

1. Um eine Protokolldatei mit Interaktionen zwischen Ihrem Store und PayPal über Braintree zu speichern, legen Sie **[!UICONTROL Debug]** nach `Yes`.

1. Um die Schaltfläche PayPal sowohl auf der Mini-Warenkorb- als auch auf der Warenkorbseite anzuzeigen, legen Sie **[!UICONTROL Display on Shopping Cart]** nach `Yes`.

## Schritt 12: Stileinstellungen festlegen

1. Für **[!UICONTROL Location]** auswählen, wo PayPal-Schaltflächen und -Nachrichten gerendert werden: `Mini-Cart and Cart Page`, `Checkout Page`oder `Product Page`

   ![PayPal-Stileinstellungen](../configuration-reference/sales/assets/payment-methods-braintree-paypal-styling.png){width="600" zoomable="yes"}

### [!UICONTROL Mini-Cart and Cart Page]

Die Optionen und Einstellungen in diesem Abschnitt variieren je nach Einstellung im _[!UICONTROL Location]_-Feld.

1. Satz **[!UICONTROL PayPal Button Type]** auf einen von drei Schaltflächentypen: `PayPal Button` / `PayPal Pay Later Button` / `PayPal Credit Button`

**[!UICONTROL PayPal Button]**

Die Optionen und Einstellungen in diesem Abschnitt variieren je nach dem im _[!UICONTROL PayPal Button Type]_-Feld.

1. Um die Schaltfläche PayPal auf der Storefront an der ausgewählten Position anzuzeigen, legen Sie **[!UICONTROL Show PayPal Button]** nach `Yes`.

1. Für **[!UICONTROL Button Label]** Wählen Sie die Schaltflächenbeschriftung PayPal aus: `Paypal`, `Checkout`, `Buynow`oder `Pay`

1. Für **[!UICONTROL Color]** wählen Sie die Schaltflächenfarbe PayPal aus: `Blue`, `Black`, `Gold`oder `Silver`

1. Für **[!UICONTROL Shape]** wählen Sie die Form der PayPal-Schaltfläche aus: `Pill` oder `Rectangle`

1. Für **[!UICONTROL Size]** wählen Sie die Schaltflächengröße PayPal aus: `Medium`, `Large`oder `Responsive`

**[!UICONTROL PayLater Messaging]**

1. Zum Anzeigen [!DNL PayLater] Messaging auf der Storefront am ausgewählten Speicherort, **[!UICONTROL Show PayLater Messaging]** nach `Yes`.

   Diese Nachricht beinhaltet die Anzeige von [!DNL PayLater] Messaging für verfügbare Angebote ([Einschränkungen gelten](https://developer.paypal.com/docs/checkout/pay-later/us/)).

1. Für **[!UICONTROL Message Layout]**, wählen Sie die [!DNL PayLater] Nachrichtenlayout: `Text` oder `Flex`

1. Für **[!UICONTROL Logo]** Wählen Sie den PayPal-Logotyp aus: `Inline`, `Primary`, `Alternative`oder `None`

1. Für **[!UICONTROL Logo Position]** wählen Sie die Position des PayPal-Logos aus: `Left`, `Right`oder `Top`

1. Für **[!UICONTROL Text Color]**, wählen Sie die [!DNL PayLater] Textfarbe der Nachricht: `Black`, `White`, `Monochrome`oder `Grayscale`

Wenn diese Optionen festgelegt sind, können Sie die Vorschau der PayPal-Schaltflächen und PayLater-Nachrichten sehen. Es gibt Steuerelemente, mit denen Sie die Einstellungen anwenden oder die Werte zurücksetzen können:

- Um die ausgewählten Stileinstellungen für Schaltflächen und PayLater-Nachrichten zu speichern und sie auf die aktuelle Position und den aktuellen Schaltflächentyp anzuwenden, klicken Sie auf **[!UICONTROL Apply]**.

- Um die ausgewählten Stileinstellungen für Schaltflächen und PayLater-Nachrichtenwerte zu speichern und sie auf alle Schaltflächentypen und -speicherorte anzuwenden, klicken Sie auf **[!UICONTROL Apply to All Buttons]**.

- Um die Stileinstellungen auf die empfohlenen Standardwerte für Schaltflächen und PayLater-Nachrichten zurückzusetzen und sie auf alle Schaltflächentypen und -speicherorte anzuwenden, klicken Sie auf **[!UICONTROL Reset to Recommended Defaults]**.

## Schritt 13: 3D-Verifizierungseinstellungen durchführen

1. Wenn Sie einen Überprüfungsschritt für Kunden hinzufügen möchten, die Kreditkarten verwenden, die in einem Überprüfungsprogramm registriert sind (z. B. _Verifiziert durch VISA_), set **[!UICONTROL 3D Secure Verification]** nach `Yes`.

   Während des Prozesses wird der Transaktionsbetrag, der zur Überprüfung vorgelegt wird, mit dem Betrag verglichen, der zur Genehmigung gesendet wird.

2. Um die 3D Secure-Anforderung für alle Transaktionen immer anzufechten, legen Sie **[!UICONTROL Always request 3DS]** nach `Yes`.

3. Für **[!UICONTROL Threshold Amount]** Geben Sie den Mindestbestellbetrag ein, der für die Trigger-3D-Verifizierung erforderlich ist.

4. Satz **[!UICONTROL Verify for Applicable Countries]** auf einen der folgenden Werte zu:

   - `All Allowed Countries` - Kunden von allen [Länder](../getting-started/store-details.md#country-options) Diese Zahlungsmethode kann in Ihrer Store-Konfiguration verwendet werden.
   - `Specific Countries` - Nach Auswahl dieser Option wird die _[!UICONTROL Verify for Specific Countries]_angezeigt. Halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und wählen Sie jedes Land in der Liste aus, in dem Kunden Käufe in Ihrem Geschäft tätigen können.

   ![Einstellungen zur 3D-Überprüfung](../configuration-reference/sales/assets/payment-methods-braintree-3d-secure-verify-config.png){width="600" zoomable="yes"}

## Schritt 14: Einrichten der dynamischen Braintree-Deskriptoren

Die folgenden Deskriptoren werden verwendet, um Käufe in Kreditkartenabschlüssen von Kunden zu identifizieren. Sie können die Anzahl der Gebühren reduzieren, indem Sie das Unternehmen, das mit jedem Kauf verbunden ist, eindeutig identifizieren. Wenn dynamische Deskriptoren für Ihr Konto nicht aktiviert sind, wenden Sie sich an den Braintree-Support.

![Dynamische Deskriptoren](../configuration-reference/sales/assets/payment-methods-braintree-dynamic-config.png){width="600" zoomable="yes"}

1. Geben Sie den dynamischen Deskriptor für die **[!UICONTROL Name]**, **[!UICONTROL Phone]**, und **[!UICONTROL URL]** gemäß diesen Leitlinien:

   - **[!UICONTROL Name]** - Es gibt zwei Teile des Namensdeskriptors, die durch ein Sternchen (*) getrennt sind. Beispiel:

     `company*myproduct`

     Der erste Teil des Deskriptors identifiziert das Unternehmen oder DBA und der zweite Teil das Produkt. Die Länge der `company` und `product` Teile des Deskriptors können auf folgende Weise für eine kombinierte Länge von bis zu 22 Zeichen zugeordnet werden.

     **_Zeichen im Namensdeskriptor_**

     _Option 1:_ `Company` muss aus drei Zeichen bestehen; `Product` kann bis zu 18 Zeichen lang sein

     _Option 2:_ `Company` muss sieben Zeichen lang sein; `Product` kann bis zu 14 Zeichen lang sein

     _Option 3_: `Company` darf 12 Zeichen lang sein; `Product` kann bis zu neun Zeichen lang sein

   - **[!UICONTROL Phone]** - Der Telefondeskriptor muss 10 bis 14 Zeichen lang sein und darf nur Zahlen, Bindestriche, Klammern und Punkte enthalten. Beispiel:

     `9999999999`

     `(999) 999-9999`

     `999.999.9999`

   - **[!UICONTROL URL]** - Der URL-Deskriptor stellt Ihren Domänennamen dar und kann bis zu 13 Zeichen lang sein. Beispiel:

     `company.com`

1. Wenn die Braintree-Konfiguration abgeschlossen ist, klicken Sie auf **[!UICONTROL Save Config]**.

## 2.4 - Upgrade-Hinweise

Bevor Sie von 2.3 auf Commerce 2.4 aktualisieren, sollten Händler die Commerce-Braintree-Kernintegration durch die offizielle Braintree-Erweiterung von ersetzen [Commerce Marketplace](https://commercemarketplace.adobe.com/catalogsearch/result/?q=braintree). Ab Adobe Commerce und Magento Open Source 2.4.0 ist die Braintree-Erweiterung in der -Version enthalten.

Wenn Sie von einer Version vor 2.4.0, in der die Marketplace-Braintree-Erweiterung installiert ist, auf Commerce 2.4.x migrieren, müssen Sie diese Erweiterung deinstallieren (`paypal/module-braintree` oder `gene/module-braintree`) und aktualisieren Sie alle Code-Anpassungen, um die `PayPal_Braintree` Namespace anstelle von `Magento_Braintree`. Konfigurationseinstellungen aus der Core-Commerce-Braintree-Payments-Bundle-Erweiterung und der auf Commerce Marketplace verteilten Erweiterung bleiben erhalten und Zahlungen, die mit diesen früheren Versionen platziert wurden, können weiterhin normal erfasst, ungültig gemacht oder rückerstattet werden.

[1]: https://www.braintreepayments.com/
[2]: https://developers.braintreepayments.com/reference/general/testing/php
