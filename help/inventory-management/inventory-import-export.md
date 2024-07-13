---
title: Import- und Ausfuhrinventar
description: Verwenden Sie die nativen Import- und Exportfunktionen mit erweiterten [!DNL Inventory Management] Optionen, um Quellen und Mengen nach SKU zu aktualisieren.
exl-id: cb2d2e0d-aef8-4b18-b013-9a7b0ab448bd
feature: Inventory, Data Import/Export
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '507'
ht-degree: 0%

---

# Import- und Ausfuhrinventar

Verwenden Sie für Kataloge mit vielen Produkten die nativen Import- und Exportfunktionen mit erweiterten [!DNL Inventory Management] -Optionen, um Quellen und Mengen nach SKU zu aktualisieren. Mit diesen Optionen können Sie neue Quellen hinzufügen und Lagerbestandsmengen für alle oder eine bestimmte Quelle aktualisieren. Sie können beispielsweise Produkte für eine Quelle in Deutschland exportieren, ohne die Produktinformationen für Quellen in Frankreich, England oder den USA zu beeinträchtigen.

- [!DNL Commerce] weist Ihren Produkten beim Upgrade von [!DNL Commerce] oder beim Import neuer Produkte automatisch die standardmäßige Source zu. Wenn Sie Produkte importieren, denen eine benutzerdefinierte Quelle zugewiesen ist, wird die standardmäßige Source mit einer Menge von 0 hinzugefügt. Verwenden Sie diese Einfuhranweisungen, um Quellen und Mengen zu aktualisieren.

- Einzelquellenhändler verwenden den Import, um nur die Produktmengen zu aktualisieren. Alle vorhandenen und hinzugefügten Produkte werden der Standard-Source zugewiesen.

- Händler mit mehreren Quellen verwenden den Import, um mehrere Quellen und Mengen pro Zeile pro SKU hinzuzufügen.

Um Aktualisierungen zu importieren, exportieren Sie zunächst eine CSV-Datei für eine bestimmte oder alle Quellen. Bearbeiten Sie die CSV-Datei und fügen Sie für jede Quelle und Menge eine Zeile pro SKU hinzu. Sie benötigen den Quellcode, wenn Sie eine Quelle hinzufügen und Lagermengen hinzufügen. Mit Import- und Exportfunktionen können Sie keine Lager hinzufügen oder aktualisieren.

## CSV-Dateiinhalt

Die Datei export-import enthält je nach Quelle die folgenden Informationen:

- `source_code` - Der Code für Quellen in [!DNL Commerce]. Für jede Quelle und SKU gibt es eine Zeile.
- `sku` - Die SKU für das Produkt in [!DNL Commerce]. Die SKU muss mit einem Produkt in Ihrem Store übereinstimmen, um [!DNL Inventory Management]-Daten ordnungsgemäß zu aktualisieren.
- `status` - 0 für nicht auf Lager. 1 für Auf Lager. Dieser Wert muss 1 betragen, um einen Lagerbestand aus dieser Quelle zu erwerben.
- `quantity` - Die Gesamtsumme des für diese SKU und Quelle verfügbaren Bestands.

Verwenden Sie eine CSV-Datei, um schnell mehrere Produkte und zugewiesene Quellen zu aktualisieren und Ungenauigkeiten in Inventardatensätzen zu aktualisieren und zu korrigieren, anstatt sie über die Anwendungsschnittstelle einzeln zu verwenden. Exportieren Sie für eine Basisdatei zuerst und aktualisieren Sie sie nach Bedarf.

![Beispiel einer CSV-Datei für den Import - Export von Bestandsdaten](assets/inventory-import-export-data.png){width="600" zoomable="yes"}

## Produktdaten für alle Quellen exportieren

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. Wählen Sie für **[!UICONTROL Entity Type]** `Stock Sources` aus.

   Der Export extrahiert nur Daten für Produkte mit einer SKU.

1. Klicken Sie auf **[!UICONTROL Continue]**.

   Die Datei wird generiert und heruntergeladen, um sie zu öffnen und zu bearbeiten.

Importieren Sie die Datei nach der Aktualisierung von Lagerbestandsmengen und Produktdaten wieder in [!DNL Commerce].

![Export von Lagerbestandsquellen für Produktdaten und -quellen](assets/inventory-export-stock-sources.png){width="350" zoomable="yes"}

## Produktdaten für eine bestimmte Quelle exportieren

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. Wählen Sie für **[!UICONTROL Entity Type]** `Stock Sources` aus.

   Der Export extrahiert nur Daten für Produkte mit einer SKU.

1. Verwenden Sie den **[!UICONTROL Entity Attributes]** , um die exportierten Produkte nach einer bestimmten Quelle zu filtern.

   Geben Sie für &quot;`source_code`&quot; den Code für die Quelle in das Filterfeld ein.

1. Klicken Sie auf **[!UICONTROL Continue]**.

   Die Datei wird generiert und heruntergeladen, um sie zu öffnen und zu bearbeiten.

Importieren Sie die Datei nach der Aktualisierung von Lagerbestandsmengen und Produktdaten wieder in [!DNL Commerce].

## Produktdaten importieren

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**.

1. Wählen Sie für **[!UICONTROL Entity Type]** `Stock Sources` aus.

   Der Export extrahiert nur Daten für Produkte mit einer SKU.

1. Wählen Sie Konfigurationen für die **[!UICONTROL Import Behavior]** aus.

1. Wählen Sie die zu importierende CSV-Datei aus.

1. Klicken Sie auf &quot;**[!UICONTROL Check Data]**&quot;und schließen Sie den Import ab.

![Importieren von Produktdaten und Quellen](assets/inventory-import-sources.png){width="600" zoomable="yes"}
