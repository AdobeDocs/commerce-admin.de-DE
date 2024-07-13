---
title: Erstellen ansprechender, personalisierter Erlebnisse im Maßstab
description: Erfahren Sie, welche Funktionen in Adobe [!DNL Commerce] es Ihnen ermöglichen, ein personalisiertes Erlebnis für Ihre Kunden zu erstellen.
feature: Customers, Storefront, Personalization
exl-id: 9546e1b8-796b-4694-8396-773a2b0e9c12
source-git-commit: 728a1fdb413009a00377cd8205dde93cd4feadc8
workflow-type: tm+mt
source-wordcount: '1808'
ht-degree: 0%

---

# Erstellen ansprechender, personalisierter Erlebnisse im Maßstab

Adobe [!DNL Commerce] bietet Ihnen ein leistungsstarkes Toolkit zur Personalisierung jedes Touchpoints, das die Interaktion, Konversion und den Umsatz der Kunden steigert.

In diesem Artikel erfahren Sie:

- Was ist Personalisierung?
- Welche Daten benötige ich für die Personalisierung?
- Wie entsperrt Adobe [!DNL Commerce] die Personalisierung?
- Verfügbare Personalisierungsanwendungsfälle

## Was ist Personalisierung?

Personalization bedeutet, dass die Aspekte des Kauferlebnisses jedes Kunden an seine individuellen Bedürfnisse, Gegebenheiten und Präferenzen angepasst werden. Personalization beschränkt sich nicht auf Inhalte auf der Site oder empfiehlt passende Produkte, sondern umfasst alle Touchpoints auf der gesamten Journey, einschließlich:

- **Kampagnen und Kommunikation** - Bereitstellung relevanter und konsistenter Nachrichten über Kampagnen und Kommunikation
- **Produkterkennung** - Anzeige der richtigen Produkte für die richtigen Kunden in genau den richtigen Augenblicken
- **Promotions und Angebote** - Targeting von Promotions und Angeboten, um jeden Kunden zur Konversion zu bewegen
- **Inhaltserlebnisse** - Anpassen von Site-Inhalten, um sie für jeden Kunden und dessen Journey überrelevant zu fühlen

![Typen von Personalization](assets/types-personalization.png){width="700" zoomable="yes"}

Diese Arten personalisierter Erlebnisse können für eine kleine Untergruppe von Kunden zwar erreichbar sein, für Tausende oder Millionen von Kunden über jeden Touchpoint und jeden Kanal personalisiert werden, aber in Echtzeit kann sich dies als unmöglich erweisen. In den folgenden Abschnitten erfahren Sie, wie Adobe [!DNL Commerce] und Adobe Experience Cloud helfen können.

## Welche Daten benötige ich für die Personalisierung?

Eine effektive Personalisierung erfordert Kontext oder Signale, die Informationen über Kunden bereitstellen, die dann zur Änderung ihres Erlebnisses verwendet werden können. Die folgende Tabelle enthält die verschiedenen Datentypen und die Rolle, die Adobe [!DNL Commerce] bei der Unterstützung der Erfassung und Aktivierung dieser Daten spielt.

| Datentypen | Storefront-Daten (Verhaltensereignisse) | Back Office Data (Server-Side Events) | Kundenprofil und Segmentdaten |
|---|---|---|---|
| **Definition** | Klicks oder Aktionen, die Kunden auf Ihrer Site ausführen. | Informationen zum Lebenszyklus und Details der einzelnen Bestellungen (Vergangenheit und aktuell). | Wer Ihre Käufer sind und für welche Segmente sie sich qualifizieren. |
| **Von Adobe Commerce erfasste Ereignisse** | [pageView](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#pageview)<br>[productPageView](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)<br>[searchRequestSent](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#searchrequestsent)<br>[searchResponseReceived](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#searchresponsereceived)<br>[addToCart](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#addtocart)<br>[openCart](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#opencart)<br>[signIn](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#signin)<br>[signOut](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#signout)<br>[startCheckout](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#startcheckout)<br>[completeCheckout](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#completecheckout)<br>[createRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#createrequisitionlist)<br>[addToRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#addtorequisitionlist)<br>[removeFromRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#removefromrequisitionlist) | **Bestellstatus**:<br>[orderPlaced](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#orderplaced)<br>[orderItemsReturnedInitiated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#orderitemsreturnedinitiated)<br>[orderItemsShipped](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#orderitemsshipped)<br>[orderCancelled](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#ordercancelled)<br>[**Auftragsverlauf**](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/fundamentals/connect-data#send-historical-order-data):<br>- SKU, Name, Preismenge, Rabatt<br>- Produkt<br>- Zahlungsbetrag, -typ, Währung<br>- Versandmethode und -betrag<br>- Rückerstattungs-ID, Betrag, Währung<br>- Rückkehrgrund, Bedingung, Auflösung<br>- Adresse<br>- E-Mail | [**Profildatensatz**](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-profilerecord): (Name, Geschlecht, Adresse, Treuestatus, Telefonnummer, E-Mail-Adresse)<br>**Kontostatus**:<br>[accountCreated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#accountcreated)<br>[accountUpdated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#accountupdated)<br>[accountDeleted](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#accountdeleted) |

Mit all diesen umfangreichen Erstanbieterdaten ([!DNL Commerce]) können Sie das Erlebnis jedes einzelnen Käufers gezielt ansprechen und personalisieren. Im nächsten Abschnitt erfahren Sie, wie Sie mit [!DNL Commerce] und Adobe Experience Cloud personalisierte Erlebnisse und Anwendungsfälle erstellen können, die Sie aktivieren können.

## Wie ermöglicht Adobe [!DNL Commerce] die Personalisierung?

Adobe [!DNL Commerce] Mit der Datenfreigabe können Sie die Datentypen in der vorherigen Tabelle erfassen und für andere Adobe Experience Cloud-Produkte freigeben, um einheitliche Kundenprofile und -zielgruppen, personalisierte Kampagnen sowie umfassende Analysen und Einblicke zu ermöglichen.

![Datenfluss zum Experience Platform Edge](assets/commerce-edge.png){width="700" zoomable="yes"}

Adobe [!DNL Commerce] Die Datenfreigabe umfasst zwei wichtige Komponenten:

1. [Datenverbindung](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/overview): Geben Sie Storefront-, Back-Office- und Kundenprofildaten von Adobe [!DNL Commerce] an das Adobe Experience Platform Edge-Netzwerk frei, um sie in allen Adobe Experience Cloud-Anwendungen zu verwenden, darunter:

   - [Adobe [!DNL Real-Time CDP]](https://experienceleague.adobe.com/en/docs/experience-platform/rtcdp/intro/rtcdp-intro/overview): Verknüpfen Sie Kundendaten aus verschiedenen Quellen (ERP, CRM, POS) mit einheitlichen Profilen und erstellen Sie regelbasierte oder AI-basierte Segmente.
   - [Adobe [!DNL Journey Optimizer]](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/get-started): Starten Sie personalisierte Omni-Channel-Journey, einschließlich E-Mail-Kampagnen, SMS, Push-Benachrichtigungen und mehr.
   - [Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview) und [Adobe [!DNL Analytics]](https://experienceleague.adobe.com/en/docs/analytics/analyze/admin-overview/analytics-overview): Erhalten Sie Einblicke in den Kunden und das Unternehmen.
   - [Adobe [!DNL Target]](https://experienceleague.adobe.com/en/docs/target/using/introduction/intro): Testen und optimieren Sie Inhalte, empfohlene Produkte, Angebote, Navigation und mehr.

1. [[!DNL Audience Activation]](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation): Verwenden Sie [!DNL Real-Time CDP] Zielgruppen, um dynamische Inhaltsbausteine, Promotions und zugehörige Produktregeln auf Ihrer Adobe [!DNL Commerce]-Site zu personalisieren.

### Personalisierte Storefront-Erlebnisse für alle Kanäle im großen Maßstab

Adobe [!DNL Commerce] kann von einer leistungsstarken Storefront namens [Edge Delivery Services](https://experienceleague.adobe.com/developer/commerce/storefront/) profitieren, die personalisierte Erlebnisse auf allen Kanälen bereitstellt, mit KI-Funktionen im Kern und Geschwindigkeit als Grundlage.

Mit Edge Delivery Services können Sie:

- **Gestalteter personalisierter Inhalt**: Verwenden Sie dokumentbasiertes Authoring und native Experimentierung mit generativen KI-Text- und Bildvarianten, um das Erlebnis skaliert zu personalisieren. Verwenden Sie die Inhaltserstellung für Assets und Generative KI, um skaliert Produkt- und Marketingbilder zu erstellen.

- **Varianten generieren**: Ermöglicht es Inhaltsautoren, generative KI zu verwenden, um große Mengen personalisierter KI-gesteuerter [Textinhalte und Bildvarianten](https://experienceleague.adobe.com/en/docs/experience-manager-learn/sites/generative-ai/generate-variations) mit Adobe Firefly zu erstellen.

- **Stellen Sie über Edge Delivery Services Storefront bereit**: Inhalte zu den Edge- und Commerce-Funktionen, die durch Dropdown-Komponenten bereitgestellt werden, um für Ihre Zielgruppen maßgeschneiderte Erlebnisse mit Shopping-Funktion zu erstellen.

- **Commerce und Adobe Experience Manager Assets**: Generative AI-Produktelementerstellung und Skalierungsversionen. Erstellen, liefern und überwachen Sie die Inhaltsbereitstellung über jeden Kanal hinweg.

![Drop-ins: Produktdetailseite](assets/drop-in.png){width="700" zoomable="yes"}

### Native Personalization: Erste Schritte mit nativen Adobe [!DNL Commerce]-Funktionen

Adobe [!DNL Commerce] bietet eine leistungsstarke Personalisierung mit nativen vordefinierten Funktionen. In der folgenden Tabelle werden die [!DNL Commerce]-Funktionen beschrieben, die Sie sofort aktivieren können, um mit der Personalisierungs-Journey zu beginnen.

| Kategorie | Funktionen |
|---|---|
| Personalisierte Produkterkennung | [[!DNL Live Search]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/overview): Personalisieren und optimieren Sie Suchergebnisse basierend auf den verhaltensbezogenen Aktionen und Affinitäten eines Käufers auf der Site mit KI-gestützter Suche.<br>[Intelligentes KategorieMerchandising](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-admin/category-merch): KI-gesteuertes Produktranking auf Kategorieseiten basierend auf den verhaltensbezogenen Aktionen und Affinitäten eines Käufers auf der Site.<br>[Produkt-Recommendations](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/guide-overview): KI-gestützte Produktempfehlungen basierend auf dem Kundenverhalten, Trends und Affinitäten.<br>[Zugehörige Produktregeln](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/product-relationships/product-related-rules): Definieren Sie benutzerdefinierte Regeln, um Produkte aus Ihrem Katalog anzuzeigen und so Cross- und Up-Sell zu fördern. |
| Personalisierte Site-Inhalte | [Dynamische Inhaltsbausteine](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks): Zeigt personalisierte Inhaltsbausteine an, z. B. Banner, die auf Kundensegmenten in Adobe Commerce basieren. |
| Personalisierte Angebote und Promotions | [Preisregeln für Warenkorb](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart): Wenden Sie Rabatte auf Artikel im Warenkorb an, die auf einer Reihe von Bedingungen basieren, einschließlich Kundensegmenten in Adobe [!DNL Commerce]. |
| Einblicke und Messung | [Adobe [!DNL Commerce] Intelligence](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started): Verstehen Sie, wie Ihre Personalisierungsstrategien im Laufe der Zeit funktionieren und verbessern. |

## Häufigste Personalisierungs-Anwendungsfälle

Adobe [!DNL Commerce] -Kunden verwenden für eine Vielzahl von Anwendungsfällen vordefinierte Funktionen und teilen Daten an Adobe Experience Cloud. In den folgenden Abschnitten werden die wichtigsten Anwendungsfälle hervorgehoben und beschrieben, wie sie mit Adobe [!DNL Commerce] Only oder [!DNL Commerce] plus Experience Cloud-Apps implementiert werden.

### Personalisierte Kampagnen und Kommunikation

| Anwendungsfall | Lösung |
|---|---|
| **Warenkorb und Durchsuchen** - Stellen Sie eine personalisierte E-Mail zur erneuten Interaktion oder Benachrichtigung bereit, wenn ein Kunde seinen Warenkorb oder seine Browser-Sitzung abgebrochen hat, nachdem er eine hohe Interaktion gezeigt hat. | **Adobe [!DNL Commerce] Nur**:<br>[E-Mail-Erinnerungen](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/communications/email-reminders/email-reminder-rules)<br>**Adobe [!DNL Commerce] mit Adobe Journey Optimizer**:<br>[!DNL Commerce] -Daten dienen als Trigger für eine Journey zum Abbruch eines Kanals. Personalisieren Sie diese Journey anhand von Kundenattributen, abgebrochenen Artikeln, anderen Kaufverhaltensweisen und früheren Käufen.<br>Commerce mit Adobe Journey Optimizer und Real-Time CDP: Kampagnen zum Abbruch von Aufgaben auf der Grundlage von einheitlichen Kundenprofilen und zentral verwalteten Zielgruppen durchführen, z. B. eine Audience mit hoher Abbruchrate erstellen. |
| **Zentralisierte Zielgruppenerstellung** - Erstellen Sie regelbasierte oder KI-gestützte Zielgruppen basierend auf dem Onsite-Verhalten, früheren Käufen, Profilattributen, Kategorieaffinitäten, Treuestatus, Kundenwert und mehr | **Adobe [!DNL Commerce] Nur**:<br>Erfassen Sie Kundenprofilinformationen, wenn [!DNL Commerce] -Kunden Konten erstellen. Erstellen Sie regelbasierte [Kundensegmente](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/segments/customer-segments) und Kundengruppen, um Inhalte und Promotions zu personalisieren.<br>**Adobe [!DNL Commerce] mit Adobe Real-Time CDP**:<br> [Einheitliche Profile](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/home) aus allen Datenquellen und Kanälen; regelbasierte oder KI-gestützte Zielgruppen. |
| **Personalisiertes E-Mail-/SMS-Angebot basierend auf dem Kaufverhalten** - Senden Sie personalisierte Angebote an Kunden über zielgerichtete E-Mails, die auf früheren Käufen und dem Kaufverhalten basieren, z. B. Senden von Angeboten für Produkte oder Kategorien, mit denen Kunden interagiert haben. | **Adobe [!DNL Commerce] Only**:<br>Exportieren Sie Daten zur Verwendung mit Marketing-Automatisierungslösungen.<br>**Adobe [!DNL Commerce] mit Adobe Journey Optimizer und Real-Time CDP**:<br>[!DNL Commerce] -Daten dienen als Trigger für E-Mail- oder SMS-Angebote und liefern Signale (Verhaltensweisen von Käufern), die personalisiert werden können. Real-Time CDP ist nicht erforderlich, aber im Allgemeinen werden diese Angebote und Kampagnen für Zielgruppen erstellt, die in Real-Time CDP erstellt und verwaltet werden. |
| **Kompatible Produkte/Marken mit Cross- oder Upsell-Funktion** - Wenn ein Kunde ein Produkt oder eine Marke kauft, das/die kompatibel ist oder eine hohe Affinität zu einem anderen Produkt oder einer anderen Marke anzeigt, senden Sie eine Kampagne (E-Mail/SMS), um die Konversionsrate zu fördern. | **Adobe [!DNL Commerce] Only**:<br>Verwenden Sie Adobe [!DNL Commerce] [Product Recommendations](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/guide-overview), um bestimmte Produkte auf der Site zu empfehlen. Sie können auch [Zugehörige Produktregeln](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/product-relationships/product-related-rules) verwenden, um andere Produkte vorzuschlagen.<br>**[!DNL Commerce] mit [!DNL Target]**:<br>Adobe [!DNL Target] verfügt auch über eine integrierte Produktempfehlungsmodul mit leistungsstarken Funktionen wie Kategorieaffinität. Dies kann für Cross- oder Upsell verwendet werden.<br>**[!DNL Commerce] mit Adobe Journey Optimizer**:<br>Verwenden Sie [!DNL Target] oder [!DNL Commerce], um die zu empfehlenden Produkte zu bestimmen und dann über Adobe Journey Optimizer bereitzustellen. |

### Personalisierte Site-Erlebnisse

| Anwendungsfall | Lösung |
|---|---|
| **Personalisierte Site-Inhalte** - Personalisieren Sie Site-Banner und andere Seiteninhalte basierend auf Käuferaktionen, z. B. Produktbrowsing und Kategorieaffinitäten. Stellen Sie Inhalte bereit, die auf den Ergebnissen von A/B-Tests oder Geschäftszielen basieren. | **Adobe [!DNL Commerce] Only**:<br>Stellen Sie segmentspezifische [dynamische Inhaltsbausteine bereit](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks).<br>**[!DNL Commerce] mit Real-Time CDP **:<br>Verwenden Sie [Audience Activation](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation), um zielgruppenspezifische dynamische Inhaltsbausteine bereitzustellen, die auf Echtzeitaktionen und einheitliche Kundenprofildaten reagieren, während Profile und Zielgruppen in Real-Time CDP zentral verwaltet werden.<br>**[!DNL Commerce] mit[!DNL Target]**:<br>Personalisieren Sie alle Teile des Site-Erlebnisses, einschließlich Inhalt, Navigationselemente, vollständiger Seitenlayouts und mehr, mithilfe von Adobe [!DNL Commerce]-Daten in Adobe [!DNL Target]. A/B-Test-Inhalte automatisch auswählen und für jeden Kunden bereitstellen.<br>**[!DNL Commerce] mit AEM Assets **:<br>Speichern Sie alle Ihre Inhalte in Adobe Experience Manager Assets. Nativer Zugriff auf diesen Inhalt über Adobe Commerce. Verwenden Sie Generative KI, um Inhaltsvarianten zu erstellen und für verschiedene Segmente oder Zielgruppen zu personalisieren. |
| **Personalisiertes Onsite-Angebot basierend auf Verhalten** - Personalisieren Sie Promotions anhand von Käuferaktionen, wie z. B. Produktsuche und Kategorieaffinitäten. Stellen Sie das nächste beste Angebot basierend auf den Ergebnissen von A/B-Tests oder Geschäftszielen bereit. | **Adobe [!DNL Commerce] Only**:<br>Bereitstellen des segmentspezifischen Katalogs und [Regeln zum Warenkorb-Preis](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart).<br>**Adobe [!DNL Commerce] mit Real-Time CDP**:<br>Verwenden Sie [Audience Activation](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation), um zielgruppenspezifische Angebote bereitzustellen und gleichzeitig Profile/Zielgruppen in Real-Time CDP zentral zu verwalten.<br>**Commerce mit[!DNL Target]**: Verwenden Sie offer decisioning, um zu bestimmen, welches Angebot bereitgestellt werden soll, A/B-Tests durchzuführen oder Geschäftsziele festzulegen, die als Leitfaden für in Adobe Commerce bereitgestellte Angebote dienen. |

### Analytics und Einblicke

| Anwendungsfall | Lösung |
|---|---|
| **Kundenverhalten nach Kanal** - Machen Sie sich mit den Nuancen der Kundeninteraktionen in den einzelnen Kanälen (Web, persönlich, App usw.) vertraut, um die Marketingstrategien für die einzelnen Kanäle zu beeinflussen. Verstehen Sie den Einkaufstrichter und die Schwächen im Kundenerlebnis. | **Adobe [!DNL Commerce] Nur**:<br>[Adobe [!DNL Commerce] Intelligence](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started) bietet Rich-Analytics auf dem digitalen Kanal [!DNL Commerce], jedoch nicht kanalübergreifend oder in größeren Teilen der Journey.<br>**Adobe [!DNL Commerce] mit Customer Journey Analytics**:<br>[!DNL Commerce] Daten-Dashboards werden in allen Phasen des Kundenerlebnisses (kanalübergreifend) für umfassende Details bereitgestellt. Machen Sie sich mit jedem Touchpoint und dem breiteren Trichter vertraut, um Schwachstellen in der Journey zu identifizieren, an denen Kunden abstürzen können. |
| **Kauftrends** - Verstehen Sie Kaufverhaltensweisen über einen bestimmten Zeitraum (z. B. Warenkorbanalyse, Produktanalyse), um Trends und Saisonabhängigkeit zu identifizieren und das Marketing basierend auf historischen Kaufmustern zu optimieren. | **Adobe [!DNL Commerce] Nur**:<br>[Adobe [!DNL Commerce] Intelligence](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started) bietet Rich-Analytics auf dem digitalen Kanal [!DNL Commerce], jedoch nicht kanalübergreifend oder in größeren Teilen der Journey.<br>**Adobe [!DNL Commerce] mit Customer Journey Analytics**:<br>[!DNL Commerce] Daten-Dashboards werden in allen Phasen des Kundenerlebnisses (kanalübergreifend) für umfassende Details bereitgestellt. Machen Sie sich mit jedem Touchpoint und dem breiteren Trichter vertraut, um Schwachstellen in der Journey zu identifizieren, an denen Kunden abstürzen können. |

## Anwendungsbeispiele

- Erfahren Sie, wie Sie Adobe Journey Optimizer verwenden können, um [eine E-Mail mit stehendem Warenkorb zu senden](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/use-cases/using-ajo).
- Erfahren Sie, wie Sie [eine Zielgruppe in Real-Time CDP erstellen](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/use-cases/create-audience), um eine Warenkorbpreisregel in Adobe [!DNL Commerce] zu informieren.
