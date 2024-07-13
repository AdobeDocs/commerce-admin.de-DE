---
title: '[!UICONTROL Sales] &gt; [!UICONTROL 3D Secure]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Sales] &gt; [!UICONTROL 3D Secure] des Commerce-Administrators.
exl-id: 38eb3ee6-8b80-4ba3-afce-8ab82baa76a9
feature: Configuration, Security, Payments
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL 3D Secure]

[!DNL 3-D Secure] wurde von [!DNL Visa] entwickelt, um sichere Online-Transaktionen zu fördern. Beispiele für von Kartennetzwerken erstellte [!DNL 3-D Secure] -Lösungen werden durch [!DNL Visa], [!DNL Mastercard SecureCode], [!DNL American Express SafeKey] und [!DNL CardinalCommerce Consumer Authentication] überprüft. [!DNL CardinalCommerce] ist ein weltweit führendes Unternehmen im Bereich der Authentifizierung digitaler Transaktionen und eine hundertprozentige Tochtergesellschaft von [!DNL Visa].

[!DNL 3-D Secure] Version 2.0 unterstützt zahlreiche Verbesserungen, darunter erweiterte Authentifizierungsmethoden und Authentifizierungsfluss sowie verbesserte Datenfreigabe zwischen Händler und Emittent.

>[!NOTE]
>
>Das Zahlungs-Gateway [Braintree](../../stores-purchase/braintree.md) unterstützt auch die Überprüfung von [!DNL 3-D Secure].

{{config}}

## [!UICONTROL CardinalCommerce]

![KardinalCommerce](./assets/3d-secure-cardinalcommerce.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Environment] | Webseite | Gibt den Betriebsmodus Ihres [!DNL CardinalCommerce]-Kontos an. Wenn Sie in einer Testumgebung ausgeführt werden, wählen Sie &quot;Sandbox&quot;. Optionen: Sandbox/Produktion (Standard) |
| [!UICONTROL Org Unit ID] | Webseite | Die Organisationseinheiten-ID aus Ihrem [!DNL CardinalCommerce] -Handelskonto. |
| [!UICONTROL API Key] | Webseite | Der API-Schlüssel aus Ihrem [!DNL CardinalCommerce] -Handelskonto. |
| [!UICONTROL API Identifier] | Webseite | Die API-ID aus Ihrem [!DNL CardinalCommerce] -Handelskonto. |
| [!UICONTROL Debug] | Webseite | Optionen: `Yes` / `No` |

{style="table-layout:auto"}
