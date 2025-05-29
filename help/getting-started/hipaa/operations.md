---
title: Vorgänge
description: Richtlinien für die Migration zu einem HIPAA-fähigen Angebot und für die Verwendung der sekundären Staging-Umgebung zur Fehlerbehebung.
exl-id: 058b43de-1cee-4557-b2e3-87ee7422bf9b
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
source-git-commit: 77e7eb00e9f8d5af6361059c287707993180c4c4
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 0%

---

# Vorgänge

Verwenden Sie diese Richtlinien, um mehr über die Migration zum HIPAA-fähigen Angebot für Adobe Commerce und die Verwendung der `staging_for_support` Umgebung zur Fehlerbehebung zu erfahren.

## Migration

Kunden, die von einem Commerce-Angebot ohne HIPAA zu einem HIPAA-fähigen Angebot migrieren, müssen die folgenden Richtlinien einhalten:

1. **Löschen vorhandener Datenräume**: Vor der Migration müssen alle vorhandenen Datenräume gelöscht werden, um zu verhindern, dass vertrauliche und nicht vertrauliche Daten in der Adobe Commerce SaaS-Ebene miteinander vermischt werden. Erstellen Sie ein Support-Ticket, um Ihre Datenräume zu löschen.
1. **Neue Umgebung konfigurieren**: Der [Commerce Services-Connector](https://experienceleague.adobe.com/en/docs/commerce/user-guides/integration-services/saas) der in der neuen HIPAA-Commerce-Instanz eingerichtet ist, sollte erst konfiguriert werden, nachdem die Datenräume gelöscht wurden. Die neue HIPAA-SaaS-Umgebung sollte erst verwendet werden, nachdem die alten Datenräume gelöscht wurden. Durch das Setup des Commerce Services Connectors wird die Erstellung neuer SaaS-Datenräume automatisch Trigger.
1. **Migrationsstrategie**: Das Löschen der SaaS-Datenräume ist ein irreversibler Prozess und löscht alle Ihre Katalogdaten und zugehörigen Konfigurationen. Wenn Sie alte Daten oder Konfigurationen weiterleiten möchten, müssen Sie über eine Migrationsstrategie verfügen. Diese Strategie liegt in der Verantwortung des Händlers. Ein Support-Ticket zum Löschen der vorhandenen Datenräume sollte erst erstellt werden, nachdem (falls zutreffend) eine Sicherungskopie der Migrationsdaten erstellt wurde.

>[!NOTE]
>Um vorhandene Datenräume zu löschen, müssen Kunden ein Adobe Commerce-Support-Ticket mit dem Titel „HIPAA-Migration: Löschen von SaaS-Datenräumen“ erstellen, ihre `MAGEID` angeben und die SaaS-Projekt-IDs angeben, die gelöscht werden müssen.

## Fehlerbehebung mit Adobe Commerce Support

Das Angebot &quot;Adobe Commerce HIPAA-ready“ enthält eine zusätzliche `staging_for_support`, die vom Adobe Commerce-Supportteam zur Fehlerbehebung verwendet werden kann.

Kunden müssen sicherstellen, dass `staging_for_support` Umgebung:

- Enthält keine sensiblen Daten wie etwa geschützte Gesundheitsinformationen (Protected Health Information, PHI).
- Darf nicht für Produktionstätigkeiten verwendet werden.
- Darf nicht anders benannt sein als `staging_for_support`, um Verwirrung zu vermeiden.
- wird sowohl mit Code als auch mit der Konfiguration aus der Produktionsumgebung auf dem neuesten Stand gehalten, um sicherzustellen, dass die Fehlerbehebung in einer Umgebung durchgeführt wird, die der Produktion möglichst nahekommt.

## Commerce Services

- **Nicht HIPAA-fähige Commerce-Services** - Kunden dürfen Adobe Commerce-Services wie Live Search, Product Recommendations, Zahlungs-Services, Vertriebskanäle oder Commerce Intelligence nicht verwenden, da sie nicht HIPAA-fähig sind. Kunden sollten nur [HIPAA-fähige Services](overview.md) verwenden.

- **Datenverbindung** - Nur der Back-Office-Collector innerhalb der [Datenverbindung](https://experienceleague.adobe.com/en/docs/commerce/data-connection/overview)-Erweiterung ist HIPAA-fähig. Kunden sollten keine PHI an Nicht-HIPAA-fähige Datenverbindungsdienste senden, z. B. Storefront-Ereignisse und Audience Activation. Kunden müssen sicherstellen, dass die Storefront-Datenerfassung deaktiviert ist.

- **Catalog Service** - Standardmäßig verarbeitet [Catalog Service](https://experienceleague.adobe.com/en/docs/commerce/catalog-service/overview) PHI nicht, sodass er außerhalb des Bereichs der HIPAA-Kompatibilitätsprüfung und -Compliance liegt. Die Kunden sind dafür verantwortlich, dass sie diesen Service auf der Grundlage ihrer eigenen Bewertung von Anwendungsfällen und in Absprache mit dem Rechtsbeistand nutzen. Kunden sollten auch nicht den Katalog-Service über den Federated Service verwenden, um das Risiko der Weitergabe von PHI an nicht HIPAA-fähige Services zu vermeiden.

- **SaaS-**: Der [SaaS-Datenexport](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/overview)-Service sollte so konfiguriert werden, dass nur Daten für HIPAA-fähige Komponenten in Adobe Commerce gesendet werden.
