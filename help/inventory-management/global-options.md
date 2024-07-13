---
title: "Configure [!DNL Inventory Management] global options"
description: Erfahren Sie, wie Sie die standardmäßigen [!DNL Inventory Management] Konfigurationsoptionen für Produkte und Lager für Ihre Websites konfigurieren.
exl-id: 1a8c9605-ae61-4d45-b549-64911b329203
feature: Inventory, Configuration
source-git-commit: 7384481d1a4a2a04882d4c99448cca75abc9be31
workflow-type: tm+mt
source-wordcount: '639'
ht-degree: 0%

---

# Globale Optionen für [!DNL Inventory Management] konfigurieren

Konfigurieren Sie die standardmäßigen Konfigurationsoptionen für Produkt und Lager für Ihre Websites. Einige dieser Einstellungen können pro Produkt durch [Konfigurieren der Produktoptionen](product-options.md) überschrieben werden. Informationen zum Konfigurieren der Einstellungen für die Distance Priority finden Sie unter [Konfigurieren des Distance Priority Algorithm](distance-priority-algorithm.md).

## Globale Produkt- und Lageroptionen konfigurieren

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Catalog]** und wählen Sie **[!UICONTROL Inventory]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Stock Options]** und legen Sie die Optionen fest:

   ![Stock Options](assets/config-catalog-inventory-stock-options.png){width="600" zoomable="yes"}

   - Um die verfügbare Menge bei einer Bestellung anzupassen, setzen Sie **[!UICONTROL Decrease Stock When Order is Placed]** auf `Yes`.

   - Um Elemente auf Lager zurückzugeben, wenn eine Bestellung storniert wird, **[!UICONTROL Set Items' Status to be in Stock When Order in Cancelled]** auf `Yes`.

   - Um weiterhin Produkte im Katalog anzuzeigen, die nicht mehr auf Lager sind, setzen Sie **[!UICONTROL Display Out of Stock Products]** auf `Yes`.

   - Wenn [Preiswarnungen](alert-setup.md) aktiviert sind, können sich Kunden für eine Benachrichtigung anmelden, wenn das Produkt wieder auf Lager ist.

   - Um den Beginn für die Anzeige des letzten verbleibenden Lagerbestands auf der Produktseite festzulegen, geben Sie einen Betrag für **[!UICONTROL Only X left Threshold]** ein.

     Die Meldung wird angezeigt, wenn die Lagermenge die Schwelle erreicht. Wenn Sie beispielsweise auf `3` setzen, wird die Meldung `Only 3 left` angezeigt, wenn die Menge auf Lager drei erreicht. Die Nachricht passt sich an die Lagermenge an, bis die Menge null erreicht.

   - Um eine Meldung &quot;Auf Lager&quot;oder &quot;Nicht auf Lager&quot;auf der Produktseite anzuzeigen, setzen Sie **[!UICONTROL Display Products Availability In Stock on Storefront]** auf `Yes`.

   - Um den Bestand beim Laden eines Produkts in den Warenkorb zu überprüfen, setzen Sie **[!UICONTROL Enable Inventory Check On Cart Load]** auf `Yes`. Wenn diese Option deaktiviert ist, wird die Bestandsüberprüfung übersprungen. Durch Deaktivieren dieser Option wird der Checkout beschleunigt, insbesondere wenn viele Artikel im Warenkorb sind. Wenn Sie die Vorab-Validierung jedoch überspringen, könnten Kunden später im Checkout-Prozess Fehler wegen &quot;Nicht vorrätig&quot;sehen.

   - Um die Konsistenz zwischen Bestand und Katalog zu wahren, setzen Sie **[!UICONTROL Synchronize with Catalog]** auf `Yes`. Wenn diese Option aktiviert ist, werden die Bestandsdaten entsprechend den Katalogänderungen angepasst (z. B. entferntes Produkt, geänderte Produkt-SKU und geänderter Produkttyp).

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Product Stock Options]** und legen Sie die Optionen fest:

   - Um die [Bestandskontrolle](enable.md) für Ihren Katalog zu aktivieren, setzen Sie **[!UICONTROL Manage Stock]** auf `Yes`.

     ![Optionen für Produktspeicher](assets/config-catalog-inventory-product-stock-options.png){width="600" zoomable="yes"}

   - Setzen Sie **[!UICONTROL Backorders]** auf einen der folgenden Werte:

     | Option | Beschreibung |
     | ----- | ----- |
     | `No Backorders` | [Rückstellungen](backorders.md) werden nicht akzeptiert, wenn das Produkt nicht vorrätig ist. |
     | `Allow Qty Below 0` | Rückaufträge werden akzeptiert, wenn die Menge unter null fällt. |
     | `Allow Qty Below 0 and Notify Customer` | Rückaufträge werden akzeptiert, wenn die Menge unter null fällt, und das System informiert den Kunden darüber, dass die Bestellung noch aufgegeben werden kann. |

   - Geben Sie den Wert **[!UICONTROL Maximum Qty Allowed in Shopping Cart]** ein.

   - Geben Sie einen Betrag für den Wert **[!UICONTROL Out-of-Stock Threshold]** ein:

     | Wert | Beschreibung |
     | ----- |-----|
     | Positiver Betrag | Geben Sie bei deaktivierten Rückgaben einen positiven Betrag ein. |
     | Null | Wenn Rückorder aktiviert sind, ermöglicht die Eingabe von `0` unendliche Rückstände. |
     | Negativer Betrag | Wenn Rückaufträge aktiviert sind, wird empfohlen, einen negativen Betrag einzugeben. Der Betrag wird der Verkaufsmenge hinzugefügt. Geben Sie beispielsweise `-50` ein, um Bestellungen bis zu diesem Betrag zuzulassen. |

   - Geben Sie den Wert **[!UICONTROL Minimum Qty Allowed in Shopping Cart]** für die ausgewählte Gruppe und die Beträge ein.

   - Geben Sie für &quot;**[!UICONTROL Notify for Quantity Below]**&quot;die Lagerposition an, die der Trigger angibt, dass der Artikel nicht mehr vorrätig ist.

   - Um Mengeninkremente für das Produkt zu aktivieren, setzen Sie **[!UICONTROL Enable Qty Increments]** auf `Yes`. Geben Sie dann für &quot;**[!UICONTROL Qty Increments]**&quot;die Anzahl der Artikel ein, die gekauft werden müssen, um die Anforderung zu erfüllen.

     Beispielsweise kann ein Artikel, der in sechs Schritten verkauft wird, in Mengen von `6`, `12`, `18` usw. gekauft werden.

   - Für [!DNL Inventory Management] ist **[!UICONTROL Automatically Return Credit Memo Item to Stock]** auf `No` gesetzt. Wenn Sie ein Kreditmemo senden, geben Sie ein und wählen Sie aus, um eine Lagerposition an die Quellen zurückzugeben.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Admin bulk operations]** und legen Sie die Optionen fest:

   ![Massenvorgänge für Administratoren](assets/config-catalog-inventory-admin-bulk-operations.png){width="600" zoomable="yes"}

   - Legen Sie **[!UICONTROL Run asynchronously]** fest, um Massenvorgänge für Massenproduktaktionen asynchron auszuführen.

     Zu diesen Vorgängen gehören die Massenzuweisung von [ und die Aufhebung der Zuweisung von Quellen](bulk-assignment.md) sowie die [Übertragung von Beständen an die Quelle](inventory-transfer.md). Sie erfasst Massenaktionen bis zur asynchronen Batch-Größe und führt diese Aktionen dann aus. Diese Option ist standardmäßig deaktiviert. Es wird empfohlen, die Leistung mit Massenaktionen zu überprüfen, bevor die Aktivierung erfolgt.

     >[!NOTE]
     >
     >Um _asynchrone Warteschlangenmanager_ zu konfigurieren und zu unterstützen, müssen Sie einen Befehl über die Befehlszeile ausgeben. Dieser Schritt erfordert möglicherweise Hilfe von Entwicklern. Siehe [Starten von Verbrauchern in der Nachrichtenwarteschlange](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/start-message-queues.html) im _Konfigurationshandbuch_.

   - Wenn diese Option aktiviert ist, legen Sie den Wert **[!UICONTROL Asynchronous batch size]** fest. Die standardmäßige Batch-Größe ist 100. Wenn Massenprozesse diesen Wert erreichen, wird dieser vom System Trigger.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save Config]**.
