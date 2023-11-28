---
title: Store-Details
description: Erfahren Sie, wie Sie die grundlegenden Informationen für Ihren Store aktualisieren.
exl-id: f4910ff7-4fcc-482f-be1d-cad8564cdd86
feature: Configuration
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '1797'
ht-degree: 0%

---

# Store-Details

Die grundlegenden Informationen für Ihren Store umfassen den Namen und die Adresse des Stores, die Telefonnummer und die E-Mail-Adresse, die in E-Mail-Nachrichten, Rechnungen und anderen an Ihre Kunden gesendeten Nachrichten angezeigt werden.

![Allgemeine Konfiguration - Store-Details](./assets/config-general-store-details.png){width="900" zoomable="yes"}

## [!UICONTROL Store Information]

Die _[!UICONTROL Store Information]_enthält die grundlegenden Informationen, die in Verkaufsdokumenten und anderen Kommunikationen angezeigt werden.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. under **[!UICONTROL General]** Wählen Sie im linken Navigationsbereich die Option **[!UICONTROL General]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Store Information]** Abschnitt.

   ![Allgemeine Konfiguration - Informationen speichern](./assets/general-store-information.png){width="700"}

1. Legen Sie die Optionen entsprechend Ihren Store-Details fest:

   - Geben Sie die **[!UICONTROL Store Name]** die Sie in allen Kommunikationen verwenden möchten.

   - Geben Sie die **[!UICONTROL Store Phone Number]**, formatiert, wie Sie es sehen möchten.

   - Für **[!UICONTROL Store Hours of Operation]**, geben Sie die Stunden ein, in denen Ihr Geschäft für Geschäftszwecke geöffnet ist. Beispiel: `Mon - Fri, 9-5, Sat 9-noon PST`.

   - Wählen Sie die **[!UICONTROL Country]** wo sich Ihr Unternehmen befindet.

   - Wählen Sie die **[!UICONTROL Region/State]** mit dem Land.

   - Geben Sie die **[!UICONTROL Store Address]**. Wenn die Adresse lang ist, setzen Sie die Adresse auf **Adresszeile 2**.

   - Geben Sie gegebenenfalls die **[!UICONTROL VAT Number]** Ihres Ladens.

     Um die Zahl zu überprüfen, klicken Sie auf die **[!UICONTROL Validate VAT Number]** Schaltfläche. Weitere Informationen finden Sie unter [MwSt-ID-Validierung](../stores-purchase/vat.md#vat-id-validation).

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

Weitere Informationen zu den Konfigurationsoptionen für Speicherinformationen finden Sie unter [_Konfigurationshandbuch_](../configuration-reference/general/general.md#store-information).

## [!UICONTROL Locale Options]

Das Gebietsschema bestimmt die Anzahl der Einstellungen, die im gesamten Speicher verwendet werden. Einige davon sind:

- Sprache
- Land
- Steuersatz
- Währung
- Preis
- Zahlenformat

Die Einstellung für das Gebietsschema bestimmt die Zeitzone und Sprache, die für jeden Store verwendet werden, und identifiziert die Wochentage der Arbeitswoche in dem Gebiet.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Im linken Navigationsbereich unter **[!UICONTROL General]** auswählen **[!UICONTROL General]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Locale Options]** Abschnitt.

   ![Allgemeine Konfiguration - Gebietsschemaoptionen](./assets/general-locale-options.png){width="700"}

1. Wählen Sie **[!UICONTROL Timezone]** aus der Liste.

1. Satz **[!UICONTROL Locale]** in die Store-Sprache.

1. Satz **[!UICONTROL Weight Unit]** zur Maßeinheit, die normalerweise für Sendungen aus Ihrem Gebietsschema verwendet wird.

1. Satz **[!UICONTROL First Day of the Week]** an dem Tag, der als erster Wochentag in Ihrer Gegend gilt.

1. Im **[!UICONTROL Weekend Days]** -Liste die Tage auswählen, die auf ein Wochenende in Ihrer Gegend fallen.

   Um mehrere Tage auszuwählen, halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie auf jedes Element.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

Weitere Informationen zu den Konfigurationsoptionen für Gebietsschemata finden Sie unter [Konfigurationshandbuch](../configuration-reference/general/general.md#locale-options).

## [!UICONTROL State Options]

In vielen Ländern ist das Bundesland, die Provinz oder die Region ein erforderlicher Teil einer Postanschrift. Die Informationen werden für Versand- und Rechnungsinformationen, zur Berechnung von Steuersätzen usw. verwendet. Bei Ländern, in denen der Status nicht erforderlich ist, kann das Feld vollständig aus der Adresse weggelassen oder als optionales Feld eingefügt werden.

Da die Standardadressenformate von Land zu Land variieren, können Sie auch die Vorlage bearbeiten, die zum Formatieren der Adresse für Rechnungen, Packungsbeilagen und Versandbeschriftungen verwendet wird.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. under **[!UICONTROL General]** Wählen Sie im linken Navigationsbereich die Option **[!UICONTROL General]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL State Options]** Abschnitt.

   ![Allgemeine Konfiguration - Statusoptionen](./assets/general-state-options.png){width="700"}

1. Verwenden Sie die **[!UICONTROL State is required for]** Liste, um jedes Land auszuwählen, in dem Region/Bundesstaat ein erforderlicher Eintrag ist.

1. Satz **[!UICONTROL Allow to Choose State if it is Optional for Country]** auf einen der folgenden Werte zu:

   `Yes` - In Ländern, in denen das Feld &quot;Bundesland&quot;nicht erforderlich ist, schließt das Feld Bundesland als optionalen Eintrag ein.

   `No` - In Ländern, in denen das Feld &quot;Bundesland&quot;nicht erforderlich ist, wird das Feld &quot;Bundesland&quot;weggelassen.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

Weitere Informationen zu den Statuskonfigurationsoptionen finden Sie unter [Konfigurationshandbuch](../configuration-reference/general/general.md#state-options).

## [!UICONTROL Country Options]

Die Länderoptionen geben an, in welchem Land sich Ihr Unternehmen befindet und aus welchem Land Sie die Zahlung annehmen.

### Festlegen der Länderoptionen für Ihren Store

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Im linken Navigationsbereich unter **[!UICONTROL General]** auswählen **[!UICONTROL General]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Country Options]** Abschnitt.

   >[!NOTE]
   >
   >Falls erforderlich, löschen Sie die **[!UICONTROL Use system value]** für jede Einstellung, die Sie ändern möchten.

   ![Allgemeine Konfiguration - Ländereinstellungen](./assets/general-country-options.png){width="700"}

1. Wählen Sie die **[!UICONTROL Default Country]** wo sich Ihr Unternehmen befindet.

1. Im **[!UICONTROL Allow Countries]** wählen Sie jedes Land aus, aus dem Sie Bestellungen annehmen.

   Standardmäßig sind alle Länder in der Liste ausgewählt. Um mehrere Länder auszuwählen, halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie auf jedes Element.

1. Verwenden Sie die **[!UICONTROL Zip/Postal Code is Optional for]** Liste, um jedes Land auszuwählen, in dem Sie Geschäfte tätigen, für das keine Postleitzahl oder Postleitzahl als Teil der Straßenanschrift erforderlich ist.

1. Im **[!UICONTROL European Union Countries]** wählen Sie jedes Land in der EU aus, in dem Sie tätig sind.

   Standardmäßig sind alle EU-Länder ausgewählt. Um die gewünschten Länder auszuwählen, halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie auf jedes Element.

1. Im **[!UICONTROL Top Destinations]** auswählen, wählen Sie die Primärländer aus, die Sie für den Verkauf als Ziel auswählen.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

### Festlegen der Länderoptionen für bestimmte Bereitstellungsmethoden

Sie können für jede verfügbare Option auch den Versand in bestimmte Länder konfigurieren [Versandmethode](../stores-purchase/delivery.md) (UPS, FedEx usw.).

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Navigationsbereich **[!UICONTROL Sales]** und wählen **[!UICONTROL Delivery Methods]**.

1. Wählen Sie den Versandunternehmen aus, auf den Sie bestimmte Länder anwenden möchten.

1. Für **[!UICONTROL Ship to Applicable Countries]**, deaktivieren Sie die **[!UICONTROL Use system value]** aktivieren und wählen Sie die **[!UICONTROL Specific Countries]** -Option.

1. Im **[!UICONTROL Top Destinations]** Liste die Primärländer auswählen, die Sie für den Versand auswählen.

   ![Beispiel für das Festlegen der Länderoptionen für die DHL-Versandmethode](./assets/country-options-for-specific-delivery-method.png){width="700"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

### Fehlerbehebung bei Ressourcen

Hilfe zur Fehlerbehebung bei Problemen mit der Länderkonfiguration finden Sie unter folgenden Themen: [!DNL Commerce] Knowledge Base-Artikel unterstützen:

- [Hinzufügen eines Landes](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/how-to/how-to-add-a-new-country-to-magento-2.html)
- [Die bereitgestellte countryId ist nicht vorhanden](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-15/mdva-33393-magento-patch-provided-countryid-does-not-exist.html)

## [!UICONTROL Merchant Location]

Die Einstellung &quot;Merchant Location&quot;wird zum Konfigurieren von [Zahlungsmethoden](../stores-purchase/payments.md). Wenn für diese Einstellung kein Wert vorhanden ist, wird die [Standardland](#uicontrol-country-options) verwendet wird.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Navigationsbereich **[!UICONTROL Sales]** und wählen **[!UICONTROL Payment Methods]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **Handelsplatz** auswählen. **[!UICONTROL Merchant Country]**.

   ![Standort des Ausführers festlegen](./assets/payment-methods-merchant-location.png){width="600"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

Weitere Informationen zu den Konfigurationsoptionen für Zahlungsmethoden finden Sie unter [Konfigurationshandbuch](../configuration-reference/sales/payment-methods.md).

## Währung

Währungseinstellungen - Definiert die Basis [currency](../stores-purchase/currency-configuration.md) und alle zusätzlichen Währungen, die als Zahlung akzeptiert werden. Stellt außerdem die Importverbindung und den Zeitplan her, die verwendet werden, um die Währungsraten automatisch zu aktualisieren.

Währungssymbole - Definiert die [Währungssymbole](../stores-purchase/currency-configuration.md#step-5-customize-currency-symbols-optional) die in Produktpreisen und Verkaufsunterlagen wie Bestellungen und Rechnungen aufgeführt sind. [!DNL Commerce] unterstützt Währungen aus über 200 Ländern auf der ganzen Welt.

Aktualisieren von Währungsraten - Währungskurse können [aktualisiert](../stores-purchase/currency-update.md) manuell oder nach Bedarf oder gemäß einem vordefinierten Zeitplan in Ihren Speicher importiert werden.

Währungsauswahl - Wenn mehrere Währungen verfügbar sind, wird die Variable [Währungsauswahl](../stores-purchase/currency.md) ist in der Kopfzeile des Stores verfügbar.

## [!UICONTROL Store Email Addresses]

Sie können über bis zu fünf verschiedene E-Mail-Adressen verfügen, die für jeden Store oder jede Ansicht unterschiedliche Funktionen oder Abteilungen darstellen. Neben den folgenden vordefinierten E-Mail-Identitäten gibt es einige benutzerdefinierte Identitäten, die Sie entsprechend Ihren Anforderungen einrichten können.

- Allgemeiner Kontakt
- Vertriebsmitarbeiter
- Kundensupport

Jede Identität und die zugehörige E-Mail-Adresse können bestimmten automatisierten E-Mail-Nachrichten zugeordnet werden und werden als Absender von E-Mail-Nachrichten angezeigt, die von Ihrem Store gesendet werden.

### Schritt 1: E-Mail-Adressen für Ihre Domäne einrichten

Bevor Sie E-Mail-Adressen für den Store konfigurieren können, muss jede als gültige E-Mail-Adresse für Ihre Domäne eingerichtet werden. Befolgen Sie die Anweisungen Ihres Serveradministrators oder E-Mail-Hosting-Anbieters, um jede erforderliche E-Mail-Adresse zu erstellen.

### Schritt 2: E-Mail-Adressen für Ihren Store konfigurieren

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. under **[!UICONTROL General]** Wählen Sie im linken Navigationsbereich die Option **[!UICONTROL Store Email Addresses]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL General Contact]** und führen Sie folgende Schritte aus:

   ![Allgemeine Konfiguration - E-Mail-Adressen speichern](./assets/store-email-addresses-general-contact.png){width="600"}

   - Für **[!UICONTROL Sender Name]** Geben Sie den Namen der Person ein, die mit der allgemeinen Kontaktidentität verknüpft ist, um als Absender von E-Mail-Nachrichten angezeigt zu werden.

   - Für **[!UICONTROL Sender Email]**, geben Sie die entsprechende E-Mail-Adresse ein.

1. Wiederholen Sie diesen Vorgang für jede Store-E-Mail-Adresse, die Sie verwenden möchten.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

### Schritt 3: Konfiguration der Verkaufs-E-Mail aktualisieren

Wenn Sie benutzerdefinierte E-Mail-Adressen verwenden, stellen Sie sicher, dass Sie die Konfiguration zugehöriger E-Mail-Nachrichten aktualisieren, damit die richtige Identität als Absender angezeigt wird.

1. Erweitern Sie im linken Navigationsbereich **[!UICONTROL Sales]** und wählen **[!UICONTROL Sales Emails]**.

   Die Seite verfügt über einen eigenen Abschnitt für jeden der folgenden Punkte:

   - Bestellkommentare
   - Rechnungen und Rechnungskommentare
   - Anmerkungen zu Versand und Versand
   - Kommentare zu Credit Memo und Credit Memo
   - RMA, RMA Authorization, RMA Admin Comments und RMA Customer Comments ![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce)

1. Einstieg in **[!UICONTROL Order]**, erweitern Sie den Bereich für jede Nachricht und stellen Sie sicher, dass der richtige Absender ausgewählt ist.

   ![Vertriebskonfiguration - Verkaufs-E-Mails](./assets/sales-emails-order.png){width="600"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

Weitere Informationen zu den Konfigurationsoptionen für E-Mails für Verkäufe finden Sie in der [_Konfigurationshandbuch_](../configuration-reference/sales/sales-emails.md).

## Kontaktformular

Die _Kontakt_ -Link in der Fußzeile des Stores ist eine einfache Möglichkeit für Kunden, mit Ihnen in Kontakt zu bleiben. Kunden können das Formular ausfüllen, um eine Nachricht an Ihren Store zu senden. Ein Standard [!DNL Commerce] Installation zeigt die Standardeinstellung an _Kontakt_ Formular. Nach dem Senden des Formulars wird eine Dankesmeldung angezeigt

Es ist wichtig zu verstehen, dass das standardmäßige Kontaktformular direkt aus dem Code und nicht aus einer CMS-Seite gerendert wird.

![Standardseite &quot;Kontakt&quot;](./assets/page-contact-us-default.png){width="700"}

Die Fußzeile des Stores enthält einen Link zur Seite Kontakt , die im gesamten Store verfügbar ist.

![Link in der Fußzeile](./assets/storefront-footer-contact-us.png){width="700"}

Die Luma-Beispieldaten enthalten zusätzliche Informationen auf der Seite Kontakt , die zeigt, wie Sie die Seite für Ihren Store anpassen können.

![Kontaktseite](./assets/storefront-contact-us.png){width="700"}

### Kontaktformular konfigurieren

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Im linken Navigationsbereich unter **[!UICONTROL General]** auswählen **[!UICONTROL Contacts]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Contact Us]** Abschnitt und Satz **[!UICONTROL Enable Contact Us]** nach `Yes`.

   ![Allgemeine Konfiguration - Kontakt](./assets/contacts-contact-us.png){width="600"}

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Email Options]** und legen Sie die E-Mail-Kontaktoptionen fest:

   ![Allgemeine Konfiguration - E-Mail-Optionen](./assets/contacts-email-options.png){width="600"}

   - Für **[!UICONTROL Send Emails to]** Geben Sie die E-Mail-Adresse ein, an die Nachrichten aus dem Kontaktformular gesendet werden.

   - Satz **[!UICONTROL Email Sender]** zur Store-Identität, die als Absender der Nachricht aus dem Kontaktformular angezeigt wird. Beispiel: Benutzerdefinierte E-Mail 2.

   - Satz **[!UICONTROL Email Template]** der Vorlage, die für vom Kontaktformular gesendete Nachrichten verwendet wird.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

### Inhalt anpassen

Sie können den Inhalt im _Kontakt_ Formular an die Anforderungen Ihrer Store- und Kundendienstrichtlinien anzupassen.

### Methode 1: Verwendung von Beispieldaten

Die Luma-Beispieldaten enthalten eine _Kontaktinformationen_ -Block, der für Ihren Store angepasst werden kann. Die `contact-us-info` [block](../content-design/blocks.md) kann einfach geändert werden, um eigene Inhalte zur Kontaktseite hinzuzufügen.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.

1. Suchen Sie die **[!UICONTROL Contact Us Info]** -Block in der Liste ein und öffnen Sie **[!UICONTROL Edit]** -Modus.

   ![Block &quot;Kontaktinformationen&quot;](./assets/content-block-contact-us-info.png){width="700"}

1. Klicken Sie unten auf der Blockseite auf **[!UICONTROL Edit with Page Builder]**.

   ![Inhaltsbaustein - Beispiel kontaktieren](./assets/content-block-contact-us-content.png){width="700"}

   >[!NOTE]
   >
   >Wenn Sie [[!DNL Page Builder] disabled](../page-builder/setup.md#disable-dnl-page-builder), können Sie den Editor [toolbar](../content-design/editor.md) , um den Text zu formatieren, und hinzufügen [images](../content-design/editor-insert-image.md) und [links](../content-design/editor-insert-link.md).

1. Bewegen Sie den Mauszeiger über den HTML-Container, um die Toolbox anzuzeigen und die _Einstellungen_ ( ![Symbol Einstellungen](../page-builder/assets/pb-icon-settings.png) ).

1. Bearbeiten Sie den HTML-Code, um die Kontaktinformationen für Ihren Store anzugeben, und klicken Sie auf **[!UICONTROL Save]**.

   ![Inhaltsbaustein - HTML-Code bearbeiten](./assets/content-block-contact-us-html.png){width="700"}

1. Beenden Sie die [!DNL Page Builder] Bühne und Klicken **[!UICONTROL Save Block]**.

### Methode 2: Ohne Beispieldaten

>[!IMPORTANT]
>
>Ab Version 2.4.0 kann das Kontaktformular nicht mehr in einem CMS-Block oder einer CMS-Seite aufrufen. Die Anpassung des Kontaktformulars sollte mit der Layout-XML oder benutzerdefinierten Designvorlagen erfolgen.

Standardmäßig greifen Käufer über die _Kontaktlink_ in der Fußzeile der Storefront-Seiten. Weiterführende Informationen zur Anpassung der Kontaktseite finden Sie im Abschnitt [Frontend-Entwicklerhandbuch][theme-guide].

[theme-guide]: https://developer.adobe.com/commerce/frontend-core/guide/themes/
