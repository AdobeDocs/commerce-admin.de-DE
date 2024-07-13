---
title: Aktionsprotokoll-Archiv
description: Erfahren Sie, wie Sie das Archiv für das Admin-Aktionsprotokoll konfigurieren und anzeigen.
exl-id: a839f1c6-b5e2-4881-bfaa-267e47585441
feature: Logs, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# Aktionsprotokoll-Archiv

{{ee-feature}}

Das Admin-Archiv [actions](action-log.md) listet die CSV-Protokolldateien auf, die auf dem Server gespeichert sind. In der Konfiguration können Sie angeben, wie lange die Protokolleinträge gespeichert werden und wie oft sie archiviert werden. Standardmäßig enthält der Dateiname das aktuelle Datum im ISO-Format:  `yyyyMMddHH`

>[!NOTE]
>
>Für die Protokollarchivierung muss ein [cron-Auftrag](cron.md) eingerichtet werden.

## Protokollarchiv konfigurieren

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Advanced]** und wählen Sie **[!UICONTROL System]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Admin Actions Log Archiving]** und legen Sie die folgenden Optionen fest:

   - **[!UICONTROL Log Entry Lifetime, Days]** - Geben Sie die Anzahl der Tage ein, nach denen die Protokolleinträge in der Datenbank beibehalten werden sollen, bevor sie entfernt werden.
   - **[!UICONTROL Log Archiving Frequency]** - Auf `Daily`, `Weekly` oder `Monthly` setzen.

   ![Erweiterte Konfiguration - Archivierung des Admin-Aktionsprotokolls](../configuration-reference/advanced/assets/system-admin-actions-log-archiving.png){width="600" zoomable="yes"}

   Eine detaillierte Liste der Konfigurationseinstellungen finden Sie unter [Protokollarchivierung von Admin-Aktionen](../configuration-reference/advanced/system.md) in der _Konfigurationsreferenz_.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

## Archiv anzeigen

Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL System]** > _[!UICONTROL Actions Logs]_>**[!UICONTROL Archive]**.

![Action log archive](./assets/action-log-archive.png){width="600" zoomable="yes"}
