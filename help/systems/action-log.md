---
title: Aktionsprotokolle
description: Erfahren Sie mehr über Aktionsprotokolle und darüber, wie Sie protokollierte Aktionen konfigurieren können, um alle Änderungen an Ihrem Store zu verfolgen.
exl-id: a482adfe-a63f-428b-b078-7542a1e2ecee
feature: Logs, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# Aktionsprotokolle

{{ee-feature}}

Die Funktion „Aktionsprotokolle“ zeichnet jede Änderung auf, die von einem Administrator bzw. einer Administratorin, der bzw. die in Ihrem Geschäft arbeitet, vorgenommen wird. Auf diese Weise können Sie alle Änderungen verfolgen, die an Ihrem Store vorgenommen wurden. Das Tracking dieser Änderungen kann zusammen mit dem [ von ](permissions.md) für einen Benutzer dazu beitragen, Ihren Store vor unerwünschten Änderungen zu schützen.

Bei den meisten Admin-Aktionen umfassen die protokollierten Informationen die Aktion, den Namen des Benutzers, den Erfolg oder Misserfolg der Aktion und die ID des von der Aktion betroffenen Objekts. IP-Adresse und Datum werden ebenfalls protokolliert.

Standardmäßig werden alle Admin-Aktionen aktiviert und protokolliert. Um die Protokollierung von Admin-Aktionen zu konfigurieren, überprüfen Sie die Optionen und aktivieren oder deaktivieren Sie das Kontrollkästchen für jeden Aktionstyp. Adobe Commerce protokolliert nur aktivierte Typen.

Zeigen Sie den [Bericht zu Aktionsprotokollen](action-log-report.md) an, um protokollierte Admin-Aktionen und -Details zu überprüfen.

![Erweiterte Konfiguration - Protokollierung von Admin-Aktionen](../configuration-reference/advanced/assets/admin-actions-logging.png){width="600" zoomable="yes"}

Eine detaillierte Liste der Konfigurationseinstellungen finden Sie unter [Admin-](../configuration-reference/advanced/system.md)-Archivierung“ in _Konfigurationsreferenz_.

## Konfigurieren von Admin-Aktionen für die Protokollierung

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Advanced]** und wählen Sie **[!UICONTROL Admin]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Admin Actions Logging]** und führen Sie für jede Aktion die folgenden Schritte aus:

   - Um die Admin-Protokollierung für die Aktion zu aktivieren, aktivieren Sie das Kontrollkästchen.
   - Um die Admin-Protokollierung für die Aktion zu deaktivieren, deaktivieren Sie das Kontrollkästchen.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

## Administratoraktionsprotokoll archivieren

Admin-Aktionsprotokolle können für eine beliebige Anzahl von Tagen archiviert werden. Archive können auch nach einer bestimmten Dauer gelöscht werden.

1. Erweitern Sie im linken Bereich **[!UICONTROL Advanced]** und wählen Sie **[!UICONTROL System]**.

1. Erweitern Sie **[!UICONTROL Admin Action Log Archiving]** und legen Sie die Optionen fest:

   - **[!UICONTROL Logs Entry Lifetime, Days]** : Legen Sie die Anzahl der Tage fest, die das archivierte Protokoll aufbewahrt werden soll.
   - **[!UICONTROL Log Archiving Frequency]** : Legen Sie die Häufigkeit für die Erstellung von Archiven fest.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.
