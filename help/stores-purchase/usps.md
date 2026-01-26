---
title: United States Postal Service (USPS)
description: Erfahren Sie, wie Sie USPS als Versanddienstleister für Ihr Geschäft einrichten.
exl-id: c9601fb8-f0f9-484a-a2e1-d50ee0f2dbf0
feature: Shipping/Delivery
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '763'
ht-degree: 0%

---

# United States Postal Service (USPS)

Der United States Postal Service ist ein unabhängiger Postdienst der Regierung der Vereinigten Staaten, der inländische und internationale Schifffahrtsdienste auf dem Land- und Luftweg anbietet.

## Schritt 1: USPS Versandkonto eröffnen

Öffnen Sie ein [USPS Web Tools](https://secure.shippingapis.com/registration/)-Konto. Nach Abschluss des Registrierungsprozesses erhalten Sie Ihre Benutzer-ID und eine URL zum USPS-Testserver.

Sie können auch ein Konto [USPS Web Tools](https://secure.shippingapis.com/registration/) eröffnen. Nach Abschluss des Registrierungsprozesses erhalten Sie Ihre Benutzer-ID und eine URL zum USPS-Testserver. Weitere Informationen zu USPS Web Tools finden Sie in der [technischen Dokumentation](https://www.usps.com/business/web-tools-apis/welcome.htm).

## Schritt 2: USPS für Ihren Shop aktivieren

{{$include /help/_includes/usps-api-type-configuration-note.md}}

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Delivery Methods]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL USPS]** .

   >[!NOTE]
   >
   >Deaktivieren Sie bei Bedarf zunächst das Kontrollkästchen **[!UICONTROL Use system value]** , um die folgenden Einstellungen wie beschrieben zu ändern.

1. Legen Sie **[!UICONTROL Enabled for Checkout]** auf `Yes` fest.

1. Setzen Sie **[!UICONTROL USPS Type]** auf `USPS Rest APIs`, wenn Sie die USPS-REST-API verwenden.

   Wenn Sie die USPS Web Tools-API verwenden, setzen Sie **[!UICONTROL USPS Type]** auf `USPS Web Tools API`.

1. Geben Sie bei Bedarf die **[!UICONTROL Gateway URL]** ein, um auf USPS Versandtarife zuzugreifen.

   Das Feld ist standardmäßig voreingestellt und muss normalerweise nicht geändert werden.

1. Geben Sie eine **[!UICONTROL Title]** für diese Versandart ein, die während des Checkouts angezeigt wird.

1. Verwenden Sie die von USPS bereitgestellten Anmeldeinformationen, um die folgenden Felder auszufüllen:

   Wenn Sie die USPS-REST-APIs verwenden, müssen Sie die folgenden Anmeldeinformationen angeben:

   - **[!UICONTROL Consumer Key]**
   - **[!UICONTROL Consumer Secret]**
   - **[!UICONTROL Pricing Options]**

   Wenn Sie die USPS Web Tools API verwenden, müssen Sie die folgenden Anmeldeinformationen angeben:

   - **[!UICONTROL User ID]**
   - **[!UICONTROL Password]**

1. Legen Sie **[!UICONTROL Mode]** auf eine der folgenden Einstellungen fest:

   - `Development` - Führt USPS in einer Testumgebung aus. Nachdem Sie USPS in einer Entwicklungsumgebung ausgeführt haben, stellen Sie sicher, dass Sie später zurückkehren und Mode auf `Live` setzen.
   - `Live` - USPS wird in einer Live-Produktionsumgebung ausgeführt.

## Schritt 3: Vervollständigen Sie die Verpackungsbeschreibung

1. Um zu bestimmen, wie die Reihenfolge verwaltet wird, wenn sie als mehrere Pakete gesendet wird, legen Sie **[!UICONTROL Packages Request Type]** auf eine der folgenden Einstellungen fest:

   - `Divide to Equal Weight` - (Eine Anfrage) Die Sendung mehrerer Pakete kann als eine Anfrage eingereicht werden, wenn die Pakete durch das gleiche Gewicht geteilt werden.
   - `Use Origin Weight` - (Mehrere Anfragen) Mehrere Pakete müssen als separate Anfragen eingereicht werden, wenn die Ursprungsgewichtung als Grundlage für die Berechnung der Versandkosten verwendet wird.

1. Legen Sie **[!UICONTROL Container]** auf die Art der Verpackung fest, die normalerweise verwendet wird, um Produkte zu versenden, die für Ihr Geschäft bestellt wurden.

1. Legen Sie die **[!UICONTROL Size]** des typischen Pakets fest, das aus Ihrem Geschäft ausgeliefert wird.

1. Legen Sie **[!UICONTROL Machinable]** auf eine der folgenden Einstellungen fest:

   - `Yes` - Wenn Ihr typisches Paket von einem Computer verarbeitet werden kann.
   - `No` - Wenn Ihr typisches Paket manuell verarbeitet werden muss.

1. Geben Sie die **[!UICONTROL Maximum Package Weight]** entsprechend den Anforderungen des Spediteurs ein.

   ![USPS-Verpackungseinstellungen](../configuration-reference/sales/assets/delivery-methods-usps-packaging.png){width="600" zoomable="yes"}

## Schritt 4: Einrichten von Bearbeitungsgebühren

Die Bearbeitungsgebühr ist optional und erscheint als zusätzliche Gebühr, die zu den DHL Versandkosten hinzugerechnet wird. Wenn Sie eine Bearbeitungsgebühr einbeziehen möchten, gehen Sie wie folgt vor:

1. Legen Sie **[!UICONTROL Calculate Handling Fee]** auf eine der folgenden Methoden fest:

   - `Fixed`
   - `Percent`

1. Um zu bestimmen, wie die Bearbeitungsgebühr angewendet wird, **[!UICONTROL Handling Applied]** Sie eine der folgenden Einstellungen ein:

   - `Per Order`
   - `Per Package`

1. Geben Sie den Betrag der zu belastenden **[!UICONTROL Handling Fee]** ein.

   Verwenden Sie das Dezimalformat, um einen Prozentsatz einzugeben. Geben Sie beispielsweise `0.25` für 25 % ein.

   ![USPS-Bearbeitungsgebühr](../configuration-reference/sales/assets/delivery-methods-usps-handling-fee.png){width="600" zoomable="yes"}

## Schritt 5: Zugelassene Methoden und anwendbare Länder angeben

1. Wählen Sie **[!UICONTROL Allowed Methods]** jede USPS-Versandart, die Ihren Kunden zur Verfügung stehen soll.

   Die Methoden werden beim Checkout unter USPS angezeigt. Zur Auswahl mehrerer Methoden halten Sie die Strg-Taste (PC) bzw. die Befehlstaste (Mac) gedrückt und klicken auf die einzelnen Optionen.

1. Wenn Sie über USPS eine Option für [kostenlosen Versand](shipping-free.md) bereitstellen möchten, legen Sie die Optionen für den kostenlosen Versand fest:

   - Legen Sie **[!UICONTROL Free Method]** auf die Methode fest, die Sie für den kostenlosen Versand verwenden möchten. Wenn Sie keinen kostenlosen Versand über USPS anbieten möchten, wählen Sie `None`.

   - Um einen Mindestbestellbetrag zu verlangen, der für einen kostenlosen Versand mit USPS geeignet ist, setzen Sie **[!UICONTROL Enable Free Shipping Threshold]** auf `Enable`. Geben Sie dann den Mindestwert in **[!UICONTROL Free Shipping Amount Threshold]** ein.

1. Ändern Sie bei Bedarf die **[!UICONTROL Displayed Error Message]**.

   Dieses Textfeld ist mit einer Standardmeldung vorbelegt, Sie können jedoch eine andere Nachricht eingeben, die angezeigt werden soll, wenn USPS nicht mehr verfügbar ist.

   ![USPS - Zulässige Methoden](../configuration-reference/sales/assets/delivery-methods-usps-allowed-methods.png){width="600" zoomable="yes"}

1. Legen Sie **[!UICONTROL Ship to Applicable Countries]** auf eine der folgenden Einstellungen fest:

   - `All Allowed Countries` - Kunden aus allen [Ländern](../getting-started/store-details.md#country-options) die in Ihrer Store-Konfiguration angegeben sind, können diese Versandmethode verwenden.
   - `Specific Countries` - Wenn Sie diese Option wählen, wird die Liste _Versand an bestimmte Länder_ angezeigt. Wählen Sie jedes Land in der Liste aus, in dem diese Versandmethode verwendet werden kann.

   ![USPS-Länder](../configuration-reference/sales/assets/delivery-methods-usps-countries.png){width="600" zoomable="yes"}

1. Legen Sie **[!UICONTROL Show Method if Not Applicable]** auf eine der folgenden Einstellungen fest:

   - `Yes` - Listet alle verfügbaren USPS Versandmethoden während des Checkouts auf, einschließlich Methoden, die nicht für die Sendung gelten.
   - `No` - Listet nur die USPS-Versandmethoden auf, die für die Sendung gelten.

1. Um eine Protokolldatei mit den Details der USPS-Sendungen aus Ihrem Geschäft zu erstellen, setzen Sie **[!UICONTROL Debug]** auf `Yes`.

1. Geben Sie **[!UICONTROL Sort Order]** eine Zahl ein, um die Reihenfolge zu bestimmen, in der USPS angezeigt wird, wenn sie beim Checkout mit anderen Versandmethoden aufgelistet wird.

   `0` = First, `1` = Second, `2` = Third usw.

1. Klicken Sie auf **[!UICONTROL Save Config]**.


<!-- Last updated from includes: 2025-11-26 10:55:00 -->
