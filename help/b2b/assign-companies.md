---
title: Verwalten der Unternehmenshierarchie
description: Erfahren Sie, wie Sie B2B-Organisationen mit komplexen Betriebsmodellen verwalten können, indem Sie Hierarchien von Unternehmen aufbauen.
feature: B2B, Companies
role: Admin
hide: false
hidefromtoc: false
exl-id: a277ed95-7935-4d27-adb2-35116972732b
source-git-commit: 582f15c422e43af9acec6313c7b777b3126030f8
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 0%

---

# Verwalten der [!UICONTROL Company Hierarchy]

[!BADGE 1.5.0-beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Nur für Beta-Programmteilnehmer verfügbar"}

Administratoren können eine &quot;[!UICONTROL Company Hierarchy]&quot;-Variable erstellen, indem sie verbundene Unternehmen einer angegebenen Muttergesellschaft zuweisen, der das Unternehmen oben in der Organisation angehört. Wenn der [!UICONTROL Company Type]-Wert `Company` ist, ist das Unternehmen nicht Teil einer Organisation und berechtigt, eine Muttergesellschaft zu werden oder einer bestehenden Muttergesellschaft zuzuweisen.

Im Admin verwalten Sie Unternehmenszuweisungen, indem Sie ein Unternehmen bearbeiten und dann die Konfiguration [!UICONTROL Company Hierarchy] aktualisieren, um Unternehmen zuzuweisen oder die Zuweisung aufzuheben.

![Unternehmenshierarchieraster](./assets/company-detail-hierarchy-current-flag.png){width="700"}

>[!NOTE]
>
>Weitere Informationen zum Raster [!UICONTROL Company Hierarchy] finden Sie unter Feldbeschreibungen für die [Unternehmenshierarchie](account-company-create.md#company-hierarchy) .

## Zuweisen von Unternehmen zu einer Organisation

1. Navigieren Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![Unternehmensraster](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. Öffnen Sie im Raster [!UICONTROL Companies] die Detailseite des Unternehmens, um die Zuweisungen zu erstellen.

   - Um einer bestehenden Muttergesellschaft weitere Unternehmen zuzuweisen, wählen Sie die Aktion **[!UICONTROL Edit]** für die Muttergesellschaft aus.
   - Um eine Muttergesellschaft zu erstellen, wählen Sie die Aktion **[!UICONTROL Edit]** aus, die das Unternehmen als Mutterunternehmen festlegen soll.

     Es ist nicht möglich, eine Muttergesellschaft aus einer bestehenden Muttergesellschaft oder einem untergeordneten Unternehmen zu erstellen.

1. Erweitern Sie auf der Detailseite des Unternehmens den Wert **[!UICONTROL Company Hierarchy]**.

   ![Unternehmenshierarchieraster](./assets/company-detail-hierarchy-current-flag.png){width="700" zoomable="yes"}

   Das Raster zeigt vorhandene Unternehmenszuweisungen an, sofern vorhanden. Die Muttergesellschaft wird immer oben im Raster [!UICONTROL Company Hierarchy] positioniert. Die Markierung `[!UICONTROL Current]` gibt das Unternehmen an, das bearbeitet wird.

1. Fügen Sie Unternehmen zur übergeordneten Organisation hinzu.

   - Wählen Sie aus einer Liste der verfügbaren Unternehmen **[!UICONTROL Assign Companies]** aus.

   - **Alle auf dieser Seite auswählen** oder ein oder mehrere bestimmte Zeileneinträge für das Unternehmen auswählen.

   - Wählen Sie **[!UICONTROL Assign Selected Companies]** aus.

   - Schließen Sie die Unternehmenszuweisung durch Auswahl von **[!UICONTROL Assign]** ab.

     ![Unternehmen Organisation zuweisen](./assets/assign-selected-companies-hierarchy.png){width="675" zoomable="yes"}

## Aufheben der Zuweisung von Unternehmen zu einer Muttergesellschaft

1. Navigieren Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![Unternehmensraster](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. Öffnen Sie im Raster [!UICONTROL Companies] die Detailseite des Unternehmens für das übergeordnete Unternehmen, indem Sie **[!UICONTROL Edit]** auswählen.

1. Zeigen Sie die Liste der zugewiesenen Unternehmen durch Erweiterung von **[!UICONTROL Company Hierarchy]** an.

1. Heben Sie im Raster [!UICONTROL Company Hierarchy] die Zuweisung eines Unternehmens auf, indem Sie das Aktionssteuerelement **[!UICONTROL Select]** zur Auswahl von **[!UICONTROL Unassign from parent]** verwenden.

   ![Zuweisung von Unternehmen zu einer übergeordneten Organisation aufheben](./assets/company-hierarchy-grid-unassign.png){width="700" zoomable="yes"}

1. Entfernen Sie bei Aufforderung das zugewiesene Unternehmen aus der Hierarchie, indem Sie **[!UICONTROL Unassign]** auswählen.
