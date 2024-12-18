---
title: Adobe Stock-Integration
description: Integrieren Sie Adobe Stock in Ihre  [!DNL Commerce] , um auf unzählige Medien-Assets zur Verwendung in Ihrem Store zuzugreifen.
exl-id: 0f399ea7-5726-476c-a945-c37e44a9ea55
feature: CMS, Media, Configuration, Integration
source-git-commit: 0d072ecdba696383bd33b88b64d751736429f2f6
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 0%

---

# Adobe Stock-Integration

Um Zugriff auf unzählige Medien-Assets für die Verwendung in Ihrem Store zu erhalten, integrieren Sie [Adobe Stock][adobe-stock] mit [!UICONTROL Commerce].

![Adobe Stock-Suchergebnisse](./assets/adobe-stock-search-grid.png){width="700" zoomable="yes"}

Der Adobe Stock-Service bietet Unternehmen Zugriff auf Millionen von hochwertigen, kuratierten und gebührenfreien Fotos, Vektorgrafiken, Illustrationen, Videos, Vorlagen und 3D-Assets für alle Kreativprojekte. [!DNL Commerce] Benutzer können Adobe Stock-Assets schnell finden, eine Vorschau anzeigen und lizenzieren. Benutzer können sie auch im [Medienspeicher](./media-storage.md) speichern, ohne den Admin-Arbeitsbereich verlassen zu müssen.

## Voraussetzungen

Diese Integration erfordert:

- Ein [Adobe Developer][dev-console]-Konto
- Adobe Commerce oder Magento Open Source, 2.3.4 oder höher

Die Lizenzierung von Adobe Stock-Bildern erfordert Folgendes:

- Ein [Adobe-Konto][adobe-signin]
- Ein gebührenpflichtiger [Adobe Stock][adobe-stock]-Plan, der mit dem Konto verknüpft ist

## Integrieren von [!DNL Commerce] und Adobe Stock

Die Konfiguration der Adobe Stock-Integration für Adobe Commerce erfolgt in zwei Schritten:

1. [Erstellen einer „adobe.developer“-Integration](#create-an-adobe-developer-integration) um einen API-Schlüssel zu generieren
1. [Konfigurieren der Adobe Stock-Integration in Commerce Admin](#configure-the-adobe-stock-integration)

### Erstellen einer Adobe Developer-Integration

1. Navigieren Sie zur [Adobe Developer Console][dev-console].

1. Klicken Sie unter _[!UICONTROL Quick Start]_auf **[!UICONTROL Create new project]**.

1. Klicken Sie im _[!UICONTROL Project overview]_auf **[!UICONTROL Add API]**.

1. Wählen Sie **[!UICONTROL Adobe Stock]** aus der Liste Integrationen aus und klicken Sie auf **[!UICONTROL Next]**.

1. Wählen Sie die OAuth 2.0-**[!UICONTROL Web App]** aus.

1. Geben Sie die **[!UICONTROL redirect URI]** an.

   Der standardmäßige Umleitungs-URI befindet sich in der `${HOST}/${ADMIN_URI}/adobe_ims/oauth/callback/`, z. B. `https://store.myshop.com/admin_hgkq1l/adobe_ims/oauth/callback/`, wobei:

   - `${HOST}` ist Ihr [!DNL Commerce] vollständig qualifizierter Domain-Name (z. B. `https://store.myshop.com`).
   - `${ADMIN_URI}` ist Ihr [!DNL Commerce] Admin-URI (z. B. `admin_hgkq1l`), der durch Ausführen von `magento info:adminuri` abgerufen werden kann.

1. Geben Sie den **[!UICONTROL Redirect URI pattern]** an, der mit dem Umleitungs-URI identisch ist, jedoch zwei Unterschiede aufweist:

   - Alle Punkte (`.`) müssen mit zwei umgekehrten Schrägstrichen (`\\`) escaped werden.
   - Fügen Sie `.*` am Ende des Musters hinzu.

   Unter Verwendung des Beispiels aus dem vorherigen standardmäßigen Weiterleitungs-URI würde er `https://store\\.myshop\\.com/admin_hgkq1l/adobe_ims/oauth/callback/.*`.

1. Klicken Sie auf **[!UICONTROL Next]**.

1. Überprüfen Sie die verfügbaren Bereiche und klicken Sie auf **[!UICONTROL Save configured API]**.

1. Kopieren Sie auf der folgenden Seite Ihre **[!UICONTROL Client ID]** (API-Schlüssel) und **[!UICONTROL Client secret]**.

   Diese Informationen werden in den Schritten des nächsten Abschnitts verwendet.

### Konfigurieren der Adobe Stock-Integration

Verwenden Sie zum Festlegen der Systemkonfiguration in Ihrem [!DNL Commerce]-Admin den _API-Schlüssel_ und _Client-_), die im [vorherigen Abschnitt][create-integration].

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Advanced]** und wählen Sie **[!UICONTROL System]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) **[!UICONTROL Adobe Stock Integration]** und führen Sie folgende Schritte aus:

   - Legen Sie **[!UICONTROL Enabled Adobe Stock]** auf `Yes` fest.

   - Geben Sie Ihre **[!UICONTROL API Key (Client ID)]** ein.

   - Geben Sie Ihre **[!UICONTROL Client Secret]** ein.

   - Klicken Sie auf **[!UICONTROL Test Connection]** , um Ihre Schlüssel zu validieren.

   ![Erweiterte Konfiguration - Adobe Stock-Integration](./assets/system-adobe-stock-integration.png){width="600" zoomable="yes"}

   Geben Sie der Validierung einige Sekunden Zeit. Wenn Ihre Anmeldeinformationen gültig sind, sollte eine grüne angezeigt werden _Verbindung erfolgreich!Nachricht_.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

[adobe-stock]: https://stock.adobe.com
[adobe-signin]: https://helpx.adobe.com/manage-account/using/access-adobe-id-account.html
[dev-console]: https://developer.adobe.com/console/home
[create-integration]: #create-an-adobeio-integration
