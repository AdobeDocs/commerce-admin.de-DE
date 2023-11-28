---
title: Newsletter-Warteschlangen
description: Erfahren Sie, wie Sie Newsletter-Warteschlangen zum Senden mehrerer Newsletter-Batches verwalten.
exl-id: bf85b3ff-3093-49a1-8a9a-d3ea71fe3f09
feature: Customers, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 0%

---

# Newsletter-Warteschlangen

Um die Auslastung des Servers zu verwalten, werden Newsletter mit vielen Abonnenten in einer Warteschlange mit mehreren Batches gesendet. Sie können die Newsletter-Warteschlange regelmäßig überprüfen, um den Status zu überprüfen und zu sehen, wie viele verarbeitet wurden. Alle Probleme, die während der Übertragung auftreten, treten auf _Newsletter-Problem_ Bericht.

## Newsletter senden

1. Im _Admin_ Menü, navigieren Sie zu **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Newsletter Template]**.

1. Suchen Sie im Raster die [Newsletter-Vorlage](newsletter-template.md) , das gesendet werden soll, und legen Sie die **[!UICONTROL Action]** Spalte zu `Queue Newsletter`.

1. Für **[!UICONTROL Queue Date Start]** das Datum auswählen, an dem die Übertragung im Kalender beginnen soll (![Kalendersymbol](../assets/icon-calendar.png)).

1. Für **[!UICONTROL Subscribers From]** auswählen, wählen Sie jede Store-Ansicht aus, die in die E-Mail-Erweiterung aufgenommen werden soll.

1. Füllen Sie die E-Mail-Kopfzeileninformationen aus:

   - Geben Sie eine kurze Beschreibung des Newsletters für die **[!UICONTROL Subject]** Zeile des E-Mail-Headers.

   - Geben Sie die **[!UICONTROL Sender Name]**.

   - Für **[!UICONTROL Sender Email]**, geben Sie die E-Mail-Adresse des Absenders ein.

     Der Standardname und die E-Mail-Adresse des Absenders werden in der Konfiguration angegeben.

     ![Newsletter-Warteschlangeninformationen](./assets/newsletter-queue-information1.png){width="600" zoomable="yes"}

1. Falls zutreffend, geben Sie im **[!UICONTROL Message]** oberhalb der Abmeldeanweisungen.

   >[!NOTE]
   >
   >Entfernen Sie nicht die Anweisungen, die in vielen Rechtsordnungen gesetzlich vorgeschrieben sind.

1. Um benutzerdefinierte Stile auf einen Newsletter anzuwenden, fügen Sie sie zum **[!UICONTROL Newsletter Styles]** -Feld.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save and Resume]**.

   Der Newsletter wird in der Warteschlange angezeigt, die auf die Verarbeitung wartet.

## Auf Probleme prüfen

Im _Admin_ Menü, navigieren Sie zu **[!UICONTROL Reports]** > _[!UICONTROL Marketing]_>**[!UICONTROL Newsletter Problem Reports]**.

## Schaltflächenleiste

| Schaltfläche | Beschreibung |
|--- |--- |
| **[!UICONTROL Back]** | Kehrt zur Seite Newsletter-Vorlagen zurück, ohne Änderungen zu speichern. |
| **[!UICONTROL Reset]** | Setzt alle nicht gespeicherten Änderungen im Formular für Warteschlangeninformationen auf ihre vorherigen Werte zurück. |
| **[!UICONTROL Preview Template]** | Öffnet eine Vorschauseite auf einer separaten Registerkarte. |
| **[!UICONTROL Save and Resume]** | Speichert alle vorgenommenen Änderungen. Stellt den Newsletter in die Warteschlange. |
| **[!UICONTROL Save Newsletter]** | Speichert alle vorgenommenen Änderungen. Stellt den Newsletter in die Warteschlange. |

{style="table-layout:auto"}

## Spalten

| Spalte | Beschreibung |
|--- |--- |
| [!UICONTROL ID] | Eine eindeutige numerische Kennung, die jeder Newsletter-Vorlage zugewiesen wird. |
| [!UICONTROL Queue Start] | Das Datum, an dem der Newsletter versendet wurde. |
| [!UICONTROL Queue End] | Das Datum, an dem der Newsletter versendet wurde. |
| [!UICONTROL Subject] | Betreff der Newsletter-Vorlage. |
| [!UICONTROL Status] | Gibt den Status des Newsletter-Versands an. Mögliche Werte: `Sent`, `Canceled`, `Not Sent`, `Sending`oder `Paused`. |
| [!UICONTROL Processed] | Gibt an, wie viele Newsletter gesendet wurden. |
| [!UICONTROL Recipients] | Gibt an, wie viele Newsletter von Abonnenten empfangen wurden. |
| [!UICONTROL Actions] | **[!UICONTROL Preview]**: öffnet ein separates Fenster zur Vorschau der Vorlage. |

{style="table-layout:auto"}
