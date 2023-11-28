---
title: "Konfigurieren [!DNL Inventory Management] globale Optionen"
description: Erfahren Sie, wie Sie den Standard konfigurieren [!DNL Inventory Management] Konfigurationsoptionen für Produkte und Lager für Ihre Websites.
exl-id: 1a8c9605-ae61-4d45-b549-64911b329203
feature: Inventory, Configuration
source-git-commit: 7384481d1a4a2a04882d4c99448cca75abc9be31
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 0%

---

# Konfigurieren [!DNL Inventory Management] globale Optionen

Konfigurieren Sie die standardmäßigen Konfigurationsoptionen für Produkt und Lager für Ihre Websites. Einige dieser Einstellungen können pro Produkt durch überschrieben werden [Konfigurieren von Produktoptionen](product-options.md). Informationen zum Konfigurieren der Einstellungen für die Distance Priority finden Sie unter [Konfigurieren des Distance Priority-Algorithmus](distance-priority-algorithm.md).

## Globale Produkt- und Lageroptionen konfigurieren

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Catalog]** und wählen **[!UICONTROL Inventory]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Stock Options]** und legen Sie die Optionen fest:

   ![Lageroptionen](assets/config-catalog-inventory-stock-options.png){width="600" zoomable="yes"}

   - Um die bei der Bestellung verfügbare Menge anzupassen, legen Sie **[!UICONTROL Decrease Stock When Order is Placed]** nach `Yes`.

   - So geben Sie Artikel wieder auf Lager, wenn eine Bestellung storniert wird: **[!UICONTROL Set Items' Status to be in Stock When Order in Cancelled]** nach `Yes`.

   - Um weiterhin nicht mehr vorrätige Produkte im Katalog anzuzeigen, legen Sie **[!UICONTROL Display Out of Stock Products]** nach `Yes`.

   - Wenn [Preisausschreibungen](alert-setup.md) aktiviert sind, können sich Kunden für eine Benachrichtigung anmelden, wenn das Produkt wieder vorrätig ist.

   - Um den Beginn für die Anzeige des letzten verbleibenden Lagerbestands auf der Produktseite festzulegen, geben Sie einen Betrag für **[!UICONTROL Only X left Threshold]**.

     Die Meldung wird angezeigt, wenn die Lagermenge die Schwelle erreicht. Wenn beispielsweise auf `3`, die Nachricht `Only 3 left` erscheint, wenn die Lagermenge drei erreicht. Die Nachricht passt sich an die Lagermenge an, bis die Menge null erreicht.

   - Um eine Meldung &quot;Auf Lager&quot;oder &quot;Nicht auf Lager&quot;auf der Produktseite anzuzeigen, legen Sie **[!UICONTROL Display Products Availability In Stock on Storefront]** nach `Yes`.

   - Um den Bestand beim Laden eines Produkts in den Warenkorb zu überprüfen, legen Sie **[!UICONTROL Enable Inventory Check On Cart Load]** nach `Yes`. Wenn diese Option deaktiviert ist, wird die Bestandsüberprüfung übersprungen. Durch Deaktivieren dieser Option wird der Checkout beschleunigt, insbesondere wenn viele Artikel im Warenkorb sind. Wenn Sie die Vorab-Validierung jedoch überspringen, könnten Kunden später im Checkout-Prozess Fehler wegen &quot;Nicht vorrätig&quot;sehen.

   - Um die Konsistenz zwischen Bestand und Katalog zu gewährleisten, legen Sie **[!UICONTROL Synchronize with Catalog]** nach `Yes`. Wenn diese Option aktiviert ist, werden die Bestandsdaten entsprechend den Katalogänderungen angepasst (z. B. entferntes Produkt, geänderte Produkt-SKU und geänderter Produkttyp).

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Product Stock Options]** und legen Sie die Optionen fest:

   - So aktivieren [Bestandskontrolle](enable.md) für Ihren Katalog festlegen **[!UICONTROL Manage Stock]** nach `Yes`.

     ![Optionen für Produktspeicher](assets/config-catalog-inventory-product-stock-options.png){width="600" zoomable="yes"}

   - Satz **[!UICONTROL Backorders]** auf einen der folgenden Werte zu:

     | Option | Beschreibung |
     | ----- | ----- |
     | `No Backorders` | [Rückstände](backorders.md) nicht akzeptiert werden, wenn das Produkt nicht vorrätig ist. |
     | `Allow Qty Below 0` | Rückaufträge werden akzeptiert, wenn die Menge unter null fällt. |
     | `Allow Qty Below 0 and Notify Customer` | Rückaufträge werden akzeptiert, wenn die Menge unter null fällt, und das System informiert den Kunden darüber, dass die Bestellung noch aufgegeben werden kann. |

   - Geben Sie die **[!UICONTROL Maximum Qty Allowed in Shopping Cart]**.

   - Geben Sie einen Betrag für die **[!UICONTROL Out-of-Stock Threshold]**:

     | Wert | Beschreibung |
     | ----- |-----|
     | Positiver Betrag | Geben Sie bei deaktivierten Rückgaben einen positiven Betrag ein. |
     | Null | Wenn Rückstände aktiviert sind, geben Sie `0` ermöglicht unendliche Rückläufe. |
     | Negativer Betrag | Wenn Rückaufträge aktiviert sind, wird empfohlen, einen negativen Betrag einzugeben. Der Betrag wird der Verkaufsmenge hinzugefügt. Geben Sie beispielsweise `-50` um Bestellungen bis zu diesem Betrag zuzulassen. |

   - Geben Sie die **[!UICONTROL Minimum Qty Allowed in Shopping Cart]** für die ausgewählte Gruppe und Beträge.

   - Für **[!UICONTROL Notify for Quantity Below]**, geben Sie die Lagerbestände an, die Trigger über die Nichtverfügbarkeit des Artikels informieren.

   - Um Mengenerhöhungen für das Produkt zu aktivieren, legen Sie **[!UICONTROL Enable Qty Increments]** nach `Yes`. Anschließend gilt für **[!UICONTROL Qty Increments]** Geben Sie die Anzahl der Artikel ein, die gekauft werden müssen, um die Anforderungen zu erfüllen.

     Ein Artikel, der in sechs Schritten verkauft wird, kann beispielsweise in folgenden Mengen gekauft werden: `6`, `12`, `18`usw.

   - Für [!DNL Inventory Management], **[!UICONTROL Automatically Return Credit Memo Item to Stock]** auf `No`. Wenn Sie ein Kreditmemo senden, geben Sie ein und wählen Sie aus, um eine Lagerposition an die Quellen zurückzugeben.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Admin bulk operations]** und legen Sie die Optionen fest:

   ![Massenvorgänge für Administratoren](assets/config-catalog-inventory-admin-bulk-operations.png){width="600" zoomable="yes"}

   - Satz **[!UICONTROL Run asynchronously]** asynchron Ausführen von Massenvorgängen für Massenproduktaktionen

     Diese Vorgänge umfassen Bulk-Vorgänge [Zuweisen und Aufheben der Zuweisung von Quellen](bulk-assignment.md), und [Bestandsübertragung an Quelle](inventory-transfer.md). Sie erfasst Massenaktionen bis zur asynchronen Batch-Größe und führt diese Aktionen dann aus. Diese Option ist standardmäßig deaktiviert. Es wird empfohlen, die Leistung mit Massenaktionen zu überprüfen, bevor die Aktivierung erfolgt.

     >[!NOTE]
     >
     >So konfigurieren und unterstützen Sie _Asynchrone Warteschlangenmanager_, müssen Sie einen Befehl über die Befehlszeile ausgeben. Dieser Schritt erfordert möglicherweise Hilfe von Entwicklern. Siehe [Starten von Nachrichtenwarteschlangen-Verbrauchern](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/start-message-queues.html) im _Konfigurationshandbuch_.

   - Wenn diese Option aktiviert ist, legen Sie die **[!UICONTROL Asynchronous batch size]**. Die standardmäßige Batch-Größe ist 100. Wenn Massenprozesse diesen Wert erreichen, wird dieser vom System Trigger.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Save Config]**.
