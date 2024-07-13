---
title: '[!DNL Commerce] upgrades'
description: Erfahren Sie, wie sich Aktualisierungen von Adobe Commerce und Magento Open Source auf Katalog- und [!DNL Inventory Management] Konfigurationen auswirken.
exl-id: ba640b91-0f29-46df-bfd9-1c43433a751f
feature: Inventory, Upgrade
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '720'
ht-degree: 0%

---

# [!DNL Commerce] Upgrades

Wenn Sie in einer früheren Version das Inventar aus einer Hand verwendet haben, enthält diese Information Details zu neuen Funktionen und Änderungen an Ihren vorhandenen Katalog- und Lagerkonfigurationen.

[!DNL Inventory Management] für Adobe Commerce und Magento Open Source umfasst Funktionen, Verbesserungen und Entwicklerunterstützung, die die Produktverwaltung verbessern und aktualisieren und neue Funktionen hinzufügen. Alle Funktionen sind standardmäßig verfügbar, einschließlich Source Selection Algorithm und Concurrent Checkout, um die Bestellmengen an die Quellen abzugleichen und die Bestellerfüllung zu gewährleisten. Abhängig von Ihren Websites, Geschäften und Händlentypen können Sie zusätzliche Lager und Quellen erstellen, Lagerbestände zuweisen und vieles mehr. Vollständige Informationen finden Sie unter [Inventory management](introduction.md).

Wenn Sie Magento Open Source 2.4.x oder Adobe Commerce 2.4.x installieren, treten die folgenden ersten Änderungen auf:

- [Inventory management](enable.md) aktiviert auf globaler Store- oder Produktebene. Die Option Lager verwalten ermöglicht bzw. deaktiviert die Verfolgung von Lagerbestandsmengen, Berechnungen aggregierter Verkaufsmengen und die Reservierungsverwaltung für die Verfolgung von Käufen bis hin zu Rechnungen und Sendungen. Sie können diese Option deaktivieren, um eine ERP und andere Dienste von Drittanbietern für die Verwaltung von Lagern, Bestellungen und Sendungen zu verwenden. Weitere Informationen finden Sie unten unter [!DNL Inventory Management] Module.

- Ein [standardmäßiger Source](sources-manage.md) und ein [Standardbestand](stocks-manage.md) werden dem System hinzugefügt. Deaktivieren oder entfernen Sie diese Standardwerte nicht. [!DNL Commerce] weist vorhandenen und neu importierten Produkten diese Standardwerte zu.

  >[!IMPORTANT]
  >
  >Von der Verwendung des Standardspeichers und des Standard-Source wird dringend abgeraten, da sie Teil des `CatalogInventory`-Moduls sind, das jetzt nicht mehr unterstützt wird. Es wird empfohlen, stattdessen benutzerdefinierte Lager und Quellen zu erstellen und zu verwenden.

   - Die Lagerbestände bieten eine aggregierte, virtuelle Verkaufsmenge mit Reservierungen, um Warenkörbe und Bestellungen zu verfolgen und so einen gleichzeitigen Checkout zu gewährleisten.

   - Alle in Ihrem Katalog vorhandenen Produkte werden der standardmäßigen Source zugewiesen. Bis Sie neue Quellen hinzufügen, ändert sich die Produktoberfläche nicht. Wenn Sie nur Produkte von einem Ort aus versenden, gibt es keine anderen Unterschiede für Quellen. Sie können benutzerdefinierte [Quellen](sources-add.md) und [Mengen](quantities-manage.md) pro Versandort zuweisen.

   - Sie können eine Quelle als Abholort konfigurieren und [Mengen zuweisen](quantities-manage.md) für diese Quelle zuweisen.

   - Ihre Website wird dem Standardbestand zugewiesen. Sie können benutzerspezifische [Lager](stocks-add.md) erstellen, um Verkaufskanäle (Websites) und Quellen (Standorte) miteinander zu verbinden.

- Zusätzliche [Konfigurationsoptionen](configuration.md) fügen Sie Ihren Produkten und dem globalen Store hinzu. Einige vorhandene Konfigurationsoptionen erhalten aktualisierte Optionen und Verhaltensweisen:

   - Benachrichtigungs-E-Mail für die Menge Unten sendet Benachrichtigungen und Abzüge von der Verkaufsmenge.

   - Der Schwellenwert für nicht vorrätige Bestände unterstützt positive, Null und negative Beträge. Bei aktivierten Rückstellungen werden positive Beträge ignoriert, als null (oder unbegrenzt) betrachtet.

   - Rückorder unterstützen Null (unendlich) und negative Beträge. Wenn diese Option aktiviert ist, wird die &quot;Für Menge benachrichtigen&quot;nicht von der &quot;Verkaufte Menge&quot;abgezogen.

- Neue Reservierungen verfolgen potenzielle Umsätze und setzen auf Mengenabzüge, wenn die Bestellung ausläuft. Sie können nie direkt auf Buchungen zugreifen oder diese erstellen. [!DNL Commerce] erstellt und verwaltet Buchungen hinter den Kulissen durch Bestellungen, Sendungen und Kreditkarten.

- [Bestellungen und Sendungen](shipments.md) enthalten neue Funktionen, mit denen Sendungen mit dem Source Selection Algorithm empfohlen werden und Teillieferungen aus verschiedenen Quellen unterstützt werden, um eine Bestellung zu erfüllen.

- Neue [Import-/Exportfunktionen](inventory-import-export.md) ermöglichen es Ihnen, für alle SKUs in Ihrem Katalog massenhafte Quellen hinzuzufügen, Lagerbestandsmengen zu aktualisieren und den Lagerstatus (in/aus Lager) festzulegen. Mit diesen Funktionen können Sie für eine, ausgewählte oder alle Quellen ändern.

- Neue Massenoptionen über die Produktraster-Seite unterstützen Batches zum Zuweisen und Aufheben der Zuweisung von Quellen](bulk-assignment.md) und zum Übertragen von Beständen an die Quelle ](inventory-transfer.md).[[

- [!DNL Inventory Management] unterstützt B2B-Katalog. Derzeit müssen alle B2B-Produkte dem Standard-Source und dem Standardbestand zugewiesen werden.

## [!DNL Commerce Order Management] und [!DNL Inventory Management]

[Commerce Order Management (MCOM)][1] ist nicht mit dem [!DNL Inventory Management] kompatibel. Wenn MCOM-Module installiert sind, bieten sie alle Lagerbestandsverwaltungsfunktionen für [!DNL Commerce], einschließlich der Verwaltung von Einzel- und Mehrfachquellen, Lagern, Reservierungen und mehr. Die [!DNL Inventory Management] -Module sind standardmäßig deaktiviert.

MCOM bietet umfangreiche Funktionen und Dienstleistungen für ein fortschrittliches Omnichannel-Auftragsmanagement, globale Inventarisierung und Multi-Sourcing, die Erfüllung von Lagern und zentralisierten Kundenservice. Eine vollständige Liste der Funktionen finden Sie in der [Liste der MCOM-Funktionen][2].

[!DNL Inventory Management] erweitert vorhandene [!DNL Commerce] -Funktionen um zusätzliche Optionen zur Verfolgung von laufenden Bestellungen, manuellem Inventar, verfügbarem Inventar für einen Bestand und APIs zur Erweiterungsentwicklung.

## [!DNL Inventory Management] Module

Sie können [!DNL Inventory Management] -Module deaktivieren, um:

- Beschleunigen Sie die Aktualisierung von Händlern, die derzeit auf Adobe Commerce oder Magento Open Source 2.0/2.1/2.2/2.3 ausgeführt werden, und die Migration auf 2.4.x.

- Verwenden Sie benutzerdefinierte oder Drittanbieter-Inventar- und -Bestellverwaltungsmodule.

- Verwenden Sie [!DNL Order Management System] für die Lagerbestandsverwaltung. Der aktuelle Connector unterstützt keine [!DNL Inventory Management] -Schnittstellen. Für OMS-Händler, die auf Adobe Commerce 2.4.0 aktualisieren, müssen sie diese Module deaktivieren.

Vollständige Informationen finden Sie unter [Installieren und Aktualisieren](install-update.md).

[1]: https://omsdocs.magento.com/
[2]: https://omsdocs.magento.com/en/getting-started/feature-list/
