---
title: PayPal Payflow Pro
description: Erfahren Sie, wie Sie PayPal Payflow Pro als Online-Zahlungslösung in Ihrem Geschäft einrichten.
exl-id: c720b33c-44e1-4954-b5be-38932393a43c
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '2173'
ht-degree: 0%

---

# PayPal Payflow Pro

PayPal Payflow Pro Gateway, früher bekannt als _Überprüfen_, ist für Kunden aus den USA, Kanada, Australien und Neuseeland verfügbar. Im Gegensatz zu anderen Zahlungsmethoden von PayPal werden Händlern unabhängig von der Zahl eine feste monatliche Gebühr zuzüglich einer festen Gebühr für jede Transaktion berechnet.

![Checkout mit PayPal](./assets/storefront-cart-paypal.png){width="700" zoomable="yes"}

>[!IMPORTANT]
>
>**PSD2-Anforderungen:** <br/>
>Ab dem 14. September 2019 könnten europäische Banken Zahlungen ablehnen, die nicht erfüllt sind [PSD2](../getting-started/compliance-payment-services-directive.md) Anforderungen. Um PSD2 zu erfüllen, muss PayPal Payflow Pro mit einem Plug-in eines Drittanbieters integriert werden. Weitere Informationen finden Sie unter [3-D-Sicherheit für Payflow](https://developer.paypal.com/api/nvp-soap/payflow/3d-secure-mpi/).

## Voraussetzungen

- [PayPal-Geschäftskonto][1] - Das PayPal Payflow Pro Gateway verbindet das Händlerkonto bei PayPal mit der Händlerwebsite, die sowohl als Gateway als auch als Handelskonto fungiert.

- Wenn Sie mehrere Adobe Commerce- und Magento Open Source-Websites verwalten, müssen Sie für jede Website über ein eigenes PayPal-Handelskonto verfügen.

## Kundenarbeitsablauf

1. **Der Kunde geht zum Checkout** - Beim Checkout entscheidet sich der Kunde, mit PayPal Payflow Pro zu bezahlen und gibt die Kreditkarteninformationen ein. Kunden benötigen keine persönlichen PayPal-Konten. Je nach Land des Händlers können Kunden jedoch auch ihr persönliches PayPal-Konto verwenden, um die Bestellung zu bezahlen.
1. **Kunde sendet Bestellung** - Der Kunde sendet die Bestellung und die Bestellinformationen werden zur Verarbeitung an PayPal gesendet. Der Kunde verlässt die Checkout-Seite Ihrer Site nicht.
1. **PayPal schließt die Transaktion ab** - Zahlungen werden zum Zeitpunkt der Bestellung akzeptiert. Je nach der in der Konfiguration angegebenen Zahlungsaktion werden entweder ein Verkaufsauftrag oder ein Verkaufsauftrag und eine Rechnung erstellt.

## Workflow zur Verarbeitung Online-Bestellungen

1. **Administrator sendet Online-Rechnung** - Der Store-Administrator reicht eine Online-Rechnung ein und erstellt infolgedessen eine entsprechende Transaktion und Rechnung.
1. **PayPal erhält die Transaktion** - Die Bestellinformationen werden an PayPal gesendet. Es wird ein Datensatz der Transaktion und eine Rechnung erstellt. Sie können alle Payflow Pro Gateway-Transaktionen in Ihrem [PayPal-Handelskonto][2].

>[!NOTE]
>
>Teilrechnungen und Teilerstattungen werden von PayPal Payflow Pro nicht unterstützt.

## PayPal-Konto konfigurieren

1. Melden Sie sich bei Ihrer [PayPal-Geschäftskonto][2].

1. Konfigurieren Sie die [Gehostete Checkout-Seiten][4] Verwenden von PayPal Manager mit den folgenden Einstellungen:

   - under **[!UICONTROL Choose your settings]**, set **[!UICONTROL Transaction Process Mode]** nach `Live`.

   - under **[!UICONTROL Display options on payment page]**, set **URL-Methode abbrechen** nach `POST`.

   - under **[!UICONTROL Billing Information]**, wählen Sie den Kartensicherheitscode aus. **[!UICONTROL CSC]** Kontrollkästchen für sowohl erforderliche als auch bearbeitbare Felder.

   - under **[!UICONTROL Payment Confirmation]**, set **[!UICONTROL Return URL Method]** nach `POST`.

   - under **[!UICONTROL Security Options]**, führen Sie die folgenden Einstellungen aus:

      - **[!UICONTROL AVS]**: `No`
      - **[!UICONTROL CSC]**: `No`
      - **[!UICONTROL Enable Secure Token]**: `Yes`

   - Auswählen **[!UICONTROL Customize]** und wählen Sie **[!UICONTROL Layout C]**.

     Layout C zeigt nur Kredit- und Debitkartenfelder an und kann entweder auf Ihrer Site gerahmt oder als eigenständiges Popup verwendet werden. Die Größe ist auf 490 x 565 Pixel festgelegt, wobei für Fehlermeldungen zusätzlicher Speicherplatz vorgesehen ist. Auf einigen Systemen behebt diese Einstellung ein Problem mit transparenter Umleitung.

1. Klicken Sie nach Abschluss der Konfigurationseinstellungen auf **[!UICONTROL Save and Publish]**.

1. Wählen Sie im Menü &quot;PayPal-Manager&quot;die Option **[!UICONTROL Account Administration]**.

1. under **[!UICONTROL Manage Security]** klicken **[!UICONTROL Transaction Settings]** und gehen Sie wie folgt vor:

   - Satz **[!UICONTROL Allow reference transactions]** nach `Yes`.

   - Klicken **[!UICONTROL Confirm]**.

     >[!NOTE]
     >
     >Wenn Sie über mehrere Commerce-Websites verfügen, müssen Sie für jedes Konto ein separates PayPal Payments Advanced-Konto erstellen.

1. Richten Sie einen anderen Benutzer ein (von PayPal empfohlen):

   - Klicken Sie in der zweiten Zeile des Hauptmenüs auf **[!UICONTROL Manage Users]**.

   - Um dem Konto einen weiteren Benutzer hinzuzufügen, klicken Sie auf **[!UICONTROL Add User]**. Der Link befindet sich direkt über dem Titel Benutzer verwalten .

   - Füllen Sie die erforderlichen Felder in den folgenden Abschnitten des _[!UICONTROL Add User]_form:

      - [!UICONTROL Admin Confirmation]
      - [!UICONTROL User Information]
      - [!UICONTROL User Login Information]
      - [!UICONTROL Assign Privilege to User]

   - Klicken **[!UICONTROL Update]**.

1. Melden Sie sich bei Ihrem PayPal-Konto ab.

## PayPal Payflow Pro in Commerce einrichten

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

1. Erweitern **[!UICONTROL PayPal Payment Gateways]** (falls erforderlich) und klicken Sie auf **[!UICONTROL Configure]** für **[!UICONTROL Payflow Pro]**.

   ![Konfigurieren - Payflow Pro](./assets/payflow-pro.png){width="600" zoomable="yes"}

### Schritt 2: Ausfüllen der erforderlichen PayPal-Einstellungen

![Erforderliche Einstellungen - PayPal Payflow Pro](./assets/payflow-pro-required-a.png){width="600" zoomable="yes"}

1. (Optional) Geben Sie die **[!UICONTROL Email Associated with your PayPal Merchant Account]**.

   >[!IMPORTANT]
   >
   >Bei E-Mail-Adressen wird zwischen Groß- und Kleinschreibung unterschieden. Um eine Zahlung zu erhalten, muss die E-Mail-Adresse mit der E-Mail-Adresse übereinstimmen, die in Ihrem PayPal-Handelskonto angegeben ist.

1. Geben Sie eine der folgenden Anmeldedaten ein, mit denen Sie sich bei Ihrem PayPal-Handelskonto anmelden:

   - **[!UICONTROL Partner]** - Ihre PayPal-Partner-ID.
   - **[!UICONTROL User]** - Die ID eines anderen Benutzers, der in Ihrem PayPal-Konto eingerichtet ist.
   - **[!UICONTROL Vendor]** - Ihr PayPal-Benutzername.

1. Geben Sie die **[!UICONTROL Password]** , die mit Ihrem PayPal-Konto verknüpft ist.

1. Um Testtransaktionen auszuführen, legen Sie **[!UICONTROL Test Mode]** nach `Yes`.

   Verwenden Sie beim Testen der Konfiguration in einer Sandbox nur [Kreditkartennummern][3] die von PayPal empfohlen werden. Wenn Sie bereit sind, zur Produktion zu wechseln, kehren Sie zur Konfiguration zurück und legen Sie den Testmodus auf `No`.

1. Wenn Ihr System einen Proxy-Server verwendet, um die Verbindung zum PayPal-System herzustellen, legen Sie **[!UICONTROL Use Proxy]** nach `Yes` und gehen Sie wie folgt vor:

   - Geben Sie die IP-Adresse des **[!UICONTROL Proxy Host]**.

   - Geben Sie die Anschlussnummer der **[!UICONTROL Proxy Port]**.

     Ein Proxy wird verwendet, wenn die Server-Firewall den direkten Zugriff auf den PayPal-Server verhindert. In diesem Fall wird ein Drittanbieter-Server zum Weiterleiten des Traffics verwendet.

1. Satz **[!UICONTROL Enable this Solution]** nach `Yes`.

1. Wenn Sie ein Angebot erstellen möchten [PayPal Credit](paypal.md#paypal-credit-and-pay-later) für Ihre Kunden festlegen, **[!UICONTROL Enable PayPal Credit]** nach `Yes`.

1. Wenn Sie Kundendaten/Kreditkartendetails sicher speichern möchten, damit Kunden die Zahlungsinformationen nicht jedes Mal erneut eingeben müssen, legen Sie **[!UICONTROL Vault Enabled]** nach `Yes`.

### Schritt 3: Einrichten von Advertise PayPal Credit / Advertise PayPal PayLater (optional)

Ab Version 2.4.3 wird PayPal PayLater in Implementierungen unterstützt, die PayPal enthalten. Diese Funktion ermöglicht es den Käufern, eine Bestellung in zweiwöchigen Tranchen zu bezahlen, anstatt den vollen Betrag zum Zeitpunkt des Kaufs zu zahlen. Das PayPal-Krediterlebnis wird nicht mehr unterstützt.

Satz **[!UICONTROL Enable PayPal PayLater Experience]** auf einen der folgenden Werte zu:

- `Yes` - Einrichten von Advertise PayPal PayLater
- `No` - So richten Sie Advertising PayPal Credit ein

#### Advertise PayPal Credit

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Advertise PayPal Credit]** Abschnitt.

   ![Advertise PayPal Credit](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png){width="600" zoomable="yes"}

1. Um Ihre Kontoinformationen zu erhalten, klicken Sie auf **[!UICONTROL Get Publisher ID from PayPal]** und befolgen Sie die Anweisungen.

1. Geben Sie Ihre **[!UICONTROL Publisher ID]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Home Page]** Abschnitt.

   ![Advertising PayPal Credit - Einstellungen der Startseite](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit-home-page.png){width="600" zoomable="yes"}

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

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die verbleibenden Abschnitte und wiederholen Sie die vorherigen Schritte für die Einstellungen der Startseite:

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
   - **[!UICONTROL Checkout Payment Step]**
   - **[!UICONTROL Catalog Category Page]**

### Schritt 4: Grundlegende Einstellungen durchführen

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Basic Settings - PayPal Payflow Pro]** Abschnitt.

   ![Grundlegende Einstellungen - PayPal Payflow Pro_](../configuration-reference/sales/assets/payment-methods-paypal-payflow-pro-basic-settings.png){width="600" zoomable="yes"}

1. Für **[!UICONTROL Title]** Geben Sie einen Titel ein, der PayPal Payflow Pro während des Checkouts identifiziert.

   Es wird empfohlen, den Titel _Schulden oder Kreditkarte_.

1. Wenn Sie mehrere Zahlungsmethoden anbieten, geben Sie eine Zahl für **[!UICONTROL Sort Order]** um die Sequenz zu bestimmen, in der Payflow Pro erscheint, wenn es mit den anderen Zahlungsmethoden aufgelistet wird.

   Diese Zahl ist relativ zu den anderen Zahlungsmethoden. (`0` = first, `1` = Sekunde, `2` = drittes Element usw.)

1. Satz **[!UICONTROL Payment Action]** auf einen der folgenden Werte zu:

   - `Authorization` - Genehmigt den Kauf und hält die Mittel fest. Der Betrag wird erst zurückgezogen, wenn er vom Händler eingezogen wurde.
   - `Sale` - Der Kaufbetrag wird genehmigt und sofort vom Konto des Kunden zurückgezogen.

1. Für **[!UICONTROL Credit Card Settings]**, wählen Sie die Kreditkarten aus, die Sie für die Zahlung in Ihrem Geschäft akzeptieren.

   Um mehrere Karten auszuwählen, halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie auf die einzelnen Karten.

   >[!NOTE]
   >
   >American Express benötigt eine zusätzliche Vereinbarung.

### Schritt 5: Erweiterte Einstellungen durchführen

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Advanced Settings]** Abschnitt.

   ![Erweiterte Einstellungen - PayPal Payflow Pro](../configuration-reference/sales/assets/payment-methods-paypal-payflow-pro-advanced-settings.png){width="600" zoomable="yes"}

1. Satz **[!UICONTROL Payment Applicable From]** auf einen der folgenden Werte zu:

   - `All Allowed Countries` - Kunden von allen [Länder](../getting-started/store-details.md#country-options) Diese Zahlungsmethode kann in Ihrer Store-Konfiguration verwendet werden.
   - `Specific Countries` - Nach Auswahl dieser Option wird die _[!UICONTROL Payment from Specific Countries]_angezeigt. Halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und wählen Sie jedes Land in der Liste aus, in dem Kunden Käufe in Ihrem Geschäft tätigen können.

1. Um die Kommunikation mit dem Zahlungssystem in die Protokolldatei zu schreiben, legen Sie **[!UICONTROL Debug Mode]** nach `Yes`.

   >[!NOTE]
   >
   >Gemäß PCI Data Security Standards werden Kreditkarteninformationen nicht in der Protokolldatei aufgezeichnet.

1. Um die Authentifizierung des Hosts zu aktivieren, legen Sie **[!UICONTROL Enable SSL Verification]** nach `Yes`.

1. Wenn Sie von Kunden die Eingabe eines CVV-Codes verlangen möchten, legen Sie **[!UICONTROL Require CVV Entry]** nach `Yes`.

1. Füllen Sie nach Bedarf die folgenden Abschnitte für Ihren Store aus:

   - [CVV- und AVS-Einstellungen](#cvv-and-avs-settings)
   - [Berichtseinstellungen einrichten](#settlement-report-settings)
   - [Frontend-Erlebniseinstellungen](#frontend-experience-settings)

#### CVV- und AVS-Einstellungen

Um festzustellen, wann eine Transaktion abgelehnt werden soll, wenn das Adressenüberprüfungssystem eine Abweichung feststellt, legen Sie fest, wie verschiedene Szenarien behandelt werden sollen.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL CVV and AVS Settings]** Abschnitt.

   ![CVV- und AVS-Einstellungen - PayPal Payflow Pro](./assets/payflow-pro-cvv-avs.png){width="600" zoomable="yes"}

1. Um eine Transaktion abzulehnen, die auf einer nicht übereinstimmenden Straßenabweichung basiert, setzen Sie **[!UICONTROL AVS Street Does Not Match]** nach `Yes`.

1. Um eine Transaktion abzulehnen, die auf einer nicht übereinstimmenden Postleitzahl basiert, setzen Sie **[!UICONTROL AVS Zip Does Not Match]** nach `Yes`.

1. Um eine Transaktion abzulehnen, die auf einer falsch übereinstimmenden Länderkennung basiert, setzen Sie **[!UICONTROL International AVS Indicator Does Not Match]** nach `Yes`.

1. Um eine Transaktion abzulehnen, die auf einem nicht übereinstimmenden CVV-Code basiert, setzen Sie **[!UICONTROL International Card Security Code Does Not Match]** nach `Yes`.

#### Berichtseinstellungen einrichten

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Settlement Report Settings]** Abschnitt.

   ![Berichtseinstellungen für die Einrichtung - PayPal Payflow Pro](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png){width="600" zoomable="yes"}

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

Verwenden Sie die Frontend-Erlebniseinstellungen, um festzulegen, welche PayPal-Logos auf Ihrer Site erscheinen, und um das Erscheinungsbild Ihrer PayPal-Kaufseiten anzupassen.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Frontend Experience Settings]** Abschnitt.

   ![Frontend-Erlebniseinstellungen - PayPal Payflow Pro](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings1.png){width="600" zoomable="yes"}

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

### Schritt 6: Grundlegende Einstellungen für PayPal Express Checkout vornehmen

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Basic Settings - PayPal Express Checkout]** Abschnitt.

   ![Express Checkout-Grundeinstellungen](../configuration-reference/sales/assets/payment-methods-paypal-payments-pro-express-checkout-basic-settings.png){width="600" zoomable="yes"}

1. Für **[!UICONTROL Title]** Geben Sie einen Titel ein, der diese Zahlungsmethode beim Checkout angibt.

   Festlegen des Titels auf _PayPal_ für jede Store-Ansicht empfohlen.

1. Wenn Sie mehrere Zahlungsmethoden anbieten, geben Sie eine Zahl für **[!UICONTROL Sort Order]** um die Reihenfolge zu bestimmen, in der PayPal Express Checkout erscheint, wenn es mit den anderen Zahlungsmethoden aufgeführt wird.

   Diese Zahl ist relativ zu den anderen Zahlungsmethoden. (`0` = first, `1` = Sekunde, `2` = drittes Element usw.)

1. Satz **[!UICONTROL Payment Action]** auf einen der folgenden Werte zu:

   - `Authorization` - Genehmigt den Kauf und hält die Mittel fest. Der Betrag wird erst zurückgezogen, wenn er _erfasst_ durch den Händler.
   - `Sale` - Der Kaufbetrag wird genehmigt und sofort vom Konto des Kunden zurückgezogen.

1. So zeigen Sie _[!UICONTROL Check out with PayPal]_Schaltfläche auf der Produktseite festlegen **[!UICONTROL Display on Product Details Page]**nach `Yes`.

### Schritt 7: Durchführen der erweiterten Einstellungen für PayPal Express Checkout

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Advanced Settings]** Abschnitt.

   ![Erweiterte Einstellung &quot;Express Checkout&quot;](../configuration-reference/sales/assets/payment-methods-paypal-payments-pro-express-checkout-advanced-settings.png){width="600" zoomable="yes"}

1. Satz **[!UICONTROL Display on Shopping Cart]** nach `Yes`.

1. Satz **[!UICONTROL Payment Applicable From]** auf einen der folgenden Werte zu:

   - `All Allowed Countries` - Kunden aus allen in Ihrer Store-Konfiguration angegebenen Ländern können diese Zahlungsmethode verwenden.
   - `Specific Countries` - Nach Auswahl dieser Option wird die _[!UICONTROL Payment from Specific Countries]_angezeigt. Um mehrere Länder auszuwählen, halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie auf jedes Element.

1. Um die Kommunikation mit dem Zahlungssystem in die Protokolldatei zu schreiben, legen Sie **[!UICONTROL Debug Mode]** nach `Yes`.

   >[!NOTE]
   >
   >Gemäß PCI Data Security Standards werden Kreditkarteninformationen nicht in der Protokolldatei aufgezeichnet.

1. Um die Authentifizierung des Hosts zu aktivieren, legen Sie **[!UICONTROL Enable SSL Verification]** nach `Yes`.

1. Um eine vollständige Zusammenfassung der Kundenbestellung nach Zeileneinträgen von der PayPal-Site anzuzeigen, legen Sie **[!UICONTROL Transfer Cart Line Items]** nach `Yes`.

1. Damit der Kunde die Transaktion von der PayPal-Site aus abschließen kann, ohne zur Bestellprüfung zu Ihrem Store zurückzukehren, legen Sie **[!UICONTROL Skip Order Review Step]** nach `Yes`.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

### Schritt 8: Hinzufügen von Google reCAPTCHA

Um PayPal Payflow Pro Checkout besser zu schützen, aktivieren Sie Google reCAPTCHA. Es enthält Optionen zum Ausführen von reCAPTCHA mithilfe einer klickbaren Schnittstelle oder einer unsichtbaren Prüfung, um den Kunden zu validieren. Die unsichtbare Option wird empfohlen, um die Umrechnung von Verkäufen zu steigern und Ihren Store zu schützen. Weitere Informationen finden Sie unter [Google reCAPTCHA](../systems/security-google-recaptcha.md).

[1]: https://www.paypal.com/webapps/mpp/how-to-sell-online
[2]: https://manager.paypal.com/
[3]: https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm
[4]: https://developer.paypal.com/docs/payflow/integration-guide/configure-hosted-checkout/#configuring-hosted-pages-using-paypal-manager
