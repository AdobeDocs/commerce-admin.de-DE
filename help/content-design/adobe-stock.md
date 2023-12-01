---
title: Adobe Stock-Integration
description: Integrieren von Adobe Stock in Ihre [!DNL Commerce] -Instanz, um auf unzählige Medien-Assets zuzugreifen, die in Ihrem Store verwendet werden können.
exl-id: 0f399ea7-5726-476c-a945-c37e44a9ea55
feature: CMS, Media, Configuration, Integration
source-git-commit: 6666073a48741cb494f408a61401f46fc20cedc4
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# Adobe Stock-Integration

Um Zugriff auf zahllose Medien-Assets zu erhalten, die in Ihrem Store verwendet werden können, integrieren Sie [Adobe Stock][adobe-stock] mit [!UICONTROL Commerce].

![Adobe Stock-Suchergebnisse](./assets/adobe-stock-search-grid.png){width="700" zoomable="yes"}

Der Adobe Stock-Dienst bietet Unternehmen Zugang zu Millionen von hochwertigen, kuratierten und gebührenfreien Fotos, Vektorgrafiken, Illustrationen, Videos, Vorlagen und 3D-Assets für alle Kreativprojekte. [!DNL Commerce] -Benutzer können Adobe Stock-Assets schnell finden, in einer Vorschau anzeigen und lizenzieren. Benutzer können sie auch in der [Medienspeicher][media-storage], ohne den Admin-Arbeitsbereich zu verlassen.

## Voraussetzungen

Diese Integration erfordert:

- Ein [Adobe Developer][dev-console] account
- Adobe Commerce oder Magento Open Source, 2.3.4 oder höher

Für das Lizenzieren von Adobe Stock-Bildern ist Folgendes erforderlich:

- Ein [Adobe-Konto][adobe-signin]
- Gebührenpflichtig [Adobe Stock][adobe-stock] mit dem Konto verknüpfter Plan

## Integrieren [!DNL Commerce] und Adobe Stock

Die Konfiguration der Adobe Stock-Integration für Adobe Commerce erfolgt in zwei Schritten:

1. [Erstellen einer adobe.developer-Integration](#create-an-adobe-developer-integration) zum Generieren eines API-Schlüssels
1. [Konfigurieren der Adobe Stock-Integration in Commerce Admin](#configure-the-adobe-stock-integration)

### Erstellen einer Adobe Developer-Integration

1. Navigieren Sie zum [Adobe Developer-Konsole][dev-console].

1. under _[!UICONTROL Quick Start]_klicken **[!UICONTROL Create new project]**.

1. Im _[!UICONTROL Project overview]_Block, klicken Sie **[!UICONTROL Add API]**.

1. Auswählen **[!UICONTROL Adobe Stock]** aus der Integrationsliste aus und klicken Sie auf **[!UICONTROL Next]**.

1. OAuth 2.0 auswählen **[!UICONTROL Web App]**.

1. Geben Sie die **[!UICONTROL redirect URI]**.

   Der standardmäßige Umleitungs-URI befindet sich im Formular `${HOST}/${ADMIN_URI}/adobe_ims/oauth/callback/`, beispielsweise `https://store.myshop.com/admin_hgkq1l/adobe_ims/oauth/callback/`, wobei:

   - `${HOST}` ist [!DNL Commerce] vollständig qualifizierter Domänenname (z. B. `https://store.myshop.com`).
   - `${ADMIN_URI}` ist [!DNL Commerce] Admin-URI (z. B. `admin_hgkq1l`), die durch Ausführen abgerufen werden können `magento info:adminuri`.

1. Geben Sie die **[!UICONTROL Redirect URI pattern]**, der mit Ihrem Umleitungs-URI identisch ist, allerdings mit zwei Unterschieden:

   - Alle Punkte (`.`) muss mit zwei umgekehrten Schrägstrichen (`\\`).
   - Hinzufügen `.*` am Ende des Musters.

   Wenn Sie das Beispiel aus dem vorherigen standardmäßigen Umleitungs-URI verwenden, wäre es `https://store\\.myshop\\.com/admin_hgkq1l/adobe_ims/oauth/callback/.*`.

1. Klicken **[!UICONTROL Next]**.

1. Überprüfen Sie die verfügbaren Bereiche und klicken Sie auf **[!UICONTROL Save configured API]**.

1. Kopieren Sie auf der folgenden Seite Ihre **[!UICONTROL Client ID]** (API-Schlüssel) und **[!UICONTROL Client secret]**.

   Diese Informationen werden in Schritten des nächsten Abschnitts verwendet.

### Konfigurieren der Adobe Stock-Integration

So legen Sie die Systemkonfiguration in Ihrer [!DNL Commerce] Admin, verwenden Sie _API-Schlüssel_ und _Client-Geheimschlüssel_ in der [vorheriger Abschnitt][create-integration].

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Advanced]** und wählen **[!UICONTROL System]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) **[!UICONTROL Adobe Stock Integration]** und gehen Sie wie folgt vor:

   - Satz **[!UICONTROL Enabled Adobe Stock]** nach `Yes`.

   - Geben Sie Ihre **[!UICONTROL API Key (Client ID)]**.

   - Geben Sie Ihre **[!UICONTROL Client Secret]**.

   - Klicks **[!UICONTROL Test Connection]** , um Ihre Schlüssel zu validieren.

   ![Erweiterte Konfiguration - Adobe Stock-Integration](./assets/system-adobe-stock-integration.png){width="600" zoomable="yes"}

   Geben Sie der Überprüfung einige Sekunden. Wenn Ihre Anmeldedaten gültig sind, sollte eine grüne _Verbindung erfolgreich!_ Nachricht.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

[adobe-stock]: https://stock.adobe.com
[adobe-signin]: https://helpx.adobe.com/manage-account/using/access-adobe-id-account.html
[media-storage]: media-storage.md
[dev-console]: https://developer.adobe.com/console/home
[create-integration]: #create-an-adobeio-integration
