---
title: '[!DNL Commerce] Upgrades'
description: Erfahren Sie, wie sich Adobe Commerce- und Magento Open Source-Upgrades auf Kataloge und  [!DNL Inventory Management]  auswirken.
exl-id: ba640b91-0f29-46df-bfd9-1c43433a751f
feature: Inventory, Upgrade
source-git-commit: 392d8550741fe6fca3ea1301575c9ebb5e2483bd
workflow-type: tm+mt
source-wordcount: '720'
ht-degree: 0%

---

# [!DNL Commerce] Upgrades

Wenn Sie in einer früheren Version Single-Source-Inventar verwendet haben, finden Sie in diesen Informationen Details zu neuen Funktionen und Änderungen an Ihren vorhandenen Katalog- und Inventarkonfigurationen.

[!DNL Inventory Management] für Adobe Commerce und Magento Open Source umfasst Funktionen, Verbesserungen und Entwicklersupport, der die gesamte Produktbestandsverwaltung verbessert und aktualisiert und neue Funktionen hinzufügt. Alle Funktionen sind vorkonfiguriert verfügbar, einschließlich des Source-Auswahlalgorithmus und des gleichzeitigen Checkouts, um die Bestellmengen an die Bezugsquellen anzupassen und die Bestellabwicklung zu optimieren. Abhängig von Ihren Websites, Geschäften und dem Händlertyp können Sie zusätzliche Lager und Quellen erstellen, Lagerbestände zuweisen und vieles mehr. Vollständige Informationen finden Sie unter [Inventory management](introduction.md).

Bei der Installation von Magento Open Source 2.4.x oder Adobe Commerce 2.4.x treten folgende Änderungen auf:

- [Inventory management](enable.md) Aktiviert auf globaler Store- oder Produktebene. Die Option Lager verwalten ermöglicht oder deaktiviert die Verfolgung von Lagermengen, die Berechnung aggregierter Verkaufsmengen und die Reservierungsverwaltung für die Verfolgung von Käufen bis hin zur Rechnung und Lieferung. Sie können diese Option deaktivieren, um ein ERP und andere Drittanbieterdienste für die Verwaltung von Lagern, Bestellungen und Lieferungen zu verwenden. Weitere Informationen finden Sie unten unter [!DNL Inventory Management] Module .

- Ein [Standard-Source](sources-manage.md) und [Standard-Stock](stocks-manage.md) werden zum System hinzugefügt. Deaktivieren oder entfernen Sie diese Standardwerte nicht. [!DNL Commerce] weist diesen Standardwerten vorhandene und neu importierte Produkte zu.

  >[!IMPORTANT]
  >
  >Von der Verwendung des Standard-Stock und der Standard-Source wird dringend abgeraten, da sie Teil des `CatalogInventory` sind, das jetzt nicht mehr unterstützt wird. Es wird empfohlen, stattdessen benutzerdefinierte Stocks und Quellen zu erstellen und zu verwenden.

   - Stocks bietet eine aggregierte, virtuelle Verkaufsmenge mit Reservierungen, um Warenkörbe und Bestellungen zu verfolgen und so einen gleichzeitigen Checkout zu gewährleisten.

   - Alle vorhandenen Produkte in Ihrem Katalog werden der standardmäßigen Source zugewiesen. Bis zum Hinzufügen neuer Quellen ändert sich die Produktoberfläche nicht. Wenn Sie nur Produkte von einem Ort aus versenden, gibt es keine anderen Unterschiede für Quellen. Sie können benutzerdefinierte [Quellen](sources-add.md) erstellen und [Mengen zuweisen](quantities-manage.md) pro Lieferort.

   - Sie können eine Quelle als Abholort konfigurieren und [&#x200B; dieser Quelle &#x200B;](quantities-manage.md)Mengen zuweisen“.

   - Ihre Website weist dem Standardlager zu. Sie können benutzerdefinierte [Stocks“ erstellen](stocks-add.md) um Verkaufskanäle (Websites) und Quellen (Standorte) zu verbinden.

- Zusätzliche [Konfigurationsoptionen](configuration.md) zu Ihren Produkten und Ihrem globalen Store hinzufügen. Einige vorhandene Konfigurationsoptionen erhalten aktualisierte Optionen und Verhaltensweisen:

   - Für Menge unten benachrichtigen sendet Benachrichtigungen und zieht von der verkaufsfähigen Menge ab.

   - Der Schwellenwert für nicht vorrätige Artikel unterstützt positive Beträge, null und negative Beträge. Bei aktivierten Auftragsrückständen werden positive Beträge ignoriert und als Null (oder unendlich) betrachtet.

   - Nachbestellungen unterstützen Null (unendliche) und negative Beträge. Wenn diese Option aktiviert ist, wird die unten stehende Menge nicht von der verkaufsfähigen Menge abgezogen.

- Neue Reservierungen verfolgen potenzielle Verkäufe und konvertieren sie in Mengenabzüge, wenn der Auftrag ausgeliefert wird. Sie können nie direkt auf Reservierungen zugreifen oder diese erstellen. [!DNL Commerce] erstellt und verwaltet Reservierungen hinter den Kulissen durch Bestellungen, Lieferungen und Gutschriften.

- [Bestellungen und Sendungen](shipments.md) enthalten neue Funktionen, um Sendungen mithilfe des Source-Auswahlalgorithmus zu empfehlen und Teilsendungen aus verschiedenen Quellen zu unterstützen, um eine Bestellung zu erfüllen.

- Neue [Import-/Exportfunktionen](inventory-import-export.md) ermöglichen das Hinzufügen von Massenquellen, das Aktualisieren von Lagermengen und das Festlegen des Lagerstatus (auf/nicht vorrätig) für alle SKUs in Ihrem Katalog. Mit diesen Funktionen können Sie für eine, ausgewählte oder alle Quellen ändern.

- Neue Massenoptionen über die Produktraster-Seite unterstützen die Massenzuweisung [&#x200B; Quellen und das Aufheben der Zuweisung &#x200B;](bulk-assignment.md) und [Übertragen von Inventar zur Quelle](inventory-transfer.md).

- [!DNL Inventory Management] unterstützt B2B-Katalog. Derzeit müssen alle B2B-Produkte den standardmäßigen Source- und Standardaktien zugewiesen werden.

## [!DNL Commerce Order Management] und [!DNL Inventory Management]

[Commerce Order Management (MCOM)][1] ist nicht mit dem [!DNL Inventory Management] kompatibel. Nach der Installation bieten MCOM-Module alle Funktionen zur Bestandsverwaltung für [!DNL Commerce], einschließlich Single- und Multi-Source-Verwaltung, Lager, Reservierungen und mehr. Die [!DNL Inventory Management] sind standardmäßig deaktiviert.

MCOM bietet umfangreiche Funktionen und Services für erweiterte Omni-Channel-Auftragsverwaltung, globale Inventarisierung und Multi-Sourcing, Store-to-Warehouse-Erfüllung und zentralisierten Kundenservice. Eine vollständige Liste der Funktionen finden Sie in der [MCOM-Funktionsliste][2].

[!DNL Inventory Management] erweitert bestehende [!DNL Commerce] um zusätzliche Optionen zur Verfolgung von laufenden Aufträgen, verfügbarem Bestand, verfügbarem Bestand für ein Lager und APIs für die Erweiterungsentwicklung.

## [!DNL Inventory Management]

Sie können [!DNL Inventory Management] Module deaktivieren, um:

- Beschleunigen Sie die Aktualisierung von Händlern, die derzeit Adobe Commerce oder Magento Open Source 2.0/2.1/2.2/2.3 verwenden und zu 2.4.x migrieren.

- Verwenden Sie benutzerdefinierte oder Drittanbieter-Inventar- und Bestellverwaltungsmodule.

- Verwenden Sie [!DNL Order Management System] für die Bestandsverwaltung. Der aktuelle Connector unterstützt keine [!DNL Inventory Management]. OMS-Händler, die ein Upgrade auf Adobe Commerce 2.4.0 durchführen, müssen diese Module deaktivieren.

Ausführliche Informationen finden Sie unter [&#x200B; und Update](install-update.md).

[1]: https://commerce-docs.github.io/oms-documentation-archive/
[2]: https://commerce-docs.github.io/oms-documentation-archive/getting-started/feature-list/
