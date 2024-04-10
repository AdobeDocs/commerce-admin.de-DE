---
title: Daten importieren
description: Erfahren Sie mehr über Datenimportrichtlinien und die Verwendung von Datenimportvorgängen.
exl-id: caae8811-445e-49d4-aa90-226a355732bc
feature: Products, Customers, Data Import/Export
source-git-commit: 1c1327dbda76283ae28f761d1e523e049e0e492f
workflow-type: tm+mt
source-wordcount: '1504'
ht-degree: 0%

---

# Daten importieren

Daten für alle Produkttypen können in den Store importiert werden. Darüber hinaus können Sie Produkte, erweiterte Preisdaten, Kundendaten, Kundenadressdaten und Produktbilder importieren. Der Import unterstützt die folgenden Vorgänge:

- Hinzufügen/Aktualisieren
- Ersetzen
- Löschen

## Importrichtlinien

### Neue Entitäten

- Entitäten werden mit den in der CSV-Datei angegebenen Attributwerten hinzugefügt.
- Für ein erforderliches Attribut ohne festgelegten Standardwert kann die Entität (die entsprechende Zeile oder Zeilen) nicht importiert werden, wenn kein Wert oder ein ungültiger Wert vorhanden ist.
- Für ein erforderliches Attribut mit einem festgelegten Standardwert wird die Entität (die entsprechende Zeile oder Zeilen) importiert und der Standardwert wird für das Attribut festgelegt, wenn kein Wert oder ein ungültiger Wert vorhanden ist.
- Wenn die komplexen Daten ungültig sind, kann die Entität (die entsprechende Zeile oder Zeilen) nicht importiert werden.

### Vorhandene Entitäten

- Bei Attributen, die keine komplexen Daten sind, ersetzen die Werte aus der Importdatei, einschließlich der leeren Werte für die nicht erforderlichen Attribute, die vorhandenen Werte.
- Wenn für ein erforderliches Attribut kein Wert oder ein ungültiger Wert vorhanden ist, wird der vorhandene Wert nicht ersetzt.
- Wenn die komplexen Daten für die Entität ungültig sind, kann die Entität (die entsprechende Zeile bzw. die entsprechenden Zeilen) nicht importiert werden. Eine Ausnahme bildet der Fall, wenn im Dropdown-Menü Importverhalten die Option Entitäten löschen ausgewählt wurde.

### Komplexe Daten

Wenn ein in der Importdatei angegebenes Attribut vorhanden ist und sein Wert aus einem definierten Satz von Werten abgeleitet wird, gilt Folgendes:

- Wenn der Wert nicht bereits in dem definierten Wertesatz enthalten ist, kann die Zeile importiert werden und für das Attribut wird, falls definiert, ein Standardwert festgelegt.
- Wenn der Wert bereits im definierten Satz enthalten ist, kann die entsprechende Zeile nicht importiert werden.
- Wenn die Importdatei einen Attributnamen angibt, der noch nicht im System definiert ist, wird er nicht erstellt und seine Werte werden nicht importiert.

### Ungültige Dateien

- Eine Datei kann nicht importiert werden, wenn alle Zeilen ungültig sind.
- Ein nicht vorhandener Service-Daten- oder komplexer Datenname wird in der Importdatei angegeben, z. B. eine Spalte mit einem `_<non-existing name>` Überschrift.

Der Importvorgang von Adobe Commerce erkennt in UTF-8 kodierte Dateien, die eine Bytereihenfolgemarkierung (Byte Order Mark, BOM) verwenden, möglicherweise nicht ordnungsgemäß. Dateien, die eine Stückliste enthalten, können zu Problemen oder Fehlern während des Importvorgangs führen.

## Importvorgänge

| Vorgang | Beschreibung |
| --------- | ----------- |
| Hinzufügen/Aktualisieren | Zu den vorhandenen Produktdaten für die vorhandenen Einträge in der Datenbank werden neue Produktdaten hinzugefügt. Alle Felder außer `sku` kann aktualisiert werden.<br><br>Neue Steuerklassen, die in den Importdaten angegeben sind, werden automatisch erstellt.<br><br>Neue Produktkategorien, die in der Importdatei angegeben sind, werden automatisch erstellt.<br><br>Neue SKUs, die in der Importdatei angegeben sind, werden automatisch erstellt <br><br>**_Hinweis:_**Bei Produkten können Sie alle Felder außer SKU durch Import aktualisieren.<br><br>**_Wichtig:_** Mehrere Feldwerte, z. B. Websites oder Kategorien, können nicht mit dem _Hinzufügen/Aktualisieren_ Importverhalten. Diese Felder bleiben nach dem Import in der Datenbank, wenn sie nicht in der CSV-Datei aufgeführt sind. |
| Ersetzen | Die vorhandenen Produktdaten werden durch neue Daten ersetzt.<br><br>**_Wichtig:_**Gehen Sie beim Ersetzen von Daten vorsichtig vor, da die vorhandenen Produktdaten gelöscht werden und alle Verweise im System verloren gehen.<br><br>Wenn eine SKU in den Importdaten mit der SKU einer vorhandenen Entität übereinstimmt, werden alle Felder, einschließlich der SKU, gelöscht und mithilfe der CSV-Daten wird ein neuer Datensatz erstellt. Ein Fehler tritt auf, wenn die CSV-Datei auf eine SKU verweist, die nicht in der Datenbank vorhanden ist. Sie können Daten überprüfen, um den Fehler anzuzeigen. |
| Löschen | Alle Entitäten in den Importdaten, die in der Datenbank vorhanden sind, werden aus der Datenbank gelöscht.<br><br>Beim Löschen werden alle Spalten in den Importdaten mit Ausnahme der SKU ignoriert. Sie können alle anderen Attribute in den Daten ignorieren.<br><br>Ein Fehler tritt auf, wenn die CSV-Datei auf eine SKU verweist, die nicht in der Datenbank vorhanden ist. Sie können Daten überprüfen, um den Fehler anzuzeigen. |

{style="table-layout:auto"}

## Importvorgang

Die Größe der Importdatei wird durch die Einstellungen im Dialogfeld `php.ini` Datei auf dem Server. Die Systemmeldung auf dem _importieren_ gibt die aktuelle Größenbeschränkung an. Die Standardgröße ist 2 MB.

Sonderzeichen (z. B. Gleichheitszeichen, Größer-und-Kleiner-Zeichen, einfache und doppelte Anführungszeichen, umgekehrte Schrägstriche, senkrechte Striche und kaufmännische Und-Zeichen) können bei der Datenübertragung zu Problemen führen. Um sicherzustellen, dass solche Sonderzeichen korrekt interpretiert werden, können sie als _Escapesequenz_. Wenn die Daten beispielsweise eine Zeichenfolge wie enthalten `code="str"`, `code="str2"`Wenn Sie sich jedoch dafür entscheiden, den Text in doppelte Anführungszeichen zu setzen, wird sichergestellt, dass die ursprünglichen doppelten Anführungszeichen als Teil der Daten verstanden werden. Wenn das System auf doppelte Anführungszeichen trifft, versteht es, dass der äußere Satz doppelter Anführungszeichen die tatsächlichen Daten einschließt.

Beim Importieren von Produktdaten werden neue Produktdaten zu vorhandenen Produktdateneinträgen in der Datenbank hinzugefügt. Alle Felder außer SKU können durch Import aktualisiert werden. Alle vorhandenen Produktdaten werden durch die importierten neuen Daten ersetzt. Gehen Sie beim Ersetzen von Daten mit Vorsicht vor. Alle vorhandenen Produktdaten werden gelöscht und alle Verweise im System gehen verloren.

![Datenimport](./assets/import-options.png){width="600" zoomable="yes"}

### Schritt 1: Daten vorbereiten

1. Auf der _Admin_ Seitenleiste, zu gehen **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**.

1. Unter _Importeinstellungen_, festlegen **[!UICONTROL Entity Type]** eine der folgenden Möglichkeiten:

   - `Advanced Pricing`
   - `Products`
   - `Customer Finances`
   - `Customers and Addresses`
   - `Customers Main File`
   - `Customer Addresses`
   - `Stock Sources`

1. Klick **[!UICONTROL Download Sample File]**.

1. Suchen Sie die Exportdatei am Downloads-Speicherort für Ihren Webbrowser und öffnen Sie die Datei .

   Die Beispieldatei enthält Spaltenüberschriften mit Platzhalterdaten für die Produkttypen.

   ![Beispieldatei für Daten importieren](./assets/data-export-sample-data.png){width="600" zoomable="yes"}

1. Untersuchen Sie die Struktur der Beispieldatei und verwenden Sie sie, um Ihre CSV-Importdatei vorzubereiten und sicherzustellen, dass die Spaltenüberschriften korrekt geschrieben sind.

1. Stellen Sie sicher, dass die Größe der Importdatei nicht das in der Meldung angezeigte Limit überschreitet.

   ![Benachrichtigung zur Datenimportgröße](./assets/data-import-size-notification.png){width="600"}

1. Wenn die Importdaten Pfade zu Produktbildern enthalten, stellen Sie sicher, dass die Bilddateien an den entsprechenden Speicherort hochgeladen wurden.

   Der Standardspeicherort auf dem Commerce-Server lautet: `pub/media/import`.

   Wenn sich die Bilder auf einem externen Server befinden, stellen Sie sicher, dass Sie über die vollständige URL zu dem Verzeichnis verfügen, das die Bilder enthält.

### Schritt 2: Importverhalten auswählen

![Verhalten beim Datenimport](./assets/data-import-import-behavior.png){width="600" zoomable="yes"}

1. set **[!UICONTROL Import Behavior]** eine der folgenden Möglichkeiten:

   - `Add/Update` (Für Produkte können Sie alle Felder außer SKU durch Import aktualisieren.)
   - `Replace`
   - `Delete`

1. Um zu bestimmen, was passiert, wenn beim Importieren von Daten ein Fehler auftritt, wählen Sie eine der folgenden Optionen:

   - `Stop on Error`
   - `Skip error entries`

1. für **[!UICONTROL Allowed Errors Count]**, geben Sie die Anzahl der Fehler ein, die auftreten können, bevor der Import abgebrochen wird.

   Der Standardwert ist 10.

1. Akzeptieren Sie den Standardwert eines Kommas (`,`) für **[!UICONTROL Field separator]**.

1. Akzeptieren Sie den Standardwert eines Kommas (`,`) für **[!UICONTROL Multiple value separator]**.

   In einer CSV-Datei ist ein Komma das Standardtrennzeichen. Wenn Sie ein anderes Zeichen verwenden möchten, stellen Sie sicher, dass die Daten in der CSV-Datei mit dem angegebenen Zeichen übereinstimmen.

1. Akzeptieren des Standardwerts `_EMPTY_VALUE_` für **[!UICONTROL Empty attribute value constant]**.

1. Wenn Sie alle Sonderzeichen, die möglicherweise in den Daten enthalten sind, als _Escapesequenz_, wählen Sie die **[!UICONTROL Fields Enclosure]** Kontrollkästchen.

### Schritt 3: Importdatei identifizieren

![Datenimportdatei](./assets/data-import-file-to-import.png){width="600" zoomable="yes"}

1. Klick **[!UICONTROL Choose File]** , um die zu importierende Datei auszuwählen.

1. Suchen Sie die CSV-Datei, die Sie importiert haben, und klicken Sie auf **[!UICONTROL Open]**.

1. für **[!UICONTROL Images File Directory]**, geben Sie den relativen Pfad zum Speicherort des hochgeladenen Bildes auf dem Commerce-Server ein.

   Beispiel: `product_images`.

   >[!NOTE]
   >
   >Beginnen mit der Adobe Commerce und der Magento Open Source `2.3.2` Release, der in angegebene Pfad _[!UICONTROL Images File Directory]_Verkettet für den Import in das Basisverzeichnis der Bilder: `<Magento-root-folder>/var/import/images`. Platzieren Sie beispielsweise `product_images` Dateien in der `<Magento-root-directory>/var/import/images/product_images` Ordner. Der Basisordner für den Import von Bildern kann in der `\Magento\ImportExport\etc\config.xml` -Datei. Wenn das Remote-Speichermodul aktiviert ist, importieren Sie Dateien in die `<remote-storage-root-directory>/var/import/images/product_images` Ordner.

   Weitere Informationen zum Importieren von Produktbildern finden Sie unter [Importieren von Produktbildern](data-import-product-images.md).

### Schritt 4: Importdaten überprüfen

1. Klicken Sie oben rechts auf **[!UICONTROL Check Data]**.

1. Warten Sie einige Augenblicke, bis der Validierungsprozess abgeschlossen ist.

   Wenn die Importdaten gültig sind, wird die folgende Meldung angezeigt:

   ![Erfolgsmeldung - Datei ist gültig](./assets/data-import-validation-message.png){width="600"}

1. Wenn die Datei gültig ist, klicken Sie auf **[!UICONTROL Import]**.

   Korrigieren Sie andernfalls jedes Problem mit den in der Nachricht aufgelisteten Daten und versuchen Sie erneut, die Datei zu importieren.

1. Der Importvorgang wird bis zum Ende der Daten fortgesetzt, es sei denn, es tritt ein Fehler auf.

   Wenn in den Validierungsergebnissen eine Fehlermeldung angezeigt wird, beheben Sie das Problem in den Daten und importieren Sie die Datei erneut.

   ![Fehlermeldung - URL-Schlüssel existiert bereits](./assets/data-import-validation-error-url-key-exists.png){width="600"}

   Nach Abschluss des Imports wird eine Meldung angezeigt.

## Importverlauf

Commerce verwaltet einen Datensatz mit Daten, die in Ihren Store importiert wurden, einschließlich Startdatum und -zeit, Benutzer, Ausführungszeit und einem Link zur importierten Datei. Die _Ausführungszeit_ ist die Dauer des Importvorgangs.

**_Anzeigen des Importverlaufs:_**

Auf der _Admin_ Seitenleiste, zu gehen **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import History]**.

![Datenimportverlauf](./assets/data-import-history.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Standardmäßig befinden sich Importverlaufsdateien im `<Magento-root-directory>/var/import_history` Ordner. Wenn das Remote-Speichermodul aktiviert ist, befinden sich die Importverlaufsdateien in der `<remote-storage-root-directory>/import_export/import_history` Ordner.

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL ID] | Eine interne Nummer, die eine Übertragung bezeichnet. |
| [!UICONTROL Start Date & Time] | Ein bestimmtes Datum und eine bestimmte Uhrzeit für die Übertragung. |
| [!UICONTROL User] | Der Kunde, der die Übertragung vorgenommen hat. |
| [!UICONTROL Imported file] | Link zum Herunterladen der importierten Datei. |
| [!UICONTROL Error file] | Die entsprechende Fehlerdatei. |
| [!UICONTROL Execution Time] | Zeitintervall des Importvorgangs. |
| [!UICONTROL Summary] | Anzahl der erstellten, aktualisierten und gelöschten Elemente oder Fehlermeldung. |

{style="table-layout:auto"}

So laden Sie das _importiert/Fehler_ Datei, klicken Sie auf **[!UICONTROL Download]**.
