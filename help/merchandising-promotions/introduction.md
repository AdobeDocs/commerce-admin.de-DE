---
title: Einführung in Commerce-Merchandising und -Promotions
description: Erfahren Sie mehr über Commerce-Tools für die Erstellung gezielter Promotions und Möglichkeiten zur Kundeninteraktion.
exl-id: 8e55ac42-aeef-4f97-b1e8-9b2db354e5e6
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '1094'
ht-degree: 0%

---

# Einführung in Commerce-Merchandising und -Promotions

Targeting von Promotions, Schaffung von Möglichkeiten für Kundeninteraktionen und Umwandlung von Käufern in Käufer. Verwalten Sie Kundenbeziehungen, indem Sie Aktivitäten nach dem Kauf unterstützen und rückkehrenden Kunden spezielle Rabatte anbieten. Lernen Sie Best Practices und Techniken kennen, um Ihre SEO-Initiativen zu unterstützen.

## Merchandising

_Merchandising_ ist ein Begriff, der im Einzelhandel verwendet wird, um die Kunst und Wissenschaft der Entwicklung von Bodenplänen und der Präsentation von Produkten zu beschreiben. Vielleicht fällt Ihnen die [kategoriebasierte Navigation](../catalog/navigation-top.md) als Grundriss des Stores und der dynamischen Präsentation von Produkten als Bedingungen, die Sie auf die Auflistung von Produkten im Geschäft anwenden können. Sie können auch Programme implementieren, die mehr Produktverkäufe fördern:

- [Visual Merchandiser](visual-merchandiser.md) - Eine Reihe erweiterter Tools, mit denen Sie Produkte positionieren und Bedingungen anwenden können, die bestimmen, welche Produkte in der Kategorienliste angezeigt werden.

- [Geschenkregister](gift-registries.md) - Ermöglichen Sie Ihren Kunden die Erstellung von Geschenkregistern für besondere Anlässe und laden Sie ihre Freunde und ihre Familie ein, ihre Geschenke aus dem Geschenkregister zu kaufen.

- [Prämien und Treue](rewards-loyalty.md) - Verwenden Sie ein Punktesystem, um eindeutige Programme zu implementieren, die die Kundeninteraktion fördern und die Kundenloyalität fördern. Sie können Punkte für eine breite Palette von Transaktions- und Kundenaktivitäten zuweisen und die Punktzahl, Balance und Gültigkeit steuern.

- [Private Verkäufe und Veranstaltungen](events-private-sales.md) - Nutzen Sie Ihren bestehenden Kundenstamm, um Buzz und neue Leads zu generieren oder überschüssigen Bestand durch private Verkäufe und andere Katalogereignisse zu entlasten.

>[!TIP]
>
>Weitere Informationen zu Product Recommendations und wie diese Ihnen Einblicke und Kontrolle verschaffen können, die Sie benötigen, um das beste Erlebnis für Ihre Käufer zu erstellen, finden Sie unter [Benutzerhandbuch zu Recommendations](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/guide-overview.html).

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
>Wenn Sie eine Bedingung basierend auf einem bestimmten Produktattribut definieren möchten, **[!UICONTROL Use for Promo Rule Conditions]** muss auf `Yes` für das -Attribut in Ihrer [Store-Eigenschaften](../catalog/attribute-product-create.md).


### Preisregeln

Für [Katalogpreisregeln](price-rules-catalog.md), erstellen Sie Bedingungen basierend auf [Attributsätze](../catalog/attribute-sets.md) in Ihrem Katalog, Vergleichsfunktionen und ausgewählten Attributen. Man erschafft die Bedingungen wie Sätze, indem man ein paar Aussagen auswählt. Sie können beispielsweise zwei Preisregeln erstellen, um Rabatte für Kinderbekleidung und Herrenbekleidung/Damenbekleidung auf der Grundlage der Kategorie anzuwenden.

![Abbildung - Beispiel für Katalogpreisregeln](./assets/diagram-catalog-price-rules.png){width="500"}

[Preisregel für Warenkorb](price-rules-cart.md) -Bedingungen können auf jeder Kategorie basieren, die dem Store untergeordnet ist [root](../catalog/category-root.md). Preisregeln werden im Voraus festgelegt und werden immer dann wirksam, wenn die erforderlichen Bedingungen erfüllt sind. Diese Regeln verwenden Attribute, einschließlich Produktattribut-Kombinationen, z. B. Übereinstimmung mit einer SKU im Warenkorb mithilfe von Produktattributen. Diese Regeln können auch Bedingungen für die Produktauswahl, Bedingungskombinationen für komplizierte Regeln und Warenkorbattribute wie Zwischensummen verwenden.

![Abbildung - Beispiel für Preisregeln für Warenkorb](./assets/diagram-cart-price-rules.png){width="500"}

## Kommunikation und SEO

Mastering [Suchmaschinenoptimierung (SEO)](seo-overview.md) ist von entscheidender Bedeutung, um potenzielle Käufer zu gewinnen. Erfahren Sie mehr über die Suchmaschinenoptimierung und Feinabstimmung des Inhalts und der Präsentation Ihrer Site, um die Art und Weise zu verbessern, wie die Seiten von Suchmaschinen indiziert werden.

Eine der Aufgaben, die vor dem Start Ihres Stores ausgeführt werden müssen, besteht darin, die E-Mail-Vorlagen zu überprüfen, die für alle von Ihrem Store gesendeten Nachrichten verwendet werden, um sicherzustellen, dass sie Ihre Marke widerspiegeln. Sie sollten dies jedoch noch weiter tun, indem Sie andere Kommunikationen entwickeln, die Ihre Marke und Ihre Produkte für bestehende Kunden bewerben. Sie können den Inhalt mit Variablen und Markup-Tags personalisieren.

>[!NOTE]
>
>Die Versionen 2.4.0 bis 2.4.3 von Adobe Commerce und Magento Open Source enthielten die von dotdigital anbietern entwickelte Erweiterung, die zur Integration in die dotdigital Engagement Cloud verwendet wurde. Ab Version 2.4.4 ist diese Erweiterung nicht mehr im Paket mit der Kernversion enthalten und muss über die Commerce Marketplace installiert und aktualisiert werden. Der Marketplace bietet außerdem Zugriff auf die aktuelle Dokumentation, die vom Erweiterungsentwickler bereitgestellt wird.
><br><br>
>Wenn Sie die gebündelte Erweiterung aktiviert und konfiguriert haben, müssen Sie Ihre Composer.json-Datei im Rahmen des Aktualisierungsprozesses von 2.4.4 aktualisieren und zukünftige Erweiterungs-Updates verwalten. Siehe [Upgrade-Module](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) im _Upgrade-Handbuch_ für weitere Informationen.

- [Newsletter](newsletters.md) - Erstellen Sie Newsletter, verwalten Sie Ihre Abonnentenliste, entwickeln Sie Inhalte und fördern Sie den Traffic zu Ihrem Geschäft.

- [RSS-Dienste](social-rss.md#rss-feeds) - Verwenden Sie RSS-Dienste, um Ihre Produktinformationen auf Shopping-Aggregations-Sites zu veröffentlichen und sie sogar in Ihre Newsletter aufzunehmen. Kunden können sich für Ihre RSS-Dienste anmelden, um mehr über neue Produkte und Promotions zu erfahren.

- [Soziale Netzwerke](social-rss.md#social-networks) - Integrieren Sie Ihren Store in Ihre sozialen Netzwerke, indem Sie eine Marketplace-Erweiterung installieren oder ein Plugin zu Ihren Inhaltsseiten hinzufügen.

## Google-Marketing-Tools

Ihre Store-Konfiguration ist mit den folgenden Google-Tools integriert, mit denen Sie Ihre Inhalte optimieren, Ihren Traffic analysieren und Ihren Katalog mit Einkaufsaggregatoren und Marketplace verbinden können.

>[!NOTE]
>
>Ab Version 2.4.5 wird die Google-Dienstintegration aktualisiert, um die Verwendung der GTag-APIs zu unterstützen. GTag ist ein einheitlicher Mechanismus für die Integration mit Google-Funktionen für Webseiten und unterstützt die neuesten Funktionen und Möglichkeiten zum Tracking und Verwalten von Inhalten über Google Services. Weitere Informationen finden Sie unter [Entwicklerdokumentation für Google Analytics](https://developers.google.com/analytics/devguides/collection/gtagjs).

- [Google Analytics](google-analytics.md) - Verwenden Sie Google Universal Analytics, um zusätzliche benutzerdefinierte Dimensionen und Metriken für das Tracking zu definieren, mit Unterstützung für Offline- und mobile App-Interaktionen und Zugriff auf laufende Aktualisierungen.

- [Google Content Experiments](google-content-experiments.md) - Richten Sie einen A/B-Test für Produkte, Kategorien oder Inhaltsseiten ein, die Google Analytics Content verwenden.

- [Google Tag Manager](google-tag-manager.md) - ![Adobe Commerce](../assets/adobe-logo.svg) (Nur Adobe Commerce) Mit dem Google Tag Manager können Sie die vielen Tags verwalten, die mit Marketingkampagnenereignissen verbunden sind.

- [Google AdWords](google-adwords.md) - Erstellen Sie eine Google AdWords-Kampagne und verfolgen Sie Konversionen für Ihren Store.
