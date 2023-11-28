---
title: '[!DNL Commerce] upgrades'
description: Erfahren Sie, wie sich Upgrades für Adobe Commerce und Magento Open Source auf Katalog und [!DNL Inventory Management] -Konfigurationen.
exl-id: ba640b91-0f29-46df-bfd9-1c43433a751f
feature: Inventory, Upgrade
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '721'
ht-degree: 0%

---

# [!DNL Commerce] Upgrades

Wenn Sie in einer früheren Version das Inventar aus einer Hand verwendet haben, enthält diese Information Details zu neuen Funktionen und Änderungen an Ihren vorhandenen Katalog- und Lagerkonfigurationen.

[!DNL Inventory Management] für Adobe Commerce und Magento Open Source umfasst Funktionen, Verbesserungen und Entwicklerunterstützung, die die Produktverwaltung verbessern und aktualisieren und neue Funktionen hinzufügen. Alle Funktionen sind standardmäßig verfügbar, einschließlich des Quellauswahlalgorithmus und des gleichzeitigen Auscheckens, um die Bestellmengen an die Quellen abzugleichen und die Bestellerfüllung zu gewährleisten. Abhängig von Ihren Websites, Geschäften und Händlentypen können Sie zusätzliche Lager und Quellen erstellen, Lagerbestände zuweisen und vieles mehr. Vollständige Informationen finden Sie unter [Inventory management](introduction.md).

Wenn Sie Magento Open Source 2.4.x oder Adobe Commerce 2.4.x installieren, treten die folgenden ersten Änderungen auf:

- [Inventory management](enable.md) aktiviert auf globaler Store- oder Produktebene. Die Option Lager verwalten ermöglicht bzw. deaktiviert die Verfolgung von Lagerbestandsmengen, Berechnungen aggregierter Verkaufsmengen und die Reservierungsverwaltung für die Verfolgung von Käufen bis hin zu Rechnungen und Sendungen. Sie können diese Option deaktivieren, um eine ERP und andere Dienste von Drittanbietern für die Verwaltung von Lagern, Bestellungen und Sendungen zu verwenden. Weitere Informationen finden Sie unter [!DNL Inventory Management] Module unten.

- A [Standardquelle](sources-manage.md) und [Standardbestand](stocks-manage.md) zum System hinzufügen. Deaktivieren oder entfernen Sie diese Standardwerte nicht. [!DNL Commerce] weist vorhandenen und neu importierten Produkten diese Standardeinstellungen zu.

  >[!IMPORTANT]
  >
  >Von der Verwendung des Standardspeichers und der Standardquelle wird dringend abgeraten, da sie zum `CatalogInventory` -Modul, das jetzt nicht mehr unterstützt wird. Es wird empfohlen, stattdessen benutzerdefinierte Lager und Quellen zu erstellen und zu verwenden.

   - Die Lagerbestände bieten eine aggregierte, virtuelle Verkaufsmenge mit Reservierungen, um Warenkörbe und Bestellungen zu verfolgen und so einen gleichzeitigen Checkout zu gewährleisten.

   - Alle vorhandenen Produkte in Ihrem Katalog werden der Standardquelle zugewiesen. Bis Sie neue Quellen hinzufügen, ändert sich die Produktoberfläche nicht. Wenn Sie nur Produkte von einem Ort aus versenden, gibt es keine anderen Unterschiede für Quellen. Sie können benutzerdefinierte [sources](sources-add.md) und [Zuteilung von Mengen](quantities-manage.md) je Versandort.

   - Sie können eine Quelle als Pickup-Speicherort konfigurieren und [Zuteilung von Mengen](quantities-manage.md) für diese Quelle.

   - Ihre Website wird dem Standardbestand zugewiesen. Sie können benutzerdefinierte [Bestände](stocks-add.md) um Vertriebskanäle (Websites) und Quellen (Standorte) miteinander zu verbinden.

- Zusätzliche [Konfigurationsoptionen](configuration.md) zu Ihren Produkten und dem globalen Store hinzufügen. Einige vorhandene Konfigurationsoptionen erhalten aktualisierte Optionen und Verhaltensweisen:

   - Benachrichtigungs-E-Mail für die Menge Unten sendet Benachrichtigungen und Abzüge von der Verkaufsmenge.

   - Der Schwellenwert für nicht vorrätige Bestände unterstützt positive, Null und negative Beträge. Bei aktivierten Rückstellungen werden positive Beträge ignoriert, als null (oder unbegrenzt) betrachtet.

   - Rückorder unterstützen Null (unendlich) und negative Beträge. Wenn diese Option aktiviert ist, wird die &quot;Für Menge benachrichtigen&quot;nicht von der &quot;Verkaufte Menge&quot;abgezogen.

- Neue Reservierungen verfolgen potenzielle Umsätze und setzen auf Mengenabzüge, wenn die Bestellung ausläuft. Sie können nie direkt auf Buchungen zugreifen oder diese erstellen. [!DNL Commerce] erstellt und verwaltet Buchungen hinter den Kulissen durch Bestellungen, Sendungen und Kreditkarten.

- [Bestellungen und Sendungen](shipments.md) enthalten neue Funktionen, um Sendungen mit dem Quellauswahlalgorithmus zu empfehlen und partielle Sendungen aus mehreren Quellen zu unterstützen, um eine Bestellung zu erfüllen.

- Neu [Import-/Exportfunktionen](inventory-import-export.md) ermöglichen es Ihnen, für alle SKUs in Ihrem Katalog massenhafte Quellen hinzuzufügen, Lagerbestandsmengen zu aktualisieren und den Lagerstatus (vorrätig/nicht vorrätig) festzulegen. Mit diesen Funktionen können Sie für eine, ausgewählte oder alle Quellen ändern.

- Neue Massenoptionen über die Produktraster-Seite unterstützen Bulk-Unterstützung [Zuweisen und Aufheben der Zuweisung von Quellen](bulk-assignment.md), und [Bestandsübertragung an Quelle](inventory-transfer.md).

- [!DNL Inventory Management] unterstützt B2B-Katalog. Derzeit müssen alle B2B-Produkte der Standardquelle und dem Standardbestand zugewiesen werden.

## [!DNL Commerce Order Management] und [!DNL Inventory Management]

[Commerce Order Management (MCOM)][1] ist nicht kompatibel mit der [!DNL Inventory Management]. Wenn MCOM-Module installiert sind, bieten sie alle Lagerbestandsverwaltungsfunktionen für [!DNL Commerce], einschließlich Verwaltung aus einer Hand und aus mehreren Quellen, Lagerbestände, Reservierungen und mehr. Die [!DNL Inventory Management] -Module sind standardmäßig deaktiviert.

MCOM bietet umfangreiche Funktionen und Dienstleistungen für ein fortschrittliches Omnichannel-Auftragsmanagement, globale Inventarisierung und Multi-Sourcing, die Erfüllung von Lagern und zentralisierten Kundenservice. Eine vollständige Liste der Funktionen finden Sie im Abschnitt [MCOM-Funktionsliste][2].

[!DNL Inventory Management] vorhandene [!DNL Commerce] Funktionen mit zusätzlichen Optionen zur Verfolgung von laufenden Bestellungen, manuellem Inventar, verfügbarem Inventar für einen Bestand und APIs zur Erweiterungsentwicklung.

## [!DNL Inventory Management] Module

Eventuell sollten Sie die [!DNL Inventory Management] Module für:

- Beschleunigen Sie die Aktualisierung von Händlern, die derzeit auf Adobe Commerce oder Magento Open Source 2.0/2.1/2.2/2.3 ausgeführt werden, und die Migration auf 2.4.x.

- Verwenden Sie benutzerdefinierte oder Drittanbieter-Inventar- und -Bestellverwaltungsmodule.

- Verwendung [!DNL Order Management System] für die Bestandsverwaltung. Der aktuelle Connector unterstützt nicht [!DNL Inventory Management] -Schnittstellen. Für OMS-Händler, die auf Adobe Commerce 2.4.0 aktualisieren, müssen sie diese Module deaktivieren.

Ausführliche Informationen finden Sie unter [Installieren und Aktualisieren](install-update.md).

[1]: https://omsdocs.magento.com/
[2]: https://omsdocs.magento.com/en/getting-started/feature-list/
