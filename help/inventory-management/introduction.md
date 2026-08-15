---
title: Einführung in [!DNL Inventory Management]
description: Erfahren Sie, wie Sie  [!DNL Inventory Management] for [!DNL Commerce] verwenden können, um Lagerbestände über Quellen und Lager hinweg zu verwalten, verkäufliche Mengen zu berechnen, Reservierungen zu verfolgen und die Auftragserfüllung zu unterstützen. Verwenden Sie den Administrator, um die Einstellungen zu konfigurieren und Berichte zu generieren, und die Befehlszeilenschnittstelle für Setup- und Hintergrundänderungen.
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
source-git-commit: 125a49f740639bce0ced8063074ca43d627c0eac
workflow-type: tm+mt
source-wordcount: 371
ht-degree: 0%

---

# Einführung in [!DNL Inventory Management]

[!DNL Inventory Management] für [!DNL Commerce] hilft Händlern bei der Verwaltung des Inventars auf einer oder mehreren Websites und physischen oder virtuellen Produktstandorten. Es bietet Tools in der Admin- und Befehlszeilenschnittstelle, um den Bestand zu konfigurieren, verfügbare und aggregierte Verkaufsmengen zu verfolgen, den Bestand während des Checkouts zu schützen und die Bestellabwicklung zu unterstützen. Sie können [!DNL Inventory Management] für eine einzelne Quelle oder ein Multi-Source-Netzwerk verwenden, das Lager, Geschäfte, Abholorte, Abholer und andere Erfüllungsorte umfasst.

## Verwendungsmöglichkeiten von [!DNL Inventory Management]

- **Admin:** Legen Sie Inventaroptionen fest und generieren Sie Inventarberichte.
- **Befehlszeilenschnittstelle:** Sie Setup-Befehle aus und wenden Sie Inventaränderungen im Hintergrund an.
- **Konfigurationsbereich:** Konfigurieren Sie Inventareinstellungen global, pro Quelle oder pro Produkt.

## Wichtigste Funktionen

Zu den [!DNL Inventory Management] Funktionen gehören:

- Unterschiedliche Konfigurationen für Händler, deren Inventar aus einer einzigen oder mehreren Quellen stammt
- Lagerbestände zur Ermittlung aggregierter Verkaufsmengen aus zugewiesenen Quellen
- Gleichzeitiger Auscheckschutz
- Algorithmen zum Sendungsabgleich, die Erfüllungsempfehlungen basierend auf Entfernung oder Priorität unterstützen

>[!NOTE]
>
>Diese Funktionen wurden im Rahmen des Projekts [Inventory management](https://github.com/magento/inventory) (ehemals MSI) über das Community Engineering-Programm entwickelt.<br/>
>
>Das [!DNL Inventory Management] wird mit Magento Open Source und Adobe Commerce installiert, wobei alle Funktionen standardmäßig aktiviert sind. Informationen zu den in den Modulversionen enthaltenen Änderungen finden Sie in den [Versionshinweisen](release-notes.md).

## Grundlegende Begriffe

Es ist wichtig, dass Sie die folgenden Begriffe bei der Arbeit mit [!DNL Inventory Management] verstehen:

[!UICONTROL Sources] stellen physische Standorte dar, an denen verfügbare Produkte gelagert und versendet werden. Beispiele [&#x200B; Diagramme finden Sie unter &#x200B;](sources-stocks.md) und Quellen . (Ein beliebiger Speicherort kann als Quelle für virtuelle Produkte angegeben werden.)

[!UICONTROL Stocks] einen Vertriebskanal (derzeit auf Websites beschränkt) Quellstandorten und verfügbarem Bestand zuordnen. Ein Lager kann mehreren Vertriebskanälen zugeordnet werden, ein Vertriebskanal kann jedoch nur einem Lager zugewiesen werden.

[!UICONTROL Aggregate Salable Quantity] ist der gesamte virtuelle Bestand, der über einen Vertriebskanal verkauft werden kann. Der Betrag wird für alle einem Lager zugeordneten Quellen berechnet.

[!UICONTROL Reservations] verfolgen Abzüge von der Verkaufsmenge, wenn Kunden Produkte zum Warenkorb hinzufügen und den Checkout abschließen. Wenn ein Auftrag ausgeliefert wird, werden die ausgelieferten Beträge durch die Reservierung verrechnet und von den jeweiligen Lagerbestandsmengen abgezogen.
