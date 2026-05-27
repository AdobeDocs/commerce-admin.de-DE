---
title: Unternehmenskonten
description: Erfahren Sie, wie in Ihrem Adobe Commerce Store verwaltete Unternehmenskonten es ermöglichen, mehrere Käufer, die zum selben Unternehmen gehören, in einem einzigen Unternehmenskonto zu vereinen.
exl-id: 0b3c3635-a1cf-4ee6-a8bc-e7cbcb4e2e63
feature: B2B, Companies, Configuration
source-git-commit: 99285b700b91e0072340a2231c39a8050818fd17
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 0%

---

# Unternehmenskonten

Wenn Sie B2B-Unternehmenskonten in Ihren Store integrieren, können Sie das Einkaufserlebnis des Unternehmens vereinfachen, indem Sie es Unternehmen ermöglichen, mehrere Unterkonten mit flexiblen Berechtigungen basierend auf Benutzerrollen in ihrer Organisation zu erstellen.

Je nach Unternehmen kann ein Store-Administrator Promotions und Preise an ihre Bedürfnisse anpassen und hochgradig angepasste Angebote erstellen, die den Anforderungen der Käufer entsprechen und die Bestellungen erhöhen.

Durch das Hinzufügen einer Unternehmenskontenzuordnung zu einer standardmäßigen [Person](../customers/account-create.md) kann der Kunde die für das Unternehmen definierten spezifischen Einkaufs-Workflows verwenden.

Vorteile eines Firmenkontos:

- Bietet unbegrenzte [Firmenbenutzer](account-company-users.md) und die Erstellung zusätzlicher Konten, was den Unternehmenskauf vereinfacht.

- Umfasst Unterstützung für eine _Smart_-Unternehmenskontenhierarchie mit verschiedenen [&#x200B; (Rollen und Berechtigungen](account-company-roles-permissions.md) für die Auftragserteilung.

- Bietet einen Mechanismus für Händler zur Einkommenssteigerung, indem sie [Firmenkundenkredit](credit-company.md) als Zahlungsmethode anbieten.

- Unterstützt [Verwaltung](account-company-manage.md) aller Unternehmenskonten vom Administrator.

## Anzeigen von Unternehmenskonten

Das _Firmen_-Raster listet alle aktiven Unternehmenskonten und ausstehenden Anfragen auf, unabhängig von der Statuseinstellung. Darüber hinaus stehen die Tools zum [&#x200B; (Erstellen](account-company-create.md) und [) &#x200B;](account-company-manage.md) Unternehmenskonten zur Verfügung. Verwenden Sie die standardmäßigen Rastersteuerelemente, um die Liste zu filtern und das Spaltenlayout anzupassen. Eine Liste der Spaltenbeschreibungen finden Sie im Abschnitt _Spaltenbeschreibungen_ in [Verwalten von Unternehmenskonten](account-company-manage.md).

Kunden können ein Unternehmenskonto in der Storefront erstellen oder ein Händler kann eines in der Admin erstellen. Standardmäßig ist die Möglichkeit zum Erstellen von Unternehmenskonten in der Storefront aktiviert. Wenn die Konfiguration dies zulässt, kann ein Besucher des Stores die Eröffnung eines Unternehmenskontos anfordern. Nachdem das Unternehmenskonto genehmigt wurde, kann der Unternehmensadministrator die Unternehmensstruktur und Benutzer mit verschiedenen Berechtigungsebenen einrichten.

Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

![Firmen-Raster](./assets/companies-grid.png){width="700" zoomable="yes"}

Das [!UICONTROL Companies]-Raster listet alle Unternehmen unabhängig vom Status auf. Die Auflistung des Unternehmens gibt an, ob ein Unternehmen einer [Unternehmenshierarchie](manage-company-hierarchy.md) zugeordnet ist, und enthält [detaillierte Informationen](/help/b2b/account-company-manage.md#company-options-and-columns) über das Unternehmen, den Unternehmensadministrator und andere Informationen. Passen Sie die Ansicht mithilfe der [Admin-Rastersteuerelemente](../getting-started/admin-grid-controls.md) an, um Filter, Spaltenansichtsoptionen und mehr festzulegen.

## Unternehmensadministrator

Das folgende Beispiel zeigt das Raster _Kunden_ mit anfänglichen Unternehmensadministratorkonten.

![Kundenraster mit Firmenadministratorkonto](./assets/company-admin-user-account.png){width="700" zoomable="yes"}

Jedes Unternehmen verfügt über einen einzelnen Unternehmensadministrator, der durch die E-Mail-Adresse des Kontos sowie den Vor- und Nachnamen des Administrators identifiziert wird. Der Administrator kann anderen Unternehmen als Benutzer zugewiesen werden, er kann jedoch Administrator nur für ein Unternehmen sein.

Nach der Erstellung des Kontos definiert der Unternehmensadministrator die Unternehmensstruktur von [Teams](account-company-structure.md), richtet die [Unternehmensbenutzer](account-company-users.md) ein und richtet [Rollen und Berechtigungen](account-company-roles-permissions.md) für jeden ein.

### Festlegen des Kennworts für den Unternehmensadministrator vor der ersten Anmeldung

1. Der Unternehmensadministrator findet eine Begrüßungs-E-Mail im Store.

   ![Beispiel-Begrüßungs-E-Mail](./assets/company-admin-welcome-email.png){width="500"}

   >[!NOTE]
   >
   >Die E-Mail-Adressziele und der Inhalt der E-Mail werden durch die Optionen bestimmt, die in der Konfiguration [E-Mail-Optionen für Unternehmen](email-company-configuration.md) angegeben sind.

1. Folgt den Anweisungen und klickt auf [!UICONTROL **link**], um sein Kennwort festzulegen.

1. Geben Sie ein [!UICONTROL **Neues Kennwort**] und eine Kennwortbestätigung für das Konto ein.

   Das Kennwort muss mindestens drei der folgenden Zeichentypen enthalten:

   - Kleinbuchstaben (abc…)
   - Großbuchstaben (ABC…)
   - Zahlen (1234567890)
   - Sonderzeichen (!@#$…)

1. Klicken Sie [!UICONTROL **Neues Kennwort festlegen**].

   ![Kundenanmeldung - Unternehmensadmin](./assets/company-admin-account-login.png){width="700" zoomable="yes"}

1. Wenn die Seite [!UICONTROL Customer Login] angezeigt wird, gibt der Kunde seine [!UICONTROL **E-Mail**] und [!UICONTROL **Passwort**] ein.

1. Klickt auf [!UICONTROL **Anmelden**], um auf sein Konto-Dashboard zuzugreifen.

   ![Konto-Dashboard - Firma](./assets/account-dashboard-company.png){width="700" zoomable="yes"}

## Unternehmensstruktur

Ein Unternehmenskonto kann entsprechend der Struktur des Unternehmens eingerichtet werden. Zunächst umfasst die Unternehmensstruktur nur den Unternehmensadministrator, kann jedoch um Teams von Benutzern erweitert werden. Die Benutzer können mit Teams verknüpft oder innerhalb einer Hierarchie von Abteilungen und Unterabteilungen innerhalb des Unternehmens organisiert sein. Die Struktur unterstützt die Verwendung von [Genehmigungsregeln](account-dashboard-approval-rules.md) für [Bestellungen](purchase-order-flow.md), die mit dem Unternehmenskonto verknüpft sind.

![Unternehmensstruktur mit Geschäftsbereichen](./assets/company-structure-diagram.svg){width="450"}

Im Dashboard des Unternehmensadministrators wird die Unternehmensstruktur als Baumstruktur dargestellt und besteht zunächst nur aus dem Unternehmensadministrator.

![Unternehmensstruktur mit Unternehmensadministrator](./assets/company-structure-tree-admin.png){width="600"}

Wenn das Konto erstellt wird, kann der Unternehmensadministrator die E-Mail-Adresse des Unternehmens verwenden oder ihm eine andere E-Mail-Adresse zugewiesen werden.

Im folgenden Beispiel umfasst die anfängliche Unternehmensstruktur den Unternehmensadministrator plus ein individuelles Benutzerkonto im Namen des Unternehmensadministrators. Funktionen des Unternehmensadministrators (z. B. Unternehmensstruktur und Genehmigungsregeln) sind jedoch nur verfügbar, wenn sie bei dem Benutzerkonto angemeldet sind, das als Unternehmensadministrator festgelegt ist.

![Unternehmensstruktur mit Administrator- und Benutzerkonto](./assets/company-structure-tree-admin-user.png){width="600"}
