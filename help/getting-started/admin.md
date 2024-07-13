---
title: Was ist der Administrator?
description: Erfahren Sie mehr über den  [!DNL Commerce] Admin, den Ort, an dem Händler Produkte und Promotions einrichten, Bestellungen verwalten und andere Verwaltungsaufgaben ausführen.
exl-id: 065cf14f-80e7-4695-8922-c761a2191d72
source-git-commit: b657db7e486fec591d5a6239d554376f00707e8c
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# Was ist der Administrator?

Ihr Store _Admin_ ist das passwortgeschützte Backoffice, in dem Sie als Händler Produkte und Promotions einrichten, Bestellungen verwalten und andere Verwaltungsaufgaben ausführen. Alle grundlegenden Konfigurationsaufgaben und Speicherverwaltungsvorgänge werden von _Admin_ ausgeführt.

Für zusätzliche Sicherheit ist die Anmeldung _Admin_ durch die Authentifizierung mit zwei Faktoren [ geschützt und kann so konfiguriert werden, dass eine [CAPTCHA](../systems/security-captcha.md) erforderlich ist. ](../systems/security-two-factor-authentication.md) Weitere Informationen finden Sie unter [Konfigurieren der Admin-Sicherheit](../systems/security-admin.md).

![Admin-Seitenleiste und Dashboard](./assets/admin-dashboard.png){width="700" zoomable="yes"}

Ihre ursprünglichen [Anmeldedaten für die Anmeldung](admin-signin.md) wurden während der Installation von Adobe Commerce oder Magento Open Source eingerichtet. Wenn Sie Ihr Passwort vergessen haben, kann ein temporäres Passwort an die E-Mail-Adresse gesendet werden, die dem Konto zugeordnet ist. Um die Sicherheit zu erhöhen, konfigurieren Sie Ihren Store so, dass ein Benutzername mit Unterscheidung zwischen Groß- und Kleinschreibung und ein sicheres Kennwort erforderlich ist.

Zusätzlich zum standardmäßigen Admin-Benutzerkonto kann Ihr Unternehmen so viele [zusätzliche Konten](../systems/permissions-users-all.md) erstellen, wie Sie zum Verwalten des Stores und zum Support von Kundenkonten benötigen. Jedes Konto kann mit einer bestimmten [Rolle](../systems/permissions-user-roles.md) und Zugriffsstufe verknüpft werden, basierend auf dem geschäftlichen _Muss wissen_. Die mit jedem Admin-Benutzerkonto verknüpfte E-Mail-Adresse muss eindeutig sein.

{{ims-admin-note}}

## Datenerfassung verwenden

Wenn Sie sich zum ersten Mal bei _Admin_ anmelden, werden Sie aufgefordert, der Adobe die Berechtigung zum Erfassen von Nutzungsdaten für alle Admin-Benutzer zu erteilen. Indem Sie die Datenerfassung durch Administratoren ermöglichen, helfen Sie Adobe bei der Verbesserung der Benutzerfreundlichkeit von Adobe Commerce Admin sowie damit verbundenen Produkten und Services.

![Zulassen der Datenerfassung durch Administratoren](./assets/admin-usage-data.png){width="600"}

Einzelne Benutzer werden in den Nutzungsdaten nicht identifiziert. Ihre Datenerfassungseinstellung kann jederzeit über die Konfiguration [Admin-Nutzung](../configuration-reference/advanced/admin.md#admin-usage) geändert werden.

Für Adobe Commerce ermöglicht die Ermöglichung der Datenerfassung auch die _In-Product Guidance_, die interaktive Inhalte an den _Admin_ bringen soll. Es bietet Hilfe, Tooltipps, schrittweise Anleitungen, Onboarding-Informationen, Funktionsankündigungen und mehr.
