---
title: Erkennung von Browser-Funktionen
description: Erfahren Sie, wie Sie die Browser-Erkennung konfigurieren und einen Hinweis anzeigen, wenn die Browser-Einstellungen des Kunden geändert werden müssen.
exl-id: 16caab8b-3ba5-43a1-a6f0-7c1e921be132
role: Admin
feature: Configuration, Security
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/de/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
TQID: https://experienceleague.adobe.com/zPxdplYIYblw6-tsDvxEmvKfAx-2M6opb6qjX7YL1I4
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 285
ht-degree: 0%

---

# Erkennung von Browser-Funktionen

Wie die meisten Websites und Anwendungen im Internet erfordern Adobe Commerce und Magento Open Source, dass der Browser des Besuchers sowohl Cookies als auch JavaScript für den vollständigen Betrieb zulässt. Gelegentlich ist jedoch der Browser eines Benutzers auf die höchste Datenschutzeinstellung eingestellt, die sowohl Cookies als auch JavaScript verhindert. Ihr Store kann so konfiguriert werden, dass die Funktionen des Browsers jedes Besuchers getestet werden und ein Hinweis angezeigt wird, wenn die Einstellungen geändert werden müssen.

- Wenn Cookies in den Datenschutzeinstellungen des Browsers nicht zulässig sind, können Sie das System so konfigurieren, dass sie automatisch zur Seite &quot;[&#x200B; aktivieren](../content-design/pages.md#enable-cookies) umgeleitet werden, auf der erläutert wird, wie Sie die empfohlenen Einstellungen mit den meisten Browsern vornehmen können.
- Wenn JavaScript in den Datenschutzeinstellungen des Browsers nicht zulässig ist, können Sie das System so konfigurieren, dass die folgende Meldung über der Kopfzeile jeder Seite angezeigt wird.

Technische Informationen finden Sie unter [Unterstützte Browser](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/system-requirements.html?lang=de#supported-browsers) im _Installationshandbuch_.

## Konfigurieren der Browser-Erkennung

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wählen Sie im Bedienfeld links unter _[!UICONTROL General]_&#x200B;**[!UICONTROL Web]**&#x200B;aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Browser Capabilities Detection]** und führen Sie folgende Schritte aus:

   - Um Anweisungen anzuzeigen, die erläutern, wie der Browser so konfiguriert wird, dass Cookies zugelassen werden, setzen Sie **[!UICONTROL Redirect to CMS-page if Cookies are Disabled]** auf `Yes`.

   - Um ein Banner über der Kopfzeile anzuzeigen, wenn JavaScript im Browser des Benutzers deaktiviert ist, setzen Sie **[!UICONTROL Show Notice if JavaScript is Disabled]** auf `Yes`.

   - Um ein Banner über der Kopfzeile anzuzeigen, wenn Lokaler Speicher im Browser des Benutzers deaktiviert ist, setzen Sie **[!UICONTROL Show Notice if Local Storage is Disabled]** auf `Yes`.

   ![Allgemeine Konfiguration - Erkennung von Webbrowser-Funktionen](../configuration-reference/general/assets/web-browser-capabilities-detection.png){width="600" zoomable="yes"}

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.
