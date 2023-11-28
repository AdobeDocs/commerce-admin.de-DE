---
title: '[!DNL Page Builder] setup'
description: Informationen zu [!DNL Page Builder] Funktionskonfiguration in Admin für Adobe Commerce und Magento Open Source.
exl-id: 48396045-0fef-4f4f-8138-e6d969560e42
feature: Page Builder, Configuration
source-git-commit: 2299beb6c11af801076d3aff0b026d41b9dbd212
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 0%

---

# [!DNL Page Builder] Setup

Wenn in der Konfiguration aktiviert, [!DNL Page Builder] ist das Standard-Tool zur Inhaltserstellung für CMS-Seiten, -Blöcke und dynamische Blöcke. Darüber hinaus wird die _[!UICONTROL Enable Advanced CMS]_Schaltflächenangebote [!DNL Page Builder] als Option für Kategorien und Produkte. Sie können auch die Standardeinstellung [Seitenlayout](../content-design/page-layout.md) die Sie für Produkte, Kategorien und CMS-Seiten verwenden möchten. [!DNL Page Builder] ist nicht für Newsletterinhalte verfügbar, die WYSIWYG verwenden [editor](../content-design/editor.md).

>[!NOTE]
>
>Wenn installiert, [!DNL Page Builder] überschreibt die Standardeinstellung für [!UICONTROL Mask for Meta Description] Konfigurationsfeld. Der Wert ändert sich von `{{name}} {{description}}` nach `{{name}}`.
><br>
>Sie können auf diese Einstellung zugreifen, wenn Sie [!UICONTROL Stores] > _[!UICONTROL Settings]_> [!UICONTROL Configuration], erweitern [!UICONTROL Catalog]und wählen Sie [!UICONTROL Catalog] darunter. Die [!UICONTROL Mask for Meta Description] im Feld [!UICONTROL Product Fields Auto-generation] Abschnitt.

>[!NOTE]
>
>Ein Admin-Benutzer muss [!UICONTROL Content] Berechtigungen für die [Rollenumfang](../systems/permissions-user-roles.md) anzeigen [!UICONTROL Edit with Page Builder] -Schaltflächen und können den Seitenaufbau verwenden.

Weitere Informationen zu den Konfigurationsoptionen für erweiterte Content Management-Tools finden Sie in der [_Konfigurationshandbuch_](../configuration-reference/general/content-management.md).

## Konfigurieren [!DNL Page Builder]

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Im linken Bereich unter _[!UICONTROL General]_auswählen **[!UICONTROL Content Management]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]** und überprüfen Sie, dass **[!UICONTROL Enable Page Builder]** auf `Yes`.

   ![Erweiterte Inhaltswerkzeuge](../configuration-reference/general/assets/content-management-advanced-content-tools.png){width="600" zoomable="yes"}

1. Wenn Sie bereit sind, [!DNL Google Maps]führen Sie folgende Schritte aus:

   - Folgen Sie bei Bedarf dem [API-Schlüssel abrufen][1] -Anweisungen und kopieren Sie dann Ihre **[!UICONTROL Google Maps API Key]**.

   - So ändern Sie die **[!UICONTROL Google Maps Style]**, fügen Sie den JSON-Code ein, der von der [[!DNL Google Maps] API-Stilassistent][2].

   >[!NOTE]
   >
   >Siehe [Media - Map](map.md) Weitere Informationen zur Verwendung von [!DNL Google Maps] in [!DNL Page Builder] Inhalt.

1. So konfigurieren Sie die Anzahl der Richtlinien in der [!DNL Page Builder] -Spalten-Raster verwenden, gehen Sie wie folgt vor:

   - Für **[!UICONTROL Default Column Grid Size]**, geben Sie die Standardanzahl der Spalten an, die im Raster angezeigt werden sollen.

   - Für **[!UICONTROL Maximum Column Grid Size]** Geben Sie die größte Anzahl von Spalten ein, die im Raster verfügbar sein sollen.

   >[!NOTE]
   >
   >Siehe [Layout - Spalte](column.md) Weitere Informationen zur Verwendung des Spaltenrasters beim Arbeiten mit Ihrer [!DNL Page Builder] Inhalt.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

## Standardlayouts konfigurieren

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Im linken Bereich unter _[!UICONTROL General]_auswählen **[!UICONTROL Web]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) **[!UICONTROL Default Layouts]** und gehen Sie wie folgt vor:

   ![Standardlayouts](../configuration-reference/general/assets/web-default-layouts.png){width="600" zoomable="yes"}

   Weitere Informationen zu den Web-Konfigurationsoptionen finden Sie unter [_Konfigurationshandbuch_](../configuration-reference/general/web.md#default-layouts).

   - Wählen Sie die **[!UICONTROL Default Product Layout]** die Sie für Produktseiten verwenden möchten.

   - Wählen Sie die **[!UICONTROL Default Category Layout]** die Sie für Kategorieseiten verwenden möchten.

   - Wählen Sie die **[!UICONTROL Default Page Layout]** die Sie für CMS-Seiten verwenden möchten.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

## Deaktivieren [!DNL Page Builder]

>[!NOTE]
>
>Deaktivieren [!DNL Page Builder] ersetzt die erweiterten Content-Tools durch WYSIWYG [editor](../content-design/editor.md)und kann Anzeigefehler in der Storefront verursachen. Inhalte, die Sie zuvor mit [!DNL Page Builder] kann möglicherweise nicht vom Administrator bearbeitet werden.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Im linken Bereich unter _[!UICONTROL General]_auswählen **[!UICONTROL Content Management]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]** und **[!UICONTROL Enable Page Builder]** nach `No`.

1. Klicken Sie bei Aufforderung zur Bestätigung auf **[!UICONTROL Turn Off]**.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

1. Bei Aufforderung [Aktualisieren](../systems/cache-management.md) ungültiger Cache.

[1]: https://developers.google.com/maps/documentation/javascript/get-api-key
[2]: https://mapstyle.withgoogle.com/
