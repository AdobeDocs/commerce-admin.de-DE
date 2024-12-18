---
title: Verwalten der Unternehmenshierarchie
description: Erstellen und verwalten Sie Unternehmenshierarchien, um B2B-Organisationen mit komplexen Betriebsmodellen zu unterstützen.
feature: B2B, Companies
role: Admin
hide: false
hidefromtoc: false
exl-id: a277ed95-7935-4d27-adb2-35116972732b
source-git-commit: 6b06f52eb4ee8ca136a1c60fd6dc04a9ac96bbfa
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 0%

---

# [!UICONTROL Company Hierarchy] verwalten

Administratoren können eine [!UICONTROL Company Hierarchy] erstellen, indem sie verknüpfte Unternehmen einer bestimmten übergeordneten Firma zuweisen, welche die Firma an der Spitze der Organisationshierarchie ist.

Erstellen Sie vom Administrator aus eine übergeordnete Firma, indem Sie eine einzelne Firma (`[!UICONTROL Company Type] = Company`) bearbeiten und in der [!UICONTROL Company Hierarchy]-Konfiguration verwandte Firmen zuweisen.

![Unternehmenshierarchierarchieraster](./assets/company-hierarchy-grid.png){width="700"}


>[!NOTE]
>
>Weitere Informationen zum [!UICONTROL Company Hierarchy] finden Sie unter [Unternehmenshierarchie](account-company-create.md#company-hierarchy) Feldbeschreibungen.

Verwalten Sie Unternehmenszuweisungen, indem Sie eine übergeordnete Firma bearbeiten und mithilfe des *[!UICONTROL Company Hierarchy]* Firmen hinzufügen oder entfernen. Verwenden Sie das *[!UICONTROL Actions]*, um die [erweiterten Einstellungen“ für ](#change-company-settings) in der Organisation zu verwalten.

## Firmen einer übergeordneten Firma zuweisen

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![Firmen-Raster](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. Öffnen Sie im [!UICONTROL Companies] die Seite „Firmendetails“, um die Zuweisungen zu erstellen.

   - Um einer bestehenden übergeordneten Firma zusätzliche Firmen zuzuweisen, wählen Sie die **[!UICONTROL Edit]** für die übergeordnete Firma aus.
   - Um eine übergeordnete Firma zu erstellen, wählen Sie die **[!UICONTROL Edit]** Aktion für die als übergeordnete Firma angegebene Firma aus.

     Sie können keine neue übergeordnete Firma aus einer vorhandenen übergeordneten oder untergeordneten Firma erstellen.

1. Erweitern Sie auf der Seite „Unternehmensdetails“ **[!UICONTROL Company Hierarchy]** und klicken Sie dann auf **[!UICONTROL Assign Companies]**.

   ![Übergeordnete Firma erstellen](./assets/company-hierarchy-grid.png){width="675" zoomable="yes"}

1. Wählen Sie aus der Liste der verfügbaren Unternehmen die zuzuweisenden Unternehmen aus und klicken Sie dann auf **[!UICONTROL Assign Selected Companies]**.

   ![Firmen zum Zuweisen auswählen](./assets/company-hierarchy-select-companies-assign.png){width="675" zoomable="yes"}

1. Wenn Sie dazu aufgefordert werden, schließen Sie die Unternehmenszuweisung ab, indem Sie **[!UICONTROL Assign]** auswählen.

## Zuweisung von Firmen zu einer übergeordneten Firma aufheben

1. Öffnen Sie auf der Seite Firmen die Firmendetailseite für die übergeordnete Firma, indem Sie die Aktion **[!UICONTROL Edit]** auswählen.

   ![Detailseite des übergeordneten Unternehmens](./assets/company-update.png){width="700" zoomable="yes"}

1. Anzeigen der Liste der zugewiesenen Unternehmen durch Erweitern von **[!UICONTROL Company Hierarchy]**.

1. Entfernen Sie die Firma aus der Organisation.

   - Wählen Sie in der Spalte [!UICONTROL Action] für das zu entfernende Unternehmen **[!UICONTROL Select]** > **[!UICONTROL Unassign from parent]** aus.

     ![Entfernen einer Firma aus einer Organisation](./assets/company-hierarchy-grid-unassign.png){width="640" zoomable="yes"}

   - Wenn Sie dazu aufgefordert werden, entfernen Sie die zugewiesene Firma aus der Hierarchie, indem Sie **[!UICONTROL Unassign]** auswählen.

## Verwalten von Unternehmenseinstellungen für eine Organisation

Aktualisieren Sie die [Erweiterte Einstellungen](account-company-create.md#advanced-settings) für eine Organisation, um die übergeordnete Konfiguration auf alle untergeordneten Unternehmen anzuwenden oder dieselben Einstellungen auf ausgewählte Unternehmen in der Organisation anzuwenden.

Während des Aktualisierungsprozesses entsprechen die anfänglichen Konfigurationswerte standardmäßig den aktuellen Werten, die für die übergeordnete Firma konfiguriert wurden. Sie müssen mindestens eine Einstellung ändern, um die Konfiguration für ausgewählte Unternehmen zu aktualisieren.

**Ändern Sie die Konfiguration der erweiterten Einstellungen für mehrere Unternehmen**

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Bearbeiten Sie im [!UICONTROL Companies] das übergeordnete Unternehmen, indem Sie **[!UICONTROL Edit]** aus der Spalte **[!UICONTROL Action]** auswählen.

1. Erweitern Sie auf der Seite mit den übergeordneten Firmendetails **[!UICONTROL Company Hierarchy]** Abschnitt, um die in der Organisation enthaltenen Unternehmen anzuzeigen.

1. Wählen Sie die zu konfigurierenden Unternehmen aus.

   ![Unternehmen aus der Unternehmenshierarchie auswählen](assets/company-hierarchy-select-companies.png){width="675" zoomable="yes"}

1. Wählen Sie im **[!UICONTROL Actions]** über dem Raster **[!UICONTROL Change company settings]** aus.

   ![Ändern der Unternehmenseinstellungen für die Unternehmenshierarchie](assets/company-hierarchy-change-company-settings-action.png){width="675" zoomable="yes"}

1. Ändern Sie die Konfigurationseinstellungen.

   - Suchen Sie auf der Seite [!UICONTROL Change company settings] nach der zu ändernden Konfigurationseinstellung.

   - Aktivieren Sie das Kontrollkästchen **[!UICONTROL Change]** , um die Einstellung zu aktivieren.

   - Aktualisieren Sie den Wert nach Bedarf.

     ![Ändern der Unternehmenseinstellungen für mehrere Unternehmen](assets/company-hierarchy-change-settings-config.png){width="575" zoomable="yes"}

1. Wählen Sie nach dem Aktualisieren der Konfiguration **[!UICONTROL Apply Changes]** aus.

1. Wenn Sie dazu aufgefordert werden, wählen Sie **[!UICONTROL Change settings]** aus, um die Konfiguration für die ausgewählten Unternehmen zu aktualisieren.

>[!TIP]
>
>Verwalten Sie die erweiterten Konfigurationseinstellungen für eine einzelne Firma, indem Sie den Zeileneintrag der Firma bearbeiten.
