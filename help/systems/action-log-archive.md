---
title: Aktions-Log-Archiv
description: Erfahren Sie, wie Sie das Admin-Aktionsprotokoll-Archiv konfigurieren und anzeigen.
exl-id: a839f1c6-b5e2-4881-bfaa-267e47585441
feature: Logs, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# Aktions-Log-Archiv

{{ee-feature}}

Das [&#x200B; „Aktionen](action-log.md)-Archiv listet die CSV-Protokolldateien auf, die auf dem Server gespeichert sind. In der Konfiguration können Sie angeben, wie lange die Protokolleinträge gespeichert werden und wie oft sie archiviert werden. Standardmäßig enthält der Dateiname das aktuelle Datum im ISO-Format:  `yyyyMMddHH`

>[!NOTE]
>
>Die Protokollarchivierung erfordert die Einrichtung eines [Cron](cron.md)Auftrags.

## Konfigurieren des Protokollarchivs

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Advanced]** und wählen Sie **[!UICONTROL System]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Admin Actions Log Archiving]** und legen Sie die folgenden Optionen fest:

   - **[!UICONTROL Log Entry Lifetime, Days]** - Geben Sie die Anzahl der Tage ein, nach denen die Protokolleinträge in der Datenbank gespeichert werden sollen, bevor sie entfernt werden.
   - **[!UICONTROL Log Archiving Frequency]** - Auf `Daily`, `Weekly` oder `Monthly` festlegen.

   ![Erweiterte Konfiguration - Archivierung des Administratoraktionsprotokolls](../configuration-reference/advanced/assets/system-admin-actions-log-archiving.png){width="600" zoomable="yes"}

   Eine detaillierte Liste der Konfigurationseinstellungen finden Sie unter [Admin-](../configuration-reference/advanced/system.md)-Archivierung“ in _Konfigurationsreferenz_.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

## Anzeigen des Archivs

Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL System]** > _[!UICONTROL Actions Logs]_>**[!UICONTROL Archive]**.

![Aktions-Log-Archiv](./assets/action-log-archive.png){width="600" zoomable="yes"}
