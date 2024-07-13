---
title: Erkennung von Browserfunktionen
description: Erfahren Sie, wie Sie die Browserfunktionserkennung konfigurieren und eine Meldung anzeigen können, wenn die Browsereinstellungen des Kunden geändert werden müssen.
exl-id: 16caab8b-3ba5-43a1-a6f0-7c1e921be132
role: Admin
feature: Configuration, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---

# Erkennung von Browserfunktionen

Wie bei den meisten Websites und Anwendungen im Internet erfordern Adobe Commerce und Magento Open Source, dass der Browser des Besuchers sowohl Cookies als auch JavaScript für den vollständigen Betrieb zulässt. Gelegentlich wird der Browser eines Benutzers jedoch auf die höchste Datenschutzeinstellung gesetzt, die sowohl Cookies als auch JavaScript verhindert. Ihr Store kann so konfiguriert werden, dass die Funktionen des Browsers jedes Besuchers getestet und ein Hinweis angezeigt wird, wenn die Einstellungen geändert werden müssen.

- Wenn die Datenschutzeinstellungen des Browsers Cookies nicht zulassen, können Sie das System so konfigurieren, dass sie automatisch zur Seite [Cookies aktivieren](../content-design/pages.md#enable-cookies) weitergeleitet werden. Dort wird erläutert, wie die empfohlenen Einstellungen für die meisten Browser vorgenommen werden.
- Wenn die Datenschutzeinstellungen des Browsers JavaScript nicht zulassen, können Sie das System so konfigurieren, dass die folgende Meldung über der Kopfzeile jeder Seite angezeigt wird.

Technische Informationen finden Sie unter [Unterstützte Browser](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/system-requirements.html#supported-browsers) im _Installationshandbuch_.

## Browserfunktionserkennung konfigurieren

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wählen Sie im Bedienfeld auf der linken Seite unter _[!UICONTROL General]_die Option **[!UICONTROL Web]**.

1. Erweitern Sie den Abschnitt **[!UICONTROL Browser Capabilities Detection]** des Erweiterungsselektors ![Erweiterung](../assets/icon-display-expand.png) und führen Sie folgende Schritte aus:

   - Um Anweisungen anzuzeigen, die erklären, wie der Browser so konfiguriert werden kann, dass Cookies zugelassen werden, setzen Sie **[!UICONTROL Redirect to CMS-page if Cookies are Disabled]** auf `Yes`.

   - Um ein Banner über der Kopfzeile anzuzeigen, wenn JavaScript im Browser des Benutzers deaktiviert ist, setzen Sie **[!UICONTROL Show Notice if JavaScript is Disabled]** auf `Yes`.

   - Um ein Banner über der Kopfzeile anzuzeigen, wenn &quot;Lokaler Speicher&quot;im Browser des Benutzers deaktiviert ist, setzen Sie **[!UICONTROL Show Notice if Local Storage is Disabled]** auf `Yes`.

   ![Allgemeine Konfiguration - Erkennung von Webbrowserfunktionen](../configuration-reference/general/assets/web-browser-capabilities-detection.png){width="600" zoomable="yes"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.
