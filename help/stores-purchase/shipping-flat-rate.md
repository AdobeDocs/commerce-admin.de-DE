---
title: Pauschalversand
description: Erfahren Sie, wie Sie eine Pauschalversandoption für Ihr Geschäft einrichten.
exl-id: a6874509-a79b-42ab-aa93-d70d18fc33f6
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 0%

---

# Pauschalversand

_Pauschalsatz_ ist eine feste, vordefinierte Gebühr, die pro Artikel oder pro Sendung erhoben werden kann. Flatrate ist eine einfache Versandlösung, besonders wenn sie mit der von einigen Transportunternehmen erhältlichen Flatrate-Verpackung verwendet wird. Wenn diese Option aktiviert ist _wird_ Flat Rate“ während des Checkouts als Option angezeigt. Da kein spezifischer Provider angegeben ist, können Sie einen Provider Ihrer Wahl verwenden.

## Pauschalversand einrichten

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Delivery Methods]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **Pauschale** .

   ![Pauschale](../configuration-reference/sales/assets/delivery-methods-flat-rate.png){width="600" zoomable="yes"}

   Eine ausführliche Beschreibung der einzelnen Konfigurationseinstellungen finden Sie unter [Flat Rate](../configuration-reference/sales/delivery-methods.md#flat-rate) im _Configuration Reference Guide_.

1. Legen Sie **[!UICONTROL Enabled]** auf `Yes` fest.

   Der Pauschalsatz wird als Option im Abschnitt „Voraussichtliche Versand- und Steuerkosten“ des Warenkorbs und auch im Abschnitt „Versand“ während des Checkouts angezeigt.

1. Geben Sie eine beschreibende **[!UICONTROL Title]** für die Pauschale ein.

1. Geben Sie einen **Methodennamen** ein, der neben der berechneten Rate im Warenkorb angezeigt werden soll.

   Der Standardmethodenname lautet `Fixed`. Wenn Sie eine Bearbeitungsgebühr berechnen, können Sie diesen Text in `Plus Handling` oder etwas Anderes ändern, das geeignet ist.

1. Um zu beschreiben, wie der Flatrate-Versand verwendet werden kann **legen Sie** Typ“ auf einen der folgenden Werte fest:

   - `None` - Deaktiviert den Zahlungstyp. Die Option Flatrate wird im Warenkorb aufgeführt, jedoch mit einem Tarif von null - was dem kostenlosen Versand entspricht.
   - `Per Order` - berechnet einen einzigen Pauschalsatz für die gesamte Bestellung.
   - `Per Item` - berechnet für jeden Artikel einen einzigen Pauschalsatz. Der Satz wird mit der Anzahl der Artikel im Warenkorb multipliziert, unabhängig davon, ob es mehrere Mengen desselben oder verschiedener Artikel gibt.

1. Geben Sie den **Preis** ein, den Sie für den Pauschalversand berechnen möchten.

1. Konfigurieren Sie die Bearbeitungsgebührenoptionen entsprechend Ihren Anforderungen.

   Die Bearbeitungsgebühr ist optional und erscheint als zusätzliche Gebühr, die zu den Versandkosten hinzugerechnet wird. Wenn Sie eine Bearbeitungsgebühr einbeziehen möchten, gehen Sie wie folgt vor:

   - Wählen **unter „Bearbeitungsgebühr berechnen** die Methode aus, die Sie zur Berechnung der Bearbeitungsgebühren verwenden möchten:

      - `Fixed`
      - `Percent`

   - Geben **unter „Bearbeitungsgebühr** den Betrag ein, der auf der Grundlage der für die Berechnung des Betrags gewählten Methode in Rechnung gestellt werden soll.

     Wenn die Gebühr beispielsweise auf einer festen Gebühr basiert, geben Sie den Betrag als Dezimalzahl ein, z. B. `4.90`. Wenn die Bearbeitungsgebühr jedoch auf einem Prozentsatz der Versandkosten basiert, geben Sie den Betrag als Prozentsatz ein. Wenn Sie beispielsweise sechs Prozent der Versandkosten berechnen, geben Sie den Wert als `6` ein.

1. Ändern Sie bei Bedarf die **Angezeigte Fehlermeldung**.

   Dieses Textfeld ist mit einer Standardnachricht vorbelegt. Sie können jedoch eine andere Nachricht eingeben, die angezeigt werden soll, wenn der Flat Rate Shipping nicht mehr verfügbar ist.

1. Setzen Sie **Versand an die entsprechenden Länder**:

   - `All Allowed Countries` - Kunden aus allen [Ländern](../getting-started/store-details.md#country-options) die in Ihrer Store-Konfiguration angegeben sind, können diese Versandmethode verwenden.
   - `Specific Countries` - Wenn Sie diese Option wählen, wird die Liste _Versand an bestimmte Länder_ angezeigt. Wählen Sie jedes Land in der Liste aus, in dem diese Versandmethode verwendet werden kann.

1. Setzen **Methode anzeigen, falls nicht zutreffend**:

   - `Yes` - Zeigt immer die Pauschale Methode an, auch wenn sie nicht anwendbar ist.
   - `No` - Zeigt die Pauschale nur an, wenn zutreffend.

1. Geben Sie **[!UICONTROL Sort Order]** eine Zahl ein, um die Reihenfolge zu bestimmen, in der der Pauschalversand angezeigt wird, wenn er während des Checkouts mit anderen Versandmethoden aufgelistet wird.

   `0` = First, `1` = Second, `2` = Third usw.

1. Klicken Sie auf **[!UICONTROL Save Config]**.
