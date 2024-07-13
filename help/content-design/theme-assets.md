---
title: Designelemente
description: Erfahren Sie, wie Sie Design-Assets wie CSS-, Schriftarten-, Bild- und JavaScript-Dateien verwalten.
exl-id: 326c648e-eace-45a0-b53d-bbc8702fee05
feature: Page Content, Themes
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 0%

---

# Designelemente

Die _statischen Dateien_ sind die von einem Design verwendeten Assets wie CSS, Schriftarten, Bilder und JavaScript. Der Speicherort statischer Dateien wird in der Konfiguration [Basis-URL](../stores-purchase/store-urls.md) angegeben. Sie können der URL jeder statischen Datei eine digitale Signatur hinzufügen, damit Browser erkennen können, wann eine neuere Version verfügbar ist. Die neuere Version der Datei wird verwendet, wenn sich die Signatur von der im Browser-Cache gespeicherten Signatur unterscheidet.

Bei einer Standardinstallation sind die mit einem Design verknüpften Assets im Ordner &quot;`web`&quot;am folgenden Speicherort unter dem Stammordner &quot;[!DNL Commerce]&quot;organisiert.

`[commerce_root]/app/design/frontend/Magento/[theme_name]/web`

## Hinzufügen einer digitalen Signatur zu statischen Datei-URLs

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Advanced]** und wählen Sie **[!UICONTROL Developer]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Static Files Settings]** .

   ![Einstellungen für statische Dateien](./assets/developer-static-files-settings.png){width="500" zoomable="yes"}

1. Setzen Sie **[!UICONTROL Sign Static Files]** auf `Yes`.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

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
>CSS-Dateien können nur dann aus dem Bedienfeld _Admin_ zusammengeführt werden, wenn Sie im [Entwicklermodus](../systems/developer-tools.md#operation-modes) arbeiten.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wählen Sie im linken Bereich **[!UICONTROL Advanced]** und dann **[!UICONTROL Developer]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL CSS Settings]** .

   ![CSS-Einstellungen](./assets/developer-css-settings.png){width="500" zoomable="yes"}

   Detaillierte Beschreibungen dieser Konfigurationsoptionen finden Sie unter [CSS-Einstellungen](../configuration-reference/advanced/developer.md#css-settings) in der _Konfigurationsreferenz_.

1. Setzen Sie **[!UICONTROL Merge CSS Files]** auf `Yes`.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

## Zusammenführen von JavaScript-Dateien

Mehrere JavaScript-Dateien können zu einer einzigen, gekürzten Datei zusammengeführt werden, um die Seitenladezeit zu verkürzen. Wenn Sie eine zusammengeführte JavaScript-Datei öffnen, wird ein kontinuierlicher Textstrom mit entfernten Zeilenumbrüchen angezeigt. Wenn Sie mit dem Entwicklungsprozess fertig sind und der Code keine Fehler enthält, sollten Sie die Dateien zusammenführen.

>[!NOTE]
>
>JavaScript-Dateien können nur beim Arbeiten im [Entwicklermodus](../systems/developer-tools.md#operation-modes) aus dem Bedienfeld _Admin_ zusammengeführt werden.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wählen Sie im linken Bereich **[!UICONTROL Advanced]** und dann **[!UICONTROL Developer]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL JavaScript Settings]** .

   ![JavaScript-Einstellungen](./assets/developer-javascript-settings.png){width="600" zoomable="yes"}

   Detaillierte Beschreibungen dieser Konfigurationsoptionen finden Sie unter [JavaScript-Einstellungen](../configuration-reference/advanced/developer.md#javascript-settings) in der _Konfigurationsreferenz_.

1. Setzen Sie **[!UICONTROL Merge JavaScript Files]** auf `Yes`.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.
