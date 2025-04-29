---
title: Planen einer Inhaltsaktualisierung
description: Sehen Sie sich dieses Kampagnenbeispiel an, das verwendet wird, um eine temporäre Preisänderung für ein Produkt zu planen.
exl-id: 36b7d7f6-4590-4192-a82b-e5f645b05f62
feature: Page Content, Staging
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
source-git-commit: 07d7ca7e7f6af42fe8e06dc3c49c2df5f50d1425
workflow-type: tm+mt
source-wordcount: '653'
ht-degree: 0%

---

# Planen einer Inhaltsaktualisierung

{{ee-feature}}

Das folgende Beispiel zeigt, wie Sie eine temporäre Preisänderung für ein Produkt planen. Dazu gehören die Planung und Vorschau von Änderungen und die Anzeige geplanter Aktualisierungen im Kalender. Obwohl dieses Beispiel nur eine einzige Änderung enthält, kann eine Kampagne mehrere Änderungen an Produkten, Preisregeln, CMS-Seiten und anderen Entitäten enthalten, die zur gleichen Zeit geplant sind. Verwenden Sie eine ähnliche Methode, um das Von-/Bis-Datum für das [!UICONTROL Set Product As New] anzugeben.

>[!NOTE]
>Sie müssen ein geplantes Update erstellen, um ein Start- (und Enddatum) für [!UICONTROL Set Product As New] anzugeben. Für [!UICONTROL Special Price] und [!UICONTROL Design Change] werden die Felder „Von“/„Bis“ aus Adobe Commerce entfernt und sind nur in Magento Open Source verfügbar.
>
>Alle geplanten Aktualisierungen werden nacheinander angewendet, d. h., jede Entität kann nur jeweils eine geplante Aktualisierung haben. Jede geplante Aktualisierung wird auf alle Store-Ansichten innerhalb ihres Zeitrahmens angewendet. Daher kann eine Entität nicht gleichzeitig verschiedene geplante Aktualisierungen für verschiedene Store-Ansichten haben. Alle Entitätsattributwerte in allen Store-Ansichten, die nicht von der aktuellen geplanten Aktualisierung betroffen sind, werden aus den Standardwerten übernommen, nicht aus der vorherigen geplanten Aktualisierung.

## Planen einer Produktaktualisierung

1. Öffnen Sie im _[!UICONTROL Products]_ein Produkt im Bearbeitungsmodus.

1. Klicken Sie im _[!UICONTROL Scheduled Changes]_oben auf der Seite auf **[!UICONTROL Schedule New Update]**.

   ![Neues Update planen](./assets/content-staging-product-schedule-new-update.png){width="600" zoomable="yes"}

1. Legen Sie bei ausgewählter Option **[!UICONTROL Save as a New Update]** die grundlegenden Parameter für die Aktualisierung fest:

   - Geben Sie **[!UICONTROL Update Name]** einen Namen für die neue Inhalts-Staging-Kampagne ein.

   - Geben Sie eine kurze **[!UICONTROL Description]** der Aktualisierung und ihrer Verwendung ein.

   - Verwenden Sie das Tool Kalender ![Kalendersymbol](../assets/icon-calendar.png), um das **Startdatum** und **Enddatum** für die Kampagne auszuwählen.

     Um eine Kampagne mit offenem Ende zu erstellen, geben Sie kein Enddatum an (leer lassen). Für dieses Beispiel soll die Kampagne am 1. Januar 2021 um Mitternacht um 12:00 Uhr (PST) beginnen.


     Für eine Preisregelkampagne, die ohne Enddatum erstellt wurde, kann kein Enddatum später hinzugefügt werden. In diesem Fall müssen Sie eine Kampagne erstellen und das Startdatum auf das Datum setzen, an dem die alte Kampagne enden soll, sowie auf das Startdatum der neuen Kampagne. An diesem Startdatum endet die alte Kampagne, und die neue Kampagne beginnt wie definiert.

     ![Planen einer Produktaktualisierung](./assets/content-staging-campaign-schedule-update.png){width="600" zoomable="yes"}

     >[!NOTE]
     >
     >Start- und Enddatum der Kampagne müssen mithilfe der Admin-Zeitzone **_Standard_** definiert werden, die aus der lokalen Zeitzone jeder Website konvertiert wird. Wenn Sie beispielsweise mehrere Websites in verschiedenen Zeitzonen haben, aber eine Kampagne auf der Grundlage einer US-amerikanischen (Standard) Zeitzone starten möchten, müssen Sie für jede lokale Zeitzone ein separates Update planen. Legen Sie in diesem Fall **[!UICONTROL Start Date]** und **[!UICONTROL End Date]** als von jeder lokalen Website-Zeitzone in die standardmäßige Admin-Zeitzone konvertiert fest.

1. Scrollen Sie nach unten zu _[!UICONTROL Price]_und klicken Sie auf **[!UICONTROL Advanced Pricing]**.

1. Geben Sie während der geplanten Kampagne einen **[!UICONTROL Special Price]** für das Produkt ein und klicken Sie auf **[!UICONTROL Done]**.

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.

   Die geplante Änderung wird oben auf der Produktseite mit dem Start- und Enddatum der Kampagne angezeigt.

   ![Geplante Änderung](./assets/content-staging-product-scheduled-update-preview-rope.png){width="600" zoomable="yes"}

## Geplante Änderung bearbeiten

1. Klicken Sie _Feld „Geplante_&quot; oben auf der Seite auf **[!UICONTROL View/Edit]**.

1. Nehmen Sie die erforderlichen Änderungen an der geplanten Aktualisierung vor.

1. Klicken Sie auf **[!UICONTROL Save]**.

## Vorschau der geplanten Änderung

Klicken Sie _Feld „Geplante_&quot; oben auf der Seite auf **[!UICONTROL Preview]**.

Die Vorschau öffnet eine neue Browser-Registerkarte und zeigt an, wie das Produkt während der geplanten Kampagne angezeigt wird.

>[!NOTE]
>
>Eine Staging-Vorschau für ein geplantes Update beginnt immer in der **Standard** Store-Ansicht, die das Kundenerlebnis beim Navigieren durch die Staging-Update-Kampagne emuliert.

Weitere Informationen zur Verwendung der Tools für die Inhaltsvorschau zum Ändern des Datums und des Umfangs der Vorschau finden Sie unter [Vorschau einer Kampagne](content-staging-preview.md). Sie können auch einen Link zur Store-Vorschau für Ihre Kollegen freigeben.
