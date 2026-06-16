---
title: PSD2-Konformität
description: Erfahren Sie mehr über die Anforderungen der Zahlungsdiensterichtlinie (PSD2), die sich auf Ihren Shop auswirken könnten.
exl-id: efe94cac-a170-48df-88cf-36019ca52951
feature: Compliance
TQID: https://experienceleague.adobe.com/paVa-tpYYzrINAPRFs4TOzbp4b4CLJDlxqNlL1gzp2Q
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: b5f00040-57a0-4a6d-a39e-383b1936c2c9
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: c32adafa-ed01-4b31-997e-2413013911b0
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2:
  - id: f0ca7b10-ef6c-4ee4-b63f-030819bdd1f3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 396
ht-degree: 0%

---

# PSD2-Konformität

Ab dem 14. September 2019 verlangt die Europäische Union, dass alle Händler in der EU und im Vereinigten Königreich die [Strong Customer Authentication](https://www.cardinalcommerce.com/content-hub/mandates/psd2-sca/understanding-psd2-sca) (SCA)-Anforderungen der Zahlungsdiensterichtlinie (PSD2) erfüllen. Händler in allen anderen Ländern werden ermutigt, PSD2 als Best Practice einzuhalten.

>[!NOTE]
>
>Dieses Thema dient nur zu Informationszwecken und ist nicht als Rechtsberatung zu verstehen. Um festzustellen, ob und wie Ihr Unternehmen rechtliche Verpflichtungen einhalten sollte, wenden Sie sich an Ihren Rechtsbeistand.

Eine starke Kundenauthentifizierung ist eine Schlüsselkomponente von PSD2 und erfordert zwei der folgenden Maßnahmen:

- Etwas, das nur der Kunde hat (Passwort oder PIN)
- Etwas, das nur der Kunde kennt (eindeutiges Sicherheits-Token, das vom Telefon oder Schlüsselfob generiert wird)
- Etwas, das nur der Kunde ist (biometrische Authentifizierung wie Fingerabdruck oder Gesichtserkennung)

Europäische Banken können Zahlungen ablehnen, die die Anforderungen nicht erfüllen. Transaktionen mit geringem Risiko und geringem Wert können jedoch weiterhin akzeptiert werden, und nachfolgende Zahlungen können in einem wiederkehrenden Abonnement erfolgen.

Aufgrund dieser wichtigen Änderung und um sicherzustellen, dass Kundenzahlungen nicht abgelehnt werden, hat Adobe die folgenden Änderungen und Empfehlungen für native [!DNL Commerce]-Zahlungsintegrationen eingeführt.

| Zahlungsmethode | Compliance Requirements |
|--- |--- |
| [PayPal](../stores-purchase/paypal.md) | Bei den meisten PayPal-Lösungen ist keine Maßnahme erforderlich, um PSD2 einzuhalten, da die Anforderungen von PayPal bearbeitet werden. Informationen zu bestimmten Lösungen finden Sie im Hinweis oben in jedem PayPal-Thema. |
| [Braintree](../stores-purchase/braintree.md) | Ab der Umstellung auf die installierte Erweiterung in 2.4.0 werden die Anforderungen innerhalb des enthaltenen Braintree Payments-Moduls gehandhabt und es sind keine Maßnahmen erforderlich, um PSD2 zu erfüllen. <br /><br />**_Hinweis:_** Führen Sie einen der folgenden Schritte aus, um PSD2 mithilfe der Kernintegration früherer Versionen zu erfüllen:<br/>- (Empfohlen) Installieren Sie die offizielle Braintree-Zahlungsintegrationserweiterung von [[!DNL Adobe Commerce Marketplace]](https://marketplace.magento.com/catalogsearch/result/?q=braintree#q=braintree&idx=m2_cloud_prod_default_products&p=0&nR%5Bvisibility_search%5D%5B%3D%5D%5B0%5D=1){:target="_blank"}.<br/>- Aktivieren und konfigurieren Sie die Braintree-Zahlungsmethode in der [!DNL Commerce].<br/><br/>Diese früheren Kernintegrationen unterstützen die 3D Secure 2.0-Verifizierung. Braintree-Implementierungen, die auf JavaScript SDK v2 ausgeführt werden, unterstützen jedoch nicht 3D Secure 2.0. |
| Sonstige | Überprüfen Sie für alle anderen Zahlungsintegrationen die verfügbaren Erweiterungen auf [[!DNL Commerce Marketplace]](https://marketplace.magento.com/extensions/payments-security/payment-integration.html?_ga=2.108129217.2105547619.1564067043-238341041.1564067043){:target="_blank"}. Bitten Sie Ihren Zahlungsanbieter, eine Lösung für die Unterstützung von PSD2-Anforderungen zu empfehlen. |

{style="table-layout:auto"}
