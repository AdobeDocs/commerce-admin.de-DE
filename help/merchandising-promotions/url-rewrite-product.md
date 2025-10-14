---
title: Neuschreibungen der Produkt-URL
description: Erfahren Sie, wie Sie Produkt-URL-Neuschreibungen verwenden, um Links zur URL eines anderen Produkts in Ihrem Commerce Store umzuleiten.
exl-id: 42b28ff7-e148-44f2-b6b4-63a38458e752
feature: Products, Configuration
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/de/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
source-git-commit: 6d782e3aafa7460a0e0d5ca07a2bde2ae371a9ea
workflow-type: tm+mt
source-wordcount: '897'
ht-degree: 0%

---

# Neuschreibungen der Produkt-URL

Bevor Sie beginnen, stellen Sie sicher, dass Sie genau verstehen, was die Umleitung erreichen soll. Denken Sie an _target_ / _ursprüngliche Anfrage_ oder _umleiten zu_ / _umleiten von_. Obwohl Personen möglicherweise immer noch über Suchmaschinen oder veraltete Links zur vorherigen Seite navigieren, führt die Umleitung dazu, dass Ihr Store zum neuen Ziel wechselt.

Wenn [automatische Weiterleitungen](url-redirect-product-automatic.md) für Ihren Store aktiviert sind, müssen Sie keine Neuschreibungen erstellen, wenn ein Produkt (URL[Schlüssel](../catalog/catalog-urls.md) geändert wird.

{{url-rewrite-skip}}

## Schritt 1. Umschreiben planen

Um Fehler zu vermeiden, schreiben Sie den Pfad _umleiten zu_ und _umleiten von_ auf und fügen Sie den URL-Schlüssel und das Suffix (falls zutreffend) hinzu.

Wenn Sie sich nicht sicher sind, öffnen Sie jede Produktseite in Ihrem Store und kopieren Sie den Pfad aus der Adressleiste Ihres Browsers. Beim Erstellen einer Produktumleitung können Sie den [Kategoriepfad“ entweder ein- oder &#x200B;](../catalog/catalog-urls.md). Für dieses Beispiel erstellen wir eine Produktumleitung ohne Kategoriepfad.

### Produkt mit Kategoriepfad

Umleiten zu: `gear/bags/impulse-duffle.html`

Umleiten von: `gear/bags/overnight-duffle.html`

### Produkt ohne Kategoriepfad

Umleiten zu: `impulse-duffle.html`

Umleiten von: `overnight-duffle.html`

## Schritt 2. Umschreiben erstellen

{{url-rewrite-params}}

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL URL Rewrites]**.

1. Bevor Sie fortfahren, gehen Sie wie folgt vor, um zu überprüfen, ob der Anfragepfad verfügbar ist.

   - Geben Sie im Suchfilter oben in der Spalte **[!UICONTROL Request Path]** den URL-Schlüssel der umzuleitenden Seite ein und klicken Sie auf **[!UICONTROL Search]**.

   - Wenn mehrere Umleitungsdatensätze für die Seite vorhanden sind, suchen Sie den entsprechenden Umleitungsdatensatz in der Store-Ansicht und öffnen Sie ihn im Bearbeitungsmodus.

   - Klicken Sie oben rechts auf **[!UICONTROL Delete]**. Wenn Sie dazu aufgefordert werden, klicken Sie zur Bestätigung auf **[!UICONTROL OK]** .

1. Klicken Sie oben rechts auf der Seite „URL-Neuschreibungen“ auf **URL-Neuschreibungen hinzufügen**.

1. Legen Sie **[!UICONTROL Create URL Rewrite]** auf `For product` fest.

1. Suchen Sie im Raster das Produkt, das das Ziel (Ziel) der Umleitung ist, und klicken Sie auf die Zeile .

   ![URL-Neuschreibungen - Produkt](./assets/url-rewrite-product.png){width="700" zoomable="yes"}

1. Klicken Sie unter der Kategoriestruktur auf **[!UICONTROL Skip Category Selection]**.

   Bei diesem Beispiel enthält die Umleitung keine Kategorie.

   ![Neuschreiben der Produkt-URL - Kategorieauswahl überspringen](./assets/url-rewrite-skip-category-selection.png){width="600" zoomable="yes"}

   Die Seite URL-Umschreibung für ein Produkt hinzufügen zeigt oben links einen Link zum Ziel an, und das Feld Zielpfad zeigt die Systemversion des Pfads an, die nicht geändert werden kann. Zunächst wird im Feld Umleitungspfad auch der Zielpfad angezeigt.

   - Wenn Sie mehrere Store-Ansichten haben, legen Sie **[!UICONTROL Store]** auf die Ansicht fest, für die die Umschreibung gilt. Andernfalls wird für jede Ansicht eine Neufassung erstellt.

   - Ersetzen Sie **[!UICONTROL Request Path]** die Standardeinstellung, indem Sie den URL-Schlüssel und das Suffix (falls zutreffend) der ursprünglichen Produktanfrage eingeben. Dies ist das Produkt _Umleitung von_ das Sie im Planungsschritt identifiziert haben.

     >[!NOTE]
     >
     >Der Anfragepfad muss für den angegebenen Speicher eindeutig sein. Wenn bereits eine Umleitung vorhanden ist, die denselben Anfragepfad verwendet, erhalten Sie eine Fehlermeldung, wenn Sie versuchen, die Umleitung zu speichern. Die vorherige Umleitung muss gelöscht werden, bevor Sie eine erstellen können.

   - Legen Sie **[!UICONTROL Redirect Type]** auf eine der folgenden Einstellungen fest:

      - `Temporary (302)`
      - `Permanent (301)`

   - Geben Sie zur eigenen Referenz einen kurzen **[!UICONTROL Description]** der Neufassung ein.

   ![Neuschreiben der Produkt-URL - Informationen](./assets/url-rewrite-product-permanent-301.png){width="600" zoomable="yes"}

1. Bevor Sie die Umleitung speichern, überprüfen Sie Folgendes:

   - Der Link in der oberen linken Ecke zeigt den Namen des Zielprodukts an.
   - Der Anfragepfad enthält den Pfad für das ursprüngliche Produkt _Umleitung von_.

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.

   Die neue Produktumschreibung wird jetzt oben im URL-Umschreibungsraster angezeigt.

## Schritt 3. Testen des Ergebnisses

1. Navigieren Sie zur Startseite Ihres Geschäfts.

1. Führen Sie einen der folgenden Schritte aus:

   - Navigieren Sie zur ursprünglichen _Umleitung von_ Produktanfrageseite.
   - Geben Sie in der Adressleiste des Browsers den Pfad zum ursprünglichen Produkt _Umleitung von_ unmittelbar nach der Store-URL ein und drücken Sie die **Eingabetaste**.

   Das neue Zielprodukt wird anstelle der ursprünglichen Produktanfrage angezeigt.

## Feldbeschreibungen

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Create URL Rewrite] | Gibt den Typ der Neuschreibung an. Der Typ kann nach dem Erstellen der Neuschreibung nicht mehr geändert werden. Optionen: `Custom` / `For category` / `For product` / `For CMS page` |
| [!UICONTROL Request Path] | Das Produkt, das umgeleitet werden soll. Abhängig von Ihrer Konfiguration kann der Anfragepfad das Suffix `.html` oder `.htm` und die Kategorie enthalten. Der Anfragepfad muss eindeutig sein und kann nicht von einer anderen Umleitung verwendet werden. Wenn Sie eine Fehlermeldung erhalten, dass der Anfragepfad vorhanden ist, löschen Sie die vorhandene Umleitung und versuchen Sie es erneut. |
| [!UICONTROL Target Path] | Der interne Pfad, der vom System verwendet wird, um auf das Ziel der Umleitung zu verweisen. Der Zielpfad ist ausgegraut und kann nicht bearbeitet werden. |
| [!UICONTROL Redirect] | Bestimmt den Umleitungstyp. Optionen: <br/>**[!UICONTROL No]**- Keine Umleitung angegeben. Viele Vorgänge erstellen Umleitungsanfragen dieses Typs. Jedes Mal, wenn Sie beispielsweise Produkte zu einer Kategorie hinzufügen, wird für jede Shop-Ansicht eine Umleitung des `No` erstellt.<br/>**[!UICONTROL Temporary (302)]** - Gibt Suchmaschinen an, dass die Neufassung für eine begrenzte Zeit erfolgt. Suchmaschinen speichern im Allgemeinen keine Seitenrangangaben für temporäre Neuschreibungen. <br/>**[!UICONTROL Permanent (301)]**- Gibt Suchmaschinen an, dass die Neuschreibung dauerhaft ist. Suchmaschinen behalten im Allgemeinen Seitenrangangaben für permanente Neuschreibungen bei. |
| [!UICONTROL Description] | Beschreibt den Zweck der Neufassung für interne Referenzen. |

{style="table-layout:auto"}

## Mehrere URL-Neuschreibungen

Mit den folgenden Schritten können Sie URL-Neuschreibungen für mehrere oder alle Produkte gleichzeitig aktualisieren.

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Wählen Sie alle Produkte aus, für die Sie URL-Neuschreibungen aktualisieren möchten.

1. Wählen Sie unter _[!UICONTROL Actions]_&#x200B;die Option **[!UICONTROL Update attributes]**&#x200B;aus, um mehrere oder alle Neuschreibungen zu aktualisieren.

1. Klicken Sie unter _[!UICONTROL PRODUCTS INFORMATION]_&#x200B;auf die Registerkarte **[!UICONTROL Websites]**.

1. Wählen Sie im Abschnitt _[!UICONTROL Add Product To Websites]_&#x200B;alle Websites aus, für die Sie URL-Neuschreibungen wiederherstellen möchten.

1. Wenn Sie bereit zum Aktualisieren sind, klicken Sie auf **[!UICONTROL Save]**.

>[!NOTE]
>
>Alle ausgewählten Produkte werden zu den ausgewählten Websites hinzugefügt und URL-Neuschreibungen werden neu generiert.

![Attribute aktualisieren - mehrere URL-Neuschreibungen aktualisieren](./assets/url-rewrites-update.png){width="600" zoomable="yes"}
