---
title: Quellenzuweisung für Massenbestand und Aufhebung der Zuweisung
description: Erfahren Sie, wie Sie mit dem Tool Quellen zuweisen Quellzuweisungen für Produkte verwalten können.
exl-id: 1f1e81a5-fb06-46b7-84ca-7feea4942093
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 0%

---

# Massenzuweisung von Quellen und Aufhebung der Zuweisung

Verwenden Sie das Tool _Quellen zuweisen_ , um Ihren Produkten eine oder mehrere Quellen hinzuzufügen. Das Tool hilft beim Erstellen und Zuweisen benutzerdefinierter Quellen zu Ihrem Standardbestand oder benutzerdefinierten Lagern und beim Vorbereiten neuer Standorte und Lagerbestände.

Nachdem Sie neue benutzerdefinierte Quellen hinzugefügt haben, können Sie [Lagerbestandsmengen pro Produkt](quantities-assign-per-product.md) oder für mehrere Produkte über den Administrator oder die [Importfunktion](inventory-import-export.md) hinzufügen.

![Hinzufügen von Inventarquellen für ausgewählte Produkte](assets/inventory-bulk-assign-sources.gif)

## Quellen und Mengen zuweisen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Wählen Sie die Produkte aus, für die Sie die Quellen ändern möchten.

   Suchen oder suchen Sie nach den Produkten und aktivieren Sie diese Kontrollkästchen.

1. Klicken Sie auf das Menü **[!UICONTROL Actions]** oben und wählen Sie **[!UICONTROL Assign Inventory Source]** aus.

1. Klicken Sie im Bestätigungsdialogfeld auf &quot;**[!UICONTROL OK]**&quot;.

1. Aktivieren Sie die Kontrollkästchen für alle Quellen, die Sie den Produkten hinzufügen möchten.

1. Klicken Sie auf **[!UICONTROL Assign Sources]**.

   ![Wählen Sie Produkte aus, um Quellen hinzuzufügen](assets/inventory-bulk-assign-sources-summary.png){width="600" zoomable="yes"}

Die Quellen werden zu den Produkten mit einer Lagerbestandsmenge von 0 hinzugefügt. Sie können [Lagerbestandsmengen](quantities-assign-per-product.md) pro Quelle hinzufügen.

## Zuteilung von Quellen und Mengen aufheben

Wenn Sie die Zuweisung einer Quelle von einem Produkt aufheben, geben Sie an, dass das Produkt nicht mehr an diesem Speicherort gespeichert ist. Durch diesen Prozess werden alle Bestandsdaten für die Quelle, die dem Produkt derzeit zugewiesen ist, vollständig gelöscht. Wenn Sie den vorhandenen Bestand an einen neuen Speicherort verschieben möchten, sollten Sie die Option _Bestand übertragen_ in Erwägung ziehen.

{{$include /help/_includes/unassign-source.md}}

Es wird dringend empfohlen, alle Bestellungen und Sendungen für diese Produkte abzuschließen, bevor die Quelle entfernt wird.

![Zuweisung von Quellen für ausgewählte Produkte aufheben](assets/inventory-bulk-unassign-sources.gif)

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Wählen Sie die Produkte aus, deren Quellen Sie ändern möchten.

   Suchen oder suchen Sie nach den Produkten und aktivieren Sie diese Kontrollkästchen.

1. Klicken Sie auf das Menü **[!UICONTROL Actions]** oben und wählen Sie **[!UICONTROL Unassign Inventory Source]** aus.

1. Klicken Sie im Bestätigungsdialogfeld auf &quot;**[!UICONTROL OK]**&quot;.

1. Wählen Sie die Quelle aus, die Sie aus den Produkten entfernen möchten.

   Auf der Seite wird ein Warnhinweis angezeigt, durch den bei Aufhebung der Zuweisung alle spezifischen Quell- und Mengendaten aus dem Produkt entfernt werden.

1. Klicken Sie auf **[!UICONTROL Unassign Sources]**.

   ![Entfernen von Quellen aus ausgewählten Produkten](assets/inventory-bulk-unassign-sources-summary.png){width="600" zoomable="yes"}
