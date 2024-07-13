---
title: Pauschalversand
description: Erfahren Sie, wie Sie eine pauschale Versandoption für Ihren Store einrichten.
exl-id: a6874509-a79b-42ab-aa93-d70d18fc33f6
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 0%

---

# Pauschalversand

_Pauschalrate_ ist eine feste, vordefinierte Ladung, die pro Artikel oder pro Sendung angewendet werden kann. Der Pauschalpreis ist eine einfache Versandlösung, insbesondere bei Verwendung mit der von einigen Transportunternehmen angebotenen Pauschalverpackung. Wenn diese Option aktiviert ist, wird _Pauschalrate_ beim Checkout als Option angezeigt. Da kein bestimmter Anbieter angegeben ist, können Sie einen Träger Ihrer Wahl verwenden.

## Pauschalbetrag für den Versand einrichten

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Delivery Methods]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **Pauschalrate** .

   ![Pauschalrate](../configuration-reference/sales/assets/delivery-methods-flat-rate.png){width="600" zoomable="yes"}

   Eine ausführliche Beschreibung der einzelnen Konfigurationseinstellungen finden Sie unter [Pauschalrate](../configuration-reference/sales/delivery-methods.md#flat-rate) im _Konfigurationshandbuch_.

1. Setzen Sie **[!UICONTROL Enabled]** auf `Yes`.

   Der Pauschalbetrag wird als Option im Abschnitt Geschätzte Versand- und Steuervorteil des Warenkorbs sowie im Abschnitt &quot;Versand&quot;beim Checkout angezeigt.

1. Geben Sie eine beschreibende **[!UICONTROL Title]** für die Methode &quot;Pauschalrate&quot;ein.

1. Geben Sie einen **Methodennamen** ein, der neben der berechneten Rate im Warenkorb angezeigt werden soll.

   Der standardmäßige Methodenname ist `Fixed`. Wenn Sie eine Bearbeitungsgebühr berechnen, können Sie diesen Text in `Plus Handling` oder etwas Anderes ändern, das geeignet ist.

1. Um zu beschreiben, wie Pauschalsendungen verwendet werden können, setzen Sie **Typ** auf einen der folgenden Werte:

   - `None` - Deaktiviert den Zahlungstyp. Die Option Pauschalpreis ist im Warenkorb aufgeführt, jedoch mit einem Nullsatz, der mit dem kostenlosen Versand identisch ist.
   - `Per Order` - berechnet einen Pauschalpreis für die gesamte Bestellung.
   - `Per Item` - berechnet für jedes Element einen Pauschalsatz. Der Prozentsatz wird mit der Anzahl der Artikel im Warenkorb multipliziert, unabhängig davon, ob es mehrere Mengen desselben oder verschiedener Artikel gibt.

1. Geben Sie den **Preis** ein, den Sie für den Pauschalversand berechnen möchten.

1. Konfigurieren Sie die Optionen für die Bearbeitungsgebühr entsprechend Ihren Anforderungen.

   Die Bearbeitungsgebühr ist optional und erscheint als zusätzliche Gebühr, die zu den Versandkosten hinzukommt. Wenn Sie eine Bearbeitungsgebühr einbeziehen möchten, gehen Sie wie folgt vor:

   - Wählen Sie für **Bearbeitungsgebühr berechnen** die Methode aus, die Sie zur Berechnung der Bearbeitungsgebühren verwenden möchten:

      - `Fixed`
      - `Percent`

   - Geben Sie für **Bearbeitungsgebühr** den zu berechnenden Betrag basierend auf der Methode ein, die Sie zur Berechnung des Betrags ausgewählt haben.

     Wenn die Gebühr beispielsweise auf einer festen Gebühr basiert, geben Sie den Betrag als Dezimalzahl ein, z. B. `4.90`. Wenn die Bearbeitungsgebühr jedoch auf einem Prozentsatz der Versandkosten basiert, geben Sie den Betrag in Prozent an. Wenn Sie beispielsweise sechs Prozent der Versandkosten in Rechnung stellen, geben Sie den Wert als `6` ein.

1. Ändern Sie bei Bedarf die **angezeigte Fehlermeldung**.

   Dieses Textfeld enthält eine Standardnachricht. Sie können jedoch eine andere Meldung eingeben, die angezeigt werden soll, wenn die Bereitstellung einer Pauschalreise nicht mehr verfügbar ist.

1. Stellen Sie **Versand auf die anwendbaren Länder** ein:

   - `All Allowed Countries` - Kunden aus allen in Ihrer Store-Konfiguration angegebenen [Ländern](../getting-started/store-details.md#country-options) können diese Bereitstellungsmethode verwenden.
   - `Specific Countries` - Wenn Sie diese Option auswählen, wird die Liste _Zu bestimmten Ländern verschicken_ angezeigt. Wählen Sie jedes Land in der Liste aus, in dem diese Versandmethode verwendet werden kann.

1. Legen Sie **Methode anzeigen , falls nicht zutreffend** fest:

   - `Yes` - Zeigt immer die Methode &quot;Pauschalrate&quot;an, auch wenn sie nicht anwendbar ist.
   - `No` - Zeigt die Methode der Pauschalrate nur an, wenn zutreffend.

1. Geben Sie für &quot;**[!UICONTROL Sort Order]**&quot; eine Zahl ein, um die Reihenfolge zu bestimmen, in der der Pauschalsatz-Versand erscheint, wenn er beim Checkout mit anderen Versandmethoden aufgeführt wird.

   `0` = first, `1` = second, `2` = third usw.

1. Klicken Sie auf **[!UICONTROL Save Config]**.
