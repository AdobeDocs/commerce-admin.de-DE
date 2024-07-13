---
title: Store-Details
description: Erfahren Sie, wie Sie die grundlegenden Informationen für Ihren Store aktualisieren.
exl-id: f4910ff7-4fcc-482f-be1d-cad8564cdd86
feature: Configuration
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '1786'
ht-degree: 0%

---

# Store-Details

Die grundlegenden Informationen für Ihren Store umfassen den Namen und die Adresse des Stores, die Telefonnummer und die E-Mail-Adresse, die in E-Mail-Nachrichten, Rechnungen und anderen an Ihre Kunden gesendeten Nachrichten angezeigt werden.

![Allgemeine Konfiguration - Speicherdetails](./assets/config-general-store-details.png){width="900" zoomable="yes"}

## [!UICONTROL Store Information]

Der Abschnitt &quot;_[!UICONTROL Store Information]_&quot; enthält die grundlegenden Informationen, die in Verkaufsdokumenten und anderen Kommunikationen angezeigt werden.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wählen Sie unter &quot;**[!UICONTROL General]**&quot;im linken Navigationsbereich &quot;**[!UICONTROL General]**&quot;.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Store Information]** .

   ![Allgemeine Konfiguration - Informationen speichern](./assets/general-store-information.png){width="700"}

1. Legen Sie die Optionen entsprechend Ihren Store-Details fest:

   - Geben Sie den **[!UICONTROL Store Name]** ein, den Sie in allen Kommunikationen verwenden möchten.

   - Geben Sie den **[!UICONTROL Store Phone Number]** ein, der so formatiert ist, wie er angezeigt werden soll.

   - Geben Sie für &quot;**[!UICONTROL Store Hours of Operation]**&quot;die Stunden ein, in denen Ihr Geschäft geöffnet ist. Beispiel: `Mon - Fri, 9-5, Sat 9-noon PST`.

   - Wählen Sie die **[!UICONTROL Country]** aus, in der sich Ihr Unternehmen befindet.

   - Wählen Sie die **[!UICONTROL Region/State]** mit dem Land aus.

   - Geben Sie den Wert **[!UICONTROL Store Address]** ein. Wenn die Adresse lang ist, setzen Sie die Adresse in **Adresszeile speichern 2** fort.

   - Falls zutreffend, geben Sie die **[!UICONTROL VAT Number]** Ihres Stores ein.

     Um die Zahl zu überprüfen, klicken Sie auf die Schaltfläche **[!UICONTROL Validate VAT Number]** . Weitere Informationen finden Sie unter [MwSt.-ID-Validierung](../stores-purchase/vat.md#vat-id-validation).

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

Weitere Informationen zu den Konfigurationsoptionen für Speicherinformationen finden Sie im [_Konfigurationshandbuch_](../configuration-reference/general/general.md#store-information).

## [!UICONTROL Locale Options]

Das Gebietsschema bestimmt die Anzahl der Einstellungen, die im gesamten Speicher verwendet werden. Einige davon sind:

- Sprache
- Land
- Steuersatz
- Währung
- Preis
- Zahlenformat

Die Einstellung für das Gebietsschema bestimmt die Zeitzone und Sprache, die für jeden Store verwendet werden, und identifiziert die Wochentage der Arbeitswoche in dem Gebiet.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wählen Sie im linken Navigationsbereich unter **[!UICONTROL General]** die Option **[!UICONTROL General]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Locale Options]** .

   ![Allgemeine Konfiguration - Gebietsschema-Optionen](./assets/general-locale-options.png){width="700"}

1. Wählen Sie Ihren **[!UICONTROL Timezone]** aus der Liste aus.

1. Setzen Sie **[!UICONTROL Locale]** auf die Store-Sprache.

1. Setzen Sie **[!UICONTROL Weight Unit]** auf die Maßeinheit, die normalerweise für Sendungen aus Ihrem Gebietsschema verwendet wird.

1. Setzen Sie **[!UICONTROL First Day of the Week]** auf den Tag, der als erster Tag der Woche in Ihrer Region gilt.

1. Wählen Sie in der Liste **[!UICONTROL Weekend Days]** die Tage aus, die auf ein Wochenende in Ihrer Gegend fallen.

   Um mehrere Tage auszuwählen, halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie auf jedes Element.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

Weitere Informationen zu den Konfigurationsoptionen für Gebietsschemas finden Sie im [Referenzhandbuch für die Konfiguration](../configuration-reference/general/general.md#locale-options).

## [!UICONTROL State Options]

In vielen Ländern ist das Bundesland, die Provinz oder die Region ein erforderlicher Teil einer Postanschrift. Die Informationen werden für Versand- und Rechnungsinformationen, zur Berechnung von Steuersätzen usw. verwendet. Bei Ländern, in denen der Status nicht erforderlich ist, kann das Feld vollständig aus der Adresse weggelassen oder als optionales Feld eingefügt werden.

Da die Standardadressenformate von Land zu Land variieren, können Sie auch die Vorlage bearbeiten, die zum Formatieren der Adresse für Rechnungen, Packungsbeilagen und Versandbeschriftungen verwendet wird.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wählen Sie unter &quot;**[!UICONTROL General]**&quot;im linken Navigationsbereich &quot;**[!UICONTROL General]**&quot;.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL State Options]** .

   ![Allgemeine Konfiguration - Statusoptionen](./assets/general-state-options.png){width="700"}

1. Verwenden Sie die Liste &quot;**[!UICONTROL State is required for]**&quot;, um jedes Land auszuwählen, in dem Region/Bundesstaat ein erforderlicher Eintrag ist.

1. Setzen Sie **[!UICONTROL Allow to Choose State if it is Optional for Country]** auf einen der folgenden Werte:

   `Yes` - Enthält in Ländern, in denen das Statusfeld nicht erforderlich ist, das Feld &quot;Bundesland&quot;als optionalen Eintrag.

   `No` - In Ländern, in denen das Statusfeld nicht erforderlich ist, wird das Feld &quot;Bundesland&quot;weggelassen.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

Weitere Informationen zu den Statuskonfigurationsoptionen finden Sie im [Konfigurationshandbuch](../configuration-reference/general/general.md#state-options).

## [!UICONTROL Country Options]

Die Länderoptionen geben an, in welchem Land sich Ihr Unternehmen befindet und aus welchem Land Sie die Zahlung annehmen.

### Festlegen der Länderoptionen für Ihren Store

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wählen Sie im linken Navigationsbereich unter **[!UICONTROL General]** die Option **[!UICONTROL General]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Country Options]** .

   >[!NOTE]
   >
   >Deaktivieren Sie bei Bedarf das Kontrollkästchen **[!UICONTROL Use system value]** für jede Einstellung, die Sie ändern möchten.

   ![Allgemeine Konfiguration - Ländereinstellungen](./assets/general-country-options.png){width="700"}

1. Wählen Sie die **[!UICONTROL Default Country]** aus, in der sich Ihr Unternehmen befindet.

1. Wählen Sie in der Liste **[!UICONTROL Allow Countries]** jedes Land aus, aus dem Sie Bestellungen annehmen.

   Standardmäßig sind alle Länder in der Liste ausgewählt. Um mehrere Länder auszuwählen, halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie auf jedes Element.

1. Verwenden Sie die Liste &quot;**[!UICONTROL Zip/Postal Code is Optional for]**&quot;, um jedes Land auszuwählen, in dem Sie geschäftlich tätig sind und für das keine Postleitzahl oder Postleitzahl erforderlich ist.

1. Wählen Sie in der Liste **[!UICONTROL European Union Countries]** jedes Land in der EU aus, in dem Sie Geschäfte tätigen.

   Standardmäßig sind alle EU-Länder ausgewählt. Um die gewünschten Länder auszuwählen, halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie auf jedes Element.

1. Wählen Sie in der Liste &quot;**[!UICONTROL Top Destinations]**&quot;die primären Länder aus, die Sie für den Verkauf als Ziel auswählen.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

### Festlegen der Länderoptionen für bestimmte Bereitstellungsmethoden

Sie können auch den Versand an bestimmte Länder für jede verfügbare [Versandmethode](../stores-purchase/delivery.md) (UPS, FedEx usw.) konfigurieren.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Navigationsbereich den Eintrag **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Delivery Methods]**.

1. Wählen Sie den Versandunternehmen aus, auf den Sie bestimmte Länder anwenden möchten.

1. Deaktivieren Sie für **[!UICONTROL Ship to Applicable Countries]** das Kontrollkästchen **[!UICONTROL Use system value]** und wählen Sie die Option **[!UICONTROL Specific Countries]** aus.

1. Wählen Sie in der Liste &quot;**[!UICONTROL Top Destinations]**&quot;die primären Länder aus, die Sie für den Versand als Zielgruppe wählen.

   ![Beispiel für das Festlegen der Länderoptionen für die DHL-Versandmethode](./assets/country-options-for-specific-delivery-method.png){width="700"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

### Fehlerbehebung bei Ressourcen

Hilfe zur Fehlerbehebung bei Problemen mit der Länderkonfiguration finden Sie in den folgenden Artikeln der Support Knowledge Base: [!DNL Commerce]

- [Hinzufügen eines Landes](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/how-to/how-to-add-a-new-country-to-magento-2.html)
- [Die bereitgestellte countryId ist nicht vorhanden](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-15/mdva-33393-magento-patch-provided-countryid-does-not-exist.html)

## [!UICONTROL Merchant Location]

Die Einstellung &quot;Merchant Location&quot;wird verwendet, um [Zahlungsmethoden](../stores-purchase/payments.md) zu konfigurieren. Wenn für diese Einstellung kein Wert vorhanden ist, wird die Einstellung [Standardland](#uicontrol-country-options) verwendet.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Navigationsbereich den Eintrag **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Payment Methods]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **Handelsposition** und wählen Sie Ihren **[!UICONTROL Merchant Country]** aus.

   ![Standort des Händlers festlegen](./assets/payment-methods-merchant-location.png){width="600"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

Weitere Informationen zu den Konfigurationsoptionen für Zahlungsmethoden finden Sie im [Konfigurationshandbuch](../configuration-reference/sales/payment-methods.md).

## Währung

Währungseinstellungen - Definiert die Basis-Währung [Währung](../stores-purchase/currency-configuration.md) und alle zusätzlichen Währungen, die als Zahlung akzeptiert werden. Stellt außerdem die Importverbindung und den Zeitplan her, die verwendet werden, um die Währungsraten automatisch zu aktualisieren.

Währungssymbole - Definiert die [Währungssymbole](../stores-purchase/currency-configuration.md#step-5-customize-currency-symbols-optional), die in Produktpreisen und Verkaufsdokumenten wie Bestellungen und Rechnungen angezeigt werden. [!DNL Commerce] unterstützt Währungen aus über 200 Ländern auf der ganzen Welt.

Aktualisieren der Währungsraten - Die Währungsraten können [manuell aktualisiert](../stores-purchase/currency-update.md) oder nach Bedarf oder gemäß einem vordefinierten Zeitplan in Ihren Speicher importiert werden.

Währungsauswahl - Wenn mehrere Währungen verfügbar sind, ist die [Währungsauswahl](../stores-purchase/currency.md) in der Kopfzeile des Stores verfügbar.

## [!UICONTROL Store Email Addresses]

Sie können über bis zu fünf verschiedene E-Mail-Adressen verfügen, die für jeden Store oder jede Ansicht unterschiedliche Funktionen oder Abteilungen darstellen. Neben den folgenden vordefinierten E-Mail-Identitäten gibt es einige benutzerdefinierte Identitäten, die Sie entsprechend Ihren Anforderungen einrichten können.

- Allgemeiner Kontakt
- Vertriebsmitarbeiter
- Kundensupport

Jede Identität und die zugehörige E-Mail-Adresse können bestimmten automatisierten E-Mail-Nachrichten zugeordnet werden und werden als Absender von E-Mail-Nachrichten angezeigt, die von Ihrem Store gesendet werden.

### Schritt 1: E-Mail-Adressen für Ihre Domäne einrichten

Bevor Sie E-Mail-Adressen für den Store konfigurieren können, muss jede als gültige E-Mail-Adresse für Ihre Domäne eingerichtet werden. Befolgen Sie die Anweisungen Ihres Serveradministrators oder E-Mail-Hosting-Anbieters, um jede erforderliche E-Mail-Adresse zu erstellen.

### Schritt 2: E-Mail-Adressen für Ihren Store konfigurieren

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wählen Sie unter &quot;**[!UICONTROL General]**&quot;im linken Navigationsbereich &quot;**[!UICONTROL Store Email Addresses]**&quot;.

1. Erweitern Sie den Abschnitt **[!UICONTROL General Contact]** des Erweiterungsselektors ![Erweiterung](../assets/icon-display-expand.png) und führen Sie folgende Schritte aus:

   ![Allgemeine Konfiguration - E-Mail-Adressen speichern](./assets/store-email-addresses-general-contact.png){width="600"}

   - Geben Sie für &quot;**[!UICONTROL Sender Name]**&quot;den Namen der Person ein, die mit der allgemeinen Kontaktidentität verknüpft ist, um als Absender von E-Mail-Nachrichten angezeigt zu werden.

   - Geben Sie für &quot;**[!UICONTROL Sender Email]**&quot;die zugehörige E-Mail-Adresse ein.

1. Wiederholen Sie diesen Vorgang für jede Store-E-Mail-Adresse, die Sie verwenden möchten.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

### Schritt 3: Konfiguration der Verkaufs-E-Mail aktualisieren

Wenn Sie benutzerdefinierte E-Mail-Adressen verwenden, stellen Sie sicher, dass Sie die Konfiguration zugehöriger E-Mail-Nachrichten aktualisieren, damit die richtige Identität als Absender angezeigt wird.

1. Erweitern Sie im linken Navigationsbereich den Eintrag **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Sales Emails]**.

   Die Seite verfügt über einen eigenen Abschnitt für jeden der folgenden Punkte:

   - Bestellkommentare
   - Rechnungen und Rechnungskommentare
   - Anmerkungen zu Versand und Versand
   - Kommentare zu Credit Memo und Credit Memo
   - RMA, RMA Authorization, RMA Admin Comments und RMA Customer Comments ![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce)

1. Erweitern Sie ab **[!UICONTROL Order]** den Abschnitt für jede Nachricht und stellen Sie sicher, dass der richtige Absender ausgewählt ist.

   ![Verkaufskonfiguration - E-Mails zum Vertrieb](./assets/sales-emails-order.png){width="600"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

Weitere Informationen zu den Konfigurationsoptionen für E-Mails für Vertrieb finden Sie im [_Konfigurationshandbuch_](../configuration-reference/sales/sales-emails.md).

## Kontaktformular

Der Link _Kontaktaufnahme mit uns_ in der Fußzeile des Stores ist eine einfache Möglichkeit für Kunden, mit Ihnen in Kontakt zu bleiben. Kunden können das Formular ausfüllen, um eine Nachricht an Ihren Store zu senden. Bei einer Standardinstallation von [!DNL Commerce] wird das standardmäßige Formular _Kontaktaufnahme_ angezeigt. Nach dem Senden des Formulars wird eine Dankesmeldung angezeigt

Es ist wichtig zu verstehen, dass das standardmäßige Kontaktformular direkt aus dem Code und nicht aus einer CMS-Seite gerendert wird.

![Standardseite für den Kontakt](./assets/page-contact-us-default.png){width="700"}

Die Fußzeile des Stores enthält einen Link zur Seite Kontakt , die im gesamten Store verfügbar ist.

![Link &quot;Kontaktaufnahme&quot;in der Fußzeile](./assets/storefront-footer-contact-us.png){width="700"}

Die Luma-Beispieldaten enthalten zusätzliche Informationen auf der Seite Kontakt , die zeigt, wie Sie die Seite für Ihren Store anpassen können.

![Kontaktseite](./assets/storefront-contact-us.png){width="700"}

### Kontaktformular konfigurieren

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wählen Sie im linken Navigationsbereich unter **[!UICONTROL General]** die Option **[!UICONTROL Contacts]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Contact Us]** und legen Sie **[!UICONTROL Enable Contact Us]** auf `Yes` fest.

   ![Allgemeine Konfiguration - Kontakt](./assets/contacts-contact-us.png){width="600"}

1. Erweitern Sie den Abschnitt ![Erweiterungsauswahl](../assets/icon-display-expand.png) und legen Sie die E-Mail-Kontaktoptionen fest:**[!UICONTROL Email Options]**

   ![Allgemeine Konfiguration - E-Mail-Optionen](./assets/contacts-email-options.png){width="600"}

   - Geben Sie für &quot;**[!UICONTROL Send Emails to]**&quot; die E-Mail-Adresse ein, an die Nachrichten aus dem Kontaktformular gesendet werden.

   - Setzen Sie **[!UICONTROL Email Sender]** auf die Store-Identität, die als Absender der Nachricht aus dem Kontaktformular angezeigt wird. Beispiel: Benutzerdefinierte E-Mail 2.

   - Setzen Sie **[!UICONTROL Email Template]** auf die Vorlage, die für Nachrichten verwendet wird, die über das Kontaktformular gesendet werden.

1. Klicken Sie in der Wettbewerbsphase auf **[!UICONTROL Save Config]**.

### Inhalt anpassen

Sie können den Inhalt im Formular _Kontaktaufnahme mit uns_ an die Anforderungen Ihrer Store- und Kundendienstrichtlinien anpassen.

### Methode 1: Verwendung von Beispieldaten

Die Luma-Beispieldaten enthalten einen Block _Contact Us Info_ , der für Ihren Store angepasst werden kann. Der `contact-us-info` [block](../content-design/blocks.md) kann einfach geändert werden, um eigene Inhalte zur Seite &quot;Kontakt&quot;hinzuzufügen.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.

1. Suchen Sie den Block **[!UICONTROL Contact Us Info]** in der Liste und öffnen Sie ihn im Modus **[!UICONTROL Edit]** .

   ![Kontaktaufnahme mit uns Info block](./assets/content-block-contact-us-info.png){width="700"}

1. Klicken Sie unten auf der Blockseite auf **[!UICONTROL Edit with Page Builder]**.

   ![Inhaltsbaustein - Beispiel kontaktieren](./assets/content-block-contact-us-content.png){width="700"}

   >[!NOTE]
   >
   >Wenn Sie [[!DNL Page Builder] disabled](../page-builder/setup.md#disable-dnl-page-builder) haben, können Sie den Text mit dem Editor [toolbar](../content-design/editor.md) formatieren und [images](../content-design/editor-insert-image.md) und [links](../content-design/editor-insert-link.md) hinzufügen.

1. Bewegen Sie den Mauszeiger über den HTML-Container, um die Toolbox anzuzeigen, und wählen Sie das Symbol _Einstellungen_ ( ![Einstellungssymbol](../page-builder/assets/pb-icon-settings.png) ).

1. Bearbeiten Sie den HTML-Code entsprechend den Kontaktdaten für Ihren Store und klicken Sie auf **[!UICONTROL Save]**.

   ![Inhaltsbaustein - HTML-Code bearbeiten](./assets/content-block-contact-us-html.png){width="700"}

1. Beenden Sie die [!DNL Page Builder] Bühne und klicken Sie auf **[!UICONTROL Save Block]**.

### Methode 2: Ohne Beispieldaten

>[!IMPORTANT]
>
>Ab Version 2.4.0 kann das Kontaktformular nicht mehr in einem CMS-Block oder einer CMS-Seite aufrufen. Die Anpassung des Kontaktformulars sollte mit der Layout-XML oder benutzerdefinierten Designvorlagen erfolgen.

Standardmäßig greifen Käufer über den Link _Kontakt_ in der Fußzeile der Storefront-Seiten auf das Kontaktformular zu. Weitere Informationen zum Anpassen der Kontaktseite finden Sie im [Frontend-Entwicklerhandbuch][theme-guide].

[theme-guide]: https://developer.adobe.com/commerce/frontend-core/guide/themes/
