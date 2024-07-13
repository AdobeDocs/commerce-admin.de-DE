---
title: Adressensuche beim Checkout
description: Erfahren Sie, wie Sie die Adresssuche beim Checkout in Ihren Store einbeziehen.
exl-id: 8153c456-0848-4bb4-8deb-8219323344ed
feature: Checkout
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 0%

---

# Adressensuche beim Checkout

{{ee-feature}}

Ihre Kunden könnten über viele gespeicherte Adressen und Informationen in ihrem Adressbuch verfügen, insbesondere über regelmäßige, wiederkehrende Kunden oder Unternehmen, die mehrere Bestellungen und Versandstandorte eingeben. Das Anzeigen vieler Adressen kann das Laden und die Verarbeitung von Kassen erheblich verlangsamen und zu einem negativen Einkaufserlebnis führen. Um die Reaktionsfähigkeit des Checkout zu erhöhen, wird empfohlen, die Adressensuche für Ihre Site zu aktivieren und zu konfigurieren.

>[!NOTE]
>
>Die Adresssuche ist standardmäßig nicht aktiviert. Sie können diese Funktion so konfigurieren, dass sie die Funktionalität auf Ihrer Site einbezieht.

Wenn diese Funktion aktiviert ist und die Anzahl der gespeicherten Adressen des Kunden das konfigurierte Limit erreicht oder überschreitet, zeigen die Schritte _Versand_ und _Überprüfung und Zahlungen_ nur eine Adresse an (Standardeinstellung). Der Kunde kann die ausgewählte Adresse ändern, indem er auf &quot;**Adresse ändern**&quot;klickt und dann nach der richtigen Adresse nach Stadt, Bundesland, Straße oder ZIP sucht. Diese Funktion unterstützt auch die Adressenauswahl für den Checkout aus der Geschenkregistrierung.

![Checkout mit angezeigten gespeicherten Versandadressen](./assets/storefront-checkout-address-search.png){width="700" zoomable="yes"}

Wenn der Kunde keine standardmäßige Versandadresse hat, wird auf der Seite _Versand_ der Eintrag _Keine Adresse ausgewählt_ angezeigt. In diesem Fall muss der Kunde auf **Adresse ändern** klicken, um eine gespeicherte Adresse auszuwählen, oder auf **Neue Adresse** klicken, um eine Adresse hinzuzufügen und auszuwählen, bevor er mit dem Checkout fortfahren kann. Wenn der Kunde keine standardmäßige Abrechnungsadresse hat, zeigt die Seite _Überprüfung und Zahlungen_ die für den Versand ausgewählte Adresse zusammen mit der Option _Adresse ändern_ an.

![Checkout ohne ausgewählte Adresse ](./assets/storefront-checkout-address-search-no-default.png){width="600" zoomable="yes"}

## Gesperrte Adresssuche nach Anführungszeichen

![Adobe Commerce B2B](../assets/b2b.svg) (nur bei Adobe Commerce B2B verfügbar)

Die Aktivierung der Adressensuche wirkt sich auch auf den Checkout für Bestellungen aus, die aus Anführungszeichen erstellt werden, bei denen die Anzahl der gespeicherten Adressen des Kunden das konfigurierte Limit erreicht oder überschreitet. Wenn das Angebot abgeschlossen ist und der Kunde zum Checkout übergeht, wird nur die ausgewählte Lieferadresse angezeigt. Auf der Seite wird auch eine Meldung angezeigt, dass die Versandadresse gesperrt ist und nur im Angebot geändert werden kann.

![Versandadresse gesperrt für ein Anführungszeichen](./assets/quote-checkout-shipping-address-locked.png){width="600" zoomable="yes"}

## Adressensuche aktivieren

1. Wechseln Sie in der Seitenleiste _Admin_ zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich den Wert **[!UICONTROL Sales]** und wählen Sie **[!UICONTROL Checkout]** aus.

1. Erweitern Sie ![Erweiterungsauswahl](../assets/icon-display-expand.png) im Abschnitt **[!UICONTROL Checkout Options]** .

   ![Konfiguration - Checkout-Optionen](./assets/checkout-checkout-options.png){width="700" zoomable="yes"}

   Eine ausführliche Beschreibung der einzelnen Konfigurationseinstellungen finden Sie unter [Checkout-Optionen](../configuration-reference/sales/checkout.md#checkout-options) im _Konfigurationshandbuch_.

1. Setzen Sie **[!UICONTROL Enable Address Search]** auf `Yes`.

1. Um den Schwellenwert für die Aufnahme der Funktion zur Adressensuche anzugeben, legen Sie die Option **[!UICONTROL Number of Customer Addresses Limit]** fest.

   Deaktivieren Sie bei Bedarf das Kontrollkästchen **[!UICONTROL Use system value]** , um diese Änderung vorzunehmen.

   Wenn die Anzahl der gespeicherten Adressen des Kunden diese Grenze erreicht oder überschreitet, zeigt die Seite entweder die Standardadresse (wenn der Kunde eine hat) oder _Keine Adresse ausgewählt_ mit der Option _Adresse ändern_ an. Der Standardwert ist `10`.

1. Klicken Sie auf **[!UICONTROL Save Config]**.
