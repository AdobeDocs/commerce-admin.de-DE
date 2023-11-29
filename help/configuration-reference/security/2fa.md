---
title: '[!UICONTROL Security] &gt; [!UICONTROL 2FA]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der [!UICONTROL Security] &gt; [!UICONTROL 2FA] Seite des Commerce-Administrators.
exl-id: d3f6e16b-6eba-47db-a9dd-cb3268d1a13f
feature: Configuration, Security
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 1%

---

# [!UICONTROL Security] > [!UICONTROL 2FA]

>[!NOTE]
>
>Bei Stores, bei denen die Authentifizierung für Adobe Identity Management Services (IMS) aktiviert wurde, sind die native Adobe Commerce- und die Magento Open Source-Zweifaktorauthentifizierung (2FA) deaktiviert. Admin-Benutzer, die mit ihren Adobe-Anmeldeinformationen bei ihrer Adobe Commerce-Instanz angemeldet sind, müssen sich nicht für viele Administratoraufgaben erneut authentifizieren. Die Authentifizierung wird von Adobe IMS verarbeitet, wenn sich der Administrator in seiner aktuellen Sitzung anmeldet. Siehe [Überblick über die Integration von Adobe Commerce mit Adobe IMS](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html).

{{config}}

Weitere Informationen zum Ändern dieser Einstellungen finden Sie unter [Zweifaktorauthentifizierung (2FA)](../../systems/security-two-factor-authentication.md) im _Administratorsystemanleitung_.

## [!UICONTROL General]

![Allgemein](./assets/2fa-general.png)<!-- zoom -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Providers to use] | Global | Gibt die zweifaktoriellen Authentifizierungsmethoden an, die Sie benötigen. Wenn Sie mehr als einen Anbieter auswählen, muss jeder Benutzer bei der nächsten Anmeldung jede 2FA-Methode konfigurieren. |
| [!UICONTROL Configuration Email URL for Web API] | Global | Bei benutzerdefinierten Implementierungen die URL für einen alternativen E-Mail-Konfigurationslink, der an gesendet wird _Admin_ Benutzer bei der ersten Anmeldung. Verwenden Sie in der E-Mail-Vorlage den Platzhalter `:tfat` , um anzugeben, wo das Token eingefügt wird. |

{style="table-layout:auto"}

## [!UICONTROL Google]

![Google](./assets/2fa-google.png)<!-- zoom -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL OTP Window] | Global | Die Lebensdauer in Sekunden jedes einmaligen Kennworts (OTP), das vom Google Authenticator generiert wurde. Standard: `30` |

{style="table-layout:auto"}

## [!UICONTROL Duo Security]

![Duo Sicherheit](./assets/2fa-duo-security.png)<!-- zoom -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Integration Key] | Global | Der Integrationsschlüssel Ihrer [!DNL Duo Security] -Konto. |
| [!UICONTROL Secret Key] | Global | Der geheime Schlüssel von Ihrem [!DNL Duo Security] -Konto. |
| [!UICONTROL API Hostname] | Global | Der API-Hostname von Ihrer [!DNL Duo Security] -Konto. |

{style="table-layout:auto"}

## [!UICONTROL Authy]

![Autor](./assets/2fa-authy.png)<!-- zoom -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL API Key] | Global | Der API-Schlüssel von Ihrer [!DNL Authy] -Konto. |
| [!UICONTROL OneTouch Message] | Global | Die Meldung, die im [!DNL Authy] Authentifizierer bei der Anmeldung. Standard: `Login request to your Magento Admin` |

{style="table-layout:auto"}

## [!UICONTROL U2F Key]

![U2F-Schlüssel](./assets/2fa-u2f-key.png)<!-- zoom -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL WebApi Challenge Domain] | Global | Die Domäne, die für die Ausgabe und Verarbeitung verwendet wird [!DNL WebAuthn] Herausforderungen bei benutzerdefinierten WebAPI-Implementierungen. |

{style="table-layout:auto"}
