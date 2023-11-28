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

_Pauschalsatz_ ist eine feste, vordefinierte Ladung, die pro Artikel oder pro Sendung angewendet werden kann. Der Pauschalpreis ist eine einfache Versandlösung, insbesondere bei Verwendung mit der von einigen Transportunternehmen angebotenen Pauschalverpackung. Wenn aktiviert, _Pauschalsatz_ wird beim Checkout als Option angezeigt. Da kein bestimmter Anbieter angegeben ist, können Sie einen Träger Ihrer Wahl verwenden.

## Pauschalbetrag für den Versand einrichten

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen **[!UICONTROL Delivery Methods]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **Pauschalsatz** Abschnitt.

   ![Pauschalsatz](../configuration-reference/sales/assets/delivery-methods-flat-rate.png){width="600" zoomable="yes"}

   Eine ausführliche Beschreibung der einzelnen Konfigurationseinstellungen finden Sie unter [Pauschalsatz](../configuration-reference/sales/delivery-methods.md#flat-rate) im _Konfigurationshandbuch_.

1. Satz **[!UICONTROL Enabled]** nach `Yes`.

   Der Pauschalbetrag wird als Option im Abschnitt Geschätzte Versand- und Steuervorteil des Warenkorbs sowie im Abschnitt &quot;Versand&quot;beim Checkout angezeigt.

1. Beschreibende Eingabe **[!UICONTROL Title]** für die Methode &quot;Pauschalrate&quot;.

1. Geben Sie einen **Name der Methode** neben der berechneten Rate im Warenkorb angezeigt.

   Der standardmäßige Methodenname lautet `Fixed`. Wenn Sie eine Bearbeitungsgebühr berechnen, können Sie diesen Text in `Plus Handling`oder etwas Anderes, das geeignet ist.

1. Um zu beschreiben, wie Pauschalsendungen verwendet werden können, legen Sie **Typ** auf einen der folgenden Werte zu:

   - `None` - Deaktiviert die Zahlungsart. Die Option Pauschalpreis ist im Warenkorb aufgeführt, jedoch mit einem Nullsatz, der mit dem kostenlosen Versand identisch ist.
   - `Per Order` - berechnet einen Pauschalpreis für die gesamte Bestellung.
   - `Per Item` - berechnet für jeden Artikel einen Pauschalbetrag. Der Prozentsatz wird mit der Anzahl der Artikel im Warenkorb multipliziert, unabhängig davon, ob es mehrere Mengen desselben oder verschiedener Artikel gibt.

1. Geben Sie die **Preis** die Sie für den Pauschalversand berechnen möchten.

1. Konfigurieren Sie die Optionen für die Bearbeitungsgebühr entsprechend Ihren Anforderungen.

   Die Bearbeitungsgebühr ist optional und erscheint als zusätzliche Gebühr, die zu den Versandkosten hinzukommt. Wenn Sie eine Bearbeitungsgebühr einbeziehen möchten, gehen Sie wie folgt vor:

   - Für **Berechnete Bereitstellungsgebühr** wählen Sie die Methode aus, die Sie zur Berechnung der Bearbeitungsgebühren verwenden möchten:

      - `Fixed`
      - `Percent`

   - Für **Bearbeitungsgebühr**, geben Sie den zu berechnenden Betrag nach der Methode an, die Sie zur Berechnung des Betrags gewählt haben.

     Wenn die Gebühr beispielsweise auf einer festen Gebühr basiert, geben Sie den Betrag als Dezimalzahl ein, z. B. `4.90`. Wenn die Bearbeitungsgebühr jedoch auf einem Prozentsatz der Versandkosten basiert, geben Sie den Betrag in Prozent an. Wenn Sie beispielsweise sechs Prozent der Versandkosten in Rechnung stellen, geben Sie den Wert als `6`.

1. Ändern Sie bei Bedarf die **Angezeigte Fehlermeldung**.

   Dieses Textfeld enthält eine Standardnachricht. Sie können jedoch eine andere Meldung eingeben, die angezeigt werden soll, wenn die Bereitstellung einer Pauschalreise nicht mehr verfügbar ist.

1. Satz **Schiff in die betreffenden Länder**:

   - `All Allowed Countries` - Kunden von allen [Länder](../getting-started/store-details.md#country-options) Diese in Ihrer Store-Konfiguration angegebene Versandmethode kann verwendet werden.
   - `Specific Countries` - Wenn Sie diese Option wählen, wird die _Schiff in bestimmte Länder_ angezeigt. Wählen Sie jedes Land in der Liste aus, in dem diese Versandmethode verwendet werden kann.

1. Satz **Methode anzeigen, falls nicht zutreffend**:

   - `Yes` - Zeigt immer die Methode der Pauschalrate an, auch wenn sie nicht anwendbar ist.
   - `No` - Zeigt nur die Pauschalsatzmethode an, wenn zutreffend.

1. Für **[!UICONTROL Sort Order]** eingeben, geben Sie eine Zahl ein, um die Reihenfolge zu bestimmen, in der beim Checkout der Pauschalpreis-Versand angezeigt wird, wenn er mit anderen Versandmethoden aufgeführt wird.

   `0` = first, `1` = Sekunde, `2` = drittes Element usw.

1. Klicken **[!UICONTROL Save Config]**.
