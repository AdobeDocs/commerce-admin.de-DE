---
title: PSD2-Konformität
description: Erfahren Sie mehr über die Anforderungen der Zahlungsdienstrichtlinie (PSD2), die sich auf Ihren Store auswirken könnten.
exl-id: efe94cac-a170-48df-88cf-36019ca52951
feature: Compliance
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '392'
ht-degree: 0%

---

# PSD2-Konformität

Ab dem 14. September 2019 verlangt die Europäische Union, dass alle Händler in der EU und im Vereinigten Königreich die [Starke Kundenauthentifizierung](https://www.cardinalcommerce.com/content-hub/mandates/psd2-sca/understanding-psd2-sca) (SCA) Anforderungen der Zahlungsdiensterichtlinie (PSD 2). Händler in allen anderen Ländern werden aufgefordert, PSD 2 als Best Practice einzuhalten.

>[!NOTE]
>
>Dieses Thema dient nur zu Informationszwecken und sollte nicht als Rechtsberatung ausgelegt werden. Wenden Sie sich an Ihren Rechtsbeistand, um festzustellen, ob und wie Ihr Unternehmen rechtliche Verpflichtungen einhalten sollte.

Eine starke Kundenauthentifizierung ist eine Schlüsselkomponente von PSD2 und erfordert zwei der folgenden Voraussetzungen:

- Nur etwas, das der Kunde hat (Passwort oder PIN)
- Irgendetwas, das nur dem Kunden bekannt ist (eindeutiges Sicherheits-Token, das vom Telefon oder von der Tastenkombination &quot;fob&quot;generiert wurde)
- Etwas, das nur der Kunde ist (biometrische Authentifizierung, z. B. Fingerabdruck oder Gesichtserkennung)

Europäische Banken können Zahlungen ablehnen, die nicht den Anforderungen entsprechen. Es können jedoch weiterhin Transaktionen mit geringem Risiko und geringem Wert akzeptiert werden und nachfolgende Zahlungen in einem wiederkehrenden Abonnement.

Aufgrund dieser erheblichen Änderung und um sicherzustellen, dass Kundenzahlungen nicht abgelehnt werden, führte Adobe die folgenden Änderungen und Empfehlungen für native Produkte ein [!DNL Commerce] Zahlungsintegrationen.

| Zahlungsmethode | Konformitätsanforderungen |
|--- |--- |
| [PayPal](../stores-purchase/paypal.md) | Für die meisten PayPal-Lösungen ist keine Maßnahme erforderlich, um PSD2 zu erfüllen, da die Anforderungen von PayPal bearbeitet werden. Informationen zu bestimmten Lösungen finden Sie in der Notiz oben in jedem PayPal-Thema. |
| [Braintree](../stores-purchase/braintree.md) | Ab der Umstellung auf die installierte Erweiterung in Version 2.4.0 werden die Anforderungen innerhalb des enthaltenen Braintree Payments-Moduls bearbeitet und es ist keine Maßnahme erforderlich, um PSD2 zu erfüllen. <br /><br />**_Hinweis:_**Führen Sie einen der folgenden Schritte aus, um PSD 2 mithilfe der Kernintegration in früheren Versionen zu erfüllen:<br/>- (Empfohlen) Installieren Sie die offizielle Braintree Payment Integration-Erweiterung von [[!DNL Adobe Commerce Marketplace]](https://marketplace.magento.com/catalogsearch/result/?q=braintree#q=braintree&amp;idx=m2_cloud_prod_default_products&amp;p=0&amp;nR%5Bvisibility_search%5D%5B%3D%5D%5B0%5D=1){:target=&quot;_blank&quot;}.<br/>- Aktivieren und konfigurieren Sie die Braintree-Zahlungsmethode im [!DNL Commerce] Konfiguration.<br/><br/>Diese früheren Kernintegrationen unterstützen die Verifizierung von 3D Secure 2.0. Braintree-Implementierungen, die mit JavaScript SDK v2 ausgeführt werden, unterstützen jedoch nicht 3D Secure 2.0. |
| Sonstiges | Überprüfen Sie für alle anderen Zahlungsintegrationen die verfügbaren Erweiterungen unter [[!DNL Commerce Marketplace]](https://marketplace.magento.com/extensions/payments-security/payment-integration.html?_ga=2.108129217.2105547619.1564067043-238341041.1564067043){:target=&quot;_blank&quot;}. Bitten Sie Ihren Zahlungsdienstleister, eine Lösung zur Unterstützung von PSD2-Anforderungen zu empfehlen. |

{style="table-layout:auto"}
