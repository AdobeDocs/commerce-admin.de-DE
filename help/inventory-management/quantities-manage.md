---
title: Lagermengen verwalten
description: Erfahren Sie, wie Sie Quellen und Mengen für neue Produkte zuweisen oder vorhandene Produkte ändern.
exl-id: b3d4a4c0-725a-4e62-854f-efb6a5709f73
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# Lagermengen verwalten

Die folgenden Informationen beschreiben, wie Sie Quellen und Mengen für neue Produkte zuordnen oder vorhandene Produkte ändern.

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
