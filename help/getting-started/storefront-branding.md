---
title: Storefront-Branding
description: Erfahren Sie mehr über das Ändern der Elemente, die die Markenidentität Ihres Stores definieren.
exl-id: 91630717-9da7-4d2f-a0d8-adb794a30ee1
feature: Storefront
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '1309'
ht-degree: 0%

---

# Storefront-Branding

Eines der ersten Dinge, die Sie tun möchten, ist [Logo ändern](#upload-your-logo) in der Kopfzeile und [ein Favicon hochladen](#add-a-favicon) für den Browser. Als Nächstes sollten Sie [Ihre Begrüßungsnachricht hinzufügen](#change-the-welcome-message) und [den Copyright-Hinweis aktualisieren](#change-the-copyright-notice) in der Fußzeile einfügen. Diese Aufgaben sind einige einfache Design-Elemente, die Sie sofort übernehmen können. Während sich Ihr Store in der Entwicklung befindet, können [ den Hinweis zur Store-Demo ](#set-the-store-demo-notice) und ihn dann entfernen, wenn Sie für den Start bereit sind.

![Storefront-Branding-Elemente](./assets/storefront-home-page-branding.png){width="600" zoomable="yes"}

## Logo hochladen

Die Größe und Position des Logos in der Kopfzeile wird durch das Store-Design bestimmt. Ihr Logo kann entweder als GIF-, PNG- oder JPG-Dateityp (JPEG) gespeichert und vom Administrator Ihres Shops hochgeladen werden.

![Logo in der Kopfzeile](./assets/storefront-header-logo.png){width="600"}

Das Logobild befindet sich am folgenden Speicherort auf dem Server. Jede Bilddatei mit dem Namen `logo.svg` wird als Standard-Design-Logo verwendet.

Vollständiger Pfad - `app/design/frontend/[vendor]/[theme]/web/images/logo.svg`

Relativer Pfad - `images/logo.svg`

Wenn Sie die Größe des Logos oder anderer in Ihrem Design verwendeter Bilder nicht kennen, öffnen Sie die Seite in einem Browser, klicken Sie mit der rechten Maustaste auf das Bild und überprüfen Sie das Element.

>[!NOTE]
>
>Zusätzlich zum Logo in der Kopfzeile erscheint Ihr Logo auch auf [E-Mail-Vorlagen](../systems/email-templates.md#prepare-your-email-logo) und auf [PDF-Rechnungen](../stores-purchase/sales-documents.md) und anderen Verkaufsdokumenten. Die Logos für E-Mail-Vorlagen und Rechnungen haben unterschiedliche Größenanforderungen und müssen separat hochgeladen werden.

Unterstützte Logodateiformate:

| Dateiformat | Beschreibung |
|--- |--- |
| PNG | (Portable Network Graphics) Diese neuere Alternative zum GIF-Format unterstützt bis zu 16 Millionen Farben (24 Bit). Das verlustfreie Komprimierungsformat erzeugt ein hochwertiges Bitmap-Bild mit klarem Text, aber einer größeren Dateigröße als einige Formate. Das PNG-Format unterstützt transparente Ebenen und wurde für die Online-Anzeige und das Streaming entwickelt. |
| GIF | (Graphics Interchange Format) Ein weit verbreitetes und älteres Bitmap-Format, das auf 256 Farben (8 Bit) beschränkt ist. Das GIF-Format unterstützt einfache Animationen und transparente Ebenen. |
| JPG (JPEG) | (Joint Fotografic Expert Group) Ein komprimiertes Bitmap-Format, das von den meisten Digitalkameras verwendet wird. Die verlustbehaftete Komprimierung verursacht einen gewissen Datenverlust, der sich manchmal als verschwommene Flecken im Text bemerkbar macht. |

{style="table-layout:auto"}

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

   ![Design-Konfigurationsseite](./assets/design-configuration.png){width="700"}

1. Suchen Sie die Store-Ansicht, die Sie konfigurieren möchten, und klicken Sie in der Spalte _[!UICONTROL Action]_auf **[!UICONTROL Edit]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Header]** .

   ![Header-Einstellungen](./assets/configuration-header.png){width="600"}

1. Um ein neues Logo hochzuladen, klicken Sie auf **[!UICONTROL Upload]** und wählen Sie die Datei aus Ihrem System aus.

1. Geben Sie **[!UICONTROL Logo Image Width]** und **[!UICONTROL Logo Image Height]** in Pixel ein.

1. Geben Sie **[!UICONTROL Logo Image Alt]** den Text ein, der angezeigt werden soll, wenn jemand den Mauszeiger über das Bild bewegt.

1. Klicken Sie abschließend auf **[!UICONTROL Save Configuration]**.

## Favicon hinzufügen

_Favicon_ ist die Abkürzung für _Lieblingssymbol_ und bezieht sich auf das kleine Symbol auf der Registerkarte jeder Browser-Seite. Je nach Browser wird das Favicon auch in der Adressleiste, direkt vor der URL, angezeigt.

Ein Favicon ist im Allgemeinen 16 x 16 Pixel oder 32 x 32 Pixel groß. [!DNL Commerce] akzeptiert die Dateitypen ICO, PNG, APNG, GIF und JPG (JPEG), auch wenn diese Formate nicht von allen Browsern unterstützt werden. Das am häufigsten unterstützte Dateiformat für ein Favicon ist ICO. Sie können auch andere Bilddateitypen verwenden, das Format wird jedoch möglicherweise nicht von allen Browsern unterstützt. Es gibt viele kostenlose Tools, die Sie online verwenden können, um ein ICO-Bild zu generieren oder ein Bild in dieses Format zu konvertieren.

![Favicon auf der Browser-Registerkarte](./assets/storefront-favicon.png){width="600"}

[!DNL Commerce] unterstützt die folgenden Dateiformate als Favicon:

| Dateiformat | Beschreibung |
|--- |--- |
| ICO | Dieses Bilddateiformat ist für kleine Computersymbolbilder konzipiert. Das ICO-Format wird hauptsächlich unter Microsoft® Windows verwendet und kann Bilder mit einer Auflösung von bis zu 256 x 256 Pixeln sowie 16 Millionen Farben (24 Bit) mit 8 Bit Transparenz enthalten. |
| PNG | (Portable Network Graphics) Diese neuere Alternative zum GIF-Format unterstützt bis zu 16 Millionen Farben (24 Bit). Das verlustfreie Komprimierungsformat erzeugt ein hochwertiges Bitmap-Bild mit klarem Text, aber einer größeren Dateigröße als einige Formate. Das PNG-Format unterstützt transparente Ebenen und wurde für die Online-Anzeige und das Streaming entwickelt. |
| APNG | (Animated Portable Network Graphics) Ein PNG-ähnliches Dateiformat, das einfache Animationen unterstützt. |
| GIF | (Graphics Interchange Format) Ein weit verbreitetes und älteres Bitmap-Format, das auf 256 Farben (8 Bit) beschränkt ist. Das GIF-Format unterstützt einfache Animationen und transparente Ebenen. |
| JPG (JPEG) | (Joint Fotografic Expert Group) Ein komprimiertes Bitmap-Format, das von den meisten Digitalkameras verwendet wird. Die verlustbehaftete Komprimierung verursacht einen gewissen Datenverlust, der sich manchmal als verschwommene Flecken im Text bemerkbar macht. |

{style="table-layout:auto"}

### Schritt 1: Favicon erstellen

1. Erstellen Sie mit dem Bildeditor Ihrer Wahl ein Grafikbild mit 16 x 16 oder 32 x 32 Ihres Logos.

1. (Optional) Verwenden Sie eines der verfügbaren Online-Tools, um die Datei in das .ico-Format zu konvertieren und die Datei auf Ihrem Computer zu speichern.

### Schritt 2: Laden Sie das Favicon in Ihren Store hoch

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Suchen Sie im Raster die Store-Ansicht, die Sie konfigurieren möchten, und klicken Sie in der Spalte _[!UICONTROL Action]_auf **[!UICONTROL Edit]**.

1. Erweitern Sie unter _[!UICONTROL Other Settings]_![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL HTML Head]**.

   ![HTML-Kopfeinstellungen](./assets/configuration-html-head.png){width="600"}

1. Wenn Sie das aktuelle Favicon entfernen möchten, klicken Sie auf das Symbol _Löschen_ (![Papierkorbsymbol](../assets/icon-delete-trashcan.png)) in der linken unteren Ecke des Bildes.

1. Klicken Sie auf **[!UICONTROL Upload]** und öffnen Sie die von Ihnen vorbereitete FAVICON-Datei.

   ![Hochgeladen favicon](./assets/favicon-upload.png){width="400"}

1. Klicken Sie abschließend auf **[!UICONTROL Save Configuration]**.

### Schritt 3: Aktualisieren Sie den Cache

1. Wenn Sie aufgefordert werden, den Cache zu aktualisieren, klicken Sie auf den Link **[!UICONTROL Cache Management]** in der Nachricht oben im Arbeitsbereich.

1. Aktivieren Sie in der Liste das Kontrollkästchen **[!UICONTROL Page Cache]** , das `Invalidated` markiert ist.

1. Legen Sie **[!UICONTROL Actions]** auf `Refresh` fest und klicken Sie auf **[!UICONTROL Submit]**.

1. Um das neue Favicon anzuzeigen, kehren Sie zu Ihrer Storefront zurück und aktualisieren Sie den Browser.

## Ändern der Willkommensnachricht

Die Begrüßungsnachricht in der Kopfzeile wird erweitert und enthält den Namen des Kunden, der angemeldet ist. Achten Sie darauf, vor dem Start Ihres Stores den Standardtext _Willkommen_ für jede Store-Ansicht zu ändern.

![Willkommensnachricht](./assets/storefront-welcome-message.png){width="600"}

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Suchen Sie im Raster die Store-Ansicht, die Sie konfigurieren möchten, und klicken Sie in der Spalte _[!UICONTROL Action]_auf **[!UICONTROL Edit]**.

1. Erweitern Sie unter _[!UICONTROL Other Settings]_![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Header]**.

1. Geben Sie **[!UICONTROL Welcome Text]** den Begrüßungstext ein, der in der Kopfzeile Ihres Stores angezeigt werden soll.

   ![Header-Einstellungen](./assets/configuration-header.png){width="600"}

1. Klicken Sie abschließend auf **[!UICONTROL Save Configuration]**.

1. Wenn Sie aufgefordert werden, den Seiten-Cache zu aktualisieren, klicken Sie auf den Link **[!UICONTROL Cache Management]** oben im Arbeitsbereich und befolgen Sie die Anweisungen zum Aktualisieren des Caches.

## Copyright-Hinweis ändern

In Ihrem Geschäft wird in der Fußzeile jeder Seite ein Copyright-Hinweis angezeigt. Als Best Practice sollte der Copyright-Hinweis das aktuelle Jahr enthalten und Ihr Unternehmen als rechtlichen Eigentümer der Inhalte auf der Website angeben.

![Beispiel für Copyright-Hinweis](./assets/storefront-footer-copyright.png){width="600"}

Der `&copy;`-Code wird verwendet, um das Copyright-Symbol einzufügen, wie in den folgenden Beispielen gezeigt:

- Beispiel für ein langes Format

  `Copyright &copy; 2013-present Luma, Inc. All rights reserved.`

- Beispiel für ein Kurzformat

  `&copy; 2021 Luma, Inc. All rights reserved.`

**_So aktualisieren Sie den Copyright-Hinweis:_**

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Suchen Sie im Raster die Store-Ansicht, die Sie konfigurieren möchten, und klicken Sie in der Spalte _[!UICONTROL Action]_auf **[!UICONTROL Edit]**.

1. Erweitern _unter_ Weitere Einstellungen![ den Abschnitt ](../assets/icon-display-expand.png)Erweiterungsauswahl **[!UICONTROL Footer]**.

   ![Fußzeilen-Design-Einstellungen](./assets/configuration-footer.png){width="600"}

1. Geben Sie **[!UICONTROL Copyright]** den Copyright-Hinweis ein, der in der Fußzeile jeder Seite angezeigt werden soll.

   Verwenden Sie den `&copy;` Zeichencode, um ein Copyright-Symbol einzufügen.

1. Klicken Sie abschließend auf **[!UICONTROL Save Configuration]**.

## Festlegen des Demohinweises für den Store

Wenn Ihr Store online ist, sich aber noch im Aufbau befindet, können Sie oben auf der Seite einen Hinweis zu einer Store-Demo anzeigen, um den Personen mitzuteilen, dass der Store noch nicht für das Geschäft geöffnet ist. Wenn Sie bereit für die _Live-Schaltung_ sind, entfernen Sie einfach die Nachricht. Es ist ähnlich wie das Umdrehen des im Fenster hängenden Schildes von _Geschlossen_ auf _Öffnen_. Das Format der Demo-Benachrichtigung wird durch das Design Ihres Stores bestimmt.

![Hinweis zu Storefront-Demos](./assets/storefront-demo-notice.png){width="600"}

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Suchen Sie im Raster die Store-Ansicht, die Sie konfigurieren möchten, und klicken Sie in der Spalte _[!UICONTROL Action]_auf **[!UICONTROL Edit]**.

1. Erweitern Sie unter _[!UICONTROL Other Settings]_![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL HTML Head]**.

   ![HTML-Kopf](./assets/configuration-html-head.png){width="600"}

1. Scrollen Sie nach unten zum unteren Rand und legen Sie die **[!UICONTROL Display Demo Store Notice]** nach Ihren Wünschen fest.

1. Klicken Sie abschließend auf **[!UICONTROL Save Configuration]**.

1. Wenn Sie aufgefordert werden, den Cache zu aktualisieren, klicken Sie in der Systemmeldung auf **[!UICONTROL Cache Management]** und befolgen Sie die Anweisungen zum Aktualisieren des Caches.
