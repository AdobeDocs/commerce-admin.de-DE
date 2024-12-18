---
title: Kontostruktur der Firma
description: Erfahren Sie mehr über Unternehmensstrukturen und darüber, wie ein Unternehmensadministrator sie definieren kann, um seine geschäftlichen Workflows und Richtlinien zu unterstützen.
exl-id: 4724b208-b6ac-4de5-9a4c-bc4d68402506
feature: B2B, Companies
role: Admin
source-git-commit: fec72b792cf3149c05803874795c45f9f4e28673
workflow-type: tm+mt
source-wordcount: '709'
ht-degree: 0%

---

# Kontostruktur der Firma

Ein Unternehmenskonto kann entsprechend der Struktur des Unternehmens eingerichtet werden. Zunächst umfasst die Unternehmensstruktur nur den Unternehmensadministrator, kann jedoch um Teams von Benutzern erweitert werden. Die Benutzer können mit Teams verknüpft oder innerhalb einer Hierarchie von Abteilungen und Unterabteilungen innerhalb des Unternehmens organisiert sein.

![Unternehmensstruktur mit Geschäftsbereichen](./assets/company-structure-diagram.svg){width="500"}

Im Dashboard des Unternehmensadministrators in der Storefront wird die Unternehmensstruktur als Baumstruktur dargestellt und besteht zunächst nur aus dem Unternehmensadministrator.

![Unternehmensstruktur mit Unternehmensadministrator](./assets/company-structure-tree-admin.png){width="700" zoomable="yes"}

Bei Händlern spiegelt sich die vollständige Unternehmensstruktur in den Rastern _Firmen_ und _Kunden_ innerhalb von Admin wider. Im Raster Firmen werden alle Unternehmen unabhängig vom Status aufgelistet.

![Firmen-Raster](./assets/companies-grid.png){width="700" zoomable="yes"}

Das folgende Beispiel zeigt für jedes Unternehmen das [!UICONTROL Customers] Raster mit den anfänglichen Unternehmensadministratorkonten.

![Kundenraster mit Firmen-Administratorkonten](./assets/company-admin-user-account.png){width="700" zoomable="yes"}

Nach der Erstellung des Kontos kann der Unternehmensadministrator eine Unternehmensstruktur mit [Teams](account-company-structure.md) definieren, die [Unternehmensbenutzer](account-company-users.md) einrichten und [Rollen und Berechtigungen](account-company-roles-permissions.md) für jeden festlegen.

>[!NOTE]
>
>Wenn ein Firmenbenutzer hinzugefügt wird, wird der Firmenbenutzer zunächst der Stammunternehmensstruktur hinzugefügt, die dem Firmenadministrator untergeordnet ist. Wenn der Unternehmensadministrator mehrere Rollen innerhalb des Unternehmens ausführt, erstellen Sie für jede Rolle separate Unternehmensbenutzerkonten mit einer anderen E-Mail-Adresse.

## Symbole für Unternehmensstrukturen

| Symbol | Beschreibung |
| ---- | ----------------- |
| ![Symbol „Unternehmensadministrator“](./assets/company-icon-admin.png) | Stellt den Unternehmensadministrator in der Unternehmensstruktur dar. |
| ![Team-Symbol](./assets/company-icon-team.png) | Stellt ein Team in der Unternehmensstruktur dar. |
| ![Benutzersymbol](./assets/company-icon-user.png) | Stellt einen Benutzer in der Unternehmensstruktur dar. |
| ![move icon](./assets/company-icon-move.png) | Verschiebt ein Team an eine andere Position in der Unternehmensstruktur. |
| ![Erweiterungssymbol](./assets/company-icon-expand.png) | Erweitert ein Team in der Unternehmensstruktur. |
| ![Symbol „Reduzieren“](./assets/company-icon-collapse.png) | Reduziert ein Team in der Unternehmensstruktur. |

{style="table-layout:auto"}

## Erstellen von Unternehmens-Teams

Die Struktur eines Unternehmenskontos sollte die Einkaufsorganisation widerspiegeln, unabhängig davon, ob es sich um eine einfache und flache oder eine komplexe Organisation mit verschiedenen Teams für jede Unterteilung und Abteilung des Unternehmens handelt.

Wenn der Store [konfiguriert](enable-basic-features.md) ist, damit Unternehmen ihre eigenen Konten verwalten können, ist die Einrichtung der Unternehmensstruktur eine der ersten Aufgaben, die ein Unternehmensadministrator nach der Genehmigung des Kontos durchführen muss. Im Unternehmenskonto wird die Struktur der Firma als Baumstruktur dargestellt, wobei der Unternehmensadministrator oben steht.

![Unternehmensstruktur mit Teams](./assets/company-structure-teams-diagram.svg){width="450"}

1. Der Unternehmensadministrator meldet sich bei seinem Konto an.

1. Wählen Sie im linken Bedienfeld **[!UICONTROL Company Structure]** aus.

1. Klicken Sie unter **[!UICONTROL Business Structure]** auf **[!UICONTROL Add Team]** und führen Sie folgende Schritte aus:

   - Gibt den **[!UICONTROL Team Title]** und die **[!UICONTROL Description]** ein.

     Der Team-Titel kann alles sein, was die Struktur des Unternehmens darstellt, z. B. ein Team, ein Büro oder eine Abteilung innerhalb des Unternehmens

     ![Team hinzufügen](./assets/company-structure-add-team.png){width="700" zoomable="yes"}

   - Wenn Sie fertig sind, klicken Sie **[!UICONTROL Save]**.

   - Erstellt so viele Teams wie nötig.

1. Um eine Hierarchie von Teams zu erstellen, führt der Administrator die folgenden Schritte aus:

   - Wählen Sie das übergeordnete Team aus und klicken Sie auf **[!UICONTROL Add Team]**.

     ![Unternehmensstruktur mit Geschäftsbereichen](./assets/company-structure-northwest-division.png){width="600" zoomable="yes"}

   - Gibt den **[!UICONTROL Team Title]** und die **[!UICONTROL Description]** ein.

   - Klicks **[!UICONTROL Save]**.

1. Wiederholt diese Schritte, um so viele Teams, Abteilungen und Unterteilungen wie nötig zu erstellen.

   ![Unternehmensstruktur mit Abteilungen und Unterabteilungen](./assets/company-structure-divisions.png){width="600" zoomable="yes"}

## Verschieben eines Teams

Da der Unternehmensadministrator mit der Unternehmensstruktur arbeitet, kann er Teams oder Abteilungen an andere Positionen in der Struktur ziehen.

1. Der Unternehmensadministrator findet das Team, das verschoben werden soll.

1. Klickt und zieht das Team an eine neue Position in der Unternehmensstruktur.

## Team löschen

>[!NOTE]
>
>Bevor Sie ein Team löschen, sollten Sie sicherstellen, dass das richtige Team ausgewählt ist - gelöschte Teams können nicht wiederhergestellt werden.

1. Der Unternehmensadministrator wählt das zu löschende Team aus.

1. Klicks **[!UICONTROL Delete Selected]**.

1. Wenn Sie zur Bestätigung aufgefordert werden, klicken Sie auf **[!UICONTROL Delete]**.

## Teamstruktur erweitern oder reduzieren

Wenn der Unternehmensadministrator bzw. die Unternehmensadministratorin mit der Unternehmensstruktur arbeitet, kann er bzw. sie die Struktur reduzieren oder erweitern:

- Klicks **[!UICONTROL Collapse All]** oder **[!UICONTROL Expand All]**.

- Klicken Sie auf ![Symbol „Erweitert](../assets/icon-display-collapse.png), um ein Team zu reduzieren, oder ![Symbol „Reduziert](../assets/icon-display-expand.png), um ein Team zu erweitern.

## Zuweisen von Benutzern zu Teams

Wenn Teams und Benutzer zum ersten Mal zur [Unternehmensstruktur](account-company-structure.md) hinzugefügt werden, werden sie auf derselben Ebene unter dem Unternehmensadministrator platziert.

![Unternehmensstruktur mit Benutzern und Teams](./assets/company-users-added.png){width="700" zoomable="yes"}

| Kontrolle | Beschreibung |
|--- |--- |
| [!UICONTROL Collapse All / Expand All] | Reduziert oder erweitert die Struktur der Unternehmensstruktur |
| [!UICONTROL Add User] | Erstellt einen Benutzer unterhalb des aktuellen Teams |
| [!UICONTROL Add Team] | Erstellt ein Team |
| [!UICONTROL Edit Selected / Remove from Structure] | Bearbeitet Benutzerinformationen oder entfernt Benutzer aus der Business-Struktur. Weitere Informationen finden Sie unter [Verwalten von Firmenbenutzerkonten](account-company-users.md). |

{style="table-layout:auto"}

1. Im linken Bedienfeld wählt der Unternehmensadministrator **[!UICONTROL Company Structure]** aus.

1. Um einen Benutzer einem vorhandenen Team zuzuweisen, ziehen sie den Benutzer (![move icon](../assets/icon-move.png)) unter das entsprechende Team.

   ![Team-Arbeitsaufträge](./assets/company-structure-teams-users-assigned.png){width="700" zoomable="yes"}
