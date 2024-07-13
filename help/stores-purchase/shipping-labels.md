---
title: Versandtitel
description: Erfahren Sie mehr über den Workflow für die Versandbeschriftung für regelmäßige Sendungen und Produkte mit der Autorisierung von Rücksendungen.
exl-id: 5da03cf9-5e92-4bb8-ba53-67c6469665ed
feature: Shipping/Delivery, Orders
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

---

# Versandtitel

Commerce verfügt über eine weit reichende Integration mit den wichtigsten Versandunternehmen, die Ihnen den Zugriff auf die Versandsysteme von Frachtführern ermöglicht, um Bestellungen zu verfolgen, Versandbeschriftungen zu erstellen und vieles mehr. Für regelmäßige Sendungen und Produkte mit Rücksendungserlaubnis können Versandetiketten erstellt werden. Zusätzlich zu den vom Versandunternehmen übermittelten Informationen enthält das Etikett auch die Commerce-Bestellnummer, die Paketnummer und die Gesamtverpackungsmenge für die Sendung.

![USPS Priority Shipping Label](./assets/shipping-usps-priority-label.png){width="300"}

- [Konfigurieren von Versandbeschriftungen](shipping-label-configure.md)
- [Erstellen von Versandbeschriftungen und Packages](shipping-label-create.md)

## Versandtitel-Workflow

Versandtitel können zum Zeitpunkt der Erstellung einer Sendung oder später erstellt werden. Versandtitel werden im PDF-Format gespeichert und auf Ihren Computer heruntergeladen.

### Schritt 1: Der Händler sendet eine Anforderung für den Versandtitel

Der Händler/Store-Manager füllt die zum Generieren von Bezeichnungen erforderlichen Informationen aus und sendet die Anfrage.

### Schritt 2: Anfrage an den Netzbetreiber senden

Commerce kontaktiert den Spediteur und erstellt eine Bestellung im System des Spediteurs. Für jedes versandte Paket wird eine separate Bestellung erstellt.

### Schritt 3: Netzbetreiber sendet Titel und Trackingnummer

Der Frachtführer sendet das Versandetikett und die Trackingnummer für die Sendung.

- Eine einzelne Sendung mit mehreren Packages erhält mehrere Versandtitel.

- Wenn Sie dieselben Versandbeschriftungen mehrmals generieren, bleiben die ursprünglichen Trackingnummern erhalten.

- Bei zurückgegebenen Produkten mit RMA-Nummern werden die alten Trackingnummern durch neue ersetzt.

### Schritt 4: Der Händler lädt den Titel herunter und druckt ihn aus

Nach der Erstellung des Versandetiketts wird der neue Versand gespeichert und das Etikett gedruckt. Wenn das Versandetikett aufgrund von Verbindungsproblemen oder anderen Gründen nicht erstellt werden kann, wird die Sendung nicht erstellt. Je nach Browsereinstellungen kann die PDF-Datei geöffnet und gedruckt werden. Jede Bezeichnung wird auf einer separaten Seite im PDF angezeigt.
