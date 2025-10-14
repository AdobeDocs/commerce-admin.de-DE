---
title: Dynamische Blöcke
description: Verwenden Sie dynamische Blöcke, um umfangreiche, interaktive Inhalte zu erstellen, die von der Logik der Preisregeln und Kundensegmente gesteuert werden.
exl-id: 0c842ad9-2e46-48aa-9a12-2f74a54c352e
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/de/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 0%

---

# Dynamische Blöcke

{{ee-feature}}

Erstellen Sie ansprechende, interaktive Inhalte, die von Logiken aus [Preisregeln](../merchandising-promotions/introduction.md#price-rules) und [Kundensegmenten](../customers/customer-segments.md) gesteuert werden. Vorhandene [dynamische Blöcke](../page-builder/dynamic-block.md) können direkt zur [!DNL Page Builder] ([) &#x200B;](../page-builder/workspace.md) werden. Ein detailliertes Beispiel der Verwendung dynamischer Blöcke finden Sie unter [Tutorial 2: Blöcke](../page-builder/2-blocks.md).

>[!NOTE]
>
>Die Option _[!UICONTROL Banner]_&#x200B;im Menü [[!UICONTROL Content] wurde &#x200B;](content-menu.md) 2.3.1 veraltet und in 2.4.0 entfernt. Seine Funktionalität wird durch dynamische Blöcke ersetzt.

![[!DNL Page Builder] - Dynamischer Block mit Preisregel und Kundensegment](../page-builder/assets/pb-tutorial2-dynamic-block-storefront.png){width="600" zoomable="yes"}

## Schritt 1: Dynamischen Block erstellen

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Dynamic Blocks]**.

   ![Liste der dynamischen Blöcke](../page-builder/assets/pb-tutorial2-block-dynamic-add.png){width="600" zoomable="yes"}

1. Klicken Sie oben rechts auf **[!UICONTROL Add Dynamic Block]**.

   ![Neuer dynamischer Block](../page-builder/assets/pb-tutorial2-block-dynamic-new.png){width="600" zoomable="yes"}

1. Legen Sie gegebenenfalls **[!UICONTROL Store View]** auf eine bestimmte Store-Ansicht fest, in der der dynamische Block angezeigt werden soll.

1. Um den dynamischen Block zu aktivieren, setzen Sie **[!UICONTROL Enable Dynamic Block]** auf `Yes`.

1. Geben Sie als interne Referenz einen beschreibenden **[!UICONTROL Dynamic Block Name]** ein.

1. Legen Sie **[!UICONTROL Dynamic Block Type]** auf den Bereich der Seite fest, auf dem der dynamische Block angezeigt werden soll, und klicken Sie auf **[!UICONTROL Done]**.

   ![Festlegen des dynamischen Blocktyps](../page-builder/assets/pb-dynamic-block-type.png){width="500" zoomable="yes"}

1. Aktivieren Sie in der **[!UICONTROL Customer Segment]** das Kontrollkästchen jedes Segments, für das Sie den dynamischen Block anzeigen möchten, und klicken Sie auf **[!UICONTROL Done]** , um die Einstellung zu speichern.

   ![Auswählen eines Kundensegments](../page-builder/assets/pb-dynamic-block-customer-segment.png){width="500" zoomable="yes"}

   >[!NOTE]
   >
   >- Wenn kein Segment erstellt wird, ist der dynamische Block für alle sichtbar.
   >- Wenn der Kunde zu keinem Segment gehört und der dynamische Block für alle Segmente erstellt wird, wird der Inhalt des dynamischen Blocks weiterhin angezeigt.
   >- Wenn alle einem dynamischen Block zugewiesenen Kundensegmente gelöscht werden, sind die Inhalte für alle sichtbar.

### Verwenden von Real-Time CDP-Zielgruppen in dynamischen Blöcken

Wenn Sie [&#x200B; [!DNL Audience Activation] Erweiterung installiert](../customers/audience-activation.md#install-the-extension) und [konfiguriert](../customers/audience-activation.md#configure-the-extension) wird ein Abschnitt namens **[!UICONTROL Audiences]** angezeigt.

![Real-Time CDP-Zielgruppe auswählen](./assets/dynamic-block-rtcdp.png){width="600" zoomable="yes"}

Aktivieren Sie in der Liste **[!UICONTROL Real-Time CDP Audience]** das Kontrollkästchen jeder Zielgruppe, für die der dynamische Block angezeigt werden soll, und klicken Sie auf **[!UICONTROL Done]** , um die Einstellung zu speichern.

## Schritt 2: Inhalt abschließen

Verwenden Sie den [!DNL Page Builder] [Arbeitsbereich](../page-builder/workspace.md), um den Inhalt abzuschließen.

![[!DNL Page Builder] - Arbeitsbereich für dynamische Blöcke](../page-builder/assets/pb-dynamic-block-workspace.png){width="600" zoomable="yes"}

## Schritt 3: Wählen Sie eine zugehörige Promotion

1. Scrollen Sie nach unten und erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) **[!UICONTROL Related Promotions]**.

1. Klicken Sie auf den Typ der Promotion, die Sie mit dem dynamischen Block verknüpfen möchten:

   - **[!UICONTROL Add Cart Price Rules]** (siehe [Warenkorb-Preisregeln](../merchandising-promotions/price-rules-cart.md))

   - **[!UICONTROL Add Catalog Price Rules]** (siehe [Katalogpreisregeln](../merchandising-promotions/price-rules-catalog.md))

   >[!NOTE]
   >
   >Katalogpreisregeln werden für Real-Time CDP-Zielgruppen nicht unterstützt.

1. Aktivieren Sie in der Liste der verfügbaren Regeln das Kontrollkästchen jeder Regel, die Sie verwenden möchten, und klicken Sie auf **[!UICONTROL Add Selected]**.

1. Wenn der dynamische Block abgeschlossen ist, klicken Sie auf **[!UICONTROL Save]**.

## Schritt 4: Dynamischen Block zu einer Seite hinzufügen

1. Öffnen Sie die Seite, auf der der dynamische Block angezeigt werden soll.

1. Verwenden Sie den Content-Typ [[!UICONTROL Add Dynamic Block]](../page-builder/dynamic-block.md) , um den dynamischen Block zum Schritt hinzuzufügen.

## Beschreibung der Felder und Werkzeuge

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Store View] | Gibt die Store-Ansichten an, in denen der dynamische Block verfügbar sein soll. |
| [!UICONTROL Enable Dynamic Block] | Aktiviert oder deaktiviert den dynamischen Block. Optionen: Ja / Nein |
| [!UICONTROL Dynamic Block Name] | Ein beschreibender Name, der den dynamischen Block in der Admin-Liste identifiziert. |
| [!UICONTROL Dynamic Block Type] | Gibt die Position im [Standardseitenlayout](layout-updates.md) an, an der der dynamische Block platziert ist. Optionen: <br/>**[!UICONTROL Content Area]**- Platziert den dynamischen Block im [&#x200B; (](layout-updates.md)) der Seite.<br/>**[!UICONTROL Footer]** - Platziert den dynamischen Block in der Seite [Fußzeile](page-setup.md#footer). <br/>**[!UICONTROL Header]**- Platziert den dynamischen Block in der [&#x200B; (](page-setup.md#header)).<br/>**[!UICONTROL Left Column]** - Platziert den dynamischen Block in der [linken &#x200B;](page-layout.md#standard-page-layouts) eines zwei- oder dreispaltigen Layouts. <br/>**[!UICONTROL Right Column]**- Platziert den dynamischen Block in der [rechten Seitenleiste](page-layout.md#standard-page-layouts) eines zweispaltigen oder dreispaltigen Layouts. |
| Kundensegment | Ordnet dem dynamischen Block ein Kundensegment zu, um zu bestimmen, welche Kunden es sehen können. |
| Real-Time CDP-Zielgruppe | Verknüpft eine [Real-Time CDP-Zielgruppe](../customers/audience-activation.md) mit dem dynamischen Block, um zu bestimmen, welche Kunden ihn sehen können. |

{style="table-layout:auto"}

### Inhalt

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Layout] | Fügen Sie dem Schritt Zeilen, Spalten oder Registerkarten hinzu. |
| [!UICONTROL Elements] | Fügen Sie Text, Überschriften, Schaltflächen, Trennlinien und HTML-Code zu einem beliebigen Layout-Container auf der Bühne hinzu. |
| [!UICONTROL Media] | Fügen Sie Bilder, Videos, Banner, Schieberegler und Google Maps zu einem beliebigen Layout-Container auf der Bühne hinzu. |
| [!UICONTROL Add Content] | Fügen Sie vorhandene Blöcke, dynamische Blöcke und Produkte zum Staging hinzu. |

{style="table-layout:auto"}

### Verwandte Promotions

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Related Cart Price Rule] | **[!UICONTROL Add Cart Price Rules]** - Verknüpfen Sie eine vorhandene [Warenkorb-Preisregel](../merchandising-promotions/price-rules-cart.md) mit dem dynamischen Block als Promotion. |
| [!UICONTROL Related Catalog Price Rule] | **[!UICONTROL Add Catalog Price Rules]** - Verknüpfen Sie eine vorhandene [Katalogpreisregel) &#x200B;](../merchandising-promotions/price-rules-catalog.md) dynamischen Block als Promotion. |

{style="table-layout:auto"}
