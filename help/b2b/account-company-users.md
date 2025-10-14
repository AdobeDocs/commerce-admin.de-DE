---
title: Verwalten von Firmenbenutzerkonten
description: Erfahren Sie mehr über Firmenbenutzerkonten und wie sie in dem zugehörigen Firmenkonto funktionieren.
exl-id: 36b55f61-e579-4eb8-8f67-0156221d378e
feature: B2B, Companies, User Account, Storefront
role: Admin, User
source-git-commit: 9c16d7a3909598328cc42bbcbf39fc14ae6a9eb9
workflow-type: tm+mt
source-wordcount: '681'
ht-degree: 0%

---

# Verwalten von Firmenbenutzerkonten

In der Storefront werden Unternehmensbenutzer vom Unternehmensadministrator zugewiesen und auf der _[!UICONTROL Company Users]_&#x200B;Seite angezeigt. Diese Personen sind in der Regel Käufer mit unterschiedlichen Berechtigungsebenen für den Zugriff auf Storedienste und -ressourcen.

Der Unternehmensadministrator richtet zunächst die [Unternehmensstruktur](account-company-structure.md) ein und führt dann bei Bedarf die folgenden Aufgaben aus:

- Erstellen von Firmenbenutzenden und Zuweisen von Benutzenden zu Teams

- Definieren von Rollen und Berechtigungen und Zuweisen von Benutzern zu Rollen

Firmenbenutzer können nur vom Unternehmensadministrator hinzugefügt, bearbeitet, deaktiviert oder gelöscht werden.

- Wenn ein(e) Benutzende(r) entfernt wird, ändert sich der Kontostatus in *inaktiv* und der Kunde kann sich nicht mehr beim Unternehmen anmelden. Administratoren können weiterhin auf alle Inhalte zugreifen, die mit dem Benutzer verknüpft sind. Der Kontoadministrator kann den Zugriff wiederherstellen, indem er den Kontostatus auf der Seite [!UICONTROL Company Users] in *[!UICONTROL Active]* ändert.

- Wenn ein Benutzerkonto gelöscht wird, werden das Konto und alle zugehörigen Inhalte aus der Storefront gelöscht. Diese Aktion kann nicht rückgängig gemacht werden.

## Hinzufügen von Firmenbenutzenden

1. In der Storefront meldet sich der Unternehmensadministrator bei seinem Konto an.

1. Wählen Sie im linken Bedienfeld **[!UICONTROL Company Users]** aus.

   ![Firmenbenutzer](./assets/company-users-list-storefront.png){width="700" zoomable="yes"}

1. Klicks **[!UICONTROL Add New User]** und bewirkt Folgendes:

   - Gibt den **[!UICONTROL Job Title]** des neuen Benutzers ein.

   - Wählt den entsprechenden **[!UICONTROL User Role]** aus, wenn die Rollen und Berechtigungen definiert sind. Andernfalls können sie später zurückkehren, um die Rolle zuzuweisen.

     ![Neuen Benutzer hinzufügen](./assets/company-structure-users-add.png){width="700" zoomable="yes"}

   - Fügt die Benutzerinformationen in die verbleibenden Felder ein:
      - **[!UICONTROL First Name]** und **[!UICONTROL Last Name]**
      - **[!UICONTROL Email]**
      - **[!UICONTROL Work Phone Number]**

   Standardmäßig ist der **[!UICONTROL Status]** des Kontos `Active`.

1. Wenn Sie fertig sind, klicken Sie **[!UICONTROL Save]**.

1. Wiederholt den Vorgang, um so viele Unternehmensbenutzer wie nötig zu erstellen.

   Die neuen Benutzer werden zusammen mit dem Unternehmensadministrator in der Liste der Firmenbenutzer angezeigt.

Um Zeit bei der ersten Bestellung zu sparen, kann der Firmenadministrator jeden Firmenbenutzer daran erinnern, die standardmäßige Rechnungs- und Lieferadresse des Unternehmens zu seinem [Adressbuch“ &#x200B;](../customers/account-dashboard-address-book.md).

## Entfernen eines Benutzers aus der [!UICONTROL Company structure]

Unternehmensadministratoren können einen Benutzer aus der [!UICONTROL Company Structure] entfernen.

Nachdem ein Konto entfernt wurde, ändert sich der Benutzerkontenstatus in *inaktiv* und der Benutzer kann sich nicht mehr bei der Storefront anmelden.
Der Administrator kann ein Konto erneut aktivieren, indem er die Benutzerkontoinformationen auf der Seite „Firmenbenutzer“ bearbeitet.

1. In der Storefront meldet sich der Unternehmensadministrator bei seinem Konto an.

1. Wählen Sie im linken Bedienfeld **[!UICONTROL Company Structure]** aus.

1. Wählt den Unternehmensbenutzer in der Unternehmensstruktur aus.

1. Klicks **[!UICONTROL Remove from Structure]**.

   ![Benutzer löschen](./assets/company-structure-delete-user.png){width="600" zoomable="yes"}

1. Wenn Sie zur Bestätigung aufgefordert werden, klicken Sie auf **[!UICONTROL Remove]**.

   In der Admin-Liste bleibt der Firmenbenutzer im Raster [Kunden](../customers/customers-all.md) aufgeführt, jedoch mit einem `Inactive` Status.

## Anzeigen und Verwalten von Firmenbenutzerkonten

Unternehmensadministratoren können Firmenbenutzerkonten mit den Filtern „Anzeigen“ auf der Seite &quot;[!UICONTROL Company Users]&quot; anzeigen und verwalten.

![Firmenbenutzer](./assets/company-users-list-storefront.png){width="700" zoomable="yes"}

- Sie können nur inaktive Benutzer anzeigen, indem Sie **[!UICONTROL Show Inactive Users]** auswählen.
- Nur aktive Benutzer durch Auswahl von &quot;**[!UICONTROL Show Active Users]**&quot; anzeigen.
- Zeigen Sie alle Benutzer an, indem Sie **[!UICONTROL Show All Users]** auswählen.

Der Unternehmensadministrator kann ein einzelnes Konto mithilfe der *[!UICONTROL Actions]* für den Zeileneintrag verwalten, um die Kontoinformationen zu bearbeiten, den Kontostatus zu verwalten oder ein Konto zu löschen.

### Informationen zum Firmenbenutzerkonto bearbeiten

Firmenadministratoren können Informationen zu Benutzerkontenprofilen aktualisieren und den Kontostatus ändern.

1. Suchen Sie auf der Seite [!UICONTROL Company Users] das zu aktualisierende Benutzerkonto. Klicken Sie auf **[!UICONTROL Edit]**.

1. Nehmen Sie die erforderlichen Änderungen an den Benutzerkontoinformationen vor, einschließlich einer Änderung des Kontostatus.

1. Wenden Sie die Änderungen an, indem Sie auf **[!UICONTROL Save]** klicken.

>[!NOTE]
>
>Wenn Sie ein Firmenbenutzerkonto bearbeiten und feststellen, dass im Profil erforderliche Kontoinformationen wie Auftragstitel und geschäftliche Telefonnummer fehlen, zeigt dies an, dass das Konto von einem Commerce Site-Administrator hinzugefügt wurde. Diese Konten können nicht in der Storefront bearbeitet werden. Wenden Sie sich an Ihren Site-Administrator, um Informationen zu aktualisieren oder den Kontostatus zu ändern.

### Deaktivieren oder Löschen eines aktiven Kontos

1. Suchen Sie auf der Seite [!UICONTROL Company Users] das zu aktualisierende Benutzerkonto. Klicken Sie auf **[!UICONTROL Manage]**.

   ![Benutzer über die Seite „Firmenbenutzer verwalten“](./assets/company-users-manage-storefront.png){width="600" zoomable="yes"}

1. Deaktivieren oder löschen Sie das Benutzerkonto nach Bedarf, wenn Sie dazu aufgefordert werden.

>[!IMPORTANT]
>
>Durch das Löschen eines Firmenbenutzerkontos werden das Konto und alle zugehörigen Inhalte aus dem System entfernt. Diese Aktion kann nicht rückgängig gemacht werden.

## Beschreibung der Felder für das Benutzerkonto des Unternehmens

| Feld | Beschreibung |
|--------------------------------|---------------|
| [!UICONTROL Job Title] | Die Stellenbezeichnung des Firmenbenutzers. |
| [!UICONTROL User Role] | Die [Rolle](account-company-roles-permissions.md), die dem Firmenbenutzer zugewiesen wurde. Optionen: `Default User` / (andere Rollen) |
| [!UICONTROL First Name] | Der Vorname des Firmenbenutzers. |
| [!UICONTROL Last Name] | Der Nachname des Firmenbenutzers. |
| [!UICONTROL Email] | Die E-Mail-Adresse des Firmenbenutzers. |
| [!UICONTROL Work Phone Number] | Die geschäftliche Telefonnummer des Firmenbenutzers. |
| [!UICONTROL Status] | Der Status des Firmenbenutzerkontos. Optionen: `Active` / `Inactive` |

{style="table-layout:auto"}
