---
title: Produkteinstellungen - [!UICONTROL Sources]
description: Für ein Produkt bieten die Einstellungen für [!UICONTROL Sources] Zugriff auf die  [!DNL Inventory Management] Quellen, aus denen das Produkt verteilt werden kann.
exl-id: 986f6031-0edc-4105-aa02-1c22364b3e7c
feature: Catalog Management, Products, Inventory
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 0%

---

# Produkteinstellungen - [!UICONTROL Sources]

Im Abschnitt _[!UICONTROL Sources]_der Produkteinstellungen werden die Quellen aufgelistet, aus denen das Produkt verteilt werden kann. Sie wird verwendet, um Quellen zuzuweisen und die Zuweisung aufzuheben sowie die Menge und Verfügbarkeit des Produkts zu verwalten. Dieser Abschnitt wird nur angezeigt, wenn mehr als eine Quelle für Ihren Store definiert ist. Weitere Informationen zu Quellen finden Sie unter [Quellen verwalten](../inventory-management/sources-manage.md).

## Zuweisen einer Quelle für ein Produkt

1. Klicken Sie auf **[!UICONTROL Assign Source]**.

1. Aktivieren Sie das Kontrollkästchen für die erforderlichen Quellen.

1. Klicken Sie auf **[!UICONTROL Done]**.

1. Wählen Sie **[!UICONTROL Source Item Status]** aus und geben Sie die Werte **[!UICONTROL Qty]** und **[!UICONTROL Notify Qty]** nach Bedarf ein.

1. Klicken Sie auf **[!UICONTROL Save]** , um die Änderungen zu speichern.

![Ansicht der Quellen](./assets/catalog-sources-list.png){width="600" zoomable="yes"}

## Feldreferenz

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Name] | Der eindeutige Name einer Quelle. |
| [!UICONTROL Source Status] | Bestimmt, ob das Produkt im Katalog aktiviert oder deaktiviert ist. |
| [!UICONTROL Source Item Status] | Bestimmt die aktuelle Verfügbarkeit des Produkts. Optionen:<br />**[!UICONTROL In Stock]**- Stellt das Produkt zum Kauf bereit.<br />**[!UICONTROL Out of Stock]** - Sofern keine Rückorder aktiviert sind, verhindert, dass das Produkt zum Kauf verfügbar ist, und entfernt die Liste aus dem Katalog. |
| [!UICONTROL Qty] | Auf Lager befindliche Beträge für jede Quelle. |
| [!UICONTROL Notify Qty] | Ein Betrag für die _Für Menge benachrichtigen_ für diese bestimmte Quelle, wenn `Notify Quantity Use Default` nicht ausgewählt ist. |
| [!UICONTROL Notify Qty Use Default] | Gibt an, dass die Standardeinstellung für _Für Menge benachrichtigen_ in der Produkteinstellung &quot;Erweiterter Bestand&quot;oder in der Speicherkonfiguration als global verwendet wird. Weitere Informationen zu erweiterten Lagerbestandseinstellungen für Ihr Produkt finden Sie unter [Erweiterte Produktoptionen konfigurieren](../inventory-management/product-options.md). |
| [!UICONTROL Actions] | Klicken Sie für eine zugewiesene Quelle auf &quot;**[!UICONTROL Unassign]**&quot;, um die Quelle für das Produkt nicht verfügbar zu machen. Klicken Sie für eine nicht zugewiesene Quelle auf **[!UICONTROL Assign Sources]** , um eine Quelle für das Produkt verfügbar zu machen. Weitere Informationen zu den [!UICONTROL Assign Sources] -Optionen finden Sie unter [Zuweisen von Quellen pro Produkt](../inventory-management/sources-assign-per-product.md). |

{style="table-layout:auto"}
