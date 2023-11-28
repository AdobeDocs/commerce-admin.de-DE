---
title: Unternehmenskonto genehmigen
description: Erfahren Sie, wie Sie in Admin Unternehmenskontoanforderungen genehmigen.
exl-id: c7123383-0e94-4d6c-be3c-b6ca84145a59
feature: B2B, Companies, Configuration
role: Admin, User
source-git-commit: 2b86fe55f980c22839de10ecc4c9023034eb9ea1
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---

# Unternehmenskonto genehmigen

Der Status von Anforderungen, die von der Storefront zum Erstellen eines Unternehmens empfangen wurden, lautet `Pending Approval` bis die Anfrage vom Store-Administrator überprüft und entweder genehmigt oder abgelehnt wird. Der Status eines Unternehmenskontos kann auf einen der folgenden Werte festgelegt werden:

- [!UICONTROL Active]
- [!UICONTROL Pending Approval]
- [!UICONTROL Rejected]
- [!UICONTROL Blocked]

Sie können auch die [Aktionssteuerung](account-company-manage.md) um mehrere Unternehmensanfragen zu genehmigen.

![Ausstehende Genehmigung](./assets/companies-pending-approval.png){width="700" zoomable="yes"}

## Genehmigen eines ausstehenden Unternehmenskontos

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   Sie können die _[!UICONTROL Columns]_Auswahl über dem Raster zum Anzeigen der **[!UICONTROL Status]**Spalte.

1. Im _[!UICONTROL Action]_Spalte, klicken **[!UICONTROL Edit]**.

1. Satz **[!UICONTROL Company Status]** nach `Active`.

   ![Festlegen des Unternehmensstatus](./assets/company-status-active.png){width="700" zoomable="yes"}

1. Klicken Sie bei Aufforderung zur Bestätigung auf **[!UICONTROL Change status]**.

   Der Unternehmensadministrator erhält eine E-Mail-Benachrichtigung, dass das Unternehmen jetzt aktiv ist.

1. Falls zutreffend, legen Sie **[!UICONTROL Sales Representative]** zu einem bestimmten Admin-Benutzerkonto hinzugefügt.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png)  die **[!UICONTROL Account Information]** und verwenden Sie **[!UICONTROL Comment]** -Feld, um Hinweise zum Konto einzugeben.

   Die Kommentare sind in der Storefront nicht sichtbar.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]**.

   Dem Unternehmens- und Unternehmensadministrator wird eine Bestätigungs-E-Mail gesendet, in der bestätigt wird, dass das Unternehmenskonto genehmigt wurde.

## Unternehmensstatus

| Status | Beschreibung |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Active] | Das Unternehmen wurde genehmigt und kann vom Unternehmensadministrator aus dem Schaufenster verwaltet werden. |
| [!UICONTROL Pending Approval] | Eine Anfrage zur Erstellung eines Unternehmenskontos wurde von der Storefront gesendet, wird jedoch noch nicht geprüft. |
| [!UICONTROL Rejected] | Die Anforderung, ein Unternehmenskonto zu erstellen, wurde vom Store-Administrator abgelehnt. |
| [!UICONTROL Blocked] | Das Unternehmenskonto hat keinen guten Ruf mehr. Der Kunde kann über die Storefront auf das Konto zugreifen, aber keine Käufe tätigen. |

{style="table-layout:auto"}
