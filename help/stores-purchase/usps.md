---
title: United States Postal Service (USPS)
description: Erfahren Sie, wie Sie USPS als Versandunternehmen für Ihr Geschäft einrichten.
exl-id: c9601fb8-f0f9-484a-a2e1-d50ee0f2dbf0
feature: Shipping/Delivery
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '746'
ht-degree: 0%

---

# United States Postal Service (USPS)

Der US-Postdienst ist der unabhängige Postdienst der US-Regierung, der inländische und internationale Seeverkehrsdienstleistungen auf dem Land- und Luftweg anbietet.

## Schritt 1: Öffnen Sie ein USPS-Versandkonto.

Öffnen Sie ein Konto für [USPS Web Tools][1]. Nach Abschluss des Registrierungsprozesses erhalten Sie Ihre Benutzer-ID und eine URL zum USPS-Testserver.

Sie können auch ein [USPS Web Tools][1] -Konto öffnen. Nach Abschluss des Registrierungsprozesses erhalten Sie Ihre Benutzer-ID und eine URL zum USPS-Testserver. Weitere Informationen zu USPS Web Tools finden Sie in der [technischen Dokumentation][2].

## Schritt 2: USPS für Ihren Store aktivieren

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Delivery Methods]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL USPS]** .

   >[!NOTE]
   >
   >Heben Sie bei Bedarf zunächst das Kontrollkästchen **[!UICONTROL Use system value]** auf, um die folgenden Einstellungen wie beschrieben zu ändern.

1. Setzen Sie **[!UICONTROL Enabled for Checkout]** auf `Yes`.

1. Geben Sie bei Bedarf den Wert **[!UICONTROL Gateway URL]** ein, um auf die USPS Versandtarife zuzugreifen.

   >[!IMPORTANT]
   >
   >Ab dem 24. Juni 2021 werden die USPS Web Tools die Unterstützung für alle unsicheren HTTP-Endpunkte entfernen. Nach dieser Änderung schlagen alle Web Tools-API-Anfragen, die an einen unsicheren HTTP-Endpunkt gesendet werden, fehl. Stellen Sie sicher, dass Ihr **[!UICONTROL Gateway URL]** den sicheren HTTPS-Endpunkt verwendet.

   Das Feld ist standardmäßig vordefiniert und muss normalerweise nicht geändert werden.

1. Geben Sie für diese Versandmethode, die beim Checkout angezeigt wird, den Wert &quot;**[!UICONTROL Title]**&quot;ein.

1. Geben Sie die **[!UICONTROL User ID]** und die **[!UICONTROL Password]** für Ihr USPS-Konto ein.

1. Setzen Sie **[!UICONTROL Mode]** auf einen der folgenden Werte:

   - `Development` - Führt USPS in einer Testumgebung aus. Nachdem Sie USPS in einer Entwicklungsumgebung ausgeführt haben, stellen Sie sicher, dass Sie später zurückkehren und den Modus auf `Live` setzen.
   - `Live` - Führt USPS in einer Live-Produktionsumgebung aus.

## Schritt 3: Angabe der Verpackungsbeschreibung

1. Um zu bestimmen, wie die Reihenfolge verwaltet wird, wenn sie als mehrere Pakete gesendet wird, setzen Sie **[!UICONTROL Packages Request Type]** auf einen der folgenden Werte:

   - `Divide to Equal Weight` - (Eine Anfrage) Die Sendung mehrerer Pakete kann als eine Anfrage eingereicht werden, wenn die Pakete durch gleiche Gewichtung geteilt werden.
   - `Use Origin Weight` - (Multiple Requests) Mehrere Pakete müssen als separate Anfragen eingereicht werden, wenn die Ursprungsgewichtung als Grundlage für die Berechnung der Versandkosten verwendet wird.

1. Setzen Sie **[!UICONTROL Container]** auf den Verpackungstyp, der normalerweise zum Versand von für Ihren Laden bestellten Produkten verwendet wird.

1. Legen Sie die **[!UICONTROL Size]** des typischen Packages fest, das von Ihrem Store ausgeliefert wird.

1. Setzen Sie **[!UICONTROL Machinable]** auf einen der folgenden Werte:

   - `Yes` - Wenn Ihr typisches Paket von einem Computer verarbeitet werden kann.
   - `No` - Wenn Ihr typisches Paket manuell verarbeitet werden muss.

1. Geben Sie den **[!UICONTROL Maximum Package Weight]** entsprechend den Anforderungen des Netzbetreibers ein.

   ![USPS-Paketeinstellungen](../configuration-reference/sales/assets/delivery-methods-usps-packaging.png){width="600" zoomable="yes"}

## Schritt 4: Einrichten von Bearbeitungsgebühren

Die Bearbeitungsgebühr ist optional und erscheint als zusätzliche Gebühr, die zu den Versandkosten von DHL hinzukommt. Wenn Sie eine Bearbeitungsgebühr einbeziehen möchten, gehen Sie wie folgt vor:

1. Setzen Sie **[!UICONTROL Calculate Handling Fee]** auf eine der folgenden Methoden:

   - `Fixed`
   - `Percent`

1. Um festzustellen, wie die Bearbeitungsgebühr angewendet wird, setzen Sie **[!UICONTROL Handling Applied]** auf einen der folgenden Werte:

   - `Per Order`
   - `Per Package`

1. Geben Sie den Betrag des zu ladenden **[!UICONTROL Handling Fee]** ein.

   Um einen Prozentsatz einzugeben, verwenden Sie das Dezimalformat. Geben Sie beispielsweise &quot;`0.25`&quot;für 25 % ein.

   ![USPS-Bearbeitungsgebühr](../configuration-reference/sales/assets/delivery-methods-usps-handling-fee.png){width="600" zoomable="yes"}

## Schritt 5: Angeben der zulässigen Methoden und der entsprechenden Länder

1. Wählen Sie für **[!UICONTROL Allowed Methods]** jede USPS-Versandmethode aus, die Ihren Kunden zur Verfügung steht.

   Die Methoden werden beim Checkout unter USPS angezeigt. Um mehrere Methoden auszuwählen, halten Sie die Strg-Taste (PC) oder die Befehlstaste (Mac) gedrückt und klicken Sie auf jede Option.

1. Wenn Sie über USPS die Option [Kostenloses Versand](shipping-free.md) bereitstellen möchten, legen Sie die kostenlosen Versandoptionen fest:

   - Setzen Sie **[!UICONTROL Free Method]** auf die Methode, die Sie für den kostenlosen Versand verwenden möchten. Wenn Sie keinen kostenlosen Versand über USPS anbieten möchten, wählen Sie `None`.

   - Um einen Mindestbestellbetrag zu verlangen, der für eine kostenlose Lieferung mit USPS qualifiziert ist, setzen Sie **[!UICONTROL Enable Free Shipping Threshold]** auf `Enable`. Geben Sie dann den Mindestwert in **[!UICONTROL Free Shipping Amount Threshold]** ein.

1. Ändern Sie bei Bedarf die **[!UICONTROL Displayed Error Message]**.

   Dieses Textfeld ist mit einer Standardmeldung vordefiniert, Sie können jedoch eine andere Meldung eingeben, die angezeigt werden soll, wenn USPS nicht verfügbar ist.

   ![Zulässige USPS-Methoden](../configuration-reference/sales/assets/delivery-methods-usps-allowed-methods.png){width="600" zoomable="yes"}

1. Setzen Sie **[!UICONTROL Ship to Applicable Countries]** auf einen der folgenden Werte:

   - `All Allowed Countries` - Kunden aus allen in Ihrer Store-Konfiguration angegebenen [Ländern](../getting-started/store-details.md#country-options) können diese Bereitstellungsmethode verwenden.
   - `Specific Countries` - Wenn Sie diese Option auswählen, wird die Liste _Zu bestimmten Ländern verschicken_ angezeigt. Wählen Sie jedes Land in der Liste aus, in dem diese Versandmethode verwendet werden kann.

   ![VERWENDETE LÄNDER](../configuration-reference/sales/assets/delivery-methods-usps-countries.png){width="600" zoomable="yes"}

1. Setzen Sie **[!UICONTROL Show Method if Not Applicable]** auf einen der folgenden Werte:

   - `Yes` - Listet alle verfügbaren USPS-Versandmethoden während des Checkout auf, einschließlich Methoden, die nicht für die Sendung gelten.
   - `No` - Listet nur die USPS-Versandmethoden auf, die für die Sendung gelten.

1. Um eine Protokolldatei mit den Details zu USPS-Sendungen zu erstellen, die aus Ihrem Store durchgeführt wurden, setzen Sie **[!UICONTROL Debug]** auf `Yes`.

1. Geben Sie für **[!UICONTROL Sort Order]** eine Zahl ein, um die Sequenz zu bestimmen, in der USPS angezeigt wird, wenn es beim Checkout mit anderen Versandmethoden aufgeführt wird.

   `0` = first, `1` = second, `2` = third usw.

1. Klicken Sie auf **[!UICONTROL Save Config]**.


[1]: https://secure.shippingapis.com/registration/
[2]: https://www.usps.com/business/web-tools-apis/welcome.htm
