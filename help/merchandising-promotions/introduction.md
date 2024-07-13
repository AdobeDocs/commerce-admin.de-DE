---
title: Einführung in Commerce-Merchandising und -Promotions
description: Informieren Sie sich über Commerce-Tools zur Erstellung zielgerichteter Werbeaktionen und Angebote für Kundinnen und Kunden.
exl-id: 8e55ac42-aeef-4f97-b1e8-9b2db354e5e6
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '1094'
ht-degree: 1%

---

# Einführung in Commerce-Merchandising und -Promotions

Targeting von Promotions, Schaffung von Möglichkeiten für Kundeninteraktionen und Umwandlung von Käufern in Käufer. Verwalten Sie Kundenbeziehungen, indem Sie Aktivitäten nach dem Kauf unterstützen und rückkehrenden Kunden spezielle Rabatte anbieten. Lernen Sie Best Practices und Techniken kennen, um Ihre SEO-Initiativen zu unterstützen.

## Merchandising

_Merchandising_ ist ein Begriff, der im Einzelhandel verwendet wird, um die Kunst und Wissenschaft der Entwicklung von Bodenplänen und der Präsentation von Produkten zu beschreiben. Sie können sich die [kategoriebasierte Navigation](../catalog/navigation-top.md) als den Bodenplan des Stores vorstellen und die dynamische Präsentation von Produkten als die Bedingungen, die auf die Auflistung von Produkten im Geschäft angewendet werden können. Sie können auch Programme implementieren, die mehr Produktverkäufe fördern:

- [Visual Merchandiser](visual-merchandiser.md) - Ein Satz erweiterter Tools, mit denen Sie Produkte positionieren und Bedingungen anwenden können, die bestimmen, welche Produkte in der Kategorieliste angezeigt werden.

- [Geschenkregistrierung](gift-registries.md) - Ermöglichen Sie Ihren Kunden die Möglichkeit, Geschenkregister für besondere Anlässe zu erstellen und ihre Freunde und Familie einzuladen, ihre Geschenke aus der Geschenkregistrierung zu kaufen.

- [Prämien und Treue](rewards-loyalty.md) - Verwenden Sie ein Punktesystem, um eindeutige Programme zu implementieren, die die Kundeninteraktion fördern und die Kundenloyalität fördern. Sie können Punkte für eine breite Palette von Transaktions- und Kundenaktivitäten zuweisen und die Punktzahl, Balance und Gültigkeit steuern.

- [Private Verkäufe und Ereignisse](events-private-sales.md) - Verwenden Sie Ihren bestehenden Kundenstamm, um Buzz und neue Leads zu generieren oder überschüssige Bestände durch private Verkäufe und andere Katalogereignisse zu verwerten.

>[!TIP]
>
>Weitere Informationen zu Product Recommendations und dazu, wie diese Ihnen Einblicke und Kontrolle verschaffen können, die Sie benötigen, um das beste Erlebnis für Ihre Käufer zu erstellen, finden Sie im [Benutzerhandbuch für Produkt-Recommendations](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/guide-overview.html).

## Promotions

Verwenden Sie in Adobe Commerce die Promotions-Funktionen, um Produktbeziehungen einzurichten und Preisregeln zu nutzen, um Trigger-Rabatte basierend auf verschiedenen Bedingungen zu nutzen. Sie können Preisregeln verwenden, um Kundenanreize anzubieten, z. B.:

- Senden Sie Ihren besten Kunden einen Gutschein zu einem Rabatt auf ein bestimmtes Produkt
- Kostenloser Versand für Einkäufe über einen bestimmten Betrag
- Eine Promotion für einen bestimmten Zeitraum planen

Eine Regel ist eine Sammlung von Bedingungen (eine oder mehrere), die Preisänderungen auf Produkte anwenden, wenn eine oder alle erfüllt sind. Jede Regel kann mehrere Bedingungen haben, die angewendet werden, wenn alle oder alle (eine oder mehrere, aber nicht alle) Anweisungen wahr oder falsch sind.

### Bedingungen

Bedingungen sind Anweisungen, die die Liste der Produkte verfeinern, und Situationen für die Anwendung der Regel. Die Attribute und Optionen für Bedingungen unterscheiden sich zwischen den verfügbaren Regeltypen. Wenn die Aktion erfüllt ist, wird die Aktion abgeschlossen, z. B. Rabatte, Buy-One-get-one (BOGO) und andere Optionen. Regeln können so einfach oder so kompliziert sein, wie es für Ihre geschäftlichen Anforderungen, saisonalen Rabatten und Promotions sowie für ganzjährige Gelegenheiten erforderlich ist. Sie können beispielsweise einige weitere Optionen für die Feiertage hinzufügen und gleichzeitig den kostenlosen Versand ganzjährig ermöglichen, wenn Warenkörbe eine hohe Zwischensumme aufweisen.

>[!NOTE]
>
>Wenn Sie eine Bedingung basierend auf einem bestimmten Produktattribut definieren möchten, muss **[!UICONTROL Use for Promo Rule Conditions]** für das Attribut in Ihren [Storefront-Eigenschaften](../catalog/attribute-product-create.md) auf `Yes` gesetzt werden.


### Preisregeln

Für [Katalogpreisregeln](price-rules-catalog.md) erstellen Sie Bedingungen, die auf [Attributsätzen](../catalog/attribute-sets.md) in Ihrem Katalog, Ihren Vergleichsfunktionen und ausgewählten Attributen basieren. Man erschafft die Bedingungen wie Sätze, indem man ein paar Aussagen auswählt. Sie können beispielsweise zwei Preisregeln erstellen, um Rabatte für Kinderbekleidung und Herrenbekleidung/Damenbekleidung auf der Grundlage der Kategorie anzuwenden.

![Diagramm - Beispiel für Katalogpreisregeln](./assets/diagram-catalog-price-rules.png){width="500"}

Die Bedingungen der [Preisregel für Warenkorb](price-rules-cart.md) können auf jeder Kategorie basieren, die dem Store [Stamm](../catalog/category-root.md) untergeordnet ist. Preisregeln werden im Voraus festgelegt und werden immer dann wirksam, wenn die erforderlichen Bedingungen erfüllt sind. Diese Regeln verwenden Attribute, einschließlich Produktattribut-Kombinationen, z. B. Übereinstimmung mit einer SKU im Warenkorb mithilfe von Produktattributen. Diese Regeln können auch Bedingungen für die Produktauswahl, Bedingungskombinationen für komplizierte Regeln und Warenkorbattribute wie Zwischensummen verwenden.

![Diagramm - Beispiel für Regeln zum Warenkorbpreis](./assets/diagram-cart-price-rules.png){width="500"}

## Kommunikation und SEO

Die Beherrschung von [Suchmaschinenoptimierung (SEO)](seo-overview.md) ist für potenzielle Käufer von entscheidender Bedeutung. Erfahren Sie mehr über die Suchmaschinenoptimierung und Feinabstimmung des Inhalts und der Präsentation Ihrer Site, um die Art und Weise zu verbessern, wie die Seiten von Suchmaschinen indiziert werden.

Eine der Aufgaben, die vor dem Start Ihres Stores ausgeführt werden müssen, besteht darin, die E-Mail-Vorlagen zu überprüfen, die für alle von Ihrem Store gesendeten Nachrichten verwendet werden, um sicherzustellen, dass sie Ihre Marke widerspiegeln. Sie sollten dies jedoch noch weiter tun, indem Sie andere Kommunikationen entwickeln, die Ihre Marke und Ihre Produkte für bestehende Kunden bewerben. Sie können den Inhalt mit Variablen und Markup-Tags personalisieren.

>[!NOTE]
>
>Die Versionen 2.4.0 bis 2.4.3 von Adobe Commerce und Magento Open Source enthielten die von dotdigital anbietern entwickelte Erweiterung, die zur Integration in die dotdigital Engagement Cloud verwendet wurde. Ab Version 2.4.4 ist diese Erweiterung nicht mehr im Paket mit der Kernversion enthalten und muss über die Commerce Marketplace installiert und aktualisiert werden. Der Marketplace bietet außerdem Zugriff auf die aktuelle Dokumentation, die vom Erweiterungsentwickler bereitgestellt wird.
><br><br>
>Wenn Sie die gebündelte Erweiterung aktiviert und konfiguriert haben, müssen Sie Ihre Composer.json-Datei im Rahmen des Aktualisierungsprozesses von 2.4.4 aktualisieren und zukünftige Erweiterungs-Updates verwalten. Weitere Informationen finden Sie unter [Aktualisierungsmodule](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) im _Aktualisierungshandbuch_.

- [Newsletter](newsletters.md) - Erstellen Sie Newsletter, verwalten Sie Ihre Abonnentenliste, entwickeln Sie Inhalte und leiten Sie Traffic zu Ihrem Store.

- [RSS-Dienste](social-rss.md#rss-feeds) - Verwenden Sie RSS-Dienste, um Ihre Produktinformationen auf Einkaufs-Aggregations-Sites zu veröffentlichen und sie sogar in Ihre Newsletter aufzunehmen. Kunden können sich für Ihre RSS-Dienste anmelden, um mehr über neue Produkte und Promotions zu erfahren.

- [Soziale Netzwerke](social-rss.md#social-networks) - Integrieren Sie Ihren Store in Ihre sozialen Netzwerke, indem Sie eine Marketplace-Erweiterung installieren oder Ihren Inhaltsseiten ein Plugin hinzufügen.

## Google-Marketing-Tools

Ihre Store-Konfiguration ist mit den folgenden Google-Tools integriert, mit denen Sie Ihre Inhalte optimieren, Ihren Traffic analysieren und Ihren Katalog mit Einkaufsaggregatoren und Marketplace verbinden können.

>[!NOTE]
>
>Ab Version 2.4.5 wird die Google-Dienstintegration aktualisiert, um die Verwendung der GTag-APIs zu unterstützen. GTag ist ein einheitlicher Mechanismus für die Integration mit Google-Funktionen für Webseiten und unterstützt die neuesten Funktionen und Möglichkeiten zum Tracking und Verwalten von Inhalten über Google Services. Weitere Informationen finden Sie in der [Google Analytics-Entwicklerdokumentation](https://developers.google.com/analytics/devguides/collection/gtagjs).

- [Google Analytics](google-analytics.md) - Verwenden Sie Google Universal Analytics, um zusätzliche benutzerdefinierte Dimensionen und Metriken für das Tracking zu definieren, mit Unterstützung für Offline- und mobile App-Interaktionen und Zugriff auf laufende Updates.

- [Google Content Experiments](google-content-experiments.md) - Richten Sie einen A/B-Test für Produkte, Kategorien oder Inhaltsseiten ein, die Google Analytics Content verwenden.

- [Google Tag Manager](google-tag-manager.md) - ![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Verwenden Sie den Google Tag Manager, um die vielen Tags zu verwalten, die mit Marketingkampagnenereignissen verbunden sind.

- [Google AdWords](google-adwords.md) - Erstellen Sie eine Google AdWords-Kampagne und verfolgen Sie Konversionen für Ihren Store.
