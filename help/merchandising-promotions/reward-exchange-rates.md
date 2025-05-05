---
title: Belohnungswechselkurse
description: Erfahren Sie, wie Sie die Belohnungswechselkurse einrichten, die die Anzahl der Belohnungspunkte bestimmen, die verdient werden.
exl-id: 4850d853-fb86-4f64-bfee-47915ea028e2
feature: Rewards, Promotions/Events, Customers
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 0%

---

# Belohnungswechselkurse

{{ee-feature}}

Die Belohnungswechselkurse bestimmen die Anzahl der Punkte, die auf der Grundlage des Bestellbetrags verdient werden, und den Wert der verdienten Punkte. Verschiedene Wechselkurse können auf verschiedene Websites und verschiedene Kundengruppen angewendet werden. Wenn mehrere Wechselkurse von verschiedenen Websites und Kundengruppen für denselben Kunden gelten, gelten die folgenden Prioritätsregeln:

## Wechselkurspriorität

**1**: Gilt für bestimmte Websites und Kundengruppen.

**2**: Gilt für alle Websites und eine bestimmte Kundengruppe.

**3**: Gilt für eine bestimmte Website und alle Kundengruppen.

**4**: Gilt für alle Websites und alle Kundengruppen.

Beim Konvertieren der Währung in Punkte kann die Anzahl der Punkte nicht geteilt werden. Etwaige übrige Währungen werden abgerundet. Wenn beispielsweise $2.00 in zehn Punkte konvertiert wird, werden Punkte in Gruppen von $2.00 verdient. Daher würde eine $7.00-Bestellung 30 Punkte sammeln, und die restlichen $1.00 würden abgerundet. Der Geldbetrag der Bestellung ist definiert als der Betrag, den der Händler erhält, oder die Gesamtsumme abzüglich Versand, Steuern, Rabatte, Warenkredite und Geschenkkarten. Die Punkte werden in dem Moment verdient, in dem keine nicht fakturierten Artikel in der Bestellung vorhanden sind (alle Artikel werden entweder bezahlt oder storniert). Wenn ein Administrator oder eine Administratorin Kunden nicht erlauben möchte, Prämienpunkte für stornierte Bestellungen zu sammeln, können diese Punkte manuell von der Seite Kunden verwalten abgezogen werden.

## Einrichten von Wechselkursen

![Wechselkurse belohnen](./assets/reward-exchange-rates.png){width="700" zoomable="yes"}

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Reward Exchange Rates]**.

1. Klicken Sie oben rechts auf **[!UICONTROL Add New Rate]**.

1. Gehen Sie im Abschnitt **[!UICONTROL Reward Exchange Rate Information]** wie folgt vor:

   ![Wechselkurse belohnen - Informationen](./assets/reward-exchange-rate-new.png){width="600" zoomable="yes"}

   - Stellen Sie **[!UICONTROL Website]** auf die Websites ein, für die der Belohnungswechselkurs gilt.

   - Legen Sie **[!UICONTROL Customer Group]** auf die Gruppen fest, für die der Belohnungswechselkurs gilt.

   - Legen Sie **[!UICONTROL Direction]** auf eine der folgenden Einstellungen fest:

      - `Points to Currency`
      - `Currency to Points`

   Für jede Richtungseinstellung wird der Betrag in der Basiswährung der Website dargestellt.

1. Geben Sie die **[!UICONTROL Rate]** Werte entsprechend der _[!UICONTROL Direction]_&#x200B;ein.

   | Richtung | Tarifeinstellungen |
   |---------|-------------|
   | [!UICONTROL Points to Currency] | Geben Sie im Feld Erster _[!UICONTROL Rate]_&#x200B;die Anzahl der Punkte ein. Geben Sie im zweiten&#x200B;_[!UICONTROL Rate]_ den Geldwert der Punkte ein. |
   | [!UICONTROL Currency to Points] | Geben Sie im Feld Erste _[!UICONTROL Rate]_&#x200B;den Geldwert ein. Geben Sie im zweiten&#x200B;_[!UICONTROL Rate]_ die Anzahl der Punkte ein, die durch den Geldwert dargestellt wird. |

   Beim Konvertieren von Punkten in eine Währung kann die Anzahl der Punkte nicht geteilt werden. Wenn beispielsweise zehn Punkte in $2.00 konvertiert werden, müssen die Punkte in Gruppen von zehn Punkten eingelöst werden. Daher würden 25 Punkte für 4,00 $ eingelöst, wobei 5 Punkte auf dem Kundensaldo verbleiben.

   Es wird empfohlen, eine Konvertierung für `Points to Currency` und `Currency to Points` einzurichten.

1. Klicken Sie abschließend auf **[!UICONTROL Save]**.

## Belohnungs-Wechselkurs löschen

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Reward Exchange Rates]**.

1. Suchen Sie den zu löschenden Belohnungswechselkurs und öffnen Sie ihn im Bearbeitungsmodus.

1. Klicken Sie in der Menüleiste auf **[!UICONTROL Delete]**.

1. Um die Aktion zu bestätigen, klicken Sie auf **[!UICONTROL OK]**.

## Feldbeschreibungen

| Feld | Beschreibung |
|--- |--- |
| [!UICONTROL Website] | Die Websites, für die die Belohnungstarife gelten. |
| [!UICONTROL Customer Group] | Die Kundengruppen, für die die Belohnungstarife gelten. |
| [!UICONTROL Direction] | Bestimmt, welche Art von Transaktion der Wechselkurs definiert. Optionen: <br/>**[!UICONTROL Points to Currency]**- Definiert die Anzahl der Punkte, die als Gutschrift auf den Betrag einer Bestellung angewendet werden können. Geben Sie im Feld Erster _[!UICONTROL Rate]_&#x200B;die Anzahl der Punkte ein. Geben Sie im zweiten&#x200B;_[!UICONTROL Rate]_ den Geldwert der Punkte ein.<br/>**[!UICONTROL Currency to Points]** - Definiert den Betrag einer Bestellung, der dem Kunden Punkte einbringen kann. Geben Sie im Feld Erste _[!UICONTROL Rate]_&#x200B;den Geldwert ein. Geben Sie im zweiten&#x200B;_[!UICONTROL Rate]_ die Anzahl der Punkte ein, die durch den Geldwert dargestellt wird. |
