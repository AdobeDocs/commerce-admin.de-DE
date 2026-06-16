---
title: Private Verkäufe und Veranstaltungen
description: Erfahren Sie, wie Sie mit privaten Verkäufen und anderen Katalogereignissen den Umsatz für Ihren bestehenden Kundenstamm steigern und neue Leads generieren können.
exl-id: 0b890463-b1e5-4327-8d8a-372afd53312a
feature: Reporting, Promotions/Events
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/de/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
TQID: https://experienceleague.adobe.com/8MvnlOp5muOQbx3b7dSKguc4wf-k47v9AtaHXu7b9pU
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
subfeature_v2:
  - id: bd0aa680-a881-4f35-9dcf-843b0574bc5f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 458
ht-degree: 0%

---

# Private Verkäufe und Veranstaltungen

{{ee-feature}}

Private Verkäufe und andere Katalogereignisse sind eine hervorragende Möglichkeit, Ihren bestehenden Kundenstamm zu nutzen, um Buzz und neue Leads zu generieren oder überschüssige Lagerbestände abzuladen. Sie können einen zeitlich begrenzten Verkauf erstellen, den Verkauf auf bestimmte Mitglieder beschränken oder eine eigenständige private Verkaufsseite erstellen. Sie können auch Einladungen und Ereignisdetails definieren. Steigern Sie die Markentreue und erzeugen Sie ein Gespräch, indem Sie Ihren besten Kunden die Behandlung mit VIP bieten. Bieten Sie exklusiven Zugriff nur auf den Verkauf durch Mitglieder oder auf den privaten Verkauf, um die Markentreue zu steigern. Sie können diese Verkäufe auch verwenden, um überschüssige Waren zu liquidieren. Kundengruppen sind nur bei der Einrichtung dieser Mitgliedertypen und bei VIP Sales hilfreich.

![Beispiel einer Storefront - Ereignis auf der Startseite](./assets/storefront-event-home-page.png){width="700" zoomable="yes"}

## Komponenten des Ereignis-Managements

- **Kategorien** - Jedes Ereignis ist mit einer [Kategorie](../catalog/category-create.md) aus Ihrem Katalog verknüpft.

- **Ereignisse** - Verkauf von Veranstaltungen basiert auf einem Start- und Enddatum. Sie können einen [Countdown-Ticker](#event-ticker) verwenden, um die verbleibende Zeit anzuzeigen.

- **Karussell für Katalogereignisse** - Wenn das [Widget Katalogereignis](../content-design/widget-event-carousel.md) in der Konfiguration aktiviert ist, kann es als Liste offener und bevorstehender Ereignisse auf Store-Seiten platziert werden, sortiert nach Enddatum. Wenn zwei oder mehr Ereignisse dasselbe Enddatum haben, werden die Ereignisse nach der in der Konfiguration angegebenen Reihenfolge sortiert.

- **[!UICONTROL Websites]** - Kategorieberechtigungen basieren hauptsächlich auf [Kundengruppen](../customers/customer-groups.md).

- **Kategorieberechtigungen** - [Kategorieberechtigungen](../catalog/category-permissions.md) gibt Ihnen volle Kontrolle über die spezifischen Aktivitäten, die in einer bestimmten Kategorie stattfinden können.

- **Zugriffsbeschränkungen** - Verhindert den öffentlichen [Zugriff](event-configure.md#restrict-access) auf die Website durch Umleitung auf eine Landingpage, Anmeldeseite oder Registrierungsseite.

- **Einladungen** - E-Mail-Nachrichten werden mit einem Link gesendet, um ein Konto im Store zu erstellen. Sie können die Möglichkeit, ein Konto zu erstellen, auf diejenigen beschränken, die eine [Einladung](invitations.md) erhalten.

- **Private Verkaufsberichte** - Die [Private Verkaufsberichte](../getting-started/private-sales-reports.md) enthalten Informationen über gesendete Einladungen, eingeladene Kunden und Konversionen.

## Event-Ticker

Der Ticker-Block zeigt einen Countdown-Ticker für offene Ereignisse mit dem Start- und Enddatum für anstehende Ereignisse an. Wenn ein Ereignis geschlossen wurde, zeigt der Ticker das Anfangs- und das Enddatum an.

![Beispiel-Storefront - Ereigniskarussell](./assets/storefront-event-ticker-carousel.png){width="700" zoomable="yes"}

Wenn die Kategorieseitenauswahl für ein Ereignis aktiviert ist, wird der Tickerblock oben in der Kategorieliste angezeigt. Wenn der Produktseitenticker aktiviert ist, wird der Tickerblock auch oben auf der Produktseite jedes Produkts angezeigt, das mit der Kategorie verknüpft ist.

Der Ereignisticker kann beim Erstellen von [&#x200B; aktiviert &#x200B;](event-create.md).

![Beispiel einer Storefront - Ereignis-Seitenleiste](./assets/storefront-event-sidebar.png){width="700" zoomable="yes"}
