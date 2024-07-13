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

![System - Data Collector](./assets/data-collector.png){width="600" zoomable="yes"}

### Ausführen des Datenerfassers

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL Data Collector]**.

1. Klicken Sie in der oberen rechten Ecke auf **[!UICONTROL New Backup]**.

   Die Erstellung des Backups dauert einige Minuten. Sie können die Verarbeitungsergebnisse durch Klicken auf **[!UICONTROL Refresh Status]** überwachen. Nach Abschluss des Vorgangs wird die Sicherung im Raster _[!UICONTROL Data Collector]_angezeigt.

1. Gehen Sie wie folgt vor, um ein Protokoll mit den Sicherungsdetails anzuzeigen:

   - Wählen Sie in der Spalte _[!UICONTROL Action]_die Option **[!UICONTROL Show Log]**aus.

   - Klicken Sie auf **[!UICONTROL Back]** , um zum Raster zurückzukehren.

   ![Datenerfassungsprotokoll](./assets/data-collector-log.png){width="600" zoomable="yes"}

### Backup-Daten exportieren

1. Aktivieren Sie in der ersten Spalte das Kontrollkästchen des zu exportierenden Backups.

1. Wählen Sie im Menü **[!UICONTROL Export]** das Format der Exportdaten aus.

   ![Exportformat](./assets/data-collector-export.png){width="600" zoomable="yes"}

1. Greifen Sie über den Speicherort des Downloads im Webbrowser auf die Datei zu und verwenden Sie **[!UICONTROL Save]** sie.

### Sicherungsdaten herunterladen

Nachdem die Sicherung generiert wurde, können Sie die Kopie von Code- und DB-Daten herunterladen.

1. Suchen Sie die benötigte Backup-Entität im Raster.

1. Vergewissern Sie sich, dass der Status &quot;`Complete`&quot;lautet.

1. Klicken Sie in den Spalten _[!UICONTROL Code Dump]_oder_[!UICONTROL DB Dump]_ auf den Entitätsnamen.

Der Download-Prozess sollte automatisch gestartet werden.

## Sicherungsdaten löschen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL Data Collector]**.

1. Suchen und wählen Sie die zu löschenden Sicherungsdaten aus.

1. Klicken Sie in der Spalte _[!UICONTROL Action]_auf **[!UICONTROL Delete]**.

1. Um die Aktion zu bestätigen, klicken Sie auf **[!UICONTROL OK]**.

## Systemberichte

Das Tool für die Systemberichterstellung bietet Ihnen die Möglichkeit, regelmäßig vollständige oder teilweise Momentaufnahmen des Systems zu erstellen und diese zur späteren Verwendung zu speichern. Sie können Leistungseinstellungen vor und nach Codeentwicklungszyklen oder Änderungen an Servereinstellungen vergleichen. Das Tool für die Systemberichterstellung kann die Zeit für die Vorbereitung und Übermittlung der vom Support benötigten Informationen für die Einleitung einer Untersuchung erheblich verkürzen.

Im Raster Systemberichte können Sie vorhandene Berichte anzeigen und herunterladen, Berichte löschen und Berichte erstellen.

### Systemberichte aufrufen

Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL System Report]**.

![Admin - Systemberichte](./assets/reports.png){width="600" zoomable="yes"}

### Bericht erstellen

1. Klicken Sie auf **[!UICONTROL New Report]**.

1. Wählen Sie in der Liste &quot;**[!UICONTROL Groups]**&quot;die einzelnen Informationen aus, die Sie in den Bericht aufnehmen möchten. Standardmäßig sind alle Gruppen ausgewählt.

   ![Systembericht - ausgewählte Gruppen](./assets/report-create.png){width="600" zoomable="yes"}

1. Klicken Sie in der oberen rechten Ecke auf **[!UICONTROL Create]**.

   Je nach der Anzahl der ausgewählten Berichtstypen kann es einige Minuten dauern, bis der Bericht generiert wird. Wenn der Bericht fertig ist, wird er oben im Raster mit dem generierten Datum und der generierten Uhrzeit angezeigt.

### Modulinformationen anzeigen

Sie finden nützliche Informationen zu installierten Modulen.

**_So zeigen Sie Berichtinformationen für jedes installierte Modul an:_**

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL System Report]**.
1. Klicken Sie auf **[!UICONTROL New Report]**.
1. Wählen Sie `Modules` aus der Liste **[!UICONTROL Groups]** aus.
1. Klicken Sie auf **[!UICONTROL Create]**.
1. Nachdem der Bericht generiert wurde, klicken Sie auf **[!UICONTROL Select]** und dann auf **[!UICONTROL View]** , um alle Modulversionen anzuzeigen.
1. Klicken Sie auf **[!UICONTROL Download]** , um den Bericht herunterzuladen.

### Systemberichte verwalten

Wählen Sie in der Spalte **[!UICONTROL Action]** des Rasters eine der folgenden Optionen aus:

- `View` - Mit dieser Funktion können Sie die Details des Berichts anzeigen.
- `Delete` - Mit dieser Funktion löschen Sie den generierten Bericht aus der Liste.
- `Download` - Mit dieser Funktion können Sie den Bericht als HTML-Datei speichern.

### Systemberichtdetails anzeigen

1. Wählen Sie für den benötigten Bericht in der Spalte _[!UICONTROL Actions]_die Option **[!UICONTROL View]**aus.

1. Erweitern Sie im linken Bereich den Bereich ![Erweiterungsauswahl](../assets/icon-display-expand.png) des Berichts, um die Details anzuzeigen.

   ![Allgemeine Informationen zum Systembericht](./assets/report-information.png){width="600" zoomable="yes"}

### Verfügbare Systemberichte

| Berichtsgruppe | Enthaltene Informationen |
| ------------ | -------------------- |
| [!UICONTROL General] | Adobe Commerce-Version<br>Datenanzahl<br>Cache-Status<br> Indexstatus |
| [!UICONTROL Environment] | Umgebungsinformationen<br>MySQL-Status |
| [!UICONTROL Data] | Duplizieren von Kategorien nach URL-Schlüssel<br>Duplizieren von Produkten nach URL-Schlüssel<br>Duplizieren von Produkten nach SKU<br> Duplizieren von Bestellungen nach Inkrement-ID<br>Duplizieren von Benutzern per E-Mail<br> Beschädigte Kategoriedaten |
| [!UICONTROL Modules] | Liste der benutzerdefinierten Module<br>Liste der deaktivierten Module<br> Liste aller Module |
| [!UICONTROL Configuration] | Konfiguration<br>Daten aus der Matrix der Zahlungsmethoden `app/etc/env.php`<br>Versandmethoden<br>Zahlungsmethoden<br>Zahlungsfunktionen |
| [!UICONTROL Logs] | Protokolldateien<br>Wichtigste Systemmeldungen<br>Die wichtigsten Systemmeldungen von heute<br>, die wichtigsten Debug-Meldungen<br>Die wichtigsten Debug-Meldungen von heute<br>Die wichtigsten Ausnahmemeldungen<br> Die heutigen wichtigsten Ausnahmemeldungen |
| [!UICONTROL Attributes] | Benutzerdefinierte eV-Attribute <br>Neue eAV-Attribute<br>Entitätstypen<br>alle EAV-Attribute <br>Kategorie-EAV-Attribute<br>Produkt-EAV-Attribute<br>Kunden-EAV-Attribute<br>EAV-Attribut für die Kundenadresse<br>RMA-Element-EAV-Attribute |
| [!UICONTROL Events] | Benutzerdefinierte globale Ereignisse<br>Benutzerspezifische Admin-Ereignisse<br>Benutzerdefinierte Frontend-Ereignisse<br>Benutzerspezifische Doc-Ereignisse<br>Benutzerspezifische Crontab-Ereignisse<br>Benutzerspezifische REST-Ereignisse<br>Benutzerdefinierte SOAP-Ereignisse<br>Globale Core-Ereignisse<br>Core-Admin-Ereignisse<br>Core-Haupt-Ereignisse<br>Dok-Ereignisse<br>Core-SOAP-Ereignisse<br> 3}Alle globalen Ereignisse<br>Alle Admin-Ereignisse<br>Alle Frontend-Ereignisse<br>Alle Doc-Ereignisse<br>Alle REST-Ereignisse<br>Alle SOAP-Ereignisse<br>Alle Crontab-Ereignisse<br><br> |
| [!UICONTROL Cron] | Cron-Zeitpläne nach Statuscode<br>Cron-Zeitpläne nach Auftragscode<br>Fehler in Cron-Zeitpläne-Warteschlange<br>Cron-Zeitplänen-Liste<br>Benutzerdefinierte globale Cron-Aufträge<br>Benutzerdefinierte konfigurierbare Cron-Aufträge<br>Globale Cron-Aufträge Core-konfigurierbare Cron-Aufträge<br>Alle globalen Cron-Aufträge<br>Alle konfigurierbaren Cron-Aufträge<br> |
| [!UICONTROL Design] | AdminHTML-Designliste<br>Frontend-Designliste |
| [!UICONTROL Stores] | Website Tree<br>Websites list<br>stores list<br>store views list |
| OMS Connector <br>_(sichtbar mit OMS-Integration)_ | Connector-Version<br>Connector-Überwachung<br>Ergebnisse bei der Nachrichtenverarbeitung |

{style="table-layout:auto"}
