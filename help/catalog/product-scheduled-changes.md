---
title: Geplante Produktaktualisierungen
description: Erfahren Sie, wie Sie Änderungen an Ihren Produktlisten planen, um Kampagnen und Werbeprogramme zu unterstützen.
exl-id: ce1aebe6-9032-438d-b950-4b13116b8ed3
feature: Catalog Management, Products
source-git-commit: 3d04e7213d90bb4c323acce69ac31c1dbcb7ca49
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 0%

---

# Produktaktualisierungen planen

{{ee-feature}}

Produktaktualisierungen können planmäßig angewendet und mit anderen Inhaltsänderungen gruppiert werden. Sie können [Content-Staging](../content-design/content-staging.md) , um eine Kampagne auf der Grundlage geplanter Änderungen am Produkt zu erstellen oder die Änderungen auf eine bestehende Kampagne anzuwenden.

>[!NOTE]
>
>Die [!UICONTROL Set Product as New From] und [!UICONTROL To] Felder und [!UICONTROL Schedule Design Update] -Registerkarte wurden entfernt in ![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce und können nicht direkt am Produkt geändert werden. Sie müssen eine geplante Aktualisierung für diese Aktivierungen erstellen.

>[!NOTE]
>
>Alle geplanten Aktualisierungen werden nacheinander angewendet, d. h. jede Entität kann nur eine geplante Aktualisierung gleichzeitig haben. Jede geplante Aktualisierung wird auf alle Store-Ansichten innerhalb des Zeitrahmens angewendet. Daher kann eine Entität nicht mehrere geplante Aktualisierungen für verschiedene Store-Ansichten gleichzeitig aufweisen. Alle Entitätsattributwerte in allen Store-Ansichten, die von der aktuellen geplanten Aktualisierung nicht betroffen sind, werden von den Standardwerten übernommen und nicht von der vorherigen geplanten Aktualisierung.

>[!NOTE]
>
>Eine Staging-Vorschau für eine geplante Aktualisierung beginnt immer bei der **default** Store-Ansicht, die das Kundenerlebnis beim Navigieren durch die Staging-Update-Kampagne emuliert.

## Geplantes Update erstellen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Wählen Sie ein vorhandenes Produkt aus und klicken Sie auf **[!UICONTROL Edit]**.

1. Klicks **[!UICONTROL Schedule New Update]**.

1. Auswählen **[!UICONTROL Save as a New Update]**.

1. Für **[!UICONTROL Update Name]** Geben Sie einen Namen für die neue Inhaltstaging-Kampagne ein.

1. Kurzbeschreibung eingeben **[!UICONTROL Description]** der Aktualisierung und ihrer Verwendung.

1. Verwenden Sie den Kalender (![Kalendersymbol](../assets/icon-calendar.png)), um das **[!UICONTROL Start Date]** und **[!UICONTROL End Date]** für die Kampagne.

   >[!NOTE]
   >
   >Kampagne **[!UICONTROL Start Date]** und **[!UICONTROL End Date]** muss mithilfe der **_default_** Admin-Zeitzone, die aus der lokalen Zeitzone für jede Website konvertiert wird. Bei mehreren Websites in verschiedenen Zeitzonen, auf denen Sie eine Kampagne basierend auf einer US-Zeitzone starten möchten, müssen Sie beispielsweise für jede lokale Zeitzone eine separate Aktualisierung planen. Satz **[!UICONTROL Start Date]** und **[!UICONTROL End Date]** und wird aus der Zeitzone der lokalen Website in die standardmäßige Zeitzone des Administrators konvertiert.

   ![Als neue Aktualisierung planen](./assets/product-schedule-as-new.png){width="600" zoomable="yes"}

1. Nach unten scrollen zu _[!UICONTROL Price]_und klicken **[!UICONTROL Advanced Pricing]**.

1. Geben Sie einen **[!UICONTROL Special Price]** für das Produkt während der geplanten Kampagne und klicken Sie **[!UICONTROL Done]**.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]**.

## Zu vorhandener Aktualisierung zuweisen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Wählen Sie ein vorhandenes Produkt aus und klicken Sie auf **[!UICONTROL Edit]**.

1. Klicks **[!UICONTROL Schedule New Update]**.

1. Auswählen **[!UICONTROL Assign to Existing Campaign]**.

1. Wählen Sie in der Liste die zu ändernde Kampagne aus.

   ![Einer vorhandenen Kampagne zuweisen](./assets/scheduled-changes-assign-to-existing-campaign.png){width="600" zoomable="yes"}

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) **[!UICONTROL Content]**.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]**.

## Geplante Änderung anzeigen

Die geplante Änderung wird oben auf der Produktseite mit dem Start- und Enddatum der Kampagne angezeigt.

![Geplante Änderung](./assets/view-product-scheduled-changes.png){width="600" zoomable="yes"}

## Geplante Änderung bearbeiten

1. Im _[!UICONTROL Scheduled Changes]_Klicken Sie oben auf der Seite auf **[!UICONTROL View/Edit]**.

1. Nehmen Sie die erforderlichen Änderungen an der geplanten Aktualisierung vor.

1. Klicks **[!UICONTROL Save]**.

## Die geplante Änderung entfernen

1. Im _[!UICONTROL Scheduled Changes]_Klicken Sie oben auf der Seite auf **[!UICONTROL View/Edit]**.

1. Klicken Sie in der oberen Leiste auf **[!UICONTROL Remove from Update]**.

   ![Geplante Änderung entfernen](./assets/remove-product-scheduled-changes.png){width="600" zoomable="yes"}

1. Wählen Sie im Dialogfeld **[!UICONTROL Delete the Update]** und klicken **[!UICONTROL Done]**.

   >[!NOTE]
   >
   >Das Produkt wird aus der Aktualisierung entfernt und alle geplanten Änderungen gehen verloren.

## Planen einer Design-Aktualisierung

{{ce-feature}}

Die _[!UICONTROL Schedule Design Update]_gibt Ihnen die Möglichkeit, temporäre Änderungen am Erscheinungsbild der Produktseite vorzunehmen. Sie können Designänderungen für eine Saison, eine Promotion oder einfach nur planen, um Dinge neu zu gestalten. Designänderungen können im Voraus geplant werden, sodass sie wirksam werden, oder_ Tropfen _, entsprechend Ihrem definierten Zeitplan.

![Geplante Design-Aktualisierung](./assets/product-design-update-scheduled-ce.png){width="600" zoomable="yes"}


| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Schedule Update From/To] | Bestimmt den Datumsbereich, in dem ein benutzerdefiniertes Layout auf das Produkt angewendet wird. |
| [!UICONTROL New Theme] | Wendet ein benutzerdefiniertes Design auf das Produkt an. |
| [!UICONTROL New Layout] | Wendet ein anderes Layout auf die Produktseite an. Optionen: <br/>**[!UICONTROL No layout updates]**- Standardmäßig sind keine Layoutaktualisierungen für die Produktseite verfügbar.<br/>**[!UICONTROL Empty]** - Ermöglicht die Definition eines eigenen Layouts, z. B. einer vierspaltigen Seite. (Erfordert ein Verständnis von XML.) <br/>**[!UICONTROL 1 column]**- Wendet ein einspaltiges Layout auf die Produktseite an.<br/>**[!UICONTROL 2 columns with left bar]** - Wendet ein zweispaltiges Layout mit einer linken Seitenleiste auf die Produktseite an. <br/>**[!UICONTROL 2 columns with right bar]**- Wendet ein zweispaltiges Layout mit einer rechten Seitenleiste auf die Produktseite an.<br/>**[!UICONTROL 3 columns]** - Wendet ein dreiseitiges Layout auf die Produktseite an. |

{style="table-layout:auto"}
