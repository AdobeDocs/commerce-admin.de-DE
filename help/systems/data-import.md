---
title: Daten importieren
description: Erfahren Sie mehr über die Richtlinien für den Datenimport und die Verwendung der Datenimportierungsvorgänge.
exl-id: caae8811-445e-49d4-aa90-226a355732bc
feature: Products, Customers, Data Import/Export
source-git-commit: 1c1327dbda76283ae28f761d1e523e049e0e492f
workflow-type: tm+mt
source-wordcount: '1504'
ht-degree: 0%

---

# Daten importieren

Daten für alle Produktarten können in den Store importiert werden. Darüber hinaus können Sie Produkte, erweiterte Preisdaten, Kundendaten, Kundenadressen und Produktbilder importieren. Import unterstützt die folgenden Vorgänge:

- Hinzufügen/Aktualisieren
- Ersetzen
- Löschen

## Importrichtlinien

### Neue Entitäten

- Entitäten werden mit den in der CSV-Datei angegebenen Attributwerten hinzugefügt.
- Für ein erforderliches Attribut ohne festgelegten Standardwert kann die Entität (die entsprechende(n) Zeile(n)) nicht importiert werden, wenn kein Wert oder ein ungültiger Wert vorhanden ist.
- Für ein erforderliches Attribut mit einem Standardwert wird die Entität (die entsprechende(n) Zeile(n)) importiert und der Standardwert für das Attribut festgelegt, wenn kein Wert oder ein ungültiger Wert vorhanden ist.
- Wenn die komplexen Daten nicht gültig sind, kann die Entität (die entsprechende(n) Zeile(n)) nicht importiert werden.

### Bestehende Entitäten

- Bei Attributen, die keine komplexen Daten sind, ersetzen die Werte aus der Importdatei, einschließlich der leeren Werte für die nicht erforderlichen Attribute, die vorhandenen Werte.
- Wenn für ein erforderliches Attribut kein Wert vorhanden ist oder ein nicht gültiger Wert vorhanden ist, wird der vorhandene Wert nicht ersetzt.
- Wenn die komplexen Daten für die Entität ungültig sind, kann die Entität (die entsprechende(n) Zeile(n)) nicht importiert werden. Eine Ausnahme bildet der Fall, wenn im Dropdown-Menü &quot;Importverhalten&quot;die Option Entitäten löschen ausgewählt wurde.

### Komplexe Daten

Wenn ein in der Importdatei angegebenes Attribut vorhanden ist und sein Wert aus einem definierten Wertesatz abgeleitet wird, gilt Folgendes:

- Wenn der Wert nicht bereits im definierten Satz von Werten enthalten ist, kann die Zeile importiert werden und für das Attribut wird, sofern definiert, ein Standardwert festgelegt.
- Wenn der Wert bereits im definierten Satz enthalten ist, kann die entsprechende Zeile nicht importiert werden.
- Wenn die Importdatei einen Attributnamen angibt, der noch nicht im System definiert ist, wird er nicht erstellt und die entsprechenden Werte werden nicht importiert.

### Ungültige Dateien

- Eine Datei kann nicht importiert werden, wenn alle Zeilen ungültig sind.
- In der Importdatei werden nicht vorhandene Dienstdaten oder komplexe Datennamen angegeben, z. B. eine Spalte mit der Überschrift `_<non-existing name>` .

Der Importprozess von Adobe Commerce erkennt möglicherweise in UTF-8 kodierte Dateien, die eine Byte Order Mark (BOM) verwenden, nicht ordnungsgemäß. Dateien, die ein BOM enthalten, können während des Importvorgangs zu Problemen oder Fehlern führen.

## Importvorgänge

| Vorgang | Beschreibung |
| --------- | ----------- |
| Hinzufügen/Aktualisieren | Zu den vorhandenen Produktdaten für die vorhandenen Einträge in der Datenbank werden neue Produktdaten hinzugefügt. Alle Felder mit Ausnahme von `sku` können aktualisiert werden.<br><br>Neue in den Importdaten angegebene Steuerklassen werden automatisch erstellt.<br><br>Neue Produktkategorien, die in der Importdatei angegeben sind, werden automatisch erstellt.<br><br>Neue SKUs, die in der Importdatei angegeben sind, werden automatisch erstellt <br><br>**_Hinweis:_**Für Produkte können Sie alle Felder außer SKU durch Importieren aktualisieren.<br><br>**_Wichtig:_** Mehrere Feldwerte wie Websites oder Kategorien können nicht mit dem Importverhalten _Hinzufügen/Aktualisieren_ entfernt werden. Diese Felder bleiben nach dem Import in der Datenbank, wenn sie nicht in der CSV-Datei aufgeführt sind. |
| Ersetzen | Die vorhandenen Produktdaten werden durch neue Daten ersetzt.<br><br>**_Wichtig:_**Gehen Sie beim Ersetzen von Daten vorsichtig vor, da die vorhandenen Produktdaten gelöscht werden und alle Verweise im System verloren gehen.<br><br>Wenn eine SKU in den Importdaten mit der SKU einer vorhandenen Entität übereinstimmt, werden alle Felder, einschließlich der SKU, gelöscht und mithilfe der CSV-Daten wird ein neuer Datensatz erstellt. Ein Fehler tritt auf, wenn die CSV-Datei auf eine SKU verweist, die nicht in der Datenbank vorhanden ist. Sie können die Option Daten zur Anzeige eines Fehlers überprüfen. |
| Löschen | Alle Entitäten in den Importdaten, die in der Datenbank vorhanden sind, werden aus der Datenbank gelöscht.<br><br>Beim Löschen werden alle Spalten in den Importdaten außer der SKU ignoriert. Sie können alle anderen Attribute in den Daten ignorieren.<br><br>Es tritt ein Fehler auf, wenn die CSV-Datei auf eine SKU verweist, die nicht in der Datenbank vorhanden ist. Sie können die Option Daten zur Anzeige eines Fehlers überprüfen. |

{style="table-layout:auto"}

## Importprozess

Die Größe der Importdatei wird durch die Einstellungen in der Datei `php.ini` auf dem Server bestimmt. Die Systemmeldung auf der Seite _Import_ gibt die aktuelle Größenbeschränkung an. Die Standardgröße beträgt 2 MB.

Sonderzeichen (wie Gleichheitszeichen, Größer- und Kleiner-als-Symbole, einfache und doppelte Anführungszeichen, umgekehrter Schrägstrich, senkrechte Strich und Und-Zeichen) können Probleme bei der Datenübertragung verursachen. Um sicherzustellen, dass solche Sonderzeichen korrekt interpretiert werden, können sie als _Escape-Sequenz_ markiert werden. Wenn die Daten beispielsweise eine Textzeichenfolge wie `code="str"` oder `code="str2"` enthalten, stellt die Wahl, den Text in doppelte Anführungszeichen zu setzen, sicher, dass die ursprünglichen doppelten Anführungszeichen als Teil der Daten verstanden werden. Wenn das System auf einen doppelten Satz doppelter Anführungszeichen trifft, versteht es, dass der äußere Satz doppelter Anführungszeichen die tatsächlichen Daten umschließt.

Beim Importieren von Produktdaten werden neue Produktdaten zu vorhandenen Produktdateneinträgen in der Datenbank hinzugefügt. Alle Felder mit Ausnahme der SKU können durch den Import aktualisiert werden. Alle vorhandenen Produktdaten werden durch die importierten neuen Daten ersetzt. Gehen Sie beim Ersetzen von Daten vorsichtig vor. Alle vorhandenen Produktdaten werden gelöscht und alle Verweise im System gehen verloren.

![Datenimport](./assets/import-options.png){width="600" zoomable="yes"}

### Schritt 1: Vorbereiten der Daten

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**.

1. Legen Sie unter _Importeinstellungen_ **[!UICONTROL Entity Type]** eine der folgenden Einstellungen fest:

   - `Advanced Pricing`
   - `Products`
   - `Customer Finances`
   - `Customers and Addresses`
   - `Customers Main File`
   - `Customer Addresses`
   - `Stock Sources`

1. Klicken Sie auf **[!UICONTROL Download Sample File]**.

1. Suchen Sie die Exportdatei im Speicherort für Downloads Ihres Webbrowsers und öffnen Sie die Datei.

   Die Beispieldatei enthält Spaltenüberschriften mit Platzhalterdaten für die Produkttypen.

   ![Import data sample file](./assets/data-export-sample-data.png){width="600" zoomable="yes"}

1. Untersuchen Sie die Struktur der Beispieldatei und bereiten Sie mit ihr Ihre CSV-Importdatei vor, um sicherzustellen, dass die Spaltenüberschriften richtig geschrieben sind.

1. Vergewissern Sie sich, dass die Größe Ihrer Importdatei die in der Nachricht angegebene Grenze nicht überschreitet.

   ![Benachrichtigung über die Datenimportgröße](./assets/data-import-size-notification.png){width="600"}

1. Wenn die Importdaten Pfade zu Produktbildern enthalten, stellen Sie sicher, dass die Bilddateien an den entsprechenden Speicherort hochgeladen wurden.

   Der Standardspeicherort auf dem Commerce-Server lautet: `pub/media/import`.

   Wenn sich die Bilder auf einem externen Server befinden, stellen Sie sicher, dass Sie über die vollständige URL zu dem Verzeichnis verfügen, das die Bilder enthält.

### Schritt 2: Importverhalten auswählen

![Verhalten beim Datenimport](./assets/data-import-import-behavior.png){width="600" zoomable="yes"}

1. Setzen Sie **[!UICONTROL Import Behavior]** auf einen der folgenden Werte:

   - `Add/Update` (Bei Produkten können Sie alle Felder außer SKU durch Import aktualisieren.)
   - `Replace`
   - `Delete`

1. Wählen Sie eine der folgenden Optionen aus, um festzustellen, was beim Datenimport passiert, wenn ein Fehler auftritt:

   - `Stop on Error`
   - `Skip error entries`

1. Geben Sie für &quot;**[!UICONTROL Allowed Errors Count]**&quot;die Anzahl der Fehler an, die auftreten können, bevor der Import abgebrochen wird.

   Der Standardwert ist 10.

1. Akzeptieren Sie den Standardwert eines Kommas (`,`) für **[!UICONTROL Field separator]**.

1. Akzeptieren Sie den Standardwert eines Kommas (`,`) für **[!UICONTROL Multiple value separator]**.

   In einer CSV-Datei ist ein Komma das Standardtrennzeichen. Um ein anderes Zeichen zu verwenden, stellen Sie sicher, dass die Daten in der CSV-Datei mit dem von Ihnen angegebenen Zeichen übereinstimmen.

1. Den Standardwert `_EMPTY_VALUE_` für **[!UICONTROL Empty attribute value constant]** akzeptieren.

1. Wenn Sie Sonderzeichen einschließen möchten, die möglicherweise in den Daten als _Escape-Sequenz_ enthalten sind, aktivieren Sie das Kontrollkästchen **[!UICONTROL Fields Enclosure]** .

### Schritt 3: Importdatei identifizieren

![Datei für den Datenimport](./assets/data-import-file-to-import.png){width="600" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Choose File]** , um die zu importierende Datei auszuwählen.

1. Suchen Sie die CSV-Datei, die Sie für den Import vorbereitet haben, und klicken Sie auf **[!UICONTROL Open]**.

1. Geben Sie für &quot;**[!UICONTROL Images File Directory]**&quot;den relativen Pfad zum Speicherort auf dem Commerce-Server ein, auf dem hochgeladene Bilder gespeichert werden.

   Beispiel: `product_images`.

   >[!NOTE]
   >
   >Ab der Adobe Commerce- und Magento Open Source `2.3.2`-Version verkettet der in _[!UICONTROL Images File Directory]_angegebene Pfad den Import in das Basisverzeichnis der Bilder: `<Magento-root-folder>/var/import/images`. Platzieren Sie beispielsweise die Dateien &quot;`product_images`&quot;im Ordner &quot;`<Magento-root-directory>/var/import/images/product_images`&quot;. Der Basisordner für Importbilder kann in der Datei `\Magento\ImportExport\etc\config.xml` konfiguriert werden. Wenn das Remote-Speichermodul aktiviert ist, importieren Sie Dateien in den Ordner &quot;`<remote-storage-root-directory>/var/import/images/product_images`&quot;.

   Weitere Informationen zum Importieren von Produktbildern finden Sie unter [Importieren von Produktbildern](data-import-product-images.md).

### Schritt 4: Überprüfen der Importdaten

1. Klicken Sie in der oberen rechten Ecke auf **[!UICONTROL Check Data]**.

1. Warten Sie kurz, bis der Validierungsprozess abgeschlossen ist.

   Wenn die Importdaten gültig sind, wird die folgende Meldung angezeigt:

   ![Erfolgsmeldung - Datei ist gültig](./assets/data-import-validation-message.png){width="600"}

1. Wenn die Datei gültig ist, klicken Sie auf **[!UICONTROL Import]**.

   Korrigieren Sie andernfalls jedes Problem mit den in der Nachricht aufgelisteten Daten und versuchen Sie erneut, die Datei zu importieren.

1. Der Importvorgang läuft bis zum Ende der Daten, es sei denn, es wird ein Fehler festgestellt.

   Wenn in den Überprüfungsergebnissen eine Fehlermeldung angezeigt wird, korrigieren Sie das Problem in den Daten und importieren Sie die Datei erneut.

   ![Fehlermeldung - URL-Schlüssel ist bereits vorhanden](./assets/data-import-validation-error-url-key-exists.png){width="600"}

   Nach Abschluss des Imports wird eine Meldung angezeigt.

## Importverlauf

Commerce führt einen Datensatz mit in Ihren Store importierten Daten, einschließlich Startzeit, Benutzer, Ausführungszeit und Link zur importierten Datei. Die _Ausführungszeit_ ist die Dauer des Importvorgangs.

**_Anzeigen des Importverlaufs:_**

Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import History]**.

![Datenimport-Verlauf](./assets/data-import-history.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Standardmäßig befinden sich die Importverlauf-Dateien im Ordner &quot;`<Magento-root-directory>/var/import_history`&quot;. Wenn das Remote-Speichermodul aktiviert ist, befinden sich die Importverlauf-Dateien im Ordner &quot;`<remote-storage-root-directory>/import_export/import_history`&quot;.

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL ID] | Interne Nummer, die zur Bezeichnung einer Übertragung verwendet wird. |
| [!UICONTROL Start Date & Time] | Datum und Uhrzeit der Übertragung. |
| [!UICONTROL User] | Der Kunde, der den Transfer vorgenommen hat. |
| [!UICONTROL Imported file] | Link zum Herunterladen der importierten Datei. |
| [!UICONTROL Error file] | Die entsprechende Fehlerdatei. |
| [!UICONTROL Execution Time] | Zeitintervall des Importvorgangs. |
| [!UICONTROL Summary] | Die Anzahl der erstellten, aktualisierten und gelöschten Elemente oder die Fehlermeldung. |

{style="table-layout:auto"}

Um die Datei _Importiert/Fehler_ herunterzuladen, klicken Sie auf **[!UICONTROL Download]**.
