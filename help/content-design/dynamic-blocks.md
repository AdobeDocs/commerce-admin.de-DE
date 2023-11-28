---
title: Dynamische Blöcke
description: Verwenden Sie dynamische Bausteine, um umfangreiche, interaktive Inhalte zu erstellen, die von der Logik der Preisregeln und Kundensegmente angetrieben werden.
exl-id: 0c842ad9-2e46-48aa-9a12-2f74a54c352e
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 0%

---

# Dynamische Blöcke

{{ee-feature}}

Rich, interaktive Inhalte erstellen, die von der Logik abgeleitet wurden [Preisregeln](../merchandising-promotions/introduction.md#price-rules) und [Kundensegmente](../customers/customer-segments.md). Bestehend [dynamische Blöcke](../page-builder/dynamic-block.md) kann direkt zum [!DNL Page Builder] [Schritt](../page-builder/workspace.md). Ein detailliertes, schrittweises Beispiel für die Verwendung dynamischer Blöcke finden Sie unter [Tutorial 2: Blöcke](../page-builder/2-blocks.md).

>[!NOTE]
>
>Die _[!UICONTROL Banner]_in der [[!UICONTROL Content] Menü](content-menu.md) wurde in Version 2.3.1 nicht mehr unterstützt und in Version 2.4.0 entfernt. Seine Funktionalität wird durch dynamische Blöcke ersetzt.

![[!DNL Page Builder] - dynamischer Block mit Preisregel und Kundensegment](../page-builder/assets/pb-tutorial2-dynamic-block-storefront.png){width="600" zoomable="yes"}

## Schritt 1: Dynamischen Baustein erstellen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Dynamic Blocks]**.

   ![Liste der dynamischen Blöcke](../page-builder/assets/pb-tutorial2-block-dynamic-add.png){width="600" zoomable="yes"}

1. Klicken Sie oben rechts auf **[!UICONTROL Add Dynamic Block]**.

   ![Neuer dynamischer Block](../page-builder/assets/pb-tutorial2-block-dynamic-new.png){width="600" zoomable="yes"}

1. Falls zutreffend, legen Sie **[!UICONTROL Store View]** in eine bestimmte Store-Ansicht, in der der dynamische Block angezeigt werden soll.

1. Um den dynamischen Block zu aktivieren, legen Sie **[!UICONTROL Enable Dynamic Block]** nach `Yes`.

1. Geben Sie als interne Referenz eine Beschreibung ein **[!UICONTROL Dynamic Block Name]**.

1. Satz **[!UICONTROL Dynamic Block Type]** in den Bereich der Seite, in dem der dynamische Block angezeigt werden soll, und klicken Sie auf **[!UICONTROL Done]**.

   ![Festlegen des dynamischen Blocktyps](../page-builder/assets/pb-dynamic-block-type.png){width="500" zoomable="yes"}

1. Im **[!UICONTROL Customer Segment]** Liste, aktivieren Sie das Kontrollkästchen jedes Segments, das den dynamischen Block sehen soll, und klicken Sie auf **[!UICONTROL Done]** , um die Einstellung zu speichern.

   ![Auswählen eines Kundensegments](../page-builder/assets/pb-dynamic-block-customer-segment.png){width="500" zoomable="yes"}

   >[!NOTE]
   >
   >- Wenn kein Segment erstellt wird, ist der dynamische Block für alle sichtbar.
   >- Wenn der Kunde keinem Segment angehört und der dynamische Block für alle Segmente erstellt wird, wird der Inhalt des dynamischen Blocks weiterhin angezeigt.
   >- Wenn alle einem dynamischen Block zugewiesenen Kundensegmente gelöscht werden, sind die zugehörigen Inhalte für alle sichtbar.

### Verwenden von Real-Time CDP-Zielgruppen in dynamischen Bausteinen

Wenn Sie [installiert](../customers/audience-activation.md#install-the-extension) und [konfiguriert](../customers/audience-activation.md#configure-the-extension) die [!DNL Audience Activation] -Erweiterung sehen Sie einen Abschnitt namens **[!UICONTROL Audiences]**.

![Real-Time CDP-Zielgruppe auswählen](./assets/dynamic-block-rtcdp.png){width="600" zoomable="yes"}

Im **[!UICONTROL Real-Time CDP Audience]** Liste, aktivieren Sie das Kontrollkästchen der einzelnen Zielgruppen, die den dynamischen Block sehen sollen, und klicken Sie auf **[!UICONTROL Done]** , um die Einstellung zu speichern.

## Schritt 2: Inhalt abschließen

Verwenden Sie die [!DNL Page Builder] [Arbeitsbereich](../page-builder/workspace.md) , um den Inhalt abzuschließen.

![[!DNL Page Builder] - Arbeitsbereich für dynamische Bausteine](../page-builder/assets/pb-dynamic-block-workspace.png){width="600" zoomable="yes"}

## Schritt 3: Auswählen einer zugehörigen Promotion

1. Hinunter scrollen und erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) **[!UICONTROL Related Promotions]**.

1. Klicken Sie auf den Promotion-Typ, den Sie mit dem dynamischen Baustein verbinden möchten:

   - **[!UICONTROL Add Cart Price Rules]** (siehe [Warenkorbpreisregeln](../merchandising-promotions/price-rules-cart.md))

   - **[!UICONTROL Add Catalog Price Rules]** (siehe [Katalogpreisregeln](../merchandising-promotions/price-rules-catalog.md))

   >[!NOTE]
   >
   >Katalogpreisregeln werden für Real-Time CDP-Zielgruppen nicht unterstützt.

1. Aktivieren Sie in der Liste der verfügbaren Regeln das Kontrollkästchen der einzelnen Regeln, die Sie verwenden möchten, und klicken Sie auf **[!UICONTROL Add Selected]**.

1. Wenn der dynamische Block abgeschlossen ist, klicken Sie auf **[!UICONTROL Save]**.

## Schritt 4: Dynamischen Baustein zu einer Seite hinzufügen

1. Öffnen Sie die Seite, auf der der dynamische Baustein angezeigt werden soll.

1. Verwenden Sie die [[!UICONTROL Add Dynamic Block]](../page-builder/dynamic-block.md) Inhaltstyp , um den dynamischen Baustein zur Bühne hinzuzufügen.

## Beschreibung von Feldern und Tools

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Store View] | Gibt die Store-Ansichten an, in denen der dynamische Block verfügbar sein soll. |
| [!UICONTROL Enable Dynamic Block] | Aktiviert oder deaktiviert den dynamischen Block. Optionen: Ja/Nein |
| [!UICONTROL Dynamic Block Name] | Ein beschreibender Name, der den dynamischen Baustein in der Admin-Konsole identifiziert. |
| [!UICONTROL Dynamic Block Type] | Identifiziert den Ort im [Standardseitenlayout](layout-updates.md) wo der dynamische Block platziert wird. Optionen: <br/>**[!UICONTROL Content Area]**- Platziert den dynamischen Baustein in der [Inhaltsbereich](layout-updates.md) der Seite.<br/>**[!UICONTROL Footer]** - Platziert den dynamischen Baustein auf der Seite [Fußzeile](page-setup.md#footer). <br/>**[!UICONTROL Header]**- Platziert den dynamischen Baustein auf der Seite [header](page-setup.md#header).<br/>**[!UICONTROL Left Column]** - Platziert den dynamischen Block im [linke Seitenleiste](page-layout.md#standard-page-layouts) eines zweispaltigen oder dreispaltigen Layouts. <br/>**[!UICONTROL Right Column]**- Platziert den dynamischen Block im [rechte Seitenleiste](page-layout.md#standard-page-layouts) aus einem zweispaltigen oder dreispaltigen Layout. |
| Kundensegment | Verbindet ein Kundensegment mit dem dynamischen Block, um zu bestimmen, welche Kunden es sehen können. |
| Real-Time CDP Audience | Verbindet eine [Real-Time CDP-Audience](../customers/audience-activation.md) mit dem dynamischen Block, um zu bestimmen, welche Kunden ihn sehen können. |

{style="table-layout:auto"}

### Inhalt

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Layout] | Fügen Sie der Bühne Zeilen, Spalten oder Registerkarten hinzu. |
| [!UICONTROL Elements] | Fügen Sie jedem Layout-Container auf der Bühne Text, Überschriften, Schaltflächen, Divider und HTML-Code hinzu. |
| [!UICONTROL Media] | Fügen Sie jedem vorhandenen Layout-Container auf der Bühne Bilder, Videos, Banner, Regler und Google Maps hinzu. |
| [!UICONTROL Add Content] | Fügen Sie der Bühne vorhandene Bausteine, dynamische Bausteine und Produkte hinzu. |

{style="table-layout:auto"}

### Verwandte Promotions

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Related Cart Price Rule] | **[!UICONTROL Add Cart Price Rules]** - Vorhandene verknüpfen [Warenkorbpreisregel](../merchandising-promotions/price-rules-cart.md) mit dem dynamischen Baustein als Promotion. |
| [!UICONTROL Related Catalog Price Rule] | **[!UICONTROL Add Catalog Price Rules]** - Vorhandene verknüpfen [Katalogpreisregel](../merchandising-promotions/price-rules-catalog.md) mit dem dynamischen Baustein als Promotion. |

{style="table-layout:auto"}
