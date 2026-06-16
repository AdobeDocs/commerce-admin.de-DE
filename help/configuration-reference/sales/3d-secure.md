---
title: '[!UICONTROL Sales] > [!UICONTROL 3D Secure]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Sales] > [!UICONTROL 3D Secure] des Commerce Admin.
exl-id: 38eb3ee6-8b80-4ba3-afce-8ab82baa76a9
feature: Configuration, Security, Payments
TQID: https://experienceleague.adobe.com/WzxM9ZYbobbC1fWSIph0jv89uXLte6Wzjs5be27eMyU
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 126
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL 3D Secure]

[!DNL 3-D Secure] wurde von [!DNL Visa] entwickelt, um sichere Online-Transaktionen zu fördern. Beispiele für [!DNL 3-D Secure] von Kartennetzwerken erstellten Lösungen werden von [!DNL Visa], [!DNL Mastercard SecureCode], [!DNL American Express SafeKey] und [!DNL CardinalCommerce Consumer Authentication] verifiziert. [!DNL CardinalCommerce] ist ein weltweit führender Anbieter von Authentifizierung digitaler Transaktionen und eine hundertprozentige Tochtergesellschaft von [!DNL Visa].

[!DNL 3-D Secure] Version 2.0 unterstützt zahlreiche Verbesserungen, einschließlich erweiterter Authentifizierungsmethoden und des Authentifizierungsflusses sowie verbesserter Datenfreigabe zwischen Händler und Aussteller.

>[!NOTE]
>
>Das Zahlungs-Gateway [Braintree](../../stores-purchase/braintree.md) unterstützt auch die [!DNL 3-D Secure].

{{config}}

## [!UICONTROL CardinalCommerce]

![CardinalCommerce](./assets/3d-secure-cardinalcommerce.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Environment] | Website | Gibt den Betriebsmodus Ihres [!DNL CardinalCommerce] Kontos an. Wenn Sie in einer Testumgebung ausführen, wählen Sie „Sandbox“ aus. Optionen: Sandbox / Produktion (Standard) |
| [!UICONTROL Org Unit ID] | Website | Die Organisationseinheitenkennung Ihres [!DNL CardinalCommerce] Händlerkontos. |
| [!UICONTROL API Key] | Website | Der API-Schlüssel aus Ihrem [!DNL CardinalCommerce] Händlerkonto. |
| [!UICONTROL API Identifier] | Website | Die API-Kennung aus Ihrem [!DNL CardinalCommerce]-Händlerkonto. |
| [!UICONTROL Debug] | Website | Optionen: `Yes` / `No` |

{style="table-layout:auto"}
