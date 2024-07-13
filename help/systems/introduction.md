---
title: Einführung in Administratorsysteme
description: Erfahren Sie mehr über die Systemwerkzeuge und -funktionen, die der Administrator des Stores verwenden kann, um die Sites, Daten, Integrationen und Admin-Benutzer effektiv zu verwalten.
exl-id: 52792a89-8f6f-4230-9a04-e193b3943410
source-git-commit: 46564240e7f76cf2a691c209b36d530763ba4f01
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 0%

---

# Einführung in Administratorsysteme

Der Store-Administrator ist das sichere Backoffice, in dem Händler Produkte und Promotions einrichten, Bestellungen verwalten und andere administrative Aufgaben erledigen. Alle grundlegenden Konfigurationsaufgaben und Speicherverwaltungsvorgänge werden vom Administrator ausgeführt. Es gibt auch Funktionen, die Unterstützung für mehrere Store-Funktionen bieten, die Administratoren für ihre Organisationen verwalten können.

## Variablen und Kundenkommunikation

Variablen sind Informationen, die einmalig erstellt und an mehreren Stellen verwendet werden können. Ihr Store enthält viele vordefinierte Variablen, die einfach verwendet werden können, um die Vorlagen [E-Mail](email-templates.md) und [Newsletter](../merchandising-promotions/newsletter-template.md) sowie andere Typen von [Inhalt](../content-design/introduction.md#content) zu personalisieren. Sie können auch benutzerdefinierte Variablen erstellen, um Informationen zu integrieren, die Ihren Anforderungen entsprechen.

- [Vordefinierte Variablen](variables-predefined.md)
- [Benutzerdefinierte Variablen](variables-custom.md)

Eine der Aufgaben, die vor dem Start Ihres Stores ausgeführt werden müssen, besteht darin, die E-Mail-Vorlagen zu überprüfen, die für alle von Ihrem Store gesendeten Nachrichten verwendet werden, um sicherzustellen, dass sie Ihre Marke widerspiegeln. Dazu gehören das Anpassen von E-Mail- und [Newsletter-Vorlagen](../merchandising-promotions/newsletter-template.md) sowie von PDF-Rechnungen und Packsvorlagen. Dazu gehört auch die Personalisierung des Inhalts mit Variablen und [Markup-Tags](markup-tags.md).

## Betriebsmanagement

Der Administrator unterstützt außerdem verschiedene Aufgaben, mit denen Systemadministratoren die Admin-Benutzer in ihrem Unternehmen verwalten und den Store betreiben können. Dazu gehören die folgenden Tools:

- **Admin-Benutzerkonten und -berechtigungen** - Verwalten von Admin [Benutzerkonten](permissions-users-all.md) sowie der zugehörigen [Rollen und Berechtigungen](permissions-user-roles.md), die ihren Zugriff auf Sites und Funktionsbereiche in der Admin-Konsole steuern.
- **Admin-Sitzungen und Website-Beschränkungen** - Überprüfen Sie die Best Practices für die Sicherheit](security.md) und erfahren Sie, wie Sie Admin-Sitzungen und -Anmeldedaten verwalten, CAPTCHA implementieren und Website-Einschränkungen verwalten.[
- **Systemtools** - Führen Sie Routinevorgänge zur Verwaltung von [Index](index-management.md) und [Cache](cache-management.md) durch, führen Sie [Sichern](backups.md) Sie das System aus, verwalten Sie [geplante Vorgänge](data-scheduled-import-export.md) und verwenden Sie eine Reihe von [Entwicklertools](developer-tools.md).
- **Datenübertragung** - Verwenden Sie die Tools zur [Datenübertragung](data-transfer.md), um Daten zu importieren und zu exportieren sowie Produkt-, Preis-, Kunden- und Steuersatzdaten zu verwalten.
- **Integrationen** - Legen Sie den Speicherort der OAuth-Anmeldeinformationen fest und geben Sie die Umleitungs-URL für [Drittanbieter-Integrationen](integrations.md) an und identifizieren Sie die verfügbaren API-Ressourcen.
- **Aktionsprotokolle** - ![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Greifen Sie auf die Datensätze ([Aktionsprotokolle](action-log.md)) für Änderungen zu, die von Admin-Benutzern vorgenommen wurden, die in Ihrem Store arbeiten.
- **Support-Tools** - ![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Die Support-Tools ([Datenerfassung](support.md#data-collector) und [Systemberichte](support.md#access-system-reports)) dienen der Identifizierung bekannter Probleme in Ihrem System. Sie können während der Entwicklungs- und Optimierungsprozesse als Ressource und als Diagnosetool verwendet werden, um unserem Supportteam bei der Identifizierung und Lösung von Problemen zu helfen.
