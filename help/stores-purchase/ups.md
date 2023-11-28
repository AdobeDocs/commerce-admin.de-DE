---
title: United Parcel Service (UPS)
description: Erfahren Sie, wie Sie UPS als Versandunternehmen für Ihr Geschäft einrichten.
exl-id: a7965b2f-2473-4b63-a247-3b2230cde5d8
feature: Shipping/Delivery
source-git-commit: 50b44190a9568a8d6ad38ab29177904596569d75
workflow-type: tm+mt
source-wordcount: '827'
ht-degree: 0%

---

# United Parcel Service (UPS)

United Parcel Service (UPS) bietet inländische und internationale Seeverkehrsdienstleistungen auf dem Land- und Luftweg in über 220 Ländern an.

{{ups-api}}

>[!NOTE]
>
>UPS kann [Dimensionsgewicht](carriers.md#dimensional-weight) um einige Versandtarife zu bestimmen. Adobe Commerce unterstützt jedoch nur die gewichtsbasierte Berechnung der Versandkosten.

## Schritt 1: Öffnen Sie ein UPS-Versandkonto.

Um diese Versandmethode Ihren Kunden anzubieten, müssen Sie zunächst ein Konto bei UPS eröffnen.

## Schritt 2: UPS für Ihren Store aktivieren

{{beta2-updates}}

1. Im _Admin-Seitenleiste_, gehen Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Im Bedienfeld auf der linken Seite, unter **[!UICONTROL Sales]** auswählen **[!UICONTROL Delivery Methods]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL UPS]** Abschnitt.

1. Satz **[!UICONTROL Enabled for Checkout]** nach `Yes`.

1. Für ein UPS XML-Konto (Standard) legen Sie **[!UICONTROL UPS Type]** nach `United Parcel Service XML` und gehen Sie wie folgt vor:

   - Geben Sie Ihre UPS-Anmeldedaten ein: **[!UICONTROL User ID]**, **[!UICONTROL Access License Number]** (das 16-stellige UPS-Konto `Access Key`) und **[!UICONTROL Password]**

   - Satz **[!UICONTROL Mode]** nach `Live` um Daten über eine sichere Verbindung an das UPS Versandsystem zu senden. (Im Entwicklungsmodus werden keine Daten über eine sichere Verbindung gesendet.)

   - Überprüfen Sie die **[!UICONTROL Gateway XML URL]** , die zum Senden von Anforderungen per XML-Datei erforderlich ist.

   - Satz **[!UICONTROL Origin of the Shipment]** in die Region, aus der die Verbringung stammt.

   - Wenn Sie Sondertarife mit UPS haben, legen Sie **[!UICONTROL Enable Negotiated Rates]** nach `Yes` und geben Sie die sechsstellige **[!UICONTROL Shipper Number]** Sie werden von UPS zugewiesen.

1. Für ein Standard-UPS-Konto legen Sie **[!UICONTROL UPS Type]** nach `United Parcel Service` und gehen Sie wie folgt vor:

   >[!NOTE]
   >
   >Der standardmäßige United Parcel Service-Typ ist für die Einstellung geplant. Für neue Konfigurationen sollten Sie die Standardeinstellung  `United Parcel Service XML` Typ. Der XML-Typ muss auch generiert werden [Versandtitel](shipping-labels.md).

   - Satz **[!UICONTROL Live Account]** auf einen der folgenden Werte zu:

      - `Yes` - Führt UPS im Produktionsmodus aus und bietet UPS als Versandmethode für Ihre Kunden an.
      - `No` - Führt UPS in einem Testmodus aus.

   - Im **[!UICONTROL Gateway URL]** Geben Sie die URL ein, die zur Berechnung der UPS Versandraten verwendet wird.

     >[!IMPORTANT]
     >
     >UPS stellt die Unterstützung von HTTP ein, die in der aktuellen Standardeinstellung (Systemwert) verwendet wird. Löschen Sie die **[!UICONTROL Use system value]** aktivieren und die URL ändern, um HTTPS zu verwenden. Beispiel: `https://www.ups.com/using/services/rave/qcostcgi.cgi`

1. Für **[!UICONTROL Title]** Geben Sie den Namen dieser Versandoption ein, wie er beim Checkout angezeigt werden soll.

   Standardmäßig ist dieses Feld auf `United Parcel Service`.

   ![UPS aktivieren](../configuration-reference/sales/assets/delivery-methods-ups1.png){width="600" zoomable="yes"}

## Schritt 3: Container-Beschreibung ausfüllen

1. Satz **[!UICONTROL Packages Request Type]** auf einen der folgenden Werte zu:

   - `Use origin weight (few requests)`
   - `Divide to equal weight (one request)`

1. Für **[!UICONTROL Container]** die typische Verpackung angeben, die für die Verbringung verwendet wird:

   - `Customer Packaging`
   - `UPS Letter Envelope`
   - `Customer Supplied Package`
   - `UPS Tube`
   - `PAK`
   - `UPS Express Box`
   - `UPS Worldwide 25 kilo`
   - `UPS Worldwide 10 kilo`
   - `Pallet`
   - `Small Express Box`
   - `Medium Express Box`
   - `Large Express Box`

1. Satz **[!UICONTROL Weight Unit]** in das System, das Sie zum Messen der Produktgewichtung verwenden.

   Das von UPS unterstützte Gewichtungssystem ist je nach Land unterschiedlich. Im Zweifelsfall fragen Sie UPS, welches Gewichtssystem Sie verwenden sollten. Zu den Optionen gehören:

   - `LBS`
   - `KGS`

1. Satz **[!UICONTROL Destination Type]** auf einen der folgenden Werte zu:

   - `Residential` - Die meisten Ihrer Sendungen sind geschäftlich (B2C).
   - `Commercial` - Die meisten Ihrer Sendungen sind geschäftlich (B2B).

1. Geben Sie die **[!UICONTROL Maximum Package Weight]** vom Beförderer zugelassen.

1. Satz **[!UICONTROL Pickup Method]** auf einen der folgenden Werte zu:

   - `Regular Daily Pickup`
   - `On Call Air`
   - `One Time Pickup`
   - `Letter Center`
   - `Customer Counter`

1. Geben Sie die **[!UICONTROL Minimum Package Weight]** vom Beförderer zugelassen.

   ![Container-Beschreibung](./assets/ups2.png){width="600" zoomable="yes"}

## Schritt 4: Einrichten von Bearbeitungsgebühren

Die Bearbeitungsgebühr ist optional und erscheint als zusätzliche Gebühr, die zu den UPS Versandkosten hinzukommt. Wenn Sie eine Bearbeitungsgebühr einbeziehen möchten, gehen Sie wie folgt vor:

1. Satz **[!UICONTROL Calculate Handling Fee]** auf eine der folgenden Methoden anwenden:

   - `Fixed`
   - `Percent`

1. Um festzustellen, wie die Bearbeitungsgebühr angewendet wird, legen Sie **[!UICONTROL Handling Applied]** auf einen der folgenden Werte zu:

   - `Per Order`
   - `Per Package`

1. Geben Sie die Menge der **[!UICONTROL Handling Fee]** zu berechnen.

   Um einen Prozentsatz einzugeben, verwenden Sie das Dezimalformat. Geben Sie beispielsweise `0.25` für 25 %.

   ![Bearbeitungsgebühr](./assets/ups3.png){width="600" zoomable="yes"}

## Schritt 5: Angeben der zulässigen Methoden und der entsprechenden Länder

1. Für **[!UICONTROL Allowed Methods]**, wählen Sie jede UPS Versandmethode aus, um für Ihre Kunden verfügbar zu sein.

   Die Methoden werden beim Checkout unter UPS angezeigt. Um mehrere Methoden auszuwählen, halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie auf jede Option.

1. Wenn Sie eine [Kostenloser Versand](shipping-free.md) -Option über UPS festlegen Sie die kostenlosen Versandoptionen:

   - Satz **[!UICONTROL Free Method]** zu der Methode, die Sie für den kostenlosen Versand verwenden möchten. Wenn Sie keinen kostenlosen Versand über UPS anbieten möchten, wählen Sie `None`.

   - Um einen Mindestbestellbetrag zu verlangen, der für einen kostenlosen Versand mit UPS qualifiziert ist, legen Sie **[!UICONTROL Enable Free Shipping Threshold]** nach `Enable`. Geben Sie dann den Mindestwert in **[!UICONTROL Free Shipping Amount Threshold]**.

1. Ändern Sie bei Bedarf die **[!UICONTROL Displayed Error Message]**.

   Dieses Textfeld enthält eine Standardmeldung, Sie können jedoch eine andere Meldung eingeben, die angezeigt werden soll, wenn UPS nicht verfügbar ist.

   ![Zulässige Methoden](./assets/ups4.png){width="600" zoomable="yes"}

1. Satz **[!UICONTROL Ship to Applicable Countries]** auf einen der folgenden Werte zu:

   - `All Allowed Countries` - Kunden von allen [Länder](../getting-started/store-details.md#country-options) Diese in Ihrer Store-Konfiguration angegebene Versandmethode kann verwendet werden.
   - `Specific Countries` - Wenn Sie diese Option wählen, wird die _Schiff in bestimmte Länder_ angezeigt. Wählen Sie jedes Land in der Liste aus, in dem diese Versandmethode verwendet werden kann.

1. Satz **[!UICONTROL Show Method if Not Applicable]** auf einen der folgenden Werte zu:

   - `Yes` - Listet alle verfügbaren UPS Versandmethoden während des Checkout auf, einschließlich Methoden, die nicht für den Versand gelten.
   - `No` - Listet nur die UPS Versandmethoden auf, die für den Versand gelten.

   ![Anwendbare Länder](./assets/ups5.png){width="600" zoomable="yes"}

1. Um eine Protokolldatei mit den Details zu UPS-Sendungen zu erstellen, die von Ihrem Store vorgenommen wurden, legen Sie **[!UICONTROL Debug]** nach `Yes`.

1. Für **[!UICONTROL Sort Order]** Geben Sie eine Zahl ein, um die Reihenfolge zu bestimmen, in der UPS beim Checkout mit anderen Versandmethoden angezeigt wird.

   `0` = first, `1` = Sekunde, `2` = drittes Element usw.

1. Klicken **[!UICONTROL Save Config]**.

## Schritt 6: Einrichten der Versandstammadresse

1. Stellen Sie sicher, dass Ihr [Store-Informationen](../getting-started/store-details.md#store-information) ist abgeschlossen.

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen **[!UICONTROL Shipping Settings]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) **[!UICONTROL Origin]** auf der Seite und konfigurieren Sie die Versandursprungsadresse.

   ![Verkaufskonfiguration - Optionen für Lieferursprungsadressen](./assets/shipping-origin.png){width="600" zoomable="yes"}

1. Klicken **[!UICONTROL Save Config]**.

>[!NOTE]
>
>Bei der Berechnung der Versandkosten erklärt der Commerce UPS den vollen Bestellpreis nicht. Dieses Verhalten kann nicht geändert werden.
