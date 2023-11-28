---
title: Konfigurieren des Distance Priority-Algorithmus
description: Legen Sie die Konfiguration für den Vergleich des Standorts der Versandzieladresse mit den Quellspeicherorten fest, um die nächstgelegene Quelle für die Erfüllung von Sendungen zu bestimmen.
exl-id: 4dec179a-25ac-48db-a84b-4974798272b0
feature: Inventory, Configuration
source-git-commit: 023716935a6657b0dc2317876debe608e65bf010
workflow-type: tm+mt
source-wordcount: '834'
ht-degree: 0%

---

# Konfigurieren des Distance Priority-Algorithmus

Der Entfernungsprioritätenalgorithmus vergleicht den Speicherort der Lieferzieladresse mit den Quellspeicherorten, um die nächstgelegene Quelle für die Durchführung von Sendungen zu bestimmen. Die Entfernung kann anhand von Daten aus der Datenbank oder von Fahren, Spaziergängen oder Fahrradfahrten von einem Ort zum anderen bestimmt werden. Verwenden Sie diese [Quellauswahlalgorithmus](selection-reservations.md) , um die nächstgelegene Quelle den Versandzieladressen zu empfehlen.

>[!NOTE]
>
>Wenn Sie den Distance Priority Algorithm verwenden, geben Sie die vollständige Straßenadresse und GPS-Koordinaten für Ihre [sources](sources-add.md) wird empfohlen.

Sie haben zwei Möglichkeiten, die Entfernung und die Zeit zu berechnen, um die nächstgelegene Quelle für die Erfüllung des Versands zu ermitteln:

- **GOOGLE MAP** - Verwendungszwecke [Google Maps-Plattform][1] Dienste zur Berechnung der Entfernung und der Zeit zwischen der Lieferadresse und den Quellstandorten. Diese Option verwendet den Breiten- und Längengrad (GPS-Koordinaten) der Quelle und kann die Straßenadresse je nach Berechnungsmodus verwenden. Ein Google-API-Schlüssel ist erforderlich für [Geocoding API][2] und [Entfernungsmatrix-API][3] aktiviert ist, können Gebühren über Google anfallen.

- **Offline-Berechnung** - Berechnet die Entfernung mithilfe von heruntergeladenen und importierten Geocode-Daten mithilfe von Postleitzahlen und GPS-Koordinaten, um die nächstgelegene Quelle für die Lieferzieladresse zu bestimmen. Um diese Option zu konfigurieren, benötigen Sie möglicherweise Hilfe von Entwicklern, um Geocodes zunächst mithilfe von Befehlszeilenanweisungen herunterzuladen und zu importieren.

>[!NOTE]
>
>Für Websites mit mehreren Stores mit mehreren Ländern konfigurieren Sie die [Standardsteuerziel](../stores-purchase/tax-class.md#default-tax-destination){target="_blank"} für jedes Land.

## Verwenden von Google-Maps

Sie benötigen zum Einstieg kein Google-Konto. Der Prozess umfasst bei Bedarf die Erstellung von Google-Konten und -Projekten. Diese Option erfordert ein Rechnungskonto und eine Zahlungsmethode, die Ihrem Google-Konto hinzugefügt werden, um Konfigurationen abzuschließen und den Algorithmus zu verwenden.
Es wird jedoch empfohlen, den entfernungsbasierten Algorithmus von Google MAP im Vergleich zur Offline-Berechnung weiter auszubauen und präziser zu gestalten.

### Schritt 1: Erstellen des Google-API-Schlüssels

Der Schlüssel stammt aus dem [Google Maps-Plattform][1] und sollten [Geocoding API][2] und [Entfernungsmatrix-API][3] aktiviert. Weitere Informationen finden Sie unter [Konfigurieren des Distance Priority-Algorithmus](distance-priority-algorithm.md).

1. Besuch [Google Maps-Plattform][1] und klicken **[!UICONTROL Get Started]**.

1. Um die Plattform zu aktivieren, wählen Sie **[!UICONTROL Maps, Routes, and Places]** und klicken **[!UICONTROL Continue]**.

   ![Google Maps-Plattform für Ihren Schlüssel](assets/inventory-google-key1.png){width="350" zoomable="yes"}

1. Melden Sie sich mit einem Google-Konto an oder erstellen Sie ein Konto.

1. Einrichten eines Projekts:

   - Wählen Sie ein Projekt aus oder geben Sie einen neuen Projektnamen ein.

   - Um die Bedingungen zu akzeptieren, wählen Sie `Yes`.

   - Klicken **[!UICONTROL Next]**.

1. Geben Sie ein Abrechnungskonto ein oder erstellen Sie eines. Sie können das Rechnungskonto überspringen und später hinzufügen.

   Für die Verwendung dieses Dienstes ist ein Rechnungskonto erforderlich.

1. Klicken Sie zum Öffnen und Konfigurieren Ihrer Google Cloud Platform-Optionen auf **[!UICONTROL Console]**.

   - Öffnen Sie Ihr Projekt.

   - Erweitern Sie das Menü und klicken Sie auf **[!UICONTROL APIs & Services]** > **[!UICONTROL Library]**.

     ![Google API-Dienste](assets/inventory-google-key2.png){width="350" zoomable="yes"}

   - Suchen Sie nach [Geocoding API][2] und [Entfernungsmatrix-API][3]. Wählen Sie die einzelnen Dienste aus und aktivieren Sie sie.

1. Erweitern Sie das Menü und klicken Sie auf **[!UICONTROL APIs & Services]** > **[!UICONTROL Credentials]** und kopieren Sie den Google-API-Schlüssel.

   ![Google API-Schlüsselkopie](assets/inventory-google-key3.png){width="350" zoomable="yes"}

### Schritt 2: Konfigurieren des Google MAP-Anbieters

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Catalog]** und wählen **[!UICONTROL Inventory]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die _[!UICONTROL Distance Provider for Distance Based SSA]_Abschnitt und Satz **[!UICONTROL Provider]**nach `Google MAP`.

   ![Anbieter von Fernabsatz-SSA](assets/config-catalog-inventory-distance-provider.png){width="350" zoomable="yes"}

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die _[!UICONTROL Google Distance Provider]_und konfigurieren Sie die Einstellungen:

   - Für **[!UICONTROL Google API Key]** Geben Sie den Schlüssel ein, der aus Ihrem Google-Konto kopiert wurde.

   - Für **[!UICONTROL Computation mode]**, wählen Sie eine Konfiguration aus.

     >[!NOTE]
     >
     >Wenn dieser Algorithmus für den Versand verwendet wird und Routen und Daten nicht für den ausgewählten Berechnungsmodus (Fahren, Fahren, Fahren oder Gehen) für eine Sendung zurückgegeben werden, verwendet die SSA standardmäßig die Quellpriorität. Festlegen der [Priorität für Quellen je Bestand](stocks-prioritize-sources.md) wird empfohlen.

     | Option | Beschreibung |
     | ----- | ----- |
     | `Driving` | (Standard) Fordert Standardfahrtanweisungen über das Straßennetz an. |
     | `Walking` | Wünsche für Wanderungen mit Fußgängerwegen und Bürgersteigen (sofern verfügbar). |
     | `Bicycling` | Erkundigen Sie sich über Fahrradwege und bevorzugte Straßen (sofern verfügbar). Die [Distance Matrix-Dienst][4] ist nur in den USA und einigen kanadischen Städten verfügbar. |

   - Für **[!UICONTROL Value]** einen Werttyp auswählen:

     | Option | Beschreibung |
     | ----- | ----- |
     | `Distance` | (Standard) Gibt die Entfernung zwischen Punkten in Metriken (Kilometer und Meter) oder dem Kaiserreich (Meilen und Fuß) zurück. |
     | `Time to Destination` | Gibt die erforderliche Zeit zurück, um von den Quell-Standorten in Stunden und Minuten zur Lieferadresse zu gelangen. |

   ![Google Distance Provider](assets/config-catalog-inventory-distance-provider-settings.png){width="350" zoomable="yes"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

## Offline-Berechnung verwenden

Offline-Berechnungen verwenden Ländercodes, um den Abstand zwischen dem Versandziel und den Quelladressen zu ermitteln. Diese Option erfordert möglicherweise Hilfe von Entwicklern bei der Konfiguration. Verwenden Sie eine [!DNL Inventory Management] CLI-Befehl zum Herunterladen und Importieren von Daten aus [geonames.org][5].

>[!NOTE]
>
>Importierte Geocodes von [geonames.org][5] Für einige Länder wie Kanada und Irland gelten Beschränkungen. Siehe Abschnitt [GeoNames Postleitzahl-Dateien][6] für weitere Informationen.

### Schritt 1: Herunterladen und Importieren von Geocodes

Vollständige Befehlszeilenkonfiguration zum Herunterladen und Importieren von Geocode-Ländern zum Versand an und zur Verwendung von Quellspeicherorten. Dieser Schritt erfordert möglicherweise Hilfe von Entwicklern für Hilfe bei Befehlszeilenaufgaben. Siehe Abschnitt [Importieren von Geocodes](cli.md#import-geocodes).

Führen Sie diese Befehle jedes Mal aus, wenn Sie weitere Geocodes hinzufügen möchten.

### Schritt 2: Berechnung festlegen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Catalog]** und wählen **[!UICONTROL Inventory]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die _[!UICONTROL Distance Provider for Distance Based SSA]_Abschnitt.

1. Deaktivieren Sie die **[!UICONTROL Use system value]** Kontrollkästchen und festlegen **[!UICONTROL Provider]** nach `Offline Calculation`.

   ![Fernanbieter für Fernabsatz-SSA](assets/inventory-distance-offline.png){width="350" zoomable="yes"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.

[1]: https://cloud.google.com/maps-platform/
[2]: https://developers.google.com/maps/documentation/geocoding/start
[3]: https://developers.google.com/maps/documentation/distance-matrix/start
[4]: https://developers.google.com/maps/documentation/javascript/distancematrix#travel_modes
[5]: https://www.geonames.org/
[6]: https://download.geonames.org/export/zip/readme.txt
