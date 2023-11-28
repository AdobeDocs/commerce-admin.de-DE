---
title: Produkteinstellungen - [!UICONTROL Product Reviews]
description: Bei einem Produkt muss die Variable [!UICONTROL Product Reviews] -Einstellungen bieten Zugriff auf eingereichte Prüfungen für das Produkt und bearbeiten den Status für ausstehende Überprüfungen.
exl-id: 9328c9f5-dcd4-4837-8902-39dc48cb8151
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# Produkteinstellungen - [!UICONTROL Product Reviews]

Die _[!UICONTROL Product Reviews]_enthält alle Bewertungen, die Kunden zum Produkt eingereicht haben. Dieser Abschnitt wird zusammen mit den anderen Produktinformationen erst angezeigt, nachdem ein neues Produkt zum ersten Mal gespeichert wurde. Weitere Informationen finden Sie unter [Produktüberprüfungen](../merchandising-promotions/product-reviews.md).

![Produktüberprüfungen](./assets/product-review.png){width="600" zoomable="yes"}

## Feldreferenz

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL ID] | Eindeutige, numerische ID, die für den Produktüberprüfungseintrag generiert wurde |
| [!UICONTROL Created] | Datum der Veröffentlichung der Überprüfung |
| [!UICONTROL Status] | Überprüfungsstatus (`Pending`, `Approved`oder `Not Approved`) |
| [!UICONTROL Title] | Prüfungstitel |
| [!UICONTROL Nickname] | Der Nachname des Benutzers, der den Review verlassen hat |
| [!UICONTROL Review] | Kundenübersicht zum aktuellen Produkt |
| [!UICONTROL Visibility] | Sichtbarkeit bei Store-Überprüfungen |
| [!UICONTROL Type] | Typ des Benutzers, der den Review verlassen hat (`Guest` oder `Customer`) |
| [!UICONTROL Product] | Überarbeiteter Produktname |
| [!UICONTROL SKU] | Die eindeutige Lagereinheit, die dem Produkt zugewiesen ist |
| [!UICONTROL Action] | Öffnet das Produkt im Bearbeitungsmodus |

{style="table-layout:auto"}

## Moderieren von Bewertungen für ein bestimmtes Produkt

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Suchen Sie das Produkt und öffnen Sie es im Bearbeitungsmodus.

1. Scrollen Sie zum _[!UICONTROL Product Reviews]_Abschnitt.

1. Klicks **[!UICONTROL Edit]** für eine Produktüberprüfung mit `Pending` -Status, um die Details anzuzeigen und zu bearbeiten.

1. Status für Überprüfung festlegen:

   - Um eine ausstehende Überprüfung zu genehmigen, wählen Sie `Approved`.
   - Um eine Überprüfung abzulehnen, wählen Sie `Not Approved`.
   - Sie können den Prüfungsstatus wieder in `Pending` jederzeit verfügbar sein.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Review]**.

Überprüfungen mit der `Pending` und `Not Approved` -Status werden nicht in der Storefront angezeigt.
