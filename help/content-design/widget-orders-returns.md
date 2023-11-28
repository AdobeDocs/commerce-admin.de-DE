---
title: Widget "Bestellungen und Rückgaben"
description: Erfahren Sie, wie Sie das Widget für Bestellungen und Rückgaben verwenden können, um Kunden die Möglichkeit zu geben, den Status ihrer Bestellungen zu überprüfen, Rechnungen zu drucken und Sendungen zu verfolgen.
exl-id: 1c3948e6-a0de-4ee4-8abf-10ab845a94a7
feature: Page Content, Orders, Returns
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 0%

---

# Widget &quot;Bestellungen und Rückgaben&quot;

Die _Bestellungen und Rückgaben_ -Widget gibt den Gästen die Möglichkeit, den Status ihrer Bestellungen zu überprüfen, Rechnungen zu drucken und Sendungen zu verfolgen. Wenn das Widget zur Storefront hinzugefügt wird, ist es nur für Gäste und Kunden sichtbar, die nicht bei ihren Konten angemeldet sind. Sie können Bestellungen unter Angabe der Bestell-ID, des Nachnamens der Abrechnung sowie der E-Mail-Adresse oder Postleitzahl finden.

![Widget Bestellungen und Rückgaben in der Seitenleiste auf der Storefront](./assets/storefront-widget-orders-returns-sidebar.png){width="600" zoomable="yes"}

## Das Widget zum Bestellen und Zurückgeben auf der Storefront

1. Der Kunde kann die **[!UICONTROL Find Order By]** -Option, um einen der folgenden Parameter auszuwählen, die zum Auffinden der Bestellung verwendet werden sollen:

   - Email-Adresse
   - Postleitzahl

1. Der Kunde gibt die **[!UICONTROL Order ID]** und **[!UICONTROL Billing Last Name]**.

1. Fügt entweder die Rechnungsstellung ein **[!UICONTROL Email Address]** oder **[!UICONTROL ZIP Code]** , der mit der Bestellung verknüpft ist.

1. Klicks **[!UICONTROL Search]** , um die Bestellung abzurufen.

   ![In der Storefront angezeigte Bestellinformationen](./assets/storefront-widget-orders-returns-view.png){width="700" zoomable="yes"}

## Einrichten des Widgets Bestellungen und Rückgaben

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Klicken Sie oben rechts auf **[!UICONTROL Add Widget]**.

1. Im _[!UICONTROL Settings]_führen Sie folgende Schritte aus:

   - Satz **[!UICONTROL Type]** nach `Orders and Returns`.

   - Wählen Sie die **[!UICONTROL Design Theme]** wird vom Store verwendet.

1. Klicken **[!UICONTROL Continue]**.

1. Im _[!UICONTROL Storefront Properties]_führen Sie folgende Schritte aus:

   - Für **[!UICONTROL Widget Title]**, geben Sie einen beschreibenden Titel für das Widget ein.

     Dieser Titel ist nur vom Administrator sichtbar.

   - Für **[!UICONTROL Assign to Store Views]**, wählen Sie die Store-Ansichten aus, in denen das Widget sichtbar ist.

     Sie können eine bestimmte Store-Ansicht auswählen oder `All Store Views`. Um mehrere Ansichten auszuwählen, halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie auf jede Option.

   - (Optional) Für **[!UICONTROL Sort Order]** Geben Sie eine Zahl ein, um die Reihenfolge zu bestimmen, in der dieses Element mit anderen Elementen im selben Teil der Seite angezeigt wird. (`0` = first, `1` = Sekunde, `3` = drittes Element usw.)

1. Im _[!UICONTROL Layout Updates]_Abschnitt, klicken Sie auf **[!UICONTROL Add Layout Update]**und gehen Sie wie folgt vor:

   - Satz **[!UICONTROL Display On]** in den Seitentyp ein, auf dem das Widget angezeigt werden soll.

   - Um zu bestimmen, wo das Widget auf der Seite angezeigt wird, füllen Sie die restlichen Informationen zur Layout-Aktualisierung aus.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]**.

1. Wenn Sie aufgefordert werden, den Cache zu aktualisieren, klicken Sie auf den Link in der Meldung oben auf der Seite und befolgen Sie die Anweisungen.
