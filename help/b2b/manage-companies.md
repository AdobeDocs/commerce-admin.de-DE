---
title: Unternehmensverwaltung
description: Optimierung der Verwaltung und Verwaltung von B2B-Organisationen mit komplexen Betriebsmodellen.
feature: B2B, Companies, Storefront
role: Admin
hide: false
hidefromtoc: false
exl-id: 8246be3d-ff9f-4f9f-875d-1b999befc534
source-git-commit: 6b06f52eb4ee8ca136a1c60fd6dc04a9ac96bbfa
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---

# Unternehmensverwaltung

Das Unternehmensmanagement optimiert den Geschäftsbetrieb für Unternehmen mit komplexen Organisationsstrukturen. Administratoren können eine Unternehmenshierarchie erstellen, um eine B2B-Organisation zu spiegeln, indem sie Unternehmen der angegebenen Muttergesellschaft zuweisen. Diese Zuweisung ermöglicht es dem Administrator der Muttergesellschaft, Unternehmen innerhalb der Organisation anzuzeigen und zu verwalten.

Starten Sie Unternehmensverwaltungsaufgaben über die Ansicht &quot;*[!UICONTROL Companies]*&quot;. Wechseln Sie vom Administrator zu **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

![B2B Unternehmenssteuerfeld verwalten](./assets/companies-grid-view.png){width="700" zoomable="yes"}

Die Spalte *[!UICONTROL Company Type]* gibt an, ob ein Unternehmen als Teil eines Unternehmens oder als separates Unternehmen verwaltet wird.

- `Parent` ist eine Geschäftsorganisation mit einem oder mehreren zugewiesenen Unternehmen. Eine Muttergesellschaft kann nicht als untergeordnetes Element eines anderen Unternehmens zugewiesen werden.

- `Child` ist ein Unternehmen, das einer Organisation zugewiesen wurde. Ein Unternehmen kann nur einer Muttergesellschaft zugewiesen werden.

- `Company` steht für ein einzelnes Unternehmen. Ein einzelnes Unternehmen kann Teil einer Organisation werden, indem es eine Muttergesellschaft wird oder sie einer bestehenden Muttergesellschaft zuweist.

Wenn Sie ein übergeordnetes oder untergeordnetes Unternehmen bearbeiten, erweitern Sie *[!UICONTROL Company Hierarchy]* , um alle Unternehmen in der Organisation anzuzeigen. Eine `Current` -Markierung gibt das Unternehmen an, das Sie bearbeiten.

![B2B-Unternehmenshierarchie-Raster](./assets/company-detail-hierarchy-current-flag.png){width="700" zoomable="yes"}

## Anzeigen und Konfigurieren des [!UICONTROL Company Hierarchy]

Bei der ersten Unternehmenserstellung ist das Raster *[!UICONTROL Company Hierarchy]* leer. Sie ist auch leer, wenn es sich bei dem Unternehmen um ein einzelnes Unternehmen handelt.

![B2B-Firmenhierarchieraster](./assets/company-hierarchy-grid.png){width="700" zoomable="yes"}

Wenn das Unternehmen ein Mutterunternehmen einer Organisation ist und die Konten des Unternehmens für andere Unternehmen in der Organisation bereits in Adobe Commerce konfiguriert wurden, können Admin-Benutzer mit entsprechenden Berechtigungen Unternehmen zuweisen und das Raster *[!UICONTROL Company Hierarchy]* verwenden, um andere Unternehmensverwaltungsaufgaben durchzuführen:

- Alle mit dem Mutterunternehmen verbundenen Unternehmen anzeigen.
- Weisen Sie der Organisation von einer Detailseite des Mutterunternehmens aus weitere Unternehmen zu.
- Entfernen Sie ein Unternehmen aus einer Organisation, indem Sie die Aktion *[!UICONTROL Unassign from parent]* verwenden.
- Aktualisieren Sie die Konfiguration *[!UICONTROL Advanced Settings]* , um dieselben Einstellungen auf mehrere Unternehmen anzuwenden.

Detaillierte Anweisungen finden Sie unter [Verwalten der Unternehmenshierarchie](manage-company-hierarchy.md).

