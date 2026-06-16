---
title: '[!UICONTROL Services] > [!UICONTROL Magento Web API]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Services] > [!UICONTROL Magento Web API] des Commerce Admin.
exl-id: 9e9857e7-6f5c-4273-9e82-c861e627827a
feature: Configuration, Integration
TQID: https://experienceleague.adobe.com/62cy3cPVxGeI-W1LElSg1TEBEb0cZN30vGZQ74UNhm8
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 325
ht-degree: 1%

---

# [!UICONTROL Services] > [!UICONTROL Magento Web API]

{{config}}

<!-- [X-ref](../systems/integrations.md) -->

## [!UICONTROL SOAP Settings]

![SOAP-Einstellungen](./assets/web-api-soap-settings.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Default Response Charset] | Shop-Ansicht | Bestimmt den Standardzeichensatz. Wenn leer, wird UTF-8 verwendet. |

{style="table-layout:auto"}

## [!UICONTROL GraphQl Input Limits]

![GraphQL-Eingabebeschränkungen](./assets/web-api-graphql-input-limits.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable Input Limits] | Shop-Ansicht | Legt fest, ob Eingabebeschränkungen für GraphQL-Aufrufe aktiviert sind. Standardwert: `No`. |
| [!UICONTROL Maximum Page Size] | Shop-Ansicht | Legt die maximale Anzahl von Elementen fest, die in einem paginierten Suchergebnis in der GraphQL-Antwort zulässig ist. Diese Option ist nicht verfügbar, wenn _Eingabegrenzwerte aktivieren_ = `No`. |

{style="table-layout:auto"}

## [!UICONTROL Web Api Input Limits]

![Beschränkungen für Web-API-Eingaben](./assets/web-api-input-limits.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable Input Limits] | Shop-Ansicht | Bestimmt, ob Eingabebeschränkungen für Web-API-Aufrufe aktiviert sind. Standardwert: `No`. |
| Maximale Anzahl von Eingabelisten | Shop-Ansicht | Legt die maximale Anzahl von Elementen fest, die in einer Entitäts-Array-Eigenschaft in der Web-API-Anfrage zulässig ist. Diese Option ist nicht verfügbar, wenn _Eingabegrenzwerte aktivieren_ = `No`. |
| [!UICONTROL Maximum Page Size] | Shop-Ansicht | Legt die maximale Anzahl von Elementen fest, die in einem paginierten Suchergebnis in der Web-API-Antwort zulässig ist. Diese Option ist nicht verfügbar, wenn _Eingabegrenzwerte aktivieren_ = `No`. |
| [!UICONTROL Default Page Size] | Shop-Ansicht | Legt die Standardanzahl von Elementen in einem paginierten Suchergebnis in der Web-API-Antwort fest. |

{style="table-layout:auto"}

## [!UICONTROL Web API Security]

![Web-API-Sicherheit](./assets/web-api-security.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Allow Anonymous Guest Access] | Global | Legt fest, ob Gäste anonym auf CMS zugreifen, Ressourcen aus SOAP und REST-APIs katalogisieren und speichern können. Standardmäßig ist der anonyme Gastzugriff nicht zulässig. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL JWT Authentication]

![JWT-Authentifizierung](./assets/web-api-jwt-authentication.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Algorithm to sign/encrypt JWTs used for authentication] | Global | Gibt den Typ des JWS- oder JWE-Algorithmus an, der für die JWT-Verschlüsselung (JSON Web Token) verwendet wird |
| [!UICONTROL Content encryption algorithm for JWEs] | Global | Gibt den Typ des Inhaltsverschlüsselungsalgorithmus an, der für die JWT-Verschlüsselung verwendet wird, wenn der JWT-Algorithmus ausgewählt ist. Diese Option wird bei JWS-Algorithmen ignoriert. |
| [!UICONTROL Customer JWT Expires In] | Global | Legt die Dauer (in Minuten) fest, nach der ein Kunden-JWT-Bearer-Token abläuft. Das Kunden-JWT-Bearer-Token läuft in 30 Minuten ab, wenn dieses Feld leer ist oder einen negativen Wert hat. Standardwert: `60` |
| [!UICONTROL Admin User JWT Expires In] | Global | Legt die Zeit (in Minuten) fest, nach der das Admin-JWT-Bearer-Token abläuft. Das Admin-JWT-Bearer-Token läuft in 30 Minuten ab, wenn dieses Feld leer ist oder einen negativen Wert aufweist. Standardwert: `60` |

{style="table-layout:auto"}
