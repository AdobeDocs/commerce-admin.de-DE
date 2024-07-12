---
title: Übersicht über Produktattribute
description: Erfahren Sie mehr über Produktattribute und ihre Verwendung zur Beschreibung spezifischer Merkmale eines Produkts.
exl-id: e15770ee-fb71-43f0-8c26-e8029935799a
feature: Catalog Management, Products
source-git-commit: e0468763b2314e69e8ee4922da9bb9cf65578904
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 0%

---

# Übersicht über Produktattribute

Attribute sind die Bausteine Ihres Produktkatalogs und beschreiben spezifische Eigenschaften eines Produkts. Produktattribute können in [Attributsätze](attribute-sets.md) organisiert werden, die dann als Vorlagen zum Erstellen von Produkten verwendet werden.

Attribute bestimmen den Typ des Eingabeditors, der für Produktoptionen verwendet wird, und geben zusätzliche Informationen für Produktseiten an. Sie werden auch als Suchparameter und Kriterien für die Navigation auf mehreren Ebenen, Produktvergleichsberichte und Promotions verwendet. Sie können beliebig viele Attribute und Attributsätze erstellen, um die Produkte in Ihrem Katalog zu beschreiben. Neben den Attributen, die Sie erstellen können, werden Systemattribute wie der Preis in die Commerce-Hauptplattform integriert und können nicht geändert werden.

![Erstellen eines neuen Attributs beim Bearbeiten eines Produkts](./assets/product-attribute-add-new.png){width="600" zoomable="yes"}

Verwenden Sie die in den folgenden Abschnitten beschriebenen Best Practices, wenn Sie Produktattribute planen und erstellen.

## Attributnamen

Konsistente Konventionen für die Attributbenennung festlegen, einschließlich Groß-/Kleinschreibung und Satzzeichen. Beispielsweise können `Color:Green` und `Color:green` von verschiedenen Systemen als zwei verschiedene Attributwerte betrachtet werden. Ein solcher Datenlärm kann sich auf Geschäftsregeln, Suchergebnisse und Datenfilter für Anwendungen auswirken, die Produkte Regeln zuordnen.

## Attributverwendung

Überlegen Sie, wie Attribute beim Zuweisen von Eigenschaften und Werten verwendet werden sollen. Identifizieren Sie die Attribute, die als Beschriftungen für die Präsentation verwendet werden, wie z. B. Produktname, Bild, Preis und Beschreibung, und welche Attribute für die Dateneingabe verwendet werden. Betrachten Sie, wie Attribute auf verschiedenen Seiten der Site dargestellt werden und wie sie auf Kategorieseiten, Produktdetailseiten, Kategorirasten und Miniaturansichten angezeigt werden.

## Farbe

Ad-hoc-Farbbeschreibungen können aus Sicht von Datenbankvorgängen eine Herausforderung darstellen. Farbnamen wie &quot;Azure Skies&quot;oder &quot;Robin Egg Blue&quot;haben eine große Anziehungskraft, geben jedoch möglicherweise nicht die besten Ergebnisse zurück, wenn sie als Suchkriterien verwendet werden oder wenn Sie für das Merchandising `Color_Family:Blue` angeben müssen. Überlegen Sie, wie Farben in Suchergebnissen und in der Navigation auf mehreren Ebenen dargestellt werden, und legen Sie einige Richtlinien für Ihre Geschäftsanforderungen fest. Seien Sie dann konsistent, wenn Sie Farbattributwerte in Ihrem Katalog zuweisen.

## Variantenverwaltung

Verwenden Sie die Produktkonfigurationsoptionen [](product-configurations.md) und [konfigurierbare Produkte](product-create-configurable.md), um Varianten in Ihren Produktangeboten zu verwalten. Diese Funktionen erleichtern die Kategorisierung von Produkten, die Erstellung von Preisregeln für Warenkorb und dynamischen Kategorienregeln sowie die Auswahl von Optionen mit verschiedenen Eingabe-Typen für Text, Auswahl und Datum.

## Gewichtete Suche

Produktattributen, die für die [Katalogsuche](search.md) aktiviert sind, können eine Gewichtung zugewiesen werden, um ihnen einen höheren Wert in den Suchergebnissen zu geben. Attribute mit einer höheren Gewichtung werden vor denen mit einer niedrigeren Gewichtung zurückgegeben. Betrachten Sie beispielsweise zwei Attribute im System: _Farbe_ mit einer Suchgewichtung von 3 und _Beschreibung_ mit einer Suchgewichtung von 1. Bei der Suche nach dem Wort _red_ wird eine Liste von Produkten mit dem Farbattributwert `red` zurückgegeben, jedoch keine Produkte mit Beschreibungen, die das Wort _red_ enthalten. In diesem Beispiel hat das Attribut `color` eine größere definierte Gewichtung als das Attribut `description`.

## Nicht verwendete Eigenschaften

Entfernen Sie nicht verwendete Produkteigenschaften für eine bessere Strukturierung und schnellere Indizierung.


>[HINWEIS!]
>
>Informationen zur Optimierung der Produktattributkonfiguration für die Leistung finden Sie unter [Best Practices für die Katalogverwaltung](https://experienceleague.adobe.com/en/docs/commerce-operations/implementation-playbook/best-practices/planning/catalog-management#product-attributes) im _Playbook für die Implementierung_.
