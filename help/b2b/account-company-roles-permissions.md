---
title: Unternehmensrollen und -berechtigungen
description: Erfahren Sie mehr über Rollen und Berechtigungen, die ein Unternehmensadministrator auf Benutzende im Unternehmen anwenden kann, wodurch er auf verschiedenen Ebenen Zugriff auf Bestellinformationen und Ressourcen hat.
exl-id: 9fe20d6a-2c9c-4618-a395-805d64dcf0de
feature: B2B, Companies, Roles/Permissions
role: Admin
source-git-commit: bad59798a1a6d97826dc421fe8614ef511e067bd
workflow-type: tm+mt
source-wordcount: '521'
ht-degree: 0%

---

# Unternehmensrollen und -berechtigungen

Rollen für Unternehmensbenutzer werden mit verschiedenen Berechtigungsebenen für den Zugriff auf Verkaufsinformationen und Ressourcen eingerichtet. Standardmäßig ist der Unternehmensadministrator ein &quot;_&quot; mit_ Berechtigungen. Die [Zugriff verweigert](../content-design/pages.md#access-denied) wird angezeigt, wenn der Benutzer nicht berechtigt ist, auf die Seite zuzugreifen.

![Seite „Rollen und Berechtigungen“ mit Standardrolle](./assets/company-roles-permissions.png){width="700" zoomable="yes"}

Das System verfügt über eine vordefinierte Standardbenutzerrolle, die Sie unverändert _oder_ Ihren Anforderungen anpassen können. Sie können so viele Rollen erstellen, wie für Ihre Unternehmensstruktur und die organisatorischen Zuständigkeiten erforderlich sind, z. B.:

- **Standardbenutzer** - Der Standardbenutzer hat vollen Zugriff auf Aktivitäten im Zusammenhang mit Verkäufen und Angeboten sowie nur Lesezugriff auf Unternehmensprofil- und Kreditinformationen.

- **Senior Buyer** - Ein Senior Buyer hat möglicherweise Zugriff auf alle Sales- und Quotes-Ressourcen und hat schreibgeschützte Berechtigungen für das Unternehmensprofil, Benutzer und Teams, Zahlungsinformationen und Firmenkredite.

- **Hilfskäufer** - Ein Hilfskäufer kann berechtigt sein, eine Bestellung über _Checkout mit Angebot_ aufzugeben und Bestellungen, Angebote und Informationen im Unternehmensprofil anzuzeigen.

## Verwalten von Rollen und Berechtigungen

1. Der Unternehmensadministrator meldet sich bei seinem Store-Konto an.

1. Wählen Sie im linken Bedienfeld **[!UICONTROL Roles and Permissions]** aus.

1. Führt eine der folgenden Aufgaben aus.

### Erstellen einer Rolle

1. Klicks **[!UICONTROL Add New Role]**.

   ![Neue Rolle hinzufügen](./assets/company-roles-permissions-add-storefront.png){width="600" zoomable="yes"}

1. Gibt einen beschreibenden **[!UICONTROL Role Name]** ein.

1. Führen Sie unter _[!UICONTROL Role Permissions]_einen der folgenden Schritte aus:

   - Aktiviert das Kontrollkästchen jeder Ressource oder Aktivität, der Benutzer bzw. Benutzerinnen, denen die Rolle zugewiesen wurde, Zugriffsberechtigungen zuweisen.

   - Aktiviert das Kontrollkästchen **[!UICONTROL All]** und deaktiviert das Kontrollkästchen aller Ressourcen oder Aktivitäten, auf die Benutzende, die der Rolle zugewiesen sind, keine Zugriffsberechtigung haben.

1. Klicks **[!UICONTROL Save Role]**.

1. Erstellt so viele Rollen wie nötig, indem diese Schritte wiederholt werden.

### Rolle ändern

1. Damit die Rolle geändert werden kann, klickt der Unternehmensadministrator in der Spalte &quot;_[!UICONTROL Actions]_&quot; auf **[!UICONTROL Edit]**.

1. Nehmen Sie die erforderlichen Änderungen an den Einstellungen für Name und Berechtigung vor.

1. Wenn Sie fertig sind, klicken Sie **[!UICONTROL Save Role]**.

### Duplizieren einer Rolle

1. Damit die Rolle dupliziert werden kann, klickt der Unternehmensadministrator in der Spalte &quot;_[!UICONTROL Actions]_&quot; auf **[!UICONTROL Duplicate]**.

1. Nehmen Sie die erforderlichen Änderungen an den Einstellungen für Name und Berechtigung vor.

1. Wenn Sie fertig sind, klicken Sie **[!UICONTROL Save Role]**.

### Löschen einer Rolle

1. Der Unternehmensadministrator findet die Rolle, die gelöscht werden soll, in der Liste der Rollen.

   Nur Rollen ohne zugewiesene Benutzer können gelöscht werden.

1. Klicks **[!UICONTROL Delete]** in die _[!UICONTROL Actions]_Spalte.

1. Wenn Sie zur Bestätigung aufgefordert werden, klicken Sie auf **[!UICONTROL OK]**.

## Aktionen

| Aktion | Beschreibung |
|-----------| ----------- |
| [!UICONTROL Duplicate] | Erstellt eine Kopie der ausgewählten Rolle. Der Name der doppelten Rolle `- Duplicated` am Ende hinzugefügt. |
| [!UICONTROL Edit] | Ändern Sie den Namen und/oder den Berechtigungssatz. |
| [!UICONTROL Delete] | Löschen Sie die Rolle. Nur Rollen ohne zugewiesene Benutzer können gelöscht werden. |

{style="table-layout:auto"}

## Rollenberechtigungen

Unternehmensadministratoren können die Berechtigungskonfiguration für eine Rolle aktualisieren, indem sie die [!UICONTROL Edit action] auswählen und dann Berechtigungen in der Liste **Rollenberechtigungen** auswählen oder entfernen.

![Rollen- und Berechtigungsliste](./assets/role-permissions-list.png){width="700" zoomable="yes"}

## Einem Firmenbenutzer eine Rolle zuweisen

Nach der Definition der erforderlichen Rollen weist der Unternehmensadministrator jedem Firmenbenutzer eine Rolle zu.

1. Meldet sich bei ihrem Unternehmenskonto als Unternehmensadministrator an.

1. Wählen Sie im linken Bedienfeld **[!UICONTROL Company Users]** aus.

   ![Firmenbenutzer](./assets/company-users-list-storefront.png){width="700" zoomable="yes"}

1. Sucht den Benutzer in der Liste und klickt auf **[!UICONTROL Edit]**.

1. Wählt den entsprechenden **[!UICONTROL User Role]** für den Benutzer aus.

   ![Benutzer bearbeiten - Benutzerrolle auswählen](./assets/company-user-assign-role.png){width="700" zoomable="yes"}

1. Klicks **[!UICONTROL Save]**.
