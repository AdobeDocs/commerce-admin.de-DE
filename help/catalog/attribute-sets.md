---
title: Attributsätze
description: Erfahren Sie, wie Sie Attribute in Gruppen organisieren, die bestimmen, wo sie im Produktdatensatz angezeigt werden.
exl-id: de0c5fa2-158c-44ff-b84d-e4904ed8aa7d
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 0%

---

# Attributsätze

Einer der ersten Schritte beim Erstellen eines Produkts besteht darin, den Attributsatz auszuwählen, der als Vorlage für den Produktdatensatz verwendet wird. Der Attributsatz bestimmt die Felder, die während der Dateneingabe verfügbar sind, und die Werte, die dem Kunden angezeigt werden.

Die Attribute sind in Gruppen unterteilt, die bestimmen, wo sie im Produktdatensatz angezeigt werden. Ihr Store verfügt über einen anfänglichen Attributsatz (namens _default_), die eine Reihe häufig verwendeter Attribute enthält. Wenn Sie nur einige Attribute hinzufügen möchten, können Sie diese zu diesem standardmäßigen Attributsatz hinzufügen. Wenn Sie Produkte verkaufen, die bestimmte Arten von Informationen erfordern, ist es möglicherweise besser, einen dedizierten Attributsatz zu erstellen, der die spezifischen Attribute enthält, die für das Produkt erforderlich sind.

![Attributsätze](./assets/attribute-sets.png){width="700" zoomable="yes"}

## Erstellen eines Attributsatzes

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Attribute Set]**.

1. Klicken **[!UICONTROL Add New Set]**.

   ![Attributsatz - Name der Bearbeitung](./assets/attribute-set-new.png){width="600" zoomable="yes"}

1. Geben Sie einen **[!UICONTROL Name]** für den Attributsatz.

1. Satz **[!UICONTROL Based On]** zu einem vorhandenen Attributsatz, der als Vorlage verwendet werden soll.

1. click **[!UICONTROL Save]**.

   Auf der nächsten Seite wird Folgendes angezeigt:

   - Die linke Spalte zeigt den Namen des Attributsatzes an. Der Name dient als interne Referenz und kann bei Bedarf geändert werden.
   - In der Mitte der Seite wird die aktuelle Auswahl der Attributgruppen aufgelistet.
   - In der rechten Spalte wird die Auswahl der Attribute aufgelistet, die dem Attributsatz derzeit nicht zugewiesen sind.

1. Um dem Satz ein Attribut hinzuzufügen, ziehen Sie das Attribut aus dem **[!UICONTROL Unassigned Attributes]** Liste zum entsprechenden Ordner im **[!UICONTROL Groups]** Spalte.

   >[!NOTE]
   >
   >Systemattribute sind mit einem Punkt markiert und können nicht aus dem _[!UICONTROL Groups]_Liste. Sie können jedoch in eine andere Gruppe im Attributsatz gezogen werden.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]**.

![Attributset - edit](./assets/attribute-set-edit.png){width="600" zoomable="yes"}

## Erstellen einer Attributgruppe

1. Im _[!UICONTROL Groups]_Spalte der Attributfestlegung, klicken Sie auf **[!UICONTROL Add New]**.

1. Geben Sie einen **[!UICONTROL Name]** für die neue Gruppe und klicken Sie auf **[!UICONTROL OK]**.

1. Führen Sie einen der folgenden Schritte aus:

   - Ziehen **[!UICONTROL Unassigned Attributes]** an die neue Gruppe an.
   - Ziehen Sie Attribute aus einer anderen Gruppe in die neue Gruppe.

   Die neue Gruppe wird zu einem Abschnitt mit Attributen in jedem Produkt, das auf dem Attributsatz basiert.

## Löschen eines Attributsatzes

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Attribute Set]**.

1. Wählen Sie den Attributsatz in der Liste aus und öffnen Sie ihn im Bearbeitungsmodus.

1. Klicken **[!UICONTROL Delete]**.

1. Klicken Sie bei Aufforderung zur Bestätigung auf **[!UICONTROL OK]**.
