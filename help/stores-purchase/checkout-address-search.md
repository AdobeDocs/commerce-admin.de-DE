---
title: Adresssuche an der Kasse
description: Erfahren Sie, wie Sie die Adresssuche an der Kasse in Ihrem Geschäft einbeziehen.
exl-id: 8153c456-0848-4bb4-8deb-8219323344ed
feature: Checkout
TQID: https://experienceleague.adobe.com/fMrmhB3-kGvDKNBnI1PCUhndVN0RhQprpZGB6rjfo8o
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 434
ht-degree: 0%

---

# Adresssuche an der Kasse

{{ee-feature}}

Ihre Kunden können viele gespeicherte Adressen und Informationen in ihrem Adressbuch haben, insbesondere regelmäßige, wiederkehrende Kunden oder Unternehmen, die mehrere Bestellungen und Versandorte eingeben. Das Anzeigen vieler Adressen kann das Laden und Laden des Checkouts erheblich verlangsamen und zu einem negativen Einkaufserlebnis führen. Es wird empfohlen, die Adresssuche für Ihre Website zu aktivieren und zu konfigurieren, um die Reaktionsgeschwindigkeit des Checkouts zu erhöhen.

>[!NOTE]
>
>Die Adresssuche ist standardmäßig nicht aktiviert. Sie können diese Funktion so konfigurieren, dass sie die Funktionalität auf Ihrer Site enthält.

Wenn diese Funktion aktiviert ist und die Anzahl der gespeicherten Adressen des Kunden das konfigurierte Limit erreicht oder überschreitet, wird in den Schritten _Versand_ und _Überprüfen und Zahlungen_ nur eine Adresse angezeigt (der Standard). Der Kunde kann die ausgewählte Adresse ändern, indem er auf **Adresse ändern** klickt und dann nach der richtigen Adresse nach Stadt, Bundesland, Straße oder Postleitzahl sucht. Diese Funktion unterstützt auch die Adressauswahl für den Checkout der Geschenkregistrierung.

![Checkout mit gespeicherten Versandadressen angezeigt](./assets/storefront-checkout-address-search.png){width="700" zoomable="yes"}

Wenn der Kunde keine standardmäßige Versandadresse hat, wird auf der Seite _Versand_ angezeigt _Keine Adresse ausgewählt_. In diesem Fall muss der Kunde auf **Adresse ändern** klicken, um eine gespeicherte Adresse auszuwählen, oder auf **Neue Adresse** klicken, um eine Adresse hinzuzufügen und auszuwählen, bevor der Checkout fortgesetzt wird. Wenn der Kunde keine standardmäßige Rechnungsadresse hat, wird auf der Seite _Überprüfen und Zahlungen_ die für den Versand ausgewählte Adresse zusammen mit der Option _Adresse ändern_ angezeigt.

![Checkout ohne ausgewählte Adresse](./assets/storefront-checkout-address-search-no-default.png){width="600" zoomable="yes"}

## Gesperrte Adresse für Anführungszeichen suchen

![Adobe Commerce B2B](../assets/b2b.svg) (nur in Adobe Commerce B2B verfügbar)

Die Aktivierung der Adresssuche wirkt sich auch auf den Checkout für Bestellungen aus, die aus Angeboten erstellt werden, bei denen die Anzahl der gespeicherten Adressen des Kunden das konfigurierte Limit erreicht oder überschreitet. Wenn das Angebot abgeschlossen ist und der Kunde zur Kasse wechselt, wird nur die ausgewählte Lieferadresse angezeigt. Auf der Seite wird außerdem eine Meldung angezeigt, dass die Lieferadresse gesperrt ist und nur im Angebot geändert werden kann.

![Lieferadresse für ein Angebot gesperrt](./assets/quote-checkout-shipping-address-locked.png){width="600" zoomable="yes"}

## Adresssuche aktivieren

1. Navigieren Sie in _Admin_-Seitenleiste zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Checkout]**.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) den Abschnitt **[!UICONTROL Checkout Options]** .

   ![Konfiguration - Checkout-Optionen](./assets/checkout-checkout-options.png){width="700" zoomable="yes"}

   Eine ausführliche Beschreibung jeder dieser Konfigurationseinstellungen finden Sie unter [Checkout-Optionen](../configuration-reference/sales/checkout.md#checkout-options) im _Konfigurationsreferenzhandbuch_.

1. Legen Sie **[!UICONTROL Enable Address Search]** auf `Yes` fest.

1. Um den Schwellenwert für die Einbeziehung der Adresssuchfunktion festzulegen, stellen Sie die Option **[!UICONTROL Number of Customer Addresses Limit]** ein.

   Deaktivieren Sie bei Bedarf das Kontrollkästchen **[!UICONTROL Use system value]** , um diese Änderung vorzunehmen.

   Wenn die Anzahl der gespeicherten Adressen dieses Limit erreicht oder überschreitet, zeigt die Seite entweder die Standardadresse (wenn der Kunde eine hat) oder _Keine Adresse ausgewählt_ mit der Option _Adresse ändern_ an. Das standardmäßige Limit ist `10`.

1. Klicken Sie auf **[!UICONTROL Save Config]**.
