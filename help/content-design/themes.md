---
title: Designs
description: Informationen zu [!DNL Commerce] Designs, die Layout-Dateien, Vorlagendateien, Übersetzungsdateien und Skins enthalten, die das Erscheinungsbild Ihres Stores definieren.
exl-id: d2ccff51-5019-4f80-8eaa-3fe50d5cd6cc
feature: Page Content, Themes
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 0%

---

# Designs

Ein Design ist eine Sammlung von Dateien, die die visuelle Präsentation Ihres Stores bestimmen. Bei der ersten Installation [!DNL Commerce], basieren die Designelemente des Stores auf der _Standard_ Design. Zusätzlich zum ursprünglichen Standarddesign, das mit Ihrem [!DNL Commerce] -Installation, gibt es eine Vielzahl von verfügbaren Designs, die Sie verwenden können _as is_ oder ändern Sie Ihre Anforderungen.

Ein responsives Design passt das Seitenlayout an den Ansichtsport des Geräts an. Beispiel _Luma_ Das Design hat ein flexibles, responsives Layout, das vom Desktop, Tablet oder Mobilgerät aus angezeigt werden kann.

[!DNL Commerce] Designs umfassen Layout-Dateien, Vorlagendateien, Übersetzungsdateien und Skins. Eine Skin ist eine Sammlung unterstützender CSS-, Bilder- und JavaScript-Dateien, die zusammen die visuelle Präsentation und Interaktionen erstellen, die Ihre Kunden beim Besuch Ihres Stores erleben. Designs und Skins können von einem Entwickler oder Designer angepasst werden, der das Design von Commerce-Designs versteht und Zugriff auf Ihren Server hat. Weitere Informationen finden Sie unter [_Frontend-Entwicklerhandbuch_](https://developer.adobe.com/commerce/frontend-core/guide/themes/).

![Luma-Design](./assets/design-responsive.png){width="600" zoomable="yes"}

## Standarddesign

Die `Magento Blank` responsives Design rendert die Anzeige Ihrer Storefront für verschiedene Geräte und enthält Best Practices für Desktop, Tabelle und Mobilgeräte. Einige Designs sind nur für die Verwendung mit bestimmten Geräten vorgesehen. Wann [!DNL Commerce] eine bestimmte Browser-ID oder einen Benutzeragenten erkennt, wird das für den jeweiligen Browser konfigurierte Design verwendet. Die Suchzeichenfolge kann auch mit Perl-kompatible reguläre Ausdrücke (PCRE) enthalten.

![Designs](./assets/themes.png){width="700" zoomable="yes"}

### Filtern des Themenrasters

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Themes]**.

1. Klicken **[!UICONTROL Filters]**.

1. Geben Sie einen ID-Bereich, einen Designnamen (oder Titel), einen Ordnerpfad oder ein übergeordnetes Design ein.

1. Klicks **[!UICONTROL Apply Filters]** , um die Liste der Themen zu aktualisieren.

## Aktuelle Designeinstellungen anzeigen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Themes]**.

1. Suchen Sie in der Liste der installierten Designs das Thema, das Sie untersuchen möchten, und klicken Sie auf die Zeile, um die Einstellungen anzuzeigen.

1. Um eine Beispielseite anzuzeigen, klicken Sie auf die **[!UICONTROL Theme Preview Image]**.

![Vorschau-Design](./assets/theme-settings.png){width="600" zoomable="yes"}

## Anwenden eines Standarddesigns

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Suchen Sie die Store-Ansicht, die Sie konfigurieren möchten, und klicken Sie auf **[!UICONTROL Edit]** im _[!UICONTROL Action]_Spalte.

1. under _[!UICONTROL Default Theme]_, set **[!UICONTROL Applied Theme]**zu dem Ordner hinzu, den Sie für die aktuelle Ansicht verwenden möchten.

   ![Angewandtes Design](./assets/theme-default-apply.png){width="600" zoomable="yes"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Configuration]**.

## Hinzufügen einer Benutzeragenten-Regel

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. under _[!UICONTROL Design Rule]_klicken **[!UICONTROL Add New User Agent Rule]**.

   ![Design-Regel](./assets/theme-design-rule.png){width="600" zoomable="yes"}

1. Für **[!UICONTROL Search String]** eingeben, geben Sie die Browser-ID für das jeweilige Gerät ein.

   Suchzeichenfolgen werden in der Reihenfolge ihrer Eingabe zugeordnet. Geben Sie beispielsweise für Firefox Folgendes ein:

   `/^mozilla/i`

1. Wiederholen Sie den Vorgang, um weitere Geräte aufzurufen.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Configuration]**.
