---
title: '[!DNL Google Tag Manager]'
description: Erfahren Sie, wie Sie  [!DNL Google Tag Manager]  verwenden, um die vielen Tags (Codeausschnitte) zu verwalten, die mit Ihren Marketing-Kampagnenereignissen auf Ihren Adobe Commerce-Sites verbunden sind.
exl-id: 9c24239b-9efd-42ee-9b99-5a194f3c4347
feature: Marketing Tools, Integration
source-git-commit: 22a619db0b0673dc520b9bdc5d6cd0c8ffecdf08
workflow-type: tm+mt
source-wordcount: '1459'
ht-degree: 0%

---

# [!DNL Google Tag Manager]

{{ee-feature}}

[!DNL Google Tag Manager] ist ein leistungsstarkes Tool, mit dem Sie verschiedene Tags (Code-Ausschnitte), die mit Ihren Marketing-Kampagnenereignissen verknüpft sind, effizient verwalten und bereitstellen können. [!DNL Google Tag Manager] bietet Ihnen die Möglichkeit, Tracking-Tags zu Ihrer Site hinzuzufügen, um die Zielgruppe zu messen oder Marketing-Initiativen für Suchmaschinen zu personalisieren, erneut anzusprechen oder durchzuführen.

[!DNL Google Tag Manager] überträgt Daten und Ereignisse direkt an [!DNL Google Analytics], Enhanced E-Commerce und andere Analyselösungen von Drittanbietern, um ein klares Bild davon zu erhalten, wie gut Ihre Site, Produkte und Promotions funktionieren.

Sie sollten über ein [!DNL Google Analytics] und ein [!DNL Tag Manager] Konto verfügen, um diesen Prozess fortzusetzen. Die folgende Anleitung führt Sie durch die Konfiguration Ihrer Google-Konten, die Konfiguration Ihrer Commerce-Geschäft und die Erstellung einer Tag.

>[!NOTE]
>
>Wenn Ihr Unternehmen Datenschutzbestimmungen wie der [Datenschutz-Grundverordnung](../getting-started/compliance-gdpr.md) und/oder dem [California Consumer Privacy Act“ unterliegt](../getting-started/compliance-ccpa.md) finden Sie weitere Informationen unter [Datenschutzeinstellungen von Google](google-tools.md#google-privacy-settings).

## Schritt 1. Konfigurieren des [!DNL Google Analytics]

Siehe [Einrichten der Site-Suche](https://support.google.com/analytics/answer/1012264) in der Hilfe zu Google für die Grundlagen, die Sie für die ersten Schritte benötigen. Siehe auch die Google-Handbücher für [Google Analytics](https://support.google.com/analytics/answer/9304153) und [Google Tag Manager](https://support.google.com/tagmanager/answer/6102821).

1. Sign in to your [!DNL Google Analytics] account.

1. Gehen Sie wie folgt vor, um **[!UICONTROL Internal Site Search Tracking]** zu aktivieren:

   - Navigate to **[!UICONTROL Select View]** > **[!UICONTROL View Settings]**.

   - Legen Sie **[!UICONTROL Site Search Tracking]** auf `On` fest.

   - Set **[!UICONTROL Query]** parameter to `q`.

   - When complete, **[!UICONTROL Save]** the settings.

1. Gehen Sie wie folgt vor, um Anzeigefunktionen zu aktivieren:

   - Wählen Sie **[!UICONTROL Property Settings]**.

   - Legen Sie unter _[!UICONTROL Advertising Features]_**[!UICONTROL Enable Demographics and Interest Reports]**auf `On` fest.

   - **[!UICONTROL Save]** der Einstellungen.

1. Gehen Sie wie folgt vor, um das E-Commerce-Tracking zu aktivieren:

   - Navigieren Sie zu **[!UICONTROL Select View]** > **[!UICONTROL Ecommerce Settings]**.

   - **[!UICONTROL Enable Ecommerce]** Festlegen bis `On`.

   - **[!UICONTROL Enable Enhanced Ecommerce Reporting]** Festlegen bis `On`.

   - **[!UICONTROL Save]** die Einstellungen geändert haben.

1. Laden Sie die Seite neu und überprüfen Sie, ob alle Einstellungen erhalten bleiben `On`.

   >[!NOTE]
   >
   >Wenn nicht alle Einstellungen vorhanden sind `On`, wiederholen Sie die vorherigen Schritte, speichern Sie und neu laden Sie die Seite. Wiederholen Sie diesen Vorgang, bis alle Einstellungen auf eingestellt sind.`On`

## Schritt 2. Konfigurieren der [!DNL Google Tag Manager] Konto

Die folgende Anleitung zeigt, wie Sie eine neue Container mit den Grundeinstellungen konfigurieren. Zur Vereinfachung des Vorgangs wird eine Composer-Konfigurationsdatei [](https://developer.adobe.com/commerce/php/development/composer/) (.json) verwendet, die importiert wird, um eine Tag in einer neuen Container zu generieren. Für dieses Beispiel empfiehlt es sich, eine Container zu erstellen, anstatt eine vorhandene Container zu ändern.

>[!NOTE]
>
>Weitere Informationen finden Sie unter Container-Export und -Import](https://support.google.com/tagmanager/answer/6106997) von Google[. Diese Anweisungen enthalten eine schrittweise Anleitung zum Importieren eines JSON-Beispiels in eine neue Container.

1. Laden Sie die verknüpfte Datei [GTM_M2_Config_json.txt](./assets/GTM_M2_Config_json.txt) herunter, öffnen Sie die Datei in einem Bearbeiter und speichern Sie sie als `GTM_M2_Config.json`.

   Die JSON-Datei wird direkt in [!DNL Google Tag Manager]hochgeladen.

1. Navigieren Sie zu **[!UICONTROL Admin]** > **[!UICONTROL Container]** > **[!UICONTROL Import Container]**.

1. Klicken Sie auf **[!UICONTROL Choose container file]** die JSON-Datei und wählen Sie sie aus.

1. Klicken Sie unter **[!UICONTROL Choose workspace]** auf **[!UICONTROL New]**.

1. Geben Sie einen Titel und eine Beschreibung ein und klicken Sie dann auf **[!UICONTROL Save]**.

1. Wählen Sie zum Importieren der Datei eine der folgenden Aktionen aus:

   - Die **[!UICONTROL Overwrite]** Option sollte für eine neue Container ausgewählt werden.

   - Diese **[!UICONTROL Merge]** Option sollte ausgewählt werden, wenn Sie ein vorhandenes Container verwenden.

1. Klicken Sie **[!UICONTROL Preview]** , um die Tags, Auslöser und Variablen zu überprüfen.

1. Gehen Sie wie folgt vor, um die **[!UICONTROL Google Analytics ID]** in Variablen referenzierten Variablen zu bearbeiten:

   - Navigieren Sie zu **[!UICONTROL Variables]** > **[!UICONTROL User-Defined Variables]**.

   - Wählen Sie den Platzhalter (`UA-xxxxxx-x`) aus und aktualisieren Sie **[!UICONTROL Google Analytics]** ihn mit Ihrem eigenen **[!UICONTROL GA ID]**.

1. Folgen Sie den Anweisungen von Google, um der neuen Container Tags, Trigger und Variablen hinzuzufügen.

   Wenn Sie Einstellungen in einer anderen Container haben, die Sie verwenden möchten, können diese in die neue Container verschoben werden.

1. Klicken Sie auf die Schaltfläche, wenn Sie **[!UICONTROL Confirm]** fertig sind.

1. Befolgen Sie die Anweisungen von Google zum Veröffentlichen der neuen Container.

## Schritt 3. Konfigurieren Sie Ihre Geschäft

{{gtag-api-note}}

1. Melden Sie sich beim Administrator Ihres Commerce-Geschäft an.

1. Wechseln Sie in der _Admin-Seitenleiste_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich, und **[!UICONTROL Sales]** wählen Sie **[!UICONTROL Google API]** aus.

1. ![Erweitern Erweiterung Selektor](../assets/icon-display-expand.png) den **[!UICONTROL Google Analytics]** Abschnitt und konfigurieren Sie Folgendes:

   ![Vertriebskonfiguration – Google Analytics](../configuration-reference/sales/assets/google-api-analytics-tag-manager.png){width="600" zoomable="yes"}

   - **[!UICONTROL Enable]** Festlegen bis `Yes`.

   - **[!UICONTROL Account type]** Festlegen bis `Google Tag Manager`.

   - Geben Sie in das **[!UICONTROL Container ID]** Feld Ihre GTM-ID ein (`GTM-xxxxxx`).

   - Wenn Sie Google Analytics auch zum Inhalte von Experimenten verwenden, legen **Sie Inhaltsexperimente** aktivieren auf `Yes`fest.

   - Verwenden Sie die Standardwerte für die verbleibenden Felder.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

1. Testen Sie Ihre [!DNL Google Tag Manager] und stellen Sie sicher, dass alles korrekt funktioniert.

>[!NOTE]
>
>Jeder Container ist einer Website zugeordnet und Sie benötigen nur einen Container pro Konto. Wenn Sie über eine Commerce-Instanz mit mehreren Sites verfügen, benötigen Sie separate Container.

## Feldbeschreibungen

| Feld | Umfang | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable] | Shop-Ansicht | Legt fest, ob Google Analytics Enhanced E-Commerce zur Analyse der Aktivitäten in Ihrem Store verwendet werden kann. Optionen: `Yes` / `No` |
| [!UICONTROL Account type] | Shop-Ansicht | Determines the Google tracking code that is used to monitor store activity and traffic. Optionen: `Google Analytics` / `Google Tag Manager` |
| [!UICONTROL Anonymize IP] | Shop-Ansicht | Determines if identifying information is removed from IP addresses that appear in Google Analytics results. |
| [!UICONTROL Enable Content Experiments] | Shop-Ansicht | Aktiviert Google-Inhaltsexperimente, mit denen bis zu zehn verschiedene Versionen derselben Seite getestet werden können. Optionen: `Yes` / `No` |
| [!UICONTROL Container Id] | Shop-Ansicht | Wenn [!DNL Google Tag Manager] bereits für Ihren Store installiert und konfiguriert ist, wird die Container-ID automatisch in diesem Feld angezeigt. |
| [!UICONTROL List property for the catalog page] | Shop-Ansicht | Identifiziert die Tag-Manager-Eigenschaft, die mit der Katalogseite verknüpft ist. Standardwert: `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | Store Ansicht | Gibt den Tag-Manager-Eigenschaft an, der dem Crosssell Block zugeordnet ist. Standardwert: `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | Store Ansicht | Gibt die Tag-Manager-Eigenschaft an, die mit dem Upsell-Block verbunden sind. Standardwert: `Up-sell` |
| [!UICONTROL List property for the related products block] | Store Ansicht | Identifies the Tag Manager property associated with the related products block. Standardwert: `Related Products` |
| [!UICONTROL List property for the search results page] | Shop-Ansicht | Identifies the Tag Manager property associated with the search results page. Standardwert: `Search Results` |
| [!UICONTROL "Internal Promotions" for promotions field "Label"] | Shop-Ansicht | Identifiziert die Tag-Manager-Eigenschaft, die mit den Kennzeichnungen für interne Promotions verknüpft ist. Standardwert: `Label` |

{style="table-layout:auto"}

## Erstellen eines Tags zum Tracking von Konversionen

Wenn Sie über ein Google AdWords-Konto verfügen, können Sie ein Tag erstellen, mit dem Konversionen verfolgt werden. Das folgende Beispiel zeigt, wie Sie sowohl [!DNL Google Tag Manager] als auch [!DNL Google Analytics] verwenden, um ein Tag zu erstellen, das auf der Konversionsseite _Shops ausgelöst_.

### Schritt 1. Erstellen einer Tag

1. Melden Sie sich bei Ihrem [!DNL Google Tag Manager] Konto an und klicken Sie auf den verknüpfen für die Container, die Sie für Ihre Geschäft erstellt haben.

1. Klicken Sie im **[!UICONTROL New Tag]** Feld auf .**[!UICONTROL Add a new tag]**

1. Rufen Sie folgende Informationen aus Ihrem AdWords-Konto ab:

   - Konversions-ID
   - Umrechnungs-Kennzeichnen

   Wenn Sie Hilfe benötigen, Visit Sie die Support-Website](https://support.google.com/tagmanager/answer/6105160) von [Google.

1. Klicken Sie im [!DNL Google Tag Manager] Dashboard und führen Sie **[!UICONTROL Google AdWords]** folgende Schritte aus:

   - Klicken Sie auf den Platzhalter für den Titel und geben Sie einen Namen für die neue Tag ein.

   - Wählen Sie unter **[!UICONTROL Choose Product]** die Option **[!UICONTROL Google AdWords]** aus.

   - Wählen Sie unter _[!UICONTROL Choose a Tag Type]_aus, und **[!UICONTROL AdWords Conversion Tracking]**klicken Sie auf **[!UICONTROL Continue]**.

1. Geben Sie in Ihrer AdWords-Konto und **[!UICONTROL Conversion ID]** **[!UICONTROL Conversion Label]** klicken Sie auf **[!UICONTROL Continue]**.

### Schritt 2. Erstellen einer Regel

Vom Dashboard ausgehend [!DNL Google Tag Manager] besteht der nächste Schritt darin, eine Regel zu erstellen, die das Tag auf der Konversion Seite auslöst.

1. Klicken Sie unter **[!UICONTROL Fire On]** auf **[!UICONTROL Some Pages]**.

1. Nehmen Sie in diesem _[!UICONTROL Choose Pages]_Abschnitt die folgenden Einstellungen vor:

   - **[!UICONTROL Name]** - Geben Sie einen Namen für die Seite Beschreibung ein.

   - **[!UICONTROL Variable]** `url`

   - **Bedienung** - `matches RegEx`

     Weitere Informationen finden Sie unter [Regex- und CSS-Selektor-Operatoren](https://support.google.com/tagmanager/answer/7679109) im Google Tag Manager-Hilfe.

   - **[!UICONTROL Value]** - `checkout/success.*`

1. Aktivieren Sie das grüne Kontrollkästchen und klicken Sie auf **[!UICONTROL Save]**.

   Der Auslöser, den Sie eingerichtet haben, wird als blaues Button im Abschnitt &quot;Feuer ein&quot; angezeigt.

1. Klicken Sie abschließend auf **[!UICONTROL Save Tag]**.

### Schritt 3. Vorschau und Veröffentlichung

Der nächste Schritt im Prozess besteht in der Vorschau des Tags. Bei jeder Vorschau des Tags wird ein Schnappschuss der Version gespeichert. Wenn Sie mit den Ergebnissen zufrieden sind, wechseln Sie zur Version, die Sie verwenden möchten, und klicken Sie auf **[!UICONTROL Publish]**.

## Benutzerdefiniertes HTML-Tag mit JavaScript

In diesem Abschnitt wird erläutert, wie Sie eine CSP-Nonce zum benutzerdefinierten HTML Tag JavaScript hinzufügen, um sie auf der Kaufseite auszuführen und so die Einhaltung der Anforderungen der Content Security Policy (CSP) sicherzustellen. Dieser Zusatz erhöht die Sicherheit der Site, indem er die Ausführung nicht autorisierter Skripte verhindert. Weitere Informationen finden Sie in der Dokumentation [Content Security Policy](https://developer.adobe.com/commerce/php/development/security/content-security-policies) .

>[!NOTE]
>
>Der Import der globalen `cspNonce`-Variablen in Google Tag Manager wird nur ab Adobe Commerce-Version 2.4.8 unterstützt.

>[!WARNING]
>
>Das Hinzufügen unbekannter Skripte zu Ihrem Store kann das Risiko von Datenkompromittierungen bergen. Skripte, die auf der Checkout-Seite autorisiert sind, können vertrauliche Kundeninformationen, einschließlich Zahlungsdetails, stehlen. Sie müssen unbedingt Vorsichtsmaßnahmen treffen, um Ihr Google Tag Manager-Konto zu schützen. Fügen Sie nur vertrauenswürdige Skripte hinzu, überprüfen Sie Ihre Tags regelmäßig und implementieren Sie strenge Sicherheitsmaßnahmen wie Zwei-Faktor-Authentifizierung (2FA) und Zugriffssteuerung.

### Schritt 1. Create a CSP Nonce Variable

You can create a CSP Nonce Variable that can be used within your Google Tag Manager by importing the variable configuration or configuring it manually.

#### Import the variable configuration

The CSP Nonce Variable is included in the example container [GTM_M2_Config_json.txt](./assets/GTM_M2_Config_json.txt). Sie können die Variable erstellen, indem Sie diesen Code in Ihre Arbeitsbereich importieren.

#### Variable manuell erstellen

Wenn Sie die Variablenkonfiguration nicht importieren können, führen Sie die folgenden Schritte aus, um sie zu erstellen.

1. Navigieren Sie in Ihrem Arbeitsbereich zum Abschnitt **Variablen** in der Seitenleiste.
1. Klicken Sie auf **Neu** Schaltfläche unten auf der Seite im Abschnitt **Benutzerdefinierte Variablen** .
1. Benennen Sie die Variable `gtmNonce`.
1. Klicken Sie auf das Stiftsymbol, um die Variable zu bearbeiten.
1. Wählen Sie **JavaScript** aus dem Abschnitt **Seitenvariable** aus.
1. Geben Sie **Feld „Globaler**&quot; `window.cspNonce` ein.
1. Speichern Sie die Variable.

Weitere Informationen zu [Google Tag Manager-Variablen](https://support.google.com/tagmanager/answer/7683056?hl=en) finden Sie unter [Benutzerdefinierte Variablentypen für das Web](https://support.google.com/tagmanager/answer/7683362?hl=en) in der Dokumentation zu Google. Diese Dokumentation bietet detaillierte Anleitungen zum Erstellen und Verwalten benutzerdefinierter Variablen, um Ihr Tag-Management auf spezifische Marketing- und Analyseanforderungen anzupassen.

### Schritt 2. Erstellen eines benutzerdefinierten HTML-Tags

1. In your workspace, navigate to the **Tags** section in the sidebar.
1. Click the **New** button.
1. In the **Tag Configuration** section, select **Custom HTML Tag**.
1. Enter your required JavaScript in the text area, and add a nonce attribute to the opening `<script>` tag that points to the variable you created in the previous step. Beispiel:

   ```html
   <script nonce="{{gtmNonce}}">
       // Your JavaScript code here
   </script>
   ```

1. Wählen Sie **Support document.write** aus.
1. Wählen Sie **Abschnitt** den gewünschten Trigger aus. Beispiel: **Einverständnisinitialisierung - Alle Seiten**.

Weitere Informationen zu [Tags](https://support.google.com/tagmanager/answer/3281060) im Tag-Manager von Google finden Sie unter [Benutzerdefinierte Tags](https://support.google.com/tagmanager/answer/6107167) in der Dokumentation zu Google.
