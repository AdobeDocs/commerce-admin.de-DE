---
title: Zuweisen eines Unternehmensadministrators
description: Erfahren Sie, wie Sie ein Firmenbenutzerkonto als designierten Unternehmensadministrator für das Firmenkonto zuweisen.
exl-id: 26f3a449-6f3a-4078-816d-6248ac6d1e46
feature: B2B, Companies
role: Admin, User
TQID: https://experienceleague.adobe.com/5h4DaxiUVTz9UFOC3BZqd5ESPRLaLgvstCODPEEgCEk
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffa
subfeature_v2: id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 274
ht-degree: 0%

---

# Zuweisen eines Unternehmensadministrators

Der Unternehmensadministrator wird beim ersten Erstellen des Unternehmenskontos zugewiesen und kann nur von einem Store-Administrator über den Administrator geändert werden.

- Jeder Firma kann nur ein Administrator zugewiesen sein.
- Ein Firmenbenutzer kann nur für ein Unternehmen der Administrator sein.
- Änderungen am zugewiesenen Unternehmensadministrator müssen von einem Store-Administrator vom Administrator vorgenommen werden.

## Zugewiesenen Unternehmensadministrator ändern

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![Firmen](./assets/companies-grid.png){width="700" zoomable="yes"}

1. Suchen Sie das Unternehmen in der Liste und klicken Sie dann auf **[!UICONTROL Edit]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Company Admin]** .

   ![Unternehmensadministrator](./assets/company-create-company-admin.png){width="700" zoomable="yes"}

1. Geben Sie die **[!UICONTROL Job Title]** des neuen Unternehmensadministrators ein.

   Durch diese Aktion wird das Formular gelöscht und die erforderlichen _[!UICONTROL First Name]_und_[!UICONTROL Last Name]_ Felder sind hervorgehoben.

1. Geben Sie die **[!UICONTROL Email]** des neuen Unternehmensadministrators ein.

   Wenn das System die E-Mail-Adresse nicht in der Datenbank findet, werden Sie aufgefordert, zu bestätigen, dass Sie den Unternehmensadministrator ersetzen möchten.

   - Wenn für den neuen Unternehmensadministrator kein Benutzerkonto vorhanden ist, erstellt das System ein Konto vom Typ `Company Admin`.

   - Wenn das Benutzerkonto im System vorhanden ist, wird es an die Position des Unternehmensadministrators in der Unternehmensstruktur verschoben.

1. Geben Sie die **[!UICONTROL First Name]** und **[!UICONTROL Last Name]** sowie alle weiteren Informationen ein, die für den neuen Unternehmensadministrator gelten.

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.

   Das individuelle Konto des früheren Unternehmensadministrators verbleibt als aktives Benutzerkonto, das der Standardbenutzerrolle zugewiesen ist, im System. Wenn dies die einzige Firma ist, die mit dem Benutzerkonto verknüpft ist, ändert sich der Kontotyp von *[!UICONTROL Company user]* in *[!UICONTROL Individual user]*.

   Das System sendet eine E-Mail-Benachrichtigung über die Änderung an die neuen und früheren Unternehmensadministratoren.

