---
title: '[!DNL AR Viewer] für Adobe Commerce-Setup'
description: Erfahren Sie mehr über die Verwaltung von 3D-Modell-Assets mit  [!DNL AR Viewer]  Erweiterung für Ihre Produktlisten.
exl-id: e3f081ff-b994-4842-a1f3-613012d33a9c
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---

# Verwalten von Produkt-3D-Modellen mit dem [!DNL AR Viewer] für Adobe Commerce

Für jedes Produkt können Sie eine `.USDZ` hochladen, mit der AR- und 3D-Modelle in Ihrer Produktliste verwendet werden können.

Der [!DNL AR Viewer] unterstützt nur `.USDZ`.

## Installieren der Erweiterung

[!DNL AR Viewer] wird als Erweiterung vom [Adobe Commerce Marketplace](https://commercemarketplace.adobe.com/magento-module-arviewer.html){target=_blank} installiert.

Weitere Informationen [_Installationsvorgang von Erweiterungen finden_](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) im „Installationshandbuch“.

Nachdem die [!DNL AR Viewer]-Erweiterung installiert und konfiguriert wurde, können Admin-Benutzer Produktlisten einrichten, anpassen und verwalten, um 3D-Modelle einzuschließen.

## Hinzufügen eines 3D-Modells

1. Öffnen Sie das Produkt im Bearbeitungsmodus.

1. Um mit einer bestimmten Store-Ansicht zu arbeiten, legen Sie die **[!UICONTROL Store View]** auf die entsprechende Ansicht fest.

   >[!NOTE]
   >
   >Neue 3D-Produktmodelle werden _immer_ hochgeladen und in _allen_ Store-Ansichten angezeigt, auch wenn der `All Store Views` nicht zum Hochladen verwendet wird. <br/><br/>Um 3D-Produktmodelle aus einer bestimmten Store-Ansicht auszublenden, müssen Sie zu dieser Store-Ansicht wechseln, das Kontrollkästchen **[!UICONTROL Hide from Product Page]** für das 3D-Modell aktivieren und auf **[!UICONTROL Save]** klicken.

1. Scrollen Sie nach unten und erweitern Sie den Abschnitt _[!UICONTROL Product 3D Model]_.

   ![Menü-Popup](assets/ar-viewer-product-options.png){width="700" zoomable="yes"}

1. Fügen Sie das 3D-Modell (`.USDZ`) des Produkts hinzu.

1. Klicken Sie auf **[!UICONTROL Save]**.

### Löschen eines 3D-Modells

So entfernen Sie ein 3D-Modell aus den Produktdetails:

1. Klicken Sie auf **[!UICONTROL Delete]**.

1. Klicken Sie auf **[!UICONTROL Save]**.

## Produkt-3D-Modelle anzeigen

Wenn die Produktdetails mit dem 3D-Modell aktualisiert werden:

1. Der [!DNL AR Viewer] generiert einen QR-Code in der Produktbeschreibung, der die AR-Datei kodiert.

1. Ein Kunde kann diesen QR-Code auf der Produktseite sehen.

1. Wenn Kunden den QR-Code mit ihren Mobilgeräten scannen, wird ein AR-Erlebnis auf dem Mobilgerät gerendert.

>[!NOTE]
>
> Eine Reihe von Demovideos, in denen gezeigt wird, wie Benutzende einem Produkt ein 3D-Modell hinzufügen, finden Sie auf der Seite [AR-Viewer für Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-learn/tutorials/catalog/augmented-reality.html) in _Commerce-Videos und -Tutorials_.
