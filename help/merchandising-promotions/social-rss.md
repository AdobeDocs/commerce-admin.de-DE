---
title: Social Media und RSS-Feeds
description: Erfahren Sie, wie Sie Social Media- und andere RSS-Feed-Integrationen hinzufügen, um die Markenwahrnehmung und das Produktbewusstsein zu steigern.
exl-id: e4a48870-f53e-4848-8faa-8f2aedaf53b7
feature: Merchandising, Communications
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1160'
ht-degree: 0%

---

# Social Media und RSS-Feeds

Viele Händler nutzen soziale Medien und andere digitale Tools, um Markenbewusstsein und Produktbewusstsein aufzubauen. Sie können Ihren Store in Ihre sozialen Netzwerke integrieren, indem Sie eine Marketplace-Erweiterung installieren oder ein Plug-in zu Ihren Inhaltsseiten hinzufügen. Verwenden Sie RSS-Feeds, um Ihre Produktinformationen auf Shopping-Aggregations-Websites zu veröffentlichen und sogar in Ihre Newsletter einzuschließen. Kunden können Ihre RSS-Feeds abonnieren, um mehr über neue Produkte und Werbeaktionen zu erfahren.

## Soziale Netzwerke

Ihr Store kann mit sozialen Netzwerken verbunden werden, indem eine [Marketplace-Erweiterung](../getting-started/commerce-marketplace.md) installiert wird. Darüber hinaus können Sie einfach Social-Plug-ins wie die Schaltfläche _Like_ zu CMS-Blöcken hinzufügen, die in Seiten in Ihrem gesamten Store integriert werden können.

Social-Networking-Websites verfügen über eine Vielzahl von Plug-ins, die einfach zu Ihrem Store hinzugefügt werden können. Darüber hinaus gibt es viele Erweiterungen auf der Commerce Marketplace, die verwendet werden können, um Ihren Store mit Social Media zu integrieren. Das folgende Beispiel zeigt, wie Sie Ihrem Store eine _Like_-Schaltfläche für Facebook hinzufügen.

>[!NOTE]
>
>Adobe Commerce hat die native Integration von _Magento Social_ Facebook entfernt und unterstützt die Erweiterung nicht mehr. Wechseln Sie zur [Commerce Marketplace](https://marketplace.magento.com/catalogsearch/result/?q=Facebook){:target="_blank"}, um alternative Erweiterungen für die Facebook-Integration zu finden.

### Schritt 1. Button-Code abrufen

1. Rufen Sie auf der Meta Developers-Website die Seite [Schaltflächen-Setup](https://developers.facebook.com/docs/plugins/like-button) auf.

1. Geben Sie **[!UICONTROL URL to Like]** die URL der Seite in Ihrem Store ein, die Personen gefallen soll _Like_.

   Sie können beispielsweise die URL der Startseite Ihres Stores eingeben.

1. Wählen Sie die **[!UICONTROL Layout]** für die Schaltfläche aus.

1. Geben Sie die **[!UICONTROL Width]** in Pixeln an, die auf Ihrer Site für die Schaltfläche und alle zugehörigen Textnachrichten verfügbar sind.

1. Legen Sie **[!UICONTROL Action Type]** auf eine der folgenden Einstellungen fest:

   - `Like`
   - `Recommend`

1. Klicken Sie auf **[!UICONTROL Get Code]** , um den generierten Code in die Zwischenablage zu kopieren.

### Schritt 2. Erstellen eines Inhaltsbausteins

1. Kehren Sie zu Ihrem Store-Administrator zurück.

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.

1. Klicken Sie oben rechts auf **[!UICONTROL Add New Block]**.

1. Geben Sie eine beschreibende **[!UICONTROL Block Title]** als interne Referenz ein.

   Beispiel: `Facebook Like Button`.

1. Weisen Sie dem Block einen eindeutigen **[!UICONTROL Identifier]** zu, indem Sie alle Kleinbuchstaben und Unterstriche anstelle von Leerzeichen verwenden.

   Beispiel: `facebook_like_button`.

1. Wenn Ihre Commerce-Instanz über mehrere Store-Ansichten verfügt, wählen Sie jede **[!UICONTROL Store View]** aus, in der der Block verfügbar sein soll.

1. Fügen Sie den Code-Ausschnitt je nach Content-Tool zum Blockinhalt hinzu:

   - Wenn Sie [!DNL Page Builder] verwenden, fügen Sie einen [HTML-Code](../page-builder/html-code.md)-Block zum Schritt hinzu und fügen Sie den Code-Ausschnitt ein, den Sie von der Facebook-Site kopiert haben. Andernfalls fügen Sie den Code-Ausschnitt in das Feld **[!UICONTROL Content]** ein.

   - Fügen Sie mit dem Editor den Code-Ausschnitt, den Sie von der Facebook-Site kopiert haben, in das Feld **[!UICONTROL Content]** ein.

1. Wenn der Block nicht bereit für die Live-Schaltung ist, setzen Sie **[!UICONTROL Enable Block]** auf `No`.

1. Klicken Sie abschließend auf **[!UICONTROL Save Block]**.

### Schritt 3. Platzieren des Blocks

1. Fügen Sie den Block je nach Content-Tool hinzu:

   - Wenn Sie [!UICONTROL Page Builder] verwenden, befolgen Sie die Anweisungen [Block hinzufügen](../page-builder/block.md) zum Schritt.

   - Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Klicken Sie oben rechts auf **[!UICONTROL Add Widget]** und führen Sie folgende Schritte aus:

   - ![Adobe Commerce B2B](../assets/b2b.svg) (nur für Adobe Commerce B2B verfügbar) Legen Sie im Abschnitt _Einstellungen_ den **[!UICONTROL Type]** auf `CMS Static Block` fest und klicken Sie auf **[!UICONTROL Continue]**.

   - Überprüfen, ob **[!UICONTROL Design Theme]** auf das aktuelle Design eingestellt ist.

   - Klicken Sie auf **[!UICONTROL Continue]**.

1. Gehen Sie im Abschnitt **[!UICONTROL Storefront Properties]** wie folgt vor:

   - Geben Sie **[!UICONTROL Widget Title]** einen Titel als interne Referenz ein.

   - Legen Sie **[!UICONTROL Assign to Store Views]** auf `All Store Views` oder auf die Ansicht fest, in der die App verfügbar sein soll. Halten Sie zum Auswählen mehrerer Ansichten die Strg-Taste (PC) bzw. die Befehlstaste (Mac) gedrückt und klicken Sie auf die einzelnen Optionen.

   - Geben Sie eine Zahl in das **[!UICONTROL Sort Order]** ein, um die Reihenfolge des Blocks zu bestimmen, wenn er so zugewiesen ist, dass er an derselben Stelle auf der Seite wie andere Inhaltselemente angezeigt wird. Die obere Position ist null.

1. Klicken Sie im Abschnitt _[!UICONTROL Layout Updates]_&#x200B;auf **[!UICONTROL Add Layout Update]**&#x200B;und legen Sie **[!UICONTROL Display On]**&#x200B;auf die Kategorie, das Produkt oder die Seite fest, in der bzw. der der Block angezeigt werden soll.

   Wenn Sie beispielsweise `All Pages` auswählen und den Block in der Kopf- oder Fußzeile platzieren, wird der Block an derselben Stelle auf jeder Seite des Stores angezeigt.

   Gehen Sie wie folgt vor, um den Block auf einer bestimmten Seite zu platzieren:

   - Legen Sie **[!UICONTROL Display On]** auf `Specified Page` fest und wählen Sie die **[!UICONTROL Page]** aus, in der der Block angezeigt werden soll.

   - Wählen Sie die **[!UICONTROL Block Reference]**, um die Position des Blocks auf der Seite zu bestimmen.

   - Akzeptieren Sie die Standardeinstellung für **[!UICONTROL Template]**, die auf `CMS Static Block Default Template` festgelegt ist.

   - Klicken Sie auf **[!UICONTROL Save and Continue Edit]**.

1. Wählen Sie im Bedienfeld auf der linken Seite **[!UICONTROL Widget Options]**.

1. Klicken Sie auf **[!UICONTROL Select Block…]** und wählen Sie den Block aus, den Sie platzieren möchten.

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.

1. Befolgen Sie bei Aufforderung die Anweisungen oben im Arbeitsbereich, um den Index und den Seiten-Cache zu aktualisieren.

   Das Widget wird jetzt in der _[!UICONTROL Widgets]_&#x200B;angezeigt.

### Schritt 4. Überprüfen des Speicherorts im Store

Kehren Sie zu Ihrer Storefront zurück, um sicherzustellen, dass sich der Block an der richtigen Position befindet. Um den Block zu verschieben, können Sie das Widget erneut öffnen und eine andere Seite oder Blockreferenz ausprobieren.

## RSS-Dienste

RSS (Really Simple Syndication) ist ein XML-basiertes Datenformat, das verwendet wird, um Informationen online zu verteilen. Ihre Kunden können Ihre RSS-Feeds abonnieren, um mehr über neue Produkte und Werbeaktionen zu erfahren. RSS-Feeds können auch verwendet werden, um Ihre Produktinformationen auf Shopping-Aggregations-Sites zu veröffentlichen, und können in Newsletter aufgenommen werden.

Wenn RSS-Feeds aktiviert sind, werden alle Ergänzungen zu Produkten, Sonderaktionen, Kategorien und Coupons automatisch an die Abonnenten jedes Feeds gesendet. Ein Link zu allen RSS-Feeds, die Sie veröffentlichen, befindet sich in der Fußzeile Ihres Stores.

![RSS-Feed-Symbol](./assets/icon-rss.png){width="100"}<br/>

Die Software, die zum Lesen eines RSS-Feeds erforderlich ist, wird als Feed-Reader bezeichnet und ermöglicht es Menschen, sich für Schlagzeilen, Blogs, Podcasts und vieles mehr zu abonnieren. Google Reader ist einer der vielen Feed-Reader, die online kostenlos zur Verfügung stehen.

![Beispiel-Storefront - RSS-Feed](./assets/storefront-rss-feeds.png){width="700" zoomable="yes"}

### Vorteile der Einrichtung eines RSS-Feeds

- Laden Sie das neueste Update von Ihrem Store oder Blog herunter.
- Light Ads
- Stammaktien
- SEO steigern
- Umsatz steigern

### Arten von RSS-Feeds

| RSS-Feed | Beschreibung |
|--- |--- |
| [!UICONTROL Wish List] | Nach der Aktivierung wird ein RSS-Feed-Link oben auf den Seiten der Kundenwunschliste angezeigt. Außerdem enthält die Seite zur Freigabe einer Wunschliste ein Kontrollkästchen, mit dem Sie einen Link zum Feed aus freigegebenen Wunschlisten einfügen können. |
| [!UICONTROL New Products] | Veröffentlicht Benachrichtigungen über neue Produkte, die dem Katalog hinzugefügt wurden. |
| [!UICONTROL Special Products] | Veröffentlicht Benachrichtigungen über alle Produkte mit Sonderpreisen. |
| [!UICONTROL Coupons / Discounts] | Veröffentlicht Benachrichtigungen über spezielle Coupons oder Rabatte, die im Store verfügbar sind. |
| [!UICONTROL Top Level Category] | Veröffentlicht Benachrichtigungen über Änderungen an der Kategoriestruktur auf oberster Ebene Ihres Katalogs, die im Hauptmenü angezeigt werden. |
| [!UICONTROL Customer Order Status] | Ermöglicht Kunden, ihren Bestellstatus per RSS-Feed zu verfolgen. Wenn diese Option aktiviert ist, wird ein RSS-Feed-Link auf der Bestellung angezeigt. |

{style="table-layout:auto"}

### Einrichten von RSS-Feeds für Ihren Store

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Stellen Sie in der oberen rechten Ecke **[!UICONTROL Store View]** auf die Ansichten, in denen die Feeds verfügbar sein sollen.

   Wenn Sie zum Bestätigen aufgefordert werden, klicken Sie auf **[!UICONTROL OK]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Catalog]** und wählen Sie **[!UICONTROL RSS Feeds]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Rss Config]** und legen Sie **[!UICONTROL Enable RSS]** auf `Enable` fest.

   ![Katalogkonfiguration - RSS-Feeds](../configuration-reference/catalog/assets/rss-feeds-rss-config.png){width="600" zoomable="yes"}

   Deaktivieren Sie bei Bedarf das Kontrollkästchen **[!UICONTROL Use Default]** , um den Standardwert zu ändern.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Wish List]** und legen Sie **[!UICONTROL Enable RSS]** auf `Enable` fest.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Catalog]** und legen Sie bei Bedarf andere Feeds auf `Enable` fest.

   - **[!UICONTROL New Products]**
   - **[!UICONTROL Special Products]**
   - **[!UICONTROL Coupons/Discounts]**
   - **[!UICONTROL Top Level Category]**

   ![Katalog - RSS-Feeds-Einstellungen](../configuration-reference/catalog/assets/rss-feeds-catalog.png){width="600" zoomable="yes"}

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Order]** und legen Sie **[!UICONTROL Customer Order Status Notification]** auf `Enable` fest.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.

1. Ergebnis auf der Storefront mit `/rss` am Ende der Seiten-URL anzeigen.

