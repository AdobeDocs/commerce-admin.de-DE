---
title: Zuweisen eines Unternehmensadministrators
description: Erfahren Sie, wie Sie ein Unternehmensbenutzerkonto als festgelegten Unternehmensadministrator für das Unternehmenskonto zuweisen.
exl-id: 26f3a449-6f3a-4078-816d-6248ac6d1e46
feature: B2B, Companies
role: Admin, User
source-git-commit: 99285b700b91e0072340a2231c39a8050818fd17
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 0%

---

# Zuweisen eines Unternehmensadministrators

Der Unternehmensadministrator wird beim ersten Erstellen des Unternehmenskontos zunächst zugewiesen und kann nur von einem Store-Administrator des Administrators geändert werden.

- Jedem Unternehmen kann nur ein Administrator zugewiesen sein.
- Ein Unternehmensbenutzer kann der Administrator für nur ein Unternehmen sein.
- Änderungen am zugewiesenen Unternehmensadministrator müssen von einem Store-Administrator des Administrators vorgenommen werden.

## Zugewiesener Unternehmensadministrator

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![Unternehmen](./assets/companies-grid.png){width="700" zoomable="yes"}

1. Suchen Sie das Unternehmen in der Liste und klicken Sie dann auf **[!UICONTROL Edit]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Company Admin]** .

   ![Unternehmensadministrator](./assets/company-create-company-admin.png){width="700" zoomable="yes"}

1. Geben Sie den Wert **[!UICONTROL Job Title]** des neuen Unternehmensadministrators ein.

   Durch diese Aktion wird das Formular gelöscht und die erforderlichen Felder _[!UICONTROL First Name]_und_[!UICONTROL Last Name]_ werden hervorgehoben.

1. Geben Sie die **[!UICONTROL Email]** -Adresse des neuen Unternehmensadministrators ein.

   Wenn das System die E-Mail-Adresse nicht in der Datenbank findet, werden Sie aufgefordert zu bestätigen, dass Sie den Unternehmensadministrator ersetzen möchten.

   - Wenn für den neuen Unternehmensadministrator kein Benutzerkonto vorhanden ist, erstellt das System ein Konto vom Typ `Company Admin`.

   - Wenn das Benutzerkonto im System vorhanden ist, wird es an die Stelle des Unternehmensadministrators in der Unternehmensstruktur verschoben.

1. Geben Sie die Werte **[!UICONTROL First Name]** und **[!UICONTROL Last Name]** sowie alle anderen Informationen ein, die für den neuen Unternehmensadministrator gelten.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]**.

   Das individuelle Konto des ehemaligen Unternehmensadministrators verbleibt im System als aktives Benutzerkonto, das der Standardbenutzerrolle zugewiesen ist. Wenn dies das einzige mit dem Benutzerkonto verknüpfte Unternehmen ist, ändert sich der Kontotyp von *[!UICONTROL Company user]* in *[!UICONTROL Individual user]*.

   Das System sendet eine E-Mail-Benachrichtigung über die Änderung an die neuen und ehemaligen Unternehmensadministratoren.

