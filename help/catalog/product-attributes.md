---
title: Übersicht über Produktattribute
description: Erfahren Sie mehr über Produktattribute und wie sie zur Beschreibung bestimmter Merkmale eines Produkts verwendet werden.
exl-id: e15770ee-fb71-43f0-8c26-e8029935799a
feature: Catalog Management, Products
source-git-commit: e0468763b2314e69e8ee4922da9bb9cf65578904
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 0%

---

# Übersicht über Produktattribute

Attribute sind die Bausteine Ihres Produktkatalogs und beschreiben spezifische Merkmale eines Produkts. Produktattribute können in &quot;[&quot; unterteilt ](attribute-sets.md), die dann als Vorlagen zum Erstellen von Produkten verwendet werden.

Attribute bestimmen den Typ des Eingabedialogs, der für Produktoptionen verwendet wird, und geben zusätzliche Informationen für Produktseiten an. Sie werden auch als Suchparameter und Kriterien für mehrschichtige Navigation, Produktvergleichsberichte und Werbeaktionen verwendet. Sie können so viele Attribute und Attributsätze erstellen, wie erforderlich sind, um die Produkte in Ihrem Katalog zu beschreiben. Zusätzlich zu den Attributen, die Sie erstellen können, sind Systemattribute, wie z. B. Preis, in die Commerce-Kernplattform integriert und können nicht geändert werden.

![Erstellen eines neuen Attributs beim Bearbeiten eines Produkts](./assets/product-attribute-add-new.png){width="600" zoomable="yes"}

Verwenden Sie die in den folgenden Abschnitten beschriebenen Best Practices, wenn Sie Produktattribute planen und erstellen.

## Attributnamen

Konsistente Konventionen für die Attributbenennung, einschließlich Groß- und Kleinschreibung und Zeichensetzung. Beispielsweise können `Color:Green` und `Color:green` von verschiedenen Systemen als zwei verschiedene Attributwerte betrachtet werden. Ein solches Rauschen in den Daten kann sich auf Geschäftsregeln, Suchergebnisse und Datenfilter für Anwendungen auswirken, die Produkte mit Regeln übereinstimmen.

## Attributverwendung

Überlegen Sie, wie Attribute beim Zuweisen von Eigenschaften und Werten verwendet werden sollen. Identifizieren Sie die Attribute, die als Beschriftungen für die Präsentation verwendet werden, z. B. Produktname, Bild, Preis und Beschreibung, und welche Attribute für die Dateneingabe verwendet werden. Beachten Sie, wie die Attribute auf verschiedenen Seiten auf der Website dargestellt werden und wie sie auf Kategorieseiten, Produktdetailseiten, Kategorienrastern und Miniatur-Reglern angezeigt werden.

## Farbe

Ad-hoc-Farbbeschreibungen können aus Sicht von Datenbankvorgängen eine Herausforderung darstellen. Farbnamen wie „Azure Skies“ oder „Robin Egg Blue“ sind sehr ansprechend, liefern jedoch möglicherweise nicht die besten Ergebnisse, wenn sie als Suchkriterien verwendet werden oder wenn Sie für das Merchandising `Color_Family:Blue` angeben müssen. Berücksichtigen Sie, wie Farben in Suchergebnissen und in der mehrschichtigen Navigation dargestellt werden, und legen Sie einige Richtlinien für Ihre Geschäftsanforderungen fest. Weisen Sie dann Farbattributwerte im gesamten Katalog konsistent zu.

## Variantenverwaltung

Verwenden Sie [Konfigurationsoptionen](product-configurations.md) und [konfigurierbare Produkte](product-create-configurable.md) um Varianten in Ihren Produktangeboten zu verwalten. Diese Funktionen erleichtern die Kategorisierung von Produkten, die Erstellung von Regeln für den Warenkorbpreis und dynamische Kategorien sowie die Bereitstellung einer Auswahl von Optionen mit verschiedenen Text-, Auswahl- und Datumseingabetypen.

## Gewichtete Suche

Produktattributen, die für die [Katalogsuche](search.md) aktiviert sind, kann eine Gewichtung zugewiesen werden, um ihnen einen höheren Wert in den Suchergebnissen zu verleihen. Attribute mit einer größeren Gewichtung werden vor Attributen mit einer niedrigeren Gewichtung zurückgegeben. Betrachten Sie beispielsweise zwei Attribute im System, _color_ mit der Suchgewichtung 3 und _description_ mit der Suchgewichtung 1. Die Suche nach dem Wort _rot_ gibt eine Liste von Produkten mit dem Farbattributwert `red` zurück, gibt jedoch keine Produkte mit Beschreibungen zurück, die das Wort _rot_ enthalten. In diesem Beispiel hat das Attribut `color` eine größere definierte Gewichtung als das Attribut `description` .

## Nicht verwendete Eigenschaften

Entfernen Sie nicht verwendete Produkteigenschaften, um eine bessere Strukturierung und schnellere Indizierung zu ermöglichen.


>[HINWEIS!]
>
>Informationen zur Leistungsoptimierung der Produktattributkonfiguration finden Sie unter [Best Practices für die Katalogverwaltung](https://experienceleague.adobe.com/en/docs/commerce-operations/implementation-playbook/best-practices/planning/catalog-management#product-attributes) im _Implementierungs-Playbook_.
