---
title: Konfiguration des Produktbilds
description: Erfahren Sie, wie Sie eine maximale Pixelgröße (Breite und Höhe) festlegen und die Größe von Produktbilddateien beim Hochladen automatisch ändern.
exl-id: d8fce5f8-eddf-4335-9a72-24036db077db
feature: Catalog Management, Products, Media
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '710'
ht-degree: 0%

---

# Konfiguration des Produktbilds

Wenn Sie große Bilder für die Anzeige auf der _[!UICONTROL Product Details]_&#x200B;hochladen möchten, sollten Sie eine maximale Pixelgröße (Breite und Höhe) festlegen und die Größe der Dateien beim Hochladen automatisch ändern. Um diesen Typ des Produktbild-Uploads zu unterstützen, gibt es eine Option, um beim Hochladen die automatische Größenanpassung größerer Bilddateien zu aktivieren. Für Produkte, die Sie Ihrem Katalog hinzufügen möchten, für die Sie aber noch kein Bild-Asset zur Anzeige haben, können Sie ein Platzhalterbild konfigurieren.

## Ändern der Größe von Produktbildern

Beim Hochladen von Produktbildern können Sie größere Bilder mit unterschiedlichen Größen hinzufügen, um detaillierte, hochwertige Zooms auf der _[!UICONTROL Product Details]_-Seite bereitzustellen. Um sicherzustellen, dass alle Bilder eine ähnliche Größe haben und ähnlich aussehen, gibt es eine Option zur Größenanpassung, um sicherzustellen, dass alle Bilder einer bestimmten Pixelgröße entsprechen. Diese Option ändert automatisch die Größe aller Produktbilder mithilfe der Konfigurationseinstellungen. Dies kann bei der Leistung des Zooms, dem schnelleren Laden von Bildern und einem einheitlichen Erscheinungsbild der Produktbilder helfen.

>[!NOTE]
>
>Aus Gründen der Kompatibilität wird empfohlen, alle Produktbilder mit dem `sRGB` Farbprofil hochzuladen. Alle anderen Farbprofile werden beim Hochladen des Produktbilds automatisch in das `sRGB` Farbprofil konvertiert, was zu Farbinkonsistenzen im hochgeladenen Bild führen kann.

Durch Festlegen einer maximalen Pixelbreite und -höhe wird die Größe des Bildes auf die physischen Abmessungen pro Pixel geändert. Commerce ändert die Bildgröße entsprechend der größeren Breite bzw. Höhe und behält dabei die Proportionen bei. Wenn Sie die Qualität von JPG-Bildern verringern, wird auch die Dateigröße verringert.

Bei einer 3000 x 2100 Pixel großen JPG mit 100 % kann es sich beispielsweise um eine Bilddatei mit einer Größe von 5 MB oder mehr handeln. Die Größe dieses Bildes würde die Breite auf 1920 Pixel reduzieren, Proportionen und Qualität auf 80 % beibehalten, um eine viel kleinere Dateigröße mit hoher Qualität zu erzielen.

### Ändern der Bildgröße aktivieren

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Advanced]** und wählen Sie **[!UICONTROL System]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt _Konfiguration des Bild-_&quot;.

   Um die Standardeinstellungen zu ändern, deaktivieren Sie bei Bedarf das Kontrollkästchen **[!UICONTROL Use system value]** .

   ![Konfiguration des Bild-Uploads](../configuration-reference/advanced/assets/system-image-upload-configuration.png){width="600" zoomable="yes"}

   Eine detaillierte Liste dieser Konfigurationseinstellungen finden Sie unter [_Konfiguration des Bild-Uploads_](../configuration-reference/advanced/system.md#image-upload-configuration) in der _Konfigurationsreferenz_.

1. Stellen Sie zum Aktivieren sicher, dass **[!UICONTROL Enable Frontend Resize]** auf `Yes` gesetzt ist.

1. Geben Sie eine **[!UICONTROL Quality]** zwischen `1` und `100` % ein.

   Für eine reduzierte Dateigröße und eine hohe Qualität wird eine Einstellung zwischen 80-90% empfohlen.

1. Legen Sie die **[!UICONTROL Maximum Width]** für das Bild in Pixel fest.

   Wenn die Größe des Bildes geändert wird, wird diese Breite nicht überschritten, und die Proportionen bleiben erhalten.

1. Legen Sie die **[!UICONTROL Maximum Height]** für das Bild in Pixel fest.

   Wenn die Größe des Bildes geändert wird, wird diese Höhe nicht überschritten, und die Proportionen bleiben erhalten.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

### Feldbeschreibungen

| Feld | [Umfang](../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Quality] | Global | Bestimmt die JPG-Qualität für das skalierte Bild. Geringere Qualität reduziert die Dateigröße. 80-90% wird empfohlen, um die Dateigröße mit hoher Qualität zu reduzieren. Standard: 80 |
| [!UICONTROL Enable Frontend Resize] | Global | Ermöglicht es Commerce, die Größe großer, übergroßer Bilder zu ändern, die für die _[!UICONTROL Product Details]_&#x200B;hochgeladen werden können. Commerce ändert die Größe der Bilddateien mithilfe von JavaScript beim Hochladen der Datei. Wenn die Größe des Bildes geändert wird, werden die exakten Proportionen beibehalten, um die größte Größe für „Maximale Breite“ oder „Maximale Höhe“ zu erfüllen und nicht zu überschreiten. Standard: `Yes` |
| [!UICONTROL Maximum Width] | Global | Bestimmt die maximale Pixelbreite für das Bild. Wenn die Größe des Bildes geändert wird, wird diese Breite nicht überschritten. Standard: `1920` |
| [!UICONTROL Maximum Height] | Global | Bestimmt die maximale Pixelhöhe für das Bild. Wenn die Größe des Bildes geändert wird, wird diese Höhe nicht überschritten. Standard: `1200` |

{style="table-layout:auto"}

## Platzhalter für Bilder

Adobe Commerce und Magento Open Source verwenden temporäre Bilder als Platzhalter, bis die permanenten Produktbilder verfügbar werden. Für jede Rolle kann ein anderer Platzhalter hochgeladen werden. Das ursprüngliche Platzhalterbild ist ein Beispiel-Logo, das Sie durch das Bild Ihrer Wahl ersetzen können.

![Bildplatzhalter](./assets/storefront-image-placeholder.png){width="600" zoomable="yes"}

**_So laden Sie Platzhalterbilder hoch:_**

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Catalog]** und wählen Sie darunter **[!UICONTROL Catalog]**.

1. Erweitern Sie ![Erweiterungssymbol](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Product Image Placeholders]** .

   ![Platzhalter für Produktbilder](../configuration-reference/catalog/assets/catalog-product-image-placeholders.png){width="600" zoomable="yes"}

   Eine detaillierte Liste dieser Konfigurationseinstellungen finden Sie unter [_Produktbild-Platzhalter_](../configuration-reference/catalog/catalog.md#product-image-placeholders) in der _Konfigurationsreferenz_.

1. Klicken Sie für jede Bildrolle auf **[!UICONTROL Choose File]**, suchen Sie das Bild auf Ihrem Computer und laden Sie die Datei hoch.

   Sie können dasselbe Bild für alle drei Rollen verwenden oder für jede Rolle ein anderes Platzhalterbild hochladen.

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.

Informationen zu Bildrollen und empfohlenen Größen finden Sie unter [Hochladen eines Bildes](product-image.md#upload-an-image).
