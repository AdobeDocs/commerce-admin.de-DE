---
title: DHL
description: Erfahren Sie, wie Sie DHL als Versandunternehmen für Ihr Geschäft einrichten.
exl-id: 765e5f90-3e93-43cf-a5bc-6132e00b506c
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 0%

---

# DHL

DHL bietet integrierte internationale Dienstleistungen und maßgeschneiderte, kundenorientierte Lösungen für die Verwaltung und den Transport von Briefen, Gütern und Informationen.

## Schritt 1: Aktivieren Sie DHL

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen **[!UICONTROL Delivery Methods]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL DHL]** Abschnitt.

   >[!NOTE]
   >
   >Bei Bedarf muss zunächst die **[!UICONTROL Use system value]** aktivieren, um die folgenden Einstellungen wie beschrieben zu ändern.

1. Satz **[!UICONTROL Enabled for Checkout]** nach `Yes`.

1. In der Regel können Sie die Standardeinstellung **[!UICONTROL Gateway URL]**.

   Wenn DHL Ihnen eine alternative URL gegeben hat, geben Sie diesen Wert in dieses Feld ein.

1. Verwenden Sie die von DHL bereitgestellten Anmeldeinformationen, um die folgenden Felder auszufüllen:

   - **[!UICONTROL Access ID]**
   - **[!UICONTROL Password]**
   - **[!UICONTROL Account Number]**

![DHL-Kontoeinstellungen](../configuration-reference/sales/assets/delivery-methods-dhl-account-settings.png){width="600" zoomable="yes"}

## Schritt 2: Geben Sie die Paketbeschreibung und die Bearbeitungsgebühr ein

1. Im **[!UICONTROL Content Type]** die Option auswählen, die den von Ihnen gelieferten Pakettyp am besten beschreibt:

   - `Documents`
   - `Non documents`

1. Konfigurieren Sie die Optionen für die Bearbeitungsgebühr entsprechend Ihren Anforderungen.

   Die Bearbeitungsgebühr ist optional und erscheint als zusätzliche Gebühr, die zu den Versandkosten von DHL hinzukommt. Wenn Sie eine Bearbeitungsgebühr einbeziehen möchten, gehen Sie wie folgt vor:

   - Für **[!UICONTROL Calculate Handling Fee]** wählen Sie die Methode aus, die Sie zur Berechnung der Bearbeitungsgebühren verwenden möchten:

      - `Fixed`
      - `Percentage`

   - Für **[!UICONTROL Handling Applied]** auswählen, wie die Bearbeitungsgebühren angewendet werden sollen:

      - `Per Order`
      - `Per Package`

   - Für **[!UICONTROL Handling Fee]**, geben Sie den zu berechnenden Betrag nach der Methode an, die Sie zur Berechnung des Betrags gewählt haben.

     Wenn die Gebühr beispielsweise auf einer festen Gebühr basiert, geben Sie den Betrag als Dezimalzahl ein, z. B. `4.90`. Wenn die Bearbeitungsgebühr jedoch auf einem Prozentsatz der Bestellung basiert, geben Sie den Betrag als Prozentsatz an. Wenn Sie beispielsweise sechs Prozent der Bestellung aufladen, geben Sie den Wert als `.06`.

   - Um eine Aufteilung des Gesamtauftragsgewichts zu ermöglichen, um eine genaue Berechnung der Versandkosten zu gewährleisten, legen Sie **[!UICONTROL Divide Order Weight]** nach `Yes`.

   - Legen Sie die **[!UICONTROL Weight Unit]** des Pakets zu einem der folgenden Punkte:

      - `Pounds`
      - `Kilograms`

   - Legen Sie die **[!UICONTROL Size]** eines typischen Pakets mit einer der folgenden Eigenschaften:

      - `Regular`
      - `Specific`

     Wenn Sie `Specific`, geben Sie die **[!UICONTROL Height]**, **[!UICONTROL Depth]**, und **[!UICONTROL Width]** der Packung in Zentimetern.

   ![DHL-Paketeinstellungen](../configuration-reference/sales/assets/delivery-methods-dhl-package-settings.png){width="600" zoomable="yes"}

## Schritt 3: Festlegen der zulässigen Versandmethoden

1. Für **[!UICONTROL Allowed Methods]** wählen Sie die einzelnen Methoden aus, die Kunden zur Verfügung stehen sollen.

   Um mehrere Methoden auszuwählen, halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie auf jede Option.

   Um die richtige Liste der Versandmethoden anzuzeigen, müssen Sie zunächst die [Herkunftsland](../configuration-reference/sales/shipping-settings.md).

1. Für **[!UICONTROL Ready Time]**, geben Sie die Anzahl der Stunden an, nach denen eine Bestellung versandbereit ist.

1. Bearbeiten Sie die **[!UICONTROL Displayed Error Message]** nach Bedarf.

   Diese Meldung wird angezeigt, wenn eine ausgewählte Methode nicht verfügbar ist.

1. Wenn Sie eine [Kostenloser Versand](shipping-free.md) -Option über DHL die kostenlosen Versandoptionen festlegen.

   - Für **[!UICONTROL Free Method]**, wählen Sie die Methode, die Sie für den kostenlosen Versand bevorzugen.

   - Satz **[!UICONTROL Free Shipping Amount Threshold]**:

     `Enable` - Wenn Sie kostenlosen Versand mit Mindestbestellung anbieten, geben Sie die **[!UICONTROL Minimum Order Amount for Free Shipping]**.

     `Disable` - gilt nicht für den kostenlosen DHL Versand auf Bestellungen.

     Diese Einstellung ähnelt der für den Standard _Kostenloser Versand_ -Methode, wird jedoch im Abschnitt DHL angezeigt, damit Kunden wissen, welche Methode für ihre Bestellung verwendet wird.

   - Für **[!UICONTROL Free Shipping Amount Threshold]** Geben Sie den Mindestbetrag für eine Bestellung ein, um für den kostenlosen Versand infrage zu kommen.

     ![Zulässige DHL-Methoden](../configuration-reference/sales/assets/delivery-methods-dhl-allowed-methods.png){width="600" zoomable="yes"}

## Schritt 4: Bestimmen Sie die entsprechenden Länder.

1. Satz **[!UICONTROL Ship to Applicable Countries]** auf einen der folgenden Werte zu:

   - `All Allowed Countries`
   - `Specific Countries`

   Wenn Sie einen Versand in bestimmte Länder durchführen möchten, wählen Sie jedes Land aus dem **[!UICONTROL Ship to Specific Countries]** Liste.

1. Satz **[!UICONTROL Show Method if Not Applicable]**:

   `Yes` - Zeigt DHL als Versandmethode während des Checkout an, auch wenn es nicht auf die Bestellung anwendbar ist.

   `No` - Zeigt DHL nur bei Bedarf als Versandmethode während des Checkout an.

1. Um eine Protokolldatei mit den Details zu DHL-Sendungen zu erstellen, die aus Ihrem Speicher durchgeführt wurden, legen Sie **[!UICONTROL Debug]** nach `Yes`.

1. Für **[!UICONTROL Sort Order]** Geben Sie eine Zahl ein, um die Reihenfolge zu bestimmen, in der DHL beim Checkout mit anderen Versandmethoden angezeigt wird.

   `0` = first, `1` = Sekunde, `2` = drittes Element usw.

1. Klicken **[!UICONTROL Save Config]**.

   ![DHL Anwendbare Länder](../configuration-reference/sales/assets/delivery-methods-dhl-applicable-countries.png){width="600" zoomable="yes"}
