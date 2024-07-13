---
title: Medienspeicher
description: Erfahren Sie, wie Sie mithilfe der Medienspeicherung die auf dem Server gespeicherten Commerce-Mediendateien organisieren und darauf zugreifen können.
exl-id: 5cf1bb20-d747-4a12-8558-e167c229efe8
feature: Page Content, Media
source-git-commit: 7dae6b6d387c796c5ff472293c6590fabaa83e85
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---

# Medienspeicher

Der Medienspeicher hilft Ihnen beim Organisieren und Empfangen von Zugriffen auf Mediendateien, die auf dem Server gespeichert sind. Der Pfad zum Speicherort der Dateien wird durch die Konfiguration [Basis-URL](../stores-purchase/store-urls.md) bestimmt. Der Zugriff auf Dateien im Medienspeicher ist über den Editor möglich, während Sie an Seiten und statischen Blöcken arbeiten. Normalerweise befindet sich der Medienspeicher im Dateisystem auf demselben Server wie die [!DNL Commerce] -Programmdateien.

Alternativ können Mediendateien in einer [Datenbank](media-storage-database.md) oder einem separaten Server oder dem [Netzwerk zur Inhaltsbereitstellung](media-storage-content-delivery-network.md) verwaltet werden. Der Vorteil der Verwendung von alternativem Speicher besteht darin, dass der für die Synchronisierung der Medien erforderliche Aufwand minimiert wird. Die Synchronisierungsleistung ist besonders betroffen, wenn mehrere Instanzen des Systems auf verschiedenen Servern bereitgestellt werden, die Zugriff auf dieselben Bilder, CSS-Dateien und anderen Mediendateien benötigen.

Der Editor kann so konfiguriert werden, dass für Kataloginhalte in Kategorie- oder Produktbeschreibungen entweder statische oder [dynamische Medien-URLs](../catalog/catalog-urls.md#configure-catalog-media-url-format) verwendet werden.

![[!DNL Commerce] Medienspeicher](./assets/media-storage.png){width="650" zoomable="yes"}

## Hinzufügen von Dateien zum Medienspeicher

Die ersten beiden Schritte sind dieselben wie beim Einfügen eines Bildes.

1. Klicken Sie in der Symbolleiste [editor](editor.md) auf das Symbol _Bild einfügen_ .

   ![Symbol &quot;Bild einfügen&quot;](./assets/editor-toolbar-image-button.png){width="700" zoomable="yes"}

   Durch diese Aktion wird das Dialogfeld &quot;_[!UICONTROL Insert/edit image]_&quot; geöffnet.

1. Klicken Sie nach _[!UICONTROL Source]_auf das Symbol_ Suchen _(![Suchsymbol](./assets/media-gallery-icon-browse.png){width="10" zoomable="no"}).

1. Führen Sie in der Ordnerstruktur auf der linken Seite einen der folgenden Schritte aus:

   - Navigieren Sie zu dem Ordner, in dem Sie das hochgeladene Bild speichern möchten.

   - Navigieren Sie zu dem Ort, an dem Sie einen Ordner erstellen möchten, und klicken Sie auf **Ordner erstellen**.

     Geben Sie zum Hinzufügen eines Ordners den Ordnernamen ein und klicken Sie auf **[!UICONTROL OK]**.

1. Um eine oder mehrere Dateien zum Medienspeicher hinzuzufügen, können Sie entweder die Dateien von Ihrem System hochladen oder die [Adobe Stock-Integration](adobe-stock.md) verwenden:

   Um Dateien von Ihrem System hochzuladen, klicken Sie auf **[!UICONTROL Choose Files]** und führen Sie die folgenden Schritte aus:

   - Navigieren Sie im Verzeichnis Ihres lokalen Computers zum Speicherort der Bilder.

   - Wählen Sie jedes Bild aus, das hochgeladen werden soll.

   - Klicken Sie auf **[!UICONTROL Open]**.

   So verwenden Sie Assets aus Adobe Stock mithilfe der [Integration](adobe-stock.md):

   - Klicken Sie auf **[!UICONTROL Search Adobe Stock]**.

   - Fügen Sie eine Vorschau oder ein lizenziertes Bild aus Adobe Stock hinzu (siehe [Verwenden von Adobe Stock-Bildern](adobe-stock-manage.md)).

Die Bilder werden in den aktuellen Ordner Medienspeicher auf dem Server hochgeladen.

![[!DNL Commerce] Medienspeicher](./assets/media-storage.png){width="650" zoomable="yes"}

## Bild aus Medienspeicher einfügen

Öffnen Sie die zu bearbeitende Seite oder den Block. Verwenden Sie dann eine der folgenden Methoden, um ein Bild aus dem Medienspeicher einzufügen:

### Methode 1: WYSIWYG-Modus

1. Klicken Sie in der Symbolleiste [editor](editor.md) auf das Symbol _Bild einfügen_ .

1. Klicken Sie nach _[!UICONTROL Source]_auf das Symbol_ Suchen _(![Suchsymbol](./assets/media-gallery-icon-browse.png){width="10" zoomable="no"}).

   ![Auswählen des Suchsymbols](./assets/editor-dialog-insert-image.png){width="250" zoomable="yes"}

1. Navigieren Sie in der Ordnerstruktur auf der linken Seite zum Ordner, in dem das Bild gespeichert ist.

1. Wählen Sie die Kachel des Bildes aus und klicken Sie auf **[!UICONTROL Add Selected]**.

### Methode 2: HTML Modus

1. Positionieren Sie den Cursor im Code, in den das Tag `<img>` eingefügt werden soll.

1. Klicken Sie auf **[!UICONTROL Insert Image]**.

   ![Bild einfügen (HTML-Modus)](./assets/editor-html-mode-insert-image.png){width="600" zoomable="yes"}
