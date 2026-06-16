---
title: Einführung in [!DNL Adobe Commerce B2B]
description: Erfahren Sie, wie Sie integrierte B2B-Funktionen nutzen können, um Ihre Anforderungen an Unternehmenskunden zu erfüllen.
exl-id: fc7e8147-5fd5-4e4b-b16e-0b0d54c415da
feature: B2B
TQID: https://experienceleague.adobe.com/dt7QZnXH9yO6vMFJBIgt4g43XVfk6Da1gyXEMqqvJlo
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 829
ht-degree: 2%

---

# Einführung in [!DNL Adobe Commerce B2B]

Im Gegensatz zum Standard-Business-to-Consumer-Modell sind integrierte B2B-Funktionen (Business-to-Business) so konzipiert, dass sie den Anforderungen von Verkäufern (Adobe Commerce-Händler) entsprechen, die Kunden haben, die Unternehmen sind. Es unterstützt Unternehmen mit komplexen Organisationsstrukturen und mehreren Benutzern mit verschiedenen Rollen und Kaufberechtigungsebenen. Ein typischer B2B-Kunde kann der Manager eines Einzelhandelsgeschäfts oder ein Käufer sein, der im Namen eines Unternehmens Einkäufe tätigt. In beiden Fällen findet die Transaktion zwischen Ihrem Unternehmen und deren Kunden statt. Sie können auch Produkte direkt an den Verbraucher verkaufen. [!DNL Adobe Commerce B2B] ist eine integrierte Lösung, die sowohl B2B- als auch B2C-Modelle unterstützt.

Mit der [Installation](install.md) und [Aktivierung](enable-basic-features.md) der B2B-Erweiterung in Ihrem Adobe Commerce-Store kann das Kauferlebnis mit kundenspezifischen Katalogen und Preisen sowie zielgerichteten Inhalten und Werbeaktionen personalisiert werden.

## Unternehmenskonten

Die Komponente Firmenkonto ist eine wichtige Entität innerhalb von B2B, von der alle anderen Funktionen in gewisser Weise abhängig sind. Dadurch können mehrere Käufer, die zu einem einzigen Unternehmen gehören, zu einem einzigen Unternehmenskonto (oder Unternehmenskonto) zusammengefasst werden. Der Unternehmensadministrator kann eine Unternehmensstruktur (Abteilungen, Unterteilungen und Benutzer) erstellen, die dem Betriebsmodell für das Unternehmen entspricht und unterschiedliche Benutzerrollen und Berechtigungen für Unternehmensmitglieder bereitstellt. Diese Struktur ermöglicht es dem Unternehmensadministrator, die Benutzeraktivität für das Unternehmenskonto zu steuern: Bestellung, Angebote, Einkauf, Zugriff auf Firmenkreditinformationen oder -profile usw.

Der Commerce-Site-Administrator kann vom Administrator aus konfigurieren, wie das Unternehmen auf der Website arbeitet. Die Konfiguration bestimmt die B2B-Funktionen, die für Unternehmensbenutzer verfügbar sind, einschließlich Zahlungsmethoden, Preisniveaus, der Möglichkeit, Preise mithilfe von Angeboten auszuhandeln, der Möglichkeit, Anforderungslisten zu erstellen, und mehr.

Weitere Informationen finden Sie unter [Unternehmenskonten](account-companies.md).

>[!NOTE]
>
>Wenn diese Option aktiviert ist, kann Ihr Store Unternehmen die Option _Auf Konto bezahlen_ geben, was bedeutet, dass Käufe in einer Firmenkreditlinie getätigt werden. Als Händler können Sie Gutschriften für ein Firmenkonto zuordnen und Krediteinstellungen für ein Unternehmen sowie die Kreditrückerstattung verwalten.

## Unternehmensleitung

Das Unternehmensmanagement unterstützt Händleradministratoren dabei, die Verwaltung und das Management von B2B-Organisationen mit komplexen Betriebsmodellen zu optimieren.

Vom Administrator aus können Benutzende mit entsprechenden Berechtigungen eine **[!UICONTROL Company Hierarchy]** erstellen, die die Organisationsstruktur eines aus mehreren Unternehmen bestehenden Unternehmens widerspiegelt. Diese Hierarchie ermöglicht es ihnen, Unternehmen als Gruppe anzuzeigen und zu verwalten. Beispielsweise kann der Administrator eine Muttergesellschaft bestimmen und alle Unternehmen zuweisen, die als Tochtergesellschaften der Muttergesellschaft tätig sind. Der Administrator der übergeordneten Firma kann dann Unternehmenskonten für alle zugewiesenen Firmen anzeigen und verwalten.

Weitere Informationen finden Sie unter [Unternehmensverwaltung](manage-companies.md).

## Dienste für Adobe Commerce

Services für Adobe Commerce sind gehostete Services, die erweiterte Funktionen für Adobe Commerce und Magento Open Source bereitstellen. Folgende Services unterstützen B2B-Workflows:

* [Katalog-Service](https://experienceleague.adobe.com/docs/commerce/catalog-service/guide-overview.html?lang=de)
* [Live Search](https://experienceleague.adobe.com/docs/commerce/live-search/guide-overview.html?lang=de)
* [Produkt Recommendations](https://experienceleague.adobe.com/docs/commerce/product-recommendations/guide-overview.html?lang=de)

## Freigegebene Kataloge

Gemeinsam genutzte Kataloge sind die Preisniveaus, mit denen benutzerdefinierte Preise pro Produkt für verschiedene Unternehmen auf einer oder mehreren Websites festgelegt werden können. Mithilfe freigegebener Kataloge können Sie Produkte verkaufen, indem Sie unterschiedliche Preisstufen für verschiedene Kundengruppen anwenden. Die Unterstützung für freigegebene Kataloge ist nur für Commerce-Stores verfügbar, die für die Unterstützung von Unternehmenskonten konfiguriert sind.

Weitere Informationen finden Sie unter [Arbeiten mit freigegebenen Katalogen](catalog-shared.md).

## Schnellauftrag

Konfigurieren Sie die Schnellbestellung, um den Bestellvorgang auf mehrere Klicks für angemeldete Kunden zu reduzieren, wenn diese den Produktnamen oder die SKU der Produkte kennen, die sie bestellen möchten.

Weitere Informationen finden Sie unter [Schnellbestellungen](quick-order.md).

## Verhandelbare Kursofferten

Verwenden Sie die Funktion „Angebote“, um Preisverhandlungen zwischen einem Unternehmenskäufer und einem Käufer zu initiieren.

* Ein autorisierter Käufer kann ein Angebot aus dem Warenkorb initiieren.

* Ein Verkäufer kann ein Angebot für einen Käufer vom Administrator initiieren.

Käufer und Verkäufer verwalten den Verhandlungsprozess mit dem Angebot, z. B. das Hinzufügen von Artikeln, das Aktualisieren von Mengen, das Anfordern und Anwenden von Rabatten, bis sie eine Vereinbarung treffen. Das _Quotes_ im Admin listet jedes erhaltene Angebot auf und bewahrt einen Verlauf der Kommunikation zwischen Käufer und Verkäufer auf.

Der Support für verhandelbare Angebote ist nur für Commerce-Stores verfügbar, die für die Unterstützung von Unternehmenskonten konfiguriert sind.

Weitere Informationen finden Sie unter [Verhandlungsfähige Anführungszeichen](quotes.md).

## Bestellgenehmigungen

Wenn Bestellungen für ein Firmenkonto aktiviert werden, werden alle Bestellungen automatisch als Bestellungen erstellt. Firmenbenutzer mit den erforderlichen Berechtigungen können von ihnen erstellte Bestellungen und von untergeordneten Benutzern erstellte Bestellungen erstellen, bearbeiten und löschen. Je nach Rolle und Reihenfolge können für Firmenbenutzer mehrere Genehmigungsregeln gelten.

Weitere Informationen finden Sie unter [Bestellungen für Unternehmen](purchase-order-flow.md).

## Anforderungslisten

Kunden können beim Kauf häufig bestellter Produkte mithilfe der Anforderungsliste Zeit sparen, da sie Artikel direkt aus der Liste in den Warenkorb legen können. Sie können mehrere Listen verwalten, die sich auf Produkte von verschiedenen Anbietern, Käufern, Teams, Kampagnen oder auf alles andere konzentrieren, was ihren Workflow optimiert.

Weitere Informationen finden Sie unter [Anforderungslisten](requisition-lists.md).
