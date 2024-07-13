---
title: Kundensegmente
description: Mit Kundensegmenten können Sie Inhalte und Promotions für bestimmte Kunden dynamisch anzeigen.
exl-id: b254a6ac-cb0b-46c1-9ef7-ffc97360a98e
source-git-commit: 0b9f394a792171e93ee72f3b4ebb904b96ea1051
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 0%

---

# Kundensegmente

Mit Kundensegmenten können Sie bestimmten Kunden basierend auf verschiedenen Eigenschaften Inhalte und Promotions dynamisch anzeigen. Beispiele sind Kundenadresse, Bestellverlauf und Warenkorbinhalte. Sie können Marketinginitiativen anhand von zielgerichteten Segmenten mit Warenkorbpreisregeln optimieren. Sie können auch Berichte erstellen und die Liste der Zielkunden exportieren. Da Kundensegmentinformationen ständig aktualisiert werden, können Kunden beim Einkauf in Ihrem Geschäft mit einem Segment verknüpft und von diesem getrennt werden.

Um den Unterschied zwischen [Kundengruppen](../customers/customer-groups.md) und Kundensegmenten besser zu verstehen, beachten Sie, wo sie verwendet werden:

|  | Kundensegment | Kundengruppe |
|--- |--- |--- |
| Katalogpreisregel |  | ✔️ |
| Preisregel für Warenkorb | ✔️ | ✔️ |
| Stückpreis |  | ✔️ |
| Verwandte Produktregel | ✔️ |  |
| Dynamischer Block | ✔️ |  |
| Wechselkurse |  | ✔️ |
| Kategorienberechtigungen |  | ✔️ |
| Einladungen |  | ✔️ |

{style="table-layout:auto"}

## Kundensegmentattribute

Kundensegmentattribute werden ähnlich wie Einkaufswagen- und Katalogpreisregeln definiert. Damit ein Attribut in einer Bedingung für Kundensegmente verwendet werden kann, muss die Eigenschaft _[!UICONTROL Use in Customer Segment]_[property](attribute-properties.md#) auf `Yes` gesetzt werden. Kundensegmentbedingungen können die folgenden Attributtypen enthalten:

| Attribut | Beschreibung |
|---|---|
| `Customer Address Fields` | Sie können jedes Adressfeld definieren, z. B. Stadt oder Land. Jede Adresse im Adressbuch eines Kunden kann diesen Bedingungen entsprechen, damit der Kunde sie erfüllt. Sie können auch festlegen, dass nur die standardmäßigen Abrechnungs- oder Versandadressen für die Übereinstimmung mit einem Kunden verwendet werden können. Kundenadressattribute stehen nur Kunden zur Verfügung, die bei ihren Konten angemeldet sind. |
| `Customer Information Fields` | Es können verschiedene Kundeninformationen definiert werden, darunter Kundengruppe, Name, E-Mail, Newsletter-Abonnementstatus und Kontoguthaben. Kundeninformationen sind nur für Kunden verfügbar, die bei ihren Konten angemeldet sind. |
| `Cart Fields` | Die Eigenschaften des Warenkorbs können entweder auf der Menge (Zeileneinträge oder Gesamtmenge) oder dem Wert (Gesamtsumme, Steuern und Geschenkkarte) des Warenkorbinhalts basieren. |
| `Products` | Sie können auf Produkte verweisen, die sich derzeit im Warenkorb oder in der Wunschliste befinden oder die zuvor angesehen oder bestellt wurden. Sie können auch einen Datumsbereich festlegen, in dem er aufgetreten ist. Die Produkte werden mithilfe von Produktattributen definiert. |
| `Order Fields` | Bestellmerkmale für vergangene Bestellungen können auf Basis der Rechnungsstellungs-/Lieferadresse in der Bestellung, der Gesamtbestellmenge (oder des Durchschnitts) oder der Gesamtbestellmenge bestimmt werden. Sie können auch einen Datumsbereich für den Zeitpunkt des Auftretens und den Bestellstatus der Bestellungen festlegen, die diesen Bedingungen entsprechen. Nur für Kunden verfügbar, die angemeldet sind. Bedingungen, die für nicht angemeldete Käufer festgelegt wurden, funktionieren nicht mehr, wenn sie sich anmelden. |

{style="table-layout:auto"}

Weitere Informationen zur Definition von Kundensegmenten finden Sie unter [Erstellen und Löschen von Kundensegmenten](../customers/customer-segment-create.md) .

## eBooks

- **Kundensegmentierung** - Rufen Sie das [eBook](https://business.adobe.com/resources/identifying-your-most-profitable-customers-introduction-customer-segmentation.html) ab, um zu erfahren, wie Sie den Gewinn und die Kundenzufriedenheit insgesamt steigern können.
- **Segmentierungstaktiken** - Besorgen Sie sich das [eBook](https://business.adobe.com/resources/3-segmentation-tactics-ignite-conversion.html), um das Targeting Ihrer Nachrichten und Promotions zu verbessern und sinnvolle Gespräche mit Ihren Kunden zu führen.
