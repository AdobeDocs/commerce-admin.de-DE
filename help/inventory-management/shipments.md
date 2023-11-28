---
title: Verwalten von Bestellungen und Sendungen aus dem Bestand
description: Weitere Informationen [!DNL Inventory Management] Funktionen und Optionen zur Verwaltung der Lagerbestandsmengen durch den Versand.
exl-id: cc4ca518-d98c-48f3-9051-6fb3c6fae9fe
feature: Inventory, Shipping/Delivery
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '723'
ht-degree: 0%

---

# Verwalten von Bestellungen und Sendungen

[!DNL Inventory Management] umfasst zusätzliche Funktionen und Optionen für die Verwaltung der Lagerbestandsmengen durch den Versand. Während Sie Sendungen überprüfen und erfüllen, stornieren Sie Bestellungen und geben Sie Kreditkarten, Produktverkäufen und Eigenmengen automatisch aktualisieren.

Diese Informationen enthalten Details zu [!DNL Inventory Management]. Weitere Informationen finden Sie im Abschnitt [Bestellungen](../stores-purchase/orders.md){target="_blank"} Thema im _Handbuch für Verkaufs- und Kauferlebnisse_.

## Bestellungen

[!DNL Commerce] unterstützt Einzelaufträge und Mehradressen-Bestellungen standardmäßig ohne zusätzliche Konfigurationen. Wenn Kunden oder Mitarbeiter Bestellungen tätigen, [!DNL Inventory Management] erfasst Inventar unter Verwendung von Vorbehalten gegen die Verkaufsmenge, abgezogen von der Bestandsmenge für fakturierte und versandte Produkte.

### Bestellungen mit mehreren Adressen

Bei Bestellungen mit mehreren Adressen wird eine Reihe von Einzelbestellungen generiert - eine für jede eingegebene Zieladresse. Während des Checkouts wählen Kunden jeden Satz von Produkten, die pro Adresse beim Checkout zugeordnet sind, als einzelne Bestellungen entsprechend der Zieladresse aus. Jede Bestellung enthält die Produkte, die pro Adresse zugeordnet sind.

[!DNL Commerce] verwaltet Inventar für diese Multi-Adresse-Bestellungen genau wie Einzelbestellungen. Sie ermöglicht die Bereitstellung von Quellenselektionsalgorithmen für Empfehlungen oder Überschreibungen während des Versands, Teillieferungen, Stornierungen von Bestellungen und die Rückerstattung von Lageraktualisierungen.

![Multi-Adresse beim Checkout](assets/inventory-multi-ship.png){width="350" zoomable="yes"}

### Erstattungen

Bei Eingabe einer [Credit Memo](../stores-purchase/credit-memo-create.md){target="_blank"} um eine Rückerstattung zu erteilen, können Sie die Produktmenge an die abgezogene Quelle zurückgeben. Die Bestellinformationen enthalten die Inventarquelle, die das Produkt ausgeliefert hat. Es wird empfohlen, die zurückgegebene Produktmenge über ein Kreditmemo zuzuweisen, wenn Sie das zurückgegebene Produkt erhalten.

![Artikel, die mit ausgewählter Rückgabe an Lager zurückgezahlt werden](assets/credit-memo-items-to-refund.png)
{width="350" zoomable="yes"}

### Abbrechen nicht versandter Bestellungen

Wenn eine Bestellung nicht versandt wurde und storniert wird (ganz oder teilweise), [!DNL Inventory Management] gibt den Produktbestand automatisch in die verkaufbare Menge zurück. Bis Rechnung und Versand werden die gekauften Produkte gegen die verkaufbare Menge, nicht abgezogen von der tatsächlichen Menge, reserviert. Zum Zeitpunkt der Rechnungsstellung und des Versands der Bestellung wandelt das System die Reservierung in einen Inventarabzug um.

Hinter den Kulissen [!DNL Inventory Management] automatisch eine Ausgleichsreservierung eingibt, die den Aufbewahrungszeitraum der Produktmenge löst. Die Menge kehrt zur aggregierten virtuellen Verkaufsmenge zurück.

## Sendungen

Mit [!DNL Inventory Management] aktiviert ist, können Sie einen Teil oder komplette Sendungen aus einer oder mehreren Quellen versenden, um Bestellungen zu erfüllen. Sie kontrollieren Ihren ausgehenden Bestand für jede Bestellung, legen die abzugsfähigen Mengen fest, senden einen oder mehrere Sendungen und liefern Lagerbestände und Rückstände, da Bestand verfügbar ist. Geben Sie für jeden Zeileneintrag in der Reihenfolge einen Abzugsbetrag von der Quellmenge an. Generieren Sie eine Lieferung pro Quelle wie Lagerbestand, bis der gesamte Auftrag erfüllt ist.

### Teilverbringungen

Für Händler mit mehreren Quellen: [!DNL Commerce] erzeugt eine Lieferung für jede ausgewählte Quelle. Im allgemeinen Workflow können Sie eine Quelle auswählen, die Produktmenge so einstellen, dass sie von der Bestellung abgezogen wird, und mit dem Versand fortfahren. Erstellen Sie nach Abschluss des Vorgangs zusätzliche Sendungen für jede Quelle, bis Sie die Bestellung erfüllt haben.

Einzelquellenhändler können auch Teillieferungen zur Unterstützung von Rückständen oder Bilanzbeständen durchführen, wenn Bestellungen für beliebte Artikel eingehen.

### Recommendations- und Quellauswahlalgorithmus

Die [Quellauswahlalgorithmus](selection-reservations.md) (SSA) enthält Empfehlungen für die Teillieferung und den vollständigen Versand. Sie können bei der Erstellung von Versandrechnungen für eine Bestellung auf die Quellauswahlalgorithmen zugreifen. Führen Sie auf der Schiffsseite jederzeit den Algorithmus Quellpriorität oder Entfernungspriorität aus, um die besten Optionen für übereinstimmende geordnete Mengen und verfügbare Quellen zu bestimmen. Das System unterstützt den Versand einer kompletten Bestellung aus einer Quelle und die Unterteilung der Bestellung in mehrere Teillieferungen aus mehreren Quellen. Sie können auf diese Optionen für die sofortige Erfüllung und gestaffelte Sendungen zugreifen, um kleinere Mengen im Laufe der Zeit zu senden.

Um eine Bestellung abzuschließen und zu versenden, muss die Zahlung abgeschlossen und in Rechnung gestellt worden sein. Zurzeit können Sie die SSA für Empfehlungen und Sendungen aus einer oder mehreren Quellen erneut ausführen oder die SSA-Empfehlungen mit manuell festgelegten Quellen und Mengen überschreiben, um den Versand durchzuführen.

- Es wird empfohlen, die SSA erneut auszuführen, um Empfehlungen für jede Sendung zu überprüfen.

- Wenn Sie die Auswahl ändern möchten, können Sie die manuellen Quellabzüge überschreiben.

### Versand und Reservierung

Bei der Erzeugung der Sendungen werden die Vorbehalte für die Erzeugnisse abgezogen und die Erzeugnismenge abgezogen. Die Vor-Ort-Menge pro Lager aktualisiert auf der Grundlage der Versanddetails. Wenn Sie beispielsweise Sendungen für zehn Produkte aus zwei Quellen durchführen, werden von den Mengen für diese Quellen jeweils 10 abgezogen. Die Salable Quantity wird automatisch für verbundene Lagerbestände aktualisiert und stellt Kunden und Mitarbeitern die neuesten Produktmengen zur Verfügung. Und die Vorbehalte sind völlig klar, nicht mehr gegen die verkaufte Menge.
