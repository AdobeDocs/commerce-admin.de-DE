---
title: Benutzerdefinierte URL-Neuschreibungen
description: Erfahren Sie, wie Sie benutzerdefinierte URL-Neuschreibungen verwenden können, um verschiedene Weiterleitungen in Ihrem Commerce-Store zu verwalten.
exl-id: b15054be-e463-48e6-b6c1-0a8a2141cc01
feature: Search, Configuration
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/de/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
source-git-commit: 6d782e3aafa7460a0e0d5ca07a2bde2ae371a9ea
workflow-type: tm+mt
source-wordcount: '690'
ht-degree: 0%

---

# Benutzerdefinierte URL-Neuschreibungen

Eine benutzerdefinierte Umschreibung kann verwendet werden, um verschiedene Umleitungen zu verwalten, z. B. die Umleitung einer Seite aus Ihrem Store zu einer externen Website. Beispielsweise könnten Sie zwei Commerce-Websites mit jeweils einer eigenen Domain haben. Sie können eine benutzerdefinierte Umleitung verwenden, um Anfragen für ein Produkt, eine Kategorie oder eine Seite an die andere Website umzuleiten. Im Gegensatz zu anderen Umleitungstypen wird das Ziel einer benutzerdefinierten Umleitung nicht aus einer Liste vorhandener Seiten in Ihrem Store ausgewählt.

Bevor Sie beginnen, stellen Sie sicher, dass Sie genau verstehen, was die Umleitung zu erreichen ist. Denken Sie an _target_ / _source_ oder _redirect to_ / _redirect from_. Obwohl Personen möglicherweise immer noch über Suchmaschinen oder veraltete Links zur vorherigen Seite navigieren, führt die Umleitung dazu, dass Ihr Store zum neuen Ziel wechselt.

## Schritt 1. Umschreiben planen

Um Fehler zu vermeiden, schreiben Sie die URL der Seite _Umleiten zu_ und den URL-Schlüssel der Seite _Umleiten von_ auf.

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

## Schritt 2. Umschreiben erstellen

{{url-rewrite-params}}

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL URL Rewrites]**.

1. Bevor Sie fortfahren, führen Sie folgende Schritte aus, um zu überprüfen, ob der Anfragepfad verfügbar ist:

   - Geben Sie im Suchfilter oben in der Spalte **[!UICONTROL Request Path]** den URL-Schlüssel der umzuleitenden Seite ein und klicken Sie auf **[!UICONTROL Search]**.

   - Wenn mehrere Umleitungsdatensätze für die Seite vorhanden sind, suchen Sie den entsprechenden Umleitungsdatensatz in der Store-Ansicht und öffnen Sie ihn im Bearbeitungsmodus.

   - Klicken Sie oben rechts auf **[!UICONTROL Delete]**. Wenn Sie dazu aufgefordert werden, klicken Sie zur Bestätigung auf **[!UICONTROL OK]** .

1. Wenn Sie zur Seite „URL-Neuschreibungen“ zurückkehren, klicken Sie auf **[!UICONTROL Add URL Rewrite]**.

1. Legen Sie **[!UICONTROL Create URL Rewrite]** auf `Custom` fest.

   ![URL-Neuschreibungen - benutzerdefiniert](./assets/url-rewrite-custom.png){width="600" zoomable="yes"}

1. Gehen Sie unter „URL Rewrite Information“ wie folgt vor:

   - Wenn Sie über mehrere Store-Ansichten verfügen, wählen Sie die **[!UICONTROL Store]** aus, für die die Umschreibung gilt.

   - Geben Sie **[!UICONTROL Request Path]** den URL-Schlüssel und ggf. den Pfad der Produkt-, Kategorie- oder CMS-Seite ein, die umgeleitet werden soll.

     >[!NOTE]
     >
     >Der Anfragepfad muss für den angegebenen Speicher eindeutig sein. Wenn bereits eine Umleitung vorhanden ist, die denselben Anfragepfad verwendet, erhalten Sie eine Fehlermeldung, wenn Sie versuchen, die Umleitung zu speichern. Die vorherige Umleitung muss gelöscht werden, bevor Sie eine erstellen können.

   - Geben Sie **[!UICONTROL Target Path]** die URL des Ziels ein. Wenn sich die Zielgruppe auf einer anderen Website befindet, geben Sie die vollqualifizierte URL ein.

   - Legen **Umleiten** auf eine der folgenden Optionen fest:

      - `Temporary (302)`
      - `Permanent (301)`

   - Geben Sie als Referenz eine kurze Beschreibung der Neufassung ein.

1. Bevor Sie die Umleitung speichern, überprüfen Sie Folgendes:

   - Die [!UICONTROL Request Path] enthält den URL-Schlüssel oder -Pfad der ursprünglichen _Umleitung von_-Seite.
   - Die [!UICONTROL Target Path] enthält die URL der Seite _Umleiten zu_.

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.

   Die neue Umschreibung wird im Raster oben in der Liste angezeigt.

## Schritt 3. Testen des Ergebnisses

1. Navigieren Sie zur Startseite Ihres Geschäfts.

1. Führen Sie einen der folgenden Schritte aus:

   - Navigieren Sie zur ursprünglichen Seite _Umleitung von_.
   - Geben Sie in der Adressleiste des Browsers den Namen der ursprünglichen Seite _Umleitung von_ unmittelbar nach der Store-URL ein und drücken Sie **Eingabetaste**.

   Die neue Zielseite wird anstelle der ursprünglichen Seitenanfrage angezeigt.

## Feldbeschreibungen

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Create URL Rewrite] | Gibt den Typ der Neuschreibung an. Der Typ kann nach dem Erstellen der Neuschreibung nicht mehr geändert werden. Optionen: `Custom` / `For category` / `For product` / `For CMS page` |
| [!UICONTROL Request Path] | Die Seite, die umgeleitet werden soll. Der Anfragepfad muss eindeutig sein und kann nicht von einer anderen Umleitung verwendet werden. Wenn Sie eine Fehlermeldung erhalten, dass der Anfragepfad vorhanden ist, löschen Sie die vorhandene Umleitung und versuchen Sie es erneut. |
| [!UICONTROL Target Path] | Der interne Pfad, der vom System zum Verweisen auf das Ziel verwendet wird. Der Zielpfad ist ausgegraut und kann nicht bearbeitet werden. |
| [!UICONTROL Redirect] | Bestimmt den Umleitungstyp. Optionen: <br/>**Nein** - Keine Umleitung angegeben. <br/>**[!UICONTROL Temporary (302)]**- Gibt Suchmaschinen an, dass die Neufassung für eine begrenzte Zeit erfolgt. Suchmaschinen speichern im Allgemeinen keine Seitenrangangaben für temporäre Neuschreibungen.<br/>**[!UICONTROL Permanent (301)]** - Gibt Suchmaschinen an, dass die Neuschreibung dauerhaft ist. Suchmaschinen behalten im Allgemeinen Seitenrangangaben für permanente Neuschreibungen bei. |
| [!UICONTROL Description] | Beschreibt den Zweck der Neufassung für interne Referenzen. |

{style="table-layout:auto"}
