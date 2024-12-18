---
title: Bericht zu Aktionslogs
description: Erfahren Sie, wie Sie den Bericht zum Aktionsprotokoll anzeigen, filtern und exportieren, der einen detaillierten Datensatz aller protokollierten Admin-Aktionen bereitstellt.
exl-id: f2be5852-9185-4f14-b0bb-44d779b40819
feature: Logs, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 0%

---

# Bericht zu Aktionslogs

{{ee-feature}}

Der _Aktionsprotokolle_ zeigt einen detaillierten Datensatz aller Admin-Aktionen an, die für die Protokollierung aktiviert sind. Jeder Datensatz erhält einen Zeitstempel und enthält die IP-Adresse und den Namen des Benutzers. Die Protokolldetails enthalten Admin-Benutzerdaten und zugehörige Änderungen, die während der Aktion vorgenommen wurden.

Aktionen, die im Bericht angezeigt werden sollen, müssen auf dem Bildschirm [Admin-Aktionsprotokollierung](action-log.md) in den Store-Einstellungen aktiviert werden. Wenn der Aktionstyp aktiviert (aktiviert) ist, werden diese Arten von Admin-Aktionen im Bericht „Aktionsprotokolle“ angezeigt.

Der Bericht kann mithilfe der Optionen in den einzelnen Spalten gefiltert werden. Sie können eine einzelne Filteroption oder Filteroptionen für mehrere Spalten festlegen, um den Bericht auf bestimmte Aktionen einzugrenzen. Sie können Berichtsdaten auch im CSV- oder Excel-XML-Format exportieren.

Der Bericht „Aktionsprotokolle“ enthält die folgenden Informationen:

- **[!UICONTROL Time]** - Datum und Uhrzeit des Vorgangs
- **[!UICONTROL Action Group]** - Zeigt den Aktionstyp an, der mit den Aktionen korreliert, die auf dem Bildschirm _Admin-Aktionsprotokollierung_ in Ihren Store-Einstellungen aktiviert sind.
- **[!UICONTROL Action]** - Zeigt die protokollierte Aktion an
- **[!UICONTROL IP Address]** - Zeigt die IP-Adresse des Computers an, auf dem die Aktion ausgeführt wurde
- **[!UICONTROL Username]** - Zeigt die Anmelde-ID des Benutzers an, der die Aktion ausgeführt hat
- **[!UICONTROL Result]** : Zeigt den Erfolg oder Misserfolg der Benutzeraktion an
- **[!UICONTROL Full Action Name]** - Zeigt den Namen der Backend-Aktion an
- **[!UICONTROL Details]** - Zeigt die Kategorie der Backend-Aktion an
- **[!UICONTROL Full Details]** - Zeigt alle protokollierten Details der Admin-Aktion an

## Anzeigen des Berichts zu Aktionsprotokollen

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL System]** > _[!UICONTROL Actions Logs]_>**[!UICONTROL Report]**.

   ![Aktionsprotokolle](./assets/action-log-report.png){width="600" zoomable="yes"}

1. Um die vollständigen Details einer aufgelisteten Admin-Aktion anzuzeigen, klicken Sie auf **[!UICONTROL View]**.

   ![Details zum Aktionsprotokolleintrag](./assets/action-log-report-view.png){width="600" zoomable="yes"}

## Filtern des Berichts zu Aktionsprotokollen

Sie können die Felder für die Filteroptionen definieren und dann auf **[!UICONTROL Search]** klicken, um die angezeigten Aktionen einzugrenzen.

Um die Filteroptionen zu löschen und zum vollständigen Bericht zurückzukehren, klicken Sie auf **[!UICONTROL Reset Filter]**.

![Filter für Aktionsprotokollberichte](./assets/action-log-report-filters.png){width="600" zoomable="yes"}

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Time] | Klicken Sie **[!UICONTROL From]** auf , um ein Datum aus dem dynamischen Kalender auszuwählen und so das Anfangsdatum für den Filter zu definieren. Klicken Sie in **[!UICONTROL To]** auf ein Datum, um das Enddatum für den Filter zu definieren. |
| [!UICONTROL Action Group] | Wählen Sie eine Aktionsgruppe aus. |
| [!UICONTROL Action] | Wählen Sie eine Aktion. |
| [!UICONTROL IP Address] | Geben Sie die IP-Adresse des Geräts ein, das für eine Aktion verwendet wird. |
| [!UICONTROL Username] | Wählen Sie einen Benutzernamen. Der Standardwert ist `All Users`. |
| [!UICONTROL Result] | Wählen Sie „Erfolg“ oder „Fehler“. |
| [!UICONTROL Full Action Name] | Geben Sie den Text ein, für den die Suche im Feld übereinstimmen soll. |
| [!UICONTROL Details] | Geben Sie den Text ein, für den die Suche im Feld übereinstimmen soll. |

{style="table-layout:auto"}

## Exportieren des Berichts „Aktionsprotokolle“

1. Wählen Sie **[!UICONTROL Export to]** ein Exportformat aus:

   - `CSV` : Eine kommagetrennte Wertedatei, die Textdaten enthält.
   - `Excel XML` - Ein XML-basiertes Tabellendatenformat

1. Klicken Sie auf **[!UICONTROL Export]**.

   Die generierte Datei wird automatisch in Ihrem vorgesehenen Ordner für Downloads gespeichert.

   ![Export von Aktionsprotokollberichten](./assets/action-log-report-export.png){width="200"}
