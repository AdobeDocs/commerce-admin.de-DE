---
title: Produkt-URL-Neuschreibungen
description: Erfahren Sie, wie Sie mit Produkt-URL-Neuschreibungen Links zur URL eines anderen Produkts in Ihrem Commerce-Store umleiten können.
exl-id: 42b28ff7-e148-44f2-b6b4-63a38458e752
feature: Products, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '877'
ht-degree: 0%

---

# Produkt-URL-Neuschreibungen

Bevor Sie beginnen, sollten Sie genau wissen, was die Umleitung erreichen soll. Denken Sie an _target_ / _Originalanfrage_ oder _umleiten zu_ / _umleiten von_. Auch wenn Personen von Suchmaschinen oder veralteten Links aus zur ersten Seite navigieren, bewirkt die Umleitung, dass Ihr Store zum neuen Ziel wechselt.

Wenn [automatische Umleitungen](url-redirect-product-automatic.md) für Ihren Store aktiviert sind, müssen Sie keine Umschreibungen erstellen, wenn ein Produkt [URL-Schlüssel](../catalog/catalog-urls.md) geändert.

{{url-rewrite-skip}}

## Schritt 1. Neuschreiben planen

Um Fehler zu vermeiden, schreiben Sie die _umleiten zu_ Pfad und _umleiten von_ und fügen Sie den URL-Schlüssel und das Suffix hinzu (falls zutreffend).

Wenn Sie sich nicht sicher sind, öffnen Sie jede Produktseite in Ihrem Store und kopieren Sie den Pfad aus der Adressleiste Ihres Browsers. Beim Erstellen einer Produktumleitung können Sie die [Kategoriepfad](../catalog/catalog-urls.md). In diesem Beispiel erstellen wir eine Produktumleitung ohne Kategoriepfad.

### Produkt mit Kategoriepfad

Umleiten zu: `gear/bags/impulse-duffle.html`

Umleiten von: `gear/bags/overnight-duffle.html`

### Produkt ohne Kategoriepfad

Umleiten zu: `impulse-duffle.html`

Umleiten von: `overnight-duffle.html`

## Schritt 2. Erstellen des Neuschreibens

{{url-rewrite-params}}

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL URL Rewrites]**.

1. Bevor Sie fortfahren, führen Sie die folgenden Schritte aus, um sicherzustellen, dass der Anfragepfad verfügbar ist.

   - Im Suchfilter oben im **[!UICONTROL Request Path]** eingeben, den URL-Schlüssel der umzuleitenden Seite eingeben und auf **[!UICONTROL Search]**.

   - Wenn mehrere Umleitungsdatensätze für die Seite vorhanden sind, suchen Sie den, der der entsprechenden Store-Ansicht entspricht, und öffnen Sie ihn im Bearbeitungsmodus.

   - Klicken Sie oben rechts auf **[!UICONTROL Delete]**. Klicken Sie bei Aufforderung auf **[!UICONTROL OK]** zur Bestätigung.

1. Klicken Sie oben rechts auf der Seite &quot;URL-Neuschreibungen&quot;auf **URL-Neufassung hinzufügen**.

1. Satz **[!UICONTROL Create URL Rewrite]** nach `For product`.

1. Suchen Sie im Raster das Produkt, das das Ziel (Ziel) der Umleitung ist, und klicken Sie auf die Zeile.

   ![URL-Neuschreibungen - Produkt](./assets/url-rewrite-product.png){width="700" zoomable="yes"}

1. Klicken Sie unter der Kategorienstruktur auf **[!UICONTROL Skip Category Selection]**.

   In diesem Beispiel enthält die Umleitung keine Kategorie.

   ![Neuschreiben der Produkt-URL - Kategorieauswahl überspringen](./assets/url-rewrite-skip-category-selection.png){width="600" zoomable="yes"}

   Auf der Seite URL-Neufassung für ein Produkt hinzufügen wird links oben ein Link zum Ziel angezeigt. Im Feld Zielpfad wird die Systemversion des Pfads angezeigt, die nicht geändert werden kann. Zunächst zeigt das Feld Umleitungspfad auch den Zielpfad an.

   - Wenn Sie mehrere Store-Ansichten haben, legen Sie **[!UICONTROL Store]** in die Ansicht, in der die Neufassung angewendet wird. Andernfalls wird für jede Ansicht ein Umschreiben erstellt.

   - Für **[!UICONTROL Request Path]** ersetzen Sie den Standardwert, indem Sie den URL-Schlüssel und das Suffix (falls zutreffend) der ursprünglichen Produktanfrage eingeben. Dies ist die _umleiten von_ Produkt, das Sie im Planungsschritt identifiziert haben.

     >[!NOTE]
     >
     >Der Anfragepfad muss für den angegebenen Store eindeutig sein. Wenn bereits eine Weiterleitung vorhanden ist, die denselben Anfragepfad verwendet, erhalten Sie beim Speichern der Weiterleitung einen Fehler. Die vorherige Umleitung muss gelöscht werden, bevor Sie sie erstellen können.

   - Satz **[!UICONTROL Redirect Type]** auf einen der folgenden Werte zu:

      - `Temporary (302)`
      - `Permanent (301)`

   - Geben Sie für Ihre eigene Referenz eine kurze Beschreibung ein **[!UICONTROL Description]** des Neuschreibens.

   ![Produkt-URL-Neuschreiben - Informationen](./assets/url-rewrite-product-permanent-301.png){width="600" zoomable="yes"}

1. Bevor Sie die Umleitung speichern, überprüfen Sie Folgendes:

   - Der Link oben links zeigt den Namen des Zielprodukts an.
   - Der Anfragepfad enthält den Pfad für das Original _umleiten von_ Produkt.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save]**.

   Das neue Produkt-Rewrite wird jetzt oben im Raster URL-Neuschreibungen angezeigt.

## Schritt 3. Ergebnis testen

1. Gehen Sie zur Startseite Ihres Stores.

1. Führen Sie einen der folgenden Schritte aus:

   - Navigieren zum Original _umleiten von_ Produktanfrageseite.
   - Geben Sie in der Adressleiste des Browsers den Pfad zum ursprünglichen _umleiten von_ Produkt unmittelbar nach der Store-URL und drücken Sie **Eingabe**.

   Das neue Zielprodukt wird anstelle der ursprünglichen Produktanfrage angezeigt.

## Feldbeschreibungen

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Create URL Rewrite] | Gibt den Typ des Neuschreibens an. Der Typ kann nach der Erstellung des Neuschreibens nicht mehr geändert werden. Optionen: `Custom` / `For category` / `For product` / `For CMS page` |
| [!UICONTROL Request Path] | Das Produkt, das umgeleitet werden soll. Je nach Konfiguration kann der Anfragepfad die Variable `.html` oder `.htm` Suffix und Kategorie. Der Anfragepfad muss eindeutig sein und kann nicht von einer anderen Umleitung verwendet werden. Wenn Sie eine Fehlermeldung erhalten, dass der Anfragepfad vorhanden ist, löschen Sie die vorhandene Umleitung und versuchen Sie es erneut. |
| [!UICONTROL Target Path] | Der interne Pfad, der vom System verwendet wird, um auf das Ziel der Umleitung zu verweisen. Der Zielpfad ist ausgegraut und kann nicht bearbeitet werden. |
| [!UICONTROL Redirect] | Bestimmt den Typ der Umleitung. Optionen: <br/>**[!UICONTROL No]**- Es wird keine Umleitung angegeben. Viele Vorgänge erstellen Umleitungsanfragen dieses Typs. Jedes Mal, wenn Sie beispielsweise Produkte zu einer Kategorie hinzufügen, wird die `No` -Typ wird für jede Store-Ansicht erstellt.<br/>**[!UICONTROL Temporary (302)]** - Gibt Suchmaschinen an, dass das Neuschreiben für eine begrenzte Zeit erfolgt. Suchmaschinen speichern in der Regel keine Seiteneinstufungsinformationen für temporäre Neuschreibungen. <br/>**[!UICONTROL Permanent (301)]**- Gibt Suchmaschinen an, dass das Neuschreiben dauerhaft ist. Suchmaschinen behalten in der Regel Seiteneinstufungsinformationen für permanente Neuschreibungen bei. |
| [!UICONTROL Description] | Beschreibt den Zweck des Neuschreibens für interne Verweise. |

{style="table-layout:auto"}

## Mehrere URL-Neuschreibungen

Mit den folgenden Schritten können Sie URL-Neuschreibungen für mehrere oder alle Produkte gleichzeitig aktualisieren.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Wählen Sie alle Produkte aus, für die Sie URL-Neuschreibungen aktualisieren möchten.

1. under _[!UICONTROL Actions]_auswählen **[!UICONTROL Update attributes]**um mehrere oder alle Neuschreibungen zu aktualisieren.

1. under _[!UICONTROL PRODUCTS INFORMATION]_, klicken Sie auf die **[!UICONTROL Websites]**Registerkarte.

1. Im _[!UICONTROL Add Product To Websites]_Wählen Sie alle Websites aus, für die Sie URL-Neuschreibungen wiederherstellen möchten.

1. Wenn die Aktualisierung fertig ist, klicken Sie auf **[!UICONTROL Save]**.

>[!NOTE]
>
>Alle ausgewählten Produkte werden auf den ausgewählten Websites angezeigt und URL-Neuschreibungen werden neu generiert.

![Attribute aktualisieren - Aktualisieren mehrerer URL-Neuschreibungen](./assets/url-rewrites-update.png){width="600" zoomable="yes"}
