---
title: Karussell-Widget "Katalogereignisse"
description: Erfahren Sie, wie Sie mit einem Karussell-Widget für Katalogereignisse einen Regler bevorstehender Ereignisse auf einer Seite anzeigen können.
exl-id: 4e88b253-f320-4c94-9996-94d7005effc6
feature: Page Content, Promotions/Events
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 0%

---

# Karussell-Widget &quot;Katalogereignisse&quot;

{{ee-feature}}

Ein Karussell-Widget für Katalogereignisse zeigt einen Regler bevorstehender Ereignisse mit einem Countdown-Ticker für jedes Ereignis an. Sie können die Seiten und den Bereich des Seitenlayouts auswählen, in dem das Karussell angezeigt werden soll, und die Breite und Anzahl der gleichzeitig angezeigten Ereignisse steuern. Das Ergebnis hängt von Ihrem Design ab, wo es zur Anzeige auf der Seite positioniert ist, sowie von den von Ihnen gewählten Optionen.

![Ereignis-Karussell in der linken Seitenleiste](./assets/storefront-event-carousel-sidebar-gear.png){width="700" zoomable="yes"}

## Schritt 1: Aktivieren des Widgets &quot;Katalog-Karussell&quot;

Bevor Sie beginnen, befolgen Sie die [Anweisungen](../merchandising-promotions/event-configure.md) , um das Widget _Catalog Event_ so zu konfigurieren, dass es für die Storefront aktiviert ist.

![Katalogereigniskonfiguration](./assets/config-catalog-catalog-events-1.png){width="500" zoomable="yes"}

## Schritt 2: Widget erstellen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Klicken Sie in der oberen rechten Ecke auf **[!UICONTROL Add Widget]**.

1. Gehen Sie im Abschnitt _[!UICONTROL Settings]_wie folgt vor:

   - Setzen Sie **[!UICONTROL Type]** auf `Catalog Events Carousel`.

   - Wählen Sie die **[!UICONTROL Design Theme]** aus, die vom Store verwendet wird.

1. Klicken Sie auf **[!UICONTROL Continue]**.

   ![Widget-Einstellungen für ein Ereignis-Karussell](./assets/widget-event-carousel-settings.png){width="500" zoomable="yes"}

1. Gehen Sie im Abschnitt _[!UICONTROL Storefront Properties]_wie folgt vor:

   - Geben Sie für **[!UICONTROL Widget Title]** einen beschreibenden Titel für das Widget ein.

     Dieser Titel ist nur in _Admin_ sichtbar.

   - Wählen Sie für &quot;**[!UICONTROL Assign to Store Views]**&quot;die Store-Ansichten aus, in denen das Widget sichtbar sein soll.

     Sie können eine bestimmte Store-Ansicht oder `All Store Views` auswählen. Um mehrere Ansichten auszuwählen, halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie auf jede Option.

   - (Optional) Geben Sie für &quot;**[!UICONTROL Sort Order]**&quot;eine Zahl ein, um die Reihenfolge zu bestimmen, in der dieses Element mit anderen im selben Teil der Seite angezeigt wird. (`0` = first, `1` = second, `3` = third usw.)

     ![Eigenschaften der Widget-Storefront](./assets/widget-event-carousel-storefront-properties.png){width="600" zoomable="yes"}

## 3. Schritt: Speicherort auswählen

1. Klicken Sie im Abschnitt _Layout-Aktualisierungen_ auf **[!UICONTROL Add Layout Update]**.

1. Setzen Sie **[!UICONTROL Display On]** auf `Specified Page`.

1. Setzen Sie **[!UICONTROL Page]** auf `CMS Home Page`.

1. Legen Sie **[!UICONTROL Container]** für eine der folgenden Optionen fest:

   - `Main Content Area`
   - `Sidebar Additional`
   - `Sidebar Main`

   >[!NOTE]
   >
   >Die Ergebnisse variieren je nach Thema und Seitenlayout. Sie müssen auch die _[!UICONTROL Catalog Events Carousel Default Template]_in der Kategoriekonfiguration angeben.

1. Wenn Sie möchten, dass das Ereigniskarussell an einer anderen Stelle in der Storefront angezeigt wird, klicken Sie auf **[!UICONTROL Add Layout Update]** und wiederholen Sie diese Schritte für diesen Ort.

   ![Layout-Updates](./assets/widget-event-carousel-layout-updates-catalog-category-sidebar.png){width="600" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Save and Continue Edit]**.

   Derzeit können Sie die Meldung ignorieren, dass der Cache aktualisiert werden soll.

## Schritt 4: Optionen konfigurieren

1. Wählen Sie im linken Bereich **[!UICONTROL Widget Options]** aus.

1. Geben Sie für &quot;**[!UICONTROL Frame Size]**&quot;die Anzahl der Ereignisse, die Sie auflisten möchten, gleichzeitig im Regler ein.

   Um jeweils nur ein Ereignis anzuzeigen, geben Sie `1` ein.

1. Geben Sie für &quot;**[!UICONTROL Scroll]**&quot;die Anzahl der Ereignislisten ein, die pro Klick gescrollt werden sollen.

   Um zum nächsten Ereignis zu wechseln, geben Sie `1` ein.

1. Geben Sie für eine benutzerdefinierte Breite die Anzahl der Pixel für **[!UICONTROL Block Custom Width]** ein.

   Auf der folgenden Beispielseite wird die benutzerdefinierte Breite auf 250 Pixel festgelegt.

   ![Widget-Optionen für benutzerdefinierte Breite](./assets/widget-options-custom-width.png){width="400" zoomable="yes"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]**.

1. Wenn Sie aufgefordert werden, den Cache zu aktualisieren, klicken Sie auf den Link in der Meldung oben auf der Seite und befolgen Sie die Anweisungen.
