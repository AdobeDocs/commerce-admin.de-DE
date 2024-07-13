---
title: Archivierungsaufträge
description: Erfahren Sie, wie Sie das Auftragsarchiv konfigurieren, um die Leistung zu verbessern und Commerce für Ihr Unternehmen zu optimieren.
exl-id: 12025591-bfe2-4f44-9358-a38ea4493b5c
feature: Orders, Configuration
source-git-commit: 47f170f1a1dd1c236b99c2e7139bb119368abf47
workflow-type: tm+mt
source-wordcount: '746'
ht-degree: 0%

---

# Archivierungsaufträge

{{ee-feature}}

Durch die regelmäßige Archivierung von Bestellungen wird die Leistung gesteigert und Ihr Arbeitsbereich wird von unnötigen Informationen befreit, sodass Sie sich auf das aktuelle Geschäft konzentrieren können. Rechnungen, Sendungen und Kreditkarten können automatisch oder manuell archiviert und jederzeit eingesehen werden.

>[!NOTE]
>
>Die Option _[!UICONTROL Archive]_wird nur dann im [[!UICONTROL Sales] Menü](sales-menu.md) angezeigt, wenn die Archivierung [aktiviert](../configuration-reference/sales/sales.md) ist.

## Bestellarchiv konfigurieren

Ihr Speicher kann so konfiguriert werden, dass Bestellungen, Rechnungen, Sendungen und Kreditkarten nach einer bestimmten Anzahl von Tagen archiviert werden. Sie können Bestellungen und die zugehörigen Dokumente in das Archiv verschieben oder wieder in ihren vorherigen Zustand zurücksetzen. Archivierte Bestellungen werden nicht gelöscht und bleiben beim Administrator verfügbar. Archivierte Daten können in eine CSV-Datei exportiert und in einer Tabelle geöffnet werden. Wenn diese Option aktiviert ist, wird die Aktion _Archivieren_ oben im Arbeitsbereich angezeigt.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Abschnitt **[!UICONTROL Sales]** und wählen Sie unter &quot;**[!UICONTROL Sales]**&quot;.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Orders, Invoices, Shipments, Credit Memos Archiving]** .

   ![Konfigurationseinstellungen für Bestellungen, Rechnungen, Sendungen, Credit Memos-Archivierung](../configuration-reference/sales/assets/sales-orders-invoices-shipments-credit-memos-archiving.png){width="600" zoomable="yes"}

1. Setzen Sie **[!UICONTROL Enable Archiving]** auf `Yes`.

   >[!NOTE]
   >
   >Wenn Sie die Archivierung später deaktivieren, werden alle archivierten Bestellungen wieder in den vorherigen Status versetzt.

1. Setzen Sie **[!UICONTROL Archive Orders Purchased]** auf die Anzahl der Tage, die gewartet werden soll, bevor abgeschlossene Bestellungen archiviert werden.

   Standardmäßig werden Bestellungen 30 Tage nach dem Kauf archiviert.

1. Wählen Sie in der Liste **[!UICONTROL Order Statuses to be Archived]** jeden Bestellstatus aus, der zur Identifizierung der zu archivierenden Bestellungen verwendet werden soll.

   Um mehrere Elemente auszuwählen, halten Sie beim Klicken auf die einzelnen Elemente die Strg- (Windows) bzw. Befehlstaste (Mac) gedrückt.

1. Klicken Sie auf **[!UICONTROL Save Config]**.

1. Aktualisieren Sie nach Aufforderung alle ungültigen Zwischenspeicher.

## Archivierte Dokumente anzeigen

1. Wählen Sie im Menü _[!UICONTROL Sales]_unter_[!UICONTROL Archive]_ eine der folgenden Optionen aus:

   - **[!UICONTROL Orders]**
   - **[!UICONTROL Invoices]**
   - **[!UICONTROL Shipments]**
   - **[!UICONTROL Credit Memos]**

1. Um Details anzuzeigen, klicken Sie auf ein archiviertes Dokument in der Liste.

## Anwenden einer Aktion auf ein archiviertes Dokument

Wählen Sie jedes Dokument aus, um als Ziel der Aktion ausgewählt zu werden, und wählen Sie eines der folgenden **[!UICONTROL Actions]**:

- `Cancel`
- `Hold`
- `Unhold`
- `Print`
- `Move to Orders Management`

## Dokumente manuell archivieren

1. Wählen Sie den Typ des zu archivierenden Dokuments wie folgt aus:

   - **[!UICONTROL Orders]**
   - **[!UICONTROL Invoices]**
   - **[!UICONTROL Shipments]**
   - **[!UICONTROL Credit Memos]**

1. Aktivieren Sie das Kontrollkästchen jedes Elements, das Sie archivieren möchten.

1. Setzen Sie oben rechts **[!UICONTROL Actions]** auf `Move to Archive`.

1. Klicken Sie auf **[!UICONTROL Submit]** , um die ausgewählten Dokumente zu archivieren.

## Archivierte Dokumente wiederherstellen

1. Wählen Sie den Dokumenttyp aus, den Sie wiederherstellen möchten.

1. Wählen Sie Dokumente mit einer der folgenden Optionen aus:

   - Um alle sichtbaren Dokumente auszuwählen, klicken Sie in der oberen linken Ecke auf **[!UICONTROL Select Visible]**.

   - Aktivieren Sie manuell das Kontrollkästchen jedes Dokuments, das Sie wiederherstellen möchten.

1. Setzen Sie oben rechts **[!UICONTROL Action]** auf `Move to Orders Management`.

1. Klicken Sie auf **[!UICONTROL Submit]** , um die Dokumente wiederherzustellen.

## Exportieren archivierter Dokumente

1. Wählen Sie den Dokumenttyp aus, den Sie exportieren möchten.

1. Setzen Sie im Menü oben rechts **[!UICONTROL Export to:]** auf einen der folgenden Werte:

   - `CSV`
   - `Excel`

1. Klicken Sie auf **[!UICONTROL Export]**.

Ihr Speicher kann so konfiguriert werden, dass Bestellungen, Rechnungen, Sendungen und Kreditkarten nach einer bestimmten Anzahl von Tagen archiviert werden. Sie können Bestellungen und die zugehörigen Dokumente in das Archiv verschieben oder wieder in ihren vorherigen Zustand zurücksetzen. Archivierte Bestellungen werden nicht gelöscht und bleiben beim Administrator verfügbar. Archivierte Daten können in eine CSV-Datei exportiert und in einer Tabelle geöffnet werden. Wenn diese Option aktiviert ist, wird der Befehl _[!UICONTROL Archive]_oben im Arbeitsbereich angezeigt.

## Manuelles Archivieren von Bestellungen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Um die Reihenfolge im Raster auszuwählen, aktivieren Sie das Kontrollkästchen in der ersten Spalte.

1. Setzen Sie das Steuerelement **[!UICONTROL Actions]** auf `Move to Archive` und suchen Sie nach der Meldung, dass die Bestellung archiviert wurde.

   ![Verschieben ausgewählter Bestellungen in das Archiv ](./assets/order-move-to-archive.png){width="700" zoomable="yes"}

>[!TIP]
>
>Informationen zum Angeben einer Liste der Bestellstatus, die archiviert werden können, finden Sie unter [Konfigurieren des Bestellarchivs](#configure-the-order-archive).

## Archivierte Reihenfolge anzeigen

1. Öffnen Sie die Archivansicht mit einer der folgenden Methoden:

   - Klicken Sie in der Schaltflächenleiste über dem Raster _[!UICONTROL Orders]_auf **[!UICONTROL Go to Archive]**.

   - Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Sales]** > _[!UICONTROL Archive]_>**[!UICONTROL Orders]**.

   >[!NOTE]
   >
   >Wie auf der Seite &quot;Bestellungen&quot;lautet der Titel der Seite mit den archivierten Bestellungen _[!UICONTROL Orders]_. Der einzige merkliche Unterschied ist die Option in der Schaltflächenleiste zu_[!UICONTROL Return to Orders Management]_. Die URL der Seite zeigt auch an, dass Sie sich im Bestellarchiv befinden.

1. Klicken Sie in der Spalte _Aktion_ auf **[!UICONTROL View]**.

   ![Archivierte Bestellung anzeigen](./assets/order-archived-view.png){width="600" zoomable="yes"}

## Archivierte Reihenfolge wiederherstellen

>[!NOTE]
>
>Eine Bestellung, die aus einer archivierten Bestellung wiederhergestellt wird, wird entsprechend der Anzahl der Tage, die in der Einstellung [!UICONTROL Archive Orders Purchased] konfiguriert wurden, erneut archiviert (siehe [Konfigurieren des Bestellarchivs](#configure-the-order-archive)). Die Anzahl der Tage wird anhand des [!UICONTROL Updated At] -Datums für die Bestellung berechnet, das geändert wird, wenn die Bestellung aus dem Archiv verschoben wird.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Klicken Sie in der Schaltflächenleiste auf **[!UICONTROL Go to Archive]**.

1. Suchen Sie den wiederherzustellenden Datensatz und klicken Sie auf das Kontrollkästchen, um ihn auszuwählen.

   ![Wählen Sie die Reihenfolge aus, die wiederhergestellt werden soll](./assets/order-archived-select-to-restore.png){width="600" zoomable="yes"}

1. Setzen Sie den Kontrollwert **[!UICONTROL Actions]** auf `Move to Order Management`.

Suchen Sie nach der Meldung, dass die archivierte Bestellung aus dem Archiv entfernt wurde.

## Archivierte Reihenfolge exportieren

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Klicken Sie im Aktionsmenü auf **[!UICONTROL Export]** und wählen Sie das gewünschte Format aus.
