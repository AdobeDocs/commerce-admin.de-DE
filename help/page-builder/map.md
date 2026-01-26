---
title: Medien - Zuordnung
description: Erfahren Sie mehr über den Inhaltstyp „Zuordnen“, der zum Hinzufügen einer Zuordnung von  [!DNL Google Maps]  zu der  [!DNL Page Builder]  verwendet wird.
exl-id: 91fea8f8-d48a-43f1-ba2a-212c7130cee9
feature: Page Builder, Page Content
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '1572'
ht-degree: 0%

---

# Medien - Zuordnung

Verwenden Sie den _Map_-Inhaltstyp, um eine Zuordnung von [[!DNL Google Maps] Platform](https://cloud.google.com/maps-platform/) zur [[!DNL Page Builder] Phase](workspace.md#stage) hinzuzufügen. Sie können beispielsweise eine Karte zu einem Block hinzufügen und dann den Block zu den Seiten [Über uns](../content-design/pages.md#about-us) und [Kontakt](../getting-started/store-details.md#contact-us-form) hinzufügen.

Um [!DNL Google Maps] Platform optimal zu nutzen, können Sie die -Karte anpassen, Ihre Store-Standorte hervorheben und Google [Places](https://cloud.google.com/maps-platform/places/) verwenden, um allen [!DNL Google Maps] umfangreiche Informationen über Ihren Store hinzuzufügen.

## Vorteile der Einbettung einer Google-Karte

1. Bietet Käufern eine vollständige Palette von Informationen über Ihr Unternehmen (Telefonnummer, Website, Bewertungen, Sternebewertungen usw.) direkt auf Ihrer Website.

1. Eine Google-Karte zeigt normalerweise die nahe gelegenen Sehenswürdigkeiten, Parks, Restaurants und so weiter. Diese Informationen helfen Ihren Kunden, Ihren physischen Standort zu bestimmen und ihre Reise zu planen.

1. Erleichtert es Kunden, die Adresse für Ihren physischen Speicher zu finden, ohne ein neues Browser-Fenster zu öffnen und Ihre Website zu verlassen.

1. Wenn Sie über eine Kette von physischen Geschäften verfügen, trägt das Hinzufügen einer Google-Karte auf Ihrer Site dazu bei, Ihre Markenbekanntheit und Glaubwürdigkeit in Form von hervorgehobenen Artikeln zu erhöhen.

![Beispiel einer Storefront - Zuordnung mit Standort](./assets/pb-media-maps-storefront.png){width="700" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Zuordnungs-Toolbox

Die Zuordnungs-Toolbox wird angezeigt, wenn Sie den Mauszeiger über den Zuordnungs-Container bewegen.

| Tool | Symbol | Beschreibung |
|--- |--- |--- |
| Verschieben | ![move icon](./assets/pb-icon-move.png){width="25"} | Verschiebt die Karte an eine andere Position auf der Bühne. |
| (Bezeichnung) | [!UICONTROL Map] | Identifiziert den aktuellen Inhalts-Container als Zuordnung. Bewegen Sie den Mauszeiger über den Map-Container, um die Toolbox anzuzeigen. |
| Einstellungen | ![Einstellungssymbol](./assets/pb-icon-settings.png){width="25"} | Öffnet die Seite Zuordnung bearbeiten , auf der Sie die Eigenschaften der Zuordnung und des Containers ändern können. |
| Ausblenden | ![Symbol ausblenden](./assets/pb-icon-hide.png){width="25"} | Blendet die aktuelle Zuordnung aus. |
| Anzeigen | ![Symbol anzeigen](./assets/pb-icon-show.png){width="25"} | Zeigt die ausgeblendete Karte an. |
| Duplikat | ![Symbol „Duplizieren“](./assets/pb-icon-duplicate.png){width="25"} | Erstellt eine Kopie der Karte. |
| entfernen | ![Symbol entfernen](./assets/pb-icon-remove.png){width="25"} | Löscht die Karte aus der Phase. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Konfigurieren von [!DNL Google Maps] für Ihren Administrator

Bevor Sie eine Karte hinzufügen, müssen Sie zunächst ein [Konto](https://cloud.google.com/maps-platform/user-guide/) für eine kostenlose Testversion von [!DNL Google Maps] Platform öffnen. Die kostenlose Testversion dauert 12 Monate und beinhaltet eine Gutschrift von 300 $. Wenn Sie Ihr Guthaben aufbrauchen, stellt Google Ihr Konto nicht ohne Ihre Erlaubnis in Rechnung.

### Schritt 1: [!DNL Google Maps]-API-Schlüssel abrufen

Je nachdem, ob Sie bereits über einen [!DNL Google Maps] verfügen, können Sie mit einem der folgenden Verfahren den für die Konfiguration erforderlichen API-Schlüssel abrufen. Um einen [!DNL Google Maps] Schlüssel einzurichten, müssen Sie ein Site-Administrator sein, der befugt ist, die Abrechnung für Ihr Konto zu aktivieren. Wenn Sie noch nicht bereit sind, ein [!DNL Google Maps] Platform-Konto einzurichten, können Sie diesen Schritt überspringen und die Platzhalterzuordnung für den Moment verwenden.

1. Wechseln Sie zur [Google Cloud Platform-Konsole](https://cloud.google.com/console/google/maps-apis/overview).

1. Klicken Sie auf die Dropdown-Liste Projekt und wählen oder erstellen Sie das Projekt, für das Sie einen API-Schlüssel hinzufügen möchten.

1. Um Ihre API-Anmeldeinformationen zu konfigurieren, befolgen Sie die [Anweisungen](https://developers.google.com/maps/documentation/javascript/get-api-key) in den [!DNL Google Maps].

1. Kopieren Sie Ihren API-Schlüssel in die Zwischenablage.

### Schritt 2: Konfigurieren von [!DNL Google Maps] in [!DNL Commerce]

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wählen Sie im linken Bedienfeld unter _[!UICONTROL General]_die Option **[!UICONTROL Content Management]**aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**.

   ![Erweiterte Inhalts-Tools](../configuration-reference/general/assets/content-management-advanced-content-tools.png){width="600" zoomable="yes"}

   Weitere Informationen zu den Konfigurationsoptionen für die erweiterten Content-Management-Tools finden Sie [ „Konfigurationshandbuch](../configuration-reference/general/content-management.md).

1. Fügen Sie **[!UICONTROL Google Maps API Key]** den in Schritt 1 kopierten Schlüssel ein.

1. Klicken Sie auf **[!UICONTROL Test Key]**.

   Wenn es ein Problem mit Ihrem Schlüssel gibt, kehren Sie zur [!DNL Google Maps] Platform-Site zurück, um das Problem zu beheben. Versuchen Sie es dann erneut.

1. Nachdem der Schlüssel überprüft wurde, klicken Sie auf **[!UICONTROL Save Config]**.

## Dem Stadium eine Karte hinzufügen

1. Öffnen Sie die Seite, den Block oder den dynamischen Block im [!DNL Page Builder] Workspace.

1. Erweitern Sie im [!DNL Page Builder] Bedienfeld **[!UICONTROL Media]** und ziehen Sie einen **[!UICONTROL Map]** Platzhalter auf das Bühnenbild.

   ![Ziehen einer Karte auf die Bühne](./assets/pb-media-map-drag.png){width="600" zoomable="yes"}

   Wenn [!DNL Google Maps] Platform für Ihren Store konfiguriert ist, wird eine Zuordnung für Ihren Store-Standort angezeigt.

   ![[!DNL Google Maps]](./assets/pb-tutorial2-google-map.png){width="600" zoomable="yes"}

   Wenn [!DNL Google Maps] Platform noch nicht für Ihren Store konfiguriert ist, wird stattdessen eine Platzhalterzuordnung angezeigt.

   ![[!DNL Google Maps] Platzhalter](./assets/pb-tutorial2-media-map-not-configured.png){width="600" zoomable="yes"}

## Benutzerdefinierte Map-Position hinzufügen

1. Bewegen Sie den Mauszeiger über den Zuordnungs-Container, um die Toolbox anzuzeigen, und wählen _das Symbol_ Einstellungen![ ( (](./assets/pb-icon-settings.png){width="20"}) aus.

1. Klicken Sie oben rechts auf der _[!UICONTROL Edit Map]_auf **[!UICONTROL Add Location]**.

1. Geben Sie die **[!UICONTROL Location Name]** ein, die mit der Nadel auf der Karte verknüpft werden soll.

1. Erfassen Sie die Standortkoordinaten, die Sie für den benutzerdefinierten Standort verwenden möchten.

   Alternativ können Sie den Pin auch in das **[!UICONTROL Position]** ziehen.

   Wechseln Sie bei Bedarf zu [[!DNL Google Maps]](https://www.google.com/maps) in einem neuen Browser-Fenster und verwenden Sie eine der folgenden Methoden, um die Koordinaten abzurufen:

   ![Koordinaten zuordnen](./assets/pb-media-maps-settings-add-location-coordinates.png){width="600" zoomable="yes"}

   **Methode 1:** aus URL kopieren

   - Geben Sie in der oberen linken Ecke die Adresse in das **[!UICONTROL Search]** ein und klicken Sie auf das Symbol _Suchen_ ( ![Suchsymbol](../assets/icon-magnify-search.png){width="20"} ).

   - Kopieren Sie die Koordinaten in der URL und fügen Sie sie in ein Notizbuch ein.

   **Methode 2:** Kopie aus „Was ist hier?“

   - Klicken Sie mit der rechten Maustaste auf den roten Pin, der die Position auf der Karte markiert, und wählen Sie **[!UICONTROL What's here?]** im Menü.

   - Kopieren Sie den Text einschließlich der Koordinaten in das angezeigte Label und fügen Sie ihn in ein Notizbuch ein.

1. Geben Sie die Zahlen ohne Komma in jedes **[!UICONTROL Coordinates]** ein.

   Sie können auch so viele der restlichen Informationen eingeben, wie Sie auf der Karte verfügbar sein möchten.

1. Geben Sie alle weiteren Informationen ein, die Sie mit der Kartenposition verknüpfen möchten:

   | Option | Beschreibung |
   | ------ | ----------- |
   | [!UICONTROL Phone Number] | Die Telefonnummer des Standorts. |
   | [!UICONTROL Street Address] | Die Straßenadresse des Standorts. |
   | [!UICONTROL City] | Die Stadt der Lage. |
   | [!UICONTROL Region/State] | Die Region oder der Status des Standorts. |
   | [!UICONTROL Zip/Postal Code] | Die Postleitzahl des Standorts. |
   | [!UICONTROL Country] | Das Land des Standorts. |
   | [!UICONTROL Comment] | Alle Kommentare, die Sie einbeziehen möchten. |

   {style="table-layout:auto"}

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.

   Der neue Ort wird auf der Karte und im Map-Standortraster auf der _[!UICONTROL Edit Map]_angezeigt.

   ![[!DNL Page Builder] - Karten Standortraster](./assets/pb-media-maps-settings-add-location-grid.png){width="600" zoomable="yes"}

## Gestalten der Zuordnung {#styling}

Verwenden Sie den [!DNL Google Maps] Platform-Stilassistenten, um eines von sechs vordefinierten Designs anzuwenden oder ein benutzerdefiniertes Design zu erstellen. Sie können eine JSON-Datei mit den Eigenschaften des Zuordnungsstils oder einen Link zur formatierten Zuordnung generieren.

### Ändern des Zuordnungsstils

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wählen Sie im linken Bedienfeld unter _[!UICONTROL General]_die Option **[!UICONTROL Content Management]**aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**.

1. Klicken Sie unter dem Textfeld **[!UICONTROL Google Maps Style]** auf [Zuordnungsstil erstellen](https://mapstyle.withgoogle.com/).

   Diese Aktion öffnet den [[!DNL Google Maps] Platform-Formatierungsassistenten](https://mapstyle.withgoogle.com/) auf einer separaten Registerkarte, auf der Sie einen Stil für Ihr [!DNL Google Maps] Platform-Projekt definieren können.

1. Klicken Sie auf **[!UICONTROL Create a Style]** und folgen Sie den Anweisungen.

   Klicken Sie abschließend auf **[!UICONTROL Finish]**.

1. Exportieren Sie den fertigen Stil als JSON-Code oder als URL, damit Sie ihn der [!DNL Commerce]-Konfiguration hinzufügen können.

   - **JSON**: Klicken Sie unter dem Feld mit dem generierten JSON-Code auf **[!UICONTROL Copy JSON]**.

   - **[!UICONTROL URL]**: Klicken Sie unter dem Feld mit der generierten URL auf **[!UICONTROL Copy URL]**.

1. Kehren Sie zu Ihrer Admin-Browser-Registerkarte zurück und fügen Sie den generierten Code oder die URL in das Feld **Google Maps Style** ein.

   Wenn Sie eine URL verwenden, ersetzen Sie den `YOUR_API_KEY` Platzhalter durch Ihren [!DNL Google Maps] API-Schlüssel. Diese URL verweist auf Ihre formatierte Google-Zuordnung.

1. Klicken Sie oben rechts auf **[!UICONTROL Save Config]**.

### Ändern der Zuordnungseinstellungen

1. Bewegen Sie den Mauszeiger über den Zuordnungs-Container, um das Toolbox anzuzeigen, und wählen Sie das Symbol _Einstellungen_ ( ![Einstellungssymbol](./assets/pb-icon-settings.png){width="20"} ) aus.

1. Ändern Sie die Grundeinstellungen nach Bedarf:

   | Option | Beschreibung |
   | ------ | ----------- |
   | [!UICONTROL Height] | Gibt die Höhe der angezeigten Zuordnung in Pixel an. |
   | [!UICONTROL Show Controls] | Legt fest, ob die standardmäßigen Google-Zuordnungssteuerelemente angezeigt werden. |

   {style="table-layout:auto"}

1. Ändern Sie die _[!UICONTROL Advanced]_nach Bedarf:

   - Um die horizontale Positionierung des Zuordnungsinhalts zu steuern, der zum Container hinzugefügt wurde, wählen Sie eine **[!UICONTROL Alignment]** aus:

     | Option | Beschreibung |
     | ------ | ----------- |
     | `Default` | Wendet die Standardeinstellung für die Ausrichtung an, die im Stylesheet des aktuellen Designs angegeben ist. |
     | `Left` | Richtet den Inhalt am linken Rand des Zuordnungs-Containers aus, wobei ein beliebiger Abstand berücksichtigt wird. |
     | `Center` | Richtet den Inhalt in der Mitte des Zuordnungs-Containers aus, wobei ein beliebiger Abstand berücksichtigt wird. |
     | `Right` | Richtet den Inhalt am rechten Rand des Zuordnungs-Containers aus, wobei ein beliebiger Abstand berücksichtigt wird. |

     {style="table-layout:auto"}

   - Legen Sie den **[!UICONTROL Border]** fest, der auf alle vier Seiten des Zuordnungs-Containers angewendet werden soll:

     | Option | Beschreibung |
     | ------ | ----------- |
     | `Default` | Wendet die Standardformatvorlage für Rahmen an, die im zugehörigen Stylesheet angegeben ist. |
     | `None` | Zeigt keine sichtbaren Begrenzungen des Containers an. |
     | `Dotted` | Der Container-Rahmen wird als gepunktete Linie angezeigt. |
     | `Dashed` | Der Container-Rahmen wird als gestrichelte Linie angezeigt. |
     | `Solid` | Der Container-Rahmen wird als durchgezogene Linie angezeigt. |
     | `Double` | Der Container-Rahmen wird als doppelte Linie angezeigt. |
     | `Groove` | Der Container-Rahmen wird als gerillte Linie angezeigt. |
     | `Ridge` | Der Container-Rahmen wird als geriffelte Linie angezeigt. |
     | `Inset` | Der Container-Rahmen wird als Einfügelinie angezeigt. |
     | `Outset` | Der Container-Rahmen wird als Ausgangslinie angezeigt. |

     {style="table-layout:auto"}

   - Wenn Sie einen anderen Rahmenstil als `None` festlegen, müssen Sie die Anzeigeoptionen für den Rahmen vervollständigen:

     ![Rahmenfarbe](./assets/pb-settings-border-color.png){width="600" zoomable="yes"}

     | Option | Beschreibung |
     | ------ |------------ |
     | [!UICONTROL Border Color] | Geben Sie die Farbe an, indem Sie einen Musterabschnitt auswählen, auf die Farbauswahl klicken oder einen gültigen Farbnamen oder einen entsprechenden Hexadezimalwert eingeben. |
     | [!UICONTROL Border Width] | Geben Sie die Anzahl der Pixel für die Rahmenlinienbreite ein. |
     | [!UICONTROL Border Radius] | Geben Sie die Anzahl der Pixel ein, um die Größe des Radius festzulegen, mit dem jede Ecke des Rahmens gerundet werden soll. |

     {style="table-layout:auto"}

   - (Optional) Geben Sie die Namen der **[!UICONTROL CSS classes]** aus dem aktuellen Stylesheet an, die auf den Zuordnungs-Container angewendet werden sollen.

     Trennen Sie mehrere Klassennamen durch ein Leerzeichen.

   - Geben Sie Werte in Pixeln für die **[!UICONTROL Margins and Padding]** ein, um die äußeren Ränder und den inneren Abstand des Zuordnungs-Containers anzugeben.

     Geben Sie jeden entsprechenden Wert im Zuordnungs-Container-Diagramm ein.

     | Container-Bereich | Beschreibung |
     | -------------- | ----------- |
     | [!UICONTROL Margins] | Die Menge des Leerraums, der auf die Außenkante aller Seiten des Containers angewendet wird. |
     | [!UICONTROL Padding] | Die Menge des Leerraums, der auf die Innenkante aller Seiten des Containers angewendet wird. |

     {style="table-layout:auto"}

     >[!NOTE]
     >
     >Auffüllung ist für den Inhaltstyp Zuordnung nicht verfügbar.

1. Klicken Sie abschließend auf **[!UICONTROL Save]** , um die Einstellungen anzuwenden und zum Arbeitsbereich [!DNL Page Builder] zurückzukehren.

### Ändern der Rastergröße

Die Rastergröße bestimmt die Größe der Zuordnung in Bezug auf eine [Spalte](column.md) auf der [!DNL Page Builder]. Standardmäßig ist die Zuordnung 12 Spalten breit, mit maximal 16 Spalten.

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wählen Sie im linken Bedienfeld unter _[!UICONTROL General]_die Option **[!UICONTROL Content Management]**aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**.

1. Aktualisieren Sie die Rasteroptionen nach Bedarf:

   >[!NOTE]
   >
   >Deaktivieren Sie bei Bedarf das Kontrollkästchen **[!UICONTROL Use system value]** , um diese Einstellungen zu ändern.

   - Geben Sie **[!UICONTROL Default Column Grid Size]** einen neuen Wert für die Standardgröße des Rasters ein.

   - Geben Sie **[!UICONTROL Maximum Column Grid Size]** einen neuen Wert für die standardmäßige maximale Rastergröße ein.

   ![Einstellungen für die Größe des Spaltenrasters](./assets/pb-configure-advanced-content-tools-grid-size.png){width="600" zoomable="yes"}

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.


<!-- Last updated from includes: 2023-09-11 14:30:19 -->
