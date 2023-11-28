---
title: Bericht "Action Logs"
description: Erfahren Sie, wie Sie den Bericht Aktionsprotokoll anzeigen, filtern und exportieren, der einen detaillierten Datensatz aller protokollaktivierten Admin-Aktionen bereitstellt.
exl-id: f2be5852-9185-4f14-b0bb-44d779b40819
feature: Logs, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 0%

---

# Bericht &quot;Action Logs&quot;

{{ee-feature}}

Die _Aktionsprotokolle_ zeigt einen detaillierten Datensatz aller Admin-Aktionen an, die für die Protokollierung aktiviert sind. Jeder Datensatz ist mit einem Zeitstempel versehen und zeichnet die IP-Adresse und den Namen des Benutzers auf. Die Protokolldetails enthalten Admin-Benutzerdaten und zugehörige Änderungen, die während der Aktion vorgenommen wurden.

Die Aktionen, die Sie im Bericht anzeigen möchten, müssen im [Protokollierung von Admin-Aktionen](action-log.md) in den Store-Einstellungen. Wenn der Aktionstyp aktiviert (aktiviert) ist, werden diese Arten von Admin-Aktionen im Bericht &quot;Aktionsprotokolle&quot;angezeigt.

Der Bericht kann mithilfe der Optionen in den einzelnen Spalten gefiltert werden. Sie können eine Einzelfilteroption festlegen oder Filteroptionen für mehrere Spalten festlegen, um den Bericht auf die Auflistung bestimmter Aktionen zu beschränken. Sie können Berichtsdaten auch im CSV- oder Excel-XML-Format exportieren.

Der Bericht &quot;Aktionsprotokolle&quot;enthält die folgenden Informationen:

- **[!UICONTROL Time]** - Datum und Uhrzeit der Aktion
- **[!UICONTROL Action Group]** - Zeigt den Aktionstyp an, korreliert mit den in aktivierten Aktionen. _Protokollierung von Admin-Aktionen_ Bildschirm in den Store-Einstellungen
- **[!UICONTROL Action]** - Zeigt die protokollierte Aktion an
- **[!UICONTROL IP Address]** - Zeigt die IP-Adresse des Computers an, auf dem die Aktion ausgeführt wurde
- **[!UICONTROL Username]** - Zeigt die Anmelde-ID des Benutzers an, der die Aktion ausgeführt hat
- **[!UICONTROL Result]** - Zeigt den Erfolg oder Misserfolg der Benutzeraktion an
- **[!UICONTROL Full Action Name]** - Zeigt den Namen der Backend-Aktion an
- **[!UICONTROL Details]** - Zeigt die Kategorie der Backend-Aktion an
- **[!UICONTROL Full Details]** - Zeigt alle protokollierten Details der Administratoraktion an

## Bericht &quot;Aktionsprotokolle&quot;anzeigen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL System]** > _[!UICONTROL Actions Logs]_>**[!UICONTROL Report]**.

   ![Aktionsprotokolle](./assets/action-log-report.png){width="600" zoomable="yes"}

1. Um die vollständigen Details einer aufgelisteten Admin-Aktion anzuzeigen, klicken Sie auf **[!UICONTROL View]**.

   ![Details zum Action Log-Eintrag](./assets/action-log-report-view.png){width="600" zoomable="yes"}

## Bericht &quot;Aktionsprotokolle&quot;filtern

Sie können die Felder für Filteroptionen definieren und auf **[!UICONTROL Search]** , um die angezeigten Aktionen einzuschränken.

Um die Filteroptionen zu löschen und zum vollständigen Bericht zurückzukehren, klicken Sie auf **[!UICONTROL Reset Filter]**.

![Filter für Aktionsprotokolle](./assets/action-log-report-filters.png){width="600" zoomable="yes"}

| Feld | description |
|--- |--- |
| [!UICONTROL Time] | In **[!UICONTROL From]** klicken Sie auf , um ein Datum aus dem dynamischen Kalender auszuwählen und das Anfangsdatum für den Filter zu definieren. In **[!UICONTROL To]** klicken Sie auf , um ein Datum auszuwählen und das Enddatum für den Filter festzulegen. |
| [!UICONTROL Action Group] | Wählen Sie eine Aktionsgruppe aus. |
| [!UICONTROL Action] | Wählen Sie eine Aktion aus. |
| [!UICONTROL IP Address] | Geben Sie die IP-Adresse des für eine Aktion verwendeten Computers ein. |
| [!UICONTROL Username] | Wählen Sie einen Benutzernamen aus. Der Standardwert ist `All Users`. |
| [!UICONTROL Result] | Wählen Sie Erfolg oder Fehler aus. |
| [!UICONTROL Full Action Name] | Geben Sie Text für die Suche ein, die im Feld übereinstimmen soll. |
| [!UICONTROL Details] | Geben Sie Text für die Suche ein, die im Feld übereinstimmen soll. |

{style="table-layout:auto"}

## Bericht &quot;Aktionsprotokolle&quot;exportieren

1. Für **[!UICONTROL Export to]**, wählen Sie ein Exportformat aus:

   - `CSV` - Eine kommagetrennte Wertdatei mit Textdaten
   - `Excel XML` - Ein XML-basiertes Tabellendatenformat

1. Klicken **[!UICONTROL Export]**.

   Die generierte Datei wird automatisch für Downloads in Ihrem angegebenen Ordner gespeichert.

   ![Export von Aktionsprotokollen](./assets/action-log-report-export.png){width="200"}
