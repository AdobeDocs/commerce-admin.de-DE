---
title: '[!UICONTROL Security] &gt; [!UICONTROL 2FA]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Security] &gt; [!UICONTROL 2FA] des Commerce-Administrators.
exl-id: d3f6e16b-6eba-47db-a9dd-cb3268d1a13f
feature: Configuration, Security
source-git-commit: 65c15bb84b28088a6e8f06f3592600779ba033f5
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 1%

---

# [!UICONTROL Security] > [!UICONTROL 2FA]

>[!NOTE]
>
>Bei Stores, bei denen die Authentifizierung für Adobe Identity Management Services (IMS) aktiviert wurde, sind die native Adobe Commerce- und die Magento Open Source-Zweifaktorauthentifizierung (2FA) deaktiviert. Admin-Benutzer, die mit ihren Adobe-Anmeldeinformationen bei ihrer Adobe Commerce-Instanz angemeldet sind, müssen sich nicht für viele Administratoraufgaben erneut authentifizieren. Die Authentifizierung wird von Adobe IMS verarbeitet, wenn sich der Administrator in seiner aktuellen Sitzung anmeldet. Siehe [Überblick über die Integration von Adobe Commerce in Adobe IMS](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html).

{{config}}

Weitere Informationen zum Ändern dieser Einstellungen finden Sie unter [Zweifaktorauthentifizierung (2FA)](../../systems/security-two-factor-authentication.md) im _Administratorsystemhandbuch_.

## [!UICONTROL General]

![Allgemein](./assets/2fa-general.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Providers to use] | Global | Gibt die zweifaktoriellen Authentifizierungsmethoden an, die Sie benötigen. Wenn Sie mehr als einen Anbieter auswählen, muss jeder Benutzer bei der nächsten Anmeldung jede 2FA-Methode konfigurieren. |
| [!UICONTROL Configuration Email URL for Web API] | Global | Bei benutzerdefinierten Implementierungen die URL für einen alternativen E-Mail-Konfigurationslink, der bei der ersten Anmeldung an _Admin_ -Benutzer gesendet wird. Verwenden Sie in der E-Mail-Vorlage den Platzhalter `:tfat`, um anzugeben, wo das Token eingefügt wird. |
| [!UICONTROL Retry attempt limit for Two-Factor Authentication] | Global | Bestimmt, wie oft ein Administrator einen &quot;[!DNL one-time password (OTP)]&quot;-Wert eingeben kann, bevor sein Konto vorübergehend deaktiviert wird. Standard: `10` |
| [!UICONTROL Two-Factor Authentication lockout time (seconds)] | Global | Bestimmt, wie lange (in Sekunden) ein Administrator warten kann, bis er einen [!DNL one-time password (OTP)] eingibt, bevor sein Konto vorübergehend deaktiviert wird. Standard: `300` |

{style="table-layout:auto"}

## [!UICONTROL Google]

![Google](./assets/2fa-google.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL OTP Window] | Global | Bestimmt, wie lange (in Sekunden) das System die [!DNL one-time-password (OTP)] eines Administrators akzeptiert, nachdem sie abgelaufen ist. Darf nicht länger sein als die Lebensdauer eines einzelnen OTP (normalerweise 30 Sekunden). Standard: `29` |

{style="table-layout:auto"}

## [!UICONTROL Duo Security]

![Duo Sicherheit](./assets/2fa-duo-security.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Integration Key] | Global | Der Integrationsschlüssel aus Ihrem [!DNL Duo Security] -Konto. |
| [!UICONTROL Secret Key] | Global | Der geheime Schlüssel aus Ihrem [!DNL Duo Security] -Konto. |
| [!UICONTROL API Hostname] | Global | Der API-Hostname aus Ihrem [!DNL Duo Security]-Konto. |

{style="table-layout:auto"}

## [!UICONTROL Authy]

![Authy](./assets/2fa-authy.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL API Key] | Global | Der API-Schlüssel aus Ihrem [!DNL Authy] -Konto. |
| [!UICONTROL OneTouch Message] | Global | Die Meldung, die bei der Anmeldung im [!DNL Authy] -Authentifizierer angezeigt wird. Standard: `Login request to your Magento Admin` |

{style="table-layout:auto"}

## [!UICONTROL U2F Key]

![U2F-Schlüssel](./assets/2fa-u2f-key.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL WebApi Challenge Domain] | Global | Die Domäne, die verwendet wird, um [!DNL WebAuthn] -Herausforderungen für benutzerdefinierte WebAPI-Implementierungen auszugeben und zu verarbeiten. |

{style="table-layout:auto"}
