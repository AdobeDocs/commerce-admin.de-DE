---
title: Geplanter Import und Export
description: Erfahren Sie, wie Sie geplante Datenimport- und -exportiervorgänge verwalten.
exl-id: 74ba40f1-a540-4425-9500-2c730c1145e7
feature: Products, Customers, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '2378'
ht-degree: 0%

---

# Geplanter Import und Export

{{ee-feature}}

Geplante Importe und Exporte können täglich, wöchentlich oder monatlich ausgeführt werden. Die zu importierenden oder exportierenden Dateien können sich auf lokalen Adobe Commerce-Servern oder Remote-FTP-Servern befinden. Geplanter Import/Export ist standardmäßig implementiert und erfordert keine zusätzliche Konfiguration. Alle geplanten Importe und Exporte werden vom Cron-Auftragsplaner verwaltet.

## Zugriff auf geplanten Import/Export

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Scheduled Imports/Exports]**.

   ![Geplanter Datenimport/-export](./assets/data-scheduled-import-export.png){width="700" zoomable="yes"}

1. Um einen neuen geplanten Import- oder Exportauftrag zu erstellen, klicken Sie auf die entsprechende Schaltfläche und befolgen Sie die Anweisungen für den Typ des geplanten Auftrags.

   - [Geplanten Export hinzufügen](#schedule-an-export)
   - [Geplanten Import hinzufügen](#schedule-an-import)

1. Wenn der Datensatz gespeichert wird, wird der Auftrag im Raster _[!UICONTROL Scheduled Import/Export]_angezeigt.

   >[!NOTE]
   >
   >Wenn Sie einen geplanten Import/Export erstellen oder aktualisieren, ändert sich die Systemkonfiguration. Stellen Sie nach dem Speichern sicher, dass Sie den Hinweis zur Cache-Invalidierung bearbeiten, der oben auf der Admin-Seite angezeigt wird, und leeren Sie den Cache, um den neuen oder aktualisierten Zeitplan anzuwenden.

1. Nach jedem geplanten Auftrag wird eine Kopie der Datei im Ordner &quot;`var/log/import_export`&quot;auf dem lokalen Adobe Commerce-Server abgelegt.

   Die Details der einzelnen Vorgänge werden nicht in das Protokoll geschrieben. Wenn ein Fehler auftritt, wird eine Benachrichtigung über den fehlgeschlagenen Import-/Exportvorgang mit einer Fehlerbeschreibung gesendet.

## Import planen

Für das verfügbare Importdateiformat und die Typen von Importentitäten ähnelt der geplante Importprozess dem manuellen Importprozess:

- Die Importdatei sollte im .CSV-Format vorliegen.
- Sie können Produkt- und Kundendaten importieren

Der Vorteil des geplanten Imports besteht darin, dass Sie eine Datendatei automatisch mehrmals importieren können, nachdem Sie die Importparameter angegeben und nur einmal geplant haben.

Die Details der einzelnen Importvorgänge werden nicht in ein Protokoll geschrieben, aber bei einem Fehler erhalten Sie eine E-Mail mit der Fehlerbeschreibung _Import fehlgeschlagen_ . Das Ergebnis des letzten geplanten Importvorgangs wird in der Spalte Letztes Ergebnis auf der Seite Geplanter Import/Export angezeigt.

Nach jedem Importvorgang wird eine Kopie der Importdatei im Ordner &quot;`var/log/import_export`&quot;auf dem Server abgelegt, auf dem Adobe Commerce oder Magento Open Source bereitgestellt ist. Der Zeitstempel, die Markierung der importierten Entität (Produkte oder Kunden) und der Typ des Vorgangs (in diesem Fall Import) werden dem Namen der Importdatei hinzugefügt.

Nach jedem geplanten Importauftrag wird automatisch ein Neuindizierungsvorgang ausgeführt. Änderungen an den Beschreibungen und anderen Textinformationen werden nach der Aktualisierung der Daten in die Datenbank übernommen, und die Preisänderungen werden erst nach der Neuindizierung übernommen.

### Schritt 1: Abschließen der Importeinstellungen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Scheduled Import/Export]**.

1. Klicken Sie in der oberen rechten Ecke auf **[!UICONTROL Add Scheduled Import]**.

1. Legen Sie die Zeitplan- und Importoptionen fest:

   - **[!UICONTROL Name]** - Geben Sie einen Namen für den geplanten Import ein.

   - **[!UICONTROL Description]** - Geben Sie eine kurze Beschreibung ein, die den Zweck des Imports und seine Verwendung erklärt.

   - **[!UICONTROL Entity Type]** - Legen Sie einen der folgenden Werte fest:

      - `Products`
      - `Advanced Pricing`
      - `Customers and Addresses (single file)`
      - `Customer Addresses`
      - `Customer Finances`
      - `Customers Main File`
      - `Stock Sources`

   - **[!UICONTROL Import Behavior]** - Legen Sie einen der folgenden Werte fest:

      - `Add/Update Complex Data` - Fügt neue komplexe Daten zu den vorhandenen komplexen Daten für vorhandene Einträge in der Datenbank hinzu oder aktualisiert sie. Dies ist der Standardwert.
      - `Replace` - Schreibt den vorhandenen Komplex für vorhandene Entitäten in der Datenbank um.
      - `Delete Entities` - Löscht vorhandene Einträge in der Datenbank.
      - `Custom Action` - Passt vorhandene Entitäten in der Datenbank an.

     >[!NOTE]
     >
     >Für die Entitätstypen _[!UICONTROL Advanced Pricing]_,_[!UICONTROL Products]_, _[!UICONTROL Customers and Addresses (single file)]_und_[!UICONTROL Stock Sources]_ werden diese Importverhaltensweisen angezeigt: `Add/Update`, `Replace` und `Delete`. Für die Entitätstypen _Kundenfinanzierungen_, _Hauptdatei der Kunden_ und _Kunden und Adressen_ werden folgende Importverhalten angezeigt: `Add/Update Complex Data`, `Delete Entities` und `Custom Action`.

   - **[!UICONTROL Start Time]** - Stellen Sie auf die Stunde, Minute und Sekunde ein, in der der Import beginnen soll.

   - **[!UICONTROL Frequency]** - Wird auf einen der folgenden Werte gesetzt: `Daily`, `Weekly` oder `Monthly`

   - **[!UICONTROL On Error]** - Legen Sie einen der folgenden Werte fest: `Stop Import` oder `Continue Processing`

   - **[!UICONTROL Status]** - Um den geplanten Import zu aktivieren, setzen Sie auf `Enabled`.

   - **[!UICONTROL Field Separator]** - Geben Sie das Zeichen ein, das zum Trennen von Feldern in der Importdatei verwendet wird. Das Standardzeichen ist ein Komma.

   - **[!UICONTROL Multiple Value Separator]** - Geben Sie das Zeichen ein, das verwendet wird, um mehrere Werte in einem Feld zu trennen.

   ![Datenimport - Geplante Importeinstellungen](./assets/data-transfer-scheduled-import-settings.png){width="600" zoomable="yes"}

### Schritt 2: Ausfüllen der Importdatei-Informationen

1. Setzen Sie **[!UICONTROL Server Type]** auf einen der folgenden Werte:

   - `Local Server` - Importiert die Daten von demselben Server, auf dem Adobe Commerce installiert ist.
   - `Remote FTP` - Importiert die Daten von einem Remote-Server.

   ![Datenimport - Informationen zur geplanten Importdatei](./assets/data-transfer-scheduled-import-file-information.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Wenn das Remote-Speichermodul aktiviert ist, wechselt `Local Server` automatisch zu `Remote Storage`.

1. Geben Sie den Wert **[!UICONTROL File Directory]** ein, aus dem die Importdatei stammt.

   - `Local Server` - Geben Sie einen relativen Pfad in die Commerce-Installation ein. Beispiel: `var/import`. Wenn das Remote-Speichermodul konfiguriert ist, verwenden Sie `import_export/import`.
   - `Remote FTP server` - Geben Sie die vollständige URL und den Pfad zum Importordner auf dem Remote-Server ein.

1. Geben Sie den zu importierenden **[!UICONTROL File Name]** ein.

1. Geben Sie für &quot;**[!UICONTROL Images File Directory]**&quot;den Pfad zu dem Ordner ein, in dem Produktbilder gespeichert werden.

   Geben Sie auf einem lokalen Server einen relativen Pfad ein, z. B.: `var/import`. Geben Sie auf einem Remote-Speicher einen relativen Pfad ein, z. B.: `import_export/import` oder `import_export/import/some/dir`.

### Schritt 3: Konfigurieren des Imports fehlgeschlagener E-Mails

![Datenimport - fehlgeschlagener Import fehlgeschlagener E-Mails](./assets/data-transfer-scheduled-import-email-fail.png){width="600" zoomable="yes"}

1. Setzen Sie **[!UICONTROL Failed Email Receiver]** auf den Store-Kontakt, der eine Benachrichtigung erhalten soll, wenn während des Imports ein Fehler auftritt.

1. Setzen Sie **[!UICONTROL Failed Email Sender]** auf den Store-Kontakt, der als Absender der Benachrichtigung angezeigt wird.

1. Setzen Sie **[!UICONTROL Failed Email Template]** auf die Vorlage, die für die Benachrichtigung verwendet wird.

1. Geben Sie für &quot;**[!UICONTROL Send Failed Email Copy To]**&quot; die E-Mail-Adresse eines Empfängers an, der eine Kopie der Benachrichtigung erhalten soll.

   Trennen Sie mehrere E-Mail-Adressen durch Kommas.

1. Setzen Sie **[!UICONTROL Failed Email Copy Method]** auf einen der folgenden Werte:

   - `Bcc` - Sendet eine blinde höfliche Kopie der fehlgeschlagenen Importbenachrichtigung. Der Name und die Adresse des Empfängers sind in der ursprünglichen E-Mail-Verteilung enthalten, jedoch nicht sichtbar.
   - `Separate Email` - Sendet eine Kopie der Benachrichtigung über den fehlgeschlagenen Import als separate E-Mail.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]**.

   Der neue geplante Importauftrag wird der Liste auf der Seite _[!UICONTROL Scheduled Import/Export]_hinzugefügt. Von dieser Seite aus kann sie sofort zum Testen und Bearbeiten ausgeführt werden. Die Importdatei wird vor der Ausführung jedes Importvorgangs validiert.

>[!NOTE]
>
>Wenn Sie einen geplanten Import/Export erstellen oder aktualisieren, ändert sich die Systemkonfiguration. Stellen Sie nach dem Speichern sicher, dass Sie den Hinweis zur Cache-Invalidierung bearbeiten, der oben auf der Admin-Seite angezeigt wird, und leeren Sie den Cache, um den neuen oder aktualisierten Zeitplan anzuwenden.

### Feldbeschreibungen

#### [!UICONTROL Import Settings]

| Feld | Beschreibung |
| ----- | ----------- | 
| [!UICONTROL Name] | Der Name des Imports. Hilft Ihnen, es zu unterscheiden, wenn viele verschiedene geplante Importe erstellt werden. |
| [!UICONTROL Description] | (Optional) Sie können eine Beschreibung eingeben. |
| [!UICONTROL Entity Type] | Definiert die zu importierenden Daten. |
| [!UICONTROL Import Behavior] | Definiert, wie komplexe Daten verarbeitet werden, wenn die importierten Entitäten in der Datenbank vorhanden sind. Zu den komplexen Daten für Produkte gehören Kategorien, Websites, benutzerdefinierte Optionen, Tier-Preise, zugehörige Produkte, Upsells, Querverkäufe und zugehörige Produktdaten. Komplexe Daten für Kunden enthalten Adressen. Optionen:<br>**[!UICONTROL Add/Update Complex Data]**- Die neuen komplexen Daten werden zu den vorhandenen komplexen Daten für vorhandene Einträge in der Datenbank hinzugefügt oder aktualisiert. Dies ist der Standardwert.<br>**[!UICONTROL Add/Update]** - Den vorhandenen Einträgen in der Datenbank werden neue Daten hinzugefügt. Alle Felder mit Ausnahme von `sku` können für Produkte aktualisiert werden. Alle nicht in der CSV-Datei aufgelisteten Feldwerte wie Kategorien oder Websites bleiben nach dem Import in der Datenbank.<br>**[!UICONTROL Replace]**- Die vorhandenen komplexen Daten für die vorhandenen Entitäten werden ersetzt.<br>**[!UICONTROL Delete Entities]** - Wenn importierte Entitäten in der Datenbank vorhanden sind, werden sie aus der Datenbank gelöscht.<br>**[!UICONTROL Custom Action]**- Die vorhandenen komplexen Entitäten werden während des Importvorgangs angepasst. |
| [!UICONTROL Start Time] | Legen Sie die Startzeit, Minuten und Sekunden des Imports fest. |
| [!UICONTROL Frequency] | Definieren Sie, wie oft der Import ausgeführt wird. Optionen: `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL On Error] | Definieren Sie das Systemverhalten für den Fall, dass bei der Dateivalidierung Fehler gefunden werden. Optionen:<br>**Import stoppen** - Die Datei wird nicht importiert, wenn bei der Validierung Fehler gefunden wurden. Dies ist der Standardwert.<br>**Verarbeitung fortsetzen** - Wenn bei der Validierung Fehler gefunden werden, aber ein Import möglich ist, wird die Datei importiert. |
| [!UICONTROL Status] | Der Import ist standardmäßig aktiviert. Sie können sie aussetzen, indem Sie den Status auf `Disabled` setzen. |
| [!UICONTROL Field Separator] | Bestimmt das Zeichen, das zum Trennen von Feldern verwendet wird. Standardwert: `,` (Komma) |
| [!UICONTROL Multiple Value Separator] | Bestimmt das Zeichen, das zum Trennen mehrerer Werte in einem Feld verwendet wird. Standardwert: `,` (Komma) |

{style="table-layout:auto"}

#### [!UICONTROL Import File Information]

| Feld | Beschreibung |
| ----- | ----------- | 
| [!UICONTROL Server Type] | Sie können eine Datei auf demselben Server importieren, auf dem Commerce bereitgestellt ist (wählen Sie &quot;`Local Server`&quot;), oder sie vom Remote-FTP-Server (wählen Sie &quot;`Remote FTP`&quot;) importieren. Wenn Sie &quot;_[!UICONTROL Remote FTP]_&quot;auswählen, werden zusätzliche Optionen für Anmeldedaten und Dateiübertragungseinstellungen angezeigt. Wenn das Remote-Speichermodul aktiviert ist, wird der Typ `Local Server` automatisch auf `Remote Storage` umgestellt. |
| [!UICONTROL File Directory] | Geben Sie den Ordner an, in dem sich die Importdatei befindet. Wenn &quot;Servertyp&quot;auf &quot;_[!UICONTROL Local Server]_&quot;festgelegt ist, geben Sie den Pfad relativ zum Commerce-Installationsordner an. Beispiel: `var/import` oder `import_export/import` für Remote-Speicher. |
| [!UICONTROL File Name] | Geben Sie den Namen der Importdatei an. |
| [!UICONTROL Images File Directory] | Geben Sie den Pfad zu dem Ordner ein, in dem Produktbilder gespeichert werden. Geben Sie für einen lokalen Server einen relativen Pfad ein. Beispiel: `var/import` oder `import_export/import` für Remote-Speicher. |

{style="table-layout:auto"}

#### [!UICONTROL Import Failed Emails]

| Feld | Beschreibung |
| ----- | ----------- | 
| [!UICONTROL Failed Email Receiver] | Geben Sie die E-Mail-Adresse an, an die eine E-Mail-Benachrichtigung (fehlgeschlagene Import-E-Mail) gesendet wird, wenn der Import fehlschlägt. |
| [!UICONTROL Failed Email Sender] | Geben Sie die E-Mail-Adresse an, die als Absender für die Import-fehlgeschlagene E-Mail verwendet wird. |
| [!UICONTROL Failed Email Template] | Wählen Sie eine Vorlage für die Import-E-Mail aus. Standardmäßig ist nur die Option Import fehlgeschlagen (Standardvorlage aus Gebietsschema) verfügbar. Benutzerdefinierte Vorlagen können unter _[!UICONTROL System]_>_[!UICONTROL Transactional Emails]_ erstellt werden. |
| [!UICONTROL Send Failed Email Copy To] | Die E-Mail-Adresse, an die eine Kopie der fehlgeschlagenen Importdatei gesendet wird. |
| [!UICONTROL Send Failed Email Copy Method] | Wählen Sie die Methode zum Kopieren des Versands für den Import der fehlgeschlagenen E-Mail aus. |

{style="table-layout:auto"}

## Export planen

Der geplante Export ähnelt einem manuellen [Export](data-export.md) im verfügbaren Exportdateiformat und den Typen von Entitäten, die exportiert werden können:

- Sie können in das CSV-Format exportieren
- Sie können Produkt- und Kundendaten exportieren

Der Vorteil der Verwendung von &quot;Geplanter Export&quot;besteht darin, dass Sie Daten nach Angabe der Exportparameter mehrmals automatisch exportieren und nur einmal planen können.

Die Details der einzelnen Exporte werden nicht in ein Protokoll geschrieben. Wenn jedoch ein Fehler auftritt, erhalten Sie eine E-Mail mit der Fehlerbeschreibung &quot;Export Failed&quot;(Export fehlgeschlagen). Das Ergebnis des letzten Exportvorgangs wird in der Spalte Letztes Ergebnis auf der Seite Geplantes Importieren/Exportieren angezeigt.

Nach jedem Export wird die Exportdatei am benutzerdefinierten Speicherort und eine Kopie im Ordner &quot;`var/log/import_export`&quot;auf dem Server abgelegt, auf dem Adobe Commerce oder Magento Open Source bereitgestellt ist. Der Zeitstempel und die Markierung der exportierten Entität (Produkte oder Kunden) sowie der Typ des Vorgangs (in diesem Fall Export) werden dem Namen der Exportdatei hinzugefügt.

### Schritt 1: Exporteinstellungen abschließen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Scheduled Import/Export]**.

1. Klicken Sie oben rechts auf **[!UICONTROL Add Scheduled Export]** und führen Sie folgende Schritte aus:

   - Geben Sie für den geplanten Export den Wert **[!UICONTROL Name]** ein.

   - Geben Sie einen kurzen **[!UICONTROL Description]** -Wert ein, der den Zweck des Exports und seine Verwendung erklärt.

   - Setzen Sie **[!UICONTROL Entity Type]** auf einen der folgenden Werte:

      - `Advanced Pricing`
      - `Products`
      - `Customer Financing`
      - `Customers Main File`
      - `Customer Addresses`
      - `Stock Sources`

     Der Abschnitt &quot;_[!UICONTROL Entity Attributes]_&quot;am unteren Rand der Seite wird aktualisiert und spiegelt den ausgewählten Entitätstyp wider.

   - Setzen Sie **[!UICONTROL Start Time]** auf die Stunde, Minute und Sekunde, in der der Export beginnen soll.

   - Setzen Sie **[!UICONTROL Frequency]** auf einen der folgenden Werte:

      - `Daily`
      - `Weekly`
      - `Monthly`

1. Um den geplanten Export zu aktivieren, setzen Sie **[!UICONTROL Status]** auf `Enabled`.

1. Akzeptieren Sie `CSV` als Standard-Wert **[!UICONTROL File Format]**.

   ![Geplante Exporteinstellungen](./assets/data-transfer-scheduled-export-settings.png){width="600" zoomable="yes"}

### Schritt 2: Ausfüllen der Exportdateiinformationen

1. Setzen Sie **[!UICONTROL Server Type]** auf einen der folgenden Werte:

   - `Local Server` - Um die Exportdatei auf demselben Server zu speichern, auf dem Commerce installiert ist.
   - `Remote FTP` - Zum Speichern der Exportdatei auf einem Remote-Server.

   ![Informationen zur geplanten Exportdatei](./assets/data-transfer-scheduled-export-file-information.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Wenn das Remote-Speichermodul aktiviert ist, wechselt der `Local Server` automatisch zu `Remote Storage`.

1. Geben Sie für **[!UICONTROL File Directory]** den Ordner ein, in dem die Exportdatei wie folgt gespeichert werden soll:

   - Geben Sie für **[!UICONTROL Local Server]** einen relativen Pfad innerhalb der Commerce-Installation ein, z. B. `var/export`. Wenn das Remote-Speichermodul konfiguriert ist, verwenden Sie `import_export/export`.
   - Geben Sie für &quot;**[!UICONTROL Remote FTP server]**&quot;die vollständige URL und den Pfad zum Zielordner auf dem Zielserver ein.

1. Wenn der _[!UICONTROL Remote FTP]_-Server ausgewählt ist, geben Sie Anmeldedaten für die Verbindung zum Server ein und wählen Sie zusätzliche Einstellungen aus:

   - Geben Sie für &quot;**[!UICONTROL FTP Host[:Port]]**&quot;die Remote-FTP-Hostadresse ein.
   - Geben Sie für &quot;**[!UICONTROL User Name]**&quot;den Benutzernamen ein, der für den Zugriff auf den Remote-Server verwendet wird.
   - Geben Sie für **[!UICONTROL Password]** das Kennwort des angegebenen Benutzerkontos ein.
   - Wählen Sie für **[!UICONTROL File Mode]** `Binary` oder `ASCII` aus.
   - Wählen Sie für **[!UICONTROL Passive Mode]** `No` oder `Yes` aus.

### Schritt 3: Konfigurieren von Export-Fehler-E-Mails

1. Setzen Sie **[!UICONTROL Failed Email Receiver]** auf den Store-Kontakt, der eine Benachrichtigung erhalten soll, wenn während des Exports ein Fehler auftritt.

1. Setzen Sie **[!UICONTROL Failed Email Sender]** auf den Store-Kontakt, der als Absender der Benachrichtigung angezeigt wird.

1. Setzen Sie **[!UICONTROL Failed Email Template]** auf die Vorlage, die für die Benachrichtigung verwendet wird.

1. Geben Sie für &quot;**[!UICONTROL Send Failed Email Copy To]**&quot; die E-Mail-Adresse eines Empfängers an, der eine Kopie der Benachrichtigung erhalten soll.

   Trennen Sie bei mehreren E-Mail-Adressen durch Kommas.

1. Setzen Sie **[!UICONTROL Failed Email Copy Method]** auf einen der folgenden Werte:

   - `Bcc` - Sendet eine blinde höfliche Kopie. Der Name und die Adresse des Empfängers sind in der ursprünglichen E-Mail-Verteilung enthalten, werden jedoch ausgeblendet.
   - `Separate Email` - Sendet die Kopie als separate E-Mail.

### Schritt 4: Entitätsattribute auswählen

1. Wählen Sie im Abschnitt _[!UICONTROL Entity Attributes]_die Attribute aus, die Sie in die Exportdaten aufnehmen möchten.

   - Um Exportdaten nach Attributwerten zu filtern, geben Sie den Attributwert in die Spalte _[!UICONTROL Filter]_ein.
   - Um Produkte oder Kunden mit bestimmten Attributwerten auszuschließen, geben Sie die Werte der Attribute ein, die Sie ausschließen möchten, und aktivieren Sie das Kontrollkästchen in der Spalte Überspringen .

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]**.

   Der neue geplante Exportauftrag wird der Liste auf der Seite _[!UICONTROL Scheduled Import/Export]_hinzugefügt. Von dieser Seite aus kann sie sofort zum Testen und Bearbeiten ausgeführt werden.

>[!NOTE]
>
>Wenn Sie einen geplanten Import/Export erstellen oder aktualisieren, ändert sich die Systemkonfiguration. Stellen Sie nach dem Speichern sicher, dass Sie den Hinweis zur Cache-Invalidierung bearbeiten, der oben auf der Admin-Seite angezeigt wird, und leeren Sie den Cache, um den neuen oder aktualisierten Zeitplan anzuwenden.

### Feldbeschreibungen

#### [!UICONTROL Export Settings]

| Feld | Beschreibung |
| ----- | ----------- | 
| [!UICONTROL Name] | Der Name des Exports. Hilft Ihnen, es zu unterscheiden, wenn viele verschiedene geplante Exporte erstellt werden. |
| [!UICONTROL Description] | (Optional) Eine Beschreibung des geplanten Exports. |
| [!UICONTROL Entity Type] | Identifiziert die zu exportierenden Daten. Nach der Auswahl werden die Entitätsattribute unten angezeigt. Optionen: `Advanced Pricing` / `Products` / `Customer Finances` / `Customers Main File` / `Customer Addresses` / `Stock Sources` |
| [!UICONTROL Start Time] | Legen Sie die Startzeit, Minuten und Sekunden des Exports fest. |
| [!UICONTROL Frequency] | Definieren Sie, wie oft der Exportauftrag ausgeführt wird. Optionen: `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL Status] | Ein neuer geplanter Export ist standardmäßig aktiviert. Sie können sie aussetzen, indem Sie Status auf Deaktiviert setzen. Optionen: `Enabled` / `Disabled` |
| [!UICONTROL File Format] | Wählen Sie das Format der Exportdatei aus. Derzeit ist nur die Option `.CSV` verfügbar. |

{style="table-layout:auto"}

#### [!UICONTROL Export Settings Information]

| Feld | Beschreibung |
| ----- | ----------- | 
| [!UICONTROL Server Type] | Bestimmt den Speicherort der Exportdatei. Optionen:<br>**Lokaler Server** - Platziert die Exportdatei auf demselben Server, auf dem Commerce bereitgestellt ist. Wenn das Remote-Speichermodul aktiviert ist, wird `Local Server` auf `Remote Storage` umgestellt.<br>**Remote FTP** - Platziert die Exportdatei auf einem Remote-Server. Es werden zusätzliche Optionen für Anmeldedaten und Dateiübertragungseinstellungen angezeigt. |
| [!UICONTROL File Directory] | Geben Sie den Ordner an, in dem die Exportdatei abgelegt ist. Wenn _[!UICONTROL Server Type]_auf `Local Server` gesetzt ist, geben Sie den Pfad relativ zum Commerce-Installationspfad an. Beispiel: `var/export` oder `import_export/export` für Remote-Speicher. |

{style="table-layout:auto"}

#### [!UICONTROL Export Failed Emails]

| Feld | Beschreibung |
| ----- | ----------- | 
| [!UICONTROL Failed Email Receiver] | Geben Sie die E-Mail-Adresse an, an die eine E-Mail-Benachrichtigung (Export fehlgeschlagener E-Mails) gesendet wird, wenn der Export fehlschlägt. |
| [!UICONTROL Failed Email Sender] | Geben Sie die E-Mail-Adresse an, die als fehlgeschlagener Export-E-Mail-Absender verwendet wird. |
| [!UICONTROL Failed Email Template] | Wählen Sie eine Vorlage für die fehlgeschlagene Export-E-Mail aus. Standardmäßig ist nur die Option `Export Failed (Default Template from Locale)` verfügbar. |
| [!UICONTROL Send Failed Email Copy To] | Die E-Mail-Adresse, an die eine Kopie der fehlgeschlagenen Export-E-Mail gesendet wird. |
| [!UICONTROL Send Failed Email Copy Method] | Geben Sie die Methode zum Kopieren des Versands für die exportierte fehlgeschlagene E-Mail an. |

{style="table-layout:auto"}
