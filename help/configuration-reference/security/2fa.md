---
title: '[!UICONTROL Security] > [!UICONTROL 2FA]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Security] > [!UICONTROL 2FA] des Commerce Admin.
exl-id: d3f6e16b-6eba-47db-a9dd-cb3268d1a13f
feature: Configuration, Security
TQID: https://experienceleague.adobe.com/-5t8bTj14iB%2D%2D%2D88TotUNefATWwE80LTswPO3xVWU70
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 97a3e3469e45ec9c7e3316f1ce5ca7894ea2ddb7
workflow-type: tm+mt
source-wordcount: 342
ht-degree: 2%

---

# [!UICONTROL Security] > [!UICONTROL 2FA]

>[!NOTE]
>
>Bei Stores mit aktivierter Adobe Identity Management Services (IMS)-Authentifizierung sind die native Adobe Commerce- und Magento Open Source-Zwei-Faktor-Authentifizierung (2FA) deaktiviert. Admin-Benutzende, die mit ihren Adobe-Anmeldeinformationen bei ihrer Adobe Commerce-Instanz angemeldet sind, müssen sich für viele Admin-Aufgaben nicht erneut authentifizieren. Die Authentifizierung wird von Adobe IMS durchgeführt, wenn sich der Administrator bei seiner aktuellen Sitzung anmeldet. Siehe [Integrieren von Adobe Commerce mit Adobe IMS - Übersicht](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html).

{{config}}

Weitere Informationen zum Ändern dieser Einstellungen finden Sie unter [Zwei-Faktor-Authentifizierung (2FA](../../systems/security-two-factor-authentication.md) im _Admin-System-Handbuch_.

## [!UICONTROL General]

![Allgemein](./assets/2fa-general.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Providers to use] | Global | Gibt die erforderlichen Zwei-Faktor-Authentifizierungsmethoden an. Wenn Sie mehr als einen Anbieter auswählen, muss jeder Benutzer jede 2FA-Methode bei der nächsten Anmeldung konfigurieren. |
| [!UICONTROL Configuration Email URL for Web API] | Global | Bei benutzerdefinierten Implementierungen die URL für einen alternativen E-Mail-Konfigurationslink, der bei der ersten Anmeldung an _Admin_-Benutzer gesendet wird. Verwenden Sie in der E-Mail-Vorlage den `:tfat` Platzhalter , um anzugeben, wo das Token eingefügt werden soll. |
| [!UICONTROL Retry attempt limit for Two-Factor Authentication] | Global | Legt fest, wie oft ein Administrator eine [!DNL one-time password (OTP)] eingeben kann, bevor sein Konto vorübergehend deaktiviert wird. Standard: `10` |
| [!UICONTROL Two-Factor Authentication lockout time (seconds)] | Global | Bestimmt, wie lange (in Sekunden) ein Administrator warten kann, bis er eine [!DNL one-time password (OTP)] eingibt, bevor sein Konto vorübergehend deaktiviert wird. Standard: `300` |

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
| [!UICONTROL Client Id] | Global | Die Client-ID aus Ihrem [!DNL Duo Security]. |
| [!UICONTROL Client Secret] | Global | Das Client-Geheimnis aus Ihrem [!DNL Duo Security]. |
| [!UICONTROL Integration Key] | Global | Der Integrationsschlüssel aus Ihrem [!DNL Duo Security]-API-Konto. |
| [!UICONTROL Secret Key] | Global | Der geheime Schlüssel aus Ihrem [!DNL Duo Security]-API-Konto. |
| [!UICONTROL API Hostname] | Global | Der API-Hostname aus Ihrem [!DNL Duo Security]. |

{style="table-layout:auto"}

## [!UICONTROL Authy]

![Autorisierung](./assets/2fa-authy.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL API Key] | Global | Der API-Schlüssel aus Ihrem [!DNL Authy]. |
| [!UICONTROL OneTouch Message] | Global | Die Meldung, die bei der Anmeldung im [!DNL Authy]-Authentifikator angezeigt wird. Standard: `Login request to your Magento Admin` |

{style="table-layout:auto"}

## [!UICONTROL U2F Key]

![U2F-Schlüssel](./assets/2fa-u2f-key.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL WebApi Challenge Domain] | Global | Die Domain, die zum Ausstellen und Verarbeiten [!DNL WebAuthn] Herausforderungen für benutzerdefinierte Web-API-Implementierungen verwendet wird. |

{style="table-layout:auto"}
