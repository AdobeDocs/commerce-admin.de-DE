---
title: Aktualisierung der Steuersatzdaten
description: Erfahren Sie, wie Sie mit Export- und Importvorgängen die Steuersätze für Ihren Store aktualisieren können.
exl-id: a3ef718d-b296-41d7-a1b8-ae8274da71b6
feature: Taxes, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '615'
ht-degree: 0%

---

# Aktualisierung der Steuersatzdaten

Wenn Sie Geschäfte in mehreren Staaten betreiben und eine große Menge von Produkten liefern, kann die manuelle Eingabe der Steuersätze sehr zeitaufwendig sein. Es ist schneller und effizienter, Steuersätze nach Postleitzahl herunterzuladen und in den Handel zu importieren. Das folgende Beispiel zeigt, wie Sie eine Reihe von staatenspezifischen Steuersätzen importieren, die von einer vertrauenswürdigen Quelle heruntergeladen wurden. Avalara bietet [Steuersatztabellen](https://www.avalara.com/taxrates/en/download-tax-tables.html), die Sie für jede Postleitzahl in den USA kostenlos herunterladen können.

>[!NOTE]
>
>Wenn Sie Ihre Verkäufe automatisieren und Steuerbestimmungen und Berichte verwenden möchten, finden Sie Commerce-vertrauenswürdige Optionen auf der Seite [Handelspartner](https://solutionpartners.adobe.com/s/directory/?solution=commerce) Site.

## Schritt 1: Exportieren der Daten zum Commerce-Steuersatz

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import/Export Tax Rates]**.

1. Klicken **[!UICONTROL Export Tax Rates]**.

1. Suchen Sie nach der Datei im Download-Speicherort für Ihren Webbrowser.

1. Speichern und öffnen Sie die Datei in einer Tabelle.

   Dieses Beispiel verwendet [!DNL OpenOffice Calc].

   Die exportierten Commerce-Steuersatzdaten enthalten die folgenden Spalten:
   - Code
   - Land
   - Bundesland
   - Postleitzahl
   - Rate
   - Bereich von
   - Bereich bis
   - Eine Spalte für jede Store-Ansicht

   ![Exportierte Daten - Steuersätze](./assets/data-exported-tax-rates.png){width="500" zoomable="yes"}

1. Öffnen Sie die neuen Steuersatzdaten in einer zweiten Instanz des Arbeitsblatts, damit Sie sie nebeneinander sehen können.

1. Beachten Sie in den neuen Steuersatzdaten alle zusätzlichen Steuersatzdaten, die Sie möglicherweise in Ihrem Speicher einrichten müssen, bevor die Daten importiert werden.

   Die Steuersatzdaten für Kalifornien umfassen beispielsweise auch:

   - `TaxRegionName`
   - `CombinedRate`
   - `StateRate`
   - `CountyRate`
   - `CityRate`
   - `SpecialRate`

   Wenn Sie weitere Importe benötigen [Steuergebiete und Steuersätze](../stores-purchase/tax-zones-rates.md)müssen Sie sie zunächst über den Administrator Ihres Stores definieren und die [Steuervorschriften](../stores-purchase/tax-rules.md) nach Bedarf. Exportieren Sie dann die Daten und öffnen Sie die Datei in einem Texteditor, damit sie als Referenz verwendet werden kann. Um dieses Beispiel einfach zu halten, importieren wir jedoch nur die Standardspalten für den Steuersatz.

## Schritt 2: Vorbereitung der Importdaten

Zwei Tabellen sind nebeneinander geöffnet. Das eine enthält die Dateistruktur des Commerce-Exports und das andere die neuen Steuersatzdaten, die Sie importieren möchten.

1. Um einen Ort zu erstellen, an dem die neuen Steuersatzdaten in der Tabelle verwendet werden können, fügen Sie rechts so viele leere Spalten ein, wie nötig sind, um Daten aus der Commerce-Exportdatei hinzuzufügen. Fügen Sie die Daten mithilfe des Cut-and-Paste-Verfahrens hinzu und ordnen Sie die Spalten so an, dass sie der Reihenfolge der Commerce-Exportdatendatei entsprechen.

1. Benennen Sie die Spaltenüberschriften so um, dass sie den Commerce-Exportdaten entsprechen.

1. Löschen Sie alle Spalten, die keine Daten enthalten.

   Andernfalls sollte die Struktur der Importdatei mit den ursprünglichen Commerce-Exportdaten übereinstimmen.

1. Scrollen Sie vor dem Speichern der Datei nach unten und stellen Sie sicher, dass die Steuersatzspalten nur numerische Daten enthalten.

   In einer Spalte mit dem Steuersatz enthaltener Text verhindert den Import der Daten.

1. Speichern Sie die vorbereiteten Daten als .CSV-Datei.

   Stellen Sie bei entsprechender Aufforderung sicher, dass ein Komma als Feldtrennzeichen und doppelte Anführungszeichen als Texttrennzeichen verwendet wird. Klicken Sie anschließend auf **[!UICONTROL OK]**.

## 3. Schritt: Einführung der Steuersätze

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import/Export Tax Rates]**.

1. Klicks **[!UICONTROL Choose File]** und wählen Sie die CSV-Steuersatzdatei aus, die Sie für den Import vorbereitet haben.

1. Klicken **[!UICONTROL Import Tax Rates]**.

   Der Import der Daten kann mehrere Minuten dauern. Wenn der Prozess abgeschlossen ist, wird die `The tax rate has been imported` angezeigt. Wenn Sie eine Fehlermeldung erhalten, korrigieren Sie das Problem in den Daten und versuchen Sie es erneut.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**.

   Die importierten Raten werden in der Liste angezeigt.

1. Verwenden Sie die Seitensteuerelemente, um die neuen Steuersätze anzuzeigen.

   ![Dateneinfuhrsteuersätze](../stores-purchase/assets/tax-zones-rates.png){width="600" zoomable="yes"}

1. Führen Sie einige Testtransaktionen in Ihrem Geschäft mit Kunden aus unterschiedlichen Postleitzahlen aus, um sicherzustellen, dass die neuen Steuersätze ordnungsgemäß funktionieren.
