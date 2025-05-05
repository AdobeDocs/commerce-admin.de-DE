---
title: Konfigurieren Sie [!DNL Inventory Management]
description: Erfahren Sie mehr über die Konfiguration  [!DNL Inventory Management]  Optionen, die die Quellverfügbarkeit, Storefront-Produkte und den Bestellversand bestimmen.
exl-id: 1696999e-77b1-45c7-9b0b-dd1512427cff
feature: Inventory, Configuration
source-git-commit: 67cbb0d05f9f63ef51ccff3580cd27df86645fd0
workflow-type: tm+mt
source-wordcount: '770'
ht-degree: 0%

---

# Konfigurieren von [!DNL Inventory Management]

Das [!DNL Inventory Management]-Modul unterstützt Lagerkonfigurationseinstellungen auf Produkt- und globaler Ebene und bietet zusätzliche Einstellungen, die sich auf die Quellverfügbarkeit, Storefront-Produkte und den Bestellversand auswirken. Die Konfigurationseinstellungen gelten für:

- Den gesamten Katalog finden Sie unter **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**. Erweitern Sie dann **[!UICONTROL Catalog]**&#x200B;im linken Bereich und wählen Sie **[!UICONTROL Inventory]**&#x200B;aus.

- Spezifische Produkte: Gehen Sie zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**. Öffnen Sie das Produkt dann im Bearbeitungsmodus und klicken Sie im Abschnitt _[!UICONTROL Sources]_&#x200B;auf **[!UICONTROL Advanced Inventory]**.

Ihr Katalog kann so konfiguriert werden, dass Inventardaten in Ihrer Storefront angezeigt werden, aktive Warenkörbe verwaltet werden und vieles mehr. Zeigt die Verfügbarkeit jedes Artikels als _Auf Lager_ oder _Nicht vorrätig_ und den verfügbaren Lagerbestand an, wenn der Lagerbestand niedrig ist.

Der Schwellenwert für nicht vorrätige Artikel gibt an, wann ein Produkt neu bestellt werden soll, subtrahiert von der verkaufsfähigen Menge für einen Bestand und kann so eingestellt werden, dass aktivierte oder deaktivierte Nachbestellungen unterstützt werden. Lassen Sie Nachbestellungen für Ihren Store zu und legen Sie eine maximale Anzahl von Bestellungen für alle oder bestimmte Produkte fest.

Eine weitere Möglichkeit, den Schwellenwert für die Lagerverfügbarkeit zu verwenden, besteht darin, Produkte zu verwalten, die stark nachgefragt sind. Wenn Sie neue Kunden gewinnen möchten, anstatt an Käufer mit hoher Menge zu verkaufen, können Sie eine maximale Menge festlegen, um zu verhindern, dass ein einzelner Käufer Ihr gesamtes Inventar abnimmt.

![Beispiel auf Lager, nur noch 1 vorhanden](assets/storefront-stock-options-1-left.png)

## Konfigurationsoptionen

[!DNL Commerce] Stores und Produkte unterstützen die folgenden Konfigurationen für die Verwaltung von Produkten, Inventar, Benachrichtigungen und mehr. [!DNL Commerce] bietet zusätzliche Konfigurationseinstellungen für Massenaktionen und den Distance Priority-Algorithmus.

| Option | Beschreibung |
|--|--|
| [!UICONTROL Manage Stock] | Ermöglicht [!DNL Commerce] die Verwaltung des gesamten Bestands. Festlegen, ob die Bestandskontrolle für dieses Produkt oder alle Produkte in [!DNL Commerce] verwendet wird. Zeigt weitere Optionen an, wenn auf `Yes` gesetzt. |
| [!UICONTROL Only X left Threshold] | Legt eine Menge fest, die benachrichtigt wird, wenn ein bestimmter Betrag zum Kauf verfügbar bleibt. Dieser Betrag wird auf Lagerebene verfolgt. |
| [!UICONTROL Out-of-Stock Threshold] | Ihr Sicherheitsbestand, Menge zum Trigger und Benachrichtigung über nicht vorrätige Artikel, um das Risiko von Lagerausfällen zu verringern. Dieser Wert wirkt sich auf Auftragsrückstände aus. Optionen: <br />**[!UICONTROL No Backorders]**: Akzeptiert keine Nachbestellungen, wenn das Produkt nicht vorrätig ist.<br />**[!UICONTROL Allow Qty Below 0]**: Akzeptiert Nachbestellungen, wenn die Menge unter null fällt.<br />**[!UICONTROL Allow Qty Below 0 and Notify Customer]**: Akzeptiert Nachbestellungen, wenn die Menge unter null fällt, informiert Kunden jedoch darüber, dass weiterhin Bestellungen aufgegeben werden können.<br /><br />**[!UICONTROL Backorders disabled]**: Es wird empfohlen, einen positiven Wert über 0 einzugeben, z. B. 5 oder 25. <br/>**[!UICONTROL Backorders enabled]**: Geben Sie einen negativen Schwellenwert für die maximale Anzahl der zulässigen Auftragsrückstände ein, z. B. -5 oder -25. Ein Wert von 0 dient als unendlicher Bestand. Ein positiver Wert wird ignoriert und als 0 behandelt. |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | Legt die Mindestmenge des Produkts fest, die in einer einzelnen Bestellung gekauft werden kann. |
| [!UICONTROL Maximum Qty Allowed in Shopping Cart] | Legt die maximale Menge des Produkts fest, die in einer einzelnen Bestellung gekauft werden kann. |
| [!UICONTROL Qty Uses Decimals] | Ermöglicht Dezimalbeträge anstelle von Ganzzahlen für die Menge eines Produkts. Diese Einstellung ist hilfreich für Produkte, die nach Gewicht, Volumen oder Länge verkauft werden. Wird auf der Source-Ebene angegeben und auf der Lagerebene basierend auf zugewiesenen Quellen berechnet. |
| [!UICONTROL Allow Multiple Boxes for Shipping] | Legt fest, ob Teile eines Produkts separat versendet werden können. Diese Option ist sichtbar, wenn **[!UICONTROL Qty Uses Decimals]** = `Yes`. |
| [!UICONTROL Backorders] | Gibt an, ob Auftragsrückstände zulässig sind. Wird auf der Source-Ebene angegeben und auf der Lagerebene basierend auf zugewiesenen Quellen berechnet. Wenn diese Option aktiviert ist, um Auftragsrückstände zuzulassen, wird empfohlen, einen negativen Wert für den Schwellenwert für nicht vorrätige Aufträge festzulegen (siehe [Konfigurieren von ](backorders.md)). Optionen: <br />**[!UICONTROL No Backorders]**: Akzeptiert keine Nachbestellungen, wenn das Produkt nicht vorrätig ist.<br />**[!UICONTROL Allow Qty Below 0]**: Akzeptiert Nachbestellungen, wenn die Menge unter null fällt.<br />**[!UICONTROL Allow Qty Below 0 and Notify Customer]**: Akzeptiert Nachbestellungen, wenn die Menge unter null fällt, informiert Kunden jedoch darüber, dass weiterhin Bestellungen aufgegeben werden können. |
| [!UICONTROL Notify for Quantity Below] | Legt die Menge fest, für die eine Benachrichtigung „Menge unter“ Trigger wird, die auf geringe Lagerbestände hinweist. Dieser Betrag wird von der Verkaufsmenge abgezogen, nicht von der Lagermenge. |
| [!UICONTROL Enable Qty Increments] | Bestimmt, ob das Produkt in Mengenschritten verkauft werden kann. Wenn diese Option aktiviert ist, geben Sie die Menge der Produkte ein, die in einem inkrementellen Schritt gekauft werden müssen. Inkremente legen fest, wie viele Produktelemente als einzelnes Produkt und als untergeordnetes Element von konfigurierbaren, gruppierten und gebündelten Produkten erworben werden müssen. |
| [!UICONTROL Automatically Return Credit Memo Item to Stock] | [!DNL Inventory Management] verwendet diesen Wert nicht. Wenn Sie eine Rücksendung oder Gutschrift abschließen, wird die Produktmenge automatisch an die entsprechende Bezugsmenge zurückgegeben. Siehe [Konfigurieren von Produktoptionen](product-options.md). |

## Konfigurationsfallback und Vererbung

Konfigurationen überschreiben oder wenden im folgenden Pfad der Vererbung an: Der Abschnitt &quot;_[!UICONTROL Sources]_&quot; überschreibt den&#x200B;_[!UICONTROL Advanced Options]_ „Globaler _[!UICONTROL Inventory]_&quot;.

Wenn [!DNL Commerce] prüft, ob benutzerdefinierte Einstellungen angewendet werden können, folgt sie dieser Reihenfolge:

1. Sucht im Abschnitt _[!UICONTROL Sources]_&#x200B;nach benutzerdefinierten Einstellungen auf Produktebene. Einige Einstellungen sind verfügbar.

1. Überprüft die _[!UICONTROL Advanced Inventory]_.

1. Wenn `Use Config Settings` für die Produkteinstellungen ausgewählt ist, wird nach einem Wert auf der Konfigurationsseite des globalen _Inventars_ Store gesucht.

Sie können zum Beispiel Nachbestellungen in Ihrem Geschäft mit einer Konfiguration ähnlich der folgenden unterschiedlich konfigurieren:

- _Global:_ Aktivieren Sie Nachbestellungen für den Store und setzen Sie den Schwellenwert für nicht vorrätige Artikel auf `-50`

- _Produkt:_ Deaktivieren Sie Nachbestellungen für ein bestimmtes Produkt und setzen Sie den Schwellenwert für nicht vorrätige Artikel auf `10`
