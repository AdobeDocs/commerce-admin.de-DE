---
title: Zwei-Faktor-Authentifizierung (2FA)
description: Erfahren Sie mehr über die Unterstützung der Zwei-Faktor-Authentifizierung, um die Sicherheit Ihres Systems und Ihrer Daten zu gewährleisten.
exl-id: d9eb3dd6-4a7b-411a-ac08-0441803cd59a
role: Admin
feature: Configuration, Security, User Account
source-git-commit: 4997c4c01f11d6e0355eb8e02f8f099db685b400
workflow-type: tm+mt
source-wordcount: '793'
ht-degree: 0%

---

# Zwei-Faktor-Authentifizierung (2FA)

Der Commerce _Admin_ für Ihre Adobe Commerce- oder Magento Open Source-Installation bietet Zugriff auf Ihren Store, Ihre Bestellungen und Ihre Kundendaten. Um den unbefugten Zugriff auf Ihre Daten zu verhindern, müssen alle Benutzer, die versuchen, sich bei _Admin_ anzumelden, einen Authentifizierungsprozess abschließen, um ihre Identität zu überprüfen.

>[!NOTE]
>
>Diese Implementierung der Zwei-Faktor-Authentifizierung (2FA) gilt nur für _Admin_ und ist nicht für Kundenkonten verfügbar. Die Zwei-Faktor-Authentifizierung, die Ihr Commerce-Konto schützt, verfügt über eine separate Einrichtung. Weitere Informationen finden Sie unter [Sichern Ihres Commerce-Kontos](../getting-started/commerce-account-secure.md).

Die Zwei-Faktor-Authentifizierung wird häufig verwendet, und es ist üblich, Zugriffscodes für verschiedene Websites in derselben App zu generieren. Diese zusätzliche Authentifizierung stellt sicher, dass sich nur Sie bei Ihrem Benutzerkonto anmelden können. Wenn Sie Ihr Kennwort verlieren oder ein Bot es erraten hat, bietet die Zwei-Faktor-Authentifizierung eine zusätzliche Schutzschicht. Sie können Google Authenticator beispielsweise verwenden, um Codes für den Administrator Ihrer Geschäft, Ihre Commerce-Konto und Google Konto zu generieren.

![Sicherheitskonfiguration iphone - 2FA](./assets/google-authenticator-iphone.png){width="300"}

Adobe Systems Commerce unterstützt 2FA-Methoden von mehreren Anbietern. Einige erfordern die Installation einer App, die ein einmaliges Kennwort (OTP) generiert, das Benutzer bei der Anmeldung eingeben, um ihre Identität zu überprüfen. Universelle U2F-Geräte (Second Factor) ähneln einem Schlüsselanhänger und erzeugen einen eindeutigen Schlüssel zur Überprüfung der Identität. Andere Geräte verifizieren ihre Identität, wenn sie in eine USB-portieren eingesteckt werden. Als Geschäft Administrator können Sie eine oder mehrere der verfügbaren 2FA-Methoden zur Überprüfung User Identität benötigen. Deine 2FA-Konfiguration gilt für alle Websites und Shops, die mit der Adobe Systems Commerce-Installation verknüpft sind.

Wenn sich ein Benutzer zum ersten Mal bei _Admin_ anmeldet, muss er jede gewünschte [2FA](../configuration-reference/security/2fa.md)-Methode einrichten und seine Identität mithilfe der zugehörigen App oder des zugehörigen Geräts überprüfen. Nach dieser Ersteinrichtung muss sich der Benutzer bei jeder Anmeldung mit einer der konfigurierten Methoden authentifizieren. Die 2FA-Informationen jedes Benutzers werden in seinem _Admin_-Konto aufgezeichnet und können bei [ zurückgesetzt ](security-two-factor-authentication-manage.md). Weitere Informationen zum Anmeldevorgang finden Sie unter [_Admin_ Sign-In](../getting-started/admin-signin.md).

>[!NOTE]
>
>Bei Stores, für die die Adobe Identity Management Services (IMS)-Authentifizierung aktiviert ist, sind native Adobe Commerce- und Magento Open Source 2FA-Dienste deaktiviert. Admin-Benutzende, die mit ihren Adobe-Anmeldeinformationen bei ihrer Commerce-Instanz angemeldet sind, müssen sich für viele Admin-Aufgaben nicht erneut authentifizieren. Die Authentifizierung wird von Adobe IMS durchgeführt, wenn sich der Administrator bei seiner aktuellen Sitzung anmeldet. Siehe Übersicht über die Integration von [Adobe Identity Management Service (IMS)](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html).

In dieser [Videodemo](https://video.tv.adobe.com/v/339104?quality=12&learn=on) erhalten Sie einen Überblick über die Zwei-Faktor-Authentifizierung in der Admin-Verwaltung.

## Konfigurieren der erforderlichen 2FA-Provider

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Security]** und wählen Sie **[!UICONTROL 2FA]**.

1. Wählen Sie im Abschnitt _[!UICONTROL General]_&#x200B;die zu verwendenden Provider aus.

   | Lieferant | Funktion |
   |--- |--- |
   | [!UICONTROL Google Authenticator] | Erzeugt ein einmaliges Passwort in der Anwendung zur Benutzerauthentifizierung. |
   | [!UICONTROL Duo Security] | Bietet SMS- und Push-Benachrichtigungen. |
   | [!UICONTROL Authy] | Erstellt einen zeitabhängigen sechsstelligen Code und stellt den Schutz oder das Token für SMS oder Voice Call 2FA bereit. |
   | [!UICONTROL U2F Devices (Yubikey and others)] | Verwendet ein physisches Gerät zur Authentifizierung, z. B. [[!DNL YubiKey]](https://www.yubico.com/). |

   Zur Auswahl mehrerer Methoden halten Sie die Strg-Taste (PC) bzw. die Befehlstaste (Mac) gedrückt und klicken auf die einzelnen Elemente.

1. Alle Applikationen die [Einstellungen](../configuration-reference/security/2fa.md) für jede erforderliche 2FA-Methode ein.

   ![Sicherheitskonfiguration – 2FA](../configuration-reference/security/assets/2fa-general.png){width="600" zoomable="yes"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

   Wenn sich Benutzer zum ersten Mal beim _Administrator_ anmelden, müssen sie jede erforderliche 2FA-Methode einrichten. Nach dieser Ersteinrichtung müssen sie sich bei jeder Anmeldung mit einer der konfigurierten Methoden authentifizieren.

## 2FA-Anbieter-Einstellungen

Füllen Sie die Einstellungen für jede 2FA-Methode aus, die Sie benötigen.

### Google

Um zu ändern, wie lange das einmalige Kennwort (OTP) während der Anmeldung verfügbar ist, deaktivieren Sie das Kontrollkästchen **[!UICONTROL Use system value]** . Geben Sie dann die Anzahl der Sekunden ein, für die die **[!UICONTROL OTP Window]** gültig sein soll.

![Sicherheitskonfiguration - Google](../configuration-reference/security/assets/2fa-google.png){width="600" zoomable="yes"}

>[!NOTE]
>
>In Adobe Systems Commerce 2.4.7 und höher steuert die Konfigurationseinstellung des OTP-Fensters, wie lange (in Sekunden) das System das One-Time-Kennwort (OTP) eines Administrators akzeptiert, nachdem es abgelaufen ist. Dieser Wert muss weniger als 30 Sekunden betragen. Die Standardeinstellung des Systems ist `29`.<br><br> In Version 2.4.6 bestimmt die Einstellung des OTP-Fensters die Anzahl vergangener und künftiger OTP-Codes, die gültig bleiben. Der Wert `1` gibt an, dass der aktuelle OTP-Code plus ein Code in der Vergangenheit und ein Code in der Zukunft zu einem bestimmten Zeitpunkt gültig bleiben.

### [!DNL Duo Security]

Geben Sie die folgenden Anmeldeinformationen aus Ihrem Duo Security-Konto ein:

- Client-ID
- Client-Geheimnis
- Integrationsschlüssel
- Geheimer Schlüssel
- API-Hostname

![Sicherheitskonfiguration – Duo](../configuration-reference/security/assets/2fa-duo-security.png){width="600" zoomable="yes"}

### [!DNL Authy]

1. Geben Sie den API-Schlüssel in Ihrem [!DNL Authy] Konto ein.

1. Um die Standardmeldung zu ändern, die während der Authentifizierung angezeigt wird, deaktivieren Sie das Kontrollkästchen.**[!UICONTROL Use system value]** Geben Sie dann den **[!UICONTROL OneTouch Message]** ein, der angezeigt werden soll.

   ![Sicherheitskonfiguration - Autorisierung](../configuration-reference/security/assets/2fa-authy.png){width="600" zoomable="yes"}

### U2F-Geräte ([!DNL Yubikey] und andere)

Die Store-Domain wird während des Authentifizierungsprozesses standardmäßig verwendet. Um eine benutzerdefinierte Domain für Authentifizierungsprobleme zu verwenden, deaktivieren Sie das Kontrollkästchen **[!UICONTROL Use system value]** . Geben Sie dann die **[!UICONTROL WebAPi Challenge Domain]** ein.

![Sicherheitskonfiguration – U2F-Geräte](../configuration-reference/security/assets/2fa-u2f-key.png){width="600" zoomable="yes"}
