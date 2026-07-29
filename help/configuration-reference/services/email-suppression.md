---
title: '[!UICONTROL Adobe Services] > [!UICONTROL Email Suppression]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Adobe Services] > [!UICONTROL Email Suppression] des Commerce Admin.
feature: Configuration, Communications
badgeSaas: label="Nur SaaS" type="Positive" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce as a Cloud Service- und Adobe Commerce Optimizer-Projekte (von Adobe verwaltete SaaS-Infrastruktur)."
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: f4d7033067a99421224ab2159b1b95775e5e949f
workflow-type: tm+mt
source-wordcount: 316
ht-degree: 0%

---

# [!UICONTROL Adobe Services] > [!UICONTROL Email Suppression]

{{config}}

[!UICONTROL Email Suppression] ermöglicht es Administratoren, bestimmte Kategorien automatisierter System-E-Mails zu deaktivieren, ohne den Rest der E-Mail-Adresse des Stores zu beeinflussen oder die Beteiligung von Entwicklern zu erfordern. Verwenden Sie diese Funktion, um bestimmte Benachrichtigungen vorübergehend oder dauerhaft zu stoppen, z. B. die Bestellung von E-Mails während einer Datenmigration oder Marketing-E-Mails.

>[!IMPORTANT]
>
>Sicherheitsbezogene Admin-Benachrichtigungen, wie z. B. Zwei-Faktor-Authentifizierungs-Codes und E-Mails zum Zurücksetzen des Admin-Kennworts, werden von dieser Funktion nie unterdrückt.

Die Einstellungen auf dieser Seite gelten pro [Store-Ansicht](../../getting-started/websites-stores-views.md#scope-settings) sodass Sie verschiedene E-Mail-Kategorien für verschiedene Storefronts unterdrücken können.

>[!NOTE]
>
>Durch Deaktivieren der Unterdrückung wird der normale E-Mail-Versand sofort wiederhergestellt, aber E-Mails, die während des Unterdrückungszeitraums gesendet wurden, werden nicht in die Warteschlange gestellt.

## [!UICONTROL Email Suppression]

![E-Mail-](./assets/email-suppression.png)<!-- zoom -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enable Email Suppression] | Shop-Ansicht | Ein-/Ausschalter für die Funktion. Wenn auf `No` (Standard) gesetzt, wird jede zweite Einstellung auf dieser Seite ignoriert und alle E-Mails werden normal gesendet. |
| [!UICONTROL Disabled Functional Areas] | Shop-Ansicht | Wählen Sie eine oder mehrere Geschäftskategorien aus, deren E-Mails unterdrückt werden. Unter [Geschäftskategorien](#business-categories) finden Sie Informationen zu den einzelnen Kategorien. |
| [!UICONTROL Disabled Template IDs] | Shop-Ansicht | Optionale kommagetrennte Liste spezifischer E-Mail-Vorlagen, die unabhängig von der Kategorie einzeln unterdrückt werden sollen. Verwenden Sie den Vorlagen-Code (z. B. `customer_password_forgot_email_template`) oder die numerische Vorlagen-ID für eine benutzerdefinierte Vorlage, die Sie in der Admin Console erstellt haben. |

{style="table-layout:auto"}

### Geschäftskategorien {#business-categories}

| Kategorie | Typische E-Mails enthalten |
|--- |--- |
| Kundenkonto | Kontoerstellung, Kennwortzurücksetzung, Änderungen der Kontoinformationen. |
| Order Management | Auftragsbestätigung, Rechnung, Versand, Gutschrift, Auftragsstornierung. |
| Rückgabe (RMA) | Benachrichtigungen zur Rücksendung von Waren. |
| Checkout und Zahlung | Checkout- und Pay-by-Link-bezogene E-Mails. |
| Marketing | Newsletter, Produktbenachrichtigungen, Freigabe von Wunschzetteln, E-Mail an Freunde, Erinnerungen, Einladungen, Geschenkregistrierung. |
| Gutschriften und Belohnungen speichern | Geschenkgutscheine, Belohnungspunkte, Kreditkontoänderungen speichern. |
| B2B | Benachrichtigungen zu Unternehmen, verhandelbaren Angeboten und Bestellungen. |
| Systembenachrichtigungen | Operative Benachrichtigungen wie geplante Import-, Export- und Kontaktformular-E-Mails. |

{style="table-layout:auto"}
