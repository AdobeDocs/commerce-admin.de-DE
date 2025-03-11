---
title: United Parcel Service (UPS)
description: Erfahren Sie, wie Sie UPS als Versandunternehmen für Ihren Shop einrichten.
exl-id: a7965b2f-2473-4b63-a247-3b2230cde5d8
feature: Shipping/Delivery
source-git-commit: 614a94856c114244c8fdb281c73650878849a2fb
workflow-type: tm+mt
source-wordcount: '1013'
ht-degree: 0%

---

# United Parcel Service (UPS)

United Parcel Service (UPS) bietet inländische und internationale Verschiffen auf dem Land- und Luftweg in mehr als 220 Länder an.

{{ups-api}}

>[!NOTE]
>
>UPS kann [Dimensional Weight](carriers.md#dimensional-weight) verwenden, um einige Versandraten zu bestimmen. Adobe Commerce unterstützt jedoch nur die gewichtsbasierte Berechnung der Versandkosten.

## Schritt 1: Öffnen Sie ein UPS Versandkonto

Um diese Versandart Ihren Kunden anzubieten, müssen Sie zunächst ein UPS-Konto eröffnen und den Antrag ausfüllen, um eine Versender-Kontonummer zu erhalten. Siehe [Kostenloses UPS-Konto ](https://www.ups.com/us/en/business-solutions/open-an-account).

## Schritt 2: Abrufen von UPS OAUTH-Anmeldeinformationen

Führen Sie die Schritte im Handbuch [Erste Schritte mit UPS-APIs](https://developer.ups.com/get-started) aus, um die API-Anmeldeinformationen (Client-ID und Client-Geheimnis) zur Aktivierung der UPS-Integration abzurufen. Sie müssen eine UPS-Anwendung erstellen, um die Anmeldeinformationen zu erhalten.

Wenn Sie die USV-Einstellungen in Admin konfigurieren, verwenden Sie die Werte der Anmeldeinformationen für die `username` und `password`.

## Schritt 3: UPS für Ihren Shop aktivieren

1. Navigieren Sie in _Admin_ Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Wählen Sie im Bedienfeld links unter **[!UICONTROL Sales]** die Option **[!UICONTROL Delivery Methods]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL UPS]** .

1. Legen Sie **[!UICONTROL Enabled for Checkout]** auf `Yes` fest.

1. Gehen Sie für ein UPS REST-Konto (Standard) wie folgt vor:

   - Geben Sie Ihre UPS-Anmeldedaten ein: UPS ClientID als **[!UICONTROL User ID]**, UPS Client Secret als **[!UICONTROL Password]**.

   - Stellen Sie **[!UICONTROL Mode]** auf `Live` ein, um Daten über eine sichere Verbindung an das UPS Versandsystem zu senden. (Der Entwicklungsmodus sendet keine Daten über eine sichere Verbindung.)

   - Überprüfen Sie die **[!UICONTROL Gateway URL]**, die zum Senden von Anfragen erforderlich ist. Verwenden Sie eine Sandbox-URL (`https://wwwcie.ups.com/`) für den Testmodus und eine Produktions-URL für Live-Anfragen (`https://onlinetools.ups.com`). Stellen Sie sicher, dass Sie für jede Anfrage mit dem angegebenen Host die entsprechenden Endpunkte verwenden.

   - Überprüfen Sie die **[!UICONTROL Tracking URL]**, die zum Abrufen von Tracking-Informationen erforderlich ist. Verwenden Sie eine Sandbox-URL (`https://wwwcie.ups.com/`) für den Testmodus und eine Produktions-URL für Live-Anfragen (`https://onlinetools.ups.com`). Stellen Sie sicher, dass Sie für jede Anfrage mit dem angegebenen Host die entsprechenden Endpunkte verwenden.

   - Legen Sie **[!UICONTROL Origin of the Shipment]** auf die Region fest, aus der die Sendung stammt.

   - Wenn Sie bei UPS Sondertarife haben, setzen Sie **[!UICONTROL Enable Negotiated Rates]** auf `Yes` und geben Sie die sechsstellige **[!UICONTROL Shipper Number]** ein, die Ihnen von UPS zugewiesen wurde.

   - Legen Sie **[!UICONTROL Live Account]** auf eine der folgenden Einstellungen fest:

      - `Yes` - Führt UPS im Produktionsmodus aus und bietet UPS als Versandmethode für Ihre Kunden an. Stellen Sie sicher, dass Sie die richtigen Endpunkte unter Gateway-URL und Tracking-URL verwenden.
      - `No` - UPS wird im Testmodus ausgeführt. Stellen Sie sicher, dass Sie die richtigen Endpunkte unter Gateway-URL und Tracking-URL verwenden.

   >[!NOTE]
   >
   >Der Standardtyp Einheitlicher Paketdienst ist für die Einstellung geplant. Verwenden Sie für neue Konfigurationen den standardmäßigen `United Parcel Service REST`. Der REST-Typ ist auch erforderlich, um [Versandkennzeichnungen](shipping-labels.md) zu generieren<br/>
   >Für die Version 2.4.7 wird **[!UICONTROL UPS Type]** entfernt, da `UPS`- und `UPS XML`-Typen zur Einstellung geplant sind und `UPS REST` der Standard ist. Die von der nativen Adobe Commerce-Integration verwendeten United Parcel Service (UPS)-APIs werden vorübergehend nicht mehr unterstützt, da sie derzeit das OAuth 2.0-Sicherheitsmodell nicht unterstützen.

   >[!IMPORTANT]
   >
   >UPS stellt die Unterstützung von HTTP ein, das im aktuellen Standard (Systemwert) verwendet wird. Deaktivieren Sie das Kontrollkästchen **[!UICONTROL Use system value]** und ändern Sie die URL so, dass HTTPS verwendet wird. Beispiel: `https://www.ups.com/using/services/rave/qcostcgi.cgi`

1. Geben Sie **[!UICONTROL Title]** den Namen dieser Versandoption so ein, wie sie beim Checkout angezeigt werden soll.

   Standardmäßig ist dieses Feld auf `United Parcel Service` festgelegt.

   ![UPS aktivieren](../configuration-reference/sales/assets/delivery-methods-ups1.png){width="600" zoomable="yes"}

## Schritt 3: Container-Beschreibung ausfüllen

1. Legen Sie **[!UICONTROL Packages Request Type]** auf eine der folgenden Einstellungen fest:

   - `Use origin weight (few requests)`
   - `Divide to equal weight (one request)`

1. Geben Sie **[!UICONTROL Container]** den typischen Verpackungstyp an, der für den Versand verwendet wird:

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

1. Legen Sie **[!UICONTROL Weight Unit]** auf das System fest, das Sie zum Messen des Produktgewichts verwenden.

   Das von UPS unterstützte Gewichtssystem variiert je nach Land. Im Zweifelsfall fragen Sie UPS, welches Gewichtssystem Sie verwenden sollten. Zu den Optionen gehören:

   - `LBS`
   - `KGS`

1. Legen Sie **[!UICONTROL Destination Type]** auf eine der folgenden Einstellungen fest:

   - `Residential` - Die meisten Ihrer Sendungen gehen vom Business-to-Consumer-Segment (B2C).
   - `Commercial` - Die meisten Ihrer Sendungen gehen von Business zu Business (B2B).

1. Geben Sie die vom Provider erlaubten **[!UICONTROL Maximum Package Weight]** ein.

1. Legen Sie **[!UICONTROL Pickup Method]** auf eine der folgenden Einstellungen fest:

   - `Regular Daily Pickup`
   - `On Call Air`
   - `One Time Pickup`
   - `Letter Center`
   - `Customer Counter`

1. Geben Sie die vom Provider erlaubten **[!UICONTROL Minimum Package Weight]** ein.

   ![Container-Beschreibung](./assets/ups2.png){width="600" zoomable="yes"}

## Schritt 5: Einrichten von Bearbeitungsgebühren

Die Bearbeitungsgebühr ist optional und erscheint als zusätzliche Gebühr, die zu den UPS Versandkosten hinzugerechnet wird. Wenn Sie eine Bearbeitungsgebühr einbeziehen möchten, gehen Sie wie folgt vor:

1. Legen Sie **[!UICONTROL Calculate Handling Fee]** auf eine der folgenden Methoden fest:

   - `Fixed`
   - `Percent`

1. Um zu bestimmen, wie die Bearbeitungsgebühr angewendet wird, **[!UICONTROL Handling Applied]** Sie eine der folgenden Einstellungen ein:

   - `Per Order`
   - `Per Package`

1. Geben Sie den Betrag der zu belastenden **[!UICONTROL Handling Fee]** ein.

   Verwenden Sie das Dezimalformat, um einen Prozentsatz einzugeben. Geben Sie beispielsweise `0.25` für 25 % ein.

   ![Bearbeitungsgebühr](./assets/ups3.png){width="600" zoomable="yes"}

## Schritt 6: Zugelassene Methoden und anwendbare Länder angeben

1. Wählen Sie **[!UICONTROL Allowed Methods]** jede UPS Versandart, die Ihren Kunden zur Verfügung steht.

   Die Methoden werden beim Auschecken unter UPS angezeigt. Zur Auswahl mehrerer Methoden halten Sie die Strg-Taste (PC) bzw. die Befehlstaste (Mac) gedrückt und klicken auf die einzelnen Optionen.

1. Wenn Sie über UPS eine Option [Kostenloser Versand](shipping-free.md) bereitstellen möchten, legen Sie die Optionen für den kostenlosen Versand fest:

   - Legen Sie **[!UICONTROL Free Method]** auf die Methode fest, die Sie für den kostenlosen Versand verwenden möchten. Wenn Sie keinen kostenlosen Versand über UPS anbieten möchten, wählen Sie `None`.

   - Um einen Mindestbestellbetrag zu verlangen, der für einen kostenlosen Versand mit UPS geeignet ist, setzen Sie **[!UICONTROL Enable Free Shipping Threshold]** auf `Enable`. Geben Sie dann den Mindestwert in **[!UICONTROL Free Shipping Amount Threshold]** ein.

1. Ändern Sie bei Bedarf die **[!UICONTROL Displayed Error Message]**.

   Dieses Textfeld ist mit einer Standardmeldung vorbelegt, Sie können jedoch eine andere Nachricht eingeben, die angezeigt werden soll, wenn UPS nicht mehr verfügbar ist.

   ![Zulässige Methoden](./assets/ups4.png){width="600" zoomable="yes"}

1. Legen Sie **[!UICONTROL Ship to Applicable Countries]** auf eine der folgenden Einstellungen fest:

   - `All Allowed Countries` - Kunden aus allen [Ländern](../getting-started/store-details.md#country-options) die in Ihrer Store-Konfiguration angegeben sind, können diese Versandmethode verwenden.
   - `Specific Countries` - Wenn Sie diese Option wählen, wird die Liste _Versand an bestimmte Länder_ angezeigt. Wählen Sie jedes Land in der Liste aus, in dem diese Versandmethode verwendet werden kann.

1. Legen Sie **[!UICONTROL Show Method if Not Applicable]** auf eine der folgenden Einstellungen fest:

   - `Yes` - Listet alle verfügbaren UPS Versandmethoden während des Checkouts auf, einschließlich der Methoden, die nicht für die Sendung gelten.
   - `No` - Listet nur die UPS Versandmethoden auf, die für die Sendung gelten.

   ![Anwendbare Länder](./assets/ups5.png){width="600" zoomable="yes"}

1. Um eine Protokolldatei mit den Details der UPS-Sendungen aus Ihrem Geschäft zu erstellen, setzen Sie **[!UICONTROL Debug]** auf `Yes`.

1. Geben Sie **[!UICONTROL Sort Order]** eine Zahl ein, um die Reihenfolge zu bestimmen, in der UPS angezeigt wird, wenn sie beim Checkout mit anderen Versandmethoden aufgelistet wird.

   `0` = First, `1` = Second, `2` = Third usw.

1. Klicken Sie auf **[!UICONTROL Save Config]**.

## Schritt 7: Versandursprungsadresse einrichten

1. Vergewissern Sie sich, dass Ihre [Store-Informationen](../getting-started/store-details.md#store-information) vollständig sind.

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Shipping Settings]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) **[!UICONTROL Origin]** auf der Seite und konfigurieren Sie die Versandursprungsadresse.

   ![Verkaufskonfiguration - Optionen für die Versandursprungsadresse](./assets/shipping-origin.png){width="600" zoomable="yes"}

1. Klicken Sie auf **[!UICONTROL Save Config]**.

>[!NOTE]
>
>Commerce meldet UPS bei der Berechnung der Versandkosten nicht den vollständigen Bestellpreis. Dieses Verhalten kann nicht geändert werden.
