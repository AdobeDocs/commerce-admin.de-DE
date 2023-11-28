---
title: Content-Staging-Dashboard
description: Greifen Sie über das Dashboard für die Inhaltstaging-Umgebung auf eine Übersicht aller aktiven und künftigen Kampagnen zu.
exl-id: 67c18c1c-94c3-4d89-ae1e-868a465431e3
feature: Page Content, Staging
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 0%

---

# Content-Staging-Dashboard

{{ee-feature}}

Die [!UICONTROL Content Staging] Das Dashboard bietet einen Überblick über alle aktiven und künftigen Kampagnen. Das Format des Dashboards kann von einem Raster zu einer Timeline geändert werden. Sie können auch Filter verwenden, um Kampagnen zu finden, das Spaltenlayout anzupassen und verschiedene Ansichten des Rasters zu speichern. Weitere Informationen zu den Steuerelementen in Workspace finden Sie unter [Admin Workspace](../getting-started/admin-workspace.md).

![Staging-Dashboard in Rasteransicht](./assets/content-staging-grid-view.png){width="600" zoomable="yes"}

## Anzeigen des Staging-Dashboards

1. Im _Admin_ Seitenleiste, navigieren Sie zu  **[!UICONTROL Content]** > _[!UICONTROL Content Staging]_>**[!UICONTROL Dashboard]**.

1. Um das Format des Dashboards zu ändern, legen Sie die **[!UICONTROL View As]** Kontrolle an `list`, `Grid`oder `Timeline`.

   ![Timeline-Ansicht](./assets/content-staging-dashboard-timeline.png){width="600" zoomable="yes"}

   Wenn die Timeline angezeigt wird, kann der Regler in der rechten unteren Ecke verwendet werden, um die Ansicht von einer bis vier Wochen anzupassen. Jede Spalte steht für einen Tag.

1. Wenn die Timeline angezeigt wird, ziehen Sie den Regler auf die `4w` Position ganz rechts, um einen längeren Zeitraum anzuzeigen.

   ![Vierwöchige Ansicht](./assets/content-staging-timeline-4-week-view.png){width="600" zoomable="yes"}

1. Um allgemeine Informationen zur Kampagne anzuzeigen, klicken Sie auf ein beliebiges Element auf der Seite.

   - Klicken Sie auf **[!UICONTROL View/Edit]**.

   - Um zu sehen, wie die Kampagne für Kunden im Store an diesem Tag aussieht, klicken Sie auf **[!UICONTROL Preview]**.

   ![Kampagneninformationen](./assets/content-staging-campaign-info.png){width="600" zoomable="yes"}

## Spaltenbeschreibungen im Staging-Dashboard

| Spalte | Beschreibung |
|--- |--- |
| [!UICONTROL Status] | Status der Kampagne. `Active` oder `Upcoming`. |
| [!UICONTROL Update Name] | Der Name der Kampagne. |
| [!UICONTROL Includes] | Definiert, wie viele Objekte in die Kampagne eingeschlossen sind. |
| [!UICONTROL Start Time] | Das Datum, an dem die Kampagne beginnt. |
| [!UICONTROL End Time] | Das Datum, an dem die Kampagne endet. |
| [!UICONTROL Description] | Zusätzliche Beschreibung jeder Kampagne. |
| [!UICONTROL Action] | Folgende Aktionen können auf einzelne Datensätze angewendet werden:<br/>**[!UICONTROL View/Edit]**- Öffnet die Kampagne im Bearbeitungsmodus.<br/>**[!UICONTROL Preview]** - Zeigt die Kampagne im Vorschaumodus an. |

{style="table-layout:auto"}

## Eine Kampagne bearbeiten

Vorhandene Kampagnenobjekte können über das Staging-Dashboard bearbeitet werden, mit Ausnahme von Preisregel-Kampagnen, die keine Enddaten haben.

>[!NOTE]
>
>Wenn eine Kampagne, die eine Preisregel enthält, zunächst ohne Enddatum erstellt wird, kann die Kampagne später nicht so bearbeitet werden, dass ein Enddatum enthalten ist. In diesem Fall ist es erforderlich, eine doppelte Kampagne zu erstellen und das erforderliche Enddatum einzugeben.

![Kampagnendetails](./assets/content-staging-dashboard-view-edit.png){width="600" zoomable="yes"}

Die Kampagne in diesem Beispiel umfasst zwei Kategorien und drei einzelne Produkte.

Gehen Sie wie folgt vor, um die Objekte dieser Kampagne zu bearbeiten.

1. Im _Admin_ Seitenleiste, navigieren Sie zu  **[!UICONTROL Content]** > _[!UICONTROL Content Staging]_>**[!UICONTROL Dashboard]**.

1. Suchen Sie die Kampagne in der angezeigten Liste oder Timeline und öffnen Sie sie, um auf die Details zuzugreifen:

   - Klicken Sie für eine Listenanzeige auf **[!UICONTROL Select]** und dann **[!UICONTROL View/Edit]** im _[!UICONTROL Action]_Spalte.
   - Klicken Sie für eine Timeline-Anzeige einmal, um die Zusammenfassung anzuzeigen, und klicken Sie dann auf **[!UICONTROL View/Edit]**.

1. Aktualisieren Sie eine der Einstellungen im _[!UICONTROL General]_nach Bedarf.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) alle Abschnitte, die ein zu bearbeitendes Element enthalten.

   ![Zugewiesene Produkte für ein Kampagnenelement aktualisieren](./assets/content-staging-campaign-edit-products.png){width="600" zoomable="yes"}

1. Klicken **[!UICONTROL Save]**.
