---
title: Produkteinstellungen - [!UICONTROL Search Engine Optimization]
description: Für ein Produkt legen die Einstellungen für [!UICONTROL Search Engine Optimization] den URL-Schlüssel und die Metadaten fest, die von Suchmaschinen für die Indizierung des Produkts verwendet werden.
exl-id: 78888094-759c-4e45-afcd-65858ee76159
feature: Catalog Management, Products, Search
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 0%

---

# Produkteinstellungen - [!UICONTROL Search Engine Optimization]

_Suchmaschinenoptimierung_ (SEO) ist die Vorgehensweise, den Inhalt und die Darstellung einer Site zu optimieren, um die Indexierung der Seiten durch Suchmaschinen zu verbessern.

In den _[!UICONTROL Search Engine Optimization]_-Einstellungen für ein Produkt werden die Felder [URL-Schlüssel](catalog-urls.md) und [Meta-Daten](../merchandising-promotions/meta-data.md) angegeben, die von Suchmaschinen für die Indizierung des Produkts verwendet werden. Obwohl einige Suchmaschinen Meta-Suchbegriffe ignorieren, verwenden andere Suchmaschinen sie weiterhin. Die aktuelle Best Practice für [SEO](../merchandising-promotions/seo-overview.md) besteht darin, hochwertige Suchbegriffe sowohl in den Metaptitel als auch in die Meta-Beschreibung zu integrieren.

Der Standardwert für jedes Metadatenfeld kann automatisch anhand der in der Konfiguration angegebenen Werte generiert werden. Jedes Feld enthält einen Platzhalter, der durch einen tatsächlichen Wert ersetzt wird. Weitere Informationen finden Sie unter [Automatische Erstellung von Produktfeldern](../configuration-reference/catalog/catalog.md#uicontrol-product-fields-auto-generation).

## Füllen Sie die SEO-Felder aus

1. Öffnen Sie das Produkt im Bearbeitungsmodus.

1. Scrollen Sie nach unten und erweitern Sie den Abschnitt _[!UICONTROL Search Engine Optimization]_um den ![Erweiterungsselektor](../assets/icon-display-expand.png).

![Suchmaschinenoptimierung](./assets/product-search-engine-optimization.png){width="600" zoomable="yes"}


1. Geben Sie den Wert **[!UICONTROL URL Key]** ein (optional).

   Der Standard-URL-Schlüssel basiert auf dem Produktnamen. Sie können die Standardeinstellung verwenden oder sie nach Bedarf ändern. Weitere Informationen finden Sie unter [Katalog-URLs](catalog-urls.md).

1. Geben Sie den Wert **[!UICONTROL Meta Title]** ein (optional).

   Der Metadatentitel ist der Text, der oben im Browser-Fenster angezeigt wird. Sie können die Standardeinstellung verwenden, die auf dem Produktnamen basiert, oder sie nach Bedarf ändern.

1. Fügen Sie die **[!UICONTROL Meta Keywords]** hinzu (optional).

   Die Meta-Keywords werden von einigen Suchmaschinen häufiger verwendet als andere. Es empfiehlt sich, einige wichtige Schlüsselwörter mit hohem Wert einzugeben, um das Produkt sichtbarer zu machen.

1. Geben Sie den Wert **[!UICONTROL Meta Description]** ein.

   Die Meta-Beschreibung ist der Text, der in den Suchergebnislisten angezeigt wird. Die besten Ergebnisse erzielen Sie, wenn Sie eine Beschreibung mit einer Länge von 150 bis 160 Zeichen eingeben.

## Feldreferenz

| Feld | [Umfang](../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |------------------|
| [!UICONTROL URL Key] | Store-Ansicht | Legt die Online-Adresse des Produkts fest. Der URL-Schlüssel wird der Basis-URL des Stores hinzugefügt und in der Adressleiste eines Browsers angezeigt. Commerce erstellt zunächst eine _suchmaschinenfreundliche_ URL, die auf dem Produktnamen basiert. Der URL-Schlüssel sollte aus Kleinbuchstaben bestehen, wobei zwischen diesen Zeichen keine Bindestriche und keine Leerzeichen stehen. Schließen Sie kein Suffix wie `.html` in den URL-Schlüssel ein, da es in der Konfiguration verwaltet wird. |
| [!UICONTROL Meta Title] | Store-Ansicht | Der Titel wird in der Titelleiste und auf der Registerkarte Ihres Browsers angezeigt und auch als Titel auf einer Suchmaschinen-Ergebnisseite (SERP) verwendet. Der Metadatentitel sollte für die Seite eindeutig und weniger als 70 Zeichen lang sein. Automatisch generierter Wert: `{{name}}` |
| [!UICONTROL Meta Keywords] | Store-Ansicht | Relevante Suchbegriffe für das Produkt. Erwägen Sie die Verwendung von Keywords, die Kunden möglicherweise verwenden, um das Produkt zu finden. Automatisch generierter Wert: `{{name}}` |
| [!UICONTROL Meta Description] | Store-Ansicht | Die Meta-Beschreibung bietet einen kurzen Überblick über die Seite für die Liste der Suchergebnisse. Die ideale Länge beträgt 150 bis 160 Zeichen, höchstens 255 Zeichen. Obwohl für den Kunden nicht sichtbar, enthalten einige Suchmaschinen die Meta-Beschreibung auf der Suchergebnisseite. Automatisch generierter Wert: `{{name}} {{description}}` |

{style="table-layout:auto"}
