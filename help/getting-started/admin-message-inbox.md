---
title: Admin-Nachrichten-Posteingang
description: Informieren Sie sich über den Posteingang der Admin-Nachricht, der wichtige und nützliche Nachrichten von Adobe und der [!DNL Commerce] System.
exl-id: c53bb0e4-9f18-4d40-8cc4-8c3b485f8d68
source-git-commit: 7b6d70e2f3052af69075790cec1f396e2505bf8b
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 0%

---

# Admin-Nachrichten-Posteingang

Ihr Geschäft erhält regelmäßig Nachrichten von Adobe. Die Nachrichten werden nach Wichtigkeit bewertet und können sich auf Systemaktualisierungen, Patches, neue Versionen, geplante Wartung oder bevorstehende Ereignisse beziehen. Das Glockensymbol in der Kopfzeile gibt die Anzahl der ungelesenen Nachrichten in Ihrem Posteingang an.

![Admin - eingehende Nachrichten](./assets/admin-inbox-summary.png){width="700" zoomable="yes"}

Die _[!UICONTROL Notifications]_-Seite listet alle Nachrichten nach Datum auf. Die_[!UICONTROL Action]_ -Befehle können verwendet werden, um einzelne Nachrichten als gelesen zu markieren, detailliertere Informationen anzuzeigen oder die Nachricht aus dem Posteingang zu entfernen.

Die Konfiguration bestimmt, wie oft der Posteingang aktualisiert wird und wie die Nachrichten zugestellt werden. Wenn Ihr Store-Administrator über eine sichere URL verfügt, müssen Benachrichtigungen über HTTPS bereitgestellt werden.

## Neue eingehende Nachrichten anzeigen

1. Klicken Sie auf **[!UICONTROL Notification]** in der Kopfzeile und lesen Sie die Zusammenfassung.

1. Führen Sie einen der folgenden Schritte aus:

   - Klicken Sie bei Bedarf auf die Nachricht, um den Volltext anzuzeigen.
   - Um die Nachricht zu löschen, klicken Sie auf das Löschsymbol rechts neben der Nachricht.
   - Um die vollständige Liste der Benachrichtigungen anzuzeigen, klicken Sie auf **[!UICONTROL See All]**.

## Kritische Nachricht beheben

Führen Sie für eine wichtige Nachricht einen der folgenden Schritte aus:

- Klicken **[!UICONTROL Read Details]**.
- Um das Warnhinweisfeld zu schließen, die Nachricht jedoch aktiv zu halten, klicken Sie auf **[!UICONTROL Close]**.

## Benachrichtigungen verwalten

1. Führen Sie einen der folgenden Schritte aus, um die Seite Benachrichtigungen zu öffnen:

   - Klicken Sie auf **[!UICONTROL Notification]** in der Kopfzeile. Wenn eine oder mehrere neue Nachrichten angezeigt werden, klicken Sie auf **[!UICONTROL See All]**.

   - Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Notifications]**.

1. Im **[!UICONTROL Action]** -Spalte einen der folgenden Schritte ausführen:

   - Klicken Sie für weitere Informationen auf **[!UICONTROL Read Details]** um die verknüpfte Seite in einem neuen Fenster zu öffnen.

   - Um die Nachricht in Ihrem Posteingang zu behalten, klicken Sie auf **[!UICONTROL Mark As Read]**.

     ![Admin - Markieren ausgewählter Benachrichtigungen als gelesen](./assets/admin-notifications-mark-as-read.png){width="700" zoomable="yes"}

   - Um die Nachricht zu löschen, klicken Sie auf **[!UICONTROL Remove]**.

1. Um eine Aktion auf mehrere Nachrichten anzuwenden, führen Sie einen der folgenden Schritte aus:

   - Aktivieren Sie das Kontrollkästchen in der ersten Spalte für jede Nachricht, die verwaltet werden soll.
   - Um mehrere Nachrichten auszuwählen, legen Sie die **[!UICONTROL Mass Actions]** nach Bedarf.

1. Legen Sie die **[!UICONTROL Actions]** ein Steuerelement zu einem der folgenden Elemente hinzufügen:

   - `Mark as Read`
   - `Remove`

1. Klicks **[!UICONTROL Submit]** , um den Prozess abzuschließen.

## Benachrichtigungen konfigurieren

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Navigationsbereich **[!UICONTROL Advanced]** und wählen **[!UICONTROL System]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png)die **[!UICONTROL Notifications]** Abschnitt.

   ![Benachrichtigungskonfiguration](./assets/system-notifications.png){width="600"}

1. Wenn Ihr Store-Administrator über eine [sichere URL](../stores-purchase/store-urls.md), set **[!UICONTROL Use HTTPS to Get Feed]** nach `Yes`.

1. Satz **[!UICONTROL Update Frequency]** um festzustellen, wie oft Ihr Posteingang aktualisiert wird.

   Das Intervall kann zwischen 1 und 24 Stunden betragen.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

Weitere Informationen zum [!UICONTROL System] Konfigurationsoptionen, siehe [_Konfigurationshandbuch_](../configuration-reference/advanced/system.md).
