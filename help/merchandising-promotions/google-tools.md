---
title: Google-Site-Tools
description: Erfahren Sie mehr über die Google-Tools-Integrationen, mit denen Sie Ihre Inhalte optimieren, Ihren Traffic analysieren und Ihren Katalog mit Einkaufsaggregatoren und Marketplace verbinden können.
exl-id: 09c48f1e-792b-4553-82fc-cd1a119b15d0
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 0%

---

# Google-Site-Tools

Ihre Store-Konfiguration ist mit den folgenden Google-Tools integriert, mit denen Sie Ihre Inhalte optimieren, Ihren Traffic analysieren und Ihren Katalog mit Einkaufsaggregatoren und Marketplace verbinden können.

- [Google Analytics](google-analytics.md) - Verwenden Sie _Google Universal Analytics_ , um zusätzliche benutzerdefinierte Dimensionen und Metriken für die Verfolgung zu definieren, mit Unterstützung für Offline- und mobile App-Interaktionen und Zugriff auf laufende Updates.

- [Google Content Experiments](google-content-experiments.md) - Richten Sie einen A/B-Test für Produkte, Kategorien oder Inhaltsseiten ein, die Google Analytics Content Experiments verwenden.

- [Google Tag Manager](google-tag-manager.md) - ![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Verwenden Sie den Google Tag Manager, um die vielen Tags zu verwalten, die mit Marketingkampagnenereignissen verbunden sind.

- [Google AdWords](google-adwords.md) - Erstellen Sie eine Google AdWords-Kampagne und verfolgen Sie Konversionen für Ihren Store.

{{gtag-api-note}}

## Datenschutzeinstellungen für Google

Wenn Ihr Unternehmen Datenschutzbestimmungen wie [DSGVO](../getting-started/compliance-gdpr.md) oder [CCPA](../getting-started/compliance-ccpa.md) einhalten muss, ändern Sie die Standardeinstellungen der Google-Tools, um die Datenschutzanforderungen zu erfüllen. Führen Sie diese Schritte aus, um sicherzustellen, dass Ihre Verwendung von Kundendaten weiterhin den Anforderungen entspricht.

### Schritt 1: Aktualisieren der Google-Einstellungen

1. [Anmelden][1]{: target=&quot;_blank&quot;} für das Google Analytics-Konto Ihres Unternehmens.

1. Wählen Sie unten in der linken Seitenleiste **[!UICONTROL Admin]** und navigieren Sie dann zu dem Konto, das Sie bearbeiten möchten (falls zutreffend).

1. Klicken Sie in der Spalte **[!UICONTROL Account]** auf **[!UICONTROL Account Settings]**.

1. Deaktivieren Sie die Datenweitergabe, um die Anforderungen an die Datenschutzbestimmungen zu erfüllen.

   Die Standardeinstellungen für Google Analytics geben Ihre Unternehmensdaten für Google und andere Benutzer frei. Deaktivieren Sie zum Deaktivieren der Datenfreigabe das Kontrollkästchen Auswahl für die folgenden Einstellungen:

   - Google-Produkte und -Dienstleistungen
   - Benchmarking
   - Technischer Support
   - Kontospezialisten

1. Akzeptieren Sie den Änderungsantrag _Datenverarbeitung_.

   Die Google Ads Data Processing-Begriffe beschreiben, wie Google Daten verarbeitet und welche Maßnahmen ergriffen werden, um die Datensicherheit für Unternehmen sicherzustellen, die der DSGVO unterliegen. Außerdem werden mit dem Änderungsantrag Aufzeichnungen über Ihre juristischen Personen und Kontaktinformationen geführt. Um [mehr zu erfahren][2]{: target=&quot;_blank&quot;}, klicken Sie auf den Link in der Nachricht oben auf der Seite.

   - Scrollen Sie auf der Seite nach unten zu **[!UICONTROL Data Processing Amendment]**.
   - Klicken Sie auf **[!UICONTROL Review Amendment]** , um die _Google Ads Data Processing Terme_ zu lesen.
   - Klicken Sie auf **[!UICONTROL Accept]**.
   - Klicken Sie auf **[!UICONTROL Save]**.

1. Füllen Sie die Details für _DPA-Administration_ aus.

   - Klicken Sie auf **[!UICONTROL Manage DPA Details]** , um eine DPA-Administrationsseite zu öffnen, auf der Sie Kontakte und die juristischen Personen Ihres Unternehmens bearbeiten können.

   - Klicken Sie im Abschnitt **[!UICONTROL Legal Entities]** auf das Symbol _Bearbeiten_ ( ![Google-Bearbeitungssymbol](./assets/google-icon-edit.png) ) und fügen Sie einen oder mehrere registrierte Namen für Ihr Unternehmen hinzu. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]**.

   - Klicken Sie im Bereich **Kontakte** auf das Symbol _Hinzufügen_ ( ![Google-Symbol zum Hinzufügen](./assets/google-icon-add.png) ) und geben Sie die Informationen für den ersten Kontakt ein. Aktivieren Sie als Nächstes das Kontrollkästchen der jeweiligen Rolle und klicken Sie auf **[!UICONTROL Add]**.

      - Primärer Kontakt - (Benachrichtigungs-E-Mail-Adresse) Der Kontakt, an den Benachrichtigungen gesendet werden.
      - Datenschutzbeauftragter - (falls zutreffend) Die Person, die dazu bestimmt ist, die Einhaltung der Datenschutzbestimmungen zu erleichtern.
      - Vertreter des Europäischen Wirtschaftsraums (EWR) (falls zutreffend): Die Person, die Kunden außerhalb der EU hinsichtlich ihrer DSGVO-Verpflichtungen vertritt.

     Wiederholen Sie diesen Vorgang, um ggf. einen weiteren Kontakt hinzuzufügen.

### Schritt 2: Ändern der Google JS-Bibliotheken

Google unterstützt drei JavaScript-Bibliotheken zur Messung der Website-Nutzung, je nach Google-Produkt: `gtag.js`, `analytics.js` und `ga.js`. Um die Datenschutzanforderungen zu erfüllen, kann der Standardcode wie folgt geändert werden:

#### IP-Adressen anonymisieren

Um die von **_Google Universal Analytics_** verwendeten IP-Adressen zu anonymisieren, fügen Sie das folgende Snippet zur `analytics.js` -Bibliothek auf Ihrem Webserver hinzu:

analytics.js

```
: `ga('set', 'anonymizeIp', true);`
```

Weitere Informationen finden Sie in der [Analytics.js-Feldreferenz][3]{: target=&quot;_blank&quot;} in der Google-Hilfe.

Wenn Sie die Legacy-Bibliothek `ga.js` verwenden, fügen Sie das folgende Snippet hinzu:

ga.js

```
: `ga('set', 'anonymizeIp', true);`
```

Um die von **_Google Tag Manager_** verwendeten IP-Adressen zu anonymisieren, setzen Sie den Parameter `anonymize_ip` in der Bibliothek `gtag.js` auf Ihrem Webserver auf `true`.

gtag.js

```
: `gtag('event', 'your_event', { 'anonymize_ip': true })`
```

Weitere Informationen finden Sie unter [IP-Anonymisierung in Analytics][4] in der Hilfe zu Google.

#### SSL erzwingen

Um zu erzwingen, dass alle Google-Daten über eine sichere Socketschicht (SSL) übertragen werden, fügen Sie das folgende Snippet zur `analytics.js` -Bibliothek auf Ihrem Webserver hinzu.

analytics.js

```
: `ga('set', 'forceSSL', true);`
```

### Schritt 3: Datenschutzrichtlinie aktualisieren

Aktualisieren Sie Ihre [Datenschutzrichtlinie](../getting-started/privacy-policy.md), um anzugeben, dass Ihr Unternehmen:

- Verwendet Google Analytics
- Verbindet IP-Adressen mit personenbezogenen Daten
- Die Google-Datenfreigabe wurde deaktiviert.
- Verwendet keine anderen Google-Dienste mit Google Analytics-Cookies

[1]: https://www.google.com/analytics/
[2]: https://support.google.com/analytics/answer/3379636
[3]: https://developers.google.com/analytics/devguides/collection/analyticsjs/field-reference
[4]: https://support.google.com/analytics/answer/2763052
