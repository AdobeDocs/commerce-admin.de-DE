---
title: Einrichten der AEM Assets-Integration
description: Erfahren Sie mehr über die Anforderungen und Schritte zum Einrichten der Integration zwischen Adobe Commerce und AEM Assets as a Cloud Service.
feature: CMS, Media, Configuration, Integration
source-git-commit: df21ea9a797a4f11d0104cf34134ced3bbabbdf4
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Einrichten der AEM Assets-Integration

Aktivieren Sie erweiterte Asset-Management-Funktionen, indem Sie Ihre AEM Assets-Umgebung einrichten und die AEM Assets-Integration für Commerce installieren und konfigurieren.

Wenn die Integration aktiv ist, können Administratoren Experience Manager Assets as a Cloud Service als zentrale &quot;Source of Truth&quot; für die Asset-Erstellung und -Verwaltung sowie als zentrales Digital Asset Management-Tool (DAM) verwenden, um Assets für Commerce-Projekte zu erstellen, zu verwalten, zu organisieren und zu verteilen.

## Voraussetzungen

- Adobe Commerce 2.4.5+
   - PHP 8.1, 8.2, 8.3
   - Verfasser: 2.x
- Adobe Experience Manager ist mit [Adobe Experience Manager Assets as a Cloud Service](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/assets/overview) bereitgestellt
- Der Adobe Commerce-Benutzer, der die Integration konfiguriert, muss Zugriff auf die [IMS-Organisation](https://experienceleague.adobe.com/en/docs/core-services/interface/administration/organizations#concept_EA8AEE5B02CF46ACBDAD6A8508646255) haben, in der das AEM Assets-Projekt bereitgestellt wurde.

## Integration einrichten

>[!BEGINSHADEBOX]

**Voraussetzungen**

Für das Einrichten der AEM Assets-Integration ist der Administratorzugriff erforderlich, um die Anwendungs- und Umgebungskonfiguration anzupassen.

- Administratorzugriff auf das Cloud Manager-Programm, in dem die AEM Assets as a Cloud Service-Umgebungen bereitgestellt werden.
- Administratorzugriff auf die Adobe Commerce-Umgebung und Möglichkeit, für die Authentifizierung erforderliche API-Schlüssel abzurufen oder zu generieren.

>[!ENDSHADEBOX]

Die Aktivierung der Commerce-Integration in Experience Manager Assets umfasst drei Schritte:

1. [Konfigurieren Sie Ihr Experience Manager Assets-Projekt für die Verwaltung von Commerce-Assets](aem-assets-configure-aem.md).

1. [Installieren Sie die Experience Manager Assets Integration-Erweiterung und konfigurieren Sie Adobe Commerce](aem-assets-configure-aem.md).

1. [Aktivieren Sie die Asset-Synchronisierung](aem-assets-setup-synchronization.md).
