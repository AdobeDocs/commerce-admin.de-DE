---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Company Configuration]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der [!UICONTROL Customers] &gt; [!UICONTROL Company Configuration] Seite des Commerce-Administrators.
exl-id: 330eabeb-edab-4a9f-968e-37d0b95cdedb
feature: Configuration, Companies
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '837'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Company Configuration]

{{b2b-feature}}

{{config}}

>[!TIP]
>
>Mit der Installation und Aktivierung von Adobe Commerce B2B kann das Kauferlebnis mit unternehmensspezifischen Funktionen personalisiert werden. Adobe Commerce B2B ist eine integrierte Lösung, die sowohl B2B- als auch B2C-Modelle unterstützt. Weitere Informationen zu den B2B-Funktionen finden Sie im [Adobe Commerce B2B-Benutzerhandbuch](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html).

>[!NOTE]
>
>Der Zugriff auf diese Konfigurationsoptionen für B2B-Funktionen wird von der [Rollenressourcen](../../systems/permissions-user-roles.md#role-resources). Diese Rollenressourcen müssen für die Benutzerrolle festgelegt werden, die dem Admin-Benutzer zugewiesen ist.

Weitere Informationen zum Konfigurieren dieser Einstellungen finden Sie unter [Grundlegende B2B-Funktionen aktivieren](../../b2b/enable-basic-features.md) im _Adobe Commerce B2B-Benutzerhandbuch_.

## [!UICONTROL General]

![Allgemein](./assets/company-general.png)<!-- zoom -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Allow Company Registration from the Storefront] | Webseite | Bestimmt, ob Besucher Ihres Stores die Wahl haben, [registrieren](../../customers/customer-sign-in.md) für ein Unternehmenskonto oder ein individuelles Konto. Optionen: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Email Options - Company Registration]

![E-Mail-Optionen - Firmenregistrierung](./assets/company-email-options-company-registration.png)<!-- zoom -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Company Registration Email Recipient] | Store-Ansicht | Der Store-Kontakt, der benachrichtigt wird, wenn eine Registrierungsanfrage für ein Unternehmen von der Storefront gesendet wird. Optionen: `General Contact` / `Sales Representative` / `Customer Support` / `Custom Email 1` / `Custom Email 2` |
| [!UICONTROL Send Company Registration Email Copy To] | Store-Ansicht | Die E-Mail-Adresse jeder Person, die eine Kopie der Registrierungsbenachrichtigung erhalten soll. Trennen Sie mehrere E-Mail-Adressen durch Kommas. |
| [!UICONTROL Send Email Copy Method] | Store-Ansicht | Die E-Mail-Methode, mit der die Kopie der Registrierungs-E-Mail gesendet wird. Optionen: `Bcc` / `Separate Email` |
| [!UICONTROL Default Company Registration Email] | Store-Ansicht | Die E-Mail-Vorlage, die standardmäßig für die Benachrichtigung zur Unternehmensregistrierung verwendet wird. Standardvorlage: `Company Registration Request` |

{style="table-layout:auto"}

## [!UICONTROL Customer-Related Emails]

![Kundenbezogene E-Mails](./assets/company-email-options-customer-related-emails.png)<!-- zoom -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Default 'Sales Rep Assigned' Email] | Store-Ansicht | Die E-Mail-Vorlage, die standardmäßig verwendet wird, wenn einem Unternehmenskonto ein Vertriebsmitarbeiter zugewiesen wird. Diese E-Mail wird an den Vertriebsmitarbeiter und den Unternehmensadministrator gesendet. Standardvorlage: `Sales Representative Assigned to Company` |
| [!UICONTROL Default 'Assign Company to Customer' Email] | Store-Ansicht | Die E-Mail-Vorlage, die standardmäßig verwendet wird, wenn ein einzelnes Kundenkonto einem Unternehmenskonto zugewiesen wird. Diese E-Mail wird nur an den Kunden gesendet. Standardvorlage: `Assign Company to Customer` |
| [!UICONTROL Default 'Assign Company Admin' Email] | Store-Ansicht | Die E-Mail-Vorlage, die verwendet wird, wenn einem Unternehmen ein Unternehmensadministrator zugewiesen wird. Diese E-Mail wird an den Vertriebsmitarbeiter und den Unternehmensadministrator gesendet. Standardvorlage: `Assign Company Admin` |
| [!UICONTROL Default 'Company Admin Inactive' Email] | Store-Ansicht | Die E-Mail-Vorlage, die standardmäßig verwendet wird, wenn der Status der Person, die als Unternehmensadministrator dient, in &quot;Inaktiv&quot;geändert wird. Das System sendet eine E-Mail-Benachrichtigung über die Änderung an die neuen und ehemaligen Unternehmensadministratoren. Standardvorlage: `Company Admin Set Inactive` |
| [!UICONTROL Default 'Company Admin Changed to Member' Email] | Store-Ansicht | Die E-Mail-Vorlage, die standardmäßig verwendet wird, wenn der frühere Unternehmensadministrator ein Mitglied des Unternehmens wird. Die E-Mail wird nur an das Mitglied des Unternehmens gesendet. Standardvorlage: `Company Admin Changed to Member` |
| [!UICONTROL Default 'Customer Status Active' Email] | Store-Ansicht | Die E-Mail-Vorlage, die standardmäßig verwendet wird, wenn der Status eines Kunden aktiv wird. Diese E-Mail wird nur an den Kunden gesendet. Standardvorlage: `Customer Status Active` |
| [!UICONTROL Default 'Customer Status Inactive' Email] | Store-Ansicht | Die standardmäßig verwendete E-Mail-Vorlage, wenn der Status eines Kunden inaktiv wird. Diese E-Mail wird nur an den Kunden gesendet. Standardvorlage: `Customer Status Inactive` |

{style="table-layout:auto"}

## [!UICONTROL Company Status Change]

![Änderung des Unternehmensstatus](./assets/company-email-options-company-status-change.png)<!-- zoom -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Company Status Change Email Recipient] | Store-Ansicht | Der Store-Kontakt, der benachrichtigt wird, wenn sich der Status eines Unternehmens ändert. Optionen: `General Contact` / `Sales Representative` / `Customer Support` / `Custom Email 1` / `Custom Email 2` |
| [!UICONTROL Send Company Status Change Email Copy To] | Store-Ansicht | Die E-Mail-Adresse jeder Person, die eine Kopie der Benachrichtigung über die Statusänderung des Unternehmens erhalten soll. Trennen Sie mehrere E-Mail-Adressen durch Kommas. |
| [!UICONTROL Send Email Copy Method] | Store-Ansicht | Die E-Mail-Methode, mit der die Kopie der Benachrichtigung über die Statusänderung gesendet wird. Optionen: `Bcc` / `Separate Email` |
| [!UICONTROL Default "Company Status Change to Active 1' Email] | Store-Ansicht | Die E-Mail-Vorlage, die verwendet wird, wenn sich der Status eines Unternehmens ändert von _Ausstehende Genehmigung_ nach _Aktiv_. Standardvorlage: `Company Status Active 1` |
| [!UICONTROL Default 'Company Status Change to Active 2' Email] | Store-Ansicht | Die E-Mail-Vorlage, die standardmäßig verwendet wird, wenn sich der Status eines Unternehmens ändert von _Abgelehnt_ oder _Blockierung_ nach _Aktiv_. Standardvorlage: `Company Status Active 2` |
| [!UICONTROL Default 'Company Status Change to Rejected' Email] | Store-Ansicht | Die E-Mail-Vorlage, die standardmäßig verwendet wird, wenn sich der Status eines Unternehmens in _Abgelehnt_. Standardvorlage: `Company Status Rejected` |
| [!UICONTROL Default 'Company Status Change to Blocked' Email] | Store-Ansicht | Die E-Mail-Vorlage, die standardmäßig verwendet wird, wenn sich der Status eines Unternehmens in _Blockierung_. Standardvorlage: `Company Status Blocked` |
| [!UICONTROL Default 'Company Status Change to Pending Approval' Email] | Store-Ansicht | Die E-Mail-Vorlage, die standardmäßig verwendet wird, wenn sich der Status eines Unternehmens in _Ausstehende Genehmigung_. Standardvorlage: `Company Status Pending Approval` |

{style="table-layout:auto"}

## [!UICONTROL Company Credit]

![Firmenguthaben](./assets/company-email-options-company-credit.png)<!-- zoom -->

| Feld | [Anwendungsbereich](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Company Credit Change Email Sender] | Store-Ansicht | Der Store-Kontakt, der benachrichtigt wird, wenn eine Änderung am Guthaben eines Unternehmens stattfindet. Optionen: `General Contact` / `Sales Representative` / `Customer Support` / `Custom Email 1` / `Custom Email 2` |
| [!UICONTROL Send Company Credit Change Email Copy To] | Store-Ansicht | Die E-Mail-Adresse jeder Person, die eine Kopie der Benachrichtigung über eine Unternehmenskreditänderung erhält. Trennen Sie mehrere E-Mail-Adressen durch Kommas. |
| [!UICONTROL Send Email Copy Method] | Store-Ansicht | Die E-Mail-Methode, mit der die Kopie der Benachrichtigung über eine Kreditänderung gesendet wird. Optionen: `Bcc` / `Separate Email` |
| [!UICONTROL Allocated Email Template] | Store-Ansicht | Die E-Mail-Vorlage, die standardmäßig bei der Zuweisung von Firmenguthaben verwendet wird. Diese E-Mail wird an den Unternehmensadministrator gesendet. Standardvorlage: `Credit Limit Allocated` |
| [!UICONTROL Updated Email Template] | Store-Ansicht | Die E-Mail-Vorlage, die standardmäßig verwendet wird, wenn das Kreditlimit eines Unternehmens aktualisiert wird. Diese E-Mail wird an den Unternehmensadministrator gesendet. Standardvorlage: `Credit Limit Updated` |
| [!UICONTROL Reimbursed Email Template] | Store-Ansicht | Die E-Mail-Vorlage, die standardmäßig verwendet wird, wenn ein [Rückerstattung](../../b2b/credit-company.md#apply-a-payment-to-a-company-account) wird dem Unternehmen zugeschrieben. Diese E-Mail wird an den Unternehmensadministrator gesendet. Standardvorlage: `Credit Reimbursed` |
| [!UICONTROL Refunded Email Template] | Store-Ansicht | Die E-Mail-Vorlage, die standardmäßig verwendet wird, wenn ein aus einer Bestellung stammender Betrag an das Firmenguthaben zurückerstattet wird. Diese E-Mail wird an den Unternehmensadministrator gesendet. Standardvorlage: `Order Refunded to Company Credit` |
| [!UICONTROL Reverted Email Template] | Store-Ansicht | Die E-Mail-Vorlage, die standardmäßig verwendet wird, wenn eine Bestellung auf die Unternehmensgutschrift zurückgesetzt wird. Diese E-Mail wird an den Unternehmensadministrator gesendet. Standardvorlage: `Order Reverted to Company Credit` |

{style="table-layout:auto"}
