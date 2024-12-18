---
title: '[!UICONTROL Catalog] &gt; [!UICONTROL Email to a Friend]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Catalog] &gt; [!UICONTROL Email to a Friend] des Commerce Admin-Bereichs.
exl-id: cd1e3a8d-14ce-47e9-a3bc-c1b1dcbe0d8c
feature: Configuration, Communications
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

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
