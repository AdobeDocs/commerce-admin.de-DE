---
title: Bestellstatus und Reservierungen
description: Erfahren Sie mehr über automatische Reservierungseinträge oder Änderungen, die die Verkaufsmenge für ein Lager (oder einen Verkaufskanal) und die Lagerbestandsmenge pro Quelle aktualisieren.
exl-id: d264cb49-5aa8-4949-ae87-5efcd463d38c
feature: Inventory, Orders, Shipping/Delivery
source-git-commit: 7384481d1a4a2a04882d4c99448cca75abc9be31
workflow-type: tm+mt
source-wordcount: '1123'
ht-degree: 0%

---

# Bestellstatus und Reservierungen

[!DNL Inventory Management] unterstützt Teil- und Vollfakturierung, Zahlungen, Versand und Stornierungen pro Bestellung. Wenn Sie einen Auftrag durch Verarbeitung, Fakturierung, Versand und ggf. Rückerstattungen verwalten, gibt [!DNL Commerce] automatisch Reservierungen ein oder ändert diese, um die Verkaufsmenge für einen Lagerbestand (oder Verkaufskanal) und die Lagerbestandsmenge pro Quelle zu aktualisieren. Sie müssen nicht aktiv auf Reservierungen zugreifen oder diese eingeben. Wenn Sie Aktionen ausführen, um eine Bestellung zu erfüllen, zu stornieren oder zurückzuerstatten, erledigt dies das für Sie.

Diese Reservierungen passen immer Ihre verkaufbare Menge an, mit positiven oder negativen Mengen, um die Mengen zu erhöhen oder zu verringern. Das Ergebnis ist eine Aktualisierung Ihres Lagerbestands und Ihrer Verkaufsmengen für eine aktuelle Produktverfügbarkeit.

Einzelheiten zu Bestellungen und Lieferungen finden Sie unter [Verwalten von Bestellungen und Lieferungen](shipments.md).

## Optionen für die Bestellverwaltung

Je nach Lagerstatus und Kundenanfragen können Sie Bestellungen mit Teilzahlungen und Stornierungen, Teillieferungen aus mehreren Quellen oder für Rückstände oder Gutschriften aktualisieren, um zurückgegebene Produkte zurückzuerstatten.

### Sendungen

Senden Sie nach der Rechnungsstellung Teilsendungen oder Vollsendungen, bis Sie die gesamte Bestellung abgeschlossen haben. Jede Lieferung rechnet eine Reservierung um und zieht den Betrag von der Produktmenge pro Quelle ab. Reservierungsvergütungen eingeben, um die Verkaufsmenge für Ihren Bestand zu aktualisieren. Wenn Sie Teilsendungen durchführen, wird dieser Betrag bei jeder Lieferung von der Produktmenge und den Reservierungen abgezogen. Alle nicht versandten Produktreservierungen bleiben bis zum Versand in Kraft, sodass Ihr Verkaufsbetrag aktuell ist und Sie die Kontrolle über den Produktbestand haben und mehrere Quelllieferungen und Rückbestellungen unterstützen können.

### Stornierte Bestellungen

Wenn ein Kunde seine Bestellung vor dem Versand (teilweise oder vollständig) storniert, wird eine neue Reservierung eingegeben, um den Lagerbetrag auf die verkaufbare Menge zurückzugeben. Die Reservierungen heben sich gegenseitig auf, ohne die Menge von irgendwelchen Quellen abzuziehen. Andere Kunden können diese Produktmengen aktiv über die zugehörigen Lager und Vertriebskanäle erwerben.

### Rückerstattete Bestellungen

Wenn ein Kunde eine Rückerstattung beantragt, stellen Sie die Gutschrift für die Teil- oder vollständigen Produktbeträge aus. Wenn Sie die zurückgegebenen Produkte erhalten, geben Sie eine Gutschrift ein, um die Mittel bereitzustellen und die Produktbeträge zu aktualisieren. Bei Auswahl der Option „Lagerrückgabe“ fügt [!DNL Commerce] den Produkten und Quellen, die die Bestellungen und Reservierungskompensationen versendet haben, wieder Mengen hinzu, um die Verkaufsmengen für den zugehörigen Bestand zu aktualisieren.

## Auftragstypen

Einfache Bestellungen beginnen mit einem Warenkorb, setzen die Zahlung fort und enden mit einem zufriedenen Versand. Bei diesen Bestellungen verarbeitet [!DNL Inventory Management] Reservierungen einfach gegen die Verfügbarkeit (oder verkäufliche Menge) im Warenkorb und Checkout und zieht sie vom Lagerbestand beim Versand ab.

![Prozess für eine einfache Bestellung](assets/diagram-simple-order-flow.png){width="600" zoomable="yes"}

Eine kompliziertere Bestellung kann Teilstornierungen, Teillieferungen und Rückerstattungen zur Folge haben. In diesen Situationen wirken sich Reservierungen auf das verfügbare Inventar aus, um Mengen für Stornierungen und Rückerstattungen hinzuzufügen und Mengen bei Bestellungen und Versand zu reduzieren.

![Prozess für eine komplizierte Bestellung](assets/diagram-complicated-order-flow.png){width="600" zoomable="yes"}

Verfügbarkeitsreservierungen und Bestandsänderungen erfolgen je nach Bestellstatus.

## Status und Reservierungen

In den folgenden Tabellen sind die Bestell- und Gutschriftenstatus mit den von [!DNL Commerce] eingegebenen Reservierungsänderungen zur Verwaltung Ihres Bestands aufgeführt.

| Bestellstatus | Beschreibung | Reservierung für verkaufsfähige Menge |
|--|--|--|
| [!UICONTROL Open] | Neu und kürzlich eingereicht, keine Verarbeitung | Die Reservierung wird gespeichert, wenn die Bestellung für das Lager eingereicht wird. |
| [!UICONTROL Canceled] | Teilweise oder vollständig vor Zahlung storniert | Eine Reservierungskompensation wird eingegeben, um die Teil- oder Vollmenge an die verkaufbare Lagermenge zurückzugeben. |
| [!UICONTROL On Hold] | Zahlung und Versand nicht bearbeitet oder in Rechnung gestellt | Die Reservierung bleibt bestehen. |
| [!UICONTROL Suspected Fraud] | Nicht verarbeitet aufgrund von Betrug | Wenn genehmigt oder überprüft, bleibt die Reservierung bestehen.<br/>Wenn abgelehnt, bleibt die Reservierung in Kraft, bis der Händler entscheidet, zu genehmigen oder zu stornieren.<br/>Bei Stornierung wird die Reservierungskompensation eingegeben, um die gesamte Menge an die verkaufsfähige Lagermenge zurückzugeben. |
| [!UICONTROL Pending] | Warten auf Zahlung | Die Reservierung bleibt bestehen. |
| [!UICONTROL Processing] | Zahlungsabwicklung, nicht eingegangen | Die Reservierung bleibt bestehen. |
| [!UICONTROL Pending Payment] | Zahlung nicht eingegangen | Die Reservierung bleibt bestehen. |
| [!UICONTROL Payment Review] | Zahlung wird zur Bearbeitung und zum Abschluss überprüft | Die Reservierung bleibt bestehen. |
| [!UICONTROL Complete] | Bezahlt und vollständig versendet | Der Reservierungsbetrag wird bei der teilweisen oder vollständigen Fakturierung von der Produktmenge für die ausgewählte Quelle abgezogen. Die Reservierungskompensation wird eingegeben, um die gesamte verkaufsfähige Menge zu aktualisieren. |
| [!UICONTROL Closed] | Zurückerstattet oder archiviert | Bei einer Archivierung ändert sich die Menge nicht. Bei teilweiser oder vollständiger Rückerstattung wird die Reservierungskompensation eingegeben und umgerechnet, um die Produktmengen pro Quelle und die verkaufsfähige Menge pro Lager hinzuzufügen. |

| Status der Gutschrift | Beschreibung | Reservierung für verkaufsfähige Menge |
|--|--|--|
| [!UICONTROL Open] | Die Rückerstattung ist fällig, nicht abgeschlossen | Bei den Reservierungen ändert sich nichts. |
| [!UICONTROL Refunded] | Abgeschlossen, Mittel zurückgegeben | Bei teilweiser oder vollständiger Rückerstattung wird die Reservierungskompensation eingegeben und umgerechnet, um die Produktmengen pro Quelle und die verkaufsfähige Menge pro Lager hinzuzufügen. |

## Beispiel für eine komplexe Reihenfolge

Blake Sanders bestellt Fahrräder und Kleidung für ihren Familienurlaub und Spaß. Sie sehen einige große Umsätze in Ihrem Biking Adventures Store mit Beständen und Quellen in den Vereinigten Staaten, Kanada und Europa.

Sie kaufen zwei tolle Park-Bikes für ihre kleinen Kinder, ein BMX-Bike für ihren Teenager, ein schönes Mountainbike für sich und ein modernes deutsches Langlaufrad für ihren Ehepartner. Der Laden hatte einen Verkauf von niedlichen Hemden, so kauften sie etwas für die ganze Familie zusammen. Unten finden Sie die Liste der Urlaubskäufe, die passenden SKUs und die eingegebenen Reservierungen für die verkaufsfähigen Lagermengen.

![Komplexe Reihenfolge](assets/diagram-order-complex.png){width="600" zoomable="yes"}

Sie zeigen ihrer Familie, was sie gefunden haben, nehmen aber einige Änderungen vor. Vor Abschluss der Zahlung stornieren sie zwei der 33-BikeFun-SKUs (Kinder mochten sie nicht). Dies ist eine teilweise Stornierung aufgrund ausstehender Zahlung, sodass keine Gutschrift erforderlich ist. Zur Aktualisierung addiert [!DNL Commerce] wieder zum verkaufbaren Lagerbestand für Kanada. Die Bestellung wird bezahlt, und alle Produkte werden versendet, rechtzeitig für den Urlaub ankommen. [!DNL Commerce] aktualisiert die verkaufbare Menge und die Quellmengen für die Versandlager für die gelieferten Produkte.

Aber das Hemd passte nicht ganz zu ihrem Ehepartner. Blake fordert eine Rückerstattung und schickt sein Hemd zurück. Die Erstellung der Gutschrift fügt ein 54-BikeLife-Shirt zurück zum Lager und Versandlager in Kanada.

- **Ausgelieferte Produkte** - Bei gekauften und ausgelieferten Produkten aktualisiert [!DNL Commerce] den Bestand. Reservierungsvergütungen werden in Abzüge der Lagerbestandsmenge aus der gelieferten Quelle umgerechnet. Die verfügbare Verkaufsmenge wird für den Bestand aktualisiert.

- **Stornierte Produkte** - Durch Stornierung des Lagers entfernt [!DNL Commerce] die Reservierung für dieses Produkt. Die Reservierungsentschädigung wird auf der Lagerebene eingegeben, um die verkaufsfähigen Mengen für die teilweise Stornierung von zwei Hemden hinzuzufügen. Dies wirkt sich nicht auf die Lagermenge auf der Quellenebene aus.

- **Gutschrift/Rückerstattetes Produkt** - Durch Rücksendung von Vorräten muss es zu den Mengen zurückaddiert werden. Bei der Ausstellung der Gutschrift können Sie wählen, ob Sie zu den Lagerbeständen zurückkehren möchten. [!DNL Commerce] fügt die Lagermenge zur gelieferten Quelle für das Produkt zurück. Buchungs-Ausgleichszahlungen werden eingegeben, um alle verbleibenden Reservierungen zu löschen. Die verkaufsfähige Menge wird anhand der aktualisierten Menge neu berechnet.

![Aktualisierungen der Rückerstattungsmenge bestellen](assets/diagram-order-refund.png){width="600" zoomable="yes"}
