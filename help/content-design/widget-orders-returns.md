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

Das Widget _Bestellungen und Rückgaben_ gibt Gästen die Möglichkeit, den Status ihrer Bestellungen zu überprüfen, Rechnungen zu drucken und Sendungen zu verfolgen. Wenn das Widget zur Storefront hinzugefügt wird, ist es nur für Gäste und Kunden sichtbar, die nicht bei ihren Konten angemeldet sind. Sie können Bestellungen unter Angabe der Bestell-ID, des Nachnamens der Abrechnung sowie der E-Mail-Adresse oder Postleitzahl finden.

![Bestellungen und Gibt das Widget in der Seitenleiste auf der Storefront zurück](./assets/storefront-widget-orders-returns-sidebar.png){width="600" zoomable="yes"}

## Das Widget zum Bestellen und Zurückgeben auf der Storefront

1. Der Kunde kann die Option **[!UICONTROL Find Order By]** verwenden, um einen der folgenden Parameter zum Suchen der Bestellung auszuwählen:

   - Email-Adresse
   - Postleitzahl

1. Der Kunde gibt **[!UICONTROL Order ID]** und **[!UICONTROL Billing Last Name]** ein.

1. Fügt entweder die Abrechnung **[!UICONTROL Email Address]** oder **[!UICONTROL ZIP Code]** ein, die der Bestellung zugeordnet ist.

1. Klicken Sie auf **[!UICONTROL Search]** , um die Bestellung abzurufen.

   ![In der Storefront angezeigte Bestellinformationen](./assets/storefront-widget-orders-returns-view.png){width="700" zoomable="yes"}

## Einrichten des Widgets Bestellungen und Rückgaben

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Klicken Sie in der oberen rechten Ecke auf **[!UICONTROL Add Widget]**.

1. Gehen Sie im Abschnitt _[!UICONTROL Settings]_wie folgt vor:

   - Setzen Sie **[!UICONTROL Type]** auf `Orders and Returns`.

   - Wählen Sie die **[!UICONTROL Design Theme]** aus, die vom Store verwendet wird.

1. Klicken Sie auf **[!UICONTROL Continue]**.

1. Gehen Sie im Abschnitt _[!UICONTROL Storefront Properties]_wie folgt vor:

   - Geben Sie für **[!UICONTROL Widget Title]** einen beschreibenden Titel für das Widget ein.

     Dieser Titel ist nur vom Administrator sichtbar.

   - Wählen Sie für &quot;**[!UICONTROL Assign to Store Views]**&quot;die Store-Ansichten aus, in denen das Widget sichtbar ist.

     Sie können eine bestimmte Store-Ansicht oder `All Store Views` auswählen. Um mehrere Ansichten auszuwählen, halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie auf jede Option.

   - (Optional) Geben Sie für &quot;**[!UICONTROL Sort Order]**&quot;eine Zahl ein, um die Reihenfolge zu bestimmen, in der dieses Element mit anderen im selben Teil der Seite angezeigt wird. (`0` = first, `1` = second, `3` = third usw.)

1. Klicken Sie im Abschnitt _[!UICONTROL Layout Updates]_auf **[!UICONTROL Add Layout Update]**und führen Sie die folgenden Schritte aus:

   - Setzen Sie **[!UICONTROL Display On]** auf den Seitentyp, auf dem das Widget angezeigt werden soll.

   - Um zu bestimmen, wo das Widget auf der Seite angezeigt wird, füllen Sie die restlichen Informationen zur Layout-Aktualisierung aus.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]**.

1. Wenn Sie aufgefordert werden, den Cache zu aktualisieren, klicken Sie auf den Link in der Meldung oben auf der Seite und befolgen Sie die Anweisungen.
