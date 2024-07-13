---
title: "Configure [!DNL Inventory Management] product options"
description: Erfahren Sie, wie Sie die [!DNL Inventory Management] Produktkonfigurationsoptionen konfigurieren.
exl-id: b5cff7d2-5197-4362-9503-b07c80793ac7
feature: Inventory, Products
source-git-commit: 67cbb0d05f9f63ef51ccff3580cd27df86645fd0
workflow-type: tm+mt
source-wordcount: '909'
ht-degree: 0%

---

# Konfigurieren von [!DNL Inventory Management] -Produktoptionen

Diese Konfigurationen gelten nur für das bearbeitete Produkt, wobei alle Konfigurationen auf globaler Website-Ebene außer Kraft gesetzt werden. Ändern Sie diese Einstellungen beim Bearbeiten eines Produkts über den Abschnitt _[!UICONTROL Sources]_und die Seite_[!UICONTROL Advanced Inventory]_.

- Konfigurieren von Produktoptionen nach Quelle
- Konfigurieren von Produktoptionen für erweiterte Inventare

## Produktoptionen nach Quelle

Konfigurieren Sie die Mengen und zusätzlichen Einstellungen pro [hinzugefügter Quelle](sources-add.md) für das Produkt.

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Öffnen Sie ein Produkt im Bearbeitungsmodus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Sources]** und konfigurieren Sie die Produkteinstellungen für jede Quelle:

   - Geben Sie einen Betrag vom Typ **[!UICONTROL Qty]** (Menge) ein.

   - Setzen Sie die **[!UICONTROL Source Item Status]** auf `In Stock` oder `Out of Stock`.

   - Um das Kontrollkästchen &quot;Für Menge unter benachrichtigen&quot;pro Quelle zu ändern, deaktivieren oder aktivieren Sie das Kontrollkästchen &quot;**[!UICONTROL Notify Quantity Use Default]**&quot;.

     Geben Sie bei einer Bereinigung den Lagerbestand an, der Trigger der Meldung des Artikels ist. Der eingegebene Betrag wird von der veräußerbaren Menge des Artikels auf der Lagerebene abgezogen.

     `Select to use Default` - [!DNL Commerce] überprüft die erweiterten Lagerbestandsoptionen des Produkts auf Konfigurationseinstellungen.
     `Clear to Modify` - Geben Sie einen Wert für &quot;Menge benachrichtigen&quot;ein und überschreiben Sie die erweiterten Konfigurations- und Speichereinstellungen.

   ![Quellabschnitt für ein Produkt](assets/inventory-product-quantity-edit.png){width="350" zoomable="yes"}

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Done]** und dann auf **[!UICONTROL Save]**.

### Feldbeschreibungen

| Feld | Anwendungsbereich | Beschreibung |
|--|--|--|
| [!UICONTROL Source Code] | Global | Der eindeutige Code für eine [Quelle](sources-manage.md). |
| [!UICONTROL Name] | Global | Der eindeutige Name einer Quelle. |
| [!UICONTROL Status] | Global | Das Produkt ist im Katalog aktiviert oder deaktiviert. |
| [!UICONTROL Source Item Status] | Global | Bestimmt die aktuelle Verfügbarkeit des Produkts. Optionen:<br />`In Stock` - Stellt das Produkt zum Kauf bereit.<br />`Out of Stock` - Sofern Rückstellungen nicht aktiviert sind, verhindert, dass das Produkt zum Kauf verfügbar ist, und entfernt die Liste aus dem Katalog. |
| [!UICONTROL Qty] | Global | Auf Lager befindliche Beträge für jede Quelle oder jeden Standort. |
| [!UICONTROL Notify Quantity] | Global | Ein Betrag für die _[!UICONTROL Notify for Quantity Below]_für diese spezifische Quelle, wenn_[!UICONTROL Notify Quantity Use Default]_ nicht ausgewählt ist. |
| [!UICONTROL Notify Quantity Use Default] | Global | Gibt an, dass die Standardeinstellung für _[!UICONTROL Notify for Quantity Below]_in der Produkteinstellung_[!UICONTROL Advanced Inventory]_ oder der globalen Einstellung in der Store-Konfiguration verwendet wird. |

## Erweiterte Produktoptionen

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Öffnen Sie ein Produkt im Bearbeitungsmodus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Sources]** und klicken Sie auf **[!UICONTROL Advanced Inventory]**.

1. Um die [Bestandskontrolle](enable.md) für Ihren Katalog zu aktivieren, setzen Sie **[!UICONTROL Manage Stock]** auf `Yes`.

   >[!NOTE]
   >
   >[!UICONTROL Manage Stock] -Einstellungen in untergeordneten Produkten überschreiben ein konfigurierbares Produkt.

   ![Erweiterter Bestand für ein Produkt](assets/inventory-backorders-product-settings.png){width="600" zoomable="yes"}

1. Geben Sie einen Betrag für den Wert **[!UICONTROL Out-of-Stock Threshold]** ein:

   | Wert | Beschreibung |
   | ----- | ----- |
   | Positiver Betrag | Wenn _[!UICONTROL Backorders]_deaktiviert ist, geben Sie einen positiven Wert ein. |
   | Null | Wenn _[!UICONTROL Backorders]_aktiviert ist, ermöglicht die Eingabe von `0` unendliche Rückstände. |
   | Negativer Betrag | Wenn _[!UICONTROL Backorders]_aktiviert ist, wird die Eingabe eines negativen Werts empfohlen. Der Betrag wird der Verkaufsmenge hinzugefügt. Geben Sie beispielsweise `-50` ein, um Bestellungen bis zu diesem Betrag zuzulassen. |

1. Geben Sie den Wert **[!UICONTROL Minimum Qty Allowed in Shopping Cart]** ein.

1. Geben Sie den Wert **[!UICONTROL Maximum Qty Allowed in Shopping Cart]** ein.

1. Setzen Sie **[!UICONTROL Qty uses Decimals]** auf `Yes` , wenn Kunden bei der Eingabe der bestellten Menge einen Dezimalwert anstelle einer ganzen Zahl verwenden können.

1. Setzen Sie **[!UICONTROL Allow Multiple Boxes for Shipping]** auf `Yes` , wenn das Produkt separat in vielen Kisten verkauft werden kann. Diese Option ist sichtbar, wenn **[!UICONTROL Qty Uses Decimals]** nur auf `Yes` gesetzt ist.

1. Setzen Sie **[!UICONTROL Backorders]** auf einen der folgenden Werte:

   | Option | Beschreibung |
   | ----- | ----- |
   | `No Backorders` | Nicht akzeptieren von Rückständen, wenn das Produkt nicht vorrätig ist. |
   | `Allow Qty Below 0` | Zu akzeptieren Rückstände, wenn die Menge unter null fällt. |
   | `Allow Qty Below 0 and Notify Customer` | Um Nachbestellungen zu akzeptieren, wenn die Menge unter null fällt, und den Kunden darüber zu informieren, dass die Bestellung noch aufgegeben werden kann. |

   Weitere Informationen finden Sie unter [Konfigurieren von Rückläufen](backorders.md).

1. Um Mengenerhöhungen für das Produkt zu aktivieren, setzen Sie **[!UICONTROL Enable Qty Increments]** auf `Yes` und geben Sie die Anzahl der Artikel ein, die gekauft werden müssen, um die Anforderung im Feld **[!UICONTROL Qty Increments]** zu erfüllen.

   So kann beispielsweise ein Artikel, der in sechs Schritten verkauft wird, in Mengen von 6, 12, 18 usw. gekauft werden.

   **[!UICONTROL Qty Increments]** -Feld legt fest, wie viele Produktelemente als einzelnes Produkt und als untergeordnetes Element konfigurierbarer, gruppierter und gebündelter Produkte gekauft werden müssen.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Done]** und dann auf **[!UICONTROL Save]**.

### Feldbeschreibungen

| Feld | Anwendungsbereich | Beschreibung |
|--|--|--|
| [!UICONTROL Manage Stock] | Global | Bestimmt, ob zur Verwaltung dieses Produkts in Ihrem Katalog eine Bestandskontrolle verwendet wird. Legen Sie diese Einstellung fest, um alle [!DNL Inventory Management]-Funktionen zu aktivieren oder zu deaktivieren. Wenn Sie eine Rückgabe oder ein Kreditmemo abschließen, wird die Produktmenge automatisch an die betroffene Quellmenge zurückgegeben. Bei Verwendung eines ERP-Systems eines Drittanbieters können Sie diese Option deaktivieren. |
| [!UICONTROL Out-of-Stock Threshold] | Global | Bestimmt den Lagerbestand, bei dem eine Ware als nicht vorrätig gilt. Optionen:<br />Positiver Wert - Geben Sie bei deaktivierten Rückständen einen positiven Wert ein.<br />Null (0) - Wenn Rückorder aktiviert sind, ermöglicht die Eingabe von null unendliche Rückläufe.<br />Negativer Wert - Wenn Rückstände aktiviert sind, wird die Eingabe eines negativen Betrags empfohlen. Der Betrag wird der Verkaufsmenge hinzugefügt. Geben Sie beispielsweise `-50` ein, um Bestellungen bis zu diesem Betrag zuzulassen. |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | Global | Bestimmt die Mindestanzahl des Produkts, das in einer Bestellung erworben werden kann. |
| [!UICONTROL Maximum Qty Allowed in Shopping Cart] | Global | Bestimmt die maximale Anzahl von Produkten, die in einer Bestellung erworben werden können. |
| [!UICONTROL Qty Uses Decimals] | Global | Bestimmt, ob Kunden bei der Eingabe der bestellten Menge einen Dezimalwert anstelle einer Ganzzahl verwenden können. Optionen:<br />`Yes` - Erlaubt die Eingabe von Werten als Dezimalstellen und nicht als Ganzzahlen. Dezimalstellen eignen sich für Produkte, die nach Gewicht, Volumen oder Länge verkauft werden.<br />`No` - Erfordert die Angabe von Mengenwerten als Ganzzahlen. |
| [!UICONTROL Allow Multiple Boxes for Shipping] | Global | Bestimmt, ob Teile des Produkts separat ausgeliefert werden können. Diese Option ist sichtbar, wenn **[!UICONTROL Qty Uses Decimals]** = `Yes`. |
| [!UICONTROL Backorders] | Global | Bestimmt, wie Rückstände verwaltet werden. Aufstockungen ändern den Verarbeitungsstatus der Bestellung nicht. Die Mittel werden weiterhin unmittelbar bei der Bestellung zugelassen oder erfasst, unabhängig davon, ob das Produkt vorrätig ist. Produkte werden versandt, sobald sie verfügbar werden. Wenn diese Option aktiviert ist, wird empfohlen, einen negativen Betrag für den Schwellenwert außerhalb des Lagers einzugeben. Optionen:<br/>`No Backorders` - Akzeptiert keine Rückstände, wenn das Produkt nicht vorrätig ist.<br />`Allow Qty Below 0` - Akzeptiert Rückstände, wenn die Menge unter null fällt.<br />`Allow Qty Below 0 and Notify Customer` - Akzeptiert Rückaufträge, wenn die Menge unter null fällt, benachrichtigt Kunden jedoch darüber, dass Bestellungen weiterhin aufgegeben werden können. |
| [!UICONTROL Enable Qty Increments] | Global | Bestimmt, ob das Produkt in Mengenschritten verkauft werden kann. Inkrementierungen legen fest, wie viele Produktelemente als einzelnes Produkt und als untergeordnetes Element konfigurierbarer, gruppierter und gebündelter Produkte erworben werden müssen. |

>[!NOTE]
>
>Die einfache Produktkonfiguration setzt konfigurierbare Produktkonfigurationen für ein bestimmtes Produkt außer Kraft.
