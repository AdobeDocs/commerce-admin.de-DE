---
title: Systemsicherungen
description: Erfahren Sie, wie Sie Systemsicherungen erstellen und planen, einschließlich Dateisystem-, Datenbank- und Mediendateien.
exl-id: 3a9655c1-c124-42be-a487-b31404dada90
feature: System, Configuration
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/de/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
TQID: https://experienceleague.adobe.com/kx2acbOSrWMJGv3ST6qKAXjLPgL2Lsh16wWvOxNO7FE
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 391
ht-degree: 0%

---

# Systemsicherungen

Mit Adobe Commerce und Magento Open Source können Sie verschiedene Teile des Systems sichern, z. B. das Dateisystem, die Datenbank und Mediendateien, und das Rollback automatisch durchführen. Für jedes Backup wird auf der Seite „Backups _ein Datensatz im Raster_. Wenn Sie einen Datensatz aus der Liste löschen, wird auch die archivierte Datei gelöscht. Die Backup-Dateien der Datenbank werden im GZ-Format komprimiert. Für die Systemsicherungen und die Datenbank- und Mediensicherungen wird das TGZ-Format verwendet. Als Best Practice sollten Sie den Zugriff auf Sicherungs-Tools einschränken und Sicherungskopien erstellen, bevor Sie Erweiterungen und Aktualisierungen installieren.

- **Beschränken des Zugriffs auf Backup-Tools.** Der Zugriff auf das Backup- und Rollback-Management-Tool kann durch die Konfiguration von [Benutzerrollen](permissions-user-roles.md) für Backup- und Rollback-Ressourcen eingeschränkt werden. Um den Zugriff einzuschränken, lassen Sie das entsprechende Kontrollkästchen deaktiviert. Um Zugriff auf Rollback-Ressourcen zu gewähren, müssen Sie auch Zugriff auf Backup-Ressourcen gewähren.

- **Sichern Sie diese, bevor Sie Erweiterungen und Updates installieren.** Führen Sie immer eine Sicherung durch, bevor Sie eine Erweiterung oder ein Update installieren.

{{$include /help/_includes/backups-note.md}}

## Aktivieren und Planen von Backups

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Advanced]** und wählen Sie **[!UICONTROL System]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Backup Settings]**.

1. Legen Sie **[!UICONTROL Enabled Schedule Backup]** auf `Yes` fest.

1. Um automatische Sicherungen zu planen, legen Sie die Planungsoptionen fest:

   - Legen Sie **[!UICONTROL Enabled Schedule Backup]** auf `Yes` fest.
   - Legen Sie **[!UICONTROL Scheduled Backup Type]** auf den Typ des Backups fest, das im geplanten Intervall ausgeführt werden soll.
   - Legen Sie **[!UICONTROL Start Time]** auf die Tageszeit fest, zu der der Backup-Vorgang ausgeführt werden soll.
   - **[!UICONTROL Frequency]** auf `Daily`, `Weekly` oder `Monthly` festlegen.
   - Legen Sie **[!UICONTROL Maintenance Mode]** auf `Yes` fest.

   ![Erweiterte Konfiguration - Sicherungen](../configuration-reference/advanced/assets/system-scheduled-backup-settings.png){width="600" zoomable="yes"}

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

## Erstellen eines Backups

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Backups]**.

1. Klicken Sie oben rechts auf den Typ der Sicherung, die Sie erstellen möchten:

   - **[!UICONTROL System Backup]** - Erstellt eine vollständige Sicherung der Datenbank und des Dateisystems. Während des Vorgangs können Sie den Medienordner in die Sicherung einbeziehen.

   - **[!UICONTROL Database and Media Backup]** - Erstellt eine Sicherung der Datenbank und des Medienordners.

   - **[!UICONTROL Database Backup]** - Erstellt ein Backup der Datenbank.

   ![Systemtools - Sicherungen](./assets/tools-backups.png){width="600" zoomable="yes"}

1. Um den Speicher während des Backups in den Wartungsmodus zu versetzen, aktivieren Sie das Kontrollkästchen.

   Nach Abschluss des Backups wird der Wartungsmodus automatisch deaktiviert.

1. Aktivieren Sie für eine Systemsicherung das Kontrollkästchen **[!UICONTROL Include Media folder to System Backup]** , um den Medienordner einzuschließen.

1. Bestätigen Sie die Aktion, wenn Sie dazu aufgefordert werden.



<!-- Last updated from includes: 2023-02-22 09:59:54 -->
