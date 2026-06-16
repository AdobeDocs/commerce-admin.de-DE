---
title: Beschaffungstypen für Händler
description: Erfahren Sie mehr über die beiden Beschaffungstypen auf der Grundlage der Anzahl der Standorte oder Quellen in Ihrem Unternehmen.
exl-id: ec928929-5826-4504-9fd0-84256b37cb39
feature: Inventory, Products
TQID: https://experienceleague.adobe.com/-ABDMLnAibksuQGkdEM683g8JwcUSt2DQERC0WJnQiM
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 486
ht-degree: 0%

---

# Beschaffungstypen für Händler

[!DNL Commerce] unterstützt [!DNL Inventory Management] für alle Unternehmensgrößen, einschließlich eines einzelnen Stores mit einer Website zu einem internationalen Netzwerk von Websites, Stores, Lagern und Drop-Verladern. Alle Händler, die Adobe Commerce oder Magento Open Source verwenden, lassen sich je nach der Anzahl der Standorte oder Quellen in Ihrem Unternehmen in zwei Typen unterteilen.

- Händler aus einer Hand versenden Produkte von einem Ort aus. Sie werden als Händler/Händler mit einer einzigen Quelle betrachtet, bis Sie Ihrer Installation benutzerdefinierte Quellen und Lager hinzufügen.

- Händler, die mehrere Bezugsquellen haben, versenden Produkte von mehr als einem Standort, z. B. aus stationären Läden, Lagerhäusern, Verladern und Vertriebszentren. Nachdem Sie benutzerdefinierte Quellen pro Standort hinzugefügt haben, werden Sie automatisch ein Händler mit mehreren Quellen.

## Händler aus einer Hand

Händler aus einer Hand haben einen einzigen Standort, der den Lagerbestand verwaltet und Bestellungen ausführt. In der Regel haben Sie mehrere Websites (oder Vertriebskanäle), die Produkte aus demselben Katalog, Inventar und Standort verkaufen.

Sie haben beispielsweise eine Website oder eine Implementierung mit mehreren Websites, wobei Sites für die USA, Deutschland, Frankreich und Brasilien alle Produkte aus einem großen Lager abrufen. Diese zentrale Quelle verwaltet alle Lagermengen, Lieferungen und Rücksendungen, unabhängig davon, welcher Vertriebskanal die Bestellung erhält.

Erste Schritte:

- Konfigurieren Sie [globale Einstellungen und ](configuration.md)) nach Bedarf für das Inventar Ihres Stores.

- Aktualisieren Sie [Standard-Source](sources-manage.md) mit Informationen zu Ihrem einzelnen Inventarspeicherort. Das Erstellen zusätzlicher Quellen ist nicht erforderlich.

- Aktualisieren Sie den [Standardbestand](stocks-manage.md). Stellen Sie sicher, dass alle Ihre Websites als Vertriebskanäle ausgewählt sind. Beim Hinzufügen neuer Websites fügt [!DNL Commerce] diese automatisch zum Standardbestand hinzu. Das Erstellen zusätzlicher Lager ist nicht erforderlich.

>[!NOTE]
>
>Wenn Ihr Unternehmen expandiert, fügen Sie zusätzliche Quellen und Lager hinzu und aktualisieren Sie Ihre [!DNL Inventory Management]-Konfiguration, um ein Händler mit mehreren Quellen zu werden. Siehe [Erweitern und Restrukturieren ](expand-restructure.md) Inventars) für alle Details.

## Händler mit mehreren Quellen

Händler, die mehrere Bezugsquellen haben, verfügen über eine Website oder eine Implementierung an mehreren Standorten und verwalten Lagerbestände und führen Bestellungen an mehreren Standorten aus.

Sie haben beispielsweise eine Multi-Site-Implementierung mit Websites für die USA, Deutschland, Frankreich und Brasilien. Ihr Unternehmen umfasst mehrere Lager und Geschäfte in diesen Ländern und Drop-Shipper-Services, die alle Lager verwalten und Bestellungen erfüllen. Diese Standorte und Websites werden zu Quellen und Lagern in [!DNL Commerce]. Sie können einen Bestand für Amerika und einen anderen für Europa erstellen und Websites und Quellen basierend auf Gebietsschemata und Standorten zuweisen. Kunden, die jede Website kaufen, haben nur Zugriff auf verkaufbare Bestände aus den zugewiesenen Quellen.

Erste Schritte:

- Konfigurieren Sie nach Bedarf globale Einstellungen für das Inventar Ihres Stores.

- Fügen Sie [benutzerdefinierte Quellen](sources-add.md) für Ihre Lagerstandorte hinzu: Lager, Geschäfte, Verteilzentren und Direktlieferanten.

- Fügen Sie [benutzerdefinierte Lager](stocks-add.md) für jede Region hinzu, um Ihre Websites mit mehreren Quellen zu mappen. Sortieren Sie die Quellen in jedem Lager nach Priorität des Standorts neu, hilfreich bei der Erfüllung Ihrer Bestellungen.

- Weisen Sie den Produkten Quellen zu und fügen Sie Mengen pro Standort hinzu.

- Schließen Sie alle weiteren Konfigurationen pro Produkt für Mengenschwellen, Auftragsrückstände usw. ab.
