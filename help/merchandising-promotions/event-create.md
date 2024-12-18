---
title: Ereignisse erstellen und aktualisieren
description: Erfahren Sie, wie Sie ein mit einer Kategorie verknüpftes Ereignis aus Ihrem Katalog erstellen.
exl-id: 6c9f6a33-6785-4c3a-add6-dc2a6b16ed88
feature: Marketing Tools, Promotions/Events
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '572'
ht-degree: 0%

---

# Ereignisse erstellen und aktualisieren

{{ee-feature}}

Jedes Ereignis ist mit einer Kategorie aus Ihrem Katalog verknüpft und es kann jeweils nur ein Ereignis mit einer bestimmten Kategorie verknüpft werden. Um eine Liste bevorstehender Ereignisse in Ihrem Store anzuzeigen, müssen Sie auch ein Widget [Karussell für Katalogereignisse](../content-design/widget-event-carousel.md) einrichten.

![Ereignisliste](./assets/category-events.png){width="700" zoomable="yes"}

## Ereignis erstellen

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Events]**.

1. Klicken Sie oben rechts auf **[!UICONTROL Add Catalog Event]**.

1. Wählen Sie in der Kategoriestruktur die Kategorie aus, die Sie mit dem Ereignis verknüpfen möchten.

   Da jede Kategorie jeweils nur ein Ereignis haben kann, sind alle Kategorien, für die bereits ein Ereignis vorhanden ist, deaktiviert.

   ![Neues Ereignis - Kategoriestruktur](./assets/catalog-events-category-tree.png){width="500" zoomable="yes"}

1. Definieren Sie die **[!UICONTROL Catalog Event Information]**:

   ![Katalogereignis-Informationen](./assets/catalog-event-information.png){width="700" zoomable="yes"}

   - Wählen Sie für die **[!UICONTROL Start Date]** des Ereignisses im Kalender (![Kalendersymbol](../assets/icon-calendar.png) das Datum aus. Stellen Sie mit den Schiebereglern **[!UICONTROL Hour]** und **[!UICONTROL Minute]** den Zeitpunkt ein, zu dem das Ereignis beginnt.

   - Wählen Sie für die **[!UICONTROL End Date]** des Ereignisses im Kalender (![Kalendersymbol](../assets/icon-calendar.png) das Datum aus. Verwenden Sie die Regler **[!UICONTROL Hour]** und **[!UICONTROL Minute]** , um die Zeit festzulegen, zu der das Ereignis endet.

   - Um eine **[!UICONTROL Image]** für das Ereignis-Widget hochzuladen, klicken Sie auf **[!UICONTROL Choose File]** und wählen Sie die Bilddatei aus Ihrem Verzeichnis aus.

   - Geben Sie im Feld **[!UICONTROL Sort Order]** eine Zahl ein, um die Reihenfolge anzugeben, in der dieses Ereignis angezeigt wird, wenn es mit anderen Ereignissen aufgelistet wird.

   - Aktivieren Sie das Kontrollkästchen jedes Seitentyps, auf dem der Countdown-Ticker angezeigt werden soll.

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.

## Ereignisse aktualisieren

Ereignisse können entweder über die Seite Ereignisse oder über die Kategorie bearbeitet werden, die mit dem Ereignis verknüpft ist. Wenn einer Kategorie ein Ereignis zugeordnet ist, wird oben rechts eine Schaltfläche Ereignis bearbeiten angezeigt.

### Methode 1: Bearbeiten eines Ereignisses auf der Seite Ereignisse

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Events]**.

1. Suchen Sie das Ereignis in der Liste und öffnen Sie es im Bearbeitungsmodus.

1. Nehmen Sie die erforderlichen Änderungen am Ereignis vor.

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.

### Methode 2: Bearbeiten eines Ereignisses aus einer Kategorie

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Wählen Sie in der Kategoriestruktur auf der linken Seite die Kategorie aus, die mit dem Ereignis verknüpft ist.

1. Klicken Sie oben rechts auf **[!UICONTROL Edit Even]t**.

1. Nehmen Sie die erforderlichen Änderungen am Ereignis vor.

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.

## Ereignis löschen

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Events]**.

1. Suchen Sie das Ereignis in der Liste und öffnen Sie es im Bearbeitungsmodus.

1. Klicken Sie oben rechts auf **[!UICONTROL Delete]**.

1. Um die Aktion zu bestätigen, klicken Sie auf **[!UICONTROL OK]**.

## Feldbeschreibungen

| Feld | [Umfang](../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Category] | Global | Beim Erstellen eines Ereignisses wird dieses Feld mit der Kategoriestruktur verknüpft. Beim Bearbeiten eines Ereignisses wird eine Verknüpfung mit der Kategorieseite erstellt, die sich auf das Ereignis bezieht. |
| [!UICONTROL Start Date] | Global | Das Startdatum und die Startzeit des Ereignisses im `MMDDYYYY HH;MM`. Klicken Sie auf das Kalendersymbol, um das Datum auszuwählen. |
| [!DNL End Date] | Global | Das Enddatum und die Endzeit des Ereignisses `MMDDYYYY HH;MM` Format. Klicken Sie auf das Kalendersymbol, um das Datum auszuwählen. |
| [!UICONTROL Image] | Shop-Ansicht | Lädt ein Bild hoch, das im [Widget Katalogereignisse - Karussell“ angezeigt ](../content-design/widget-event-carousel.md). |
| [!UICONTROL Sort Order] | Global | Bestimmt die Reihenfolge, in der dieses Ereignis angezeigt wird, wenn es mit anderen Ereignissen aufgelistet wird. |
| [!UICONTROL Display Countdown Ticker On] | Global | Zeigt den Countdown-Ticker in der Kopfzeile jeder angegebenen Seite an. Optionen: `Category Page` / `Product Page` |
| [!UICONTROL Status] | Global | Gibt den Status des Ereignisses basierend auf dem Start- und Enddatumsbereich an. Status ist ein schreibgeschützter Wert. Werte: `Open` / `Closed` / `Upcoming` |

{style="table-layout:auto"}

## Schaltflächenleiste

| Schaltfläche | Beschreibung |
|--- |--- |
| **[!UICONTROL Back]** | Kehrt zur Seite Ereignisse zurück, ohne das neue Ereignis oder die Änderungen in einem vorhandenen Ereignis zu speichern. |
| **[!UICONTROL Delete]** | Löscht das Ereignis. |
| **[!UICONTROL Reset]** | Löscht das Formular von nicht gespeicherten Änderungen und stellt die ursprünglichen Ereignisinformationen wieder her. |
| **[!UICONTROL Save and Continue Edit]** | Speichert alle Änderungen und lässt das Formular im Bearbeitungsmodus geöffnet. |
| **[!UICONTROL Save]** | Speichert Änderungen, schließt das Formular und kehrt zur Seite Ereignisse zurück. |

{style="table-layout:auto"}
