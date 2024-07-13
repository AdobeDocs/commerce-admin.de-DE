---
title: Kundensegmentbericht
description: Der Kundensegmentbericht enthält Informationen zur Anzahl der Kunden in den einzelnen Segmenten.
exl-id: a767ee80-7b6e-4acd-9772-2f8adcf3233e
source-git-commit: c855a691ed33e1e6e74865ebdfb30ddad21ad83e
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 0%

---

# Kundensegmentbericht

{{ee-feature}}

Der Bericht &quot;Kundensegment&quot;enthält Informationen zur Anzahl der Kunden in den einzelnen Segmenten.

![Bericht &quot;Kundensegment&quot;](assets/customer-segments-reports.png){width="700" zoomable="yes"}

| Spalte | Beschreibung |
|--- |--- |
| **[!UICONTROL Select]** | Aktivieren Sie das Kontrollkästchen für jedes Segment, das einer Aktion unterzogen werden soll, oder verwenden Sie das Auswahlsteuerelement in der Spaltenüberschrift. Optionen: `Select All` / `Deselect All` / `Select Visible` / `Unselect Visible` |
| **[!UICONTROL ID]** | Eine eindeutige numerische ID, die jedem Segment zugewiesen wird |
| **[!UICONTROL Segment]** | Segmentname |
| **[!UICONTROL Status]** | Segmentstatus. Optionen: `Active` / `Inactive` |
| **[!UICONTROL Website]** | Website, der das Segment zugewiesen wurde |
| **[!UICONTROL Customers]** | Anzahl der einem Segment zugewiesenen Kunden |

{style="table-layout:auto"}

Sie können einen Drilldown zu einer Liste von Kunden im Segment durchführen und die Daten exportieren.

![Drilldown zu Kundendaten](assets/customer-segment-drilldown.png){width="600" zoomable="yes"}

Damit Sie über die neuesten Daten verfügen, müssen die Segmentdaten aktualisiert werden. Wenn die Segmentdaten nicht verfügbar oder veraltet sind, klicken Sie in der Schaltflächenleiste auf **[!UICONTROL Refresh Segment Data]** , um sie zu aktualisieren.

1. Wählen Sie für **[!UICONTROL Export to]** ein Exportformat:

   * CSV - Eine kommagetrennte Wertdatei mit Textdaten.
   * Excel XML - Ein XML-basiertes Tabellendatenformat.

1. Klicken Sie auf **[!UICONTROL Export]**.

   | Spalte | Beschreibung |
   |--- |--- |
   | **[!UICONTROL ID]** | Eine eindeutige numerische Kennung, die jedem Benutzer zugewiesen ist |
   | **[!UICONTROL Name]** | Kundenname |
   | **[!UICONTROL Email]** | Die E-Mail-Adresse eines registrierten Kunden |
   | **[!UICONTROL Group]** | Die Kundengruppe, der der Kunde zugewiesen ist |
   | **[!UICONTROL Phone]** | Die Telefonnummer des Kunden |
   | **[!UICONTROL ZIP]** | Postleitzahl des Kunden |
   | **[!UICONTROL Country]** | Das Land, in dem sich der Kunde befindet |
   | **[!UICONTROL State/Province]** | Das Bundesland oder die Provinz, in dem sich der Kunde befindet |
   | **[!UICONTROL Customer Since]** | Datum und Uhrzeit der Erstellung des Kundenkontos |

   {style="table-layout:auto"}

1. Die generierte Datei wird automatisch auf Ihrem lokalen Computer gespeichert.
