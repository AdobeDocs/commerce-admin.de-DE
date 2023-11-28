---
title: Support-Tools
description: Erfahren Sie mehr über die bereitgestellten Support-Tools, mit denen Sie Probleme in Ihrem System identifizieren können.
exl-id: f67616e6-7879-4fd3-947a-16856f8447ba
source-git-commit: 97eeb733836f0336401664c5cfb3df2b9f2f2ccf
workflow-type: tm+mt
source-wordcount: '837'
ht-degree: 0%

---

# Support-Tools

{{ee-feature}}

Die Support-Tools wurden entwickelt, um bekannte Probleme in Ihrem System zu erkennen. Sie können während der Entwicklungs- und Optimierungsprozesse als Ressource und als Diagnosetool verwendet werden, um unserem Supportteam bei der Identifizierung und Lösung von Problemen zu helfen.

## Datenerfassung

Der Datenerfasser sammelt die Informationen über Ihr System, die unser Support-Team benötigt, um Probleme mit Ihrer Adobe Commerce-Installation zu beheben. Das erstellte Backup dauert mehrere Minuten und umfasst sowohl einen Code- als auch einen Datenbank-Dump. Die Daten können in eine CSV- oder Excel-XML-Datei exportiert werden.

![System - Datenerfassung](./assets/data-collector.png){width="600" zoomable="yes"}

### Ausführen des Datenerfassers

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL Data Collector]**.

1. Klicken Sie oben rechts auf **[!UICONTROL New Backup]**.

   Die Erstellung des Backups dauert einige Minuten. Sie können die Ergebnisse der Verarbeitung durch Klicken auf **[!UICONTROL Refresh Status]**. Nach Abschluss des Backups wird das Backup im _[!UICONTROL Data Collector]_Gitter.

1. Gehen Sie wie folgt vor, um ein Protokoll mit den Sicherungsdetails anzuzeigen:

   - Im _[!UICONTROL Action]_Spalte auswählen **[!UICONTROL Show Log]**.

   - Klicks **[!UICONTROL Back]** , um zum Raster zurückzukehren.

   ![Datenerfassungsprotokoll](./assets/data-collector-log.png){width="600" zoomable="yes"}

### Backup-Daten exportieren

1. Aktivieren Sie in der ersten Spalte das Kontrollkästchen des zu exportierenden Backups.

1. Verwenden Sie die **[!UICONTROL Export]** -Menü, um das Format der Exportdaten auszuwählen.

   ![Exportformat](./assets/data-collector-export.png){width="600" zoomable="yes"}

1. Rufen Sie die Datei über den Speicherort des Downloads im Webbrowser auf und **[!UICONTROL Save]** es.

### Sicherungsdaten herunterladen

Nachdem die Sicherung generiert wurde, können Sie die Kopie von Code- und DB-Daten herunterladen.

1. Suchen Sie die benötigte Backup-Entität im Raster.

1. Stellen Sie sicher, dass `Complete` -Status.

1. Klicken Sie auf den Entitätsnamen in _[!UICONTROL Code Dump]_oder_[!UICONTROL DB Dump]_ Spalten.

Der Download-Prozess sollte automatisch gestartet werden.

## Sicherungsdaten löschen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL Data Collector]**.

1. Suchen und wählen Sie die zu löschenden Sicherungsdaten aus.

1. Im _[!UICONTROL Action]_Spalte, klicken **[!UICONTROL Delete]**.

1. Klicken Sie zur Bestätigung der Aktion auf **[!UICONTROL OK]**.

## Systemberichte

Das Tool für die Systemberichterstellung bietet Ihnen die Möglichkeit, regelmäßig vollständige oder teilweise Momentaufnahmen des Systems zu erstellen und diese zur späteren Verwendung zu speichern. Sie können Leistungseinstellungen vor und nach Codeentwicklungszyklen oder Änderungen an Servereinstellungen vergleichen. Das Tool für die Systemberichterstellung kann die Zeit für die Vorbereitung und Übermittlung der vom Support benötigten Informationen für die Einleitung einer Untersuchung erheblich verkürzen.

Im Raster Systemberichte können Sie vorhandene Berichte anzeigen und herunterladen, Berichte löschen und Berichte erstellen.

### Systemberichte aufrufen

Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL System Report]**.

![Admin - Systemberichte](./assets/reports.png){width="600" zoomable="yes"}

### Bericht erstellen

1. Klicken **[!UICONTROL New Report]**.

1. Im **[!UICONTROL Groups]** auswählen, wählen Sie die einzelnen Informationen aus, die Sie in den Bericht aufnehmen möchten. Standardmäßig sind alle Gruppen ausgewählt.

   ![Systembericht - ausgewählte Gruppen](./assets/report-create.png){width="600" zoomable="yes"}

1. Klicken Sie oben rechts auf **[!UICONTROL Create]**.

   Je nach der Anzahl der ausgewählten Berichtstypen kann es einige Minuten dauern, bis der Bericht generiert wird. Wenn der Bericht fertig ist, wird er oben im Raster mit dem generierten Datum und der generierten Uhrzeit angezeigt.

### Modulinformationen anzeigen

Sie finden nützliche Informationen zu installierten Modulen.

**_So zeigen Sie Berichtinformationen für jedes installierte Modul an:_**

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL System Report]**.
1. Klicken **[!UICONTROL New Report]**.
1. Auswählen `Modules` aus dem **[!UICONTROL Groups]** Liste.
1. Klicken **[!UICONTROL Create]**.
1. Nachdem der Bericht generiert wurde, klicken Sie auf **[!UICONTROL Select]** und dann **[!UICONTROL View]** um alle Modulversionen anzuzeigen.
1. Klicks **[!UICONTROL Download]** , um den Bericht herunterzuladen.

### Systemberichte verwalten

Im **[!UICONTROL Action]** Wählen Sie eine der folgenden Optionen aus:

- `View` - Verwenden Sie diese Funktion, um die Details des Berichts anzuzeigen.
- `Delete` - Mit dieser Funktion löschen Sie den erstellten Bericht aus der Liste.
- `Download` - Speichern Sie den Bericht mithilfe dieser Funktion als HTML-Datei.

### Systemberichtdetails anzeigen

1. Wählen Sie für den gewünschten Bericht **[!UICONTROL View]** im _[!UICONTROL Actions]_Spalte.

1. Erweitern Sie im linken Bereich ![Erweiterungsauswahl](../assets/icon-display-expand.png) für jeden Abschnitt des Berichts, um die Details anzuzeigen.

   ![Allgemeine Systemberichtinformationen](./assets/report-information.png){width="600" zoomable="yes"}

### Verfügbare Systemberichte

| Berichtsgruppe | Enthaltene Informationen |
| ------------ | -------------------- |
| [!UICONTROL General] | Adobe Commerce-Version<br>Datenanzahl<br>Cache-Status<br>Indexstatus |
| [!UICONTROL Environment] | Umgebungsinformationen<br>MySQL-Status |
| [!UICONTROL Data] | Kategorien nach URL-Schlüssel duplizieren<br>Produkte nach URL-Schlüssel duplizieren<br>Produkte nach SKU duplizieren<br>Duplizieren von Bestellungen nach Inkrement-ID<br>Benutzer per E-Mail duplizieren<br>Beschädigte Kategoriedaten |
| [!UICONTROL Modules] | Benutzerdefinierte Modulliste<br>Liste der deaktivierten Module<br>Liste aller Module |
| [!UICONTROL Configuration] | Konfiguration<br>Daten aus `app/etc/env.php`<br>Versandmethoden<br>Zahlungsmethoden<br>Zahlungsfunktionsmatrix |
| [!UICONTROL Logs] | Protokolldateien<br>Häufigste Systemmeldungen<br>Die wichtigsten Systemmeldungen von heute<br>Häufigste Debug-Meldungen<br>Die wichtigsten Debug-Meldungen von heute<br>Häufigste Ausnahmemeldungen<br>Die wichtigsten Ausnahmemeldungen von heute |
| [!UICONTROL Attributes] | Benutzerdefinierte eV-Attribute<br>Neue EAV-Attribute<br>Entitätstypen<br>Alle EAV-Attribute<br>Kategorie-EAV-Attribute<br>Produkt-EAV-Attribute<br>Kunden-EAV-Attribute<br>EAV-Attribut für Kundenadresse<br>RMA-Element-EAV-Attribute |
| [!UICONTROL Events] | Benutzerspezifische globale Ereignisse<br>Benutzerspezifische Admin-Ereignisse<br>Benutzerdefinierte Frontend-Ereignisse<br>Benutzerspezifische Doc-Ereignisse<br>Benutzerspezifische Registerkarten-Ereignisse<br>Benutzerdefinierte REST-Ereignisse<br>Benutzerdefinierte SOAP-Ereignisse<br>Globale Kernereignisse<br>Hauptadministratorereignisse<br>Haupt-Frontend-Ereignisse<br>Zentrale Doc-Ereignisse<br>Kernkronregisterereignisse<br>REST-Haupt-Ereignisse<br>SOAP-Hauptereignisse<br>Alle globalen Ereignisse<br>Alle Admin-Ereignisse<br>Alle Frontend-Ereignisse<br>Alle Doc-Ereignisse<br>Alle REST-Ereignisse<br>Alle SOAP-Ereignisse<br>Alle Crontab-Ereignisse |
| [!UICONTROL Cron] | Cron-Zeitpläne nach Status-Code<br>Cron-Zeitpläne nach Auftragscode<br>Fehler in der Warteschlange der Cron-Zeitpläne<br>Cron-Zeitplanliste<br>Benutzerdefinierte globale Cron-Aufträge<br>Benutzerdefinierte konfigurierbare Cron-Aufträge<br>Allgemeine globale Cron-Aufträge<br>Kernkonfigurierte Cron-Aufträge<br>Alle globalen Cron-Aufträge<br>Alle konfigurierbaren Cron-Aufträge |
| [!UICONTROL Design] | AdminHTML-Designliste<br>Liste der Frontend-Themen |
| [!UICONTROL Stores] | Website-Baum<br>Websites-Liste<br>Speicherliste<br>Liste der Store-Ansichten |
| OMS Connector <br>_(bei OMS-Integration sichtbar)_ | Connector-Version<br>Connector-Überwachung<br>Nachrichtenverarbeitungsergebnisse |

{style="table-layout:auto"}
