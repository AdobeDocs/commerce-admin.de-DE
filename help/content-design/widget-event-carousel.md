---
title: Karussell-Widget "Katalogereignisse"
description: Erfahren Sie, wie Sie mit einem Karussell-Widget für Katalogereignisse einen Regler bevorstehender Ereignisse auf einer Seite anzeigen können.
exl-id: 4e88b253-f320-4c94-9996-94d7005effc6
feature: Page Content, Promotions/Events
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 0%

---

# Karussell-Widget &quot;Katalogereignisse&quot;

{{ee-feature}}

Ein Karussell-Widget für Katalogereignisse zeigt einen Regler bevorstehender Ereignisse mit einem Countdown-Ticker für jedes Ereignis an. Sie können die Seiten und den Bereich des Seitenlayouts auswählen, in dem das Karussell angezeigt werden soll, und die Breite und Anzahl der gleichzeitig angezeigten Ereignisse steuern. Das Ergebnis hängt von Ihrem Design ab, wo es zur Anzeige auf der Seite positioniert ist, sowie von den von Ihnen gewählten Optionen.

![Ereigniskarussell in der linken Seitenleiste](./assets/storefront-event-carousel-sidebar-gear.png){width="700" zoomable="yes"}

## Schritt 1: Aktivieren des Widgets &quot;Katalog-Karussell&quot;

Bevor Sie beginnen, folgen Sie dem [instructions](../merchandising-promotions/event-configure.md) , um die _Katalogereignis_ -Widget, damit es für die Storefront aktiviert ist.

![Katalogereigniskonfiguration](./assets/config-catalog-catalog-events-1.png){width="500" zoomable="yes"}

## Schritt 2: Widget erstellen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Klicken Sie oben rechts auf **[!UICONTROL Add Widget]**.

1. Im _[!UICONTROL Settings]_führen Sie folgende Schritte aus:

   - Satz **[!UICONTROL Type]** nach `Catalog Events Carousel`.

   - Wählen Sie die **[!UICONTROL Design Theme]** wird vom Store verwendet.

1. Klicken **[!UICONTROL Continue]**.

   ![Widget-Einstellungen für ein Ereignis-Karussell](./assets/widget-event-carousel-settings.png){width="500" zoomable="yes"}

1. Im _[!UICONTROL Storefront Properties]_führen Sie folgende Schritte aus:

   - Für **[!UICONTROL Widget Title]**, geben Sie einen beschreibenden Titel für das Widget ein.

     Dieser Titel ist nur im _Admin_.

   - Für **[!UICONTROL Assign to Store Views]**, wählen Sie die Store-Ansichten aus, in denen das Widget sichtbar sein soll.

     Sie können eine bestimmte Store-Ansicht auswählen oder `All Store Views`. Um mehrere Ansichten auszuwählen, halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie auf jede Option.

   - (Optional) Für **[!UICONTROL Sort Order]** Geben Sie eine Zahl ein, um die Reihenfolge zu bestimmen, in der dieses Element mit anderen Elementen im selben Teil der Seite angezeigt wird. (`0` = first, `1` = Sekunde, `3` = drittes Element usw.)

     ![Eigenschaften der Widget-Storefront](./assets/widget-event-carousel-storefront-properties.png){width="600" zoomable="yes"}

## 3. Schritt: Speicherort auswählen

1. Im _Layout-Updates_ Abschnitt, klicken Sie auf **[!UICONTROL Add Layout Update]**.

1. Satz **[!UICONTROL Display On]** nach `Specified Page`.

1. Satz **[!UICONTROL Page]** nach `CMS Home Page`.

1. Satz **[!UICONTROL Container]** eine der folgenden Optionen:

   - `Main Content Area`
   - `Sidebar Additional`
   - `Sidebar Main`

   >[!NOTE]
   >
   >Die Ergebnisse variieren je nach Thema und Seitenlayout. Sie müssen auch die _[!UICONTROL Catalog Events Carousel Default Template]_in der Kategoriekonfiguration.

1. Wenn das Ereigniskarussell an einer anderen Stelle im Storefront angezeigt werden soll, klicken Sie auf **[!UICONTROL Add Layout Update]** und wiederholen Sie diese Schritte für diesen Ort.

   ![Layout-Aktualisierungen](./assets/widget-event-carousel-layout-updates-catalog-category-sidebar.png){width="600" zoomable="yes"}

1. Klicken **[!UICONTROL Save and Continue Edit]**.

   Derzeit können Sie die Meldung ignorieren, dass der Cache aktualisiert werden soll.

## Schritt 4: Optionen konfigurieren

1. Wählen Sie im linken Bereich die Option **[!UICONTROL Widget Options]**.

1. Für **[!UICONTROL Frame Size]** Geben Sie die Anzahl der Ereignisse, die Sie auflisten möchten, gleichzeitig im Regler ein.

   Um jeweils nur ein Ereignis anzuzeigen, geben Sie `1`.

1. Für **[!UICONTROL Scroll]** Geben Sie die Anzahl der Ereignislisten ein, die pro Klick gescrollt werden sollen.

   Um zum nächsten Ereignis zu wechseln, geben Sie `1`.

1. Geben Sie für eine benutzerdefinierte Breite die Anzahl Pixel für **[!UICONTROL Block Custom Width]**.

   Auf der folgenden Beispielseite wird die benutzerdefinierte Breite auf 250 Pixel festgelegt.

   ![Widget-Optionen für benutzerdefinierte Breite](./assets/widget-options-custom-width.png){width="400" zoomable="yes"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]**.

1. Wenn Sie aufgefordert werden, den Cache zu aktualisieren, klicken Sie auf den Link in der Meldung oben auf der Seite und befolgen Sie die Anweisungen.
