---
title: Daten exportieren
description: Erfahren Sie mehr über Datenexportfilter und -attribute und darüber, wie Sie Daten aus Ihrem Store exportieren.
exl-id: 80e7a2fc-beaa-416e-a00f-a3cad5055975
feature: Products, Customers, Data Import/Export
source-git-commit: f8254db7d69e58c8e9a78948ee6e40f5ea88cea0
workflow-type: tm+mt
source-wordcount: '792'
ht-degree: 0%

---

# Daten exportieren

Die beste Möglichkeit, sich mit der Struktur Ihrer Datenbank vertraut zu machen, besteht darin, die Daten zu exportieren und in einer Tabelle zu öffnen. Nachdem Sie sich mit dem Prozess vertraut gemacht haben, können Sie ihn als effiziente Methode zum Verwalten großer Informationsmengen verwenden.

Sonderzeichen - wie das Gleichheitszeichen, größer und kleiner als Symbole, einfache und doppelte Anführungszeichen, umgekehrte Schrägstriche, senkrechte Striche und kaufmännische Und-Zeichen - können bei der Datenübertragung zu Problemen führen. Um sicherzustellen, dass solche Sonderzeichen korrekt interpretiert werden, können sie als _Escape-Sequenz“ markiert_. Wenn die Daten beispielsweise eine Textzeichenfolge wie `code="str"`, `code="str2"` enthalten, wird durch das Einschließen des Textes in doppelte Anführungszeichen sichergestellt, dass die ursprünglichen doppelten Anführungszeichen als Teil der Daten verstanden werden: `"code="str""`. Wenn das System auf doppelte Anführungszeichen trifft, versteht es, dass der äußere Satz doppelter Anführungszeichen die tatsächlichen Daten einschließt.

Der Datenexport ist ein asynchroner Vorgang, der im Hintergrund ausgeführt wird, damit Sie in der Admin weiterarbeiten können, ohne auf den Abschluss des Vorgangs zu warten. Wenn die Aufgabe abgeschlossen ist, wird eine Meldung angezeigt.

## Exportkriterien

Exportfilter werden verwendet, um die Daten, die Sie in die Exportdatei aufnehmen möchten, basierend auf dem Attributwert anzugeben. Darüber hinaus können Sie angeben, welche Attributdaten Sie ein- oder vom Export ausschließen möchten.

![Datenexportkriterien](./assets/data-export-entity-attributes-exclude.png){width="600" zoomable="yes"}

### Filter exportieren

Sie können Filter verwenden, um zu bestimmen, welche SKUs in der Exportdatei enthalten sind. Wenn Sie beispielsweise einen Wert im Filter Herstellungsland eingeben, enthält die exportierte CSV-Datei nur die in diesem Land hergestellten Produkte.

Der Filtertyp entspricht dem Datentyp. Bei Datumsfeldern können Sie das Datum im Kalender (![) &#x200B;](../assets/icon-calendar.png). Weitere Informationen finden [&#x200B; unter &quot;](../catalog/attributes-input-types.md)-Eingabetypen“.

Das Format des Datums wird durch das [Gebietsschema“ &#x200B;](../getting-started/store-details.md#locale-options).

Um nur Datensätze mit einem bestimmten Wert einzubeziehen, z. B. eine SKU, geben Sie den Wert in das Feld Filter ein. Einige Felder wie „Preis“, „Gewicht“ und „Produkt als neu festlegen“ haben einen Wertebereich von/bis .

### Ausschließen von Attributen

Das Kontrollkästchen in der ersten Spalte wird verwendet, um Attribute aus der Exportdatei auszuschließen. Wenn ein Attribut ausgeschlossen wird, wird die zugehörige Spalte in den Exportdaten einbezogen, sie ist jedoch leer.

| ausschließen | Filter | Ergebnis |
|--- |--- |--- |
| ![Kontrollkästchen deaktiviert](../assets/checkbox-clear.png) | Nein | Die exportierte Datei enthält jedes Attribut für alle vorhandenen Datensätze. |
| ![Kontrollkästchen deaktiviert](../assets/checkbox-clear.png) | Ja | Die Exportdatei enthält jedes Attribut mit nur den vom Filter zulässigen Datensätzen. |
| ![Kontrollkästchen aktiviert](../assets/checkbox-selected.png) | Nein | Die Exportdatei enthält nicht die Spalte für das ausgeschlossene Attribut, sondern alle vorhandenen Datensätze. |
| ![Kontrollkästchen aktiviert](../assets/checkbox-selected.png) | Ja | Die Exportdatei enthält nicht die Spalte für das ausgeschlossene Attribut und enthält nur die vom Filter zulässigen Datensätze. |

{style="table-layout:auto"}

## Daten exportieren

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. Legen _im Abschnitt_ Exporteinstellungen **[!UICONTROL Entity Type]** eine der folgenden Einstellungen fest:

   - `Advanced Pricing`
   - `Products`
   - `Customer Finances`
   - `Customers Main File`
   - `Customer Addresses`
   - `Stock Sources`

   ![Einstellungen für den Datenexport](./assets/data-export-settings.png){width="600" zoomable="yes"}

1. Akzeptieren Sie die **[!UICONTROL Export File Format]** der CSV-Datei.

1. Wenn Sie alle Sonderzeichen, die sich möglicherweise in den Daten befinden, als _Escape-Sequenz_ einschließen möchten, aktivieren Sie das Kontrollkästchen **[!UICONTROL Fields Enclosure]** .

1. Ändern Sie bei Bedarf die Anzeige der Entitätsattribute.

   Standardmäßig werden im Abschnitt Entitätsattribute alle verfügbaren Attribute in alphabetischer Reihenfolge aufgelistet. Sie können die standardmäßigen [Listensteuerelemente“ verwenden](../getting-started/admin-grid-controls.md) um nach bestimmten Attributen zu suchen und die Liste zu sortieren. Die Steuerelemente zum Suchen und Zurücksetzen steuern die Anzeige der Liste, haben jedoch keine Auswirkungen auf die Auswahl der Attribute, die in die Exportdatei aufgenommen werden sollen.

   ![Datenexport - Gefilterte Entitätsattribute](./assets/data-export-filter-entity-attributes.png){width="600" zoomable="yes"}

1. Gehen Sie wie folgt vor, um die exportierten Daten nach Attributwerten zu filtern:

   - Um nur Datensätze mit bestimmten Attributwerten zu exportieren, geben Sie den erforderlichen Wert in die Spalte **[!UICONTROL Filter]** ein. Im folgenden Beispiel wird nur eine bestimmte SKU exportiert.

   - Um ein Attribut im Export wegzulassen, aktivieren Sie das Kontrollkästchen **[!UICONTROL Exclude]** am Anfang der Zeile. Um beispielsweise nur die Spalten `sku` und `image` zu exportieren, aktivieren Sie das Kontrollkästchen jedes anderen Attributs. Die Spalte wird in der Exportdatei angezeigt, jedoch ohne Werte.

1. Scrollen Sie nach unten und klicken Sie in der rechten unteren Ecke der Seite auf **[!UICONTROL Continue]** .

   Nach Abschluss der Aufgabe wird die Datei über eine Nachrichtenwarteschlange verarbeitet (stellen Sie sicher, dass Ihr Cron-Auftrag ausgeführt wird). Die exportierte Datei wird im `var/export/ folder` gespeichert. Weitere Informationen zur Nachrichtenwarteschlange finden Sie unter [Verwalten von Nachrichtenwarteschlangen](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html?lang=de) im _Konfigurationshandbuch_.

   Sie können die exportierte CSV-Datei als Tabelle speichern oder öffnen, dann die Daten bearbeiten und sie wieder in Ihren Store importieren.

   >[!NOTE]
   >
   >Standardmäßig befinden sich alle exportierten Dateien im Ordner `<Magento-root-directory>/var/export` . Wenn das Remote-Speichermodul aktiviert ist, befinden sich alle exportierten Dateien im `<remote-storage-root-directory>/import_export/export`.

## Fehlerbehebung bei Ressourcen

Hilfe bei der Fehlerbehebung bei Problemen mit dem Datenexport finden Sie in den folgenden Artikeln der Commerce-Support-Wissensdatenbank:

- [Exportierte Produkte.csv-Datei wird nicht angezeigt](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/exported-products-.csv-file-does-not-appear.html?lang=de)
