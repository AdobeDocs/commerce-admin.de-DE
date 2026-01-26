---
title: PayPal Express-Checkout
description: Erfahren Sie, wie Sie PayPal Express Checkout als Online-Zahlungslösung in Ihrem Geschäft einrichten.
exl-id: 0cd90306-cf47-4a5f-8994-6ae96904ae2f
feature: Payments
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/de/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '3111'
ht-degree: 0%

---

# PayPal Express-Checkout

Der PayPal Express Checkout hilft, den Umsatz zu steigern, indem er Ihren Kunden die Möglichkeit gibt, mit Kreditkarte oder über die Sicherheit ihrer persönlichen PayPal-Konten zu bezahlen. Während des Checkouts wird der Kunde zur sicheren PayPal-Website weitergeleitet, um die Zahlungsinformationen auszufüllen. Der Kunde wird dann in Ihr Geschäft zurückgeschickt, um den restlichen Checkout-Prozess abzuschließen. Wenn Sie Express Checkout wählen, wird Ihrem Geschäft die vertraute PayPal-Schaltfläche hinzugefügt, die laut Berichten den Umsatz steigert.

>[!IMPORTANT]
>
>**PSD2-Anforderungen:** <br/>
>Ab dem 14. September 2019 können europäische Banken Zahlungen ablehnen, die [PSD2&rbrace;-](../getting-started/compliance-payment-services-directive.md) nicht erfüllen. Die Einhaltung von PSD2 durch PayPal Express Checkout erfordert keine Maßnahmen, da alle Anforderungen durch PayPal abgewickelt werden.

Kunden mit aktuellen PayPal-Konten können einen Kauf in einem einzigen Schritt tätigen, indem sie auf die Schaltfläche _[!UICONTROL Check out with PayPal]_&#x200B;klicken. Express Checkout kann als eigenständige oder mit einer der PayPal-All-in-One-Lösungen verwendet werden. Wenn Sie bereits Kreditkarten online akzeptieren, können Sie Express Checkout als zusätzliche Option anbieten, um neue Kunden zu gewinnen, die lieber mit PayPal bezahlen möchten.

>[!NOTE]
>
>PayPal unterstützt den Verkauf digitaler Waren über den PayPal Express Checkout nicht mehr und empfiehlt, entweder [PayPal Payments Standard](paypal-payments-standard.md) oder ein anderes PayPal-Zahlungs-Gateway zu verwenden, um jede Bestellung zu bearbeiten, die [virtuelle Produkte](../catalog/product-create-virtual.md) enthält.

## Anforderungen

- Händler: [PayPal-Konto für Unternehmen](https://www.paypal.com/webapps/mpp/how-to-sell-online)
- Kunde: [Persönliches PayPal-Konto](https://www.paypal.com/webapps/mpp/buying-online)

## Express-Checkout-Workflow

Im Gegensatz zu anderen Zahlungsmethoden ermöglicht PayPal Express Checkout dem Kunden, am Anfang des üblichen Checkout-Workflows von der Produktseite, dem Mini-Warenkorb und dem Warenkorb aus zu checken.

1. **Kunde platziert Bestellung** - Der Kunde klickt/tippt auf die _[!UICONTROL Check out with PayPal]_.
1. **Kunde wird zur PayPal-Website weitergeleitet** - Der Kunde wird zur PayPal-Website weitergeleitet, um die Transaktion abzuschließen.
1. **Kunde meldet sich bei seinem PayPal-Konto an** - Der Kunde muss sich bei seinem PayPal-Konto anmelden, um die Transaktion abzuschließen. Das Zahlungssystem verwendet die Rechnungs- und Versandinformationen von seinem PayPal-Konto.
1. **Der Kunde kehrt zur Kaufbestätigungsseite zurück** - Der Kunde wird zurück zur Kaufbestätigungsseite in Ihrem Geschäft geleitet, um die Bestellung zu überprüfen.
1. **Kunde gibt Bestellung auf** - Der Kunde gibt die Bestellung auf, und die Bestellinformationen werden an PayPal übermittelt.
1. **PayPal rechnet die Transaktion ab** - PayPal erhält die Bestellung und rechnet die Transaktion ab.

>[!NOTE]
>
>PayPal Express Checkout unterstützt keine Bestellungen mit Mehrfachadressen.

## Kontextbezogenes Auschecken

Der _In-Context Checkout_ von PayPal macht es einfacher denn je, online zu bezahlen. Kunden verlieren bei diesem vereinfachten nahtlosen Ein- oder Zwei-Klick-Checkout nie Ihren Shop aus den Augen. Der kontextbezogene Checkout funktioniert auf Macs und PCs gleichermaßen und bietet ein konsistentes Erlebnis auf Desktop-Computern, Tablets und Mobilgeräten. Weitere Informationen finden Sie unter [Kontextbezogenes Auschecken in einem Express-Checkout](https://www.paypal.com/rs/webapps/mpp/express-checkout).

![Kontextbezogene PayPal-Checkout-Demo](./assets/storefront-paypal-in-context.png){width="700" zoomable="yes"}

[_Kontextbezogene PayPal-Checkout-Demo_](https://demo.paypal.com/us/demo/navigation?merchant=bigbox&page=incontextProductCheckout)

Wenn Sie Ihren Store für [!DNL PayPal Express Checkout] konfigurieren, können Sie diese Option aktivieren.

## Konfigurieren Ihres PayPal-Kontos

Bevor Sie den PayPal Express-Checkout im Commerce-Admin einrichten, müssen Sie Ihr Händlerkonto auf der PayPal-Website konfigurieren.

1. Melden Sie sich bei Ihrem PayPal Advanced-Konto unter [manager.paypal.com](https://manager.paypal.com/) an.

1. Gehen Sie zu **[!UICONTROL Service Settings]** > **[!UICONTROL Hosted Checkout Pages]** > **[!UICONTROL Set Up]** und nehmen Sie die folgenden Einstellungen vor:

   - **[!UICONTROL AVS]**: `No`
   - **[!UICONTROL CSC]**: `No`
   - **[!UICONTROL Enable Secure Token]**: `Yes`

1. Klicken Sie auf **[!UICONTROL Save Changes]**.

1. Einrichten eines anderen Benutzers (empfohlen von PayPal):

   - Gehen Sie [manager.paypal.com](https://manager.paypal.com/) und melden Sie sich bei Ihrem Konto an.

   - Um einen anderen Benutzer einzurichten, befolgen Sie die Anweisungen.

   - Klicken Sie auf **[!UICONTROL Update]**.

## Einrichten des PayPal Express-Checkouts in Commerce

Sie können zwei PayPal-Lösungen gleichzeitig aktivieren: PayPal Express Checkout und eine All-in-One-Lösung. Wenn Sie eine andere Lösung aktivieren, wird die zuvor verwendete automatisch deaktiviert.

>[!NOTE]
>
>Klicken Sie jederzeit auf **[!UICONTROL Save Config]** , um Ihren Fortschritt zu speichern.

### Schritt 1: Starten der Konfiguration

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Payment Methods]**.

1. Wenn Ihre Installation über mehrere Websites, Stores oder Ansichten verfügt, legen Sie **[!UICONTROL Store View]** auf die Store-Ansicht fest, in der Sie diese Konfiguration anwenden möchten.

1. Wählen Sie im Abschnitt _[!UICONTROL Merchant Location]_&#x200B;die **[!UICONTROL Merchant Country]**&#x200B;aus, in der sich Ihr Unternehmen befindet.

   Diese Einstellung bestimmt die Auswahl der PayPal-Lösungen, die in der Konfiguration angezeigt werden.

   ![Handelsland](../configuration-reference/sales/assets/payment-methods-merchant-location.png){width="600" zoomable="yes"}

1. Klicken Sie unter _[!UICONTROL Recommended Solutions]_&#x200B;auf **[!UICONTROL Configure]**&#x200B;für **[!UICONTROL PayPal Express Checkout]**.

   ![Konfigurieren von PayPal Express Checkout](./assets/paypal-express-checkout.png){width="600"}

### Schritt 2: Aktivieren und Verbinden Ihres PayPal-Kontos

1. Erweitern Sie bei Bedarf ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Required PayPal Settings]** .

   ![Verbinden Sie Ihr PayPal-Konto](./assets/paypal-express-required.png){width="600" zoomable="yes"}

1. Verbinden Sie Ihr -Konto für Tests oder die Produktion:

   - Klicken Sie für den Test-(Entwicklungs-)Modus auf **[!UICONTROL Sandbox Credentials]** und geben Sie Ihre [PayPal-Sandbox](https://developer.paypal.com/docs/api-basics/sandbox/)-Anmeldeinformationen ein.
   - Klicken Sie im Produktionsmodus auf **[!UICONTROL Connect with PayPal]** und geben Sie die Anmeldeinformationen für Ihr Produktionskonto ein.

   Wenn Ihre Verbindung validiert wurde, können Sie fortfahren.

1. Legen Sie **[!UICONTROL Enable this Solution]** auf `Yes` fest.

1. So aktivieren Sie [kontextbezogene PayPal-](#in-context-checkout):

   - Legen Sie **[!UICONTROL Enable In-Context Checkout Experience]** auf `Yes` fest.

   - Geben Sie Ihre PayPal-**[!UICONTROL Merchant Account ID]** ein.

     Ihre Händlerkonto-ID befindet sich im Profil Ihres PayPal-Geschäftskontos.

>[!NOTE]
>
>[PayPal-Guthaben](paypal.md#paypal-credit-and-pay-later) ist für diese Zahlungsoption standardmäßig aktiviert.

### Schritt 3: Die erforderlichen PayPal-Einstellungen vornehmen

1. Erweitern Sie bei Bedarf ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Express Checkout]** .

   ![PayPal Express Checkout - erforderliche Einstellungen](./assets/paypal-express-settings.png){width="600" zoomable="yes"}

1. (Optional) Geben Sie die **[!UICONTROL Email Associated with PayPal Merchant Account]** ein.

   >[!IMPORTANT]
   >
   >Bei E-Mail-Adressen wird zwischen Groß- und Kleinschreibung unterschieden. Um eine Zahlung zu erhalten, muss die von Ihnen eingegebene E-Mail-Adresse mit der in Ihrem PayPal-Händlerkonto angegebenen E-Mail-Adresse übereinstimmen.

   Wenn Sie kein PayPal-Konto haben, klicken Sie auf **[!UICONTROL Start accepting payments via PayPal]**.

1. Legen Sie **[!UICONTROL API Authentication Methods]** auf eine der folgenden Einstellungen fest:

   - `API Signature` - Diese PayPal-Authentifizierungsmethode ist am einfachsten zu implementieren und basiert auf Ihrem Benutzernamen, Kennwort und einer eindeutigen Zeichenfolge von Zeichen und Zahlen, die Ihr Konto identifiziert. API-Signatur-Anmeldeinformationen laufen nicht ab.
   - `API Certificate` - Diese PayPal-Authentifizierungsmethode ist sicherer, basiert auf Ihrem Benutzernamen, Passwort und einem herunterladbaren Zertifikat. API-Anmeldeinformationen laufen nach drei Jahren ab und müssen erneuert werden.

   Füllen Sie bei Bedarf Folgendes aus:

   - **[!UICONTROL API Username]**
   - **[!UICONTROL API Password]**
   - **[!UICONTROL API Signature]**

1. Wenn Sie Anmeldeinformationen aus Ihrem Sandbox-Konto verwenden, setzen Sie **[!UICONTROL Sandbox Mode]** auf `Yes`.

   Verwenden Sie beim Testen der Konfiguration in einer Sandbox nur [Kreditkartennummern](https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm) die von PayPal empfohlen werden. Wenn Sie bereit sind, zur Produktion zu wechseln, kehren Sie zur Konfiguration zurück und setzen Sie den Sandbox-Modus auf `No` und verbinden Sie sich mit Ihrem PayPal-Produktionskonto.

1. Wenn Ihr System einen Proxyserver verwendet, um die Verbindung zwischen Commerce und dem PayPal-Zahlungssystem herzustellen, setzen Sie **[!UICONTROL API Uses Proxy]** auf `Yes` und führen Sie Folgendes aus:

   - **[!UICONTROL Proxy Host]**
   - **[!UICONTROL Proxy Port]**

Am Ende dieser Sequenz von Schritten sind die erforderlichen PayPal-Einstellungen abgeschlossen. Sie können mit den allgemeinen und erweiterten Einstellungen fortfahren oder auf **[!UICONTROL Save Config]** klicken und später zurückkehren, um die Konfiguration anzupassen

### Schritt 4: Einrichten von Advertise PayPal Credit / Advertise PayPal PayLater (optional)

Ab Version 2.4.3 wird PayPal Later in Bereitstellungen unterstützt, die PayPal enthalten. Mit dieser Funktion können Käufer eine Bestellung in zweiwöchentlichen Raten bezahlen, anstatt den vollen Betrag zum Zeitpunkt des Kaufs zu bezahlen. Das PayPal-Krediterlebnis ist veraltet.

Legen Sie **[!UICONTROL Enable PayPal PayLater Experience]** auf eine der folgenden Einstellungen fest:

- `Yes` - Einrichten von Advertise PayPal PayLater
- `No` - Einrichten von Advertise PayPal-Guthaben

>[!NOTE]
>
>Mit der **[!UICONTROL Enable PayPal PayLater Experience]** Einstellung wird die [!DNL PayPal PayLater]-Funktion nicht deaktiviert und **_[!UICONTROL PayPal PayLater]_** Schaltflächen werden nicht aus der Storefront entfernt. Um die Schaltflächen **_[!UICONTROL PayPal PayLater]_** und **_[!UICONTROL PayPal Credit]_** in der Storefront zu deaktivieren, müssen Sie den `PayPal Credit` Wert für die **[!UICONTROL Disable Funding Options]**-Einstellung auswählen ([!UICONTROL Advanced Settings] unter [!UICONTROL Frontend Experience Settings]).

#### PayPal-Guthaben ankündigen

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Advertise PayPal Credit]** .

1. Um Ihre Kontoinformationen zu erhalten, klicken Sie auf **[!UICONTROL Get Publisher ID from PayPal]** und folgen Sie den Anweisungen.

1. Geben Sie Ihre **[!UICONTROL Publisher ID]** ein.

   ![Advertise PayPal-Guthaben](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png){width="600" zoomable="yes"}

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Home Page]** .

1. Um ein Banner auf der Seite zu platzieren, setzen Sie **[!UICONTROL Display]** auf `Yes`.

1. Legen Sie **[!UICONTROL Position]** auf eine der folgenden Einstellungen fest:

   - `Header (center)`
   - `Sidebar (right)`

1. Legen Sie **[!UICONTROL Size]** auf eine der folgenden Einstellungen fest:

   - `190 x 100`
   - `234 x 60`
   - `300 x 50`
   - `468 x 60`
   - `728 x 90`
   - `800 x 66`

   ![Advertise PayPal-Credit-Homepage-Einstellungen](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit-home-page.png){width="600" zoomable="yes"}

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) die restlichen Abschnitte und wiederholen Sie die vorherigen Schritte:

   - [!UICONTROL Catalog Category Page]
   - [!UICONTROL Catalog Product Page]
   - [!UICONTROL Checkout Cart Page]

#### Werbung für PayPal PayLater

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Advertise PayPal PayLater]** .

1. Legen Sie **[!UICONTROL Enable PayPal PayLater]** auf `Yes` fest.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Home Page]** .

1. Um ein Banner auf der Seite zu platzieren, setzen Sie **[!UICONTROL Display]** auf `Yes`.

1. Legen Sie **[!UICONTROL Position]** auf eine der folgenden Einstellungen fest:

   - `Header (center)`
   - `Sidebar`

1. Legen Sie **[!UICONTROL Style Layout]** auf eine der folgenden Einstellungen fest:

   - `Text`
   - `Flex`

1. Legen Sie [!UICONTROL Style Layout] nur für **[!UICONTROL Text]** **[!UICONTROL Logo Type]** auf eine der folgenden Einstellungen fest:

   - `Primary`
   - `Alternative`
   - `Inline`
   - `None`

1. Legen Sie [!UICONTROL Style Layout] nur für **[!UICONTROL Text]** **[!UICONTROL Logo Position]** auf eine der folgenden Einstellungen fest:

   - `Left`
   - `Right`
   - `Top`

1. Legen Sie [!UICONTROL Style Layout] nur für **[!UICONTROL Text]** **[!UICONTROL Text Color]** auf eine der folgenden Einstellungen fest:

   - `Black`
   - `White`
   - `Monochrome`
   - `Grayscale`

1. Legen Sie [!UICONTROL Style Layout] nur für **[!UICONTROL Text]** **[!UICONTROL Text Size]** auf eine der folgenden Einstellungen fest:

   - `10px`
   - `11px`
   - `12px`
   - `13px`
   - `14px`
   - `15px`
   - `16px`

1. Legen Sie [!UICONTROL Style Layout] nur für **[!UICONTROL Flex]** **[!UICONTROL Ratio]** auf eine der folgenden Einstellungen fest:

   - `1x1`
   - `1x4`
   - `8x1`
   - `20x1`

1. Legen Sie [!UICONTROL Style Layout] nur für **[!UICONTROL Flex]** **[!UICONTROL Color]** auf eine der folgenden Einstellungen fest:

   - `Blue`
   - `Black`
   - `White`
   - `White No Border`
   - `Gray`
   - `Monochrome`
   - `Grayscale`

   ![Advertise PayPal-Credit-Homepage-Einstellungen](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-paylater-home-page.png){width="600" zoomable="yes"}

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) die restlichen Abschnitte und wiederholen Sie die vorherigen Schritte:

   - [!UICONTROL Catalog Product Page]
   - [!UICONTROL Checkout Cart Page]
   - [!UICONTROL Checkout Payment Step]
   - [!UICONTROL Catalog Category Page]

### Schritt 5: Abschließen der Grundeinstellungen

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Basic Settings - PayPal Express Checkout]** .

   ![Grundeinstellungen](../configuration-reference/sales/assets/payment-methods-paypal-express-checkout-basic-settings.png){width="600" zoomable="yes"}

1. Geben Sie **[!UICONTROL Title]** einen Titel ein, der diese Zahlungsmethode beim Checkout identifiziert.

   Es wird empfohlen, für alle Store _Ansichten den Titel_ PayPal“ zu verwenden.

1. Wenn Sie mehrere Zahlungsmethoden anbieten, geben Sie eine Nummer für **[!UICONTROL Sort Order]** ein, um die Reihenfolge zu bestimmen, in der PayPal Express Checkout angezeigt wird, wenn es mit den anderen Zahlungsmethoden aufgelistet wird.

   Diese Zahl steht im Verhältnis zu den anderen Zahlungsmethoden. (`0` = First, `1` = Second, `2` = Third usw.)

1. Legen Sie **[!UICONTROL Payment Action]** auf eine der folgenden Einstellungen fest:

   - `Authorization` - Genehmigt den Kauf und legt die Mittel fest. Der Betrag wird erst abgehoben, wenn er _Händler_ wird.
   - `Sale` - Der Betrag des Kaufs wird autorisiert und sofort vom Konto des Kunden zurückgezogen.
   - `Order` - Der Betrag der Bestellung wird nicht erfasst oder autorisiert im Kundensaldo, Bankkonto oder Kreditkarte bei PayPal. Die Aktion „Bestellen“ stellt eine Vereinbarung zwischen dem PayPal-Zahlungssystem und dem Händler dar. Sie ermöglicht es dem Händler, einen oder mehrere Beträge bis zur bestellten Gesamtsumme über einen Zeitraum von bis zu 29 Tagen vom Kundenkäuferkonto zu erfassen. Nachdem die Gelder bestellt wurden, kann der Händler sie jederzeit während des folgenden 29-tägigen Zeitraums erfassen. Die Erfassung des Bestellbetrags kann nur vom Commerce-Administrator durchgeführt werden, indem eine oder mehrere Rechnungen erstellt werden.

1. Um die Schaltfläche _[!UICONTROL Check out with PayPal]_&#x200B;auf der Produktseite anzuzeigen, setzen Sie **[!UICONTROL Display on Product Details Page]**&#x200B;auf `Yes`.

1. Wenn die Zahlungsaktion auf `Order` gesetzt ist, führen Sie Folgendes aus

   - **[!UICONTROL Authorization Honor Period (days)]** - Legt fest, wie lange die primäre Autorisierung gültig bleibt. Der Wert sollte gleich dem entsprechenden Wert in Ihrem PayPal-Händlerkonto sein. Der Standardwert in Ihrem PayPal-Händlerkonto ist `3`. Um diese Zahl zu erhöhen, müssen Sie sich an PayPal wenden. Die Autorisierung wird um 11:49 Uhr US Pacific Time des letzten Tages ungültig.

   - **[!UICONTROL Order Valid Period (days)]** - Legt fest, wie lange die Bestellung gültig bleibt. Wenn die Bestellung ungültig wird, können Sie keine Rechnungen mehr dafür erstellen. Geben Sie in Ihrem PayPal-Händlerkonto einen Wert ein, der dem Wert für den Zeitraum der gültigen Bestellung entspricht. Der Standardwert in Ihrem PayPal-Händlerkonto ist `29`. Um diese Nummer zu ändern, müssen Sie sich an PayPal wenden.

   - **[!UICONTROL Number of Child Authorizations]** - Gibt die maximale Anzahl von Genehmigungen für eine einzelne Bestellung an. Diese bestimmt die maximale Anzahl von Online-Teilrechnungen, die Sie für eine Bestellung erstellen können. Dieser Wert sollte gleich der entsprechenden Einstellung in Ihrem PayPal-Händlerkonto sein. Die Standardanzahl an untergeordneten Berechtigungen in Ihrem PayPal-Konto ist `1`. Um diese Zahl zu erhöhen, müssen Sie sich an PayPal wenden.

### Schritt 6: Erweiterte Einstellungen abschließen

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Advanced Settings]** .

   ![Erweiterte Einstellungen - PayPal Express Checkout](../configuration-reference/sales/assets/payment-methods-paypal-express-checkout-advanced-settings.png){width="600" zoomable="yes"}

1. Legen Sie **[!UICONTROL Display on Shopping Cart]** auf `Yes` fest.

1. Legen Sie **[!UICONTROL Payment Applicable From]** auf eine der folgenden Einstellungen fest:

   - `All Allowed Countries` - Kunden aus allen Ländern, die in Ihrer Store-Konfiguration angegeben sind, können diese Zahlungsmethode verwenden.
   - `Specific Countries` - Nach Auswahl dieser Option wird die _[!UICONTROL Payment from Specific Countries]_&#x200B;angezeigt. Zur Auswahl mehrerer Länder halten Sie die Strg-Taste (PC) bzw. die Befehlstaste (Mac) gedrückt und klicken auf die einzelnen Elemente.

1. Um die Kommunikation mit dem Zahlungssystem in die Protokolldatei zu schreiben, setzen Sie **[!UICONTROL Debug Mode]** auf `Yes`.

   Die Protokolldatei für PayPal Payments Advanced wird `_payflow_advanced.log`.

   >[!NOTE]
   >
   >In Übereinstimmung mit den PCI Data Security Standards werden Kreditkarteninformationen nicht in der Protokolldatei aufgezeichnet.

1. Um die Host-Authentizitätsüberprüfung zu aktivieren, setzen Sie **[!UICONTROL Enable SSL Verification]** auf `Yes`.

1. Um eine vollständige Zusammenfassung der Kundenbestellung nach Zeileneintrag auf der PayPal-Website anzuzeigen, setzen Sie **[!UICONTROL Transfer Cart Line Items]** auf `Yes`.

1. Um bis zu zehn Versandoptionen in die Zusammenfassung aufzunehmen, setzen Sie **[!UICONTROL Transfer Shipping Options]** auf `Yes`. (Diese Option wird nur angezeigt, wenn Zeileneinträge auf Übertragung eingestellt sind.)

1. Um die Art des Bildes zu bestimmen, das für die PayPal-Akzeptanzschaltfläche verwendet wird, legen Sie **[!UICONTROL Shortcut Buttons Flavor]** auf einen der folgenden Werte fest:

   - `Dynamic` - (Empfohlen) Zeigt ein Bild an, das dynamisch vom PayPal-Server geändert werden kann.
   - `Static` - Zeigt ein bestimmtes Bild an, das nicht dynamisch geändert werden kann.

1. Damit Kunden ohne PayPal-Konten einen Kauf mit dieser Methode tätigen können, setzen Sie **[!UICONTROL Enable PayPal Guest Checkout]** auf `Yes`.

1. Legen Sie **[!UICONTROL Require Customer's Billing Address]** auf eine der folgenden Einstellungen fest:

   - `Yes` - Erfordert die Rechnungsadresse des Kunden für alle Käufe.
   - `No` - Erfordert für Käufe keine Rechnungsadresse des Kunden.
   - `For Virtual Quotes Only` - Erfordert die Rechnungsadresse des Kunden nur für virtuelle Angebote.

   >[!NOTE]
   >
   >Diese Funktion muss für das Händlerkonto über den technischen Support von PayPal aktiviert werden.

1. (Optional) Legen Sie die **[!UICONTROL Billing Agreement Signup]** fest, damit Kundinnen und Kunden einen [Abrechnungsvertrag](paypal-billing-agreements.md) mit Ihrem Geschäft im PayPal-Zahlungssystem unterzeichnen können, wenn im Kundenkonto keine aktiven Abrechnungsvereinbarungen verfügbar sind:

   - `Auto` - Der Kunde kann entweder während des Express-Checkout-Flusses eine Abrechnungsvereinbarung unterzeichnen oder eine andere Zahlungsmethode verwenden.
   - `Ask Customer` - Der Kunde kann entscheiden, ob er während des Express-Checkout-Flusses einen Abrechnungsvertrag unterzeichnet.
   - `Never` - Der Kunde kann während des Express-Checkout-Flusses keine Abrechnungsvereinbarung unterzeichnen.

   >[!NOTE]
   >
   >Händler müssen [PayPal Merchant Technical Support](https://developer.paypal.com/support/) bitten, Abrechnungsvereinbarungen in ihren Konten zu aktivieren. Der _Billing Agreement Signup_-Parameter wird erst aktiviert, nachdem PayPal bestätigt hat, dass die Billing Agreements für Ihr Händlerkonto aktiviert sind.

1. Damit der Kunde die Transaktion von der PayPal-Website abschließen kann, ohne zur Bestellüberprüfung an Ihren Store zurückzukehren, setzen Sie **[!UICONTROL Skip Order Review Step]** auf `Yes`.

1. Füllen Sie die zusätzlichen Abschnitte nach Bedarf für Ihren Store aus:

   - [PayPal-Rechnungsvereinbarungseinstellungen](#paypal-billing-agreement-settings)
   - [Einstellungen für Abrechnungsberichte](#settlement-report-settings)
   - [Frontend-Erlebniseinstellungen](#frontend-experience-settings)
   - [Anpassen von Smart-Schaltflächen](#customize-smart-buttons)
   - [Funktionen](#features)

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

#### PayPal-Rechnungsvereinbarungseinstellungen

Ein [Abrechnungsvertrag](paypal-billing-agreements.md) ist ein Kaufvertrag zwischen dem Händler und dem Kunden, der von PayPal zur Verwendung bei mehreren Bestellungen autorisiert wurde. Während des Checkout-Prozesses wird die Zahlungsoption „Abrechnungsvertrag“ nur für Kunden angezeigt, die bereits einen Abrechnungsvertrag mit Ihrem Unternehmen abgeschlossen haben. Nachdem PayPal den Vertrag genehmigt hat, gibt das Zahlungssystem eine eindeutige Referenz-ID aus, um jede Bestellung zu identifizieren, die mit dem Vertrag verbunden ist. Ähnlich wie bei einer Bestellung gibt es keine Begrenzung für die Anzahl der Abrechnungsvereinbarungen, die ein Kunde mit Ihrem Unternehmen abschließen kann.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL PayPal Billing Agreement Settings]** .

   ![Einstellungen für Abrechnungsvereinbarungen](../configuration-reference/sales/assets/payment-methods-paypal-express-checkout-billing-agreement-settings.png){width="600" zoomable="yes"}

1. Legen Sie **[!UICONTROL Enabled]** auf `Yes` fest.

1. Geben Sie **[!UICONTROL Title]** einen Titel ein, der die PayPal-Abrechnungsvereinbarungsmethode beim Checkout angibt.

1. Wenn Sie mehrere Zahlungsmethoden anbieten, geben Sie eine Zahl in das Feld &quot;**[!UICONTROL Sort Order]**&quot; ein, um die Reihenfolge zu bestimmen, in der der Abrechnungsvertrag angezeigt wird, wenn er beim Checkout mit anderen Zahlungsmethoden aufgelistet wird.

1. Legen Sie **[!UICONTROL Payment Action]** auf eine der folgenden Einstellungen fest:

   - `Authorization` - Genehmigt den Kauf und legt die Mittel fest. Der Betrag wird erst abgehoben, wenn er vom Händler „eingezogen“ wurde.
   - `Sale` - Der Betrag des Kaufs wird autorisiert und sofort vom Konto des Kunden zurückgezogen.

1. Legen Sie **[!UICONTROL Payment Applicable From]** auf eine der folgenden Einstellungen fest:

   - `All Allowed Countries` - Kunden aus allen Ländern, die in Ihrer Store-Konfiguration angegeben sind, können diese Zahlungsmethode verwenden.
   - `Specific Countries` - Nach Auswahl dieser Option wird die _[!UICONTROL Payment from Specific Countries]_&#x200B;angezeigt. Zur Auswahl mehrerer Länder halten Sie die Strg-Taste (PC) bzw. die Befehlstaste (Mac) gedrückt und klicken auf die einzelnen Länder.

1. Um die Kommunikation mit dem Zahlungssystem in der Protokolldatei aufzuzeichnen, setzen Sie **[!UICONTROL Debug Mode]** auf `Yes`.

   >[!NOTE]
   >
   >Die Protokolldatei wird auf dem Server gespeichert und steht nur Entwicklern zur Verfügung. In Übereinstimmung mit den PCI Data Security Standards werden Kreditkarteninformationen nicht in der Protokolldatei aufgezeichnet.

1. Um die SSL-Überprüfung zu aktivieren, setzen Sie **[!UICONTROL Enable SSL Verification]** auf `Yes`.

1. Um auf Ihrer PayPal-Zahlungsseite eine Zusammenfassung jedes Einzelpostens in der Bestellung des Kunden anzuzeigen, setzen Sie **[!UICONTROL Transfer Cart Line Items]** auf `Yes`.

1. Damit Kundinnen und Kunden über das Dashboard ihres Kundenkontos eine Abrechnungsvereinbarung initiieren können, setzen Sie **[!UICONTROL Allow in Billing Agreement Wizard]** auf `Yes`.

#### Einstellungen für Abrechnungsberichte

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Settlement Report Settings]** .

   ![Einstellungen für Abrechnungsberichte](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png){width="600" zoomable="yes"}

1. Gehen Sie **[!UICONTROL SFTP Credentials]** wie folgt vor:

   - Wenn Sie sich für den sicheren PayPal-FTP-Server angemeldet haben, geben Sie die folgenden SFTP-Anmeldedaten ein:

      - Login
      - Kennwort

   - Um Testberichte vor der Live _-Schaltung mit_ Express-Checkout auf Ihrer Site auszuführen, setzen Sie **[!UICONTROL Sandbox Mode]** auf `Yes`.

   - Geben Sie die **[!UICONTROL Custom Endpoint Hostname or IP Address]** ein.

     Standardmäßig lautet der Wert: `reports.paypal.com`

   - Geben Sie die **[!UICONTROL Custom Path]** ein, in der Berichte gespeichert werden.

     Standardmäßig lautet der Wert: `/ppreports/outgoing`

1. Um Berichte nach einem Zeitplan zu generieren, führen Sie die **[!UICONTROL Scheduled Fetching]** aus:

   - Legen Sie **[!UICONTROL Enable Automatic Fetching]** auf `Yes` fest.

   - Legen Sie **[!UICONTROL Schedule]** auf eine der folgenden Einstellungen fest:

      - `Daily`
      - `Every 3 Days`
      - `Every 7 Days`
      - `Every 10 Days`
      - `Every 14 Days`
      - `Every 30 Days`
      - `Every 40 Days`

     PayPal bewahrt jeden Bericht 45 Tage lang auf.

   - Legen Sie **[!UICONTROL Time of Day]** auf die Stunde, Minute und Sekunde fest, zu der die Berichte generiert werden sollen.

#### Frontend-Erlebniseinstellungen

Verwenden Sie die Frontend-Erlebniseinstellungen , um zu entscheiden, welche PayPal-Logos auf Ihrer Site angezeigt werden sollen, und um das Erscheinungsbild Ihrer PayPal-Händlerseiten anzupassen.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Frontend Experience Settings]** .

   ![Frontend-Erlebniseinstellungen](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings1.png){width="600" zoomable="yes"}

1. Wählen Sie die **[!UICONTROL PayPal Product Logo]** aus, die im PayPal-Block in Ihrem Geschäft angezeigt werden soll.

   Die PayPal-Logos sind in vier Stilen und zwei Größen erhältlich:

   - `No Logo`
   - `We Prefer PayPal (150 x 60 or 150 x 40)`
   - `Now Accepting PayPal (150 x 60 or 150 x 40)`
   - `Payments by PayPal (150 x 60 or 150 x 40)`
   - `Shop Now Using PayPal (150 x 60 or 150 x 40)`

1. Gehen Sie wie folgt vor, um das Erscheinungsbild Ihrer PayPal-Händlerseiten anzupassen:

   - Geben Sie den Namen der **[!UICONTROL Page Style]** ein, die Sie auf Ihre PayPal-Händlerseiten anwenden möchten:

      - `paypal` - Verwendet den PayPal-Seitenstil.
      - `primary` - Verwendet den Seitenstil, den Sie im Kontoprofil als _primären_ Stil identifiziert haben.
      - `your_custom_value` - Verwendet einen benutzerdefinierten Zahlungsseitenstil, der in Ihrem Kontoprofil angegeben ist.

   - Geben Sie **[!UICONTROL Header Image URL]** die URL des Bildes ein, das in der linken oberen Ecke der Zahlungsseite angezeigt werden soll. Die maximale Dateigröße beträgt 750 Pixel breit und 90 Pixel hoch.

     >[!NOTE]
     >
     >PayPal empfiehlt, dass sich das Bild auf einem sicheren (HTTPS-)Server befindet. Andernfalls kann ein Browser warnen, dass _die Seite sowohl sichere als auch nicht sichere Elemente enthält_.

   - Um die Farbe für Ihre Seiten festzulegen, geben Sie für jede der folgenden Aktionen den sechsstelligen Hexadezimalcode ohne `#` ein:

      - **[!UICONTROL Header Background Color]** - Hintergrundfarbe für die Kopfzeile der Kaufbestätigungsseite.
      - **[!UICONTROL Header Border Color]** - Farbe für Zwei-Pixel-Rahmen um die Kopfzeile.
      - **[!UICONTROL Page Background Color]** - Hintergrundfarbe für die Checkout-Seite und um die Kopfzeile und das Zahlungsformular.

#### Anpassen von Smart-Schaltflächen

Mit _Funktion „Smart Payment Buttons_ können Sie die PayPal-Schaltfläche anpassen, die auf den Seiten Checkout, Produktdetails, Warenkorb und Mini-Warenkorb angezeigt werden kann. Interne Untersuchungen von PayPal deuten darauf hin, dass die Standardoptionen gut erkennbar sind und zu höheren Kaufraten führen können, aber ihre Standardeinstellungen entsprechen möglicherweise nicht Ihrem Store-Stil. Sie können zwischen folgenden Optionen wählen:

- Größe, Farbe und Form der PayPal-Schaltfläche
- Der Text, der auf der PayPal-Schaltfläche angezeigt wird
- Das Layout, wenn mehrere Schaltflächen angezeigt werden (horizontal oder vertikal)

Um die Schaltflächen anzupassen, erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) jeden der folgenden Abschnitte und passen Sie die Einstellungen an:

- **[!UICONTROL Checkout Page]**
- **[!UICONTROL Product Pages]**
- **[!UICONTROL Cart Page]**
- **[!UICONTROL Mini Cart]**

![Einstellungen der Kaufbestätigungsseite](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings2.png){width="600" zoomable="yes"}

**_So konfigurieren Sie die Schaltflächenanzeige für jeden Seitentyp:_**

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt .

1. Legen Sie **[!UICONTROL Customize Button]** auf `Yes` fest.

1. Um den Text festzulegen, den PayPal auf der Schaltfläche „Smart Payment“ anzeigt, legen Sie **[!UICONTROL Label]** auf einen der folgenden Werte fest:

   - `Checkout` - PayPal-Kasse
   - `Pay` - PayPal-Kasse
   - `Buy Now` - Jetzt kaufen mit PayPal
   - `PayPal` - PayPal
   - `Installment` - PayPal
   - `Credit` - PayPal-Guthaben

1. Legen Sie **[!UICONTROL Layout]** auf eine der folgenden Einstellungen fest:

   - `Vertical` - (Standard) Zeigt PayPal Smart Buttons vertikal an. Der Käufer muss sich entweder bei PayPal anmelden oder ein PayPal-Konto erstellen, unabhängig davon, ob **[!UICONTROL Enable Guest Checkout]** ausgewählt ist.
   - `Horizontal` - Zeigt PayPal-Smart-Schaltflächen horizontal an. Wenn **[!UICONTROL Enable Guest Checkout]** ausgewählt ist, wird die Schaltfläche **[!UICONTROL Pay with Debit Card or Credit Card]** im Popup-Fenster von PayPal angezeigt. Andernfalls muss sich der Käufer entweder bei PayPal anmelden oder ein PayPal-Konto erstellen.

1. Legen Sie **[!UICONTROL Size]** auf eine der folgenden Einstellungen fest:

   - `Medium` - 250 x 35 Pixel.
   - `Large` - 350 x 40 Pixel.
   - `Responsive` - (Standard) Passt sich an die Breite des Containers an. Die Mindestbreite beträgt 100 Pixel, die maximale Breite 500 Pixel. Die Höhe wird basierend auf der Breite dynamisch angepasst.

1. Legen Sie **[!UICONTROL Shape]** auf eine der folgenden Einstellungen fest:

   - `Pill` - (Standard) Die Schaltfläche hat die Form einer Pille (lang in der Mitte und an den Enden gekrümmt).
   - `Rectangle` - Rechteckige Form, ohne Kurven.

1. Legen Sie **[!UICONTROL Color]** auf eine der folgenden Einstellungen fest:

   - `Gold` (Standard)
   - `Blue`
   - `Silver`
   - `Black`

#### Funktionen

Mit den Funktionseinstellungen können Sie bestimmte Funktionen im Zusammenhang mit dieser PayPal-Lösung deaktivieren.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Features]** .

   ![Einstellungen der Kaufbestätigungsseite](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings3.png){width="600" zoomable="yes"}

1. Legen Sie die **[!UICONTROL Disable Funding Options]** fest, um zu bestimmen, welche anderen PayPal-Finanzierungsoptionen auf der Seite _Checkout_ angezeigt werden.

   Die ausgewählten Optionen werden nicht auf der Seite _Checkout_ angezeigt. Nicht ausgewählte Optionen werden nur angezeigt, wenn PayPal die Store-Währung und den Käuferstandort unterstützt. Zu den Optionen gehören:

   - PayPal-Guthaben
   - Venmo
   - PayPal Guest Checkout Kreditkartensymbole
   - Elektronisches Lastschriftverfahren - Deutscher ELV
