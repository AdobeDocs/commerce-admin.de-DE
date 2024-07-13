---
title: DHL
description: Erfahren Sie, wie Sie DHL als Versandunternehmen für Ihr Geschäft einrichten.
exl-id: 765e5f90-3e93-43cf-a5bc-6132e00b506c
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 0%

---

# DHL

DHL bietet integrierte internationale Dienstleistungen und maßgeschneiderte, kundenorientierte Lösungen für die Verwaltung und den Transport von Briefen, Gütern und Informationen.

## Schritt 1: Aktivieren Sie DHL

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Delivery Methods]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL DHL]** .

   >[!NOTE]
   >
   >Deaktivieren Sie bei Bedarf zunächst das Kontrollkästchen **[!UICONTROL Use system value]** , um die folgenden Einstellungen wie beschrieben zu ändern.

1. Setzen Sie **[!UICONTROL Enabled for Checkout]** auf `Yes`.

1. Normalerweise können Sie den Standardwert **[!UICONTROL Gateway URL]** akzeptieren.

   Wenn DHL Ihnen eine alternative URL gegeben hat, geben Sie diesen Wert in dieses Feld ein.

1. Verwenden Sie die von DHL bereitgestellten Anmeldeinformationen, um die folgenden Felder auszufüllen:

   - **[!UICONTROL Access ID]**
   - **[!UICONTROL Password]**
   - **[!UICONTROL Account Number]**

![DHL-Kontoeinstellungen](../configuration-reference/sales/assets/delivery-methods-dhl-account-settings.png){width="600" zoomable="yes"}

## Schritt 2: Geben Sie die Paketbeschreibung und die Bearbeitungsgebühr ein

1. Wählen Sie in der Liste &quot;**[!UICONTROL Content Type]**&quot;die Option aus, die den von Ihnen gelieferten Pakettyp am besten beschreibt:

   - `Documents`
   - `Non documents`

1. Konfigurieren Sie die Optionen für die Bearbeitungsgebühr entsprechend Ihren Anforderungen.

   Die Bearbeitungsgebühr ist optional und erscheint als zusätzliche Gebühr, die zu den Versandkosten von DHL hinzukommt. Wenn Sie eine Bearbeitungsgebühr einbeziehen möchten, gehen Sie wie folgt vor:

   - Wählen Sie für **[!UICONTROL Calculate Handling Fee]** die Methode aus, die Sie zur Berechnung der Bearbeitungsgebühren verwenden möchten:

      - `Fixed`
      - `Percentage`

   - Wählen Sie für **[!UICONTROL Handling Applied]** aus, wie die Bearbeitungsgebühren angewendet werden sollen:

      - `Per Order`
      - `Per Package`

   - Geben Sie für **[!UICONTROL Handling Fee]** den zu berechnenden Betrag basierend auf der Methode ein, die Sie zur Berechnung des Betrags ausgewählt haben.

     Wenn die Gebühr beispielsweise auf einer festen Gebühr basiert, geben Sie den Betrag als Dezimalzahl ein, z. B. `4.90`. Wenn die Bearbeitungsgebühr jedoch auf einem Prozentsatz der Bestellung basiert, geben Sie den Betrag als Prozentsatz an. Wenn Sie beispielsweise sechs Prozent der Bestellung aufladen, geben Sie den Wert als `.06` ein.

   - Damit die Gesamtauftragsgewichtung aufgeteilt werden kann, um eine genaue Berechnung der Versandkosten zu gewährleisten, setzen Sie **[!UICONTROL Divide Order Weight]** auf `Yes`.

   - Setzen Sie die **[!UICONTROL Weight Unit]** des Pakets auf einen der folgenden Werte:

      - `Pounds`
      - `Kilograms`

   - Setzen Sie die **[!UICONTROL Size]** eines typischen Pakets auf einen der folgenden Werte:

      - `Regular`
      - `Specific`

     Wenn Sie `Specific` auswählen, geben Sie die **[!UICONTROL Height]**, **[!UICONTROL Depth]** und **[!UICONTROL Width]** des Pakets in Zentimetern ein.

   ![DHL-Paketeinstellungen](../configuration-reference/sales/assets/delivery-methods-dhl-package-settings.png){width="600" zoomable="yes"}

## Schritt 3: Festlegen der zulässigen Versandmethoden

1. Wählen Sie für &quot;**[!UICONTROL Allowed Methods]**&quot;jede Methode aus, die Kunden zur Verfügung stehen soll.

   Um mehrere Methoden auszuwählen, halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie auf jede Option.

   Um die richtige Liste der Versandmethoden anzuzeigen, müssen Sie zunächst das [Ursprungsland](../configuration-reference/sales/shipping-settings.md) angeben.

1. Geben Sie für &quot;**[!UICONTROL Ready Time]**&quot;die Anzahl der Stunden ein, nach denen eine Bestellung gesendet wurde, die zum Versand eines Pakets erforderlich ist.

1. Bearbeiten Sie die **[!UICONTROL Displayed Error Message]** nach Bedarf.

   Diese Meldung wird angezeigt, wenn eine ausgewählte Methode nicht verfügbar ist.

1. Wenn Sie die Option [Free Shipping](shipping-free.md) über DHL bereitstellen möchten, legen Sie die kostenlosen Versandoptionen fest.

   - Wählen Sie für **[!UICONTROL Free Method]** die Methode, die Sie für den kostenlosen Versand bevorzugen.

   - Legen Sie **[!UICONTROL Free Shipping Amount Threshold]** fest:

     `Enable` - Wenn Sie kostenlosen Versand mit Mindestbestellung anbieten, geben Sie die **[!UICONTROL Minimum Order Amount for Free Shipping]** ein.

     `Disable` - Keine kostenlose DHL-Lieferung auf Bestellungen.

     Diese Einstellung ähnelt der für die standardmäßige _kostenlose Versandmethode_ , wird jedoch im Abschnitt DHL angezeigt, damit Kunden wissen, welche Methode für ihre Bestellung verwendet wird.

   - Geben Sie für **[!UICONTROL Free Shipping Amount Threshold]** den Mindestbetrag für eine Bestellung ein, um für den kostenlosen Versand infrage zu kommen.

     ![Zulässige DHL-Methoden](../configuration-reference/sales/assets/delivery-methods-dhl-allowed-methods.png){width="600" zoomable="yes"}

## Schritt 4: Bestimmen Sie die entsprechenden Länder.

1. Setzen Sie **[!UICONTROL Ship to Applicable Countries]** auf einen der folgenden Werte:

   - `All Allowed Countries`
   - `Specific Countries`

   Wenn Sie einen Versand in bestimmte Länder durchführen, wählen Sie aus der Liste **[!UICONTROL Ship to Specific Countries]** jedes Land aus.

1. Legen Sie **[!UICONTROL Show Method if Not Applicable]** fest:

   `Yes` - Zeigt DHL als Versandmethode beim Checkout an, auch wenn dies nicht für die Bestellung gilt.

   `No` - Zeigt DHL beim Checkout nur dann als Versandmethode an, wenn zutreffend.

1. Um eine Protokolldatei mit Details zu DHL-Sendungen aus Ihrem Speicher zu erstellen, setzen Sie **[!UICONTROL Debug]** auf `Yes`.

1. Geben Sie für &quot;**[!UICONTROL Sort Order]**&quot; eine Zahl ein, um die Sequenz zu bestimmen, in der DHL beim Checkout mit anderen Versandmethoden angezeigt wird.

   `0` = first, `1` = second, `2` = third usw.

1. Klicken Sie auf **[!UICONTROL Save Config]**.

   ![DHL-Anwendbare Länder](../configuration-reference/sales/assets/delivery-methods-dhl-applicable-countries.png){width="600" zoomable="yes"}
