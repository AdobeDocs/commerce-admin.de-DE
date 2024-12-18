---
title: Einrichten der AEM Assets-Integration
description: Erfahren Sie mehr über die Anforderungen und Schritte zum Einrichten der Integration zwischen Adobe Commerce und AEM Assets as a Cloud Service.
feature: CMS, Media, Configuration, Integration
exl-id: 75cf72ed-0110-4aed-b44a-193ad4dae202
source-git-commit: 824d55a3bc6c43d2feec549add6dfc8288bc4e97
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---

# Einrichten der AEM Assets-Integration

Aktivieren Sie erweiterte Asset-Management-Funktionen, indem Sie Ihre AEM Assets-Umgebung einrichten und die AEM Assets-Integration für Commerce installieren und konfigurieren.

Wenn die Integration aktiv ist, können Admins Experience Manager Assets as a Cloud Service als zentrale Datenquelle für die Asset-Erstellung und -Verwaltung und als zentrales Digital Asset Management-Tool (DAM) zum Erstellen, Verwalten, Organisieren und Verteilen von Assets für Commerce-Projekte verwenden.

## Anforderungen

- Adobe Commerce 2.4.5+
   - PHP 8.1, 8.2, 8.3
   - Komponist: 2.x
- Adobe Experience Manager ist mit [Adobe Experience Manager Assets as a Cloud Service bereitgestellt](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/assets/overview)
- Der Adobe Commerce-Benutzer, der die Integration konfiguriert, muss Zugriff auf die [IMS-Organisation](https://experienceleague.adobe.com/en/docs/core-services/interface/administration/organizations#concept_EA8AEE5B02CF46ACBDAD6A8508646255) haben, in der das AEM Assets-Projekt bereitgestellt wird.

## Einrichten der Integration

>[!BEGINSHADEBOX]

**Voraussetzungen**

Das Einrichten der AEM Assets-Integration erfordert administrativen Zugriff, um die Anwendungs- und Umgebungskonfiguration anzupassen.

- Administrativer Zugriff auf das Cloud Manager-Programm, in dem die AEM Assets as a Cloud Service-Umgebungen bereitgestellt werden.
- Administratorzugriff auf die Adobe Commerce-Umgebung und Möglichkeit, die für die Authentifizierung erforderlichen API-Schlüssel abzurufen oder zu generieren.

>[!ENDSHADEBOX]

Die Aktivierung der Commerce-Integration mit Experience Manager Assets ist ein dreistufiger Prozess:

1. [Konfigurieren Sie Ihr Experience Manager Assets-Projekt, um Commerce-Assets zu ](aem-assets-configure-aem.md).

1. [Installieren Sie die Experience Manager Assets-Integrationserweiterung und konfigurieren Sie Adobe Commerce](aem-assets-configure-aem.md).

1. [Asset-Synchronisierung aktivieren](aem-assets-setup-synchronization.md).
