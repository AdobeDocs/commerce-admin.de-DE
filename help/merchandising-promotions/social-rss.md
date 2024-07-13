---
title: Social Media- und RSS-Dienste
description: Erfahren Sie, wie Sie soziale Medien und andere RSS-Feed-Integration hinzufügen können, um Marken- und Produktbewusstsein zu schaffen.
exl-id: e4a48870-f53e-4848-8faa-8f2aedaf53b7
feature: Merchandising, Communications
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1162'
ht-degree: 0%

---

# Social Media- und RSS-Dienste

Viele Händler verwenden soziale Medien und andere digitale Werkzeuge, um Marken- und Produktbewusstsein zu schärfen. Sie können Ihren Store in Ihre sozialen Netzwerke integrieren, indem Sie eine Marketplace-Erweiterung installieren oder ein Plugin zu Ihren Inhaltsseiten hinzufügen. Verwenden Sie RSS-Dienste, um Ihre Produktinformationen auf Einkaufs-Aggregations-Sites zu veröffentlichen und sie sogar in Ihre Newsletter aufzunehmen. Kunden können sich für Ihre RSS-Dienste anmelden, um mehr über neue Produkte und Promotions zu erfahren.

## Soziale Netzwerke

Ihr Store kann mit sozialen Netzwerken verbunden werden, indem Sie eine [Marketplace-Erweiterung](../getting-started/commerce-marketplace.md) installieren. Darüber hinaus können Sie CMS-Blöcken einfach soziale Plug-ins wie die Schaltfläche _Like_ hinzufügen, die in Seiten Ihres Stores integriert werden können.

Social-Networking-Sites verfügen über eine Vielzahl von Plugins, die einfach zu Ihrem Store hinzugefügt werden können. Darüber hinaus gibt es viele Erweiterungen auf dem Commerce Marketplace, die zur Integration Ihres Stores in Social Media verwendet werden können. Das folgende Beispiel zeigt, wie Sie Ihrem Store eine Facebook-Schaltfläche _Like_ hinzufügen.

>[!NOTE]
>
>Adobe Commerce hat die native Facebook-Integration _Magento Social_ entfernt und unterstützt die Erweiterung nicht mehr. Navigieren Sie zu [Commerce Marketplace](https://marketplace.magento.com/catalogsearch/result/?q=Facebook){:target=&quot;_blank&quot;} , um alternative Erweiterungen für die Facebook-Integration zu suchen.

### Schritt 1. Button-Code abrufen

1. Navigieren Sie auf der Meta-Entwickler-Website zur Seite [Schaltflächen-Setup](https://developers.facebook.com/docs/plugins/like-button) .

1. Geben Sie für &quot;**[!UICONTROL URL to Like]**&quot;die URL der Seite in Ihrem Store ein, die Sie für Personen mit &quot;_Gefällt mir_&quot;-Klicks verwenden möchten.

   Sie können beispielsweise die URL der Startseite Ihres Stores eingeben.

1. Wählen Sie die **[!UICONTROL Layout]** für die Schaltfläche aus.

1. Geben Sie die **[!UICONTROL Width]** in Pixel ein, die auf Ihrer Site für die Schaltfläche und die damit verknüpfte Textmeldung verfügbar sind.

1. Setzen Sie **[!UICONTROL Action Type]** auf einen der folgenden Werte:

   - `Like`
   - `Recommend`

1. Klicken Sie auf **[!UICONTROL Get Code]** , um den generierten Code in die Zwischenablage zu kopieren.

### Schritt 2. Inhaltsbaustein erstellen

1. Kehren Sie zu Ihrem Store-Administrator zurück.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.

1. Klicken Sie in der oberen rechten Ecke auf **[!UICONTROL Add New Block]**.

1. Geben Sie eine beschreibende **[!UICONTROL Block Title]** als internen Verweis ein.

   Beispiel: `Facebook Like Button`.

1. Weisen Sie dem Block ein eindeutiges &quot;**[!UICONTROL Identifier]**&quot;zu, indem Sie alle Kleinbuchstaben und Unterstriche anstelle von Leerzeichen verwenden.

   Beispiel: `facebook_like_button`.

1. Wenn Ihre Commerce-Instanz über mehrere Store-Ansichten verfügt, wählen Sie jeden **[!UICONTROL Store View]**, in dem der Block verfügbar sein soll.

1. Fügen Sie das Codefragment je nach Content-Tool zum Inhalt der Bausteine hinzu:

   - Fügen Sie bei Verwendung von [!DNL Page Builder] einen Block [HTML-Code](../page-builder/html-code.md) zur Bühne hinzu und fügen Sie den Codeausschnitt ein, den Sie von der Facebook-Site kopiert haben. Fügen Sie andernfalls den Codeausschnitt in das Feld **[!UICONTROL Content]** ein.

   - Fügen Sie mit dem Editor den Codeausschnitt, den Sie von der Facebook-Site kopiert haben, in das Feld **[!UICONTROL Content]** ein.

1. Wenn der Block nicht bereit ist, live zu gehen, setzen Sie **[!UICONTROL Enable Block]** auf `No`.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Block]**.

### Schritt 3. Platzieren Sie den Block

1. Fügen Sie den Block je nach Inhalts-Tool hinzu:

   - Befolgen Sie bei Verwendung von [!UICONTROL Page Builder] die Anweisungen zum Hinzufügen des Blocks](../page-builder/block.md) zur Bühne.[

   - Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Klicken Sie oben rechts auf **[!UICONTROL Add Widget]** und führen Sie folgende Schritte aus:

   - ![Adobe Commerce B2B](../assets/b2b.svg) (Nur für Adobe Commerce B2B verfügbar) Setzen Sie im Abschnitt _Einstellungen_ **[!UICONTROL Type]** auf `CMS Static Block` und klicken Sie auf **[!UICONTROL Continue]**.

   - Stellen Sie sicher, dass **[!UICONTROL Design Theme]** auf das aktuelle Design eingestellt ist.

   - Klicken Sie auf **[!UICONTROL Continue]**.

1. Gehen Sie im Abschnitt **[!UICONTROL Storefront Properties]** wie folgt vor:

   - Geben Sie für **[!UICONTROL Widget Title]** einen Titel für die interne Referenz ein.

   - Setzen Sie **[!UICONTROL Assign to Store Views]** auf `All Store Views` oder auf die Ansicht, in der die App verfügbar sein soll. Um mehrere Ansichten auszuwählen, halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie auf jede Option.

   - Geben Sie eine Zahl in das Feld **[!UICONTROL Sort Order]** ein, um die Reihenfolge des Bausteins zu bestimmen, wenn er so zugeordnet ist, dass er an derselben Stelle auf der Seite wie andere Inhaltselemente angezeigt wird. Die oberste Position ist Null.

1. Klicken Sie im Abschnitt _[!UICONTROL Layout Updates]_auf **[!UICONTROL Add Layout Update]**und legen Sie **[!UICONTROL Display On]**auf die Kategorie, das Produkt oder die Seite fest, in der der Block erscheinen soll.

   Wenn Sie beispielsweise &quot;`All Pages`&quot;auswählen und den Block entweder in der Kopf- oder Fußzeile platzieren, wird der Block auf jeder Seite des Stores an derselben Stelle angezeigt.

   Gehen Sie wie folgt vor, um den Baustein auf einer bestimmten Seite zu platzieren:

   - Setzen Sie **[!UICONTROL Display On]** auf `Specified Page` und wählen Sie die **[!UICONTROL Page]** aus, wo der Block erscheinen soll.

   - Wählen Sie **[!UICONTROL Block Reference]** aus, um die Stelle auf der Seite anzugeben, an der der Block platziert werden soll.

   - Akzeptieren Sie die Standardeinstellung für **[!UICONTROL Template]**, die auf `CMS Static Block Default Template` festgelegt ist.

   - Klicken Sie auf **[!UICONTROL Save and Continue Edit]**.

1. Wählen Sie im Bedienfeld auf der linken Seite **[!UICONTROL Widget Options]** aus.

1. Klicken Sie auf **[!UICONTROL Select Block…]** und wählen Sie den Block aus, den Sie platzieren möchten.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]**.

1. Befolgen Sie bei entsprechender Aufforderung die Anweisungen oben im Arbeitsbereich, um den Index- und Seiten-Cache zu aktualisieren.

   Das Widget wird jetzt in der Liste _[!UICONTROL Widgets]_angezeigt.

### Schritt 4. Überprüfen des Speicherorts im Store

Kehren Sie zu Ihrer Storefront zurück, um zu überprüfen, ob sich der Block an der richtigen Stelle befindet. Um den Block zu verschieben, können Sie das Widget erneut öffnen und eine andere Seite oder einen anderen Blockverweis ausprobieren.

## RSS-Feeds

RSS (Really Simple Syndication) ist ein XML-basiertes Datenformat, mit dem Informationen online verteilt werden. Ihre Kunden können sich für Ihre RSS-Dienste anmelden, um mehr über neue Produkte und Promotions zu erfahren. RSS-Dienste können auch verwendet werden, um Ihre Produktinformationen auf Shopping-Aggregations-Sites zu veröffentlichen, und können in Newslettern enthalten sein.

Wenn RSS-Dienste aktiviert sind, werden alle Ergänzungen zu Produkten, Sonderaktionen, Kategorien und Gutscheinen automatisch an die Abonnenten jedes Feeds gesendet. Ein Link zu allen RSS-Feeds, die Sie veröffentlichen, befindet sich in der Fußzeile Ihres Stores.

![RSS-Feed-Symbol](./assets/icon-rss.png){width="100"}<br/>

Die Software, die zum Lesen eines RSS-Dienstes erforderlich ist, wird als Feed-Reader bezeichnet und ermöglicht es Menschen, Überschriften, Blogs, Podcasts und vieles mehr zu abonnieren. Google Reader ist einer der vielen Feed-Leser, die online kostenlos verfügbar sind.

![Beispiel-Storefront - RSS-Feed](./assets/storefront-rss-feeds.png){width="700" zoomable="yes"}

### Vorteile der Einrichtung eines RSS-Dienstes

- Laden Sie das neueste Update von Ihrem Store oder Blog herunter
- Leuchtende Anzeigen
- Stammaktien
- SEO steigern
- Umsatzsteigerung

### Typen von RSS-Diensten

| RSS-Feed | Beschreibung |
|--- |--- |
| [!UICONTROL Wish List] | Wenn diese Option aktiviert ist, wird oben auf den Seiten mit der Kundenwunschliste ein RSS-Feed-Link angezeigt. Außerdem enthält die Seite zur Freigabe der Wunschliste ein Kontrollkästchen, mit dem Sie einen Link zum Feed aus freigegebenen Wunschlisten einfügen können. |
| [!UICONTROL New Products] | Veröffentlicht Benachrichtigungen über neue Produkte, die zum Katalog hinzugefügt wurden. |
| [!UICONTROL Special Products] | Veröffentlicht Benachrichtigungen über Produkte mit Sonderpreisen. |
| [!UICONTROL Coupons / Discounts] | Veröffentlicht Benachrichtigungen über spezielle Gutscheine oder Rabatte, die im Store verfügbar sind. |
| [!UICONTROL Top Level Category] | Veröffentlicht Benachrichtigungen über Änderungen an der Kategoriestruktur der obersten Ebene Ihres Katalogs, was im Hauptmenü angezeigt wird. |
| [!UICONTROL Customer Order Status] | Bietet Kunden die Möglichkeit, ihren Bestellstatus nach RSS-Feed zu verfolgen. Wenn diese Option aktiviert ist, wird in der Bestellung ein RSS-Feed-Link angezeigt. |

{style="table-layout:auto"}

### RSS-Dienste für Ihren Store einrichten

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Setzen Sie oben rechts **[!UICONTROL Store View]** auf die Ansichten, in denen die Feeds verfügbar sein sollen.

   Wenn Sie zur Bestätigung aufgefordert werden, klicken Sie auf **[!UICONTROL OK]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Catalog]** und wählen Sie **[!UICONTROL RSS Feeds]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Rss Config]** und legen Sie **[!UICONTROL Enable RSS]** auf `Enable` fest.

   ![Katalogkonfiguration - RSS-Feeds](../configuration-reference/catalog/assets/rss-feeds-rss-config.png){width="600" zoomable="yes"}

   Deaktivieren Sie bei Bedarf das Kontrollkästchen **[!UICONTROL Use Default]** , um den Standardwert zu ändern.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Wish List]** und legen Sie **[!UICONTROL Enable RSS]** auf `Enable` fest.

1. Erweitern Sie den Abschnitt **[!UICONTROL Catalog]** um ![Erweiterungsauswahl](../assets/icon-display-expand.png) und setzen Sie andere Feeds nach Bedarf auf `Enable`.

   - **[!UICONTROL New Products]**
   - **[!UICONTROL Special Products]**
   - **[!UICONTROL Coupons/Discounts]**
   - **[!UICONTROL Top Level Category]**

   ![Katalog - RSS-Feeds-Einstellungen](../configuration-reference/catalog/assets/rss-feeds-catalog.png){width="600" zoomable="yes"}

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Order]** und legen Sie **[!UICONTROL Customer Order Status Notification]** auf `Enable` fest.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.

1. Das Ergebnis wird in der Storefront mit `/rss` am Ende der Seiten-URL angezeigt.

