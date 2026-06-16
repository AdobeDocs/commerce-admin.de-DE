---
title: '[!UICONTROL Services] > [!UICONTROL OAuth]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Services] > [!UICONTROL OAuth] des Commerce Admin.
exl-id: 984793e0-6ac9-443b-b234-e0cea717dada
feature: Configuration, Security
TQID: https://experienceleague.adobe.com/gwRxAaSnEul4D-LjjoGIcEiUCLl8ZrKjcSaMTvlGUKY
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 209
ht-degree: 2%

---

# [!UICONTROL Services] > [!UICONTROL OAuth]

{{config}}

## [!UICONTROL Access Token Expiration]

![Gültigkeit des Zugriffstokens](./assets/oauth-token-expire.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Customer Token Lifetime (hours]) | Global | Bestimmt den Zeitraum in Stunden, nach dem ein Kunden-API-Token abläuft. Das Kunden-Token läuft nie ab, wenn das Feld leer ist. Standardwert: `1` |
| [!UICONTROL Admin Token Lifetime (hours)] | Global | Bestimmt, wie lange ein Admin-API-Token in Stunden abläuft. Das Admin-Token läuft nie ab, wenn das Feld leer ist. Standardwert: `4` |

{style="table-layout:auto"}

>[!NOTE]
>
>Lebensdauer- und Verschlüsselungsalgorithmen der Bearer-Kunden- und Admin-API-Token werden von den Konfigurationseinstellungen [JWT-Authentifizierung](magento-web-api.md#jwt-authentication) gesteuert.

## [!UICONTROL Cleanup Settings]

![Bereinigungsparameter](./assets/oauth-cleanup.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Cleanup Probability] | Global | Gibt die Anzahl der OAuth-Anfragen an, bevor die Bereinigung gestartet wird. Geben Sie keine `0` ein, um die Bereinigung zu deaktivieren. |
| [!UICONTROL Enable WSDL Cache] | Global | Bestimmt das Alter der Einträge in Minuten, bevor sie bereinigt werden. |

{style="table-layout:auto"}

## [!UICONTROL Consumer Settings]

![Verbrauchereinstellungen](./assets/oauth-consumer-settings.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL OAuth consumer credentials HTTP Post timeout] | Global | Gibt an, wie lange das System nach einer Zeitüberschreitung braucht, wenn Kunden ihre Anmeldeinformationen veröffentlichen. |
| [!UICONTROL OAuth consumer credentials HTTP Post maxredirects] | Global | Gibt die maximale Anzahl von Weiterleitungen an, die mit einer Veröffentlichung von Verbraucheranmeldeinformationen verbunden sind. |
| [!UICONTROL Expiration Period] | Global | Bestimmt die Anzahl der Sekunden, bevor ein nicht verwendeter Schlüssel/Geheimnis abläuft, nachdem der OAuth-Token-Austausch begonnen hat. |

{style="table-layout:auto"}

## [!UICONTROL Authentication Locks]

![Authentifizierungssperren](./assets/oauth-locks.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Maximum Login Failures to Lock Out Account] | Global | Gibt die maximale Anzahl von Authentifizierungsfehlern für das Sperren eines Kontos an. |
| [!UICONTROL Lockout Time (seconds)] | Global | Gibt den Zeitraum in Sekunden an, nach dem das Konto entsperrt wird. |

{style="table-layout:auto"}
