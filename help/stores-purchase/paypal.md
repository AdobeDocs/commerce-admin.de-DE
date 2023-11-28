---
title: PayPal-Zahlungslösungen
description: Erfahren Sie mehr über die PayPal Payment-Lösungsintegrationen, die für Ihren Store verfügbar sind.
exl-id: d447b98e-d30c-4759-9ae0-94ccbeed9ba4
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1236'
ht-degree: 0%

---

# PayPal-Zahlungslösungen

PayPal ist ein weltweit führender Anbieter von Online-Zahlungen und eine schnelle und sichere Möglichkeit für Ihre Kunden, online zu bezahlen. Die Auswahl der verfügbaren PayPal-Lösungen variiert je nach Händlerstandort. PayPal Express Checkout und PayPal Payments Standard können in allen Teilen der Welt verwendet werden. Weitere Informationen finden Sie unter [PayPal-Lösungen nach Ländern](#paypal-solutions-by-country).

>[!IMPORTANT]
>
>**PSD2-Anforderungen:** <br/>
>Ab dem 14. September 2019 können europäische Banken Zahlungen ablehnen, die nicht erfüllt werden [PSD2](../getting-started/compliance-payment-services-directive.md) Anforderungen. Für die meisten PayPal-Lösungen ist keine Maßnahme erforderlich, um PSD2 zu erfüllen, da diese Anforderungen von PayPal bearbeitet werden.

## PayPal-Geschäftskonto

Um PayPal als Zahlungsmethode in Ihrem Geschäft anzubieten, benötigen Sie eine PayPal [Geschäftskonto][1] oder [PayPal-Payflow-Konto][2]. Die Kontoanforderungen werden in der Beschreibung der einzelnen PayPal-Lösungen angegeben. Ihr PayPal-Handelskonto wird auch für die Verwaltung von [Betrugsfilter](#paypal-fraud-management-filters) , die auf Käufe angewendet werden, die über Ihren Store getätigt werden.

Kunden, die PayPal Express Checkout oder Express Checkout für Payflow Pro verwenden, müssen über ein PayPal-Käuferkonto verfügen. PayPal Payments Standard (Website Payments Standard in einigen Ländern) kann direkt oder über ein Käuferkonto verwendet werden, wenn der Händler _PayPal-Konto optional_. Standardmäßig ist dieser Parameter aktiviert, sodass Kunden ihre Kreditkarteninformationen eingeben oder ein Käuferkonto mit PayPal erstellen können. Wenn diese Option deaktiviert ist, müssen Kunden zunächst ein PayPal-Kaufkonto erstellen, bevor sie einen Kauf tätigen.

Website Payments Pro, Website Payments Pro Payflow Edition, Payflow Pro Gateway und Payflow Link verpflichten Kunden, während des Checkouts Kreditkarteninformationen einzugeben.

## PayPal Credit und PayLater

PayPal PayLater bietet Ihren Kunden schnellen Zugang zu Finanzierungen, sodass sie jetzt kaufen und mit der Zeit zahlen können, ohne dass Sie dafür zusätzliche Kosten haben. Sie werden nicht belastet, wenn Kunden PayPal-Kreditoptionen wählen, und Sie zahlen nur Ihre normale PayPal-Transaktionsgebühr. Weitere Informationen finden Sie unter [PayPal-Website][3].

Steigern Sie Ihren Umsatz bei der Werbung für Finanzierungen. Mit PayPal können Sie Browser mit PayPal PayLater-Finanzierungen zu Käufern machen. Ihre Kunden können mit der Zeit zahlen, während Sie vorher bezahlt werden - ohne zusätzliche Kosten für Sie. Verwenden Sie PayPal kostenlose Banneranzeigen, um PayPal-Finanzierungen als Zahlungsoption zu bewerben, wenn Ihre Kunden mit PayPal auschecken. Das PayPal Advertising Program generiert nachweislich zusätzliche Käufe und erhöht die durchschnittliche Kaufgröße um 15 % oder mehr.

Sie können einfach kostenlose, vorgefertigte Banneranzeigen zu Seiten Ihrer Site und dem _PayPal Credit_ -Schaltfläche in den Warenkorb während des Checkout, um Ihre Kunden daran zu erinnern, dass die Finanzierung sofort verfügbar ist.

>[!NOTE]
>
>Ab Version 2.4.3 wird PayPal PayLater in Implementierungen unterstützt, die PayPal enthalten. Diese Funktion ermöglicht es den Käufern, eine Bestellung in zweiwöchigen Tranchen zu bezahlen, anstatt den vollen Betrag zum Zeitpunkt des Kaufs zu zahlen. Das PayPal-Krediterlebnis wird nicht mehr unterstützt.

Bei US-Händlern ist PayPal-Guthaben standardmäßig für die [PayPal Express Checkout](paypal-express-checkout.md) Zahlungsoption. Informationen zur Deaktivierung dieser Zahlungsmethode finden Sie unter _Funktionen_ Abschnitt [PayPal Express Checkout-Konfiguration](paypal-express-checkout.md#features).

PayPal-Guthaben ist für die anderen PayPal-Zahlungslösungen standardmäßig deaktiviert, kann aber in der Zahlungsmethodenkonfiguration für unterstützende Lösungen aktiviert werden:

- [Zahlungen erweitert](paypal-payments-advanced.md)
- [Payments Pro](paypal-payments-pro.md)
- [Zahlungsstandard](paypal-payments-standard.md)
- [Payflow Pro](paypal-payflow-pro.md)
- [Payflow-Link](paypal-payflow-link.md)

>[!IMPORTANT]
>
>Bevor Sie PayPal-Guthaben oder PayPal PayLater für Ihren Store konfigurieren, stellen Sie sicher, dass es in Ihrem PayPal-Kaufkonto aktiviert ist.

## Integrierte PayPal-Lösungen

Mit PayPal und Adobe Commerce können Sie Zahlungen von allen wichtigen Debit- und Kreditkarten akzeptieren. PayPal bietet zusätzlichen Komfort ohne zusätzlichen Aufwand, da auch Ihre Kunden, die kein PayPal-Konto haben, für ihre Käufe mit PayPal bezahlen können.

>[!NOTE]
>
>Sie können nicht mehrere PayPal-Methoden gleichzeitig in Ihrem Store aktivieren lassen, mit Ausnahme von PayPal Express Checkout. PayPal Express Checkout kann mit anderen Zahlungsmethoden von PayPal verwendet werden, mit Ausnahme von PayPal Payments Standard. Wenn Sie Zahlungslösungen ändern, ist die vorherige Methode deaktiviert.

### PayPal Express Checkout

[PayPal Express Checkout](paypal-express-checkout.md)

### PayPal All-in-One-Zahlungslösungen

In den USA bietet PayPal die folgenden PCI-konformen Lösungen an, um den Anforderungen Ihres wachsenden Unternehmens gerecht zu werden.

- [PayPal Payments Advanced](paypal-payments-advanced.md)
- [PayPal Payments Pro](paypal-payments-pro.md)
- [PayPal Payments Standard](paypal-payments-standard.md)

![PayPal All-in-One-Zahlungslösungen](./assets/paypal-all-in-one.png){width="600" zoomable="yes"}

### PayPal-ZahlungsGateways

Ein Payment Gateway ist ein Händlerdienst, der von einem E-Commerce-Anwendungs-Dienstleister bereitgestellt wird, der Kreditkarten- oder Direktzahlungsvorgänge zulässt. Sie fungieren als Vermittler zwischen Kunden und Banken.

Zahlungskanäle sind in Online- und Offline-Umgebungen verfügbar. Zahlungen können telefonisch, online oder über eine App akzeptiert werden. Die Transaktion wird an das Verarbeitungssystem des Dienstleisters gesendet und dann zur Überprüfung und Bestätigung an die Bank des Kunden gesendet. Bei Überprüfung erhält der Händler die Zahlung, ohne direkten Kontakt mit dem Bankkonto des Kunden zu haben.

Es gibt zwei Arten von Zahlungstüren - direkt und gehostet.

- Direkte Zahlungskanäle ermöglichen es Benutzern, ihre Kartendaten auf der Store-Website einzugeben.
- Gehostete Zahlungskanäle leiten Benutzer zu einer gehosteten Zahlungsseite außerhalb der Store-Website weiter.

Das Payment Gateway bietet Sicherheit und Schutz für alle an einer Transaktion beteiligten Parteien.

PayPal bietet Ihnen zwei Payment Gateway-Lösungen für Ihr Unternehmen an. Sie können PayPal Ihren Zahlungsvorgang auf seiner sicheren Zahlungsseite hosten lassen, oder Sie können die Kontrolle über das gesamte Zahlungserlebnis mit einer anpassbaren Lösung übernehmen.

- [PayPal Payflow Pro](paypal-payflow-pro.md)
- [PayPal-Payflow-Link](paypal-payflow-link.md)

![PayPal-ZahlungsGateways einrichten](./assets/paypal-payment-gateway.png){width="600" zoomable="yes"}

## PayPal-Steuerungs-Filter

PayPal-Steuerungs-Filter erleichtern die Erkennung und Reaktion auf betrügerische Transaktionen und können so konfiguriert werden, dass sie riskantere Zahlungen kennzeichnen, zur Überprüfung halten oder ablehnen. Aktionen im Zusammenhang mit Commerce [Bestellstatus](order-status.md) Werte, die entsprechend den Betrugsfiltereinstellungen geändert wurden:

| Aktion | Ergebnis |
| --- | --- |
| [!UICONTROL Review] | Der verdächtige Befehl erhält den Status _Zahlungsüberprüfung_ wenn die Bestellung aufgegeben wird. Sie können die Bestellung überprüfen und die Zahlung im Admin oder auf der PayPal-Seite genehmigen oder stornieren. Wenn Sie auf **[!UICONTROL Accept Payment]** oder **[!UICONTROL Deny Payment]**, werden keine neuen Transaktionen für die Bestellung erstellt. <br/><br/>Wenn Sie den Status der Transaktion auf der PayPal-Site ändern, müssen Sie auf **[!UICONTROL Get Payment Update]** auf der Seite &quot;Reihenfolge&quot;des Administrators klicken, um die Änderungen anzuwenden. Wenn Sie auf **[!UICONTROL Accept Payment]** oder **[!UICONTROL Deny Payment]**, werden die auf der PayPal-Site vorgenommenen Änderungen übernommen. |
| [!UICONTROL Deny] | Die verdächtige Bestellung kann vom Kunden nicht aufgegeben werden, da die entsprechende Transaktion von PayPal abgelehnt wird. <br/><br/>Um die Zahlung vom Administrator abzulehnen, klicken Sie auf **[!UICONTROL Deny Payment]** in der oberen rechten Ecke der Seite. Der Bestellstatus ändert sich in `Canceled`, wird die Transaktion rückgängig gemacht und die Mittel werden auf dem Kundenkonto freigegeben. Die entsprechenden Informationen werden im _[!UICONTROL Comments History]_-Abschnitt der Bestellansicht. |
| [!UICONTROL Flag] | Der verdächtige Befehl erhält den Status `Processing` wenn sie platziert wird. Die entsprechende Transaktion wird in der Liste der Transaktionen mit Handelskonten mit einer Markierung markiert. |

{style="table-layout:auto"}

## PayPal-Lösungen nach Ländern

| Land | PayPal Zahlungslösung |
|--- |--- |
| Australien | [!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Payflow Pro]](paypal-payflow-pro.md)<br/>[!DNL PayPal Website Payments Pro Hosted Solution]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Kanada | [!DNL PayPal Website Payments Standard]<br/>[!DNL PayPal Website Payments Pro]<br/>[[!DNL PayPal Payflow Pro]](paypal-payflow-pro.md)<br/>[[!DNL PayPal Payflow Link]](paypal-payflow-link.md) (einschließlich Express-Checkout)<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Frankreich | [!DNL PayPal Integral Evolution]<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Deutschland | [[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Hongkong SAR China | [!DNL PayPal Website Payments Pro Hosted Solution]<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Italien | [!DNL PayPal ProPay]<br/>[[!DNL Pal Payments Standard]](paypal-payments-standard.md)<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Japan | [!DNL PayPal Website Payments Plus]<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Neuseeland | [[!DNL PayPal Payflow Pro]](paypal-payflow-pro.md)<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Spanien | [!DNL PayPal Pasarela Integral]<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Vereinigtes | [!DNL PayPal Payments Pro Hosted Solution] (einschließlich Express-Checkout)<br/>[[!DNL PayPal Payments Standard]](paypal-payments-standard.md)<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Vereinigte Staaten | [[!DNL PayPal Payments Advanced]](paypal-payments-advanced.md) (einschließlich Express-Checkout)<br/>[[!DNL PayPal Payments Pro]](paypal-payments-pro.md) (einschließlich Express-Checkout)<br/>[[!DNL PayPal Payments Standard+]](paypal-payments-standard.md)<br/>[[!DNL PayPal Payflow Pro]](paypal-payflow-pro.md) (einschließlich Express-Checkout)<br/>[[!DNL PayPal Payflow Link]](paypal-payflow-link.md) (einschließlich Express-Checkout)<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |

{style="table-layout:auto"}

### Andere Länder

PayPal Express Checkout und PayPal Website Payments Standard sind in den folgenden Ländern verfügbar:

- Argentinien
- Österreich
- Belgien
- Brasilien
- Bulgarien
- Chile
- Costa Rica
- Zypern
- Tschechische Republik
- Dänemark
- Dominikanische Republik
- Equador
- Estland
- Finnland
- Französisch-Guayana
- Gibraltar
- Griechenland
- Guadeloupe
- Ungarn
- Island
- Indien
- Indonesien
- Irland
- Israel
- Jamaika
- Lettland
- Liechtenstein
- Litauen
- Luxemburg
- Malaysia
- Malta
- Martinique
- Mexiko
- Niederlande
- Norwegen
- Philippinen
- Polen
- Portugal
- Réunion
- Rumänien
- San Marino
- Singapur
- Slowakei
- Slowenien
- Südafrika
- Südkorea
- Schweden
- Schweiz
- Taiwan
- Thailand
- Türkei
- Vereinigte Arabische Emirate
- Uruguay
- Venezuela
- Vietnam


[1]: https://manager.paypal.com/
[2]: https://developer.paypal.com/docs/payflow/payflow-gateway/
[3]: https://www.paypal.com/us/business/buy-now-pay-later
