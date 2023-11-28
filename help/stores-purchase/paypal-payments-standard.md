---
title: PayPal Payments Standard
description: Erfahren Sie, wie Sie PayPal Payments Standard als Online-Zahlungslösung in Ihrem Geschäft einrichten.
exl-id: b4024dac-34d7-4f1a-ad9d-0fc406194609
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '2073'
ht-degree: 0%

---

# PayPal Payments Standard

[PayPal Payments Standard][4] ist der einfachste Weg, Zahlungen online zu akzeptieren. Sie können Ihren Kunden die bequeme Bezahlung sowohl per Kreditkarte als auch per PayPal anbieten, indem Sie einfach eine Checkout-Schaltfläche zu Ihrem Geschäft hinzufügen.

>[!NOTE]
>
>Bei Händlern außerhalb der USA heißt es: _PayPal Website Payments Standard_.

Mit PayPal Payments Standard können Sie Kreditkarten auf Mobilgeräten wischen. Es gibt keine monatliche Gebühr und Sie können per eBay bezahlt werden. Zu den unterstützten Kreditkarten gehören Visa, MasterCard, Discover und American Express. Darüber hinaus können Kunden direkt von ihren persönlichen PayPal-Konten bezahlen. PayPal Payments Standard ist in allen Ländern auf der weltweiten PayPal Referenzliste verfügbar.

>[!IMPORTANT]
>
>**PSD2-Anforderungen:** <br/>
>Ab dem 14. September 2019 könnten europäische Banken Zahlungen ablehnen, die nicht erfüllt sind [PSD2](../getting-started/compliance-payment-services-directive.md) Anforderungen. Für die Einhaltung von PSD2 ist kein Eingreifen erforderlich, da alle Anforderungen von PayPal bearbeitet werden.

## Handelsanforderungen

- [PayPal-Geschäftskonto][1]

## Checkout-Workflow

Für Kunden ist PayPal Payments Standard ein einstufiger Prozess, wenn die Kreditkarteninformationen auf ihren persönlichen PayPal-Konten auf dem neuesten Stand sind.

1. **Customer Places Order** - Der Kunde klickt/tippt auf die _Jetzt bezahlen_ zum Abschließen des Kaufs.

1. **PayPal verarbeitet die Transaktion** - Der Kunde wird zur PayPal-Site weitergeleitet, um die Transaktion abzuschließen.

## PayPal Payments Standard einrichten

>[!NOTE]
>
>PayPal Payments Standard kann nicht gleichzeitig mit anderen PayPal-Methoden verwendet werden, einschließlich Express Checkout. Wenn Sie Zahlungslösungen ändern, ist die zuvor verwendete Lösung deaktiviert.

>[!TIP]
>
>Klicks **[!UICONTROL Save Config]** um den Fortschritt zu speichern.

### Schritt 1: Konfiguration beginnen

Bei dieser Einrichtungsmethode wird davon ausgegangen, dass Sie über ein vorhandenes PayPal-Konto verfügen.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen **[!UICONTROL Payment Methods]**.

1. Wenn Ihre Commerce-Installation über mehrere Websites, Stores oder Ansichten verfügt, legen Sie **[!UICONTROL Store View]** in die Store-Ansicht, auf die Sie diese Konfiguration anwenden möchten.

1. Im _[!UICONTROL Merchant Location]_auswählen, wählen Sie die **[!UICONTROL Merchant Country]**wo sich Ihr Unternehmen befindet.

   Diese Einstellung bestimmt die Auswahl der PayPal-Lösungen, die in der Konfiguration angezeigt werden.

   ![Merchant Country](../configuration-reference/sales/assets/payment-methods-merchant-location.png){width="600" zoomable="yes"}

1. Erweitern **[!UICONTROL PayPal All-in-One Payment Solutions]** und klicken **[!UICONTROL Configure]** für **[!UICONTROL Payments Standard]**.

   ![PayPal Payments Standard](./assets/paypal-payments-standard.png){width="700" zoomable="yes"}

### Schritt 2: Aktivieren und Verbinden Ihres PayPal-Kontos

![PayPal Payments Standard-Konfiguration](./assets/paypal-payments-display.png){width="600" zoomable="yes"}

1. Verbinden Sie Ihr Konto für Test oder Produktion:

   - Klicken Sie für den Testmodus (Entwicklung) auf **[!UICONTROL Sandbox Credentials]** und geben Sie [PayPal-Sandbox][3] Anmeldedaten.
   - Klicken Sie im Produktionsmodus auf **[!UICONTROL Connect with PayPal]** und geben Sie die Anmeldedaten für das Produktionskonto ein.

   Wenn Ihre Verbindung validiert wurde, können Sie fortfahren.

1. Satz **[!UICONTROL Enable this Solution]** nach `Yes`.

1. Wenn Sie ein Angebot erstellen möchten [PayPal Credit](paypal.md#paypal-credit-and-pay-later) für Ihre Kunden festlegen, **[!UICONTROL Enable PayPal Credit]** nach `Yes`.

### Schritt 3: Ausführen der Einstellungen für den Payments-Standard

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Payments Standard]** Abschnitt.

   ![Erforderliche Einstellungen](../configuration-reference/sales/assets/payment-methods-paypal-payments-standard-required.png){width="600" zoomable="yes"}

1. Geben Sie die **[!UICONTROL Email Associated with your PayPal Merchant Account]**.

   >[!IMPORTANT]
   >
   >Bei E-Mail-Adressen wird zwischen Groß- und Kleinschreibung unterschieden. Um eine Zahlung zu erhalten, muss die von Ihnen eingegebene E-Mail-Adresse mit der in Ihrem PayPal-Handelskonto angegebenen E-Mail-Adresse übereinstimmen.

   Wenn Sie kein PayPal-Konto haben, klicken Sie auf **[!UICONTROL Start accepting payments via PayPal]**.

1. Satz **[!UICONTROL API Authentication Methods]** auf einen der folgenden Werte zu:

   - `API Signature` - Diese PayPal-Authentifizierungsmethode ist am einfachsten zu implementieren und basiert auf Ihrem Benutzernamen, Kennwort und einer eindeutigen Zeichenfolge aus Zeichen und Zahlen, die Ihr Konto identifiziert. API-Signaturberechtigungen laufen nicht ab.
   - `API Certificate` - Diese PayPal-Authentifizierungsmethode ist sicherer und basiert auf Ihrem Benutzernamen, Kennwort und einem herunterladbaren Zertifikat. API-Anmeldeinformationen laufen nach drei Jahren ab und müssen verlängert werden.

   Führen Sie bei Bedarf Folgendes aus:

   - **[!UICONTROL API Username]**
   - **[!UICONTROL API Password]**
   - **[!UICONTROL API Signature]**

1. Wenn Sie Anmeldeinformationen aus Ihrem Sandbox-Konto verwenden, legen Sie **[!UICONTROL Sandbox Mode]** nach `Yes`.

   Verwenden Sie beim Testen der Konfiguration in einer Sandbox nur [Kreditkartennummern][2] die von PayPal empfohlen werden. Wenn Sie bereit sind, zur Produktion zu wechseln, kehren Sie zur Konfiguration zurück und legen Sie den Sandbox-Modus auf `No` und stellen Sie eine Verbindung zu Ihrem PayPal-Produktionskonto her.

1. Wenn Ihr System einen Proxy-Server verwendet, um die Verbindung zwischen Adobe Commerce oder Magento Open Source und dem PayPal-Zahlungssystem herzustellen, setzen Sie **[!UICONTROL API Uses Proxy]** nach `Yes` und führen Sie Folgendes aus:

   - **[!UICONTROL Proxy Host]**
   - **[!UICONTROL Proxy Port]**

### Schritt 4: Einrichten von Advertise PayPal Credit / Advertise PayPal PayLater (optional)

Ab Version 2.4.3 wird PayPal PayLater in Implementierungen unterstützt, die PayPal enthalten. Diese Funktion ermöglicht es den Käufern, eine Bestellung in zweiwöchigen Tranchen zu bezahlen, anstatt den vollen Betrag zum Zeitpunkt des Kaufs zu zahlen. Das PayPal-Krediterlebnis wird nicht mehr unterstützt.

Satz **[!UICONTROL Enable PayPal PayLater Experience]** auf einen der folgenden Werte zu:

- `Yes` - Einrichten von Advertise PayPal PayLater
- `No` - So richten Sie Advertising PayPal Credit ein

#### Advertise PayPal Credit

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Advertise PayPal Credit]** Abschnitt.

   ![Advertising PayPal Credit - Einstellungen der Startseite](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit-home-page.png){width="600" zoomable="yes"}

1. Um Ihre Kontoinformationen zu erhalten, klicken Sie auf **[!UICONTROL Get Publisher ID from PayPal]** und befolgen Sie die Anweisungen.

1. Geben Sie Ihre **[!UICONTROL Publisher ID]**.

   ![Advertise PayPal Credit](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png){width="600" zoomable="yes"}

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Home Page]** Abschnitt.

1. Um ein Banner auf der Seite zu platzieren, legen Sie **[!UICONTROL Display]** nach `Yes`.

1. Satz **[!UICONTROL Position]** auf einen der folgenden Werte zu:

   - `Header (center)`
   - `Sidebar (right)`

1. Satz **[!UICONTROL Size]** auf einen der folgenden Werte zu:

   - `190 x 100`
   - `234 x 60`
   - `300 x 50`
   - `468 x 60`
   - `728 x 90`
   - `800 x 66`

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die verbleibenden Abschnitte und wiederholen Sie die vorherigen Schritte:

   - **[!UICONTROL Catalog Category Page]**
   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**

#### Advertise PayPal PayLater

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Advertise PayPal PayLater]** Abschnitt.

1. Satz **[!UICONTROL Enable PayPal PayLater]** nach `Yes`.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Home Page]** Abschnitt.

   ![Advertising PayPal Credit - Einstellungen der Startseite](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-paylater-home-page.png){width="600" zoomable="yes"}

1. Um ein Banner auf der Seite zu platzieren, legen Sie **[!UICONTROL Display]** nach `Yes`.

1. Satz **[!UICONTROL Position]** auf einen der folgenden Werte zu:

   - `Header (center)`
   - `Sidebar`

1. Satz **[!UICONTROL Style Layout]** auf einen der folgenden Werte zu:

   - `Text`
   - `Flex`

1. Für [!UICONTROL Style Layout] **[!UICONTROL Text]** nur festlegen **[!UICONTROL Logo Type]** auf einen der folgenden Werte zu:

   - `Primary`
   - `Alternative`
   - `Inline`
   - `None`

1. Für [!UICONTROL Style Layout] **[!UICONTROL Text]** nur festlegen **[!UICONTROL Logo Position]** auf einen der folgenden Werte zu:

   - `Left`
   - `Right`
   - `Top`

1. Für [!UICONTROL Style Layout] **[!UICONTROL Text]** nur festlegen **[!UICONTROL Text Color]** auf einen der folgenden Werte zu:

   - `Black`
   - `White`
   - `Monochrome`
   - `Grayscale`

1. Für [!UICONTROL Style Layout] **[!UICONTROL Text]** nur festlegen **[!UICONTROL Text Size]** auf einen der folgenden Werte zu:

   - `10px`
   - `11px`
   - `12px`
   - `13px`
   - `14px`
   - `15px`
   - `16px`

1. Für [!UICONTROL Style Layout] **[!UICONTROL Flex]** nur festlegen **[!UICONTROL Ratio]** auf einen der folgenden Werte zu:

   - `1x1`
   - `1x4`
   - `8x1`
   - `20x1`

1. Für [!UICONTROL Style Layout] **[!UICONTROL Flex]** nur festlegen **[!UICONTROL Color]** auf einen der folgenden Werte zu:

   - `Blue`
   - `Black`
   - `White`
   - `White No Border`
   - `Gray`
   - `Monochrome`
   - `Grayscale`

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die verbleibenden Abschnitte und wiederholen Sie die vorherigen Schritte:

   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**
   - **Zahlungsschritt**
   - **[!UICONTROL Catalog Category Page]**

### Schritt 5: Grundlegende Einstellungen durchführen

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Basic Settings - PayPal Website Payments Standard]** Abschnitt.

   ![Grundlegende Einstellungen](./assets/paypal-payments-basic.png){width="600" zoomable="yes"}

1. Für **[!UICONTROL Title]** Geben Sie einen Titel ein, der diese Zahlungsmethode beim Checkout angibt.

   Es wird empfohlen, den Titel _PayPal_ für alle Store-Ansichten.

1. Wenn Sie mehrere Zahlungsmethoden anbieten, geben Sie eine Zahl für **[!UICONTROL Sort Order]** um die Reihenfolge zu bestimmen, in der PayPal Payments Standard erscheint, wenn es mit den anderen Zahlungsmethoden aufgeführt wird.

   Diese Zahl ist relativ zu den anderen Zahlungsmethoden. (`0` = first, `1` = Sekunde, `2` = drittes Element usw.)

1. Satz **[!UICONTROL Payment Action]** auf einen der folgenden Werte zu:

   - `Authorization` - Genehmigt den Kauf und hält die Mittel fest. Der Betrag wird erst zurückgezogen, wenn er vom Händler eingezogen wurde.
   - `Sale` - Der Kaufbetrag wird genehmigt und sofort vom Konto des Kunden zurückgezogen.

1. So zeigen Sie _[!UICONTROL Check out with PayPal]_Schaltfläche auf der Produktseite festlegen **[!UICONTROL Display on Product Details Page]**nach `Yes`.

### Schritt 6: Erweiterte Einstellungen durchführen

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Advanced Settings]** Abschnitt.

   ![Erweiterte Einstellungen](../configuration-reference/sales/assets/payment-methods-paypal-payment-standard-advanced.png){width="600" zoomable="yes"}

1. Um PayPal Payments Standard sowohl im Warenkorb als auch im Mini-Warenkorb verfügbar zu machen, legen Sie **[!UICONTROL Display on Shopping Cart]** nach `Yes`.

1. Satz **[!UICONTROL Payment from Applicable Countries]** auf einen der folgenden Werte zu:

   - `All Allowed Countries` - Kunden von allen [Länder](../getting-started/store-details.md#country-options) Diese Zahlungsmethode kann in Ihrer Store-Konfiguration verwendet werden.
   - `Specific Countries` - Wenn Sie diese Option ausgewählt haben, wird die _[!UICONTROL Payment from Specific Countries]_angezeigt. Um mehrere Länder auszuwählen, halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie auf jede Option.

1. Um die Kommunikation mit dem Zahlungssystem in der Protokolldatei aufzuzeichnen, legen Sie **[!UICONTROL Debug Mode]** nach `Yes`.

   >[!NOTE]
   >
   >Die Protokolldatei wird auf dem Server gespeichert und steht nur Entwicklern zur Verfügung. Gemäß PCI Data Security Standards werden Kreditkarteninformationen nicht in der Protokolldatei aufgezeichnet.

1. Um die SSL-Verifizierung zu aktivieren, legen Sie **[!UICONTROL Enable SSL Verification]** nach `Yes`.

1. Um eine Zusammenfassung jedes Zeileneintrags in der Bestellung auf Ihrer PayPal-Zahlungsseite anzuzeigen, legen Sie **[!UICONTROL Transfer Cart Line Items]** nach `Yes`.

   Um bis zu zehn Versandoptionen in die Zusammenfassung aufzunehmen, legen Sie **[!UICONTROL Transfer Shipping Options]** nach `Yes`. (Diese Option wird nur angezeigt, wenn Zeileneinträge für die Übertragung festgelegt sind.)

1. Um den Bildtyp zu bestimmen, der für die PayPal-Akzeptanzschaltfläche verwendet wird, legen Sie **[!UICONTROL Shortcut Buttons Flavor]** auf einen der folgenden Werte zu:

   - `Dynamic` - (Empfohlen) Zeigt ein Bild an, das dynamisch vom PayPal-Server aus geändert werden kann.
   - `Static` - Zeigt ein bestimmtes Bild an, das nicht dynamisch geändert werden kann.

1. Damit Kunden, die kein PayPal-Konto haben, mit dieser Methode einen Kauf tätigen können, legen Sie **[!UICONTROL Enable PayPal Guest Checkout]** nach `Yes`.

1. Satz **[!UICONTROL Require Customer's Billing Address]** auf einen der folgenden Werte zu:

   - `Yes` - Erfordert die Rechnungsadresse des Kunden für alle Käufe.
   - `No` - Für Käufe ist die Rechnungsadresse des Kunden nicht erforderlich.
   - `For Virtual Quotes Only` - Erfordert nur die Abrechnungsadresse des Kunden für virtuelle Angebote.

1. So lassen Sie zu, dass ein Kunde eine [PayPal-Abrechnungsvertrag](paypal-billing-agreements.md) mit Ihrem Geschäft, wenn im Kundenkonto keine aktiven Abrechnungsvereinbarungen verfügbar sind, legen Sie **[!UICONTROL Billing Agreement Signup]** auf einen der folgenden Werte zu:

   - `Auto` - Der Kunde kann entweder während des Express Checkout-Flusses einen Abrechnungsvertrag schließen oder eine andere Zahlungsmethode verwenden.
   - `Ask Customer` - Der Kunde kann während des Express Checkout-Workflows entscheiden, ob er einen Abrechnungsvertrag schließt.
   - `Never` - Der Kunde kann während des Express-Checkout-Workflows keinen Abrechnungsvertrag schließen.

   >[!NOTE]
   >
   >Händler müssen den technischen Support von PayPal Merchant anfordern, um Abrechnungsvereinbarungen in ihren Konten zu ermöglichen. Die _Unterzeichnung des Abrechnungsabkommens_ kann nur aktiviert werden, nachdem PayPal bestätigt hat, dass Abrechnungsvereinbarungen für Ihr Händlerkonto aktiviert sind.

1. Damit der Kunde die Transaktion von der PayPal-Site aus abschließen kann, ohne zur Bestellprüfung zu Ihrem Store zurückzukehren, legen Sie **[!UICONTROL Skip Order Review Step]** nach `Yes`.

### Schritt 7: Konfigurationseinstellungen abschließen und speichern

1. Füllen Sie nach Bedarf die folgenden Abschnitte für Ihren Store aus:

   - [Einstellungen der PayPal-Abrechnungsvereinbarung](#paypal-billing-agreement-settings)
   - [Berichtseinstellungen einrichten](#settlement-report-settings)
   - [Frontend-Erlebniseinstellungen](#frontend-experience-settings)

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

#### Einstellungen der PayPal-Abrechnungsvereinbarung

A [Abrechnungsvereinbarung](paypal-billing-agreements.md) ist ein Kaufvertrag zwischen dem Händler und dem Kunden, der von PayPal zur Verwendung mit mehreren Bestellungen genehmigt wurde. Während des Checkout-Prozesses wird die Zahlungsoption für die Abrechnungsvereinbarung nur für Kunden angezeigt, die bereits einen Abrechnungsvertrag mit Ihrem Unternehmen geschlossen haben. Nachdem PayPal die Vereinbarung genehmigt hat, gibt das Zahlungssystem eine eindeutige Referenz-ID aus, um jede Bestellung zu identifizieren, die der Vereinbarung zugeordnet ist. Ähnlich wie bei einer Bestellung gibt es keine Begrenzung für die Anzahl der Abrechnungsvereinbarungen, die ein Kunde mit Ihrem Unternehmen schließen kann.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL PayPal Billing Agreement Settings]** Abschnitt.

   ![Rechnungsabschlussparameter](../configuration-reference/sales/assets/payment-methods-paypal-express-checkout-billing-agreement-settings.png){width="600" zoomable="yes"}

1. Satz **[!UICONTROL Enabled]** nach `Yes`.

1. Für **[!UICONTROL Title]** eingeben, geben Sie einen Titel ein, der die Methode der PayPal-Abrechnungsvereinbarung während des Kassengangs angibt.

1. Wenn Sie mehrere Zahlungsmethoden anbieten, geben Sie im Feld **[!UICONTROL Sort Order]** -Feld, um die Reihenfolge zu bestimmen, in der die Abrechnungsvereinbarung angezeigt wird, wenn sie beim Checkout mit anderen Zahlungsmethoden aufgelistet wird.

1. Satz **[!UICONTROL Payment Action]** auf einen der folgenden Werte zu:

   - `Authorization` - Genehmigt den Kauf und hält die Mittel fest. Der Betrag wird erst dann zurückgezogen, wenn er vom Händler &quot;erfasst&quot;wurde.
   - `Sale` - Der Kaufbetrag wird genehmigt und sofort vom Konto des Kunden zurückgezogen.

1. Satz **[!UICONTROL Payment Applicable From]** auf einen der folgenden Werte zu:

   - `All Allowed Countries` - Kunden aus allen in Ihrer Store-Konfiguration angegebenen Ländern können diese Zahlungsmethode verwenden.
   - `Specific Countries` - Nach Auswahl dieser Option wird die _[!UICONTROL Payment from Specific Countries]_angezeigt. Um mehrere Länder auszuwählen, halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie auf jedes Land.

1. Um die Kommunikation mit dem Zahlungssystem in der Protokolldatei aufzuzeichnen, legen Sie **[!UICONTROL Debug Mode]** nach `Yes`.

   >[!NOTE]
   >
   >Die Protokolldatei wird auf dem Server gespeichert und steht nur Entwicklern zur Verfügung. Gemäß PCI Data Security Standards werden Kreditkarteninformationen nicht in der Protokolldatei aufgezeichnet.

1. Um die SSL-Verifizierung zu aktivieren, legen Sie **[!UICONTROL Enable SSL Verification]** nach `Yes`.

1. Um eine Zusammenfassung jedes Zeileneintrags in der Bestellung des Kunden auf Ihrer PayPal-Zahlungsseite anzuzeigen, legen Sie **[!UICONTROL Transfer Cart Line Items]** nach `Yes`.

1. Um Kunden die Möglichkeit zu geben, eine Abrechnungsvereinbarung über das Dashboard ihres Kundenkontos zu initiieren, legen Sie **[!UICONTROL Allow in Billing Agreement Wizard]** nach `Yes`.

#### Berichtseinstellungen einrichten

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Settlement Report Settings]** Abschnitt.

   ![Berichtseinstellungen einrichten](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png){width="600" zoomable="yes"}

1. Für **[!UICONTROL SFTP Credentials]** führen Sie folgende Schritte aus:

   - Wenn Sie sich für den PayPal Secure FTP Server angemeldet haben, geben Sie die folgenden SFTP-Anmeldedaten ein:

      - Anmelden
      - Kennwort

   - Um Testberichte auszuführen, bevor Sie mit dem Express Checkout auf Ihrer Site live geschaltet werden, legen Sie **[!UICONTROL Sandbox Mode]** nach `Yes`.

   - Geben Sie die **[!UICONTROL Custom Endpoint Hostname or IP Address]**.

     Standardmäßig lautet der Wert `reports.paypal.com`.

   - Geben Sie die **[!UICONTROL Custom Path]** wo Berichte gespeichert werden.

     Standardmäßig lautet der Wert `/ppreports/outgoing`.

1. Um Berichte planmäßig zu erstellen, müssen Sie die Variable **[!UICONTROL Scheduled Fetching]** Einstellungen:

   - Satz **[!UICONTROL Enable Automatic Fetching]** nach `Yes`.

   - Satz **[!UICONTROL Schedule]** auf einen der folgenden Werte zu:

      - `Daily`
      - `Every 3 Days`
      - `Every 7 Days`
      - `Every 10 Days`
      - `Every 14 Days`
      - `Every 30 Days`
      - `Every 40 Days`

     PayPal behält jeden Bericht für 45 Tage bei.

   - Satz **[!UICONTROL Time of Day]** auf die Stunde, Minute und Sekunde, in der die Berichte erstellt werden sollen.

#### Frontend-Erlebniseinstellungen

Verwenden Sie die _[!UICONTROL Frontend Experience Settings]_, um zu wählen, welche PayPal-Logos auf Ihrer Website erscheinen, und um das Erscheinungsbild Ihrer PayPal-Händlergeseiten anzupassen.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Frontend Experience Settings]** Abschnitt.

   ![Frontend-Erlebniseinstellungen](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings1.png){width="600" zoomable="yes"}

1. Wählen Sie die **[!UICONTROL PayPal Product Logo]** die Sie im PayPal-Block in Ihrem Geschäft erscheinen möchten.

   Die PayPal Logos sind in vier Formaten und in zwei Größen erhältlich:

   - `No Logo`
   - `We Prefer PayPal (150 x 60 or 150 x 40)`
   - `Now Accepting PayPal (150 x 60 or 150 x 40)`
   - `Payments by PayPal (150 x 60 or 150 x 40)`
   - `Shop Now Using PayPal (150 x 60 or 150 x 40)`

1. So passen Sie das Erscheinungsbild Ihrer PayPal-Händlerseiten an:

   - Geben Sie den Namen der **[!UICONTROL Page Style]** die Sie auf Ihre PayPal-Händlerseiten anwenden möchten:

      - `paypal` - Verwendet den PayPal-Seitenstil.
      - `primary` - Verwendet den Seitenstil, den Sie als _primary_ -Stile in Ihrem Kontoprofil.
      - `your_custom_value` - Verwendet einen benutzerdefinierten Zahlungsseitenstil, der in Ihrem Kontoprofil angegeben ist.

   - Für **[!UICONTROL Header Image URL]** Geben Sie die URL des Bildes ein, das Sie in der linken oberen Ecke der Zahlungsseite anzeigen möchten. Die maximale Dateigröße ist 750 Pixel breit und 90 Pixel hoch.

     >[!NOTE]
     >
     >PayPal empfiehlt, dass sich das Bild auf einem sicheren (HTTPS-)Server befindet. Andernfalls kann ein Browser darauf hinweisen, dass _Die Seite enthält sowohl sichere als auch nicht sichere Elemente._.

   - Um die Farbe für Ihre Seiten festzulegen, geben Sie den sechsstelligen Hexadezimalcode ohne die `#` für jedes der folgenden Zeichen:

      - **[!UICONTROL Header Background Color]** - Hintergrundfarbe für die Kopfzeile der Kassenseite.
      - **[!UICONTROL Header Border Color]** - Farbe für den Rahmen von zwei Pixeln um die Kopfzeile.
      - **[!UICONTROL Page Background Color]** - Hintergrundfarbe für die Checkout-Seite und um die Kopfzeile und das Zahlungsformular.

[1]: https://www.paypal.com/webapps/mpp/how-to-sell-online
[2]: https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm
[3]: https://developer.paypal.com/docs/api-basics/sandbox/
[4]: https://developer.paypal.com/docs/paypal-payments-standard/mobile-paypal-payments-standard/
