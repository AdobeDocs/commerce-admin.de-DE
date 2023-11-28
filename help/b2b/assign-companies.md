---
title: Verwalten der Unternehmenshierarchie
description: Erstellen und verwalten Sie Unternehmenshierarchien, um B2B-Organisationen mit komplexen Betriebsmodellen zu unterstützen.
feature: B2B, Companies
role: Admin
hide: false
hidefromtoc: false
exl-id: a277ed95-7935-4d27-adb2-35116972732b
source-git-commit: 10b01db562777ef2fcc224177d7a83c0a6fc90e7
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 0%

---

# Verwalten Sie die [!UICONTROL Company Hierarchy]

[!BADGE 1.5.0-Beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Nur für Beta-Programmteilnehmer verfügbar"}

Administratoren können eine [!UICONTROL Company Hierarchy] indem verbundene Unternehmen einer benannten Muttergesellschaft zugewiesen werden, die das Unternehmen an der Spitze der Organisationshierarchie steht.

Erstellen Sie eine Muttergesellschaft, indem Sie ein Unternehmen bearbeiten, das keiner vorhandenen [!UICONTROL Company Hierarchy]und die Zuweisung verbundener Unternehmen.

![Unternehmenshierarchieraster](./assets/company-detail-view.png){width="700"}

Nachdem ein Unternehmen einer Hierarchie zugewiesen wurde, wird die [!UICONTROL Company type] in der **Unternehmen** Grid identifiziert das Unternehmen als `Parent` oder  `Child` Unternehmen.  Wenn die Variable [!UICONTROL Company Type] is `Company`, ist das Unternehmen nicht Teil einer Unternehmenshierarchie und berechtigt, Muttergesellschaft zu werden oder einer bestehenden Muttergesellschaft zuzuweisen.

>[!NOTE]
>
>Weitere Informationen zum [!UICONTROL Company Hierarchy] Raster, siehe [Unternehmenshierarchie](account-company-create.md#company-hierarchy) Feldbeschreibungen.

Im Admin verwalten Sie Unternehmenszuweisungen, indem Sie ein Unternehmen bearbeiten und dann die [!UICONTROL Company Hierarchy] Abschnitt [!UICONTROL Company] -Seite, um Unternehmen zuzuweisen oder die Zuweisung aufzuheben.

## Zuweisen von Unternehmen zu einer Muttergesellschaft

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![Unternehmensraster](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. Öffnen Sie im Raster Unternehmen die Detailseite des Unternehmens, um die Zuweisungen zu erstellen.

   - Um einer bestehenden Muttergesellschaft weitere Unternehmen zuzuweisen, wählen Sie die **[!UICONTROL Edit]** Maßnahmen für die Muttergesellschaft.
   - Um eine neue Muttergesellschaft zu erstellen, wählen Sie die **[!UICONTROL Edit]** Maßnahmen für die Muttergesellschaft.

     Es ist nicht möglich, eine neue Muttergesellschaft aus einer bestehenden Muttergesellschaft oder einem untergeordneten Unternehmen zu erstellen.

   ![Neue Firma](./assets/company-update.png){width="700" zoomable="yes"}

1. Erweitern Sie auf der Detailseite Firma die **[!UICONTROL Company Hierarchy]** und wählen Sie **[!UICONTROL Assign Companies]**.

   ![Neue Firma](./assets/company-hierarchy-grid.png){width="700" zoomable="yes"}

   Wenn Sie diese Ansicht erweitern, können Sie vorhandene Unternehmenszuweisungen sehen, sofern vorhanden. Die Muttergesellschaft erscheint immer über dem _[!UICONTROL Company Hierarchy]_Raster mit `current company indicator` in der Zeile des Unternehmens angezeigt, die bearbeitet wird.

1. Zur Zuweisung verfügbare Unternehmen werden im Raster aufgeführt. Wählen Sie die zuzuweisenden Unternehmen aus und wählen Sie dann **[!UICONTROL Assign Selected Companies]**.

1. Sie können **Alle auf dieser Seite auswählen** oder eines bestimmten Unternehmens-Zeileneintrags und klicken Sie auf **[!UICONTROL Assign Selected Companies]**.

   ![Neue Firma](./assets/assign-selected-companies.png){width="700" zoomable="yes"}

1. Wenn Sie dazu aufgefordert werden, schließen Sie die Unternehmenszuweisung ab, indem Sie **[!UICONTROL Assign]**.

## Aufheben der Zuweisung von Unternehmen zu einer Muttergesellschaft

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![Unternehmensraster](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. Öffnen Sie auf der Seite &quot;Unternehmen&quot;die Firmendetailseite für das Mutterunternehmen, indem Sie die **[!UICONTROL Edit]** Aktion.

   ![Neue Firma](./assets/company-update.png){width="700" zoomable="yes"}

1. Zeigen Sie die Liste der zugewiesenen Unternehmen an, indem Sie die **[!UICONTROL Company Hierarchy]** Dropdown.

1. Heben Sie die Zuweisung eines Unternehmens in der Hierarchie des Unternehmens auf, indem Sie die **[!UICONTROL Select]** Aktion für das Unternehmen und wählen Sie dann **[!UICONTROL Unassign from parent]**.

   ![Neue Firma](./assets/company-hierarchy-grid.png){width="700" zoomable="yes"}

1. Entfernen Sie bei Aufforderung das zugewiesene Unternehmen aus der Hierarchie, indem Sie **[!UICONTROL Unassign]**.
