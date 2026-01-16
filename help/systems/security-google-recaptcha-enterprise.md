---
title: Google reCAPTCHA Enterprise
description: Erfahren Sie, wie Sie Google reCAPTCHA Enterprise konfigurieren, um Ihre Adobe Commerce as a Cloud Service-Storefront vor Bots und betrügerischen Aktivitäten zu schützen.
role: Admin
feature: Configuration, Security
badgeSaas: label="Nur SaaS" type="Positive" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce as a Cloud Service-Projekte (von Adobe verwaltete SaaS-Infrastruktur)."
source-git-commit: dde1d634a1c6c7435668a8ad6084b926cc0d6193
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 0%

---

# Google reCAPTCHA Enterprise

[!BADGE Sandbox]{type=Caution tooltip="Die aufgelisteten Elemente sind derzeit nur in Sandbox-Umgebungen verfügbar. Adobe veröffentlicht zuerst Aktualisierungen für Sandbox, damit Sie bevorstehende Änderungen testen können, bevor sie in die Produktion übergehen."}

[Google reCAPTCHA Enterprise](https://cloud.google.com/security/products/recaptcha#protect-against-fraud-and-abuse-with-modern-bot-protection-and-fraud-prevention-platform) bietet einen erweiterten Bot-Schutz für Ihre Adobe Commerce as a Cloud Service-Storefront, indem mithilfe von adaptiver Risikoanalyse und maschinellem Lernen zwischen menschlichen Benutzern und Bots unterschieden wird. Dadurch können betrügerische Aktivitäten, Spam und Missbrauch auf Ihrer Site verhindert werden.

>[!NOTE]
>
>Diese Funktion bietet KEINE reCAPTCHA-Unterstützung für Admins.

Informationen zum Konfigurieren anderer Versionen von Google reCAPTCHA finden Sie unter [Google reCAPTCHA ](security-google-recaptcha.md)3 und v2}.

## Funktionen

Google reCAPTCHA Enterprise umfasst die folgenden Funktionen:

- **Erweiterte Bot-Erkennung**: Verwendet die maschinellen Lernmodelle von Google Cloud für eine überlegene Bot-Erkennung
- **Risikobewertungsanalyse**: Bietet detaillierte Risikobewertungen (0,0-1,0) für jede Interaktion
- **Konfigurierbare Schwellenwerte**: Festlegen der akzeptablen Mindestrisikowerte pro Mandant
- **Unterstützung für mehrere Mandanten**: Mandantenspezifische Konfiguration mit isolierten Google Cloud-Projekten
- **Verschlüsselte Anmeldeinformationen**: In einer Datenbank verschlüsselte Anmeldeinformationen für Service-Konten
- **Formularschutz**: Schützt alle standardmäßigen Commerce-Formulare, einschließlich Anmeldung, Checkout, Produktbewertungen und mehr.

## Voraussetzungen

Sie benötigen die folgenden Ressourcen, bevor Sie Google reCAPTCHA Enterprise für Ihre Adobe Commerce as a Cloud Service-Storefront konfigurieren können:

- Ein gültiges Google Cloud-Konto mit aktiviertem reCAPTCHA Enterprise.
- Zugriff auf die Google Cloud Console zum Erstellen und Verwalten von reCAPTCHA Enterprise-Schlüsseln.

Bei einer Installation von Adobe Commerce as a Cloud Service mit mehreren Mandanten muss jeder Mandant über ein eigenes Google-Cloud-Projekt und eigene reCAPTCHA-Unternehmensschlüssel verfügen.

## Schritt 1: Einrichten von Google reCAPTCHA Enterprise

Führen Sie diese allgemeinen Schritte aus, um Google reCAPTCHA Enterprise für Ihre Storefront einzurichten. Detaillierte Anweisungen finden Sie in der Dokumentation zu [Google reCAPTCHA Enterprise](https://docs.cloud.google.com/recaptcha/docs/overview).

1. [Erstellen eines Google-Cloud-](https://developers.google.com/workspace/guides/create-project) für Ihre reCAPTCHA Enterprise-Implementierung.

1. Aktivieren Sie die [reCAPTCHA Enterprise API](https://docs.cloud.google.com/recaptcha/docs/prepare-environment).

1. Erstellen Sie einen Score-basierten reCAPTCHA Enterprise [Site-Schlüssel](https://docs.cloud.google.com/recaptcha/docs/choose-key-type).

1. Erstellen Sie ein Service-Konto mit der Rolle `roles/recaptchaenterprise.admin` IAM.

1. Laden Sie die JSON-Schlüsseldatei für das Service-Konto herunter, die die Anmeldeinformationen enthält, die zum Authentifizieren Ihrer Adobe Commerce as a Cloud Service-Storefront mit Google reCAPTCHA Enterprise erforderlich sind.

## Schritt 2: Konfigurieren von Google reCAPTCHA für die Storefront

1. Wählen Sie im linken Bedienfeld unter _[!UICONTROL Security]_die Option **[!UICONTROL Google reCAPTCHA Storefront]**aus.

1. Füllen Sie den **[!UICONTROL reCAPTCHA Enterprise]** Abschnitt wie folgt aus.

   - Kopieren Sie **[!UICONTROL Site Key]** Ihren reCAPTCHA Enterprise-Site-Schlüssel aus Ihrer Google Cloud-Konsole und fügen Sie ihn ein.

   - Kopieren Sie **[!UICONTROL Google Cloud Project ID]** die Projekt-ID und fügen Sie sie aus Ihrem Google Cloud-Projekt ein.

   - Kopieren Sie **[!UICONTROL Service Account JSON]** den Inhalt der JSON-Schlüsseldatei für das Service-Konto, die Sie in [Schritt 1: Einrichten von Google reCAPTCHA Enterprise](#step-1-set-up-google-recaptcha-enterprise) heruntergeladen haben.

   - Geben Sie **[!UICONTROL Minimum Score Threshold]** den Mindestwert (0,0-1,0) ein, um zu ermitteln, wann eine Benutzerinteraktion als potenzielles Risiko gekennzeichnet wird. Ein Score von 1,0 ist eine typische Benutzerinteraktion, und 0,0 ist wahrscheinlich ein Bot.

   - Wählen Sie **[!UICONTROL Badge Position]** auf jeder Seite die Position des unsichtbaren reCAPTCHA-Badges aus. Optionen: `Inline` / `Bottom Right` / `Bottom Left`.

   - Wählen Sie **[!UICONTROL Theme]** entweder `Light Theme` (Standard) oder `Dark Theme`, um den Stil des Google reCAPTCHA-Felds zu bestimmen.

   - Geben Sie **[!UICONTROL Language Code]** einen ([-Code) ein](https://developers.google.com/recaptcha/docs/language) der die Sprache angibt, die für Google reCAPTCHA-Text und -Nachrichten verwendet wird.

   - Ändern Sie **[!UICONTROL Validation Failure Message]** optional die Meldung, die auf der Storefront angezeigt wird, wenn die Validierung nicht erfolgreich war.


1. Erweitern Sie den Abschnitt **[!UICONTROL Storefront]** und legen Sie jedes Storefront-Formular, das Sie schützen möchten, auf **[!UICONTROL reCAPTCHA Enterprise]** fest.

   {{recaptcha-forms-list}}

   ![Konfiguration der Storefront-Optionen](../configuration-reference/security/assets/recaptcha-storefront.png){width="600" zoomable="yes"}

## Schritt 3: Speichern Sie die Konfiguration

1. Wenn die Konfigurationseinstellungen abgeschlossen sind, klicken Sie auf **[!UICONTROL Save Config]**.

1. Klicken Sie in der Meldung oben im Arbeitsbereich auf **[!UICONTROL Cache Management]** und aktualisieren Sie jeden ungültigen Cache.
