---
title: '[!DNL Google Tag Manager]'
description: Erfahren Sie, wie Sie mit [!DNL Google Tag Manager] die vielen Tags (Codefragmente) verwalten können, die sich auf Ihre Marketingkampagnenereignisse auf Ihren Adobe Commerce-Sites beziehen.
exl-id: 9c24239b-9efd-42ee-9b99-5a194f3c4347
feature: Marketing Tools, Integration
source-git-commit: be426ca16fb7a72ebeda4a2f92c0f0062a9acc62
workflow-type: tm+mt
source-wordcount: '1050'
ht-degree: 0%

---

# [!DNL Google Tag Manager]

{{ee-feature}}

[!DNL Google Tag Manager] ist ein leistungsstarkes Tool, mit dem Sie effizient verschiedene Tags (Codefragmente) verwalten und bereitstellen können, die mit Ihren Marketingkampagnenereignissen verknüpft sind. [!DNL Google Tag Manager] gibt Ihnen die Möglichkeit, Tracking-Tags zu Ihrer Site hinzuzufügen, um die Zielgruppe zu messen oder Suchmaschinen-Marketing-Initiativen zu personalisieren, neu auszurichten oder durchzuführen.

[!DNL Google Tag Manager] überträgt Daten und Ereignisse direkt an [!DNL Google Analytics], Enhanced E-Commerce und andere Analyselösungen von Drittanbietern, um ein klares Bild von der Leistung Ihrer Site, Produkte und Promotions zu erhalten.

Sie sollten über ein [!DNL Google Analytics] - und ein [!DNL Tag Manager] -Konto verfügen, um diesen Prozess fortzusetzen. Die folgenden Anweisungen führen Sie durch den Prozess der Konfiguration Ihrer Google-Konten, der Konfiguration Ihres Commerce-Stores und der Erstellung eines Tags.

>[!NOTE]
>
>Wenn Ihr Unternehmen Datenschutzbestimmungen wie die [Datenschutz-Grundverordnung](../getting-started/compliance-gdpr.md) und/oder den [California Consumer Privacy Act](../getting-started/compliance-ccpa.md) unterliegt, finden Sie weitere Informationen unter [Google-Datenschutzeinstellungen](google-tools.md#google-privacy-settings).

## Schritt 1. Konfigurieren Ihres [!DNL Google Analytics]-Kontos

Informationen zu den Grundlagen für die ersten Schritte finden Sie unter [Einrichten der Site-Suche](https://support.google.com/analytics/answer/1012264) in der Google-Hilfe. Weitere Informationen finden Sie in den Google-Handbüchern für [Google Analytics](https://support.google.com/analytics/answer/9304153) und [Google Tag Manager](https://support.google.com/tagmanager/answer/6102821).

1. Melden Sie sich bei Ihrem [!DNL Google Analytics] -Konto an.

1. Gehen Sie wie folgt vor, um **[!UICONTROL Internal Site Search Tracking]** zu aktivieren:

   - Navigieren Sie zu **[!UICONTROL Select View]** > **[!UICONTROL View Settings]**.

   - Setzen Sie **[!UICONTROL Site Search Tracking]** auf `On`.

   - Setzen Sie den Parameter **[!UICONTROL Query]** auf `q`.

   - Wenn Sie fertig sind, **[!UICONTROL Save]** die Einstellungen.

1. Gehen Sie wie folgt vor, um Anzeigefunktionen zu aktivieren:

   - Wählen Sie **[!UICONTROL Property Settings]** aus.

   - Setzen Sie unter _[!UICONTROL Advertising Features]_**[!UICONTROL Enable Demographics and Interest Reports]**auf `On`.

   - **[!UICONTROL Save]** die Einstellungen.

1. Gehen Sie wie folgt vor, um das E-Commerce-Tracking zu aktivieren:

   - Navigieren Sie zu **[!UICONTROL Select View]** > **[!UICONTROL Ecommerce Settings]**.

   - Setzen Sie **[!UICONTROL Enable Ecommerce]** auf `On`.

   - Setzen Sie **[!UICONTROL Enable Enhanced Ecommerce Reporting]** auf `On`.

   - **[!UICONTROL Save]** die Einstellungen.

1. Laden Sie die Seite neu und stellen Sie sicher, dass alle Einstellungen `On` bleiben.

   >[!NOTE]
   >
   >Wenn nicht alle Einstellungen `On` sind, wiederholen Sie die vorherigen Schritte, speichern und laden Sie die Seite neu. Wiederholen Sie diesen Vorgang, bis alle Einstellungen auf `On` gesetzt sind.

## Schritt 2. Konfigurieren Ihres [!DNL Google Tag Manager]-Kontos

Die folgenden Anweisungen zeigen, wie Sie einen neuen Container mit den grundlegenden Einstellungen konfigurieren. Zur Vereinfachung des Prozesses wird eine Beispieldatei mit der Konfiguration [Composer](https://developer.adobe.com/commerce/php/development/composer/) (.json) verwendet, die zum Generieren eines Tags in einem neuen Container importiert wird. Für dieses Beispiel wird empfohlen, einen Container zu erstellen, anstatt einen vorhandenen Container zu ändern.

>[!NOTE]
>
>Weitere Informationen finden Sie unter Googles [Container-Export und -Import](https://support.google.com/tagmanager/answer/6106997). Diese Anweisungen bieten eine schrittweise Anleitung zum Importieren einer JSON-Musterdatei in einen neuen Container.

1. Laden Sie die verknüpfte Datei [GTM_M2_Config_json.txt](./assets/GTM_M2_Config_json.txt) herunter, öffnen Sie die Datei in einem Editor und speichern Sie sie als `GTM_M2_Config.json`.

   Die JSON-Datei wird direkt in [!DNL Google Tag Manager] hochgeladen.

1. Navigieren Sie zu **[!UICONTROL Admin]** > **[!UICONTROL Container]** > **[!UICONTROL Import Container]**.

1. Klicken Sie auf **[!UICONTROL Choose container file]** und wählen Sie die JSON-Datei aus.

1. Klicken Sie unter **[!UICONTROL Choose workspace]** auf **[!UICONTROL New]**.

1. Geben Sie einen Titel und eine Beschreibung ein und klicken Sie dann auf **[!UICONTROL Save]**.

1. Wählen Sie einen der folgenden Schritte aus, um die Datei zu importieren:

   - Die Option **[!UICONTROL Overwrite]** sollte für einen neuen Container ausgewählt werden.

   - Wenn Sie einen vorhandenen Container verwenden, sollte die Option **[!UICONTROL Merge]** ausgewählt sein.

1. Klicken Sie auf **[!UICONTROL Preview]** , um die Tags, Trigger und Variablen zu überprüfen.

1. Gehen Sie wie folgt vor, um die **[!UICONTROL Google Analytics ID]** zu bearbeiten, auf die in Variablen verwiesen wird:

   - Navigieren Sie zu **[!UICONTROL Variables]** > **[!UICONTROL User-Defined Variables]**.

   - Wählen Sie **[!UICONTROL Google Analytics]** aus und aktualisieren Sie den Platzhalter (`UA-xxxxxx-x`) mit Ihrem eigenen **[!UICONTROL GA ID]**.

1. Befolgen Sie die Anweisungen von Google zum Hinzufügen von Tags, Triggern und Variablen zum neuen Container.

   Wenn Sie Einstellungen in einem anderen Container haben, den Sie verwenden möchten, können sie in den neuen Container verschoben werden.

1. Klicken Sie nach Abschluss auf **[!UICONTROL Confirm]** .

1. Befolgen Sie die Anweisungen von Google zum Veröffentlichen des neuen Containers.

## Schritt 3. Konfigurieren des Stores

{{gtag-api-note}}

1. Melden Sie sich beim Administrator Ihres Commerce-Stores an.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Google API]** aus.

1. Erweitern Sie ![Erweiterungsselektor](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Google Analytics]** und konfigurieren Sie Folgendes:

   ![Verkaufskonfiguration - Google Analytics](../configuration-reference/sales/assets/google-api-analytics-tag-manager.png){width="600" zoomable="yes"}

   - Setzen Sie **[!UICONTROL Enable]** auf `Yes`.

   - Setzen Sie **[!UICONTROL Account type]** auf `Google Tag Manager`.

   - Geben Sie im Feld **[!UICONTROL Container ID]** Ihre GTM-ID (`GTM-xxxxxx`) ein.

   - Wenn Sie auch Google Analytics für Inhaltsexperimente verwenden, setzen Sie **Inhaltsexperimente aktivieren** auf `Yes`.

   - Verwenden Sie die Standardwerte für die übrigen Felder.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

1. Testen Sie Ihre [!DNL Google Tag Manager] -Einstellungen und stellen Sie sicher, dass alles ordnungsgemäß funktioniert.

>[!NOTE]
>
>Jeder Container ist mit einer Website verknüpft und Sie benötigen nur einen Container pro Konto. Wenn Sie über eine Commerce-Instanz mit mehreren Sites verfügen, benötigen Sie separate Container.

## Feldbeschreibungen

| Feld | Anwendungsbereich | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable] | Store-Ansicht | Bestimmt, ob Google Analytics Enhanced E-Commerce zur Analyse von Aktivitäten in Ihrem Store verwendet werden kann. Optionen: `Yes` / `No` |
| [!UICONTROL Account type] | Store-Ansicht | Bestimmt den Google-Trackingcode, der zur Überwachung von Store-Aktivitäten und -Traffic verwendet wird. Optionen: `Google Analytics` / `Google Tag Manager` |
| [!UICONTROL Anonymize IP] | Store-Ansicht | Bestimmt, ob Identifizierungsinformationen aus IP-Adressen entfernt werden, die in Google Analytics-Ergebnissen angezeigt werden. |
| [!UICONTROL Enable Content Experiments] | Store-Ansicht | Aktiviert Google Content Experiments, mit denen bis zu zehn verschiedene Versionen derselben Seite getestet werden können. Optionen: `Yes` / `No` |
| [!UICONTROL Container Id] | Store-Ansicht | Wenn [!DNL Google Tag Manager] bereits für Ihren Store installiert und konfiguriert ist, wird die Container-ID in diesem Feld automatisch angezeigt. |
| [!UICONTROL List property for the catalog page] | Store-Ansicht | Gibt die Tag-Manager-Eigenschaft an, die mit der Katalogseite verknüpft ist. Standardwert: `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | Store-Ansicht | Identifiziert die Tag-Manager-Eigenschaft, die mit dem Querverkaufsblock verknüpft ist. Standardwert: `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | Store-Ansicht | Identifiziert die Tag-Manager-Eigenschaft, die mit dem Upsell-Block verknüpft ist. Standardwert: `Up-sell` |
| [!UICONTROL List property for the related products block] | Store-Ansicht | Identifiziert die Tag-Manager-Eigenschaft, die mit dem zugehörigen Produktblock verknüpft ist. Standardwert: `Related Products` |
| [!UICONTROL List property for the search results page] | Store-Ansicht | Identifiziert die Tag-Manager-Eigenschaft, die mit der Suchergebnisseite verknüpft ist. Standardwert: `Search Results` |
| [!UICONTROL "Internal Promotions" for promotions field "Label"] | Store-Ansicht | Identifiziert die Tag-Manager-Eigenschaft, die mit den Bezeichnungen für interne Promotions verknüpft ist. Standardwert: `Label` |

{style="table-layout:auto"}

## Erstellen eines Tags zum Verfolgen von Konversionen

Wenn Sie über ein Google AdWords-Konto verfügen, können Sie ein Tag erstellen, das Konversionen verfolgt. Das folgende Beispiel zeigt, wie Sie mit [!DNL Google Tag Manager] und [!DNL Google Analytics] ein Tag erstellen, das auf der Konversionsseite Ihres Stores _Erfolg_ ausgelöst wird.

### Schritt 1. Tag erstellen

1. Melden Sie sich bei Ihrem [!DNL Google Tag Manager] -Konto an und klicken Sie auf den Link für den Container, den Sie für Ihren Store erstellt haben.

1. Klicken Sie im Feld **[!UICONTROL New Tag]** auf **[!UICONTROL Add a new tag]**.

1. Rufen Sie die folgenden Informationen aus Ihrem AdWords-Konto ab:

   - Konversions-ID
   - Konversionsbezeichnung

   Wenn Sie Hilfe benötigen, besuchen Sie die [Support-Site](https://support.google.com/tagmanager/answer/6105160) von Google.

1. Klicken Sie im Dashboard [!DNL Google Tag Manager] auf **[!UICONTROL Google AdWords]** und führen Sie folgende Schritte aus:

   - Klicken Sie auf den Platzhalter für den Titel und geben Sie einen Namen für das neue Tag ein.

   - Wählen Sie unter &quot;**[!UICONTROL Choose Product]**&quot;die Option &quot;**[!UICONTROL Google AdWords]**&quot;.

   - Wählen Sie unter &quot;_[!UICONTROL Choose a Tag Type]_&quot;die Option &quot;**[!UICONTROL AdWords Conversion Tracking]**&quot;aus und klicken Sie auf &quot;**[!UICONTROL Continue]**&quot;.

1. Geben Sie die **[!UICONTROL Conversion ID]** und **[!UICONTROL Conversion Label]** aus Ihrem AdWords-Konto ein und klicken Sie auf **[!UICONTROL Continue]**.

### Schritt 2. Erstellen einer Regel

Im Anschluss an das Dashboard [!DNL Google Tag Manager] besteht der nächste Schritt darin, eine Regel zu erstellen, die das Tag auf der Konvertierungsseite auslöst.

1. Klicken Sie unter **[!UICONTROL Fire On]** auf **[!UICONTROL Some Pages]**.

1. Führen Sie im Abschnitt _[!UICONTROL Choose Pages]_die folgenden Einstellungen aus:

   - **[!UICONTROL Name]** - Geben Sie einen Namen für die Seitenbeschreibung ein.

   - **[!UICONTROL Variable]** `url`

   - **Operation** - `matches RegEx`

     Weitere Informationen finden Sie unter [Regex- und CSS-Selektor-Operatoren](https://support.google.com/tagmanager/answer/7679109) in der Hilfe zu Google Tag Manager.

   - **[!UICONTROL Value]** - `checkout/success.*`

1. Aktivieren Sie das grüne Kontrollkästchen und klicken Sie auf **[!UICONTROL Save]**.

   Der von Ihnen eingerichtete Trigger wird im Bereich &quot;Fire On&quot;als blaue Schaltfläche angezeigt.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Tag]**.

### Schritt 3. Vorschau erstellen und veröffentlichen

Der nächste Schritt in diesem Prozess ist die Vorschau des Tags. Jedes Mal, wenn eine Vorschau des Tags angezeigt wird, wird ein Schnappschuss der Version gespeichert. Wenn Sie mit den Ergebnissen zufrieden sind, wechseln Sie zur Version, die Sie verwenden möchten, und klicken Sie auf **[!UICONTROL Publish]**.
