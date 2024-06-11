---
title: Erstellen ansprechender, personalisierter Erlebnisse im Maßstab
description: Erfahren Sie, welche Funktionen im Adobe verfügbar sind [!DNL Commerce] ermöglichen es Ihnen, ein personalisiertes Erlebnis für Ihre Kunden zu erstellen.
feature: Customers, Storefront, Personalization
exl-id: 9546e1b8-796b-4694-8396-773a2b0e9c12
source-git-commit: 728a1fdb413009a00377cd8205dde93cd4feadc8
workflow-type: tm+mt
source-wordcount: '1808'
ht-degree: 0%

---

# Erstellen ansprechender, personalisierter Erlebnisse im Maßstab

Adobe [!DNL Commerce] bietet Ihnen ein leistungsstarkes Toolkit zur Personalisierung jedes Touchpoints beim Kunden, wodurch die Interaktion, Konversion und der Umsatz der Kunden gesteigert werden.

In diesem Artikel erfahren Sie:

- Was ist Personalisierung?
- Welche Daten benötige ich für die Personalisierung?
- Wie funktioniert Adobe? [!DNL Commerce] Personalisierung entsperren?
- Verfügbare Personalisierungsanwendungsfälle

## Was ist Personalisierung?

Personalisierung bedeutet, die Aspekte des Kauferlebnisses jedes Kunden an seine individuellen Bedürfnisse, Umstände und Vorlieben anzupassen. Die Personalisierung beschränkt sich nicht auf Inhalte auf der Site oder empfiehlt passende Produkte, sondern umfasst alle Touchpoints auf der gesamten Journey, einschließlich:

- **Kampagnen und Kommunikation** - Bereitstellung relevanter und konsistenter Nachrichten über Kampagnen und Kommunikation
- **Produktsuche** - Anzeige der richtigen Produkte für die richtigen Kunden in den richtigen Augenblicken
- **Promotions und Angebote** - Targeting von Promotions und Angeboten, um jeden Kunden zur Konversion zu bewegen
- **Inhaltserlebnisse** - Anpassen von Site-Inhalten, um sich für jeden Kunden und dessen Journey hyper zu fühlen

![Personalisierungstypen](assets/types-personalization.png){width="700" zoomable="yes"}

Diese Arten personalisierter Erlebnisse können für eine kleine Untergruppe von Kunden zwar erreichbar sein, für Tausende oder Millionen von Kunden über jeden Touchpoint und jeden Kanal personalisiert werden, aber in Echtzeit kann sich dies als unmöglich erweisen. In den folgenden Abschnitten erfahren Sie, wie Adobe [!DNL Commerce] und Adobe Experience Cloud können helfen.

## Welche Daten benötige ich für die Personalisierung?

Eine effektive Personalisierung erfordert Kontext oder Signale, die Informationen über Kunden bereitstellen, die dann zur Änderung ihres Erlebnisses verwendet werden können. Die folgende Tabelle enthält die verschiedenen Datentypen und die Rolle, die das Adobe [!DNL Commerce] unterstützt die Erfassung und Aktivierung dieser Daten.

| Datentypen | Storefront-Daten (Verhaltensereignisse) | Back Office Data (Server-Side Events) | Kundenprofil und Segmentdaten |
|---|---|---|---|
| **Definition** | Klicks oder Aktionen, die Kunden auf Ihrer Site ausführen. | Informationen zum Lebenszyklus und Details der einzelnen Bestellungen (Vergangenheit und aktuell). | Wer Ihre Käufer sind und für welche Segmente sie sich qualifizieren. |
| **Von Adobe Commerce erfasste Ereignisse** | [pageView](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#pageview)<br>[productPageView](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)<br>[searchRequestSent](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#searchrequestsent)<br>[searchResponseReceived](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#searchresponsereceived)<br>[addToCart](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#addtocart)<br>[openCart](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#opencart)<br>[signIn](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#signin)<br>[signOut](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#signout)<br>[startCheckout](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#startcheckout)<br>[completeCheckout](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#completecheckout)<br>[createRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#createrequisitionlist)<br>[addToRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#addtorequisitionlist)<br>[removeFromRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events#removefromrequisitionlist) | **Bestellstatus**:<br>[orderPlaced](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#orderplaced)<br>[orderItemsReturnedInitiated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#orderitemsreturnedinitiated)<br>[orderItemsShipped](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#orderitemsshipped)<br>[orderCancelled](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#ordercancelled)<br>[**Auftragsverlauf**](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/fundamentals/connect-data#send-historical-order-data):<br>- SKU, Name, Preismenge, Rabatt<br>- Produktkategorie<br>- Zahlungsbetrag, Art, Währung<br>- Versandmethode und -betrag<br>- Rückerstattungs-ID, Betrag, Währung<br>- Grund für die Rückgabe, Bedingung, Auflösung<br>- Adresse<br>- E-Mail | [**Profildatensatz**](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-profilerecord): (Name, Geschlecht, Adresse, Treuestatus, Telefonnummer, E-Mail-Adresse)<br>**Kontostatus**:<br>[accountCreated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#accountcreated)<br>[accountUpdated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#accountupdated)<br>[accountDeleted](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice#accountdeleted) |

Mit all diesen reichen Erstanbietern [!DNL Commerce] -Daten verwenden, können Sie das Erlebnis jedes einzelnen Käufers gezielt ansprechen und personalisieren. Im nächsten Abschnitt erfahren Sie, wie Sie [!DNL Commerce] Mit Adobe Experience Cloud können Sie personalisierte Erlebnisse und Anwendungsfälle erstellen, die Sie aktivieren können.

## Wie funktioniert Adobe? [!DNL Commerce] Personalisierung optimieren?

Adobe [!DNL Commerce] Mit der Datenfreigabe können Sie die Datentypen der vorherigen Tabelle erfassen und für andere Adobe Experience Cloud-Produkte freigeben, um einheitliche Kundenprofile und -zielgruppen, personalisierte Kampagnen sowie umfassende Analysen und Einblicke zu ermöglichen.

![Datenfluss zum Experience Platform-Edge](assets/commerce-edge.png){width="700" zoomable="yes"}

Adobe [!DNL Commerce] Die Datenfreigabe umfasst zwei wichtige Komponenten:

1. [Datenverbindung](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/overview): Freigeben von Storefront-, Back-Office- und Kundenprofildaten von Adobe [!DNL Commerce] zum Adobe Experience Platform Edge-Netzwerk zur Verwendung in Adobe Experience Cloud-Anwendungen, einschließlich:

   - [Adobe [!DNL Real-Time CDP]](https://experienceleague.adobe.com/en/docs/experience-platform/rtcdp/intro/rtcdp-intro/overview): Verknüpfen Sie Kundendaten aus verschiedenen Quellen (ERP, CRM, POS) mit einheitlichen Profilen und erstellen Sie regelbasierte oder AI-basierte Segmente.
   - [Adobe [!DNL Journey Optimizer]](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/get-started): Starten Sie personalisierte Omni-Channel-Journey, einschließlich E-Mail-Kampagnen, SMS, Push-Benachrichtigungen und mehr.
   - [Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview) und [Adobe [!DNL Analytics]](https://experienceleague.adobe.com/en/docs/analytics/analyze/admin-overview/analytics-overview): Erhalten Sie Einblicke in den Kunden und das Unternehmen.
   - [Adobe [!DNL Target]](https://experienceleague.adobe.com/en/docs/target/using/introduction/intro): Testen und optimieren Sie Inhalte, empfohlene Produkte, Angebote, Navigation und mehr.

1. [[!DNL Audience Activation]](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation): Verwenden Sie [!DNL Real-Time CDP] Zielgruppen, um dynamische Inhaltsbausteine, Promotions und zugehörige Produktregeln auf Ihrer Adobe zu personalisieren. [!DNL Commerce] Site.

### Personalisierte Storefront-Erlebnisse für alle Kanäle im großen Maßstab

Adobe [!DNL Commerce] kann die Vorteile einer leistungsstarken Storefront mit dem Namen [Edge Delivery Services](https://experienceleague.adobe.com/developer/commerce/storefront/), um personalisierte Erlebnisse über alle Ihre Kanäle hinweg bereitzustellen, mit KI-Funktionen im Kern und Geschwindigkeit als Grundlage.

Mit Edge Delivery Services können Sie:

- **Personalisierte Inhalte erstellen**: Verwenden Sie dokumentbasiertes Authoring und native Experimente mit generativen KI-Text- und Bildvarianten, um das Erlebnis skaliert zu personalisieren. Verwenden Sie Assets und die Generative AI-Inhaltserstellung, um skaliert Produkt- und Marketing-Bilder zu erstellen.

- **Generieren von Varianten**: Ermöglicht es Inhaltsautoren, mithilfe der generativen KI große Mengen personalisierter KI zu erstellen [Textinhalt und Bildvarianten](https://experienceleague.adobe.com/en/docs/experience-manager-learn/sites/generative-ai/generate-variations) mit Adobe Firefly.

- **Bereitstellen über Edge Delivery Services Storefront**: Content on the Edge and Commerce-Funktionen basierend auf Dropdown-Komponenten, um für Ihre Zielgruppen maßgeschneiderte Shopping-fähige Erlebnisse zu erstellen.

- **Commerce und Adobe Experience Manager Assets**: Generative KI-Produktsortimente und Skalierungsversionen. Erstellen, liefern und überwachen Sie die Inhaltsbereitstellung über jeden Kanal hinweg.

![Dropins: Produktdetailseite](assets/drop-in.png){width="700" zoomable="yes"}

### Vordefinierte Personalisierung: Erste Schritte mit nativem Adobe [!DNL Commerce] Funktionen

Adobe [!DNL Commerce] bietet leistungsstarke Personalisierung mit nativen nativen Funktionen. Die folgende Tabelle beschreibt Folgendes [!DNL Commerce] Funktionen können Sie sofort aktivieren, um mit der Personalisierung-Journey zu beginnen.

| Kategorie | Funktionen |
|---|---|
| Personalisierte Produkterkennung | [[!DNL Live Search]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/overview): Personalisieren und optimieren Sie Suchergebnisse basierend auf den verhaltensbezogenen Aktionen und Affinitäten eines Käufers auf der Site mit KI-gestützter Suche.<br>[Intelligent Category Merchandising](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-admin/category-merch): KI-gesteuertes Produktranking auf Kategorieseiten basierend auf den Verhaltensaktionen und Affinitäten eines Käufers vor Ort.<br>[Produkt-Recommendations](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/guide-overview): KI-gestützte Produktempfehlungen, die auf dem Verhalten, den Trends und den Affinitäten der Käufer basieren.<br>[Verwandte Produktregeln](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/product-relationships/product-related-rules): Definieren Sie benutzerdefinierte Regeln, um Produkte aus Ihrem Katalog anzuzeigen und so Cross- und Up-Sell zu fördern. |
| Personalisierte Site-Inhalte | [Dynamische Inhaltsbausteine](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks): Zeigt personalisierte Inhaltsbausteine an, z. B. Banner, die auf Kundensegmenten in Adobe Commerce basieren. |
| Personalisierte Angebote und Promotions | [Warenkorbpreisregeln](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart): Wenden Sie Rabatte auf Artikel im Warenkorb an, die auf einer Reihe von Bedingungen basieren, einschließlich Kundensegmenten im Adobe. [!DNL Commerce]. |
| Einblicke und Messung | [Adobe [!DNL Commerce] Intelligence](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started): Erfahren Sie, wie Ihre Personalisierungsstrategien funktionieren und sich im Laufe der Zeit verbessern. |

## Häufigste Personalisierungs-Anwendungsfälle

Adobe [!DNL Commerce] -Kunden nutzen für eine Vielzahl von Anwendungsfällen vordefinierte Funktionen und teilen Daten an Adobe Experience Cloud. In den folgenden Abschnitten werden die wichtigsten Anwendungsfälle hervorgehoben und beschrieben, wie sie mithilfe von Adobe implementiert werden [!DNL Commerce] Nur oder [!DNL Commerce] und Experience Cloud-Apps.

### Personalisierte Kampagnen und Kommunikation

| Anwendungsfall | Lösung |
|---|---|
| **Warenkorb abgebrochen und durchsuchen** - Bereitstellen einer personalisierten E-Mail zur erneuten Interaktion oder Benachrichtigung, wenn ein Kunde seinen Warenkorb oder seine Browser-Sitzung nach der Demonstration einer hohen Interaktion beendet | **Adobe [!DNL Commerce] Nur**:<br>[E-Mail-Erinnerungen](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/communications/email-reminders/email-reminder-rules)<br>**Adobe [!DNL Commerce] mit Adobe Journey Optimizer**:<br>[!DNL Commerce] data dient als Trigger für eine kanalübergreifende Abbruch-Journey. Personalisieren Sie diese Journey anhand von Kundenattributen, abgebrochenen Artikeln, anderen Kaufverhaltensweisen und früheren Käufen.<br>Commerce mit Adobe Journey Optimizer und Real-Time CDP: Kampagnen für abgebrochene Suche auf der Basis von einheitlichen Kundenprofilen und zentral verwalteten Zielgruppen erstellen, z. B. eine Audience mit hoher Abbruchrate. |
| **Zentralisierte Zielgruppenerstellung** - Erstellen Sie regelbasierte oder KI-basierte Zielgruppen basierend auf dem Verhalten vor Ort, früheren Käufen, Profilattributen, Kategorieaffinitäten, Treuestatus, Kundenwert und mehr | **Adobe [!DNL Commerce] Nur**:<br>Erfassen Sie Kundenprofilinformationen, wenn [!DNL Commerce] -Kunden Konten erstellen. Regelbasiert erstellen [Kundensegmente](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/segments/customer-segments) und Kundengruppen , um Inhalte und Promotions zu personalisieren.<br>**Adobe [!DNL Commerce] mit Adobe Real-Time CDP**:<br> [Einheitliche Profile](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/home) aus Datenquellen und Kanälen; regelbasierte oder KI-gestützte Zielgruppen. |
| **Personalisierte E-Mail-/SMS-Angebote basierend auf dem Kaufverhalten** - Senden Sie personalisierte Angebote an Kunden über zielgerichtete E-Mails, die auf früheren Käufen und dem Kaufverhalten basieren, z. B. Senden von Angeboten für Produkte oder Kategorien, mit denen Kunden interagiert haben. | **Adobe [!DNL Commerce] Nur**:<br>Exportieren Sie Daten zur Verwendung mit Lösungen zur Marketing-Automatisierung.<br>**Adobe [!DNL Commerce] mit Adobe Journey Optimizer und Real-Time CDP**:<br>[!DNL Commerce] -Daten dienen als Trigger für E-Mail- oder SMS-Angebote und bieten Signale (Verhaltensweisen von Käufern), auf denen Personalisierungen durchgeführt werden können. Real-Time CDP ist nicht erforderlich, aber im Allgemeinen werden diese Angebote und Kampagnen für Zielgruppen erstellt, die in Real-Time CDP erstellt und verwaltet werden. |
| **Kompatible Produkte/Marken übergreifend oder hochverkaufen** - Wenn ein Kunde ein Produkt oder eine Marke kauft, das bzw. die kompatibel ist oder eine hohe Affinität zu einem anderen Produkt oder einer anderen Marke anzeigt, senden Sie eine Kampagne (E-Mail/SMS), um die Konvertierung über Querverkäufe zu fördern. | **Adobe [!DNL Commerce] Nur**:<br>Adobe verwenden [!DNL Commerce] [Produkt-Recommendations](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/guide-overview) , um bestimmte Produkte auf der Site zu empfehlen. Sie können auch [Verwandte Produktregeln](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/product-relationships/product-related-rules) andere Erzeugnisse vorzuschlagen.<br>**[!DNL Commerce] mit [!DNL Target]**:<br>Adobe [!DNL Target] verfügt außerdem über eine integrierte Produktempfehlungs-Engine mit leistungsstarken Funktionen wie Kategorieaffinität. Dies kann für Cross- oder Upsell verwendet werden.<br>**[!DNL Commerce] mit Adobe Journey Optimizer**:<br>Verwendung [!DNL Target] oder [!DNL Commerce] , um die zu empfehlenden Produkte zu bestimmen, und dann über Adobe Journey Optimizer bereitstellen. |

### Personalisierte Site-Erlebnisse

| Anwendungsfall | Lösung |
|---|---|
| **Personalisierte Site-Inhalte** - Personalisieren von Site-Bannern und anderen Seiteninhalten basierend auf Käuferaktionen wie Produktbrowsing und Kategorieaffinitäten. Stellen Sie Inhalte bereit, die auf den Ergebnissen von A/B-Tests oder Geschäftszielen basieren. | **Adobe [!DNL Commerce] Nur**:<br>Bereitstellen segmentspezifischer [dynamische Inhaltsbausteine](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks).<br>**[!DNL Commerce] mit Real-Time CDP **:<br>Verwendung [Audience Activation](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation) , um zielgruppenspezifische dynamische Inhaltsbausteine bereitzustellen, die auf Echtzeit-Aktionen und einheitliche Kundenprofildaten reagieren, während Profile und Zielgruppen in Real-Time CDP zentral verwaltet werden.<br>**[!DNL Commerce] mit[!DNL Target]**:<br>Personalisieren Sie alle Teile des Site-Erlebnisses, einschließlich Inhalt, Navigationselemente, ganzseitigen Layouts und mehr mithilfe von Adobe. [!DNL Commerce] Daten in Adobe [!DNL Target]. A/B-Test-Inhalte automatisch auswählen und für jeden Kunden bereitstellen.<br>**[!DNL Commerce] mit AEM Assets **:<br>Speichern Sie alle Ihre Inhalte in Adobe Experience Manager Assets. Nativer Zugriff auf diesen Inhalt über Adobe Commerce. Verwenden Sie Generative KI, um Inhaltsvarianten zu erstellen und für verschiedene Segmente oder Zielgruppen zu personalisieren. |
| **Personalisiertes Onsite-Angebot basierend auf Verhalten** - Personalisieren Sie Promotions auf der Basis von Käuferaktionen, wie z. B. Produktsuche und Kategorieaffinitäten. Stellen Sie das nächste beste Angebot basierend auf den Ergebnissen von A/B-Tests oder Geschäftszielen bereit. | **Adobe [!DNL Commerce] Nur**:<br>Bereitstellung des segmentspezifischen Katalogs und [Warenkorbpreisregeln](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart).<br>**Adobe [!DNL Commerce] mit Real-Time CDP**:<br>Verwendung [Audience Activation](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation) , um zielgruppenspezifische Angebote bereitzustellen und gleichzeitig Profile/Audiences in Real-Time CDP zentral zu verwalten.<br>**Commerce mit[!DNL Target]**: Verwenden Sie offer decisioning, um zu bestimmen, welches Angebot bereitgestellt werden soll, um A/B-Tests durchzuführen oder Geschäftsziele festzulegen, die als Leitfaden für in Adobe Commerce bereitgestellte Angebote dienen. |

### Analytics und Einblicke

| Anwendungsfall | Lösung |
|---|---|
| **Kundenverhalten nach Kanal** - Machen Sie sich mit den Nuancen der Interaktion der Kunden mit den einzelnen Kanälen (Web, persönlich, App usw.) vertraut, um die Marketing-Strategien für die einzelnen Kanäle zu beeinflussen; verstehen Sie den Einkaufstrichter und die Schwächen im Kundenerlebnis. | **Adobe [!DNL Commerce] Nur**:<br>[Adobe [!DNL Commerce] Intelligence](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started) bietet umfassende Analysen digitaler [!DNL Commerce] -Kanal, jedoch nicht kanalübergreifend oder in größeren Teilen der Kunden-Journey.<br>**Adobe [!DNL Commerce] mit Customer Journey Analytics**:<br>[!DNL Commerce] Daten-Feeds Daten-Dashboards , um detaillierte Details zu allen Phasen des Kundenerlebnisses (kanalübergreifend) zu erhalten. Machen Sie sich mit jedem Touchpoint und dem breiteren Trichter vertraut, um Schwachstellen in der Journey zu identifizieren, an denen Kunden abstürzen können. |
| **Kauftrends** - Verstehen Sie das Kaufverhalten über einen bestimmten Zeitrahmen (z. B. Warenkorbanalyse, Produktanalyse), um Trends und Saisonabhängigkeit zu identifizieren und das Marketing basierend auf historischen Kaufmustern zu optimieren. | **Adobe [!DNL Commerce] Nur**:<br>[Adobe [!DNL Commerce] Intelligence](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started) bietet umfassende Analysen digitaler [!DNL Commerce] -Kanal, jedoch nicht kanalübergreifend oder in größeren Teilen der Kunden-Journey.<br>**Adobe [!DNL Commerce] mit Customer Journey Analytics**:<br>[!DNL Commerce] Daten-Feeds Daten-Dashboards , um detaillierte Details zu allen Phasen des Kundenerlebnisses (kanalübergreifend) zu erhalten. Machen Sie sich mit jedem Touchpoint und dem breiteren Trichter vertraut, um Schwachstellen in der Journey zu identifizieren, an denen Kunden abstürzen können. |

## Anwendungsbeispiele

- Erfahren Sie, wie Sie mit Adobe Journey Optimizer [E-Mail mit stehendem Warenkorb senden](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/use-cases/using-ajo).
- Erfahren Sie, wie [Erstellen einer Zielgruppe in Real-Time CDP](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/use-cases/create-audience) , um eine Preisregel für den Warenkorb in Adobe zu informieren. [!DNL Commerce].
