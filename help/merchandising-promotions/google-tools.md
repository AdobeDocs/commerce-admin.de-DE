---
title: Google Site-Tools
description: Erfahren Sie mehr über die Google-Tools-Integrationen, mit denen Sie Ihre Inhalte optimieren, Ihren Traffic analysieren und Ihren Katalog mit Shopping-Aggregatoren und Marktplätzen verbinden können.
exl-id: 09c48f1e-792b-4553-82fc-cd1a119b15d0
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '665'
ht-degree: 0%

---

# Google Site-Tools

Ihre Store-Konfiguration ist mit den folgenden Google-Tools integriert, um Ihre Inhalte zu optimieren, Ihren Traffic zu analysieren und Ihren Katalog mit Shopping-Aggregatoren und Marktplätzen zu verbinden.

- [Google Analytics](google-analytics.md) - Verwenden Sie _Google Universal Analytics_, um zusätzliche benutzerdefinierte Dimensionen und Metriken für das Tracking zu definieren, mit Unterstützung für Offline- und Mobile-App-Interaktionen und Zugriff auf laufende Updates.

- [Google-Inhaltsexperimente](google-content-experiments.md) - Richten Sie mithilfe von Google Analytics-Inhaltsexperimenten einen A/B-Test für Produkte, Kategorien oder Inhaltsseiten ein.

- [Google Tag Manager](google-tag-manager.md) - ![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Verwenden Sie den Google Tag Manager, um die vielen Tags zu verwalten, die sich auf Marketing-Kampagnenereignisse beziehen.

- [Google AdWords](google-adwords.md) - Erstellen Sie eine Google AdWords-Kampagne und verfolgen Sie Konversionen für Ihren Store.

{{gtag-api-note}}

## Datenschutzeinstellungen für Google

Wenn Ihr Unternehmen Datenschutzbestimmungen wie die [DSGVO](../getting-started/compliance-gdpr.md) oder den [CCPA](../getting-started/compliance-ccpa.md) einhalten muss, ändern Sie die Standardeinstellungen der Google-Tools, um die Datenschutzanforderungen zu erfüllen. Führen Sie diese Schritte aus, um sicherzustellen, dass Ihre Verwendung von Kundendaten den Vorschriften entspricht.

### Schritt 1: Google-Einstellungen aktualisieren

1. [Anmelden][1]{: target="_blank"} beim Google Analytics-Konto Ihres Unternehmens.

1. Wählen Sie am unteren Rand der linken Seitenleiste **[!UICONTROL Admin]** aus und navigieren Sie dann zu dem Konto, das Sie bearbeiten möchten (falls zutreffend).

1. Klicken Sie in der Spalte **[!UICONTROL Account]** auf **[!UICONTROL Account Settings]**.

1. Deaktivieren Sie die Datenfreigabe, um die Datenschutzanforderungen zu erfüllen.

   Die Standardeinstellungen für Google Analytics geben Ihre Unternehmensdaten für Google und andere Parteien frei. Deaktivieren Sie zum Deaktivieren der Datenfreigabe das Kontrollkästchen für die folgenden Einstellungen:

   - Google-Produkte und -Services
   - Benchmarking
   - Technischer Support
   - Account Specialists

1. Akzeptieren Sie die _Änderung der Datenverarbeitung_.

   Die Google Ads-Datenverarbeitungsbedingungen beschreiben, wie Google Daten verarbeitet und welche Maßnahmen es ergreift, um die Datensicherheit für Unternehmen zu gewährleisten, die der DSGVO unterliegen. Mit der Änderung werden auch Ihre juristischen Personen und Kontaktinformationen aufgezeichnet. Um [weitere Informationen][2]{: target="_blank"} zu erhalten, klicken Sie auf den Link in der Nachricht oben auf der Seite.

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

Weitere Informationen finden Sie in der [Analytics.js-Feldreferenz][3]{: target="_blank"} in der Google-Hilfe.

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

Weitere Informationen finden Sie unter [IP-Anonymisierung in Analytics][4] in der Hilfe zu Google.

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

[1]: https://www.google.com/analytics/
[2]: https://support.google.com/analytics/answer/3379636
[3]: https://developers.google.com/analytics/devguides/collection/analyticsjs/field-reference
[4]: https://support.google.com/analytics/answer/2763052
