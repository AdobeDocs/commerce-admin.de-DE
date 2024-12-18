---
title: Einführung in Inventory management
description: Erfahren Sie, wie Sie  [!DNL Inventory Management] -Funktionen verwenden können, um Lagerbestände an mehreren Orten zu verwalten, sodass  [!DNL Commerce]  Ladengeschäft den physischen Bestand genau widerspiegelt.
exl-id: 6a7dd27e-248f-4c40-b2db-0d70529422a1
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 0%

---

# Einführung in Inventory management

[!DNL Inventory Management] für [!DNL Commerce] stellt Ihnen die Tools zur Verwaltung Ihres Produktbestands zur Verfügung. Händler mit einem einzigen Shop für mehrere Lager, Geschäfte, Abholorte, Drop-Versender und mehr können diese Funktionen verwenden, um Mengen für den Verkauf zu verwalten und Sendungen zu bearbeiten, um Bestellungen abzuschließen. Sie können Ihre Lagermengen verfolgen, genaue verkaufbare Lagerbestände für Kunden für alle Ihre Websites bereitstellen und gemäß Empfehlungen versenden, die auf Entfernung oder Priorität basieren. Sie können Ihre bevorzugten Produktkonfigurationen auch global (für alle Geschäfte und Produkte), pro Quelle und pro Produkt konfigurieren. Diese Funktionen wachsen mit Ihrem Unternehmen und ermöglichen es Ihnen, von einem einzigen Lager oder einem komplexen Versandnetzwerk mit einigen zusätzlichen Einstellungen zu arbeiten.

Zu den [!DNL Inventory Management] Funktionen gehören:

- Verschiedene Konfigurationen für Händler, deren Inventar aus einer einzigen Quelle und aus mehreren Quellen stammt
- Lagerbestände zur Ermittlung verfügbarer aggregierter Mengen aus zugewiesenen Quellen
- Gleichzeitiger Auscheckschutz
- Algorithmen zum Abgleich von Sendungen

>[!NOTE]
>
>Diese Funktionen wurden im Rahmen des Projekts [Inventory management](https://github.com/magento/inventory) (ehemals MSI) über das Community Engineering-Programm entwickelt.<br/>
>
>Das [!DNL Inventory Management] wird mit Magento Open Source und Adobe Commerce installiert, wobei alle Funktionen standardmäßig aktiviert sind. Informationen zu den in den Modulversionen enthaltenen Änderungen finden Sie in den [Versionshinweisen](release-notes.md).

## Grundlegende Begriffe

Es ist wichtig, dass Sie die folgenden Begriffe bei der Arbeit mit [!DNL Inventory Management] verstehen:

[!UICONTROL **Quellen**] stellen physische Standorte dar, an denen verfügbare Produkte gespeichert und versendet werden. Zu diesen Standorten können Lagerhäuser, stationäre Läden, Vertriebszentren und Verlader gehören. (Ein beliebiger Speicherort kann als Quelle für virtuelle Produkte angegeben werden.)

[!UICONTROL **Lager**] Ordnen Sie einen Verkaufskanal (derzeit auf Websites beschränkt) Quellstandorten und verfügbarem Inventar zu. Ein Lager kann mehreren Vertriebskanälen zugeordnet werden, ein Vertriebskanal kann jedoch nur einem Lager zugewiesen werden.

[!UICONTROL **Aggregierte Verkaufsmenge**] ist der gesamte virtuelle Bestand, der über einen Verkaufskanal verkauft werden kann. Der Betrag wird für alle einem Lager zugeordneten Quellen berechnet.

[!UICONTROL **Reservierungen**] Verfolgen Sie Abzüge von der verkaufsfähigen Menge, wenn Kunden Produkte zum Warenkorb hinzufügen und den Checkout abschließen. Wenn ein Auftrag ausgeliefert wird, werden die ausgelieferten Beträge durch die Reservierung verrechnet und von den jeweiligen Lagerbestandsmengen abgezogen.
