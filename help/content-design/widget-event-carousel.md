---
title: Widget „Katalogereignisse - Karussell“
description: Erfahren Sie, wie Sie mit einem Karussell-Widget für Katalogereignisse einen Schieberegler für anstehende Ereignisse auf einer Seite anzeigen können.
exl-id: 4e88b253-f320-4c94-9996-94d7005effc6
feature: Page Content, Promotions/Events
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 0%

---

# Widget „Katalogereignisse - Karussell“

{{ee-feature}}

Ein Karussell-Widget für Katalogereignisse zeigt einen Schieberegler für anstehende Ereignisse mit einem Countdown-Ticker für jedes Ereignis an. Sie können die Seiten und den Bereich des Seiten-Layouts auswählen, in dem das Karussell angezeigt werden soll, und die Breite und Anzahl der gleichzeitig angezeigten Ereignisse steuern. Das Ergebnis hängt von Ihrem Design, der Position, an der es auf der Seite angezeigt werden soll, und den ausgewählten Optionen ab.

![Ereignis-Karussell in der linken Seitenleiste](./assets/storefront-event-carousel-sidebar-gear.png){width="700" zoomable="yes"}

## Schritt 1: Aktivieren des Katalog-Karussell-Widgets

Bevor Sie beginnen, befolgen Sie die [Anweisungen](../merchandising-promotions/event-configure.md), um das _Katalogereignis_-Widget so zu konfigurieren, dass es für die Storefront aktiviert ist.

![Konfiguration von Katalogereignissen](./assets/config-catalog-catalog-events-1.png){width="500" zoomable="yes"}

## Schritt 2: Widget erstellen

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Klicken Sie oben rechts auf **[!UICONTROL Add Widget]**.

1. Gehen Sie im Abschnitt _[!UICONTROL Settings]_&#x200B;wie folgt vor:

   - Legen Sie **[!UICONTROL Type]** auf `Catalog Events Carousel` fest.

   - Wählen Sie die **[!UICONTROL Design Theme]** aus, die vom Store verwendet wird.

1. Klicken Sie auf **[!UICONTROL Continue]**.

   ![Widget-Einstellungen für ein Ereigniskarussell](./assets/widget-event-carousel-settings.png){width="500" zoomable="yes"}

1. Gehen Sie im Abschnitt _[!UICONTROL Storefront Properties]_&#x200B;wie folgt vor:

   - Geben Sie **[!UICONTROL Widget Title]** einen beschreibenden Titel für das Widget ein.

     Dieser Titel ist nur in „Admin _sichtbar_.

   - Wählen Sie **[!UICONTROL Assign to Store Views]** die Store-Ansichten aus, in denen das Widget sichtbar sein soll.

     Sie können eine bestimmte Shop-Ansicht oder `All Store Views` auswählen. Halten Sie zum Auswählen mehrerer Ansichten die Strg-Taste (PC) bzw. die Befehlstaste (Mac) gedrückt und klicken Sie auf die einzelnen Optionen.

   - (Optional) Geben Sie **[!UICONTROL Sort Order]** eine Zahl ein, um die Reihenfolge zu bestimmen, in der dieses Element zusammen mit anderen im selben Teil der Seite angezeigt wird. (`0` = First, `1` = Second, `3` = Third usw.)

     ![Widget-Storefront-Eigenschaften](./assets/widget-event-carousel-storefront-properties.png){width="600" zoomable="yes"}

## Schritt 3: Speicherort auswählen

1. Klicken Sie _Abschnitt_ Layout-Updates“ auf **[!UICONTROL Add Layout Update]**.

1. Legen Sie **[!UICONTROL Display On]** auf `Specified Page` fest.

1. Legen Sie **[!UICONTROL Page]** auf `CMS Home Page` fest.

1. Legen Sie **[!UICONTROL Container]** eine der folgenden Einstellungen fest:

   - `Main Content Area`
   - `Sidebar Additional`
   - `Sidebar Main`

   >[!NOTE]
   >
   >Die Ergebnisse variieren je nach Design und Seiten-Layout. Sie müssen den _[!UICONTROL Catalog Events Carousel Default Template]_&#x200B;auch in der Kategoriekonfiguration angeben.

1. Wenn das Ereignis-Karussell an einem anderen Ort in der Storefront angezeigt werden soll, klicken Sie auf **[!UICONTROL Add Layout Update]** und wiederholen Sie diese Schritte für diesen Ort.

   ![Layout-Aktualisierungen](./assets/widget-event-carousel-layout-updates-catalog-category-sidebar.png){width="600" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Save and Continue Edit]**.

   Vorerst können Sie die Meldung ignorieren, um den Cache zu aktualisieren.

## Schritt 4: Konfigurieren der Optionen

1. Wählen Sie im linken Bedienfeld **[!UICONTROL Widget Options]** aus.

1. Geben Sie **[!UICONTROL Frame Size]** die Anzahl der Ereignisse ein, die Sie gleichzeitig im Schieberegler auflisten möchten.

   Um jeweils nur ein Ereignis anzuzeigen, geben Sie `1` ein.

1. Geben Sie **[!UICONTROL Scroll]** die Anzahl der Ereignisauflistungen ein, die pro Klick gescrollt werden sollen.

   Um zum nächsten Ereignis zu scrollen, geben Sie `1` ein.

1. Für eine benutzerdefinierte Breite geben Sie die Anzahl der Pixel für **[!UICONTROL Block Custom Width]** ein.

   Auf der folgenden Beispielseite wird die benutzerdefinierte Breite auf 250 Pixel festgelegt.

   ![Widget-Optionen für benutzerdefinierte Breite](./assets/widget-options-custom-width.png){width="400" zoomable="yes"}

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.

1. Wenn Sie aufgefordert werden, den Cache zu aktualisieren, klicken Sie auf den Link in der Nachricht oben auf der Seite und folgen Sie den Anweisungen.
