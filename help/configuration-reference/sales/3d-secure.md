---
title: '[!UICONTROL Sales] &gt; [!UICONTROL 3D Secure]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der [!UICONTROL Sales] &gt; [!UICONTROL 3D Secure] Seite des Commerce-Administrators.
exl-id: 38eb3ee6-8b80-4ba3-afce-8ab82baa76a9
feature: Configuration, Security, Payments
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL 3D Secure]

[!DNL 3-D Secure] wurde von [!DNL Visa] Förderung sicherer Online-Transaktionen. Beispiele für [!DNL 3-D Secure] von Kartennetzwerken erstellte Lösungen durch [!DNL Visa], [!DNL Mastercard SecureCode], [!DNL American Express SafeKey], und [!DNL CardinalCommerce Consumer Authentication]. [!DNL CardinalCommerce] ist ein weltweit führendes Unternehmen im Bereich der digitalen Transaktionsauthentifizierung und eine hundertprozentige Tochtergesellschaft von [!DNL Visa].

[!DNL 3-D Secure] Version 2.0 unterstützt zahlreiche Verbesserungen, einschließlich erweiterter Authentifizierungsmethoden und Authentifizierungsfluss sowie verbesserter Datenfreigabe zwischen Händlern und Ausstellern.

>[!NOTE]
>
>Die [Braintree](../../stores-purchase/braintree.md) auch das Payment Gateway unterstützt [!DNL 3-D Secure] Verifizierung.

{{config}}

## [!UICONTROL CardinalCommerce]

![CardinalCommerce](./assets/3d-secure-cardinalcommerce.png)<!-- zoom -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Environment] | Webseite | Gibt den Betriebsmodus Ihrer [!DNL CardinalCommerce] -Konto. Wenn Sie in einer Testumgebung ausgeführt werden, wählen Sie &quot;Sandbox&quot;. Optionen: Sandbox/Produktion (Standard) |
| [!UICONTROL Org Unit ID] | Webseite | Die Organisationseinheiten-ID von Ihrer [!DNL CardinalCommerce] Handelskonto. |
| [!UICONTROL API Key] | Webseite | Der API-Schlüssel aus Ihrem [!DNL CardinalCommerce] Handelskonto. |
| [!UICONTROL API Identifier] | Webseite | Die API-Kennung aus Ihrem [!DNL CardinalCommerce] Handelskonto. |
| [!UICONTROL Debug] | Webseite | Optionen: `Yes` / `No` |

{style="table-layout:auto"}
