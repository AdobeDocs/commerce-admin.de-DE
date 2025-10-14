---
title: Erstellen ansprechender, personalisierter Erlebnisse in jedem Maßstab
description: Erfahren Sie, mit welchen Funktionen  [!DNL Commerce]  Adobe ein personalisiertes Erlebnis für Ihre Kunden erstellen können.
feature: Customers, Storefront, Personalization
exl-id: 9546e1b8-796b-4694-8396-773a2b0e9c12
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '1808'
ht-degree: 0%

---

# Erstellen ansprechender, personalisierter Erlebnisse in jedem Maßstab

Adobe [!DNL Commerce] bietet ein leistungsstarkes Toolkit zur Personalisierung jedes Kunden-Touchpoints, wodurch Kundeninteraktion, Konversion und Umsatz gesteigert werden.

In diesem Artikel erfahren Sie mehr über:

- Was ist Personalisierung?
- Welche Daten benötige ich, um eine Personalisierung zu erreichen?
- Wie ermöglicht Adobe [!DNL Commerce] Personalisierung?
- Verfügbare Anwendungsfälle für die Personalisierung

## Was ist Personalisierung?

Personalization bedeutet, die Kauferfahrung jedes Kunden an seine individuellen Bedürfnisse, seinen Kontext und seine Vorlieben anzupassen. Personalization ist nicht auf Inhalte auf der Website beschränkt oder empfiehlt Best-Fit-Produkte, sondern umfasst alle Touchpoints auf der Kunden-Journey, einschließlich:

- **Kampagnen und Kommunikation** - Bereitstellen relevanter und konsistenter Nachrichten über Kampagnen und Kommunikationen
- **Produktentdeckung** - Präsentation der richtigen Produkte für die richtigen Kunden in genau den richtigen Momenten
- **Promotions und Angebote** - Targeting-Promotions und -Angebote, um jeden Kunden zur Konversion zu bewegen
- **Content-Erlebnisse** - Anpassen des Site-Inhalts, damit er für jeden Kunden und sein Journey äußerst relevant ist

![Typen von Personalization](assets/types-personalization.png){width="700" zoomable="yes"}

Während diese Arten personalisierter Erlebnisse für eine kleine Untergruppe von Kunden erreichbar scheinen, kann die Personalisierung in großem Umfang für Tausende oder Millionen von Kunden über jeden Touchpoint und Kanal hinweg, alles in Echtzeit, unmöglich sein. In den folgenden Abschnitten erfahren Sie, wie Adobe [!DNL Commerce] und Adobe Experience Cloud helfen können.

## Welche Daten benötige ich, um eine Personalisierung zu erreichen?

Eine effektive Personalisierung erfordert Kontext oder Signale, die Informationen über Kunden bereitstellen, die dann verwendet werden können, um ihr Erlebnis zu ändern. Die folgende Tabelle enthält die verschiedenen Datentypen und die Rolle, die Adobe [!DNL Commerce] bei der Unterstützung der Erfassung und Aktivierung dieser Daten spielt.

| Datentypen | Storefront-Daten (Verhaltensereignisse) | Back-Office-Daten (Server-seitige Ereignisse) | Kundenprofil- und Segmentdaten |
|---|---|---|---|
| **Definition** | Klicks oder Aktionen, die Kunden auf Ihrer Site durchführen. | Informationen über den Lebenszyklus und Details jeder Bestellung (vergangene und aktuelle). | Wer sind Ihre Kunden und für welche Segmente sind sie qualifiziert? |
| **Von Adobe Commerce erfasste Ereignisse** | [pageView](https://experienceleague.adobe.com/de/docs/commerce/data-connection/event-forwarding/events#pageview)<br>[productPageView](https://experienceleague.adobe.com/de/docs/commerce/data-connection/event-forwarding/events)<br>[searchRequestSent](https://experienceleague.adobe.com/de/docs/commerce/data-connection/event-forwarding/events#searchrequestsent)<br>[searchResponseReceived](https://experienceleague.adobe.com/de/docs/commerce/data-connection/event-forwarding/events#searchresponsereceived)<br>[addToCart](https://experienceleague.adobe.com/de/docs/commerce/data-connection/event-forwarding/events#addtocart)<br>[openCart](https://experienceleague.adobe.com/de/docs/commerce/data-connection/event-forwarding/events#opencart)<br>[signIn](https://experienceleague.adobe.com/de/docs/commerce/data-connection/event-forwarding/events#signin)<br>[signOut](https://experienceleague.adobe.com/de/docs/commerce/data-connection/event-forwarding/events#signout)<br>[startCheckout](https://experienceleague.adobe.com/de/docs/commerce/data-connection/event-forwarding/events#startcheckout)<br>[completeCheckout](https://experienceleague.adobe.com/de/docs/commerce/data-connection/event-forwarding/events#completecheckout)<br>[createRequisitionList](https://experienceleague.adobe.com/de/docs/commerce/data-connection/event-forwarding/events#createrequisitionlist)<br>[addToRequisitionList](https://experienceleague.adobe.com/de/docs/commerce/data-connection/event-forwarding/events#addtorequisitionlist)<br>[removeFromRequisitionList](https://experienceleague.adobe.com/de/docs/commerce/data-connection/event-forwarding/events#removefromrequisitionlist) | **Bestellstatus**:<br>[orderPlaced](https://experienceleague.adobe.com/de/docs/commerce/data-connection/event-forwarding/events-backoffice#orderplaced)<br>[orderItemsReturnedInitiated](https://experienceleague.adobe.com/de/docs/commerce/data-connection/event-forwarding/events-backoffice#orderitemsreturnedinitiated)<br>[orderItemsShipped](https://experienceleague.adobe.com/de/docs/commerce/data-connection/event-forwarding/events-backoffice#orderitemsshipped)<br>[orderCancelled](https://experienceleague.adobe.com/de/docs/commerce/data-connection/event-forwarding/events-backoffice#ordercancelled)<br>[**Bestellverlauf**](https://experienceleague.adobe.com/de/docs/commerce/data-connection/fundamentals/connect-data#send-historical-order-data):<br>- SKU, Name, Preismenge, Rabatt<br>- Produktkategorie<br>- Zahlungsbetrag, Typ, Währung<br>- Versandart und Betrag<br>- Rückerstattungs-ID, Betrag, Währung<br>- Rückgabegrund, Bedingung, Lösung<br>- Adresse<br>- E-Mail | [**Profildatensatz**](https://experienceleague.adobe.com/de/docs/commerce/data-connection/event-forwarding/events-profilerecord): (Name, Geschlecht, Adresse, Treuestatus, Telefonnummer, E-Mail-Adresse)<br>**Kontostatus**:<br>[accountCreated](https://experienceleague.adobe.com/de/docs/commerce/data-connection/event-forwarding/events-backoffice#accountcreated)<br>[accountUpdated](https://experienceleague.adobe.com/de/docs/commerce/data-connection/event-forwarding/events-backoffice#accountupdated)<br>[accountDeleted](https://experienceleague.adobe.com/de/docs/commerce/data-connection/event-forwarding/events-backoffice#accountdeleted) |

Mit all diesen umfangreichen First-Party-[!DNL Commerce] können Sie die Erlebnisse Ihrer Kunden zielgerichtet personalisieren. Im nächsten Abschnitt erfahren Sie, wie Sie mit [!DNL Commerce] und Adobe Experience Cloud personalisierte Erlebnisse und die aktivierbaren Anwendungsfälle erstellen können.

## Wie ermöglicht Adobe [!DNL Commerce] Personalisierung?

Mit der Datenfreigabe in Adobe [!DNL Commerce] können Sie die Datentypen in der vorherigen Tabelle erfassen und für andere Adobe Experience Cloud-Produkte freigeben, um einheitliche Kundenprofile und Zielgruppen, personalisierte Kampagnen und umfangreiche Analysen und Einblicke zu ermöglichen.

![Datenfluss zum Experience Platform Edge](assets/commerce-edge.png){width="700" zoomable="yes"}

Die Datenfreigabe in Adobe [!DNL Commerce] umfasst zwei Hauptkomponenten:

1. [Datenverbindung](https://experienceleague.adobe.com/de/docs/commerce/data-connection/overview): Geben Sie Storefront-, Back-Office- und Kundenprofildaten aus Adobe [!DNL Commerce] an das Adobe Experience Platform Edge Network weiter, um sie in allen Adobe Experience Cloud-Programmen zu verwenden, einschließlich:

   - [Adobe [!DNL Real-Time CDP]](https://experienceleague.adobe.com/de/docs/experience-platform/rtcdp/intro/rtcdp-intro/overview): Fügen Sie Kundendaten aus verschiedenen Quellen (ERP, CRM, POS) in einheitliche Profile ein und erstellen Sie regelbasierte oder KI-basierte Segmente.
   - [Adobe [!DNL Journey Optimizer]](https://experienceleague.adobe.com/de/docs/journey-optimizer/using/get-started/get-started): Starten Sie personalisierte Omni-Channel-Journey, einschließlich E-Mail-Kampagnen, SMS, Push-Benachrichtigungen und mehr.
   - [Customer Journey Analytics](https://experienceleague.adobe.com/de/docs/analytics-platform/using/cja-overview/cja-overview) und [Adobe [!DNL Analytics]](https://experienceleague.adobe.com/de/docs/analytics/analyze/admin-overview/analytics-overview): Gewinnen Sie Einblicke in den Kunden und das Unternehmen.
   - [Adobe [!DNL Target]](https://experienceleague.adobe.com/de/docs/target/using/introduction/intro): Testen und Optimieren von Inhalten, empfohlenen Produkten, Angeboten, Navigation und mehr.

1. [[!DNL Audience Activation]](https://experienceleague.adobe.com/de/docs/commerce-admin/customers/audience-activation): Verwenden Sie [!DNL Real-Time CDP] Zielgruppen, um dynamische Inhaltsbausteine, Promotions und zugehörige Produktregeln auf Ihrer Adobe-[!DNL Commerce]-Site zu personalisieren.

### Personalisierte Storefront-Erlebnisse über jeden Kanal hinweg, skaliert

Adobe [!DNL Commerce] kann eine leistungsstarke Storefront namens [Edge Delivery Services](https://experienceleague.adobe.com/developer/commerce/storefront/?lang=de) nutzen, um personalisierte Erlebnisse auf allen Kanälen bereitzustellen. Dabei stehen KI-Funktionen im Mittelpunkt und Geschwindigkeit als Grundlage.

Mit Edge Delivery Services können Sie:

- **Erstellen personalisierter Inhalte**: Verwenden Sie das dokumentenbasierte Authoring, native Experimente mit Text- und Bildvarianten der generativen KI, um das Erlebnis skaliert zu personalisieren. Verwenden Sie Assets und die generative KI-Inhaltserstellung, um Produkt- und Marketing-Bilder im benötigten Umfang zu erstellen.

- **Varianten generieren**: Ermöglicht Inhaltsautoren die Verwendung von generativer KI zum Erstellen großer Mengen personalisierter KI-gesteuerter [Textinhalte und Bildvarianten](https://experienceleague.adobe.com/de/docs/experience-manager-learn/sites/generative-ai/generate-variations) mit Adobe Firefly.

- **Bereitstellung über die Edge Delivery Services-Storefront**: Inhalte in den Edge- und Commerce-Funktionen, die auf Dropdown-Komponenten basieren, um maßgeschneiderte Erlebnisse mit Shopping-Funktion für Ihre Zielgruppen zu erstellen.

- **Commerce und Adobe Experience Manager Assets**: Generative KI - Asset-Erstellung und Varianten in großem Maßstab. Erstellen, Bereitstellen und Überwachen der Inhaltsbereitstellung über jeden Kanal hinweg.

![Dropins: Produktdetailseite](assets/drop-in.png){width="700" zoomable="yes"}

### Vorkonfiguriertes Personalization: Erste Schritte mit nativen Adobe-[!DNL Commerce]

Adobe [!DNL Commerce] bietet mit seinen nativen vordefinierten Funktionen eine leistungsstarke Personalisierung. In der folgenden Tabelle werden [!DNL Commerce] Funktionen beschrieben, die Sie sofort aktivieren können, um auf Ihrem Personalisierungs-Journey zu beginnen.

| Kategorie | Funktionen |
|---|---|
| Personalisierte Produkterkennung | [[!DNL Live Search]](https://experienceleague.adobe.com/de/docs/commerce/live-search/overview): Personalisieren und optimieren Sie Suchergebnisse basierend auf den Verhaltensaktionen eines Käufers vor Ort und seiner Affinität zu einer KI-gestützten Suche.<br>[Intelligentes Kategorie-Merchandising](https://experienceleague.adobe.com/de/docs/commerce/live-search/live-search-admin/category-merch): KI-gesteuertes Produkt-Ranking auf Kategorieseiten basierend auf den Verhaltensaktionen und Affinitäten eines Käufers vor Ort.<br>[Produktempfehlungen](https://experienceleague.adobe.com/de/docs/commerce/product-recommendations/guide-overview): KI-gestützte Produktempfehlungen, die auf dem Kundenverhalten, den Trends und der Affinität basieren.<br>[Verwandte Produktregeln](https://experienceleague.adobe.com/de/docs/commerce-admin/marketing/promotions/product-relationships/product-related-rules) Definieren Sie benutzerdefinierte Regeln, um Produkte aus Ihrem Katalog anzuzeigen und so den Crosssell und den Upsell zu fördern. |
| Personalisierte Site-Inhalte | [Dynamische Inhaltsbausteine](https://experienceleague.adobe.com/de/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks): Zeigen Sie personalisierte Inhaltsbausteine, z. B. Banner, basierend auf Kundensegmenten in Adobe Commerce an. |
| Personalisierte Angebote und Angebote | [Warenkorbpreisregeln](https://experienceleague.adobe.com/de/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart): Wenden Sie Rabatte auf Artikel im Warenkorb basierend auf einer Reihe von Bedingungen an, einschließlich Kundensegmenten in Adobe [!DNL Commerce]. |
| Einblicke und Messung | [Adobe [!DNL Commerce] Intelligence](https://experienceleague.adobe.com/de/docs/commerce-business-intelligence/mbi/getting-started): Erfahren Sie, wie Ihre Personalisierungsstrategien funktionieren und im Laufe der Zeit verbessert werden. |

## Häufigste Anwendungsfälle für die Personalisierung

Adobe [!DNL Commerce]-Kunden verwenden vordefinierte Funktionen und geben Daten für eine Vielzahl von Anwendungsfällen an Adobe Experience Cloud weiter. In den folgenden Abschnitten werden die häufigsten Anwendungsfälle hervorgehoben und beschrieben, wie sie mit Adobe [!DNL Commerce] Only oder [!DNL Commerce] plus Experience Cloud Apps implementiert werden.

### Personalisierte Kampagnen und Mitteilungen

| Anwendungsfall | Lösung |
|---|---|
| **Transaktionsabbruch und Durchsuchen** - Versenden Sie eine personalisierte E-Mail oder Benachrichtigung zur erneuten Interaktion, wenn ein Kunde seinen Warenkorb oder seine Browsersitzung nach der Demonstration einer hohen Interaktion verlässt | **Nur Adobe-[!DNL Commerce]**:<br>[E-Mail-Erinnerungen](https://experienceleague.adobe.com/de/docs/commerce-admin/marketing/communications/email-reminders/email-reminder-rules)<br>**Adobe-[!DNL Commerce] mit Adobe Journey Optimizer**:<br>[!DNL Commerce]-Daten dienen als Trigger für eine Omni-Channel-Journey zum Abbruch von Vorgängen. Personalisieren Sie diese Journey anhand von Kundenattributen, dem, was sie abgebrochen haben, anderen Einkaufsverhaltensweisen und früheren Käufen.<br>Commerce mit Adobe Journey Optimizer und Real-Time CDP: Passen Sie Abbruchskampagnen auf der Basis von einheitlichen Kundenprofilen und zentral verwalteten Zielgruppen an, z. B. die Erstellung einer Zielgruppe mit hoher Abbruchsrate. |
| **Zentralisierte Zielgruppenerstellung** - Erstellen Sie regelbasierte oder KI-gestützte Zielgruppen basierend auf dem Onsite-Verhalten, früheren Käufen, Profilattributen, Kategorieaffinitäten, dem Treuestatus, dem Kundenwert und mehr | **Nur Adobe-[!DNL Commerce]**:<br>Sammeln Sie Kundenprofilinformationen, wenn [!DNL Commerce] Kunden Konten erstellen. Erstellen Sie regelbasierte [&#x200B; (Kundensegmente](https://experienceleague.adobe.com/de/docs/commerce-admin/customers/segments/customer-segments) und Kundengruppen, um Inhalte und Promotions zu personalisieren.<br>**Adobe [!DNL Commerce] mit Adobe Real-Time CDP**:<br> [Einheitliche Profile](https://experienceleague.adobe.com/de/docs/experience-platform/segmentation/home) aus allen Datenquellen und Kanälen; regelbasierte oder KI-gestützte Zielgruppen. |
| **Personalisiertes E-Mail-/SMS-Angebot basierend auf dem Käuferverhalten** - Senden Sie personalisierte Angebote an Kunden über eine zielgerichtete E-Mail basierend auf früheren Käufen und dem Käuferverhalten, z. B. ein Angebot für Produkte oder Kategorien, die Kunden angesehen oder mit denen sie interagiert haben. | **Nur Adobe-[!DNL Commerce]**:<br>Exportieren Sie Daten zur Verwendung mit Marketing-Automatisierungslösungen.<br>**Adobe [!DNL Commerce] mit Adobe Journey Optimizer und Real-Time CDP**:<br>[!DNL Commerce] Daten dienen als Trigger für E-Mail- oder SMS-Angebote und liefern Signale (Käuferverhalten) zur Personalisierung auf Grundlage von. Real-Time CDP ist nicht erforderlich, aber im Allgemeinen werden diese Angebote und Kampagnen für Audiences erstellt, die in Real-Time CDP erstellt und verwaltet werden. |
| **Cross- oder Upsell-kompatible Produkte/Marken** - Wenn ein Kunde ein Produkt oder eine Marke kauft, die kompatibel ist oder eine hohe Affinität zu einem anderen Produkt oder einer anderen Marke anzeigt, senden Sie eine Kampagne (E-Mail/SMS), um die Crosssell-Konversion zu fördern. | **Nur Adobe-[!DNL Commerce]**:<br>Verwenden Sie Adobe [!DNL Commerce] [Produktempfehlungen](https://experienceleague.adobe.com/de/docs/commerce/product-recommendations/guide-overview), um bestimmte Produkte auf der Website zu empfehlen. Sie können auch &quot;[&#x200B; Produktregeln“ verwenden](https://experienceleague.adobe.com/de/docs/commerce-admin/marketing/promotions/product-relationships/product-related-rules) um andere Produkte vorzuschlagen.<br>**[!DNL Commerce] mit [!DNL Target]**:<br>Adobe [!DNL Target] verfügt auch über eine integrierte Produktempfehlungs-Engine mit leistungsstarken Funktionen wie Kategorieaffinität. Dies kann für Cross- oder Upsell verwendet werden.<br>**[!DNL Commerce] mit Adobe Journey Optimizer**:<br>Verwenden Sie [!DNL Target] oder [!DNL Commerce], um Produkte zu bestimmen, die empfohlen werden sollen, und versenden Sie sie dann über Adobe Journey Optimizer. |

### Personalisierte Site-Erlebnisse

| Anwendungsfall | Lösung |
|---|---|
| **Personalisierter Site-Inhalt** - Personalisieren Sie Site-Banner und anderen Seiteninhalt basierend auf Käuferaktionen, wie Produktbrowsen und Kategorieaffinitäten. Bereitstellung von Best-Fit-Inhalten basierend auf den Ergebnissen von A/B-Tests oder Geschäftszielen | **Nur Adobe**&#x200B;[!DNL Commerce]:<br>Segmentspezifische (dynamische [) &#x200B;](https://experienceleague.adobe.com/de/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks) bereitstellen.<br>**[!DNL Commerce] mit Real-Time CDP &#x200B;**:<br>Verwenden Sie [Audience Activation](https://experienceleague.adobe.com/de/docs/commerce-admin/customers/audience-activation), um zielgruppenspezifische dynamische Inhaltsbausteine bereitzustellen, die auf Echtzeitaktionen und einheitliche Kundenprofildaten reagieren, und verwalten Sie gleichzeitig Profile und Zielgruppen in Real-Time CDP zentral.<br>**[!DNL Commerce] mit[!DNL Target]**:<br> Personalisieren Sie jeden Teil des Site-Erlebnisses, einschließlich Inhalt, Navigationselementen, vollständigen Seiten-Layouts und mehr, mithilfe von Adobe-[!DNL Commerce] in Adobe [!DNL Target]. A/B-Testinhalte: Wählen Sie die erfolgreichsten Inhalte für jeden Kunden automatisch aus und stellen Sie sie bereit.<br>**[!DNL Commerce] mit AEM Assets &#x200B;**:<br>Speichern Sie alle Ihre Inhalte in Adobe Experience Manager Assets. Nativer Zugriff auf diese Inhalte von Adobe Commerce aus. Verwenden Sie generative KI , um Inhaltsvarianten zu erstellen und für verschiedene Segmente oder Audiences zu personalisieren. |
| **Personalisiertes Onsite-Angebot basierend auf dem Verhalten** - Personalisieren Sie Werbeaktionen basierend auf Kundenaktionen, wie Produktsuche und Kategorieaffinitäten. Stellen Sie das nächstbeste Angebot basierend auf den Ergebnissen von A/B-Tests oder Geschäftszielen bereit. | **Nur Adobe-[!DNL Commerce]**:<br>Bereitstellen eines segmentspezifischen Katalogs und [Warenkorb-Preisregeln](https://experienceleague.adobe.com/de/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart).<br>**Adobe [!DNL Commerce] mit Real-Time CDP**:<br>Verwenden Sie [Audience Activation](https://experienceleague.adobe.com/de/docs/commerce-admin/customers/audience-activation), um zielgruppenspezifische Angebote bereitzustellen, während Sie Profile/Zielgruppen in Real-Time CDP zentral verwalten.<br>**Commerce mit[!DNL Target]**: Verwenden Sie Offer Decisioning, um zu bestimmen, welches Angebot bereitgestellt, A/B-Tests durchgeführt oder Geschäftsziele festgelegt werden sollen, um die in Adobe Commerce bereitgestellten Angebote zu leiten. |

### Analytics und Insights

| Anwendungsfall | Lösung |
|---|---|
| **Kundenverhalten nach Kanal** - Verstehen Sie die Feinheiten, in denen Kundinnen und Kunden in den einzelnen Kanälen (Web, persönlich, App usw.) interagieren, um sich auf Marketing-Strategien für jeden Kanal auszuwirken, und verstehen Sie den Kundentrichter und die Schwächen im Kundenerlebnis. | **Nur Adobe-[!DNL Commerce]**:<br>[Adobe [!DNL Commerce] Intelligence](https://experienceleague.adobe.com/de/docs/commerce-business-intelligence/mbi/getting-started) bietet umfangreiche Analysen auf dem digitalen [!DNL Commerce], jedoch nicht kanalübergreifend oder über Teile der Kunden-Journey hinweg.<br>**Adobe [!DNL Commerce] mit Customer Journey Analytics**:<br>[!DNL Commerce] Daten-Feeds-Daten-Dashboards für umfassende Details zu allen Phasen des Kundenerlebnisses (kanalübergreifend). Machen Sie sich mit jedem Touchpoint und dem erweiterten Trichter vertraut, um Schwachstellen auf der Kunden-Journey zu identifizieren, an denen Kunden herabfallen könnten. |
| **Kauftrends** - Verstehen Sie das Kaufverhalten über einen bestimmten Zeitraum (z. B. Warenkorbanalyse, Produktanalyse), um Trends und Saisonabhängigkeit zu identifizieren und das Marketing basierend auf historischen Kaufmustern zu optimieren. | **Nur Adobe-[!DNL Commerce]**:<br>[Adobe [!DNL Commerce] Intelligence](https://experienceleague.adobe.com/de/docs/commerce-business-intelligence/mbi/getting-started) bietet umfangreiche Analysen auf dem digitalen [!DNL Commerce], jedoch nicht kanalübergreifend oder über Teile der Kunden-Journey hinweg.<br>**Adobe [!DNL Commerce] mit Customer Journey Analytics**:<br>[!DNL Commerce] Daten-Feeds-Daten-Dashboards für umfassende Details zu allen Phasen des Kundenerlebnisses (kanalübergreifend). Machen Sie sich mit jedem Touchpoint und dem erweiterten Trichter vertraut, um Schwachstellen auf der Kunden-Journey zu identifizieren, an denen Kunden herabfallen könnten. |

## Beispielhafte Anwendungsfälle

- Erfahren Sie, wie Sie mit Adobe Journey Optimizer [E-Mail zu einem Transaktionsabbruch senden](https://experienceleague.adobe.com/de/docs/commerce/data-connection/use-cases/using-ajo).
- Erfahren Sie, wie [eine Zielgruppe in Real-Time CDP erstellen](https://experienceleague.adobe.com/de/docs/commerce/data-connection/use-cases/create-audience) um eine Warenkorb-Preisregel in Adobe [!DNL Commerce] zu informieren.
