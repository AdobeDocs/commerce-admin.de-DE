---
title: Wechselkurse
description: Erfahren Sie, wie Sie die Bonuswechselkurse einrichten, die die Anzahl der eingenommenen Bonuspunkte bestimmen.
exl-id: 4850d853-fb86-4f64-bfee-47915ea028e2
feature: Rewards, Promotions/Events, Customers
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 0%

---

# Wechselkurse

{{ee-feature}}

Die Prämienwechselkurse bestimmen die Anzahl der Punkte, die auf der Grundlage des Bestellbetrags verdient werden, und den Wert der verdienten Punkte. Unterschiedliche Wechselkurse können auf verschiedene Websites und verschiedene Kundengruppen angewendet werden. Wenn mehrere Wechselkurse von verschiedenen Websites und Kundengruppen für denselben Kunden gelten, gelten die folgenden Prioritätsregeln:

## Wechselkurspriorität

**1**: Gilt für bestimmte Websites und bestimmte Kundengruppen.

**2**: Gilt für alle Websites und eine bestimmte Kundengruppe.

**3**: Gilt für eine bestimmte Website und alle Kundengruppen.

**4**: Gilt für alle Websites und alle Kundengruppen.

Beim Konvertieren der Währung in Punkte kann die Anzahl der Punkte nicht aufgeteilt werden. Alle Währungsübrige werden abgerundet. Wenn beispielsweise 2,00 $ auf 10 Punkte umgerechnet werden, werden Punkte in Gruppen von 2,00 $ gesammelt. Daher würde eine Bestellung im Wert von 7,00 $ 30 Punkte sammeln, und die verbleibenden 1,00 $ würden abgerundet. Der Geldbetrag der Bestellung ist definiert als der Betrag, den der Händler erhält, oder die Gesamtsumme abzüglich Versand-, Steuer-, Rabatt-, Geschäfts- und Geschenkkarten. Die Punkte werden in dem Moment verdient, in dem es keine nicht fakturierten Artikel in der Bestellung gibt (alle Artikel werden entweder bezahlt oder storniert). Wenn ein Admin-Benutzer Kunden nicht die Möglichkeit geben möchte, Prämienpunkte für stornierte Bestellungen zu erhalten, können diese Punkte manuell von der Seite Kunden verwalten abgezogen werden.

## Wechselkurse einrichten

![Rewards-Wechselkurse](./assets/reward-exchange-rates.png){width="700" zoomable="yes"}

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Reward Exchange Rates]**.

1. Klicken Sie in der oberen rechten Ecke auf **[!UICONTROL Add New Rate]**.

1. Gehen Sie im Abschnitt **[!UICONTROL Reward Exchange Rate Information]** wie folgt vor:

   ![Prämienwechselkurse - Informationen](./assets/reward-exchange-rate-new.png){width="600" zoomable="yes"}

   - Setzen Sie **[!UICONTROL Website]** auf die Sites, auf denen der Bonuswechselkurs gilt.

   - Setzen Sie **[!UICONTROL Customer Group]** auf die Gruppen, in denen der Belohnungskurs gilt.

   - Setzen Sie **[!UICONTROL Direction]** auf einen der folgenden Werte:

      - `Points to Currency`
      - `Currency to Points`

   Bei beiden Richtungseinstellungen wird der Betrag in der Basiswährung der Website dargestellt.

1. Geben Sie die **[!UICONTROL Rate]** -Werte entsprechend der Einstellung _[!UICONTROL Direction]_ein.

   | Richtung | Rateneinstellungen |
   |---------|-------------|
   | [!UICONTROL Points to Currency] | Geben Sie im ersten Feld _[!UICONTROL Rate]_die Anzahl der Punkte ein. Geben Sie im zweiten Feld_[!UICONTROL Rate]_ den Geldwert der Punkte ein. |
   | [!UICONTROL Currency to Points] | Geben Sie im ersten Feld _[!UICONTROL Rate]_den Geldwert ein. Geben Sie im zweiten Feld_[!UICONTROL Rate]_ die Anzahl der Punkte ein, die durch den Geldwert dargestellt werden. |

   Beim Konvertieren von Punkten in Währungen kann die Anzahl der Punkte nicht aufgeteilt werden. Wenn beispielsweise zehn Punkte in $2,00 umgewandelt werden, müssen Punkte in Gruppen von zehn eingelöst werden. Daher würden 25 Punkte für 4,00 USD eingelöst, während 5 Punkte auf dem Kundensaldo verbleiben.

   Es wird empfohlen, eine Konvertierung für `Points to Currency` und `Currency to Points` einzurichten.

1. Klicken Sie nach Abschluss des Vorgangs auf **[!UICONTROL Save]**.

## Löschen eines Belohnungswechselkurses

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Reward Exchange Rates]**.

1. Suchen Sie den zu löschenden Belohnungskurs und öffnen Sie ihn im Bearbeitungsmodus.

1. Klicken Sie in der Menüleiste auf **[!UICONTROL Delete]**.

1. Um die Aktion zu bestätigen, klicken Sie auf **[!UICONTROL OK]**.

## Feldbeschreibungen

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Website] | Die Websites, auf denen die Prämien gelten. |
| [!UICONTROL Customer Group] | Die Kundengruppen, auf die die Belohnungssätze angewandt werden. |
| [!UICONTROL Direction] | Bestimmt, welche Art von Transaktion der Wechselkurs definiert. Optionen: <br/>**[!UICONTROL Points to Currency]**- Definiert die Anzahl der Punkte, die dem Betrag einer Bestellung gutgeschrieben werden können. Geben Sie im ersten Feld _[!UICONTROL Rate]_die Anzahl der Punkte ein. Geben Sie im zweiten Feld_[!UICONTROL Rate]_ den Geldwert der Punkte ein.<br/>**[!UICONTROL Currency to Points]** - Definiert den Betrag einer Bestellung, die die Kundenpunkte verdienen kann. Geben Sie im ersten Feld _[!UICONTROL Rate]_den Geldwert ein. Geben Sie im zweiten Feld_[!UICONTROL Rate]_ die Anzahl der Punkte ein, die durch den Geldwert dargestellt werden. |
