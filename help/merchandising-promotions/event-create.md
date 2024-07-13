---
title: Ereignisse erstellen und aktualisieren
description: Erfahren Sie, wie Sie aus Ihrem Katalog ein Ereignis erstellen, das mit einer Kategorie verknüpft ist.
exl-id: 6c9f6a33-6785-4c3a-add6-dc2a6b16ed88
feature: Marketing Tools, Promotions/Events
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '572'
ht-degree: 0%

---

# Ereignisse erstellen und aktualisieren

{{ee-feature}}

Jedes Ereignis ist mit einer Kategorie aus Ihrem Katalog verknüpft und es kann jeweils nur ein Ereignis mit einer bestimmten Kategorie verknüpft werden. Um eine Liste bevorstehender Ereignisse in Ihrem Store anzuzeigen, müssen Sie auch ein Widget [Katalogereignis-Karussell](../content-design/widget-event-carousel.md) einrichten.

![Ereignisliste](./assets/category-events.png){width="700" zoomable="yes"}

## Ereignis erstellen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Events]**.

1. Klicken Sie in der oberen rechten Ecke auf **[!UICONTROL Add Catalog Event]**.

1. Wählen Sie im Kategoriebaum die Kategorie aus, die Sie mit dem Ereignis verbinden möchten.

   Da jede Kategorie nur ein Ereignis gleichzeitig haben kann, werden alle Kategorien, die bereits über ein Ereignis verfügen, deaktiviert.

   ![Neues Ereignis - Kategoriestruktur](./assets/catalog-events-category-tree.png){width="500" zoomable="yes"}

1. Definieren Sie den **[!UICONTROL Catalog Event Information]**:

   ![Katalogereignisinformationen](./assets/catalog-event-information.png){width="700" zoomable="yes"}

   - Verwenden Sie für die **[!UICONTROL Start Date]** des Ereignisses den Kalender (![Kalendersymbol](../assets/icon-calendar.png)), um das Datum auszuwählen. Verwenden Sie die Regler **[!UICONTROL Hour]** und **[!UICONTROL Minute]**, um die Zeit festzulegen, zu der das Ereignis beginnt.

   - Verwenden Sie für die **[!UICONTROL End Date]** des Ereignisses den Kalender (![Kalendersymbol](../assets/icon-calendar.png)), um das Datum auszuwählen. Verwenden Sie die Regler **[!UICONTROL Hour]** und **[!UICONTROL Minute]**, um die Zeit festzulegen, zu der das Ereignis endet.

   - Um eine 0 für das Ereignis-Widget hochzuladen, klicken Sie auf **[!UICONTROL Choose File]** und wählen Sie die Bilddatei aus Ihrem Verzeichnis aus.**[!UICONTROL Image]**

   - Geben Sie im Feld **[!UICONTROL Sort Order]** eine Zahl ein, um die Sequenz anzugeben, in der dieses Ereignis bei der Auflistung mit anderen Ereignissen erscheint.

   - Aktivieren Sie das Kontrollkästchen jedes Seitentyps, in dem der Countdown-Ticker angezeigt werden soll.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]**.

## Ereignisse aktualisieren

Ereignisse können auf der Seite Ereignisse oder in der Kategorie bearbeitet werden, die dem Ereignis zugeordnet ist. Wenn einer Kategorie ein Ereignis zugeordnet ist, wird oben rechts die Schaltfläche Ereignis bearbeiten angezeigt.

### Methode 1: Bearbeiten eines Ereignisses auf der Seite &quot;Ereignisse&quot;

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Events]**.

1. Suchen Sie das Ereignis in der Liste und öffnen Sie es im Bearbeitungsmodus.

1. Nehmen Sie die erforderlichen Änderungen am Ereignis vor.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]**.

### Methode 2: Bearbeiten eines Ereignisses aus einer Kategorie

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Wählen Sie in der Kategorienstruktur auf der linken Seite die Kategorie aus, die mit dem Ereignis verknüpft ist.

1. Klicken Sie oben rechts auf **[!UICONTROL Edit Even]t**.

1. Nehmen Sie die erforderlichen Änderungen am Ereignis vor.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]**.

## Ereignis löschen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Events]**.

1. Suchen Sie das Ereignis in der Liste und öffnen Sie es im Bearbeitungsmodus.

1. Klicken Sie in der oberen rechten Ecke auf **[!UICONTROL Delete]**.

1. Um die Aktion zu bestätigen, klicken Sie auf **[!UICONTROL OK]**.

## Feldbeschreibungen

| Feld | [Umfang](../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Category] | Global | Beim Erstellen eines Ereignisses verknüpft dieses Feld mit dem Kategoriebaum zurück. Beim Bearbeiten eines Ereignisses wird eine Verknüpfung zu der Kategorieseite des Ereignisses hergestellt. |
| [!UICONTROL Start Date] | Global | Das Startdatum und die Startzeit des Ereignisses im Format `MMDDYYYY HH;MM`. Klicken Sie auf das Kalendersymbol, um das Datum auszuwählen. |
| [!DNL End Date] | Global | Das Enddatum und die Endzeit des Ereignisses im Format `MMDDYYYY HH;MM`. Klicken Sie auf das Kalendersymbol, um das Datum auszuwählen. |
| [!UICONTROL Image] | Store-Ansicht | Lädt ein Bild hoch, das im Widget [Katalogereignis-Karussell](../content-design/widget-event-carousel.md) angezeigt wird. |
| [!UICONTROL Sort Order] | Global | Bestimmt die Reihenfolge, in der dieses Ereignis angezeigt wird, wenn es mit anderen Ereignissen aufgelistet wird. |
| [!UICONTROL Display Countdown Ticker On] | Global | Zeigt den Countdown-Ticker in der Kopfzeile jeder angegebenen Seite an. Optionen: `Category Page` / `Product Page` |
| [!UICONTROL Status] | Global | Gibt den Status des Ereignisses basierend auf dem Startdatum und dem Enddatumsbereich an. Status ist ein schreibgeschützter Wert. Werte: `Open` / `Closed` / `Upcoming` |

{style="table-layout:auto"}

## Schaltflächenleiste

| Schaltfläche | Beschreibung |
|--- |--- |
| **[!UICONTROL Back]** | Kehrt zur Seite &quot;Ereignisse&quot;zurück, ohne das neue Ereignis oder Änderungen in einem vorhandenen Ereignis zu speichern. |
| **[!UICONTROL Delete]** | Löscht das Ereignis. |
| **[!UICONTROL Reset]** | Löscht das Formular nicht gespeicherter Änderungen und stellt die ursprünglichen Ereignisinformationen wieder her. |
| **[!UICONTROL Save and Continue Edit]** | Speichert alle Änderungen und öffnet das Formular im Bearbeitungsmodus. |
| **[!UICONTROL Save]** | Speichert Änderungen, schließt das Formular und kehrt zur Seite Ereignisse zurück. |

{style="table-layout:auto"}
