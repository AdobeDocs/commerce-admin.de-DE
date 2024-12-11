---
title: Adobe Stock-Integration
description: Integrieren Sie Adobe Stock in Ihre [!DNL Commerce] Instanz, um auf unzählige Medien-Assets zuzugreifen, die in Ihrem Store verwendet werden können.
exl-id: 0f399ea7-5726-476c-a945-c37e44a9ea55
feature: CMS, Media, Configuration, Integration
source-git-commit: 0d072ecdba696383bd33b88b64d751736429f2f6
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 0%

---

# Adobe Stock-Integration

Um Zugriff auf unzählige Medien-Assets zu erhalten, die in Ihrem Store verwendet werden können, integrieren Sie [Adobe Stock][adobe-stock] mit [!UICONTROL Commerce].

![Adobe Stock-Suchergebnisse](./assets/adobe-stock-search-grid.png){width="700" zoomable="yes"}

Der Adobe Stock-Dienst bietet Unternehmen Zugang zu Millionen von hochwertigen, kuratierten und gebührenfreien Fotos, Vektorgrafiken, Illustrationen, Videos, Vorlagen und 3D-Assets für alle Kreativprojekte. [!DNL Commerce] -Benutzer können Adobe Stock-Assets schnell finden, in einer Vorschau anzeigen und lizenzieren. Benutzer können sie auch im [Medienspeicher](./media-storage.md) speichern, ohne den Admin Workspace verlassen zu müssen.

## Voraussetzungen

Diese Integration erfordert:

- Ein [Adobe Developer][dev-console] -Konto
- Adobe Commerce oder Magento Open Source, 2.3.4 oder höher

Für das Lizenzieren von Adobe Stock-Bildern ist Folgendes erforderlich:

- Ein [Adobe-Konto][adobe-signin]
- Ein bezahlter [Adobe Stock][adobe-stock]-Plan, der mit dem Konto verknüpft ist

## Integrieren von [!DNL Commerce] und Adobe Stock

Die Konfiguration der Adobe Stock-Integration für Adobe Commerce erfolgt in zwei Schritten:

1. [Erstellen einer adobe.developer-Integration](#create-an-adobe-developer-integration) zum Generieren eines API-Schlüssels
1. [Konfigurieren der Adobe Stock-Integration in Commerce Admin](#configure-the-adobe-stock-integration)

### Erstellen einer Adobe Developer-Integration

1. Navigieren Sie zur [Adobe Developer Console][dev-console].

1. Klicken Sie unter _[!UICONTROL Quick Start]_auf **[!UICONTROL Create new project]**.

1. Klicken Sie im Block _[!UICONTROL Project overview]_auf **[!UICONTROL Add API]**.

1. Wählen Sie **[!UICONTROL Adobe Stock]** aus der Integrationsliste und klicken Sie auf **[!UICONTROL Next]**.

1. Wählen Sie OAuth 2.0 **[!UICONTROL Web App]** aus.

1. Geben Sie den Wert **[!UICONTROL redirect URI]** an.

   Der standardmäßige Umleitungs-URI hat das Format `${HOST}/${ADMIN_URI}/adobe_ims/oauth/callback/`, z. B. `https://store.myshop.com/admin_hgkq1l/adobe_ims/oauth/callback/`, wobei:

   - `${HOST}` ist Ihr [!DNL Commerce] voll qualifizierter Domänenname (z. B. `https://store.myshop.com`).
   - `${ADMIN_URI}` ist Ihr [!DNL Commerce] Admin-URI (z. B. `admin_hgkq1l`), der durch Ausführen von `magento info:adminuri` abgerufen werden kann.

1. Geben Sie den **[!UICONTROL Redirect URI pattern]** -Wert an, der mit dem Umleitungs-URI identisch ist, allerdings mit zwei Unterschieden:

   - Alle Punkte (`.`) müssen mit zwei umgekehrten Schrägstrichen (`\\`) maskiert werden.
   - Fügen Sie am Ende des Musters `.*` hinzu.

   Unter Verwendung des Beispiels aus dem vorherigen standardmäßigen Umleitungs-URI wäre es `https://store\\.myshop\\.com/admin_hgkq1l/adobe_ims/oauth/callback/.*`.

1. Klicken Sie auf **[!UICONTROL Next]**.

1. Überprüfen Sie die verfügbaren Bereiche und klicken Sie auf &quot;**[!UICONTROL Save configured API]**&quot;.

1. Kopieren Sie auf der folgenden Seite Ihre **[!UICONTROL Client ID]** (API-Schlüssel) und **[!UICONTROL Client secret]**.

   Diese Informationen werden in Schritten des nächsten Abschnitts verwendet.

### Konfigurieren der Adobe Stock-Integration

Um die Systemkonfiguration in Ihrem [!DNL Commerce] -Admin festzulegen, verwenden Sie den _API-Schlüssel_ und den _Client-geheimen Schlüssel_, die im [vorherigen Abschnitt][create-integration] generiert wurden.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Advanced]** und wählen Sie **[!UICONTROL System]** aus.

1. Erweitern Sie ![Erweiterungsselektor](../assets/icon-display-expand.png) **[!UICONTROL Adobe Stock Integration]** und führen Sie folgende Schritte aus:

   - Setzen Sie **[!UICONTROL Enabled Adobe Stock]** auf `Yes`.

   - Geben Sie Ihren **[!UICONTROL API Key (Client ID)]** ein.

   - Geben Sie Ihren **[!UICONTROL Client Secret]** ein.

   - Klicken Sie auf **[!UICONTROL Test Connection]** , um Ihre Schlüssel zu überprüfen.

   ![Erweiterte Konfiguration - Adobe Stock-Integration](./assets/system-adobe-stock-integration.png){width="600" zoomable="yes"}

   Geben Sie der Überprüfung einige Sekunden. Wenn Ihre Anmeldedaten gültig sind, sollte eine grüne _Verbindung erfolgreich hergestellt! angezeigt werden._ -Meldung.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

[adobe-stock]: https://stock.adobe.com
[adobe-signin]: https://helpx.adobe.com/manage-account/using/access-adobe-id-account.html
[dev-console]: https://developer.adobe.com/console/home
[create-integration]: #create-an-adobeio-integration
