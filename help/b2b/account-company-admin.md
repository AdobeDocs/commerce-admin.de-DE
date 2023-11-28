---
title: Zuweisen eines Unternehmensadministrators
description: Erfahren Sie, wie Sie ein Unternehmensbenutzerkonto als festgelegten Unternehmensadministrator für das Unternehmenskonto zuweisen.
exl-id: 26f3a449-6f3a-4078-816d-6248ac6d1e46
feature: B2B, Companies
role: Admin, User
source-git-commit: fb075822e318073053cdf8cdd5cd9bb3a6343904
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# Zuweisen eines Unternehmensadministrators

Der Unternehmensadministrator wird beim ersten Erstellen des Unternehmenskontos zunächst zugewiesen und kann nur von einem Store-Administrator des Administrators geändert werden.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Suchen Sie das Unternehmen in der Liste und klicken Sie auf **[!UICONTROL Edit]**.

   ![Unternehmen](./assets/companies-grid.png){width="700" zoomable="yes"}

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Company Admin]** Abschnitt.

   ![Unternehmensadministrator](./assets/company-create-company-admin.png){width="700" zoomable="yes"}

1. Geben Sie die **[!UICONTROL Job Title]** des neuen Unternehmensadministrators und klicken Sie auf **[!UICONTROL Proceed]** , um fortzufahren.

   Durch diese Aktion werden das Formular und die erforderlichen _[!UICONTROL First Name]_und_[!UICONTROL Last Name]_ -Felder hervorgehoben werden.

1. Geben Sie die **[!UICONTROL Email]** Adresse des neuen Unternehmensadministrators.

   Wenn das System die E-Mail-Adresse nicht in der Datenbank findet, werden Sie aufgefordert zu bestätigen, dass Sie den Unternehmensadministrator ersetzen möchten.

   - Wenn für den neuen Unternehmensadministrator kein Benutzerkonto vorhanden ist, erstellt das System ein Konto der `Company Admin` Typ.

   - Wenn das Benutzerkonto im System vorhanden ist, wird es an die Stelle des Unternehmensadministrators in der Unternehmensstruktur verschoben.

1. Geben Sie die **[!UICONTROL First Name]** und **[!UICONTROL Last Name]** sowie alle anderen für den neuen Unternehmensadministrator relevanten Informationen.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]**.

   Das individuelle Konto des ehemaligen Unternehmensadministrators verbleibt im System als aktives individuelles Benutzerkonto in der Unternehmensstruktur, das der Standardbenutzerrolle zugewiesen ist.

   Das System sendet eine E-Mail-Benachrichtigung über die Änderung an die neuen und ehemaligen Unternehmensadministratoren.
