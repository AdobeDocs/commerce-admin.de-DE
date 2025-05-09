---
title: PayPal-Zahlungslösungen
description: Erfahren Sie mehr über die Integrationen der PayPal-Zahlungslösung, die für Ihren Shop verfügbar sind.
exl-id: d447b98e-d30c-4759-9ae0-94ccbeed9ba4
feature: Payments
badgePaas: label="Nur PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Gilt nur für Adobe Commerce in Cloud-Projekten (von Adobe verwaltete PaaS-Infrastruktur) und lokale Projekte."
source-git-commit: cd5b5ebec6e72ab4ba9de775bcfe8f8a89fbbb93
workflow-type: tm+mt
source-wordcount: '1247'
ht-degree: 0%

---

# PayPal-Zahlungslösungen

PayPal ist ein weltweit führender Anbieter von Online-Zahlungen und bietet Ihren Kunden eine schnelle und sichere Möglichkeit, online zu bezahlen. Die Auswahl der verfügbaren PayPal-Lösungen variiert je nach Standort des Händlers. PayPal Express Checkout und PayPal Payments Standard können in allen Teilen der Welt verwendet werden. Weitere Informationen finden Sie unter [PayPal-Lösungen nach Land](#paypal-solutions-by-country).

>[!IMPORTANT]
>
>**PSD2-Anforderungen:** <br/>
>Ab dem 14. September 2019 können europäische Banken Zahlungen ablehnen, die [PSD2}-](../getting-started/compliance-payment-services-directive.md) nicht erfüllen. Bei den meisten PayPal-Lösungen ist keine Maßnahme erforderlich, um PSD2 einzuhalten, da diese Anforderungen von PayPal erfüllt werden.

## PayPal-Geschäftskonto

Um PayPal als Zahlungsmethode in Ihrem Geschäft anzubieten, müssen Sie über ein PayPal [Geschäftskonto][1] und/oder ein [PayPal Payflow-Konto][2] verfügen. Die Kontoanforderungen sind in der Beschreibung jeder PayPal-Lösung angegeben. Ihr PayPal-Händlerkonto wird auch zur Verwaltung von [Betrugsfiltern](#paypal-fraud-management-filters) verwendet, die auf Käufe aus Ihrem Geschäft angewendet werden.

Kunden, die PayPal Express Checkout oder Express Checkout für Payflow Pro verwenden, müssen über ein PayPal-Kaufkonto verfügen. PayPal Payments Standard (Website Payments Standard in einigen Ländern) kann direkt oder über ein Käuferkonto verwendet werden, wenn der Händler _PayPal-Konto optional_ aktiviert. Standardmäßig ist dieser Parameter aktiviert, sodass Kunden ihre Kreditkarteninformationen eingeben oder ein Kundenkonto bei PayPal erstellen können. Wenn diese Option deaktiviert ist, müssen Kunden vor einem Kauf zunächst ein PayPal-Kaufkonto erstellen.

Website Payments Pro, Website Payments Pro Payflow Edition, Payflow Pro Gateway und Payflow Link erfordern, dass Kunden während des Checkouts Kreditkarteninformationen eingeben.

## PayPal-Guthaben und PayLater

PayPal PayLater bietet Ihren Kunden schnellen Zugang zu Finanzierungen, sodass sie jetzt kaufen und im Laufe der Zeit bezahlen können, ohne zusätzliche Kosten für Sie. Sie werden nicht belastet, wenn Kunden PayPal-Kreditoptionen wählen, und Sie zahlen nur Ihre normale PayPal-Transaktionsgebühr. Weitere Informationen finden Sie auf der [PayPal-Website][3].

Schaffen Sie Ihren Verkäufen einen Schub, wenn Sie mit Finanzierungen werben. Mit PayPal können Browser durch die Finanzierung mit PayPal Later zu Käufern werden. Ihre Kunden können im Laufe der Zeit bezahlen, während Sie im Voraus bezahlt werden - ohne zusätzliche Kosten für Sie. Verwenden Sie kostenlose PayPal-Bannerwerbung, um die PayPal-Finanzierung als Zahlungsoption anzuzeigen, wenn Ihre Kunden mit PayPal auschecken. Es hat sich gezeigt, dass das PayPal Advertising-Programm zusätzliche Käufe generiert und die durchschnittliche Kaufgröße um 15 % oder mehr erhöht.

Sie können kostenlos vorgefertigte Bannerwerbung auf Seiten Ihrer Website und die Schaltfläche _PayPal-Guthaben_ während des Checkouts einfach in Ihren Warenkorb legen, um Ihre Kunden daran zu erinnern, dass eine Finanzierung jederzeit verfügbar ist.

>[!NOTE]
>
>Ab Version 2.4.3 wird PayPal Later in Bereitstellungen unterstützt, die PayPal enthalten. Mit dieser Funktion können Käufer eine Bestellung in zweiwöchentlichen Raten bezahlen, anstatt den vollen Betrag zum Zeitpunkt des Kaufs zu bezahlen. Das PayPal-Krediterlebnis ist veraltet.

Für US-Händler ist PayPal Credit standardmäßig für die Zahlungsoption [PayPal Express Checkout](paypal-express-checkout.md) aktiviert. Informationen zur Deaktivierung für diese Zahlungsmethode finden Sie im Abschnitt _Funktionen_ der [PayPal Express-Checkout-Konfiguration](paypal-express-checkout.md#features).

PayPal-Guthaben ist für die anderen PayPal-Zahlungslösungen standardmäßig deaktiviert, kann aber in der Zahlungsmethode-Konfiguration für unterstützende Lösungen aktiviert werden:

- [Vorauszahlungen](paypal-payments-advanced.md)
- [Zahlungen pro](paypal-payments-pro.md)
- [Zahlungsstandard](paypal-payments-standard.md)
- [Payflow Pro](paypal-payflow-pro.md)
- [Payflow-Link](paypal-payflow-link.md)

>[!IMPORTANT]
>
>Bevor Sie PayPal Credit oder PayPal PayLater für Ihren Shop konfigurieren, stellen Sie sicher, dass es in Ihrem PayPal-Händlerkonto aktiviert ist.

## Integrierte PayPal-Lösungen

Mit PayPal und Adobe Commerce können Sie Zahlungen von allen gängigen Debit- und Kreditkarten akzeptieren. PayPal bietet zusätzlichen Komfort ohne zusätzlichen Aufwand, da auch Ihre Kunden, die kein PayPal-Konto haben, für ihre Käufe mit PayPal bezahlen können.

>[!NOTE]
>
>Sie können nicht mehr als eine PayPal-Methode gleichzeitig in Ihrem Geschäft aktiviert haben, außer für den PayPal Express-Checkout. PayPal Express Checkout kann mit anderen PayPal-Zahlungsmethoden verwendet werden, mit Ausnahme von PayPal Payments Standard. Wenn Sie Zahlungslösungen ändern, wird die vorherige Methode deaktiviert.

### PayPal Express-Checkout

[PayPal Express-Checkout](paypal-express-checkout.md)

### PayPal All-in-One-Zahlungslösungen

In den USA bietet PayPal die folgenden PCI-kompatiblen Lösungen, um die Anforderungen Ihres wachsenden Unternehmens zu erfüllen.

- [PayPal-Zahlungen - Erweitert](paypal-payments-advanced.md)
- [PayPal Payments Pro](paypal-payments-pro.md)
- [PayPal-Zahlungsstandard](paypal-payments-standard.md)

![PayPal-All-in-One-Zahlungslösungen](./assets/paypal-all-in-one.png){width="600" zoomable="yes"}

### PayPal-Zahlungs-Gateways

Ein Zahlungs-Gateway ist ein Handelsdienst, der von einem E-Commerce-Anwendungs-Dienstleister bereitgestellt wird, der die Verarbeitung von Kreditkarten oder Direktzahlungen autorisiert. Sie fungieren als Vermittler zwischen Kunden und Banken.

Zahlungs-Gateways sind in Online- und Offline-Umgebungen verfügbar. Zahlungen können telefonisch, online oder über eine Mobile App akzeptiert werden. Die Transaktion wird an das Verarbeitungssystem des Dienstleisters gesendet und dann zur Überprüfung und Bestätigung an die Bank des Kunden gesendet. Bei Bestätigung erhält der Händler die Zahlung, ohne direkten Kontakt mit dem Bankkonto des Kunden zu haben.

Es gibt zwei Arten von Zahlungs-Gateways - direkt und gehostet.

- Über Direktzahlungs-Gateways können Benutzer ihre Kartendaten auf der Store-Website eingeben.
- Gehostete Zahlungs-Gateways leiten Benutzer zu einer gehosteten Zahlungsseite außerhalb der Store-Website weiter.

Das Payment Gateway bietet Sicherheit und Schutz für alle an einer Transaktion beteiligten Parteien.

PayPal bietet zwei Payment Gateway-Lösungen für Ihr Unternehmen. Sie können PayPal Ihre Kasse auf seiner sicheren Zahlungsseite hosten lassen, oder Sie können mit einer anpassbaren Lösung die Kontrolle über das gesamte Zahlungserlebnis übernehmen.

- [PayPal Payflow Pro](paypal-payflow-pro.md)
- [PayPal-Payflow-Link](paypal-payflow-link.md)

![Einrichten von PayPal-Zahlungs-Gateways](./assets/paypal-payment-gateway.png){width="600" zoomable="yes"}

## PayPal-Betrugsmanagementfilter

PayPal-Filter zur Betrugsverwaltung erleichtern die Erkennung und Reaktion auf betrügerische Transaktionen und können so konfiguriert werden, dass riskantere Zahlungen markiert, zur Überprüfung gespeichert oder verweigert werden. Die mit Commerce [Bestellstatus) ](order-status.md) Werte wurden entsprechend den Einstellungen für den Betrugsfilter geändert:

| Aktion | Ergebnis |
| --- | --- |
| [!UICONTROL Review] | Die verdächtige Bestellung erhält den Status _Zahlungsüberprüfung_ wenn die Bestellung aufgegeben wird. Sie können die Bestellung überprüfen und die Zahlung im Admin oder auf der PayPal-Seite genehmigen oder stornieren. Wenn Sie auf **[!UICONTROL Accept Payment]** oder **[!UICONTROL Deny Payment]** klicken, werden keine neuen Transaktionen für die Bestellung erstellt. <br/><br/>Wenn Sie den Status der Transaktion auf der PayPal-Website ändern, müssen Sie auf der Seite Bestellung des Administrators auf **[!UICONTROL Get Payment Update]** klicken, um die Änderungen anzuwenden. Wenn Sie auf **[!UICONTROL Accept Payment]** oder **[!UICONTROL Deny Payment]** klicken, werden die auf der PayPal-Website vorgenommenen Änderungen übernommen. |
| [!UICONTROL Deny] | Der Verdachtsauftrag kann vom Kunden nicht erteilt werden, da die entsprechende Transaktion von PayPal abgelehnt wird. <br/><br/>Um die Zahlung vom Administrator abzulehnen, klicken Sie oben rechts auf der Seite auf **[!UICONTROL Deny Payment]** . Der Bestellstatus ändert sich in `Canceled`, die Transaktion wird rückgängig gemacht und das Guthaben wird auf dem Kundenkonto freigegeben. Die entsprechenden Informationen werden im _[!UICONTROL Comments History]_Abschnitt der Bestellansicht hinzugefügt. |
| [!UICONTROL Flag] | Der Status der verdächtigen Bestellung wird bei ihrer Platzierung `Processing`. Die entsprechende Transaktion ist in der Liste der Händlerkontobuchungen mit einer Markierung gekennzeichnet. |

{style="table-layout:auto"}

## PayPal-Lösungen nach Land

| Land | PayPal-Zahlungslösung |
|--- |--- |
| Australien | [!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Payflow Pro]](paypal-payflow-pro.md)<br/>[!DNL PayPal Website Payments Pro Hosted Solution]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Kanada | [!DNL PayPal Website Payments Standard]<br/>[!DNL PayPal Website Payments Pro]<br/>[[!DNL PayPal Payflow Pro]](paypal-payflow-pro.md)<br/>[[!DNL PayPal Payflow Link]](paypal-payflow-link.md) (einschließlich Express-Checkout)<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Frankreich | [!DNL PayPal Integral Evolution]<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Deutschland | [[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Sonderverwaltungsregion Hongkong China | [!DNL PayPal Website Payments Pro Hosted Solution]<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Italien | [!DNL PayPal ProPay]<br/>[[!DNL Pal Payments Standard]](paypal-payments-standard.md)<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Japan | [!DNL PayPal Website Payments Plus]<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Neuseeland | [[!DNL PayPal Payflow Pro]](paypal-payflow-pro.md)<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Spanien | [!DNL PayPal Pasarela Integral]<br/>[!DNL PayPal Website Payments Standard]<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
| Vereinigtes Königreich | [!DNL PayPal Payments Pro Hosted Solution] (einschließlich Express-Checkout)<br/>[[!DNL PayPal Payments Standard]](paypal-payments-standard.md)<br/>[[!DNL PayPal Express Checkout]](paypal-express-checkout.md) |
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
- Ecuador
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
