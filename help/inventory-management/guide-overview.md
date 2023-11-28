---
title: '"Inventory management-Anleitung [!DNL Inventory Management] Guide'''
description: Umfassende Informationen zu [!DNL Inventory Management] für Adobe Commerce- und Magento Open Source-Administratoren, einschließlich Migration und Konfiguration.
seo-title: Adobe Commerce Inventory Management Guide
seo-description: Describes how to use the [!DNL Inventory Management] module in Adobe Commerce or Magento Open Source.
exl-id: 8013bc13-b057-4ad7-bbed-ee00c2f6e4eb
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 1%

---

# [!DNL Inventory Management] Guide - Übersicht

Dieses Handbuch richtet sich an Administratoren von Adobe Commerce und Magento Open Source. Es enthält detaillierte Informationen zur Aktivierung dieses Moduls, einschließlich Konfiguration und Verwaltung seiner Funktionen. Es wird von einem grundlegenden Verständnis des Kerns ausgegangen. [!DNL Commerce] Konfiguration und Funktionalität.

[!DNL Inventory Management] verfügt über zwei Bereiche für Administratoren:

- Admin: Verwenden Sie diesen Bereich, um auf die Konfigurationsoberfläche und die Berichterstellung zuzugreifen.
- Befehlszeilenschnittstelle: Verwenden Sie dieses Tool, um Installations- und Backend-Konfigurationsaufgaben auszuführen.

Dieses Handbuch behandelt:

| Betreff | Beschreibung |
| ------- | ----------- |
| [Einführung](introduction.md) | Übersicht über die [!DNL Inventory Management] Funktionen, mit denen Sie Lagerbestände an mehreren Standorten verwalten können, sodass Ihr Commerce-Store den physischen Bestand genau widerspiegelt. |
| [Versionshinweise](release-notes.md) | In den Versionshinweisen finden Sie Informationen zu allen [!DNL Inventory Management] veröffentlicht. |
| Grundlagen zum Bestand | Lernen Sie die Grundlagen zum Verwalten des Bestands kennen: [Bestände und Quellen](sources-stocks.md), [Quellauswahl und -reservierung](selection-reservations.md), [Status der Bestellung und Reservierung](order-status.md), und [Produkttypen](product-types.md) |
| Erste Schritte | Informationen zum [!DNL Inventory Management] -Modul und wie es in Ihre Commerce-Instanz und Ihre Store-Vorgänge passt: [Commerce-Upgrades](migrate.md), [Modulinstallation und -aktualisierung](install-update.md), [Beschaffungstypen für Händler](merchant-sourcing.md), und [Änderungen der Beschaffungsstruktur](expand-restructure.md) |
| [Konfiguration](configuration.md) | Informationen zur Konfiguration von [!DNL Inventory Management] Optionen, die die Verfügbarkeit der Quelle, Storefront-Produkte und den Versand von Bestellungen bestimmen. |
| [Quellen verwalten](sources-manage.md) | Erfahren Sie mehr über Quellen und wie sie die physischen Orte definieren, an denen Produktbestand verwaltet und zur Erfüllung von Bestellungen versandt wird oder wo Dienste verfügbar sind. |
| [Verwalten von Lagern](stocks-manage.md) | Erfahren Sie, wie mit &quot;stock&quot;ein virtueller, aggregierter Produktbestand für die Quellen Ihrer Verkaufskanäle dargestellt wird. |
| [Mengen verwalten](quantities-manage.md) | Erfahren Sie, wie Sie Quellen und Mengen für neue Produkte zuweisen oder vorhandene Produkte ändern. |
| [Verwalten von Bestellungen und Sendungen](shipments.md) | Weitere Informationen [!DNL Inventory Management] Funktionen und Optionen zur Verwaltung der Lagerbestandsmengen durch den Versand. |
| [CLI-Referenz](cli.md) | Erfahren Sie mehr über die Befehle, die von der [!DNL Inventory Management] -Modul zur Verwaltung von Bestandsdaten und Konfigurationseinstellungen. |

{style="table-layout:auto"}

## Entwicklerinformationen

Siehe [[!DNL Inventory Management]](https://developer.adobe.com/commerce/webapi/rest/inventory/) in der Entwicklerdokumentation für weitere Informationen zur Modularchitektur, zu APIs und zur Algorithmusanpassung.

## Commerce-Dokumentation

{{docs-links}}

## Fehlerbehebung und Support

Verwenden Sie die folgenden Ressourcen, wenn Sie Informationen benötigen oder Fragen haben, die nicht in diesem Handbuch behandelt werden:

- [Unstimmigkeiten bei zahlreichen Reservierungen](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-8/mdva-30112-magento-patch-large-number-reservation-inconsistencies.html)
- [Probleme bei der Inventarinkonsistenz](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-14/mdva-33281-magento-patch-inventory-inconsistency-issues.html)
- [Muster, die nicht im Durchlaufinventar erfasst werden, erreichen &quot;0&quot;](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-17/mdva-34850-swatches-not-strike-through-inventory-reaches-0.html)
- [Der Lagerstatus ist nach der Lagerbestandsinstallation fehlerhaft](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/stock-status-incorrect-after-magento-inventory-install.html)
- [Support-Tickets](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#submit-ticket)—Senden Sie ein Ticket, um zusätzliche Hilfe zu erhalten.
