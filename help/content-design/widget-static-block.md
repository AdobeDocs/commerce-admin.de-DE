---
title: Verwenden eines Widgets zum Positionieren eines Blocks
description: Erfahren Sie, wie Sie mit einem statischen Block-Widget vorhandenen Inhalt nahezu an einer beliebigen Stelle in Ihrem Store platzieren können.
exl-id: 174deef2-33c4-4f1a-8ca8-4969be209bc7
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 0%

---

# Verwenden eines Widgets zum Positionieren eines Blocks

Das Widget _CMS Static Block_ [widget](widgets.md) bietet Ihnen die Möglichkeit, einen vorhandenen [Inhaltsbaustein](blocks.md) fast an beliebiger Stelle in Ihrem Store zu platzieren.

![Widgets](./assets/widgets.png){width="700" zoomable="yes"}

## Schritt 1: Widget-Typ auswählen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Klicken Sie in der oberen rechten Ecke auf **[!UICONTROL Add Widget]**.

1. Setzen Sie im Abschnitt _Einstellungen_ **[!UICONTROL Type]** auf `CMS Static Block` und klicken Sie auf **[!UICONTROL Continue]**.

1. Stellen Sie sicher, dass der **[!UICONTROL Design Theme]** auf das aktuelle Design eingestellt ist, und klicken Sie auf **[!UICONTROL Continue]**.

   ![Widget-Einstellungen](./assets/widget-settings.png){width="600" zoomable="yes"}

1. Gehen Sie im Abschnitt _[!UICONTROL Storefront Properties]_wie folgt vor:

   - Geben Sie für **[!UICONTROL Widget Title]** einen beschreibenden Titel für das Widget ein.

     Dieser Titel ist nur in _Admin_ sichtbar.

   - Wählen Sie für &quot;**[!UICONTROL Assign to Store Views]**&quot;die Store-Ansichten aus, in denen das Widget sichtbar ist.

     Sie können eine bestimmte Store-Ansicht oder `All Store Views` auswählen. Um mehrere Ansichten auszuwählen, halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie auf jede Option.

   - (Optional) Geben Sie für &quot;**[!UICONTROL Sort Order]**&quot;eine Zahl ein, um die Reihenfolge zu bestimmen, in der dieses Element mit anderen im selben Teil der Seite angezeigt wird. (`0` = first, `1` = second, `3` = third usw.)

     ![Storefront-Eigenschaften](./assets/widget-storefront-properties.png){width="600" zoomable="yes"}

## Schritt 2: Durchführen der Aktualisierungen des Widget-Layouts

1. Klicken Sie im Abschnitt _[!UICONTROL Layout Updates]_auf **[!UICONTROL Add Layout Update]**.

1. Setzen Sie **[!UICONTROL Display On]** auf die Kategorie, das Produkt oder die Seite, auf der der Block erscheinen soll.

1. Gehen Sie wie folgt vor, um den Baustein auf einer bestimmten Seite zu platzieren:

   - Wählen Sie die **[!UICONTROL Page]** aus, in der der Block erscheinen soll.

   - Wählen Sie die **[!UICONTROL Block Reference]** aus, die den Ort angibt, an dem der Block auf der Seite angezeigt wird.

   - Akzeptieren Sie die Standardeinstellung für **[!UICONTROL Template]**, die auf `CMS Static Block Default Template` festgelegt ist.

     ![Layout-Updates](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

### Optionen für Layoutaktualisierungen

| Feld | Beschreibung |
|--- |--- |
| **_[!UICONTROL Categories]_** |  |
| [!UICONTROL Anchor Categories] | Zeigt das Widget auf der Seite der Ankerkategorie an.<br/>**[!UICONTROL Categories]**- Kategorien, in denen der Anker angezeigt wird. Optionen: `All` /`Specific Categories`<br/>**[!UICONTROL Container]** - Setzen Sie den Container auf den Teil des Seitenlayouts, in dem das Widget angezeigt werden soll.<br/>**[!UICONTROL Template]**- Bestimmt das Design des Layouts. |
| [!UICONTROL Non-Anchor Categories] | Zeigt das Widget auf der Seite ohne Ankerkategorie an.<br/>**[!UICONTROL Categories]**- Kategorien, in denen der Anker angezeigt wird. Optionen: `All` /`Specific Categories`<br/>**[!UICONTROL Container]** - Setzen Sie den Container auf den Teil des Seitenlayouts, in dem das Widget angezeigt werden soll.<br/>**[!UICONTROL Template]**- Bestimmt das Design des Layouts. |
| **_[!UICONTROL Products]_** |  |
| Alle Produkttypen | Zeigt das Widget auf einer bestimmten Produktseite oder auf allen Produktseiten an. <br/>**[!UICONTROL Products]**- Produkte, für die das Widget angezeigt wird. Optionen: `All` /` Specific Products`<br/>**[!UICONTROL Container]** - Setzen Sie den Container auf den Teil des Seitenlayouts, in dem das Widget angezeigt werden soll.<br/>**[!UICONTROL Template]**- Bestimmt das Design des Layouts. |
| **_[!UICONTROL Generic Pages]_** |  |
| [!UICONTROL All Pages] | Zeigt das Widget auf allen Seiten an. <br/>**[!UICONTROL Container]**- Setzen Sie den Container auf den Teil des Seitenlayouts, in dem Sie das Widget anzeigen möchten.<br/>**[!UICONTROL Template]** - Bestimmt das Design des Layouts. |
| [!UICONTROL Specified Page] | Zeigt das Widget auf einer bestimmten Seite an. Optionen:<br/>**[!UICONTROL Page]**- Seiten, für die das Widget angezeigt wird.<br/>**[!UICONTROL Container]** - Setzen Sie den Container auf den Teil des Seitenlayouts, in dem Sie das Widget anzeigen möchten.<br/>**Vorlage** - Bestimmt das Design des Layouts. |
| [!UICONTROL Page Layouts] | Zeigt das Widget auf Seiten mit einem bestimmten Layout an. <br/>**[!UICONTROL Page]**- Seiten, für die das Widget angezeigt wird.<br/>**[!UICONTROL Container]** - Setzen Sie den Container auf den Teil des Seitenlayouts, in dem Sie das Widget anzeigen möchten.<br/>**[!UICONTROL Template]**- Bestimmt das Design des Layouts. |

{style="table-layout:auto"}

## 3. Schritt: Block platzieren

1. Wählen Sie im linken Bereich **[!UICONTROL Widget Options]** aus.

1. Klicken Sie auf **[!UICONTROL Select Block…]** und wählen Sie den Block aus, den Sie in der Liste platzieren möchten.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]**.

   Die App wird jetzt in der Liste angezeigt.

1. Befolgen Sie bei Aufforderung die Anweisungen oben auf der Seite, um den Index und den Seiten-Cache zu aktualisieren.

1. Kehren Sie zu Ihrer Storefront zurück, um sicherzustellen, dass der Block an der richtigen Stelle angezeigt wird.

   Um den Block zu verschieben, können Sie das Widget erneut öffnen oder eine andere Seite oder einen anderen Blockverweis ausprobieren.
