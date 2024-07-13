---
title: Struktur des Unternehmenskontos
description: Erfahren Sie mehr über Unternehmensstrukturen und wie ein Unternehmensadministrator sie definieren kann, um ihre geschäftsbezogenen Workflows und Richtlinien zu unterstützen.
exl-id: 4724b208-b6ac-4de5-9a4c-bc4d68402506
feature: B2B, Companies
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 0%

---

# Struktur des Unternehmenskontos

Es kann ein Unternehmenskonto eingerichtet werden, das die Struktur des Unternehmens widerspiegelt. Zunächst umfasst die Unternehmensstruktur nur den Unternehmensadministrator, kann jedoch erweitert werden, um Teams von Benutzern aufzunehmen. Die Benutzer können Teams zugeordnet oder innerhalb einer Hierarchie von Abteilungen und Unterteilungen innerhalb des Unternehmens organisiert werden.

![Unternehmensstruktur mit Divisionen](./assets/company-structure-diagram.svg){width="500"}

Im Konto-Dashboard des Unternehmensadministrators wird die Unternehmensstruktur als Struktur dargestellt und besteht zunächst nur aus dem Unternehmensadministrator.

![Unternehmensstruktur mit Unternehmensadministrator](./assets/company-structure-tree-admin.png){width="600" zoomable="yes"}

Wenn das Konto erstellt und genehmigt wird, kann der Unternehmensadministrator die E-Mail-Adresse des Unternehmens verwenden oder eine andere E-Mail-Adresse erhalten.

Es ist möglich, dass die Person, die als Unternehmensadministrator fungiert, innerhalb des Unternehmens über mehrere Rollen verfügt. Wenn für den Unternehmensadministrator eine separate E-Mail-Adresse angegeben wird, umfasst die ursprüngliche Unternehmensstruktur den Unternehmensadministrator sowie ein einzelnes Benutzerkonto im Namen des Unternehmensadministrators. In diesem Fall kann sich der Unternehmensadministrator als Unternehmen oder als einzelner Benutzer beim Konto anmelden.

![Unternehmensstruktur mit Administrator- und Benutzerkonto](./assets/company-structure-tree-admin-user.png){width="600" zoomable="yes"}

Bei Händlern spiegelt sich die gesamte Unternehmensstruktur in den Rastern _Unternehmen_ und _Kunden_ innerhalb des Administrators wider. Das Unternehmensnetz listet alle Unternehmen unabhängig vom Status auf. Das folgende Beispiel zeigt Konten für zwei Unternehmen: das Unternehmen _ACME_ und das Unternehmen _Vendelay_.

![Unternehmensraster](./assets/companies-grid.png){width="700" zoomable="yes"}

Das folgende Beispiel zeigt das Raster [!UICONTROL Customers] mit den anfänglichen Unternehmensadministratorkonten für diese Unternehmen.

![Kundenraster mit dem Unternehmensadministratorkonto](./assets/company-admin-user-account.png){width="700" zoomable="yes"}

Nach Erstellung des Kontos muss der Unternehmensadministrator die Unternehmensstruktur von [Teams](account-company-structure.md) definieren, die [Unternehmensbenutzer](account-company-users.md) einrichten und für jede Gruppe [Rollen und Berechtigungen](account-company-roles-permissions.md) festlegen.

## Symbole für die Unternehmensstruktur

| Symbol | Beschreibung |
| ---- | ----------------- |
| ![Symbol &quot;Unternehmensadministrator&quot;](./assets/company-icon-admin.png) | Bezeichnet den Unternehmensadministrator in der Unternehmensstruktur. |
| ![Team-Symbol](./assets/company-icon-team.png) | Stellt ein Team in der Unternehmensstruktur dar. |
| ![Benutzersymbol](./assets/company-icon-user.png) | Stellt einen Benutzer in der Unternehmensstruktur dar. |
| ![Symbol &quot;Verschieben&quot;](./assets/company-icon-move.png) | Verschiebt ein Team an eine andere Position in der Unternehmensstruktur. |
| ![Erweiterungssymbol](./assets/company-icon-expand.png) | Erweitert ein Team in der Unternehmensstruktur. |
| ![Symbol &quot;Reduzieren&quot;](./assets/company-icon-collapse.png) | Reduziert ein Team in der Unternehmensstruktur. |

{style="table-layout:auto"}

## Erstellen von Unternehmensteams

Die Struktur eines Unternehmenskontos sollte die Einkaufs-Organisation widerspiegeln, sei es einfach und einfach oder komplex eine Organisation mit unterschiedlichen Teams für jede Unterteilung und jeden Geschäftsbereich des Unternehmens.

Wenn der Store [konfiguriert](enable-basic-features.md) ist, damit Unternehmen ihre eigenen Konten verwalten können, ist die Einrichtung der Unternehmensstruktur eine der ersten Aufgaben, die ein Unternehmensadministrator nach der Genehmigung des Kontos abschließen muss. Im Unternehmenskonto wird die Struktur des Unternehmens als Baum dargestellt, wobei sich der Unternehmensadministrator oben befindet.

![Unternehmensstruktur mit Teams](./assets/company-structure-teams-diagram.svg){width="450"}

1. Der Unternehmensadministrator meldet sich bei seinem Konto an.

1. Wählen Sie im linken Bereich **[!UICONTROL Company Structure]** aus.

1. Klicken Sie unter &quot;**[!UICONTROL Business Structure]**&quot;auf &quot;**[!UICONTROL Add Team]**&quot;und führt Folgendes aus:

   - Fügt die Werte **[!UICONTROL Team Title]** und **[!UICONTROL Description]** ein.

     Der Teamtitel kann beliebig sein, was die Struktur des Unternehmens darstellt, z. B. ein Team, ein Büro oder eine Abteilung innerhalb des Unternehmens

     ![Team hinzufügen](./assets/company-structure-add-team.png){width="700" zoomable="yes"}

   - Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]**.

   - Erstellt so viele Teams wie nötig.

     ![Unternehmensstruktur mit Teams](./assets/company-structure-teams.png){width="600" zoomable="yes"}

1. Gehen Sie wie folgt vor, um eine Hierarchie von Teams zu erstellen:

   - Wählt das übergeordnete Team aus und klicken Sie auf **[!UICONTROL Add Team]**.

     ![Unternehmensstruktur mit Divisionen](./assets/company-structure-northwest-division.png){width="600" zoomable="yes"}

   - Fügt die Werte **[!UICONTROL Team Title]** und **[!UICONTROL Description]** ein.

   - Klicks **[!UICONTROL Save]**.

1. Wiederholt diese Schritte, um so viele Teams, Divisionen und Unterteilungen wie nötig zu erstellen.

   ![Unternehmensstruktur mit Divisionen und Unterteilungen](./assets/company-structure-divisions.png){width="600" zoomable="yes"}

## Verschieben eines Teams

Wenn der Unternehmensadministrator mit der Unternehmensstruktur arbeitet, kann er Teams oder Abteilungen an andere Positionen in der Struktur ziehen.

1. Der Unternehmensadministrator ermittelt das zu verschiebende Team.

1. Klickt und zieht das Team an eine neue Position in der Unternehmensstruktur.

## Team löschen

>[!NOTE]
>
>Bevor Sie ein Team löschen, sollten Sie sicherstellen, dass das richtige Team ausgewählt ist. Gelöschte Teams können nicht wiederhergestellt werden.

1. Der Unternehmensadministrator wählt das zu löschende Team aus.

1. Klicks **[!UICONTROL Delete Selected]**.

1. Wenn Sie zur Bestätigung aufgefordert werden, klicken Sie auf **[!UICONTROL Delete]**.

## Erweitern oder Reduzieren der Teamstruktur

Wenn der Unternehmensadministrator mit der Unternehmensstruktur arbeitet, kann er den Baum reduzieren oder erweitern:

- Klicks **[!UICONTROL Collapse All]** oder **[!UICONTROL Expand All]**.

- Klicken Sie auf das Symbol ![Erweitert](../assets/icon-display-collapse.png) , um ein Team zu reduzieren, oder auf das Symbol &quot;Reduziert&quot;](../assets/icon-display-expand.png), um ein Team zu erweitern.![

## Zuweisen von Benutzern zu Teams

Wenn Teams und Benutzer zum ersten Mal zur [Unternehmensstruktur](account-company-structure.md) hinzugefügt werden, werden sie unter dem Unternehmensadministrator auf derselben Ebene platziert.

![Unternehmensstruktur mit Benutzern und Teams](./assets/company-users-added.png){width="700" zoomable="yes"}

| Kontrolle | Beschreibung |
|--- |--- |
| [!UICONTROL Collapse All / Expand All] | Die Struktur der Geschäftsstruktur wird entweder reduziert oder erweitert |
| [!UICONTROL Add User] | Erstellt einen Benutzer unterhalb des aktuellen Teams |
| [!UICONTROL Add Team] | Erstellt ein Team |
| [!UICONTROL Edit Selected / Delete Selected] | Bearbeiten oder Entfernen von Benutzern aus der Geschäftsstruktur |

{style="table-layout:auto"}

1. Im linken Bereich wählt der Unternehmensadministrator **[!UICONTROL Company Structure]** aus.

1. Um einen Benutzer einem vorhandenen Team zuzuweisen, ziehen sie den Benutzer (![Verschieben-Symbol](../assets/icon-move.png)) unter das entsprechende Team.

   ![Team-Zuweisungen](./assets/company-structure-teams-users-assigned.png){width="700" zoomable="yes"}
