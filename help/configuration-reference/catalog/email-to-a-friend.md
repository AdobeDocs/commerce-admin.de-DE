---
title: '[!UICONTROL Catalog] > [!UICONTROL Email to a Friend]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Catalog] > [!UICONTROL Email to a Friend] des Commerce Admin.
exl-id: cd1e3a8d-14ce-47e9-a3bc-c1b1dcbe0d8c
feature: Configuration, Communications
TQID: https://experienceleague.adobe.com/TzkDDALdwE5MMIEuZBpBL4DnOgngN93-YEf4biNwYMI
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
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 172
ht-degree: 1%

---

# [!UICONTROL Catalog] > [!UICONTROL Email to a Friend]

{{config}}

## [!UICONTROL Email Templates]

![E-Mail-Vorlagen](./assets/email-to-a-friend-email-templates.png)<!-- zoom -->

<!-- [Email Templates](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/communications/email-templates#configure-email-templates) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enabled] | Shop-Ansicht | Aktiviert den Prozess, der Kunden die Möglichkeit gibt, E-Mails über Produkte in Ihrem Geschäft an Freunde zu senden. Optionen: `Yes` / `No` |
| [!UICONTROL Select Email Template] | Shop-Ansicht | Gibt die E-Mail-Vorlage an, die für Nachrichten verwendet wird, die von der Funktion _E-Mail an einen Freund_ generiert werden. Standardvorlage: `Send Product to Friend` |
| [!UICONTROL Allow for Guests] | Shop-Ansicht | Bestimmt, ob der Absender ein registrierter Kunde sein muss, um E-Mails zu einem Produkt an Freunde zu senden. Optionen: `Yes` / `No` |
| [!UICONTROL Max Recipients] | Shop-Ansicht | Beschränkt die Anzahl der Personen, die sich für eine einzelne E-Mail auf der Verteilerliste befinden können. |
| [!UICONTROL Max Products Sent in 1  Hour] | Shop-Ansicht | Beschränkt die Anzahl der Produkte, die von einem einzelnen Benutzer über einen Zeitraum von einer Stunde geteilt werden können. |
| [!UICONTROL Limit Sending By] | Shop-Ansicht | Bestimmt die Methode zur Identifizierung des Absenders. Zu den Optionen gehören: <br/>**`IP Address`**- (Empfohlen) Identifiziert den Absender anhand der IP-Adresse des Computers, der zum Senden der Produkt-E-Mails verwendet wird.<br/>**`Cookie (unsafe)`** - Identifiziert den Absender anhand eines Browser-Cookies. Diese Methode ist nicht sicher, da der Benutzer das Cookie löschen kann, um die Einschränkung zu vermeiden. |

{style="table-layout:auto"}
