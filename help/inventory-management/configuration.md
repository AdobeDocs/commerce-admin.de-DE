---
title: "Konfigurieren [!DNL Inventory Management]"
description: Informationen zur Konfiguration von [!DNL Inventory Management] Optionen, die die Verfügbarkeit der Quelle, Storefront-Produkte und den Versand von Bestellungen bestimmen.
exl-id: 1696999e-77b1-45c7-9b0b-dd1512427cff
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '739'
ht-degree: 0%

---

# Konfigurieren [!DNL Inventory Management]

Die [!DNL Inventory Management] -Modul unterstützt Einstellungen der Lagerbestandskonfiguration auf Produkt- und globaler Ebene und bietet außerdem zusätzliche Einstellungen, die sich auf die Quellverfügbarkeit, Storefront-Produkte und den Bestellversand auswirken. Die Konfigurationseinstellungen gelten für:

- Der gesamte Katalog: **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**. Anschließend erweitern Sie **[!UICONTROL Catalog]**im linken Bereich und wählen Sie **[!UICONTROL Inventory]**.

- Spezifische Produkte: Gehen Sie zu **[!UICONTROL Catalog]** > **[!UICONTROL Products]**. Öffnen Sie dann das Produkt im Bearbeitungsmodus und klicken Sie auf **[!UICONTROL Advanced Inventory]** im _[!UICONTROL Sources]_Abschnitt.

Ihr Katalog kann so konfiguriert werden, dass er Bestandsdaten in Ihrer Storefront anzeigt, aktive Warenkörbe verwaltet und vieles mehr. Die Verfügbarkeit der einzelnen Artikel anzeigen als _Auf Lager_ oder _Nicht vorrätig_ und den verfügbaren Bestand, wenn der Lagerbestand gering ist.

Die &quot;Nicht vorrätig&quot;-Schwelle gibt an, wann ein Produkt neu angeordnet werden soll, von der &quot;Verkaufte Menge&quot;für ein Lager abgezogen und auf die Unterstützung von aktivierten oder deaktivierten Rückständen eingestellt werden kann. Lassen Sie für Ihren Store Aufstockungen zu, indem Sie eine maximale Anzahl von Bestellungen für alle oder bestimmte Produkte festlegen.

Eine andere Möglichkeit, den Schwellenwert für die Lagerverfügbarkeit zu nutzen, besteht darin, Produkte zu verwalten, die stark nachgefragt sind. Wenn Sie neue Kunden erfassen möchten, anstatt an Käufer mit hoher Menge zu verkaufen, können Sie eine Höchstmenge festlegen, um zu verhindern, dass ein einzelner Käufer Ihren gesamten Bestand ausnimmt.

![Beispiel auf Lager, nur 1 links](assets/storefront-stock-options-1-left.png)

## Konfigurationsoptionen

[!DNL Commerce] Stores und Produkte unterstützen die folgenden Konfigurationen zum Verwalten von Produkten, Inventaren, Benachrichtigungen und mehr. [!DNL Commerce] bietet zusätzliche Konfigurationseinstellungen für Massenaktionen und den Algorithmus Distance Priority .

| Option | Beschreibung |
|--|--|
| [!UICONTROL Manage Stock] | Aktiviert [!DNL Commerce] um alle Bestände zu verwalten. Legen Sie fest, ob die Bestandskontrolle für dieses Produkt oder alle Produkte in [!DNL Commerce]. Zeigt weitere Optionen an, die auf `Yes`. |
| [!UICONTROL Only X left Threshold] | Legt eine Menge fest, die benachrichtigt wird, wenn ein bestimmter Betrag zum Kauf verfügbar bleibt. Dieser Betrag wird auf Lagerebene nachverfolgt. |
| [!UICONTROL Out-of-Stock Threshold] | Ihre Sicherheitsvorräte, die Menge an Trigger und die Meldung von Nichtvorräten, um das Risiko von Lagervorräten zu verringern. Dieser Wert wirkt sich auf Rückstände aus. Optionen:<br />**[!UICONTROL No Backorders]**: Akzeptiert keine Nachbestellungen, wenn das Produkt nicht vorrätig ist.<br />**[!UICONTROL Allow Qty Below 0]**: Akzeptiert Rückaufträge, wenn die Menge unter null fällt.<br />**[!UICONTROL Allow Qty Below 0 and Notify Customer]**: Akzeptiert Rückaufträge, wenn die Menge unter null fällt, benachrichtigt Kunden jedoch darüber, dass weiterhin Bestellungen aufgegeben werden können.<br /><br />**[!UICONTROL Backorders disabled]**: Es wird empfohlen, einen positiven Wert über 0 einzugeben, z. B. 5 oder 25. <br/>**[!UICONTROL Backorders enabled]**: Geben Sie einen negativen Schwellenwert für die maximal zulässige Anzahl von Backorders ein, z. B. -5 oder -25. Der Wert 0 dient als unendlicher Bestand. Ein positiver Wert wird ignoriert und als 0 behandelt. |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | Legt die Mindestmenge des Produkts fest, das in einer Bestellung erworben werden kann. |
| [!UICONTROL Maximum Qty Allowed in Shopping Cart] | Legt die maximale Menge des Produkts fest, die in einer Bestellung erworben werden kann. |
| [!UICONTROL Qty Uses Decimals] | Ermöglicht Dezimalmengen anstelle von Ganzzahlen für die Menge eines Produkts. Diese Einstellung ist hilfreich für Produkte, die nach Gewicht, Volumen oder Länge verkauft werden. Wird auf der Ebene der Quelle angegeben, berechnet auf der Ebene des Lagers basierend auf zugewiesenen Quellen. |
| [!UICONTROL Allow Multiple Boxes for Shipping] | Bestimmt, ob Teile eines Produkts separat ausgeliefert werden können. Diese Option ist sichtbar, wenn **[!UICONTROL Qty Uses Decimals]** = `Yes`. |
| [!UICONTROL Backorders] | Gibt an, ob Rückläufe zulässig sind. Wird auf der Ebene der Quelle angegeben, berechnet auf der Ebene des Lagers basierend auf zugewiesenen Quellen. Wenn diese Option aktiviert ist, um Rückstände zuzulassen, legen Sie einen negativen Wert für den Schwellenwert für &quot;Nicht auf Lager&quot; fest (siehe [Konfigurieren von Rückständen](backorders.md)) wird empfohlen. Optionen:<br />**[!UICONTROL No Backorders]**: Akzeptiert keine Nachbestellungen, wenn das Produkt nicht vorrätig ist.<br />**[!UICONTROL Allow Qty Below 0]**: Akzeptiert Rückaufträge, wenn die Menge unter null fällt.<br />**[!UICONTROL Allow Qty Below 0 and Notify Customer]**: Akzeptiert Rückaufträge, wenn die Menge unter null fällt, benachrichtigt Kunden jedoch darüber, dass weiterhin Bestellungen aufgegeben werden können. |
| [!UICONTROL Notify for Quantity Below] | Legt die Menge fest, die Trigger eine Meldung über die Menge unter und warnt vor einem niedrigen Lagerbestand. Dieser Betrag wird von der Verkaufsmenge abgezogen, nicht von der Bestandsmenge. |
| [!UICONTROL Enable Qty Increments] | Bestimmt, ob das Produkt in Mengenschritten verkauft werden kann. Wenn diese Option aktiviert ist, geben Sie die Menge der Produkte an, die in einem inkrementellen Schritt erworben werden müssen. |
| [!UICONTROL Automatically Return Credit Memo Item to Stock] | [!DNL Inventory Management] verwendet diesen Wert nicht. Wenn Sie eine Rückgabe oder ein Kreditmemo abschließen, wird die Produktmenge automatisch an die betroffene Quellmenge zurückgegeben. Siehe [Konfigurieren von Produktoptionen](product-options.md). |

## Zurückfallen und Vererbung der Konfiguration

Konfigurationen, die den folgenden Vererbungspfad überschreiben oder anwenden: Produkt _[!UICONTROL Sources]_-Abschnitt überschreibt Produkt_[!UICONTROL Advanced Options]_ überschreibt global _[!UICONTROL Inventory]_Store-Konfiguration.

Wann [!DNL Commerce] überprüft, ob die benutzerdefinierten Einstellungen angewendet werden sollen, wird diese Reihenfolge befolgt:

1. Prüft auf benutzerdefinierte Einstellungen auf Produktebene im _[!UICONTROL Sources]_Abschnitt. Es sind einige Einstellungen verfügbar.

1. Prüft das Produkt _[!UICONTROL Advanced Inventory]_-Einstellungen.

1. Wenn `Use Config Settings` für die Produkteinstellungen ausgewählt ist, wird auf einen Wert aus der globalen _Bestand_ Konfigurationsseite speichern.

Sie können beispielsweise Backorder in Ihrem Store unterschiedlich konfigurieren, mit einer ähnlichen Konfiguration wie die folgende:

- _Global:_ Aktivieren Sie die Rückstände für den Store, setzen Sie den Schwellenwert für nicht vorrätige Waren auf `-50`

- _Produkt:_ Deaktivieren Sie Rückstände für ein bestimmtes Produkt, setzen Sie den Schwellenwert für nicht vorrätige Verwendung auf `10`
