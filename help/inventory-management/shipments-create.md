---
title: Erstellen von Sendungen aus mehreren Quellen
description: Erfahren Sie, wie Händler mit mehreren Quellen Sendungen erstellen und versenden können.
exl-id: d2995139-0fc3-4379-a4ec-b0d38ed566bb
feature: Inventory, Shipping/Delivery
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# Erstellen von Sendungen aus mehreren Quellen

Mit [!DNL Inventory Management] senden Sie eine oder mehrere Sendungen, wie Sie über Inventar verfügen. Um bei Bedarf weitere Sendungen zu erstellen, wiederholen Sie diese Anweisungen unter Verwendung empfohlener oder manuell eingegebener Mengen und Quellen. In diesen Anweisungen wird beschrieben, wie Händler mit mehreren Quellen Sendungen senden. Einzelquell-Händler senden Sendungen ohne diese zusätzlichen Schritte (siehe [Erstellen einer Sendung](../stores-purchase/shipments.md#create-a-shipment){target="_blank"} im Benutzerhandbuch zu Kernaufgaben).

Verwenden Sie beim Erstellen von Sendungen den Source-Auswahlalgorithmus für berechnete Empfehlungen. Befolgen Sie diese Empfehlungen und verwenden Sie sie oder legen Sie die Beträge pro Quelle fest, indem Sie benutzerdefinierte Sendungen generieren. Sie kontrollieren Ihren ausgehenden Bestand für jede Bestellung, legen die abzugsfähigen Mengen fest, senden einen oder mehrere Sendungen und liefern Lagerbestände und Rückstände, da Bestand verfügbar ist. Geben Sie für jeden Zeileneintrag in der Reihenfolge einen Abzugsbetrag von der Quellmenge an.

Sie können Teilsendungen an folgende Empfänger senden:

- Aufstockung bei Bestandsaufnahme

- Bestandsabzüge über Quellen hinweg

Bei der Verschiffung werden die von Ihnen eingenommenen Lagerbestandsmengen abgesetzt. In der Tat konvertieren Reservierungen in tatsächliche Mengenabzüge.

## Erstellen einer Sendung

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Suchen Sie die Reihenfolge und öffnen Sie sie im Ansichtsmodus.

1. Wenn die Bestellung bezahlt und in Rechnung gestellt wird und versandbereit ist, klicken Sie auf **[!UICONTROL Ship]**.

1. Führen Sie die Source-Auswahl für den Versand von Produkten pro Quelle aus:

   - Um Empfehlungen zum Versand anzuzeigen, klicken Sie auf **[!UICONTROL Source Selection Algorithm]** und wählen Sie einen Algorithmus aus.

     | Algorithmus | Beschreibung |
     |--|--|
     | [Source-Priorität](source-priority-algorithm.md) | Empfiehlt Sendungen aus Quellen entsprechend den Bestellungen der dem Lager zugewiesenen Quellen. |
     | [Distance Priority](distance-priority-algorithm.md) | Empfiehlt Sendungen aus Quellen, die der Lieferadresse am nächsten sind, auf der Grundlage der physischen Entfernung oder der kürzesten Lieferzeit. |

     >[!IMPORTANT]
     >
     >Wenn der Distance Priority-Algorithmus für Versand verwendet wird und Routen und Daten für den ausgewählten [Berechnungsmodus](distance-priority-algorithm.md) (Fahren, Fahren, Fahren oder Gehen) für eine Sendung nicht zurückgegeben werden, wird der SSA-Standardwert für die Source-Priorität verwendet. Es wird empfohlen, auch die [Priorität für Quellen pro Lager](stocks-prioritize-sources.md) festzulegen.


   - Wählen Sie für **[!UICONTROL Select a Source to Ship from]** eine Quelle aus, an die eine Sendung gesendet werden soll.

   - Behalten Sie für jeden Zeileneintrag den empfohlenen Betrag bei oder geben Sie einen bestimmten Betrag in den Wert **[!UICONTROL Qty to Deduct]** ein. Dieser Wert gibt den Betrag an, der vom Bestand der ausgewählten Quelle abgezogen wird.

   - Klicken Sie auf **[!UICONTROL Proceed to Shipment]**.

     ![Wählen Sie eine Source aus und geben Sie eine Menge ein](assets/shipment-adobe-shipping-sources.png){width="350" zoomable="yes"}

1. Überprüfen Sie die Seite _[!UICONTROL New Shipment]_und geben Sie bei Bedarf weitere Änderungen ein.

   Im Abschnitt &quot;_[!UICONTROL Inventory]_&quot; werden die Quelle, der Versand von Produkten, die bestellte Gesamtmenge und die zu versendende Menge angezeigt.

   ![Inventardetails für die Lieferung, z. B. Teillieferung](assets/inventory-shipment-details.png){width="350" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Submit Shipment]** , um abzuschließen.
