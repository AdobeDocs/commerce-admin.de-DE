---
title: Einrichten der AEM Assets-Integration für Commerce
description: Erfahren Sie, wie Sie Ihre Experience Manager Assets-Umgebung einrichten und konfigurieren, um Commerce-Assets für Ihren Store zu verwalten.
feature: CMS, Media, Configuration
exl-id: 699f517e-1545-4c22-aa8d-9c8d60d352af
source-git-commit: 934473c5124002b3b0b1bee2da47afff468406dc
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 0%

---

# Einrichten der AEM Assets-Integration für Commerce

Das Einrichten der Adobe Experience Manager Assets-Integration für Commerce erfordert administrativen Zugriff, um die Anwendungs- und Umgebungskonfiguration anzupassen.

- Administrativer Zugriff auf das Cloud Manager-Programm, in dem die AEM Assets as a Cloud Service-Umgebungen bereitgestellt werden.

- Administratorzugriff auf die Adobe Commerce-Umgebung und die Möglichkeit, die für die Authentifizierung erforderlichen API-Schlüssel abzurufen oder zu generieren.

## Voraussetzungen für die Verwendung der Integration

Um diese Integration nutzen zu können, müssen Unternehmen die folgenden Anforderungen erfüllen:

- Aktive Lizenzen für Adobe Commerce, Adobe Experience Manager Assets und [AEM Dynamic Media](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/assets/dynamic/administering-dynamic-media).

- Adobe Commerce 2.4.5+

   - PHP 8.1, 8.2, 8.3
   - Komponist: 2.x

- Adobe Experience Manager ist mit [Adobe Experience Manager Assets as a Cloud Service bereitgestellt](https://experienceleague.adobe.com/de/docs/experience-manager-cloud-service/content/assets/overview)

- Der Adobe Commerce-Benutzer, der die Integration konfiguriert, muss Zugriff auf die [IMS-Organisation](https://experienceleague.adobe.com/en/docs/core-services/interface/administration/organizations#concept_EA8AEE5B02CF46ACBDAD6A8508646255) haben, in der das AEM Assets-Projekt bereitgestellt wird.

## Die wichtigsten Vorteile

- **Keine zusätzlichen Kosten** - Diese Integration wird für Händler, die die Lizenzanforderungen erfüllen, kostenlos bereitgestellt.

- **Offizielle Adobe-Lösung** - Von Adobe entwickelt, gepflegt und vollständig unterstützt, um Stabilität und Ausrichtung an zukünftigen Plattformverbesserungen sicherzustellen.

- **Adobe Managed Support Model** - Adobe übernimmt die Unterstützung und Fehlerbehebung und bietet Ihnen ein sicheres Gefühl und optimierte Problemlösungen.

## Nächste Schritte

Die Aktivierung der Commerce-Integration mit Experience Manager Assets ist ein dreistufiger Prozess:

1. [Konfigurieren Sie Ihr Adobe Experience Manager Assets-Projekt, um Adobe Commerce-Assets zu verwalten](aem-assets-configure-aem.md).

1. [Installieren Sie die Erweiterung Adobe Experience Manager Assets Integration for Commerce und konfigurieren Sie Adobe Commerce](aem-assets-configure-aem.md).

1. [Asset-Synchronisierung aktivieren](aem-assets-setup-synchronization.md).
