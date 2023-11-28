---
title: Inventar erweitern und umstrukturieren
description: Erfahren Sie, wie Sie zu einem Multi-Source-Händler erweitern oder auf einen Einzelquell-Händler reduzieren können.
exl-id: 880474e3-6533-4b2f-adf7-4312787ff736
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---

# Inventar erweitern und umstrukturieren

Je mehr Ihr Unternehmen wächst und sich ändert, desto mehr [!DNL Inventory Management] unterstützt Ihre Anforderungen. Sie können zu einem Händler mit mehreren Quellen erweitern oder auf einen Einzelquellenhändler reduzieren.

## In mehrere Quellen erweitern

Einzelquellenhändler können neue Geschäfte, Lagerhäuser, Spediteure und mehr hinzufügen. Für das Erweitern auf Multi-Sourcing sind nur wenige Ergänzungen und Lageraktualisierungen erforderlich:

1. Hinzufügen [benutzerdefinierte Quellen](sources-add.md) für jeden neuen Standort.

   Sie verwenden nur die Standardquelle für Bundle-Produkte.

1. Hinzufügen [benutzerdefinierte Bestände](stocks-add.md) nach Bedarf für Ihre neuen Quellen.

   Sie können beispielsweise Lagerbestände pro Website, Land, Gebietsschema oder anderer Methode erstellen. Sie können Ihren benutzerdefinierten Lagern Quellen zuweisen. Sie verwenden nur den Standardspeicher für Bundle-Produkte.

1. Aktualisieren [Quellzuweisungen und -mengen](quantities-manage.md) für Ihre Produkte.

   Sie können auch die [Werkzeug für Massenaktionen](bulk-assignment.md) und [Import-Export](inventory-import-export.md) Funktion zum schnellen Hinzufügen von Quellen und Produktdaten.

## Neustrukturierung in eine einzelne Quelle

Für Händler mit mehreren Quellen, die Online-Verkäufe für den Versand an einen Ort reduzieren möchten, ändern Sie die Quellen, Lager und Mengen, die aktualisiert werden sollen:

1. Deaktivieren [benutzerdefinierte Quellen](sources-disable.md).

1. Übertragen Sie den Produktbestand in Ihre Standardquelle.

   Die Verwendung von Massenaktionen wird empfohlen. Siehe [Übertragen des Bestands an die Quelle](inventory-transfer.md).

1. Weisen Sie alle Websites dem [Standardbestand](stocks-manage.md).
