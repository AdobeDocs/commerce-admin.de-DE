---
title: Lagermengen verwalten
description: Übersicht über die Administrationsverfahren zur Zuordnung von Quellen und Stückzahlen für neue und vorhandene Produkte in [!DNL Inventory Management].
exl-id: b3d4a4c0-725a-4e62-854f-efb6a5709f73
feature: Inventory, Products
TQID: 'https://experienceleague.adobe.com/ykiHTLnzZGtJrRdp2wZvlL7YLbEb7iAiYlcbY8K7IX8'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: 8dc0e58b-adf0-51bb-8db5-bb36e3e656fb
    internal-label: Inventory
  - id: 4067ab89-2e97-5de1-8d98-de8318461a8d
    internal-label: Products
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 0%
---
# Lagermengen verwalten

Verwenden Sie die folgenden Richtlinien, um Quellen und Mengen für neue oder vorhandene Produkte zuzuweisen.

Weisen Sie beim Erstellen von Produkten Quellen und Mengen während der Produkterstellung zu. Vollständige Anweisungen finden [ unter ](../catalog/product-create.md)Erstellen eines Produkts“. Diese Seiten enthalten Informationen aus einer und mehreren Quellen für Quellen und Mengen pro Quelle.

Beim erstmaligen Zugriff auf ein upgegradetes [!DNL Commerce] mit [!DNL Inventory Management] werden alle Produkte und Mengen der Standard-Source zugewiesen. Beim Importieren neuer Produkte über eine CSV-Datei werden diese ebenfalls der Standard-Source zugewiesen.

Händler, die aus einer oder mehreren Quellen stammen, können Quellen, Lagermengen und Schwellenwerte pro Produkt oder in großen Mengen aktualisieren.

- Einzelhändler können Produktmengen für die Standard-Source aktualisieren. Diese Menge ist die Gesamtzahl der zum Verkauf verfügbaren Produkte.

- Händler, die mehrere Bezugsquellen haben, können für jeden Standort (Lager, Geschäfte, Ablieferer usw.) mehrere Bezugsquellen und Mengen pro Produkt zuweisen. Es wird empfohlen, Quellen hinzuzufügen, bevor Sie die Produktinventarbeträge festlegen.

Beim Hinzufügen von Quellen und Mengen zu Ihren Produkten können Sie die Mengen über das Produktraster anzeigen. Wenn Sie eine hohe Anzahl von Quellen haben, bewegen Sie den Mauszeiger über die _[!UICONTROL Quantity per Source]_, um die vollständige, scrollbare Liste der Quellen mit aktuellen Mengen anzuzeigen.

![Produktmengen pro Quelle](assets/inventory-product-quantity.png){width="600" zoomable="yes"}

Sie haben die folgenden Optionen, um den Produkten Inventar zuzuweisen:

- [Quellen pro Produkt zuweisen](sources-assign-per-product.md) - Manuelles Zuweisen von Quellen pro Produkt in Ihrem Katalog.

- [Mengen pro Produkt zuweisen](quantities-assign-per-product.md) - Bestandsmengen zu Ihren Produkten pro Quelle hinzufügen. Diese Informationen sind spezifisch für Händler, die mehrere Quellen nutzen.

- [Massenzuweisung und -aufheben](bulk-assignment.md) - Zuweisen von Quellen zu ausgewählten Produkten als Massenaktion. Verwenden Sie die Option [Inventar an Source übertragen](inventory-transfer.md), wenn Sie Inventar übertragen und die Quelle entfernen möchten.

- [Lagertransfer an Source](inventory-transfer.md) - Massentransfer des gesamten Lagerbestands von einer Ursprungsquelle zu einer Zielquelle.

- [Mengen importieren und exportieren](inventory-import-export.md) - Verwenden Sie Import- und Exportfunktionen, um mehrere Produkt-SKUs mit Quellen und Lagermengen zu aktualisieren.
