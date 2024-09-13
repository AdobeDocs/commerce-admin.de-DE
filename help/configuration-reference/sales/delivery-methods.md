---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Delivery Methods]'
description: Überprüfen Sie die Konfigurationseinstellungen auf der Seite [!UICONTROL Sales] &gt; [!UICONTROL Delivery Methods] des Commerce-Administrators.
exl-id: 159b76a8-3676-4692-9cd6-18947bda4666
feature: Configuration, Shipping/Delivery
source-git-commit: 8e80e6f33ede2f49f320394905b9d1a964cf8331
workflow-type: tm+mt
source-wordcount: '3792'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Delivery Methods]

{{config}}

## [!UICONTROL Basic Delivery Methods]

### [!UICONTROL Flat Rate]

![Pauschalrate](./assets/delivery-methods-flat-rate.png)<!-- zoom -->

<!-- [Flat Rate](https://docs.magento.com/user-guide/shipping/shipping-flat-rate.html) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enabled] | Webseite | Wenn diese Option aktiviert ist, wird der Pauschalsatz im Abschnitt _Geschätzter Versand und Steuern_ des Warenkorbs und im Abschnitt _Versand_ beim Checkout als Option angezeigt. Optionen: `Yes` / `No` |
| [!UICONTROL Title] | Store-Ansicht | Der Name, der für diese Versandmethode beim Checkout verwendet wird. |
| [!UICONTROL Method Name] | Store-Ansicht | Ein Name, der die Berechnungsmethode beschreibt, mit der eine Versandschätzung erstellt wird. Der Name der Methode wird neben der berechneten geschätzten Rate im Warenkorb angezeigt. Der Standardwert ist `Fixed`. |
| [!UICONTROL Type] | Webseite | Beschreibt die Art der Berechnung, die zur Bestimmung des Pauschalsatzes verwendet wird. Optionen: <br/>**`None`**- Es wird keine Berechnung verwendet. Legt den Pauschalsatz auf null fest, was dem kostenlosen Versand entspricht.<br/>**`Per Order`** - berechnet einen Pauschalpreis für die gesamte Bestellung. <br/>**`Per Item`**- berechnet für jeden Artikel im Warenkorb einen separaten Pauschalsatz. Der Prozentsatz wird mit der Anzahl der Artikel im Warenkorb multipliziert, auch wenn die Gesamtmenge eine Kombination verschiedener Artikel enthält. |
| [!UICONTROL Price] | Webseite | Der Preis, den Sie dem Kunden für den Pauschalversand berechnen. |
| [!UICONTROL Calculate Handling Fee] | Webseite | Bestimmt, wie die Bearbeitungsgebühr berechnet wird (sofern vorhanden). Optionen: `Fixed` / `Percent` |
| [!UICONTROL Handling Fee] | Webseite | Geben Sie den Betrag an, der für eine Bearbeitungsgebühr in Rechnung gestellt werden soll, basierend auf der Methode, die Sie zur Berechnung des Betrags ausgewählt haben. Wenn die Gebühr beispielsweise auf einer festen Gebühr basiert, geben Sie den Betrag als Dezimalzahl an, z. B. 4,90. Wenn die Bearbeitungsgebühr jedoch auf einem Prozentsatz der Bestellung basiert, geben Sie den Betrag als Prozentsatz an. Wenn Sie beispielsweise sechs Prozent der Bestellung aufladen, geben Sie den Wert als `.06` ein. |
| [!UICONTROL Displayed Error Message] | Store-Ansicht | Eine Meldung, die angezeigt wird, wenn ein Kunde die Pauschalrate auswählt, die -Methode jedoch aus irgendeinem Grund nicht verfügbar ist. |
| [!UICONTROL Ship to Applicable Countries] | Webseite | Identifiziert die Länder, in denen Sie Pauschalreisen anbieten. Optionen: <br/>**`All Allowed Countries`**- Kunden aus jedem Land, das in der Store-Konfiguration angegeben ist, können den Pauschalpreis-Versand verwenden.<br/>**`Specific Countries`** - Kunden aus nur bestimmten Ländern können den Pauschalpreis-Versand verwenden. |
| [!UICONTROL Ship to Specific Countries] | Webseite | Identifiziert jedes Land, in dem Kunden Pauschalsendungen verwenden können. |
| [!UICONTROL Show Method if Not Applicable] | Webseite | Bestimmt, ob die Pauschalrate beim Checkout als Option angezeigt wird, wenn die Methode nicht auf den Kauf angewendet wird. Optionen: `Yes` / `No` |
| [!UICONTROL Sort Order] | Webseite | Eine Zahl, die bestimmt, in welcher Reihenfolge die Pauschalrate angezeigt wird, wenn sie beim Checkout mit anderen Versandmethoden aufgeführt wird. |

{style="table-layout:auto"}

### [!UICONTROL Free Shipping]

![Kostenloser Versand](./assets/delivery-methods-free-shipping.png)<!-- zoom -->

<!-- [Free Shipping](https://docs.magento.com/user-guide/shipping/shipping-free.html) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enabled] | Webseite | Wenn diese Option aktiviert ist, wird beim Checkout im Abschnitt Versand als Option angezeigt. Optionen: `Yes` / `No` |
| [!UICONTROL Title] | Store-Ansicht | Der Name, der für diese Versandmethode beim Checkout verwendet wird. |
| Name der Methode | Store-Ansicht | Ein Name, der die Berechnungsmethode beschreibt, mit der eine Versandschätzung erstellt wird. Der Name der Methode wird neben der berechneten geschätzten Rate im Warenkorb angezeigt. Der Standardwert ist `Free`. |
| Mindestauftragsbetrag | Webseite | Der Mindestkauf, der erforderlich ist, um kostenlosen Versand auf eine Bestellung anzuwenden. |
| Steuern auf Betrag einschließen | Webseite | Bestimmt, ob die Steuer in der Berechnung des Mindestauftragsbetrags enthalten ist. Optionen: <br/>**Ja** - Die Steuer wird bei der Berechnung des Mindestauftragsbetrags (Zwischensumme + Steuern - Rabatt) berücksichtigt.<br/>**Nein** - Die Steuer ist bei der Berechnung des Mindestauftragsbetrags (Zwischensumme - Rabatt) nicht inbegriffen. |
| Angezeigte Fehlermeldung | Store-Ansicht | Eine Meldung, die angezeigt wird, wenn ein Kunde sich für kostenlosen Versand entscheidet, die -Methode jedoch aus irgendeinem Grund nicht verfügbar ist. |
| Schiff in die betreffenden Länder | Webseite | Identifiziert die Länder, in denen Sie kostenlosen Versand anbieten. Optionen: <br/>**Alle zugelassenen Länder** - Kunden aus jedem Land, das in der Store-Konfiguration angegeben ist, können die kostenlose Lieferung verwenden. <br/>**Bestimmte Länder** - Kunden aus nur bestimmten Ländern können den kostenlosen Versand verwenden. |
| Schiff in bestimmte Länder | Webseite | Identifiziert jedes Land, in dem Kunden kostenlosen Versand verwenden können. |
| Methode anzeigen, falls nicht zutreffend | Webseite | Bestimmt, ob beim Checkout als Option der kostenlose Versand angezeigt wird, wenn die Methode nicht auf den Kauf zutrifft. Optionen: `Yes` / `No` |
| [!UICONTROL Sort Order] | Webseite | Eine Zahl, die bestimmt, in welcher Reihenfolge beim Checkout der kostenlose Versand angezeigt wird, wenn er mit anderen Versandmethoden aufgeführt wird. |

{style="table-layout:auto"}

### [!UICONTROL Table Rates]

![Tabellenraten](./assets/delivery-methods-table-rates.png)<!-- zoom -->

<!-- [Table Rates](https://docs.magento.com/user-guide/shipping/shipping-table-rate.html) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enabled] | Webseite | Wenn diese Option aktiviert ist, werden die Tabellenraten im Abschnitt Geschätzter Versand und Steuern des Warenkorbs sowie im Abschnitt Versand während des Checkout angezeigt. Optionen: `Yes` / `No` |
| [!UICONTROL Title] | Store-Ansicht | Der Name, der für diese Versandmethode beim Checkout verwendet wird. |
| Name der Methode | Store-Ansicht | Ein Name, der die Berechnungsmethode beschreibt, mit der eine Versandschätzung erstellt wird. Der Name der Methode wird neben der berechneten geschätzten Rate im Warenkorb angezeigt. Der Standardwert ist `Table Rate`. |
| [!UICONTROL Condition] | Webseite | Bestimmt die Bedingung, auf der die Berechnung basiert. Das Format der hochgeladenen CSV-Datei ist für jede Bedingung spezifisch. Optionen: `Weight vs. Destination` / `Price vs. Destination` / `# of Items vs. Destination` |
| [!UICONTROL Include Virtual Products in Price Calculation] | Webseite | Bestimmt, ob virtuelle Produkte, die nicht versandpflichtig sind, in Preisberechnungen für Tabellen enthalten sind. |
| [!UICONTROL Calculate Handling Fee] | Webseite | Bestimmt, wie die Bearbeitungsgebühr berechnet wird (sofern vorhanden). Optionen: `Fixed` / `Percent` |
| [!UICONTROL Handling Fee] | Webseite | Die Höhe der Gebühren, die der Versandgebühr hinzugefügt werden, um die Kosten für die Bearbeitung der Sendung zu decken. Geben Sie den Wert als Dezimalzahl ein. Wenn die Gebühr beispielsweise auf einem Prozentsatz basiert, geben Sie 0,06 anstelle von 6 % ein. Geben Sie für einen festen Betrag `6.00` ein. |
| [!UICONTROL Displayed Error Message] | Store-Ansicht | Eine Meldung, die angezeigt wird, wenn ein Kunde Tabellenraten auswählt, die -Methode jedoch aus irgendeinem Grund nicht verfügbar ist. |
| [!UICONTROL Ship to Applicable Countries] | Webseite | Identifiziert die Länder, in denen der Versand zum Tabellenpreis angeboten wird. Optionen: <br/>**`All Allowed Countries`**- Kunden aus jedem Land, das in der Store-Konfiguration angegeben ist, können den Versand der Tabellenrate verwenden.<br/>**`Specific Countries`** - Kunden aus nur bestimmten Ländern können den Versand der Tabellenpreise nutzen. |
| [!UICONTROL Ship to Specific Countries] | Webseite | Identifiziert jedes Land, in dem Kunden den Tabellenpreis-Versand verwenden können. |
| [!UICONTROL Show Method if Not Applicable] | Webseite | Bestimmt, ob die Tabellenraten beim Checkout als Option angezeigt werden, wenn die Methode nicht auf den Kauf angewendet wird. Optionen: `Yes` / `No` |
| [!UICONTROL Sort Order] | Webseite | Eine Zahl, die bestimmt, in welcher Reihenfolge die Tabellenraten angezeigt werden, wenn sie beim Checkout mit anderen Versandmethoden aufgeführt werden. |

{style="table-layout:auto"}

### [!UICONTROL In-Store Delivery]

![ In-Store-Bereitstellung](./assets/delivery-methods-in-store-delivery.png)<!-- zoom -->

<!-- [In-Store Delivery](https://docs.magento.com/user-guide/shipping/shipping-in-store-delivery.html) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enabled] | Webseite | Wenn diese Option aktiviert ist, kann der In-Store-Versand als Option im Abschnitt _Geschätzter Versand und Steuern_ des Warenkorbs und im Abschnitt _Versand_ beim Checkout angezeigt werden. Optionen: `Yes` / `No` |
| [!UICONTROL Method Name] | Store-Ansicht | Ein Name, der die In-Store-Abholfunktion als Versandmethode angibt. Dieser Wert wird als Titel eines Tabs oben auf der Seite &quot;Versandkasse&quot;und in der Tabelle der verfügbaren Versandmethoden am unteren Rand derselben Seite angezeigt. Der Standardwert ist `In-store Delivery`. |
| [!UICONTROL Title] | Store-Ansicht | Der Name, der für diese Versandmethode beim Checkout verwendet wird. |
| [!UICONTROL Price] | Webseite | Der Preis, den Sie dem Kunden für eine In-store-Abholung berechnen. |
| [!UICONTROL Search Radius] | Webseite | Der Radius in km, der bei der Suche nach Auffangstellen verwendet werden soll. |
| [!UICONTROL Displayed Error Message] | Store-Ansicht | Eine Meldung, die angezeigt wird, wenn ein Kunde die In-Store-Abholung auswählt, die Versandmethode jedoch nicht verfügbar ist. |

{style="table-layout:auto"}

## [!UICONTROL Carriers]

### [!UICONTROL UPS]

{{ups-api}}

![UPS REST Account Settings](./assets/delivery-methods-ups1.png)<!-- zoom -->

![UPS XML-Kontoeinstellungen](./assets/delivery-methods-ups1.png)<!-- zoom -->

<!-- [UPS REST Account Settings](https://docs.magento.com/user-guide/shipping/ups.html) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Enabled for Checkout] | Webseite | Bestimmt, ob UPS für Kunden als Versandmethode während des Checkout verfügbar ist. Optionen: `Yes` / `No` |
| [!UICONTROL Enabled for RMA] | Webseite | Stellt fest, ob UPS für Kunden als Versandmethode für eine RMA verfügbar ist. Optionen: `Yes` / `No` |
| _[!UICONTROL UPS Account Settings]_ |  |  |
| [!UICONTROL Live Account] | Store-Ansicht | Gibt an, dass das United Parcel Service-Konto aktiv ist. Optionen: `Yes` / `No` |
| [!UICONTROL Title] | Store-Ansicht | Der Name, der für diese Versandmethode beim Checkout verwendet wird. |
| _[!UICONTROL UPS REST Account Settings]_ |  |  |
| [!UICONTROL Gateway URL] | Webseite | Für den UPS REST-Dienst werden die folgenden URLs angezeigt, die zur Übertragung von JSON-Daten erforderlich sind: Gateway-URL, Tracking-URL, Versand-URL. Verwenden Sie entweder Sandbox- oder Produktions-Endpunkte gemäß der Einstellung &quot;Live-Konto&quot;. |
| [!UICONTROL Mode] | Webseite | Bestimmt den Übertragungsmodus für Daten, die an das UPS-System gesendet werden. Optionen: <br/>**`Development`**- UPS überprüft nicht, ob vom Commerce-Server empfangene Daten über SSL gesendet werden.<br/>**`Live`** - UPS überprüft, ob vom Commerce-Server empfangene Daten über eine sichere Socketschicht (SSL) gesendet werden. |
| Benutzer-ID | Webseite | Ihre UPS Versandkonto-Client-ID. |
| [!UICONTROL Origin of the Shipment] | Webseite | (Nur UPS REST) Das Land oder die Region, aus dem bzw. in der das Produkt versandt wird. |
| [!UICONTROL Password] | Store-Ansicht | Ihr UPS Versandkonto Client Secret. |

{style="table-layout:auto"}

![UPS-Paketinformationen](./assets/delivery-methods-ups-packaging-settings.png)<!-- zoom -->

<!-- [UPS Package Information](https://docs.magento.com/user-guide/shipping/ups.html) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| _[!UICONTROL UPS Negotiated Rate Settings]_ |  |  |
| [!UICONTROL Enable Negotiated Rates] | Webseite | (Nur UPS REST) Aktiviert/deaktiviert Sonderpreise gemäß Ihrer Vereinbarung mit UPS. Optionen: `Yes` / `No` |
| [!UICONTROL Packages Request Type] | Webseite | Bestimmt, wie die Gewichtung für Sendungen mit mehreren Packages berechnet wird. Optionen: `Divide to equal weight (one request)` / `Use origin weight (multiple requests)` |
| [!UICONTROL Shipper Number] | Webseite | (Nur UPS REST) Die sechsstellige UPS Shipper Number ist erforderlich, damit auf die ausgehandelten Tarife verwiesen wird. |
| [!UICONTROL Container] | Webseite | Legt den Behältertyp fest, der zum Verpacken von Sendungen verwendet wird. Optionen: `Customer Packaging` / `UPS Letter Envelope` / `Customer Packaging` / `UPS Letter Envelope` / `UPS Tube` / `UPS Express Box` / `UPS Worldwide 25 kilo` / `UPS Worldwide 10 kilo` |
| [!UICONTROL Weight Unit] | Webseite | Legt die Standardmaßeinheit für die Produktgewichtung in Ihrem Geschäft fest. Weitere Informationen finden Sie unter [Dimensional weight](../../stores-purchase/carriers.md#dimensional-weight) . |
| [!UICONTROL Tracking URL] | Webseite | (Nur UPS REST) Die UPS-URL, die zum Tracking von Paketen verwendet wird. Verwenden Sie `https://onlinetools.ups.com/api/track` für die Produktion ODER `https://wwwcie.ups.com/api/track` für die Sandbox-Einrichtung. |
| [!UICONTROL Destination Type] | Webseite | Legt den standardmäßigen Versandzieltyp fest. Optionen: `Business` / `Residential` |
| [!UICONTROL Maximum Package Weight] | Webseite | Legt die maximale Gewichtung fest, die ein Paket gemäß den UPS-Vorgaben erhalten kann. Wenn die bestellten Produkte die maximale Paketgewichtung überschreiten, ist diese Versandoption nicht verfügbar. Gemäß [UPS.com](https://www.ups.com/us/en/global.page) dürfen Pakete nicht mehr als 150 lbs (70 kg) betragen. Wenden Sie sich an Ihren Versandunternehmen, um das Höchstgewicht zu überprüfen. |
| [!UICONTROL Pickup Method] | Webseite | Legt die UPS-Erfassungsmethode fest. Optionen: `Regular Daily Pickup` / `On Call Air` / `One Time Pickup` / `Letter Center` / `Customer Counter` |
| [!UICONTROL Minimum Package Weight] | Webseite | Legt die Mindestgewichtung fest, die ein Paket gemäß UPS aufweisen kann. Wenn die bestellten Produkte weniger als die Mindestverpackungsgewichtung wiegen, ist diese Versandoption nicht verfügbar. Um das Mindestgewicht zu überprüfen, fragen Sie bei Ihrem Versandunternehmen nach. |
| [!UICONTROL Calculate Handling Fee] | Webseite | Legt die Methode zur Berechnung der Bearbeitungsgebühr für den Versand von Tabellen fest. Optionen: <br>**`Fixed`**- Die Bearbeitungsgebühr ist ein Festpreis.<br>**`Percent`** - Die Bearbeitungsgebühr wird als Prozentsatz des Bestellbetrags angewendet. |
| [!UICONTROL Handling Applied] | Webseite | Gibt an, ob die Bearbeitungsgebühr auf jede Bestellung oder auf jedes Paket innerhalb einer Bestellung angewendet wird. |
| [!UICONTROL Handling Fee] | Webseite | Legt die Handhabung fest, die im Versandpreis enthalten ist. Die Bearbeitungsgebühr kann als fester Betrag oder Prozentsatz festgelegt werden. <br/><br/>**_Hinweis:_**Wenn Sie einen Prozentwert eingeben, verwenden Sie das Dezimalformat `0.25` für 25 %. |

{style="table-layout:auto"}

![Zulässige UPS-Methoden](./assets/delivery-methods-ups-allowed-methods.png)<!-- zoom -->

<!-- [UPS Allowed Methods](https://docs.magento.com/user-guide/shipping/ups.html) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| _[!UICONTROL UPS allowed methods]_ |  |  |
| [!UICONTROL Allowed Methods] | Webseite | Gibt die zulässigen Versandmethoden für UPS an, die Kunden angeboten werden. Die Versandkosten werden nach der gewählten Versandmethode berechnet. |
| [!UICONTROL Free Method] | Webseite | Gibt die Methode an, die für die kostenlose Versandmethode über UPS verwendet wird. Um den kostenlosen Versand zu deaktivieren, wählen Sie &quot;Keine&quot;. <br/><br/>**_Hinweis:_**Diese Methode ähnelt dem einfachen [kostenlosen Versand](../../stores-purchase/shipping-free.md), erscheint jedoch beim Checkout als UPS-Versandoption. |
| [!UICONTROL Free Shipping Amount Threshold] | Webseite | Bestimmt, ob der kostenlose Versand angewendet wird, wenn der Bestellbetrag die Schwelle für den kostenlosen Versand erreicht. Optionen: `Enable` / `Disable` |
| [!UICONTROL Free Shipping Amount Threshold] | Webseite | Legt den Mindestgesamtbetrag fest, den eine Bestellung erreichen muss, um für den kostenlosen Versand infrage zu kommen. |
| [!UICONTROL Displayed Error Message] | Store-Ansicht | Die Fehlermeldung wird angezeigt, wenn diese Versandmethode aus irgendeinem Grund nicht verfügbar ist. |

{style="table-layout:auto"}

![Gültige UPS-Länder und andere Einstellungen](./assets/delivery-methods-ups-ship-to.png)<!-- zoom -->

<!-- [UPS Applicable Countries and Other Settings](https://docs.magento.com/user-guide/shipping/ups.html) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| _[!UICONTROL UPS Applicable countries and other Settings]_ |  |  |
| [!UICONTROL Ship to Applicable Countries] | Webseite | Gibt an, welches Land Kunden diese Versandmethode verwenden dürfen. Optionen: <br/>**`All Allowed Countries`**- Kunden aus allen in Ihrer Store-Konfiguration angegebenen [Ländern](../../getting-started/store-details.md#country-options) können diese Versandmethode verwenden.<br/>**`Specific Countries`** - Nach Auswahl dieser Option wird die Liste [!UICONTROL Ship to Specific Countries] angezeigt. Wählen Sie jedes Land in der Liste aus, in dem diese Versandmethode verwendet werden kann. |
| [!UICONTROL Show Method if Not Applicable] | Webseite | Bestimmt, ob UPS beim Checkout immer als Versandoption angezeigt wird. Optionen: <br/>**`Yes`**- UPS wird beim Checkout immer als Versandoption angezeigt, auch wenn dies nicht für die Bestellung gilt.<br/>**`No`** - UPS wird beim Checkout nur dann als Versandoption angezeigt, wenn es auf die Bestellung anwendbar ist. (Wenn beispielsweise die Bestellgewichtung die maximale Gewichtung überschreitet.) |
| [!UICONTROL Debug] | Webseite | Gibt an, ob Datenübertragungen zwischen Ihrem Store und UPS zum Debugging im System protokolliert werden. Sofern kein Problem vorliegt, das verfolgt und protokolliert werden muss, sollte diese Option auf `No` gesetzt werden. |
| [!UICONTROL Sort Order] | Webseite | Eine Zahl, die bestimmt, in welcher Reihenfolge UPS beim Checkout mit anderen Versandmethoden angezeigt wird. Geben Sie oben in der Liste `0` ein. |

{style="table-layout:auto"}

### [!UICONTROL USPS]

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| Aktiviert für Kasse | Webseite | Stellt fest, ob USPS für Kunden als Versandmethode beim Checkout verfügbar ist. Optionen: `Yes` / `No` |
| _[!UICONTROL USPS Account Settings]_ |  |  |
| [!UICONTROL Gateway URL] | Webseite | Die URL, über die eine Verbindung zum USPS-System hergestellt wird, um Versandraten dynamisch abzurufen. |
| [!UICONTROL Secure Gateway URL] | Webseite | Die sichere URL, die verwendet wird, um über eine sichere Socketschicht (SSL) eine Verbindung zum USPS-System herzustellen, um Versandraten dynamisch abzurufen. |
| [!UICONTROL Title] | Store-Ansicht | Der Titel dieser Versandoption, wie er im Warenkorb angezeigt wird. |
| [!UICONTROL User ID] | Webseite | Ihre Benutzer-ID des USPS-Versandkontos. |
| [!UICONTROL Password] | Webseite | Ihr Passwort für Ihr USPS-Versandkonto. |
| [!UICONTROL Mode] | Webseite | Bestimmt den Übertragungsmodus für Daten, die an das USPS-System gesendet werden. Zu den Optionen gehören: <br/>**`Development`**- USPS überprüft nicht, ob vom Commerce-Server empfangene Daten über SSL gesendet werden.<br/>**`Live`** - USPS überprüft, ob vom Commerce-Server empfangene Daten über eine sichere Socketschicht (SSL) gesendet werden. |

{style="table-layout:auto"}

![USPS-Paketeinstellungen](./assets/delivery-methods-usps-packaging.png)<!-- zoom -->

<!-- [USPS Packaging Settings](https://docs.magento.com/user-guide/shipping/usps.html) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| _[!UICONTROL USPS packaging Settings]_ |  |  |
| [!UICONTROL Packages Request Type] | Webseite | Bestimmt, wie die Gewichtung für Sendungen mit mehreren Packages berechnet wird. Optionen: `Divide to equal weight (one request)` / `Use origin weight (multiple requests)` |
| [!UICONTROL Container] | Webseite | Legt den Behältertyp fest, der zum Verpacken von Sendungen verwendet wird. Optionen: `Variable` / `Flat Rate Box` / `Flat Rate Envelope` / `Rectangular` / Nicht rechteckig |
| [!UICONTROL Size] | Webseite | Legt die Option Größe auf die typische Größe des Versandpakets fest. Diese Option wirkt sich auf die Berechnung des Versandtarifs aus. Optionen: `Regular` / `Large` / `Oversize` |
| [!UICONTROL Machinable] | Webseite | Gibt an, ob das Paket von einem Computer verarbeitet werden kann. Diese Option wirkt sich auf die Berechnung des Versandtarifs aus. |
| [!UICONTROL Maximum Package Weight] | Webseite | Legt die maximale Gewichtung eines Pakets fest, die von USPS festgelegt werden kann. Wenn die bestellten Produkte die maximale Paketgewichtung überschreiten, ist diese Versandoption nicht verfügbar. |

{style="table-layout:auto"}

![USPS-Einstellungen für die Handhabung von Gebühren](./assets/delivery-methods-usps-handling-fee.png)<!-- zoom -->

<!-- [USPS Handling Fee Settings](https://docs.magento.com/user-guide/shipping/usps.html) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| _[!UICONTROL USPS Handling Fee settings]_ |  |  |
| [!UICONTROL Calculate Handling Fee] | Webseite | Legt die Methode zur Berechnung der Bearbeitungsgebühr für den Versand von Tabellen fest. Optionen: <br/>**`Fixed`**- Die Bearbeitungsgebühr ist ein Festpreis.<br/>**`Percent`** - Die Bearbeitungsgebühr wird als Prozentsatz des Bestellbetrags angewendet. |
| [!UICONTROL Handling Applied] | Webseite | Gibt an, ob die Bearbeitungsgebühr auf jede Bestellung oder auf jedes Paket innerhalb einer Bestellung angewendet wird. |
| [!UICONTROL Handling Fee] | Webseite | Legt die Handhabung fest, die im Versandpreis enthalten ist. Die Bearbeitungsgebühr kann als fester Betrag oder Prozentsatz festgelegt werden. <br/><br/>**_Hinweis:_**Verwenden Sie beim Eingeben eines Prozentbetrags das Dezimalformat `0.25` für 25 %. |

{style="table-layout:auto"}

![Zulässige USPS-Methoden](./assets/delivery-methods-usps-allowed-methods.png)<!-- zoom -->

<!-- [USPS Allowed Methods](https://docs.magento.com/user-guide/shipping/usps.html) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| _[!UICONTROL USPS Allowed Methods]_ |  |  |
| [!UICONTROL Allowed Methods] | Webseite | Gibt die zulässigen Versandmethoden für USPS an, die Kunden angeboten werden. Die Versandkosten werden nach der gewählten Versandmethode berechnet. |
| [!UICONTROL Free Method] | Webseite | Legt die kostenlose Versandmethode über USPS fest oder kann durch Auswahl von `None` deaktiviert werden. <br/><br/>**_Hinweis:_**Diese Versandmethode ähnelt der kostenlosen Versandmethode Ihres Stores, ist jedoch als USPS-Versandoption aufgeführt und als USPS-Versand gekennzeichnet. |
| [!UICONTROL Minimum Order Amount for Free Shipping] | Webseite | Legt den Mindestbestellbetrag fest, der erfüllt sein muss, um für den kostenlosen Versand infrage zu kommen. |
| [!UICONTROL Displayed Error Message] | Store-Ansicht | Die Fehlermeldung, die angezeigt wird, wenn USPS aus irgendeinem Grund nicht verfügbar ist. |

{style="table-layout:auto"}

![VERWENDETE LÄNDER](./assets/delivery-methods-usps-countries.png)<!-- zoom -->

<!-- [USPS Applicable Countries](https://docs.magento.com/user-guide/shipping/usps.html) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| _[!UICONTROL USPS Applicable Countries]_ |  |  |
| [!UICONTROL Ship to Applicable Countries] | Webseite | Gibt die Länder an, in denen Bestellungen versandt werden können. Optionen: <br/>**`All Allowed Countries`**- Kunden aus allen in Ihrer Store-Konfiguration angegebenen [Ländern](../../getting-started/store-details.md#country-options) können diese Versandmethode verwenden.<br/>**`Specific Countries`** - Nach Auswahl dieser Option wird die Liste [!UICONTROL Ship to Specific Countries] angezeigt. Wählen Sie jedes Land in der Liste aus, in dem diese Versandmethode verwendet werden kann. |
| [!UICONTROL Show Method if Not Applicable] | Webseite | Steuert die Anzeige des USPS-Versands beim Checkout. Optionen: <br/>**`Yes`**- USPS wird beim Checkout immer als Versandoption angezeigt, auch wenn dies nicht für die Bestellung gilt.<br/>**`No`** - USPS erscheint beim Checkout nur dann als Versandoption, wenn es auf die Bestellung anwendbar ist (d. h. die Bestellgewichtung übersteigt die maximale Gewichtung). |
| [!UICONTROL Debug] | Webseite | Bestimmt, ob das System zum Debugging ein Protokoll der Datenübertragungen zwischen Ihrem Speicher und USPS verwaltet. Sofern kein Problem vorliegt, das verfolgt und protokolliert werden muss, sollte diese Option auf `No` gesetzt werden. |
| [!UICONTROL Sort Order] | Webseite | Eine Zahl, die bestimmt, in welcher Reihenfolge USPS angezeigt wird, wenn es beim Checkout mit anderen Versandmethoden aufgeführt wird. Geben Sie oben in der Liste `0` ein. |

{style="table-layout:auto"}

### [!UICONTROL FedEx]

<!-- [FedEx Account Settings](https://docs.magento.com/user-guide/shipping/fedex.html) -->

#### FedEx-Kontoeinstellungen

![FedEx-Kontoeinstellungen](./assets/delivery-methods-fedex-account-settings.png){width="600" zoomable="yes"}

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|-------|------ |-----------------------------------------------------------------------------|
| [!UICONTROL Enabled for Checkout] | Webseite | Bestimmt, ob FedEx für Kunden als Versandmethode während des Checkouts verfügbar ist. Optionen: `Yes` / `No` |
| [!UICONTROL Title] | Store-Ansicht | Der Titel dieser Versandoption, wie er im Warenkorb angezeigt wird. |
| [!UICONTROL Account ID] | Webseite | Ihre FedEx-Konto-ID. |
| [!UICONTROL Api Key] | Webseite | Ihr FedEx-Konto-API-Schlüssel. |
| [!UICONTROL Secret Key] | Webseite | Ihr geheimer Schlüssel für die FedEx-Konto-API. |
| [!UICONTROL Sandbox Mode] | Webseite | Um FedEx-Transaktionen in einer Testumgebung auszuführen, setzen Sie den Sandbox-Modus auf `Yes`. Optionen: `Yes` / `No`. |
| [!UICONTROL Web-Services URL] | Webseite | Die erforderliche URL hängt von der Einstellung des Sandbox-Modus ab. Optionen: <br/>**`Production`**- Die URL für den Zugriff auf FedEx-Webdienste, wenn der Store live ist.<br/>**`Sandbox`** - Die URL für den Zugriff auf die Testumgebung für FedEx-Webdienste. |

{style="table-layout:auto"}

#### FedEx-Verpackungsparameter

![FedEx-Verpackung](./assets/delivery-methods-fedex-packaging.png){width="600" zoomable="yes"}

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Pickup Type] | Webseite | Wählen Sie aus der Liste die Abholmethode aus: <br/>**`DropOff at Fedex Location`**- (Standard) Gibt an, dass Sie Sendungen auf Ihrer lokalen FedEx-Station abbrechen.<br/>**`Contact Fedex to Schedule`** - Gibt an, dass Sie sich an FedEx wenden, um eine Abholung anzufordern. <br/>**`Use Scheduled Pickup`**- Gibt an, dass die Sendung im Rahmen einer regelmäßigen geplanten Abholung aufgenommen wird.<br/>**`On Call`** - Gibt an, dass die Abholung durch Aufruf von FedEx geplant ist. <br/>**`Package Return Program`**- Gibt an, dass die Sendung vom FedEx Ground Package Retouren Program aufgenommen wird.<br/>**`Regular Stop`** - Gibt an, dass die Sendung im regelmäßigen Pickup-Zeitplan aufgenommen wird. <br/>**`Tag`**- Gibt an, dass die Sendungs-Abholung spezifisch für eine Express-Tag- oder Ground-Aufruf-Tag-Abrufanforderung ist. Dies gilt nur für einen Rücksendeschlüssel. |
| [!UICONTROL Packages Request Type] | Webseite | Bestimmt, wie die Gewichtung für Sendungen mit mehreren Packages berechnet wird. Optionen: `Divide to equal weight (one request)` / `Use origin weight (multiple requests)` |
| [!UICONTROL Packaging] | Webseite | Wählen Sie in der Liste den Behältertyp aus, den Sie normalerweise verwenden, um Produkte zu verpacken, die in Ihrem Store bestellt wurden. |
| [!UICONTROL Weight Unit] | Webseite | Die für die Verpackungsgewichtung verwendete Einheit. Optionen: `Pounds` (Standard) / `Kilograms` |
| [!UICONTROL Maximum Package Weight] | Webseite | Der Standardwert für FedEx beträgt 150 Pfund. Wenden Sie sich an Ihren Versanddienstleister, um eine maximale unterstützte Gewichtung zu erhalten. Es wird empfohlen, den Standardwert zu verwenden, es sei denn, Sie verfügen über besondere Vereinbarungen mit FedEx. |

{style="table-layout:auto"}

#### Einstellungen für die FedEx-Bearbeitungsgebühr

![FedEx-Bearbeitungsgebühr](./assets/delivery-methods-fedex-handling-fee.png){width="600" zoomable="yes"}

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Calculate Handling Fee] | Webseite | Bestimmt die Methode zur Berechnung der Bearbeitungsgebühren. Optionen: `Fixed Fee` / `Percentage` <br/><br/>**_Hinweis:_**Die Bearbeitungsgebühr ist optional und erscheint als zusätzliche Gebühr, die zu den FedEx-Versandkosten hinzugefügt wird. |
| [!UICONTROL Handling Applied] | Webseite | Legt fest, wie Bearbeitungsgebühren angewendet werden. Optionen: `Per Order` / `Per Package` |
| [!UICONTROL Handling Fee] | Webseite | Gibt den Betrag an, der als Bearbeitungsgebühr in Rechnung gestellt wird, basierend auf der Methode zur Berechnung des Betrags. Wenn die Gebühr auf einer festen Gebühr basiert, geben Sie den Betrag als Dezimalzahl an, z. B. `4.90`. Wenn die Bearbeitungsgebühr auf einem Prozentsatz der Bestellung basiert, geben Sie den Betrag als Prozentsatz an. Wenn Sie beispielsweise sechs Prozent der Bestellung aufladen möchten, geben Sie den Wert als `.06` ein. |

{style="table-layout:auto"}

#### FedEx-Bereitstellungsmethoden

![Bereitstellungsmethoden von FedEx](./assets/delivery-methods-fedex-delivery-methods.png){width="600" zoomable="yes"}

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Residential Delivery] | Webseite | Stellen Sie einen der folgenden Schritte ein, je nachdem, ob Sie B2C (Business-to-Consumer) oder B2B (Business-to-Business) verkaufen: <br/>**`Yes`**- Für B2C-Sendungen<br/>**`No`** - Für B2B-Sendungen |
| [!UICONTROL Allowed Methods] | Webseite | Wählen Sie aus der Liste die Versandmethoden aus, die Sie unterstützen. Die Methoden hängen von Ihrem FedEx-Konto, der Häufigkeit und Größe Ihrer Sendungen sowie davon ab, ob Sie internationale Sendungen zulassen. Als Kaufmann können Sie sich entscheiden, nur den Bodenversand anzubieten. |
| [!UICONTROL Hub ID] | Webseite | Eine von FedEx bereitgestellte ID, die mit der [!DNL Smart Post] -Methode verwendet wird. |
| [!UICONTROL Free Method] | Webseite | Wählen Sie in der Liste die Versandmethode aus, die Sie für Angebote des kostenlosen Versands bevorzugen. <br/><br/>**_Hinweis:_**Diese Versandmethode ähnelt der normalen kostenlosen Versandmethode, ist jedoch in den FedEx-Versandoptionen aufgeführt und wird als FedEx-Versand identifiziert. |
| [!UICONTROL Free Shipping Amount Threshold] | Webseite | Bestimmt, ob ein Mindestbestellbetrag für den kostenlosen Versand erforderlich ist. Optionen: <br/>**`Enable`**- Ermöglicht den kostenlosen Versand von FedEx für Bestellungen, die den Mindestbetrag erfüllen.<br/>**`Disable`** - Deaktiviert den kostenlosen Versand von FedEx mit Mindestbestellung. |
| [!UICONTROL Free Shipping Amount Threshold] | Webseite | Gibt den Mindestbestellbetrag an, der für den kostenlosen Versand erforderlich ist. |
| [!UICONTROL Displayed Error Message] | Store-Ansicht | Die Meldung, die angezeigt wird, wenn FedEx aus irgendeinem Grund nicht verfügbar ist. Sie können die Standardnachricht verwenden oder eine andere eingeben. |

{style="table-layout:auto"}

#### Für FedEx geltende Ländereinstellungen

![FedEx Anwendbare Länder](./assets/delivery-methods-fedex-applicable-countries.png){width="600" zoomable="yes"}

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| [!UICONTROL Ship to Applicable Countries] | Webseite | Gibt die Länder an, in denen Ihre Kunden nach FedEx versenden können. Optionen: <br/>**`All Allowed Countries`**- Kunden aus allen in Ihrer Store-Konfiguration angegebenen [Ländern](../../getting-started/store-details.md#country-options) können diese Versandmethode verwenden.<br/>**`Specific Countries`** - Nach Auswahl dieser Option wird die Liste [!UICONTROL Ship to Specific Countries] angezeigt. Wählen Sie jedes Land in der Liste aus, in dem diese Versandmethode verwendet werden kann. |
| [!UICONTROL Ship to Specific Countries] | Webseite | Gibt an, in welchen Ländern Ihre Kunden nach FedEx versenden können. |
| [!UICONTROL Debug] | Webseite | Bestimmt, ob das System zum Debugging ein Protokoll der Datenübertragungen zwischen Ihrem Store und FedEx verwaltet. Sofern kein Problem vorliegt, das verfolgt und protokolliert werden muss, sollte diese Option auf `No` gesetzt werden. |
| [!UICONTROL Show Method if Not Applicable] | Webseite | Bestimmt, wann FedEx beim Checkout als Versandmethode angezeigt wird. Optionen: <br/>**`Yes`**- Die Option FedEx-Versand wird in der Liste der Versandmethoden angezeigt, unabhängig davon, ob die Bestellung zur Verwendung geeignet ist.<br/>**`No`** - Die Option FedEx-Versand wird nicht in der Liste der Versandmethoden angezeigt, wenn sie nicht auf die Bestellung anwendbar ist (z. B. wenn die Bestellgewichtung die maximale Gewichtung überschreitet). |
| [!UICONTROL Sort Order] | Webseite | Eine Zahl, die bestimmt, in welcher Reihenfolge FedEx angezeigt wird, wenn es beim Checkout mit anderen Versandmethoden aufgeführt wird. Geben Sie oben in der Liste `0` ein. |

{style="table-layout:auto"}

### [!UICONTROL DHL]

![DHL-Kontoeinstellungen](./assets/delivery-methods-dhl-account-settings.png)<!-- zoom -->

<!-- [DHL Account Settings](https://docs.magento.com/user-guide/shipping/dhl.html) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| _[!UICONTROL DHL Account Settings]_ |  |  |
| [!UICONTROL Enabled for Checkout] | Webseite | Bestimmt, ob DHL für Kunden als Versandmethode während des Checkout verfügbar ist. Optionen: `Yes` / `No` |
| [!UICONTROL Title] | Store-Ansicht | Der Titel dieser Versandmethode, wie er beim Checkout erscheint. |
| [!UICONTROL Gateway URL] | Webseite | Normalerweise können Sie die standardmäßige Gateway-URL akzeptieren. Wenn Ihnen DHL jedoch eine alternative URL gegeben hat, geben Sie den Wert in dieses Feld ein. |
| [!UICONTROL Access ID] | Webseite | Zugriffskennung des DHL-Versandkontos. |
| [!UICONTROL Password] | Webseite | Ihr DHL-Versandkontokennwort. |
| [!UICONTROL Account Number] | Webseite | Ihre DHL-Versandkontonummer. |

{style="table-layout:auto"}

![DHL-Paketeinstellungen](./assets/delivery-methods-dhl-package-settings.png)<!-- zoom -->

<!-- [DHL Package Settings](https://docs.magento.com/user-guide/shipping/dhl.html) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| _[!UICONTROL DHL Package Settings]_ |  |  |
| [!UICONTROL Calculate Handling Fee] | Webseite | Die Bearbeitungsgebühr ist optional und erscheint als zusätzliche Gebühr zu den Versandkosten von DHL. Wählen Sie in der Liste die Methode aus, die Sie zur Berechnung der Bearbeitungsgebühren verwenden möchten. Optionen: Feste Gebühr/Prozentsatz. |
| [!UICONTROL Handling Applied] | Webseite | Wählen Sie aus der Liste aus, wie die Bearbeitungsgebühren angewendet werden sollen. Optionen: `Per Order` / `Per Package` |
| Bearbeitungsgebühr | Webseite | Geben Sie den Betrag an, der für eine Bearbeitungsgebühr in Rechnung gestellt werden soll, basierend auf der Methode, die Sie zur Berechnung des Betrags ausgewählt haben. Wenn die Gebühr beispielsweise auf einer festen Gebühr basiert, geben Sie den Betrag als Dezimalzahl ein, z. B. `4.90`. Wenn die Bearbeitungsgebühr jedoch auf einem Prozentsatz der Bestellung basiert, geben Sie den Betrag als Prozentsatz an. Wenn Sie beispielsweise sechs Prozent der Bestellung aufladen, geben Sie den Wert als `.06` ein. |
| [!UICONTROL Divide Order Weight] | Store-Ansicht | Bestimmt, ob das Gewicht einer Bestellung über 70 kg in kleinere Einheiten aufgeteilt werden kann, um eine genaue Versandkosten zu gewährleisten. Optionen: `Yes` / `No` |
| [!UICONTROL Weight Unit] | Store-Ansicht | Bestimmt die Maßeinheit für Gewicht, die in Versandberechnungen verwendet wird. Optionen: `Pounds` / `Kilograms` |
| [!UICONTROL Size] | Store-Ansicht | Bestimmt die Größe des Pakets. Optionen: <br/>**`Regular`**- Die gelieferten Pakete entsprechen den DHL-Standardverpackungsmethoden. Wählen Sie in der Liste &quot;[!UICONTROL Allowed Methods]&quot;jede Verpackungsmethode aus, die zum Versand von Produkten aus Ihrem Geschäft verwendet wird.<br/>**`Specific`** - Wenn die gelieferten Pakete benutzerdefinierte Dimensionen aufweisen, führen Sie Folgendes aus: [!UICONTROL Height (cm)] / [!UICONTROL Depth (cm)] / [!UICONTROL Width (cm)] |

{style="table-layout:auto"}

![Zulässige DHL-Methoden](./assets/delivery-methods-dhl-allowed-methods.png)<!-- zoom -->

<!-- DHL Allowed Methods](https://docs.magento.com/user-guide/shipping/dhl.html) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| _[!UICONTROL DHL allowed methods]_ |  |  |
| [!UICONTROL Allowed Methods] | Webseite | Wählen Sie in der Liste jede Versandmethode aus, die Sie unterstützen. |
| [!UICONTROL Ready Time] | Webseite | Gibt an, wann das Paket nach dem Absenden einer Bestellung zur Übernahme bereit ist (in Stunden). |
| [!UICONTROL Displayed Error Message] | Store-Ansicht | Diese Meldung wird angezeigt, wenn DHL aus irgendeinem Grund nicht verfügbar ist. Sie können die Standardnachricht verwenden oder eine eigene Nachricht eingeben. |
| [!UICONTROL Free Method] |  | Diese Versandmethode ähnelt der normalen Free Shipping-Methode, ist jedoch in den DHL Versandoptionen aufgeführt und wird als DHL-Versand bezeichnet. Wählen Sie in der Liste die Versandmethode aus, die Sie für Angebote des kostenlosen Versands bevorzugen. |
| [!UICONTROL Free Shipping with Minimum Order Amount] | Webseite | Legen Sie einen der folgenden Werte fest: <br/>**`Enable`**- Um den kostenlosen DHL-Versand für Bestellungen zu ermöglichen, die den Mindestbetrag erreichen.<br/>**`Disable`** - Um keine kostenlose DHL-Lieferung mit Mindestbestellung anzubieten. |
| [!UICONTROL Minimum Order Amount for Free Shipping] | Webseite | Wenn Sie [!UICONTROL Free Shipping with Minimum Order] aktivieren, geben Sie den Mindestbestellwert in das Feld ein. |

{style="table-layout:auto"}

![DHL-Anwendbare Länder](./assets/delivery-methods-dhl-applicable-countries.png)<!-- zoom -->

<!-- [DHL Applicable Countries](https://docs.magento.com/user-guide/shipping/dhl.html) -->

| Feld | [Umfang](../../getting-started/websites-stores-views.md#scope-settings) | Beschreibung |
|--- |--- |--- |
| _[!UICONTROL DHL applicable countries]_ |  |  |
| [!UICONTROL Ship to Applicable Countries] | Webseite | Gibt an, welches Land Kunden diese Versandmethode verwenden dürfen. Optionen: <br/>**Alle zugelassenen Länder** - Alle zulässigen Länder können die kostenlose Versandmethode verwenden. Die zulässigen Länder werden auf der Konfigurationsseite [!UICONTROL General] angegeben. <br/>**Bestimmte Länder** - Beschränkt diese Versandoption auf die Länder, die in der Liste &quot;Versand an bestimmte Länder&quot;angegeben sind. |
| [!UICONTROL Ship to Specific Countries] | Webseite | Gibt die Länder an, in denen DHL-Sendungen durchgeführt werden können. Diese Liste der ausgewählten Länder wird verwendet, wenn in der Option [!UICONTROL Ship to Applicable Countries] die Option `Specific Countries` ausgewählt ist. |
| [!UICONTROL Show Method if Not Applicable] | Webseite | Bestimmt, wann DHL beim Checkout als Versandmethode angezeigt wird. Optionen: <br/>**`Yes`**- DHL erscheint beim Checkout immer als Versandoption, auch wenn dies nicht für die Bestellung gilt.<br/>**`No`** - DHL erscheint beim Checkout nur dann als Versandoption, wenn es auf die Bestellung anwendbar ist (d. h. wenn die Bestellgewichtung die maximale Gewichtung überschreitet). |
| [!UICONTROL Debug] | Webseite | Erstellt eine Protokolldatei mit Fehlerinformationen. |
| [!UICONTROL Sort Order] | Webseite | Eine Zahl, die bestimmt, in welcher Reihenfolge DHL angezeigt wird, wenn sie beim Checkout mit anderen Versandmethoden aufgeführt wird. Geben Sie `0` ein, um sie oben in der Liste zu platzieren. |

{style="table-layout:auto"}
