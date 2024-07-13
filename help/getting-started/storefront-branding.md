---
title: Storefront-Branding
description: Erfahren Sie, wie Sie die Elemente ändern, die die Markenidentität Ihres Stores definieren.
exl-id: 91630717-9da7-4d2f-a0d8-adb794a30ee1
feature: Storefront
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '1309'
ht-degree: 0%

---

# Storefront-Branding

Als Erstes sollten Sie [das Logo](#upload-your-logo) in der Kopfzeile ändern und [eine Favicon](#add-a-favicon) für den Browser hochladen. Als Nächstes sollten Sie [Ihre Willkommensnachricht hinzufügen](#change-the-welcome-message) und [den Copyright-Hinweis](#change-the-copyright-notice) in der Fußzeile aktualisieren. Diese Aufgaben sind ein paar einfache Designelemente, die Sie sofort erledigen können. Während Ihr Store in Entwicklung ist, können Sie [den Demohinweis zum Store aktivieren](#set-the-store-demo-notice) und ihn dann entfernen, wenn Sie bereit zum Starten sind.

![Branding-Elemente der Storefront](./assets/storefront-home-page-branding.png){width="600" zoomable="yes"}

## Logo hochladen

Die Größe und Position des Logos in der Kopfzeile wird durch das Store-Design bestimmt. Ihr Logo kann entweder als GIF-, PNG- oder JPG-Dateityp (JPEG) gespeichert und vom Administrator Ihres Stores hochgeladen werden.

![Logo in Kopfzeile](./assets/storefront-header-logo.png){width="600"}

Das Logo-Bild befindet sich am folgenden Speicherort auf dem Server. Jede Bilddatei mit dem Namen &quot;`logo.svg`&quot; wird als Standard-Design-Logo verwendet.

Vollständiger Pfad - `app/design/frontend/[vendor]/[theme]/web/images/logo.svg`

Relativer Pfad - `images/logo.svg`

Wenn Sie die Größe des Logos oder anderer im Design verwendeter Bilder nicht kennen, öffnen Sie die Seite in einem Browser, klicken Sie mit der rechten Maustaste auf das Bild und überprüfen Sie das Element.

>[!NOTE]
>
>Zusätzlich zum Logo in der Kopfzeile erscheint Ihr Logo auch auf [E-Mail-Vorlagen](../systems/email-templates.md#prepare-your-email-logo) und auf [PDF-Rechnungen](../stores-purchase/sales-documents.md) und anderen Verkaufsdokumenten. Die Logos für E-Mail-Vorlagen und Rechnungen haben unterschiedliche Größen und müssen separat hochgeladen werden.

Unterstützte Logodateiformate:

| Dateiformat | Beschreibung |
|--- |--- |
| PNG | (Portable Network Graphics) Diese neuere Alternative zum GIF-Format unterstützt bis zu 16 Millionen Farben (24 Bit). Das verlustfreie Komprimierungsformat liefert ein hochwertiges Bitmap-Bild mit scharfem Text, jedoch eine größere Dateigröße als einige Formate. Das PNG-Format unterstützt transparente Ebenen und ist für die Online-Anzeige und das Streaming konzipiert. |
| GIF | (Graphics Interchange Format) Ein weithin unterstütztes und älteres Bitmap-Format, das auf 256 Farben (8 Bit) begrenzt ist. Das GIF-Format unterstützt einfache Animationen und transparente Ebenen. |
| JPG (JPEG) | (Joint Fotografic Expert Group) Ein komprimiertes Bitmap-Format, das von den meisten Digitalkameras verwendet wird. Die verlustreiche Komprimierung führt zu Datenverlust, der manchmal als unscharfe Flecken im Text wahrgenommen werden kann. |

{style="table-layout:auto"}

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

   ![Seite &quot;Designkonfiguration&quot;](./assets/design-configuration.png){width="700"}

1. Suchen Sie die Store-Ansicht, die Sie konfigurieren möchten, und klicken Sie in der Spalte _[!UICONTROL Action]_auf **[!UICONTROL Edit]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Header]** .

   ![Kopfzeileneinstellungen](./assets/configuration-header.png){width="600"}

1. Um ein neues Logo hochzuladen, klicken Sie auf **[!UICONTROL Upload]** und wählen Sie die Datei aus Ihrem System aus.

1. Geben Sie die Werte **[!UICONTROL Logo Image Width]** und **[!UICONTROL Logo Image Height]** in Pixel ein.

1. Geben Sie für **[!UICONTROL Logo Image Alt]** den Text ein, der angezeigt werden soll, wenn der Mauszeiger über das Bild bewegt wird.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Configuration]**.

## Favicon hinzufügen

_Favicon_ ist die Abkürzung für _Lieblingssymbol_ und verweist auf das kleine Symbol auf der Registerkarte jeder Browser-Seite. Je nach Browser wird die Favicon auch in der Adressleiste direkt vor der URL angezeigt.

Ein Favicon ist in der Regel 16 x 16 Pixel oder 32 x 32 Pixel groß. [!DNL Commerce] akzeptiert die Dateitypen ICO, PNG, APNG, GIF und JPG (JPEG), obwohl nicht alle Browser diese Formate unterstützen. Das am weitesten unterstützte Dateiformat für eine Favicon ist ICO. Sie können andere Bilddateitypen verwenden, das Format wird jedoch möglicherweise nicht von allen Browsern unterstützt. Es gibt viele kostenlose Tools, die Sie verwenden können, um ein ICO-Bild zu erstellen oder ein Bild in dieses Format zu konvertieren.

![Favicon auf der Browser-Registerkarte](./assets/storefront-favicon.png){width="600"}

[!DNL Commerce] unterstützt die folgenden Dateiformate als Favicon:

| Dateiformat | Beschreibung |
|--- |--- |
| ICO | Dieses Bilddateiformat wurde für kleine Computersymbolbilder entwickelt. Das ICO-Format, das hauptsächlich unter Microsoft® Windows OS verwendet wird, kann Bilder mit bis zu 256 x 256 Pixel und 16 Millionen Farben (24 Bit) mit 8 Bit Transparenz enthalten. |
| PNG | (Portable Network Graphics) Diese neuere Alternative zum GIF-Format unterstützt bis zu 16 Millionen Farben (24 Bit). Das verlustfreie Komprimierungsformat liefert ein hochwertiges Bitmap-Bild mit scharfem Text, jedoch eine größere Dateigröße als einige Formate. Das PNG-Format unterstützt transparente Ebenen und ist für die Online-Anzeige und das Streaming konzipiert. |
| APNG | (Animierte Portable Network Graphics) Ein Dateiformat ähnlich dem PNG, das einfache Animationen unterstützt. |
| GIF | (Graphics Interchange Format) Ein weithin unterstütztes und älteres Bitmap-Format, das auf 256 Farben (8 Bit) begrenzt ist. Das GIF-Format unterstützt einfache Animationen und transparente Ebenen. |
| JPG (JPEG) | (Joint Fotografic Expert Group) Ein komprimiertes Bitmap-Format, das von den meisten Digitalkameras verwendet wird. Die verlustreiche Komprimierung führt zu Datenverlust, der manchmal als unscharfe Flecken im Text wahrgenommen werden kann. |

{style="table-layout:auto"}

### Schritt 1: Erstellen einer Funktion

1. Erstellen Sie mit dem Bildeditor Ihrer Wahl ein 16 x 16- oder 32 x 32-Bildbild Ihres Logos.

1. (Optional) Verwenden Sie eines der verfügbaren Online-Tools, um die Datei in das .ico-Format zu konvertieren und die Datei auf Ihrem Computer zu speichern.

### Schritt 2: Hochladen der Funktion in Ihren Speicher

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Suchen Sie im Raster die Store-Ansicht, die Sie konfigurieren möchten, und klicken Sie in der Spalte _[!UICONTROL Action]_auf **[!UICONTROL Edit]**.

1. Erweitern Sie unter _[!UICONTROL Other Settings]_den Abschnitt ![Erweiterungsauswahl](../assets/icon-display-expand.png) um den Abschnitt **[!UICONTROL HTML Head]**.

   ![HTML-Head-Einstellungen](./assets/configuration-html-head.png){width="600"}

1. Wenn Sie die aktuelle Favicon entfernen möchten, klicken Sie in der linken unteren Ecke des Bildes auf das Symbol _Löschen_ (![Papierkorbsymbol](../assets/icon-delete-trashcan.png)).

1. Klicken Sie auf **[!UICONTROL Upload]** und öffnen Sie die von Ihnen vorbereitete Favicon-Datei.

   ![Hochgeladenes Favicon](./assets/favicon-upload.png){width="400"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Configuration]**.

### Schritt 3: Cache aktualisieren

1. Wenn Sie aufgefordert werden, den Cache zu aktualisieren, klicken Sie in der Meldung oben im Arbeitsbereich auf den Link **[!UICONTROL Cache Management]** .

1. Wählen Sie in der Liste das Kontrollkästchen **[!UICONTROL Page Cache]** aus, das mit `Invalidated` markiert ist.

1. Setzen Sie **[!UICONTROL Actions]** auf `Refresh` und klicken Sie auf **[!UICONTROL Submit]**.

1. Um die neue Favicon anzuzeigen, kehren Sie zu Ihrer Storefront zurück und aktualisieren Sie den Browser.

## Willkommensnachricht ändern

Die Willkommensnachricht in der Kopfzeile wird um den Namen des Kunden erweitert, der angemeldet ist. Stellen Sie vor dem Start Ihres Stores sicher, dass Sie den standardmäßigen Text _Willkommen_ für jede Store-Ansicht ändern.

![Willkommensnachricht](./assets/storefront-welcome-message.png){width="600"}

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Suchen Sie im Raster die Store-Ansicht, die Sie konfigurieren möchten, und klicken Sie in der Spalte _[!UICONTROL Action]_auf **[!UICONTROL Edit]**.

1. Erweitern Sie unter _[!UICONTROL Other Settings]_den Abschnitt ![Erweiterungsauswahl](../assets/icon-display-expand.png) um den Abschnitt **[!UICONTROL Header]**.

1. Geben Sie für &quot;**[!UICONTROL Welcome Text]**&quot;den Begrüßungstext ein, der in der Kopfzeile Ihres Stores angezeigt werden soll.

   ![Kopfzeileneinstellungen](./assets/configuration-header.png){width="600"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Configuration]**.

1. Wenn Sie aufgefordert werden, den Seiten-Cache zu aktualisieren, klicken Sie oben im Arbeitsbereich auf den Link **[!UICONTROL Cache Management]** und befolgen Sie die Anweisungen zum Aktualisieren des Caches.

## Urheberrechtshinweis ändern

Ihr Store zeigt in der Fußzeile jeder Seite einen Copyright-Hinweis an. Als Best Practice sollte der Urheberrechtshinweis das aktuelle Jahr enthalten und Ihr Unternehmen als rechtmäßigen Eigentümer des Inhalts der Website identifizieren.

![Beispiel für Copyright-Hinweis](./assets/storefront-footer-copyright.png){width="600"}

Der Code des Zeichens `&copy;` wird zum Einfügen des Copyright-Symbols verwendet, wie in den folgenden Beispielen gezeigt:

- Beispiel für ein langes Format

  `Copyright &copy; 2013-present Luma, Inc. All rights reserved.`

- Beispiel für ein kurzes Format

  `&copy; 2021 Luma, Inc. All rights reserved.`

**_Aktualisieren des Copyright-Vermerks:_**

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Suchen Sie im Raster die Store-Ansicht, die Sie konfigurieren möchten, und klicken Sie in der Spalte _[!UICONTROL Action]_auf **[!UICONTROL Edit]**.

1. Erweitern Sie unter _Andere Einstellungen_ den Abschnitt ![Erweiterungsauswahl](../assets/icon-display-expand.png)für den Abschnitt **[!UICONTROL Footer]**.

   ![Fußzeilendesign-Einstellungen](./assets/configuration-footer.png){width="600"}

1. Geben Sie für &quot;**[!UICONTROL Copyright]**&quot;den Copyright-Hinweis ein, der in der Fußzeile jeder Seite angezeigt werden soll.

   Verwenden Sie den Code des Zeichens `&copy;` , um ein Copyright-Symbol einzufügen.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Configuration]**.

## Festlegen des Demohinweises zum Store

Wenn Ihr Store online ist, sich aber noch im Aufbau befindet, können Sie oben auf der Seite einen Demohinweis zum Geschäft anzeigen, um den Benutzern mitzuteilen, dass der Store noch nicht für Unternehmen geöffnet ist. Wenn Sie bereit sind, _live zu gehen_, entfernen Sie einfach die Nachricht. Sie ähnelt dem Spiegeln des im Fenster hängenden Zeichens von _Geschlossen_ in _Öffnen_. Das Format des Demohinweises wird durch das Design Ihres Stores bestimmt.

![Demohinweis zur Storefront](./assets/storefront-demo-notice.png){width="600"}

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. Suchen Sie im Raster die Store-Ansicht, die Sie konfigurieren möchten, und klicken Sie in der Spalte _[!UICONTROL Action]_auf **[!UICONTROL Edit]**.

1. Erweitern Sie unter _[!UICONTROL Other Settings]_den Abschnitt ![Erweiterungsauswahl](../assets/icon-display-expand.png) um den Abschnitt **[!UICONTROL HTML Head]**.

   ![HTML head](./assets/configuration-html-head.png){width="600"}

1. Scrollen Sie nach unten nach unten und legen Sie die **[!UICONTROL Display Demo Store Notice]** auf Ihre Voreinstellung fest.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Configuration]**.

1. Wenn Sie aufgefordert werden, den Cache zu aktualisieren, klicken Sie in der Systemmeldung auf **[!UICONTROL Cache Management]** und befolgen Sie die Anweisungen zum Aktualisieren des Caches.
