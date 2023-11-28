---
title: '[!DNL AR Viewer] für Adobe Commerce-Setup'
description: Erfahren Sie mehr über das Verwalten von 3D-Modell-Assets mithilfe des [!DNL AR Viewer] -Erweiterung für Ihre Produktlisten.
exl-id: e3f081ff-b994-4842-a1f3-613012d33a9c
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 0%

---

# Verwalten Sie Produkt-3D-Modelle mit dem [!DNL AR Viewer] für Adobe Commerce

Für jedes Produkt können Sie eine `.USDZ` -Datei, die die Verwendung von AR- und 3D-Modellen in Ihrer Produktliste ermöglicht.

Die [!DNL AR Viewer] nur unterstützt `.USDZ` -Dateien.

## Installieren der Erweiterung

[!DNL AR Viewer] wird als Erweiterung aus dem [Adobe Commerce Marketplace](https://commercemarketplace.adobe.com/magento-module-arviewer.html){target=_blank}.

Siehe [_Installationsanleitung_](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) für weitere Informationen zum Installationsprozess der Erweiterung.

Nach dem [!DNL AR Viewer] -Erweiterung installiert und konfiguriert ist, können Admin-Benutzer Produktlisten einrichten, anpassen und verwalten, um 3D-Modelle einzuschließen.

## Hinzufügen eines 3D-Modells

1. Öffnen Sie das Produkt im Bearbeitungsmodus.

1. Um mit einer bestimmten Store-Ansicht zu arbeiten, legen Sie die **[!UICONTROL Store View]** zur entsprechenden Ansicht.

   >[!NOTE]
   >
   >Neue Produkt-3D-Modelle _always_ hochgeladen und in sichtbar _all_ Store-Ansichten, auch wenn die `All Store Views` Der Umfang wird nicht für den Upload verwendet. <br/><br/>Um alle Produkt-3D-Modelle aus einer bestimmten Store-Ansicht auszublenden, müssen Sie zu dieser Store-Ansicht wechseln. Wählen Sie dazu die **[!UICONTROL Hide from Product Page]** Kontrollkästchen für das 3D-Modell aktivieren und auf **[!UICONTROL Save]**.

1. Scrollen Sie nach unten und erweitern Sie die _[!UICONTROL Product 3D Model]_Abschnitt.

   ![Menü-Popup](assets/ar-viewer-product-options.png){width="700" zoomable="yes"}

1. Hinzufügen des 3D-Modells (`.USDZ` -Datei) des Produkts.

1. Klicken **[!UICONTROL Save]**.

### Löschen eines 3D-Modells

So entfernen Sie ein 3D-Modell aus den Produktdetails:

1. Klicken **[!UICONTROL Delete]**.

1. Klicken **[!UICONTROL Save]**.

## Produkt-3D-Modelle anzeigen

Wenn die Produktdetails mit dem 3D-Modell aktualisiert werden:

1. Die [!DNL AR Viewer] generiert einen QR-Code in der Produktbeschreibung, der die AR-Datei kodiert.

1. Ein Kunde kann diesen QR-Code auf der Produktseite sehen.

1. Wenn Kunden den QR-Code mit ihren Mobilgeräten scannen, wird auf dem Mobilgerät ein AR-Erlebnis gerendert.

>[!NOTE]
>
> Eine Reihe von Demonstrationsvideos eines Benutzers, der einem Produkt ein 3D-Modell hinzufügt, finden Sie in der [AR-Viewer für Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-learn/tutorials/catalog/augmented-reality.html) Seite in _Handelsvideos und Tutorials_.
