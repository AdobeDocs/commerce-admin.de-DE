---
title: Die Admin-Tools und der Arbeitsbereich
description: Erfahren Sie mehr über den Admin Workspace, der Zugriff auf alle Tools, Daten und Inhalte bietet, die zum Ausführen Ihres Stores verwendet werden.
exl-id: 61cc53ab-e1c5-4349-b306-a15eb7c5ab57
source-git-commit: 7b6d70e2f3052af69075790cec1f396e2505bf8b
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 0%

---

# Die Admin-Tools und der Arbeitsbereich

Der Admin-Arbeitsbereich bietet Zugriff auf alle Tools, Daten und Inhalte, die zum Ausführen Ihres Stores verwendet werden. Die standardmäßige Startseite kann in der Konfiguration festgelegt werden. Viele Admin-Seiten verfügen über ein Raster, das die Daten für den Abschnitt auflistet, mit einer Reihe von Tools zum Suchen, Sortieren, Filtern, Auswählen und Anwenden von Aktionen. Standardmäßig ist das [Dashboard](admin-dashboard.md) die Startseite für den Administrator. Sie können jedoch bei der Anmeldung eine beliebige andere Seite auswählen, die als Startseite angezeigt werden soll. Sie können auf das Logo in der Admin-Seitenleiste klicken, um zur Admin-Startseite zurückzukehren.

![Admin - Workspace](./assets/admin-workspace.png){zoomable="yes"}

## Workspace-Steuerelemente

| Kontrolle | Beschreibung |
|--- |--- |
| [!UICONTROL Global Search] | Mit dem Suchsymbol oben rechts können Sie einen beliebigen Wert in der Datenbank finden, einschließlich Produkt-, Kunden- und Bestellungsdatensätzen. |
| [!UICONTROL Grid Search] | Das Suchfeld über dem Raster kann verwendet werden, um die Rasteranzeige schnell nach Schlüsselwörtern zu filtern, die in den Datensätzen gefunden wurden. |
| [!UICONTROL Sort] | Die Kopfzeile jeder Spalte kann verwendet werden, um die Liste in auf- oder absteigender Reihenfolge zu sortieren. |
| [!UICONTROL Filters] | Definiert einen Satz von Suchparametern, der die Datensätze bestimmt, die im Raster angezeigt werden. Darüber hinaus können die Filter in der Kopfzeile einiger Spalten verwendet werden, um die Liste auf bestimmte Werte zu beschränken. Einige Filter verfügen über zusätzliche Optionen, die aus einem Listenfeld ausgewählt werden können. |
| [!UICONTROL Default View] | Bestimmt das standardmäßige Spalten-Layout des Rasters. |
| [!UICONTROL Columns] | Bestimmt die Auswahl von [Spalten](admin-grid-controls.md) und ihre Reihenfolge im Raster. Das Spalten-Layout kann geändert und als (_) gespeichert_. Standardmäßig sind nur einige der Spalten im Raster enthalten. |
| [!UICONTROL Paginate] | Die Steuerelemente für die Paginierung werden verwendet, um die zusätzlichen Ergebnisseiten anzuzeigen. |
| [!UICONTROL Actions] | Die Aktionssteuerung wendet einen Vorgang auf alle ausgewählten Datensätze an. |
| [!UICONTROL Select] | Das Select-Steuerelement wird verwendet, um mehrere Datensätze auszuwählen, die das Ziel der Aktion sein sollen. Optionen: `Select All` / `Deselect All` |

{style="table-layout:auto"}

## Workspace-Suche

Um einen Datensatz in der Datenbank zu finden, verwenden Sie das Lupensymbol in der Kopfzeile des _Admin_. Die Ergebnisse können Kunden, Produkte, Bestellungen oder beliebige verwandte Attribute umfassen. Wenn Sie beispielsweise einen Kundennamen eingeben, können die Ergebnisse den Kundendatensatz und alle Bestellungen enthalten, die mit dem Namen verknüpft sind.

![Admin Search Tool](./assets/admin-search.png){width="700" zoomable="yes"}

1. Klicken Sie in der Kopfzeile auf das Symbol _Suchen_ (![Lupe](../assets/icon-magnify-search.png)), um das Suchfeld zu öffnen.

1. Führen Sie einen der folgenden Schritte aus:

   - Um eine genaue Übereinstimmung zu finden, geben Sie die ersten Buchstaben dessen ein, was Sie suchen.
   - Um eine exakte Übereinstimmung zu finden, geben Sie das Wort oder mehrere Wörter ein, die Sie suchen möchten.

1. Klicken Sie in den angezeigten Suchergebnissen auf ein beliebiges Element, um den Datensatz zu öffnen.

## Ändern der Admin-Startseite

Das [Dashboard](admin-workspace.md#the-dashboard) ist die standardmäßige Startseite für Admins, obwohl Sie eine andere Startseite konfigurieren können.

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wählen Sie im linken Navigationsbereich unter **[!UICONTROL Advanced]** die Option **[!UICONTROL Admin]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Startup Page]** .

   ![Erweiterte Konfiguration - Admin-Startseiteneinstellung](./assets/admin-startup-page.png){width="600"}

1. Legen Sie **[!UICONTROL Startup Page]** auf die Seite fest, die nach der Anmeldung bei der Administratorin bzw. dem Administrator zuerst angezeigt werden soll.

   Eine detaillierte Liste aller Admin-Optionen finden Sie unter [Admin](../configuration-reference/advanced/admin.md) in der _Konfigurationsreferenz_.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.
