---
title: Designs
description: Erfahren Sie mehr über [!DNL Commerce] Designs, darunter Layoutdateien, Vorlagendateien, Übersetzungsdateien und Skins, die das Erscheinungsbild Ihres Stores definieren.
exl-id: d2ccff51-5019-4f80-8eaa-3fe50d5cd6cc
feature: Page Content, Themes
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 0%

---

# Designs

Ein Design ist eine Sammlung von Dateien, die die visuelle Präsentation Ihres Stores bestimmen. Wenn Sie [!DNL Commerce] zum ersten Mal installieren, basieren die Designelemente des Stores auf dem Design _Standard_ . Zusätzlich zum ursprünglichen Standarddesign, das mit Ihrer [!DNL Commerce] -Installation geliefert wird, gibt es eine Vielzahl von verfügbaren Designs, die Sie _im Ist-Zustand_ verwenden oder Ihren Anforderungen entsprechend ändern können.

Ein responsives Design passt das Seitenlayout an den Ansichtsport des Geräts an. Das Muster _Luma_ hat ein flexibles, responsives Layout, das vom Desktop, Tablet oder Mobilgerät aus angezeigt werden kann.

[!DNL Commerce] Designs umfassen Layout-Dateien, Vorlagendateien, Übersetzungsdateien und Skins. Eine Skin ist eine Sammlung unterstützender CSS-, Bilder- und JavaScript-Dateien, die zusammen die visuelle Präsentation und Interaktionen erstellen, die Ihre Kunden beim Besuch Ihres Stores erleben. Designs und Skins können von einem Entwickler oder Designer angepasst werden, der mit dem Design von Commerce vertraut ist und Zugriff auf Ihren Server hat. Weitere Informationen finden Sie im [_Frontend-Entwicklerhandbuch_](https://developer.adobe.com/commerce/frontend-core/guide/themes/).

![Luma-Design](./assets/design-responsive.png){width="600" zoomable="yes"}

## Standarddesign

Das responsive Design `Magento Blank` rendert die Anzeige Ihrer Storefront für verschiedene Geräte und enthält Best Practices für Desktop-, Tabellen- und Mobilgeräte. Einige Designs sind nur für die Verwendung mit bestimmten Geräten vorgesehen. Wenn [!DNL Commerce] eine bestimmte Browser-ID oder einen Benutzeragenten erkennt, wird das für den jeweiligen Browser konfigurierte Design verwendet. Die Suchzeichenfolge kann auch mit Perl-kompatible reguläre Ausdrücke (PCRE) enthalten.

![Designs](./assets/themes.png){width="700" zoomable="yes"}

### Filtern des Themenrasters

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Themes]**.

1. Klicken Sie auf **[!UICONTROL Filters]**.

1. Geben Sie einen ID-Bereich, einen Designnamen (oder Titel), einen Ordnerpfad oder ein übergeordnetes Design ein.

1. Klicken Sie auf **[!UICONTROL Apply Filters]** , um die Liste der Designs zu aktualisieren.

## Aktuelle Designeinstellungen anzeigen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Themes]**.

1. Suchen Sie in der Liste der installierten Designs das Thema, das Sie untersuchen möchten, und klicken Sie auf die Zeile, um die Einstellungen anzuzeigen.

1. Um eine Beispielseite anzuzeigen, klicken Sie auf &quot;**[!UICONTROL Theme Preview Image]**&quot;.

![Design-Vorschau anzeigen](./assets/theme-settings.png){width="600" zoomable="yes"}

## Anwenden eines Standarddesigns

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Suchen Sie die Store-Ansicht, die Sie konfigurieren möchten, und klicken Sie in der Spalte _[!UICONTROL Action]_auf **[!UICONTROL Edit]**.

1. Legen Sie unter _[!UICONTROL Default Theme]_**[!UICONTROL Applied Theme]**den Wert fest, den Sie für die aktuelle Ansicht verwenden möchten.

   ![Angewandtes Design](./assets/theme-default-apply.png){width="600" zoomable="yes"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Configuration]**.

## Hinzufügen einer Benutzeragenten-Regel

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Klicken Sie unter _[!UICONTROL Design Rule]_auf **[!UICONTROL Add New User Agent Rule]**.

   ![Designregel](./assets/theme-design-rule.png){width="600" zoomable="yes"}

1. Geben Sie für &quot;**[!UICONTROL Search String]**&quot;die Browser-ID für das jeweilige Gerät ein.

   Suchzeichenfolgen werden in der Reihenfolge ihrer Eingabe zugeordnet. Geben Sie beispielsweise für Firefox Folgendes ein:

   `/^mozilla/i`

1. Wiederholen Sie den Vorgang, um weitere Geräte aufzurufen.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Configuration]**.
