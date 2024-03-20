---
title: Skalierte Personalisierung
description: Erfahren Sie, welche Funktionen in Adobe Commerce es Ihnen ermöglichen, ein personalisiertes Erlebnis für Ihre Kunden zu erstellen.
feature: Customers, Storefront, Personalization
source-git-commit: a4eeda918adcb74ad5e7008b80eff703fa15e878
workflow-type: tm+mt
source-wordcount: '1341'
ht-degree: 0%

---

# Skalierte Personalisierung

&#x200B; Personalisierung im Maßstab ermöglicht es Unternehmen, das Einkaufserlebnis für jeden Kunden-Touchpoint basierend auf dem unmittelbaren Kontext und dem zuvor beobachteten Verhalten zu personalisieren. Ziel ist es, jedes Mal das relevanteste und personalisierteste Erlebnis zu präsentieren.

Laden Sie die [_Erste Schritte mit Personalisierung im Maßstab_](https://business.adobe.com/resources/reports/getting-started-with-personalization-at-scale.html) Bericht.

Zum Erstellen eines personalisierten Einkaufserlebnisses müssen Sie sich über die Datentypen informieren, die zum Verständnis des Kundenkontexts erforderlich sind. Dort erfahren Sie mehr über Adobe Commerce-Funktionen, die diese Daten verwenden, um die Kundeneinblicke zu erhalten, die Sie zum Erstellen eines personalisierten Einkaufserlebnisses benötigen.

Die folgende Abbildung zeigt die Konzepte zur Personalisierung des Einkaufserlebnisses:

![Erstellen einer Personalisierungspipeline](assets/personalization-journey.png){width="700" zoomable="yes"}

In diesem Artikel werden die oben genannten Konzepte ausführlicher erläutert.

## Wie personalisieren Sie das Einkaufserlebnis?

Eine erfolgreiche Personalisierung beginnt mit dem Kundenkontext. In diesem Abschnitt erfahren Sie mehr über die Datentypen, die Ihnen beim Erstellen des Kundenkontexts zur Verfügung stehen.

### Store-Daten

Storefront-Daten, auch Verhaltensdaten oder Browserdaten genannt, können Einblicke in die Interaktion Ihrer Kunden mit Ihrer Site vermitteln. Beispiel:

- An welchen Produkten und Kategorien interessieren sich meine Käufer am meisten?
- Welche Art von Suchabfragen sind meine Käufer am meisten beschäftigt?
- Füllen meine Käufer Produkte zum Warenkorb und geben ihn dann auf?
- Verwenden meine Käufer einen Desktop- oder einen mobilen Browser?

Die folgenden Storefront-Ereignisse erfassen Daten, die Ihnen bei der Beantwortung dieser Fragen helfen können:

- [pageView](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [searchRequestSent](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [searchResponseReceived](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [productPageView](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [addToCart](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [openCart](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [signIn](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [signOut](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [startCheckout](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [completeCheckout](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [createRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [addToRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [removeFromRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)

### Backoffice-Daten

Back Office-Daten, auch Server-seitige Daten genannt, können Einblicke in den Auftragslebenszyklus liefern. Beispiel:

- Gibt es Produkte, die häufiger je nach Saison gekauft werden?
- Gibt es bei meinen Käufern Produkte zurück?
- Wie kann ich den Lebenszeitkundenwert berechnen?

Die folgenden Back-Office-Ereignisse erfassen Daten, die Ihnen bei der Beantwortung dieser Fragen helfen können:

- [orderPlaced](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [orderItemsReturnedInitiated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [orderItemsShipped](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [orderCancelled](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)

### Kundenprofil und Segmentdaten

Kundenprofildaten können Einblicke in die Identität Ihrer Kunden und die Segmente, für die sie sich qualifizieren, liefern. Beispiel:

- Name
- Geschlecht
- Adresse
- Treuestatus
- Telefonnummer
- Email-Adresse
- Treuestatus
- Telefonnummer
- Email-Adresse
- Berechtigung für Upgrades
- Cross-Channel-Käufer
- Perspektiven für neue Produkte
- Treuemitglieder aus Gold, Silber oder Bronze

Die folgenden Profilereignisse erfassen Daten, die Ihnen bei der Beantwortung dieser Fragen helfen können:

- [Profildatensatz](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-profilerecord)
- [accountCreated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [accountUpdated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [accountDeleted](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)

Storefront-, Back-Office- und Profildaten bilden die Grundlage des Commerce-Kunden- und Bestellkontexts, der Ihnen hilft zu wissen, welche Produkte Ihre Kunden anzeigen und schließlich kaufen. Anschließend können Sie ihre Interessen verfolgen und ihre Erlebnisse personalisieren. Im nächsten Abschnitt erfahren Sie, welche Arten personalisierter Erlebnisse Sie mit Ihren Kunden verbinden können.

## Typen von personalisierten Erlebnissen

Die Kontextdaten für Kunden und Bestellungen in Commerce unterstützen die folgenden Arten personalisierter Erlebnisse:

| Erlebnis | Beschreibung |
|---|---|
| **Produktsuche** | Enthält Merchandising-Dienste, die [bereitgestellt als SaaS](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/user-guides/integration-services/saas). Diese Funktionen ermöglichen Ihnen die Verwendung von Verhaltensdaten, Produktattributen und Bestandsebene, um die Produkterkennung über Suchergebnisse, Produktempfehlungen und Durchsuchen-Seiten hinweg automatisch zu personalisieren. Alle Funktionen verwenden [Adobe Sensei AI](https://business.adobe.com/products/sensei/adobe-sensei.html). |
| **Site-Content** | Bezieht sich auf die Möglichkeit, basierend auf dem aktuellen Kunden, der Ihre Site durchsucht, personalisierte dynamische Inhaltsbausteine bereitzustellen. |
| **Angebote und Kampagnen** | Ermöglicht die Bereitstellung personalisierter Werbeinhalte basierend auf Segmentdaten. |
| **Messung** | Verwendet Data Intelligence, um Ihr Geschäft besser zu verstehen, einschließlich Umsatz, Kanal- und Merchandising-Leistung, Promotions usw. |

In den nächsten beiden Abschnitten erfahren Sie, wie Sie diese Daten verwenden können, um personalisierte Erlebnisse in [Adobe Experience Platform](#using-commerce-data-in-adobe-experience-platform) und [Native Commerce-Funktionen](#using-commerce-data-in-native-commerce-features).

## Verwenden von Commerce-Daten in Adobe Experience Platform

Um ein personalisiertes Erlebnis für Ihre Kunden über alle Kanäle hinweg zu erstellen, senden Sie Ihre Commerce-Daten mithilfe des [[!DNL Data Connection]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/overview) -Erweiterung.

![Datenfluss zum Experience Platform-Edge](assets/commerce-edge.png){width="700" zoomable="yes"}

In der obigen Abbildung werden Ihre Storefront-, Back-Office- und Kundenprofildaten mithilfe eines SDK, einer API und eines Quell-Connectors an die Experience Platform Edge gesendet. Sie müssen nicht vollständig verstehen, wie diese Teile funktionieren, da die Erweiterung die Komplexität der Datenweitergabe für Sie handhabt. Wenn sich die Ereignisdaten am Rand befinden, können Sie diese Daten in andere Experience Platform-Anwendungen ziehen.

In der folgenden Tabelle werden einige der verfügbaren Experience Platform-Anwendungen und die Verwendung Ihrer Commerce-Daten durch diese Anwendungen erläutert.

| Erlebnis | Anwendung | Verwendung von Commerce-Daten |
|---|---|---|
| **Site-Content** | [Adobe [!DNL Real-Time CDP]](https://experienceleague.adobe.com/en/docs/experience-platform/rtcdp/intro/rtcdp-intro/overview) | Adobe Commerce-Daten ermöglichen die Integration von Kundenprofilen, wobei Real-Time CDP Daten aus verschiedenen Quellen (ERP, CRM, CMS, POS) in einzelne Profile zusammenführt. Real-Time CDP kann auch regelbasierte und KI-basierte Segmente erstellen, die dann für alle Marketinglösungssätze verwendet werden. Sie können Real-Time CDP-Zielgruppen auch verwenden, um Inhaltsbausteine, Promotions und zugehörige Produktregeln zu personalisieren. Siehe [[!DNL Audience Activation]](../customers/audience-activation.md) Weitere Informationen &#x200B; |
|  | [Adobe [!DNL Target]](https://experienceleague.adobe.com/en/docs/target/using/introduction/intro) | Adobe Commerce-Daten können in Adobe aktiviert werden [!DNL Target] zum Testen, Optimieren und Erstellen dynamischer Landingpages. Sie können die Reihenfolge personalisieren, in der Inhalte auf einer Seite angezeigt werden, z. B. Beschreibungen, Spezifikationen, Überprüfungen und empfohlene Produkte, basierend auf den gesendeten Commerce-Daten. |
| **Angebote und Kampagnen** | [Adobe [!DNL Journey Optimizer]](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/get-started) | Verhaltensdaten und Back-Office-Daten von Adobe Commerce können als Trigger für personalisierte kanalübergreifende Journey dienen, darunter E-Mail-Kampagnen, SMS, Push-Benachrichtigungen und mehr. &#x200B; |
| **Messung** | [Adobe [!DNL Analytics]](https://experienceleague.adobe.com/en/docs/analytics/analyze/admin-overview/analytics-overview) und [Kunde [!DNL Journey Analytics]](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview) | Commerce sendet sowohl Storefront- als auch Back-Office-Daten an den Kunden [!DNL Journey Analytics] (und nur Storefront-Daten an Adobe [!DNL Analytics]), um eine umfassendere Analyse über grundlegende Metriken in Adobe Commerce Intelligence hinaus zu ermöglichen, wie Umsatz, Waren und Promotions. &#x200B; |

Weitere Informationen dazu, wie Sie Ihre Commerce-Daten an die Experience Platform senden können, finden Sie unter [Datenverbindung](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/overview).

## Verwenden von Commerce-Daten in nativen Commerce-Funktionen

Im folgenden Abschnitt erfahren Sie, wie Sie native Commerce-Funktionen wie Produkt-Recommendations und Live Search verwenden können, um ein personalisiertes Einkaufserlebnis zu erstellen. Außerdem erfahren Sie mehr über eine Funktion mit dem Namen [!DNL Audience Activation], bei dem, wie bereits erwähnt, Daten aus einem in der Experience Platform verfügbaren Produkt namens Real-Time CDP verwendet werden [before](#using-commerce-data-in-adobe-experience-platform). Real-Time CDP ist zwar nicht nativ für Commerce, aber seine Informationen können über die [[!DNL Audience Activation]](../customers/audience-activation.md) -Erweiterung.

In der folgenden Tabelle werden die Commerce-Funktionen vorgestellt, mit denen Commerce-Kunden- und Bestellkontextdaten in umsetzbare Einblicke umgewandelt werden können.

| Erlebnis | Funktion | Beschreibung |
|---|---|---|
| **Produktsuche** | [Live Search](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/guide-overview) | Verwendet KI-Rangalgorithmen, um Suchergebnisse basierend auf den Verhaltensaktionen eines Käufers vor Ort zu personalisieren und zu optimieren, wodurch die Suchrelevanz und Konversion erhöht werden. |
|  | [Produkt-Recommendations](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/guide-overview) | Zeigt KI-gestützte Produktempfehlungen basierend auf dem Kaufverhalten, Trends, der Produktähnlichkeit und mehr an. In Kombination mit Ihrem Adobe Commerce-Katalog bieten Produktempfehlungen ein sehr ansprechendes, relevantes und personalisiertes Erlebnis. |
|  | [Kategorie-Merchandising](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-admin/category-merch) | Kategorievermarktung, auf die über den Live-Suchadministrator zugegriffen wird, verwendet KI, um die Produktsequenz auf jeder Kategorieseite automatisch neu zu ordnen, um die Relevanz und Konversion für jeden Käufer zu steigern. Sie können KI-gestützte Regeln erstellen und verwalten, um die Produktreihenfolge auf Kategorieseiten automatisch entsprechend den Aktionen und Affinitäten des Käufers neu zu ordnen. |
| **Site-Content** | [Dynamische Bausteine, die von nativen Commerce-Funktionen unterstützt werden](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks) | Ermöglicht die Bereitstellung personalisierter Site-Inhalte basierend auf der in den Preisregeln und Kundensegmenten konfigurierten Logik. |
|  | [Von Real-Time CDP-Zielgruppen informierte dynamische Bausteine](../customers/audience-activation.md) | Ermöglicht Händlern die Bereitstellung personalisierter Site-Inhalte basierend auf in Real-Time CDP konfigurierten Zielgruppen. |
| **Angebote und Kampagnen** | [Preisregeln für Warenkorb](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart) | Ermöglicht Ihnen, Rabatte auf Artikel im Warenkorb auf der Grundlage einer Reihe von Bedingungen anzuwenden. |
|  | [Dynamische Bausteine, die von nativen Commerce-Funktionen unterstützt werden](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks) | Ermöglicht die Anzeige personalisierter Banneraktionen basierend auf Kundensegmenten, die nativ in Commerce konfiguriert wurden. |
|  | [Von Real-Time CDP-Zielgruppen informierte dynamische Bausteine](../customers/audience-activation.md) | Ermöglicht die Anzeige personalisierter Promotions basierend auf in Real-Time CDP konfigurierten Zielgruppen. |
| **Messung** | [Adobe Commerce Intelligence](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started) | (Zuvor als Magento Business Intelligence bezeichnet) ist eine Cloud-Plattform, die Best Practice-Einblicke bietet, mit deren Hilfe Sie datengesteuerte Entscheidungen treffen und klare und fundierte Maßnahmen treffen können. Adobe Commerce Intelligence kann Ihre Daten analysieren, um Ihnen bei der Beantwortung von Fragen zum Auftragswachstum, zum Kundenverhalten und zur Effektivität von Werbestrategien zu helfen. |
