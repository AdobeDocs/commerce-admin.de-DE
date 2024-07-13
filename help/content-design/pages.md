---
title: Seiten
description: Erfahren Sie mehr über die Kerninhaltsseiten, die im [!DNL Commerce] Demospeicher enthalten sind, und über die Änderung der Konfiguration der Standardseiten.
exl-id: 4be7d3d6-ce36-42bc-9224-4804c3211f16
feature: Page Content, Configuration
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '915'
ht-degree: 0%

---

# Seiten

Der Inhalt kann in Bezug auf seine Haltbarkeit betrachtet werden, so wie jedes Produkt in einem Geschäft. Wussten Sie, dass die Haltbarkeitsdauer von Social-Media-Inhalten weniger als 24 Stunden beträgt? Die potenzielle Haltbarkeitsdauer des von Ihnen erstellten Inhalts kann Ihnen dabei helfen, zu entscheiden, wo Sie Ihre Ressourcen investieren.

Inhalte mit langer Haltbarkeitsdauer werden manchmal als _evergreen content_ bezeichnet. Beispiele für zeitlose Inhalte sind Erfolgsgeschichten von Kunden, _Anweisungen zum_ und häufig gestellte Fragen (FAQ). Im Gegensatz dazu umfassen Inhalte, die von der Natur verderbt werden, Veranstaltungen, Branchennachrichten und Pressemitteilungen.

![Die Seite &quot;Über uns&quot;im Beispiel-Luma-Store ](./assets/storefront-about-us.png){width="700" zoomable="yes"}

## Kerninhaltsseiten

Der Demospeicher [!DNL Commerce] enthält Beispiele für Seiten mit Kerninhalten, die Ihnen bei den ersten Schritten helfen. Alle diese Seiten können Ihren Bedürfnissen entsprechend angepasst werden. Sehen Sie sich die folgenden Seiten in Ihrem Store an und stellen Sie sicher, dass der Inhalt Ihre Nachricht, Ihre Stimme und Ihre Marke vermittelt.

### Startseite

Die Demoseite [Home](../getting-started/storefront.md#home-page) enthält ein Banner, ein Bildkarussell, mehrere statische Bausteine mit Links und eine Liste neuer Produkte.

### Datenschutzrichtlinie

Die Seite [Datenschutzrichtlinie](../getting-started/privacy-policy.md) speichern sollte mit Ihren eigenen Informationen aktualisiert werden. Als Best Practice sollte Ihre Datenschutzrichtlinie Ihren Kunden die Art der von Ihrem Unternehmen erfassten Informationen und deren Verwendung erläutern.

### 404 nicht gefunden

Die Seite &quot;404 Seite nicht gefunden&quot;ist nach dem Antwortcode benannt, der zurückgegeben wird, wenn eine Seite nicht gefunden werden kann. URL-Umleitungen reduzieren die Anzahl der Wiedergaben dieser Seite. In solchen Fällen, in denen dies erforderlich ist, können Sie jedoch auch die Möglichkeit nutzen, Links zu Produkten anzubieten, die für den Kunden interessant sein könnten.

### Zugriff verweigert

{{b2b-feature}}

Die Seite [Zugriff verweigert](../b2b/account-company-roles-permissions.md) wird angezeigt, wenn die einem Unternehmensbenutzer zugewiesenen Berechtigungen den Zugriff auf die Seite verhindern.

### Cookies aktivieren

Die Seite [Cookies aktivieren](../getting-started/compliance-cookie-law.md) wird angezeigt, wenn für Besucher Ihrer Site in ihren Browsern keine Cookies aktiviert sind. Die Seite enthält eine schrittweise, illustrierte Anleitung zur Aktivierung von Cookies für die beliebtesten Browser.

### Dienst nicht verfügbar

Die Seite &quot;[503 Service Unavailable](../configuration-reference/general/general.md)&quot; wird nach dem Antwortcode benannt, der zurückgegeben wird, wenn der Server nicht verfügbar ist.

### Über uns

Die Seite Über uns ist in der Fußzeile Ihres Stores verlinkt. Sie können Bilder, Videos, Links zu Pressemitteilungen und Ankündigungen hinzufügen. Die Beispielseite enthält ein Bild rechts und ein dekoratives Bild, das das Ende der Seite angibt.

### Kundendienst

Die Seite &quot;Kundendienst&quot;ist ein weiterer Knoten in der Seitenhierarchie. Die beiden Kopfzeilen auf der Seite enthalten Inhalte, die nur sichtbar werden, wenn der Kunde auf die Kopfzeile klickt.

![Seite &quot;Kundendienst&quot;auf der Storefront](./assets/storefront-customer-service.png){width="700" zoomable="yes"}

## Standardseiten konfigurieren

Die Konfiguration _Standardseiten_ bestimmt die Landingpage, die der [Basis-URL](../stores-purchase/store-urls.md) und der entsprechenden Startseite zugeordnet ist. Sie bestimmt außerdem, welche Seite angezeigt wird, wenn ein Fehler vom Typ _Seite nicht gefunden_ auftritt und oben auf jeder Seite ein Breadcrumb-Pfad vom Typ [ angezeigt wird.](../catalog/navigation-breadcrumb-trail.md)

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wählen Sie im linken Bereich unter _[!UICONTROL General]_die Option **[!UICONTROL Web]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Default Pages]** .

   ![Standardseiten](./assets/web-default-pages.png){width="500" zoomable="yes"}

   | Feld | [Umfang](../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
   |--- |--- |--- |
   | [!UICONTROL Default Web URL] | Store-Ansicht | Gibt die Landingpage an, die mit der Basis-URL verknüpft ist. Standardmäßig ist dieses Feld auf `cms` gesetzt, um eine Seite aus dem Content Management System [!DNL Commerce] anzugeben. Sie können auch einen anderen Landingpage-Typ verwenden, z. B. einen Blog. Wenn beispielsweise ein Blog unter `magento/blog` auf dem Server installiert ist, können Sie den Ordnernamen `blog` als relativen Pfad zur Seitenauswahl eingeben. |
   | [!UICONTROL CMS Home Page] | Store-Ansicht | Um die Startseite für den Store auszuwählen, wählen Sie einfach die CMS-Seite aus der Liste aus. Standardmäßig listet die CMS-Startseite die gesamte Auswahl an CMS-Seiten auf, die für Ihren Store verfügbar sind. |
   | [!UICONTROL Default No-route URL] | Store-Ansicht | Enthält die URL der Standardseite, die angezeigt werden soll, wenn ein `404 Page not Found` -Fehler auftritt. Der Standardwert ist `cms/noroute/index`. |
   | [!UICONTROL CMS No Route Page] | Store-Ansicht | Identifiziert eine bestimmte CMS-Seite, die angezeigt werden soll, wenn der Fehler &quot;404 Seite nicht gefunden&quot;auftritt. Die Standardseite ist `404 Not Found`. |
   | [!UICONTROL CMS No Cookies Page] | Store-Ansicht | Identifiziert eine bestimmte CMS-Seite, die angezeigt wird, wenn Cookies für den Browser nicht aktiviert sind. Auf dieser Seite wird erläutert, warum Cookies verwendet werden und wie sie für jeden Browser aktiviert werden. Die Standardseite ist `Enable Cookies`. |
   | [!UICONTROL Show Breadcrumbs for CMS Pages] | Store-Ansicht | Bestimmt, ob eine Breadcrumb-Leiste auf allen CMS-Seiten im Katalog angezeigt wird. Optionen: `Yes` / `No` |

   {style="table-layout:auto"}

1. Geben Sie für &quot;**[!UICONTROL Default Web URL]**&quot;den relativen Pfad zum Ordner in der [!DNL Commerce] -Installation ein, die die Landingpage enthält.

   Die Standardeinstellung &quot;`cms`&quot; zeigt eine Seite aus dem Content Management System &quot;[!DNL Commerce]&quot; an.

   >[!NOTE]
   >
   >Für eine bestimmte Store-Ansicht deaktivieren Sie das Kontrollkästchen **[!UICONTROL Use Default]** neben _[!UICONTROL Default Web URL]_und alle anderen Standardeinstellungen, die geändert werden sollen.

1. Setzen Sie **[!UICONTROL CMS Home Page]** auf die CMS-Seite, die als Startseite verwendet werden soll. Andere erstellte Seiten können als Startseite verwendet werden, z. B.:

   - Willkommen beim exklusiven Online Store
   - Prämienpunkte
   - Über uns
   - Kundendienst
   - Cookies aktivieren
   - Datenschutzrichtlinie
   - Unternehmen: Zugriff verweigert

1. Geben Sie für &quot;**[!UICONTROL Default No-route URL]**&quot;den relativen Pfad zum Ordner in der [!DNL Commerce] -Installation ein, bei der die Seite umgeleitet wird, wenn ein Fehler vom Typ _404 Seite nicht gefunden_ auftritt.

   Der Standardwert ist `cms/index/noRoute`.

1. Setzen Sie **[!UICONTROL CMS No Route Page]** auf die CMS-Seite, die angezeigt wird, wenn der Fehler _404 Seite nicht gefunden_ auftritt.

1. Setzen Sie **[!UICONTROL CMS No Cookies Page]** auf die CMS-Seite, die angezeigt wird, wenn Cookies im Browser deaktiviert sind. Auf dieser Seite wird erläutert, warum Cookies verwendet werden und wie sie für jeden Browser aktiviert werden. Die Standardseite ist `Enable Cookies`.

1. Wenn Sie möchten, dass oben auf allen CMS-Seiten ein Breadcrumb-Pfad angezeigt wird, setzen Sie **[!UICONTROL Show Breadcrumbs for CMS Pages]** auf `Yes`.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.
