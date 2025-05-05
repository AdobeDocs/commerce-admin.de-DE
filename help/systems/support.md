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

Die Support-Tools dienen zur Identifizierung bekannter Probleme in Ihrem System. Sie können während der Entwicklungs- und Optimierungsprozesse als Ressource und als Diagnosewerkzeug verwendet werden, um unser Supportteam bei der Identifizierung und Lösung von Problemen zu unterstützen.

## Datensammler

Die Datenerfassung erfasst die Informationen über Ihr System, die unser Support-Team benötigt, um Probleme mit Ihrer Adobe Commerce-Installation zu beheben. Das erstellte Backup dauert mehrere Minuten und umfasst sowohl einen Code- als auch einen Datenbank-Dump. Die Daten können in eine CSV- oder Excel-XML-Datei exportiert werden.

![System - Datenerfassung](./assets/data-collector.png){width="600" zoomable="yes"}

### Ausführen des Datenerfassers

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL Data Collector]**.

1. Klicken Sie oben rechts auf **[!UICONTROL New Backup]**.

   Die Erstellung des Backups dauert einige Minuten. Sie können die Ergebnisse der Verarbeitung überwachen, indem Sie auf **[!UICONTROL Refresh Status]** klicken. Nach Abschluss des Vorgangs wird die Sicherung im _[!UICONTROL Data Collector]_&#x200B;angezeigt.

1. Gehen Sie wie folgt vor, um ein Protokoll mit den Backup-Details anzuzeigen:

   - Wählen Sie in der _[!UICONTROL Action]_&#x200B;Spalte **[!UICONTROL Show Log]**&#x200B;aus.

   - Klicken Sie auf **[!UICONTROL Back]** , um zum Raster zurückzukehren.

   ![Datenerfassungsprotokoll](./assets/data-collector-log.png){width="600" zoomable="yes"}

### Exportieren von Sicherungsdaten

1. Aktivieren Sie in der ersten Spalte das Kontrollkästchen des zu exportierenden Backups.

1. Wählen Sie im Menü **[!UICONTROL Export]** das Format der Exportdaten aus.

   ![Exportformat](./assets/data-collector-export.png){width="600" zoomable="yes"}

1. Greifen Sie über den Webbrowser-Download-Speicherort auf die Datei zu und **[!UICONTROL Save]** Sie sie.

### Sicherungsdaten herunterladen

Nachdem das Backup generiert wurde, können Sie die Kopie von Code- und DB-Daten herunterladen.

1. Suchen Sie die erforderliche Backup-Entität im Raster.

1. Stellen Sie sicher, dass sie einen `Complete` Status hat.

1. Klicken Sie auf den Entitätsnamen in _[!UICONTROL Code Dump]_&#x200B;oder&#x200B;_[!UICONTROL DB Dump]_ Spalten.

Der Download-Prozess sollte automatisch gestartet werden.

## Sicherungsdaten löschen

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL Data Collector]**.

1. Suchen Sie die zu löschenden Sicherungsdaten und wählen Sie sie aus.

1. Klicken Sie in der Spalte _[!UICONTROL Action]_&#x200B;auf **[!UICONTROL Delete]**.

1. Um die Aktion zu bestätigen, klicken Sie auf **[!UICONTROL OK]**.

## Systemberichte

Mit dem Tool für die Systemberichterstellung können Sie regelmäßig vollständige oder teilweise Momentaufnahmen des Systems erstellen und diese zur späteren Verwendung speichern. Sie können Leistungseinstellungen vor und nach Code-Entwicklungszyklen oder Änderungen an den Server-Einstellungen vergleichen. Das System-Reporting-Tool kann den Zeitaufwand für die Vorbereitung und Übermittlung der vom Support benötigten Informationen für den Beginn einer Untersuchung erheblich reduzieren.

Über das Raster Systemberichte können Sie vorhandene Berichte anzeigen und herunterladen, Berichte löschen und Berichte erstellen.

### Zugriff auf Systemberichte

Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL System Report]**.

![Admin - System Reports](./assets/reports.png){width="600" zoomable="yes"}

### Erstellen eines Berichts

1. Klicken Sie auf **[!UICONTROL New Report]**.

1. Wählen Sie in der Liste **[!UICONTROL Groups]** alle Informationen aus, die Sie in den Bericht aufnehmen möchten. Standardmäßig sind alle Gruppen ausgewählt.

   ![Systembericht - Gruppen auswählen](./assets/report-create.png){width="600" zoomable="yes"}

1. Klicken Sie oben rechts auf **[!UICONTROL Create]**.

   Je nach der Anzahl der ausgewählten Berichtstypen kann es einige Minuten dauern, bis der Bericht generiert wird. Wenn der Bericht fertig ist, wird er am oberen Rand des Rasters mit dem generierten Datum und der generierten Uhrzeit angezeigt.

### Modulinformationen anzeigen

Nützliche Informationen zu installierten Modulen finden Sie hier.

**_So zeigen Sie Berichtsinformationen für jedes installierte Modul an:_**

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL System Report]**.
1. Klicken Sie auf **[!UICONTROL New Report]**.
1. Wählen Sie `Modules` aus der Liste **[!UICONTROL Groups]** aus.
1. Klicken Sie auf **[!UICONTROL Create]**.
1. Nachdem der Bericht generiert wurde, klicken Sie auf **[!UICONTROL Select]** und dann auf **[!UICONTROL View]** , um alle Modulversionen anzuzeigen.
1. Klicken Sie auf **[!UICONTROL Download]** , um den Bericht herunterzuladen.

### Systemberichte verwalten

Wählen Sie in der Spalte **[!UICONTROL Action]** des Rasters eine der folgenden Optionen aus:

- `View` - Verwenden Sie diese Funktion, um die Details des Berichts anzuzeigen.
- `Delete` - Mit dieser Funktion können Sie den generierten Bericht aus der Liste löschen.
- `Download` - Mit dieser Funktion kann der Bericht als HTML-Datei gespeichert werden.

### Anzeigen von Systemberichtsdetails

1. Wählen Sie für den benötigten Bericht **[!UICONTROL View]** in der Spalte _[!UICONTROL Actions]_&#x200B;aus.

1. Erweitern Sie im linken Bereich ![Erweiterungsauswahl](../assets/icon-display-expand.png) jeden Abschnitt des Berichts, um die Details anzuzeigen.

   ![Allgemeine Informationen zu Systemberichten](./assets/report-information.png){width="600" zoomable="yes"}

### Verfügbare Systemberichte

| Berichtsgruppe | Enthaltene Informationen |
| ------------ | -------------------- |
| [!UICONTROL General] | Adobe Commerce version<br>data count<br>cache status<br>index status |
| [!UICONTROL Environment] | Umgebungsinformationen/<br>-Status |
| [!UICONTROL Data] | Kategorien nach URL-Schlüssel duplizieren<br> Produkte nach URL-Schlüssel duplizieren<br> Produkte nach SKU duplizieren<br> Bestellungen nach Inkrement-ID <br>Duplizieren von Benutzern nach E-Mail<br>beschädigte Kategoriedaten |
| [!UICONTROL Modules] | Benutzerdefinierte Module Liste<br>Deaktivierte Module Liste<br>Alle Module Liste |
| [!UICONTROL Configuration] | Konfiguration<br>Daten aus der Funktionsmatrix `app/etc/env.php`<br>Versandmethoden<br>Zahlungsmethoden<br>Zahlungen |
| [!UICONTROL Logs] | Protokolldateien<br>Top-Systemmeldungen<br>Aktuelle Top-Systemmeldungen<br>Top-Debugmeldungen<br>Aktuelle Top-Debugmeldungen<br>Top-Ausnahmemeldungen<br>Aktuelle Top-Ausnahmemeldungen |
| [!UICONTROL Attributes] | Benutzerdefinierte EAV-Attribute<br>neue EAV-Attribute<br>Entitätstypen<br>Alle EAV-Attribute<br>Kategorie-EAV-Attribute<br>Produkt-EAV-Attribute<br>Kunden-EAV-Attribute<br>Kundenadresse EAV-Attribut<br>RMA-Element EAV-Attribute |
| [!UICONTROL Events] | Benutzerdefinierte globale Ereignisse<br>benutzerdefinierte Admin-Ereignisse<br>benutzerdefinierte Frontend-Ereignisse<br>benutzerdefinierte Dokumentereignisse<br>benutzerdefinierte Crontab-Ereignisse<br>benutzerdefinierte REST-Ereignisse<br>benutzerdefinierte SOAP-Ereignisse<br>Core-globale Ereignisse<br>Core-Admin-Ereignisse<br>Core-Frontend-Ereignisse<br>Core-Doc-Ereignisse<br><br> Core-Crontab-Ereignisse<br>Core-SOAP-Ereignisse<br>Alle globalen Ereignisse<br>Alle Admin-Ereignisse<br><br> Alle Doc-Ereignisse<br>Alle REST-Ereignisse<br>Alle SOAP-Ereignisse<br> alle Crontab-Ereignisse |
| [!UICONTROL Cron] | Cron-Zeitpläne nach Status-Code<br>Cron-Zeitpläne nach Auftrags-Code<br>Fehler in Cron-Zeitplänen Warteschlange<br>Cron-Zeitplanliste<br>Benutzerdefinierte globale Cron-Aufträge<br>Benutzerdefinierte konfigurierbare Cron-Aufträge<br>Core-globale Cron-Aufträge<br>Core konfigurierbare Cron-Aufträge<br>Alle globalen Cron-Aufträge<br>Alle konfigurierbaren Cron-Aufträge |
| [!UICONTROL Design] | AdminHTML-Designliste<br>Frontend-Designliste |
| [!UICONTROL Stores] | Website-Baumstruktur<br>Websites-Liste<br>Stores-Liste<br>Store-Ansichten-Liste |
| OMS-Connector <br>_(sichtbar mit OMS-Integration)_ | Ergebnisse <br> Connector-<br>-Connector-Überwachung |

{style="table-layout:auto"}
