---
title: Einführung in Inventory management
description: Verwendung von [!DNL Inventory Management] Funktionen zur Verwaltung von Lagern an mehreren Standorten, damit Ihre [!DNL Commerce] den tatsächlichen Bestand genau widerspiegelt.
exl-id: 6a7dd27e-248f-4c40-b2db-0d70529422a1
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---

# Einführung in Inventory management

[!DNL Inventory Management] für [!DNL Commerce] bietet Ihnen die Tools zur Verwaltung Ihres Produktbestands. Händler mit einem einzigen Geschäft zu mehreren Lagern, Geschäften, Abholstandorten, Ablagelagern und mehr können diese Funktionen nutzen, um die Mengen für den Verkauf zu halten und Sendungen für komplette Bestellungen abzuwickeln. Sie können Ihre Lagerbestandsmengen nachverfolgen, Kunden für alle Ihre Websites genaue verkaufbare Lagerbestände zur Verfügung stellen und gemäß Empfehlungen auf der Grundlage der Entfernung oder Priorität versenden. Sie können Ihre bevorzugten Produktkonfigurationen auch global (für alle Stores und Produkte), pro Quelle und pro Produkt konfigurieren. Diese Funktionen wachsen mit Ihrem Unternehmen, sodass Sie von einem einzigen Warehouse oder einem komplexen Versandnetz mit einigen zusätzlichen Einstellungen aus arbeiten können.

[!DNL Inventory Management] Zu den Funktionen gehören:

- Verschiedene Konfigurationen für Händler, deren Inventar aus einer einzigen Quelle und aus mehreren Quellen stammt
- Bestände zur Verfolgung der verfügbaren aggregierten Mengen über zugewiesene Quellen
- Schutz beim gleichzeitigen Checkout
- Versandzuordnungsalgorithmen

>[!NOTE]
>
>Diese Funktionen wurden im Rahmen der [Inventory management](https://github.com/magento/inventory) (ehemals MSI) Projekt durch das Engineering-Programm der Community.<br/>
>
>Die [!DNL Inventory Management] -Modul wird mit Magento Open Source und Adobe Commerce installiert, wobei alle Funktionen standardmäßig aktiviert sind. Informationen zu den Änderungen, die in Modulversionen enthalten sind, finden Sie unter [Versionshinweise](release-notes.md).

## Grundlegende Terminologie

Es ist wichtig, die folgenden Begriffe bei der Arbeit mit [!DNL Inventory Management]:

[!UICONTROL **Quellen**] physische Orte darstellen, an denen verfügbare Produkte gelagert und befördert werden. Zu diesen Standorten zählen Lagerhäuser, Bausteine- und Mörtelgeschäfte, Vertriebszentren und Tropfenlieferanten. (Jeder Standort kann als Quelle für virtuelle Produkte bezeichnet werden.)

[!UICONTROL **Lagerbestände**] Ordnen Sie einen (derzeit auf Websites beschränkten) Vertriebskanal den Quellstandorten und dem lokalen Inventar zu. Ein Lager kann mehreren Absatzkanälen zugeordnet werden, aber ein Vertriebskanal kann nur einem Lager zugewiesen werden.

[!UICONTROL **Aggregierte Verkaufsmenge**] ist der gesamte virtuelle Bestand, der über einen Vertriebskanal verkauft werden kann. Der Betrag wird aus allen Quellen berechnet, die einem Bestand zugeordnet sind.

[!UICONTROL **Reservierungen**] Sie können Abzüge von der Verkaufsmenge verfolgen, wenn Kunden Produkte zum Warenkorb hinzufügen und den Kassengang abschließen. Wenn eine Bestellung ausgeliefert wird, werden die versandten Mengen durch die Reservierung von bestimmten Quellbestandsmengen abgezogen.
