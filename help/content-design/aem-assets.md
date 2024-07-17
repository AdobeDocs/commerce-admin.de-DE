---
title: Experience Manager Assets-Integration für Commerce
description: Erfahren Sie, wie Sie Experience Manager Assets in Ihre [!DNL Commerce] Instanz integrieren können, um auf unzählige Medien-Assets zuzugreifen, die in Ihrem Store verwendet werden können.
feature: CMS, Media, Configuration, Integration
source-git-commit: d91ba86b77ef91e849d1737628b575f2309376b8
workflow-type: tm+mt
source-wordcount: '432'
ht-degree: 0%

---

# Experience Manager Assets-Integration für Commerce

{{$include /help/_includes/aem-assets-integration-beta-note.md}}

Die Integration zwischen Commerce und Adobe Experience Manager (AEM) Assets kombiniert die robusten Funktionen von AEM as a Digital Asset Management (DAM) mit Adobe Commerce, um E-Commerce-Erlebnisse zu verbessern. Diese Integration nutzt AEM leistungsstarken Asset-Management-Funktionen, um eine nahtlose, skalierbare und effiziente Methode zur Verwaltung und Bereitstellung von Assets über Commerce-Storefronts hinweg bereitzustellen.

**Schlüsselfunktionen**

- **Zentralisierte Asset-Verwaltung**

   - **AEM Assets als Single Source of Truth**-AEM Assets dient als zentrales Repository für alle digitalen Assets und stellt sicher, dass alle E-Commerce-Plattformen Zugriff auf marken- und genehmigte Assets haben.

   - **Massen-Asset-Management** - Unternehmen können große Mengen von Assets effizient verwalten, dank AEM umfassenden Asset-Management-Funktionen. Dadurch können Marketing-Experten und Merchandiser große Mengen von Bildern für neue Produktlinien effizient zuordnen.

- **Personalisierte Commerce-Erlebnisse** - Mit GenAI-Diensten in AEM können Unternehmen Millionen von Produktvarianten für personalisierte E-Commerce-Erlebnisse generieren. Marketingexperten und Merchandiser können diese Bilder verwenden, um dynamische Storefronts für Produktstarts und saisonale Kampagnen zu erstellen, die Interaktion zu verbessern und Konversionsraten zu steigern.

- **Automatische Asset-Übereinstimmung** - Die Integration umfasst einen Regel-Engine-Dienst, der Assets in AEM auf der Grundlage der SKU oder anderer Schlüsselattribute automatisch mit Produkten in Adobe Commerce abgleicht. Der Dienst stellt sicher, dass die neuesten Produkt-Assets und -Varianten immer in E-Commerce-Storefronts verfügbar sind. Außerdem wird der manuelle Aufwand für die Verwaltung von Assets reduziert und Zeit für strategischere Aktivitäten freigesetzt.

- **Optimierte Prozesse**
   - **Aktivieren und konfigurieren Sie die Integration über Commerce Admin** -Administratoren und Entwickler können die Integration über Adobe Commerce mit vertrauten Tools und Prozessen installieren und konfigurieren.
   - **Dynamische Updates** - Halten Sie Produktbilder mit den neuesten Änderungen im Asset-Management-System auf dem neuesten Stand. Diese automatisierten Aktualisierungen stellen sicher, dass Commerce-Storefronts immer über die aktuellsten Produktinformationen verfügen.
   - **Effizientes Katalogmanagement** - Vereinfacht die Wartung des Produktkatalogs durch Automatisierung der Asset-Bereinigung und -Aktualisierung.

## Integrieren von Commerce und Experience Manager Assets

>[!BEGINSHADEBOX]

**Voraussetzungen**

- Adobe Commerce muss mit der [Commerce Admin-Integration mit Adobe ID](/help/getting-started/adobe-ims-config.md) mit einer zugewiesenen Organisations-ID konfiguriert werden.
- Experience Manager Assets muss derselben Organisations-ID als Produkt zugewiesen werden.
- Der Benutzer, der die Integration konfiguriert, muss über ein Konto in derselben Organisation mit Administratorrechten verfügen, um auf Adobe Commerce und Experience Manager Assets zugreifen zu können.

>[!ENDSHADEBOX]

Aktivierung der Commerce-Integration in Experience Manager Assets durch Ausführen der folgenden Aufgaben:

1. [Konfigurieren Ihres Experience Manager Assets-Projekts zum Verwalten von Commerce-Assets](aem-assets-configure-aem.md)

1. [Installieren der Experience Manager Assets Integration-Erweiterung und Konfigurieren von Adobe Commerce](aem-assets-configure-commerce.md)

1. [Aktivieren der Asset-Synchronisierung](aem-assets-setup-synchronization.md)
