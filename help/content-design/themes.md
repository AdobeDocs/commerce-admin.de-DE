---
title: Designs
description: Erfahren Sie mehr über  [!DNL Commerce] -Designs, darunter Layout-Dateien, Vorlagendateien, Übersetzungsdateien und Designs, die das Erscheinungsbild Ihres Stores definieren.
exl-id: d2ccff51-5019-4f80-8eaa-3fe50d5cd6cc
feature: Page Content, Themes
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 0%

---

# Designs

Ein Design ist eine Sammlung von Dateien, die die visuelle Darstellung Ihres Stores bestimmt. Bei der ersten Installation von [!DNL Commerce] basieren die Designelemente des Stores auf dem Design _Standard_. Zusätzlich zum anfänglichen Standarddesign, das mit Ihrer [!DNL Commerce]-Installation geliefert wird, gibt es eine Vielzahl von verfügbaren Designs, die Sie _wie sie sind_ verwenden oder für Ihre Anforderungen ändern können.

Ein responsives Design passt das Seiten-Layout an den Ansichtsanschluss des Geräts an. Das Beispiel _Design „Luma_ verfügt über ein flexibles, responsives Layout, das auf dem Desktop, Tablet oder Mobilgerät angezeigt werden kann.

Zu [!DNL Commerce] Designs gehören Layout-Dateien, Vorlagendateien, Übersetzungsdateien und Designs. Ein Design ist eine Sammlung unterstützender CSS-, Bild- und JavaScript-Dateien, die zusammen die visuelle Präsentation und die Interaktionen erstellen, die Ihren Kundinnen und Kunden beim Besuch Ihres Geschäfts angezeigt werden. Designs und Designs können von einem Entwickler oder Designprofi geändert und angepasst werden, der mit dem Design von Commerce vertraut ist und Zugriff auf Ihren Server hat. Weitere Informationen finden Sie im [_Frontend-Entwicklerhandbuch_](https://developer.adobe.com/commerce/frontend-core/guide/themes/).

![Luma-Design](./assets/design-responsive.png){width="600" zoomable="yes"}

## Das Standarddesign

Das `Magento Blank` responsive Design rendert die Anzeige Ihrer Storefront für verschiedene Geräte und beinhaltet Best Practices für Desktop-, Tabellen- und Mobilgeräte. Einige Designs sind nur für die Verwendung mit bestimmten Geräten konzipiert. Wenn [!DNL Commerce] eine bestimmte Browser-ID oder einen Benutzeragenten erkennt, verwendet es das Design, das für den jeweiligen Browser konfiguriert ist. Die Suchzeichenfolge kann auch Perl-kompatible reguläre Ausdrücke (PCRE) enthalten.

![Designs](./assets/themes.png){width="700" zoomable="yes"}

### Filtern des Design-Rasters

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Themes]**.

1. Klicken Sie auf **[!UICONTROL Filters]**.

1. Geben Sie einen ID-Bereich, einen Design-Namen (oder Titel), einen Ordnerpfad oder ein übergeordnetes Design ein.

1. Klicken Sie auf **[!UICONTROL Apply Filters]** , um die Liste der Designs zu aktualisieren.

## Aktuelle Design-Einstellungen anzeigen

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Themes]**.

1. Suchen Sie in der Liste der installierten Designs das Design, das Sie untersuchen möchten, und klicken Sie auf die Zeile, um die Einstellungen anzuzeigen.

1. Um eine Beispielseite anzuzeigen, klicken Sie auf die **[!UICONTROL Theme Preview Image]**.

![Design in der Vorschau](./assets/theme-settings.png){width="600" zoomable="yes"}

## Anwenden eines Standarddesigns

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Suchen Sie die Store-Ansicht, die Sie konfigurieren möchten, und klicken Sie in der Spalte _[!UICONTROL Action]_&#x200B;auf **[!UICONTROL Edit]**.

1. Legen Sie unter _[!UICONTROL Default Theme]_&#x200B;**[!UICONTROL Applied Theme]**&#x200B;auf den Wert fest, den Sie für die aktuelle Ansicht verwenden möchten.

   ![Angewendetes Design](./assets/theme-default-apply.png){width="600" zoomable="yes"}

1. Klicken Sie abschließend auf **[!UICONTROL Save Configuration]**.

## Hinzufügen einer Benutzeragenten-Regel

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Klicken Sie unter _[!UICONTROL Design Rule]_&#x200B;auf **[!UICONTROL Add New User Agent Rule]**.

   ![Regel entwerfen](./assets/theme-design-rule.png){width="600" zoomable="yes"}

1. Geben Sie **[!UICONTROL Search String]** die Browser-ID für das jeweilige Gerät ein.

   Suchzeichenfolgen werden in der Reihenfolge abgeglichen, in der sie eingegeben werden. Geben Sie beispielsweise für Firefox Folgendes ein:

   `/^mozilla/i`

1. Um weitere Geräte einzugeben, wiederholen Sie den Vorgang.

1. Klicken Sie abschließend auf **[!UICONTROL Save Configuration]**.
