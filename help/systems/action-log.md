---
title: Aktionsprotokolle
description: Erfahren Sie mehr über Aktionsprotokolle und wie Sie protokollierte Aktionen konfigurieren können, um alle Änderungen zu verfolgen, die an Ihrem Store vorgenommen wurden.
exl-id: a482adfe-a63f-428b-b078-7542a1e2ecee
feature: Logs, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# Aktionsprotokolle

{{ee-feature}}

Die Funktion &quot;Aktionsprotokolle&quot;zeichnet alle Änderungen auf, die von einem Administrator vorgenommen wurden, der in Ihrem Store arbeitet. Auf diese Weise können Sie alle Änderungen verfolgen, die an Ihrem Store vorgenommen wurden. Das Verfolgen dieser Änderungen sowie das Festlegen von [Administratorberechtigungen](permissions.md) für einen Benutzer kann dazu beitragen, Ihren Store vor unerwünschten Änderungen zu schützen.

Bei den meisten Admin-Aktionen umfassen die protokollierten Informationen die Aktion, den Namen des Benutzers, den Erfolg oder das Fehlschlagen der Aktion und die ID des Objekts, das von der Aktion betroffen ist. Die IP-Adresse und das Datum werden ebenfalls protokolliert.

Standardmäßig sind alle Admin-Aktionen aktiviert und protokolliert. Um die Protokollierung von Admin-Aktionen zu konfigurieren, überprüfen Sie die Optionen und aktivieren oder deaktivieren Sie das Kontrollkästchen für jeden Aktionstyp. Adobe Commerce protokolliert nur geprüfte Typen.

Zeigen Sie den Bericht [Aktionsprotokolle](action-log-report.md) an, um die protokollierten Admin-Aktionen und -Details zu überprüfen.

![Erweiterte Konfiguration - Protokollierung von Administratoraktionen](../configuration-reference/advanced/assets/admin-actions-logging.png){width="600" zoomable="yes"}

Eine detaillierte Liste der Konfigurationseinstellungen finden Sie unter [Protokollarchivierung von Admin-Aktionen](../configuration-reference/advanced/system.md) in der _Konfigurationsreferenz_.

## Konfigurieren von Admin-Aktionen für die Protokollierung

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Advanced]** und wählen Sie **[!UICONTROL Admin]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Admin Actions Logging]** und führen Sie für jede Aktion Folgendes aus:

   - Um die Admin-Protokollierung für die Aktion zu aktivieren, aktivieren Sie das Kontrollkästchen.
   - Um die Admin-Protokollierung für die Aktion zu deaktivieren, deaktivieren Sie das Kontrollkästchen .

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

## Protokoll der Admin-Aktionen archivieren

Admin-Aktionsprotokolle können für eine beliebige Anzahl von Tagen archiviert werden. Archive können auch nach einer bestimmten Dauer gelöscht werden.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Advanced]** und wählen Sie **[!UICONTROL System]** aus.

1. Erweitern Sie **[!UICONTROL Admin Action Log Archiving]** und legen Sie die Optionen fest:

   - **[!UICONTROL Logs Entry Lifetime, Days]** - Legen Sie die Anzahl der Tage fest, nach denen das archivierte Protokoll beibehalten werden soll.
   - **[!UICONTROL Log Archiving Frequency]** - Legen Sie die Häufigkeit für das Erstellen von Archiven fest.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.
