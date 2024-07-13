---
title: Media - Map
description: Erfahren Sie mehr über den Inhaltstyp Zuordnung , mit dem eine Zuordnung von  [!DNL Google Maps] Plattform zur [!DNL Page Builder] Bühne hinzugefügt wird.
exl-id: 91fea8f8-d48a-43f1-ba2a-212c7130cee9
feature: Page Builder, Page Content
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '1571'
ht-degree: 0%

---

# Media - Map

Verwenden Sie den Inhaltstyp _Zuordnung_ , um der [[!DNL Page Builder] Bühne](workspace.md#stage) eine Zuordnung von [[!DNL Google Maps] Plattform][1] hinzuzufügen. Sie können beispielsweise einem Block eine Zuordnung hinzufügen und den Block dann den Seiten [Über uns](../content-design/pages.md#about-us) und [Kontakt](../getting-started/store-details.md#contact-us-form) hinzufügen.

Um das Beste aus der [!DNL Google Maps]-Plattform zu erhalten, können Sie die Karte anpassen, Ihre Speicherorte hervorheben und Google [Places][2] verwenden, um allen [!DNL Google Maps] umfassende Informationen über Ihren Store hinzuzufügen.

## Vorteile der Einbettung einer Google-Karte

1. Bietet Käufern eine umfassende Auswahl an Informationen über Ihr Unternehmen (Telefonnummer, Website, Bewertungen, Sternbewertungen usw.) direkt auf Ihrer Site.

1. Auf einer Google-Karte werden in der Regel Sehenswürdigkeiten, Parks, Restaurants usw. in der Nähe vorgestellt. Diese Informationen helfen Ihren Kunden dabei, Ihren physischen Standort zu bestimmen und ihre Reise zu planen.

1. Dies erleichtert es Kunden, die Adresse für Ihren physischen Speicher zu finden, ohne ein neues Browser-Fenster öffnen und Ihre Website verlassen zu müssen.

1. Wenn Sie über eine Kette von physischen Stores verfügen, hilft das Hinzufügen einer Google-Karte auf Ihrer Site, Ihr Markenbewusstsein und Ihre Glaubwürdigkeit in Form von hervorgehobenen Artikeln zu steigern.

![Beispiel-Storefront - Zuordnung mit Position](./assets/pb-media-maps-storefront.png){width="700" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Zuordnungs-Tool

Die Zuordnungs-Toolbox wird angezeigt, wenn Sie den Mauszeiger über den Zuordnungscontainer bewegen.

| Tool | Symbol | Beschreibung |
|--- |--- |--- |
| Verschieben | ![Symbol &quot;Verschieben&quot;](./assets/pb-icon-move.png){width="25"} | Verschiebt die Karte an eine andere Position auf der Bühne. |
| (Titel) | [!UICONTROL Map] | Identifiziert den aktuellen Inhalts-Container als Zuordnung. Bewegen Sie den Mauszeiger über den Zuordnungsbehälter, um die Toolbox anzuzeigen. |
| Einstellungen | ![Einstellungssymbol](./assets/pb-icon-settings.png){width="25"} | Öffnet die Seite Zuordnung bearbeiten , auf der Sie die Eigenschaften der Zuordnung und des Containers ändern können. |
| Ausblenden | ![Symbol zum Ausblenden](./assets/pb-icon-hide.png){width="25"} | Blendet die aktuelle Karte aus. |
| Anzeigen | ![Symbol &quot;Anzeigen&quot;](./assets/pb-icon-show.png){width="25"} | Zeigt die ausgeblendete Karte an. |
| Duplizieren | ![Symbol &quot;Duplizieren&quot;](./assets/pb-icon-duplicate.png){width="25"} | Kopiert die Karte. |
| Entfernen | ![Symbol &quot;Entfernen&quot;](./assets/pb-icon-remove.png){width="25"} | Löscht die Zuordnung aus der Bühne. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Konfigurieren Sie [!DNL Google Maps] für Ihren Admin

Bevor Sie eine Zuordnung hinzufügen, müssen Sie zunächst ein [Konto][3] für eine kostenlose Testversion von [!DNL Google Maps] Platform öffnen. Die kostenlose Testversion dauert 12 Monate und beinhaltet 300 USD. Wenn Sie Ihr Guthaben in Anspruch nehmen, rechnet Google Ihr Konto nicht ohne Ihre Erlaubnis ab.

### Schritt 1: Abrufen des [!DNL Google Maps]-API-Schlüssels

Je nachdem, ob Sie bereits über einen [!DNL Google Maps] -Schlüssel verfügen, verwenden Sie eine der folgenden Vorgehensweisen, um den für die Konfiguration erforderlichen API-Schlüssel abzurufen. Um einen [!DNL Google Maps] -Schlüssel einzurichten, müssen Sie ein Site-Administrator sein, der zur Aktivierung der Abrechnung für Ihr Konto berechtigt ist. Wenn Sie noch nicht bereit sind, ein [!DNL Google Maps] Platform-Konto einzurichten, können Sie diesen Schritt überspringen und die Platzhalterzuordnung für den Moment verwenden.

1. Wechseln Sie zur [Google Cloud Platform Console](https://cloud.google.com/console/google/maps-apis/overview).

1. Klicken Sie auf das Projekt-Dropdown-Menü und wählen oder erstellen Sie das Projekt, für das Sie einen API-Schlüssel hinzufügen möchten.

1. Um Ihre API-Anmeldeinformationen zu konfigurieren, befolgen Sie die [Anweisungen][4] in der [!DNL Google Maps] -Dokumentation.

1. Kopieren Sie Ihren API-Schlüssel in die Zwischenablage.

### Schritt 2: Konfigurieren Sie [!DNL Google Maps] in [!DNL Commerce]

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wählen Sie im linken Bereich unter _[!UICONTROL General]_die Option **[!UICONTROL Content Management]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**.

   ![Erweiterte Content-Tools](../configuration-reference/general/assets/content-management-advanced-content-tools.png){width="600" zoomable="yes"}

   Weitere Informationen zu den Konfigurationsoptionen für die erweiterten Werkzeuge für Content Management finden Sie im [Konfigurationshandbuch](../configuration-reference/general/content-management.md).

1. Fügen Sie für **[!UICONTROL Google Maps API Key]** den Schlüssel ein, den Sie in Schritt 1 kopiert haben.

1. Klicken Sie auf **[!UICONTROL Test Key]**.

   Wenn ein Problem mit Ihrem Schlüssel auftritt, kehren Sie zur Platform-Site &quot;[!DNL Google Maps]&quot;zurück, um das Problem zu beheben. Versuchen Sie es dann erneut.

1. Nachdem Ihr Schlüssel verifiziert wurde, klicken Sie auf **[!UICONTROL Save Config]**.

## Hinzufügen einer Karte zur Bühne

1. Öffnen Sie die Seite, den Block oder den dynamischen Block im Arbeitsbereich [!DNL Page Builder] .

1. Erweitern Sie im Bedienfeld [!DNL Page Builder] den Wert **[!UICONTROL Media]** und ziehen Sie einen Platzhalter **[!UICONTROL Map]** auf die Bühne.

   ![Ziehen einer Zuordnung zur Bühne](./assets/pb-media-map-drag.png){width="600" zoomable="yes"}

   Wenn [!DNL Google Maps] Platform für Ihren Store konfiguriert ist, wird eine Zuordnung für Ihren Store-Speicherort angezeigt.

   ![[!DNL Google Maps]](./assets/pb-tutorial2-google-map.png){width="600" zoomable="yes"}

   Wenn [!DNL Google Maps] Platform noch nicht für Ihren Store konfiguriert ist, wird stattdessen eine Platzhalterzuordnung angezeigt.

   ![[!DNL Google Maps] Platzhalter](./assets/pb-tutorial2-media-map-not-configured.png){width="600" zoomable="yes"}

## Hinzufügen eines benutzerdefinierten Zuordnungsstandorts

1. Bewegen Sie den Mauszeiger über den Zuordnungsbehälter, um die Toolbox anzuzeigen, und wählen Sie das Symbol _Einstellungen_ ( ![Einstellungssymbol](./assets/pb-icon-settings.png){width="20"} ).

1. Klicken Sie in der rechten oberen Ecke der Seite _[!UICONTROL Edit Map]_auf **[!UICONTROL Add Location]**.

1. Geben Sie den **[!UICONTROL Location Name]** ein, der mit dem Pin auf der Karte verknüpft werden soll.

1. Erfassen Sie die Standortkoordinaten, die Sie für den benutzerdefinierten Speicherort verwenden möchten.

   Alternativ können Sie im Feld &quot;**[!UICONTROL Position]**&quot; den Pin auf die angezeigte Karte ziehen.

   Wechseln Sie bei Bedarf in einem neuen Browserfenster zu [[!DNL Google Maps]][5] und verwenden Sie eine der folgenden Methoden, um die Koordinaten abzurufen:

   ![Zuordnungskoordinaten](./assets/pb-media-maps-settings-add-location-coordinates.png){width="600" zoomable="yes"}

   **Methode 1:** Kopie von URL

   - Geben Sie oben links die Adresse in das Feld **[!UICONTROL Search]** ein und klicken Sie auf das Symbol _Suchen_ ( ![Suchsymbol](../assets/icon-magnify-search.png){width="20"} ).

   - Kopieren Sie die Koordinaten in der URL und fügen Sie sie in ein Notebook ein.

   **Methode 2:** Kopie von &quot;Was ist hier?&quot;

   - Klicken Sie mit der rechten Maustaste auf den roten Pin, der die Position auf der Karte markiert, und wählen Sie im Menü **[!UICONTROL What's here?]** aus.

   - Kopieren Sie in der angezeigten Beschriftung den Text, einschließlich der Koordinaten, und fügen Sie den Text in ein Notizblock ein.

1. Geben Sie die Zahlen ohne Komma in die einzelnen **[!UICONTROL Coordinates]**-Felder ein.

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

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]**.

   Die neue Position wird auf der Karte und im Raster für die Zuordnungsposition auf der Seite _[!UICONTROL Edit Map]_angezeigt.

   ![[!DNL Page Builder] - ordnet das Positionsraster](./assets/pb-media-maps-settings-add-location-grid.png){width="600" zoomable="yes"} zu

## Zuordnung formatieren {#styling}

Verwenden Sie den Assistenten für Plattformstile, um ein von sechs vordefinierten Designs anzuwenden oder ein benutzerdefiniertes Design zu erstellen. [!DNL Google Maps] Sie können eine JSON-Datei mit den Eigenschaften des Zuordnungsstils oder einen Link zur formatierten Zuordnung generieren.

### Ändern des Zuordnungsstils

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wählen Sie im linken Bereich unter _[!UICONTROL General]_die Option **[!UICONTROL Content Management]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**.

1. Klicken Sie unter dem Textfeld **[!UICONTROL Google Maps Style]** auf [Zuordnungsstil erstellen][6].

   Durch diese Aktion wird der [[!DNL Google Maps] Assistent für die Platform-Formatierung][6] auf einer separaten Registerkarte geöffnet, auf der Sie einen Stil für Ihr [!DNL Google Maps] Platform-Projekt definieren können.

1. Klicken Sie auf **[!UICONTROL Create a Style]** und befolgen Sie die angegebenen Anweisungen.

   Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Finish]**.

1. Exportieren Sie den abgeschlossenen Stil als JSON-Code oder als URL, damit Sie ihn zur [!DNL Commerce] -Konfiguration hinzufügen können.

   - **JSON**: Klicken Sie unter dem Feld mit dem generierten JSON-Code auf **[!UICONTROL Copy JSON]**.

   - **[!UICONTROL URL]**: Klicken Sie unter dem Feld mit der generierten URL auf **[!UICONTROL Copy URL]**.

1. Kehren Sie zur Registerkarte Ihres Admin-Browsers zurück und fügen Sie den generierten Code oder die URL in das Feld **Google Maps Style** ein.

   Wenn Sie eine URL verwenden, ersetzen Sie den Platzhalter `YOUR_API_KEY` durch Ihren API-Schlüssel [!DNL Google Maps] . Diese URL verweist auf Ihre formatierte Google Map.

1. Klicken Sie in der oberen rechten Ecke auf **[!UICONTROL Save Config]**.

### Ändern der Zuordnungseinstellungen

1. Bewegen Sie den Mauszeiger über den Zuordnungsbehälter, um das Tool-Feld anzuzeigen, und wählen Sie das Symbol _Einstellungen_ ( ![Einstellungssymbol](./assets/pb-icon-settings.png){width="20"} ).

1. Ändern Sie die grundlegenden Einstellungen nach Bedarf:

   | Option | Beschreibung |
   | ------ | ----------- |
   | [!UICONTROL Height] | Gibt die Höhe der angezeigten Karte in Pixel an. |
   | [!UICONTROL Show Controls] | Bestimmt, ob die standardmäßigen Google Map-Steuerelemente angezeigt werden. |

   {style="table-layout:auto"}

1. Ändern Sie die Einstellungen für _[!UICONTROL Advanced]_nach Bedarf:

   - Um die horizontale Positionierung des Zuordnungsinhalts zu steuern, der dem Container hinzugefügt wird, wählen Sie einen **[!UICONTROL Alignment]**:

     | Option | Beschreibung |
     | ------ | ----------- |
     | `Default` | Wendet die Standardeinstellung für die Ausrichtung an, die im Stylesheet des aktuellen Designs angegeben ist. |
     | `Left` | Richtet den Inhalt am linken Rand des Map-Containers aus, wobei der angegebene Abstand berücksichtigt wird. |
     | `Center` | Richtet den Inhalt in der Mitte des Map-Containers aus, wobei der angegebene Abstand berücksichtigt wird. |
     | `Right` | Richtet den Inhalt am rechten Rand des Map-Containers aus, wobei der angegebene Abstand berücksichtigt wird. |

     {style="table-layout:auto"}

   - Legen Sie den **[!UICONTROL Border]** -Stil fest, der auf alle vier Seiten des Zuordnungscontainers angewendet wird:

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

   - Wenn Sie einen anderen Rahmenstil als `None` festlegen, füllen Sie die Anzeigeoptionen für die Rahmenanzeige aus:

     ![Rahmenfarbe](./assets/pb-settings-border-color.png){width="600" zoomable="yes"}

     | Option | Beschreibung |
     | ------ |------------ |
     | [!UICONTROL Border Color] | Geben Sie die Farbe an, indem Sie ein Muster auswählen, auf die Farbauswahl klicken oder einen gültigen Farbnamen oder einen entsprechenden Hexadezimalwert eingeben. |
     | [!UICONTROL Border Width] | Geben Sie die Anzahl Pixel für die Rahmenlinienbreite an. |
     | [!UICONTROL Border Radius] | Geben Sie die Anzahl der Pixel an, um die die Größe des Radius definiert wird, mit dem die einzelnen Ecken des Rands gerundet werden. |

     {style="table-layout:auto"}

   - (Optional) Geben Sie die Namen von **[!UICONTROL CSS classes]** aus dem aktuellen Stylesheet an, das auf den Zuordnungscontainer angewendet werden soll.

     Trennen Sie mehrere Klassennamen durch ein Leerzeichen.

   - Geben Sie Werte in Pixel an, damit der **[!UICONTROL Margins and Padding]** die äußeren Ränder und den inneren Abstand des Zuordnungscontainers angibt.

     Geben Sie jeden entsprechenden Wert in das Zuordnungsbehälterdiagramm ein.

     | Container-Bereich | Beschreibung |
     | -------------- | ----------- |
     | [!UICONTROL Margins] | Die Menge an leerem Raum, die auf den äußeren Rand aller Seiten des Containers angewendet wird. |
     | [!UICONTROL Padding] | Die Menge an leerem Raum, die auf den inneren Rand aller Seiten des Containers angewendet wird. |

     {style="table-layout:auto"}

     >[!NOTE]
     >
     >Der Abstand ist für den Inhaltstyp Zuordnung nicht verfügbar.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]** , um die Einstellungen anzuwenden und zum Arbeitsbereich [!DNL Page Builder] zurückzukehren.

### Rastergröße ändern

Die Rastergröße bestimmt die Größe der Karte, die sich auf eine [Spalte](column.md) auf der [!DNL Page Builder]-Bühne bezieht. Standardmäßig ist die Karte 12 Spalten breit, mit maximal 16 Spalten.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wählen Sie im linken Bereich unter _[!UICONTROL General]_die Option **[!UICONTROL Content Management]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**.

1. Aktualisieren Sie die Rasteroptionen nach Bedarf:

   >[!NOTE]
   >
   >Deaktivieren Sie bei Bedarf das Kontrollkästchen **[!UICONTROL Use system value]** , um diese Einstellungen zu ändern.

   - Geben Sie für **[!UICONTROL Default Column Grid Size]** einen neuen Wert für die Standardgröße des Rasters ein.

   - Geben Sie für **[!UICONTROL Maximum Column Grid Size]** einen neuen Wert für die standardmäßige maximale Rastergröße ein.

   ![Einstellungen für die Spaltenrastergröße](./assets/pb-configure-advanced-content-tools-grid-size.png){width="600" zoomable="yes"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

[1]: https://cloud.google.com/maps-platform/
[2]: https://cloud.google.com/maps-platform/places/
[3]: https://cloud.google.com/maps-platform/user-guide/
[4]: https://developers.google.com/maps/documentation/javascript/get-api-key
[5]: https://www.google.com/maps
[6]: https://mapstyle.withgoogle.com/
