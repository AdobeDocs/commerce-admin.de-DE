---
title: FedEx
description: Erfahren Sie, wie Sie FedEx als Versandunternehmen für Ihr Geschäft einrichten.
exl-id: 75bb3ed1-3ae9-418a-be90-888046b28a7b
feature: Shipping/Delivery
source-git-commit: 50b44190a9568a8d6ad38ab29177904596569d75
workflow-type: tm+mt
source-wordcount: '849'
ht-degree: 0%

---

# FedEx

FedEx ist eines der weltweit größten Schifffahrtsunternehmen, das Luft-, Fracht- und Bodenschifffahrtsdienste mit mehreren Schwerpunkten anbietet.

![FedEx-Versandoptionen beim Checkout](./assets/storefront-checkout-shipping-fedex.png){width="700" zoomable="yes"}

>[!NOTE]
>
>FedEx kann [Dimensionsgewicht](carriers.md#dimensional-weight) um einige Versandtarife zu bestimmen. Adobe Commerce und Magento Open Source unterstützen jedoch nur eine gewichtsbasierte Berechnung der Versandkosten.

## Schritt 1: Registrieren Sie sich für die FedEx Web Services Production.

A [FedEx-Handelskonto][1] und die Registrierung für den Zugriff auf die FedEx Web Services Production ist erforderlich. Lesen Sie nach der Erstellung eines FedEx-Kontos die Seite mit den Produktionskontoinformationen und klicken Sie auf die Schaltfläche _Produktionsschlüssel abrufen_ unten auf der Seite zu registrieren und einen Schlüssel zu erhalten.

>[!NOTE]
>
>Stellen Sie sicher, dass Sie den Authentifizierungsschlüssel kopieren oder schreiben. Es ist erforderlich, FedEx in Ihren Commerce-Versandeinstellungen einzurichten.

## Schritt 2: FedEx für Ihren Store aktivieren

{{beta2-updates}}

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen **[!UICONTROL Delivery Methods]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL FedEx]** Abschnitt.

1. Satz **[!UICONTROL Enabled for Checkout]** nach `Yes`.

1. Für **[!UICONTROL Title]** Geben Sie einen Titel ein, der die FedEx-Versandmethode beim Checkout angibt.

1. Geben Sie die folgenden Informationen aus Ihrem FedEx-Konto ein:

   - **[!UICONTROL Account ID]**
   - **[!UICONTROL Meter Number]**
   - **[!UICONTROL Key]**
   - **[!UICONTROL Password]**

1. Wenn Sie eine FedEx-Sandbox eingerichtet haben und in der Testumgebung arbeiten möchten, legen Sie **[!UICONTROL Sandbox Mode]** nach `Yes`.

   >[!NOTE]
   >
   >Denken Sie daran, den Sandbox-Modus auf `No` wenn Sie bereit sind, Ihren Kunden FedEx als Versandmethode anzubieten.

   ![FedEx-Kontoeinstellungen](../configuration-reference/sales/assets/delivery-methods-fedex-account-settings.png){width="600" zoomable="yes"}

## Schritt 3: Paketbeschreibung und Bearbeitungsgebühr

1. Wählen Sie die **[!UICONTROL Packages Request Type]** zu der Option, die Ihre Voreinstellung am besten beschreibt, wenn Sie eine Bestellung in mehrere Sendungen aufteilen:

   - `Divide to equal weight (one request)`
   - `Use origin weight (few requests)`

1. Wählen Sie den Typ **[!UICONTROL Packaging]** wird normalerweise zum Versand von Produkten aus Ihrem Geschäft verwendet.

1. Satz **[!UICONTROL Dropoff]** zur Abholmethode, die für den Versand verwendet wird.

   - `Regular Pickup` - Wenn Sie eine große Anzahl von Sendungen haben, kann es kostengünstig sein, Vereinbarungen mit FedEx für regelmäßige Pickups zu treffen.

   - `Request Courier` - Sie müssen einen FedEx-Kurier anrufen und anfordern, um Sendungen abzuholen.

   - `Drop Box` - Sie müssen Sendungen an Ihrem nahe gelegenen FedEx-Ablagefeld abbrechen.

   - `Business Service Center` - Sie müssen den Versand in Ihrem FedEx Business Service Center einstellen.

   - `Station` - Sie müssen den Versand an Ihrem lokalen FedEx-Bahnhof abbrechen.

1. Satz **[!UICONTROL Weight Unit]** zur Maßeinheit, die in Ihrem Gebietsschema verwendet wird.

   - `Pounds`
   - `Kilograms`

1. Geben Sie die **[!UICONTROL Maximum Package Weight]** für FedEx-Sendungen zugelassen.

   Die standardmäßige maximale FedEx-Gewichtung beträgt 150 lbs. Weitere Informationen erhalten Sie von Ihrem Versandunternehmen. Der Standardwert wird empfohlen, es sei denn, Sie haben besondere Vereinbarungen mit FedEx getroffen. Siehe [Dimensionsgewicht](carriers.md#dimensional-weight) für weitere Informationen.

   ![FedEx-Paketeinstellungen](../configuration-reference/sales/assets/delivery-methods-fedex-packaging.png){width="600" zoomable="yes"}

1. Konfigurieren Sie die Optionen für die Bearbeitungsgebühr entsprechend Ihren Anforderungen.

   Die Bearbeitungsgebühr ist optional und ist beim Checkout nicht sichtbar. Wenn Sie eine Bearbeitungsgebühr einbeziehen möchten, gehen Sie wie folgt vor:

   - Satz **[!UICONTROL Calculate Handling Fee]**:

      - `Fixed Fee`
      - `Percentage`

   - Für **[!UICONTROL Handling Applied]** wählen Sie eine der folgenden Methoden für die Verwaltung von Gebühren:

      - `Per Order`
      - `Per Package`

   - Geben Sie die **[!UICONTROL Handling Fee]** entweder als `fixed` Betrag oder `percentage`, abhängig von der Berechnungsmethode.

1. Satz **[!UICONTROL Residential Delivery]** auf eine der folgenden Optionen zu setzen, je nachdem, ob Sie B2C (Business-to-Consumer) oder B2B (Business-to-Business) verkaufen.

   - `Yes` - für B2C-Wohnraumlieferungen.
   - `No` - für B2B-Wohnraumlieferungen.

   ![Einstellungen für FedEx-Gebühren](../configuration-reference/sales/assets/delivery-methods-fedex-handling-fee.png){width="600" zoomable="yes"}

## Schritt 4: Zulässige Methoden und anwendbare Länder

1. Satz **[!UICONTROL Allowed Methods]** für jede Versandmethode, die Sie anbieten möchten.

   Berücksichtigen Sie bei der Wahl der Methoden Ihr FedEx-Konto, die Häufigkeit und Größe Ihrer Sendungen und wenn Sie internationale Sendungen zulassen. Sie können beliebig viele oder beliebig wenige Methoden anbieten, z. B.:

   - Europa - Erste Priorität
   - Optionen für Bereitstellungstage: 1 Tag Fracht, 2 Tage Fracht, 2 Tage, 2 Tage AM, 3 Tage Freude
   - Interne Optionen - Express Saver, Ground, First, Overnight, Home Delivery, Standard Übernachtung
   - Internationale Optionen - Internationale Wirtschaft, Intl Economy Freight, International First, International Ground, International, Priority Intl
   - Prioritätsoptionen - Fracht, Priorität - Übernachtung
   - Smart Post-Wenn die Smart Post-Methode anbietet (geben Sie die **Hub-ID**)
   - Frachtoptionen - Fracht, Nationaler Güterverkehr

1. Wenn Sie eine [Kostenloser Versand](shipping-free.md) -Option durch FedEx, legen Sie die kostenlosen Versandoptionen fest.

   - Satz **[!UICONTROL Free Method]** zu der Methode, die Sie für den kostenlosen Versand verwenden möchten. Wenn Sie keinen kostenlosen Versand über FedEx anbieten möchten, wählen Sie `None`.

   - Um einen Mindestbestellbetrag zu verlangen, der eine Bestellung für den kostenlosen Versand mit FedEx qualifiziert, setzen Sie **[!UICONTROL Enable Free Shipping Threshold]** nach `Enable`. Geben Sie dann den Mindestwert in **[!UICONTROL Free Shipping Amount Threshold]**.

   Diese Einstellung ähnelt der für die standardmäßige Free Shipping-Methode, wird jedoch beim Checkout im FedEx-Abschnitt angezeigt, sodass Kunden wissen, welche Methode für ihre Bestellung verwendet wird.

1. Ändern Sie bei Bedarf die **[!UICONTROL Displayed Error Message]**.

   Dieses Textfeld enthält eine Standardmeldung, Sie können jedoch eine andere Meldung eingeben, die angezeigt werden soll, wenn FedEx nicht verfügbar ist.

   ![Zustellmethoden für FedEx-Administratoren](../configuration-reference/sales/assets/delivery-methods-fedex-delivery-methods.png){width="600" zoomable="yes"}

1. Satz **[!UICONTROL Ship to Applicable Countries]**:

   - `All Allowed Countries` - Kunden von allen [Länder](../getting-started/store-details.md#country-options) Diese in Ihrer Store-Konfiguration angegebene Versandmethode kann verwendet werden.

   - `Specific Countries` - Wenn Sie diese Option wählen, wird die _Schiff in bestimmte Länder_ angezeigt. Wählen Sie jedes Land in der Liste aus, in dem diese Versandmethode verwendet werden kann.

1. Wenn Sie ein Protokoll aller Kommunikation zwischen Ihrem Store und dem FedEx-System speichern möchten, legen Sie **[!UICONTROL Debug]** nach `Yes`.

1. Satz **[!UICONTROL Show Method if Not Applicable]**:

   - `Yes` - Zeigt alle FedEx-Versandmethoden für Kunden an, unabhängig von ihrer Verfügbarkeit.
   - `No` - Zeigt nur die FedEx-Versandmethoden an, die für die Bestellung gelten.

1. Für **[!UICONTROL Sort Order]** Geben Sie eine Zahl ein, um die Sequenz zu bestimmen, in der FedEx angezeigt wird, wenn es beim Checkout mit anderen Versandmethoden aufgeführt wird.

   `0` = first, `1` = Sekunde, `2` = drittes Element usw.

1. Klicken **[!UICONTROL Save Config]**.

   ![FedEx-anwendbare Länder](../configuration-reference/sales/assets/delivery-methods-fedex-applicable-countries.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Bei der Berechnung der Versandkosten meldet Commerce immer den vollen Bestellpreis an FedEx. Dieses Verhalten kann nicht geändert werden.

[1]: https://www.fedex.com/login/web/jsp/contactInfo1.jsp
