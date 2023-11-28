---
title: Beschaffungstypen für Händler
description: Erfahren Sie mehr über die beiden Beschaffungstypen basierend auf der Anzahl der Standorte oder Quellen in Ihrem Unternehmen.
exl-id: ec928929-5826-4504-9fd0-84256b37cb39
feature: Inventory, Products
source-git-commit: 023716935a6657b0dc2317876debe608e65bf010
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 0%

---

# Beschaffungstypen für Händler

[!DNL Commerce] unterstützt [!DNL Inventory Management] für alle Unternehmensgrößen, einschließlich eines einzigen Stores mit einer Website zu einem internationalen Netz von Websites, Geschäften, Lagern und Drop-Spediteuren. Alle Händler, die Adobe Commerce oder Magento Open Source verwenden, fallen je nach Anzahl der Standorte oder Quellen in Ihrem Unternehmen in zwei Typen.

- Einzelquellenhändler liefern Produkte von einem Ort aus. Sie werden als Einzelquellenhändler/-modus betrachtet, bis Sie mit dem Hinzufügen von benutzerdefinierten Quellen und Lagern zu Ihrer Installation beginnen.

- Multi-Source-Händler liefern Produkte aus mehreren Standorten, wie z.B. Ziegeleien, Lagerhäuser, Drop-Spediteure und Vertriebszentren. Nachdem Sie benutzerdefinierte Quellen pro Standort hinzugefügt haben, werden Sie automatisch zu einem Händler mit mehreren Quellen.

## Einzelquell-Händler

Einzelquellenhändler verfügen über einen einzigen Standort, an dem Lagerbestände verwaltet und Bestellungen ausgeführt werden. In der Regel verfügen Sie über mehrere Websites (oder Vertriebskanäle), die Produkte aus demselben Katalog, Bestand und Standort verkaufen.

Sie verfügen beispielsweise über eine Website oder eine Multi-Site-Implementierung mit Sites für die USA, Deutschland, Frankreich und Brasilien, die alle Produkte aus einem großen Lager beziehen. Diese einzige Quelle verwaltet alle Lagerbestandsmengen, Sendungen und Rückgaben, unabhängig davon, welcher Absatzkanal die Bestellung erhält.

Erste Schritte:

- Konfigurieren [globale und Produkteinstellungen](configuration.md) für den Lagerbestand Ihres Stores nach Bedarf.

- Aktualisieren Sie die [Standardquelle](sources-manage.md) mit Informationen für Ihren einzelnen Lagerort. Das Erstellen zusätzlicher Quellen ist nicht erforderlich.

- Aktualisieren Sie die [Standardbestand](stocks-manage.md). Stellen Sie sicher, dass alle Ihre Websites als Vertriebskanäle ausgewählt sind. Beim Hinzufügen neuer Websites [!DNL Commerce] fügt sie automatisch zum Standardbestand hinzu. Die Erstellung zusätzlicher Lager ist nicht erforderlich.

>[!NOTE]
>
>Wenn Ihr Unternehmen expandiert, fügen Sie zusätzliche Quellen und Lager hinzu und aktualisieren Sie Ihre [!DNL Inventory Management] -Konfiguration, um zu einem Multi-Source-Händler zu werden. Siehe [Inventar erweitern und umstrukturieren](expand-restructure.md) für alle Details.

## Händler mit mehreren Quellen

Multi-Source-Händler verfügen über eine Website oder eine Multi-Site-Implementierung und verwalten den On-Hand-Bestand und die Bestellungen über mehrere Standorte.

Sie haben beispielsweise eine Site-übergreifende Implementierung mit Websites für die USA, Deutschland, Frankreich und Brasilien. Ihr Geschäft umfasst mehrere Lagerhäuser und Geschäfte in diesen Ländern und Drop-Versanddienste, die alle Lagerbestände verwalten und Aufträge erfüllen. Diese Standorte und Websites werden zu Quellen und Lagern in [!DNL Commerce]. Sie können eine Lagerhaltung für Nord- und Südamerika und eine andere für Europa erstellen, indem Sie Websites und Quellen nach Gebietsschemata und Standorten zuweisen. Kunden, die auf jeder Website einkaufen, haben nur Zugriff auf Verkaufsbestände aus den zugewiesenen Quellen.

Erste Schritte:

- Konfigurieren Sie nach Bedarf globale Einstellungen für den Lagerbestand Ihres Stores.

- Hinzufügen [benutzerdefinierte Quellen](sources-add.md) für Ihre Lagerstandorte: Lagerhäuser, Geschäfte, Vertriebszentren und Spediteure.

- Hinzufügen [benutzerdefinierte Bestände](stocks-add.md) für jede Region, um Ihre Websites mehreren Quellen zuzuordnen. Ordnen Sie die Quellen in jedem Lager in Priorität des Standorts an, was bei der Erfüllung Ihrer Bestellungen hilfreich ist.

- Weisen Sie den Produkten Quellen zu, indem Sie Mengen pro Standort hinzufügen.

- Schließen Sie alle weiteren Konfigurationen pro Produkt für Mengenschwellen, Rückstände usw. ab.
