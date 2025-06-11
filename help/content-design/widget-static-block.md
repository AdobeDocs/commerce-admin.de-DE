---
title: Verwenden eines Widgets zum Positionieren eines Blocks
description: Erfahren Sie, wie Sie mit einem statischen Block-Widget einen vorhandenen Inhalt nahezu überall in Ihrem Store platzieren können.
exl-id: 174deef2-33c4-4f1a-8ca8-4969be209bc7
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '586'
ht-degree: 0%

---

# Verwenden eines Widgets zum Positionieren eines Blocks

Mit dem _statischen CMS_ Block[Widget](widgets.md) können Sie einen vorhandenen [Inhaltsblock](blocks.md) nahezu überall in Ihrem Store platzieren.

![Widgets](./assets/widgets.png){width="700" zoomable="yes"}

## Schritt 1: Wählen Sie den Widget-Typ

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Klicken Sie oben rechts auf **[!UICONTROL Add Widget]**.

1. Legen _im Abschnitt_ Einstellungen“ **[!UICONTROL Type]** auf `CMS Static Block` fest und klicken Sie auf **[!UICONTROL Continue]**.

1. Stellen Sie sicher, dass die **[!UICONTROL Design Theme]** auf das aktuelle Design eingestellt ist, und klicken Sie auf **[!UICONTROL Continue]**.

   ![Widget-Einstellungen](./assets/widget-settings.png){width="600" zoomable="yes"}

1. Gehen Sie im Abschnitt _[!UICONTROL Storefront Properties]_&#x200B;wie folgt vor:

   - Geben Sie **[!UICONTROL Widget Title]** einen beschreibenden Titel für das Widget ein.

     Dieser Titel ist nur in „Admin _sichtbar_.

   - Wählen Sie **[!UICONTROL Assign to Store Views]** die Store-Ansichten aus, in denen das Widget sichtbar ist.

     Sie können eine bestimmte Shop-Ansicht oder `All Store Views` auswählen. Halten Sie zum Auswählen mehrerer Ansichten die Strg-Taste (PC) bzw. die Befehlstaste (Mac) gedrückt und klicken Sie auf die einzelnen Optionen.

   - (Optional) Geben Sie **[!UICONTROL Sort Order]** eine Zahl ein, um die Reihenfolge zu bestimmen, in der dieses Element zusammen mit anderen im selben Teil der Seite angezeigt wird. (`0` = First, `1` = Second, `3` = Third usw.)

     ![Storefront-Eigenschaften](./assets/widget-storefront-properties.png){width="600" zoomable="yes"}

## Schritt 2: Abschließen der Widget-Layout-Aktualisierungen

1. Klicken Sie im Abschnitt _[!UICONTROL Layout Updates]_&#x200B;auf **[!UICONTROL Add Layout Update]**.

1. Legen Sie **[!UICONTROL Display On]** auf die Kategorie, das Produkt oder die Seite fest, auf der der Block angezeigt werden soll.

1. Gehen Sie wie folgt vor, um den Block auf einer bestimmten Seite zu platzieren:

   - Wählen Sie die **[!UICONTROL Page]**, in der der Block angezeigt werden soll.

   - Wählen Sie die **[!UICONTROL Block Reference]**, die die Stelle angibt, an der der Block auf der Seite angezeigt wird.

   - Akzeptieren Sie die Standardeinstellung für **[!UICONTROL Template]**, die auf `CMS Static Block Default Template` festgelegt ist.

     ![Layout-Aktualisierungen](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

### Optionen zur Layout-Aktualisierung

| Feld | Beschreibung |
|--- |--- |
| **_[!UICONTROL Categories]_** |  |
| [!UICONTROL Anchor Categories] | Zeigt das Widget auf der Ankerkategorieseite an.<br/>**[!UICONTROL Categories]**- Kategorien, in denen der Anker angezeigt wird. Optionen: `All`/`Specific Categories`<br/>**[!UICONTROL Container]** - Den Container auf den Teil des Seiten-Layouts festlegen, in dem Sie das Widget anzeigen möchten.<br/>**[!UICONTROL Template]**- Bestimmt das Design des Layouts. |
| [!UICONTROL Non-Anchor Categories] | Zeigt das Widget auf der Kategorieseite ohne Anker an.<br/>**[!UICONTROL Categories]**- Kategorien, in denen der Anker angezeigt wird. Optionen: `All`/`Specific Categories`<br/>**[!UICONTROL Container]** - Den Container auf den Teil des Seiten-Layouts festlegen, in dem Sie das Widget anzeigen möchten.<br/>**[!UICONTROL Template]**- Bestimmt das Design des Layouts. |
| **_[!UICONTROL Products]_** |  |
| Alle Produktarten | Zeigt das Widget entweder auf einer bestimmten Produktseite oder auf allen Produktseiten an. <br/>**[!UICONTROL Products]**- Produkte, für die das Widget angezeigt wird. Optionen: `All`/` Specific Products`<br/>**[!UICONTROL Container]** - Legen Sie den Container auf den Teil des Seiten-Layouts fest, in dem Sie das Widget anzeigen möchten.<br/>**[!UICONTROL Template]**- Bestimmt das Design des Layouts. |
| **_[!UICONTROL Generic Pages]_** |  |
| [!UICONTROL All Pages] | Zeigt das Widget auf allen Seiten an. <br/>**[!UICONTROL Container]**: Legen Sie den Container auf den Teil des Seiten-Layouts fest, in dem Sie das Widget anzeigen möchten.<br/>**[!UICONTROL Template]** - Bestimmt das Design des Layouts. |
| [!UICONTROL Specified Page] | Zeigt das Widget auf einer bestimmten Seite an. Optionen: <br/>**[!UICONTROL Page]**- Seiten, für die das Widget angezeigt wird.<br/>**[!UICONTROL Container]** : Legen Sie den Container auf den Teil des Seiten-Layouts fest, in dem Sie das Widget anzeigen möchten.<br/>**Vorlage** - Bestimmt das Design des Layouts. |
| [!UICONTROL Page Layouts] | Zeigt das Widget auf Seiten mit einem bestimmten Layout an. <br/>**[!UICONTROL Page]**- Seiten, für die das Widget angezeigt wird.<br/>**[!UICONTROL Container]** : Legen Sie den Container auf den Teil des Seiten-Layouts fest, in dem Sie das Widget anzeigen möchten.<br/>**[!UICONTROL Template]**- Bestimmt das Design des Layouts. |

{style="table-layout:auto"}

## Schritt 3: Platzieren des Blocks

1. Wählen Sie im linken Bedienfeld **[!UICONTROL Widget Options]** aus.

1. Klicken Sie auf **[!UICONTROL Select Block…]** und wählen Sie den Block aus der Liste aus, den Sie platzieren möchten.

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.

   Die App wird jetzt in der Liste angezeigt.

1. Befolgen Sie bei Aufforderung die Anweisungen oben auf der Seite, um den Index und den Seiten-Cache zu aktualisieren.

1. Kehren Sie zu Ihrer Storefront zurück, um zu überprüfen, ob der Block an der richtigen Stelle angezeigt wird.

   Um den Block zu verschieben, können Sie das Widget erneut öffnen oder eine andere Seite oder Blockreferenz ausprobieren.
