---
title: Genehmigen eines Unternehmenskontos
description: Erfahren Sie, wie Sie Anfragen für Unternehmenskonten in der Admin-Liste genehmigen.
exl-id: c7123383-0e94-4d6c-be3c-b6ca84145a59
feature: B2B, Companies, Configuration
role: Admin, User
TQID: https://experienceleague.adobe.com/ZpDdYMYaSnG1lOwV22mmrkYjBvf90pUJVZxP2r526pw
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 246
ht-degree: 0%

---

# Genehmigen eines Unternehmenskontos

Der Status der Anfragen, die von der Storefront empfangen werden, um ein Unternehmen zu erstellen, wird `Pending Approval`, bis die Anfrage vom Store-Administrator geprüft und entweder genehmigt oder abgelehnt wird. Der Status eines Unternehmenskontos kann auf einen der folgenden Werte festgelegt werden:

- [!UICONTROL Active]
- [!UICONTROL Pending Approval]
- [!UICONTROL Rejected]
- [!UICONTROL Blocked]

Sie können auch die [Aktionssteuerung“ verwenden](account-company-manage.md) um mehrere Unternehmensanfragen zu genehmigen.

![Vorbehaltlich der Genehmigung](./assets/companies-pending-approval.png){width="700" zoomable="yes"}

## Ausstehendes Firmenkonto genehmigen

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   Sie können den _[!UICONTROL Columns]_-Selektor über dem Raster verwenden, um die Spalte **[!UICONTROL Status]**&#x200B;anzuzeigen.

1. Klicken Sie in der Spalte _[!UICONTROL Action]_&#x200B;auf **[!UICONTROL Edit]**.

1. Legen Sie **[!UICONTROL Company Status]** auf `Active` fest.

   ![Legen Sie den Unternehmensstatus fest](./assets/company-status-active.png){width="700" zoomable="yes"}

1. Wenn Sie zum Bestätigen aufgefordert werden, klicken Sie auf **[!UICONTROL Change status]**.

   Der Unternehmensadministrator erhält eine E-Mail-Benachrichtigung, dass die Firma jetzt aktiv ist.

1. Legen Sie gegebenenfalls **[!UICONTROL Sales Representative]** auf ein bestimmtes Admin-Benutzerkonto fest.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Account Information]** und geben Sie im Feld **[!UICONTROL Comment]** Anmerkungen zum Konto ein.

   Die Kommentare sind in der Storefront nicht sichtbar.

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.

   Der Firma und dem Unternehmensadministrator wird eine Bestätigungs-E-Mail gesendet, mit der bestätigt wird, dass das Unternehmenskonto genehmigt wurde.

## Unternehmensstatus

| Status | Beschreibung |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Active] | Das Unternehmen ist genehmigt und kann vom Unternehmensadministrator in der Storefront verwaltet werden. |
| [!UICONTROL Pending Approval] | Eine Anfrage zur Erstellung eines Unternehmenskontos wurde von der Storefront eingereicht, wird jedoch noch nicht geprüft. |
| [!UICONTROL Rejected] | Die Anforderung zum Erstellen eines Unternehmenskontos wurde vom Store-Administrator abgelehnt. |
| [!UICONTROL Blocked] | Das Firmenkonto ist nicht mehr in gutem Zustand. Der Kunde kann von der Storefront aus auf das Konto zugreifen, jedoch keine Käufe tätigen. |

{style="table-layout:auto"}
