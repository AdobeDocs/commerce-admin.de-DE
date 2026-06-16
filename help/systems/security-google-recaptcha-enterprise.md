---
title: Google reCAPTCHA Enterprise
description: Erfahren Sie, wie Sie Google reCAPTCHA Enterprise konfigurieren, um Ihre Adobe Commerce as a Cloud Service-Storefront vor Bots und betrügerischen Aktivitäten zu schützen.
role: Admin
feature: Configuration, Security
badgeSaas: label="Nur SaaS" type="Positive" url="https://experienceleague.adobe.com/de/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce as a Cloud Service-Projekte (von Adobe verwaltete SaaS-Infrastruktur)."
exl-id: 2c88488c-8ff1-41db-b81b-89ad164e134d
TQID: https://experienceleague.adobe.com/oMZleuJsp2QiDD7IsMDV647LWKm938lNvY4--o6G3c8
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 633
ht-degree: 0%

---

# Google reCAPTCHA Enterprise

[Google reCAPTCHA Enterprise](https://cloud.google.com/security/products/recaptcha#protect-against-fraud-and-abuse-with-modern-bot-protection-and-fraud-prevention-platform) bietet einen erweiterten Bot-Schutz für Ihre Adobe Commerce as a Cloud Service-Storefront, indem mithilfe von adaptiver Risikoanalyse und maschinellem Lernen zwischen menschlichen Benutzern und Bots unterschieden wird. Dadurch können betrügerische Aktivitäten, Spam und Missbrauch auf Ihrer Site verhindert werden.

>[!NOTE]
>
>Diese Funktion bietet KEINE reCAPTCHA-Unterstützung für Admins.

[reCAPTCHA-Integration](https://experienceleague.adobe.com/developer/commerce/storefront/dropins/user-auth/recaptcha/?lang=de) beschreibt, wie Sie Unterstützung für reCAPTCHA Enterprise in Ihre Storefront hinzufügen.

Informationen zum Konfigurieren anderer Versionen von Google reCAPTCHA finden Sie unter [Google reCAPTCHA &#x200B;](security-google-recaptcha.md)3 und v2&rbrace;.

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

1. Navigieren Sie in der _Admin_-Seitenleiste von Adobe Commerce zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie _[!UICONTROL Security]_&#x200B;und wählen Sie **[!UICONTROL Google reCAPTCHA Storefront]**.

1. Scrollen Sie nach unten zum Abschnitt **[!UICONTROL reCAPTCHA Enterprise]** und schließen Sie die Konfiguration wie folgt ab.

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
