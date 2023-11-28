---
title: Media - Map
description: Erfahren Sie mehr über den Inhaltstyp "Map"zum Hinzufügen einer Zuordnung aus [!DNL Google Maps] Plattform für [!DNL Page Builder] Bühne.
exl-id: 91fea8f8-d48a-43f1-ba2a-212c7130cee9
feature: Page Builder, Page Content
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '1583'
ht-degree: 0%

---

# Media - Map

Verwenden Sie die _Zuordnung_ Inhaltstyp zum Hinzufügen einer Zuordnung aus [[!DNL Google Maps] Plattform][1] der [[!DNL Page Builder] Schritt](workspace.md#stage). Sie können beispielsweise eine Zuordnung zu einem Block hinzufügen und den Block dann zum [Über uns](../content-design/pages.md#about-us) und [Kontakt](../getting-started/store-details.md#contact-us-form) Seiten.

So nutzen Sie das Beste aus [!DNL Google Maps] Platform: Sie können die Zuordnung anpassen, Ihre Speicherorte hervorheben und Google verwenden [Orte][2] um umfassende Informationen zu Ihrem Geschäft zu allen hinzuzufügen [!DNL Google Maps].

## Vorteile der Einbettung einer Google-Karte

1. Bietet Käufern eine umfassende Auswahl an Informationen über Ihr Unternehmen (Telefonnummer, Website, Bewertungen, Sternbewertungen usw.) direkt auf Ihrer Site.

1. Auf einer Google-Karte werden in der Regel Sehenswürdigkeiten, Parks, Restaurants usw. in der Nähe vorgestellt. Diese Informationen helfen Ihren Kunden dabei, Ihren physischen Standort zu bestimmen und ihre Reise zu planen.

1. Dies erleichtert es Kunden, die Adresse für Ihren physischen Speicher zu finden, ohne ein neues Browser-Fenster öffnen und Ihre Website verlassen zu müssen.

1. Wenn Sie über eine Kette von physischen Stores verfügen, hilft das Hinzufügen einer Google-Karte auf Ihrer Site, Ihr Markenbewusstsein und Ihre Glaubwürdigkeit in Form von hervorgehobenen Artikeln zu steigern.

![Beispiel-Storefront - Karte mit Standort](./assets/pb-media-maps-storefront.png){width="700" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Zuordnungs-Tool

Die Zuordnungs-Toolbox wird angezeigt, wenn Sie den Mauszeiger über den Zuordnungscontainer bewegen.

| Tool | Symbol | Beschreibung |
|--- |--- |--- |
| Verschieben | ![Symbol Verschieben](./assets/pb-icon-move.png){width="25"} | Verschiebt die Karte an eine andere Position auf der Bühne. |
| (Titel) | [!UICONTROL Map] | Identifiziert den aktuellen Inhalts-Container als Zuordnung. Bewegen Sie den Mauszeiger über den Zuordnungsbehälter, um die Toolbox anzuzeigen. |
| Einstellungen | ![Symbol Einstellungen](./assets/pb-icon-settings.png){width="25"} | Öffnet die Seite Zuordnung bearbeiten , auf der Sie die Eigenschaften der Zuordnung und des Containers ändern können. |
| Ausblenden | ![Symbol &quot;Ausblenden&quot;](./assets/pb-icon-hide.png){width="25"} | Blendet die aktuelle Karte aus. |
| Anzeigen | ![Symbol &quot;Anzeigen&quot;](./assets/pb-icon-show.png){width="25"} | Zeigt die ausgeblendete Karte an. |
| Duplizieren | ![Symbol &quot;Duplizieren&quot;](./assets/pb-icon-duplicate.png){width="25"} | Kopiert die Karte. |
| Entfernen | ![Symbol &quot;Entfernen&quot;](./assets/pb-icon-remove.png){width="25"} | Löscht die Zuordnung aus der Bühne. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Konfigurieren [!DNL Google Maps] für Ihren Administrator

Bevor Sie eine Zuordnung hinzufügen, müssen Sie zunächst eine [account][3] für einen kostenlosen Prozess von [!DNL Google Maps] Plattform. Die kostenlose Testversion dauert 12 Monate und beinhaltet 300 USD. Wenn Sie Ihr Guthaben in Anspruch nehmen, rechnet Google Ihr Konto nicht ohne Ihre Erlaubnis ab.

### Schritt 1: Herunterladen [!DNL Google Maps] API-Schlüssel

Je nachdem, ob Sie bereits über eine [!DNL Google Maps] verwenden Sie eines der folgenden Verfahren, um den für die Konfiguration erforderlichen API-Schlüssel abzurufen. So richten Sie eine [!DNL Google Maps] eingeben, müssen Sie ein autorisierter Site-Administrator sein, um die Abrechnung für Ihr Konto zu aktivieren. Wenn Sie noch nicht bereit sind, eine [!DNL Google Maps] Platform-Konto können Sie diesen Schritt überspringen und die Platzhalterzuordnung für jetzt verwenden.

1. Navigieren Sie zu [Google Cloud Platform-Konsole](https://cloud.google.com/console/google/maps-apis/overview).

1. Klicken Sie auf das Projekt-Dropdown-Menü und wählen oder erstellen Sie das Projekt, für das Sie einen API-Schlüssel hinzufügen möchten.

1. Um Ihre API-Anmeldeinformationen zu konfigurieren, folgen Sie dem [instructions][4] im [!DNL Google Maps] Dokumentationen.

1. Kopieren Sie Ihren API-Schlüssel in die Zwischenablage.

### Schritt 2: Konfigurieren [!DNL Google Maps] in [!DNL Commerce]

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Im linken Bereich unter _[!UICONTROL General]_auswählen **[!UICONTROL Content Management]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**.

   ![Erweiterte Inhaltswerkzeuge](../configuration-reference/general/assets/content-management-advanced-content-tools.png){width="600" zoomable="yes"}

   Weitere Informationen zu den Konfigurationsoptionen für erweiterte Content Management-Tools finden Sie in der [Konfigurationshandbuch](../configuration-reference/general/content-management.md).

1. Für **[!UICONTROL Google Maps API Key]**, fügen Sie den Schlüssel ein, den Sie in Schritt 1 kopiert haben.

1. Klicken **[!UICONTROL Test Key]**.

   Wenn ein Problem mit Ihrem Schlüssel vorliegt, kehren Sie zum [!DNL Google Maps] Plattform-Site zur Lösung des Problems. Versuchen Sie es dann erneut.

1. Nachdem Ihr Schlüssel verifiziert wurde, klicken Sie auf **[!UICONTROL Save Config]**.

## Hinzufügen einer Karte zur Bühne

1. Öffnen Sie die Seite, den Baustein oder den dynamischen Baustein in der [!DNL Page Builder] Arbeitsbereich.

1. Im [!DNL Page Builder] Bedienfeld, erweitern **[!UICONTROL Media]** und ziehen Sie eine **[!UICONTROL Map]** Platzhalter zur Bühne.

   ![Ziehen einer Karte auf die Bühne](./assets/pb-media-map-drag.png){width="600" zoomable="yes"}

   Wenn [!DNL Google Maps] Platform für Ihren Store konfiguriert ist, wird eine Zuordnung für Ihren Store-Speicherort angezeigt.

   ![[!DNL Google Maps]](./assets/pb-tutorial2-google-map.png){width="600" zoomable="yes"}

   Wenn [!DNL Google Maps] Platform noch nicht für Ihren Store konfiguriert ist, wird stattdessen eine Platzhalterzuordnung angezeigt.

   ![[!DNL Google Maps] Platzhalter](./assets/pb-tutorial2-media-map-not-configured.png){width="600" zoomable="yes"}

## Hinzufügen eines benutzerdefinierten Zuordnungsstandorts

1. Bewegen Sie den Mauszeiger über den Map-Container, um die Toolbox anzuzeigen und die _Einstellungen_ ( ![Symbol Einstellungen](./assets/pb-icon-settings.png){width="20"} ).

1. In der oberen rechten Ecke der _[!UICONTROL Edit Map]_Seite, klicken **[!UICONTROL Add Location]**.

1. Geben Sie die **[!UICONTROL Location Name]** die Sie mit dem Pin auf der Karte verknüpfen möchten.

1. Erfassen Sie die Standortkoordinaten, die Sie für den benutzerdefinierten Speicherort verwenden möchten.

   Alternativ können Sie in der **[!UICONTROL Position]** können Sie den Stift in die angezeigte Karte ziehen.

   Gehen Sie bei Bedarf zu [[!DNL Google Maps]][5] in einem neuen Browserfenster verwenden und eine der folgenden Methoden verwenden, um die Koordinaten abzurufen:

   ![Map Coordinates](./assets/pb-media-maps-settings-add-location-coordinates.png){width="600" zoomable="yes"}

   **Methode 1:** Aus URL kopieren

   - Geben Sie in der linken oberen Ecke die Adresse in das Feld **[!UICONTROL Search]** und klicken Sie auf _Suche_ ( ![Suchsymbol](../assets/icon-magnify-search.png){width="20"} ).

   - Kopieren Sie die Koordinaten in der URL und fügen Sie sie in ein Notebook ein.

   **Methode 2:** Kopie von &quot;Was ist hier?&quot;

   - Klicken Sie mit der rechten Maustaste auf den roten Pin, der die Position auf der Karte markiert, und wählen Sie **[!UICONTROL What's here?]** im Menü.

   - Kopieren Sie in der angezeigten Beschriftung den Text, einschließlich der Koordinaten, und fügen Sie den Text in ein Notizblock ein.

1. Geben Sie in jedem der **[!UICONTROL Coordinates]** Boxen.

   Sie können auch so viele der restlichen Informationen eingeben, die Sie auf der Karte zur Verfügung haben möchten.

1. Füllen Sie alle weiteren Informationen aus, die Sie mit dem Zuordnungsspeicherort verknüpfen möchten:

   | Option | Beschreibung |
   | ------ | ----------- |
   | [!UICONTROL Phone Number] | Die Telefonnummer des Standorts. |
   | [!UICONTROL Street Address] | Die Straßenadresse des Standorts. |
   | [!UICONTROL City] | Die Stadt des Standorts. |
   | [!UICONTROL Region/State] | Die Region oder der Status des Standorts. |
   | [!UICONTROL Zip/Postal Code] | Die Postleitzahl des Standorts. |
   | [!UICONTROL Country] | Das Land des Standorts. |
   | [!UICONTROL Comment] | Alle Kommentare, die Sie einbeziehen möchten. |

   {style="table-layout:auto"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]**.

   Die neue Position wird auf der Karte und im Raster für die Zuordnungsposition auf der Karte angezeigt _[!UICONTROL Edit Map]_Seite.

   ![[!DNL Page Builder] - Zuordnungsspeichergitter](./assets/pb-media-maps-settings-add-location-grid.png){width="600" zoomable="yes"}

## Zuordnung formatieren {#styling}

Verwenden Sie die [!DNL Google Maps] Assistent für den Plattformstil , um ein von sechs vordefinierten Designs anzuwenden oder ein benutzerdefiniertes Design zu erstellen. Sie können eine JSON-Datei mit den Eigenschaften des Zuordnungsstils oder einen Link zur formatierten Zuordnung generieren.

### Ändern des Zuordnungsstils

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Im linken Bereich unter _[!UICONTROL General]_auswählen **[!UICONTROL Content Management]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**.

1. Unter dem **[!UICONTROL Google Maps Style]** Textfeld, klicken Sie auf [Kartenstil erstellen][6].

   Diese Aktion öffnet die [[!DNL Google Maps] Assistent für die Platform-Formatierung][6] auf einer separaten Registerkarte, auf der Sie einen Stil für Ihre [!DNL Google Maps] Plattform-Projekt.

1. Klicks **[!UICONTROL Create a Style]** und befolgen Sie die angegebenen Anweisungen.

   Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Finish]**.

1. Exportieren Sie den abgeschlossenen Stil als JSON-Code oder als URL, damit Sie ihn zum [!DNL Commerce] Konfiguration.

   - **JSON**: Klicken Sie unter dem Feld mit dem generierten JSON-Code auf **[!UICONTROL Copy JSON]**.

   - **[!UICONTROL URL]**: Klicken Sie unter dem Feld mit der generierten URL auf **[!UICONTROL Copy URL]**.

1. Kehren Sie zur Registerkarte Ihres Admin-Browsers zurück und fügen Sie den generierten Code oder die URL in die **Stil von Google Maps** ankreuzen.

   Wenn Sie eine URL verwenden, ersetzen Sie die `YOUR_API_KEY` Platzhalter mit Ihrem [!DNL Google Maps] API-Schlüssel. Diese URL verweist auf Ihre formatierte Google Map.

1. Klicken Sie oben rechts auf **[!UICONTROL Save Config]**.

### Ändern der Zuordnungseinstellungen

1. Bewegen Sie den Mauszeiger über den Zuordnungsbehälter, um das Tool-Feld anzuzeigen und die _Einstellungen_ ( ![Symbol Einstellungen](./assets/pb-icon-settings.png){width="20"} ).

1. Ändern Sie die grundlegenden Einstellungen nach Bedarf:

   | Option | Beschreibung |
   | ------ | ----------- |
   | [!UICONTROL Height] | Gibt die Höhe der angezeigten Karte in Pixel an. |
   | [!UICONTROL Show Controls] | Bestimmt, ob die standardmäßigen Google Map-Steuerelemente angezeigt werden. |

   {style="table-layout:auto"}

1. Ändern Sie die _[!UICONTROL Advanced]_Einstellungen nach Bedarf:

   - Um die horizontale Positionierung des Zuordnungsinhalts zu steuern, der dem Container hinzugefügt wird, wählen Sie eine **[!UICONTROL Alignment]**:

     | Option | Beschreibung |
     | ------ | ----------- |
     | `Default` | Wendet die Standardeinstellung für die Ausrichtung an, die im Stylesheet des aktuellen Designs angegeben ist. |
     | `Left` | Richtet den Inhalt am linken Rand des Map-Containers aus, wobei der angegebene Abstand berücksichtigt wird. |
     | `Center` | Richtet den Inhalt in der Mitte des Map-Containers aus, wobei der angegebene Abstand berücksichtigt wird. |
     | `Right` | Richtet den Inhalt am rechten Rand des Map-Containers aus, wobei der angegebene Abstand berücksichtigt wird. |

     {style="table-layout:auto"}

   - Legen Sie die **[!UICONTROL Border]** Stil angewendet auf alle vier Seiten des Map-Containers:

     | Option | Beschreibung |
     | ------ | ----------- |
     | `Default` | Wendet den standardmäßigen Randstil an, der vom zugehörigen Stylesheet angegeben wird. |
     | `None` | liefert keine sichtbare Anzeige der Containergrenzen. |
     | `Dotted` | Der Container-Rahmen wird als gepunktete Linie angezeigt. |
     | `Dashed` | Der Container-Rahmen wird als gestrichelte Linie angezeigt. |
     | `Solid` | Der Container-Rahmen wird als durchgehende Linie angezeigt. |
     | `Double` | Der Container-Rahmen wird als doppelte Linie angezeigt. |
     | `Groove` | Der Container-Rahmen wird als Rillenlinie angezeigt. |
     | `Ridge` | Der Container-Rahmen wird als gekürzte Linie angezeigt. |
     | `Inset` | Der Container-Rahmen wird als Inset-Zeile angezeigt. |
     | `Outset` | Der Container-Rahmen wird als Ausgangspunkt angezeigt. |

     {style="table-layout:auto"}

   - Wenn Sie einen anderen Rahmenstil als `None`, füllen Sie die Randanzeigeoptionen aus:

     ![Rahmenfarbe](./assets/pb-settings-border-color.png){width="600" zoomable="yes"}

     | Option | Beschreibung |
     | ------ |------------ |
     | [!UICONTROL Border Color] | Geben Sie die Farbe an, indem Sie ein Muster auswählen, auf die Farbauswahl klicken oder einen gültigen Farbnamen oder einen entsprechenden Hexadezimalwert eingeben. |
     | [!UICONTROL Border Width] | Geben Sie die Anzahl Pixel für die Rahmenlinienbreite an. |
     | [!UICONTROL Border Radius] | Geben Sie die Anzahl der Pixel an, um die die Größe des Radius definiert wird, mit dem die einzelnen Ecken des Rands gerundet werden. |

     {style="table-layout:auto"}

   - (Optional) Geben Sie die Namen von **[!UICONTROL CSS classes]** aus dem aktuellen Stylesheet, das auf den Zuordnungscontainer angewendet werden soll.

     Trennen Sie mehrere Klassennamen durch ein Leerzeichen.

   - Geben Sie Werte in Pixel für die **[!UICONTROL Margins and Padding]** um die äußeren Ränder und den inneren Abstand des Kartencontainers anzugeben.

     Geben Sie jeden entsprechenden Wert in das Zuordnungsbehälterdiagramm ein.

     | Container-Bereich | Beschreibung |
     | -------------- | ----------- |
     | [!UICONTROL Margins] | Die Menge an leerem Raum, die auf den äußeren Rand aller Seiten des Containers angewendet wird. |
     | [!UICONTROL Padding] | Die Menge an leerem Raum, die auf den inneren Rand aller Seiten des Containers angewendet wird. |

     {style="table-layout:auto"}

     >[!NOTE]
     >
     >Der Abstand ist für den Inhaltstyp Zuordnung nicht verfügbar.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]** , um die Einstellungen anzuwenden und zum [!DNL Page Builder] Arbeitsbereich.

### Rastergröße ändern

Die Rastergröße bestimmt die Größe der Karte, die sich auf eine [column](column.md) auf [!DNL Page Builder] Bühne. Standardmäßig ist die Karte 12 Spalten breit, mit maximal 16 Spalten.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Im linken Bereich unter _[!UICONTROL General]_auswählen **[!UICONTROL Content Management]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**.

1. Aktualisieren Sie die Rasteroptionen nach Bedarf:

   >[!NOTE]
   >
   >Falls erforderlich, löschen Sie die **[!UICONTROL Use system value]** aktivieren, um diese Einstellungen zu ändern.

   - Für **[!UICONTROL Default Column Grid Size]**, geben Sie einen neuen Wert für die Standardgröße des Rasters ein.

   - Für **[!UICONTROL Maximum Column Grid Size]**, geben Sie einen neuen Wert für die standardmäßige maximale Rastergröße ein.

   ![Größeneinstellungen des Spalten-Rasters](./assets/pb-configure-advanced-content-tools-grid-size.png){width="600" zoomable="yes"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

[1]: https://cloud.google.com/maps-platform/
[2]: https://cloud.google.com/maps-platform/places/
[3]: https://cloud.google.com/maps-platform/user-guide/
[4]: https://developers.google.com/maps/documentation/javascript/get-api-key
[5]: https://www.google.com/maps
[6]: https://mapstyle.withgoogle.com/
