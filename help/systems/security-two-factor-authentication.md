---
title: Zweifaktorauthentifizierung (2FA)
description: Erfahren Sie mehr über die Zwei-Faktor-Authentifizierungsunterstützung, um die Sicherheit Ihres Systems und Ihrer Daten zu gewährleisten.
exl-id: d9eb3dd6-4a7b-411a-ac08-0441803cd59a
role: Admin
feature: Configuration, Security, User Account
source-git-commit: 65c15bb84b28088a6e8f06f3592600779ba033f5
workflow-type: tm+mt
source-wordcount: '789'
ht-degree: 0%

---

# Zweifaktorauthentifizierung (2FA)

Commerce _Admin_ für Ihre Adobe Commerce- oder Magento Open Source-Installation bietet Zugriff auf Ihre Store-, Bestellungen- und Kundendaten. Um den nicht autorisierten Zugriff auf Ihre Daten zu verhindern, müssen alle Benutzer, die versuchen, sich bei _Admin_ anzumelden, einen Authentifizierungsprozess abschließen, um ihre Identität zu überprüfen.

>[!NOTE]
>
>Diese Implementierung der Zwei-Faktor-Authentifizierung (2FA) gilt nur für _Admin_ und ist nicht für Kundenkonten verfügbar. Die Zwei-Faktor-Authentifizierung, die Ihr Commerce-Konto schützt, verfügt über eine separate Einrichtung. Weitere Informationen finden Sie unter [Sichern Ihres Commerce-Kontos](../getting-started/commerce-account-secure.md).

Die Authentifizierung mit zwei Faktoren wird häufig verwendet und es kommt häufig vor, Zugriffscodes für verschiedene Websites in derselben App zu generieren. Diese zusätzliche Authentifizierung stellt sicher, dass nur Sie sich bei Ihrem Benutzerkonto anmelden können. Wenn Sie Ihr Passwort verlieren oder ein Bot versucht es zu erraten, fügt die Zwei-Faktor-Authentifizierung eine Schutzschicht hinzu. Beispielsweise können Sie mit dem Google Authenticator Codes für den Administrator Ihres Stores, Ihr Commerce-Konto und Ihr Google-Konto generieren.

![iPhone für die Sicherheitskonfiguration - 2FA](./assets/google-authenticator-iphone.png){width="300"}

Adobe Commerce unterstützt 2FA-Methoden mehrerer Anbieter. Einige erfordern die Installation einer App, die ein einmaliges Kennwort (OTP) generiert, das Benutzer bei der Anmeldung eingeben, um ihre Identität zu überprüfen. Geräte mit dem zweiten universellen Faktor (U2F) ähneln einer Schlüsselfob und generieren einen eindeutigen Schlüssel zur Überprüfung der Identität. Andere Geräte überprüfen die Identität, wenn sie an einen USB-Port angeschlossen werden. Als Store-Administrator können Sie eine oder mehrere der verfügbaren 2FA-Methoden zur Überprüfung der Benutzeridentität benötigen. Ihre 2FA-Konfiguration gilt für alle Websites und Stores, die mit der Adobe Commerce-Installation verbunden sind.

Wenn sich ein Benutzer zum ersten Mal bei _Admin_ anmeldet, muss er jede erforderliche [2FA](../configuration-reference/security/2fa.md) -Methode einrichten und seine Identität mithilfe der zugehörigen App oder des zugehörigen Geräts überprüfen. Nach dieser ersten Einrichtung muss sich der Benutzer bei jeder Anmeldung bei einer der konfigurierten Methoden authentifizieren. Die 2FA-Informationen jedes Benutzers werden in seinem _Admin_ -Konto aufgezeichnet und können bei Bedarf auf [reset](security-two-factor-authentication-manage.md) gesetzt werden. Weitere Informationen zum Anmeldeprozess finden Sie unter [_Admin_ Anmelden](../getting-started/admin-signin.md).

>[!NOTE]
>
>Bei Stores, bei denen die Authentifizierung für Adobe Identity Management Services (IMS) aktiviert wurde, sind die native Adobe Commerce- und Magento Open Source 2FA-Authentifizierung deaktiviert. Admin-Benutzer, die mit ihren Adobe-Anmeldeinformationen bei ihrer Commerce-Instanz angemeldet sind, müssen sich nicht für viele Administratoraufgaben erneut authentifizieren. Die Authentifizierung wird von Adobe IMS verarbeitet, wenn sich der Administrator in seiner aktuellen Sitzung anmeldet. Siehe [Adobe Identity Management Service (IMS)-Integrationsübersicht](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html).

Sie können sich dieses [Video-Demo](https://video.tv.adobe.com/v/339104?quality=12&learn=on) ansehen, um einen Überblick über die Zwei-Faktor-Authentifizierung im Admin zu erhalten.

## Konfigurieren der erforderlichen 2FA-Anbieter

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Security]** und wählen Sie **[!UICONTROL 2FA]** aus.

1. Wählen Sie im Abschnitt _[!UICONTROL General]_die zu verwendenden Provider aus.

   | Anbieter | Funktion |
   |--- |--- |
   | [!UICONTROL Google Authenticator] | Generiert ein einmaliges Kennwort in der Anwendung zur Benutzerauthentifizierung. |
   | [!UICONTROL Duo Security] | Stellt SMS- und Push-Benachrichtigungen bereit. |
   | [!UICONTROL Authy] | Erstellt einen zeitabhängigen sechsstelligen Code und stellt einen Schutz oder Token für SMS oder Voice Call 2FA bereit. |
   | [!UICONTROL U2F Devices (Yubikey and others)] | Verwendet ein physisches Gerät zur Authentifizierung, z. B. [[!DNL YubiKey]](https://www.yubico.com/). |

   Um mehrere Methoden auszuwählen, halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie auf jedes Element.

1. Füllen Sie die [Einstellungen](../configuration-reference/security/2fa.md) für jede erforderliche 2FA-Methode aus.

   ![Sicherheitskonfiguration - 2FA](../configuration-reference/security/assets/2fa-general.png){width="600" zoomable="yes"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

   Wenn sich Benutzer zum ersten Mal bei _Admin_ anmelden, müssen sie jede erforderliche 2FA-Methode einrichten. Nach dieser Ersteinrichtung müssen sie sich bei jeder Anmeldung bei einer der konfigurierten Methoden authentifizieren.

## 2FA-Provider-Einstellungen

Füllen Sie die Einstellungen für jede erforderliche 2FA-Methode aus.

### Google

Um zu ändern, wie lange das einmalige Kennwort (OTP) während der Anmeldung verfügbar ist, deaktivieren Sie das Kontrollkästchen **[!UICONTROL Use system value]** . Geben Sie dann die Anzahl der Sekunden ein, für die die **[!UICONTROL OTP Window]** gültig sein soll.

![Sicherheitskonfiguration - Google](../configuration-reference/security/assets/2fa-google.png){width="600" zoomable="yes"}

>[!NOTE]
>
>In Adobe Commerce 2.4.7 und höher steuert die OTP-Fensterkonfigurationseinstellung, wie lange (in Sekunden) das System das einmalige Kennwort (OTP) eines Administrators nach dessen Ablauf akzeptiert. Dieser Wert muss weniger als 30 Sekunden betragen. Die Standardeinstellung des Systems ist `29`.<br><br> In Version 2.4.6 bestimmt die OTP-Fenstereinstellung die Anzahl vergangener und zukünftiger OTP-Codes, die gültig bleiben. Der Wert &quot;`1`&quot;zeigt an, dass der aktuelle OTP-Code plus ein Code in der Vergangenheit und ein Code in der Zukunft jederzeit gültig bleiben.

### [!DNL Duo Security]

Geben Sie die folgenden Anmeldedaten aus Ihrem Duo Security-Konto ein:

- Integrationsschlüssel
- Geheimer Schlüssel
- API-Hostname

![Sicherheitskonfiguration - Duo](../configuration-reference/security/assets/2fa-duo-security.png){width="600" zoomable="yes"}

### [!DNL Authy]

1. Geben Sie den API-Schlüssel aus Ihrem [!DNL Authy] -Konto ein.

1. Um die Standardmeldung zu ändern, die während der Authentifizierung angezeigt wird, deaktivieren Sie das Kontrollkästchen **[!UICONTROL Use system value]** . Geben Sie dann den **[!UICONTROL OneTouch Message]** ein, der angezeigt werden soll.

   ![Sicherheitskonfiguration - Authy](../configuration-reference/security/assets/2fa-authy.png){width="600" zoomable="yes"}

### U2F-Geräte ([!DNL Yubikey] und andere)

Die Store-Domäne wird standardmäßig während des Authentifizierungsprozesses verwendet. Um eine benutzerdefinierte Domäne für Authentifizierungsprobleme zu verwenden, deaktivieren Sie das Kontrollkästchen **[!UICONTROL Use system value]** . Geben Sie dann den Wert **[!UICONTROL WebAPi Challenge Domain]** ein.

![Sicherheitskonfiguration - U2F-Geräte](../configuration-reference/security/assets/2fa-u2f-key.png){width="600" zoomable="yes"}
