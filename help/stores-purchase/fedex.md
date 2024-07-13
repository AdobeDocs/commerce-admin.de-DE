---
title: FedEx
description: Erfahren Sie, wie Sie FedEx als Versandunternehmen für Ihr Geschäft einrichten.
exl-id: 75bb3ed1-3ae9-418a-be90-888046b28a7b
feature: Shipping/Delivery
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '881'
ht-degree: 0%

---

# FedEx

FedEx ist eines der weltweit größten Schifffahrtsunternehmen, das Luft-, Fracht- und Bodenschifffahrtsdienste mit mehreren Schwerpunkten anbietet.

![FedEx-Versandoptionen beim Checkout](./assets/storefront-checkout-shipping-fedex.png){width="700" zoomable="yes"}

>[!NOTE]
>
>FedEx kann [dimensionale Gewichtung](carriers.md#dimensional-weight) verwenden, um einige Versandraten zu bestimmen. Adobe Commerce und Magento Open Source unterstützen jedoch nur eine gewichtsbasierte Berechnung der Versandkosten.

## Schritt 1: Registrieren Sie sich für die FedEx Web Services Production.

Ein [FedEx-Handelskonto][1] und eine Registrierung für den Zugriff auf die FedEx-Web-Services-Produktion sind erforderlich. Lesen Sie nach der Erstellung eines FedEx-Kontos die Seite mit den Produktionskontoinformationen und klicken Sie dann unten auf der Seite auf den Link _Produktionsschlüssel abrufen_ , um sich zu registrieren und einen Schlüssel zu erhalten.

>[!NOTE]
>
>Stellen Sie sicher, dass Sie den Authentifizierungsschlüssel kopieren oder schreiben. Es ist erforderlich, FedEx in Ihren Versandeinstellungen für Commerce einzurichten.

## Schritt 2: FedEx für Ihren Store aktivieren

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Delivery Methods]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL FedEx]** .

1. Setzen Sie **[!UICONTROL Enabled for Checkout]** auf `Yes`.

1. Geben Sie für **[!UICONTROL Title]** einen Titel ein, der die FedEx-Versandmethode beim Checkout angibt.

1. Geben Sie die folgenden Informationen aus Ihrem FedEx-Konto ein:

   - **[!UICONTROL Account ID]**
   - **[!UICONTROL Api Key]**
   - **[!UICONTROL Secret Key]**

1. Wenn Sie eine FedEx-Sandbox eingerichtet haben und in der Testumgebung arbeiten möchten, setzen Sie **[!UICONTROL Sandbox Mode]** auf `Yes`.

   >[!NOTE]
   >
   >Denken Sie daran, den Sandbox-Modus auf `No` festzulegen, wenn Sie bereit sind, Ihren Kunden FedEx als Versandmethode anzubieten.

   ![FedEx-Kontoeinstellungen](../configuration-reference/sales/assets/delivery-methods-fedex-account-settings.png){width="600" zoomable="yes"}

## Schritt 3: Paketbeschreibung und Bearbeitungsgebühren

1. Setzen Sie **[!UICONTROL Pickup Type]** auf die für Sendungen verwendete Abholmethode.

   - `DropOff at Fedex Location` - (Standard) Gibt an, dass Sie Sendungen auf Ihrer lokalen FedEx-Station abbrechen.
   - `Contact Fedex to Schedule` - Gibt an, dass Sie sich an FedEx wenden, um eine Abholung anzufordern.
   - `Use Scheduled Pickup` - Gibt an, dass die Sendung im Rahmen einer regelmäßigen geplanten Abholung aufgenommen wird.
   - `On Call` - Gibt an, dass die Abholung durch Aufruf von FedEx geplant ist.
   - `Package Return Program` - Gibt an, dass die Sendung vom FedEx Ground Package Retouren Program aufgenommen wird.
   - `Regular Stop` - Gibt an, dass die Sendung im regelmäßigen Pickup-Zeitplan aufgenommen wird.
   - `Tag` - Gibt an, dass die Sendungs-Abholung spezifisch für eine Express-Tag- oder Ground-Aufruf-Tag-Abrufanforderung ist. Dies gilt nur für einen Rücksendeschlüssel.

1. Wählen Sie für &quot;**[!UICONTROL Packages Request Type]**&quot;den Anfragetyp aus, der Ihre Voreinstellungen beim Aufteilen einer Bestellung in mehrere Sendungen am besten beschreibt:

   - `Divide to equal weight (one request)`
   - `Use origin weight (few requests)`

1. Wählen Sie für **[!UICONTROL Packaging]** den Typ der FedEx-Verpackung aus, die Sie normalerweise zum Versand von Produkten aus Ihrem Geschäft verwenden.

1. Setzen Sie **[!UICONTROL Weight Unit]** auf die Maßeinheit, die in Ihrem Gebietsschema verwendet wird.

   - `Pounds`
   - `Kilograms`

1. Geben Sie die für FedEx-Sendungen zulässige **[!UICONTROL Maximum Package Weight]** ein.

   Die standardmäßige maximale FedEx-Gewichtung beträgt 150 lbs. Weitere Informationen erhalten Sie von Ihrem Versandunternehmen. Der Standardwert wird empfohlen, es sei denn, Sie haben besondere Vereinbarungen mit FedEx getroffen. Weitere Informationen finden Sie unter [Dimensional weight](carriers.md#dimensional-weight) .

   ![FedEx-Paketeinstellungen](../configuration-reference/sales/assets/delivery-methods-fedex-packaging.png){width="600" zoomable="yes"}

1. Konfigurieren Sie die Optionen für die Bearbeitungsgebühr entsprechend Ihren Anforderungen.

   Die Bearbeitungsgebühr ist optional und ist beim Checkout nicht sichtbar. Wenn Sie eine Bearbeitungsgebühr einbeziehen möchten, gehen Sie wie folgt vor:

   - Legen Sie **[!UICONTROL Calculate Handling Fee]** fest:

      - `Fixed Fee`
      - `Percentage`

   - Wählen Sie für **[!UICONTROL Handling Applied]** eine der folgenden Methoden für die Verwaltung von Bearbeitungsgebühren:

      - `Per Order`
      - `Per Package`

   - Geben Sie den **[!UICONTROL Handling Fee]** je nach Berechnungsmethode entweder als `fixed` Betrag oder als `percentage` ein.

1. Setzen Sie **[!UICONTROL Residential Delivery]** auf einen der folgenden Werte, je nachdem, ob Sie B2C (Business-to-Consumer) oder B2B (Business-to-Business) verkaufen.

   - `Yes` - für B2C-Wohnungslieferungen.
   - `No` - für B2B-Wohnraumlieferungen.

   ![Einstellungen für FedEx-Gebühren ](../configuration-reference/sales/assets/delivery-methods-fedex-handling-fee.png){width="600" zoomable="yes"}

## Schritt 4: Zulässige Methoden und anwendbare Länder

1. Setzen Sie **[!UICONTROL Allowed Methods]** auf jede Versandmethode, die Sie anbieten möchten.

   Berücksichtigen Sie bei der Wahl der Methoden Ihr FedEx-Konto, die Häufigkeit und Größe Ihrer Sendungen und wenn Sie internationale Sendungen zulassen. Sie können beliebig viele oder beliebig wenige Methoden anbieten, z. B.:

   - Europa - Erste Priorität
   - Optionen für Bereitstellungstage: 1 Tag Fracht, 2 Tage Fracht, 2 Tage, 2 Tage AM, 3 Tage Freude
   - Interne Optionen - Express Saver, Ground, First, Overnight, Home Delivery, Standard Übernachtung
   - Internationale Optionen - Internationale Wirtschaft, Intl Economy Freight, International First, International Ground, International, Priority Intl
   - Prioritätsoptionen - Fracht, Priorität - Übernachtung
   - Smart Post - Wenn die Smart Post-Methode angeboten wird (geben Sie die **Hub-ID** ein)
   - Frachtoptionen - Fracht, Nationaler Güterverkehr

1. Wenn Sie über FedEx die Option [Free Shipping](shipping-free.md) bereitstellen möchten, legen Sie die kostenlosen Versandoptionen fest.

   - Setzen Sie **[!UICONTROL Free Method]** auf die Methode, die Sie für den kostenlosen Versand verwenden möchten. Wenn Sie keinen kostenlosen Versand über FedEx anbieten möchten, wählen Sie `None`.

   - Setzen Sie **[!UICONTROL Enable Free Shipping Threshold]** auf `Enable`, um einen Mindestbestellbetrag zu verlangen, der für eine kostenlose Lieferung mit FedEx qualifiziert ist. Geben Sie dann den Mindestwert in **[!UICONTROL Free Shipping Amount Threshold]** ein.

   Diese Einstellung ähnelt der für die standardmäßige Free Shipping-Methode, wird jedoch beim Checkout im FedEx-Abschnitt angezeigt, sodass Kunden wissen, welche Methode für ihre Bestellung verwendet wird.

1. Ändern Sie bei Bedarf die **[!UICONTROL Displayed Error Message]**.

   Dieses Textfeld enthält eine Standardmeldung, Sie können jedoch eine andere Meldung eingeben, die angezeigt werden soll, wenn FedEx nicht verfügbar ist.

   ![Zugelassene Bereitstellungsmethoden für FedEx](../configuration-reference/sales/assets/delivery-methods-fedex-delivery-methods.png){width="600" zoomable="yes"}

1. Legen Sie **[!UICONTROL Ship to Applicable Countries]** fest:

   - `All Allowed Countries` - Kunden aus allen in Ihrer Store-Konfiguration angegebenen [Ländern](../getting-started/store-details.md#country-options) können diese Bereitstellungsmethode verwenden.

   - `Specific Countries` - Wenn Sie diese Option auswählen, wird die Liste _Zu bestimmten Ländern verschicken_ angezeigt. Wählen Sie jedes Land in der Liste aus, in dem diese Versandmethode verwendet werden kann.

1. Wenn Sie ein Protokoll aller Kommunikation zwischen Ihrem Store und dem FedEx-System aufbewahren möchten, setzen Sie **[!UICONTROL Debug]** auf `Yes`.

1. Legen Sie **[!UICONTROL Show Method if Not Applicable]** fest:

   - `Yes` - Zeigt alle FedEx-Versandmethoden an Kunden an, unabhängig von ihrer Verfügbarkeit.
   - `No` - Zeigt nur die FedEx-Versandmethoden an, die für die Bestellung gelten.

1. Geben Sie für **[!UICONTROL Sort Order]** eine Zahl ein, um die Sequenz zu bestimmen, in der FedEx angezeigt wird, wenn es beim Checkout mit anderen Versandmethoden aufgeführt wird.

   `0` = first, `1` = second, `2` = third usw.

1. Klicken Sie auf **[!UICONTROL Save Config]**.

   ![FedEx Anwendbare Länder](../configuration-reference/sales/assets/delivery-methods-fedex-applicable-countries.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Commerce meldet bei der Berechnung der Versandkosten immer den vollen Bestellpreis an FedEx. Dieses Verhalten kann nicht geändert werden.

[1]: https://www.fedex.com/login/web/jsp/contactInfo1.jsp
