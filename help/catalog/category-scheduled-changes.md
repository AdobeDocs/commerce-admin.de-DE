---
title: Geplante Änderungen für Kategorien
description: Erfahren Sie, wie Sie Kategorieänderungen zur Unterstützung von Marketing-Kampagnen und zum Speichern von Promotions planen.
exl-id: 9e25082f-4e76-4148-b76e-dca0b14971eb
feature: Catalog Management, Categories
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 0%

---

# Geplante Änderungen für Kategorien

{{ee-feature}}

Kategorieaktualisierungen können planmäßig angewendet und mit anderen Inhaltsänderungen gruppiert werden. Sie können eine Kampagne basierend auf geplanten Änderungen an der Kategorie erstellen oder die Änderungen auf eine bestehende Kampagne anwenden. Weitere Informationen finden Sie unter [Inhaltstaging](../content-design/content-staging.md).

>[!NOTE]
>
>Alle geplanten Aktualisierungen werden nacheinander angewendet, d. h. jede Entität kann nur eine geplante Aktualisierung gleichzeitig haben. Jede geplante Aktualisierung wird auf alle Store-Ansichten innerhalb des Zeitrahmens angewendet. Daher kann eine Entität nicht mehrere geplante Aktualisierungen für verschiedene Store-Ansichten gleichzeitig haben. Alle Entitätsattributwerte in allen Store-Ansichten, die von der aktuellen geplanten Aktualisierung nicht betroffen sind, werden von den Standardwerten übernommen und nicht von der vorherigen geplanten Aktualisierung.

## Eine Aktualisierung auf eine Kategorie planen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Wählen Sie in der Kategorienstruktur auf der linken Seite die zu ändernde Kategorie aus.

1. Im _Geplante Änderungen_ Klicken Sie oben auf der Seite auf **[!UICONTROL Schedule New Update]**.

   ![Geplante Änderungen](./assets/category-scheduled-changes.png){width="600" zoomable="yes"}

1. Mit dem **[!UICONTROL Save as a New Update]** die Option ausgewählt ist, legen Sie die grundlegenden Parameter für die Aktualisierung fest:

   - Für **[!UICONTROL Update Name]** Geben Sie einen Namen für die neue Inhaltstaging-Kampagne ein.

   - Kurzbeschreibung eingeben **[!UICONTROL Description]** der Aktualisierung und ihrer Verwendung.

   - Verwenden Sie den Kalender ( ![Kalendersymbol](../assets/icon-calendar.png) ), um das **[!UICONTROL Start Date]** und **[!UICONTROL End Date]** für die Kampagne.

   >[!IMPORTANT]
   >
   >Kampagne **[!UICONTROL Start Date]** und **[!UICONTROL End Date]** muss mithilfe der **_default_** Admin-Zeitzone, die aus der lokalen Zeitzone jeder Website konvertiert wird. Bei mehreren Websites in verschiedenen Zeitzonen, auf denen Sie eine Kampagne basierend auf einer US-Zeitzone starten möchten, müssen Sie beispielsweise für jede lokale Zeitzone eine separate Aktualisierung planen. Sie legen die **[!UICONTROL Start Date]** und **[!UICONTROL End Date]** für jede Variable, die aus der Zeitzone der lokalen Website in die standardmäßige Zeitzone des Administrators konvertiert wird.

   ![Geplante Änderungen](./assets/category-scheduled-changes-new-update.png){width="600" zoomable="yes"}

1. Nehmen Sie die erforderlichen Änderungen an der geplanten Aktualisierung vor.

1. Um eine Vorschau der Änderungen anzuzeigen, klicken Sie auf **[!UICONTROL Preview]** in der oberen rechten Schaltflächenleiste.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]**.

## Einer vorhandenen Aktualisierung zuweisen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Wählen Sie in der Kategorienstruktur auf der linken Seite die zu ändernde Kategorie aus.

1. Im _Geplante Änderungen_ Klicken Sie oben auf der Seite auf **[!UICONTROL Schedule New Update]**.

1. Auswählen **[!UICONTROL Assign to Existing Campaign]**.

1. Suchen Sie in der Liste die gewünschte Kampagne und klicken Sie auf **[!UICONTROL Select]**.

1. Nehmen Sie die erforderlichen Änderungen an der geplanten Aktualisierung vor.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]**.
