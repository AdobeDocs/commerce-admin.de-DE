---
title: Produkteinstellungen - [!UICONTROL Search Engine Optimization]
description: Für ein Produkt legen die [!UICONTROL Search Engine Optimization] den URL-Schlüssel und die Metadaten fest, die von Suchmaschinen zur Indizierung des Produkts verwendet werden.
exl-id: 78888094-759c-4e45-afcd-65858ee76159
feature: Catalog Management, Products, Search
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 0%

---

# Produkteinstellungen - [!UICONTROL Search Engine Optimization]

_Suchmaschinenoptimierung_ (SEO) ist die Praxis der Feinabstimmung des Inhalts und der Präsentation einer Site, um die Art und Weise zu verbessern, wie die Seiten von Suchmaschinen indiziert werden.

Die _[!UICONTROL Search Engine Optimization]_&#x200B;für ein Produkt geben die Felder [URL-Schlüssel](catalog-urls.md) und [Meta-Daten](../merchandising-promotions/meta-data.md) an, die von Suchmaschinen zur Indizierung des Produkts verwendet werden. Obwohl einige Suchmaschinen Meta-Keywords ignorieren, werden diese von anderen Suchmaschinen weiterhin verwendet. Die aktuelle [SEO Best Practice](../merchandising-promotions/seo-overview.md) besteht darin, hochwertige Keywords sowohl in den Meta-Titel als auch in die Meta-Beschreibung einzubinden.

Der Standardwert für jedes Metadatenfeld kann automatisch basierend auf den in der Konfiguration angegebenen Werten generiert werden. Jedes Feld enthält einen Platzhalter, der durch einen tatsächlichen Wert ersetzt wird. Weitere Informationen finden Sie unter [Produktfelder automatisch generieren](../configuration-reference/catalog/catalog.md#uicontrol-product-fields-auto-generation).

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
