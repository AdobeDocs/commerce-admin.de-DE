---
title: Archivierungsaufträge
description: Erfahren Sie, wie Sie das Auftragsarchiv konfigurieren, um die Leistung zu verbessern und den Commerce für Ihr Unternehmen zu optimieren.
exl-id: 12025591-bfe2-4f44-9358-a38ea4493b5c
feature: Orders, Configuration
source-git-commit: 47f170f1a1dd1c236b99c2e7139bb119368abf47
workflow-type: tm+mt
source-wordcount: '745'
ht-degree: 0%

---

# Archivierungsaufträge

{{ee-feature}}

Durch die regelmäßige Archivierung von Bestellungen wird die Leistung gesteigert und Ihr Arbeitsbereich wird von unnötigen Informationen befreit, sodass Sie sich auf das aktuelle Geschäft konzentrieren können. Rechnungen, Sendungen und Kreditkarten können automatisch oder manuell archiviert und jederzeit eingesehen werden.

>[!NOTE]
>
>Die _[!UICONTROL Archive]_wird in der [[!UICONTROL Sales] Menü](sales-menu.md) nur, wenn die Archivierung [enabled](../configuration-reference/sales/sales.md).

## Bestellarchiv konfigurieren

Ihr Speicher kann so konfiguriert werden, dass Bestellungen, Rechnungen, Sendungen und Kreditkarten nach einer bestimmten Anzahl von Tagen archiviert werden. Sie können Bestellungen und die zugehörigen Dokumente in das Archiv verschieben oder wieder in ihren vorherigen Zustand zurücksetzen. Archivierte Bestellungen werden nicht gelöscht und bleiben beim Administrator verfügbar. Archivierte Daten können in eine CSV-Datei exportiert und in einer Tabelle geöffnet werden. Wenn diese Option aktiviert ist, wird die _Archivieren_ -Aktion wird oben im Arbeitsbereich angezeigt.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den **[!UICONTROL Sales]** auswählen **[!UICONTROL Sales]** darunter.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Orders, Invoices, Shipments, Credit Memos Archiving]** Abschnitt.

   ![Konfigurationseinstellungen für Bestellungen, Rechnungen, Sendungen, Credit Memos-Archivierung](../configuration-reference/sales/assets/sales-orders-invoices-shipments-credit-memos-archiving.png){width="600" zoomable="yes"}

1. Satz **[!UICONTROL Enable Archiving]** nach `Yes`.

   >[!NOTE]
   >
   >Wenn Sie die Archivierung später deaktivieren, werden alle archivierten Bestellungen wieder in den vorherigen Status versetzt.

1. Satz **[!UICONTROL Archive Orders Purchased]** auf die Anzahl der Tage, die gewartet werden muss, bevor abgeschlossene Bestellungen archiviert werden.

   Standardmäßig werden Bestellungen 30 Tage nach dem Kauf archiviert.

1. Im **[!UICONTROL Order Statuses to be Archived]** auswählen, wählen Sie jeden Bestellstatus aus, der zur Identifizierung der zu archivierenden Bestellungen verwendet werden soll.

   Um mehrere Elemente auszuwählen, halten Sie beim Klicken auf die einzelnen Elemente die Strg- (Windows) bzw. Befehlstaste (Mac) gedrückt.

1. Klicken **[!UICONTROL Save Config]**.

1. Aktualisieren Sie nach Aufforderung alle ungültigen Zwischenspeicher.

## Archivierte Dokumente anzeigen

1. Im _[!UICONTROL Sales]_Menü unter_[!UICONTROL Archive]_, wählen Sie eine der folgenden Optionen aus:

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

1. Legen Sie in der oberen rechten Ecke **[!UICONTROL Actions]** nach `Move to Archive`.

1. Klicks **[!UICONTROL Submit]** um die ausgewählten Dokumente zu archivieren.

## Archivierte Dokumente wiederherstellen

1. Wählen Sie den Dokumenttyp aus, den Sie wiederherstellen möchten.

1. Wählen Sie Dokumente mit einer der folgenden Optionen aus:

   - Um alle sichtbaren Dokumente auszuwählen, klicken Sie oben links auf **[!UICONTROL Select Visible]**.

   - Aktivieren Sie manuell das Kontrollkästchen jedes Dokuments, das Sie wiederherstellen möchten.

1. Legen Sie oben rechts **[!UICONTROL Action]** nach `Move to Orders Management`.

1. Klicks **[!UICONTROL Submit]** um die Dokumente wiederherzustellen.

## Exportieren archivierter Dokumente

1. Wählen Sie den Dokumenttyp aus, den Sie exportieren möchten.

1. Legen Sie im Menü oben rechts **[!UICONTROL Export to:]** auf einen der folgenden Werte zu setzen:

   - `CSV`
   - `Excel`

1. Klicken **[!UICONTROL Export]**.

Ihr Speicher kann so konfiguriert werden, dass Bestellungen, Rechnungen, Sendungen und Kreditkarten nach einer bestimmten Anzahl von Tagen archiviert werden. Sie können Bestellungen und die zugehörigen Dokumente in das Archiv verschieben oder wieder in ihren vorherigen Zustand zurücksetzen. Archivierte Bestellungen werden nicht gelöscht und bleiben beim Administrator verfügbar. Archivierte Daten können in eine CSV-Datei exportiert und in einer Tabelle geöffnet werden. Wenn diese Option aktiviert ist, wird die _[!UICONTROL Archive]_wird oben im Arbeitsbereich angezeigt.

## Manuelles Archivieren von Bestellungen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Um die Reihenfolge im Raster auszuwählen, aktivieren Sie das Kontrollkästchen in der ersten Spalte.

1. Legen Sie die **[!UICONTROL Actions]** Kontrolle an `Move to Archive` und suchen Sie nach der Meldung, dass die Bestellung archiviert wurde.

   ![Verschieben ausgewählter Bestellungen in das Archiv ](./assets/order-move-to-archive.png){width="700" zoomable="yes"}

>[!TIP]
>
>Eine Liste der zu archivierenden Bestellstatus finden Sie unter [Bestellarchiv konfigurieren](#configure-the-order-archive).

## Archivierte Reihenfolge anzeigen

1. Öffnen Sie die Archivansicht mit einer der folgenden Methoden:

   - In der Schaltflächenleiste über dem _[!UICONTROL Orders]_Raster, klicken **[!UICONTROL Go to Archive]**.

   - Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Sales]** > _[!UICONTROL Archive]_>**[!UICONTROL Orders]**.

   >[!NOTE]
   >
   >Wie auf der Seite &quot;Bestellungen&quot;lautet der Titel der archivierten Bestellungsseite _[!UICONTROL Orders]_. Der einzige erkennbare Unterschied ist die Option in der Schaltflächenleiste zum_[!UICONTROL Return to Orders Management]_. Die URL der Seite zeigt auch an, dass Sie sich im Bestellarchiv befinden.

1. Im _Aktion_ Spalte, klicken **[!UICONTROL View]**.

   ![Archivierte Reihenfolge anzeigen](./assets/order-archived-view.png){width="600" zoomable="yes"}

## Archivierte Reihenfolge wiederherstellen

>[!NOTE]
>
>Eine Bestellung, die aus einer archivierten Bestellung wiederhergestellt wird, wird entsprechend der in der [!UICONTROL Archive Orders Purchased] -Einstellung (siehe [Bestellarchiv konfigurieren](#configure-the-order-archive)). Die Anzahl der Tage wird anhand der [!UICONTROL Updated At] Datum für die Bestellung, das geändert wird, wenn die Bestellung aus dem Archiv verschoben wird.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Klicken Sie in der Symbolleiste auf **[!UICONTROL Go to Archive]**.

1. Suchen Sie den wiederherzustellenden Datensatz und klicken Sie auf das Kontrollkästchen, um ihn auszuwählen.

   ![Wählen Sie &quot;Reihenfolge wiederherstellen&quot;](./assets/order-archived-select-to-restore.png){width="600" zoomable="yes"}

1. Legen Sie die **[!UICONTROL Actions]** Kontrollwert zu `Move to Order Management`.

Suchen Sie nach der Meldung, dass die archivierte Bestellung aus dem Archiv entfernt wurde.

## Archivierte Reihenfolge exportieren

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Klicken Sie im Aktionsmenü auf **[!UICONTROL Export]** und wählen Sie das gewünschte Format aus.
