---
title: Designelemente
description: Erfahren Sie, wie Sie Design-Assets wie CSS-, Schriftarten-, Bilder- und JavaScript-Dateien verwalten.
exl-id: 326c648e-eace-45a0-b53d-bbc8702fee05
feature: Page Content, Themes
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 0%

---

# Designelemente

Die _statische Dateien_ sind die Sammlung von Assets wie CSS, Schriftarten, Bildern und JavaScript, die von einem Design verwendet werden. Der Speicherort statischer Dateien wird im Abschnitt [Basis-URL](../stores-purchase/store-urls.md) Konfiguration. Sie können der URL jeder statischen Datei eine digitale Signatur hinzufügen, damit Browser erkennen können, wann eine neuere Version verfügbar ist. Die neuere Version der Datei wird verwendet, wenn sich die Signatur von der im Browser-Cache gespeicherten Signatur unterscheidet.

Bei einer Standardinstallation werden die mit einem Design verknüpften Assets im `web` Ordner am folgenden Speicherort unter dem Ordner [!DNL Commerce] root.

`[commerce_root]/app/design/frontend/Magento/[theme_name]/web`

## Hinzufügen einer digitalen Signatur zu statischen Datei-URLs

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Advanced]** und wählen **[!UICONTROL Developer]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Static Files Settings]** Abschnitt.

   ![Einstellungen für statische Dateien](./assets/developer-static-files-settings.png){width="500" zoomable="yes"}

1. Satz **[!UICONTROL Sign Static Files]** nach `Yes`.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

| Dateityp | Beschreibung |
|--- |--- |
| CSS | Steuern Sie den visuellen Stil, der der Haut zugeordnet ist. Beispielspeicherort auf dem Server: `[commerce]/app/design/frontend/Magento/[theme]/web/css` |
| Schriftarten | Geben Sie die Schriftarten an, die für die Verwendung durch das Design verfügbar sind. Speicherort auf dem Server: `[commerce]/app/design/frontend/Magento/[theme]/web/fonts` |
| Bilder | Geben Sie die vom Design verwendeten grafischen Assets an, einschließlich Schaltflächen, Hintergrundtexturen usw. Beispielspeicherort auf dem Server: `[commerce]/app/design/frontend/Magento/[theme]/web/images` |
| JS | Designspezifische JavaScript-Routinen und aufrufbare Funktionen. Beispielspeicherort auf dem Server: `[commerce]/app/design/frontend/Magento/[theme]/web/js` |

{style="table-layout:auto"}

## Zusammenführen von CSS-Dateien

Im Rahmen der Optimierung Ihrer Site und der Verkürzung der Seitenladezeit können Sie die Anzahl separater CSS-Dateien reduzieren, indem Sie sie zu einer einzigen, gekürzten Datei zusammenführen. Wenn Sie eine zusammengeführte CSS-Datei öffnen, wird ein kontinuierlicher Textstrom mit entfernten Zeilenumbrüchen angezeigt. Sie können die zusammengeführte Datei nicht bearbeiten. Daher sollten Sie am besten warten, bis Sie nicht mehr im Entwicklungsmodus sind und keine häufigen Änderungen mehr an der CSS vornehmen.

>[!NOTE]
>
>CSS-Dateien können aus der _Admin_ nur beim Arbeiten in [Entwicklermodus](../systems/developer-tools.md#operation-modes).

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Im linken Bereich: **[!UICONTROL Advanced]** und wählen **[!UICONTROL Developer]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL CSS Settings]** Abschnitt.

   ![CSS-Einstellungen](./assets/developer-css-settings.png){width="500" zoomable="yes"}

   Eine ausführliche Beschreibung dieser Konfigurationsoptionen finden Sie unter [CSS-Einstellungen](../configuration-reference/advanced/developer.md#css-settings) im _Konfigurationsreferenz_.

1. Satz **[!UICONTROL Merge CSS Files]** nach `Yes`.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

## Zusammenführen von JavaScript-Dateien

Mehrere JavaScript-Dateien können zu einer einzigen, gekürzten Datei zusammengeführt werden, um die Seitenladezeit zu verkürzen. Wenn Sie eine zusammengeführte JavaScript-Datei öffnen, wird ein kontinuierlicher Textstrom mit entfernten Zeilenumbrüchen angezeigt. Wenn Sie mit dem Entwicklungsprozess fertig sind und der Code keine Fehler enthält, sollten Sie die Dateien zusammenführen.

>[!NOTE]
>
>JavaScript-Dateien können aus der _Admin_ nur beim Arbeiten in [Entwicklermodus](../systems/developer-tools.md#operation-modes).

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Im linken Bereich: **[!UICONTROL Advanced]** und wählen **[!UICONTROL Developer]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL JavaScript Settings]** Abschnitt.

   ![JavaScript-Einstellungen](./assets/developer-javascript-settings.png){width="600" zoomable="yes"}

   Eine ausführliche Beschreibung dieser Konfigurationsoptionen finden Sie unter [JavaScript-Einstellungen](../configuration-reference/advanced/developer.md#javascript-settings) im _Konfigurationsreferenz_.

1. Satz **[!UICONTROL Merge JavaScript Files]** nach `Yes`.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.
