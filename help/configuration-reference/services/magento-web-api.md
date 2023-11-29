---
title: '[!UICONTROL Services] &gt; [!UICONTROL Magento Web API]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der [!UICONTROL Services] &gt; [!UICONTROL Magento Web API] Seite des Commerce-Administrators.
exl-id: 9e9857e7-6f5c-4273-9e82-c861e627827a
feature: Configuration, Integration
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 1%

---

# [!UICONTROL Services] > [!UICONTROL Magento Web API]

{{config}}

<!-- [X-ref](../systems/integrations.md) -->

## [!UICONTROL SOAP Settings]

![SOAP-Einstellungen](./assets/web-api-soap-settings.png)<!-- zoom -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Default Response Charset] | Store-Ansicht | Legt den Standardzeichensatz fest. Wenn leer, wird UTF-8 verwendet. |

{style="table-layout:auto"}

## [!UICONTROL GraphQl Input Limits]

![GraphQl-Eingabegrenzen](./assets/web-api-graphql-input-limits.png)<!-- zoom -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable Input Limits] | Store-Ansicht | Bestimmt, ob Eingabegrenzen für GraphQL-Aufrufe aktiviert sind. Standardwert: `No`. |
| [!UICONTROL Maximum Page Size] | Store-Ansicht | Legt die maximal zulässige Anzahl von Elementen in einem paginierten Suchergebnis in der GraphQL-Antwort fest. Diese Option ist nicht verfügbar, wenn _Eingabegrenzen aktivieren_ = `No`. |

{style="table-layout:auto"}

## [!UICONTROL Web Api Input Limits]

![Eingabegrenzen für Web-API](./assets/web-api-input-limits.png)<!-- zoom -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable Input Limits] | Store-Ansicht | Bestimmt, ob Eingabegrenzen für Web-API-Aufrufe aktiviert sind. Standardwert: `No`. |
| Begrenzung der Eingabeliste | Store-Ansicht | Legt die maximale Anzahl von Elementen fest, die in einer Entitäts-Array-Eigenschaft in der Web-API-Anfrage zulässig sind. Diese Option ist nicht verfügbar, wenn _Eingabegrenzen aktivieren_ = `No`. |
| [!UICONTROL Maximum Page Size] | Store-Ansicht | Legt die maximal zulässige Anzahl von Elementen in einem paginierten Suchergebnis in der Web-API-Antwort fest. Diese Option ist nicht verfügbar, wenn _Eingabegrenzen aktivieren_ = `No`. |
| [!UICONTROL Default Page Size] | Store-Ansicht | Legt die Standardanzahl von Elementen in einem paginierten Suchergebnis in der Web-API-Antwort fest. |

{style="table-layout:auto"}

## [!UICONTROL Web API Security]

![Web-API-Sicherheit](./assets/web-api-security.png)<!-- zoom -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Allow Anonymous Guest Access] | Global | Bestimmt, ob Gäste anonym auf CMS zugreifen, Ressourcen katalogisieren und speichern können, sowohl aus SOAP- als auch aus REST-APIs. Standardmäßig ist der anonyme Gastzugriff nicht erlaubt. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL JWT Authentication]

![JWT-Authentifizierung](./assets/web-api-jwt-authentication.png)<!-- zoom -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Algorithm to sign/encrypt JWTs used for authentication] | Global | Gibt den Typ des JWS- oder JWE-Algorithmus an, der für die JWT-Verschlüsselung (JSON Web Token) verwendet wird |
| [!UICONTROL Content encryption algorithm for JWEs] | Global | Gibt den Typ des Inhaltsverschlüsselungsalgorithmus an, der für die JWT-Verschlüsselung verwendet wird, wenn der JWE-Algorithmus ausgewählt ist. Diese Option wird bei JWS-Algorithmen ignoriert. |
| [!UICONTROL Customer JWT Expires In] | Global | Legt die Dauer (in Minuten) fest, bevor ein JWT-Bearer-Token des Kunden abläuft. Das JWT-Bearer-Token des Kunden läuft nach 30 Minuten ab, wenn dieses Feld leer ist oder einen negativen Wert aufweist. Standardwert: `60` |
| [!UICONTROL Admin User JWT Expires In] | Global | Legt die Dauer (in Minuten) fest, bevor das Admin-JWT-Trägertoken abläuft. Das Admin-JWT-Trägertoken läuft nach 30 Minuten ab, wenn dieses Feld leer ist oder einen negativen Wert aufweist. Standardwert: `60` |

{style="table-layout:auto"}
