---
title: Systemsicherungen
description: Erfahren Sie, wie Sie Systemsicherungen erstellen und planen, einschließlich Dateisystem, Datenbank und Mediendateien.
exl-id: 3a9655c1-c124-42be-a487-b31404dada90
feature: System, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 0%

---

# Systemsicherungen

Mit Adobe Commerce und Magento Open Source können Sie verschiedene Systemteile wie Dateisystem, Datenbank und Mediendateien sichern und automatisch zurücksetzen. Ein Datensatz für jedes Backup wird im Raster auf der Seite _Backups_ angezeigt. Durch das Löschen eines Datensatzes aus der Liste wird auch die archivierte Datei gelöscht. Datenbanksicherungsdateien werden im GZ-Format komprimiert. Für die System-Backups sowie die Datenbank- und Mediensicherungen wird das TGZ-Format verwendet. Als Best Practice sollten Sie den Zugriff auf Backup-Tools einschränken und vor der Installation von Erweiterungen und Aktualisierungen sichern.

- **Schränken Sie den Zugriff auf Backup-Tools ein.** Der Zugriff auf das Sicherungs- und Rollback-Verwaltungstool kann eingeschränkt werden, indem [Benutzerrollen](permissions-user-roles.md) für Backup- und Rollback-Ressourcen konfiguriert werden. Lassen Sie das entsprechende Kontrollkästchen deaktiviert, um den Zugriff zu beschränken. Um Zugriff auf Rollback-Ressourcen zu gewähren, müssen Sie auch Zugriff auf Backup-Ressourcen gewähren.

- **Sichern Sie sich vor der Installation von Erweiterungen und Updates.** Führen Sie immer eine Sicherung durch, bevor Sie eine Erweiterung oder ein Update installieren.

{{$include /help/_includes/backups-note.md}}

## Sicherungen aktivieren und planen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Advanced]** und wählen Sie **[!UICONTROL System]** aus.

1. Erweitern Sie ![Erweiterungsselektor](../assets/icon-display-expand.png) den **[!UICONTROL Backup Settings]**.

1. Setzen Sie **[!UICONTROL Enabled Schedule Backup]** auf `Yes`.

1. Um automatische Sicherungen zu planen, legen Sie die Planungsoptionen fest:

   - Setzen Sie **[!UICONTROL Enabled Schedule Backup]** auf `Yes`.
   - Setzen Sie **[!UICONTROL Scheduled Backup Type]** auf den Sicherungstyp, der im geplanten Intervall ausgeführt werden soll.
   - Stellen Sie **[!UICONTROL Start Time]** auf die Tageszeit ein, um den Sicherungsvorgang auszuführen.
   - Setzen Sie **[!UICONTROL Frequency]** auf `Daily`, `Weekly` oder `Monthly`.
   - Setzen Sie **[!UICONTROL Maintenance Mode]** auf `Yes`.

   ![Erweiterte Konfiguration - Sicherungen](../configuration-reference/advanced/assets/system-scheduled-backup-settings.png){width="600" zoomable="yes"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

## Erstellen eines Backups

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Backups]**.

1. Klicken Sie oben rechts auf den zu erstellenden Sicherungstyp:

   - **[!UICONTROL System Backup]** - Erstellt eine vollständige Sicherung der Datenbank und des Dateisystems. Während des Vorgangs können Sie den Ordner media in die Sicherung einbeziehen.

   - **[!UICONTROL Database and Media Backup]** - Erstellt eine Sicherung der Datenbank und des Medienordners.

   - **[!UICONTROL Database Backup]** - Erstellt eine Sicherung der Datenbank.

   ![Systemwerkzeuge - Sicherungen](./assets/tools-backups.png){width="600" zoomable="yes"}

1. Um den Speicher während der Sicherung in den Wartungsmodus zu versetzen, aktivieren Sie das Kontrollkästchen.

   Nach Abschluss des Backups wird der Wartungsmodus automatisch deaktiviert.

1. Aktivieren Sie für eine Systemsicherung das Kontrollkästchen &quot;**[!UICONTROL Include Media folder to System Backup]**&quot;, um den Medienordner einzuschließen.

1. Bestätigen Sie die Aktion, wenn Sie dazu aufgefordert werden.


