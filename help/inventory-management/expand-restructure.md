---
title: Inventar erweitern und neu strukturieren
description: Erfahren Sie, wie Sie sich zu einem Händler aus mehreren Quellen entwickeln oder auf einen Händler aus einer Hand reduzieren können.
exl-id: 880474e3-6533-4b2f-adf7-4312787ff736
feature: Inventory, Configuration
TQID: https://experienceleague.adobe.com/w4TV-BQrg0RzlHn4DVSdHFPD2M5CF11wA7I5OyA7jsY
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 219
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
