---
title: Produktbildkonfiguration
description: Erfahren Sie, wie Sie beim Hochladen eine maximale Pixelgröße (Breite und Höhe) festlegen und die Größe der Produktbilddateien automatisch ändern.
exl-id: d8fce5f8-eddf-4335-9a72-24036db077db
feature: Catalog Management, Products, Media
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 0%

---

# Produktbildkonfiguration

Wenn Sie große Bilder für die Anzeige auf der _[!UICONTROL Product Details]_-Seite können Sie erwägen, eine maximale Pixelgröße (Breite und Höhe) festzulegen und die Größe der Dateien beim Hochladen automatisch zu ändern. Um diesen Typ von Produktbild-Upload zu unterstützen, gibt es eine Option, um die automatische Größenanpassung größerer Bilddateien beim Hochladen zu aktivieren. Für Produkte, die Sie zum Katalog hinzufügen möchten, aber noch kein Bild-Asset zur Anzeige haben, können Sie ein Platzhalterbild konfigurieren.

## Größe des Produktbilds ändern

Beim Hochladen von Produktbildern können Sie größere Bilder mit unterschiedlichen Größen hinzufügen, um detaillierte, hochwertige Zoomfunktionen für die _[!UICONTROL Product Details]_Seite. Um sicherzustellen, dass alle Bilder eine ähnliche Größe und einen ähnlichen Look haben, gibt es eine Option zur Größenanpassung des Bildes, um sicherzustellen, dass alle Bilder einer bestimmten Pixelgröße entsprechen. Diese Option passt die Größe aller Produktbilder mithilfe der Konfigurationseinstellungen automatisch an. Dies kann bei der Zoom-Leistung, beim schnelleren Laden von Bildern und beim einheitlichen Erscheinungsbild der Produktbilder hilfreich sein.

>[!NOTE]
>
>Für eine optimale Kompatibilität wird empfohlen, alle Produktbilder mit dem `sRGB` Farbprofil. Alle anderen Farbprofile werden automatisch in die `sRGB` Farbprofil während des Produktbild-Uploads, was zu Farbinkonsistenzen im hochgeladenen Bild führen kann.

Durch Festlegen einer maximalen Pixelbreite und -höhe wird die Größe des Bildes auf die physischen Abmessungen nach Pixel geändert. Durch Commerce wird die Größe des Bildes entsprechend der höheren Breite oder Höhe angepasst, wobei die Proportionen beibehalten werden. Durch die Reduzierung der Qualitätsmenge für JPG-Bilder wird die Dateigröße reduziert.

Eine JPG mit 3000 x 2100 Pixel bei 100 % kann beispielsweise eine Bilddatei mit 5 MB oder mehr sein. Wenn Sie die Größe dieses Bildes ändern, wird die Breite auf 1920 Pixel reduziert, wobei die Proportionen und die Qualität auf 80 % gehalten werden, um eine wesentlich kleinere Dateigröße mit hoher Qualität zu erzielen.

### Bildgröße aktivieren

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Advanced]** und wählen **[!UICONTROL System]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die _Konfiguration zum Hochladen von Bildern_ Abschnitt.

   Um die Standardeinstellungen zu ändern, deaktivieren Sie die Option **[!UICONTROL Use system value]** bei Bedarf.

   ![Konfiguration zum Hochladen von Bildern](../configuration-reference/advanced/assets/system-image-upload-configuration.png){width="600" zoomable="yes"}

   Eine detaillierte Liste dieser Konfigurationseinstellungen finden Sie unter [_Konfiguration zum Hochladen von Bildern_](../configuration-reference/advanced/system.md#image-upload-configuration) im _Konfigurationsreferenz_.

1. Stellen Sie zum Aktivieren sicher, dass **[!UICONTROL Enable Frontend Resize]** auf `Yes`.

1. Geben Sie einen **[!UICONTROL Quality]** Einstellung zwischen `1` und `100`%.

   Eine Einstellung zwischen 80 und 90 % wird für eine reduzierte Dateigröße und hohe Qualität empfohlen.

1. Legen Sie die **[!UICONTROL Maximum Width]** in Pixel für das Bild.

   Wenn die Größe des Bildes geändert wird, überschreitet es diese Breite nicht und behält Proportionen bei.

1. Legen Sie die **[!UICONTROL Maximum Height]** in Pixel für das Bild.

   Wenn die Größe des Bildes geändert wird, überschreitet es diese Höhe nicht und behält Proportionen bei.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

### Feldbeschreibungen

| Feld | [Anwendungsbereich](../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Quality] | Global | Bestimmt die JPG-Qualität für das in der Größe angepasste Bild. Eine niedrigere Qualität verringert die Dateigröße. 80-90 % werden empfohlen, um die Dateigröße bei hoher Qualität zu reduzieren. Standard: 80 |
| [!UICONTROL Enable Frontend Resize] | Global | Ermöglicht es Commerce, die Größe großer, übergroßer Bilder zu ändern, die Sie für die _[!UICONTROL Product Details]_Seite. Commerce ändert die Größe der Bilddateien beim Hochladen der Datei mit JavaScript. Wenn die Größe des Bildes geändert wird, behält es die genauen Proportionen bei, um die größte Größe für &quot;Maximale Breite&quot;oder &quot;Maximale Höhe&quot;zu erreichen und nicht zu überschreiten. Standard: `Yes` |
| [!UICONTROL Maximum Width] | Global | Legt die maximale Pixelbreite für das Bild fest. Wenn die Größe des Bildes geändert wird, überschreitet es diese Breite nicht. Standard: `1920` |
| [!UICONTROL Maximum Height] | Global | Legt die maximale Pixelhöhe für das Bild fest. Wenn die Größe des Bildes geändert wird, überschreitet es diese Höhe nicht. Standard: `1200` |

{style="table-layout:auto"}

## Bild-Platzhalter

Adobe Commerce und Magento Open Source verwenden temporäre Bilder als Platzhalter, bis die permanenten Produktbilder verfügbar sind. Für jede Rolle kann ein anderer Platzhalter hochgeladen werden. Das anfängliche Platzhalterbild ist ein Beispiellogo, das Sie durch das Bild Ihrer Wahl ersetzen können.

![Bild-Platzhalter](./assets/storefront-image-placeholder.png){width="600" zoomable="yes"}

**_Hochladen von Platzhalterbildern:_**

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Catalog]** und wählen **[!UICONTROL Catalog]** darunter.

1. Erweitern ![Erweiterungssymbol](../assets/icon-display-expand.png) die **[!UICONTROL Product Image Placeholders]** Abschnitt.

   ![Produkt-Bild-Platzhalter](../configuration-reference/catalog/assets/catalog-product-image-placeholders.png){width="600" zoomable="yes"}

   Eine detaillierte Liste dieser Konfigurationseinstellungen finden Sie unter [_Produkt-Bild-Platzhalter_](../configuration-reference/catalog/catalog.md#product-image-placeholders) im _Konfigurationsreferenz_.

1. Klicken Sie für jede Bildrolle auf **[!UICONTROL Choose File]**, suchen Sie das Bild auf Ihrem Computer und laden Sie die Datei hoch.

   Sie können dasselbe Bild für alle drei Rollen verwenden oder für jede Rolle ein anderes Platzhalterbild hochladen.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]**.

Informationen zu Bildrollen und empfohlenen Größen finden Sie unter [Bild hochladen](product-image.md#upload-an-image).
