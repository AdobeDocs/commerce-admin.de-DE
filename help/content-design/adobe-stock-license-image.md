---
title: Adobe Stock-Bild lizenzieren
description: Lizenzieren Sie Ihre Adobe Stock-Bilder, um sicherzustellen, dass Sie Zugriff auf das Adobe Stock-Wasserzeichen haben, und um es zu eliminieren.
exl-id: a2d6b7b8-e9ac-4f3e-bcd1-05e2bb74b6c2
feature: CMS, Media
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 0%

---

# Adobe Stock-Bild lizenzieren

Adobe Stock-Assets, die Sie für Ihre Produktions-Adobe Commerce- und Magento Open Source-Stores verwenden möchten, sollten lizenziert sein. Diese Lizenzierung stellt sicher, dass Sie rechtlichen Zugriff auf das Bild haben und das Adobe Stock-Wasserzeichen, das auf allen [Bildvorschau][save-preview]. Um Bilder zu lizenzieren oder bereits lizenzierte Bilder zu speichern, müssen Sie bei Ihrem Adobe-Konto angemeldet sein.

Die neue [[!DNL Media Gallery]](media-gallery.md) bietet eine direkte Integration mit Adobe Stock, wodurch die direkte Lizenzierung Ihrer Bilder von der Galerieseite aus erleichtert wird.

## Voraussetzungen

Diese Funktion erfordert die [Adobe Stock-Integration][adobe-stock-integration] -Modul und -Konfiguration. Lizenzierung [Adobe Stock][adobe-stock] Bilder erfordern einen bezahlten Adobe Stock-Plan und eine [Adobe-Konto][adobe-signin].

## Ein Bild vom neuen [!DNL Media Gallery]

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Führen Sie die Schritte unter [Verwenden von Adobe Stock-Bildern][using-adobe-stock] , um sich anzumelden und Vorschaubilder in der [Medienspeicher][media-storage].

   ![Gespeichertes Vorschaubild](./assets/adobe-stock-gallery-unlicensed.png){width="600" zoomable="yes"}

1. Klicken Sie auf die drei Punkte unter dem Bild (![Asset-Menüsymbol](./assets/media-gallery-asset-menu-icon.png){width="10" zoomable="no"}) und klicken Sie dann auf **[!UICONTROL License]**.

   ![Adobe Stock-Bildaktionen](./assets/adobe-stock-gallery-image-actions.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Wenn Sie nicht angemeldet sind, wird das Anmeldeformular angezeigt. Weitere Informationen zur Anmeldung finden Sie unter [Verwenden von Adobe Stock-Bildern][using-adobe-stock].

1. Klicken Sie im Dialogfeld zur Lizenzbestätigung auf **[!UICONTROL Confirm]** um das Bild zu lizenzieren.

   ![Lizenzbestätigung](./assets/adobe-stock-gallery-license-confirm.png){width="350" zoomable="yes"}

   >[!NOTE]
   >
   >Sie müssen verfügbar sein [Adobe Stock-Gutschriften][stock-credits] in Ihrem Konto, um das Bild zu lizenzieren.

## Lizenzieren eines Bildes aus dem standardmäßigen Medienspeicher

1. [Zugriff auf das Adobe Stock-Suchraster][access-search].

1. nach [Bilddetails anzeigen][view-details], klicken Sie in der Reihenfolge auf ein Bild im Suchraster.

1. Führen Sie je nach aktuellem Lizenzstatus des Bildes einen der folgenden Schritte aus:

   - Wenn das Bild bereits lizenziert ist, klicken Sie auf **[!UICONTROL Save]**.

   - Wenn das Bild _not_ lizenziert, klicken Sie auf **[!UICONTROL License and Save]**.

     >[!NOTE]
     >
     >Sie müssen verfügbar sein [Adobe Stock-Gutschriften][stock-credits] in Ihrem Konto, um das Bild zu lizenzieren.

   Durch diese Aktion werden Sie aufgefordert, einen Dateinamen anzugeben, mit dem das Bild in der [Medienspeicher][media-storage]. Es wird ein standardmäßiger Dateiname angegeben, aber Sie können den Namen Ihren Voreinstellungen anpassen.

   ![Adobe Stock-lizenziertes Bild speichern](./assets/adobe-stock-save-licensed.png){width="550" zoomable="yes"}

1. Klicken **[!UICONTROL Confirm]**.

   Die Seite wird zum Medienspeicher weitergeleitet und Ihre gespeicherte Vorschau wird angezeigt.

[adobe-stock-integration]: adobe-stock.md
[media-storage]: media-storage.md
[using-adobe-stock]: adobe-stock-manage.md
[save-preview]: adobe-stock-save-preview.md
[access-search]: adobe-stock-manage.md#access-the-adobe-stock-search-grid
[view-details]: adobe-stock-manage.md#view-image-details
[stock-credits]: https://helpx.adobe.com/stock/help/credit-packs.html
[adobe-stock]: https://stock.adobe.com
[adobe-signin]: https://helpx.adobe.com/manage-account/using/access-adobe-id-account.html
