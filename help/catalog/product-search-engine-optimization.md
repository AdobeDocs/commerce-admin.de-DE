---
title: Produkteinstellungen - [!UICONTROL Search Engine Optimization]
description: Für ein Produkt legen die [!UICONTROL Search Engine Optimization] den URL-Schlüssel und die Metadaten fest, die von Suchmaschinen zur Indizierung des Produkts verwendet werden.
exl-id: 78888094-759c-4e45-afcd-65858ee76159
feature: Catalog Management, Products, Search
TQID: https://experienceleague.adobe.com/ya6B95jMPXfOYW785xN7WrmbFOwtKXdcr7yXTDvOAcw
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 5e73225b71682f6d2527dab772abe0301ce5f0c8
workflow-type: tm+mt
source-wordcount: 531
ht-degree: 0%

---

# Produkteinstellungen - [!UICONTROL Search Engine Optimization]

_Suchmaschinenoptimierung_ (SEO) ist die Praxis der Feinabstimmung des Inhalts und der Präsentation einer Site, um die Art und Weise zu verbessern, wie die Seiten von Suchmaschinen indiziert werden.

Die _[!UICONTROL Search Engine Optimization]_&#x200B;für ein Produkt geben die Felder [URL-Schlüssel](catalog-urls.md) und [Meta-Daten](../merchandising-promotions/meta-data.md) an, die von Suchmaschinen zur Indizierung des Produkts verwendet werden. Obwohl einige Suchmaschinen Meta-Keywords ignorieren, werden diese von anderen Suchmaschinen weiterhin verwendet. Die aktuelle [SEO Best Practice](../merchandising-promotions/seo-overview.md) besteht darin, hochwertige Keywords sowohl in den Meta-Titel als auch in die Meta-Beschreibung einzubinden.

Der Standardwert für jedes Metadatenfeld kann automatisch basierend auf den in der Konfiguration angegebenen Werten generiert werden. Jedes Feld enthält einen Platzhalter, der durch einen tatsächlichen Wert ersetzt wird. Weitere Informationen finden Sie unter [Produktfelder automatisch generieren](../configuration-reference/catalog/catalog.md#uicontrol-product-fields-auto-generation).

>[!NOTE]
>
>Die Kataloganreicherung hilft bei der Verbesserung von Produktnamen und Beschreibungen für LLM und die KI-gestützte Erkennung. SEO-Metafelder werden nicht ersetzt. Weitere Informationen finden Sie unter [Kataloganreicherung](catalog-enrichment.md).

## Ausfüllen der SEO-Felder

1. Öffnen Sie das Produkt im Bearbeitungsmodus.

1. Scrollen Sie nach unten und erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt _[!UICONTROL Search Engine Optimization]_.

![Suchmaschinenoptimierung](./assets/product-search-engine-optimization.png){width="600" zoomable="yes"}


1. Geben Sie die **[!UICONTROL URL Key]** ein (optional).

   Der Standard-URL-Schlüssel basiert auf dem Produktnamen. Sie können die Standardeinstellung verwenden oder nach Bedarf ändern. Weitere Informationen finden Sie unter [Katalog-URLs](catalog-urls.md).

1. Geben Sie die **[!UICONTROL Meta Title]** ein (optional).

   Der Meta-Titel ist der Text, der oben im Browser-Fenster angezeigt wird. Sie können die Standardeinstellung verwenden, die auf dem Produktnamen basiert, oder sie nach Bedarf ändern.

1. Fügen Sie die **[!UICONTROL Meta Keywords]** hinzu (optional).

   Die Meta-Keywords werden von einigen Suchmaschinen häufiger verwendet als von anderen. Es empfiehlt sich, einige hochwertige Schlüsselwörter einzugeben, um dem Produkt mehr Sichtbarkeit zu verschaffen.

1. Geben Sie die **[!UICONTROL Meta Description]** ein.

   Die Metabeschreibung ist der Text, der in den Suchergebnislisten angezeigt wird. Um optimale Ergebnisse zu erzielen, geben Sie eine Beschreibung ein, die zwischen 150 und 160 Zeichen lang ist.

## Feldverweis

| Feld | [Umfang](../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |------------------|
| [!UICONTROL URL Key] | Shop-Ansicht | Bestimmt die Online-Adresse des Produkts. Der URL-Schlüssel wird zur Basis-URL des Stores hinzugefügt und in der Adressleiste eines Browsers angezeigt. Commerce erstellt zunächst eine _suchmaschinenfreundliche_ URL, die auf dem Produktnamen basiert. Der URL-Schlüssel sollte aus Kleinbuchstaben bestehen und nicht nachfolgende Bindestriche anstelle von Leerzeichen enthalten. Fügen Sie kein Suffix wie `.html` in den URL-Schlüssel ein, da er in der Konfiguration verwaltet wird. |
| [!UICONTROL Meta Title] | Shop-Ansicht | Der Titel wird in der Titelleiste und auf der Registerkarte Ihres Browsers angezeigt und wird auch als Titel auf einer Suchmaschinenergebnisseite (SERP) verwendet. Der Meta-Titel sollte für die Seite eindeutig sein und weniger als 70 Zeichen lang sein. Automatisch erstellter Wert: `{{name}}` |
| [!UICONTROL Meta Keywords] | Shop-Ansicht | Relevante Schlüsselwörter für das Produkt. Erwägen Sie die Verwendung von Keywords, mit denen Kunden das Produkt finden können. Automatisch erstellter Wert: `{{name}}` |
| [!UICONTROL Meta Description] | Shop-Ansicht | Die Meta-Beschreibung bietet einen kurzen Überblick über die Seite für Suchergebnislisten. Eine ideale Länge liegt zwischen 150 und 160 Zeichen, maximal jedoch 255 Zeichen. Obwohl sie für den Kunden nicht sichtbar sind, enthalten einige Suchmaschinen die Meta-Beschreibung auf der Suchergebnisseite. Automatisch erstellter Wert: `{{name}} {{description}}` |

{style="table-layout:auto"}
