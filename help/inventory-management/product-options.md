---
title: "Konfigurieren [!DNL Inventory Management] Produktoptionen"
description: Erfahren Sie, wie Sie die [!DNL Inventory Management] Produktkonfigurationsoptionen.
exl-id: b5cff7d2-5197-4362-9503-b07c80793ac7
feature: Inventory, Products
source-git-commit: ccd93a54b6fa23a7a54fb423f8232c72cd8fe027
workflow-type: tm+mt
source-wordcount: '859'
ht-degree: 0%

---

# Konfigurieren [!DNL Inventory Management] Produktoptionen

Diese Konfigurationen gelten nur für das bearbeitete Produkt, wobei alle Konfigurationen auf globaler Website-Ebene außer Kraft gesetzt werden. Ändern Sie diese Einstellungen beim Bearbeiten eines Produkts über die _[!UICONTROL Sources]_und_[!UICONTROL Advanced Inventory]_ Seite.

- Konfigurieren von Produktoptionen nach Quelle
- Konfigurieren von Produktoptionen für erweiterte Inventare

## Produktoptionen nach Quelle

Konfigurieren Sie die Mengen und zusätzlichen Einstellungen pro [hinzugefügte Quelle](sources-add.md) für das Produkt.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Öffnen Sie ein Produkt im Bearbeitungsmodus.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Sources]** und konfigurieren Sie die Produkteinstellungen für jede Quelle:

   - Geben Sie einen **[!UICONTROL Qty]** (Menge)

   - Legen Sie die **[!UICONTROL Source Item Status]** as `In Stock` oder `Out of Stock`.

   - Um die Meldung für die Menge unter pro Quelle zu ändern, deaktivieren oder wählen Sie die Option **[!UICONTROL Notify Quantity Use Default]** aktivieren.

     Geben Sie bei einer Bereinigung den Lagerbestand an, der Trigger der Meldung des Artikels ist. Der eingegebene Betrag wird von der veräußerbaren Menge des Artikels auf der Lagerebene abgezogen.

     `Select to use Default` - [!DNL Commerce] überprüft die erweiterten Lagerbestandsoptionen des Produkts auf Konfigurationseinstellungen.
     `Clear to Modify` - Geben Sie einen Wert für &quot;Menge benachrichtigen&quot;ein und überschreiben Sie die erweiterten Konfigurations- und Speichereinstellungen.

   ![Quellen für ein Produkt](assets/inventory-product-quantity-edit.png){width="350" zoomable="yes"}

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Done]**, dann **[!UICONTROL Save]**.

### Feldbeschreibungen

| Feld | Anwendungsbereich | Beschreibung |
|--|--|--|
| [!UICONTROL Source Code] | Global | Der eindeutige Code für eine [source](sources-manage.md). |
| [!UICONTROL Name] | Global | Der eindeutige Name einer Quelle. |
| [!UICONTROL Status] | Global | Das Produkt ist im Katalog aktiviert oder deaktiviert. |
| [!UICONTROL Source Item Status] | Global | Bestimmt die aktuelle Verfügbarkeit des Produkts. Optionen:<br />`In Stock` - Stellt das Produkt zum Kauf bereit.<br />`Out of Stock` - Sofern Rückstellungen nicht aktiviert sind, verhindert, dass das Produkt zum Kauf verfügbar ist, und entfernt die Liste aus dem Katalog. |
| [!UICONTROL Qty] | Global | Auf Lager befindliche Beträge für jede Quelle oder jeden Standort. |
| [!UICONTROL Notify Quantity] | Global | Ein Betrag für _[!UICONTROL Notify for Quantity Below]_für diese spezifische Quelle, wenn_[!UICONTROL Notify Quantity Use Default]_ nicht ausgewählt ist. |
| [!UICONTROL Notify Quantity Use Default] | Global | Gibt an, dass die Standardeinstellung für _[!UICONTROL Notify for Quantity Below]_im Produkt_[!UICONTROL Advanced Inventory]_ oder globale Einstellung in der Store-Konfiguration. |

## Erweiterte Produktoptionen

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Öffnen Sie ein Produkt im Bearbeitungsmodus.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Sources]** und klicken Sie auf **[!UICONTROL Advanced Inventory]**.

1. Aktivieren [Bestandskontrolle](enable.md) für Ihren Katalog festlegen **[!UICONTROL Manage Stock]** nach `Yes`.

   >[!NOTE]
   >
   >[!UICONTROL Manage Stock] -Einstellungen in untergeordneten Produkten überschreiben ein konfigurierbares Produkt.

   ![Erweiterter Bestand für ein Produkt](assets/inventory-backorders-product-settings.png){width="600" zoomable="yes"}

1. Geben Sie einen Betrag für die **[!UICONTROL Out-of-Stock Threshold]**:

   | Wert | Beschreibung |
   | ----- | ----- |
   | Positiver Betrag | Mit _[!UICONTROL Backorders]_deaktiviert ist, geben Sie einen positiven Wert ein. |
   | Null | Mit _[!UICONTROL Backorders]_aktiviert, Eingabe `0` ermöglicht unendliche Rückläufe. |
   | Negativer Betrag | Mit _[!UICONTROL Backorders]_aktiviert ist, wird die Eingabe eines negativen Werts empfohlen. Der Betrag wird der Verkaufsmenge hinzugefügt. Geben Sie beispielsweise `-50` um Bestellungen bis zu diesem Betrag zuzulassen. |

1. Geben Sie die **[!UICONTROL Minimum Qty Allowed in Shopping Cart]**.

1. Geben Sie die **[!UICONTROL Maximum Qty Allowed in Shopping Cart]**.

1. Satz **[!UICONTROL Qty uses Decimals]** nach `Yes` , wenn Kunden bei der Eingabe der bestellten Menge einen Dezimalwert anstelle einer Ganzzahl verwenden können.

1. Satz **[!UICONTROL Allow Multiple Boxes for Shipping]** nach `Yes` wenn das Produkt separat verkauft werden kann, in vielen Kisten. Diese Option ist sichtbar, wenn **[!UICONTROL Qty Uses Decimals]** auf `Yes` nur.

1. Satz **[!UICONTROL Backorders]** auf einen der folgenden Werte zu:

   | Option | Beschreibung |
   | ----- | ----- |
   | `No Backorders` | Nicht akzeptieren von Rückständen, wenn das Produkt nicht vorrätig ist. |
   | `Allow Qty Below 0` | Zu akzeptieren Rückstände, wenn die Menge unter null fällt. |
   | `Allow Qty Below 0 and Notify Customer` | Um Nachbestellungen zu akzeptieren, wenn die Menge unter null fällt, und den Kunden darüber zu informieren, dass die Bestellung noch aufgegeben werden kann. |

   Weitere Informationen finden Sie unter [Konfigurieren von Rückständen](backorders.md).

1. Um Mengenerhöhungen für das Produkt zu aktivieren, legen Sie **[!UICONTROL Enable Qty Increments]** nach `Yes` und geben Sie die Anzahl der Artikel an, die gekauft werden müssen, um die Anforderungen in der **[!UICONTROL Qty Increments]** -Feld.

   So kann beispielsweise ein Artikel, der in sechs Schritten verkauft wird, in Mengen von 6, 12, 18 usw. gekauft werden.

1. Wenn Sie fertig sind, klicken Sie auf **[!UICONTROL Done]** und dann **[!UICONTROL Save]**.

### Feldbeschreibungen

| Feld | Anwendungsbereich | Beschreibung |
|--|--|--|
| [!UICONTROL Manage Stock] | Global | Bestimmt, ob zur Verwaltung dieses Produkts in Ihrem Katalog eine Bestandskontrolle verwendet wird. Alle aktivieren oder deaktivieren [!DNL Inventory Management] Funktionen. Wenn Sie eine Rückgabe oder ein Kreditmemo abschließen, wird die Produktmenge automatisch an die betroffene Quellmenge zurückgegeben. Bei Verwendung eines ERP-Systems eines Drittanbieters können Sie diese Option deaktivieren. |
| [!UICONTROL Out-of-Stock Threshold] | Global | Bestimmt den Lagerbestand, bei dem eine Ware als nicht vorrätig gilt. Optionen:<br />Positiver Wert - Wenn die Rückstände deaktiviert sind, geben Sie einen positiven Wert ein.<br />Null (0) - Wenn Rückorder aktiviert sind, ermöglicht die Eingabe von Null unendliche Rückläufe.<br />Negativer Wert - Bei aktivierten Rückständen wird die Eingabe eines negativen Betrags empfohlen. Der Betrag wird der Verkaufsmenge hinzugefügt. Geben Sie beispielsweise `-50` um Bestellungen bis zu diesem Betrag zuzulassen. |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | Global | Bestimmt die Mindestanzahl des Produkts, das in einer Bestellung erworben werden kann. |
| [!UICONTROL Maximum Qty Allowed in Shopping Cart] | Global | Bestimmt die maximale Anzahl von Produkten, die in einer Bestellung erworben werden können. |
| [!UICONTROL Qty Uses Decimals] | Global | Bestimmt, ob Kunden bei der Eingabe der bestellten Menge einen Dezimalwert anstelle einer Ganzzahl verwenden können. Optionen:<br />`Yes` - Erlaubt die Eingabe von Werten als Dezimalstellen anstelle von Ganzzahlen. Dezimalstellen eignen sich für Produkte, die nach Gewicht, Volumen oder Länge verkauft werden.<br />`No` - Erfordert die Angabe von Mengenwerten als Ganzzahlen. |
| [!UICONTROL Allow Multiple Boxes for Shipping] | Global | Bestimmt, ob Teile des Produkts separat ausgeliefert werden können. Diese Option ist sichtbar, wenn **[!UICONTROL Qty Uses Decimals]** = `Yes`. |
| [!UICONTROL Backorders] | Global | Bestimmt, wie Rückstände verwaltet werden. Aufstockungen ändern den Verarbeitungsstatus der Bestellung nicht. Die Mittel werden weiterhin unmittelbar bei der Bestellung zugelassen oder erfasst, unabhängig davon, ob das Produkt vorrätig ist. Produkte werden versandt, sobald sie verfügbar werden. Wenn diese Option aktiviert ist, wird empfohlen, einen negativen Betrag für den Schwellenwert außerhalb des Lagers einzugeben. Optionen:<br/>`No Backorders` - Keine Nachbestellungen, wenn das Produkt nicht vorrätig ist.<br />`Allow Qty Below 0` - Akzeptiert Rückstände, wenn die Menge unter null fällt.<br />`Allow Qty Below 0 and Notify Customer` - Akzeptiert Rückaufträge, wenn die Menge unter null fällt, benachrichtigt Kunden jedoch darüber, dass weiterhin Bestellungen aufgegeben werden können. |
| [!UICONTROL Enable Qty Increments] | Global | Bestimmt, ob das Produkt in Mengenschritten verkauft werden kann. |

>[!NOTE]
>
>Die einfache Produktkonfiguration setzt konfigurierbare Produktkonfigurationen für ein bestimmtes Produkt außer Kraft.
