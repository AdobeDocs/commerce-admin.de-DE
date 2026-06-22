---
title: '[!DNL AR Viewer] für Adobe Commerce-Setup'
description: Erfahren Sie mehr über die Verwaltung von 3D-Modell-Assets mit  [!DNL AR Viewer]  Erweiterung für Ihre Produktlisten.
exl-id: e3f081ff-b994-4842-a1f3-613012d33a9c
TQID: https://experienceleague.adobe.com/6OlcZ4Psm3INgVm7f-Y9JvqfUdmR6Rg48tcigLAHiaE
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: ccaac3a13a346ce192a724efb3384ef2d612c980
workflow-type: tm+mt
source-wordcount: 313
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
> Eine Reihe von Demovideos eines Benutzers, in denen er ein 3D-Modell zu einem Produkt hinzufügt, finden Sie auf der Seite [AR-Viewer für Adobe Commerce](https://experienceleague.adobe.com/docs/commerce-learn/tutorials/catalog/augmented-reality.html) in _Commerce-Videos und -Tutorials_.

