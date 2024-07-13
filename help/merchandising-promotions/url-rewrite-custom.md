---
title: Benutzerdefinierte URL-Neuschreibungen
description: Erfahren Sie, wie Sie benutzerdefinierte URL-Umschreibungen verwenden können, um verschiedene Umleitungen in Ihrem Commerce-Store zu verwalten.
exl-id: b15054be-e463-48e6-b6c1-0a8a2141cc01
feature: Search, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '673'
ht-degree: 0%

---

# Benutzerdefinierte URL-Neuschreibungen

Eine benutzerdefinierte Umschreibung kann verwendet werden, um verschiedene Umleitungen zu verwalten, z. B. das Umleiten einer Seite von Ihrem Store zu einer externen Website. Sie können beispielsweise zwei Commerce-Websites verwenden, von denen jede über eine eigene Domäne verfügt. Sie können eine benutzerdefinierte Umleitung verwenden, um Anforderungen für ein Produkt, eine Kategorie oder eine Seite erneut an die andere Website zu senden. Im Gegensatz zu anderen Umleitungstypen wird das Ziel einer benutzerdefinierten Umleitung nicht aus einer Liste vorhandener Seiten in Ihrem Store ausgewählt.

Bevor Sie beginnen, sollten Sie genau wissen, was die Umleitung erreichen soll. Denken Sie an _target_ / _source_ oder _redirect to_ / _redirect from_. Auch wenn Personen von Suchmaschinen oder veralteten Links aus zur ersten Seite navigieren, bewirkt die Umleitung, dass Ihr Store zum neuen Ziel wechselt.

## Schritt 1. Neuschreiben planen

Um Fehler zu vermeiden, schreiben Sie die URL der Seite _Umleitung auf_ und den URL-Schlüssel der Seite _Umleitung von_ auf.

Wenn Sie sich nicht sicher sind, öffnen Sie jede Seite und kopieren Sie die URL aus der Adressleiste Ihres Browsers.

**Beispiel**

Umleiten zu:

    http://www.different-website.com/page.html

Umleiten von:

    cms-page
    category.html
    category/subcategory.html
    product.html
    category/product.html

## Schritt 2. Erstellen des Neuschreibens

{{url-rewrite-params}}

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL URL Rewrites]**.

1. Bevor Sie fortfahren, führen Sie die folgenden Schritte aus, um sicherzustellen, dass der Anfragepfad verfügbar ist:

   - Geben Sie im Suchfilter oben in der Spalte **[!UICONTROL Request Path]** den URL-Schlüssel der Seite ein, die umgeleitet werden soll, und klicken Sie auf **[!UICONTROL Search]**.

   - Wenn mehrere Umleitungsdatensätze für die Seite vorhanden sind, suchen Sie den, der der entsprechenden Store-Ansicht entspricht, und öffnen Sie ihn im Bearbeitungsmodus.

   - Klicken Sie in der oberen rechten Ecke auf **[!UICONTROL Delete]**. Klicken Sie nach Aufforderung zur Bestätigung auf **[!UICONTROL OK]** .

1. Wenn Sie zur Seite &quot;URL-Neuschreibungen&quot;zurückkehren, klicken Sie auf **[!UICONTROL Add URL Rewrite]**.

1. Setzen Sie **[!UICONTROL Create URL Rewrite]** auf `Custom`.

   ![URL-Neuschreibungen - custom](./assets/url-rewrite-custom.png){width="600" zoomable="yes"}

1. Führen Sie unter &quot;URL Rewrite Information&quot;die folgenden Schritte aus:

   - Wenn Sie mehrere Store-Ansichten haben, wählen Sie die **[!UICONTROL Store]** aus, für die das Neuschreiben gilt.

   - Geben Sie für &quot;**[!UICONTROL Request Path]**&quot;den URL-Schlüssel und den Pfad (falls zutreffend) der umzuleitenden Produkt-, Kategorie- oder CMS-Seite ein.

     >[!NOTE]
     >
     >Der Anfragepfad muss für den angegebenen Store eindeutig sein. Wenn bereits eine Weiterleitung vorhanden ist, die denselben Anfragepfad verwendet, erhalten Sie beim Speichern der Weiterleitung einen Fehler. Die vorherige Umleitung muss gelöscht werden, bevor Sie sie erstellen können.

   - Geben Sie für &quot;**[!UICONTROL Target Path]**&quot;die URL des Ziels ein. Wenn sich die Zielgruppe auf einer anderen Website befindet, geben Sie die vollständig qualifizierte URL ein.

   - Setzen Sie **Redirect** auf einen der folgenden Werte:

      - `Temporary (302)`
      - `Permanent (301)`

   - Geben Sie als Referenz eine kurze Beschreibung des Neuschreibens ein.

1. Bevor Sie die Umleitung speichern, überprüfen Sie Folgendes:

   - Der [!UICONTROL Request Path] enthält den URL-Schlüssel oder Pfad der ursprünglichen _Umleitung von der_ Seite.
   - Der [!UICONTROL Target Path] enthält die URL der Seite _Umleitung auf_.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]**.

   Das neue Neuschreiben wird im Raster oben in der Liste angezeigt.

## Schritt 3. Ergebnis testen

1. Gehen Sie zur Startseite Ihres Stores.

1. Führen Sie einen der folgenden Schritte aus:

   - Navigieren Sie von der Seite _zur ursprünglichen_ Umleitung.
   - Geben Sie in der Adressleiste des Browsers den Namen der ursprünglichen _Umleitung von der_ -Seite direkt nach der Store-URL ein und drücken Sie die **Eingabetaste**.

   Die neue Zielseite wird anstelle der ursprünglichen Seitenanforderung angezeigt.

## Feldbeschreibungen

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Create URL Rewrite] | Gibt den Typ des Neuschreibens an. Der Typ kann nach der Erstellung des Neuschreibens nicht mehr geändert werden. Optionen: `Custom` / `For category` / `For product` / `For CMS page` |
| [!UICONTROL Request Path] | Die Seite, die umgeleitet werden soll. Der Anfragepfad muss eindeutig sein und kann nicht von einer anderen Umleitung verwendet werden. Wenn Sie eine Fehlermeldung erhalten, dass der Anfragepfad vorhanden ist, löschen Sie die vorhandene Umleitung und versuchen Sie es erneut. |
| [!UICONTROL Target Path] | Der interne Pfad, der vom System verwendet wird, um auf das Ziel zu verweisen. Der Zielpfad ist ausgegraut und kann nicht bearbeitet werden. |
| [!UICONTROL Redirect] | Bestimmt den Typ der Umleitung. Optionen: <br/>**Nein** - Es wird keine Umleitung angegeben. <br/>**[!UICONTROL Temporary (302)]**- Gibt Suchmaschinen an, dass das Neuschreiben für eine begrenzte Zeit erfolgt. Suchmaschinen speichern in der Regel keine Seiteneinstufungsinformationen für temporäre Neuschreibungen.<br/>**[!UICONTROL Permanent (301)]** - Gibt Suchmaschinen an, dass das Neuschreiben dauerhaft ist. Suchmaschinen behalten in der Regel Seiteneinstufungsinformationen für permanente Neuschreibungen bei. |
| [!UICONTROL Description] | Beschreibt den Zweck des Neuschreibens für interne Verweise. |

{style="table-layout:auto"}
