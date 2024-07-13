---
title: Vorabstartprüfliste
description: Verwenden Sie diese Liste, um die erforderlichen Konfigurationseinstellungen zu überprüfen und sicherzustellen, dass alles korrekt ist, bevor Ihr Store in die Produktion geht.
exl-id: 649809c2-7217-4274-b365-c682bfff24ba
feature: Site Management, System
role: Admin, Leader
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 0%

---

# Vorabstartprüfliste

Nachdem Sie das Design, die Entwicklung und den Test Ihres Stores abgeschlossen haben, überprüfen Sie die folgenden Konfigurationseinstellungen, um sicherzustellen, dass alles korrekt ist, bevor der Store _live geschaltet wird_. Eine umfassende Beschreibung jeder Konfigurationseinstellung finden Sie in der [_Konfigurationsreferenz_](../configuration-reference/guide-overview.md).

## Allgemeine Einstellungen

- [Store-URLs](../stores-purchase/store-urls.md) - Stellen Sie sicher, dass die Store-URLs für Storefront und Admin für eine Live-Produktionsumgebung korrekt sind.
- Sicherheitszertifikat - Installieren Sie vor dem Start Ihres Stores ein 100 % signiertes und vertrauenswürdiges Sicherheitszertifikat für die in der Basis-URL angegebene Domäne.
- [E-Mail-Adressen speichern](../getting-started/store-details.md#store-email-addresses) - Füllen Sie alle E-Mail-Adressen aus, die zum Senden und Empfangen von E-Mail-Benachrichtigungen verwendet werden, z. B. neue Bestellungen, Rechnungen, Sendungen, Kreditkarten, Produktpreiswarnungen und Newsletter. Stellen Sie sicher, dass jedes Feld eine gültige geschäftliche E-Mail-Adresse enthält.

## Marketing-Einstellungen

- [E-Mail-Vorlagen](../systems/email-templates.md) - Aktualisieren Sie die Standard-E-Mail-Vorlagen entsprechend Ihrer Marke. Aktualisieren Sie die Konfiguration bei der Erstellung von Vorlagen unbedingt.
- [Verkaufsmitteilungen](../stores-purchase/introduction.md#order-management-and-operations) - Stellen Sie sicher, dass Ihre Rechnungen und Packungsbeilagen die richtigen Geschäftsinformationen enthalten und Ihre Marke widerspiegeln.
- [Google Tools](../merchandising-promotions/google-tools.md) - [!DNL Commerce] bietet Integration in die Google-API, damit Ihr Unternehmen Google Analytics und Google AdWords verwenden kann.

## Verkaufseinstellungen

- [Warenkorboptionen](../stores-purchase/cart-configuration.md) - Sehen Sie sich die Konfigurationseinstellungen für den Warenkorb an, um festzustellen, ob Sie irgendetwas ändern möchten, z. B. die Festlegung des Mindestbestellbetrags und der Lebensdauer der Preise im Warenkorb.
- [Optionen zum Auschecken](../stores-purchase/checkout-process.md#checkout-options) - Sehen Sie sich die Optionen zum Auschecken an, um festzustellen, ob Sie etwas ändern möchten, z. B. das Einrichten von Geschäftsbedingungen und das Konfigurieren des Auscheckens.
- [Steuern](../stores-purchase/taxes.md) - Stellen Sie sicher, dass die Steuern entsprechend Ihren Unternehmenssteuerregeln und lokalen Anforderungen richtig konfiguriert sind.
- [Versandmethoden](../stores-purchase/delivery.md) - Ermöglichen Sie die Verwendung aller Anbieter und Versandmethoden durch das Unternehmen.
- [PayPal](../stores-purchase/paypal.md) - Wenn Sie Ihren Kunden die bequeme Zahlung mit PayPal anbieten möchten, öffnen Sie ein PayPal-Handelskonto und richten Sie eine Zahlungsmethode ein. Führen Sie einige Testtransaktionen im Sandbox-Modus aus, bevor der Store live geschaltet wird.
- [Zahlungsmethoden](../stores-purchase/payments.md) - Aktivieren Sie die Zahlungsmethoden, die Sie verwenden möchten, und stellen Sie sicher, dass sie richtig konfiguriert sind. Überprüfen Sie die Einstellungen für den Bestellstatus, die akzeptierte Währung, die zulässigen Länder usw.

## Systemeinstellungen

[Cron (Geplante Aufgaben)](../systems/cron.md) - Cron-Aufträge werden verwendet, um E-Mails, Katalogpreisregeln, Newsletter, Kundenwarnungen, Google-Sitemaps, Währungskurse usw. zu verarbeiten. Stellen Sie sicher, dass Cron-Aufträge so eingestellt sind, dass sie im entsprechenden Zeitintervall (in Minuten) ausgeführt werden.
