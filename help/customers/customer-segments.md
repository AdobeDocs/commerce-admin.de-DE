---
title: Kundensegmente
description: Mit Kundensegmenten können Sie bestimmten Kunden Inhalte und Promotions dynamisch anzeigen.
exl-id: b254a6ac-cb0b-46c1-9ef7-ffc97360a98e
TQID: https://experienceleague.adobe.com/K10qvsYlYebR6fJG8-QNI5qrqwjE-Sn-kSxzfiuoXdo
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: c1256247-af4b-46d8-9dca-0c654ecfa157
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 492
ht-degree: 0%

---

# Kundensegmente

Mit Kundensegmenten können Sie bestimmten Kunden basierend auf verschiedenen Eigenschaften dynamisch Inhalte und Promotions anzeigen. Einige Beispiele sind die Kundenadresse, der Bestellverlauf und der Inhalt des Warenkorbs. Sie können Marketing-Initiativen basierend auf zielgerichteten Segmenten mit Preisregeln für den Warenkorb optimieren. Sie können auch Berichte generieren und die Liste der Zielkunden exportieren. Da Kundensegmentinformationen ständig aktualisiert werden, können Kunden mit einem Segment verknüpft und von ihm getrennt werden, wenn sie in Ihrem Geschäft einkaufen.

Um den Unterschied zwischen [Kundengruppen](../customers/customer-groups.md) und Kundensegmenten besser zu verstehen, notieren Sie sich, wo sie verwendet werden:

|  | Kundensegment | Kundengruppe |
|--- |--- |--- |
| Katalogpreisregel |  | ✔️ |
| Warenkorb-Preisregel | ✔️ | ✔️ |
| Stückpreis |  | ✔️ |
| Zugehörige Produktregel | ✔️ |  |
| Dynamischer Block | ✔️ |  |
| Belohnungswechselkurse |  | ✔️ |
| Kategorieberechtigungen |  | ✔️ |
| Einladungen |  | ✔️ |

{style="table-layout:auto"}

## Segmentattribute des Kunden

Segmentattribute für Kunden werden auf ähnliche Weise wie Warenkorb- und Katalogpreisregeln definiert. Damit ein Attribut in einer Kundensegmentbedingung verwendet werden kann, muss _[!UICONTROL Use in Customer Segment]_[Eigenschaft](attribute-properties.md#) auf `Yes` gesetzt sein. Kundensegmentbedingungen können die folgenden Arten von Attributen enthalten:

| Attribut | Beschreibung |
|---|---|
| `Customer Address Fields` | Sie können jedes der Adressfelder definieren, z. B. Stadt oder Land. Jede Adresse im Adressbuch eines Kunden kann diese Bedingungen erfüllen, damit der Kunde sie erfüllt. Sie können auch festlegen, dass nur die standardmäßigen Abrechnungs- oder Versandadressen für die Zuordnung zu einem Kunden verwendet werden können. Kundenadressenattribute sind nur für Kunden verfügbar, die bei ihren Konten angemeldet sind. |
| `Customer Information Fields` | Es können verschiedene Kundeninformationen definiert werden, einschließlich Kundengruppe, Name, E-Mail, Newsletter-Abonnementstatus und Kontostand speichern. Kundeninformationen stehen nur Kunden zur Verfügung, die bei ihren Konten angemeldet sind. |
| `Cart Fields` | Die Warenkorbeigenschaften können entweder auf der Menge (Zeileneinträge oder Gesamtmenge) oder dem Wert (wie Gesamtsumme, Steuer und Geschenkkarte) des Warenkorbinhalts basieren. |
| `Products` | Sie können auf Produkte verweisen, die sich derzeit im Warenkorb oder auf der Wunschliste befinden oder die bereits angesehen oder bestellt wurden. Sie können auch einen Datumsbereich festlegen, in dem es aufgetreten ist. Die Produkte werden mithilfe von Produktattributen definiert. |
| `Order Fields` | Die Bestellmerkmale vergangener Bestellungen können anhand der Rechnungs-/Lieferadresse der Bestellung, des Gesamtbetrags (oder Durchschnitts) oder der Menge der Bestellungen oder der Gesamtzahl der Bestellungen definiert werden. Sie können auch einen Datumsbereich für den Zeitpunkt und den Bestellstatus der Bestellungen festlegen, die diesen Bedingungen entsprechen. Nur für angemeldete Kunden verfügbar. Bedingungen, die für nicht angemeldete Kunden festgelegt sind, funktionieren nach der Anmeldung nicht mehr. |

{style="table-layout:auto"}

Weitere [ zum Definieren von Kundensegmenten finden Sie ](../customers/customer-segment-create.md) „Kundensegmente erstellen und löschen“.

## eBooks

- **Kundensegmentierung** - Holen Sie sich das [eBook](https://business.adobe.com/resources/identifying-your-most-profitable-customers-introduction-customer-segmentation.html), um zu erfahren, wie Sie Ihre Gewinne und die Kundenzufriedenheit insgesamt steigern können.
- **Segmentierungstaktiken** - Holen Sie sich das [eBook](https://business.adobe.com/resources/3-segmentation-tactics-ignite-conversion.html), um das Targeting Ihrer Nachrichten und Werbeaktionen zu verbessern und aussagekräftige Konversationen mit Ihren Kunden zu erstellen.
