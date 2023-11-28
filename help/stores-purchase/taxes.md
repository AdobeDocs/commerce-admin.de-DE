---
title: Steuern
description: Erfahren Sie, wie Sie Ihren Store so konfigurieren, dass Steuern entsprechend den Anforderungen Ihres Gebietsschemas berechnet werden.
exl-id: bf807132-416f-497a-82c4-b00dba4d3092
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1115'
ht-degree: 0%

---

# Steuern

Konfigurieren Sie Ihren Speicher so, dass Steuern entsprechend den Anforderungen Ihres Gebietsschemas berechnet werden. Sie können [Steuerklassen](tax-class.md) für Produkte und Kundengruppen und erstellen Sie [Steuervorschriften](tax-rules.md) die Produkt- und Kundenklassen, Steuerzonen und Tarife kombinieren. Der Handel bietet außerdem Konfigurationseinstellungen für feste Produktsteuern, zusammengesetzte Steuern und Preisangaben über internationale Grenzen hinweg. Wenn Sie eine [Mehrwertsteuer](vat.md), können Sie Ihren Store so einrichten, dass der entsprechende Betrag bei Validierung automatisch berechnet wird.

>[!NOTE]
>
>Die Versionen 2.4.0 bis 2.4.3 von Adobe Commerce und Magento Open Source umfassten die vom Vertex-Anbieter entwickelte Erweiterung, die zur Integration in die Vertex Cloud verwendet wurde, um Steuerverwaltung und Adressbereinigung zu ermöglichen. Ab Version 2.4.4 ist diese Erweiterung nicht mehr im Paket mit der Kernversion enthalten und muss über die Commerce Marketplace oder direkt vom Anbieter installiert und aktualisiert werden. [Kontaktverweis](https://marketplace.magento.com/partner/vertex_inc) für Informationen zur Erweiterung und Dokumentation.<br><br>
>
>Wenn Sie die gebündelte Erweiterung aktiviert und konfiguriert haben, müssen Sie Ihre Composer.json-Datei im Rahmen des Aktualisierungsprozesses von 2.4.4 aktualisieren und zukünftige Erweiterungs-Updates verwalten. Siehe [Upgrade-Module](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) im _Upgrade-Handbuch_.

## Kurzübersicht

Einige Steuereinstellungen haben die Wahl zwischen Optionen, die bestimmen, wie die Steuer berechnet und dem Kunden angezeigt wird. Weitere Informationen finden Sie unter [International Tax Guidelines](international-tax-guidelines.md).

Verwenden Sie die folgenden Tabellen als Referenz bei der Konfiguration der Steuerberechnungseinstellungen:

### Methoden der Steuerberechnung

Optionen für die Steuerberechnungsmethode: [!UICONTROL Unit Price], [!UICONTROL Row Total], und [!UICONTROL Total]. In der folgenden Tabelle wird erläutert, wie die Rundung (auf zwei Stellen) für verschiedene Einstellungen durchgeführt wird.

| Einstellung | Berechnung und Anzeige |
|--- |--- |
| [!UICONTROL Unit Price] | Der Handel berechnet die Steuer für jeden Artikel und zeigt die Preise inklusive Steuern an. Zur Berechnung des Steuergesamtbetrags wird die Steuer für jedes Element gerundet und dann addiert. |
| [!UICONTROL Row Total] | Commerce berechnet die Steuer für jede Zeile. Zur Berechnung der Steuersumme wird die Steuer für jeden Zeileneintrag gerundet und dann addiert. |
| [!UICONTROL Total] | Commerce berechnet die Steuer für jedes Element und fügt diese Steuerwerte hinzu, um den nicht gerundeten Steuerbetrag für die Bestellung zu berechnen. Anschließend wird der angegebene Rundungsmodus auf die Gesamtsteuer angewendet, um die Gesamtsteuer für die Bestellung zu ermitteln. |

{style="table-layout:auto"}

### Katalogpreise mit oder ohne Steuern

Die möglichen Anzeigefelder variieren je nach Berechnungsmethode und je nachdem, ob die Katalogpreise Steuern enthalten oder ausschließen. Anzeigefelder haben in normalen Berechnungen eine zweidezimale Genauigkeit. Einige Kombinationen aus Preiseinstellungen zeigen Preise an, die sowohl Steuern enthalten als auch ausschließen. Wenn beide im selben Zeilenelement angezeigt werden, kann es für Kunden verwirrend sein, und Trigger können [warning](taxes.md#warning-messages).

| Einstellung | Berechnung und Anzeige |
|--- |--- |
| [!UICONTROL Excluding Tax] | Mit dieser Einstellung wird der Basispreis des Elements so verwendet, wie er eingegeben wurde, und die Methoden zur Berechnung der Steuern werden angewendet. |
| [!UICONTROL IncludingTax] | Mit dieser Einstellung wird der Basispreis des Artikels, der Steuern ausschließt, zuerst berechnet. Dieser Wert wird als Basispreis verwendet und die Methoden zur Berechnung der Steuern werden angewendet. |

{style="table-layout:auto"}

>[!IMPORTANT]
>
>Es gibt Änderungen gegenüber früheren Versionen für EU-Händler oder andere MwSt-Händler, die Preise anzeigen, einschließlich Steuern und in mehreren Ländern mit mehreren Store-Ansichten. Wenn Sie Preise mit mehr als zwei Stellen genau laden, rundet Commerce automatisch alle Preise auf zwei Stellen, um sicherzustellen, dass den Käufern ein einheitlicher Preis präsentiert wird.

### Versandpreise mit oder ohne Steuern

| Einstellung | Anzeige | Berechnung |
|--- |--- |--- |
| [!UICONTROL Excluding Tax] | Wird ohne Steuern angezeigt. | Normale Berechnung. Der Versand wird der Gesamtsumme des Warenkorbs hinzugefügt, die normalerweise als separater Artikel angezeigt wird. |
| [!UICONTROL Including Tax] | Kann steuerfrei sein, oder Steuern können separat angezeigt werden. | Der Versand wird mit Steuern wie ein anderer Artikel im Warenkorb behandelt, der dieselben Berechnungen verwendet. |

{style="table-layout:auto"}

### Steuerbeträge als Posten

Um zwei verschiedene Steuerbeträge als separate Zeileneinträge anzuzeigen, wie z. B. GST und PST für kanadische Geschäfte, müssen Sie für die entsprechenden Steuerregeln unterschiedliche Prioritäten festlegen. In früheren Steuerberechnungen würden jedoch automatisch Steuern mit unterschiedlichen Prioritäten erhöht. Um separate Steuerbeträge ohne fehlerhafte Addition der Steuerbeträge korrekt anzuzeigen, können Sie verschiedene Prioritäten festlegen und auch die _Nur Zwischensumme berechnen_ aktivieren. Diese Einstellung erzeugt korrekt berechnete Steuerbeträge, die als separate Zeileneinträge angezeigt werden.

## Warnmeldungen

Einige Kombinationen von steuerbezogenen Optionen können für Kunden verwirrend sein und eine Warnung an den Trigger verwerfen. Diese Bedingungen können auftreten, wenn die Methode zur Berechnung der Steuern auf `Row` oder `Total`und dem Kunden Preise angezeigt werden, die sowohl Steuern als auch Steuern enthalten. Sie kann auch auftreten, wenn im Warenkorb Steuern pro Artikel erhoben werden. Da die Steuerberechnung gerundet wird, kann der im Warenkorb angezeigte Betrag von dem Betrag abweichen, den ein Kunde erwartet.

Wenn Ihre Steuerberechnung auf einer problematischen Konfiguration basiert, werden die folgenden Warnungen angezeigt:

![Ausrufezeichen](../assets/icon-warning.png) **Warnung**. `Tax discount configuration might result in different discounts than a customer might expect for store(s); Europe Website (French), Europe Website (German). Please see source for more details.`

![Ausrufezeichen](../assets/icon-warning.png) **Warnung**. `Tax configuration can result in rounding errors for store(s): Europe Websites (French), Europe Websites (German).`

## Ort der Versorgung mit digitalen Gütern (EU)

Händler in der Europäischen Union (EU) müssen ihre digitalen Waren vierteljährlich an jedes Mitgliedsland melden. Digitale Waren werden nach der Lieferadresse des Kunden besteuert. Nach dem Gesetz müssen die Händler einen Steuerbericht erstellen und die entsprechenden Steuerbeträge für digitale Waren im Gegensatz zu physischen Gütern ermitteln.

Die Händler müssen alle von den EU-Mitgliedstaaten verkauften digitalen Waren vierteljährlich an eine zentrale Steuerverwaltung melden, zusammen mit der Zahlung, die während des Zeitraums für die Erhebung der Steuer fällig ist.

Händler, die die Schwelle (50.000 Euro Jahresumsatz) noch nicht erreicht haben, müssen weiterhin Waren melden, die in die EU-Staaten verkauft werden, in denen sie Mehrwertsteuernummern registriert haben.

Händler, die für die für digitale Waren gezahlten Steuern geprüft werden, müssen zwei Belege vorlegen, um den Wohnort des Kunden zu ermitteln.

- Die Lieferadresse des Kunden und eine Aufzeichnung eines erfolgreichen Zahlungsvorgangs können zur Bestimmung des Wohnorts des Kunden verwendet werden. (Die Zahlung wird nur akzeptiert, wenn die Lieferadresse mit den Informationen des Zahlungsdienstleisters übereinstimmt.)
- Die Informationen können auch direkt aus dem Datenspeicher in den Commerce-Datenbanktabellen erfasst werden.

_**So sammeln Sie Informationen zur digitalen Gütersteuer:**_

1. Laden Sie die Steuersätze für alle EU-Mitgliedsländer.

1. Erstellen Sie eine digitale Produktsteuerklasse für Waren.

1. Weisen Sie alle Ihre digitalen Waren der Produktsteuerklasse für digitale Waren zu.

1. Erstellen [Steuervorschriften](tax-rules.md) für Ihre Waren, unter Verwendung von Körperschaftssteuerklassen und unter Berücksichtigung der entsprechenden Steuersätze.

1. Erstellen Sie Steuerregeln für Ihre digitalen Waren, verwenden Sie die Produktsteuerklasse für digitale Waren und verbinden Sie sie mit den entsprechenden Steuersätzen für EU-Mitgliedstaaten.

1. Führen Sie den Steuerbericht für den entsprechenden Zeitraum aus und sammeln Sie die erforderlichen digitalen Wareninformationen.

1. Exportieren Sie die Steuerbeträge, die mit den Steuersätzen für die digitale Warenproduktklasse in Verbindung stehen.

Zusätzliche Ressourcen:

- [Europäische Kommission - Steuern und Zollunion][1]
- [EU 1015 - Veränderungen beim Versorgungsort][2]

[1]: https://europa.eu/youreurope/business/taxation/vat/vat-rules-rates/index_en.htm
[2]: https://www2.deloitte.com/global/en/services/tax.html
