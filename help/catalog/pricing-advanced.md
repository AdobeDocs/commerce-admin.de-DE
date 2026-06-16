---
title: Erweiterte Preisgestaltung
description: Erfahren Sie mehr über die erweiterten Preiskontrollen in Adobe Commerce.
exl-id: 0f353341-1b6b-4093-bba9-4a1b88323f8a
feature: Catalog Management, Products
TQID: https://experienceleague.adobe.com/HyKkLwxHzBuyvh-YhjsMec9cMua9owWF--r-DShKnj8
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
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
source-wordcount: 886
ht-degree: 0%

---

# Erweiterte Preisgestaltung

Adobe Commerce und Magento Open Source unterstützen verschiedene Preisoptionen, die Sie für Werbeaktionen oder zur Erfüllung der Mindestpreisanforderungen des Herstellers verwenden können. Änderungen an den Produktpreisen können planmäßig oder durch eine Preisregel vorgenommen werden, die auf Produktebene oder im Warenkorb angewendet wird.

Verwalten Sie die Preise für Ihre Produkte mit erweiterten Preisen, um Kunden bessere Preise anzubieten, die die Verbraucher dazu ermutigen, mehr auszugeben, den Traffic auf Ihre Website zu lenken und alte Bestände zu löschen.

Die _[!UICONTROL Advanced Pricing]_&#x200B;definieren die erforderlichen Bedingungen für Sonderpreise, die für eine bestimmte Kundengruppe oder einen freigegebenen Katalog verfügbar sind. Erweiterte Preise können auf einfache, virtuelle, herunterladbare und gebündelte Produkte angewendet werden. Verwenden Sie eine Katalogpreisregel, um [&#x200B; anderen Produkttypen reduzierte Preise &#x200B;](../merchandising-promotions/price-rules-catalog.md). Weitere Informationen finden Sie unter [Preisbereich](catalog-price-scope.md).

Erweiterte Preisdaten werden mit Produktseiten synchronisiert. Wenn Sie beispielsweise eine Preismenge aktualisieren, aktualisiert das System den Wert auf der Produktseite.

![Adobe Commerce B2B](../assets/b2b.svg) (nur verfügbar mit [Adobe Commerce B2B](./b2b/../introduction.md)) Wenn Sie freigegebene Kataloge verwenden, werden die erweiterten Preisdaten sowohl mit Produktseiten als auch mit freigegebenen Katalogen synchronisiert. Wenn Sie beispielsweise die Preismenge einer Stufe aktualisieren, aktualisiert das System den Wert im freigegebenen Katalog und auf der Produktseite. Alle benutzerdefinierten Preise, die im freigegebenen Katalog angegeben sind, haben Vorrang vor den Preisen der Kundengruppe. Weitere Informationen finden Sie [Festlegen von Preisen und Strukturen für freigegebene Kataloge](https://experienceleague.adobe.com/docs/commerce-admin/b2b/shared-catalogs/define/catalog-shared-pricing-structure.html) im _Adobe Commerce B2B-Handbuch_.

![Advanced Pricing](./assets/product-pricing-advanced-link.png){width="600" zoomable="yes"}

## Zugriff auf erweiterte Preisoptionen

1. Öffnen Sie das Produkt im Bearbeitungsmodus.

1. Klicken Sie unter **[!UICONTROL Price]** auf **[!UICONTROL Advanced Pricing]**.

1. Befolgen Sie die Anweisungen für die Art der erforderlichen erweiterten Preisgestaltung.

   - [Gruppenpreis](product-price-group.md)

   - [Sonderpreis](product-price-special.md)

   - [Stückpreis](product-price-tier.md)

   - [Mindestpreis](product-price-minimum-advertised.md)

## Seitenverweis

### [!UICONTROL Special Price]

Geben Sie den Sonderpreis ein, um einen ermäßigten Preis für einen bestimmten Zeitraum oder eine geplante Kampagne anzubieten. Wenn ein Sonderpreis verfügbar ist, wird der Einzelhandelspreis durchgestrichen und der Sonderpreis erscheint unten in großer, fett gedruckter Schrift.

#### [!UICONTROL Special Price From]

{{ce-feature}}

| Feld | Beschreibung |
| ---- | ----------- |
| [!UICONTROL From] | Legt das erste Datum fest, ab dem der Sonderpreis verfügbar ist. Sie können das Datum entweder eingeben oder aus dem Kalender auswählen. |
| [!UICONTROL To] | Legt das letzte Datum fest, an dem der Sonderpreis verfügbar ist. Sie können das Datum entweder eingeben oder aus dem Kalender auswählen. |

{style="table-layout:auto"}

### [!UICONTROL Cost]

Geben Sie die Istkosten des Artikels ein.

### [!UICONTROL Customer Group Price]

![Advanced Pricing](./assets/product-pricing-advanced-group-price.png){width="600" zoomable="yes"}

Richtet Werbe- und Stufenpreise für bestimmte Kundengruppen ein.

| Element | Beschreibung |
| ---- | ----------- |
| [!UICONTROL Website] | Gibt die Website an, auf die die Gruppenpreisregel angewendet wird. Diese Option wird nur angezeigt, wenn die Installation über mehrere Websites verfügt. |
| [!UICONTROL Customer Group] | (Erforderlich) Gibt die Kundengruppe an, die für den Erhalt des Rabattpreises qualifiziert ist. Wenn ein Wert in einem Gruppen- oder Katalogfeld geändert wird, wird die entsprechende benutzerdefinierte Preiszeile, die mit der vorherigen Einstellung übereinstimmt, aus dem freigegebenen Katalog gelöscht. <br/>**[!UICONTROL ALL GROUPS]**- Wendet die Regel auf alle Kundengruppen an.<br/>**[!UICONTROL NOT LOGGED IN]** - Wendet die Regel „Gäste und Kunden“ an, die nicht bei ihren Konten angemeldet sind. |
| [!UICONTROL Quantity] | Gibt die Menge an, die erforderlich ist, um einen Stufenpreis zu erhalten. |
| [!UICONTROL Price] | (Erforderlich) Gibt einen festen oder ermäßigten Produktpreis für Mitglieder der Kundengruppe innerhalb der spezifischen Website an. Optionen: <br/>**[!UICONTROL Fixed]**- (Standard) Der Rabattpreis wird als fester Dezimalwert eingegeben. Geben Sie beispielsweise `9.99` als Rabattpreis ein.<br/>**[!UICONTROL Discount]** - Der Rabattpreis wird als Prozentsatz (%) des Basisproduktpreises eingegeben. Geben Sie beispielsweise `10` für einen Rabatt von 10 % ein. |
| ![Papierkorb-Symbol](../assets/icon-delete-trashcan-solid.png) | Löscht die aktuelle Regel. |
| **[!UICONTROL Add]** | Fügt eine weitere Zeile für eine neue Regel ein. |

{style="table-layout:auto"}

### [!UICONTROL Catalog and Tier Price]

Richtet Werbe- und Stufenpreise für bestimmte freigegebene Kataloge und Kundengruppen ein.

{{b2b-feature}}

![Erweiterte Preise für B2B-Stores mit freigegebenen Katalogen](./assets/product-pricing-advanced.png){width="600" zoomable="yes"}

| Element | Beschreibung |
|----|-----------|
| [!UICONTROL Website] | Gibt die Website an, auf die die Gruppenpreisregel angewendet wird. Diese Option wird nur angezeigt, wenn die Installation über mehrere Websites verfügt. <br>**_Important:_**&#x200B;Wählen Sie_ Website_ in der Konfiguration [Katalogpreisbereich](catalog-price-scope.md), andernfalls werden die festgelegten erweiterten Preise für **alle**-Websites angezeigt. |
| [!UICONTROL Group or Catalog] | (Erforderlich) Gibt die Kundengruppe oder den freigegebenen Katalog an, die bzw. der für den Erhalt des Rabattpreises qualifiziert ist. Wenn ein Wert in einem Gruppen- oder Katalogfeld geändert wird, wird die entsprechende benutzerdefinierte Preiszeile, die mit der vorherigen Einstellung übereinstimmt, aus dem freigegebenen Katalog gelöscht. <br/>**[!UICONTROL ALL GROUPS]**- Wendet die Regel auf alle Kundengruppen an. Der Wert wird nicht auf den freigegebenen Katalog angewendet, und Änderungen an den erweiterten Preisdaten werden nicht mit dem freigegebenen Katalog synchronisiert.<br/>**[!UICONTROL NOT LOGGED IN]** - Wendet die Regel „Gäste und Kunden“ an, die nicht bei ihren Konten angemeldet sind.<br/>**[!UICONTROL Shared Catalogs]**- Wendet die Regel auf einen bestimmten freigegebenen Katalog an. |
| Menge | Gibt die Menge an, die erforderlich ist, um einen Stufenpreis zu erhalten. |
| [!UICONTROL Price] | (Erforderlich) Gibt einen festen oder ermäßigten Produktpreis für Mitglieder der Kundengruppe innerhalb der spezifischen Website an. Optionen: <br/>**[!UICONTROL Fixed]**- (Standard) Der Rabattpreis wird als fester Dezimalwert eingegeben. Geben Sie beispielsweise `9.99` als Rabattpreis ein.<br/>**[!UICONTROL Discount]** - Der Rabattpreis wird als Prozentsatz (%) des Basisproduktpreises eingegeben. Geben Sie beispielsweise `10` für einen Rabatt von 10 % ein. |
| ![Papierkorb-Symbol](../assets/icon-delete-trashcan-solid.png) | Löscht die aktuelle Regel. |
| **[!UICONTROL Add]** | Fügt eine weitere Zeile für eine neue Regel ein. |

{style="table-layout:auto"}

### [!UICONTROL Minimum Advertised Price]

Der minimale Angebotspreis (MAP) für das Produkt.

### [!UICONTROL Display Actual Price]

Bestimmt, wo der tatsächliche Preis des Produkts für den Kunden sichtbar ist.

| Element | Beschreibung |
|----|-----------|
| [!UICONTROL Use Config] | Verwendet die aktuelle Konfigurationseinstellung für die Preisanzeige. |
| [!UICONTROL On Gesture] | Zeigt den tatsächlichen Produktpreis in einem Popup als Antwort auf die _Klick für Preis_ oder _Was ist das?_ Link. |
| [!UICONTROL In Cart] | Zeigt den tatsächlichen Produktpreis im Warenkorb an. |
| [!UICONTROL Before Order Confirmation] | Zeigt den tatsächlichen Produktpreis am Ende des Checkout-Prozesses an, unmittelbar vor der Absendung der Bestellung. |

{style="table-layout:auto"}
