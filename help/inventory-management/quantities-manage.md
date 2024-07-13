---
title: Lagerbestandsmengen verwalten
description: Erfahren Sie, wie Sie Quellen und Mengen für neue Produkte zuweisen oder vorhandene Produkte ändern.
exl-id: b3d4a4c0-725a-4e62-854f-efb6a5709f73
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# Lagerbestandsmengen verwalten

Im Folgenden wird beschrieben, wie Quellen und Mengen für neue Produkte zugewiesen oder bestehende Produkte geändert werden.

Weisen Sie bei der Erstellung von Produkten Quellen und Mengen zu. Vollständige Anweisungen finden Sie unter [Produkt erstellen](../catalog/product-create.md) . Diese Seiten enthalten Informationen zu einzelnen und mehreren Quellen für Quellen und Mengen pro Quelle.

Beim erstmaligen Zugriff auf eine aktualisierte [!DNL Commerce] mit [!DNL Inventory Management] werden alle Produkte und Mengen der Standard-Source zugewiesen. Beim Import neuer Produkte über die .csv -Datei werden diese auch der Standard-Source zugewiesen.

Einzelhändler und Händler mit mehreren Quellen können Quellen, Lagerbestandsmengen und Schwellenwerte pro Produkt oder in großen Mengen aktualisieren.

- Einzelquellenhändler können die Produktmengen für die Standard-Source aktualisieren. Diese Menge entspricht der Gesamtzahl der zum Verkauf stehenden Produkte.

- Händler mit mehreren Quellen können für jeden Standort (Lagerhäuser, Geschäfte, Spediteure usw.) mehrere Quellen und Mengen pro Produkt zuweisen. Es wird empfohlen, dass Sie Quellen hinzugefügt haben, bevor Sie Produktinventarmengen festlegen.

Beim Hinzufügen von Quellen und Mengen zu Ihren Produkten können Sie die Beträge über das Produktraster anzeigen. Wenn Sie eine große Anzahl von Quellen haben, halten Sie den Mauszeiger über die _[!UICONTROL Quantity per Source]_, um die vollständige, durchlaufbare Liste der Quellen mit aktuellen Mengen anzuzeigen.

![Produktmengen pro Quelle](assets/inventory-product-quantity.png){width="600" zoomable="yes"}

Sie haben die folgenden Optionen, um Inventar Produkten zuzuweisen:

- [Zuweisen von Quellen pro Produkt](sources-assign-per-product.md) - Zuweisen von Quellen manuell pro Produkt in Ihrem Katalog.

- [Zuweisen von Mengen pro Produkt](quantities-assign-per-product.md) - Fügen Sie die Lagerbestände Ihrer Produkte pro Quelle hinzu. Diese Informationen sind spezifisch für Händler mit mehreren Quellen.

- [Zuweisen und Aufheben der Zuweisung von Quellen durch Massenzugriff](bulk-assignment.md) - Weisen Sie ausgewählten Produkten Quellen Massenaktionen zu. Verwenden Sie die Option [Inventar an Source übertragen](inventory-transfer.md) , wenn Sie den Bestand übertragen und die Quelle entfernen möchten.

- [Inventar auf Source übertragen](inventory-transfer.md) - Alle Bestände werden von einer Quelle an eine Zielquelle übertragen.

- [Importieren und Exportieren von Mengen](inventory-import-export.md) - Verwenden Sie Import- und Exportfunktionen, um mehrere Produkt-SKUs mit Quellen und Lagerbestandsmengen zu aktualisieren.
