---
title: Inventar erweitern und neu strukturieren
description: Erfahren Sie, wie Sie sich zu einem Händler aus mehreren Quellen entwickeln oder auf einen Händler aus einer Hand reduzieren können.
exl-id: 880474e3-6533-4b2f-adf7-4312787ff736
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---

# Inventar erweitern und neu strukturieren

Wenn Ihr Unternehmen wächst und sich ändert, unterstützt [!DNL Inventory Management] Ihre Anforderungen. Sie können sich zu einem Händler mit mehreren Quellen erweitern oder auf einen Händler mit nur einer Quelle reduzieren.

## Auf mehrere Quellen erweitern

Händler aus einer Hand können neue Stores, Warehouses, Drop-Shipper und mehr hinzufügen. Für die Erweiterung auf Multi-Sourcing sind nur wenige Ergänzungen und Stock-Updates erforderlich:

1. Fügen Sie [ neuen Speicherort ](sources-add.md)benutzerdefinierte Quellen“ hinzu.

   Sie verwenden nur die standardmäßige Source für Bundle-Produkte.

1. Fügen Sie [benutzerdefinierte Lager](stocks-add.md) nach Bedarf für Ihre neuen Quellen hinzu.

   Beispielsweise können Sie Lager nach Website, Land, Gebietsschema oder einer anderen Methode erstellen. Sie können Ihren benutzerdefinierten Lagern Quellen zuweisen. Sie verwenden nur den Standardbestand für Bundle-Produkte.

1. Aktualisieren Sie [Quellzuweisungen und -mengen](quantities-manage.md) für Ihre Produkte.

   Sie können auch die Funktionen [Massenaktionen-Tool](bulk-assignment.md) und [Import-Export](inventory-import-export.md) verwenden, um schnell Quellen und Produktdaten hinzuzufügen.

## Restrukturierung in eine einzige Quelle

Händler, die aus mehreren Quellen stammen und ihre Online-Verkäufe für den Versand auf einen Ort reduzieren möchten, ändern Ihre Quellen, Lager und Mengen, um sie zu aktualisieren:

1. Deaktivieren Sie [benutzerdefinierte Quellen](sources-disable.md).

1. Übertragen Sie den Produktbestand auf Ihre Standard-Source.

   Es wird empfohlen, Massenaktionen zu verwenden. Siehe [Lagertransfer zu Source](inventory-transfer.md).

1. Weisen Sie alle Websites dem [Standardlager“ ](stocks-manage.md).
