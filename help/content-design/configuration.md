---
title: Designkonfiguration
description: Die Designkonfiguration erleichtert die Bearbeitung von Entwurfsregeln und Konfigurationseinstellungen, indem die Einstellungen auf einer einzelnen Seite angezeigt werden.
exl-id: 43fec57f-d76d-45a9-812b-ba1947cea46d
feature: Page Content, Configuration
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# Designkonfiguration

Die Designkonfiguration erleichtert die Bearbeitung von Regeln und Konfigurationseinstellungen, indem die Einstellungen auf einer Seite angezeigt werden.

![Seite &quot;Designkonfiguration&quot;](./assets/configuration.png){width="700" zoomable="yes"}

## Designkonfiguration ändern

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Suchen Sie die Store-Ansicht, die Sie konfigurieren möchten, und klicken Sie in der Spalte _[!UICONTROL Action]_auf **[!UICONTROL Edit]**.

   Auf der Seite werden die aktuellen Designeinstellungen für die Store-Ansicht angezeigt.

1. Um das Standarddesign zu ändern, setzen Sie **[!UICONTROL Applied Theme]** auf das Design, das Sie auf die Ansicht anwenden möchten.

   Wenn kein Design angegeben ist, wird das standardmäßige Systemdesign verwendet. Einige Drittanbietererweiterungen ändern das Standarddesign des Systems.

1. Wenn das Design nur für ein bestimmtes Gerät verwendet werden soll, legen Sie die **[!UICONTROL User Agent Rules]** fest.

   ![Benutzeragenten-Regeln](./assets/configuration-user-agent-rules.png){width="400" zoomable="yes"}

   Für jeden Gerätetyp, für den Sie ein Design angeben möchten:

   - Klicken Sie auf **[!UICONTROL Add New User Agent Rule]**.

   - Geben Sie für &quot;**[!UICONTROL Search String]**&quot;die Browser-ID für das jeweilige Gerät ein.

     Eine Suchzeichenfolge kann entweder ein normaler Ausdruck oder ein mit Perl kompatibler regulärer Ausdruck (PCRE) sein (weitere Informationen finden Sie unter [Benutzeragent](https://en.wikipedia.org/wiki/User_agent) ). Die folgende Suchzeichenfolge identifiziert Firefox:

         /^mozilla/i
     
   - Wählen Sie für **[!UICONTROL Theme Name]** das Design aus, das für das angegebene Gerät verwendet werden soll.

   >[!NOTE]
   >
   >Sie können so viele Regeln für die Geräte hinzufügen, die Sie festlegen möchten. Die Suchzeichenfolgen werden in der angegebenen Reihenfolge abgeglichen.

1. Erweitern Sie unter _[!UICONTROL Other Settings]_jeden Abschnitt und befolgen Sie die Anweisungen in den verknüpften Themen, um die Einstellungen nach Bedarf zu bearbeiten.

   - [[!UICONTROL Pagination]](../catalog/navigation-product-listings.md#pagination-controls)
   - [[!UICONTROL HTML Head]](page-setup.md#html-head)
   - [[!UICONTROL Header]](page-setup.md#header)
   - [[!UICONTROL Footer]](page-setup.md#footer)
   - [[!UICONTROL Search Engine Robots]](../merchandising-promotions/seo-overview.md#search-engine-robots)
   - [[!UICONTROL Product Image Watermarks]](../catalog/product-image.md#watermarks)
   - [[!UICONTROL Transactional Emails]](../systems/email-templates.md#configure-email-templates)

   ![Andere Einstellungen mit Auswirkungen auf das Design](./assets/configuration-other-settings.png){width="500" zoomable="yes"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Configuration]**.
