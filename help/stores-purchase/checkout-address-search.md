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

Wenn diese Funktion aktiviert ist und die Anzahl der gespeicherten Adressen des Kunden das konfigurierte Limit erreicht oder überschreitet, wird die _Versand_ und _Überprüfung und Zahlungen_ -Schritte zeigen nur eine Adresse an (Standard). Der Kunde kann die ausgewählte Adresse ändern, indem er auf **Adresse ändern** und dann nach der richtigen Adresse nach Stadt, Bundesland, Straße oder Postleitzahl suchen. Diese Funktion unterstützt auch die Adressenauswahl für den Checkout aus der Geschenkregistrierung.

![Checkout mit gespeicherten Versandadressen angezeigt](./assets/storefront-checkout-address-search.png){width="700" zoomable="yes"}

Wenn der Kunde keine standardmäßige Lieferadresse hat, wird die _Versand_ Seitenanzeigen _Keine Adresse ausgewählt_. In diesem Fall muss der Kunde auf **Adresse ändern** zum Auswählen einer gespeicherten Adresse oder klicken Sie auf **Neue Adresse** , um eine Adresse hinzuzufügen und auszuwählen, bevor Sie mit dem Checkout fortfahren. Wenn der Kunde keine standardmäßige Abrechnungsadresse hat, wird die _Überprüfung und Zahlungen_ auf der Seite wird die für den Versand ausgewählte Adresse zusammen mit der _Adresse ändern_ -Option.

![Checkout ohne gewählte Adresse](./assets/storefront-checkout-address-search-no-default.png){width="600" zoomable="yes"}

## Gesperrte Adresssuche nach Anführungszeichen

![Adobe Commerce B2B](../assets/b2b.svg) (Nur bei Adobe Commerce B2B verfügbar)

Die Aktivierung der Adressensuche wirkt sich auch auf den Checkout für Bestellungen aus, die aus Anführungszeichen erstellt werden, bei denen die Anzahl der gespeicherten Adressen des Kunden das konfigurierte Limit erreicht oder überschreitet. Wenn das Angebot abgeschlossen ist und der Kunde zum Checkout übergeht, wird nur die ausgewählte Lieferadresse angezeigt. Auf der Seite wird auch eine Meldung angezeigt, dass die Versandadresse gesperrt ist und nur im Angebot geändert werden kann.

![Versandadresse gesperrt für ein Angebot](./assets/quote-checkout-shipping-address-locked.png){width="600" zoomable="yes"}

## Adressensuche aktivieren

1. Im _Admin_ Seitenleiste, navigieren Sie zu **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Erweitern Sie im linken Bereich **[!UICONTROL Sales]** und wählen **[!UICONTROL Checkout]**.

1. Erweitern ![Erweiterungsauswahl](../assets/icon-display-expand.png) die **[!UICONTROL Checkout Options]** Abschnitt.

   ![Konfiguration - Checkout-Optionen](./assets/checkout-checkout-options.png){width="700" zoomable="yes"}

   Eine ausführliche Beschreibung der einzelnen Konfigurationseinstellungen finden Sie unter [Checkout-Optionen](../configuration-reference/sales/checkout.md#checkout-options) im _Konfigurationshandbuch_.

1. Satz **[!UICONTROL Enable Address Search]** nach `Yes`.

1. Um den Schwellenwert für die Aufnahme der Funktion zur Adressensuche anzugeben, legen Sie die **[!UICONTROL Number of Customer Addresses Limit]** -Option.

   Falls erforderlich, löschen Sie die **[!UICONTROL Use system value]** aktivieren, um diese Änderung vorzunehmen.

   Wenn die Anzahl der gespeicherten Adressen des Kunden diese Grenze erreicht oder überschreitet, zeigt die Seite entweder die Standardadresse an (wenn der Kunde eine hat) oder _Keine Adresse ausgewählt_ mit dem _Adresse ändern_ -Option. Die Standardbeschränkung beträgt `10`.

1. Klicks **[!UICONTROL Save Config]**.
