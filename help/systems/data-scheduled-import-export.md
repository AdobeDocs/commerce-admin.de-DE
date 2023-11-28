---
title: Geplanter Import und Export
description: Erfahren Sie, wie Sie geplante Datenimport- und -exportiervorgänge verwalten.
exl-id: 74ba40f1-a540-4425-9500-2c730c1145e7
feature: Products, Customers, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '2371'
ht-degree: 0%

---

# Geplanter Import und Export

{{ee-feature}}

Geplante Importe und Exporte können täglich, wöchentlich oder monatlich ausgeführt werden. Die zu importierenden oder exportierenden Dateien können sich auf lokalen Adobe Commerce-Servern oder Remote-FTP-Servern befinden. Geplanter Import/Export ist standardmäßig implementiert und erfordert keine zusätzliche Konfiguration. Alle geplanten Importe und Exporte werden vom Cron-Auftragsplaner verwaltet.

## Zugriff auf geplanten Import/Export

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Scheduled Imports/Exports]**.

   ![Geplanter Datenimport/-export](./assets/data-scheduled-import-export.png){width="700" zoomable="yes"}

1. Um einen neuen geplanten Import- oder Exportauftrag zu erstellen, klicken Sie auf die entsprechende Schaltfläche und befolgen Sie die Anweisungen für den Typ des geplanten Auftrags.

   - [Geplanten Export hinzufügen](#schedule-an-export)
   - [Geplanten Import hinzufügen](#schedule-an-import)

1. Wenn der Datensatz gespeichert wird, wird der Auftrag im _[!UICONTROL Scheduled Import/Export]_Gitter.

   >[!NOTE]
   >
   >Wenn Sie einen geplanten Import/Export erstellen oder aktualisieren, ändert sich die Systemkonfiguration. Stellen Sie nach dem Speichern sicher, dass Sie den Hinweis zur Cache-Invalidierung bearbeiten, der oben auf der Admin-Seite angezeigt wird, und leeren Sie den Cache, um den neuen oder aktualisierten Zeitplan anzuwenden.

1. Nach jedem geplanten Auftrag wird eine Kopie der Datei im `var/log/import_export` auf dem lokalen Adobe Commerce-Server.

   Die Details der einzelnen Vorgänge werden nicht in das Protokoll geschrieben. Wenn ein Fehler auftritt, wird eine Benachrichtigung über den fehlgeschlagenen Import-/Exportvorgang mit einer Fehlerbeschreibung gesendet.

## Import planen

Für das verfügbare Importdateiformat und die Typen von Importentitäten ähnelt der geplante Importprozess dem manuellen Importprozess:

- Die Importdatei sollte im .CSV-Format vorliegen.
- Sie können Produkt- und Kundendaten importieren

Der Vorteil des geplanten Imports besteht darin, dass Sie eine Datendatei automatisch mehrmals importieren können, nachdem Sie die Importparameter angegeben und nur einmal geplant haben.

Die Details der einzelnen Importvorgänge werden nicht in ein Protokoll geschrieben, aber bei einem Fehler erhalten Sie eine _Import Fehlgeschlagen_ E-Mail mit einer Fehlerbeschreibung. Das Ergebnis des letzten geplanten Importvorgangs wird in der Spalte Letztes Ergebnis auf der Seite Geplanter Import/Export angezeigt.

Nach jedem Import-Vorgang wird eine Kopie der Importdatei im `var/log/import_export` -Ordner auf dem Server, auf dem Adobe Commerce oder Magento Open Source bereitgestellt ist. Der Zeitstempel, die Markierung der importierten Entität (Produkte oder Kunden) und der Typ des Vorgangs (in diesem Fall Import) werden dem Namen der Importdatei hinzugefügt.

Nach jedem geplanten Importauftrag wird automatisch ein Neuindizierungsvorgang ausgeführt. Änderungen an den Beschreibungen und anderen Textinformationen werden nach der Aktualisierung der Daten in die Datenbank übernommen, und die Preisänderungen werden erst nach der Neuindizierung übernommen.

### Schritt 1: Abschließen der Importeinstellungen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Scheduled Import/Export]**.

1. Klicken Sie oben rechts auf **[!UICONTROL Add Scheduled Import]**.

1. Legen Sie die Zeitplan- und Importoptionen fest:

   - **[!UICONTROL Name]** — Geben Sie einen Namen für den geplanten Import ein.

   - **[!UICONTROL Description]** — Geben Sie eine kurze Beschreibung ein, in der der Zweck des Imports und seine Verwendung erläutert werden.

   - **[!UICONTROL Entity Type]** — Legen Sie einen der folgenden Parameter fest:

      - `Products`
      - `Advanced Pricing`
      - `Customers and Addresses (single file)`
      - `Customer Addresses`
      - `Customer Finances`
      - `Customers Main File`
      - `Stock Sources`

   - **[!UICONTROL Import Behavior]** — Legen Sie einen der folgenden Parameter fest:

      - `Add/Update Complex Data` — Fügt neue komplexe Daten zu den vorhandenen komplexen Daten für vorhandene Einträge in der Datenbank hinzu oder aktualisiert sie. Dies ist der Standardwert.
      - `Replace` — Schreibt vorhandenen Komplex für bestehende Entitäten in der Datenbank um.
      - `Delete Entities` — Löscht vorhandene Einträge in der Datenbank.
      - `Custom Action` - Passt vorhandene Entitäten in der Datenbank an.

     >[!NOTE]
     >
     >Für _[!UICONTROL Advanced Pricing]_,_[!UICONTROL Products]_, _[!UICONTROL Customers and Addresses (single file)]_, und_[!UICONTROL Stock Sources]_ Entitätstypen werden diese Importverhaltensweisen angezeigt: `Add/Update`, `Replace`, und `Delete`. Für _Kundenfinanzierungen_, _Hauptdatei des Kunden_, und _Kunden und Adressen_ Entitätstypen werden diese Importverhaltensweisen angezeigt: `Add/Update Complex Data`, `Delete Entities`, und `Custom Action`.

   - **[!UICONTROL Start Time]** — Stellen Sie auf die Stunde, Minute und Sekunde ein, für die der Import geplant ist.

   - **[!UICONTROL Frequency]** — Legen Sie einen der folgenden Parameter fest: `Daily`, `Weekly`oder `Monthly`

   - **[!UICONTROL On Error]** - Legen Sie einen der folgenden Parameter fest: `Stop Import` oder `Continue Processing`

   - **[!UICONTROL Status]** — Um den geplanten Import zu aktivieren, setzen Sie auf `Enabled`.

   - **[!UICONTROL Field Separator]** — Geben Sie das Zeichen ein, das zum Trennen von Feldern in der Importdatei verwendet wird. Das Standardzeichen ist ein Komma.

   - **[!UICONTROL Multiple Value Separator]** — Geben Sie das Zeichen ein, das verwendet wird, um mehrere Werte in einem Feld zu trennen.

   ![Datenimport - Geplante Importeinstellungen](./assets/data-transfer-scheduled-import-settings.png){width="600" zoomable="yes"}

### Schritt 2: Ausfüllen der Importdatei-Informationen

1. Satz **[!UICONTROL Server Type]** auf einen der folgenden Werte zu:

   - `Local Server` - Importiert die Daten von demselben Server, auf dem Adobe Commerce installiert ist.
   - `Remote FTP` - Importiert die Daten von einem Remote-Server.

   ![Datenimport - Informationen zu geplanten Importdateien](./assets/data-transfer-scheduled-import-file-information.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Wenn das Remote-Speichermodul aktiviert ist, `Local Server` wechselt automatisch zu `Remote Storage`.

1. Geben Sie die **[!UICONTROL File Directory]** wo die Importdatei ihren Ursprung hat.

   - `Local Server` - Geben Sie einen relativen Pfad in die Commerce-Installation ein. Beispiel, `var/import`. Wenn das Remote-Speichermodul konfiguriert ist, verwenden Sie `import_export/import`.
   - `Remote FTP server` - Geben Sie die vollständige URL und den Pfad zum Importordner auf dem Remote-Server ein.

1. Geben Sie die **[!UICONTROL File Name]** zu importieren.

1. Für **[!UICONTROL Images File Directory]** Geben Sie den Pfad zu dem Verzeichnis ein, in dem die Produktbilder gespeichert werden.

   Geben Sie auf einem lokalen Server einen relativen Pfad wie den folgenden ein: `var/import`. Geben Sie auf einem Remote-Speicher einen relativen Pfad ein, z. B.: `import_export/import` oder `import_export/import/some/dir`.

### Schritt 3: Konfigurieren des Imports fehlgeschlagener E-Mails

![Datenimport - fehlgeschlagene Importe fehlgeschlagener E-Mails](./assets/data-transfer-scheduled-import-email-fail.png){width="600" zoomable="yes"}

1. Satz **[!UICONTROL Failed Email Receiver]** an den Store-Kontakt, der eine Benachrichtigung erhalten soll, wenn beim Import ein Fehler auftritt.

1. Satz **[!UICONTROL Failed Email Sender]** an den Store-Kontakt, der als Absender der Benachrichtigung angezeigt wird.

1. Satz **[!UICONTROL Failed Email Template]** der Vorlage, die für die Benachrichtigung verwendet wird.

1. Für **[!UICONTROL Send Failed Email Copy To]** die E-Mail-Adresse eines Empfängers eingeben, der eine Kopie der Benachrichtigung erhalten soll.

   Trennen Sie mehrere E-Mail-Adressen durch Kommas.

1. Satz **[!UICONTROL Failed Email Copy Method]** auf einen der folgenden Werte zu:

   - `Bcc` - Sendet eine blinde Kopie der fehlgeschlagenen Importbenachrichtigung. Der Name und die Adresse des Empfängers sind in der ursprünglichen E-Mail-Verteilung enthalten, jedoch nicht sichtbar.
   - `Separate Email` - Sendet eine Kopie der fehlgeschlagenen Importbenachrichtigung als separate E-Mail.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]**.

   Der neue geplante Importauftrag wird der Liste auf der Seite _[!UICONTROL Scheduled Import/Export]_Seite. Von dieser Seite aus kann sie sofort zum Testen und Bearbeiten ausgeführt werden. Die Importdatei wird vor der Ausführung jedes Importvorgangs validiert.

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
| [!UICONTROL Import Behavior] | Definiert, wie komplexe Daten verarbeitet werden, wenn die importierten Entitäten in der Datenbank vorhanden sind. Zu den komplexen Daten für Produkte gehören Kategorien, Websites, benutzerdefinierte Optionen, Tier-Preise, zugehörige Produkte, Upsells, Querverkäufe und zugehörige Produktdaten. Komplexe Daten für Kunden enthalten Adressen. Optionen:<br>**[!UICONTROL Add/Update Complex Data]**- Die neuen komplexen Daten werden zu den vorhandenen komplexen Daten für vorhandene Einträge in der Datenbank hinzugefügt oder aktualisiert. Dies ist der Standardwert.<br>**[!UICONTROL Add/Update]** - Den vorhandenen Einträgen in der Datenbank werden neue Daten hinzugefügt. Alle Felder außer `sku` kann für Produkte aktualisiert werden. Alle nicht in der CSV-Datei aufgelisteten Feldwerte wie Kategorien oder Websites bleiben nach dem Import in der Datenbank.<br>**[!UICONTROL Replace]**- Die vorhandenen komplexen Daten für die vorhandenen Entitäten werden ersetzt.<br>**[!UICONTROL Delete Entities]** - Wenn importierte Entitäten in der Datenbank vorhanden sind, werden sie aus der Datenbank gelöscht.<br>**[!UICONTROL Custom Action]**- Die vorhandenen komplexen Entitäten werden während des Importvorgangs angepasst. |
| [!UICONTROL Start Time] | Legen Sie die Startzeit, Minuten und Sekunden des Imports fest. |
| [!UICONTROL Frequency] | Definieren Sie, wie oft der Import ausgeführt wird. Optionen: `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL On Error] | Definieren Sie das Systemverhalten für den Fall, dass bei der Dateivalidierung Fehler gefunden werden. Optionen:<br>**Import stoppen** — Die Datei wird nicht importiert, wenn bei der Validierung Fehler gefunden wurden. Dies ist der Standardwert.<br>**Verarbeitung fortsetzen** - Wenn bei der Validierung Fehler gefunden werden, aber ein Import möglich ist, wird die Datei importiert. |
| [!UICONTROL Status] | Der Import ist standardmäßig aktiviert. Sie können die Aussetzung vornehmen, indem Sie den Status auf `Disabled`. |
| [!UICONTROL Field Separator] | Bestimmt das Zeichen, das zum Trennen von Feldern verwendet wird. Standardwert: `,` (Komma) |
| [!UICONTROL Multiple Value Separator] | Bestimmt das Zeichen, das zum Trennen mehrerer Werte in einem Feld verwendet wird. Standardwert: `,` (Komma) |

{style="table-layout:auto"}

#### [!UICONTROL Import File Information]

| Feld | Beschreibung |
| ----- | ----------- | 
| [!UICONTROL Server Type] | Sie können aus einer Datei auf demselben Server importieren, auf dem Commerce bereitgestellt wird (wählen Sie `Local Server`) oder vom Remote-FTP-Server (wählen Sie `Remote FTP`). Wenn Sie _[!UICONTROL Remote FTP]_, werden zusätzliche Optionen für Anmeldedaten und Dateiübertragungseinstellungen angezeigt. Wenn das Remote-Speichermodul aktiviert ist, `Local Server` Typ automatisch auf `Remote Storage`. |
| [!UICONTROL File Directory] | Geben Sie den Ordner an, in dem sich die Importdatei befindet. Wenn der Servertyp auf _[!UICONTROL Local Server]_Geben Sie den Pfad relativ zum Commerce-Installationsordner an. Beispiel: `var/import` oder `import_export/import` für Remote-Speicher. |
| [!UICONTROL File Name] | Geben Sie den Namen der Importdatei an. |
| [!UICONTROL Images File Directory] | Geben Sie den Pfad zu dem Ordner ein, in dem Produktbilder gespeichert werden. Geben Sie für einen lokalen Server einen relativen Pfad ein. Beispiel: `var/import` oder `import_export/import` für Remote-Speicher. |

{style="table-layout:auto"}

#### [!UICONTROL Import Failed Emails]

| Feld | Beschreibung |
| ----- | ----------- | 
| [!UICONTROL Failed Email Receiver] | Geben Sie die E-Mail-Adresse an, an die eine E-Mail-Benachrichtigung (fehlgeschlagene Import-E-Mail) gesendet wird, wenn der Import fehlschlägt. |
| [!UICONTROL Failed Email Sender] | Geben Sie die E-Mail-Adresse an, die als Absender für die Import-fehlgeschlagene E-Mail verwendet wird. |
| [!UICONTROL Failed Email Template] | Wählen Sie eine Vorlage für die Import-E-Mail aus. Standardmäßig ist nur die Option Import fehlgeschlagen (Standardvorlage aus Gebietsschema) verfügbar. Benutzerdefinierte Vorlagen können unter _[!UICONTROL System]_>_[!UICONTROL Transactional Emails]_. |
| [!UICONTROL Send Failed Email Copy To] | Die E-Mail-Adresse, an die eine Kopie der fehlgeschlagenen Importdatei gesendet wird. |
| [!UICONTROL Send Failed Email Copy Method] | Wählen Sie die Methode zum Kopieren des Versands für den Import der fehlgeschlagenen E-Mail aus. |

{style="table-layout:auto"}

## Export planen

Geplanter Export ähnelt einem manuellen [Export](data-export.md) im verfügbaren Exportdateiformat und den Typen der Entitäten, die exportiert werden können:

- Sie können in das CSV-Format exportieren
- Sie können Produkt- und Kundendaten exportieren

Der Vorteil der Verwendung von &quot;Geplanter Export&quot;besteht darin, dass Sie Daten nach Angabe der Exportparameter mehrmals automatisch exportieren und nur einmal planen können.

Die Details der einzelnen Exporte werden nicht in ein Protokoll geschrieben. Wenn jedoch ein Fehler auftritt, erhalten Sie eine E-Mail mit der Fehlerbeschreibung &quot;Export Failed&quot;(Export fehlgeschlagen). Das Ergebnis des letzten Exportvorgangs wird in der Spalte Letztes Ergebnis auf der Seite Geplantes Importieren/Exportieren angezeigt.

Nach jedem Export wird die Exportdatei an dem benutzerdefinierten Speicherort abgelegt und eine Kopie im `var/log/import_export` -Ordner auf dem Server, auf dem Adobe Commerce oder Magento Open Source bereitgestellt ist. Der Zeitstempel und die Markierung der exportierten Entität (Produkte oder Kunden) sowie der Typ des Vorgangs (in diesem Fall Export) werden dem Namen der Exportdatei hinzugefügt.

### Schritt 1: Exporteinstellungen abschließen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Scheduled Import/Export]**.

1. Klicken Sie oben rechts auf **[!UICONTROL Add Scheduled Export]** und gehen Sie wie folgt vor:

   - Geben Sie einen **[!UICONTROL Name]** für den geplanten Export.

   - Kurzbeschreibung eingeben **[!UICONTROL Description]** erklärt den Zweck des Exports und seine Verwendung.

   - Satz **[!UICONTROL Entity Type]** auf einen der folgenden Werte zu:

      - `Advanced Pricing`
      - `Products`
      - `Customer Financing`
      - `Customers Main File`
      - `Customer Addresses`
      - `Stock Sources`

     Die _[!UICONTROL Entity Attributes]_-Abschnitt am unteren Rand der Seite aktualisiert, um den ausgewählten Entitätstyp widerzuspiegeln.

   - Satz **[!UICONTROL Start Time]** auf die Stunde, Minute und Sekunde, in der der Export beginnen soll.

   - Satz **[!UICONTROL Frequency]** auf einen der folgenden Werte zu:

      - `Daily`
      - `Weekly`
      - `Monthly`

1. Um den geplanten Export zu aktivieren, legen Sie **[!UICONTROL Status]** nach `Enabled`.

1. Accept `CSV` als Standard **[!UICONTROL File Format]**.

   ![Einstellungen für geplante Exporte](./assets/data-transfer-scheduled-export-settings.png){width="600" zoomable="yes"}

### Schritt 2: Ausfüllen der Exportdateiinformationen

1. Satz **[!UICONTROL Server Type]** auf einen der folgenden Werte zu:

   - `Local Server` - Zum Speichern der Exportdatei auf dem Server, auf dem Commerce installiert ist.
   - `Remote FTP` — Zum Speichern der Exportdatei auf einem Remote-Server.

   ![Informationen zur geplanten Exportdatei](./assets/data-transfer-scheduled-export-file-information.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Wenn das Remote-Speichermodul aktiviert ist, wird die `Local Server` wechselt automatisch zu `Remote Storage`.

1. Für **[!UICONTROL File Directory]** Geben Sie den Ordner ein, in dem die Exportdatei wie folgt gespeichert werden soll:

   - Für **[!UICONTROL Local Server]** einen relativen Pfad innerhalb der Commerce-Installation eingeben, z. B. `var/export`. Wenn das Remote-Speichermodul konfiguriert ist, verwenden Sie `import_export/export`.
   - Für **[!UICONTROL Remote FTP server]** Geben Sie die vollständige URL und den Pfad zum Zielordner auf dem Zielserver ein.

1. Wenn die Variable _[!UICONTROL Remote FTP]_-Server ausgewählt ist, geben Sie Anmeldedaten für die Verbindung zum Server ein und wählen Sie zusätzliche Einstellungen aus:

   - Für **[!UICONTROL FTP Host[:Port]]**, geben Sie die Remote-FTP-Hostadresse ein.
   - Für **[!UICONTROL User Name]** Geben Sie den Benutzernamen ein, der für den Zugriff auf den Remote-Server verwendet wird.
   - Für **[!UICONTROL Password]**, geben Sie das Kennwort des angegebenen Benutzerkontos ein.
   - Für **[!UICONTROL File Mode]** auswählen `Binary` oder `ASCII`.
   - Für **[!UICONTROL Passive Mode]** auswählen `No` oder `Yes`.

### Schritt 3: Konfigurieren von Export-Fehler-E-Mails

1. Satz **[!UICONTROL Failed Email Receiver]** an den Store-Kontakt, der eine Benachrichtigung erhalten soll, wenn beim Export ein Fehler auftritt.

1. Satz **[!UICONTROL Failed Email Sender]** an den Store-Kontakt, der als Absender der Benachrichtigung angezeigt wird.

1. Satz **[!UICONTROL Failed Email Template]** der Vorlage, die für die Benachrichtigung verwendet wird.

1. Für **[!UICONTROL Send Failed Email Copy To]** die E-Mail-Adresse eines Empfängers eingeben, der eine Kopie der Benachrichtigung erhalten soll.

   Trennen Sie bei mehreren E-Mail-Adressen durch Kommas.

1. Satz **[!UICONTROL Failed Email Copy Method]** auf einen der folgenden Werte zu:

   - `Bcc` - Sendet eine blinde höfliche Kopie. Der Name und die Adresse des Empfängers sind in der ursprünglichen E-Mail-Verteilung enthalten, werden jedoch ausgeblendet.
   - `Separate Email` — Sendet die Kopie als separate E-Mail.

### Schritt 4: Entitätsattribute auswählen

1. Im _[!UICONTROL Entity Attributes]_auswählen, die Attribute, die Sie in die Exportdaten aufnehmen möchten.

   - Um Exportdaten nach Attributwerten zu filtern, geben Sie den Attributwert in das Feld _[!UICONTROL Filter]_Spalte.
   - Um Produkte oder Kunden mit bestimmten Attributwerten auszuschließen, geben Sie die Werte der Attribute ein, die Sie ausschließen möchten, und aktivieren Sie das Kontrollkästchen in der Spalte Überspringen .

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]**.

   Der neue geplante Exportauftrag wird der Liste auf der Seite _[!UICONTROL Scheduled Import/Export]_Seite. Von dieser Seite aus kann sie sofort zum Testen und Bearbeiten ausgeführt werden.

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
| [!UICONTROL File Format] | Wählen Sie das Format der Exportdatei aus. Derzeit ist nur der `.CSV` verfügbar ist. |

{style="table-layout:auto"}

#### [!UICONTROL Export Settings Information]

| Feld | Beschreibung |
| ----- | ----------- | 
| [!UICONTROL Server Type] | Bestimmt den Speicherort der Exportdatei. Optionen:<br>**Lokaler Server** — Platziert die Exportdatei auf demselben Server, auf dem Commerce bereitgestellt wird. Wenn das Remote-Speichermodul aktiviert ist, `Local Server` wird auf umgestellt `Remote Storage`.<br>**Remote FTP** — Platziert die Exportdatei auf einem Remote-Server. Es werden zusätzliche Optionen für Anmeldedaten und Dateiübertragungseinstellungen angezeigt. |
| [!UICONTROL File Directory] | Geben Sie den Ordner an, in dem die Exportdatei abgelegt ist. In diesem Fall _[!UICONTROL Server Type]_auf `Local Server`Geben Sie den Pfad relativ zum Commerce-Installationspfad an. Beispiel: `var/export`oder `import_export/export` für Remote-Speicher. |

{style="table-layout:auto"}

#### [!UICONTROL Export Failed Emails]

| Feld | Beschreibung |
| ----- | ----------- | 
| [!UICONTROL Failed Email Receiver] | Geben Sie die E-Mail-Adresse an, an die eine E-Mail-Benachrichtigung (Export fehlgeschlagener E-Mails) gesendet wird, wenn der Export fehlschlägt. |
| [!UICONTROL Failed Email Sender] | Geben Sie die E-Mail-Adresse an, die als fehlgeschlagener Export-E-Mail-Absender verwendet wird. |
| [!UICONTROL Failed Email Template] | Wählen Sie eine Vorlage für die fehlgeschlagene Export-E-Mail aus. Standardmäßig wird nur der `Export Failed (Default Template from Locale)` verfügbar ist. |
| [!UICONTROL Send Failed Email Copy To] | Die E-Mail-Adresse, an die eine Kopie der fehlgeschlagenen Export-E-Mail gesendet wird. |
| [!UICONTROL Send Failed Email Copy Method] | Geben Sie die Methode zum Kopieren des Versands für die exportierte fehlgeschlagene E-Mail an. |

{style="table-layout:auto"}
