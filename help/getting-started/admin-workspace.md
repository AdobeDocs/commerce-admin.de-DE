---
title: Admin Tools und Arbeitsbereich
description: Erfahren Sie mehr über den Admin Workspace, der Zugriff auf alle Tools, Daten und Inhalte bietet, die zum Ausführen Ihres Stores verwendet werden.
exl-id: 61cc53ab-e1c5-4349-b306-a15eb7c5ab57
source-git-commit: 7b6d70e2f3052af69075790cec1f396e2505bf8b
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 0%

---

# Admin Tools und Arbeitsbereich

Der Admin Workspace bietet Zugriff auf alle Tools, Daten und Inhalte, die zum Ausführen Ihres Stores verwendet werden. Die standardmäßige Startseite kann in der Konfiguration festgelegt werden. Viele Admin-Seiten verfügen über ein Raster, das die Daten für den Abschnitt auflistet, mit einer Reihe von Tools zum Suchen, Sortieren, Filtern, Auswählen und Anwenden von Aktionen. Standardmäßig ist das [Dashboard](admin-dashboard.md) die Startseite für den Admin. Sie können jedoch jede andere Seite auswählen, die bei der Anmeldung als Startseite angezeigt wird. Sie können auf das Logo in der Admin-Seitenleiste klicken, um zur Startseite &quot;Admin&quot;zurückzukehren.

![Admin - workspace](./assets/admin-workspace.png){zoomable="yes"}

## Workspace-Steuerelemente

| Kontrolle | Beschreibung |
|--- |--- |
| [!UICONTROL Global Search] | Das Suchsymbol oben rechts kann verwendet werden, um einen beliebigen Wert in der Datenbank zu finden, einschließlich Produkt-, Kunden- und Bestelldatensätzen. |
| [!UICONTROL Grid Search] | Das Suchfeld über dem Raster kann verwendet werden, um die Rasteranzeige anhand der in den Datensätzen gefundenen Schlüsselwörter schnell zu filtern. |
| [!UICONTROL Sort] | Die Kopfzeile jeder Spalte kann verwendet werden, um die Liste in auf- oder absteigender Reihenfolge zu sortieren. |
| [!UICONTROL Filters] | Definiert einen Satz von Suchparametern, die die im Raster angezeigten Datensätze bestimmen. Darüber hinaus können die Filter in der Kopfzeile einiger Spalten verwendet werden, um die Liste auf bestimmte Werte zu beschränken. Einige Filter verfügen über zusätzliche Optionen, die aus einem Listenfeld ausgewählt werden können. |
| [!UICONTROL Default View] | Legt das standardmäßige Spaltenlayout des Rasters fest. |
| [!UICONTROL Columns] | Bestimmt die Auswahl von [Spalten](admin-grid-controls.md) und deren Reihenfolge im Raster. Das Spaltenlayout kann geändert und als _Ansicht_ gespeichert werden. Standardmäßig sind nur einige der Spalten im Raster enthalten. |
| [!UICONTROL Paginate] | Mit den Paginierungssteuerelementen werden die zusätzlichen Ergebnisseiten angezeigt. |
| [!UICONTROL Actions] | Das Steuerelement Aktionen wendet einen Vorgang auf alle ausgewählten Datensätze an. |
| [!UICONTROL Select] | Das Steuerelement Auswählen wird verwendet, um mehrere Datensätze auszuwählen, die als Aktionsziel dienen sollen. Optionen: `Select All` / `Deselect All` |

{style="table-layout:auto"}

## Workspace-Suche

Um einen Datensatz in der Datenbank zu finden, verwenden Sie das Lupensymbol in der Kopfzeile von _Admin_. Die Ergebnisse können Kunden, Produkte, Bestellungen oder alle zugehörigen Attribute umfassen. Wenn Sie beispielsweise einen Kundennamen eingeben, können die Ergebnisse den Kundendatensatz und alle Bestellungen enthalten, die mit dem Namen verknüpft sind.

![Admin-Suchwerkzeug](./assets/admin-search.png){width="700" zoomable="yes"}

1. Klicken Sie in der Kopfzeile auf das Symbol _Suchen_ (![Lupe](../assets/icon-magnify-search.png)), um das Suchfeld zu öffnen.

1. Führen Sie einen der folgenden Schritte aus:

   - Um eine enge Übereinstimmung zu finden, geben Sie die ersten Buchstaben des gesuchten Inhalts ein.
   - Um eine genaue Übereinstimmung zu finden, geben Sie das Wort oder mehrere Wörter ein, die Sie finden möchten.

1. Klicken Sie in den angezeigten Suchergebnissen auf ein beliebiges Element, um den Datensatz zu öffnen.

## Admin-Startseite ändern

Das [Dashboard](admin-workspace.md#the-dashboard) ist die Standardstartseite für den Admin, Sie können jedoch eine andere Startseite konfigurieren.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wählen Sie im linken Navigationsbereich unter **[!UICONTROL Advanced]** die Option **[!UICONTROL Admin]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Startup Page]** .

   ![Erweiterte Konfiguration - Einstellung der Admin-Startseite](./assets/admin-startup-page.png){width="600"}

1. Setzen Sie **[!UICONTROL Startup Page]** auf die Seite, die nach der Anmeldung beim Administrator zuerst angezeigt werden soll.

   Eine detaillierte Liste aller Admin-Optionen finden Sie unter [Admin](../configuration-reference/advanced/admin.md) in der _Konfigurationsreferenz_.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.
