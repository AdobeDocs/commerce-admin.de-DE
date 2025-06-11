---
title: Medienspeicher
description: Erfahren Sie, wie Sie mit der Medienspeicherung Commerce-Mediendateien organisieren und auf diese zugreifen können, die auf dem Server gespeichert sind.
exl-id: 5cf1bb20-d747-4a12-8558-e167c229efe8
feature: Page Content, Media
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/de/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 0%

---

# Medienspeicher

Mit der Medienspeicherung können Sie Mediendateien, die auf dem Server gespeichert sind, organisieren und auf sie zugreifen. Der Pfad zum Speicherort der Dateien wird durch die Konfiguration [Basis-URL](../stores-purchase/store-urls.md) bestimmt. Auf Dateien im Medienspeicher kann vom Editor aus zugegriffen werden, während an Seiten und statischen Blöcken gearbeitet wird. Normalerweise befindet sich der Medienspeicher im Dateisystem auf demselben Server wie die [!DNL Commerce] Programmdateien.

Alternativ können Mediendateien in einer [Datenbank](media-storage-database.md) oder auf einem separaten Server oder [Content Delivery Network](media-storage-content-delivery-network.md) verwaltet werden. Der Vorteil der Verwendung von alternativem Speicher besteht darin, dass der Aufwand für die Synchronisierung von Medien minimiert wird. Die Synchronisierungsleistung wird besonders dann beeinträchtigt, wenn mehrere Instanzen des Systems auf verschiedenen Servern bereitgestellt werden, die Zugriff auf dieselben Bilder, CSS-Dateien und andere Mediendateien benötigen.

Der Editor kann so konfiguriert werden, dass entweder statische oder [Dynamic Media-URLs](../catalog/catalog-urls.md#configure-catalog-media-url-format) für Kataloginhalte in Kategorie- oder Produktbeschreibungen verwendet werden.

![[!DNL Commerce] Media-Speicher](./assets/media-storage.png){width="650" zoomable="yes"}

## Hinzufügen von Dateien zum Medienspeicher

Die ersten beiden Schritte sind die gleichen wie beim Einfügen eines Bildes.

1. Klicken Sie in [Editor](editor.md)-Symbolleiste auf das Symbol _Bild einfügen_.

   ![Symbol „Bild einfügen“](./assets/editor-toolbar-image-button.png){width="700" zoomable="yes"}

   Diese Aktion öffnet das _[!UICONTROL Insert/edit image]_&#x200B;Dialogfeld.

1. Klicken Sie _[!UICONTROL Source]_&#x200B;auf das Symbol_ Suchen _(![Suchsymbol](./assets/media-gallery-icon-browse.png){width="10" zoomable="no"}).

1. Führen Sie in der Verzeichnisstruktur auf der linken Seite einen der folgenden Schritte aus:

   - Navigieren Sie zu dem Ordner, in dem Sie das hochgeladene Bild speichern möchten.

   - Navigieren Sie zu der Stelle, an der Sie einen Ordner erstellen möchten, und klicken Sie auf **Ordner erstellen**.

     Um einen Ordner hinzuzufügen, geben Sie den Ordnernamen ein und klicken Sie auf **[!UICONTROL OK]**.

1. Um eine oder mehrere Dateien zum Medienspeicher hinzuzufügen, können Sie die Dateien entweder aus Ihrem System hochladen oder die [Adobe Stock-Integration verwenden](adobe-stock.md):

   Um Dateien von Ihrem System hochzuladen, klicken Sie auf **[!UICONTROL Choose Files]** und führen Sie folgende Schritte aus:

   - Navigieren Sie im Verzeichnis Ihres lokalen Computers zum Speicherort der Bilder.

   - Wählen Sie die Bilder für den Upload aus.

   - Klicken Sie auf **[!UICONTROL Open]**.

   So verwenden Sie Assets aus Adobe Stock mithilfe der [Integration](adobe-stock.md):

   - Klicken Sie auf **[!UICONTROL Search Adobe Stock]**.

   - Hinzufügen einer Vorschau oder eines lizenzierten Bildes aus Adobe Stock (siehe [Verwenden von Adobe Stock-Bildern](adobe-stock-manage.md))

Die Bilder werden in den aktuellen Medienspeicherordner auf dem Server hochgeladen.

![[!DNL Commerce] Media-Speicher](./assets/media-storage.png){width="650" zoomable="yes"}

## Einfügen eines Bildes aus dem Medienspeicher

Öffnen Sie die Seite oder den Block, die/der bearbeitet werden soll. Verwenden Sie dann eine der folgenden Methoden, um ein Bild aus dem Medienspeicher einzufügen:

### Methode 1: WYSIWYG-Modus

1. Klicken Sie in [Editor](editor.md)-Symbolleiste auf das Symbol _Bild einfügen_.

1. Klicken Sie _[!UICONTROL Source]_&#x200B;auf das Symbol_ Suchen _(![Suchsymbol](./assets/media-gallery-icon-browse.png){width="10" zoomable="no"}).

   ![Auswählen des Suchsymbols](./assets/editor-dialog-insert-image.png){width="250" zoomable="yes"}

1. Navigieren Sie in der Verzeichnisstruktur auf der linken Seite zu dem Ordner, in dem das Bild gespeichert ist.

1. Wählen Sie die Kachel des Bildes aus und klicken Sie auf **[!UICONTROL Add Selected]**.

### Methode 2: HTML-Modus

1. Positionieren Sie den Cursor im Code, in den das `<img>`-Tag eingefügt werden soll.

1. Klicken Sie auf **[!UICONTROL Insert Image]**.

   ![Bild einfügen (HTML-Modus)](./assets/editor-html-mode-insert-image.png){width="600" zoomable="yes"}
