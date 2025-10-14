---
title: Beschaffungstypen für Händler
description: Erfahren Sie mehr über die beiden Beschaffungstypen auf der Grundlage der Anzahl der Standorte oder Quellen in Ihrem Unternehmen.
exl-id: ec928929-5826-4504-9fd0-84256b37cb39
feature: Inventory, Products
source-git-commit: 023716935a6657b0dc2317876debe608e65bf010
workflow-type: tm+mt
source-wordcount: '470'
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

- Konfigurieren Sie [globale Einstellungen und &#x200B;](configuration.md)) nach Bedarf für das Inventar Ihres Stores.

- Aktualisieren Sie [Standard-Source](sources-manage.md) mit Informationen zu Ihrem einzelnen Inventarspeicherort. Das Erstellen zusätzlicher Quellen ist nicht erforderlich.

- Aktualisieren Sie den [Standardbestand](stocks-manage.md). Stellen Sie sicher, dass alle Ihre Websites als Vertriebskanäle ausgewählt sind. Beim Hinzufügen neuer Websites fügt [!DNL Commerce] diese automatisch zum Standardbestand hinzu. Das Erstellen zusätzlicher Lager ist nicht erforderlich.

>[!NOTE]
>
>Wenn Ihr Unternehmen expandiert, fügen Sie zusätzliche Quellen und Lager hinzu und aktualisieren Sie Ihre [!DNL Inventory Management]-Konfiguration, um ein Händler mit mehreren Quellen zu werden. Siehe [Erweitern und Restrukturieren &#x200B;](expand-restructure.md) Inventars) für alle Details.

## Händler mit mehreren Quellen

Händler, die mehrere Bezugsquellen haben, verfügen über eine Website oder eine Implementierung an mehreren Standorten und verwalten Lagerbestände und führen Bestellungen an mehreren Standorten aus.

Sie haben beispielsweise eine Multi-Site-Implementierung mit Websites für die USA, Deutschland, Frankreich und Brasilien. Ihr Unternehmen umfasst mehrere Lager und Geschäfte in diesen Ländern und Drop-Shipper-Services, die alle Lager verwalten und Bestellungen erfüllen. Diese Standorte und Websites werden zu Quellen und Lagern in [!DNL Commerce]. Sie können einen Bestand für Amerika und einen anderen für Europa erstellen und Websites und Quellen basierend auf Gebietsschemata und Standorten zuweisen. Kunden, die jede Website kaufen, haben nur Zugriff auf verkaufbare Bestände aus den zugewiesenen Quellen.

Erste Schritte:

- Konfigurieren Sie nach Bedarf globale Einstellungen für das Inventar Ihres Stores.

- Fügen Sie [benutzerdefinierte Quellen](sources-add.md) für Ihre Lagerstandorte hinzu: Lager, Geschäfte, Verteilzentren und Direktlieferanten.

- Fügen Sie [benutzerdefinierte Lager](stocks-add.md) für jede Region hinzu, um Ihre Websites mit mehreren Quellen zu mappen. Sortieren Sie die Quellen in jedem Lager nach Priorität des Standorts neu, hilfreich bei der Erfüllung Ihrer Bestellungen.

- Weisen Sie den Produkten Quellen zu und fügen Sie Mengen pro Standort hinzu.

- Schließen Sie alle weiteren Konfigurationen pro Produkt für Mengenschwellen, Auftragsrückstände usw. ab.
