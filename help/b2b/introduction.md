---
title: Einführung in [!DNL B2B for Adobe Commerce]
description: Erfahren Sie, wie Sie integrierte B2B-Funktionen nutzen können, um Ihre Anforderungen an Unternehmenskunden zu erfüllen.
exl-id: fc7e8147-5fd5-4e4b-b16e-0b0d54c415da
feature: B2B
source-git-commit: fb075822e318073053cdf8cdd5cd9bb3a6343904
workflow-type: tm+mt
source-wordcount: '841'
ht-degree: 0%

---

# Einführung in [!DNL B2B for Adobe Commerce]

Im Gegensatz zum Standardmodell von Business zu Consumer sind integrierte B2B-Funktionen (Business to Business) so konzipiert, dass sie den Anforderungen von Verkäufern (Adobe Commerce-Händlern) gerecht werden, deren Kunden Unternehmen sind. Es unterstützt Unternehmen mit komplexen Organisationsstrukturen und mehreren Benutzern mit verschiedenen Rollen und unterschiedlichen Einkaufsberechtigungen. Ein typischer B2B-Kunde könnte der Geschäftsführer eines Einzelhandelsgeschäfts oder ein Käufer sein, der im Namen eines Unternehmens Einkäufe tätigt. In beiden Fällen erfolgt die Transaktion zwischen Ihrem Unternehmen und dem Unternehmen. Sie können Produkte auch direkt an den Verbraucher verkaufen. [!DNL B2B for Adobe Commerce] ist eine integrierte Lösung, die sowohl B2B- als auch B2C-Modelle unterstützt.

Mit dem [Installation](install.md) und [Aktivierung](enable-basic-features.md) der B2B-Erweiterung in Ihrem Adobe Commerce-Store, kann das Kauferlebnis mit kundenspezifischen Katalogen und Preisen sowie zielgerichteten Inhalten und Promotions personalisiert werden.

## Unternehmenskonten

Die Unternehmenskomponente ist eine Schlüsselentität innerhalb von B2B, von der alle anderen Funktionen in irgendeiner Weise abhängig sind. Sie ermöglicht die Verbindung mehrerer Käufer, die innerhalb eines Unternehmens ansässig sind, zu einem einzigen Unternehmenskonto (oder Unternehmenskonto). Der Unternehmensadministrator kann eine Unternehmensstruktur (Abteilungen, Unterteilungen und Benutzer) erstellen, die das Betriebsmodell für das Unternehmen widerspiegelt und verschiedene Benutzerrollen und Berechtigungen für Unternehmensmitglieder bereitstellt. Diese Struktur ermöglicht es dem Unternehmensadministrator, die Benutzeraktivität für das Unternehmenskonto zu steuern: Bestellung, Angebote, Einkauf, Zugriff auf Unternehmenskreditinformationen oder -profile usw.

Der Administrator der Commerce-Site kann vom Administrator aus konfigurieren, wie das Unternehmen auf der Website funktioniert. Die Konfiguration bestimmt die B2B-Funktionen, die für Benutzer von Unternehmen verfügbar sind, einschließlich Zahlungsmethoden, Preisniveaus, Möglichkeit, Preise mithilfe von Anführungszeichen zu verhandeln, Möglichkeit, Anforderungslisten zu erstellen, und mehr.

Weitere Informationen finden Sie unter [Unternehmenskonten](account-companies.md).

>[!NOTE]
>
>Wenn dieser aktiviert ist, kann Ihr Store Unternehmen die Möglichkeit geben, _Kontobezahlung_, d. h. Einkäufe über eine Firmenkreditlinie tätigen. Als Händler können Sie einem Unternehmenskonto Guthaben zuweisen und die Krediteinstellungen für ein Unternehmen verwalten sowie die Kreditrückerstattung vornehmen.

## Unternehmensverwaltung

[!BADGE 1.5.0-Beta]{type=Informative url="/help/b2b/release-notes.md" tooltip="Nur für Beta-Programmteilnehmer verfügbar"}

Die Unternehmensverwaltung hilft Händlern, die Verwaltung und Verwaltung von B2B-Organisationen mit komplexen Betriebsmodellen zu optimieren.

Benutzer mit entsprechenden Berechtigungen können vom Administrator eine **[!UICONTROL Company Hierarchy]** , die die Organisationsstruktur eines aus mehreren Unternehmen bestehenden Unternehmens widerspiegelt. Diese Hierarchie ermöglicht es ihnen, Unternehmen als Gruppe anzuzeigen und zu verwalten. Beispielsweise kann der Administrator eine Muttergesellschaft bestimmen und alle Unternehmen zuweisen, die als Tochterunternehmen der Muttergesellschaft tätig sind. Anschließend kann der Administrator der Muttergesellschaft Unternehmenskonten für alle zugewiesenen Unternehmen anzeigen und verwalten.

Weitere Informationen finden Sie unter [Unternehmensverwaltung](manage-companies.md).

## Dienste für Adobe Commerce

Dienste für Adobe Commerce sind gehostete Dienste, die erweiterte Funktionen für Adobe Commerce und Magento Open Source bieten. Dienste, die B2B-Workflows unterstützen:

* [Catalog Service](https://experienceleague.adobe.com/docs/commerce-merchant-services/catalog-service/guide-overview.html)
* [Live Search](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/guide-overview.html)
* [Produkt-Recommendations](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/guide-overview.html)

## Freigegebene Kataloge

Gemeinsame Kataloge sind die Preisniveaus, die es ermöglichen, für verschiedene Unternehmen auf einer oder mehreren Websites benutzerdefinierte Preise pro Produkt festzulegen. Mithilfe freigegebener Kataloge können Sie Produkte verkaufen, indem Sie unterschiedliche Preisniveaus für verschiedene Kundengruppen anwenden. Unterstützung für freigegebene Kataloge ist nur für Commerce-Stores verfügbar, die zur Unterstützung von Unternehmenskonten konfiguriert sind.

Weitere Informationen finden Sie unter [Arbeiten mit freigegebenen Katalogen](catalog-shared.md).

## Schnellbestellung

Konfigurieren Sie die Schnellbestellung, um den Bestellprozess auf mehrere Klicks für angemeldete Kunden zu reduzieren, wenn sie den Produktnamen oder die SKU der Produkte kennen, die bestellt werden sollen.

Weitere Informationen finden Sie unter [Schnellbestellungen](quick-order.md).

## Negotiable Anführungszeichen

Verwenden Sie die Funktion Angebote , um Preisverhandlungen zwischen einem Firmenkäufer und -verkäufer einzuleiten.

* Ein autorisierter Käufer kann ein Angebot aus dem Warenkorb einreichen.

* Ein Verkäufer kann ein Angebot für einen Käufer von Admin einreichen.

Käufer und Verkäufer verwenden das Angebot, um den Verhandlungsprozess zu verwalten, z. B. das Hinzufügen von Artikeln, die Aktualisierung von Mengen, die Anforderung und die Anwendung von Rabatten, bis sie eine Einigung erzielen. Die _Anführungszeichen_ im Admin-Raster werden die einzelnen erhaltenen Angebote aufgelistet und die Kommunikation zwischen Käufer und Verkäufer protokolliert.

Die Unterstützung für verhandelbare Anführungszeichen ist nur für Commerce-Stores verfügbar, die zur Unterstützung von Unternehmenskonten konfiguriert sind.

Weitere Informationen finden Sie unter [Negotiable Anführungszeichen](quotes.md).

## Bestellgenehmigungen

Wenn die Bestellung für ein Unternehmenskonto aktiviert wird, werden alle Bestellungen automatisch als Bestellungen (Bestellformular) erstellt. Unternehmensbenutzer mit den erforderlichen Berechtigungen können von ihnen erstellte und von untergeordneten Benutzern erstellte POs und POs erstellen, bearbeiten und löschen. Je nach Rolle und Bestellung können Benutzer des Unternehmens mehreren Validierungsregeln unterliegen.

Weitere Informationen finden Sie unter [Bestellungen für Unternehmen](purchase-order-flow.md).

## Anforderungslisten

Kunden können die Anforderungsliste verwenden, um beim Kauf häufig bestellter Produkte Zeit zu sparen, da sie Artikel direkt aus der Liste zum Warenkorb hinzufügen können. Sie können mehrere Listen verwalten, die sich auf Produkte verschiedener Anbieter, Käufer, Teams, Kampagnen oder alles andere konzentrieren, das ihren Workflow optimiert.

Weitere Informationen finden Sie unter [Anforderungslisten](requisition-lists.md).
