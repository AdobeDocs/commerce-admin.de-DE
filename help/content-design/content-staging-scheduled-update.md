---
title: Inhaltsaktualisierung planen
description: Sehen Sie sich dieses Kampagnenbeispiel an, mit dem eine temporäre Preisänderung für ein Produkt geplant wird.
exl-id: 36b7d7f6-4590-4192-a82b-e5f645b05f62
feature: Page Content, Staging
source-git-commit: b3897ba034770229ef8f3117231bed286abdddb9
workflow-type: tm+mt
source-wordcount: '636'
ht-degree: 0%

---

# Inhaltsaktualisierung planen

{{ee-feature}}

Das folgende Beispiel zeigt, wie eine temporäre Preisänderung für ein Produkt geplant wird. Dazu gehören die Planung und Vorschau von Änderungen sowie die Anzeige geplanter Aktualisierungen im Kalender. Obwohl dieses Beispiel nur eine einzige Änderung enthält, kann eine Kampagne mehrere Änderungen an Produkten, Preisregeln, CMS-Seiten und anderen Entitäten enthalten, die zur selben Zeit stattfinden sollen. Verwenden Sie eine ähnliche Methode, um die Von-/Bis-Daten für die [!UICONTROL Set Product As New] -Attribut.

>[!NOTE]
>Sie müssen eine geplante Aktualisierung erstellen, um ein Start- (und Enddatum) für [!UICONTROL Set Product As New]. Für [!UICONTROL Special Price] und [!UICONTROL Design Change], werden die Datumsfelder von/aus aus Adobe Commerce entfernt und stehen nur in Magento Open Source zur Verfügung.
>
>Alle geplanten Aktualisierungen werden nacheinander angewendet, d. h. jede Entität kann nur eine geplante Aktualisierung gleichzeitig haben. Jede geplante Aktualisierung wird auf alle Store-Ansichten innerhalb des Zeitrahmens angewendet. Daher kann eine Entität nicht gleichzeitig eine andere geplante Aktualisierung für verschiedene Store-Ansichten haben. Alle Entitätsattributwerte in allen Store-Ansichten, die von der aktuellen geplanten Aktualisierung nicht betroffen sind, werden von den Standardwerten übernommen und nicht von der vorherigen geplanten Aktualisierung.

## Eine Aktualisierung eines Produkts planen

1. Aus dem _[!UICONTROL Products]_ein Produkt im Bearbeitungsmodus öffnen.

1. Im _[!UICONTROL Scheduled Changes]_Klicken Sie oben auf der Seite auf **[!UICONTROL Schedule New Update]**.

   ![Neue Aktualisierung planen](./assets/content-staging-product-schedule-new-update.png){width="600" zoomable="yes"}

1. Mit dem **[!UICONTROL Save as a New Update]** ausgewählt ist, legen Sie die grundlegenden Parameter für die Aktualisierung fest:

   - Für **[!UICONTROL Update Name]** Geben Sie einen Namen für die neue Inhaltstaging-Kampagne ein.

   - Kurzbeschreibung eingeben **[!UICONTROL Description]** der Aktualisierung und ihrer Verwendung.

   - Verwenden Sie den Kalender (![Kalendersymbol](../assets/icon-calendar.png)), um das **Startdatum** und **Enddatum** für die Kampagne.

     Um eine Kampagne mit offenem Ende zu erstellen, geben Sie kein Enddatum an (leer lassen). In diesem Beispiel soll die Kampagne für das neue Jahr, den 1. Januar 2021 um 12:00 Uhr PST, um Mitternacht beginnen.


     Für eine Preisregel-Kampagne, die ohne Enddatum erstellt wurde, kann kein Enddatum zu einem späteren Zeitpunkt hinzugefügt werden. In diesem Fall ist es erforderlich, eine Kampagne zu erstellen und das Startdatum auf das Datum festzulegen, an dem die alte und die neue Kampagne enden sollen. Ab diesem Startdatum endet die alte Kampagne und die neue Kampagne beginnt wie definiert.

     ![Produktaktualisierung planen](./assets/content-staging-campaign-schedule-update.png){width="600" zoomable="yes"}

     >[!NOTE]
     >
     >Das Start- und Enddatum der Kampagne muss mithilfe der Variablen **_default_** Admin-Zeitzone, die aus der lokalen Zeitzone jeder Website konvertiert wird. Wenn Sie beispielsweise mehrere Websites in verschiedenen Zeitzonen haben, aber eine Kampagne mit einer US-Zeitzone (Standard) starten möchten, müssen Sie für jede lokale Zeitzone eine separate Aktualisierung planen. Legen Sie in diesem Fall **[!UICONTROL Start Date]** und **[!UICONTROL End Date]** aus jeder lokalen Website-Zeitzone in die standardmäßige Admin-Zeitzone konvertiert.

1. Nach unten scrollen zu _[!UICONTROL Price]_und klicken **[!UICONTROL Advanced Pricing]**.

1. Geben Sie einen **[!UICONTROL Special Price]** für das Produkt während der geplanten Kampagne und klicken Sie **[!UICONTROL Done]**.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]**.

   Die geplante Änderung wird oben auf der Produktseite mit dem Start- und Enddatum der Kampagne angezeigt.

   ![Geplante Änderung](./assets/content-staging-product-scheduled-update-preview-rope.png){width="600" zoomable="yes"}

## Geplante Änderung bearbeiten

1. Im _Geplante Änderungen_ Klicken Sie oben auf der Seite auf **[!UICONTROL View/Edit]**.

1. Nehmen Sie die erforderlichen Änderungen an der geplanten Aktualisierung vor.

1. Klicken **[!UICONTROL Save]**.

## Vorschau der geplanten Änderung

Im _Geplante Änderungen_ Klicken Sie oben auf der Seite auf **[!UICONTROL Preview]**.

Die Vorschau öffnet eine neue Browser-Registerkarte und zeigt an, wie das Produkt während der geplanten Kampagne erscheint.

>[!NOTE]
>
>Eine Staging-Vorschau für eine geplante Aktualisierung beginnt immer bei der **default** Store-Ansicht, die das Kundenerlebnis beim Navigieren durch die Staging-Update-Kampagne emuliert.

Weitere Informationen zur Verwendung der Werkzeuge für die Vorschau von Inhalten zum Ändern von Datum und Umfang der Vorschau finden Sie unter [Vorschau einer Kampagne](content-staging-preview.md). Sie können auch einen Link zur Store-Vorschau für Ihre Kollegen freigeben.
