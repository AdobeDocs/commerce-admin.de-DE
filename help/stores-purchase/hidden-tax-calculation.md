---
title: Ausgeblendete Steuerberechnung
description: Erfahren Sie, wie Sie eine versteckte Steuerberechnung konfigurieren, wenn ein Rabatt vorhanden ist, in den Steuern eingebettet sind.
exl-id: be2000b1-09d7-4a28-814a-f5da7591e387
feature: Invoices, Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Ausgeblendete Steuerberechnung

_Versteckte Steuer_ ist der Mehrwertsteuerbetrag, den ein Rabattbetrag hat. Sie ist ungleich null, wenn alle diese Bedingungen erfüllt sind:

- Katalogpreise inklusive Steuer
- Der Mehrwertsteuersatz liegt nicht bei null
- Es ist ein Rabatt vorhanden

Wenn es einen Rabatt gibt, in den eine Steuer eingebettet ist, berechnet Commerce eine _versteckte_), die zur Berechnung des reduzierten Preises zurückaddiert wird.

`discountedItemPrice = fullPriceWithoutTax - discountAmountOnFullPriceWithoutTax + vatAmountOnDiscountedPrice + hiddenTax`

## Beispiel

1. Voller Preis des Artikels, mit Steuer inbegriffen: $100
1. MwSt.: 20 %
1. Rabatt von 10% auf den Artikelpreis ohne Steuern:

### Ungültiges erwartetes Ergebnis

- Artikelpreis nach Steuern ohne Rabatt=100 USD
- Artikelpreis vor Steuern ohne Rabatt=100/1,2=83,33 USD
- Rabatt=83,33 \ *0,1=8,33 USD
- TAX=(83.33-8.33) \ *0.2=**15 USD (ungültig)**
- Bestellsumme ohne MwSt. = 83,33-8,33 = **75 USD (ungültig)**
- Bestellsumme inkl. MwSt.=75+15=**90 USD (ungültig)**

### Gültiges tatsächliches Ergebnis im Warenkorb

![Ausgeblendete Steuerberechnung im Warenkorb](./assets/hidden-tax.png){width="700" zoomable="yes"}

### Gültige Berechnungen

1. Der volle Preis des Artikels ohne Steuern ist: $100 / 1.2 = **$83.33**

1. MwSt.-Betrag auf den gesamten Artikelpreis ist: $100 - $83.33 = $16.67

   _Kann auch wie folgt berechnet werden: $100 \ * (1 - 1/1.2)._

1. Rabatt von 10% auf $83.33 ist: **$8.33** (wenn Sie keine Steuer abziehen)

1. Rabattpreis für Artikel mit Steuern ist: $100 - $8.33 = $91.67

   >[!NOTE]
   >
   >Diese Gleichung veranschaulicht die Wahrnehmung des Kunden hinsichtlich der Anwendung von Rabatten.

1. Der reduzierte Preis des Artikels ohne Steuern beträgt: $91.67 / 1.2 = $76.39

1. MwSt.-Betrag auf den ermäßigten Preis ist: $91.67 - $76.39 = **$15.28 (gültig)**

   _Kann auch wie folgt berechnet werden: $91.67 \ * (1 - 1/1.2)._

1. Die versteckte Steuer oder _Diskontsteuervergütung_ ist die Differenz zwischen dem Mehrwertsteuerbetrag des vollen Preises und dem diskontierten Preis: $16.67 - $15.28 = **$1.39**

   _Eine andere Möglichkeit, es zu sehen: versteckte Steuer ist der Mehrwertsteuerbetrag, der innerhalb des $8.33 Rabatts: $8.33 befördert wird \* (1 - 1/1.2)._

1. So versteht der Kunde in der Regel den Rabattpreis (Bestellsumme):

   _Gesamtpreis des Artikels einschließlich Steuern **abzüglich**Rabattbetrag: $100 - $8.33 = $91.67_

1. **Wie Commerce den ermäßigten Preis berechnet** (Formel siehe oben):

   _$83.33 - $8.33 + 15.28 + 1.39 =**$91.67***_
