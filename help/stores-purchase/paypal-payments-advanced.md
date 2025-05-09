---
title: PayPal-Zahlungen - Erweitert
description: Erfahren Sie, wie Sie PayPal Payments Advanced als Online-Zahlungslösung in Ihrem Geschäft einrichten.
exl-id: 018dd999-2f17-4650-8f61-624809ae76c6
feature: Payments
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/de/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
source-git-commit: cd5b5ebec6e72ab4ba9de775bcfe8f8a89fbbb93
workflow-type: tm+mt
source-wordcount: '2161'
ht-degree: 0%

---

# PayPal-Zahlungen - Erweitert

[PayPal Payments Advanced][4] ist eine [PCI-kompatible](../getting-started/compliance-pci.md) Lösung, mit der Ihre Kunden mit Debit- oder Kreditkarte bezahlen können, ohne Ihre Website zu verlassen. Sie enthält eine eingebettete Checkout-Seite, die angepasst werden kann, um ein nahtloses und sicheres Checkout-Erlebnis zu schaffen.

Auch Kunden ohne PayPal-Konto können über das sichere PayPal-Zahlungs-Gateway Einkäufe tätigen. Akzeptierte Karten sind Visa, MasterCard, Switch/Maestro und Solo Kreditkarten in den USA und Großbritannien. Für zusätzlichen Komfort ist der PayPal Express Checkout in PayPal Payments Advanced enthalten.

>[!IMPORTANT]
>
>**PSD2-Anforderungen:** <br/>
>Ab dem 14. September 2019 können europäische Banken Zahlungen ablehnen, die [PSD2&rbrace;-](../getting-started/compliance-payment-services-directive.md) nicht erfüllen. Um PSD2 zu erfüllen, muss PayPal Payments Advanced mit einem Plug-in eines Drittanbieters integriert sein. Weitere Informationen finden Sie unter [3-D Secure for Payflow](https://developer.paypal.com/api/nvp-soap/payflow/3d-secure-mpi/).

>[!NOTE]
>
>PayPal Payments Advanced kann nicht für Bestellungen verwendet werden, die vom Administrator Ihres Geschäfts erstellt wurden.

## Anforderungen

- [PayPal-Geschäftskonto][1]
- Wenn Sie mehrere Websites von Adobe Commerce und Magento Open Source verwalten, müssen Sie für jede Website über ein separates PayPal-Händlerkonto verfügen.

## Checkout-Workflow

1. **Der Kunde wählt die Zahlungsmethode** - Während der Kasse entscheidet sich der Kunde für die Zahlung mit PayPal Payments Advanced. Die Schaltfläche Jetzt bezahlen wird anstelle der Schaltfläche Bestellung aufgeben angezeigt.

1. **Jetzt bezahlen** - Der Kunde klickt/tippt auf _Jetzt bezahlen_ und ein von PayPal gehostetes Formular wird angezeigt. Der Kunde gibt die Karteninformationen ein, und die Karte wird verifiziert. Bei Erfolg wird die Seite mit der Bestellbestätigung angezeigt.

   **Mit PayPal bezahlen** - Das Formular enthält auch die Schaltfläche _Mit PayPal bezahlen_, die den Kunden zur PayPal-Website weiterleitet, wo die Zahlung mit PayPal Express Checkout erfolgen kann.

1. **Fehlerbehebung** - Wenn die Transaktion aus irgendeinem Grund fehlschlägt, wird auf der Kaufbestätigungsseite eine Fehlermeldung angezeigt und der Kunde wird angewiesen, es erneut zu versuchen. Alle Probleme werden von PayPal verwaltet.

## Workflow für die Bestellabwicklung

Die Verarbeitung von Bestellungen mit PayPal Payments Advanced ist die gleiche wie bei jeder regulären PayPal-Bestellung. Bestellungen werden fakturiert und versendet, und es werden Gutschriften für Online- und Offline-Rückerstattungen generiert. Bei Bestellungen, die mit PayPal Payments Advanced bezahlt werden, sind jedoch keine Online-Rückerstattungen möglich.

1. **Kunde platziert Bestellung** - In der letzten Phase des Checkouts tippt der Kunde auf die Schaltfläche Bestellung aufgeben .

1. **PayPal antwortet** - PayPal bewertet die Anfrage. Wenn sich herausstellt, dass die Transaktion gültig ist, verarbeitet PayPal sie.

1. **Commerce legt den Bestellstatus fest** - Commerce erhält eine Antwort von PayPal und setzt den Bestellstatus auf einen der folgenden Werte:

   - **Verarbeitung** - Die Transaktion war erfolgreich.
   - **Zahlung ausstehend** - Das System hat keine Antwort von PayPal erhalten.
   - **Abgebrochen** - Die Transaktion war aus irgendeinem Grund nicht erfolgreich
   - **Betrugsverdacht** - Bei der Transaktion wurden einige der „PayPal[Betrugsfilter“ ](paypal.md#paypal-fraud-management-filters). Das System erhält die Antwort von PayPal, dass die Transaktion von Fraud Service überprüft wird.

1. **Händler erfüllt Bestellung** - Der Händler stellt Rechnungen aus und versendet die Bestellung.

## Konfigurieren Ihres PayPal-Kontos

Bevor Sie PayPal Payments Advanced in Commerce einrichten, müssen Sie Ihr Konto auf der PayPal-Website konfigurieren.

1. Melden Sie sich bei Ihrem [PayPal-Geschäftskonto][2] an.

1. Navigieren Sie zu **[!UICONTROL Service Settings]** > **[!UICONTROL Hosted Checkout Pages]** > **[!UICONTROL Set Up Menu]** und füllen Sie die folgenden Einstellungen aus:

   - **[!UICONTROL AVS]**: `No`
   - **[!UICONTROL CSC]**: `No`
   - **[!UICONTROL Enable Secure Token]**: `Yes`

1. **[!UICONTROL Save]** der Einstellungen.

   >[!NOTE]
   >
   >Wenn Sie mehrere Websites von Commerce haben, müssen Sie für jede Seite ein separates PayPal Payments Advanced-Konto erstellen.

1. Wenn Sie zum Erstellen eines Layouts aufgefordert werden, gehen Sie wie folgt vor:

   - Klicken Sie oben auf der Seite auf **[!UICONTROL Customize]**.

   - Wählen Sie **[!UICONTROL Layout C]**.

   - Klicken Sie auf **[!UICONTROL Save and Publish]**.

1. Einrichten eines anderen Benutzers (empfohlen von PayPal):

   - Melden Sie sich bei Ihrem [PayPal-Geschäftskonto][2] an.

   - Um einen anderen Benutzer einzurichten, befolgen Sie die Anweisungen.

   - **[!UICONTROL Save]** die Änderungen.

## Einrichten von PayPal Payments Advanced in Commerce

>[!NOTE]
>
>Sie können zwei PayPal-Lösungen gleichzeitig aktivieren: Express Checkout und jede beliebige All-In-One- oder Payment Gateway-Lösung. Wenn Sie Zahlungslösungen ändern, wird die zuvor verwendete deaktiviert.

>[!TIP]
>
>Klicken Sie jederzeit auf **[!UICONTROL Save Config]** , um Ihren Fortschritt zu speichern.

### Schritt 1: Starten der Konfiguration

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Payment Methods]**.

1. Wenn Ihre Commerce-Installation über mehrere Websites, Stores oder Ansichten verfügt, legen Sie **[!UICONTROL Store View]** auf die Store-Ansicht fest, in der Sie diese Konfiguration anwenden möchten.

1. Wählen Sie im Abschnitt _[!UICONTROL Merchant Location]_&#x200B;die **[!UICONTROL Merchant Country]**&#x200B;aus, in der sich Ihr Unternehmen befindet.

   Diese Einstellung bestimmt die Auswahl der PayPal-Lösungen, die in der Konfiguration angezeigt werden.

   ![Handelsland](../configuration-reference/sales/assets/payment-methods-merchant-location.png){width="600" zoomable="yes"}

1. Erweitern Sie **[!UICONTROL PayPal All-in-One Payment Solution]** und klicken Sie auf **[!UICONTROL Configure]** für **[!UICONTROL Payments Advanced]**.

   ![PayPal-Zahlungen - ](./assets/paypal-payments-advanced.png){width="600" zoomable="yes"}

### Schritt 2: Erforderliche Einstellungen vornehmen

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) bei Bedarf den Abschnitt **[!UICONTROL Required PayPal Settings]** .

   ![Erweiterte erforderliche Einstellungen - PayPal Payments Advanced](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-required.png){width="600" zoomable="yes"}

1. (Optional) Geben Sie die **[!UICONTROL Email Associated with your PayPal Merchant Account]** ein.

   >[!IMPORTANT]
   >
   >Bei E-Mail-Adressen wird zwischen Groß- und Kleinschreibung unterschieden. Um die Zahlung zu erhalten, muss die E-Mail-Adresse mit der E-Mail-Adresse übereinstimmen, die in Ihrem PayPal-Händlerkonto angegeben ist.

   Wenn Sie kein PayPal-Konto haben, klicken Sie auf **[!UICONTROL Start accepting payments via PayPal]**.

1. Geben Sie eine der folgenden Anmeldedaten ein, mit denen Sie sich bei Ihrem PayPal-Händlerkonto anmelden:

   - **[!UICONTROL Partner]** - Ihre PayPal Partner ID.
   - **[!UICONTROL Vendor]** - Ihr PayPal-Benutzername.
   - **[!UICONTROL User]** - Die ID eines anderen Benutzers, der auf Ihrem PayPal-Konto eingerichtet ist.

1. Geben Sie die **[!UICONTROL Password]** ein, die Ihrem PayPal-Konto zugeordnet ist.

1. Um Testtransaktionen auszuführen, setzen Sie **[!UICONTROL Test Mode]** auf `Yes`.

   Verwenden Sie beim Testen der Konfiguration in einer Sandbox nur [Kreditkartennummern][3] die von PayPal empfohlen werden. Wenn Sie bereit sind, zur Produktion zu wechseln, kehren Sie zur Konfiguration zurück und setzen Sie den Testmodus auf `No`.

1. Wenn Ihr System einen Proxy-Server verwendet, um die Verbindung zum PayPal-System herzustellen, setzen Sie **[!UICONTROL Use Proxy]** auf `Yes` und gehen Sie folgendermaßen vor:

   - Geben Sie die IP-Adresse der **[!UICONTROL Proxy Host]** ein.

   - Geben Sie die Port-Nummer des **[!UICONTROL Proxy Port]** ein.

     Ein Proxy wird verwendet, wenn die Server-Firewall den direkten Zugriff auf den PayPal-Server verhindert. In diesem Fall wird ein Drittanbieterserver verwendet, um Traffic weiterzuleiten.

1. Legen Sie **[!UICONTROL Enable this Solution]** auf `Yes` fest.

1. Wenn Sie Ihren Kunden [PayPal-Guthaben](paypal.md#paypal-credit-and-pay-later) anbieten möchten, setzen Sie **[!UICONTROL Enable PayPal Credit]** auf `Yes`.

### Schritt 3: Einrichten von Advertise PayPal Credit / Advertise PayPal PayLater (optional)

Ab Version 2.4.3 wird PayPal Later in Bereitstellungen unterstützt, die PayPal enthalten. Mit dieser Funktion können Käufer eine Bestellung in zweiwöchentlichen Raten bezahlen, anstatt den vollen Betrag zum Zeitpunkt des Kaufs zu bezahlen. Das PayPal-Krediterlebnis ist veraltet.

Legen Sie **[!UICONTROL Enable PayPal PayLater Experience]** auf eine der folgenden Einstellungen fest:

- `Yes` - Einrichten von Advertise PayPal PayLater
- `No` - Einrichten von Advertise PayPal-Guthaben

#### PayPal-Guthaben ankündigen

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Advertise PayPal Credit]** .

   ![Advertise PayPal-Guthaben](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png){width="600" zoomable="yes"}

1. Um Ihre Kontoinformationen zu erhalten, klicken Sie auf **[!UICONTROL Get Publisher ID from PayPal]** und folgen Sie den Anweisungen.

1. Geben Sie Ihre **[!UICONTROL Publisher ID]** ein.

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

   - **[!UICONTROL Catalog Category Page]**
   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**

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

1. Legen Sie **[!UICONTROL Logo Type]** nur für [!UICONTROL Style Layout] **[!UICONTROL Text]** auf eine der folgenden Einstellungen fest:

   - `Primary`
   - `Alternative`
   - `Inline`
   - `None`

1. Legen Sie **[!UICONTROL Logo Position]** nur für [!UICONTROL Style Layout] **[!UICONTROL Text]** auf eine der folgenden Einstellungen fest:

   - `Left`
   - `Right`
   - `Top`

1. Legen Sie **[!UICONTROL Text Color]** nur für [!UICONTROL Style Layout] **[!UICONTROL Text]** auf eine der folgenden Einstellungen fest:

   - `Black`
   - `White`
   - `Monochrome`
   - `Grayscale`

1. Legen Sie **[!UICONTROL Text Size]** nur für [!UICONTROL Style Layout] **[!UICONTROL Text]** auf eine der folgenden Einstellungen fest:

   - `10px`
   - `11px`
   - `12px`
   - `13px`
   - `14px`
   - `15px`
   - `16px`

1. Legen Sie **[!UICONTROL Ratio]** nur für [!UICONTROL Style Layout] **[!UICONTROL Flex]** auf eine der folgenden Einstellungen fest:

   - `1x1`
   - `1x4`
   - `8x1`
   - `20x1`

1. Legen Sie **[!UICONTROL Color]** nur für [!UICONTROL Style Layout] **[!UICONTROL Flex]** auf eine der folgenden Einstellungen fest:

   - `Blue`
   - `Black`
   - `White`
   - `White No Border`
   - `Gray`
   - `Monochrome`
   - `Grayscale`

   ![Advertise PayPal-Credit-Homepage-Einstellungen](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-paylater-home-page.png){width="600" zoomable="yes"}

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) die restlichen Abschnitte und wiederholen Sie die vorherigen Schritte:

   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**
   - **[!UICONTROL Checkout Payment Step]**
   - **[!UICONTROL Catalog Category Page]**

### Schritt 4: Vervollständigen Sie die Grundeinstellungen

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) bei Bedarf den Abschnitt **[!UICONTROL Basic Settings - PayPal Payments Advanced]** .

   ![Erweiterte Grundeinstellungen für PayPal-Zahlungen](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-basic-settings.png){width="600" zoomable="yes"}

1. Geben Sie einen **[!UICONTROL Title]** ein, um PayPal Payments Advanced während des Checkouts zu identifizieren.

   Es wird empfohlen, den Titel _Debit- oder Kreditkarte_ zu verwenden.

1. Wenn Sie mehrere Zahlungsmethoden anbieten, geben Sie eine Zahl für **[!UICONTROL Sort Order]** ein, um die Reihenfolge zu bestimmen, in der PayPal Payments Advanced angezeigt wird, wenn es während des Checkouts mit anderen Zahlungsmethoden aufgelistet wird.

   Diese Zahl steht im Verhältnis zu den anderen Zahlungsmethoden. (`0` = First, `1` = Second, `2` = Third usw.)

1. Legen Sie **[!UICONTROL Payment Action]** auf eine der folgenden Einstellungen fest:

   - `Authorization` - Genehmigt den Kauf, setzt jedoch die Mittel zurück. Der Betrag wird erst abgehoben, wenn er _Händler_ wird.
   - `Sale` - Der Betrag des Kaufs wird autorisiert und sofort vom Konto des Kunden zurückgezogen.

### Schritt 5: Erweiterte Einstellungen abschließen

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Advanced Settings]** .

   ![Erweiterte Einstellungen - PayPal Payments Advanced](./assets/paypal-payments-advanced2.png){width="600" zoomable="yes"}

1. Legen Sie **[!UICONTROL Payment Applicable From]** auf eine der folgenden Einstellungen fest:

   - `All Allowed Countries` - Kunden aus allen [Ländern](../getting-started/store-details.md#country-options) die in Ihrer Store-Konfiguration angegeben sind, können diese Zahlungsmethode verwenden.
   - `Specific Countries` - Nach Auswahl dieser Option wird die _[!UICONTROL Payment from Specific Countries]_&#x200B;angezeigt. Halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und wählen Sie jedes Land in der Liste aus, in dem Kunden in Ihrem Geschäft Einkäufe tätigen können.

1. Um die Kommunikation mit dem Zahlungssystem in die Protokolldatei zu schreiben, setzen Sie **[!UICONTROL Debug Mode]** auf `Yes`.

   Die Protokolldatei für PayPal Payments Advanced wird `payments_payflow_advanced.log`.

   >[!NOTE]
   >
   >In Übereinstimmung mit den PCI Data Security Standards werden Kreditkarteninformationen nicht in der Protokolldatei aufgezeichnet.

1. Um die Host-Authentizitätsüberprüfung zu aktivieren, setzen Sie **[!UICONTROL Enable SSL Verification]** auf `Yes`.

1. Damit der Kunde seine Eingabe des dreistelligen CVV-Sicherheitscodes von der Rückseite einer Kreditkarte korrigieren kann, setzen Sie **[!UICONTROL CVV Entry is Editable]** auf `Yes`.

1. Um Kunden zur Eingabe eines CVV-Codes aufzufordern, setzen Sie **[!UICONTROL Require CVV Entry]** auf `Yes`.

1. Um eine Zahlungsbestätigung an den Kunden zu senden, setzen Sie **[!UICONTROL Send Email Confirmation]** auf `Yes`.

1. Um die Methode zu ermitteln, die zum Austausch von Informationen mit dem PayPal-Server während einer Transaktion verwendet wird, setzen Sie die **[!UICONTROL URL method for Cancel URL and Return URL]** auf eine der folgenden Optionen:

   - `GET` - (Standard) Ruft Informationen ab, die das Ergebnis eines Prozesses sind.
   - `POST` - Stellt einen Datenblock bereit, z. B. in ein Formular eingegebene Daten, für einen Datenverarbeitungsprozess.

   Die _Abbruch_ URL und _Rückgabe-URL_ beziehen sich auf die Seite, auf der der Kunde nach Abschluss oder Stornierung des Zahlungsteils des Checkout-Prozesses auf dem PayPal-Server zurückkehrt.

1. Füllen Sie die folgenden Abschnitte nach Bedarf für Ihren Store aus:

   - [Einstellungen für Abrechnungsberichte](#settlement-report-settings)
   - [Frontend-Erlebniseinstellungen](#frontend-experience-settings)

#### Einstellungen für Abrechnungsberichte

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Settlement Report Settings]** .

   ![Einstellungen für PayPal-Abrechnungsberichte](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png){width="600" zoomable="yes"}

1. Gehen Sie **[!UICONTROL SFTP Credentials]** wie folgt vor:

   - Wenn Sie sich für den sicheren FTP-Server von PayPal angemeldet haben, geben Sie die folgenden SFTP-Anmeldedaten ein:

      - Login
      - Kennwort

   - Um Testberichte vor der Live-Schaltung auszuführen, setzen Sie **[!UICONTROL Sandbox Mode]** auf `Yes`.

   - Geben Sie die **[!UICONTROL Custom Endpoint Hostname or IP Address]** ein.

     Standardmäßig ist der Wert `reports.paypal.com`.

   - Geben Sie die **[!UICONTROL Custom Path]** ein, in der Berichte gespeichert werden.

     Standardmäßig ist der Wert `/ppreports/outgoing`.

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

Verwenden Sie die _[!UICONTROL Frontend Experience Settings]_, um festzulegen, welche PayPal-Logos auf Ihrer Site erscheinen sollen, und um das Erscheinungsbild Ihrer PayPal-Händlerseiten anzupassen.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Frontend Experience Settings]** .

   ![PayPal-Frontend-Erlebniseinstellungen](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings.png){width="600" zoomable="yes"}

1. Wählen Sie die **[!UICONTROL PayPal Product Logo]** aus, die im PayPal-Block in Ihrem Geschäft angezeigt werden soll.

   Die PayPal-Logos sind in vier Stilen und zwei Größen erhältlich:

   - `No Logo`
   - `We Prefer PayPal (150 x 60 or 150 x 40)`
   - `Now Accepting PayPal (150 x 60 or 150 x 40)`
   - `Payments by PayPal (150 x 60 or 150 x 40)`
   - `Shop Now Using PayPal (150 x 60 or 150 x 40)`

1. So passen Sie das Erscheinungsbild Ihrer PayPal-Händlerseiten an:

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

### Schritt 6: Vollständige Grundeinstellungen für PayPal Express Checkout

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Basic Settings - PayPal Express Checkout]** .

   ![PayPal Express Checkout - Grundeinstellungen](../configuration-reference/sales/assets/payment-methods-paypal-advanced-express-checkout-basic-settings.png){width="600" zoomable="yes"}

1. Geben Sie **[!UICONTROL Title]** einen Titel ein, der diese Zahlungsmethode beim Checkout identifiziert.

   Es wird empfohlen, für _Store-Ansicht den_ „PayPal“ festzulegen.

1. Wenn Sie mehrere Zahlungsmethoden anbieten, geben Sie eine Nummer für **[!UICONTROL Sort Order]** ein, um die Reihenfolge zu bestimmen, in der PayPal Express Checkout angezeigt wird, wenn es mit den anderen Zahlungsmethoden aufgelistet wird.

   Diese Zahl steht im Verhältnis zu den anderen Zahlungsmethoden. (`0` = First, `1` = Second, `2` = Third usw.)

1. Legen Sie **[!UICONTROL Payment Action]** auf eine der folgenden Einstellungen fest:

   - `Authorization` - Genehmigt den Kauf und legt die Mittel fest. Der Betrag wird erst abgehoben, wenn er _Händler_ wird.
   - `Sale` - Der Betrag des Kaufs wird autorisiert und sofort vom Konto des Kunden zurückgezogen.

1. Um die Schaltfläche _[!UICONTROL Check out with PayPal]_&#x200B;auf der Produktseite anzuzeigen, setzen Sie **[!UICONTROL Display on Product Details Page]**&#x200B;auf `Yes`.

### Schritt 7: Erweiterte Einstellungen abschließen - PayPal Express-Checkout

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Advanced Settings]** .

   ![Erweiterte Einstellungen für den PayPal Express-Checkout](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-express-checkout-advanced.png){width="600" zoomable="yes"}

1. Um den PayPal Express-Checkout sowohl im Warenkorb als auch im Mini-Warenkorb verfügbar zu machen, setzen Sie **[!UICONTROL Display on Shopping Cart]** auf `Yes`.

1. Legen Sie **[!UICONTROL Payment Applicable From]** auf eine der folgenden Einstellungen fest:

   - `All Allowed Countries` - Kunden aus allen [Ländern](../getting-started/store-details.md#country-options) die in Ihrer Store-Konfiguration angegeben sind, können diese Zahlungsmethode verwenden.
   - `Specific Countries` |Nach Auswahl dieser Option wird die _Zahlung aus der Liste spezifischer_&quot; angezeigt. Halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie auf jedes Land in der Liste, in dem Kunden in Ihrem Geschäft Einkäufe tätigen können.

1. Um die Kommunikation mit dem Zahlungssystem in die Protokolldatei zu schreiben, setzen Sie **[!UICONTROL Debug Mode]** auf `Yes`.

   >[!NOTE]
   >
   >Gemäß [PCI Data Security Standards](../getting-started/compliance-pci.md) werden Kreditkarteninformationen nicht in der Protokolldatei aufgezeichnet.

1. Um die Host-Authentizitätsüberprüfung zu aktivieren, setzen Sie **[!UICONTROL Enable SSL Verification]** auf `Yes`.

1. Um eine vollständige Zusammenfassung der Bestellung des Kunden nach Zeileneintrag auf der PayPal-Website anzuzeigen, setzen Sie **[!UICONTROL Transfer Cart Line Items]** auf `Yes`.

1. Damit der Kunde die Transaktion von der PayPal-Website abschließen kann, ohne zur Bestellüberprüfung an Ihren Store zurückzukehren, setzen Sie **[!UICONTROL Skip Order Review Step]** auf `Yes`.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

[1]: https://www.paypal.com/webapps/mpp/how-to-sell-online
[2]: https://manager.paypal.com/
[3]: https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm
[4]: https://developer.paypal.com/docs/payflow/gs-ppa-hosted-pages/
