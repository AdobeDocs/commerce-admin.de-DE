---
title: Sendungen aus mehreren Quellen erstellen
description: Erfahren Sie, wie Händler mit mehreren Quellen Sendungen erstellen und senden können.
exl-id: d2995139-0fc3-4379-a4ec-b0d38ed566bb
feature: Inventory, Shipping/Delivery
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# Sendungen aus mehreren Quellen erstellen

Senden Sie mit [!DNL Inventory Management] eine oder mehrere Lieferungen, sobald Sie über Lagerbestand verfügen. Um bei Bedarf zusätzliche Lieferungen zu erzeugen, wiederholen Sie diese Anweisungen mit empfohlenen oder manuell eingegebenen Mengen und Quellen. Diese Anweisungen beschreiben, wie Händler aus mehreren Quellen Sendungen durchführen. Händler aus einer Hand versenden Sendungen ohne diese zusätzlichen Schritte (siehe [Sendung erstellen](../stores-purchase/shipments.md#create-a-shipment){target="_blank"} im Benutzerhandbuch zu Core).

Verwenden Sie beim Erstellen von Sendungen den Source-Auswahlalgorithmus für berechnete Empfehlungen. Befolgen und verwenden Sie diese Empfehlungen oder legen Sie die Beträge pro Quelle fest, um benutzerdefinierte Sendungen zu generieren. Sie steuern Ihren ausgehenden Bestand für jede Bestellung, legen die abzuziehenden Beträge fest, versenden eine oder mehrere Lieferungen und liefern Lagerbestände und Nachbestellungen, sobald der Bestand verfügbar ist. Geben Sie für jeden Einzelposten im Auftrag einen Betrag ein, der von der Bezugsmenge abgezogen werden soll.

Sie können Teilsendungen an folgende Adressen senden:

- Auftragsrückstände beim Eintreffen des Inventars erfüllen

- Saldo der Lagerabzüge über Quellen hinweg

Wenn Sie Lieferungen eingeben, werden die eingegebenen Beträge von den Lagerbestandsmengen abgezogen. Buchungen werden in tatsächliche Mengenabzüge umgewandelt.

## Erstellen einer Sendung

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Suchen Sie die Bestellung und öffnen Sie sie im Ansichtsmodus.

1. Wenn die Bestellung bezahlt und fakturiert wurde und versandbereit ist, klicken Sie auf **[!UICONTROL Ship]**.

1. Schließen Sie die Source-Auswahl für den Versand von Produkten pro Quelle ab:

   - Um Versandempfehlungen anzuzeigen, klicken Sie auf **[!UICONTROL Source Selection Algorithm]** und wählen Sie einen Algorithmus aus.

     | Algorithmus | Beschreibung |
     |--|--|
     | [Source-Priorität](source-priority-algorithm.md) | empfiehlt Lieferungen aus Quellen entsprechend den Bestellungen der dem Lager zugeordneten Quellen. |
     | [Priorität der Entfernung](distance-priority-algorithm.md) | empfiehlt Sendungen aus Quellen, die der Versandadresse am nächsten liegen, basierend auf der physischen Entfernung oder der kürzesten Lieferzeit. |

     >[!IMPORTANT]
     >
     >Wenn Sie den Distance Priority-Algorithmus für Versand und Routen verwenden und die Daten für den ausgewählten [Berechnungsmodus) (](distance-priority-algorithm.md), Fahrradfahren oder Gehen) für eine Sendung nicht zurückgegeben werden, verwendet die SSA standardmäßig die Source-Priorität. Es wird empfohlen, auch die [Priorität für Quellen pro Lager) ](stocks-prioritize-sources.md).


   - Wählen Sie **[!UICONTROL Select a Source to Ship from]** eine Quelle aus, um eine Sendung zu versenden.

   - Behalten Sie für jeden Zeileneintrag den empfohlenen Betrag bei oder geben Sie einen bestimmten Betrag in die **[!UICONTROL Qty to Deduct]** ein. Dieser Wert gibt den Betrag an, der vom Bestand der ausgewählten Quelle abgezogen wird.

   - Klicken Sie auf **[!UICONTROL Proceed to Shipment]**.

     ![Wählen Sie eine Source aus und geben Sie eine Menge ein](assets/shipment-adobe-shipping-sources.png){width="350" zoomable="yes"}

1. Überprüfen Sie die _[!UICONTROL New Shipment]_Seite und geben Sie bei Bedarf zusätzliche Änderungen ein.

   Im Abschnitt _[!UICONTROL Inventory]_werden die Herkunft, die Lieferprodukte, die bestellte Gesamtmenge und die zu versendende Menge angezeigt.

   ![Lagerdetails für die Lieferung, z. B. Teillieferung](assets/inventory-shipment-details.png){width="350" zoomable="yes"}

1. Klicken Sie zum Abschluss auf **[!UICONTROL Submit Shipment]** .
