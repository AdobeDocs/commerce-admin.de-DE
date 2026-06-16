---
title: Google Site-Tools
description: Erfahren Sie mehr über die Google-Tools-Integrationen, mit denen Sie Ihre Inhalte optimieren, Ihren Traffic analysieren und Ihren Katalog mit Shopping-Aggregatoren und Marktplätzen verbinden können.
exl-id: 09c48f1e-792b-4553-82fc-cd1a119b15d0
feature: Marketing Tools, Integration
TQID: https://experienceleague.adobe.com/P-IniOyLDfDk8oe1v9ysmRV6yC7IWpxUBaFF--2YMCg
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: c32adafa-ed01-4b31-997e-2413013911b0
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 662
ht-degree: 0%

---

# Google Site-Tools

Ihre Store-Konfiguration ist mit den folgenden Google-Tools integriert, um Ihre Inhalte zu optimieren, Ihren Traffic zu analysieren und Ihren Katalog mit Shopping-Aggregatoren und Marktplätzen zu verbinden.

- [Google Analytics](google-analytics.md) - Verwenden Sie _Google Universal Analytics_, um zusätzliche benutzerdefinierte Dimensionen und Metriken für das Tracking zu definieren, mit Unterstützung für Offline- und Mobile-App-Interaktionen und Zugriff auf laufende Aktualisierungen.

- [Google Tag Manager](google-tag-manager.md) - ![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Verwenden Sie den Google Tag Manager, um die vielen Tags zu verwalten, die sich auf Marketing-Kampagnenereignisse beziehen.

- [Google AdWords](google-adwords.md) - Erstellen Sie eine Google AdWords-Kampagne und verfolgen Sie Konversionen für Ihren Store.

{{gtag-api-note}}

## Datenschutzeinstellungen für Google

Wenn Ihr Unternehmen Datenschutzbestimmungen wie die [DSGVO](../getting-started/compliance-gdpr.md) oder den [CCPA](../getting-started/compliance-ccpa.md) einhalten muss, ändern Sie die Standardeinstellungen der Google-Tools, um die Datenschutzanforderungen zu erfüllen. Führen Sie diese Schritte aus, um sicherzustellen, dass Ihre Verwendung von Kundendaten den Vorschriften entspricht.

### Schritt 1: Google-Einstellungen aktualisieren

1. [Anmelden](https://www.google.com/analytics/){: target="_blank"} beim Google Analytics-Konto Ihres Unternehmens.

1. Wählen Sie am unteren Rand der linken Seitenleiste **[!UICONTROL Admin]** aus und navigieren Sie dann zu dem Konto, das Sie bearbeiten möchten (falls zutreffend).

1. Klicken Sie in der Spalte **[!UICONTROL Account]** auf **[!UICONTROL Account Settings]**.

1. Deaktivieren Sie die Datenfreigabe, um die Datenschutzanforderungen zu erfüllen.

   Die standardmäßigen Google Analytics-Einstellungen geben Ihre Unternehmensdaten für Google und andere Parteien frei. Deaktivieren Sie zum Deaktivieren der Datenfreigabe das Kontrollkästchen für die folgenden Einstellungen:

   - Google-Produkte und -Services
   - Benchmarking
   - Technischer Support
   - Account Specialists

1. Akzeptieren Sie die _Änderung der Datenverarbeitung_.

   Die Google Ads-Datenverarbeitungsbedingungen beschreiben, wie Google Daten verarbeitet und welche Maßnahmen es ergreift, um die Datensicherheit für Unternehmen zu gewährleisten, die der DSGVO unterliegen. Mit der Änderung werden auch Ihre juristischen Personen und Kontaktinformationen aufgezeichnet. Um [weitere Informationen](https://support.google.com/analytics/answer/3379636){: target="_blank"} zu erhalten, klicken Sie auf den Link in der Nachricht oben auf der Seite.

   - Scrollen Sie auf der Seite nach unten zum **[!UICONTROL Data Processing Amendment]**.
   - Klicken Sie auf **[!UICONTROL Review Amendment]**, um die _Datenverarbeitungsbedingungen für Google Ads zu_.
   - Klicken Sie auf **[!UICONTROL Accept]**.
   - Klicken Sie auf **[!UICONTROL Save]**.

1. Füllen Sie die Details _DPA-Administration_ aus.

   - Klicken Sie auf **[!UICONTROL Manage DPA Details]** , um eine DPA-Verwaltungsseite zu öffnen, auf der Sie Kontakte und die juristischen Personen Ihres Unternehmens bearbeiten können.

   - Klicken Sie im Abschnitt **[!UICONTROL Legal Entities]** auf das Symbol _Bearbeiten_ ( ![Google-Bearbeitungssymbol](./assets/google-icon-edit.png) ) und fügen Sie einen oder mehrere registrierte Namen für Ihr Unternehmen hinzu. Klicken Sie abschließend auf **[!UICONTROL Save]**.

   - Klicken Sie im Abschnitt **Kontakte** auf das Symbol _Hinzufügen_ ( ![Google-Hinzufügen](./assets/google-icon-add.png) ) und geben Sie die Informationen für den ersten Kontakt ein. Aktivieren Sie als Nächstes das Kontrollkästchen jeder entsprechenden Rolle und klicken Sie auf **[!UICONTROL Add]**.

      - Primärer Kontakt - (E-Mail-Benachrichtigungsadresse) Der Kontakt, an den Benachrichtigungen gesendet werden.
      - Datenschutzbeauftragter - (falls zutreffend) Die Person, die dazu bestimmt ist, die Einhaltung von Datenschutzbestimmungen zu erleichtern.
      - Vertreter des Europäischen Wirtschaftsraums (EWR) - (falls zutreffend) Die Person, die Kunden außerhalb der EU in Bezug auf deren DSGVO-Verpflichtungen vertritt.

     Wiederholen Sie diesen Vorgang, um ggf. einen weiteren Kontakt hinzuzufügen.

### Schritt 2: Google JS-Bibliotheken ändern

Google unterstützt drei JavaScript-Bibliotheken zur Messung der Website-Nutzung, je nach Google-Produkt: `gtag.js`, `analytics.js` und `ga.js`. Um Datenschutzanforderungen zu erfüllen, kann der Standard-Code wie folgt geändert werden:

#### IP-Adressen anonymisieren

Um die von **_Google Universal Analytics_** verwendeten IP-Adressen zu anonymisieren, fügen Sie der `analytics.js`-Bibliothek auf Ihrem Webserver folgenden Code-Ausschnitt hinzu:

analytics.js

```
: `ga('set', 'anonymizeIp', true);`
```

Weitere Informationen finden Sie in der [Analytics.js-Feldreferenz](https://developers.google.com/analytics/devguides/collection/analyticsjs/field-reference){: target="_blank"} in der Google-Hilfe.

Wenn Sie die veraltete `ga.js`-Bibliothek verwenden, fügen Sie das folgende Snippet hinzu:

ga.js

```
: `ga('set', 'anonymizeIp', true);`
```

Um die von **_Google Tag Manager_** verwendeten IP-Adressen zu anonymisieren, legen Sie den `anonymize_ip` Parameter in der `gtag.js` auf Ihrem Webserver auf `true` fest.

gtag.js

```
: `gtag('event', 'your_event', { 'anonymize_ip': true })`
```

Weitere Informationen finden Sie unter [IP-Anonymisierung in Analytics](https://support.google.com/analytics/answer/2763052) in der Hilfe zu Google.

#### SSL erzwingen

Um die Übertragung aller Google-Daten über eine Secure Socket Layer (SSL) zu erzwingen, fügen Sie der `analytics.js`-Bibliothek auf Ihrem Webserver das folgende Snippet hinzu.

analytics.js

```
: `ga('set', 'forceSSL', true);`
```

### Schritt 3: Aktualisieren Sie Ihre Datenschutzrichtlinie

Aktualisieren Sie Ihre [Datenschutzrichtlinie](../getting-started/privacy-policy.md), um anzugeben, dass Ihr Unternehmen:

- Verwendet Google Analytics
- Maskiert IP-Adressen zum Ausblenden personenbezogener Daten
- Google-Datenfreigabe deaktiviert
- Verwendet keine anderen Google-Services mit Google Analytics-Cookies
