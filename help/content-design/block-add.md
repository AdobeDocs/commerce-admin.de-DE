---
title: Inhaltsbausteine hinzufügen
description: Erstellen Sie benutzerdefinierte Inhaltsbausteine, die Sie auf jeder Seite oder in einem anderen Baustein wiederverwenden können.
exl-id: 2f104d77-a1d1-4f10-82ce-014955fe560b
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 0%

---

# Inhaltsbausteine hinzufügen

Benutzerdefinierte Inhaltsbausteine können erstellt und dann zu jeder Seite, Seitengruppe oder sogar zu einem anderen Baustein hinzugefügt werden. Sie können beispielsweise einen Bildschieberegler in einen Block platzieren und dann den Block auf die Startseite setzen. Der Arbeitsbereich &quot;Blöcke&quot;verwendet dieselben [grundlegenden Steuerelemente](pages-workspace.md) wie der Arbeitsbereich _Seiten_, um Ihnen bei der Suche nach verfügbaren Blöcken und der routinemäßigen Wartung zu helfen. Wenn der Block abgeschlossen ist, können Sie ihn mit dem Tool [Widget](widget-static-block.md) auf bestimmten Seiten in Ihrem Store platzieren.

![Die Seite &quot;Blöcke&quot;zeigt ein Raster vorhandener Blöcke an](./assets/blocks-workspace.png){width="700" zoomable="yes"}

## Baustein erstellen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.

1. Klicken Sie oben rechts auf **Neuen Block hinzufügen**.

   ![Auf der Seite &quot;Neuer Block&quot;werden Optionen und ein Inhaltsraum angezeigt](./assets/block-detail.png){width="500" zoomable="yes"}

1. Wenn Sie den standardmäßigen aktivierten Status des neuen Blocks ändern möchten, setzen Sie **Block aktivieren** auf `No`.

1. Weisen Sie einen **Blocktitel** als internen Verweis zu.

1. Weisen Sie dem Block eine eindeutige **Kennung** zu.

   Verwenden Sie alle Kleinbuchstaben mit Unterstrichen anstelle von Leerzeichen.

1. Wählen Sie die einzelnen **[!UICONTROL Store View]** aus, in denen der Block verfügbar sein soll.

1. Fügen Sie den Inhalt für den Baustein mithilfe des angezeigten Inhalts-Tool-Sets hinzu:

   - Wenn [Seitenaufbau](../page-builder/introduction.md) aktiviert ist, wählen Sie **[!UICONTROL Edit with Page Builder]** aus, um die Seitenaufbau-Tools im Inhalt zu verwenden [Arbeitsbereich](../page-builder/workspace.md).

     ![Seitenaufbau-Arbeitsbereich](./assets/pb-workspace-block.png){width="500" zoomable="yes"}

     >[!NOTE]
     >
     >Weitere Informationen zum Hinzufügen von Blöcken mit Page Builder finden Sie in [Tutorial 2: Blöcke](../page-builder/2-blocks.md).

   - Verwenden Sie den [Editor](editor.md), um Text zu formatieren, Links zu erstellen und Tabellen, Bilder, Videos und Audio hinzuzufügen.

     Wenn Sie lieber mit HTML-Code arbeiten möchten, klicken Sie auf **Bearbeiter einblenden/ausblenden**.

     ![Blockeditor (ausgeblendet)](./assets/block-editor-hidden.png){width="500" zoomable="yes"}

1. Klicken Sie nach Abschluss des Vorgangs auf den Pfeil **[!UICONTROL Save]** und wählen Sie **[!UICONTROL Save & Close]**.

   Der neue Block wird unten in der Liste im Raster Blöcke angezeigt.

1. Verwenden Sie das Tool [Widget](widget-static-block.md) , um den abgeschlossenen Block auf einer bestimmten Seite in Ihrem Store zu platzieren.

## Baustein löschen

Es gibt zwei Möglichkeiten, einen benutzerdefinierten Block zu entfernen. Sie können sie aus dem Raster _Blöcke_ oder aus der Seite mit den Bearbeitungsblöcken entfernen.

### Methode 1: Entfernen eines Blocks aus dem Blockraster

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.
1. Suchen Sie die Blöcke mithilfe von Filtern über dem Raster und aktivieren Sie das Kontrollkästchen für einen oder mehrere zu löschende Blöcke.
1. Setzen Sie **[!UICONTROL Actions]** in der linken oberen Ecke der Liste auf `Delete`.
1. Um die Aktion zu bestätigen, klicken Sie auf **[!UICONTROL OK]**.

### Methode 2: Entfernen eines Bausteins von der Bearbeitungsseite

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.
1. Suchen Sie den zu löschenden Block.
1. Klicken Sie in der Spalte _Aktionen_ für den Block auf **[!UICONTROL Select]** und wählen Sie **[!UICONTROL Edit]**.
1. Klicken Sie in der Menüleiste auf **[!UICONTROL Delete Block]**.
1. Um die Aktion zu bestätigen, klicken Sie auf **[!UICONTROL OK]**.

## Menü &quot;Speichern&quot;

| Befehl | Beschreibung |
|----------|----------- |
| [!UICONTROL Save] | Speichern Sie den aktuellen Block und fahren Sie mit der Arbeit fort. |
| [!UICONTROL Save & Duplicate] | Speichern und schließen Sie den aktuellen Block und öffnen Sie eine neue Kopie. |
| [!UICONTROL Save & Close] | Speichern und schließen Sie den aktuellen Block und kehren Sie zum Raster Blöcke zurück. |

{style="table-layout:auto"}

## Hinzufügen einer Lightbox oder eines Reglers

- Es ist einfach, mit [[!DNL Page Builder]](../page-builder/introduction.md) einen [Regler](../page-builder/slider.md) zu Ihrem Geschäft hinzuzufügen. Der Regler kann so eingestellt werden, dass er automatisch abgespielt wird, oder manuell mit Navigationsschaltflächen gesteuert werden.

  ![Seitenaufbau-Regler](./assets/pb-tutorial3-slider-tee-shirt-promo.png){width="600" zoomable="yes"}

  Es gibt auch eine große Auswahl an jQuery-basierten Bild-Lightboxes, die auf [[!DNL Commerce Marketplace]][1] verfügbar sind, und einige sind kostenlos.

- Sie können eine Erweiterung auch von [!DNL Commerce Marketplace] herunterladen. Weitere Hilfe finden Sie in der Dokumentation des Entwicklers.

[1]: https://marketplace.magento.com/extensions.html?q=lightbox
