---
title: Aktionssteuerung
description: Erfahren Sie mehr über die Verwendung des Steuerelements Aktionen , um einen Vorgang auf einen oder mehrere Datensätze in Admin anzuwenden.
exl-id: 03f313a9-bc17-4151-a2c8-8906342f025d
source-git-commit: a3fb702d0b6e08c3aaaa0d6b5e07aa825026ef76
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 0%

---

# Aktionssteuerung

Wenn Sie mit einer Sammlung von Datensätzen im Raster arbeiten, können Sie mithilfe des Steuerelements Aktionen einen Vorgang auf einen oder mehrere Datensätze anwenden. Das Steuerelement Aktionen listet jeden Vorgang auf, der für den jeweiligen Datentyp verfügbar ist. Beispielsweise können Sie das Steuerelement Aktionen verwenden, um die Attribute ausgewählter Produkte zu aktualisieren und den Status von `Disabled` nach `Enabled`oder um Datensätze aus der Datenbank zu löschen.

Sie können so viele Änderungen wie nötig vornehmen und die Datensätze dann in einem Schritt aktualisieren. Es ist viel effizienter, als die Einstellungen für jedes Produkt einzeln zu ändern. Das Anwenden von Bearbeitungen auf einen Datensatz-Batch ist ein asynchroner Vorgang, der im Hintergrund ausgeführt wird, sodass Sie die Arbeit im Admin fortsetzen können, ohne warten zu müssen, bis der Vorgang abgeschlossen ist. Das System zeigt eine Meldung an, wenn die Aufgabe abgeschlossen ist.

Die Auswahl der verfügbaren Aktionen hängt von der Liste ab. Je nach ausgewählter Aktion können zusätzliche Optionen angezeigt werden. Wenn Sie beispielsweise den Status einer Datensatzgruppe ändern, muss eine _[!UICONTROL Status]_neben dem Steuerelement Aktionen mit zusätzlichen Optionen angezeigt.

## Schritt 1: Datensätze auswählen

Mit dem Kontrollkästchen in der ersten Spalte der Liste werden die einzelnen Datensätze identifiziert, die als Ziel für die Aktion festgelegt wurden. Die [Filtersteuerelemente](admin-grid-controls.md) kann verwendet werden, um die Liste auf die Datensätze zu beschränken, die für die Aktion als Ziel ausgewählt werden sollen.

1. Legen Sie bei Bedarf die Filter oben in jeder Spalte fest, um nur die Datensätze anzuzeigen, die Sie einbeziehen möchten.

1. Aktivieren Sie das Kontrollkästchen jedes Datensatzes, der ein Ziel für die Aktion ist, oder wählen Sie über die Spaltenauswahl eine Massenauswahl aus.

![Auswählen oder Aufheben der Auswahl aller oder aller Elemente auf der Seite](./assets/action-change-selection.png){width="500"}

## Schritt 2: Anwenden einer Aktion auf ausgewählte Datensätze

1. Legen Sie die **[!UICONTROL Actions]** -Steuerelement auf den Vorgang, den Sie anwenden möchten.

   **_Beispiel:_** Aktualisieren von Attributen

   - Aktivieren Sie in der Liste das Kontrollkästchen jedes zu aktualisierenden Datensatzes.

   - Legen Sie die **[!UICONTROL Actions]** Kontrolle an `Update Attributes`.

     ![Auswählen der Aktion &quot;Attribute aktualisieren&quot;](./assets/action-select.png){width="450"}

   - Klicken **[!UICONTROL Submit]**.

     Auf der Seite &quot;Attribute aktualisieren&quot;werden alle verfügbaren Attribute nach Gruppe im Bereich auf der linken Seite aufgelistet.

     ![Seite &quot;Attribute aktualisieren&quot;](./assets/action-update-attributes.png){width="700" zoomable="yes"}

   - Wählen Sie die **[!UICONTROL Change]** neben jedem Attribut und nehmen Sie die erforderlichen Änderungen vor.

   - Klicks **[!UICONTROL Save]** um die Attribute für die Gruppe der ausgewählten Datensätze zu aktualisieren.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Submit]**.

## Kontrollkästchen-Aktionen

| Aktion | Beschreibung |
|--- |--- |
| [!UICONTROL Select All] | Markiert das Kontrollkästchen aller Datensätze in der Liste. |
| [!UICONTROL Unselect All] | Löscht das Kontrollkästchen aller Datensätze in der Liste. |
| [!UICONTROL Select All on This Page] | Aktiviert das Kontrollkästchen der auf der aktuellen Seite angezeigten Datensätze. |
| [!UICONTROL Deselect All on This Page] | Löscht das Kontrollkästchen der auf der aktuellen Seite angezeigten Datensätze. |

{style="table-layout:auto"}
