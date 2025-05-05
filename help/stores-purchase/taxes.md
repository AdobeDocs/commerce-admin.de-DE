---
title: Steuern
description: Erfahren Sie, wie Sie Ihren Store so konfigurieren, dass die Steuern entsprechend den Anforderungen Ihres Gebietsschemas berechnet werden.
exl-id: bf807132-416f-497a-82c4-b00dba4d3092
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1100'
ht-degree: 0%

---

# Steuern

Konfigurieren Sie Ihren Store, um die Steuern entsprechend den Anforderungen Ihres Gebietsschemas zu berechnen. Sie können [Steuerklassen](tax-class.md) für Produkte und Kundengruppen einrichten und [Steuerregeln](tax-rules.md) erstellen, die Produkt- und Kundenklassen, Steuerzonen und Sätze kombinieren. Commerce bietet außerdem Konfigurationseinstellungen für feste Produktsteuern, zusammengesetzte Steuern und die Anzeige von Preisen über internationale Grenzen hinweg. Wenn Sie eine ([) Mehrwertsteuer einziehen müssen](vat.md) können Sie Ihr Geschäft so einrichten, dass der entsprechende Betrag automatisch mit Validierung berechnet wird.

>[!NOTE]
>
>Die Adobe Commerce- und Magento Open Source-Versionen 2.4.0 bis 2.4.3 enthielten die vom Vertex-Anbieter entwickelte Erweiterung, die für die Integration mit Vertex Cloud verwendet wurde, um Steuerverwaltung und Adressbereinigung bereitzustellen. Ab Version 2.4.4 ist diese Erweiterung nicht mehr im Paket mit der Hauptversion enthalten und muss von der Commerce Marketplace oder direkt vom Anbieter installiert und aktualisiert werden. [Kontaktieren Sie Vertex](https://marketplace.magento.com/partner/vertex_inc), um Informationen zur Erweiterung und Dokumentation zu erhalten.<br><br>
>
>Wenn Sie die gebündelte Erweiterung aktiviert und konfiguriert haben, müssen Sie Ihre Datei „composer.json“ im Rahmen des Upgrade-Prozesses auf 2.4.4 aktualisieren, um zukünftige Erweiterungs-Updates zu verwalten. Siehe [Upgrade-](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) im _Upgrade-Handbuch_.

## Kurzübersicht

Einige Steuereinstellungen verfügen über eine Auswahl von Optionen, die bestimmen, wie die Steuer berechnet und dem Kunden präsentiert wird. Weitere Informationen finden Sie unter [Internationale Steuerrichtlinien](international-tax-guidelines.md).

Verwenden Sie die folgenden Tabellen als Referenz bei der Konfiguration der Einstellungen für die Steuerberechnung:

### Methoden zur Steuerberechnung

Zu den Optionen für die Steuerberechnungsmethode gehören [!UICONTROL Unit Price], [!UICONTROL Row Total] und [!UICONTROL Total]. In der folgenden Tabelle wird erläutert, wie das Runden (auf zwei Stellen) für verschiedene Einstellungen gehandhabt wird.

| Einstellung | Berechnung und Anzeige |
|--- |--- |
| [!UICONTROL Unit Price] | Commerce berechnet die Steuer für jeden Artikel und zeigt die Preise inklusive Steuer an. Zur Berechnung der Steuersumme wird die Steuer für jeden Artikel gerundet und dann addiert. |
| [!UICONTROL Row Total] | Commerce berechnet die Steuer für jede Zeile. Zur Berechnung der Steuersumme wird die Steuer für jeden Einzelposten gerundet und dann addiert. |
| [!UICONTROL Total] | Commerce berechnet die Steuer für jeden Artikel und addiert diese Steuerwerte, um den Gesamtbetrag der nicht gerundeten Steuer für die Bestellung zu berechnen. Anschließend wird der angegebene Rundungsmodus auf die Gesamtsteuer angewendet, um die Gesamtsteuer für den Auftrag zu bestimmen. |

{style="table-layout:auto"}

### Katalogpreise mit oder ohne Steuer

Die möglichen Anzeigefelder variieren je nach Berechnungsmethode und ob die Katalogpreise Steuern enthalten oder nicht. Bei normalen Berechnungen haben Anzeigefelder eine Zwei-Dezimalpräzision. Einige Kombinationen von Preiseinstellungen zeigen Preise an, die sowohl Steuern enthalten als auch nicht enthalten. Wenn beide in demselben Zeileneintrag angezeigt werden, kann dies für Kunden und Trigger verwirrend sein und eine [Warnung](taxes.md#warning-messages) darstellen.

| Einstellung | Berechnung und Anzeige |
|--- |--- |
| [!UICONTROL Excluding Tax] | Mit dieser Einstellung wird der Artikelgrundpreis so verwendet, wie er eingegeben wurde, und die Steuerberechnungsmethoden werden angewendet. |
| [!UICONTROL IncludingTax] | Mit dieser Einstellung wird zuerst der Basispreis des Artikels ohne Steuer berechnet. Dieser Wert wird als Grundpreis verwendet und die Methoden zur Berechnung der Steuer werden angewendet. |

{style="table-layout:auto"}

>[!IMPORTANT]
>
>Es gibt Änderungen gegenüber früheren Versionen für EU-Händler oder andere MwSt-Händler, die Preise einschließlich Steuern anzeigen und in mehreren Ländern mit mehreren Store-Ansichten tätig sind. Wenn Sie Preise mit mehr als zwei Stellen Genauigkeit laden, rundet Commerce alle Preise automatisch auf zwei Stellen, um sicherzustellen, dass den Käufern ein einheitlicher Preis angezeigt wird.

### Versandkosten mit oder ohne Steuer

| Einstellung | Anzeige | Kalkulation |
|--- |--- |--- |
| [!UICONTROL Excluding Tax] | Erscheint ohne Steuer. | Normale Berechnung. Der Versand wird der Gesamtsumme des Warenkorbs hinzugefügt und normalerweise als separater Artikel angezeigt. |
| [!UICONTROL Including Tax] | Kann „Steuern inklusive“ sein oder „Steuern“ separat angezeigt werden. | Der Versand wird als ein weiterer Artikel im Warenkorb mit Steuern behandelt, wobei dieselben Berechnungen verwendet werden. |

{style="table-layout:auto"}

### Steuerbeträge als Posten

Um zwei verschiedene Steuerbeträge als separate Zeileneinträge anzuzeigen, z. B. GST und PST für kanadische Geschäfte, müssen Sie unterschiedliche Prioritäten für die entsprechenden Steuerregeln festlegen. Bei früheren Steuerberechnungen würden Steuern mit unterschiedlichen Prioritäten jedoch automatisch verschärft. Um separate Steuerbeträge korrekt anzuzeigen, ohne die Steuerbeträge falsch zu kombinieren, können Sie verschiedene Prioritäten festlegen und auch das Kontrollkästchen _Nur Zwischensumme berechnen_ aktivieren. Diese Einstellung erzeugt korrekt berechnete Steuerbeträge, die als separate Posten erscheinen.

## Warnmeldungen

Einige Kombinationen von steuerbezogenen Optionen könnten für Kunden verwirrend sein und Trigger eine Warnung sein. Diese Bedingungen können auftreten, wenn die Steuerberechnungsmethode auf `Row` oder `Total` festgelegt ist und dem Kunden Preise angezeigt werden, die sowohl Steuern als auch Steuern enthalten. Dies kann auch vorkommen, wenn im Warenkorb eine Steuer pro Artikel enthalten ist. Da die Steuerberechnung gerundet ist, kann der im Warenkorb angezeigte Betrag von dem Betrag abweichen, den ein Kunde zu zahlen erwartet.

Wenn Ihre Steuerberechnung auf einer problematischen Konfiguration basiert, werden die folgenden Warnungen angezeigt:

![Ausrufezeichen](../assets/icon-warning.png) **Warnung**. `Tax discount configuration might result in different discounts than a customer might expect for store(s); Europe Website (French), Europe Website (German). Please see source for more details.`

![Ausrufezeichen](../assets/icon-warning.png) **Warnung**. `Tax configuration can result in rounding errors for store(s): Europe Websites (French), Europe Websites (German).`

## Ort der Lieferung digitaler Güter (EU)

Händler in der Europäischen Union (EU) müssen ihre digitalen Waren, die in jedem Mitgliedsland verkauft werden, nach Viertel melden. Digitale Waren werden je nach Lieferadresse des Kunden besteuert. Das Gesetz verpflichtet Händler, einen Steuerbericht zu erstellen und die relevanten Steuerbeträge für digitale Güter zu identifizieren, im Gegensatz zu physischen Gütern.

Händler müssen alle digitalen Waren, die von den EU-Mitgliedstaaten verkauft werden, vierteljährlich einer zentralen Steuerverwaltung melden, zusammen mit der Zahlung der während des Zeitraums erhobenen Steuer.

Händler, die die Schwelle (50.000.000 Euro Jahresumsatz) noch nicht erreicht haben, müssen weiterhin physische Waren melden, die in die EU-Staaten verkauft werden, in denen sie MwSt-Nummern registriert haben.

Händler, die auf Steuern geprüft werden, die für digitale Waren gezahlt werden, müssen zwei unterstützende Informationen zur Verfügung stellen, um den Wohnsitz des Kunden zu ermitteln.

- Die Lieferadresse des Kunden und ein Nachweis über einen erfolgreichen Zahlungsvorgang können zur Ermittlung des Wohnorts des Kunden verwendet werden. (Die Zahlung wird nur akzeptiert, wenn die Lieferadresse mit den Angaben des Zahlungsanbieters übereinstimmt.)
- Die Informationen können auch direkt aus dem Datenspeicher in den Commerce-Datenbanktabellen erfasst werden.

_&#x200B;**So erfassen Sie Steuerinformationen für digitale Waren:**&#x200B;_

1. Laden Sie die Steuersätze für alle EU-Mitgliedsländer.

1. Erstellen Sie eine Produktsteuerklasse für digitale Waren.

1. Ordnen Sie alle digitalen Waren der Produktsteuerklasse „Digitale Waren“ zu.

1. Erstellen Sie [Steuerregeln](tax-rules.md) für Ihre physischen Waren, indem Sie die Klassen für die physische Produktsteuer verwenden, und verknüpfen Sie sie mit den entsprechenden Steuersätzen.

1. Erstellen Sie Steuerregeln für Ihre digitalen Waren mithilfe der Produktsteuerklasse für digitale Waren und verknüpfen Sie sie mit den entsprechenden Steuersätzen für die EU-Mitgliedsländer.

1. Führen Sie den Steuerbericht für den entsprechenden Zeitraum aus und erfassen Sie die erforderlichen digitalen Wareninformationen.

1. Exportieren Sie die Steuerbeträge, die sich auf die Steuersätze für die Produktsteuerklasse „Digitale Waren“ beziehen.

Zusätzliche Ressourcen:

- [Europäische Kommission - Steuern und Zollunion][1]
- [EU 1015 Lieferortänderungen][2]

[1]: https://europa.eu/youreurope/business/taxation/vat/vat-rules-rates/index_en.htm
[2]: https://www2.deloitte.com/global/en/services/tax.html
