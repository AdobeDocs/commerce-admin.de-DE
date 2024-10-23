---
title: Geplante Änderungen für Kategorien
description: Erfahren Sie, wie Sie Kategorieänderungen zur Unterstützung von Marketing-Kampagnen und zum Speichern von Promotions planen.
exl-id: 9e25082f-4e76-4148-b76e-dca0b14971eb
feature: Catalog Management, Categories
source-git-commit: 714904d6d81bde6374a5ce644262de252c70a391
workflow-type: tm+mt
source-wordcount: '463'
ht-degree: 0%

---

# Geplante Änderungen für Kategorien

{{ee-feature}}

Kategorieaktualisierungen können planmäßig angewendet und mit anderen Inhaltsänderungen gruppiert werden. Sie können eine Kampagne basierend auf geplanten Änderungen an der Kategorie erstellen oder die Änderungen auf eine bestehende Kampagne anwenden. Weitere Informationen finden Sie unter [Inhaltstaging](../content-design/content-staging.md).

Beachten Sie beim Planen von Änderungen für Kategorien Folgendes:

- Alle geplanten Aktualisierungen werden nacheinander angewendet, d. h. jede Entität kann nur eine geplante Aktualisierung gleichzeitig haben. Jede geplante Aktualisierung wird auf alle Store-Ansichten innerhalb des Zeitrahmens angewendet. Daher kann eine Entität nicht mehrere geplante Aktualisierungen für verschiedene Store-Ansichten gleichzeitig haben. Alle Entitätsattributwerte in allen Store-Ansichten, die von der aktuellen geplanten Aktualisierung nicht betroffen sind, werden von den Standardwerten übernommen und nicht von der vorherigen geplanten Aktualisierung.

- Wenn eine Kampagne mit mehr als einer Kategorie verknüpft ist, kann die Kampagne nur über das Dashboard [Inhaltstaging-Dashboard](../content-design/content-staging-dashboard.md) bearbeitet werden.

- Wenn eine Kampagne mit mehr als einer Kategorie verknüpft ist, kann die Kampagne nur über das Dashboard [Inhaltstaging-Dashboard](../content-design/content-staging-dashboard.md) bearbeitet werden.

>[!NOTE]
>
>Die Registerkarte [!UICONTROL Schedule Design Update] wurde in der Adobe Commerce ![Adobe Commerce](../assets/adobe-logo.svg) entfernt und kann nicht direkt in der Kategorie geändert werden. Sie müssen eine geplante Aktualisierung für diese Aktivierungen erstellen.

## Eine Aktualisierung auf eine Kategorie planen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Wählen Sie in der Kategorienstruktur auf der linken Seite die zu ändernde Kategorie aus.

1. Klicken Sie im Feld _Geplante Änderungen_ oben auf der Seite auf **[!UICONTROL Schedule New Update]**.

   ![Geplante Änderungen](./assets/category-scheduled-changes.png){width="600" zoomable="yes"}

1. Legen Sie bei ausgewählter Option **[!UICONTROL Save as a New Update]** die grundlegenden Parameter für die Aktualisierung fest:

   - Geben Sie für **[!UICONTROL Update Name]** einen Namen für die neue Inhaltstaging-Kampagne ein.

   - Geben Sie eine kurze Beschreibung **[!UICONTROL Description]** der Aktualisierung ein und geben Sie an, wie sie verwendet werden soll.

   - Verwenden Sie das Tool Kalender ( ![Kalendersymbol](../assets/icon-calendar.png) ), um die **[!UICONTROL Start Date]** und die **[!UICONTROL End Date]** für die Kampagne auszuwählen.

   >[!IMPORTANT]
   >
   >Campaign **[!UICONTROL Start Date]** und **[!UICONTROL End Date]** müssen mithilfe der **_default_** Admin-Zeitzone definiert werden, die aus der lokalen Zeitzone jeder Website konvertiert wird. Bei mehreren Websites in verschiedenen Zeitzonen, auf denen Sie eine Kampagne basierend auf einer US-Zeitzone starten möchten, müssen Sie beispielsweise für jede lokale Zeitzone eine separate Aktualisierung planen. Sie legen die **[!UICONTROL Start Date]** und **[!UICONTROL End Date]** für jede Variable fest, die aus der Zeitzone der lokalen Website in die standardmäßige Zeitzone des Administrators konvertiert werden.

   ![Geplante Änderungen](./assets/category-scheduled-changes-new-update.png){width="600" zoomable="yes"}

1. Nehmen Sie die erforderlichen Änderungen an der geplanten Aktualisierung vor.

1. Um eine Vorschau der Änderungen anzuzeigen, klicken Sie in der oberen rechten Schaltflächenleiste auf **[!UICONTROL Preview]** .

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]**.

## Einer vorhandenen Aktualisierung zuweisen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Wählen Sie in der Kategorienstruktur auf der linken Seite die zu ändernde Kategorie aus.

1. Klicken Sie im Feld _Geplante Änderungen_ oben auf der Seite auf **[!UICONTROL Schedule New Update]**.

1. Wählen Sie **[!UICONTROL Assign to Existing Campaign]** aus.

1. Suchen Sie in der Liste die gewünschte Kampagne und klicken Sie auf **[!UICONTROL Select]**.

1. Nehmen Sie die erforderlichen Änderungen an der geplanten Aktualisierung vor.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]**.
