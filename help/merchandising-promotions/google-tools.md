---
title: Google-Site-Tools
description: Erfahren Sie mehr über die Google-Tools-Integrationen, mit denen Sie Ihre Inhalte optimieren, Ihren Traffic analysieren und Ihren Katalog mit Einkaufsaggregatoren und Marketplace verbinden können.
exl-id: 09c48f1e-792b-4553-82fc-cd1a119b15d0
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 0%

---

# Google-Site-Tools

Ihre Store-Konfiguration ist mit den folgenden Google-Tools integriert, mit denen Sie Ihre Inhalte optimieren, Ihren Traffic analysieren und Ihren Katalog mit Einkaufsaggregatoren und Marketplace verbinden können.

- [Google Analytics](google-analytics.md) - Verwendung _Google Universal Analytics_ , um zusätzliche benutzerdefinierte Dimensionen und Metriken für die Verfolgung zu definieren, mit Unterstützung für Offline- und mobile App-Interaktionen und Zugriff auf laufende Aktualisierungen.

- [Google Content Experiments](google-content-experiments.md) - Richten Sie mithilfe von Google Analytics Content Experiments einen A/B-Test für Produkte, Kategorien oder Inhaltsseiten ein.

- [Google Tag Manager](google-tag-manager.md) - ![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce) Mit dem Google Tag Manager können Sie die vielen Tags verwalten, die mit Marketingkampagnenereignissen verbunden sind.

- [Google AdWords](google-adwords.md) - Erstellen Sie eine Google AdWords-Kampagne und verfolgen Sie Konversionen für Ihren Store.

{{gtag-api-note}}

## Datenschutzeinstellungen für Google

Wenn Ihr Unternehmen Datenschutzbestimmungen wie die [DSGVO](../getting-started/compliance-gdpr.md) oder [CCPA](../getting-started/compliance-ccpa.md)ändern Sie die Standardeinstellungen der Google-Tools, um die Datenschutzanforderungen zu erfüllen. Führen Sie diese Schritte aus, um sicherzustellen, dass Ihre Verwendung von Kundendaten weiterhin den Anforderungen entspricht.

### Schritt 1: Aktualisieren der Google-Einstellungen

1. [Anmelden][1]{: target=&quot;_blank&quot;} auf das Google Analytics-Konto Ihres Unternehmens verweist.

1. Wählen Sie unten in der linken Seitenleiste **[!UICONTROL Admin]** und navigieren Sie dann zu dem Konto, das Sie bearbeiten möchten (falls zutreffend).

1. Im **[!UICONTROL Account]** Spalte, klicken **[!UICONTROL Account Settings]**.

1. Deaktivieren Sie die Datenweitergabe, um die Anforderungen an die Datenschutzbestimmungen zu erfüllen.

   Die Standardeinstellungen für Google Analytics geben Ihre Unternehmensdaten für Google und andere Benutzer frei. Deaktivieren Sie zum Deaktivieren der Datenfreigabe das Kontrollkästchen Auswahl für die folgenden Einstellungen:

   - Google-Produkte und -Dienstleistungen
   - Benchmarking
   - Technischer Support
   - Kontospezialisten

1. Akzeptieren Sie die _Änderung der Datenverarbeitung_.

   Die Google Ads Data Processing-Begriffe beschreiben, wie Google Daten verarbeitet und welche Maßnahmen ergriffen werden, um die Datensicherheit für Unternehmen sicherzustellen, die der DSGVO unterliegen. Außerdem werden mit dem Änderungsantrag Aufzeichnungen über Ihre juristischen Personen und Kontaktinformationen geführt. nach [Weitere Informationen][2]{: target=&quot;_blank&quot;}, klicken Sie oben auf der Seite auf den Link in der Nachricht.

   - Scrollen Sie nach unten zu **[!UICONTROL Data Processing Amendment]**.
   - Klicks **[!UICONTROL Review Amendment]** zum Lesen der _Google Ads Data Processing-Begriffe_.
   - Klicken **[!UICONTROL Accept]**.
   - Klicken **[!UICONTROL Save]**.

1. Führen Sie die _DPA-Verwaltung_ Details.

   - Klicks **[!UICONTROL Manage DPA Details]** um eine DPA-Administrationsseite zu öffnen, auf der Sie Kontakte und die juristischen Personen Ihres Unternehmens bearbeiten können.

   - Im **[!UICONTROL Legal Entities]** klicken Sie auf die _Bearbeiten_ ( ![Symbol &quot;Google bearbeiten&quot;](./assets/google-icon-edit.png) ) und fügen Sie einen oder mehrere registrierte Namen für Ihre Organisation hinzu. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]**.

   - Im **Kontakte** klicken Sie auf die _Hinzufügen_ ( ![Symbol &quot;Google hinzufügen&quot;](./assets/google-icon-add.png) ) und geben Sie die Informationen für den ersten Kontakt ein. Aktivieren Sie als Nächstes das Kontrollkästchen der jeweiligen Rolle und klicken Sie auf **[!UICONTROL Add]**.

      - Primärer Kontakt - (Benachrichtigungs-E-Mail-Adresse) Der Kontakt, an den Benachrichtigungen gesendet werden.
      - Datenschutzbeauftragter - (falls zutreffend) Die Person, die dazu bestimmt ist, die Einhaltung der Datenschutzbestimmungen zu erleichtern.
      - Vertreter des Europäischen Wirtschaftsraums (EWR) (falls zutreffend): Die Person, die Kunden außerhalb der EU hinsichtlich ihrer DSGVO-Verpflichtungen vertritt.

     Wiederholen Sie diesen Vorgang, um ggf. einen weiteren Kontakt hinzuzufügen.

### Schritt 2: Ändern der Google JS-Bibliotheken

Google unterstützt drei JavaScript-Bibliotheken zur Messung der Website-Nutzung, je nach Google-Produkt: `gtag.js`, `analytics.js`, und `ga.js`. Um die Datenschutzanforderungen zu erfüllen, kann der Standardcode wie folgt geändert werden:

#### IP-Adressen anonymisieren

Anonymisieren der von **_Google Universal Analytics_** Fügen Sie dem `analytics.js` -Bibliothek auf Ihrem Webserver:

analytics.js

```
: `ga('set', 'anonymizeIp', true);`
```

Weitere Informationen finden Sie unter [Analytics.js-Feldreferenz][3]{: target=&quot;_blank&quot;} in der Google-Hilfe.

Wenn Sie die veraltete `ga.js` -Bibliothek hinzufügen, fügen Sie das folgende Snippet hinzu:

ga.js

```
: `ga('set', 'anonymizeIp', true);`
```

Anonymisieren der von **_Google Tag Manager_**, legen Sie die `anonymize_ip` Parameter auf `true` im `gtag.js` -Bibliothek auf Ihrem Webserver.

gtag.js

```
: `gtag('event', 'your_event', { 'anonymize_ip': true })`
```

Weitere Informationen finden Sie unter [IP-Anonymisierung in Analytics][4] in der Google-Hilfe.

#### SSL erzwingen

Um zu erzwingen, dass alle Google-Daten über eine sichere Socketschicht (SSL) übertragen werden, fügen Sie das folgende Snippet zum `analytics.js` -Bibliothek auf Ihrem Webserver.

analytics.js

```
: `ga('set', 'forceSSL', true);`
```

### Schritt 3: Datenschutzrichtlinie aktualisieren

Aktualisieren Sie Ihre [Datenschutzrichtlinie](../getting-started/privacy-policy.md) um anzugeben, dass Ihr Unternehmen

- Verwendet Google Analytics
- Verbindet IP-Adressen mit personenbezogenen Daten
- Die Google-Datenfreigabe wurde deaktiviert.
- Verwendet keine anderen Google-Dienste mit Google Analytics-Cookies

[1]: https://www.google.com/analytics/
[2]: https://support.google.com/analytics/answer/3379636
[3]: https://developers.google.com/analytics/devguides/collection/analyticsjs/field-reference
[4]: https://support.google.com/analytics/answer/2763052
