---
title: PayPal Payflow Pro
description: Erfahren Sie, wie Sie PayPal Payflow Pro als Online-Zahlungslösung in Ihrem Geschäft einrichten.
exl-id: c720b33c-44e1-4954-b5be-38932393a43c
feature: Payments
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/de/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '2212'
ht-degree: 0%

---

# PayPal Payflow Pro

Das PayPal Payflow Pro-Gateway, früher _Verisign_ genannt, ist für Kunden aus den USA, Kanada, Australien und Neuseeland verfügbar. Im Gegensatz zu anderen PayPal-Zahlungsmethoden wird Händlern eine feste monatliche Gebühr zuzüglich einer festen Gebühr für jede Transaktion unabhängig von der Nummer berechnet.

![Checkout mit PayPal](./assets/storefront-cart-paypal.png){width="700" zoomable="yes"}

>[!IMPORTANT]
>
>**PSD2-Anforderungen:** <br/>
>Ab dem 14. September 2019 können europäische Banken Zahlungen ablehnen, die [PSD2&rbrace;-](../getting-started/compliance-payment-services-directive.md) nicht erfüllen. Um PSD2 zu erfüllen, muss PayPal Payflow Pro mit einem Plug-in eines Drittanbieters integriert sein. Weitere Informationen finden Sie unter [3-D Secure for Payflow](https://developer.paypal.com/api/nvp-soap/payflow/3d-secure-mpi/).

## Anforderungen

- [PayPal Business Account](https://www.paypal.com/webapps/mpp/how-to-sell-online) - Das PayPal Payflow Pro Gateway verbindet das Händlerkonto bei PayPal mit der Händlerwebsite und fungiert sowohl als Gateway als auch als Händlerkonto.

- Wenn Sie mehrere Websites von Adobe Commerce und Magento Open Source verwalten, müssen Sie für jede Website über ein separates PayPal-Händlerkonto verfügen.

## Kunden-Workflow

1. **Der Kunde geht zur Kasse** - Während der Kasse bezahlt der Kunde mit PayPal Payflow Pro und gibt die Kreditkarteninformationen ein. Kunden müssen keine persönlichen PayPal-Konten haben. Je nach Land des Händlers können Kunden jedoch auch ihr persönliches PayPal-Konto verwenden, um für die Bestellung zu bezahlen.
1. **Kunde sendet Bestellung** - Der Kunde sendet die Bestellung und die Bestellinformationen werden zur Verarbeitung an PayPal gesendet. Der Kunde verlässt die Checkout-Seite Ihrer Site nicht.
1. **PayPal schließt die Transaktion ab** - Zahlungen werden zum Zeitpunkt der Bestellung akzeptiert. Abhängig von der in der Konfiguration angegebenen Zahlungsaktion werden entweder ein Kundenauftrag oder ein Kundenauftrag und eine Rechnung erstellt.

## Workflow für die Online-Bestellabwicklung

1. **Der Administrator reicht eine Online** Rechnung ein - Der Store-Administrator reicht eine Online-Rechnung ein und erstellt daraufhin eine entsprechende Transaktion und Rechnung.
1. **PayPal erhält die Transaktion** - Die Bestellinformationen werden an PayPal gesendet. Es wird ein Datensatz der Transaktion und eine Rechnung generiert. Sie können alle Payflow Pro Gateway-Transaktionen in Ihrem [PayPal-Händlerkonto](https://manager.paypal.com/) anzeigen.

>[!NOTE]
>
>Teilrechnungen und Teilerstattungen werden von PayPal Payflow Pro nicht unterstützt.

## Konfigurieren Ihres PayPal-Kontos

1. Melden Sie sich bei Ihrem [PayPal-Geschäftskonto](https://manager.paypal.com/) an.

1. Konfigurieren Sie die [gehosteten Checkout](https://developer.paypal.com/docs/payflow/integration-guide/configure-hosted-checkout/#configuring-hosted-pages-using-paypal-manager)Seiten mithilfe von PayPal Manager mit den folgenden Einstellungen:

   - Legen Sie unter **[!UICONTROL Choose your settings]** **[!UICONTROL Transaction Process Mode]** auf `Live` fest.

   - Legen Sie unter **[!UICONTROL Display options on payment page]** **URL-Methode abbrechen** auf `POST` fest.

   - Aktivieren Sie unter **[!UICONTROL Billing Information]** die Kontrollkästchen Kartensicherheitscode **[!UICONTROL CSC]** sowohl für erforderliche als auch für bearbeitbare Felder.

   - Legen Sie unter **[!UICONTROL Payment Confirmation]** **[!UICONTROL Return URL Method]** auf `POST` fest.

   - Füllen Sie unter **[!UICONTROL Security Options]** die folgenden Einstellungen aus:

      - **[!UICONTROL AVS]**: `No`
      - **[!UICONTROL CSC]**: `No`
      - **[!UICONTROL Enable Secure Token]**: `Yes`

   - Wählen Sie **[!UICONTROL Customize]** und dann **[!UICONTROL Layout C]** aus.

     Layout C zeigt nur Kredit- und Debitkartenfelder an und kann entweder auf der Site umrahmt oder als eigenständiges Popup verwendet werden. Die Größe ist auf 490 x 565 Pixel festgelegt, mit zusätzlichem Platz für Fehlermeldungen. Auf einigen Systemen wird durch diese Einstellung ein Problem mit transparenter Umleitung behoben.

1. Wenn die Konfigurationseinstellungen abgeschlossen sind, klicken Sie auf **[!UICONTROL Save and Publish]**.

1. Wählen Sie im Menü PayPal Manager die Option **[!UICONTROL Account Administration]**.

1. Klicken Sie unter **[!UICONTROL Manage Security]** auf **[!UICONTROL Transaction Settings]** und führen Sie folgende Schritte aus:

   - Legen Sie **[!UICONTROL Allow reference transactions]** auf `Yes` fest.

   - Klicken Sie auf **[!UICONTROL Confirm]**.

     >[!NOTE]
     >
     >Wenn Sie mehrere Websites von Commerce haben, müssen Sie für jede Seite ein separates PayPal Payments Advanced-Konto erstellen.

1. Einrichten eines anderen Benutzers (empfohlen von PayPal):

   - Klicken Sie in der zweiten Zeile des Hauptmenüs auf **[!UICONTROL Manage Users]**.

   - Um einen weiteren Benutzer zum Konto hinzuzufügen, klicken Sie auf **[!UICONTROL Add User]**. Der Link befindet sich direkt über dem Titel Benutzer verwalten .

   - Füllen Sie die erforderlichen Felder in den folgenden Abschnitten des _[!UICONTROL Add User]_&#x200B;Formulars aus:

      - [!UICONTROL Admin Confirmation]
      - [!UICONTROL User Information]
      - [!UICONTROL User Login Information]
      - [!UICONTROL Assign Privilege to User]

   - Klicken Sie auf **[!UICONTROL Update]**.

1. Melden Sie sich unbedingt von Ihrem PayPal-Konto ab.

## Einrichten von PayPal Payflow Pro in Commerce

>[!TIP]
>
>Klicken Sie jederzeit auf **[!UICONTROL Save Config]** , um Ihren Fortschritt zu speichern.

### Schritt 1: Starten der Konfiguration

Bei dieser Einrichtungsmethode wird davon ausgegangen, dass Sie über ein vorhandenes PayPal-Konto verfügen.

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Payment Methods]**.

1. Wenn Ihre Commerce-Installation über mehrere Websites, Stores oder Ansichten verfügt, legen Sie **[!UICONTROL Store View]** auf die Store-Ansicht fest, in der Sie diese Konfiguration anwenden möchten.

1. Wählen Sie im Abschnitt _[!UICONTROL Merchant Location]_&#x200B;die **[!UICONTROL Merchant Country]**&#x200B;aus, in der sich Ihr Unternehmen befindet.

   Diese Einstellung bestimmt die Auswahl der PayPal-Lösungen, die in der Konfiguration angezeigt werden.

   ![Handelsland](../configuration-reference/sales/assets/payment-methods-merchant-location.png){width="600" zoomable="yes"}

1. Erweitern Sie **[!UICONTROL PayPal Payment Gateways]** (falls erforderlich) und klicken Sie zum **[!UICONTROL Configure]** auf **[!UICONTROL Payflow Pro]** .

   ![Konfigurieren - Payflow Pro](./assets/payflow-pro.png){width="600" zoomable="yes"}

### Schritt 2: Die erforderlichen PayPal-Einstellungen vornehmen

![Erforderliche Einstellungen - PayPal Payflow Pro](./assets/payflow-pro-required-a.png){width="600" zoomable="yes"}

1. (Optional) Geben Sie die **[!UICONTROL Email Associated with your PayPal Merchant Account]** ein.

   >[!IMPORTANT]
   >
   >Bei E-Mail-Adressen wird zwischen Groß- und Kleinschreibung unterschieden. Um die Zahlung zu erhalten, muss die E-Mail-Adresse mit der E-Mail-Adresse übereinstimmen, die in Ihrem PayPal-Händlerkonto angegeben ist.

1. Geben Sie eine der folgenden Anmeldedaten ein, mit denen Sie sich bei Ihrem PayPal-Händlerkonto anmelden:

   - **[!UICONTROL Partner]** - Ihre PayPal Partner ID.
   - **[!UICONTROL User]** - Wenn Sie einen oder mehrere zusätzliche Benutzer für das Konto einrichten, ist dieser Wert die ID des Benutzers, der zur Verarbeitung von Transaktionen autorisiert ist. Wenn Sie jedoch keine zusätzlichen Benutzer eingerichtet haben, hat **[!UICONTROL USER]** denselben Wert wie **[!UICONTROL Vendor]**.
   - **[!UICONTROL Vendor]** - Ihre Händler-Login-ID, die bei der Registrierung für das Konto erstellt wurde.

1. Geben Sie die **[!UICONTROL Password]** ein, die Ihrem PayPal-Konto zugeordnet ist.

1. Um Testtransaktionen auszuführen, setzen Sie **[!UICONTROL Test Mode]** auf `Yes`.

   Verwenden Sie beim Testen der Konfiguration in einer Sandbox nur [Kreditkartennummern](https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm) die von PayPal empfohlen werden. Wenn Sie bereit sind, zur Produktion zu wechseln, kehren Sie zur Konfiguration zurück und setzen Sie den Testmodus auf `No`.

1. Wenn Ihr System einen Proxy-Server verwendet, um die Verbindung zum PayPal-System herzustellen, setzen Sie **[!UICONTROL Use Proxy]** auf `Yes` und gehen Sie folgendermaßen vor:

   - Geben Sie die IP-Adresse der **[!UICONTROL Proxy Host]** ein.

   - Geben Sie die Port-Nummer des **[!UICONTROL Proxy Port]** ein.

     Ein Proxy wird verwendet, wenn die Server-Firewall den direkten Zugriff auf den PayPal-Server verhindert. In einem solchen Fall wird ein Drittanbieterserver verwendet, um Traffic weiterzuleiten.

1. Legen Sie **[!UICONTROL Enable this Solution]** auf `Yes` fest.

1. Wenn Sie Ihren Kunden [PayPal-Guthaben](paypal.md#paypal-credit-and-pay-later) anbieten möchten, setzen Sie **[!UICONTROL Enable PayPal Credit]** auf `Yes`.

1. Wenn Sie die Zahlungs-/Kreditkartendetails eines Kunden sicher speichern möchten, sodass Kunden nicht jedes Mal erneut Zahlungsinformationen eingeben müssen, setzen Sie **[!UICONTROL Vault Enabled]** auf `Yes`.

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

   ![Advertise PayPal-Credit-Homepage-Einstellungen](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit-home-page.png){width="600" zoomable="yes"}

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

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) die restlichen Abschnitte und wiederholen Sie die vorherigen Schritte für die Einstellungen der Startseite:

   - **[!UICONTROL Catalog Category Page]**
   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**

#### Werbung für PayPal PayLater

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Advertise PayPal PayLater]** .

1. Legen Sie **[!UICONTROL Enable PayPal PayLater]** auf `Yes` fest.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Home Page]** .

   ![Advertise PayPal-Credit-Homepage-Einstellungen](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-paylater-home-page.png){width="600" zoomable="yes"}

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

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) die restlichen Abschnitte und wiederholen Sie die vorherigen Schritte:

   - **[!UICONTROL Catalog Product Page]**
   - **[!UICONTROL Checkout Cart Page]**
   - **[!UICONTROL Checkout Payment Step]**
   - **[!UICONTROL Catalog Category Page]**

### Schritt 4: Vervollständigen Sie die Grundeinstellungen

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Basic Settings - PayPal Payflow Pro]** .

   ![Grundeinstellungen - PayPal Payflow Pro_](../configuration-reference/sales/assets/payment-methods-paypal-payflow-pro-basic-settings.png){width="600" zoomable="yes"}

1. Geben Sie **[!UICONTROL Title]** einen Titel ein, der PayPal Payflow Pro während des Checkouts identifiziert.

   Es wird empfohlen, den Titel _Debit- oder Kreditkarte_ zu verwenden.

1. Wenn Sie mehrere Zahlungsmethoden anbieten, geben Sie eine Zahl für **[!UICONTROL Sort Order]** ein, um die Reihenfolge zu bestimmen, in der Payflow Pro angezeigt wird, wenn es mit den anderen Zahlungsmethoden aufgelistet wird.

   Diese Zahl steht im Verhältnis zu den anderen Zahlungsmethoden. (`0` = First, `1` = Second, `2` = Third usw.)

1. Legen Sie **[!UICONTROL Payment Action]** auf eine der folgenden Einstellungen fest:

   - `Authorization` - Genehmigt den Kauf und legt die Mittel fest. Der Betrag wird erst abgehoben, wenn er vom Händler eingezogen wurde.
   - `Sale` - Der Betrag des Kaufs wird autorisiert und sofort vom Konto des Kunden zurückgezogen.

1. Wählen Sie **[!UICONTROL Credit Card Settings]** die Kreditkarten aus, die Sie für die Zahlung in Ihrem Geschäft akzeptieren.

   Zur Auswahl mehrerer Karten halten Sie die Strg-Taste (PC) bzw. die Befehlstaste (Mac) gedrückt und klicken auf jede Karte.

   >[!NOTE]
   >
   >American Express erfordert eine zusätzliche Vereinbarung.

### Schritt 5: Erweiterte Einstellungen abschließen

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Advanced Settings]** .

   ![Erweiterte Einstellungen - PayPal Payflow Pro](../configuration-reference/sales/assets/payment-methods-paypal-payflow-pro-advanced-settings.png){width="600" zoomable="yes"}

1. Legen Sie **[!UICONTROL Payment Applicable From]** auf eine der folgenden Einstellungen fest:

   - `All Allowed Countries` - Kunden aus allen [Ländern](../getting-started/store-details.md#country-options) die in Ihrer Store-Konfiguration angegeben sind, können diese Zahlungsmethode verwenden.
   - `Specific Countries` - Nach Auswahl dieser Option wird die _[!UICONTROL Payment from Specific Countries]_&#x200B;angezeigt. Halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und wählen Sie jedes Land in der Liste aus, in dem Kunden in Ihrem Geschäft Einkäufe tätigen können.

1. Um die Kommunikation mit dem Zahlungssystem in die Protokolldatei zu schreiben, setzen Sie **[!UICONTROL Debug Mode]** auf `Yes`.

   >[!NOTE]
   >
   >In Übereinstimmung mit den PCI Data Security Standards werden Kreditkarteninformationen nicht in der Protokolldatei aufgezeichnet.

1. Um die Host-Authentizitätsüberprüfung zu aktivieren, setzen Sie **[!UICONTROL Enable SSL Verification]** auf `Yes`.

1. Um Kunden zur Eingabe eines CVV-Codes aufzufordern, setzen Sie **[!UICONTROL Require CVV Entry]** auf `Yes`.

1. Füllen Sie die folgenden Abschnitte nach Bedarf für Ihren Store aus:

   - [CVV- und AVS-Einstellungen](#cvv-and-avs-settings)
   - [Einstellungen für Abrechnungsberichte](#settlement-report-settings)
   - [Frontend-Erlebniseinstellungen](#frontend-experience-settings)

#### CVV- und AVS-Einstellungen

Um zu bestimmen, wann eine Transaktion abgelehnt werden soll, wenn das Adressenüberprüfungssystem eine Diskrepanz erkennt, geben Sie an, wie verschiedene Szenarien zu behandeln sind.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL CVV and AVS Settings]** .

   ![CVV- und AVS-Einstellungen - PayPal Payflow Pro](./assets/payflow-pro-cvv-avs.png){width="600" zoomable="yes"}

1. Um eine Transaktion aufgrund einer nicht übereinstimmenden Straße abzulehnen, setzen Sie **[!UICONTROL AVS Street Does Not Match]** auf `Yes`.

1. Um eine Transaktion aufgrund einer nicht übereinstimmenden Postleitzahl abzulehnen, setzen Sie **[!UICONTROL AVS Zip Does Not Match]** auf `Yes`.

1. Um eine Transaktion aufgrund einer nicht übereinstimmenden Länderkennung abzulehnen, setzen Sie **[!UICONTROL International AVS Indicator Does Not Match]** auf `Yes`.

1. Um eine Transaktion aufgrund eines nicht übereinstimmenden CVV-Codes abzulehnen, setzen Sie **[!UICONTROL International Card Security Code Does Not Match]** auf `Yes`.

#### Einstellungen für Abrechnungsberichte

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Settlement Report Settings]** .

   ![Einstellungen für Abrechnungsberichte - PayPal Payflow Pro](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png){width="600" zoomable="yes"}

1. Gehen Sie **[!UICONTROL SFTP Credentials]** wie folgt vor:

   - Wenn Sie sich für den sicheren PayPal-FTP-Server angemeldet haben, geben Sie die folgenden SFTP-Anmeldedaten ein:

      - Login
      - Kennwort

   - Um Testberichte vor der Live-Schaltung mit dem Express-Checkout auf Ihrer Site auszuführen, setzen Sie **[!UICONTROL Sandbox Mode]** auf `Yes`.

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

Verwenden Sie die Frontend-Erlebniseinstellungen , um zu entscheiden, welche PayPal-Logos auf Ihrer Site angezeigt werden sollen, und um das Erscheinungsbild Ihrer PayPal-Händlerseiten anzupassen.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Frontend Experience Settings]** .

   ![Frontend-Erlebniseinstellungen - PayPal Payflow Pro](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings1.png){width="600" zoomable="yes"}

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

### Schritt 6: Vervollständigen Sie die Grundeinstellungen für PayPal Express Checkout

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Basic Settings - PayPal Express Checkout]** .

   ![Grundeinstellungen für den Express-Checkout](../configuration-reference/sales/assets/payment-methods-paypal-payments-pro-express-checkout-basic-settings.png){width="600" zoomable="yes"}

1. Geben Sie **[!UICONTROL Title]** einen Titel ein, der diese Zahlungsmethode beim Checkout identifiziert.

   Es wird empfohlen, für _Store-Ansicht den_ „PayPal“ festzulegen.

1. Wenn Sie mehrere Zahlungsmethoden anbieten, geben Sie eine Nummer für **[!UICONTROL Sort Order]** ein, um die Reihenfolge zu bestimmen, in der PayPal Express Checkout angezeigt wird, wenn es mit den anderen Zahlungsmethoden aufgelistet wird.

   Diese Zahl steht im Verhältnis zu den anderen Zahlungsmethoden. (`0` = First, `1` = Second, `2` = Third usw.)

1. Legen Sie **[!UICONTROL Payment Action]** auf eine der folgenden Einstellungen fest:

   - `Authorization` - Genehmigt den Kauf und legt die Mittel fest. Der Betrag wird erst abgehoben, wenn er _Händler_ wird.
   - `Sale` - Der Betrag des Kaufs wird autorisiert und sofort vom Konto des Kunden zurückgezogen.

1. Um die Schaltfläche _[!UICONTROL Check out with PayPal]_&#x200B;auf der Produktseite anzuzeigen, setzen Sie **[!UICONTROL Display on Product Details Page]**&#x200B;auf `Yes`.

### Schritt 7: Vervollständigen Sie die erweiterten Einstellungen für PayPal Express Checkout

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Advanced Settings]** .

   ![Erweiterte Einstellung für Express-Checkout](../configuration-reference/sales/assets/payment-methods-paypal-payments-pro-express-checkout-advanced-settings.png){width="600" zoomable="yes"}

1. Legen Sie **[!UICONTROL Display on Shopping Cart]** auf `Yes` fest.

1. Legen Sie **[!UICONTROL Payment Applicable From]** auf eine der folgenden Einstellungen fest:

   - `All Allowed Countries` - Kunden aus allen Ländern, die in Ihrer Store-Konfiguration angegeben sind, können diese Zahlungsmethode verwenden.
   - `Specific Countries` - Nach Auswahl dieser Option wird die _[!UICONTROL Payment from Specific Countries]_&#x200B;angezeigt. Zur Auswahl mehrerer Länder halten Sie die Strg-Taste (PC) bzw. die Befehlstaste (Mac) gedrückt und klicken auf die einzelnen Elemente.

1. Um die Kommunikation mit dem Zahlungssystem in die Protokolldatei zu schreiben, setzen Sie **[!UICONTROL Debug Mode]** auf `Yes`.

   >[!NOTE]
   >
   >In Übereinstimmung mit den PCI Data Security Standards werden Kreditkarteninformationen nicht in der Protokolldatei aufgezeichnet.

1. Um die Host-Authentizitätsüberprüfung zu aktivieren, setzen Sie **[!UICONTROL Enable SSL Verification]** auf `Yes`.

1. Um eine vollständige Zusammenfassung der Kundenbestellung nach Zeileneintrag auf der PayPal-Website anzuzeigen, setzen Sie **[!UICONTROL Transfer Cart Line Items]** auf `Yes`.

1. Damit der Kunde die Transaktion von der PayPal-Website abschließen kann, ohne zur Bestellüberprüfung an Ihren Store zurückzukehren, setzen Sie **[!UICONTROL Skip Order Review Step]** auf `Yes`.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

### Schritt 8: Google reCAPTCHA hinzufügen

Um den PayPal Payflow Pro-Checkout besser zu schützen, aktivieren Sie Google reCAPTCHA. Es enthält Optionen zum Ausführen von reCAPTCHA mit einer anklickbaren Oberfläche oder einer unsichtbaren Prüfung, um den Kunden zu validieren. Die Option „Unsichtbar“ wird empfohlen, um die Umsätze zu steigern und Ihren Store zu schützen. Weitere Informationen finden Sie unter [Google reCAPTCHA](../systems/security-google-recaptcha.md).
