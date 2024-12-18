---
title: Design-Assets
description: Erfahren Sie, wie Sie Ihre Design-Assets wie CSS, Schriftarten, Bilder und JavaScript-Dateien verwalten.
exl-id: 326c648e-eace-45a0-b53d-bbc8702fee05
feature: Page Content, Themes
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 0%

---

# Design-Assets

Die _statischen Dateien_ sind die Sammlung von Assets wie CSS, Schriftarten, Bildern und JavaScript, die von einem Design verwendet wird. Der Speicherort statischer Dateien wird in der Konfiguration [Basis-URL](../stores-purchase/store-urls.md) angegeben. Sie können der URL jeder statischen Datei eine digitale Signatur hinzufügen, damit Browser erkennen können, wann eine neuere Version verfügbar ist. Die neuere Version der Datei wird verwendet, wenn sich die Signatur von der im Browsercache gespeicherten unterscheidet.

Bei einer Standardinstallation sind die mit einem Design verknüpften Assets im Ordner `web` am folgenden Speicherort unter dem [!DNL Commerce] organisiert.

`[commerce_root]/app/design/frontend/Magento/[theme_name]/web`

## Hinzufügen einer digitalen Signatur zu statischen Datei-URLs

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Advanced]** und wählen Sie **[!UICONTROL Developer]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Static Files Settings]** .

   ![Statische Dateieinstellungen](./assets/developer-static-files-settings.png){width="500" zoomable="yes"}

1. Legen Sie **[!UICONTROL Sign Static Files]** auf `Yes` fest.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

| Dateityp | Beschreibung |
|--- |--- |
| CSS | Steuern Sie den visuellen Stil, der mit dem Design verknüpft ist. Beispielspeicherort auf dem Server: `[commerce]/app/design/frontend/Magento/[theme]/web/css` |
| Schriftarten | Geben Sie die Schriftarten an, die für die Verwendung durch das Design verfügbar sind. Speicherort auf Server: `[commerce]/app/design/frontend/Magento/[theme]/web/fonts` |
| Bilder | Stellen Sie die vom Design verwendeten grafischen Assets bereit, einschließlich Schaltflächen, Hintergrundtexturen usw. Beispielspeicherort auf dem Server: `[commerce]/app/design/frontend/Magento/[theme]/web/images` |
| JS | Themenspezifische JavaScript-Routinen und aufrufbare Funktionen. Beispielspeicherort auf dem Server: `[commerce]/app/design/frontend/Magento/[theme]/web/js` |

{style="table-layout:auto"}

## Zusammenführen von CSS-Dateien

Um Ihre Site zu optimieren und die Seitenladezeit zu reduzieren, können Sie die Anzahl der separaten CSS-Dateien reduzieren, indem Sie sie in einer einzigen, zusammengefassten Datei zusammenführen. Wenn Sie eine zusammengeführte CSS-Datei öffnen, wird ein fortlaufender Textfluss angezeigt, aus dem Zeilenumbrüche entfernt wurden. Sie können die zusammengeführte Datei nicht bearbeiten. Daher ist es am besten, zu warten, bis Sie den Entwicklungsmodus verlassen haben und keine häufigen Änderungen mehr an CSS vornehmen.

>[!NOTE]
>
>CSS-Dateien können aus dem Bedienfeld _Admin_ nur zusammengeführt werden, wenn [Entwicklermodus) ](../systems/developer-tools.md#operation-modes).

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wählen Sie im linken Bedienfeld **[!UICONTROL Developer]** aus und **[!UICONTROL Advanced]** Sie diese aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL CSS Settings]** .

   ![CSS-Einstellungen](./assets/developer-css-settings.png){width="500" zoomable="yes"}

   Detaillierte Beschreibungen dieser Konfigurationsoptionen finden Sie unter [CSS-Einstellungen](../configuration-reference/advanced/developer.md#css-settings) in _Konfigurationsreferenz_.

1. Legen Sie **[!UICONTROL Merge CSS Files]** auf `Yes` fest.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

## Zusammenführen von JavaScript-Dateien

Mehrere JavaScript-Dateien können zu einer einzigen, zusammengefassten Datei zusammengeführt werden, um die Seitenladezeit zu reduzieren. Wenn Sie eine zusammengeführte JavaScript-Datei öffnen, wird ein fortlaufender Textstrom angezeigt, wobei die Zeilenumbrüche entfernt wurden. Wenn Sie mit dem Entwicklungsprozess fertig sind und der Code keine Fehler enthält, sollten Sie die Dateien zusammenführen.

>[!NOTE]
>
>JavaScript-Dateien können aus dem Bedienfeld _Admin_ nur zusammengeführt werden, wenn [Entwicklermodus](../systems/developer-tools.md#operation-modes).

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wählen Sie im linken Bedienfeld **[!UICONTROL Developer]** aus und **[!UICONTROL Advanced]** Sie diese aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL JavaScript Settings]** .

   ![JavaScript-Einstellungen](./assets/developer-javascript-settings.png){width="600" zoomable="yes"}

   Detaillierte Beschreibungen dieser Konfigurationsoptionen finden Sie unter [JavaScript-Einstellungen](../configuration-reference/advanced/developer.md#javascript-settings) in _Konfigurationsreferenz_.

1. Legen Sie **[!UICONTROL Merge JavaScript Files]** auf `Yes` fest.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.
