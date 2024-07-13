---
title: CSV-Datendateien
description: Erfahren Sie mehr über die Struktur, die in CSV-Dateien zum Importieren und Exportieren von Daten verwendet wird.
exl-id: 86e362af-2af7-4557-ac49-1efad2f0e976
feature: Products, Customers, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '713'
ht-degree: 0%

---

# CSV-Datendateien

Das CSV-Dateiformat (CSV) dient als Grundlage für Datenübertragungsvorgänge und wird von allen Tabellen- und Datenbankanwendungen unterstützt. Die folgenden Dateitypen werden für den Import und Export unterstützt:

- Import: `CSV` und `ZIP` (eine komprimierte CSV-Datei)
- Export: `CSV`

>[!IMPORTANT]
>
>Es wird empfohlen, ein Programm zu verwenden, das UTF-8-Kodierung unterstützt, z. B. Notepad++, um CSV-Dateien zu bearbeiten. Microsoft® Excel fügt zusätzliche Zeichen in die Spaltenüberschrift der CSV-Datei ein, wodurch verhindert werden kann, dass die Daten wieder in Commerce importiert werden. Wenn Sie mit Mac arbeiten, können Sie Ihre Daten im CSV-Format (Windows) speichern.

CSV-Dateien weisen eine bestimmte Struktur auf, die mit der Datenbank übereinstimmen muss. Jede Spaltenüberschrift entspricht dem Attributcode des Felds, das durch die Spalte dargestellt wird. Um sicherzustellen, dass die Spaltenüberschriften von Commerce gelesen werden können, exportieren Sie zunächst die Daten aus Ihrem Store als CSV-Datei. Sie können die Daten dann bearbeiten und erneut in Commerce importieren.

Wenn Sie eine exportierte CSV-Datei in einem Texteditor öffnen, sehen Sie, dass Werte durch Kommas getrennt sind und mehrere Werte in doppelten Anführungszeichen gesetzt sind. Beim Import können Sie ein benutzerdefiniertes Trennzeichen angeben, obwohl standardmäßig ein Komma verwendet wird.

## Produkt-CSV-Struktur

Ein vollständiger Export der Produktdatenbank enthält Informationen zu den einzelnen Produkten im Katalog und die Beziehungen zwischen ihnen. Jeder Datensatz verfügt über eine feste Auswahl von Spalten, die den Attributen im Katalog entsprechen, obwohl die Reihenfolge der Attribute während des Importvorgangs ignoriert wird.

Die erste Zeile der Tabelle enthält die Namen der einzelnen Attribute, die als Spaltenüberschriften verwendet werden. Die übrigen Zeilen beschreiben die einzelnen Produktdatensätze. Jede Zeile, die mit einem Wert in der SKU-Spalte beginnt, ist der Anfang eines neuen Produktdatensatzes. Ein einzelnes Produkt kann mehrere Zeilen enthalten, die Informationen über mehrere Bilder oder Produktoptionen enthalten. Die nächste Zeile mit einem Wert in der SKU-Spalte beginnt mit einem neuen Produkt.

Die Spalte &quot;Kategorie&quot;enthält einen Pfad für jede Kategorie, der das Produkt zugewiesen ist. Der Pfad enthält die Stammkategorie, gefolgt von einem Schrägstrich (`/`) zwischen den einzelnen Ebenen. Standardmäßig wird das Komma `,` verwendet, um verschiedene Kategoriepfade zu trennen. (Sie können mit der Option _[!UICONTROL Multiple value separator]_ein anderes Trennzeichen angeben.) Beispiel:

`Default Category/Gear,Default Category/Gear/Bags`

Um Daten zu importieren, müssen Sie nur die SKU und alle Spalten mit Änderungen einschließen. Leere Spalten werden während des Importvorgangs ignoriert. Während des Importvorgangs können keine Attribute hinzugefügt werden. Sie können nur vorhandene Attribute einbeziehen.

Eine ausführliche Beschreibung der einzelnen Produktattribute finden Sie unter [Struktur der CSV-Produktdatei](data-attributes-product.md).

| Spaltenname | Beschreibung |
| ----------- | ----------- |
| `_<name>` | Spaltenüberschriften, die mit einem Unterstrich beginnen, enthalten Eigenschaften von Dienstentitäten oder komplexe Daten. Dienstspalten sind keine Produktattribute. |
| `<attribute_name>` | Spaltenüberschriften mit Attributcode oder Feldname geben die Datenspalte an. Eine Spalte kann ein Systemattribut oder ein vom Store-Administrator erstelltes Attribut darstellen. |

{style="table-layout:auto"}

## CSV-Struktur des Kunden

Die CSV-Datei des Kunden enthält Kundeninformationen aus der Datenbank und weist die folgende Struktur auf:

Die erste Zeile der Tabelle enthält die Namen der Attributspalten (die mit den Attributcodes identisch sind). Es gibt zwei Arten von Spaltennamen, wie in der folgenden Tabelle dargestellt. Andere Zeilen enthalten Attributwerte, Dienstdaten und komplexe Daten. Jede Zeile mit nicht leeren Werten in den Spalten `email` und `_website` beginnt mit der Beschreibung des nachfolgenden Kunden. Jede Zeile kann Kundendaten mit oder ohne Adressdaten oder nur die Adressdaten darstellen. Wenn eine Zeile nur die Adressdaten enthält, werden die Werte in den Spalten, die sich auf das Kundenprofil beziehen, ignoriert und können leer sein.

Um mehr als eine Adresse für einen Kunden hinzuzufügen oder zu ersetzen, fügen Sie für jede neue Adresse eine Zeile mit leeren Kundendaten und den neuen oder aktualisierten Adressdaten unterhalb der Kundendatenzeile hinzu.

Eine ausführliche Beschreibung der einzelnen Kundenattribute finden Sie unter [Struktur der CSV-Datei für Kunden](data-attributes-customer.md).

| Spaltenname | Beschreibung |
| ----------- | ----------- |
| `_<name>` | Spaltenüberschriften, die mit einem Unterstrich beginnen, enthalten Eigenschaften von Dienstentitäten oder komplexe Daten. Dienstspalten sind keine Kundenattribute. |
| `<attribute name>` | Die Namen der Spalten mit Werten von vom System erstellten Attributen und vom Store-Administrator erstellten Attributen. |

{style="table-layout:auto"}
