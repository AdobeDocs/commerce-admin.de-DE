---
title: '[!DNL Google Tag Manager]'
description: Verwendung von [!DNL Google Tag Manager] um die vielen Tags (Codefragmente) zu verwalten, die mit Ihren Marketingkampagnenereignissen auf Ihren Adobe Commerce-Sites in Verbindung stehen.
exl-id: 9c24239b-9efd-42ee-9b99-5a194f3c4347
feature: Marketing Tools, Integration
source-git-commit: 7384481d1a4a2a04882d4c99448cca75abc9be31
workflow-type: tm+mt
source-wordcount: '1161'
ht-degree: 0%

---

# [!DNL Google Tag Manager]

{{ee-feature}}

[!DNL Google Tag Manager] hilft Ihnen bei der Verwaltung der vielen Tags (Codefragmente), die mit Ihren Marketing-Kampagnenereignissen verbunden sind. [!DNL Google Tag Manager] bietet Ihnen die Möglichkeit, Tracking-Tags zu Ihrer Site hinzuzufügen, um die Zielgruppe zu messen oder Suchmaschinen-Marketing-Initiativen zu personalisieren, erneut auszurichten oder durchzuführen.

[!DNL Google Tag Manager] übermittelt Daten und Ereignisse direkt an [!DNL Google Analytics], Enhanced E-Commerce und andere Analytics-Lösungen von Drittanbietern, um ein klares Bild davon zu erhalten, wie gut Ihre Site, Produkte und Promotions funktionieren.

Sie sollten eine [!DNL Google Analytics] und [!DNL Tag Manager] , um diesen Prozess fortzusetzen. Die folgenden Anweisungen führen Sie durch den Prozess der Konfiguration Ihrer Google-Konten, der Konfiguration Ihres Commerce-Stores und der Erstellung eines Tags.

>[!NOTE]
>
>Wenn Ihr Unternehmen Datenschutzbestimmungen wie die [Die Datenschutz-Grundverordnung](../getting-started/compliance-gdpr.md) und/oder [California Consumer Privacy Act](../getting-started/compliance-ccpa.md), siehe [Google-Datenschutzeinstellungen](google-tools.md#google-privacy-settings).

## Schritt 1. Konfigurieren Sie Ihre [!DNL Google Analytics] account

Siehe [Site-Suche einrichten](https://support.google.com/analytics/answer/1012264) in der Google-Hilfe zu den Grundlagen für die ersten Schritte. Weitere Informationen finden Sie in den Google-Handbüchern für [Google Analytics](https://support.google.com/analytics/answer/9304153) und [Google Tag Manager](https://support.google.com/tagmanager/answer/6102821).

1. Anmelden bei [!DNL Google Analytics] -Konto.

1. Aktivieren **[!UICONTROL Internal Site Search Tracking]** führen Sie folgende Schritte aus:

   - Navigieren Sie zu **[!UICONTROL Select View]** > **[!UICONTROL View Settings]**.

   - Satz **[!UICONTROL Site Search Tracking]** nach `On`.

   - Satz **[!UICONTROL Query]** Parameter auf `q`.

   - Wenn abgeschlossen, **[!UICONTROL Save]** die Einstellungen.

1. Gehen Sie wie folgt vor, um Anzeigefunktionen zu aktivieren:

   - Auswählen **[!UICONTROL Property Settings]**.

   - under _[!UICONTROL Advertising Features]_, set **[!UICONTROL Enable Demographics and Interest Reports]**nach `On`.

   - **[!UICONTROL Save]** die Einstellungen.

1. Gehen Sie wie folgt vor, um das E-Commerce-Tracking zu aktivieren:

   - Navigieren Sie zu **[!UICONTROL Select View]** > **[!UICONTROL Ecommerce Settings]**.

   - Satz **[!UICONTROL Enable Ecommerce]** nach `On`.

   - Satz **[!UICONTROL Enable Enhanced Ecommerce Reporting]** nach `On`.

   - **[!UICONTROL Save]** die Einstellungen.

1. Laden Sie die Seite neu und stellen Sie sicher, dass alle Einstellungen beibehalten werden. `On`.

   >[!NOTE]
   >
   >Wenn nicht alle Einstellungen `On`, wiederholen Sie die vorherigen Schritte, speichern und laden Sie die Seite neu. Wiederholen Sie diesen Vorgang, bis alle Einstellungen auf `On`.

## Schritt 2. Konfigurieren Sie Ihre [!DNL Google Tag Manager] account

Die folgenden Anweisungen zeigen, wie Sie einen neuen Container mit den grundlegenden Einstellungen konfigurieren. Beispiel [Verfasser](https://developer.adobe.com/commerce/php/development/composer/) -Konfigurationsdatei (.json) wird verwendet, um den Prozess zu vereinfachen und zum Generieren eines Tags in einem neuen Container zu importieren. Für dieses Beispiel wird empfohlen, einen Container zu erstellen, anstatt einen vorhandenen Container zu ändern.

>[!NOTE]
>
>Weitere Informationen finden Sie unter Google [Containerexport und -import](https://support.google.com/tagmanager/answer/6106997). Diese Anweisungen bieten eine schrittweise Anleitung zum Importieren einer JSON-Musterdatei in einen neuen Container.

1. Verknüpfte Datei herunterladen [GTM_M2_Config_json.txt](./assets/GTM_M2_Config_json.txt), öffnen Sie die Datei in einem Editor und speichern Sie sie als `GTM_M2_Config.json`.

   Die JSON-Datei wird direkt in [!DNL Google Tag Manager].

1. Navigieren Sie zu **[!UICONTROL Admin]** > **[!UICONTROL Container]** > **[!UICONTROL Import Container]**.

1. Klicks **[!UICONTROL Choose container file]** und wählen Sie die JSON-Datei aus.

1. under **[!UICONTROL Choose workspace]** klicken **[!UICONTROL New]**.

1. Geben Sie einen Titel und eine Beschreibung ein und klicken Sie auf **[!UICONTROL Save]**.

1. Wählen Sie einen der folgenden Schritte aus, um die Datei zu importieren:

   - Die **[!UICONTROL Overwrite]** sollte für einen neuen Container ausgewählt werden.

   - Die **[!UICONTROL Merge]** sollte ausgewählt werden, wenn Sie einen vorhandenen Container verwenden.

1. Klicks **[!UICONTROL Preview]** , um die Tags, Trigger und Variablen zu überprüfen.

1. So bearbeiten Sie die **[!UICONTROL Google Analytics ID]** die in Variablen referenziert wird, gehen Sie wie folgt vor:

   - Navigieren Sie zu **[!UICONTROL Variables]** > **[!UICONTROL User-Defined Variables]**.

   - Auswählen **[!UICONTROL Google Analytics]** und aktualisieren Sie den Platzhalter (`UA-xxxxxx-x`) mit eigenen **[!UICONTROL GA ID]**.

1. Befolgen Sie die Anweisungen von Google zum Hinzufügen von Tags, Triggern und Variablen zum neuen Container.

   Wenn Sie Einstellungen in einem anderen Container haben, den Sie verwenden möchten, können sie in den neuen Container verschoben werden.

1. Klicks **[!UICONTROL Confirm]** wenn abgeschlossen.

1. Befolgen Sie die Anweisungen von Google zum Veröffentlichen des neuen Containers.

## Schritt 3. Konfigurieren des Stores

{{gtag-api-note}}

1. Melden Sie sich bei Admin Ihres Commerce-Stores an.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen **[!UICONTROL Google API]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Google Analytics]** und konfigurieren Sie Folgendes:

   ![Vertriebskonfiguration - Google Analytics](../configuration-reference/sales/assets/google-api-analytics-tag-manager.png){width="600" zoomable="yes"}

   - Satz **[!UICONTROL Enable]** nach `Yes`.

   - Satz **[!UICONTROL Account type]** nach `Google Tag Manager`.

   - Im **[!UICONTROL Container ID]** Geben Sie Ihre GTM-ID (`GTM-xxxxxx`).

   - Wenn Sie auch Google Analytics für Inhaltsexperimente verwenden, legen Sie **Aktivieren von Inhaltsexperimenten** nach `Yes`.

   - Verwenden Sie die Standardwerte für die übrigen Felder.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

1. Testen [!DNL Google Tag Manager] und überprüfen Sie, ob alles ordnungsgemäß funktioniert.

>[!NOTE]
>
>Jeder Container ist mit einer Website verknüpft und Sie benötigen nur einen Container pro Konto. Wenn Sie über eine Commerce-Instanz mit mehreren Sites verfügen, benötigen Sie separate Container.

## Schritt 4. Fügen Sie Ihrem Adobe Commerce-Store den GTM-Code hinzu.

1. Um den GTM-Code zu kopieren, gehen Sie zu **[!UICONTROL Admin]** > **[!UICONTROL Install Google Tag Manager]**.

   Es gibt zwei GTM-Code-Snippets, die zu Ihrer Commerce-Site hinzugefügt werden: das erste für die `<head>` -Tag und die zweite für `<body>` -Tag.

1. Wechseln Sie im Commerce Admin zu **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**und öffnen Sie die Store-Ansicht im Bearbeitungsmodus.

1. under _[!UICONTROL Other Settings]_, erweitern **[!UICONTROL HTML Head]**und fügen Sie den Code ein, den Sie aus GTM für die `<head>` -Tag im **[!UICONTROL Scripts and Style Sheets]**-Feld.

   ![Einfügen von Code in die HTML-Kopfzeile](./assets/head-tag.png){width="600" zoomable="yes"}

1. Erweitern **[!UICONTROL Footer]** und fügen Sie den GTM-Code für `<body>` im **[!UICONTROL Miscellaneous HTML]** -Feld.

   ![Einfügen von Code in die Fußzeile](./assets/footer-tag-section.png){width="600" zoomable="yes"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Configuration]**.

## Feldbeschreibungen

| Feld | Anwendungsbereich | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable] | Store-Ansicht | Bestimmt, ob Google Analytics Enhanced E-Commerce zur Analyse von Aktivitäten in Ihrem Store verwendet werden kann. Optionen: `Yes` / `No` |
| [!UICONTROL Account type] | Store-Ansicht | Bestimmt den Google-Trackingcode, der zur Überwachung von Store-Aktivitäten und -Traffic verwendet wird. Optionen: `Google Analytics` / `Google Tag Manager` |
| [!UICONTROL Anonymize IP] | Store-Ansicht | Bestimmt, ob Identifizierungsinformationen aus IP-Adressen entfernt werden, die in Google Analytics-Ergebnissen angezeigt werden. |
| [!UICONTROL Enable Content Experiments] | Store-Ansicht | Aktiviert Google Content Experiments, mit denen bis zu zehn verschiedene Versionen derselben Seite getestet werden können. Optionen: `Yes` / `No` |
| [!UICONTROL Container Id] | Store-Ansicht | Wenn [!DNL Google Tag Manager] bereits für Ihren Store installiert und konfiguriert ist, wird die Container-ID automatisch in diesem Feld angezeigt. |
| [!UICONTROL List property for the catalog page] | Store-Ansicht | Gibt die Tag-Manager-Eigenschaft an, die mit der Katalogseite verknüpft ist. Standardwert: `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | Store-Ansicht | Identifiziert die Tag-Manager-Eigenschaft, die mit dem Querverkaufsblock verknüpft ist. Standardwert: `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | Store-Ansicht | Identifiziert die Tag-Manager-Eigenschaft, die mit dem Upsell-Block verknüpft ist. Standardwert: `Up-sell` |
| [!UICONTROL List property for the related products block] | Store-Ansicht | Identifiziert die Tag-Manager-Eigenschaft, die mit dem zugehörigen Produktblock verknüpft ist. Standardwert: `Related Products` |
| [!UICONTROL List property for the search results page] | Store-Ansicht | Identifiziert die Tag-Manager-Eigenschaft, die mit der Suchergebnisseite verknüpft ist. Standardwert: `Search Results` |
| [!UICONTROL "Internal Promotions" for promotions field "Label"] | Store-Ansicht | Identifiziert die Tag-Manager-Eigenschaft, die mit den Bezeichnungen für interne Promotions verknüpft ist. Standardwert: `Label` |

{style="table-layout:auto"}

## Erstellen eines Tags zum Verfolgen von Konversionen

Wenn Sie über ein Google AdWords-Konto verfügen, können Sie ein Tag erstellen, das Konversionen verfolgt. Das folgende Beispiel zeigt, wie Sie beide [!DNL Google Tag Manager] und [!DNL Google Analytics] , um ein Tag zu erstellen, das bei der Konversion Ihres Stores ausgelöst wird. _Erfolg_ Seite.

### Schritt 1. Tag erstellen

1. Melden Sie sich bei Ihrer [!DNL Google Tag Manager] und klicken Sie auf den Link für den Container, den Sie für Ihren Store erstellt haben.

1. Im **[!UICONTROL New Tag]** Feld, klicken Sie auf **[!UICONTROL Add a new tag]**.

1. Rufen Sie die folgenden Informationen aus Ihrem AdWords-Konto ab:

   - Konversions-ID
   - Konversionsbezeichnung

   Wenn Sie Hilfe benötigen, besuchen Sie Googles [Support-Site](https://support.google.com/tagmanager/answer/6105160).

1. Aus dem [!DNL Google Tag Manager] Dashboard, klicken Sie auf **[!UICONTROL Google AdWords]** und gehen Sie wie folgt vor:

   - Klicken Sie auf den Platzhalter für den Titel und geben Sie einen Namen für das neue Tag ein.

   - under **[!UICONTROL Choose Product]** auswählen **[!UICONTROL Google AdWords]**.

   - under _[!UICONTROL Choose a Tag Type]_auswählen **[!UICONTROL AdWords Conversion Tracking]**und klicken **[!UICONTROL Continue]**.

1. Geben Sie die **[!UICONTROL Conversion ID]** und **[!UICONTROL Conversion Label]** aus Ihrem AdWords-Konto aus und klicken Sie auf **[!UICONTROL Continue]**.

### Schritt 2. Erstellen einer Regel

Fortsetzung aus dem [!DNL Google Tag Manager] Dashboard erstellen Sie als nächsten Schritt eine Regel, die das Tag auf der Konvertierungsseite auslöst.

1. under **[!UICONTROL Fire On]** klicken **[!UICONTROL Some Pages]**.

1. Im _[!UICONTROL Choose Pages]_müssen Sie die folgenden Einstellungen vornehmen:

   - **[!UICONTROL Name]** - Geben Sie einen Namen für die Seitenbeschreibung ein.

   - **[!UICONTROL Variable]** `url`

   - **Vorgang** - `matches RegEx`

     Weitere Informationen finden Sie unter [Regex- und CSS-Selektor-Operatoren](https://support.google.com/tagmanager/answer/7679109) in der Hilfe zu Google Tag Manager.

   - **[!UICONTROL Value]** - `checkout/success.*`

1. Aktivieren Sie das grüne Kontrollkästchen und klicken Sie auf **[!UICONTROL Save]**.

   Der von Ihnen eingerichtete Trigger wird im Bereich &quot;Fire On&quot;als blaue Schaltfläche angezeigt.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Tag]**.

### Schritt 3. Vorschau erstellen und veröffentlichen

Der nächste Schritt in diesem Prozess ist die Vorschau des Tags. Jedes Mal, wenn eine Vorschau des Tags angezeigt wird, wird ein Schnappschuss der Version gespeichert. Wenn Sie mit den Ergebnissen zufrieden sind, wechseln Sie zur gewünschten Version und klicken Sie auf **[!UICONTROL Publish]**.
