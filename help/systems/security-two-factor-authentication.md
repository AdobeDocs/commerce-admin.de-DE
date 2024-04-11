---
title: Zweifaktorauthentifizierung (2FA)
description: Erfahren Sie mehr über die Zwei-Faktor-Authentifizierungsunterstützung, um die Sicherheit Ihres Systems und Ihrer Daten zu gewährleisten.
exl-id: d9eb3dd6-4a7b-411a-ac08-0441803cd59a
role: Admin
feature: Configuration, Security, User Account
source-git-commit: c391a3eef8be0dd45cc8a499b63bcb0fc32640aa
workflow-type: tm+mt
source-wordcount: '786'
ht-degree: 0%

---

# Zweifaktorauthentifizierung (2FA)

Die Commerce _Admin_ für Ihre Adobe Commerce- oder Magento Open Source-Installation bietet Zugriff auf Ihre Store-, Bestellungen- und Kundendaten. Um den nicht autorisierten Zugriff auf Ihre Daten zu verhindern, müssen alle Benutzer, die versuchen, sich bei der _Admin_ muss einen Authentifizierungsprozess abschließen, um ihre Identität zu überprüfen.

>[!NOTE]
>
>Diese Implementierung der Zwei-Faktor-Authentifizierung (2FA) gilt für die _Admin_ und ist nicht für Kundenkonten verfügbar. Die Zwei-Faktor-Authentifizierung, die Ihr Commerce-Konto schützt, verfügt über eine separate Einrichtung. Weitere Informationen finden Sie unter [Sichern Ihres Commerce-Kontos](../getting-started/commerce-account-secure.md).

Die Authentifizierung mit zwei Faktoren wird häufig verwendet und es kommt häufig vor, Zugriffscodes für verschiedene Websites in derselben App zu generieren. Diese zusätzliche Authentifizierung stellt sicher, dass nur Sie sich bei Ihrem Benutzerkonto anmelden können. Wenn Sie Ihr Passwort verlieren oder ein Bot versucht es zu erraten, fügt die Zwei-Faktor-Authentifizierung eine Schutzschicht hinzu. Beispielsweise können Sie mit dem Google Authenticator Codes für den Administrator Ihres Stores, Ihr Commerce-Konto und Ihr Google-Konto generieren.

![iPhone für Sicherheitskonfiguration - 2FA](./assets/google-authenticator-iphone.png){width="300"}

Adobe Commerce unterstützt 2FA-Methoden mehrerer Anbieter. Einige erfordern die Installation einer App, die ein einmaliges Kennwort (OTP) generiert, das Benutzer bei der Anmeldung eingeben, um ihre Identität zu überprüfen. Geräte mit dem zweiten universellen Faktor (U2F) ähneln einer Schlüsselfob und generieren einen eindeutigen Schlüssel zur Überprüfung der Identität. Andere Geräte überprüfen die Identität, wenn sie an einen USB-Port angeschlossen werden. Als Store-Administrator können Sie eine oder mehrere der verfügbaren 2FA-Methoden zur Überprüfung der Benutzeridentität benötigen. Ihre 2FA-Konfiguration gilt für alle Websites und Stores, die mit der Adobe Commerce-Installation verbunden sind.

Wenn sich ein Benutzer zum ersten Mal bei der _Admin_, müssen sie [2FA](../configuration-reference/security/2fa.md) -Methode verwenden und ihre Identität mithilfe der zugehörigen App oder des zugehörigen Geräts überprüfen. Nach dieser ersten Einrichtung muss sich der Benutzer bei jeder Anmeldung bei einer der konfigurierten Methoden authentifizieren. Die 2FA-Informationen jedes Benutzers werden in seiner _Admin_ und kann [reset](security-two-factor-authentication-manage.md) falls erforderlich. Weitere Informationen zum Anmeldeprozess finden Sie unter [_Admin_ Anmelden](../getting-started/admin-signin.md).

>[!NOTE]
>
>Bei Stores, bei denen die Authentifizierung für Adobe Identity Management Services (IMS) aktiviert wurde, sind die native Adobe Commerce- und Magento Open Source 2FA-Authentifizierung deaktiviert. Admin-Benutzer, die mit ihren Adobe-Anmeldeinformationen bei ihrer Commerce-Instanz angemeldet sind, müssen sich nicht für viele Administratoraufgaben erneut authentifizieren. Die Authentifizierung wird von Adobe IMS verarbeitet, wenn sich der Administrator in seiner aktuellen Sitzung anmeldet. Siehe [Integrationsübersicht für Adobe Identity Management Service (IMS)](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html).

Sie können sich das ansehen [Video-Demo](https://video.tv.adobe.com/v/339104?quality=12&learn=on) für einen Überblick über die Zwei-Faktor-Authentifizierung im Admin.

## Konfigurieren der erforderlichen 2FA-Anbieter

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Security]** und wählen **[!UICONTROL 2FA]**.

1. Im _[!UICONTROL General]_die zu verwendenden Anbieter auswählen.

   | Anbieter | Funktion |
   |--- |--- |
   | [!UICONTROL Google Authenticator] | Generiert ein einmaliges Kennwort in der Anwendung zur Benutzerauthentifizierung. |
   | [!UICONTROL Duo Security] | Stellt SMS- und Push-Benachrichtigungen bereit. |
   | [!UICONTROL Authy] | Erstellt einen zeitabhängigen sechsstelligen Code und stellt einen Schutz oder Token für SMS oder Voice Call 2FA bereit. |
   | [!UICONTROL U2F Devices (Yubikey and others)] | Verwendet ein physisches Gerät zur Authentifizierung, z. B. [[!DNL YubiKey]](https://www.yubico.com/). |

   Um mehrere Methoden auszuwählen, halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie auf jedes Element.

1. Führen Sie die Einstellungen für jede erforderliche 2FA-Methode aus.

   ![Sicherheitskonfiguration - 2FA](../configuration-reference/security/assets/2fa-general.png){width="600" zoomable="yes"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

   Erstmalige Anmeldung bei der _Admin_ müssen sie jede erforderliche 2FA-Methode einrichten. Nach dieser Ersteinrichtung müssen sie sich bei jeder Anmeldung bei einer der konfigurierten Methoden authentifizieren.

## 2FA-Provider-Einstellungen

Füllen Sie die Einstellungen für jede erforderliche 2FA-Methode aus.

### Google

Um zu ändern, wie lange das einmalige Kennwort (OTP) während der Anmeldung verfügbar ist, löschen Sie die **[!UICONTROL Use system value]** aktivieren. Geben Sie dann die gewünschte Anzahl von Sekunden ein. **[!UICONTROL OTP Window]** gültig sein.

>[!NOTE]
>
>In Adobe Commerce 2.4.7 und höher steuert die OTP-Fensterkonfigurationseinstellung, wie lange (in Sekunden) das System das einmalige Kennwort (OTP) eines Administrators nach dessen Ablauf akzeptiert. Dieser Wert muss weniger als 30 Sekunden betragen. Die Standardeinstellung des Systems lautet `1`.<br><br> In Version 2.4.6 bestimmt die OTP-Fenstereinstellung die Anzahl der vergangenen und zukünftigen OTP-Codes, die gültig bleiben. Ein Wert von `1` gibt an, dass der aktuelle OTP-Code sowie ein Code in der Vergangenheit und ein Code in der Zukunft zu jedem beliebigen Zeitpunkt gültig bleiben.

### [!DNL Duo Security]

Geben Sie die folgenden Anmeldedaten aus Ihrem Duo Security-Konto ein:

- Integrationsschlüssel
- Geheimer Schlüssel
- API-Hostname

![Sicherheitskonfiguration - Duo](../configuration-reference/security/assets/2fa-duo-security.png){width="600" zoomable="yes"}

### [!DNL Authy]

1. Geben Sie den API-Schlüssel aus Ihrem [!DNL Authy] -Konto.

1. Um die Standardmeldung zu ändern, die während der Authentifizierung angezeigt wird, löschen Sie die **[!UICONTROL Use system value]** aktivieren. Geben Sie dann die **[!UICONTROL OneTouch Message]** , die Sie anzeigen möchten.

   ![Sicherheitskonfiguration - Authoring](../configuration-reference/security/assets/2fa-authy.png){width="600" zoomable="yes"}

### U2F-Geräte ([!DNL Yubikey] und andere)

Die Store-Domäne wird standardmäßig während des Authentifizierungsprozesses verwendet. Um eine benutzerdefinierte Domäne für Authentifizierungsprobleme zu verwenden, löschen Sie die **[!UICONTROL Use system value]** aktivieren. Geben Sie dann die **[!UICONTROL WebAPi Challenge Domain]**.

![Sicherheitskonfiguration - U2F-Geräte](../configuration-reference/security/assets/2fa-u2f-key.png){width="600" zoomable="yes"}
