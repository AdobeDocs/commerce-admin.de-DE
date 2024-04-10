---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Delivery Methods]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der [!UICONTROL Sales] &gt; [!UICONTROL Delivery Methods] Seite des Commerce-Administrators.
exl-id: 159b76a8-3676-4692-9cd6-18947bda4666
feature: Configuration, Shipping/Delivery
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '3773'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Delivery Methods]

{{config}}

## [!UICONTROL Basic Delivery Methods]

### [!UICONTROL Flat Rate]

![Pauschalpreis](./assets/delivery-methods-flat-rate.png)<!-- zoom -->

<!-- [Flat Rate](https://docs.magento.com/user-guide/shipping/shipping-flat-rate.html) -->

| Feld | [Scope](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enabled] | Website | Wenn diese Option aktiviert ist, wird die Option Flatrate in der _Voraussichtliche Versand- und Steuerkosten_ im Warenkorb und in der _Versand_ -Abschnitt während des Checkouts. Optionen: `Yes` / `No` |
| [!UICONTROL Title] | Shop-Ansicht | Der Name, der während des Checkouts für diese Versandmethode verwendet wird. |
| [!UICONTROL Method Name] | Shop-Ansicht | Ein Name, der die Berechnungsmethode beschreibt, die zum Erstellen einer Versandschätzung verwendet wird. Der Methodenname wird neben der berechneten geschätzten Rate im Warenkorb angezeigt. Der Standardwert lautet `Fixed`. |
| [!UICONTROL Type] | Website | Beschreibt die Art der Berechnung, die zur Ermittlung des Pauschalsatzes verwendet wird. Optionen: <br/>**`None`**- Es wird keine Berechnung verwendet. Legt die Flatrate auf Null fest, was dem kostenlosen Versand entspricht.<br/>**`Per Order`** - Es wird ein einheitlicher Pauschalsatz für die gesamte Bestellung berechnet. <br/>**`Per Item`**- Für jeden Artikel im Warenkorb wird ein separater Pauschalpreis berechnet. Der Satz wird mit der Anzahl der Artikel im Warenkorb multipliziert, auch wenn die Gesamtmenge eine Kombination verschiedener Artikel enthält. |
| [!UICONTROL Price] | Website | Der Preis, den Sie dem Kunden für den Pauschalversand berechnen. |
| [!UICONTROL Calculate Handling Fee] | Website | Legt fest, wie die Bearbeitungsgebühr berechnet wird, falls enthalten. Optionen: `Fixed` / `Percent` |
| [!UICONTROL Handling Fee] | Website | Geben Sie den Betrag ein, der für eine Bearbeitungsgebühr in Rechnung gestellt werden soll. Dieser Betrag basiert auf der Methode, die Sie zur Berechnung des Betrags gewählt haben. Wenn die Gebühr beispielsweise auf einer festen Gebühr basiert, geben Sie den Betrag als Dezimalzahl ein, z. B. 4,90. Wenn die Bearbeitungsgebühr jedoch auf einem Prozentsatz der Bestellung basiert, geben Sie den Betrag als Prozentsatz ein. Wenn Sie beispielsweise sechs Prozent der Bestellung berechnen, geben Sie den Wert wie folgt ein `.06`. |
| [!UICONTROL Displayed Error Message] | Shop-Ansicht | Eine Meldung, die angezeigt wird, wenn eine Kundin oder ein Kunde einen Pauschalpreis wählt. Aus irgendeinem Grund ist die Methode jedoch nicht verfügbar. |
| [!UICONTROL Ship to Applicable Countries] | Website | Gibt die Länder an, in denen Sie Pauschallieferungen anbieten. Optionen: <br/>**`All Allowed Countries`**- Kunden aus jedem Land, das in der Store-Konfiguration angegeben ist, können den Flat-Rate-Versand verwenden.<br/>**`Specific Countries`** - Kunden aus bestimmten Ländern können den Pauschalversand nutzen. |
| [!UICONTROL Ship to Specific Countries] | Website | Gibt jedes Land an, in dem Kunden Pauschallieferungen verwenden können. |
| [!UICONTROL Show Method if Not Applicable] | Website | Bestimmt, ob während des Checkouts eine Pauschale als Option angezeigt wird, wenn die Methode nicht für den Kauf gilt. Optionen: `Yes` / `No` |
| [!UICONTROL Sort Order] | Website | Eine Zahl, die die Reihenfolge bestimmt, in der die Pauschale angezeigt wird, wenn sie beim Checkout mit anderen Versandmethoden aufgelistet wird. |

{style="table-layout:auto"}

### [!UICONTROL Free Shipping]

![kostenloser Versand](./assets/delivery-methods-free-shipping.png)<!-- zoom -->

<!-- [Free Shipping](https://docs.magento.com/user-guide/shipping/shipping-free.html) -->

| Feld | [Scope](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enabled] | Website | Wenn diese Option aktiviert ist, wird der kostenlose Versand während des Checkouts als Option im Abschnitt Versand angezeigt. Optionen: `Yes` / `No` |
| [!UICONTROL Title] | Shop-Ansicht | Der Name, der während des Checkouts für diese Versandmethode verwendet wird. |
| Methodenname | Shop-Ansicht | Ein Name, der die Berechnungsmethode beschreibt, die zum Erstellen einer Versandschätzung verwendet wird. Der Methodenname wird neben der berechneten geschätzten Rate im Warenkorb angezeigt. Der Standardwert lautet `Free`. |
| Mindestbestellmenge | Website | Der Mindestkauf, der erforderlich ist, um einen kostenlosen Versand auf eine Bestellung anzuwenden. |
| Steuer in Betrag einbeziehen | Website | Bestimmt, ob die Steuer in der Berechnung des Mindestauftragsbetrags enthalten ist. Optionen: <br/>**Ja** - Die Steuer wird bei der Berechnung des Mindestbestellungsbetrags berücksichtigt (Zwischensumme + Steuer - Rabatt).<br/>**Nein** - Steuer ist bei der Berechnung des Mindestauftragsbetrags nicht enthalten (Zwischensumme - Rabatt). |
| Angezeigte Fehlermeldung | Shop-Ansicht | Eine Meldung, die angezeigt wird, wenn eine Kundin oder ein Kunde den kostenlosen Versand wählt, die Methode jedoch aus irgendeinem Grund nicht verfügbar ist. |
| Versand in die entsprechenden Länder | Website | Gibt die Länder an, in denen Sie kostenlosen Versand anbieten. Optionen: <br/>**Alle zulässigen Länder** - Kunden aus jedem Land, das in der Store-Konfiguration angegeben ist, können den kostenlosen Versand verwenden. <br/>**Bestimmte Länder** - Kunden aus bestimmten Ländern können den kostenlosen Versand verwenden. |
| Versand in bestimmte Länder | Website | Gibt jedes Land an, in dem Kunden den kostenlosen Versand verwenden können. |
| Methode anzeigen, falls nicht zutreffend | Website | Legt fest, ob beim Checkout der kostenlose Versand als Option angezeigt wird, wenn die Methode nicht auf den Kauf angewendet wird. Optionen: `Yes` / `No` |
| [!UICONTROL Sort Order] | Website | Eine Zahl, die die Bestellung bestimmt, die der kostenlose Versand angezeigt wird, wenn er mit anderen Versandmethoden während des Checkouts aufgelistet wird. |

{style="table-layout:auto"}

### [!UICONTROL Table Rates]

![Tabellen-Tarife](./assets/delivery-methods-table-rates.png)<!-- zoom -->

<!-- [Table Rates](https://docs.magento.com/user-guide/shipping/shipping-table-rate.html) -->

| Feld | [Scope](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enabled] | Website | Wenn diese Option aktiviert ist, werden die Tabellensätze als Option im Abschnitt „Schätzung von Versand und Steuer“ des Warenkorbs und im Abschnitt „Versand“ während des Checkouts angezeigt. Optionen: `Yes` / `No` |
| [!UICONTROL Title] | Shop-Ansicht | Der Name, der während des Checkouts für diese Versandmethode verwendet wird. |
| Methodenname | Shop-Ansicht | Ein Name, der die Berechnungsmethode beschreibt, die zum Erstellen einer Versandschätzung verwendet wird. Der Methodenname wird neben der berechneten geschätzten Rate im Warenkorb angezeigt. Der Standardwert lautet `Table Rate`. |
| [!UICONTROL Condition] | Website | Bestimmt die Bedingung, auf der die Berechnung basiert. Das Format der hochgeladenen CSV-Datei ist für jede Bedingung spezifisch. Optionen: `Weight vs. Destination` / `Price vs. Destination` / `# of Items vs. Destination` |
| [!UICONTROL Include Virtual Products in Price Calculation] | Website | Bestimmt, ob virtuelle Produkte, die nicht versendet werden müssen, in die Berechnung des Tabellenratenpreises einbezogen werden. |
| [!UICONTROL Calculate Handling Fee] | Website | Legt fest, wie die Bearbeitungsgebühr berechnet wird, falls enthalten. Optionen: `Fixed` / `Percent` |
| [!UICONTROL Handling Fee] | Website | Die Höhe der Gebühr, die der Versandgebühr zur Deckung der Kosten für die Bearbeitung der Sendung hinzugefügt wird. Geben Sie den Wert als Dezimalzahl ein. Wenn die Gebühr beispielsweise auf einem Prozentsatz basiert, geben Sie 0,06 anstatt 6 % ein. Geben Sie als festen Betrag ein. `6.00`. |
| [!UICONTROL Displayed Error Message] | Shop-Ansicht | Eine Meldung, die angezeigt wird, wenn eine Kundin oder ein Kunde „Tarife - Tabelle“ auswählt, die Methode jedoch aus irgendeinem Grund nicht verfügbar ist. |
| [!UICONTROL Ship to Applicable Countries] | Website | Gibt die Länder an, in denen Sie Versand mit Tabellensatz anbieten. Optionen: <br/>**`All Allowed Countries`**- Kunden aus einem beliebigen Land, das in der Store-Konfiguration angegeben ist, können den Versand mit Tabellensätzen verwenden.<br/>**`Specific Countries`** - Kunden aus bestimmten Ländern können den Versand mit Tabellenraten verwenden. |
| [!UICONTROL Ship to Specific Countries] | Website | Gibt jedes Land an, in dem Kunden den Versand mit dem Tarif „Tabelle“ verwenden können. |
| [!UICONTROL Show Method if Not Applicable] | Website | Bestimmt, ob die Tabellensätze während des Kaufs als Option angezeigt werden, wenn die Methode nicht auf den Kauf angewendet wird. Optionen: `Yes` / `No` |
| [!UICONTROL Sort Order] | Website | Eine Zahl, die die Reihenfolge bestimmt, in der die Tabellensätze angezeigt werden, wenn sie während des Checkouts mit anderen Versandmethoden aufgelistet werden. |

{style="table-layout:auto"}

### [!UICONTROL In-Store Delivery]

![Versand im Geschäft](./assets/delivery-methods-in-store-delivery.png)<!-- zoom -->

<!-- [In-Store Delivery](https://docs.magento.com/user-guide/shipping/shipping-in-store-delivery.html) -->

| Feld | [Scope](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enabled] | Website | Wenn diese Option aktiviert ist, kann der Versand im Geschäft als Option im _Voraussichtliche Versand- und Steuerkosten_ im Warenkorb und in der _Versand_ -Abschnitt während des Checkouts. Optionen: `Yes` / `No` |
| [!UICONTROL Method Name] | Shop-Ansicht | Ein Name, der die Funktion „Abholung im Geschäft“ als Versandmethode identifiziert. Dieser Wert wird als Beschriftung einer Registerkarte oben auf der Seite zur Versandkasse und in der Tabelle der verfügbaren Versandmethoden unten auf derselben Seite angezeigt. Der Standardwert lautet `In-store Delivery`. |
| [!UICONTROL Title] | Shop-Ansicht | Der Name, der während des Checkouts für diese Versandmethode verwendet wird. |
| [!UICONTROL Price] | Website | Der Preis, den Sie dem Kunden für eine Abholung im Geschäft in Rechnung stellen. |
| [!UICONTROL Search Radius] | Website | Der Radius in km, der bei der Suche nach Abholorten verwendet werden soll. |
| [!UICONTROL Displayed Error Message] | Shop-Ansicht | Eine Meldung, die angezeigt wird, wenn eine Kundin oder ein Kunde eine Abholung im Geschäft auswählt, die Versandmethode jedoch nicht verfügbar ist. |

{style="table-layout:auto"}

## [!UICONTROL Carriers]

### [!UICONTROL UPS]

{{ups-api}}

![UPS REST-Kontoeinstellungen](./assets/delivery-methods-ups1.png)<!-- zoom -->

![UPS XML-Kontoeinstellungen](./assets/delivery-methods-ups1.png)<!-- zoom -->

<!-- [UPS REST Account Settings](https://docs.magento.com/user-guide/shipping/ups.html) -->

| Feld | [Scope](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enabled for Checkout] | Website | Bestimmt, ob UPS Kunden während des Checkouts als Versandmethode zur Verfügung steht. Optionen: `Yes` / `No` |
| [!UICONTROL Enabled for RMA] | Website | Bestimmt, ob UPS Kunden als Versandmethode für eine RMA zur Verfügung steht. Optionen: `Yes` / `No` |
| _[!UICONTROL UPS Account Settings]_ |  |  |
| [!UICONTROL Live Account] | Shop-Ansicht | Gibt an, dass das United Parcel Service-Konto live ist. Optionen: `Yes` / `No` |
| [!UICONTROL Title] | Shop-Ansicht | Der Name, der während des Checkouts für diese Versandmethode verwendet wird. |
| _[!UICONTROL UPS REST Account Settings]_ |  |  |
| [!UICONTROL Gateway URL] | Website | Für den UPS-REST-Dienst zeigt die folgenden URLs an, die zur Übertragung von JSON-Daten erforderlich sind: Gateway-URL, Tracking-URL, Versand-URL |
| [!UICONTROL Mode] | Website | Bestimmt den Übertragungsmodus für Daten, die an das USV-System gesendet werden. Optionen: <br/>**`Development`**- UPS überprüft nicht, ob vom Commerce-Server empfangene Daten über SSL gesendet werden.<br/>**`Live`** - UPS überprüft, ob vom Commerce-Server empfangene Daten über eine SSL (Secure Socket Layer) gesendet werden. |
| Benutzer-ID | Website | Ihre UPS Versand Konto Client ID. |
| [!UICONTROL Origin of the Shipment] | Website | (Nur UPS-REST) Das Land oder die Region, aus dem/der die Produktlieferung stammt. |
| [!UICONTROL Password] | Shop-Ansicht | Ihr UPS Versand-Konto Kundengeheimnis. |

{style="table-layout:auto"}

![UPS Paketinformationen](./assets/delivery-methods-ups-packaging-settings.png)<!-- zoom -->

<!-- [UPS Package Information](https://docs.magento.com/user-guide/shipping/ups.html) -->

| Feld | [Scope](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| _[!UICONTROL UPS Negotiated Rate Settings]_ |  |  |
| [!UICONTROL Enable Negotiated Rates] | Website | (Nur UPS-REST) Aktiviert/deaktiviert Sondertarife gemäß Ihrer Vereinbarung mit UPS. Optionen: `Yes` / `No` |
| [!UICONTROL Packages Request Type] | Website | Bestimmt, wie das Gewicht für Sendungen mit mehreren Paketen berechnet wird. Optionen: `Divide to equal weight (one request)` / `Use origin weight (multiple requests)` |
| [!UICONTROL Shipper Number] | Website | (Nur UPS-REST) Die sechsstellige UPS-Liefernummer ist für Referenzzwecke zur Verwendung ausgehandelter Tarife erforderlich. |
| [!UICONTROL Container] | Website | Legt den Container-Typ fest, der zum Verpacken von Sendungen verwendet wird. Optionen: `Customer Packaging` / `UPS Letter Envelope` / `Customer Packaging` / `UPS Letter Envelope` / `UPS Tube` / `UPS Express Box` / `UPS Worldwide 25 kilo` / `UPS Worldwide 10 kilo` |
| [!UICONTROL Weight Unit] | Website | Legt die Standardmaßeinheit für das Produktgewicht in Ihrem Geschäft fest. Siehe [Dimensionsgewicht](../../stores-purchase/carriers.md#dimensional-weight) für weitere Informationen. |
| [!UICONTROL Tracking URL] | Website | (Nur UPS-REST) Die UPS-URL, die zum Nachverfolgen von Paketen verwendet wird. |
| [!UICONTROL Destination Type] | Website | Legt den Standard-Zieltyp für die Lieferung fest. Optionen: `Business` / `Residential` |
| [!UICONTROL Maximum Package Weight] | Website | Legt das maximale Gewicht fest, das ein Paket gemäß der Angabe von UPS haben kann. Wenn die bestellten Produkte das maximale Paketgewicht überschreiten, ist diese Versandoption nicht verfügbar. Nach [UPS.com](https://www.ups.com/us/en/global.page), Packstücke dürfen 150 lbs (70 kg) nicht überschreiten. Erkundigen Sie sich bei Ihrem Spediteur nach dem maximalen Gewicht. |
| [!UICONTROL Pickup Method] | Website | Einstellung der Abholmethode der USV. Optionen: `Regular Daily Pickup` / `On Call Air` / `One Time Pickup` / `Letter Center` / `Customer Counter` |
| [!UICONTROL Minimum Package Weight] | Website | Legt die Mindestgewichtung eines Pakets fest, die von UPS angegeben werden kann. Wenn die bestellten Produkte weniger wiegen als das minimale Paketgewicht, ist diese Versandoption nicht verfügbar. Um das Mindestgewicht zu überprüfen, fragen Sie Ihren Spediteur. |
| [!UICONTROL Calculate Handling Fee] | Website | Legt die Methode zur Berechnung der Bearbeitungsgebühr für den Versand mit Tabellensätzen fest. Optionen: <br>**`Fixed`**- Die Bearbeitungsgebühr ist ein fester Satz.<br>**`Percent`** - Die Bearbeitungsgebühr wird in Prozent des Bestellbetrags erhoben. |
| [!UICONTROL Handling Applied] | Website | Gibt an, ob die Bearbeitungsgebühr auf jede Bestellung oder auf jedes Paket innerhalb einer Bestellung angewendet wird. |
| [!UICONTROL Handling Fee] | Website | Legt die Handhabung fest, die im Versandratenpreis enthalten ist. Die Bearbeitungsgebühr kann als fester Betrag oder als Prozentsatz festgelegt werden. <br/><br/>**_Hinweis:_**Wenn Sie einen Prozentwert eingeben, verwenden Sie das Dezimalformat . `0.25` für 25 %. |

{style="table-layout:auto"}

![Zugelassene USV-Methoden](./assets/delivery-methods-ups-allowed-methods.png)<!-- zoom -->

<!-- [UPS Allowed Methods](https://docs.magento.com/user-guide/shipping/ups.html) -->

| Feld | [Scope](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| _[!UICONTROL UPS allowed methods]_ |  |  |
| [!UICONTROL Allowed Methods] | Website | Gibt die zulässigen Methoden für den UPS-Versand an, die Kunden angeboten werden. Die Versandkosten werden anhand der gewählten Versandart berechnet. |
| [!UICONTROL Free Method] | Website | Identifiziert die Methode, die für den kostenlosen Versand über UPS verwendet wird. Um den kostenlosen Versand zu deaktivieren, wählen Sie „Keine„. <br/><br/>**_Hinweis:_**Diese Methode ähnelt der grundlegenden [kostenloser Versand](../../stores-purchase/shipping-free.md)Allerdings erscheint es während des Checkouts als UPS Versandoption. |
| [!UICONTROL Free Shipping Amount Threshold] | Website | Bestimmt, ob ein kostenloser Versand angewendet wird, wenn der Bestellbetrag den Schwellenwert für den kostenlosen Versand erreicht. Optionen: `Enable` / `Disable` |
| [!UICONTROL Free Shipping Amount Threshold] | Website | Legt den minimalen Gesamtbetrag fest, den eine Bestellung erreichen muss, um für den kostenlosen Versand qualifiziert zu sein. |
| [!UICONTROL Displayed Error Message] | Shop-Ansicht | Die Fehlermeldung, die angezeigt wird, wenn diese Versandmethode aus irgendeinem Grund nicht verfügbar ist. |

{style="table-layout:auto"}

![UPS Anwendbare Länder und andere Einstellungen](./assets/delivery-methods-ups-ship-to.png)<!-- zoom -->

<!-- [UPS Applicable Countries and Other Settings](https://docs.magento.com/user-guide/shipping/ups.html) -->

| Feld | [Scope](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| _[!UICONTROL UPS Applicable countries and other Settings]_ |  |  |
| [!UICONTROL Ship to Applicable Countries] | Website | Gibt an, welches Land Kundinnen und Kunden diese Versandart verwenden dürfen. Optionen: <br/>**`All Allowed Countries`**- Kunden aus allen [Länder](../../getting-started/store-details.md#country-options) Diese Versandmethode kann verwendet werden, wenn sie in Ihrer Store-Konfiguration angegeben ist.<br/>**`Specific Countries`** - Nach Auswahl dieser Option wird die [!UICONTROL Ship to Specific Countries] Liste angezeigt. Wählen Sie jedes Land in der Liste aus, in dem diese Versandart verwendet werden kann. |
| [!UICONTROL Show Method if Not Applicable] | Website | Bestimmt, ob UPS beim Checkout immer als Versandoption angezeigt wird. Optionen: <br/>**`Yes`**- UPS erscheint immer als Versandoption während des Checkouts, auch wenn dies nicht auf die Bestellung zutrifft.<br/>**`No`** - UPS erscheint nur dann als Versandoption beim Checkout, wenn es auf die Bestellung zutrifft. (Zum Beispiel, wenn die Auftragsgewichtung die maximale Gewichtsmenge überschreitet.) |
| [!UICONTROL Debug] | Website | Gibt an, ob Datenübertragungen zwischen Ihrem Store und UPS zum Debugging im System protokolliert werden. Sofern kein Problem vorliegt, das verfolgt und protokolliert werden muss, sollte diese Option auf Folgendes festgelegt werden `No`. |
| [!UICONTROL Sort Order] | Website | Eine Zahl, die die Reihenfolge bestimmt, in der UPS beim Checkout mit anderen Versandmethoden aufgelistet wird. eintreten in `0` am Anfang der Liste. |

{style="table-layout:auto"}

### [!UICONTROL USPS]

| Feld | [Scope](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| Aktiviert für Checkout | Website | Bestimmt, ob USPS Kunden während des Checkouts als Versandmethode zur Verfügung steht. Optionen: `Yes` / `No` |
| _[!UICONTROL USPS Account Settings]_ |  |  |
| [!UICONTROL Gateway URL] | Website | Die URL, über die eine Verbindung zum USPS-System hergestellt wird, um Versandraten dynamisch abzurufen. |
| [!UICONTROL Secure Gateway URL] | Website | Die sichere URL, die verwendet wird, um über eine SSL (Secure Socket Layer) eine Verbindung zum USPS-System herzustellen und Versandraten dynamisch abzurufen. |
| [!UICONTROL Title] | Shop-Ansicht | Der Titel dieser Versandoption, wie er im Warenkorb-Checkout angezeigt wird. |
| [!UICONTROL User ID] | Website | Die Benutzer-ID Ihres USPS-Versandkontos. |
| [!UICONTROL Password] | Website | Ihr USPS Versandekonto-Passwort. |
| [!UICONTROL Mode] | Website | Bestimmt den Übertragungsmodus für Daten, die an das USPS-System gesendet werden. Zu den Optionen gehören: <br/>**`Development`**- USPS überprüft nicht, ob vom Commerce-Server empfangene Daten über SSL gesendet werden.<br/>**`Live`** - USPS überprüft, ob vom Commerce-Server empfangene Daten über eine Secure Socket Layer (SSL) gesendet werden. |

{style="table-layout:auto"}

![USPS-Verpackungseinstellungen](./assets/delivery-methods-usps-packaging.png)<!-- zoom -->

<!-- [USPS Packaging Settings](https://docs.magento.com/user-guide/shipping/usps.html) -->

| Feld | [Scope](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| _[!UICONTROL USPS packaging Settings]_ |  |  |
| [!UICONTROL Packages Request Type] | Website | Bestimmt, wie das Gewicht für Sendungen mit mehreren Paketen berechnet wird. Optionen: `Divide to equal weight (one request)` / `Use origin weight (multiple requests)` |
| [!UICONTROL Container] | Website | Legt den Container-Typ fest, der zum Verpacken von Sendungen verwendet wird. Optionen: `Variable` / `Flat Rate Box` / `Flat Rate Envelope` / `Rectangular` / Nicht rechteckig |
| [!UICONTROL Size] | Website | Legt die Option Größe auf die typische Größe des Versandpakets fest. Diese Option wirkt sich auf die Berechnung der Versandrate aus. Optionen: `Regular` / `Large` / `Oversize` |
| [!UICONTROL Machinable] | Website | Gibt an, ob das Paket maschinell verarbeitet werden kann. Diese Option wirkt sich auf die Berechnung der Versandrate aus. |
| [!UICONTROL Maximum Package Weight] | Website | Legt das maximale Gewicht fest, das ein Paket gemäß USPS haben kann. Wenn die bestellten Produkte das maximale Paketgewicht überschreiten, ist diese Versandoption nicht verfügbar. |

{style="table-layout:auto"}

![Gebühreneinstellungen für USPS Handling](./assets/delivery-methods-usps-handling-fee.png)<!-- zoom -->

<!-- [USPS Handling Fee Settings](https://docs.magento.com/user-guide/shipping/usps.html) -->

| Feld | [Scope](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| _[!UICONTROL USPS Handling Fee settings]_ |  |  |
| [!UICONTROL Calculate Handling Fee] | Website | Legt die Methode zur Berechnung der Bearbeitungsgebühr für den Versand mit Tabellensätzen fest. Optionen: <br/>**`Fixed`**- Die Bearbeitungsgebühr ist ein fester Satz.<br/>**`Percent`** - Die Bearbeitungsgebühr wird in Prozent des Bestellbetrags erhoben. |
| [!UICONTROL Handling Applied] | Website | Gibt an, ob die Bearbeitungsgebühr auf jede Bestellung oder auf jedes Paket innerhalb einer Bestellung angewendet wird. |
| [!UICONTROL Handling Fee] | Website | Legt die Handhabung fest, die im Versandratenpreis enthalten ist. Die Bearbeitungsgebühr kann als fester Betrag oder als Prozentsatz festgelegt werden. <br/><br/>**_Hinweis:_**Verwenden Sie beim Eingeben eines Prozentsatzes das Dezimalformat . `0.25` für 25 %. |

{style="table-layout:auto"}

![Zulässige USPS-Methoden](./assets/delivery-methods-usps-allowed-methods.png)<!-- zoom -->

<!-- [USPS Allowed Methods](https://docs.magento.com/user-guide/shipping/usps.html) -->

| Feld | [Scope](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| _[!UICONTROL USPS Allowed Methods]_ |  |  |
| [!UICONTROL Allowed Methods] | Website | Gibt die zulässigen Methoden für den Versand von USPS an, die Kunden angeboten werden. Die Versandkosten werden anhand der gewählten Versandart berechnet. |
| [!UICONTROL Free Method] | Website | Legt die kostenlose Versandmethode über USPS fest oder kann durch Auswahl von deaktiviert werden `None`. <br/><br/>**_Hinweis:_**Diese Versandmethode ähnelt der kostenlosen Versandmethode Ihres Geschäfts, wird jedoch als USPS-Versandoption aufgeführt und als USPS-Versand identifiziert. |
| [!UICONTROL Minimum Order Amount for Free Shipping] | Website | Legt den Mindestbestellbetrag fest, der erfüllt sein muss, um für den kostenlosen Versand qualifiziert zu sein. |
| [!UICONTROL Displayed Error Message] | Shop-Ansicht | Die Fehlermeldung, die angezeigt wird, wenn USPS aus irgendeinem Grund nicht verfügbar ist. |

{style="table-layout:auto"}

![Für USPS geltende Länder](./assets/delivery-methods-usps-countries.png)<!-- zoom -->

<!-- [USPS Applicable Countries](https://docs.magento.com/user-guide/shipping/usps.html) -->

| Feld | [Scope](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| _[!UICONTROL USPS Applicable Countries]_ |  |  |
| [!UICONTROL Ship to Applicable Countries] | Website | Gibt die Länder an, in denen Bestellungen versendet werden können. Optionen: <br/>**`All Allowed Countries`**- Kunden aus allen [Länder](../../getting-started/store-details.md#country-options) Diese Versandmethode kann verwendet werden, wenn sie in Ihrer Store-Konfiguration angegeben ist.<br/>**`Specific Countries`** - Nach Auswahl dieser Option wird die [!UICONTROL Ship to Specific Countries] Liste angezeigt. Wählen Sie jedes Land in der Liste aus, in dem diese Versandart verwendet werden kann. |
| [!UICONTROL Show Method if Not Applicable] | Website | Steuert die Anzeige des USPS-Versands während des Checkouts. Optionen: <br/>**`Yes`**- USPS erscheint immer als Versandoption während des Checkouts, auch wenn dies nicht auf die Bestellung zutrifft.<br/>**`No`** - USPS erscheint nur dann als Versandoption beim Checkout, wenn dies auf die Bestellung zutrifft (d. h. das Bestellgewicht überschreitet den maximalen Gewichtsbetrag). |
| [!UICONTROL Debug] | Website | Bestimmt, ob ein Protokoll der Datenübertragungen zwischen Ihrem Store und USPS vom System zum Debugging gepflegt wird. Sofern kein Problem vorliegt, das verfolgt und protokolliert werden muss, sollte diese Option auf Folgendes festgelegt werden `No`. |
| [!UICONTROL Sort Order] | Website | Eine Zahl, die die Reihenfolge bestimmt, in der USPS beim Checkout mit anderen Versandmethoden aufgelistet wird. eintreten in `0` am Anfang der Liste. |

{style="table-layout:auto"}

### [!UICONTROL FedEx]

<!-- [FedEx Account Settings](https://docs.magento.com/user-guide/shipping/fedex.html) -->

#### FedEx-Kontoeinstellungen

![FedEx-Kontoeinstellungen](./assets/delivery-methods-fedex-account-settings.png){width="600" zoomable="yes"}

| Feld | [Scope](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|-------|------ |-----------------------------------------------------------------------------|
| [!UICONTROL Enabled for Checkout] | Website | Legt fest, ob FedEx für Kunden als Versandmethode während des Checkouts verfügbar ist. Optionen: `Yes` / `No` |
| [!UICONTROL Title] | Shop-Ansicht | Der Titel dieser Versandoption, wie er im Warenkorb-Checkout angezeigt wird. |
| [!UICONTROL Account ID] | Website | Ihre FedEx-Konto-ID. |
| [!UICONTROL Api Key] | Website | Ihr FedEx-Konto-API-Schlüssel. |
| [!UICONTROL Secret Key] | Website | Ihr geheimer Schlüssel für die FedEx-Konto-API. |
| [!UICONTROL Sandbox Mode] | Website | Um FedEx-Transaktionen in einer Testumgebung auszuführen, setzen Sie Sandbox Mode auf `Yes`. Optionen: `Yes` / `No`. |
| [!UICONTROL Web-Services URL] | Website | Die erforderliche URL hängt von der Einstellung des Sandbox-Modus ab. Optionen: <br/>**`Production`**- Die URL für den Zugriff auf FedEx-Web-Services, wenn der Store live ist.<br/>**`Sandbox`** - Die URL für den Zugriff auf die Testumgebung für FedEx-Web-Services. |

{style="table-layout:auto"}

#### FedEx-Verpackungseinstellungen

![FedEx-Verpackung](./assets/delivery-methods-fedex-packaging.png){width="600" zoomable="yes"}

| Feld | [Scope](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Pickup Type] | Website | Wählen Sie aus der Liste die Aufnahmemethode aus: <br/>**`DropOff at Fedex Location`**- (Standard) Zeigt an, dass Sie Sendungen an Ihrer lokalen FedEx-Station abgeben.<br/>**`Contact Fedex to Schedule`** - Zeigt an, dass Sie FedEx kontaktieren, um eine Abholung anzufordern. <br/>**`Use Scheduled Pickup`**- Zeigt an, dass die Sendung im Rahmen einer regelmäßigen geplanten Abholung abgeholt wird.<br/>**`On Call`** - Zeigt an, dass die Abholung durch einen Aufruf von FedEx geplant wird. <br/>**`Package Return Program`**- Zeigt an, dass die Sendung vom FedEx Ground Package Retouren-Programm aufgenommen wird.<br/>**`Regular Stop`** - Zeigt an, dass die Sendung zum regulären Abholplan abgeholt wird. <br/>**`Tag`**- Gibt an, dass die Sendungsabholung spezifisch für eine Anfrage zur Abholung von Express-Tags oder Bound-Tag-Aufrufen ist. Dies gilt nur für einen Rückversand-Aufkleber. |
| [!UICONTROL Packages Request Type] | Website | Bestimmt, wie das Gewicht für Sendungen mit mehreren Paketen berechnet wird. Optionen: `Divide to equal weight (one request)` / `Use origin weight (multiple requests)` |
| [!UICONTROL Packaging] | Website | Wählen Sie aus der Liste den Container-Typ aus, den Sie normalerweise zum Verpacken von Produkten verwenden, die in Ihrem Geschäft bestellt wurden. |
| [!UICONTROL Weight Unit] | Website | Die für das Package-Gewicht verwendete Einheit. Optionen: `Pounds` (Standard) / `Kilograms` |
| [!UICONTROL Maximum Package Weight] | Website | Der Standardwert für FedEx beträgt 150 Pfund. Wenden Sie sich bezüglich des maximal unterstützten Gewichts an Ihren Spediteur. Es wird empfohlen, den Standardwert zu verwenden, es sei denn, Sie haben besondere Vereinbarungen mit FedEx. |

{style="table-layout:auto"}

#### Gebühreneinstellungen für FedEx-Bearbeitung

![Bearbeitungsgebühr für FedEx](./assets/delivery-methods-fedex-handling-fee.png){width="600" zoomable="yes"}

| Feld | [Scope](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Calculate Handling Fee] | Website | Bestimmt die Methode zur Berechnung der Bearbeitungsgebühren. Optionen: `Fixed Fee` / `Percentage` <br/><br/>**_Hinweis:_**Die Bearbeitungsgebühr ist optional und wird als zusätzliche Gebühr angezeigt, die zu den Versandkosten von FedEx hinzugerechnet wird. |
| [!UICONTROL Handling Applied] | Website | Legt fest, wie Bearbeitungsgebühren angewendet werden. Optionen: `Per Order` / `Per Package` |
| [!UICONTROL Handling Fee] | Website | Gibt den Betrag an, der als Bearbeitungsgebühr in Rechnung gestellt wird, basierend auf der Methode zur Berechnung des Betrags. Wenn die Gebühr auf einer festen Gebühr basiert, geben Sie den Betrag als Dezimalzahl ein, z. B. `4.90`. Wenn die Bearbeitungsgebühr auf einem Prozentsatz der Bestellung basiert, geben Sie den Betrag als Prozentsatz ein. Um beispielsweise sechs Prozent der Bestellung zu berechnen, geben Sie den Wert wie folgt ein `.06`. |

{style="table-layout:auto"}

#### FedEx-Versandmethoden

![FedEx-Versandmethoden](./assets/delivery-methods-fedex-delivery-methods.png){width="600" zoomable="yes"}

| Feld | [Scope](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Residential Delivery] | Website | Legen Sie eine der folgenden Einstellungen fest, je nachdem, ob Sie Business-to-Consumer (B2C) oder Business-to-Business (B2B) verkaufen: <br/>**`Yes`**- Für B2C-Sendungen<br/>**`No`** - Für B2B-Sendungen |
| [!UICONTROL Allowed Methods] | Website | Wählen Sie aus der Liste die von Ihnen unterstützten Versandmethoden aus. Die Methoden hängen von Ihrem FedEx-Konto, der Häufigkeit und Größe Ihrer Sendungen und davon ab, ob Sie internationale Sendungen zulassen. Als Händler könnten Sie sich dafür entscheiden, nur Bodentransport anzubieten. |
| [!UICONTROL Hub ID] | Website | Eine von FedEx bereitgestellte ID, die mit dem [!DNL Smart Post] -Methode. |
| [!UICONTROL Free Method] | Website | Wählen Sie aus der Liste die Versandart aus, die Sie für Angebote des kostenlosen Versands bevorzugen. <br/><br/>**_Hinweis:_**Diese Versandart ähnelt der regulären kostenlosen Versandart, wird jedoch in den FedEx Versandoptionen aufgeführt und wird als FedEx Versand bezeichnet. |
| [!UICONTROL Free Shipping Amount Threshold] | Website | Bestimmt, ob ein Mindestbestellbetrag für den kostenlosen Versand erforderlich ist. Optionen: <br/>**`Enable`**- Ermöglicht den kostenlosen Versand von FedEx für Bestellungen, die den Mindestbetrag erreichen.<br/>**`Disable`** - Deaktiviert kostenlosen FedEx-Versand mit Mindestbestellung. |
| [!UICONTROL Free Shipping Amount Threshold] | Website | Gibt den Mindestbestellungsbetrag an, der für den kostenlosen Versand erforderlich ist. |
| [!UICONTROL Displayed Error Message] | Shop-Ansicht | Die Meldung, die angezeigt wird, wenn FedEx aus irgendeinem Grund nicht verfügbar ist. Sie können die Standardmeldung verwenden oder eine andere eingeben. |

{style="table-layout:auto"}

#### Für FedEx geltende Ländereinstellungen

![Für die FedEX geltende Länder](./assets/delivery-methods-fedex-applicable-countries.png){width="600" zoomable="yes"}

| Feld | [Scope](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Ship to Applicable Countries] | Website | Gibt die Länder an, in denen Ihre Kunden per FedEx versenden können. Optionen: <br/>**`All Allowed Countries`**- Kunden aus allen [Länder](../../getting-started/store-details.md#country-options) Diese Versandmethode kann verwendet werden, wenn sie in Ihrer Store-Konfiguration angegeben ist.<br/>**`Specific Countries`** - Nach Auswahl dieser Option wird die [!UICONTROL Ship to Specific Countries] Liste angezeigt. Wählen Sie jedes Land in der Liste aus, in dem diese Versandart verwendet werden kann. |
| [!UICONTROL Ship to Specific Countries] | Website | Gibt die spezifischen Länder an, in denen Ihre Kunden per FedEx versenden können. |
| [!UICONTROL Debug] | Website | Bestimmt, ob das System ein Protokoll der Datenübertragungen zwischen Ihrem Store und FedEx zum Debugging verwaltet. Sofern kein Problem vorliegt, das verfolgt und protokolliert werden muss, sollte diese Option auf Folgendes festgelegt werden `No`. |
| [!UICONTROL Show Method if Not Applicable] | Website | Bestimmt, wann FedEx während des Checkouts als Versandmethode angezeigt wird. Optionen: <br/>**`Yes`**- Die Versandoption FedEx wird in der Liste der Versandmethoden angezeigt, unabhängig davon, ob die Bestellung für die Verwendung geeignet ist.<br/>**`No`** - Die Versandoption FedEx wird nicht in der Liste der Versandmethoden angezeigt, wenn sie nicht auf die Bestellung anwendbar ist (z. B. wenn das Bestellgewicht den maximalen Gewichtsbetrag überschreitet). |
| [!UICONTROL Sort Order] | Website | Eine Zahl, die die Reihenfolge bestimmt, in der FedEx beim Checkout mit anderen Versandmethoden aufgelistet wird. eintreten in `0` am Anfang der Liste. |

{style="table-layout:auto"}

### [!UICONTROL DHL]

![DHL-Kontoeinstellungen](./assets/delivery-methods-dhl-account-settings.png)<!-- zoom -->

<!-- [DHL Account Settings](https://docs.magento.com/user-guide/shipping/dhl.html) -->

| Feld | [Scope](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| _[!UICONTROL DHL Account Settings]_ |  |  |
| [!UICONTROL Enabled for Checkout] | Website | Bestimmt, ob DHL während des Checkouts für Kunden als Versandmethode verfügbar ist. Optionen: `Yes` / `No` |
| [!UICONTROL Title] | Shop-Ansicht | Der Titel dieser Versandmethode, wie er während des Checkouts angezeigt wird. |
| [!UICONTROL Gateway URL] | Website | Normalerweise können Sie die Standard-Gateway-URL akzeptieren. Wenn Ihnen jedoch DHL eine alternative URL gegeben hat, geben Sie den Wert in dieses Feld ein. |
| [!UICONTROL Access ID] | Website | Ihre DHL-Versand-Konto-Zugriffs-ID. |
| [!UICONTROL Password] | Website | Ihr DHL-Versandkonto-Passwort. |
| [!UICONTROL Account Number] | Website | Ihre DHL-Spediteurkontonummer. |

{style="table-layout:auto"}

![DHL-Paketeinstellungen](./assets/delivery-methods-dhl-package-settings.png)<!-- zoom -->

<!-- [DHL Package Settings](https://docs.magento.com/user-guide/shipping/dhl.html) -->

| Feld | [Scope](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| _[!UICONTROL DHL Package Settings]_ |  |  |
| [!UICONTROL Calculate Handling Fee] | Website | Die Bearbeitungsgebühr ist optional und wird als zusätzliche Gebühr zu den DHL Versandkosten angezeigt. Wählen Sie aus der Liste die Methode aus, die Sie zur Berechnung der Bearbeitungsgebühren verwenden möchten. Optionen: Feste Gebühr / Prozentsatz. |
| [!UICONTROL Handling Applied] | Website | Wählen Sie aus der Liste aus, wie die Bearbeitungsgebühren angewendet werden sollen. Optionen: `Per Order` / `Per Package` |
| Bearbeitungsgebühr | Website | Geben Sie den Betrag ein, der für eine Bearbeitungsgebühr in Rechnung gestellt werden soll. Dieser Betrag basiert auf der Methode, die Sie zur Berechnung des Betrags gewählt haben. Wenn die Gebühr beispielsweise auf einer festen Gebühr basiert, geben Sie den Betrag als Dezimalzahl ein, z. B. `4.90`. Wenn die Bearbeitungsgebühr jedoch auf einem Prozentsatz der Bestellung basiert, geben Sie den Betrag als Prozentsatz ein. Wenn Sie beispielsweise sechs Prozent der Bestellung berechnen, geben Sie den Wert wie folgt ein `.06`. |
| [!UICONTROL Divide Order Weight] | Shop-Ansicht | Bestimmt, ob das Gewicht einer Bestellung über 70 kg in kleinere Einheiten aufgeteilt werden kann, um eine genaue Versandgebühr zu gewährleisten. Optionen: `Yes` / `No` |
| [!UICONTROL Weight Unit] | Shop-Ansicht | Bestimmt die Maßeinheit für das Gewicht, die in Versandberechnungen verwendet wird. Optionen: `Pounds` / `Kilograms` |
| [!UICONTROL Size] | Shop-Ansicht | Bestimmt die Größe des Pakets. Optionen: <br/>**`Regular`**- Packstücke, die nach den DHL-Standardverpackungsmethoden geliefert werden. In der [!UICONTROL Allowed Methods] Liste, wählen Sie jede Verpackungsmethode, die zum Versand von Produkten aus Ihrem Geschäft verwendet wird.<br/>**`Specific`** - Wenn die ausgelieferten Pakete benutzerdefinierte Dimensionen aufweisen, führen Sie folgende Schritte aus: [!UICONTROL Height (cm)] / [!UICONTROL Depth (cm)] / [!UICONTROL Width (cm)] |

{style="table-layout:auto"}

![Zulässige DHL-Methoden](./assets/delivery-methods-dhl-allowed-methods.png)<!-- zoom -->

<!-- DHL Allowed Methods](https://docs.magento.com/user-guide/shipping/dhl.html) -->

| Feld | [Scope](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| _[!UICONTROL DHL allowed methods]_ |  |  |
| [!UICONTROL Allowed Methods] | Website | Wählen Sie in der Liste jede unterstützte Versandmethode aus. |
| [!UICONTROL Ready Time] | Website | Gibt an, wann das Paket nach dem Absenden einer Bestellung zur Abholung bereit ist (in Stunden). |
| [!UICONTROL Displayed Error Message] | Shop-Ansicht | Diese Meldung erscheint, wenn DHL aus irgendeinem Grund nicht mehr verfügbar ist. Sie können die Standardmeldung verwenden oder eine eigene Nachricht eingeben. |
| [!UICONTROL Free Method] |  | Diese Versandart ähnelt der regulären kostenlosen Versandart, wird jedoch in den DHL Versandoptionen aufgeführt und wird als DHL Versand bezeichnet. Wählen Sie in der Liste die Versandart aus, die Sie für Angebote des kostenlosen Versands bevorzugen. |
| [!UICONTROL Free Shipping with Minimum Order Amount] | Website | Legen Sie einen der folgenden Werte fest: <br/>**`Enable`**- um den kostenlosen DHL-Versand für Bestellungen zu ermöglichen, die den Mindestbetrag erreichen.<br/>**`Disable`** - Um nicht kostenlosen DHL-Versand mit Mindestbestellung anzubieten. |
| [!UICONTROL Minimum Order Amount for Free Shipping] | Website | Wenn Sie [!UICONTROL Free Shipping with Minimum Order], geben Sie den Wert für den Mindestbestellbetrag in das Feld ein. |

{style="table-layout:auto"}

![Für DHL geltende Länder](./assets/delivery-methods-dhl-applicable-countries.png)<!-- zoom -->

<!-- [DHL Applicable Countries](https://docs.magento.com/user-guide/shipping/dhl.html) -->

| Feld | [Scope](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| _[!UICONTROL DHL applicable countries]_ |  |  |
| [!UICONTROL Ship to Applicable Countries] | Website | Gibt an, welches Land Kundinnen und Kunden diese Versandart verwenden dürfen. Optionen: <br/>**Alle zulässigen Länder** - Alle zulässigen Länder können die kostenlose Versandmethode verwenden. Die zulässigen Länder werden im Feld [!UICONTROL General] Konfigurationsseite. <br/>**Bestimmte Länder** - Beschränkt diese Versandoption auf die im Verzeichnis „Schiff in Bestimmte Länder“ angegebenen Länder. |
| [!UICONTROL Ship to Specific Countries] | Website | Gibt die Länder an, in die DHL-Sendungen gesendet werden können. Diese Liste ausgewählter Länder wird verwendet, wenn `Specific Countries` wird in der [!UICONTROL Ship to Applicable Countries] Option. |
| [!UICONTROL Show Method if Not Applicable] | Website | Bestimmt, wann DHL während des Checkouts als Versandmethode angezeigt wird. Optionen: <br/>**`Yes`**- DHL erscheint immer als Versandoption während des Checkouts, auch wenn dies nicht auf die Bestellung zutrifft.<br/>**`No`** - DHL erscheint nur dann als Versandoption beim Checkout, wenn es auf die Bestellung zutrifft (d.h. das Bestellgewicht überschreitet die maximale Gewichtsmenge). |
| [!UICONTROL Debug] | Website | Erstellt eine Protokolldatei mit Fehlerinformationen. |
| [!UICONTROL Sort Order] | Website | Eine Zahl, die die Reihenfolge bestimmt, in der DHL beim Checkout mit anderen Versandmethoden aufgelistet wird. Um sie an den Anfang der Liste zu setzen, geben Sie Folgendes ein `0`. |

{style="table-layout:auto"}
