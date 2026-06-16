---
title: Einführung in Inventory management
description: Erfahren Sie, wie Sie  [!DNL Inventory Management] -Funktionen verwenden können, um Lagerbestände an mehreren Orten zu verwalten, sodass  [!DNL Commerce]  Ladengeschäft den physischen Bestand genau widerspiegelt.
exl-id: 6a7dd27e-248f-4c40-b2db-0d70529422a1
TQID: https://experienceleague.adobe.com/7v-G-DZEki7y-4HSmq-rJxsmu6vih26jRYYCRRUF-XY
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 364
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
