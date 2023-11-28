---
title: Seiten
description: Erfahren Sie mehr über die Kerninhaltsseiten, die im [!DNL Commerce] Demospeicher und Änderung der Konfiguration Standardseiten .
exl-id: 4be7d3d6-ce36-42bc-9224-4804c3211f16
feature: Page Content, Configuration
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '908'
ht-degree: 0%

---

# Seiten

Der Inhalt kann in Bezug auf seine Haltbarkeit betrachtet werden, so wie jedes Produkt in einem Geschäft. Wussten Sie, dass die Haltbarkeitsdauer von Social-Media-Inhalten weniger als 24 Stunden beträgt? Die potenzielle Haltbarkeitsdauer des von Ihnen erstellten Inhalts kann Ihnen dabei helfen, zu entscheiden, wo Sie Ihre Ressourcen investieren.

Inhalte mit langer Haltbarkeitsdauer werden manchmal auch als _evergreen content_. Beispiele für zeitlose Inhalte sind Kundenerfolgsgeschichten, _Anleitung_ Anweisungen und häufig gestellte Fragen (FAQ). Im Gegensatz dazu umfassen Inhalte, die von der Natur verderbt werden, Veranstaltungen, Branchennachrichten und Pressemitteilungen.

![Die Seite &quot;Über uns&quot;im Beispiel-Luma-Store ](./assets/storefront-about-us.png){width="700" zoomable="yes"}

## Kerninhaltsseiten

Die [!DNL Commerce] Der Demospeicher enthält Beispiele für die wichtigsten Inhaltsseiten, die Ihnen bei den ersten Schritten helfen. Alle diese Seiten können Ihren Bedürfnissen entsprechend angepasst werden. Sehen Sie sich die folgenden Seiten in Ihrem Store an und stellen Sie sicher, dass der Inhalt Ihre Nachricht, Ihre Stimme und Ihre Marke vermittelt.

### Startseite

Die Demo [Startseite](../getting-started/storefront.md#home-page) enthält ein Banner, ein Bildkarussell, mehrere statische Bausteine mit Links und eine Liste neuer Produkte.

### Datenschutzrichtlinie

Der Laden [Datenschutzrichtlinie](../getting-started/privacy-policy.md) sollte mit Ihren eigenen Informationen aktualisiert werden. Als Best Practice sollte Ihre Datenschutzrichtlinie Ihren Kunden die Art der von Ihrem Unternehmen erfassten Informationen und deren Verwendung erläutern.

### 404 nicht gefunden

Die Seite &quot;404 Seite nicht gefunden&quot;ist nach dem Antwortcode benannt, der zurückgegeben wird, wenn eine Seite nicht gefunden werden kann. URL-Umleitungen reduzieren die Anzahl der Wiedergaben dieser Seite. In solchen Fällen, in denen dies erforderlich ist, können Sie jedoch auch die Möglichkeit nutzen, Links zu Produkten anzubieten, die für den Kunden interessant sein könnten.

### Zugriff verweigert

{{b2b-feature}}

Die [Zugriff verweigert](../b2b/account-company-roles-permissions.md) angezeigt, wenn die einem Unternehmensbenutzer zugewiesenen Berechtigungen den Zugriff auf die Seite verhindern.

### Cookies aktivieren

Die [Cookies aktivieren](../getting-started/compliance-cookie-law.md) angezeigt, wenn für Besucher Ihrer Site in ihren Browsern keine Cookies aktiviert sind. Die Seite enthält eine schrittweise, illustrierte Anleitung zur Aktivierung von Cookies für die beliebtesten Browser.

### Dienst nicht verfügbar

Die [503 Dienst nicht verfügbar](../configuration-reference/general/general.md) -Seite wird nach dem Antwort-Code benannt, der zurückgegeben wird, wenn der Server nicht verfügbar ist.

### Über uns

Die Seite Über uns ist in der Fußzeile Ihres Stores verlinkt. Sie können Bilder, Videos, Links zu Pressemitteilungen und Ankündigungen hinzufügen. Die Beispielseite enthält ein Bild rechts und ein dekoratives Bild, das das Ende der Seite angibt.

### Kundendienst

Die Seite &quot;Kundendienst&quot;ist ein weiterer Knoten in der Seitenhierarchie. Die beiden Kopfzeilen auf der Seite enthalten Inhalte, die nur sichtbar werden, wenn der Kunde auf die Kopfzeile klickt.

![Seite &quot;Kundendienst&quot;auf der Storefront](./assets/storefront-customer-service.png){width="700" zoomable="yes"}

## Standardseiten konfigurieren

Die _Standardseiten_ -Konfiguration bestimmt die Landingpage, die der [Basis-URL](../stores-purchase/store-urls.md) und der entsprechenden Startseite. Es wird auch bestimmt, welche Seite angezeigt wird, wenn ein _Seite nicht gefunden_ -Fehler auftritt und wenn eine [Breadcrumb-Pfad](../catalog/navigation-breadcrumb-trail.md) wird oben auf jeder Seite angezeigt.

1. Im _Admin_ Seitenleiste, navigieren Sie zu  **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Im linken Bereich unter _[!UICONTROL General]_auswählen **[!UICONTROL Web]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Default Pages]** Abschnitt.

   ![Standardseiten](./assets/web-default-pages.png){width="500" zoomable="yes"}

   | Feld | [Anwendungsbereich](../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
   |--- |--- |--- |
   | [!UICONTROL Default Web URL] | Store-Ansicht | Gibt die Landingpage an, die mit der Basis-URL verknüpft ist. Standardmäßig ist dieses Feld auf `cms` , um eine Seite aus der [!DNL Commerce] Content Management System. Sie können auch einen anderen Landingpage-Typ verwenden, z. B. einen Blog. Wenn beispielsweise ein Blog auf dem Server unter `magento/blog`können Sie den Ordnernamen eingeben `blog` als relativen Pfad zur Seitenauswahl. |
   | [!UICONTROL CMS Home Page] | Store-Ansicht | Um die Startseite für den Store auszuwählen, wählen Sie einfach die CMS-Seite aus der Liste aus. Standardmäßig listet die CMS-Startseite die gesamte Auswahl an CMS-Seiten auf, die für Ihren Store verfügbar sind. |
   | [!UICONTROL Default No-route URL] | Store-Ansicht | Enthält die URL der Standardseite, die angezeigt werden soll, wenn eine `404 Page not Found` Fehler auftritt. Der Standardwert ist `cms/noroute/index`. |
   | [!UICONTROL CMS No Route Page] | Store-Ansicht | Identifiziert eine bestimmte CMS-Seite, die angezeigt werden soll, wenn der Fehler &quot;404 Seite nicht gefunden&quot;auftritt. Die Standardseite lautet `404 Not Found`. |
   | [!UICONTROL CMS No Cookies Page] | Store-Ansicht | Identifiziert eine bestimmte CMS-Seite, die angezeigt wird, wenn Cookies für den Browser nicht aktiviert sind. Auf dieser Seite wird erläutert, warum Cookies verwendet werden und wie sie für jeden Browser aktiviert werden. Die Standardseite lautet `Enable Cookies`. |
   | [!UICONTROL Show Breadcrumbs for CMS Pages] | Store-Ansicht | Bestimmt, ob eine Breadcrumb-Leiste auf allen CMS-Seiten im Katalog angezeigt wird. Optionen: `Yes` / `No` |

   {style="table-layout:auto"}

1. Für **[!UICONTROL Default Web URL]** Geben Sie den relativen Pfad zum Ordner im [!DNL Commerce] -Installation, die die Landingpage enthält.

   Die Standardeinstellung, `cms`, zeigt eine Seite aus der [!DNL Commerce] Content Management System.

   >[!NOTE]
   >
   >Für eine bestimmte Store-Ansicht löschen Sie die **[!UICONTROL Use Default]** Kontrollkästchen neben _[!UICONTROL Default Web URL]_und alle anderen Standardeinstellungen, die geändert werden sollen.

1. Satz **[!UICONTROL CMS Home Page]** zur CMS-Seite, die als Startseite verwendet werden soll. Andere erstellte Seiten können als Startseite verwendet werden, z. B.:

   - Willkommen beim exklusiven Online Store
   - Prämienpunkte
   - Über uns
   - Kundendienst
   - Cookies aktivieren
   - Datenschutzrichtlinie
   - Unternehmen: Zugriff verweigert

1. Für **[!UICONTROL Default No-route URL]** Geben Sie den relativen Pfad zum Ordner im [!DNL Commerce] Installation, bei der die Seite umgeleitet wird, wenn eine _404 Seite nicht gefunden_ Fehler auftritt.

   Der Standardwert ist `cms/index/noRoute`.

1. Satz **[!UICONTROL CMS No Route Page]** zur CMS-Seite, die angezeigt wird, wenn eine _404 Seite nicht gefunden_ Fehler auftritt.

1. Satz **[!UICONTROL CMS No Cookies Page]** zur CMS-Seite, die angezeigt wird, wenn Cookies im Browser deaktiviert sind. Auf dieser Seite wird erläutert, warum Cookies verwendet werden und wie sie für jeden Browser aktiviert werden. Die Standardseite lautet `Enable Cookies`.

1. Wenn eine Breadcrumb-Leiste oben auf allen CMS-Seiten angezeigt werden soll, legen Sie **[!UICONTROL Show Breadcrumbs for CMS Pages]** nach `Yes`.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.
