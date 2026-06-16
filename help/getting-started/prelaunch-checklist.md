---
title: Checkliste für den Vorabstart
description: Verwenden Sie diese Liste, um die erforderlichen Konfigurationseinstellungen zu überprüfen, um sicherzustellen, dass alles korrekt ist, bevor Ihr Store in die Produktion geht.
exl-id: 649809c2-7217-4274-b365-c682bfff24ba
feature: Site Management, System
role: Admin, Leader
TQID: https://experienceleague.adobe.com/cthgB115wuL6ewlKBtfOXwfqevj2jpbdARQHB9pvIcc
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 416
ht-degree: 0%

---

# Checkliste für den Vorabstart

Überprüfen Sie nach Abschluss des Designs, der Entwicklung und der Tests Ihres Stores die folgenden Konfigurationseinstellungen, um sicherzustellen, dass alles korrekt ist, bevor der Store _live)_. Eine umfassende Beschreibung jeder Konfigurationseinstellung finden Sie unter [_Konfigurationsreferenz_](../configuration-reference/guide-overview.md).

## Allgemeine Einstellungen

- [Store-URLs](../stores-purchase/store-urls.md): Überprüfen Sie, ob die Store-URLs für die Storefront und den Admin Console für eine Live-Produktionsumgebung korrekt sind.
- Sicherheitszertifikat : Vor dem Starten Ihres Stores installieren Sie ein zu 100 % signiertes und vertrauenswürdiges Sicherheitszertifikat für die in der Basis-URL angegebene Domain.
- [E-Mail-Adressen speichern](../getting-started/store-details.md#store-email-addresses) - Vervollständigen Sie alle E-Mail-Adressen, die zum Senden und Empfangen von E-Mail-Benachrichtigungen verwendet werden, z. B. neue Bestellungen, Rechnungen, Sendungen, Gutschriften, Produktpreisbenachrichtigungen und Newsletter. Stellen Sie sicher, dass jedes Feld eine gültige Geschäfts-E-Mail-Adresse enthält.

## Marketing-Einstellungen

- [E-Mail-Vorlagen](../systems/email-templates.md) - Aktualisieren Sie die standardmäßigen E-Mail-Vorlagen, um Ihre Marke widerzuspiegeln. Stellen Sie sicher, dass Sie die Konfiguration aktualisieren, wenn Sie Vorlagen erstellen.
- [Verkaufskommunikation](../stores-purchase/introduction.md#order-management-and-operations) - Stellen Sie sicher, dass Ihre Rechnungen und Lieferscheine die richtigen Geschäftsinformationen enthalten und Ihre Marke widerspiegeln.
- [Google-Tools](../merchandising-promotions/google-tools.md) - [!DNL Commerce] bietet eine Integration mit der Google-API, damit Ihr Unternehmen Google Analytics und Google AdWords verwenden kann.

## Verkaufseinstellungen

- [Warenkorboptionen](../stores-purchase/cart-configuration.md) - Sehen Sie sich die Einstellungen für die Warenkorbkonfiguration an, um festzustellen, ob Sie etwas ändern möchten, z. B. die Festlegung des Mindestbestellbetrags und der Lebensdauer der Preise im Warenkorb.
- [Checkout-Optionen](../stores-purchase/checkout-process.md#checkout-options) - Sehen Sie sich die Checkout-Optionen an, um festzustellen, ob Sie etwas ändern möchten, z. B. das Einrichten von Geschäftsbedingungen und das Konfigurieren des Gast-Checkouts.
- [Steuern](../stores-purchase/taxes.md) - Stellen Sie sicher, dass die Steuern entsprechend Ihren Unternehmenssteuerregeln und lokalen Anforderungen konfiguriert sind.
- [Versandmethoden](../stores-purchase/delivery.md) - Ermöglicht die Verwendung aller Spediteure und Versandmethoden durch das Unternehmen.
- [PayPal](../stores-purchase/paypal.md) - Wenn Sie Ihren Kunden die Möglichkeit bieten möchten, mit PayPal zu bezahlen, eröffnen Sie ein PayPal-Händlerkonto und richten Sie eine Zahlungsmethode ein. Führen Sie einige Testtransaktionen im Sandbox-Modus aus, bevor der Store live geschaltet wird.
- [Zahlungsmethoden](../stores-purchase/payments.md) - Aktivieren Sie die Zahlungsmethoden, die Sie verwenden möchten, und stellen Sie sicher, dass sie ordnungsgemäß konfiguriert sind. Überprüfen Sie den Bestellstatus, die akzeptierte Währung, die zulässigen Länder usw.

## Systemeinstellungen

[Cron (Geplante Aufgaben)](../systems/cron.md) Cron-Aufträge werden zur Verarbeitung von E-Mails, Katalogpreisregeln, Newslettern, Kundenbenachrichtigungen, Google-Sitemaps, Aktualisierung von Währungskursen usw. verwendet. Stellen Sie sicher, dass Cron-Aufträge so eingestellt sind, dass sie im entsprechenden Zeitintervall in Minuten ausgeführt werden.
