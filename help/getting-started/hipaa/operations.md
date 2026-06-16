---
title: Vorgänge
description: Richtlinien für die Migration zu einem HIPAA-fähigen Angebot und für die Verwendung der sekundären Staging-Umgebung zur Fehlerbehebung.
exl-id: 058b43de-1cee-4557-b2e3-87ee7422bf9b
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/de/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
TQID: https://experienceleague.adobe.com/w3CGUMXmuXy8006HmWG0K-q3ntjbHFAaC61O6t7S4Ao
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 581
ht-degree: 0%

---

# Vorgänge

{{ee-feature}}

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
