---
title: Was ist der Administrator?
description: Erfahren Sie mehr über den [!DNL Commerce] Admin, den Ort, an dem Händler Produkte und Promotions einrichten, Bestellungen verwalten und andere administrative Aufgaben ausführen.
exl-id: 065cf14f-80e7-4695-8922-c761a2191d72
TQID: https://experienceleague.adobe.com/A0DuYohA907-EHXQ6fyy2Sz83Y6cFZ7PDY5SmtBa14Y
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
    internal-label: Accessibility
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: eec5be4541c143c34dd75cda1903990ac4b74f8c
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 0%
---
# Was ist der Administrator?

Ihr Store _Admin_ ist das passwortgeschützte Backoffice, in dem Sie als Händler Produkte und Werbeaktionen einrichten, Bestellungen verwalten und andere administrative Aufgaben ausführen. Alle grundlegenden Konfigurationsaufgaben und Speicherverwaltungsvorgänge werden über den _Admin_ ausgeführt.

{{$include /help/_includes/admin-unified-experience-note.md}}

Für zusätzliche Sicherheit ist die _Admin_-Anmeldung durch [Zwei-Faktor-Authentifizierung](../systems/security-two-factor-authentication.md) geschützt und kann so konfiguriert werden, dass ein [CAPTCHA) &#x200B;](../systems/security-captcha.md). Weitere Informationen finden Sie unter &quot;[&#x200B; von Admin Security](../systems/security-admin.md).

![Admin-Seitenleiste und -Dashboard](./assets/admin-dashboard.png){width="700" zoomable="yes"}

Ihre [&#x200B; Anmeldedaten &#x200B;](admin-signin.md) während der Installation von Adobe Commerce oder Magento Open Source eingerichtet. Wenn Sie Ihr Kennwort vergessen haben, kann ein temporäres Kennwort an die mit dem Konto verknüpfte E-Mail-Adresse gesendet werden. Um die Sicherheit zu erhöhen, konfigurieren Sie Ihren Store so, dass ein Benutzername und ein starkes Kennwort unter Berücksichtigung der Groß-/Kleinschreibung erforderlich sind.

Zusätzlich zum standardmäßigen Admin-Benutzerkonto kann Ihr Unternehmen so viele [zusätzliche Konten“ erstellen, &#x200B;](../systems/permissions-users-all.md) Sie für die Verwaltung des Stores und der Support-Kundenkonten benötigen. Jedes Konto kann basierend auf dem &quot;_wissen“ mit einer bestimmten [Rolle](../systems/permissions-user-roles.md) und Zugriffsebene_ werden. Die E-Mail-Adresse, die mit jedem Admin-Benutzerkonto verknüpft ist, muss eindeutig sein.

{{ims-admin-note}}

## Nutzungsdatenerfassung

Wenn Sie sich zum ersten Mal bei _Admin_ anmelden, werden Sie aufgefordert, Adobe die Berechtigung zum Erfassen von Nutzungsdaten für alle Admin-Benutzer zu erteilen. Durch die Ermöglichung der Datenerfassung durch Administratoren können Sie Adobe bei der Verbesserung der Nutzung von Adobe Commerce Admin und zugehörigen Produkten und Services unterstützen.

![Datenerfassung der Admin-Nutzung zulassen](./assets/admin-usage-data.png){width="600"}

Einzelne Benutzende werden in den Nutzungsdaten nicht identifiziert. Ihre Datenerfassungseinstellung kann jederzeit über die Konfiguration [Admin Usage“ &#x200B;](../configuration-reference/advanced/admin.md#admin-usage) werden.

Für Adobe Commerce ermöglicht die Datenerfassung auch _Produktinterne Anleitung_ die dem Administrator interaktive Inhalte __. Es bietet Hilfe, QuickInfos, Anleitungen zu schrittweisen Anleitungen, Onboarding-Informationen, Ankündigungen zu Funktionen und mehr.
