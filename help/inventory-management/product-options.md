---
title: Konfigurieren  [!DNL Inventory Management]  Produktoptionen
description: Erfahren Sie, wie Sie die  [!DNL Inventory Management] -Produktkonfigurationsoptionen konfigurieren.
exl-id: b5cff7d2-5197-4362-9503-b07c80793ac7
feature: Inventory, Products
source-git-commit: 67cbb0d05f9f63ef51ccff3580cd27df86645fd0
workflow-type: tm+mt
source-wordcount: '909'
ht-degree: 0%

---

# Konfigurieren [!DNL Inventory Management] Produktoptionen

Diese Konfigurationen gelten nur für das bearbeitete Produkt und überschreiben alle Konfigurationen auf der globalen Website-Ebene. Ändern Sie diese Einstellungen beim Bearbeiten eines Produkts über den Abschnitt _[!UICONTROL Sources]_und_[!UICONTROL Advanced Inventory]_ Seite.

- Konfigurieren von Produktoptionen nach Quelle
- Konfigurieren von Produktoptionen für eine erweiterte Inventarisierung

## Produktoptionen nach Quelle

Konfigurieren Sie die Mengen und zusätzlichen Einstellungen pro [hinzugefügte Quelle](sources-add.md) für das Produkt.

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Öffnen Sie ein Produkt im Bearbeitungsmodus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Sources]** und konfigurieren Sie Produkteinstellungen für jede Quelle:

   - Geben Sie einen **[!UICONTROL Qty]** (Menge) ein.

   - Legen Sie die **[!UICONTROL Source Item Status]** als `In Stock` oder `Out of Stock` fest.

   - Um die Benachrichtigung für die unten stehende Menge pro Quelle zu ändern, deaktivieren oder aktivieren Sie das Kontrollkästchen **[!UICONTROL Notify Quantity Use Default]**.

     Wenn dies deaktiviert ist, geben Sie den Lagerbetrag ein, der den nicht vorrätigen Hinweis des Artikels Trigger. Der eingegebene Betrag wird von der Verkaufsmenge des Artikels auf Lagerebene abgezogen.

     `Select to use Default` - [!DNL Commerce] prüft die erweiterten Inventaroptionen des Produkts auf Konfigurationseinstellungen.
     `Clear to Modify` - Geben Sie einen Wert für die Menge benachrichtigen ein, wobei erweiterte Inventar- und Store-Konfigurationseinstellungen außer Kraft gesetzt werden.

   ![Abschnitt „Quellen“ für ein Produkt](assets/inventory-product-quantity-edit.png){width="350" zoomable="yes"}

1. Klicken Sie abschließend auf **[!UICONTROL Done]** und dann auf **[!UICONTROL Save]**.

### Feldbeschreibungen

| Feld | Umfang | Beschreibung |
|--|--|--|
| [!UICONTROL Source Code] | Global | Der eindeutige Code für eine [Quelle](sources-manage.md). |
| [!UICONTROL Name] | Global | Der eindeutige Name für eine Quelle. |
| [!UICONTROL Status] | Global | Produkt ist im Katalog aktiviert oder deaktiviert. |
| [!UICONTROL Source Item Status] | Global | Legt die aktuelle Verfügbarkeit des Produkts fest. Optionen: <br />`In Stock` - Stellt das Produkt zum Kauf bereit.<br />`Out of Stock` - Wenn keine Auftragsrückstände aktiviert sind, verhindert , dass das Produkt zum Kauf verfügbar ist, und entfernt die Auflistung aus dem Katalog. |
| [!UICONTROL Qty] | Global | Verfügbare Lagerbestände für jede Quelle oder jeden Standort. |
| [!UICONTROL Notify Quantity] | Global | Ein Betrag für die _[!UICONTROL Notify for Quantity Below]_für diese spezifische Quelle, wenn_[!UICONTROL Notify Quantity Use Default]_ nicht ausgewählt ist. |
| [!UICONTROL Notify Quantity Use Default] | Global | Gibt an, dass die Standardeinstellung für _[!UICONTROL Notify for Quantity Below]_in der_[!UICONTROL Advanced Inventory]_ oder die globale Einstellung in der Store-Konfiguration verwendet werden soll. |

## Erweiterte Produktoptionen

1. Navigieren Sie in der _Admin_-Seitenleiste zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Öffnen Sie ein Produkt im Bearbeitungsmodus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Sources]** und klicken Sie auf **[!UICONTROL Advanced Inventory]**.

1. Um die [Bestandskontrolle](enable.md) für Ihren Katalog zu aktivieren, legen Sie **[!UICONTROL Manage Stock]** auf `Yes` fest.

   >[!NOTE]
   >
   >[!UICONTROL Manage Stock] Einstellungen in untergeordneten Produkten setzen konfigurierbare Produkte außer Kraft.

   ![Erweiterter Bestand für ein Produkt](assets/inventory-backorders-product-settings.png){width="600" zoomable="yes"}

1. Geben Sie einen Betrag für die **[!UICONTROL Out-of-Stock Threshold]** ein:

   | Wert | Beschreibung |
   | ----- | ----- |
   | Positiver Betrag | Geben Sie bei deaktiviertem _[!UICONTROL Backorders]_einen positiven Wert ein. |
   | Null | Wenn _[!UICONTROL Backorders]_aktiviert ist, ermöglicht die Eingabe von `0` unendliche Nachbestellungen. |
   | Negativer Betrag | Bei aktiviertem _[!UICONTROL Backorders]_wird die Eingabe eines negativen Werts empfohlen. Der Betrag wird der Verkaufsmenge hinzugefügt. Geben Sie beispielsweise `-50` ein, um Bestellungen bis zu diesem Betrag zuzulassen. |

1. Geben Sie die **[!UICONTROL Minimum Qty Allowed in Shopping Cart]** ein.

1. Geben Sie die **[!UICONTROL Maximum Qty Allowed in Shopping Cart]** ein.

1. Legen Sie **[!UICONTROL Qty uses Decimals]** auf `Yes` fest, wenn Kunden bei der Eingabe der bestellten Menge einen Dezimalwert anstatt einer Ganzzahl verwenden können.

1. Legen Sie **[!UICONTROL Allow Multiple Boxes for Shipping]** auf `Yes` fest, ob das Produkt separat in vielen Kisten verkauft werden kann. Diese Option ist nur sichtbar, wenn **[!UICONTROL Qty Uses Decimals]** auf `Yes` festgelegt ist.

1. Legen Sie **[!UICONTROL Backorders]** auf eine der folgenden Einstellungen fest:

   | Option | Beschreibung |
   | ----- | ----- |
   | `No Backorders` | Keine Rückstände akzeptieren, wenn das Produkt nicht vorrätig ist. |
   | `Allow Qty Below 0` | Rückstände annehmen, wenn die Menge unter null fällt. |
   | `Allow Qty Below 0 and Notify Customer` | Rückstände zu akzeptieren, wenn die Menge unter null fällt, und dem Kunden mitzuteilen, dass die Bestellung noch aufgegeben werden kann. |

   Weitere Informationen finden Sie unter [Konfigurieren von Rückständen](backorders.md).

1. Um Mengeninkremente für das Produkt zu aktivieren, setzen Sie **[!UICONTROL Enable Qty Increments]** auf `Yes` und geben Sie die Anzahl der Artikel ein, die gekauft werden müssen, um die Anforderung zu erfüllen, im Feld **[!UICONTROL Qty Increments]** an.

   Beispielsweise kann ein Artikel, der in Schritten von sechs verkauft wird, in Mengen von 6, 12, 18 usw. gekauft werden.

   **[!UICONTROL Qty Increments]** Feld legt fest, wie viele Produktelemente als einzelnes Produkt und als untergeordnetes Element von konfigurierbaren, gruppierten und gebündelten Produkten erworben werden müssen.

1. Klicken Sie abschließend auf **[!UICONTROL Done]** und dann auf **[!UICONTROL Save]**.

### Feldbeschreibungen

| Feld | Umfang | Beschreibung |
|--|--|--|
| [!UICONTROL Manage Stock] | Global | Legt fest, ob die Bestandskontrolle zur Verwaltung dieses Produkts in Ihrem Katalog verwendet wird. Legen Sie fest, um alle [!DNL Inventory Management] zu aktivieren oder zu deaktivieren. Wenn Sie eine Rücksendung oder Gutschrift abschließen, wird die Produktmenge automatisch an die entsprechende Bezugsmenge zurückgegeben. Sie sollten ggf. deaktivieren, wenn Sie ein ERP-System eines Drittanbieters verwenden. |
| [!UICONTROL Out-of-Stock Threshold] | Global | Bestimmt den Lagerbestand, bei dem ein Produkt als nicht vorrätig gilt. Optionen:<br />Positiver Wert - Geben Sie einen positiven Betrag ein, wenn die Rückstände deaktiviert sind.<br />Null (0) - Bei aktivierten Rückbestellungen ermöglicht die Eingabe von Null unendliche Rückbestellungen.<br />Negativer Wert - Bei aktivierten Rückständen wird die Eingabe eines negativen Betrags empfohlen. Der Betrag wird der Verkaufsmenge hinzugefügt. Geben Sie beispielsweise `-50` ein, um Bestellungen bis zu diesem Betrag zuzulassen. |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | Global | Bestimmt die Mindestanzahl des Produkts, das in einer einzigen Bestellung gekauft werden kann. |
| [!UICONTROL Maximum Qty Allowed in Shopping Cart] | Global | Bestimmt die maximale Anzahl des Produkts, das in einer einzigen Bestellung gekauft werden kann. |
| [!UICONTROL Qty Uses Decimals] | Global | Legt fest, ob Kunden bei der Eingabe der bestellten Menge einen Dezimalwert anstelle einer Ganzzahl verwenden können. Optionen: <br />`Yes` - Ermöglicht die Eingabe von Werten als Dezimalzahlen und nicht als Ganzzahlen. Dezimalzahlen eignen sich für Produkte, die nach Gewicht, Volumen oder Länge verkauft werden.<br />`No` - Erfordert die Eingabe von Mengenwerten als Ganzzahl. |
| [!UICONTROL Allow Multiple Boxes for Shipping] | Global | Legt fest, ob Teile des Produkts separat versendet werden können. Diese Option ist sichtbar, wenn **[!UICONTROL Qty Uses Decimals]** = `Yes`. |
| [!UICONTROL Backorders] | Global | Legt fest, wie Auftragsrückstände verwaltet werden. Rückstände ändern den Verarbeitungsstatus der Bestellung nicht. Die Mittel werden unmittelbar nach Auftragserteilung noch bewilligt oder eingezogen, unabhängig davon, ob das Produkt auf Lager ist. Produkte werden versendet, sobald sie verfügbar werden. Wenn diese Option aktiviert ist, wird empfohlen, einen negativen Betrag für den Schwellenwert für nicht vorrätige Artikel einzugeben. Optionen: <br/>`No Backorders` - Akzeptiert keine Nachbestellungen, wenn das Produkt nicht vorrätig ist.<br />`Allow Qty Below 0` - Akzeptiert Nachbestellungen, wenn die Menge unter null fällt.<br />`Allow Qty Below 0 and Notify Customer` - Akzeptiert Nachbestellungen, wenn die Menge unter null fällt, benachrichtigt Kunden jedoch, dass weiterhin Bestellungen aufgegeben werden können. |
| [!UICONTROL Enable Qty Increments] | Global | Bestimmt, ob das Produkt in Mengenschritten verkauft werden kann. Inkremente legen fest, wie viele Produktelemente als einzelnes Produkt und als untergeordnetes Element von konfigurierbaren, gruppierten und gebündelten Produkten erworben werden müssen. |

>[!NOTE]
>
>Eine einfache Produktkonfiguration überschreibt konfigurierbare Produktkonfigurationen für ein bestimmtes Produkt.
