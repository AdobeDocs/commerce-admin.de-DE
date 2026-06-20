---
title: Dynamic Media-URLs
description: Erfahren Sie mehr über die Verwendung einer Dynamic Media-URL als relativer Verweis auf ein Bild oder ein anderes Medien-Asset.
exl-id: 41aabde2-f6cc-4b83-8d56-9753a7aa93e9
feature: CMS, Media
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/de/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
TQID: https://experienceleague.adobe.com/nml-pHTHdSPcvIVnRwlyjJPhEo2PWdTEKfkn2AFKjvA
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 316
ht-degree: 0%

---

# Dynamic Media-URLs

Eine Dynamic Media-URL ist ein relativer Verweis auf ein Bild oder ein anderes Medien-Asset. Wenn diese Option aktiviert ist, können Dynamic Media-URLs verwendet werden, um eine direkte Verbindung zu Assets auf Ihrem Server oder zu Dateien herzustellen, die in einem [Content Delivery Network“ gespeichert &#x200B;](media-storage-content-delivery-network.md). Die Verwendung von Dynamic Media-URLs kann sich auf die Katalogleistung auswirken, und der [Editor](editor.md#configure-the-editor) kann so konfiguriert werden, dass entweder statische oder Dynamic Media-URLs verwendet werden.

Wie bei allen [Markup-Tags](../systems/markup-tags.md) ist die Direktive in doppelte geschweifte Klammern eingeschlossen. Das Format einer Dynamic Media-URL sieht wie folgt aus:

`\{\{media url="path/to/image.jpg"}}`

Dynamische URL-Anweisungen werden aus gespeicherten HTML-Inhalten verarbeitet, wenn die Seite in der Storefront gerendert wird. Jedes Mal, wenn die Seite gerendert wird, wird der Inhalt auf `\{\{media url="..."}}` überprüft und jede Anweisung wird durch die entsprechende Medien-URL ersetzt.

{{$include /help/_includes/directives-caution.md}}

## Konfigurieren von statischen Medien-URLs

Standardmäßig verfügen die aus dem WYSIWYG-Editor in den Katalog eingefügten Bilder über relative, dynamische URLs. Wenn Sie eine statische URL bevorzugen, können Sie die Konfigurationseinstellung ändern.

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wählen Sie im linken Bedienfeld unter _[!UICONTROL General]_&#x200B;die Option **[!UICONTROL Content Management]**&#x200B;aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL WYSIWYG Options]** .

   ![WYSIWYG-Optionen](../configuration-reference/general/assets/content-management-wysiwyg-options.png){width="600" zoomable="yes"}

>[!NOTE]
>
>TinyMCE wurde in Magento 2.4.6 und höheren Versionen durch Hugerte als standardmäßigen WYSIWYG-Editor ersetzt.

1. Legen Sie **[!UICONTROL Use Static URLs for Media Content in WYSIWYG]** auf eine der folgenden Einstellungen fest:

   - `Yes` - Verwendet statische URLs für Medieninhalte, die mit dem WYSIWYG-Editor eingefügt werden. Statische URLs sind absolut und werden ungültig, wenn sich die [Basis-URL](../stores-purchase/store-urls.md) des Stores ändert.

   - `No` - (Standard) Verwendet dynamische URLs für Medieninhalte, die mit dem WYSIWYG-Editor eingefügt werden, basierend auf der `\{\{media url="..."}}`. Dynamische URLs sind relativ und funktionieren nicht beschädigt, wenn sich die Basis-URL des Stores ändert.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

<!-- Last updated from includes: 2022-08-30 15:36:09 -->
