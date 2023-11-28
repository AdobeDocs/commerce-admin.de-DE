---
title: Designkonfiguration
description: Die Designkonfiguration erleichtert die Bearbeitung von Entwurfsregeln und Konfigurationseinstellungen, indem die Einstellungen auf einer einzelnen Seite angezeigt werden.
exl-id: 43fec57f-d76d-45a9-812b-ba1947cea46d
feature: Page Content, Configuration
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 0%

---

# Designkonfiguration

Die Designkonfiguration erleichtert die Bearbeitung von Regeln und Konfigurationseinstellungen, indem die Einstellungen auf einer Seite angezeigt werden.

![Seite &quot;Designkonfiguration&quot;](./assets/configuration.png){width="700" zoomable="yes"}

## Designkonfiguration ändern

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Suchen Sie die Store-Ansicht, die Sie konfigurieren möchten, und klicken Sie auf **[!UICONTROL Edit]** im _[!UICONTROL Action]_Spalte.

   Auf der Seite werden die aktuellen Designeinstellungen für die Store-Ansicht angezeigt.

1. Um das Standarddesign zu ändern, legen Sie **[!UICONTROL Applied Theme]** auf das Design, das Sie auf die Ansicht anwenden möchten.

   Wenn kein Design angegeben ist, wird das standardmäßige Systemdesign verwendet. Einige Drittanbietererweiterungen ändern das Standarddesign des Systems.

1. Wenn das Design nur für ein bestimmtes Gerät verwendet werden soll, legen Sie die **[!UICONTROL User Agent Rules]**.

   ![Benutzeragenten-Regeln](./assets/configuration-user-agent-rules.png){width="400" zoomable="yes"}

   Für jeden Gerätetyp, für den Sie ein Design angeben möchten:

   - Klicken **[!UICONTROL Add New User Agent Rule]**.

   - Für **[!UICONTROL Search String]** eingeben, geben Sie die Browser-ID für das jeweilige Gerät ein.

     Eine Suchzeichenfolge kann entweder ein normaler Ausdruck oder ein mit Perl kompatibler regulärer Ausdruck (PCRE) sein (siehe [Benutzeragent](https://en.wikipedia.org/wiki/User_agent) für weitere Informationen). Die folgende Suchzeichenfolge identifiziert Firefox:

         /^mozilla/i
     
   - Für **[!UICONTROL Theme Name]** wählen Sie das Design für das angegebene Gerät aus.

   >[!NOTE]
   >
   >Sie können so viele Regeln für die Geräte hinzufügen, die Sie festlegen möchten. Die Suchzeichenfolgen werden in der angegebenen Reihenfolge abgeglichen.

1. under _[!UICONTROL Other Settings]_, erweitern Sie jeden Abschnitt und befolgen Sie die Anweisungen in den verknüpften Themen, um die Einstellungen nach Bedarf zu bearbeiten.

   - [[!UICONTROL Pagination]](../catalog/navigation-product-listings.md#pagination-controls)
   - [[!UICONTROL HTML Head]](page-setup.md#html-head)
   - [[!UICONTROL Header]](page-setup.md#header)
   - [[!UICONTROL Footer]](page-setup.md#footer)
   - [[!UICONTROL Search Engine Robots]](../merchandising-promotions/seo-overview.md#search-engine-robots)
   - [[!UICONTROL Product Image Watermarks]](../catalog/product-image.md#watermarks)
   - [[!UICONTROL Transactional Emails]](../systems/email-templates.md#configure-email-templates)

   ![Andere Einstellungen, die sich auf das Design auswirken](./assets/configuration-other-settings.png){width="500" zoomable="yes"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Configuration]**.
