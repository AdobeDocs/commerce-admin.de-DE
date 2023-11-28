---
title: PayPal Payments Advanced
description: Erfahren Sie, wie Sie PayPal Payments Advanced als Online-Zahlungslösung in Ihrem Geschäft einrichten.
exl-id: 018dd999-2f17-4650-8f61-624809ae76c6
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '2155'
ht-degree: 0%

---

# PayPal Payments Advanced

[PayPal Payments Advanced][4] ist [PCI-kompatibel](../getting-started/compliance-pci.md) -Lösung, die es Ihren Kunden ermöglicht, per Debit oder Kreditkarte zu bezahlen, ohne Ihre Website zu verlassen. Es enthält eine eingebettete Checkout-Seite, die angepasst werden kann, um ein nahtloses und sicheres Checkout-Erlebnis zu erstellen.

Auch Kunden ohne PayPal-Konto können über das sichere PayPal-Zahlungsportal Einkäufe tätigen. Zu den akzeptierten Kreditkarten gehören Visa, MasterCard, Switch/Maestro und Solo Kreditkarten in den Vereinigten Staaten und im Vereinigten Königreich. Für zusätzlichen Komfort ist PayPal Express Checkout im Lieferumfang von PayPal Payments Advanced enthalten.

>[!IMPORTANT]
>
>**PSD2-Anforderungen:** <br/>
>Ab dem 14. September 2019 könnten europäische Banken Zahlungen ablehnen, die nicht erfüllt sind [PSD2](../getting-started/compliance-payment-services-directive.md) Anforderungen. Um PSD2 einzuhalten, muss PayPal Payments Advanced mit einem Plug-in eines Drittanbieters integriert werden. Weitere Informationen finden Sie unter [3-D-Sicherheit für Payflow](https://developer.paypal.com/api/nvp-soap/payflow/3d-secure-mpi/).

>[!NOTE]
>
>PayPal Payments Advanced kann nicht für Bestellungen verwendet werden, die vom Administrator Ihres Stores erstellt wurden.

## Voraussetzungen

- [PayPal-Geschäftskonto][1]
- Wenn Sie mehrere Adobe Commerce- und Magento Open Source-Websites verwalten, müssen Sie für jede Website über ein eigenes PayPal-Handelskonto verfügen.

## Checkout-Workflow

1. **Kunde wählt Zahlungsmethode** - Während des Checkout wählt der Kunde PayPal Payments Advanced. Die Schaltfläche Jetzt bezahlen wird anstelle der Schaltfläche Bestellung platzieren angezeigt.

1. **Jetzt bezahlen** - Der Kunde klickt/tippt _Jetzt bezahlen_ und ein von PayPal gehostetes Formular angezeigt. Der Kunde gibt die Karteninformationen ein und die Karte wird verifiziert. Bei erfolgreicher Ausführung wird die Bestellbestätigungsseite angezeigt.

   **PayPal** - Das Formular enthält auch die _PayPal_ -Schaltfläche, die den Kunden zur PayPal-Site weiterleitet, wo die Zahlung mit PayPal Express Checkout erfolgen kann.

1. **Fehlerbehebung** - Wenn die Transaktion aus irgendeinem Grund fehlschlägt, wird eine Fehlermeldung auf der Checkout-Seite angezeigt und der Kunde wird angewiesen, es erneut zu versuchen. Alle Probleme werden von PayPal verwaltet.

## Workflow zur Auftragsverarbeitung

Die Verarbeitung von Bestellungen mit PayPal Payments Advanced ist dieselbe wie bei jeder normalen PayPal-Bestellung. Bestellungen werden fakturiert und versandt und Kreditkarten für Online- und Offline-Erstattungen generiert. Für Bestellungen, die mit PayPal Payments Advanced bezahlt werden, stehen jedoch keine vielfältigen Online-Erstattungen zur Verfügung.

1. **Bestellung von Kunden** - In der letzten Phase des Checkout tippt der Kunde auf die Schaltfläche Bestellung aufgeben .

1. **PayPal antwortet** - PayPal bewertet den Antrag. Wenn es als gültig erachtet wird, verarbeitet PayPal die Transaktion.

1. **Bestellstatus von Commerce-Sets** - Commerce erhält Antwort von PayPal und setzt den Bestellstatus auf einen der folgenden Werte:

   - **Verarbeitung** - Die Transaktion war erfolgreich.
   - **Ausstehende Zahlung** - Das System erhielt keine Antwort von PayPal.
   - **Abgebrochen** - Die Transaktion war aus irgendeinem Grund nicht erfolgreich.
   - **Verdächtiger Betrug** - Der Zusammenschluss hat nicht einige der [PayPal-Betrugsfilter](paypal.md#paypal-fraud-management-filters). Das System erhält die Antwort von PayPal, dass die Transaktion von Fraud Service geprüft wird.

1. **Merchant erfüllt Bestellung** - Die Handelsrechnungen und die Lieferung der Bestellung.

## PayPal-Konto konfigurieren

Bevor Sie PayPal Payments Advanced in Commerce einrichten, müssen Sie Ihr Konto auf der PayPal-Website konfigurieren.

1. Melden Sie sich bei Ihrer [PayPal-Geschäftskonto][2].

1. Navigieren Sie zu **[!UICONTROL Service Settings]** > **[!UICONTROL Hosted Checkout Pages]** > **[!UICONTROL Set Up Menu]** und führen Sie die folgenden Einstellungen aus:

   - **[!UICONTROL AVS]**: `No`
   - **[!UICONTROL CSC]**: `No`
   - **[!UICONTROL Enable Secure Token]**: `Yes`

1. **[!UICONTROL Save]** die Einstellungen.

   >[!NOTE]
   >
   >Wenn Sie über mehrere Commerce-Websites verfügen, müssen Sie für jedes Konto ein separates PayPal Payments Advanced-Konto erstellen.

1. Wenn Sie dazu aufgefordert werden, ein Layout zu erstellen, gehen Sie wie folgt vor:

   - Klicken Sie oben auf der Seite auf **[!UICONTROL Customize]**.

   - Auswählen **[!UICONTROL Layout C]**.

   - Klicken **[!UICONTROL Save and Publish]**.

1. Richten Sie einen anderen Benutzer ein (von PayPal empfohlen):

   - Melden Sie sich bei Ihrer [PayPal-Geschäftskonto][2].

   - Um einen anderen Benutzer einzurichten, befolgen Sie die Anweisungen.

   - **[!UICONTROL Save]** die Änderungen.

## Einrichten von PayPal-Zahlungen in Commerce

>[!NOTE]
>
>Sie können zwei PayPal-Lösungen gleichzeitig verwenden: Express Checkout sowie alle All-In-One- oder Payment Gateway-Lösungen. Wenn Sie Zahlungslösungen ändern, wird die zuvor verwendete deaktiviert.

>[!TIP]
>
>Klicks **[!UICONTROL Save Config]** um den Fortschritt zu speichern.

### Schritt 1: Konfiguration beginnen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen **[!UICONTROL Payment Methods]**.

1. Wenn Ihre Commerce-Installation über mehrere Websites, Stores oder Ansichten verfügt, legen Sie **[!UICONTROL Store View]** in die Store-Ansicht, auf die Sie diese Konfiguration anwenden möchten.

1. Im _[!UICONTROL Merchant Location]_auswählen, wählen Sie die **[!UICONTROL Merchant Country]**wo sich Ihr Unternehmen befindet.

   Diese Einstellung bestimmt die Auswahl der PayPal-Lösungen, die in der Konfiguration angezeigt werden.

   ![Handelsland](../configuration-reference/sales/assets/payment-methods-merchant-location.png){width="600" zoomable="yes"}

1. Erweitern **[!UICONTROL PayPal All-in-One Payment Solution]** und klicken **[!UICONTROL Configure]** für **[!UICONTROL Payments Advanced]**.

   ![PayPal Payments Advanced](./assets/paypal-payments-advanced.png){width="600" zoomable="yes"}

### Schritt 2: Abschließen der erforderlichen Einstellungen

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Required PayPal Settings]** bei Bedarf.

   ![Erweiterte erforderliche Einstellungen - PayPal-Zahlungen erweitert](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-required.png){width="600" zoomable="yes"}

1. (Optional) Geben Sie die **[!UICONTROL Email Associated with your PayPal Merchant Account]**.

   >[!IMPORTANT]
   >
   >Bei E-Mail-Adressen wird zwischen Groß- und Kleinschreibung unterschieden. Um eine Zahlung zu erhalten, muss die E-Mail-Adresse mit der E-Mail-Adresse übereinstimmen, die in Ihrem PayPal-Handelskonto angegeben ist.

   Wenn Sie kein PayPal-Konto haben, klicken Sie auf **[!UICONTROL Start accepting payments via PayPal]**.

1. Geben Sie eine der folgenden Anmeldedaten ein, mit denen Sie sich bei Ihrem PayPal-Handelskonto anmelden:

   - **[!UICONTROL Partner]** - Ihre PayPal-Partner-ID.
   - **[!UICONTROL Vendor]** - Ihr PayPal-Benutzername.
   - **[!UICONTROL User]** - Die ID eines anderen Benutzers, der in Ihrem PayPal-Konto eingerichtet ist.

1. Geben Sie die **[!UICONTROL Password]** , die mit Ihrem PayPal-Konto verknüpft ist.

1. Um Testtransaktionen auszuführen, legen Sie **[!UICONTROL Test Mode]** nach `Yes`.

   Verwenden Sie beim Testen der Konfiguration in einer Sandbox nur [Kreditkartennummern][3] die von PayPal empfohlen werden. Wenn Sie bereit sind, zur Produktion zu wechseln, kehren Sie zur Konfiguration zurück und legen Sie den Testmodus auf `No`.

1. Wenn Ihr System einen Proxy-Server verwendet, um die Verbindung zum PayPal-System herzustellen, legen Sie **[!UICONTROL Use Proxy]** nach `Yes` und gehen Sie wie folgt vor:

   - Geben Sie die IP-Adresse des **[!UICONTROL Proxy Host]**.

   - Geben Sie die Anschlussnummer der **[!UICONTROL Proxy Port]**.

     Ein Proxy wird verwendet, wenn die Server-Firewall den direkten Zugriff auf den PayPal-Server verhindert. In diesem Fall wird ein Drittanbieter-Server zum Weiterleiten des Traffics verwendet.

1. Satz **[!UICONTROL Enable this Solution]** nach `Yes`.

1. Wenn Sie ein Angebot erstellen möchten [PayPal Credit](paypal.md#paypal-credit-and-pay-later) für Ihre Kunden festlegen, **[!UICONTROL Enable PayPal Credit]** nach `Yes`.

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

   ![Advertising PayPal Credit - Einstellungen der Startseite](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit-home-page.png){width="600" zoomable="yes"}

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die verbleibenden Abschnitte und wiederholen Sie die vorherigen Schritte:

   - **[!UICONTROL Catalog Category Page]**
   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**

#### Advertise PayPal PayLater

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Advertise PayPal PayLater]** Abschnitt.

1. Satz **[!UICONTROL Enable PayPal PayLater]** nach `Yes`.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Home Page]** Abschnitt.

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

   ![Advertising PayPal Credit - Einstellungen der Startseite](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-paylater-home-page.png){width="600" zoomable="yes"}

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die verbleibenden Abschnitte und wiederholen Sie die vorherigen Schritte:

   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**
   - **[!UICONTROL Checkout Payment Step]**
   - **[!UICONTROL Catalog Category Page]**

### Schritt 4: Grundlegende Einstellungen durchführen

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Basic Settings - PayPal Payments Advanced]** bei Bedarf.

   ![PayPal-Zahlungen - Erweiterte Grundeinstellungen](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-basic-settings.png){width="600" zoomable="yes"}

1. Um PayPal-Zahlungen während des Checkout zu identifizieren, geben Sie einen **[!UICONTROL Title]**.

   Es wird empfohlen, den Titel _Schulden oder Kreditkarte_.

1. Wenn Sie mehrere Zahlungsmethoden anbieten, geben Sie eine Zahl für **[!UICONTROL Sort Order]** um die Reihenfolge zu bestimmen, in der PayPal Payments Advanced angezeigt wird, wenn es beim Checkout mit anderen Zahlungsmethoden aufgeführt wird.

   Diese Zahl ist relativ zu den anderen Zahlungsmethoden. (`0` = first, `1` = Sekunde, `2` = drittes Element usw.)

1. Satz **[!UICONTROL Payment Action]** auf einen der folgenden Werte zu:

   - `Authorization` - Genehmigt den Kauf, aber hält die Mittel fest. Der Betrag wird erst zurückgezogen, wenn er _erfasst_ durch den Händler.
   - `Sale` - Der Kaufbetrag wird genehmigt und sofort vom Konto des Kunden zurückgezogen.

### Schritt 5: Erweiterte Einstellungen durchführen

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Advanced Settings]** Abschnitt.

   ![Erweiterte Einstellungen - PayPal Payments Advanced](./assets/paypal-payments-advanced2.png){width="600" zoomable="yes"}

1. Satz **[!UICONTROL Payment Applicable From]** auf einen der folgenden Werte zu:

   - `All Allowed Countries` - Kunden von allen [Länder](../getting-started/store-details.md#country-options) Diese Zahlungsmethode kann in Ihrer Store-Konfiguration verwendet werden.
   - `Specific Countries` - Nach Auswahl dieser Option wird die _[!UICONTROL Payment from Specific Countries]_angezeigt. Halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und wählen Sie jedes Land in der Liste aus, in dem Kunden Käufe in Ihrem Geschäft tätigen können.

1. Um die Kommunikation mit dem Zahlungssystem in die Protokolldatei zu schreiben, legen Sie **[!UICONTROL Debug Mode]** nach `Yes`.

   Die Protokolldatei für PayPal Payments Advanced ist `payments_payflow_advanced.log`.

   >[!NOTE]
   >
   >Gemäß PCI Data Security Standards werden Kreditkarteninformationen nicht in der Protokolldatei aufgezeichnet.

1. Um die Authentifizierung des Hosts zu aktivieren, legen Sie **[!UICONTROL Enable SSL Verification]** nach `Yes`.

1. Um dem Kunden zu ermöglichen, seinen Eintrag des dreistelligen CVV-Sicherheitscodes von der Rückseite einer Kreditkarte aus zu korrigieren, setzen Sie **[!UICONTROL CVV Entry is Editable]** nach `Yes`.

1. Wenn Sie von Kunden die Eingabe eines CVV-Codes verlangen möchten, legen Sie **[!UICONTROL Require CVV Entry]** nach `Yes`.

1. Um dem Kunden eine Zahlungsbestätigung zu senden, setzen Sie **[!UICONTROL Send Email Confirmation]** nach `Yes`.

1. Um die Methode zu bestimmen, die für den Austausch von Informationen mit dem PayPal-Server während einer Transaktion verwendet wird, legen Sie die **[!UICONTROL URL method for Cancel URL and Return URL]** auf einen der folgenden Werte zu:

   - `GET` - (Standard) Ruft Informationen ab, die das Ergebnis eines Prozesses sind.
   - `POST` - Stellt einen Datenblock, z. B. Daten, die in ein Formular eingegeben werden, für einen Datenverarbeitungsprozess bereit.

   Die _URL abbrechen_ und _Rückgabe-URL_ Beziehen Sie sich in die Seite, auf die der Kunde nach Abschluss oder Abbruch des Zahlungs-Teils des Checkout-Prozesses auf dem PayPal-Server zurückkehrt.

1. Füllen Sie nach Bedarf die folgenden Abschnitte für Ihren Store aus:

   - [Berichtseinstellungen einrichten](#settlement-report-settings)
   - [Frontend-Erlebniseinstellungen](#frontend-experience-settings)

#### Berichtseinstellungen einrichten

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Settlement Report Settings]** Abschnitt.

   ![Berichtseinstellungen für PayPal-Konfiguration](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png){width="600" zoomable="yes"}

1. Für **[!UICONTROL SFTP Credentials]** führen Sie folgende Schritte aus:

   - Wenn Sie sich für den sicheren FTP-Server von PayPal angemeldet haben, geben Sie die folgenden SFTP-Anmeldedaten ein:

      - Anmelden
      - Kennwort

   - Um vor der Live-Schaltung Testberichte auszuführen, legen Sie **[!UICONTROL Sandbox Mode]** nach `Yes`.

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

   ![PayPal Frontend-Erlebniseinstellungen](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings.png){width="600" zoomable="yes"}

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

### Schritt 6: Vollständige Grundeinstellungen für PayPal Express Checkout

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Basic Settings - PayPal Express Checkout]** Abschnitt.

   ![PayPal Express Checkout - Grundlegende Einstellungen](../configuration-reference/sales/assets/payment-methods-paypal-advanced-express-checkout-basic-settings.png){width="600" zoomable="yes"}

1. Für **[!UICONTROL Title]** Geben Sie einen Titel ein, der diese Zahlungsmethode beim Checkout angibt.

   Festlegen des Titels auf _PayPal_ für jede Store-Ansicht empfohlen.

1. Wenn Sie mehrere Zahlungsmethoden anbieten, geben Sie eine Zahl für **[!UICONTROL Sort Order]** um die Reihenfolge zu bestimmen, in der PayPal Express Checkout erscheint, wenn es mit den anderen Zahlungsmethoden aufgeführt wird.

   Diese Zahl ist relativ zu den anderen Zahlungsmethoden. (`0` = first, `1` = Sekunde, `2` = drittes Element usw.)

1. Satz **[!UICONTROL Payment Action]** auf einen der folgenden Werte zu:

   - `Authorization` - Genehmigt den Kauf und hält die Mittel fest. Der Betrag wird erst zurückgezogen, wenn er _erfasst_ durch den Händler.
   - `Sale` - Der Kaufbetrag wird genehmigt und sofort vom Konto des Kunden zurückgezogen.

1. So zeigen Sie _[!UICONTROL Check out with PayPal]_Schaltfläche auf der Produktseite festlegen **[!UICONTROL Display on Product Details Page]**nach `Yes`.

### Schritt 7: Vollständige erweiterte Einstellungen - PayPal Express Checkout

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Advanced Settings]** Abschnitt.

   ![PayPal Express Checkout - Erweiterte Einstellungen](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-express-checkout-advanced.png){width="600" zoomable="yes"}

1. Um PayPal Express Checkout sowohl im Warenkorb als auch im Mini-Warenkorb verfügbar zu machen, legen Sie **[!UICONTROL Display on Shopping Cart]** nach `Yes`.

1. Satz **[!UICONTROL Payment Applicable From]** auf einen der folgenden Werte zu:

   - `All Allowed Countries` - Kunden von allen [Länder](../getting-started/store-details.md#country-options) Diese Zahlungsmethode kann in Ihrer Store-Konfiguration verwendet werden.
   - `Specific Countries` |Nach Auswahl dieser Option wird die _Zahlung aus der Liste der spezifischen Länder_ angezeigt. Halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie in der Liste auf jedes Land, in dem Kunden Käufe in Ihrem Geschäft tätigen können.

1. Um die Kommunikation mit dem Zahlungssystem in die Protokolldatei zu schreiben, legen Sie **[!UICONTROL Debug Mode]** nach `Yes`.

   >[!NOTE]
   >
   >Gemäß [PCI Data Security Standards](../getting-started/compliance-pci.md), werden Kreditkarteninformationen nicht in der Protokolldatei aufgezeichnet.

1. Um die Authentifizierung des Hosts zu aktivieren, legen Sie **[!UICONTROL Enable SSL Verification]** nach `Yes`.

1. Um eine vollständige Zusammenfassung der Bestellung des Kunden nach Zeileneinträgen von der PayPal-Site aus anzuzeigen, legen Sie **[!UICONTROL Transfer Cart Line Items]** nach `Yes`.

1. Damit der Kunde die Transaktion von der PayPal-Site aus abschließen kann, ohne zur Bestellprüfung zu Ihrem Store zurückzukehren, legen Sie **[!UICONTROL Skip Order Review Step]** nach `Yes`.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

[1]: https://www.paypal.com/webapps/mpp/how-to-sell-online
[2]: https://manager.paypal.com/
[3]: https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm
[4]: https://developer.paypal.com/docs/payflow/gs-ppa-hosted-pages/
