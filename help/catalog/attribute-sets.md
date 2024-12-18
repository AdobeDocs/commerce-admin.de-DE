---
title: Attributsätze
description: Erfahren Sie, wie Sie Attribute in Gruppen organisieren können, die bestimmen, wo sie im Produktdatensatz angezeigt werden.
exl-id: de0c5fa2-158c-44ff-b84d-e4904ed8aa7d
feature: Catalog Management, Products
source-git-commit: 43550b9370f4ed4b631ae7773324ed0913718a79
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# Attributsätze

Einer der ersten Schritte beim Erstellen eines Produkts besteht darin, den Attributsatz auszuwählen, der als Vorlage für den Produktdatensatz verwendet wird. Der Attributsatz bestimmt die Felder, die bei der Dateneingabe verfügbar sind, und die Werte, die dem Kunden angezeigt werden.

Die Attribute sind in Gruppen unterteilt, die bestimmen, wo sie im Produktdatensatz angezeigt werden. Ihr Store verfügt über einen anfänglichen Attributsatz (_default_) mit einer Reihe häufig verwendeter Attribute. Wenn Sie nur einige Attribute hinzufügen möchten, können Sie sie zu diesem Standardattributsatz hinzufügen. Wenn Sie Produkte verkaufen, für die bestimmte Arten von Informationen erforderlich sind, ist es möglicherweise besser, einen dedizierten Attributsatz zu erstellen, der die für das Produkt benötigten spezifischen Attribute enthält.

![Attributsätze](./assets/attribute-sets.png){width="700" zoomable="yes"}

## Erstellen eines Attributsatzes

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Attribute Set]**.

1. Klicken Sie auf **[!UICONTROL Add New Set]**.

   ![Attributsatz - Name bearbeiten](./assets/attribute-set-new.png){width="600" zoomable="yes"}

1. Geben Sie einen **[!UICONTROL Name]** für den Attributsatz ein.

1. Legen Sie **[!UICONTROL Based On]** auf ein vorhandenes Attribut fest, das als Vorlage verwendet werden soll.

1. Klicken Sie auf **[!UICONTROL Save]**.

   Auf der nächsten Seite wird Folgendes angezeigt:

   - In der linken Spalte wird der Name des Attributsatzes angezeigt. Der Name dient als interne Referenz und kann bei Bedarf geändert werden.
   - In der Mitte der Seite wird die aktuelle Auswahl von Attributgruppen aufgeführt.
   - In der rechten Spalte wird die Auswahl der Attribute aufgeführt, die derzeit nicht dem Attributsatz zugewiesen sind.

1. Um dem Set ein Attribut hinzuzufügen, ziehen Sie das Attribut aus der **[!UICONTROL Unassigned Attributes]** in den entsprechenden Ordner in der Spalte **[!UICONTROL Groups]** . Um ein Attribut aus dem Set zu entfernen, ziehen Sie es in die **[!UICONTROL Unassigned Attributes]**.

   >[!NOTE]
   >
   >Systemattribute sind mit einem Punkt gekennzeichnet und können nicht aus der _[!UICONTROL Groups]_entfernt werden. Sie können jedoch in eine andere Gruppe im Attributsatz gezogen werden.

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.

![Attributsatz - Bearbeiten](./assets/attribute-set-edit.png){width="600" zoomable="yes"}

## Erstellen einer Attributgruppe

1. Klicken Sie in der Spalte _[!UICONTROL Groups]_des Attributsatzes auf **[!UICONTROL Add New]**.

1. Geben Sie einen **[!UICONTROL Name]** für die neue Gruppe ein und klicken Sie auf **[!UICONTROL OK]**.

1. Führen Sie einen der folgenden Schritte aus:

   - Ziehen Sie **[!UICONTROL Unassigned Attributes]** in die neue Gruppe.
   - Ziehen Sie Attribute aus einer beliebigen anderen Gruppe in die neue Gruppe.
   - Ziehen Sie unnötige Attribute in den **[!UICONTROL Unassigned Attributes]**.

   Die neue Gruppe wird zu einem Abschnitt mit Attributen in jedem Produkt, das auf dem Attributsatz basiert.

## Löschen eines Attributsatzes

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Attribute Set]**.

1. Wählen Sie das in der Liste festgelegte Attribut aus und öffnen Sie es im Bearbeitungsmodus.

1. Klicken Sie auf **[!UICONTROL Delete]**.

1. Wenn Sie zum Bestätigen aufgefordert werden, klicken Sie auf **[!UICONTROL OK]**.
