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

# Verwalten der [!UICONTROL Company Hierarchy]

Administratoren können eine &quot;[!UICONTROL Company Hierarchy]&quot;-Variable erstellen, indem sie verbundene Unternehmen einer bestimmten Muttergesellschaft zuweisen, der das Unternehmen oben in der Organisationshierarchie angehört.

Erstellen Sie ausgehend vom Administrator eine Muttergesellschaft, indem Sie ein einzelnes Unternehmen (`[!UICONTROL Company Type] = Company`) bearbeiten und verbundene Unternehmen in der [!UICONTROL Company Hierarchy] -Konfiguration zuweisen.

![Unternehmenshierarchieraster](./assets/company-hierarchy-grid.png){width="700"}


>[!NOTE]
>
>Weitere Informationen zum Raster [!UICONTROL Company Hierarchy] finden Sie unter Feldbeschreibungen für die [Unternehmenshierarchie](account-company-create.md#company-hierarchy) .

Verwalten Sie Unternehmenszuweisungen, indem Sie eine Muttergesellschaft bearbeiten und das Raster *[!UICONTROL Company Hierarchy]* zum Hinzufügen oder Entfernen von Unternehmen verwenden. Verwenden Sie das Steuerelement *[!UICONTROL Actions]* , um die Konfiguration der erweiterten Einstellungen [ für Unternehmen in der Organisation zu verwalten.](#change-company-settings)

## Zuweisen von Unternehmen zu einer Muttergesellschaft

1. Navigieren Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![Unternehmensraster](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. Öffnen Sie im Raster [!UICONTROL Companies] die Detailseite des Unternehmens, um die Zuweisungen zu erstellen.

   - Um einer bestehenden Muttergesellschaft weitere Unternehmen zuzuweisen, wählen Sie die Aktion **[!UICONTROL Edit]** für die Muttergesellschaft aus.
   - Um eine Muttergesellschaft zu erstellen, wählen Sie die Aktion &quot;**[!UICONTROL Edit]**&quot;für das als Mutterunternehmen bezeichnete Unternehmen aus.

     Es ist nicht möglich, eine neue Muttergesellschaft aus einer bestehenden Muttergesellschaft oder einem untergeordneten Unternehmen zu erstellen.

1. Erweitern Sie auf der Detailseite Firma den Eintrag **[!UICONTROL Company Hierarchy]** und wählen Sie dann **[!UICONTROL Assign Companies]** aus.

   ![Mutterunternehmen erstellen](./assets/company-hierarchy-grid.png){width="675" zoomable="yes"}

1. Wählen Sie aus der Liste der verfügbaren Unternehmen die zuzuweisenden Unternehmen und dann **[!UICONTROL Assign Selected Companies]** aus.

   ![Wählen Sie die Unternehmen aus, die zugewiesen werden sollen.](./assets/company-hierarchy-select-companies-assign.png){width="675" zoomable="yes"}

1. Wenn Sie dazu aufgefordert werden, schließen Sie die Unternehmenszuweisung durch Auswahl von **[!UICONTROL Assign]** ab.

## Aufheben der Zuweisung von Unternehmen zu einer Muttergesellschaft

1. Öffnen Sie auf der Seite &quot;Unternehmen&quot;die Firmendetailseite für das Mutterunternehmen, indem Sie die Aktion &quot;**[!UICONTROL Edit]**&quot;auswählen.

   ![Übergeordnete Firmendetailseite](./assets/company-update.png){width="700" zoomable="yes"}

1. Zeigen Sie die Liste der zugewiesenen Unternehmen durch Erweiterung von **[!UICONTROL Company Hierarchy]** an.

1. Entfernen Sie das Unternehmen aus der Organisation.

   - In der Spalte [!UICONTROL Action] für das zu entfernende Unternehmen **[!UICONTROL Select]** > **[!UICONTROL Unassign from parent]**.

     ![Entfernen eines Unternehmens aus einer Organisation](./assets/company-hierarchy-grid-unassign.png){width="640" zoomable="yes"}

   - Entfernen Sie bei Aufforderung das zugewiesene Unternehmen aus der Hierarchie, indem Sie **[!UICONTROL Unassign]** auswählen.

## Unternehmenseinstellungen für eine Organisation verwalten

Aktualisieren Sie die Konfiguration [Erweiterte Einstellungen](account-company-create.md#advanced-settings) für eine Organisation, um die übergeordnete Konfiguration auf alle untergeordneten Unternehmen anzuwenden oder um dieselben Einstellungen auf ausgewählte Unternehmen in der Organisation anzuwenden.

Während des Aktualisierungsprozesses werden die ursprünglichen Konfigurationswerte standardmäßig auf die für das Mutterunternehmen konfigurierten aktuellen Werte gesetzt. Sie müssen mindestens eine Einstellung ändern, um die Konfiguration für ausgewählte Unternehmen zu aktualisieren.

**Ändern der Konfiguration der erweiterten Einstellungen für mehrere Unternehmen**

1. Navigieren Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

1. Bearbeiten Sie im Raster [!UICONTROL Companies] die übergeordnete Firma, indem Sie in der Spalte **[!UICONTROL Action]** die Option **[!UICONTROL Edit]** auswählen.

1. Erweitern Sie auf der Detailseite des übergeordneten Unternehmens den Abschnitt **[!UICONTROL Company Hierarchy]** , um die in der Organisation enthaltenen Unternehmen anzuzeigen.

1. Wählen Sie die zu konfigurierenden Unternehmen aus.

   ![Unternehmen aus der Unternehmenshierarchie auswählen](assets/company-hierarchy-select-companies.png){width="675" zoomable="yes"}

1. Wählen Sie aus dem Steuerelement **[!UICONTROL Actions]** oberhalb des Rasters **[!UICONTROL Change company settings]** aus.

   ![Ändern der Unternehmenseinstellungen für die Unternehmenshierarchie](assets/company-hierarchy-change-company-settings-action.png){width="675" zoomable="yes"}

1. Ändern Sie die Konfiguration der Einstellungen.

   - Suchen Sie auf der Seite [!UICONTROL Change company settings] nach der Konfigurationseinstellung, die geändert werden soll.

   - Aktivieren Sie das Kontrollkästchen **[!UICONTROL Change]** , um die Einstellung zu aktivieren.

   - Aktualisieren Sie den Wert nach Bedarf.

     ![Ändern der Unternehmenseinstellungen für mehrere Unternehmen](assets/company-hierarchy-change-settings-config.png){width="575" zoomable="yes"}

1. Wählen Sie nach dem Aktualisieren der Konfiguration **[!UICONTROL Apply Changes]** aus.

1. Wenn Sie dazu aufgefordert werden, wählen Sie **[!UICONTROL Change settings]** aus, um die Konfiguration für die ausgewählten Unternehmen zu aktualisieren.

>[!TIP]
>
>Verwalten Sie die Konfiguration der erweiterten Einstellungen für ein einzelnes Unternehmen, indem Sie den Zeileneintrag &quot;Unternehmen&quot;bearbeiten.
