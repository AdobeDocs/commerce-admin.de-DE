---
title: Seiten
description: Erfahren Sie mehr über die wichtigsten Inhaltsseiten, die im Demo [!DNL Commerce] Store enthalten sind, und über das Ändern der Konfiguration der Standardseiten.
exl-id: 4be7d3d6-ce36-42bc-9224-4804c3211f16
feature: Page Content, Configuration
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '932'
ht-degree: 0%

---

# Seiten

Inhalte können in Bezug auf ihre Haltbarkeit angezeigt werden, genau wie jedes Produkt in einem Geschäft. Wussten Sie, dass die Haltbarkeit von Social-Media-Inhalten weniger als 24 Stunden beträgt? Die potenzielle Haltbarkeit der von Ihnen erstellten Inhalte kann Ihnen bei der Entscheidung helfen, wo Sie Ihre Ressourcen investieren möchten.

Inhalte mit einer langen Haltbarkeitsdauer werden manchmal als _immergrüne Inhalte“_. Beispiele für zeitlose Inhalte sind Kundenerfolge _Anleitungen_ häufig gestellte Fragen (FAQ). Zu den von Natur aus verderblichen Inhalten gehören dagegen Veranstaltungen, Branchennachrichten und Pressemitteilungen.

![Die Seite „Über uns“, die im Luma-Beispiel-Store enthalten ist](./assets/storefront-about-us.png){width="700" zoomable="yes"}

## Grundlegende Inhaltsseiten

Der [!DNL Commerce] Demo-Store enthält Beispiele für zentrale Inhaltsseiten, die Ihnen bei den ersten Schritten helfen. Alle diese Seiten können Ihren Anforderungen entsprechend geändert werden. Sehen Sie sich die folgenden Seiten in Ihrem Store an und stellen Sie sicher, dass der Inhalt Ihre Nachricht, Ihre Stimme und Ihre Marke vermittelt.

### Startseite

Die Demo[Startseite](../getting-started/storefront.md#home-page) enthält ein Banner, ein Bildkarussell, mehrere statische Blöcke mit Links und eine Liste neuer Produkte.

### Datenschutzrichtlinie

Die Seite [ Store-](../getting-started/privacy-policy.md) sollte mit Ihren eigenen Informationen aktualisiert werden. Als Best Practice sollte Ihre Datenschutzrichtlinie Ihren Kunden erklären, welche Art von Informationen Ihr Unternehmen erfasst und wie sie verwendet werden.

### 404 nicht gefunden

Die Seite „404 Page Not Found“ wurde nach dem Antwort-Code benannt, der zurückgegeben wird, wenn eine Seite nicht gefunden werden kann. URL-Umleitungen verringern die Häufigkeit, mit der diese Seite angezeigt wird. Für die Zeiten, in denen es notwendig ist, können Sie aber auch die Gelegenheit nutzen, einige Links zu Produkten anzubieten, die der Kunde vielleicht interessant findet.

### Zugriff verweigert

{{b2b-feature}}

Die Seite [Zugriff verweigert](../b2b/account-company-roles-permissions.md) wird angezeigt, wenn die einem Unternehmensbenutzer zugewiesenen Berechtigungen den Zugriff auf die Seite verhindern.

### Aktivieren von Cookies

Die [Cookies aktivieren](../getting-started/compliance-cookie-law.md) wird angezeigt, wenn die Besucher Ihrer Site Cookies in ihren Browsern nicht aktiviert haben. Die Seite enthält Schritt-für-Schritt-Anweisungen, um Cookies für die beliebtesten Browser zu aktivieren.

### Service nicht verfügbar

Die Seite [503 Service Unavailable](../configuration-reference/general/general.md) ist nach dem Antwort-Code benannt, der zurückgegeben wird, wenn der Server nicht verfügbar ist.

### Über uns

Die Seite Über uns ist von der Fußzeile Ihres Stores verlinkt. Sie können Bilder, Videos, Links zu Pressemitteilungen und Ankündigungen einfügen. Die Beispielseite enthält rechts ein Bild und eine dekorative Seite, die das Ende der Seite anzeigt.

### Kundendienst

Die Kundendienstseite ist ein weiterer Knoten in der Seitenhierarchie. Die beiden Kopfzeilen auf der Seite enthalten Inhalte, die nur sichtbar werden, wenn der Kunde auf die Kopfzeile klickt.

![Kundendienstseite in der Storefront](./assets/storefront-customer-service.png){width="700" zoomable="yes"}

## Konfigurieren von Standardseiten

Die Konfiguration _Standardseiten_ bestimmt die Landingpage, die mit der [Basis-URL](../stores-purchase/store-urls.md) und der entsprechenden Startseite verknüpft ist. Außerdem wird festgelegt, welche Seite angezeigt wird _wenn ein Fehler_ Seite nicht gefunden“ auftritt und ob oben auf jeder Seite eine [Breadcrumb-](../catalog/navigation-breadcrumb-trail.md)&quot; angezeigt wird.

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wählen Sie im linken Bedienfeld unter _[!UICONTROL General]_die Option **[!UICONTROL Web]**aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Default Pages]** .

   ![Standardseiten](./assets/web-default-pages.png){width="500" zoomable="yes"}

   | Feld | [Umfang](../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
   |--- |--- |--- |
   | [!UICONTROL Default Web URL] | Shop-Ansicht | Gibt die Landingpage an, die mit der Basis-URL verknüpft ist. Standardmäßig ist dieses Feld auf `cms` gesetzt, um eine Seite aus dem [!DNL Commerce] Content Management System anzugeben. Sie können auch einen anderen Typ von Landingpage verwenden, z. B. einen Blog. Wenn beispielsweise ein Blog auf dem Server unter `magento/blog` installiert ist, können Sie den Ordnernamen `blog` als relativen Pfad zur Auswahl der Seiten eingeben. |
   | [!UICONTROL CMS Home Page] | Shop-Ansicht | Um die Startseite für den Store auszuwählen, wählen Sie einfach die CMS-Seite aus der Liste aus. Standardmäßig listet die CMS-Startseite alle CMS-Seiten auf, die für Ihren Store verfügbar sind. |
   | [!UICONTROL Default No-route URL] | Shop-Ansicht | Enthält die URL der Standardseite, die angezeigt werden soll, wenn ein `404 Page not Found` auftritt. Der Standardwert ist `cms/noroute/index`. |
   | [!UICONTROL CMS No Route Page] | Shop-Ansicht | Gibt eine bestimmte CMS-Seite an, die angezeigt werden soll, wenn der Fehler 404 Page Not Found auftritt. Die Standardseite ist `404 Not Found`. |
   | [!UICONTROL CMS No Cookies Page] | Shop-Ansicht | Gibt eine bestimmte CMS-Seite an, die angezeigt wird, wenn Cookies für den Browser nicht aktiviert sind. Auf dieser Seite wird erläutert, warum Cookies verwendet werden und wie Sie sie für jeden Browser aktivieren können. Die Standardseite ist `Enable Cookies`. |
   | [!UICONTROL Show Breadcrumbs for CMS Pages] | Shop-Ansicht | Legt fest, ob eine Breadcrumb-Spur auf allen CMS-Seiten im Katalog angezeigt wird. Optionen: `Yes` / `No` |

   {style="table-layout:auto"}

1. Geben Sie **[!UICONTROL Default Web URL]** den relativen Pfad zum Ordner in der [!DNL Commerce] ein, die die Landingpage enthält.

   Die Standardeinstellung `cms` zeigt eine Seite aus dem [!DNL Commerce] Content Management System an.

   >[!NOTE]
   >
   >Deaktivieren Sie für eine bestimmte Store-Ansicht das Kontrollkästchen **[!UICONTROL Use Default]** neben _[!UICONTROL Default Web URL]_und ändern Sie alle anderen Standardeinstellungen.

1. Legen Sie **[!UICONTROL CMS Home Page]** auf die CMS-Seite fest, die als Startseite verwendet werden soll. Andere erstellte Seiten können als Homepage verwendet werden, z. B.:

   - Willkommen im exklusiven Online-Store
   - Rewards-Punkte
   - Über uns
   - Kundendienst
   - Aktivieren von Cookies
   - Datenschutzrichtlinie
   - Firma: Zugriff verweigert

1. Geben Sie **[!UICONTROL Default No-route URL]** den relativen Pfad zum Ordner in der [!DNL Commerce] ein, zu dem die Seite umgeleitet wird, wenn der Fehler _404 Page Not Found_ auftritt.

   Der Standardwert ist `cms/index/noRoute`.

1. Legen Sie **[!UICONTROL CMS No Route Page]** auf die CMS-Seite fest, die angezeigt wird, wenn der Fehler _404 Page Not Found_ auftritt.

1. Legen Sie **[!UICONTROL CMS No Cookies Page]** auf die CMS-Seite fest, die angezeigt wird, wenn Cookies im Browser deaktiviert sind. Auf dieser Seite wird erläutert, warum Cookies verwendet werden und wie Sie sie für jeden Browser aktivieren können. Die Standardseite ist `Enable Cookies`.

1. Wenn ein Breadcrumb-Pfad oben auf allen CMS-Seiten angezeigt werden soll, setzen Sie **[!UICONTROL Show Breadcrumbs for CMS Pages]** auf `Yes`.

1. Klicken Sie abschließend auf **[!UICONTROL Save Config]**.
