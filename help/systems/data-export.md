---
title: Daten exportieren
description: Erfahren Sie mehr über Datenexportfilter und -attribute und über das Exportieren von Daten aus Ihrem Store.
exl-id: 80e7a2fc-beaa-416e-a00f-a3cad5055975
feature: Products, Customers, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 0%

---

# Daten exportieren

Die beste Möglichkeit, sich mit der Struktur Ihrer Datenbank vertraut zu machen, besteht darin, die Daten zu exportieren und in einer Tabelle zu öffnen. Nachdem Sie sich mit dem Prozess vertraut gemacht haben, können Sie ihn als effiziente Methode zur Verwaltung großer Datenmengen verwenden.

Sonderzeichen wie Gleichheitszeichen, Größer- und Kleiner-als-Symbole, einfache und doppelte Anführungszeichen, umgekehrter Schrägstrich, Strich und Und-Zeichen können Probleme bei der Datenübertragung verursachen. Um sicherzustellen, dass solche Sonderzeichen richtig interpretiert werden, können sie als _Escape-Sequenz_. Wenn die Daten beispielsweise eine Textzeichenfolge wie `code="str"`, `code="str2"`, wodurch der Text in doppelte Anführungszeichen gesetzt wird, stellen sicher, dass die ursprünglichen doppelten Anführungszeichen als Teil der Daten verstanden werden: `"code="str""`. Wenn das System auf einen doppelten Satz doppelter Anführungszeichen trifft, versteht es, dass der äußere Satz doppelter Anführungszeichen die tatsächlichen Daten umschließt.

Der Datenexport ist ein asynchroner Vorgang, der im Hintergrund ausgeführt wird, damit Sie die Arbeit in Admin fortsetzen können, ohne auf den Abschluss des Vorgangs warten zu müssen. Das System zeigt eine Meldung an, wenn die Aufgabe abgeschlossen ist.

## Exportkriterien

Exportfilter dienen dazu, die Daten anzugeben, die Sie in der Exportdatei basierend auf dem Attributwert verwenden möchten. Darüber hinaus können Sie festlegen, welche Attributdaten Sie in den Export einbeziehen oder daraus ausschließen möchten.

![Datenexportkriterien](./assets/data-export-entity-attributes-exclude.png){width="600" zoomable="yes"}

### Filter exportieren

Mithilfe von Filtern können Sie bestimmen, welche SKUs in der Exportdatei enthalten sind. Wenn Sie beispielsweise einen Wert in den Filter Land des Herstellers eingeben, enthält die exportierte CSV-Datei nur Produkte, die in diesem Land hergestellt wurden.

Der Filtertyp entspricht dem Datentyp. Für Datumsfelder können Sie das Datum aus dem Kalender auswählen ![Kalendersymbol](../assets/icon-calendar.png). Siehe [Attributeingabetypen](../catalog/attributes-input-types.md) für weitere Informationen.

Das Format des Datums wird durch die [locale](../getting-started/store-details.md#locale-options).

Um nur Datensätze mit einem bestimmten Wert einzuschließen, z. B. eine SKU, geben Sie den Wert in das Feld Filter ein. Einige Felder wie &quot;Preis&quot;, &quot;Gewichtung&quot;und &quot;Produkt als neu festlegen&quot;weisen einen von/zu Wertebereich auf.

### Attribute ausschließen

Das Kontrollkästchen in der ersten Spalte wird verwendet, um Attribute aus der Exportdatei auszuschließen. Wenn ein Attribut ausgeschlossen wird, wird die zugehörige Spalte in den Exportdaten eingeschlossen, jedoch leer.

| Ausschließen | Filter | Ergebnis |
|--- |--- |--- |
| ![Gelöschtes Kontrollkästchen](../assets/checkbox-clear.png) | Nein | Die exportierte Datei enthält jedes Attribut für alle vorhandenen Datensätze. |
| ![Gelöschtes Kontrollkästchen](../assets/checkbox-clear.png) | Ja | Die Exportdatei enthält jedes Attribut mit nur den vom Filter erlaubten Datensätzen. |
| ![Ausgewähltes Kontrollkästchen](../assets/checkbox-selected.png) | Nein | Die Exportdatei enthält nicht die Spalte für das ausgeschlossene Attribut, sondern enthält alle vorhandenen Datensätze. |
| ![Ausgewähltes Kontrollkästchen](../assets/checkbox-selected.png) | Ja | Die Exportdatei enthält nicht die Spalte für das ausgeschlossene Attribut und nur die vom Filter zugelassenen Datensätze. |

{style="table-layout:auto"}

## Daten exportieren

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. Im _Exporteinstellungen_ Abschnitt, festlegen **[!UICONTROL Entity Type]** auf einen der folgenden Werte zu:

   - `Advanced Pricing`
   - `Products`
   - `Customer Finances`
   - `Customers Main File`
   - `Customer Addresses`
   - `Stock Sources`

   ![Datenexporteinstellungen](./assets/data-export-settings.png){width="600" zoomable="yes"}

1. Standard akzeptieren **[!UICONTROL Export File Format]** von CSV

1. Wenn Sie Sonderzeichen einschließen möchten, die möglicherweise in den Daten als _Escape-Sequenz_, wählen Sie die **[!UICONTROL Fields Enclosure]** aktivieren.

1. Ändern Sie bei Bedarf die Anzeige der Entitätsattribute.

   Standardmäßig werden im Abschnitt &quot;Entitätsattribute&quot;alle verfügbaren Attribute in alphabetischer Reihenfolge aufgelistet. Sie können den Standard [Listenelemente](../getting-started/admin-grid-controls.md) , um nach bestimmten Attributen zu suchen und die Liste zu sortieren. Die Steuerelemente Suche und Filter zurücksetzen steuern die Anzeige der Liste, wirken sich jedoch nicht auf die Auswahl der Attribute aus, die in die Exportdatei aufgenommen werden sollen.

   ![Datenexport gefilterte Entitätsattribute](./assets/data-export-filter-entity-attributes.png){width="600" zoomable="yes"}

1. Gehen Sie wie folgt vor, um die exportierten Daten nach Attributwerten zu filtern:

   - Um nur Datensätze mit bestimmten Attributwerten zu exportieren, geben Sie den erforderlichen Wert in die **[!UICONTROL Filter]** Spalte. Im folgenden Beispiel wird nur eine bestimmte SKU exportiert.

   - Um ein Attribut aus dem Export auszuschließen, wählen Sie die **[!UICONTROL Exclude]** am Anfang der Zeile. Um beispielsweise nur die `sku` und `image` -Spalten das Kontrollkästchen jedes anderen Attributs aktivieren. Die Spalte wird in der Exportdatei angezeigt, jedoch ohne Werte.

1. Scrollen Sie nach unten und klicken Sie auf **[!UICONTROL Continue]** in der rechten unteren Ecke der Seite.

   Nach Abschluss der Aufgabe wird die Datei über eine Nachrichtenwarteschlange verarbeitet (stellen Sie sicher, dass Ihr Cron-Auftrag ausgeführt wird). Die exportierte Datei wird im `var/export/ folder`. Weitere Informationen zur Nachrichtenwarteschlange finden Sie unter [Verwalten von Nachrichtenwarteschlangen](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) im _Konfigurationshandbuch_.

   Sie können die exportierte CSV-Datei als Tabelle speichern oder öffnen, dann die Daten bearbeiten und wieder in Ihren Speicher importieren.

   >[!NOTE]
   >
   >Standardmäßig befinden sich alle exportierten Dateien im `<Magento-root-directory>/var/export` Ordner. Wenn das Remote-Speichermodul aktiviert ist, befinden sich alle exportierten Dateien im `<remote-storage-root-directory>/import_export/export` Ordner.

## Fehlerbehebung bei Ressourcen

Hilfe zur Behebung von Problemen beim Datenexport finden Sie in den folgenden Artikeln der Knowledge Base des Commerce-Supports:

- [Die .csv-Datei der exportierten Produkte wird nicht angezeigt](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/exported-products-.csv-file-does-not-appear.html)
- [Die Produktexport-Datei wird nicht in Admin angezeigt.](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-9/mdva-31168-magento-patch-product-export-file-does-not-show-in-admin.html)
- [Problem beim Exportieren von Bestellungen im CSV-Format](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-8/mdva-31242-magento-patch-issue-in-exporting-orders-in-csv-format.html)
