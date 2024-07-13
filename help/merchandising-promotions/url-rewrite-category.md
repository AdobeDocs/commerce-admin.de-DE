---
title: Neuschreibungen der Kategorie-URL
description: Erfahren Sie, wie Sie mit Kategorie-URL-Neuschreibungen Links zur URL einer anderen Kategorie in Ihrem Commerce-Store umleiten können.
exl-id: fc18f472-4aa8-4203-ade9-7ca576689d61
feature: Categories, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 0%

---

# Neuschreibungen der Kategorie-URL

Wenn eine Kategorie aus Ihrem Katalog entfernt wird, können Sie eine Kategorienumschreibung verwenden, um Links zur URL einer anderen Kategorie in Ihrem Store umzuleiten. Denken Sie an die Werte _target_ / _original request_ oder _redirect to_ / _redirect from_. Auch wenn Personen von Suchmaschinen oder veralteten Links aus zur ersten Seite navigieren, bewirkt die Umleitung, dass Ihr Store zum neuen Ziel wechselt.

Wenn [automatische Umleitungen](url-redirect-product-automatic.md) für Ihren Store aktiviert sind, müssen Sie keine Umschreibungen erstellen, wenn eine Kategorie [URL-Schlüssel](../catalog/catalog-urls.md) geändert wird.

{{url-rewrite-skip}}

## Schritt 1. Neuschreiben planen

Um Fehler zu vermeiden, schreiben Sie den Pfad _redirect to_ und den Pfad _redirect from_ auf und fügen Sie den URL-Schlüssel und das Suffix hinzu (falls zutreffend).

Wenn Sie sich nicht sicher sind, öffnen Sie jede Kategorieseite in Ihrem Store und kopieren Sie den Pfad aus der Adressleiste Ihres Browsers.

**Beispiel:**

Umleiten zu: `gear/backpacks-and-bags.html`

Umleiten von: `gear/bags.html`

## Schritt 2. Erstellen des Neuschreibens

{{url-rewrite-params}}

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL URL Rewrites]**.

1. Bevor Sie fortfahren, führen Sie die folgenden Schritte aus, um sicherzustellen, dass der Anfragepfad verfügbar ist:

   - Geben Sie im Suchfilter oben in der Spalte **[!UICONTROL Request Path]** den URL-Schlüssel der Kategorie ein, die umgeleitet werden soll, und klicken Sie auf **[!UICONTROL Search]**.

   - Wenn mehrere Umleitungsdatensätze für die Seite vorhanden sind, suchen Sie den Datensatz, der mit der entsprechenden Store-Ansicht übereinstimmt, und öffnen Sie den Umleitungsdatensatz im Bearbeitungsmodus.

   - Klicken Sie in der oberen rechten Ecke auf **[!UICONTROL Delete]**. Klicken Sie nach Aufforderung zur Bestätigung auf **[!UICONTROL OK]** .

1. Wenn Sie zur Seite _[!UICONTROL URL Rewrites]_zurückkehren, klicken Sie auf **[!UICONTROL Add URL Rewrite]**.

1. Setzen Sie **[!UICONTROL Create URL Rewrite]** auf `For category` und wählen Sie die Zielkategorie im Baum aus, der das Ziel der Umleitung ist.

   ![URL rewrite - Kategorie auswählen](./assets/url-rewrite-category-choose.png){width="700" zoomable="yes"}

1. Führen Sie im Abschnitt _URL Rewrite_ folgende Schritte aus:

   - Wenn mehrere Stores vorhanden sind, wählen Sie den **[!UICONTROL Store]** aus, für den die Neufassung gilt.

   - Geben Sie für &quot;**[!UICONTROL Request Path]**&quot;den URL-Schlüssel der Kategorie ein, die der Kunde anfordert. Dies ist die _Umleitung aus der_ -Kategorie.

     >[!NOTE]
     >
     >Der Anfragepfad muss für den angegebenen Store eindeutig sein. Wenn bereits eine Weiterleitung vorhanden ist, die denselben Anfragepfad verwendet, erhalten Sie beim Speichern der Weiterleitung einen Fehler. Die vorherige Umleitung muss gelöscht werden, bevor Sie sie erstellen können.

   - Setzen Sie **[!UICONTROL Redirect]** auf einen der folgenden Werte:

      - `Temporary (302)`
      - `Permanent (301)`

   - Geben Sie als Referenz eine kurze Beschreibung des Neuschreibens ein.

   ![Hinzufügen von URL-Neuschreibungen für Kategorie](./assets/url-rewrite-for-category.png){width="700" zoomable="yes"}

1. Bevor Sie die Umleitung speichern, überprüfen Sie Folgendes:

   - Der Link oben links zeigt den Namen der Zielkategorie an.
   - Der Anfragepfad enthält den Pfad für die ursprüngliche _Umleitung aus der_ -Kategorie.

1. Klicken Sie nach Abschluss des Vorgangs auf die Schaltfläche **[!UICONTROL Save]** .

   Das neue Kategorienrewrite wird oben im Raster URL-Neuschreibungen angezeigt.

## Schritt 3. Ergebnis testen

1. Gehen Sie zur Startseite Ihres Stores.

1. Führen Sie einen der folgenden Schritte aus:

   - Navigieren Sie von der Kategorie _zur ursprünglichen_ Umleitung.
   - Geben Sie in der Adressleiste des Browsers den Pfad zur ursprünglichen _Umleitung von der Kategorie_ unmittelbar nach der Store-URL ein und drücken Sie **[!UICONTROL Enter]**.

   Die neue Zielkategorie wird anstelle der ursprünglichen Kategorieanforderung angezeigt.

## Feldbeschreibungen

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Create URL Rewrite] | Gibt den Typ des Neuschreibens an. Der Typ kann nach der Erstellung des Neuschreibens nicht mehr geändert werden. Optionen: `Custom` / `For category` / `For product` / `For CMS page` |
| [!UICONTROL Request Path] | Die Kategorie, die umgeleitet werden soll. Je nach Konfiguration kann der Anfragepfad das Suffix .html oder .htm sowie die übergeordnete Kategorie enthalten. Der Anfragepfad muss eindeutig sein und kann nicht von einer anderen Umleitung verwendet werden. Wenn Sie eine Fehlermeldung erhalten, dass der Anfragepfad vorhanden ist, löschen Sie die vorhandene Umleitung und versuchen Sie es erneut. |
| [!UICONTROL Target Path] | Der interne Pfad, der vom System verwendet wird, um auf das Ziel der Umleitung zu verweisen. Der Zielpfad ist ausgegraut und kann nicht bearbeitet werden. |
| [!UICONTROL Redirect] | Bestimmt den Typ der Umleitung. Optionen: <br/>**[!UICONTROL No]**- Es wird keine Umleitung angegeben. Viele Vorgänge erstellen Umleitungsanfragen dieses Typs. Jedes Mal, wenn Sie beispielsweise Produkte zu einer Kategorie hinzufügen, wird für jede Store-Ansicht eine Umleitung vom Typ `No` erstellt.<br/>**[!UICONTROL Temporary (302)]** - Gibt Suchmaschinen an, dass das Neuschreiben für eine begrenzte Zeit erfolgt. Suchmaschinen speichern in der Regel keine Seiteneinstufungsinformationen für temporäre Neuschreibungen. <br/>**[!UICONTROL Permanent (301)]**- Gibt Suchmaschinen an, dass das Neuschreiben dauerhaft ist. Suchmaschinen behalten in der Regel Seiteneinstufungsinformationen für permanente Neuschreibungen bei. |
| [!UICONTROL Description] | Beschreibt den Zweck des Neuschreibens für interne Verweise. |

{style="table-layout:auto"}
