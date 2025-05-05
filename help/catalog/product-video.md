---
title: Hinzufügen von Produktvideos
description: Erfahren Sie, wie Sie Produktvideos für Ihren Store konfigurieren. Dafür wird ein YouTube-Daten-API-Schlüssel von einem Google-Konto benötigt, und fügen Sie einen Video-Link für ein Produkt hinzu.
exl-id: 0cfcee67-a2e2-41cb-ac70-304452f5db6d
feature: Catalog Management, Products, Media
source-git-commit: e439c1082834cbc81f6ccc7ca99e240d649c8b81
workflow-type: tm+mt
source-wordcount: '656'
ht-degree: 0%

---

# Hinzufügen von Produktvideos

Um ein Produktvideo hinzuzufügen, müssen Sie zunächst einen API-Schlüssel von Ihrem Google-Konto abrufen und ihn in die Konfiguration Ihres Stores eingeben. Anschließend können Sie vom Produkt aus eine Verknüpfung zum Video herstellen.

## Schritt 1: YouTube-API-Schlüssel abrufen

1. Melden Sie sich bei Ihrem Google-Konto an und besuchen Sie die [Google Developers Console][1].

1. Geben Sie oben im Suchfeld `YouTube Data API v3` ein und klicken Sie auf das Suchsymbol.

1. Wenn die API-Seite angezeigt wird, stellen Sie sicher, dass sie aktiviert ist.

1. Wählen Sie im linken Bedienfeld **[!UICONTROL Credentials]** aus.

1. Führen Sie je nachdem, ob Sie über Anmeldeinformationen verfügen oder nicht, einen der folgenden Schritte aus:

   - Wenn Sie bereits über die erforderlichen Anmeldeinformationen verfügen, kopieren Sie den Schlüssel in die Tabelle _API-Schlüssel_ .

   - Wenn Sie noch keine Anmeldeinformationen für diese API haben, klicken Sie oben auf **[!UICONTROL Create Credentials]** und befolgen Sie die Anweisungen zum Erstellen der erforderlichen Anmeldeinformationen. Kopieren _unter &quot;_ abrufen“ den API-Schlüssel und klicken Sie auf **[!UICONTROL Done]**.

1. Kopieren Sie den API-Schlüssel in die Zwischenablage.

1. Klicken Sie auf das Symbol Bearbeiten auf der rechten Seite und legen Sie die Einschränkungen fest, um sicherzustellen, dass der API-Schlüssel auf die richtigen Referrer beschränkt ist.

1. Warten Sie einige Augenblicke, während der Schlüssel generiert wird, und kopieren Sie dann den Schlüssel in die Zwischenablage.

   Im nächsten Schritt fügen Sie den Schlüssel in die Konfiguration Ihres Stores ein.

## Schritt 2: Konfigurieren des Schlüssels in Commerce

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Catalog]** und wählen Sie darunter **[!UICONTROL Catalog]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt _[!UICONTROL Product Video]_&#x200B;und fügen Sie Ihre **[!UICONTROL YouTube API key]**&#x200B;ein.

   ![Konfiguration des Produktvideos](../configuration-reference/catalog/assets/catalog-product-video.png){width="600" zoomable="yes"}

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

1. Aktualisieren Sie bei Aufforderung den Cache.

## Schritt 3: Link zum Video

1. Öffnen Sie ein Produkt im Bearbeitungsmodus.

1. Scrollen Sie zum Abschnitt _[!UICONTROL Images and Videos]_&#x200B;und erweitern Sie ihn.

   ![Bilder und Videos](./assets/product-simple-images-videos.png){width="600" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Add Video]**.

   Wenn Sie Ihren YouTube-API-Schlüssel noch nicht konfiguriert haben, klicken Sie auf **[!UICONTROL OK]** , um fortzufahren. Sie können keine Verknüpfung zu einem YouTube-Video herstellen, aber Sie können den Prozess durchlaufen.

1. Geben Sie **[!UICONTROL Url]** die URL des YouTube- oder Vimeo-Videos ein.

   ![Neues Video für Produkt](./assets/product-video-add.png){width="600" zoomable="yes"}

1. Klicken Sie außerhalb des Felds und warten Sie auf Feedback zum API-Schlüssel oder Video.

   Wenn alles ausgecheckt wird, stellt YouTube Basisinformationen zum Video bereit

1. Geben Sie die **[!UICONTROL Title]** und **[!UICONTROL Description]** des Videos ein.

1. Um ein **[!UICONTROL Preview Image]** hochzuladen, navigieren Sie zum Bild und wählen Sie die Datei aus.

   >[!NOTE]
   >
   >Nach dem Hochladen wird das angezeigte Vorschaubild automatisch von einem externen Videodienstanbieter generiert. Das Bild kann nicht über die Adobe Commerce Admin bearbeitet werden.

1. Wenn Sie die Video-Metadaten lieber verwenden möchten, klicken Sie auf **[!UICONTROL Get Video Information]**.

1. Um zu bestimmen, wie das Video im Store verwendet wird, aktivieren Sie das Kontrollkästchen jedes entsprechenden **[!UICONTROL Role]**:

   - `Base Image`
   - `Small Image`
   - `Swatch Image`
   - `Thumbnail`
   - `Hide from Product Page`

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.

   >[!NOTE]
   >
   >Wenn die _[!UICONTROL Autostart base video]_&#x200B;Konfigurationsoption auf `Yes` festgelegt ist, das Video jedoch nicht automatisch wiedergegeben wird, kann dies an den automatischen Wiedergaberichtlinien liegen, die vom Browser erzwungen werden und nicht von Adobe Commerce gesteuert werden können. Jeder unterstützte Browser verfügt über seine eigenen Richtlinien zur automatischen Wiedergabe, die sich im Laufe der Zeit ändern können, und Ihr Video wird in Zukunft möglicherweise nicht automatisch wiedergegeben. Als Best Practice wird empfohlen, sich nicht auf die automatische Wiedergabe für geschäftskritische Funktionen zu verlassen und das Verhalten der automatischen Videowiedergabe in Ihrem Store mit jedem unterstützten Browser zu testen.

## API-Zugriff verwalten

Gemäß den Google-[ (Nutzungsbedingungen] kann YouTube den API-Zugriff für Konten deaktivieren, die seit mehr als 90 Tagen inaktiv sind. Dieses Ereignis kann dazu führen, dass Ihre Videos nicht angezeigt werden. Um den API-Zugriff auf dem neuesten Stand zu halten, verwenden Sie einen Cron-Auftrag, um die API in regelmäßigen Abständen anzupingen:

```code
30 10 1 * * curl -i -G -e https://yourdomain.com/ -d "part=snippet&maxResults=1&q=test&key=YOUTUBEAPIKEY" https://www.googleapis.com/youtube/v3/search >/dev/null 2>&1
```

## Feldverweis

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL URL] | Die URL des zugehörigen Videos. |
| [!UICONTROL Title] | Der Videotitel. |
| [!UICONTROL Description] | Die Videobeschreibung. |
| [!UICONTROL Preview Image] | Ein hochgeladenes Bild, das als Vorschau des Videos in Ihrem Store verwendet wird. |
| [!UICONTROL Get Video Information] | Ruft die Video-Metadaten ab, die auf dem Host-Server gespeichert sind. Sie können die Originaldaten verwenden oder bei Bedarf aktualisieren. |
| [!UICONTROL Role] | Legt fest, wie das Vorschaubild in Ihrem Store verwendet wird. Sie können eine beliebige Kombination von Optionen auswählen: `Base Image`, `Small Image`, `Thumbnail`, `Swatch Image`, `Hide from Product Page` |

{style="table-layout:auto"}

[1]: https://console.developers.google.com/
[Allgemeine Geschäftsbedingungen]: https://developers.google.com/youtube/terms/developer-policies#d.-accessing-youtube-api-services
