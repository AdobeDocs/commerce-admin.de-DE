---
title: Unternehmensleitung
description: Optimieren Sie die Verwaltung und das Management von B2B-Organisationen mit komplexen Betriebsmodellen.
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

# Unternehmensleitung

Das Unternehmensmanagement optimiert die Geschäftsprozesse für Unternehmen mit komplexen Organisationsstrukturen. Admin-Benutzer können eine Unternehmenshierarchie erstellen, die eine B2B-Organisation spiegelt, indem sie der designierten übergeordneten Firma Firmen zuweisen. Diese Zuweisung ermöglicht es dem Administrator der übergeordneten Firma, Unternehmen innerhalb der Organisation anzuzeigen und zu verwalten.

Starten Sie Unternehmensverwaltungsaufgaben über die *[!UICONTROL Companies]*. Navigieren Sie vom Administrator aus zu **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

![B2B-Unternehmensraster verwalten](./assets/companies-grid-view.png){width="700" zoomable="yes"}

Die Spalte *[!UICONTROL Company Type]* gibt an, ob ein Unternehmen als Teil einer Organisation oder als separates Unternehmen verwaltet wird.

- `Parent` ist eine Unternehmensorganisation mit einem oder mehreren zugeordneten Unternehmen. Eine Muttergesellschaft kann nicht als untergeordnetes Element einer anderen Gesellschaft zugewiesen werden.

- `Child` ist eine Firma, die einer Organisation zugewiesen wurde. Eine Firma kann nur einer übergeordneten Firma zugewiesen werden.

- `Company` repräsentiert ein einzelnes Unternehmen. Ein einzelnes Unternehmen kann Teil einer Organisation werden, indem es zu einer Muttergesellschaft wird oder indem es einer bestehenden Muttergesellschaft zugewiesen wird.

Wenn Sie ein übergeordnetes oder untergeordnetes Unternehmen bearbeiten, erweitern Sie *[!UICONTROL Company Hierarchy]* , um alle Unternehmen in der Organisation anzuzeigen. Eine `Current` Markierung zeigt das Unternehmen an, das Sie bearbeiten.

![B2B-Unternehmens-Hierarchieraster](./assets/company-detail-hierarchy-current-flag.png){width="700" zoomable="yes"}

## Anzeigen und Konfigurieren der [!UICONTROL Company Hierarchy]

Bei der ersten Erstellung des Unternehmens ist das *[!UICONTROL Company Hierarchy]* leer. Es ist auch leer, wenn es sich bei dem Unternehmen um ein einzelnes Unternehmen handelt.

![B2B-Unternehmens-Hierarchieraster](./assets/company-hierarchy-grid.png){width="700" zoomable="yes"}

Wenn die Firma eine übergeordnete Firma für eine Organisation ist und die Unternehmenskonten für andere Firmen in der Organisation bereits in Adobe Commerce konfiguriert wurden, können Admin-Benutzer mit entsprechenden Berechtigungen Unternehmen zuweisen und das *[!UICONTROL Company Hierarchy]*-Raster verwenden, um andere Unternehmensverwaltungsaufgaben abzuschließen:

- Alle mit der übergeordneten Firma verknüpften Firmen anzeigen.
- Weisen Sie der Organisation auf der Seite mit den übergeordneten Firmendetails weitere Firmen zu.
- So entfernen Sie mithilfe der *[!UICONTROL Unassign from parent]* eine Firma aus einer Organisation.
- Aktualisieren Sie die *[!UICONTROL Advanced Settings]*, um dieselben Einstellungen auf mehrere Unternehmen anzuwenden.

Detaillierte Anweisungen finden Sie unter [Verwalten der Firmenhierarchie](manage-company-hierarchy.md).

