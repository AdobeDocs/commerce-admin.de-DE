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

![Unternehmensstruktur mit Geschäftsbereichen](./assets/company-structure-diagram.svg){width="500"}

Im Konto-Dashboard des Unternehmensadministrators wird die Unternehmensstruktur als Struktur dargestellt und besteht zunächst nur aus dem Unternehmensadministrator.

![Unternehmensstruktur mit Unternehmensadministrator](./assets/company-structure-tree-admin.png){width="600" zoomable="yes"}

Wenn das Konto erstellt und genehmigt wird, kann der Unternehmensadministrator die E-Mail-Adresse des Unternehmens verwenden oder eine andere E-Mail-Adresse erhalten.

Es ist möglich, dass die Person, die als Unternehmensadministrator fungiert, innerhalb des Unternehmens über mehrere Rollen verfügt. Wenn für den Unternehmensadministrator eine separate E-Mail-Adresse angegeben wird, umfasst die ursprüngliche Unternehmensstruktur den Unternehmensadministrator sowie ein einzelnes Benutzerkonto im Namen des Unternehmensadministrators. In diesem Fall kann sich der Unternehmensadministrator als Unternehmen oder als einzelner Benutzer beim Konto anmelden.

![Unternehmensstruktur mit Administrator- und Benutzerkonto](./assets/company-structure-tree-admin-user.png){width="600" zoomable="yes"}

Bei Händlern spiegelt sich die gesamte Unternehmensstruktur in der _Unternehmen_ und _Kunden_ Raster innerhalb des Administrators. Das Unternehmensnetz listet alle Unternehmen unabhängig vom Status auf. Das folgende Beispiel zeigt zwei Unternehmen: die _ACME_ und _Vendelay_ Unternehmen.

![Unternehmensraster](./assets/companies-grid.png){width="700" zoomable="yes"}

Das folgende Beispiel zeigt die [!UICONTROL Customers] mit den anfänglichen Unternehmensadministratorkonten für diese Unternehmen.

![Kunden werden mit dem Unternehmensadministratorkonto über das Raster informiert](./assets/company-admin-user-account.png){width="700" zoomable="yes"}

Nach Erstellung des Kontos muss der Unternehmensadministrator die Unternehmensstruktur von [Teams](account-company-structure.md), richten Sie die [Unternehmensbenutzer](account-company-users.md)und [Rollen und Berechtigungen](account-company-roles-permissions.md) für jede.

## Symbole für die Unternehmensstruktur

| Symbol | Beschreibung |
| ---- | ----------------- |
| ![Symbol für Unternehmensadministrator](./assets/company-icon-admin.png) | Bezeichnet den Unternehmensadministrator in der Unternehmensstruktur. |
| ![Team-Symbol](./assets/company-icon-team.png) | Stellt ein Team in der Unternehmensstruktur dar. |
| ![Benutzersymbol](./assets/company-icon-user.png) | Stellt einen Benutzer in der Unternehmensstruktur dar. |
| ![Symbol Verschieben](./assets/company-icon-move.png) | Verschiebt ein Team an eine andere Position in der Unternehmensstruktur. |
| ![Erweiterungssymbol](./assets/company-icon-expand.png) | Erweitert ein Team in der Unternehmensstruktur. |
| ![Symbol &quot;Reduzieren&quot;](./assets/company-icon-collapse.png) | Reduziert ein Team in der Unternehmensstruktur. |

{style="table-layout:auto"}

## Erstellen von Unternehmensteams

Die Struktur eines Unternehmenskontos sollte die Einkaufs-Organisation widerspiegeln, sei es einfach und einfach oder komplex eine Organisation mit unterschiedlichen Teams für jede Unterteilung und jeden Geschäftsbereich des Unternehmens.

Wenn der Store [konfiguriert](enable-basic-features.md) Damit Unternehmen ihre eigenen Konten verwalten können, gehört die Einrichtung der Unternehmensstruktur zu den ersten Aufgaben, die ein Unternehmensadministrator nach Genehmigung des Kontos abschließen muss. Im Unternehmenskonto wird die Struktur des Unternehmens als Baum dargestellt, wobei sich der Unternehmensadministrator oben befindet.

![Unternehmensstruktur mit Teams](./assets/company-structure-teams-diagram.svg){width="450"}

1. Der Unternehmensadministrator meldet sich bei seinem Konto an.

1. Wählen Sie im linken Bereich **[!UICONTROL Company Structure]**.

1. under **[!UICONTROL Business Structure]**, Klicks **[!UICONTROL Add Team]** und führt Folgendes aus:

   - Fügt die **[!UICONTROL Team Title]** und **[!UICONTROL Description]**.

     Der Teamtitel kann beliebig sein, was die Struktur des Unternehmens darstellt, z. B. ein Team, ein Büro oder eine Abteilung innerhalb des Unternehmens

     ![Team hinzufügen](./assets/company-structure-add-team.png){width="700" zoomable="yes"}

   - Klicken Sie nach Abschluss **[!UICONTROL Save]**.

   - Erstellt so viele Teams wie nötig.

     ![Unternehmensstruktur mit Teams](./assets/company-structure-teams.png){width="600" zoomable="yes"}

1. Gehen Sie wie folgt vor, um eine Hierarchie von Teams zu erstellen:

   - Wählen Sie das übergeordnete Team aus und klicken Sie auf **[!UICONTROL Add Team]**.

     ![Unternehmensstruktur mit Geschäftsbereichen](./assets/company-structure-northwest-division.png){width="600" zoomable="yes"}

   - Fügt die **[!UICONTROL Team Title]** und **[!UICONTROL Description]**.

   - Klicks **[!UICONTROL Save]**.

1. Wiederholt diese Schritte, um so viele Teams, Divisionen und Unterteilungen wie nötig zu erstellen.

   ![Unternehmensstruktur mit Abteilungen und Unterteilungen](./assets/company-structure-divisions.png){width="600" zoomable="yes"}

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

1. Wenn Sie zur Bestätigung aufgefordert werden, klickt **[!UICONTROL Delete]**.

## Erweitern oder Reduzieren der Teamstruktur

Wenn der Unternehmensadministrator mit der Unternehmensstruktur arbeitet, kann er den Baum reduzieren oder erweitern:

- Klicks **[!UICONTROL Collapse All]** oder **[!UICONTROL Expand All]**.

- Klicks ![Symbol &quot;Erweitert&quot;](../assets/icon-display-collapse.png) zum Reduzieren eines Teams oder ![Reduziertes Symbol](../assets/icon-display-expand.png) , um ein Team zu erweitern.

## Zuweisen von Benutzern zu Teams

Wenn Teams und Benutzer zum ersten Mal zum [Unternehmensstruktur](account-company-structure.md), werden sie unter dem Unternehmensadministrator auf derselben Ebene platziert.

![Unternehmensstruktur mit Benutzern und Teams](./assets/company-users-added.png){width="700" zoomable="yes"}

| Kontrolle | Beschreibung |
|--- |--- |
| [!UICONTROL Collapse All / Expand All] | Die Struktur der Geschäftsstruktur wird entweder reduziert oder erweitert |
| [!UICONTROL Add User] | Erstellt einen Benutzer unterhalb des aktuellen Teams |
| [!UICONTROL Add Team] | Erstellt ein Team |
| [!UICONTROL Edit Selected / Delete Selected] | Bearbeiten oder Entfernen von Benutzern aus der Geschäftsstruktur |

{style="table-layout:auto"}

1. Im linken Bereich wählt der Unternehmensadministrator **[!UICONTROL Company Structure]**.

1. Um einen Benutzer einem vorhandenen Team zuzuweisen, ziehen sie (![Symbol Verschieben](../assets/icon-move.png)) den Benutzer unter dem entsprechenden Team.

   ![Teamzuweisungen](./assets/company-structure-teams-users-assigned.png){width="700" zoomable="yes"}
