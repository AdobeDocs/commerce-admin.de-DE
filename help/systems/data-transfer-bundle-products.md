---
title: Bundle-Produkte importieren
description: Sehen Sie sich ein Beispiel für den Import von Produktdaten für ein Produkt-Bundle an.
exl-id: 52146979-9911-449b-9f14-54377e2ae9f4
feature: Products, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 0%

---

# Bundle-Produkte importieren

Ein Produktpaket enthält eine Auswahl an Artikeln und ermöglicht es Kunden, die Artikel auszuwählen, die sie erwerben möchten. Alle Elemente, aus denen ein Bundle besteht, sind im Katalog entweder [Einfache Produkte](../catalog/product-create-simple.md) oder [Virtuelle Produkte](../catalog/product-create-virtual.md). In der Regel werden Bundle-Produkte von der Administratorin bzw. dem Administrator erstellt und aktualisiert. Sie können jedoch auch Daten importieren, um ein Bundle-Produkt zu erstellen, oder Sie können vorhandene Bundle-Produkte exportieren, die Daten bearbeiten und sie wieder in den Katalog importieren. Das Sprite Yoga Companion Kit ist ein Bundle-Produkt in den Beispieldaten, das in den folgenden Beispielen verwendet wird.

![Bundle-Produkt](../catalog/assets/product-bundle.png){width="700" zoomable="yes"}

## Reihenfolge der Bundle-Elemente ändern

Es gibt zwei Möglichkeiten, die Reihenfolge der Elemente in einem Produktpaket zu ändern.

### Methode 1: Ziehen und Ablegen

Beim Arbeiten mit einem [Bundle](../catalog/product-create-bundle.md)-Produkt vom Administrator können Sie Elemente und Abschnitte per Drag-and-Drop an die gewünschte Position ziehen.

![Bundle-Elemente](../catalog/assets/product-bundle-items-move.png){width="600" zoomable="yes"}

### Methode 2: Bearbeiten der Produktdaten

Die beste Möglichkeit, die Struktur eines Produktpakets zu verstehen, besteht darin, das Produkt zu exportieren und die Daten in einer Tabelle zu untersuchen. Sie können die Reihenfolge der Bundle-Elemente ändern, indem Sie das Produkt exportieren und den Daten für jedes Element einen Positionsparameter hinzufügen. Die Elementdaten befinden sich in der Spalte `bundle_values` des exportierten Produkts. Beim Öffnen in einer Tabelle befinden sich alle mit dem Produkt verknüpften Elemente in einer Zelle als lange Textzeichenfolge. Die Spalte `bundle_values` enthält für jedes Element die folgenden Elemente:

- Name des Artikelabschnitts
- Eingabekontrolle
- Indikator für erforderliches Element
- SKU
- Farbe
- Preis
- Indikator für Standardoption
- Standardmenge
- Preisart
- Indikator für bearbeitbare Menge

#### Schritt 1: Bundle-Produkt exportieren

In diesem Schritt wird das Sprite Yoga Companion Kit als (CSV[-Datei &#x200B;](data-csv.md). Sie können jedes andere Bundle-Produkt verwenden, das Sie in Ihrem Katalog haben.

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. Legen _unter „Exporteinstellungen_ den **[!UICONTROL Entity Type]** auf `Products` fest.

1. Scrollen Sie in der Liste der Produktattribute nach unten zu **[!UICONTROL SKU]** und geben Sie die SKU des Produktpakets ein, das Sie exportieren möchten.

   In diesem Beispiel wird die SKU für das Produkt `24-WG080`.

1. Scrollen Sie nach unten zum unteren Rand des Abschnitts und klicken Sie auf **[!UICONTROL Continue]**.

1. Klicken Sie in der Spalte _[!UICONTROL Action]_&#x200B;des&#x200B;_[!UICONTROL File name]_ Rasters auf **[!UICONTROL Select]** und wählen Sie `Download` aus.

   Die Datei wird im von Ihrem Browser verwendeten Download-Speicherort angezeigt.

#### Schritt 2: Daten bearbeiten

1. Öffnen Sie die heruntergeladene CSV-Datei in einer Tabelle.

1. Scrollen Sie nach ganz rechts, bis Sie die Spalte `bundle_values` sehen.

   In den `bundle_values` Daten wird jedes Element durch Kommas getrennt, und jedes Bundle-Element wird vom nächsten durch einen vertikalen Balken getrennt. (Das letzte Element endet nicht mit einem vertikalen Balken.) Die exportierten Bundle-Daten sollten etwa wie im folgenden Beispiel aussehen:

   ![Paketwerte](./assets/product-bundle-values-export-data.png){width="600" zoomable="yes"}

1. Um die Bearbeitung zu vereinfachen, können Sie die `bundle_values` Daten kopieren und in einen Texteditor einfügen und dann nach jedem Element einen Zeilenumbruch hinzufügen, sodass sich jedes Element in einer separaten Zeile befindet.

1. Nachdem Sie die Daten bearbeitet haben, entfernen Sie die Zeilenumbrüche sorgfältig und fügen Sie die bearbeiteten Daten wieder in die Spalte `bundle_values` ein.

   In der folgenden Abbildung wird jedem Yoga-Riemen ein `position=[number]` hinzugefügt, um die Reihenfolge der Elemente in der Store-Liste zu ändern.

   ![Positionsparameter](./assets/product-bundle-values-position-parameter.png){width="500" zoomable="yes"}

1. Nachdem Sie die Daten bearbeitet haben, **[!UICONTROL Save]** Sie die CSV-Datei.

#### Schritt 3: Importieren des aktualisierten Produkts

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**.

1. Legen Sie unter _[!UICONTROL Import Settings]_&#x200B;**[!UICONTROL Entity Type]**&#x200B;auf `Products` fest.

1. Legen Sie **[!UICONTROL Import Behavior]** auf `Replace` fest.

   Diese Option überschreibt die vorherigen Daten für Ihr Produktpaket, anstatt Ihre Änderungen als zusätzliche Elemente hinzuzufügen.

1. Scrollen Sie nach unten zum Abschnitt _Zu importierende Datei_ und klicken Sie auf **[!UICONTROL Choose File]**.

1. Wählen Sie die bearbeitete CSV-Datei aus.

1. Klicken Sie auf **[!UICONTROL Check Data]** und warten Sie einige Augenblicke, bis die Daten überprüft wurden.

1. Wenn die Datei gültig ist, klicken Sie auf **[!UICONTROL Import]**.

1. Wenn der Vorgang abgeschlossen ist, navigieren Sie zu **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**&#x200B;und klicken Sie auf **[!UICONTROL Flush Cache Storage]**.

   Dadurch wird sichergestellt, dass das aktualisierte Produkt sofort in der Storefront verfügbar ist.
