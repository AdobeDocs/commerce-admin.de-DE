---
title: PSD2-Konformität
description: Erfahren Sie mehr über die Anforderungen der Zahlungsdiensterichtlinie (PSD2), die sich auf Ihren Shop auswirken könnten.
exl-id: efe94cac-a170-48df-88cf-36019ca52951
feature: Compliance
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 0%

---

# PSD2-Konformität

Ab dem 14. September 2019 verlangt die Europäische Union, dass alle Händler in der EU und im Vereinigten Königreich die [Strong Customer Authentication](https://www.cardinalcommerce.com/content-hub/mandates/psd2-sca/understanding-psd2-sca) (SCA)-Anforderungen der Zahlungsdiensterichtlinie (PSD2) erfüllen. Händler in allen anderen Ländern werden ermutigt, PSD2 als Best Practice einzuhalten.

>[!NOTE]
>
>Dieses Thema dient nur zu Informationszwecken und ist nicht als Rechtsberatung zu verstehen. Um festzustellen, ob und wie Ihr Unternehmen rechtliche Verpflichtungen einhalten sollte, wenden Sie sich an Ihren Rechtsbeistand.

Eine starke Kundenauthentifizierung ist eine Schlüsselkomponente von PSD2 und erfordert zwei der folgenden Schritte:

- Etwas, das nur der Kunde hat (Passwort oder PIN)
- Etwas, das nur der Kunde kennt (eindeutiges Sicherheits-Token, das vom Telefon oder Schlüsselfob generiert wird)
- Etwas, das nur der Kunde ist (biometrische Authentifizierung wie Fingerabdruck oder Gesichtserkennung)

Europäische Banken können Zahlungen ablehnen, die die Anforderungen nicht erfüllen. Transaktionen mit geringem Risiko und geringem Wert können jedoch weiterhin akzeptiert werden, und nachfolgende Zahlungen können in einem wiederkehrenden Abonnement erfolgen.

Aufgrund dieser wichtigen Änderung und um sicherzustellen, dass Kundenzahlungen nicht abgelehnt werden, führte Adobe die folgenden Änderungen und Empfehlungen für native [!DNL Commerce]-Zahlungsintegrationen ein.

| Zahlungsmethode | Compliance Requirements |
|--- |--- |
| [PayPal](../stores-purchase/paypal.md) | Bei den meisten PayPal-Lösungen ist keine Handlung erforderlich, um PSD2 einzuhalten, da die Anforderungen von PayPal bearbeitet werden. Informationen zu bestimmten Lösungen finden Sie im Hinweis oben in jedem PayPal-Thema. |
| [Braintree](../stores-purchase/braintree.md) | Ab der Umstellung auf die installierte Erweiterung in 2.4.0 werden die Anforderungen innerhalb des enthaltenen Braintree Payments-Moduls gehandhabt und es sind keine Maßnahmen erforderlich, um PSD2 zu erfüllen. <br /><br />**_Hinweis:_**&#x200B;Führen Sie einen der folgenden Schritte aus, um PSD2 mithilfe der Kernintegration früherer Versionen einzuhalten:<br/>- (Empfohlen) Installieren Sie die offizielle Braintree-Zahlungsintegrationserweiterung von [[!DNL Adobe Commerce Marketplace]](https://marketplace.magento.com/catalogsearch/result/?q=braintree#q=braintree&amp;idx=m2_cloud_prod_default_products&amp;p=0&amp;nR%5Bvisibility_search%5D%5B%3D%5D%5B0%5D=1){:target="_blank"}.<br/>- Aktivieren und konfigurieren Sie die Braintree-Zahlungsmethode in der [!DNL Commerce].<br/><br/>Diese früheren Kernintegrationen unterstützen die 3D Secure 2.0-Verifizierung. Braintree-Implementierungen, die auf JavaScript SDK v2 ausgeführt werden, unterstützen jedoch nicht 3D Secure 2.0. |
| Sonstige | Überprüfen Sie für alle anderen Zahlungsintegrationen die verfügbaren Erweiterungen auf [[!DNL Commerce Marketplace]](https://marketplace.magento.com/extensions/payments-security/payment-integration.html?_ga=2.108129217.2105547619.1564067043-238341041.1564067043){:target="_blank"}. Bitten Sie Ihren Zahlungsanbieter, eine Lösung für die Unterstützung von PSD2-Anforderungen zu empfehlen. |

{style="table-layout:auto"}
