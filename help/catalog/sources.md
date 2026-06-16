---
title: Produkteinstellungen - [!UICONTROL Sources]
description: Für ein Produkt bieten die [!UICONTROL Sources] Zugriff auf die  [!DNL Inventory Management] , aus denen das Produkt verteilt werden kann.
exl-id: 986f6031-0edc-4105-aa02-1c22364b3e7c
feature: Catalog Management, Products, Inventory
TQID: https://experienceleague.adobe.com/7LFF4ufXyKtJwUp4DiNDdnRMhFRsM1tX8Z2TlPt1Kso
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: c18ed297-2187-4aec-affb-9d9654eca6fcid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 259
ht-degree: 0%

---

# Produkteinstellungen - [!UICONTROL Sources]

Im Abschnitt _[!UICONTROL Sources]_der Produkteinstellungen werden die Quellen aufgelistet, aus denen das Produkt verteilt werden kann. Es wird verwendet, um Quellen zuzuweisen und deren Zuweisung aufzuheben sowie die Menge und Verfügbarkeit des Produkts zu verwalten. Dieser Abschnitt wird nur angezeigt, wenn für Ihren Store mehr als eine Quelle definiert ist. Weitere Informationen zu Quellen finden Sie unter [Verwalten von Quellen](../inventory-management/sources-manage.md).

## Zuweisen einer Quelle für ein Produkt

1. Klicken Sie auf **[!UICONTROL Assign Source]**.

1. Aktivieren Sie das Kontrollkästchen für die erforderlichen Quellen.

1. Klicken Sie auf **[!UICONTROL Done]**.

1. Wählen Sie **[!UICONTROL Source Item Status]** aus und geben Sie die **[!UICONTROL Qty]** und **[!UICONTROL Notify Qty]** Werte nach Bedarf ein.

1. Klicken Sie auf **[!UICONTROL Save]** , um die Änderungen zu speichern.

![Quellansicht](./assets/catalog-sources-list.png){width="600" zoomable="yes"}

## Feldverweis

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Name] | Der eindeutige Name für eine Quelle. |
| [!UICONTROL Source Status] | Bestimmt, ob das Produkt im Katalog aktiviert oder deaktiviert ist. |
| [!UICONTROL Source Item Status] | Legt die aktuelle Verfügbarkeit des Produkts fest. Optionen: <br />**[!UICONTROL In Stock]**- Macht das Produkt zum Kauf verfügbar.<br />**[!UICONTROL Out of Stock]** - Sofern keine Auftragsrückstände aktiviert sind, verhindert, dass das Produkt zum Kauf zur Verfügung steht, und entfernt die Auflistung aus dem Katalog. |
| [!UICONTROL Qty] | Verfügbare Lagerbestände für jede Quelle. |
| [!UICONTROL Notify Qty] | Ein Betrag für die _Mengenbenachrichtigung_ für diese spezifische Quelle, wenn `Notify Quantity Use Default` nicht ausgewählt ist. |
| [!UICONTROL Notify Qty Use Default] | Gibt an, dass die Standardeinstellung für _Für Menge benachrichtigen_ im erweiterten Warenbestand oder die globale Einstellung in der Store-Konfiguration verwendet werden soll. Weitere Informationen zu erweiterten Inventareinstellungen für Ihr Produkt finden Sie unter [Konfigurieren erweiterter Produktoptionen](../inventory-management/product-options.md). |
| [!UICONTROL Actions] | Klicken Sie für eine zugewiesene Quelle auf **[!UICONTROL Unassign]** , damit die Quelle nicht für das Produkt verfügbar ist. Klicken Sie bei einer nicht zugewiesenen Quelle auf **[!UICONTROL Assign Sources]** , um eine Quelle für das Produkt verfügbar zu machen. Weitere Informationen zu [!UICONTROL Assign Sources] Optionen finden Sie unter [Zuweisen von Quellen pro Produkt](../inventory-management/sources-assign-per-product.md). |

{style="table-layout:auto"}
