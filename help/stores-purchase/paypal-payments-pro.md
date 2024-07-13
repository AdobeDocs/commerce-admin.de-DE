---
title: PayPal Payments Pro
description: Erfahren Sie, wie Sie PayPal Payments Pro als Online-Zahlungslösung in Ihrem Geschäft einrichten.
exl-id: 9cc5c3a6-d471-4198-85a2-c4cf9dfd378b
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '2240'
ht-degree: 0%

---

# PayPal Payments Pro

[PayPal Payments Pro][3] bietet Ihnen alle Vorteile eines Händlers und eines Zahlungs-Gateways sowie die Möglichkeit, ein eigenes, vollständig angepasstes Checkout-Erlebnis zu erstellen. PayPal Express Checkout wird automatisch mit PayPal Payments Pro aktiviert, sodass Sie mehr als 110 Millionen aktive PayPal-Benutzer erfassen können.

![PayPal Payments Pro wird im Mini-Warenkorb angezeigt](./assets/storefront-mini-cart-payments-pro-racer-tank.png){width="700" zoomable="yes"}

>[!IMPORTANT]
>
>**Anforderungen an PSD2:** <br/>
>Ab dem 14. September 2019 könnten europäische Banken Zahlungen ablehnen, die nicht den Anforderungen von [PSD2](../getting-started/compliance-payment-services-directive.md) entsprechen. Um PSD2 einzuhalten, muss PayPal Payments Pro mit einem Plug-in eines Drittanbieters integriert werden.

>[!NOTE]
>
>Zurzeit ist PayPal Payments Pro in den USA, Großbritannien und Kanada verfügbar.

## Voraussetzungen

- [PayPal-Handelskonto][1] (mit aktivierten Direktzahlungen)

## Checkout-Workflow

1. **Der Kunde geht zum Checkout** - Der Kunde fügt Produkte zum Warenkorb hinzu und klickt/tippt auf _Fahren Sie mit dem Checkout fort_.|
1. **Der Kunde wählt die Zahlungsmethode** - Während des Checkout wählt der Kunde die Option _PayPal Direct Payment_ aus und gibt die Kreditkarteninformationen ein.
   - Wenn der Kunde mit PayPal Payments Pro bezahlt, bleibt er während des Checkout-Verfahrens auf Ihrer Website.
   - Wenn Sie mit PayPal Express Checkout zahlen, wird der Kunde zur PayPal-Site weitergeleitet, um die Transaktion abzuschließen.

Auf Anfrage des Kunden kann der Store-Administrator auch eine Bestellung vom Administrator erstellen und die Transaktion mit PayPal Payments Pro verarbeiten.

## Workflow zur Auftragsverarbeitung

1. **Bestellung aufgegeben** - Die Bestellung kann entweder vom Administrator Ihres Stores oder von Ihrem PayPal-Kaufkonto verarbeitet werden.

1. **[!UICONTROL Payment Action]** - Die in der Konfiguration angegebene Zahlungsaktion wird auf die Bestellung angewendet. Zu den Optionen gehören:

   - **Autorisieren** - Commerce erstellt eine Verkaufsbestellung mit dem Status _Verarbeitung_ . In diesem Fall steht der zu genehmigende Geldbetrag noch aus.
   - **Verkauf** - Commerce erstellt sowohl einen Verkaufsauftrag als auch eine Rechnung.
   - **Capture** - PayPal überweist den Bestellbetrag aus dem Kundenkonto, dem Bankkonto oder der Kreditkarte an das Handelskonto.

1. **Rechnungsstellung** - In Commerce wird eine Rechnung erstellt, nachdem PayPal eine sofortige Zahlungsbenachrichtigung an Commerce sendet.

   Stellen Sie sicher, dass sofortige Zahlungsbenachrichtigungen in Ihrem PayPal-Handelskonto aktiviert sind.

   >[!NOTE]
   >
   >Bei Bedarf kann eine Bestellung teilweise für eine bestimmte Produktmenge in Rechnung gestellt werden. Für jede partielle Rechnung wird eine separate Capture-Transaktion mit einer eindeutigen ID bereitgestellt und eine separate Rechnung erstellt.

   Nur-Autorisierungs-Zahlungsvorgänge werden erst abgeschlossen, nachdem der volle Bestellbetrag erfasst wurde.

   Eine Bestellung kann jederzeit online storniert werden, bis der Bestellbetrag vollständig in Rechnung gestellt ist.

1. **Rückgabe** - Wenn der Kunde die gekauften Produkte zurückgibt und eine Rückerstattung beantragt, wie bei der Erfassung des Bestellbetrags und der Erstellung der Rechnung, können Sie eine Online-Rückerstattung entweder vom Administrator oder von Ihrem PayPal-Handelskonto erstellen.

## PayPal-Konto konfigurieren

Bevor Sie PayPal Payments Pro in Commerce einrichten, müssen Sie Ihr Händlerkonto auf der PayPal-Website konfigurieren.

1. Melden Sie sich bei Ihrem [PayPal-Geschäftskonto](https://manager.paypal.com/) an.

1. Wählen Sie im Menü &quot;PayPal-Manager&quot;die Option &quot;**[!UICONTROL Service Settings]**&quot;.

1. Klicken Sie unter **[!UICONTROL Hosted Checkout Pages]** auf **[!UICONTROL Set Up]**.

1. Setzen Sie unter **[!UICONTROL Choose your settings]** **[!UICONTROL Transaction Process Mode]** auf `Live`.

1. Setzen Sie unter **[!UICONTROL Display options on payment page]** **[!UICONTROL Cancel URL Method]** auf `POST`.

1. Aktivieren Sie unter &quot;**[!UICONTROL Billing Information]**&quot;die Kontrollkästchen für den Kartensicherheitscode &quot;**[!UICONTROL CSC]**&quot;für sowohl die erforderlichen als auch die bearbeitbaren Felder.

1. Setzen Sie unter **[!UICONTROL Payment Confirmation]** **[!UICONTROL Return URL Method]** auf `POST`.

1. Konfigurieren Sie unter **[!UICONTROL Security Options]** Folgendes:

   - **[!UICONTROL AVS]**: `No`
   - **[!UICONTROL CSC]**: `No`
   - **[!UICONTROL Enable Secure Token]**: `Yes`

1. Klicken Sie auf **[!UICONTROL Save Changes]**.

1. Wählen Sie im Menü _PayPal-Manager_ die Option **[!UICONTROL Service Settings]** und wählen Sie unter _Gehostete Checkout-Seiten_ die Option **[!UICONTROL Customize]**.

1. Wählen Sie **[!UICONTROL Layout C]** aus.

   Layout C zeigt nur Kredit- und Debitkartenfelder an und kann entweder auf Ihrer Site gerahmt oder als eigenständiges Popup verwendet werden. Die Größe ist auf 490 x 565 Pixel festgelegt, wobei für Fehlermeldungen zusätzlicher Speicherplatz vorgesehen ist. Auf einigen Systemen behebt diese Einstellung ein Problem mit transparenter Umleitung.

1. Klicken Sie auf **[!UICONTROL Save and Publish]**.

1. Wählen Sie im Menü &quot;PayPal-Manager&quot;die Option &quot;**[!UICONTROL Account Administration]**&quot;. Klicken Sie unter **[!UICONTROL Manage Security]** auf **[!UICONTROL Transaction Settings]**.

1. Setzen Sie **[!UICONTROL Allow reference transactions]** auf `Yes`.

1. Klicken Sie auf **[!UICONTROL Confirm]**.

   >[!NOTE]
   >
   >Wenn Sie über mehrere Commerce-Websites verfügen, müssen Sie für jedes PayPal Payments Pro-Konto ein eigenes Konto erstellen.

1. Richten Sie einen anderen Benutzer ein (von PayPal empfohlen):

   - Klicken Sie in der zweiten Zeile des Hauptmenüs auf **[!UICONTROL Manage Users]**.

   - Um dem Konto einen weiteren Benutzer hinzuzufügen, klicken Sie auf **[!UICONTROL Add User]**. Der Link befindet sich direkt über dem Titel Benutzer verwalten .

   - Füllen Sie die erforderlichen Felder in den folgenden Abschnitten des Formulars _[!UICONTROL Add User]_aus:

      - [!UICONTROL Admin Confirmation]
      - [!UICONTROL User Information]
      - [!UICONTROL User Login Information]
      - [!UICONTROL Assign Privilege to User]

   - Klicken Sie auf **[!UICONTROL Update]**.

1. Melden Sie sich bei Ihrem PayPal-Konto ab.

## PayPal Payments Pro in Commerce einrichten

>[!NOTE]
>
>Sie können zwei PayPal-Lösungen gleichzeitig aktivieren: [PayPal Express Checkout](paypal-express-checkout.md) und eine der [All-in-One-Lösungen](paypal.md#paypal-all-in-one-payment-solutions). Wenn Sie Zahlungslösungen ändern, wird die zuvor verwendete automatisch deaktiviert.

>[!TIP]
>
>Klicken Sie jederzeit auf **[!UICONTROL Save Config]** , um Ihren Fortschritt zu speichern.

### Schritt 1: Konfiguration beginnen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Payment Methods]** aus.

1. Wenn Ihre Commerce-Installation über mehrere Websites, Stores oder Ansichten verfügt, setzen Sie **[!UICONTROL Store View]** auf die Store-Ansicht, auf die Sie diese Konfiguration anwenden möchten.

1. Wählen Sie im Abschnitt _[!UICONTROL Merchant Location]_die **[!UICONTROL Merchant Country]**aus, in der sich Ihr Unternehmen befindet.

   Diese Einstellung bestimmt die Auswahl der PayPal-Lösungen, die in der Konfiguration angezeigt werden.

   ![Handelsland](../configuration-reference/sales/assets/payment-methods-merchant-location.png){width="600" zoomable="yes"}

1. Erweitern Sie **[!UICONTROL PayPal All-in-One Payment Solution]** und klicken Sie auf **[!UICONTROL Configure]** für **[!UICONTROL Payments Pro]**.

   ![PayPal Payments Pro](./assets/paypal-payments-pro.png){width="600" zoomable="yes"}

### Schritt 2: Ausfüllen der erforderlichen PayPal-Einstellungen

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Payments Pro and Express Checkout]** .

   ![PayPal Payments Pro Erforderliche Einstellungen](../configuration-reference/sales/assets/payment-methods-paypal-payments-pro-required.png){width="600" zoomable="yes"}

1. (Optional) Geben Sie den Wert **[!UICONTROL Email Associated with your PayPal Merchant Account]** ein.

   >[!IMPORTANT]
   >
   >Bei E-Mail-Adressen wird zwischen Groß- und Kleinschreibung unterschieden. Um eine Zahlung zu erhalten, muss die E-Mail-Adresse mit der E-Mail-Adresse übereinstimmen, die in Ihrem PayPal-Handelskonto angegeben ist.

   Wenn Sie kein PayPal-Konto haben, klicken Sie auf **[!UICONTROL Start accepting payments via PayPal]**.

1. Geben Sie eine der folgenden Anmeldedaten ein, mit denen Sie sich bei Ihrem PayPal-Handelskonto anmelden:

   - **[!UICONTROL Partner]** - Ihre PayPal-Partner-ID.
   - **[!UICONTROL Vendor]** - Ihr Name für die PayPal-Benutzeranmeldung.
   - **[!UICONTROL User]** - Die ID eines anderen Benutzers, der in Ihrem PayPal-Konto eingerichtet ist.

1. Geben Sie die **[!UICONTROL Password]** ein, die mit Ihrem PayPal-Konto verknüpft ist.

1. Um Testtransaktionen auszuführen, setzen Sie **[!UICONTROL Test Mode]** auf `Yes`.

   Verwenden Sie beim Testen der Konfiguration in einer Sandbox nur die von PayPal empfohlenen [Kreditkartennummern][2]. Wenn Sie bereit sind, zur Produktion zu wechseln, kehren Sie zur Konfiguration zurück und legen Sie den Testmodus auf `No` fest.

1. Wenn Ihr System einen Proxy-Server verwendet, um die Verbindung zum PayPal-System herzustellen, setzen Sie **[!UICONTROL Use Proxy]** auf `Yes` und gehen Sie wie folgt vor:

   - Geben Sie die IP-Adresse des **[!UICONTROL Proxy Host]** ein.

   - Geben Sie die Portnummer von **[!UICONTROL Proxy Port]** ein.

   Ein Proxy wird verwendet, wenn die Server-Firewall den direkten Zugriff auf den PayPal-Server verhindert. In diesem Fall wird ein Drittanbieter-Server zum Weiterleiten des Traffics verwendet.

1. Setzen Sie **[!UICONTROL Enable this Solution]** auf `Yes`.

1. Wenn Sie Ihren Kunden [PayPal Credit](paypal.md#paypal-credit-and-pay-later) anbieten möchten, setzen Sie **[!UICONTROL Enable PayPal Credit]** auf `Yes`.

1. Wenn Sie Kundendaten zu Zahlungen/Kreditkarten sicher speichern möchten, damit Kunden nicht jedes Mal wieder Zahlungsinformationen eingeben müssen, setzen Sie **[!UICONTROL Vault Enabled]** auf `Yes`.

### Schritt 3: Einrichten von Advertise PayPal Credit / Advertise PayPal PayLater (optional)

Ab Version 2.4.3 wird PayPal PayLater in Implementierungen unterstützt, die PayPal enthalten. Diese Funktion ermöglicht es den Käufern, eine Bestellung in zweiwöchigen Tranchen zu bezahlen, anstatt den vollen Betrag zum Zeitpunkt des Kaufs zu zahlen. Das PayPal-Krediterlebnis wird nicht mehr unterstützt.

Setzen Sie **[!UICONTROL Enable PayPal PayLater Experience]** auf einen der folgenden Werte:

- `Yes` - So richten Sie Advertise PayPal PayLater ein
- `No` - So richten Sie Advertising PayPal-Guthaben ein

#### Advertise PayPal Credit

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Advertise PayPal Credit]** .

   ![PayPal-Guthaben für Werbung](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png){width="600" zoomable="yes"}

1. Um Ihre Kontoinformationen zu erhalten, klicken Sie auf **[!UICONTROL Get Publisher ID from PayPal]** und befolgen Sie die Anweisungen.

1. Geben Sie Ihren **[!UICONTROL Publisher ID]** ein.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Home Page]** .

   ![Einstellungen der Advertise PayPal Credit-Startseite ](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit-home-page.png){width="600" zoomable="yes"}

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

1. Erweitern Sie ![Erweiterungsselektor](../assets/icon-display-expand.png) die verbleibenden Abschnitte und wiederholen Sie die vorherigen Schritte:

   - **[!UICONTROL Catalog Category Page]**
   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**

#### Advertise PayPal PayLater

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Advertise PayPal PayLater]** .

1. Setzen Sie **[!UICONTROL Enable PayPal PayLater]** auf `Yes`.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Home Page]** .

   ![Einstellungen der Advertise PayPal Credit-Startseite ](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-paylater-home-page.png){width="600" zoomable="yes"}

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

1. Erweitern Sie ![Erweiterungsselektor](../assets/icon-display-expand.png) die verbleibenden Abschnitte und wiederholen Sie die vorherigen Schritte:

   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**
   - **[!UICONTROL Checkout Payment Step]**
   - **[!UICONTROL Catalog Category Page]**

### Schritt 4: Grundlegende Einstellungen durchführen

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Basic Settings - PayPal Payments Pro]** .

   ![PayPal Payment Pro Basic Settings](../configuration-reference/sales/assets/payment-methods-paypal-payments-pro-basic-settings.png){width="600" zoomable="yes"}

1. Geben Sie für **[!UICONTROL Title]** einen Titel ein, der PayPal Payments Pro während des Checkout angibt.

   Es wird empfohlen, den Titel _Debit oder Credit Card_ zu verwenden.

1. Wenn Sie mehrere Zahlungsmethoden anbieten, geben Sie eine Zahl für **[!UICONTROL Sort Order]** ein, um die Sequenz zu bestimmen, in der PayPal Payments Pro erscheint, wenn Sie beim Checkout mit anderen Zahlungsmethoden aufgeführt werden.

   Diese Zahl ist relativ zu den anderen Zahlungsmethoden. (`0` = first, `1` = second, `2` = third usw.)

1. Setzen Sie **[!UICONTROL Payment Action]** auf einen der folgenden Werte:

   - `Authorization` - Genehmigt den Kauf, legt aber einen Halten für die Fonds fest. Der Betrag wird erst zurückgezogen, wenn er vom Händler _erfasst_ wurde.
   - `Sale` - Der Betrag des Kaufs wird genehmigt und sofort aus dem Kundenkonto zurückgezogen.

1. Wählen Sie für **[!UICONTROL Credit Card Settings]** die Kreditkarten aus, die Sie für die Zahlung in Ihrem Geschäft akzeptieren.

   Um mehrere Karten auszuwählen, halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie auf die einzelnen Karten.

   >[!NOTE]
   >
   >American Express benötigt eine zusätzliche Vereinbarung.

### Schritt 5: Erweiterte Einstellungen durchführen

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Advanced Settings]** .

   ![PayPal Payments Pro Advanced Settings](./assets/paypal-payments-pro-advanced-settings.png){width="600" zoomable="yes"}

1. Setzen Sie **[!UICONTROL Payment Applicable From]** auf einen der folgenden Werte:

   - `All Allowed Countries` - Kunden aus allen in Ihrer Store-Konfiguration angegebenen [Ländern](../getting-started/store-details.md#country-options) können diese Zahlungsmethode verwenden.
   - `Specific Countries` - Nach Auswahl dieser Option wird die Liste _[!UICONTROL Payment from Specific Countries]_angezeigt. Halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und wählen Sie jedes Land in der Liste aus, in dem Kunden Käufe in Ihrem Geschäft tätigen können.

1. Um Nachrichten mit dem Zahlungssystem in die Protokolldatei zu schreiben, setzen Sie **[!UICONTROL Debug Mode]** auf `Yes`.

   >[!NOTE]
   >
   >Gemäß PCI Data Security Standards werden Kreditkarteninformationen nicht in der Protokolldatei aufgezeichnet.

1. Um die Authentifizierungsüberprüfung des Hosts zu aktivieren, setzen Sie **[!UICONTROL Enable SSL Verification]** auf `Yes`.

1. Damit Kunden einen CVV-Code eingeben müssen, setzen Sie **[!UICONTROL Require CVV Entry]** auf `Yes`.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL CVV and AVS Settings]** .

1. Um festzustellen, wann eine Transaktion abgelehnt werden soll, wenn das Adressenüberprüfungssystem eine Nichtübereinstimmung feststellt, legen Sie fest, wie jedes der folgenden Szenarien behandelt werden soll:

   - Setzen Sie **[!UICONTROL AVS Street Does Not Match]** auf `Yes`, um eine Transaktion abzulehnen, die auf einer nicht übereinstimmenden Straßenabweichung basiert.

   - Um eine Transaktion basierend auf einer falsch übereinstimmenden Postleitzahl abzulehnen, setzen Sie **[!UICONTROL AVS Zip Does Not Match]** auf `Yes`.

   - Um eine Transaktion abzulehnen, die auf einer falsch übereinstimmenden Länderkennung basiert, setzen Sie **[!UICONTROL International AVS Indicator Does Not Match]** auf `Yes`.

   - Um eine Transaktion abzulehnen, die auf einem nicht übereinstimmenden CVV-Code basiert, setzen Sie **[!UICONTROL International Card Security Code Does Not Match]** auf `Yes`.

   ![PayPal Payments Pro Erforderliche Einstellungen - CVV und AVS](./assets/paypal-payments-pro-cvv-avs-settings.png){width="600" zoomable="yes"}

1. Füllen Sie nach Bedarf die folgenden Abschnitte für Ihren Store aus:

   - [Berichtseinstellungen einrichten](#settlement-report-settings)
   - [Frontend-Erlebniseinstellungen](#frontend-experience-settings)

#### Berichtseinstellungen einrichten

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Settlement Report Settings]** .

   ![Berichtseinstellungen für PayPal-Vergleich](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png){width="600" zoomable="yes"}

1. Gehen Sie für **[!UICONTROL SFTP Credentials]** wie folgt vor:

   - Wenn Sie sich für den sicheren FTP-Server von PayPal angemeldet haben, geben Sie die folgenden SFTP-Anmeldedaten ein:

      - Anmelden
      - Kennwort

   - Um Testberichte auszuführen, bevor Sie mit Payments Pro auf Ihrer Site live gehen, setzen Sie **[!UICONTROL Sandbox Mode]** auf `Yes`.

   - Geben Sie den Wert **[!UICONTROL Custom Endpoint Hostname or IP Address]** ein.

     Der Standardwert ist `reports.paypal.com`.

   - Geben Sie den **[!UICONTROL Custom Path]** ein, in dem Berichte gespeichert werden.

     Der Standardwert ist `/ppreports/outgoing`.

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

Verwenden Sie den _[!UICONTROL Frontend Experience Settings]_, um festzulegen, welche PayPal-Logos auf Ihrer Site erscheinen, und um das Erscheinungsbild Ihrer PayPal-Händlerseiten anzupassen.

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

### Schritt 6: Grundlegende Einstellungen für PayPal Express Checkout vornehmen

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Basic Settings - PayPal Express Checkout]** .

   ![Express-Checkout-Grundeinstellungen](../configuration-reference/sales/assets/payment-methods-paypal-payments-pro-express-checkout-basic-settings.png){width="600" zoomable="yes"}

1. Geben Sie für **[!UICONTROL Title]** einen Titel ein, der diese Zahlungsmethode beim Checkout angibt.

   Es wird empfohlen, den Titel für jede Store-Ansicht auf _PayPal_ festzulegen.

1. Wenn Sie mehrere Zahlungsmethoden anbieten, geben Sie eine Nummer für **[!UICONTROL Sort Order]** ein, um die Reihenfolge zu bestimmen, in der PayPal Express Checkout erscheint, wenn es mit den anderen Zahlungsmethoden aufgeführt wird.

   Diese Zahl ist relativ zu den anderen Zahlungsmethoden. (`0` = first, `1` = second, `2` = third usw.)

1. Setzen Sie **[!UICONTROL Payment Action]** auf einen der folgenden Werte:

   - `Authorization` - Genehmigt den Kauf und legt einen Besitz an den Fonds fest. Der Betrag wird erst zurückgezogen, wenn er vom Händler _erfasst_ wurde.
   - `Sale` - Der Betrag des Kaufs wird genehmigt und sofort vom Konto des Kunden zurückgezogen.

1. Um die Schaltfläche _[!UICONTROL Check out with PayPal]_auf der Produktseite anzuzeigen, setzen Sie **[!UICONTROL Display on Product Details Page]**auf `Yes`.

### Schritt 7: Durchführen der erweiterten Einstellungen für PayPal Express Checkout

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Advanced Settings]** .

   ![Erweiterte Einstellung für Express-Checkout](../configuration-reference/sales/assets/payment-methods-paypal-payments-pro-express-checkout-advanced-settings.png){width="600" zoomable="yes"}

1. Setzen Sie **[!UICONTROL Display on Shopping Cart]** auf `Yes`.

1. Setzen Sie **[!UICONTROL Payment Applicable From]** auf einen der folgenden Werte:

   - `All Allowed Countries` - Kunden aus allen in Ihrer Store-Konfiguration angegebenen [Ländern](../getting-started/store-details.md#country-options) können diese Zahlungsmethode verwenden.
   - `Specific Countries` - Nach Auswahl dieser Option wird die Liste _[!UICONTROL Payment from Specific Countries]_angezeigt. Um mehrere Länder auszuwählen, halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie auf jedes Element.

1. Um Nachrichten mit dem Zahlungssystem in die Protokolldatei zu schreiben, setzen Sie **[!UICONTROL Debug Mode]** auf `Yes`.

   >[!NOTE]
   >
   >Gemäß PCI Data Security Standards werden Kreditkarteninformationen nicht in der Protokolldatei aufgezeichnet.

1. Um die Authentifizierungsüberprüfung des Hosts zu aktivieren, setzen Sie **[!UICONTROL Enable SSL Verification]** auf `Yes`.

1. Um eine vollständige Zusammenfassung der Kundenbestellung nach Zeileneintrag von der PayPal-Site aus anzuzeigen, setzen Sie **[!UICONTROL Transfer Cart Line Items]** auf `Yes`.

1. Damit der Kunde die Transaktion von der PayPal-Site ausführen kann, ohne zur Überprüfung der Bestellung zu Ihrem Store zurückzukehren, setzen Sie **[!UICONTROL Skip Order Review Step]** auf `Yes`.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

[1]: https://www.paypal.com/webapps/mpp/how-to-sell-online
[2]: https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm
[3]: https://developer.paypal.com/docs/paypal-payments-pro/
