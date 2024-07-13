---
title: '[!DNL Page Builder] setup'
description: Erfahren Sie mehr über die Konfiguration von [!DNL Page Builder] Funktionen in Admin für Adobe Commerce und Magento Open Source.
exl-id: 48396045-0fef-4f4f-8138-e6d969560e42
feature: Page Builder, Configuration
source-git-commit: 2299beb6c11af801076d3aff0b026d41b9dbd212
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# [!DNL Page Builder] Setup

Wenn in der Konfiguration aktiviert, ist [!DNL Page Builder] das standardmäßige Tool zur Inhaltserstellung für CMS-Seiten, -Blöcke und dynamische Blöcke. Darüber hinaus bietet die Schaltfläche _[!UICONTROL Enable Advanced CMS]_[!DNL Page Builder] als Option für Kategorien und Produkte. Sie können auch das standardmäßige [Seitenlayout](../content-design/page-layout.md) auswählen, das Sie für Produkte, Kategorien und CMS-Seiten verwenden möchten. [!DNL Page Builder] ist nicht für Newsletterinhalte verfügbar, die den WYSIWYG [editor](../content-design/editor.md) verwenden.

>[!NOTE]
>
>Bei der Installation überschreibt [!DNL Page Builder] die Standardeinstellung für das Konfigurationsfeld [!UICONTROL Mask for Meta Description]. Der Wert wird von `{{name}} {{description}}` in `{{name}}` geändert.
><br>
>Sie können auf diese Einstellung zugreifen, wenn Sie &quot;[!UICONTROL Stores]&quot;> &quot;_[!UICONTROL Settings]_&quot;> &quot;[!UICONTROL Configuration]&quot;, &quot;[!UICONTROL Catalog]&quot;erweitern und &quot;[!UICONTROL Catalog]&quot;darunter auswählen. Das Feld [!UICONTROL Mask for Meta Description] befindet sich im Abschnitt [!UICONTROL Product Fields Auto-generation] .

>[!NOTE]
>
>Ein Admin-Benutzer muss über [!UICONTROL Content] -Berechtigungen für seinen [Rollenbereich](../systems/permissions-user-roles.md) verfügen, um die [!UICONTROL Edit with Page Builder] -Schaltflächen anzuzeigen und den Seitenaufbau verwenden zu können.

Weitere Informationen zu den Konfigurationsoptionen für die erweiterten Werkzeuge für Content Management finden Sie im [_Konfigurationshandbuch_](../configuration-reference/general/content-management.md).

## Konfigurieren von [!DNL Page Builder]

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wählen Sie im linken Bereich unter _[!UICONTROL General]_die Option **[!UICONTROL Content Management]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]** und überprüfen Sie, ob **[!UICONTROL Enable Page Builder]** auf `Yes` eingestellt ist.

   ![Erweiterte Content-Tools](../configuration-reference/general/assets/content-management-advanced-content-tools.png){width="600" zoomable="yes"}

1. Wenn Sie bereit sind, [!DNL Google Maps] einzurichten, gehen Sie wie folgt vor:

   - Folgen Sie bei Bedarf den Anweisungen [API-Schlüssel abrufen][1] , kopieren Sie dann Ihren **[!UICONTROL Google Maps API Key]** und fügen Sie ihn ein.

   - Fügen Sie zum Ändern von **[!UICONTROL Google Maps Style]** den JSON-Code ein, der vom [[!DNL Google Maps] APIs-Stilassistenten][2] generiert wird.

   >[!NOTE]
   >
   >Weitere Informationen zur Verwendung von [!DNL Google Maps] in Ihrem [!DNL Page Builder]-Inhalt finden Sie unter [Medien - Zuordnung](map.md) .

1. Gehen Sie wie folgt vor, um die Anzahl der Führungslinien im Spaltenraster [!DNL Page Builder] zu konfigurieren:

   - Geben Sie für &quot;**[!UICONTROL Default Column Grid Size]**&quot;die Standardanzahl der Spalten ein, die im Raster angezeigt werden sollen.

   - Geben Sie für &quot;**[!UICONTROL Maximum Column Grid Size]**&quot;die größte Anzahl von Spalten ein, die im Raster verfügbar sein soll.

   >[!NOTE]
   >
   >Weitere Informationen zur Verwendung des Spaltenrasters beim Arbeiten mit Ihrem [!DNL Page Builder] -Inhalt finden Sie unter [Layout - Spalte](column.md) .

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

## Standardlayouts konfigurieren

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wählen Sie im linken Bereich unter _[!UICONTROL General]_die Option **[!UICONTROL Web]**.

1. Erweitern Sie ![Erweiterungsselektor](../assets/icon-display-expand.png) **[!UICONTROL Default Layouts]** und führen Sie folgende Schritte aus:

   ![Standardlayouts](../configuration-reference/general/assets/web-default-layouts.png){width="600" zoomable="yes"}

   Weitere Informationen zu den Web-Konfigurationsoptionen finden Sie im [_Konfigurationshandbuch_](../configuration-reference/general/web.md#default-layouts).

   - Wählen Sie die **[!UICONTROL Default Product Layout]** aus, die Sie für Produktseiten verwenden möchten.

   - Wählen Sie die **[!UICONTROL Default Category Layout]** aus, die Sie für Kategorieseiten verwenden möchten.

   - Wählen Sie die **[!UICONTROL Default Page Layout]** aus, die Sie für CMS-Seiten verwenden möchten.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

## [!DNL Page Builder] deaktivieren

>[!NOTE]
>
>Durch die Deaktivierung von [!DNL Page Builder] werden die erweiterten Content-Tools durch den WYSIWYG [editor](../content-design/editor.md) ersetzt und es können Anzeigefehler im Storefront auftreten. Inhalte, die Sie zuvor mit [!DNL Page Builder] erstellt haben, können möglicherweise nicht vom Administrator bearbeitet werden.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wählen Sie im linken Bereich unter _[!UICONTROL General]_die Option **[!UICONTROL Content Management]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]** und legen Sie **[!UICONTROL Enable Page Builder]** auf `No` fest.

1. Klicken Sie bei Aufforderung zur Bestätigung auf **[!UICONTROL Turn Off]**.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

1. Wenn Sie dazu aufgefordert werden, [aktualisieren](../systems/cache-management.md) alle ungültigen Zwischenspeicher.

[1]: https://developers.google.com/maps/documentation/javascript/get-api-key
[2]: https://mapstyle.withgoogle.com/
