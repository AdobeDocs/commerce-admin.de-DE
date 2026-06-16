---
title: '[!UICONTROL Customers] > [!UICONTROL Invitations]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Customers] > [!UICONTROL Invitations] des Commerce Admin.
exl-id: edafeaed-9c4f-4d9f-b35c-381ae5f43b67
feature: Configuration, Promotions/Events
TQID: https://experienceleague.adobe.com/UOJF8r7CsXWK6qG7FjkJoJTIqnH2fPQhnRyZrJ7u4nE
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 250
ht-degree: 1%

---

# [!UICONTROL Customers] > [!UICONTROL Invitations]

{{ee-feature}}

{{config}}

## [!UICONTROL General]

![Allgemein](./assets/invitations-general.png)<!-- zoom -->

<!-- [General](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/events/invitations#enable-invitations-for-your-store) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable Invitations Functionality] | Global | Legt fest, ob das Einladungsmodul aktiviert ist. Optionen: `Yes` / `No` |
| [!UICONTROL Enable Invitations on Frontend] | Website | Legt fest, ob Einladungen von der Storefront aus verwaltet werden können. Optionen: `Yes` / `No` |
| [!UICONTROL Referred Customer Group] | Shop-Ansicht | Bestimmt die Kundengruppe des Einladenden. Optionen: <br/>**`Same as Inviter`**- Einladende werden automatisch derselben Kundengruppe zugewiesen wie die Kunden, die sie eingeladen haben.<br/>**`Default Customer Group from Configuration`** - Einladende haben automatisch die Standardeinstellung [Kundengruppe](../../customers/customer-groups.md). |
| [!UICONTROL New Accounts Registration] | Shop-Ansicht | Legt fest, wie Einladende ein Konto erstellen können. Optionen: <br/>**`By Invitation Only`**- Einladende müssen dem Link in der Einladungs-E-Mail folgen, um ein Konto zu erstellen.<br/>**`Available to All`** - Einladende können das Formular zur Kontoregistrierung verwenden, das im Store verfügbar ist. |
| [!UICONTROL Allow Customers to Add Custom Message to Invitation Email] | Shop-Ansicht | Bestimmt, ob im Einladungsformular ein Feld vorhanden ist, in dem der Einladende eine benutzerdefinierte Nachricht hinzufügen kann, die per E-Mail an den Einladenden gesendet wird. Dies wirkt sich nicht auf die Fähigkeit des Administrators aus, eine Nachricht zu einer Einladung hinzuzufügen. Optionen: `Yes` / `No`. |
| [!UICONTROL Max Invitations Allowed to be Sent at One Time] | Shop-Ansicht | Bestimmt die maximale Anzahl von Einladungen, die der Einladende gleichzeitig senden kann. An jede E-Mail-Adresse, die der Einladende in das Formular einfügt, wird eine andere Einladung gesendet. Dadurch werden Server-Ressourcen geschützt, da eine große Anzahl von Einladungen nicht gleichzeitig versendet wird, und die Wahrscheinlichkeit, dass Einladungen als Spam versendet werden, sinkt. |

{style="table-layout:auto"}

## [!UICONTROL Email]

![E-Mail](./assets/invitations-email.png)<!-- zoom -->

<!-- [Email](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/events/invitations#enable-invitations-for-your-store) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Customer Invitation Email Sender] | Shop-Ansicht | Bestimmt den Absender der E-Mail, die Einladungen erhalten, wenn eine Einladungs-E-Mail gesendet wird. Standardwert: `General Contact` |
| [!UICONTROL Customer Invitation Email Template] | Shop-Ansicht | Bestimmt die Vorlage der E-Mail, die Einladungen beim Senden einer Einladungs-E-Mail erhalten. Standardvorlage: `Customer Invitation` |

{style="table-layout:auto"}
