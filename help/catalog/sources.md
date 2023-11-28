---
title: Produkteinstellungen - [!UICONTROL Sources]
description: Bei einem Produkt muss die Variable [!UICONTROL Sources] -Einstellungen bieten Zugriff auf [!DNL Inventory Management] Quellen, aus denen das Produkt verteilt werden kann.
exl-id: 986f6031-0edc-4105-aa02-1c22364b3e7c
feature: Catalog Management, Products, Inventory
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 1%

---

# Produkteinstellungen - [!UICONTROL Sources]

Die _[!UICONTROL Sources]_in den Produkteinstellungen werden die Quellen aufgelistet, aus denen das Produkt verteilt werden kann. Sie wird verwendet, um Quellen zuzuweisen und die Zuweisung aufzuheben sowie die Menge und Verfügbarkeit des Produkts zu verwalten. Dieser Abschnitt wird nur angezeigt, wenn mehr als eine Quelle für Ihren Store definiert ist. Weitere Informationen zu Quellen finden Sie unter [Quellen verwalten](../inventory-management/sources-manage.md).

## Zuweisen einer Quelle für ein Produkt

1. Klicken **[!UICONTROL Assign Source]**.

1. Aktivieren Sie das Kontrollkästchen für die erforderlichen Quellen.

1. Klicken **[!UICONTROL Done]**.

1. Auswählen **[!UICONTROL Source Item Status]** und geben Sie die **[!UICONTROL Qty]** und **[!UICONTROL Notify Qty]** Werte nach Bedarf.

1. Klicks **[!UICONTROL Save]** , um die Änderungen zu speichern.

![Quellansicht](./assets/catalog-sources-list.png){width="600" zoomable="yes"}

## Feldreferenz

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Name] | Der eindeutige Name einer Quelle. |
| [!UICONTROL Source Status] | Bestimmt, ob das Produkt im Katalog aktiviert oder deaktiviert ist. |
| [!UICONTROL Source Item Status] | Bestimmt die aktuelle Verfügbarkeit des Produkts. Optionen:<br />**[!UICONTROL In Stock]**- Stellt das Produkt zum Kauf bereit.<br />**[!UICONTROL Out of Stock]** - Wenn keine Rückbestellungen aktiviert sind, verhindert, dass das Produkt zum Kauf verfügbar ist, und entfernt die Liste aus dem Katalog. |
| [!UICONTROL Qty] | Auf Lager befindliche Beträge für jede Quelle. |
| [!UICONTROL Notify Qty] | Ein Betrag für _Für Menge benachrichtigen_ für diese spezifische Quelle, wenn `Notify Quantity Use Default` nicht ausgewählt ist. |
| [!UICONTROL Notify Qty Use Default] | Gibt an, dass die Standardeinstellung für _Für Menge benachrichtigen_ in der Produktkonfiguration &quot;Erweiterter Bestand&quot;oder &quot;Global&quot;angezeigt. Weitere Informationen zu erweiterten Lagerbestandseinstellungen für Ihr Produkt finden Sie unter [Erweiterte Produktoptionen konfigurieren](../inventory-management/product-options.md). |
| [!UICONTROL Actions] | Klicken Sie für eine zugewiesene Quelle auf **[!UICONTROL Unassign]** um die Quelle für das Produkt nicht verfügbar zu machen. Klicken Sie für eine nicht zugewiesene Quelle auf **[!UICONTROL Assign Sources]** , um eine Quelle für das Produkt verfügbar zu machen. Weitere Informationen finden Sie unter [!UICONTROL Assign Sources] Optionen, siehe [Zuweisen von Quellen pro Produkt](../inventory-management/sources-assign-per-product.md). |

{style="table-layout:auto"}
