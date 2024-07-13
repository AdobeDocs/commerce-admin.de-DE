---
title: Unternehmensverwaltung
description: Optimierung der Verwaltung und Verwaltung von B2B-Organisationen mit komplexen Betriebsmodellen.
feature: B2B, Companies, Storefront
role: Admin
hide: false
hidefromtoc: false
exl-id: 8246be3d-ff9f-4f9f-875d-1b999befc534
source-git-commit: 582f15c422e43af9acec6313c7b777b3126030f8
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# Unternehmensverwaltung

[!BADGE 1.5.0-beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Nur für Beta-Programmteilnehmer verfügbar"}

Das Unternehmensmanagement optimiert den Geschäftsbetrieb für Unternehmen mit komplexen Organisationsstrukturen. Administratoren können eine Unternehmenshierarchie erstellen, um eine B2B-Organisation zu spiegeln, indem sie Unternehmen der angegebenen Muttergesellschaft zuweisen. Diese Zuweisung ermöglicht es dem Administrator der Muttergesellschaft, Unternehmen innerhalb der Organisation anzuzeigen und zu verwalten.

Starten Sie Unternehmensverwaltungsaufgaben über die Ansicht &quot;*[!UICONTROL Companies]*&quot;. Wechseln Sie vom Administrator zu **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

![B2B Unternehmenssteuerfeld verwalten](./assets/companies-grid-view.png){width="700" zoomable="yes"}

In der Spalte *[!UICONTROL Companies grid]* gibt die Spalte *[!UICONTROL Company Type]* an, ob ein Unternehmen als Teil einer Organisation oder als separates Unternehmen verwaltet wird.

- `Parent` ist eine Geschäftsorganisation mit einem oder mehreren zugewiesenen Unternehmen. Eine Muttergesellschaft kann nicht als untergeordnetes Element eines anderen Unternehmens zugewiesen werden.

- `Child` ist ein Unternehmen, das einer Organisation zugewiesen wurde. Ein Unternehmen kann nur einer Muttergesellschaft zugewiesen werden.

- `Company` steht für ein einzelnes Unternehmen. Ein einzelnes Unternehmen kann Teil einer Organisation werden, indem es eine Muttergesellschaft wird oder sie einer bestehenden Muttergesellschaft zuweist.

Wenn Sie ein übergeordnetes oder untergeordnetes Unternehmen bearbeiten, erweitern Sie *[!UICONTROL Company Hierarchy]* , um alle Unternehmen in der Organisation anzuzeigen. Eine `Current` -Markierung gibt das Unternehmen an, das Sie bearbeiten.

![B2B-Unternehmenshierarchie-Raster](./assets/company-detail-hierarchy-current-flag.png){width="700" zoomable="yes"}


## Anzeigen und Konfigurieren des [!UICONTROL Company Hierarchy]

Bei der ersten Unternehmenserstellung ist das Raster [!UICONTROL Company Hierarchy] leer. Sie ist auch leer, wenn es sich bei dem Unternehmen um ein einzelnes Unternehmen handelt.

![B2B-Firmenhierarchieraster](./assets/company-hierarchy-grid.png){width="700" zoomable="yes"}

Für Mutterunternehmen können Admin-Benutzer mit entsprechenden Berechtigungen die folgenden Aufgaben ausführen:

- Erstellen Sie die Unternehmenshierarchie, indem Sie eine neue übergeordnete Organisation erstellen oder eine bestehende aktualisieren.
- Verwalten Sie eine bestehende Organisation, um Unternehmen hinzuzufügen oder zu entfernen.

Weitere Informationen finden Sie unter [Verwalten der Unternehmenshierarchie](assign-companies.md).
