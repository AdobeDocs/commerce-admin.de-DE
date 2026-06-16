---
title: Einführung in Commerce Merchandising und Promotions
description: Informieren Sie sich über Commerce-Tools zur Erstellung zielgerichteter Werbeaktionen und Angebote für Kundinnen und Kunden.
exl-id: 8e55ac42-aeef-4f97-b1e8-9b2db354e5e6
TQID: https://experienceleague.adobe.com/2ZEsUmKW8TQM53KFXWxyQGb9h4yFXHsjnFu8q25PCT8
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 1049
ht-degree: 1%

---

# Einführung in Commerce Merchandising und Promotions

Targeting von Werbeaktionen und Schaffung von Möglichkeiten für Kundeninteraktion und Umwandlung von Käufern in Käufer. Verwalten Sie Kundenbeziehungen, indem Sie Aktivitäten nach dem Kauf unterstützen und wiederkehrenden Kunden spezielle Rabatte anbieten. Best Practices und Techniken zur Unterstützung Ihrer SEO-Initiativen

## Verkauf von Waren

_Merchandising_ ist ein Begriff, der im Einzelhandel verwendet wird, um die Kunst und Wissenschaft der Grundrissentwicklung und der Präsentation von Produkten zu beschreiben. Sie können sich die [kategoriebasierte Navigation](../catalog/navigation-top.md) als Grundriss des Stores vorstellen und die dynamische Präsentation von Produkten als die Bedingungen, die Sie auf die Auflistung von Produkten im Store anwenden können. Außerdem können Sie Programme implementieren, die den Absatz von Produkten steigern:

- [!BADGE Nur PaaS]{type=Informative url="https://experienceleague.adobe.com/de/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."} [Visual Merchandiser](visual-merchandiser.md) - Eine Reihe erweiterter Tools, mit denen Sie Produkte positionieren und Bedingungen anwenden können, die bestimmen, welche Produkte in der Kategorieliste angezeigt werden.

- [Geschenkregistrierungen](gift-registries.md) - Geben Sie Ihren Kunden die Möglichkeit, Geschenkregistrierungen für besondere Anlässe zu erstellen und ihre Freunde und Familie einzuladen, ihre Geschenke aus der Geschenkregistrierung zu kaufen.

- [Prämien und Treue](rewards-loyalty.md) - Verwenden Sie ein Punktesystem, um einzigartige Programme zu implementieren, die die Kundenbindung fördern und die Kundenloyalität steigern. Sie können Punkte für eine Vielzahl von Transaktions- und Kundenaktivitäten vergeben und die Punktezuteilung, den Saldo und den Ablauf steuern.

- [Privater Verkauf und Veranstaltungen](events-private-sales.md) - Nutzen Sie Ihren bestehenden Kundenstamm, um Begeisterung und neue Leads zu generieren oder überschüssigen Bestand durch private Verkäufe und andere Katalogereignisse abzuladen.

>[!TIP]
>
>Informationen zu Produktempfehlungen und dazu, wie sie Ihnen die insight und die Kontrolle geben können, die Sie benötigen, um das beste Erlebnis für Ihre Käufer zu schaffen, finden Sie im [Benutzerhandbuch zu Produktempfehlungen](https://experienceleague.adobe.com/docs/commerce/product-recommendations/guide-overview.html?lang=de).

## Promotions

Verwenden Sie in Adobe Commerce die Aktionsfunktionen, um Produktbeziehungen einzurichten, und verwenden Sie Preisregeln, um Rabatte auf der Grundlage verschiedener Bedingungen Trigger. Sie können Preisregeln verwenden, um Kundenanreize anzubieten, z. B.:

- Senden Sie Ihren besten Kunden einen Gutschein für einen Rabatt auf ein bestimmtes Produkt
- Kostenloser Versand für Einkäufe über einen bestimmten Betrag anbieten
- Planen einer Promotion für einen bestimmten Zeitraum

Eine Regel ist eine Sammlung von Bedingungen (eine oder mehrere), die Preisänderungen auf Produkte anwenden, wenn eine oder alle Bedingungen erfüllt sind. Jede Regel kann mehrere Bedingungen aufweisen, die angewendet werden, wenn alle oder alle (eine oder mehrere, aber nicht alle) Anweisungen wahr oder falsch sind.

### Bedingungen

Bedingungen sind Anweisungen, die die Liste der Produkte und die Situationen für die Anwendung der Regel verfeinern. Die Attribute und Optionen für Bedingungen unterscheiden sich zwischen den Typen der verfügbaren Regeln. Wenn erfüllt, wird die Aktion abgeschlossen, z. B. Rabatte, Buy-One-Get-One (BOGO) und andere Optionen. Die Regeln können so einfach oder so kompliziert sein, wie sie benötigt werden, um Ihren Geschäftsanforderungen, saisonalen Rabatten und Werbeaktionen und ganzjährigen Möglichkeiten gerecht zu werden. Zum Beispiel können Sie einige zusätzliche Optionen für die Feiertage hinzufügen und dabei das ganze Jahr über kostenlosen Versand anbieten, wenn Warenkörbe eine hohe Zwischensumme haben.

>[!NOTE]
>
>Wenn Sie eine Bedingung basierend auf einem bestimmten Produktattribut definieren möchten, muss **[!UICONTROL Use for Promo Rule Conditions]** für das Attribut in Ihren „Storefront[Eigenschaften“ auf `Yes` festgelegt &#x200B;](../catalog/attribute-product-create.md).


### Preisregeln

Für [Katalogpreisregeln](price-rules-catalog.md) erstellen Sie Bedingungen basierend auf [Attributsätzen](../catalog/attribute-sets.md) in Ihrem Katalog, Vergleichsfunktionen und ausgewählten Attributen. Die Bedingungen wie Sätze erschafft man, indem man einige Aussagen wählt. Sie können beispielsweise zwei Preisregeln erstellen, um Rabatte für Kinderbekleidung und Herren-/Damenbekleidung je nach Kategorie anzuwenden.

![Diagramm - Beispiel für Katalogpreisregeln](./assets/diagram-catalog-price-rules.png){width="500"}

[Warenkorbpreisregel](price-rules-cart.md) Bedingungen können auf jeder Kategorie basieren, die ein untergeordnetes Element des Stores ([) &#x200B;](../catalog/category-root.md). Preisregeln werden im Voraus festgelegt und treten in Kraft, wenn die erforderlichen Bedingungen erfüllt sind. Diese Regeln verwenden Attribute, einschließlich Produktattributkombinationen wie den Abgleich einer SKU im Warenkorb mithilfe von Produktattributen. Diese Regeln können auch Produktauswahl-Mengenbedingungen, Bedingungskombinationen für komplizierte Regeln und Warenkorbattribute wie Zwischensumme verwenden.

![Diagramm - Beispiel für Warenkorb-Preisregeln](./assets/diagram-cart-price-rules.png){width="500"}

## Kommunikation und SEO

Das [&#x200B; von Suchmaschinenoptimierung (SEO)](seo-overview.md) ist entscheidend, um potenzielle Käufer einzubinden. Erfahren Sie mehr über die Suchmaschinenoptimierung und die Feinabstimmung des Inhalts und der Präsentation Ihrer Site, um die Art und Weise zu verbessern, wie die Seiten von Suchmaschinen indiziert werden.

Eine der Aufgaben, die Sie vor dem Start Ihres Stores ausführen müssen, besteht darin, die E-Mail-Vorlagen zu überprüfen, die für alle von Ihrem Store gesendeten Nachrichten verwendet werden, um sicherzustellen, dass sie Ihre Marke widerspiegeln. Aber Sie sollten diesen Schritt weiter gehen, indem Sie andere Kommunikationen entwickeln, die Ihre Marke und Ihre Produkte bei bestehenden Kunden bewerben. Sie können den Inhalt mit Variablen und Markup-Tags personalisieren.

>[!NOTE]
>
>Die Versionen 2.4.0 bis 2.4.3 von Adobe Commerce und Magento Open Source enthielten die vom dotdigital-Anbieter entwickelte Erweiterung, die zur Integration mit der dotdigital Engagement Cloud verwendet wurde. Ab Version 2.4.4 ist diese Erweiterung nicht mehr im Bundle der Hauptversion enthalten und muss von der Commerce Marketplace installiert und aktualisiert werden. Der Marketplace bietet außerdem Zugriff auf die aktuelle Dokumentation, die vom Erweiterungsentwickler bereitgestellt wird.
><br><br>>Wenn Sie die gebündelte Erweiterung aktiviert und konfiguriert haben, müssen Sie Ihre Datei „composer.json“ im Rahmen des Upgrades auf 2.4.4 aktualisieren und zukünftige Erweiterungsaktualisierungen verwalten. Siehe [Upgrade-Module](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html?lang=de) im _Upgrade-Handbuch_ für weitere Informationen.

- [Newsletter](newsletters.md) - Erstellen Sie Newsletter, verwalten Sie Ihre Abonnentenliste, entwickeln Sie Inhalte und leiten Sie den Traffic zu Ihrem Store weiter.

- [RSS-Feeds](social-rss.md#rss-feeds) - Verwenden Sie RSS-Feeds, um Ihre Produktinformationen auf Shopping-Aggregations-Sites zu veröffentlichen und sie sogar in Ihre Newsletter aufzunehmen. Kunden können Ihre RSS-Feeds abonnieren, um mehr über neue Produkte und Werbeaktionen zu erfahren.

- [Soziale Netzwerke](social-rss.md#social-networks) - Integrieren Sie Ihren Store in Ihre sozialen Netzwerke, indem Sie eine Marketplace-Erweiterung installieren oder ein Plug-in zu Ihren Inhaltsseiten hinzufügen.

## Google Marketing-Tools

Ihre Store-Konfiguration ist mit den folgenden Google-Tools integriert, um Ihre Inhalte zu optimieren, Ihren Traffic zu analysieren und Ihren Katalog mit Shopping-Aggregatoren und Marktplätzen zu verbinden.

>[!NOTE]
>
>Ab Version 2.4.5 wird die Google Services-Integration aktualisiert, um die Verwendung der GTag-APIs zu unterstützen. GTag ist ein einheitlicher Integrationsmechanismus mit Google-Funktionen für Web-Seiten und unterstützt die neuesten Funktionen und Möglichkeiten für das Tracking und die Verwaltung von Inhalten mit Google Services. Weitere Informationen finden Sie in der Entwicklerdokumentation zu [Google Analytics](https://developers.google.com/analytics/devguides/collection/gtagjs).

- [Google Analytics](google-analytics.md) - Verwenden Sie Google Universal Analytics, um zusätzliche benutzerdefinierte Dimensionen und Metriken für das Tracking zu definieren, mit Unterstützung für Offline- und Mobile-App-Interaktionen und Zugriff auf laufende Aktualisierungen.

- [Google Tag Manager](google-tag-manager.md) - ![Adobe Commerce](../assets/adobe-logo.svg) (nur Adobe Commerce) Verwenden Sie den Google Tag Manager, um die vielen Tags zu verwalten, die sich auf Marketing-Kampagnenereignisse beziehen.

- [Google AdWords](google-adwords.md) - Erstellen Sie eine Google AdWords-Kampagne und verfolgen Sie Konversionen für Ihren Store.
