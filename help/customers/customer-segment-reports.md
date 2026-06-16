---
title: Bericht zu Kundensegmenten
description: Der Bericht „Kundensegment“ enthält Informationen zur Anzahl der Kunden in jedem Segment.
exl-id: a767ee80-7b6e-4acd-9772-2f8adcf3233e
TQID: https://experienceleague.adobe.com/asBYmrf5lkWyfH6xf8o-OxZwK25rr4okrtsyON3Fv1s
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 247
ht-degree: 0%

---

# Bericht zu Kundensegmenten

{{ee-feature}}

Der Bericht „Kundensegment“ enthält Informationen zur Anzahl der Kunden in jedem Segment.

![Kundensegmentbericht](assets/customer-segments-reports.png){width="700" zoomable="yes"}

| Spalte | Beschreibung |
|--- |--- |
| **[!UICONTROL Select]** | Aktivieren Sie das Kontrollkästchen für jedes Segment, das einer Aktion unterzogen werden soll, oder verwenden Sie die Auswahlsteuerung in der Spaltenüberschrift. Optionen: `Select All` / `Deselect All` / `Select Visible` / `Unselect Visible` |
| **[!UICONTROL ID]** | Eine eindeutige numerische Kennung, die jedem Segment zugewiesen ist |
| **[!UICONTROL Segment]** | Segmentname |
| **[!UICONTROL Status]** | Segmentstatus. Optionen: `Active` / `Inactive` |
| **[!UICONTROL Website]** | Website, der das Segment zugewiesen ist |
| **[!UICONTROL Customers]** | Anzahl der einem Segment zugewiesenen Kunden |

{style="table-layout:auto"}

Sie können einen Drilldown in eine Liste von Kunden im Segment durchführen und die Daten exportieren.

![Drilldown zu Kundendaten](assets/customer-segment-drilldown.png){width="600" zoomable="yes"}

Um sicherzustellen, dass Sie über die neuesten Daten verfügen, müssen die Segmentdaten aktualisiert werden. Wenn die Segmentdaten nicht verfügbar oder veraltet sind, klicken Sie zum Aktualisieren in der Schaltflächenleiste auf **[!UICONTROL Refresh Segment Data]** .

1. Wählen Sie **[!UICONTROL Export to]** ein Exportformat aus:

   * CSV - Eine kommagetrennte Wertedatei, die Textdaten enthält.
   * Excel XML - Ein XML-basiertes Tabellendatenformat.

1. Klicken Sie auf **[!UICONTROL Export]**.

   | Spalte | Beschreibung |
   |--- |--- |
   | **[!UICONTROL ID]** | Eine eindeutige numerische Kennung, die jedem Benutzer zugewiesen ist |
   | **[!UICONTROL Name]** | Kundenname |
   | **[!UICONTROL Email]** | Die E-Mail-Adresse eines registrierten Kunden |
   | **[!UICONTROL Group]** | Die Debitorengruppe, der der Debitor zugewiesen ist |
   | **[!UICONTROL Phone]** | Die Telefonnummer des Kunden |
   | **[!UICONTROL ZIP]** | Die Postleitzahl, an der sich der Kunde befindet |
   | **[!UICONTROL Country]** | Das Land, in dem sich der Kunde befindet |
   | **[!UICONTROL State/Province]** | Das Bundesland, in dem sich der Kunde befindet |
   | **[!UICONTROL Customer Since]** | Datum und Uhrzeit der Erstellung des Kundenkontos |

   {style="table-layout:auto"}

1. Die generierte Datei wird automatisch auf Ihrem lokalen Computer gespeichert.
