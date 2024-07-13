---
title: PayPal Express Checkout
description: Erfahren Sie, wie Sie PayPal Express Checkout als Online-Zahlungslösung in Ihrem Geschäft einrichten.
exl-id: 0cd90306-cf47-4a5f-8994-6ae96904ae2f
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '3093'
ht-degree: 0%

---

# PayPal Express Checkout

Mit PayPal Express Checkout können Sie den Umsatz steigern, indem Sie Ihren Kunden die Möglichkeit geben, mit Kreditkarte oder aus der Sicherheit ihrer persönlichen PayPal-Konten zu bezahlen. Während des Checkouts wird der Kunde zur sicheren PayPal-Site weitergeleitet, um die Zahlungsinformationen auszufüllen. Der Kunde wird dann an Ihren Store zurückgegeben, um den Rest des Checkout-Prozesses abzuschließen. Durch die Auswahl von Express Checkout wird die bekannte PayPal-Schaltfläche zu Ihrem Geschäft hinzugefügt, die laut Berichten den Umsatz steigert.

>[!IMPORTANT]
>
>**Anforderungen an PSD2:** <br/>
>Ab dem 14. September 2019 könnten europäische Banken Zahlungen ablehnen, die nicht den Anforderungen von [PSD2](../getting-started/compliance-payment-services-directive.md) entsprechen. Für PayPal Express Checkout ist kein Eingreifen erforderlich, um PSD 2 zu erfüllen, da alle Anforderungen von PayPal erfüllt werden.

Kunden mit aktuellen PayPal-Konten können in einem Schritt einen Kauf tätigen, indem Sie auf die Schaltfläche _[!UICONTROL Check out with PayPal]_klicken. Express Checkout kann als eigenständige Lösung oder mit einer der PayPal All-in-One-Lösungen verwendet werden. Wenn Sie bereits Kreditkarten online akzeptieren, können Sie Express Checkout als zusätzliche Option anbieten, um neue Kunden zu gewinnen, die lieber mit PayPal zahlen.

>[!NOTE]
>
>PayPal unterstützt nicht mehr den Verkauf digitaler Waren über PayPal Express Checkout und empfiehlt, entweder [PayPal Payments Standard](paypal-payments-standard.md) oder ein anderes PayPal Payment Gateway zu verwenden, um alle Bestellungen zu verarbeiten, die [virtuelle Produkte](../catalog/product-create-virtual.md) enthalten.

## Voraussetzungen

- Händler: [PayPal-Konto für Unternehmen][1]
- Kunde: [Persönliches PayPal-Konto][2]

## Express-Checkout-Workflow

Im Gegensatz zu anderen Zahlungsmethoden ermöglicht PayPal Express Checkout dem Kunden, zu Beginn des üblichen Checkout-Workflows von der Produktseite, dem Mini-Warenkorb und dem Warenkorb aus auszuchecken.

1. **Kunde legt Bestellung auf** - Der Kunde klickt/tippt auf die Schaltfläche _[!UICONTROL Check out with PayPal]_.
1. **Der Kunde wird zur PayPal-Site weitergeleitet** - Der Kunde wird zur PayPal-Site weitergeleitet, um die Transaktion abzuschließen.
1. **Der Kunde meldet sich bei seinem PayPal-Konto an** - Der Kunde muss sich bei seinem PayPal-Konto anmelden, um die Transaktion abzuschließen. Das Zahlungssystem verwendet die Abrechnungs- und Versandinformationen von seinem PayPal-Konto.
1. **Der Kunde kehrt zur Checkout-Seite zurück** - Der Kunde wird zur Checkout-Seite in Ihrem Store zurückgeleitet, um die Bestellung zu überprüfen.
1. **Kunde stellt Bestellung auf** - Der Kunde gibt die Bestellung auf und die Bestellinformationen werden an PayPal übermittelt.
1. **PayPal regelt die Transaktion** - PayPal erhält die Bestellung und verrechnet die Transaktion.

>[!NOTE]
>
>PayPal Express Checkout unterstützt keine Bestellungen mit mehreren Adressen.

## Im Kontext Auschecken

PayPals _In-Context Checkout_ erleichtert die Online-Bezahlung. Kunden verlieren nie den Überblick über Ihren Store, während dieses vereinfachten Ein- oder Zweiklick-nahtlosen Checkout stattfindet. Der kontextbezogene Checkout funktioniert auf Macs und PCs gleichermaßen gut und bietet ein konsistentes Erlebnis auf Desktop-Computern, Tablets und Mobilgeräten. Weitere Informationen finden Sie unter [In-Context Checkout in Express Checkout][5].

![PayPal im Kontext Checkout-Demo](./assets/storefront-paypal-in-context.png){width="700" zoomable="yes"}

[_PayPal im Kontext Checkout-Demo_][6]

Wenn Sie Ihren Store für [!DNL PayPal Express Checkout] konfigurieren, können Sie diese Option aktivieren.

## PayPal-Konto konfigurieren

Bevor Sie PayPal Express Checkout im Commerce Admin einrichten, müssen Sie Ihr Händlerkonto auf der PayPal-Website konfigurieren.

1. Melden Sie sich bei Ihrem PayPal Advanced-Konto unter [manager.paypal.com][3] an.

1. Gehen Sie zu **[!UICONTROL Service Settings]** > **[!UICONTROL Hosted Checkout Pages]** > **[!UICONTROL Set Up]** und nehmen Sie die folgenden Einstellungen vor:

   - **[!UICONTROL AVS]**: `No`
   - **[!UICONTROL CSC]**: `No`
   - **[!UICONTROL Enable Secure Token]**: `Yes`

1. Klicken Sie auf **[!UICONTROL Save Changes]**.

1. Richten Sie einen anderen Benutzer ein (von PayPal empfohlen):

   - Gehen Sie zu [manager.paypal.com][3] und melden Sie sich bei Ihrem Konto an.

   - Um einen anderen Benutzer einzurichten, befolgen Sie die Anweisungen.

   - Klicken Sie auf **[!UICONTROL Update]**.

## PayPal Express-Checkout in Commerce einrichten

Sie können zwei PayPal-Lösungen gleichzeitig verwenden: PayPal Express Checkout und eine All-in-One-Lösung. Wenn Sie eine andere Lösung aktivieren, wird die zuvor verwendete automatisch deaktiviert.

>[!NOTE]
>
>Klicken Sie jederzeit auf **[!UICONTROL Save Config]** , um Ihren Fortschritt zu speichern.

### Schritt 1: Konfiguration beginnen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Payment Methods]** aus.

1. Wenn Ihre Installation über mehrere Websites, Stores oder Ansichten verfügt, setzen Sie **[!UICONTROL Store View]** auf die Store-Ansicht, auf die Sie diese Konfiguration anwenden möchten.

1. Wählen Sie im Abschnitt _[!UICONTROL Merchant Location]_die **[!UICONTROL Merchant Country]**aus, in der sich Ihr Unternehmen befindet.

   Diese Einstellung bestimmt die Auswahl der PayPal-Lösungen, die in der Konfiguration angezeigt werden.

   ![Handelsland](../configuration-reference/sales/assets/payment-methods-merchant-location.png){width="600" zoomable="yes"}

1. Klicken Sie unter _[!UICONTROL Recommended Solutions]_auf **[!UICONTROL Configure]**für **[!UICONTROL PayPal Express Checkout]**.

   ![PayPal Express-Checkout konfigurieren](./assets/paypal-express-checkout.png){width="600"}

### Schritt 2: Aktivieren und Verbinden Ihres PayPal-Kontos

1. Erweitern Sie bei Bedarf den Abschnitt ![Erweiterungsselektor](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Required PayPal Settings]** .

   ![Verbinden Sie Ihr PayPal-Konto](./assets/paypal-express-required.png){width="600" zoomable="yes"}

1. Verbinden Sie Ihr Konto für Test oder Produktion:

   - Klicken Sie zum Testen des (Entwicklungs-)Modus auf **[!UICONTROL Sandbox Credentials]** und geben Sie Ihre [PayPal-Sandbox][7]-Anmeldeinformationen ein.
   - Klicken Sie im Produktionsmodus auf **[!UICONTROL Connect with PayPal]** und geben Sie die Anmeldeinformationen Ihres Produktionskontos ein.

   Wenn Ihre Verbindung validiert wurde, können Sie fortfahren.

1. Setzen Sie **[!UICONTROL Enable this Solution]** auf `Yes`.

1. So aktivieren Sie [PayPal InContext Checkout](#in-context-checkout):

   - Setzen Sie **[!UICONTROL Enable In-Context Checkout Experience]** auf `Yes`.

   - Geben Sie Ihren PayPal **[!UICONTROL Merchant Account ID]** ein.

     Ihre Merchant-Konto-ID befindet sich in Ihrem PayPal-Geschäftskontoprofil.

>[!NOTE]
>
>[PayPal Credit](paypal.md#paypal-credit-and-pay-later) ist für diese Zahlungsoption standardmäßig aktiviert.

### Schritt 3: Abschließen der erforderlichen PayPal-Einstellungen

1. Erweitern Sie bei Bedarf den Abschnitt ![Erweiterungsselektor](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Express Checkout]** .

   ![PayPal Express Checkout - erforderliche Einstellungen](./assets/paypal-express-settings.png){width="600" zoomable="yes"}

1. (Optional) Geben Sie den Wert **[!UICONTROL Email Associated with PayPal Merchant Account]** ein.

   >[!IMPORTANT]
   >
   >Bei E-Mail-Adressen wird zwischen Groß- und Kleinschreibung unterschieden. Um eine Zahlung zu erhalten, muss die von Ihnen eingegebene E-Mail-Adresse mit der in Ihrem PayPal-Handelskonto angegebenen E-Mail-Adresse übereinstimmen.

   Wenn Sie kein PayPal-Konto haben, klicken Sie auf **[!UICONTROL Start accepting payments via PayPal]**.

1. Setzen Sie **[!UICONTROL API Authentication Methods]** auf einen der folgenden Werte:

   - `API Signature` - Diese PayPal-Authentifizierungsmethode ist am einfachsten zu implementieren und basiert auf Ihrem Benutzernamen, Kennwort und einer eindeutigen Zeichenfolge aus Zeichen und Zahlen, die Ihr Konto identifiziert. API-Signaturberechtigungen laufen nicht ab.
   - `API Certificate` - Diese PayPal-Authentifizierungsmethode ist sicherer und basiert auf Ihrem Benutzernamen, Kennwort und einem herunterladbaren Zertifikat. API-Anmeldeinformationen laufen nach drei Jahren ab und müssen verlängert werden.

   Führen Sie bei Bedarf Folgendes aus:

   - **[!UICONTROL API Username]**
   - **[!UICONTROL API Password]**
   - **[!UICONTROL API Signature]**

1. Wenn Sie Anmeldeinformationen aus Ihrem Sandbox-Konto verwenden, setzen Sie **[!UICONTROL Sandbox Mode]** auf `Yes`.

   Verwenden Sie beim Testen der Konfiguration in einer Sandbox nur die von PayPal empfohlenen [Kreditkartennummern][4]. Wenn Sie bereit sind, zur Produktion zu wechseln, kehren Sie zur Konfiguration zurück, setzen Sie den Sandbox-Modus auf &quot;`No`&quot;und stellen Sie eine Verbindung zu Ihrem PayPal-Produktionskonto her.

1. Wenn Ihr System einen Proxy-Server verwendet, um die Verbindung zwischen Commerce und dem PayPal-Zahlungssystem herzustellen, setzen Sie **[!UICONTROL API Uses Proxy]** auf `Yes` und führen Sie Folgendes aus:

   - **[!UICONTROL Proxy Host]**
   - **[!UICONTROL Proxy Port]**

Am Ende dieser Schrittfolge sind die erforderlichen PayPal-Einstellungen abgeschlossen. Sie können mit den grundlegenden und erweiterten Einstellungen fortfahren oder auf **[!UICONTROL Save Config]** klicken und später zur Anpassung der Konfiguration zurückkehren

### Schritt 4: Einrichten von Advertise PayPal Credit / Advertise PayPal PayLater (optional)

Ab Version 2.4.3 wird PayPal PayLater in Implementierungen unterstützt, die PayPal enthalten. Diese Funktion ermöglicht es den Käufern, eine Bestellung in zweiwöchigen Tranchen zu bezahlen, anstatt den vollen Betrag zum Zeitpunkt des Kaufs zu zahlen. Das PayPal-Krediterlebnis wird nicht mehr unterstützt.

Setzen Sie **[!UICONTROL Enable PayPal PayLater Experience]** auf einen der folgenden Werte:

- `Yes` - So richten Sie Advertise PayPal PayLater ein
- `No` - So richten Sie Advertising PayPal-Guthaben ein

>[!NOTE]
>
>Die Einstellung **[!UICONTROL Enable PayPal PayLater Experience]** deaktiviert die Funktion [!DNL PayPal PayLater] nicht und entfernt die Schaltflächen **_[!UICONTROL PayPal PayLater]_** nicht aus der Storefront. Um sowohl die Tasten **_[!UICONTROL PayPal PayLater]_** als auch **_[!UICONTROL PayPal Credit]_** auf der Storefront zu deaktivieren, müssen Sie den Wert `PayPal Credit` für die Einstellung **[!UICONTROL Disable Funding Options]** ([!UICONTROL Advanced Settings] unter [!UICONTROL Frontend Experience Settings]) auswählen.

#### Advertise PayPal Credit

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Advertise PayPal Credit]** .

1. Um Ihre Kontoinformationen zu erhalten, klicken Sie auf **[!UICONTROL Get Publisher ID from PayPal]** und befolgen Sie die Anweisungen.

1. Geben Sie Ihren **[!UICONTROL Publisher ID]** ein.

   ![PayPal-Guthaben für Werbung](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png){width="600" zoomable="yes"}

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Home Page]** .

1. Um ein Banner auf der Seite zu platzieren, setzen Sie **[!UICONTROL Display]** auf `Yes`.

1. Setzen Sie **[!UICONTROL Position]** auf einen der folgenden Werte:

   - `Header (center)`
   - `Sidebar (right)`

1. Setzen Sie **[!UICONTROL Size]** auf einen der folgenden Werte:

   - `190 x 100`
   - `234 x 60`
   - `300 x 50`
   - `468 x 60`
   - `728 x 90`
   - `800 x 66`

   ![Einstellungen der Advertise PayPal Credit-Startseite ](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit-home-page.png){width="600" zoomable="yes"}

1. Erweitern Sie ![Erweiterungsselektor](../assets/icon-display-expand.png) die verbleibenden Abschnitte und wiederholen Sie die vorherigen Schritte:

   - [!UICONTROL Catalog Category Page]
   - [!UICONTROL Catalog Product Page]
   - [!UICONTROL Checkout Cart Page]

#### Advertise PayPal PayLater

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Advertise PayPal PayLater]** .

1. Setzen Sie **[!UICONTROL Enable PayPal PayLater]** auf `Yes`.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Home Page]** .

1. Um ein Banner auf der Seite zu platzieren, setzen Sie **[!UICONTROL Display]** auf `Yes`.

1. Setzen Sie **[!UICONTROL Position]** auf einen der folgenden Werte:

   - `Header (center)`
   - `Sidebar`

1. Setzen Sie **[!UICONTROL Style Layout]** auf einen der folgenden Werte:

   - `Text`
   - `Flex`

1. Setzen Sie **[!UICONTROL Logo Type]** nur für [!UICONTROL Style Layout] **[!UICONTROL Text]** auf einen der folgenden Werte:

   - `Primary`
   - `Alternative`
   - `Inline`
   - `None`

1. Setzen Sie **[!UICONTROL Logo Position]** nur für [!UICONTROL Style Layout] **[!UICONTROL Text]** auf einen der folgenden Werte:

   - `Left`
   - `Right`
   - `Top`

1. Setzen Sie **[!UICONTROL Text Color]** nur für [!UICONTROL Style Layout] **[!UICONTROL Text]** auf einen der folgenden Werte:

   - `Black`
   - `White`
   - `Monochrome`
   - `Grayscale`

1. Setzen Sie **[!UICONTROL Text Size]** nur für [!UICONTROL Style Layout] **[!UICONTROL Text]** auf einen der folgenden Werte:

   - `10px`
   - `11px`
   - `12px`
   - `13px`
   - `14px`
   - `15px`
   - `16px`

1. Setzen Sie **[!UICONTROL Ratio]** nur für [!UICONTROL Style Layout] **[!UICONTROL Flex]** auf einen der folgenden Werte:

   - `1x1`
   - `1x4`
   - `8x1`
   - `20x1`

1. Setzen Sie **[!UICONTROL Color]** nur für [!UICONTROL Style Layout] **[!UICONTROL Flex]** auf einen der folgenden Werte:

   - `Blue`
   - `Black`
   - `White`
   - `White No Border`
   - `Gray`
   - `Monochrome`
   - `Grayscale`

   ![Einstellungen der Advertise PayPal Credit-Startseite ](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-paylater-home-page.png){width="600" zoomable="yes"}

1. Erweitern Sie ![Erweiterungsselektor](../assets/icon-display-expand.png) die verbleibenden Abschnitte und wiederholen Sie die vorherigen Schritte:

   - [!UICONTROL Catalog Product Page]
   - [!UICONTROL Checkout Cart Page]
   - [!UICONTROL Checkout Payment Step]
   - [!UICONTROL Catalog Category Page]

### Schritt 5: Grundlegende Einstellungen durchführen

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Basic Settings - PayPal Express Checkout]** .

   ![Grundlegende Einstellungen](../configuration-reference/sales/assets/payment-methods-paypal-express-checkout-basic-settings.png){width="600" zoomable="yes"}

1. Geben Sie für **[!UICONTROL Title]** einen Titel ein, der diese Zahlungsmethode beim Checkout angibt.

   Es wird empfohlen, den Titel _PayPal_ für alle Store-Ansichten zu verwenden.

1. Wenn Sie mehrere Zahlungsmethoden anbieten, geben Sie eine Nummer für **[!UICONTROL Sort Order]** ein, um die Reihenfolge zu bestimmen, in der PayPal Express Checkout erscheint, wenn es mit den anderen Zahlungsmethoden aufgeführt wird.

   Diese Zahl ist relativ zu den anderen Zahlungsmethoden. (`0` = first, `1` = second, `2` = third usw.)

1. Setzen Sie **[!UICONTROL Payment Action]** auf einen der folgenden Werte:

   - `Authorization` - Genehmigt den Kauf und legt einen Besitz an den Fonds fest. Der Betrag wird erst zurückgezogen, wenn er vom Händler _erfasst_ wurde.
   - `Sale` - Der Betrag des Kaufs wird genehmigt und sofort vom Konto des Kunden zurückgezogen.
   - `Order` - Der Betrag der Bestellung wird nicht im Kundenkonto, Bankkonto oder Kreditkarte bei PayPal erfasst oder autorisiert. Die Bestellzahlung stellt eine Vereinbarung zwischen dem Zahlungssystem PayPal und dem Händler dar. Sie ermöglicht es dem Händler, einen oder mehrere Beträge bis zum bestellten Gesamtbetrag vom Kunden-Käuferkonto über einen Zeitraum von bis zu 29 Tagen zu erfassen. Nachdem die Mittel bestellt wurden, kann der Händler sie jederzeit während der folgenden 29-Tage-Periode erfassen. Die Erfassung des Bestellbetrags kann nur vom Commerce-Administrator durch die Erstellung einer oder mehrerer Rechnungen erfolgen.

1. Um die Schaltfläche _[!UICONTROL Check out with PayPal]_auf der Produktseite anzuzeigen, setzen Sie **[!UICONTROL Display on Product Details Page]**auf `Yes`.

1. Wenn die Zahlungsaktion auf `Order` festgelegt ist, führen Sie Folgendes aus

   - **[!UICONTROL Authorization Honor Period (days)]** - Bestimmt, wie lange die primäre Autorisierung gültig bleibt. Der Wert sollte dem entsprechenden Wert in Ihrem PayPal-Handelskonto entsprechen. Der Standardwert in Ihrem PayPal-Handelskonto ist `3`. Um diese Zahl zu erhöhen, müssen Sie sich an PayPal wenden. Die Autorisierung wird am letzten Tag um 23:49 Uhr US Pacific Time ungültig.

   - **[!UICONTROL Order Valid Period (days)]** - Bestimmt, wie lange die Bestellung gültig bleibt. Wenn die Bestellung ungültig wird, können Sie keine Rechnungen mehr dafür erstellen. Geben Sie in Ihrem PayPal-Handelskonto den Wert für den gültigen Bestellzeitraum an. Der Standardwert in Ihrem PayPal-Handelskonto ist `29`. Um diese Nummer zu ändern, müssen Sie sich an PayPal wenden.

   - **[!UICONTROL Number of Child Authorizations]** - Gibt die maximale Anzahl von Berechtigungen für eine einzelne Bestellung an, die die maximale Anzahl von Online-Teilrechnungen bestimmt, die Sie für eine Bestellung erstellen können. Dieser Wert sollte der entsprechenden Einstellung in Ihrem PayPal-Kaufkonto entsprechen. Die Standardanzahl der untergeordneten Berechtigungen in Ihrem PayPal-Konto ist `1`. Um diese Zahl zu erhöhen, müssen Sie sich an PayPal wenden.

### Schritt 6: Erweiterte Einstellungen durchführen

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Advanced Settings]** .

   ![Erweiterte Einstellungen - PayPal Express Checkout](../configuration-reference/sales/assets/payment-methods-paypal-express-checkout-advanced-settings.png){width="600" zoomable="yes"}

1. Setzen Sie **[!UICONTROL Display on Shopping Cart]** auf `Yes`.

1. Setzen Sie **[!UICONTROL Payment Applicable From]** auf einen der folgenden Werte:

   - `All Allowed Countries` - Kunden aus allen in Ihrer Store-Konfiguration angegebenen Ländern können diese Zahlungsmethode verwenden.
   - `Specific Countries` - Nach Auswahl dieser Option wird die Liste _[!UICONTROL Payment from Specific Countries]_angezeigt. Um mehrere Länder auszuwählen, halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie auf jedes Element.

1. Um Nachrichten mit dem Zahlungssystem in die Protokolldatei zu schreiben, setzen Sie **[!UICONTROL Debug Mode]** auf `Yes`.

   Die Protokolldatei für PayPal Payments Advanced ist `_payflow_advanced.log`.

   >[!NOTE]
   >
   >Gemäß PCI Data Security Standards werden Kreditkarteninformationen nicht in der Protokolldatei aufgezeichnet.

1. Um die Authentifizierungsüberprüfung des Hosts zu aktivieren, setzen Sie **[!UICONTROL Enable SSL Verification]** auf `Yes`.

1. Um eine vollständige Zusammenfassung der Kundenbestellung nach Zeileneintrag von der PayPal-Site aus anzuzeigen, setzen Sie **[!UICONTROL Transfer Cart Line Items]** auf `Yes`.

1. Um bis zu zehn Versandoptionen in die Zusammenfassung aufzunehmen, setzen Sie **[!UICONTROL Transfer Shipping Options]** auf `Yes`. (Diese Option wird nur angezeigt, wenn Zeileneinträge für die Übertragung festgelegt sind.)

1. Um den Bildtyp für die PayPal-Akzeptanzschaltfläche zu bestimmen, setzen Sie **[!UICONTROL Shortcut Buttons Flavor]** auf einen der folgenden Werte:

   - `Dynamic` - (Empfohlen) Zeigt ein Bild an, das dynamisch vom PayPal-Server aus geändert werden kann.
   - `Static` - Zeigt ein bestimmtes Bild an, das nicht dynamisch geändert werden kann.

1. Damit Kunden ohne PayPal-Konten mit dieser Methode einen Kauf tätigen können, setzen Sie **[!UICONTROL Enable PayPal Guest Checkout]** auf `Yes`.

1. Setzen Sie **[!UICONTROL Require Customer's Billing Address]** auf einen der folgenden Werte:

   - `Yes` - Erfordert die Rechnungsadresse des Kunden für alle Käufe.
   - `No` - Für Käufe ist die Rechnungsadresse des Kunden nicht erforderlich.
   - `For Virtual Quotes Only` - Erfordert nur die Rechnungsadresse des Kunden für virtuelle Anführungszeichen.

   >[!NOTE]
   >
   >Diese Funktion muss über den technischen Support von PayPal für das Handelskonto aktiviert werden.

1. (Optional) Legen Sie den **[!UICONTROL Billing Agreement Signup]** fest, damit Kunden mit Ihrem Store im PayPal-Zahlungssystem eine [Abrechnungsvereinbarung](paypal-billing-agreements.md) unterzeichnen können, wenn im Kundenkonto keine aktiven Abrechnungsvereinbarungen verfügbar sind:

   - `Auto` - Der Kunde kann entweder während des Express-Checkout-Flusses einen Abrechnungsvertrag unterzeichnen oder eine andere Zahlungsmethode verwenden.
   - `Ask Customer` - Der Kunde kann entscheiden, ob er während des Express Checkout-Flusses eine Abrechnungsvereinbarung unterzeichnet.
   - `Never` - Der Kunde kann während des Express-Checkout-Flusses keine Abrechnungsvereinbarung unterzeichnen.

   >[!NOTE]
   >
   >Händler müssen den technischen Support von [PayPal Merchant ](https://developer.paypal.com/support/) bitten, Abrechnungsvereinbarungen in ihren Konten zu aktivieren. Der Parameter _Abrechnungsvereinbarung unterschreiben_ wird erst aktiviert, nachdem PayPal bestätigt hat, dass Abrechnungsvereinbarungen für Ihr Händlerkonto aktiviert sind.

1. Damit der Kunde die Transaktion von der PayPal-Site ausführen kann, ohne zur Überprüfung der Bestellung zu Ihrem Store zurückzukehren, setzen Sie **[!UICONTROL Skip Order Review Step]** auf `Yes`.

1. Füllen Sie die zusätzlichen Abschnitte nach Bedarf für Ihren Store aus:

   - [Einstellungen der PayPall-Abrechnungsvereinbarung](#paypal-billing-agreement-settings)
   - [Berichtseinstellungen einrichten](#settlement-report-settings)
   - [Frontend-Erlebniseinstellungen](#frontend-experience-settings)
   - [Anpassen von Smart-Schaltflächen](#customize-smart-buttons)
   - [Funktionen](#features)

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

#### Einstellungen der PayPal-Abrechnungsvereinbarung

Ein [Abrechnungsvertrag](paypal-billing-agreements.md) ist ein Kaufvertrag zwischen dem Händler und dem Kunden, der von PayPal zur Verwendung mit mehreren Bestellungen genehmigt wurde. Während des Checkout-Prozesses wird die Zahlungsoption für die Abrechnungsvereinbarung nur für Kunden angezeigt, die bereits einen Abrechnungsvertrag mit Ihrem Unternehmen geschlossen haben. Nachdem PayPal die Vereinbarung genehmigt hat, gibt das Zahlungssystem eine eindeutige Referenz-ID aus, um jede Bestellung zu identifizieren, die der Vereinbarung zugeordnet ist. Ähnlich wie bei einer Bestellung gibt es keine Begrenzung für die Anzahl der Abrechnungsvereinbarungen, die ein Kunde mit Ihrem Unternehmen schließen kann.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL PayPal Billing Agreement Settings]** .

   ![Rechnungsvertragseinstellungen](../configuration-reference/sales/assets/payment-methods-paypal-express-checkout-billing-agreement-settings.png){width="600" zoomable="yes"}

1. Setzen Sie **[!UICONTROL Enabled]** auf `Yes`.

1. Geben Sie für &quot;**[!UICONTROL Title]**&quot;einen Titel ein, der die Methode der PayPal-Abrechnungsvereinbarung während des Checkouts identifiziert.

1. Wenn Sie mehrere Zahlungsmethoden anbieten, geben Sie im Feld **[!UICONTROL Sort Order]** eine Zahl ein, um die Reihenfolge zu bestimmen, in der die Abrechnungsvereinbarung erscheint, wenn sie beim Checkout mit anderen Zahlungsmethoden aufgeführt wird.

1. Setzen Sie **[!UICONTROL Payment Action]** auf einen der folgenden Werte:

   - `Authorization` - Genehmigt den Kauf und legt einen Besitz an den Fonds fest. Der Betrag wird erst dann zurückgezogen, wenn er vom Händler &quot;erfasst&quot;wurde.
   - `Sale` - Der Betrag des Kaufs wird genehmigt und sofort vom Konto des Kunden zurückgezogen.

1. Setzen Sie **[!UICONTROL Payment Applicable From]** auf einen der folgenden Werte:

   - `All Allowed Countries` - Kunden aus allen in Ihrer Store-Konfiguration angegebenen Ländern können diese Zahlungsmethode verwenden.
   - `Specific Countries` - Nach Auswahl dieser Option wird die Liste _[!UICONTROL Payment from Specific Countries]_angezeigt. Um mehrere Länder auszuwählen, halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie auf jedes Land.

1. Um die Kommunikation mit dem Zahlungssystem in der Protokolldatei aufzuzeichnen, setzen Sie **[!UICONTROL Debug Mode]** auf `Yes`.

   >[!NOTE]
   >
   >Die Protokolldatei wird auf dem Server gespeichert und steht nur Entwicklern zur Verfügung. Gemäß PCI Data Security Standards werden Kreditkarteninformationen nicht in der Protokolldatei aufgezeichnet.

1. Um die SSL-Verifizierung zu aktivieren, setzen Sie **[!UICONTROL Enable SSL Verification]** auf `Yes`.

1. Um eine Zusammenfassung jedes Zeileneintrags in der Bestellung des Kunden auf Ihrer PayPal-Zahlungsseite anzuzeigen, setzen Sie **[!UICONTROL Transfer Cart Line Items]** auf `Yes`.

1. Damit Kunden eine Abrechnungsvereinbarung über das Dashboard ihres Kundenkontos initiieren können, setzen Sie **[!UICONTROL Allow in Billing Agreement Wizard]** auf `Yes`.

#### Berichtseinstellungen einrichten

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Settlement Report Settings]** .

   ![Berichtseinstellungen festlegen](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png){width="600" zoomable="yes"}

1. Gehen Sie für **[!UICONTROL SFTP Credentials]** wie folgt vor:

   - Wenn Sie sich für den PayPal Secure FTP Server angemeldet haben, geben Sie die folgenden SFTP-Anmeldedaten ein:

      - Anmelden
      - Kennwort

   - Um Testberichte auszuführen, bevor _live geschaltet wird_, mit Express Checkout auf Ihrer Site, setzen Sie **[!UICONTROL Sandbox Mode]** auf `Yes`.

   - Geben Sie den Wert **[!UICONTROL Custom Endpoint Hostname or IP Address]** ein.

     Standardmäßig lautet der Wert: `reports.paypal.com`

   - Geben Sie den **[!UICONTROL Custom Path]** ein, in dem Berichte gespeichert werden.

     Standardmäßig lautet der Wert: `/ppreports/outgoing`

1. Um Berichte planmäßig zu erstellen, führen Sie die Einstellungen für **[!UICONTROL Scheduled Fetching]** aus:

   - Setzen Sie **[!UICONTROL Enable Automatic Fetching]** auf `Yes`.

   - Setzen Sie **[!UICONTROL Schedule]** auf einen der folgenden Werte:

      - `Daily`
      - `Every 3 Days`
      - `Every 7 Days`
      - `Every 10 Days`
      - `Every 14 Days`
      - `Every 30 Days`
      - `Every 40 Days`

     PayPal behält jeden Bericht für 45 Tage bei.

   - Stellen Sie **[!UICONTROL Time of Day]** auf die Stunde, Minute und Sekunde ein, wenn die Berichte generiert werden sollen.

#### Frontend-Erlebniseinstellungen

Verwenden Sie die Frontend-Erlebniseinstellungen, um festzulegen, welche PayPal-Logos auf Ihrer Site erscheinen, und um das Erscheinungsbild Ihrer PayPal-Kaufseiten anzupassen.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Frontend Experience Settings]** .

   ![Frontend-Erlebniseinstellungen](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings1.png){width="600" zoomable="yes"}

1. Wählen Sie den **[!UICONTROL PayPal Product Logo]** aus, der im Block PayPal in Ihrem Geschäft angezeigt werden soll.

   Die PayPal Logos sind in vier Formaten und in zwei Größen erhältlich:

   - `No Logo`
   - `We Prefer PayPal (150 x 60 or 150 x 40)`
   - `Now Accepting PayPal (150 x 60 or 150 x 40)`
   - `Payments by PayPal (150 x 60 or 150 x 40)`
   - `Shop Now Using PayPal (150 x 60 or 150 x 40)`

1. Gehen Sie wie folgt vor, um das Erscheinungsbild Ihrer PayPal-Kaufseiten anzupassen:

   - Geben Sie den Namen des **[!UICONTROL Page Style]** ein, den Sie auf Ihre PayPal-Händlergeseiten anwenden möchten:

      - `paypal` - Verwendet den PayPal-Seitenstil.
      - `primary` - Verwendet den Seitenstil, den Sie in Ihrem Kontoprofil als _primär_ -Stil identifiziert haben.
      - `your_custom_value` - Verwendet einen benutzerdefinierten Zahlungsseitenstil, der in Ihrem Kontoprofil angegeben ist.

   - Geben Sie für &quot;**[!UICONTROL Header Image URL]**&quot;die URL des Bildes ein, das oben links auf der Zahlungsseite angezeigt werden soll. Die maximale Dateigröße ist 750 Pixel breit und 90 Pixel hoch.

     >[!NOTE]
     >
     >PayPal empfiehlt, dass sich das Bild auf einem sicheren (HTTPS-)Server befindet. Andernfalls kann ein Browser warnen, dass _die Seite sowohl sichere als auch nicht sichere Elemente enthält_.

   - Um die Farbe für Ihre Seiten festzulegen, geben Sie den sechsstelligen Hexadezimalcode ohne das `#` -Symbol für jeden der folgenden Elemente ein:

      - **[!UICONTROL Header Background Color]** - Hintergrundfarbe für die Kopfzeile der Checkout-Seite.
      - **[!UICONTROL Header Border Color]** - Farbe für einen Rahmen von zwei Pixeln um die Kopfzeile.
      - **[!UICONTROL Page Background Color]** - Hintergrundfarbe für die Checkout-Seite und um die Kopfzeile und das Zahlungsformular.

#### Anpassen von Smart-Schaltflächen

Mit der Funktion _Smart Payment Buttons_ können Sie die Schaltfläche PayPal anpassen, die auf den Seiten Checkout, Produktdetails, Warenkorb und Mini-Warenkorb angezeigt werden kann. Die interne Untersuchung von PayPal legt nahe, dass die Standardoptionen hochgradig erkennbar sind und zu höheren Kaufraten führen können, aber ihre Standardeinstellungen stimmen möglicherweise nicht mit Ihrem Store-Stil überein. Sie können Folgendes auswählen:

- Größe, Farbe und Form der Schaltfläche &quot;PayPal&quot;
- Der Text, der auf der Schaltfläche &quot;PayPal&quot;angezeigt wird
- Layout, wenn mehrere Schaltflächen angezeigt werden (horizontal oder vertikal)

Um Schaltflächen anzupassen, erweitern Sie den ![Erweiterungsselektor](../assets/icon-display-expand.png) für jeden der folgenden Abschnitte und passen Sie die Einstellungen an:

- **[!UICONTROL Checkout Page]**
- **[!UICONTROL Product Pages]**
- **[!UICONTROL Cart Page]**
- **[!UICONTROL Mini Cart]**

![Einstellungen der Checkout-Seite](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings2.png){width="600" zoomable="yes"}

**_So konfigurieren Sie die Schaltflächenanzeige für jeden Seitentyp:_**

1. Erweitern Sie den Abschnitt ![Erweiterungsselektor](../assets/icon-display-expand.png).

1. Setzen Sie **[!UICONTROL Customize Button]** auf `Yes`.

1. Um den Text festzulegen, den PayPal auf der Schaltfläche &quot;Smart Payment&quot;anzeigt, setzen Sie **[!UICONTROL Label]** auf einen der folgenden Werte:

   - `Checkout` - PayPal Checkout
   - `Pay` - PayPal Checkout
   - `Buy Now` - Jetzt mit PayPal kaufen
   - `PayPal` - PayPal
   - `Installment` - PayPal
   - `Credit` - PayPal-Guthaben

1. Setzen Sie **[!UICONTROL Layout]** auf einen der folgenden Werte:

   - `Vertical` - (Standard) Zeigt die PayPal-Smart-Schaltflächen vertikal an. Der Käufer muss sich entweder bei PayPal anmelden oder ein PayPal-Konto erstellen, unabhängig davon, ob **[!UICONTROL Enable Guest Checkout]** ausgewählt ist.
   - `Horizontal` - Zeigt die PayPal-Smart-Schaltflächen horizontal an. Wenn **[!UICONTROL Enable Guest Checkout]** ausgewählt ist, wird die Schaltfläche **[!UICONTROL Pay with Debit Card or Credit Card]** im Popup-Fenster &quot;PayPal&quot;angezeigt. Andernfalls muss sich der Käufer entweder bei PayPal anmelden oder ein PayPal-Konto erstellen.

1. Setzen Sie **[!UICONTROL Size]** auf einen der folgenden Werte:

   - `Medium` - 250 Pixel x 35 Pixel.
   - `Large` - 350 Pixel x 40 Pixel.
   - `Responsive` - (Standard) Passt an die Breite des Containers an. Die Mindestbreite beträgt 100 Pixel, die maximale Breite 500 Pixel. Die Höhe passt sich dynamisch an die Breite an.

1. Setzen Sie **[!UICONTROL Shape]** auf einen der folgenden Werte:

   - `Pill` - (Standard) Die Schaltfläche ist wie eine Pille geformt (lang in der Mitte und gekrümmt an den Enden).
   - `Rectangle` - Quadratische Form ohne Kurven in einem Rechteck.

1. Setzen Sie **[!UICONTROL Color]** auf einen der folgenden Werte:

   - `Gold` (Standard)
   - `Blue`
   - `Silver`
   - `Black`

#### Funktionen

Mit den Funktionseinstellungen können Sie bestimmte Funktionen dieser PayPal-Lösung deaktivieren.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Features]** .

   ![Einstellungen der Checkout-Seite](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings3.png){width="600" zoomable="yes"}

1. Legen Sie den **[!UICONTROL Disable Funding Options]** fest, um zu bestimmen, welche anderen PayPal-Finanzierungsoptionen auf der Seite _Checkout_ angezeigt werden.

   Die ausgewählten Optionen werden nicht auf der Seite _Checkout_ angezeigt. Nicht ausgewählte Optionen werden nur angezeigt, wenn PayPal die Store-Währung und den Käuferstandort unterstützt. Zu den Optionen gehören:

   - PayPal Credit
   - Venmo
   - PayPal Guest Checkout-Kreditkartensymbole
   - Elektronisches Lastschriftverfahren - deutsches ELV

[1]: https://www.paypal.com/webapps/mpp/how-to-sell-online
[2]: https://www.paypal.com/webapps/mpp/buying-online
[3]: https://manager.paypal.com/
[4]: https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm
[5]: https://www.paypal.com/rs/webapps/mpp/express-checkout
[6]: https://demo.paypal.com/us/demo/navigation?merchant=bigbox&amp;amp;page=incontextProductCheckout
[7]: https://developer.paypal.com/docs/api-basics/sandbox/
