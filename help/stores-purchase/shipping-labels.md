---
title: Versand-Kennzeichnungen
description: Erfahren Sie mehr über den Workflow für den Versand von Etiketten für reguläre Sendungen und Produkte mit Warenrücksendegenehmigung.
exl-id: 5da03cf9-5e92-4bb8-ba53-67c6469665ed
feature: Shipping/Delivery, Orders
TQID: https://experienceleague.adobe.com/Cjf9-372TRGIfWXpWR20OUII5XorPdfO1qgG-b2yPYI
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 314
ht-degree: 0%

---

# Versand-Kennzeichnungen

Commerce bietet einen hohen Integrationsgrad mit wichtigen Spediteuren, der Ihnen Zugriff auf Spediteursysteme bietet, um Bestellungen zu verfolgen, Versandkennzeichnungen zu erstellen und vieles mehr. Für reguläre Sendungen und Produkte mit Warenrücksendegenehmigung können Versandkennzeichnungen erstellt werden. Zusätzlich zu den vom Spediteur bereitgestellten Informationen enthält das Etikett auch die Commerce-Bestellnummer, die Nummer der Verpackung und die Gesamtmenge der Packstücke für die Sendung.

![USPS Priority Shipping Label](./assets/shipping-usps-priority-label.png){width="300"}

- [Konfigurieren von Versandkennzeichnungen](shipping-label-configure.md)
- [Erstellen von Versandkennzeichnungen und -paketen](shipping-label-create.md)

## Workflow für Versandtitel

Versandaufkleber können zum Zeitpunkt der Sendungserstellung oder zu einem späteren Zeitpunkt erstellt werden. Versandetiketten werden im PDF-Format gespeichert und auf Ihren Computer heruntergeladen.

### Schritt 1: Händler reicht Anfrage für Versandtitel ein

Der Händler/Store-Manager füllt die Informationen aus, die zum Generieren von Kennzeichnungen erforderlich sind, und sendet die Anfrage.

### Schritt 2: Anfrage an Provider gesendet

Commerce kontaktiert den Spediteur und erstellt eine Bestellung im System des Spediteurs. Für jedes Paket, das versendet wird, wird eine separate Bestellung erstellt.

### Schritt 3: Provider sendet Titel und Tracking-Nummer

Der Spediteur sendet das Versandetikett und die Sendungsnummer für die Sendung.

- Eine einzelne Sendung mit mehreren Paketen erhält mehrere Versandaufkleber.

- Wenn Sie dieselben Versandkennzeichnungen mehrmals generieren, bleiben die ursprünglichen Tracking-Nummern erhalten.

- Bei zurückgegebenen Produkten mit RMA-Nummern werden die alten Tracking-Nummern durch neue ersetzt.

### Schritt 4: Händler lädt das Label herunter und druckt es aus

Nachdem das Versandlabel generiert wurde, wird die neue Sendung gespeichert und das Label kann gedruckt werden. Wenn die Versandkennzeichnung aufgrund von Verbindungsproblemen oder anderen Gründen nicht erstellt werden kann, wird die Sendung nicht erstellt. Abhängig von Ihren Browsereinstellungen kann die PDF-Datei geöffnet und gedruckt werden. Jede Beschriftung wird in der PDF auf einer separaten Seite angezeigt.
