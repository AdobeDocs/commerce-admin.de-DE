---
title: '[!DNL AR Viewer] für Adobe Commerce-Setup'
description: Erfahren Sie mehr über das Verwalten von 3D-Modell-Assets mit der Erweiterung [!DNL AR Viewer] für Ihre Produktlisten.
exl-id: e3f081ff-b994-4842-a1f3-613012d33a9c
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---

# Verwalten von Produkt-3D-Modellen mit dem [!DNL AR Viewer] für Adobe Commerce

Sie können für jedes Produkt eine `.USDZ` -Datei hochladen, die die Verwendung von AR- und 3D-Modellen in Ihrer Produktliste ermöglicht.

Der [!DNL AR Viewer] unterstützt nur `.USDZ` -Dateien.

## Installieren der Erweiterung

[!DNL AR Viewer] wird als Erweiterung vom [Adobe Commerce Marketplace](https://commercemarketplace.adobe.com/magento-module-arviewer.html){target=_blank} installiert.

Weitere Informationen zur Installation der Erweiterung finden Sie im [_Installationshandbuch_](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) .

Nachdem die Erweiterung [!DNL AR Viewer] installiert und konfiguriert wurde, können Admin-Benutzer Produktlisten einrichten, anpassen und verwalten, um 3D-Modelle einzuschließen.

## Hinzufügen eines 3D-Modells

1. Öffnen Sie das Produkt im Bearbeitungsmodus.

1. Um mit einer bestimmten Store-Ansicht zu arbeiten, legen Sie die Auswahl **[!UICONTROL Store View]** auf die entsprechende Ansicht fest.

   >[!NOTE]
   >
   >Neue Produkt-3D-Modelle werden _immer_ hochgeladen und in _allen_ Store-Ansichten angezeigt, selbst wenn der Bereich `All Store Views` nicht für den Upload verwendet wird. <br/><br/>Um alle Produkt-3D-Modelle aus einer bestimmten Store-Ansicht auszublenden, müssen Sie zu dieser Store-Ansicht wechseln, das Kontrollkästchen **[!UICONTROL Hide from Product Page]** für das 3D-Modell aktivieren und auf **[!UICONTROL Save]** klicken.

1. Scrollen Sie nach unten und erweitern Sie den Abschnitt _[!UICONTROL Product 3D Model]_.

   ![Menü-Popup](assets/ar-viewer-product-options.png){width="700" zoomable="yes"}

1. Fügen Sie das 3D-Modell (`.USDZ` -Datei) des Produkts hinzu.

1. Klicken Sie auf **[!UICONTROL Save]**.

### Löschen eines 3D-Modells

So entfernen Sie ein 3D-Modell aus den Produktdetails:

1. Klicken Sie auf **[!UICONTROL Delete]**.

1. Klicken Sie auf **[!UICONTROL Save]**.

## Produkt-3D-Modelle anzeigen

Wenn die Produktdetails mit dem 3D-Modell aktualisiert werden:

1. Der [!DNL AR Viewer] generiert einen QR-Code in der Produktbeschreibung, der die AR-Datei kodiert.

1. Ein Kunde kann diesen QR-Code auf der Produktseite sehen.

1. Wenn Kunden den QR-Code mit ihren Mobilgeräten scannen, wird auf dem Mobilgerät ein AR-Erlebnis gerendert.

>[!NOTE]
>
> Eine Reihe von Demonstrationsvideos eines Benutzers, der einem Produkt ein 3D-Modell hinzufügt, finden Sie auf der Seite [AR Viewer für Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-learn/tutorials/catalog/augmented-reality.html) in _Videos und Tutorials_ von Commerce.
