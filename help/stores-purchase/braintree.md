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

Braintree bietet eine vollständig anpassbare Checkout-Erfahrung mit der Betrugserkennung und PayPal-Integration. Es unterstützt die Zahlungsmethoden [!DNL Apple Pay], [!DNL Google Pay], ACH, Venmo und lokal. Braintree reduziert die PCI-Compliance-Belastung für Händler, da die Transaktion auf dem Braintree-System stattfindet. Die Braintree Payments-Integration wird von [GENE Commerce](https://www.gene.co.uk/gene-braintree-payments/) entwickelt.

>[!NOTE]
>
>Wenn Sie von einer früheren Version von Adobe Commerce auf 2.4.x aktualisieren oder die Magento Open Source mit der installierten Braintree-Erweiterung von Commerce Marketplace auf 2.4.x aktualisieren, lesen Sie die [2.4 Upgrade-Hinweise](#24-upgrade-notes) am Ende dieser Seite.


## Schritt 1: Braintree-Anmeldedaten abrufen

Wechseln Sie zu [Braintree-Zahlungen][1] und melden Sie sich für ein Konto an.

## Schritt 2: Grundlegende Einstellungen durchführen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Payment Methods]** aus.

   - Wenn Ihre Commerce-Installation über mehrere Websites, Stores oder Ansichten verfügt, wählen Sie oben links die **[!UICONTROL Store View]** aus, für die die Konfiguration gilt.

   - Überprüfen Sie im Abschnitt _[!UICONTROL Merchant Location]_, ob **[!UICONTROL Merchant Country]**auf den Speicherort Ihres Unternehmens festgelegt ist.

1. Klicken Sie unter _[!UICONTROL Recommended Solutions]_im Abschnitt_[!UICONTROL Braintree Payments] (durch den Abschnitt [GENE Commerce](https://www.gene.co.uk/gene-braintree-payments/) v4.6.1 - [Versionshinweise](https://support.gene.co.uk/support/solutions/articles/35000228529)_) auf **[!UICONTROL Configure]**.

   ![Braintree konfigurieren](./assets/braintree-payments.png){width="600" zoomable="yes"}

1. Geben Sie für **[!UICONTROL Title]** einen Titel ein, der Braintree als Zahlungsoption beim Checkout angibt.

1. Setzen Sie die aktuelle operative **[!UICONTROL Environment]** für Braintree-Transaktionen auf `Sandbox` oder `Production`

   Verwenden Sie beim Testen der Konfiguration in einer Sandbox nur die von Braintree empfohlenen [Kreditkartennummern][2]. Wenn Sie bereit sind, mit Braintree zur Produktion zu gehen, setzen Sie **[!UICONTROL Environment]** auf `Production`.

   ![Grundlegende Einstellungen für Anmeldedaten](./assets/braintree-settings1.png){width="600" zoomable="yes"}

1. Setzen Sie **[!UICONTROL Payment Action]** auf einen der folgenden Werte:

   - `Authorize Only` - Genehmigt den Kauf und legt einen Besitz an den Fonds fest. Der Betrag wird nicht vom Bankkonto des Kunden abgezogen, bis der Verkauf vom Händler _erfasst_ wurde.|
   - `Intent Sale` - Der Betrag des Kaufs wird genehmigt und sofort vom Konto des Kunden zurückgezogen. **_Hinweis:_** Dieser Wert war _Autorisieren und Erfassen_ in 2.3.x und früheren Versionen.|

1. Geben Sie die **[!UICONTROL Sandbox Merchant ID / Merchant ID]** aus Ihrem Braintree-Konto ein.

1. Geben Sie die folgenden Anmeldedaten aus Ihrem Braintree-Konto ein:

   - **[!UICONTROL Sandbox Public Key / Public Key]**
   - **[!UICONTROL Sandbox Private Key / Private Key]**

   >[!NOTE]
   >
   >Es gibt separate Felder für die Umgebungen **(Sandbox und Produktion)** und die anderen Felder werden basierend auf der ausgewählten Umgebung gerendert.

1. Klicken Sie vor dem Speichern der Konfiguration auf **[!UICONTROL Validate Credentials]** , um Ihre Anmeldedaten zu überprüfen.

1. Setzen Sie **[!UICONTROL Enable Card Payments]** auf `Yes`.

   ![Grundlegende Einstellungen](./assets/braintree-settings2.png){width="600" zoomable="yes"}

   Wenn Sie möchten, dass Kundeninformationen sicher gespeichert werden können, sodass Kunden sie nicht jedes Mal erneut eingeben müssen, wenn sie einen Kauf tätigen, setzen Sie **[!UICONTROL Enable Vault for Card Payments]** auf `Yes`.

## Schritt 3: Erweiterte Einstellungen durchführen

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Advanced Braintree Settings]** .

   ![Erweiterte Einstellungen](../configuration-reference/sales/assets/payment-methods-braintree-advanced-config.png){width="550" zoomable="yes"}

1. Geben Sie für &quot;**[!UICONTROL Vault Title]**&quot;einen beschreibenden Titel für Ihre Referenz ein, der den Vault angibt, in dem die Kundenkarteninformationen gespeichert sind.

1. Geben Sie die **[!UICONTROL Merchant Account ID]** aus Ihrem Braintree-Konto ein.

   Wenn Sie das zu verwendende Händlerkonto nicht angeben, verarbeitet Braintree die Transaktion mit Ihrem standardmäßigen Händlerkonto.

1. Setzen Sie **[!UICONTROL Enable Checkout Express Payments]** auf `Yes`, um zu Beginn des Checkout-Prozesses ein schnelleres Checkout-Erlebnis mit Express-Zahlungsoptionen zu bieten, einschließlich PayPal, PayLater, Apple Pay und Google Pay.

1. Wenn Sie verhindern möchten, dass die Transaktion im Rahmen der Prüfungen der erweiterten Betrugswerkzeuge zur Auswertung gesendet wird, setzen Sie bei Bestellungen, die über den Admin aufgegeben werden, **[!UICONTROL Skip Fraud Checks on Admin Orders]** auf `Yes`.

1. Setzen Sie die **[!UICONTROL Bypass Fraud Protection Threshold]** so, dass die `Advanced Fraud Protection`-Prüfungen umgangen werden, wenn der Schwellenwert erreicht oder überschritten wird.

   Wenn Sie dieses Feld leer lassen, wird diese Option deaktiviert.

1. Wenn Sie möchten, dass das System eine Protokolldatei mit Interaktionen zwischen Ihrem Speicher und Braintree speichert, setzen Sie **[!UICONTROL Debug]** auf `Yes`.

1. Damit Kunden den dreistelligen Sicherheitscode von der Rückseite einer Kreditkarte aus bereitstellen können, setzen Sie **[!UICONTROL CVV Verification]** auf `Yes`.

   Stellen Sie bei Verwendung der CVV-Verifizierung sicher, dass Sie AVS und/oder CVV im Abschnitt _Einstellungen/Verarbeitung_ Ihres Braintree-Kontos aktivieren.

1. Um die Zeileneinträge aus dem Warenkorb für alle Zahlungsmethoden zu senden, setzen Sie **[!UICONTROL Send Card Line Items]** auf `Yes`.

1. Wählen Sie für **[!UICONTROL Credit Card Types]** jede Kreditkarte aus, die von Ihrem Geschäft als Zahlung über Braintree akzeptiert wird.

   Um mehrere Kartentypen auszuwählen, halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie auf jede Option.

1. Geben Sie für **[!UICONTROL Sort Order]** eine Zahl ein, um die Reihenfolge zu bestimmen, in der Braintree angezeigt wird, wenn sie beim Checkout mit anderen Zahlungsmethoden aufgeführt wird.

## Schritt 4: Abschließen der Braintree-Webhook-Einstellungen

![Braintree Webhooks-Einstellungen](../configuration-reference/sales/assets/payment-methods-braintree-webhooks-config.png){width="600" zoomable="yes"}

1. Setzen Sie **[!UICONTROL Enable Webhook]** auf `Yes` , um die Webhook-Funktionalität für den Schutz von Betrug, ACH-Zahlungen und lokale Zahlungsmethoden zu aktivieren.

1. Kopieren Sie die URL im Feld **[!UICONTROL Fraud Protection URL]** und fügen Sie sie Ihrem Braintree-Konto als _[!UICONTROL Webhook Destination URL]_hinzu.

   >[!IMPORTANT]
   >
   >Diese URL muss sicher und öffentlich zugänglich sein.

1. Legen Sie das Feld **[!UICONTROL Fraud Protection Approve Order Status]** fest, um zu bestimmen, wann der Betrugsschutz von Braintree genehmigt wird.

   Der ausgewählte Bestellstatus wird der Commerce-Bestellung zugewiesen.

1. Legen Sie das Feld **[!UICONTROL Fraud Protection Reject Order Status]** fest, um festzustellen, wann der Betrugsschutz von Braintree abgelehnt wird.

   Der ausgewählte Bestellstatus wird der Commerce-Bestellung zugewiesen.

## Schritt 5: Länderspezifische Einstellungen eingeben

1. Setzen Sie **[!UICONTROL Payment from Applicable Countries]** auf einen der folgenden Werte:

   - `All Allowed Countries` - Kunden aus allen in Ihrer Store-Konfiguration angegebenen [Ländern](../getting-started/store-details.md#country-options) können diese Zahlungsmethode verwenden.
   - `Specific Countries` - Nach Auswahl dieser Option wird die Liste _[!UICONTROL Payment from Specific Countries]_angezeigt. Halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und wählen Sie jedes Land in der Liste aus, in dem Kunden Käufe in Ihrem Geschäft tätigen können.

   ![Länderspezifische Einstellungen](../configuration-reference/sales/assets/payment-methods-braintree-country-specific-config.png){width="600" zoomable="yes"}

1. So richten Sie **[!UICONTROL Country Specific Credit Card Types]** ein:

   - Klicken Sie auf **[!UICONTROL Add]**.

   - Legen Sie die **[!UICONTROL Country]** fest und wählen Sie jeden **[!UICONTROL Allowed Credit Card Type]** aus.

   - Wiederholen Sie diese Schritte, um die Kreditkarten zu identifizieren, die von jedem Land akzeptiert werden.

## Schritt 6: Durchführen der ACH-Braintree-Einstellungen

![ACH DURCH Braintree](../configuration-reference/sales/assets/payment-methods-braintree-ach-config.png){width="600" zoomable="yes"}

1. Um ACH als Zahlungsoption mit Braintree einzubeziehen, setzen Sie **[!UICONTROL Enable ACH Direct Debit]** auf `Yes`.

1. Kunden können ihre einmalige Zahlungsmethode mit ACH Direct Debit nutzen und sie für die zukünftige Verwendung speichern. Nach der Überprüfung können Kunden ACH Direct Debit wiederverwenden, ohne ihre Zahlungsinformationen erneut eingeben oder authentifizieren zu müssen, wenn **[!UICONTROL Enable Vault for ACH Direct Debit]** auf `Yes` gesetzt wird.

1. Geben Sie für **[!UICONTROL Sort Order]** eine Zahl ein, um die Reihenfolge zu bestimmen, in der die Braintree ACH-Zahlungsoption erscheint, wenn sie beim Checkout mit anderen Zahlungsoptionen aufgeführt wird.

## Schritt 7: Durchführen der [!UICONTROL Apple Pay] durch Braintree-Einstellungen

![ApplePay durch Braintree-Einstellungen](../configuration-reference/sales/assets/payment-methods-braintree-applepay-config.png){width="600" zoomable="yes"}

1. Um [!DNL Apple Pay] als Zahlungsoption mit Braintree einzubeziehen, setzen Sie **[!UICONTROL Enable ApplePay through Braintree]** auf `Yes`.

   Überprüfen Sie zunächst den Domänennamen [ in Ihrem Braintree-Konto.](https://developer.paypal.com/braintree/docs/guides/apple-pay/configuration/javascript/v3)

1. Wenn Sie möchten, dass Kundeninformationen sicher gespeichert werden können, sodass Kunden sie nicht jedes Mal erneut eingeben müssen, wenn sie mit Apple Pay einkaufen, setzen Sie **[!UICONTROL Enable Vault for ApplePay]** auf `Yes`.

1. Setzen Sie **[!UICONTROL Payment Action]** auf einen der folgenden Werte:

   - `Authorize Only` - Genehmigt den Kauf und legt einen Besitz an den Fonds fest. Der Betrag wird erst dann vom Bankkonto des Kunden abgezogen, wenn der Verkauf vom Händler _erfasst_ wurde.
   - `Intent Sale` - Der Betrag des Kaufs wird genehmigt und sofort vom Konto des Kunden zurückgezogen.

1. Geben Sie für &quot;**[!UICONTROL Merchant Name]**&quot;Text ein, der die Beschriftung angibt, die Kunden im Dialogfeld &quot;Apple Pay&quot;angezeigt wird.

1. Geben Sie für **[!UICONTROL Sort Order]** eine Zahl ein, um die Reihenfolge zu bestimmen, in der die Zahlungsoption [!DNL Apple Pay] angezeigt wird, wenn sie beim Checkout mit anderen Zahlungsoptionen aufgeführt wird.

## Schritt 8: Ausführen der Einstellungen für die lokalen Zahlungsmethoden

1. Um lokale Zahlungsmethoden als Zahlungsoption mit Braintree einzubeziehen, setzen Sie **[!UICONTROL Enable Local Payment Methods]** auf `Yes`.

1. Geben Sie für &quot;**[!UICONTROL Title]**&quot;den Text ein, der für die Beschriftung verwendet werden soll, die im Abschnitt &quot;Zahlungsmethode des Checkout&quot;angezeigt wird (Standardwert: `Local Payments`).

1. Geben Sie für **[!UICONTROL Fallback Button Text]** den Text ein, der für die Schaltfläche verwendet werden soll, die auf der Fallback-Braintree-Seite angezeigt wird, um den Kunden zurück zur Website zu bringen (z. B. `Complete Checkout`).

1. Geben Sie für &quot;**[!UICONTROL Redirect on Fail]**&quot;die URL ein, an die Kunden weitergeleitet werden sollen, wenn lokale Zahlungsmethoden-Transaktionen abgebrochen werden, fehlschlagen oder Fehler auftreten. Dies sollte die Zahlungsseite für den Checkout sein (z. B. `https://www.domain.com/checkout#payment`).

1. Wählen Sie für **[!UICONTROL Allowed Payment Methods]** die lokale Zahlungsmethode aus, die aktiviert werden soll.

   Optionen: `Bancontact` / `EPS` / `giropay` / `iDeal` / `Klarna Pay Now` / `SOFORT` / `MyBank` / `P24` / `SEPA/ELV Direct Debit` (noch nicht unterstützt)

   ![Einstellungen für lokale Zahlungsmethoden](../configuration-reference/sales/assets/payment-methods-braintree-local-payment-config.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Die gebündelte Braintree-Erweiterung unterstützt nicht alle in der [Braintree-Entwicklerdokumentation](https://developer.paypal.com/braintree/docs/guides/local-payment-methods/overview) aufgelisteten lokalen Zahlungsmethoden. Andere lokale Zahlungsmethoden werden derzeit entwickelt, um in zukünftigen Versionen unterstützt zu werden.

1. Geben Sie für **[!UICONTROL Sort Order]** eine Zahl ein, um die Reihenfolge zu bestimmen, in der die lokale Zahlungsmethode angezeigt wird, wenn sie beim Checkout mit anderen Zahlungsoptionen aufgeführt wird.

## Schritt 9: Durchführen der [!DNL Google Pay] durch Braintree-Einstellungen

![Google-Pay durch Braintree](../configuration-reference/sales/assets/payment-methods-braintree-googlepay-config.png){width="600" zoomable="yes"}

1. Um [!DNL Google Pay] als Zahlungsoption mit Braintree einzubeziehen, setzen Sie **[!UICONTROL Enable GooglePay Through Braintree]** auf `Yes`.

1. Wenn Sie möchten, dass Kundeninformationen sicher gespeichert werden können, sodass Kunden sie nicht jedes Mal erneut eingeben müssen, wenn sie mit Google Pay einkaufen, setzen Sie **[!UICONTROL Enable Vault for GooglePay]** auf `Yes`.

1. Setzen Sie **[!UICONTROL Payment Action]** auf einen der folgenden Werte:

   - `Authorize Only` - Genehmigt den Kauf und legt einen Besitz an den Fonds fest. Der Betrag wird erst dann vom Bankkonto des Kunden abgezogen, wenn der Verkauf vom Händler _erfasst_ wurde.
   - `Intent Sale` - Der Betrag des Kaufs wird genehmigt und sofort vom Konto des Kunden zurückgezogen.

1. Legen Sie **[!UICONTROL Button Color]** fest, um die Farbe der Schaltfläche [!DNL Google Pay] zu bestimmen: `White` oder `Black`

1. Geben Sie für **[!UICONTROL Merchant ID]** Ihre MerchantID ein (von Google bereitgestellt).

1. Wählen Sie für &quot;**[!UICONTROL Accepted Cards]**&quot;den Kartentyp aus, den ein Kunde verwenden kann, um eine Bestellung mit &quot;[!DNL Google Pay]&quot;aufzugeben.

   Optionen: `Visa` / `MasterCard` / `AMEX` / `Discover` / `JCB`

1. Geben Sie für **[!UICONTROL Sort Order]** eine Zahl ein, um die Sequenz zu bestimmen, in der [!DNL Google Pay] angezeigt wird, wenn während des Checkout andere Zahlungsoptionen aufgeführt werden.

## Schritt 10: Durchführen der Venmo-Braintree-Einstellungen

1. Um Venmo als Zahlungsoption mit Braintree einzubeziehen, setzen Sie **[!UICONTROL Enable Venmo through Braintree]** auf `Yes`.

1. Setzen Sie **[!UICONTROL Enable Vault for Venmo]** auf `Yes` , um die Verwendung eines sicheren Vault zum Speichern des Venmo-Kontos von Kunden zu aktivieren, damit sich Kunden nicht für künftige Transaktionen erneut bei ihrem Venmo-Konto anmelden müssen.

   ![Venmo durch Braintree](../configuration-reference/sales/assets/payment-methods-braintree-venmo-config.png){width="600" zoomable="yes"}

1. Setzen Sie **[!UICONTROL Payment Action]** auf einen der folgenden Werte:

   - `Authorize Only` - Genehmigt den Kauf und legt einen Besitz an den Fonds fest. Der Betrag wird erst dann vom Bankkonto des Kunden abgezogen, wenn der Verkauf vom Händler _erfasst_ wurde.
   - `Intent Sale` - Der Betrag des Kaufs wird genehmigt und sofort vom Konto des Kunden zurückgezogen.

1. Geben Sie für **[!UICONTROL Sort Order]** eine Zahl ein, um die Sequenz zu bestimmen, in der Venmo angezeigt wird, wenn sie beim Checkout mit anderen Zahlungsoptionen aufgeführt wird.

## Schritt 11: Durchführen der PayPal-Braintree-Einstellungen

![PayPal durch Braintree-Einstellungen](./assets/braintree-paypal.png){width="550" zoomable="yes"}

1. Um PayPal als Zahlungsoption mit Braintree einzubeziehen, setzen Sie **[!UICONTROL Enable PayPal through Braintree]** auf `Yes`.

1. Geben Sie Ihre PayPal über die Braintree-Zahlungsmethode an:

   >[!NOTE]
   >
   >Es kann entweder **[!DNL PayPal Credit]** oder **[!DNL PayPal PayLater]** aktiviert werden. Beide Methoden können nicht gleichzeitig aktiviert werden.

   - Um [!DNL PayPal Credit] als Zahlungsoption mit Braintree einzubeziehen, setzen Sie **[!UICONTROL Enable PayPal Credit through Braintree]** auf `Yes`.

     Wenn **PayPal durch Braintree aktivieren** auf `Yes` gesetzt ist, wird nur dieses Feld angezeigt.

     >[!NOTE]
     >
     >PayPal Credit ist nur in den Vereinigten Staaten und im Vereinigten Königreich erhältlich. PayPal-Guthaben ist deaktiviert, wenn der ausgewählte Wert für das Feld _[!UICONTROL Merchant Country]_nicht `US` oder `UK` ist.

   - Um [!DNL PayPal PayLater] als Zahlungsoption mit Braintree einzubeziehen, setzen Sie **[!UICONTROL Enable PayPal PayLater through Braintree]** auf `Yes`.

     Wenn **[!UICONTROL Enable PayPal PayLater through Braintree]** auf `Yes` gesetzt ist, wird nur dieses Feld angezeigt.

     Sie können PayLater-Nachrichten auf Ihrer Site für Angebote wie _Pay in 3_ anzeigen, mit denen Kunden mit drei zinsfreien monatlichen Zahlungen zahlen können. Die Braintree-Integration kann Meldungen auf Ihrer Site anzeigen, um diese Funktion zu bewerben. Sie können PayLater-Angebote nicht mit anderen Inhalten, Marketingaktivitäten oder Materialien bewerben.

1. Geben Sie für **[!UICONTROL Title]** einen Titel ein, der die Braintree-Zahlung nach PayPal-Option beim Checkout angibt.

1. Setzen Sie **[!UICONTROL Vault Enabled]** auf `Yes` , um die Verwendung eines sicheren Vault zum Speichern des PayPal-Kontos von Kunden zu aktivieren. Für zukünftige Transaktionen kann ein ausgewertetes PayPal-Konto verwendet werden, wodurch sich die Anzahl der Schritte für Kunden verringert.

1. Setzen Sie **[!UICONTROL Send Cart Line Items for PayPal]** auf `Yes` , um die Zeileneinträge (Bestelleinträge) zusammen mit Geschenkkarten, Geschenkverpackungen für Artikel, Geschenkverpackungen für Bestellungen, Gutschriften für Geschäfte, Versand und Steuern als Zeileneinträge an PayPal zu senden.

1. Geben Sie für **[!UICONTROL Sort Order]** eine Zahl ein, um die Reihenfolge zu bestimmen, in der die Zahlungsoption Braintree PayPal angezeigt wird, wenn sie beim Checkout mit anderen Zahlungsoptionen aufgeführt wird.

1. Um den Namen Ihres Händlers anders anzuzeigen als in Ihrer [Store-Konfiguration](../getting-started/store-details.md#store-information) definiert, geben Sie den Namen in das Feld **[!UICONTROL Override Merchant Name]** ein, wie er angezeigt werden soll.

1. Setzen Sie **[!UICONTROL Payment Action]** auf einen der folgenden Werte:

   - `Authorize Only` - Genehmigt den Kauf und legt einen Besitz an den Fonds fest. Der Betrag wird erst dann vom Bankkonto des Kunden abgezogen, wenn der Verkauf vom Händler _erfasst_ wurde.
   - `Authorize and Capture` - Der Betrag des Kaufs wird genehmigt und sofort vom Konto des Kunden zurückgezogen.

1. Setzen Sie **[!UICONTROL Payment from Applicable Countries]** für Braintree-Transaktionen, die von PayPal verarbeitet werden, auf einen der folgenden Werte:

   - `All Allowed Countries` - Kunden aus allen in Ihrer Store-Konfiguration angegebenen [Ländern](../getting-started/store-details.md#country-options) können diese Zahlungsmethode verwenden.
   - `Specific Countries` - Nach Auswahl dieser Option wird die Liste _[!UICONTROL Payment from Specific Countries]_angezeigt. Halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und wählen Sie jedes Land in der Liste aus, in dem Kunden Käufe in Ihrem Geschäft tätigen können.

1. Damit Kunden eine Rechnungsadresse angeben müssen, setzen Sie **[!UICONTROL Require Customer's Billing Address]** auf `Yes`.

   >[!NOTE]
   >
   >Diese Funktion muss vom technischen Support von PayPal für Ihr Konto aktiviert werden.

1. Um eine Protokolldatei mit Interaktionen zwischen Ihrem Store und PayPal über Braintree zu speichern, setzen Sie **[!UICONTROL Debug]** auf `Yes`.

1. Um die Schaltfläche PayPal sowohl auf der Mini-Warenkorbseite als auch auf der Warenkorbseite anzuzeigen, setzen Sie **[!UICONTROL Display on Shopping Cart]** auf `Yes`.

## Schritt 12: Stileinstellungen festlegen

1. Wählen Sie für **[!UICONTROL Location]** aus, wo PayPal-Schaltflächen und -Nachrichten gerendert werden: `Mini-Cart and Cart Page`, `Checkout Page` oder `Product Page`

   ![PayPal-Stileinstellungen](../configuration-reference/sales/assets/payment-methods-braintree-paypal-styling.png){width="600" zoomable="yes"}

### [!UICONTROL Mini-Cart and Cart Page]

Die Optionen und Einstellungen in diesem Abschnitt variieren je nach Einstellung im Feld _[!UICONTROL Location]_.

1. Setzen Sie **[!UICONTROL PayPal Button Type]** auf einen von drei Schaltflächentypen: `PayPal Button` / `PayPal Pay Later Button` / `PayPal Credit Button`

**[!UICONTROL PayPal Button]**

Die Optionen und Einstellungen in diesem Abschnitt variieren je nach dem im Feld _[!UICONTROL PayPal Button Type]_ausgewählten Schaltflächentyp.

1. Um die Schaltfläche PayPal auf der Storefront an der ausgewählten Position anzuzeigen, setzen Sie **[!UICONTROL Show PayPal Button]** auf `Yes`.

1. Wählen Sie für **[!UICONTROL Button Label]** die Schaltflächenbeschriftung PayPal aus: `Paypal`, `Checkout`, `Buynow` oder `Pay`

1. Wählen Sie für **[!UICONTROL Color]** die Schaltflächenfarbe PayPal aus: `Blue`, `Black`, `Gold` oder `Silver`

1. Wählen Sie für **[!UICONTROL Shape]** die Schaltflächenform PayPal aus: `Pill` oder `Rectangle`

1. Wählen Sie für **[!UICONTROL Size (Deprecated)]** die Schaltflächengröße PayPal aus: `Medium`, `Large` oder `Responsive`

>[!NOTE]
>
>Das Konfigurationsfeld **[!DNL Size(Deprecated)]** ist veraltet und wird nicht zum Formatieren der PayPal-Schaltflächen verwendet.

**[!UICONTROL PayLater Messaging]**

1. Um die [!DNL PayLater]-Nachrichten auf der Storefront an der ausgewählten Position anzuzeigen, setzen Sie **[!UICONTROL Show PayLater Messaging]** auf `Yes`.

   Diese Nachricht beinhaltet die Anzeige von [!DNL PayLater]-Nachrichten für verfügbare Angebote ([Beschränkungen gelten](https://developer.paypal.com/docs/checkout/pay-later/us/)).

1. Wählen Sie für **[!UICONTROL Message Layout]** das Layout der [!DNL PayLater] Nachricht aus: `Text` oder `Flex`

1. Wählen Sie für **[!UICONTROL Logo]** den Logotyp PayPal aus: `Inline`, `Primary`, `Alternative` oder `None`

1. Wählen Sie für **[!UICONTROL Logo Position]** die Position des PayPal-Logos aus: `Left`, `Right` oder `Top`

1. Wählen Sie für **[!UICONTROL Text Color]** die Textfarbe [!DNL PayLater] der Nachricht aus: `Black`, `White`, `Monochrome` oder `Grayscale`

Wenn diese Optionen festgelegt sind, können Sie die Vorschau der PayPal-Schaltflächen und PayLater-Nachrichten sehen. Es gibt Steuerelemente, mit denen Sie die Einstellungen anwenden oder die Werte zurücksetzen können:

- Um die ausgewählten Stileinstellungen für Schaltflächen und PayLater-Nachrichten zu speichern und sie auf die aktuelle Position und den aktuellen Schaltflächentyp anzuwenden, klicken Sie auf **[!UICONTROL Apply]**.

- Um die ausgewählten Stileinstellungen für Schaltflächen und PayLater-Nachrichtenwerte zu speichern und sie auf alle Schaltflächentypen und -speicherorte anzuwenden, klicken Sie auf **[!UICONTROL Apply to All Buttons]**.

- Um die Stileinstellungen auf die empfohlenen Standardwerte für Schaltflächen und PayLater-Nachrichten zurückzusetzen und sie auf alle Schaltflächentypen und -speicherorte anzuwenden, klicken Sie auf **[!UICONTROL Reset to Recommended Defaults]**.

## Schritt 13: 3D-Verifizierungseinstellungen durchführen

1. Wenn Sie einen Überprüfungsschritt für Kunden hinzufügen möchten, die Kreditkarten verwenden, die in einem Überprüfungsprogramm registriert sind (z. B. _Verifiziert durch VISA_), setzen Sie **[!UICONTROL 3D Secure Verification]** auf `Yes`.

   Während des Prozesses wird der Transaktionsbetrag, der zur Überprüfung vorgelegt wird, mit dem Betrag verglichen, der zur Genehmigung gesendet wird.

2. Um die 3D Secure-Anforderung immer für alle Transaktionen herauszufordern, setzen Sie **[!UICONTROL Always request 3DS]** auf `Yes`.

3. Geben Sie für &quot;**[!UICONTROL Threshold Amount]**&quot;den Mindestbestellbetrag ein, der für die Trigger-3D-Verifizierung erforderlich ist.

4. Setzen Sie **[!UICONTROL Verify for Applicable Countries]** auf einen der folgenden Werte:

   - `All Allowed Countries` - Kunden aus allen in Ihrer Store-Konfiguration angegebenen [Ländern](../getting-started/store-details.md#country-options) können diese Zahlungsmethode verwenden.
   - `Specific Countries` - Nach Auswahl dieser Option wird die Liste _[!UICONTROL Verify for Specific Countries]_angezeigt. Halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und wählen Sie jedes Land in der Liste aus, in dem Kunden Käufe in Ihrem Geschäft tätigen können.

   ![3D-Überprüfungseinstellungen](../configuration-reference/sales/assets/payment-methods-braintree-3d-secure-verify-config.png){width="600" zoomable="yes"}

## Schritt 14: Einrichten der dynamischen Braintree-Deskriptoren

Die folgenden Deskriptoren werden verwendet, um Käufe in Kreditkartenabschlüssen von Kunden zu identifizieren. Sie können die Anzahl der Gebühren reduzieren, indem Sie das Unternehmen, das mit jedem Kauf verbunden ist, eindeutig identifizieren. Wenn dynamische Deskriptoren für Ihr Konto nicht aktiviert sind, wenden Sie sich an den Braintree-Support.

![Dynamische Deskriptoren](../configuration-reference/sales/assets/payment-methods-braintree-dynamic-config.png){width="600" zoomable="yes"}

1. Geben Sie den dynamischen Deskriptor für die **[!UICONTROL Name]**, **[!UICONTROL Phone]** und **[!UICONTROL URL]** gemäß den folgenden Richtlinien ein:

   - **[!UICONTROL Name]** - Der Namensdeskriptor besteht aus zwei Teilen, die durch ein Sternchen (*) getrennt sind. Beispiel:

     `company*myproduct`

     Der erste Teil des Deskriptors identifiziert das Unternehmen oder DBA und der zweite Teil das Produkt. Die Länge der Teile `company` und `product` des Deskriptors kann auf folgende Weise für eine kombinierte Länge von bis zu 22 Zeichen zugeordnet werden.

     **_Zeichen im Namensdeskriptor_**

     _Option 1:_ `Company` muss aus drei Zeichen bestehen, `Product` darf bis zu 18 Zeichen lang sein

     _Option 2:_ `Company` muss aus sieben Zeichen bestehen, `Product` darf bis zu 14 Zeichen lang sein

     _Option 3_: `Company` muss 12 Zeichen lang sein, `Product` darf bis zu neun Zeichen lang sein

   - **[!UICONTROL Phone]** - Der Telefondeskriptor muss 10 bis 14 Zeichen lang sein und darf nur Zahlen, Bindestriche, Klammern und Punkte enthalten. Beispiel:

     `9999999999`

     `(999) 999-9999`

     `999.999.9999`

   - **[!UICONTROL URL]** - Der URL-Deskriptor stellt Ihren Domänennamen dar und kann bis zu 13 Zeichen lang sein. Beispiel:

     `company.com`

1. Klicken Sie nach Abschluss der Braintree-Konfiguration auf **[!UICONTROL Save Config]**.

## 2.4 - Upgrade-Hinweise

Ab Adobe Commerce und Magento Open Source 2.4.0 ist die Braintree-Erweiterung in der -Version enthalten. Wenn Sie von einer Version vor 2.4.0, in der die Marketplace-Braintree-Erweiterung installiert ist, auf Commerce 2.4.x migrieren, müssen Sie diese Erweiterung (`paypal/module-braintree` oder `gene/module-braintree`) deinstallieren und alle Codeanpassungen aktualisieren, um den Namespace `PayPal_Braintree` anstelle von `Magento_Braintree` zu verwenden. Konfigurationseinstellungen aus der gebündelten Commerce Braintree Payments-Erweiterung und der auf Commerce Marketplace verteilten Erweiterung bleiben erhalten und Zahlungen, die mit diesen Vorgängerversionen platziert wurden, können dennoch wie gewohnt erfasst, ungültig gemacht oder rückerstattet werden.

[1]: https://www.braintreepayments.com/
[2]: https://developers.braintreepayments.com/reference/general/testing/php
