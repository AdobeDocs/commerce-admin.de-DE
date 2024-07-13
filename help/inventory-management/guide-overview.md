---
title: "Inventory management Guide [!DNL Inventory Management] Guide"
description: Umfassende Informationen zu [!DNL Inventory Management] für Adobe Commerce- und Magento Open Source-Administratoren, einschließlich Migration und Konfiguration.
seo-title: Adobe Commerce Inventory Management Guide
seo-description: Describes how to use the [!DNL Inventory Management] module in Adobe Commerce or Magento Open Source.
exl-id: 8013bc13-b057-4ad7-bbed-ee00c2f6e4eb
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 0%

---

# [!DNL Inventory Management] Guide - Übersicht

Dieses Handbuch richtet sich an Administratoren von Adobe Commerce und Magento Open Source. Es enthält detaillierte Informationen zur Aktivierung dieses Moduls, einschließlich Konfiguration und Verwaltung seiner Funktionen. Es wird von einem grundlegenden Verständnis der Core-Konfiguration und -Funktionalität von [!DNL Commerce] ausgegangen.

[!DNL Inventory Management] hat zwei Bereiche für Administratoren:

- Admin: Verwenden Sie diesen Bereich, um auf die Konfigurationsoberfläche und die Berichterstellung zuzugreifen.
- Befehlszeilenschnittstelle: Verwenden Sie dieses Tool, um Installations- und Backend-Konfigurationsaufgaben auszuführen.

Dieses Handbuch behandelt:

| Betreff | Beschreibung |
| ------- | ----------- |
| [Einführung](introduction.md) | Überblick über die [!DNL Inventory Management]-Funktionen, mit denen Sie Lagerbestände an mehreren Standorten verwalten können, sodass Ihr Commerce-Store den physischen Bestand exakt widerspiegelt. |
| [Versionshinweise](release-notes.md) | Informationen zu allen [!DNL Inventory Management]-Versionen finden Sie in den Versionshinweisen . |
| Grundlagen zum Bestand | Lernen Sie die Grundlagen zum Verwalten des Bestands kennen: [Lager und Quellen](sources-stocks.md), [Quellauswahl und -reservierung](selection-reservations.md), [Bestell- und Reservierungsstatus](order-status.md) und [Produktarten](product-types.md) |
| Erste Schritte | Erfahren Sie mehr über das Modul [!DNL Inventory Management] und wie es in Ihre Commerce-Instanz und Speichervorgänge passt: [Commerce-Upgrades](migrate.md), [Modulinstallation und -aktualisierung](install-update.md), [Merchant-Sourcing-Typen](merchant-sourcing.md) und [Änderungen der Beschaffungsstruktur](expand-restructure.md) |
| [Konfiguration](configuration.md) | Erfahren Sie mehr über die Konfiguration von [!DNL Inventory Management] -Optionen, die die Verfügbarkeit der Quelle, Storefront-Produkte und den Versand von Bestellungen bestimmen. |
| [Quellen verwalten](sources-manage.md) | Erfahren Sie mehr über Quellen und wie sie die physischen Orte definieren, an denen Produktbestand verwaltet und zur Erfüllung von Bestellungen versandt wird oder wo Dienste verfügbar sind. |
| [Verwalten von Lagern](stocks-manage.md) | Erfahren Sie, wie mit &quot;stock&quot;ein virtueller, aggregierter Produktbestand für die Quellen Ihrer Verkaufskanäle dargestellt wird. |
| [Verwalten von Mengen](quantities-manage.md) | Erfahren Sie, wie Sie Quellen und Mengen für neue Produkte zuweisen oder vorhandene Produkte ändern. |
| [Bestellungen und Sendungen verwalten](shipments.md) | Erfahren Sie mehr über die zusätzlichen [!DNL Inventory Management] Funktionen und Optionen zum Verwalten von Lagerbestandsmengen während des Versandprozesses. |
| [CLI-Referenz](cli.md) | Erfahren Sie mehr über die Befehle des Moduls [!DNL Inventory Management] zum Verwalten von Bestandsdaten und Konfigurationseinstellungen. |

{style="table-layout:auto"}

## Entwicklerinformationen

Weitere Informationen zur Modularchitektur, zu APIs und zur Algorithmusanpassung finden Sie unter [[!DNL Inventory Management]](https://developer.adobe.com/commerce/webapi/rest/inventory/) in der Entwicklerdokumentation.

## Commerce-Dokumentation

{{docs-links}}

## Fehlerbehebung und Support

Verwenden Sie die folgenden Ressourcen, wenn Sie Informationen benötigen oder Fragen haben, die nicht in diesem Handbuch behandelt werden:

- [Unstimmigkeiten bei Zahlenreservierungen](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-8/mdva-30112-magento-patch-large-number-reservation-inconsistencies.html)
- [Inventarinkonsistenzprobleme](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-14/mdva-33281-magento-patch-inventory-inconsistency-issues.html)
- [Farbmuster, die nicht durchgestrichen werden, erreichen &quot;0&quot;](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-17/mdva-34850-swatches-not-strike-through-inventory-reaches-0.html)
- [Lagerstatus nach der Lagerbestandsinstallation fehlerhaft](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/stock-status-incorrect-after-magento-inventory-install.html)
- [Support-Tickets](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#submit-ticket): Senden Sie ein Ticket, um zusätzliche Hilfe zu erhalten.
